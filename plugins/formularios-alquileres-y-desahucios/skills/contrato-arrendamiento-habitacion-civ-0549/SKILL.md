---
name: contrato-arrendamiento-habitacion-civ-0549
description: "Contrato de arrendamiento de una habitación. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de arrendamiento de una habitación

> Formulario **CIV-0549** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 24-11-2026.

## Qué es

Modelo de contrato de arrendamiento por el que se cede el uso de una habitación dentro de la vivienda a cambio de un precio, incluyendo las condiciones, estipulaciones y circunstancias necesarias para llevar a cabo el arrendamiento, así como los derechos y obligaciones de las partes..

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de arrendamiento de una habitación» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de arrendamiento de una habitación” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:contrato-arrendamiento-habitacion-civ-0549`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] Nº (5 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] NÚMERO (4 veces)
- [ ] IMPORTE (3 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] ESTADO CIVIL (2 veces)
- [ ] CALLE
- [ ] DIRECCIÓN
- [ ] DÍA
- [ ] FECHA
- [ ] FECHAS
- [ ] FOLIO
- [ ] LIBRO
- [ ] LUGAR
- [ ] MEDIO DE PAGO
- [ ] Nº DE FINCA
- [ ] NÚMERO DE HABITACIONES
- [ ] SUCURSAL
- [ ] TOMO

## Normas que cita el formulario

- art. 1.851 Código Civil

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

Modelo de contrato de arrendamiento por el que se cede el uso de una habitación dentro de la vivienda a cambio de un precio, incluyendo las condiciones, estipulaciones y circunstancias necesarias para llevar a cabo el arrendamiento, así como los derechos y obligaciones de las partes..


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

De una parte:

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número

De otra:

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número

Intervienen

[ELEGIR UNA OPCIÓN: En representación / Nombre propio]

Todas las partes, en el respectivo carácter con el que intervienen, se reconocen mutuamente la capacidad legal en Derecho necesaria para concertar el presente CONTRATO DE ARRENDAMIENTO DE HABITACIÓN, y a tal efecto, libremente y de común acuerdo,

Exponen

Primero.– Que LA ARRENDADORA es propietaria en régimen de plena propiedad y dominio de la vivienda sita en [LOCALIDAD], calle [CALLE] número [NÚMERO] con una superficie de metros cuadrados inscrito en el Registro de la Propiedad de [LOCALIDAD] en el Tomo [TOMO], Libro [LIBRO], Folio [FOLIO], Finca [Nº DE FINCA] e inscripción número [NÚMERO].

Que la mencionada vivienda se encuentra dividida en [NÚMERO DE HABITACIONES] habitaciones de uso privativo, baño, vestíbulo, pasillo y cocina de uso compartido con el resto de los inquilinos,

Que la mencionada vivienda se encuentra libre de cargas y gravámenes y al corriente en el pago de impuestos.

Segundo.– Que LA ARRENDATARIA se encuentra interesada en el arrendamiento de la habitación número [NÚMERO] situada en [DIRECCIÓN] de la vivienda descrita en el anterior Exponendo.

Tercera.– Como quiera que ambas partes se encuentran interesadas en el arrendamiento de la habitación supra referido, ambas partes de común acuerdo llevan a efecto el presente contrato con arreglo a las siguientes:

Cláusulas

Objeto.–

[ELEGIR UNA OPCIÓN: No amueblada / Amueblada]

Entrega.–

[ELEGIR UNA OPCIÓN: Con la firma / Con posterioridad]

Renta.–

– Importe de la renta

El importe de la renta se concreta en la cantidad de [IMPORTE] euros mensuales ( €).

Dicha cantidad no incluye los consumos de gas, electricidad, teléfono, agua así como cualquier otro impuesto, suministro o servicio que se generen. Los consumos que fueren abonados por los anteriores conceptos por LA ARRENDADORA serán pasados al cobro a LA ARRENDATARIA junto con la renta mensual en las proporciones que a continuación se especificarán.

– Pago de la renta
El pago se efectuará entre los días [FECHAS] y [DÍA] de cada mes en la cuenta corriente núm. [Nº] que LA ARRENDADORA tiene suscrita con la entidad [DENOMINACIÓN SOCIAL] en su sucursal [SUCURSAL].
– Retraso en el pago

El retraso en más de [Nº] días en cualquiera de los pagos dará derecho a LA ARRENDADORA a exigir a LA ARRENDATARIA un interés moratorio del % respecto de cada uno de los pagos no satisfechos puntualmente, sin perjuicio de la facultad de resolver el contrato si concurren las circunstancias legales para ello.

Actualización de la renta.–

Transcurrido el primer año de vigencia del presente contrato, la renta pactada será actualizada anualmente en función de la evolución anual experimentada por el Índice General de Precios al Consumo del Instituto Nacional de Estadística.

La renta actualizada será exigible a LA ARRENDATARIA a partir del mes siguiente a aquél en que LA ARRENDADORA se lo notifique por escrito, expresando el porcentaje de alteración aplicado. Se considerará valida la notificación hecha mediante anotación en el recibo de la mensualidad precedente.

Duración del contrato.–

El presente arrendamiento se conviene y concierta por plazo de un año, a contar desde la celebración del presente contrato. Llegado el día del vencimiento del contrato, el mismo se prorrogará por plazos anuales hasta un máximo de cuatro, salvo que cualquiera de las partes manifieste a la contraria con [Nº] días de antelación como mínimo a la fecha de terminación del contrato, su voluntad de no renovarlo.

Una vez hayan transcurrido los cinco años, si ninguna de las partes comunica a la otra su deseo de forma expresa de rescindirlo, quedará automáticamente renovado por períodos sucesivos de un año.

Avalista/Fiador.–

D. [NOMBRE Y APELLIDOS], provisto de D.N.I. número [NÚMERO] y presente en este acto, se constituye en fiador/avalista de las obligaciones contraídas por LA ARRENDATARIA con LA ARRENDADORA, obligándose solidariamente con LA ARRENDATARIA al cumplimiento de las obligaciones arrendaticias y especialmente al pago de la renta, así como a cualquier cantidad económica que se derive del presente contrato o por disposición legal, y a la conservación del buen estado de la vivienda por toda la duración del contrato, con renuncia expresa a los beneficios de excusión, división.

A tal efecto, acepta de antemano cualquier prórroga o renovación que LA ARRENDADORA pudiera conceder, sea cual sea la forma en que se instrumente la misma, sin que, en consecuencia, la concesión de la indicada prórroga o renovación pueda producir los efectos establecidos en el artículo 1.851 del Código Civil.

Obras necesarias.–

[ELEGIR UNA OPCIÓN: Del arrendador / Del arrendatario]

Obras útiles.–

[ELEGIR UNA OPCIÓN: No autorizadas / Autorizadas]

Fianza.–

LA ARRENDATARIA entrega en el acto de la firma de este contrato la cantidad de [IMPORTE] euros ( €), equivalente a una mensualidad de renta, en concepto de fianza legal obligatoria.

La fianza le será devuelta a LA ARRENDATARIA en el plazo de [Nº] días contados a partir del momento de la devolución de la habitación arrendada una vez cumplidas por LA ARRENDATARIA las obligaciones contraídas, a cuya responsabilidad queda afectada, así como al resarcimiento de daños y perjuicios, sirviendo este documento como formal carta de pago. Dicha fianza no devengará intereses.

Queda establecido que bajo ningún concepto LA ARRENDATARIA podrá canjear la fianza depositada en este acto por ninguna mensualidad de alquiler, ni cualquier otro pago inherente al presente contrato de arrendamiento.

Contribución a los gastos comunes.–

Además de la renta pactada, serán por cuenta de LA ARRENDATARIA una cuota fija de gastos del %, estimada en proporción al área de vivienda alquilada, y convenida por ambas partes, en concepto de gastos generales para el adecuado sostenimiento de la finca, así como sus servicios, tributos, cargas y responsabilidades que no sean susceptibles de individualización y que corresponden a la vivienda y a sus accesorios, y en concepto de gastos de suministros de electricidad, gas y agua.

El pago de estos gastos se realizará en la forma pactada para el pago de la renta. EL ARRENDATARIO podrá contratar con las compañías telefónicas el suministro telefónico individualizado, siendo de su exclusivo cargo los gastos por dicho suministro

Autorización de subarriendo o traspaso.–

LA ARRENDATARIA podrá subarrendar la habitación o ceder el contrato de arrendamiento sin necesidad de contar con el consentimiento de LA ARRENDADORA, teniendo ésta derecho a una elevación de la renta del % en el supuesto de producirse la cesión del contrato.

Tanto la cesión como el subarriendo deberán notificarse de forma fehaciente a LA ARRENDADORA en el plazo de un mes desde que aquéllos se hubieran concertado.

Seguro.–

LA ARRENDATARIA, junto con el resto de los inquilinos, cada uno de en proporción a la participación que tienen asignada en los gastos comunes, contratarán un seguro que resulte satisfactorio para LA ARRENDADORA y que cubra el riesgo de daños o pérdida que pueda sufrir la vivienda durante todo el período de vigencia del presente contrato.

Honorarios del mediador inmobiliario.–

En este arrendamiento ha intervenido como mediador la entidad [DENOMINACIÓN SOCIAL].

Mediante el presente contrato se fijan los honorarios por la intervención de la referida entidad en el % de la renta de un año.

El precio fijado se pagará por la parte arrendadora y por la arrendataria por mitad e iguales partes.

Resolución del contrato.–

El incumplimiento de las obligaciones que resulten del presente contrato facultará a la parte que cumpla los suyos a exigir a la otra su cumplimiento, o, a su elección, a resolver el contrato, con abono en ambos casos de la indemnización por daños y perjuicios que proceda.

Opción de compra.–

LA ARRENDADORA concede gratuitamente a LA ARRENDATARIA durante la vigencia de este contrato un derecho de opción de compra del inmueble arrendado por un precio de [IMPORTE] euros ( €), del cual se deducirán las cantidades abonadas en concepto de renta por LA ARRENDATARIA hasta el momento en que haga uso de la opción de compra.

Dicho precio se abonará en [MEDIO DE PAGO] en el momento de hacer uso de la opción y el negocio se transmitirá libre de cargas y gravámenes y al corriente en el pago de impuestos.

Gastos e impuestos.–

Todos los gastos e impuestos que se originen como consecuencia de la formalización, cumplimiento o extinción del presente contrato y de las obligaciones que de él se deriven serán de cargo de la parte

Igualmente, los gastos judiciales que se ocasionen por incumplimiento del presente contrato serán por cuenta de la parte incumplidora, incluidos honorarios del Procurador y Abogado aunque sus intervenciones no fueran preceptivas.

Jurisdicción competente y ley aplicable.–

El conocimiento de los litigios relativos a que diera lugar la interpretación y/o ejecución del presente contrato corresponderá al Juez de Primera Instancia del lugar en que se halle la finca.

El presente contrato tiene carácter civil, se regirá por sus propias cláusulas, y en lo en ellas no dispuesto, por lo previsto en el Código Civil y demás leyes especiales.

Notificaciones.–

Toda notificación que se efectúe entre las partes se hará por escrito y será entregada personalmente o de cualquier otra forma que certifique la recepción por la parte notificada en los respectivos domicilios indicados en el encabezamiento de este Contrato.

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

Generalidades.–

El presente contrato anula y reemplaza cualquier contrato o acuerdo anterior entre las partes con el mismo objeto y sólo podrá ser modificado por un nuevo acuerdo firmado por ambas partes.

Si alguna de las cláusulas del presente contrato fuere declarada nula o inaplicable, dicha cláusula se considerará excluida del contrato, sin que implique la nulidad del mismo. En este caso las partes harán cuanto esté a su alcance para encontrar una solución equivalente que sea válida y que refleje debidamente sus intenciones.

Los encabezamientos de las distintas cláusulas lo son sólo a efectos informativos, y no afectarán, calificarán o ampliarán la interpretación de este Contrato.

Y en prueba de conformidad y aceptación de cuanto antecede, ambas partes firman los [Nº] folios del presente CONTRATO DE ARRENDAMIENTO DE HABITACIÓN, extendido por duplicado y a un solo efecto, en la ciudad y fecha mencionados en el encabezamiento.

Parte arrendadora	Parte arrendataria

Fdo. D./Dña. [NOMBRE Y APELLIDOS]: Fdo. D./Dña. [NOMBRE Y APELLIDOS]:

========================================================================
