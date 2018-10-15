# Introducción a Terminal y Línea de Comandos

#### Autor @_garyDav referencia [Platzi](https://platzi.com/cursos/terminal/)

>Los siguientes comandos son para _Unix_.

---

### Qué es la terminal y para qué sirve

La linea de comandos es la herramienta mas potente que tenemos en la computadora.

Nos permite hacer casi cualquier cosa desde nuestro computador, desde editar texto, compilar código, ejecutar código, configuraciones del computador, etc... lo podemos hacer si utilizamos bien la terminal.

__¿Cuántos binarios ejecutables tengo en mi Sistema Operativo?__

>No se preocupen si no entienden los comandos se explicará a lo largo de este curso

```bash
~ ls /usr/bin
```

Cáda uno de estos resultados son comandos que podemos ejecutar en nuestro S.O. (Sistema Operativo).

__Ctrl+l__ o el comando `clear` Limpia nuestra terminal.

```bash
~ ls /usr/bin | wc -l
```

Muestra cuantos binarios tenemos.

### Árbol de directorios y navegación

__¿Qué es lo que se hace en la terminal?__

Simple y sencillamente ejecutar comandos.

La experiencia que nos dará a lo largo del tiempo es aprender varios comandos y saber por donde vá algunos que no conozcamos.

El comando `ls` es _listar_, por si sola es muy confuso cuando tenemos demasiadas carpetas y archivos.

Por tal motivo todos los comandos tienen la opción de mandar diferentes _banderas_, y valores a las _banderas_.

Al comando `ls` añadiremos la bandera `-l`, nos mostrará un monton de información adicional en vertical.

```bash
~ ls -l
-rwxrwxrwx@  1 gary  staff     33015 Jul  5 12:07 bitmap.png
drwx------+ 30 gary  staff       960 Jul 23 19:11 Desktop
drwx------+ 33 gary  staff      1056 Jul 20 11:59 Documents
drwx------+ 59 gary  staff      1888 Aug 16 11:50 Downloads
lrwxr-xr-x   1 gary  staff        26 Oct 11  2017 Webs -> /Applications/XAMPP/htdocs
^    ^       ^   ^     ^          ^  ^__________^    ^
|    |       |   |     |          |       |          |
1    2       3   4     5          6       7          8
```

__Explicación__

1. La `d` nos dice que es un _directorio_, el `-` sería un _archivo_, y `l` es un _directorio lógico_, como se vé el directorio `Webs` apunta a `/Applications/XAMPP/htdocs`.
2. Esta parte son los permisos, que se representa en `rwx` (Read Write Execution) se repite tres veces, si no tiene ese permiso se lo remplaza con `-`. El primer `rwx` son los permisos del usuario que los creó. El segundo `rwx` permisos del grupo, y el tercer `rwx` permisos para otros usuarios.
3. Número de enlaces asociados al archivo, ó número de Identidad de Usuario.
4. UID (User Identity), nombre del usuario al que pertenece el directorio ó archivo.
5. GID (Group Identity), nombre del grupo propietario al que pertenece el directorio ó archivo.
6. Tamaño en bytes ó número de Identidad de Grupo.
7. Fecha de la ultima modificación.
8. Nombre del directorio o archivo.

__j__
