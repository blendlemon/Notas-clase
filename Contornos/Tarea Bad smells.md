```python
import sqlite3

  

def conectar():

    conn = sqlite3.connect('Empresa.db')

    return conn

  

def crear_taboas(conn):

    cursor = conn.cursor()

  

    cursor.execute('''

        CREATE TABLE IF NOT EXISTS departamentos(

                   cod_d INT PRIMARY KEY,

                   nome TEXT NOT NULL,

                   director VARCHAR(9),

                   PRIMARY KEY (id),

                   );

  

                   ''')

    conn.commit()

  
  

    cursor.execute('''

        CREATE TABLE IF NOT EXISTS empregados(

                   dni CHAR(9),

                   nome TEXT NOT NULL,

                   salario REAL NOT NULL,

                   departamento INT,

                   PRIMARY KEY (dni),

                   FOREIGN KEY (departamento) REFERENCES departamentos(cod_d)

                   );

  

    ''')

    conn.commit()

  

def inserir_departamento(conn,departamento):

    cursor = conn.cursor()

  

    cursor.execute(f"INSERT IN departamentos(id,nome,director) VALUES('{departamento.cod_d}','{departamento.nome}','{departamento.director}');")

    conn.commit()

  

def inserir_empregado(conn, empregado):

    cursor = conn.cursor()

  

    cursor.execute(f"INSERT IN empregados(dni,nome,salario,departamento) VALUES('{empregado.dni}','{empregado.nome}',{empregado.salario},'{empregado.departamento}');")

    conn.commit()

  

def obter_departamentos(conn):

    cursor = conn.cursor()

    cursor.execute("SELECT * FROM departamentos")

    conn.commit()

  

def obter_departamento_por_codigo(conn):

    codigo = int(input("Introduce el código del departamento a obtener"))

  

    cursor = conn.cursor()

    cursor.execute(f"SELECT * FROM departamentos WHERE cod_d={codigo}")

    conn.commit()

  

def obter_empregados(conn):

    cursor = conn.cursor()

  

    cursor.execute("SELECT * FROM empregados")

    conn.commit()

def obter_empregado_por_dni(conn):

    dni = input("DNI empregado: ")

  

    cursor = conn.cursor()

  

    cursor.execute(f"SELECT * FROM empregados WHERE dni={dni}")

    conn.commit()

  

def obter_empregado_por_departamento(conn):

    codigo = int(input("Introduce el código del departamento: "))

  

    cursor = conn.cursor()

    cursor.execute(f"SELECT * FROM empregados WHERE departamento={codigo}")

    conn.commit()

  

def actualizar_departamento(conn):

    codigo = int(input("Codigo del departamento a modificar: "))

    nome = input("Nuevo nombre del departamento")

    director = input("Nuevo dni del director")

  

    cursor = conn.cursor()

  

    cursor.execute(f"UPDATE departamentos SET nome='{nome}', director='{director}' WHERE cod_d={codigo}")

    conn.commit()

  

def actualizar_empregado(conn):

    dni = input("Dni de empleado a modificar: ")

    nome = input("Nuevo nombre: ")

    salario = float(input("Nuevo salario: "))

    departamento = int(input("Nuevo codigo de departamento"))

  

    cursor = conn.cursor()

    cursor.execute(f"UPDATE empregados SET nome='{nome}', salario={salario}, departamento={departamento} WHERE dni='{dni}'")

    conn.commit()

  

def eliminar_departamento(conn):

    codigo = int(input("Codigo departamento a eliminar: "))

  

    cursor = conn.cursor()

  

    cursor.execute(f"DELETE FROM departamentos WHERE cod_d={codigo}")

    conn.commit()

  

def eliminar_empregado(conn):

    codigo = input("DNI empleado a eliminar: ")

  

    cursor = conn.cursor()

  

    cursor.execute(f"DELETE FROM empreagados WHERE dni='{codigo}'")

    conn.commit()

  

def pechar_conexion(conn):

    conn.close()
 
```


```python
 import sqlite3
 

 def conectar():
  # Primitive Obsession: Se usa un string literal para el nombre de la base de datos.
  # Sugerencia: Definir una constante para el nombre de la base de datos.
  conn = sqlite3.connect('Empresa.db')
  return conn
 

 def crear_taboas(conn):
  cursor = conn.cursor()
 

  # Long Method: Esta función hace demasiado (crea dos tablas).
  # Divergent Change: Si la estructura de la base de datos cambia, esta función tendrá que ser modificada en múltiples lugares.
  # Sugerencia: Dividir en funciones más pequeñas, una para crear cada tabla.
  cursor.execute('''
  CREATE TABLE IF NOT EXISTS departamentos(
  cod_d INT PRIMARY KEY,
  nome TEXT NOT NULL,
  director VARCHAR(9),
  PRIMARY KEY (cod_d) -- Corrección: cod_d en lugar de id
  );
  ''')
  conn.commit()
 

  cursor.execute('''
  CREATE TABLE IF NOT EXISTS empregados(
  dni CHAR(9),
  nome TEXT NOT NULL,
  salario REAL NOT NULL,
  departamento INT,
  PRIMARY KEY (dni),
  FOREIGN KEY (departamento) REFERENCES departamentos(cod_d)
  );
 

  ''')
  conn.commit()
 

 def inserir_departamento(conn, departamento):
  cursor = conn.cursor()
 

  # Stringly Typed: Se usa f-strings para construir la consulta SQL, lo cual es propenso a errores de sintaxis y SQL injection.
  # Data Clump: El objeto `departamento` podría ser un diccionario o similar, pero se accede a sus atributos directamente en la consulta.
  # Sugerencia: Usar parámetros parametrizados en la consulta SQL para evitar SQL injection y mejorar la legibilidad.
  cursor.execute(f"INSERT INTO departamentos(cod_d, nome, director) VALUES('{departamento.cod_d}', '{departamento.nome}', '{departamento.director}');")
  conn.commit()
 

 def inserir_empregado(conn, empregado):
  cursor = conn.cursor()
 

  # Stringly Typed: Similar al anterior, usar parámetros parametrizados.
  # Data Clump: Similar al anterior, el objeto `empregado` podría ser mejor manejado.
  cursor.execute(f"INSERT INTO empregados(dni, nome, salario, departamento) VALUES('{empregado.dni}', '{empregado.nome}', {empregado.salario}, '{empregado.departamento}');")
  conn.commit()
 

 def obter_departamentos(conn):
  cursor = conn.cursor()
  cursor.execute("SELECT * FROM departamentos")
  conn.commit() # Omitir commit en operaciones de lectura
 

 def obter_departamento_por_codigo(conn):
  # Shotgun Surgery: Si cambias la forma de obtener el código, tendrás que modificarlo en varios lugares.
  codigo = int(input("Introduce el código del departamento a obtener"))
 

  cursor = conn.cursor()
  # Stringly Typed: Riesgo de SQL injection.
  cursor.execute(f"SELECT * FROM departamentos WHERE cod_d={codigo}")
  conn.commit() # Omitir commit en operaciones de lectura
 

 def obter_empregados(conn):
  cursor = conn.cursor()
 

  cursor.execute("SELECT * FROM empregados")
  conn.commit() # Omitir commit en operaciones de lectura
 def obter_empregado_por_dni(conn):
  dni = input("DNI empregado: ")
 

  cursor = conn.cursor()
 

  # Stringly Typed: Riesgo de SQL injection.
  cursor.execute(f"SELECT * FROM empregados WHERE dni='{dni}'")
  conn.commit() # Omitir commit en operaciones de lectura
 

 def obter_empregado_por_departamento(conn):
  codigo = int(input("Introduce el código del departamento: "))
 

  cursor = conn.cursor()
  # Stringly Typed: Riesgo de SQL injection.
  cursor.execute(f"SELECT * FROM empregados WHERE departamento={codigo}")
  conn.commit() # Omitir commit en operaciones de lectura
 

 def actualizar_departamento(conn):
  codigo = int(input("Codigo del departamento a modificar: "))
  nome = input("Nuevo nombre del departamento")
  director = input("Nuevo dni del director")
 

  cursor = conn.cursor()
 

  # Stringly Typed: Riesgo de SQL injection.
  cursor.execute(f"UPDATE departamentos SET nome='{nome}', director='{director}' WHERE cod_d={codigo}")
  conn.commit()
 

 def actualizar_empregado(conn):
  dni = input("Dni de empleado a modificar: ")
  nome = input("Nuevo nombre: ")
  salario = float(input("Nuevo salario: "))
  departamento = int(input("Nuevo codigo de departamento"))
 

  cursor = conn.cursor()
  # Stringly Typed: Riesgo de SQL injection.
  cursor.execute(f"UPDATE empregados SET nome='{nome}', salario={salario}, departamento={departamento} WHERE dni='{dni}'")
  conn.commit()
 

 def eliminar_departamento(conn):
  codigo = int(input("Codigo departamento a eliminar: "))
 

  cursor = conn.cursor()
 

  # Stringly Typed: Riesgo de SQL injection.
  cursor.execute(f"DELETE FROM departamentos WHERE cod_d={codigo}")
  conn.commit()
 

 def eliminar_empregado(conn):
  codigo = input("DNI empleado a eliminar: ")
 

  cursor = conn.cursor()
 

  # Typo: "empreagados" en lugar de "empregados".
  # Stringly Typed: Riesgo de SQL injection.
  cursor.execute(f"DELETE FROM empregados WHERE dni='{codigo}'")
  conn.commit()
 

 def pechar_conexion(conn):
  conn.close()
```

**Resumen de "Bad Smells" Encontrados:**

- **Primitive Obsession:** Uso de strings literales en lugar de constantes.
- **Long Method:** La función `crear_taboas` hace demasiado.
- **Divergent Change:** La función `crear_taboas` es susceptible a cambios en múltiples lugares si la estructura de la base de datos cambia.
- **Stringly Typed:** Uso de f-strings para construir consultas SQL, lo que es peligroso y dificulta el mantenimiento.
- **Data Clump:** Los objetos `departamento` y `empregado` no se manejan de la mejor manera al construir las consultas.
- **Shotgun Surgery:** Cambios en la forma de obtener datos requieren modificaciones en varios lugares.
- **Typo:** Error de escritura en `eliminar_empregado` ("empreagados").
- **Useless commit:** Se llama a `conn.commit()` en funciones de lectura.

**Recomendaciones Generales:**

- **Usar ORM (Object-Relational Mapper):** Considera usar un ORM como SQLAlchemy para abstraer la interacción con la base de datos. Esto reducirá la cantidad de código SQL directo y ayudará a prevenir SQL injection.
- **Parametrizar Consultas SQL:** Siempre usa parámetros parametrizados en lugar de interpolación de strings para construir consultas SQL.
- **Crear Clases para Entidades:** Define clases `Departamento` y `Empregado` para representar las entidades de la base de datos. Esto hará que el código sea más legible y fácil de mantener.
- **Separar la Lógica de la Base de Datos:** Crea una capa de abstracción para la base de datos para que el resto del código no tenga que interactuar directamente con la conexión y los cursores.
- **Manejo de Excepciones:** Añade manejo de excepciones para capturar errores de la base de datos y manejarlos de forma adecuada.
- **Validación de Datos:** Valida los datos de entrada antes de insertarlos o actualizarlos en la base de datos.

Aplicar estas refactorizaciones mejorará la calidad, seguridad y mantenibilidad del código.