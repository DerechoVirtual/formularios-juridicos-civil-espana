---
name: escrito-oposicion-modificacion-medida-cautelar-civ-1223
description: "Escrito de oposición a la modificación de una medida cautelar. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito de oposición a la modificación de una medida cautelar

> Formulario **CIV-1223** del plugin **Medidas cautelares y diligencias preliminares** (`formularios-medidas-cautelares-civiles`) · Civil › Medidas cautelares y diligencias preliminares · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito de oposición a la modificación de una medida cautelar» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito de oposición a la modificación de una medida cautelar” para mi caso». También puedes invocarla directamente con `/formularios-medidas-cautelares-civiles:escrito-oposicion-modificacion-medida-cautelar-civ-1223`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-medidas-cautelares-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Medidas cautelares y diligencias preliminares) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (2 veces)
- [ ] FINCA (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] TIPO DE MEDIDA CAUTELAR (2 veces)
- [ ] AÑO
- [ ] DÍA
- [ ] ENTIDAD BANCARIA
- [ ] LUGAR
- [ ] MES
- [ ] NOMBRE DE LA PARTE
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] NOMBRE Y APELLIDOS
- [ ] Nº
- [ ] Nº REGISTRAL
- [ ] SEDE

## Normas que cita el formulario

- art. 743 LEC
- art. 723 LEC

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

- Junto a «…ES NÚMERO A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
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

PROCESO NÚMERO

MEDIDAS CAUTELARES NÚMERO

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

D. [NOMBRE Y APELLIDOS] Procurador de los Tribunales, en nombre y representación de [NOMBRE DEL REPRESENTADO/A] parte [ELEGIR: demandante / demandada] en el procedimiento arriba referenciado, según tengo acreditado en autos, ante el Tribunal comparezco y como mejor proceda en Derecho DIGO:

Que dentro del plazo concedido a esta parte formulo OPOSICIÓN A LA MODIFICACIÓN DE LA MEDIDA CAUTELAR de [TIPO DE MEDIDA CAUTELAR] interesada de contrario, en base a los siguientes:

HECHOS

La modificación de la medida cautelar de [TIPO DE MEDIDA CAUTELAR] decretada por el Tribunal al que me dirijo por auto de fecha [FECHA] no se ajusta al régimen procesal establecido en los artículos 730 y siguientes de la Ley de Enjuiciamiento Civil en relación al momento de solicitar las medidas cautelares que establece la regla general de que se deberán solicitar conjuntamente con la demanda principal, pudiendo también solicitarse antes de la presentación de la demanda, si bien de forma excepcional se permite que puedan solicitarse las medidas cautelares en un momento posterior del proceso, pero siempre que se basen en hechos y circunstancias que justifiquen la solicitud en dicho momento, conforme a lo dispuesto en el art. 743 de la LEC.

Del escrito presentado por la contraparte se deduce que los hechos y circunstancias alegados ya existían con anterioridad a decretarse la medida, puesto que se pretende el alzamiento del embargo sobre la finca [FINCA] y la traba de la finca [FINCA], invocando una escritura de préstamo hipotecario de fecha [FECHA] que era conocida por el solicitante al tiempo de decretarse la medida, por lo que no ha tenido lugar ninguna variación o modificación de hechos y circunstancias, y los extremos esgrimidos eran conocidos y pudieron ser alegados en la anterior vista que dio lugar a la adopción de la medida.

Por tanto, no se cumplen los requisitos establecidos en el artículo 743 de la Ley de Enjuiciamiento Civil es tajante al prescribir que las medidas cautelares podrán ser modificadas alegando y probando hechos y circunstancias que no pudieron tenerse en cuenta al tiempo de su concesión o dentro del plazo para oponerse a ellas, por lo que no se cumplen en este caso los requisitos de la norma de aplicación.

Además de no cumplirse los requisitos del art. 743 la LEC, la medida solicitada no se ajusta a los requisitos establecidos en el art. 726 y 727 del mismo texto legal, puesto que se trata de una medida más gravosa que no tiene mayor eficacia que la ya decretada, puesto que la extensión del embargo que se pretende con relación a la finca registral nº [Nº REGISTRAL]., tiene como única justificación la escritura de préstamo hipotecario antes mencionada, pero que en ningún caso supone la insuficiencia del valor del inmueble para hacer frente al pago de la deuda reclamada, mayormente cuando queda pendiente a fecha de hoy la cantidad de [IMPORTE] euros por principal y [IMPORTE] euros por intereses, según se acredita por la certificación de la entidad bancaria [ENTIDAD BANCARIA] que se acompaña como documento número 1.

A los anteriores hechos le son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

Competencia, procedimiento y legitimación

Artículo 743 en relación con los artículos 723 y 734 de la LEC.

Oposición a la modificación

Artículos 726, 728 y 743 de la LEC.

Costas

Artículos 394 y 736 LEC.

Por lo expuesto,

SUPLICO AL TRIBUNAL: Tenga por presentado este escrito, documentos y copias, se sirva admitirlos y unirlos a autos, teniendo por formulada, en tiempo y forma, oposición a la modificación de medidas cautelares instada de contrario y, previa su sustanciación tras la práctica de la prueba que desde este momento se solicita, se desestime la medida cautelar solicitada por la parte [NOMBRE DE LA PARTE], condenando en costas al solicitante.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma Abogado y Procurador

========================================================================
