---
area: bruce
status: 🟡 en marcha
priority: alta
updated: 2026-09-10
---

# Bruce — Fase 1 (codificar los agentes)

## Objetivo
Los agentes de `~/bruce/agents/*.md` existen como documentos de especificación (qué hace cada uno, cuándo activarlo) pero **no están codificados/activos todavía**. Hay que implementarlos uno a uno para que Bruce los use de verdad. Empezaron siendo 7; el 18 jul 2026 se añadió un 8º (`health.md`), fuera del plan original de David pero surgido de una necesidad real de Adrián (cumple 45 años el 23 jul, carrera de 42K el 3 de octubre).

## Próxima acción
`agents/comercial.md` e `internacional.md` están cerrados (o casi). `health.md` nace ya con su primer pilar documentado (la carrera de 42K). **Decidido (10 sep 2026): la próxima sesión se dedica entera a `personas.md`.** Estado a esa fecha: capa de Equipo ya con 8 perfiles (`knowledge/personas/equipo/`, incluidas las 2 incorporaciones de esa semana — María José y Virginia), competidores ya cerrado (`knowledge/real-estate/competitors.md`, reescrito 11 ago). **Los dos huecos reales que quedan:** clientes clave (solo `vadim.md` documentado) y red de contactos (solo 2 entradas: Open Club, WTG) — ahí es donde entra la próxima sesión.

## Acciones / Tareas
- [ ] `agents/mercado.md` — Análisis de mercado, precios, hipotecas, Euribor, solares
- [x] `agents/internacional.md` — Estrategia USA, red europea, nómadas digitales, family offices ← **COMPLETO** (12 jul 2026): pautas de prospección de agencias europeas (`knowledge/mpc-group/red-internacional-agencias.md`), plan USA New Orleans/Tampa noviembre (`knowledge/usa-market/plan-tampa-noviembre.md`), nómadas digitales enlazado a `/leads` sin duplicar, family offices (`knowledge/mpc-group/family-offices-inversores.md`, genuinamente sin empezar salvo segmento AER Global), vuelos Alicante refrescado a mano + GitHub Action roto desactivado.
- [ ] `agents/marketing.md` — Contenido, LinkedIn, Instagram, YouTube, marca
- [~] `agents/comercial.md` — Power BI, CRM Dynamics, leads, agencias, formación equipo ← **CASI COMPLETO**: `/report-comercial`, `/agencias`, `/reunion-equipo`, `/leads` codificados (12 jul 2026). Formaciones: módulo 01 creado (`knowledge/formacion/01-proceso-venta-cliente-internacional.md`), quedan 03/04/05 (02-Dynamics aparcado igual que CRM).
- [x] `agents/briefing.md` — Noticias diarias, NFL, fútbol, pulso del mercado — skill `/news` (14 jun 2026)
- [~] `agents/personas.md` — Equipo, clientes clave, red de contactos, competidores ← Equipo (8 perfiles) y competidores cerrados. **Próxima sesión (decidido 10 sep 2026): clientes clave (solo Vadim documentado) y red de contactos (solo Open Club + WTG) — los dos huecos que quedan.**
- [~] `agents/personal.md` — Bolsa, películas, mejora de inglés (la dieta se movió a `health.md` el 18 jul para no duplicar)
- [~] `agents/health.md` — **NUEVO** (18 jul 2026), no estaba en los 7 originales. Pilar 1 (carrera 42K Mula→Caravaca) documentado con plan completo en `knowledge/salud/maraton-2026-plan.md`. Pilar 2 (dieta) con el enfoque heredado de `personal.md`. Pilar 3 (sueño, chequeos médicos) sin empezar.

## Notas
- Se hará poco a poco, no todos de golpe — dentro de cada agente, mejor una rebanada fina que funcione que codificarlo entero de golpe.
- Estos 7 agentes son la base de la que parten las capacidades de [[fase-2]] y [[fase-3]] — conviene tenerlos codificados antes de añadir esas capacidades.
- Fuente: `~/bruce/CLAUDE.md` — Hoja de Ruta de Bruce, Fase 1 (que la describe como "activa ahora", pero en la práctica los agentes aún no están codificados).
