---
name: demanda-reconocimiento-ejecucion-sentencia-suiza-civ-0313
description: "Demanda de reconocimiento y ejecución de sentencia suiza de divorcio (tratado de 1896). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de reconocimiento y ejecución de sentencia suiza de divorcio (tratado de 1896)

> Formulario **CIV-0313** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de reconocimiento y ejecución de sentencia suiza de divorcio (tratado de 1896)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de reconocimiento y ejecución de sentencia suiza de divorcio (tratado de 1896)” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-reconocimiento-ejecucion-sentencia-suiza-civ-0313`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (9 veces)
- [ ] FECHA (5 veces)
- [ ] CALLE (4 veces)
- [ ] FOLIO (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] NOMBRE DEL HIJO/A (2 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] SEDE (2 veces)
- [ ] AÑO
- [ ] COLEGIO
- [ ] DENOMINACIÓN SOCIAL
- [ ] DÍA
- [ ] ENTIDAD BANCARIA
- [ ] IMPORTE EN CIFRA
- [ ] LIBRO
- [ ] LUGAR
- [ ] MES
- [ ] Nº
- [ ] SUCURSAL
- [ ] TOMO

## Normas que cita el formulario

- art. 41 Ley 29/2015
- art. 85.1 LOPJ
- art. 749.2 LEC
- art. 755 LEC

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

### Avisos de actualización (3) — se aplican en el texto, nunca se copian en el documento

- Junto a «…MILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.
- Junto a «…uzgado de Primera Instancia ante el cual se interponga la demanda de exequatur".»: el texto legal citado entre comillas es la redacción anterior a la LO 1/2025; hoy esas competencias corresponden a la Sección Civil del Tribunal de Instancia. Fuente: LO 1/2025 (BOE-A-2025-76).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Notas al pie del formulario original:
(1) Las sentencias dictadas por los tribunales suizos son ejecutables directamente en España, en virtud de lo acordado en el Tratado entre España y Suiza de 19 de noviembre de 1896 sobre ejecución recíproca de sentencias o fallos en materia civil y comercial ratificado el 6 de julio de 1898.

En dicho Tratado se establece en el art. 1.º la ejecutoriedad de las sentencias o fallos, pudiéndose pedir, conforme al art. 2.º, directamente al órgano judicial español que tenga competencia para la ejecución (con referencia a este tratado la doctrina ha manifestado la ambigüedad del precepto -que confiere la competencia al Juez del lugar donde la sentencia deba ser ejecutada- el cual, no obstante, ha sido interpretado por el Tribunal Supremo en el sentido de atribuir la competencia a los Jueces de Primera Instancia) acompañando al escrito inicial el testimonio literal de la sentencia, debidamente legalizado por el representante consular o diplomático del país en el que se pide el cumplimiento, un documento en el que se acredite que la parte contraria ha sido debidamente citada y se le ha notificado el fallo, y una certificación, también legalizada, expedida por el Letrado/a de la Administración de Justicia que ha dictado la sentencia, haciendo constar que la sentencia o fallo es definitiva y ejecutoria por no existir apelación ni oposición.

Conforme a lo dispuesto en el art. 6.º la ejecución únicamente podrá denegarse cuando la resolución dimana de jurisdicción incompetente (caso de sentencia de divorcio dictada sobre cónyuges españoles), que haya sido dictada sin que las partes hayan sido debidamente citadas o legalmente representadas, o si las reglas de Derecho Público del país donde se pide la ejecución se oponen a que la decisión de la jurisdicción extranjera reciba en él su cumplimiento (caso de divorcio en Suiza acordado antes de la reforma de Código Civil de 1981).

Por lo tanto, en la actualidad, cualquier sentencia de separación o divorcio dictada en Suiza en un matrimonio de español con extranjera, o viceversa, puede ser ejecutada directamente en España.

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

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE]

HECHOS
FUNDAMENTOS DE DERECHO

Modelo de demanda de reconocimiento y ejecución en España de sentencia de divorcio cuando existe tratado bilateral.

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE]

Don [NOMBRE Y APELLIDOS], Procurador de los Tribunales, en representación de D.ª [NOMBRE Y APELLIDOS], mayor de edad, divorciada, con domicilio en Madrid, calle [CALLE], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº uno, y con la intervención del Letrado que suscribe, colegiado n.º [NÚMERO] del Ilustre Colegio de Abogados de [COLEGIO], ante el Tribunal comparezco y, como mejor proceda en Derecho, DIGO:

Que por medio del presente escrito formulo SOLICITUD DE EJECUCIÓN EN ESPAÑA DE LA SENTENCIA EXTRANJERA dictada por el Tribunal de Instancia de Basilea (Confederación Helvética) con fecha [FECHA], en procedimiento judicial de divorcio entre los cónyuges D. y D.ª [NOMBRE Y APELLIDOS].

Fundamento la solicitud en los siguientes hechos y consideraciones jurídicas:

HECHOS

PRIMERO.- Mi representada, D.ª [NOMBRE Y APELLIDOS], estuvo casada con D. [NOMBRE Y APELLIDOS], de nacionalidad suiza, con domicilio en dicho país, calle [CALLE] de la ciudad de Basilea, habiendo contraido matrimonio en la dicha ciudad de Basilea con fecha [FECHA], estando inscrito dicho matrimonio en el Registro Civil Central en el folio [FOLIO] del libro [LIBRO], conforme se acredita con la certificación de dicha inscripción que se acompaña como documento número dos [Nº DE DOCUMENTO].

SEGUNDO.- Que de dicha unión nacieron y viven dos hijos menores de edad, llamados [NOMBRE DEL HIJO/A] y [NOMBRE DEL HIJO/A], como se acredita con sendas certificaciones de nacimiento aportadas como documentos tres y cuatro.

Dichos menores residen con su madre en España.

TERCERO.- En fecha [FECHA], el Tribunal de Instancia de Basilea (Confederación Helvética), dictó sentencia que concede el divorcio de ambos cónyuges.

Se acompaña como documento número cinco testimonio literal de la referida sentencia; y como documento número seis su correspondiente traducción al castellano por el Traductor Intérprete Jurado D. [NOMBRE Y APELLIDOS], con la oportuna legalización realizada por el Cónsul General de España en Basilea.

CUARTO.- Seguido el procedimiento ante el Tribunal de Instancia de Basilea, se han observado todas las prescripciones legales, habiendo comparecido el esposo D. [NOMBRE Y APELLIDOS], y estando presente en todo el procedimiento, que se llevó a cabo de forma contradictoria.

Se acompaña como documento número siete certificación del Tribunal, debidamente legalizada; y como documento número ocho, su correspondiente traducción.

QUINTO.- La sentencia cuya ejecución se solicita fue notificada a la parte demandada con fecha [FECHA], y en la actualidad es firme y ejecutoria, como se acredita con la certificación del Letrado/a de la Administración de Justicia de Instancia de Basilea (documento número nueve), legalizada por el Cónsul General de España en dicha ciudad suiza, y su correspondiente traducción (documento número diez [Nº DE DOCUMENTO]).

SEXTO.- Que estando inscrito el matrimonio en el Registro Civil Central del Ministerio de Justicia, es preciso que se haga la anotación marginal correspondiente donde figure el divorcio de los contrayentes.

SÉPTIMO.- Que en la mencionada sentencia se establece, entre otros pronunciamientos, que el padre abonará como alimentos para los hijos menores, la cantidad de [IMPORTE] francos suizos al mes, sin que hasta el momento D. haya abonado cantidad alguna, a pesar de que han transcurrido ya once meses desde que la sentencia adquirió firmeza, por lo que adeuda la cantidad de [IMPORTE] francos suizos.

OCTAVO.- La resolución fue dictada por órgano jurisdiccional competente suizo no siendo, por tanto, aplicable el Derecho de la Unión Europea. Por encontrase dentro de su ámbito de aplicación la materia objeto de resolución, la ejecución se ajustará a lo dispuesto en el Tratado bilateral entre España y Suiza sobre ejecución de Sentencias en materia civil y comercial hecho en Madrid el 10 de noviembre de 1896.

En lo no dispuesto en él, el procedimiento de exequatur se desarrollará según lo dispuesto en los arts. 41 a 55 de la Ley 29/2015, de 30 de julio, de cooperación jurídica internacional en materia civil (LCJI).

FUNDAMENTOS DE DERECHO

I.- El artículo 1.º del Tratado de 19 de noviembre de 1896 entre España y la Confederación Helvética, por el cual se establece la ejecutoriedad de las sentencias o fallos de los Tribunales de ambos países.

II.- El art. 22. e) LOPJ que dispone que los jueces y Tribunales del orden civil son competentes, con carácter exclusivo y con preferencia de cualquier otro, para reconocer y ejecutar en territorio español las resoluciones judiciales dictadas en el extranjero.

Y en virtud del art. 52.1 LCJI "la competencia para conocer de las solicitudes de exequatur corresponde a los Juzgados de Primera Instancia del domicilio de la parte frente a la que se solicita el reconocimiento o ejecución, o de la persona a quien se refieren los efectos de la resolución judicial extranjera. Subsidiariamente, la competencia territorial se determinará por el lugar de ejecución o por el lugar en el que la resolución deba producir sus efectos, siendo competente, en último caso, el Juzgado de Primera Instancia ante el cual se interponga la demanda de exequatur".

Por otro lado, el art. 85.1º LOPJ, tras la reforma de la LO 1/2025, establece que los Tribunales de Instancia son los órganos judiciales de base en el ámbito civil, asumiendo las competencias que antes tenían los Tribunales de Instancia (Sección Civil).

III.- El artículo 2.º del citado tratado, en donde se establecen los requisitos y condiciones que deben cumplir las sentencias suizas para que puedan ser ejecutadas en España.

IV.- Los demás preceptos del mencionado Tratado, en cuanto hacen referencia a las comunicaciones judiciales y auxilio judicial.

V.- El artículo 749.2 de la LEC en cuanto a que será preceptiva la intervención del Ministerio Fiscal, siempre que alguno de los interesados en el procedimiento sea menor.

VI.- El artículo 755 de la LEC, en lo referente a la comunicación al Registro Civil de las sentencias de divorcio.

VII.- El art. 54.1 LCJI en cuanto a la obligación de las partes de comparecer representadas por procurador y bajo la dirección técnica de letrado.

VIII.- Conforme a lo dispuesto en el art. 46 LCJI se hace constar que no concurren causas de denegación del reconocimiento y en su caso, causas de denegación de ejecución previstas en el art. 6 del Tratado entre España y Suiza.

Por lo expuesto,

SUPLICO AL TRIBUNAL que, admitiendo este escrito con los documentos que lo acompañan y sus copias, se tenga por instada la ejecución de la sentencia de divorcio dictada en fecha [FECHA] por el Tribunal de Instancia de Basilea (Confederación Helvética) y, previa notificación al Ministerio Fiscal, se ACUERDE:

1.º Remitir testimonio de la parte dispositiva de la sentencia donde figura el acuerdo de declarar disuelto, por causa de divorcio, el matrimonio de las partes que figura en el Registro Civil del Ministerio de Justicia, inscrito en el folio [FOLIO] del tomo [TOMO] de la sección de matrimonios.

2.º Requerir a D. [NOMBRE Y APELLIDOS], con domicilio en la ciudad de Basilea para que abone de forma regular la pensión de [IMPORTE EN CIFRA] francos suizos mensuales, bajo los apercibimientos legales.

3.º Requerir igualmente a D. [NOMBRE Y APELLIDOS] para que pague los atrasos de la pensión correspondientes a los once últimos meses, cuya cantidad se eleva a un total de [Nº] francos suizos, bajo el apercibimiento de que de no hacerlo, se procederá al embargo de bienes suficiente para satisfacer el pago de dicha cantidad.

OTROSÍ DIGO que para los requerimientos solicitados en los apartados 2 y 3 del suplico de este escrito, se proceda a remitir exhorto a la Autoridad Judicial que corresponda de la ciudad suiza de Basilea, haciendo constar en el mismo exhorto que en caso de impago, se proceda al embargo de la nómina que percibe D. de la empresa [DENOMINACIÓN SOCIAL] con domicilio en la misma ciudad, calle [CALLE], sin necesidad de nuevo requerimiento por parte de la Autoridad Judicial española.

SUPLICO AL TRIBUNAL se acuerde librar el exhorto a la Autoridad Judicial suiza para los requerimientos solicitados, haciendo constar que los ingresos deberán efectuarse en la cuenta corriente a nombre de la actora, número [NÚMERO] del Banco [ENTIDAD BANCARIA], sucursal [SUCURSAL], sita en Madrid calle [CALLE].

Es Justicia en [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma de Abogado y número de colegiado: Firma del Procurador:
