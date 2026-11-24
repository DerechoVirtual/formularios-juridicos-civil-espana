---
name: contestacion-demanda-sobre-derechos-articulo-160-civ-0268
description: "Contestación a la demanda sobre los derechos del artículo 160 del Código Civil. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contestación a la demanda sobre los derechos del artículo 160 del Código Civil

> Formulario **CIV-0268** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Escrito de contestación, en juicio verbal, a la demanda de abuelos u otros parientes y allegados que reclaman un régimen de relaciones personales con un menor al amparo del art. 160 del Código Civil (arts. 753 y 405 LEC). El modelo se redacta desde la posición del progenitor titular de la patria potestad que se opone, solicita subsidiariamente una limitación del régimen y propone prueba pericial y testifical.

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contestación a la demanda sobre los derechos del artículo 160 del Código Civil» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contestación a la demanda sobre los derechos del artículo 160 del Código Civil” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:contestacion-demanda-sobre-derechos-articulo-160-civ-0268`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] Nº (4 veces)
- [ ] SEDE (3 veces)
- [ ] DOMICILIO (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL PERITO (2 veces)
- [ ] AÑO
- [ ] DÍA
- [ ] FECHA
- [ ] FECHA O CIRCUNSTANCIA
- [ ] MES
- [ ] NOMBRE DEL MENOR
- [ ] NOMBRE Y APELLIDOS DE LOS ABUELOS DEMANDANTES
- [ ] NOMBRE Y APELLIDOS DEL MENOR
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] NOMBRE Y APELLIDOS DEL PROGENITOR DEMANDADO

## Normas que cita el formulario

- art. 160 Código Civil
- art. 753 LEC
- art. 160.2 Código Civil
- art. 394 LEC
- art. 339.2 LEC

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

- Junto a «…Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.

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

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

Don/Doña [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, en nombre y representación de Doña/Don [NOMBRE Y APELLIDOS DEL PROGENITOR DEMANDADO], titular de la patria potestad del menor [NOMBRE Y APELLIDOS DEL MENOR], con domicilio en [DOMICILIO], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº], ante el Tribunal comparezco y DIGO:

Que habiendo sido demandada/o en juicio verbal promovido por Don/Doña [NOMBRE Y APELLIDOS DE LOS ABUELOS DEMANDANTES] para la efectividad de los derechos reconocidos en el art. 160 del Código Civil, al amparo de los artículos 753 y 405 de la LEC paso a contestar la demanda en base a los siguientes

HECHOS

PRIMERO.- Mi representado/a Doña/Don [NOMBRE Y APELLIDOS], progenitor/a del menor [NOMBRE DEL MENOR], tiene atribuida por sentencia judicial dictada por la Sección Civil del Tribunal de Instancia de [SEDE], de fecha [FECHA], la titularidad exclusiva de la patria potestad del mentado menor (doc. nº 1).

SEGUNDO.- En la citada sentencia se expresa claramente que el otro progenitor, Don/Doña [NOMBRE Y APELLIDOS], queda privado del ejercicio de la patria potestad debido a las graves circunstancias que en la misma se exponen, en especial por cuanto desde el nacimiento del menor se desentendió completamente de sus obligaciones [OPCIONAL — otras circunstancias].

TERCERO.- Al haberse atribuido la patria potestad solo a mi representado/a, este/a ha perdido todo contacto con la familia del otro progenitor, pues aunque sus relaciones anteriores habían sido siempre cordiales, a partir de la sentencia de [ELEGIR: divorcio / separación / medidas paternofiliales] ha dejado de relacionarse con su familia política que, en el largo y problemático proceso, siempre apoyó la actuación y defensa de su ex cónyuge o ex pareja.

En la propia demanda se reconoce que el menor venía sufriendo, desde hace tiempo, la problemática de sus progenitores, y esta y no otra es la causa que justifica la decisión de mi representado/a de no permitir a dichos familiares que se relacionen con el menor.

CUARTO.- Por otra parte, existe un hecho que ha sido omitido y que tiene gran trascendencia, cual es que los demandantes conviven en el mismo domicilio que el progenitor privado de la patria potestad, tal como se acredita por la hoja del padrón municipal que se acompaña (doc. 2).

A estos hechos son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

PRIMERO.- El art. 160.2 del Código Civil, en la redacción dada por la Ley 26/2015, de 28 de julio, establece que «No podrán impedirse sin justa causa las relaciones personales del hijo con sus abuelos y otros parientes y allegados.

En caso de oposición, el Juez, a petición del menor, hermanos, abuelos, parientes o allegados, resolverá atendidas las circunstancias. Especialmente deberá asegurar que las medidas que se puedan fijar para favorecer las relaciones entre hermanos, y entre abuelos y nietos, no faculten la infracción de las resoluciones judiciales que restrinjan o suspendan las relaciones de los menores con alguno de sus progenitores».

SEGUNDO.- No discute esta parte que las relaciones entre los menores y los abuelos, paternos o maternos, son por lo general enriquecedoras y permiten insertar al menor en un entorno familiar completo.

Pero ello no ocurre en este caso, puesto que, frente a las alegaciones de la demanda, en modo alguno los abuelos forman una familia aglutinada y, por lo tanto, no desempeñan el papel fundamental de cohesión y transmisión de valores de la familia que es la finalidad que el precepto invocado persigue.

TERCERO.- Precisamente la circunstancia de que los abuelos demandantes convivan en el mismo domicilio que el progenitor privado de la patria potestad es la que justifica que mi representado/a niegue el derecho de visitas, en tanto que de acceder a esta pretensión permitiría burlar lo acordado en la sentencia antes citada, lo cual resulta proscrito en el art. 160.2, párrafo segundo, del Código Civil, cuando se establece que debe asegurarse especialmente que las visitas no instrumentalicen un incumplimiento de la resolución que priva a dicho progenitor de la patria potestad.

CUARTO.- Por otra parte, frente a lo alegado en la demanda, aporto prueba pericial emitida por Don/Doña [NOMBRE Y APELLIDOS DEL PERITO], psicólogo/a, que viene examinando al menor desde hace tiempo y que desaconseja totalmente el mantenimiento de estas relaciones, puesto que podrían afectar al libre desarrollo de la personalidad del menor; acompaño a dichos efectos informe del citado profesional y la documentación correspondiente a dicho tratamiento como docs. [Nº] a [Nº].

QUINTO.- Que, no obstante, y de accederse a lo solicitado, esta parte interesa que se limiten a dos horas a la semana, que la comunicación no tenga lugar en el domicilio de los demandantes, que se adopten las medidas para que no pueda burlarse la prohibición del progenitor privado de la patria potestad de relacionarse con el menor y, además, que la relación se mantenga en presencia de mi representado/a o, en su defecto, de un miembro de los servicios de asistencia social del Ayuntamiento de [LOCALIDAD].

SEXTO.- Con arreglo a lo establecido en el art. 394 de la LEC procede imponer las costas de este proceso a la parte actora, por ser improcedente la acción ejercitada.

Y por cuanto antecede,

SUPLICO AL TRIBUNAL: Que tenga por contestada la demanda junto con la copia de la misma destinada al Ministerio Fiscal y por efectuado el traslado a la parte actora, según justificante que aporto para unir a los autos, que la admita y que me tenga por personado y parte en la representación que ostento de Doña/Don [NOMBRE Y APELLIDOS], en virtud de la copia electrónica del poder notarial de representación (o digitalizada) general para pleitos, cuya devolución intereso previa unión a los autos de copia testimoniada, que se entiendan conmigo las sucesivas diligencias del juicio verbal para la efectividad de los derechos reconocidos en el artículo 160 del Código Civil, el cual se sustanciará en la forma prevista para el juicio verbal con las especialidades que contiene el capítulo I del título I del Libro IV de la LEC, en especial con intervención del Ministerio Fiscal, y que se señale día y hora para la celebración del juicio verbal con citación a las partes en legal forma, así como que, en su día, se dicte sentencia por la que se desestime la demanda y se declare que Don/Doña [NOMBRE Y APELLIDOS] y Don/Doña [NOMBRE Y APELLIDOS] no tienen derecho a relacionarse con su nieto/a y, subsidiariamente, para el caso de que la pretensión principal no fuera aceptada por el Tribunal, se establezca que el régimen de visitas no podrá ser superior a dos horas semanales y que se realizará siempre en presencia de mi representado/a o, en su defecto, de un miembro de los servicios de asistencia social del Ayuntamiento, adoptándose las medidas que procedan para evitar que se frustre la efectividad de la sentencia dictada por la Sección Civil del Tribunal de Instancia de [SEDE], con condena en costas a la parte actora.

OTROSÍ DIGO: Que interesa a esta parte que se proceda a citar a Don/Doña [NOMBRE Y APELLIDOS DEL PERITO], psicólogo/a, con domicilio en [DOMICILIO], que viene examinando al menor desde [FECHA O CIRCUNSTANCIA], a fin de que se ratifique en los informes aportados, así como para que pueda ofrecer cualquier aclaración que, respecto a sus informes y conclusiones, fuera necesaria.

OTROSÍ PRIMERO DIGO: Que esta parte no se opone a la designación judicial de perito al amparo del art. 339.2 de la LEC, interesada por la parte actora, si bien entiende que el dictamen deberá también tener en cuenta la documentación aportada junto a esta contestación en la que se constatan los exámenes efectuados por el psicólogo Don/Doña [NOMBRE Y APELLIDOS].

OTROSÍ SEGUNDO DIGO: Que manifiesto mi conformidad con la fijación de la cuantía del proceso en indeterminada.

SUPLICO AL TRIBUNAL: que tenga por hechas las manifestaciones precedentes a todos los efectos legales que procedan y que acuerde de conformidad.

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma de Abogado/a y de Procurador/a.
