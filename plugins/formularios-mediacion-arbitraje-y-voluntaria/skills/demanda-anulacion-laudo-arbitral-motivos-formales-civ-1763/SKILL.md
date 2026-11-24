---
name: demanda-anulacion-laudo-arbitral-motivos-formales-civ-1763
description: "Demanda de anulación de laudo arbitral por motivos formales. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de anulación de laudo arbitral por motivos formales

> Formulario **CIV-1763** del plugin **Mediación, MASC, arbitraje y jurisdicción voluntaria** (`formularios-mediacion-arbitraje-y-voluntaria`) · Civil › Jurisdicción voluntaria, MASC, mediación y arbitraje · normativa revisada el 24-11-2026.

## Qué es

Demanda ante la Sala de lo Civil y de lo Penal del Tribunal Superior de Justicia para ejercitar la acción de anulación de un laudo arbitral por motivos formales: vulneración del procedimiento (denegación inmotivada de prueba relevante) y falta de motivación del laudo, ambas contrarias al orden público (art. 41.1 de la Ley 60/2003, de Arbitraje). Debe presentarse en el plazo de dos meses desde la notificación del laudo (formulario adaptado a la reforma procesal de la LO 1/2025).

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de anulación de laudo arbitral por motivos formales» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de anulación de laudo arbitral por motivos formales” para mi caso». También puedes invocarla directamente con `/formularios-mediacion-arbitraje-y-voluntaria:demanda-anulacion-laudo-arbitral-motivos-formales-civ-1763`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-mediacion-arbitraje-y-voluntaria:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Mediación, MASC, arbitraje y jurisdicción voluntaria) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (15 veces)
- [ ] Nº (6 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] INSTITUCIÓN ARBITRAL (4 veces)
- [ ] IMPORTE (3 veces)
- [ ] NOMBRE Y APELLIDOS O DENOMINACIÓN SOCIAL (3 veces)
- [ ] DOMICILIO (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] Nº DE DOCUMENTOS (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] AÑO
- [ ] COMUNIDAD AUTÓNOMA
- [ ] DÍA
- [ ] HECHO QUE HABRÍAN ACREDITADO
- [ ] HECHO QUE SE PRETENDÍA ACREDITAR
- [ ] LA OBRA / LOS HECHOS
- [ ] MES
- [ ] NOMBRE Y APELLIDOS O DENOMINACIÓN SOCIAL DEL DEMANDANTE
- [ ] Nº DE CLÁUSULA
- [ ] Nº DE PROCEDIMIENTO ARBITRAL
- [ ] OBJETO DE LA DECLARACIÓN
- [ ] OTROS HECHOS RELEVANTES, SI LOS HUBIERA
- [ ] OTROS MEDIOS DE PRUEBA
- [ ] OTROS MOTIVOS, SI LOS HUBIERA
- [ ] PRUEBA PROPUESTA
- [ ] TIPO DE ARBITRAJE

## Normas que cita el formulario

- art. 399 Ley 1/2000
- art. 394 LEC
- art. 252.2 LEC

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

### Avisos de actualización (3) — se aplican en el texto, nunca se copian en el documento

- Junto a «…f) por ser el laudo contrario al orden público; [OTROS MOTIVOS, SI LOS HUBIERA].»: el artículo 41.1 de la Ley de Arbitraje recoge, en su letra d), que el procedimiento arbitral no se haya ajustado al acuerdo entre las partes o a la ley, y en su letra f) que el laudo sea contrario al orden público; comprobar la letra aplicable a cada motivo.
- Junto a «…l auto de 4 de mayo de 1992, rec. 31/1992, y la sentencia de 18 de julio de 1994»: completar número de sentencia o ECLI
- Junto a «…] Firma Abogado: ______________________ Firma Procurador: ______________________»: requisito de procedibilidad (art. 5 LO 1/2025): antes de demandar hay que intentar un medio adecuado de solución de controversias y acreditarlo con la demanda, salvo las materias excluidas del art. 5.2.

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

A LA SALA DE LO CIVIL Y DE LO PENAL DEL TRIBUNAL SUPERIOR DE JUSTICIA DE [COMUNIDAD AUTÓNOMA]

D./Dª [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, en nombre y representación de [NOMBRE Y APELLIDOS O DENOMINACIÓN SOCIAL DEL DEMANDANTE], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño a este escrito, comparezco ante este Tribunal y DIGO:

Que en la representación que ostento formulo demanda en ejercicio de la acción de anulación contra el laudo arbitral dictado por [INSTITUCIÓN ARBITRAL: Junta Arbitral de Consumo / Corte Arbitral / Asociación de Arbitraje] de [LOCALIDAD] en fecha [FECHA] en el procedimiento arbitral número [Nº DE PROCEDIMIENTO ARBITRAL], contra el demandado D./Dª [NOMBRE Y APELLIDOS O DENOMINACIÓN SOCIAL], con domicilio en [DOMICILIO], la cual fundo en los siguientes

HECHOS

PRIMERO.– Por medio de esta demanda se ejercita la acción de anulación del laudo arbitral arriba expresado con fundamento en los siguientes motivos: a) al amparo del artículo 41.1.f) de la Ley de Arbitraje, por no ajustarse el procedimiento a las prescripciones de la ley, infringiéndose el artículo 37 de la Ley de Arbitraje; b) al amparo del artículo 41.1.f) por ser el laudo contrario al orden público; [OTROS MOTIVOS, SI LOS HUBIERA].

Los antecedentes procedimentales son los siguientes:

1) En fecha [FECHA] se inició procedimiento arbitral con el número [Nº] ante [INSTITUCIÓN ARBITRAL] de [LOCALIDAD], por reclamación de [IMPORTE] euros frente a esta parte derivados del impago alegado por el demandante en la ejecución de un contrato de [CONTRATO: p. ej., arrendamiento de obra], que finalizó por el laudo arbitral dictado en fecha [FECHA], en el cual se condenaba a mi representada a indemnizar al demandante en la cantidad de [IMPORTE] euros, con imposición de costas del procedimiento arbitral.

2) En la notificación de iniciación del procedimiento arbitral se dio traslado de la solicitud de arbitraje a mi representada, que contestó en fecha [FECHA], proponiéndose prueba consistente en [PRUEBA PROPUESTA], que fue inadmitida por el árbitro sin ningún tipo de razonamiento.

3) Seguidamente, y sin observar otro trámite procedimental, se dictó laudo arbitral en fecha [FECHA], el cual fue notificado a mi representado en fecha [FECHA].

A efectos acreditativos, y de conformidad con lo que dispone el artículo 42 de la Ley de Arbitraje, se acompañan como documentos [Nº DE DOCUMENTOS] de la demanda el contrato de fecha [FECHA], objeto de controversia, en cuya cláusula [Nº DE CLÁUSULA] consta que la reclamación será resuelta a través del arbitraje [TIPO DE ARBITRAJE], el laudo dictado y la diligencia de notificación practicada a mi mandante.

SEGUNDO.– El primer motivo que alegamos se funda en la denegación totalmente indebida e inmotivada de la prueba testifical propuesta en nuestro escrito de fecha [FECHA], que era totalmente relevante para la resolución de la controversia, puesto que se proponía como testigos a [NÚMERO] personas que conocían [HECHO QUE SE PRETENDÍA ACREDITAR: p. ej., el estado de las obras objeto de controversia cuando la entidad demandante abandonó el trabajo], lo cual era absolutamente esencial para determinar [CUESTIÓN QUE SE PRETENDÍA PROBAR: p. ej., qué partidas de las facturadas se correspondían con obras efectivamente realizadas]. Pues bien, ante dicha proposición de prueba, el árbitro se limitó a rechazar simplemente la prueba propuesta por no considerarla pertinente y útil, sin mayor razonamiento, y dictando seguidamente el laudo sin más trámite (acompañamos como documentos [Nº DE DOCUMENTOS] certificación del procedimiento número [Nº] seguido ante [INSTITUCIÓN ARBITRAL], donde se incluyen la proposición de prueba (documento [Nº]), la resolución del árbitro de fecha [FECHA] denegatoria de la prueba (documento [Nº]) y la protesta formulada por esta parte (documento [Nº])).

TERCERO.– En fecha [FECHA] se dictó laudo arbitral sin seguir otro trámite procedimental, el cual carece de la más mínima motivación, puesto que se limita a dar por buenos los hechos alegados por el demandante y, sin otro tipo de razonamiento, se realiza un pronunciamiento estimatorio total de las pretensiones del demandante, con lo que se infringe manifiestamente lo dispuesto en el artículo 37.4 de la Ley de Arbitraje, el cual preceptúa la motivación de los laudos, colocando a esta parte en una situación de total indefensión al desconocer los motivos de estimación del laudo arbitral.

CUARTO.– [OTROS HECHOS RELEVANTES, SI LOS HUBIERA].

A los anteriores hechos son de aplicación los siguientes

FUNDAMENTOS DE DERECHO PROCESAL

COMPETENCIA

Es competente la Sala a la que me dirijo conforme a lo dispuesto en el artículo 8.5 de la Ley de Arbitraje, el cual establece: «Para conocer de la acción de anulación del laudo será competente la Sala de lo Civil y de lo Penal del Tribunal Superior de Justicia de la Comunidad Autónoma donde aquél se hubiere dictado».

PROCEDIMIENTO

Es de aplicación lo dispuesto en el artículo 42.1 de la Ley de Arbitraje, el cual establece que la acción de anulación se sustanciará por los cauces del juicio verbal, con las especialidades establecidas en dicho precepto, disponiendo el mismo que la demanda deberá presentarse conforme a lo establecido en el artículo 399 de la Ley 1/2000, de 7 de enero, de Enjuiciamiento Civil, acompañada de los documentos justificativos de su pretensión, del convenio arbitral y del laudo, y, en su caso, contendrá la proposición de los medios de prueba cuya práctica interese el actor.

PLAZO

El artículo 41.4 de la Ley de Arbitraje establece que la acción de anulación habrá de ejercitarse dentro de los dos meses siguientes al de la notificación del laudo, estando en este caso la acción interpuesta en plazo por cuanto que el laudo se notificó a mi representado en fecha [FECHA] (documento número [Nº]).

COSTAS

Es de aplicación el artículo 394 de la LEC.

FUNDAMENTOS DE DERECHO SUSTANTIVO

Motivo primero de anulación, al amparo del artículo 41.1.f) de la Ley de Arbitraje, por ser el laudo contrario al orden público al no haberse desarrollado el procedimiento de forma contradictoria, generando indefensión a esta parte, al no admitirse la prueba propuesta en fecha [FECHA].

El laudo es contrario al orden público por la indebida e inmotivada denegación de una prueba que era relevante y totalmente esencial en términos de defensa, pues el árbitro se limitó a afirmar simplemente que la prueba propuesta por mi representado no era considerada pertinente y útil, sin mayor razonamiento, con lo cual se ha impedido que declaren unos testigos que conocían [HECHO QUE SE PRETENDÍA ACREDITAR].

Con ello se ha privado a mi representado de la posibilidad de probar en el procedimiento, contraviniendo el orden público, el cual viene integrado en particular por las exigencias del artículo 24 de la Constitución, criterio que también ha tenido en cuenta el Tribunal Constitucional para valorar el orden público dentro del arbitraje, y así puede citarse el auto de 4 de mayo de 1992, rec. 31/1992, y la sentencia de 18 de julio de 1994 , dictada cuando estaba vigente la anterior Ley de Arbitraje, que indica que «en el artículo 45 (actualmente el 41) se contemplan las causas de anulación judicial de un Laudo, las cuales, en atención a la naturaleza propia del instituto del arbitraje, necesariamente deben limitarse a los supuestos de contravención grave del propio contrato de arbitraje (aps. 1.º a 4.º art. 45) o de las garantías esenciales de procedimiento que a todos asegura el artículo 24 C.E. (art. 45.5), sin extenderse a los supuestos de infracción del Derecho material aplicable al caso, y ello porque, de lo contrario, la finalidad última del arbitraje, que no es otra que la de alcanzar la pronta solución extrajudicial de un conflicto, se vería inevitablemente desnaturalizada ante la eventualidad de que la decisión arbitral pudiera ser objeto de revisión en cuanto al fondo». Como indica la STC 71/2003, de 9 de abril, en relación al derecho a utilizar los medios de prueba pertinentes para la defensa, es preciso que la falta de actividad probatoria se haya traducido en una efectiva indefensión del recurrente, o lo que es lo mismo, que sea «decisiva en términos de defensa», lo que exige que se haya alegado y fundamentado adecuadamente dicha indefensión material.

Pues bien, en este caso, esta parte ha fundamentado que pretendía probar que [HECHO QUE SE PRETENDÍA PROBAR: p. ej., las obras incluidas en la reclamación del demandante no habían sido ejecutadas efectivamente por dicha entidad], para lo que propuso [NÚMERO] testigos con conocimiento especialmente cualificado dada su participación en [LA OBRA / LOS HECHOS], y que sin duda hubieran afirmado que en la fecha [FECHA] [HECHO QUE HABRÍAN ACREDITADO], y que constituyen el montante más importante de su reclamación.

Por todo ello se han infringido las normas de orden público que regulan el procedimiento, colocando en situación de indefensión a esta parte, lo cual debe determinar la nulidad del laudo dictado.

Motivo segundo: al amparo del artículo 41.1.f) de la Ley de Arbitraje, en relación con el artículo 37.4 de la misma Ley, el laudo es contrario al orden público por su total falta de motivación.

El artículo 37.4 de la Ley de Arbitraje establece que el laudo deberá ser siempre motivado, a menos que se trate de un laudo pronunciado en los términos convenidos por las partes conforme al artículo 36.

Esta prescripción se integra dentro del más amplio contenido del conjunto de disposiciones de orden público que deben regir el procedimiento arbitral y su resolución, como extensión de los derechos establecidos en el artículo 24 de la Constitución, siendo que en este caso el laudo carece de las mínimas condiciones para rellenar tales garantías, al estar totalmente huérfano de motivación, dictándose una resolución que simplemente se limita a reproducir los hechos de la demanda y a estimar la pretensión, sin responder a ninguna de las alegaciones realizadas por esta parte.

Ello se agrava en mayor medida si ponemos en relación este motivo con el anterior, puesto que de la conjunción de ambos motivos se desprende que se ha tramitado todo el procedimiento arbitral con preterición de mi representado, colocándole en una situación de absoluta indefensión, que debe determinar la anulación del laudo dictado.

Por todo lo expuesto,

SUPLICO AL TRIBUNAL: Tenga por presentado este escrito, la copia electrónica del poder notarial de representación (informática o digitalizada) y demás documentos, junto con las copias que se acompañan, a las que se dará el curso legal, lo admita, me tenga por comparecido y parte en la representación que ostento de [NOMBRE Y APELLIDOS O DENOMINACIÓN SOCIAL], entendiéndose conmigo las sucesivas diligencias. Y tenga por formulada demanda en ejercicio de la acción de anulación del laudo arbitral de fecha [FECHA] dictado por [INSTITUCIÓN ARBITRAL] de [LOCALIDAD] contra el demandado [NOMBRE Y APELLIDOS O DENOMINACIÓN SOCIAL], cuyas demás circunstancias personales constan en el encabezamiento de este escrito, y, tras los trámites correspondientes, dicte sentencia por la que se anule y deje sin efecto el laudo arbitral dictado en fecha [FECHA] por [INSTITUCIÓN ARBITRAL] de [LOCALIDAD], imponiendo a la parte demandada las costas del proceso si se opusiere a nuestras pretensiones.

OTROSÍ PRIMERO DIGO: Que intereso la devolución del poder general para pleitos por precisarlo para otro menester, quedando en los autos copia debidamente testimoniada.

OTROSÍ SEGUNDO DIGO: Que la cuantía del pleito es de [IMPORTE] euros, que resultan del principal que se reclama y los intereses ya vencidos, al amparo del artículo 252.2 de la LEC.

OTROSÍ TERCERO DIGO: Que, al amparo del artículo 42.1 de la Ley de Arbitraje, solicito que se reciba a prueba el proceso y se practiquen los medios probatorios siguientes:

1) Documental, dando por reproducidos los documentos que acompaño.

2) Testifical, de D./Dª [NOMBRE Y APELLIDOS], con domicilio en [DOMICILIO], quien puede declarar sobre [OBJETO DE LA DECLARACIÓN], interesando que se le cite judicialmente para el acto de la vista.

3) [OTROS MEDIOS DE PRUEBA].

SUPLICO AL TRIBUNAL que tenga hechas las anteriores manifestaciones a los efectos legales que procedan y acuerde de conformidad.

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO]

Firma Abogado: ______________________

Firma Procurador: ______________________
