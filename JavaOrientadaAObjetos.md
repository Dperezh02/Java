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

--Las clases se representan así:

![I1]() 

En la parte superior se colocan los atributos o propiedades, y debajo las operaciones de la clase. Notarás que el primer caracter con el que empiezan es un símbolo. Este denotará la visibilidad del atributo o método.

Estos son los niveles de visibilidad que puedes tener:

- private
+ public
# protected
~ default

--Asociación:

![I1]() 

Como su nombre lo dice, notarás que cada vez que esté referenciada este tipo de flecha significará que ese elemento contiene al otro en su definición. La flecha apuntará hacia la dependencia.

![I1]() 

Con esto vemos que la ClaseA está asociada y depende de la ClaseB.

--Herencia:

![I1]() 

Siempre que veamos este tipo de flecha se estará expresando la herencia.
La dirección de la flecha irá desde el hijo hasta el padre.

![I1]() 

Con esto vemos que la ClaseB hereda de la ClaseA.

--Agregación:

![I1]() 

Este se parece a la asociación en que un elemento dependerá del otro, pero en este caso será: Un elemento dependerá de muchos otros. Aquí tomamos como referencia la multiplicidad del elemento. Lo que comúnmente conocerías en Bases de Datos como Relaciones uno a muchos.

![I1]() 

Con esto decimos que la ClaseA contiene varios elementos de la ClaseB. Estos últimos son comúnmente representados con listas o colecciones de datos.

--Composición:


![I1]() 

Este es similar al anterior solo que su relación es totalmente compenetrada de tal modo que conceptualmente una de estas clases no podría vivir si no existiera la otra.


![I1]() 