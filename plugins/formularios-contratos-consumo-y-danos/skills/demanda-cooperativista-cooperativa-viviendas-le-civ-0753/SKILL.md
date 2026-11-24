---
name: demanda-cooperativista-cooperativa-viviendas-le-civ-0753
description: "Demanda del cooperativista para que la cooperativa de viviendas le devuelva lo aportado. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda del cooperativista para que la cooperativa de viviendas le devuelva lo aportado

> Formulario **CIV-0753** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio ordinario sobre reclamación de cantidad frente a cooperativa de viviendas por reintegro de las cantidades entregadas en concepto de aportaciones al capital y pago de una vivienda, a consecuencia de baja de cooperativista, habiendo transcurrido el plazo para proceder a su devolución.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda del cooperativista para que la cooperativa de viviendas le devuelva lo aportado» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda del cooperativista para que la cooperativa de viviendas le devuelva lo aportado” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:demanda-cooperativista-cooperativa-viviendas-le-civ-0753`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº DE DOCUMENTO (7 veces)
- [ ] IMPORTE (6 veces)
- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] FECHA (4 veces)
- [ ] DENOMINACIÓN SOCIAL (3 veces)
- [ ] FECHAS (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] EJERCICIO
- [ ] LUGAR
- [ ] Nº
- [ ] Nº DE ARTÍCULO
- [ ] PARTE DEMANDADA
- [ ] SEDE
- [ ] TEXTO DEL ESCRITO

## Normas que cita el formulario

- art. 399.1 LEC
- art. 9.2 LOPJ
- art. 87.6.a LOPJ
- art. 45 LEC
- art. 51 LEC
- art. 6.1.3.º LEC
- art. 7.4 LEC
- art. 10 LEC
- art. 253.1 LEC
- art. 251 LEC
- art. 23 LEC
- art. 399 LEC
- art. 5 Ley Orgánica 1/2025
- art. 1 Ley 5/1998
- art. 7.1 Código Civil
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

### Avisos de actualización (0) — se aplican en el texto, nunca se copian en el documento

- Ninguno.

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

A LA SECCIÓN DE LO MERCANTIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS], según acredito mediante escritura de poder inscrito en el Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], dirigido por el Letrado abajo firmante D./Dña. [NOMBRE Y APELLIDOS], con despacho profesional en [LOCALIDAD], ante el Tribunal comparezco y como mejor proceda en Derecho DIGO:

Que en la representación que ostento, interpongo DEMANDA DE JUICIO DECLARATIVO ORDINARIO sobre reclamación de cantidad frente a la mercantil [DENOMINACIÓN SOCIAL], Sociedad Cooperativa Gallega, con domicilio en

Que esta parte asume el compromiso de recibir cualquier comunicación dirigida por la oficina judicial, durante toda la fase declarativa, e, incluso, en una eventual fase de ejecución por medios telemáticos, en términos del art. 399.1 II LEC, consignándose a estos efectos la siguiente dirección de correo electrónico y nº [Nº] de teléfono:

Fundamento la misma en los siguientes hechos y consideraciones jurídicas:

HECHOS

PRIMERO.- Mi representado ha venido ostentado la condición de socio de [DENOMINACIÓN SOCIAL], según acredito con copia del libro-registro de socios de la cooperativa citada, que acompaño como documento número [Nº DE DOCUMENTO] de los que se unen a la presente demanda.

SEGUNDO.- La entidad demandada es una sociedad cooperativa de viviendas cuyo objeto es procurar a sus socios principalmente una vivienda para uso personal y familiar o local para el desarrollo de sus actividades, según resulta de la escritura pública fundacional y de los estatutos incorporados a la misma, cuya copia se aporta como documento número

TERCERO.- Con este designio y de acuerdo con el objeto propio de la cooperativa, D./Dña. [NOMBRE Y APELLIDOS] ha realizado diversas aportaciones con destino a la construcción de un edificio de viviendas sito en [LOCALIDAD], por importe de [IMPORTE] euros, cuyo reintegro se solicita en esta demanda.

Aparte de las citadas cantidades entregadas para financiar el pago de la vivienda, la devolución de las aportaciones obligatorias al capital social (reembolso de participaciones) asciende a la cantidad de [IMPORTE] euros, calculados conforme al balance de cierre del ejercicio [EJERCICIO] en el que se ha causado la baja.

Para acreditar los extremos anteriores se acompañan los siguientes documentos:

CUARTO.- Con fecha [FECHA], mi mandante dirigió escrito al Consejo Rector de [DENOMINACIÓN SOCIAL], expresando textualmente que [TEXTO DEL ESCRITO]; y terminaba solicitando la baja voluntaria y el reintegro de las cantidades aportadas antes detalladas.

Acredito dicha circunstancia con el original del burofax por el que se efectuó dicha solicitud (documento número [Nº DE DOCUMENTO]).

QUINTO.- El Consejo Rector, en reunión de [FECHA], acordó "darse por enterado del escrito de solicitud de baja voluntaria", acordando comunicarlo a la Asamblea, previa convocatoria al efecto (documento número [Nº DE DOCUMENTO]).

SEXTO.- La cooperativa adoptó un acuerdo, en Asamblea de fecha [FECHA] en el que se "acordaba por unanimidad aceptar la baja como socio de la cooperativa de D./Dña. [NOMBRE Y APELLIDOS] y devolverle en su momento las cantidades aportadas" (documento número [Nº DE DOCUMENTO]).

SÉPTIMO.- El día, el actor remitió burofax a la cooperativa, requiriéndole para que procediese a efectuar la liquidación de las cantidades que se le debían por todos los conceptos, al haber transcurrido con exceso el plazo señalado por la ley y los estatutos para proceder a su devolución, tanto de las aportaciones a capital social como de las entregas para el pago de la vivienda (documento número [Nº DE DOCUMENTO]).

Dicho requerimiento no ha sido atendido por la demandada lo que fuerza la interpelación judicial.

OCTAVO.- Previamente a la presentación de la presente solicitud, se llevaron a cabo diversos esfuerzos de negociación con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad, y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria.

Entre las acciones realizadas, se incluyen el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución; así como la participación en reuniones llevadas a cabo los días [FECHAS], cuyos objetivos fueron buscar una conciliación respecto de las diferencias planteadas.

Se adjuntan como prueba copias de las comunicaciones enviadas y recibidas durante el proceso de negociación, incluidas cartas, correos electrónicos y/o actas de reuniones como documentos números [Nº DE DOCUMENTO].

FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN Y COMPETENCIA.

Sobre materia de la competencia genérica del orden civil de la jurisdicción (art. 9.2 LOPJ), tiene la competencia objetiva y funcional [art. 87.6.a) I LOPJ y art. 45 LEC) la Sección de lo Mercantil del Tribunal de Instancia de esta villa, y la territorial, puesto que la entidad demandada tiene su domicilio social en el partido judicial del Tribunal al cual tengo el honor de dirigirme (art. 51 LEC).

II.- CAPACIDAD Y LEGITIMACIÓN.

Mi representado es mayor de edad y se encuentra en situación de pleno ejercicio de sus derechos civiles, en virtud de lo dispuesto en los arts. 6.1.1.º y 7.1 LEC. Asimismo, la demandada es persona jurídica, cuya capacidad se reconoce en el art. 6.1.3.º LEC, derivándose su personalidad de su constitución en escritura pública inscrita en el Registro de Sociedades Cooperativas, con la necesidad de comparecer en juicio por medio de sus representantes legales (art. 7.4 LEC).

La legitimación activa corresponde al demandante en su calidad de socio de la sociedad cooperativa demandada, que ostenta la legitimación pasiva correlativa (art. 10 LEC).

III.- PROCEDIMIENTO.

La presente demanda deberá sustanciarse por las normas del juicio ordinario, a tenor de lo prevenido en los arts. 248 y 249.2 LEC, toda vez que el criterio de atribución preferente de la materia objeto del proceso resulta inaplicable, al carecer de especialidad típica la de éste, y cumplir entonces el criterio de cuantía, que supera los 15.000 euros.

IV.- CUANTÍA.

Cumpliendo lo prevenido en el art. 253.1 LEC, hacemos constar que la cuantía de esta demanda es de [IMPORTE] euros ( [IMPORTE] €), calculada con arreglo a la regla 1.ª del art. 251 LEC, según la cual si se reclama una cantidad de dinero determinada, la cuantía de la demanda estará representada por dicha cantidad.

V.- POSTULACIÓN Y DEFENSA.

Conforme a los arts. 23 y 31 LEC se formula esta demanda a través de Procurador/a de los Tribunales con poder notarial para pleitos, y con dirección y firma de Letrado habilitado ante el Tribunal. Asimismo, se cumplen los requisitos formales del art. 399 LEC.

VI.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

VII.- FONDO DEL ASUNTO

1) Sobre el derecho del socio a causar baja en la cooperativa:

Las cooperativas son definidas en el art. 1 de la Ley 5/1998, de 18 de diciembre, de cooperativas de Galicia (en adelante, LCG) -aplicable al caso por tratarse de entidad cooperativas con domicilio social en la Comunidad Autónoma de Galicia y actividad cooperativizada dentro del territorio de la Comunidad gallega (art. 2 LCG)-, como sociedades de capital variable, de estructura democrática, en régimen de libre adhesión y baja voluntaria. El art. 14 LCG, en línea con dicha previsión, establece como contenido mínimo de los estatutos la obligatoria regulación de las condiciones y requisitos para adquirir la condición de socio y el régimen de baja. Y el art. 20 reconoce, en consonancia con lo anterior, el derecho del socio a causar baja en cualquier momento, exigiendo un preaviso por el tiempo previsto en los estatutos, que no podrá exceder del año. Si la obligación de preaviso se incumple, la norma declara la obligación de responder de los daños y perjuicios causados a la cooperativa.

La ley permite también que los estatutos impongan al socio el compromiso de no darse de baja voluntariamente sin justa causa en un período determinado, no superior a diez años, o hasta el final del ejercicio económico en que quiera causar baja. Desarrollando esta previsión, los estatutos de la cooperativa demandada (art. [Nº DE ARTÍCULO]), determinan el plazo de cinco años desde que el socio ingresó en la cooperativa. La consecuencia del incumplimiento por el socio de tal compromiso se expresa en la ley de forma alternativa: la obligación de participar en las actividades o servicios cooperativizados por el plazo comprometido o hasta el final del ejercicio, o bien la exigencia de una indemnización de daños y perjuicios.

En todo caso, tanto en situaciones de baja justificada o no, la norma estatutaria exige un preaviso de la intención de causar baja de al menos seis meses. La consecuencia de su incumplimiento no ha de ser la imposibilidad de causar baja -pues es este un derecho del socio, inherente a la naturaleza de la sociedad cooperativa-, sino la de indemnizar a la sociedad los perjuicios causados (cfr. STS de 16 de marzo de 1998, Rec. 247/1994).

De lo anterior se sigue el carácter esencial que presenta la calificación de la baja como justificada o no justificada. La ley permite al socio la libre y voluntaria decisión para poderse dar de baja de la Cooperativa en cualquier momento, como derecho inherente a su condición de cooperativista, pero sólo la baja justificada le permite una restitución plena y puntual de las cantidades aportadas al capital y a la actividad cooperativizada.

En efecto, la baja da derecho al socio al reembolso de sus aportaciones al capital social. Pero conviene distinguir entre las aportaciones de los socios al capital social, unas obligatorias y otras voluntarias, de las aportaciones de cantidades entregadas por los cooperativistas para financiar el pago de la vivienda -que no integran el capital social-, con régimen legal y estatutario distinto para el caso de baja del socio, sea por causa justificada o injustificada.

Así, el art. 64 LCG permite, en caso de baja del socio, que el plazo de reembolso por la cooperativa de las aportaciones al capital social pueda ser hasta cinco años a partir de la fecha de la baja. Y así se acuerda en el art. de los estatutos, en el caso de baja del socio, que en todo caso se retendrán las aportaciones al capital social mientras no finalice el ejercicio económico del año en que se presente la baja y siempre y cuando el socio haya sido sustituido por otro socio; en caso contrario se podrán retener hasta un máximo de doce meses a constar desde la aprobación de la baja por el Consejo Rector.

Por otra parte, el art. 121.2 LCG establece que en caso de baja del socio, la cooperativa podrá retener, por el plazo previsto en los estatutos, que no podrá exceder de un año, el total de las cantidades entregadas para financiar el pago de las viviendas hasta que sea sustituido por otro socio. Además, si la baja del socio es considerada como no justificada, los estatutos podrán prever la aplicación a las cantidades entregadas por el socio de determinadas reducciones y en un cierto porcentaje, destinando la cantidad retenida al fondo de reserva obligatorio. Así lo prevé el art. de los estatutos de la cooperativa demandada y recogiendo en esencia dicho precepto literalmente refiere "En caso de baja del socio, la Cooperativa podrá retener el total de las cantidades entregadas por el socio para financiar el pago de viviendas, hasta que sea sustituido en sus derechos y obligaciones por otro socio siempre y cuando finalizara el ejercicio económico del año en que presentase la baja. El plazo máximo de duración del derecho de retención será de doce meses a contar desde la aprobación de la baja por el Consejo Rector".

De tal modo se adecuan los estatutos a lo dispuesto en la Ley, al establecer que no podrá ser superior a un año el plazo de retención del total de las cantidades entregadas por el socio para financiar el pago de viviendas, que para el caso de que en ese interregno fuese sustituido en sus derechos y obligaciones por otro socio y siempre y cuando finalizara el ejercicio económico del año en que presentase la baja, en este momento, antes del transcurso del año fijado por la cooperativa con derecho a retención, está obligada al reembolso de las referidas aportaciones al socio que causó baja.

2) Sobre la comunicación y el carácter justificado de la baja:

El socio demandante comunicó en forma la solicitud de baja al órgano de administración. Desde ese momento la baja ha de producir efecto, pero sus consecuencias serán diferentes, en función de que la baja sea justificada o no, o se haya producido sin atención del plazo de preaviso. El consejo rector, en lugar de pronunciarse sobre el carácter de la baja o sobre la determinación de sus efectos, acordó remitir la cuestión a la asamblea, órgano que expresamente aceptó la baja, posponiendo sus consecuencias: la efectiva restitución de las cantidades aportadas.

De esta descripción de hechos se sigue, como forzada consecuencia, que la baja del cooperativista fue admitida como justa por la cooperativa. Los órganos de la entidad aceptaron la baja y aceptaron sus efectos, si bien decidieron posponerlos, sin plazo o razón alguna. Tal supone una actuación con capacidad para causar estado en la esfera jurídica de los litigantes.

Se está en presencia de un acto propio, dirigido a configurar un estado jurídico. El órgano soberano de la cooperativa expresamente admitió la baja del socio, lo que es tanto como reconocer su carácter justificado. De lo contrario se estaría actuando en contra de las exigencias de la buena fe.

En palabras de la STS de 19 de noviembre 2008, rec. 1531/2003: "la doctrina de los actos propios, o de la inadmisibilidad del "venire contra factum proprium" es de elaboración y desarrollo jurisprudencial y encuentra su fundamento en el principio de la buena fe (artículo 7.1 Código Civil) y en la protección de la confianza creada por la apariencia, que impone un deber de coherencia y limita la libertad de actuar cuando se han creado unas expectativas razonables, pues el comportamiento supone en tal caso la expresión inequívoca de una determinada voluntad en referencia a una relación jurídica o situación de hecho que impide la admisión como legítimo de un posterior comportamiento contradictorio (sentencias de esta Sala de 14 y 28 octubre 2005, 26 enero 2006 y 23 enero 2008, entre otras muchas)".

No cabe pues entender que el acto de expresa aceptación de la baja es inocuo desde el punto de vista de su calificación. El sistema legal exige que la decisión del socio sea calificada por los órganos de la cooperativa, pues sólo así podrán determinarse sus efectos. No cabe sostener que la decisión de la asamblea hubiera sido una suerte de dación de cuenta, con postergación de la decisión definitiva. La asamblea, se repite, expresamente "aceptó" la baja, lo que supone aceptar los argumentos del solicitante, que fundamentaban también de forma expresa su decisión en el aumento de los precios experimentados en el coste de la obra de edificación. Aceptar lo contrario supondría sumir en situación de indefensión al cooperativista, que no podría recurrir la decisión de considerar la baja como injustificada. La buena fe obligaba a la cooperativa a proclamar esta situación. Con su silencio ha de entenderse que aceptó el carácter justificado de la baja.

Tampoco los órganos de la cooperativa se pronunciaron sobre si el socio había infringido o no el plazo de preaviso, por lo que la solución ha de ser exactamente la misma. En este particular, la aceptación por la asamblea de la baja del socio supone dar ésta por válida, sin necesidad de posponer su eficacia seis meses después. La baja causa efecto desde el momento de su declaración por el cooperativista, de modo que el preaviso lo único que determina es, en su caso, un derecho de indemnización a favor de la cooperativa, pero ello no significa que los efectos de la baja se hayan de posponer al momento de conclusión del preaviso.

3) Sobre la restitución de las cantidades aportadas

Por tanto, aceptada la baja por la asamblea, lo procedente es la restitución de las cantidades anticipadas por el socio, sin que proceda, se insiste, la exigencia de indemnización alguna, ni la posibilidad de retener o deducir cantidades, al entenderse la baja como justificada, reembolso que habría de producirse en el plazo de un año desde que se produjo la baja, lo que tuvo lugar el día

VIII.- COSTAS.

Conforme al art. 394 LEC, las costas han de imponerse a la demandada.

En virtud de lo expuesto,

SUPLICO AL TRIBUNAL

que habiendo por presentado este escrito de demanda con los documentos que lo acompañan y copias de uno y otros, los admita y me tenga por comparecido en parte en la representación que ostento y que acreditada dejo; y por promovido juicio declarativo ordinario frente a [PARTE DEMANDADA], dé al mismo el curso señalado en la ley y, en su día, dicte sentencia en la que, estimando íntegramente esta demanda se condene a la entidad demandada al pago a mi representado de la cantidad de [IMPORTE] euros en concepto de devolución de sus aportaciones al capital social, así como la cantidad de [IMPORTE] euros entregada para financiar el pago de la vivienda, más los intereses legales que correspondan, y al pago de las costas

Es justicia de hacerse en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a

========================================================================
