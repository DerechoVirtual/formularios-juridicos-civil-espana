---
name: recurso-casacion-interes-casacional-regimen-anterior-civ-1331
description: "Recurso de casación por interés casacional (régimen anterior al RDL 5 2023). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Recurso de casación por interés casacional (régimen anterior al RDL 5 2023)

> Formulario **CIV-1331** del plugin **Recursos civiles: reposición, apelación, casación y queja** (`formularios-recursos-civiles`) · Civil › Recursos · normativa revisada el 24-11-2026.

## Qué es

Escrito de interposición de recurso de casación por interés casacional (art. 477.2.3º LEC) contra sentencia de Audiencia Provincial que se opone a la jurisprudencia del Tribunal Supremo. El modelo desarrolla, como ejemplo, la aplicación de los intereses de mora del art. 20 de la Ley de Contrato de Seguro. Está redactado conforme al régimen anterior al Real Decreto-ley 5/2023.

Es un modelo de tipo **recursos**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Recurso de casación por interés casacional (régimen anterior al RDL 5 2023)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Recurso de casación por interés casacional (régimen anterior al RDL 5 2023)” para mi caso». También puedes invocarla directamente con `/formularios-recursos-civiles:recurso-casacion-interes-casacional-regimen-anterior-civ-1331`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-recursos-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Recursos civiles: reposición, apelación, casación y queja) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (8 veces)
- [ ] Nº (4 veces)
- [ ] PROVINCIA (2 veces)
- [ ] AÑO
- [ ] DÍA
- [ ] IMPORTE
- [ ] LOCALIDAD
- [ ] MES
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] NOMBRE Y APELLIDOS O DENOMINACIÓN SOCIAL DEL RECURRENTE
- [ ] Nº DE PROCEDIMIENTO
- [ ] Nº DE ROLLO
- [ ] SEDE
- [ ] SENTIDO DEL FALLO

## Normas que cita el formulario

- art. 477.2 LEC
- art. 477 LEC
- art. 479 LEC
- art. 448.2 LEC
- art. 481.2 LEC
- art. 477.2.3 LEC
- art. 477.3 LEC
- art. 20 LCS
- art. 487.3 LEC

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

- Al principio del formulario: este modelo responde al régimen del recurso de casación previo al Real Decreto-ley 5/2023; comprobar la redacción vigente de los arts. 477 y siguientes LEC (supuestos de admisión, plazos y requisitos de admisibilidad) y de la disposición adicional decimoquinta LOPJ antes de utilizarlo.

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

A LA SECCIÓN [Nº] DE LA ILMA. AUDIENCIA PROVINCIAL DE [PROVINCIA]

ROLLO Nº [Nº DE ROLLO]

Don/Doña [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, actuando en representación de [NOMBRE Y APELLIDOS O DENOMINACIÓN SOCIAL DEL RECURRENTE], según viene acreditado en los presentes autos, como mejor proceda en Derecho, DIGO:

1) Que en fecha [FECHA] esta parte ha sido notificada de la sentencia de fecha [FECHA] dictada en el Rollo arriba expresado, por la que [SENTIDO DEL FALLO]. Frente a dicha sentencia se dedujo solicitud de complemento, siendo desestimada por auto de fecha [FECHA], notificado en fecha [FECHA].

2) Que entendiendo que dicha sentencia no es ajustada a derecho, dicho sea con los debidos respetos y en términos de defensa, por medio del presente escrito, al amparo de lo dispuesto en el apartado 3º del artículo 477.2 de la LEC, interpongo contra la misma RECURSO DE CASACIÓN POR INTERÉS CASACIONAL, por oposición a la jurisprudencia del Tribunal Supremo, en base a los siguientes presupuestos de admisibilidad y motivos:

I. ADMISIBILIDAD DEL RECURSO

PRIMERO.- El presente recurso se deduce contra la sentencia dictada por la Audiencia Provincial en fecha [FECHA], por presentar interés casacional como se fundamentará ampliamente, al amparo de lo dispuesto en el apartado 2.3º del artículo 477 de la LEC, y produce un evidente gravamen a esta parte, impugnando el pronunciamiento relativo a [PRONUNCIAMIENTO IMPUGNADO; EJEMPLO: la imposición de los intereses del 20% a mi representada durante la totalidad del periodo de mora].

SEGUNDO.- El supuesto que habilita la presentación es que la resolución del recurso presenta interés casacional, al amparo de lo dispuesto en el apartado 2.3º del artículo 477 de la LEC, al tratarse de un proceso seguido por razón de cuantía inferior a 600.000 euros.

TERCERO.- El presente recurso se interpone dentro del plazo de veinte días establecido en el artículo 479 de la LEC, computados conforme al artículo 448.2 de la LEC.

CUARTO.- El recurso presenta interés casacional puesto que la sentencia impugnada se opone a la doctrina jurisprudencial del Tribunal Supremo en relación con [MATERIA; EJEMPLO: los intereses de mora que debe abonar el asegurador], con infracción del art. 20 de la Ley de Contrato de Seguro, que rechaza la teoría del tramo único aplicada por la sentencia recurrida, interpretando que deben diferenciarse dos tramos de interés, tal como se expresa por el Tribunal Supremo a partir de la sentencia del Pleno núm. 251/2007, de 1 de marzo de 2007 (recurso de casación 2302/2001), doctrina jurisprudencial recogida asimismo en la STS de 1 de julio de 2008 (núm. 670/2008), que se decantan por el criterio de los dos tramos, fijando como doctrina que el interés de demora a satisfacer al lesionado por la aseguradora debe calcularse, durante los dos primeros años siguientes al siniestro, al tipo legal más su 50% y, solo a partir de ese momento, al tipo del 20%.

La interpretación sostenida en la sentencia que se recurre es contraria a la doctrina jurisprudencial de la Sala Primera del Tribunal Supremo expresada, entre otras, en las citadas SSTS de 1 de marzo de 2007 y 1 de julio de 2008, por lo que el recurso presenta interés casacional.

QUINTO.- De conformidad con lo dispuesto en el artículo 481.2 de la LEC se acompaña certificación de la sentencia y texto de las que se aducen como fundamento del interés casacional (documentos número [Nº] a [Nº]).

II. MOTIVOS DEL RECURSO

PRIMERO.- Al amparo del art. 477.2.3º de la LEC y art. 477.3 de la LEC, por oposición a la jurisprudencia del Tribunal Supremo, con infracción del art. 20 de la Ley de Contrato de Seguro, el cual resulta vulnerado por cuanto que se hace una interpretación incorrecta del mismo al aplicar el interés del 20% a todo el periodo de mora una vez transcurridos más de dos años desde el siniestro, cuando el tenor literal del precepto establece que dicho interés de mora solo puede aplicarse a partir de los dos años. La interpretación de la sentencia recurrida se opone a la jurisprudencia del Tribunal Supremo, recogida en la sentencia del Pleno núm. 251/2007, de 1 de marzo de 2007, y en la STS de 1 de julio de 2008 (núm. 670/2008), pretendiéndose que la Sala aplique la doctrina desconocida por la sentencia recurrida, estableciendo que el art. 20 LCS dispone que el interés del 20% solo se devenga una vez transcurridos los dos primeros años del siniestro y, por tanto, en los dos primeros años desde la producción del siniestro se devenga el interés legal incrementado en un 50%.

Desarrollo del motivo: La sentencia dictada el día [FECHA] por esa Sección de la Audiencia Provincial de [PROVINCIA], en resolución del recurso de apelación presentado por esta parte frente a la sentencia dictada el [FECHA] por la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº] en los autos [Nº DE PROCEDIMIENTO], hace, a juicio de esta parte, una interpretación incorrecta del art. 20 de la LCS al aplicar, en un caso como el presente, una vez transcurridos más de dos años desde la producción del siniestro, un interés del 20% desde la fecha del siniestro y no el legal incrementado en un 50% durante los dos primeros años y el del 20% a partir de esa fecha, lo cual implica una infracción normativa del artículo 20 de la LCS, justificativa del acceso a la casación con fundamento en el art. 477.1 y 2.3º de la LEC.

El fundamento de la posición que sostiene esta parte se encuentra en la doctrina emanada de la Sala Primera en las expresadas SSTS de 1 de marzo de 2007 y 1 de julio de 2008, que se adjuntan por copia y a las que se opone la interpretación sostenida por la Audiencia en la sentencia recurrida, y que es la que justifica la concurrencia en este caso de un interés casacional (art. 477.2.3º LEC).

En efecto, la mora del asegurador, según la jurisprudencia de la Sala Primera del Tribunal Supremo, superado el viejo aforismo in illiquidis non fit mora, debe excluirse únicamente cuando de las circunstancias concurrentes en el siniestro o del texto de la póliza surge una incertidumbre sobre la cobertura del seguro que hace precisa la intervención del órgano jurisdiccional ante la discrepancia existente entre las partes al respecto, en tanto dicha incertidumbre no resulta despejada por la resolución judicial. Por el contrario, carece de justificación la mera oposición al pago frente a la reclamación por el asegurado o perjudicado aunque se formule en un proceso judicial, pues la razón del mandato legal radica no solo en evitar el perjuicio para el asegurado o perjudicado que deriva del retraso en el abono de la indemnización, sino también en impedir que se utilice el proceso como instrumento falaz para dificultar o retrasar el cumplimiento de la expresada obligación. No obstante, tal interpretación no autoriza a fijar un tramo de interés penitencial en todo caso, de manera que los intereses moratorios del art. 20 de la Ley de Contrato de Seguro solo son de aplicación cuando se han superado los dos años establecidos en el precepto. La controversia había dado lugar a distintas y contradictorias sentencias de las Audiencias Provinciales, unas aplicando la denominada teoría del tramo único, es decir, el 20% a todo el periodo una vez superados los dos años, como hace la sentencia recurrida, en tanto que otras aplicaban dos tramos de interés, postura esta que ha sido definitivamente acogida por el Tribunal Supremo a partir de la sentencia del Pleno de 1 de marzo de 2007 (recurso de casación 2302/2001), que se decanta por el criterio de los dos tramos, fijando como doctrina que el interés de demora a satisfacer al lesionado por la aseguradora debe calcularse, durante los dos primeros años siguientes al siniestro, al tipo legal más su 50% y, solo a partir de ese momento, al tipo del 20% (entre otras, STS 670/2008, de 1 de julio de 2008).

Por todo ello, de conformidad con lo dispuesto en el artículo 487.3 de la LEC se interesa que se case la sentencia recurrida, declarando la divergencia de la interpretación sostenida con la jurisprudencia en el sentido expuesto, con el pronunciamiento inherente.

En base a lo anterior,

SUPLICO A LA SALA que tenga por presentado este escrito teniendo por interpuesto el recurso de casación por interés casacional frente a la sentencia dictada por esa Sala en las presentes actuaciones de fecha [FECHA] y, tras la pertinente tramitación y remisión de las actuaciones al Tribunal Supremo, se dicte por éste sentencia estimatoria del recurso, casando en parte la sentencia recurrida, declarando que el art. 20 LCS dispone que el interés del 20% solo se devenga una vez transcurridos los dos primeros años del siniestro y, por tanto, en los dos primeros años desde la producción del siniestro se devenga el interés legal incrementado en un 50%, y aplicando en el caso el interés legal incrementado en un 50% en los dos primeros años a partir del siniestro.

OTROSÍ PRIMERO DIGO que, de conformidad con lo dispuesto en los apartados 3.d) y 6 de la disposición adicional decimoquinta de la LOPJ, acompaño a este escrito resguardo de consignación en la cuenta de Depósitos y Consignaciones abierta a nombre del Tribunal del depósito exigido para interponer el recurso, por importe de [IMPORTE] euros.

Por lo que SUPLICO A LA SALA que tenga por constituido el depósito, dejando interesada desde este momento su devolución para el caso de estimación total o parcial del recurso.

En virtud de lo anterior,

SUPLICO A LA SALA: que tenga por hecha la anterior manifestación.

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma de Procurador/a y Abogado/a.
