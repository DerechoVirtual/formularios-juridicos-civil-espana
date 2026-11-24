---
name: acta-notarial-sobre-vivienda-efectos-reagrupacion-civ-0213
description: "Acta notarial sobre la vivienda a efectos de reagrupación familiar. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Acta notarial sobre la vivienda a efectos de reagrupación familiar

> Formulario **CIV-0213** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Acta notarial en la que el notario constata las características de una vivienda (titularidad, cargas, dependencias, suministros) a requerimiento de un extranjero residente que quiere acreditar que dispone de alojamiento adecuado y medios suficientes para solicitar la reagrupación familiar de su cónyuge e hijos menores.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Acta notarial sobre la vivienda a efectos de reagrupación familiar» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Acta notarial sobre la vivienda a efectos de reagrupación familiar” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:acta-notarial-sobre-vivienda-efectos-reagrupacion-civ-0213`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NÚMERO (8 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] AÑO (3 veces)
- [ ] DÍA (3 veces)
- [ ] MES (3 veces)
- [ ] NOMBRE DEL NOTARIO (3 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] Nº DE PROTOCOLO (2 veces)
- [ ] CALLE
- [ ] CLASE
- [ ] COLEGIO NOTARIAL
- [ ] DATOS REGISTRALES
- [ ] DOMICILIO
- [ ] ESTADO CIVIL
- [ ] FOLIO
- [ ] LIBRO
- [ ] LOS HIJOS Y EL CÓNYUGE
- [ ] NACIONALIDAD
- [ ] Nº
- [ ] Nº DE FINCA
- [ ] Nº DE TARJETA DE RESIDENTE
- [ ] NÚMEROS
- [ ] PORCENTAJE
- [ ] PROFESIÓN
- [ ] REFERENCIA CATASTRAL
- [ ] SERIE
- [ ] SUPERFICIE
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

### Avisos de actualización (1) — se aplican en el texto, nunca se copian en el documento

- Junto a «…tamiento, de su seguridad y confidencialidad el Notario titular de esta notaría.»: el original citaba la Orden del Ministerio de Justicia 484/2003, de 19 de febrero, sobre ficheros automatizados, y el consentimiento del art. 6 LO 3/2018; comprobar la cláusula de protección de datos vigente que utilice la notaría.

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

ACTA DE VIVIENDA PARA REAGRUPACIÓN FAMILIAR

Núm. [Nº DE PROTOCOLO]

En la ciudad de [LOCALIDAD], a [DÍA] de [MES] de [AÑO]

Ante mí, [NOMBRE DEL NOTARIO], Notario del Ilustre Colegio Notarial de [COLEGIO NOTARIAL],

COMPARECE

Don/doña [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], de profesión [PROFESIÓN], de nacionalidad [NACIONALIDAD], con domicilio en [DOMICILIO], y tarjeta de residente número [Nº DE TARJETA DE RESIDENTE].

INTERVIENE

En su propio nombre y derecho, me aseguro de su identidad por la exhibición de la tarjeta de residente reseñada.

Y le juzgo, a mi juicio, con capacidad legal para el otorgamiento de esta escritura y, a tal efecto,

EXPONE

PRIMERO.– Que don/doña [NOMBRE Y APELLIDOS] tiene [ELEGIR: esposo / esposa] y [NÚMERO] hijos menores de edad.

SEGUNDO.– Que el compareciente dispone de un alojamiento adecuado y de los medios de subsistencia suficientes para atender las necesidades de su familia, una vez que se lleve a cabo el reagrupamiento.

TERCERO.– Que la vivienda se encuentra en [LOCALIDAD], calle [CALLE] número [NÚMERO], con una superficie de [SUPERFICIE] metros cuadrados, y el compareciente es propietario en pleno dominio de la misma.

Cuota de [PORCENTAJE] % en el valor del bloque donde está ubicada la citada vivienda y elementos comunes.

Título: adquirida por [TÍTULO: compraventa / herencia / donación], efectuada en virtud de escritura pública otorgada ante el Notario de [LOCALIDAD] D. [NOMBRE DEL NOTARIO] el día [DÍA] de [MES] de [AÑO], número de protocolo [Nº DE PROTOCOLO].

Inscripción: está inscrita en el Registro de la Propiedad número [Nº] de [LOCALIDAD], en el tomo [TOMO], libro [LIBRO], folio [FOLIO], finca [Nº DE FINCA] [DATOS REGISTRALES], según información solicitada al referido Registro de la Propiedad, que ha sido recibida por [ELEGIR: telefax / vía telemática]. Se incorpora la nota simple informativa a esta matriz.

Referencia catastral: [REFERENCIA CATASTRAL], según consta en la referencia del último recibo del Impuesto sobre Bienes Inmuebles. Asimismo se incorpora la certificación catastral descriptiva y gráfica obtenida por mí, el Notario, en la Oficina Virtual del Catastro, que uno a esta matriz.

Cargas: la referida finca se encuentra libre de cargas y gravámenes, según nota simple expedida por el Registro de la Propiedad el día de hoy, y que se une a este documento.

Arrendamientos: la referida finca no se encuentra arrendada y está libre de ocupantes e inquilinos.

Gastos de Comunidad: el inmueble se encuentra al corriente en el pago de los gastos de comunidad de propietarios del edificio al que la finca pertenece, de acuerdo con el certificado expedido por la administración del inmueble que queda unido a este documento.

Régimen de Comunidad: se rige por lo dispuesto en los Estatutos de la Comunidad de Propietarios autorizados en virtud de escritura pública otorgada ante el Notario de [LOCALIDAD] D. [NOMBRE DEL NOTARIO] el día [DÍA] de [MES] de [AÑO].

CUARTO.– Que la vivienda tiene [NÚMERO] dependencias, de las cuales [NÚMERO] son baños, [NÚMERO] dormitorios, [NÚMERO] cocina y [NÚMERO] salón.

Que las citadas habitaciones se encuentran a día de hoy vacías, salvo la de don/doña [NOMBRE Y APELLIDOS], por lo que, a partir de la reagrupación familiar, se destinarán a su utilización por [LOS HIJOS Y EL CÓNYUGE] del compareciente.

QUINTO.– Que la vivienda dispone de agua corriente, electricidad y gas, tal y como consta en los contratos que el compareciente me exhibe.

REQUIERE

ÚNICO.– Que el compareciente me requiere para que me constituya en la vivienda cuya dirección ha sido detallada, al objeto de acreditar las características de la misma y, en concreto, si lo manifestado en la presente escritura es fiel reflejo de la realidad del inmueble, y haga constar la certeza de los referidos extremos.

OTORGAMIENTO Y AUTORIZACIÓN

Reservas y advertencias legales

Se las realizo al compareciente, en especial las de carácter fiscal y registral.

Se informa al compareciente de que sus datos personales serán tratados por el Notario conforme al Reglamento (UE) 2016/679 (RGPD) y a la Ley Orgánica 3/2018, de 5 de diciembre, de Protección de Datos Personales y garantía de los derechos digitales, con la finalidad de facilitar la tramitación y seguimiento de esta escritura, conservándose con carácter confidencial y reservado y sin perjuicio de las comunicaciones autorizadas por la ley. Es responsable del tratamiento, de su seguridad y confidencialidad el Notario titular de esta notaría.

Lectura

Permito al señor compareciente la lectura de esta escritura, porque así lo solicita después de advertido de la opción del artículo 193 del Reglamento Notarial.

Consentimiento

Enterado, según dice, por la lectura que ha practicado y por mis explicaciones verbales, el señor compareciente hace constar libremente su consentimiento al contenido de la escritura.

Firma

Y la firma.

Autorización

Yo, el Notario, compruebo que este otorgamiento se adecua a la legalidad y a la voluntad debidamente informada y expresada ante mí; y con el contenido de esta escritura, extiendo en [NÚMERO] folios de papel timbrado notarial de la clase [CLASE], serie [SERIE], números [NÚMEROS]. DOY FE.

Firmas
