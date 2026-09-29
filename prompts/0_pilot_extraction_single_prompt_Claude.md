# Pilot extraction with a single integrated prompt (Claude Sonnet 5)

Used to refine the template and to select the snowballing seeds.

Actúa como asistente experto en revisiones sistemáticas de literatura (SLR) de ingeniería de
software y educación. Del paper cargado, produce un análisis exhaustivo, denso en evidencia, que
sirva a la vez de (a) evaluación profunda de calidad (Quality Assessment) y de cobertura de las
Research Questions (RQ) del proyecto, y (b) matriz de contenido temático adicional del proyecto.

Reglas generales:
- Usa solo el contenido del paper cargado. Si falta un dato: `N/E`.
- Toda afirmación debe llevar evidencia verificable: cita textual breve entre comillas, en el
  idioma original del paper, más `Evidencia: p. X, secc. X`.
- Nunca inventes un número de página. Si no puedes precisarlo, usa el nombre de la
  sección/encabezado visible (ej. `Evidencia: secc. Results`). Si ni eso es identificable:
  `Evidencia: N/E (no localizable en el texto)`.
- Conserva marcadores de cita tipo `[8]`, `[10,19]` si el paper los usa.
- Distingue siempre **afirma** (declaración no probada por el propio estudio, opinión de autores o
  cita de otro trabajo) de **demuestra** (resultado empírico obtenido por el propio estudio).
- Distingue siempre **percepción** (autorreporte, encuesta, opinión) de **resultado objetivo**
  (medición, desempeño, dato cuantitativo directo).
- Si una RQ no está cubierta por el paper, dilo explícitamente: `No cubierta en este paper` — no la
  fuerces ni la infieras de otra sección.
- Prioriza densidad de evidencia sobre extensión de prosa: sé conciso pero completo.

## FORMATO DE SALIDA (respetar este orden exacto)

### IDENTIFICACIÓN Y CONTEXTO (trazabilidad — una línea por campo, sin elaborar salvo que se indique)

Título:
Autores:
Año:
DOI:
Venue / Fuente:
País(es)/contexto del estudio:
Tipo de revisión (SLR, Systematic Review, Scoping Review, Mapping, etc. + directrices metodológicas si se citan):
Período cubierto (rango + fecha de búsqueda):
N.º de estudios incluidos:
Bases de datos/fuentes utilizadas:
Área educativa (SE / Programming / CS / Computing Education):
Nivel educativo (escolar, superior, etc.):

### QUALITY ASSESSMENT

Para cada ítem: **Verdicto** (Yes/Partially/No) — **Justificación** (1-2 frases) — **Evidencia: p. X, secc. X**.

QA1. ¿Define claramente objetivos y/o preguntas de investigación?:
QA2. ¿Describe una estrategia de búsqueda sistemática y reproducible, incluyendo términos/string?:
QA3. ¿Identifica claramente bases de datos/fuentes y período cubierto?:
QA4. ¿Define explícitamente criterios de inclusión y exclusión?:
QA5. ¿Describe claramente el proceso de selección/screening y medidas para reducir sesgo?:
QA6. ¿Describe claramente extracción de datos y análisis/síntesis?:
QA7. ¿Reporta estudios y evidencia con suficiente detalle para asegurar trazabilidad?:
QA8. ¿Resultados y conclusiones están respaldados por la evidencia sintetizada?:
QA9. ¿Discute limitaciones, amenazas a la validez o fuentes de sesgo?:
Quality Score (0–10): [Yes=1, Partially=0.5, No=0; suma sobre los 9 ítems, expresa en escala 0–10 y muestra el cálculo]

### RESEARCH QUESTIONS DEL PROYECTO (foco principal — profundidad y trazabilidad, no resumen genérico)

Para cada RQ entrega, en este orden exacto:
1. **Cobertura**: Alta / Media / Baja / Nula
2. **Síntesis** (2-4 frases, en español, respondiendo directamente lo que dice ESTE paper)
3. **Cita(s) verbatim** relevantes, entre comillas, idioma original, con marcadores `[n]` si el paper los usa
4. **Afirma vs demuestra**: cuál de las dos aplica a lo citado
5. **Percepción vs resultado objetivo**: cuál de las dos aplica (si no corresponde a esta RQ: N/A)
6. **Evidencia: p. X, secc. X**

RQ1: Identificar en qué actividades de enseñanza o aprendizaje de Ingeniería de Software se utiliza IAG (programación, debugging, diseño, requisitos, testing, documentación, tutoría, feedback, resolución de problemas, etc.).:
RQ2: Identificar qué estrategias didácticas se utilizan en la enseñanza de Ingeniería de Software y explicar cómo se incorpora la IAG dentro de ellas.:
RQ3: Identificar qué efectos del uso de IAG se reportan sobre los resultados de aprendizaje relacionados a la Ingeniería de Software.:
RQ4: Identificar qué métodos o estrategias de evaluación del aprendizaje son modificados, apoyados o realizados mediante IAG.:
RQ5: Identificar los beneficios, riesgos y limitaciones pedagógicas reportados sobre el uso de IAG en la enseñanza de Ingeniería de Software.:
RQ6: Identificar los vacíos de investigación encontrados en la literatura, limitaciones de la evidencia existente y temas que los autores señalan como necesarios para futuras investigaciones.:
RQ7: Identificar qué competencias o habilidades de Ingeniería de Software se consideran menos susceptibles de ser automatizadas por IAG y qué estrategias educativas se proponen para fortalecerlas.:

### HALLAZGOS Y CONTENIDO ADICIONAL (complementa, NO repite, las RQ anteriores)

8. Herramientas/tecnologías de IAG mencionadas (nombre + uso en el estudio):
9. Marcos teóricos / modelos pedagógicos citados:
10. Instrumentos de evaluación o medición usados en los estudios primarios:
11. Definiciones o conceptualizaciones relevantes (p. ej. qué entienden por "IAG", "competencia", "pensamiento computacional", etc.):
12. Recomendaciones para docentes/instituciones:
13. Citas textuales adicionales de interés:
14. Otros hallazgos o datos útiles para el proyecto:
