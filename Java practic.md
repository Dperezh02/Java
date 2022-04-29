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
### Existe byte (ocupa 1 byte en la memoria RAM) short (ocupa 2 byte en la memoria) int (4 byte) long (8 byte).
### Para el caso de puntos decimal java usa dos tipos de datos double (8 byte - para calculos matematicos que necesitan mucha precisión) y float (4 byte)  
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
##Tipos de datos texto
### Tenemos char (Ocupa 2 bytes y solo puede almacenar 1 dígito, debemos usar comillas simples en vez de comillas dobles.) y boolean (Son un tipo de dato lógico, solo aceptan los valores true y false. También ocupa 2 bytes y almacena únicamente 1 dígito.)