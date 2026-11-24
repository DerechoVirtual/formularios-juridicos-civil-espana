---
name: oposicion-solicitud-declarar-gasto-extraordinario-no-civ-0051
description: "Oposición a la solicitud de declarar un gasto extraordinario no previsto en las medidas. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Oposición a la solicitud de declarar un gasto extraordinario no previsto en las medidas

> Formulario **CIV-0051** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Escrito de oposición del progenitor obligado a la solicitud, formulada por el otro progenitor, de que se declare gasto extraordinario de los hijos uno o varios gastos no previstos en las medidas definitivas o provisionales, incidente previo al despacho de ejecución regulado en el art. 776.4.ª LEC.

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Oposición a la solicitud de declarar un gasto extraordinario no previsto en las medidas» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Oposición a la solicitud de declarar un gasto extraordinario no previsto en las medidas” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:oposicion-solicitud-declarar-gasto-extraordinario-no-civ-0051`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] AÑO (2 veces)
- [ ] FIRMA (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL SOLICITANTE (2 veces)
- [ ] CLASE DE PROCEDIMIENTO
- [ ] COLEGIO
- [ ] DÍA
- [ ] LOCALIDAD
- [ ] MES
- [ ] NOMBRE Y APELLIDOS DEL ABOGADO/A
- [ ] NOMBRE Y APELLIDOS DEL OPONENTE
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] Nº DE COLEGIADO
- [ ] Nº DE PLAZA
- [ ] Nº DE PROCEDIMIENTO
- [ ] SEDE

## Normas que cita el formulario

- art. 776.4.ª LEC
- art. 440 LEC
- art. 154 Código Civil

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

AL TRIBUNAL DE INSTANCIA DE [SEDE]

[ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL (O SECCIÓN ÚNICA), según la organización del Tribunal en el partido judicial], PLAZA N.º [Nº DE PLAZA]

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, que actúa en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS DEL OPONENTE], tal y como consta acreditado en los autos de [CLASE DE PROCEDIMIENTO] n.º [Nº DE PROCEDIMIENTO]/[AÑO], asistido por el Letrado/a D./Dña. [NOMBRE Y APELLIDOS DEL ABOGADO/A], colegiado/a n.º [Nº DE COLEGIADO] del Ilustre Colegio de la Abogacía de [COLEGIO], ante el Tribunal comparezco y como mejor proceda en Derecho (véase la nota explicativa final), DIGO:

Que dentro del plazo concedido, conforme al art. 776.4.ª LEC, por medio del presente escrito y en la representación acreditada, vengo a presentar OPOSICIÓN a la declaración de gasto extraordinario solicitada por D./Dña. [NOMBRE Y APELLIDOS DEL SOLICITANTE], en base a las siguientes:

ALEGACIONES

PRIMERA.- [ADAPTAR AL CASO LOS GASTOS CONCRETOS. Redacción del modelo:] Los gastos relativos al material escolar, así como los gastos relativos al cuidado de los menores, y comedor y aula matinal, por conceptos usuales y perfectamente previsibles, es llano que carecen de las notas de eventualidad y difícil previsibilidad ínsitas en la caracterización de gastos extraordinarios (cfr., por ejemplo, SAP Jaén 149/2007, de 12 de junio, rec. 191/2007).

Así, la jurisprudencia ha venido señalando que los gastos de material escolar, en tanto se producen habitualmente al inicio de curso, no son extraordinarios, habida cuenta de su periodicidad y de su clara previsibilidad, por lo que necesariamente han de considerarse ordinarios e incluidos dentro de los alimentos que comprenden lo necesario para el sustento, habitación, vestido y educación de los menores (SAP Pontevedra 45/2010, de 29 de enero, rec. 4334/2009).

Tampoco pueden considerarse gastos extraordinarios a sufragar también por mi representado/a los gastos de comedor o aula matinal y los gastos de cuidado del menor, por cuanto tales gastos responden a necesidades del progenitor custodio que hubo de tener en cuenta a la hora de asumir a su sólo cargo la custodia del menor que, habitualmente, requiere compatibilizar las obligaciones laborales con el cuidado de los hijos.

SEGUNDA.- [ADAPTAR AL CASO. Redacción del modelo:] En cuanto a la asistencia de psicólogo, se trata de prestaciones cubiertas por la Seguridad Social, lo que hace no imprescindible, salvo circunstancias excepcionales que no se acreditan, este gasto. Las vitaminas, en fin, ni constituyen en principio gasto extraordinario, ni se ha justificado una prescripción facultativa que denote la necesidad de su adquisición.

En virtud de lo expuesto,

SUPLICO AL TRIBUNAL:

Que, teniendo por presentado este escrito y por realizadas las manifestaciones que en él se contienen, se sirva admitirlo; teniéndome por opuesto/a a la pretensión deducida de contrario, convoque a las partes a la celebración de la correspondiente vista; y, previos los trámites legales oportunos, se dicte auto por el que se declare que los gastos incluidos en la solicitud presentada por D./Dña. [NOMBRE Y APELLIDOS DEL SOLICITANTE] no tienen condición de gastos extraordinarios.

Es justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Abogado/a: [FIRMA] Firma del Procurador/a: [FIRMA]

NOTA EXPLICATIVA

Ciertamente, no existe unanimidad ni jurisprudencial ni doctrinal en la calificación como ordinarios o extraordinarios de algunos gastos de los hijos, manteniéndose posturas disímiles sobre ellos, lo cual propicia el planteamiento de infinidad de oposiciones frente al auto despachando ejecución por impago de gastos extraordinarios, al considerarlos el ejecutado ordinarios.

Y aunque a efectos prácticos sería conveniente que la sentencia dictada en el proceso de familia concretara y especificara qué conceptos tendrán la consideración de gasto extraordinario, a menudo no sucede en la práctica pues la resolución suele limitarse a considerar como gasto extraordinario los médicos no cubiertos por la Seguridad Social o los de educación, dado el carácter impredecible de estos gastos.

Ante dicha indeterminación y los problemas que su reclamación forzosa pueda provocar en ejecución, el art. 776.4.ª LEC regula una suerte de incidente declarativo de previo pronunciamiento que tiene como único objeto resolver si la cantidad reclamada como gasto extraordinario tiene dicha consideración. El incidente se sustancia conforme a las reglas del juicio verbal (art. 440 y siguientes LEC) si hay oposición, y finalizará mediante auto; tendrá lugar cuando se reclamen gastos extraordinarios no expresamente previstos en las medidas provisionales o definitivas. Para González del Pozo es posible acudir a este incidente: a) cuando en las medidas acordadas no se hubiera hecho pronunciamiento expreso relativo a gastos extraordinarios de los hijos; b) cuando se hubiera establecido de forma genérica la contribución en los gastos extraordinarios pero sin enumerar los requisitos que deben reunir aquéllos; o c) cuando se hubiera determinado en las medidas qué gastos tienen la consideración de gasto extraordinario y se reclama como tal un gasto distinto a los predeterminados.

Pues bien, siguiendo al citado autor, la falta de doctrina uniforme de las Audiencias Provinciales sobre la calificación de ordinarios o extraordinarios recae en dos grandes grupos de gastos de los hijos.

- En primer lugar, los gastos de uniforme, libros y material escolar, gastos de enseñanza y gastos de comedor y transporte escolar. En contra de su consideración como gastos extraordinarios podemos citar, entre otras resoluciones, el AAP Barcelona 214/2008, de 8 de julio, rec. 1248/2007, y la SAP Barcelona 453/2008, de 30 de junio, rec. 1066/2007.

En el mismo sentido, las SSAP Murcia 431/2006, de 7 de noviembre, rec. 298/2006 (la previsibilidad del gasto de los libros escolares, que alcanza a los de comedor, matrícula y transporte, hace que ninguno merezca la consideración de extraordinarios) y 119/2012, de 23 de febrero, rec. 51/2012.

Argumenta esta última resolución: «En relación con el primer motivo de recurso, la parte recurrente fundamenta su pretensión revocatoria en el error de la Juzgadora de instancia al conceptuar como gastos extraordinarios los relativos a matrícula del curso escolar, libros académicos, uniformes y material escolar del hijo menor de edad, por entender que los mismos quedarían integrados en el concepto de gastos ordinarios.

Sobre esta cuestión nos hemos pronunciado de forma reiterada, afirmando con carácter general que tales gastos por las partidas señaladas no revisten ese carácter extraordinario. Así, en la Sentencia de esta Audiencia Provincial de 15 de marzo de 2006, se afirma que los gastos extraordinarios "se circunscriben a aquellos que son de carácter imprevisible y que exceden de los que representa la atención habitual de las necesidades del alimentista", y más concretamente y con respecto a los gastos ahora cuestionados, identificados como gastos de educación, hemos afirmado que "a tenor de lo establecido en el artº. 154 del Código Civil, la educación es un concepto que puede incluirse sin esfuerzo interpretativo dentro del más amplio de alimentos que recoge el artº. 142, párrafo segundo, del propio cuerpo legal, no encontrándose razones suficientes para que los gastos de matrícula, libros y material escolar hayan de ser desglosados de los alimentos". Sin embargo, y no obstante el citado criterio jurídico-interpretativo, es posible también, en determinados casos, como aquí acontece, que el Juzgador, sin perjuicio de reconocer la naturaleza de esos gastos como ordinarios e incardinables por tanto en el concepto más amplio de alimentos, decida en función de su cuantía y de las disponibilidades económicas de sus padres que los mismos se distribuyan porcentualmente entre ambos progenitores. Por ello debemos aceptar la fórmula empleada al respecto por la Juzgadora de instancia, distribuyendo al 50% entre los ahora litigantes el pago de tales partidas».

En esta misma línea, SAP Madrid 548/2007, de 21 de septiembre, rec. 977/2006 (las matrículas, vestuario, calzado, material escolar, actividades extraescolares, inglés y natación se excluyen del concepto de gastos extraordinarios); SAP Salamanca 304/2009, de 15 de julio, rec. 127/2009 (los gastos de educación de los estudios de ingeniería no cubiertos por el sistema público, como matrículas, libros y material, son ordinarios por previsibles); y SAP Lugo 525/2009, de 3 de julio, rec. 213/2009.

Otras resoluciones, en cambio, consideran extraordinarios algunos de estos gastos, por tener su causa última en la enseñanza. Así, la SAP Madrid 423/2008, de 16 de junio, rec. 294/2007, considera gastos extraordinarios los libros de texto y material escolar, a excepción de las partes cubiertas por ayudas oficiales, o la SAP Navarra 82/2008, de 5 de marzo, rec. 151/2007, que considera extraordinarios los gastos de libros, campamentos y excursiones escolares por estar todos ellos excluidos del coste de la matrícula, ya que, pese a ser previsibles, su monto puede ser tan considerable que no admita ser asumido sin un cierto quebranto.

- El segundo grupo de gastos sobre los que no existe coincidencia entre las Audiencias en su consideración como gastos ordinarios o extraordinarios son los relativos a las actividades extraescolares del menor.

Entre las resoluciones que no los consideran gastos extraordinarios tenemos:

El AAP Barcelona 214/2008, de 8 de julio, rec. 1248/2007, citando la sentencia de la misma Sección 81/2006, de 14 de febrero, rec. 653/2005, no considera gastos extraordinarios los correspondientes a actividades extraescolares del menor, al carecer de las notas referidas a la naturaleza de tales gastos. Específicamente, la SAP Barcelona 33/2008, de 16 de enero, rec. 587/2007, considera gastos ordinarios los «gastos extraescolares y las colonias de verano». Y las SSAP Barcelona 373/2008, de 29 de mayo, rec. 804/2007, y 351/2008, de 23 de mayo, rec. 906/2007, excluyen las actividades extraescolares del concepto de gastos extraordinarios por venir realizándolas los hijos de forma asidua y derivar de actividades cotidianas o periódicas de los hijos.

A favor de considerar gastos extraordinarios las actividades extraescolares se pronuncian la SAP Madrid 423/2008, de 16 de junio, rec. 294/2007, que considera gasto extraordinario la actividad extraescolar de multideporte, a excepción de la parte cubierta por ayudas oficiales; y la SAP La Rioja 25/2009, de 26 de enero, rec. 360/2008, que considera extraordinarios los referidos a inicio de curso, como libros y matrículas, minorados en el importe de las ayudas públicas recibidas por tales conceptos, «pues aunque se trate de un gasto previsible en cuanto a su periodicidad, su cuantía no puede fijarse con anterioridad a su devengo...».

Anotamos también la SAP Murcia 212/2005, de 6 de julio, rec. 77/2005:

«Los únicos gastos que por estudios se vienen considerando extraordinarios son los universitarios y las actividades extraescolares. Ya lo dijimos en nuestra sentencia 168/02, de 18 de abril, rec. 167/2002. Al respecto hemos insistido en la conveniencia de delimitar la cobertura ordinaria de la pensión alimenticia de aquellos otros gastos, comúnmente denominados como extraordinarios, que quedan fuera, que constituyen un plus y que han de ser abonados diferenciadamente. La primera de las contribuciones cubre exclusivamente las necesidades básicas, ordinarias y normales de los hijos señaladas en el artículo 142 en relación con el artículo 154, siempre del Código Civil, esto es, todo aquello que se precisa para el sustento, habitación, vestido, asistencia médica, educación e instrucción y, en definitiva, formación integral del alimentista, todo ello entendido conforme al status familiar. Por ello, no precisan del consenso previo de los progenitores ni autorización judicial para su devengo, sino que el acreedor a cuyo cargo se encuentran los beneficiarios puede disponer de la pensión discrecionalmente en ejercicio de la administración doméstica.

Por el contrario, los extraordinarios integran también la obligación alimenticia pero nacen de necesidades de los hijos de naturaleza excepcional, eventuales, difícilmente previsibles y de un montante económico considerable que, por ello, no pueden incluirse en la pensión ordinaria a la vez que no pueden ser costeadas por uno solo de los progenitores sin desequilibrar en su perjuicio la equivalencia de sus respectivas contribuciones (personal y económica). Ello no significa que hayan de ser siempre imprescindibles y necesarias (silla de ruedas, elementos ortopédicos, asistencia por terceras personas en caso de enfermedad, etc.), cabe también que puedan ser accesorias (por ejemplo, operaciones quirúrgicas cubiertas por la Seguridad Social que, sin embargo, se practican en centros privados) o, simplemente, complementarias (viajes de estudios, clases particulares, etc.).

Consecuente con lo anterior, la regla general es que los gastos extraordinarios deben ser consentidos previamente a su devengo por ambos progenitores a fin de que cada uno de ellos pueda opinar sobre su conveniencia o su cuantía y, a falta de acuerdo, que sean autorizados judicialmente. Sólo si se cumplen estas condiciones es factible que uno pueda exigir del otro su respectiva contribución. Con ello se evita tanto que el cumplimiento de las obligaciones quede al arbitrio de una de las partes, lo que vulneraría el artículo 1256, como que, de hecho, se impida al cotitular del ejercicio de la patria potestad participar en decisiones importantes sobre la formación, salud, ocio y, en definitiva, todas aquellas fundamentales para el desarrollo de la personalidad de sus hijos. Excepcionalmente, en evitación de que se causen perjuicios irreparables a aquéllos, lo que contraviene el artículo 158 y, en general, el principio del favor filii y las normas sobre protección de menores, los gastos inaplazables y, por ende, que no toleran demora sin grave riesgo o daño para éstos, pueden ser autorizados judicialmente "a posteriori" si concurriese discordia entre los obligados.

De acuerdo con lo expuesto, los gastos de educación, incluidos el material escolar, matrícula y equipamiento, en cuanto previsibles y habituales, no pueden considerarse extraordinarios. El hecho de que no sea un gasto constante (se abonan una vez al año) no merma ese carácter, lo esencial es que es una prestación usual, común y necesaria, bastando para afrontar su pago con que la acreedora de la pensión ajuste su economía y el presupuesto doméstico a tales devengos, previsibles y ciertos. Precisamente porque no participan de ese carácter, no pueden considerarse ordinarios el coste de las actividades extraescolares porque ab initio se desconoce su necesidad o conveniencia, su importe, su duración, el modo en que se van a recibir, si comporta o no desplazamientos, etcétera, amén de que se recae sobre una materia en la que debe participar el deudor, no sólo pagando, sino también en la toma de la decisión».

Se mantiene también como tercera vía la solución consistente en entender que las actividades extraescolares no constituyen gastos extraordinarios, pero que deben abonarse por mitad por ambos progenitores, siempre que exista previa consulta y conformidad de ambos en la conveniencia o necesidad de que el menor las realice, sufragándose, en caso de desacuerdo, por el progenitor que las promueva. Esta es la solución dada por la SAP Barcelona 311/2008, de 7 de mayo, rec. 83/2007; la SAP Barcelona, Sección 12.ª, 710/2007, de 21 de noviembre, rec. 533/2007, considera, en igual sentido, que procede excluir de la relación de gastos extraordinarios los relativos a las actividades extraescolares tales como excursiones, campamentos, natación, música, judo, inglés o similares, que «deberán ser atendidos en un cincuenta por ciento por ambos padres, siempre que presten su consentimiento en la realización de tales actividades extraescolares, resolviendo el órgano judicial, en caso de discrepancia sobre la necesidad o conveniencia de llevarlas a cabo, y sobre la determinación cuantitativa de las mismas».

En cuanto a la cuota de asociación de padres de alumnos, la SAP Valencia 110/2005, de 17 de febrero, rec. 970/2004, entiende que está comprendida en la pensión ordinaria de alimentos, formando parte de la atención a la educación de los menores.

En el mismo sentido, el AAP Murcia 5/2008, de 29 de enero, rec. 526/2007:

«...se ha de coincidir con el recurrente en que los gastos escolares reclamados como extraordinarios de educación (matrículas, uniforme, libros, material escolar, seguro escolar y APA) no revisten ese carácter. Indica la sentencia de esta Sección, SAP Murcia 115/2006, de 15 de marzo, rec. 491/2005, citada en el recurso, que los gastos extraordinarios "se circunscriben a aquellos que son de carácter imprevisible y que exceden de los que representa la atención habitual de las necesidades del alimentista"; y, más concretamente, en cuanto a los gastos de educación (en el caso contemplado en esa resolución referidos al coste del material escolar), que "a tenor de lo establecido en el artículo 154 del Código Civil, la educación es un concepto que puede incluirse sin esfuerzo interpretativo dentro del más amplio de alimentos que recoge el artículo 142, párrafo segundo, del propio Cuerpo legal, no encontrándose razones suficientes para que los gastos de matrícula, libros y material escolar hayan de ser desglosados de los alimentos". En definitiva, los gastos escolares que nos ocupan, como lo indispensable para la formación del hijo, no pueden tener otra consideración que la de gastos ordinarios, incluibles dentro del concepto de alimentos».
