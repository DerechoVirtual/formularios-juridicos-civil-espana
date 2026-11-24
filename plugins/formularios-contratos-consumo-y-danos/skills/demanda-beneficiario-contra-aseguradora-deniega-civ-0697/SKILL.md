---
name: demanda-beneficiario-contra-aseguradora-deniega-civ-0697
description: "Demanda del beneficiario contra la aseguradora que deniega la indemnización de un seguro de vida. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda del beneficiario contra la aseguradora que deniega la indemnización de un seguro de vida

> Formulario **CIV-0697** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio ordinario del beneficiario de un seguro de vida contra la aseguradora que deniega la indemnización alegando que el asegurado ocultó datos (p. ej. una enfermedad) al contestar el cuestionario de salud. Se funda en el art. 10 LCS y reclama el capital asegurado más los intereses del art. 20 LCS.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda del beneficiario contra la aseguradora que deniega la indemnización de un seguro de vida» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda del beneficiario contra la aseguradora que deniega la indemnización de un seguro de vida” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:demanda-beneficiario-contra-aseguradora-deniega-civ-0697`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (9 veces)
- [ ] FECHA (5 veces)
- [ ] DENOMINACIÓN SOCIAL DE LA ASEGURADORA (4 veces)
- [ ] NOMBRE Y APELLIDOS DEL ASEGURADO (4 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] DOMICILIO (2 veces)
- [ ] ENFERMEDAD (2 veces)
- [ ] FIRMA (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] SEDE (2 veces)
- [ ] AÑO
- [ ] CONTENIDO DE LA CONTESTACIÓN
- [ ] CORREO ELECTRÓNICO
- [ ] DATO RELEVANTE DEL INFORME MÉDICO
- [ ] DOMICILIO PROFESIONAL
- [ ] DÍA
- [ ] EDAD
- [ ] EL ASEGURADO / LA ASEGURADA
- [ ] ENFERMEDAD O CAUSA DEL FALLECIMIENTO
- [ ] EXPRESIÓN DEL CUESTIONARIO
- [ ] MES
- [ ] NOMBRE Y APELLIDOS DEL DEMANDANTE
- [ ] NOMBRE Y APELLIDOS DEL LETRADO/A
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] Nº DE INSCRIPCIÓN
- [ ] Nº DE PÓLIZA
- [ ] TELÉFONO
- [ ] TEXTO DE LA PREGUNTA DEL CUESTIONARIO

## Normas que cita el formulario

- art. 399.1 LEC
- art. 9.2 LOPJ
- art. 85.1 LOPJ
- art. 68 LEC
- art. 52.2 LEC
- art. 24 LCS
- art. 6.1.3.º LEC
- art. 7.4 LEC
- art. 1 LCS
- art. 251 LEC
- art. 10 LCS
- art. 10.3 LCS
- art. 3 Ley 21/1990
- art. 89 LCS
- art. 1269 Código Civil
- art. 20 LCS
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

### Avisos de actualización (2) — se aplican en el texto, nunca se copian en el documento

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «… de [MES] de [AÑO]. Firma del Abogado/a: [FIRMA] Firma del Procurador/a: [FIRMA]»: requisito de procedibilidad (art. 5 LO 1/2025): antes de demandar hay que intentar un medio adecuado de solución de controversias y acreditarlo con la demanda, salvo las materias excluidas del art. 5.2.

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

[NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, en nombre y representación de [NOMBRE Y APELLIDOS DEL DEMANDANTE], con domicilio en [LOCALIDAD], calle [DOMICILIO], según acredito con la escritura de poder inscrita en el Registro Electrónico de Apoderamientos Judiciales con el nº [Nº DE INSCRIPCIÓN]; asistido/a por el Letrado/a en ejercicio abajo firmante [NOMBRE Y APELLIDOS DEL LETRADO/A], con despacho profesional en [DOMICILIO PROFESIONAL], ante el Tribunal comparezco y, como mejor proceda en Derecho, DIGO:

Que mediante el presente escrito interpongo DEMANDA DE JUICIO ORDINARIO en reclamación de cantidad contra la entidad [DENOMINACIÓN SOCIAL DE LA ASEGURADORA], domiciliada en [DOMICILIO].

Que esta parte asume el compromiso de recibir cualquier comunicación dirigida por la oficina judicial, durante toda la fase declarativa e, incluso, en una eventual fase de ejecución, por medios telemáticos, en términos del art. 399.1 II LEC, consignándose a estos efectos la siguiente dirección de correo electrónico y número de teléfono: [CORREO ELECTRÓNICO] / [TELÉFONO].

Sirvan a la misma los siguientes:

HECHOS

PRIMERO.- Mi representado/a tiene la condición de beneficiario/a de la póliza de seguro de vida n.º [Nº DE PÓLIZA], cuya copia se acompaña señalada como documento número [Nº].

Dicha póliza fue suscrita con fecha [FECHA] por [ELEGIR: su difunto esposo / su difunta esposa / su difunto familiar], [NOMBRE Y APELLIDOS DEL ASEGURADO], en la que se concertó un capital de [IMPORTE] euros para el riesgo garantizado.

SEGUNDO.- [NOMBRE Y APELLIDOS DEL ASEGURADO] falleció en fecha [FECHA] como consecuencia de [ENFERMEDAD O CAUSA DEL FALLECIMIENTO], que el asegurado tenía diagnosticada desde [FECHA].

Se acompaña como documento número [Nº] informe médico forense.

TERCERO.- Comunicado el siniestro en fecha [FECHA] a la entidad aseguradora y haciendo llegar a ésta la oportuna reclamación, la misma denegó el pago de la indemnización debida alegando "que el fallecido ocultó el padecimiento de [ENFERMEDAD] cuando rellenó el cuestionario de salud".

Se acompaña como documento número [Nº] la carta que, bajo la referencia "Asunto", la demandada hizo llegar a mi principal, y en la que, reconociendo tácitamente la condición de asegurado de [NOMBRE Y APELLIDOS DEL ASEGURADO] y la de beneficiario/a de mi principal, le deniega el pago de la cantidad asegurada; y como documento número [Nº] el cuestionario de salud suscrito por [NOMBRE Y APELLIDOS DEL ASEGURADO], que, según reconoce la propia demandada, fue cumplimentado por un empleado pero plasmaba las manifestaciones del asegurado.

CUARTO.- El Letrado que firma esta demanda dirigió a la demandada la carta que se acompaña señalada como documento número [Nº].

En esa carta se requería a la aseguradora para que procediese a hacer efectiva a mi mandante la correspondiente indemnización y así evitar una reclamación judicial; es la actitud de silencio de la demandada lo que motiva la presente reclamación judicial.

Finalmente, mi representado/a envió un requerimiento fehaciente a la demandada con fecha [FECHA], con el objeto de iniciar una negociación tendente a resolver la controversia de manera amistosa y extrajudicial, que fue contestado por la entidad [DENOMINACIÓN SOCIAL DE LA ASEGURADORA] en los siguientes términos: [CONTENIDO DE LA CONTESTACIÓN].

Acompaño como documento núm. [Nº] el requerimiento efectuado y como documento núm. [Nº] la contestación de la demandada.

A los hechos anteriores son de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN Y COMPETENCIA.

Sobre materia de la competencia genérica del orden civil de la jurisdicción (art. 9.2 LOPJ), tiene la competencia objetiva y funcional (arts. 85.1 LOPJ y 45 LEC) la Sección Civil del Tribunal de Instancia de [SEDE] que por turno de reparto corresponda (art. 68 LEC), y la territorial, puesto que el domicilio del demandante se halla en la localidad de [LOCALIDAD] (art. 52.2 LEC y art. 24 LCS).

II.- CAPACIDAD.

Mi mandante es persona física, mayor de edad, en pleno ejercicio de sus derechos civiles, por lo que tiene capacidad para ser parte y capacidad procesal ex arts. 6.1.1.º y 7.1 LEC, como lo es la entidad demandada, [DENOMINACIÓN SOCIAL DE LA ASEGURADORA], persona jurídico-mercantil con capacidad para ser parte que se reconoce en el art. 6.1.3.º LEC, debiendo comparecer en juicio por medio de sus representantes legales (art. 7.4 LEC).

III.- LEGITIMACIÓN.

La legitimación activa corresponde a mi representado/a por su condición de beneficiario/a en la póliza de seguros suscrita por [EL ASEGURADO / LA ASEGURADA] con la mercantil demandada, que ostenta la correlativa legitimación pasiva como entidad aseguradora y parte del contrato de seguro, al amparo de lo dispuesto por el art. 1 LCS y en cuanto deudora por incumplimiento de sus obligaciones contractuales al no haber indemnizado a mi representado/a por el siniestro producido.

IV.- PROCEDIMIENTO.

El juicio ordinario a que se refieren los arts. 248, 249.2 y 399 y ss. LEC, por ser la cuantía reclamada superior a 15.000 euros.

V.- CUANTÍA.

La cuantía de la demanda asciende al importe reclamado, conforme a la regla 1.ª del art. 251 LEC, por lo que no quedan excepcionados los litigantes de representación técnica y defensa letrada con Procurador/a y Abogado/a habilitados ante el tribunal (arts. 23.1 y 31.1 LEC).

VI.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda cumple con el requisito de procedibilidad exigido por la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia, según se ha expuesto en el hecho cuarto y se acredita con los documentos aportados.

VII.- FONDO DEL ASUNTO.

El art. 10 LCS contempla el deber precontractual de declaración de riesgo al establecer que "el tomador del seguro tiene el deber, antes de la conclusión del contrato, de declarar al asegurador, de acuerdo con el cuestionario que éste le someta, todas las circunstancias por él conocidas que puedan influir en la valoración del riesgo".

La entidad aseguradora demandada entiende infringido dicho deber por parte del asegurado fallecido al no haber puesto en conocimiento que padecía [ENFERMEDAD] cuando se le pregunta en el cuestionario de salud si padece enfermedad crónica y contesta que no.

La STS de 4 de enero de 2008, Rec. 4746/2000, concreta la doctrina del Tribunal sobre el alcance de la obligación de declaración del riesgo de acuerdo con el cuestionario y razona en el siguiente sentido:

"El artículo 10 LCS impone al tomador del seguro el deber de declarar a la aseguradora, de acuerdo con el cuestionario que éste le someta, todas las circunstancias por él conocidas que puedan influir en la valoración del riesgo.

El incumplimiento de este deber faculta al asegurador para rescindir el contrato. Si el siniestro sobreviene antes de que el asegurador haga uso de esta facultad, la LCS prevé la reducción proporcional de la prestación. Pero si medió dolo o culpa grave del tomador del seguro quedará el asegurador liberado del pago de la prestación, según el inciso añadido al artículo 10.3 LCS por el artículo 3 de la Ley 21/1990, de 19 de diciembre, aplicable al caso controvertido. Estos preceptos son aplicables a los seguros de vida en virtud de lo previsto en el art. 89 LCS, el cual limita a un año, si no existe dolo, la posibilidad de impugnar el contrato.

El cumplimiento del deber de información que se impone al asegurado debe valorarse en relación con la declaración prestada ante el cuestionario desde el prisma subjetivo de la buena fe en relación con la finalidad del contrato y el grado de claridad y precisión del cuestionario que se le somete.

De la prueba analizada por el tribunal de instancia se infiere que el asegurado incurrió en una inexactitud, al contestar negativamente a la pregunta sobre si padecía «problemas de estómago», cuando había padecido molestias que motivaron atención médica. El hecho de que se haya probado que los análisis realizados con anterioridad a raíz de las expresadas molestias arrojaron un resultado de normalidad médica revelan, sin embargo, como justificable la postura del tomador del seguro, en cuanto pudo considerar que dichas molestias carecían de trascendencia alguna a los efectos del contrato de seguro, por lo que no constituían, a estos efectos, un 'problema'.

El canon de claridad y precisión del cuestionario impone, en efecto, en el caso enjuiciado una escasa exigencia al tomador del seguro, pues el cuestionario aludía de manera indeterminada a 'problemas' de estómago y otros órganos, sin precisar si se refería a simples molestias, trastornos o patologías específicas. En relación con la finalidad del contrato encaminado a cubrir el riesgo de fallecimiento por parte del paciente, la aplicación del canon de la buena fe conduce a estimar razonable que éste omitiese la declaración de unas molestias que se resolvieron médicamente mediante un diagnóstico que descartaba cualquier tipo de patología relevante o maligna, dado que no se ha acreditado que las molestias se reprodujesen o agravasen con anterioridad al momento en que se rellenó el cuestionario de salud que le fue exigido por la aseguradora.

No puede apreciarse, según esto, una infracción del art. 10 LCS."

En el mismo sentido recuerda la STS de 18 de julio de 2012, Rec. 1256/2010:

"La jurisprudencia de esta Sala, de la que es ejemplo la Sentencia de 11 de mayo de 2007, con cita de las de 31 de diciembre de 1998, 26 de julio de 2002 y 31 de mayo de 2004, define el dolo al que tales preceptos se refieren -en sentido plenamente aplicable al caso enjuiciado- como la «reticencia en la expresión de las circunstancias conocidas por el tomador del seguro que puedan influir en la valoración del riesgo y que de haberlas conocido el asegurador hubieran influido decisivamente en la voluntad de celebrarlo». (Sentencia de 15 noviembre 2007, rec. 5498/2000).

En el presente caso no hubo reticencia ni reserva mental pues si dejó de comunicar determinadas circunstancias era porque las consideró intrascendentes, como así se concluyó por los médicos al considerar el quiste «negativo para malignidad». Es decir, no hubo maquinaciones insidiosas, ni intención engañosa, ni representación consciente y probable de una enfermedad (art. 1269 del Código Civil)."

Por tanto, resulta que la regulación del deber de declaración de las circunstancias del riesgo ha convertido la inicial obligación del asegurado de declarar espontáneamente en otra de responder, trasladando a la aseguradora la iniciativa de la averiguación de las circunstancias que influyen en la evaluación del riesgo. La STS de 8 de noviembre de 2007, Rec. 5376/2000, así lo recoge cuando afirma que "El artículo 10, en lugar de concebir de una forma general y abstracta los límites del deber del tomador de declarar todas las circunstancias por él conocidas que puedan influir en la valoración del riesgo, ha acotado este deber limitándolo a la contestación del cuestionario que le someta el asegurador. Aparece así, no un deber espontáneo o independiente del tomador, sino un deber de responder a un cuestionario que tiene su precedente en el derecho suizo". El deber de contestación veraz exige por ello que por el asegurador se haya presentado el correspondiente cuestionario y exigido su cumplimentación, ya que el mismo actúa como un instrumento previo a poder concretar la concurrencia del actuar incumplidor contractual que se imputa al asegurado. Hasta tal punto es ello así que la jurisprudencia del TS ha declarado igualmente (SSTS de 15 de noviembre de 2007, Rec. 5498/2000; 31 de mayo de 1997, Rec. 1951/1993; y 6 de abril de 2001, Rec. 878/1996) que la ausencia de cuestionario, la no cumplimentación o la constatación de que fue el agente de seguros el que rellenó el mismo, sin intervención alguna del asegurado, equivale a falta de presentación, con la consecuencia de que es la aseguradora quien debe pechar con las consecuencias adversas de su falta por haber relevado al tomador del deber de cumplimentar dicha información previa al contrato.

En definitiva, el deber legal y precontractual de declaración del riesgo, que impone al tomador del seguro el art. 10 LCS, se traduce en el deber de contestar verazmente al cuestionario que el asegurador le someta. Así, el cuestionario permite hacer saber al tomador las circunstancias que el asegurador considera relevantes para la valoración del riesgo, pesando sobre éste la carga de incluir en él todos aquellos datos que estime que pudieran tener esta relevancia, con la mayor precisión y detalle, a fin de que el tomador del seguro pueda conocer el alcance de sus respuestas y la real influencia o alteración que los datos declarados u omitidos tienen para el riesgo asegurado, quedando en otro caso el tomador exonerado de su deber (art. 10, párrafo primero, inciso final).

Por tanto, en este supuesto se trataría de comprobar si la redacción del cuestionario era suficientemente clara para determinar que el asegurado infringió el deber de veracidad.

En el cuestionario que se aporta como documento número [Nº] consta como tercera pregunta si "[TEXTO DE LA PREGUNTA DEL CUESTIONARIO]". Y en el único espacio para responder el fallecido señaló que no.

La entidad demandada considera que se faltó al deber de veracidad y que no procede estimar la reclamación formulada. Sin embargo, el análisis del contenido del cuestionario de salud nos obliga a discrepar. Entendemos que las preguntas formuladas carecen de claridad, pues se acumulan varias y se ofrece una sola oportunidad de respuesta. La mezcla en un mismo apartado de enfermedades de naturaleza distinta es completamente inapropiada y la respuesta ofrecida no puede considerarse como un intento de ocultación de la verdad por parte del asegurado. Incluso la formulación sobre enfermedad crónica induce a confusión y consideramos que los conocimientos del fallecido sobre su enfermedad no eran suficientes como para entender el riesgo que implicaba y la circunstancia de que se trataba de una enfermedad crónica. Así resulta del informe médico acompañado como documento número [Nº], en el que se refiere [DATO RELEVANTE DEL INFORME MÉDICO].

Por tales circunstancias, entendemos justificable la postura del tomador del seguro, en cuanto pudo considerar que no padecía enfermedades de la clase por la que se le preguntaba. Como señalamos anteriormente, siguiendo la doctrina del TS, el cumplimiento del deber de información que se impone al asegurado debe valorarse en relación con la declaración prestada desde el grado de claridad y precisión del cuestionario que se le somete y, en este caso, el cuestionario es confuso y en absoluto preciso.

Resulta que el canon de precisión del cuestionario impone en el caso enjuiciado una escasa exigencia al tomador del seguro, pues el cuestionario aludía de manera indeterminada a "[EXPRESIÓN DEL CUESTIONARIO]", y previamente se preguntaba sobre una serie de padecimientos que no se identifican con las enfermedades del fallecido. Consideramos que era exigible por parte de la entidad aseguradora un mayor esfuerzo en la formulación de las preguntas, y mucho más teniendo en cuenta la edad del tomador, [EDAD] años cuando suscribe el seguro de vida, circunstancia que exige una mínima diligencia en la redacción del cuestionario de salud.

En el caso de autos, entendemos que no se ha producido en forma alguna un incumplimiento como para excluir la prestación contratada.

Y citamos la STS de 10 de mayo de 2011, Rec. 1401/2007, que concreta el alcance de la obligación de declaración del riesgo por parte del tomador del seguro: "...no toda omisión influye de la misma forma en la valoración del riesgo ni conlleva la liberación de la entidad aseguradora del pago de la prestación, sino tan solo la de aquellas circunstancias por él conocidas actuando con dolo o culpa grave determinante de la celebración de un contrato que, de otra forma, la aseguradora no hubiera concertado en las mismas condiciones (SSTS 27 de octubre de 1998, Rec. 1761/1994; 25 de noviembre de 1993, Rec. 933/1991; 31 de mayo de 2004, Rec. 2109/1998; 17 de octubre de 2007, Rec. 3398/2000, entre otras); dolo que la jurisprudencia ha definido como la «reticencia en la expresión de las circunstancias conocidas por el tomador del seguro que puedan influir en la valoración del riesgo y que de haberlas conocido el asegurador hubiera influido decisivamente en la voluntad de celebrarlo» (STS 15 de noviembre de 2007, Rec. 5498/2000, y las que cita)".

Aplicando la anterior doctrina jurisprudencial al supuesto objeto de análisis, entendemos que en modo alguno puede considerarse probada la concurrencia de dolo o culpa grave en la declaración del riesgo y que, siendo el cuestionario de salud muy poco preciso, resulta obligado estimar la reclamación formulada por el/la beneficiario/a de la póliza de vida contratada y, en consecuencia, condenar a la entidad demandada al pago de la suma reclamada en la presente demanda.

VIII.- INTERESES.

Deben reconocerse a mi patrocinado/a los del régimen especial del art. 20 LCS al haber incurrido en mora la entidad aseguradora demandada (reglas 4.ª y 6.ª).

Dichos intereses deberán devengarse desde la fecha del siniestro, sin que resulte objetable la aplicación al caso enjuiciado de lo previsto en la regla 8.ª del art. 20 LCS, puesto que estamos ante una póliza de seguro de vida, donde las sumas a pagar están predeterminadas en el contrato, sin que haya duda alguna sobre el importe de las mismas, tal como así lo entiende la reiterada doctrina jurisprudencial.

A mayor abundamiento, [DENOMINACIÓN SOCIAL DE LA ASEGURADORA] ni tan siquiera ha consignado hasta la fecha cantidad alguna, lo que demuestra la mala fe de la aseguradora y la falta de intención por su parte de pago de las cantidades a las que estaba obligada.

IX.- COSTAS.

Conforme al art. 394 LEC, las costas procesales han de imponerse a la parte demandada.

En virtud de lo expuesto,

SUPLICO AL TRIBUNAL

que tenga por presentado este escrito con sus documentos y copias de todo ello, teniéndome por comparecido y parte en la representación que ostento, y ordenando se entiendan conmigo las sucesivas actuaciones, se sirva admitir a trámite la demanda de juicio ordinario que se interpone y, una vez seguido el procedimiento por todos sus trámites, se venga a dictar sentencia que condene a la entidad aseguradora demandada a abonar a la actora la cantidad de [IMPORTE] euros, más los intereses del art. 20 LCS desde la fecha del fallecimiento, con costas procesales.

Es justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Abogado/a: [FIRMA]	Firma del Procurador/a: [FIRMA]
