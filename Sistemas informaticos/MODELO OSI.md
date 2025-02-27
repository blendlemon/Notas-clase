Proceso Un servidor de Minecraft

1. **Capa de Aplicación**
	 El servidor de Minecraft y el juego del usuario se comunican mediante el protocolo de Minecraft, donde se manejan cosas especificas para el juego como:
	 1. Acciones del jugador: Moverse, construir, romper bloques...
	 2. Comandos del servidor: comandos como /tp, /seed
	 3. Plugins o mods: Si el servidor tiene de estos funciona en esta capa
	 
2. **Capa de Presentación**
	Aquí se determina el formato de los datos y como se estructuran los paquetes de información entre cliente-servidor así como el cifrado de datos para datos sensibles como pueden ser contraseñas ofreciendo una conexión segura.

3. **Capa de Sesión**
	Es donde se gestiona la conexión cliente-servidor, se establece la sesión cuando alguien se conecta al servidor, se mantiene esta cuando se esta jugando y se cierra cuando alguien corta la conexión con el servidor
	
4. **Capa de Transporte**
	Se utiliza el protocolo TPC para garantizar que los datos lleguen de manera confiable y en orden ya que es necesario enviar paquetes de datos que son los que determinan las acciones que tienen que realizarse y asegura una conexión fiable donde se asegura que no se pierdan paquetes para una experiencia fluida.

5. **Capa de Red**
	Tanto el servidor como los jugadores necesitan una IP, en el caso del servidor es la dirección de acceso a este y en caso de los jugadores sirve como un segundo identificador a la hora de conectarse, y el enrutamiento es necesario ya que es lo que dirigen los paquetes de un cliente al servidor y viceversa.

6. **Capa de Enlace de Datos**
	Es como se maneja la transmisión de datos en una red local o entre dispositivos.
	Se conectan los dispositivos a internet mediante cableado o wifi ya que es necesario para que los datos viajen a través de internet y los dispositivos necesitan de una dirección MAC para identificarse dentro de esta misma red.
	Por ejemplo si alguien se quiere conectar al servidor desde la misma red local que este necesitará su dirección en la red local.

7. **Capa física**
	Cables o señales inalámbricas: Infraestructura de internet.
	Hardware: Tarjetas de red, routers y otros dispositivos que permiten la conexión.