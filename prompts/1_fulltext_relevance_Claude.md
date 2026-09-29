# Stage 3: relevance of each full text to the focus of the study (Claude Sonnet 5)

```text
Clasifica la relación de cada documento cargado con la línea pedagógica del FONDECYT 11260438: enseñanza y evaluación universitarias que integran o responden a la IA generativa (IAG) para fortalecer competencias de ingeniería de software y estudiar sus efectos educativos.
 Ingeniería de software: requisitos, diseño, arquitectura, construcción, pruebas, despliegue, operación, mantenimiento, calidad, gestión, trabajo en equipo. No la reduzcas a programación.
 Procesa TODAS las fuentes cargadas, una fila por documento, sin omitir ninguna y sin mezclar contenido entre documentos. Basa cada punto en el cuerpo del texto, no en título/abstract. No inventes citas ni ubicaciones.
 Antes de clasificar, identifica: (1) qué estrategia, mecanismo o efecto educativo con IAG desarrolla el documento, (2) qué competencia de ingeniería de software aborda, (3) qué aporta concretamente para diseñar o evaluar una intervención pedagógica.
 Niveles:
Alta: aborda cómo se usa la IAG en la enseñanza de ingeniería de software (no solo programación) Y reporta o discute efectos concretos en resultados de aprendizaje (desarrollo de competencias, desempeño, motivación, satisfacción docente, etc.), con aporte sustancial, no una mención aislada. Antes de asignarla, descarta explícitamente: ¿es solo un tema afín sin desarrollo? ¿confundes herramienta con enseñanza, rendimiento de la IA con aprendizaje, uso investigativo con integración educativa, o IA tradicional con IAG? Si hay duda razonable, asigna Media.
Media: relación pedagógica directa (uso de IAG en enseñanza de ISW o efectos en aprendizaje), pero uno de los dos elementos falta o está poco desarrollado.
Baja: contexto general o mención sin desarrollo directo de uso pedagógico ni de efectos en aprendizaje.
Ninguna: no aporta al foco pedagógico descrito.
 No fuerces cuotas ni resultados positivos; clasifica cada documento por su mérito individual.
Salida (cada campo breve, para no cortar la tabla):
Documento: autor, año, título.
Relación: ninguna / baja / media / alta.
Aporte y competencia: 1 línea.
Justificación: máx. 2 líneas.
Evidencia: 1 cita breve (máx. 25 palabras) con página o sección.
 -Resumen breve del paper
```
