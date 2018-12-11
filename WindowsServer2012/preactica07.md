[Volver al curso completo](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/teoria.md)

## Unir el cliente Windows a nuestro controlador de domínio 

### Módulo 5 (Séptina Práctica)

__Verificando la versión del sistema operativo__

Precionamos la combinación de teclas `Windows + R` escribimos `winver` luego `Aceptar`, nos dice que el sistema operativo es `Windows 10 Pro`.

![Imagen prac07_img01](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac07_img01.png)

![Imagen prac07_img02](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac07_img02.png)

__Unir la máquina al dominio__

Primero el sistema operativo debe estar actualizado, debe tener un nombre, y debe tener una dirección IP, por último debemos comprobar que esa dirección IP debe estar comunicándose con el servidor, para luego unir esta máquina al domínio.

Precionamos la combinación de teclas `Windows + R` escribimos `ncpa.cpl -> Aceptar` en `Ethernet0` hacemos click derecho y vamos a `Propiedades` desactivamos el protocolo TCP/IPv6, luego vamos a `Protocolo de Internet versión 4 (TCP/IPv4) -> Propiedades` añadimos la siguiente dirección estática `192.168.1.11`, la máscara de sub red `255.255.255.0`, en `DNS` introducimos `192.168.1.10` Aceptamos y cerramos todo.

![Imagen prac07_img03](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac07_img03.png)

![Imagen prac07_img04](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac07_img04.png)

![Imagen prac07_img05](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac07_img05.png)

![Imagen prac07_img06](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac07_img06.png)

Para verificar la conexión de nuestro servidor con nuestro cliente.

Realizamos lo siguiente desde nuestro Windows cliente: `Windows + R -> cmd -> Aceptar`, podemos verificar nuestra IP con el comando `ipconfig`, ahora hacemos un ping a nuestro servidor, con el comando `ping 192.168.1.10`.

![Imagen prac07_img07](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac07_img07.png)

![Imagen prac07_img08](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac07_img08.png)

![Imagen prac07_img09](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac07_img09.png)

Observamos que tenemos respuesta desde nuestro servidor, procedemos a salir de la consola escribiento el comando `exit`.

Precionamos click derecho en `Este equipo -> Propiedades -> Configuración avanzada del sistema` nos dirigimos a la pestaña `Nombre de equipo -> Cambiar... -> Arena -> Miembro del Dominio -> iofullstack.local -> Aceptar` nos pregunta las credenciales del dominio `Nombre de usuario: Administrador, Contraseña: Clave001 -> Aceptar`.

![Imagen prac07_img10](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac07_img10.png)

![Imagen prac07_img11](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac07_img11.png)

![Imagen prac07_img12](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac07_img12.png)

![Imagen prac07_img13](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac07_img13.png)

![Imagen prac07_img14](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac07_img14.png)

Una ver terminado reiniciamos el equipo.

Para verificar que el equipo se unió al domínio, nos dirigimos a __Windows Server 2012__.

Vamos a `Herramientas -> Usuarios y equipos de Active Directory` desplegamos `iofullstack.local -> Computers` vemos que tenemos el equipo ARENA agregado a nuestro domínio.

![Imagen prac07_img15](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac07_img15.png)

Ahora nos dirigimos a `Herramientas -> DNS` desplegamos `Zonas de búsqueda directa -> iofullstack.local` observamos que tenemos el Host (A) `Arena` con la direción IP `192.168.1.11` con esto comprovamos que todo está bien.

![Imagen prac07_img16](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac07_img16.png)

[Volver al curso completo](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/teoria.md)
