---
name: contrato-promesa-compraventa-inmueble-clausula-penal-civ-0837
description: "Contrato de promesa de compraventa de inmueble con cláusula penal y pago aplazado. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de promesa de compraventa de inmueble con cláusula penal y pago aplazado

> Formulario **CIV-0837** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Contrato de promesa de compraventa de bien inmueble con cláusula penal y pago aplazado con obligación del promitente comprador de subrogarse o liquidar la hipoteca concertada por el vendedor, siendo el promitente vendedor una sociedad inmobiliaria. Destacar que el mismo se encuentra sujeto a condición suspensiva y resolutoria.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de promesa de compraventa de inmueble con cláusula penal y pago aplazado» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de promesa de compraventa de inmueble con cláusula penal y pago aplazado” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:contrato-promesa-compraventa-inmueble-clausula-penal-civ-0837`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (10 veces)
- [ ] LOCALIDAD (7 veces)
- [ ] IMPORTE (5 veces)
- [ ] NÚMERO (5 veces)
- [ ] FECHA (4 veces)
- [ ] DENOMINACIÓN SOCIAL (3 veces)
- [ ] ENTIDAD BANCARIA (2 veces)
- [ ] SUCURSAL (2 veces)
- [ ] AÑO
- [ ] CALLE
- [ ] CARGO
- [ ] CÓDIGO DE CUENTA DE COTIZACIÓN
- [ ] DATOS REGISTRALES
- [ ] DOMICILIO
- [ ] IDENTIFICACIÓN DE LA VIVIENDA
- [ ] INSTITUCIÓN ARBITRAL
- [ ] LUGAR
- [ ] MUNICIPIO
- [ ] NOMBRE DE LA CALLE
- [ ] NOMBRE DE LA PROMOCIÓN
- [ ] Nº
- [ ] Nº DE COLEGIADO/A
- [ ] Nº DE CUENTA (IBAN)
- [ ] Nº DE PARCELAS
- [ ] Nº DE TRIMESTRE
- [ ] OTROS DATOS
- [ ] PLAZO

## Normas que cita el formulario

- art. 1.504 Código Civil
- art. 5 Real Decreto 515/1989
- art. 1.522 Código Civil
- art. 106 Real Decreto Legislativo 2/2004

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

Notas al pie del formulario original:
(1) Jurisprudencia de interés.- En el ámbito de la diferenciación entre los supuestos de auténticos contratos de compraventa y contratos de promesa de compra.

— Audiencia Provincial de Alicante, Sección 9ª, Sentencia 328/2011 de 14 Jul. 2011, rec. 39/2011.

«(...) En relación con el concepto de la promesa de comprar y vender la STS de 24 de octubre de 2008, Rec. 2454/2002, nos dice que" La Sentencia de 5 de octubre de 2005, Rec. 563/1999, en línea con la doctrina consolidada de esta Sala, diferencia el precontrato de compraventa del definitivo, constituyendo el precontrato "una primera fase del iter contractus: la relación jurídica obligacional nace en aquél y posteriormente, de común acuerdo o por exigencia de una de las partes, se pone en vigor el contrato que había sido preparado. Así, se distinguen dos fases: la primera, el precontrato que es distinto del contrato y no produce los efectos de éste, como pudiera ser la transmisión de la propiedad, sino sólo el que las partes pueden exigirse el paso a la fase segunda, que es la celebración del contrato preparado y es éste el que producirá los efectos que le son propios. Distinción entre el precontrato consistente en la promesa de venta y el contrato de compraventa que han seguido con clara precisión las Sentencias de 11 de octubre de 2000, rec. 2750/1995, 20 de abril de 2001, rec. 968/1996 y 31 de diciembre de 2001, rec. 2652/1996.»

— Audiencia Provincial de Granada, Sección 3ª, Sentencia 213/2010 de 28 May. 2010, rec. 190/2010.

« (...) La jurisprudencia siempre ha distinguido entre la promesa bilateral de vender y comprar y el contrato de compraventa" (STS de 23 de marzo de 1995, rec. 632/1992); y que "es incuestionable que no siempre se presenta de la misma forma y manera el contrato de promesa de venta, pues unas veces las propias partes contratantes han dejado para el futuro la propia obligación de celebrar el contrato definitivo, sino también la total y completa determinación de los elementos y circunstancias del referido contrato; en otros supuestos, las mismas partes, demuestran su decidida voluntad —en todos los pormenores y detalles— de celebrar un auténtico contrato de compraventa, que de momento no pueden actuar por impedirlo la concurrencia de determinados obstáculos como falta de autorizaciones o liberación de gravámenes, o simplemente porque en dicho instante no les conviene la celebración en firme y desean esperar cierto plazo, poniendo de manifiesto su voluntad de presente, sino exacta y total para cuando cesen aquellos obstáculos o venza el término establecido, momento a partir del cual es incuestionable que si uno incumple lo prometido el otro estará facultado a exigir el cumplimiento no de la promesa en sí, sino también del contrato definitivo al que aquella voluntad se determinó y para cuya realidad actual no existe ya obstáculo.»

— Otras sentencias de interés. Audiencia Provincial de Barcelona, Sección 14ª, Sentencia 274/2014 de 17 Jul. 2014, Rec. 21/2013.

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

En [LUGAR], a [FECHA].

REUNIDOS

DE UNA PARTE, D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con domicilio en [LOCALIDAD], provisto de N.I.F. número [NÚMERO].

Y, DE OTRA PARTE, D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con domicilio en [LOCALIDAD], provisto de N.I.F. número [NÚMERO].

INTERVIENEN

El primero, como [CARGO] en nombre y representación de la sociedad denominada [DENOMINACIÓN SOCIAL], constituida por escritura pública otorgada el [FECHA] ante el Notario de [LOCALIDAD] D./Dña. [NOMBRE Y APELLIDOS] con el número [NÚMERO] de su protocolo, domiciliada en [DOMICILIO] y con N.I.F número [NÚMERO]. Está autorizado para la celebración de este acto, en virtud del poder que dicha sociedad le tiene conferido en escritura pública otorgada el [FECHA] ante el Notario de [LOCALIDAD] D./Dña. [NOMBRE Y APELLIDOS] con el número [NÚMERO] de su protocolo. Inscrita en [DATOS REGISTRALES], de nacionalidad española, es designada en adelante en este documento como la parte promitente vendedora.

El segundo, en su propio nombre y derecho, y será designado en el presente contrato como la parte promitente compradora.

Ambas partes recíprocamente se reconocen la suficiente capacidad legal y legitimación para llevar a efecto el presente contrato de PROMESA DE COMPRAVENTA, acreditando su identidad por los documentos indicados, y que de común acuerdo se regirá por todo lo establecido libre y voluntariamente en el contenido de las siguientes:

ESTIPULACIONES

Primera

Que [DENOMINACIÓN SOCIAL] tiene proyectado el desarrollo de una promoción inmobiliaria consistente en un conjunto de viviendas en las parcelas [Nº DE PARCELAS], en el término municipal de [MUNICIPIO], cuya denominación comercial será [NOMBRE DE LA PROMOCIÓN], según proyecto redactado por D./Dña. [NOMBRE Y APELLIDOS], colegiado/a nº [Nº DE COLEGIADO/A] del Colegio Oficial de Arquitectos de [LOCALIDAD].

Segunda

Que interesando a [NOMBRE Y APELLIDOS] adquirir, en su día, la vivienda del proyecto de identificación: [IDENTIFICACIÓN DE LA VIVIENDA]; y habiendo llegado a un acuerdo con [NOMBRE Y APELLIDOS], lo formalizan mediante el presente contrato de promesa de compraventa, que se regirá con sujeción a lo dispuesto en el Código Civil Español y muy particularmente conforme a lo acordado en las sucesivas estipulaciones.

Tercera

La sociedad [DENOMINACIÓN SOCIAL] promete vender a [NOMBRE Y APELLIDOS], quien promete comprar, en su día, la vivienda descrita en la anterior estipulación, bajo la condición suspensiva establecida en la cuarta estipulación, en la modalidad de "llaves en mano", y como cuerpo cierto.

Para la correcta identificación de la vivienda citada y de sus características se adjunta al presente contrato, firmado por ambas partes y como parte del mismo, la siguiente documentación:

- Plano de la vivienda y del conjunto residencial, donde se identifica la vivienda que se trasmite.
- Memoria descriptiva de las características técnicas de la construcción.

Cuarta

La presente promesa de compraventa queda sujeta a la condición suspensiva consistente en que, no más tarde del día [FECHA] haya sido concedida por parte del Excmo. Ayuntamiento de [LOCALIDAD] la licencia de obras mayores para la construcción del conjunto de viviendas de constante referencia. En el supuesto caso de que llegado dicho día, no se hubiera cumplido la condición, la parte promitente compradora quedará facultada para resolver la compraventa y solicitar la devolución por parte de la sociedad promitente vendedora de la totalidad de las cantidades entregadas hasta entonces a cuenta del precio, más el interés legal correspondiente. En caso de no ejercitar la parte promitente compradora la facultad de resolución, mediante comunicación fehaciente, en los 15 días siguientes a la fecha del [OTROS DATOS], se entenderá a todos los efectos prorrogado el plazo de esta condición suspensiva en otros seis meses más.

Quinta

El precio pactado de esta promesa de venta es de [IMPORTE] euros ( €). Hallándose la presente promesa de compraventa sujeta al Impuesto sobre el Valor Añadido, el pago de dicho precio se verá incrementado con el mismo, al tipo que en cada momento sea de aplicación conforme a la Ley y Reglamento reguladores de dicho tributo.

Sexta

La forma de pago del precio convenida por las partes es la siguiente:

La parte promitente vendedora ha recibido la cantidad de [IMPORTE] euros ( €) más el IVA correspondiente a dicha cantidad, que asciende a [IMPORTE] euros ( €), quedando pendientes cuatro Letras trimestrales por importe de [IMPORTE] euros ( €), cuyos vencimientos son los días uno de enero, abril, julio, y octubre respectivamente, plazo en el que se entregarán las llaves y se elevará la escritura pública de compraventa, quedando pendiente la cantidad de [IMPORTE] euros ( €) que se harán efectivas mediante crédito hipotecario que la sociedad mantiene con el Banco de [ENTIDAD BANCARIA], sucursal [SUCURSAL], nº [Nº] de ccc [CÓDIGO DE CUENTA DE COTIZACIÓN], y domicilio social en la calle [CALLE], y en el que la parte promitente compradora se subrogará bien de forma total o parcial, o en su defecto la liquidará. Tanto a las Letras trimestrales como a la cantidad pendiente de hipoteca la sociedad promitente vendedora incrementará el IVA de legal aplicación.

Asimismo, la parte promitente vendedora se obliga a ingresar las cantidades recibidas de la promitente compradora, a cuenta del precio de la presente promesa de compraventa, en la cuenta n° [Nº DE CUENTA (IBAN)] de la Entidad bancaria [ENTIDAD BANCARIA], oficina [SUCURSAL], situada en la [NOMBRE DE LA CALLE] de esta capital, comprometiéndose a disponer de las mismas únicamente para atender los gastos e inversiones derivados de la promoción inmobiliaria de referencia.

Séptima

La presente promesa de compraventa queda sometida a condición resolutoria para el supuesto de impago en las fechas pactadas de alguna de las cantidades del precio aplazado, lo que es considerado expresamente por las partes como condición esencial del contrato. En consecuencia, si la parte promitente compradora no satisfaciera el precio aplazado en la forma y plazos estipulados y, previa notificación, notarial o judicial, de conformidad con lo dispuesto en el artículo 1.504 del Código Civil, la parte promitente vendedora podrá considerar automáticamente resuelta la presente promesa de compraventa, con pérdida para el promitente comprador de las cantidades entregadas hasta entonces, en concepto de cláusula penal.

En todo caso, la parte promitente vendedora podrá reclamar el pago de las cantidades aplazadas mientras no haya efectuado la notificación fehaciente de resolución de este contrato.

Particularmente, se hace constar que cualquier pago parcial de las cantidades pactadas se entenderá que lleva implícito parte del precio y su parte proporcional de I.V.A., es decir, se entenderá como ‘con I.V.A. incluido’.

Cuantos honorarios, gastos e impuestos se devenguen por la reclamación judicial o extrajudicial que debiera interponer la vendedora, en caso de incumplimiento en el pago de la promitente compradora hasta obtener su cumplimiento o, en su caso, la resolución de presente contrato, serán de la exclusiva cuenta y cargo de la promitente compradora, con inclusión de los honorarios y suplidos de Letrado y Procurador, aun cuando su intervención no fuese preceptiva o no se produjese imposición de costas.

A los efectos de la notificación a que se refiere el mentado artículo 1.504 del Código Civil, se establece como domicilio del promitente comprador el que figura en la comparecencia de este documento.

Octava

La finca vendida se entregará libre de cargas y gravámenes, arrendatarios y ocupantes y al corriente de gastos, contribuciones e impuestos.

A partir de entonces, la parte compradora participará en la proporción que resulte de la aplicación de los coeficientes que le correspondan en el mantenimiento de los gastos comunes del conjunto, que vendrá obligada a pagar, al igual que cualesquiera otros gastos, impuestos, tasas y arbitrios que se refieran o graven la finca objeto de este contrato.

Novena

La promitente vendedora, siempre bajo supervisión de la dirección facultativa de las obras, se reserva la facultad de efectuar en las mismas las modificaciones que le fuesen impuestas por las autoridades estatales, autonómicas o municipales, así como aquellas otras que le fuesen autorizadas y viniesen motivadas por exigencias técnicas o jurídicas durante su ejecución. Será responsabilidad de la promitente vendedora la obtención de las pertinentes licencias que, en su caso, amparen y autoricen dichas modificaciones.

Décima

La parte promitente vendedora se obliga a tener finalizadas las obras de construcción de la vivienda que se trasmite, salvo causa de fuerza mayor, desastres naturales o causas técnicas o administrativas de tipo objetivo, como máximo antes del término del [Nº DE TRIMESTRE] trimestre del año [AÑO], gozando no obstante la promitente vendedora de un plazo de gracia de otros tres meses.

Si la parte promitente vendedora incumpliese su obligación de entregar a la parte promitente compradora la referida vivienda en la fecha estipulada y conforme a las condiciones y características convenidas, el presente contrato quedará resuelto, en cuyo caso la parte promitente vendedora deberá devolver a la parte promitente compradora las cantidades que ésta haya anticipado a cuenta del precio estipulado, incrementadas, de conformidad con lo establecido en la Ley 38/1999, de 5 de noviembre, de Ordenación de la Edificación.

[ELEGIR UNA DE LAS ALTERNATIVAS QUE SIGUEN Y SUPRIMIR LAS DEMÁS]

Undécima

Finalizadas las obras de construcción de la vivienda, la parte promitente vendedora requerirá con al menos tres días de antelación a la promitente compradora, para que esta última comparezca, ante el Notario que la parte promitente vendedora designe, a lo que da la parte promitente compradora su conformidad, a los efectos de abonar la total cantidad del precio pendiente de pago, formalizar la oportuna escritura pública de compraventa, y recibir las llaves de la finca que adquiere, quedando obligada la parte promitente compradora a recibirlas.

Undécima

De conformidad con lo dispuesto en el artículo 126 del Reglamento Notarial y en el artículo 5 Real Decreto 515/1989 de 21 de abril, la elección del Notario autorizante de la Escritura Pública de compraventa corresponderá a la parte promitente compradora, debiendo notificar a la parte promitente vendedora su elección por cualquier medio con una antelación mínima de [PLAZO] a la fecha de otorgamiento de la escritura.

[ELEGIR UNA DE LAS ALTERNATIVAS QUE SIGUEN Y SUPRIMIR LAS DEMÁS]

A partir de la fecha en que fuera requerida para formalizar la escritura de compraventa y en el supuesto de que no acudiese a ella, los intereses legales del importe pendiente de pago, serán por cuenta de la parte promitente compradora.

Si alguna de las partes no concurriera a la firma de la escritura pública y a efectuar el correspondiente pago y cobro, quien no sea culpable del incumplimiento podrá reclamar a la otra parte los derechos y obligaciones del presente contrato y los daños y perjuicios que el retraso le ocasione o reclamar los daños y perjuicios que el incumplimiento de este contrato le ocasione desistiendo del mismo.

Duodécima

En el momento previo a la entrega, el promitente comprador podrá solicitar de la promitente vendedora una visita a la vivienda.

Decimotercera

En este acto y muy expresamente la parte promitente compradora autoriza y, en lo menester apodera, a la parte promitente vendedora a:

a) Otorgar la correspondiente escritura de declaración de obra nueva y, en su caso, división en propiedad horizontal del conjunto a construir, estableciendo libremente y en los términos que tenga por convenientes los estatutos que vendrán a regir la comunidad de propietarios, asignando las cuotas de participación y, en su caso, constituyendo las servidumbres que conforme al proyecto y usos pretendidos del edificio hubiere a lugar.
b) Convocar, en su momento, la oportuna primera reunión de copropietarios a fin de constituir la comunidad y designar, en su caso, el Presidente y el Secretario-Administrador. A estos efectos, y conforme a lo dispuesto en la vigente Ley de Propiedad Horizontal, la entidad aquí promitente vendedora fijará por escrito y con la suficiente antelación, el lugar, día y hora de dicha reunión, a la que caso de no asistir por sí mismo o representado el aquí promitente comprador, lo estará a todos los efectos y asuntos que hayan de tratarse, por la promitente vendedora, en quien delega en este acto y para dicho supuesto y momento su representación, con plenitud de facultades.
c) Asimismo, la promitente compradora deberá efectuar la correspondiente provisión de fondos para afrontar los gastos de la puesta en marcha de los servicios generales de la comunidad.
d) Contratar, por su cuenta y cargo, los servicios necesarios para la puesta en funcionamiento del edificio, así como la oportuna póliza de seguro, en Compañía de reconocida solvencia, que cubra el riesgo de incendio, si lo estimare conveniente.

Decimocuarta

La parte promitente compradora renuncia en este acto, expresa y formalmente, al derecho de retracto que le concede el artículo 1.522 del Código Civil sobre las ventas que puedan efectuarse de los restantes elementos y participaciones indivisas de la finca.

Decimoquinta

Cuantos honorarios, gastos e impuestos se deriven del presente contrato serán de exclusiva cuenta y cargo de la parte compradora, con exclusión del Impuesto sobre el Incremento del Valor de los Terrenos de Naturaleza Urbana que de conformidad con establecido en el artículo 106 del Real Decreto Legislativo 2/2004, de 5 de marzo, por el que se aprueba el texto refundido de la Ley Reguladora de las Haciendas Locales, será a cargo del vendedor. Para atender el pago de estos honorarios, gastos e impuestos, el comprador efectuará la oportuna provisión de fondos en el momento en que se otorgue la correspondiente escritura pública de compraventa.

Por contra, serán de la exclusiva cuenta y cargo del vendedor los gastos derivados de su título de propiedad, de la escritura de obra nueva y división en régimen de propiedad horizontal y de la constitución de la hipoteca que en su caso se contrate.

Decimosexta

El promitente comprador declara conocer cuántos documentos y disposiciones legales se citan en el presente contrato, y particularmente los artículos 1.279 y 1.280.1 del Código Civil.

Por su parte, la promitente vendedora hace expresa manifestación de que tiene en sus oficinas a disposición del público en general, y del promitente comprador en particular, cuantos documentos e información viene obligado a suministrar de conformidad con las disposiciones que regulan la protección de los consumidores.

Decimoséptima

A los efectos de cualesquiera notificación o requerimiento, se establecen como domicilios de las partes los que constan en la comparecencia de esta escritura. Cualquier traslado de domicilio, para tener efectos frente a la otra parte, deberá ser previa y fehacientemente comunicado.

Decimoctava

De conformidad con el Real Decreto 390/2021, de 1 de junio, por el que se aprueba el procedimiento básico para la certificación de la eficiencia energética de los edificios, el vendedor se obliga a entregar al comprador copia de la etiqueta energética con la que debidamente cuente el inmueble objeto del presente contrato.

[ELEGIR UNA DE LAS ALTERNATIVAS QUE SIGUEN Y SUPRIMIR LAS DEMÁS]

Decimonovena

Para cualquier duda o divergencia acerca de la interpretación y/o ejecución del presente contrato, las partes, con expresa renuncia a sus propios fueros si fuesen otros, se someten a los Tribunales de la ciudad de [LOCALIDAD].

Decimonovena

Las partes se comprometen a dilucidar las cuestiones, controversias y discrepancias que puedan surgir de la aplicación e interpretación del presente contrato a arbitraje, y en particular a [INSTITUCIÓN ARBITRAL].

Y, en prueba de conformidad con cuanto antecede, ambas partes, por duplicado ejemplar y a un sólo efecto, firman el presente documento, quedando uno en poder de cada parte, en el lugar y fecha al principio indicados, visando todas sus hojas.

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

ANEXO I: PLANO DE LA VIVIENDA

ANEXO II: MEMORIA DESCRIPTIVA
