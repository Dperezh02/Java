# Java SE Orientado a Objetos

#### La Programación Orientada a Objetos (POO) nos ayuda a analizar y entender todos estos problemas para resolverlos de la forma más sostenible en el futuro. Java surgió con este paradigma y es uno de los lenguajes que define en gran manera el rumbo que sigue la POO.

## Abstracción: ¿Qué es una Clase?
#### Es el modelo sobre el cual se construira nuestro objeto. 

La Abstracción se trata de analizar objetos de forma independiente, sus propiedades, características y comportamientos, para abstraer su composición y generar un modelo, lo que traducimos a código como clases.

Las Clases son los modelos sobre los cuales construimos nuestros objetos, es decir, las clases son los “moldes” que nos permiten generar objetos. Cada clase debe tener identidad (con un nombre de clase único usando Upper Camel Case), estado (con sus atributos) y comportamiento (con sus métodos y operaciones). el primer paso es analizar (Abstracción) y el segundo diseñar sobre UML.

![I1](https://github.com/Dperezh02/Java/blob/master/Imagenes%20de%20referencia/Abstracci%C3%B3n.png)

### Clase - Objeto
#### Ejemplo: Clase, instancia, objetos, comportamientos y atributos.

![I1](https://github.com/Dperezh02/Java/blob/master/Imagenes%20de%20referencia/Clases-Objetos.png)

## Ahora a programar 
### Metodo Constructor 
#### El Método Constructor es el primer método que se ejecuta por defecto cuando creamos una clase, nos permite crear nuevas instancias de una clase. Lo invocamos con la palabra reservada new seguida del nombre con el que inicializamos la clase y paréntesis.

```java
	// nombreDeLaInstancia = new MétodoConstructor();
	myDoctor = new Doctor();
```