---
area: trabajo
status: 🟡 en marcha
priority: alta
updated: 2026-08-21
---

# Sistema de reports mensuales para Manuel

## Objetivo
Dar visibilidad real del trabajo de Adrián ante Manuel. Manuel prefiere todo por escrito/impreso — el email es poco eficaz con él.

## Próxima acción
Seguir usando `/report-comercial` cada semana — tercer uso end-to-end completado el 21 ago (con los tres comerciales de Aura a la vez). 3 semanas guardadas (8 jul, 27 jul, 21 ago), siguen faltando las intermedias — cuando haya 3-4 semanas seguidas, montar el primer report mensual real.

## Acciones / Tareas
- [x] Arrancar el tracker semanal (2026-07-08, primera semana con Aura activa) — `knowledge/mpc-group/reports-comerciales/`
- [x] Codificar el informe semanal como skill (`/report-comercial`, `.claude/commands/report-comercial.md`) — cabecera corporativa con logo real de MPC Group (`knowledge/mpc-group/assets/mpc-group-logo.jpg`) y colores exactos del logo (12 jul 2026)
- [x] Probar `/report-comercial` con datos reales de una semana nueva (27 jul 2026 — primer caso end-to-end con clasificación de calidad de visitas por Oskar, exportado también a PDF en `Desktop/MPC Group/Comité dirección/`)
- [ ] Aclarar con Eduardo el descuadre entre visitas reportadas por el equipo y visitas registradas en Dynamics/Power BI (persiste: el 27/07 el equipo reportó 21 visitas vs 5 en Power BI, rangos de fecha no coinciden)
- [ ] Validar formato del informe semanal con Manuel
- [ ] Diseñar propuesta de formato del report mensual (escrito/impreso) — pendiente de acumular 3-4 semanas

## Informe de tracción para el socio inversor de Manuel — Aura + Pórtico (21 ago 2026)
Nuevo tipo de documento: Manuel pidió un informe que él mismo comparte con su socio inversor/capitalista, combinando Aura Condomina y Pórtico Plaza II (hasta ahora el `informe-inversores` solo existía para un proyecto, ver el del 8 jul de Aura). Construido sobre el reporte semanal (`2026-08-21.md`) pero con datos agregados y **sin nombres de clientes ni detalles personales** — mismo criterio que el informe de julio.

Contenido final tras varias rondas de ajuste de Adrián: 8 ventas reales en Aura (14,8% del objetivo de 54, en 6 semanas) y 10 en Pórtico con el mismo protagonismo visual; ratio visita/venta destacado como señal de calidad de proyecto; de dónde vienen las 18 ventas combinadas (83,3% red propia); 10 de esas 18 son internacionales pese a que Aura no se ha lanzado fuera todavía; pipeline de seguimiento por proyecto sin nombres; hito de financiación CaixaBank de Pórtico. Sin nota de confidencialidad al pie, con logo real de MPC Group arriba.

**Guardado en `knowledge/mpc-group/reports-comerciales/2026-08-21-informe-inversor-aura-portico.html/.pdf`. Enviado por Adrián — confirmado.**

**Lección de formato aprendida esta sesión:** los PDFs exportados con Chrome headless no deben partir una tabla/caja a mitad entre dos páginas — aplicar `break-inside: avoid` por defecto en las plantillas nuevas y comprobar siempre el PDF renderizado, no solo el HTML (memoria guardada en el sistema de Bruce: `feedback_pdf-evitar-saltos-pagina-a-mitad-bloque.md`).

## Informe ad hoc — Leads/campañas Aura/Pórtico/Nature Views (17 ago 2026)
Manuel pidió por email una evaluación detallada de leads, visitas, ventas, inversión y coste por lead/visita/venta de las tres campañas activas desde el lanzamiento de Aura (2 jul), distinto del report semanal habitual. Construido cruzando 2 PDFs de Meta Ads Manager + Power BI/Dynamics, con 3 huecos de medición explicitados en el propio informe (periodo no homogéneo, sin atribución venta→campaña específica, Aura sin desglose por sub-campaña). Guardado en `~/bruce/knowledge/mpc-group/reports-comerciales/2026-08-17-leads-campanas-aura-portico-nature-views-manuel.html/.pdf`. **No enviado a Manuel todavía** — Adrián lo revisa primero.

## Notas
- Objetivo de fondo: que Manuel vea el trabajo real de Adrián, no solo resultados.
- El tracker semanal es el input para este report — se guarda un archivo por semana con datos manuales del equipo + Power BI, y una tabla resumen para ver evolución sin reconstruir nada.
- Las "visitas programadas" (ej. 15 para la semana del 8 jul) son un dato que reporta el equipo directamente, no algo que se pueda cruzar con Power BI.
- Colores de marca MPC Group (muestreados del logo real, no aproximados): navy `#0E3C89`, azul `#43BBED`, ámbar `#FFB71C`. Reutilizables en cualquier otro documento corporativo.
