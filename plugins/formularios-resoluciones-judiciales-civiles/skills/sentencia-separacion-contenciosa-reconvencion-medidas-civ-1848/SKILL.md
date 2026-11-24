---
name: sentencia-separacion-contenciosa-reconvencion-medidas-civ-1848
description: "Sentencia de separación contenciosa con reconvención, medidas previas de otro tribunal y Fiscal. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Sentencia de separación contenciosa con reconvención, medidas previas de otro tribunal y Fiscal

> Formulario **CIV-1848** del plugin **Resoluciones judiciales civiles: autos, decretos y diligencias** (`formularios-resoluciones-judiciales-civiles`) · Civil › Resoluciones judiciales (autos, decretos, providencias, diligencias) · normativa revisada el 24-11-2026.

## Qué es

Sentencia dictada en proceso de separación matrimonial contenciosa, el cual estuvo precedido por otro proceso de medidas provisionales previas seguido en otro Tribunal, existiendo demanda y reconvención y siendo parte el Ministerio Fiscal en tutela del hijo menor de edad.

Es un modelo de tipo **resoluciones judiciales (autos, decretos, providencias, diligencias)**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Sentencia de separación contenciosa con reconvención, medidas previas de otro tribunal y Fiscal» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Sentencia de separación contenciosa con reconvención, medidas previas de otro tribunal y Fiscal” para mi caso». También puedes invocarla directamente con `/formularios-resoluciones-judiciales-civiles:sentencia-separacion-contenciosa-reconvencion-medidas-civ-1848`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-resoluciones-judiciales-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Resoluciones judiciales civiles: autos, decretos y diligencias) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (20 veces)
- [ ] FECHA (13 veces)
- [ ] NOMBRE DEL MENOR (9 veces)
- [ ] IMPORTE (8 veces)
- [ ] LOCALIDAD (8 veces)
- [ ] Nº (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] SEDE (2 veces)
- [ ] ÓRGANO ADMINISTRATIVO (2 veces)
- [ ] AÑO
- [ ] BARRIO
- [ ] DESCRIPCIÓN DEL EPISODIO
- [ ] DIRECCIÓN
- [ ] DOMICILIO
- [ ] GRUPO
- [ ] LUGAR
- [ ] MES
- [ ] OTROS DATOS

## Normas que cita el formulario

- art. 86 CC
- art. 1.392.4.º CC
- art. 810 LEC
- art. 92.3 CC
- art. 170 CC
- art. 94 CC
- art. 91 CC
- art. 93 CC
- art. 147 CC
- art. 144 CC
- art. 149 CC
- art. 154 CC
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

- Junto a «…ado-Juez de la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

SENTENCIA

En [LUGAR], a [FECHA].

Vistos los presentes autos de Separación Matrimonial n.º [NÚMERO]/[AÑO], por el Magistrado-Juez de la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº] , D./Dña. [NOMBRE Y APELLIDOS], a instancias de D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, en nombre y representación de D. [NOMBRE Y APELLIDOS], asistido del Letrado D./Dña. [NOMBRE Y APELLIDOS], contra Dña. [NOMBRE Y APELLIDOS], representada por el/la Procurador/a de los Tribunales D./Dña. [NOMBRE Y APELLIDOS], y asistido de/la Letrado/a D./Dña. [NOMBRE Y APELLIDOS], habiendo sido parte el Ministerio Fiscal; ha pronunciado sentencia en base a los siguientes

ANTECEDENTES DE HECHO

PRIMERO.- El/La Procurador/a Sr./a. [NOMBRE Y APELLIDOS], en nombre y representación de D. [NOMBRE Y APELLIDOS], interpuso el [FECHA], demanda de separación matrimonial contra su esposa, invocando los fundamentos de derecho que estimaba pertinentes y terminando con la súplica de que se declarara la separación del matrimonio, interesando expresamente el mantenimiento de las medidas provisionales como definitivas

SEGUNDO.- Por decreto/auto de [FECHA], se admitió a trámite la demanda, emplazándose a Dña. [NOMBRE Y APELLIDOS], y dando traslado al Ministerio Fiscal para personación y contestación a la demanda, compareciendo la demandada quien después de alegar los fundamentos de derecho que estimaba aplicables, terminaba suplicando se dictara sentencia declarando no haber lugar a la separación matrimonial y aportando razonamientos jurídicos, dedujo reconvención, suplicando se declarara la disolución del matrimonio por divorcio y las medidas de

Igualmente, el Ministerio Fiscal contestó pidiendo resolución atenida a las prevenciones legales en que subsumir los hechos que se prueben, y las medidas en interés del hijo menor.

TERCERO.- Mediante decreto de fecha [FECHA], se admitió la reconvención y se confirió traslado al demandante para su contestación en plazo de diez días, lo que verificó en tiempo y forma, lo que se corroboró en diligencia de ordenación de [FECHA] siguiente, en que se convocaba a la vista del proceso.

CUARTO.- En la vista, que se celebró el [FECHA], las partes alegaron en apoyo de sus escritos expositivos por su orden, como hizo el Ministerio Fiscal, proponiendo la prueba que les fue de interés, y se practicaron en el acto las que fueron declaradas pertinentes, interrogatorio de los litigantes, diversa documental, mediante petición de tener por reproducido lo instrumentado en la pieza separada de medidas provisionales, y testifical, con el resultado que aparece en acta y reproducido en soporte audiovisual.

QUINTO.- Mediante providencia de [FECHA],se acordaron diligencias de prueba que restaban por practicar, por plazo de treinta días desde la vista, de despacho de diversos oficios para certificación, y [OTROS DATOS], lo que cumplimentó con fecha [FECHA], quedando el juicio concluso para sentencia, habiéndose observado todas las formalidades que prescribe la Ley.

FUNDAMENTOS DE DERECHO

PRIMERO.- Está probado por la conformidad entre partes y aparece documentado en las actuaciones que D. y Dña. contrajeron matrimonio civil con fecha [FECHA] en [LOCALIDAD], habiéndose separado de hecho con anterioridad; que de dicho matrimonio ha nacido un hijo al que se ha puesto por nombre [NOMBRE DEL MENOR] el [FECHA]; que el último domicilio familiar se situaba en [DIRECCIÓN], barrio [BARRIO], casa [Nº], disfrutándolo el matrimonio a título de propiedad común, residiendo en el mismo la demandada reconviniente y el demandante reconvenido en [DOMICILIO]; y que la convivencia conyugal es inexistente desde contrato de [FECHA].

En Auto de medidas provisionales de [FECHA], dictado por la Sección Civil del Tribunal de Instancia de [SEDE], y unido el procedimiento sustanciado a la pieza separada del proceso, se acordó la separación provisional del matrimonio, la anotación registral de la revocación de poderes y consentimientos para vincular por la esposa bienes comunes del patrimonio por su actividad profesional, la atribución de la guarda y custodia del hijo menor y el correlativo uso de la vivienda familiar a la esposa demandada reconviniente, y se fijó un régimen de comunicación y visitas entre padre e hijo, de forma que el demandante reconvenido pueda tener consigo al hijo todos los sábados y todos los domingos desde las diez de la mañana hasta las ocho de la tarde, llevando siempre al hijo a dormir al domicilio materno y, en fin, se decidió la formación de inventario para la liquidación del régimen de bienes previamente disuelto por capitulaciones.

En su ejecución se ha evidenciado que no ha sido viable la visita del padre a su hijo de manera pacífica hasta el momento.

SEGUNDO.- El demandante postula la separación matrimonial en tanto que la demandada contesta oponiéndose a la separación y solicitando la disolución del matrimonio por divorcio.

Habida cuenta que según la nueva redacción del art. 86 CCiv dada por la Ley 15/2005, de 8 de julio, se decretará judicialmente el divorcio, cualquiera que sea la celebración del matrimonio, a petición de uno sólo de los cónyuges cuando hayan transcurrido tres meses desde la celebración del matrimonio, la acreditación de que dicho plazo ha transcurrido sobradamente conduce a efectuar dicha declaración con los efectos a la misma inherentes.

TERCERO.- Sentado lo antecedente, las partes hacen mérito alegatorio y probatorio de las medidas que siguen necesariamente a la separación, según previenen los arts. 92 y ss. CCiv, debiéndose destacar, enlazándolo con lo dicho, que en la fijación de guarda y custodia de los hijos menores, de alimentos, o de compensación por desequilibrio económico, está en la ley ausente toda idea de culpabilidad o inocencia.

En primer lugar, corresponde mantener que, de los pedimentos de la demanda reconvencional, no se traducirán al fallo aquellos efectos de la declaración de separación que se producen por ministerio de la ley, y en cuanto a la liquidación de la sociedad de gananciales, ésta fue disuelta conforme al art. 1.392.4.º CCiv mediante capitulaciones matrimoniales que convinieron régimen de absoluta separación de bienes.

Habiéndose formado inventario en pieza separada de los autos del pretendido patrimonio común pendiente de liquidación de los que pleitean, dentro del que puedan ponerse ciertos bienes en uso y disfrute exclusivo de uno de los cónyuges, de no lograrse un acuerdo extrajudicial, la división de esa comunidad, proindiviso postconyugal conforme al régimen de los arts. 392 y ss. CCiv, se sustanciará conforme al proceso del art. 810 LEC.

CUARTO.- La demanda reconvencional solicita le sea privada a D. la patria potestad sobre el hijo [NOMBRE DEL MENOR], por la vía del art. 92.3 CCiv, sin que pueda ser acogida tan grave determinación, ya que no ha quedado probado el incumplimiento de los deberes inherentes a la misma que abonan causa legal conforme al art. 170 CCiv.

Efectivamente, la demandada aduce que el padre rechazó el nacimiento de su hijo, llegando a amenazar con no reconocerlo, y que no le quiere. Aunque ello fuera cierto no es causa para privar de la patria potestad, y desde luego es contradictorio con la aseveración de parte de la Sra. de que su marido afirmase en una ocasión que si lograba tener en su poder a [NOMBRE DEL MENOR] no lo devolvería, con la perseverante petición de visitas del Sr. [NOMBRE Y APELLIDOS], y con la misma ejecución conflictiva del derecho a visitar al menor que se acordó en medidas provisionales del Tribunal de [LOCALIDAD]. Lo acreditado es que [NOMBRE DEL MENOR] fue inscrito como hijo matrimonial del Sr./a. y el proceso mental y volitivo interno del padre es un arcano para el proceso civil, siendo absolutamente pueril el episodio de [DESCRIPCIÓN DEL EPISODIO] que relata la contestación a la demanda.

Por otro lado, el estado de salud mental del Sr./a [NOMBRE Y APELLIDOS], según informe del psiquiatra del Centro de Salud de [LOCALIDAD], Dr./a [NOMBRE Y APELLIDOS], se encuentra estabilizado, aun reconociéndose padecer un síndrome depresivo ansioso, sujeto a tratamiento periódico ambulatorio, que el mismo afectado llega a admitir (preguntas 2.ª y 8.ª de su interrogatorio de parte), y en todo caso no reviste ninguna transcendencia de cara a las obligaciones dimanantes de la patria potestad, sobremanera cuando ambas partes están de acuerdo en que la guarda y custodia del menor quede exclusivamente para la madre.

En realidad, el Juzgador más bien opina que, a la vista de los avatares de la ejecución de las medidas provisionales, ambos cónyuges participan de un grado de personalidad inestable, aunque el trastorno conductual no reviste las características necesarias para privar a ninguno de los progenitores de la patria potestad, hasta el momento por lo menos, y que más al contrario, ello derivaría en un empeoramiento de la situación del menor.

El testimonio de las Sras. [NOMBRE Y APELLIDOS], referencial y subjetivo en cuanto a la falta de preocupación del padre por [NOMBRE DEL MENOR], y con relación a un presunto accidente doméstico intencionado el pasado [FECHA] de [MES], puesto en conexión con lo que declara la asistente social de [LOCALIDAD], no tiene el vigor preciso para, por sí mismo, entender provocada causa legal para despojar al padre de la potestad sobre el hijo.

Finalmente, respecto a la salida del domicilio conyugal del padre después del parto, las versiones son ampliamente contradictorias.

QUINTO.- No existiendo debate sobre la guarda y custodia del menor, que ha de atribuirse a la madre, en cuya compañía quedará [NOMBRE DEL MENOR], sin embargo, se niega por la Sra. el ejercicio del derecho de visitas para el padre, por lo menos en tanto no crezca el hijo, o se mejoren las condiciones psíquicas del Sr. [NOMBRE Y APELLIDOS].

Desde la psicología aplicada a la separación matrimonial, en favor del hijo menor, tan nefasto puede ser la privación de contacto con uno de los progenitores como la imposición conflictiva, cuando no violenta, de la visita del mismo cuando se opone aquel que tenga consigo al hijo.

Sin embargo, por la edad de [NOMBRE DEL MENOR], siendo prudente, en la generalidad de los casos, acordar la guarda y custodia de los hijos, hasta por lo menos los tres años, por el progenitor primario, que también ordinariamente es la madre, el derecho de visita conflictivo, hasta dichos tres años, viene a tener escaso impacto en la personalidad del niño.

No se encuentran en el caso las graves circunstancias que muevan a limitar o suspender algo que es un derecho del padre que no tiene consigo al hijo menor (art. 94 CCiv), aunque sí por el contrario a modalizarlo conforme a su edad, discapacidad psíquica, y enfermedad crónica probada.

Así se ratifica el régimen resuelto en medidas provisionales, si bien en atención a los problemas derivados de su ejecución, y a la inexistencia del domicilio en localidad común o siquiera cercana, se establecerá que la comunicación se produzca en el módulo de asistencia social de [LOCALIDAD] lugar neutral y conveniente para ambos padres (la madre por su residencia, y el padre por coincidir con un servicio ‘ad hoc’ que puede compaginar con su trabajo), y pudiendo recabar los interesados el auxilio de fuerza pública mediante solicitud de oficio judicial para [ÓRGANO ADMINISTRATIVO], a fin de que tutelen las condiciones de la visita, que será siempre en presencia de la madre, pero sin que concurran otras personas, lo que se dispone no en términos absolutos, sino precisándose la autorización judicial específica, en evitación de hechos como los que por desgracia han tenido lugar, todo ello por supuesto, en los términos del art. 91 CCiv, es decir, esperando que estas garantías devengan innecesarias por el acuerdo de los cónyuges, y en tanto no se alteren sustancialmente las circunstancias, entre las que se declara elemental la edad y salud de [NOMBRE DEL MENOR], pudiendo después de los tres años cumplidos, ampliarse el tiempo de la comunicación, obviarse la presencia de la madre, e incluso ser pertinente la pernocta con el padre.

SEXTO.- Las partes no están de acuerdo en la fijación de una pensión alimenticia en favor del hijo menor.

La contribución de cada progenitor a los alimentos debidos a los hijos, que prevé el art. 93 CCiv, no se funda en un estado de necesidad en el alimentista, como ocurre con el derecho de alimentos entre parientes del Título VI del Libro I del CCiv (art. 147 CCiv), sino que es un régimen especial (STS de 5 de octubre de 1993, Rec. 536/1991), que arraiga en la posibilidad económica en el obligado, como ocurre en los arts. 146, 147 y 152.2.º CCiv, que es la referencia legal subsidiaria.

Si, conforme a los arts. 144 y 145 CCiv, la obligación alimenticia es de ambos padres, desde la economía de la madre procede de sus ingresos profesionales, y de prestación directa a través de la atención personal y proporcionando vivienda, ex art. 149 CCiv. Lo cual, pese a ser pingües tales ingresos, en tanto que la contribución al mantenimiento de los hijos menores procede del denominado contenido patrimonial de la patria potestad (vid. art. 154 CCiv), también habrá de proceder desde la economía del padre, de su salario por medio de una pensión de determinada cifra en metálico.

Para fijar los medios económicos del deudor, es decir, el demandante reconvenido, se atiende a que cobró de la empresa que le emplea, en [IMPORTE], [IMPORTE] euros brutos, lo que se traduce en otro certificado, en [IMPORTE] euros netos mensuales con [IMPORTE] euros de retribuciones extras, que podemos sumarlas, en tanto que la retención fiscal quede compensada, si se valora el que el Sr. reconoce obtener retribuciones extraordinarias en la respuesta 5.ª de su interrogatorio de la pieza de medidas provisionales. Por ello, se estima que las percepciones reales del demandante deben ser siempre superiores a los [IMPORTE] euros mensuales.

El marido prueba una serie de abonos en que incurre necesariamente para ingresar su salario

Si admitimos una renta libre de [IMPORTE] euros mensuales, teniendo en cuenta, de un lado las exigentes necesidades del niño, y algunas de las previsiones cuantificadoras, parece razonable estimar la pensión de alimentos en [IMPORTE] euros mensuales, siendo el global aproximadamente la tercera parte de la renta libre del perceptor de la renta.

La cláusula de estabilización conforme a los incrementos del salario del deudor de las pensiones carece de certeza y origina graves dificultades de ejecución, siendo además desincentivadora profesionalmente, por lo que se recurre a la más adecuada de articular la fórmula habitual de conjurar la depreciación de capacidad adquisitiva, a salvo siempre la modificación por alteraciones sustanciales en la economía de los interesados, tanto en uno como en otro sentido.

SÉPTIMO.- El vencimiento parcial, con independencia de lo que se opine acerca de la aplicabilidad del principio del art. 394 LEC para los juicios declarativos a estos procesos especiales no dispositivos, no apreciándose temeridad de ninguna parte, indica que cada litigante abone las costas causadas a su instancia y las comunes por mitad.

Vistos los preceptos legales citados, los demás de general y pertinente aplicación, a virtud de la potestad jurisdiccional conferida, en nombre de S.M. el Rey de España, pronuncio el siguiente

FALLO

Que, estimando parcialmente la demanda presentada por la Procurador de los Tribunales [NOMBRE Y APELLIDOS], en representación de D [NOMBRE Y APELLIDOS], contra Dña. [NOMBRE Y APELLIDOS], representada por el Procurador/a de los Tribunales [NOMBRE Y APELLIDOS], y asimismo estimando en parte la reconvención formulada, declaro la disolución por divorcio del matrimonio formado por D [NOMBRE Y APELLIDOS] y Dña. por concurrir todos los requisitos que, con carácter objetivo, vienen establecidos en el art. 86 CCiv, decretando las siguientes medidas:

1.ª) Ambos cónyuges pueden señalar libremente su domicilio, y la esposa tiene derecho a excluir al esposo de la vivienda que fue domicilio conyugal, en la que tendrá en compañía al hijo común [NOMBRE DEL MENOR], cuyo cuidado diario se le atribuye.

2.ª) Se concede al padre un derecho de comunicación y estancia con el hijo común, de dos horas y media, dos días laborables de la semana, y de cuatro horas cada sábado o domingo, que se verificará en presencia de la madre, debiendo preavisarla con veinticuatro horas de anticipación para que se produzca en el módulo de asistencia social de [LOCALIDAD], procediendo, si lo solicitare alguna de las partes, a remitir oficio a [ÓRGANO ADMINISTRATIVO] para que custodie las condiciones de la comunicación y visita, y debiéndose recabar autorización judicial para que concurran otras personas, todo ello salvo pacto entre los litigantes y sujeto a modificación, además de lo procedente en Ley, cuando cumpla el menor la edad de tres años.

3.ª) Se fija una pensión alimenticia en favor del hijo común y en cuantía de [IMPORTE] euros ( €), a cargo del demandante, pagaderas por meses anticipados dentro de los primeros cinco días de cada mes, mediante ingreso en la cuenta corriente que designe la demandada, actualizables anualmente conforme al índice que publique el Instituto Nacional de Estadística u organismo que lo sustituya.

Se absuelve al demandante reconvenido de cuantos demás pedimentos se contienen en la demanda reconvencional.

No se hace expresa declaración sobre costas.

Una vez firme esta resolución, líbrese mandamiento para el asiento del divorcio del matrimonio al Registro Civil de [LOCALIDAD], acompañándose testimonio de esta sentencia.

Líbrese y únase testimonio de esta resolución a las actuaciones, con inclusión de la original en el Libro de Sentencias.

Así por esta mi sentencia, juzgando definitivamente en la instancia, lo pronuncio, mando y firmo.

Contra la anterior Sentencia cabe Recurso de Apelación ante la Ilma. Audiencia Provincial de [LOCALIDAD], que deberá interponerse en el plazo de veinte días hábiles a contar desde el siguiente a la notificación de la misma, mediante escrito ante este Tribunal exponiendo el apelante las alegaciones en que se base la impugnación, además de citar la resolución apelada y los pronunciamientos que impugna. El recurso no suspenderá la eficacia de las medidas que se han acordado, y si la impugnación afecta únicamente a los pronunciamientos sobre medidas, se declarará la firmeza del pronunciamiento sobre la separación conyugal.

Para interponer el recurso será necesario la constitución de un depósito de 50 euros, sin cuyo requisito no será admitido a trámite. El depósito se constituirá consignando dicho importe en la Cuenta de Depósitos y Consignaciones que este Tribunal tiene abierta en el grupo [GRUPO] con el número [NÚMERO], indicando en el campo concepto del resguardo de ingreso que se trata de un "Recurso" código 02-Apelación. La consignación deberá ser acreditada al interponer el recurso (disp. adic. 15.ª de la LOPJ).

No están obligados a constituir el depósito para recurrir los declarados exentos en la disposición citada y quienes tengan reconocido el derecho a la asistencia jurídica gratuita.

Firma del Juez:

========================================================================
