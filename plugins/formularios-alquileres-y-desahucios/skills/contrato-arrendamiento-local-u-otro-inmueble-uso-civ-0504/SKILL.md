---
name: contrato-arrendamiento-local-u-otro-inmueble-uso-civ-0504
description: "Contrato de arrendamiento de local u otro inmueble para uso distinto del de vivienda. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de arrendamiento de local u otro inmueble para uso distinto del de vivienda

> Formulario **CIV-0504** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 24-11-2026.

## Qué es

Contrato de arrendamiento para uso distinto al de vivienda, en el que se concretan las condiciones, estipulaciones y circunstancias para llevar a cabo el contrato, así como los derechos y obligaciones del arrendador y arrendatario.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de arrendamiento de local u otro inmueble para uso distinto del de vivienda» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de arrendamiento de local u otro inmueble para uso distinto del de vivienda” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:contrato-arrendamiento-local-u-otro-inmueble-uso-civ-0504`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (9 veces)
- [ ] LOCALIDAD (7 veces)
- [ ] DÍA (6 veces)
- [ ] IMPORTE (5 veces)
- [ ] MES (5 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] NÚMERO (4 veces)
- [ ] AÑO (3 veces)
- [ ] CALLE (3 veces)
- [ ] DIRECCIÓN A EFECTOS DE NOTIFICACIONES (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] ESTADO CIVIL (2 veces)
- [ ] PISO (2 veces)
- [ ] PUERTA (2 veces)
- [ ] ACTIVIDAD
- [ ] DENOMINACIÓN SOCIAL
- [ ] FECHAS
- [ ] FINCA
- [ ] FOLIO
- [ ] INSTITUCIÓN DE MEDIACIÓN
- [ ] LIBRO
- [ ] LUGAR
- [ ] MEDIO DE PAGO
- [ ] Nº DE FINCA
- [ ] PLAZO
- [ ] PROVINCIA
- [ ] REGLAMENTO DE LA INSTITUCIÓN ARBITRAL
- [ ] SUCURSAL
- [ ] TOMO

## Normas que cita el formulario

- No cita artículos concretos; Claude localizará las normas aplicables con Jurisprudenciator si el documento las necesita.

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

En [LUGAR], a [DÍA] de [MES] de [AÑO].

REUNIDOS

De una parte:

D [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número [NÚMERO]

De otra:

D [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número [NÚMERO]

[ELEGIR UNA OPCIÓN: Intervienen / En representación / Nombre propio]

Exponen

PRIMERO.- Que LA ARRENDADORA es propietaria en régimen de plena propiedad y dominio del local sito en [LOCALIDAD], calle [CALLE] número [NÚMERO] con una superficie de [Nº] metros cuadrados inscrito en el Registro de la Propiedad de [LOCALIDAD] en el Tomo [TOMO], Libro [LIBRO], Folio [FOLIO], Finca [Nº DE FINCA] e inscripción número [NÚMERO], en el que se desarrolla la actividad de

Que el mencionado local se encuentra libre de cargas y gravámenes y al corriente en el pago de impuestos.

SEGUNDO.- Que LA ARRENDATARIA se encuentra interesada en el arrendamiento del local descrito en el anterior Exponendo.

TERCERA.- Como quiera que ambas partes se encuentran interesadas en el arrendamiento del local supra referido, ambas partes de común acuerdo llevan a efecto el presente contrato con arreglo a las siguientes:

CLÁUSULAS

Objeto

Constituye el objeto del presente contrato el arrendamiento del local descrito en el Exponendo Primero para destinarlo a la actividad de [ACTIVIDAD].

[ELEGIR UNA OPCIÓN: Entrega / Con la firma / Con posterioridad]

Renta

Importe de la renta

El importe de la renta se concreta en la cantidad de [IMPORTE] euros mensuales ( €). El precio total de la operación asciende a la cantidad de [IMPORTE] euros ( €).

Dicha cantidad no incluye los impuestos, tasas, precios públicos y licencias, tanto municipales como estatales o autonómicas que recaigan sobre la actividad que se pretende desempeñar, ni los consumos de gas, electricidad, teléfono, agua así como cualquier otro impuesto, suministro o servicio que se generen. Los consumos que fueren abonados por los anteriores conceptos por LA ARRENDADORA serán pasados al cobro a LA ARRENDATARIA junto con la renta mensual.

Pago de la renta

El pago se efectuará entre los días [FECHAS] y [DÍA] de cada mes en la cuenta corriente núm. [Nº] que LA ARRENDADORA tiene suscrita con la entidad [DENOMINACIÓN SOCIAL] en su sucursal [SUCURSAL].

Retraso en el pago

El retraso en más de [Nº] días en cualquiera de los pagos dará derecho a LA ARRENDADORA a exigir a LA ARRENDATARIA un interés moratorio del % respecto de cada uno de los pagos no satisfechos puntualmente.

Actualización de la renta

Transcurrido el primer año de vigencia del presente contrato, la renta pactada será actualizada anualmente en función de la evolución anual experimentada por el Índice General de Precios al Consumo del Instituto Nacional de Estadística.

La renta actualizada será exigible a LA ARRENDATARIA a partir del mes siguiente a aquél en que LA ARRENDADORA se lo notifique por escrito, expresando el porcentaje de alteración aplicado. Se considerará valida la notificación hecha mediante anotación en el recibo de la mensualidad precedente.

Duración del contrato

El plazo de duración del arrendamiento será de [Nº] años, por lo que el presente contrato quedará extinguido y sin efecto alguno el día [DÍA] de [MES] de [AÑO], sin que ello genere a su término derecho o indemnización alguna para las partes.

Si terminado el contrato LA ARRENDADORA no notificase a LA ARRENDATARIA con una antelación mínima de 30 días con respecto a la fecha de vencimiento del contrato su intención de no prorrogar el contrato o no le requiriese al desalojo de la finca arrendada, procederá la prórroga de manera automática por plazo de [Nº] años si así lo desease LA ARRENDATARIA.

Al término de la prórroga inicial se aplicará en su caso el mismo sistema para los períodos sucesivos. No obstante, durante dichas prórrogas, así como durante el tiempo que transcurra hasta la devolución de la finca arrendada a LA ARRENDADORA será exigible por ésta la cantidad mensual que resultare de aplicar la actualización periódica pactada en la cláusula cuarta.

Indemnización al arrendatario

Derecho a la indemnización

La extinción por transcurso del término convencional del arrendamiento dará a LA ARRENDATARIA derecho a una indemnización a cargo de LA ARRENDADORA, siempre que A ARRENDATARIA haya manifestado con cuatro meses de antelación a la expiración del plazo su voluntad de renovar el contrato por un mínimo de cinco años más y por una renta de mercado. Se considerará renta de mercado la que al efecto acuerden las partes; en defecto de pacto, la que, al efecto determine el árbitro designado por las partes.

Cuantía de la indemnización

La cuantía de la indemnización se determinará en la forma siguiente:

1. Si LA ARRENDATARIA iniciara en el mismo municipio, dentro de los seis meses siguientes a la expiración del arrendamiento, el ejercicio de la misma actividad a la que viniera estando dedicada, la indemnización comprenderá los gastos del traslado y los perjuicios derivados de la pérdida de clientela ocurrida con respecto a la que tuviera en el local anterior, calculada con respecto a la habida durante los seis primeros meses de la nueva actividad.

2. Si LA ARRENDATARIA iniciara dentro de los seis meses siguientes a la extinción del arrendamiento una actividad diferente o no iniciara actividad alguna, y el arrendador o un tercero desarrollan en la finca dentro del mismo plazo la misma actividad o una afín a la desarrollada por el arrendatario, la indemnización será de una mensualidad por año de duración del contrato, con un máximo de dieciocho mensualidades.

Se considerarán afines las actividades típicamente aptas para beneficiarse, aunque sólo en parte de la clientela captada por la actividad que ejerció el arrendatario.

En caso de falta de acuerdo entre las partes sobre la cuantía de la indemnización, la misma será fijada por el árbitro designado por aquéllas.

Licencias, permisos y autorizaciones

LA ARRENDATARIA gestionará y sufragará a su exclusiva cuenta y cargo, todas las licencias, permisos, autorizaciones, obras de adecuación, etc., que la actividad descrita en la cláusula primera requiera, con independencia de que sean exigidos por la Administración Central, Autonómica o Local y cumplirá con todas aquellas disposiciones, ordenanzas o exigencias de cualquier autoridad y organismo competente que a tal fin le sean requeridos.

Obras necesarias

Durante el período de vigencia del presente contrato, los gastos de mantenimiento del local e instalaciones, reposición de elementos averiados, etc. serán de cargo exclusivo de LA ARRENDATARIA, quien deberá mantener el local e instalaciones en las condiciones óptimas de conservación y uso para el desempeño de la actividad.

LA ARRENDATARIA deberá permitir el acceso al local a LA ARRENDADORA y a los operarios o industriales mandados por ésta para la inspección y comprobación del estado del inmueble.

Si advirtiese riesgo de daños o mal estado de conservación en cualquier instalación general deberá ponerlo urgentemente en conocimiento de LA ARRENDADORA.

[ELEGIR UNA OPCIÓN: Obras útiles / No autorizadas / Autorizadas]

Fianza

LA ARRENDATARIA entrega en el acto de la firma de este contrato la cantidad de [IMPORTE] euros ( €), equivalente a dos mensualidades de renta, en concepto de fianza legal obligatoria.

La fianza le será devuelta a LA ARRENDATARIA en el plazo de [Nº] días contados a partir del momento de la devolución del local arrendado una vez cumplidas por LA ARRENDATARIA las obligaciones contraídas, a cuya responsabilidad queda afectada, así como al resarcimiento de daños y perjuicios, sirviendo este documento como formal carta de pago. Dicha fianza no devengará intereses.

Queda establecido que bajo ningún concepto LA ARRENDATARIA podrá canjear la finca depositada en este acto por ninguna mensualidad de alquiler, ni cualquier otro pago inherente al presente contrato de arrendamiento.

Fondo de garantía

Para garantizar la buena conservación del local e instalaciones, LA ARRENDADORA constituirá un fondo económico materializado en un Fondo de Inversión al que anualmente deberá realizarse una aportación de [IMPORTE] euros ( €), que se verificará, la primera antes de [DÍA] de [MES] de [AÑO], las siguientes antes de [DÍA] de [MES] de cada año de vigencia del contrato, hasta la última que tendrá lugar antes de [DÍA] de [MES], según aparece en el siguiente cuadro:

En ningún caso podrá ser considerada la plusvalía que pudiera generarse en el fondo como parte de la aportación, ya e esta plusvalía refuerza la garantía expresada al principio de esta cláusula.

LA ARRENDATARIA no podrá disponer de este fondo sin la autorización de LA ARRENDADORA, por lo que se constituirá con firma mancomunada de ambas.

Al término de este contrato serán con cargo al Fondo las reparaciones necesarias para dejar el local e instalaciones en perfectas condiciones de uso y conservación, quedando el remanente, si lo hubiera, de libre disposición por LA ARRENDATARIA y siempre que no hubiese ningún débito por parte de ésta a LA ARRENDADORA. De no ser así, la cantidad que quedase de remanente se emplearía como parte del pago.

Autorización de subarriendo o traspaso

LA ARRENDATARIA podrá subarrendar la finca o ceder el contrato de arrendamiento sin necesidad de contar con el consentimiento de LA ARRENDADORA, teniendo ésta derecho a una elevación de la renta del % en el supuesto de producirse el subarriendo parcial y del % en el supuesto de producirse la cesión del contrato.

Tanto la cesión como el subarriendo deberá notificarse de forma fehaciente a LA ARRENDADORA en el plazo de un mes desde que aquéllos se hubieran concertado.

Renuncia al derecho de adquisición preferente

LA ARRENDATARIA renuncia al derecho de adquisición preferente prevenido en el artículo 31 de la Ley de Arrendamientos Urbanos.

Seguro

LA ARRENDATARIA contratará un seguro que resulte satisfactorio para LA ARRENDADORA y que cubra el riesgo de daños o pérdida que pueda sufrir el local comercial durante todo el período de vigencia del presente contrato.

LA ARRENDATARIA proporcionará a LA ARRENDADORA, a su solicitud, pruebas de la existencia de dicho seguro. La cobertura incluirá, entre otros aspectos, los daños provocados por incendios, agua, fenómenos naturales y robo.

Resolución del contrato

El incumplimiento de las obligaciones que resulten del presente contrato facultará a la parte que cumpla los suyos a exigir a la otra su cumplimiento, o, a su elección, a resolver el contrato, con abono en ambos casos de la indemnización por daños y perjuicios que proceda.

Opción de compra

LA ARRENDADORA concede gratuitamente a LA ARRENDATARIA durante la vigencia de este contrato un derecho de opción de compra del local arrendado por un precio de [IMPORTE] euros ( €), del cual se deducirán las cantidades abonadas en concepto de renta por LA ARRENDATARIA hasta el momento en que haga uso de la opción de compra.

Dicho precio se abonará en [MEDIO DE PAGO] en el momento de hacer uso de la opción y el negocio se transmitirá libre de cargas y gravámenes y al corriente en el pago de impuestos.

Gastos e impuestos

Todos los gastos e impuestos que se originen como consecuencia de la formalización, cumplimiento o extinción del presente contrato y de las obligaciones que de él se deriven serán de cargo de la parte

Igualmente, los gastos judiciales que se ocasionen por incumplimiento del presente contrato serán por cuenta de la parte incumplidora, incluidos honorarios del Procurador y Abogado aunque sus intervenciones no fueran preceptivas.

Sumisión a mediación y/o arbitraje; Jurisdicción competente y ley aplicable

Las partes contratantes acuerdan libre y voluntariamente que todas las desavenencias, divergencias o cuestiones litigiosas que deriven de este contrato, incluso cuando la controversia verse sobre la validez o existencia del presente contrato, se resolverán a través de la Mediación de [INSTITUCIÓN DE MEDIACIÓN], antes de acudir a la jurisdicción o a otra solución extrajudicial de conflictos, sometiéndose a la regulación establecida en la Ley 5/2012, de 6 de julio, y (caso de fijar un plazo máximo [PLAZO]) fijando un plazo máximo de duración del procedimiento de sesenta días desde la solicitud de iniciación por cualquiera de las partes.

A falta de resolución de la controversia en el procedimiento de mediación, la misma será definitivamente resuelta mediante Arbitraje de la Corte de [LOCALIDAD], a la que se encomienda la administración del arbitraje y la designación de los árbitros, de acuerdo con su reglamento [REGLAMENTO DE LA INSTITUCIÓN ARBITRAL].

El conocimiento de los litigios relativos a que diera lugar la interpretación y/o ejecución del presente contrato corresponderá al Juez de Primera Instancia del lugar en que se halle la finca [FINCA].

El presente contrato tiene carácter civil, se regirá por sus propias cláusulas, y en lo en ellas no dispuesto, por lo previsto en el Título III de la Ley de Arrendamientos Urbanos de 24 de Noviembre de 1.994 y, supletoriamente, por lo dispuesto en el Código Civil.

Notificaciones

A efectos de notificaciones o emplazamientos judiciales, y en general, toda comunicación o requerimiento que hayan de oír las partes en relación con el presente contrato, se tomará como domicilio del arrendador el señalado al inicio del presente contrato, es decir, calle [CALLE], núm. [Nº], piso [PISO], puerta [PUERTA], de la localidad/ciudad de [LOCALIDAD], provincia de [PROVINCIA], y como domicilio del arrendatario, el de la calle [CALLE], núm. [Nº], piso [PISO], puerta [PUERTA], de la localidad/ciudad de [LOCALIDAD], provincia de

De conformidad a lo dispuesto en el artículo 4.6 de la Ley de Arrendamientos Urbanos, las partes designan las siguientes direcciones electrónicas para realizar las notificaciones:

- Por el arrendador [DIRECCIÓN A EFECTOS DE NOTIFICACIONES]

- Por el arrendatario [DIRECCIÓN A EFECTOS DE NOTIFICACIONES]

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

Generalidades

El presente contrato anula y reemplaza cualquier contrato o acuerdo anterior entre las partes con el mismo objeto y sólo podrá ser modificado por un nuevo acuerdo firmado por ambas partes.

Si alguna de las cláusulas del presente contrato fuere declarada nula o inaplicable, dicha cláusula se considerará excluida del contrato, sin que implique la nulidad del mismo. En este caso las partes harán cuanto esté a su alcance para encontrar una solución equivalente que sea válida y que refleje debidamente sus intenciones.

Los encabezamientos de las distintas cláusulas lo son sólo a efectos informativos, y no afectarán, calificarán o ampliarán la interpretación de este Contrato.

Y en prueba de conformidad y aceptación de cuanto antecede, ambas partes firman los [Nº] folios del presente CONTRATO DE ARRENDAMIENTO PARA USO DISTINTO DE VIVIENDA, extendido por duplicado y a un solo efecto, en la ciudad y fecha mencionados en el encabezamiento.

Fdo. Don [NOMBRE Y APELLIDOS]

(La Arrendadora)

Fdo. Don [NOMBRE Y APELLIDOS]

(La Arrendataria)

========================================================================
