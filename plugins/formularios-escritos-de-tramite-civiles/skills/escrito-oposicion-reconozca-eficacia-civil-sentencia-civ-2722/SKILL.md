---
name: escrito-oposicion-reconozca-eficacia-civil-sentencia-civ-2722
description: "Escrito de oposición a que se reconozca eficacia civil a la sentencia canónica de nulidad. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito de oposición a que se reconozca eficacia civil a la sentencia canónica de nulidad

> Formulario **CIV-2722** del plugin **Escritos de trámite en el proceso civil** (`formularios-escritos-de-tramite-civiles`) · Civil › Escritos procesales (demanda, contestación, prueba, vista) · normativa revisada el 25-11-2026.

## Qué es

Escrito de oposición a la demanda de solicitud de la eficacia en el orden civil de sentencia canónica dictada por el Tribunal eclesiástico sobre nulidad matrimonial, no solicitando la adopción o modificación de medidas.

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito de oposición a que se reconozca eficacia civil a la sentencia canónica de nulidad» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito de oposición a que se reconozca eficacia civil a la sentencia canónica de nulidad” para mi caso». También puedes invocarla directamente con `/formularios-escritos-de-tramite-civiles:escrito-oposicion-reconozca-eficacia-civil-sentencia-civ-2722`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-escritos-de-tramite-civiles:indice`.

## Qué contiene esta skill

- `SKILL.md` (este fichero): qué es el formulario, para qué sirve, cómo se usa, los datos que pide, las normas que cita, los avisos de actualización y las instrucciones para Claude.
- `assets/formulario.md`: el formulario seco, tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…]. Es el texto que se rellena; no lleva explicaciones.
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Escritos de trámite en el proceso civil) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] COMPLETAR (6 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] FECHA (3 veces)
- [ ] NÚMERO (2 veces)
- [ ] AÑO
- [ ] DESCRIBIR
- [ ] LUGAR
- [ ] Nº
- [ ] Nº DE COLEGIADO/A
- [ ] Nº DE DOCUMENTO
- [ ] TIPO Y Nº DE PROCEDIMIENTO

## Normas que cita el formulario

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

- Junto a «… DE INSTANCIA [ELEGIR: SECCIÓN CIVIL / SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD]»: Denominación legal: Sección de Familia, Infancia y Capacidad. Si no existe en el partido, conoce la Sección Civil o la Única (art. 86.3-4 LOPJ). Fuente: LOPJ arts. 84.2.a) y 86 (redacc. LO 1/2025, BOE-A-2025-76).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Notas al pie del formulario original:
(1) EFICACIA CIVIL DE LAS RESOLUCIONES ECLESIASTICAS

Al respecto hay que tener en cuenta el artículo 99 del Reglamento (UE) 2019/1111 del Consejo, de 25 de junio de 2019, relativo a la competencia, el reconocimiento y la ejecución de resoluciones en materia matrimonial y de responsabilidad parental, y sobre la sustracción internacional de menores.

Por su parte, el artículo VI, 2 de los Acuerdos entre España y la Santa Sede, concretamente, el de Asuntos Jurídicos de 3 de enero de 1979, ratificado por Instrumento de 4 de diciembre de 1979 (BOE 15 Dic. 1979), tratado internacional firmado al amparo del art. 16.3 CE, faculta a los cónyuges a acudir a los Tribunales Eclesiásticos solicitando la declaración de nulidad del matrimonio canónico o la decisión del Papa sobre matrimonio rato y no consumado (los Tribunales eclesiásticos mantienen competencia para dictar tales resoluciones), pero para que dicha resolución dictada por un Tribunal Eclesiástico, sea este residente en España o en cualquier país del extranjero, alcance eficacia civil en el Derecho interno español (los efectos de cosa juzgada) como si de una sentencia de un juez civil español se tratara, se ha de seguir los trámites señalados en el artículo 778 LEC, sin necesidad de acudir al procedimiento de homologación llamado de exequatur ("procédase"), lo que se recoge en el art. 80 CC, que se remite -en cuanto a la regulación sustantiva del reconocimiento de su eficacia civil- a los requisitos para el reconocimiento de resoluciones extranjeras o ‘exequatur’; actualmente arts. 44 y ss. de la Ley 29/2015, de 30 de julio, de cooperación jurídica internacional en materia civil (AATS de 11 de enero de 1983 y 23 de enero de 1984, entre otros, puesto que las resoluciones de la Iglesia católica sean del país que sean no tienen carácter de extranjeras).

Las "solicitudes" para la eficacia civil de las resoluciones dictadas por los Tribunales eclesiásticos sobre nulidad del matrimonio canónico o las decisiones pontificias sobre matrimonio rato y no consumado han de presentase en forma de demanda por cualquiera de las partes, ante los tribunales del Estado con los requisitos objetivos y de forma de esta clase de documentos (art 399 LEC), solicitando la eficacia civil de la sentencia eclesiástica, y expresando si se solicita medida complementaria alguna o no o la modificación si ya existían medidas adoptadas con anterioridad.

Así, habrá de acompañarse, además de la certificación del registro electrónico de apoderamientos judiciales o referencia al número asignado por dicho registro (art 264.1º LEC), el testimonio literal auténtico de la resolución de cuya eficacia se trata, la diligencia de firmeza y de que no ha sido dictada en rebeldía.

Si el Tribunal eclesiástico fuera extranjero habrán de cumplirse los requisitos que establecen en los artículos 144, 265 y 273 de la Ley de Enjuiciamiento Civil, es decir, que en caso de estar redactado en un idioma que no sea el castellano, se acompañarán la traducción del mismo y copias de aquél y de ésta

En la nueva regulación hay diferencias importantes, en tanto el procedimiento varía, según que se solicite o no en la demanda, al propio tiempo, la adopción o modificación de medidas, a saber:

1. Si en la demanda no se pretende la adopción de medidas complementarias cautelares matrimoniales o la modificación de las que pudieran ya estar adoptadas en un procedimiento previo de carácter civil, el procedimiento es semejante al que previera la Disposición Adicional Segunda de la Ley 30/1981, en tanto se inicia por la demanda que presente cualquiera de los cónyuges, sigue con la admisión de la demanda mediante auto (art. 206.2.2ª LEC), en el que se acuerda dar audiencia al otro cónyuge y al Ministerio Fiscal, por plazo de 10 días (no por nueve días como expresaba la anterior normativa), y se resolverá por medio de auto lo que corresponda acerca de dicha eficacia.

Al igual que sucediera en aquélla, la nueva norma tampoco expresa si este plazo ha de ser simultáneo o sucesivo, laguna que la doctrina científica y la práctica forense han colmado entendiendo que se trata de un plazo simultáneo (Fernández-Ballesteros, Rifá y Valls).

El Juez dará audiencia, dice el texto legal, aunque lo que debe interpretarse es que se dará traslado a la otra parte y al Ministerio Fiscal, para que en el plazo de diez días alegue lo que estime necesario. Esta alegación, en el caso de la parte, por lógica, debe reunir los mismos requisitos objetivos y formales que una contestación a la demanda, es decir, ir firmada por abogado y procurador y conteniendo los elementos propios de este tipo de escritos, aunque si el objeto es manifestar su conformidad con la autenticidad de la sentencia y con su contenido, reconociendo la eficacia civil de lo acordado por la sentencia cuya validez se trata de reconocer, entendemos que es posible que se realice por comparecencia ante el Tribunal.

El contenido, tanto de la contestación de la parte como de la actuación del Fiscal, puede ser el de manifestar su conformidad con la autenticidad de la sentencia y con su contenido, reconociendo la eficacia civil de lo acordado por la sentencia cuya validez se trata de reconocer, o bien el de manifestar su oposición a la misma.

Transcurrido este plazo, el Tribunal dictará auto resolviendo lo que proceda. No se dice el plazo para dictar la resolución, si bien por aplicación analógica de otros preceptos similares, puede estimarse que será el plazo de cinco días.

Nada dice el texto legal si la demanda puede solicitarse de común acuerdo en este supuesto, pero en el caso de que así sea (lo que parece posible a tenor del artículo 770.5 LEC al que remite en bloque el art. 788.2 de La LEC para el supuesto que se soliciten medidas o su modificación), entendemos que bastará con dar audiencia al Ministerio Fiscal, por el plazo de diez días, y dictar el oportuno auto.

Otra omisión se refiere a los efectos de la oposición del otro cónyuge o del Fiscal a que se reconozca la eficacia civil, y en su caso, el cauce para tramitarla. Entendemos que, frente a la solución dual preconizada por la Disposición Adicional Segunda de la Ley 30/1981, la LEC 1/2000 se dispone que cualquiera que sea el contenido de las alegaciones que evacuen los demandados -de conformidad u oposición a la solicitud deducida, fundada o meramente formularia, razonable o disparatada-, o si dejan transcurrir el plazo sin hacerlo, el Juez ha de resolver definitivamente por medio de auto sobre el fondo de la pretensión deducida, acordando o denegando la eficacia civil postulada según que, respectivamente, concurran o no los presupuestos formales o procesales -firmeza y ejecutoriedad; que haya existido posibilidad de efectiva contradicción (inexistencia de rebeldía); autenticidad de la ejecutoria- y materiales -que la resolución de que se trate no contradiga el orden público interno- a que se subordina la concesión de la tutela --vid. STS, Sala Primera, de 1 de julio de 1994--, sin que la oposición impida la homologación civil, vetando que se pueda acudir a un juicio ordinario, con la duda entre el proceso ordinario o el verbal especial del artículo 770.

En consecuencia, parece que con la nueva regulación no nos hallamos ante una intervención judicial «al modo de la jurisdicción voluntaria, que responde a una actividad de constatación encomendada al juez civil que ha de incluirse entre las funciones que de acuerdo con el art. 117.4 CE puede atribuir la Ley expresamente al Juez en garantía de cualquier derecho...», como sostuvieran las SSTC 93/1983, de 8 de noviembre y 328/1993, de 8 de noviembre, dictadas en interpretación de la Disposición Adicional Segunda de la Ley 30/1981, máxime cuando a falta de norma explícita en contrario, la citada resolución es apelable en el plazo de cinco días para ante la Audiencia Provincial al tratarse de un auto definitivo (art. 455, núms. 1 y 2.2.º LEC 1/2000).

Respecto de este procedimiento, la Circular 1/2001, de 5 de abril, de la Fiscalía General del Estado, sobre la incidencia de la nueva Ley de Enjuiciamiento Civil en la intervención del Fiscal en los procesos civiles, señala que: "El párrafo 1 del art. 778 LEC instituye un verdadero proceso especial en el que se sustancian las demandas en solicitud de eficacia civil de las resoluciones dictadas por tribunales eclesiásticos sobre nulidad del matrimonio católico o sobre las decisiones pontificias sobre matrimonio rato y no consumado. Se trata de un proceso especial y sumario ya que, presentada la demanda, el tribunal competente da audiencia por plazo de diez días al otro cónyuge y al Ministerio Fiscal para que aleguen frente a la demanda lo que estimen procedente, resolviendo el tribunal la cuestión mediante Auto. Este procedimiento especial es autónomo y autosuficiente, de ratio limitada, y puede llevar aparejada la solicitud de adopción o modificación de medidas.

2. Si en la demanda se pretende la adopción de medidas complementarias matrimoniales o la modificación de las que pudieran ya estar adoptadas, el art. 778.2 dispone la sustanciación conjunta de ésta con la pretensión principal de eficacia civil de la resolución o decisión canónica, remitiéndose al «procedimiento que corresponda con arreglo a lo dispuesto en el art. 770» (conforme a la corrección de errores publicada en el BOE núm. 18, del día 28 julio 2001, que vuelve a corregir la corrección de errores publicada en el BOE número 90, del día 14 de abril de 2000, que se remitía al art. 775, la que deja sin efecto, de acuerdo con la publicación inicial de la Ley 1/2000, de 7 de enero, que tuvo lugar en el BOE número 7, de 8 de enero de 2000), donde se regula el procedimiento procedimiento principal para la sustanciación de las demandas de separación y divorcio.

Consecuentemente se podrán acumular a la petición de eficacia civil de la sentencia canónica, cualesquiera otros relativas a los efectos subsiguientes en orden a las medidas del art. 91 ss del Código Civil, incluso, en su caso la modificación (SAP Málaga 21 Abr. 1992).

La citada Circular 1/2001, de 5 de abril, de la Fiscalía General del Estado señalaba respecto a la redacción anterior a la corrección de errores publicada en el BOE núm. 18, del día 28 julio 2001 que: "Cuando además de la pretensión de eficacia civil de las resoluciones eclesiásticas se insta la adopción de medidas, el párrafo 2 del art. 778 no crea otro procedimiento distinto, sino que manteniendo la sumariedad esquemática del párrafo primero, inserta en el mismo, a modo de incidente, de la misma manera que en otros procesos regulados en el Capítulo IV del Título I del Libro IV LEC, el trámite para solventar la petición de modificación o adopción de medidas" ... resultando tal regulación "mucho más coherente y sistemática, ya que manteniéndose el esquema sumario del procedimiento creado en el párrafo 1 del art. 778, se rellena con la remisión al art. 775 la necesidad de proveer a la adopción de medidas o su modificación, ya que este precepto sí que está diseñado para la materia propia del tratamiento de las medidas".

Entendemos que el presente procedimiento debe encuadrarse dentro de un procedimiento tipo entre la variedad de juicios declarativos existentes en nuestro sistema procesal, si bien el legislador los ha incluido dentro de los procedimientos especiales a considerar dentro de los procesos matrimoniales, puesto que comienza por demanda, si bien lo estructura con base en dos posibilidades procedimentales distintas (arts. 748.5º y 778 LEC)

La solución que contenía la Ley con anterioridad a la corrección de errores publicada en el BOE núm. 18, del día 28 julio 2001, de hacer depender la sustanciación contenciosa o consensual de la petición principal no ya de la existencia o no de oposición a propósito de la misma, sino de la petición accesoria de medidas, producía cierta perplejidad y extrañeza, al igual que la remisión procedimental que se hacía al artículo 775, en tanto se trata de adoptar las medidas inicialmente y no su modificación, sin que participen de la naturaleza cautelar o provisional.

Así, con la regulación aprobada en el caso de adopción inicial de medidas habrá de acudirse al proceso contencioso del artículo 770 o al proceso consensual del art. 777, según se presenten las medidas sin acuerdo o de mutuo acuerdo.

En cuanto a la adopción o modificación de las medidas habrá de estarse según los casos a lo previsto para la modificación de las adoptadas con anterioridad a la demanda (art. 772), o para la adopción ex novo de medidas interesadas junto con la demanda (art. 773) o para la modificación de las medidas (art. 775).

La modificación de las medidas lo podrán ser por haber solicitado la adopción de medidas provisionales en el orden civil, independientemente de la tramitación del procedimiento de nulidad canónica, pues aquellas no son incompatibles con éste, pudiendo acudir las partes de forma paralela, es más, suele ser frecuente esta coincidencia en el tiempo.

En todo caso debe destacarse que no se considerarán «medidas» en sentido propio a los efectos de que, en su caso, se inste la modificación a que se refiere este precepto las que haya podido adoptar la resolución canónica de cuya eficacia se trate, en cuanto que los efectos civiles de las resoluciones eclesiásticas son de la exclusiva competencia de los órganos jurisdiccionales civiles --STC de 13 de enero de 1997--. En consecuencia, se ha de tratar de medidas coetáneas al proceso canónico solicitadas del Juez de Primera Instancia competente ex art. 769 (SAP de Zaragoza, Secc. 2.ª, de 16 de marzo de 1996).

La solicitud de modificación de medidas cabrá también si ha habido antes una sentencia de separación o divorcio, que no impide la eficacia civil de la resolución eclesiástica; aunque parece que no cabrá si ha habido antes una sentencia civil de nulidad, ya que a diferencia de lo que sucede en el procedimiento de exequatur en el que se aprecia la litispendencia cuando existe un procedimiento incoado sobre el mismo objeto (salvo que exista un Tratado que la excluya), en el ámbito que comentamos, cabe la simultánea tramitación de una causa de separación, divorcio y la de nulidad eclesiástica ante los Tribunales canónicos, pudiendo ser esta última ejecutada sin perjuicio de que el Juez ordinario decida con plena jurisdicción sobre los efectos civiles.

La doctrina controvierte acerca si se puede instar o no en concepto de «medidas» la modificación de las definitivas convenidas o decretadas como consecuencia de un precedente proceso de separación o de divorcio. En contra de esta posibilidad se argumenta que por esta vía, en último término, unas medidas «provisionales» estarían reemplazando a otras definitivas adoptadas en una sentencia firme. A favor de la postura positiva milita la concurrencia de eadem ratio y la previsión del art. 775.3, que se remite a lo dispuesto en el art. 773.

Por otra parte, por analogía con lo dispuesto en el art. 773.4, parece que el demandado no podrá pedir medidas más que en los casos en que no se hubieran adoptado con anterioridad o no hubieran sido solicitadas por el actor.

Lo significativo viene dado por lo suprimido en comparación con la regulación hasta ahora vigente. Es curioso, y nos atrevemos a decir que es tremendamente significativo, que una ley con abundantes incursiones de regulación sustantiva calle toda mención a los requisitos necesarios para el reconocimiento de la eficacia civil, de manera que hay que acudir al artículo 80 del Código Civil que, a su vez, nos remite a los requisitos para el reconocimiento de resoluciones extranjeras o ‘exequatur’; actualmente arts. 44 y ss. LCJI. Habrá que aplicar toda la doctrina constitucional recaída sobre los aspectos de fondo, que la nueva ley en nada afecta.

Por último, ha de resaltarse que el conflicto jurisdiccional entre una sentencia firme de divorcio, con sus consiguientes efectos económicos, y otra posterior de nulidad canónica, también firme, cuyos efectos civiles fueron igualmente reconocidos y fijados, ha de resolverse manteniendo los efectos acordados en la sentencia de divorcio, ya que la existencia de una sentencia firme de nulidad canónica y el subsiguiente reconocimiento de sus efectos civiles no puede estimarse como cambio sustancial de circunstancias, para dejar sin efecto lo acordado en la sentencia firme de divorcio. Llegar por este solo hecho a la solución contraria sería tanto como otorgar a la jurisdicción canónica efectos de prevalencia civil sobre los jueces y Tribunales del Estado, hecho que impide en absoluto el principio de exclusividad jurisdiccional (Cfr. AP Sevilla S 2 Nov. 1993 y TS 1.ª S 5 Mar. 2001.-Ponente: Sr. Almagro Nosete. La Ley, 2001, 3234).

COMPETENCIA.

Era norma habitual, conforme a la Ley de 1881, que en los casos en los que, paralelamente al proceso canónico, se hayan seguido medidas provisionales, se dirija la demanda directamente a este Tribunal sin necesidad de que tenga que pasar por reparto. Los Tribunales que conocieron de aquéllas suelen tramitarlas por antecedentes.

No obstante, la nueva Ley de Enjuiciamiento Civil que deroga la mencionada Ley de 1881, nada dice sobre la competencia debiendo entenderse por tanto que será la misma que para las demás cuestiones matrimoniales, y que se comprenden en el artículo 769 de dicha Ley Procesal en el que se establecen criterios de competencia territorial y la imposibilidad de sumisión para fijar el fuero.

Por ello, como en todos los supuestos de demandas matrimoniales deberá acreditarse la competencia territorial del órgano ante el que se presenta, por los medios ordinarios.

RESOLUCIONES ECLESIÁSTICAS SUSCEPTIBLES DE SER OBJETO DE CONVALIDACIÓN. REQUISITOS DE HOMOLOGACIÓN.

Según la jurisprudencia de la Sala Primera del TS (1 de julio de 1994, y 5 Mar. 2001, Ponente: Sr. Almagro Nosete, La Ley, 2001, 3234) y la Jurisprudencia menor, la eficacia en el orden civil de las sentencias canónicas depende exclusivamente, sin mayores cortapisas, al igual que cualquier otra resolución dictada por Tribunales extranjeros, de la superación de un juicio de homologación, que se ciñe a dos extremos concretos: a) autenticidad de la sentencia firme, esto es, comprobación o verificación de su validez extrínseca -en otras palabras, que el documento sea veraz y no falso o falsificado-, y b) adecuación de la sentencia, en su contenido, al Derecho del Estado, lo cual comporta un examen de fondo que sólo se extiende a constatar sí las declaraciones de la sentencia, conforme al Derecho canónico, no están en contradicción con los conceptos jurídicos y disposiciones equiparables o análogas del Derecho estatal, de manera que no se vea perjudicado o alterado el sistema de libertades públicas y derechos fundamentales del ciudadano. Al margen de estas verificaciones, el juicio de homologación no debe extenderse a hacer nuevos pronunciamientos que desvirtuarían su naturaleza y excederían del cometido que tiene atribuido por ley.

En consecuencia, pese a no consignarse la obligación, de carácter procesal, establecida por el propio art. 80 CC, han de concurrir los siguientes requisitos:

a) Que la resolución se refiera al fondo de la causa del matrimonio sobre nulidad de matrimonio canónico, o las resoluciones pontificias, sobre matrimonio rato y no consumado (art. 80 CC). Ha de tratarse de sentencias dictadas por Autoridad competente canónica en materias reservadas a la jurisdicción eclesiástica, en el ejercicio de acciones personales.

No es posible la homologación de otras resoluciones como las sentencias canónicas de disolución del vínculo fundadas en los privilegios paulino (que disuelve el matrimonio consumado entre bautizados) o petrino, ni las recaídas en causas de separación quo ad thorum -SAP de Pamplona, de 8 de mayo de 1981- ya que la separación es competencia exclusiva del Estado. Por otra parte, hay que destacar que el divorcio no reconocido por la Iglesia Católica.

b) Que la resolución cuya eficacia se pretende obtener sea firme y ejecutoria en el ámbito canónico, ya que no se puede solicitar la eficacia civil de una resolución canónica cuando aún no es firme ni ha surtido efectos en el ámbito del que emana.

c) Que la resolución tenga el carácter de autentica para que haga fe.

d) Ausencia de rebeldía y necesidad que se observe el principio de audiencia bilateral, lo que es interpretado en el sentido de que el demandado haya tenido oportunidad de intervenir en el proceso cuya resolución se pretende homologar, lo que se cumple en los casos de rebeldía voluntaria o por conveniencia, en los cuales la ausencia es voluntaria tras el traslado de la pretensión en debida forma, dándosele la posibilidad de defenderse de ella o alegar lo que le conviniere; o de rebeldía por convicción, es decir, al no reconocer la jurisdicción del Tribunal. Por tanto, sólo la genera una situación de falta de la debida contradicción y audiencia bilateral que no puede ser amparada (Auto del Tribunal Supremo de 25 febrero 1985 y Sentencia del Tribunal Constitucional 43/1986, de 15 abril), al contrario de la rebeldía "a la fuerza", que existe cuando no se le emplaza o no se realiza la diligencia en tiempo y forma

e) Que la resolución no sea contraria al orden público interno tanto matrimonial como procesal, con especial incidencia en el respeto a las garantías reconocidas en el art. 24 CE, debiéndose ajustar a los principios del ordenamiento jurídico español, sin que pueda confundirse con una revisión sobre el fondo ni un ajuste de las causas de nulidad canónicas a las establecidas en el CC (STS 23 Nov. 1995).

No es habitual en los Tribunales españoles la petición de convalidación de decisiones pontificias sobre matrimonios ratos no consumados, por lo que, generalmente, estas resoluciones suelen ir referidas a los Tribunales Eclesiásticos.

RESOLUCIÓN DE LA EFICACIA CIVIL DE LAS RESOLUCIONES ECLESIÁSTICAS.

La resolución acerca de la eficacia civil de las resoluciones eclesiásticas será por medio de auto, tras haber examinado el Juez "ex officio" los presupuestos, que contendrá uno de los siguientes contenidos:

a) Acordar el reconocimiento de la eficacia en el orden civil de la resolución o decisión eclesiástica (y su ejecución) si el Juez aprecia que la resolución es auténtica y ajustada al Derecho del Estado.

b) Denegar el reconocimiento si no concurren tales circunstancias. La denegación de la eficacia civil de las sentencias eclesiásticas se producirá cuando el Juez estime que no se reúnen los requisitos, aunque las partes manifiesten su conformidad, e incluso el Ministerio Fiscal.

Nada dice el nuevo texto legal sobre las consecuencias de la denegación de la eficacia civil de la sentencia eclesiástica; si bien parece que, en este caso, y lo mismo si se hubiese formulado oposición, quedará a salvo el derecho de las partes y del Fiscal, para recurrir en apelación, sin que proceda reserva de derechos a las partes o al Ministerio Fiscal para que puedan instar su derecho en el procedimiento correspondiente como se señalaba en la Disposición Adicional Segunda de la Ley 30/1981.

No parece que el Juez civil deba entrar a valorar lo resuelto en materia del propio vínculo, en decir, sobre el aspecto sustantivo de la resolución eclesiástica la nulidad o el matrimonio rato y no consumado (Sala Primera del Tribunal Supremo en sentencia de 31 de diciembre de 1982, [COMPLETAR])

No se puede omitir el hecho de que si las partes entienden que es preferible acudir al procedimiento de divorcio y no seguir con la nulidad, deberán acudir al trámite del procedimiento contencioso del artículo 770 de la Ley de Enjuiciamiento Civil, o al de común acuerdo del 777, siguiendo la vía normal en estos casos.

EFECTOS DEL RECONOCIMIENTO DE LA EFICACIA EN EL ORDEN CIVIL DE LA RESOLUCIÓN O DECISIÓN ECLESIÁSTICA.

El efecto directo que se produce por el reconocimiento de la sentencia eclesiástica es el de su inscripción en el Registro Civil, que ha de practicarse de oficio por el Tribunal.

Mayor importancia puede tener todo lo relativo a la declaración y cumplimiento de los efectos relativos a las medidas o efectos complementarios (relaciones paterno-filiales y patrimoniales) fijados inicialmente por el Juez civil o acordados por el Tribunal eclesiástico, y reconocida su validez por el Juez civil (como declaró la TC S 1/1981 son de la exclusiva competencia de los jueces y Tribunales civiles), que se ejecutarán directamente. En este caso nos encontramos con su correspondiente ejecución.

COMENTARIOS DE JURISPRUDENCIA:

‐ El trámite previsto en el derogado art. 82 CC, de ejecución a efectos civiles de las sentencias y resoluciones firmes dimanantes de la jurisdicción eclesiástica sobre nulidad o separación de matrimonio canónico, de acuerdo con lo establecido en el art. citado y en el 80 del mismo texto, constituye un procedimiento "especialísimo" y de específica naturaleza porque los organismos jurisdiccionales del Estado no se limitan a ejecutar en sentido estricto las resoluciones de la jurisdicción canónica, sino que regulan las consecuencias meramente civiles de la nulidad o de la separación, resolviendo con jurisdicción propia los diversos problemas que cada situación matrimonial plantea, para lo que han de servirse de las disposiciones del ordenamiento jurídico estatal, actuando con independencia de criterio y en proceso dotado de sustantividad respecto de la resolución anterior, lo que excluye la posibilidad de acudir al recurso singular y extraordinario a que se refiere el art. 1695 LEC.

(TS 1.ª S 31 Dic. 1982.-Ponente: Sr. De Castro García, [COMPLETAR])


### Flujo

1. **Paso 0**: comprueba Jurisprudenciator (arriba).
2. Lee entero `assets/formulario.md` (el formulario que vas a rellenar, en la carpeta de esta skill) y la parte de `../indice/marco.md` que afecte al caso. Limítate a la materia de este formulario: no añadas contenido ajeno a él.
3. Pide los datos de la lista en una sola tanda. Si un dato aparece varias veces, aclara a qué persona o acto corresponde cada vez. Lo que el usuario no sepa se queda como hueco visible con su etiqueta (p. ej. [FECHA]).
4. Resuelve cada [ELEGIR …] y cada [OPCIONAL …] según los hechos, y sustituye cualquier indicación entre paréntesis del formulario («(se describirá…)», «(indicar…)») por el contenido que corresponda. Redacta las partes que dependen del caso (hechos, motivos, descripción de bienes).
5. Aplica los avisos de actualización en el lugar que indican. Comprueba con `buscar_articulo` cada norma citada; si alguna ha cambiado, usa la redacción vigente. Si citas jurisprudencia, localízala con `buscar_sentencias` o `buscar_por_cita` y léela con `leer_sentencias`.
6. Antes de entregarlo, pasa `verificar_escrito` con las frases que citan normas o sentencias y corrige lo que señale.
7. **Documento final = el formulario tal cual, rellenado y limpio.**
   - Empieza exactamente por la primera línea de `assets/formulario.md` y sigue su estructura y su orden hasta la firma.
   - No pongas en el documento título, nombre del formulario o de la skill, código, encabezados, «Para qué sirve», leyendas, avisos, notas de uso, comentarios ni explicaciones. Tampoco marcas [ELEGIR…] u [OPCIONAL…]: ya están resueltas.
   - Formato Word (.docx, con la skill de Word disponible): **Times New Roman 11 pt** en todo el documento, **interlineado 1,15**, **texto justificado**, márgenes de 2,5 cm. Los rótulos del formulario (REUNIDOS, CLÁUSULAS, HECHOS, SUPLICO…) en su propia línea y en negrita, sin cambiar su texto.
8. En el chat (nunca dentro del documento): datos pendientes, partes redactadas por ti, normas y sentencias comprobadas con Jurisprudenciator (y, si algún dato sale de internet, cuál y su enlace) y, si es un escrito judicial o administrativo, el plazo y el órgano ante el que se presenta.

El resultado es un borrador para que lo revise un profesional antes de usarlo.
