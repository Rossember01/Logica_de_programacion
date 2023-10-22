<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 9 
```java

import java.util.Scanner;

public class Resistencia {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        String[] colores = { "negro", "marrón", "rojo", "naranja", "amarillo", "verde", "azul", "púrpura", "gris",
                "blanco" };
        double[] multiplicador = { 1, 10, 100, 1000, 10000, 100000, 1000000, 0.1, 0.01 };

        System.out.println("Selecciona el color de la primera banda:");
        for (int i = 0; i < colores.length; i++) {
            System.out.println((i + 1) + ". " + colores[i]);
        }
        int banda1 = scanner.nextInt() - 1;

        System.out.println("Selecciona el color de la segunda banda:");
        for (int i = 0; i < colores.length; i++) {
            System.out.println((i + 1) + ". " + colores[i]);
        }
        int banda2 = scanner.nextInt() - 1;

        String c1 = String.valueOf(banda1);
        String c2 = String.valueOf(banda2);

        String conc = c1 + c2;

        int resultado = Integer.parseInt(conc);

        double multi = 1;

        System.out.println("Selecciona el color de la tercera banda (Multiplicador):");
        System.out.println("1. Negro (*1)");
        System.out.println("2. Marrón (*10)");
        System.out.println("3. Rojo (*100)");
        System.out.println("4. Naranja (*1000)");
        System.out.println("5. Amarillo (*10000)");
        System.out.println("6. Verde (*100000)");
        System.out.println("7. Azul (*1000000)");
        System.out.println("8. Púrpura (/10)");
        System.out.println("9. Gris (/100)");
        System.out.println("10. Blanco");
        double seleccionmultiplicador = scanner.nextDouble();

        System.out.println("Selecciona el color de la cuarta banda (tolerancia):");
        System.out.println("1. Marrón (1%)");
        System.out.println("2. Rojo (2%)");
        System.out.println("3. Oro (5%)");
        System.out.println("4. Plata (10%)");
        int seleccionTolerancia = scanner.nextInt();

        double tolerancia = 0;
        switch (seleccionTolerancia) {
            case 1:
                tolerancia = 1;
                break;
            case 2:
                tolerancia = 2;
                break;
            case 3:
                tolerancia = 5;
                break;
            case 4:
                tolerancia = 10;
                break;
        }

        if (seleccionmultiplicador >= 1 && seleccionmultiplicador <= 9) {
            multi = resultado * multiplicador[(int) seleccionmultiplicador - 1];

            if (seleccionmultiplicador == 8 || seleccionmultiplicador == 9) {
                System.out.println("El valor de la resistencia es: " + multi + "Ohms");
            } else if (multi >= 1000) {
                int valorEnKiloOhms = (int) (multi / 1000);
                System.out.println("El valor de la resistencia es: " + valorEnKiloOhms + "kOhms");
            } else {
                System.out.println("El valor de la resistencia es: " + (int) multi + "Ohms");
            }
        }

        System.out.println("Tolerancia: " + tolerancia + "%");

        scanner.close();
    }
}
```







