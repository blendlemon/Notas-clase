Ejecute el siguiente script para crear una base de datos llamada ventas.

		DROP DATABASE IF EXISTS ventas;
		CREATE DATABASE ventas CHARACTER SET latin1;
		USE ventas;
		
		CREATE TABLE cliente(
		id INT UNSIGNED AUTO_INCREMENT PRIMARY KEY,
		nombre VARCHAR(25),
		primer_apellido VARCHAR(15) NOT NULL,
		ciudad VARCHAR(100),
		categoria INT UNSIGNED
		);
		
		CREATE TABLE comercial (
			id INT UNSIGNED AUTO_INCREMENT PRIMARY KEY,
			nombre VARCHAR(100) NOT NULL,
			apellido1 VARCHAR(100) NOT NULL,
			apellido2 VARCHAR(100),
			comision FLOAT
		);
		
1. Una vez que ha ejecutado el script y ha creado la base de datos en MySQL Server, ¿qué sentencia SQL debería ejecutar para modificar el encoding de la base de datos y utilizar utf8mb4 en lugar de latin1?

		ALTER DATABASE ventas 
        CHARACTER SET = utf8mb4
        COLLATE = utf8mb4_unicode_ci;

2. Modifique la columna nombre de la tabla cliente para que pueda almacenar cadenas de hasta 100 caracteres y para que no pueda ser NULL.

		ALTER TABLE cliente MODIFY nombre VARCHAR(100) NOT NULL;

3. ¿Qué comando puede ejecutar para comprobar que el cambio que se ha realizado en el paso anterior se ha ejecutado correctamente?

		DESCRIBE cliente;

4. Modifique el nombre de la columna primer_apellido y asígnele apellido1. También tendrá que permitir que pueda almacenar hasta 100 caracteres y que no pueda ser un valor NULL.

		ALTER TABLE cliente CHANGE primer_apellido apellido1 VARCHAR(100) NOT NULL;

5. Añada una nueva columna a la tabla cliente para poder almacenar el segundo apellido. La columna se debe llamar apellido2 debe estar entre la columna apellido1 y ciudad, puede almacenar hasta 100caracteres y puede ser NULL.

		ALTER TABLE cliente ADD apellido2 VARCHAR(100) AFTER apellido1;

6. Elimine la columna categoria de la tabla cliente.

		ALTER TABLE cliente DROP categoria;

7. Modifique la columna comision de la tabla comercial para que almacene por defecto el valor 10.

		ALTER TABLE comercial ALTER comision SET DEFAULT 10;