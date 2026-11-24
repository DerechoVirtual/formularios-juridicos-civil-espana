---
name: recurso-reposicion-demandado-contra-decreto-admite-civ-1313
description: "Recurso de reposición del demandado contra el decreto que admite la demanda en juicio ordinario. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Recurso de reposición del demandado contra el decreto que admite la demanda en juicio ordinario

> Formulario **CIV-1313** del plugin **Recursos civiles: reposición, apelación, casación y queja** (`formularios-recursos-civiles`) · Civil › Recursos · normativa revisada el 24-11-2026.

## Qué es

Recurso de reposición del demandado contra el decreto del Letrado de la Administración de Justicia que admite a trámite una demanda de juicio ordinario, por incumplir un requisito de admisión (en el modelo, la falta de consignación del precio o de caución en una demanda de retracto, artículo 266.2.º de la Ley de Enjuiciamiento Civil).

Es un modelo de tipo **recursos**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Recurso de reposición del demandado contra el decreto que admite la demanda en juicio ordinario» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Recurso de reposición del demandado contra el decreto que admite la demanda en juicio ordinario” para mi caso». También puedes invocarla directamente con `/formularios-recursos-civiles:recurso-reposicion-demandado-contra-decreto-admite-civ-1313`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-recursos-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Recursos civiles: reposición, apelación, casación y queja) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (3 veces)
- [ ] SEDE (3 veces)
- [ ] ACCIÓN
- [ ] AÑO
- [ ] DENOMINACIÓN
- [ ] DÍA
- [ ] LOCALIDAD
- [ ] MES
- [ ] NOMBRE Y APELLIDOS
- [ ] NOMBRE Y APELLIDOS DEL DEMANDANTE
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR
- [ ] NOMBRE Y APELLIDOS O DENOMINACIÓN SOCIAL DEL DEMANDADO
- [ ] Nº
- [ ] Nº DE PROCEDIMIENTO

## Normas que cita el formulario

- No cita artículos concretos; Claude localizará las normas aplicables con Jurisprudenciator si el documento las necesita.

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

- Junto a «…DICIAL DE [SEDE] / AL SERVICIO COMÚN [DENOMINACIÓN] DE LOS TRIBUNALES DE [SEDE]]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

Juicio número [Nº DE PROCEDIMIENTO]

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº] [ELEGIR: / A LA OFICINA JUDICIAL DE [SEDE] / AL SERVICIO COMÚN [DENOMINACIÓN] DE LOS TRIBUNALES DE [SEDE]]

Don/Doña [NOMBRE Y APELLIDOS DEL PROCURADOR], Procurador/a de los Tribunales, actuando en representación de [NOMBRE Y APELLIDOS O DENOMINACIÓN SOCIAL DEL DEMANDADO], según se acredita mediante copia electrónica de poder notarial otorgado a mi favor que acompaño, comparezco y, como mejor proceda en Derecho, DIGO:

1) Que el pasado día [FECHA] se emplazó a mi representado/a como parte demandada en el procedimiento arriba expresado, entregándosele copia del decreto de admisión a trámite de la demanda dictado por el Letrado de la Administración de Justicia de ese órgano el día [FECHA].

2) Que, entendiendo que dicha resolución infringe el artículo 266.2.º de la Ley de Enjuiciamiento Civil en relación con el artículo 403.2 del mismo texto legal, y siendo lesiva para los intereses de mi principal, por medio del presente escrito paso a interponer recurso de reposición contra el citado decreto en base a los siguientes

MOTIVOS

PRIMERO.– El motivo del recurso, a los efectos de los artículos 451 y 452.1 de la Ley de Enjuiciamiento Civil, es que se entiende que se ha producido la vulneración del artículo 266.2.º del mismo texto legal, en relación con el artículo 403.2, ya que en la demanda objeto de los presentes autos se pretende ejercitar por el demandante una acción de retracto [ELEGIR: / u otra acción sujeta a requisito especial de admisión: [ACCIÓN]], sin que haya procedido en ningún momento a consignar el precio ni ha acreditado la constitución de caución tan pronto el precio sea conocido.

El artículo 266.2 de la Ley de Enjuiciamiento Civil exige expresamente que con las demandas de retracto se cumplan dichos requisitos de consignación del precio o, al menos, de constitución de caución, siendo que en este caso en ningún momento se han cumplido por el demandante, debiendo añadirse que el precio era claramente conocido por el actor según el mismo relato fáctico de la demanda.

Por tanto, se infringe lo dispuesto en los preceptos citados, debiendo concederse el oportuno plazo de subsanación y, en su caso, dar cuenta al Juez para inadmisión de la demanda conforme previene el artículo 404 de la Ley de Enjuiciamiento Civil.

Es por ello que, en virtud de lo anterior,

SUPLICO: que tenga por interpuesto recurso de reposición, con justificante de traslado, frente al decreto dictado por el Letrado de la Administración de Justicia de ese órgano de fecha [FECHA], en el que se acordaba la admisión a trámite de la demanda de juicio ordinario interpuesta por el Procurador Don/Doña [NOMBRE Y APELLIDOS], actuando en representación de [NOMBRE Y APELLIDOS DEL DEMANDANTE], frente a mi mandante, y, tras la pertinente tramitación, dicte decreto reponiendo el anterior y acordando en su lugar que se acredite la consignación o constitución de caución en plazo, todo ello con imposición de costas al demandante si se opusiere.

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firmas del Abogado y del Procurador
