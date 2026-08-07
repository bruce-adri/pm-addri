---
area: personal
status: 🟡 en marcha
priority: baja
updated: 2026-07-18
---

# Bruce crea playlists en Apple Music

## Objetivo
Que Bruce pueda crear y poblar listas de reproducción en Apple Music de Adrián (Mac + iPhone vía iCloud) a partir de un criterio dado (ocasión, estado de ánimo, evento), sin que Adrián tenga que buscar canción a canción.

## Estado real (18 jul 2026)
**No funciona todavía de forma automática.** Se investigaron tres vías en la sesión del 18 de julio:

1. **AppleScript nativo (`osascript`)** — permiso de Terminal ya concedido (Automatización → Música), funciona perfecto para leer/crear/reorganizar playlists y canciones **que ya están en la biblioteca** de Adrián. Pero Apple cerró hace años el acceso por script al catálogo de streaming (el objeto `source "iTunes Store"` es vestigial, `search` devuelve siempre 0 resultados). **No sirve para añadir canciones nuevas del catálogo.**
2. **Shortcuts.app (Atajos)** — tiene acciones nativas pensadas para esto ("Search Music" + "Add to Playlist"), y hay un CLI (`shortcuts run`) para invocarlas desde Terminal. Es la vía "oficial" de Apple. **Se creó el atajo `Bruce Add Song`** (busca en Apple Music → añade a la playlist `Bruce Buzón`), pero al ejecutarlo da siempre `Error de MPErrorDomain 0` — confirmado que no es cuenta/suscripción (Music.app reproduce el catálogo sin problema) ni permisos (Música con acceso en Ajustes). Es un bug conocido y no resuelto de la integración Atajos↔Música en macOS.
3. **UI-scripting vía Accesibilidad (`System Events`)** — permiso de Accesibilidad concedido a Terminal. Se consiguió controlar el buscador de Music.app por completo (escribir la consulta, ejecutar, leer resultados reales). Pero el botón "Añadir a la biblioteca" de cada resultado no tiene nombre accesible (solo aparece al hacer hover), y el menú contextual (clic derecho / `AXShowMenu`) sí contiene el item correcto ("Añadir a playlist") pero consultarlo cuelga temporalmente System Events — frágil y con riesgo real de dejar la app en un estado raro. Se abandonó por seguridad.

## Vía recomendada — MusicKit API (pendiente, sesión futura dedicada)
La solución robusta de verdad: la API oficial de Apple Music (MusicKit).
- Requiere cuenta de **Apple Developer Program (99$/año)**.
- Bruce genera una clave MusicKit (JWT firmado) — la clave privada va en `.env`, nunca en código ni en `knowledge/`.
- Adrián autoriza el acceso **una vez** (flujo tipo login con su Apple ID) para obtener un Music User Token.
- Con eso, búsqueda de catálogo + añadir a biblioteca/playlist por API REST — sin bugs de Shortcuts ni fragilidad de UI-scripting.

**Esto queda aparcado hasta que Adrián lo priorice explícitamente** — no es gratis (cuenta de pago) ni instantáneo (enrollment + verificación de Apple puede tardar días).

## Convención adoptada
Cualquier playlist que cree Bruce lleva el nombre pedido por Adrián + sufijo **`(Bruce)`** al final, para distinguirlas a simple vista de las suyas. Ej: `Argentina 0 - España 1 (Bruce)`.

## Mientras tanto — flujo manual funcional
1. Adrián busca cada canción en Music.app y la añade directamente a la playlist **`Bruce Buzón`** (ya creada, sirve de buzón de entrada reutilizable).
2. Cuando están todas, Bruce coge esa lista tal cual por AppleScript, la reordena/renombra a la playlist final con sufijo `(Bruce)`, y vacía `Bruce Buzón` para la próxima vez.

## Caso de uso de esta sesión — Final Argentina-España (19 jul 2026)
Playlist pedida para ver la final del Mundial. Primer intento con géneros genéricos (reggaetón/flamenco pop) rechazado por Adrián — "no soy de este estilo". Se le pidió inspiración a sus propias playlists (`Himnos`, `Holanda 26`, `2025`): perfil real = rock clásico/indie (Killers, Kings of Leon, Arctic Monkeys, The Clash, Foo Fighters), country-americana (Morgan Wallen, Teddy Swims, Zach Bryan, Luke Combs) e indie español con pegada (Nolasco, El Rumbo, Diego de Rubeo). Con eso se construyó una segunda lista con temas *distintos* a los que ya tiene (para no repetir, solo usar de inspiración):

1. Arctic Monkeys — R U Mine?
2. Kings of Leon — Use Somebody
3. The Killers — When You Were Young
4. Oasis — Don't Look Back in Anger
5. Kasabian — Fire
6. The White Stripes — Seven Nation Army
7. Franz Ferdinand — Take Me Out
8. Vetusta Morla — Copenhague
9. Love of Lesbian — Allí Donde Solíamos Gritar
10. Zach Bryan — Something in the Orange
11. Chris Stapleton — Tennessee Whiskey
12. Bailey Zimmerman — Rock and a Hard Place
13. Old Dominion — Written in the Sand

**Pendiente al cierre de la sesión:** Adrián tenía que añadir estas 13 a `Bruce Buzón` a mano; no confirmó "listo" antes de cerrar. Retomar al inicio de la próxima sesión — si ya las añadió, crear `Argentina 0 - España 1 (Bruce)` inmediatamente (la final es el domingo 19 jul).

## Próxima acción
1. Confirmar con Adrián si añadió las 13 canciones a `Bruce Buzón` → si sí, crear la playlist final ya.
2. Cuando Adrián priorice la vía robusta, retomar MusicKit (cuenta Developer + clave + autorización).
