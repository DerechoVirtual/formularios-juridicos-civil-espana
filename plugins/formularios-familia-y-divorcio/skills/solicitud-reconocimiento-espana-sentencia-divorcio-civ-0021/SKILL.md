---
name: solicitud-reconocimiento-espana-sentencia-divorcio-civ-0021
description: "Solicitud de reconocimiento en España de una sentencia de divorcio colombiana (Convenio de 1908). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud de reconocimiento en España de una sentencia de divorcio colombiana (Convenio de 1908)

> Formulario **CIV-0021** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Solicitud de reconocimiento en España de sentencia colombiana de divorcio según el convenio España-Colombia de 1908.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud de reconocimiento en España de una sentencia de divorcio colombiana (Convenio de 1908)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud de reconocimiento en España de una sentencia de divorcio colombiana (Convenio de 1908)” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:solicitud-reconocimiento-espana-sentencia-divorcio-civ-0021`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] FECHA (3 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] AÑO
- [ ] CALLE
- [ ] COLEGIO
- [ ] DÍA
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] MES
- [ ] SEDE

## Normas que cita el formulario

- art. 36 LEC
- art. 85.5 LOPJ
- art. 52.1 Ley 29/2015
- art. 5.3 LO 1/2025
- art. 85 CC

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Notas al pie del formulario original:
(1) De suyo no es necesaria la previa inscripción del matrimonio, de cuyo divorcio se trata, en el Registro Civil español, para la homologación de los efectos civiles de la sentencia de divorcio, como argumentó el AAP Madrid de 28 de septiembre de 2007, rec. 662/2007; en sentido análogo, AAP Madrid de 6 de noviembre de 2007, rec. 809/2007, siendo reiteradas las resoluciones del TS que han otorgado el exequátur a pesar de no constar inscrito el matrimonio en el Registro Civil español, AATS de 6 de julio de 2004, rec. 667/2003; 2 de marzo de 2004, rec. 197/2003; 2 de diciembre de 2003, rec. 161/2003; 24 de junio de 2003, rec. 368/2002; 13 de febrero de 2001, rec. 5558/2000. Por tanto, la decisión sobre el exequátur no puede venir negativamente condicionada por la sola circunstancia de que el matrimonio no haya tenido ningún efecto en España, ya que sí lo puede tener su ulterior disolución, en orden a reconocer plena eficacia en nuestro país, para unos u otros fines, al estado civil del solicitante, en cuanto derivado del divorcio dictado por los Tribunales de otro Estado; por otro lado, como dispone el art. 89 CCiv, la disolución del matrimonio por divorcio produce efectos desde la firmeza de la sentencia que así lo declare; por lo que la inscripción carece de efectos constitutivos, tratándose de un reconocimiento registral a fin de dotarla de eficacia frente a terceros.

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

Don [NOMBRE Y APELLIDOS], Procurador de los Tribunales, en representación de Doña [NOMBRE Y APELLIDOS], según acredito mediante la escritura de poder que acompaño, y con la intervención del Letrado que suscribe, colegiado n.º [NÚMERO] del Ilustre Colegio de Abogados de [COLEGIO], ante el Tribunal comparezco y, como mejor proceda en Derecho, DIGO:

Que por medio del presente escrito formulo SOLICITUD DE RECONOCIMIENTO DE LA SENTENCIA de fecha [FECHA], pronunciada por el Tribunal Segundo de Familia de Palmira-Valle del Cauca (República de Colombia), para que pueda dicha sentencia extranjera ser cumplida y en su caso ejecutada en España, con arreglo a lo establecido por el Convenio de 30 mayo de 1908, entre España y Colombia, sobre ejecución de sentencias civiles dictadas por los Tribunales de ambos países, citándose al demandado Don [NOMBRE Y APELLIDOS], domiciliado en la ciudad de [LOCALIDAD], calle [CALLE], número [NÚMERO], a efectos de ser oído tal y como se establece en la normativa aplicable.

Fundamento la solicitud en los siguientes hechos y consideraciones jurídicas:

HECHOS

PRIMERO.- En fecha [FECHA], el Tribunal Segundo de Familia de Palmira-Valle del Cauca (República de Colombia), dictó sentencia declarando disuelto, por divorcio, el matrimonio contraído por Don [NOMBRE Y APELLIDOS] y Doña [NOMBRE Y APELLIDOS]

Se acompañan como documentos números [Nº DE DOCUMENTO] y [Nº DE DOCUMENTO] copia apostillada de la ejecutoria cuyo reconocimiento se pretende, con expresión de su firmeza; y certificado de inscripción del matrimonio en el Registro Civil de dicha localidad.

SEGUNDO.- La sentencia adquirió firmeza en fecha [FECHA] habiéndose dictado como consecuencia de una acción civil ejercitada por mi representada contra Don [NOMBRE Y APELLIDOS], incluída dentro del ámbito de aplicación del Convenio entre España y la República de Colombia para el cumplimiento de las sentencias civiles dictadas por los Tribunales de ambos países de 30 de mayo de 1908, ratificado el 16 de abril de 1909 y publicado en el BOE el 18 de abril de 1909, cumpliéndose todos los requisitos que establece el mismo para que se pueda dar a efecto su reconocimiento y posterior ejecución.

A estos hechos le son aplicables los siguientes:

FUNDAMENTOS DE DERECHO

I.- COMPETENCIA. Es de aplicación lo dispuesto en el art. 36 LEC, en cuanto determina la extensión y límites de la jurisdicción de los tribunales civiles españoles, y el art. 85.5º LOPJ, que atribuye a las Secciones Civiles de los Tribunales de Instancia el conocimiento de las solicitudes de reconocimiento y ejecución de sentencias extranjeras, salvo que por tratado o norma internacional se disponga la competencia de otra Sección o Tribunal.

Es territorialmente competente el Tribunal del domicilio del demandado, por aplicación de lo dispuesto en el art. 52.1 de la Ley 29/2015, de 30 de julio, de cooperación jurídica internacional en materia civil (en lo sucesivo LCJIMC), que establece que la competencia para conocer de las solicitudes de exequátur corresponde a los Tribunales de Instancia del domicilio de la parte frente a la que se solicita el reconocimiento o ejecución, o de la persona a quien se refieren los efectos de la resolución judicial extranjera.

II.- PROCEDIMIENTO. Serán aplicables los arts. 52 y siguientes LCJIMC.

III.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD. Conforme a lo dispuesto en el art. 5.3 LO 1/2025, la presente demanda ejecutiva no está sujeta al requisito de MASC.

IV.- FUNDAMENTO LEGAL DE LA PETICIÓN. Es aplicable al presente caso el Convenio de 30 mayo de 1908, entre España y Colombia, sobre ejecución de sentencias civiles dictadas por los Tribunales de ambos países, de conformidad con su art. 1º, por la naturaleza y materia del acto cuyo exequátur se solicita.

A tenor de dicho Convenio ha de ser controlada la firmeza de la resolución (art. 1º,1), y la conformidad con el orden público del estado requerido (art. 1º,2), debiendo oírse al Ministerio Fiscal (art. 3º); requisitos establecidos por dicho Tratado bilateral que aparecen cumplidos en el caso que se examina, dado que consta la firmeza de la sentencia, cuyo exequátur se pretende, que acordó el divorcio de los cónyuges que intervinieron en el proceso; siendo plena la conformidad con el orden público español, atendido que el art. 85 CCiv establece la posibilidad del divorcio cualesquiera que sean la forma y tiempo de celebración del matrimonio; estando garantizada, de otro lado, la autenticidad de la resolución por la apostilla con la que se ha diligenciado.

Por lo expuesto,

SUPLICO AL TRIBUNAL que, teniendo por presentado este escrito, con los documentos que lo acompañan y sus copias, se sirva admitirlo; tenerme por parte en la representación que ostento de Doña [NOMBRE Y APELLIDOS] entendiéndose conmigo las sucesivas actuaciones y, previa audiencia de la parte contraria y del Ministerio Fiscal por el término legal, se proceda a dictar AUTO por el que se otorgue el exequátur a la Sentencia extranjera referida.

Es Justicia en [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma de Abogado

Firma de Procurador
