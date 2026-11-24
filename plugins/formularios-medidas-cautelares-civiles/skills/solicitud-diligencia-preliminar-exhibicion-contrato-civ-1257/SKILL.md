---
name: solicitud-diligencia-preliminar-exhibicion-contrato-civ-1257
description: "Solicitud de diligencia preliminar de exhibición del contrato de seguro de responsabilidad civil. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud de diligencia preliminar de exhibición del contrato de seguro de responsabilidad civil

> Formulario **CIV-1257** del plugin **Medidas cautelares y diligencias preliminares** (`formularios-medidas-cautelares-civiles`) · Civil › Medidas cautelares y diligencias preliminares · normativa revisada el 24-11-2026.

## Qué es

Escrito solicitando diligencia preliminar de juicio declarativo, de exhibición de contrato de seguro de responsabilidad civil.

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud de diligencia preliminar de exhibición del contrato de seguro de responsabilidad civil» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud de diligencia preliminar de exhibición del contrato de seguro de responsabilidad civil” para mi caso». También puedes invocarla directamente con `/formularios-medidas-cautelares-civiles:solicitud-diligencia-preliminar-exhibicion-contrato-civ-1257`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-medidas-cautelares-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Medidas cautelares y diligencias preliminares) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] DENOMINACIÓN SOCIAL (4 veces)
- [ ] FECHA (4 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] NOMBRE DE LA PARTE (4 veces)
- [ ] ASEGURADORA (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] LUGAR
- [ ] MARCA/MODELO
- [ ] MATRÍCULA
- [ ] Nº DE CARRETERA
- [ ] Nº DE DOCUMENTO
- [ ] PUNTO KILOMÉTRICO
- [ ] SEDE

## Normas que cita el formulario

- art. 256.1.5.º LEC
- art. 43 LCS
- art. 1.903 CC
- art. 76 LCS
- art. 256.2 LEC
- art. 258.1 LEC
- art. 258 LEC
- art. 261.2.ª LEC

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

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, que actúa en nombre y representación de Seguros [ASEGURADORA], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], y bajo la dirección letrada de D./Dña. [NOMBRE Y APELLIDOS], abogado en ejercicio del Iltre. Colegio de [LOCALIDAD], con despacho abierto en [LOCALIDAD]; ante el Tribunal comparezco y como mejor proceda en Derecho, DIGO:

Que en la representación que ostento y al amparo del artículo 256.1.5.º LEC, vengo a solicitar DILIGENCIA PRELIMINAR de juicio declarativo, de exhibición de contrato de seguro de responsabilidad civil frente a la mercantil [DENOMINACIÓN SOCIAL], con domicilio en [LOCALIDAD], y frente a la Compañía Anónima de Seguros [ASEGURADORA], con domicilio en [LOCALIDAD], en base a las siguientes:

ALEGACIONES

PRIMERA.- Mi mandante es la compañía de seguros que cubría el día [FECHA], las responsabilidades derivadas de la conducción del vehículo marca [MARCA/MODELO], matrícula [MATRÍCULA], que guiaba su titular y tomador de la póliza n.º [NÚMERO], D./Dña. [NOMBRE Y APELLIDOS], por la carretera comarcal [Nº DE CARRETERA], cuando en el p.k [PUNTO KILOMÉTRICO], padeció aquél un accidente del que resultó con lesiones, así como con importantes daños materiales en el vehículo, por razón de la precipitación de un poste de la catenaria de la vía de ferrocarril que surca paralelo a la carretera, debido al golpe que le propinó en el instante en que pasaba por el lugar, circulando correctamente, la pala de la retroexcavadora que trabajaba en las obras de ampliación del corredor de

Adjunto copias de la póliza de seguro n.º [NÚMERO], y del atestado policial n.º [NÚMERO], elaborado al efecto, en el que consta todo el pormenor del asunto.

SEGUNDA.- El conductor de la retroexcavadora, D./Dña. [NOMBRE Y APELLIDOS], prestaba servicios laborales para la empresa [DENOMINACIÓN SOCIAL], quien era la propietaria de tal vehículo, y conforme a las manifestaciones obtenidas en el mentado atestado, tal empresa tiene concertado seguro de responsabilidad civil patronal con la Compañía de Seguros frente a la que se formula solicitud de diligencias preparatorias.

TERCERA.- Mi representada, ha satisfecho a su asegurado D./Dña. [NOMBRE Y APELLIDOS] la integridad de la indemnización pertinente por lesiones y daños, habiendo éste suscrito el oportuno recibo de finiquito, con lo que, en virtud del art. 43 LCS y los pactos contractuales, la aseguradora se subroga en el derecho del perjudicado, por lo que, a través de la abogado que le asiste, envió por correo certificado con acuse de recibo, en fecha [FECHA], carta a la empresa [DENOMINACIÓN SOCIAL], en que se pedía información sobre el aseguramiento de la responsabilidad civil por hechos de sus empleados, y respuesta a la reclamación de reembolso de la reparación abonada a D./Dña. [NOMBRE Y APELLIDOS], sin que se haya recibido noticia alguna hasta el momento.

Se acompaña el consignado recibo de finiquito y la carta a que se hace referencia.

CUARTA.- Mi mandante se verá en la necesidad de instar la acción que le corresponde para exigir la responsabilidad civil por actos de terceros, conforme al art. 1.903 CCiv respecto de [NOMBRE DE LA PARTE], y por el contrato de seguro con base a la acción directa del art. 76 LCS respecto de la compañía aseguradora de dicha responsabilidad civil.

QUINTA.- Circunstanciada la referencia al asunto objeto del juicio que se quiere preparar, conforme previene el art. 256.2 LEC, constando el interés legítimo, activo, por ser subrogado en el perjuicio mi mandante, y pasivo, por ser los interesados el responsable civil y su supuesto asegurador, se justifica la adecuación y justa causa, en términos del art. 258.1 LEC, en la medida que mi patrocinada precisa conocer la veracidad de la cobertura de seguro con la compañía que se le dice, la vigencia en el momento del siniestro, la inclusión del riesgo, así como la eventual limitación de capital asegurado, todo lo cual no ha conseguido sin recurso a esta tutela jurisdiccional.

Siendo la responsabilidad solidaria, y no especificando la norma habilitante más que la legitimación pasiva de quien tiene en poder el contrato de seguro, como debieran ser poseedores tanto el tomador como la compañía aseguradora, se interpela conjuntamente a ambos sujetos, a fin de evitar inútiles dilaciones.

SEXTA.- Es competente el Tribunal al que me dirijo, a tenor del art. 257.1 párrafo 1.º LEC, por ser el del lugar del domicilio de [NOMBRE DE LA PARTE], indistinto sujeto pasivo, debiéndose dar curso al procedimiento de los arts. 258 a 260 LEC.

SÉPTIMA.- Con arreglo al art. 261.2.ª LEC, si ninguno de los interesados comparece al requerimiento, y tampoco se opone, corresponderá acordar la entrada y registro en el domicilio social [NOMBRE DE LA PARTE], y subsidiariamente en el de la Compañía de Seguros, para ocupar la póliza original de seguro.

OCTAVA.- Se ofrece caución en forma de aval de sociedad de garantía recíproca indefinido exigible a primer requerimiento para atender a los gastos de las diligencias y posibles daños y perjuicios irrogables, que fijará el Tribunal.

Por lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito, se sirva admitirlo, teniéndome por comparecido y parte en nombre de quien comparezco, mande se entiendan conmigo los sucesivos trámites, admita a trámite la DILIGENCIA PRELIMINAR que solicito, y acuerde citar y requerir a los representantes legales de [DENOMINACIÓN SOCIAL] y de la Compañía Anónima de Seguros [ASEGURADORA], para que presenten en la sede del Tribunal el contrato de seguro de responsabilidad civil por actos de los dependientes de [NOMBRE DE LA PARTE] con vigencia el día [FECHA], bajo apercibimiento de que en el caso de negarse sin justa causa, se ordenará judicialmente la entrada y registro en los respectivos domicilios sociales para ocupar dicho documento.

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a

========================================================================
