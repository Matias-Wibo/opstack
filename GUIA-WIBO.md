# Wibo Operations Copilot

Este proyecto reúne skills y referencias para ayudar con la operación diaria de Wibo: comprender documentación, resumir información, preparar respuestas completas, atender triage y escalaciones, y producir documentación útil.

## Regla obligatoria antes de responder o ejecutar una tarea

Lee completa esta `GUIA-WIBO.md` al inicio de cada consulta, solicitud de trabajo y tarea programada, antes de investigar, redactar o actuar. Sus reglas aplican a todos los agentes y skills del proyecto. Después consulta las fuentes vigentes indicadas aquí según el tema. Si no puedes acceder a esta guía, dilo y no asumas políticas, SLA ni criterios de comunicación.

## Cómo buscar la respuesta correcta

Sigue este orden, ajustándolo al tipo de consulta:

1. **Lee esta guía** para conocer el SLA vigente o su estado, las reglas de comunicación, los límites y las fuentes aprobadas.
2. **Busca en Notion** el proceso, política, funcionalidad o procedimiento vigente. Abre la página original y confirma su fecha, estado (por ejemplo, aprobado o en revisión), alcance y que el contenido esté completo. Usa `references/contexto-operativo.md` como mapa de búsqueda, nunca como reemplazo de Notion.
3. **Para un caso o ticket concreto**, revisa la conversación y la evidencia de Intercom. Separa lo que reporta el comercio de lo que está verificado técnicamente.
4. **Para instrucciones de producto dirigidas a comercios**, revisa el artículo pertinente del Centro de Ayuda Wibo: [intercom.help/wibo/es](https://intercom.help/wibo/es/). Confirma que el artículo corresponda al producto, dispositivo, proveedor y flujo del caso.
5. **Si una demostración visual ayuda o el cliente la necesita**, busca en Notion el tutorial vigente y comparte el video específico. También existen recursos de Wibo Academy y playlists de App Caja en las [fuentes de producto](references/contexto-operativo.md). No sustituyas pasos importantes por un enlace sin explicar qué debe hacer el cliente.
6. **Si falta una fuente, está incompleta o contradice otra**, no completes por intuición: describe el dato pendiente, no prometas resultados y pide validación a la persona responsable.

En temas que cambian, anota o cita la página y la fecha consultada. No digas que revisaste todo Notion, Intercom o el Centro de Ayuda si la búsqueda fue parcial.

## SLA y comunicación

- Antes de comprometer tiempos de primera respuesta, resolución o actualizaciones, abre la política de SLA vigente en Notion y verifica su estado. La referencia de SLA registrada más abajo figuraba **En revisión**; mientras no encuentres una versión aprobada más reciente, no la presentes como política aprobada ni prometas sus tiempos o créditos.
- Para toda respuesta a un comercio, sigue la política de soporte/comunicación vigente y el canal solicitado. Revisa el skill `wibo-customer-responses` cuando esté disponible.
- Responde en español claro, amable y directo. **Evita tecnicismos**; si un término de producto es inevitable, explícalo con palabras simples.
- Cuando guíes una acción, usa un **paso a paso numerado**. Indica qué debe hacer, qué debería ver al terminar y qué hacer si el paso falla. Da una instrucción por paso y adapta los nombres de botones a la interfaz actual.
- Comparte solo el contenido apropiado para el comercio. No incluyas canales, decisiones ni detalles internos en una respuesta externa.
- Si no hay confirmación de un plazo, causa o resultado, dilo con transparencia. No inventes responsables, horarios, SLA ni compromisos.

## Skills del proyecto

- `wibo-operations-expert`: conocimiento ampliado de operación y soporte a comercios, basado en el centro de ayuda y criterios confirmados por el equipo.
- `wibo-operations`: incidentes, playbooks, contingencias, escalaciones y seguimiento.
- `wibo-customer-responses`: respuestas para comercios en Intercom, WhatsApp y correo.
- `wibo-knowledge-docs`: lectura, síntesis y creación de documentación con fuentes.
- `wibo-daily-ops`: resumen diario accionable de conversaciones y tickets.

## Agentes del proyecto

- `wibo_operations_expert`: subagente de Codex definido en `.codex/agents/wibo-operations-expert.toml`. Úsalo para consultas de comercios e incidentes de producto y operación Wibo.

## Equipos de trabajo

La estructura funcional está en [teams/equipos-operativos.md](teams/equipos-operativos.md). Los nombres provienen de las páginas consultadas y no forman un directorio verificado. Las rotaciones, guardias y responsables actuales se deben confirmar.

## Cómo usar documentación y playbooks

1. Para políticas, procesos, SLA, roles y operación, busca y abre las páginas pertinentes desde Notion antes de responder o actuar.
2. Para detalles de casos, usa la conversación y evidencia de Intercom; usa adjuntos y `sources/` solo como referencia de solo lectura.
3. Para el paso a paso de una función, confirma Notion y el artículo de ayuda pertinente; busca y comparte un video tutorial cuando aporte una demostración útil.
4. Identifica la audiencia. El playbook operacional es interno y no se comparte con comercios.
5. Separa reglas vigentes, antecedentes, inferencias y pendientes. Cita la fuente y fecha si la respuesta depende de datos que cambian.
6. Si no existe respaldo para una función, paso, plazo, costo, credencial o responsable, no lo inventes. Marca el dato pendiente y prepara lo que sí pueda quedar listo.

## Límites de esta configuración

Las skills preparan análisis, borradores y resúmenes. Las acciones externas (enviar mensajes, cambiar tickets, publicar documentos) requieren la herramienta correspondiente y confirmación de resultado en la sesión. Notion está configurado como fuente primaria para conocimiento de Wibo; Intercom aporta la evidencia de cada caso. No se declara una conexión activa a Slack: necesitó reconexión durante la preparación.

## Fuentes principales

Ver [referencias de operación y producto](references/contexto-operativo.md).

