# nexoEdu — Plan de Calidad del Proyecto

## Introducción

El proyecto parte de una visión amplia: una plataforma que centralice la información académica, disciplinaria, administrativa y de comunicación de una escuela. Esa visión es demasiado grande para nueve semanas y tres integrantes. Por eso el plan separa con claridad lo que el equipo se compromete a entregar (la base operativa) de lo que queda como evolución futura.

Establecer la calidad desde el inicio evita dos errores comunes: descubrir al final que “terminado” significaba cosas distintas para cada integrante, y dejar que el alcance crezca sin control. Aquí la calidad se define como requisitos verificables, criterios de aceptación medibles, métricas simples, control de cambios y evidencias conservadas. La gestión del proyecto y la calidad del software se tratan como un mismo proceso: lo que no se planifica y registra no se puede demostrar.

## Descripción del proyecto

El sistema es una plataforma de gestión escolar con un solo acceso mediante login y control de permisos por roles (RBAC). Su visión es centralizar la información académica, disciplinaria, administrativa y de comunicación entre escuela, docentes, prefectura, alumnos y padres o tutores.

**Necesidad que atiende:** facilitar el registro diario de información, el seguimiento de alumnos, la comunicación con las familias, la operación administrativa y la generación de reportes para la toma de decisiones.

**Principales usuarios:** alumno; padre, madre o tutor; docente; prefectura; dirección; administración y contaduría; administrador del sistema.

**Principios base del producto** (tomados del resumen ejecutivo):

- Un solo acceso al sistema mediante login con roles.
- Control de permisos basado en RBAC.
- Información organizada por ciclo escolar.
- Relación entre alumnos y uno o más padres/tutores.
- Bitácora para acciones sensibles.
- Desarrollo por fases para evitar construir todo al mismo tiempo.

**Escuela destinataria:** caso simulado de una preparatoria (nivel medio superior). El sistema no se desarrolla para una escuela específica; todos los datos de prueba serán ficticios.

## Problemática

nexoEdu se plantea como un caso simulado: una preparatoria genérica, no una escuela específica. La problemática se deriva de la documentación del proyecto, a partir de lo que el sistema debe resolver. No se usan estadísticas ni datos externos.

**Situación actual (inferida):** la información de alumnos, asistencia, conducta y comunicación con las familias no está centralizada en un sistema único con control de acceso por rol.

**Problemas identificados:**

- El registro de asistencia, faltas y retardos no queda en un historial consultable por alumno, grupo o periodo.
- Los reportes de conducta y sus evidencias no llegan de forma directa a prefectura ni a los padres/tutores.
- Los padres/tutores no tienen un medio para consultar la asistencia y conducta de sus hijos.
- No existe un control formal de quién puede ver o modificar información sensible de alumnos y familias.
- No hay trazabilidad de quién creó o modificó un registro, lo que dificulta resolver aclaraciones o disputas.

**Consecuencias:** seguimiento tardío de ausencias e incidencias, información dispersa o duplicada, exposición de datos personales a personas no autorizadas y falta de evidencia ante reclamaciones.

**Necesidad de una solución:** un sistema que concentre el flujo escolar principal (alumnos, grupos, asistencia y conducta), restrinja el acceso según el rol y deje registro de las acciones sensibles.

## Justificación

Construir primero la base operativa resuelve el flujo escolar más frecuente y deja lista la estructura sobre la que crecerán las demás fases.

| Aspecto | Qué aporta la primera versión |
| --- | --- |
| Centralización de información | Alumnos, padres/tutores, docentes, grados y grupos en una sola base, organizada por ciclo escolar. |
| Seguimiento de alumnos | Historial de asistencia y de reportes de conducta consultable por alumno. |
| Control de asistencia y conducta | Prefectura registra asistencia diaria; docentes registran reportes de conducta con evidencias. |
| Comunicación entre actores | Los padres/tutores consultan la asistencia y los reportes de conducta de sus hijos. Las notificaciones automáticas quedan para la Fase 2. |
| Seguridad y permisos | Login único con RBAC: cada rol ve y hace solo lo que le permite la matriz de permisos. |
| Trazabilidad | Bitácora de quién creó, modificó o eliminó información relevante, con fecha y hora. |
| Crecimiento futuro | Arquitectura modular y datos por ciclo escolar para agregar comunicación, académico, administración y reportes sin rehacer la base. |

## Objetivos

### Objetivo general

Desarrollar, entre el 23 de septiembre y el 25 de noviembre de 2026, la primera versión funcional de la plataforma de gestión escolar (base operativa), que permita registrar alumnos, padres/tutores, docentes, grados y grupos, controlar la asistencia y los reportes de conducta con evidencias, y ofrecer consulta a padres/tutores, con acceso por roles y bitácora de acciones sensibles, verificando su cumplimiento mediante los criterios y métricas de este plan.

### 6.2 Objetivos específicos

1. Implementar un login único con control de acceso por roles conforme a la matriz de permisos del proyecto.
2. Permitir al administrador del sistema gestionar usuarios, roles, ciclos escolares, grados y grupos.
3. Registrar alumnos, padres/tutores y docentes, con sus asociaciones a grupos y entre alumno y tutor.
4. Permitir a prefectura registrar asistencias, faltas y retardos diarios por grupo.
5. Permitir a docentes y prefectura registrar reportes de conducta con evidencias adjuntas.
6. Permitir a los padres/tutores consultar asistencia, reportes de conducta y evidencias solo de sus hijos.
7. Registrar en bitácora las acciones sensibles del alcance inicial.
8. Verificar la primera versión con casos de prueba documentados, incluidas pruebas de permisos por rol.
9. Mantener control de cambios, métricas y evidencias durante todo el proyecto.

## Alcance del proyecto

### Visión completa del sistema

A largo plazo, el sistema contempla 15 módulos: autenticación y acceso, docentes, alumnos, padres o tutores, prefectura, dirección, administración y contaduría, inventario de uniformes, académico, calendario escolar, comunicación y notificaciones, inscripciones y matrícula, pagos y colegiaturas, reportes y dashboards, y auditoría y bitácora.

### Alcance de la primera versión

| Área | Qué incluye |
| --- | --- |
| Autenticación y roles | Login con usuario y contraseña, cierre de sesión, menú según rol, restricción de módulos y acciones. |
| Gestión de usuarios | Crear, editar, desactivar y reactivar usuarios; asignar roles. |
| Estructura escolar mínima | Ciclo escolar, grados y grupos. |
| Comunidad escolar | Alumnos, padres/tutores (relación muchos a muchos) y docentes asignados a grupos. |
| Prefectura | Registro y consulta de asistencias, faltas y retardos. |
| Conducta | Reportes de conducta con evidencias, registrados por docentes y prefectura. |
| Padres/tutores | Consulta de datos, asistencia, reportes de conducta y evidencias de sus hijos. |
| Bitácora básica | Registro y consulta de acciones sensibles del alcance inicial. |

## Usuarios y actores

La visión general contempla siete roles; la primera versión involucra directamente a cinco. Alumno y Administración y contaduría quedan fuera de esta versión.

| Rol | Función en la visión general | Participación en el alcance inicial |
| --- | --- | --- |
| Administrador del sistema | Configura usuarios, roles, ciclos, grados, grupos, catálogos y consulta la bitácora. | **Directa.** Da de alta usuarios, roles y estructura escolar. |
| Prefectura | Asistencia, disciplina, permisos y control operativo de alumnos. | **Directa.** Registra asistencia y da seguimiento a la conducta. |
| Docente | Imparte clases, registra información académica y reporta situaciones de sus alumnos. | **Directa.** Registra reportes de conducta con evidencias de sus grupos. |
| Padre, madre o tutor | Da seguimiento académico, disciplinario, administrativo y de asistencia. | **Directa.** Consulta asistencia y conducta de sus hijos. |
| Dirección | Visión global de consulta y supervisión; reportes estratégicos. | **Directa, de consulta.** Consulta alumnos, asistencia, conducta y bitácora; puede crear y editar alumnos según la matriz. |
| Alumno | Consulta su información académica y escolar. | **Fuera del alcance inicial.** No tendrá cuenta propia en la primera versión (D-01); su información la consultan sus padres/tutores. |
| Administración y contaduría | Pagos, colegiaturas, ventas e inventario de uniformes. | **Fuera del alcance inicial** (Fase 4). La matriz le permite crear y editar alumnos; ver inconsistencia I-03. |

## Requerimientos funcionales del alcance inicial

La primera versión compromete 26 requisitos, tomados de los módulos 1, 2, 3, 4, 5 y 15 de los requisitos funcionales y filtrados por la Fase 1 del roadmap. Los permisos citados provienen de la matriz de roles.

| ID | Requisito | Descripción | Prioridad | Criterio de aceptación |
| --- | --- | --- | --- | --- |
| RF-01 | Iniciar sesión | Todo usuario ingresa con usuario y contraseña por un login único. | Alta | Con credenciales válidas se accede; con inválidas se rechaza el acceso con mensaje y no se crea sesión. |
| RF-02 | Mantener sesión segura | El usuario puede cerrar sesión; las páginas protegidas exigen sesión activa. | Alta | Tras cerrar sesión, ninguna página protegida es accesible sin volver a autenticarse. |
| RF-03 | Menú según rol | El sistema muestra opciones diferentes según el rol del usuario. | Alta | Cada rol ve solo los módulos que la matriz le permite (verificado con un usuario de prueba por rol). |
| RF-04 | Restringir acciones según permisos | Las acciones no permitidas se bloquean aunque se intente acceder directamente (URL o petición). | Alta | 100 % de los intentos de acción no permitida en la matriz de pruebas de permisos son rechazados. |
| RF-05 | Restablecer contraseña | El administrador restablece la contraseña de un usuario. Sin recuperación por correo en la primera versión (D-04). | Baja | El usuario accede con la nueva contraseña y la anterior deja de funcionar. |
| RF-06 | Gestionar usuarios | El administrador crea y edita usuarios. | Alta | Un usuario creado puede iniciar sesión; no se permite un nombre de usuario duplicado. |
| RF-07 | Desactivar y reactivar usuarios | El administrador bloquea, desactiva o reactiva usuarios. | Media | Un usuario desactivado no puede iniciar sesión; al reactivarlo, sí. La acción queda en bitácora. |
| RF-08 | Asignar roles | El administrador asigna rol(es) a cada usuario. Un usuario puede tener varios roles (D-02). | Alta | Al cambiar el rol, cambian el menú y los permisos en el siguiente inicio de sesión. |
| RF-09 | Configurar ciclo escolar, grados y grupos | Administrador (y dirección para grupos) configuran la estructura escolar. | Alta | Todo grupo pertenece a un grado y a un ciclo escolar; no se permiten grupos duplicados en el mismo grado y ciclo. |
| RF-10 | Registrar alumnos | Registro de datos generales y matrícula del alumno (dirección, administrador). | Alta | El alumno se guarda con los datos obligatorios (nombre completo, matrícula, fecha de nacimiento, CURP y grupo; D-17); el sistema impide duplicados por matrícula. |
| RF-11 | Asociar alumno a grado, grupo y ciclo | Cada alumno queda inscrito en un grupo de un ciclo escolar. | Alta | El alumno aparece en la lista de su grupo y ciclo, y en ningún otro grupo del mismo ciclo. |
| RF-12 | Registrar padres/tutores y asociarlos | Un tutor puede tener varios alumnos y un alumno varios tutores. | Alta | Un tutor con dos hijos ve a ambos; un alumno con dos tutores es visible para los dos. |
| RF-13 | Registrar docentes y asignarlos a grupos | Alta de docentes y su asignación a uno o más grupos. | Alta | El docente ve únicamente los grupos asignados. |
| RF-14 | Editar alumnos | Edición por dirección y administrador; prefectura “limitado” \[POR DEFINIR\]. | Media | La edición se guarda y queda en bitácora con el valor anterior y el nuevo. |
| RF-15 | Registrar asistencia diaria | Prefectura marca asistencia, falta o retardo por alumno, por grupo y fecha. | Alta | Se guarda un solo registro por alumno y fecha; un segundo intento se rechaza o se trata como edición. |
| RF-16 | Modificar asistencia | Corrección de un registro de asistencia ya capturado. | Media | El cambio se guarda y la bitácora conserva quién, cuándo y qué cambió. |
| RF-17 | Consultar asistencia | Por alumno, grupo y fecha o periodo (prefectura, dirección; docente solo sus grupos). | Media | Los filtros devuelven exactamente los registros capturados en los datos de prueba. |
| RF-18 | Registrar reporte de conducta | Docente (sus grupos), prefectura y dirección registran reportes sobre un alumno. | Alta | Un docente solo puede elegir alumnos de sus grupos; el reporte queda asociado al alumno, autor y fecha. |
| RF-19 | Adjuntar evidencias | Se suben archivos como evidencia de un reporte de conducta. | Alta | El archivo se guarda y puede abrirse desde el reporte. Solo se aceptan JPG, PNG y PDF; el tamaño máximo está por confirmar (I-13). |
| RF-20 | Consultar reportes y evidencias | Prefectura y dirección ven todos; docente, los de sus grupos. | Alta | Cada rol ve exactamente los reportes que le corresponden en los datos de prueba. |
| RF-21 | Registrar incidencias disciplinarias | Prefectura registra incidencias y da seguimiento a reportes. Relación con “reporte de conducta” por confirmar (I-01). | Media | La incidencia queda asociada al alumno y es consultable por prefectura, dirección y sus tutores. |
| RF-22 | Padre/tutor consulta datos del alumno | Datos generales de sus hijos o tutorados. | Alta | Solo ve alumnos asociados; intentar abrir otro alumno (por ejemplo, cambiando el ID en la URL) es rechazado. |
| RF-23 | Padre/tutor consulta asistencia | Asistencias, faltas y retardos de sus hijos. | Alta | Los datos mostrados coinciden con lo capturado por prefectura. |
| RF-24 | Padre/tutor consulta conducta | Reportes de conducta y evidencias de sus hijos. | Alta | Ve los reportes y abre las evidencias de sus hijos; no ve los de otros alumnos. |
| RF-25 | Registrar bitácora | Quién creó, modificó o eliminó usuarios, roles, alumnos, asistencias y reportes de conducta, con fecha y hora. | Alta | Cada acción sensible de la lista genera exactamente un registro con usuario, acción, entidad y fecha/hora. |
| RF-26 | Consultar bitácora | Administrador y dirección consultan la bitácora con filtros básicos (usuario, fecha). | Media | Los filtros devuelven los registros esperados; ningún otro rol puede abrir la bitácora. |

**Cuentas de alumno:** quedan fuera de la primera versión (D-01). La consulta de asistencia propia del alumno (antes RF-27) pasa a trabajo futuro.

**Requisitos del documento general que no entran en esta versión:** justificar faltas, permisos de salida, notificaciones, mensajes a padres, tareas, calificaciones, historial académico, documentos entregados, estado administrativo y generación de reportes exportables (ver 7.3).

## Requerimientos no funcionales

Los RNF-01 a RNF-08 vienen de los requisitos no funcionales iniciales del proyecto. RNF-09 y RNF-10 son añadidos del equipo, necesarios para poder medir la calidad; se marcan como tales.

| ID | Requisito | Descripción | Método de verificación |
| --- | --- | --- | --- |
| RNF-01 | Seguridad basada en roles y permisos | Toda función valida el rol del usuario en el servidor (reglas de seguridad de Firebase o backend), no solo ocultando botones. | Matriz de pruebas rol × acción ejecutada con un usuario por rol, incluyendo accesos directos por URL. |
| RNF-02 | Registro de auditoría | Las acciones sensibles del alcance inicial quedan en bitácora (RF-25). | Ejecutar cada acción sensible y comprobar su registro en la bitácora. |
| RNF-03 | Diseño para múltiples ciclos escolares | Grupos, inscripciones y asistencias se asocian a un ciclo escolar. | Crear dos ciclos con datos de prueba y verificar que las consultas de uno no muestran datos del otro. |
| RNF-04 | Interfaz responsiva | Uso en computadora, tablet y celular. | Revisar las pantallas principales en tres anchos de pantalla (herramientas del navegador) con una lista de verificación y capturas. |
| RNF-05 | Protección de datos personales | Datos de alumnos y familias solo visibles para roles autorizados; contraseñas almacenadas cifradas con hash. | Pruebas de acceso cruzado (tutor A intenta ver alumno de tutor B) y revisión de la tabla de usuarios en la base de datos. |
| RNF-06 | Respaldos de información | Procedimiento documentado para respaldar y restaurar la base de datos. Será manual (D-20): exportación de las colecciones de Firestore a archivos. | Ejecutar al menos un respaldo y una restauración completa antes de la entrega final; conservar evidencia. |
| RNF-07 | Validaciones contra duplicidad | Se evitan alumnos, usuarios y registros de asistencia duplicados. | Casos de prueba que intentan crear cada duplicado y esperan rechazo. |
| RNF-08 | Arquitectura modular | El código se organiza por módulos para agregar fases posteriores. | Revisión de la estructura del repositorio contra el diseño de arquitectura en cada cierre de iteración. |
| RNF-09 *(añadido)* | Tiempo de respuesta | Las operaciones principales responden en menos de 3 segundos en el entorno de pruebas con los datos de prueba del equipo. | Medición con las herramientas de red del navegador sobre RF-01, RF-15, RF-20 y RF-23. |
| RNF-10 *(añadido)* | Control de versiones | Todo el código y la documentación se versionan en el repositorio del proyecto. | Historial de commits con participación de los tres integrantes. |

El requisito “posibilidad de exportar reportes en formatos comunes” se pospone a la Fase 5 junto con los reportes avanzados.

## Control de acceso y seguridad

La seguridad se trata como criterio de calidad central: un error de permisos en este sistema expone datos de menores y familias. Se aplican cinco reglas.

1. **Control de acceso basado en roles (RBAC).** Cada usuario tiene rol(es) y cada rol determina módulos y acciones permitidas, conforme a la matriz de permisos del proyecto.
2. **Restricción de módulos.** El menú muestra solo los módulos del rol (RF-03).
3. **Restricción de acciones.** El servidor valida cada acción; ocultar un botón no cuenta como control (RF-04, RNF-01).
4. **Mínimo privilegio por relación.** El docente solo accede a alumnos de sus grupos; el padre/tutor solo a sus hijos o tutorados. Estas reglas vienen de la matriz y de las reglas generales.
5. **Registro de acciones importantes.** Altas, cambios y bajas sobre usuarios, roles, alumnos, asistencia y conducta quedan en bitácora (RF-25).

**Matriz de permisos aplicable a la primera versión** (extracto literal de la matriz del proyecto; las filas de fases posteriores se omiten):

| Acción | Alumno | Padre/Tutor | Docente | Prefectura | Dirección | Administración | Administrador |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Consultar datos del alumno | Sí | Sí, de sus hijos | Sí, de sus grupos | Sí | Sí | Limitado | Sí |
| Crear alumnos | No | No | No | No | Sí | Sí | Sí |
| Editar alumnos | No | No | No | Limitado | Sí | Sí | Sí |
| Registrar asistencia | No | No | No | Sí | Sí | No | Sí |
| Consultar asistencia | Sí, propia | Sí, de sus hijos | Sí, de sus grupos | Sí | Sí | No | Sí |
| Registrar reportes de conducta | No | No | Sí | Sí | Sí | No | Sí |
| Consultar reportes de conducta | Sí, propios si aplica | Sí, de sus hijos | Sí, de sus grupos | Sí | Sí | No | Sí |
| Subir evidencias de conducta | No | No | Sí | Sí | Sí | No | Sí |
| Consultar evidencias de conducta | Sí, propias si aplica | Sí, de sus hijos | Sí, de sus grupos | Sí | Sí | No | Sí |
| Gestionar materias y grupos | No | No | No | No | Sí | No | Sí |
| Consultar bitácora | No | No | No | No | Sí | Limitado | Sí |
| Administrar usuarios y roles | No | No | No | No | No | No | Sí |

**Valores por definir:** los permisos “Limitado” y “si aplica” no están definidos en la documentación. Mientras no se definan, la primera versión los tratará como **No** (mínimo privilegio), y se registrará en control de cambios cuando se decidan (D-10, D-16, I-12).

## Criterios de calidad

La primera versión se considera de calidad solo si cumple los siete criterios siguientes, cada uno con evidencia.

| Criterio | Qué significa | Cómo se verificará | Evidencia generada |
| --- | --- | --- | --- |
| Funcionalidad | El sistema cumple los requisitos del alcance inicial. | Un caso de prueba por requisito con resultado esperado y obtenido. | Bitácora de pruebas; matriz de trazabilidad actualizada. |
| Seguridad | Cada usuario solo accede a lo que su rol permite. | Matriz de pruebas rol × acción y pruebas de acceso cruzado. | Registro de pruebas de permisos con capturas de accesos rechazados. |
| Usabilidad | Las funciones principales se completan sin ayuda. | Recorrido guiado: un integrante que no desarrolló la función completa las tareas clave (login, pasar lista, registrar reporte, consulta del tutor) sin instrucciones. | Lista de tareas con resultado (completada / con dificultad) y observaciones. |
| Integridad de datos | No hay registros duplicados ni inconsistentes. | Casos de prueba de duplicidad y de campos obligatorios (RNF-07). | Resultados de pruebas y capturas de los mensajes de validación. |
| Trazabilidad | Las acciones sensibles se pueden identificar. | Verificar que cada acción de RF-25 genera su registro. | Capturas de la bitácora con los registros generados en las pruebas. |
| Rendimiento | Respuesta ágil en las operaciones principales. | Medición de RNF-09 (menos de 3 s) con herramientas del navegador. | Tabla de mediciones con fecha y capturas. |
| Mantenibilidad | Las siguientes fases se pueden agregar sin rehacer la base. | Revisión de código por un integrante distinto al autor; estructura por módulos (RNF-08). | Revisiones registradas en el repositorio (pull requests o comentarios) y diagrama de arquitectura. |

## Metodología de trabajo

El equipo usará **Scrum adaptado a un equipo de tres integrantes**, con iteraciones (sprints) de dos semanas alineadas a las etapas de la materia.

**Justificación:**

- La materia exige avances funcionales desde la Etapa II; las iteraciones cortas producen un incremento demostrable al final de cada sprint.
- El backlog priorizado (Alta, Media, Baja) permite posponer requisitos de forma ordenada cuando falta tiempo, que es el principal riesgo del proyecto.
- Las revisiones al cierre de cada sprint coinciden con los puntos de control de la materia y generan evidencia de seguimiento.
- Se descartan ceremonias que no aportan a un equipo de tres (por ejemplo, un Scrum Master dedicado): el líder del proyecto asume esa función.

**Aplicación (calendario tentativo; se detalla en el Plan del Proyecto de la Etapa II):**

| Sprint | Fechas | Objetivo del sprint |
| --- | --- | --- |
| Sprint 0 | 23 sep – 6 oct | Plan de calidad, repositorio, modelo de datos inicial, prototipos. |
| Sprint 1 | 7 – 20 oct | Autenticación, roles, usuarios, ciclo/grados/grupos, bitácora base (RF-01 a RF-09, RF-25). |
| Sprint 2 | 21 oct – 3 nov | Alumnos, tutores, docentes y asistencia (RF-10 a RF-17). |
| Sprint 3 | 4 – 17 nov | Conducta, evidencias, vista de padres/tutores y consulta de bitácora (RF-18 a RF-24, RF-26). |
| Cierre | 18 – 24 nov | Pruebas de regresión, correcciones, manual de usuario y entrega. |

**Prácticas y su relación con la calidad:**

| Práctica | Frecuencia | Aporte a la calidad |
| --- | --- | --- |
| Planeación del sprint | Inicio de cada sprint | Se revisan y aclaran los requisitos y criterios de aceptación antes de programar. |
| Reunión breve de seguimiento | 2 veces por semana | Detecta bloqueos a tiempo; se registra en la bitácora de participación. |
| Revisión del sprint | Cierre de cada sprint | Se demuestran las funciones terminadas y se calculan las métricas. |
| Retrospectiva | Cierre de cada sprint | Acciones de mejora registradas. |
| Definición de terminado | Cada requisito | Un requisito está terminado solo si su código fue revisado por otro integrante, su caso de prueba pasó y su permiso por rol fue verificado. |

**Gestión de cambios y avances:** todo cambio de alcance pasa por el procedimiento de la sección 18; el avance se mide con las métricas de la sección 16 en el tablero de gestión y el historial del repositorio.

## Organización del equipo

**Roles confirmados por el equipo.** Stephanie y Ricardo desarrollan la aplicación y Dylan construye la base de datos; los tres deben poder explicar cualquier parte del sistema en las revisiones, y nadie prueba únicamente su propio trabajo.

| Integrante | Rol | Responsabilidades | Evidencias generadas |
| --- | --- | --- | --- |
| Stephanie Ariana Medrano Vargas | Líder del proyecto; desarrollo; diseño de interfaz | Coordinar sprints y tablero; controlar cambios y decisiones; diseñar prototipos y pantallas; desarrollar autenticación, roles, vista de padres/tutores y bitácora. | Registro de cambios, actas de revisión de sprint, prototipos, commits. |
| Dylan Alexis Padilla | Responsable de análisis y documentación; responsable de base de datos | Mantener requisitos y matriz de trazabilidad; redactar los documentos de cada etapa y el manual de usuario; diseñar el modelo de datos; crear scripts, datos de prueba ficticios y procedimiento de respaldo. | Plan de calidad, requisitos, matriz de permisos, modelo de datos, reglas de seguridad de Firebase, manual de usuario, commits. |
| Ricardo Alejandro Pineda Gómez | Responsable de pruebas y calidad; desarrollo | Diseñar casos de prueba; ejecutar la matriz de permisos; llevar la bitácora de pruebas y las métricas; desarrollar alumnos, tutores, docentes, asistencia y conducta. | Casos de prueba, bitácora de pruebas, registro de métricas, commits. |

**Reglas del equipo:**

- Cada integrante registra su trabajo en la **bitácora de participación** (fecha, actividad, responsable, evidencia, tiempo empleado, resultado).
- Todo cambio de código lo revisa un integrante distinto a su autor antes de integrarse.
- Las decisiones de alcance se toman por consenso de los tres; si no lo hay, decide el líder y queda registrado.

## Tecnologías y herramientas

Las tecnologías principales están definidas. El framework, el reparto entre JavaScript y Python y el almacenamiento de evidencias quedan como decisiones futuras (CC-03), con fecha límite en la sección 20. La elección es libre según la materia, pero debe ser congruente con el proyecto y quedar decidida antes del cierre de la Etapa I (D-22).

| Categoría | Tecnología | Propósito |
| --- | --- | --- |
| Lenguaje de programación | JavaScript y Python (reparto entre frontend y backend \[POR DEFINIR\], I-14) | Desarrollo del sistema. |
| Framework | \[TECNOLOGÍA POR DEFINIR\]; el frontend usará las plantillas del framework (HTML, CSS y JavaScript) | Estructura de la aplicación web responsiva. |
| Base de datos | Firebase (Cloud Firestore, base de datos NoSQL de documentos) | Almacenamiento de usuarios, alumnos, asistencia, conducta y bitácora. |
| Almacenamiento de evidencias | \[DECISIÓN PENDIENTE\]: se eligió guardarlas dentro de la base de datos, pero Firestore admite como máximo 1 MiB por documento (I-13) | Archivos adjuntos a reportes de conducta. |
| Control de versiones | Git | Historial de cambios y evidencia de participación. |
| Repositorio remoto | GitHub — github.com/StephAmv/nexoEdu | Alojamiento del código y la documentación. |
| Gestión del proyecto | GitHub Projects | Backlog, tablero de sprints y seguimiento. |
| Diseño y prototipos | draw.io | Prototipos de interfaz y diagramas. |
| Pruebas | \[TECNOLOGÍA POR DEFINIR\] | Registro de casos de prueba; pruebas automatizadas si el equipo las adopta. |
| Documentación | \[TECNOLOGÍA POR DEFINIR\] | Plan de calidad, reportes y manual de usuario. |

**Restricción de plataforma:** nexoEdu será una aplicación web responsiva (D-05) y no tendrá app nativa en este periodo (D-06). El lenguaje y el framework deben elegirse para desarrollo web.

## Métricas e indicadores de calidad

Nueve métricas, todas calculables con una hoja de cálculo, el tablero de gestión y el historial del repositorio. Se reportan al cierre de cada sprint.

| ID | Métrica | Fórmula | Meta | Frecuencia | Responsable | Evidencia |
| --- | --- | --- | --- | --- | --- | --- |
| M-01 | Requisitos cumplidos | RF aceptados / RF comprometidos × 100 | 100 % de RF Alta; ≥ 80 % del total | Cierre de sprint | Pruebas y calidad | Matriz de trazabilidad |
| M-02 | Pruebas satisfactorias | Casos aprobados / casos ejecutados × 100 | ≥ 90 % antes de la entrega final | Cierre de sprint | Pruebas y calidad | Bitácora de pruebas |
| M-03 | Cobertura de pruebas de permisos | Combinaciones rol × acción probadas / combinaciones definidas × 100 | 100 %, todas aprobadas | Cierre de sprint | Pruebas y calidad | Matriz de pruebas de permisos |
| M-04 | Errores detectados | Conteo por prioridad (alta, media, baja) | Seguimiento; sin meta numérica | Semanal | Pruebas y calidad | Bitácora de pruebas |
| M-05 | Errores corregidos | Errores cerrados / errores detectados × 100 | 100 % de prioridad alta; ≥ 80 % del total al cierre | Semanal | Líder del proyecto | Bitácora de pruebas; commits de corrección |
| M-06 | Cumplimiento de actividades | Tareas terminadas / tareas planificadas del sprint × 100 | ≥ 80 % por sprint | Cierre de sprint | Líder del proyecto | Tablero de gestión |
| M-07 | Cambios solicitados y aprobados | Conteo de solicitudes; aprobados / solicitados | 100 % de cambios con registro y decisión | Cierre de sprint | Líder del proyecto | Registro de cambios |
| M-08 | Incidencias abiertas y cerradas | Conteo de abiertas vs. cerradas | 0 incidencias de prioridad alta abiertas en la entrega final | Semanal | Pruebas y calidad | Tablero o bitácora de pruebas |
| M-09 | Participación del equipo | Horas y actividades por integrante / total del equipo | Cada integrante con actividades registradas en todos los sprints | Cierre de sprint | Análisis y documentación | Bitácora de participación; historial de commits |

El tiempo de respuesta (RNF-09) se mide como parte de las pruebas, no como métrica de seguimiento semanal.

## Plan de aseguramiento y control de calidad

La calidad se revisa en cada paso del desarrollo, no solo al final. Estas son las actividades y su momento.

| Actividad | Momento | Responsable | Qué se revisa |
| --- | --- | --- | --- |
| Revisión de requisitos | Planeación de cada sprint | Todo el equipo | Que cada requisito sea claro, esté dentro del alcance y tenga criterio de aceptación. |
| Revisión de diseño | Antes de programar cada módulo | Autor + un revisor | Modelo de datos, relaciones (alumno–tutor, docente–grupo) y asociación con ciclo escolar. |
| Revisión de código | Antes de integrar cada cambio | Integrante distinto al autor | Legibilidad, estructura por módulos, validación de permisos en el servidor. |
| Pruebas funcionales | Al terminar cada requisito | Pruebas y calidad | Caso de prueba del requisito con resultado esperado y obtenido. |
| Validación de permisos | Cierre de cada sprint | Pruebas y calidad | Matriz rol × acción y accesos cruzados. |
| Validación de datos | Al terminar cada formulario | Pruebas y calidad | Campos obligatorios, formatos y duplicados. |
| Pruebas de regresión | Cierre (18–24 nov) | Todo el equipo | Todos los casos de prueba de nuevo sobre la versión final. |

**Flujo de manejo de errores:**

1. **Detectar** — Se encuentra un error al probar o revisar.
2. **Registrar** — Se anota en la bitácora de pruebas: funcionalidad probada, fecha, responsable, resultado esperado, resultado obtenido, error detectado, nivel de prioridad, acción correctiva y estado final (campos que pide la Etapa IV).
3. **Corregir** — El responsable asignado corrige y referencia el ID del error en el commit.
4. **Verificar** — Un integrante distinto al que corrigió repite la prueba.
5. **Cerrar** — Si la prueba pasa, el error se marca como cerrado; si no, vuelve al paso 3.

**Prioridad de errores:** alta (bloquea una función o expone datos a un rol no autorizado), media (la función opera con un defecto) y baja (detalle visual o de texto).

## Control de cambios

Ningún cambio al alcance, a los requisitos o a este plan se implementa sin registro y decisión. Este plan (versión 1.0) es la línea base.

**Procedimiento:**

1. Cualquier integrante (o la docente) propone el cambio y se registra con un ID.
2. El líder analiza el impacto en tiempo, complejidad, recursos, requisitos, calidad y alcance.
3. El equipo decide: **aprobar**, **rechazar** o **posponer** (al backlog de trabajo futuro).
4. Si se aprueba, se actualizan los documentos afectados (requisitos, trazabilidad, plan) con nueva versión.
5. Se implementa y se verifica como cualquier requisito; luego se cierra.

**Reglas para proteger la viabilidad:**

- Un cambio que agregue funciones de las fases 2 a 5 se pospone por defecto.
- Un cambio que ponga en riesgo un requisito de prioridad Alta se rechaza o se compensa retirando un requisito de prioridad Media o Baja.
- Después del 17 de noviembre solo se aceptan correcciones de errores, no funciones nuevas.
- Resolver una decisión pendiente (sección 20) también se registra como cambio.

**Registro de cambios:**

| ID | Fecha | Cambio solicitado | Motivo | Impacto | Prioridad | Decisión | Responsable | Estado |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| CC-00 | \[POR COMPLETAR\] | Establecer la línea base del alcance: Fase 1 del roadmap, RF-01 a RF-26 | Inicio del proyecto | Define el alcance comprometido | Alta | Aprobado | Líder del proyecto | Cerrado |
| CC-01 | 30 sep 2026 | Resolver D-01, D-02, D-03, D-05 y D-06 | Decisiones requeridas antes del cierre de la Etapa I | Sin cuentas de alumno (sale RF-27); modelo usuario–rol con varios roles; solo el Administrador crea usuarios; plataforma solo web responsiva | Alta | Aprobado | Líder del proyecto | Cerrado |
| CC-02 | 30 sep 2026 | Definir tecnologías y resolver D-04, D-11, D-15, D-17 a D-21 y D-23 (tipos) | Completar el Plan de Calidad | Firebase como base de datos; datos obligatorios de alumno y tutor; sin recuperación por correo; respaldo manual; consultas sin reportes adicionales. Abre I-13 e I-14 | Alta | Aprobado | Líder del proyecto | Cerrado |
| CC-03 | 6 oct 2026 | Posponer I-13 (almacenamiento y tamaño de evidencias) e I-14 (framework y reparto JavaScript/Python) | Requieren analizar opciones fuera de la Etapa I | I-14 bloquea el inicio del código; I-13 bloquea RF-19 | Alta | Pospuesto | Líder del proyecto | Abierto |
| CC-04 |  |  |  |  |  |  |  |  |

## Riesgos relacionados con la calidad

Los dos riesgos más altos son el crecimiento del alcance y la falta de tiempo: el alcance inicial ya es exigente para tres personas en nueve semanas.

| ID | Riesgo | Probabilidad | Impacto | Nivel | Mitigación | Responsable |
| --- | --- | --- | --- | --- | --- | --- |
| R-01 | Crecimiento excesivo del alcance (agregar funciones de otras fases) | Alta | Alto | Alto | Línea base CC-00; reglas de control de cambios; posponer por defecto. | Líder del proyecto |
| R-02 | Falta de tiempo para completar el alcance | Alta | Alto | Alto | Prioridades Alta/Media/Baja; entregar primero los RF Alta; revisión de M-06 en cada sprint. | Líder del proyecto |
| R-03 | Decisiones pendientes sin resolver bloquean el desarrollo | Media | Alto | Alto | Fecha límite por decisión (sección 20); valor por defecto de mínimo privilegio mientras tanto. | Líder del proyecto |
| R-04 | Errores de permisos que exponen datos a roles no autorizados | Media | Alto | Alto | Validación en servidor; matriz de pruebas de permisos al 100 % (M-03). | Pruebas y calidad |
| R-05 | Manejo incorrecto de datos sensibles (contraseñas, datos de alumnos, evidencias) | Media | Alto | Alto | Contraseñas con hash; solo datos de prueba ficticios; evidencias accesibles solo por rol. | Base de datos |
| R-06 | Requisitos ambiguos (“Limitado”, “si aplica”, reporte vs. incidencia) | Alta | Medio | Alto | Registro de inconsistencias (sección 21); criterio de aceptación por requisito. | Análisis y documentación |
| R-07 | Falta de pruebas por dejarlas al final | Media | Alto | Alto | Definición de terminado exige caso de prueba aprobado. | Pruebas y calidad |
| R-08 | Problemas de integración entre módulos (roles, alumnos, asistencia, conducta) | Media | Medio | Medio | Modelo de datos revisado antes de programar; integración continua en la rama principal. | Base de datos |
| R-09 | Dependencia excesiva de una persona | Media | Alto | Alto | Revisión cruzada de código y de base de datos; cada integrante documenta su parte; bitácora de participación. | Líder del proyecto |
| R-10 | Cambios tardíos que desestabilizan la versión final | Media | Alto | Alto | Congelamiento de funciones después del 17 de noviembre. | Líder del proyecto |
| R-11 | Tecnologías elegidas tarde o poco conocidas por el equipo | Media | Medio | Medio | Decidir el framework antes del Sprint 1 (7 de octubre) y el almacenamiento de evidencias antes del Sprint 3 (4 de noviembre), priorizando lo que el equipo ya domina. | Todo el equipo |

Nivel = combinación de probabilidad e impacto (probabilidad Alta con impacto Alto o Medio, o probabilidad Media con impacto Alto = Alto; Media/Medio = Medio).
