---
name: convenio-regulador-divorcio-custodia-compartida-civ-0223
description: "Convenio regulador de divorcio con custodia compartida y liquidación del régimen económico. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Convenio regulador de divorcio con custodia compartida y liquidación del régimen económico

> Formulario **CIV-0223** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Convenio regulador de divorcio con custodia compartida y liquidación del régimen económico» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Convenio regulador de divorcio con custodia compartida y liquidación del régimen económico” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:convenio-regulador-divorcio-custodia-compartida-civ-0223`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (6 veces)
- [ ] AÑO (4 veces)
- [ ] MES (4 veces)
- [ ] TOMO (3 veces)
- [ ] CALLE (2 veces)
- [ ] DÍA (2 veces)
- [ ] FECHA (2 veces)
- [ ] NOMBRE DEL HIJO/A
- [ ] PÁGINA

## Normas que cita el formulario

- art. 81.1 Código Civil

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

En la ciudad de [LOCALIDAD], a [DÍA] de [MES] de dos mil [AÑO]

EXPONEN

I.- Que los comparecientes contrajeron matrimonio civil, en [LOCALIDAD], el día [DÍA] de [MES] de [AÑO] figurando dicho matrimonio inscrito en el Registro Civil de [LOCALIDAD], al tomo [TOMO], página

II.- Que de dicho matrimonio, han nacido y viven dos hijos., nacido el [FECHA] de [MES] de [AÑO], y [NOMBRE DEL HIJO/A], nacido el [FECHA] de [MES] de [AÑO], inscrito el primero en el Registro Civil de [LOCALIDAD], en el tomo [TOMO], página [PÁGINA], y el segundo, en el mismo Registro, tomo [TOMO] página

III.- Debido a la situación de quiebra en la convivencia conyugal, ambos esposos han acordado realizar vidas independientes.

IV. El régimen económico matrimonial es el de gananciales.

V. En cumplimiento de lo establecido en el artículo 86 en relación con el artículo 81.1º el Código Civil, y en el apartado 2º del artículo 777 de la Ley de Enjuiciamiento Civil, se acompañará la presente propuesta, a la demanda de divorcio solicitados de mutuo acuerdo, para su aprobación por la autoridad judicial, y a tal fin:

ACUERDAN

Del consentimiento

Por medio del presente convenio los esposos de modo reflexionado, y previos los asesoramientos que han creído convenientes, se ratifican en la decisión de proceder a la disolución de su vínculo matrimonial y a la liquidación del régimen económico matrimonial.

Del domicilio

Ambos cónyuges, se comprometen a respetar la libertad e independencia tanto profesional como personal del otro, así como la libre fijación de sus domicilios, sin intervenir ni inmiscuirse en modo alguno.

[ELEGIR UNA OPCIÓN: Atribución del uso de la vivienda conyugal / La vivienda que constituye domicilio conyugal lo sea en propiedad / La vivienda que constituye domicilio conyugal sea arrendada]

Patria potestad

La patria potestad se ejercerá conjuntamente por ambos progenitores, que adoptarán de común acuerdo y velando siempre por el interés de los menores, todas las decisiones que les afecten, decidiendo en los casos de falta de acuerdo la autoridad judicial.

Guarda y custodia de los hijos

Respecto a la guarda y custodia de los dos menores, por acuerdo de ambas partes se establece que la misma sea compartida por ambos progenitores, estableciéndose la misma, a falta de acuerdo entre los padres, por periodos mensuales. Ello por considerar esta solución óptima para el buen desarrollo, educación y equilibrio emocional de los dos hijos menores de edad. Es preciso resaltar la proximidad entre los domicilios paterno (calle [CALLE] de [LOCALIDAD]) y materno (calle [CALLE] de [LOCALIDAD]), así como la existencia de paradas de autobús / la cercanía de los mismos del colegio de los menores, lo que facilita que éstos no cambien sus hábitos. Tanto en el domicilio paterno como en el materno, los menores tienen su propia habitación, debidamente acondicionada.

Todo ello se llevará a efecto, dentro de criterios de flexibilidad y atendiendo siempre, prioritariamente, al interés de los hijos y en segundo lugar a las circunstancias y compromisos laborales de los progenitores.

Comunicaciones.- Ambos progenitores podrán comunicarse telefónica y telemáticamente con sus hijos con total libertad, respetándose para este tipo de comunicación el horario de descanso y estudio de los menores.

Regimen de visitas para el progenitor con quien no esté conviviendo el menor

A falta de otro acuerdo entre las partes, el progenitor con quien no estuvieran conviviendo los menores permanecerá dos tardes entre semana con los menores, desde la salida del colegio y/o actividades extraescolares hasta las 20:00 horas en la que serán reintegrados en el domicilio del progenitor que corresponda, así como los fines de semana alternos.

Todo ello se llevará a efecto, dentro de criterios de flexibilidad y atendiendo siempre, prioritariamente, al interés de los hijos.

Periodos vacacionales

A falta de acuerdo entre los progenitores, los periodos vacacionales se disfrutaran del modo siguiente:

Las vacaciones de Navidad, Semana Santa y verano, serán repartidas por mitades entre los progenitores, correspondiendo la elección a la madre en los años pares y al padre en los impares, para las vacaciones de navidad y semana santa.

Con las siguientes puntualizaciones:

- La recogida de los menores será a las 11:00 horas del primer día de vacaciones y finalizará a las 20:00 horas del último día que corresponda al que disfruta del primer periodo, o las 20:00 horas del último día de las vacaciones escolares al que disfrute del segundo periodo.

- En las vacaciones de Navidad, en todo caso, el primer periodo comprenderá Noche Buena y Navidad, y el segundo, Fin de Año y Reyes.

- Las vacaciones de verano comprenderán los meses de Julio y Agosto, y se distribuirán en cuatro quincenas, correspondiendo a la madre elegir en los años impares las dos quincenas que estará con los menores, y al padre en los pares, pudiendo ser consecutivas las referidas quincenas.

Todo ello se llevará a efecto, dentro de criterios de flexibilidad y atendiendo siempre, prioritariamente, al interés de los hijos.

Alimentos y sustento de los hijos

Ambos progenitores acuerdan no establecer pensión alimenticia a favor de los hijos menores, toda vez que se establece una custodia compartida, de tal manera que cada progenitor satisfará los alimentos (manutención y vestido) de los dos menores durante el periodo que convivan con ellos, abonándose por mitades todos los gastos concernientes al colegio y estudios de los menores.

Los gastos extraordinarios de los hijos, de naturaleza médica, farmacéutica, ópticos, odontológicos y demás de carácter médico no cubiertos por la Seguridad Social o seguro médico privado, y los relativos a clases de apoyo o refuerzo escolar que precisen los menores y sean recomendados por los profesores y tutores, serán abonados entre los progenitores por mitades. Cualesquiera otros gastos deberán ser pactados previamente, decidiendo la autoridad judicial en caso de desacuerdo.

El resto de gastos no urgentes que tengan un origen lúdico o académico y no cuenten para su realización con el acuerdo de ambos progenitores deberán abonarse por aquél que determine su realización.

[ELEGIR UNA OPCIÓN: Compensación por desequilibrio / Si no existiera desequilibrio entre las partes / Compensacion por desequilibrio / Si existiera desequilibrio entre las partes / — y además elegir: Liquidación del régimen económico matrimonial / Liquidación del régimen económico de gananciales / Liquidación del régimen económico matrimonial / Sociedad de gananciales liquidada previamente mediante capitulaciones matrimoniales / Inexistencia de bienes gananciales]

Eficacia del convenio

Los presentes acuerdos obligan a las partes comprometiéndose a cumplirlos de buena fe desde la fecha de la firma del presente convenio regulador.

Así mismo se comprometen a ratificarse en el presente convenio ante la Autoridad Judicial, junto con solicitud de divorcio, que a tenor de la legislación vigente solicitarán de mutuo acuerdo.

En prueba de conformidad con todo lo acordado, firman los comparecientes el presente documento por triplicado y en todas sus hojas, en el lugar y fecha indicados en el encabezamiento, quedando un ejemplar para cada cónyuge, y otro a los efectos de su aportación al Tribunal, junto con la demanda de divorcio.

Fdo.: D. Fdo.: Dª.

========================================================================
