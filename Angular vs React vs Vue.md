# Angular vs React vs Vue

## Frameworks Similitudes

* __Open Source__
  Cualquier persona pueda tomar codigo que existe y variarlo, para dar un nuevo tipo de solución o nuevo tipo de enfoque para resolver un problema
* __In constantly evolve__
  El navegador es un entorno que canvia continuamente, no cambia por el sencillo capricho que quiere agregar nuevas cosas, sino por las necesidades que se están utilizando hoy en día.
* __Have a cli for start a quick project__
  Si algo en común tienen estos tres, es que... no es nada sencillo poder crear un proyecto desde cero. De hecho Angular en sus inicios requerian diez archivos para configurarse. React necesitaba unirse a otras herramientas para tener un entorno más profecional, y Vuejs de la misma manera.
  Ahora tenemos herramientas de línea de comando que generan un proyecto completamente desde cero, pero un proyecto con una configuración profecional.
* __Based on components and modularity__
  Los tres utilizan una manera de dividir una aplicación grande en pequeñas partes.
  Los componentes no es mas que poder encapsular ciertas partes de nuestra aplicación.
* __Transpiling Code: superset languages, DSL or news versions of the language__
  Convierten el código por la sencilla razon,  que no todos los navegadores soportan las mismas características.
  Transpilar código hace referencia, convertir código de álto nivel a código de álto nivel.
* __They use the Most recent versions of javascript__
  Usan las funcionalidades nuevas de javascript.
* __But it can work very well with Nodejs__
  Es necesario conocer los conocimientos básicos para poder manejar varios paquetes asociados con la aplicación, como transpiladores como sass, o como babel, empaquetadores como webpack, los linters como slim o jslint. Para poder configurar un proyecto y luego customizarlo cuando la aplicación sea mucho mas grande es muy importante.
* __Use modern javascript tools like, module bundlers transpiler, linters, etc__
* __Concepts you can Apply with any framework/library__
  Si utiliamos un framework/library y entendemos los conceptos básicos, esto nos ayudará a poder adaptarnos ah otras tecnologías.
  * __TDD__ (testing)
  * __GraphQL__
    Mucho más que un concepto es una tecnología, que fue creada por los desarrolladores de facebook. Es una tecnología que permite traer datos desde el back-end al front-end e includo pedir solo los datos que se necesite.
  * __PWA, and HTML5 APIs__ (Progressive Web Apps)
    Que nuestra app web pueda ejecutarse como una aplicación movil.
  * __Functional Programming__
    Podemos utilizar paradigmas relativamente nuevos como: la programación funcional, que hace referencia en poder escribir una app basada en funciones y tambien manteniendo el estado de nuestra aplicación.
  * __Managing the state with a library__
    Tambien es importante hablar de sus complementos, que nos ayudan a mantener el estado de un aplicación.
  * __You can build your custom configuration__
    Más personalizados, si queremos modificarlo necesitaremos saber como funciona la tecnología.
  * __Important companies are using them__
    Son usadas por empresas muy importante como Google que mantiene a Angular o Facebook que mantiene a Reactjs, mientras que empresas muy importantes como Alibaba usa Vuejs tambien en producción.

Si sale algun tipo de tecnología o estandar en la Web también tratan de actualizarse para ponerse al día.

### Angular
* Is a full Featured Framework
Angular es un framework completo a diferencia de ReactJS y VueJS, por ejemplo si dedicimos aprender angular o VueJS, cuando creemos un proyecto utilizándolos, luego tendremos que decidir que proyecto o librería utilizar para poder crecer, es decir, que biblioteca de enrutamiento necesitamos, que biblioteca para manejar los formularios necesitamos, etc.

* Is the upgrade for the most popular js ___framework___ developed by Google.
Este framework es conocido como AngularJS, por el año 2007-2008 aproximandamente AngularJS empezaba a ser bastante popupal para crear aplicaciones detro de un navegador. Utilizaba JS EC5

* Versions: angularjs, 2 ,4 , 5, 6. Now is just Angular.
Al intentar mejorar el framework, buscó un lenguaje, que le diera funcionalidades añadidas a JS, este leguaje es TS, Es desarrollado por Microsoft y le permite a los desarrolladores de AngularJS mejorarlo a tal punto que es practicamente distinto. Entonces Angular 2 y AngularJS son completamente distintos, luego empieza a salir Angular 2, 4, 5, 6, no sale la tres por problemas del nombre o por conflictos, desde estas versiones solo se llama ___Angular___

* All alone to build an entire SPA: animations, routing, http, D/I, Testing.
Angular es un framework con el objetivo de crear Single Page Aplicattions, Antes se utilizaba lenguajes del Back-End.

* Use Typescript, a superset  of Javascript developed by Microsoft.
Utiliza un lenguaje para crear aplicaciones un poco mas simple, un poco más fácil. TS es un lenguaje superconjunto de Microsoft, permite añadir funcionalidades a JS y poder crear aplicaciones grandes usando solo JS con funcionalidades añadidas obviamente.

* A easy transition from ___enterprise___ framework as spring, .NET.
Si conoces Java o C#, ahora conocer Angular con TS será muy sencillo adaptarse.

* You can build mobile hybrid apps with Ionic.
No solo puedes desarrollar aplicaciones con Angular, también se puede desarrollar aplicaciones híbridas, aplicaciones móviles híbridas para ser exacto. Cuando hablamos de aplicaciones con datos intencivos las app híbridas puede no ser la mejor alternativa.

* And Mobile Apps with NativeScript.
Java, Objetive-C, Swift. Aplicaciones nativas.

2. Angular 2 Sale septiembre del 2016


Tips. Angular Ayuda al desarrollador a manejar el estado.
http://blog.desafiolatam.com/vale-la-pena-aprender-programar-con-angularjs/
https://rawgit.com/krausest/js-framework-benchmark/master/webdriver-ts-results/table.html


### ReactJS
* It Is a lightway and efficient library to built UI.
* React is the most popular web development ___library___ created by Facebook and Instagram.
* You decide what you wire to your SPA: your Apis, state management(fluw, redux), routing, http libraries, etc.
* The core es small, easy to learn, is more matural for javacript debelopers.
* Usa a JSX (DSL) transpiler.
* Just focus on wiew, UI.
* You can create native apps with React native
* And more Rreact Windows, React IoT, React AR/VR

### VueJS
* Progressive Framework.
* Flexible and productive.
* Very fast and good preformance.
* Simple and easy to learn.
* Support two way data binding.
* Virtual DOM.
* Templating, use native HTML, and javascript, css
* For this reason is the most easy to integrate in existing projects.
* It is very popular for open source proyect, instead of depending on Google or Facebbok.
* Alibaba is working on Weex, to build native apps with Vuejs.
