// Calcula el promedio de una lista de N datos.
// Permite repetir el cálculo hasta que el usuario decida salir.

Algoritmo PromedioRepetido
	
	Definir n, i Como Entero
	Definir dato, acum, prom Como Real
	Definir continuar Como Cadena

	continuar <- "si"

	Mientras continuar = "si" o continuar = "sí" o continuar = "SI" o continuar = "Sí" Hacer
		
		Escribir "Ingrese la cantidad de datos:"
		
		Repetir
			Leer n
			Si n <= 0 Entonces
				Escribir "El número debe ser positivo y distinto de cero."
			Fin Si
		Hasta Que n > 0
		
		acum <- 0
		
		Para i <- 1 Hasta n Con Paso 1 Hacer
			Escribir "Ingrese el dato ", i, ":"
			
			Repetir
				Leer dato
				Si dato < 0 Entonces
					Escribir "El dato debe ser positivo. Intente nuevamente:"
				Fin Si
			Hasta Que dato >= 0
			
			acum <- acum + dato
		Fin Para
		
		prom <- acum / n
		Escribir "El promedio es: ", prom
		
		Escribir "¿Desea calcular otro promedio? (si/no):"
		Leer continuar
	Fin Mientras
	
	Escribir "Gracias por usar el programa. ¡Hasta luego!"

FinAlgoritmo
