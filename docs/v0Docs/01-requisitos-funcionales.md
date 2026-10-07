# Requisitos funcionales

## 1. Módulo de autenticación y acceso

Permite el ingreso seguro al sistema mediante un login único basado en roles.

Requisitos:

- Iniciar sesión con usuario y contraseña.
- Asignar uno o más roles a cada usuario.
- Restringir módulos y acciones según permisos.
- Permitir recuperación o restablecimiento de contraseña.
- Bloquear, desactivar o reactivar usuarios.
- Mantener sesión segura.

Decisión recomendada:

- Usar un login único para todos los tipos de usuarios.
- Mostrar opciones diferentes según el rol del usuario.
- Permitir que un padre o tutor tenga varios alumnos asociados.
- Definir si los alumnos tendrán cuenta propia desde la primera versión.

## 2. Módulo de docentes

Permite a los docentes gestionar actividades académicas y reportar situaciones relevantes de sus alumnos.

Requisitos:

- Consultar grupos y materias asignadas.
- Registrar tareas y entregas.
- Capturar calificaciones.
- Subir evidencias académicas.
- Subir evidencias de conducta.
- Registrar reportes de conducta.
- Consultar reportes previamente registrados.
- Enviar observaciones o mensajes a padres/tutores.

Regla clave:

- Las evidencias y reportes de conducta registrados por docentes deben poder ser visualizados por prefectura y por los padres/tutores del alumno correspondiente.

## 3. Módulo de alumnos

Centraliza el expediente escolar del alumno.

Requisitos:

- Registrar datos generales del alumno.
- Asociar alumno con padre, madre o tutor.
- Asociar alumno con grado, grupo, ciclo escolar y matrícula.
- Consultar historial académico.
- Consultar historial de asistencia.
- Consultar historial de conducta.
- Consultar documentos entregados o pendientes.
- Consultar estado administrativo, como adeudos o pagos, según permisos.

## 4. Módulo de padres o tutores

Permite a las familias dar seguimiento a sus hijos o tutorados.

Requisitos:

- Consultar datos generales del alumno asociado.
- Visualizar asistencias, faltas y retardos.
- Visualizar evidencias y reportes de conducta.
- Visualizar calificaciones y boletas.
- Justificar faltas.
- Solicitar permisos o autorizaciones de salida.
- Recibir notificaciones.
- Consultar avisos generales.
- Consultar pagos, colegiaturas y adeudos.
- Comunicarse con docentes, prefectura o dirección.

## 5. Módulo de prefectura

Permite controlar asistencia, disciplina y permisos de alumnos.

Requisitos:

- Registrar asistencia diaria.
- Registrar faltas y retardos.
- Consultar y dar seguimiento a reportes de conducta.
- Registrar incidencias disciplinarias.
- Revisar justificantes de faltas.
- Registrar permisos y salidas autorizadas.
- Notificar a padres/tutores sobre incidencias, faltas o retardos.
- Generar reportes por alumno, grupo, fecha o periodo.

## 6. Módulo de dirección

Permite la supervisión general de la escuela.

Requisitos:

- Consultar dashboards institucionales.
- Consultar estadísticas de asistencia.
- Consultar estadísticas de conducta.
- Consultar desempeño académico por alumno, grupo, grado o periodo.
- Publicar avisos generales.
- Consultar reportes financieros resumidos.
- Consultar inventario bajo o movimientos relevantes.
- Dar seguimiento a casos importantes.

## 7. Módulo de administración y contaduría

Permite gestionar información financiera y administrativa de alumnos.

Requisitos:

- Registrar colegiaturas.
- Registrar pagos.
- Consultar adeudos.
- Generar recibos o comprobantes.
- Consultar historial de pagos por alumno.
- Generar reportes de ingresos y adeudos.
- Registrar conceptos de cobro.
- Administrar descuentos, becas o recargos, si aplica.

## 8. Módulo de inventario de uniformes

Permite controlar existencia, venta y movimientos de uniformes escolares.

Requisitos:

- Registrar productos de uniforme.
- Registrar tallas, modelos, precios y existencias.
- Registrar entradas y salidas de inventario.
- Registrar ventas de uniformes.
- Asociar ventas a alumnos o padres/tutores cuando aplique.
- Generar alertas de bajo stock.
- Consultar historial de movimientos.
- Generar reportes de inventario y ventas.

## 9. Módulo académico

Permite administrar la estructura académica y el avance escolar de los alumnos.

Requisitos:

- Configurar grados, grupos y materias.
- Definir plan de estudios por grado.
- Asignar docentes a materias y grupos.
- Registrar tareas y entregas.
- Registrar calificaciones.
- Generar boletas.
- Consultar kardex o historial académico.
- Consultar desempeño por alumno, grupo, materia o periodo.

## 10. Módulo de calendario escolar

Permite organizar fechas importantes y eventos escolares.

Requisitos:

- Registrar horarios de clases.
- Registrar eventos escolares.
- Registrar exámenes.
- Registrar juntas de padres.
- Registrar días festivos o suspensión de clases.
- Mostrar calendario por rol.
- Enviar recordatorios o notificaciones de eventos relevantes.

## 11. Módulo de comunicación y notificaciones

Permite centralizar avisos, mensajes y alertas automáticas.

Requisitos:

- Publicar avisos generales desde dirección.
- Enviar mensajes dirigidos por grupo, alumno o rol.
- Notificar a padres/tutores cuando se registre una falta, retardo o incidencia.
- Notificar cuando se suba una evidencia de conducta.
- Notificar fechas importantes del calendario escolar.
- Registrar historial de notificaciones enviadas.

Canales sugeridos:

- Notificación dentro del sistema.
- Correo electrónico.
- Notificación push, si se desarrolla aplicación móvil o PWA.

## 12. Módulo de inscripciones y matrícula

Permite gestionar altas, reinscripciones y documentación escolar.

Requisitos:

- Registrar nuevos alumnos.
- Registrar documentación requerida.
- Controlar documentos entregados y pendientes.
- Asignar ciclo escolar, grado y grupo.
- Gestionar reinscripciones.
- Consultar historial de matrícula.

## 13. Módulo de pagos y colegiaturas

Permite controlar obligaciones económicas de alumnos y familias.

Requisitos:

- Definir conceptos de pago.
- Generar colegiaturas por ciclo o periodo.
- Registrar pagos realizados.
- Consultar adeudos.
- Registrar descuentos, becas o recargos.
- Emitir recibos.
- Generar reportes financieros.

## 14. Módulo de reportes y dashboards

Permite generar información para dirección, administración, prefectura y docentes.

Requisitos:

- Reporte de asistencia por alumno, grupo, grado o periodo.
- Reporte de incidencias por alumno, grupo, tipo o periodo.
- Reporte de calificaciones y desempeño académico.
- Reporte de adeudos y pagos.
- Reporte de ventas de uniformes.
- Reporte de inventario bajo en stock.
- Dashboard general para dirección.
- Exportación a PDF o Excel, si aplica.

## 15. Módulo de auditoría y bitácora

Permite registrar acciones importantes realizadas dentro del sistema.

Requisitos:

- Registrar quién creó, modificó o eliminó información relevante.
- Registrar fecha y hora de cada acción.
- Registrar cambios en asistencias, calificaciones, pagos, incidencias y permisos.
- Permitir consulta de bitácora por administradores autorizados.
- Mantener evidencia ante aclaraciones o disputas.
