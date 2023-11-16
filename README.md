# Diagramas
Actividades Grupo 2

Algoritmo virus
	Definir h, m, s Como Entero
	Para h<-1 Hasta 23 Hacer
		Para m<-1 Hasta 59 Hacer
			Para s<-1 Hasta 59 Hacer
				Escribir h, ':', m, ':', s
			FinPara
		FinPara
	FinPara
FinAlgoritmo
/
Algoritmo profe_explicacio
	Definir r Como Cadena
	Escribir 'deseas ingresar al ciclo'
	Leer r
	Mientras (r='s') O (r='casa') Hacer
		Escribir 'quieres entrar nuevamente al ciclo'
	FinMientras
	Escribir 'fin'
FinAlgoritmo
/
Algoritmo dowhile
	Definir PrimerNumero, SegundoNumero, Respuesta Como Entero
	Definir RespuestaUsuario Como Cadena
	PrimerNumero <- 0
	SegundoNumero <- 0
	Respuesta <- 0
	RespuestaUsuario <- 's'
	Repetir
		Escribir 'Digite el primer numero'
		Leer PrimerNumero
		Escribir 'digite el segundo numero'
		Leer SegundoNumero
		Respuesta <- PrimerNumero+SegundoNumero
		Escribir 'Respuesta: ', Respuesta
		Escribir '¿ Desea realizar otra operacion? S/N'
		Leer RespuestaUsuario
	Hasta Que RespuestaUsuario='N' O RespuestaUsuario='n'
FinAlgoritmo
/
Algoritmo while_icft 
	Definir numero, factor, numero2 Como Real
	Escribir 'ingrese un numero para obtener el factorial'
	Leer numero
	factor <- 1
	numero2 <- numero
	Si numero>=0 Entonces
		Mientras numero<>0 Hacer
			factor <- factor*numero
			numero <- numero-1
		FinMientras
	SiNo
		Mientras numero<>0 Hacer
			factor <- factor*numero
			numero <- numero+1
		FinMientras
	FinSi
	Escribir 'el factorial del numero ', numero2, 'es: ', factor
FinAlgoritmo
/
Algoritmo SumaHastaCero_DoWhile
	Definir numero, suma Como Real
	suma <- 0
	Repetir
		Escribir 'Ingrese números para sumar (ingrese 0 para finalizar):'
		Leer numero
		suma <- suma+numero
	Hasta Que numero=0
	Escribir 'La suma de los números ingresados es: ', suma
FinAlgoritmo
/
Algoritmo AdivinaElNumero
	Definir numeroSecreto, intento Como Entero
	numeroSecreto <- 50
	intento <- 0
	Escribir 'Adivina el número secreto (del 1 al 100):'
	Mientras intento<>numeroSecreto Hacer
		Escribir 'Ingrese tu intento:'
		Leer intento
		Si intento<numeroSecreto Entonces
			Escribir 'El número secreto es mayor.'
		SiNo
			Si intento>numeroSecreto Entonces
				Escribir 'El número secreto es menor.'
			FinSi
		FinSi
	FinMientras
	Escribir '¡Felicidades! Has adivinado el número secreto.'
FinAlgoritmo
/
Algoritmo ContadorPares
	Definir limite, contador Como Entero
	Escribir 'Ingrese un límite:'
	Leer limite
	contador <- 0
	Mientras contador<=limite Hacer
		Si contador MOD 2=0 Entonces
			Escribir contador
		FinSi
		contador <- contador+1
	FinMientras
FinAlgoritmo
/
Algoritmo Adivina_Numero
	intentos <- 10
	num_secreto <- azar(100)
	Escribir 'encuentra el numero (de 1 a 100):'
	Leer num_ingresado
	Mientras num_secreto<>num_ingresado Y intentos>1 Hacer
		Si num_secreto>num_ingresado Entonces
			Escribir 'Muy bajo'
		SiNo
			Escribir 'Muy alto'
		FinSi
		intentos <- intentos-1
		Escribir 'Le quedan ', intentos, ' intentos:'
		Leer num_ingresado
	FinMientras
	Si num_secreto=num_ingresado Entonces
		Escribir 'Exacto! Usted adivino en ', 11-intentos, ' intentos.'
	SiNo
		Escribir 'El numero era: ', num_secreto
	FinSi
FinAlgoritmo
/
Algoritmo sin_titulo
	Repetir
		// mostrar menu
		Limpiar Pantalla
		Escribir 'Menú de recomendaciones'
		Escribir '   1. Literatura'
		Escribir '   2. Cine'
		Escribir '   3. Música'
		Escribir '   4. Videojuegos'
		Escribir '   5. Salir'
		// ingresar una opcion
		Escribir 'Elija una opción (1-5): '
		Leer OP
		// procesar esa opción
		Según OP Hacer
			1:
				Escribir 'Lecturas recomendables:'
				Escribir ' + Esperándolo a Tito y otros cuentos de fúbol (Eduardo Sacheri)'
				Escribir ' + El juego de Ender (Orson Scott Card)'
				Escribir ' + El sueño de los héroes (Adolfo Bioy Casares)'
			2:
				Escribir 'Películas recomendables:'
				Escribir ' + Matrix (1999)'
				Escribir ' + El último samuray (2003)'
				Escribir ' + Cars (2006)'
			3:
				Escribir 'Discos recomendables:'
				Escribir ' + Despedazado por mil partes (La Renga, 1996)'
				Escribir ' + Búfalo (La Mississippi, 2008)'
				Escribir ' + Gaia (Mägo de Oz, 2003)'
			4:
				Escribir 'Videojuegos clásicos recomendables'
				Escribir ' + Día del tentáculo (LucasArts, 1993)'
				Escribir ' + Terminal Velocity (Terminal Reality/3D Realms, 1995)'
				Escribir ' + Death Rally (Remedy/Apogee, 1996)'
			5:
				Escribir 'Gracias, vuelva prontos'
			De Otro Modo:
				Escribir 'Opción no válida'
		FinSegún
		Escribir 'Presione enter para continuar'
		Esperar Tecla
	Hasta Que OP=5
FinAlgoritmo
