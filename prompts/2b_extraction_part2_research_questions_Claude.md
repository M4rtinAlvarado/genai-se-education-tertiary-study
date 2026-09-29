# Extraction, part 2 of 3: research questions (Claude Sonnet 5)

```text
Formas parte de un proyecto de revisión sistemática de literatura (SLR) sobre el uso de Inteligencia Artificial Generativa (IAG) en la enseñanza de Ingeniería de Software (SE/Programming/CS/Computing Education). Tu tarea es leer directamente UN artículo académico completo en PDF y realizar tu propia extracción estructurada de datos, actuando como analista experto en SLR.

NO consultes ni utilices extracciones previas, ni otros archivos del proyecto. El análisis debe ser independiente y basarse exclusivamente en tu lectura del PDF.

**Cómo leer el documento:** utiliza la herramienta Read sobre el PDF. Esta herramienta permite leer un máximo de 20 páginas por llamada. Si el artículo supera esa extensión, realiza las llamadas necesarias para cubrirlo completo. Por ejemplo, para un documento de 37 páginas, solicita pages="1-20" y luego pages="21-37". Lee el artículo COMPLETO, no solo el resumen, la introducción o las conclusiones.

Esta es la PARTE 2 de 3 de un análisis dividido en identificación y evaluación de calidad, preguntas de investigación y hallazgos adicionales. En esta parte, aborda únicamente las preguntas de investigación del proyecto, priorizando la profundidad y la trazabilidad del análisis. No entregues un resumen genérico.

**Reglas generales —aplicables a esta parte y a las demás—:**

* Utiliza únicamente el contenido del artículo cargado. Si falta un dato, indica N/E.
* Respalda cada afirmación con evidencia verificable: una cita textual breve entre comillas, en el idioma original del artículo, seguida de "Evidencia: p. X, secc. X".
* Nunca inventes números de página. Si no puedes precisar la página, utiliza el nombre de la sección o el encabezado visible. Si tampoco puedes identificarlo, indica: "Evidencia: N/E (no localizable en el texto)".
* Conserva los marcadores de cita, como [8] o [10,19], cuando aparezcan en el fragmento citado.
* Distingue siempre entre afirma y demuestra.
* Distingue siempre entre percepción y resultado objetivo.
* Si el artículo no cubre una RQ, indícalo explícitamente: "No cubierta en este artículo". No fuerces una respuesta ni la infieras de otra sección.
* Prioriza la densidad de evidencia sobre la extensión del texto.

**FORMATO DE SALIDA**

**PREGUNTAS DE INVESTIGACIÓN DEL PROYECTO**

Para cada RQ, incluye los siguientes campos en este orden:

1. Cobertura: Alta/Media/Baja/Nula.
2. Síntesis: entre 2 y 4 frases en español.
3. Cita(s) textuales relevantes: entre comillas, en el idioma original y con los marcadores [n] cuando aparezcan en el fragmento citado.
4. Afirma vs. demuestra.
5. Percepción vs. resultado objetivo. Si no corresponde, indica N/A.
6. Evidencia: p. X, secc. X.

**RQ1:** Identificar en qué actividades de enseñanza o aprendizaje de Ingeniería de Software se utiliza IAG (programación, depuración, diseño, requisitos, pruebas, documentación, tutoría, retroalimentación, resolución de problemas, etc.).

**RQ2:** Identificar qué estrategias didácticas se utilizan en la enseñanza de Ingeniería de Software y explicar cómo se incorpora la IAG en ellas.

**RQ3:** Identificar qué efectos del uso de IAG se reportan sobre los resultados de aprendizaje relacionados con la Ingeniería de Software.

**RQ4:** Identificar qué métodos o estrategias de evaluación del aprendizaje son modificados, apoyados o realizados mediante IAG.

**RQ5:** Identificar los beneficios, riesgos y limitaciones pedagógicas reportados sobre el uso de IAG en la enseñanza de Ingeniería de Software.

**RQ6:** Identificar los vacíos de investigación encontrados en la literatura, las limitaciones de la evidencia existente y los temas que los autores señalan como necesarios para futuras investigaciones.

**RQ7:** Identificar qué competencias o habilidades de Ingeniería de Software se consideran menos susceptibles de ser automatizadas por IAG y qué estrategias educativas se proponen para fortalecerlas.

Entrega una única tabla con estas columnas, en este orden:

| Contenido | Valor | Cita_textual | Ubicación |

Genera una fila por cada RQ (RQ1 a RQ7).

En **Contenido** escribe en una sola celda:

la síntesis de la RQ, indicando además si el estudio afirma o demuestra y si la evidencia corresponde a percepción o a resultados objetivos.
integrar los 3 campos en la celda «Contenido» de cada RQ, después de la síntesis y separados por saltos de línea:
Síntesis: [Respuesta a la RQ].
 Afirma vs. demuestra: [Clasificación y explicación].
 Percepción vs. resultado objetivo: [Clasificación y explicación, o N/A].


En **Valor** incluye la cobertura de la RQ, 

En **Cita_textual** incluye las citas que respaldan el análisis.

En **Ubicación** indica página, sección, tabla o apartado de cada cita.

Si una RQ no está cubierta, indícalo claramente. No inventes información, citas ni ubicaciones. Devuelve únicamente la tabla.
```
