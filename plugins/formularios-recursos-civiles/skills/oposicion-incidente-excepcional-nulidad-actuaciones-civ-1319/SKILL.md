---
name: oposicion-incidente-excepcional-nulidad-actuaciones-civ-1319
description: "Oposición al incidente excepcional de nulidad de actuaciones. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Oposición al incidente excepcional de nulidad de actuaciones

> Formulario **CIV-1319** del plugin **Recursos civiles: reposición, apelación, casación y queja** (`formularios-recursos-civiles`) · Civil › Recursos · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Oposición al incidente excepcional de nulidad de actuaciones» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Oposición al incidente excepcional de nulidad de actuaciones” para mi caso». También puedes invocarla directamente con `/formularios-recursos-civiles:oposicion-incidente-excepcional-nulidad-actuaciones-civ-1319`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-recursos-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Recursos civiles: reposición, apelación, casación y queja) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] FECHA (3 veces)
- [ ] Nº DE PROCEDIMIENTO (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] SEDE (2 veces)
- [ ] DOMICILIO
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] Nº
- [ ] ÓRGANO JUDICIAL

## Normas que cita el formulario

- art. 228.2 LEC

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

### Avisos de actualización (2) — se aplican en el texto, nunca se copian en el documento

- Junto a «…eso [Nº DE PROCEDIMIENTO] A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…uidos con el número [NÚMERO] del Tribunal de Instancia de [SEDE], plaza n.º [Nº]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

Tribunal [ÓRGANO JUDICIAL]

Proceso [Nº DE PROCEDIMIENTO]

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D. [NOMBRE Y APELLIDOS] Procurador de los Tribunales y de [NOMBRE DEL REPRESENTADO/A], según tengo acreditado proceso verbal arriba referenciado, como mejor en Derecho proceda DIGO:

Que evacuando el traslado conferido por providencia de fecha [FECHA], por medio del presente escrito, y en relación a la posible nulidad de actuaciones de la sentencia instada por la contraparte, paso a oponerme a la pretensión deducida de contrario en las siguientes

ALEGACIONES

PRIMERO.- Nos oponemos a la pretensión de nulidad sostenida de contrario, pues la exposición fáctica que realiza no se ajusta a la realidad, siendo fácilmente constatable que tanto por esta parte como por el Tribunal al que me dirijo se han utilizado diligentemente las modalidades de comunicación legalmente previstas para asegurar la recepción por el destinatario de la correspondiente cédula, y que la falta de personación en este proceso sólo es atribuible a la actitud negligente del promotor del incidente.

Al efecto, baste exponer los hechos que resultan de las actuaciones para demostrar que en modo alguno hay indefensión en este caso:

a) el demandado tenía conocimiento del litigio pues compareció al acto de conciliación celebrado sin avenencia en fecha [FECHA] que obra como documento número 3 de la demanda. Al citado acto fue citado en el domicilio de [DOMICILIO], el mismo que se indicó en la demanda, en la persona de D. [NOMBRE Y APELLIDOS], tal como se acredita por testimonio de la diligencia de citación cuyo original obra en los autos de juicio de conciliación seguidos con el número [NÚMERO] del Tribunal de Instancia de [SEDE], plaza n.º [Nº] esta localidad (acompañamos testimonio como documento número 1).

b) al realizar el emplazamiento en este proceso, el demandado fue citado en la misma persona y en el mismo domicilio, por lo que lógicamente puede concluirse lógicamente que tuvo conocimiento del proceso.

c) en fechas inmediatamente posteriores, concretamente el día [FECHA], fue emplazado en este mismo domicilio en los autos de proceso ordinario número [Nº DE PROCEDIMIENTO], seguidos ante el Tribunal de Instancia número [NÚMERO], donde compareció. El emplazamiento se realizó en la misma persona D. [NOMBRE Y APELLIDOS] que en los dos casos anteriores (acompañamos como documentos 2 y 3 diligencia de emplazamiento y personación en los referidos autos, obrando en los mismos los originales).

d) en la fase de prueba, el demandado fue citado nuevamente para interrogatorio en el mismo domicilio por entrega de cédula a D. [NOMBRE Y APELLIDOS], quien se identificó como padre del destinatario, coincidiendo el apellido, tal como consta en los autos, lo que refuerza la deducción que el demandado conocía la pendencia del proceso.

e) finalmente, al finalizar el proceso y ser imposible la notificación de la sentencia en forma personal, es cuando se procede a la comunicación edictal de la misma, mas ello se realizó en legal forma, sin infringir precepto procesal alguno, a la vista del relato de hechos antes expuesto.

Por tanto, debe concluirse que ha sido la propia actitud del promotor del incidente la que contribuyó a crear la situación ahora expresada, descuidando su localización y dificultando su citación personal, por lo que ninguna situación de indefensión cabe apreciar, tal como ha indicado el TC y el TS reiteradamente, como es muestra la STC 90/2003, de 19 de mayo.

SEGUNDO.- De acuerdo a lo anterior, solicitamos la imposición de costas al promotor del expediente, así como que sea sancionado con la multa que prescribe el art. 228.2, segundo párrafo, de la LEC, habida cuenta de su manifiesta temeridad, en la cuantía que S.Sª estime conveniente.

Por lo expuesto, AL TRIBUNAL SUPLICO que tenga por presentado este escrito con justificante de traslado y, en su virtud, se deniegue la nulidad instada de contrario, manteniendo la validez de la sentencia firme dictada en este proceso, imponiendo al promotor las costas de este incidente y la sanción por temeridad prevenida legalmente.

En L. y F.

(Firma de Procurador y Abogado)

========================================================================
