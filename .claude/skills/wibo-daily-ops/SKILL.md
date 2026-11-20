---
name: wibo-daily-ops
description: Convierte conversaciones, notas y cambios de tickets Wibo en un resumen diario accionable con prioridades, responsables funcionales, seguimientos y pendientes de respuesta.
---

# Resumen diario de operaciones

Obtén las reglas de operación, los SLA y los responsables vigentes desde Notion. Obtén los hechos de cada caso desde las conversaciones de Intercom y cualquier evidencia enlazada. Trabaja solo con los períodos y fuentes que hayas podido revisar, y aplica `wibo-operations` para triage y `wibo-customer-responses` para mensajes a comercios.

## Proceso

1. Indica el período y las fuentes cubiertas. Si una fuente no está disponible, decláralo y no describas el resumen como completo.
2. Por conversación, conserva folio, comercio si está autorizado, tema, impacto, nivel respaldado, estado, último avance, siguiente acción, responsable por función y fecha de seguimiento confirmada.
3. Separa novedades, acciones vencidas, bloqueos externos, datos faltantes y riesgos. No marques un ticket cerrado por ausencia de actividad.
4. Prioriza con el playbook vigente: incidentes críticos sin contingencia, importantes detenidos, riesgo de SLA, casos sin actualización y luego el resto según impacto.
5. Incluye una lista corta “Hoy”, con acción concreta, responsable funcional y hora/condición de seguimiento. Si la fecha o persona no está confirmada, déjala como pendiente de asignación.
6. Evita duplicados del mismo folio y distingue claramente los hechos de cualquier inferencia.

## Formato recomendado

### Prioridades de hoy
| Prioridad | Folio y tema | Impacto/estado | Próxima acción | Responsable | Seguimiento |

### Riesgos y bloqueos
### Casos que necesitan respuesta al comercio
### Cambios desde el último corte
### Cobertura y datos pendientes

No envíes mensajes ni cambies estados mediante herramientas si no existe esa capacidad en la sesión o no se ha solicitado la acción. Entrega borradores listos para revisión.

