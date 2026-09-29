# Extraction, part 3 of 3: additional findings (Claude Sonnet 5)

```text
Formas parte de un proyecto de revisión sistemática de literatura (SLR) sobre el uso de Inteligencia Artificial Generativa (IAG) en la enseñanza de Ingeniería de Software (SE/Programming/CS/Computing Education). Tu tarea es leer directamente UN artículo académico completo en PDF y realizar tu propia extracción estructurada de datos, actuando como analista experto en SLR.

NO consultes ni utilices extracciones previas, ni otros archivos del proyecto. El análisis debe ser independiente y basarse exclusivamente en tu lectura del PDF.

**Cómo leer el documento:** utiliza la herramienta Read sobre el PDF. Esta herramienta permite leer un máximo de 20 páginas por llamada. Si el artículo supera esa extensión, realiza las llamadas necesarias para cubrirlo completo. Por ejemplo, para un documento de 37 páginas, solicita pages="1-20" y luego pages="21-37". Lee el artículo COMPLETO, no solo el resumen, la introducción o las conclusiones.

Esta es la PARTE 3 de 3 de un análisis dividido en identificación y evaluación de calidad, preguntas de investigación y hallazgos adicionales. En esta parte, aborda únicamente los hallazgos y el contenido adicional. Complementa lo ya cubierto en las RQ, sin repetirlo.

**Reglas generales —aplicables a esta parte y a las demás—:**

* Utiliza únicamente el contenido del artículo cargado. Si falta un dato, indica N/E.
* Respalda cada afirmación con evidencia verificable: una cita textual breve entre comillas, en el idioma original del artículo, seguida de "Evidencia: p. X, secc. X".
* Nunca inventes números de página. Si no puedes precisar la página, utiliza el nombre de la sección o el encabezado visible. Si tampoco puedes identificarlo, indica: "Evidencia: N/E (no localizable en el texto)".
* Conserva los marcadores de cita, como [8] o [10,19], cuando aparezcan en el fragmento citado.
* Distingue siempre entre afirma y demuestra.
* Distingue siempre entre percepción y resultado objetivo.
* Prioriza la densidad de evidencia sobre la extensión del texto.

**FORMATO DE SALIDA**

**HALLAZGOS Y CONTENIDO ADICIONAL**

Los siguientes apartados definen los campos de la matriz final; no los presentes por separado:

* Herramientas o tecnologías de IAG mencionadas: nombre y uso en el estudio.
* Marcos teóricos o modelos pedagógicos citados.
* Instrumentos de evaluación o medición utilizados en los estudios primarios.
* Definiciones o conceptualizaciones relevantes: por ejemplo, qué se entiende por “IAG”, “competencia” o “pensamiento computacional”.
* Recomendaciones para docentes o instituciones.
* Citas textuales adicionales de interés.
* Otros hallazgos o datos útiles para el proyecto.

Los siguientes apartados definen los campos de la salida; no los presentes por separado.

Entrega una única tabla con estas columnas, en este orden:

Contenido | Valor | Cita_textual | Ubicación

Genera una fila para cada uno de estos campos:

* Herramientas/tecnologías de IAG mencionadas
* Marcos teóricos/modelos pedagógicos citados
* Instrumentos de evaluación/medición en estudios primarios
* Definiciones o conceptualizaciones relevantes
* Recomendaciones para docentes/instituciones
* Citas textuales adicionales de interés
* Otros hallazgos o datos útiles

Para cada fila:

* Contenido: incluye el contenido del hallazgo, seguido de **Afirma vs. demuestra:** y **Percepción vs. resultado objetivo:** en la misma celda.
* Valor: N/A.
* Cita_textual: incluye las citas textuales que respaldan el contenido.
* Ubicación: página, sección, tabla o apartado correspondiente.

No inventes información, citas ni ubicaciones. Devuelve únicamente la tabla.
```
