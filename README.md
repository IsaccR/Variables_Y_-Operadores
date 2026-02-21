# Variables_Y_-Operadores

¿PARA QUÉ SE UTILIZAN LOS OPERADORES LÓGICOS EN PROGRAMACIÓN?
--
Los operadores lógicos se usan para evaluar dos o más condiciones al mismo tiempo. Sirven para que el programa pueda tomar decisiones más completas.

Por ejemplo:

&& significa que las dos condiciones deben cumplirse.

|| significa que con que una se cumpla es suficiente.

! niega una condición.

En mi programa los usé en la verificación de acceso, porque el usuario y la contraseña deben ser correctos al mismo tiempo. Si uno falla, no deja entrar.

¿POR QUÉ ES IMPORTANTE DECLARAR CORRECTAMENTE EL TIPO DE DATO DE UNA VARIABLE?
--

Es importante porque cada variable guarda un tipo diferente de información.

Por ejemplo:

int es para números enteros double para decimales boolean para verdadero o falso String para texto

Si no se usa el tipo correcto puede dar error o no funcionar bien el programa. También ayuda a que las operaciones se hagan correctamente.

JUSTIFICACIÓN TÉCNICA
--
CLASIFICACIÓN DE EDAD
--
Usé switch porque solo estaba evaluando una variable que puede tomar valores del 1 al 7.

Es más ordenado usar switch cuando son valores exactos, en vez de poner muchos if.

VERIFICACIÓN DE ACCESO
--
Usé if - else con el operador lógico &&.

Lo hice así porque necesitaba validar dos cosas al mismo tiempo: usuario y contraseña.

No usé switch porque aquí no se comparan números exactos, sino combinaciones de condiciones.*

#CODIGO:
--

package VariablesYOperadores;

importar java.util.Scanner;

clase pública Variables { Int final estática pública EDAD_MINIMA = 18;

public static void main(String[] args) {

    Scanner sc = new Scanner(System.in);


    System.out.print("Ingrese un valor entero: ");
    int valorEntero = sc.nextInt();

    System.out.print("Ingrese un valor decimal : ");
    double valorDecimal = sc.nextDouble();

    sc.nextLine(); 

    System.out.print("Ingrese un texto : ");
    String texto = sc.nextLine();

    System.out.print("Ingrese un estado true o false : ");
    boolean estado = sc.nextBoolean();

    System.out.println("Entero: " + valorEntero);
    System.out.println("Decimal: " + valorDecimal);
    System.out.println("Texto: " + texto);
    System.out.println("Estado: " + estado);

    System.out.print("Ingrese primer numero (int): ");
    int a = sc.nextInt();

    System.out.print("Ingrese segundo numero (int): ");
    int b = sc.nextInt();

    System.out.println("Suma: " + (a + b));
    System.out.println("Resta: " + (a - b));
    System.out.println("Multiplicacion: " + (a * b));

    if (b != 0) {
        System.out.println("Division: " + (a / b));
    } else {
        System.out.println("No se puede dividir entre cero");
    }

    System.out.println("La division entre enteros elimina los decimales.");


    double d1 = a;
    double d2 = b;
    System.out.println("Division con double: " + (d1 / d2));

    float f1 = a;
    float f2 = b;
    System.out.println("Division con float: " + (f1 / f2));

    short s1 = (short) a;
    short s2 = (short) b;
    if (s2 != 0) {
        System.out.println("Division con short: " + (s1 / s2));
    }

    byte by1 = (byte) a;
    byte by2 = (byte) b;
    if (by2 != 0) {
        System.out.println("Division con byte: " + (by1 / by2));
    }


    System.out.println("\n=== OPERACIONES LOGICAS ===");

    System.out.println("a > b: " + (a > b));
    System.out.println("a < b: " + (a < b));
    System.out.println("a == b: " + (a == b));

    System.out.println("AND (a > 0 && b > 0): " + (a > 0 && b > 0));
    System.out.println("OR (a > 0 || b > 0): " + (a > 0 || b > 0));


    System.out.print("Ingrese su edad: ");
    int edad = sc.nextInt();

    if (edad < 12) {
        System.out.println("Nino");
    } else if (edad <= 17) {
        System.out.println("Adolescente");
    } else if (edad <= 59) {
        System.out.println("Adulto");
    } else {
        System.out.println("Adulto mayor");
    }


    System.out.print("Ingrese un numero del 1 al 7: ");
    int dia = sc.nextInt();

    switch (dia) {
        case 1:
            System.out.println("Lunes");
            break;
        case 2:
            System.out.println("Martes");
            break;
        case 3:
            System.out.println("Miercoles");
            break;
        case 4:
            System.out.println("Jueves");
            break;
        case 5:
            System.out.println("Viernes");
            break;
        case 6:
            System.out.println("Sabado");
            break;
        case 7:
            System.out.println("Domingo");
            break;
        default:
            System.out.println("Numero invalido");
    }


    sc.nextLine(); 


    System.out.print("Usuario: ");
    String usuario = sc.nextLine();

    System.out.print("Contrasena: ");
    String contrasena = sc.nextLine();

    if (usuario.equals("david") && contrasena.equals("2009")) {
        System.out.println("Acceso concedido");
    } else if (usuario.equals("admin")) {
        System.out.println("Contrasena incorrecta");
    } else {
        System.out.println("Usuario no registrado");
    }

    sc.close();
}
}

