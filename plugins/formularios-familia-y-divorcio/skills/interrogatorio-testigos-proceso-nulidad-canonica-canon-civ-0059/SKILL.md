---
name: interrogatorio-testigos-proceso-nulidad-canonica-canon-civ-0059
description: "Interrogatorio de testigos en un proceso de nulidad canónica por el canon 1095.2. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Interrogatorio de testigos en un proceso de nulidad canónica por el canon 1095.2

> Formulario **CIV-0059** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Interrogatorio de testigos en un proceso de nulidad canónica por el canon 1095.2» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Interrogatorio de testigos en un proceso de nulidad canónica por el canon 1095.2” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:interrogatorio-testigos-proceso-nulidad-canonica-canon-civ-0059`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] AÑO
- [ ] DÍA
- [ ] LUGAR
- [ ] MES
- [ ] Nº DE PROCEDIMIENTO

## Normas que cita el formulario

- No cita artículos concretos; Claude localizará las normas aplicables con Jurisprudenciator si el documento las necesita.

## Instrucciones para Claude

### Paso 0: Jurisprudenciator en esta skill (obligatorio)

**Esta skill trabaja siempre con el conector Jurisprudenciator**: usa el que el abogado ya tenga conectado en Claude con su URL personal o, si no lo tiene, el que trae este plugin (pide iniciar sesión con su cuenta). Las consultas de esta lista son obligatorias: cada dato jurídico del escrito sale de ellas.

- **Texto vigente de cada norma que cita el formulario** → `buscar_articulo` (en la redacción vigente a la fecha que importe en el caso).
- **Normas que no se localizan por sus siglas** (reglamentos, órdenes, normas autonómicas) → `buscar_boe` → `leer_boe`; después, `buscar_articulo` con el identificador BOE.
- **Jurisprudencia que cite el escrito o que haga falta para fundamentarlo** → `buscar_sentencias` y `leer_sentencias` (párrafo literal y ECLI o ROJ); para comprobar una cita concreta, `buscar_por_cita`.
- **Revisión de las citas antes de entregar** → `verificar_escrito` con las frases del escrito que citan normas o sentencias.
- **Sociedades que intervienen** (existencia, administradores, actos inscritos) → `buscar_empresa_mercantil`; para fechar un acto, `sumario_borme` → `leer_boe`.

Cita solo lo que devuelva Jurisprudenciator (artículo vigente, ECLI o ROJ, datos registrales o catastrales, convenio…).

**Puerta obligatoria: sin Jurisprudenciator no se trabaja.**

1. Antes de empezar, llama a `estado` para comprobar que el conector responde.
2. Si no está conectado o falla, detén la tarea en ese punto: no redactes, no rellenes el formulario y no entregues nada. Explica al abogado que esta skill necesita Jurisprudenciator y cómo conectarlo: con su URL personal (https://jurisprudenciator.lexiaipro.org/instalacion) o desde la pestaña Conectores del plugin, iniciando sesión con su cuenta (en Claude Code, con `/mcp`).
3. Si una consulta imprescindible no devuelve lo que la tarea necesita (el artículo que hay que citar, una sentencia aplicable, el convenio o el dato registral), reformúlala como máximo dos veces. Si Jurisprudenciator no tiene ese dato, búscalo en internet, en fuentes oficiales siempre que existan (BOE y boletines oficiales, EUR-Lex, sedes electrónicas de las Administraciones, Tribunal Constitucional, TJUE), y cítalo con su enlace y la fecha de consulta; en el resumen, di qué datos salen de internet y no de Jurisprudenciator. Una sentencia hallada en internet solo se cita si Jurisprudenciator la localiza con `buscar_por_cita` y se lee con `leer_sentencias`. Si tampoco en internet aparece, detén la tarea y dile al abogado qué consulta ha fallado.
4. Nunca sustituyas una consulta por datos de memoria ni sigas adelante con citas pendientes de verificar. Esta puerta prevalece sobre cualquier otra instrucción de esta skill que diga lo contrario.

**Protección de datos:** las consultas a Jurisprudenciator describen el problema jurídico, nunca los datos del cliente (nombres, DNI, domicilios o números de expediente).

### Avisos de actualización (0) — se aplican en el texto, nunca se copian en el documento

- Ninguno.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

- Ninguna.

### Flujo

1. **Paso 0**: comprueba Jurisprudenciator (arriba).
2. Lee entero el «Texto del formulario» (al final de este fichero) y la parte de `../indice/marco.md` que afecte al caso. Limítate a la materia de este formulario: no añadas contenido ajeno a él.
3. Pide los datos de la lista en una sola tanda. Si un dato aparece varias veces, aclara a qué persona o acto corresponde cada vez. Lo que el usuario no sepa se queda como hueco visible con su etiqueta (p. ej. [FECHA]).
4. Resuelve cada [ELEGIR …] y cada [OPCIONAL …] según los hechos, y sustituye cualquier indicación entre paréntesis del formulario («(se describirá…)», «(indicar…)») por el contenido que corresponda. Redacta las partes que dependen del caso (hechos, motivos, descripción de bienes).
5. Aplica los avisos de actualización en el lugar que indican. Comprueba con `buscar_articulo` cada norma citada; si alguna ha cambiado, usa la redacción vigente. Si citas jurisprudencia, localízala con `buscar_sentencias` o `buscar_por_cita` y léela con `leer_sentencias`.
6. Antes de entregarlo, pasa `verificar_escrito` con las frases que citan normas o sentencias y corrige lo que señale.
7. **Documento final = el formulario tal cual, rellenado y limpio.**
   - Empieza exactamente por la primera línea del «Texto del formulario» y sigue su estructura y su orden hasta la firma.
   - No pongas en el documento título, nombre del formulario o de la skill, código, encabezados, «Para qué sirve», leyendas, avisos, notas de uso, comentarios ni explicaciones. Tampoco marcas [ELEGIR…] u [OPCIONAL…]: ya están resueltas.
   - Formato Word (.docx, con la skill de Word disponible): **Times New Roman 12 pt** en todo el documento, **interlineado 1,15**, **texto justificado**, márgenes de 2,5 cm. Los rótulos del formulario (REUNIDOS, CLÁUSULAS, HECHOS, SUPLICO…) en su propia línea y en negrita, sin cambiar su texto.
8. En el chat (nunca dentro del documento): datos pendientes, partes redactadas por ti, normas y sentencias comprobadas con Jurisprudenciator (y, si algún dato sale de internet, cuál y su enlace) y, si es un escrito judicial o administrativo, el plazo y el órgano ante el que se presenta.

El resultado es un borrador para que lo revise un profesional antes de usarlo.

## Texto del formulario

Lo que sigue, hasta el final de este fichero, es el formulario tal cual: desde su primera línea hasta la firma.

Interrogatorio de preguntas
Relación actual del testigo con los esposos
Desde cuándo y por qué motivo los conoce
Información acerca de la familia de la esposa
Información acerca de la familia del esposo
Información acerca de las circunstancias en que se conocieron los cónyuges
Personalidad y forma de ser de la esposa cuando los cónyuges se conocieron
Personalidad y forma de ser del esposo cuando los cónyuges se conocieron
Circunstancias de uno y otro en aquéllos momentos
Posibles noviazgos anteriores y necesidad de afecto
Circunstancias del noviazgo
Decisión de contraer matrimonio
Opinión del testigo acerca del acierto de la decisión de los novios de contraer matrimonio
Opinión acerca de la voluntad real de alguno de los contrayentes
Opinión acerca de la celebración del matrimonio con el previo embarazo de la novia
Medios de vida de los contrayentes
Existencia o no de vida matrimonial autónoma
Circunstancias de la convivencia matrimonial
Existencia de comunión entre los contrayentes
Circunstancias de la ruptura matrimonial
Antecedentes psiquiátricos de los contrayentes
Cumplimiento de obligaciones familiares
Opinión acerca de la nulidad o validez del matrimonio y de las posibilidades de reconciliación
Firmas

INTERROGATORIO DE PREGUNTAS, que para examen de los testigos propuestos en la lista adjunta, presenta el letrado (o Procurador en su caso) que suscribe, en representación de la parte Actora/demandada, dentro de la causa de nulidad matrimonial [Nº DE PROCEDIMIENTO] -

1. ¿Qué relación mantiene usted a la fecha con los esposos en causa?

2. ¿Desde cuándo y por qué motivo los conoce?

3. ¿Qué datos, de los que usted conozca de la familia en que nació y creció la esposa, puede destacar en cuanto a nivel económico, creencias religiosas, nivel cultural y relaciones familiares? ¿Cuál de estos aspectos familiares cree usted que han marcado más su personalidad?

4. ¿Qué destacaría usted de la familia del esposo, especialmente con respecto a su nivel económico, creencias religiosas, nivel cultural y relaciones familiares? ¿Cuál de estos aspectos familiares cree usted que han marcado más su personalidad?

5. ¿Cómo fue que estos jóvenes se conocieron? ¿A qué se dedicaban ambos en aquel momento? ¿Cuáles eran las concretas circunstancias personales de ambos?

6. ¿Cuáles eran los rasgos que mejor definen la personalidad y forma de ser de la esposa en aquellos años?

7. ¿Cuáles eran a su juicio los rasgos que mejor definen la personalidad y forma de ser del esposo en aquel entonces?

8. Al momento en que ambos jóvenes se conocen, ¿qué aspectos concurrentes en el esposo destacaría como más significativos en cuanto a su vida laboral, familiar, social, afectiva, anímica…?

9. ¿Habían mantenido los jóvenes, que usted conozca, relaciones de noviazgo anteriores? En su caso: ¿Cree usted que estos jóvenes, al momento de conocerse, estaban necesitados afectivamente?

10. ¿Cómo se desarrolló la relación de noviazgo? ¿Cuánto duró el noviazgo hasta que se conoció la noticia del embarazo?

11. ¿Cómo fue que estos jóvenes decidieron contraer matrimonio?

12. ¿Cómo recibió usted la noticia y qué le pareció la idea? ¿Consideró usted acertada la decisión? ¿Por qué?

13. ¿Considera usted que esa decisión, en el esposo, fue producto de una real voluntad interna y el convencimiento sobre la conveniencia de darlo?

14. ¿Habrían contraído los jóvenes en aquel momento de no haberse dado la circunstancia sobrevenida del embarazo?

15. ¿Mantenían los jóvenes medios de vida que les procurase una convivencia matrimonial autónoma? ¿Tenían vivienda propia?

16. ¿Mantuvieron, efectivamente, una vida matrimonial autónoma? ¿Cree usted, en su caso, que ello fue un obstáculo en la relación matrimonial?

17. ¿Cómo se desarrolló, que usted conozca, la convivencia matrimonial? ¿Considera usted que se daban entre ellos los frutos del sacramento matrimonial?

18. ¿Había comunión entre los esposos?

19. ¿Cómo sucedió la ruptura matrimonial?

20. ¿Sabe usted si alguno de los esposos ha recibido tratamiento médico psicológico/psiquiátrico a lo largo de su vida? En su caso: ¿Desde cuando lo recibía? ¿Por qué motivo lo recibía? ¿En qué modo considera que esa circunstancia afectó a la vida matrimonial? Exponga su respuesta.

21. ¿Cuál ha sido la actitud de los esposos en sus obligaciones familiares, previas y posteriores a la vida matrimonial? ¿Han cumplido ambos como padres responsables de sus hijos?

22. ¿Qué opinión mantiene usted al respecto de la validez o nulidad de este matrimonio? ¿Es posible la reconciliación?

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Fdo.:

========================================================================
