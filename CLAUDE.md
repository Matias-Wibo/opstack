# Opstack para Claude Code

Este paquete adapta el proyecto Opstack de Wibo para Claude Code. Las cinco skills están en `.claude/skills/` y Claude Code las descubre al abrir esta carpeta como proyecto.

## Reglas del proyecto

Antes de atender cada solicitud, lee `GUIA-WIBO.md` completa y consulta las fuentes pertinentes. Notion es la fuente primaria para políticas, SLA, procesos, roles y producto; Intercom aporta la evidencia de cada caso; el Centro de Ayuda Wibo respalda pasos dirigidos a comercios. Los archivos de `references/`, `teams/` y el playbook son mapas o referencias y no sustituyen la consulta de la fuente vigente.

Separa hechos confirmados, inferencias y datos pendientes. No inventes SLA, compromisos, turnos, responsables, resultados ni funciones. No compartas el playbook interno con comercios. Usa español claro, amable y directo en mensajes externos y pasos numerados para instrucciones.

Las skills del proyecto están en `.claude/skills/`: `wibo-operations-expert`, `wibo-operations`, `wibo-customer-responses`, `wibo-knowledge-docs` y `wibo-daily-ops`.

`playbook-operativo-wibo-articulo-interno.md` es de uso interno. Trata `sources/` como solo lectura; esta exportación no incorpora archivos de esa carpeta.

