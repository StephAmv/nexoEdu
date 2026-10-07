# Resumen ejecutivo

## Objetivo

Construir una plataforma integral para la gestión escolar que centralice información académica, disciplinaria, administrativa y de comunicación entre escuela, docentes, prefectura, alumnos y padres o tutores.

El sistema debe facilitar el registro diario de información, el seguimiento de alumnos, la comunicación con las familias, la operación administrativa y la generación de reportes para la toma de decisiones.

## Alcance inicial

El sistema se organizará en módulos funcionales conectados entre sí:

1. Autenticación y acceso.
2. Docentes.
3. Alumnos.
4. Padres o tutores.
5. Prefectura.
6. Dirección.
7. Administración y contaduría.
8. Inventario de uniformes.
9. Académico.
10. Calendario escolar.
11. Comunicación y notificaciones.
12. Inscripciones y matrícula.
13. Pagos y colegiaturas.
14. Reportes y dashboards.
15. Auditoría y bitácora.

## Actores principales

- Alumno.
- Padre, madre o tutor.
- Docente.
- Prefectura.
- Dirección.
- Administración y contaduría.
- Administrador del sistema.

## Principios base

- Un solo acceso al sistema mediante login con roles.
- Control de permisos basado en RBAC.
- Información organizada por ciclo escolar.
- Relación entre alumnos y uno o más padres/tutores.
- Bitácora para acciones sensibles.
- Notificaciones automáticas ante eventos importantes.
- Desarrollo por fases para evitar construir todo al mismo tiempo.

## Primera versión recomendada

La primera versión debe enfocarse en:

- Autenticación.
- Usuarios y roles.
- Alumnos, padres/tutores, docentes, grados y grupos.
- Registro de asistencia por prefectura.
- Reportes de conducta y evidencias por docentes.
- Visualización de información para padres/tutores.
- Bitácora básica.

Esta base permite validar el flujo escolar principal antes de agregar calificaciones, pagos, inventario avanzado y dashboards.
