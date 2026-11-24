---
name: demanda-ejecutiva-basada-aval-bancario-ley-57-1968-civ-1466
description: "Demanda ejecutiva basada en aval bancario de la Ley 57 de 1968 sobre cantidades anticipadas. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda ejecutiva basada en aval bancario de la Ley 57 de 1968 sobre cantidades anticipadas

> Formulario **CIV-1466** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Demanda ejecutiva contra la entidad de crédito avalista, fundada en el aval bancario constituido conforme a la Ley 57/1968 para garantizar la devolución de las cantidades anticipadas por el comprador de una vivienda sobre plano, cuando la promotora no la entrega en plazo.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda ejecutiva basada en aval bancario de la Ley 57 de 1968 sobre cantidades anticipadas» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda ejecutiva basada en aval bancario de la Ley 57 de 1968 sobre cantidades anticipadas” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:demanda-ejecutiva-basada-aval-bancario-ley-57-1968-civ-1466`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (14 veces)
- [ ] Nº (13 veces)
- [ ] FECHA (7 veces)
- [ ] DENOMINACIÓN SOCIAL (5 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] DENOMINACIÓN SOCIAL DE LA PROMOTORA (3 veces)
- [ ] ÓRGANO MUNICIPAL DE URBANISMO (3 veces)
- [ ] FECHA DE ENTREGA (2 veces)
- [ ] NOMBRE DEL NOTARIO (2 veces)
- [ ] Nº DE COLEGIADO (2 veces)
- [ ] Nº DE PROTOCOLO (2 veces)
- [ ] AÑO
- [ ] DESCRIPCIÓN DE LA VIVIENDA SEGÚN EL CONTRATO
- [ ] DNI/NIE
- [ ] DOMICILIO
- [ ] DOMICILIO SOCIAL
- [ ] DÍA
- [ ] FOLIO
- [ ] IMPORTE TOTAL
- [ ] LIBRO
- [ ] LOCALIDAD DEL REGISTRO
- [ ] MES
- [ ] MES Y AÑO
- [ ] NIF
- [ ] NOMBRE Y APELLIDOS DEL EJECUTANTE
- [ ] NOMBRE Y APELLIDOS DEL LETRADO
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] Nº DE CLÁUSULA
- [ ] Nº DE FINCA
- [ ] Nº DE INSCRIPCIÓN
- [ ] SEDE

## Normas que cita el formulario

- art. 3 Ley 57/1968
- art. 6.3 Código Civil

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

### Avisos de actualización (3) — se aplican en el texto, nunca se copian en el documento

- Junto a «…a compra de viviendas, que determinaba anteriormente el art. 3 de la Ley 57/1968»: La Ley 57/1968 quedó derogada el 1-1-2016 (Ley 20/2015, disposición final 3.ª); su régimen está hoy en la disposición adicional 1.ª de la Ley 38/1999, de Ordenación de la Edificación. La Ley 57/1968 sigue aplicándose a las garantías constituidas antes de esa fecha. Fuente: BOE-A-1999-21567, DA 1.ª.
- Junto a «…d al 1 de enero de 2016.] A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «… del título de garantía, resulta evidente la viabilidad de la acción ejercitada.»: el original refería la normativa de protección de consumidores en términos generales; para la nulidad de cláusulas abusivas, la referencia vigente es el texto refundido de la Ley General para la Defensa de los Consumidores y Usuarios (RDLeg 1/2007).

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

[ATENCIÓN: la Ley 57/1968, de 27 de julio, sobre percepción de cantidades anticipadas en la construcción y venta de viviendas, fue derogada a partir del 1 de enero de 2016 por la disposición derogatoria tercera de la Ley 38/1999, de Ordenación de la Edificación, introducida por la Ley 20/2015, de 14 de julio, de ordenación, supervisión y solvencia de las entidades aseguradoras y reaseguradoras, que no establece ya el carácter ejecutivo del aval o de la póliza de seguro de caución en la compra de viviendas, que determinaba anteriormente el art. 3 de la Ley 57/1968 . Por ello, este formulario solo es válido para las cantidades entregadas con anterioridad al 1 de enero de 2016.]

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dª [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, colegiado/a n.º [Nº DE COLEGIADO], actuando en nombre y representación de D./Dª [NOMBRE Y APELLIDOS DEL EJECUTANTE], con domicilio en [DOMICILIO] y DNI/NIE n.º [DNI/NIE], según acredito con la escritura de poder general para pleitos que acompaño, bajo la dirección letrada de D./Dª [NOMBRE Y APELLIDOS DEL LETRADO], colegiado/a n.º [Nº DE COLEGIADO], ante el Tribunal comparezco y, como mejor proceda en derecho,

DIGO:

Que en la representación que ostento formulo DEMANDA EJECUTIVA BASADA EN TÍTULO NO JUDICIAL contra la entidad [ELEGIR: BANCO / CAJA DE AHORROS] [DENOMINACIÓN SOCIAL], con domicilio social en [DOMICILIO SOCIAL] y CIF n.º [NIF], en reclamación de la cantidad de [IMPORTE] euros en concepto de principal, [IMPORTE] euros en concepto de intereses moratorios vencidos, más otros [IMPORTE] euros presupuestados provisionalmente para hacer frente a los intereses que puedan devengarse durante la ejecución y a las costas de ésta, demanda que formulo con base en los siguientes

HECHOS

PRIMERO.- Mi mandante y la mercantil [DENOMINACIÓN SOCIAL DE LA PROMOTORA] suscribieron, en documento privado de fecha [FECHA], la compraventa de nueva vivienda, cuya descripción se transcribe a continuación:

«[DESCRIPCIÓN DE LA VIVIENDA SEGÚN EL CONTRATO]»

En el citado contrato se fijó como fecha de entrega de la vivienda [FECHA DE ENTREGA], y quedó fijado en la cláusula n.º [Nº DE CLÁUSULA] que el precio de la compraventa era de [IMPORTE] euros, el cual se aplazaba mediante abonos mensuales de [IMPORTE] euros, después de un inicial pago alzado de otros [IMPORTE] euros.

También se recoge la forma de pago y se relacionan los recibos para su presentación al cobro en la entidad bancaria demandada [DENOMINACIÓN SOCIAL], en los que se documentó el precio aplazado.

Se acompaña el contrato como DOCUMENTO N.º [Nº].

SEGUNDO.- En dicho acto, mi representado/a abonó a la vendedora la cantidad de [IMPORTE] euros (estipulación n.º [Nº]), más el IVA correspondiente.

Posteriormente, ha abonado un total de [IMPORTE] euros más IVA, a razón de [IMPORTE] euros más IVA al mes, durante [Nº] meses, en el periodo que va desde [FECHA] hasta [FECHA]. Todo ello hace un total de [IMPORTE TOTAL] euros.

En orden a la concreción cuantitativa de los intereses, se adjunta como DOCUMENTO N.º [Nº] el bloque de los recibos bancarios que acreditan el pago de la cantidad inicial y de las [Nº] mensualidades posteriores referidas.

TERCERO.- A solicitud de la Promotora, la entidad bancaria demandada [DENOMINACIÓN SOCIAL] constituyó en fecha [FECHA] un aval bancario por las cantidades que se irían entregando a cuenta de la vivienda en la forma referida, con objeto de garantizar el cumplimiento de la obligación de entrega del contrato y la devolución de las cantidades entregadas por mi mandante a cuenta del precio, conforme a la Ley 57/1968, según lo previsto en la estipulación n.º [Nº] del contrato.

Una vez formalizada la garantía y constituida la demandada como avalista, la Promotora hizo entrega del aval a mi poderdante, como beneficiario/a.

Se adjunta como DOCUMENTO N.º [Nº] el referido contrato de aval.

CUARTO.- Llegada la fecha pactada en el contrato privado para la entrega de la vivienda construida y el correspondiente otorgamiento de escritura pública, la promotora [DENOMINACIÓN SOCIAL DE LA PROMOTORA] informó verbalmente que, por diversos problemas sufridos por la misma, las obras sufrían un retraso de [Nº] meses y no estarían listas para la entrega hasta el mes de [MES Y AÑO].

Puesto en contacto mi mandante con personal de la constructora, se le informa de que no se ha solicitado todavía la licencia de primera ocupación, cuya concesión requiere un procedimiento que puede durar según las circunstancias de cada administración municipal concedente. Asimismo, personados en el lugar de la construcción, se observa, a primera vista, que el estado actual de las obras hace muy difícil que las mismas se terminen en el plazo referido.

Ante tal situación, mi mandante comunicó verbalmente a la Promotora que optaba por la resolución del contrato con devolución de las cantidades entregadas, dándole plazo para que procediera a dicha devolución más los intereses correspondientes.

QUINTO.- Con fecha [FECHA], vencido el plazo, después de agotados los intentos de solución pacífica del asunto y consolidada la certeza de que la promotora no iba a poder terminar la vivienda en un plazo razonable, se practicó requerimiento notarial ante D./Dª [NOMBRE DEL NOTARIO], que lleva n.º [Nº DE PROTOCOLO] de su protocolo general corriente, al cual aquella no respondió, en el que se exigía la devolución de las cantidades entregadas, por resolución debida al incumplimiento radical de la entrega.

Con posterioridad, en fecha [FECHA], se practicó requerimiento notarial ante D./Dª [NOMBRE DEL NOTARIO], que lleva n.º [Nº DE PROTOCOLO] de su protocolo general corriente, frente a la entidad avalista [DENOMINACIÓN SOCIAL], para el pago de las cantidades entregadas a cuenta, donde se hacía constar el incumplimiento de la Promotora y la obligación asumida por el avalista al constituirse la garantía.

Por la misma se contestó negando la exigibilidad del aval, por haber caducado, careciendo éste de fuerza ejecutiva.

Se acompañan las actas públicas de requerimiento como DOCUMENTOS N.º [Nº] y [Nº], así como la contestación escrita del banco como DOCUMENTO N.º [Nº].

SEXTO.- A día de hoy, la entidad garante sigue sin atender la solicitud de pago, a pesar de la no terminación de las obras y, consecuentemente, de que la vivienda adquirida por nuestro mandante no se entregó en plazo, como queda acreditado con el informe de [ÓRGANO MUNICIPAL DE URBANISMO] de [LOCALIDAD], que se aporta como DOCUMENTO N.º [Nº], donde consta que, a fecha [FECHA], aún no se le había concedido a la Promotora la licencia de primera ocupación, imprescindible para que tuviera lugar la entrega y recepción de la vivienda en el plazo previsto, y es preciso impetrar el auxilio judicial, lo que, efectivamente, se hace por medio del presente escrito.

SÉPTIMO.- Mi mandante tiene conocimiento de que la entidad ejecutada es titular del siguiente bien susceptible de embargo, que se considera suficiente para el fin de la ejecución:

- Finca n.º [Nº DE FINCA], inscrita en el Registro de la Propiedad n.º [Nº] de [LOCALIDAD], en el libro [LIBRO], folio [FOLIO], inscripción [Nº DE INSCRIPCIÓN].

A los anteriores hechos resultan de aplicación los siguientes

FUNDAMENTOS DE DERECHO

I.- COMPETENCIA.

Por remisión expresa de lo dispuesto en el art. 545.3 de la Ley de Enjuiciamiento Civil, conforme al art. 51.1 de dicha Ley, que contempla el fuero general de las personas jurídicas y señala como tal el de su domicilio, será competente para la ejecución la Sección Civil del Tribunal de Instancia al que nos dirigimos, por corresponder la acción ejercitada con el domicilio de la persona jurídica demandada.

II.- LEGITIMACIÓN.

Las partes en este concreto proceso de ejecución, ejecutante y ejecutado, quedan determinadas mediante legitimación ordinaria, con arreglo al art. 538 de la Ley de Enjuiciamiento Civil, siendo que la entidad demandada garantiza una obligación pecuniaria, esto es, la restitución de las cantidades anticipadas que se reclaman, en virtud de la constitución de aval del que es beneficiario mi mandante, por lo que ostentan legitimación pasiva y activa, respectivamente.

III.- POSTULACIÓN.

Conforme a lo dispuesto en el art. 539.1 de la Ley de Enjuiciamiento Civil, la demanda viene firmada por abogado y Procurador/a, ya que es preceptiva la intervención de dichos profesionales.

IV.- TÍTULO.

El art. 517.1 de la Ley de Enjuiciamiento Civil dispone que la acción ejecutiva deberá fundarse en un título que tenga aparejada ejecución, encontrándose entre éstos los «documentos que, por disposición de esta u otra ley, lleven aparejada ejecución» (ordinal 9.º). Tal es la ejecutividad del título en cuestión, aval solidario constituido por una promotora con la entidad financiera ejecutada para garantizar la devolución de las sumas entregadas por el ejecutante, que viene expresamente reconocida en el párrafo segundo del art. 3 de la Ley 57/1968, de 27 de julio, reguladora de las percepciones de cantidades anticipadas en la construcción y venta de viviendas.

V.- REQUISITOS FORMALES.

La presente demanda contiene todos los requisitos enumerados en el art. 549 de la Ley de Enjuiciamiento Civil, ya que se ha indicado cuál es el título en que se funda, la tutela ejecutiva que se pretende y la entidad frente a la que se interesa el despacho de la ejecución, así como los bienes del ejecutado susceptibles de embargo conocidos por mi poderdante. Por último, se acompaña a la demanda ejecutiva la documentación necesaria de la contemplada en el art. 550 del mismo texto legal. Así, se adjunta a la demanda ejecutiva el aval bancario de la ley especial, que, acompañado del documento fehaciente que demuestra el incumplimiento por el promotor de su obligación de entrega, consistente en el informe de [ÓRGANO MUNICIPAL DE URBANISMO] de [LOCALIDAD], integra el título susceptible de ser ejecutado.

VI.- ACCIÓN EJERCITADA.

La acción ejercitada es la prevista en el art. 517.2.9.º de la Ley de Enjuiciamiento Civil, en base al aval bancario, regulada específicamente y de forma imperativa en la Ley 57/1968, de 27 de julio, sobre percepción de cantidades anticipadas en la construcción y venta de viviendas, siendo el objeto de la garantía la devolución de las cantidades entregadas a cuenta por los compradores.

Como se pone de manifiesto en la sentencia de la Audiencia Provincial de Ávila de 10 de diciembre de 2002 (rec. 1367/2002), cuando el Legislador promulga, por las razones que recoge su exposición de motivos, la Ley 57/1968 (modificada por la disposición adicional primera de la Ley 38/1999, de 5 de noviembre, de Ordenación de la Edificación, que mantiene el carácter específico de la Ley de 1968 respecto de la adquisición de toda clase de viviendas), acude a la figura del aval bancario, como alternativa del seguro, para garantizar al comprador la devolución de las cantidades entregadas a cuenta en el contrato de adquisición de vivienda.

La norma legal, teniendo en cuenta que esas cantidades a cuenta se han de depositar en una cuenta especial abierta a tal fin en entidad bancaria o en una caja de ahorros, restringe la posibilidad de prestar el aval a esas entidades. El art. 1.1.ª, además, señala el carácter solidario del aval y la finalidad de su constitución: «para el caso de que la construcción no se inicie o no llegue a buen fin, por cualquier causa, en el plazo convenido».

Como quiera que los derechos del beneficiario son irrenunciables (art. 7), no pueden las partes modificar en sentido restrictivo el ámbito de ese afianzamiento, sin perjuicio de que su autonomía contractual les permita extenderlo a otros hipotéticos supuestos, y, en todo caso, en la interpretación de los términos del aval se habrá de obrar siempre «pro beneficiario», dado el carácter tuitivo de la norma.

Al tratarse de un aval bancario constituido con la finalidad señalada en la Ley, le es de aplicación el art. 1.1.ª de la norma en cuanto al concreto supuesto en que puede ejecutarse el aval, en su caso la posibilidad de que constituya título ejecutivo acompañado de documento fehaciente de la no entrega de la vivienda, y en cuanto a la posibilidad que tienen los beneficiarios, si la vivienda no se ha terminado en el plazo fijado en el contrato en condiciones de proceder a su entrega, de optar por la rescisión del contrato con devolución de las cantidades entregadas más el incremento legalmente establecido.

Son, pues, presupuestos de la eficacia del aval:

1.º Que las obras no hayan llegado a buen fin en el plazo convenido.

2.º Que los compradores comuniquen esta circunstancia al vendedor acogiéndose a la posibilidad de devolución indicada en la Ley.

3.º Que quien entregó las cantidades a cuenta no haya concedido prórroga al promotor para terminar las obras.

En este caso ha de entenderse por «llegar a buen fin» (expresión que recoge el aval) lo equivalente al cumplimiento del contrato, en este caso la obligación principal de [DENOMINACIÓN SOCIAL DE LA PROMOTORA] de poner a disposición del comprador el inmueble en la fecha establecida de [FECHA DE ENTREGA]. Obligación de hacer que se fija en el contrato firmado por avalado y beneficiario con un límite temporal que aparece ampliamente rebasado cuando se comunica la intención de resolver el contrato y se requiere la devolución de las cantidades entregadas, por lo que se cumple el primero de los citados presupuestos y también aparece acreditado que el comprador se dirigió a la vendedora haciéndole saber su voluntad de resolver el contrato.

En este sentido, la sentencia del Tribunal Supremo de 9 de abril de 2003, rec. 2631/1997, señala que «El artículo primero de la Ley 57/1968, de 27 de julio, lo que trata es de garantizar al comprador de vivienda futura la devolución de las cantidades que anticipó, tanto si la construcción no se hubiera iniciado, como cuando no llega a buen fin por cualquier causa, que es el supuesto de autos. La garantía cabe prestarla por medio de contrato de seguro o por medio de aval, que se establece como solidario, a cargo de entidad bancaria y para que resulte operativa es preciso que se den los supuestos fácticos que se dejan reseñados, en cuyo caso el comprador está facultado, por la opción que la ley le concede, para rescindir el contrato con devolución de las cantidades entregadas a cuenta, incrementadas con el 6 % de interés anual (sentencia del Tribunal Supremo, Sala Primera, de lo Civil, de 15 de noviembre de 1999, rec. 3320/1995).

La resolución del contrato, lo que impone integrar el «factum», tuvo lugar en forma extrajudicial por vía notarial el 21 de noviembre de 1991, conforme refiere el acta de 13 de abril de 1994 y a la vez y seguidamente se produjo la judicial por sentencia anterior a la presentación de la demanda, y aunque resultase firme posteriormente esto no es impeditivo para la ejecución de aval cuando concurren los supuestos fácticos que establece el artículo uno de la Ley 57/1968 y que la sentencia recurrida concreta a incumplimiento único del vendedor como hecho que resultó probado.

La norma no exige precisamente que la resolución tenga que ser necesariamente judicial ni tampoco supedita la operatividad del aval a la misma, pues el artículo tres contiene la expresión de que el comprador podrá optar por la rescisión contractual, con lo que ésta no se presenta imperativa, es decir que deberá de proceder en todo caso. Lo que ha de tenerse en cuenta es la concurrencia de incumplimiento acreditado, pues esta situación actúa como presupuesto que facilita la devolución de las cantidades anticipadas. En el caso presente tal situación incumplidora ha quedado precisada a la no terminación de la vivienda vendida en construcción por haberse paralizado las obras sin causa justificada y por tanto se está ante supuesto de construcción que no alcanzó buen fin, es decir el previsto y pactado en el contrato de adquisición».

Cumplidos, por tanto, los presupuestos para la ejecutividad del aval, constituido en fecha distinta y posterior a la del contrato de compraventa, no puede atenderse a requisitos formales no contemplados en la Ley y establecidos entre avalada y avalista sin intervención de los beneficiarios, pues supone de hecho una renuncia por parte de éstos a los derechos que, sin duda como consumidores de un bien de primera necesidad, les reconoce la Ley 57/1968, cuando lo cierto es que el art. 7 de la misma ley establece que «los derechos que la presente ley otorga a los cesionarios tendrán el carácter de irrenunciables», especialmente en lo referido al establecimiento de un plazo de validez del aval, cuando la Ley es clara en que el efecto de la expedición de la cédula de habitabilidad (salvo en aquellas Comunidades Autónomas donde baste la licencia de primera ocupación, por haberse suprimido la cédula de habitabilidad como documento necesario para reconocer la aptitud de un inmueble para ser destinado a vivienda) es la cancelación del aval y, por tanto, en clara contravención de lo dispuesto en esa Ley de carácter tuitivo e irrenunciable, no pudiendo verse perjudicados los consumidores por un pacto entre avalista y promotora estableciendo un plazo de validez del aval restringido y superando los límites del plazo de entrega convenido en el contrato, vinculándolo a unos requerimientos no contemplados en la norma y excediendo las fechas pactadas, con vulneración de la legislación protectora de consumidores y usuarios, y lleva a reputar tales estipulaciones como nulas y que han de tenerse por no puestas, visto lo dispuesto en el art. 6.3 del Código Civil, considerando el aval cuya ejecución se pretende plenamente válido, puesto que la limitación temporal de validez resulta ineficaz como óbice para la realización de un aval constituido conforme a lo dispuesto en la Ley, dentro de la finalidad de garantía de devolución de las cantidades adelantadas a cuenta caso de resolución del contrato, y sin perjuicio de las relaciones entre avalista y avalado ajenas a la sustanciación del pleito.

Por tanto, la devolución de las cantidades a cuenta ha de ser asumida por la ejecutada, por efecto del aval bancario constituido, ya que es avalista solidaria respecto del deudor principal, sin perjuicio de las consecuencias derivadas de la naturaleza solidaria del propio aval.

En definitiva, acreditada la no entrega en plazo por parte del promotor, por el informe de [ÓRGANO MUNICIPAL DE URBANISMO] de [LOCALIDAD], donde se constata que la Promotora no contaba con licencia de primera ocupación a la fecha pactada de entrega, existiendo aval del que resulta beneficiario mi mandante, y amparándole el derecho a acudir contra el garante para la ejecución del título de garantía, resulta evidente la viabilidad de la acción ejercitada.

VII.- COSTAS.

En virtud de lo dispuesto en el art. 539.2, párrafo 2.º, en relación con el 583.2 de la Ley de Enjuiciamiento Civil, las costas de la ejecución serán a cargo del ejecutado, puesto que no es preciso ninguna imposición expresa.

Por lo anteriormente expuesto,

SUPLICO AL TRIBUNAL

Que, teniendo por presentado este escrito con los documentos que se acompañan y sus copias, se sirva admitirlo, ordenando se entiendan conmigo las sucesivas diligencias y en nombre de mi patrocinado/a se me tenga por comparecido y parte, y por presentada demanda ejecutiva, se digne, previo el traslado legal, despachar ejecución frente a la entidad [DENOMINACIÓN SOCIAL], por el importe de la cantidad de [IMPORTE] euros ([IMPORTE] €) en concepto de principal, [IMPORTE] euros en concepto de intereses devengados hasta la fecha, más otros [IMPORTE] euros ([IMPORTE] €) presupuestados provisionalmente para los intereses que puedan generarse durante la ejecución y las costas de ésta, procediéndose, sin necesidad de efectuar previo requerimiento de pago, mediante decreto del Letrado de la Administración de Justicia, al embargo de la finca designada en el ordinal 7.º de los Hechos de esta demanda, que deberá asegurarse mediante mandamiento dirigido al Registrador de la Propiedad de [LOCALIDAD DEL REGISTRO], con la finalidad de que mi poderdante sea satisfecho en la totalidad de la deuda de la que esta ejecución dimana. Todo ello con imposición de las costas derivadas de esta ejecución al ejecutado.

Por ser de justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma de Abogado/a Firma de Procurador/a
