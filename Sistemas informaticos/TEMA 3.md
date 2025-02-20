1. Sistemas operativos
	1. Versiones de los sistemas operativos más utilizados
		1. Sistemas operativos de Microsoft:
			1. Home
			2. Pro
			3. Enterprise
			4. IoT
			5. Pro for Workstations
		2. Para equipos de tipo servidor: Microsoft Windows Server 2019
			1. Datacenter
			2. Standard
			3. Essentials
	2. Sistemas operativos GNU/Linux:
		1. Distribuciones escritorio	
			1. Ubuntu y Mint
			2. Arch Linux
			3. Kali Linux y Mint
			4. Chromium OS
			5. Manjaro
			6. Android
		2. Distribuciones Servidores:
			1. Red Hat Enterprise Linux
			2. Ubuntu Server
			3. CentOS
			4. SUSE Linux Enterprise Server
			5. Debian
			6. FreeBSD
	3. Arquitecturas de los sistemas operativos
		1. Sistemas con capas o anillos:
			1. Estructura jerárquica interna, en niveles o capas
			2. Formados por un conjunto de anillos concéntricos que representan servicios y funciones diferentes, cada nivel se comunica sólo con el nivel inmediatamente inferior o superior
			3. Ventajas: Uso de una estructura bien definida que facilita la corrección de errores
			4. Desventajas: Resulta lento y complejo al definir las capas
			5. Ejemplos: MULTICS y THE
		2. Sistemas con capas o anillos (Estructura):
			1. Núcleo o Kernel
				1. Capa que interactúa directamente con el hardware
				2. Formada por los componentes esenciales del sistema operativo debido a su relevancia y frecuencia de uso
				3. Cargado permanentemente en memoria principal
				4. Una parte del núcleo se encarga de abstraer la parte hardware del sistema para que el sistema operativo trabaje independientemente de la máquina donde sea instalada
				5. Se llama HAL (Hardware Abstraction Layer)
			2. Servicios
				1. Formada por un conjunto de funciones básicas que dan soporte a la capa superior para que interactúe con el núcleo.
				2. Funciones (más o menos diferenciadas):
					1. Gestión de procesos
					2. Gestión de memoria
					3. Gestión de I/O
					4. Gestión de almacenamiento secundario
			3. Interfaz:
				1. Constituida principalmente por un intérprete de órdenes cuya función es traducir y trasladar las acciones deseadas por un usuario a las capas inferiores.
				2. En este mismo nivel, aunque de manera diferenciada, se pueden catalogar los "programas de usuario" ("cualquier aplicación o software que instalamos en nuestro equipo y que nos permite realizar tareas concretas")
		3. Sistemas monolíticos:
			1. Estructura: un gran programa dividido en rutinas , en el que todas tienen los mismos privilegios y se pueden llamar unas a otras
			2. Formados por un conjunto de anillos concéntricos que representan servicios o funciones diferentes
			3. Cada capa solo se puede comunicar con la capa inmediatamente superior o inferior
			4. Se ejecuta en un espacio de direcciones de memoria principal único y compartido
			5. Ventajas: Diseño sencillo, rendimiento y velocidad
			6. Han evolucionado dejando atrás sus inconvenientes: difícil evolución, resolución de errores y estabilidad
			7. Ejemplos: DOS, UNIX y Ubuntu
		4. MicroKernel:
			1. Libera al núcleo del máximo de su funcionalidad
			2. Restringe el modo supervisor y facilita la evolución y el mantenimiento del sistema
			3. Los servicios quedan fuera del núcleo y se ejecutan en modo usuario
			4. El micronúcleo solo se encarga de la comunicación y gestión de todos los servicios clientes
			5. Ventajas: Seguridad, estabilidad y actualización del sistema operativo
			6. Desventajas: Posible sobrecarga que afecte al rendimiento del sistema
			7. Ejemplos: MINIX
		5. Kernel híbrido:
			1. Microkernel con implementación monolítica
			2. Ventajas: Estabilidad y rendimiento
			3. Los drivers y todos proceso relacionado con la comunicación entre procesos se ejecuta en modo supervisor
		6. Arquitecturas de los sistemas operativos actuales:
			1. MacOS: Híbrido
			2. Windows familia NT: Híbrido
			3. Ubuntu: Monolítico
2. Gestión de archivos
	1. Gestión de archivos
		1. Uno de los pilares fundamentales de cualquier SO
		2. Sistemas de archivos: Manera de almacenar y realizar operaciones con información
		3. Cada tipo de sistema de archivos tiene diferentes características, seguridad, rendimiento o gestión de datos.
	2. Funciones de los sistemas de archivos
		1. Acceder a la información
		2. Crear, eliminar y modificar ficheros
		3. Acceder a los ficheros mediante protocolos u otros ficheros
		4. Facilitar acceso multiusuario 
		5. Facilitar el acceso a medios de almacenamiento
		6. Realizar copias de seguridad
		7. Utilizar herramientas de recuperación de la información
		8. Priorizar eficiencia y seguridad
		9. Maximizar rendimiento
		10. Permitir monitorización y contabilidad
		11. Administrar el espacio de almacenamiento
	3. Sistemas de archivos
		1. Espacios de asignación: Unidades físicas mínimas de almacenamiento gestionadas por los sistemas de archivos
		2. Si el usuario no define el tamaño se asignará automáticamente (MBR o UEFI)
		3. Archivo: Unidad lógica mínima de información
		4. Directorio: Contenedor lógico de archivos y subdirectorios
		5. Partición: División del almacenamiento para organizar información
		6. Journaling: Registro que previene inconsistencias en caso de errores
	4. Journaling
		1. Registro o diario del sistema de archivos
		2. Registro de operaciones que permite deshacer estas en caso de errores
	5. Tipos de sistemas de archivos: FAT
		1. FAT (File Alocation Table)
		2. Creado para el sistema operativo MS-DOS
		3. Administración sencilla del espacio
		4. Limitaciones:
			1. Imposibilidad gestionar particiones superiores a 8TB y archivos de mas de 4GB
			2. Bajo rendimiento
			3. Inseguro
	6. Tipos de sistemas de archivos: exFAT
		1. Elimina limitaciones de FAT32
		2. Archivos de hasta 16 EB y mantiene ligereza
		3. Sigue resultando inseguro pero ideal para medios de almacenamiento FLASH
	7. Tipos de sistemas de archivos: NTFS
		1. Estándar Windows
		2. Mejoras considerables respecto a FAT32, seguridad y confiabilidad
		3. Ventajas
			1. Journaling
			2. cifrado y compresión
			3. Reduce la fragmentación y aumenta la velocidad de búsqueda
			4. volumenes de hasta 16EB y archivos de hasta 16TB
			5. Unicode para el nombre de los archivos
	8. Tipos de sistemas de archivos: APFS
		1. Sistema de archivos empleado por Apple Inc
		2. Versión mejorada de su predesora
		3. Sus características son similares a NTFS y ext4, archivos y volúmenes de hasta 8EB
		4. Permite encriptación y está optimizado para almacenamiento Flash
	9. Tipos de sistemas de archivos: ext4
		1. Para SO tipo linux en su cuarta versión
		2. Incluye journaling, archivos de hasta 16TB y volúmenes de hasta 1 EB
		3. No emplea extensiones como parte del nombre de los archivos, no obstante muchos nombres de archivos en Linux incorporan sufijos separados por un punto en el nombre del fichero por convención
3. Particiones de disco
	1. Particiones de disco
		1. Partición: División presente en una sola unidad física de almacenamiento de datos.
		2. Toda partición tiene su propio formato
		3. Generalmente, casi cualquier sistema operativo interpreta, utiliza y manipula cada partición como un disco físico independiente
	2. Ejemplo particionado de disco
		1. Windows con sistema de archivos NTFS
		2. (/) con sistema de archivos EXT4
		3. Intercambio o swap
		4. /home con sistema de archivos EXT4, datos de usuario en una partición aparte
	3. Estrucura lógica de un disco duro
		1. Primer sector cabeza 0, cilindro 0, sector 1
		2. Tabla de particiones y Master Boot
		3. Master Boot: programa de inicialización que lee la tabla de particiones y cede el control al sector de arranque
		4. Espacio particionado
		5. Espacio no particionado
	4. Particiones primarias, extendidas y lógicas
		1. Las particiones a las que se puede asignar un sistema de archivos pueden ser de dos tipos: Primarias y lógicas
		2. Partición extendida: Partición primaria especial donde se cran las particiones lógicas
		3. Las particiones extendidas se inventaron para superar el límite de 4 particiones primarias máximas por cada disco duro y poder crear un número ilimitado de unidades lógicas, cada una con un sistema de archivos diferente de la otra
	5. Cantidad de particiones en dispositivo físico
		1. Mínimo una máximo cuatro
		2. No puede haber más de una partición extendida en un mismo disco duro
		3. dentro de una partición extendida puede haber todas las particiones lógicas que queramos
	6. El MBR y la tabla de particiones
		1. MBR primer sector de un disco duro (512 bytes)
		2. La BIOS lee el código ejecutable del MBR durante el proceso de arranque el cual apunta al siguiente punto a mirar
		3. Elementos del MBR:
			1. Programa encargado de pasar el control al sector cero de la partición  o sector de arranque que contiene el sistema operativo a iniciar
			2. tabla de particiones del disco
			3. Firma de unidad arrancable
			4. Primeros 446 bytes de MBR podemos tener un programa gestor de arranque o una indicación de cual es la partición activa
				1. Primer caso menú de arranque
				2. Si no se pasaría el control al sector 0 de dicha partición
			5. La tabla de particiones está alojada en el Master Boot Record a partir del byte 446 y ocupa 64 bytes, conteniendo 4 registros de 16 bytes, los cuales definen las particiones primarias. En ellos se almacena toda la información básica sobre la partición:
				1. Si es arrancable o si no lo es
				2. El formato o sistema de archivos
				3. El tamaño de la partición
				4. El sector de inicio de la partición
			6. Cuando sólo hay instalado un sistema operativo el gestor de arranque suele ser transparente y el usuario puede que no se de cuenta de que existe
	7. Identificación de particiones
		1. Windows
			1. Va por letras y las letras A y B se reservan para disquetes externos
		2. Linux
			1. /dev/xxyN
				1. dev directorio asociado a todos los archivos de dispositivo 
				2. xx se refiere a si es hd o sd
				3. y indica donde se indica la partición
				4. N de 1 a 4 partición primaria o extendia a partir de 5 partición lógica de una partición extendida
4. RAID
	1. RAID
		1. Redundant Array of Independent Disk: sistema de emparejamiento de discos que nos permite crear uno o varios volúmenes
	2. Configuración de RAID
		1. Por software: Ralentiza el equipo ya que el SO lo gestiona y tiene que dedicar recursos a esto
		2. Por hardware: Requiere una tarjeta controladora RAID instalada en el equipo que tiene su propia CPU
		3. Híbrido: PseudoRAID que de suele administrar desde la BIOS de algunas placas base simulando ser un RAID por hardware pero con funcionalidades limitadas, no consume recursos pero es más lenta y menos fiable
	3. Tipos de RAID
		1. RAID 0
			1. No hay redundancia si un disco falla se pierde la información, mejora la capacidad y el rendimiento
		2. RAID 1
			1. Cada disco tiene la misma información para garantizar la continuidad en caso de fallo de uno de ellos, el tamaño total es igual al disco más pequeño, no mejora la velocidad de escritura pero si la de lectura aunque no siempre se logra
		3. RAID 5
			1. Al menos 3 discos y emplea paridad permitiendo reconstruir datos si uno de los discos falla, no mejora la velocidad de escritura pero optimiza la lectura
		4. RAID 6
			1. Evolución RAID 5, requiere al menos 4 discos, mayor fiabilidad mejor rendimiento y mayor seguridad ante fallos de disco
		5. RAID 10
			1. Combina los beneficios de la raid 1 y 0, requiere al menos 4 discos y ofrece tanto rendimiento como redundancia. Mejora rendimiento en comparación a los anteriores pero solo permite el fallo de un disco por par de discos espejados. Si fallan ambos discos se pierde la información
		6. Calculadoras
			1. Existen diversas combinaciones de configuraciones de RAID, se pueden usar calculadoras de RAID en línea. Algunas permiten añadir un disco spare que se activa automáticamente cuando un disco falla, permitiendo la reconstrucción del sistema RAID sin pérdida de datos.
5. Gestión de Usuarios
	1. Funciones
		1. Controlar el acceso
		2. Seguridad
		3. Evitar accesos no autorizados
		4. Administración del sistema
	2. Tipos de Usuarios
		1. Administrador
			1. control total
			2. crear modificar y eliminar cuentas
			3. acceso total
			4. instalar y desinstalar programas
			5. Modificar permisos
		2. Estandar
			1. no puede realizar cambios críticos
			2. No puede instalar software
			3. acceso restringido
			4. minimiza riesgos de seguridad
		3. Invitado
			1. Acceso limitado
			2. No puede modificar configuraciones ni instalar programas
			3. usuario temporal
	3. Permisos
		1. Windows
			1. modelo basado en grupos y permisos NTFS
			2. Cada archivo tiene una lista de permisos configurables
				1. Control total
				2. Lectura y ejecucion
				3. Escritura
				4. Modificación
			3. Se puede modificar en:
				1. propiedades de una carpeta > seguridad > Editar permisos
				2. Herramientas avanzadas como gpedit.msc
		2. Linux
			1. Usa un modelo basado en usuarios grupos y permisos en archivos
			2. Cada archivo tiene tres tipos de permisos
			3. r,w,x
	4. Seguridad
		1. Contraseñas seguras (lo tipico 8-12 caracteres blablabla)
		2. Politicas de seguridad (Forzar cambio contraseñas, bloquear tras intentos fallidos...)
		3. Gestión de permisos
			1. No otorgar privilegios de administrador a todos los usuarios
			2. Crear grupos de usuarios con permisos diferenciados
			3. Revisar y actualizar los permisos periódicamente
		4. Registro de actividad y auditoria
			1. Windows visor de eventos (eventvwr.msc)
			2. En linux revisar logs sudo cat /var/log/auth.log
	5. Herramientas
		1. Windows
			1. Panel de control cuentas usuario, para gestionar usuarios basicos
			2. Administración de equipos compmgmt.msc para usuarios y grupos locales
			3. Editor de directivas de grupo gpedit.msc para configurar políticas avanzadas
			4. cmd y powershell comandos como net user  usuario/add
		2. Linux
			1. sudo add user usuario
			2. sudo passwd usuario
			3. sudo chmod 750 carpeta
			4. cat /etc/passwd