---
name: escritura-capitulaciones-matrimoniales-regimen-civ-0212
description: "Escritura de capitulaciones matrimoniales con régimen de participación. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escritura de capitulaciones matrimoniales con régimen de participación

> Formulario **CIV-0212** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escritura de capitulaciones matrimoniales con régimen de participación» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escritura de capitulaciones matrimoniales con régimen de participación” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:escritura-capitulaciones-matrimoniales-regimen-civ-0212`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (21 veces)
- [ ] LOCALIDAD (10 veces)
- [ ] IMPORTE (8 veces)
- [ ] MES (6 veces)
- [ ] Nº (6 veces)
- [ ] NÚMERO (6 veces)
- [ ] AÑO (4 veces)
- [ ] DÍA (4 veces)
- [ ] FECHA (3 veces)
- [ ] TOMO (3 veces)
- [ ] CALLE (2 veces)
- [ ] ENTIDAD BANCARIA (2 veces)
- [ ] FINCA (2 veces)
- [ ] FOLIO (2 veces)
- [ ] LIBRO (2 veces)
- [ ] NIF (2 veces)
- [ ] PORCENTAJE (2 veces)
- [ ] PROFESIÓN (2 veces)
- [ ] TÍTULO DE ADQUISICIÓN (2 veces)
- [ ] CLASE
- [ ] COLEGIO
- [ ] DENOMINACIÓN SOCIAL
- [ ] MARCA/MODELO
- [ ] Nº DE BASTIDOR
- [ ] Nº DE PROTOCOLO
- [ ] PÁGINA
- [ ] SERIE
- [ ] TIPO DE VEHÍCULO

## Normas que cita el formulario

- art. 6 Ley Orgánica 3/2018

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

- Junto a «… garantía de los derechos digitales (LOPDGDD), y Reglamento (UE) 2016/679 (RGPD)»: La LO 15/1999 y su Reglamento (RD 1720/2007) fueron sustituidos por el Reglamento (UE) 2016/679 (RGPD) y la LO 3/2018, de 5 de diciembre (LOPDGDD). Fuente: LO 3/2018, disposición derogatoria única.

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

CAPITULACIONES MATRIMONIALES RÉGIMEN DE PARTICIPACIÓN

Núm. [Nº]

En la ciudad de [LOCALIDAD], a [FECHA]

Ante mí, Notario del Ilustre Colegio de [COLEGIO]

COMPARECEN

Los cónyuges, don/doña [NOMBRE Y APELLIDOS], mayor de edad, de profesión [PROFESIÓN], y NIF número [NIF], y don/doña [NOMBRE Y APELLIDOS], mayor de edad, de profesión [PROFESIÓN], y NIF [NIF], con domicilio ambos en

INTERVIENEN

Ambos en su propio nombre y derecho, me aseguro de su identidad por la exhibición de los reseñados documentos nacionales de identidad.

Y les juzgo, a mi juicio, con capacidad legal para el otorgamiento de esta escritura y, a tal efecto,

EXPONEN

Don [NOMBRE Y APELLIDOS] y doña [NOMBRE Y APELLIDOS] manifiestan que el [DÍA] de [MES] de [AÑO] contrajeron entre sí matrimonio, que fue inscrito en el Registro Civil de [LOCALIDAD] tomo [TOMO] página [PÁGINA], siendo su régimen económico matrimonial el de sociedad de gananciales.

a) Que don [NOMBRE Y APELLIDOS] y doña [NOMBRE Y APELLIDOS] son propietarios del inmueble sito en [LOCALIDAD], calle [CALLE] número [NÚMERO] con una superficie de [Nº] metros cuadrados.

Cuota de [PORCENTAJE] % en el valor del bloque donde está ubicado la citada vivienda y elementos comunes.

Título: Adquirido por [TÍTULO DE ADQUISICIÓN] efectuada en virtud de escritura pública otorgada ante el Notario de [LOCALIDAD], D. el día [DÍA] de [MES] de [AÑO] número protocolo

Inscripción: Está inscrita en el Registro de la Propiedad número [NÚMERO] de [LOCALIDAD] en el tomo [TOMO], libro [LIBRO] folio [FOLIO], finca [FINCA], según información solicitada al referido Registro de la Propiedad, que ha sido recibida mediante Telefax. Se incorpora la nota simple informativa a esta matriz.

Referencia catastral: según consta en la referencia del último recibo del Impuestos sobre bienes Inmuebles. Así mismo se incorpora la certificación catastral descriptiva y gráfica obtenida por mí, el Notario, en la Oficina Virtual del Catastro, que uno a esta matriz.

Cargas: La referida finca se encuentra libre de cargas y gravámenes, según nota simple expedida por el Registro de la Propiedad el día de hoy, y que se une a este documento, salvo la hipoteca que en adelante se detallará.

Arrendamientos: La referida finca no se encuentra arrendada y está libre de ocupantes e inquilinos.

Gastos de Comunidad: El inmueble se encuentra al corriente en el pago de los gastos de comunidad de propietarios del edificio al que la finca pertenece, de acuerdo con el certificado expedido por la administración del Inmueble que queda unido a este documento.

Régimen de Comunidad: Se rige por lo dispuesto en los Estatutos de la Comunidad de Propietarios autorizados en virtud de escritura pública otorgada ante el Notario de [LOCALIDAD] (localidad) D. el día [FECHA] de [MES] de

Valor: La finca se valora en [IMPORTE] euros.

b) Que don [NOMBRE Y APELLIDOS] y doña [NOMBRE Y APELLIDOS], resultan prestatarios de un crédito hipotecario del que faltan por amortizar [IMPORTE] euros, tal y como consta en la escritura de [DÍA] de [MES] de [AÑO], con numero de protocolo [Nº DE PROTOCOLO], otorgada ante el Notario D. [NOMBRE Y APELLIDOS]

c) Que don [NOMBRE Y APELLIDOS] y doña [NOMBRE Y APELLIDOS] son propietarios del vehículo [TIPO DE VEHÍCULO], marca [MARCA/MODELO], con número de bastidor [Nº DE BASTIDOR]

Valor: El vehículo se valora en [IMPORTE] euros.

d) Que don [NOMBRE Y APELLIDOS] es titular de [Nº] participaciones en la mercantil [DENOMINACIÓN SOCIAL] de responsabilidad limitada.

Valor: Las participaciones se valoran en [IMPORTE] euros.

e) Que doña [NOMBRE Y APELLIDOS] es propietaria del inmueble sito en [LOCALIDAD], calle [CALLE] número [NÚMERO] con una superficie de [Nº] metros cuadrados.

Cuota de [PORCENTAJE] % en el valor del bloque donde está ubicado la citada vivienda y elementos comunes.

Título: Adquirido por [TÍTULO DE ADQUISICIÓN] efectuada en virtud de escritura pública otorgada ante el Notario de [LOCALIDAD], D. el día [DÍA] de [MES] de [AÑO] número protocolo

Inscripción: Está inscrita en el Registro de la Propiedad número [NÚMERO] de [LOCALIDAD] en el tomo [TOMO], libro [LIBRO] folio [FOLIO], finca [FINCA], según información solicitada al referido Registro de la Propiedad, que ha sido recibida mediante Telefax. Se incorpora la nota simple informativa a esta matriz.

Referencia catastral: según consta en la referencia del último recibo del Impuestos sobre bienes Inmuebles. Así mismo se incorpora la certificación catastral descriptiva y gráfica obtenida por mí, el Notario, en la Oficina Virtual del Catastro, que uno a esta matriz.

Cargas: La referida finca se encuentra libre de cargas y gravámenes, según nota simple expedida por el Registro de la Propiedad el día de hoy, y que se une a este documento

Arrendamientos: La referida finca se encuentra arrendada y está libre de ocupantes e inquilinos.

Gastos de Comunidad: El inmueble se encuentra al corriente en el pago de los gastos de comunidad de propietarios del edificio al que la finca pertenece, de acuerdo con el certificado expedido por la administración del Inmueble que queda unido a este documento.

Régimen de Comunidad: Se rige por lo dispuesto en los Estatutos de la Comunidad de Propietarios autorizados en virtud de escritura pública otorgada ante el Notario de [LOCALIDAD] D. el día [FECHA] de [MES] de

Valor: La finca se valora en [IMPORTE] euros.

f) Que don [NOMBRE Y APELLIDOS] es propietario de la cuenta corriente nº [NÚMERO] de la entidad bancaria [ENTIDAD BANCARIA]

g) Que doña [NOMBRE Y APELLIDOS] es propietaria de la cuenta corriente nº [NÚMERO] de la entidad bancaria [ENTIDAD BANCARIA]

Que los comparecientes desean modificar su régimen económico matrimonial, transformándolo en un régimen de participación.

ESTIPULACIONES

Objeto

Los comparecientes acuerdan, para lo sucesivo, someterse al régimen económico matrimonial de participación que se encuentra desarrollado en el Código Civil, artículos 1.411 a 1.434.

Patrimonios iniciales

El patrimonio inicial de don [NOMBRE Y APELLIDOS] se compone de los siguientes bienes:

- Vehículo descrito en el expositivo segundo, apartado c).

- 50% de la vivienda descrita en el expositivo segundo, apartado a).

- Participaciones detalladas en el expositivo segundo, apartado d).

- Cuenta corriente descrita en el expositivo segundo, apartado f).

El valor del patrimonio inicial de don [NOMBRE Y APELLIDOS] asciende a [IMPORTE] euros.

El patrimonio inicial de doña [NOMBRE Y APELLIDOS] se compone de los siguientes bienes:

- 50% de la vivienda descrita en el expositivo segundo, apartado a).

- Vivienda descrita en el expositivo segundo, apartado e).

- Cuenta corriente descrita en el expositivo segundo, apartado g).

El valor del patrimonio inicial de doña [NOMBRE Y APELLIDOS] asciende a [IMPORTE] Euros.

Al valor del patrimonio inicial de cada compareciente, hay que restarle el 50% del importe que se adeuda a la entidad bancaria que les concedió el préstamo hipotecario que figura en el expositivo segundo, apartado b).

Liquidación de la sociedad de gananciales

Los comparecientes acuerdan liquidar la sociedad de gananciales, adjudicándose cada uno el 50% de la vivienda descrita en el expositivo segundo, apartado a), y el 50% del crédito hipotecario detallado en el expositivo segundo, apartado b).

Respecto al vehículo mencionado en el expositivo segundo, apartado c), se lo adjudica don [NOMBRE Y APELLIDOS], quien compensa a doña [NOMBRE Y APELLIDOS], con el pago de [IMPORTE] euros por su 50%.

Registro civil

Los comparecientes solicitan que se haga constar en el Registro Civil el cambio de régimen económico del matrimonio.

OTORGAMIENTO Y AUTORIZACIÓN

Reservas y advertencias legales

Se las realizo a los comparecientes, en especial, las de carácter fiscal y registral.

Advierto también sobre la incorporación de datos a los ficheros automatizados regulados en la Orden del Ministerio de Justicia 484/2003, de 19 de febrero.

De conformidad con el art. 6º de la Ley Orgánica 3/2018, de 5 de diciembre, de Protección de Datos Personales y garantía de los derechos digitales (LOPDGDD), y Reglamento (UE) 2016/679 (RGPD) (B.O.E. de 14 de diciembre de 1999), los comparecientes prestan su expreso consentimiento para que sus datos de carácter personal queden incorporados a los ficheros automatizados de esta Notaría, conservándose en la misma, con carácter confidencial y reservado, y sin perjuicio de las remisiones autorizadas por la Ley.

La finalidad de esta incorporación es facilitar la tramitación y seguimiento de esta escritura.

Es responsable del fichero, de su seguridad y confidencialidad, el Notario titular de esta notaría.

Lectura

Permito a los señores comparecientes la lectura de esta escritura, porque así lo solicitan después de advertidos de la opción del artículo 193 del Reglamento Notarial.

Consentimiento

Enterados, según dicen, por la lectura que han practicado y por mis explicaciones verbales, los señores comparecientes hacen constar libremente su consentimiento al contenido de la escritura.

Firma

Y la firman.

Autorización

Yo, el Notario, compruebo que este otorgamiento se adecúa a la legalidad, y a la voluntad debidamente informada y expresada ante mi; y con el contenido de esta escritura, extiendo en [Nº] folios de papel timbrado notarial de la clase [CLASE], serie [SERIE], números [Nº] DOY FE.

========================================================================
