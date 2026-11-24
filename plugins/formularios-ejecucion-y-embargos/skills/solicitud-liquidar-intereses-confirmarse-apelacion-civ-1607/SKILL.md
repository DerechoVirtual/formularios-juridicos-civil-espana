---
name: solicitud-liquidar-intereses-confirmarse-apelacion-civ-1607
description: "Solicitud de liquidar intereses al confirmarse en apelación la condena consignada por la aseguradora. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud de liquidar intereses al confirmarse en apelación la condena consignada por la aseguradora

> Formulario **CIV-1607** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Escrito de solicitud de liquidación de intereses al haberse ratificado la condena en segunda instancia y existiendo consignación judicial por parte de la compañía aseguradora demandada.

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud de liquidar intereses al confirmarse en apelación la condena consignada por la aseguradora» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud de liquidar intereses al confirmarse en apelación la condena consignada por la aseguradora” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:solicitud-liquidar-intereses-confirmarse-apelacion-civ-1607`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (22 veces)
- [ ] IMPORTE EN LETRA (11 veces)
- [ ] FECHA (2 veces)
- [ ] NOMBRE DEL REPRESENTADO/A (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] AÑO
- [ ] LUGAR
- [ ] MOTIVO
- [ ] Nº
- [ ] NÚMERO
- [ ] SEDE

## Normas que cita el formulario

- art. 20 LCS
- art. 449.3 LEC
- art. 20.4.º LCS

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS], Procurador de los Tribunales y de D./Dña. [NOMBRE Y APELLIDOS], demandante en autos de JUICIO ORDINARIO n.º [NÚMERO]/[AÑO], sobre materia de responsabilidad derivada de la circulación de vehículos de motor, ante el Tribunal comparezco, y como mejor en Derecho proceda, DIGO:

Que, [MOTIVO] vengo a presentar la liquidación de intereses, interesando la entrega a esta parte de la cantidad consignada, e interesando que se requiera a la demandada para que proceda al abono a esta parte de la cantidad que, en concepto de intereses moratorios especiales procede, sobre la cantidad por ella consignada, con fundamento en las siguientes:

ALEGACIONES

PRIMERA.- INTERESES DEVENGADOS DESDE LA FECHA DEL SINIESTRO HASTA EL MOMENTO DE LA CONSIGNACION EFECTUADA POR LA DEMANDADA EL 11 DE MAYO DE 2001.

En la sentencia dictada en este procedimiento se condena a la demandada a pagar a mi representada [NOMBRE DEL REPRESENTADO/A] xxx [IMPORTE] € en concepto de principal, con más sus intereses del art. 20 LCS.

La demandada consignó los [IMPORTE EN LETRA] xxx [IMPORTE] € de principal el 11 de mayo de 2001, consignando en la misma fecha [FECHA] yyy [IMPORTE] € en concepto de intereses.

Desde la fecha del siniestro (30 de agosto de 1994) hasta la fecha de tal consignación se devengaron [IMPORTE EN LETRA] zzz [IMPORTE] € en concepto de intereses, desglosadas de la siguiente manera:

- Desde el 30 de agosto de 1994 hasta el 30 de agosto de 1996 (730 días), a razón de [IMPORTE] €/día: sss [IMPORTE] €. Desde el 31 de agosto de 1996 hasta el 11 de mayo de 2001 ( [Nº] días), a razón de [IMPORTE] €/día, asciende a [IMPORTE EN LETRA] rrr [IMPORTE] €.

Así pues, el total de intereses devengados desde la fecha del siniestro hasta la fecha de consignación por la demandada, asciende a [IMPORTE EN LETRA] zzz [IMPORTE] € ( [IMPORTE] sss [IMPORTE] + [IMPORTE] rrr [IMPORTE]), es decir, [IMPORTE EN LETRA] uuu [IMPORTE] € más que las consignadas por la demandada en tal concepto el 11 de mayo ( [IMPORTE EN LETRA] yyy [IMPORTE] €).

Así pues, en el supuesto de que se considerara por este Tribunal que los intereses sólo han de ser calculados hasta la fecha de la consignación efectuada por la demandada, procedería:

1º.- Que se haga entrega a esta parte de la cantidad consignada en tal concepto por la demandada, al tener vocación de pago, por la firmeza de la condena, y ser inferior a la procedente.
2°.- Que se requiera a la demandada para que abone a esta parte los [IMPORTE EN LETRA] uuu [IMPORTE] € también devengados, y no consignados, hasta esa fecha.

No obstante, entiende esta parte que la fecha final para el cómputo de tales intereses no ha de ser la de la fecha de la consignación realizada por la demandada, sino la fecha en que a este Tribunal llegaron los autos procedentes de la Audiencia Provincial, y así se proveyó en resolución comunicada a las partes, por las razones que exponemos en el apartado siguiente.

SEGUNDA.- INTERESES PROCEDENTES DESDE LA FECHA DE LA CONSIGNACION POR LA DEMANDADA HASTA LA FECHA DE LLEGADA DE LOS AUTOS, PROCEDENTES DE LA AUDIENCIA PROVINCIAL, A ESTE TRIBUNAL.

Mi representada tiene derecho a los intereses de la cantidad fijada como principal desde la [ELEGIR: fecha del siniestro hasta la de su pago / fecha en que se pudo solicitar tal pago por el Tribunal de la consignación efectuada por el deudor].

La demandada consignó la cantidad procedente en concepto de principal, sin ofrecimiento de pago de dicha cantidad a mi representada, y sin solicitar que la misma fuera entregada a ésta, realizando tal consignación simplemente para cumplir un requisito necesario para la válida interposición del recurso de apelación que ha sido desestimado.

No fue, pues, una consignación que se realizara con la finalidad de proceder al pago a mi representada con efectos liberatorios, a tenor de los arts. 1.157 y 1.160 CCiv, sino con la finalidad de poder interponer dicho recurso, como ordena el art. 449.3 LEC.

Evidentemente, tal pago no pudo ser realizado a mi representada por este Tribunal, porque la sentencia dictada por este (y posteriormente confirmada) no era firme, y no se instó la ejecución provisional, que no es una carga de quien vence en primera instancia, sino una facultad.

Y cuando dicha sentencia adquirió firmeza (al dictarse por la Audiencia Provincial sentencia el 27 de septiembre, que fue notificada el 4 de octubre de 2002), tampoco este Tribunal podía proceder a la entrega del dinero consignado a mi representada, pues, al no tener los autos, desconocía si se había dictado sentencia definitiva por la Audiencia Provincial, desconociendo, por ello, si confirmaba o no la dictada por este Tribunal, y el valor que podía entonces tener la consignación de la demandada.

Al menos en ese momento, pudiera haber presentado la demandada un escrito a este Tribunal solicitando que, dado que la sentencia ya era firme, procediera a entregar a mi representada las cantidades consignadas. En tal caso, aun cuando este Tribunal no hubiera poseído los autos, solicitándose por la propia parte consignante la entrega a mi representada, podía haber procedido a tal entrega. Pero tampoco la demandada hizo esto, de manera que, este Tribunal, hizo lo único que podía hacer: esperar a la llegada de los autos para proceder a la entrega de la cantidad consignada a esta parte.

Entiende por ello esta parte que, puesto que la consignación no se realizó por la demandada con la finalidad de que se entregara a mi representada con fines liberatorios, sino simplemente como requisito para recurrir que ni siquiera cuando el recurso sabía haber sido desestimado empleó los medios a su alcance (medios sencillos, un simple escrito), tendentes a evitar que se produjera un retraso (que sabía inevitable) en el pago (no imputable a este Tribunal que no tenía los autos ni la sentencia definitiva), será la demandada la que deba hacer frente a los intereses a los que mi presentada tiene derecho (hasta el momento de su pago). Y, por lo tanto, que la demandada deberá pagar intereses hasta el momento en que este Tribunal estuvo en disposición de poder entregar a mi representada, esta vez sí con la finalidad de pago de la deuda en ejecutoria, las cantidades consignadas por la demandada.

Así pues, el "dies ad quem" para el cómputo de intereses debe ser el momento a partir del cual la cantidad objeto de condena se puso a disposición de esta parte, que no es otro que aquel en el que se notificó la providencia que enteraba de la recepción de los autos por este Tribunal.

Así se ha entendido por la doctrina de apelación: AAPP Valladolid, autos de 5 de mayo de 1994 y 19 de abril de 1996; Navarra, auto de 10 de septiembre de 1998; Burgos, auto de 15 de julio de 1999; Castellón, auto de 11 de octubre de 1999; Salamanca, auto de 25 de octubre de 1999; Vizcaya, auto de 3 de marzo de 2000; Soria, auto de 13 de mayo de 2004; Valencia, auto de 10 de mayo de 2007.

Además, en el caso que nos ocupa, ha de tenerse presente el excesivo tiempo transcurrido desde la producción del siniestro hasta que mi representada estuvo en disposición de poder cobrar la cantidad que se le adeudaba con la llegada de las autos a este Tribunal (más de siete años), hasta el punto de que la cantidad procedente en concepto de intereses es superior a la indemnización correspondiente en concepto de principal.

Es decir, aunque se impusieron a la demandada merecidísimamente los intereses del 20%, con arreglo al art. 20.4.º LCS (pues habían pasado más de dos años desde el siniestro sin consignar ni pagar una céntimo), podía llegar a ser entendible que recurriera la sentencia de este Tribunal en lo relativo a la imposición de tal tipo de interés, pero desde luego, lo que ya entraba de lleno en la temeridad era seguir sin realizar, con efectos liberatorios de pago, una consignación por la cantidad fijada en sentencia por un accidente ocurrido seis años antes, siendo más injustificable aún que dejara transcurrir otro mes más (desde el 4 de octubre en que se le notifica la sentencia definitiva hasta que el 8 de noviembre este Tribunal tiene constancia de la llegada de los autos), sin presentar un simple escrito en este Tribunal otorgando, al menos a la consignación realizada en concepto de principal, efectos liberatorios.

Así pues, a la cantidad indicada en el apartado precedente en concepto de intereses, HABRÁN DE AÑADIRSE LOS INTERESES DEVENGADOS DESDE EL 12 DE MAYO DE 2001 (día siguiente a la consignación realizada por la demandada) HASTA EL 8 DE NOVIEMBRE DE 2000 (fecha de la providencia de este Tribunal dando por recibidos los autos de la Audiencia Provincial), LO QUE SUPONEN 181 DÍAS QUE, A RAZÓN DE [IMPORTE] € DIARIOS, ARROJAN LA CIFRA DE [IMPORTE EN LETRA] vvv [IMPORTE] €.

TERCERA.- RESUMEN

En resumen, procede a juicio de esta parte, que:

1.- Con carácter inmediato, se proceda a la entrega a esta parte de los [IMPORTE EN LETRA] yyy [IMPORTE] € consignados por la demandada en concepto de intereses.
2.- Se requiera a la compañía de seguros demandada para que abone a mi representada [NOMBRE DEL REPRESENTADO/A] uuu [IMPORTE] € en concepto de intereses devengados desde la fecha del siniestro hasta la consignación por ella realizada.
3.- Se requiera a la demandada para que abone a mí representada [IMPORTE EN LETRA] vvv [IMPORTE] € en concepto de intereses devengados desde el día siguiente a la consignación realizada por la llegada de los autos a este Tribunal.

Por lo expuesto,

SUPLICO AL TRIBUNAL

que acuerde tener por presentada la liquidación de intereses, y se sirva ordenar el pago de la cantidad calculada, previo el trámite procesal oportuno, y con carácter previo a ello, y a la mayor brevedad que las ocupaciones de S.S.ª Ilma. lo permita, haga entrega a mi representada de los [IMPORTE EN LETRA] yyy [IMPORTE] € consignados por la demandada en concepto de intereses.

Por ser de Justicia que pido en [LUGAR], a [FECHA].

Firma de Abogado/a	Firma de Procurador/a

========================================================================
