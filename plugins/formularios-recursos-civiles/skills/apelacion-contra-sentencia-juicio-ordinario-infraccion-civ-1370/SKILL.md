---
name: apelacion-contra-sentencia-juicio-ordinario-infraccion-civ-1370
description: "Apelación contra sentencia de juicio ordinario por infracción de normas y garantías procesales. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Apelación contra sentencia de juicio ordinario por infracción de normas y garantías procesales

> Formulario **CIV-1370** del plugin **Recursos civiles: reposición, apelación, casación y queja** (`formularios-recursos-civiles`) · Civil › Recursos · normativa revisada el 24-11-2026.

## Qué es

Escrito de interposición de recurso de apelación contra sentencia dictada en juicio ordinario, fundado en infracción de normas y garantías procesales que han producido indefensión (aquí, un emplazamiento inválido), con solicitud de nulidad de las actuaciones posteriores y reposición de las actuaciones al momento anterior a la infracción.

Es un modelo de tipo **recursos**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Apelación contra sentencia de juicio ordinario por infracción de normas y garantías procesales» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Apelación contra sentencia de juicio ordinario por infracción de normas y garantías procesales” para mi caso». También puedes invocarla directamente con `/formularios-recursos-civiles:apelacion-contra-sentencia-juicio-ordinario-infraccion-civ-1370`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-recursos-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Recursos civiles: reposición, apelación, casación y queja) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (16 veces)
- [ ] PAÍS (7 veces)
- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] DENOMINACIÓN SOCIAL DEL DEMANDADO (4 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] MES (4 veces)
- [ ] AÑO (3 veces)
- [ ] DÍA (3 veces)
- [ ] DENOMINACIÓN DE LA FERIA (2 veces)
- [ ] DENOMINACIÓN SOCIAL DEL ACTOR (2 veces)
- [ ] CONTENIDO DEL FALLO
- [ ] DENOMINACIÓN SOCIAL O NOMBRE DEL RECURRENTE
- [ ] FECHAS
- [ ] NOMBRE
- [ ] Nº DE PROCEDIMIENTO
- [ ] PROVINCIA

## Normas que cita el formulario

- art. 458.1 LEC
- art. 238.3.º LOPJ
- art. 459 LEC
- art. 155.1 LEC
- art. 240.1 LOPJ
- art. 155.3 LEC
- art. 243.1 LOPJ
- art. 276 LEC
- art. 465.3 LEC

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

- Al principio del formulario: adaptado a la reforma del Real Decreto-ley 6/2023, aplicable a los procesos incoados desde el 20-3-2024. Comprobar el órgano ante el que debe presentarse el escrito de interposición conforme al art. 458 LEC (con carácter general, el órgano que dictó la resolución apelada) y el encabezamiento que corresponda, así como el depósito para recurrir (disp. adic. 15.ª LOPJ).
- Junto a «… adic. 15.ª LOPJ).] A LA SECCIÓN CIVIL DE LA AUDIENCIA PROVINCIAL DE [PROVINCIA]»: La AP no tiene «Sección Civil» como denominación legal: se cita la Sección por su número (p. ej. «A LA SECCIÓN [ ] DE LA AUDIENCIA PROVINCIAL DE [ ]»). Fuente: LOPJ arts. 80 y 82 (Audiencia Provincial, sin cambio de denominación).

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

A LA SECCIÓN CIVIL DE LA AUDIENCIA PROVINCIAL DE [PROVINCIA]

Don/Doña [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, que actúa en nombre y representación de [DENOMINACIÓN SOCIAL O NOMBRE DEL RECURRENTE], según ya queda acreditado en autos de juicio ordinario n.º [Nº DE PROCEDIMIENTO], en los mismos comparezco y como mejor en Derecho proceda, DIGO (1):

Que el pasado día [DÍA] de [MES] de [AÑO] se me ha notificado la sentencia de fecha [FECHA], recaída en las presentes actuaciones, por la que se acuerda [CONTENIDO DEL FALLO], y estimando la misma gravosa para los intereses de mi mandante, dicho sea en términos de defensa, dentro del plazo de veinte días legalmente establecido en el art. 458.1 LEC, INTERPONGO RECURSO DE APELACIÓN contra dicha resolución.

REQUISITOS PROCESALES

I

Se presenta este escrito de interposición ante ese Tribunal, que es el competente para conocer del recurso, con arreglo al art. 458.1 LEC.

II

Se presenta este escrito de interposición dentro del plazo de veinte días contados desde el día siguiente a la notificación de la resolución impugnada (art. 458.1 y 3 LEC).

III

Mi representada está legitimada, en tanto que parte que niega su obligación de reparación tal y como se fijó el crédito de la parte actora, y tiene perjuicio o gravamen por la resolución impugnada, puesto que se condena al cumplimiento, mediante el pago de una indemnización (arts. 10 y 448.1 LEC).

IV

Las exigencias de postulación se llenan para este escrito de interposición, ya que se comparece mediante Procurador de los Tribunales, y asistido de abogado en ejercicio, ambos colegiados y habilitados para ejercer ante el Tribunal (arts. 23.1 y 31.1 LEC).

FUNDAMENTOS DEL RECURSO

INFRACCIÓN PROCESAL

Indefensión por haberse vedado la contestación de esta parte en base a un acto de comunicación nulo de pleno derecho.

Antecedentes

Presentada y admitida a trámite el [FECHA] demanda del Procurador/a Sr./Sra. [NOMBRE Y APELLIDOS], en representación de [DENOMINACIÓN SOCIAL DEL ACTOR], contra la mercantil extranjera [DENOMINACIÓN SOCIAL DEL DEMANDADO], recayó auto de admisión de [FECHA], en que se emplazaba para contestación a la mercantil demandada, lo que se ordenaba por medio de comisión rogatoria a [PAÍS]. Personada en fecha [FECHA] la demandada con el mandatario procesal Sr./Sra. [NOMBRE Y APELLIDOS], se le hizo saber que le restaba el término de una audiencia para contestar a la demanda, resolución que fue recurrida por ambas partes y ratificada en auto de [FECHA]. Presentándose luego escrito de contestación, por providencia de [FECHA] se inadmitió, devolviéndose con sus documentos, y se convocó la audiencia previa, frente a la que interpuso recurso de reposición, y entre tanto se tramitaba, en el acto de dicha audiencia previa se volvió a reproducir la solicitud de la demandada de que se subsanara su emplazamiento para contestar, o que se diera validez a su contestación presentada, con nulo éxito. Impugnado de adverso el predicho recurso de reposición, recayó auto desestimándolo de [FECHA].

En escrito de [FECHA], el Procurador/a Sr./Sra. [NOMBRE Y APELLIDOS] vuelve a producir un escrito por el que se solicita la dispensa de preclusión del trámite de contestación, a la luz de la comisión rogatoria remitida de [PAÍS], con retroacción de actuaciones, que en providencia de [FECHA] el Tribunal decidió repeler.

Celebrado el acto del juicio el [FECHA] se ha dictado sentencia condenatoria contra mi mandante.

Efectiva indefensión

El que se prescinda de las formas del procedimiento no engendra directamente un vicio de nulidad absoluta, sino que es exigido que tal elusión procure efectiva indefensión (cfr.: art. 238.3.º LOPJ).

Conforme a constante y reiterada doctrina constitucional se ha establecido que del mandato contenido en el art. 24 CE se deriva que la indefensión debe ser entendida como aquella que produce un efectivo y real menoscabo del derecho de defensa, es decir, que no se trate de una abstracción, de manera que una determinada irregularidad que atañe a las posibilidades de conducta procesal de parte sea originadora de indefensión, y otra nunca, sino que debe examinarse la circunstancia por comprobar si el demérito de defensa es un pretexto o algo verídico. Por otro lado la indefensión relevante no es situación objetiva de falta de defensa sino subjetiva, en el sentido de que haya tenido que imponerse contra la voluntad del justiciable, que acredite su voluntad expresa o tácita contraria, sin que se amparen intencionadas ausencias de «voz» procesal o simplemente la negligencia en el levantamiento de las cargas legales para ser oído.

Objetivamente, el no poder contestar la demanda supone la inviabilidad de plantear su resistencia a la pretensión actora, quedando sus posibilidades defensivas, por razón de la tesis de la «ficta contestatio» de nuestro sistema procesal en juicios declarativos, reducida a confiar en que la parte actora no logre probar los hechos constitutivos de su pretensión y a plantear contrapruebas que impidan, extingan o excluyan la existencia de tales hechos, lo que supone mengua capital de defensa.

Denuncia tempestiva de la infracción en la instancia (art. 459 LEC)

No puede dudarse de que esta parte, desde su personamiento en autos el [FECHA], ha protestado de su voluntad de comparecer y contestar a la demanda. Al negársele, ha producido dos recursos de reposición, las alegaciones en el acto de la audiencia previa, y el final escrito quiso suscitar, sin éxito, incidente de nulidad de actuaciones. Por otro lado, no se ha hecho dejación del derecho, es decir, la indefensión no ha sido asumida por el que la invoca.

Se dice por la contraparte que conoció la existencia de la demanda mi representada —aunque la comisión rogatoria no llevaba copia de la demanda y documentos—, que otorgó poderes para pleitos el representante legal de la mercantil extranjera, y que cuando compareció el mes de [MES] con dichos poderes y dirección letrada fue porque tal día expiraba el plazo para contestar del emplazamiento que se hizo —con copias de demanda y documentos— a quien era empleado o delegado hallado en un «stand» de la Feria internacional de [DENOMINACIÓN DE LA FERIA] en la ciudad de [LOCALIDAD], y que lo debía haber transmitido a la casa matriz. La suspicacia de la parte contendiente no tiene base, y los órganos judiciales no han de edificar sus decisiones sobre suspicacias, a riesgo de parcialidad, sino sobre datos ciertos (o la ausencia relevante de datos ciertos, claro es).

Hasta personarse en autos los asesores de mi patrocinada no pudieron conocer el contenido de la demanda y documentos anejos, y el individuo que recibió el emplazamiento en [LOCALIDAD] no lo hizo llegar a [DENOMINACIÓN SOCIAL DEL DEMANDADO] o tales asesores. En definitiva, sin acudir a la sospecha, no hay hechos que puedan hacer mantener que [DENOMINACIÓN SOCIAL DEL DEMANDADO] aceptó la indefensión, y ésta se produce claramente en términos objetivos.

Infracción de garantías procesales

Es claro que las resoluciones de fechas [FECHAS] se asientan en el emplazamiento de [FECHA], en una persona de la que conocemos que se llamaba [NOMBRE], y que se encontró en la Feria de [DENOMINACIÓN DE LA FERIA] por indicaciones de la parte actora, de la que se dice en la diligencia que era «empleado» de [DENOMINACIÓN SOCIAL DEL DEMANDADO], y que prefirió no firmar.

Y dicho emplazamiento es a todas luces ineficaz, ya que no se produce en el domicilio de la demandada, designado en la demanda (art. 155.1 y 2 LEC), ni en domicilio alguno, ya que se practicó en un establecimiento fugaz en una feria industrial, pero además, se entendió con persona inidentificada, por lo que no se hace personalmente (arts. 155.4, párrafo 2.º, 158 y 161 LEC), y resulta el supuesto cabal de ausencia de requisito indispensable en un acto de comunicación para alcanzar su fin, por añadidura a que determinara efectiva indefensión (art. 240.1 LOPJ).

La jurisprudencia venía preocupándose de considerar válidos una serie de domicilios en que se debe cívica y socialmente recibir comunicaciones por los ciudadanos (figurantes en padrón municipal: STS de 5 de noviembre de 1996, rec. 2221/1994; en boletín del colegio profesional: STS de 13 de abril de 1996, rec. 2987/1992; en registro civil: STS de 13 de noviembre de 1995, rec. 2163/1993; en registro de la propiedad: STS de 10 de abril de 1997, rec. 1117/1994; en registro mercantil: STS de 10 de septiembre de 1996, rec. 3634/1992), y así se amplía el elenco domiciliario en el art. 155.3 LEC. Lo que no se admite es el acto de comunicación al interesado en cualquier lugar fuera del domicilio designado, y tratándose de una persona jurídico mercantil, en una persona física cualquiera que no se identifique debidamente (o en su caso, en la sede del Tribunal cuando comparece, a través de procurador).

De otra parte, si se prescinde de la ilicitud de tal emplazamiento, remitida una comisión rogatoria a [PAÍS], porque el domicilio de la demandada se estableció en [PAÍS] por la parte actora, debió esperarse a su cumplimentación y devolución, o en otro caso, atenerse a la solicitud de la parte comparecida voluntariamente (que pedía traslado para contestar). La parte actora debió justificar la existencia de un establecimiento permanente en España para que funcionara como alternativa domiciliaria a la comisión rogatoria a [PAÍS]; en otro caso, el emplazamiento correcto era el intentado en el extranjero. El caso es que, si por el fracaso de la comunicación a través de comisión rogatoria, se hubiera declarado rebelde a mi mandante conforme al art. 15 del Convenio de La Haya de 1965, por el transcurso de un lapso temporal exagerado sin noticias de los tribunales de [PAÍS], la preclusión también debiera haberse dispensado conforme al art. 16, como indica dicha entidad, en atención de los datos del asunto.

La conclusión es que ha existido un quebrantamiento formal del acto de comunicación esencial que interpela para contestar a la demanda, y no ha conseguido acreditar el fin previsto del enteramiento cabal y completo a la demandada, mientras que ha provocado indefensión no pretextativa (arts. 238.3.º y 240 LOPJ).

La sanción ante ello es la declaración de nulidad con expulsión del mundo jurídico de los actos procesales posteriores al momento inmediatamente anterior a la providencia de [FECHA] —primera que concede eficacia al acto de comunicación que no debe tenerla—, excepto de los que, independientes, no hubieran podido ser distintos en caso de no haberse cometido la infracción de nulidad (art. 243.1 LOPJ), que son la consideración de personada y parte de la demandada con su representación procesal, y la unión a los autos de la comisión rogatoria recibida el día [FECHA].

FUNDAMENTOS DE FONDO

[FUNDAMENTOS DE FONDO, EN SU CASO. En este modelo no se alegan, al fundarse el recurso únicamente en infracción procesal.]

En su virtud,

SUPLICO AL TRIBUNAL

Que, teniendo por presentado este escrito con su copia, y documento acompañado, de lo que se ha dado traslado al Procurador de la parte contraria en la forma que previene el art. 276 LEC, se sirva tener por INTERPUESTO recurso de apelación contra la sentencia de fecha [FECHA], y

SUPLICO A LA SALA

Que, seguido que sea el legal procedimiento, dicte sentencia que decrete la nulidad radical de todas las actuaciones en el presente juicio promovido por [DENOMINACIÓN SOCIAL DEL ACTOR] hasta el momento inmediatamente anterior al dictado de la providencia de [FECHA], a excepción de las resoluciones que tienen por personada y parte a esta parte, y que tienen por unida la comisión rogatoria a [PAÍS] que consta recibida en autos, debiéndose conceder a esta parte plazo a fin de que vuelva a presentar su escrito de contestación que le fue rechazado, con lo demás que proceda.

Es Justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

OTROSÍ DIGO, que se acompaña a este escrito resguardo acreditativo del pago del depósito de 50 euros en la Cuenta de Depósitos y Consignaciones del Tribunal al que se dirige, conforme exige la disposición adicional 15.ª LOPJ, por lo que,

SUPLICO AL TRIBUNAL

Que tenga por causada la manifestación anterior a los efectos oportunos.

Por ser de Justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma de Abogado/a: [NOMBRE Y APELLIDOS] | Firma de Procurador/a: [NOMBRE Y APELLIDOS]

NOTA (1): La interposición de recurso de apelación que introduce argumentos sobre infracción de normas o garantías procesales puede tener tres clases de pedimentos. Además de las dos peticiones que se han visto, de un recurso de apelación por supuesta infracción formal en la sentencia, en que hay que pedir la revocación y el dictado por la Audiencia de nueva sentencia que entre al fondo decidiendo correctamente (art. 465.3 LEC), y por supuesta infracción formal anterior a la sentencia, que no puede subsanarse en la segunda instancia, en que hay que pedir la declaración de nulidad radical y reposición de actuaciones al momento en que se hallaban cuando la infracción se cometió (art. 465.4, párrafo 1.º LEC), está la posibilidad de que el defecto procesal advertido anterior a la sentencia sea subsanable en la segunda instancia. En este último caso, hay que pedir la subsanación, que se proveerá para efectuarse en plazo de diez días, salvo que se pueda subsanar en el acto de la vista (por ejemplo, el escrito de interposición no está presentado por Procurador habilitado ante la Audiencia, y en la vista comparece quien sí lo está, al que apodera «apud acta» el litigante que ha recurrido), y subsanada la infracción, se oirá a las partes, incluso pudiéndose practicar prueba, y seguirá sentencia que decida el objeto del pleito (art. 465.4, párrafo 3.º LEC). La parte opuesta, siempre pedirá la desestimación del recurso, y la confirmación de la resolución apelada, pero en el último caso, bien directamente, bien de manera subsidiaria, pedirá también la oportunidad de subsanación.
