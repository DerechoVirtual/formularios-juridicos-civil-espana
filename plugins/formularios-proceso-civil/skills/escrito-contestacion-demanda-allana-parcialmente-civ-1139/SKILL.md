---
name: escrito-contestacion-demanda-allana-parcialmente-civ-1139
description: "Escrito de contestación a la demanda que se allana parcialmente a las pretensiones del actor. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito de contestación a la demanda que se allana parcialmente a las pretensiones del actor

> Formulario **CIV-1139** del plugin **Proceso civil: demandas, contestaciones, prueba y vista** (`formularios-proceso-civil`) · Civil › Escritos procesales (demanda, contestación, prueba, vista) · normativa revisada el 24-11-2026.

## Qué es

Contestación a la demanda de juicio ordinario en la que el demandado se allana parcialmente a las pretensiones del actor (aquí, el pago del precio de unos suministros, con consignación judicial de lo adeudado y sus intereses legales) y se opone al resto, en particular a la revalorización de la deuda y a los pedimentos indemnizatorios, sin imposición de costas.

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito de contestación a la demanda que se allana parcialmente a las pretensiones del actor» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito de contestación a la demanda que se allana parcialmente a las pretensiones del actor” para mi caso». También puedes invocarla directamente con `/formularios-proceso-civil:escrito-contestacion-demanda-allana-parcialmente-civ-1139`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-proceso-civil:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Proceso civil: demandas, contestaciones, prueba y vista) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (3 veces)
- [ ] FECHA (2 veces)
- [ ] FIRMA (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NOMBRE O DENOMINACIÓN SOCIAL DEL ACTOR (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A (2 veces)
- [ ] AÑO
- [ ] DÍA
- [ ] HECHO NEGADO
- [ ] INDICAR CUÁLES
- [ ] MES
- [ ] NOMBRE O DENOMINACIÓN SOCIAL DEL DEMANDADO
- [ ] NOMBRE Y APELLIDOS DEL LETRADO/A
- [ ] Nº
- [ ] Nº DE DOCUMENTO
- [ ] Nº DE PROCEDIMIENTO
- [ ] PORCENTAJE
- [ ] SEDE
- [ ] Y, EN SU CASO:

## Normas que cita el formulario

- art. 23 LEC
- art. 31 LEC
- art. 1108 CC
- art. 394 LEC

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

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, en nombre y representación de [NOMBRE O DENOMINACIÓN SOCIAL DEL DEMANDADO], según acredito en virtud de escritura de poder especial con expresa facultad de allanamiento, inscrita en el Registro Electrónico de Apoderamientos Judiciales, a cuya justificación aporto certificación de dicho Registro como documento n.º [Nº DE DOCUMENTO], en los autos de juicio ordinario n.º [Nº DE PROCEDIMIENTO] contra mi principal seguidos por [NOMBRE O DENOMINACIÓN SOCIAL DEL ACTOR], dirigido por el Letrado/a abajo firmante D./Dña. [NOMBRE Y APELLIDOS DEL LETRADO/A], con despacho profesional en [LOCALIDAD], ante el Tribunal comparezco y, como mejor proceda en Derecho, DIGO:

Que, evacuando el traslado conferido y cumpliendo instrucciones expresas de mi mandante, vengo a allanarme parcialmente a las pretensiones contenidas en la demanda presentada por [NOMBRE O DENOMINACIÓN SOCIAL DEL ACTOR] y a formular contestación a la demanda según los hechos y fundamentos de derecho que se exponen a continuación:

ALLANAMIENTO

El actor presenta en su demanda una cantidad que se reclama en virtud de una serie de contratos de suministro de material electrónico efectuados a favor de mi representada.

Esta parte se allana parcialmente a las pretensiones formuladas en la demanda en cuanto a la entrega del material electrónico contratado y recepcionado totalmente de conformidad, consignando judicialmente a disposición de la parte actora la cantidad de [IMPORTE] euros, correspondiente a lo adeudado, de [IMPORTE] euros, y el resto a los intereses legales desde el día [FECHA] al [FECHA], calculados al [PORCENTAJE] por ciento de acuerdo con la Ley de Presupuestos Generales del Estado, oponiéndose a los pedimentos indemnizatorios de la demandante en el sentido en que vienen formulados, invocando a sensu contrario los preceptos que aquélla hizo valer en apoyo de sus pretensiones, como oportunamente desarrollaré en mi contestación.

CONTESTACIÓN A LA DEMANDA

Paso a contestar la demanda con base en los siguientes

HECHOS

PRIMERO.– De conformidad con el hecho primero de contrario.

SEGUNDO.– No es cierto el hecho correlativo de la demanda, en el sentido de que [HECHO NEGADO], como se desprende del documento n.º [Nº] que se acompaña.

TERCERO.– Esta parte reconoce los hechos contenidos en el correlativo de la demanda [INDICAR CUÁLES].

[Y, EN SU CASO:] Se niega expresamente el correlativo de la demanda.

A estos hechos les son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

I, II.– Conforme esta parte con la competencia y el tipo de procedimiento señalados por el actor en el correlativo de la demanda.

III, IV, V.– De conformidad con los expuestos de contrario.

VI.– POSTULACIÓN Y DEFENSA

La parte está representada por el Procurador/a [NOMBRE Y APELLIDOS DEL PROCURADOR/A], legalmente habilitado según el art. 23 LEC, y defendida por el Letrado/a que consta en el encabezamiento, art. 31 LEC.

VII.– FONDO DEL ASUNTO

La cuestión básica viene determinada por la petición de la demandante relativa a la revalorización de la cantidad adeudada, al pretender su pago en [IMPORTE] euros constantes a una determinada fecha, conectando la cuestión con la problemática de las denominadas deudas de valor.

En este punto puede decirse, en principio, que debe ser tenida como deuda de valor aquella en que la prestación no está integrada por dinero o, en su caso, cuando, consistiendo la prestación en dinero, no se debe meramente una cantidad de dinero sino su valor, valor que se sobrentiende tiene que ser distinto del nominal, ya que en esto consiste stricto sensu la deuda dineraria; y, en síntesis, lo decisivo y esencial es que se deba un valor y que este valor no sea el nominal del dinero. Lo expuesto lleva a considerar que, como consecuencia del contrato para la adquisición de material electrónico que mi representada suscribió con la actora, se obligó a pagar el precio de la adjudicación, esto es, una concreta y determinada suma de dinero, sobre la que por la actora se pretende percibir unos intereses especiales por razón de unos supuestos perjuicios que dice se le derivaron de las incidencias que surgieron a lo largo de sus relaciones con mi patrocinada, en particular las obligaciones que por su parte tuvo que contraer hasta obtener el pago de la demandada por cuenta de diferentes operaciones, en parte marginales a la que nos ocupa.

Si se contempla el suplico de la demanda, en el mismo se pide el cumplimiento del contrato (pago del precio por el adquirente) y, junto a ello, el abono de intereses moratorios, esto es, el pago de una deuda dineraria pura, sometida en principio a los avatares del criterio nominalista al que se acoge nuestro Código Civil (art. 1170). Por consecuencia, la exclusión del valor nominal del dinero como medio de determinar el importe de lo debido sólo podría operarse con la entrada en juego de medios correctores con base en la ley, el pacto o una alteración de circunstancias notoriamente alteradora del justo y preciso equilibrio de las prestaciones, lo que en ningún caso resulta de predicamento con respecto al asunto que se trata. De aquí que, supuesta la mora, la pretensión de resarcimiento por encima de lo que dinerariamente se debe en relación con los intereses exige la prueba de que, efectivamente, la dilación en el pago ha originado efectivo perjuicio, ya por la necesidad de acudir a créditos especialmente gravosos, ya por haberse producido una oscilación devaluatoria importante, lo que no se ha dado con referencia al asunto litigioso, en el que, por lo demás, podría ponerse en entredicho la existencia de efectiva mora, en cuanto que su apreciación exige, según reiterada doctrina jurisprudencial, una base fáctica de apoyo que, habida cuenta de las múltiples y complejas relaciones entre los litigantes, no ha sido acreditada en su sentido de resistencia o rebeldía al pago, ya que el mero retraso en completar el pago no constituye por sí mora [STS de 7 de abril de 1993].

Por todo lo expuesto, la función indemnizatoria de los daños y perjuicios imputables a la simple mora, admitida por esta parte vía allanamiento parcial, debe desenvolverse a través del abono del interés fijado por pacto, por disposición legal específica o del interés legal, único supuesto este último aplicable al caso (art. 1108 CC).

VIII.– COSTAS

No concurriendo en mi mandante la mala fe que establece el art. 394 LEC, no procede su expresa condena en costas.

Por lo expuesto,

SUPLICO AL TRIBUNAL.

Que, teniendo por presentado este escrito con los documentos y copias que le acompañan, lo admita y se me tenga por personado/a y parte en la representación que ostento, entendiéndose conmigo las sucesivas diligencias, y tenga a mi representado/a por allanado/a parcialmente a las pretensiones formuladas por el actor en su escrito de demanda y por contestada en tiempo y forma la demanda en los términos formulados en este escrito, rechazándose las peticiones de la parte actora en todo lo que no haya sido expresamente admitido en el escrito de contestación, y dicte sentencia rechazando las pretensiones del actor no comprendidas en el allanamiento, sin hacer especial condena de las costas causadas a mi representado/a.

Es justicia que debe hacerse en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Abogado/a: [FIRMA] Firma del Procurador/a: [FIRMA]
