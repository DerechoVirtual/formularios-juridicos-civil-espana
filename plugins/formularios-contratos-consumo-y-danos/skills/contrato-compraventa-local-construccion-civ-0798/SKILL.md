---
name: contrato-compraventa-local-construccion-civ-0798
description: "Contrato de compraventa de un local en construcción. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de compraventa de un local en construcción

> Formulario **CIV-0798** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de compraventa de un local en construcción» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de compraventa de un local en construcción” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:contrato-compraventa-local-construccion-civ-0798`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] AÑO (5 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] MES (5 veces)
- [ ] Nº (4 veces)
- [ ] DÍA (3 veces)
- [ ] FECHA (3 veces)
- [ ] IMPORTE (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] CALLE (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] ENTIDAD BANCARIA (2 veces)
- [ ] ESTADO CIVIL (2 veces)
- [ ] ACTIVIDAD
- [ ] COLEGIO
- [ ] DENOMINACIÓN SOCIAL
- [ ] LUGAR
- [ ] NOMBRE DE LA PARTE
- [ ] OBJETO DE LA OBRA
- [ ] OTROS DATOS
- [ ] PORCENTAJE
- [ ] SUCURSAL

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

PRIMERO.- Que LA VENDEDORA-PROMOTORA es una mercantil dedicada a [ACTIVIDAD] que va a realizar una promoción de viviendas y locales en [LOCALIDAD] en la calle [CALLE], número

SEGUNDO.- Que LA COMPRADORA está interesado en la adquisición de un local en dicha promoción.

TERCERA.- Como quiera que ambas partes se encuentren interesadas en ello, ambas partes de común acuerdo llevan a efecto el presente contrato con arreglo a las siguientes:

CLÁUSULAS

Objeto

En virtud del presente Contrato, LA VENDEDORA-PROMOTORA vende a LA COMPRADORA que compra el local en construcción cuya descripción se encuentra en el Anexo I al presente Contrato.

Dicho local forma parte del solar descrito en el Anexo II al presente Contrato.

El Comprador adquiere, además de la propiedad del local, la copropiedad de los elementos comunes, participando en los gastos de conservación, limpieza u otros afines, de manera proporcional a su participación en el total del edificio o conjunto residencial en el que se halla, que es del [PORCENTAJE] (número % según consta en la escritura de declaración de obra nueva en construcción y de constitución del régimen de propiedad horizontal, que se adjunta como Anexo III al presente Contrato, junto con certificación registral en la que constan las cuotas de participación en los elementos comunes.

Construcción del local

Descripción del proceso de construcción

LA VENDEDORA-PROMOTORA ha iniciado la ejecución de una obra sobre el solar descrito en el Exponiendo Primero del presente Contrato.

La obra a ejecutar consiste en la construcción de [OBJETO DE LA OBRA], de acuerdo con el proyecto redactado por el arquitecto D. [NOMBRE Y APELLIDOS], compuesto por Memoria, Planos, Pliego de Condiciones y Capítulo de Mediciones, debidamente visados por los organismos procedentes, contando para ello con la preceptiva Licencia de edificación expedida por el Excelentísimo Ayuntamiento de [LOCALIDAD] de [DÍA] de [MES] de [AÑO], adjuntándose copia de cada documento en Anexo II.

La Obra será ejecutada bajo la dirección del Arquitecto del Ilustre Colegio de [COLEGIO] y Director de las obras D. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], en la calle [CALLE], número

Modificaciones del proyecto inicial

La modificación de los proyectos básico y de ejecución autorizados por la Administración competente precisará la expresa autorización de ésta.

Cualquier modificación o alteración de los proyectos básicos o de ejecución, salvo que sea consentida expresamente por todos los compradores o que sea técnicamente imprescindible para la viabilidad de la ejecución de las obras, deberá ser expresamente notificada por escrito a LA COMPRADORA con siete días de antelación al otorgamiento de la escritura pública de compraventa.

Salvo que sean consentidas expresamente por todos los compradores, o por aquellos directamente afectados, o que sean técnicamente imprescindibles para la viabilidad de la ejecución de las obras, las modificaciones de los proyectos técnicos no podrán consistir en la supresión de servicios previstos, la imposición de nuevas cargas o gravámenes, la alteración de la distribución de espacios en elementos de aprovechamiento común o privativo, la creación de nuevos espacios constructivos, el cambio de naturaleza jurídica de algunos de los ya configurados o la constitución de ámbitos de comunidad distintos de los contemplados en el proyecto técnico de obra, con edificios con los que se forme un complejo inmobiliario.

Cuando se trate de modificaciones de fuerza mayor o técnicamente imprescindibles para la viabilidad de la ejecución de las obras, deberán ir obligatoriamente avaladas con el informe técnico de la dirección facultativa de obra justificando la necesidad de los citados cambios.

Precio

El precio de la venta del local descrito en el Anexo I se concreta en la cantidad de [IMPORTE] euros (€).

El Precio establecido en el presente Contrato incluye los impuestos indirectos que según la legislación vigente son aplicables.

Forma de pago

El pago del Precio se realizará de la siguiente forma:

a) En este acto LA COMPRADORA entrega la cantidad de [IMPORTE] euros ( €), sirviendo la presente como la más eficaz carta de pago y quedando pendiente de abonar la cantidad de [IMPORTE] euros ( €) para el completo pago del Precio.

b) Hasta el momento de la entrega del Local, LA COMPRADORA abonará el % del precio pendiente de pago en períodos mensuales. El pago se efectuará el día [FECHA] de cada mes en la cuenta corriente núm. [Nº] que la VENDEDORA-PROMOTORA tiene suscrita con la entidad [DENOMINACIÓN SOCIAL] en su sucursal [SUCURSAL].

El retraso en más de [Nº] días en cualquiera de los pagos dará derecho a la VENDEDORA-PROMOTORA a exigir a la COMPRADORA un interés moratorio del % respecto de cada uno de los pagos no satisfechos puntualmente. Si la COMPRADORA se retrasara en el pago de dos plazos o en el pago del último, la VENDEDORA podrá optar entre exigir el pago de los plazos pendientes o resolver el contrato, con abono en ambos caso de las indemnizaciones que puedan corresponder.

c) El % restante del Precio se abonará en el momento de la entrega del local.

Subrogación en el préstamo hipotecario de la promotora

LA VENDEDORA-PROMOTORA ha obtenido un préstamo con garantía hipotecaria sobre los elementos inmobiliarios objeto del presente Contrato por la entidad bancaria [ENTIDAD BANCARIA], cuyas condiciones pone a disposición de LA COMPRADORA.

En este acto, LA COMPRADORA manifiesta que su deseo de subrogarse en dicho préstamo.

Entrega

LA VENDEDORA-PROMOTORA se obliga a terminar el local antes del día [FECHA], del mes [MES] de [AÑO] (año), y efectuará la entrega del mismo antes del día [FECHA] del mes [MES] del año [AÑO], salvo caso fortuito o fuerza mayor mediante la entrega de llaves y firma de escritura pública.

Dicha entrega se realizará en perfectas condiciones de habitabilidad, con las autorizaciones administrativas necesarias para su habitabilidad, y con todos sus elementos en perfecto funcionamiento con todos los servicios que a continuación se detallan dados de alta y listos para utilizarse.

[ELEGIR UNA OPCIÓN: Garantías del buen fin de la promoción / Seguro / Aval]

Otras garantías

LA VENDEDORA-PROMOTORA garantiza que cada una de las cantidades anticipadas por LA COMPRADORA se percibirán únicamente a través de la cuenta especial número [NÚMERO] de la entidad bancaria [ENTIDAD BANCARIA] separada de cualquier otro fondo perteneciente a LA VENDEDORA-PROMOTORA.

LA VENDEDORA-PROMOTORA garantiza que únicamente dispondrá de tales cantidades para las atenciones propias de la promoción.

Evicción (Contienda pendiente)

LA COMPRADORA conoce que LA VENDEDORA-PROMOTORA ha tenido que sustanciar un procedimiento judicial contrata un tercero que pretendía reclamar [OTROS DATOS], que es objeto de este contrato.

LA VENDEDORA-PROMOTORA responderá solamente de la posesión legal pero no de la posesión pacífica. LA COMPRADORA acepta la limitación establecida por LA VENDEDORA a su derecho de saneamiento.

Autorización de subrogación

LA COMPRADORA consiente y autoriza a LA VENDEDORA-PROMOTORA para que subrogue en la titularidad de la finca y promoción del edificio a cualquier persona física o jurídica que pueda surgir en el proceso de fusión, escisión, constitución y cesión de rama de actividad, siempre que la entidad subrogada acepte y cumpla puntualmente los términos de este Contrato y, en todo caso, con obligación de notificar la subrogación a LA COMPRADORA.

Condición resolutoria

El presente Contrato se resolverá por cualquier otro incumplimiento de las obligaciones de las Partes.

En particular, en caso de impago por parte de LA COMPRADORA del precio en los términos y condiciones acordados en el presente Contrato, LA COMPRADORA perderá el % de lo entregado en concepto de daños y perjuicios y se producirá la resolución del Contrato. No obstante, como requisito previo a la resolución, LA VENDEDORA-PROMOTORA deberá notificar a LA COMPRADORA el incumplimiento y conceder un plazo de [Nº] días, desde la notificación, para que LA COMPRADORA subsane dicho incumplimiento. Transcurrido dicho plazo LA VENDEDORA-PROMOTORA podrá resolver el Contrato previa comunicación fehaciente mediante conducto notarial.

Elevación a escritura pública

La escritura pública se otorgará ante el Notario que acuerden la parte [NOMBRE DE LA PARTE]

En todo caso la escritura pública deberá otorgarse antes del próximo día [DÍA] de [MES] de [AÑO].

De no comparecer alguna de las partes al otorgamiento de la escritura pública, podrá la parte que haya requerido para ello ejercitar las acciones judiciales tendentes a solicitar el referido otorgamiento. En este caso, la parte que no haya comparecido a dicho otorgamiento quedará obligada a indemnizar a la otra parte en una cantidad equivalente el importe de los gastos que se hayan derivado del ejercicio de dichas acciones, así como al pago de los daños y perjuicios que dicho incumplimiento hayan causado al requirente.

Gastos e impuestos

Todos los gastos e impuestos, directos o indirectos, conocidos o de nueva implantación, recargos, arbitrios, notariales y registrales y demás exacciones que se deriven del presente Contrato, de su elevación a público o del otorgamiento de la correspondiente escritura pública de compraventa y, en su caso, de la subrogación del préstamo hipotecario, serán de cuenta exclusiva de LA COMPRADORA, excepto el Impuesto del Incremento del Valor de los Terrenos de Naturaleza Urbana (Plusvalía), que serán por cuenta de la parte a quien legalmente corresponda.

En todo caso, serán de cuenta de LA VENDEDORA-PROMOTORA los siguientes gastos:

- Los gastos derivados de la declaración de obra nueva, propiedad horizontal y constitución de hipoteca para financiar la construcción de las viviendas, en su caso, así como los de su división y cancelación.

- Los gastos generados por la constitución de las garantías legalmente exigidas.

- Los gastos generados por la obtención de las autorizaciones exigidas para la construcción del inmueble.

- Los gastos derivados de la obtención de la cédula urbanística.

Igualmente, los gastos judiciales que se ocasionen por incumplimiento del presente contrato serán por cuenta de la parte incumplidora, incluidos honorarios del Procurador y Abogado aunque sus intervenciones no fueran preceptivas.

[ELEGIR UNA OPCIÓN: Sumisión a tribunales / Sin cláusula penal / Con cláusula penal / — y además elegir: Sumisión a arbitraje / Sin cláusula penal / Con cláusula penal]

Notificaciones

Toda notificación que se efectúe entre las partes se hará por escrito y será entregada personalmente o de cualquier otra forma que certifique la recepción por la parte notificada en los respectivos domicilios indicados en el encabezamiento de este Contrato.

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

Generalidades

El presente contrato anula y reemplaza cualquier contrato o acuerdo anterior entre las partes con el mismo objeto y sólo podrá ser modificado por un nuevo acuerdo firmado por ambas partes.

Si alguna de las cláusulas del presente contrato fuere declarada nula o inaplicable, dicha cláusula se considerará excluida del contrato, sin que implique la nulidad del mismo. En este caso las partes harán cuanto esté a su alcance para encontrar una solución equivalente que sea válida y que refleje debidamente sus intenciones.

Los encabezamientos de las distintas cláusulas lo son sólo a efectos informativos, y no afectarán, calificarán o ampliarán la interpretación de este Contrato.

Y en prueba de conformidad y aceptación de cuanto antecede, ambas partes firman los [Nº] folios del presente CONTRATO DE COMPRAVENTA DE LOCAL EN CONSTRUCCIÓN, extendido por duplicado y a un solo efecto, en la ciudad y fecha mencionados en el encabezamiento.

Fdo. Don [NOMBRE Y APELLIDOS]

(La VENDEDORA-PROMOTORA)

Fdo. Don [NOMBRE Y APELLIDOS]

(La COMPRADORA)

========================================================================
