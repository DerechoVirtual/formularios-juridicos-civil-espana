---
name: demanda-divorcio-contencioso-alimentos-vivienda-hijo-civ-0046
description: "Demanda de divorcio contencioso con alimentos y vivienda para hijo mayor sin ingresos conviviente. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de divorcio contencioso con alimentos y vivienda para hijo mayor sin ingresos conviviente

> Formulario **CIV-0046** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Demanda de divorcio contencioso interpuesta por uno de los cónyuges, con petición de medidas definitivas: pensión de alimentos a favor de un hijo mayor de edad que convive en el domicilio familiar y carece de ingresos propios, y atribución del uso de la vivienda familiar al progenitor conviviente y al hijo mientras no alcance independencia económica.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de divorcio contencioso con alimentos y vivienda para hijo mayor sin ingresos conviviente» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de divorcio contencioso con alimentos y vivienda para hijo mayor sin ingresos conviviente” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-divorcio-contencioso-alimentos-vivienda-hijo-civ-0046`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (8 veces)
- [ ] IMPORTE (4 veces)
- [ ] Nº DE DOCUMENTO (4 veces)
- [ ] Nº DE DOCUMENTOS (4 veces)
- [ ] AÑO (3 veces)
- [ ] NOMBRE Y APELLIDOS DE LA DEMANDANTE (3 veces)
- [ ] NOMBRE Y APELLIDOS DEL DEMANDADO (3 veces)
- [ ] CALLE (2 veces)
- [ ] FECHA (2 veces)
- [ ] FIRMA (2 veces)
- [ ] SEDE (2 veces)
- [ ] COLEGIO
- [ ] DNI/NIE
- [ ] DOMICILIO
- [ ] DÍA
- [ ] EDAD
- [ ] EMPRESA
- [ ] ESTUDIOS
- [ ] FACULTAD
- [ ] FECHA DE NACIMIENTO
- [ ] FECHAS
- [ ] IMPORTE EN LETRA
- [ ] MES
- [ ] NOMBRE DEL HIJO
- [ ] NOMBRE Y APELLIDOS DEL ABOGADO/A
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] Nº DE COLEGIADO
- [ ] PROFESIÓN Y EMPLEO DEL DEMANDADO
- [ ] PROFESIÓN Y JORNADA
- [ ] RÉGIMEN
- [ ] TÍTULO DE ADQUISICIÓN
- [ ] UNIVERSIDAD

## Normas que cita el formulario

- art. 86 CC
- art. 770 LEC
- art. 93 CC
- art. 251 LEC
- art. 5 Ley Orgánica 1/2025
- art. 91 CC
- art. 143 CC
- art. 93.2 Código Civil
- art. 142 CC
- art. 146 CC
- art. 152 CC
- art. 142 Código Civil
- art. 143 Código Civil
- art. 152 Código Civil
- art. 93 Código Civil
- art. 96 CC
- art. 394 LEC
- art. 773.1 LEC

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

- Junto a «…r casado, como corolario legal del derecho del art. 32 CE a contraer matrimonio.»: el original citaba además el art. 81.2.º CC por remisión del art. 86 CC; comprobar la redacción vigente de los arts. 81 y 86 CC tras la Ley 15/2005 antes de mantener esa cita.

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

A LA SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD DEL TRIBUNAL DE INSTANCIA DE [SEDE]

[ELEGIR: A LA SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / A LA SECCIÓN CIVIL (O SECCIÓN ÚNICA) DEL TRIBUNAL DE INSTANCIA DE [SEDE], según la organización del Tribunal en el partido judicial]

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, que actúa en nombre y representación de Dña. [NOMBRE Y APELLIDOS DE LA DEMANDANTE], provista de DNI n.º [DNI/NIE], con domicilio en [LOCALIDAD], calle [CALLE], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], bajo la dirección del/la Letrado/a D./Dña. [NOMBRE Y APELLIDOS DEL ABOGADO/A], colegiado/a n.º [Nº DE COLEGIADO] del Ilustre Colegio de la Abogacía de [COLEGIO], cuyo despacho se abre en [LOCALIDAD], calle [CALLE], ante el Tribunal comparezco y como mejor en Derecho proceda, DIGO:

Que por medio del presente escrito, siguiendo la instrucción de mi mandante, vengo a formular demanda de DIVORCIO frente a su esposo D. [NOMBRE Y APELLIDOS DEL DEMANDADO], con domicilio actual en [DOMICILIO], ejercitando la acción prevista en el art. 86 CC y con base en los siguientes datos y argumentos:

HECHOS

PRIMERO.- Mi mandante contrajo matrimonio [ELEGIR: civil / canónico] con D. [NOMBRE Y APELLIDOS DEL DEMANDADO], en [LOCALIDAD], el día [FECHA], a cuya acreditación se acompaña certificación expedida por el Registro Civil de [LOCALIDAD], como documento n.º [Nº DE DOCUMENTO].

SEGUNDO.- Del referido matrimonio nació un hijo, de nombre [NOMBRE DEL HIJO], el [FECHA DE NACIMIENTO], que, teniendo [EDAD] años de edad, es mayor de edad pero sigue en el domicilio familiar y carece de independencia económica, puesto que cursa estudios de [ESTUDIOS] en la Facultad de [FACULTAD], con buen aprovechamiento académico.

Adjunto certificación de nacimiento del Registro Civil de [LOCALIDAD], certificados de matrícula y calificaciones académicas en la Universidad de [UNIVERSIDAD], que hacen los documentos números [Nº DE DOCUMENTOS].

TERCERO.- El régimen económico matrimonial es el de [ELEGIR: sociedad de gananciales, por la vecindad de los consortes y no haberse otorgado nunca capitulaciones matrimoniales / otro régimen: [RÉGIMEN]], siendo que mi patrocinada tiene empleo como [PROFESIÓN Y JORNADA] en [EMPRESA], mientras que el demandado es [PROFESIÓN Y EMPLEO DEL DEMANDADO], gozando de ingresos con los que es dable contribuir al mantenimiento de los gastos de manutención y de educación del hijo común.

Se adjuntan copias de las autoliquidaciones del I.R.P.F. de los ejercicios [AÑO] y [AÑO], de la actora y del demandado, como documentos números [Nº DE DOCUMENTOS].

CUARTO.- Atendiendo a los gastos de matrícula y mensualidades de la universidad, más los gastos necesarios propios de su edad de vestido y alimentación, consideramos que el padre debe contribuir a los alimentos de su hijo en la cantidad de [IMPORTE] euros mensuales. Se acreditan dichos extremos con los documentos números [Nº DE DOCUMENTOS].

QUINTO.- En la actualidad, mi mandante ocupa el domicilio conyugal junto al hijo habido del matrimonio, adquirido [ELEGIR: para la sociedad de gananciales por ambos cónyuges / por [TÍTULO DE ADQUISICIÓN]] mediante documento público (inscripción registral y certificado de empadronamiento del Ayuntamiento de [LOCALIDAD], documentos números [Nº DE DOCUMENTOS]).

SEXTO.- Por consecuencia de las desavenencias entre los cónyuges, mi representada está persuadida de lo adecuado de su decisión de disolver el vínculo matrimonial mediante divorcio, no habiendo sido posible tramitarlo de mutuo acuerdo, por lo que se interpone la presente demanda contenciosa.

SÉPTIMO.- La parte actora manifiesta que, previo a la presentación de la presente demanda, se han llevado a cabo negociaciones con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria, incluyéndose entre las acciones realizadas el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución.

Finalmente, mi representada envió un requerimiento fehaciente al demandado con fecha [FECHA], fijando un plazo de 30 días naturales para llegar a un acuerdo amistoso, a través del abogado que firma este escrito, el cual fue contestado por el demandado por el mismo medio, [ELEGIR: rechazando el acuerdo / habiendo sido solo posible un acuerdo parcial], viéndonos en la necesidad de acudir a la presente vía judicial, respecto a los extremos de la controversia en los que se mantiene la discrepancia.

Acompaño como documento nº [Nº DE DOCUMENTO] el requerimiento efectuado y como documento nº [Nº DE DOCUMENTO] la contestación del demandado.

A los anteriores hechos les son de aplicación los siguientes,

FUNDAMENTOS DE DERECHO

I.- Es competente el Tribunal de Instancia del lugar del domicilio del demandado, que es el criterio alternativo, a elección del demandante, conforme al art. 769.1, párrafo 1.º, LEC.

II.- El procedimiento adecuado es el del art. 770 LEC para conocer de las demandas de divorcio contenciosas.

III.- Tienen legitimación ordinaria, por hallarse en la situación jurídica de relación matrimonial, ambos cónyuges (arts. 86 CC y 10, párrafo 1.º, LEC), siendo el objeto de la pretensión principal la disolución vincular por divorcio.

Conforme al art. 93 CC, el progenitor conviviente detenta legitimación extraordinaria para recabar alimentos para el hijo mayor de edad que carece de medios de vida independiente del otro cónyuge progenitor, sin que ello suponga litisconsorcio necesario.

IV.- Se fija la cuantía de la demanda, en lo que tiene de estimable, por razón de la pretensión de medidas que incluye reclamaciones de pensiones periódicas, acumulada a la disolución vincular, en [IMPORTE] euros, en armonía con la regla 7.ª del art. 251 LEC.

V.- La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4.º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

VI.- El fondo de la pretensión consiste en la declaración de divorcio, a fin de la disolución del matrimonio, a instancia de uno de los cónyuges, de conformidad con el art. 86 CC, sin que pueda oponerse por el otro cónyuge ninguna causa de oposición material, al fundarse en la voluntad de no permanecer casado, como corolario legal del derecho del art. 32 CE a contraer matrimonio.

VII.- En orden a las medidas cuya adopción con carácter definitivo se interesan, se invoca como aplicable el art. 91 CC, que establece que «En las sentencias de nulidad, separación o divorcio, o en ejecución de las mismas, el Juez, en defecto de acuerdo de los cónyuges o en caso de no aprobación del mismo, determinará conforme a lo establecido en los artículos siguientes las medidas que hayan de sustituir a las ya adoptadas con anterioridad en relación con los hijos, la vivienda familiar, las cargas del matrimonio, liquidación del régimen económico y las cautelas o garantías respectivas, estableciendo las que procedan si para alguno de estos conceptos no se hubiera adoptado ninguna. Estas medidas podrán ser modificadas cuando se alteren sustancialmente las circunstancias».

VIII.- En cuanto al pronunciamiento sobre la pensión de alimentos a favor del hijo, el art. 93 CC, en su párrafo segundo, dispone que «Si convivieran en el domicilio familiar hijos mayores de edad o emancipados que carecieran de ingresos propios, el Juez, en la misma resolución, fijará los alimentos que sean debidos conforme a los artículos 142 y siguientes de este Código».

Efectivamente, los progenitores tienen el deber de ayudar económicamente a sus hijos, aunque lleguen a la mayoría de edad, en tanto no alcancen la posibilidad de proveer por sí mismos sus necesidades, de modo que la obligación de prestar alimentos corresponde a los padres respecto de sus descendientes, con independencia de la edad de estos, tal y como establece el art. 143 CC, siempre que se dé la situación de necesidad en los segundos y la posibilidad de prestarlos en los primeros.

Por lo demás, constituye doctrina jurisprudencial clara y consolidada, que compendia la STS de 24 de abril de 2000, rec. 4618/1999, aquella que afirma que, conforme a lo dispuesto en el art. 93, párrafo 2.º, CC, los hijos mayores de edad precisados de alimentos en sentido jurídico tienen derecho a los mismos, ya que la mayoría de edad no implica extinción «per se» del derecho a ellos. Por otra parte, tampoco cabe duda respecto al aspecto procesal según el cual en un juicio de separación, nulidad o divorcio únicamente pueden ser partes ambos cónyuges. Por lo tanto, será uno de ellos el que habrá de impetrar los derechos alimenticios de los hijos mayores de edad.

Así, señala la citada STS de 24 de abril de 2000, rec. 4618/1999, que «Del art. 93.2 del Código Civil emerge un indudable interés del cónyuge con quien conviven los hijos mayores de edad necesitados de alimentos a que, en la sentencia que pone fin al proceso matrimonial, se establezca la contribución del otro progenitor a la satisfacción de esas necesidades alimenticias de los hijos. Por consecuencia de la ruptura matrimonial el núcleo familiar se escinde, surgiendo una o dos familias monoparentales compuestas por cada progenitor y los hijos que con él quedan conviviendo, sean o no mayores de edad; en esas familias monoparentales, las funciones de dirección y organización de la vida familiar en todos sus aspectos corresponde al progenitor, que si ha de contribuir a satisfacer los alimentos de los hijos mayores de edad que con él conviven, tiene un interés legítimo, jurídicamente digno de protección, a demandar del otro progenitor su contribución a esos alimentos de los hijos mayores. No puede olvidarse que la posibilidad que establece el art. 93, párrafo 2.º del Código Civil de adoptar en la sentencia que recaiga en estos procedimientos matrimoniales, medidas atinentes a los alimentos de los hijos mayores de edad se fundamenta, no en el indudable derecho de esos hijos a exigirlos de sus padres, sino en la situación de convivencia en que se hallan respecto a uno de los progenitores, convivencia que no puede entenderse como el simple hecho de morar en la misma vivienda, sino que se trata de una convivencia familiar en el más estricto sentido del término con lo que la misma comporta entre las personas que la integran. De todo lo expuesto se concluye que el cónyuge con el cual conviven hijos mayores de edad que se encuentran en la situación de necesidad a que se refiere el art. 93, párrafo 2.º, del Código Civil, se halla legitimado para demandar del otro progenitor la contribución de éste a los alimentos de aquellos hijos, en los procesos matrimoniales entre los comunes progenitores».

A la hora de fijar una cuantía económica a prestar en concepto de alimentos hay que tener en cuenta lo señalado en los arts. 142, 146, 147 y 152 CC. Mientras que en el primero de estos preceptos se señala que dentro del concepto de alimentos se acogen también los gastos por educación y formación del hijo mayor de edad, cuando éste no haya terminado su formación por causa que no le sea imputable, los arts. 146 y 147 CC indican las circunstancias que determinarán la cuantía de esos alimentos: así, dicha cuantía será proporcionada al caudal o medios de quien los da y a las necesidades de quien los recibe, reduciéndose o aumentándose proporcionalmente según el aumento o disminución que sufran las necesidades del alimentista y la fortuna del que hubiera de satisfacerlos. Por su parte, en el art. 152 CC se señalan las causas por las que cesa la obligación de dar alimentos, entre las que se incluye: «cuando la fortuna del obligado a darlos se hubiere reducido hasta el punto de no poder satisfacerlos sin desatender sus propias necesidades y las de su familia» y «cuando el alimentista pueda ejercer un oficio, profesión o industria, o haya adquirido un destino o mejorado de fortuna, de suerte que no le sea necesaria la pensión alimenticia para su subsistencia».

Y con respecto a esta cuestión mantiene la doctrina de apelación un criterio uniforme en relación con la necesidad de examen de las pensiones de alimentos a favor de los hijos mayores de edad de forma individualizada en cada uno de los casos en los que se plantea, partiendo de unos principios que recoge, entre otras resoluciones, la SAP Murcia de 20 de diciembre de 2005, rec. 363/2005, según la cual «El derecho de alimentos entre parientes, entre los que se encuentran los hijos, bien sean mayores o menores de edad, descansa en principios de solidaridad familiar, alcanzando inclusive rango constitucional en lo concerniente a los hijos, según el artículo 39.2 y 3 CE, que sin embargo viene a distinguir entre la asistencia debida a los hijos durante su minoría de edad y en los demás casos en que legalmente proceda. Concretamente en cuanto a los hijos mayores de edad, los artículos 142 y siguientes del Código Civil configuran el derecho a los alimentos a favor de los mismos como una obligación legal que se impone a personas determinadas, como consecuencia de la vinculación con el beneficiario por vínculos de parentesco o estado, y que en sus límites obligacionales se concreta asimismo legalmente a lo indispensable para el sustento, habitación, asistencia médica, vestido y educación, derecho que subsiste en los hijos, aun después de la mayoría de edad, si permanece la situación de necesidad por causa que no sea imputable al alimentado, circunscribiendo la institución la obligación de prestar los citados alimentos a los sujetos que se encuentran dentro del círculo familiar, cual se previene en el artículo 143 del Código Civil, y cesará la obligación cuando el hijo no conviva en casa o tenga recursos propios, conforme señala el número 3 del artículo 152 del Código Civil, entendidos, no como una mera capacidad subjetiva de ejercer profesión u oficio, sino como una posibilidad real y concreta en relación con las circunstancias concurrentes, debiendo emplear el hijo la debida diligencia en la búsqueda de un trabajo, so pena de perder el derecho, salvo que no haya aún terminado su formación académica por causa que no le sea imputable. Asimismo, la pensión alimenticia a favor de los hijos, que tiene por finalidad cubrir las necesidades de los mismos, para su determinación es necesario tener en cuenta no sólo los ingresos y caudal del que ha de prestarlos sino también las necesidades de los hijos, que vendrán determinadas, entre otros factores, por su edad, sin olvidarse que son ambos progenitores los que han de contribuir a satisfacer dichas necesidades, debiendo ser conscientes aquellos de que la ruptura de la relación supondrá siempre unas pérdidas, que han de ser asumidas por ambos. La contribución de ambos progenitores debe ser en forma mancomunada y en cantidad proporcional a sus respectivos caudales, tal como reseñan los artículos 93 y 145 del Código Civil, y no tiene por finalidad el mantenimiento de un nivel de vida análogo al que la familia tenía constante matrimonio, ni la de compensar situaciones de desequilibrio económico, sino la de dar fiel cumplimiento a las necesidades alimenticias de los hijos, en el sentido que determina el artículo 142 del Código Civil, es decir, lo indispensable para el sustento, habitación, vestido y asistencia médica, como los gastos derivados de la educación e instrucción».

Por todo ello se valora la cuota mensual de la pensión alimenticia a favor del hijo en [IMPORTE EN LETRA] euros ([IMPORTE] €), como adecuada al caudal económico del sujeto obligado y a las necesidades del alimentista.

IX.- En cuanto al uso del domicilio familiar, se invoca como aplicable el art. 96 CC, a los fines de fundamentar la petición de que se atribuya el uso y disfrute a la esposa y a su hijo, ya que, aunque mayor de edad, sigue conviviendo en el domicilio familiar junto a su madre, en dependencia económica de sus progenitores, y en los casos en los que, como el presente, el hijo queda (por su propia decisión voluntaria, siendo mayor de edad) en el domicilio junto a su madre desde que se produjo la separación de hecho, el interés de éste vence a cualquier otro interés, no ostentando el padre un interés más digno de protección que aquél.

X.- No hay ninguna razón para excluir la aplicación del principio del vencimiento en punto a las costas procesales (art. 394 LEC), debiéndose condenar al demandado que se oponga, dado que el obtener la razón precisando de un proceso no ha de suponer una merma patrimonial del que tiene razón.

Y demás normas y jurisprudencia de general y pertinente aplicación.

En virtud de lo expuesto,

SUPLICO AL TRIBUNAL

Que, teniendo por presentado este escrito con los documentos que se acompañan y sus copias, se digne admitirlos, tenerme por comparecido/a y parte en la representación que ostento, entendiéndose conmigo las sucesivas diligencias, y por formulada demanda de disolución del matrimonio por divorcio, de modo que, seguido que sea el pertinente procedimiento, se dicte en su día sentencia por la que se declare el divorcio de los esposos D. [NOMBRE Y APELLIDOS DEL DEMANDADO] y Dña. [NOMBRE Y APELLIDOS DE LA DEMANDANTE], oficiándose al Registro Civil de [LOCALIDAD] para la anotación de su parte dispositiva en la inscripción del matrimonio, y se acuerden las siguientes medidas definitivas, que se podrán modificar si se alteraren sustancialmente las circunstancias:

1.º.- El establecimiento de una pensión alimenticia a favor del hijo mayor de edad de [IMPORTE] euros mensuales, pagadera por meses anticipados, actualizable anualmente conforme a las variaciones que experimente el Índice de Precios al Consumo que publique el Instituto Nacional de Estadística, u organismo oficial que lo sustituya.

2.º.- La atribución del uso de la vivienda conyugal a Dña. [NOMBRE Y APELLIDOS DE LA DEMANDANTE], así como al hijo mayor mientras no tenga independencia económica, así como del ajuar y mobiliario que en la misma se encuentra.

Es Justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

OTROSÍ DIGO: Que al amparo del art. 773.1 LEC, no habiéndose adoptado con anterioridad, se solicitan mediante el presente escrito MEDIDAS PROVISIONALES coetáneas a la admisión de la demanda, en base a los siguientes motivos: [EXPONER LOS MOTIVOS Y LAS MEDIDAS PROVISIONALES QUE SE SOLICITAN, p. ej. pensión alimenticia provisional a favor del hijo y atribución provisional del uso de la vivienda familiar, con los mismos fundamentos expuestos en esta demanda].

SUPLICO AL TRIBUNAL: Que se tengan por solicitadas las medidas provisionales indicadas y se acuerden en los términos interesados.

Reitero Justicia en el lugar y fecha «ut supra».

Firma del Abogado/a: [FIRMA] Firma del Procurador/a: [FIRMA]
