# INTRODUCCIÓN A JAVA

## Variables en java 
Una variable nos va a permitir almacenar información y se llama variable dado que en cualquier momento el contenido de esta pueda cambiar, nuestras variables pueden almacenar diferentes tipos de datos como por ejemplo, **Numericos**, **Textos** o **Cadenas**.

En java exiten dos diferentes tipos de datos de tipo **Primitivos** y **Referenciados** (Tipo object (Clases, interfaces, arrays))

## Declaraciones en java
  ```java
    int manzanas;
    String nombre;
  ```
## Asignación
  ```java
  // Después del igual a ese dato se le llama "literal".
    manzanas = 10;
    nombre = "jack";
  ```

## Declaración y asignación
  ```java
    int manzanas = 10;
    String nombre = "jack";
  ```
Apartir de la versión 10 de java podemos usar la palabra reservada **VAR** en lugar de usar el tipo de dato definido, podemos simplemente poner var para que java infiera el tipo de dato que estamos utilizando.
  ```java
  // var - inferencia en tipo de datos segun la literal que se le proporcione.
    var manzanas = 10;
    var nombre = "jack";
  ```
## Impresión en la consola java (sout)
  ```java
    int manzanas = 10;
    System.out.println(manzanas);
    
    String nombre= "jack";
    System.out.println(nombre);
  ```
## Concatenación de variables 
  ```java
    String nombre = "jack";
    nombre = nombre + " florez jimenez";
    nombre = "hola como estas " + nombre;
  ```
  ```java
    String usuario = "Juan";
    String titulo = "Ingeniero";
    String union = titulo + " " + usuario;
    System.out.println("union = " + union);
        
    int i = 3;
    int j = 4;
        
    System.out.println(i + j);//se realiza la suma de numeros (7)
    System.out.println(i + j + usuario); //Evaluación de izq a der, realiza suma (7Juan)
    System.out.println(usuario + i + j);//contexto cadena, todo es una cadena (Juan34)
    System.out.println(usuario + (i + j));//uso de parentesis modifican la prioridad en la evaluación (Juan7)  
  ```
## Caracteres especiales
  ```java
    String nombre = "Karla";

      System.out.println("Nueva linea: \n" + nombre);
      System.out.println("Tabulador: \t" + nombre);
      System.out.println("Retroceso: \b\b" + nombre);
      System.out.println("Comilla simple: \'" + nombre + "\'");
      System.out.println(" Comilla doble: \"" + nombre + "\"");
  ```
## Clase Scanner en java
  ```java
    System.out.println("Escribe tu nombre:");
    
    Scanner consola = new Scanner(System.in); // Puede llamarse el Scanner 1 vez 
    String usuario = consola.nextLine(); // usarse en esta linea
    System.out.println("usuario = " + usuario);
    
    System.out.println("Escribe el titulo:");
    String titulo = consola.nextLine(); // Y volver a reutilizarse en esta linea
    System.out.println("Resultado: " + titulo + " " + usuario); 
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
#### 2. Para el caso de puntos decimal java usa dos tipos de datos double (8 byte - para calculos matematicos que necesitan mucha precisión) y float (4 byte).

![I1](https://github.com/Dperezh02/Java/blob/master/Imagenes%20de%20referencia/Tipo%20de%20datos%20numericos.png)
![I1](https://github.com/Dperezh02/Java/blob/master/Imagenes%20de%20referencia/Tipos%20de%20datos%20numericos.png)

#### Por un lado tenemos los tipos enteros, entre los cuales tenemos el tipo byte el cual ocupa 8 bits.
Posteriormente tenemos el tipo short, el cual ocupa 16 bits. También tenemos el tipo char, el cual ocupa
16 bits pero maneja el código UNICODE para almacenar valores tipo char. A su vez tenemos el tipo int el cual ocupa 32 bits, y finalmente el tipo long el cual ocupa 64 bits.
Por otro lado tenemos los tipos flotantes, por un lado el tipo float el cual ocupa 32 bits, y el tipo double
que ocupa 64 bits. El tipo boolean en Java también es un tipo primitivo y puede almacenar sólo el valor de
true o false. Su valor por default es false.

![I1](https://github.com/Dperezh02/Java/blob/master/Imagenes%20de%20referencia/Tipo%20primitivos.png)

  ```java
    // Numero entero (max. 10 numeros)
    int n = 1234567890;

    //Para diferenciarlo de Int colocar una L al final
     long nL = 12345678901L;

    //Numero grande en decimales
     double nD = git123.456;

    //Para diferenciarlo de Double colocar una F al final
     float nF = 123.456F;
  ```  
  ```java
    byte numeroByte = 10;
    System.out.println("Valor byte:" + numeroByte);
    // MIN_VALUE es una constante la cual nos trae el valor minimo de Byte
    System.out.println("Valor minimo byte:" + Byte.MIN_VALUE);
    // MAX_VALUE es una constante la cual nos trae el valor maximo de Byte
    System.out.println("Valor maximo byte:" + Byte.MAX_VALUE);
    // Rango de byte -128 a 127

    /* Si queremos asignar el valor 129 nos va a salir un error pues se sale del rango de byte, entonces lo que podemos hacer es obligar al copilador a convertir ese número entero (129) a un tipo byte con la siguiente sintaxis; sin embargo al impimir nuestra variable no almacena el valor (129)*/
    byte numeroByte = (byte) 129;
  ``` 
## Tipos de datos texto
#### También tenemos el tipo char, el cual ocupa 16 bits pero maneja el código UNICODE para almacenar valores tipo char y solo puede almacenar 1 dígito, debemos usar comillas simples en vez de comillas dobles.
En esta página podemos encontrar la lista de Unicode characters.(https://en.wikipedia.org/wiki/List_of_Unicode_characters)
  ```java
  char miCaracter = 'a';
  System.out.println("miCaracter = " + miCaracter);
  //miCaracter = a

  // Simbolo unicode - \u      
  char varChar = '\u0021';
  System.out.println("varChar = " + varChar);
  //varChar = !
        
  char varCharDecimal = 33;
  System.out.println("varCharDecimal = " + varCharDecimal);
  //varCharDecimal = !
        
  char varCharSimbolo = '!';
  System.out.println("varCharSimbolo = " + varCharSimbolo);
  //varCharSimbolo = !
        
  var varChar1 = '\u0021';
  System.out.println("varChar1 = " + varChar1);
  //varChar1 = !
        
  var varCharDecimal2 = 33;
  System.out.println("varCharDecimal2 = " + varCharDecimal2);
  //varCharDecimal2 = 33
        
  var varCharSimbolo3 = '!';
  System.out.println("varCharSimbolo3 = " + varCharSimbolo3);
  //varCharSimbolo3 = !
        
  int variableEnteraSimbolo = '!';
  System.out.println("variableEnteraSimbolo = " + variableEnteraSimbolo);
  //variableEnteraSimbolo = 33
        
  int letra = 'A';
  System.out.println("letra = " + letra);
  //letra = 65
  ```  
#### y boolean (Son un tipo de dato lógico, solo aceptan los valores true y false. También ocupa 2 bytes y almacena únicamente 1 dígito.)
  ```java
  public class HolaMundo {
    public static void main(String args[]) {
       boolean varBoolean = true;
       System.out.println("varBoolean = " + varBoolean);
        
       if(varBoolean){
           System.out.println("La bandera es verdadera");
       } 
       else{
           System.out.println("La bandera es falsa");
       }
       
       System.out.println("-------------------");

       var edad = 10;
       //var esAdulto = edad >= 18;
       if( edad >= 18 ){
           System.out.println("Eres mayor de edad");
       }
       else{
           System.out.println("Eres menor de edad");
       }
    }
}
  ```
## Operadores
### Asignación 
  ```java
    +=: a += b es equivalente a a = a + b.
    -=: a -= b es equivalente a a = a - b.
    *=: a *= b es equivalente a a = a * b.
    /=: a /= b es equivalente a a = a / b.
    %=: a %= b es equivalente a a = a % b.
  ```
### Incremento y decremento 
  ```java
    ++: i++ es equivalente a i = i + 1.
    --: i-- es equivalente a i = i - 1.
  ```
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

**Más sobre operadores en el recurso "Operadores en java"**

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
## Conversión de tipos primitivos
  ```java
    public class HolaMundo {
      public static void main(String args[]) {
        //Convertir tipo String a un tipo int
        var edad = Integer.parseInt("20");
        //var edad = "20";
        System.out.println("edad = " + (edad + 1));
        
        var valorPI = Double.parseDouble("3.1416");
        System.out.println("valorPI = " + valorPI);
        
        //Pedir un valor 
        //Integer.parseInt() - intenta tomar un valor de una cadena y convertirlo a un entero
        var consola = new Scanner(System.in);
        System.out.println("Proporciona tu edad:");
        edad = Integer.parseInt( consola.nextLine() );
        System.out.println("edad = " + edad);
      }
    }
  ```
Ahora un tipo int a un tipo String (inverso) mediante  String.valueOf(10); el cual convierte un tipo proporcionado a un tipo String 
  ```java
public class HolaMundo {
    public static void main(String args[]) {
        //Convertir tipo String a un tipo int
        var edad = Integer.parseInt("20");
        //var edad = "20";
        System.out.println("edad = " + (edad + 1));
        
        var valorPI = Double.parseDouble("3.1416");
        System.out.println("valorPI = " + valorPI);
        
        //Pedir un valor 
        var consola = new Scanner(System.in);
        //System.out.println("Proporciona tu edad:");
        //edad = Integer.parseInt( consola.nextLine() );
        //System.out.println("edad = " + edad);
        
        var edadTexto = String.valueOf(10);
        System.out.println("edadTexto = " + edadTexto);
        
        //De tipo String a char
        var caracter = "hola".charAt(1);
        System.out.println("caracter = " + caracter);
        //charAt(0) devuelve el caracter que allí solicital, sin embargo un valor de tipo entero no contiene este metodo solo toma los de tipo String
        System.out.println("Proporciona un caracter:");
        caracter = consola.nextLine().charAt(0);
        System.out.println("caracter = " + caracter);
      }
    }
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
![I1](https://github.com/Dperezh02/Java/blob/master/Imagenes%20de%20referencia/Funciones.png) 

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
## Tags Java Docs
![I1](https://github.com/Dperezh02/Java/blob/master/Imagenes%20de%20referencia/Tags%20java%20Docs.png) 

## Tags 
  ```java
    /**
     *Descripción: funcion que especificando la moneda convierte una cantidad de dinero a dolares // Descripción general de nuestra función. 
     * 
     * @param quantity Cantidad de dinero // Descripción del parámetro quanity.
     * @param currency Tipo de moneda: solo acepta COP o EUR // Descripción del parámetro currency (MXN o COP).
     * @return Devuelve la cantidad actualizada en dolares// Descripción del valor que devolvemos en esta función.
     * */
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
#### Para activar la visibilidad de la documentación en Windows:
  ```java
    File > Settings > Editor > General > Code Completion 
    y pasas a activar la opción 
    "Show the documentation popup in 1000 ms" 
    y por ultimo le das a OK
  ```
## Bucle Do While
#### Primero se ejecuta y luego se evalua la condición
  ```java
    do {
      //Instrucciones
    } while (condicion);
  ```
#### Ejemplo 1:
  ```java
    var contador = 0;
        do {
          System.out.println("contador = " + contador);
          contador++;
        } while (contador < 3);
  ```
#### Ejemplo 2:
  ```java
    int respuesta = 0;

    do {
      System.out.println("Bienvenida Daniela, seleccione la opción deseada");
      System.out.println("1. Peliculas");
      System.out.println("2. Musica");
      System.out.println("3. salir");

      Scanner in = new Scanner(System.in);
      respuesta = Integer.valueOf(in.nextLine());

      switch (respuesta) {
          case 1:
              System.out.println("Estas son las peliculas disponibles, Casa fantasmas, el ataque, que paso ayer");
              break;
          case 2:
              System.out.println("Esta es la musica disponible, Pop, Ballenato, Salsa");
              break;
          case 3:
              System.out.println("Gracias por visitarnos");
              break;
          default:
              System.out.println("Selecciona una respuesta correcta");
      }
    } while (respuesta != 3);
    System.out.println("Gracias por visitarnos");
  ```
## Bucle While
#### Primero se ejecuta la condición y luego se ejecuta
  ```java
  while (condicion) {
    //instrucciones
  }
  ```
#### Ejemplo 1:
  ```java
    var contador = 0;
        while ( contador < 3 ) {
          System.out.println("contador = " + contador);
          contador++;
        }
  ```
#### Ejemplo 2:
  ```java
    int x = 1;

      // Salir cuando x llega a ser mayor que 4
      while (x <= 4)
      {
          System.out.println("Valor de x: " + x);

          //incrementa el valor de x para la siguiente iteración
          x++;
      }
  ```
## Bucle for
  ```java
    for (inicializacion;condicion;incremento) {
      //Instrucciones
    }
  ```
#### Ejemplo 1:
  ```java
    var contador = 0;
        while ( contador < 3 ) {
          System.out.println("contador = " + contador);
          contador++;
        }
  ```
#### Ejemplo 2:
  ```java
    for( var contador = 0 ; contador < 3 ; contador++ ){
      System.out.println("contador = " + contador);
    }
  ```
### Palabras Break y Continue
- Break: Rompe un ciclo.
```java
    for(var contador = 0 ; contador < 3 ; contador++){
        if( contador % 2 == 0){
            System.out.println("contador = " + contador);
            break; //Al poner este break aqui estaremos rompiendo el ciclo y solo se va a ejecutar una vez, Si es número par, se imprime en consola pero ademas termina el ciclo, si se quita el break lo que sucede es que se imprimen todos los números pares.
        }   
    }
```
- Continue: Continuar a la sigiente iteración
```java
  for(var contador = 0 ; contador < 3 ; contador++){
        if(contador % 2 != 0){
            continue;//ir a la siguiente iteracion
        }   
        System.out.println("contador = " + contador);
  }
```
### Uso de etiquetas 
El manejo de etiquetas es simplemente agregar un texto, por ejemplo **Inicio**, utilizamos la palabra continue y posteriormente la palabra que hemos definido "Inicio", entonces en este caso en lugar de decir que vamos a la siguiente iteración le estamos diciendo que vamos a ir a la línea de código donde hemos puesto esa etiqueta, este uso de etiquetas puede ser de utilidad en ciclos for anidados, en otros casos no es común usarlo y para la palabra Break es lo mismo.
```java
  inicio:
  for(var contador = 0 ; contador < 3 ; contador++){
      if( contador % 2 != 0){
          continue inicio;//ir a la linea de codigo de la etiqueta
      }   
      System.out.println("contador = " + contador);
  }
```
Más, sin embargo, no es recomendable usar este tipo de programación 
## Arrays
#### Los arreglos o arrays son objetos en los que podemos guardar más de una variable.
#### Los arrays se definen en código de las siguientes maneras:
  ```java
    // 1. Definir el nombre de la variable y el tipo de datos
    //  que va a contener, cualquiera de las siguientes dos
    // opciones es válida:
    TipoDato[] nombreVariable;
    TipoDato nombreVariable[];

    // 2. Definir el tamaño del array, la cantidad de elementos
    // que podemos guardar en el array:
    TipoDato[] nombreVariable = new TipoDato[capacidad];

    // Array de dos dimensiones:
    TipoDato[][] cities = new String[númeroFilas][númeroColumnas];
  ```
#### Declarando arreglos
  ```java
    String[][] cities = new String[4][2];

    //Tres dimensiones
    String[][][] cities = new String[3][2][2];
  ```
## Indices y búsqueda de elementos en Arrays
#### Los índices son variables simples que nos ayudan a identificar las posiciones en un arreglo. Estas variables siempre guardan números, comienzan en 0 e incrementan de abajo a arriba y de izquierda a derecha.

#### Para guardar un valor en alguna posición de nuestro array solo debemos usar el índice de la siguiente forma:
  ```java
    //[filas][columnas]
    cities[0][0] = "Colombia";
    cities[1][0] = "Colombia";
    cities[2][0] = "Mexico";
    cities[3][0] = "Mexico";
    cities[0][1] = "Medellin";
    cities[1][1] = "Bogota";
    cities[2][1] = "Guadalajara";
    cities[3][1] = "CDMX";

    System.out.println(cities[0][0]);
    System.out.println(cities[0][1]);
    System.out.println(cities[1][0]);
    System.out.println(cities[1][1]);
    System.out.println(cities[2][0]);
    System.out.println(cities[2][1]);
    System.out.println(cities[3][0]);
    System.out.println(cities[3][1]);
  ```
## Imprimir en consola un arreglo
  ```java
    import java.util.Scanner;
    import java.util.Arrays;
    //Se debe de importar la libreria util.Arrays
    public class DoWhile {

        public static void main(String[] args) {

            System.out.println("--- Creemos una lista ---");

            System.out.println("Digite un número");
            Scanner num = new Scanner(System.in);
            int numeroInicial = num.nextInt();

            //TipoDeDato / nombre = new tipoDeDato[Capacidad]
            String[] list = new String[numeroInicial]; // la capacidad es el número que tomamos del scanner pues este puede ser aleatorio seleccionado por el humano.
            /*[ , , , ]
               0 1 2 3 */
            int acomulador = 0; // Se crea una variable inicializada en 0 para ir incrementando hasta llegar al numero ingresado desde el scanner
            while (acomulador < numeroInicial) {
                System.out.println("Digite la palabra");
                Scanner pl = new Scanner(System.in);
                String palabra = pl.nextLine(); // un scanner para ir guardando las palabras ingresadas

                //0 ciclo
                        //1 ciclo
                                //2 ciclo
                                        //3 ciclo
                list[acomulador]= palabra; //Se pone acumulador pues va recorriendo cada ciclo y en cada recorrido va a ir guardando la palabra que fue ingresada en el scanner

                acomulador++; //va incrementando + 1 hasta llegar al numero inicial 
            }
            System.out.println(Arrays.toString(list)); //Arrays clase que tiene un metodo toString; coge un arreglo y lo permite visualizar en consola.
        }
    }

  ```
## Ciclos for anidados
  ```java
    // Array de una sola dimensión:
    for (int i = 0; i <= 3; i++) {
      System.out.println(i);
    }
    // El resultado será: 0, 1, 2, 3

    // Array de dos dimensiones:
    for (int filas = 0; filas < cities.length; filas++) {
      for (int columnas = 0; columnas < cities[filas].length; columnas++) {
        System.out.println(cities[filas][columnas]);
      }
    }
    // El resultado será:
    // Colombia
    // Bogotá
    // México
    // Guadalajara
    // España
    // Madrid
  ```



