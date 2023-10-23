<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 10 


# Actividad: Prueba, ejecución y explicación de ejercicios de lógica de programación.

Selecciona dos ejercicios de la sesión 10, impleméntalos, ejecútalos y proporciona una explicación detallada de cada uno


# Ejercicio 1

```java
import java.util.Scanner;
import java.text.DecimalFormat;

public class Main {
    public static void main(String[] args) {
        DecimalFormat decimalFormat = new DecimalFormat("#,###");
        Scanner scanner = new Scanner(System.in);

        System.out.println("Bienvenido al calculador de CDT!");

        // Pedir al usuario que ingrese los datos del CDT
        System.out.print("Ingrese el monto del depósito: ");
        double montoDeposito = scanner.nextDouble();

        System.out.print("Ingrese la tasa de interés anual (%): ");
        double tasaInteresAnual = scanner.nextDouble();

        System.out.print("Ingrese el plazo en meses: ");
        int plazoMeses = scanner.nextInt();

        // Calcular el interés y el monto total al vencimiento
        double tasaInteresMensual = tasaInteresAnual / 12 / 100;
        double interesMensual = montoDeposito * tasaInteresMensual;
        double montoTotalVencimiento = montoDeposito + (interesMensual * plazoMeses);

        // Mostrar el resumen del CDT
        System.out.println("Resumen del CDT:");
        System.out.println("- Monto del depósito: $" + decimalFormat.format(montoDeposito));
        System.out.println("- Tasa de interés anual: " + tasaInteresAnual + "%");
        System.out.println("- Plazo en meses: " + plazoMeses);
        System.out.println("- Interés mensual: $" + interesMensual);
        System.out.println("- Monto total al vencimiento: $" + decimalFormat.format(montoTotalVencimiento));
    }
}
```

## Explicación

- Se ingresan los datos: monto del deposito, Tasa de interes anual en porcentaje y el plazo en meses.
- se realiza el caluculo de la tasa de interes mensual, el interes mensual, el monto total del vencimiento y el interes acumulado durante el plazo del CDT.



# Ejercicio 2

```java

import java.util.Scanner;

public class MovimientoParabolico {
   public static void main(String[] args) {
      Scanner input = new Scanner(System.in);
      double velocidadInicial, angulo, alturaInicial, tiempo;
      final double gravedad = 9.81;
      
      // Solicita la velocidad inicial, el ángulo y la altura inicial
      System.out.print("Ingrese la velocidad inicial en metros por segundo: ");
      velocidadInicial = input.nextDouble();
      System.out.print("Ingrese el ángulo de lanzamiento en grados: ");
      angulo = input.nextDouble();
      System.out.print("Ingrese la altura inicial en metros: ");
      alturaInicial = input.nextDouble();

      // Calcula la velocidad en los ejes x e y
      double velocidadX = velocidadInicial * Math.cos(Math.toRadians(angulo));
      double velocidadY = velocidadInicial * Math.sin(Math.toRadians(angulo));

      // Calcula el tiempo de vuelo
      tiempo = (2 * velocidadY) / gravedad;

      // Calcula la distancia recorrida
      double distancia = velocidadX * tiempo;

      // Calcula la altura máxima alcanzada
      double alturaMaxima = alturaInicial + (velocidadY * velocidadY) / (2 * gravedad);

      // Muestra los resultados en la consola
      System.out.printf("La distancia recorrida es de %.2f metros.", distancia);
      System.out.printf("La altura máxima alcanzada es de %.2f metros.", alturaMaxima);
      System.out.printf("El tiempo de vuelo es de %.2f segundos.", tiempo);
   }
}
```

# explicacion

- Se ingresan todos los datos relacionados con un objeto en movimiento, se caluculan las propiedades claves del movimiento, entre ellas, la distancia recorrida, el tiempo de vuelo y la altura maxima.



