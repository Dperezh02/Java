# Abstracción
Basicamente analiza un objeto para abstraer su composición y entonces generar un molde, cuando nos referimos a abstracción hablamos de analizar ese objeto, cuales son sus comportamientos y propiedades para luego hacer muchos otros objetos que tengan las mismas caracteristicas para así reutilizar el codigo lo más posible 

Por ejemplo:
```java
Nombre de la clase: Person
Atributos: Name, Age
Operaciones: Walk()
```
# Herencia 
# Encapsulamiento
Existe algo llamado **Modificadores de acceso** los cual nos ayudaran a  limitar desde dónde podemos leer o modificar atributos especiales de nuestras clases. Podemos definir qué variables se pueden leer/editar por fuera de las clases donde fueron creadas. 
```java
________________________________________________
Modificador | Clase | Package | Subclase | Otros
________________________________________________
public      |   √   |    √    |    √     |   √
________________________________________________
protected   |   √   |    √    |    √     |   X
________________________________________________
default     |   √   |    √    |    X     |   X
________________________________________________
private     |   √   |    X    |    X     |   X
________________________________________________
```
### Getters y Setters
Los **Getters y Setters** nos permiten leer y escribir (respectivamente) los valores de nuestras variables privadas desde fuera de la clase donde fueron creadas. Con los Getters obtenemos los datos de las variables y con los Setters asignamos o cambiamos su valor.

![I1]()

Por ejemplo: 
```java
public class Patient {
  private String name;

  public String getName() {
    return "Patient name is " + this.name;
  }

  public void setName(String newName) {
    this.name = newName;
  }
}
```
# Polimorfismo 