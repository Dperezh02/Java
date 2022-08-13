# Operadores 

## Operadores Aritmeticos
```java
  public static void main(String args[]) {
    int a=3, b=2;
    var resultado = a + b;
    System.out.println("resultado suma = " + resultado);
    
    resultado = a - b;
    System.out.println("resultado resta = " + resultado);
    
    resultado = a * b;
    System.out.println("resultado multiplicacion = " + resultado);
    
    var resultado2 = 3D / b;
    System.out.println("resultado division = " + resultado2);
    
    resultado = a % b;
    System.out.println("resultado modulo = " + resultado);
    
    if( b % 2 == 0)
        System.out.println("Es numero par");
    else
        System.out.println("Es numero impar");
  }
```
## Operadores Asignación Composición
```java
  public static void main(String args[]) {
    int a = 3, b=2;
    int c = a + 5 - b; 
    System.out.println("c = " + c);
    
    a += 1;//a = a + 1
    System.out.println("a = " + a);
    
    a += 3;//a = a + 3
    System.out.println("a = " + a);
    
    a -= 2;//a = a - 2
    System.out.println("a = " + a);
    
    // *=   /=   %=
  }
```
## Operadores Unarios
```java
  public static void main(String args[]) {
    var a = 3;
    var b = -a;
    System.out.println("a = " + a);
    System.out.println("b = " + b);
    
    var c = true;
    var d = !c;
    System.out.println("c = " + c);
    System.out.println("d = " + d);
    
    //incremento
    //1.preincremento (simbolo antes de la variable)
    var e = 3;
    var f = ++e;//primero se incrementa la variable y despues se usa su valor
    System.out.println("e = " + e);
    System.out.println("f = " + f);
    //2.postincremento (simbolo despues de la variable)
    var g = 5;
    var h = g++;//primero se utiliza el valor y despues se incrementa
    System.out.println("g = " + g);//teniamos pendiente un incremento
    System.out.println("h = " + h);
    
    //decremento
    //1.predecremento
    var i = 2;
    var j = --i;
    System.out.println("i = " + i);//ya esta drecrementada
    System.out.println("j = " + j);
    
    //2.postdecremento
    var k = 4;
    var l = k--;//primero se usa el valor de la variable y queda pendiente decremento
    System.out.println("k = " + k);//tenia pendiente un drecremento
    System.out.println("l = " + l);
  }
```
## Operadores Igualdad
```java
  public static void main(String args[]) {
    var a = 3;
    var b = 2;

    var c = (a == b);
    System.out.println("c = " + c);

    var d = a != b;
    System.out.println("d = " + d);

    var cadena = "Hola";
    var cadena2 = "Hola";
    var e = cadena == cadena2;//compara referencias de objetos
    System.out.println("e = " + e);

    var f = cadena.equals(cadena2);//comparamos contenido de cadenas
    System.out.println("f = " + f);
  }
```
## Operador Relacional
```java
  public static void main(String args[]) {
    var a = 3;
    var b = 2;

    var c = (a == b);
    System.out.println("c = " + c);

    var d = a != b;
    System.out.println("d = " + d);

    var cadena = "Hola";
    var cadena2 = "Hola";
    var e = cadena == cadena2;//compara referencias de objetos
    System.out.println("e = " + e);

    var f = cadena.equals(cadena2);//comparamos contenido de cadenas
    System.out.println("f = " + f);

    var g = a >= b;//mayor  que > o el mayor o igual >=
    System.out.println("g = " + g);

    if (a % 2 == 0) {
        System.out.println("Es numero par");
    } else {
        System.out.println("Es numero impar");
    }
    
    var edad = 10;
    var adulto = 18;
    if(edad >= adulto){
        System.out.println("Es un adulto");
    }
    else{
        System.out.println("Es menor de edad");
    }
  }
```
## Operadores Condicionales
```java
  public static void main(String args[]) {
    var a = 8;
    var valorMinimo = 0;
    var valorMaximo = 10;
    
    var resultado = a >= 0 && a <= 10;
    if(resultado){
        System.out.println("Dentro de rango");
    }
    else{
        System.out.println("Fuera de rango");
    }
    
    var vacaciones = false;
    var diaDescanso = true;
    
    if( vacaciones || diaDescanso){
        System.out.println("Padre puede asisitir al juego del hijo");
    }
    else{
        System.out.println("El padre esta ocupado");
    }      
  }
```
## Operadores Ternario
```java
  public static void main(String args[]) {
    var resultado = (1 > 2) ? "verdadero" : "falso";        
    System.out.println("resultado = " + resultado);
    
    var numero = 9;
    resultado = (numero % 2 == 0) ? "numero par" : "numero impar";
    System.out.println("resultado = " + resultado);
  }
```
## PrecedenciaOperadores
```java
  public static void main(String args[]) {
    var x = 5;
    var y = 10;
    var z = ++x + y--;
    System.out.println("x = " + x);
    System.out.println("y = " + y);
    System.out.println("z = " + z);
    
    var resultado = 4 + 5 * 6 / 3;//4 + ((5*6)/3)
    System.out.println("resultado = " + resultado);//14
    
    resultado = (4 + 5) * 6 / 3;
    System.out.println("resultado = " + resultado);
  }
```