---
name: impugnacion-ejecutante-liquidacion-intereses-ejecutado-civ-1583
description: "Impugnación del ejecutante a la liquidación de intereses del ejecutado opuesto a la ejecución. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Impugnación del ejecutante a la liquidación de intereses del ejecutado opuesto a la ejecución

> Formulario **CIV-1583** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Escrito de impugnación de la relación de intereses liquidados por la parte ejecutada opuesta, que deduce la ejecutante, ratificando la pretensión ejecutiva

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Impugnación del ejecutante a la liquidación de intereses del ejecutado opuesto a la ejecución» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Impugnación del ejecutante a la liquidación de intereses del ejecutado opuesto a la ejecución” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:impugnacion-ejecutante-liquidacion-intereses-ejecutado-civ-1583`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] FECHA (2 veces)
- [ ] ASEGURADORA
- [ ] AÑO
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] Nº
- [ ] SEDE

## Normas que cita el formulario

- art. 575 LEC
- art. 20 LCS
- art. 394.2 LEC
- art. 585 LEC

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
(1) El cálculo o cuenta de intereses de mora puede producirse en dos momentos del proceso de declaración, y dos del de ejecución. Al ejercerse una pretensión declarativa de condena, se cuantificarán los vencidos al momento de interponer la demanda, fijándose las bases de los que están por correr, y luego se cuantificarán hasta el dictado de la sentencia estimatoria en ésta, estando fijadas legalmente las bases de los que corren a partir de entonces. Al ejercerse la pretensión de ejecución derivada, se calculan los vencidos hasta el momento de la demanda ejecutiva, estando legalmente fijadas las bases de los que corren desde entonces, y luego se cuantificarán hasta el pago definitivo cuando éste se produzca. En principio, son operaciones que no requieren de un genuino proceso de liquidación de los arts. 712 y ss. LEC. Pero si falta algún dato en la sentencia no parece que pueda prescindirse de un trámite liquidatorio. Es la opción del modelo, como fórmula de conceder salida al problema de que el ejecutado que paga discuta la cuantificación del ejecutante en la demanda ejecutiva, que no está previsto en la norma

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

D./Dña [NOMBRE Y APELLIDOS], Procuradora de los Tribunales, actuando en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS], según tengo acreditado en los autos de EJECUCIÓN DE TÍTULO JUDICIAL n.º [Nº]/[AÑO], ante el Tribunal comparezco y como mejor proceda en Derecho, DIGO:

Que dentro del plazo de cinco días desde el traslado proveído del escrito de la parte ejecutada en que se oponía al Auto de despacho de ejecución, procedo a impugnar la liquidación de intereses formulada como oposición de contrario, sobre la base de los siguientes:

HECHOS

ÚNICO.-

La Sentencia recaída en este procedimiento condena a la entidad demandada al pago solidario de una cantidad con carácter de principal, con más sus intereses del art. 20 de la Ley de Contrato de Seguro (LCS).

No se niega por la parte ejecutada, sino que reconoce el impago de cantidad alguna tras haber transcurrido más de dos años desde ocurrido el siniestro, y que sólo se ha producido consignación en pago tras haber sido instada por esta parte la ejecución de la sentencia en fecha 1 de febrero de 2002.

La ejecución se solicitó, conforme establece el art. 575 LEC, por el importe del principal más los intereses moratorios (del art. 20 LCS) vencidos a la fecha de presentación del escrito, y calculados hasta el 1 de febrero de 2002, a pesar de no existir aún en dicha fecha consignación alguna por parte de la compañía demandada, con lo cual el ‘dies ad quem’ del devengo todavía no estaba determinado, y desde luego no era dicha fecha, como pretende la ejecutada.

La fecha de final del devengo tampoco es la del día en que ingresó la demandada en la cuenta del Tribunal la cantidad que ha sido entregada a esta parte, y supone intereses moratorios inferiores, sino la de notificación de la providencia que tiene por efectuada la consignación y lo comunica a esta parte, con orden de pago, a fin de manifestación sobre los intereses liquidados en definitiva. Así:

Transcurridos desde 02/02/02 a 29/03/02= 60 días

-52.600’12 (20%)/365= 28’82 €/día / 60 x 28’82 = 1.729’20 €

Por consiguiente, el TOTAL debido asciende a 63.157'25 + 1.729’20 = 64.886’45 €.

Si se descuenta de lo que ofrece la parte demandada acreedora, resulta una deuda pendiente de: 64.886’45- 64.310'05 = 576‘40 €

A los anteriores hechos resultan de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

PRIMERO. Se rechazan todos los que han sido citados en el escrito de oposición, en la medida en que sean distintos a los que fueron alegados en la demanda ejecutiva y a los que en este escrito se mencionan.

Esta parte da por reproducidos los fundamentos jurídicos aducidos en la demanda rectora del proceso ejecutivo, con la finalidad de evitar tediosas reiteraciones.

SEGUNDO. Sentencia de la Audiencia Provincial de [LOCALIDAD] de fecha [FECHA]

TERCERO. En cuanto a las costas son de aplicación los arts. 394.2 y 561 LEC, debiendo imponerse al ejecutado de desestimarse su oposición.

En virtud de los hechos y fundamentos jurídicos invocados y de cualesquiera otros que resultaren de empleo,

AL TRIBUNAL SUPLICO

que, teniendo por presentado este escrito de impugnación a la oposición ejecutiva, junto con justificación de haber trasladado la copia simple al Procurador de la ejecutada, se sirva admitirlo, teniendo por contestada la oposición a la ejecución despachada, y que se plantea de contrario como liquidación de intereses moratorios divergentes, y tras los trámites legales pertinentes, se dicte auto por el que, desestimando totalmente la oposición, se declare procedente que la ejecución siga adelante por la cantidad pendiente de pago de QUINIENTOS SETENTA Y SEIS euros y CUARENTA céntimos (576’40 €), todo ello con expresa imposición de costas al ejecutado.

Es Justicia que solicito en [LUGAR], a [FECHA].

OTROSÍ DIGO: Que con relación al traslado de la solicitud de levantamiento del embargo por Cía de Seguros [ASEGURADORA], S.A., la ejecución está despachada por cantidad de 82.057'25 €, que incluye lo presupuestado para intereses y costas del proceso de ejecución, de tal forma que si la parte ejecutada pretende tal levantamiento debió consignar dicha cantidad para oponerse, según resulta de los arts. 585 y 586 LEC, sin que resulte de aplicación, como queda dicho, el art. 558 respecto de la oposición por pluspetición.

Habiéndose entregado la cantidad de 64.310'05 € a esta parte, se manifiesta la resistencia a que se produzca el levantamiento de embargo en la cifra que resta hasta aquella por la que fue despachada la ejecución (17.747'20 €), en tanto no se liquiden en firme intereses y costas.

AL TRIBUNAL SUPLICO que, teniendo por causada la manifestación antecedente al efecto del traslado conferido por el Tribunal, se tenga a mis representados por contrarios al alzamiento de embargo, sólo autorizándose su reducción.

Reitero Justicia en lugar y fecha que constan.

Firma de Abogado/a	Firma de Procurador/a
