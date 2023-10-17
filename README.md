![Logo Java](https://seeklogo.com/images/J/java-logo-7833D1D21A-seeklogo.com.png))

# Datos de Apo1 - Apo2

Datos relacionados a programación desde primer semestre hasta el actual.

## Empezando

### Metodos de Java

/**
 * Clase que representa un rango de edad para la encuesta
 * @class RangoEdad
 */
public class RangoEdad {
/**
 * Atributos
 */
	
	/**
	 * Cantidad de opiniones hechas por solteros en este rango de edad
	 */
	private int numeroSolteros;
	/**
	 * Cantidad de opiniones hechas por casados en este rango de edad
	 */
	private int numeroCasados;
	
	
	/**
	 * Suma de las opiniones hechas por gente soltera en este rango de edad
	 */
	private int totalOpinionSolteros;
	/**
	 * Suma de las opiniones hechas por gente casada en este rango de edad
	 */
	private int totalOpinionCasados;
	
	
	/**
	 * Edad mínima para este rango de edad de la población
	 */
	private int edadMinima;
	
	/**
	 * Edad máxima para este rango de edad de la población
	 */
	private int edadMaxima;
	
	/**
	 * @method RangoEdad
	 * Construye el rango de encuestas.
	 * La edad mínima y máxima fueron inicializados con los valores de los parámetros,
	 * estos son inicializados en 0
	 * @param pEdadMinima Edad mínima para este rango.
	 * @param pEdadMaxima Edad máxima para este rango.
	 */
	public RangoEdad(int pEdadMinima, int pEdadMaxima) {
		this.numeroCasados=0;
		this.numeroSolteros=0;
		this.totalOpinionCasados=0;
		this.totalOpinionSolteros=0;
		this.edadMaxima=pEdadMaxima;
		this.edadMinima=pEdadMinima;
	}

	public double DarPromedio() {
		return (double) DarTotalOpiniones()/DarNumeroOpiniones();
	}
	
	/**
	 * Retorna la edad minima de este rango de edad
	 * @return edad mínima de este rango de edad
	 */
	public int DarEdadMinima() {
		return this.edadMinima;
	}
	
	/**
	 * Retorna la edad máxima de este rango de edad
	 * @return edad máxima de este rango de edad
	 */
	public int DarEdadMaxima() {
		return this.edadMaxima;
	}
	
	/**
	 * Retorna el promedio de las opiniones de la gente en este rango de edad
	 * @return Promedio de opinion del curso de la encuesta en el rango de edad de la
	 * clase considerando solo los casados.
	 */
	public double DarPromedioCasados() {
		return (double) this.totalOpinionCasados/this.numeroCasados;
	}
	
	/**
	 * Retorna el promedio de las opiniones de la gente en este rango de edad
	 * @return Promedio de opinion del curso de la encuesta en el rango de edad de la
	 * clase considerando solo los solteros.
	 */
	public double DarPromedioSolteros() {
		return (double) this.totalOpinionSolteros/this.numeroSolteros;
	}
	
	/**
	 * Retorna la suma de opiniones hechas para este rango
	 * @return DarTotalOpiniones
	 * Da el total de opiniones del curso
	 */
	public int DarTotalOpiniones() {
		return this.totalOpinionCasados+this.totalOpinionSolteros;
	}
	
	/**
	 * Retorna el número de opiniones hechas para este rango
	 * @return DarNumerosOpiniones
	 * Cantidad total de opiniones
	 */
	public int DarNumeroOpiniones() {
		return numeroCasados+numeroSolteros;
	}
	
	/**
	 * Retorna el numero de personas casadasque respondieron la encuesta en este rango
	 * de edad
	 * @return Numero de personas casadas
	 */
	public int DarNumeroCasados() {
		return this.numeroCasados;
	}
	
	/**
	 * Retorna el numero de personas casadasque respondieron la encuesta en este rango
	 * de edad
	 * @return Numero de personas solteras
	 */
	public int DarNumeroSolteros() {
		return this.numeroSolteros;
	}
	
	/**
	 * Retorna el numero total de opiniones de los encuestados casados en este rango de edad
	 * @return Numero total de opiniones de los casados
	 */
	public int DarTotalOpinionesCasados() {
		return this.totalOpinionCasados;
	}
	
	/**
	 * Retorna el numero total de opiniones de los encuestados casados en este rango de edad
	 * @return Numero total de opiniones de los solteros
	 */
	public int DarTotalOpinionesSolteros() {
		return this.totalOpinionSolteros;
	}
	
	/**
	 * Retorna una cadena de texto con la edad mínima y edad máxima
	 * @return Cadena de caracteres con el rango de edad
	 */
	public String DarRangoEdad() {
		return "El rango de edad es: "+this.edadMinima+" a "+(this.edadMaxima-1); 
	}
	
	/**
	 * Agrega una opinion de una persona soltera para este rango de edad.  <br>
	 * Post: se agrega una nueva opinion
	 * @param pOpinion  Opinión del encuestado
	 * pOpinion >= 0 && pOpinion < 11. 
	 */
	public void AgregarOpinionSoltero(int pOpinion) {
		// this.numeroSolteros = this.numeroSolteros+1;
		this.numeroSolteros += 1;
		// this.totalOpinionSolteros = this.totalOpinionSolteros+1;
		this.totalOpinionSolteros += pOpinion;
	}
	
	/**
	 * Agrega una opinion de una persona casada para este rango de edad.  <br>
	 * Post: se agrega una nueva opinion
	 * @param pOpinion  Opinión del encuestado
	 * pOpinion >= 0 && pOpinion < 11. 
	 */
	public void AgregarOpinionCasado(int pOpinion) {
		// this.numeroCasados = this.numeroCasados+1;
		this.numeroCasados += 1;
		// this.totalOpinionCasados = this.totalOpinionCasados+1;
		this.totalOpinionCasados += pOpinion;
	}
}

public class Condicional_for {

	public static void main(String[] args) {
		// TODO Auto-generated method stub

for (int i=0; i<=10; i++) {
	int result= 8*i;
	System.out.print("8x" +i+ "=" + result + "\n");
	
}
	}
}

import javax.swing.JOptionPane;

public class CalculadoraSimple {
    public static void main(String[] args) {
        String input1 = JOptionPane.showInputDialog("Ingresa el primer número:");
        double numero1 = Double.parseDouble(input1);

        String input2 = JOptionPane.showInputDialog("Ingresa el segundo número:");
        double numero2 = Double.parseDouble(input2);

        double resultado = numero1 + numero2;

        JOptionPane.showMessageDialog(null, "La suma es: " + resultado);
    }
} 

import javax.swing.JOptionPane;

public class TablaDeMultiplicar {
    public static void main(String[] args) {
        String input = JOptionPane.showInputDialog("Ingresa un número para obtener su tabla de multiplicar:");
        int numero = Integer.parseInt(input);

        String tabla = generarTablaDeMultiplicar(numero);

        JOptionPane.showMessageDialog(null, tabla, "Tabla de Multiplicar de " + numero, JOptionPane.INFORMATION_MESSAGE);
    }

    public static String generarTablaDeMultiplicar(int numero) {
        StringBuilder tabla = new StringBuilder();
        for (int i = 1; i <= 10; i++) {
            int resultado = numero * i;
            tabla.append(numero).append(" x ").append(i).append(" = ").append(resultado).append("\n");
        }
        return tabla.toString();
    }
}

public class Consecutivos {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		
		int x1 = 0;
		int x2 = 1;
		int x3 = 20;
		
		for (int i=0; i<=x3; i++) {
		int secuencia = x1 + x2;
		
		System.out.print("La secuencia es:" + secuencia + "\n");
	    
	    x1 = x2;
	    x2 = secuencia;
	}
}
}
import java.util.Scanner;

public class PromedioNotas {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        System.out.println("Ingresa la primera nota: ");
        double nota1 = scanner.nextDouble();
        
        System.out.println("Ingresa la segunda nota: ");
        double nota2 = scanner.nextDouble();
        
        System.out.println("Ingresa la tercera nota: ");
        double nota3 = scanner.nextDouble();
        
        // Calcula el promedio
        double promedio = (nota1 + nota2 + nota3) / 3.0;
        
        System.out.println("El promedio de las tres notas es: " + promedio);
        
        scanner.close(); // Cerrar el Scanner al finalizar
    }
}

public class AnalisisNumeros {
    public static void main(String[] args) {
        int cantidadNumeros = 5;
        int[] numeros = new int[cantidadNumeros];

        // Solicitar al usuario que ingrese 5 números
        for (int i = 0; i < cantidadNumeros; i++) {
            String input = JOptionPane.showInputDialog("Ingresa el número #" + (i + 1) + ":");
            numeros[i] = Integer.parseInt(input);
        }

        // Encontrar el número más grande y el número más pequeño
        int maximo = numeros[0];
        int minimo = numeros[0];
        int suma = 0;

        for (int i = 0; i < cantidadNumeros; i++) {
            suma += numeros[i];
            if (numeros[i] > maximo) {
                maximo = numeros[i];
            }
            if (numeros[i] < minimo) {
                minimo = numeros[i];
            }
        }

        // Calcular el promedio
        double promedio = (double) suma / cantidadNumeros;

        // Mostrar los resultados en un cuadro de diálogo
        String resultado = "Número más grande: " + maximo + "\n" +
                           "Número más pequeño: " + minimo + "\n" +
                           "Promedio: " + promedio;
        JOptionPane.showMessageDialog(null, resultado);
	}	
}

public class Menu_Parcial_C1 {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Scanner sc = new Scanner (System.in);
			int opcion=0;
while(opcion!=3) {
		System.out.print("Bienvenido al menú\n");
		
		System.out.print("Selecciona la opción a realizar \n");
		System.out.print("Opción 1: Pedir números hasta que sea 0 y sumarlos \n");
		System.out.print("Opción 2: Pedir 10 números y promediarlos \n");
		System.out.print("Opción 3: Salir \n");
		opcion=sc.nextInt();
	switch (opcion) {
	case 1:
		System.out.print("Ingresa diferentes números, para sumarlos digita 0: \n");
		int numeros = 1;
		int suma= 0;
	while (numeros !=0) {
		System.out.print("Ingresa un número: \n");
		numeros=sc.nextInt();
		suma=suma+numeros;
		}
	System.out.print("El total de la suma es:" + suma +"\n");
	break;
	case 2:
		System.out.print("Ingresa 10 números para promediarlos: \n");
		double promedio=0;
		for (int i=0; i<10; i++) {
		System.out.print("Ingresa un número: \n");
		double nume=0;
		nume=sc.nextInt();
		promedio=promedio+nume;
		}
		System.out.print("El promedio es:" + promedio/10 +"\n");
	break;
	default: 
		System.out.print("Gracias por usar este menú \n");
	}
	}
	}
}

import javax.swing.JOptionPane;

public class PuntuacionPartidos {
    public static void main(String[] args) {
        String ganadosInput = JOptionPane.showInputDialog("Partidos ganados:");
        int ganados = Integer.parseInt(ganadosInput);

        String empatadosInput = JOptionPane.showInputDialog("Partidos empatados:");
        int empatados = Integer.parseInt(empatadosInput);

        String perdidosInput = JOptionPane.showInputDialog("Partidos perdidos:");
        int perdidos = Integer.parseInt(perdidosInput);

        int puntosGanados = ganados * 5;
        int puntosEmpatados = empatados * 3;
        int puntosPerdidos = perdidos * 2;

        int totalPuntos = puntosGanados + puntosEmpatados - puntosPerdidos;

        String resultado = "Puntos ganados: " + puntosGanados + "\n"
                + "Puntos empatados: " + puntosEmpatados + "\n"
                + "Puntos perdidos: " + puntosPerdidos + "\n"
                + "Puntuación total: " + totalPuntos;

        JOptionPane.showMessageDialog(null, resultado, "Puntuación de Partidos", JOptionPane.INFORMATION_MESSAGE);
    }
}

import javax.swing.JOptionPane;

public class ProductoNumeros {
    public static void main(String[] args) {
        String input1 = JOptionPane.showInputDialog("Ingresa el primer número:");
        double numero1 = Double.parseDouble(input1);

        String input2 = JOptionPane.showInputDialog("Ingresa el segundo número:");
        double numero2 = Double.parseDouble(input2);

        double producto = numero1 * numero2;

        JOptionPane.showMessageDialog(null, "El producto de los números es: " + producto);
    }
}
****************************************************************
Codigo de Factorial Con Try and Catch
	public static void main(String[] args) {
		// TODO Auto-generated method stub

	int opcion = 0;	
	
while(opcion!=2) {
try {
	opcion=Integer.parseInt(JOptionPane.showInputDialog(null, "Selecciona la opción a realizar \n Opción 1: Factorial \n Opción 2: Salir \n","Bienvenido al menú",1));
}
catch(NumberFormatException e){
	JOptionPane.showMessageDialog(null, "Elige entre 1 y 2\n", null, 1);
}
	switch (opcion) {
	case 1:
	try {
	int x=Integer.parseInt(JOptionPane.showInputDialog(null, "Escribe un número: \n"));
	if (x>=0) {
		int x1=calcularFactorial(x);
		
				JOptionPane.showMessageDialog(null, "El valor factorial de "+ x + " es: "+ x1 + "\n", null, 1);
			}
			else {
				JOptionPane.showMessageDialog(null, "El valor factorial de "+ x + " no es posible de calcular \n", null, 1);
			}
			}catch (NumberFormatException e) {
				JOptionPane.showMessageDialog(null, "Ingresa un número entero", null, 0);
			}
			break;
			case 2:
				JOptionPane.showMessageDialog(null, "Gracias por usar este menú \n", null, 1);
			break;
			default: 
			JOptionPane.showMessageDialog(null, "Opción invalida \n", null, 0);
			}
		}

	}
	public static int calcularFactorial (int x) {
		int factorial = 1;
		for (int i = 1; i <= x; i++) {
	    factorial *= i;
	    }
		return factorial;
	}
}
********************************************************************
Codigo de If and Else
public class Taller {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Scanner sc= new Scanner (System.in);
		byte dia=sc.nextByte();
		if (dia==1) {
			System.out.print("El día es Lunes");
			}
		else if (dia==2) {
			System.out.print("El día es Martes");
			}
		else if (dia==3) {
			System.out.print("El día es Miercoles");
			}
		else if (dia==4) {
			System.out.print("El día es Jueves");
			}
		else if (dia==5) {
			System.out.print("El día es Viernes");
			}
		else if (dia==6) {
			System.out.print("El día es Sábado");
			}
		else if (dia==7) {
			System.out.print("El día es Domingo");
			}
		else if (dia>7){
			System.out.print("El día no existe");
			}
	}

}
*********************************************************
Tabla con While
public class Tabla {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		
		System.out.print("¿Necesitas la tabla del número? \n");
		Scanner sc = new Scanner (System.in);
		int numero=sc.nextInt();
		int x=1;
		
while(x <= 10) {
	int resultado= numero*x;
	System.out.print(numero + " x " + x + " = " + resultado + "\n");
	x++;
}
}
}
*********************************************************************
Conversor De Pesos a Dolares
public class Conversor {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		System.out.print("Ingresa el valor en pesos a convertir en dolares:");
		Scanner sc= new Scanner (System.in);
		double pesos=sc.nextDouble();
		
		double dolares=0;
		dolares=(pesos/4150);
		System.out.print("El valor en dolares es: "+dolares);
	}
}
************************************************************************
Condicional es par o no
public class Condicional {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Scanner sc= new Scanner (System.in);
		double numero=sc.nextDouble();
		if (numero==0) {
			System.out.print("El número es 0");
			}
		else if (numero%2==0) {
		System.out.print("Es par");
		}
		else {
		System.out.print("Es impar");
		}
	}
}
********************************************************************
Uso del JOp
public class Main {
	public static void main(String[]args)
	{
		String mensaje = JOptionPane.showInputDialog(null, "Introduce tu nombre");
		// Para recibir números se tiene que tranformar el tipo de variable a entero.
		// 
		int suma=0;
		int suma1=Integer.parseInt(JOptionPane.showInputDialog(null, "Ingresa el primer número"));
		JOptionPane.showMessageDialog(null, mensaje,"Se acabo tu tiempo", 0);
	}
}
**************************************************************************
Uso de las Funciones
public class Funciones {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		
		double x=Integer.parseInt(JOptionPane.showInputDialog(null, "Ingresa el primer número"));
		double y=Integer.parseInt(JOptionPane.showInputDialog(null, "Ingresa el segundo número"));
		
		double x1=suma(x,y);
		double x2=resta(x,y);
		double x3=multiplicacion(x,y);
		double x4=division(x,y);
		JOptionPane.showMessageDialog(null,"Suma es igual a: "+x1+ "\n","Resultado",1);
		JOptionPane.showMessageDialog(null,"Resta es igual a: "+x2+ "\n","Resultado",1);
		JOptionPane.showMessageDialog(null,"Multiplicación es igual a: "+x3+ "\n","Resultado",1);
		JOptionPane.showMessageDialog(null,"División es igual a: "+x4+ "\n","Resultado",1);
	}
	
	public static double suma (double a, double b) {
			return a+b;
	}
	public static double resta (double a, double b) {
			return a-b;
	}
	public static double multiplicacion (double a, double b) {
		return a*b;
	}
	public static double division (double a, double b) {
		return a/b;
	}
}
**************************************************************************
Contenedoras en Java
public class Contenedora1 {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
	int totalNotas= Integer.parseInt(JOptionPane.showInputDialog(null, "Ingresa el número de notas: "));
	double notas [] = new double [totalNotas];
	
	JOptionPane.showMessageDialog(null, "Ingresa tus notas");
	
	notas[0]=Double.parseDouble(JOptionPane.showInputDialog(null, "Ingresa la nota 1: "));
	notas[1]=Double.parseDouble(JOptionPane.showInputDialog(null, "Ingresa la nota 2: "));
	notas[2]=Double.parseDouble(JOptionPane.showInputDialog(null, "Ingresa la nota 3: "));
	
	double suma=0;
	double promedio;
	suma=notas[0]+notas[1]+notas[2];
	promedio=suma/3;
	
	if (promedio<=29)
		JOptionPane.showMessageDialog(null, "Repobraste, tu promedio es: "+promedio,"Promedio", 0);
	else
		JOptionPane.showMessageDialog(null, "Aprobaste, tu promedio es: "+promedio,"Promedio", 15);
	}
}
***************************************************************************
Menu Con While
public static void main(String[] args) {
		// TODO Auto-generated method stub

	Scanner sc = new Scanner (System.in);
		byte opcion=0;
		
while(opcion!=6) {
	
	System.out.print("Ingresa tu función a realizar:\n Opción 1: Conversor de pesos\n Opción 2: Promedio de notas \n Opción 3: Clasificación de equipos \n Opción 4: Número Par o Impar\n");
	opcion=sc.nextByte();
switch (opcion) {
case 1:
	System.out.print("Ingresa el valor en pesos a convertir en dolares: \n");
	Scanner sc1= new Scanner (System.in);
	double pesos=sc1.nextDouble();
	double dolares=0;
	dolares=(pesos/4150);
	System.out.print("El valor en dolares es: "+dolares);
break;

case 2:
	System.out.print("Ingrese la nota 1 \n");
	Scanner sc2= new Scanner (System.in);
	float nota1=sc2.nextFloat();
	System.out.print("Ingrese la nota 2 \n");
	Scanner sc3= new Scanner (System.in);
	float nota2=sc3.nextFloat();
	System.out.print("Ingrese la nota 3 \n");
	Scanner sc4= new Scanner (System.in);
	float nota3=sc4.nextFloat();
	double promedio=0;
	promedio=(nota1+nota2+nota3)/3;
	System.out.print("El promedio del estudiante es"+ promedio);
break;
	
case 3:
	System.out.print("Ingresa el número de partidos ganados \n");
	Scanner sc5= new Scanner (System.in);
	float pGanados=sc5.nextFloat();
	System.out.print("Ingresa el número de partidos empatados \n");
	Scanner sc6= new Scanner (System.in);
	float pEmpatados=sc6.nextFloat();
	int totalPuntos=0;
	totalPuntos=(int) ((pGanados*3)+(pEmpatados*1));
	System.out.print("El total de puntos del equipo son "+ totalPuntos);
break;

case 4:
	System.out.print("Ingresa tu número para saber si es par, impar o 0 \n ");
	Scanner sc7= new Scanner (System.in);
	int numero=sc7.nextInt();
	if (numero==0) {
		System.out.print("El número es 0 \n");
		}
	else if (numero%2==0) {
	System.out.print("Es par \n");	}
	else {
	System.out.print("Es impar \n");}
break;

case 5:
	System.out.print("Gracias por usar este menú \n ");

default: 
	System.out.print("Este número no es valido \n");
}
}
}
