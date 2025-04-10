1) Averigua quien está conectado
		who
2) Quien eres tu
		whoaim
3) Crea todos las carpetas siguientes con una sola instrucción :

	piso1A piso1B piso1C piso1D piso2A piso2B piso2C piso2D
	
	mkdir piso1A piso1B piso1C piso1D piso2A piso2B piso2C piso2D
4) Crea un archivo llamado prueba.txt
	touch prueba.txt
5) Redirecciona la salida del man -who a un archivo : ayuda.txt
	man who > ayuda.txt
6) Copia archivos de la carpeta piso1A a piso2D
	cp piso1A/* piso2D/
7) Visualiza el contenido del archivo ayuda.txt
	cat ayuda.txt
8) Visualiza lo que contiene la variable $HOME
	echo $HOME
9) Mueve un archivo de la carpeta piso1D a la carpeta piso2C
	mv piso1D/nombre_del_archivo piso2C/
10) Utiliza los comandos cat, less, more, tail y head para ver un archivo de texto grande (Lo puedes crear redireccionando)

11) Elimina todas las carpetas pisos con una sola instrucción
	rm -r piso1A piso1B piso1C piso1D piso2A piso2B piso2C piso2D
12) Visualiza la fecha.txt
	date > fecha.txt
	cat fecha.txt