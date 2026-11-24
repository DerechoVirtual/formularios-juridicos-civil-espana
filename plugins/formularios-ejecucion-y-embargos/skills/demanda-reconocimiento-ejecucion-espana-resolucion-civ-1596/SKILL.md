---
name: demanda-reconocimiento-ejecucion-espana-resolucion-civ-1596
description: "Demanda de reconocimiento y ejecución en España de resolución extranjera con convenio. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de reconocimiento y ejecución en España de resolución extranjera con convenio

> Formulario **CIV-1596** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de reconocimiento y ejecución en España de resolución extranjera con convenio» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de reconocimiento y ejecución en España de resolución extranjera con convenio” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:demanda-reconocimiento-ejecucion-espana-resolucion-civ-1596`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (9 veces)
- [ ] CONVENIO APLICABLE (6 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] SEDE (4 veces)
- [ ] NÚMERO (3 veces)
- [ ] PAÍS (3 veces)
- [ ] AÑO (2 veces)
- [ ] CALLE (2 veces)
- [ ] DÍA (2 veces)
- [ ] FECHA (2 veces)
- [ ] LUGAR (2 veces)
- [ ] MES (2 veces)
- [ ] COLEGIO
- [ ] CONTENIDO DE LA RESOLUCIÓN A EJECUTAR
- [ ] CONTENIDO DEL CONVENIO
- [ ] DESCRIBIR
- [ ] IDENTIFICACIÓN DEL PROCESO
- [ ] IDIOMA
- [ ] MEDIDAS DE EJECUCIÓN
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] NORMATIVA PROCESAL APLICABLE
- [ ] Nº
- [ ] Nº DE DOCUMENTO
- [ ] PARTE DISPOSITIVA DE LA SENTENCIA
- [ ] TIPO DE PROCEDIMIENTO
- [ ] ÓRGANO JUDICIAL EXTRANJERO

## Normas que cita el formulario

- art. 22.1 LOPJ
- art. 85.5 LOPJ
- art. 276 LOPJ

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…dictada por la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Notas al pie del formulario original:
(1) Conforme al régimen general, la competencia para conocer de las solicitudes de reconocimiento y ejecución de sentencias y demás resoluciones judiciales extranjeras corresponde a los Tribunales de Instancia del domicilio de la parte frente a la que se solicita el reconocimiento o ejecución, o del domicilio de la persona a quien se refieren los efectos de aquéllas; determinándose subsidiariamente la competencia territorial por el lugar de ejecución o donde aquellas sentencias y resoluciones deban producir sus efectos, aunque se exceptúan los casos en que por Tratado corresponda conocer a un órgano jurisdiccional diferente.

(2) El procedimiento se ajustará a lo dispuesto en el convenio aplicable suscrito por España. Y en lo no dispuesto en él, el procedimiento de exequatur se desarrollará según lo dispuesto en los arts. 41 a 55 LCJI.

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

HECHOS
FUNDAMENTOS DE DERECHO

Modelo general de demanda de reconocimiento y ejecución en España de sentencia extranjera cuando existe convenio internacional.

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

Don [NOMBRE Y APELLIDOS], Procurador de los Tribunales, en representación de [NOMBRE DEL REPRESENTADO/A], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], y con la intervención del Letrado que suscribe, colegiado n.º [NÚMERO] del Ilustre Colegio de Abogados de [COLEGIO], ante el Tribunal comparezco y, como mejor proceda en Derecho, DIGO:

Que por medio del presente escrito formulo SOLICITUD DE RECONOCIMIENTO y en su caso EJECUCIÓN DE LA SENTENCIA EXTRANJERA dictada por la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº] la circunscripción judicial de [LOCALIDAD] (se indicará el órgano jurisdiccional extranjero de que se trate) [ÓRGANO JUDICIAL EXTRANJERO], en procedimiento judicial de [TIPO DE PROCEDIMIENTO] entre D.ª A [NOMBRE Y APELLIDOS] y D. B [NOMBRE Y APELLIDOS], con domicilio accidental en dicha población, calle [CALLE], siendo que, actualmente D. B [NOMBRE Y APELLIDOS] lo tiene en Madrid, calle [CALLE] (se indicará el domicilio en España).

Fundamento la solicitud en los siguientes hechos y consideraciones jurídicas:

HECHOS

PRIMERO.- Antecedentes.

En fecha [FECHA], el Tribunal de Instancia (Sección Civil, plaza n.º ero) [NÚMERO] de la circunscripción judicial de [LOCALIDAD] (República de [PAÍS]), dictó sentencia firme y ejecutoria cuya parte dispositiva dice: ‘ [PARTE DISPOSITIVA DE LA SENTENCIA] ‘, o sea, se trata de ejecutar y dar cumplimiento a la resolución judicial que dispone [CONTENIDO DE LA RESOLUCIÓN A EJECUTAR] (se identificará el proceso en el que se dictó la sentencia cuya ejecución en España se solicita) [IDENTIFICACIÓN DEL PROCESO].

Se acompaña como documento número 1 testimonio literal de la referida sentencia con indicación de que la misma es firme y ejecutoria; y como documento número 2 su correspondiente traducción al español por el Traductor Intérprete Jurado D. [NOMBRE Y APELLIDOS], con las oportunas legalizaciones realizadas por las autoridades diplomáticas (el requisito de la legalización no es necesario cuando el correspondiente país ha suscrito el Convenio de La Haya de 5 de octubre de 1961, sobre supresión de la exigencia de la legalización de los documentos públicos extranjeros. En ese caso se expresará: Se acompaña como documento número 1 testimonio literal de la referida sentencia, según la legislación de dicho Estado, redactada en idioma [IDIOMA], oportunamente apostillado, con indicación de que la misma es firme y ejecutoria; y como documento número 2 su correspondiente traducción al español por el Traductor Intérprete Jurado D. [NOMBRE Y APELLIDOS]).

SEGUNDO.- Cumplimiento de los requisitos legales y procedencia de la ejecución.

Seguido el procedimiento ante el Tribunal de Instancia (Sección Civil, plaza n.º ero) [NÚMERO] de la circunscripción judicial de [LOCALIDAD] (República de [PAÍS]), se han observado todas las prescripciones legales, y si bien no ha comparecido D. B [NOMBRE Y APELLIDOS], fue notificado y emplazado a tales fines, habiéndosele notificado la sentencia cuya ejecución se solicita, con fecha

Se acompaña como documento número 3 copia auténtica del acta de notificación, debidamente apostillada, en el que consta la misma; y como documento número 4, su correspondiente traducción.

(En su caso, se expresará: "En el procedimiento seguido ante el Tribunal de Instancia de [SEDE] se han observado todas las prescripciones legales, habiendo comparecido el demandado, y estando presente en todo el procedimiento, que se llevó a cabo de forma contradictoria")

Por otro lado, la materia sobre la que versa la sentencia no se encuentra entre las competencias exclusivas previtas en el art. 22.1 LOPJ ni existe obstáculo alguno relativo al orden público interno español.

TERCERO.- Convenio internacional aplicable.

La Resolución fue dictada por órgano jurisdiccional competente de un Estado tercero no siendo, por tanto, aplicable el Derecho de la Unión Europea. La normativa marco a aplicar es el convenio [CONVENIO APLICABLE] (se especificará el Convenio que sea aplicable) [CONVENIO APLICABLE].

FUNDAMENTOS DE DERECHO

I.- COMPETENCIA. Son de aplicación los arts. 85.5 LOPJ y 52.1 de la Ley 29/2015, de 30 de julio, de cooperación jurídica internacional en materia civil (LCJI).

En el presente caso, es directamente aplicable el Convenio [CONVENIO APLICABLE] que señala que [CONTENIDO DEL CONVENIO]

II.- PROCEDIMIENTO. El Convenio [CONVENIO APLICABLE] dispone que el procedimiento de solicitud de ejecución (extensible al reconocimiento) se regirá por [NORMATIVA PROCESAL APLICABLE].

III.- CAPACIDAD Y LEGITIMACIÓN.Mi mandante D.ª A [NOMBRE Y APELLIDOS] es española, goza del pleno ejercicio de sus derechos civiles y ostenta interés legítimo para deducir el derecho ante el Estado español.

IV.- FUNDAMENTO LEGAL DE LA PETICIÓN. Resulta aplicable al presente caso el Convenio [CONVENIO APLICABLE] (se especificará el Convenio vinculante para España y el país de origen de la sentencia) [CONVENIO APLICABLE], cumpliéndose todos los requisitos exigidos en el mismo para reconocer fuerza ejecutiva en España a una sentencia extranjera.

Por lo expuesto,

SUPLICO AL TRIBUNAL que, teniendo por presentado este escrito con los documentos que lo acompañan y sus copias, se sirva admitirlo; tenerme por parte en la representación que ostento de D.ª A [NOMBRE Y APELLIDOS], entendiéndose conmigo las sucesivas actuaciones, se tenga por promovida la solicitud de reconocimiento u homologación (y en su caso, ejecución) de sentencia extranjera de fecha [FECHA] dictada por el Tribunal de [LOCALIDAD] sobre [DESCRIBIR], y previa audiencia de la parte contraria y del Ministerio Fiscal por el término legal, se proceda a dictar Auto por el que se reconozca eficacia en España a dicha sentencia extranjera (en su caso, mandando dar cumplimiento a la ejecutoria, a cuyo efecto se ordene [MEDIDAS DE EJECUCIÓN]).

Es Justicia en [LUGAR], a [DÍA] de [MES] de [AÑO].

(Si la parte contraria contra quien se dirige el cumplimiento de la ejecutoria tiene domicilio en el extranjero, se expresará:

"OTROSÍ DIGO: Que debiendo ser oída la parte contra quien se dirige el cumplimiento de la ejecutoria y teniendo su domicilio en el extranjero, a los efectos del art. 54.5 LCJI, para llevar a cabo este trámite ha de cursarse comisión rogatoria en solicitud de cooperación internacional.

En su virtud, conforme a los arts. 276 LOPJ y 177 LEC,

SUPLICO AL TRIBUNAL:Que a los expresados fines se sirva librar comisión rogatoria a la Autoridad Judicial competente de [PAÍS] ( [LOCALIDAD]) y elevarla al Ministerio de Justicia, a fin de que haga llegar esta solicitud a la expresada Autoridad Judicial del Estado requerido, bien por la vía diplomática o directamente si así lo prevén los Tratados internacionales.

Es justicia que pido, en cuanto a principal y otrosí, en [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma de Abogado y número de colegiado: Firma del Procurador:
