<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 5 



# Actividad 5: Ejercicios de bucles


Resolver los siguientes ejercicios:

## Ejercicios - while

 - Pedir al usuario que ingrese un número y mostrar su tabla de multiplicar hasta el número 10.

```java

import java.util.Scanner;

public class TabladeMultiplicar {
    public static void main(String[] args){

        Scanner scanner = new Scanner(System.in);
        System.out.println("Ingrese un numero: ");
        int numero = scanner.nextInt();

int x = 1;
while(x <=10){
    int resultado = numero * x;
    System.out.println(numero + "x" + x + "=" + resultado);
    x++;
}

scanner.close();
        
        }



    }
```

 - Pedir al usuario que ingrese una cadena de caracteres y contar la cantidad de caracteres que son números.

 ```java
 import java.util.Scanner;

public class CadenadeCaracteres {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Ingrese una cadena de caracteres: ");
        String cadena = sc.nextLine();

        int i = 0;
        int contadorCaracteres = 0;

        while (i < cadena.length()) {
            char caracter = cadena.charAt(i);
            if (caracter == '1' || caracter == '2' || caracter == '3' || caracter == '4' || caracter == '5' ||
                caracter == '6' || caracter == '7' || caracter == '8' || caracter == '9' || caracter == '0') {
                contadorCaracteres++;
            }
            i++;
        }

        System.out.println("La cadena ingresada contiene " + contadorCaracteres + " numeros.");
    }
    }
 
 ```
## Ejercicios - do while

 - Escribe un programa en Java que imprima los números del 1 al 100, pero que se detenga si el usuario introduce un número negativo.

 ```java
 import java.util.Scanner;

public class DoWhile1 {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int numero;

        do {
            System.out.println("introduce un numero (o un numero negativo para detenerse): ");
            numero = scanner.nextInt();

            if (numero >= 0) {
                for (int i = 1; i <= 100; i++) {
                    System.out.println(i);
                }
            } else {
                System.out.println("programa detenido");
            }
            
        } while (numero >= 0);

        scanner.close();
    }

}

 
 ```

 - Escribe un programa en Java que pida al usuario un número entero e imprima la tabla de multiplicar de ese número, pero que se detenga si el usuario introduce el número 0.

 ```java
 import java.util.Scanner;

public class DoWhile2 {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int x;
        do {
            System.out.println("ingrese un numero (o ingresa 0 para salir): ");
            x = sc.nextInt();

            if (x != 0) {
                System.out.println("Tabla de multiplicar de" + x + ":");
                for (int i = 1; i <= 10; i++) {
                    System.out.println(x + "*" + i + "=" + (x * i));
                }
            } else {
                System.out.println("Programa detenido");
            }

        } while (x != 0);

        sc.close();
    }
}
 
 ```
## Ejercicios - for


 - Imprimir los números impares del 1 al 50.

 ```java
 public class Impares {

    public static void main(String[] args) {
        for (int i = 1; i <= 50; i += 2) {
            System.out.println(i);
        }
    }

    
}

 
 ```
 - Imprimir los números primos del 1 al 100.

 ```java
 
 
 ```








