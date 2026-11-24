---
name: oposicion-eficacia-civil-sentencia-canonica-nulidad-civ-0333
description: "Oposición a la eficacia civil de sentencia canónica de nulidad sin petición de medidas. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Oposición a la eficacia civil de sentencia canónica de nulidad sin petición de medidas

> Formulario **CIV-0333** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Escrito de oposición a la demanda que solicita la eficacia civil de la sentencia de nulidad matrimonial dictada por el Tribunal eclesiástico, sin solicitud de medidas.

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Oposición a la eficacia civil de sentencia canónica de nulidad sin petición de medidas» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Oposición a la eficacia civil de sentencia canónica de nulidad sin petición de medidas” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:oposicion-eficacia-civil-sentencia-canonica-nulidad-civ-0333`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] FECHA (3 veces)
- [ ] NÚMERO (2 veces)
- [ ] CALLE
- [ ] LUGAR
- [ ] SEDE

## Normas que cita el formulario

- art. 778 LEC
- art. 80 CC

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] PLAZA Nº [NÚMERO]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] PLAZA Nº [NÚMERO]

D./Dña. [NOMBRE Y APELLIDOS], Procurador de los Tribunales, en la representación que ostento de D [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], calle [CALLE] nº [NÚMERO], provisto de D.N.I. núm. según acredito mediante la escritura de poder que he aceptado y acompaño, ante el Tribunal comparezco, y como mejor proceda en Derecho, DIGO:

Que por medio del presente escrito me opongo a la demanda que solicita la eficacia civil de la sentencia de nulidad matrimonial dictada por el Tribunal eclesiástico de [LOCALIDAD] en fecha [FECHA], en causa canónica promovida por Doña [NOMBRE Y APELLIDOS], con base en los siguientes hechos y fundamentos jurídicos

HECHOS

PRIMERO. – Esta parte manifiesta su conformidad con el correlativo de la demanda, en cuanto a la existencia y circunstancias del matrimonio, y la realidad de la sentencia del Tribunal de la Iglesia [LOCALIDAD], cuya efectividad se pretende.

SEGUNDO. – En el procedimiento de nulidad matrimonial que se siguió ante dicho Tribunal, mi mandante no ha mantenido postura alegatoria alguna, y lo ha ignorado totalmente, hasta comparecer después de finalizado el periodo probatorio, bajo representación del procurador Sr./a [NOMBRE Y APELLIDOS], sin que tampoco entonces haya podido exponer su postura mi principal, que no ha sido interrogado, ni tiene escrito expositivo alguno en el procedimiento que ha terminado en la sentencia de mérito.

Se acompaña como documento certificación del Letrado de la Administración de Justicia del Tribunal Eclesiástico de [LOCALIDAD], al objeto de transmitir la constancia de estos hechos.

FUNDAMENTOS DE DERECHO

I.- Muestra esta parte su conformidad con la competencia objetiva y territorial del Tribunal, asume la capacidad procesal y legitimación de la parte actora, y considera adecuado el procedimiento a seguir fijado, del trámite del art. 778 LEC.

II.- El art. 80 CCiv estipula una remisión a los requisitos para el reconocimiento de resoluciones extranjeras o ‘exequatur’, como si se tratara la resolución canónica del caso de una resolución judicial extranjera, de manera que su eficacia o reconocimiento estatal en el plano civil depende de que la resolución sea auténtica y no desajuste con el Derecho del Estado, pero además que no se haya dictado en rebeldía, como es lo que se prueba

Por todo cuanto antecede,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito, con sus copias y documentos acompañados, me tenga por comparecido y parte en la representación que ostento de D. [NOMBRE Y APELLIDOS], se admita a trámite, entendiéndose conmigo las sucesivas diligencias; y por opuesto a mi mandante a la demanda en solicitud de eficacia civil de la sentencia dictada por el Tribunal eclesiástico de [LOCALIDAD] de fecha [FECHA], en la que se declara la nulidad del matrimonio canónico de los esposos Dña. y D. [NOMBRE Y APELLIDOS], se conceda a los autos el curso señalado en la Ley, de modo que en su día, se venga a dictar auto por el que se desestime la homologación de efectos civiles, con expresa imposición de las costas a la parte actora.

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a

========================================================================
