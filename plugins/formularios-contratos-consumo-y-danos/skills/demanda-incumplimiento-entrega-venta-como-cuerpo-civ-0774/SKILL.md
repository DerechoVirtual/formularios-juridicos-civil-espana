---
name: demanda-incumplimiento-entrega-venta-como-cuerpo-civ-0774
description: "Demanda por incumplimiento de la entrega en una venta como cuerpo cierto con defecto de cabida. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda por incumplimiento de la entrega en una venta como cuerpo cierto con defecto de cabida

> Formulario **CIV-0774** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio ordinario del comprador de una finca vendida como cuerpo cierto y a precio alzado, que reclama una rebaja proporcional del precio por no poder entregarle el vendedor todo lo comprendido dentro de los linderos (aquí, por existir un enclave ajeno, como un camino público). Se usa al amparo del art. 1.471, párrafo segundo, del Código Civil, dentro del plazo de seis meses desde la entrega.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda por incumplimiento de la entrega en una venta como cuerpo cierto con defecto de cabida» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda por incumplimiento de la entrega en una venta como cuerpo cierto con defecto de cabida” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:demanda-incumplimiento-entrega-venta-como-cuerpo-civ-0774`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (6 veces)
- [ ] IMPORTE (5 veces)
- [ ] Nº DE DOCUMENTO (5 veces)
- [ ] NOMBRE Y APELLIDOS DEL DEMANDADO (4 veces)
- [ ] AÑO (2 veces)
- [ ] CORREO ELECTRÓNICO (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] DÍA (2 veces)
- [ ] FECHA (2 veces)
- [ ] MES (2 veces)
- [ ] Nº DE DOCUMENTOS (2 veces)
- [ ] SEDE (2 veces)
- [ ] SUPERFICIE (2 veces)
- [ ] TELÉFONO (2 veces)
- [ ] ANCHURA
- [ ] DESCRIPCIÓN Y SITUACIÓN DE LA FINCA
- [ ] DOMICILIO LABORAL
- [ ] DOMICILIO PROFESIONAL
- [ ] FOLIO
- [ ] LIBRO
- [ ] LINDERO
- [ ] LINDERO ESTE
- [ ] LINDERO NORTE
- [ ] LINDERO OESTE
- [ ] LINDERO SUR
- [ ] NOMBRE DEL NOTARIO
- [ ] NOMBRE Y APELLIDOS DEL ABOGADO/A
- [ ] NOMBRE Y APELLIDOS DEL DEMANDANTE
- [ ] NOMBRE Y APELLIDOS DEL PERITO
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] Nº DE COLEGIADO
- [ ] PORCENTAJE
- [ ] SITUACIÓN DE LA FINCA
- [ ] TOMO

## Normas que cita el formulario

- art. 24.1 LEC
- art. 399.1 LEC
- art. 21 LOPJ
- art. 36 LEC
- art. 22.3.º LOPJ
- art. 9.2 LOPJ
- art. 85.1 LOPJ
- art. 45 LEC
- art. 68 LEC
- art. 50.1 LEC
- art. 6.1.1.º LEC
- art. 7.1 LEC
- art. 10 LEC
- art. 399 LEC
- art. 403.3 LEC
- art. 1.472 CC
- art. 1.471 CC
- art. 253.1 LEC
- art. 251.1.ª LEC
- art. 5 Ley Orgánica 1/2025
- art. 1469 Código Civil
- art. 1471 CC
- art. 394.1 LEC
- art. 24.2 LEC
- art. 155.3 LEC

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales y de D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDANTE], con domicilio en [DOMICILIO], representación que acredito mediante escritura de poder otorgada a mi favor (existen tres posibilidades para otorgar el apoderamiento al Procurador de los Tribunales, conforme dispone el art. 24.1 LEC) (1)

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]
— Si el poder se otorga a través de la sede judicial electrónica: mediante comparecencia electrónica, a través de la sede judicial electrónica e inscrito en el Registro Electrónico de Apoderamientos Judiciales; y a cuya justificación acompaño certificación de dicho Registro aportada como Documento nº [Nº DE DOCUMENTO], y que se puede acreditar mediante consulta automatizada orientada al dato por parte del órgano judicial al cual tengo el honor de dirigirme.
— Si el poder se otorga mediante comparecencia apud acta: mediante comparecencia personal apud acta ante el Tribunal Decano de [LOCALIDAD], posteriormente inscrito en el Registro Electrónico de Apoderamientos Judiciales; y a cuya justificación acompaño certificación de dicho Registro aportada como Documento nº [Nº DE DOCUMENTO], y que se puede acreditar mediante consulta automatizada orientada al dato por parte del órgano judicial al cual tengo el honor de dirigirme.
— Si el poder se otorga ante Notario: mediante escritura de poder otorgada a mi favor ante el Notario/Notaria [NOMBRE DEL NOTARIO], con Notaría sita en [LOCALIDAD]. El poder se inscribió en el Registro Electrónico de Apoderamientos Judiciales, lo cual justifico mediante certificación de dicho Registro aportada como Documento nº [Nº DE DOCUMENTO], y que se puede acreditar mediante consulta automatizada orientada al dato por parte del órgano judicial al cual tengo el honor de dirigirme.

bajo la dirección letrada de D./Dña. [NOMBRE Y APELLIDOS DEL ABOGADO/A], abogado/a en ejercicio, con despacho profesional abierto en [DOMICILIO PROFESIONAL], colegiado nº [Nº DE COLEGIADO] del Ilustre Colegio de la Abogacía de [LOCALIDAD], ante el Tribunal comparezco y como mejor en Derecho proceda, DIGO:

Que mediante el presente escrito vengo a formular DEMANDA DE JUICIO ORDINARIO, contra D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDADO], con domicilio (2) primero en [DOMICILIO]

[OPCIONAL — incluir si procede]
y, segundo, el domicilio laboral en [DOMICILIO LABORAL];

con (3) email [CORREO ELECTRÓNICO] y con número de teléfono móvil [TELÉFONO]; en ejercicio de la acción de incumplimiento de la obligación de entrega derivada de defectos de cabida en la venta de finca como cuerpo cierto, que se concretará en el cuerpo del escrito y en el suplico, y todo ello de conformidad con los siguientes hechos y fundamentos de derecho.

Que esta parte asume el compromiso de recibir cualquier comunicación dirigida por la oficina judicial, durante toda la fase declarativa e, incluso, en una eventual fase de ejecución, por medios telemáticos, en términos del art. 399.1 II LEC, consignándose a estos efectos la siguiente dirección de correo electrónico y nº de teléfono: [CORREO ELECTRÓNICO] y [TELÉFONO].

HECHOS

PRIMERO.- Con fecha [DÍA] de [MES] de [AÑO], mi mandante en calidad de comprador y el demandado como vendedor contrataron la compraventa de la finca sita en [DESCRIPCIÓN Y SITUACIÓN DE LA FINCA]. En el contrato de compraventa consta su descripción, tanto literaria como gráfica, con referencia a un plano, que identifica la finca como de una cabida de [SUPERFICIE] metros cuadrados que linda: Norte con [LINDERO NORTE]; Oeste con [LINDERO OESTE]; Este con [LINDERO ESTE] y parte con [LINDERO]; Sur, en parte con el anterior y con [LINDERO SUR]. Dicho contrato privado se elevó a escritura pública, practicándose la oportuna inscripción en el Registro de la Propiedad de [LOCALIDAD], al tomo [TOMO], folio [FOLIO], del libro [LIBRO], con fecha [FECHA]. Se acompaña copia simple de la escritura de compraventa y del plano, y nota simple registral acreditativa de la superficie de la finca y sus linderos, como documentos números [Nº DE DOCUMENTOS].

SEGUNDO.- El precio pactado para la compraventa fue de [IMPORTE] euros, el cual fue satisfecho íntegramente en el momento de otorgamiento de la escritura, tal y como resulta de la copia simple de la escritura que se acompaña con la demanda.

TERCERO.- Posteriormente, mi representado pudo constatar que la porción de terreno que discurre paralela y adyacente al lindero oeste de la finca, en toda su banda longitudinal, en una zona de una anchura de [ANCHURA] metros, corresponde a camino público incorporado en el nuevo planeamiento general de ordenación urbana, como se comprueba por certificado emitido por el Ayuntamiento de [LOCALIDAD] que se acompaña como documento número [Nº DE DOCUMENTO], cuya existencia se había silenciado en la escritura.

Como la finca fue adquirida a precio alzado y como cuerpo cierto, se vende todo lo que hay dentro de los lindes y todo esto es lo que ha pagado el comprador, y si después resulta que no puede entregarlo todo, porque una parte no es suya, la venta a cuerpo cierto queda desnaturalizada, ya que no se vende lo convenido, debiendo el comprador ser indemnizado.

CUARTO.- Habida cuenta de que mi representado había satisfecho en su integridad el precio fijado para la venta en el momento de formalización de la escritura pública, si la finca resulta finalmente con una dimensión inferior es por lo que, al no poderse cumplir con lo estipulado para la misma, solicita que el precio se modifique proporcionalmente a juicio de peritos, lo que da lugar a una rebaja o disminución del [PORCENTAJE] % del precio abonado por su compra.

Se acompaña como documento número [Nº DE DOCUMENTO] dictamen pericial elaborado por el/la perito D./Dña. [NOMBRE Y APELLIDOS DEL PERITO], del que resulta que el precio de dichos [SUPERFICIE] metros cuadrados es de [IMPORTE] euros, que se reclaman en la presente demanda.

QUINTO.- A pesar de las gestiones amistosas realizadas extrajudicialmente por mi mandante para resolver el problema derivado del incumplimiento de sus obligaciones por el vendedor, ello no ha sido posible, y es preciso impetrar el auxilio judicial, lo que efectivamente se hace por medio del presente escrito.

Se acreditan estos extremos con los documentos números [Nº DE DOCUMENTOS], acreditativos del requerimiento efectuado por burofax a D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDADO] y de la entrega de dicho requerimiento en su domicilio con fecha [FECHA].

A los anteriores hechos son de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN Y COMPETENCIA.

Con arreglo a los preceptos que se contienen en el art. 117 de la Constitución, art. 21 LOPJ y art. 36 LEC, la jurisdicción ordinaria del Reino de España es la única competente para conocer de los negocios o demandas civiles que se susciten en territorio español entre españoles, además de que los órganos jurisdiccionales son los competentes, con carácter exclusivo, en materia de obligaciones contractuales, cuando estas hayan nacido o deban cumplirse en España (art. 22.3.º LOPJ).

El conocimiento del litigio pertenece a la materia del orden jurisdiccional civil (art. 9.2 LOPJ), y le corresponde la competencia específica objetiva a los Tribunales de Instancia, concretamente a la Sección Civil, en cuanto por disposición legal expresa no viene atribuido a otros Jueces o Tribunales (art. 85.1 LOPJ y art. 45 LEC).

Corresponde el conocimiento del juicio a la Sección Civil del Tribunal de Instancia que por reparto corresponda (art. 68 LEC) de los de [SEDE], al que me dirijo en aplicación del art. 50.1 LEC, por ser el del domicilio del demandado.

II.- CAPACIDAD.

Conforme al art. 6.1.1.º LEC tienen capacidad para ser parte las personas físicas, y a tenor del art. 7.1 LEC detentan capacidad de obrar procesal, en tanto que mayores de edad y en pleno ejercicio de sus derechos civiles, las implicadas en el proceso.

III.- LEGITIMACIÓN.

El art. 10 LEC legitima para comparecer y actuar en juicio a los titulares de la relación jurídica o del objeto litigioso. En el caso de autos, demandante y demandado son los sujetos titulares del contrato cuyo incumplimiento fundamenta la acción que se ejerce, existiendo, pues, legitimación directa ordinaria. La legitimación activa de mi representado resulta indiscutible en su calidad de comprador de una finca con una cabida inferior a la expresada en el contrato, y corresponde la pasiva al demandado como parte vendedora de dicho contrato.

IV.- PROCEDIMIENTO.

El interés económico de la demanda supera la suma de 15.000 euros, por lo que, al no tener la presente contienda una tramitación especial «ratione materiae», será de aplicación lo dispuesto en los arts. 248.3, 249.2 y 254.1 LEC, debiendo ventilarse por el juicio ordinario, regulado en el Título II del Libro II LEC (arts. 399 y ss. LEC), debiendo asimismo secundarse las Disposiciones Comunes a los Procesos Declarativos previstas en el Título I de dicho Libro (arts. 248 y ss. LEC).

V.- POSTULACIÓN Y DEFENSA.

Se cumplen las normas de postulación procesal, ya que la demanda se presenta por medio de Procurador/a legalmente habilitado para actuar ante los tribunales de este partido, y bajo la dirección de Letrado en ejercicio que redacta y firma, conforme a lo dispuesto en los arts. 23.1 y 31.1 LEC.

VI.- REQUISITOS FORMALES.

Se inicia el proceso por medio de demanda que reúne todos los requisitos exigidos en el art. 399 LEC, sin que existan otras exigencias especiales de procedibilidad, y no estando prevista legalmente una acreditación preliminar de la legitimación o principio de prueba del derecho, por lo que, competente el tribunal, deberá aquella admitirse, a tenor de los arts. 403.3 y 404 LEC.

VII.- PRESCRIPCIÓN.

Según lo establecido en el art. 1.472 CCiv, las acciones ejercitables conforme al art. 1.471 CCiv prescribirán a los seis meses, contados desde el día de la entrega, por lo que, al no haber transcurrido dicho plazo, la presente demanda se presenta dentro del establecido en dicho precepto.

VIII.- CUANTÍA.

Cumpliendo la exigencia del art. 253.1 LEC, se cifra la cuantía de la demanda en la cantidad de [IMPORTE] euros, que integra la cantidad líquida reclamada conforme al art. 251.1.ª LEC.

IX.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4.º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

X.- FUNDAMENTO MATERIAL DE LA TUTELA.

Se ejercita acción de incumplimiento de la obligación de entrega con fundamento en el párrafo 2.º del art. 1.471 CCiv.

Como señala la STS de 21 de julio de 2000, rec. n.º 2801/1995, «cuando es vendido un inmueble, para la determinación del mismo, no es necesario que sean precisadas en el contrato las dimensiones, la medida, pudiendo tener esta indicación dos significaciones, dos valores bien distintos: primero, que las partes hayan querido obtener aquella determinada medida por aquel determinado precio, estableciendo que en tanto se convenía aquel precio en cuanto el inmueble tenía tal medida, siendo obvio que si después resulta que el inmueble tenía dimensiones distintas, también el importe del precio debe modificarse proporcionalmente, en más o en menos, hipótesis de la venta de inmuebles por unidad de medida o número prevista y disciplinada por los arts. 1469 y 1470 del Código Civil; y segundo, que el inmueble sea vendido como cuerpo cierto, es decir, por lo que es, independientemente de sus dimensiones efectivas, hipótesis regulada por el art. 1471 del propio cuerpo legal», y la sentencia de 25 de febrero de 1997 afirma que «esta Sala tiene declarado, entre otras, en sentencias de 28 de noviembre de 1962 y 4 de febrero de 1979, que para la determinación del objeto vendido no es preciso determinar sus dimensiones, y aunque así se haga, siempre que falte la indicación del precio concreto por unidad de medida, la ley supone que tal individualización no ha tenido para las partes valor esencial, y constituía tan solo una superabundancia de datos, que es una presunción de valor absoluto».

Si como se ha dicho «la venta a cuerpo cierto requiere que el precio no se haya pactado por unidad de medida, y estipulándose un precio sin referencia a este dato, sino de forma alzada, ninguna trascendencia tiene para su calificación como tal venta el que se haga mención de la extensión del objeto comprado», habrá que concluir que en el caso objeto de esta litis se está ante una compraventa de cuerpo cierto y no a un tanto por medida de superficie.

En este sentido, el Tribunal Supremo, en su sentencia de 14 de febrero de 2002, rec. n.º 2724/1996, señala que «versando la compraventa sobre cosa cierta y determinada (“cuerpo cierto”), perfectamente individualizada y delimitada por datos físicos, no resulta relevante la superficie que puedan tener las fincas de que se trata (art. 1471, p. primero CC y Sentencias, entre otras, de 12 Dic. 1991, 25 Feb. 1997, 25 Jul. 1998, 18 Jun. 1999, 21 Jul. 2000 y 31 Ene. 2001)»; el fundamento de la acción que se ejercita no es la falta de entrega de la cabida pactada, sino la falta de entrega de todo lo comprendido dentro de los linderos, por existir dentro del terreno comprendido en los mismos un enclave ajeno.

El art. 1.471 CCiv establece que en la venta de un inmueble, hecha por precio alzado y no a razón de un tanto por unidad de medida o número, no tendrá lugar el aumento o disminución del precio, aunque resulte mayor o menor cabida o número de los expresados en el contrato, lo que tendrá lugar igualmente cuando sean dos o más las fincas vendidas por un solo precio; añadiendo el segundo inciso del referido precepto legal que, si, además de expresarse los linderos, indispensables en toda enajenación de inmuebles, se designaren en el contrato su cabida o número, el vendedor estará obligado a entregar todo lo que se comprenda dentro de los mismos linderos, aun cuando exceda de la cabida o número expresados en el contrato, y, si no pudiera, sufrirá una disminución en el precio, proporcional a lo que falta de cabida o número, a no ser que el contrato quede anulado por no conformarse el comprador con que se deje de entregar lo que se estipuló. Esta regla, como indica la doctrina científica, inicialmente se presenta con incorrecta redacción gramatical, como una especie de galimatías jurídico, tachada de oscuridad al contradecir en apariencia lo dispuesto en el inciso primero del art. 1471 CCiv, suscitando serias dudas sobre su ámbito de aplicación, habida cuenta de que algún sector de la doctrina científica consideró que su alcance era exclusivamente el de los casos de venta conjunta de varias fincas por un solo precio, pero que, no obstante, mayoritariamente se entiende que debe aplicarse tanto a los supuestos de venta de un solo inmueble por precio alzado como a la venta conjunta de dos o más fincas por un solo precio, habida cuenta de que lo esencial, como se viene diciendo, no es otra cosa que el vendedor haga entrega de «todo» lo que se comprende dentro de los mismos linderos, aun cuando exceda de la cabida o número expresados en el contrato, lo que correlativamente supone que el comprador tenga acción para exigir la entrega de lo acordado. Y así, mientras el vendedor puede entregar, y por ello entregue, todo el terreno comprendido dentro de los linderos asignados a la finca, no cabe reclamación alguna, ni por su parte, aunque resulte una cabida mucho mayor que la expresada, ni por parte del comprador, aunque esa cabida sea en realidad mucho menor; pero si se vende todo lo que hay dentro de los lindes y todo esto es lo que ha pagado o debe pagar el comprador, sea mucho o sea poco, si después resulta que no puede entregarlo todo, la venta a cuerpo cierto queda desnaturalizada, ya que no se vende lo convenido, lo que da paso a la entrada en juego de la regla comprendida en el segundo inciso del comentado art. 1471 CCiv, todo ello en base a la existencia de un error sustancial (art. 1266, párrafo 1.º CCiv).

Corolario de lo anterior, de acuerdo con lo establecido en el art. 1.471, inciso segundo, CCiv, que prevé la venta de cuerpo cierto con designación añadida de cabida o número, aplicable al supuesto enjuiciado, mi representado se halla legitimado, como parte compradora, para optar por instar la resolución del contrato o exigir una disminución proporcional del precio a juicio de peritos por dejarse de entregar lo que se estipuló. Mi representado opta por esta segunda opción, por lo que, según lo expuesto en el ordinal cuarto de los hechos de la demanda, tendrá derecho a exigir [IMPORTE] euros.

XI.- COSTAS.

Las costas del presente proceso deberán ser impuestas a la parte demandada, en la medida en que deben resultar estimadas la totalidad de nuestras pretensiones, conforme al principio del vencimiento que destaca el art. 394.1 LEC, en lo que respecta a los juicios declarativos en su primera instancia.

En atención a todo lo expuesto,

SUPLICO AL TRIBUNAL

Que, teniendo por presentado este escrito de demanda junto con los documentos que se acompañan y copias simples de todo ello, se sirva admitir uno y otros, se me tenga por comparecido y parte, en la representación que ostento y con carácter de demandante, entendiéndose conmigo las ulteriores sucesivas diligencias, y por promovido juicio ordinario contra D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDADO], se le confiera traslado emplazándole en legal forma de comparecencia y eventual contestación y, seguido que sea el oportuno procedimiento, en su día se dicte sentencia por la que se CONDENE a D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDADO] al pago al actor de la cantidad de [IMPORTE] euros, como consecuencia del incumplimiento contractual y en concepto de rebaja del precio pagado por la finca sita en [SITUACIÓN DE LA FINCA], vendida por el demandado al actor, más los intereses legales desde la fecha de la reclamación judicial.

Todo ello con expresa condena en costas del presente procedimiento.

Es justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Abogado/a | Firma del Procurador/a

NOTAS DE AYUDA

(1) A la hora de su acreditación, todos los poderes deben estar inscritos en el Registro Electrónico de Apoderamientos Judiciales (REAJ). Se supone que, para su acreditación, basta con la consulta automatizada (de dicho Registro) orientada al dato, que está a disposición de cualquier Letrado de la Administración de Justicia. Sin embargo, dado que el art. 24.2 LEC configura la certificación de dicha inscripción como vía subsidiaria de acreditación, para el caso de que el sistema no permita aquella consulta automatizada, se señala en el modelo que se acompaña certificación electrónica. El sistema permite emitir dicha certificación a quien inscribe el poder.

(2) El art. 155.3 LEC permite expresar varios domicilios del demandado (el que aparezca en el padrón municipal o conste oficialmente a estos efectos; el que aparezca en Registro oficial o en publicaciones de colegios profesionales, si se trata de empresas o personas colegiadas; donde desarrolle su actividad profesional o laboral no ocasional; si es empresa mercantil, el domicilio de cualquiera de sus administradores, gerentes o apoderados; o, si es asociación que consta en registro oficial, el domicilio del presidente, miembro o gestor de la Junta correspondiente). Cuando se señalen varios, se indicará el orden a seguir para la notificación, con vistas al éxito de la misma.

(3) El art. 155.3 LEC configura una obligación adicional del demandante, consistente en aportar cuantos datos sean de utilidad para localizar al demandado: número de identificación fiscal o de extranjeros, número de teléfono o de fax, dirección de correo electrónico o similares.
