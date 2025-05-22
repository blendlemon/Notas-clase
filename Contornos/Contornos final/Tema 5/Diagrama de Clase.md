#### **Introducción a UML**

- **UML (Unified Modeling Language)**: Estándar para modelar sistemas orientados a objetos, creado en 1997 por Booch, Rumbaugh y Jacobson.
    
- **Propósito**: Facilitar la comunicación en equipos de desarrollo mediante representaciones visuales estandarizadas.
    
- **Tipos de Diagramas**:
    
    - **Estructurales** (clases, componentes, paquetes).
        
    - **Comportamiento** (secuencia, casos de uso).
        

---

#### **Diagramas de Clase**

**Definición**: Representan la estructura estática de un sistema mediante **clases**, **atributos**, **métodos** y **relaciones**.

**Elementos Principales**:

1. **Clase**:
    
    - **Notación**: Rectángulo con tres secciones (nombre, atributos, métodos).
        
    - **Ejemplo**:
        

2. - +---------------------+
        |      Persona        |
        +---------------------+
        | - nombre: String    |
        | - edad: int         |
        +---------------------+
        | + caminar()         |
        | + hablar()          |
        +---------------------+
        
    - **Visibilidad**: `+` (público), `-` (privado), `#` (protegido).
        
3. **Atributos**:
    
    - Formato: `visibilidad nombre: tipo [= valor por defecto]`.
        
    - Ejemplo: `- saldo: double = 0.0`.
        
4. **Métodos**:
    
    - Formato: `visibilidad nombre(parámetros): tipoRetorno`.
        
    - Ejemplo: `+ depositar(monto: double): void`.
        

---

#### **Relaciones entre Clases**

|**Tipo**|**Símbolo**|**Descripción**|**Ejemplo**|
|---|---|---|---|
|**Asociación**|`─────`|Conexión básica entre clases. Puede tener multiplicidad (`1`, `*`, `0..1`).|`Cliente ───── Pedido` (1..*)|
|**Herencia**|`─────▷` (flecha hueca)|Relación "es-un" (generalización). Subclase hereda de superclase.|`Empleado ▷ Persona`|
|**Agregación**|`─────◇` (rombo hueco)|Relación "tiene-un" débil. El objeto parte puede existir sin el todo.|`Biblioteca ◇── Libro`|
|**Composición**|`─────◆` (rombo relleno)|Relación "tiene-un" fuerte. El objeto parte no existe sin el todo.|`Casa ◆── Habitación`|
|**Dependencia**|`⤳` (línea discontinua)|Una clase usa temporalmente otra (ejemplo: parámetro en un método).|`Factura ⤳ Producto`|

**Multiplicidad**:

- `1`: Exactamente uno.
    
- `*` o `0..*`: Cero o más.
    
- `1..*`: Uno o más.
    

---

#### **Conceptos Avanzados**

- **Clases Abstractas**:
    
    - No instanciables. Métodos abstractos (sin implementación).
        
    - Notación: Nombre en _cursiva_.
        
- **Interfaces**:
    
    - Contratos con métodos abstractos.
        
    - Notación: `<<interface>>` o círculo.
        
- **Asociaciones Reflexivas**: Una clase se relaciona consigo misma (ejemplo: `Empleado` supervisa a `Empleado`).
    

---

#### **Recomendaciones para Diseño**

1. **Identificar Clases**:
    
    - Sustantivos en requisitos → Clases.
        
    - Verbos → Métodos.
        
2. **Evitar Clases "Dios"**: Dividir responsabilidades.
    
3. **Usar Paquetes**: Agrupar clases relacionadas para modularidad.
    

---

#### **Diagramas de Objetos**

- **Propósito**: Mostrar instancias específicas de clases en tiempo de ejecución.
    
- **Notación**:
    

lavadoraCasa:Lavadora
[marca="Bosch", capacidad=10.5]