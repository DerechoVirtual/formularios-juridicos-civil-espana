---
name: escrito-pidiendo-costas-multa-mala-fe-procesal-civ-1188
description: "Escrito pidiendo costas y multa por mala fe procesal al demandante que desiste en el monitorio. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito pidiendo costas y multa por mala fe procesal al demandante que desiste en el monitorio

> Formulario **CIV-1188** del plugin **Cobrar deudas: monitorio y cambiario** (`formularios-reclamar-deudas-monitorio`) · Civil › Monitorio y cambiario · normativa revisada el 24-11-2026.

## Qué es

Escrito de parte demandada en un proceso monitorio que ha formulado oposición por el que solicita la imposición de costas y de multa por mala fe procesal al demandante que ha desistido.

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito pidiendo costas y multa por mala fe procesal al demandante que desiste en el monitorio» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito pidiendo costas y multa por mala fe procesal al demandante que desiste en el monitorio” para mi caso». También puedes invocarla directamente con `/formularios-reclamar-deudas-monitorio:escrito-pidiendo-costas-multa-mala-fe-procesal-civ-1188`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-reclamar-deudas-monitorio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Cobrar deudas: monitorio y cambiario) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] DENOMINACIÓN SOCIAL (7 veces)
- [ ] AÑO (5 veces)
- [ ] NÚMERO (5 veces)
- [ ] ASEGURADORA (4 veces)
- [ ] Nº DE PROCEDIMIENTO (3 veces)
- [ ] FECHA (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] IMPORTE
- [ ] LUGAR
- [ ] MES
- [ ] SEDE

## Normas que cita el formulario

- art. 816.2 LEC
- art. 32.5 LEC
- art. 247.3 LEC

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Notas al pie del formulario original:
(1) Otra posibilidad de supuesto de exigencia de condena en costas que incluya gastos de profesionales no preceptivos, y multa por mala fe procesal, podría ser el supuesto inverso del deudor al que se le formulan requerimientos monitorios, deduce oposición, y luego no asiste al acto de la vista. También podría pensarse que, si media oposición del deudor a requerimiento monitorio que impone demanda de juicio ordinario, y luego el deudor opuesto no contesta y queda rebelde en el juicio, la postura es de mera dilación contraria a la buena fe procesal, acreedora de sanción.

========================================================================


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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales y de D./Dña. [NOMBRE Y APELLIDOS], como tengo acreditado en estos autos de Juicio Monitorio n.º [Nº DE PROCEDIMIENTO]/[AÑO], ante el Tribunal comparezco y como mejor proceda en Derecho, DIGO:

Que mediante el presente escrito vengo a evacuar el traslado conferido por el Tribunal del escrito de desistimiento de la demanda en base a las siguientes

ALEGACIONES

PRIMERO.- La entidad [DENOMINACIÓN SOCIAL] S.L., solicitó requerimiento monitorio frente a mi mandante, dando lugar al presente juicio, aduciendo un crédito de [IMPORTE] euros, que justificaba con una factura, que ni siquiera estaba emitida contra la que señalaba como deudora, sino contra la compañía de seguros [ASEGURADORA], S.A., apareciendo el nombre de mi patrocinada entre paréntesis.

SEGUNDO.- El caso es que [DENOMINACIÓN SOCIAL], S.L. presentó similares solicitudes de proceso monitorio contra diversas personas en próximas fechas del mes de [MES] de [AÑO], siempre por obras ejecutadas y facturadas a cuenta de la compañía de seguros [ASEGURADORA] S.A., a raíz de avisos por siniestros relacionados con filtraciones en viviendas.

Sin que se haya podido por esta parte obtener resultados completos de las solicitudes presentadas, por lo menos en esta circunscripción se han identificados los seis siguientes procedimientos: n.º [NÚMERO]/[AÑO] del Tribunal de Instancia nº [NÚMERO]; nº [NÚMERO]/[AÑO] y n.º [NÚMERO]/[AÑO] del Tribunal de Instancia n.º [NÚMERO]; [Nº DE PROCEDIMIENTO]. Aportamos fotocopias conseguidas privadamente, de la solicitud, siempre idéntica, y de los decretos de admisión, remitiéndonos a los archivos del Tribunal Decano.

TERCERO.- Esta parte dedujo oposición en escrito de fecha [FECHA], al de dos días hábiles de habérsele formulado el requerimiento, representada por quien comparece y con defensa letrada, a pesar de que la reclamación no supere los 2.000 euros.

Cabalmente, de los seis procedimientos mencionados, en otros tres (nos. [Nº DE PROCEDIMIENTO]) se ha producido oposición, con el mismo argumento de que quien contrató a la entidad actora es la compañía de seguros [ASEGURADORA] S.A [DENOMINACIÓN SOCIAL], a la que no nos consta que se haya demandado. Se acompañan copias de los escritos de oposición.

CUARTO.- Pues bien, en todos los juicio monitorios en que se ha verificado la oposición, incluido el presente, [DENOMINACIÓN SOCIAL], S.L ha procedido a presentar escrito de desistimiento, antes de que se pudiera citar a la vista como ordena el art. 816.2 LEC, mientras que en los otros tres que se tienen identificados, idénticos, al no haber oposición, ha pedido el despacho de ejecución. Se adjuntan fotocopias, con protesta de autenticidad en las respectivas actuaciones.

QUINTO.- La conducta de [DENOMINACIÓN SOCIAL], S.L de una parte, no puede considerarse desistimiento unilateral del proceso, porque si bien se produce antes de la citación, es consecuencia de la solicitud inicial de juicio monitorio ante la que esta parte ha debido comparecer para oponerse; de otra, no puede quedar sin condena en costas, a pesar de que no merezca la pena celebrar vista, ya que no se consiente; y en fin, la condena en costas debe incluir el reintegro de los honorarios de procurador y abogado, por apreciarse temeridad procesal en la demandante, que utiliza el juicio monitorio de manera torticera, a fin de conseguir un título ejecutivo, por crédito que conoce no le corresponde contra los que interpela, sin querer enfrentarse con su comitente (compañía de seguros [ASEGURADORA] S.A [DENOMINACIÓN SOCIAL]), arropada en la necesidad de que los requeridos deban costear el asesorarse y comparecer oponiéndose, como demuestra la batería de pretensiones iguales que ha llevado a estos tribunales en poco tiempo, y que desista de cuantas encuentran una resistencia formal.

Invocándose el tenor del art. 32.5 LEC para la inclusión de derechos de profesionales de la postulación en la condena en costas, asimismo se considera a la parte actora acreedora, no de lo que pedía a ésta, sino de la multa por transgresión de la buena fe procesal, motivada en lo predicho, de conformidad con art. 247.3 LEC, teniendo en cuenta los perjuicios que a mi mandante se han ocasionado.

Por todo ello,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito, con sus documentos, se sirva admitirlo, y en mérito a lo manifestado, incluso previa las comprobaciones que se acuerden o la contradicción de adverso, se tenga a esta parte por disconforme con un desistimiento sin condena en costas, sin perjuicio de no considerar preciso convocatoria de vista para resolver, y se tenga a [DENOMINACIÓN SOCIAL], S.L, por desistida con expresa condena en costas, que por su temeridad incluirán honorarios y suplidos de procurador y abogado de esta parte, y conllevarán multa por mala fe procesal, en la cuantía que prudencialmente fije S.Sª, con lo demás que proceda

Por ser de Justicia que pido en [LUGAR], a [FECHA].

Firma de Abogado/a	Firma de Procurador/a
