# APLICACIONES EN TIEMPO REAL
---

![Imagen 1](https://github.com/garyDav/Blogs/blob/master/img/img1.png)

#### Web sockets

Es un canal de comunicación implementado por el estandar [HTML5](https://www.w3.org/html/logo/), nos permite una conectividad más eficiente por medio de eventos entre el cliente y el servidor.

Cada lenguaje en el Back-End como: __PHP__, __Python__, __Java__, __Rubi__, __.NET__, tienen sus propias librerías para trabajar con ___Sockets___

Los ___Sockets___ es un concepto que viene de los <abbr title="Sistemas Operativos">S.O.</abbr> habre un canal de comunicación entre el servidor y la aplicación que lo este solicitando. __Socket__ es un concepto antiguo que podemos hablar de ellos desde los primeros lenguajes de programación en la arquitectura basado en cliente y servidor, es decir una computadora (cliente) solicitaba cierta información a un computador (servidor) dentro de una red.

La diferencia de un __Socket__ de la época antes de la web, con __[Web Socket](http://www.websocket.org/)__ es, a través del navegador web poder establecer una comunicación __Bidireccional (Full-duplex)__.

Nos permite tener __una sola comunicación permanente__, es decir no tenemos que abrir y cerrar conexiones, para poder trabajar con los __[Web Socket](http://www.websocket.org/)__.

Actualmente está [soportada](https://caniuse.com/#search=web%20sockets) por todos los navegadores web, nos permite mandar chorros de información (Stream de mensajes) con un contenido en tiempo real.

>A grandes rasgos, el cliente puede enviar y recibir datos en tiempo real. Son orientados a "eventos", practicamente los eventos son nativos de javascript del lado del cliente como del lado del servidor, en este caso nuestros eventos serán los mensajes, podremos crear y darles nombres a nuestros propios eventos, esto nos permitirá siempre estar conectados y tener una baja latencia.

#### Web sockets y NodeJS

NodeJS al ser un entorno de desarrollo muy ágil, nos permite manejar múchas conexiones de manera simultánea, de hecho las aplicaciones en tiempo real, fue para lo que originalmente se empezó a trabajar con NodeJS.

Los Web sockets tienen una buena integración con __JSON__, practicamente su funcionamiento depende de __Eventos__.

#### ¿Para qué sirven?

Fundamentalmente, para:

* Actividades colaborativas: Como __Google Drive__, editar archivos con diferentes personas.

* Juegos multijugador: Manejando tecnologías __HTML5__, como canvas.

* Enviar datos: Como las aplicaciones tipo mensajería, __Houngouts__, __Facebook messenger__, __Whatsapp__.

* Cargar recursos: Como __Dropbox__, __Google Drive__. __GitHub__.

* En resumen: tiempo real en vez de "a petición"

#### Socket\.io

* Una librería para manipular websockets.

* Muy popular.

* Fallback para navegadores obsoletos.

* Muy fácil de usar.

* Servidor / Cliente.

* [API DOC](https://socket.io/docs/)

Los sockets emiten eventos.

* Un evento = un "mensaje".

* Se puede pasar parámetros.

* `socket.on(mensaje, callback)`

* `socket.emit(mensaje, [param1, param2, ...])`

Eventos reservados en el. 

* Servidor:
  * `io.sockets.on('connection', cb)`
  * `socket.on('message', cb)`
  * `socket.on('disconnect', cb)`

* Cliente:
  * `socket.on('connect', cb)`
  * `socket.on('disconnect', cb)`
  * `socket.on('error', cb)`
  * `socket.on('message', cb)`
