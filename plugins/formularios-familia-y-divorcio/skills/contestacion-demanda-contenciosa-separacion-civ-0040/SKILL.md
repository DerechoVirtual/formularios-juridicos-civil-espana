---
name: contestacion-demanda-contenciosa-separacion-civ-0040
description: "Contestación a demanda contenciosa de separación con reconvención de divorcio y medidas definitivas. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contestación a demanda contenciosa de separación con reconvención de divorcio y medidas definitivas

> Formulario **CIV-0040** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Parte Contestación a la demanda e interposición de demanda reconvencional Hechos FUNDAMENTOS DE DERECHO Suplico Interposición de demanda reconvencional Firmas

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contestación a demanda contenciosa de separación con reconvención de divorcio y medidas definitivas» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contestación a demanda contenciosa de separación con reconvención de divorcio y medidas definitivas” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:contestacion-demanda-contenciosa-separacion-civ-0040`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] PROGENITOR (OPCIÓN ALTERNATIVA) (8 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] AÑO (2 veces)
- [ ] CALLE (2 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] COLEGIO
- [ ] DESCRIPCIÓN DEL BIEN
- [ ] DÍA
- [ ] DÍA O FECHA DE INICIO
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] MES
- [ ] Nº
- [ ] Nº DE DOCUMENTO FINAL
- [ ] Nº DE PROCEDIMIENTO
- [ ] NÚMERO
- [ ] PROFESIÓN
- [ ] SEDE

## Normas que cita el formulario

- art. 86 CC
- art. 770 LEC
- art. 770.2 LEC
- art. 409 LEC
- art. 91 Código Civil
- art. 92.8 CC
- art. 142 CC

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

D./Dª [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, en nombre y representación de D./Dª [NOMBRE Y APELLIDOS], mayor de edad, de profesión [PROFESIÓN], con domicilio en [LOCALIDAD], calle [CALLE], nº [NÚMERO], pta., cuya representación acreditaré mediante comparecencia apud acta cuando sea requerido para ello, comparezco en este TRIBUNAL con la asistencia del Letrado D./Dª [NOMBRE Y APELLIDOS], del Ilustre Colegio de Abogados de [COLEGIO], y DIGO:

Que por medio del presente escrito y en la representación que ostento, tras habérseme dado traslado de la demanda de separación conforme a lo dispuesto en el art. 753 de la Ley de Enjuiciamiento Civil, me persono en los autos de juicio núm. [Nº DE PROCEDIMIENTO]/[AÑO], instados por D./Dª [NOMBRE Y APELLIDOS], y formulo dentro del plazo legal de veinte días CONTESTACIÓN A LA DEMANDA e interpongo DEMANDA RECONVENCIONAL, con base en los siguientes

HECHOS:

PRIMERO.- De acuerdo con los hechos expuestos en la demanda de contrario en sus números PRIMERO y SEGUNDO, relativos a la existencia y fecha del matrimonio y a la existencia y datos identificativos del/de la hijo/a común del matrimonio.

SEGUNDO.- De acuerdo con la existencia de crisis matrimonial y separación de hecho de los cónyuges. Dado que han transcurrido más de tres meses desde el matrimonio, resulta procedente no sólo la separación, que se pretende en la demanda, sino el divorcio que desea mi mandante y solicitará en la reconvención.

TERCERO.- En desacuerdo con la conveniencia de que se otorgue la guarda y custodia individual del/la hijo/a común menor al/a la demandante y, en relación con ello, de que se fije la pensión alimenticia solicitada en la demanda a cargo de mi mandante.

Por el contrario, existen razones que justifican que sólo mediante un régimen de custodia compartida a través del cual se haga efectiva la corresponsabilidad de ambos progenitores en el cuidado del/de la hija menor, queda adecuadamente atendido el interés superior del mismo, sin que, en correspondencia con ello, proceda fijar la pensión alimenticia solicitada en la demanda.

Son estas razones las siguientes:

Se aporta para acreditar las anteriores circunstancias, como DOCUMENTOS Nos a [Nº DE DOCUMENTO FINAL], los siguientes:

CUARTO.- Así mismo y en relación con lo anterior, no procede fijar una pensión de alimentos a cargo de mi mandante, que sólo tendría sentido si se atribuyera la guarda y custodia individual al otro progenitor.

En lugar de esto, cada progenitor deberá mantener al menor durante el tiempo que conviva con él, además de satisfacer por mitad los gastos extraordinarios.

QUINTO.- En lo relativo al uso de la vivienda familiar, que corresponde en comunidad ordinaria a ambos cónyuges, tal y como resulta de la certificación registral que se acompaña como DOCUMENTO Nº [Nº DE DOCUMENTO], se propone la atribución de su uso a mi mandante con base en los siguientes hechos: El/la demandante cuenta con otra vivienda ubicada en la calle [CALLE], con las siguientes características [DESCRIPCIÓN DEL BIEN], como se acredita con la certificación registral que se acompaña DOCUMENTO Nº [Nº DE DOCUMENTO], en la que habita en la actualidad. Por el contrario, mi representado no dispone de otro inmueble en el que fijar su residencia. A lo anterior, se unen las siguientes circunstancias:

Resultan aplicables a los citados hechos los siguientes

FUNDAMENTOS DE DERECHO

Competencia, procedimiento, legitimación y postulación procesal

Conformes con la competencia objetiva y territorial del Tribunal, la legitimación de las partes, y el procedimiento, compareciendo esta parte con la debida representación técnica y asistencia letrada.

Se decretará la exploración del menor, habida cuenta de la edad del mismo y ello según el espíritu de la Ley 8/2021 de 2 de junio que otorga intervención a los menores y a los mayores con discapacidad en aquellas decisiones judiciales que les afecten.

Derecho sustantivo

Concurren en el caso presente los presupuestos de la separación conforme al artículo 81 del Código civil, presupuestos que reitera, el artículo 86 CC para el divorcio por remisión al precepto antes citado.

Ahora bien, al solicitar mi mandante el divorcio en la reconvención que incluye este escrito, y no ser preceptivo, después de la Ley 15/2005, de 8 de julio, por la que se modifican el Código Civil y la Ley de Enjuiciamiento Civil en materia de separación y divorcio, que la separación preceda al divorcio, no procede decretar la separación judicial, sino el divorcio directamente.

En cuanto a las medidas definitivas reguladas en los arts. 91 y ss. del Código Civil, mi mandante manifiesta su disconformidad en relación con las propuestas en la demanda que se contesta, proponiendo en su lugar las que se expondrán en la demanda reconvencional que a continuación se formula.

Costas

Las costas deberán ser asumidas por el demandante como consecuencia de ser desestimadas sus pretensiones, conforme al art. 394 de la Ley de Enjuiciamiento Civil.

Iura novit curia y las demás normas que resulten procedentes.

Por lo expuesto,

SUPLICO AL TRIBUNAL

Que tras admitir este escrito con los documentos que lo acompañan, me tenga por comparecido y parte en la representación que ostento, entendiéndose conmigo las sucesivas diligencias, y tenga por interpuesta en tiempo y forma CONTESTACIÓN A LA DEMANDA CONTENCIOSA DE SEPARACIÓN y, previos los trámites procesales oportunos, dicte en su día sentencia por la que se desestime íntegramente la demanda en el sentido de que no se acuerde la separación sino el divorcio, tal y como se interesa en la reconvención, con imposición de las costas al demandante.

Interposición de demanda reconvencional

OTROSÍ DIGO que conforme al art. 770 LEC, formulamos DEMANDA RECONVENCIONAL conforme a los siguientes

HECHOS:

Se dan por reproducidos los HECHOS expuestos en la contestación a la demanda.

Resultan aplicables a los citados hechos los siguientes

FUNDAMENTOS DE DERECHO

I.- COMPETENCIA.- La competencia para conocer de la demanda reconvencional corresponde al Juez que esté conociendo de la demanda principal.

II.- RECONVENCIÓN.- El art. 770.2ª LEC admite que se formule reconvención al contestar la demanda de separación o divorcio en los siguientes casos:

a) Cuando se funde en alguna de las causas que puedan dar lugar a la nulidad del matrimonio.

b) Cuando el cónyuge demandado de separación o de nulidad pretenda el divorcio.

c) Cuando el cónyuge demandado de nulidad pretenda la separación.

d) Cuando el cónyuge demandado pretenda la adopción de medidas definitivas, que no hubieran sido solicitadas en la demanda, y sobre las que el tribunal no deba pronunciarse de oficio. En el caso presente el supuesto se ajusta al enunciado bajo la letra b). La demanda reconvencional se sustanciará y resolverá conforme a lo dispuesto en el art. 409 LEC.

III. DERECHO SUSTANTIVO.- Tras la reforma del Código civil por Ley 15/2005, de 8 de julio, por la que se modifica el Código Civil y la Ley de Enjuiciamiento Civil, en materia de separación y divorcio, no es necesaria la separación previa de los cónyuges para acceder al divorcio.

Bastará para solicitar y obtener el divorcio, con que concurran los requisitos del art. 86 CC, que dispone: "Se decretará judicialmente el divorcio, cualquiera que sea la forma de celebración del matrimonio, a petición de uno solo de los cónyuges, de ambos o de uno con el consentimiento del otro, cuando concurran los requisitos y circunstancias exigidos en el art. 81". Por su parte, el art. 81 del mismo Cuerpo legal, que regula la separación, exige como único requisito que hayan transcurrido, al menos, tres meses desde la celebración del matrimonio, sin perjuicio de que deba acompañarse a la demanda convenio regulador si el procedimiento se inicia a petición de ambos cónyuges o de uno de ellos con el consentimiento del otro, o propuesta de medidas definitivas cuando el procedimiento es contencioso.

En relación con los efectos personales y patrimoniales del matrimonio, con amparo en los arts 91 y ss del Código Civil, en especial los arts. 92.8, 93 y 96 CC, se propone la adopción de las siguientes medidas definitivas:

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

Ambos progenitores se harán cargo de los gastos en concepto de alimentos, en sentido amplio que necesite el/la hijo/a cuando esté bajo la respectiva custodia de uno y otro, según el anterior régimen establecido.

Los gastos de colegios, institutos, facultades o universidades de carácter Público donde curse estudios el/la hijo/a, así como las matrículas, serán abonados por mitad por ambos progenitores. En el caso de Centros Privados, se sufragarán por mitad siempre que haya acuerdo por ambas partes. En caso de desacuerdo, el exceso que suponga sobre el Centro Público será sufragado por el progenitor que haya decidido que realicen los estudios en el Centro Privado que finalmente haya elegido. Los relativos a gastos por clases extraordinarias de repaso, viajes escolares de las menores, tanto si se llevan a cabo en el mismo colegio o en un centro externo, serán a cargo, por mitad, de ambos progenitores, siempre que previamente hayan prestado su conformidad o así vengan recomendados por el centro escolar. Caso contrario, serán sufragados por el progenitor que haya decidido su realización.

Otros gastos extraordinarios, en concreto aquellos de naturaleza médica necesarios, no cubiertos por la Seguridad Social ni por cualquier otra mutualidad u organismo, serán abonados por mitad por ambos progenitores.

Si, tras cumplir los dieciocho años, el hijo se encuentra todavía en período de formación y no pueda mantenerse por sí mismo, ambos progenitores le prestarán los alimentos debidos de acuerdo con los arts. 142 y ss CC en proporción a sus respectivos recursos.

3) Atribución del uso de la vivienda familiar:

En relación con el uso de la vivienda familiar, así como del ajuar doméstico, se propone la atribución del mismo a mi mandante, por ser el suyo el interés familiar más necesitado de protección, en los siguientes términos:

III. COSTAS.- Cada parte deberá satisfacer sus propias costas y las comunes por mitad, salvo que la demandada en reconvención se oponga a las pretensiones de la demanda reconvencional, en cuyo caso procederá su condena al pago íntegro de las costas, conforme a lo dispuesto en el art. 394 de la Ley de Enjuiciamiento Civil.

En virtud de lo expuesto,

SUPLICO AL TRIBUNAL

Que tenga por presentado este escrito y los documentos que lo acompañan y por interpuesta en tiempo y forma DEMANDA RECONVENCIONAL y, previos los trámites procesales oportunos, dicte en su día sentencia por la que se acuerde la disolución del matrimonio por divorcio, con obligación de satisfacer cada parte sus costas y las comunes por mitad, salvo que el/la demandado/a reconvencional se oponga a esta pretensión, en cuyo caso procederá su condena al pago íntegro de las mismas, conforme a lo dispuesto en el art. 394 de la Ley de Enjuiciamiento Civil. Así miso, solicito que se adopten las siguientes medidas definitivas:

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma y número del Letrado	Firma del Procurador

========================================================================
