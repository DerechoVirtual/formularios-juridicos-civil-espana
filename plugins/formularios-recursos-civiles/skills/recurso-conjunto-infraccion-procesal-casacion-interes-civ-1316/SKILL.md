---
name: recurso-conjunto-infraccion-procesal-casacion-interes-civ-1316
description: "Recurso conjunto por infracción procesal y casación por interés casacional (anterior al RDL 5 2023). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Recurso conjunto por infracción procesal y casación por interés casacional (anterior al RDL 5 2023)

> Formulario **CIV-1316** del plugin **Recursos civiles: reposición, apelación, casación y queja** (`formularios-recursos-civiles`) · Civil › Recursos · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **recursos**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Recurso conjunto por infracción procesal y casación por interés casacional (anterior al RDL 5 2023)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Recurso conjunto por infracción procesal y casación por interés casacional (anterior al RDL 5 2023)” para mi caso». También puedes invocarla directamente con `/formularios-recursos-civiles:recurso-conjunto-infraccion-procesal-casacion-interes-civ-1316`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-recursos-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Recursos civiles: reposición, apelación, casación y queja) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (9 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] REFERENCIA DE LA SAP (3 veces)
- [ ] FUENTE DOCTRINAL O JURISPRUDENCIAL (2 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] EXPONER EL MOTIVO
- [ ] FECHA DE LA SENTENCIA
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] NOMBRE Y APELLIDOS
- [ ] NORMA INFRINGIDA
- [ ] Nº
- [ ] Nº DE ARTÍCULO
- [ ] Nº DE MOTIVO
- [ ] Nº DE PROCEDIMIENTO
- [ ] SEDE
- [ ] TIPO Y Nº DE PROCEDIMIENTO

## Normas que cita el formulario

- art. 470 LEC
- art. 448.2 LEC
- art. 481.2 LEC
- art. 469.1 LEC
- art. 217 LEC
- art. 429.1 LEC
- art. 477.2.3 LEC
- art. 477.3 LEC
- art. 20 LCS
- art. 477.1 LEC

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

- Junto a «…tencia dictada el [FECHA] por el Tribunal de Instancia de [SEDE], plaza n.º [Nº]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

Rollo nº [Nº DE PROCEDIMIENTO]

A LA SECCIÓN DE LA AUDIENCIA PROVINCIAL

D. [NOMBRE Y APELLIDOS], Procurador de los Tribunales y de [NOMBRE DEL REPRESENTADO/A], según tengo acreditado en autos, ante la Sala comparezco y como mejor proceda en derecho DIGO:

1) Que en fecha [FECHA] esta parte ha sido notificada de la sentencia de fecha [FECHA DE LA SENTENCIA] dictada en el Rollo arriba expresado, cuya parte dispositiva es del tenor literal siguiente:

2) Que entendiendo que dicha sentencia no es ajustada a derecho, dicho sea con los debidos respetos y en términos de defensa, por medio del presente escrito, al amparo de lo dispuesto en la disposición final decimosexta de la LEC paso a INTERPONER RECURSO POR INFRACCIÓN PROCESAL Y RECURSO DE CASACIÓN ante la Sala Primera del Tribunal Supremo (o ante la Sala de lo Civil y lo Penal del Tribunal Superior de Justicia de...), en base a los siguientes presupuestos de admisibilidad y motivos:

I. ADMISIBILIDAD DEL RECURSO

PRIMERO.- Se recurre la sentencia de la Audiencia Provincial de fecha [FECHA] dictada en el Rollo arriba expresado, en proceso seguido por razón de la materia, siendo que dicha sentencia produce un evidente gravamen a esta parte, impugnándose todos sus pronunciamientos.

SEGUNDO.- El presente recurso se interpone al amparo de lo establecido en la disposición final decimosexta de la LEC, formulándose conjuntamente el recurso de casación por interés casacional con el recurso extraordinario por infracción procesal, quedando subordinada la admisión de éste a la del recurso de casación.

TERCERO.- El presente recurso se interpone dentro del plazo de veinte días establecido en los artículos 470 y 479 de la LEC, computados conforme al artículo 448.2 de la LEC.

CUARTO.- El recurso presenta interés casacional puesto que la sentencia impugnada se opone a la doctrina jurisprudencial del Tribunal Supremo (o se pronuncia sobre una cuestión en la que existe jurisprudencia contradictoria de las Audiencias Provinciales), infrigiendo los arts. de la Ley [NORMA INFRINGIDA], y la doctrina jurisprudencial en interpretación de dichos preceptos recogida en la S.T.S. de [FECHA], según se fundamentará seguidamente.

De conformidad a lo dispuesto en el artículo 481.2 de la LEC se acompaña certificación de la sentencia y texto de las que se aducen como fundamento del interés casacional (documentos número [Nº DE DOCUMENTO] a [Nº DE DOCUMENTO])

QUINTO.- Que siendo asimismo recurrible la citada sentencia por la vía del recurso extraordinario por infracción procesal, según dispone la disposición final decimosexta de la LEC, por medio del presente se interpone asimismo recurso de infracción procesal, en este único escrito y subordinado a la admisión de la casación, al amparo de los siguientes motivos: 1) al amparo del motivo [Nº DE MOTIVO] del artículo 469.1 de la LEC en relación con el artículo [Nº DE ARTÍCULO], sin que se haya podido denuncia la infracción en la instancia; 2)

II. MOTIVOS DEL RECURSO

A) DEL RECURSO POR INFRACCIÓN PROCESAL

PRIMERO.- El primer motivo de infracción procesal invocado al amparo del motivo segundo del artículo 469.1 de la LEC lo es por infracción del art. 217 de la LEC en cuanto a aplicación de las normas legales de distribución del onus probandi, al haberse aplicado erróneamente la inversión de la carga de la prueba concretado en el hecho de que la sentencia impugnada desconoce en supuestos de que ambas partes realizan una actividad con idéntico riesgo, no rige dicho principio básico de inversión de la carga de la prueba.

Desarrollo del motivo: El recurso extraordinario por infracción procesal se funda en la infracción de las reglas de distribución de la carga de prueba por la sentencia recurrida, lo cual se produce, según constante jurisprudencia, cuando, no estimándose probados unos hechos, se atribuyen las consecuencias de la falta de prueba a quién según las reglas generales o específicas, legales o jurisprudenciales, no le incumbía probar, y, por tanto, no le corresponde que se le impute la laguna o deficiencia probatoria. Esta cuestión tiene acceso a este recurso extraordinario, tal como se ha manifestado reiteradamente por el Alto Tribunal en sentencias de 26 de febrero, 14 de marzo y 6 de abril de 1998, entre otras muchas.

De acuerdo a los antecedentes, tanto en la sentencia de primera instancia como en la recurrida se parte de la inexistencia de prueba sobre la conducta negligente del demandado, lo que determinó la sentencia desestimatoria de primera instancia, posteriormente revocada por la Audiencia en la sentencia recurrida.

En el fundamento segundo de la sentencia dictada por el Tribunal en fecha [FECHA] (folio) se expresa claramente que no hay prueba alguna sobre la negligencia en la conducta del demandado, ausencia absoluta de prueba que determinó el pronunciamiento desestimatorio del Tribunal de Instancia, tal como se evidencia de la lectura de la sentencia.

La Audiencia entendió que, pese a esa ausencia absoluta de prueba aceptada expresamente en el fundamento segundo (folio), correspondía al demandado la carga de acreditar que obró con la diligencia debida, inversión de la carga de la prueba que infringe las normas legales sobre la materia recogidas en el art. 217 de la LEC.

Así, en primer lugar, es de aplicación la regla general recogida en el art. 217 de la LEC en cuanto a la carga del demandante de la prueba de la certeza de los hechos constitutivos de su derecho, y a él correspondía probar que fue el demandado quien rebasó el semáforo en fase roja. En segundo lugar, no puede operar aquí una inversión de la carga de la prueba, como se sostiene en la sentencia recurrida, ni so pretexto del principio de responsabilidad por riesgo, pues ambos intervinientes estaban conduciendo un vehículo y, en consecuencia, generaban idéntico riesgo en su actividad, sin perjuicio que fuera finalmente el demandante quien resultara con las graves lesiones descritas, no controvertidas en la demanda.

Por último, esta parte es conocedora que de la doctrina emanada en el anterior 1214 del Código Civil que venía a subrayar que cuando había prueba, no se podía citar como vulnerado este artículo (STS de 24 de febrero de 1993), lo cierto es que tal doctrina no es de aplicación a nuestro caso, pues claramente se aprecia que no se propuso ninguna prueba por la parte demandante en la audiencia previa, pese a que fue invitada a ello por el Juzgador en el trámite prevenido en el art. 429.1 de la LEC.

Por tanto, interesamos que se estime el motivo, revocando la sentencia recurrida y, conforme a la DF decimosexta, apartado 1, regla séptima de la LEC, se dicte nueva sentencia sobre la cuestión debatida en forma concorde al art. 217 de la LEC y, en consecuencia, entendemos que ha de confirmarse la sentencia dictada en primera instancia, imponiendo a la contraparte las costas del recurso de apelación.

SEGUNDO.- [EXPONER EL MOTIVO]
B) DEL RECURSO DE CASACIÓN POR INTERÉS CASACIONAL

PRIMERO.- Al amparo del art. 477.2.3º de la LEC y art. 477.3 de la LEC, al existir jurisprudencia contradictoria de las Audiencias Provinciales, por infracción del art. 20 de la Ley de Contrato de Seguro, el cual resulta vulnerado por cuanto que se hace una interpretación incorrecta del mismo al aplicar el interés del 20% a todo el periodo de mora una vez transcurridos más de dos años desde el siniestro, cuando el tenor literal del precepto establece que dicho interés de mora sólo puede aplicarse a partir de los dos años. Existe jurisprudencia contradictoria de las Audiencias Provinciales, de un lado, en la sentencia recurrida y en la sentencia firme de la misma Sección de la AP de [LOCALIDAD] de fecha [FECHA], en las cuales se sostiene la interpretación que se estima errónea, y, de otro lado, en sentencias firmes de la Sección… de la AP de [LOCALIDAD] y de [LOCALIDAD] de fecha [FECHA], en las cuales se sostiene la interpretación que se estima correcta, pretendiéndose que la Sala fije doctrina estableciendo que el art. 20 LCS dispone que el interés del 20% sólo se devenga una vez transcurridos los dos primeros años del siniestro y, por tanto, en los dos primeros años desde la producción del siniestro se devenga el interés legal incrementado en un 50%.

Desarrollo del motivo: En el caso de desestimarse el recurso por infracción procesal, la resolución del recurso presenta interés casacional, por existir jurisprudencia contradictoria de las Audiencias Provinciales, entendiendo que la sentencia recurrida aplica incorrectamente el art. 20 de la Ley de Contrato de Seguro.

Que la sentencia dictada el [FECHA] por parte de esa Sección de la Audiencia Provincial de [LOCALIDAD] en resolución del recurso de apelación presentado por esta parte ante la sentencia dictada el [FECHA] por el Tribunal de Instancia de [SEDE], plaza n.º [Nº] en los autos [TIPO Y Nº DE PROCEDIMIENTO] se estima que la misma hace una interpretación incorrecta del art. 20 de la LCS al aplicar en un caso como el presente, una vez transcurridos más de dos años, desde la producción del siniestro un interés del 20% desde la fecha del siniestro y no el legal incrementado en un 50% durante los dos primeros años y el del 20% a partir de esa fecha, lo cual implica una infracción normativa justificativa del acceso a la casación con fundamento en el art. 477.1 LEC.

El fundamento de la posición que sostiene esta parte se encuentra tanto en [FUENTE DOCTRINAL O JURISPRUDENCIAL] como en [FUENTE DOCTRINAL O JURISPRUDENCIAL], siendo una materia muy debatida y sobre la que existen decisiones contradictorias y que es la que justifica la concurrencia en este caso de un interés casacional (art. 477.2.3º LEC).

En tal sentido y como manifestación de la tesis que aquí se defiende se pueden citar las SAP [REFERENCIA DE LA SAP] y SAP [REFERENCIA DE LA SAP], ambas firmes, que se adjuntan por copia y como exponente de la posición contraria se citan las SAP [REFERENCIA DE LA SAP], también firmes, que asimismo se adjunta por copia.

Es por ello que, de forma subsidiaria, solicitamos que se case la sentencia, aplicando el interés legal incrementado en un 50% en los dos primeros años desde la producción del siniestro.

Por lo expuesto,

SUPLICO A LA SALA Que tenga por presentado este escrito con certificación de traslado, se sirva admitirlo y, en su virtud, tenga por interpuestos recursos por infracción procesal y de casación contra la sentencia [FECHA] dictada en el Recurso arriba indicado y que se remitan los autos a la Sala Primera del Tribunal Supremo, suplicando a la Excma. Sala acuerde estimar el recurso de infracción procesal, dictando nueva sentencia confirmatoria de la de primera instancia con imposición de costas de la segunda instancia al demandante. Caso de desestimarse el recurso por infracción procesal, se solicita la estimación de los motivos de casación alegados, casando en parte la sentencia dictada, fijando como doctrina el art. 20 LCS dispone que el interés del 20% sólo se devenga una vez transcurridos los dos primeros años del siniestro y, por tanto, en los dos primeros años desde la producción del siniestro se devenga el interés legal incrementado en un 50%, y aplicando en el caso el interés legal incrementado en un 50% en los dos primeros años a partir del siniestro.

OTROSÍ PRIMERO DIGO que, de conformidad con lo dispuesto en los apartados 3.d) y 6 de la disposición adicional decimoquinta de la LOPJ acompaño a este escrito resguardo de consignación en la cuenta de Depósitos y Consignaciones abierta a nombre del Tribunal del depósito exigido para interponer el recurso por importe de 50 euros.

Por lo que, SUPLICO A LA SALA que tenga por constituido el depósito, dejando interesada desde este momento su devolución para el caso de estimación total o parcial del recurso.

En L. y F.

(Firma Procurador y Abogado)

========================================================================
