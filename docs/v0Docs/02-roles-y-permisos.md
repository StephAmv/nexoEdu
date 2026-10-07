# Roles y permisos

## Enfoque RBAC

El sistema debe usar control de acceso basado en roles, también conocido como RBAC. Cada usuario tendrá uno o más roles, y cada rol determinará qué módulos puede consultar y qué acciones puede realizar.

Este enfoque es importante porque el sistema manejará información sensible de alumnos, familias, conducta, asistencia y pagos.

## Roles del sistema

### Alumno

Usuario asociado a un expediente académico y escolar. Puede consultar información propia según las reglas definidas por la institución.

Acceso esperado:

- Consultar horarios de clase.
- Consultar tareas y entregas asignadas.
- Consultar calificaciones propias si la escuela lo permite.
- Consultar avisos generales.
- Consultar calendario escolar.

### Padre, madre o tutor

Usuario responsable de uno o más alumnos. Su función principal es dar seguimiento académico, disciplinario, administrativo y de asistencia.

Acceso esperado:

- Consultar información de sus hijos o tutorados.
- Visualizar evidencias y reportes de conducta.
- Recibir notificaciones por incidencias, faltas, retardos o avisos escolares.
- Justificar faltas.
- Solicitar o autorizar permisos y salidas.
- Consultar calificaciones, boletas y estado académico.
- Consultar adeudos, pagos y colegiaturas.
- Comunicarse con docentes, prefectura o dirección según las reglas de la escuela.

### Docente

Usuario responsable de impartir clases, registrar información académica y reportar situaciones relevantes sobre los alumnos.

Acceso esperado:

- Consultar grupos y alumnos asignados.
- Registrar tareas y entregas.
- Capturar calificaciones.
- Subir evidencias académicas o conductuales.
- Registrar reportes de conducta.
- Consultar historial académico y conductual de sus alumnos asignados, según permisos.
- Enviar comunicados a alumnos, padres o tutores de sus grupos.

### Prefectura

Usuario responsable del seguimiento disciplinario, asistencia, retardos, permisos y control operativo de alumnos dentro de la escuela.

Acceso esperado:

- Registrar asistencias, faltas y retardos.
- Consultar reportes de conducta creados por docentes.
- Registrar incidencias disciplinarias.
- Validar o revisar justificantes de faltas.
- Registrar autorizaciones de salida o permisos.
- Notificar a padres o tutores sobre incidencias o ausencias.
- Generar reportes de asistencia y conducta.

### Dirección

Usuario con visión global de la operación escolar y facultad para consultar reportes estratégicos.

Acceso esperado:

- Consultar información general de alumnos, grupos, docentes y ciclos escolares.
- Consultar estadísticas de asistencia, desempeño académico y conducta.
- Consultar reportes administrativos y financieros.
- Publicar avisos generales.
- Supervisar incidencias relevantes.
- Autorizar procesos especiales, si aplica.
- Acceder a dashboards institucionales.

### Administración y contaduría

Usuario responsable de procesos administrativos, pagos, colegiaturas, ventas e inventario relacionado con uniformes.

Acceso esperado:

- Registrar pagos y colegiaturas.
- Consultar adeudos por alumno.
- Emitir comprobantes o recibos.
- Administrar ventas de uniformes.
- Consultar y actualizar inventario de uniformes.
- Generar reportes de ingresos, adeudos y ventas.

### Administrador del sistema

Usuario técnico o institucional con permisos para configurar el sistema.

Acceso esperado:

- Crear, editar y desactivar usuarios.
- Asignar roles y permisos.
- Configurar ciclos escolares, grados, grupos y materias.
- Administrar catálogos generales.
- Consultar bitácoras de auditoría.
- Configurar parámetros del sistema.

## Matriz inicial de permisos

| Módulo / Acción | Alumno | Padre/Tutor | Docente | Prefectura | Dirección | Administración | Administrador |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Consultar datos propios del alumno | Sí | Sí, de sus hijos | Sí, de sus grupos | Sí | Sí | Limitado | Sí |
| Crear alumnos | No | No | No | No | Sí | Sí | Sí |
| Editar alumnos | No | No | No | Limitado | Sí | Sí | Sí |
| Registrar asistencia | No | No | No | Sí | Sí | No | Sí |
| Consultar asistencia | Sí, propia | Sí, de sus hijos | Sí, de sus grupos | Sí | Sí | No | Sí |
| Justificar faltas | No | Solicita | No | Revisa/valida | Sí | No | Sí |
| Registrar reportes de conducta | No | No | Sí | Sí | Sí | No | Sí |
| Consultar reportes de conducta | Sí, propios si aplica | Sí, de sus hijos | Sí, de sus grupos | Sí | Sí | No | Sí |
| Subir evidencias de conducta | No | No | Sí | Sí | Sí | No | Sí |
| Consultar evidencias de conducta | Sí, propias si aplica | Sí, de sus hijos | Sí, de sus grupos | Sí | Sí | No | Sí |
| Registrar calificaciones | No | No | Sí | No | Sí | No | Sí |
| Consultar calificaciones | Sí, propias | Sí, de sus hijos | Sí, de sus grupos | No | Sí | No | Sí |
| Gestionar materias y grupos | No | No | No | No | Sí | No | Sí |
| Publicar avisos generales | No | No | No | No | Sí | No | Sí |
| Enviar mensajes | Limitado | Sí | Sí | Sí | Sí | Limitado | Sí |
| Registrar pagos | No | No | No | No | Sí | Sí | Sí |
| Consultar adeudos | Limitado | Sí, de sus hijos | No | No | Sí | Sí | Sí |
| Gestionar inventario de uniformes | No | No | No | No | Sí | Sí | Sí |
| Consultar reportes institucionales | No | No | Limitado | Limitado | Sí | Según área | Sí |
| Consultar bitácora | No | No | No | No | Sí | Limitado | Sí |
| Administrar usuarios y roles | No | No | No | No | No | No | Sí |
