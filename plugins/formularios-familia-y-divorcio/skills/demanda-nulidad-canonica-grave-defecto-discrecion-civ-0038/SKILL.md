---
name: demanda-nulidad-canonica-grave-defecto-discrecion-civ-0038
description: "Demanda de nulidad canónica por grave defecto de discreción de juicio y prórroga de competencia. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de nulidad canónica por grave defecto de discreción de juicio y prórroga de competencia

> Formulario **CIV-0038** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de nulidad canónica por grave defecto de discreción de juicio y prórroga de competencia» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de nulidad canónica por grave defecto de discreción de juicio y prórroga de competencia” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-nulidad-canonica-grave-defecto-discrecion-civ-0038`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (14 veces)
- [ ] NOMBRE Y APELLIDOS (14 veces)
- [ ] Nº (6 veces)
- [ ] DÍA (3 veces)
- [ ] MES (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] AÑO (2 veces)
- [ ] CALLE (2 veces)
- [ ] CENTRO DE TRABAJO
- [ ] LUGAR
- [ ] NOMBRE DE LA PARROQUIA

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

AL RVDO. TRIBUNAL ECLESIÁSTICO DEL ARZOBISPADO DE [LOCALIDAD]

D./Dª [NOMBRE Y APELLIDOS], Procurador de los Tribunales y de Dña. [NOMBRE Y APELLIDOS], mayor de edad, católica, vecina de [LOCALIDAD], calle [CALLE], nº [NÚMERO], según resulta del Acta de mandato procuratorio y comisión a letrado que se acompaña, ante el Tribunal comparezco y DIGO:

Que en la representación y defensa que ostento y siguiendo instrucciones de mi mandante, interpongo demanda de NULIDAD DEL MATRIMONIO contraído por esta con D. [NOMBRE Y APELLIDOS], mayor de edad, bautizado en la Iglesia Católica, vecino de [LOCALIDAD], calle [CALLE], nº [NÚMERO], C.P., la que se basa y fundamenta en los siguientes:

HECHOS

D. [NOMBRE Y APELLIDOS] y Dª [NOMBRE Y APELLIDOS], contando ambos con [Nº] y [Nº] años de edad, respectivamente, contrajeron formalmente matrimonio canónico en la Parroquia de [NOMBRE DE LA PARROQUIA] de [LOCALIDAD], el [DÍA] de [MES] de

Se adjunta a la presente demanda Partida de matrimonio con número UNO de documentos.

De su unión matrimonial no existen hijos.

Los cónyuges cesaron la convivencia marital transcurridos escasos seis meses de la celebración del matrimonio.

En la actualidad se encuentran Divorciados según Sentencia dictada por el Tribunal de Familia número [NÚMERO] de [LOCALIDAD], en fecha [DÍA] de [MES] de [AÑO]

Adjuntamos bajo número DOS de documentos copia testimoniada de la Sentencia.

Dª [NOMBRE Y APELLIDOS] es educada por sus abuelos maternos con ocasión del fallecimiento de sus padres en un accidente de tráfico. Su infancia se desarrolla en la pedanía de [LOCALIDAD] (). Todos sus recuerdos de la época evocan una grandísima soledad y una gran necesidad afectiva que, por circunstancias, no son cubiertas en el seno de esa familia. Contando con [Nº] años, la joven Dª [NOMBRE Y APELLIDOS], inicia su andadura laboral en [CENTRO DE TRABAJO], de la localidad de [LOCALIDAD] A tal fin, y como requisito para incorporarse al puesto, debe efectuar prácticas durante un mes en la capital. Encontrándose allí es cuando conoce casualmente al joven venezolano, D. [NOMBRE Y APELLIDOS], con quien se encuentra fortuitamente en dos o tres ocasiones por las inmediaciones del centro de trabajo en donde realiza las prácticas y con quien sale en un par de ocasiones.

Finalizadas sus prácticas laborales y ya de regreso en la ciudad de [LOCALIDAD], aparece sorpresivamente el joven D. [NOMBRE Y APELLIDOS] en su centro de trabajo y le pide matrimonio. Era un joven que tenía completamente deslumbrada a Dª [NOMBRE Y APELLIDOS], puesto que era bien parecido y de trato muy dulce. Además, trabajaba como auxiliar de vuelo de una compañía aérea, resultándole ese aspecto también sumamente atrayente. Todo ello, acompañado de una gran inmadurez, una extraordinaria necesidad afectiva y su gran interés por independizarse y viajar, hizo que Dª [NOMBRE Y APELLIDOS] con sus [Nº] años decidiera, de modo tan absurdo e irreflexivo, casarse con aquel desconocido que le prometía una vida color de rosa.

QUINTO: Así, nada más iniciar su vida en común, viajan a [LOCALIDAD] y luego a [LOCALIDAD], e inmediatamente ella empieza a descubrir su grave error. Ni él era todo lo dulce ni caballeroso que parecía ni la relación matrimonial resultaba lo idílica que ella había pensado. Empezó a conocer la realidad de D. [NOMBRE Y APELLIDOS], y ya no se asemejaba en absoluto con la imagen que inicialmente se había forjado. Empezó a conocer la vida real y familiar de D. [NOMBRE Y APELLIDOS] y tampoco resultaba en nada parecida a lo que ella había imaginado.

SEXTO: Constatado su gravísimo error y transcurridos escasos [Nº] meses de haberse celebrado la boda, ella decide romper la convivencia.

SÉPTIMO: Nunca más se recondujo la convivencia ni hubo más trato entre ellos.

OCTAVO: Dª [NOMBRE Y APELLIDOS], transcurridos más de [Nº] años desde aquella ruptura, y convencida de la nulidad de tan irregular matrimonio solicita de la Iglesia su discernimiento en tal declaración.

FUNDAMENTOS DE DERECHO

Los cánones 1.671 y 1.673.2 del Corpus Iuris Canonici (C.I.C.), en relación con el artículo 10 de la Instrucción Pontificia Dignitas Connubii y disposiciones concordantes, que establecen la competencia del Tribunal Eclesiástico al que me dirijo por razón de la materia y territorio, dado que en esta ciudad de la Diócesis de [LOCALIDAD], se celebró el matrimonio canónico entre las partes y resulta el domicilio de la esposa actora, residiendo ambos en territorio de la misma Conferencia Episcopal, solicitando del Tribunal formule solicitud al Vicario Judicial de la Diócesis de [LOCALIDAD], a fin de que otorgue su consentimiento una vez oída la parte demandada. La justificación en la elección del Tribunal del lugar del domicilio de la actora se funda en el hecho de que si bien parece ser que el domicilio del esposo está situado en el referido en el encabezamiento de la presente demanda, no es un dato que podamos confirmar absolutamente, dado que esta parte, pese a intentarlo no ha podido ponerse en contacto con la misma. De igual modo el fuero del domicilio de la actora atiende mejor los motivos de conciencia que presiden su actuar en el presente supuesto, al entender el desinterés del demandado.

El canon 1.674-1, del Corpus Iuris Canonici, en relación con el artículo 92.1 de la Instrucción Pontificia Dignitas Connubii, determina la legitimación de mi representada a impugnar su matrimonio.

El procedimiento adecuado será el establecido para el Juicio contencioso ordinario, al amparo de lo previsto en los cánones 1.501, siguientes y concordantes, del Corpus Iuris Canonici.

Los cánones 1.055 siguientes y concordantes del C.I.C., que tratan del matrimonio cristiano, sus propiedades y, en especial, el canon 1.057 del mismo, que establece que "el matrimonio lo produce el consentimiento de las partes legítimamente manifestado entre personas jurídicamente hábiles, consentimiento que ningún poder humano puede suplir". También el canon 1.057.2 que determina que "El consentimiento matrimonial es el acto de la voluntad por el cual varón y mujer se entregan y aceptan mutuamente en alianza irrevocable para constituir el matrimonio".

V.- El canon 1.095.2 del C.I.C., que establece que es incapaz para contraer matrimonio quien tiene un grave defecto de discreción de juicio acerca de los derechos y deberes esenciales del matrimonio que, mutuamente, se han de dar y aceptar; estableciendo dicho canon, y los siguientes, las circunstancias que debe reunir el consentimiento para que sea válido.

No basta el conocimiento puramente teórico del matrimonio para que la voluntad se decida libremente a abrazarlo, sino que es menester que el contrayente esté dotado, aparte de la facultad cognoscitiva o abstracta, de la llamada facultad crítica (vis crítica) o estimativa; es decir, de la "fuerza de razonar, de estimar o ponderar prácticamente el matrimonio que se va a celebrar, así como las obligaciones inherentes al mimo y los motivos para elegirlo o no".

Así la discreción de juicio debe abarcar no sólo el vínculo matrimonial, sino todos los efectos esenciales que brotan del mismo, así como los derechos y obligaciones que han de ser mutuamente entregados y aceptados por los contrayentes, de modo que dicho objeto sea valorado y elegido libremente.

En la actualidad, se admite que una perturbación de la afectividad puede dejar intacta la función intelectiva y, sin embargo, atacar la volición, afirmando que no se puede excluir necesariamente que haya procesos patológicos de la voluntad independientes del grado de maduración del juicio.

Puede afirmarse que trastornos emocionales pueden destruir la libertad, no sólo cegando previamente el entendimiento, sino también durante la formación del acto formalmente volitivo, impidiendo la ejecución de las órdenes de la voluntad libre. Las motivaciones son necesarias para que haya deliberación y en consecuencia, para que la elección no sea razonable sino, incluso, exista. Puede decirse que las motivaciones siempre condicionan el obrar humano; unas veces posibilitando y facilitando la deliberación/elección y otras veces, imposibilitándolas o dificultándolas.

Las motivaciones pueden ser "conscientes" o "inconscientes" -según dispone Mnsñ. García Failde-; por "inconsciente" se entiende el conjunto de todas las nociones impresiones recuerdos, tendencias, complejos remociones, que no son actualmente conocidas por el individuo, pero que existen influenciando su conducta. Estos contenidos inconscientes están representados o por elementos de experiencia que no han podido alcanzar los niveles de la contienda, (contenidos latentes), o por ideas sentimientos, impulsos, etc…, que por ser incompatibles con las normas socio-culturales del sujeto o del grupo han pasado por un proceso de "remoción" -esto es, han sido rechazados inconscientemente-.

Por su parte, la Rota Romana en estos últimos años viene reconociendo que existen determinadas enfermedades, como la inmadurez afectiva, que atacan directamente a la voluntad, sin lesionar ostensiblemente la inteligencia. Dichas enfermedades, al disminuir gravemente la libertad o suprimirla impiden que se de la suficiente discreción de juicio para contraer matrimonio válidamente.

En la práctica, suele designarse este elemento constitutivo del consentimiento matrimonial con diversas expresiones. Así, a la discreción de juicio se le denomina madurez personal, madurez de juicio, personalidad madura, discernimiento de espíritu, madurez afectiva, facultad crítica, facultad valorativa, facultad estimativa, juicio práctico.

Los cánones 1.481 y siguientes de C.I.C., en relación con los artículos 101 al 113 de la Instrucción Pontificia Dignitas Connubii, que establecen las condiciones que deben reunir los Letrados y Procuradores que intervengan las presentes causas.

En su virtud,

SUPLICO AL TRIBUNAL, que habiendo por presentada esta demanda, la admita, teniéndome por comparecido en la representación que ostento, se sirva dar traslado de la misma al esposo demandado y al Defensor del Vínculo; y en su día, tras recibimiento a prueba en fase de instrucción de la causa y demás trámites legales, dicte sentencia por la que declare la nulidad del matrimonio contraído por la actora con el demandado por los capítulos de Grave defecto de discreción de juicio (c. 1095.2) padecido por la esposa.

PRIMER OTROSÍ DIGO: Que reuniendo quien suscribe los requisitos necesarios para defender y representar a la actora, interesa del Tribunal confiera a su favor la oportuna comisión canónica a tal efecto, SUPLICO DEL RVDO. TRIBUNAL, así se acuerde.

SEGUNDO OTROSÍ DIGO: Que habiéndose interpuesto la presente demanda de nulidad ante los Tribunales Eclesiástico de [LOCALIDAD], de conformidad con lo previsto en el canon 1673.3, se interesa del Rvdo. Tribunal solicite del Vicario Judicial de [LOCALIDAD], su consentimiento previo para la sustanciación del procedimiento y SUPLICO DEL RVDO. TRIBUNAL, acuerde lo oportuno a tal fin.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Fdo.: Proc. y Ltdo.

========================================================================
