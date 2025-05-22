### Introducción

El conjunto de diagramas de UML se subdivide en dos grandes subconjuntos: **diagramas estructurales** y **diagramas de comportamiento**.

- **Diagramas estructurales**: muestran los elementos estáticos del modelo (clases, paquetes, componentes).
    
- **Diagramas de comportamiento**: reflejan la conducta en tiempo de ejecución del sistema, tanto a nivel global como a nivel de instancias u objetos.
    

### Tipos de Diagramas de Comportamiento

Los diagramas de comportamiento modelan el comportamiento dinámico del sistema ante estímulos externos, eventos internos y cambios de estado. Se clasifican en:

- **Diagrama de casos de uso**: representa los requisitos funcionales del sistema y los actores que interactúan con él.
    
- **Diagrama de secuencia**: muestra la secuencia cronológica de interacciones entre objetos.
    
- **Diagrama de actividad**: refleja el flujo de actividades o acciones para alcanzar un objetivo.
    
- **Diagrama de estado**: describe los estados de un objeto y las transiciones entre ellos.
    
- **Diagrama de comunicación**: destaca las interacciones entre objetos sin centrarse en el tiempo.
    
- **Diagrama de tiempos**
    
- **Diagrama global de interacciones**
    

### Diagramas de Interacción

Son un subtipo de diagramas de comportamiento que ilustran cómo interactúan los objetos entre sí:

- **Diagramas de secuencia**: representan la secuencia de mensajes entre objetos a lo largo del tiempo.
    
- **Diagramas de comunicación**: enfatizan las relaciones entre objetos y los mensajes enviados.
    
- **Diagramas de tiempo**
    
- **Diagrama de interacción global**
    

### Diagramas de Actividad

#### Introducción

Representan la ejecución de actividades o acciones. Las transiciones se disparan al finalizar la ejecución de estas.

- **Estados**: atómicos, representan condiciones.
    
- **Actividades**: divisibles, representan procesos.
    

#### Usos

- Modelar procesos de negocio.
    
- Describir casos de uso.
    
- Representar métodos o funciones.
    

#### Elementos

- **Actividad/Acción**: rectángulo con bordes redondeados o cápsula.
    
- **Transición**: flechas entre actividades.
    
- **Bifurcación**: rombos con condiciones de guardia.
    
- **Divisiones/Uniones**: barras para ejecución paralela.
    
- **Particiones**: para agrupar acciones por actor o característica común.
    

#### Recomendaciones

1. Seleccionar operaciones clave a modelar.
    
2. Definir inicio y fin del ciclo.
    
3. Observar la operación y dividirla en elementos.
    

### Diagramas de Casos de Uso

#### Definición

Modelan los requisitos funcionales desde la perspectiva del usuario. Representan interacciones entre actores y el sistema.

#### Componentes

- **Actores**: stickman.
    
- **Casos de uso**: elipses.
    
- **Relaciones**: asociación, generalización, inclusión.
    
- **Sistema**: rectángulo contenedor.
    

#### Características

- Describen funcionalidades desde el punto de vista del usuario.
    
- Documentación en la fase de análisis.
    
- Relaciones: Include, Extends, Generalización.
    

### Diagramas de Máquina de Estados

#### Introducción

Muestran los diferentes estados de un objeto y cómo transiciona entre ellos según eventos recibidos.

#### Elementos

- **Estados**: con nombre, atributos y acciones (entry, exit, do).
    
- **Transiciones**: flechas con eventos y condiciones de guardia.
    

#### Ejemplo

- **Ascensor**: sube o baja según eventos, temporizador reinicia en estado parado.
    
- **Llamada telefónica**: distintos estados según eventos recibidos.
    

#### Características

- Modelan comportamiento discreto.
    
- Representan protocolos de uso y comportamiento de objetos.
    

### Diagramas de Secuencia

#### Características

- Representan el intercambio de mensajes entre objetos a lo largo del tiempo.
    
- Tres tipos de mensajes: simples, sincrónicos, asincrónicos.
    

#### Construcción

- **Horizontal**: objetos participantes.
    
- **Vertical**: línea de tiempo de ejecución.
    

#### Elementos

- **Objeto**: rectángulo con línea de vida.
    
- **Mensaje**: flecha con nombre y argumentos.
    
- **Respuesta**: flecha discontinua.
    

### Diagramas de Comunicación

#### Características

- Interacción entre líneas de vida con énfasis en la estructura interna.
    
- La secuencia se da mediante numeración.
    
- Muestran qué objetos interactúan, qué mensajes se envían y en qué orden.
    
- Equivalentes a diagramas de secuencia pero con diferente representación visual.