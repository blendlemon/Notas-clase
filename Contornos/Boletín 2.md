**Ejercicio 1: Determinar si un número es par o impar**

**Grafo de flujo**

	1. Inicio --> Leer n
	2. Decisión: ¿n mod 2 == 0?
		1. Si es verdadero: Escribir "El número es par" --> Fin
		2. Si es falso: Escribir "El número es impar" --> Fin

**Complejidad ciclomática**

CC = 1+1 = 2

**Ejercicio 2: Encontrar el mayor de dos números**

**Grafo de flujo**

	1. Inicio --> Leer a y b
	2. Decisión: ¿a > b?
		1. Si es verdadero: Escribir "a es mayor" --> Fin
		2. Si es falso: Escribir "b es mayor o iguales" --> Fin

**Complejidad ciclomática**

CC = 1+1 = 2

**Ejercicio 3: Calcular la suma de los primeros N números**

**Grafo de flujo**

	1. Inicio --> Leer n
	2. Decisión: suma = 0
	3. Bucle: Para i = 1 hasta n
		1. Sumar i a suma	
	4. Fin del bucle: Escribir suma --> Fin

**Complejidad ciclomática**
1. Hay 1 bucle
2. No hay decisiones adicionales
CC = 1+1 = 2
