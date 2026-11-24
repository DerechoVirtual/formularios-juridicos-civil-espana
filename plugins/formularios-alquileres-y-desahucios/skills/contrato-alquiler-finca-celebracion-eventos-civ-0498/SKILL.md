---
name: contrato-alquiler-finca-celebracion-eventos-civ-0498
description: "Contrato de alquiler de finca para la celebración de eventos. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de alquiler de finca para la celebración de eventos

> Formulario **CIV-0498** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de alquiler de finca para la celebración de eventos» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de alquiler de finca para la celebración de eventos” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:contrato-alquiler-finca-celebracion-eventos-civ-0498`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (8 veces)
- [ ] IMPORTE (6 veces)
- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] NÚMERO (4 veces)
- [ ] DOMICILIO (2 veces)
- [ ] AÑO
- [ ] CALLE
- [ ] DENOMINACIÓN SOCIAL
- [ ] DÍA
- [ ] ESTADO CIVIL
- [ ] FOLIO
- [ ] LIBRO
- [ ] LUGAR
- [ ] MES
- [ ] Nº DE FINCA
- [ ] OTROS DATOS
- [ ] PORCENTAJE
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

En [LUGAR], a [DÍA] de [MES] de [AÑO].

REUNIDOS

De una parte:

D [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número [NÚMERO]

De otra:

D D [NOMBRE Y APELLIDOS], mayor de edad, de estado civil, vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número [NÚMERO]

[ELEGIR UNA OPCIÓN: Intervienen / Si intervienen en nombre y representación del alguien / Opción 1: Si intervienen en nombre y representación de alguien / Si intervienen en su propio nombre y derecho / Opción 2: Si intervienen en su propio nombre y derecho]

EXPONEN

Que LA ARRENDADORA es propietaria en régimen de plena propiedad y dominio de la hacienda sita en [LOCALIDAD], calle [CALLE] número [NÚMERO] con una superficie de [Nº] metros cuadrados inscrito en el Registro de la Propiedad de [LOCALIDAD] en el Tomo [TOMO], Libro [LIBRO], Folio [FOLIO], Finca [Nº DE FINCA] e inscripción número

Que la mencionada hacienda se encuentra dividida en [Nº] habitaciones de uso privativo, baño, vestíbulo, pasillo y cocina de uso compartido con el resto de los inquilinos,

Que la mencionada vivienda se encuentra libre de cargas y gravámenes y al corriente en el pago de impuestos.

Que LA ARRENDATARIA se encuentra interesada en el arrendamiento de la Hacienda descrita en el anterior Exponendo.

Como quiera que ambas partes se encuentran interesadas en el arrendamiento de la Hacienda supra referida, ambas partes de común acuerdo llevan a efecto el presente contrato con arreglo a las siguientes:

CLÁUSULAS

[ELEGIR UNA OPCIÓN: Objeto / Opción 1: con mobiliario / Opción 2: sin mobiliario]

Precio

LA ARRENDADORA recibirá la cantidad de [IMPORTE] EUROS ( €) por el alquiler de las instalaciones de la Hacienda en aquellos casos en que el evento a realizar supere la cantidad de [IMPORTE] personas y sea inferior a

Para celebraciones de un número de personas superior a [Nº] personas, este precio tendrá además un suplemento de [IMPORTE] € por cada persona que supere este número. En caso de realizar el arrendamiento más de un evento en la misma fecha, este deberá abonar [IMPORTE] euros por cada persona de los demás eventos. Está incluido en el precio las instalaciones de cocina.

Por debajo de esta cantidad de comensales, siendo este un alquiler parcial de las instalaciones, el arrendatario pagará [IMPORTE] € por persona. Si el arrendatario quisiera hacer uso de las cocinas deberá pagar [IMPORTE] €.

A la firma del presente contrato, se entregará en concepto de depósito, el 50% del importe total del arrendamiento concertado. En caso de cancelación del arrendamiento de las instalaciones, por parte del arrendatario, éste perderá el importe de dicho depósito pero la arrendataria podrá solicitar un único cambio de fecha del mismo evento que le concederá el arrendador siempre que esté disponible, pudiendo la Arrendadora aplicarla a los gastos generales por tal anulación.

Uso

El arrendamiento de la Hacienda será de uso exclusivo para celebración de eventos con un número mínimo de [Nº] personas y estará delimitado a las zonas e instalaciones del establecimiento que se Acuerden.

Para aquellos eventos que el número de comensales se inferior a [Nº] el uso de las instalaciones será parcial, esto es, se delimitará la zona a utilizar para dicho evento y LA ARRENDADORA tendrá potestad de arrendar otras estancias de la Hacienda para la celebración de eventos a otras empresas en la misma fecha.

Queda totalmente prohibido la utilización de fuegos artificiales de cualquier tipo, artefactos explosivos, como petardos, tracas, cañones de humos [OTROS DATOS], dentro de la propiedad de la Hacienda, tanto en su interior como en su exterior. Si se produjera cualquier acto de este tipo, la propiedad no tendrá responsabilidad alguna, siendo el arrendatario el responsable ante las autoridades de cualquier hecho que pudiera imputarse.

[ELEGIR UNA OPCIÓN: Limpieza / Opción 1: por cuenta de la arrerndataria / Opción 1: Por cuenta de la arrendataria / Opción 2: por cuenta de la arrendadora]

Servicio de aparcamiento y vigilancia

El servicio de aparcamiento y vigilancia, incluso para estacionamiento de autobuses estará incluido en el precio.

LA ARRENDADORA no asume responsabilidad en daños causados al vehículo por vuelco, colisión, caída de árbol, cables, lluvia, granizo, rayo, incendio, explosión, ni en los casos de robo total del vehículo, de partes interiores y/o exteriores, así como en la sustracción del interior del mismo de objetos, documentos, sustancias, valores materiales, diversos, u otros.

Si el evento a celebrar en las instalaciones cuenta con la asistencia de niños de edades comprendidas entre 3 y 12 años, LA ARRENDATARIA deberá contratar un servicio de cuidado (un cuidador por cada [Nº] niños), cuyo coste irá a su cargo

Publicidad

LA ARRENDATARIA podrá llevar a cabo la publicidad que considera oportuna de las instalaciones arrendadas y de la actividad o servicio que desarrolle en las mismas. En ningún caso, podrá colocar en la fachada de la Hacienda ni en sus interiores, rótulos publicitarios.

Catering

La empresa de catering que ofrezca el servicio, deberá disponer del correspondiente registro sanitario para el servicio de Catering de colectividades diversas, así como de un seguro de Responsabilidad Civil vigente.

Fianza

LA ARRENDATARIA debe hacer entrega a LA ARRENDADORA en concepto de fianza, de un % del importe del arrendamiento.

La fianza le será devuelta a LA ARRENDADATARIA en el plazo de [Nº] días contados a partir del momento de la devolución de la habitación arrendada una vez cumplidas por LA ARRENDATARIA las obligaciones contraídas, a cuya responsabilidad queda afectada, así como al resarcimiento de daños y perjuicios, sirviendo este documento como formal carta de pago. Dicha fianza no devengará intereses.

Queda establecido que bajo ningún concepto LA ARRENDATARIA podrá canjear la fianza depositada en este acto por ninguna mensualidad de alquiler, ni cualquier otro pago inherente al presente contrato de arrendamiento.

Avalista/fiador

D. [NOMBRE Y APELLIDOS], provisto de D.N.I. número [NÚMERO] y presente en este acto, se constituye en fiador/avalista de las obligaciones contraídas por LA ARRENDATARIA con LA ARRENDADORA, obligándose solidariamente con LA ARRENDATARIA al cumplimiento de las obligaciones arrendaticias y especialmente al pago de la renta, así como a cualquier cantidad económica que se derive del presente contrato o por disposición legal, y a la conservación del buen estado de la vivienda por toda la duración del contrato, con renuncia expresa a los beneficios de excusión, división.

A tal efecto, acepta de antemano cualquier prórroga o renovación que LA ARRENDADORA pudiera conceder, sea cual sea la forma en que se instrumente la misma, sin que, en consecuencia, la concesión de la indicada prórroga o renovación pueda producir los efectos establecidos en el artículo 1.851 del Código Civil.

Seguro

LA ARRENDATARIA contratará un seguro que resulte satisfactorio para LA ARRENDADORA y que cubra el riesgo de daños o pérdida que pueda sufrir la vivienda durante todo el periodo de vigencia del presente contrato.

Honorarios del mediador inmobiliario

En este arrendamiento ha intervenido como mediador la entidad [DENOMINACIÓN SOCIAL]

Mediante el presente contrato se fijan los honorarios por la intervención de la referida entidad en el [PORCENTAJE] % de la renta de un año.

El precio fijado se pagará por la parte arrendadora y por la arrendataria por mitad e iguales partes.

Resolución del contrato

El incumplimiento de las obligaciones que resulten del presente contrato facultará a la parte que cumpla los suyos a exigir a la otra su cumplimiento, o, a su elección, a resolver el contrato, con abono en ambos casos de la indemnización por daños y perjuicios que proceda.

Gastos e Impuestos

Todos los gastos e impuestos que se originen como consecuencia del evento, así como la obtención de las licencias y permisos necesarios para su celebración serán de cargo de la parte arrendataria.

Igualmente, los gastos judiciales que se ocasionen por incumplimiento del presente contrato serán por cuenta de la parte incumplidora, incluidos honorarios del Procurador y Abogado aunque sus intervenciones no fueran preceptivas.

Jurisdicción competente y ley aplicable

El conocimiento de los litigios relativos a que diera lugar la interpretación y/o ejecución del presente contrato corresponderá al Tribunal de Instancia del lugar en que se halle la finca.

El presente contrato tiene carácter civil, se regirá por sus propias cláusulas, y en lo en ellas no dispuesto, por lo previsto en el Código Civil y demás leyes especiales.

Notificaciones

Toda notificación que se efectúe entre las partes se hará por escrito y será entregada personalmente o de cualquier otra forma que certifique la recepción por la parte notificada en los respectivos domicilios indicados en el encabezamiento de este Contrato.

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

Generalidades

El presente contrato anula y reemplaza cualquier contrato o acuerdo anterior entre las partes con el mismo objeto y sólo podrá ser modificado por un nuevo acuerdo firmado por ambas partes.

Si alguna de las cláusulas del presente contrato fuere declarada nula o inaplicable, dicha cláusula se considerará excluida del contrato, sin que implique la nulidad del mismo. En este caso las partes harán cuanto esté a su alcance para encontrar una solución equivalente que sea válida y que refleje debidamente sus intenciones.

Los encabezamientos de las distintas cláusulas lo son sólo a efectos informativos, y no afectarán, calificarán o ampliarán la interpretación de este Contrato.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

Y en prueba de conformidad y aceptación de cuanto antecede, ambas partes firman los [Nº] folios del presente CONTRATO DE ALQUILER DE HACIENDA PARA LA CELEBRACIÓN DE EVENTOS, extendido por duplicado y a un solo efecto, en la ciudad y fecha mencionados en el encabezamiento.

Fdo. Don [NOMBRE Y APELLIDOS]

(La Arrendadora)

Fdo. Don [NOMBRE Y APELLIDOS]

(La Arrendataria)
