---
name: demanda-nulidad-testamento-incapacidad-testador-falta-civ-0436
description: "Demanda de nulidad de testamento por incapacidad del testador y falta de formalidades. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de nulidad de testamento por incapacidad del testador y falta de formalidades

> Formulario **CIV-0436** del plugin **Herencias, testamentos y donaciones** (`formularios-herencias-y-donaciones`) · Civil › Sucesiones y donaciones · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio ordinario para que se declare la nulidad de un testamento cerrado, por falta de capacidad natural del testador al otorgarlo y por inobservancia de las formalidades legales esenciales. La ejercita un hijo del causante contra los herederos instituidos.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de nulidad de testamento por incapacidad del testador y falta de formalidades» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de nulidad de testamento por incapacidad del testador y falta de formalidades” para mi caso». También puedes invocarla directamente con `/formularios-herencias-y-donaciones:demanda-nulidad-testamento-incapacidad-testador-falta-civ-0436`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-herencias-y-donaciones:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Herencias, testamentos y donaciones) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (7 veces)
- [ ] Nº (6 veces)
- [ ] NOMBRE Y APELLIDOS DEL CAUSANTE (3 veces)
- [ ] SEDE (3 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NOMBRE DEL NOTARIO (2 veces)
- [ ] AÑO
- [ ] COLEGIO
- [ ] DIAGNÓSTICO
- [ ] DOMICILIO
- [ ] DÍA
- [ ] EDAD
- [ ] HOSPITAL
- [ ] IMPORTE
- [ ] INDICAR EL MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] INDICAR OTROS HECHOS RELEVANTES
- [ ] MES
- [ ] NOMBRE Y APELLIDOS
- [ ] NOMBRE Y APELLIDOS DEL ABOGADO/A
- [ ] NOMBRE Y APELLIDOS DEL DEMANDADO 1
- [ ] NOMBRE Y APELLIDOS DEL DEMANDADO 2
- [ ] NOMBRE Y APELLIDOS DEL DEMANDANTE
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] VECINDAD CIVIL

## Normas que cita el formulario

- art. 707 Código Civil
- art. 685 Código Civil
- art. 715 Código Civil
- art. 52.1.4.º LEC
- art. 422 Código Civil
- art. 5 Ley Orgánica 1/2025
- art. 662 Código Civil
- art. 706 Código Civil
- art. 1255 Código Civil
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

### Avisos de actualización (4) — se aplican en el texto, nunca se copian en el documento

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…idad de 15.000 euros, calculada conforme al artículo 251, regla 12.ª, de la LEC.»: comprobar la redacción vigente de los arts. 249 y 251 LEC tras la LO 1/2025 y las reglas de cuantía aplicables.
- Junto a «…gún la legislación civil aplicable por razón de la vecindad civil del causante].»: el original citaba el art. 422-3 del Código Civil de Cataluña, aunque el causante se identifica con vecindad civil común; comprobar el plazo aplicable según la ley sucesoria y suprimir la referencia que no proceda.
- Junto a «… en el curso de este proceso. Ello determina la nulidad del testamento otorgado.»: el art. 663 CC fue modificado por la Ley 8/2021 (ya no habla de «incapacitados»); ajustar la fundamentación a su redacción vigente.

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

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, actuando en representación de [NOMBRE Y APELLIDOS DEL DEMANDANTE], según se acredita [ELEGIR: por certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño / mediante designación apud acta otorgada ante el Letrado/a de la Administración de Justicia de [SEDE] que acompaño / mediante copia electrónica del poder notarial de representación que se acompaña y se solicita sea devuelta una vez testimoniada], y bajo la dirección letrada de D./Dña. [NOMBRE Y APELLIDOS DEL ABOGADO/A], Abogado/a del Colegio de [COLEGIO], ante el Tribunal comparezco y, como mejor en derecho proceda, por medio de la presente formulo demanda de juicio ordinario en ejercicio de acción de impugnación del testamento otorgado por el causante D./Dña. [NOMBRE Y APELLIDOS DEL CAUSANTE], la cual dirijo contra los herederos D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDADO 1] y D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDADO 2], con domicilio en [DOMICILIO], en base a los siguientes

HECHOS

PRIMERO.– Que mi mandante es hijo/a del causante D./Dña. [NOMBRE Y APELLIDOS DEL CAUSANTE], fallecido/a el día [FECHA], de vecindad civil [VECINDAD CIVIL], según resulta de las certificaciones de nacimiento, matrimonio y defunción que se adjuntan como documentos números [Nº].

SEGUNDO.– El causante D./Dña. [NOMBRE Y APELLIDOS DEL CAUSANTE] otorgó testamento cerrado en fecha [FECHA] ante el Notario de [LOCALIDAD] D. [NOMBRE DEL NOTARIO], protocolizado en fecha [FECHA], en el cual, entre otras disposiciones, instituía como herederos universales a los demandados, legando a mi representado los bienes que se expresan en la cláusula [Nº] del testamento (acompaño como documentos [Nº] testamento de fecha [FECHA], acta de protocolización de fecha [FECHA] y certificado del Registro General de Actos de Última Voluntad).

TERCERO.– Hechos que fundan la nulidad por incapacidad del testador.

Se ejercita la acción de nulidad del testamento por cuanto el causante, a la fecha de otorgar testamento, sufría una enfermedad mental severa que afectaba completamente a su entendimiento, [encontrándose en una fase avanzada de demencia senil,] no hallándose en plena capacidad y lucidez para comprender dicho acto.

El causante, de [EDAD] años de edad al momento de otorgar el testamento, sufría una enfermedad mental degenerativa, estando sometido a tratamiento médico, tal y como se desprende del informe realizado por el Dr./Dra. [NOMBRE Y APELLIDOS], que acompaño como documento n.º [Nº], en el cual se incluye el diagnóstico de [DIAGNÓSTICO], lo cual impedía que el causante pudiera otorgar testamento al carecer de la capacidad natural para hacerlo. Asimismo, y tal como se acreditará en este proceso, era notorio que el causante, en los últimos meses de su vida y desde luego desde mucho antes de otorgar el testamento impugnado, no podía ni tan siquiera mantener una conversación normal, era incapaz de coordinar una conversación y no conocía ni tan siquiera a sus propios hijos y nietos, debido al ostensible y manifiesto deterioro del estado general de su salud, que no solamente alteró las funciones psicomotoras, sino de forma muy particular las perceptivas y emocionales, anulando su capacidad de conciencia.

Si bien es cierto que el notario autorizante D. [NOMBRE DEL NOTARIO] afirma apreciar la capacidad natural del otorgante, lo cierto es que existen elementos que desvirtúan tal apreciación, como se deriva claramente del hecho de que el mismo día [FECHA] en que se otorgó el testamento el causante tuvo que ser atendido en el servicio de urgencias del Hospital de [HOSPITAL] al presentar un cuadro de desorientación psíquica y sensorial, tal como se acredita por los informes que se acompañan como documentos números [Nº].

De todo ello se deduce claramente que la apreciación del notario autorizante sobre la capacidad del causante se basó en un juicio erróneo, puesto que el mismo carecía de mínimas facultades para otorgar testamento, desvirtuándose de este modo la presunción de capacidad del testador, tal como se probará en el curso de este proceso.

CUARTO.– Motivo de impugnación referido a la falta de formalidades del testamento.

El testamento impugnado no cumple las formalidades del artículo 707 del Código Civil para los testamentos cerrados, en tanto que no consta en el acta de otorgamiento si el testamento estaba manuscrito o no, ni si estaba firmado por el testador, a la vez que tampoco se hizo constar que el testador se hubiere identificado en la forma prevenida en los artículos 685 y 686 del Código Civil.

Tal como es de ver en el acta de protocolización del testamento, el mismo estaba mecanografiado, sin firma del testador, de lo que se deduce que la falta de formalidades legales cuestiona la misma autenticidad del testamento, lo que determina su nulidad según dispone el artículo 715 del Código Civil, no siendo válido ni tan siquiera como testamento ológrafo.

En este sentido, si bien la regla general en la legislación civil es la de la libertad de forma o principio espiritualista, la forma del testamento es sin embargo un requisito ad solemnitatem, siendo los requisitos formales esenciales (STS de 24 de mayo de 1927), preceptivos e inderogables (STS de 19 de junio de 1959). En este caso nos encontramos ante un testamento cerrado donde no se han cumplido formalidades tan esenciales como la de hacer constar si el testamento estaba escrito por el testador o por otro medio mecánico, mencionar si había o no firma, la cual no existía en este caso, y no constando la identificación del testador por parte del Notario conforme establece el artículo 707.4.º en relación con los artículos 685 y 686 del Código Civil, todo lo cual supone el quebrantamiento de formalidades esenciales, al tiempo que hace dudar de que fuera efectivamente el causante quien compareciera ante el Notario a otorgar el testamento, todo lo cual determina la nulidad del testamento conforme al artículo 715 del Código Civil.

QUINTO.– Proceso de negociación previo y medios de solución de controversias de manera amistosa y extrajudicial.

Previamente a la interposición de la presente demanda se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial. En este sentido, se acudió a [INDICAR EL MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo. Se acompaña como documento n.º [Nº].

[OPCIONAL — incluir si procede]

SEXTO.– Otros hechos: [INDICAR OTROS HECHOS RELEVANTES].

FUNDAMENTOS DE DERECHO

COMPETENCIA.– Corresponde a los Tribunales de [SEDE], al ser el lugar en el que el finado tuvo su último domicilio, con fundamento en el artículo 52.1.4.º LEC.

LEGITIMACIÓN.– Le corresponde a esta parte la legitimación activa ante su condición de hijo/a del causante, heredero forzoso y legatario, pudiendo ser beneficiado por la declaración de nulidad, correspondiendo la legitimación pasiva a los herederos demandados.

PROCEDIMIENTO.– Versando la presente demanda sobre sucesión testamentaria, y no teniendo la misma regulada ninguna tramitación especial, debe decidirse por los trámites del juicio ordinario, conforme establece el artículo 249.2 de la Ley de Enjuiciamiento Civil, al exceder su cuantía de la cantidad de 15.000 euros, calculada conforme al artículo 251, regla 12.ª, de la LEC.

PLAZO DE EJERCICIO DE LA ACCIÓN DE NULIDAD.– Se ejercita la presente acción de nulidad antes de que transcurran [ELEGIR: cuatro años desde que el demandante conoció o pudo conocer razonablemente la causa de nulidad, de conformidad con lo que dispone el artículo 422-3 del Código Civil de Cataluña / el plazo que corresponda según la legislación civil aplicable por razón de la vecindad civil del causante].

REQUISITOS DE PROCEDIBILIDAD.– La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4.º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

NULIDAD DEL TESTAMENTO (FALTA DE CAPACIDAD).– Se ejercita la acción de nulidad del testamento citado en base a la incapacidad de testar del causante, tomando como fundamento los artículos 662, 663 y 666 del Código Civil en relación con el artículo 687 del mismo texto legal.

La falta de capacidad natural no resulta desvirtuada por la intervención de notario, puesto que la apreciación de capacidad de éste puede ser objeto de prueba en contrario, tal como indica la STS de 19 de septiembre de 1998, rec. 2318/1994, acreditándose la falta de capacidad por los documentos acompañados con esta demanda y a través de la prueba que pretende ejercitar esta parte en el curso de este proceso.

Ello determina la nulidad del testamento otorgado.

NULIDAD DEL TESTAMENTO (FALTA DE FORMALIDADES).– El testamento impugnado es nulo, con fundamento en el artículo 715 del Código Civil, al no haberse observado las formalidades establecidas en los artículos 706 y siguientes del Código Civil, sin que reúna los requisitos de validez establecidos para el testamento ológrafo.

La infracción tiene relevancia para declarar la nulidad del testamento puesto que, como declara la sentencia del Tribunal Supremo de 16 de junio de 1997, rec. 2210/1993: «el criterio de libertad que impera en el ámbito contractual –del que es ejemplo el artículo 1255 del Código Civil– quiebra en lo sucesorio, en especial en materia de testamentos, como ponen de relieve sus disposiciones reguladoras, al ser constante la jurisprudencia en el sentido de establecer que el carácter formalista del testamento obliga al cumplimiento escrupuloso de los requisitos extrínsecos y a su interpretación restrictiva, de manera que para su validez es absolutamente necesario que se cumplan de modo riguroso todas las solemnidades esenciales y requisitos exigidos por el Código Civil, como explícitamente reconoce el artículo 687, que estatuye la nulidad del testamento en cuyo otorgamiento no se observaren las formalidades establecidas, y ello hasta el punto de que este aspecto formal –imperativamente impuesto– predomina sobre la búsqueda interpretativa de la voluntad del testador, interpretación que avala el artículo 675 del Código».

COSTAS.– El artículo 394 LEC señala que las de primera instancia se imponen a la parte que vea en primera instancia rechazadas sus pretensiones.

En base a lo anterior,

SUPLICO AL TRIBUNAL que tenga por presentada la presente demanda con los documentos a ella adjuntos y sus copias y, tras la pertinente tramitación, se dicte por ese Tribunal sentencia en que se declare nulo el testamento objeto de la presente demanda, otorgado por el causante en fecha [FECHA], así como la nulidad de todas las actuaciones realizadas como consecuencia del referido testamento, condenando a los demandados a estar y pasar por dicha declaración, con imposición de costas si se opusieran a la demanda.

OTROSÍ PRIMERO DIGO.– Se fija la cuantía de este procedimiento en [IMPORTE] euros, de conformidad con lo que dispone el artículo 251, regla 12.ª, de la LEC.

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Abogado/a Firma del Procurador/a
