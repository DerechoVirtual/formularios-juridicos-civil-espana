---
name: solicitud-actualizar-pension-alimentos-segun-ipc-civ-0334
description: "Solicitud de actualizar la pensión de alimentos según el IPC con reclamación de atrasos. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud de actualizar la pensión de alimentos según el IPC con reclamación de atrasos

> Formulario **CIV-0334** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Demanda ejecutiva dentro del proceso de familia para exigir el cumplimiento de la sentencia que fijó una pensión de alimentos actualizable anualmente conforme al IPC, cuando el obligado al pago no ha aplicado la actualización. Se reclaman los atrasos generados por la falta de actualización y se pide que se tenga por actualizada la pensión para el futuro.

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud de actualizar la pensión de alimentos según el IPC con reclamación de atrasos» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud de actualizar la pensión de alimentos según el IPC con reclamación de atrasos” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:solicitud-actualizar-pension-alimentos-segun-ipc-civ-0334`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (9 veces)
- [ ] NOMBRE Y APELLIDOS DE LA PARTE EJECUTADA (4 veces)
- [ ] IMPORTE (3 veces)
- [ ] NOMBRE Y APELLIDOS DE LA PARTE EJECUTANTE (3 veces)
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A (2 veces)
- [ ] AÑO
- [ ] CLASE DE PROCEDIMIENTO
- [ ] DESGLOSE DE LOS ATRASOS POR PERIODOS
- [ ] DÍA
- [ ] EMPRESA O ENTIDAD PAGADORA
- [ ] LOCALIDAD
- [ ] MES
- [ ] MESES
- [ ] Nº
- [ ] Nº DE PROCEDIMIENTO
- [ ] Nº DE ROLLO
- [ ] PLAZO TRANSCURRIDO
- [ ] REFERENCIA A LA RESOLUCIÓN QUE FIJÓ LA PENSIÓN
- [ ] SEDE
- [ ] SENTIDO DE LA RESOLUCIÓN DE LA AUDIENCIA PROVINCIAL

## Normas que cita el formulario

- art. 545.1 LEC
- art. 538 LEC
- art. 539.1 LEC
- art. 517.2.1.º LEC
- art. 93 Código Civil
- art. 92 CC
- art. 154.1.º CC
- art. 549 LEC
- art. 550 LEC
- art. 551 LEC
- art. 571 LEC
- art. 776 LEC
- art. 539.2 LEC
- art. 583 LEC
- art. 711 LEC

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

- Junto a «…damentales «el de alimentarlos, educarlos y procurarles una formación integral».»: comprobar la redacción vigente de los arts. 92, 93 y 154 CC tras las reformas posteriores (Leyes 8/2021 y 4/2024) antes de entrecomillarlos.

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

A LA SECCIÓN CIVIL (SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD) DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales y de D./Dña. [NOMBRE Y APELLIDOS DE LA PARTE EJECUTANTE], cuya representación tengo acreditada en los autos de [CLASE DE PROCEDIMIENTO], registrados con el número [Nº DE PROCEDIMIENTO], seguidos frente a D./Dña. [NOMBRE Y APELLIDOS DE LA PARTE EJECUTADA], cuyos datos personales obran en las actuaciones, siguiendo instrucciones de mi mandante y como mejor proceda en Derecho, DIGO:

Que mediante el presente escrito solicito la ejecución de la sentencia dictada con fecha [FECHA], todo ello según resulta de los siguientes

HECHOS

PRIMERO.– El pasado día [FECHA] por el Tribunal al que me dirijo se dictó sentencia que en su parte dispositiva decía lo siguiente: [TRANSCRIPCIÓN DEL FALLO EN LO RELATIVO A LA PENSIÓN DE ALIMENTOS Y SU ACTUALIZACIÓN].

[OPCIONAL — si ha lugar]
Interpuesto recurso de apelación, se resolvió en la Audiencia Provincial, mediante resolución firme de fecha [FECHA], declarando [SENTIDO DE LA RESOLUCIÓN DE LA AUDIENCIA PROVINCIAL]. A los efectos pertinentes designo las actuaciones seguidas en los presentes autos y en el rollo de apelación número [Nº DE ROLLO].

SEGUNDO.– Que, habiendo transcurrido [PLAZO TRANSCURRIDO] desde que se dictó la sentencia, y a pesar de que en la misma se fijaba una actualización anual del importe de la pensión alimenticia conforme a las variaciones del IPC publicadas por el Instituto Nacional de Estadística, el demandado no ha actualizado voluntariamente el importe de la citada pensión, por lo que mi mandante se ve obligada a acudir a la vía judicial para hacer efectiva la misma.

TERCERO.– Partiendo como base de la fecha de [FECHA] y como consecuencia de las revisiones aplicadas conforme a los índices del IPC correspondientes a los meses de [MESES], resulta que la pensión fijada ha experimentado los siguientes aumentos: [CUADRO DE ACTUALIZACIONES: PERIODO | ÍNDICE IPC APLICADO | IMPORTE ACTUALIZADO DE LA PENSIÓN].

A efectos probatorios se acompaña certificado expedido por el Instituto Nacional de Estadística comprensivo de los índices de precios al consumo de los períodos indicados.

CUARTO.– Que, como resultado de la aplicación de las anteriores actualizaciones, D./Dña. [NOMBRE Y APELLIDOS DE LA PARTE EJECUTADA] resulta deudor/a de mi representado/a, en concepto de atrasos derivados de la no actualización de la pensión en el período comprendido entre [FECHA] y [FECHA], de la cantidad de [IMPORTE] euros, desglosada de la siguiente forma: [DESGLOSE DE LOS ATRASOS POR PERIODOS].

FUNDAMENTOS DE DERECHO

I.– COMPETENCIA.

Según el art. 545.1 LEC, será competente para la ejecución de resoluciones judiciales y de transacciones y acuerdos judicialmente homologados o aprobados el tribunal que conoció del asunto en primera instancia o el que homologó o aprobó la transacción o el acuerdo.

Por eso se presenta esta demanda ante el Tribunal al que me dirijo, ya que fue quien dictó la sentencia que sirve de título para la presente ejecución.

II.– LEGITIMACIÓN.

El art. 538 LEC regula que es parte en el proceso de ejecución la persona o personas que piden y obtienen el despacho de la ejecución y la persona o personas frente a las que ésta se despacha.

III.– POSTULACIÓN.

Conforme a lo dispuesto en el art. 539.1 LEC, la demanda viene firmada por abogado y procurador, ya que estamos ante la ejecución de una resolución dictada en un proceso en que es preceptiva la intervención de dichos profesionales.

IV.– TÍTULO DE EJECUCIÓN.

El art. 517.2.1.º LEC enumera como uno de los títulos que llevan aparejada ejecución la sentencia de condena firme, como la que sirve de fundamento a esta demanda.

A diferencia de lo que ocurre con las rentas en los contratos de arrendamiento, respecto de las que el Tribunal Supremo con reiteración ha mantenido que los efectos de la actualización se producen «ex nunc» y que no es posible la concesión de las diferencias que se podrían haber cobrado de haber ejercitado la facultad de revisión en momento oportuno, en relación con las pensiones alimenticias, al estar reconocidas en una sentencia que ha resuelto una contienda, no queda otra cosa que ejecutarla en sus propios términos, siempre que no pueda deducirse de los actos de las partes que ha existido un común acuerdo en alterar alguno de ellos, lo que podría suceder, por ejemplo, si el beneficiario o beneficiaria de la pensión accediera a percibir por un prolongado período de tiempo cantidades inferiores a las resultantes de la aplicación estricta de los índices actualizadores de la sentencia, mas no por el solo hecho de que se haya dejado pasar alguna anualidad sin reclamar la actualización, pues aparte de lo poco rentable que para dicho beneficiario sería el tener que acudir todos los años a reclamar del Tribunal la revisión y soportar en muchos casos un incidente de ejecución, no parece legal y menos justo el que hayan de ser los acreedores de la pensión los que necesariamente hayan de acudir al Juez para que, en definitiva, se les reconozca y materialice un derecho que ya tienen reconocido en sentencia y que implica una obligación de la otra parte y que, por estar en aquélla declarada, no debe sino cumplir.

Conclusión, la anterior, a la que contribuye el que, a diferencia también de lo que ocurre con las rentas en los contratos de arrendamiento, en los que las relaciones entre los arrendadores y los arrendatarios se enmarcan en el ámbito de la autonomía de la voluntad, no solo al tiempo de celebrar el contrato sino también en el trance de ejecutarlo, las pensiones alimenticias emanan de una norma imperativa, el art. 93 del Código Civil, que obliga al Juez, en todo caso, a determinar «la contribución de cada progenitor para satisfacer los alimentos», así como a adoptar «las medidas convenientes para asegurar la efectividad y acomodación de las prestaciones a las circunstancias económicas y necesidades de los hijos en cada momento», corolario de lo establecido en el art. 92 CC, conforme al cual «la separación, la nulidad y el divorcio no eximen a los padres de sus obligaciones para con los hijos», y en el art. 154.1.º CC, que, al enumerar el conjunto de deberes de la patria potestad, configura como uno de los fundamentales «el de alimentarlos, educarlos y procurarles una formación integral».

Por todo lo cual D./Dña. [NOMBRE Y APELLIDOS DE LA PARTE EJECUTADA] debe ser conminado/a al pago de los atrasos generados entre [FECHA] y [FECHA].

V.– REQUISITOS FORMALES.

La presente demanda contiene todos los requisitos enumerados en el art. 549 LEC, ya que se ha indicado cuál es el título en que se funda, la tutela ejecutiva que se pretende y las personas frente a las que se interesa el despacho de la ejecución, los bienes del ejecutado susceptibles de embargo conocidos por mi poderdante, así como las medidas de localización e investigación de otros bienes del ejecutado, dada la insuficiencia de los reseñados. Por último, se acompaña a la demanda ejecutiva la documentación necesaria de la contemplada en el art. 550 LEC.

VI.– PROCEDIMIENTO.

El Tribunal despachará ejecución y el Letrado de la Administración de Justicia concretará las medidas ejecutivas, por los trámites de los arts. 551 a 554 LEC, en relación con los arts. 571 y siguientes LEC, con las especialidades que se contienen en el art. 776 LEC para la ejecución forzosa de los pronunciamientos sobre medidas.

VII.– COSTAS.

En virtud de lo dispuesto en el art. 539.2 LEC en relación con el art. 583 LEC, las costas de esta ejecución deberán ser impuestas al ejecutado, ya que ha sido quien ha originado la necesidad de este procedimiento al no haber cumplido con lo establecido en la sentencia recaída en las presentes actuaciones.

De conformidad con lo anteriormente expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito con los documentos acompañados y copia de todo ello, se sirva admitirlo, y por comparecido al Procurador/a D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A] en la representación que ostenta de D./Dña. [NOMBRE Y APELLIDOS DE LA PARTE EJECUTANTE], entendiéndose conmigo las sucesivas diligencias; se tenga por solicitada la ejecución de la sentencia dictada por este Tribunal con fecha [FECHA] y, tras el previo traslado a la parte contraria, ACUERDE:

1.º Que se requiera a D./Dña. [NOMBRE Y APELLIDOS DE LA PARTE EJECUTADA] para que en el plazo de diez días abone a D./Dña. [NOMBRE Y APELLIDOS DE LA PARTE EJECUTANTE] la cantidad de [IMPORTE] euros que le adeuda, bajo apercibimiento de iniciarse la vía de apremio y, de mantenerse en su actitud, de incurrir en delito según preceptúa el art. 227 del Código Penal.

2.º Que se tenga por actualizada la pensión fijada en [REFERENCIA A LA RESOLUCIÓN QUE FIJÓ LA PENSIÓN], librándose oficio a [EMPRESA O ENTIDAD PAGADORA] a fin de que de la próxima nómina que perciba el demandado se le retenga el importe de [IMPORTE] euros mensuales, ingresándolo en la cuenta designada por mi mandante.

3.º Que se imponga por el Letrado de la Administración de Justicia al demandado una multa coercitiva con arreglo a lo dispuesto en el art. 711 LEC, y sin perjuicio de hacer efectivas sobre su patrimonio las cantidades debidas y no satisfechas.

Todo ello con imposición de las costas derivadas de esta ejecución al ejecutado.

Es justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Abogado/a Firma del Procurador/a
