## Ejercicios 

1. Creamos una clase Account y una clase Car
```java
	public class Account {
    int id;
    String name;
    String document;
    String email;
    String password;
	}
```
```java
	public class Car {
    int id;
    String license;
    String driver;
    int passegenger;
	}
```
Creamos los metodos constructores para las dos clases 
```java
	public class Account {
    int id;
    String name;
    String document;
    String email;
    String password;
	}

    public Account(String name, String document, String email) {
        this.name = name;
        this.document = document;
        this.email = email;
    }
```
```java
	public class Car {
    int id;
    String license;
    String driver;
    int passegenger;
	}

    public Car(String license, String driver, int passegenger) {
        this.license = license;
        this.driver = driver;
        this.passegenger = passegenger;
    }
```

Ahora lo que se quiere mostrar es que dentro de un objeto puede instanciarse otro objeto de la siguiente manera:
```java
public class Car {
    int id;
    String license;
    String driver;
    int passegenger;
    Account atributoCuenta; // En la clase car creamos otro atributo un tipo de dato declarado Account por la clase que anteriormente creamos "Account"(Esto quiere decir que podemos tener otras clases dentro de clases)

    //Llamamos a "atributoCuenta" en el metodo constructor
    public Car(String license, String driver, int passegenger, Account atributoCuenta) {
        this.license = license;
        this.driver = driver;
        this.passegenger = passegenger;
        this.atributoCuenta = atributoCuenta;
    }
```
despues en el atributo (atributoCuenta) se instancia los atributos requeridos por el metodo constructor de la clase Account los cuales son (name, document, email)

Y en la clase Account lo que se hara es crear un metodo llamado "datosDeCuenta" 
```java
public class Account {
    Integer id;
    String name;
    String document;
    String email;
    String password;

    //Metodo constructor 
    public Account(String name, String document, String email) {
        this.name = name;
        this.document = document;
        this.email = email;
    }

    // Metodo para imprimir los datos que se solicita en el metodo constructor 
    void datosDeCuenta() {
        System.out.println("Name: " + this.name + " Document: " + this.document + "Email: " + this.email);
    }
}
```

que se podra llamar en la clase principal o main de la siguiente manera:
```java
public class Main {
    public static void main(String[] args) {
        Car carA = new Car("XCXV", "Daniela", 4, new Account("daniela", "234567", "DanielaPerezH@gm.com"));
        carA.printDataCar();
        carA.atributoCuenta.datosDeCuenta(); // Para ingresar a "datosCuenta" y poder imprimer el resultado toca entrar por el atributo de la clase car tipo de dato "Account" atributo "atributoCuenta"
    }
}
```
## Ejemplo 2
Clase Main 
```java
public class Main {
    public static void main(String[] args) {
        Empaque a = new Empaque("Plastico", "El piedruno", new FrutosSecos("Frutos secos", "Avellana", 22300));
        a.infoEmpaque();
        a.contenido.datosFrutos();
        System.out.println("----------------------------------");

        Empaque b = new Empaque("Carton", "Tosh", new FrutosSecos("Frutos rojos", "Rojo", 11500));
        b.contenido.datosFrutos();
        System.out.println("----------------------------------");

        Empaque c = new Empaque("Plastico", "Hindu", new FrutosSecos("Frutos Verdes", "Verde", 9000));
        c.infoEmpaque();
    }
}
```
Clase Empaque
```java
public class Empaque {
    String material;
    String logo;
    FrutosSecos contenido;

    public Empaque(String material, String logo, FrutosSecos contenido) {
        this.material = material;
        this.logo = logo;
        this.contenido = contenido;
    }
    void infoEmpaque() {
        System.out.println("Información basica del empaque:");
        System.out.println("- Material: " + this.material);
        System.out.println("- Logo: " + this.logo);
    }
}
```
Clase FrutosSecos
```java
public class FrutosSecos {
    String olor;
    String color;
    int precio;

    public FrutosSecos(String olor, String color, int precio) {
        this.olor = olor;
        this.color = color;
        this.precio = precio;
    }
    void datosFrutos(){
        System.out.println("Datos de los frutos secos:");
        System.out.println("- Olor: " + this.olor);
        System.out.println("- Color: " + this.color);
        System.out.println("- Precio: " + this.precio);
    }
}
```
## Ejemplo 3
Clase Main
```java
public class Main {
    public static void main(String[] args) {
        Billetera a = new Billetera("Gucchi", "Rojo, café y blanco", new Cedula(1002653647, "Daniela", "Pérez Henao", "F"));
        a.infoBilletera();
        System.out.println("-----------------------------");

        Billetera b = new Billetera("Arturo Calle", "Café", new Cedula(1009878765, "Andres", "Lopez Toro", "M"));
        System.out.println("-----------------------------");

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
        this.atributoCedula.datosCedula();
    }
}
```
Clase Cedula
```java
public class Cedula {
    int id;
    String nombre;
    String apellido;
    String sexo;

    public Cedula(int id, String nombre, String apellido, String sexo) {
        this.id = id;
        this.nombre = nombre;
        this.apellido = apellido;
        this.sexo = sexo;
    }
    void datosCedula() {
        System.out.println("Datos de la cedula: ");
        System.out.println("- Número de la cedula: " + this.id);
        System.out.println("- Nombre: " + this.nombre);
        System.out.println("- Apellido: " + this.apellido);
        System.out.println("- Sexo: " + this.sexo);
    }
}
```