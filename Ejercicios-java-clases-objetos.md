### Main
```java
	public class Main {
	   public static void main(String[] args) {
	       // nace malu instanciamos un gato nuevo en la creacion y eres Dios wiii
	       Gato a = new Gato("malu");
	       System.out.println("gato a: " + a.nombre);
	       System.out.println("gato a: " + a.color);
	       System.out.println("gato a: " + a.tamano);

	       System.out.println("--------------");

	       Gato b = new Gato("luna");
	       System.out.println("gato b: " + b.nombre);
	       System.out.println("gato b: " + b.color);
	       System.out.println("gato a: " + b.tamano);
	       b.fichaTecnica();
	       System.out.println(b.crecer(10));
	       b.fichaTecnica();
	       b.crecer(10);
	       b.fichaTecnica();
	   }
	}

```

### Clase
```java
	public class Gato {
	   String nombre;
	   String color;
	   int tamano;

	   // Metodo constructor -- el primer parametro que se utiliza para generar la base inicial del objeto y no generar tantas lineas de codigo en el main
	   public Gato(String nombre){
	       this.nombre = nombre;
	       this.color = "rojo";
	       this.tamano = 5;// cm
	   }

	   void fichaTecnica(){
	       System.out.println("Datos del gato: -------- " + "Nombre: " +  this.nombre + ", color: " + this.color + ", tamaño: " + this.tamano);
	   }

	   int crecer(int anos){
	       this.nombre = "creciooo";
	       this.tamano = this.tamano + anos;
	       return this.tamano;
	   }

```

### Main
```java
	public static void main(String[] args) {
	   /*Crear un metodo constructor llamada persona. Sus atributos son: nombre, edad y cedula.
	   Construye los siguientes métodos para la clase:
	   1.1 mostrar(): Muestra los datos de la persona.
	   1.2 es_mayor_de_edad(): Devuelve un valor lógico indicando si es mayor de edad.*/

	   Persona Persona = new Persona("Jack", 12, 1053803202);
	   Persona.mostrar();
	   Persona.esMayorDeEdad();
	}

```

### Clase
```java
	public class Persona {
	   String nombre;
	   int edad;
	   int cedula;

	   public Persona(String nombre, int edad, int cedula) {
	       this.nombre = nombre;
	       this.edad = edad;
	       this.cedula = cedula;
	   }
	   void mostrar() {
	       System.out.println("Estos son los datos de la persona ----> " + " Nombre: " + this.nombre + ", edad: " + this.edad + ", cédula: " + this.cedula);
	   }
	   void esMayorDeEdad() {
	       if (this.edad >= 18) {
	           System.out.println("El humano es mayor de edad");
	       } else {
	           System.out.println("Error(X) el humano es menor");
	       }
	   }
	}

```
