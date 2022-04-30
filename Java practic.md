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