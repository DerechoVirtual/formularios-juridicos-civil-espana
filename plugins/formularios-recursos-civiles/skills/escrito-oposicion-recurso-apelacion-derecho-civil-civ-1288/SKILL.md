---
name: escrito-oposicion-recurso-apelacion-derecho-civil-civ-1288
description: "Escrito de oposición al recurso de apelación (Derecho civil catalán). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito de oposición al recurso de apelación (Derecho civil catalán)

> Formulario **CIV-1288** del plugin **Recursos civiles: reposición, apelación, casación y queja** (`formularios-recursos-civiles`) · Civil › Recursos · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito de oposición al recurso de apelación (Derecho civil catalán)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito de oposición al recurso de apelación (Derecho civil catalán)” para mi caso». También puedes invocarla directamente con `/formularios-recursos-civiles:escrito-oposicion-recurso-apelacion-derecho-civil-civ-1288`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-recursos-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Recursos civiles: reposición, apelación, casación y queja) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (3 veces)
- [ ] FECHA (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] AÑO
- [ ] DÍA
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] MES
- [ ] Nº
- [ ] NÚMERO
- [ ] SEDE

## Normas que cita el formulario

- art. 461 LEC
- art. 233 Código Civil

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

Proceso matrimonial

A LA AUDIENCIA PROVINCIAL DE [LOCALIDAD]

D. [NOMBRE Y APELLIDOS], Procurador de los Tribunales, en nombre y representación de D. [NOMBRE Y APELLIDOS], parte demandada en este proceso seguido con el número [NÚMERO], según tengo acreditado en autos, ante la Sala comparezco y como mejor proceda en derecho DIGO:

Que esta representación ha sido emplazada en fecha [FECHA] para oposición e impugnación del recurso de apelación interpuesto de contrario, por lo que, de conformidad a lo dispuesto en el art. 461 de la LEC, mediante el presente escrito me opongo al recurso en base a los siguientes

MOTIVOS:

Nos oponemos al correlativo alegado por la parte apelante, que versa sobre el error en la valoración de la prueba en la sentencia recurrida.

Esta parte comparte plenamente las conclusiones fácticas, y sobre todo las consideraciones jurídicas, que se exponen a lo largo de la sentencia apelada a los fines de sustentar su fallo estimatorio de los pedimentos deducidos en nuestra demanda, sin que queden desvirtuadas por las alegaciones vertidas de contrario en el escrito de interposición del recurso. Las amplias y sobre todo acertadas consideraciones que se exponen en la sentencia objeto de recurso dispensan a esta parte de mayor argumentación, si bien debemos subrayar sobre todo que el Juez ha tomado en consideración a la hora de fijar la pensión alimenticia los ingresos de la otra parte derivados de los signos externos de riqueza que se desprenden de la prueba practicada, de los cuales se deduce lógicamente que los ingresos de la contraparte son muy superiores a los que reflejan sus declaraciones tributarias, puesto que es poseedor de dos vehículos de alta gama valorados en [IMPORTE] euros, así como de dos inmuebles, uno de ellos adquirido después de la ruptura matrimonial por importe de [IMPORTE] euros, todo lo cual resulta totalmente acreditado por las pruebas documentales aportadas por esta parte que obran en folios [Nº] de las actuaciones, así como por la prueba de interrogatorio de la contraparte donde ha reconocido la titularidad y adquisición de todos estos bienes, lo cual pone de manifiesto un nivel de ingresos muy elevado, tal como se concluye en la sentencia de instancia.

No existe infracción del artículo 233-4 del Código Civil catalán, puesto que la fijación de la pensión alimenticia a favor de los hijos menores se ha fijado tomando en consideración todas las circunstancias concurrentes, siendo de destacar que los gastos por alimentos han de cubrir tanto las necesidades ordinarias de los hijos como las extraordinarias, según previsión expresa del artículo 233-2 del citado Código Civil de Cataluña, englobándose en el concepto de alimentos, además de la manutención propiamente dicha y según constante doctrina jurisprudencial, gastos como los de vestido, educación, sanidad, habitación, vacaciones u ocio, resultando que la cantidad mensual establecida de [IMPORTE] euros se ajusta al nivel de ingresos de la contraparte y a las necesidades de los hijos.

Por tanto, interesamos la desestimación del recurso de apelación, y de conformidad con lo dispuesto en los artículos 394 y 398 de la Ley de Enjuiciamiento Civil, que se impongan las costas de esta alzada a la parte recurrente al ser preceptivas.

En base a lo anterior,

SUPLICO A LA SALA que tenga por presentado este escrito con justificante de traslado a las demás partes, teniéndome por opuesto al recurso de apelación frente a la sentencia dictada por la Sección Civil del Tribunal de Instancia de [SEDE] en las presentes actuaciones de fecha [FECHA] y tras la pertinente tramitación, se desestime el recurso de apelación interpuesto, con imposición a la parte apelante de las costas ocasionadas en esta alzada.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma Procurador y Abogado

========================================================================
