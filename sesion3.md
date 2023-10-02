<!-- No borrar o modificar -->
[Inicio](./index.md)

# Sesión 3 


Actividad 3: Ejercicios de operaciones básicas en Java.


 - Suma y multiplicación: Escribe un programa que solicite al usuario dos números enteros y luego imprima la suma y multiplicación de esos números.

```java

 import java.util.Scanner;

public class SumaMultiplicacion {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        System.out.println("Ingrese el primer numero entero: ");
        int numero1 = scanner.nextInt();
        
        System.out.println("Ingrese el segundo numero entero: ");
        int numero2 = scanner.nextInt();
        
        int suma = numero1 + numero2;
        int multiplicacion = numero1 * numero2;

        
        System.out.println("La suma de los numeros es: " + suma);
        System.out.println("La multiplicacion de los numeros es:" + multiplicacion);
        
        scanner.close();
        
        
                

    }
}

```

 - Resta y división: Escribe un programa que tome dos números enteros ingresados por el usuario y calcule la resta y división de esos números.

 ```java
 import java.util.Scanner;

public class RestaDivision {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
    
    System.out.print("Ingrese el primer numero entero: ");
    int numero1 = scanner.nextInt();
    
    System.out.print("Ingrese el segundo numero entero: ");
    int numero2 = scanner.nextInt();
    
    int resta = numero1 - numero2;
    int division = numero1 / numero2;
    
    System.out.println("La resta de los numeros es: " + resta);
    System.out.println("La division de los numeros es: " + division);
 
 
 ```

 - Operaciones combinadas: Escribe un programa que solicite al usuario tres números enteros y realice las siguientes operaciones: suma de los tres números, multiplicación del primer número por el segundo y división del resultado entre el tercer número.

 ```java
 import java.util.Scanner;

public class OperacionesCombinadas {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.println("Ingrese el primer numero entero: ");
        int numero1 = scanner.nextInt();

        System.out.println("Ingrese el segundo numero entero: ");
        int numero2 = scanner.nextInt();

        System.out.println("Ingrese el tercer numero entero: ");
        int numero3 = scanner.nextInt();

        int suma = numero1 + numero2 + numero3;
        float multiplicacion = numero1 * numero2;
        float division = (numero1 * numero2) / numero3;

System.out.println("La suma de los numeros es: " + suma);
System.out.println("La multiplicacion de los numeros es: " + multiplicacion);
System.out.println("La division de los numeros es: " + division);


    }
}

 
 ```

 - Operaciones con decimales: Escribe un programa que solicite al usuario dos números decimales y realice las siguientes operaciones: suma, resta, multiplicación y división.

```java
import java.util.Scanner;

public class Decimales {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.println("Ingrese el primer numero: ");
        float numero1 = scanner.nextFloat();

        System.out.println("Ingrese el segundo numero: ");
        float numero2 = scanner.nextFloat();

        float suma = numero1 + numero2;
        float resta = numero1 - numero2;
        float multiplicacion = numero1 * numero2;
        float division = numero1 / numero2;

        System.out.println("La suma de los numeros es: " + suma);
        System.out.println("La resta de los numeros es: " + resta);
        System.out.println("La multiplicacion de los numeros es:" + multiplicacion);
        System.out.println("La division de los numeros es:" + division);

    }
}

```

 - Incremento y decremento: Escribe un programa que declare una variable entera y la inicialice con un valor. Luego, incrementa su valor en 1 y muestra el resultado. Después, decrementa su valor en 1 y muestra el resultado nuevamente.

 ```java
 public class IncrementoDecremento {
    public static void main(String[] args) {
        int a = 15;

        a++;
        System.out.println(a);

        a--;
        System.out.println(a);

    }
}
 
 ```

 - Operador de asignación compuesta: Escribe un programa que declare una variable entera y la inicialice con un valor. Utiliza el operador de asignación compuesta para sumar 5 a la variable y luego mostrar su valor.

 ```java
 public class AsignacionCompuesto {
    public static void main(String[] args){
        int x = 12;

        x += 5;
        System.out.println("El valor de la variable despues de sumar 5 es: " + x);
    }
}

 
 ```

 - Operadores lógicos: Escribe un programa que tome dos valores booleanos ingresados por el usuario y muestre el resultado de las operaciones lógicas AND, OR y NOT entre esos valores.

 ```java
 public class OperadoresLogicos {
    public static void main(String[] args){
int edad = 18;

boolean esEstudiante = true;
boolean esTrabajador = false;
boolean esUniversitario = true;

boolean resultado1 = (edad <= 18)  && esEstudiante;
boolean resultado2 = esTrabajador || esEstudiante;
boolean resultado3 = !esTrabajador;

System.out.println("El resultado1 es: " + resultado1);
System.out.println("El resultado2 es: " + resultado2);
System.out.println("El resultado3 es: " + resultado3);


    }

}
 
 ```

 - Operador ternario: Escribe un programa que tome un número entero ingresado por el usuario y utilice el operador ternario para determinar si el número es positivo o negativo. Luego, muestra el resultado en la salida.

 ```java
 import java.util.Scanner;

public class OperadorTernario {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);



        int x = 20;

        if (x > 20){
            System.out.println("x es mayor que 20");

        }else{ 
            System.out.println("x es menor que 20");
        }
}
}

 
 ```


 