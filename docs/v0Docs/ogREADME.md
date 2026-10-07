# Documentación base del sistema escolar

Este directorio contiene la documentación inicial para comenzar el desarrollo del sistema escolar. La información está dividida por tema para que sea más fácil consultarla, mantenerla y convertirla después en historias de usuario, diseño de base de datos o tareas técnicas.

## Documentos disponibles

| Documento | Propósito |
| --- | --- |
| [`00-resumen-ejecutivo.md`](00-resumen-ejecutivo.md) | Explica de forma breve el objetivo, alcance, módulos y fases del proyecto. |
| [`01-requisitos-funcionales.md`](01-requisitos-funcionales.md) | Detalla los módulos funcionales del sistema y lo que debe hacer cada uno. |
| [`02-roles-y-permisos.md`](02-roles-y-permisos.md) | Define los roles del sistema y una matriz inicial de permisos RBAC. |
| [`03-entidades-y-reglas.md`](03-entidades-y-reglas.md) | Lista las entidades principales sugeridas y reglas generales que impactan el diseño de datos. |
| [`04-roadmap.md`](04-roadmap.md) | Propone una ruta de desarrollo por fases para construir el sistema de forma incremental. |
| [`05-decisiones-pendientes.md`](05-decisiones-pendientes.md) | Agrupa decisiones que conviene resolver antes o durante el diseño técnico. |

## Cómo usar esta documentación

1. Comenzar con el resumen ejecutivo para entender la visión general.
2. Revisar requisitos funcionales para identificar los módulos del sistema.
3. Validar roles y permisos antes de diseñar la base de datos o pantallas.
4. Usar entidades y reglas como punto de partida para el modelo de datos.
5. Convertir el roadmap en épicas, historias de usuario o tareas de desarrollo.
6. Resolver las decisiones pendientes antes de cerrar el alcance de la primera versión.

## Enfoque recomendado

La primera versión debe priorizar la base operativa: autenticación, roles, alumnos, tutores, docentes, grupos, asistencia, reportes de conducta, evidencias y visualización para padres/tutores. Esto permite entregar valor rápido y deja preparada la estructura para módulos académicos, administrativos y de reportes avanzados.
