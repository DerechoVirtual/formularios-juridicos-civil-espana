---
name: auto-aparta-definitivamente-juez-asunto-interes-civ-1906
description: "Auto que aparta definitivamente al juez del asunto por interés indirecto. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Auto que aparta definitivamente al juez del asunto por interés indirecto

> Formulario **CIV-1906** del plugin **Resoluciones judiciales civiles: autos, decretos y diligencias** (`formularios-resoluciones-judiciales-civiles`) · Civil › Resoluciones judiciales (autos, decretos, providencias, diligencias) · normativa revisada el 24-11-2026.

## Qué es

Modelo de auto apartando definitivamente del conocimiento de los presentes autos de juicio ordinario al Juez que ha instado su abstención, al existir interés directo en el pleito. Documento adapatado a la reforma orgánica de la LO 1/2025.

Es un modelo de tipo **resoluciones judiciales (autos, decretos, providencias, diligencias)**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Auto que aparta definitivamente al juez del asunto por interés indirecto» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Auto que aparta definitivamente al juez del asunto por interés indirecto” para mi caso». También puedes invocarla directamente con `/formularios-resoluciones-judiciales-civiles:auto-aparta-definitivamente-juez-asunto-interes-civ-1906`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-resoluciones-judiciales-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Resoluciones judiciales civiles: autos, decretos y diligencias) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (4 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] LUGAR (2 veces)
- [ ] SECCIÓN (2 veces)
- [ ] SEDE (2 veces)
- [ ] ACTO O RESOLUCIÓN
- [ ] FECHA DEL AUTO
- [ ] GRUPO
- [ ] LOCALIDAD
- [ ] Nº

## Normas que cita el formulario

- art. 219 LOPJ
- art. 102.4 LEC
- art. 102 LEC
- art. 451 LEC

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

Modelo de auto apartando definitivamente del conocimiento de los presentes autos de juicio ordinario al Juez que ha instado su abstención, al existir interés directo en el pleito.

Documento adapatado a la reforma orgánica de la LO 1/2025.


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

AUTO

Ilmo. Sr./a Magistrado-Juez D:/Dña. [NOMBRE Y APELLIDOS]

En [LUGAR], a [FECHA].

Dada cuenta del anterior oficio de la Sección [SECCIÓN] de la Audiencia Provincial de [LOCALIDAD], por el que se comunica que se ha admitido la abstención del proveyente, únase a los autos de su razón, y acúsese recibo.

ANTECEDENTES DE HECHO

Primero

Con fecha [FECHA] se dictó auto decretando el proveyente la abstención para conocer del presente procedimiento, por hallarse incurso en la causa del n.º 10 del art. 219 LOPJ remitiéndose escrito razonado a la Ilma. Sra. Audiencia Provincial, que planteaba tal abstención.

Segundo

Se ha dictado el [FECHA] auto por la Sección [SECCIÓN] de la Audiencia Provincial, en que se ha estimado justificada la abstención decretada en el presente procedimiento, habiéndose participado a los efectos procedentes.

FUNDAMENTOS DE DERECHO

ÚNICO.-

Preceptúa el art. 102.4 LEC que si se estimare justificada la abstención por el tribunal competente para decidir, el abstenido dictará auto apartándose definitivamente del conocimiento del asunto y ordenando remitir las actuaciones al que deba sustituirle.

En este sentido, en las presentes actuaciones se dictó auto con fecha [FECHA DEL AUTO] en el que se acordaba la abstención para conocer de los presentes autos por concurrir la causa de interés indirecto en el pleito, habiéndose aceptado tal circunstancia por la Audiencia Provincial.

Corresponde la remisión de las actuaciones al Magistrado-Juez de la Sección Civil del Tribunal de Instancia n.º [NÚMERO], que es a quien le corresponde la sustitución de este Tribunal en base a las normas aprobadas al respecto por la Sala de Gobierno del TSJ, a propuesta de la Junta de Jueces, manteniéndose la competencia de este Tribunal, aunque con sustitución de la persona del juzgador por parte del Magistrado citado.

Por lo expuesto,

PARTE DISPOSITIVA

1.- D:/Dña. [NOMBRE Y APELLIDOS], Magistrado-Juez de la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [NÚMERO], SE APARTA definitivamente del conocimiento de los presentes autos de juicio ordinario seguidos a instancia de D:/Dña. [NOMBRE Y APELLIDOS] contra [ACTO O RESOLUCIÓN].

2.- Remítanse los autos a conocimiento del Magistrado-Juez de la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº] este partido, a quien legalmente le corresponde la sustitución.

Una vez verificado, se acordará lo procedente en cuanto al alzamiento de la suspensión acordada en su día.

3.- Comuníquese a las partes la abstención y sustitución operada, en los términos prevenidos en el n.º 5 del art. 102 LEC.

La presente resolución se notificará a las partes, con indicación de que no es firme, y que contra la misma cabe formular, en el plazo de cinco días, recurso de reposición (arts. 451 a 454 LEC) ante este Tribunal.

Para interponer el recurso será necesario la constitución de un depósito de 25 euros, sin cuyo requisito no será admitido a trámite. El depósito se constituirá consignando dicho importe en la Cuenta de Depósitos y Consignaciones que este Tribunal tiene abierta en el grupo [GRUPO] con el número [NÚMERO], indicando en el campo concepto del resguardo de ingreso que se trata de un "Recurso" código 00-Reposición. La consignación deberá ser acreditada al interponer el recurso (disp. adic. 15ª de la LOPJ).

Están exentos de constituir el depósito para recurrir los incluidos en el apartado 5 de la disposición citada y quienes tengan reconocido el derecho a la asistencia jurídica gratuita

Lo acuerdo, mando y firmo.

Es justicia de hacerse en [LUGAR], a [FECHA].

Firma del Juez/a

========================================================================
