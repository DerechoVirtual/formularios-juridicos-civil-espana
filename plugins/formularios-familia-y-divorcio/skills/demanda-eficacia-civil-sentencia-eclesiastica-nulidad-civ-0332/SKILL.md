---
name: demanda-eficacia-civil-sentencia-eclesiastica-nulidad-civ-0332
description: "Demanda de eficacia civil de sentencia eclesiástica de nulidad matrimonial con petición de medidas. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de eficacia civil de sentencia eclesiástica de nulidad matrimonial con petición de medidas

> Formulario **CIV-0332** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Demanda en solicitud de eficacia civil de la sentencia de nulidad matrimonial dictada por el Tribunal Eclesiástico, con petición de medidas definitivas.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de eficacia civil de sentencia eclesiástica de nulidad matrimonial con petición de medidas» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de eficacia civil de sentencia eclesiástica de nulidad matrimonial con petición de medidas” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-eficacia-civil-sentencia-eclesiastica-nulidad-civ-0332`.
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
- [ ] NÚMERO (6 veces)
- [ ] FECHA (5 veces)
- [ ] CALLE (4 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] AÑO
- [ ] COLEGIO
- [ ] DNI/NIE
- [ ] LETRA
- [ ] LUGAR
- [ ] OTROS DATOS
- [ ] PUERTA
- [ ] ÓRGANO JUDICIAL

## Normas que cita el formulario

- art. 769.1 LEC
- art. 9.2 LOPJ
- art. 85 LOPJ
- art. 80 CC
- art. 749.1 LEC
- art. 23 LEC
- art. 778 LEC
- art. 91 CC
- art. 770 LEC
- art. 96 CC
- art. 394 LEC

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

- Junto a «…ELEGIR: SECCIÓN CIVIL / SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD] DE [LOCALIDAD]»: Denominación legal: Sección de Familia, Infancia y Capacidad. Si no existe en el partido, conoce la Sección Civil o la Única (art. 86.3-4 LOPJ). Fuente: LOPJ arts. 84.2.a) y 86 (redacc. LO 1/2025, BOE-A-2025-76).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Notas al pie del formulario original:
(1) El texto original del art. 778 LEC que se publicó en el BOE de 8 de enero de 2000 remitía al art. 770; la corrección de errores del BOE de 14 de abril de 2000 lo hizo al art. 775, y la publicada en el BOE de 28 de julio de 2001 vuelve a remitirse al art. 770 LEC de acuerdo con la publicación inicial de la Ley.

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

AL TRIBUNAL DE INSTANCIA [ELEGIR: SECCIÓN CIVIL / SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD] DE [LOCALIDAD]

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, en la representación que ostento de Dña. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD],calle [CALLE] n.º [NÚMERO],provista de D.N.I. núm.- [DNI/NIE], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], bajo dirección letrada de D./Dña. [NOMBRE Y APELLIDOS], ejerciente en el Iltre. Colegio de Abogados de [COLEGIO], y con despacho abierto en calle [CALLE] n.º [NÚMERO],ante el Tribunal comparezco, y como mejor proceda en Derecho, DIGO:

Que por medio del presente escrito vengo a formular demanda en solicitud de eficacia civil de la sentencia de nulidad matrimonial dictada por el TRIBUNAL ECLESIÁSTICO de [LOCALIDAD] en fecha [FECHA], en causa canónica n.º [NÚMERO]/[AÑO], a instancias de mi representada contra su marido D. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], calle [CALLE] número [NÚMERO], y frente al MINISTERIO FISCAL, con base en los siguiente hechos y fundamentos de derecho:

HECHOS

PRIMERO.- Mi representada contrajo matrimonio canónico con D. [NOMBRE Y APELLIDOS], el [FECHA] en la localidad de [LOCALIDAD], inscrito en el Registro Civil de [LOCALIDAD], según certificación de matrimonio que se acompaña (DOCUMENTO N.º [NÚMERO])

SEGUNDO.- De dicho matrimonio no ha habido descendencia.

TERCERO.- Presentada demanda de nulidad matrimonial ante el Tribunal Eclesiástico de [LOCALIDAD] en fecha [FECHA], ha recaído sentencia en fecha anteriormente referida ante la imposibilidad de continuar con el matrimonio por defecto de consentimiento al quedar demostrada la reserva mental del esposo respecto de las propiedad esenciales de aquél, acreditándose con el testimonio literal de la misma que se acompaña como DOCUMENTO N.º [Nº DE DOCUMENTO]

CUARTO.- Se solicitan como medidas definitivas, la constancia registral del fallo civilmente eficaz, y de atribución de uso y disfrute del domicilio conyugal. A la acreditación de su fundamento se adjuntan documentos patrimoniales y de ingresos fiscales del esposo (DOCUMENTOS Nos. [Nº DE DOCUMENTO])

FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN Y COMPETENCIA

Es competente ese Tribunal al ser el lugar del domicilio conyugal, conforme al art. 769.1 LEC, ostentando competencia genérica (art. 9.2 LOPJ) y objetiva (art. 85 LOPJ y 45 LEC).

II.- LEGITIMACIÓN Y POSTULACIÓN

Ostenta legitimación activa esta parte como titular del derecho (art. 10 párrafo 1.º LEC) derivado del art. 80 CCiv, para el que las resoluciones de los Tribunales Eclesiásticos tendrán eficacia en el orden civil, a solicitud de cualquiera de las partes, y la legitimación pasiva del esposo deriva de tal carácter de parte en el proceso canónico de nulidad, siendo la legitimación pasiva extraordinaria del Ministerio Fiscal conforme al art. 749.1 LEC.

Comparece esta parte debidamente representada por procurador de los tribunales y dirigida por abogado ejerciente, como exigen los arts. 23, 31 y 750 LEC.

III.- PROCEDIMIENTO

El establecido en el art. 778 LEC, para el conocimiento de la solicitud de eficacia civil y también para conocimiento de solicitud de la medida de atribución de uso de vivienda familiar, con base en el pronunciamiento necesario que previene el art. 91 CCiv, y por lo tanto el trámite del art. 770 LEC al que se remite aquél.

IV.- FONDO

Conforme dispone el art. 80 CCiv las resoluciones dictadas por los Tribunales eclesiásticos sobre nulidad de matrimonio canónico o las decisiones pontificias sobre matrimonio rato y no consumado tendrán eficacia en el ordenamiento civil, a solicitud de cualquiera de las partes, si se declaran ajustados al derecho del Estado en resolución dictada por el Juez civil competente [ÓRGANO JUDICIAL].

La medida definitiva solicitada se justifica en los criterios legales del art. 96 CCiv, puesto que en defecto de acuerdo, puede determinarse que el uso de la vivienda familiar quede para uno de los cónyuges, si lo aconsejan las circunstancias, y su interés fuera el más necesitado de protección, y debe tenerse en cuenta que mi mandante es cotitular de la vivienda porque se adquirió para la sociedad de gananciales que se disuelve con la eficacia civil de la sentencia firme de nulidad del matrimonio, que el esposo ha salido hace tiempo del domicilio conyugal, y que mientras que éste detenta medios económicos holgados, mi mandante carece de rentas y de capacitación profesional para conseguirlas a medio plazo [OTROS DATOS] (etc)

La inscripción registral es más un efecto necesario de la estimación de la solicitud, según interpretación armónica de los arts. 80, 102 y 106 CCiv, 755 LEC, y 76 Ley del Registro Civil y arts. 263 y ss. del Reglamento de ésta.

V.- COSTAS

Por aplicación del principio del vencimiento en punto a la costas procesales (art. 394 LEC), se debe condenar al demandado si se resiste a la demanda, dado que el obtener la razón precisando de un proceso no ha de suponer una merma patrimonial del que tiene razón.

Por todo cuanto antecede,

SUPLICO AL TRIBUNAL

que, por presentada esta demanda, con sus copias y documentos que acompaño, se sirva tenerme por comparecido y parte en la representación que ostento de Dña. [NOMBRE Y APELLIDOS], se admita a trámite, y se entiendan conmigo las sucesivas diligencias, deducida demanda en solicitud de eficacia civil de la sentencia firme dictada por el Tribunal Eclesiástico de [LOCALIDAD] de fecha [FECHA], por la que se declaraba la nulidad del matrimonio canónico de los esposos Dña. y D. [NOMBRE Y APELLIDOS], y se venga a dictar auto por el que se tenga la meritada resolución eclesiástica por ajustada al Derecho del Estado y se declare su eficacia en el orden civil, librando mandamiento para la inscripción de la parte dispositiva de tal auto y de la sentencia canónica en el Registro Civil, y se atribuya por término de diez años a la esposa el uso y disfrute exclusivo de la vivienda conyugal sita en [LOCALIDAD] calle [CALLE] n.º [NÚMERO] puerta [PUERTA] letra [LETRA], con condena en costas del demandado si entablara oposición.

Por ser de justicia, así lo solicita en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a
