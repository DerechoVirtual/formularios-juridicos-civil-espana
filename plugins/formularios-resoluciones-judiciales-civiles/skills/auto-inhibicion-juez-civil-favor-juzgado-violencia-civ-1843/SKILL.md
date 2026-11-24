---
name: auto-inhibicion-juez-civil-favor-juzgado-violencia-civ-1843
description: "Auto de inhibición del juez civil a favor del Juzgado de Violencia sobre la Mujer. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Auto de inhibición del juez civil a favor del Juzgado de Violencia sobre la Mujer

> Formulario **CIV-1843** del plugin **Resoluciones judiciales civiles: autos, decretos y diligencias** (`formularios-resoluciones-judiciales-civiles`) · Civil › Resoluciones judiciales (autos, decretos, providencias, diligencias) · normativa revisada el 24-11-2026.

## Qué es

Auto de inhibición de la Sección Civil del Tribunal de Instancia del conocimiento de la demanda de proceso de separación conyugal remitiendo los autos en el estado en que se hallan a la Sección de Violencia sobre la Mujer del Tribunal de Instancia, al resultar competente atendiendo a los actos de violencia de género que han dado lugar a la iniciación de un procedimiento penal u orden de protección.

Es un modelo de tipo **resoluciones judiciales (autos, decretos, providencias, diligencias)**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Auto de inhibición del juez civil a favor del Juzgado de Violencia sobre la Mujer» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Auto de inhibición del juez civil a favor del Juzgado de Violencia sobre la Mujer” para mi caso». También puedes invocarla directamente con `/formularios-resoluciones-judiciales-civiles:auto-inhibicion-juez-civil-favor-juzgado-violencia-civ-1843`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-resoluciones-judiciales-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Resoluciones judiciales civiles: autos, decretos y diligencias) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (14 veces)
- [ ] FECHA (4 veces)
- [ ] NÚMERO (4 veces)
- [ ] AÑO (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] GRUPO
- [ ] LUGAR
- [ ] Nº
- [ ] Nº DE FAX
- [ ] SEDE
- [ ] TELÉFONO

## Normas que cita el formulario

- art. 49 bis.1 LEC
- art. 1 Ley Orgánica 1/2004
- art. 89 Ley Orgánica 6/1985
- art. 87 ter.2 LOPJ
- art. 1.1 LO 1/2004
- art. 87 ter LOPJ
- art. 87 ter.3 LOPJ
- art. 48.3 LEC
- art. 49 bis.5 LEC

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

- Junto a «…ado-Juez de la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. «De los de» es residuo de los varios juzgados de una plaza. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA N.º [NÚMERO]

Tfno [TELÉFONO]

Fax [Nº DE FAX]

Separación n.º [NÚMERO]/[AÑO]

Demandante: D./Dña. [NOMBRE Y APELLIDOS]

Abogado/a [NOMBRE Y APELLIDOS] Procurador/a [NOMBRE Y APELLIDOS]

Demandado: Don [NOMBRE Y APELLIDOS]

AUTO

D./Dña. [NOMBRE Y APELLIDOS], Magistrado-Juez de la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº]

En la ciudad de [LOCALIDAD], a [FECHA]

ANTECEDENTES DE HECHO

PRIMERO.- Por la Procurador/a de los Tribunales Sr./a. [NOMBRE Y APELLIDOS], en representación de D./Dña. [NOMBRE Y APELLIDOS], se ha presentado el [FECHA], demanda de separación matrimonial a su instancia, señalando como parte demandada a Don [NOMBRE Y APELLIDOS]

SEGUNDO.- Por la parte demandante se ha presentado escrito que reclama la inhibición a la Sección de Violencia sobre la Mujer del Tribunal de Instancia con testimonio del Auto que acuerda Orden de Protección en favor de aquélla por acciones que se imputan al demandado Don [NOMBRE Y APELLIDOS], en Diligencias Urgentes n.º [NÚMERO]/[AÑO], dictado por el Servicio de Guardia de esta ciudad el [FECHA],

FUNDAMENTOS DE DERECHO

PRIMERO.- Dispone el art. 49 bis.1 LEC que, cuando un juzgado, que esté conociendo en primera instancia de un procedimiento civil, tuviese noticia de la comisión de un acto de violencia de los definidos en el artículo 1 de la Ley Orgánica 1/2004, de 28 de diciembre, de Medidas de Protección Integral contra la Violencia de Género, que haya dado lugar a la iniciación de un proceso penal o a una orden de protección, tras verificar la concurrencia de los requisitos previstos en el apartado 7 del artículo 89 de la Ley Orgánica 6/1985, de 1 de julio, del Poder Judicial, deberá inhibirse, remitiendo los autos en el estado en que se hallen al juez de violencia sobre la mujer que resulte competente, salvo que se haya iniciado materialmente la vista o comparecencia del procedimiento civil contencioso o de jurisdicción voluntaria.

SEGUNDO.- En el caso presente concurren los siguientes presupuestos:

a) Este Tribunal está conociendo en primera instancia de procedimiento civil que versa sobre materia prevista en el art. 87 ter.2 LOPJ, en concreto de su letra b), como de separación del matrimonio.
b) Este proceso no ha iniciado la fase de juicio oral, puesto que, admitida la demanda, se acaba de emplazar al demandado.
c) Se ha proporcionado al Tribunal noticia de la comisión de un acto de violencia de género de los definidos en el art. 1.1 LO 1/2004, y que delimita la competencia de la Sección de Violencia sobre la Mujer del Tribunal de Instancia, por referencia del art. 87 ter LOPJ.
d) Dicha supuesta conducta violenta ha dado lugar a la incoación de un procedimiento judicial preliminar penal en que se ha dictado Orden de Protección, según resulta del testimonio que acompaña la representación de D./Dña. [NOMBRE Y APELLIDOS] (art. 49 bis.4 párrafo 2.º LEC).
e) Concurren en este proceso los demás requisitos que previene el art. 87 ter.3 LOPJ, y precisamente la vinculación subjetiva con el procedimiento penal, de manera que la parte aquí demandante es víctima de la Orden de Protección, y el demandado Don [NOMBRE Y APELLIDOS] es el imputado por el supuesto acto de violencia, al tenor del indicado testimonio.

TERCERO.- Puesto que concurriendo los anteriores presupuestos, compete la acción civil en concreto, de forma exclusiva y excluyente, a la Sección de Violencia sobre la Mujer del Tribunal de Instancia, procede declarar la inhibición de este Tribunal civil a su favor para conocer de la demanda, con remisión de los autos al mismo, sin que sea de aplicación lo previsto en el art. 48.3 LEC, debiendo las partes desde este momento comparecer ante dicho órgano (art. 49 bis.4 párrafo 1.º LEC), ejerciendo la Sección de Violencia sobre la Mujer del Tribunal de Instancia sus competencias en la materia, en todo caso, de conformidad con los procedimientos y recursos previstos en la ley procesal civil (art. 49 bis.5 LEC).

PARTE DISPOSITIVA

1.- Se inhibe este Tribunal del conocimiento de la demanda de proceso de separación conyugal promovida por la Procuradora de los Tribunales D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS], en la que figura como parte demandada Don [NOMBRE Y APELLIDOS].

2.- Remítanse los autos en el estado en que se hallan a la Sección de Violencia sobre la Mujer del Tribunal de Instancia de esta capital, el cual resulta competente.

Notifíquese con advertencia de que contra la presente resolución cabe recurso de APELACIÓN ante la Audiencia Provincial de [LOCALIDAD], que se interpondrá por medio de escrito presentado en este Tribunal en el plazo de VEINTE DÍAS hábiles contados desde el día siguiente de la notificación, exponiendo el apelante las alegaciones en que se base la impugnación, además de citar la resolución apelada y los pronunciamientos que impugna.

Para interponer el recurso será necesario la constitución de un depósito de 50 euros, sin cuyo requisito no será admitido a trámite. El depósito se constituirá consignando dicho importe en la Cuenta de Depósitos y Consignaciones que este Tribunal tiene abierta en el grupo [GRUPO] con el número [NÚMERO], indicando en el campo concepto del resguardo de ingreso que se trata de un "Recurso" código 02-Apelación. La consignación deberá ser acreditada al interponer el recurso (disp. adic. 15.ª de la LOPJ).

No están obligados a constituir el depósito para recurrir los declarados exentos en la disposición citada y quienes tengan reconocido el derecho a la asistencia jurídica gratuita.

Lo acuerda y firma S. S.ª Ilma. Doy fe

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Juez/a	Firma del Letrado de la Administración de Justicia

========================================================================
