[Volver al curso completo](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/teoria.md)

## Instalación del Sistema Operativo Windows Server 2012 Físicamente

### Módulo 3 (Primera Práctica)

__Es necesario tener lo siguiente para todo el curso:__

![Imagen prac01_img01](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac01_img01.png)

__Pasos a Seguir__

Iniciaremos con unas series de fotografías para la instalación paso por paso del sistema operativo.

![Imagen prac01_img02](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac01_img02.png)

El servidor que instalaremos es:

![Imagen prac01_img03](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac01_img03.png)

![Imagen prac01_img04](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac01_img04.png)

![Imagen prac01_img05](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac01_img05.png)

Lo primero es insertar el DVD:

![Imagen prac01_img06](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac01_img06.png)

Lo siguiente es cambiar el boot desde Bios para que inicie desde el lector DVD, al iniciar el arranque nos aparecerá lo siguiente:

![Imagen prac01_img07](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac01_img07.png)

Si no está booteando desde ahí, aparecerá lo siguiente.

![Imagen prac01_img08](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac01_img08.png)

Luego de presionar una tecla, empezará a cargar los archivos.

![Imagen prac01_img09](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac01_img09.png)

Una vez que termine de leer y cargar los archivos, aparecerá el logo típico de Windows, una vez que cargue nos aparece la primera ventana del asistente de instalación.

Tiene la obción de elegir el lenguaje del sistema operativo, la hora, y la entrada del teclado. Una vez seleccionados las obciones deceadas, precionamos click en el botón de siguiente "Next".

![Imagen prac01_img10](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac01_img10.png)

Luego nos aparece esta ventana, y presionamos en "Install now".

![Imagen prac01_img11](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac01_img11.png)

>No es el caso, pero si falla el sistema operativo más adelante podemos precionar en la obción "Repair your computer".

Después de hacer click en "Install now", automáticamente nos dice que la configuración está iniciando y se pondrá a leer.

![Imagen prac01_img12](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac01_img12.png)

Luego nos aparecerá esta ventana, donde nos aparece distintas formas de instalar el sistema operativo

![Imagen prac01_img13](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac01_img13.png)

Podemos instalar tanto a nivel de server core, ó como a nivel de GUI. Server core es la parte que nos muesta las opciones de PowerShell y el GUI (Graphical User Interface) nos mostrará la parte gráfica del sistema operativo.

![Imagen prac01_img14](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac01_img14.png)

Debajo de estas obciones, tendremos dos partes: una es la colección de la información, y el otro el proceso de instalación del sistema operativo.

![Imagen prac01_img15](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac01_img15.png)

Cuando seleccionamos la obción deseada y le damos click en siguiente "Next"

![Imagen prac01_img16](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac01_img16.png)

Nos aparece el contrato de licencia entre Microsoft y nosotros, una vez leído los terminos hacemos click en aceptar el contrato "I accept the license terms", para poder continuar con la instalación

![Imagen prac01_img17](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac01_img17.png)

Una vez aceptada la licencia nos vamos a la otra esquina y precionamos en siguiente "Next"

![Imagen prac01_img18](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac01_img18.png)

Debemos tenerlo de esta manera

![Imagen prac01_img19](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac01_img19.png)

Luego nos aparece esta otra ventana, la cual nos pregunta que tipo de instalación deceamos instalar. Hay dos formas de instalacion, una es "Upgrade" y la otra "Custom", la parte de "Upgrade" es si tenemos un sistema operativo viejo como Windows Server 2008 y si queremos actualizar al de 2012, esta obción es la adecuada, pero en caso de querer una instalación perzonalidada "Custom", ya que estamos instalando el sistema operativo por primera vez es ese disco duro.

![Imagen prac01_img20](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac01_img20.png)

Una vez seleccionado "Custom", nos aparece esta ventana que es la parte más importante de la instalación, ya que por medio de esta ventana podemos manejar o administrar todas las particiones y formateo necesario para que el sistema operativo pueda funcionar. Este disco duro está particionado en dos, una partición es de 146.5Gb y el otro es de 86.3Gb 

![Imagen prac01_img21](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac01_img21.png)

En las opciones debajo como "Refresh" y "Load driver", "Refresh" es cuando no se encuentra ningún disco duro y al precionar en este actualiza y busca el disco duro para ver si lo encuentra, "Load driver" es si deceamos instalar el sistema operativo, que no sea el que nos está mostrando, así lo cargamos de manera manual.

![Imagen prac01_img22](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac01_img22.png)

Del otro lado tenemos obciones avanzadas "Drive options (advanced)".

![Imagen prac01_img23](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac01_img23.png)

Al hacer click en "Drive options (advanced)", se activarán estas obciones "Delete", "Format", "Extend"

![Imagen prac01_img24](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac01_img24.png)

Seleccionamos una partición, y luego procedemos a eliminarla

![Imagen prac01_img25](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac01_img25.png)

![Imagen prac01_img26](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac01_img26.png)

Automáticamente nos aparecerá una diálogo donde dice que la partición puede contener archivos de información importante y que si precionamos "ok", pues perderemos todo en esa partición.

Procedemos hacer lo mismo con la otra partición, esto si en caso a ustedes les aparece algo similar.

![Imagen prac01_img27](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac01_img27.png)

Una vez eliminadas todas las particiones que teníamos antes, vemos que tenemos todo el espacio disponible en el disco duro.

![Imagen prac01_img28](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac01_img28.png)

Después de precionar en la obción nuevo "New", nos muestra el tamaño (size) completo del disco duro.

Podemos particionar el disco duro pero dejaremos que solo haya una partición para el sistema operativo.

![Imagen prac01_img29](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac01_img29.png)

Nos aparece un dialogo donde dice, que para asegurar las característecas de Windows Firewall o el cortafuegos de Windows, él necesita crear una particion adicional para los archivos del sistema, siempre le daremos en "ok"

![Imagen prac01_img30](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac01_img30.png)

Una vez terminado, nos queda de esta menera, seleccionamos en que partición se procederá hacer la instalación (Partition 2), precionamos en siguiente "Next"

![Imagen prac01_img31](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac01_img31.png)

Ya pasamos al proceso final de Windows Server 2012, donde solo nos queda esperar a que finalize la instalación.

![Imagen prac01_img32](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac01_img32.png)

![Imagen prac01_img33](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac01_img33.png)

Una vez terminada esta parte, el computador se reinicia.

![Imagen prac01_img34](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac01_img34.png)

>Nos muestra otra vez esta parte de precionar una tecla para iniciar la instalación, es importante obviar esta parte y NO precionar una tecla y dejar a que termine esta parte.

Luego de no precionar ninguna tecla, nos aparece el sistema operativo ya queriendo iniciar.

![Imagen prac01_img35](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac01_img35.png)

Nos dice que esta obteniendo la configuración de los dispositivos conectados a él.

![Imagen prac01_img36](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac01_img36.png)

Una vez que llegue a 100%, se pondrá en marcha en todas las configuraciones que respecta.

![Imagen prac01_img37](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac01_img37.png)

En esta parte debemos proporcionar al usuario "Administrator" una contraseña segura, se recomienda utilizar una contraseña strong password, la cual es una convinación de tres de estos cuatro tipos, por ejemplo están las mayúsculas, minúsculas, caracteres especiales, y los números.

![Imagen prac01_img38](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac01_img38.png)

Una vez ingresada la contraseña.

![Imagen prac01_img39](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac01_img39.png)

Podemos observar la contraseña, en la parte derecha de la caja de texto, nos aparece un ojo, que al precionar, cambia esos puntos negros a texto y así observamos si lo tenemos bien escrito.

![Imagen prac01_img40](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac01_img40.png)

La clave ó contraseña contiene tres de los cuatro tipos de una contraseña strong password que especificamos anteriormente con un mínimo de ocho caracteres.

![Imagen prac01_img41](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac01_img41.png)

Luego tenemos esta ventana que nos dá la bienvenida al sistema, donde nos dice que precionemos esta combinación de teclas: Ctrl+Alt+Delete ó Ctrl+Alt+Supr para iniciar.

![Imagen prac01_img42](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac01_img42.png)

Cuando precionamos esa combinación de teclas, pues entonces nos aparecerá el administrador y la clave para introducir.

![Imagen prac01_img43](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac01_img43.png)

Una vez introduzida la contraseña, deberemos esperar a que cargue el "Server Manager"

![Imagen prac01_img44](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac01_img44.png)

¡Listo! con esto concluimos la instalación de Windows Server 2012.

![Imagen prac01_img45](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac01_img45.png)

[Volver al curso completo](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/teoria.md)
