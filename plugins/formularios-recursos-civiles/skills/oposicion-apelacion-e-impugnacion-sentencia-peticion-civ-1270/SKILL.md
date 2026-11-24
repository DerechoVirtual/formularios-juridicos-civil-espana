---
name: oposicion-apelacion-e-impugnacion-sentencia-peticion-civ-1270
description: "Oposición a la apelación e impugnación de la sentencia con petición de prueba en segunda instancia. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Oposición a la apelación e impugnación de la sentencia con petición de prueba en segunda instancia

> Formulario **CIV-1270** del plugin **Recursos civiles: reposición, apelación, casación y queja** (`formularios-recursos-civiles`) · Civil › Recursos · normativa revisada el 24-11-2026.

## Qué es

Escrito dirigido a la Audiencia Provincial por la parte apelada (actora en primera instancia) para oponerse al recurso de apelación interpuesto por la parte demandada e impugnar la sentencia apelada en lo que le resulte desfavorable, con solicitud de práctica de prueba en la segunda instancia.

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Oposición a la apelación e impugnación de la sentencia con petición de prueba en segunda instancia» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Oposición a la apelación e impugnación de la sentencia con petición de prueba en segunda instancia” para mi caso». También puedes invocarla directamente con `/formularios-recursos-civiles:oposicion-apelacion-e-impugnacion-sentencia-peticion-civ-1270`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-recursos-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Recursos civiles: reposición, apelación, casación y queja) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL APELANTE (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR (2 veces)
- [ ] CLASE DE JUICIO
- [ ] DETALLAR EL OBJETO DE LA PETICIÓN
- [ ] DETALLAR, EN SU CASO
- [ ] INDICAR LOS MEDIOS DE PRUEBA QUE VAN A SER UTILIZADOS
- [ ] LOCALIDAD
- [ ] MOTIVOS DE INADMISIBILIDAD
- [ ] NOMBRE Y APELLIDOS DEL APELADO
- [ ] NOMBRE Y APELLIDOS DEL LETRADO
- [ ] Nº
- [ ] Nº DE COLEGIADO
- [ ] Nº DE PROCEDIMIENTO
- [ ] PROVINCIA
- [ ] RESTO DE MOTIVOS DE OPOSICIÓN, NUMERADOS: SEGUNDO, TERCERO…

## Normas que cita el formulario

- art. 461.1 LEC
- art. 458.4 LEC
- art. 461.3 LEC
- art. 394.1 LEC
- art. 276 LEC

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

A LA SALA DE LA AUDIENCIA PROVINCIAL DE [PROVINCIA], SECCIÓN [Nº]

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR], Procurador/a de los Tribunales, actuando en nombre de [NOMBRE Y APELLIDOS DEL APELADO], cuya representación tengo acreditada en los autos de juicio [CLASE DE JUICIO] n.º [Nº DE PROCEDIMIENTO], seguido contra [NOMBRE Y APELLIDOS DEL APELANTE], ante el Tribunal comparezco y, como mejor proceda en Derecho,

DIGO:

Que, dentro del plazo legal conferido al efecto por el Tribunal a esta parte mediante diligencia de ordenación de fecha [FECHA], formalizo escrito de oposición al recurso de apelación, así como de impugnación de la resolución apelada, con base en las siguientes

ALEGACIONES

PRESUPUESTO PROCESAL

Siendo por quien comparezco parte actora en el proceso, se reúnen los presupuestos subjetivos y objetivos para presentar ante el Tribunal el escrito de oposición al recurso de apelación interpuesto por la parte demandada [NOMBRE Y APELLIDOS DEL APELANTE], junto con la impugnación de la propia sentencia, ya que esta parte está debidamente comparecida, hallándose legitimada con arreglo al art. 461.1 LEC.

[OPCIONAL — incluir si procede]

INADMISIBILIDAD DEL RECURSO DE APELACIÓN

Aunque el Letrado de la Administración de Justicia tuvo por interpuesto el recurso de apelación al que por medio del presente escrito se muestra oposición, de conformidad con el art. 458.4 LEC, se alega la inadmisibilidad de la apelación para ante la Audiencia Provincial, por [MOTIVOS DE INADMISIBILIDAD].

OPOSICIÓN AL RECURSO DE APELACIÓN

PRIMERO.- OPOSICIÓN A LA APORTACIÓN DOCUMENTAL DEL APELANTE

De conformidad con el art. 461.3 LEC, siendo el momento de alegar acerca de la admisibilidad de los documentos aportados y de las pruebas propuestas por la contraparte, debe destacarse que [DETALLAR EL OBJETO DE LA PETICIÓN].

[RESTO DE MOTIVOS DE OPOSICIÓN, NUMERADOS: SEGUNDO, TERCERO…]

IMPUGNACIÓN DE LA SENTENCIA APELADA

[DETALLAR EL OBJETO DE LA IMPUGNACIÓN Y LOS PRONUNCIAMIENTOS DE LA SENTENCIA QUE SE IMPUGNAN].

COSTAS PROCESALES

Como debe inadmitirse el recurso, lo cual equivale a la desestimación, o, en todo caso, habrá de desestimarse, las costas serán impuestas al recurrente inicial, según establece el art. 394.1 LEC, al que se remite el art. 398.1.

En virtud de cuanto antecede,

SUPLICO A LA SALA, que, teniendo por presentado este escrito en tiempo y forma, que se ha trasladado en términos del art. 276 LEC al Procurador de la parte recurrente, se sirva admitirlo y tener por deducida OPOSICIÓN al recurso de apelación interpuesto, e IMPUGNACIÓN de la sentencia apelada, y previo traslado de esta última a la apelante inicial, a fin de que tenga ocasión de manifestar lo que a su derecho convenga en plazo legal,

SUPLICO A LA AUDIENCIA PROVINCIAL que dicte auto que inadmita el recurso de apelación inicial o, para el caso de que se admita, dicte sentencia que lo desestime en su integridad, o, subsidiariamente, [DETALLAR, EN SU CASO], todo ello con imposición de las costas al recurrente.

Por ser de justicia que pido en [LOCALIDAD], a [FECHA].

Firma del Abogado/a: [NOMBRE Y APELLIDOS DEL LETRADO] — Col. n.º [Nº DE COLEGIADO]

Firma del Procurador/a: [NOMBRE Y APELLIDOS DEL PROCURADOR]

OTROSÍ DIGO que interesa al derecho de esta parte valerse, para esta segunda instancia, de la práctica del siguiente medio de PRUEBA: [INDICAR LOS MEDIOS DE PRUEBA QUE VAN A SER UTILIZADOS].

SUPLICO A LA AUDIENCIA PROVINCIAL que, teniendo por causada la antecedente manifestación a los efectos oportunos, se digne resolver accediendo al acto de prueba solicitado, señalando vista para su práctica, como es procedente en justicia, que reitero en lugar y fecha ut supra.
