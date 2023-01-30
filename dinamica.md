# Dinámica de Sistemas

## Introducción

### Generalidades y Definiciones

**Sistema**, de manera formal, como un objeto dotado de alguna complejidad, formado por partes coordinadas, de modo que el conjunto posea una cierta unidad, que es precisamente el sistema. En este sentido un sistema, lo entendemos como una unidad cuyos elementos interaccionan juntos, ya que continuamente se afectan unos a otros, de modo que operan hacia una meta común.

![Imagen01](https://github.com/garyDav/Blogs/blob/master/img/dinamica/img1.png)

Con respecto a la imagen, enunciaremos ese conjunto de partes y establecer cómo se influyen esas partes entre sí, cuyos nodos son esas partes y cuyas aristas representan las influencias que se producen entre ellas.

**Dinámica**, lo emplearemos por oposición a *estática*, y con él expresamos el carácter cambiante de aquello que adjetivamos con ese término.

![Imagen02](https://github.com/garyDav/Blogs/blob/master/img/dinamica/img2.png)

A algo que cambia se le suele asociar la anteriór imagen, que muestra la trayectoria de una magnitud.

Al hablar de **Dinámica de Sistemas** nos referimos a que las distintas variables que podemos asociar a sus partes sufren cambios a lo largo del tiempo, como consecuencia de las iteracciones que se producen entre ellas.

**Experimento**, el proceso de extraer datos de un sistema mediante la activación de sus entradas.

**Modelo**, es un objeto que representa a otro, según *Marvin Minsky*: Para un observador *O* un objeto "M" es un modelo de un objeto *S* (un sistema) y un experimento (*E*), si *O* se puede servir de *M* para aplicar *E* y responder a cuestiones que le importan con relación a *S*.

Las propiedades de un buen modelo:

1. Debe de reflejar adecuadamente aquellas características del sistema que son de nuestro interés.

2. Debe ser lo suficientemente sencillo como para resultar manejable.

**Simulación**, según *Granino Korn*: Una simulación es un experimento realizado sobre un modelo. Nuestro interés está en el subconjunto de simulaciones que son codificables como programas de ordenador (simulaciones matemáticas). Donde, una simulación matemática es una descripción codificada de un experimento que hace referencia al modelo al cual se aplica.

### Metodología Sistémica

Pretende aportar instrumentos con los que estudiar aquellos problemas que resultan de las iteracciones que se producen en el seno de un sistema, y no de las partes del sistema consideradas aisladamente.

### Aplicaciones de la Dinámica de Sistemas

A mediados de los años 60, Forrester propone la aplicación de la técnica que había desarrollado originalmente para los estudios industriales, a sistemas urbanos. Surge así la dinámica urbana, en las que las variables consideradas son los habitantes en un área urbana, las viviendas, las empresas, etc. Una aplicación análoga a la dinámica urbana lo constituye la dinámica regional.

## Estructura y comportamiento elemental en dinámica de sistemas

### Un Lenguaje Elemental Para La Descripción De Sistemas: Diagramas de Influencias

Si $$A$$ y $B$ son dos partes de un sistema, el hecho de que $A$ influya sobre $B$ se representa mediante una flecha de la forma $A \to B$ e indica que $B$ es una función de $A$, es decir $B = f(A)$, aunque no conozcamos la forma matemática exacta de la función.

![Imagen03](https://github.com/garyDav/Blogs/blob/master/img/dinamica/img3.png)

El conjunto de las relaciones entre los elementos de un sistema recibe la denominación de *estructura* del sistema y se representa mediante el *diagrama de influencias* o *causal*. El diagrama de la figura constituye un ejemplo de la estructura de un sistema.

$A \overrightarrow{_+} B$ Las flechas representan las aristas de un grafo, se puede asociar un signo, del antecedente y del consecuente, si existe una relación de influencia positiva. Si $A$ incremeta lo mismo sucede con $B$; y, por el contrario, si $A$ disminuye, así mismo lo hará $B$. Por otra parte, si la influencia fuese negativa $A \overrightarrow{_-} B$; un incremento de $A$ seguiría una disminución de $B$; y, viceversa.

![Imagen04](https://github.com/garyDav/Blogs/blob/master/img/dinamica/img4.png)

### Diagramas de Forrester

Forrester clasifica a las variables dde un diagrama de influencias en tres grupos:

* Variables de estado (o de nivel)
* Variables de flujo
* Variables auxiliares

Las variables de nivel son las variables más importantes y representan esas magnitudes cuya evoluciónes especialmente significativa. Asociada a cada variable de nivel se encuentra una o varias variables de flujo, que determinan su variación a lo largo del tiempo. Por último, las varibles auxiliares son el resto de las varibles que aprecen en el diagrama, y representan pasos intermedios para la determinación de las varibles de flujo a partir de las variables de nivel.

Si somos capaces de clasificar éstas variables en el diagrama de influencias estamos en disposición de obtener, lo que se conoce como _diagrama de Forrester_, que es uno de los elementos básicos de la dinámica de sistemas.

A éstas variables se les asocian unos iconos (gráficos) como se indican en la figura 2.3, en la que una variable de estado se asocia un rectángulo, a una de flujo un icono que recuerda una válvula y a una variable auxiliar mediante un círculo.

![Imagen05](https://github.com/garyDav/Blogs/blob/master/img/dinamica/img5.png)

En la Tabla 2.1, se mestran todos los símbolos utilizados originalmente en los diagramas de Forrester.

![Imagen06](https://github.com/garyDav/Blogs/blob/master/img/dinamica/img6.png)

En la figura 2.4 se tiene el diagrama de Forrester, donde mediante los símbolos "K" y "Nivel Deseado" las constantes que aparecen en el modelo. donde "K" representa la proporción de agua que se deja pasar en función de la "Discrepancia" existente.

![Imagen07](https://github.com/garyDav/Blogs/blob/master/img/dinamica/img7.png)

Por último, en la figura 2.4, aparece en el extremo izquierdo, una fuente que representa una fuente, o un sumidero, que no es relevante para la descripción del sistema. Se podría prescindir de él pero se incluye para dar mayor coherencia al diagrama.

### Modelo Matemático


