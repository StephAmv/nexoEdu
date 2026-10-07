# Entidades y reglas generales

## Reglas generales del sistema

- Toda información debe estar asociada a un ciclo escolar.
- Un alumno puede tener uno o más padres o tutores asociados.
- Un padre o tutor puede tener uno o más alumnos asociados.
- Un docente solo debe gestionar alumnos de sus grupos o materias asignadas.
- Prefectura debe poder consultar reportes de conducta y asistencia de todos los alumnos bajo su responsabilidad operativa.
- Dirección debe tener visibilidad global, principalmente de consulta y supervisión.
- Administración debe tener acceso a información financiera y de inventario, pero no necesariamente a información disciplinaria detallada.
- Toda modificación importante debe quedar registrada en la bitácora.
- Las notificaciones automáticas deben generarse ante eventos relevantes como faltas, retardos, incidencias, evidencias de conducta y avisos generales.

## Entidades principales sugeridas

Estas entidades sirven como base para el futuro diseño de base de datos:

### Seguridad y usuarios

- Usuario.
- Rol.
- Permiso.
- Bitácora.

### Comunidad escolar

- Alumno.
- Padre o tutor.
- Docente.
- Grupo.
- Grado.
- Materia.
- Ciclo escolar.
- Inscripción o matrícula.

### Asistencia y conducta

- Asistencia.
- Justificante.
- Reporte de conducta.
- Evidencia.
- Permiso o autorización de salida.

### Académico

- Calificación.
- Tarea.
- Entrega.
- Boleta.
- Kardex o historial académico.
- Plan de estudios.

### Calendario y comunicación

- Calendario escolar.
- Evento escolar.
- Aviso.
- Notificación.
- Mensaje.

### Administración y finanzas

- Pago.
- Concepto de pago.
- Adeudo.
- Recibo.
- Beca o descuento.
- Recargo.

### Inventario de uniformes

- Producto de uniforme.
- Talla.
- Modelo.
- Movimiento de inventario.
- Venta de uniforme.

## Requisitos no funcionales iniciales

- Seguridad basada en roles y permisos.
- Registro de auditoría para acciones sensibles.
- Diseño preparado para múltiples ciclos escolares.
- Interfaz responsiva para uso en computadora, tablet o celular.
- Protección de datos personales de alumnos y familias.
- Respaldos de información.
- Validaciones para evitar duplicidad de alumnos, usuarios, pagos o registros críticos.
- Posibilidad de exportar reportes en formatos comunes.
- Arquitectura modular para agregar funciones por etapas.
