---
name: contrato-compraventa-vivienda-construccion-segun-civ-0686
description: "Contrato de compraventa de vivienda en construcción según el Derecho civil catalán. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de compraventa de vivienda en construcción según el Derecho civil catalán

> Formulario **CIV-0686** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de compraventa de vivienda en construcción según el Derecho civil catalán» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de compraventa de vivienda en construcción según el Derecho civil catalán” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:contrato-compraventa-vivienda-construccion-segun-civ-0686`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (14 veces)
- [ ] LOCALIDAD (11 veces)
- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] FECHA (7 veces)
- [ ] Nº (7 veces)
- [ ] LINDEROS (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] PROVINCIA (3 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] ENTIDAD BANCARIA (2 veces)
- [ ] NIF/DNI (2 veces)
- [ ] AÑO
- [ ] CALLE
- [ ] DOMICILIO
- [ ] DÍA
- [ ] INSCRIPCIÓN
- [ ] LETRA
- [ ] MES
- [ ] NIF
- [ ] NOMBRE DEL NOTARIO
- [ ] Nº DE CUENTA (IBAN)
- [ ] Nº DE PAGOS
- [ ] Nº DE PISO
- [ ] Nº DE SÓTANO
- [ ] SUCURSAL

## Normas que cita el formulario

- art. 1.279 Código Civil

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

- Junto a «…UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD)»: La LO 15/1999 y su Reglamento (RD 1720/2007) fueron sustituidos por el Reglamento (UE) 2016/679 (RGPD) y la LO 3/2018, de 5 de diciembre (LOPDGDD). Fuente: LO 3/2018, disposición derogatoria única.

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

En la ciudad/localidad de [LOCALIDAD], provincia de [PROVINCIA], a [DÍA] de [MES] de [AÑO]

REUNIDOS

De una parte D./Dª [NOMBRE Y APELLIDOS], mayor de edad, vecino/a de [LOCALIDAD], con domicilio en la localidad/ciudad de [LOCALIDAD], provincia de [PROVINCIA], provisto/a del N.I.F. número [NIF/DNI]

Y de otra parte D./Dª [NOMBRE Y APELLIDOS], mayor de edad, vecino/a de [LOCALIDAD], con domicilio en la localidad/ciudad de [LOCALIDAD], provincia de [PROVINCIA] provisto/a del N.I.F [NIF/DNI]

INTERVIENEN

D./Dª [NOMBRE Y APELLIDOS], interviene en nombre y representación de la mercantil de [DENOMINACIÓN SOCIAL], CIF [NIF], domiciliada en [DOMICILIO] y constituida en [LOCALIDAD] ante el Notario de [LOCALIDAD] D. [NOMBRE Y APELLIDOS], en fecha [FECHA] e inscrita en el Registro Mercantil de [LOCALIDAD] inscripción [INSCRIPCIÓN] (en adelante LA VENDEDORA)

D./Dª [NOMBRE Y APELLIDOS], interviene en nombre propio (en adelante LA COMPRADORA).

MANIFIESTAN

Que intervienen en la indicada representación, se reconocen mutua y plena capacidad legal de obrar y de obligarse para este acto, otorgando de forma libre y espontánea y a su tenor el presente CONTRATO DE COMPRAVENTA DE INMUEBLE EN CONSTRUCCIÓN, asumiendo la responsabilidad que corresponda en función de la veracidad de sus manifestaciones, y, de mutuo acuerdo,

EXPONEN

I. Que la VENDEDORA/PROMOTORA es titular en pleno dominio del inmueble con la siguiente descripción: (se harían constar los datos del inmueble…)

II. Que, sobre el inmueble descrito, la PROMOTORA/VENDEDORA está construyendo un edificio compuesto de un número de [Nº] viviendas, [Nº] locales comerciales y [Nº] garajes, según proyecto, memoria, planos e indicaciones redactadas en el Libro de Órdenes, durante la obra, del Arquitecto D [NOMBRE Y APELLIDOS] y licencia del Ayuntamiento de [LOCALIDAD] de fecha

III. Que, dentro de la promoción expresada anteriormente, la parte COMPRADORA está interesada en adquirir la vivienda y garaje que tiene la siguiente descripción:

NÚMERO [NÚMERO]: VIVIENDA PISO [Nº DE PISO] LETRA [LETRA] del edificio sito en la localidad de [LOCALIDAD], en la calle [CALLE], número [NÚMERO] Tiene una superficie construida de [Nº] metros cuadrados y útil de [Nº] metros cuadrados. Linda: al frente, por donde tiene su entrada, con [LINDEROS] a la derecha entrando, con [LINDEROS]; a la izquierda entrando, con [LINDEROS] y al fondo, con

Tiene atribuida una cuota del % del total aparcamiento, que se concreta en el derecho de uso exclusivo de la PLAZA DE APARCAMIENTO número del sótano [Nº DE SÓTANO]

CUOTA: Le corresponde una cuota de participación en los elementos y gastos comunes de la comunidad de propietarios de por ciento para la vivienda y de [Nº] por ciento para la plaza de aparcamiento del total aparcamiento, que tiene asignado un [Nº] por ciento del total del inmueble.

HIPOTECA: El departamento descrito está afecto a una hipoteca en construcción otorgada por la entidad bancaria [ENTIDAD BANCARIA] por un principal de [IMPORTE] euros. Dicha hipoteca fue autorizada por el Notario [NOMBRE DEL NOTARIO] en escritura de fecha [FECHA], inscrita en el Registro de la Propiedad de [LOCALIDAD], finca número [NÚMERO], con una responsabilidad hipotecaria de [IMPORTE] euros, con vencimiento en fecha

IV. Que la COMPRADORA/ARRENDADORA está interesada en adquirir la vivienda y plaza de aparcamiento descritos en el expositivo anterior.

V. Que, conviniendo ambas partes en concertar el contrato, otorgan a tal fin el presente CONTRATO DE COMPRAVENTA DE INMUEBLE EN CONSTRUCCIÓN, que se rige por el Código Civil de Cataluña, en base en las siguientes

CLÁUSULAS

PRIMERA. - OBJETO DEL CONTRATO

Por medio del presente contrato, la VENDEDORA/PROMOTORA VENDE el inmueble descrito en el expositivo tercero a la COMPRADORA.

La venta se efectúa con cuantos derechos, usos, servicios y servidumbres son inherentes al inmueble, y que resultan del proyecto de ejecución. La venta se produce libre de arrendatarios y ocupantes, sin otras cargas y afecciones que las mencionadas en este contrato.

La vivienda y aparcamiento adquiridos se corresponden con los planos que se adjuntan como ANEXO I, y las calidades de los materiales de la vivienda serán las que se indican en el proyecto y las que se especifican en el documento ANEXO II, firmando los contratantes ambos anexos en prueba de conformidad y como parte integrante de este contrato.

SEGUNDA, PRECIO DE LA COMPRAVENTA

El precio total de esta compraventa es de [IMPORTE] Euros, con el siguiente desglose:

La cantidad de [IMPORTE] euros corresponde a la vivienda.
La cantidad de [IMPORTE] euros corresponde a la plaza de garaje.
La cantidad de [IMPORTE] euros es el % de IVA a abonar por LA COMPRADORA.

TERCERA. - FORMA DE PAGO

El precio pactado de compraventa lo abonarán la COMPRADORA de la siguiente forma:

a) En cuanto a la cantidad de [IMPORTE] euros, se abonará de forma anticipada a cuenta del precio, según detalle:

la cantidad de [IMPORTE] euros a la firma del presente contrato, sirviendo este documento de carta de pago y recibo de la citada cantidad.
la cantidad de [IMPORTE] euros mediante un número de [Nº DE PAGOS] pagos mensuales por importe de [IMPORTE] euros, con vencimiento el primero de ellos a la finalización del mes siguiente al de la firma de este documento.
la cantidad de [IMPORTE] euros antes del día [FECHA]

Las cantidades anticipadas entregadas a cuenta del precio se ingresarán en la cuenta especial [Nº DE CUENTA (IBAN)] abierta en la sucursal [SUCURSAL] de la entidad [DENOMINACIÓN SOCIAL] y quedan garantizadas, junto con el interés legal correspondiente, en la forma que se expresa en la estipulación cuarta.

b) En cuanto a la cantidad de [IMPORTE] euros, la abonará la COMPRADORA a la entrega de llaves que tendrá lugar dentro de los treinta días siguientes al plazo final establecido en la licencia el día [FECHA]

Para el pago correspondiente a la entrega de llaves, la COMPRADORA se subrogará en la hipoteca descrita en el expositivo III.

En cuanto a la cantidad restante de [IMPORTE] euros, la COMPRADORA manifiesta que será financiada por entidad de crédito.

CUARTA. - GARANTÍAS

La VENDEDORA declara y hace constar que ha garantizado la devolución, en su caso, del importe total de las cantidades anticipadas por la parte compradora mediante aval bancario prestado a su favor por la entidad de crédito [ENTIDAD BANCARIA], habiendo quedado formalizado el aval mediante póliza intervenida por el Notario Don [NOMBRE Y APELLIDOS], el día [FECHA]

La VENDEDORA entrega a la parte compradora en el momento de la firma de este contrato privado una copia del citado aval bancario, y se obliga a la devolución al adquirente de las cantidades percibidas a cuenta, incluidos los impuestos aplicables, más los intereses legales en caso de que la construcción no se inicie o termine en los plazos convenidos en este contrato, o no se obtenga la cédula de habitabilidad, licencia de primera ocupación o el documento equivalente que faculten para la ocupación de la vivienda.

La VENDEDORA se compromete a facilitar a la COMPRADORA el correspondiente certificado de garantía individual.

QUINTA. - DESISTIMIENTO POR FALTA DE FINANCIACIÓN

Caso de que la COMPRADORA no logre la financiación en el plazo de los treinta días siguientes al de la entrega de llaves, podrá desistir del contrato si justifica documentalmente la negativa de tres entidades de crédito a conceder la financiación o de la entidad hipotecante a aceptar la subrogación del comprador en la hipoteca que grava el inmueble, salvo que la denegación se derive de la negligencia de la COMPRADORA.

En este caso, el desistimiento obliga a la VENDEDORA a la devolución del precio que le hubiera sido entregado y obliga a la COMPRADORA a dejar a la VENDEDORA en la misma situación en la que se habría encontrado si no se hubiera concluido el contrato, sin perjuicio de lo establecido por la legislación hipotecaria.

SEXTA. PLAZO DE ENTREGA

La entrega de llaves se realizará dentro de los treinta días siguientes al plazo final establecido en la licencia el día [FECHA], salvo caso de fuerza mayor, siempre que la COMPRADORA tenga abonadas las devengadas en dicha fecha conforme a lo previsto en la estipulación tercera del presente contrato.

Se considera fecha de la entrega de llaves el día de la firma de la escritura pública de compraventa, según lo dispuesto en la estipulación séptima. Antes de dicha firma, la finca deberá contar con la correspondiente licencia municipal de primera ocupación, así como con la conformidad la COMPRADORA, quien podrá inspeccionar la finca. Si se supera la fecha pactada de entrega, el Comprador podrá optar por exigir el cumplimiento de la obligación, o por la resolución del contrato, en los términos estipulados en la cláusula novena.

SÉPTIMA. OTORGAMIENTO DE LA ESCRITURA DE VENTA Y TRANSMISION DE LA PROPIEDAD

Las partes contratantes se obligan a otorgar escritura pública de compraventa de la vivienda objeto de este contrato mediante su comparecencia ante Notario en el plazo de entrega. El otorgamiento de la escritura pública de compraventa implicará la entrega de la finca vendida, con la consiguiente transmisión de la propiedad de la misma.

La elección del Notario ante el cual deba otorgarse la correspondiente escritura pública de compraventa corresponderá a la COMPRADORA, debiendo notificar a la VENDEDORA el Notario de su elección por cualquier medio con una antelación mínima de siete días naturales a la fecha de otorgamiento de la escritura. La COMPRADORA no puede imponer Notario que, por su competencia territorial carezca de conexión razonable con alguno de los elementos personales o reales del negocio.

OCTAVA. RÉGIMEN DE COMUNIDAD

La COMPRADORA faculta a LA VENDEDORA para que otorgue e inscriba en el Registro de la Propiedad las escrituras públicas de agrupación y segregación que considere oportunas, la escritura de Declaración de Obra Nueva y División Horizontal, los Estatutos de la Comunidad, su Reglamento de Régimen Interior.

La descripción individualizada de los inmuebles vendidos con referencia expresa a las circunstancias reguladas por el artículo 553-9.1 del Código Civil de Cataluña, se adjuntan como ANEXO III de este contrato, el cual es firmado por ambas partes en prueba de conformidad.

NOVENA. CAUSAS DE RESOLUCIÓN Y CLÁUSULA PENAL

Serán causas de resolución de la compraventa el incumplimiento grave y culpable de cualquiera de las partes de las obligaciones de este contrato.

En el caso de incumplimiento por la COMPRADORA por falta de pago, en los plazos pactados, de cualquiera de las cantidades que se han aplazado hasta el otorgamiento de la escritura, la VENDEDORA podrá optar por resolver el contrato, previo requerimiento de pago de dichas cantidades, o por el cumplimiento.

En este caso, si la VENDEDORA decidiera resolver la compraventa, tendrá derecho a retener como propias las cantidades entregadas hasta la fecha por la COMPRADORA, hasta el límite del diez por ciento (10%) del precio de la compraventa, en concepto de cláusula penal que sustituye a la indemnización de daños y perjuicios.

Si la VENDEDORA optara por exigir el estricto cumplimiento del contrato, tendrá derecho a una indemnización consistente en la cantidad que resulte de aplicar al importe adeudado el interés de demora del 8% sobre las cantidades impagadas en concepto de cláusula penal que sustituye a indemnización de daños y perjuicios.

En el caso de incumplimiento por la VENDEDORA del plazo de entrega previsto en la estipulación sexta, la COMPRADORA podrá optar por la resolución del contrato o por el cumplimiento.

Si la COMPRADORA opta por la resolución del contrato, la VENDEDORA, además de devolver las cantidades entregadas por la COMPRADORA, le indemnizará con una cantidad equivalente al cinco por ciento del precio de la compraventa, en concepto de cláusula penal que sustituye a la indemnización de daños y perjuicios.

Si la COMPRADORA opta el cumplimiento, la VENDEDORA le indemnizará con la suma de [IMPORTE] euros diarios desde la fecha pactada hasta el día de la entrega efectiva de la finca, en concepto de cláusula penal que sustituye a indemnización de daños y perjuicios.

DÉCIMA. GASTOS E IMPUESTOS

Serán dé cuenta de la VENDEDORA el Impuesto sobre el Incremento de valor de los Terrenos de Naturaleza Urbana y cualesquiera gastos que deriven de actos previos al otorgamiento de la escritura de compraventa y que sean necesarios para el otorgamiento de la misma y su inscripción en el Registro de la Propiedad. En consecuencia, serán dé cuenta de la VENDEDORA todos los gastos notariales, registrales, fiscales o de otro tipo que deriven del otorgamiento e inscripción de la escritura de obra nueva y división horizontal, del préstamo hipotecario concedido al promotor, y de la cancelación de embargos, hipotecas, condiciones resolutorias expresas, precios aplazados o cualesquiera otras cargas que recaigan sobre la finca vendida en la fecha de otorgamiento de la escritura de compraventa. Asimismo, serán de su cuenta los gastos del otorgamiento de la escritura de compraventa.

Serán dé cuenta de la COMPRADORA los impuestos de cualquier tipo que graven la adquisición de la finca comprada en virtud de este contrato, los gastos por el otorgamiento de la primera copia y demás posteriores de la escritura pública de compraventa y los honorarios registrales por la inscripción en el Registro de la Propiedad a nombre de la COMPRADORA de la adquisición efectuada.

UNDÉCIMA. PROTECCIÓN AL CONSUMIDOR

De conformidad a lo dispuesto en el RD 515/1989, de 21 de abril, la parte VENDEDORA hace constar la siguiente información dirigida al consumidor-COMPRADORA:

a) Que el consumidor no soportará los gastos derivados de la titulación que correspondan legalmente al vendedor.

b) El artículo 1.280, 1.º del Código Civil establece: “Deberán constar en documento público: 1.º Los actos y contratos que tengan por objeto la creación, transmisión, modificación o extinción de derechos reales sobre bienes inmuebles”.

El art. 1.279 del Código Civil establece: “Si la ley exigiere el otorgamiento de escritura u otra forma especial para hacer efectivas las obligaciones propias de un contrato, los contratantes podrán compelerse recíprocamente a llenar aquella forma desde que hubiese intervenido el consentimiento y demás requisitos necesarios para su validez”.

c) El derecho a la elección de Notario que corresponde al consumidor, sin que éste pueda imponer Notario que, por su competencia territorial carezca de conexión razonable con alguno de los elementos personales o reales del negocio, tal como se pacta en la estipulación séptima.

d) La fecha máxima de entrega de la edificación será el día [FECHA], conforme a lo pactado en la estipulación sexta.

e) La edificación se divide en las siguientes fases, con las siguientes fechas de finalización: ()

f) Nombre y domicilio del Arquitecto: ()

g) Nombre o razón social y domicilio del constructor:()

DUODÉCIMA. NOTIFICACIONES

Toda notificación que se efectúe entre las partes se hará por escrito y será entregada personalmente o de cualquier otra forma que certifique la recepción por la parte notificada en los respectivos domicilios indicados en el encabezamiento de este contrato.

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

Y en prueba de conformidad de cuanto antecede, las partes firman y rubrican el presente contrato y sus Anexos I, II y III, a un solo efecto y por duplicado ejemplar, en todas sus hojas, en el lugar y fecha del encabezamiento.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

Fdo [NOMBRE Y APELLIDOS]: Fdo.:
