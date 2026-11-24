---
name: alegaciones-recurrente-admision-recurso-casacion-civ-1334
description: "Alegaciones del recurrente en la admisión del recurso de casación (anterior al RDL 5 2023). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Alegaciones del recurrente en la admisión del recurso de casación (anterior al RDL 5 2023)

> Formulario **CIV-1334** del plugin **Recursos civiles: reposición, apelación, casación y queja** (`formularios-recursos-civiles`) · Civil › Recursos · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Alegaciones del recurrente en la admisión del recurso de casación (anterior al RDL 5 2023)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Alegaciones del recurrente en la admisión del recurso de casación (anterior al RDL 5 2023)” para mi caso». También puedes invocarla directamente con `/formularios-recursos-civiles:alegaciones-recurrente-admision-recurso-casacion-civ-1334`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-recursos-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Recursos civiles: reposición, apelación, casación y queja) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (4 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] Nº DE PROCEDIMIENTO (2 veces)
- [ ] CAUSA
- [ ] LOCALIDAD

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

### Avisos de actualización (0) — se aplican en el texto, nunca se copian en el documento

- Ninguno.

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

Rollo [Nº DE PROCEDIMIENTO]

A LA SALA PRIMERA DEL TRIBUNAL SUPREMO

D. [NOMBRE Y APELLIDOS], Procurador de los Tribunales, en nombre y representación de D. [NOMBRE Y APELLIDOS], parte recurrente en el recurso de casación seguido ante la Sala con el número de Rollo [Nº DE PROCEDIMIENTO], ante la Excma. Sala comparezco y como mejor proceda en derecho DIGO:

- Que en virtud del traslado conferido por providencia de fecha [FECHA] sobre la posible concurrencia de la causa de inadmisión [CAUSA] en el recurso de casación interpuesto por esta representación, mediante el presente escrito paso a formular las siguientes ALEGACIONES:

ÚNICA.-La Sala ha puesto de manifiesto la posible inexistencia de interés casacional por falta de jurisprudencia contradictoria de las Audiencias Provinciales en la aplicación del art. 16 de la Ley de Propiedad Horizontal, acogiendo el planteamiento realizado de contrario al personarse en el recurso de casación, quien había alegado que en el recurso no se había citado una segunda sentencia contradictoria del signo de la recurrida.

No obstante, debe subrayarse que esta parte ya puso de manifiesto en el escrito de interposición que la Audiencia Provincial de [LOCALIDAD] en sentencia firme de fecha [FECHA] ya había seguido la misma interpretación que la sentencia que se recurre, por lo que es obvio que se dan dos pronunciamientos de este signo, contradictorio con el de las dos sentencias citadas en nuestro escrito de preparación.

Posteriormente, al escrito de interposición del recurso acompañamos el texto de la mencionada sentencia de fecha [FECHA], designada como documento número 3 de los acompañados a nuestro escrito de interposición, siendo citada reiteradamente en el citado escrito de interposición.

Acaso el planteamiento del óbice de admisibilidad viene dado por no existir un relato fáctico específico en relación a esta sentencia, que siempre mencionamos junto con la recurrida, pero es que tal relato separado resultaba totalmente superficial e inocuo, pues fácilmente se constata que ambas sentencias son idénticas, recaídas en relación al mismo supuesto de hecho y recogiendo una interpretación totalmente coincidente del art. 16 de la Ley de Propiedad Horizontal en el fundamento tercero de ambas. En este punto, las exigencias formales establecidas en el Acuerdo del Pleno de la Sala Primera de 27 de enero de 2017 han sido cumplidas, puesto que tanto en el encabezamiento como en el desarrollo del primer motivo se cita expresamente la segunda sentencia de la misma Sección de fecha [FECHA] (punto 3.3 del apartado IV), la cual tiene contenido idéntico a la sentencia recurrida según resulta fundamentado

Por este motivo entendemos que se han cumplido manifiestamente los requisitos legalmente exigidos, por lo que solicitamos que se admita el recurso de casación interpuesto por esta representación.

En base a lo anterior,

SUPLICO A LA SALA que tenga por presentado este escrito, con certificación de traslado y, en su virtud, admita el recurso de casación interpuesto por esta representación, continuando su sustanciación.

En L. y F.

(Firma Procurador y Abogado)

========================================================================
