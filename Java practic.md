# JAVA

## 1. Declaraciones en java
  ```java
    int manzanas;
    String nombre;
  ```
## 2. Asignacion
  ```java
    manzanas = 10;
    nombre = "jack";
  ```

## 3. Declaracion y asignacion
  ```java
    int manzanas = 10;
    String nombre= "jack";
  ```

## 4. Impresión en la consola java
  ```java
    int manzanas = 10;
      System.out.println(manzanas);
    String nombre= "jack";
      System.out.println(nombre);
  ```
## 5. Concatenar
  ```java
    String nombre = "jack";
    nombre = nombre + " florez jimenez";
    nombre = "hola como estas " + nombre;
  ```
## 6. Constantes en java
  ```java
    String LAST_NAME = "Pérez";
    int ID_NUMBER = 1;
  ```

## 7. Low Camel Case y Upper Camel Case
  ```java
    // Upper Camel Case
    public class ExamplesTest {
    }
  
    // Low Camel Case
    String nameEmployee = "Daniela Pérez Henao";
  ```  
## 8. Tipos de datos númericos
### 8.1. Existe byte (ocupa 1 byte en la memoria RAM) short (ocupa 2 byte en la memoria) int (4 byte) long (8 byte).
### 8.2. Para el caso de puntos decimal java usa dos tipos de datos double (8 byte - para calculos matematicos que necesitan mucha precisión) y float (4 byte) 
![I1](https://github.com/Dperezh02/Java/blob/master/Imagenes%20de%20referencia/Tipo%20de%20datos%20numericos.png)
![I1](https://github.com/Dperezh02/Java/blob/master/Imagenes%20de%20referencia/Tipos%20de%20datos%20numericos.png)

  ```java
    // Numero entero (max. 10 numeros)
    int n = 1234567890;

    //Para diferenciarlo de Int colocar una L al final
     long nL = 12345678901L;

    //Numero grande en decimales
     double nD = 123.456;

    //Para diferenciarlo de Double colocar una F al final
     float nF = 123.456F;
  ```  
## 9. Tipos de datos texto
### Tenemos char (Ocupa 2 bytes y solo puede almacenar 1 dígito, debemos usar comillas simples en vez de comillas dobles.) y boolean (Son un tipo de dato lógico, solo aceptan los valores true y false. También ocupa 2 bytes y almacena únicamente 1 dígito.)
  ```java
    //Despues de java 10 se puede usar la palabra "Var"
    var nameEmployee = "Daniela Pérez"
  ```
## Operadores
### Asignación 
  ```java
    +=: a += b es equivalente a a = a + b.
    -=: a -= b es equivalente a a = a - b.
    *=: a *= b es equivalente a a = a * b.
    /=: a /= b es equivalente a a = a / b.
    %=: a %= b es equivalente a a = a % b.
### Incremento y decremento 
    ++: i++ es equivalente a i = i + 1.
    --: i-- es equivalente a i = i - 1.
  ```
## Operaciones Matematicas en Java con Math 
  ```java
    Math.PI // 3.141592653589793
    Math.E // 2.718281828459045

    Math.ceil(2.1) // 3.0 (redondear número hacia arriba)
    Math.floar(2.1) // 2.0 (redondear número hacia abajo)

    Math.pow(2, 3) // 8.0 (número elevado a una potencia)
    Math.sqrt(3) // 1.73... (raíz cuadrada)

    Math.max(2, 3) // 3.0 (el número más grande)

    // Área de un círculo (PI * r^2):
    Math.PI * Math.pow(r, 2)

    // Área de una esfera (4 * PI * r^2):
    4 * Math.PI * Math.pow(r, 2)

    // Volumen de una esfera ( (4/3) * PI * r^3):
    (4/3) * Math.PI * Math.pow(r, 3)
  ```
## Cast en variables: Estimación y exactitud
#### Estimación
  ```java
    double monthlyDogs = dogsQuantity / 12.0;
    // monthlyDogs: 2.5 (pero no es posible, ¡no rescatamos medio perrito!)

    int estimatedMonthlyDogs = (int) monthlyDogs;
    // estimatedMonthlyDogs: 2

    // Recuerda que el casteo no redondea, solo quita los decimales:
    Math.sqrt(3) // 1.7320508075688772
    (int) Math.sqrt(3) // 1
  ```
#### Exactitud
  ```java
    int a = 30;
    int b = 12;

    a / b // 2
    (double) a / b // 2.5
  ```
## Conversiones Cast
![I1]()
  ```java
    public class PracticaVideos {
      public static void main(String[] args) {
        int valorA = 300;
        int valorB = 45;
        
        System.out.println(valorA/valorB); //6
        System.out.println((double) valorA/valorB); //6.666666666666667

        double c = (double) valorA/valorB;

        System.out.println(c); //6.666666666666667
      }
  ```
## Ejercicios platzi
  ```java
      public class PracticaVideos {
        public static void main(String[] args) {
            //Ejercicio 1
            String nombrePadre = "Jhon Fredy";
            String primer_apellido_padre = " Pérez ";
            String segundo_apellido_padre = "Bañol";
            int edadPadre = 42;

            System.out.println("Mi papá se llama " + nombrePadre + primer_apellido_padre + segundo_apellido_padre + ". Y su edad es = " + edadPadre);

            String nombreMadre = "Vivian ";
            String primer_apellido_madre = "Henao ";
            String segundo_apellido_madre = "Londoño";
            int edadMadre = 34;

            System.out.println("Mi mamá se llama " + nombreMadre + primer_apellido_madre + segundo_apellido_madre + ". Y su edad es = " + edadMadre);

            String nombreHermana = "Maria Antonia ";
            String primer_apellido_Hermana = "Pérez ";
            String segundo_apellido_Hermana = "Henao";
            int edadHermana = 8;

            System.out.println("Mi Hermana se llama " + nombreHermana + primer_apellido_Hermana + segundo_apellido_Hermana + ". Y su edad es = " + edadHermana);

            /*char c = ‘z’; conviertelo a int
            int i = 250; conviertelo a long y luego de long a short
            double d = 301.067; conviertelo a long
            int i = 100; súmale 5000.66 y conviertelo a float
            int i = 737; multiplícalo por 100 y conviertelo a byte
            double d = 298.638; divídelo entre 25 y conviertelo a long*/

            //Ejercicio 2

            int i = 250;
            long il = (long) i;
            System.out.println(il); //250 estimación

            short ils = (short) il;
            System.out.println(ils); //250 estimación

            double d = 301.067;
            long dl = (long) d;
            System.out.println(dl); //301 exactitud

            int iI = 100;
            float iF = (float) (iI + 5000.66);
            System.out.println(iF); // 5100.66 estimación 

            int a = 737;
            System.out.println((byte) a*100); //-3100 estimación

            double b = 298.638;
            double b_operation = b/25;
            System.out.println((long) b_operation); //11 exactitud

        }
    }
  ```
## if en java 
  ```java
    boolean tiempo = true;
    boolean energia = true;
      
    if(tiempo && energia){
    System.out.println("Pues ponte a estudiar el Curso de Introducción a Java SE con Anahí Salgado en Platzi");
    } else {
      System.ou.println("Ve a terminar tus haceres y vuelve para estudiar")
    }
  ```
## Alcance y Scope de las variables 
### es que existen dos tipos de declaracion para variables:

##### Las variables globales: Se definen antes de entrar a una funcion o proceso y que como su nombre indica pueden ser llamadas a procesos en cualquier lugar ya que fueron previamente declaradas. (USO PUBLICO PODRIA DECIRSE)

##### Las variables locales: Son las que se definen para un proceso en especifico en un funcion especifica y solo van a ser reconocidas para esa funcion o proceso, es decir que si intentamos hacer la llamada a una variable local en otra funcion que no sea la de origen no la reconocera como declarada.(USO PRIVATIZADO)

