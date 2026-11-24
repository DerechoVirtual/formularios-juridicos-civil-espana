---
name: oposicion-ejecucion-provisional-pide-reducir-pension-civ-1452
description: "Oposición a la ejecución provisional que pide reducir la pensión compensatoria. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Oposición a la ejecución provisional que pide reducir la pensión compensatoria

> Formulario **CIV-1452** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Al Tribunal Procurador y representación Dirección letrada y anuncio de trámite (oposición a la ejecución provisional) HECHOS FUNDAMENTOS DE DERECHO Suplico Firmas

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Oposición a la ejecución provisional que pide reducir la pensión compensatoria» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Oposición a la ejecución provisional que pide reducir la pensión compensatoria” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:oposicion-ejecucion-provisional-pide-reducir-pension-civ-1452`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (6 veces)
- [ ] AÑO (4 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] Nº (2 veces)
- [ ] COLEGIO
- [ ] DÍA
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] MES
- [ ] Nº DE PROCEDIMIENTO
- [ ] NÚMERO
- [ ] OTROS DATOS

## Normas que cita el formulario

- art. 528 LEC

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

- Junto a «…Sección Civil del Tribunal de Instancia nº [NÚMERO]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.
- Junto a «…CIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA NÚMERO DE [LOCALIDAD]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

Sección Civil del Tribunal de Instancia nº [NÚMERO]

Ejecución provisional nº [Nº DE PROCEDIMIENTO]/[AÑO]

Traslado de copias al Procurador D. [NOMBRE Y APELLIDOS]

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA NÚMERO DE [LOCALIDAD]

D/Dª [NOMBRE Y APELLIDOS], Procurador/ de los Tribunales, en nombre de D./Dª [NOMBRE Y APELLIDOS], representación que acredito mediante primera copia de escritura de poder que acompaño, con el ruego de que una vez sea suficientemente testimoniada en autos me sea devuelta por precisarla a otros usos, ante el Tribunal, en los autos de ejecución provisionales de títulos judiciales núm. [Nº]/[AÑO], comparezco y DIGO:

Que mediante el presente escrito, dentro del plazo legal a tal efecto concedido, y bajo la dirección del/la Letrado del Ilustre Colegio de Abogados de [COLEGIO], D./Dª [NOMBRE Y APELLIDOS], paso a oponerme a la actuación concreta, en el marco de la ejecución provisional despachada [OTROS DATOS], consistente en que quede sin efecto la retención, de la cuenta del ejecutante, e ingreso en la cuenta de mi representada, del importe de la pensión compensatoria, en base a los siguientes:

HECHOS

Cierto el correlativo en cuanto recoge el fallo de la sentencia recaída en los autos de referencia, por la que se reduce en un 50% la pensión compensatoria acordada a favor de mi mandante en los autos de divorcio núm. [Nº]/[AÑO]

Incierto el correlativo en cuanto se insiste en que las circunstancias tenidas en cuenta cuando se acordó el pago mensual de [IMPORTE], en concepto de pensión compensatoria, han variado sustancialmente.

No obstante, dicha variación o no, sustancial, constituye el objeto del recurso de apelación interpuesto por mi parte contra la sentencia de modificación de las medidas.

La pensión compensatoria que percibe mi mandante constituye actualmente su único ingreso.

De su percepción depende que pueda hacer frente a sus necesidades primarias.

A tal efecto debe tenerse en cuenta que mi representada percibe hasta la fecha la suma de 600 € de pensión compensatoria. Con dicho importe, único ingreso tal y como acreditamos mediante copia de su declaración del IRPF del año 2.010 (DOCUMENTO NUM. UNO), debe hacer frente a:

1.- Recibo de alquiler por importe de [IMPORTE] €

2.- Recibo de la luz por importe de [IMPORTE] €

3.- Recibo de agua por importe de [IMPORTE] €

4.- Recibo de teléfono por importe de [IMPORTE] €

5.-Alimentación y vestido por importe de [IMPORTE] € (aproximadamente).

Adjunto aportamos como DOCUMENTOS NUMS. DOS al CINCO recibos acreditativos del pago de suministros.

Como es de ver, si se reduce la pensión, provisionalmente, hasta la resolución del recurso, se verá mi mandante imposibilitada de atender sus necesidades perentorias.

A los anteriores hechos les son de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

Competencia

Conformes con el correlativo.

Procedimiento

Conformes con el correlativo.

Legitimación activa y pasiva

Conformes con el correlativo.

Fondo del asunto

El art. 528 de la LEC dispone que "si la sentencia fuese de condena dineraria, el ejecutado no podrá oponerse a la ejecución provisional, sino únicamente a actuaciones ejecutivas concretas del procedimiento de apremio, cuando entienda que dichas actuaciones causarán una situación absolutamente imposible de restaurar o de compensar económicamente mediante el resarcimiento de daños y perjuicios".

Al formular esta oposición a medidas ejecutivas concretas, el ejecutado habrá de indicar otras medidas o actuaciones ejecutivas que sean posibles y no provoquen situaciones similares a las que causaría, a su juicio, la actuación o medida a la que se opone, así como ofrecer caución suficiente para responder de la demora en la ejecución, si las medidas alternativas no fuesen aceptadas por el Tribunal y el pronunciamiento de condena dineraria resultare posteriormente confirmado"

Si no se acuerda dejar sin efecto la medida que se solicita de contrario, y que se acuerda en la ejecución, de que en esta sede, interin se resuelve el recurso de apelación, se anule la orden de retención de la cuenta del ejecutante, del importe de la pensión, y su correlativo ingreso en la cuenta de mi mandante, el daño que se va a ocasionar será irreparable, pudiendo la misma llegar a ser desahuciada si no puede atender el pago de la renta arrendaticia, no pudiendo restaurarse tal situación.

A los efectos de garantizar la efectividad de la reducción, de confirmarse la sentencia, proponemos como alternativa el embargo y retención del importe de las cantidades que la Agencia Tributaria debe devolver a mi mandante, según consta en el documento núm. uno adjunto.

Asimismo ofrecemos caución suficiente para compensar la demora en la ejecución, en su caso, en la suma de 1.200 €

Costas

Deberán imponerse al ejecutante de no aceptar la alternativa que se propone a su ejecución provisional y en concreto a la actuación referida por la que se deja sin efecto la retención e ingreso de la pensión.

Por lo expuesto:

SUPLICO AL TRIBUNAL tenga por presentado este escrito, lo admita, por formulada oposición a la medida concreta de ejecución instada en el marco de la presente ejecución provisional, acordándose que la misma quede sin efecto, y admitiéndose la alternativa y la caución que se proponen.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma y número de letrado

Firma Procurador.

========================================================================
