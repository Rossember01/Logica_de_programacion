<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 8 


# Actividad: Ejecicios de métodos en Java
Implementar los siguientes métodos:

 - Escribe un método que reciba dos números como parámetros y devuelva el mayor de los dos.
```java
public class MayorDeDosNumeros {
    public static int obtenerMayor(int numero1, int numero2) {
        if (numero1 > numero2) {
            return numero1;
        } else {
            return numero2;
        }
    }

    public static void main(String[] args) {
        int num1 = 30;
        int num2 = 50;
        int resultado = obtenerMayor(num1, num2);
        System.out.println("El número mayor entre " + num1 + " y " + num2 + " es: " + resultado);
    }
}


```
- Escribe un método que reciba una cadena de texto como parámetro y devuelva el número de vocales que contiene.

```java
public class ContadorVocales {
    public static int contarVocales(String texto) {
        int contador = 0;
        texto = texto.toLowerCase(); 

        for (int i = 0; i < texto.length(); i++) {
            char caracter = texto.charAt(i);
            if (caracter == 'a' || caracter == 'e' || caracter == 'i' || caracter == 'o' || caracter == 'u') {
                contador++;
            }
        }

        return contador;
    }

    public static void main(String[] args) {
        String texto = "Las aerolíneas ultiman detalles para la alta demanda de fin de año y esta vez habrá un factor adicional: el aeropuerto El Dorado, de Bogotá, tendrá una operación histórica de 74 vuelos por hora, lo cual repercutirá en todas las terminales aéreas del país.";
        int numVocales = contarVocales(texto);
        System.out.println("El número de vocales en el texto es: " + numVocales);
    }
}

```

- Escribe un método que reciba una cadena de texto como parámetro y devuelva una nueva cadena con todas las letras mayúsculas en minúsculas y viceversa.

```java
public class CambiarMayusculasMinusculas {
    public static String intercambiarMayusculasMinusculas(String texto) {
        StringBuilder resultado = new StringBuilder();
        
        for (int i = 0; i < texto.length(); i++) {
            char caracter = texto.charAt(i);
            if (Character.isUpperCase(caracter)) {
                resultado.append(Character.toLowerCase(caracter));
            } else if (Character.isLowerCase(caracter)) {
                resultado.append(Character.toUpperCase(caracter));
            } else {
                resultado.append(caracter);
            }
        }
        
        return resultado.toString();
    }

    public static void main(String[] args) {
        String texto = "que ejercicios tan bravos";
        String resultado = intercambiarMayusculasMinusculas(texto);
        System.out.println("Texto con mayúsculas y minúsculas intercambiadas: " + resultado);
    }
}

```

- Escribe un método que reciba una cadena de texto como parámetro y devuelva el número de palabras que contiene.

```java
public class ContadorPalabras {
    public static int contarPalabras(String texto) {
        if (texto == null || texto.isEmpty()) {
            return 0;
        }
        
        String[] palabras = texto.split("\\s+");

               return palabras.length;
    }

    public static void main(String[] args) {
        String texto = "En la primera semana del semestre son muchas las expectativas que surgen respecto al panorama económico y político del país que acompañará los próximos meses, y a las cifras que se verán influidas con ello. ";
        int numPalabras = contarPalabras(texto);
        System.out.println("El número de palabras en el texto es: " + numPalabras);
    }
}

```

- Escribe un método que reciba una cadena de texto como parámetro y devuelva una nueva cadena con todas las palabras en orden alfabético.

```java
import java.util.Arrays;

public class OrdenarPalabras {
    public static String ordenarPalabrasAlfabeticamente(String texto) {
        if (texto == null || texto.isEmpty()) {
            return "";
        }

       
        String[] palabras = texto.split("\\s+");

        
        Arrays.sort(palabras);

        
        String resultado = String.join(" ", palabras);

        return resultado;
    }

    public static void main(String[] args) {
        String texto = "Futbol Baloncesto Volei Natación Beisbol";
        String textoOrdenado = ordenarPalabrasAlfabeticamente(texto);
        System.out.println("Palabras ordenadas alfabéticamente: " + textoOrdenado);
    }
}

```


