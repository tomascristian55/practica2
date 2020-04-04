# practica2
package javaapplication5;
import java.util.Scanner;

public class JavaApplication5 {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        // TODO code application logic here
        
        Scanner Leer = new Scanner(System.in);
        int rand = 0, opt, tope = 0, n = 27;
        char[] pila = new char[n];
        System.out.println("elija una opcion ");
        do {
            System.out.println("1.llenar \n");
            System.out.println("2.agregar \n");
            System.out.println("3.mostrar \n");
            System.out.println("4.eliminar \n");
            System.out.println("5.ordenar \n");
            System.out.println("6.buscar\n");
            System.out.println("7.salir\n");
            opt = Leer.nextInt();

            switch (opt) {
                case 1:
                    System.out.println("llenar");
                    String[] abc = {"a", "b", "c", "d", "e", "f", "g", "h",
                        "i", "j", "k", "l", "m", "n", "ñ", "o",
                        "p", "q", "r", "s", "t", "u", "v", "w", "x", "y", "z"};
                    for (int i = 0; i < n; i++) {
                        System.out.print(abc[i] + " ");

                    }
                    break;
                case 2:

                    System.out.println("---------agregar datos: ------------\n");
                    if (tope < n) {

                        System.out.println("digite un caracter");
                        pila[tope] = Leer.next().charAt(0);
                        tope++;
                    } else {
                        System.out.println("pila llena");

                    }
                    break;

                case 3:
                    System.out.println("LOS DATOS SON: ");
                    if (tope > 0) {

                        for (int i = 0; i < n; i++) {
                            rand = (int) Math.round(Math.random() * 25);
                            System.out.println(" " + pila[rand]);

                        }
                    } else {
                        System.out.println("pila vacia ");

                    }

                    break;

                case 4:

                    tope--;

                    break;
                case 5:
                    System.out.println("ordenamiento de z--a: ");
                      for (int i = tope - 1; i >= 0; i--) {
                        System.out.println("  " +  pila[i]);
                    }
                    break;
                case 6:
                    System.out.println("buscar pocisiones: ");
                    for (int i = 0; i < tope; i++) {
                        System.out.println("El Valor" + pila[i] + " Ocupa el : " + i + " Lugar");
                    }
                    break;
            }
        } while (opt != 7);
    }
}
