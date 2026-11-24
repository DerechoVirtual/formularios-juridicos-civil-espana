---
name: demanda-ejecutiva-contra-herederos-beneficiario-civ-1514
description: "Demanda ejecutiva contra los herederos del beneficiario de una hipoteca inversa. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda ejecutiva contra los herederos del beneficiario de una hipoteca inversa

> Formulario **CIV-1514** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Demanda ejecutiva de préstamo garantizado con hipoteca inversa interpuesta por entidad de crédito contra herederos del beneficiario

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda ejecutiva contra los herederos del beneficiario de una hipoteca inversa» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda ejecutiva contra los herederos del beneficiario de una hipoteca inversa” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:demanda-ejecutiva-contra-herederos-beneficiario-civ-1514`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (19 veces)
- [ ] NOMBRE Y APELLIDOS (17 veces)
- [ ] Nº DE DOCUMENTO (8 veces)
- [ ] LOCALIDAD (7 veces)
- [ ] FECHA (6 veces)
- [ ] NÚMERO (5 veces)
- [ ] Nº (3 veces)
- [ ] NOMBRE DEL REPRESENTADO/A (2 veces)
- [ ] AÑO
- [ ] DENOMINACIÓN SOCIAL
- [ ] DÍA
- [ ] FOLIO
- [ ] LIBRO
- [ ] LUGAR
- [ ] MES
- [ ] Nº DE PLAZOS
- [ ] PARTE DEMANDADA
- [ ] SEDE
- [ ] TOMO
- [ ] ÓRGANO O PERSONA

## Normas que cita el formulario

- art. 681 LEC
- art. 85.1 LOPJ
- art. 539.1 LEC
- art. 685.2 LEC
- art. 682 LEC
- art. 573 LEC
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

Procurador de los Tribunales, en nombre y representación de [NOMBRE DEL REPRESENTADO/A], según consta en la escritura de poder inscrito en el Registro Electrónico de Apoderamientos Judiciales, a cuya justificación aporto certificación de dicho Registro como documento nº [Nº DE DOCUMENTO], ante el Tribunal comparezco y como mejor proceda en derecho DIGO:

Que por medio del presente escrito formulo demanda ejecutiva para exigir el pago de una deuda con garantía hipotecaria, al amparo de lo dispuesto en los artículos 681 y siguientes de la LEC, contra D./Dña. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], contra D./Dña. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], y contra D./Dña. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], como herederos de D./Dña. [NOMBRE Y APELLIDOS], fallecido en fecha [FECHA], ejercitando la acción hipotecaria en relación con la finca que luego se dirá y con fundamento en los siguientes

HECHOS

PRIMERO.- Mi mandante es una entidad de crédito debidamente autorizada para operar en España, que acordó conceder en fecha [FECHA] a D./Dña. [NOMBRE Y APELLIDOS], quien contaba con la edad de años en dicha fecha, una renta vitalicia por importe de [IMPORTE] euros mensuales con un máximo de [IMPORTE] euros, garantizada, además de con la responsabilidad personal, con una hipoteca inversa sobre la vivienda propiedad de este último, sita en [LOCALIDAD] e inscrita en el en el Registro de la Propiedad nº [NÚMERO] de [LOCALIDAD], al Tomo [TOMO], Libro [LIBRO], Folio [FOLIO], Finca nº [NÚMERO]; y destinada a su residencia particular. D./Dña. [NOMBRE Y APELLIDOS] fue previamente asesorado por la entidad [DENOMINACIÓN SOCIAL] de su situación financiera y los riesgos económicos derivados de la suscripción de este producto.

Todo ello, se formalizó en escritura pública ante el Notario de esta localidad D./Dña. [NOMBRE Y APELLIDOS], número [NÚMERO] de su protocolo. Se acompaña como documento número [Nº DE DOCUMENTO] copia de la escritura pública mencionada expedida con eficacia ejecutiva.

SEGUNDO.- En dicha escritura se hizo constar:

1.- Que D./Dña. [NOMBRE Y APELLIDOS] tenía entonces la edad de [Nº] años.
2.- Que D./Dña. [NOMBRE Y APELLIDOS] dispondría, con carácter vitalicio de una renta mensual de [IMPORTE] euros.
3.- Que la deuda sólo sería exigible por el acreedor y la garantía ejecutable, cuando falleciera el prestatario.
4.- Que la vivienda hipotecada había sido tasada en [IMPORTE] euros, tal y como se aprecia en la tasación, acompañada como documento nº [Nº DE DOCUMENTO], efectuada por el agente de la propiedad inmobiliaria D./Dña. [NOMBRE Y APELLIDOS] integrante de los servicios de tasación de mi mandante, y aceptada de común acuerdo por las partes. Se pactó que la misma serviría de tipo en la subasta y el deudor señala como domicilio para la práctica de los requerimientos y las notificaciones, los de sus herederos en la forma antes consignada.
5.- Asimismo, la vivienda se aseguró contra daños por el valor de tasación, siendo la aseguradora mi mandante. Se aporta el contrato de seguro firmado como documento nº [Nº DE DOCUMENTO].

TERCERO.- La parte prestataria garantizó la devolución del máximo del capital prestado, intereses, costas y gastos por un total de [IMPORTE] euros ( [IMPORTE] €), que corresponden [IMPORTE] euros ( [IMPORTE] €) por el principal, [IMPORTE] euros ( [IMPORTE] €) por intereses remuneratorios y [IMPORTE] euros ( [IMPORTE] €) por costas y gastos, constituyendo el deudor hipoteca sobre la finca descrita.

CUARTO.- D./Dña. [NOMBRE Y APELLIDOS] falleció en fecha [Nº], [Nº] años después de constituir la hipoteca inversa, tal y como se desprende del certificado de defunción que aporto como documento nº [Nº DE DOCUMENTO]. Hasta la fecha se le han abonado un total de [IMPORTE] euros, computándose [IMPORTE] euros ( [IMPORTE] €) por intereses remuneratorios de nueve años. Se acompaña el cálculo convenientemente desglosado en documento nº [Nº DE DOCUMENTO].

QUINTO.- La demanda se dirige contra los herederos de D./Dña. [NOMBRE Y APELLIDOS], tal y como se desprende del testamento autorizado por la Notaria de [LOCALIDAD], D./Dña. [NOMBRE Y APELLIDOS], de fecha [FECHA], n.º [NÚMERO] de su protocolo general corriente, en el cual aquel instituyó herederos a partes iguales a D./Dña. [NOMBRE Y APELLIDOS], D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS]. Se aporta copia autorizada del testamento como documento nº [Nº DE DOCUMENTO].

SEXTO.- Los citados herederos han dejado transcurrir el plazo de un mes, previsto en el contrato para cancelar el préstamo, haciendo pago a la entidad acreedora de las cantidades correspondientes a la suma abonada en el tiempo con sus intereses pactados, tras haberse operado el oportuno requerimiento mediante correo certificado a los tres herederos, notificado en fechas, y [FECHA]. Se acompaña en el bloque documental nº [NÚMERO] notificación y acuses de recibo a todos ellos.

Razón por la cual mi representada se ve en la necesidad de promover la presente ejecución en reclamación de la cantidad que se le adeuda y que, según resulta de la certificación que se acompaña como documento nº [Nº DE DOCUMENTO], ascendía a fecha [FECHA] a la cantidad de [IMPORTE] euros ( [IMPORTE] €), suma a la que deben incrementarse los intereses que se devenguen desde dicha fecha hasta la del completo pago, al tipo de interés de demora convenido.

A los anteriores hechos les son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

I.- COMPETENCIA.

Conforme al artículo 684.1.1.º, en relación con lo dispuesto en el art. 85.1º LOPJ, para conocer de los procedimientos de ejecución sobre bienes hipotecados o pignorados será competente si los bienes fueren inmuebles, el Tribunal de Instancia del lugar en que radique la finca y si ésta radicare en más de un partido judicial, lo mismo que si fueren varias y radicaren en diferentes partidos, el Tribunal de Instancia de cualquiera de ellos, a elección del demandante, sin que sean aplicables en este caso las normas sobre sumisión expresa o tácita contenidas en la presente Ley.

En el presente caso, la finca hipotecada se encuentra localizada dentro del partido judicial del Tribunal al que me dirijo.

II.- POSTULACIÓN.

Es preceptiva la intervención de abogado y procurador en este procedimiento, tal y como prescribe el artículo 539.1 de la LEC.

III.- TÍTULO DE EJECUCIÓN.

El artículo 685.2 de la LEC dispone que a la demanda se acompañará el título o títulos de crédito, revestidos de los requisitos que esta Ley exige para el despacho de la ejecución. Por lo tanto, de acuerdo con el artículo 517.2.4.º de la Ley Procesal, en relación con lo dispuesto en el artículo 17.1 párrafo 4.º de la Ley del Notariado, que dice que a los efectos del mismo se considerará título ejecutivo aquella copia que el interesado solicite que se expida con tal carácter, se ha acompañado copia de la escritura de préstamo hipotecario expedida con las características indicadas en el artículo 233 del Reglamento Notarial, en cumplimiento de lo legalmente establecido.

IV.- REQUISITOS FORMALES.

La escritura de constitución de la hipoteca determinará el precio en que los interesados tasan la finca o bien hipotecado, para que sirva de tipo en la subasta, debiendo constar en la misma escritura un domicilio, que fijará el deudor, para la práctica de los requerimientos y de las notificaciones (artículo 682 LEC).

Además, aparte de acompañar a la demanda el título de crédito, se aportan los demás documentos a que se refieren el artículo 550 (poder) y, en sus respectivos casos, los artículos 573 y 574 de la LEC (liquidación de la deuda).

V.- REQUISITOS DE ADMISIBILIDAD DE LA DEMANDA

Dando cumplimiento a la exigencia contenida en el art. 685.2 LEC se indica que el inmueble objeto de la misma, según consta a esta parte, no constituye la vivienda habitual del deudor, así como que concurre en la parte ejecutante la condición de gran tenedora de vivienda de acuerdo con la definición contenida en la Ley 12/2023, de 24 de mayo, por el derecho a la vivienda.

Asimismo, se indica que el deudor no se encuentra en situación de vulnerabilidad económica, como se justifica con el documento expedido por [ÓRGANO O PERSONA] que se acompaña como documento nº ……

VI.- ASPECTOS SUSTANTIVOS.

La hipoteca sujeta directa e inmediatamente los bienes sobre los que se impone, cualquiera que sea su poseedor, al cumplimiento de la obligación para cuya seguridad fue constituida. La forma, extensión y efectos de la hipoteca, así como lo relativo a su constitución, modificación y extinción y a lo demás pertinente, queda sometido a las prescripciones de la Ley Hipotecaria (artículos 1.876 y 1.880 del Código Civil).

En cuanto a la escritura pública de préstamo hipotecario se señalan los artículos 1.740, 1.753, 1.755, 1.857, 1.859, 1.861 y demás concordantes del Código Civil, con arreglo a los cuales queda plenamente justificada la certeza y subsistencia del crédito que se reclama y de sus intereses, que el mismo es líquido, vencido y exigible con arreglo a derecho y que la entidad que represento es su titular actual.

Por último, el artículo 105 de la Ley Hipotecaria dispone que la hipoteca podrá constituirse en garantía de toda clase de obligaciones y no alterará la responsabilidad personal ilimitada del deudor que establece el artículo 1.911 del Código Civil.

Asimismo la hipoteca inversa que nos ocupa cumple con los requisitos establecidos en la Disposición Adicional Primera de la Ley 41/2007, de 7 de diciembre, por la que se modifica la Ley 2/1981, de 25 de marzo, de Regulación del Mercado Hipotecario y otras normas del sistema hipotecario y financiero, de regulación de las hipotecas inversas y el seguro de dependencia y por la que se establece determinada norma tributaria. Así:

— Mi mandante es una entidad autorizada para conceder la hipoteca inversa, título de la presente ejecución, de conformidad con lo dispuesto en el artículo 2 RD 716/2009.
— El solicitante era mayor de 65 años en el momento de la concesión y fue asesorado por el correspondiente servicio de asesoramiento independiente de su situación financiera y los riesgos de la operación, trasladados, en este caso, a sus herederos. Todo ello, en los términos establecidos por el Ministro de Economía y Hacienda para garantizar el régimen de transparencia y comercialización exigido.
— El solicitante ha dispuesto periódicamente, sin obstáculo alguno, de las cantidades pactadas hasta su fallecimiento.
— La deuda se exige a sus herederos, como previene la ley, los cuales no han atendido el requerimiento efectuado para el pago y cancelación del préstamo.
— La vivienda, residencia particular de D./Dña. [NOMBRE Y APELLIDOS] fue convenientemente tasada y asegurada contra daños por el valor de tasación, en los términos establecidos en los arts. 8 y 10 RD 716/2009.

VII.- SOBRE EJECUCIÓN DE BIENES HIPOTECADOS.

Los artículos 681.1 de la LEC y 129 de la Ley Hipotecaria prescriben que la acción para exigir el pago de deudas garantizadas por prenda o hipoteca podrá ejercitarse directamente contra los bienes pignorados o hipotecados, sujetando su ejercicio a lo dispuesto para la ejecución dineraria, con las especialidades que se establecen en los artículos 681 a 698.

En virtud de todo lo anterior

SOLICITA

que se tenga por presentado este escrito junto con los documentos que se acompañan y, admitiéndolos, se me tenga por comparecido y parte en nombre y representación de [NOMBRE DEL REPRESENTADO/A], entendiéndose conmigo las sucesivas diligencias, y por promovido procedimiento de ejecución hipotecaria contra [PARTE DEMANDADA], respecto de la finca descrita en el hecho tercero de esta demanda, a fin de que, tras los trámites pertinentes, con el producto que se obtenga con su realización, se haga pago a mi poderdante de la cantidad de [IMPORTE] euros [IMPORTE] €) en concepto de principal e intereses devengados hasta la fecha de la liquidación de la deuda, más los intereses que a los tipos pactados se devenguen computados desde el día [FECHA] hasta que se practique la liquidación definitiva, así como las costas de este procedimiento que deberán ser sufragadas por el demandado.

Es de Justicia que pido en [LUGAR], a [DÍA] de [MES] de [AÑO].

PRIMER OTROSÍ DIGO: De acuerdo con el artículo 688.1 de la LEC

SE SOLICITA que se reclame del Registrador de la Propiedad de [LOCALIDAD] certificación en la que consten la titularidad del dominio y demás derechos reales del bien hipotecado, así como los derechos de cualquier naturaleza que existan sobre dicho bien, en especial relación completa de las cargas inscritas que lo graven o, en su caso, que se halla libre de cargas y que exprese, asimismo, que la hipoteca a favor del ejecutante se halla subsistente y sin cancelar o, en su caso, la cancelación o modificaciones que aparecieren en el Registro.

SEGUNDO OTROSÍ DIGO: Al haberse incumplido el pago de [Nº DE PLAZOS] en que se distribuyó la deuda y, pese a que se convino en el contrato de préstamo hipotecario el vencimiento total y la posibilidad de reclamar la totalidad de lo adeudado por capital y por intereses, de conformidad con lo dispuesto en el artículo 693.3 de la LEC,

SE SOLICITA que se comunique a los deudores que, hasta el día señalado para la celebración de la subasta, podrán liberar el bien mediante la consignación de la cantidad exacta que por principal e intereses estuviere vencida en la fecha de presentación de esta demanda, incrementada, en su caso, con los intereses de demora que se vayan produciendo a lo largo del procedimiento.

Igual Justicia y fecha.

Firma del Abogado/a	Firma del Procurador/a

========================================================================
