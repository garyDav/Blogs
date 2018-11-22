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

### Literal y triples

#### 1. Una segunda pieza básica de RDF: los literales

Un literal representa un __valor__ concreto en una especificación RDF, ejemplo: Messi nació en la fecha __"1987-06-24"__, la fecha es un literal.

Un literal es simplemente una cadena de caracteres:

* __"1987-06-24"__

* __"Lionel Messi"__

* __"157.38"__

* __"18:25:00"__

Un literal puede tener un tipo asociado. En los siguientes literales, los tipos se destacan en negrita:

* Fecha: "1987-06-24"__^^xsd:date__

* Número real: "157.38"__^^xsd:float__

* Hora: "18:25:00"__^^xsd:time__

2. Contruyendo una especificación RDF

En una especificación RDF, una __relación__ entre dos __recursos__ es dada a través de un __triple__:

>Un triple tambien puede ser utilizado para dar el __valor__ de un atributo asociado a un __recurso__.

#### 2.1 Un triple en RDF

![Imagen20](https://github.com/garyDav/Blogs/blob/master/img/web_semantica/Imagen20.png)

#### 2.2 Abreviación de URIs

Usualmente, las URIs son abreviados utilizando prefijos.

Si se declara:

__`@prefix dbpedia: http://dbpedia.org/resource/`__

Entonces:

__`dbpedia:Lionel_Messi`__

Es la abreciación de:

__`http://dbpedia.org/resource/Lionel_Messi`__

#### 2.3 Ejemplos de triples RDF

Usamos los siguientes prefijos:

```rdf
@prefix dbpprop: http://dbpedia.org/property/
@prefix dbpedia: http://dbpedia.org/resource/
@prefix example: http://dbpedia.org/
```

#### 2.3.1 Un primer ejemplo de triple

El siguiente triple indica que Messi nació en Argentina:

![Imagen21](https://github.com/garyDav/Blogs/blob/master/img/web_semantica/Imagen21.png)

Este triple indica una relación entre los recursos __dbpedia:Lionel_Messi__ y __dbpedia:Argentina__

#### 2.3.2 Un segundo ejemplo de triple

El siguiente triple indica que Messi juega en Barcelona:

![Imagen22](https://github.com/garyDav/Blogs/blob/master/img/web_semantica/Imagen22.png)

Este triple indica una relación entre los recursos __dbpedia:Lionel_Messi__ y __dbpedia:FC_Barcelona__

#### 2.3.3 Un tercer ejemplo de triple

El siguiente triple indica que Messi nació el 24 de junio de 1987:

![Imagen23](https://github.com/garyDav/Blogs/blob/master/img/web_semantica/Imagen23.png)

>Hay que indicar que esto no es una fecha si no, una cadena de caracteres

Este triple indica que el valor del atributo __example:birthday__ para el recurso __dbpedia:Lionel_Messi__ es __"1987-06-24"__.

#### 3. Sintesis

* Un literal es una cadena de carcteres que representa un valor concreto y que puede tener un tipo asociado.

* Un triple en RDF tiene un sujeto, un predicado y un objeto.

* El sujeto y el predicado de un triple son URIs, mientras que el objeto puede ser un URI o un literal.

* Usualmente, los URIs son abreviados usando prefijos.

### El concepto de grafo RDF

#### 1. Un grafo RDF

Un grafo RDF está formado por un conjunto de triples RDF.

#### 1.1 Un primer ejemplo de un grafo RDF

Un grafo RDF puede tener sólo un triple.

![Imagen24](https://github.com/garyDav/Blogs/blob/master/img/web_semantica/Imagen24.png)

Este grafo RDF indica que Messi nació en Rosario.

#### 1.2 Un segundo ejemplo de grafo RDF

En este grafo RDF también especificamos que Messi vive en Barcelona:

![Imagen25](https://github.com/garyDav/Blogs/blob/master/img/web_semantica/Imagen25.png)

#### 1.3 Un ejemplo con aún más triples

En el siguiente grafo RDF además decimos que Rosario pertenece a la provincia de Santa Fe, y Barcelona a la provincia de Barcelona:

![Imagen26](https://github.com/garyDav/Blogs/blob/master/img/web_semantica/Imagen26.png)

#### 2. Un grafo RDF en la Web

Hemos construido un grafo en base a triples:

* Messi nació en Rosario

* Messi vive en Barcelona

* Rosario es parte de la Provincia de Santa Fe

* Barcelona es parte de la Provincia de Barcelona

>¿Cómo se almacena este __grafo__ en la Web?

#### 2.1 Un grafo RDF como un archivo

```rdf
dbpedia:Lionel_Messi   dbpprop:birthPlace     dbpedia:Rosario .
dbpedia:Lionel_Messi   dbpedia-owl:residence  dbpedia:Barcelona .
dbpedia:Rosario        dbpedia-owl:isPartOf   dbpedia:Santa_Fe_Province .
dbpedia:Barcelona      dbpedia-owl:isPartOf   dbpedia:Province_of_Barcelona .
```

#### 2.2 Uso de prefijos en un grafo RDF

Para simplificar la escritura de URIs en un grafo RDF usamos prefijos:

En el grafo RDF anterior usamos los siguientes prefijos:

```rdf
@prefix dbpedia:      http://dbpedia.org/resource/
@prefix dbpprop:      http://dbpedia.org/property/
@prefix dbpedia-owl:  http://dbpedia.org/ontology/
```

#### 2.3 Un grafo RDF completo

Aquí vemos un archivo completo de un grafo RDF

```rdf
@prefix dbpedia:      http://dbpedia.org/resource/
@prefix dbpprop:      http://dbpedia.org/property/
@prefix dbpedia-owl:  http://dbpedia.org/ontology/

dbpedia:Lionel_Messi   dbpprop:birthPlace     dbpedia:Rosario .
dbpedia:Lionel_Messi   dbpedia-owl:residence  dbpedia:Barcelona .
dbpedia:Rosario        dbpedia-owl:isPartOf   dbpedia:Santa_Fe_Province .
dbpedia:Barcelona      dbpedia-owl:isPartOf   dbpedia:Province_of_Barcelona .
```

#### 3. Síntesis

* Un grafo RDF está formado por un conjunto de triples.

* En la Web un grafo RDF se almacena como un asecuencia de triples.

* Para simplificar la escritura de URIs en un grafo RDF se utilizan prefijos.

### Vocabularios RDF

#### 1. ¿Qué indican lo prefijos de los URIs?

![Imagen27](https://github.com/garyDav/Blogs/blob/master/img/web_semantica/Imagen27.png)

#### 2. ¿Para qué sirven los vocabularios RDF?

![Imagen28](https://github.com/garyDav/Blogs/blob/master/img/web_semantica/Imagen28.png)

En resumen, los vocabularios sirven para construir
