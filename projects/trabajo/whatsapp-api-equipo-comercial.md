---
area: trabajo
status: 🟡 en marcha
priority: alta
updated: 2026-08-06
---

# WhatsApp Business API — equipo comercial bloqueado

## Problema
El equipo comercial está siendo bloqueado en WhatsApp normal. Volumen actual: 100+ mensajes/día a leads que dejan sus datos en formularios (Idealista, Meta, web) — canal crítico de comunicación con leads.

## Causa
WhatsApp normal (o WhatsApp Business app) no soporta ese volumen sin baneos — es la causa nº1 de bloqueos en inmobiliarias. La solución real es migrar a la API oficial de WhatsApp Business (Cloud API) vía un proveedor certificado (BSP), usando una plantilla de opt-in pre-aprobada como primer mensaje a cada lead nuevo.

## Estado
Eduardo (IT) propone **Saysimple**. Investigación propia (Bruce) hecha el 6 ago: comparativa completa de proveedores en `~/bruce/knowledge/mpc-group/whatsapp-api-comparativa-proveedores.md`.

**Hallazgo clave:** ninguno de los candidatos (Saysimple, 360dialog, Wati, Respond.io) tiene integración nativa documentada con Microsoft Dynamics (el CRM de MPC). Existe un conector específico — **Inogic WhatsApp4Dynamics** — pensado exactamente para esto, sin precio público. La vía nativa de Microsoft (Azure Communication Services) tiene fricción real en España por la verificación de negocio de Meta.

## Próxima acción
Pedir a Eduardo, antes de decidir: (1) cotización real de Saysimple para el volumen actual y cómo conecta exactamente con Dynamics, y (2) una alternativa de contraste (Inogic WhatsApp4Dynamics + un BSP barato como 360dialog) para comparar coste total (licencia + desarrollo de integración).
