---
name: demanda-ejecutiva-deuda-garantizada-hipoteca-maximo-civ-1497
description: "Demanda ejecutiva por deuda garantizada con hipoteca de máximo. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda ejecutiva por deuda garantizada con hipoteca de máximo

> Formulario **CIV-1497** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Demanda ejecutiva para exigir el pago de una deuda con garantía hipotecaria de máximo

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda ejecutiva por deuda garantizada con hipoteca de máximo» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda ejecutiva por deuda garantizada con hipoteca de máximo” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:demanda-ejecutiva-deuda-garantizada-hipoteca-maximo-civ-1497`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (22 veces)
- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] NÚMERO (6 veces)
- [ ] FECHA (5 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] LUGAR (2 veces)
- [ ] NOMBRE DEL REPRESENTADO/A (2 veces)
- [ ] Nº (2 veces)
- [ ] AÑO
- [ ] CALLE
- [ ] FOLIO
- [ ] LIBRO
- [ ] MES
- [ ] Nº DE CLÁUSULA
- [ ] Nº DE DOCUMENTO
- [ ] PARTE DEMANDADA
- [ ] PISO
- [ ] SEDE
- [ ] TOMO
- [ ] ÓRGANO
- [ ] ÓRGANO O PERSONA

## Normas que cita el formulario

- art. 681 LEC
- art. 684.1.1.º LEC
- art. 85.1 LOPJ
- art. 539.1 LEC
- art. 685.2 LEC
- art. 682 LEC
- art. 573 LEC
- art. 129 LH
- art. 153 LH
- art. 153 bis LH
- art. 105 LH
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

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a. de los Tribunales, en nombre y representación de [NOMBRE DEL REPRESENTADO/A], según consta en la escritura de poder general para pleitos que acompaño, ante el Tribunal comparezco y como mejor proceda en derecho DIGO:

Que por medio del presente escrito formulo demanda ejecutiva para exigir el pago de una deuda con garantía hipotecaria de máximo, al amparo de lo dispuesto en los artículos 681 y siguientes de la LEC, contra [PARTE DEMANDADA], con domicilio en [LOCALIDAD], ejercitando la acción hipotecaria en relación con el bien inmueble que se indica a continuación y con fundamento en los siguientes:

HECHOS

PRIMERO.- En fecha [FECHA] mi mandante acordó conceder a D./Dña. [NOMBRE Y APELLIDOS] una póliza de crédito hasta un máximo de [IMPORTE] euros ( [IMPORTE] €), garantizándose el cumplimiento de la obligación de restitución del capital del que efectivamente se disponga y de sus intereses, con la hipoteca sobre la finca n.º [NÚMERO] inscrita en el Registro de la Propiedad n.º [NÚMERO]; y sin perjuicio de la responsabilidad personal del deudor al respecto. Dicho contrato se formalizó en escritura pública otorgada en fecha [FECHA] ante el Notario de esta localidad D./Dña. [NOMBRE Y APELLIDOS], número [NÚMERO] de su protocolo. Se acompaña como documento n.º copia de dicha escritura pública expedida con eficacia ejecutiva.

SEGUNDO.- La línea de crédito garantizada con la hipoteca señalada reunía, básicamente, las siguientes características:

A) Se pactó que D./Dña. [NOMBRE Y APELLIDOS] podía disponer durante el plazo del contrato, concretado en [Nº] meses, desde su fecha hasta el mes de [MES] de [AÑO] (prorrogable por plazos idénticos sin denuncia de ninguna de las partes al respecto), de hasta un máximo de [IMPORTE] euros que debía destinar de manera obligatoria a sufragar los gastos derivados del desarrollo de su actividad como hostelero en la explotación del restaurante [ÓRGANO] sito en [LOCALIDAD]. Con objeto de facilitar el desarrollo del contrato, se aperturó una cuenta corriente auxiliar donde mi mandante debía ingresar las cantidades interesadas por el cliente en la forma prevista, y desde la cual se realizarían las devoluciones correspondientes a las que se obligaba el cliente.
B) Se fijó un periodo de carencia durante el cual no existía obligación de devolver el principal de las cantidades prestadas, abonando trimestralmente el interés pactado del %, en relación a las disposiciones correspondientes. Asimismo, transcurrido el periodo de carencia, se devolvería el capital finalmente utilizado, en cuotas que el deudor se compromete a satisfacer por trimestres vencidos.
C) En el caso de que el deudor incurriese en mora en los pagos, el interés moratorio se liquidaría conforme a la fórmula expresada en el contrato, consistente en interés devengado = I = Principal *23/100/365* días transcurridos.
D) El deudor podía, durante el periodo de carencia, devolver total o parcialmente el capital del que se hubiera dispuesto, con la correspondiente disminución de intereses contractuales.
E) Se tendría por vencido el préstamo y podría exigir el acreedor el inmediato reintegro del capital, cuando el deudor dejara de satisfacer dos mensualidades consecutivas de las cuotas de amortización de la deuda, cualquiera que fuera el carácter de las mismas; correspondiendo a la entidad bancaria la facultad de liquidar el saldo deudor resultante en cada caso.

TERCERO.- D./Dña. [NOMBRE Y APELLIDOS] garantizó la devolución del capital del que finalmente dispusiera, con sus consiguientes intereses, y eventuales costas y gastos, por un total de [IMPORTE] euros ( [IMPORTE] €), que se corresponden a [IMPORTE] euros ( [IMPORTE] €) por el principal, [IMPORTE] euros ( [IMPORTE] €) por intereses remuneratorios y [IMPORTE] euros ( [IMPORTE] €) por costas y gastos. Ello se hizo constituyendo el deudor hipoteca sobre la finca inscrita a su favor que se describe en la estipulación número [NÚMERO] de la escritura y que aquí se detalla:

DESCRIPCIÓN COMPLETA DE LA FINCA

La hipoteca mencionada causó en el Registro de la Propiedad de [LOCALIDAD] la inscripción número [NÚMERO] al Tomo [TOMO], Folio [FOLIO], Libro [LIBRO], Finca número

CUARTO.- Según consta en la cláusula [Nº DE CLÁUSULA] de la escritura de póliza de crédito, ambas partes tasaron de mutuo acuerdo la finca hipotecada en la suma de [IMPORTE] euros ( [IMPORTE] €) para que sirviera de tipo en la subasta, y el deudor señaló como domicilio para la práctica de los requerimientos y las notificaciones, el sito en la localidad de [LOCALIDAD] calle [CALLE] número [NÚMERO], piso [PISO]. Tal domicilio se mantiene vigente, constituye el domicilio familiar del deudor y es el que consta en el Registro a los efectos antes mencionados.

QUINTO.- La demanda se dirige contra el único deudor responsable, dado que en este negocio jurídico no hay hipotecante no deudor ni tercer poseedor.

SEXTO.- El deudor, una vez transcurrido el periodo de carencia, ha dejado transcurrir cuatro plazos contractualmente previstos, por importe cada uno de ellos de [IMPORTE] euros, para hacer pago a mi mandante de las cantidades a que se había comprometido a devolver en función del capital prestado. Se acompaña, como documento n.º requerimiento notarial efectuado en fecha [FECHA], en la que se reclama el pago de las cuotas vencidas calculadas conforme a lo acordado en relación a las cantidades dispuestas. Por ello, mi mandante se ve en la necesidad de promover la presente ejecución en reclamación de la cantidad que se le adeuda por importe de [IMPORTE] euros como principal dispuesto, [IMPORTE] euros por intereses contractuales, y [IMPORTE] euros por intereses moratorios. Todo ello tal y como se detalla en la certificación de saldo y liquidación que se acompaña como documento n.º [Nº], a la que deben incrementarse los intereses que se devenguen desde dicha fecha hasta la del completo pago, al tipo de interés de demora convenido.

A los anteriores hechos les son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

I.- COMPETENCIA.

Conforme al artículo 684.1.1.º de la LEC, en relación con lo dispuesto en el art. 85.1º LOPJ, para conocer de los procedimientos de ejecución sobre bienes hipotecados o pignorados será competente si los bienes fueren inmuebles, el Tribunal de Instancia del lugar en que radique la finca y si ésta radicare en más de un partido judicial, lo mismo que si fueren varias y radicaren en diferentes partidos, el Tribunal de Instancia de cualquiera de ellos, a elección del demandante, sin que sean aplicables en este caso las normas sobre sumisión expresa o tácita contenidas en la LEC.

En el presente caso, la finca hipotecada se encuentra localizada dentro del partido judicial del Tribunal al que me dirijo.

II.- POSTULACIÓN.

Es preceptiva la intervención de abogado y procurador en este procedimiento, tal y como prescribe el artículo 539.1 de la LEC.

III.- TÍTULO DE EJECUCIÓN.

El artículo 685.2 de la LEC dispone que a la demanda se acompañará el título o títulos de crédito, revestidos de los requisitos que esta Ley exige para el despacho de la ejecución. Por lo tanto, de acuerdo con el artículo 517.2.4.º de la Ley Procesal, en relación con lo dispuesto en el artículo 17.1 párrafo 4.º de la Ley del Notariado, que dice que a los efectos del mismo se considerará título ejecutivo aquella copia que el interesado solicite que se expida con tal carácter. De esta forma, se acompaña copia de la escritura de la póliza de crédito, expedida con las características legalmente previstas en el artículo 233 del Reglamento Notarial.

IV.- REQUISITOS FORMALES.

La escritura de constitución de la hipoteca determinará el precio en que los interesados tasan la finca o bien hipotecado, para que sirva de tipo en la subasta, debiendo constar en la misma escritura un domicilio, que fijará el deudor, para la práctica de los requerimientos y de las notificaciones (artículo 682 LEC).

Asimismo, además de acompañar a la demanda el título de crédito, se aportan los demás documentos a que se refieren el artículo 550 (poder) y la certificación del saldo deudor, los artículos 573 y 574 de la LEC (liquidación de la deuda).

V.- REQUISITOS DE ADMISIBILIDAD DE LA DEMANDA

Dando cumplimiento a la exigencia contenida en el art. 685.2 LEC se indica que el inmueble objeto de la misma, según consta a esta parte, no constituye la vivienda habitual del deudor, así como que concurre en la parte ejecutante la condición de gran tenedora de vivienda de acuerdo con la definición contenida en la Ley 12/2023, de 24 de mayo, por el derecho a la vivienda.

Asimismo, se indica que el deudor no se encuentra en situación de vulnerabilidad económica, como se justifica con el documento expedido por [ÓRGANO O PERSONA] que se acompaña como documento nº [Nº DE DOCUMENTO]

VI.- ASPECTOS SUSTANTIVOS.

1.- Por mi mandante se procede a plantear esta ejecución judicial directa frente al inmueble hipotecado, con objeto de reclamar las cantidades que se le adeudan, a partir de la posibilidad habilitada por el art. 129 LH. La especialidad deriva de la concreta garantía real en su momento otorgada, concretada en una hipoteca de máximo dirigida a proteger la devolución del capital, e intereses correspondientes, en el marco de la póliza de crédito concertada entre las partes. En la misma, se podía disponer de hasta un máximo de [IMPORTE] euros, fijando el valor máximo garantizado en función de los intereses contractuales y posibles intereses de demora que pudieran generarse, a partir de la finalización del periodo de carencia. Extremos, todos ellos, recogidos en la escritura pública reseñada

La figura de la hipoteca de máximo o seguridad, está especialmente prevista para garantizar concretas obligaciones cuyos elementos no se encuentran registralmente determinados de forma íntegra, y en las que no aparece fijado el importe exacto de la obligación asegurada, sino sólo el máximo a que puede ascender la responsabilidad hipotecaria (que puede comprender el capital prestado, los intereses ordinarios, los intereses de demora, costas judiciales, y eventuales gastos). Y, de esta manera, las hipotecas de máximo suelen estar asociadas a las líneas de crédito a largo plazo, como aquí acontece, con una específica necesidad de garantía, atendiendo a la indeterminación inicial de la cantidad de la que finalmente se disponga en cada caso.

De esta forma, la presente hipoteca de máximo se contrae a los requisitos exigidos en el art. 153 LH, pudiéndose observar en la escritura pública acompañada la cantidad máxima de la que respondía la finca, el plazo de carencia, y los plazos de devolución. Asimismo, conforme a la liquidación acompañada, el saldo final reclamado se concreta en un total de [IMPORTE] euros, cantidad inferior al máximo posible, sin perjuicio de los intereses de demora que se sigan generando desde la fecha de dicha liquidación. El mismo se ha calculado según lo expresamente pactado, y ha sido notificado notarialmente a D./Dña. [NOMBRE Y APELLIDOS]

2.- Asimismo, mi mandante es una entidad de crédito que puede otorgar préstamos y créditos como el que nos ocupa, conforme al art. 2 RD 716/2009, con relación al art. 153 bis LH.

3.- La hipoteca de máximo, como cualquier otra hipoteca, sujeta directa e inmediatamente los bienes sobre los que se impone, cualquiera que sea su poseedor, al cumplimiento de la obligación para cuya seguridad fue constituida. La forma, extensión y efectos de la hipoteca, así como lo relativo a su constitución, modificación y extinción y a lo demás pertinente, queda sometido a las prescripciones de la Ley Hipotecaria (artículos 1.876 y 1.880 del Código Civil); con las especialidades mencionadas para este supuesto.

4.- En cuanto a la escritura pública de línea de crédito y la liquidación acompañada, se señalan los artículos 1.740, 1.753, 1.755, 1.857, 1.859, 1.861 y demás concordantes del Código Civil, con arreglo a los cuales queda plenamente justificada la certeza y subsistencia del crédito que se reclama y de sus intereses, que el mismo ya es líquido, vencido y exigible con arreglo a derecho y que la entidad que represento es su titular actual.

Por último, el artículo 105 LH dispone que la hipoteca podrá constituirse en garantía de toda clase de obligaciones y no alterará la responsabilidad personal ilimitada del deudor que establece el artículo 1.911 del Código Civil.

VII.- SOBRE EJECUCIÓN DE BIENES HIPOTECADOS.

Los artículos 681.1 de la LEC y 129 LH prescriben que la acción para exigir el pago de deudas garantizadas por prenda o hipoteca podrá ejercitarse directamente contra los bienes pignorados o hipotecados, sujetando su ejercicio a lo dispuesto para la ejecución dineraria, con las especialidades que se establecen en los artículos 681 a 698.

En virtud de todo lo anterior se

SOLICITA

que se tenga por presentado este escrito junto con los documentos que se acompañan y, admitiéndolos, se me tenga por comparecido y parte en nombre y representación de [NOMBRE DEL REPRESENTADO/A], entendiéndose conmigo las sucesivas diligencias, y por promovido procedimiento de ejecución hipotecaria contra D./Dña. [NOMBRE Y APELLIDOS], respecto de la finca descrita en el hecho tercero de esta demanda, a fin de que, tras los trámites pertinentes, con el producto que se obtenga con su realización, se haga pago a mi poderdante de la cantidad de [IMPORTE] euros por el principal dispuesto, [IMPORTE] euros por intereses contractuales, y [IMPORTE] euros por intereses moratorios, que deberán incluir los que se devenguen desde la liquidación hasta la del completo pago, así como las costas de este procedimiento que deberán ser sufragadas por el demandado.

Es de Justicia que pido en [LUGAR], a [FECHA].

PRIMER OTROSÍ DIGO: De acuerdo con el artículo 688.1 de la LEC,

SE SOLICITA que se reclame del Registrador de la Propiedad de [LOCALIDAD] certificación en la que consten la titularidad del dominio y demás derechos reales del bien hipotecado, así como los derechos de cualquier naturaleza que existan sobre dicho bien, en especial relación completa de las cargas inscritas que lo graven o, en su caso, que se halla libre de cargas y que exprese, asimismo, que la hipoteca a favor del ejecutante se halla subsistente y sin cancelar o, en su caso, la cancelación o modificaciones que aparecieren en el Registro.

SEGUNDO OTROSÍ DIGO: Al haberse incumplido el pago de las cuatro cuotas de devolución e intereses correspondientes, de conformidad con lo dispuesto en el artículo 693.3 de la LEC,

SE SOLICITA que se comunique al deudor que, hasta el día señalado para la celebración de la subasta, podrá liberar el bien mediante la consignación de la cantidad exacta que por principal e intereses estuviere vencida en la fecha de presentación de esta demanda.

Igual Justicia y fecha.

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a

========================================================================
