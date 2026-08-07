---
area: trabajo
status: 🟡 en marcha
priority: alta
updated: 2026-08-07
---

# WhatsApp Business API — equipo comercial bloqueado

## Problema
El equipo comercial está siendo bloqueado en WhatsApp normal. Volumen actual: 100+ mensajes/día a leads que dejan sus datos en formularios (Idealista, Meta, web) — canal crítico de comunicación con leads.

## Causa
WhatsApp normal (o WhatsApp Business app) no soporta ese volumen sin baneos — es la causa nº1 de bloqueos en inmobiliarias. La solución real es migrar a la API oficial de WhatsApp Business (Cloud API) vía un proveedor certificado (BSP), usando una plantilla de opt-in pre-aprobada como primer mensaje a cada lead nuevo.

## Estado
Eduardo (IT) propone **Saysimple**. Investigación propia (Bruce) hecha el 6 ago: comparativa completa de proveedores en `~/bruce/knowledge/mpc-group/whatsapp-api-comparativa-proveedores.md`.

**Hallazgo clave:** ninguno de los candidatos (Saysimple, 360dialog, Wati, Respond.io) tiene integración nativa documentada con Microsoft Dynamics (el CRM de MPC). Existe un conector específico — **Inogic WhatsApp4Dynamics** — pensado exactamente para esto, sin precio público. La vía nativa de Microsoft (Azure Communication Services) tiene fricción real en España por la verificación de negocio de Meta.

## Plantillas de WhatsApp (7 ago 2026)
Set completo de 3 plantillas listas en `~/bruce/knowledge/mpc-group/whatsapp-plantillas-leads.md`: opt-in inicial, seguimiento (24-48h sin respuesta) y confirmación de cita/visita. Genéricas para los tres canales (Idealista, Meta Ads, web), solo en español, redactadas como categoría UTILITY para no caer en tarifas/condiciones de MARKETING. Listas para enviar a aprobación de Meta en cuanto haya proveedor — el contenido no depende de si se elige Saysimple u otra alternativa.

## Próxima acción
1. Pedir a Eduardo, antes de decidir: (1) cotización real de Saysimple para el volumen actual y cómo conecta exactamente con Dynamics, y (2) una alternativa de contraste (Inogic WhatsApp4Dynamics + un BSP barato como 360dialog) para comparar coste total (licencia + desarrollo de integración).
2. En cuanto haya proveedor: enviar las 3 plantillas a aprobación de Meta.
3. Decidir con el equipo comercial (María, Oskar, Oliver) qué nombre va en las variables de comercial de cada plantilla.
