# Extraction, part 1 of 3: identification and quality assessment (Claude Sonnet 5)

```text
Formas parte de un proyecto de revisión sistemática de literatura (SLR) sobre el uso de Inteligencia Artificial Generativa (IAG) en la enseñanza de Ingeniería de Software (SE/Programming/CS/Computing Education). Tu tarea es leer directamente UN artículo académico completo en PDF y realizar tu propia extracción estructurada de datos, actuando como analista experto en SLR.

NO consultes ni utilices extracciones previas, ni otros archivos del proyecto. El análisis debe ser independiente y basarse exclusivamente en tu lectura del PDF.

**Cómo leer el documento:** utiliza la herramienta Read sobre el PDF. Esta herramienta permite leer un máximo de 20 páginas por llamada. Si el artículo supera esa extensión, realiza las llamadas necesarias para cubrirlo completo. Por ejemplo, para un documento de 37 páginas, solicita pages="1-20" y luego pages="21-37". Lee el artículo COMPLETO, no solo el resumen, la introducción o las conclusiones.

Esta es la PARTE 1 de 3 de un análisis dividido en identificación y evaluación de calidad, preguntas de investigación y hallazgos adicionales. En esta parte, realiza únicamente la identificación y la evaluación de calidad (quality assessment).

**Reglas generales —aplicables a esta parte y a las siguientes—:**

* Utiliza únicamente el contenido del artículo cargado. Si falta un dato, indica N/E.
* Respalda cada afirmación con evidencia verificable: una cita textual breve entre comillas, en el idioma original del artículo, seguida de "Evidencia: p. X, secc. X".
* Nunca inventes números de página. Si no puedes precisar la página, utiliza el nombre de la sección o el encabezado visible, por ejemplo: "Evidencia: secc. Results". Si tampoco puedes identificarlo, indica: "Evidencia: N/E (no localizable en el texto)".
* Conserva los marcadores de cita, como [8] o [10,19], cuando aparezcan en el fragmento citado.
* Distingue siempre entre **afirma** (declaración no probada por el propio estudio, opinión de los autores o cita de otro trabajo) y **demuestra** (resultado empírico obtenido por el propio estudio).
* Distingue siempre entre **percepción** (autorreporte, encuesta u opinión) y **resultado objetivo** (medición, desempeño o dato cuantitativo directo).
* Prioriza la densidad de evidencia sobre la extensión del texto: sé conciso, pero completo.

**FORMATO DE SALIDA**

Presenta los siguientes campos en el orden indicado.

**IDENTIFICACIÓN Y CONTEXTO**

Registra cada dato de forma breve, sin explicaciones adicionales salvo que se soliciten.

Título:
Autores:
Año:
DOI:
Venue / Fuente:
País(es) / contexto del estudio:
Tipo de revisión (SLR, Systematic Review, Scoping Review, Mapping, etc.; incluye las directrices metodológicas si se citan):
Período cubierto (rango y fecha de búsqueda):
N.º de estudios incluidos:
Bases de datos / fuentes utilizadas:
Área educativa (SE / Programming / CS / Computing Education):
Nivel educativo (escolar, superior, etc.):

**QUALITY ASSESSMENT**

Para cada ítem, incluye: **Veredicto (Yes/Partially/No) — Justificación (1–2 frases) — Cita textual breve — Evidencia: p. X, secc. X.**

QA1. ¿Define claramente los objetivos y/o las preguntas de investigación?
QA2. ¿Describe una estrategia de búsqueda sistemática y reproducible, incluidos los términos o la cadena de búsqueda?
QA3. ¿Identifica claramente las bases de datos o fuentes y el período cubierto?
QA4. ¿Define explícitamente los criterios de inclusión y exclusión?
QA5. ¿Describe claramente el proceso de selección (screening) y las medidas para reducir el sesgo?
QA6. ¿Describe claramente la extracción de datos y el proceso de análisis o síntesis?
QA7. ¿Reporta los estudios y la evidencia con suficiente detalle para asegurar su trazabilidad?
QA8. ¿Los resultados y las conclusiones están respaldados por la evidencia sintetizada?
QA9. ¿Discute limitaciones, amenazas a la validez o fuentes de sesgo?

**Quality Score (0–10):** asigna Yes = 1, Partially = 0.5 y No = 0. Suma los valores de los nueve ítems y convierte el resultado a una escala de 0 a 10 mediante la fórmula: **(suma / 9) × 10**. Muestra el cálculo.

Los siguientes apartados definen los campos de la salida; no los presentes por separado.

Entrega una única tabla con estas columnas, en este orden:

Contenido | Valor | Cita_textual | Ubicación

Genera una fila para cada dato de identificación del artículo y una fila para cada QA (QA1–QA9).

Para los datos de identificación (Título, Autores, Año, DOI, Venue, País/contexto, Tipo de revisión, Período cubierto, N.º estudios, Bases de datos, Área educativa y Nivel educativo):

Contenido: solo su información, no pongas titulo.
Valor: N/A.
Cita_textual: N/A.
Ubicación: N/A.

Para QA1–QA9:

Contenido: incluye la justificación.
Valor: coloca únicamente el veredicto.
Cita_textual: cita textual que respalda el veredicto.
Ubicación: página, sección, tabla o apartado de la cita.

Al final agrega una fila para Quality Score, dejando el puntaje total en Valor.

No inventes citas ni ubicaciones. Devuelve únicamente la tabla.
```
