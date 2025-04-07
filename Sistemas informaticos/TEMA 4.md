# Protocolo

- **Protocolo:** Es un conjunto de reglas y procedimientos que permiten a los ordenadores comunicarse a través de una red, estableciendo una semántica y sintaxis común para la identificación, comunicación, sincronización y recuperación de errores.
- **Modelos:** Inicialmente, las redes usaban protocolos específicos de cada fabricante, lo que generaba incompatibilidad. Para solucionar esto, la ISO desarrolló el modelo OSI en 1984. Sin embargo, el modelo TCP/IP ganó popularidad y se impuso. El modelo OSI, aunque no implementado, es fundamental como referencia.
- **Beneficios del modelo OSI:**
    - Simplifica el diseño e implementación al dividir la comunicación en componentes más pequeños.
    - Permite a los desarrolladores enfocarse en entradas y salidas concretas de cada capa.
    - Los cambios en una capa no afectan a las demás.
    - Facilita la estandarización de funciones.
    - Permite la comunicación entre hardware y software nuevo y antiguo.

# Modelo OSI

- **Aplicación:** Interfaz entre el software de aplicación y la red. Define protocolos como FTP, HTTP, POP, SMTP, Telnet.
- **Presentación:** Traduce y codifica datos entre la aplicación y un formato genérico para la red. Se encarga de la conversión de juegos de caracteres, compresión/descompresión y cifrado/descifrado.
- **Sesión:** Gestiona las sesiones de comunicación para diferentes aplicaciones, asegurando que los datos lleguen a la aplicación correcta. Crea, administra y destruye sesiones, controlando la comunicación entre sistemas.
- **Transporte:** Establece una conexión lógica entre los equipos, independizándolos de la red física. Proporciona entrega de datos (fiable o no), control de flujo y recuperación de errores.
- **Red:** Identifica origen y destino con direcciones lógicas. Los routers utilizan esta capa para determinar la mejor ruta para los paquetes. Utiliza protocolos enrutados (direccionamiento y reenvío) y de enrutamiento (determinación de ruta).
- **Enlace de datos:** Transfiere datos dentro de la red local usando direcciones físicas. Controla el acceso al medio para evitar colisiones y detecta errores en los datos.
- **Física:** Gestiona los dispositivos físicos de comunicación. Envía y recibe bits sin interpretar su significado, adaptándolos al medio de transmisión (óptico, infrarrojo, etc.).

# Modelo TCP/IP

Modelo TCP/IP: Estándar abierto con un planteamiento muy parecido al modelo de
referencia OSI.
Es el que se utiliza de forma generalizada en la actualidad.

- **Capa de Aplicación:** Incluye comunicación con el software, traducción y codificación de datos, y diálogo entre sistemas.
- **Protocolos de la capa de aplicación:**
    - **Telnet:** Emula una terminal de texto de un equipo remoto.
    - **HTTP:** Transfiere páginas web entre un servidor y un cliente.
    - **FTP:** Transfiere archivos entre dos equipos.
    - **TFTP:** Versión simplificada de FTP, rápida pero insegura.
    - **SMTP:** Envía correos electrónicos.
    - **DNS:** Traduce nombres de dominio a direcciones IP.
    - **DHCP:** Asigna automáticamente direcciones IP y otros parámetros de red.

- **Capa de Transporte:** Administra la conexión lógica entre los equipos y el envío de datos.
- **Protocolos de la capa de transporte:**
    - **TCP (Transmission Control Protocol):** Protocolo confiable y orientado a la conexión, con acuse de recibo. Los routers solo ven datagramas y TCP se encarga de verificarlos y ordenarlos.
    - **UDP (User Datagram Protocol):** Protocolo simple y no confiable, sin detección de errores. Ideal para video y audio cuando la red es fiable.
- **Concepto de puerto:**
    - TCP y UDP utilizan puertos para separar el tráfico de diferentes aplicaciones.
    - Los puertos comunes (1-1024) están predeterminados.
    - Se asigna un puerto aleatorio (mayor que 1024) para el tráfico de retorno.
- **Socket:** Conjunto formado por la dirección IP, el protocolo (TCP o UDP) y el número de puerto. Permite que una aplicación se comunique con diferentes equipos simultáneamente.

- **Capa Internet:**
    - Equivalente a la capa de red del modelo OSI.
    - Los routers utilizan esta capa para el direccionamiento lógico, la determinación de la ruta y el reenvío de paquetes.
    - **Protocolos:**
        - **IP (Internet Protocol):** Transporta datagramas, pero no garantiza su entrega.
        - **ARP (Address Resolution Protocol):** Utilizado por los routers para obtener información sobre las redes a su alcance.
        - **ICMP (Internet Control Message Protocol):** Facilita la administración de mensajes de error.
        - **IGMP (Internet Group Management Protocol):** Permite que los equipos formen parte de grupos de multidifusión.
        - **RARP (Reverse Address Resolution Protocol):** Resuelve la dirección IP a partir de la dirección hardware.
- **Capa de Acceso a la Red:**
    - Especifica la transferencia de paquetes desde la capa Internet a través de la red física.
    - El destino puede ser otro equipo en la misma red o un router.
    - A diferencia de la capa Internet, su alcance solo llega hasta el primer router.
    - **Aspectos que se resuelven:**
        - Enrutamiento de datos a través de la conexión.
        - Sincronización de la transmisión.
        - Formato de los datos.
        - Conversión de señales (analógica/digital).
        - Detección de errores.
    - **Ejemplos de protocolos:** Ethernet (redes locales), PPP y Frame Relay (redes WAN).

# Conexión de sistema en red

- **Direcciones IP:**
    - Utilizadas por el protocolo IP para identificar cada ordenador en la red.
    - Formadas por 4 bytes (números enteros de 0 a 255) separados por puntos.
    - Cada equipo debe tener una dirección IP única dentro de la misma red.
    - Estructura:
        - **NetID:** Identifica la red.
        - **Host-ID:** Identifica cada ordenador dentro de la red.
- **Clases de Redes:**
    - Se dividen según el número de bits utilizados para la red (NetID) y los equipos (Host-ID).
    - **Clase A:**
        - Primer octeto para la red, 24 bits para los equipos.
        - Primer bit siempre a cero, lo que deja 7 bits para identificar redes (126 redes posibles).
        - Usos: Pocas redes con muchos equipos.
    - **Clase B:**
        - 16 bits para la red, 16 bits para los equipos.
        - Los dos primeros bits son 10, dejando 14 bits para identificar redes (16384 redes).
        - Usos: Redes de tamaño intermedio.
    - **Clase C:**
        - 24 bits para la red, 8 bits para los equipos.
        - Los tres primeros bits son 110, dejando 21 bits para identificar redes (2097152 redes).
        - Usos: Redes pequeñas.
    - **Clase D:**
        - Los primeros 4 bits son 1110.
        - Usos: Multidifusión de contenidos.
    - **Clase E:**
        - Los primeros 4 bits son 1111.
        - Usos: Investigación.

# Direcciones IP especiales 

- **Dirección de red:** Todos los bits del Host-ID son 0. Identifica la red (ej: 192.168.0.0 en una red clase C).
- **Dirección del equipo:** Todos los bits del NetID son 0.
- **Dirección de difusión:** Todos los bits del Host-ID son 1. Se usa para enviar un mensaje a todos los equipos de la red (ej: 192.168.0.255 en la red 192.168.0.0).
- **Dirección de bucle de retorno (loopback):** Hace referencia al propio equipo (127.0.0.1).
- **Direcciones IP de ámbito local:** Se utilizan cuando los equipos no tienen acceso directo a Internet y acceden a través de un proxy o pasarela. Evitan conflictos con las direcciones IP de Internet. Solo el dispositivo que actúa como pasarela necesita una dirección IP asignada por la ICANN.

# Mascara de red

- **Máscara de red:**
    - Formada por 32 bits, similar a una dirección IP.
    - Los bits del NetID son 1 y los del Host-ID son 0.
- **Función:**
    - Separa la parte de la dirección IP que identifica la red.
    - Se obtiene aplicando una operación lógica AND entre la dirección IP y la máscara de red.
- **Creación de subredes:**
    - Divide una red grande en subredes más manejables.
    - Controla el tráfico y reduce el ámbito de las operaciones de broadcast.
    - Se crean añadiendo bits a la máscara de red.
- **Ejemplo de creación de subredes:**
    - Red de clase B: 172.16.0.0 con máscara 255.255.0.0.
    - Dividir en cuatro subredes: tomar los dos primeros bits del tercer byte.
    - Nueva máscara: 255.255.192.0.
    - Cada subred admite 16382 ordenadores (2^14 - 2).
    - Se pierden dos direcciones por subred: la dirección de red y la dirección de difusión (broadcast).
- **Notación simplificada (CIDR):**
    - Dirección IP seguida de una barra inclinada (/) y el número de unos consecutivos en la máscara de red.
    - Ejemplo: 192.168.0.32 con máscara 255.255.255.0 se representa como 192.168.0.32/24.

# Protocolo TCP/IPV6

- **Necesidad de IPv6:**
    - IPv4 (32 bits) no es suficiente debido a direcciones reservadas, múltiples dispositivos por usuario y el auge del Internet de las Cosas.
- **Formación de una dirección IPv6:**
    - 128 bits, permitiendo 2^128 direcciones diferentes.
    - 8 campos de 16 bits separados por dos puntos (:).
    - Notación hexadecimal.
    - Ejemplo: 2001:0db8:ac10:0013:0000:0000:2b4e:0c11
- **Notación simplificada:**
    - Representar cuatro 0's como uno solo: 2001:0db8:ac10:0013:0:0:2b4e:0c11
    - Eliminar un campo completo de ceros (solo una vez por dirección): 2001:0db8:ac10:0013:::2b4e:0c11
    - Omitir los 0's a la izquierda dentro de un campo: 2001:db8::2b4e:c11
- **Partes de una dirección IPv6:**
    - **Prefijo del sitio:** Máximo 48 bits (3 primeros campos), parte pública de la dirección. Se expresa en notación CIDR (ej: 2001:db8:ac10::/48).
    - **Prefijo de subred:** 16 bits (cuarto campo), identifica la topología interna de la red. Se expresa en notación CIDR (ej: 2001:db8:ac10:13::/64).
    - **ID de la interfaz (Token):** 64 bits (últimos cuatro campos), puede ser asignado manualmente o derivado de la dirección MAC.
- **Tipos de configuración de IPv6:**
    - **Manual:** El administrador introduce los valores manualmente.
    - **Autoconfiguración (Sin Estado):** El equipo busca un router IPv6 que le proporcione el prefijo de subred y añade su dirección MAC en formato EUI-64 Modificado.
    - **Mediante un servidor (Con Estado):** Se utiliza un servidor DHCP.
- **Direcciones IPv6 con direcciones IPv4:**
    - Se pueden incrustar direcciones IPv4 en direcciones IPv6 para compatibilidad.
    - La dirección IPv6 se divide en dos partes: los 6 primeros campos en hexadecimal y los 4 últimos en notación decimal (IPv4).
    - Ejemplo: 0:0:0:0:0:ffff:192.1.1.25 o ::ffff:192.1.1.25/96.