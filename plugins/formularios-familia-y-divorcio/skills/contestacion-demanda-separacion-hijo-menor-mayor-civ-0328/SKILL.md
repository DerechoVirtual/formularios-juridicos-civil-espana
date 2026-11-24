---
name: contestacion-demanda-separacion-hijo-menor-mayor-civ-0328
description: "Contestación a demanda de separación con hijo menor y mayor conviviente, y reconvención de divorcio. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contestación a demanda de separación con hijo menor y mayor conviviente, y reconvención de divorcio

> Formulario **CIV-0328** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Escrito de contestación a la demanda de separación de matrimonio con hijo menor e hijo mayor conviviente, formulando reconvención en la que se solicita el divorcio, así como la privación de la patria potestad del hijo menor de edad al padre.

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contestación a demanda de separación con hijo menor y mayor conviviente, y reconvención de divorcio» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contestación a demanda de separación con hijo menor y mayor conviviente, y reconvención de divorcio” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:contestacion-demanda-separacion-hijo-menor-mayor-civ-0328`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] NÚMERO (4 veces)
- [ ] IMPORTE (3 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] FECHA (2 veces)
- [ ] NOMBRE DEL HIJO/A (2 veces)
- [ ] AÑO
- [ ] CALLE
- [ ] ENFERMEDAD
- [ ] LUGAR

## Normas que cita el formulario

- art. 81.2.º CC
- art. 91 CC
- art. 774 LEC
- art. 394 LEC
- art. 409 LEC
- art. 253 LEC
- art. 251 LEC
- art. 93 CC

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

AL TRIBUNAL

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, que actúa en nombre y representación de Dña. [NOMBRE Y APELLIDOS], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], bajo la dirección del/la Letrado/a Dña. [NOMBRE Y APELLIDOS], colegiada n.º [NÚMERO] del Iltre. Colegio de [LOCALIDAD], con despacho abierto en [LOCALIDAD], calle [CALLE], n.º [NÚMERO], en autos de Juicio de Separación matrimonial n.º [NÚMERO]/[AÑO] promovido por D. [NOMBRE Y APELLIDOS], ante el Tribunal comparezco y como mejor proceda en Derecho, DIGO:

Que, en la representación que ostento y dentro del plazo legal, vengo a CONTESTAR a la demanda y formular RECONVENCIÓN.

1º.- Fundamento la CONTESTACIÓN A LA DEMANDA en los siguientes hechos y consideraciones jurídicas.

HECHOS

PRIMERO.- De acuerdo con los correlativos de la demanda sobre los datos del matrimonio celebrado, y separación conyugal de hecho.

SEGUNDO.- Por la relación conflictiva entre los casados, difícil hasta el momento de ser documentada la separación de hecho, al traducirse en un trato insoportable por los evidentes problemas psíquicos del hijo común menor [NOMBRE DEL HIJO/A], con culpabilización absurda de la madre, ésta tiene decidida la disolución del vínculo conyugal con el demandante.

TERCERO.- Incierta la integridad de la versión del correlativo, en cuanto que para nada tiene en cuenta la existencia de [NOMBRE DEL HIJO/A], hijo común de los casados, mayor de edad, pero que convive sin independencia económica con mi representada.

Se acompaña como documento n.º [NÚMERO] certificado municipal de convivencia.

CUARTO.- El hijo menor no sólo padece la enfermedad genética señalada, sino que sufre la dolencia crónica de [ENFERMEDAD], que precisa del cuidado constante de quien, como su madre que es doctora en medicina, y que dispone de autonomía profesional para tenerle permanentemente en compañía, es capaz de proporcionar. El padre, según la demanda reconoce, está viajando continuamente, y su actual residencia está alejada del domicilio familiar y de la consulta de mi patrocinada en la localidad de [LOCALIDAD] Se acompañan informes médicos relativos al padecimiento del hijo como documentos nos. y [Nº DE DOCUMENTO].

QUINTO.- En cuanto a la obligación de mantenimiento del hijo menor, ha de tenerse en cuenta, por su proporcionalidad a los recursos económicos de los padres, no sólo que la madre custodia goza de unas rentas suficientes, sino que el demandante, que dice en la demanda ser agente comercial, en realidad tiene título de ingeniero y desempeña un importante cargo en la empresa [DENOMINACIÓN SOCIAL]., adjuntándose a esta exposición, como documentos nos. y [Nº DE DOCUMENTO], copia de la última declaración de IRPF de D. [NOMBRE Y APELLIDOS] que ha tenido en su poder mi mandante, y certificado del plan de pensiones con la entidad [DENOMINACIÓN SOCIAL], en que consta el capital acumulado al [FECHA].

FUNDAMENTOS DE DERECHO

I.- Conformes con la competencia objetiva y territorial del Tribunal, la legitimación de los cónyuges, y el procedimiento adecuado escogido, compareciendo esta parte con la debida representación técnica y asistencia letrada.

II.- El fondo de la pretensión actora consiste en la declaración de separación conyugal a instancia del marido, y al no producirse por causa legal alguna, sino por la pura voluntad del casado ex art. 81.2.º CCiv, tampoco puede oponer mi representada a esa voluntad de que continúen los efectos de vida en común del matrimonio motivos materiales a la consideración judicial.

Sin embargo, la separación matrimonial, como fórmula autónoma, no puede evitar que cada cónyuge decida libremente que no desea mantenerse en el matrimonio, con lo que la disolución pedida por la esposa enerva las razones que puedan existir para mantenerlo en la intención del esposo.

III.- Conforme a los arts. 91 y 106 CCiv y art. 774 LEC, el Tribunal deberá pronunciarse en definitiva sobre las determinadas medidas, con independencia de lo que solicita el actor o lo que se adoptara como medidas provisionales previas, con oposición de mi mandante.

Las condiciones de tales medidas, para regular las resultancias del divorcio, deberán asumirse con arreglo a los hechos reseñados, y según se pedirá en la reconvención expresa.

IV.- Las costas procesales deben ser impuestas a la parte demandante, al ver desestimadas sus precisas pretensiones, con arreglo al art. 394 LEC

Por todo lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito y por formulada en tiempo y forma contestación a la demanda, se digne admitirla a trámite junto con los documentos de fondo acompañados, y previo el procedimiento que le corresponda, se venga dictar sentencia por la que, con desestimación íntegra de la demanda, se absuelva libremente a la demandada de cuantos concretos pedimentos se le dirigen, con expresa condena en costas de la parte actora.

2º.- Al propio tiempo esta parte formula RECONVENCIÓN contra el actor D. [NOMBRE Y APELLIDOS] en solicitud del pronunciamiento que en el suplico se concretará, y que se basa en los siguientes:

HECHOS

PRIMERO.- Se tienen por expresamente reproducidos los hechos que, al contestar a la demanda, se han ordenado como realidad adversa a la que relaciona la demanda.

SEGUNDO.- En cuanto al hijo mayor de edad, encontrándose sin empleo, finalizados sus estudios, y cohabitando con su madre, obviamente le corresponde al padre sufragar todas sus necesidades de costumbre.

FUNDAMENTOS DE DERECHO

I.- Es Juez competente para conocer de la demanda reconvencional el que esté conociendo de la demanda principal.

II.- Conforme al artículo 409 LEC, la reconvención se sustanciará y resolverá al propio tiempo y en la misma forma que la cuestión principal del pleito y será resuelta con éste en la sentencia definitiva.

III.- Las partes en la cuestión reconvencional son las mismas que en la demanda principal, pero con su papel invertido, esto es, el actor en la principal es aquí el demandado reconvencional, y el demandado es aquí demandante reconvencional.

IV.- Conforme a la admonición del art. 253 LEC, puesto que se reclama una prestación pecuniaria, junto con materias inestimables o de cuantía indeterminable, cifro la cuantía de esta reconvención en [IMPORTE] euros, que es la pensión alimenticia anualizada multiplicada por diez, en armonía con la regla 7ª del art. 251 LEC.

V.- Fundamento legal de la reconvención:

Las pretensiones que, sobre desechar la ejercida por D. [NOMBRE Y APELLIDOS], vienen a ampliar objetivamente el proceso, radican de una parte, en que se pide, con arreglo a la previsión del art. 770.2.ª.b) LEC, el divorcio del matrimonio, en cuanto que el libre derecho a dejar de estar casado, sin precisión de invocar o demostrar causa material alguna enerva el otro derecho autónomo, igualmente libre, a la separación legal, de modo que la voluntad de disolver el vínculo de uno de los cónyuges prevalece y se sobrepone a un cese de convivencia, que ya preexiste, al igual que a una mera separación, que no extingue el matrimonio, y en la que no están conformes ambos casados. Basta que uno de los cónyuges no desee la continuación del matrimonio para que pueda pretender el divorcio, sin que se le puedan oponer motivos materiales.

De otra parte, según previene el art. 770.2.ª.d) LEC, se acumula la pretensión de medidas definitivas que no hubieran sido solicitadas en la demanda y sobre las que el tribunal no debe pronunciarse de oficio. Sobre las de determinación oficial, bien que para las consecuencias del divorcio, se pedirá con plena falta de sintonía con las solicitudes de la demanda, pero entre las no oficiales, se cuenta la de alimentos del hijo mayor de edad que convive y depende económicamente de la demandada.

Conforme al art. 93 CCiv el progenitor conviviente detenta legitimación extraordinaria para recabar alimentos para el hijo mayor de edad que carece de medios de vida independiente del otro cónyuge progenitor, sin que ello suponga litisconsorcio necesario.

En la solicitud de medidas contradictorias, en todo o parte, o sencillamente diferentes de las solicitadas por el demandante, en coherencia con la oposición a las medidas provisionales que se mantuvo en su día

VI.- Con arreglo al artículo 394 LEC han de imponerse al demandado reconvencional, por el vencimiento.

Por lo expuesto,

SUPLICO AL TRIBUNAL.

Que teniendo por presentado este escrito y por formulada en tiempo y forma demanda reconvencional, la admita a trámite y previos los que le correspondan al juicio de separación matrimonial en el que se ha presentado, se sirva dictar sentencia en la que, además de la desestimación de la demanda principal formulada por D [NOMBRE Y APELLIDOS], se estime la presente RECONVENCIÓN, declarando:

a) La disolución del matrimonio de D. y Dña. por divorcio.
b) La guarda y custodia del hijo menor de edad correspondiente a la madre, así como la patria potestad, privándose de la misma al padre.
c) La provisional denegación al padre del derecho de comunicación y estancia respecto del hijo menor, en tanto no transcurra un tiempo que prudencialmente fije SSª, cuando se precisará si el hijo puede prescindir de la atención especial actual y si es apto el estado mental del padre, y en todo caso, se lleven a cabo las comunicaciones en el domicilio de la madre y en su presencia.
d) La atribución del uso de la vivienda conyugal para el hijo menor de edad y su madre, así como para el hijo mayor mientras no tenga independencia económica, así como del ajuar y mobiliario que en la misma se encuentra.
e) La fijación para el hijo menor a cargo del padre de una pensión de alimentos en cuantía de [IMPORTE] euros mensuales, y para el hijo mayor en cuantía de [IMPORTE] euros mensuales, con independencia de que se determine la obligación del padre de contribuir a la satisfacción de los gastos extraordinarios que las necesidades de dichos descendientes precisen, actualizable en cuantía equivalente a las variaciones que experimenten los ingresos del demandante reconvenido, a partir del 1 de enero del año siguiente a que se dicte la sentencia.
f) Se proceda a liquidar la sociedad de gananciales previamente disuelta por capitulaciones matrimoniales, de forma que, con independencia de la atribución que se determine de la propiedad de los bienes se respete el uso y disfrute exclusivo de los citados al hijo y al cónyuge con el cual convive.

Todo ello con expresa imposición de costas a la parte contraria.

Es de Justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a

========================================================================
