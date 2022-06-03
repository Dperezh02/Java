# JAVA

## Declaraciones en java
  ```java
    int manzanas;
    String nombre;
  ```
## Asignacion
  ```java
    manzanas = 10;
    nombre = "jack";
  ```

## Declaracion y asignacion
  ```java
    int manzanas = 10;
    String nombre= "jack";
  ```

## Impresión en la consola java
  ```java
    int manzanas = 10;
      System.out.println(manzanas);
    String nombre= "jack";
      System.out.println(nombre);
  ```
## Concatenar
  ```java
    String nombre = "jack";
    nombre = nombre + " florez jimenez";
    nombre = "hola como estas " + nombre;
  ```
## Constantes en java
  ```java
    String LAST_NAME = "Pérez";
    int ID_NUMBER = 1;
  ```

## Low Camel Case y Upper Camel Case
  ```java
    // Upper Camel Case
    public class ExamplesTest {
    }
  
    // Low Camel Case
    String nameEmployee = "Daniela Pérez Henao";
  ```  
## Tipos de datos númericos
#### 1. Existe byte (ocupa 1 byte en la memoria RAM) short (ocupa 2 byte en la memoria) int (4 byte) long (8 byte).
#### 2. Para el caso de puntos decimal java usa dos tipos de datos double (8 byte - para calculos matematicos que necesitan mucha precisión) y float (4 byte) 
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
## Tipos de datos texto
#### Tenemos char (Ocupa 2 bytes y solo puede almacenar 1 dígito, debemos usar comillas simples en vez de comillas dobles.) y boolean (Son un tipo de dato lógico, solo aceptan los valores true y false. También ocupa 2 bytes y almacena únicamente 1 dígito.)
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
![I1](https://github.com/Dperezh02/Java/blob/master/Imagenes%20de%20referencia/Casteo%20de%20datos.png)
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
![I1](https://github.com/Dperezh02/Java/blob/master/Imagenes%20de%20referencia/Scope%20de%20las%20variables.png)

## Operadores logicos
  ```java
  Operadores de equidad:

   - Igualdad: ==
   - Desigualdad: !=

  Operadores Relacionales:

   - Menor que: <
   - Mayor que: >
   - Menor o igual que: <=
   - Mayor o igual que: >=
  
  Operadores lógicos:

   - &&: AND (evaluar si dos o más condiciones son verdaderas).
   - ||: OR (evaluar si al menos una de las condiciones es verdadera).
   - !: NOT (evaluar que la condición NO sea verdadera).
  ```
  ![I1](https://github.com/Dperezh02/Java/blob/master/Imagenes%20de%20referencia/Operadores%20logicos%20-%20tabla%20de%20la%20verdad.png) 

## Estrucura if / else if 
  ```java
    if (condición) {
      instrucciones
    } else if (condcion) {
      instrucciones
    } else {
      instrucciones
    }
  ```
## Sentencia Switch
  ```java
  String fruta = "Mangostino";
  switch (fruta){
    case "Mango":
      System.out.println("¡Mi fruta favorita es el mango!");
      break;
    case "Lulo":
      System.out.println("¡Mi fruta favorita es el lulo!");
      break;
    case "Mangostino":
      System.out.println("Mi fruta favorita es el mangostino");
      break;
    default:
      System.out.println("¡no hay frutas!");
      break;
  }
  ```
## ¿Para qué sirven las funciones?

### • Funciones: 
#### nos ayudan a organizar, modularizar y evitar el código repetido.
### • Return: 
#### palabra clave cuando una función tiene un valor de regreso.
### • Void: 
#### palabra clave cuando una función no tiene un valor de regreso.
### • Nota: 
#### si nuestras funciones van a devolver argumentos, lo mejor es que especifiques el tipo de dato que serán. Para utilizar nuestras funciones solo debemos asignar el resultado de la función y sus parámetros a una variable con el mismo tipo de dato de la función.
![I1]() 

## Implementación función 
 ```java
public static double suma(double numeroUno, double numeroDos){
  int suma = numeroUno + numeroDos;

  return suma; 
}
  ```
 ```java
 public static double conversorDeDolar(double quantity, String currency){
  switch (currency);
    case "COP":
      quantity = quantity * 0.00031;
      break;
    case "EUR":
      quantity = quantity * 0,00025;
      break;
}
return quantity;
  ```