# Web Semántica

#### La web actual

La Web actual es un conjunto de __documentos__, en general __páginas Web__ escritas en HTML:

![Imagen01](https://github.com/garyDav/Blogs/blob/master/img/web_semantica/Imagen01.png)

Esas páginas Web HTML están formadas por __contenido__ y por __enlaces:__

![Imagen02](https://github.com/garyDav/Blogs/blob/master/img/web_semantica/Imagen02.png)

#### Desafíos de la Web actual

* __Heterogénea:__ Múltiples organizaciones generan datos, de forma independiente.

![Imagen03](https://github.com/garyDav/Blogs/blob/master/img/web_semantica/Imagen03.png)

* __Masiva:__ La cantidad de información existente es enorme.

![Imagen04](https://github.com/garyDav/Blogs/blob/master/img/web_semantica/Imagen04.png)

![Imagen05](https://github.com/garyDav/Blogs/blob/master/img/web_semantica/Imagen05.png)

* __Cambia muy rápido:__ Cada día son publicados y borrados enormes volúmenes de información.

![Imagen06](https://github.com/garyDav/Blogs/blob/master/img/web_semantica/Imagen06.png)

* __Hecha para humanos:__ En general, sólo una persona puede interpretar la información de una página Web.

#### La Web está hecha para humanos

Por ejemplo, Facebook lo consumen principalmente las personas, Wikipedia lo entienden las personas.

Que pasa si yo quiero enlazar o combinar datos de la Wikipedia y de Facebook, eso actualmente con el diseño de la Web actual no es posible. ¿Entonces cómo podría una aplicación construir datos de dos Web distintas? ¿Leyendo texto, contenido? ¿Cómo sabría que texto leer? ¿Cómo sabría que contenido leer dentro de una página Web? ¿Mirando el código HTML? ¿Es posible identificar el nombre de una persona en el código HTML?.

#### Síntesis

* La Web actual está compuesta por documentos, que a su vez tienen contenidos y enlaces a otros documentos.

* Cuatros desafíos de la Web actual son su heterogeneidad, masividad, velocidad de cambio y estructura diseñada para humanos.

## Capitulo 1: Nociones básicas y el modelo de datos RDF

#### 1. Datos en la Web

Hay datos de todo tipo en la Web: genéricos, médicos, noticias, gubernamentales...

![Imagen07](https://github.com/garyDav/Blogs/blob/master/img/web_semantica/Imagen07.png)

Pero la cantidad de datos es tan grande que no podemos gestionarlos todos...

![Imagen08](https://github.com/garyDav/Blogs/blob/master/img/web_semantica/Imagen08.png)

#### 1.1 Datos genéricos: Wikipedia

![Imagen09](https://github.com/garyDav/Blogs/blob/master/img/web_semantica/Imagen09.png)

#### 1.2 Datos médicos: Biblioteca Nacional de Medicina de Estados Unidos

![Imagen10](https://github.com/garyDav/Blogs/blob/master/img/web_semantica/Imagen10.png)

#### 1.3 Noticias: The New York Times

![Imagen11](https://github.com/garyDav/Blogs/blob/master/img/web_semantica/Imagen11.png)

#### 1.4 Datos gubernamentales: London Datastore

![Imagen12](https://github.com/garyDav/Blogs/blob/master/img/web_semantica/Imagen12.png)

#### 2. ¿Cómo podemos aprovechar estos datos?

Los computadores tienen la capacidad para poder analizar estos datos.

Pero actualmente no son capaces de interpreatarlos correctamente...

(Las páginas que mostramos están pensadas para personas).

Hay que permitir que las aplicaciones computacionales entiendan los datos...

¿Cómo hacemos esto?

#### 3. Requisitos para una Web de datos efectiva

Primero, es necesario tener un lenguaje que permita especificar recursos en la Web y las relaciones entre ellas.

Segundo, necesitamos poder consultar estos datos mediante aplicaciones computacionales.

__Dos requisitos fundamentales:__

* Debemos tener un lenguaje para escribir consultas que sean procesables por un computador.

* Debemos ser capaces de sacar conclusiones de los datos de manera antomática.

#### 4. La Web semántica

![Imagen13](https://github.com/garyDav/Blogs/blob/master/img/web_semantica/Imagen13.png)

La Web Semántica es una extensión de la Web actual en la cual se da un significado bien definido a la información, permitiendo mejorar la colaboración entre personas y computadores en la Web (Tim Berners-Lee, 2001).

![Imagen13_01](https://github.com/garyDav/Blogs/blob/master/img/web_semantica/Imagen13_01.png)

#### 4.1 La Web semántica en la práctica

La Web semántica es un conjunto de recomendaciones desarrolladas por el Word Wide Web Consortium, cuyo objetivo es que los computadores sean capaces de enterder los datos en la Web.

Una recomendación es una descripción formal de una tecnología que debería ser utilizada por todos. Es decir, un lenguaje común para todos.

El Word Wide Web Consortium es el organismo regulador en la Web.

#### 4.2 Los estándares para la Web Semántica

![Imagen14](https://github.com/garyDav/Blogs/blob/master/img/web_semantica/Imagen14.png)

#### 5. Síntesis

* Hay datos de todo tipo en la Web que son de fácil acceso para las personas.

* La cantidad de datos es tan grande que las personas no los pueden gestionar en su totalidad.

* Es difícil para un computador acceder a estos datos ya que no los sabe interpretar.

* La Web Semántica es un conjunto de recomentadionces para facilitar el acceso de los computadores a los datos.

### La noción de URI

#### 1.1 ¿Cómo realizar la Web Semántica?

![Imagen15](https://github.com/garyDav/Blogs/blob/master/img/web_semantica/Imagen15.png)

#### 2.1 Características básicas de RDF

RDF es la propuesta del Word Wide Web Consortium (W3C) para representar información sobre recursos en la Web.

1. RDF está basado en el uso de grafos dirigidos y etiquetados

2. Una especificación RDF puede ser procesada por un computador

3. Las piezas básicas para construir una especificación RDF son las URIs y los literales

#### Figura: Ejemplo de un grafo

En esta figura podemos ver un grafo que tiene tantos nodos como arcos, estos están etiquetados. Los nodos son los círculos celestes, en el caso de los RDF representarán recursos de una página web, las flechas de negro son los arcos que también están etiquetados, que representan las relaciones que tenemos entre los recursos en la Web.

![Imagen16](https://github.com/garyDav/Blogs/blob/master/img/web_semantica/Imagen16.png)

#### 3. URI (Uniform Recource Identifier)

Un URI es un identificador de un recurso en el Web:

![Imagen17](https://github.com/garyDav/Blogs/blob/master/img/web_semantica/Imagen17.png)

#### 3.1 Ejemplo y componentes de un URI

Observa la siguiente figura:

![Imagen18](https://github.com/garyDav/Blogs/blob/master/img/web_semantica/Imagen18.png)

#### 3.2 URI: Más que una dirección Web

__URI:__

* Los URIs son una generalización de los URL.

* Un URI puede ser utilizado como identificador de cualquier recurso en la Web.

__URL:__

* Un URL (Uniform Resource Locator) es el identificador de una página Web

>Ejemplo: http://www.uc.cl

#### 3.3 Algunos ejemplos de URIs

Observa los siguientes ejemplos de URIs

![Imagen19](https://github.com/garyDav/Blogs/blob/master/img/web_semantica/Imagen19.png)

#### 4. Síntesis

* RDF es un lenguaje para especificar relaciones entre recursos en la Web.

* RDF puede ser procesado por un computador.

* Un URI es un identificador de un recurso en la Web.
