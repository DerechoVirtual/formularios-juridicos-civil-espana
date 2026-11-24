---
name: contestacion-demanda-revision-sentencia-firme-civil-civ-1336
description: "Contestación a la demanda de revisión de sentencia firme civil. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contestación a la demanda de revisión de sentencia firme civil

> Formulario **CIV-1336** del plugin **Recursos civiles: reposición, apelación, casación y queja** (`formularios-recursos-civiles`) · Civil › Recursos · normativa revisada el 24-11-2026.

## Qué es

Modelo de escrito de contestación a la demanda de revisión de sentencia firme.

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contestación a la demanda de revisión de sentencia firme civil» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contestación a la demanda de revisión de sentencia firme civil” para mi caso». También puedes invocarla directamente con `/formularios-recursos-civiles:contestacion-demanda-revision-sentencia-firme-civil-civ-1336`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-recursos-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Recursos civiles: reposición, apelación, casación y queja) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (4 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] IMPORTE
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] Nº
- [ ] Nº DE PROCEDIMIENTO
- [ ] OTROS DATOS
- [ ] SEDE

## Normas que cita el formulario

- art. 512 LEC
- art. 514 LEC
- art. 510.4 LEC
- art. 516.2 LEC

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

### Avisos de actualización (1) — se aplican en el texto, nunca se copian en el documento

- Junto a «…ación al proceso seguido ante el Tribunal de Instancia de [SEDE], plaza n.º [Nº]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

Rollo nº [Nº DE PROCEDIMIENTO]

A LA SALA PRIMERA DEL TRIBUNAL SUPREMO

D. [NOMBRE Y APELLIDOS] Procurador de los Tribunales, actuando en representación de [NOMBRE DEL REPRESENTADO/A] según se acredita mediante escritura de poder que se acompaña y se solicita sea devuelta una vez testimoniada (o en virtud de apoderamiento apud acta que se otorgará ante la Secretaría de la Excma. Sala) comparezco en el presente procedimiento en el que se emplazó a mi representada el pasado [FECHA] y por medio de la presente paso a contestar a la demanda de revisión de la sentencia de fecha [FECHA] interpuesta por D. [NOMBRE Y APELLIDOS] en base a los siguientes:

HECHOS

PRIMERO.- Se niegan todos los hechos expuestos en la demanda a excepción de los que se vean aceptados en la presente contestación.

SEGUNDO.- En cuanto al hecho primero de la demanda, se aceptan las fechas que figuran en los antecedentes en relación al proceso seguido ante el Tribunal de Instancia de [SEDE], plaza n.º [Nº] [OTROS DATOS], pero se rechaza que esta parte ocultara el domicilio de la contraparte, e incluso rechazamos que el demandante de revisión desconociera el pleito como indica.

En efecto, las comunicaciones en el proceso se practicaron todas ellas en legal forma en el único domicilio que constaba a esta parte, que fue el que facilitó mi representada. Dicho domicilio es el mismo que el que figura en el Registro Mercantil (acompañamos como documento número 1 nota simple de inscripción de la sociedad), siendo hay indicios para afirmar, como expondremos a continuación, que la contraria tuvo efectivo conocimiento del proceso.

En cualquier caso, esta parte no realizó conducta alguna tendente a ocultar el domicilio de la contraria, actuando siempre conforme a las reglas de la buena fe procesal.

TERCERO.- En cuanto al hecho segundo de la demanda, debe subrayarse que el demandante de revisión no precisa en momento alguno cuál es el plazo en que conoció el presunto fraude, pues no lo concreta en ningún momento. Negamos en cualquier caso la fecha que parece indicar, pues el demandante conocía al menos desde hace un año que se había dictado sentencia estimatoria, ya que en fecha [FECHA] el director financiero de dicha empresa remitió un fax a mi representada solicitando una entrevista para negociar el pago de la cantidad de [IMPORTE] euros, precisamente la que fue objeto de condena (acompañamos como documento número 1 copia del referido fax). Lógicamente, tal documento pone de manifiesto que la sentencia se conocía desde mucho antes del plazo de tres meses a que se refiere el art. 512 de la LEC y, además, que ningún fraude procesal se produjo, pues la contraparte tuvo efectivo conocimiento del pleito.

CUARTO.- En cuanto al hecho tercero de la demanda, negamos los hechos, pues no hubo fraude alguno, conforme se ha expuesto en los anteriores hechos.

FUNDAMENTOS DE DERECHO

PRIMERO.- Competencia y procedimiento.-Se acepta la competencia de la Sala y la tramitación de la causa por los trámites del art. 514 de la LEC y asumiendo las alegaciones en este sentido vertidas en el escrito de demanda.

SEGUNDO.- En cuanto a la inadmisibilidad e improcedencia de la demanda de revisión, es de aplicación el art. 512 de la LEC, por haberse excedido el plazo de interposición de tres meses, no concurriendo el motivo del art. 510.4 de la LEC, al tratarse de sentencia ganada justamente, sin fraude procesal alguno como se ha expuesto en los hechos.

TERCERO.- En materia de costas y pérdida del depósito, el art. 516.2 LEC.

En base a lo anterior,

SUPLICO A LA SALA que tenga por presentado este escrito junto con sus copias, teniendo a esta parte por personada en las presentes actuaciones entendiéndose conmigo las siguientes diligencias y por contestada a la demanda interpuesta contra mi principal y tras la pertinente tramitación se sirva dictar sentencia por la que se desestime la demanda de revisión de la sentencia de fecha [FECHA], con pérdida de depósito e imposición de costas al demandante.

En L. y F.

(Firma Procurador y Abogado)

========================================================================
