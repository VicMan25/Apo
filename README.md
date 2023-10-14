![Logo Java](https://seeklogo.com/images/J/java-logo-7833D1D21A-seeklogo.com.png))

# Datos de Apo1 - Apo2

Datos relacionados a progración desde primer semestre hasta el actual.

## Empezando

<<<<<<< HEAD
En este documento vamos agregar nuestro trabjo de programacion de segundo semestre
=======
Se agregan apuntes y datos utiles de aprendizaje en la materia de APO
>>>>>>> c506c150bbbf15eb26f6bf275fe9d04800ac7e91

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