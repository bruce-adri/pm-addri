---
area: personal
status: 🟢 activo
priority: baja
updated: 2026-07-24
---

# Integrar con Calendario de Apple

## Objetivo
Bruce lee y escribe en el Calendario de Apple de Adrián (compartido Mac/iPhone vía iCloud): avisar de citas importantes, y crear eventos/recordatorios (con alerta) para fechas importantes de `~/pm` que aún no estén agendadas.

## Próxima acción
Ninguna pendiente — capacidad operativa. Usar en sesiones cuando sea relevante (revisar agenda, cruzar deadlines de `~/pm` con el calendario).

## Acciones / Tareas
- [x] Aclarar el caso de uso prioritario → lectura + escritura, con foco en avisos/recordatorios de fechas importantes
- [x] Confirmar permiso de Calendario para Terminal (ya concedido)
- [x] Probar lectura de eventos (osascript) — OK, agenda del 15/06 leída correctamente
- [x] Probar creación/borrado de evento de prueba (osascript) — OK

## Notas
- Mecanismo y protocolo documentados en `CLAUDE.md` → sección "Calendario de Apple".
- Bruce nunca crea/borra eventos sin confirmación de Adrián.
- Ideas futuras (sin desarrollar): aviso proactivo aunque Adrián no abra sesión ese día — requeriría un agente programado (`/schedule`) aparte.

## Agenda semanal (24 jul 2026)
Construida con Adrián una plantilla de semana tipo (Benejúzar lunes+miércoles, Aura Condomina + comida agencias jueves, Alicante viernes, martes flexible) — guardada en `~/bruce/knowledge/mpc-group/agenda-semanal-adrian.md`. Los bloques fijos ya están creados como eventos recurrentes semanales con alerta en el calendario "Trabajo", a partir de la semana del 27/07/2026.

**Bug encontrado y solución:** el comando `delete` de AppleScript sobre eventos del calendario "Trabajo" (iCloud) **no persiste** — se ejecuta sin error pero el evento sigue existiendo, incluso tras relanzar Calendar.app. En cambio, `set` (modificar propiedades) sí funciona y persiste. Workaround validado: en vez de borrar un evento sobrante, vaciar su `recurrence` (`set recurrence of e to ""`) y renombrarlo para dejarlo claro — así deja de repetirse sin necesidad de borrarlo. Aplicar este workaround la próxima vez que haga falta eliminar un evento por script.
