---
name: incidente-nulidad-actuaciones-defecto-forma-civ-0868
description: "Incidente de nulidad de actuaciones por defecto de forma. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Incidente de nulidad de actuaciones por defecto de forma

> Formulario **CIV-0868** del plugin **Proceso civil: demandas, contestaciones, prueba y vista** (`formularios-proceso-civil`) · Civil › Escritos procesales (demanda, contestación, prueba, vista) · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Incidente de nulidad de actuaciones por defecto de forma» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Incidente de nulidad de actuaciones por defecto de forma” para mi caso». También puedes invocarla directamente con `/formularios-proceso-civil:incidente-nulidad-actuaciones-defecto-forma-civ-0868`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-proceso-civil:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Proceso civil: demandas, contestaciones, prueba y vista) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] OTROS DATOS (7 veces)
- [ ] MOTIVO (4 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] Nº DE ARTÍCULO (3 veces)
- [ ] FECHA (2 veces)
- [ ] Nº DE PROCEDIMIENTO (2 veces)
- [ ] AÑO
- [ ] CONDICIÓN PROCESAL
- [ ] DESCRIBIR
- [ ] DÍA
- [ ] INDEFENSIÓN CAUSADA
- [ ] LUGAR
- [ ] MES
- [ ] Nº
- [ ] Nº DE DOCUMENTO
- [ ] PLAZO
- [ ] SEDE

## Normas que cita el formulario

- art. 228.1 LEC
- art. 228 LEC
- art. 228.2 LEC

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº].»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº].

D./Dña. [NOMBRE Y APELLIDOS], Procurador de los Tribunales, en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS], según tengo debidamente acreditado en los autos de juicio [Nº DE PROCEDIMIENTO] número [Nº DE PROCEDIMIENTO], ante el Tribunal comparezco y como mejor proceda en derecho DIGO:

Que mediante el presente escrito, y en aplicación del artículo 228 de la Ley de Enjuiciamiento Civil, formulo incidente de nulidad de actuaciones de [OTROS DATOS] que determina la consiguiente nulidad de [OTROS DATOS] de fecha [FECHA], por vulneración del derecho fundamental del artículo [Nº DE ARTÍCULO] de la Constitución, con base en las siguientes alegaciones:

CONCURRENCIAS DE REQUISITOS

D./Dña. [NOMBRE Y APELLIDOS] es parte legítima en el procedimiento por ostentar en el mismo la condición de [CONDICIÓN PROCESAL], artículo 228.1 de la LEC.

Se ha vulnerado el derecho fundamental de [OTROS DATOS] porque [MOTIVO].

Se cumplen los requisitos formales exigidos por el artículo 228 de la LEC así:

— no se pudo denunciar antes de recaer esta resolución por [MOTIVO].

— se tiene que impugnar por esta vía por no caber contra la resolución afectada de nulidad recurso alguno.

Nos encontramos dentro del plazo de [PLAZO] desde que [OTROS DATOS]

ALEGACIONES

La resolución recurrida literalmente expresaba que [OTROS DATOS]

Contra esta medida no cabe recurso alguno, según establece el artículo [Nº DE ARTÍCULO].

Esta parte considera, dicho sea con los debidos respetos y en términos de defensa, que [OTROS DATOS] no resulta conforme a derecho, puesto que se vulnera el artículo [Nº DE ARTÍCULO] de la Constitución relativo a [DESCRIBIR].

Tales defectos son de tal envergadura que han causado clara indefensión a mi representado al impedirle [INDEFENSIÓN CAUSADA].

Por la naturaleza de los mismos ha sido imposible para esta parte denunciar tales defectos en un momento previo, tal como se acredita con el documento número [Nº DE DOCUMENTO].

La resolución no es susceptible de recurso ordinario alguno en el que quepa reparar la indefensión sufrida.

Es competente para conocer el presente incidente el Tribunal al que nos dirigimos por ser el que dictó la resolución cuya nulidad se pretende.

De este escrito y de los documentos que se acompañan se dará traslado a la otra parte para que manifieste lo que a su derecho convenga.

Por lo expuesto,

SUPLICO AL TRIBUNAL: Que tenga por presentado este escrito con los documentos que acompaño y copia de todo ello, lo admita y, previos los trámites legales oportunos, en su día acuerde la nulidad de [OTROS DATOS] por [MOTIVO], y la expresa imposición de las costas del incidente a la otra parte en caso de oponerse a esta pretensión.

Es justicia que pido en [LUGAR], a [DÍA] de [MES] de [AÑO].

OTROSÍ DIGO: Que según permite el artículo 228.2 de la LEC desde este momento interesamos la suspensión de la ejecución y eficacia de la resolución de fecha [FECHA] a fin de evitar que este incidente pueda perder su finalidad, ya que si llegara a ejecutarse los perjuicios serían de imposible reparación por [MOTIVO].

SUPLICO: Se acuerde conforme al precedente otrosí por ser justicia que pido en mismo lugar y fecha.

========================================================================
