# 📄 Planeación del Sistema

## Desglose de trabajo: Épicas, Historias de Usuario y Tareas

La implementación de los requerimientos identificados de TechCup se desglosa de la siguiente manera:

### 1. Épica:

| Campo | Descripción |
|------|-------------|
| **ID** | EP-01 |
| **Título** | TechCup |
| **Descripción** | TechCup necesita esta épica para centralizar, administrar y controlar la inscripción y participación de los equipos de estudiantes en el torneo semestral de fútbol de la Escuela Colombiana de Ingeniería, garantizando el cumplimiento de las reglas de negocio (como la inscripción exclusiva en torneos activos y la asociación de integrantes) de manera digital, segura y estructurada. |
| **Stakeholder** | Capitanes de equipo (estudiantes de Sistemas, IA, Ciberseguridad y Estadística), Organizadores del torneo TechCup y Decanatura |

### 1.1 Feature:

| Campo | Descripción |
|------|-------------|
| **ID** | FT-01 |
| **Título** | Registro de Equipos en el Torneo Activo (RF-02) |
| **Descripción** | Permitir a los capitanes autenticados registrar un equipo e inscribir a sus compañeros/integrantes en el torneo de fútbol que se encuentre en estado *Active*, validando los datos requeridos para habilitar su participación en el torneo y preparar el proceso de pago de inscripción. |
| **Stakeholder** | Capitán (Captain) y Organizadores del torneo |

### 2. Historias de usuario:

| Campo | Descripción |
|------|-------------|
| **ID** | HU-01 |
| **Título** | Autenticación del capitán para registrar equipo |
| **Descripción** | *Como capitán, quiero iniciar sesión en TechCup con mi nombre de usuario y contraseña, para poder acceder de forma segura a la opción de registro de equipo.* |
| **Criterios de aceptación** | 1. Dado que el capitán ingresa un usuario y contraseña válidos, cuando envíe el formulario, entonces el sistema le concede acceso y lo redirige al módulo de registro de equipo.<br>2. Dado que el capitán ingresa credenciales inválidas, cuando envíe el formulario, entonces el sistema muestra un mensaje de error sin conceder acceso.<br>3. Dado que el capitán deja campos vacíos, cuando intente iniciar sesión, entonces el sistema le indica qué campos son obligatorios. |
| **Prioridad** | *Alta* |
| **Estimación** | *3 puntos de historia* |
 
| Campo | Descripción |
|------|-------------|
| **ID** | HU-02 |
| **Título** | Validación de torneo activo antes del registro |
| **Descripción** | *Como capitán, quiero que el sistema verifique que exista un torneo en estado Active, para poder registrar mi equipo únicamente cuando la inscripción se encuentre habilitada.* |
| **Criterios de aceptación** | 1. Dado que existe un torneo en estado Active, cuando el capitán ingrese al módulo de registro, entonces el sistema habilita la opción de registrar equipo.<br>2. Dado que no existe ningún torneo en estado Active, cuando el capitán intente acceder al registro, entonces el sistema bloquea la acción y muestra un mensaje explicativo.<br>3. Dado que existe más de un torneo, cuando el sistema realice la verificación, entonces solo considera el torneo cuyo estado sea Active. |
| **Prioridad** | *Alta* |
| **Estimación** | *2 puntos de historia* |
 
| Campo | Descripción |
|------|-------------|
| **ID** | HU-03 |
| **Título** | Registro de datos del equipo e integrantes |
| **Descripción** | *Como capitán, quiero ingresar el nombre del equipo y los datos de mis compañeros/integrantes, para poder inscribir formalmente al equipo en el torneo activo.* |
| **Criterios de aceptación** | 1. Dado que el capitán diligencia el nombre del equipo y el número mínimo de integrantes requerido, cuando envíe el formulario, entonces el sistema registra el equipo y lo asocia al torneo activo.<br>2. Dado que el capitán ingresa un número de integrantes fuera del rango permitido, cuando intente enviar el formulario, entonces el sistema rechaza el registro e indica el rango válido.<br>3. Dado que un estudiante ya pertenece a otro equipo en el mismo torneo, cuando el capitán intente inscribirlo, entonces el sistema impide agregarlo y muestra un mensaje de duplicidad. |
| **Prioridad** | *Alta* |
| **Estimación** | *5 puntos de historia* |
 
| Campo | Descripción |
|------|-------------|
| **ID** | HU-04 |
| **Título** | Confirmación del registro exitoso del equipo |
| **Descripción** | *Como capitán, quiero recibir una confirmación visible tras registrar mi equipo, para poder tener certeza de que quedó inscrito en el torneo.* |
| **Criterios de aceptación** | 1. Dado que el equipo se registró exitosamente, cuando el sistema termine de procesar la solicitud, entonces muestra al capitán un mensaje de confirmación con el nombre del equipo y el torneo asociado.<br>2. Dado que el equipo quedó registrado, cuando un organizador consulte los equipos del torneo, entonces el equipo aparece visible en el listado.<br>3. Dado que ocurre un error al registrar el equipo, cuando el sistema detecte la falla, entonces informa al capitán que el registro no se completó, sin mostrar una confirmación falsa. |
| **Prioridad** | *Media* |
| **Estimación** | *2 puntos de historia* |

### 3. Tareas:

| Campo | Descripción |
|------|-------------|
| **ID** | TR-01 |
| **Título** | |
| **ID de la Historia de Uso asociada** | HU-01 |
| **Descripción** | *Como [tipo de usuario] quiero [necesidad o acción] para [beneficio u objetivo]* |
| **Tareas requisito** | *Id de las tareas de las cuales es dependiente* |
