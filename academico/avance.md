# Avance de la nueva aplicación web académico para el Colegio DonBosco-Sucre en todos sus turnos, utilizando el Stack MERN

[mern-stack]: ./img/mern-stack.png "MERN STACK"

---

### MERN

Esta pila de tecnologías permite construir fácilmente una arquitectura de tres niveles (__front-end, back-end, base de datos__) completamente usando JavaScript y JSON.

![Imagen][mern-stack]

## Sistema Académico Backend

### Tecnologías

Actualmente se está utilizando la ultimas versiones de:

* __NodeJS:__ >= v18.12.1
* __MongoDB:__ >= v6.0.2
* __Mongosh:__ >= v1.6.0

### Librerías Utilizadas

Solo se implementó librerias específicas mientras se avanza en los módulos, esto dá como resultado código mas ligero y rapido acceso.

__Librerías para Módulo DB:__

* __mongoose:__ >= v6.6.5

>Mongoose es una herramienta de modelado de objetos MongoDB diseñada para trabajar en un entorno asíncrono.

* __bcryptjs:__ >= v2.4.3

>bcrypt es una librería para encriptar contraseñas, ayuda en la seguridad optimizado en JavaScript con cero dependencias

* __chalk:__ >= v5.1.2

>Estilo de cadena de terminales bien hecho, se utiliza para vizualizar y configurar la base de datos a un estado inicial

* __debug:__ >= v4.3.4

>Una pequeña utilidad de depuración de JavaScript basada en la técnica de depuración del núcleo de NodeJS

* __dotenv:__ >= v16.0.3

>Dotenv es un módulo de dependencia cero que carga variables de entorno desde un archivo .env en process.env

* __inquirer:__ >= v9.1.4

>Una colección de interfaces de usuario de línea de comando interactivas comunes, se utiliza para configurar la Base de Datos

* __minimist:__ >= v1.2.7

>Este módulo es el corazón del analizador de argumentos optimista sin toda la decoración fantasiosa.

__Librerías para Módulo API:__

* __boom:__ >= v7.3.0

>Objetos de respuesta de auge en Express, se utiliza para especificar los errores que puedan surgir.

* __cors:__ >= v2.8.5

>Middleware para Express, es un mecanismo que utiliza cabeceras HTTP adicionales para permitir que un user agent (en-US) obtenga permiso para acceder a recursos seleccionados desde un servidor, en un origen distinto (dominio) al que pertenece.

* __debug:__ >= v4.3.4

>Utilidad ligera de depuración para NodeJS

* __dotenv:__ >= v16.0.3

>Dotenv es un módulo de dependencia cero que carga variables de entorno desde un archivo .env en process.env

* __express:__ >= v4.18.2

>Framework web minimalista, rápido y sin opiniones.

* __express-fileupload:__ >= v1.4.0

>Middleware simple de carga rápida de archivos que envuelve a Busboy.

* __helmet:__ >= v6.0.0

>Protege las aplicaciones Express/Connect con varios encabezados HTTP, ayuda en la seguridad.

* __joi:__ >= v17.7.0

>El lenguaje de descripción de esquemas y validador de datos más potente para JavaScript.

* __jsonwebtoken:__ >= v8.5.1

>Cumple con el es un estándar abierto basado en JSON propuesto por IETF (RFC 7519) para la creación de tokens de acceso que permiten la propagación de identidad y privilegios

* __module-db:__ module-db/server

>Usando el Módulo DB que se construyó.

* __morgan:__ >= v1.10.0

>Middleware de registro de solicitudes HTTP para NodeJS.

* __passport:__ >= v0.6.0

>Autenticación simple y discreta para NodeJS.

* __passport-jwt:__ >= v4.0.0

>Estrategia de autenticación de pasaporte usando tokens web JSON

* __passport-local:__ >= v1.0.0

>Estrategia de autenticación de nombre de usuario y contraseña local para Passport.

### Modulos

#### Módulo DB (Data Base)

Se realizó lo siguiente:

* Se configuró un usuario con seguridad para la base de datos module-db.
* Se Programó un script para la configuración inicial de la base de datos, con un usuario admin por defecto y vacias la base de datos
* Se configuró e implementó Docker Compose para crear una imagen de MongoDB.
* Se crearon los Esquemas de los Documentos con Mongoose como ser: User, Role, Administrativos, Academicos, Estudiantes, Materias, BancoPreguntas, SimulacroArea, SimulacroMateria, SimulacroExamen.
* Se Documento la configuración y demas detalles del sistema.
* Se implementó PrettierRC y EsLintRC para tener un código formateado y Depurado, cumpliendo así con los estándares de programación.

#### Módulo API (Application Programming Interface)

Se realizó lo siguiente:

* Se realizaron los Schemas para recibir peticiones como: authUserSchema, createUserSchema, RolSchema
* Se realizó las estrategias de autenticación: BasicStrategy, JWT y LocalStrategy.
* Se realizó los servicios que se comunican con el Módulo DB como ser: UserService, uploadFile, MateriasService, EstudiantesService, BancoPreguntasService, AuthService, AdministrativosService y AcademicosService
* Se realizaron las rutas de los endpoints como ser: authApiRouter, userApiRouter, AdministrativosApiRouter, EstudiantesApiRouter, AcademicosApiRouter, MateriasApiRouter, UploadApiRouter y BancoPreguntasApiRouter.
* Se incorporó varios middlewares de seguridad y validación, como ser: authJwt, verifySignup, verifyExist, validation, uploadFileMiddleware y verifyRol.
* Se Documento la configuración y demas detalles del sistema.
* Se implementó PrettierRC y EsLintRC para tener un código formateado y Depurado, cumpliendo así con los estándares de programación.

---

## Sistema Académico FrontEnd

### Tecnologías

Se implementó las nuevas tecnologías de ReactJS con Vite.

* __react:__ >= v18.2.0
* __npm:__ >= v8.19.2
* __yarn:__ >= v1.22.19
* __vite:__ >= v3.2.4

### Librerías Utilizadas

* __@tailwindcss/forms:__ >= v0.5.2
* __chart.js:__ >= v3.8.0
* __chartjs-adapter-moment:__ >= v1.0.0
* __moment:__ >= v2.29.4
* __@reduxjs/toolkit:__ ~1.9.0
* __axios:__ >= v1.2.0
* __react:__ >= v18.2.0
* __react-dom:__ >= v18.2.0
* __react-flatpickr:__ >= v3.10.13
* __react-router-dom:__ >= v6.4.3
* __react-transition-group:__ >= v4.4.2
* __react-redux:__ >= v8.0.5
* __react-tsparticles:__ >= v2.6.0
* __redux-persist:__ >= v6.0.0
* __redux-thunk:__ >= v2.4.2
* __sweetalert2:__ >= v11.6.15
* __tsparticles:__ >= v2.6.
* __@types/react:__ >= v18.0.24
* __@types/react-dom:__ >= v18.0.8
* __@vitejs/plugin-react:__ >= v2.2.0
* __autoprefixer:__ >= v10.4.13
* __eslint:__ >= v8.29.0
* __postcss:__ >= v8.4.19
* __prettier:__ >= v2.8.0
* __tailwindcss:__ >= v3.2.4

### Modulos

* Se implementó Redux al proyecto a partir de Store, Slices con Thunks.
* Se implementó varias utilidades para configurar la fecha regional y demas funciones para la aplicación en general.
* Se desarrolló algunos componentes parciales para el Header, Sidebar y demás.
* Se desarrolló el diseño del Dashboard
* se desarrolló Hooks para los formularios.
* Se desarrolló varios componentes como ser: Auth, Home, UI, DatePicker, DropdownFilter, DropdownHelp, DropdownNotifications, DropdownProfile, y Modal
* Se incorporó Axios para las peticiones al Servidor.
