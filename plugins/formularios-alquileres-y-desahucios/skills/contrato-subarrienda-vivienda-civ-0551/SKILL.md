---
name: contrato-subarrienda-vivienda-civ-0551
description: "Contrato por el que se subarrienda una vivienda. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato por el que se subarrienda una vivienda

> Formulario **CIV-0551** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato por el que se subarrienda una vivienda» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato por el que se subarrienda una vivienda” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:contrato-subarrienda-vivienda-civ-0551`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (7 veces)
- [ ] Nº (7 veces)
- [ ] DÍA (6 veces)
- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] NÚMERO (5 veces)
- [ ] IMPORTE (4 veces)
- [ ] MES (4 veces)
- [ ] CALLE (3 veces)
- [ ] AÑO (2 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] DIRECCIÓN ELECTRÓNICA (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] ESTADO CIVIL (2 veces)
- [ ] FECHAS (2 veces)
- [ ] PISO (2 veces)
- [ ] PUERTA (2 veces)
- [ ] SUCURSAL (2 veces)
- [ ] FOLIO
- [ ] INSTITUCIÓN DE MEDIACIÓN
- [ ] LIBRO
- [ ] LUGAR
- [ ] Nº DE FINCA
- [ ] PROVINCIA
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

PRIMERO.- Que LA SUBARRENDADORA es arrendataria de la vivienda sita en [LOCALIDAD], calle [CALLE] número [NÚMERO] con una superficie de metros cuadrados inscrito en el Registro de la Propiedad de [LOCALIDAD] en el Tomo [TOMO], Libro [LIBRO], Folio [FOLIO], Finca [Nº DE FINCA] e inscripción número [NÚMERO] y está autorizada a subarrendar el inmueble al haber prestado su consentimiento el arrendador.

Se adjunta copia de dicho contrato como anexo I.

SEGUNDO.- Que LA SUBARRENDATARIA se encuentra interesada en el subarrendamiento parcial de la vivienda descrita en el anterior Exponendo.

TERCERA.- Como quiera que ambas partes se encuentran interesadas en el subarrendamiento de la vivienda supra referido, ambas partes de común acuerdo llevan a efecto el presente contrato con arreglo a las siguientes:

CLÁUSULAS

[ELEGIR UNA OPCIÓN: Objeto / No amueblado / Amueblado / — y además elegir: Entrega / Con la firma / Con posterioridad]

Renta

Importe de la renta

El importe de la renta se concreta en la cantidad de [IMPORTE] euros mensuales ( €). De conformidad con lo convenido con la propiedad la renta se ha aumentado en un %.

Dicha cantidad no incluye los consumos de gas, electricidad, teléfono, agua así como cualquier otro impuesto, suministro o servicio que se generen. Los consumos que fueren abonados por los anteriores conceptos por LA SUBARRENDADORA serán pasados al cobro a LA SUBARRENDATARIA junto con la renta mensual.

Pago de la renta

De conformidad con lo convenido con la propiedad del inmueble, LA SUBARRENDATARIA retendrá la suma de [IMPORTE] euros ( €), para su entrega a la propiedad mediante ingreso que se efectuará entre los días [FECHAS] y [DÍA] de cada mes en la cuenta corriente núm. [Nº] que la propiedad tiene suscrita con la entidad [DENOMINACIÓN SOCIAL] en su sucursal [SUCURSAL].

El pago de las cantidades restantes se efectuará entre los días [FECHAS] y [DÍA] de cada mes en la cuenta corriente núm. [Nº] que LA SUBARRENDADORA tiene suscrita con la entidad [DENOMINACIÓN SOCIAL] en su sucursal [SUCURSAL].

Retraso en el pago

El retraso en más de [Nº] días en cualquiera de los pagos dará derecho a LA SUBARRENDADORA a exigir a LA SUBARRENDATARIA un interés moratorio del % respecto de cada uno de los pagos no satisfechos puntualmente.

Actualización de la renta

Transcurrido el primer año de vigencia del presente contrato, la renta pactada será actualizada anualmente en función de la evolución anual experimentada por el Índice General de Precios al Consumo del Instituto Nacional de Estadística.

La renta actualizada será exigible a LA SUBARRENDATARIA a partir del mes siguiente a aquél en que LA SUBARRENDADORA se lo notifique por escrito, expresando el porcentaje de alteración aplicado. Se considerará valida la notificación hecha mediante anotación en el recibo de la mensualidad precedente.

[ELEGIR UNA OPCIÓN: Duración del contrato / Con prórroga / Sin prórroga]

Avalista

D. [NOMBRE Y APELLIDOS], provisto de D.N.I. número [NÚMERO] y presente en este acto, se constituye en fiador o avalista de las obligaciones contraídas por LA SUBARRENDATARIA con LA SUBARRENDADORA, obligándose solidariamente con LA SUBARRENDATARIA al cumplimiento de las obligaciones arrendaticias y especialmente al pago de la renta, así como a cualquier cantidad económica que se derive del presente contrato o por disposición legal, y a la conservación del buen estado de la vivienda por toda la duración del contrato, con renuncia expresa a los beneficios de excusión, división.

A tal efecto, acepta de antemano cualquier prórroga o renovación que LA SUBARRENDADORA pudiera conceder, sea cual sea la forma en que se instrumente la misma, sin que, en consecuencia, la concesión de la indicada prórroga o renovación pueda producir los efectos establecidos en el artículo 1.851 del Código Civil.

Conservación y mantenimiento

Obras necesarias

Durante el período de vigencia del presente contrato, los gastos de mantenimiento del local e instalaciones, reposición de elementos averiados, etc. serán de cargo exclusivo de LA SUBARRENDATARIA, quien deberá mantener el local e instalaciones en las condiciones óptimas de conservación y uso para el desempeño de la actividad.

LA SUBARRENDATARIA deberá permitir el acceso al local de negocio a LA SUBARRENDADORA y a la Propiedad para la inspección y comprobación del estado del inmueble.

Si advirtiese riesgo de daños o mal estado de conservación en cualquier instalación general deberá ponerlo urgentemente en conocimiento de LA SUBARRENDADORA.

Obras útiles

LA SUBARRENDATARIA no podrá realizar sin el consentimiento escrito de LA SUBARRENDADORA y de la Propiedad obras de ninguna clase que no sean las de mera conservación y mantenimiento.

Fianza

LA SUBARRENDATARIA entrega en el acto de la firma de este contrato la cantidad de [IMPORTE] euros ( €), equivalente a dos mensualidades de renta, en concepto de fianza legal obligatoria.

La fianza le será devuelta a LA ARRENDATARIA en el plazo de [Nº] días contados a partir del momento de la devolución del local arrendado una vez cumplidas por LA SUBARRENDATARIA las obligaciones contraídas, a cuya responsabilidad queda afectada, así como al resarcimiento de daños y perjuicios, sirviendo este documento como formal carta de pago. Dicha fianza no devengará intereses.

Queda establecido que bajo ningún concepto LA SUBARRENDATARIA podrá canjear la finca depositada en este acto por ninguna mensualidad de alquiler, ni cualquier otro pago inherente al presente contrato de arrendamiento.

Fondo de garantía

Para garantizar la buena conservación del inmueble, LA SUBARRENDADORA constituirá un fondo económico materializado en un Fondo de Inversión al que anualmente deberá realizarse una aportación de [IMPORTE] euros ( €), que se verificará, la primera antes de [DÍA] de [MES] de [AÑO], las siguientes antes de [DÍA] de [MES] de cada año de vigencia del contrato, hasta la última que tendrá lugar antes de [DÍA] de [MES], según aparece en el siguiente cuadro:

En ningún caso podrá ser considerada la plusvalía que pudiera generarse en el fondo como parte de la aportación, ya e esta plusvalía refuerza la garantía expresada al principio de esta cláusula.

LA SUBARRENDATARIA no podrá disponer de este fondo sin la autorización de LA SUBARRENDADORA, por lo que se constituirá con firma mancomunada de ambas.

Al término de este contrato serán con cargo al Fondo las reparaciones necesarias para dejar la vivienda en perfectas condiciones de uso y conservación, quedando el remanente, si lo hubiera, de libre disposición por LA SUBARRENDATARIA y siempre que no hubiese ningún débito por parte de ésta a LA SUBARRENDADORA. De no ser así, la cantidad que quedase de remanente se emplearía como parte del pago.

Prohibición de subarriendo o traspaso

LA SUBARRENDATARIA no podrá subarrendar la finca o ceder el contrato de arrendamiento.

Seguro

LA SUBARRENDATARIA contratará un seguro que resulte satisfactorio para LA SUBARRENDADORA y que cubra el riesgo de daños o pérdida que pueda sufrir la vivienda durante todo el período de vigencia del presente contrato.

LA SUBARRENDATARIA proporcionará a LA SUBARRENDADORA, a su solicitud, pruebas de la existencia de dicho seguro. La cobertura incluirá, entre otros aspectos, los daños provocados por incendios, agua, fenómenos naturales y robo.

Resolución del contrato

El incumplimiento de las obligaciones que resulten del presente contrato facultará a la parte que cumpla los suyos a exigir a la otra su cumplimiento, o, a su elección, a resolver el contrato, con abono en ambos casos de la indemnización por daños y perjuicios que proceda.

Gastos e impuestos

Todos los gastos e impuestos que se originen como consecuencia de la formalización, cumplimiento o extinción del presente contrato y de las obligaciones que de él se deriven serán de cargo de la parte

Igualmente, los gastos judiciales que se ocasionen por incumplimiento del presente contrato serán por cuenta de la parte incumplidora, incluidos honorarios del Procurador y Abogado aunque sus intervenciones no fueran preceptivas.

Sumisión a mediación y/o arbitraje; Jurisdicción competente y ley aplicable

Las partes contratantes acuerdan libre y voluntariamente que todas las desavenencias, divergencias o cuestiones litigiosas que deriven de este contrato, incluso cuando la controversia verse sobre la validez o existencia del presente contrato, se resolverán a través de la Mediación de [INSTITUCIÓN DE MEDIACIÓN], antes de acudir a la jurisdicción o a otra solución extrajudicial de conflictos, sometiéndose a la regulación establecida en la Ley 5/2012, de 6 de julio, y (caso de fijar un plazo máximo) fijando un plazo máximo de duración del procedimiento de sesenta días desde la solicitud de iniciación por cualquiera de las partes.

A falta de resolución de la controversia en el procedimiento de mediación, la misma será definitivamente resuelta mediante Arbitraje de la Corte de [LOCALIDAD], a la que se encomienda la administración del arbitraje y la designación de los árbitros, de acuerdo con su reglamento.

El conocimiento de los litigios relativos a que diera lugar la interpretación y/o ejecución del presente contrato corresponderá al Juez de Primera Instancia del lugar en que se halle la finca.

El presente contrato tiene carácter civil, se regirá por sus propias cláusulas, y en lo en ellas no dispuesto, por lo previsto en la Ley de Arrendamientos Urbanos de 24 de Noviembre de 1.994.

Notificaciones

A efectos de notificaciones o emplazamientos judiciales, y en general, toda comunicación o requerimiento que hayan de oír las partes en relación con el presente contrato, se tomará como domicilio del subarrendador el señalado al inicio del presente contrato, es decir, calle [CALLE], núm. [Nº], piso [PISO], puerta [PUERTA], de la localidad/ciudad de [LOCALIDAD], provincia de [PROVINCIA], y como domicilio del subarrendatario, el de la calle [CALLE], núm. [Nº], piso [PISO], puerta [PUERTA], de la localidad/ciudad de [LOCALIDAD], provincia de

De conformidad a lo dispuesto en el artículo 4.6 de la Ley de Arrendamientos Urbanos, las partes designan las siguientes direcciones electrónicas para realizar las notificaciones:

- Por el subarrendador [DIRECCIÓN ELECTRÓNICA]

- Por el subarrendatario [DIRECCIÓN ELECTRÓNICA]

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

Generalidades

El presente contrato anula y reemplaza cualquier contrato o acuerdo anterior entre las partes con el mismo objeto y sólo podrá ser modificado por un nuevo acuerdo firmado por ambas partes.

Si alguna de las cláusulas del presente contrato fuere declarada nula o inaplicable, dicha cláusula se considerará excluida del contrato, sin que implique la nulidad del mismo. En este caso las partes harán cuanto esté a su alcance para encontrar una solución equivalente que sea válida y que refleje debidamente sus intenciones.

Los encabezamientos de las distintas cláusulas lo son sólo a efectos informativos, y no afectarán, calificarán o ampliarán la interpretación de este Contrato.

Y en prueba de conformidad y aceptación de cuanto antecede, ambas partes firman los [Nº] folios del presente CONTRATO DE SUBARRIENDO DE VIVIENDA, extendido por duplicado y a un solo efecto, en la ciudad y fecha mencionados en el encabezamiento.

Fdo. Don [NOMBRE Y APELLIDOS]

(La SUBARRENDADORA)

Fdo. Don [NOMBRE Y APELLIDOS]

(La SUBARRENDATARIA)

========================================================================
