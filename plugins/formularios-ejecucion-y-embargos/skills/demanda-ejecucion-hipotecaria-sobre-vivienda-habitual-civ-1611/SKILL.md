---
name: demanda-ejecucion-hipotecaria-sobre-vivienda-habitual-civ-1611
description: "Demanda de ejecución hipotecaria sobre la vivienda habitual del deudor - variante 2. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de ejecución hipotecaria sobre la vivienda habitual del deudor - variante 2

> Formulario **CIV-1611** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Demanda de procedimiento de ejecución hipotecaria sobre la vivienda habitual del deudor, conforme a los artículos 681 y siguientes de la LEC y 129 de la Ley Hipotecaria. Contrato preexistente a la Ley 5/2019, de 15 de marzo, reguladora de los contratos de crédito inmobiliario, vencido con posterioridad al 16 de junio de 2019.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de ejecución hipotecaria sobre la vivienda habitual del deudor - variante 2» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de ejecución hipotecaria sobre la vivienda habitual del deudor - variante 2” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:demanda-ejecucion-hipotecaria-sobre-vivienda-habitual-civ-1611`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (8 veces)
- [ ] IMPORTE EN CIFRA (8 veces)
- [ ] FECHA (7 veces)
- [ ] Nº DE DOCUMENTO (5 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] NÚMERO (4 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] NOMBRE DEL REPRESENTADO/A (2 veces)
- [ ] PARTE DEMANDADA (2 veces)
- [ ] AÑO
- [ ] CALLE
- [ ] FECHAS
- [ ] FOLIO
- [ ] LIBRO
- [ ] LUGAR
- [ ] MES
- [ ] Nº DE CLÁUSULA
- [ ] Nº DE PLAZOS IMPAGADOS
- [ ] Nº DE VENCIMIENTOS PAGADOS
- [ ] PERIODICIDAD
- [ ] PISO
- [ ] PLAZO
- [ ] PORCENTAJE
- [ ] SEDE
- [ ] TIPO DE INTERÉS
- [ ] TOMO
- [ ] ÓRGANO O PERSONA

## Normas que cita el formulario

- art. 681 LEC
- art. 693.2 LEC
- art. 24 Ley 5/2019
- art. 686 LEC
- art. 85.1 LOPJ
- art. 539.1 LEC
- art. 685.2 LEC
- art. 18 RDL 24/2021
- art. 682 LEC
- art. 573 LEC
- art. 129 bis LH
- art. 1.911 Código Civil
- art. 681.1 LEC
- art. 688.1 LEC
- art. 693.3 LEC

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

D./Dña. [NOMBRE Y APELLIDOS] Procurador de los tribunales, en nombre y representación de [NOMBRE DEL REPRESENTADO/A], según consta en la escritura de poder inscrito en el Registro Electrónico de Apoderamientos Judiciales, a cuya justificación aporto certificación de dicho Registro como documento nº [Nº DE DOCUMENTO], ante el Tribunal comparezco y como mejor proceda en derecho DIGO:

Que por medio del presente escrito formulo demanda ejecutiva para exigir el pago de una deuda con garantía hipotecaria, al amparo de lo dispuesto en los artículos 681 y siguientes de la LEC, contra [PARTE DEMANDADA], con domicilio en [LOCALIDAD], ejercitando la acción hipotecaria en relación con la finca que luego se dirá y con fundamento en los siguientes

HECHOS

PRIMERO.- Por la entidad que represento se acordó conceder a D./Dña. [NOMBRE Y APELLIDOS] un préstamo hipotecario por importe de [IMPORTE] euros ([IMPORTE EN CIFRA] €), garantizándose el cumplimiento de la obligación además de con la responsabilidad personal, con la hipoteca sobre la finca de la que es su vivienda habitual que más adelante se describe, solemnizándose dicho préstamo en escritura pública otorgada en fecha [FECHA] ante el Notario de esta localidad D./Dña. [NOMBRE Y APELLIDOS], número [NÚMERO] de su protocolo. Se acompaña como documento número [Nº DE DOCUMENTO] copia de la escritura pública mencionada expedida con eficacia ejecutiva.

SEGUNDO.- Como pactos más importantes del citado contrato de préstamo con garantía hipotecaria, se destacan los siguientes:

A) El capital concedido devengará un interés del [TIPO DE INTERÉS] anual, que el deudor se compromete a satisfacer por trimestres vencidos.
B) En el caso de que el deudor incurriese en mora en los pagos, el interés moratorio se liquidaría al tipo que en ese momento devengue el préstamo incrementado en [PORCENTAJE] enteros.
C) El deudor abonará todos los meses la cantidad establecida en el cuadro de amortizaciones establecido para toda la duración del préstamo y que se compone de cuotas a pagar en [PERIODICIDAD].
D) Se tendrá por vencido el préstamo y podrá exigir el acreedor el inmediato reintegro del capital, cuando el deudor deje de satisfacer mensualidades de las cuotas de amortización de la deuda o un número de cuotas tal que suponga que el deudor ha incumplido su obligación por un plazo equivalente a [PLAZO].

Se indica, a los efectos contemplados en la disposición transitoria primera, apartado 4, de la Ley 5/2019, de 15 de marzo, reguladora de los contratos de crédito inmobiliario, que el régimen de vencimiento anticipado del art. 24 de la citada Ley es más favorable para el deudor.

TERCERO.- La parte prestataria garantizó la devolución del capital prestado, intereses, costas y gastos por un total de [IMPORTE] euros ([IMPORTE EN CIFRA] €), que corresponden [IMPORTE] euros ([IMPORTE EN CIFRA] €) por el principal, [IMPORTE] euros ([IMPORTE EN CIFRA] €) por intereses remuneratorios de años y [IMPORTE] euros ([IMPORTE EN CIFRA] €) por costas y gastos, constituyendo el deudor hipoteca sobre la finca inscrita a su favor que se describe en la estipulación número [NÚMERO] de la escritura y que aquí se detalla:

DESCRIPCIÓN COMPLETA DE LA FINCA

La hipoteca mencionada causó en el Registro de la Propiedad de [LOCALIDAD] la inscripción número [NÚMERO] al Tomo [TOMO], Folio [FOLIO], Libro [LIBRO], Finca número

CUARTO.- Según consta en la cláusula [Nº DE CLÁUSULA] de la escritura de préstamo, ambas partes tasan de mutuo acuerdo la finca hipotecada en la suma de [IMPORTE] euros ([IMPORTE EN CIFRA] €) para que sirva de tipo en la subasta y el deudor señala como domicilio para la práctica de los requerimientos y las notificaciones, el sito en la localidad de [LOCALIDAD] calle [CALLE] número [NÚMERO], piso [PISO] Este domicilio no ha sufrido modificación ni variación alguna, siendo el domicilio familiar del deudor y el que consta en el Registro a los efectos antes mencionados.

QUINTO.- La demanda se dirige contra el único deudor responsable, pues en este negocio jurídico no hay hipotecante no deudor ni tercer poseedor.

SEXTO.- Que si bien el deudor cumplió con el pago de los [Nº DE VENCIMIENTOS PAGADOS] primeros vencimientos de los plazos estipulados, desatendió los [Nº DE PLAZOS IMPAGADOS] siguientes plazos con vencimiento los días [FECHAS], del mes [MES] del año [AÑO], suma de dinero que sigue adeudando a fecha de interposición de la presente demanda.

Mi representada, de conformidad con lo dispuesto en el art. 693.2 de la LEC en relación con el art. 24 y disposición transitoria primera, apartado 4, de la Ley 5 / 2019, de 15 de marzo, reguladora de los contratos de crédito inmobiliario, al hallarse el préstamo en la primera mitad de su duración y haber incurrido el deudor en mora por más de doce plazos mensuales de capital vencidos y no satisfechos, remitió requerimiento notarial al deudor el pasado día [FECHA],concediéndole un plazo de un mes para el cumplimiento y advirtiéndole de que, de no ser atendido, se reclamaría el reembolso total adeudado del préstamo. El requerimiento fue recibido por el deudor el pasado día [FECHA], según acredito por copia notarial auténtica que acompaño, sin que haya satisfecho cantidad alguna hasta la fecha pese a haber transcurrido en exceso el plazo concedido.

Por tanto, de conformidad con los preceptos expresados, con fecha [FECHA], posterior a la entrada en vigor de la citada Ley 5 / 2019, se dio por vencido anticipadamente el préstamo, procediendo a la reclamación del total de lo adeudado según contempla el art. 693.2 LEC en relación con el art. 24 y disposición transitoria primera, apartado 4, de la Ley 5/2019.

Por todo lo anterior, mi representada se ve en la necesidad de promover la presente ejecución en reclamación de la cantidad que se le adeuda y que, según resulta de la certificación que se acompaña como documento número [Nº DE DOCUMENTO], ascendía a fecha [FECHA] a la cantidad de [IMPORTE] euros ([IMPORTE EN CIFRA] €), suma a la que deben incrementarse los intereses que se devenguen desde dicha fecha hasta la del completo pago, al tipo de interés de demora convenido.

Que interesa al derecho de esta parte señalar que se ha practicado el requerimiento de pago al deudor en cumplimiento de lo establecido en el art. 24 de la Ley 5/2019 para el vencimiento anticipado, con concesión de plazo de un mes para el pago de la cantidad pendiente y se han cumplido todas las prescripciones legales para el despacho de ejecución, por lo que se solicita que se dicte auto en que se autorice y despache ejecución, según lo dispuesto en el art. 686 LEC.

A los anteriores hechos les son de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

I.- COMPETENCIA.

Conforme al artículo 684.1.1.º, en relación con lo dispuesto en el art. 85.1º LOPJ, para conocer de los procedimientos de ejecución sobre bienes hipotecados o pignorados será competente si los bienes fueren inmuebles, el Tribunal de Instancia del lugar en que radique la finca y si ésta radicare en más de un partido judicial, lo mismo que si fueren varias y radicaren en diferentes partidos, el Tribunal de Instancia de cualquiera de ellos, a elección del demandante, sin que sean aplicables en este caso las normas sobre sumisión expresa o tácita contenidas en la presente Ley.

En el presente caso, la finca hipotecada se encuentra localizada dentro del partido judicial del Tribunal al que me dirijo.

II.- POSTULACIÓN.

Es preceptiva la intervención de abogado y procurador en este procedimiento, tal y como prescribe el artículo 539.1 de la LEC.

III.- TÍTULO DE EJECUCIÓN.

El artículo 685.2 de la LEC dispone que a la demanda se acompañará el título o títulos de crédito, revestidos de los requisitos que esta Ley exige para el despacho de la ejecución. Por lo tanto, de acuerdo con el artículo 517.2.4.º de la Ley Procesal, en relación con lo dispuesto en el artículo 17.1 párrafo 4.º de la Ley del Notariado, que dice que a los efectos del mismo se considerará título ejecutivo aquella copia que el interesado solicite que se expida con tal carácter, se ha acompañado copia de la escritura de préstamo hipotecario expedida con las características indicadas en el artículo 233 del Reglamento Notarial, en cumplimiento de lo legalmente establecido.

IV.- REQUISITOS FORMALES.

La escritura de constitución de la hipoteca determinará el precio en que los interesados tasan la finca o bien hipotecado, para que sirva de tipo en la subasta, que no podrá ser inferior, en ningún caso, al 75 por cien del valor señalado en la tasación realizada en virtud de lo previsto en el art.18 RDL 24/2021; debiendo constar en la misma escritura un domicilio, que fijará el deudor, para la práctica de los requerimientos y de las notificaciones (artículo 682 LEC).

Además, aparte de acompañar a la demanda el título de crédito, se aportan los demás documentos a que se refieren el artículo 550 (poder) y, en sus respectivos casos, los artículos 573 y 574 de la LEC (liquidación de la deuda).

V.- REQUISITOS DE ADMISIBILIDAD DE LA DEMANDA

Dando cumplimiento a la exigencia contenida en el art. 685.2 LEC se indica que el inmueble objeto de la misma, según consta a esta parte, constituye la vivienda habitual del deudor, así como que no concurre en la parte ejecutante la condición de gran tenedora de vivienda de acuerdo con la definición contenida en la Ley 12/2023, de 24 de mayo, por el derecho a la vivienda, a cuya acreditación se adjuntar a la demanda certificación del Registro de la Propiedad en el que consten la relación de propiedades a nombre de la parte actora (documento nº [Nº DE DOCUMENTO]).

Asimismo, se indica que el deudor no se encuentra en situación de vulnerabilidad económica, como se justifica con el documento expedido por [ÓRGANO O PERSONA] que se acompaña como documento nº [Nº DE DOCUMENTO]

VI.- VENCIMIENTO ANTICIPADO

Es de aplicación lo dispuesto en el art. 693.2 LEC, que establece que podrá reclamarse la totalidad de lo adeudado por capital y por intereses en los términos en los que así se hubiese convenido en la escritura de constitución y consten en el asiento respectivo. Siempre que se trate de un préstamo o crédito concluido por una persona física y que esté garantizado mediante hipoteca sobre vivienda o cuya finalidad sea la adquisición de bienes inmuebles para uso residencial, se estará a lo que prescriben el art. 24 de la Ley 5/2019, reguladora de los contratos de crédito inmobiliario y, en su caso, el art. 129 bis LH, siendo de aplicación a los contratos preexistentes vencidos con posterioridad al 16 de junio de 2019 según establece la disposición transitoria primera, apartado 4, de la citada Ley 5/2019.

VII.- ASPECTOS SUSTANTIVOS.

La hipoteca sujeta directa e inmediatamente los bienes sobre los que se impone, cualquiera que sea su poseedor, al cumplimiento de la obligación para cuya seguridad fue constituida. La forma, extensión y efectos de la hipoteca, así como lo relativo a su constitución, modificación y extinción y a lo demás pertinente, queda sometido a las prescripciones de la Ley Hipotecaria (artículos 1.876 y 1.880 del Código Civil).

En cuanto a la escritura pública de préstamo hipotecario se señalan los artículos 1.740, 1.753, 1.755, 1.857, 1.859, 1.861 y demás concordantes del Código Civil, con arreglo a los cuales queda plenamente justificada la certeza y subsistencia del crédito que se reclama y de sus intereses, que el mismo es líquido, vencido y exigible con arreglo a derecho y que la entidad que represento es su titular actual.

Por último, el artículo 105 de la Ley Hipotecaria dispone que la hipoteca podrá constituirse en garantía de toda clase de obligaciones y no alterará la responsabilidad personal ilimitada del deudor que establece el artículo 1.911 del Código Civil.

VIII- SOBRE EJECUCIÓN DE BIENES HIPOTECADOS.

Los artículos 681.1 de la LEC y 129 de la Ley Hipotecaria prescriben que la acción para exigir el pago de deudas garantizadas por prenda o hipoteca podrá ejercitarse directamente contra los bienes pignorados o hipotecados, sujetando su ejercicio a lo dispuesto para la ejecución dineraria, con las especialidades que se establecen en los artículos 681 a 698.

En virtud de todo lo anterior se

SOLICITA

que se tenga por presentado este escrito junto con los documentos que se acompañan y, admitiéndolos, se me tenga por comparecido y parte en nombre y representación de [NOMBRE DEL REPRESENTADO/A], entendiéndose conmigo las sucesivas diligencias, y por promovido procedimiento de ejecución hipotecaria contra [PARTE DEMANDADA], respecto de la finca descrita en el hecho tercero de esta demanda, a fin de que, tras los trámites pertinentes, con el producto que se obtenga con su realización, se haga pago a mi poderdante de la cantidad de [IMPORTE] euros ([IMPORTE EN CIFRA] €) en concepto de principal e intereses devengados hasta la fecha de la liquidación de la deuda, más los intereses que a los tipos pactados se devenguen computados desde el día [FECHA] hasta que se practique la liquidación definitiva, así como las costas de este procedimiento que deberán ser sufragadas por el demandado.

Es justicia que pido en [LUGAR], a [FECHA].

PRIMER OTROSÍ DIGO: De acuerdo con el artículo 688.1 de la LEC

SE SOLICITA que se reclame del Registrador de la Propiedad de [LOCALIDAD] certificación en la que consten la titularidad del dominio y demás derechos reales del bien hipotecado, así como los derechos de cualquier naturaleza que existan sobre dicho bien, en especial relación completa de las cargas inscritas que lo graven o, en su caso, que se halla libre de cargas y que exprese, asimismo, que la hipoteca a favor del ejecutante se halla subsistente y sin cancelar o, en su caso, la cancelación o modificaciones que aparecieren en el Registro.

SEGUNDO OTROSÍ DIGO: Que siendo el bien hipotecado una vivienda familiar, si bien el deudor puede aun sin el consentimiento del acreedor liberar el bien mediante la consignación de los importes correspondientes a principal e intereses, al amparo de lo dispuesto en el art. 693.3 LEC, interesa al derecho de esta parte se aperciba al deudor que liberado un bien por primera vez, podrá liberarse en segunda o ulteriores ocasiones, siempre que al menos, medien tres años entre la fecha de la liberación y la del requerimiento de pago judicial o extrajudicial efectuada por el acreedor.

SE SOLICITA que tenga por realizada la anterior manifestación a todos los efectos, y previos los trámites con arreglo a derecho acuerde de conformidad con lo interesado.

Igual Justicia y fecha.

Firma del Abogado/a	Firma del Procurador/a

========================================================================
