![Logo Java](https://seeklogo.com/images/J/java-logo-7833D1D21A-seeklogo.com.png))

# Datos de Apo1 - Apo2

Datos relacionados a progración desde primer semestre hasta el actual.

## Empezando

<<<<<<< HEAD
En este documento vamos agregar nuestro trabajo de programacion de segundo semestre
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
***********************************************************************************************
#nuevo codigo
/**
	 * Clase que representa la encuesta del curso
	 * @class Encuesta
	 */
public class Encuesta {
	/**
	 *Atibutos 
	 */
	// Modela el rango de edad de 0 a 17 años
	private RangoEdad rangoEdadJovenes;
	
	// Modela el rango de edad de 18 a 54 años
	private RangoEdad rangoEdadAdultos;
	
	// Modela el rango de edad de 55 años en adelante
	private RangoEdad rangoEdadMayores;
	
	/**
	 * Metodos
	 */
****************************************************************************************************
public class HolaMundo {
    public static void main(String[] args) {
        System.out.println("Hola, mundo");
    }
}


