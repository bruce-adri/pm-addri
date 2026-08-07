---
area: trabajo
status: 🟡 en marcha
priority: alta
updated: 2026-07-29
---

# Proceso Comercial y Tecnología — con Cris

## Objetivo
Rediseñar el proceso comercial completo de MPC (lead a postventa) incorporando IA y automatización, con Cris (consultora externa de RRHH/organización, ahora liderando la parte tecnológica de procesos) y Manuel. Reunión de arranque: **20 de julio de 2026**.

## Qué se ha preparado (16 jul 2026)
- **Customer journey completo** (10 fases, lead a postventa) con huecos del proceso marcados y un caso real (reserva sin señal de Jose Manuel, 8 jul). Artifact: journey-cliente-completo.
- **Rediseño con IA**: la IA informa 24/7 (autoservicio), el comercial entra tarde con contexto y se dedica a cerrar, el contrato se genera solo al cobrar la señal.
- **Agencias colaboradoras**: regla de mailing automático (cada 10 días o cada 4 ventas, lo que ocurra primero) + boceto de dashboard único (sustituye el Excel) — con los 4 datos que hoy faltan (país, fecha de última visita, dirección del contacto, ventas por proyecto).
- **Dashboard diario para Manuel y Adrián**: vista compartida con alertas (no informe mensual) — leads, tiempo de respuesta, visitas, ofertas, reservas/contratos, ventas, pagos, agencias.
- **Informe final en PDF (11 páginas)** para Manuel y Cris: `~/Desktop/Bruce/Informe - El Futuro del Proceso Comercial MPC (Manuel y Cris).pdf`. Incluye narrativa del sector, el journey completo, el dashboard, próximos pasos con Cris, y objetivos de impacto (+30% conversión, +45% satisfacción, mismo equipo con más volumen) **etiquetados explícitamente como metas a validar, no datos demostrados** — con el embudo real de Dynamics (16 visitas → 1 oportunidad → 0 ventas, 5 semanas) como línea base.

## Revisión del informe (17 jul 2026, feedback de Adrián)
Segunda pasada sobre el PDF antes de la reunión — 7 cambios aplicados y PDF regenerado (v2, en `data/informe-proceso-comercial-cris/`, pendiente de mover a `~/Desktop/Bruce/` por Adrián — Bruce no tiene permiso de escritura ahí):
1. Añadido el dato de **1.599 leads de Aura Condomina en el primer mes completo**.
2. Añadida la futura **vertical de alquileres de Aura Condomina** en la postventa (ingresos recurrentes).
3. Corregido el canal Idealista (ya no se dice "el que mejor funciona") + añadido RRSS (funciona bien para venta de unidad/inversión concreta) + matizado el canal de agencias (más selectivas, acciones propias más allá de inauguraciones).
4. Resuelto en el documento: el lead español/nacional de Aura ahora se reparte entre Oskar y Oliver (decisión real, no solo de redacción).
5. Añadido el flujo completo de un lead (email+WhatsApp automático → llamada del comercial → visita virtual o presencial → registro en CRM), con el dato de Pórtico Plaza II (70% ventas online) y un aviso de riesgo de spam/bloqueo de WhatsApp por Meta.
6. Eliminada del documento la sección de "línea base real" (embudo 16→1→0 de Dynamics) — **sigue siendo el dato real que usamos internamente para validar si se cumplen los objetivos de +30%/+45%; solo se quitó de lo que ve Manuel/Cris.**
7. Renombrado "Próximos pasos con Cris" a **"Sugerencias de futuro"**, dejando explícito que el informe es un borrador de trabajo y que los próximos pasos concretos se definen en la reunión, no antes.

## Segunda revisión (17 jul 2026, tarde) — feedback de Oskar
Oskar envió 5 mejoras de CRM/Dynamics basadas en su uso diario (prioridad automática de llamadas, autocompletar datos de la promoción, filtrar números inválidos, WhatsApp iniciado por el cliente en vez de por el comercial, gestión automática de visitas). Añadidas como página nueva del informe ("Mejoras propuestas por el equipo comercial", atribución genérica al equipo, no al nombre — mismo criterio que con Pascual), con especial mención: el punto de WhatsApp iniciado por el cliente **resuelve directamente** el riesgo de bloqueo por spam de Meta señalado en la página 6 — se enlazaron ambas páginas. El informe pasa a 12 páginas.

## Sistemática del proceso comercial — construida el 24 jul 2026, para la reunión del 30 jul
De la reunión del 20/07 (proceso/procedimiento, con Cris, Oskar y Edu) salieron notas manuscritas de Adrián con huecos claros: automatizar doc de reserva→contrato, email genérico de contratos/reservas, sistemática de envío al cliente, plazos (1 semana nacional / 2 semanas internacional de reserva a contrato), y sobre todo que **las incidencias no se miran y no viven solo en CRM** (una parte en Excel aparte). Adrián se comprometió a entregar su parte antes de la reunión del 30/07.

Con Bruce se construyó **`~/bruce/knowledge/mpc-group/reports-comerciales/2026-07-24-sistematica-proceso-comercial.html`** (+ PDF, también copiado a `~/Desktop/MPC Group/`): sistemática completa de las 6 fases del cliente (Lead→Oportunidad, Oportunidad→Reserva, Reserva→Contrato, Contrato→Firma Escritura —dividida en Inspección previa/Financiación/Escritura—, Durante la Compra/Reformas, Postventa), con pasos numerados, responsable de cada paso y condiciones, al mismo nivel de detalle que el proceso de gestión de lead ya existente de Cris. Se basó en tres fuentes: el proceso de Cris (Fase 1, sin tocar), los procedimientos antiguos heredados de plantilla "mahersol" (PC03 venta directa/agencias, inspección pre-entrega, financiación, reformas, PC06 postventa — extraídos de un .doc que no se podía leer directamente, usando `qlmanage` para sacar los diagramas como imágenes/PDF), y las notas manuscritas del 20/07.

Principio rector explícito en el documento: el Departamento Comercial (Adrián) es responsable de **todo** contacto con el cliente, de punta a punta — confirmar entrada de dinero, enviar contrato, coordinar firma, resolver incidencias en postventa. Ningún tramo se transfiere a otro departamento sin su seguimiento.

**Primera versión rechazada por Adrián** por ser demasiado resumida frente al detalle real del proceso de Cris — se reconstruyó con pasos numerados y responsables extraídos de los diagramas antiguos, no solo titulares de sección. Lección para futuras sistemáticas: iguala el nivel de detalle del documento de referencia que ya existe, no lo resumas.

## Ampliación de la sistemática (29 jul 2026, día antes de la reunión)

Adrián revisó el documento del 24/07 y pidió 6 añadidos, todos incorporados:
- **Fase 2:** visita a piso piloto ahora presencial o virtual (dato: 65% de ventas de Pórtico Plaza II cerradas online) + nuevo paso de **aprobación de Dirección Comercial/General** para cualquier negociación fuera de estándar (forma de pago, precio, mobiliario).
- **Fase 3:** nuevo paso de email de bienvenida a la familia MPC Group tras la firma de contrato.
- **Fase 5:** bloque de 4 emails automáticos durante la construcción (recordatorio de pago, aviso de impago, confirmación de pago, envío de aval bancario) — plantillas ya hechas desde Administración, pendientes de que Adrián las revise.
- **Fase 4a:** ventana de 10 días tras la revisión conjunta para que el cliente siga detectando incidencias antes de firmar la recepción.
- **Fase 4c:** nota sobre aprovechar la firma ante notario para conocer mejor al cliente (comida con Dirección si el perfil lo justifica).
- **Fase 6 / cierre:** caja nueva de servicio a cliente inversor (Aura, Pórtico Plaza II) — gestión de alquiler y apoyo en reventa futura, con aviso de confirmar capacidad operativa real antes de comprometerlo por escrito.

Se añadió también un **checklist de emails** al final del documento (9 emails del proceso, con fase, responsable y badge de color: verde = plantilla lista, ámbar = existe pero pendiente de revisión). De los 9, solo 3 están definitivamente listos (bienvenida, envío de contrato, contacto de lead); los otros 6 ya existen (hechos desde Administración/Postventa) pero Adrián tiene que revisarlos.

**Control de calidad antes de enviarlo:** en la primera pasada de edición se perdió por error la caja-resumen "Para cerrar el 30/07" — detectado y restaurado (ampliado con todos los pendientes nuevos) antes de dar el documento por bueno. También se corrigió una contradicción (email de contrato marcado a la vez como "listo" y como "pendiente") y una errata de numeración ya preexistente del 24/07 (una fase remitía a "Fase 4b" en vez de "Fase 4c"). Documento y PDF actualizados en `knowledge/mpc-group/reports-comerciales/2026-07-24-sistematica-proceso-comercial.html/.pdf`, copiado también a `~/Desktop/MPC Group/` — commiteado y subido a GitHub.

Quedan 2 decisiones explícitamente marcadas como "pendiente de definir el 30/07" dentro del propio documento: el umbral de importe para exigir también Dirección General en la aprobación de negociaciones (Fase 2), y si hay tope de vueltas de revisión dentro de la ventana de 10 días (Fase 4a).

## Resultado de la reunión del 30 jul — 12 acciones repartidas por área
La reunión con Manuel y Cris del 30/07 sí tuvo resultado (contradice el registro anterior de "sin resultado" — corregido 3 ago). Salieron 12 acciones concretas con responsable:

1. Homogeneizar el formato de los modelos de contrato y reserva — **Oihana**
2. Exportar la lista completa de campos del CRM y compartirla para revisión por área — **Eduardo y equipo**
3. Definir y crear nuevos campos en el CRM y ver cuáles serán obligatorios — **Eduardo y equipo**
4. Crear un repositorio estructurado para la documentación del cliente — **Eduardo y equipo**
5. Enviar documento a Laberit con puntos a tratar — **Eduardo**
6. Revisar automatismos a realizar y cómo desactivar/activar + esquema de notificaciones internas por rol — **Eduardo y equipo**
7. Diseñar un panel de control en el CRM con tareas, hitos y fechas de vencimiento — **Eduardo y equipo**
8. **Estandarizar el proceso, workflow y manual comercial adaptable por promoción — Adrián**
9. **Inventariar, revisar y estandarizar todas las notificaciones al cliente, definiendo textos, canales y momentos (línea de tiempo) — Adrián**
10. **Marketing: preparar borrador de guías visuales de acompañamiento para clientes — Adrián**
11. Abordar con Etosa los problemas en su servicio de postventa para exigir mejoras — **Producción y gerencia**
12. Definir plazos internos para la resolución de incidencias postventa — **Producción y gerencia**

**De estas, 3 son responsabilidad directa de Adrián (8, 9, 10) y son lo que hay que tener listo para la reunión del jueves 6 de agosto por la mañana con Cris.**

- **#8 (workflow/manual comercial por promoción) — ✅ cerrado 4 ago 2026.** `knowledge/mpc-group/reports-comerciales/2026-07-24-sistematica-proceso-comercial.html/.pdf` ampliado con la sección "Cómo Varía por Promoción" (reparto de equipo y cuello de botella en Aura, 70% online + servicio a inversor en Pórtico Plaza II, key-ready sin obra + sin servicio a inversor en Nature Views). De paso se corrigió el dato de Pórtico (65%→70% online, confirmado por Adrián) y se limpiaron las referencias muertas a "pendiente de definir el 30/07" (esas decisiones no se cerraron ese día, siguen abiertas).
- **#9 (inventario de notificaciones al cliente) — ✅ cerrado 4 ago 2026.** Documento nuevo `knowledge/mpc-group/reports-comerciales/2026-08-04-inventario-notificaciones-cliente.html/.pdf`: línea de tiempo de las 9 notificaciones (fase, canal, momento exacto, responsable) + texto propuesto para cada una. Las 6 marcadas "revisar" son propuesta de Bruce, no lo que ya existe en Administración/Postventa — **pendiente de cotejar** antes de darlas por definitivas. 4 plazos nuevos propuestos (recordatorio 7 días antes, impago 3 días después, aval 5 días hábiles, escritura 15 días antes) sin acuerdo previo, para validar el 6/08.
- **#10 (guías visuales de acompañamiento) — ✅ cerrado 5 ago 2026, en 3 versiones.** Enfoque del 5/08 ejecutado: mockup HTML/PDF de Bruce (6 fases del cliente, contenido real, colores de marca) como base para que Jonathan haga el diseño final en Canva. Construidas 3 versiones en `knowledge/mpc-group/reports-comerciales/` (+ `~/Desktop/Bruce/`): `2026-08-05-guia-visual-acompanamiento-cliente-mockup.html/.pdf` (trabajo interno, notas de diseño), `2026-08-05-guia-visual-acompanamiento-cliente.html/.pdf` (limpia, para reunión/Jonathan) y `2026-08-05-guia-cliente-para-enviar.html/.pdf` (apta para cliente real: sin plazos sin validar, con hueco de personalización y contacto del comercial). Extra pedido sobre la marcha: `2026-08-05-timeline-cliente.html/.pdf`, mapa visual de las 6 fases con los 3 colores reales de marca de MPC (navy `#0E3C89`, sky `#43BBED`, oro `#FFB71C`) y logo real.

## Mejoras de CRM del equipo comercial (5 ago 2026, extra fuera de las 3 acciones de Adrián)
Adrián grabó una reunión con Óscar y Oliver (4/08) recorriendo el CRM campo a campo. Condensado en `knowledge/mpc-group/reports-comerciales/2026-08-05-mejoras-crm-equipo-comercial.html/.pdf`: qué eliminar de la ficha de contacto (puesto, aniversario, 3 teléfonos, competidores...), qué falta/arreglar (desplegable cerrado de promoción, arrastrar datos Lead→Contacto, registrar llamadas/WhatsApp, ambos compradores en la misma ficha), qué mantener (contexto cualitativo, dormitorios/baños mínimo, financiación), automatizaciones a construir (conecta con #9) y dashboards de comercial/dirección. Enlaza directamente con la **acción 6 de las 12 del 30/07** (revisar automatismos y notificaciones internas, responsable Eduardo) — es el input directo del equipo comercial para esa revisión. Documento validado por Adrián y sin ninguna mención a Bruce, listo para compartir.

## Próxima acción
**Reunión del jueves 6 de agosto por la mañana con Cris.** Las 3 acciones de Adrián (#8, #9, #10) están cerradas, más el documento adicional de mejoras de CRM. Pendiente sin hacer: cotejar los 6 textos "revisar" del inventario de notificaciones (#9) con lo que ya existe en Administración/Postventa.

Pendiente sin resolver de sesiones anteriores: mover el PDF del informe desde `~/bruce/data/informe-proceso-comercial-cris/` a `~/Desktop/Bruce/` (arrastrado desde el 17/07).

## Pendiente / huecos detectados en el proceso (para trabajar con Cris — lista interna, más completa que lo que se muestra en el PDF)
1. ~~Quién lleva el lead nacional/español de Aura Condomina~~ — **resuelto 17 jul: repartido entre Oskar y Oliver.**
2. Protocolo de visita a distancia para cliente internacional. *(quitado del PDF a petición de Adrián, sigue sin resolver en la operativa real)*
3. A quién derivar una duda legal/fiscal compleja en la visita. *(idem — quitado del PDF, sigue abierto)*
4. Plazo estándar de seguimiento cuando el cliente "pide tiempo". *(idem — quitado del PDF, sigue abierto)*
5. Quién valida el contrato autogenerado antes de firma.
6. Protocolo de reclamación cuando un pago se retrasa.
7. Si la oferta de MPC 365 al inversor es sistemática o no.
8. Cadencia formal de seguimiento postventa (hoy inexistente).
9. **Nuevo (17 jul):** cómo usar WhatsApp automático en la entrada de un lead sin arriesgarnos a que Meta bloquee el número por spam.

## Notas
- Cris es **consultora externa** (RRHH y organización — probablemente vía Valderrama y Asociados, ver `knowledge/mpc-group/company-context.md`), ahora liderando también la parte tecnológica de procesos.
- El informe evitó deliberadamente inventar cifras de mercado — los % de mejora están marcados como objetivo, no como dato, a petición explícita tras aviso de Bruce.
