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
- Dar un estado inicial al objeto
- Tiene el mismo nombre de la clase 
- Son los parametros minimos que necesita un objeto para vivir 
- En java el metodo puede no estar declarado por que el copilador de java siempre nos va a porveer un metodo constructor por defecto para todas las clases

```java
	// nombreDeLaInstancia = new MétodoConstructor();
	myDoctor = new Doctor();
```

### Aplicando herencia en lenguaje Java
```java
	//La calse Studen (Clase Hija) Extiende o hereda de la clase Person (Extiende de una clase padre)
	class Student extends Person
	// "extends Person" esto nos trae todos los metodos y atributos de la clase Person
```
Luego se debe de crear un constructor en la clase hijo que coincida con la clase padre, como se muestra acontinuación: 
```java
public class Person {
	int id;
	int edad;
    String nombre;
    String apellido;
    String sexo;

    public Person(int edad, String nombre, String apellido, String sexo) {
        this.edad = edad;
        this.nombre = nombre;
        this.apellido = apellido;
		this.sexo = sexo;
    }
}
```
```java
public class Student extends Person{
	String grado;
    String nombreColegio;

	//Metodo constructor en la clase hija que coincida con la clase padre
    public Student(int edad, String nombre, String apellido, String sexo, String grado, String nombreColegio) {
		//Super representara a la clase padre, super hara referencia a los atributos y metodos de la super clase
		super(edad, nombre, apellido, sexo)

		//this. hara referencia a los atributos y metodos de la subclase
        this.grado = grado;
        this.nombreColegio = nombreColegio;
    
    }
}
```
### ¿Como acceder a atributos de una clase padre en una clase hija?

#### Ejemplo

Clase main
```java
public class Main {
    public static void main(String[] args) {
        Billetera a = new Billetera("Gucchi", "Rojo, café y blanco", new Cedula(1002653647, "Daniela", "Pérez Henao", "F"));
        a.infoBilletera();
        System.out.println("-----------------------------");

        Billetera b = new Billetera("Arturo Calle", "Café", new Cedula(1009878765, "Andres", "Lopez Toro", "M"));
        System.out.println
		b.infoBilletera();
		b.datosCedula();
		("-----------------------------");

        Billetera c = new Billetera("Habbana", "Rosa", new Cedula(1049238798, "Manuela", "Montoya", "F"));
        c.infoBilletera();
    }
}
```
Clase Billetera
```java
public class Billetera {
    String marca;
    String color;
    Cedula atributoCedula;

    public Billetera(String marca, String color, Cedula atributoCedula) {
        this.marca = marca;
        this.color = color;
        this.atributoCedula = atributoCedula;
    }
    void infoBilletera() {
        System.out.println("Diseño billetera: ");
        System.out.println("- Marca: " + this.marca);
        System.out.println("- Color: " + this.color);
        this.atributoCedula.datosCedula(); //al llamar en MAIN "a.infoBilletera" se imprime lo que esta dentro este metodo y para no imprimir en el main el metodo "a.infoBilletera" y "datosCedula()" unimos todo en esta linea e imprimimos la información general de la clase cedula, el metodo (datosCedula())
    }
}
```
Clase Tarjeta (Clase padre)
```java
public class Tarjeta {
    int id;
    String nombre;
    String apellido;

    public Tarjeta(int id, String nombre, String apellido){
        this.id = id;
        this.nombre = nombre;
        this.apellido = apellido;
    }
    void datos(){
        System.out.println("- Número de la cedula: " + this.id);
        System.out.println("- Nombre: " + this.nombre);
        System.out.println("- Apellido: " + this.apellido);
    }
}
```
Clase Cedula (Clase hija)
Como se puede observar acontinuación para imprimir en el metodo de la clase hija un atributo de la clase padre se debe de poner:
```java
super.nombre
//En vez de 
this.nombre
/*Pues como se explico anteriormente "super" hace referencia a la super clase (Clase padre) y "this" hace referencia a la subclase (Clase hija)*/
```

```java
public class Cedula extends Tarjeta{
    String sexo;

    public Cedula(int id, String nombre, String apellido, String sexo) {
        super(id, nombre, apellido);

        this.sexo = sexo;
    }
    void datosCedula() {
        System.out.println("Datos de la cedula: ");
        System.out.println("- Número de la cedula: " + super.id); // acceder a los datos del super
        System.out.println("- Nombre: " + super.nombre);
        System.out.println("- Apellido: " + super.apellido);
        System.out.println("- Sexo: " + this.sexo);
    }
}
```
Clase TarjetaDeCredito (Clase hija)
```java
public class TarjetaDeCredito extends Tarjeta{
    String banco;
    int ccv;
    String fechaDeValidez;
    String fechaDeterminacion;

    public TarjetaDeCredito(int id, String nombre, String apellido, String banco, int ccv, String fechaDeValidez, String fechaDeterminacion) {
        super(id, nombre, apellido);

        this.banco = banco;
        this.ccv = ccv;
        this.fechaDeValidez = fechaDeValidez;
        this.fechaDeterminacion = fechaDeterminacion;
    }
}
```
### Aplicando encapsulamiento en lenguaje Java
El encapsulamiento es hacer que un dato sea inalterable cuando se le asigne un modificador de acceso (no se trata solo de ocultar el dato sino también de protegerlo). Un modificador de acceso define el alcance y visibilidad de un miembro de clase.
La encapsulacion es también llamada **ocultamiento de información.**

Algunos beneficios de encapsulación son:

- Controlar la manera en que los datos son accedidos o modificados.
- Código más flexible y fácil de cambiar a partir de nuevos requerimientos.
- Posibilidad de modificar una parte del código sin afectar otras partes del mismo.
- Mantiene la integridad de los datos

Estos son los modificadores de acceso:
```java
public // Todas las clases 
protected // Clases, paquetes y sub clases
default // Clases internas y paquetes, no podra ser accedido al nivel de la herencia 
private // Clases, solo puede ser modificado dentro de la clase 
```
Ejemplo:
```java
public class FrutosSecos {
    String olor;
    String color;
    private int precio;
}
```
#### ¿Como acceder a un atributo privado?
Mediante los getters y setters podemos acceder a un atributo privado, estos metodos me permiten alterar el atributo privado 
```java
    // Con el get traemos el dato privado
    public int getPrecio(){
        return precio;
    }
    //Con set cambiamos el dato y se pone public void por que no se va a devolver nada.
    public void setPrecio(int precio)/*adentro va el tipo de dato que va a solicitar en el main*/{
        this.precio = precio;//Como se hace en el metodo constructor
    }
```
y ponemos una condición para que solo se ingrese el número que se desea conservar 
```java
    // Con el get traemos el dato privado
    public int getPrecio(){
        return precio;
    }
    //Con set cambiamos el dato
    public void setPrecio(int precio){
        this.precio = precio;

        if (this.precio == 20000) {
            System.out.println("Datos de los frutos secos:");
            System.out.println("- Olor: " + this.olor);
            System.out.println("- Color: " + this.color);
            System.out.println(this.precio);
        } else {
            System.out.println("El precio para este producto debe ser 20000");
        }
    }
```
Y así se llamaria en el main
```java
public class Main {
    public static void main(String[] args) {

        FrutosSecos a = new FrutosSecos("Manazana verde", "Verde");
        a.setPrecio(20000);

    }
}
```
