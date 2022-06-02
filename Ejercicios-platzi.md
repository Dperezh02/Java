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