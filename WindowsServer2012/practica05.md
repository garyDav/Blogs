[Volver al curso completo](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/teoria.md)

## Puntos a tener en cuenta antes de crear el domínio

### Módulo 4 (Quinta Práctica)

__Cambiar nombre del Servidor__

En el `Administrador del servidor` nos dirigimos al panel lateral izquierdo, vamos a precionar `Local Server -> Nombre del equipo -> Cambiar` cambiamos el nombre de equipo a `DC-HOJA` luego precionamos en `Aceptar` nos pide reiniciar ahora, precionamos en `Aceptar -> Cerrar -> Reiniciar ahora`.

![Imagen prac05_img01](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac05_img01.png)

__Asignar IP estática__

Vamos a `Panel de control -> Redes e Internet -> Centro de redes y recursos compartidos -> Cambiar configuración del adaptador` click derecho en propiedades de `Ethernet0 -> Protocolo de Internet versión 4 (TCP/IPv4) -> Propiedades` es obcional desabilitar `Protocolo de Internet versión 6 (TCP/IPv6)`, despues de entrar en propiedades de IPv4, seleccionamos `Usar la siguiente dirección IP`, en `Dirección IP: ` colocamos `192.168.1.10`, la `Máscara de subred: ` colocamos `255.255.255.0`, la `Puerta de enlace predeterminada: ` por ahora lo dejaremos en blanco, en `Servidor DNS preferido: ` colocamos `192.168.1.10` como el servidor mismo será el servidor __DNS__ tiene que ser la misma que la IP, precionamos en `Aceptar` luego cerramos las otras ventanas.

![Imagen prac05_img02](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac05_img02.png)

>Una forma de ingresar a la configuración de red más rápido, precionamos `Win+R` tecla de windows + R, y escribimos `ncpa.cpl` y precionamos en `Aceptar`.

__Habilitar el Remote Desktop__

En el `Administrador del servidor` nos dirigimos al panel lateral izquierdo, vamos a precionar `Local Server -> Nombre del equipo (DC-HOJA)` cambiamos de pestaña a `Acceso remoto` y seleccionamos `Permitir las conexiones remotas a este equipo -> Aceptar -> Aplicar -> Aceptar`.

![Imagen prac05_img03](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac05_img03.png)

__Cambiar la zona horaria__

![Imagen prac05_img04](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac05_img04.png)

![Imagen prac05_img05](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac05_img05.png)

![Imagen prac05_img06](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/img/prac05_img06.png)

____

### Power Shell

__Cambiar nombre del Servidor__

```shell
> powershell
> hostname
WIN-4F0L49ABEF8
> rename-computer PSDC-HOJA
WARNING: The changes will take effect after you restart the computer WIN-4F0L49ABEF8.
> shutdown /s
...
> powershell
> hostname
PSDC-HOJA
```

__Definir una IP Estática__

Un punto muy importante es decir a que InterfaceAlias quiero aplicar el cambio

```shell
> Get-netipaddress
IPAddress       : fe80::5efe:192.168.1.10%13
InterfaceIndex  : 13
InterfaceAlias  : isatap.{2426A078-DAA7-4DF7-911E-2DB9F068ABBA}
AddressFamily   : IPv6
Type            : Unicast
...
> New-netipaddress
cmdlet New-NetIPAddress at command pipe line position 1
Supply values for the following parameters:
IPAddress: 192.168.1.1
InterfaceAlias: ethernet
> cls
```

[Volver al curso completo](https://github.com/garyDav/Blogs/blob/master/WindowsServer2012/teoria.md)
