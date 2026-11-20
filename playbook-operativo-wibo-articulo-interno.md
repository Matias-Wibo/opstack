# Playbook operativo de Wibo: atención y gestión de incidentes

Descripción: Guía interna para diagnosticar, clasificar, contener, escalar y cerrar incidentes, con criterios de seguimiento y atención fuera de horario.

> Uso interno del equipo Wibo. No compartir con comercios.

## Propósito y principios

Este playbook orienta la atención de incidentes desde el primer reporte hasta el cierre. Soporte mantiene la comunicación con el comercio; IT/Dev lidera el diagnóstico técnico y la solución cuando corresponde.

- Clasifica por el impacto operativo y la evidencia disponible. Si hay duda entre dos niveles, usa provisionalmente el nivel más alto.
- Activa una contingencia para contener un caso Crítico o Importante antes de buscar la causa raíz.
- Documenta hechos, evidencia, decisiones, responsable y siguiente actualización. Un workaround reduce el impacto, pero no cierra el ticket.
- Mantén un folio de Intercom y su historia asociada en Jira. Jira es la fuente para el estado técnico y la medición del SLA.
- No atribuyas la causa a Wibo sin evidencia. Hardware, internet, sistema operativo y sistemas de terceros requieren diagnóstico propio.

## Flujo de atención

### 1. Recibir y diagnosticar

Soporte L1 recibe el reporte, acusa recibo y registra:

- Comercio y folio de Intercom.
- Aplicación o dispositivo afectado y síntoma concreto.
- Desde cuándo ocurre y a cuántas personas o comercios afecta.
- Evidencia útil y disponible: captura para errores visuales, video para mostrar un flujo o comportamiento, y logs cuando existan.
- Si funciona en otro dispositivo con la misma conexión.
- Impacto actual, workaround disponible y próximo control.

Pide solo la evidencia necesaria y posible de obtener. Evita volver a pedir información que ya está en el ticket.

### 2. Clasificar y contener

Asigna el nivel por el impacto real en la operación. Si la evidencia aún no permite confirmarlo, indica que la clasificación es provisional y solicita validación técnica. Si cambia el impacto o se activa un workaround, reevalúa el nivel y documenta el cambio.

Para casos Críticos o Importantes, prioriza la continuidad operacional:

| Problema | Contingencia documentada |
| --- | --- |
| Kiosco caído | Usar PWA/Web desde un navegador. |
| Pagos en kiosco no disponibles | Habilitar pago en caja. |
| Impresora de cocina caída | Consultar pedidos en la App de Pedidos o el Dashboard. |
| Impresora de kiosco caída | Consultar el número de orden en pantalla; algunas terminales permiten imprimir desde la máquina de pago. |
| POS no recibe pedidos | Gestionar y monitorear pedidos desde el Dashboard de Wibo. |

Confirma que la alternativa esté habilitada para ese comercio. La contingencia es temporal y no sustituye el arreglo definitivo.

### 3. Escalar y coordinar

Con diagnóstico inicial, nivel y evidencia, Soporte crea el ticket en Intercom, que debe quedar asociado a una historia en Jira. El Sheriff on Duty de IT recibe el caso, confirma responsable técnico y asignación al sprint.

La excepción es un caso Crítico con posibilidad de caída del servicio: se escala de inmediato y se crea el folio en paralelo. Registra la excepción en el ticket.

Coordina el caso en el hilo operativo asociado al ticket y deja allí la evidencia. Registra en Intercom o Jira las decisiones relevantes, aunque también se hayan coordinado por otro canal. Si Jira no muestra avance, Soporte consulta al Sheriff on Duty, no directamente al developer.

### 4. Mantener informado al comercio y al equipo

Comunica lo que se sabe, qué acción está en curso y cuándo será la siguiente actualización, aunque todavía no exista una solución. Soporte mantiene la relación con el comercio; IT comunica proactivamente sus avances a Soporte.

El playbook define estas frecuencias mínimas:

| Nivel | Actualización al comercio | Actualización de IT a Soporte |
| --- | --- | --- |
| Crítico | Cada 30 minutos | Cada 30 minutos |
| Importante | Cada día hábil | Cada 4 horas |
| Normal | Al inicio y al cierre | Cada día hábil |
| Menor | Al inicio y al cierre | Cada 3 días |

Si no hay avance técnico dentro del plazo correspondiente, Soporte consulta al Sheriff según la pauta del playbook. Confirma los tiempos y turnos vigentes antes de comprometerlos.

## Caída masiva: Protocolo Rojo

Activa el protocolo solo cuando IT confirme que software o infraestructura de Wibo dejó la plataforma caída o inoperable para varios comercios. Un reporte aislado no basta.

Una vez confirmada la caída:

1. El Sheriff on Duty asume la coordinación técnica; si no está disponible, toma el rol la persona senior de desarrollo disponible.
2. Se activa la coordinación del equipo técnico y se centraliza la información y las tareas para evitar intervenciones duplicadas.
3. Soporte envía el aviso inicial a los comercios afectados dentro de los primeros 15 minutos y actualiza cada 30 minutos, aunque no haya solución. IT entrega el estado a Soporte antes de cada ciclo.
4. Al recuperar el servicio, Soporte comunica el cierre con una explicación breve de qué pasó y qué se hizo.
5. Dentro de las siguientes 24 horas hábiles, documenta el post-mortem: duración, comercios afectados, causa raíz, solución y acciones preventivas.

## Seguimiento de SLA y capacidad

Jira es la fuente de medición de los tiempos de resolución. El playbook indica que el SLA se pausa mientras se espera respuesta del comercio o de un tercero, y que el tiempo fuera del horario hábil, fines de semana y feriados no se contabiliza. Verifica la política de SLA aprobada antes de aplicar estos criterios o comunicar compromisos: la referencia localizada de SLA figura en revisión.

Cuando un SLA se acerca al vencimiento o vence, documenta impacto, estado, bloqueo, decisión requerida y próximo compromiso interno. El playbook describe alertas al 50%, al vencimiento y una escalación posterior si no hay fecha de resolución; los canales, responsables y plazos deben confirmarse en la versión vigente.

La capacidad de IT se distribuye en el playbook como 40% para operaciones y 60% para desarrollo planificado. No reasignes unilateralmente tickets activos o compromisos. Si la demanda supera la capacidad, presenta los trade-offs y escala la decisión a quienes corresponda. El playbook establece que un ticket con SLA activo o vencido no debe desplazarse por un requerimiento comercial nuevo.

## Atención fuera de horario

La política de guardia consultada asigna a la guardia Ops/Comercial el rol de punto único de contacto con IT durante fines de semana y feriados. La guardia canaliza los incidentes de plataforma hacia Guardia IT; los pendientes individuales siguen a cargo de quien los dejó abiertos. La atención fuera de horario se describe como best effort. Los casos normales o menores se registran para el próximo día hábil.

Hay una diferencia entre las fuentes: el playbook operacional indica contacto directo a Guardia IT fuera de horario; la Política de Guardia, consultada después, indica que la guardia Ops/Comercial centraliza el contacto. Aplica la política vigente y confirma quién está de turno antes de escalar.

## Cierre del caso

IT documenta la causa raíz y la solución en Jira, y avisa a Soporte. Soporte confirma el resultado con el comercio, documenta el cierre en Intercom y cierra el caso. Si quedó un workaround activo, deja claro qué solución definitiva sigue pendiente.

## Puntos que se deben validar antes de actuar

- Vigencia de los plazos de respuesta y resolución, y estado aprobado de la política SLA.
- Turno actual y responsables de Sheriff, Guardia IT y guardia Ops/Comercial.
- Canal operativo vigente para coordinación interna.
- Elegibilidad de una contingencia para el comercio afectado.
- Criterio de créditos por indisponibilidad: las fuentes consultadas no son consistentes y la política SLA localizada figura en revisión.

## Fuentes consultadas

- [VF- Playbook operacional Wibo](https://www.notion.so/3606e73ee61280fa8bd8d814698198b5), consultado el 4 de noviembre de 2026. Última edición registrada en la página: 14 de mayo de 2026. Estado de verificación: no verificado.
- [Política de Guardia: fines de semana, feriados y fuera de horario](https://www.notion.so/3796e73ee61281238a15f8e0f0ba5f1d), consultada el 4 de noviembre de 2026. Última edición registrada en la página: 8 de junio de 2026. Estado de verificación: no verificado.

Este artículo resume las fuentes anteriores. No sustituye la política vigente de Soporte/SLA ni la confirmación del turno operativo.

