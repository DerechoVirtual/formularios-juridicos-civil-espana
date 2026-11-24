---
name: demanda-ejecucion-hipotecaria-sobre-vivienda-habitual-civ-1426
description: "Demanda de ejecución hipotecaria sobre la vivienda habitual del deudor. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de ejecución hipotecaria sobre la vivienda habitual del deudor

> Formulario **CIV-1426** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de ejecución hipotecaria sobre la vivienda habitual del deudor» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de ejecución hipotecaria sobre la vivienda habitual del deudor” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:demanda-ejecucion-hipotecaria-sobre-vivienda-habitual-civ-1426`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (9 veces)
- [ ] NOMBRE Y APELLIDOS (9 veces)
- [ ] AÑO (6 veces)
- [ ] FECHA (6 veces)
- [ ] LOCALIDAD (6 veces)
- [ ] Nº (5 veces)
- [ ] MES (4 veces)
- [ ] SEDE (4 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] CALLE (2 veces)
- [ ] PISO (2 veces)
- [ ] PORCENTAJE (2 veces)
- [ ] COLEGIO
- [ ] DÍA
- [ ] FECHAS
- [ ] FINCA
- [ ] FOLIO
- [ ] FU
- [ ] LIBRO
- [ ] LUGAR
- [ ] Nº DE COLEGIADO
- [ ] Nº DE PLAZOS
- [ ] OTROS DATOS
- [ ] PUERTA
- [ ] TOMO

## Normas que cita el formulario

- art. 129 LH
- art. 24 Ley 5/2019
- art. 685.2 LEC
- art. 693.2 LEC
- art. 575.1bis LEC
- art. 686 LEC
- art. 684.1.1 LEC
- art. 682.2 LEC
- art. 682.3 LEC
- art. 25 Ley 5/2019
- art. 688 LEC
- art. 656.1 LEC
- art. 693.3 LEC
- art. 7.2 Ley 10/2012

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: Un solo TI por partido judicial (art. 84.1 LOPJ): sobra «de los de». Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

D./Dª. [NOMBRE Y APELLIDOS] Procurador/a de los Tribunales, en nombre y representación de D./Dª. [NOMBRE Y APELLIDOS], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], bajo la dirección Letrada de [NOMBRE Y APELLIDOS], Abogado colegiado núm. [Nº DE COLEGIADO] del Iltre. Colegio de Abogados de [COLEGIO], ante la Sección Civil del Tribunal de Instancia de [SEDE] que por turno de reparto corresponda comparezco y, como mejor proceda en Derecho, DIGO:

Que en la indicada representación, y siguiendo instrucciones de mi mandante, por medio del presente escrito promuevo DEMANDA DE EJECUCIÓN BIENES HIPOTECADOS al amparo de los artículos 681 y ss. de la LEC contra el deudor hipotecario [NOMBRE Y APELLIDOS], la cual baso en los siguientes

HECHOS

Suscripción de la garantía hipotecaria sobre vivienda habitual. Título de la ejecución

Que en virtud de la adquisición del ahora demandado de la que es su vivienda habitual, el día [FECHA], del mes [MES] del año [AÑO], sita en la localidad de [LOCALIDAD], calle [CALLE], piso [PISO], puerta [PUERTA], resulta que mi principal es acreedor del demandado de ejecución hipotecaria por la cantidad de [IMPORTE] euros.

Que ante el Notario de [LOCALIDAD], D. [NOMBRE Y APELLIDOS], el mismo día en que se formalizó la adquisición, el ahora demandado se comprometió al pago de la cantidad adeudada en [Nº DE PLAZOS] plazos sucesivos. En concreto el vencimiento del primer plazo sería el [FECHA] y el del último plazo el [FECHA], pagándose en cada uno de los plazos la cuota fija de [IMPORTE] euros, que comprende el principal y los intereses calculados al [PORCENTAJE] tanto por 100 sobre el capital pendiente en cada momento, con arreglo a la fórmula financiera plasmada en documento suscrito por las partes y que se incorpora como Anexo a la escritura notarial.

Que para garantizar el pago del principal que importa un total de [Nº], así como de los intereses que ascienden a la suma de [IMPORTE] euros, el ahora demando constituyó garantía hipotecaria a favor de mi principal sobre el inmueble de su propiedad que constituye su vivienda habitual y que pasamos a identificar:

Que la mencionada garantía hipotecaria se elevó a escritura pública el día [FECHA] del mes [MES] del año [AÑO], ante el Notario de [LOCALIDAD], D. [NOMBRE Y APELLIDOS], protocolo núm. [Nº] del año [AÑO], acompañando en prueba de lo manifestado copia de la citada escritura como documento núm. [Nº], así como nota simple de inscripción en el Registro de Propiedad de los de [SEDE] al tomo [TOMO], libro [LIBRO], folio [FOLIO], finca [FINCA], como documento núm. [Nº DE DOCUMENTO].

Que entre las diversas cláusulas que constan en el contrato de garantía hipotecaria, en apoyo de nuestras pretensiones, son de destacar las siguientes:

1.- Cláusula quinta: "En el supuesto de que a sus respectivos vencimientos el deudor deje de pagar de forma total o parcial cualquiera de los plazos pactados, el acreedor podrá acudir, para obtener el cobro de la totalidad de lo adeudado por capital y por intereses, al ejercicio de la acción hipotecaria directa contra la finca sobre la que recae la garantía, de conformidad con los artículos 129 y 130 de la LH y 681 y ss. de la LEC".

Debe advertirse, a los efectos contemplados en la disposición transitoria primera, apartado 4, de la Ley 5/2019, de 15 de marzo, que el régimen de vencimiento anticipado del art. 24 de la citada Ley 5/2019 es más favorable para el deudor.

2.- Cláusula sexta: "A los efectos del ejercicio de la acción hipotecaria directa contra la finca sobre la que se constituye la garantía pactada en este contrato, las partes tasan la mencionada finca en el importe de…………………… euros, precio que servirá como tipo para la subasta de la finca llegado el caso".

3.- Cláusula séptima: "El domicilio fijado por el deudor a los efectos de que se practiquen los requerimientos y notificaciones pertinentes es el sito en la localidad de [LOCALIDAD], calle [CALLE], piso [PISO], puerta ".

Constituyendo el inmueble la vivienda habitual del deudor, de conformidad a lo dispuesto en el art. 685.2 de la LEC, modificado por Ley 12/2023, se expresan los siguientes extremos:

-Mi representada SÍ/NO tiene la condición de gran tenedora de vivienda ( a efectos acreditativos de que mi representada no es gran tenedora aporto certificado del Registro de la Propiedad como documento número…………).

Tutela ejecutiva que se pretende

Que si bien el deudor cumplió con el pago de los ocho primeros vencimientos de los plazos estipulados, desatendió los catorce siguientes plazos con vencimiento los días [FECHAS], del mes [MES] del año [AÑO], suma de dinero que sigue adeudando a fecha de interposición de la presente demanda.

Mi representada, de conformidad con lo dispuesto en el art. 693.2 de la LEC en relación con el art. 24 y disposición transitoria primera, apartado 4, de la Ley 5/2019, de 15 de marzo, reguladora de los contratos de crédito inmobiliario, al hallarse el préstamo en la primera mitad de su duración y haber incurrido el deudor en mora por más de doce plazos mensuales de capital vencidos y no satisfechos, remitió requerimiento notarial al deudor el pasado día [FECHA], ¡ concediéndole un plazo de un mes para el cumplimiento y advirtiéndole de que, de no ser atendido, se reclamaría el reembolso total adeudado del préstamo. El requerimiento fue recibido por el deudor el pasado día, según acredito por copia notarial auténtica que acompaño, sin que haya satisfecho cantidad alguna hasta la fecha pese a haber transcurrido en exceso el plazo concedido.

Por tanto, de conformidad con los preceptos expresados, con fecha [FECHA], posterior a la entrada en vigor de la citada Ley 5/2019, se dio por vencido anticipadamente el préstamo, procediendo a la reclamación del total de lo adeudado según contempla el art. 693.2 de la LEC en relación con el art. 24 y disposición transitoria primera, apartado 4, de la Ley 5/2019.

Que el importe de la deuda que se reclama asciende a [IMPORTE] euros, con arreglo a lo pactado en cuanto a los importes de los plazos y como se desprende del hecho primero de la presente demanda.

Al citado importe habrá que adicionar en concepto de intereses moratorios, una vez que se pactaron en el [PORCENTAJE] tanto por 100, otros [IMPORTE] euros devengados en concepto de intereses por demora en el pago acontecida desde el incumplimiento hasta la fecha de interposición de la presente demanda de ejecución hipotecaria. (caso de limitación de intereses moratorios [OTROS DATOS]).).

Que igualmente, a los anteriores importes habrá que sumar [IMPORTE] euros que se reclaman a los efectos de cubrir el pago de los intereses de demora que se generen desde la fecha de la demanda hasta el pago así como las costas que se causen en esta ejecución, tomando en consideración lo dispuesto en el artículo 575.1bis de la LEC, sin que se exceda el límite legal del 30 por 100 de las cantidades reclamadas como principal, intereses ordinarios e intereses de demora.

Despacho de ejecución

Que interesa al derecho de esta parte señalar que se ha practicado el requerimiento de pago al deudor en cumplimiento de lo establecido en el art. 24 de la Ley 5/2019 para el vencimiento anticipado, con concesión de plazo de un mes para el pago de la cantidad pendiente y se han cumplido todas las prescripciones legales para el despacho de ejecución, por lo que se solicita que se dicte auto en que se autorice y despache ejecución, según lo dispuesto en el artículo 686 de la LEC.

A los anteriores hechos le son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

Competencia

En cuanto a la competencia, con arreglo a lo dispuesto en el artículo 684.1.1º de la LEC, señalar que resulta competente el Tribunal de Instancia de [SEDE] por ser esta localidad en la que radica el bien hipotecado objeto de este procedimiento de ejecución

Procedimiento

En cuanto al procedimiento aplicable, por tratarse de la ejecución directa y exclusiva de un bien hipotecado, es el regulado en los artículos 129 y 130 de la LH, así como en los artículos 681 y ss. de la LEC, habiéndose cumplido con los requisitos previstos en el artículo 682.2 de la LEC, consistentes en la determinación en la escritura de hipoteca del precio que servirá del tipo para la subasta así como el domicilio del deudor para la práctica de requerimientos y notificaciones, quedando constancia registral de ambas cuestiones con arreglo a lo dispuesto en el artículo 682.3 de la LEC.

Legitimación

La legitimación activa la ostenta mi representado en cuanto afirma ser el acreedor de la deuda garantizada con la finca hipotecada objeto de este procedimiento de ejecución hipotecaria.

La legitimación pasiva corresponde al demandado por ser la persona que figura como deudor de las cantidades reclamadas y ser el propietario del bien hipotecado que garantiza dicha deuda.

Tratándose de vivienda habitual, en la demanda se expresan las circunstancias del acreedor y del deudor, y se acredita el cumplimiento de los requisitos establecidos en el art. 685.2 de la LEC.

Vencimiento

Es de aplicación lo dispuesto en el artículo 693.2 de la LEC, que establece que podrá reclamarse la totalidad de lo adeudado por capital y por intereses en los términos en los que así se hubiese convenido en la escritura de constitución y consten en el asiento respectivo. Siempre que se trate de un préstamo o crédito concluido por una persona física y que esté garantizado mediante hipoteca sobre vivienda o cuya finalidad sea la adquisición de bienes inmuebles para uso residencial, se estará a lo que prescriben el artículo 24 de la Ley 5/2019, reguladora de los contratos de crédito inmobiliario y, en su caso, el artículo 129 bis de la Ley Hipotecaria, siendo de aplicación a los contratos preexistentes vencidos con posterioridad al 16 de junio de 2019 según establece la disposición transitoria primera, apartado 4, de la citada Ley 5/2019..

Intereses de demora

Tratándose de la vivienda habitual del deudor, conforme a lo dispuesto en el artículo 114.III de la Ley Hipotecaria y art. 25 de la Ley 5/2019, los intereses de demora de préstamos o créditos para la adquisición de vivienda habitual, garantizados con hipotecas constituidas sobre la misma vivienda, serán el interés remuneratorio más tres puntos porcentuales a lo largo del periodo que aquel resulte exigible. El interés de demora sólo podrá devengarse sobre el principal vencido y pendiente de pago y no podrá ser capitalizado en ningún caso, salvo en el supuesto previsto en el artículo 579.2.a) de la Ley de Enjuiciamiento Civil. En este caso, el préstamo concertado por mi representada respeta dicho límite legal por lo que procede despachar ejecución también por los intereses de demora reclamados.

[FU]

Costas

Sobre costas, será de aplicación lo dispuesto en los artículos 394, 539.2, 575.1 bis y 583.2 de la LEC.

Por todo lo expuesto,

SUPLICO AL TRIBUNAL: Que tenga por presentado este escrito con los documentos acompañados y sus copias, lo admita, y previo testimonio suficiente del poder para pleitos en autos, se proceda a la devolución del original por ser necesario para otros usos, dándose a las copias el curso legal, teniendo por comparecido y parte en la representación que ostento al Procurador [NOMBRE Y APELLIDOS] en la representación de D./Dª. [NOMBRE Y APELLIDOS], teniendo por promovida DEMANDA DE EJECUCIÓN BIENES HIPOTECADOS al amparo de los artículos 681 y ss. de la LEC contra el deudor hipotecario [NOMBRE Y APELLIDOS], para exigir el pago de la totalidad de lo adeudado por capital y por intereses de la deuda garantizada con el bien hipotecado que asciende a [IMPORTE] euros del plazo impagado, más [IMPORTE] euros de intereses de demora hasta la interposición de la demanda, más [IMPORTE] euros para cubrir el resto de intereses de demora y las costas ocasionadas por este procedimiento; y previos los trámites con arreglo a derecho se proceda a despachar ejecución contra el deudor ejecutado y, previos los trámites procesales legalmente previstos, se proceda a señalar día y hora para la celebración de subasta pública subasta del bien hipotecado, para que con el producto obtenido se proceda a pagar a mi representado de las cantidades que se le adeudan y se liquiden los demás intereses y costas generados por la presente ejecución.

OTROSÍ DIGO I: Que de conformidad con lo establecido en el artículo 688 de la LEC deberá procederse a la reclamación del Registrador de la Propiedad núm. [Nº] de [LOCALIDAD], la certificación que contenga los extremos a que se refiere el artículo 656.1 LEC y en la que se haga constar que la carga hipotecaria a favor de mi representado se haya subsistente y sin cancelar.

Por ello,

SUPLICO AL TRIBUNAL: Que se proceda al libramiento del correspondiente mandamiento al Registro de la propiedad núm. [Nº] de [LOCALIDAD] al objeto de que proceda a expedir la certificación establecida en el artículo 688 de la LEC y se proceda a realizar anotación marginal en la inscripción de la hipoteca en la que se constate el libramiento de la misma indicando fecha y procedimiento a que está referida.

OTROSÍ DIGO II: Que siendo el bien hipotecado una vivienda familiar, si bien el deudor puede aun sin el consentimiento del acreedor puede liberar el bien mediante la consignación de los importes correspondientes a principal e intereses, al amparo de lo dispuesto en el artículo 693.3 de la LEC, interesa al derecho de esta parte se aperciba al deudor que liberado un bien por primera vez, podrá liberarse en segunda o ulteriores ocasiones, siempre que al menos, medien tres años entre la fecha de la liberación y la del requerimiento de pago judicial o extrajudicial efectuada por el acreedor.

Por lo que,

SUPLICO AL TRIBUNAL: Que tenga por realizada la anterior manifestación a todos los efectos, y previos los trámites con arreglo a derecho acuerde de conformidad con lo interesado, dando a los autos el impulso procesal con arreglo a derecho.

OTROSÍ DIGO.- Que estando la presente demanda sujeta al abono de la tasa por el ejercicio de la potestad jurisdiccional fijada por la Ley 10/2012, de 20 de noviembre, modificada por RDL 3/2013 y Ley 25/2015, de 28 julio, y desarrollada por Orden HAP/2662/2012, de 13 de diciembre, siendo mi representada personas jurídica no exenta de su pago, se acompaña a la presente demanda como documento nº [Nº DE DOCUMENTO] la correspondiente autoliquidación con el ejemplar para la Administración de Justicia debidamente validado y en el que consta el pago de la cantidad de 200 euros correspondiente a la cuota fija, sin que se incluya la cuota variable prevista en el artículo 7.2 de la Ley 10/2012 al haber sido declarado inconstitucional y nulo por la STC 140/2016, de 21 de julio.

Por lo que,

SUPLICO AL TRIBUNAL: que tenga por hecha la anterior manifestación a los efectos pertinentes y por acompañado el documento justificativo del abono de la tasa

Es Justicia que insto en [LUGAR], a [DÍA] de [MES] de [AÑO].l año [AÑO]

Firma de Letrado Firma de Procurador

========================================================================
