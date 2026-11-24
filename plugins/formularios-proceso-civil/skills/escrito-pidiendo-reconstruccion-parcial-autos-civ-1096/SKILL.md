---
name: escrito-pidiendo-reconstruccion-parcial-autos-civ-1096
description: "Escrito pidiendo la reconstrucción parcial de autos. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito pidiendo la reconstrucción parcial de autos

> Formulario **CIV-1096** del plugin **Proceso civil: demandas, contestaciones, prueba y vista** (`formularios-proceso-civil`) · Civil › Escritos procesales (demanda, contestación, prueba, vista) · normativa revisada el 24-11-2026.

## Qué es

Escrito de parte que señala la mutilación de unos autos e insta procedimiento de reconstrucción parcial de los mismos, conforme a los arts. 232 a 235 de la LEC.

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito pidiendo la reconstrucción parcial de autos» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito pidiendo la reconstrucción parcial de autos” para mi caso». También puedes invocarla directamente con `/formularios-proceso-civil:escrito-pidiendo-reconstruccion-parcial-autos-civ-1096`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-proceso-civil:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Proceso civil: demandas, contestaciones, prueba y vista) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (6 veces)
- [ ] AÑO (2 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] ACTO O RESOLUCIÓN
- [ ] LUGAR
- [ ] Nº
- [ ] Nº DE PROCEDIMIENTO
- [ ] NÚMERO
- [ ] SEDE

## Normas que cita el formulario

- art. 232 LEC
- art. 233 LEC
- art. 328 LEC

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

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, que actúa en nombre y representación del demandante D./Dña. [NOMBRE Y APELLIDOS], en autos de Juicio Ordinario nº [Nº DE PROCEDIMIENTO]/[AÑO], promovidos contra [ACTO O RESOLUCIÓN], comparezco y como mejor en Derecho proceda, DIGO:

Que por medio del presente escrito vengo a instar procedimiento de reconstrucción parcial de los presentes autos, conforme arts. 232 a 235 LEC, en base a las siguientes:

ALEGACIONES

PRIMERA

Que el pasado día [FECHA] esta parte recibió notificación de diligencia de ordenación por la que se convocaba a los litigantes a la audiencia previa del juicio, y su Procuradora suscrita se interesó por la documentación de la pieza separada de prueba anticipada nº [NÚMERO]/[AÑO], que se practicó antes de la interposición de la demanda, siendo informada de que no se localizaba, y transcurridos los días, se llega a la conclusión de que, quedando rastro informático por la asignación de número de identificación en el Tribunal Decano con fecha [FECHA], ha desaparecido del Tribunal a que me dirijo, junto con la pérdida completa de otros expediente, lo cual está siendo investigado, y es la precisión posible que se puede tener —en términos del art. 233 LEC— de cuando ocurrió la desaparición de la pieza separada que deja mutilado este juicio ordinario.

SEGUNDA

La pretensión de esta parte es la reclamación de comisiones devengadas con arreglo al contrato de agencia que vincula a las partes, y dado que han existido unos pagos anticipados a cuenta de las mismas y una resolución contractual ulterior por la demandada, es menester conocer los datos de cartera con los movimientos de los asegurados que suscribieron póliza por intermediación del actor desde el [FECHA] hasta el [FECHA], lo que se conseguía con el requerimiento de documental contable a [DENOMINACIÓN SOCIAL], con arreglo a los arts. 328 y 329 LEC, de manera que debe procederse a la reconstrucción de pieza separada de los autos extraviada, hallándose las actuaciones de prueba anticipada de requerimiento de documental a la parte contraria concluidas.

TERCERA

A los efectos de que pueda realizarse la reconstrucción de actuaciones, esta parte se encuentra en disposición de acompañar copia del escrito de solicitud de prueba anticipada, diligencia de ordenación de fecha [FECHA] que admite la anticipación probatoria, y cita y requiere a [DENOMINACIÓN SOCIAL], para que en plazo de [Nº] días comparezca aportando la documentación interesada, así como diligencia de ordenación que tiene por contestado el requerimiento en tiempo y forma, que dio traslado a esta parte para que alegara lo conveniente, junto con la copia del escrito —cinco folios— y el listado informático de la cuenta del agente actor —veintitrés folios—, siendo ésta la última actuación que obraba en la pieza separada perdida.

Por lo expuesto,

SUPLICO AL TRIBUNAL

que por presentado este escrito con los documentos que lo acompañan, y el recibo acreditativo de haber trasladado copia de todo ello al representante procesal de la contraparte, se digne admitirlo, tener por solicitado trámite de reconstrucción de las actuaciones de pieza separada de prueba anticipada de este juicio ordinario, concedido el preceptivo traslado al Ministerio Fiscal, y previa la celebración de la vista que marca la ley, acuerde dar por reconstituidas las actuaciones teniendo por causada la prueba documental de la demandada que se aporta.

Es justicia de hacerse en [LUGAR], a [FECHA].

Firma del Abogado	Firma del Procurador/a

========================================================================
