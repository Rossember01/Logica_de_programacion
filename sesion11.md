<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 11 


# Actividad: Ejercicios de Lógica de Programación

- Basándose en el algoritmo 1 de la sesión 11, aplicar la siguiente variante: Dado un conjunto de números enteros, se debe determinar si existe algún número que aparezca más de una vez. Si es así, se deben imprimir todos los números que aparezcan más de una vez.


```java
import java.util.HashSet;

public class EjercicioVariante {

    public static void main(String[] args) {
        
        int[] numeros = {1, 2, 3, 4, 5, 2, 4, 6, 7, 7};

        
        HashSet<Integer> numerosRepetidos = new HashSet<>();
        HashSet<Integer> numerosVistos = new HashSet<>();

        for (int numero : numeros) {
            if (numerosVistos.contains(numero)) {
                
                numerosRepetidos.add(numero);
            } else {
                
                numerosVistos.add(numero);
            }
        }

        
        if (!numerosRepetidos.isEmpty()) {
            System.out.println("Los números repetidos son: " + numerosRepetidos);
        } else {
            
            System.out.println("No hay ningún número repetido");
        }
    }
}

```

- Desarrollar un algoritmo que realice la conversión de binario a decimal.

```java
public class BinarioADecimal {
    public static int convertirBinarioADecimal(String numeroBinario) {
        int decimal = 0;
        int longitud = numeroBinario.length();

        for (int i = 0; i < longitud; i++) {
            char digito = numeroBinario.charAt(i);
            int valor = Character.getNumericValue(digito);
            int potencia = longitud - i - 1;
            decimal += valor * Math.pow(2, potencia);
        }

        return decimal;
    }

    public static void main(String[] args) {
        String binario = "1101"; 
        int decimal = convertirBinarioADecimal(binario);
        System.out.println("El valor decimal de " + binario + " es: " + decimal);
    }
}

```



