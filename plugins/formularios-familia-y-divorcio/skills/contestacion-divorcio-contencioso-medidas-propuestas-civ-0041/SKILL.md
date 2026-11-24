---
name: contestacion-divorcio-contencioso-medidas-propuestas-civ-0041
description: "Contestación a divorcio contencioso con medidas propuestas y reconvención de pensión compensatoria. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contestación a divorcio contencioso con medidas propuestas y reconvención de pensión compensatoria

> Formulario **CIV-0041** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Al Tribunal Contestación a la demanda e interposición de demanda reconvencional Hechos FUNDAMENTOS DE DERECHO Suplico Interposición de demanda reconvencional Fundamentos de derecho Suplico Firmas

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contestación a divorcio contencioso con medidas propuestas y reconvención de pensión compensatoria» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contestación a divorcio contencioso con medidas propuestas y reconvención de pensión compensatoria” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:contestacion-divorcio-contencioso-medidas-propuestas-civ-0041`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] PROGENITOR (OPCIÓN ALTERNATIVA) (8 veces)
- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] Nº (5 veces)
- [ ] Nº DE DOCUMENTO (5 veces)
- [ ] IMPORTE (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] PROFESIÓN (3 veces)
- [ ] AÑO (2 veces)
- [ ] CALLE (2 veces)
- [ ] DESCRIPCIÓN DEL BIEN (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] Nº DE DOCUMENTO FINAL (2 veces)
- [ ] COLEGIO
- [ ] DÍA
- [ ] DÍA O FECHA DE INICIO
- [ ] LUGAR
- [ ] MES
- [ ] Nº DE PROCEDIMIENTO
- [ ] SEDE

## Normas que cita el formulario

- art. 750 LEC
- art. 770 LEC
- art. 81 Código Civil
- art. 91 Código Civil
- art. 92.8 CC
- art. 142 CC
- art. 770.2 LEC
- art. 409 LEC
- art. 97 CC

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

- Junto a «…Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Denominación legal: Sección de Familia, Infancia y Capacidad. Si no existe en el partido, conoce la Sección Civil o la Única (art. 86.3-4 LOPJ). Fuente: LOPJ arts. 84.2.a) y 86 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «….3-4 LOPJ). Fuente: LOPJ arts. 84.2.a) y 86 (redacc. LO 1/2025, BOE-A-2025-76).]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

D./Dª [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, en nombre y representación de D./Dª [NOMBRE Y APELLIDOS], mayor de edad, de profesión [PROFESIÓN], con domicilio en [LOCALIDAD], calle [CALLE], nº [NÚMERO], pta., según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], comparezco en este TRIBUNAL con la asistencia del Letrado D./Dª [NOMBRE Y APELLIDOS], del Ilustre Colegio de Abogados de [COLEGIO], y DIGO:

Que por medio del presente escrito y en la representación que ostento, tras habérseme dado traslado de la demanda de divorcio conforme a lo dispuesto en el art. 753 de la Ley de Enjuiciamiento Civil, me persono en los autos de juicio núm. [Nº DE PROCEDIMIENTO]/[AÑO], instados por D./Dª [NOMBRE Y APELLIDOS], y formulo dentro del plazo legal de veinte días CONTESTACIÓN A LA DEMANDA e interpongo DEMANDA RECONVENCIONAL, con base en los siguientes:

HECHOS:

PRIMERO.- De acuerdo con el correlativo de la demanda, en relación con la existencia y fecha del matrimonio.

SEGUNDO.- De acuerdo con el correlativo de la demanda, en relación con la existencia y datos identificativos del/de la hijo/a común del matrimonio.

TERCERO.- De acuerdo con el correlativo de la demanda, en relación con la existencia de crisis matrimonial. Dado que han transcurrido más de tres meses desde el matrimonio, resulta procedente el divorcio que se pretende en la demanda.

CUARTO.- En desacuerdo con la conveniencia de que se otorgue la guarda y custodia del/la hijo/a común menor al/a la demandante.

Por el contrario, existen razones que justifican que sólo mediante un régimen de guarda y custodia compartida a través del cual se haga efectiva la corresponsabilidad de ambos progenitores en el cuidado del/de la hija menor, quedan adecuadamente atendido el interés superior de éste.

Son estas razones las siguientes:

El/la menor tiene una edad y, como consecuencia de ella, un grado de madurez, que hace aconsejable atender de modo razonable a sus preferencias, las cuales se decantan por la convivencia con ambos padres en un régimen de paridad.

Por otra parte, ambos progenitores tienen su residencia en la misma localidad y zona. Dada su ubicación, permitirían al/a la menor asistir con comodidad a su colegio actual y seguir relacionándose con los mismos amigos y compañeros. Y tanto uno como otro, cuentan con disponibilidad horaria suficiente para ocuparse del cuidado de su hijo/a. Además, comparten hábitos y criterios educativos semejantes.

Para acreditar los anteriores hechos se aportan como DOCUMENTOS Nos a [Nº DE DOCUMENTO FINAL], los siguientes:

Se aporta, igualmente, como DOCUMENTO Nº [Nº DE DOCUMENTO], informe emitido por el psicólogo D. [NOMBRE Y APELLIDOS], en el que se manifiesta la conveniencia de un régimen de guarda y custodia compartida para el/la menor.

Finalmente, y en orden al correcto desarrollo de la medida de guarda y custodia compartida propuesta, se acompaña como DOCUMENTO NÚMERO [Nº DE DOCUMENTO], plan de parentalidad, en el cual se recoge la forma en que debe llevarse a cabo la guarda y custodia compartida en beneficio del/de la hijo/a menor, por considerar este sistema el más adecuado para el buen desarrollo, educación y equilibrio emocional del hijo/a, atribuyéndose la guarda y custodia al padre y a la madre por periodos alternativos de un mes, comenzando por el padre, con el régimen de visitas indicado para la semana fuera de períodos vacacionales, y fines de semana, vacaciones, días señalados, debiendo cada progenitor hacerse cargo de los gastos en concepto de alimentos, en sentido amplio, que necesite el/la hijo/a cuando esté bajo la respectiva custodia de uno y otro, según el anterior régimen establecido, abonándose por mitad los gastos de colegios, institutos, facultades o universidades de carácter Público donde curse estudios el/la hijo/a, así como las matrículas, así como otros gastos extraordinarios, en concreto aquellos de naturaleza médica necesarios, no cubiertos por la Seguridad Social ni por cualquier otra mutualidad u organismo, serán abonados por mitad por ambos progenitores.

QUINTO.- En relación con lo anterior, y al contrario de lo que se solicita en la demanda, no procede fijar una pensión de alimentos a cargo de mi mandante, que sólo tendría sentido si se atribuyera la guarda y custodia individual al otro progenitor.

En lugar de esto, cada progenitor deberá mantener al menor durante el tiempo que conviva con él, además de satisfacer por mitad los gastos extraordinarios.

SEXTO.- En lo relativo al uso de la vivienda familiar, se propone su atribución a mi mandante con base en los siguientes hechos: Debe tenerse en cuenta que, a pesar de proponerse la guarda compartida, existe un claro desequilibrio entre las posiciones económicas de los progenitores, en perjuicio de mi representado/a, como se justificará en la demanda reconvencional. Por otra parte, el/la demandante cuenta con otra vivienda ubicada en la calle [CALLE] de [LOCALIDAD], con las siguientes características [DESCRIPCIÓN DEL BIEN], como se acredita con la certificación registral que se acompaña como DOCUMENTO Nº [Nº DE DOCUMENTO]

Resultan aplicables a los citados hechos los siguientes:

FUNDAMENTOS DE DERECHO

Competencia, procedimiento y legitimación. Conformes con la competencia objetiva y territorial del Tribunal, la legitimación de las partes, y el procedimiento.

Se decretará la audiencia del menor habida cuenta de la edad del mismo y ello según el espíritu de la Ley 8/2021 de 2 de junio que otorga intervención a los menores y a los mayores con discapacidad en aquellas decisiones judiciales que les afecten.

Representación y defensa. Mi mandante comparece representado/a y defendido/a, respectivamente, por el Procurador y el Letrado que constan en el encabezamiento de este escrito, de acuerdo con lo dispuesto en el artículo 750 LEC, en relación con el artículo 770 LEC.

De acuerdo con la fundamentación de los presupuestos del divorcio conforme al artículo 86 del Código civil, en relación con el art. 81 del Código Civil, en la nueva redacción dada por la Ley 8/2021 de 2 de junio, manifestándose mi mandante de acuerdo con la solicitud de divorcio.

Sin embargo, al no estar conforme con el contenido de las medidas definitivas solicitadas en relación con la guarda y custodia de los hijos, los alimentos a favor de éstos y la atribución del uso de la vivienda habitual de la familia, se formula oposición en cuanto a estos extremos y se solicita, con amparo en los arts 91 y ss del Código Civil, en especial los arts. 92.8, 93 y 96 CC, la adopción de las siguientes medidas definitivas, desarrolladas en extenso en el plan de parentalidad acompañado como DOCUMENTO NÚMERO [Nº DE DOCUMENTO], que son las siguientes:

1) Guarda y custodia compartida del/de la hijo/a menor:

El/La hijo/a menor de edad, quedará bajo la guarda y custodia compartida de ambos progenitores, por considerar este sistema el más adecuado para el buen desarrollo, educación y equilibrio emocional del hijo/a, lo que se llevará a efecto de conformidad a cuanto sigue:

1.- Cuantas decisiones sean necesarias en cuestiones que afecten directa o indirectamente al/a la menor, serán consultadas y decididas por ambos progenitores. En este sentido se fijan como de inexcusable consenso paterno-filial las medidas que conciernan al hijo/a referentes a elección de colegio, clases particulares, actividades extraescolares, cursos en el extranjero, viajes o salidas al extranjero en el que no vayan acompañados por algún progenitor, tratamientos médicos o intervenciones quirúrgicas, etc.

En virtud del derecho-deber que tienen los progenitores de velar por el hijo/a menor de edad, cuando se encuentren bajo la custodia de uno (guarda y custodia) u otro progenitor (régimen de visitas y estancias), deberán informarse mutuamente y de manera inmediata de cualquier circunstancia que acontezca respecto del/de la menor y que tenga carácter relevante y muy especialmente de cualquier enfermedad, favoreciendo y facilitando el contacto. Igualmente, ambos progenitores tendrán derecho a estar informados del rendimiento escolar, para lo cual, tendrán pleno derecho a asistir y recibir cuanta información requieran del Colegio donde asista el/la menor.

2.- La guarda y custodia se atribuye al padre y a la madre por periodos alternativos de una semana, comenzando por el padre [DÍA O FECHA DE INICIO] No se computan los meses de Julio y Agosto, por corresponder a estancias vacacionales.

3.- En el periodo en que un progenitor tenga la guarda y custodia del/de la menor, se establece para el otro el siguiente régimen de visitas:

Durante la semana fuera de períodos vacacionales.

Fines de semana.

El/La menor estará con el progenitor que no tenga la guarda los domingos desde las 9 h., que lo recogerá en el domicilio del progenitor que tenga la guarda, y se encargará de llevarlo al colegio los lunes por la mañana.

De lunes a viernes.

El/La menor estará con el progenitor que no tenga la guarda un día entre semana -de no acordar otra cosa ambos progenitores, será el miércoles- desde la salida del colegio, o en su defecto las 17 horas, hasta las 21 horas, momento en el que será reintegrado en el domicilio del progenitor que tenga la guarda y custodia del/de la menor esa semana.

Días festivos y puentes escolares fuera de períodos vacacionales.

Se distribuirán por mitad entre al padre y la madre. En caso de desacuerdo sobre la concreta distribución, la madre [PROGENITOR (OPCIÓN ALTERNATIVA)] tendrá preferencia para elegir si el menor permanece con ella [PROGENITOR (OPCIÓN ALTERNATIVA)] o con el padre [PROGENITOR (OPCIÓN ALTERNATIVA)] el primer festivo o puente que se presente. El siguiente, el/la menor permanecerá con el otro progenitor y a partir de ahí se irán alternando las estancias con uno y otro. Los puentes no se dividirán, salvo que ambos progenitores acuerden lo contrario.

Vacaciones de Navidad, Semana Santa y Verano.

Las vacaciones escolares de Navidad, Semana Santa y Verano, serán repartidas por mitad entre los progenitores, correspondiendo a la madre [PROGENITOR (OPCIÓN ALTERNATIVA)] la primera mitad los años pares y la segunda los impares, y al padre [PROGENITOR (OPCIÓN ALTERNATIVA)] a la inversa, salvo que ambos acuerden otro reparto diferente, haciéndose las siguientes puntualizaciones:

Primera. La recogida del/de la menor será a las 11 horas del primer día de vacaciones y finalizará a las 21 horas del último día que corresponda al que disfruta del primer periodo, o las 21 horas del último día de las vacaciones escolares al que disfrute del segundo periodo.

Segunda. En las vacaciones de Navidad, en todo caso, con independencia de a qué progenitor corresponda cada periodo se considerarán aparte los siguientes días: Nochebuena, que corresponderá al padre [PROGENITOR (OPCIÓN ALTERNATIVA)], y Navidad, que corresponderá a la madre

Tercera. Las vacaciones de verano comprenderán los meses de Julio y Agosto, y se distribuirán en cuatro quincenas, correspondiendo al padre [PROGENITOR (OPCIÓN ALTERNATIVA)] elegir en los años impares las dos quincenas que estará con el/la menor, y a la madre [PROGENITOR (OPCIÓN ALTERNATIVA)] en los pares, pudiendo ser consecutivas las referidas quincenas.

Comunicaciones telefónicas.

Ambos progenitores podrán comunicarse telefónicamente con su hijo/a con total libertad, respetándose para este tipo de comunicación el horario de descanso o estudio del/de la menor. Para el caso de que en periodo de vacaciones escolares se marchara de viaje, ambos progenitores se facilitarán un teléfono de contacto o colaborarán en que el/la menor efectúe la pertinente llamada telefónica. Todo ello se llevará a efecto, dentro de criterios de flexibilidad y atendiendo siempre, prioritariamente, al interés del/de la hijo/a."

2) Alimentos en favor del/de la hijo/a menor:

Ambos progenitores se harán cargo de los gastos en concepto de alimentos, en sentido amplio, que necesite el/la hijo/a cuando esté bajo la respectiva custodia de uno y otro, según el anterior régimen establecido.

Los gastos de colegios, institutos, facultades o universidades de carácter Público donde curse estudios el/la hijo/a, así como las matrículas, serán abonados por mitad por ambos progenitores. En el caso de Centros Privados, se sufragarán por mitad siempre que haya acuerdo por ambas partes. En caso de desacuerdo, el exceso que suponga sobre el Centro Público será sufragado por el progenitor que haya decidido que realicen los estudios en el Centro Privado que finalmente haya elegido. Los relativos a gastos por clases extraordinarias de repaso, viajes escolares de las menores, tanto si se llevan a cabo en el mismo colegio o en un centro externo, serán a cargo, por mitad, de ambos progenitores, siempre que previamente hayan prestado su conformidad o así vengan recomendados por el centro escolar. Caso contrario, serán sufragados por el progenitor que haya decidido su realización.

Otros gastos extraordinarios, en concreto aquellos de naturaleza médica necesarios, no cubiertos por la Seguridad Social ni por cualquier otra mutualidad u organismo, serán abonados por mitad por ambos progenitores.

Si, tras cumplir los dieciocho años, el hijo se encuentra todavía en período de formación y no pueda mantenerse por sí mismo, ambos progenitores le prestarán los alimentos debidos de acuerdo con los arts. 142 y ss CC en proporción a sus respectivos recursos.

3) Atribución del uso de la vivienda familiar:

En relación con el uso de la vivienda familiar, así como del ajuar doméstico, se propone la atribución del mismo a mi mandante, por ser el suyo el interés familiar más necesitado de protección, en los siguientes términos:

Costas. Las costas deben ser impuestas a la parte demandante conforme al art. 394 de la Ley de Enjuiciamiento Civil.

Iura novit curia y las demás normas que resulten procedentes.

En virtud de lo expuesto,

SUPLICO AL TRIBUNAL

Que tras admitir este escrito con los documentos que lo acompañan, me tenga por comparecido y parte en la representación que ostento, entendiéndose conmigo las sucesivas diligencias, y tenga por interpuesta en tiempo y forma CONTESTACIÓN A LA DEMANDA CONTENCIOSA DE DIVORCIO y, previos los trámites procesales oportunos y con intervención del Ministerio Fiscal, dicte en su día sentencia por la que se estime el divorcio y se desestimen las medidas definitivas propuestas en la demanda, con estimación, en su lugar, de las que propone mi mandante, que han sido detalladas en los Fundamentos de Derecho de esta contestación y que reiteramos en esta Solicitud, con obligación de satisfacer cada parte sus costas y las comunes por mitad. Las medidas definitivas cuya adopción se solicita son las siguientes:

Interposición de demanda reconvencional

OTROSÍ DIGO que conforme al art. 770 LEC, formulamos, al mismo tiempo, DEMANDA RECONVENCIONAL frente a la parte actora, con intervención del Ministerio Fiscal, conforme a los siguientes:

PRIMERO.- Dense por reiterados los hechos de la contestación.

SEGUNDO.- Existe un acentuado desequilibrio patrimonial entre mi mandante y el/la demandante, que implica un empeoramiento en su situación anterior en el matrimonio, por lo que mi mandante tiene derecho a una compensación económica para corregir este desequilibrio. Deriva tal desequilibrio de los siguientes hechos: desde que el matrimonio se celebró, hace ahora [Nº] años, mi mandante, renunciando a su profesión de [PROFESIÓN], que en aquellos momento desempeñaba, ha dedicado todo su esfuerzo y trabajo al cuidado del hogar, de su cónyuge y de los hijos comunes de ambos. Para ello ha renunciado a la posibilidad de desarrollar una profesión que le permitiera tener independencia económica, con la consiguiente pérdida de oportunidades y dificultad para volver a acceder a un empleo, que se ve incrementada por su actual edad, que es de [Nº] años. El desequilibrio se acentúa por la circunstancia de haberse regido los cónyuges, durante la vigencia de su matrimonio, por la separación de bienes y no contar mi representado/a con patrimonio propio. Esta situación contrasta con la del/de la demandante, que durante todos los años de duración del matrimonio ha venido desempeñando su profesión de: De dicha actividad profesional obtiene el/la demandante unos ingresos mensuales de [IMPORTE] euros. Además, es propietario de los siguientes inmuebles por título de herencia [DESCRIPCIÓN DEL BIEN]:

Para acreditar las anteriores circunstancias, se acompañan, como DOCUMENTOS Nos a [Nº DE DOCUMENTO FINAL], los siguientes:

Resultan aplicables a los citados hechos los siguientes.

Fundamentos de derecho

I. Resulta competente para conocer de la demanda reconvencional el mismo Juez que esté conociendo de la demanda principal.

II. El art. 770.2ª LEC admite que se formule reconvención al contestar la demanda de separación o divorcio en los siguientes casos:

a) Cuando se funde en alguna de las causas que puedan dar lugar a la nulidad del matrimonio.

b) Cuando el cónyuge demandado de separación o de nulidad pretenda el divorcio.

c) Cuando el cónyuge demandado de nulidad pretenda la separación.

d) Cuando el cónyuge demandado pretenda la adopción de medidas definitivas, que no hubieran sido solicitadas en la demanda, y sobre las que el tribunal no deba pronunciarse de oficio. En el caso presente el supuesto se ajusta al enunciado bajo la letra d), debiendo sustanciarse y resolverse la reconvención conforme con lo prevenido en el art. 409 LEC.

III. En relación con la compensación económica por desequilibro patrimonial, el art. 97 CC.

La pensión procede en favor de mi mandante por existir, tal y como se ha justificado en los HECHOS, un claro desequilibrio patrimonial en relación con la posición del otro cónyuge, que implica un empeoramiento en su situación anterior en el matrimonio.

Con el fin de determinar la cuantía de la pensión, deben tomarse en consideración las siguientes circunstancias: la edad de mi representado/a, que es de [Nº] años, y su dedicación exclusiva a la familia durante los [Nº] años que ha durado el matrimonio, renunciando a su desarrollo profesional y, en concreto, con abandono de su actividad como [PROFESIÓN], al contraer matrimonio. Todas estas circunstancias, dificultan además gravemente su posibilidades de acceder al mercado de trabajo en la actualidad.

De acuerdo con lo anterior, consideramos que procede fijar una pensión de carácter indefinido, dada la larga duración del matrimonio y el resto de circunstancias antes expuestas, por cuantía de [IMPORTE] euros mensuales, a pagar mediante ingreso en la cuenta corriente nº [NÚMERO], de la que es titular mi representado/a, durante los cinco primeros días de cada mes y actualizable anualmente de acuerdo con las variaciones del Índice de Precios al Consumo publicado por el Instituto Nacional de Estadística u organismo, público o privado, que en el futuro le sustituya.

IV. COSTAS.- Deben imponerse a la parte demandada en reconvención si se opone a la demanda reconvencional, conforme a lo dispuesto en el art. 394 de la Ley de Enjuiciamiento Civil.

En virtud de lo expuesto,

SUPLICO AL TRIBUNAL

Que tenga por interpuesta en tiempo y forma DEMANDA RECONVENCIONAL contra D./Dª [NOMBRE Y APELLIDOS] y, previos los trámites procesales oportunos con intervención del Ministerio Fiscal, y tras declarar el divorcio de las partes, acuerde el establecimiento de una pensión compensatoria en favor de mi mandante y a cargo de la parte reconvenida por importe de [IMPORTE] euros mensuales, a pagar mediante ingreso en la cuenta corriente nº [NÚMERO], de la que es titular mi representado/a, durante los cinco primeros días de cada mes y actualizable anualmente de acuerdo con las variaciones del Índice de Precios al Consumo publicado por el Instituto Nacional de Estadística u organismo, público o privado, que en el futuro le sustituya, con imposición de las costas de esta reconvención a la parte reconvenida.

OTROSÍ PRIMERO DIGO que se acompaña en anexo relación de documentos presentados debidamente foliados y con índice electrónico para su debida localización y consulta.

SUPLICO AL TRIBUNAL tenga hecha esta manifestación a los efectos oportunos y por aportados los documentos relacionados en el anexo

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma y número del Letrado	Firma del Procurador

========================================================================
