### Introducción

Es una tecnica util para analizar el desempeño de sistemas de computadora.

El usuario define la estructura del sistema que quiere simular.

Sin embargo los modelos de simulación a menudo fallan, producen resultados poco útiles o resultados desconocidos. Debido al pado del modelo formal del sistema a un programa de software, o a un deficiente formalización del modelo, o a una deficiencia recopilación de datos y su ajuste estadístico

### Historia

La simulación como técnica científica es joven, y sus inicios remontan a 1940, con el advenimiento de las primeras computadoras.

La construcción de los modelos no es nueva.

En el Renacimiento la formulación de modelos especialmente matemáticos alcanza un alto grado de formalismo. Su ejecución estuvo basada en procesos manuales.

El uso moderno de la palabra simulación adquiere un nivel de ciencia, al implementar los modelos formales de simulación en algoritmos y código ejecutable en una computadora.

Los pioneros en la aplicación de esta técnica son los científicos *J. Von Neuman* y *S. Ulam* que trabajaban en el proyecto **Montecarlo**, durante la segunda Guerra Mundial.

La simulación está siendo aplicada a toda rama del saber humano donde esta presente un evento, proceso, subsistema o sistema que requiere ser estudiado.

### Definiciones

Podríamos decir que es una técnica que imita el funcionamiento de un sistema del mundo real cuando evoluciona en el tiempo. Esto se hace por lo general al crear un modelo de simulación. En síntesis, cada modelo o representación de una cosa es una forma de simulación.

*C. West Churchman* define formalmente el proceso de la simulación como "X simula a Y si y solo si: a) X y Y son sistemas formales, b) Y se considera como el sistema real, c) X se toma como una aproximación al sistema real, d) Las reglas de validez en X no están exentas de error."

*Martin Shubik* define el proceso de simulación como "La formulación de un modelo (simulador) que representa X en un sistema y puede sujetarse a manipulaciones imposibles de experimentar en el sistema real, La operación de un módulo puede estudiarse para luego inferir sobre el comportamiento del sistema o subsistema"

*Thomas H. Naylor* define la "Simulación como una técnica numérica para conducir experimentos en un computador. los cuales requieren de ciertos tipos de modelos lógicos y matemáticos que describen el comportamiento real de un negocio o sistema económico en periodos extensos de tiempo real".

*Robert E. Shannon* define "La simulación como el proceso de diseñar un modelo de un sistema real y realizar experimentos con este modelo con el propósito de entender el comportamiento del sistema o evaluar varias estrategias (dentro de los límites impuestos por un criterio o por un conjunto de criterios para la operación del sistema.)"

### Sistemas, Modelos, Experimentación y Optimización

## Generación de números aleatorios

### Propiedades de los números aleatorios

1. Normalizados en el rango [0,1]
2. Uniformemente distribuidos
3. Estadísticamente independientes
4. Reproducibles
5. De un periodo grande
6. De generación rápida
7. Poca utilización de memoria
8. Libres de degeneración

### Clasificación de los métodos de generación

1. Métodos Manuales
2. Tablas de Biblioteca
3. Provisión Externa
4. Generación Interna Física
5. Generación Interna Lógica
  Métodos matemáticos: $!= \bmod$
  Métodos congruenciales: $d=n \bmod m$

### Métodos que utilizan relaciones de recurrencia

Un valor de la secuencia es obtenido a partir de uno previo, y toda la secuencia a partir de la semilla ($x_0$)

#### Métodos de los cuadrados medios

Excluye los dígitos primeros y últimos, menos los centrales

$$n = dígitos\ significativos$$

$$x_0 = semilla\ entera\ (entero\ positivo)$$

$$x_1 = dígitos\ centrales\ de\ x^2_0$$

$$x_i = dígitos\ centrales\ de \ x^2_{i-1}\ para\ i = 1,2,3\dots$$

*Ejemplo:*
$n=3$
$x_0 = 0.528$
$x_1 = 0.27874 = 0.787$
$x_2 = 0.619369 = 0.193$
$x_3 = 0.037249 = 0.372$
$x_4 = 0.138124 = 0.381$
$x_5 = 0.146689 = 0.466$
$x_6 = 0.217151 = 0.171$
$x_7 = 0.029241 = 0.292$
$x_8 = 0.085264 = 0.852$
$x_9 = 0.725904 = 0.259$
$x_{10} = 0.067021 = 0.670$
$x_{11} = 0.448900 = 0.489$
$x_{12} = 0.239121 = 0.391$
$x_{13} = 0.15281 = 0.528$
$Periodo\ del\ generador\ p = 13$

#### Método del producto medio

Excluye los dígitos primeros y últimos, menos los centrales. Existen dos alternativas:

$$x_{n+1} = k * x_n$$

$$x_{n+1} = x_n * x_{n-1}$$

#### Método congruencial lineal mixto

Es el más utilizado, utiliza el operador $\bmod$.

$$x_{n+1} = (ax_n + c) \bmod m$$

$$r_n = \frac{x_n}{m}$$

*Donde:*
$x_0 = semilla\ del\ generador\ x_0 > 0$
$a: constante\ multiplicativa\ a > 0$
$c: constante\ aditiva\ c > 0$
$m: modulo\ m > a;\ m > x_0;\ m > c$

* $x_n$ es el valor base anterior
* $x_{n+1}$ es el nuevo valor uniforme entero
* $r_n$  es el número aleatorio normalizado

#### Método congruencial lineal multiplicativo

$$x_{n+1} = (ax_n) \bmod m$$

$$r_n = \frac{x_n}{m}$$

#### Método congruencial cuadrático

$$x_{n+1} = (ax^2_n + bx_n + c) \bmod m$$

>Resulta más lento que los anteriores, la aleatoriedad no depende de la complejidad de la expresión, ni de valores grandes de los parámetros, sino de la selección adecuada de ellos.

#### Método congruencial de fibonacci

$$x_{n+1} = (x_n + x_{n-1}) \bmod m$$

>Reproduce periodos más largos mayores a m, pero no padan algunas pruebas de aleatoriedad. Requiere de dos valores raíz base.

### Criterios de selección de la semilla

1. No use cero
2. Evite valores pares
3. No subdivida una secuencia
4. Use secuencias que no se solapan
5. Reuse semillas en replicaciones sucesivas
6. No use semillas aleatorias

### Algunos generadores de números aleatorios

1. __Generador SIMPL/I__
  $x_{n+1} = (7^5x_n) \bmod (2^{31}-1)$
2. __Generador SIMSCRIP__
  $x_{n+1} = (630360016\ x_n) \bmod (2^{31}-1)$
3. __Generador Pascal__
  $x_{n+1} = (16807\ x_n) \bmod (2^{31})$
4. __Generador Simula__
  $x_{n+1} = (5^{13}x_n) \bmod (2^{35})$
5. __Generador Unix__
  $x_{n+1} = (1103515245\ x_n + 12345) \bmod (2^{32})$

### Mitos sobre la generación de números aleatorios

### Pruebas de aleatoriedad

#### Función de distribución de los números aleatorios

#### Prueba de los promedios


