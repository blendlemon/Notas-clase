# Teoría sobre Diseño y Realización de Pruebas

# El testing

Las pruebas de software son investigaciones técnicas que buscan evaluar la calidad de un producto de software, proporcionando información objetiva a los interesados. Son parte del control de calidad y varían según el modelo de desarrollo utilizado.

Su objetivo no es garantizar que el software no tenga defectos, sino identificar errores de manera eficiente, diseñando pruebas que detecten fallos con el menor tiempo y esfuerzo posibles. En resumen, las pruebas ayudan a encontrar problemas, pero no aseguran que el software sea perfecto.

# Características:
	1. Efectividad: Debe tener alta probabilidad de detectar fallos
	2. Doble enfoque:
		1. Verificar que el software no hace lo que debería hacer.
		2. Asegurar que no hace lo que no debería hacer.
	3. No redundante: Cada prueba debe tener un propósito único para optimizar tiempo y recursos
	4. Óptima: Debe ser la prueba con mayor probabilidad de detectar una categoría completa de errores
	5. Equilibrada: Ni demasiado simple ni demasiado compleja, lo ideal es ejecutarlas de forma independiente
	Objetivo: Maximizar la detección de errores con el menor esfuerzo posible.

# Importancia de las pruebas de software
	- Verificar que el software cumple con los requisitos
	- Validar que el producto final es el esperado
	- Aumentar la confianza
	- Detectar y prevenir fallos
	- Informar al cliente
- Beneficios clave:
	- Reducción de costos y plazos
	- Menos riesgos
	- Mayor calidad

# Contexto clásico de las pruebas de software:
- Ejecución controlado
	- El software se prueba bajo configuraciones especificas
	- se registran los resultados obtenidos
- Evaluación
	- Se comparan los resultados reales vs esperados para identificar fallos
- Depuración
	- Se localiza y corrige el error asociado al fallo
	- Puede requerir nuevas pruebas tras la corrección
- Resultado final
	- Predicción de fiabilidad
	- Nivel de confianza
- Ciclo clave: Prueba -> Evaluación-> Depuración-> Nueva prueba (si es necesario)

# Fases de las pruebas del software

1. Diseño de las Pruebas
	- Identificar las técnicas de prueba más adecuadas según el contexto.
	- Cada técnica evalúa diferentes aspectos del software.
2. Generación de Casos de Prueba
	- Definir entradas, condiciones de ejecución y resultados esperados.
	- Cada técnica sugiere distintos criterios para crear casos de prueba
	- Cada caso debe incluir el resultado esperado para validar el comportamiento.
3. Definición de los Procedimientos
	- Establecer cómo, quién y cuándo se ejecutarán las pruebas.
	- Planificar recursos, entorno y responsables.
4. Ejecución de las Pruebas
	- Aplicar los casos de prueba y comparar resultados reales vs esperados
	- Registrar fallos detectados.
5. Informe de Resultados
	- Documentar qué pruebas pasaron/fallaron y los defectos encontrados.
	- Proporcionar métricas de calidad al equipo y stakeholders.
6. Depuración
	- Corregir los errores identificados.
	- Volver a probar (regresión) para confirmar las correcciones

# Nuevos Paradigmas: TDD y BDD

Test-Driven Development(TDD)

Enfoque: Escribir pruebas antes que el código.
Pasos:
1. Escribir una prueba (falla inicialmente)
2. Implementar el código mínimo para que la prueba pase.
3. Refactorizar (mejorar el código sin cambiar su funcionalidad)
- Ventajas
	- Evita código innecesario
	- Aumenta la confianza en el software
	- Facilita la integración continua
Behavior-Driven Development (BDD)

Origen: Extiende TDD con un enfoque en el comportamiento esperado
Características:
- Usa lenguaje natural para definir pruebas
- Fomenta la colaboración entre desarrolladores, testers y negocio
- Combina TDD, fiseño orientado a dominio y OOP.
Objetivo: 
- Asegurar que el software cumple con los requisitos del negocio, no solo con pruebas técnicas

Conclusión
- Las pruebas tradicionales siguen un flujo estructurado (diseño-> ejecución -> informe)
- TDD y BDD son metodologías ágiles que integran pruebas desde el inicio, mejorando la calidad y alineación con los requisitos
- TDD se centra en pruebas técnicas; BDD en el comportamiento y la comunicación con stakeholders.

# Error, Defecto y Fallo

- Error: Equivocación humana (ej: código mal escrito)
- Defecto: El error se convierte en  un bug en el software
- Fallo: Cuando el defecto se ejecuta y causa un mal funcionamiento
Causas comunes:
- Presión, falta de experiencia, mala comunicación, complejidad, tecnologías nuevas

# Niveles de Testing

1. Unit Testing
	- Objetivo: Verificar el funcionamiento de unidades individuales (métodos, clases, funciones).
	- Responsable: Desarrolladores (a veces QAs)
	- Enfoque: Pruebas de caja blanca o TDD.
	- Ventajas:
		- Detecta errores temprano
		- Facilita el mantenimiento y depuración
		- Reduce costos de corrección

2. Integration Testing
	- Objetivo: Validar la comunicación entre módulos
	- Responsable: Desarrolladores o equipos externos
	- Enfoque: Caja negra, blanca o gris
	- Estrategias: Big Bang, Top-Down, Bottom-Up, Híbrido.

3. System Testing
	- Objetivo: Evaluar el sistema completo (end-to-end)
	- Responsable: QAs especializados
	- Tipos:
		- Funcionales (cumplimiento de requisitos)
		- No funcionales (rendimiento, usabilidad)
	- Ventajas
		- Valida experiencia de usuario
		- Reduce errores en producción

4. Acceptance Testing
	- Objetivo: Validar que el producto cumple con las expectativas del cliente
	- Responsable: Cliente o usuarios finales (con apoyo de QAs)
	- Tipos:
		- UAT (User Acceptance Testing).
		- BAT (Business Acceptance Testing)
		- Beta/Alfa Testing (pruebas en entorno real)
	- Resultado: Decisión GO/NO GO para producción

Resumen
- Unit -> Integration -> System -> Acceptance
- Cada nivel validad desde componentes individuales hasta el sistema completo y su aceptación por el cliente
- Involucra a desarrolladores, QA y stakeholders clave.

# Tipos de Prueba de Software

1. Pruebas Funcionales

Objetivo: Verificar que el sistema cumple con sus requisitos funcionales (documentados o no)

- Enfoque: Pruebas de caja negra (sin conocer código interno).
- Ejecución
	- Manual: Un tester simula acciones de usuario siguiendo un plan de pruebas.
	- Automáticas: se automatizan casos críticos (happy paths) para validar regresiones.

2. Pruebas No Funcionales

Objetivo: Evaluar atributos de calidad como rendimiento, seguridad o usabilidad.

- Tipos:
	- Rendimiento (carga, estrés)
	- Seguridad (vulnerabilidades)
	- Usabilidad (experiencia de usuario)
	- Compatibilidad (navegadores, dispositivos)
- Estándares: ISO 25000 (SQuaRE) para métricas de calidad

3. Pruebas Regresivas

Objetivo: Asegurar que cambios nuevos no rompan funcionalidades existentes.

 - Recomendación: Automatizar para eficiencia.
 - Foco: Validar casos de prueba previos tras actualizaciones.

Resumen:
- Funcionales: ¿Hace lo que debe hacer? (Manual/Automático)
- No funcionales: ¿Cómo lo hace? (Rendimiento, seguridad, etc.).
- Regresivas: ¿Sigue funcionando después de los cambios?

# Caja Blanca

Las pruebas de caja blanca se centran en analizar la estructura interna del software, incluyendo el código, flujos de control, estructuras de datos y lógica interna. Requieren acceso al código fuente y conocimientos de programación.

**Objetivos de las Pruebas de Caja Blanca**
- Detectar problemas de seguridad internos
- Evaluar la calidad del código
- Verificar el flujo de ejecución para diferentes entradas
- Comprobar el funcionamiento de bucles y condiciones
- Probar individualmente declaraciones, objetos y funciones

**Proceso Iterativo**
1. Entender el código fuente
2. Crear casos de prueba
3. Ejecutar los casos de prueba

**Criterios de cobertura**

1. **Cobertura de Sentencias**: Ejecutar cada sentencia al menos una vez
2. **Cobertura de Decisión**: Probar cada condición (verdadero y falso)
3. **Cobertura de Condiciones**: Cada subcondición dentro de una decisión debe evaluarse como verdadera y falsa.
4. **Cobertura Decisión/Condición**: Combinación de cobertura de decisiones y condiciones.
5. **Cobertura de Caminos**: Ejecutar todos los caminos posibles del programa

**Cobertura de Caminos y Complejidad Ciclomática (McCabe)**

- Técnica para garantizar que se prueban todos los caminos posibles
- **Pasos**:
	1. **Representar el programa como un grafo de flujo**
	2. **Calcular la complejidad ciclomática**
	3. **Identificar caminos básicos independientes**
	4. **Generar casos de prueba**

**Elementos del Grafo de Flujo**:
- **Nodos**
- **Aristas**
- **Regiones**: Áreas delimitadas por nodos y aristas
- **Nodos predicado**: Nodos que representan condiciones lógicas (AND, OR, etc.)

Estas técnicas permiten diseñar pruebas más exhaustivas y detectar errores ocultos en la lógica interna del software

**Complejidad Ciclomática**

Es una métrica que mide la complejidad lógica de un programa y determina el número de **caminos independientes** necesarios para probarlo

**Métodos de Cálculo:**

1. **Número de reginoes del grafo**: `V(G) = Nº de regiones`
2. **Fórmula de aristas y nodos**: `V(G) = Aristas - Nodos + 2`
3. **Nodos predicado**: `V(G) = Nodos Predicado + 1`

**Conjunto Básico de Caminos Independientes**

- Cada camino debe incluir al menos una **nueva aristas o condición** no explorada antes
- **Heurísticas para definirlos:**
	1. Elegir un **camino principal** que cubra la mayor cantidad de decisiones
	2. Alternar el resultado de la **primera decisión** en el camino base
	3. Modificar la **segunda decisión** manteniendo las demás igual
	4. Repetir hasta cubrir todas las decisiones

**Derivación de Casos de Prueba**

Se diseñan pruebas específicas para forzar la ejecución de cada **camino independiente**, asegurando cobertura de sentencias y decisiones

**Otras Técnicas de Prueba de Caja Blanca**

1. **Prueba de Interfaz**
	- Verifica el flujo de datos entre módulos (entradas/salidas)
	- Asegura que los parámetros se pasan correctamente
2. **Prueba de Estructuras de Datos Locales**
	- Valida la integridad de variables y estructuras internas durante la ejecución
3. **Prueba del Camino Básico**
	- Basada en la **complejidad ciclomática** para definir casos de prueba
4. **Prueba de Bucles**
	- Evalúa la correcta implementación de bucles

**Técnicas para Prueba de Bucles**

1. **Bucles Simples**
	- **Casos de prueba:**
		- Saltar el bucle
		- 1 iteración
		- 2 iteraciones
		- m iteraciones (m<n)
		- n-1, n, n+1 iteraciones
2. **Bucles Anidados**
	- **Enfoque**
		- Probar desde el **bucle más interno** hacia fuera
		- Fijar bucles externos en **valores mínimos** mientras se prueba el interno
3. **Bucles Concatenados**
	- **Si son independientes**: Probar como bucles simples
	- **Si son dependientes**: Tratar como bucles anidados
4. **Bucles No Estructurados**
	- **Solución**: Rediseñar para usar estructuras de control estándar

**Conclusión**
- La **complejidad ciclomática** ayuda a determinar el número mínimo de pruebas necesarias
- Las **pruebas de bucles** son esenciales para validar algoritmos iterativos
- Combinar estas técnicas asegura una **cobertura efectiva** del código 

# Caja Negra

**Definición de Pruebas de Caja Negra**

- Se enfoca en probar la **funcionalidad del software** sin conocer su estructura interna
- Basada en **requisitos y especificaciones**, no en el código

**Técnicas de Prueba de Caja Negra**
1. **Partición de Equivalencia**
	- Divide los datos de entrada en **clases de equivalencia**
	- Prueba un **valor representativo** de cada clase (si uno falla, toda la clase puede fallar)
2. **Análisis de Valores Límite**
	- Prueba valores en los **bordes** de las clases de equivalencia
	- Ejemplo:  Si el rango válido es `n <= i <= m`, se prueban:
		- `n-1` (inválido), `n` (válido), `n+1` (válido)
		- `m-1` (válido), `m` (válido), `m+1` (inválido)
3. **Grafos Causa-Efecto**
	- Modela relaciones entre **entradas (causas) y salidas (efectos)**
	- Útil para probar combinaciones complejas de condiciones
4. **Pruebas de Casos de Uso**
	- Simulan **escenarios reales de usuario** para validar el flujo de trabajo
5. **Dirigidas por Sintaxis**
	- Valida el **formato de entrada**

**Comparación: Caja Blanca vs. Caja Negra**


| **Aspecto**      | **Caja Blanca**                           | **Caja Negra**                            |
| ---------------- | ----------------------------------------- | ----------------------------------------- |
| **Enfoque**      | código                                    | Funcionalidad                             |
| **Conocimiento** | Requiere acceso al código                 | No necesita conocer el código             |
| **Técnicas**     | Cobertura de caminos, bucles, condiciones | Partición de equivalencia, valores límite |
| **Objetivo**     | Detectar errores de lógica                | Validar comportamiento esperado           |

**Prueba Basadas en Experiencia**

1. **Alpha Testing**
	- Realizado **internamente** por el equipo de desarrollo o QA
	- Objetivo: **Simular usuarios reales** antes del lanzamiento
	- Combina técnicas de **caja negra y blanca**
2. **Beta Testing**
	- Realizado por **usuarios reales** en un entorno real
	- Tipos
		- **Tradicional**: Feedback del mercado objetivo
		- **Público**: Cualquier usuario puede probar
		- **Técnico**: Pruebas internas de las organización
		- **Enfocado**: Validar características específicas
		- **Post-Lanzamiento**: Mejoras para futuras verisones

**Organización de Casos de Prueba**
- **Objetivos**
	- Facilitar la comprensión y priorización
	- Optimizar pruebas de regresión
	- Mejorar la escalabilidad y la calidad del proyecto

**Conclusiones**

1. Las pruebas son clave para garantizar la **calidad del software**
2. La **documentación** mejora el mantenimiento y evolución del producto
3. **Alpha y Beta Testing** ayudan a detectar errores antes y después del lanzamiento

**En resumen:**

- **Caja negra** = Validar qué hace el software
- **Caja blanca** = Validar cómo lo hace
- **Pruebas de experiencia** = Validar usabilidad en entornos reales