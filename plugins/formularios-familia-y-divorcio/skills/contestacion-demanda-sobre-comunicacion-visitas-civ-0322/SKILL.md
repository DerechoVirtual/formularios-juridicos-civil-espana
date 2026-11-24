---
name: contestacion-demanda-sobre-comunicacion-visitas-civ-0322
description: "Contestación a la demanda sobre comunicación y visitas de los abuelos con su nieto. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contestación a la demanda sobre comunicación y visitas de los abuelos con su nieto

> Formulario **CIV-0322** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Contestación a la demanda en juicio verbal promovida por los abuelos para que se fije un régimen de comunicación y visitas con su nieto, cuando la madre (que ostenta la guarda) no se opone a la relación pero pide que se establezcan medidas de garantía, en particular por existir una prohibición de aproximación del padre respecto del menor.

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contestación a la demanda sobre comunicación y visitas de los abuelos con su nieto» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contestación a la demanda sobre comunicación y visitas de los abuelos con su nieto” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:contestacion-demanda-sobre-comunicacion-visitas-civ-0322`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] HORA (4 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] FECHA (3 veces)
- [ ] AÑO (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] COLEGIO
- [ ] DOMICILIO
- [ ] DÍA
- [ ] DÍA DE LA SEMANA
- [ ] DÍAS
- [ ] MES
- [ ] NOMBRE Y APELLIDOS DE LA PARTE DEMANDADA
- [ ] NOMBRE Y APELLIDOS DEL LETRADO/A
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] NOMBRE Y APELLIDOS DEL PROGENITOR
- [ ] Nº
- [ ] Nº DE COLEGIADO
- [ ] Nº DE PROCEDIMIENTO
- [ ] NÚMERO
- [ ] SEDE
- [ ] ÓRGANO JUDICIAL

## Normas que cita el formulario

- art. 160 CC
- art. 158.4.º CC
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

- Junto a «…injan o suspendan las relaciones de los menores con alguno de sus progenitores».»: el art. 160 CCiv fue modificado por la Ley 42/2003 y posteriormente por la Ley 8/2021 y otras reformas; comprobar la redacción vigente y la numeración de sus párrafos antes de citarlo literalmente.

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

A LA SECCIÓN CIVIL (SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD) DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, que actúa en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS DE LA PARTE DEMANDADA], como acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento n.º [Nº DE DOCUMENTO], bajo la dirección del Letrado/a D./Dña. [NOMBRE Y APELLIDOS DEL LETRADO/A], colegiado/a n.º [Nº DE COLEGIADO] del Ilustre Colegio de Abogados de [COLEGIO], con despacho abierto en [LOCALIDAD], calle [DOMICILIO], n.º [NÚMERO], en autos de JUICIO VERBAL n.º [Nº DE PROCEDIMIENTO] / [AÑO], promovido por D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS], ante el Tribunal comparezco y, como mejor proceda en Derecho, DIGO:

Que, en la representación que ostento y dentro del plazo legal, vengo a CONTESTAR A LA DEMANDA formulada de adverso, en base a los siguientes hechos y consideraciones jurídicas:

HECHOS

PRIMERO.– De acuerdo con el correlativo de la demanda, sobre el parentesco de los actores con el hijo menor de mi representada, así como sobre la regularidad de las relaciones existentes entre abuelos y nieto hasta la separación de mi mandante de D./Dña. [NOMBRE Y APELLIDOS DEL PROGENITOR].

SEGUNDO.– No podemos sino contradecir las afirmaciones formuladas en el correlativo de la demanda, en cuanto mi mandante siempre ha consentido la continuación de las relaciones de su hijo con sus abuelos después de la separación de los progenitores del menor. Por el contrario, la comunicación del menor con los abuelos ha sido constante, en lo que permitía la crianza del menor y el trabajo de la madre, tanto en casa de los abuelos paternos como mediante estancias fuera de ella, cuando la edad del niño lo ha permitido, y dentro de la mayor flexibilidad, como se acreditará en periodo probatorio.

TERCERO.– Absolutamente incierto. Por más que se empeñen los demandantes, mi representada nunca se ha opuesto al mantenimiento de la relación del menor con sus abuelos, sino que entiende que, por el momento, las comunicaciones con su nieto deben producirse en todo caso sin la presencia de su hijo y padre del menor, en tanto no se depuren sus responsabilidades penales, por entenderlo plenamente justificado por la circunstancia de que el derecho de los abuelos a mantener relaciones con los nietos no sea medio para eludir la prohibición al padre de aproximarse al referido menor, que fue acordada en resolución dictada en [FECHA], cuyo testimonio se adjunta como documento n.º [Nº DE DOCUMENTO].

FUNDAMENTOS DE DERECHO

I.– JURÍDICO-PROCESALES

Conforme con los fundamentos jurídicos I a VI del escrito de demanda, sobre jurisdicción, competencia objetiva y territorial del Tribunal, legitimación y el procedimiento adecuado escogido, compareciendo esta parte con la debida representación técnica y asistencia letrada.

II.– JURÍDICO-MATERIALES

II.1. Del art. 160 CCiv resulta el apoyo normativo a las relaciones personales del nieto con sus abuelos, que solo podrán impedirse por existencia de justa causa que así lo aconseje. Y, así, como se ha referido en los hechos de la contestación, mi patrocinada no se opone a la relación sino que simplemente entiende que tales relaciones deben desarrollarse de forma distinta a la pretendida, estableciéndose medidas de garantía en relación con el menor. Por lo tanto, esta demanda resulta manifiestamente innecesaria en cuanto los actores pueden visitar a su nieto siempre que lo deseen.

Como viene reiteradamente señalando el Tribunal Supremo en esta materia del derecho de los abuelos a relacionarse con sus nietos (SSTS de 7 de abril de 1994, de 11 de junio de 1996, rec. 3446/1991, de 17 de septiembre de 1996, rec. 2631/1992, y de 11 de junio de 1998, rec. 1474/1994), «este tipo de relaciones, que insertan beneficiosamente al menor en su entorno familiar completo, resultan más necesarias cuando de los ascendientes se trata, por su privilegiado grado de parentesco, dado que la personalidad se forja también entre las contradicciones que emanan, a veces de los planteamientos y opiniones de los parientes, siempre que revistan un carácter de normalidad, o sea, no respondan a patologías o ejemplos corruptores». El derecho de los abuelos a relacionarse con sus nietos, en los términos que se acaban de señalar, en tanto que dicha relación beneficia al menor y no puede impedirse sin causa que lo justifique, tiene respaldo jurisprudencial, entre otras, en la STS de 23 de noviembre de 1999, rec. 1048/1995, y las en ella citadas de 11 de junio y 17 de septiembre de 1996.

Frente a ello, lo que se alega es la posibilidad de que, aprovechando estas visitas, el padre del menor se pueda poner en contacto con el mismo, lo cual está en principio suprimido en virtud del auto de [FECHA], en el que se prohíbe al padre aproximarse al referido menor. Y ello con fundamento en lo establecido en el párrafo 3.º del art. 160 CCiv, que dispone que la autoridad judicial «especialmente deberá asegurar que las medidas que se puedan fijar para favorecer las relaciones entre abuelos y nietos no faculten la infracción de las resoluciones judiciales que restrinjan o suspendan las relaciones de los menores con alguno de sus progenitores».

Obviamente, una cosa es el derecho de los abuelos a las visitas al nieto, y otra la supresión del derecho del padre, no pudiendo afectar una a la otra. Por estas razones y no existiendo una causa para suprimir ese derecho de los abuelos y del propio menor, no procede suspender o suprimir el mismo, no obstante lo cual el propio juzgador, ante la posibilidad de que dichas visitas pudiesen servir como pretexto para el incumplimiento de la orden de alejamiento, debe adoptar de una parte unas visitas restringidas y, de otra, unas medidas de garantía, en el sentido de hacer recaer sobre los abuelos la obligación de que en todo caso las comunicaciones se realicen fuera de la presencia del padre. Y así se entiende conveniente, de una parte, establecer como régimen de comunicación entre los actores y el menor, nieto de los mismos, el de una visita semanal, los [DÍA DE LA SEMANA] de [HORA] a [HORA] horas, y dos visitas mensuales los fines de semana, que serán los [DÍAS] alternos de cada mes de [HORA] a [HORA] horas del día, manteniendo dicho régimen también durante los periodos de vacaciones de Navidad, Semana Santa y verano, debiendo velar los abuelos porque las mencionadas comunicaciones con su nieto se realicen en todo caso sin la presencia de su hijo y padre del menor, en tanto no se depuren sus responsabilidades penales; y, de otra, acordar que el referido régimen de visitas se inicie una vez que se compruebe que el padre del menor salga del domicilio de los abuelos; que dicho régimen de visitas sea participado a las Fuerzas y Cuerpos de Seguridad del Estado, a fin de velar por el cumplimiento del auto de fecha [FECHA] dictado por [ÓRGANO JUDICIAL], así como requerir a los abuelos para el cumplimiento de lo acordado en esta resolución, con los apercibimientos legales, y sin perjuicio de adoptar en cualquier momento y en caso de incumplimiento de tales medidas, conforme al art. 158.4.º CCiv, lo que resulte conveniente en interés del menor.

II.2. Las costas procesales deben ser impuestas a la parte demandante, con arreglo al art. 394 LEC, y ello aunque se decreten medidas, puesto que, como se ha expuesto, mi representada no se ha opuesto a la relación entre su hijo y los actores, resultando ser la presentación de esta demanda temeraria por innecesaria.

Por todo lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito, se tenga por contestada en tiempo y forma la demanda interpuesta contra mi mandante por D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS], y por formulada oposición a la pretensión de los actores, se digne admitirla a trámite junto con los documentos acompañados y sus copias, y previo el procedimiento que le corresponda, se dicte sentencia en la que se fije la forma en que han de mantenerse las relaciones entre los demandantes y el hijo de mi representada, estableciéndose las medidas de garantía en relación con el menor de conformidad con lo expuesto por esta parte en el fundamento de Derecho II.1 de esta contestación, o las que se determinen más adecuadas al interés del menor por el Tribunal, con expresa imposición de costas a la parte actora.

Es justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Abogado/a Firma del Procurador/a
