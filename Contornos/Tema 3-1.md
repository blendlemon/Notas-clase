# Introducción al Testing

- **Definición**: Proceso de evaluar el software para determinar su calidad, verificando que cumpla con los requisitos funcionales y no funcionales
- **Fase clave** en el ciclo de vida del desarrollo, aunque en metodologías ágiles se integra iterativamente
- **No siempre requiere conocimientos profundos de programación**, pero ayuda a realizar pruebas más exhaustivas.

**Rol del QA Tester (Quality Assurance)**
- **Objetivo**: Asegurar la calidad del software mediante pruebas sistemáticas
- **Funciones**:
	- Diseñar y ejecutar pruebas
	- Detectar errores antes del lanzamiento
	- Verificar el cumplimiento de estándares y requisitos
- **No es obligatorio saber programar**, pero facilita la identificación de bugs y la colaboración con desarroladores
# Objetivos del Testing

1. **Validar requisitos**: Confirmar que el software cumple con lo solicitado por el cliente
2. **Completitud**: Asegura que todos los requisitos están implementados
3. **Confianza en el desarrollo**: Detectar errores tempranos para reducir riesgos
4. **Prevención de errores futuros**: Mejorar la calidad del código
5. **Detección de fallos**: Identificar bugs en etapas iniciales
6. **Reduccioón de riesgos**: Minimizar problemas en producción
7. **Reporte de calidad**: Informar al cliente sobre el estado del software

# Importancia del Testing
- **Ahorro de costos**
- **Seguridad**
-   **Satisfacción del cliente**

# Conceptos Clave
- **Error vs Defecto vs Fallo**
	- **Error** : Equivocación humana
	- **Defecto:** Manifestación del error en el software
	- **Fallo**: Cuando el defecto se ejecuta y causa un mal funcionamiento
- **Causas de errores**: Lógica incorrecta, factores externos

# 7 Principios del Testing

1. **Muestra defectos, no su ausencia**
2. **Pruebas exhaustivas son imposibles**
3. **Testing temprano ahorra tiempo y dinero**
4. **Los defectos se agrupan**
5. **Paradoja del pesticida:** Las pruebas repetitivas pierden efectividad
6. **Depende del contexto**
7. **Ausencia de errores es una falacia**

# Calidad del Software

- **Definición:** Cumplimiento de requisitos funcionales, estándares de desarrollo y expectativas de usuario
- **Indicadores de baja calidad**
	- Incumplimiento de requisitos
	- Errores críticos
	- Dificultad de uso o mantenimiento
- **Enfoque**
	- **Verificación**: ¿Se construyó correctamente?
	- **Validación:** ¿Es el producto correcto?

# Normalización y Certificación

- **Estandarización**(ISO, IEC, AENOR)
	- Simplifica procesos y unifica criterios internacionales
	- Ejemplo: Normas **ISO 9000** (gestión de calidad) o **ISO/IEC 25010** (calidad de software)
- **Certificación**
	- Voluntaria, demuestra cumplimiento de estándares
	- Ejemplo: **Sello de AENOR** en España

# Tipos de Pruebas

1. **Pruebas Unitarias**
	- Prueban módulos individuales
	- Enfoque: **Caja blanca + Caja negra**
	- Herramientas: **JUnit, NUnit, PyTest**
2. **Pruebas de Integración**
	- Verifican la interacción entre módulos ya probados
	- Estrategias:
		- **Incremental** (ascendente/descendente)
		- **Big Bang** (integración total de una vez)

# Conclusión

- El testing es esencial para garantizar software funcional, seguro y de calidad.
- Combina técnicas técnicas (caja blanca/negra) y basadas en experiencia (Alpha/Beta Testing).
- La automatización y la normalización (ISO, IEEE) optimizan el proceso.
- Objetivo final: Entregar un producto que cumpla con las expectativas del usuario y minimice riesgos en producción.