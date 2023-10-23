<!-- No borrar o modificar -->
[Inicio](./index.md)

# Sesión 7 Rossember Restrepo - Natalia Alzate


# 1. En parejas, probar, analizar y explicar el funcionamiento de los siguientes ejemplos de Array y ArrayList.

## Ejemplo Array
```java
import java.util.Arrays;

public class EjercicioArray {

    public static void main(String[] args) {
        // Crear un array de números enteros
        int[] numeros = {5, 2, 10, 7, 1};

        // Imprimir el array original
        System.out.println("Array original: " + Arrays.toString(numeros));

        // Calcular la suma de los elementos del array
        int suma = 0;
        for (int i = 0; i < numeros.length; i++) {
            suma += numeros[i];
        }
        System.out.println("La suma de los elementos es: " + suma);

        // Encontrar el número más grande en el array
        int maximo = numeros[0];
        for (int i = 1; i < numeros.length; i++) {
            if (numeros[i] > maximo) {
                maximo = numeros[i];
            }
        }
        System.out.println("El número más grande es: " + maximo);

        // Ordenar el array en orden ascendente
        Arrays.sort(numeros);
        System.out.println("Array ordenado: " + Arrays.toString(numeros));
    }
}
```
# Explicación:

•	Se crea un array de números enteros llamado numeros.

•	Imprime el array original.

•	Calcula la suma de los elementos del array.

•	Localiza el número más grande en el array.

•	Ordena el array en orden ascendente utilizando Arrays.sort()
 

 ## Ejemplo Array list

 ```java
 
 import java.util.ArrayList; 
import java.util.Scanner;

public class AppNotas {

  public static void main(String[] args) {

    ArrayList<String> notas = new ArrayList<>();
    
    Scanner scan = new Scanner(System.in);

    while(true) {

      System.out.println("1. Agregar nota");  
      System.out.println("2. Mostrar notas");
      System.out.println("3. Salir");

      int opcion = scan.nextInt();

      if (opcion == 1) {
        agregarNota(notas, scan);  
      } else if (opcion == 2) {
        mostrarNotas(notas);
      } else {
        break;
      }

    }

  }

  public static void agregarNota(ArrayList<String> notas, Scanner scan) {
    
    System.out.println("Ingrese el titulo de la nota:");
    String titulo = scan.nextLine();
    
    System.out.println("Ingrese el contenido de la nota:");
    String contenido = scan.nextLine();
    
    notas.add(titulo + " - " + contenido);

  }

  public static void mostrarNotas(ArrayList<String> notas) {

    for(String n : notas) {
      System.out.println(n);
    }

  }

}
 
 ```
# Explicación 
•	El programa utiliza un ArrayList llamado notas para almacenarlas.

•	Permite agregar notas ingresando títulos y contenidos.

•	Permite mostrar las notas almacenadas en el ArrayList.





# 2. Crear un ejemplo de Array y otro de ArrayList para visualizar sus diferencias.

# Array

```java
public class EjemploArray {

    public static void main(String[] args) {
       int[] numeros = new int[5];

        numeros[0] = 4;
        numeros[1] = 6;
        numeros[2] = 10;
        numeros[3] = 8;
        numeros[4] = 1;

        // Imprimir el array original.
        for (int i = 0; i < numeros.length; i++) {
            System.out.println("Elemento " + i + ": " + numeros[i]);
        }
    }
}

```


# Arraylist

```java
import java.util.ArrayList;

public class EjemploArrayList {

    public static void main(String[] args) {
        ArrayList<String> nombres = new ArrayList<>();

        nombres.add("Andres");
        nombres.add("Laura");
        nombres.add("Carlos");
        nombres.add("Diego");

        for (String nombre : nombres) {
            System.out.println("Nombre: " + nombre);
        }
    }
}



```