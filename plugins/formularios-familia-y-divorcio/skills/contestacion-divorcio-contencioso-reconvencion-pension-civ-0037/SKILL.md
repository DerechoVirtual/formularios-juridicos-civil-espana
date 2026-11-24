---
name: contestacion-divorcio-contencioso-reconvencion-pension-civ-0037
description: "Contestación a divorcio contencioso con reconvención de pensión compensatoria, Derecho catalán. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contestación a divorcio contencioso con reconvención de pensión compensatoria, Derecho catalán

> Formulario **CIV-0037** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Al Tribunal Comparecencia, representación y asistencia letrada Contestación a la demanda e interposición de demanda reconvencional Hechos FUNDAMENTOS DE DERECHO Suplico Interposición de demanda reconvencional Firmas

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contestación a divorcio contencioso con reconvención de pensión compensatoria, Derecho catalán» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contestación a divorcio contencioso con reconvención de pensión compensatoria, Derecho catalán” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:contestacion-divorcio-contencioso-reconvencion-pension-civ-0037`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº DE DOCUMENTO (8 veces)
- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] Nº (6 veces)
- [ ] PROFESIÓN (4 veces)
- [ ] IMPORTE (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] AÑO (2 veces)
- [ ] CALLE (2 veces)
- [ ] DESCRIPCIÓN DEL BIEN (2 veces)
- [ ] FUNDAMENTOS (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] RELACIÓN DE DOCUMENTOS (2 veces)
- [ ] COLEGIO
- [ ] DÍA
- [ ] MES
- [ ] Nº DE PROCEDIMIENTO
- [ ] PETICIÓN
- [ ] SEDE

## Normas que cita el formulario

- art. 750 LEC
- art. 770 LEC
- art. 233 Código Civil
- art. 233.20.3.a Código Civil
- art. 770.2 LEC
- art. 409 LEC

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

Que por medio del presente escrito y en la representación que ostento, tras habérseme dado traslado de la demanda de divorcio conforme a lo dispuesto en el art. 753 de la Ley de Enjuiciamiento Civil, me persono en los autos de juicio núm. [Nº DE PROCEDIMIENTO]/[AÑO], instados por D./Dª [NOMBRE Y APELLIDOS], y formulo dentro del plazo legal de veinte días CONTESTACIÓN A LA DEMANDA e interpongo DEMANDA RECONVENCIONAL, con base en los siguientes

HECHOS:

PRIMERO De acuerdo con el correlativo de la demanda, en relación con los datos de celebración del matrimonio.

SEGUNDO De acuerdo con el correlativo de la demanda, en relación con los datos del/de la hijo/a común del matrimonio.

TERCERO De acuerdo con el correlativo de la demanda en cuanto al régimen económico matrimonial, que es el legal de separación de bienes

CUARTO De acuerdo con el correlativo de la demanda, en relación con la existencia de crisis matrimonial. Dado que han transcurrido más de tres meses desde el matrimonio, nada tiene que oponer mi representado/a a la pretensión de divorcio del/de la actor/a.

QUINTO En desacuerdo con la conveniencia de que se otorgue la guarda y custodia del/la hijo/a común menor al/a la demandante y, en relación con ello, de que se fije la pensión alimenticia solicitada en la demanda a cargo de mi mandante.

Por el contrario, existen razones que hacen conveniente la fijación de un régimen de guarda y custodia compartida a través del cual se haga efectiva la corresponsabilidad de ambos progenitores en el cuidado del/de la hija menor, sin que, en correspondencia con ello, proceda fijar la pensión alimenticia solicitada en la demanda.

Son estas razones las siguientes:

Para acreditar los anteriores hechos se aportan como DOCUMENTOS Nº [Nº DE DOCUMENTO] a [Nº DE DOCUMENTO], los siguientes: [RELACIÓN DE DOCUMENTOS].

Se aporta, igualmente, como DOCUMENTO Nº [Nº DE DOCUMENTO], informe emitido por el psicólogo D. [NOMBRE Y APELLIDOS], en el que se manifiesta la conveniencia de un régimen de guarda y custodia compartida para el/la menor.

SEXTO Así mismo y en relación con lo anterior, no procede fijar una pensión de alimentos a cargo de mi mandante, que sólo tendría sentido si se atribuyera la guarda y custodia individual al otro progenitor.

En lugar de esto, cada progenitor deberá mantener al menor durante el tiempo que conviva con él, además de satisfacer por mitad los gastos extraordinarios.

SÉPTIMO En relación con el uso de la vivienda familiar, cuya titularidad corresponde en comunidad a ambos cónyuges, tal y como resulta de la certificación registral que se acompaña como DOCUMENTO Nº [Nº DE DOCUMENTO], se propone la atribución de su uso a mi mandante con base en los siguientes hechos: Debe tenerse en cuenta que, a pesar de proponerse la guarda compartida, existe un claro desequilibrio entre las posiciones económicas de los progenitores, en perjuicio de mi mandante, como se justificará en la demanda reconvencional. Por otra parte, el/la demandante cuenta con otra vivienda ubicada en la calle [CALLE], con las siguientes características [DESCRIPCIÓN DEL BIEN], como se acredita con la certificación registral que se acompaña como DOCUMENTO Nº [Nº DE DOCUMENTO]

Resultan aplicables a los citados hechos los siguientes:

FUNDAMENTOS DE DERECHO

COMPETENCIA, PROCEDIMIENTO Y LEGITIMACIÓN

Conformes con la competencia objetiva y territorial del Tribunal, la legitimación de las partes, y el procedimiento.

REPRESENTACIÓN Y DEFENSA

Mi mandante comparece representado/a y defendido/a, respectivamente, por el Procurador y el Letrado que constan en el encabezamiento de este escrito, de acuerdo con lo dispuesto en el artículo 750 LEC, en relación con el artículo 770 LEC.

DERECHO SUSTANTIVO

Dado que el vigente art. 86 del Código civil, no requiere causa alguna de divorcio, bastando para poder solicitarlo y que sea decretado por el Juez el transcurso de tres meses desde el matrimonio, nada hay que oponer a este extremo.

Sin embargo, al no estar de acuerdo con el contenido de las medidas definitivas solicitadas, en relación con la guarda y custodia de los hijos, los alimentos a favor de éstos y la atribución del uso de la vivienda habitual de la familia, se formula oposición en cuanto a estos extremos y, con amparo en los artículos 233-4 y ss. del Código Civil de Cataluña, se solicita la adopción de las siguientes medidas definitivas:

A) Guarda y custodia compartida del/de la hijo/a menor.- Dispone el art. 233-8 del Código Civil de Cataluña, bajo la rúbrica "Responsabilidad parental":

"1. La nulidad del matrimonio, el divorcio o la separación no alteran las responsabilidades que los progenitores tienen hacia sus hijos de acuerdo con el artículo 236-17.1. En consecuencia, estas responsabilidades mantienen el carácter compartido y, en la medida de lo posible, deben ejercerse conjuntamente.

2. Los cónyuges, para determinar cómo deben ejercerse las responsabilidades parentales, deben presentar sus propuestas de plan de parentalidad, con el contenido establecido por el artículo 233-9.

3. La autoridad judicial, en el momento de decidir sobre las responsabilidades parentales de los progenitores, debe atender de forma prioritaria al interés del menor”.

Por su parte, el art. 233-10 del mismo Cuerpo Legal, establece: "Ejercicio de la guarda

1. La guarda debe ejercerse de la forma convenida por los cónyuges en el plan de parentalidad, salvo que resulte perjudicial para los hijos.

2. La autoridad judicial, si no existe acuerdo o si este no se ha aprobado, debe determinar la forma de ejercer la guarda, ateniéndose al carácter conjunto de las responsabilidades parentales, de acuerdo con el artículo 233-8.1. Sin embargo, la autoridad judicial puede disponer que la guarda se ejerza de modo individual si conviene más al interés del hijo.

3. La forma de ejercer la guarda no altera el contenido de la obligación de alimentos hacia los hijos comunes, si bien es preciso ponderar el tiempo de permanencia de los menores con cada uno de los progenitores y los gastos que cada uno de ellos haya asumido pagar directamente. (…)"

Conforme con los anteriores preceptos y en atención a los criterios que expone el art. 233-11 del Código Civil de Cataluña, en relación con los hechos antes expuestos, se acompaña como documento número [Nº] Plan de Parentalidad, ajustado a lo dispuesto en el art. 233-9 del Código Civil de Cataluña, cuyos aspectos más relevantes son los siguientes: [FUNDAMENTOS].

B) Alimentos en favor del/de la hijo/a menor.- El art. 236-17.1 del Código Civil de Cataluña dispone: "Relaciones entre padres e hijos.1. Los progenitores, en virtud de sus responsabilidades parentales, deben cuidar de los hijos, prestarles alimentos en el sentido más amplio, convivir con ellos, educarlos y proporcionarles una formación integral. (…)". El art. 233-10.3 del Código Civil de Cataluña señala que "La forma de ejercer la guarda no altera el contenido de la obligación de alimentos hacia los hijos comunes, si bien es preciso ponderar el tiempo de permanencia de los menores con cada uno de los progenitores y los gastos que cada uno de ellos haya asumido pagar directamente.(…)". Y los arts. 237-1 y ss. del Código Civil de Cataluña, regulan los alimentos entre parientes.

En atención al régimen de guarda y custodia compartida propuesto, procede establecer en relación con los alimentos el siguiente régimen:

Ambos progenitores se harán cargo de los gastos en concepto de alimentos, en sentido amplio que necesite el/la hijo/a cuando esté bajo la respectiva custodia de uno y otro, según el anterior régimen establecido.

Los gastos de colegios, institutos, facultades o universidades de carácter Público donde curse estudios el/la hijo/a, así como las matrículas, serán abonados por mitad por ambos progenitores. En el caso de Centros Privados, se sufragarán por mitad siempre que haya acuerdo por ambas partes. En caso de desacuerdo, el exceso que suponga sobre el Centro Público será sufragado por el progenitor que haya decidido que realicen los estudios en el Centro Privado que finalmente haya elegido. Los relativos a gastos por clases extraordinarias de repaso, viajes escolares de las menores, tanto si se llevan a cabo en el mismo colegio o en un centro externo, serán a cargo, por mitad, de ambos progenitores, siempre que previamente hayan prestado su conformidad o así vengan recomendados por el centro escolar. Caso contrario, serán sufragados por el progenitor que haya decidido su realización.

Otros gastos extraordinarios, en concreto aquellos de naturaleza médica necesarios, no cubiertos por la Seguridad Social ni por cualquier otra mutualidad u organismo, serán abonados por mitad por ambos progenitores.

Si, tras cumplir los dieciocho años, el hijo se encuentra todavía en período de formación y no pueda mantenerse por sí mismo, ambos progenitores le prestarán los alimentos debidos de acuerdo con los arts. 142 y ss. CC en proporción a sus respectivos recursos.

C) Atribución del uso de la vivienda familiar.- El art. 233.20.3.a) del Código Civil de Cataluña establece: "No obstante lo establecido por el apartado 2, la autoridad judicial debe atribuir el uso de la vivienda familiar al cónyuge más necesitado en los siguientes casos: a) Si la guarda de los hijos queda compartida o distribuida entre los progenitores."

Conforme con la citada norma, se propone la atribución del uso de la vivienda familiar, así como del ajuar doméstico, a mi mandante, al haber acreditado en los hechos que el suyo es el interés familiar más necesitado de protección, en los siguientes términos: [FUNDAMENTOS].

COSTAS.- Las costas deben ser impuestas a la parte demandante conforme al art. 394 de la Ley de Enjuiciamiento Civil.

Iura novit curia y las demás normas que resulten procedentes.

En virtud de lo expuesto,

SUPLICO AL TRIBUNAL

Que tras admitir este escrito con los documentos que lo acompañan, me tenga por comparecido y parte en la representación que ostento, entendiéndose conmigo las sucesivas diligencias, y tenga por interpuesta en tiempo y forma CONTESTACIÓN A LA DEMANDA CONTENCIOSA DE DIVORCIO y, previos los trámites procesales oportunos, dicte en su día sentencia por la que se estime el divorcio y se desestimen las medidas definitivas propuestas en la demanda, con estimación, en su lugar, de las que propone mi mandante, que han sido detalladas en los Fundamentos de Derecho de esta contestación y que reiteramos en esta Solicitud, con obligación de satisfacer cada parte sus costas y las comunes por mitad. Las medidas definitivas cuya adopción se solicita son las siguientes: [PETICIÓN].

Interposición de demanda reconvencional

Conforme al art. 770 LEC, formulamos, al mismo tiempo, DEMANDA RECONVENCIONAL conforme a los siguientes

Interposición de demanda reconvencional

HECHOS

PRIMERO Dense por reiterados los hechos de la contestación.

SEGUNDO La situación económica de mi representado/a, como consecuencia de la ruptura de la convivencia, ha resultado claramente perjudicada en relación con la de su cónyuge. Por ello tiene derecho a solicitar la prestación compensatoria regulada en los arts. 233-14 y ss. del Código Civil de Cataluña, siendo éste el primer proceso matrimonial seguido entre las partes.

Deriva este perjuicio económico de los siguientes hechos: desde que el matrimonio se celebró, hace ahora [Nº] años, mi mandante, abandonando su profesión de [PROFESIÓN], que en aquellos momento desempeñaba, ha dedicado todo su esfuerzo y trabajo al cuidado del hogar, de su cónyuge y de los hijos comunes de ambos. Para ello ha renunciado a la posibilidad de desarrollar una profesión que le permitiera tener independencia económica, con la consiguiente pérdida de oportunidades y dificultad para volver a acceder a un empleo, que se ve acentuada por la edad de mi mandante que, en la actualidad es de [Nº] años. El desequilibrio se acentúa por la circunstancia de haberse regido los cónyuges, durante la vigencia de su matrimonio, por el régimen legal de separación de bienes y no contar mi representado/a con patrimonio propio.

Esta situación contrasta con la del/de la demandante, que durante todos los años de duración del matrimonio ha venido desempeñando su profesión de: [PROFESIÓN]. De dicha actividad profesional obtiene el/la demandante unos ingresos mensuales de: [IMPORTE] euros. Además, es propietario de los siguientes inmuebles por título de herencia: [DESCRIPCIÓN DEL BIEN].

Para acreditar las anteriores circunstancias, se acompañan, como DOCUMENTOS Nº [Nº DE DOCUMENTO] a [Nº DE DOCUMENTO], los siguientes: [RELACIÓN DE DOCUMENTOS].

Resultan aplicables a los citados hechos los siguientes

FUNDAMENTOS DE DERECHO

I. Resulta competente para conocer de la demanda reconvencional el mismo Juez que esté conociendo de la demanda principal.

II. El art. 770.2ª LEC admite que se formule reconvención al contestar la demanda de separación o divorcio en los siguientes casos: a) Cuando se funde en alguna de las causas que puedan dar lugar a la nulidad del matrimonio.b) Cuando el cónyuge demandado de separación o de nulidad pretenda el divorcio.c) Cuando el cónyuge demandado de nulidad pretenda la separación.d) Cuando el cónyuge demandado pretenda la adopción de medidas definitivas, que no hubieran sido solicitadas en la demanda, y sobre las que el tribunal no deba pronunciarse de oficio. En el caso presente el supuesto se ajusta al enunciado bajo la letra d), debiendo sustanciarse y resolverse la reconvención conforme con lo prevenido en el art. 409 LEC.

III. En relación con la compensación económica por desequilibro patrimonial, resultan aplicables los artículos 233-14 y ss. del Código Civil de Cataluña.

De acuerdo con el primero, el cónyuge cuya situación económica, como consecuencia de la ruptura de la convivencia, resulte más perjudicada tiene derecho a solicitar en el primer proceso matrimonial una prestación compensatoria que no exceda del nivel de vida de que gozaba durante el matrimonio ni del que pueda mantener el cónyuge obligado.

Al efecto de determinar la cuantía y duración de la citada prestación económica, deben valorarse especialmente, a tenor del art. 233-15 del Código Civil de Cataluña, las siguientes circunstancias: a) La posición económica de los cónyuges, teniendo en cuenta, si procede, la compensación económica por razón de trabajo o las previsibles atribuciones derivadas de la liquidación del régimen económico matrimonial. b) La realización de tareas familiares u otras decisiones tomadas en interés de la familia durante la convivencia, si eso ha reducido la capacidad de uno de los cónyuges para obtener ingresos. c) Las perspectivas económicas previsibles de los cónyuges, teniendo en cuenta su edad y estado de salud y la forma en que se atribuye la guarda de los hijos comunes. d) La duración de la convivencia. e) Los nuevos gastos familiares del deudor, si procede.

En relación con el pago de la pensión, hay que atender al art. 233-17 del Código Civil de Cataluña.

La pensión procede en favor de mi mandante por existir, tal y como se ha justificado en los HECHOS, el perjuicio económico al que nos hemos referido, derivado de la crisis matrimonial.

Con el fin de determinar la cuantía de la pensión, deben tomarse en consideración las siguientes circunstancias: la edad de mi representado/a, que es de [Nº] años, y su dedicación exclusiva a la familia durante los [Nº] años que ha durado el matrimonio, renunciando a su desarrollo profesional y, en concreto, con abandono de su actividad como [PROFESIÓN], al contraer matrimonio. Todas estas circunstancias, dificultan además gravemente su posibilidades de acceder al mercado de trabajo en la actualidad.

De acuerdo con lo anterior, consideramos que concurren circunstancias que justifican, en el caso presente, la fijación de una pensión compensatoria indefinida, tal y como admite el art. 233-17.4, dada la larga duración del matrimonio y el resto de circunstancias antes expuestas, por cuantía de [IMPORTE] euros mensuales, a pagar mediante ingreso en la cuenta corriente nº [NÚMERO], de la que es titular mi mandante, durante los cinco primeros días de cada mes y actualizable anualmente de acuerdo con las variaciones del Índice de Precios al Consumo publicado por el Instituto Nacional de Estadística u organismo, público o privado, que en el futuro le sustituya.

IV. COSTAS.- Deben imponerse a la parte demandada en reconvención si se opone a la demanda reconvencional, conforme a lo dispuesto en el art. 394 de la Ley de Enjuiciamiento Civil.

IV.Iura novit curia.

En virtud de lo expuesto,

SUPLICO AL TRIBUNAL

Que tenga por interpuesta en tiempo y forma DEMANDA RECONVENCIONAL contra D./Dª [NOMBRE Y APELLIDOS] y, previos los trámites procesales oportunos, y tras declarar el divorcio de las partes, acuerde el establecimiento de una pensión compensatoria indefinida en favor de mi mandante y a cargo de la parte reconvenida por importe de [IMPORTE] euros mensuales, a pagar mediante ingreso en la cuenta corriente nº [NÚMERO], de la que es titular mi mandante, durante los cinco primeros días de cada mes y actualizable anualmente de acuerdo con las variaciones del Índice de Precios al Consumo publicado por el Instituto Nacional de Estadística u organismo, público o privado, que en el futuro le sustituya, con imposición de las costas de esta reconvención a la parte reconvenida.

En [LOCALIDAD], a [DÍA], de [MES], de [AÑO]

Firma y número del Letrado Firma del Procurador

========================================================================
