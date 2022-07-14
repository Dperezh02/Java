# JAVA ORIENTADA A OBJETOS

## ¿Qué resuelve la Programación Orientada a Objetos?
#### La programación Orientada a Objetos nace de los problemas creados por la programación estructurada y nos ayuda a resolver cierto problemas como:

- Código muy largo: A medida que un sistema va creciendo y se hace más robusta el código generado se vuelve muy extenso haciéndose difícil de leer, depurar, mantener.

- Si algo falla, todo se rompe: Ya que con la programación estructurada el código se ejecuta secuencialmente al momento de que una de esas líneas fallara todo lo demás deja de funcionar.

- Difícil de mantener.

## Paradigma Orientado a Objetos

#### La Programación Orientada a Objetos viene de una filosofía o forma de pensar que es la Orientación a Objetos y esto surge a partir de los problemas que necesitamos plasmar en código.

Es analizar un problema en forma de objetos para después llevarlo a código, eso es la Orientación a Objetos.

Un paradigma es una teoría que suministra la base y modelo para resolver problemas. La paradigma de Programación Orientada a Objetos se compone de 4 elementos:

- Clases
- Propiedades
- Métodos
- Objetos

Y 4 Pilares:

- Encapsulamiento
- Abstracción
- Herencia
- Polimorfismo

## Diagramas de Modelado

#### OMT: Object Modeling Techniques. Es una metodología para el análisis orientado a objetos.

#### UML: Unified Modeling Language o Lenguaje de Modelado Unificado. Tomó las bases y técnicas de OMT unificándolas. Tenemos más opciones de diagramas como lo son Clases, Casos de Uso, Objetos, Actividades, Iteración, Estados, Implementación.

#### Esto significa que tendremos una manera gráfica de representar una situación. a continuación los elemenostos que se usan para realizar estas representaciones.

#### - Las clases se representan así:

![I1](https://github.com/Dperezh02/Java/blob/master/Imagenes%20de%20referencia/ClasesUML.png) 

En la parte superior se colocan los atributos o propiedades, y debajo las operaciones de la clase. Notarás que el primer caracter con el que empiezan es un símbolo. Este denotará la visibilidad del atributo o método.

Estos son los niveles de visibilidad que puedes tener:

- private -
- public +
- protected #
- default ~

#### - Asociación:

![I1](https://github.com/Dperezh02/Java/blob/master/Imagenes%20de%20referencia/Asociaci%C3%B3nUML.png) 

Como su nombre lo dice, notarás que cada vez que esté referenciada este tipo de flecha significará que ese elemento contiene al otro en su definición. La flecha apuntará hacia la dependencia.

![I1](https://github.com/Dperezh02/Java/blob/master/Imagenes%20de%20referencia/GraficoAsociaci%C3%B3nUML.png) 

Con esto vemos que la ClaseA está asociada y depende de la ClaseB.

#### - Herencia:

![I1](https://github.com/Dperezh02/Java/blob/master/Imagenes%20de%20referencia/HerenciaUML.png) 

Siempre que veamos este tipo de flecha se estará expresando la herencia.
La dirección de la flecha irá desde el hijo hasta el padre.

![I1](https://github.com/Dperezh02/Java/blob/master/Imagenes%20de%20referencia/GraficoHerenciaUML.png) 

Con esto vemos que la ClaseB hereda de la ClaseA.

#### - Agregación:

![I1](https://github.com/Dperezh02/Java/blob/master/Imagenes%20de%20referencia/Agregaci%C3%B3nUML.png) 

Este se parece a la asociación en que un elemento dependerá del otro, pero en este caso será: Un elemento dependerá de muchos otros. Aquí tomamos como referencia la multiplicidad del elemento. Lo que comúnmente conocerías en Bases de Datos como Relaciones uno a muchos.

![I1](https://github.com/Dperezh02/Java/blob/master/Imagenes%20de%20referencia/GraficoAsociaci%C3%B3nUML.png) 

Con esto decimos que la ClaseA contiene varios elementos de la ClaseB. Estos últimos son comúnmente representados con listas o colecciones de datos.

#### - Composición:


![I1](https://github.com/Dperezh02/Java/blob/master/Imagenes%20de%20referencia/Composici%C3%B3nUML.png) 

Este es similar al anterior solo que su relación es totalmente compenetrada de tal modo que conceptualmente una de estas clases no podría vivir si no existiera la otra.


![I1](https://github.com/Dperezh02/Java/blob/master/Imagenes%20de%20referencia/GraficoComposici%C3%B3nUML.png) 

## Modularidad

#### La modularidad va muy relacionada con las clases y es un principio de la Programación Orientado a Objetos y va de la mano con el Diseño Modular que significa dividir un sistema en partes pequeñas y estas serán nuestros módulos pudiendo funcionar de manera independiente. 

La modularidad nos permite:
- Reutilizar código
- Evitar Colapsos
- Mantenible
- Legibilidad
- Resolución Rápida de Problemas

## ¿Que es la herencia?

#### - Don’t repeat yourself - es una filosofía que promueve la reducción de duplicación en programación, esto nos va a inculcar que no tengamos líneas de código duplicadas.

Toda pieza de información nunca debería ser duplicada debido a que incrementa la dificultad en los cambios y evolución

La herencia nos permite crear nuevas clases a partir de otras, se basa en modelos y conceptos de la vida real. También tenemos una jerarquía de padre e hijo.


Ejemplo de la herencia:
- Sistema de uber

En user y driver se puede ver que se tienen los mismos atributos por ende estos pueden nacer de una superclase (Clase padre), llamada Accout de esta forma esta clase conendra la jerarquia principal de nuestras clases
![I1](https://github.com/Dperezh02/Java/blob/master/Imagenes%20de%20referencia/EjemploHerencia1.png) 

Las clases que estan abajo van a desaparecer, estos atributos podemos hacer que hereden de ACCOUNT

![I1](https://github.com/Dperezh02/Java/blob/master/Imagenes%20de%20referencia/EjemploHerencia2.png) 

#### La otra forma de utiliazar herencia es en elementos que tengan cosas en común, en este caso todas estas clases tienen  en comun que pertenecen a una clase llamada payments ()

![I1](https://github.com/Dperezh02/Java/blob/master/Imagenes%20de%20referencia/EjemploHerencia3.png) 

Ahora vamos con ubers, estas clases poseen diferentes atributos pero almenos entre ellos comperten 4 elementos, estos 4 elementos son los que van a conformar la clase padre CAR

![I1](https://github.com/Dperezh02/Java/blob/master/Imagenes%20de%20referencia/EjemploHerencia4.png) 

Las sub clases seran Uberx, uberPool, UberBlack y UberVan 

![I1](https://github.com/Dperezh02/Java/blob/master/Imagenes%20de%20referencia/EjemploHerencia5.png)

#### Modelo Completo UML

![I1](https://github.com/Dperezh02/Java/blob/master/Imagenes%20de%20referencia/EjemploHerencia6.png)