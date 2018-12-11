[Volver al curso completo](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/teoria.md)

## Creación del controlador de domínio

### Módulo 5 (Sexta Práctica)

__Creamos un nuevo Rol__

Desde el panel lateral izquierdo precionamos en `Panel -> Agregar roles y características -> Siguiente -> Siguiente` dejamos seleccionado `Seleccionar un servidor del grupo de servidores` luego `Siguiente` buscamos y seleccionamos `Sevicios de dominio de Active Directory` nos aparece un dialogo precionamos en `Agregar Características -> Siguiente` en características lo dejamos como está `Siguiente -> Siguiente` nos aparece un resumen de todo lo que se vá a instalar, precionamos `Instalar`

![Imagen prac06_img01](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac06_img01.png)

Precionamos en `Promover este servidor a controlador de dominio`

![Imagen prac06_img02](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac06_img02.png)

Nos aparece una ventana, en esta parte crearemos un nuevo forest ó bosque, para esto seleccionamos la tercera opción `Crear un nuevo Forest` colocamos el nombre de `iofullstack.local` luego precionamos en `Siguiente` escribimos la contraseña `Clave001` lo mismo en repetir contraseña `Siguiente -> Siguiente` verificará el nombre NetBIOS lo dejamos con el nombre `IOFULLSTACK -> Siguiente` luego especificamos donde almacenará la base de datos y los logs, lo dejsmos como esta y precionamos en `Siguiente`, si queremos ver como se instala mediante `script`, pare eso se puede precionar a `Ver script`, luego precionan en `Siguiente -> Instalar`, cuando finaliza debemos reiniciar el computador.

![Imagen prac06_img03](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac06_img03.png)

Una vez terminado en el `Administrador del servidor` nos muestra el rol ya instalado en `GRUPOS DE SERVIDORES Y ROLES`, con el nombre de `AD DS`.

![Imagen prac06_img04](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac06_img04.png)

Para configurar `DNS` vamos a `Herramientas -> DNS` desplegamos `DC-HOJA`, si desplegamos `Zonas de búsqueda directa` tenemos ya la zona creada `iofullstack.local`.

![Imagen prac06_img05](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac06_img05.png)

Pero en la parte de `Zonas de búsqueda inversa` esta vacío, damos click derecho luego en `Zona nueva... -> Siguiente -> Siguiente -> Siguiente -> Siguiente` en `Id. de red:` escribimos `192.168.1`.

![Imagen prac06_img06](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac06_img06.png)

Luego precionamos en `Siguiente -> Siguiente -> Finalizar`.

![Imagen prac06_img07](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac06_img07.png)

Ahora modificaremos una dirección de red, para eso precionamos la combinación de teclas `Windows + R` escribimos `ncpa.cpl` luego `Aceptar`.

![Imagen prac06_img08](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac06_img08.png)

Luego hacemos click derecho en `Ethernet0 -> Propiedades -> Protocolo de Internet versión 4 (TCP/IPv4) -> Propiedades` observamos que nos cambió la dirección del `Servidor DNS preferido`

![Imagen prac06_img09](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac06_img09.png)

![Imagen prac06_img10](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac06_img10.png)

![Imagen prac06_img11](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac06_img11.png)

Lo cambiamos a `192.168.1.10` luego aceptamos y cerramos todo.

![Imagen prac06_img12](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac06_img12.png)

Para comprobar abrimos el `Power Shell` escribimos el comando `nslookup`, nos dice que es servidor es desconocido, luego salimos `exit` y escribimos `ipconfig /registerdns` ahora volvemos a escribir `nslookup` y vemos como ahora sí reconoce el nombre de nuestro servidor, podemos preguntar quien es `192.168.1.10` ahora por el nombre `dc-hoja` ó `dc-hoja.iofullstack.local` luego salimos.

```shell
> nslookup
Servidor predeterminado: Unknown
Address: 192.168.1.10
> exit
> ipconfig /registerdns
> nslookup
Servidor predeterminado: dc-hoja.iofullstack.local
Address: 192.168.1.10
> 192.168.1.10
Servidor: dc-hoja.iofullstack.local
Address: 192.168.1.10

Nombre: dc-hoja.iofullstack.local
Address: 192.168.1.10
> dc-hoja
Servidor: dc-hoja.iofullstack.local
Address: 192.168.1.10

Nombre: dc-hoja.iofullstack.local
Address: 192.168.1.10
> exit
> exit
```

[Volver al curso completo](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/teoria.md)
