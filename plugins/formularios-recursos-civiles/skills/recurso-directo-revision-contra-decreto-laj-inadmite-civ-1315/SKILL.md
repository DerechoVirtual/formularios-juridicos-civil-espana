---
name: recurso-directo-revision-contra-decreto-laj-inadmite-civ-1315
description: "Recurso directo de revisión contra el decreto del LAJ que inadmite un recurso de reposición. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Recurso directo de revisión contra el decreto del LAJ que inadmite un recurso de reposición

> Formulario **CIV-1315** del plugin **Recursos civiles: reposición, apelación, casación y queja** (`formularios-recursos-civiles`) · Civil › Recursos · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **recursos**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Recurso directo de revisión contra el decreto del LAJ que inadmite un recurso de reposición» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Recurso directo de revisión contra el decreto del LAJ que inadmite un recurso de reposición” para mi caso». También puedes invocarla directamente con `/formularios-recursos-civiles:recurso-directo-revision-contra-decreto-laj-inadmite-civ-1315`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-recursos-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Recursos civiles: reposición, apelación, casación y queja) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (6 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] ACTO O RESOLUCIÓN
- [ ] FUNDAMENTOS
- [ ] LUGAR
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] Nº
- [ ] Nº DE PROCEDIMIENTO
- [ ] SEDE

## Normas que cita el formulario

- art. 454.b LEC
- art. 135.1 LEC
- art. 452.1 LEC
- art. 454 bis.1 LEC

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

### Avisos de actualización (2) — se aplican en el texto, nunca se copian en el documento

- Junto a «…so número A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

Proceso número

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

D. [NOMBRE Y APELLIDOS], Procurador de los Tribunales y de [NOMBRE DEL REPRESENTADO/A], según tengo acreditado en los autos de proceso civil [Nº DE PROCEDIMIENTO] arriba referenciados, ante el Tribunal comparezco y como mejor proceda en derecho DIGO:

Que habiendo sido notificado a esta representación el decreto de fecha [FECHA], dictado por el Letrado de la Administración de Justicia del órgano al que me dirijo, por el que se inadmite el recurso de reposición contra [ACTO O RESOLUCIÓN] de fecha [FECHA], mediante el presente escrito, al amparo del art. 452.2 y art. 454.bis de la LEC, interpongo recurso directo de revisión de la mencionada resolución citando como infringido el mismo artículo 452 de la Ley de Enjuiciamiento Civil en base a los siguientes motivos:

Motivos

[OPCIONAL — incluir si procede]

La inadmisión se funda en el incumplimiento del plazo para recurrir, estimando que se infringe el art. 452 en relación con el art. 135.1 de la LEC por cuanto que la resolución recurrida fue notificada el día [FECHA] y el recurso de reposición se presentó el día [FECHA], no habiendo transcurrido el plazo de cinco días establecido en el art. 452.1 de la LEC.

Por tanto, se solicita que se revoque la resolución, acordando en su lugar la admisión del recurso.

[OPCIONAL — incluir si procede]

La inadmisión se funda en que no se ha citado el precepto infringido en el escrito de recurso, cuestión ésta sobre la que se ha pronunciado reiteradamente la jurisprudencia en relación al recurso de reposición contra providencias y autos, donde se entendía que es un requisito que tan solo es necesario en los casos en que efectivamente se infrinja un precepto legal, pero no así como se impugna por motivos fondo, añadiendo que era suficiente la cita de un precepto constitucional.

Así, la jurisprudencia ya vino indicando que la reposición podía interponerse por motivos de forma o de fondo, de manera que en el caso de que se impugnara por motivos de fondo era inútil citar el precepto procesal, entendiéndose que no había obligación de citar normas procesales que no habían sido vulneradas (S.T.C. 162/1990, de 22 de octubre; y que la cita de un precepto constitucional, como es el art. 24 CE referido a la tutela efectiva, es suficiente para fundamentar cualquier recurso en cuanto se alega indefensión (ATS 10 abril 2003).

De acuerdo a ello, se solicita que se revoque la resolución, acordando en su lugar la admisión del recurso

[OPCIONAL — incluir si procede]

El decreto de inadmisión impugnado infringe lo dispuesto en el art. de la Ley de Enjuiciamiento Civil por cuanto [FUNDAMENTOS]

La resolución es susceptible de recurso de revisión, de acuerdo a lo establecido en la doctrina constitucional expresada en la STC 15/2020, de 28 de enero, en la cual se afirma que las resoluciones dictadas por los Letrados de la Administración de Justicia han de ser objeto de control judicial, lo que determinó la declaración de inconstitucionalidad y nulidad del artículo 454 bis.1, párrafo primero, de la LECiv, por lo que debe entrarse a conocer del fondo del recurso de revisión planteado.

En consecuencia, se solicita también por este motivo revocar el Decreto impugnado y en su lugar acordar la admisión del recurso de reposición interpuesto por esta parte.

En su virtud,

SUPLICO AL TRIBUNAL que teniendo por presentado este escrito, con justificante de traslado, se sirva admitirlo, tener por interpuesto recurso directo de revisión contra el decreto dictado por el Letrado de la Administración de Justicia de ese órgano de fecha [FECHA] y, tras los trámites legales, se dicte por el Tribunal auto por el que se revoque y deje sin efecto el Decreto impugnado, ordenando en su lugar la admisión del recurso de reposición interpuesto por esta parte.

[OPCIONAL — incluir si procede]

OTROSÍ DIGO que, de conformidad con lo dispuesto en los apartados 4 y 6 de la disposición adicional decimoquinta de la LOPJ acompaño a este escrito resguardo de consignación en la cuenta de Depósitos y Consignaciones abierta a nombre del Tribunal del depósito exigido para interponer el recurso por importe de 25 euros.

Por lo que SUPLICO AL TRIBUNAL que tenga por constituido el depósito, dejando interesada desde este momento su devolución para el caso de estimación total o parcial del recurso.

En [LUGAR], a [FECHA].

Procurador/a	Abogado/a

Fdo. D. Dña. [NOMBRE Y APELLIDOS]: Fdo. D. Dña. [NOMBRE Y APELLIDOS]:

========================================================================
