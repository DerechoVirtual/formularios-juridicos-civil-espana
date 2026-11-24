---
name: demanda-desahucio-impago-reclamacion-rentas-sin-civ-0552
description: "Demanda de desahucio por impago y reclamación de rentas, sin enervación y con condonación de deuda. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de desahucio por impago y reclamación de rentas, sin enervación y con condonación de deuda

> Formulario **CIV-0552** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 24-11-2026.

## Qué es

Parte HECHOS FUNDAMENTOS DE DERECHO Suplico de presentación de demanda Otrosí de cuantía Otrosí para designar domicilio en caso de actos de comunicación y solicitud de práctica de requerimiento Otrosí de Vigentecitadisposición adicional quinta de la LEC Otrosí sobre las circunstancias de enervación correlativo al fundamento de la demanda Otrosí de compromiso de condonación total o parcial correlativo al fundamento de la demanda Otrosí solicitando la ejecución directa del lanzamiento Otrosí de Tasa Firmas

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de desahucio por impago y reclamación de rentas, sin enervación y con condonación de deuda» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de desahucio por impago y reclamación de rentas, sin enervación y con condonación de deuda” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:demanda-desahucio-impago-reclamacion-rentas-sin-civ-0552`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (6 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] CALLE (2 veces)
- [ ] FECHA (2 veces)
- [ ] MES (2 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] AÑO
- [ ] DÍA
- [ ] FOLIO
- [ ] LIBRO
- [ ] LUGAR
- [ ] MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] Nº
- [ ] PISO
- [ ] PLAZO
- [ ] PUERTA
- [ ] SEDE
- [ ] TOMO

## Normas que cita el formulario

- art. 439.6 LEC
- art. 3 k) Ley 12/2023
- art. 22.4 LEC
- art. 250.1.1 LEC
- art. 438.5 LEC
- art. 438.3 LEC
- art. 85.1 LOPJ
- art. 437.1 LEC
- art. 5 Ley Orgánica 1/2025
- art. 437 LEC
- art. 1108 Código Civil
- art. 220.2 LEC
- art. 394 LEC
- art. 438 LEC
- art. 441.5 LEC
- art. 252 LEC
- art. 155 LEC
- art. 161 LEC
- art. 152.1 LEC
- art. 21 LEC
- art. 549.3 LEC
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

### Avisos de actualización (1) — se aplican en el texto, nunca se copian en el documento

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] Q.P.T.R.C.»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] Q.P.T.R.C.

Don [NOMBRE Y APELLIDOS], Procurador de los Tribunales, en nombre y representación de Don [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], según acredito con la copia electrónica del poder notarial de representación informática (o digitalizada) general para pleitos que acompaño y cuya devolución solicito previa unión a los autos de testimonio suficiente, por ser necesaria para otros asuntos, ante el Tribunal comparezco y DIGO:

Que formulo demanda de juicio verbal de desahucio por falta de pago de la renta pactada contractualmente y acumuladamente demanda de reclamación de las rentas vencidas y no satisfechas contra Don [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], y fundo mi pretensión en los siguientes:

HECHOS

Primero.- Mi mandante es [ELEGIR: propietario / usufructuario] de la finca urbana sita en esta Ciudad, calle [CALLE], nº [NÚMERO] inscrita en el Registro de la Propiedad de [LOCALIDAD], Libro [LIBRO], Tomo [TOMO] Folio [FOLIO] Adjunto copia de la escritura pública, como doc. nº 1.

Al amparo de lo establecido en el artículo 439.6 de la LEC, se hace constar que:

Mi mandante NO tiene la condición de gran tenedora de vivienda en los términos que establece el art. 3 k) de la Ley 12/2023, según se acredita por la certificación del Registro de la Propiedad donde figura la relación de propiedades de mi representada, que acompaño como documento número 1 bis.

Según se recoge en el contrato, el inmueble SÍ constituye la vivienda habitual de la persona arrendataria.

Segundo.- La vivienda sita en el piso [PISO] puerta [PUERTA] fue cedida por mi principal en arrendamiento al demandado en virtud de contrato de fecha [FECHA], en el que se pactó una renta mensual actualizable anualmente en los términos que resulta de la cláusula 10ª del contrato. Esta renta -y las cantidades a ella asimiladas- es pagadera por meses anticipados, dentro de los cinco primeros días de cada mes, pasándose el cobro de los recibos a la cuenta corriente de la entidad bancaria designada por el arrendatario. Acompaño copia del citado contrato como doc. nº 2.

Tercero.- Que desde hace dos meses la entidad bancaria ha retornado los recibos pasados al cobro por el arrendador, tal como consta al dorso de los mismos (adjunto copia de los recibos como docs. 3 y 4).

A efectos de rentas futuras, se hace constar expresamente que el importe de la última mensualidad reclamada asciende a [IMPORTE] euros, según se acredita en el doc. núm. 4 acompañado.

Cuarto.- Mi mandante requirió notarialmente al demandado en los términos y al amparo de lo establecido en el art. 22.4 de la LEC, con más de treinta días de antelación a la presentación de esta demanda, sin que hasta el momento de interponer la demanda se haya avenido a cumplir con la obligación pactada (acompaño como doc. núm. burofax remitido al arrendatario que consta recibido el día [FECHA]).

Quinto.- Teniendo en cuenta que el demandado adeuda los meses de [MES] y que la renta a satisfacer asciende a [IMPORTE] euros mensuales, la cantidad que en esta demanda de forma acumulada se reclama asciende a la suma total de [IMPORTE] euros, a la que habrá de sumarse la de las rentas que venzan durante el procedimiento y los intereses legales que correspondan.

Sexto.- Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento nº [Nº DE DOCUMENTO]

A estos hechos son de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

Primero.- La pretensión que se ejercita queda amparada en el art. 250.1.1ª de la LEC que tutela la recuperación de la posesión de una finca, dada en arrendamiento, por impago de la renta o de las cantidades debidas por el arrendatario y que, conforme al mismo precepto, se seguirá por los trámites del juicio verbal acumulándose la acción de desahucio por falta de pago y la de reclamación de rentas o cantidades vencidas y no pagadas, debiendo, conforme al articulo 438.5 de la LEC, requerirse al demandado por el Letrado de la Administración de Justicia a los efectos prevenidos en dicho precepto en plazo de diez días, advirtiéndole que si no atendiere el requerimiento de pago o no compareciere para oponerse o allanarse, se dictará decreto dando por terminado el juicio de desahucio, estimando la demanda y procediendo a su inmediato lanzamiento. Además, al amparo del número 3º del apartado tercero del artículo 438.3 de la LEC, la acumulación de la acción de desahucio por falta de pago y la de reclamación de rentas o cantidades vencidas y no pagadas es procedente con independencia de la cantidad que se reclame.

Segundo.- Corresponde la competencia para conocer de esta clase de procesos al Tribunal de Instancia del lugar en que se halle la finca a tenor de lo establecido en los arts. 85.1º LOPJ, 45, 47 y 52.1.7º de la LEC, al cual me dirijo.

Tercero.- El demandante tiene legitimación activa por ser el arrendador de la vivienda y el demandado está legitimado pasivamente por ostentar la cualidad de arrendatario tal como consta en el contrato aportado como documento nº 2.

A los efectos establecidos en el art. 439.6 de la LEC, se hace constar expresamente que:

-Mi representada es persona arrendadora que NO tiene la condición de gran tenedora de vivienda, según se acredita por el documento acompañado como 1bis.

-El inmueble constituye la vivienda habitual de la persona arrendataria, tal como consta en el contrato aportado como documento número 2.

Por lo demás, desde la STC 26/2025, de 29 de enero, no es obligatorio presentar informe de vulnerabilidad ni acreditar mediación previa.

Cuarto.- La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 en relación con el art. 437.1 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

Quinto.- Al tratarse de una finca urbana, es de aplicación el artículo 27.2.a) de la Ley de Arrendamientos Urbanos que faculta al arrendador a resolver el contrato de arrendamiento, entre otros casos, cuando el arrendatario incumpla su obligación de satisfacer la renta contenida o de las cantidades cuya obligación de pago haya asumido o corresponda al arrendatario.

Sexto.- La LEC en su artículo 439.3 exige que se indique en el escrito de demanda las circunstancias que concurran y que permitan o no la enervación de la acción en los términos que regula el art. 22.4 de la misma LEC.

En este caso la enervación es improcedente ya que se ha producido el requerimiento previo de pago sin ser atendido por el arrendatario conforme a lo expuesto en el hecho cuarto de esta demanda.

Séptimo.- Al amparo del apartado 3 del artículo 437 de la LEC, el arrendador anuncia en esta demanda que asume el compromiso de condonar al arrendatario toda la deuda (o parte de la deuda si fuera el caso), que asciende a la cantidad de [IMPORTE] euros, así como las costas, siempre que el arrendatario desaloje voluntariamente la vivienda dejándola vacua, libre y expedita a disposición de mi mandante dentro del plazo de [Nº] días (no inferior a 15 días), lo que deberá ponerse de manifiesto al demandado en el requerimiento que se realice para manifestar su aceptación a este compromiso.

Octavo.- Que al amparo del artículo 27 de la Ley de Arrendamientos Urbanos el incumplimiento por cualquiera de las partes de las obligaciones resultantes del contrato dará derecho a la parte que hubiere cumplido las suyas a exigir el cumplimiento de la obligación.

En este caso, el demandado ha disfrutado de la posesión de la vivienda cedida en arrendamiento incumpliendo su obligación de pagar la renta pactada en el apartado b) de la cláusula del contrato, en los términos convenidos por las partes. En el caso de que el demandado no atienda el requerimiento del Letrado de la Administración de Justicia, la falta de oposición supone el consentimiento a la resolución del contrato, según dispone el artículo 438.5 de la LEC.

Noveno.- Que al amparo del art. 1108 del Código Civil, las cantidades adeudadas devengan el interés legal desde que el deudor incurra en mora, siendo así que en este caso las mensualidades vencidas y no satisfechas han devengado el interés legal desde el primer día de cada mes. A dichos efectos adjuntamos la correspondiente liquidación de los intereses de demora por las cantidades adeudadas hasta el momento de presentar la demanda.

Décimo.-De conformidad con lo dispuesto en el art. 220.2 de la LEC en los casos de reclamación de rentas periódicas, cuando la acción de reclamación se acumule a la acción de desahucio por falta de pago o por expiración legal o contractual del plazo, y el demandante lo hubiere interesado expresamente en su escrito de demanda, la sentencia, el auto o el decreto incluirán la condena a satisfacer también las rentas debidas que se devenguen con posterioridad a la presentación de la demanda hasta la entrega de la posesión efectiva de la finca, tomándose como base de la liquidación de las rentas futuras, el importe de la última mensualidad reclamada al presentar la demanda.

Undécimo.- En cuanto a las costas, es de aplicación el último párrafo del artículo 438.5 de la LEC para el caso de falta de oposición, y el artículo 394 de la LEC para el caso que el demandado se oponga, debiendo imponerse las costas a la parte cuyas pretensiones sean totalmente desestimadas.

Y por cuanto antecede:

SUPLICO AL TRIBUNAL: Que tenga por presentada demanda de juicio de desahucio por falta de pago y la acumulada de reclamación de las rentas o cantidades vencidas y no pagadas, con su copia y documentos que la acompañan, que la admita y que me tenga por personado y parte en la representación que ostento de Don [NOMBRE Y APELLIDOS] en virtud de la copia electrónica del poder notarial de representación informática (o digitalizada) general para pleitos cuya devolución intereso previa unión a los autos de copia testimoniada (o designa apud acta), que se entiendan conmigo las sucesivas diligencias del juicio verbal civil de desahucio por falta de pago de la renta y de reclamación de rentas, y que:

1) se requiera al demandado en los términos que se indican en el artículo. 438, apartado 5, de la LEC, (caso de vivienda habitual, dando cumplimiento a lo prevenido en el art. 441.5 de la LEC), sin que proceda la enervación, y en el caso de no atender el requerimiento o no comparecer para oponerse o allanarse, se dicte decreto dando por terminado el juicio, con estimación de la demanda, decretando el lanzamiento, solicitando que se ejecute directamente conforme dejo interesado en el otrosí, y condenado al demandado al pago de las rentas debidas incluyendo las que se devenguen con posterioridad a la demanda hasta que mi mandante recupere la posesión efectiva de la finca, tomándose como base de la liquidación de las rentas futuras, el importe de la última mensualidad reclamada en esta demanda por importe de [IMPORTE] euros mensuales, más los intereses legales que procedan, e imponiendo las costas al demandado.

2) para el caso de oposición, tras el señalamiento y celebración de la vista con citación al demandado en legal forma con los apercibimientos establecidos en el apartado 5 del artículo 438 de la LEC, se dicte sentencia estimando la demanda de desahucio por falta de pago de la renta, decretando el lanzamiento, solicitando que se ejecute directamente conforme dejo interesado en el otrosí, y condenado al demandado al pago de las rentas debidas incluyendo las que se devenguen con posterioridad a la demanda hasta que mi mandante recupere la posesión efectiva de la finca, tomándose como base de la liquidación de las rentas futuras, tomando como base de liquidación la expuesta en el anterior apartado, más los intereses legales que procedan e imponiendo las costas al demandado.

OTROSÍ PRIMERO DIGO: Que fijo la cuantía del proceso en [IMPORTE] euros, que se corresponde con la cuantía de mayor valor, por aplicación de la regla 2ª del art. 252 de la LEC.

SUPLICO AL TRIBUNAL: Tenga por efectuada la anterior manifestación a todos los efectos legales que procedan.

OTROSÍ SEGUNDO DIGO: Que al amparo del apartado 3 del art. 155 de la LEC designo como domicilio del demandado, a efectos de actos de comunicación, el de la vivienda arrendada sita en la calle [CALLE], nº [NÚMERO], de esta Ciudad, al no haberse señalado otro domicilio para actos de comunicación en el contrato, interesando asimismo, al amparo del primer párrafo del apartado tercero del artículo 161 de la LEC y teniendo en cuenta que el domicilio donde se ha de practicar la comunicación es la vivienda arrendada al demandado, si en el momento de practicar la comunicación no se encontrare allí dicho destinatario, se efectúe la entrega a cualquier empleado o familiar mayor de 14 años, que se encuentre en ese lugar, o al conserje de la finca, si lo tuviere, advirtiendo al receptor que está obligado a entregar la copia de la resolución o la cédula al destinatario de ésta o a darle aviso, si sabe su paradero.

SUPLICO AL TRIBUNAL: Tenga por efectuada la anterior manifestación a todos los efectos legales que procedan.

OTROSÍ TERCERO DIGO: Que al amparo del artículo 152.1 de la LEC(o de la disposición adicional quinta de la LEC) intereso que se entregue al Procurador de esta parte las comunicaciones y cédulas que se expidan con el fin de realizar los actos de comunicación a costa de esta parte en los términos que la norma citada dispone que, una vez cumplimentadas, serán aportadas ante el Tribunal al que turno corresponda el conocimiento de esta demanda.

SUPLICO AL TRIBUNAL: Que tenga por hechas las manifestaciones precedentes a todos los efectos legales que procedan y que acuerde de conformidad.

OTROSÍ CUARTO DIGO: Que intereso se haga constar en el requerimiento que el arrendatario no puede enervar el desahucio conforme a lo expuesto en el fundamento quinto de esta demanda.

SUPLICO AL TRIBUNAL: Que tenga por hechas las manifestaciones precedentes a todos los efectos legales que procedan.

OTROSÍ QUINTO DIGO: Que habiendo adquirido mi mandante en la demanda el compromiso de condonar al arrendatario toda la deuda reclamada, incluso las rentas no vencidas hasta el momento mismo del desalojo voluntario de la vivienda, y de las costas, con la condición de que dicho desalojo voluntario que tenga lugar en el plazo no inferior a quince días y no superior a [PLAZO] a contar desde que se le notifique la demanda, al amparo del apartado 3 del art. 437 la LEC, intereso que se requiera al demandado a fin de que manifieste si acepta este compromiso con la indicación de que su aceptación equivaldrá a un allanamiento con los efectos del art. 21 de la LEC, condonación que comprenderá la cuantía señalada en el Fundamento de Derecho sexto de esta demanda.

SUPLICO AL TRIBUNAL: Tenga por efectuadas las anteriores manifestaciones a todos los efectos legales que procedan.

OTROSÍ SEXTO DIGO: Que, de conformidad a lo dispuesto en el artículo 549.3 de la LEC intereso que se proceda a la ejecución directa de la sentencia condenatoria o decreto que ponga fin al desahucio, procediendo al lanzamiento en el día y hora exacta señalados en la propia sentencia o en la fecha que se hubiere fijado al ordenar la realización del requerimiento al demandante.

SUPLICO AL TRIBUNAL tenga por efectuadas las anteriores manifestaciones a todos los efectos legales que procedan y, en consecuencia, acuerde la ejecución directa de la sentencia condenatoria que en su día se dicte, llevándose a efecto el lanzamiento en el día señalado.

OTROSÍ SÉPTIMO: (Caso de personas jurídicas no exentas) Que estando la presente demanda sujeta al abono de la tasa por el ejercicio de la potestad jurisdiccional fijada por la Ley 10/2012, de 20 de noviembre, modificada por Real Decreto Ley 3/2013, de 22 de febrero, y Ley 25/2015, de 28 julio, y por Orden HAP/861/2015, de 7 de mayo, siendo mi representada persona jurídica no exenta, se acompaña a la presente demanda como documento nº [Nº DE DOCUMENTO] la correspondiente autoliquidación con el ejemplar para la Administración de Justicia debidamente validado y en el que consta el pago de la cantidad de 150 euros correspondiente a la cuota fija, sin que se incluya la cuota variable prevista en el artículo 7.2 de la Ley 10/2012 al haber sido declarado inconstitucional y nulo por la STC 140/2016, de 21 de julio.

En virtud de lo anterior,

SUPLICO AL TRIBUNAL que tenga por hecha la anterior manifestación a los efectos pertinentes y por acompañado el documento justificativo del abono de la tasa.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma Abogado Firma Procurador

========================================================================
