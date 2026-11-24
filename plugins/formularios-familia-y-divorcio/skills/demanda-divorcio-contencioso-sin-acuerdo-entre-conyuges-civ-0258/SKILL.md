---
name: demanda-divorcio-contencioso-sin-acuerdo-entre-conyuges-civ-0258
description: "Demanda de divorcio contencioso sin acuerdo entre los cónyuges. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de divorcio contencioso sin acuerdo entre los cónyuges

> Formulario **CIV-0258** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Demanda de divorcio contencioso (arts. 81 y 86 del Código Civil y 769 y 770 LEC) con petición de medidas definitivas. El modelo incluye, como opcional, la solicitud de compensación por el trabajo doméstico en régimen de separación de bienes (art. 1438 CC). Las medidas provisionales se articulan por otrosí en la misma demanda.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de divorcio contencioso sin acuerdo entre los cónyuges» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de divorcio contencioso sin acuerdo entre los cónyuges” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-divorcio-contencioso-sin-acuerdo-entre-conyuges-civ-0258`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (5 veces)
- [ ] AÑO (4 veces)
- [ ] DÍA (4 veces)
- [ ] MES (4 veces)
- [ ] Nº (4 veces)
- [ ] FECHA (3 veces)
- [ ] SEDE (3 veces)
- [ ] CALLE (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] PISO (2 veces)
- [ ] PUERTA (2 veces)
- [ ] DOMICILIO
- [ ] EDAD
- [ ] ENTIDAD O PROFESIONAL
- [ ] EXPRESAR LAS RAZONES
- [ ] EXPRESAR RAZONES Y CRITERIOS DE CUANTIFICACIÓN
- [ ] FECHAS DE LAS COMUNICACIONES
- [ ] FECHAS DE LAS REUNIONES
- [ ] FOLIO
- [ ] LUGAR DE CELEBRACIÓN
- [ ] NOMBRE Y APELLIDOS DEL CÓNYUGE DEMANDADO
- [ ] NOMBRE Y APELLIDOS DEL CÓNYUGE DEMANDANTE
- [ ] NOMBRE Y APELLIDOS DEL DEMANDADO
- [ ] NOMBRE Y APELLIDOS DEL DEMANDANTE
- [ ] NOMBRE Y APELLIDOS DEL HIJO/A
- [ ] NOMBRE Y APELLIDOS DEL LETRADO/A
- [ ] NOMBRE Y APELLIDOS DEL MEDIADOR/A
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] Nº DE DOCUMENTOS
- [ ] Nº DE PROCEDIMIENTO
- [ ] RÉGIMEN ECONÓMICO MATRIMONIAL
- [ ] SECCIÓN
- [ ] TOMO

## Normas que cita el formulario

- art. 86 Código Civil
- art. 81 Código Civil
- art. 1438 Código Civil
- art. 769 LEC
- art. 85.1 LOPJ
- art. 92 Código Civil
- art. 749.2 LEC
- art. 437.1 LEC
- art. 5 Ley Orgánica 1/2025
- art. 1438 CC

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

A LA SECCIÓN [ELEGIR: CIVIL / DE FAMILIA, INFANCIA Y CAPACIDAD] DEL TRIBUNAL DE INSTANCIA DE [SEDE]

Don/Doña [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, en la representación que ostento de Don/Doña [NOMBRE Y APELLIDOS DEL CÓNYUGE DEMANDANTE], según acredito mediante escritura de poderes que acompaño para su unión a los autos por medio de copia testimoniada, previo cotejo y devolución del original, y bajo la dirección letrada de Don/Doña [NOMBRE Y APELLIDOS DEL LETRADO/A], ante la Sección [ELEGIR: Civil / de Familia, Infancia y Capacidad] del Tribunal de Instancia de [SEDE] que por turno de reparto corresponda, comparezco y como mejor proceda en Derecho, DIGO:

Que siguiendo instrucciones de mi poderdante, por medio del presente escrito interpongo, en su nombre, DEMANDA DE DISOLUCIÓN MATRIMONIAL POR DIVORCIO contra Doña/Don [NOMBRE Y APELLIDOS DEL CÓNYUGE DEMANDADO], vecino/a de la localidad de [LOCALIDAD], con domicilio en [DOMICILIO], la cual baso en los siguientes

HECHOS

PRIMERO.- Mi representado/a y su cónyuge, ahora demandado/a, contrajeron matrimonio en forma [ELEGIR: civil / religiosa] el día [DÍA] del mes de [MES] del año [AÑO], en [LUGAR DE CELEBRACIÓN], según acredito mediante certificación literal del Registro Civil de [LOCALIDAD] que acompaño como documento núm. uno, constando inscrito el mismo en el Tomo [TOMO], Folio [FOLIO], Sección [SECCIÓN].

[OPCIONAL — incluir si el matrimonio es canónico] Se acompaña asimismo certificación eclesiástica del matrimonio.

SEGUNDO.- Del referido matrimonio nació y vive un único hijo/a, [NOMBRE Y APELLIDOS DEL HIJO/A], nacido/a el día [DÍA] del mes de [MES] del año [AÑO], por lo que en la actualidad tiene [EDAD] años de edad y es, por tanto, menor de edad. En prueba de lo manifestado acompaño certificación literal del Registro Civil como documento núm. dos.

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— Divorcio tras separación judicial previa. TERCERO.- En virtud de sentencia firme de separación fechada el día [DÍA] del mes de [MES] del año [AÑO], dictada por la Sección [ELEGIR: Civil / de Familia, Infancia y Capacidad] del Tribunal de Instancia núm. [Nº] de [SEDE], en autos [Nº DE PROCEDIMIENTO], aprobatoria del convenio regulador de fecha [FECHA], los esposos están separados judicialmente. En prueba de lo manifestado acompaño testimonio de la sentencia como documento núm. tres, la cual fue debidamente inscrita en el Registro Civil, como consta en la certificación literal del Registro Civil señalada como documento núm. uno, por lo que es indudable que se dan los requisitos establecidos en el art. 86 del Código Civil para el divorcio. Todo ello sin perjuicio de que determinados desacuerdos puntuales sobrevenidos hacen imposible plantear ahora la demanda de divorcio de mutuo acuerdo.

— Divorcio directo, sin separación previa. TERCERO.- Han transcurrido más de tres meses desde la celebración del matrimonio, por lo que, teniendo mi mandante la voluntad de disolver el matrimonio, concurre la causa establecida en el art. 86 en relación con el art. 81 del Código Civil.

CUARTO.- El que fue domicilio conyugal, que actualmente ocupan [ELEGIR: el cónyuge demandado y el hijo común / OTRA SITUACIÓN], es el sito en la localidad de [LOCALIDAD], calle [CALLE], núm. [Nº], piso [PISO], puerta [PUERTA]. Mi representado/a tiene su domicilio en [LOCALIDAD], calle [CALLE], núm. [Nº], piso [PISO], puerta [PUERTA].

QUINTO.- El régimen económico del matrimonio es el de [RÉGIMEN ECONÓMICO MATRIMONIAL], debido a las siguientes razones: [EXPRESAR LAS RAZONES].

SEXTO.- Con relación a las medidas o efectos derivados del divorcio, paso a manifestar lo siguiente: [FUNDAMENTAR Y JUSTIFICAR, DOCUMENTALMENTE A SER POSIBLE, LAS MEDIDAS PROPIAS DEL DIVORCIO QUE SE SOLICITAN, A MODO SEMEJANTE AL SUPUESTO DE DEMANDA DE SEPARACIÓN. Cuando existe sentencia de separación previa, la variación de las medidas comunes respecto de las ya dictadas debe basarse en una alteración sustancial de las circunstancias tenidas en consideración].

[OPCIONAL — incluir si se reclama compensación por trabajo doméstico en régimen de separación de bienes] La parte actora ha contribuido a las cargas del matrimonio exclusivamente con el trabajo realizado para la casa, por lo que le corresponde la compensación del artículo 1438 del Código Civil, que se cuantifica en [IMPORTE] euros por las razones siguientes: [EXPRESAR RAZONES Y CRITERIOS DE CUANTIFICACIÓN]. Según la doctrina jurisprudencial, el derecho a obtener la compensación por haber contribuido uno de los cónyuges a las cargas del matrimonio con trabajo doméstico en el régimen de separación de bienes requiere que, habiéndose pactado este régimen, se haya contribuido a las cargas del matrimonio solo con el trabajo realizado para la casa, excluyéndose que sea necesario para obtener la compensación que se haya producido un incremento patrimonial del otro cónyuge (STS de 14 de julio de 2011).

SÉPTIMO.- La parte actora manifiesta que, previo a la presentación de la presente demanda, se llevaron a cabo diversos esfuerzos de negociación con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria.

Entre las acciones realizadas, se incluyen el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS DE LAS COMUNICACIONES], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución; así como la participación en reuniones llevadas a cabo los días [FECHAS DE LAS REUNIONES], cuyos objetivos fueron buscar una conciliación respecto de las diferencias planteadas.

Se adjuntan como prueba copias de las comunicaciones enviadas y recibidas durante el proceso de negociación, incluidas cartas, correos electrónicos y/o actas de reuniones, como documentos números [Nº DE DOCUMENTOS].

Ambas partes, finalmente, acudieron a un medio adecuado de solución de controversias, en cumplimiento de las disposiciones legales aplicables. En este sentido, se participó en el procedimiento de mediación familiar ante el mediador Don/Doña [NOMBRE Y APELLIDOS DEL MEDIADOR/A], elegido por ambas partes, en fecha [FECHA], sin que se haya logrado un acuerdo definitivo.

A su justificación se adjunta acta de no conciliación emitida por [ENTIDAD O PROFESIONAL], de fecha [FECHA], que acredita que las partes acudieron al medio adecuado de solución de controversias sin alcanzar un acuerdo, como documento nº [Nº].

A los anteriores hechos le son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

I. Legitimación activa y pasiva. La ostentan ambas partes por su condición de cónyuges del matrimonio cuya disolución por divorcio se solicita, en relación con la causa legal invocada.

II. Competencia. Es competente este Tribunal al que tengo el honor de dirigirme, de conformidad con lo previsto en el artículo 769 de la LEC, en relación con lo dispuesto en el art. 85.1º LOPJ, por [FUNDAR LA COMPETENCIA: ÚLTIMO DOMICILIO CONYUGAL O DOMICILIO DEL DEMANDADO O DEL DEMANDANTE, SEGÚN CORRESPONDA].

III. Disolución por divorcio. Artículo 86 del Código Civil en relación con el art. 81 en la redacción dada por la Ley 8/2021, de 2 de junio.

IV. Efectos derivados o medidas. Artículos 91 y siguientes del Código Civil. [AÑADIR LOS DEMÁS FUNDAMENTOS QUE EN SU CASO PROCEDIEREN E INVOCAR LA JURISPRUDENCIA Y DOCTRINA CORRESPONDIENTES].

V. Audiencia del menor. La audiencia del menor es preceptiva, conforme a lo previsto en el artículo 92 del Código Civil, especialmente en virtud de los criterios establecidos por la Ley 8/2021, de 2 de junio.

VI. Procedimiento. Son de aplicación los trámites del juicio verbal, conforme a lo establecido en el Capítulo Primero, Título Primero del Libro IV de la LEC, y con sujeción, además, a las reglas establecidas en el artículo 770 de la misma ley.

VII. Intervención del Ministerio Fiscal. Procede la intervención del Ministerio Fiscal, por existir un hijo menor de edad, conforme a lo previsto en el artículo 749.2 de la LEC.

VIII. Cumplimiento de los requisitos de procedibilidad. La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC en relación con el art. 437.1 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

IX. Costas. Artículo 394 de la LEC.

X. Demás normas concordantes y de aplicación: iura novit curia.

En su virtud,

SUPLICO AL TRIBUNAL: Que tenga por presentado este escrito con los documentos acompañados y sus copias; admita todo ello; por interpuesta por el Procurador/a que suscribe, con quien se entiendan las sucesivas diligencias, en nombre y representación de Don/Doña [NOMBRE Y APELLIDOS DEL DEMANDANTE], con devolución de la escritura de poderes una vez quede testimonio en autos, DEMANDA DE DISOLUCIÓN MATRIMONIAL POR DIVORCIO contra Don/Doña [NOMBRE Y APELLIDOS DEL DEMANDADO]; y previa notificación y emplazamiento, y por los trámites procesales pertinentes, con intervención del Ministerio Fiscal y audiencia del menor, dicte sentencia por la que, dando lugar a dicha disolución del matrimonio, determine como medidas o efectos derivados de la misma los siguientes: [ARTICULAR LAS MEDIDAS, EN SU CASO CON CARÁCTER ALTERNATIVO O SUBSIDIARIO].

[OPCIONAL — incluir si se reclama la compensación del art. 1438 CC] Condene a la parte demandada a abonar a la actora la cantidad de [IMPORTE] euros en concepto de compensación por el trabajo realizado para la casa, conforme al artículo 1438 del Código Civil.

Y con condena en costas a la parte demandada, si concurrieren las circunstancias previstas en el artículo 394 de la Ley de Enjuiciamiento Civil.

Es justicia que insto en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firmas de Letrado/a y Procurador/a.
