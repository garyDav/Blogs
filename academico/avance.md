# Avance de la nueva aplicación web académico para el Colegio DonBosco-Sucre en todos sus turnos, utilizando el Stack MERN

[mern-stack]: ./img/mern-stack.png 'MERN STACK'
[workspace]: ./img/workspace.png 'MODULOS DEL SISTEMA'

---

### MERN

Esta pila de tecnologías permite construir fácilmente una arquitectura de tres niveles (**front-end, back-end, base de datos**) completamente usando JavaScript y JSON.

![Imagen][mern-stack]

### Módulos necesarios para ejecutar la aplicación.

Estos son los módulos necesarios y requeridos para el uso de todo el sistema.

![Imagen][workspace]

## Sistema Académico Backend

### Tecnologías

Actualmente se está utilizando la ultimas versiones de:

- **NodeJS:** >= v18.12.1
- **MongoDB:** >= v6.0.2
- **Mongosh:** >= v1.6.0

### Librerías Utilizadas

Solo se implementó librerias específicas mientras se avanza en los módulos, esto dá como resultado código mas ligero y rapido acceso.

**Librerías para Módulo DB:**

- **bcryptjs:** >= v2.4.3

> bcrypt es una librería para encriptar contraseñas, ayuda en la seguridad optimizado en JavaScript con cero dependencias

- **chalk:** >= v5.1.2

> Estilo de cadena de terminales bien hecho, se utiliza para vizualizar y configurar la base de datos a un estado inicial

- **debug:** >= v4.3.4

> Una pequeña utilidad de depuración de JavaScript basada en la técnica de depuración del núcleo de NodeJS

- **dotenv:** >= v16.0.3

> Dotenv es un módulo de dependencia cero que carga variables de entorno desde un archivo .env en process.env

- **inquirer:** >= v9.1.4

> Una colección de interfaces de usuario de línea de comando interactivas comunes, se utiliza para configurar la Base de Datos

- **minimist:** >= v1.2.7

> Este módulo es el corazón del analizador de argumentos optimista sin toda la decoración fantasiosa.

- **mongoose:** >= v6.6.5

> Mongoose es una herramienta de modelado de objetos MongoDB diseñada para trabajar en un entorno asíncrono.

- **mongoose-paginate-v2:** >= v1.7.1

> mongoose-paginate-v2 es una biblioteca de paginación que tiene un contenedor de página. El uso principal del complemento es que puede modificar las claves de valor de retorno directamente en la consulta misma para que no necesite ningún código adicional para la transformación.

- **mongoose-sequence:** >= v5.3.1

> Este complemento le permite crear campos que incrementan automáticamente su valor. cada vez que se inserta un nuevo documento en una colección, ó cuando quieres incrementarlos explícitamente.

- **xlsx:** >= 0.18.5

> SheetJS Community Edition ofrece soluciones de código abierto probadas en batalla para extraer datos útiles de casi cualquier hoja de cálculo compleja y generar nuevas hojas de cálculo que funcionarán con software heredado y moderno por igual.

---

**Librerías para Módulo API:**

- **boom:** >= v7.3.0

> Objetos de respuesta de auge en Express, se utiliza para especificar los errores que puedan surgir.

- **cors:** >= v2.8.5

> Middleware para Express, es un mecanismo que utiliza cabeceras HTTP adicionales para permitir que un user agent (en-US) obtenga permiso para acceder a recursos seleccionados desde un servidor, en un origen distinto (dominio) al que pertenece.

- **debug:** >= v4.3.4

> Utilidad ligera de depuración para NodeJS

- **dotenv:** >= v16.0.3

> Dotenv es un módulo de dependencia cero que carga variables de entorno desde un archivo .env en process.env

- **express:** >= v4.18.2

> Framework web minimalista, rápido y sin opiniones.

<<<<<<< HEAD
>Cumple con el estándar abierto basado en JSON propuesto por IETF (RFC 7519) para la creación de tokens de acceso que permiten la propagación de identidad y privilegios
=======
- **express-fileupload:** >= v1.4.0
>>>>>>> 656639f (Avance Enero)

> Middleware simple de carga rápida de archivos que envuelve a Busboy.

- **helmet:** >= v6.0.0

> Protege las aplicaciones Express/Connect con varios encabezados HTTP, ayuda en la seguridad.

- **joi:** >= v17.7.0

> El lenguaje de descripción de esquemas y validador de datos más potente para JavaScript.

- **jsonwebtoken:** >= v8.5.1

> Cumple con el es un estándar abierto basado en JSON propuesto por IETF (RFC 7519) para la creación de tokens de acceso que permiten la propagación de identidad y privilegios

- **module-db:** module-db/server

> Usando el Módulo DB que se construyó.

- **morgan:** >= v1.10.0

> Middleware de registro de solicitudes HTTP para NodeJS.

- **passport:** >= v0.6.0

> Autenticación simple y discreta para NodeJS.

- **passport-jwt:** >= v4.0.0

> Estrategia de autenticación de pasaporte usando tokens web JSON

- **passport-local:** >= v1.0.0

> Estrategia de autenticación de nombre de usuario y contraseña local para Passport.

- **pdfmake:** >= v0.2.7

> Biblioteca de generación de documentos PDF para uso del lado del servidor y del cliente en JavaScript puro.

### Modulos

#### Módulo DB (Data Base)

Se realizó lo siguiente:

**:spiral_calendar: Diciembre.**

- Se configuró un usuario con seguridad para la base de datos module-db.
- Se Programó un script para la configuración inicial de la base de datos, con un usuario admin por defecto y vacias la base de datos
- Se configuró e implementó Docker Compose para crear una imagen de MongoDB.
- Se crearon los Esquemas de los Documentos con Mongoose como ser: User, Role, Administrativos, Academicos, Estudiantes, Materias, BancoPreguntas, SimulacroArea, SimulacroMateria, SimulacroExamen.
- Se Documento la configuración y demas detalles del sistema.
- Se implementó PrettierRC y EsLintRC para tener un código formateado y Depurado, cumpliendo así con los estándares de programación.

**:spiral_calendar: Enero.**

- Se Programó un script para **_subir_** nuevos registros de usuarios, estudiantes, y parte de la inscripción por cada estudiante, mediante un archivo Excel.
- Se Programó un script para **_bloquear_** el acceso al sistema por cada estudiante, para las inscripciones, mediante un archivo Excel.
- Se Programó un script para **_habilitar_** el acceso al sistema por cada estudiante, para las inscripciones, mediante un archivo Excel.
- Se creó el esquema del documento con Mongoose: Inscripcion.
- Se guardó y se estructuró los archivos en Excel en el directorio "xlsx". teniendo un total del 23 archivos en excel que permitieron subir, bloquear, y habilitar estudiantes.
- Se creó varios servicios para los esquemas y reportes: InscripcionService, ReportesService, UserService.
- Se realizó y documentó cómo realizar **_backup_** y **_restore_** de la base de datos con **_docker_**.

#### Módulo API (Application Programming Interface)

Se realizó lo siguiente:

**:spiral_calendar: Diciembre.**

- Se realizaron los Schemas para recibir peticiones como: authUserSchema, createUserSchema, RolSchema
- Se realizó las estrategias de autenticación: BasicStrategy, JWT y LocalStrategy.
- Se realizó los servicios que se comunican con el Módulo DB como ser: UserService, uploadFile, MateriasService, EstudiantesService, BancoPreguntasService, AuthService, AdministrativosService y AcademicosService
- Se realizaron las rutas de los endpoints como ser: authApiRouter, userApiRouter, AdministrativosApiRouter, EstudiantesApiRouter, AcademicosApiRouter, MateriasApiRouter, UploadApiRouter y BancoPreguntasApiRouter.
- Se incorporó varios middlewares de seguridad y validación, como ser: authJwt, verifySignup, verifyExist, validation, uploadFileMiddleware y verifyRol.
- Se Documento la configuración y demas detalles del sistema.
- Se implementó PrettierRC y EsLintRC para tener un código formateado y Depurado, cumpliendo así con los estándares de programación.

**:spiral_calendar: Enero.**

- Se documentó los siguientes archivos: dataRude.json, formatoRude.js, y formatoRude2.js.
- Se Programó una librería para crear y utilizar PDF a partir de pdfmake.
- Se crearon las diferentes rutas para los endpoints de la API, como ser: inscripcionRouter, reportsPDFRouter.
- Se crearon los servicios de la API-REST que se comunicarán con los servicios de Module-db: inscripcionServiceApi, reportesServiceApi.
- Se crearon los PDF para contrato y rude a partir de los servicios de reporteServiceApi.

---

## Sistema Académico FrontEnd

### Tecnologías

Se implementó las nuevas tecnologías de ReactJS con Vite.

- **react:** >= v18.2.0
- **npm:** >= v8.19.2
- **yarn:** >= v1.22.19
- **vite:** >= v3.2.4

### Librerías Utilizadas

- **@reduxjs/toolkit:** >= v1.9.0
- **@tailwindcss/forms:** >= v0.5.2
- **axios:** >= v1.2.0
- **chart.js:** >= v3.8.0
- **chartjs-adapter-moment:** >= v1.0.0
- **file-saver:** >= v2.0.5
- **moment:** >= v2.29.4
- **react:** >= v18.2.0
- **react-dom:** >= v18.2.0
- **react-flatpickr:** >= v3.10.13
- **react-image-crop:** >= v10.0.9
- **react-redux:** >= v8.0.5
- **react-router-dom:** >= v6.4.3
- **react-select:** >= v5.7.0
- **react-transition-group:** >= v4.4.2
- **react-tsparticles:** >= v2.6.0
- **redux-persist:** >= v6.0.0
- **redux-thunk:** >= v2.4.2
- **sweetalert2:** >= v11.6.15
- **tsparticles:** >= v2.6.
- **@types/react:** >= v18.0.24
- **@types/react-dom:** >= v18.0.8
- **@vitejs/plugin-react:** >= v2.2.0
- **autoprefixer:** >= v10.4.13
- **eslint:** >= v8.29.0
- **postcss:** >= v8.4.19
- **prettier:** >= v2.8.0
- **tailwindcss:** >= v3.2.4
- **vite:** >= v3.2.3

### Modulos

**:spiral_calendar: Diciembre.**

- Se implementó Redux al proyecto a partir de Store, Slices con Thunks.
- Se implementó varias utilidades para configurar la fecha regional y demas funciones para la aplicación en general.
- Se desarrolló algunos componentes parciales para el Header, Sidebar y demás.
- Se desarrolló el diseño del Dashboard
- se desarrolló Hooks para los formularios.
- Se desarrolló varios componentes como ser: Auth, Home, UI, DatePicker, DropdownFilter, DropdownHelp, DropdownNotifications, DropdownProfile, y Modal
- Se incorporó Axios para las peticiones al Servidor.

**:spiral_calendar: Enero.**

- Se desarrolló componentes para la gestión de usuarios: UserModal.jsx, UserPasswordModa.jsx, UserDropdownFilter.jsx, UserPagination.jsx, UserTable.jsx, UserTableItem.jsx.
- Se implementó las rutas y se añadió las páginas enlazadas a estas rutas para la gestión de Usuarios: ./src/pages/users/Users.jsx.
- Se implementó las rutas y se añadió las páginas enlazadas a estas rutas para los formularios de inscripciones: ./src/pages/inscripcion/Inscripcion01.jsx, .../Inscripcion02.jsx, .../Inscripcion03.jsx, .../Inscripcion04.jsx, .../Inscripcion05.jsx, .../Inscripcion06.jsx, .../Inscripcion07.jsx, .../Inscripcion08.jsx.
- Se incorporó los diferentes slices y thunks para usuarios en: ./src/store/slices/users/thunks.js, .../usersSlice.js.
- Se incorporó los diferentes slices y thunks para inscripcion en: ./src/store/slices/inscripcion/thunks.js, .../inscripcionSlice.js.
- Se refactorizó algunas utilidades y compomentes: ./src/utils/_, ./src/components/_.
