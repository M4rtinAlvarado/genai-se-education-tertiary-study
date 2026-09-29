# Coding of primary studies at the practice level (NotebookLM)

One query per study. `{CITA}` and `{ARCHIVO}` are replaced by the reference and the PDF of the study; the query sources are that PDF and the two controlled vocabularies.

```text
EXTRACCIÓN COMPLEMENTARIA A NIVEL DE PRÁCTICA. Paper: {CITA} (archivo {ARCHIVO}). Analiza SOLO este paper; usa Catalogo_tecnicas_didacticas_1.md y SWEBOK_vocabulario_controlado.md únicamente como vocabulario controlado.

OBJETIVO: cruce SWEBOK × técnica didáctica × nivel taxonómico. La unidad es la PRÁCTICA, no el paper: cada práctica lleva SU área, SU técnica y SU nivel. Nunca combines la técnica de una práctica con el área de otra.

PRÁCTICA EDUCATIVA CON IAG = actividad de enseñanza/aprendizaje en la que estudiantes o docentes usan IA generativa, descrita con detalle suficiente para saber qué hace la persona. NO son prácticas: (a) instrumentos de investigación del estudio (encuestas, entrevistas, grupos focales, pre/post test, análisis de contenido hechos por los investigadores para recolectar o analizar datos), salvo que formen parte de la actividad del estudiante; (b) benchmarks que solo evalúan la herramienta; (c) menciones al pasar en el estado del arte. Fusiona menciones de una misma práctica. Nada genérico ("uso de ChatGPT", "feedback"): describe la acción concreta.

PARA CADA PRÁCTICA:
1 DESCRIPCION: qué hace el estudiante/docente y qué hace la IAG (1-2 frases).
2 AREA/SUBAREA (obligatorias): según la competencia de IS que desarrolla el estudiante, no según la herramienta o el artefacto. Solo áreas y subáreas del vocabulario SWEBOK; la subárea debe pertenecer al área; si no se puede precisar, "No determinable". Programación introductoria (escribir, leer, depurar código) = Construction, salvo foco explícito en pruebas, diseño, mantenimiento, etc. Si no desarrolla ninguna competencia de IS: "Fuera de SWEBOK", subárea "N/A".
3 AREA_2/SUBAREA_2 (opcional): solo si la actividad desarrolla clara y directamente una segunda competencia de IS. No por mencionar o producir un artefacto de otra área. Ante la duda, N/A en ambos.
4 TECNICA: la técnica del catálogo (código T001-T100 y nombre) que mejor representa CÓMO está organizada la actividad didáctica en la que ocurre la práctica (p. ej., sesión práctica guiada, trabajo en equipo, proyecto, caso, rol, simulación, evaluación práctica, preguntas), no solo la acción con la IA. "Sin equivalente" solo si ni la acción ni su formato corresponden a ninguna técnica; "No determinable" si el paper no describe el formato. No fuerces por parecido de nombre.
5 NIVEL: exactamente el del catálogo para esa técnica; si técnica = Sin equivalente o No determinable, nivel = "No determinable".
6 ESTADO: Implementada y evaluada (aplicada con estudiantes y con resultados) / Implementada sin evaluación / Propuesta (diseño o herramienta no aplicada en curso) / Recomendación (sugerencia de los autores).
7 ESTUDIO_PRIMARIO: "Este estudio" si la práctica es del propio paper; si viene de un trabajo citado, autor(es) y año, varios separados por "; "; sin trazabilidad, N/E.
8 RESULTADO: Objetivo (medida objetiva del aprendizaje del ESTUDIANTE) / Percepción (autorreporte) / Desempeño de herramienta (calidad de la salida de la IA) / Sin evaluación / N/E; varios separados por "; ".
9 CITA: textual y literal, idioma original, máx. 2 frases, que respalde la práctica.
10 UBICACION: página y/o sección.
No inventes clasificaciones, estudios, citas ni ubicaciones.

SALIDA (sin tablas, sin Markdown, sin "|", sin texto antes ni después). Primera línea:
PAPER_VERIFICADO: <título exacto del PDF>
Luego un bloque por práctica, separados por línea en blanco, con estos campos en este orden:
PRACTICA: <n>
DESCRIPCION:
AREA:
SUBAREA:
AREA_2:
SUBAREA_2:
TECNICA_COD:
TECNICA:
NIVEL:
ESTADO:
ESTUDIO_PRIMARIO:
RESULTADO:
CITA:
UBICACION:
Si no hay prácticas suficientemente detalladas: un único bloque con DESCRIPCION: No determinable en este artículo y N/A o N/E en el resto.
```

## Second query for studies with no practice found

Appended to the prompt above for the 19 studies whose first query returned no practice.

```text
SEGUNDA REVISIÓN: una primera lectura no encontró prácticas. Revisa de nuevo TODO el paper, incluidas metodología, discusión, implicancias para la enseñanza y trabajo futuro. Cuentan también las propuestas o recomendaciones CONCRETAS de uso docente de la IAG (Estado = Propuesta o Recomendación). Si de verdad no hay ninguna, mantén el bloque "No determinable en este artículo". No inventes.
```
