---
name: declinatoria-jurisdiccion-monitorio-sometimiento-civ-1171
description: "Declinatoria de jurisdicción en un monitorio por sometimiento a arbitraje. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Declinatoria de jurisdicción en un monitorio por sometimiento a arbitraje

> Formulario **CIV-1171** del plugin **Cobrar deudas: monitorio y cambiario** (`formularios-reclamar-deudas-monitorio`) · Civil › Monitorio y cambiario · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Declinatoria de jurisdicción en un monitorio por sometimiento a arbitraje» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Declinatoria de jurisdicción en un monitorio por sometimiento a arbitraje” para mi caso». También puedes invocarla directamente con `/formularios-reclamar-deudas-monitorio:declinatoria-jurisdiccion-monitorio-sometimiento-civ-1171`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-reclamar-deudas-monitorio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Cobrar deudas: monitorio y cambiario) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (2 veces)
- [ ] Nº DE CLÁUSULA (2 veces)
- [ ] Nº DE PROCEDIMIENTO (2 veces)
- [ ] AÑO
- [ ] DÍA
- [ ] FOLIO
- [ ] IMPORTE
- [ ] LUGAR
- [ ] MES
- [ ] NOMBRE DE LA CORTE ARBITRAL
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] NOMBRE Y APELLIDOS
- [ ] NOMBRE Y APELLIDOS DEL ABOGADO
- [ ] Nº
- [ ] Nº DE DOCUMENTO
- [ ] NÚMERO
- [ ] SEDE

## Normas que cita el formulario

- art. 63 LEC
- art. 63.2 LEC

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

- Junto a «…DIMIENTO] A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

Proceso ordinario nº [Nº DE PROCEDIMIENTO]

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

D. [NOMBRE Y APELLIDOS] Procurador de los Tribunales, actuando en representación de [NOMBRE DEL REPRESENTADO/A], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño a este escrito, en virtud de apoderamiento apud acta, ante el Tribunal comparezco y como mejor proceda en derecho, DIGO:

1) Que el pasado día [FECHA] mi representado fue emplazado para contestar la demanda en proceso ordinario número [NÚMERO] seguido ante ese Tribunal derivado de procedimiento monitorio número [Nº DE PROCEDIMIENTO] en reclamación de

2) Que entendiendo que el órgano al que me dirijo carece de jurisdicción por haberse sometido el asunto litigioso a arbitraje, por medio de este escrito, y dentro de los diez primeros días del plazo de contestación a la demanda, formulo DECLINATORIA DE JURISDICCIÓN en base a los siguientes

HECHOS

PRIMERO.- Que el presente procedimiento tiene por objeto la reclamación de [IMPORTE] euros, solicitadas por la actora con fundamento en un presunto impago del precio pactado en el contrato de arrendamiento de servicios suscrito entre el demandante y mi representado de fecha [FECHA] que obra en folio [FOLIO] del procedimiento monitorio unido a las actuaciones y aportado por el demandante como documento [Nº DE DOCUMENTO] de la demanda.

Como es de ver en la cláusula [Nº DE CLÁUSULA] del citado contrato de arrendamiento de servicios somete a los contratantes al servicio de corte arbitral y mercantil de arbitraje [NOMBRE DE LA CORTE ARBITRAL] en lo atinente a su aplicación e interpretación.

En este caso, la actora reclama una presunta deuda contractual, por lo que se está cuestionando la aplicación del contrato y, en consecuencia, cede la jurisdicción de los Tribunales de Justicia.

SEGUNDO.- Ante la eventual alegación que pueda realizarse de contrario en cuanto a que no se cuestionó específicamente la jurisdicción en el procedimiento monitorio previo, debemos indicar que esta parte se opuso al requerimiento de pago en tiempo y forma, alegando, entre otras excepciones, la falta de jurisdicción del tribunal, y reservándose su derecho para plantearla en el momento procesal oportuno, por lo que se cumplen los requisitos del artículo 63 y 818 de la LEC en relación con el artículo 11 de la Ley de Arbitraje para el planteamiento de la declinatoria de jurisdicción.

Por tanto, estando interpuesta la declinatoria en forma y existiendo un convenio arbitral válido según establece el artículo 9 de la Ley de Arbitraje y tratándose de materia susceptible de arbitraje, ambas partes vienen obligadas a cumplir lo estipulado, impidiendo a los tribunales conocer las controversia sometida a arbitraje, tal como imperativamente dispone el artículo 11 de la Ley de Arbitraje, lo cual nos obliga a formular la presente declinatoria de jurisdicción.

A los anteriores hechos son de aplicación los siguientes,

FUNDAMENTOS DE DERECHO

Competencia

Para formular y resolver la presente declinatoria corresponde al Tribunal que conoce del asunto ante el que sigue la tramitación de la causa (art. 63.2 LEC).

Legitimación

Le corresponde a esta parte ante su condición de demandada en las presentes actuaciones (arts. 39 y 63.2 LEC).

Procedimiento

Es el previsto en el arts. 63 y ss. de la LEC.

Plazo

El artículo 11.1, párrafo segundo, de la Ley de Arbitraje, redactado por Ley 11/2011, de 20 de mayo, establece: "el plazo para la proposición de la declinatoria será dentro de los diez primeros días del plazo para contestar a la demanda en las pretensiones que se tramiten por el procedimiento del juicio ordinario, o en los diez primeros días posteriores a la citación para vista, para las que se tramiten por el procedimiento del juicio verbal", formulándose la presente declinatoria en el plazo legalmente establecido.

(fundamento referido al monitorio previo) No es óbice a ello la tramitación de un monitorio previo, puesto que la interpretación jurisprudencial viene sosteniendo que el procedimiento monitorio tiene su propia autonomía y es un procedimiento de ejecución condicionada a la actitud, que frente a él, adopte la parte demandada, pues, en caso de oponerse el demandado, se deja sin efecto ni tiene valor alguno, teniendo como punto de conexión con los declarativos subsiguientes, simplemente la cuestión de las costas, que en caso de desestimarse el declarativo incluiría las costas de la oposición al monitorio o viceversa en su caso, así como, cuando se continua un verbal, se utilizaría el escrito inicial como demanda de verbal, al cumplir con el mínimo de los requisitos exigidos en dichas demanda de verbales, sin que otra conexión exista o establezca la Ley. En consecuencia, habiéndose opuesto mi representado en tiempo y forma, quedó sin efecto ni valor alguno el monitorio, siendo totalmente independiente el declarativo interpuesto, con lo que al ser el primer acto de la parte demandada frente a la demanda del declarativo ordinario interpuesto, independiente del monitorio previo, la interposición de la declinatoria de jurisdicción, está perfectamente interpuesta en tiempo y forma.

Fondo de la reclamación

El artículo 9 de la Ley de Arbitraje en cuanto a la forma y contenido del convenio arbitral y el artículo 11.1 de la misma Ley en cuanto a la falta de jurisdicción de los tribunales ordinarios, cuando establece:" 1. El convenio arbitral obliga a las partes a cumplir lo estipulado e impide a los tribunales conocer de las controversias sometidas a arbitraje, siempre que la parte a quien interese lo invoque mediante declinatoria".

Ante el hecho de constar la sumisión de la cuestión litigiosa a arbitraje según la cláusula [Nº DE CLÁUSULA] del contrato que antes se ha transcrito, el conocimiento de este litigio no corresponde al Tribunal ante el que me dirijo siendo el fundamento de ello los arts 1, 4, 5 y 9 de la Ley de Arbitraje, y especialmente el citado artículo 11 de la Ley según el que; "1. El convenio arbitral obliga a las partes a estar y pasar por lo estipulado e impedirá a los tribunales conocer de las cuestiones litigiosas sometidas a arbitraje en el convenio, siempre que la parte a quien interese lo invoque mediante declinatoria () 2. Las partes podrán renunciar por convenio al arbitraje pactado, quedando expedita la vía judicial. En todo caso, se entenderán que renuncian cuando, interpuesta demanda por cualquiera de ellas, el demandado o todos los demandados, si fuesen varios, realicen, después de personados en juicio, cualquier gestión procesal que no sea proponer en forma la declinatoria".

En este punto, como reitera la jurisprudencia, el poder de disposición de las partes en orden a la exclusión de los órganos jurisdiccionales del Estado en las materias de derecho disponible es prácticamente total, pudiendo citarse la STC 136/2010, entre las más recientes, que trata la conexión de esa facultad con el derecho fundamental a la tutela judicial efectiva, de modo que el convenio arbitral es apto para expresar "la voluntad de las partes de someter a arbitraje todas o algunas de las controversias que hayan surgido o puedan surgir respecto de una determinada relación, contractual o no contractual", todo lo cual determina la falta de jurisdicción del órgano al que nos dirigimos.

En base a lo anterior,

SUPLICO AL TRIBUNAL que tenga por interpuesta la presente declinatoria, se sirva por tener a esta parte por debidamente personada a los solos efectos de poner de manifiesto la falta de jurisdicción por estimar que corresponde el conocimiento de la controversia suscitada a árbitros y tras la suspensión inmediata del procedimiento en el que se interpone y la tramitación pertinente dando traslado a las demás partes, se dicte auto por el que se abstenga ese Tribunal de conocer de las presentes actuaciones por entender que la cuestión litigiosa se ha sometido a arbitraje, todo ello con imposición de costas a la parte demandante si se opusiere.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma Abogado [NOMBRE Y APELLIDOS DEL ABOGADO] Firma Procurador

========================================================================
