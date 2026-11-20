# Contexto operativo Wibo

Notion es la fuente primaria de conocimiento operativo y de producto de Wibo. Antes de responder o producir documentación, busca y abre desde la conexión Notion las páginas pertinentes, valida fecha/estado/truncamiento y cita los enlaces utilizados. Este archivo es un índice y una síntesis inicial, no un volcado completo del espacio ni sustituto de las páginas originales. Si la consulta es amplia, declara qué áreas se revisaron y no afirmes haber cubierto todo Notion sin una búsqueda exhaustiva posible. Los archivos en `sources/` son referencias sincronizadas y no deben modificarse.

## Producto y mercados

Wibo es una plataforma SaaS de autoservicio para restaurantes y comercios. La documentación de producto disponible describe seis superficies: Kiosk/tótem Android, PWA, App de Pedidos, App Caja (`pos.holadary.com`), Dashboard/Back Office (`admin.holadary.com`) y Order Display. El ecosistema incluye integraciones POS, pagos web, terminales, periféricos y un agente de impresión Windows. La lista exacta de compatibilidad varía por país y debe verificarse en la página de producto vigente antes de responder.

Fuentes primarias:

- [Funcionalidades Wibo en Notion](https://www.notion.so/35f6e73ee6128026b672d13df2282856)
- [Componentes de autoservicio Wibo](https://www.notion.so/1216e73ee61280838a41ead556980ba3)
- [Linktree de clientes Wibo](https://linktr.ee/AutoservicioWIBO)
- [Wibo Academy](https://www.youtube.com/playlist?list=PL-9O13wA5glG3enSQ-q8fGFKhxRxOGkwu)
- [Playlist App Caja](https://www.youtube.com/playlist?list=PL-9O13wA5glGaX_yTlseIkH53Iuahbq52)
- [Centro de Ayuda](https://intercom.help/wibo/es)

## Playbook operacional

Fuente interna de referencia: [VF- Playbook operacional Wibo](https://www.notion.so/3606e73ee61280fa8bd8d814698198b5). Se presenta como uso exclusivo interno. La página fue consultada el 14 de mayo de 2026. Para llamadas fuera de horario, contrástala con la [Política de Guardia](https://www.notion.so/3796e73ee61281238a15f8e0f0ba5f1d), consultada el 8 de junio de 2026: esta asigna el primer contacto a guardia Ops/Comercial y establece que Guardia IT recibe casos escalados por ese rol. Valida vigencia y turno antes de actuar.

- Soporte L1 recibe, diagnostica, crea ticket, comunica y acompaña; IT/Dev diagnostica causa raíz y resuelve software/infraestructura; el Sheriff on Duty rota semanalmente; la Guardia IT cubre críticos fuera de horario y feriados.
- Todo reporte debe tener folio Intercom y Jira asociado. La única excepción descrita es un Crítico con posibilidad de caída, que se escala de inmediato y se registra en paralelo.
- Coordinación de tickets en el hilo de `#ops-customersupport`; Jira es la fuente de verdad para resolución y SLA.
- Diagnóstico inicial: síntoma, aplicación/dispositivo, desde cuándo, evidencia adecuada y si funciona en otro dispositivo con la misma conexión.
- Contingencias documentadas: Kiosk caído → PWA/Web; pago en tótem no disponible → pago en caja; impresora de cocina caída → App de Pedidos o Dashboard; POS sin recibir → gestionar pedidos en Dashboard. Confirma que la opción siga habilitada para el comercio.
- Protocolo Rojo solo después de confirmación técnica de caída de Wibo que afecte a múltiples comercios. Sheriff es Commander en horario hábil; guardia actúa fuera de horario si confirma la caída. El playbook indica aviso inicial dentro de 15 minutos y actualizaciones cada 30 minutos durante el incidente.
- El mismo playbook indica seguimiento periódico por nivel, alertas de SLA, y revisiones de capacidad. Revisa el texto original antes de dar plazos: algunos detalles dependen de estados y horarios vigentes.

Regla de seguridad editorial: estas instrucciones internas no se copian al comercio. Para clasificación de cara al cliente, consulta la política de soporte vigente; las categorías Crítico/Importante/Normal/Menor dependen de impacto y evidencia, y no deben inferirse solo por la dificultad reportada.

## Soporte y onboarding

- [Políticas de Soporte y Acompañamiento](https://www.notion.so/3ba6e73ee61280cbac2bfa6921b344b3)
- [Políticas de soporte y tiempos de respuesta (SLA) de Wibo](https://www.notion.so/3f46e73ee61281fe825eef623071066d). Estado en Notion: En revisión, consultado el 9 de octubre de 2026. No tratar como aprobada. La página deja pendiente resolver si el crédito por indisponibilidad es automático o debe solicitarlo el comercio.
- [Política de Guardia — Fines de Semana, Feriados y Fuera de Horario](https://www.notion.so/3796e73ee61281238a15f8e0f0ba5f1d). Consultada el 8 de junio de 2026. Verifica vigencia y turno actual antes de dar instrucciones.
- [SOP — Proceso de onboarding Wibo](https://www.notion.so/3f96e73ee61281a5b578fa00d86ef5d4). Consultado el 14 de octubre de 2026; la página se declara versión documental con puntos de validación operativa. No conviertas sus pasos en compromisos sin revisar esos puntos.
- [Proceso completo de onboarding](https://www.notion.so/2bc6e73ee6128073b188de36ee4ec688)
- [Proceso de Onboarding Wibo 2025](https://www.notion.so/13c6e73ee61280c78ec9df9223a79a9d)

La política consultada describe horario hábil de lunes a viernes, 09:00–18:00 hora de Chile y establece que la causa raíz debe estar respaldada. Los tiempos de SLA, exclusiones, créditos y compromisos al comercio se deben confirmar en una versión aprobada; el artículo de SLA localizado figura en revisión y mantiene una discrepancia abierta sobre créditos.

## Páginas maestras adicionales descubiertas en Notion

- [Arquitectura del Ecosistema Wibo — Estado real (2026)](https://www.notion.so/3ca6e73ee612817db11ec93992599af9): página canónica del stack, verificada contra código al 28 de agosto de 2026.
- [Funcionalidades Wibo para clientes](https://www.notion.so/3276e73ee6128011b99ce57848a8e135): está dentro de guías de ventas; valida que el contenido aplique al caso antes de usarlo.
- [Guía de Integraciones Sistema de ventas API Wibo — Para Partners y Resellers](https://www.notion.so/3766e73ee61281a19ca2fcff5d1c7b83), consultada el 2 de octubre de 2026.
- [Integración Wibo + Toteat — configuración y problemas frecuentes](https://www.notion.so/3746e73ee612813e8556ccea729f5676), consultada el 14 de septiembre de 2026.
- [Checklist Onboarding Wibo](https://www.notion.so/37b6e73ee612808da419d3919a9dba14), consultado el 10 de junio de 2026.

Notion devuelve páginas duplicadas sobre funcionalidades, políticas y onboarding. Escoge la fuente cuyo alcance, estado y vigencia correspondan al trabajo; no asumas que la página con título más genérico es la aprobada.

## Personas y equipos

Consulta [Equipos y personas por función](../teams/equipos-operativos.md). El playbook cita a Ari para Comercial, Greg/Leo en contexto IT y Leo como líder de infraestructura; no aporta una asignación completa ni confirma que estos nombres sigan vigentes. Nunca rellenes los turnos rotativos con esos nombres sin confirmación actual.

## Fuentes y cobertura de consultas

- Notion está disponible para localizar y leer páginas; úsalo como fuente primaria para procesos, políticas, roles y producto. Registra URL y fecha consultada.
- Slack requirió reconexión durante la preparación de esta guía. No lo presentes como consultado hasta que el conector funcione.
- Intercom ofrece herramientas de lectura de conversaciones abiertas en la sesión, pero no se debe afirmar que se revisaron todos los tickets salvo que se haya completado la lectura/paginación requerida.
- Las skills globales `wibo-docs`, `wibo-documentacion`, `wibo-customer-communication` y `wibo-intercom-articles` aportan reglas de estilo y documentación. No duplicar sus manuales; consultar el skill correspondiente cuando esté disponible.

## Calidad de respuesta

Separa hechos, inferencias y pendientes. Nunca inventes funcionalidades, pasos, credenciales, costos, responsables, fechas, SLA ni resultado de una acción. Para un dato operativo cambiante, abre la fuente primaria y confirma la vigencia. Si falta respaldo esencial, marca `[PENDIENTE DE VALIDAR: dato]`.

