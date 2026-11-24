---
name: escritura-constitucion-pareja-hecho-segun-derecho-civ-0201
description: "Escritura de constitución de pareja de hecho según el Derecho de Canarias. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escritura de constitución de pareja de hecho según el Derecho de Canarias

> Formulario **CIV-0201** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escritura de constitución de pareja de hecho según el Derecho de Canarias» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escritura de constitución de pareja de hecho según el Derecho de Canarias” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:escritura-constitucion-pareja-hecho-segun-derecho-civ-0201`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (9 veces)
- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] Nº (6 veces)
- [ ] NÚMERO (4 veces)
- [ ] CALLE (2 veces)
- [ ] ENTIDAD BANCARIA (2 veces)
- [ ] ESTADO CIVIL (2 veces)
- [ ] MUNICIPIO DE EMPADRONAMIENTO (2 veces)
- [ ] NIF (2 veces)
- [ ] AÑO
- [ ] CLASE
- [ ] COLEGIO
- [ ] DENOMINACIÓN SOCIAL
- [ ] DÍA
- [ ] FECHA
- [ ] FINCA
- [ ] FOLIO
- [ ] LIBRO
- [ ] MARCA/MODELO
- [ ] MES
- [ ] Nº DE BASTIDOR
- [ ] Nº DE HIJOS
- [ ] PERITO
- [ ] PORCENTAJE
- [ ] SERIE
- [ ] TIPO DE VEHÍCULO
- [ ] TOMO
- [ ] TÍTULO DE ADQUISICIÓN

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

### Avisos de actualización (2) — se aplican en el texto, nunca se copian en el documento

- Junto a «…hasta el tercer grado. e. No están persona con discapacidad con medidas de apoyo»: Desde la Ley 8/2021, de 2 de junio, no existe la incapacitación judicial ni la tutela de mayores de edad: donde el texto dice «incapacitado» debe entenderse persona con discapacidad que cuenta con medidas de apoyo (en su caso, curatela representativa). Fuente: Ley 8/2021.
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

Núm. [Nº]

En la ciudad de [LOCALIDAD], a [FECHA]

Ante mí, Notario del Ilustre Colegio de [COLEGIO]

COMPARECEN

Don/doña [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], con domicilio en [LOCALIDAD], y empadronado en [MUNICIPIO DE EMPADRONAMIENTO], y NIF número [NIF]

Don/doña [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], con domicilio en [LOCALIDAD], y empadronado en [MUNICIPIO DE EMPADRONAMIENTO], y NIF número [NIF]

INTERVIENEN

Ambos en su propio nombre y derecho, me aseguro de su identidad por la exhibición de los reseñados documentos nacionales de identidad.

Y les juzgo, a mi juicio, con capacidad legal para el otorgamiento de esta escritura y, a tal efecto,

EXPONEN

PRIMERO Que llevan conviviendo en relación de afectividad, de forma libre, pública y notoria, desde hace [Nº] años.

Que tienen [Nº DE HIJOS] hijos comunes, menores de edad.

SEGUNDO Que no se hallan incursos en ninguno de los motivos que impiden la constitución de la pareja de hecho:

a. No son menores de edad.

b. No se encuentran ligadas por el vínculo del matrimonio.

c. No forman una unión estable con otra persona.

d. No son parientes en línea recta por consanguinidad o adopción, o colateral hasta el tercer grado.

e. No están persona con discapacidad con medidas de apoyo .

TERCERO Que me entregan la siguiente documentación:

- Certificado del Registro Civil de [LOCALIDAD] acerca del estado civil de los comparecientes.

- Certificado de empadronamiento del Municipio de [LOCALIDAD] de los comparecientes.

ESTIPULACIONES

Los comparecientes desean constituirse en pareja de hecho, sin condiciones y con carácter de permanencia, conforme a la Ley 5/2003, de 6 de marzo, de parejas de hecho de la Comunidad Autónoma de Canarias.

Los comparecientes establecen su domicilio en la calle [CALLE], de [LOCALIDAD]

Los comparecientes contribuirán al mantenimiento del hogar y a los gastos comunes, con el trabajo doméstico y con sus recursos, en proporción a sus ingresos respectivos, y si no son suficientes, de acuerdo a sus patrimonios.

Son bienes privativos de cada compareciente, que continuarán ostentando dicha condición:

A) D [NOMBRE Y APELLIDOS] es propietario en régimen de plena propiedad y dominio del inmueble sito en [LOCALIDAD], calle [CALLE] número [NÚMERO] con una superficie de [Nº] metros cuadrados, distribuidos en dos plantas.

Cuota de [PORCENTAJE] % en el valor del bloque donde está ubicado la citada vivienda y elementos comunes.

Título: Adquirido por [TÍTULO DE ADQUISICIÓN] efectuada en virtud de escritura pública otorgada ante el Notario de [LOCALIDAD], D. el día [DÍA] de [MES] de [AÑO] número protocolo

Inscripción: Está inscrita en el Registro de la Propiedad número [NÚMERO] de [LOCALIDAD] en el tomo [TOMO], libro [LIBRO] folio [FOLIO], finca [FINCA]

Referencia catastral: según consta en la referencia del último recibo del Impuestos sobre bienes Inmuebles.

Cargas: La referida finca se encuentra libre de cargas y gravámenes.

B) D. [NOMBRE Y APELLIDOS], es propietario del vehículo [TIPO DE VEHÍCULO], marca [MARCA/MODELO], con número de bastidor [Nº DE BASTIDOR]

C) Don [NOMBRE Y APELLIDOS] es titular de [Nº] participaciones en la mercantil [DENOMINACIÓN SOCIAL] de responsabilidad limitada.

D) Don [NOMBRE Y APELLIDOS] es propietario de la cuenta corriente nº [NÚMERO] de la entidad bancaria [ENTIDAD BANCARIA]

E) Doña [NOMBRE Y APELLIDOS] es propietaria de la cuenta corriente nº [NÚMERO] de la entidad bancaria [ENTIDAD BANCARIA]

Los comparecientes mantendrán la administración individual sobre sus bienes actuales, debiendo responder con los mismos, de sus deudas personales.

No obstante, a partir de la constitución de la pareja de hecho, deciden someterse al régimen de comunidad de bienes, otorgando carácter común a los bienes y ganancias que adquieran en un futuro.

Los comparecientes se facultan para obtener información y autorización médica en relación con el otro miembro de la pareja, en los casos en que razones médicas lo exijan o aconsejen.

En caso de cese de la convivencia, y extinción de la pareja de hecho, los comparecientes acuerdan someterse a la valoración pericial de los inmuebles que pudieran adquirir, mientras se encuentre vigente la pareja estable, al objeto de proceder a la extinción del condominio, de manera inmediata.

El dictamen pericial se encargará a [PERITO]

OTORGAMIENTO Y AUTORIZACIÓN

Reservas y advertencias legales.-

Se las realizo a los comparecientes, en especial, las de carácter fiscal y registral.

Advierto también sobre la incorporación de datos a los ficheros automatizados regulados en la Orden del Ministerio de Justicia 484/2003, de 19 de febrero.

De conformidad con el art. 6º de la Ley Orgánica 3/2018, de 5 de diciembre, de Protección de Datos Personales y garantía de los derechos digitales (LOPDGDD), y Reglamento (UE) 2016/679 (RGPD) (B.O.E. de 14 de diciembre de 1999), los comparecientes prestan su expreso consentimiento para que sus datos de carácter personal queden incorporados a los ficheros automatizados de esta Notaría, conservándose en la misma, con carácter confidencial y reservado, y sin perjuicio de las remisiones autorizadas por la Ley.

La finalidad de esta incorporación es facilitar la tramitación y seguimiento de esta escritura.

Es responsable del fichero, de su seguridad y confidencialidad, el Notario titular de esta notaría.

Lectura.-

Permito a los señores comparecientes la lectura de esta escritura, porque así lo solicitan después de advertidos de la opción del artículo 193 del Reglamento Notarial.

Consentimiento.-

Enterados, según dicen, por la lectura que han practicado y por mis explicaciones verbales, los señores comparecientes hacen constar libremente su consentimiento al contenido de la escritura.

Firma.-

Y la firman.

Autorización.-

Yo, el Notario, compruebo que este otorgamiento se adecúa a la legalidad, y a la voluntad debidamente informada y expresada ante mi; y con el contenido de esta escritura, extiendo en [Nº] folios de papel timbrado notarial de la clase [CLASE], serie [SERIE], números [Nº] DOY FE.

========================================================================
