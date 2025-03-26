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