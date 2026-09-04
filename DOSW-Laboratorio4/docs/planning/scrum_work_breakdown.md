# 📄 Planeación del Sistema

## Desglose de trabajo: Épicas, Historias de Usuario y Tareas

La implementación de los requerimientos identificados de TechCup se desglosa de la siguiente manera:

### 1. Épica:

| Campo | Descripción |
|------|-------------|
| **ID** | SCRUM-5 |
| **Título** | TechCup |
| **Descripción** | TechCup necesita esta épica para centralizar, administrar y controlar la inscripción y participación de los equipos de estudiantes en el torneo semestral de fútbol de la Escuela Colombiana de Ingeniería, garantizando el cumplimiento de las reglas de negocio (como la inscripción exclusiva en torneos activos y la asociación de integrantes) de manera digital, segura y estructurada. |
| **Stakeholder** | Capitanes de equipo (estudiantes de Sistemas, IA, Ciberseguridad y Estadística), Organizadores del torneo TechCup y Decanatura |

### 1.1 Feature:

| Campo | Descripción |
|------|-------------|
| **ID** | SCRUM-6 |
| **Título** | Registro de Equipos en el Torneo Activo (RF-02) |
| **Descripción** | Permitir a los capitanes autenticados registrar un equipo e inscribir a sus compañeros/integrantes en el torneo de fútbol que se encuentre en estado *Active*, validando los datos requeridos para habilitar su participación en el torneo y preparar el proceso de pago de inscripción. |
| **Stakeholder** | Capitán (Captain) y Organizadores del torneo |

### 2. Historias de usuario:

| Campo | Descripción |
|------|-------------|
| **ID** | SCRUM-13 |
| **Título** | Autenticación del capitán para registrar equipo |
| **Descripción** | *Como capitán, quiero iniciar sesión en TechCup con mi nombre de usuario y contraseña, para poder acceder de forma segura a la opción de registro de equipo.* |
| **Criterios de aceptación** | 1. Dado que el capitán ingresa un usuario y contraseña válidos, cuando envíe el formulario, entonces el sistema le concede acceso y lo redirige al módulo de registro de equipo.<br>2. Dado que el capitán ingresa credenciales inválidas, cuando envíe el formulario, entonces el sistema muestra un mensaje de error sin conceder acceso.<br>3. Dado que el capitán deja campos vacíos, cuando intente iniciar sesión, entonces el sistema le indica qué campos son obligatorios. |
| **Prioridad** | *Alta* |
| **Estimación** | *5 puntos de historia* |
 
| Campo | Descripción |
|------|-------------|
| **ID** | SCRUM-14 |
| **Título** | Validación de torneo activo antes del registro |
| **Descripción** | *Como capitán, quiero que el sistema verifique que exista un torneo en estado Active, para poder registrar mi equipo únicamente cuando la inscripción se encuentre habilitada.* |
| **Criterios de aceptación** | 1. Dado que existe un torneo en estado Active, cuando el capitán ingrese al módulo de registro, entonces el sistema habilita la opción de registrar equipo.<br>2. Dado que no existe ningún torneo en estado Active, cuando el capitán intente acceder al registro, entonces el sistema bloquea la acción y muestra un mensaje explicativo.<br>3. Dado que existe más de un torneo, cuando el sistema realice la verificación, entonces solo considera el torneo cuyo estado sea Active. |
| **Prioridad** | *Alta* |
| **Estimación** | *5 puntos de historia* |
 
| Campo | Descripción |
|------|-------------|
| **ID** | SCRUM-15 |
| **Título** | Registro de datos del equipo e integrantes |
| **Descripción** | *Como capitán, quiero ingresar el nombre del equipo y los datos de mis compañeros/integrantes, para poder inscribir formalmente al equipo en el torneo activo.* |
| **Criterios de aceptación** | 1. Dado que el capitán diligencia el nombre del equipo y el número mínimo de integrantes requerido, cuando envíe el formulario, entonces el sistema registra el equipo y lo asocia al torneo activo.<br>2. Dado que el capitán ingresa un número de integrantes fuera del rango permitido, cuando intente enviar el formulario, entonces el sistema rechaza el registro e indica el rango válido.<br>3. Dado que un estudiante ya pertenece a otro equipo en el mismo torneo, cuando el capitán intente inscribirlo, entonces el sistema impide agregarlo y muestra un mensaje de duplicidad. |
| **Prioridad** | *Alta* |
| **Estimación** | *5 puntos de historia* |
 
| Campo | Descripción |
|------|-------------|
| **ID** | SCRUM-16 |
| **Título** | Confirmación del registro exitoso del equipo |
| **Descripción** | *Como capitán, quiero recibir una confirmación visible tras registrar mi equipo, para poder tener certeza de que quedó inscrito en el torneo.* |
| **Criterios de aceptación** | 1. Dado que el equipo se registró exitosamente, cuando el sistema termine de procesar la solicitud, entonces muestra al capitán un mensaje de confirmación con el nombre del equipo y el torneo asociado.<br>2. Dado que el equipo quedó registrado, cuando un organizador consulte los equipos del torneo, entonces el equipo aparece visible en el listado.<br>3. Dado que ocurre un error al registrar el equipo, cuando el sistema detecte la falla, entonces informa al capitán que el registro no se completó, sin mostrar una confirmación falsa. |
| **Prioridad** | *Media* |
| **Estimación** | *3 puntos de historia* |

### 3. Tareas:

| Campo | Descripción |
|------|-------------|
| **ID** | SCRUM-17 |
| **Título** | CONECTAR BASE DE DATOS AL SOFTWARE |
| **ID de la Historia de Uso asociada** | SCRUM-13 |
| **Descripción** | *Como desarrollador, quiero conectar la base de datos al software , para poder realizar consultas.*  |
| **Tareas requisito** | *NINGUNA*|

| Campo | Descripción |
|------|-------------|
| **ID** | SCRUM-18 |
| **Título** | *RECIBIR DATOS*|
| **ID de la Historia de Uso asociada** | SCRUM-13 |
| **Descripción** | *Como desarrollador, quiero poder recibir datos, para poder realizar consultas en mi base de datos.*  |
| **Tareas requisito** | *SCRUM-17* |

| Campo | Descripción |
|------|-------------|
| **ID** | SCRUM-19 |
| **Título** | *CONSULTA BASE DE DATOS*|
| **ID de la Historia de Uso asociada** | SCRUM-13 |
| **Descripción** | *Como desarrollador, quiero poder realizar consultas, para poder realizar validaciones de datos.*  |
| **Tareas requisito** | *SCRUM-17* |

| Campo | Descripción |
|------|-------------|
| **ID** | SCRUM-20 |
| **Título** | *PODER CREAR TORNEOS*|
| **ID de la Historia de Uso asociada** | SCRUM-14 |
| **Descripción** | *Como desarrollador, quiero crear torneos en mi base de datos, para poder .incribir personas en mi torneo*  |
| **Tareas requisito** | *SCRUM-17,SCRUM-19* |

| Campo | Descripción |
|------|-------------|
| **ID** | SCRUM-21 |
| **Título** | *CONSULTAR ESTADO DE TORNEO ACTIVO*|
| **ID de la Historia de Uso asociada** | SCRUM-14 |
| **Descripción** | *Como desarrollador, quiero crear un endpoint o consulta en la base de datos que busque y retorne únicamente el torneo que tenga el estado "Active", para saber si las inscripciones deben estar abiertas.*  |
| **Tareas requisito** | *SCRUM-17,SCRUM-19* |

| Campo | Descripción |
|------|-------------|
| **ID** | SCRUM-23 |
| **Título** | *BLOQUEO O HABILITACIÓN DE INTERFAZ DE REGISTRO*|
| **ID de la Historia de Uso asociada** | SCRUM-14 |
| **Descripción** | *Como desarrollador, quiero implementar lógica en el frontend que consulte el torneo activo y, si no existe, bloquee la pantalla de registro mostrando un mensaje explicativo al usuario.*  |
| **Tareas requisito** | *SCRUM-21* |

| Campo | Descripción |
|------|-------------|
| **ID** | SCRUM-22 |
| **Título** | *CREAR FORMULARIO DE REGISTRO DE EQUIPOS*|
| **ID de la Historia de Uso asociada** | SCRUM-15 |
| **Descripción** | *Como desarrollador, quiero construir un formulario en la interfaz de usuario que permita ingresar el nombre del equipo y agregar dinámicamente los campos requeridos para los integrantes (respetando el mínimo y máximo de jugadores).*  |
| **Tareas requisito** | *SCRUM-23* |

| Campo | Descripción |
|------|-------------|
| **ID** | SCRUM-24 |
| **Título** | *VALIDAR DUPLICADOS Y GUARDAR EQUIPO*|
| **ID de la Historia de Uso asociada** | SCRUM-15 |
| **Descripción** | *Como desarrollador, quiero crear la lógica en el backend que reciba los datos del formulario, valide que ningún estudiante esté ya inscrito en otro equipo del mismo torneo, y finalmente guarde los datos en la base de datos.*  |
| **Tareas requisito** | *SCRUM-17,SCRUM-18,SCRUM-22* |

| Campo | Descripción |
|------|-------------|
| **ID** | SCRUM-25 |
| **Título** | *VALIDACIÓN DE LÍMITES DE INTEGRANTES EN EL FRONTEND*|
| **ID de la Historia de Uso asociada** | SCRUM-15 |
| **Descripción** | *Como desarrollador, quiero implementar validaciones en el formulario de registro para evitar que se envíen los datos si el número de integrantes es menor al mínimo requerido o mayor al máximo permitido, mostrando un mensaje de error con el rango válido.*  |
| **Tareas requisito** | *SCRUM-22* |

| Campo | Descripción |
|------|-------------|
| **ID** | SCRUM-26 |
| **Título** | *CREAR COMPONENTE DE ALERTA O MENSAJE DE ESTADO*|
| **ID de la Historia de Uso asociada** | SCRUM-16 |
| **Descripción** | *Como desarrollador, quiero crear un componente en la interfaz que reciba la respuesta del proceso de registro y muestre al usuario un mensaje de confirmación exitosa (incluyendo nombre de equipo y torneo) o un mensaje de error si el proceso falla.*  |
| **Tareas requisito** | *SCRUM-24* |

| Campo | Descripción |
|------|-------------|
| **ID** | SCRUM-27 |
| **Título** | *IMPLEMENTAR RESPUESTAS DE ÉXITO Y ERROR EN BACKEND*|
| **ID de la Historia de Uso asociada** | SCRUM-16 |
| **Descripción** | *Como desarrollador, quiero asegurar que el endpoint de registro devuelva la información detallada (nombre del equipo y torneo) cuando el registro es exitoso, y un código de error claro si falla, para que el frontend pueda procesarlo.*  |
| **Tareas requisito** | *SCRUM-24* |

| Campo | Descripción |
|------|-------------|
| **ID** | SCRUM-28 |
| **Título** | *CREAR CONSULTA Y VISTA DE EQUIPOS INSCRITOS*|
| **ID de la Historia de Uso asociada** | SCRUM-16 |
| **Descripción** | *Como desarrollador, quiero implementar una consulta a la base de datos y una vista para los organizadores, de manera que puedan ver el listado actualizado de los equipos registrados en el torneo activo.*  |
| **Tareas requisito** | *SCRUM-19,SCRUM-24* |
