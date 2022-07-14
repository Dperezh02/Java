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
### Main
```java
	 public static void main(String[] args) {
	        /*Crea una clase llamado cuenta que tendrá los siguientes atributos:
	        titular (que es nombre de la persona) y cantidad. El titular será obligatorio y la cantidad es opcional.
	        Construye los siguientes métodos para el metodo:
	        2.1 mostrar(): Muestra los datos de la cuenta.
	        2.2 ingresar(cantidad): se ingresa una cantidad a la cuenta, si la cantidad introducida es negativa, no se hará nada.
	        2.3 retirar(cantidad): se retira una cantidad a la cuenta. La cuenta puede estar en números rojos.*/

	        System.out.println("Bienvenido al sistema");
	        Cuenta cuenta = new Cuenta("Daniela Pérez Henao");
	        cuenta.mostrar();
	        cuenta.ingresar(20000);
	        cuenta.retirar();
	        cuenta.mostrar();
	        cuenta.ingresar(34000);
	        cuenta.mostrar();
	    }
```

### Clase
```java
	public class Cuenta {
	    String titular; //obligatorio
	    int cantidad; //Opcional

	    public Cuenta(String titular) {
	        this.titular = titular;
	    }

	    public void mostrar(){
	        System.out.println("Estos son los datos de la cuenta seleccionada---> " + " Titular de la cuenta: " + this.titular + ", Saldo disponible: " + this.cantidad);
	    }

	    void ingresar(int ingresarDinero){

	        this.cantidad = (ingresarDinero + this.cantidad);
	            System.out.println("Saldo diponible: " + this.cantidad);

	    }
	    void retirar(){
	        System.out.println("Ingrese la cantidad de dinero a retirar:");
	        Scanner sacar = new Scanner(System.in);
	        int sacarDinero = sacar.nextInt();

	        this.cantidad = (this.cantidad - sacarDinero);

	        System.out.println("Saldo disponible: " + this.cantidad);
	        if (this.cantidad < 0) {
	            System.out.println("El saldo esta en mora");
	        }
	    }
	}

```