---
name: solicitud-multas-coercitivas-incumplimiento-medida-civ-1515
description: "Solicitud de multas coercitivas por incumplimiento de una medida de un proceso matrimonial. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud de multas coercitivas por incumplimiento de una medida de un proceso matrimonial

> Formulario **CIV-1515** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud de multas coercitivas por incumplimiento de una medida de un proceso matrimonial» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud de multas coercitivas por incumplimiento de una medida de un proceso matrimonial” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:solicitud-multas-coercitivas-incumplimiento-medida-civ-1515`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] SEDE (2 veces)
- [ ] FECHA
- [ ] LOCALIDAD
- [ ] Nº
- [ ] NÚMERO

## Normas que cita el formulario

- art. 711 LEC

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

### Avisos de actualización (3) — se aplican en el texto, nunca se copian en el documento

- Junto a «…Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. «De los de» es residuo de los varios juzgados de una plaza. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).
- Junto a «…2666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.

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

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

Don [NOMBRE Y APELLIDOS], Procurador de los Tribunales, actuando en nombre y represtación de Doña [NOMBRE Y APELLIDOS], conforme tengo debidamente acreditado en Procedimiento de Separación Contenciosa /, promovido por mi principal contra Don [NOMBRE Y APELLIDOS], y bajo la dirección Letrada de Don [NOMBRE Y APELLIDOS], ante la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [NÚMERO] comparezco y, como mejor proceda en Derecho, DIGO:

Que en la indicada representación por medio del presente escrito formulo SOLICITUD DE IMPOSICIÓN DE MULTAS COERCITIVAS POR INCUMPLIMIENTO DE MEDIDAS por parte de Don [NOMBRE Y APELLIDOS], al amparo de lo dispuesto en el artículo 776.1 y 2 de la Ley de Enjuiciamiento Civil, y demás artículos de legal y pertinente aplicación, pasando a realizar las siguientes

ALEGACIONES

Incumplimiento de manera reiterada de las obligaciones de pago

Que el progenitor y padre del menor Don [NOMBRE Y APELLIDOS] de forma reiterada está incumpliendo la obligación impuesta en virtud de Sentencia de fecha [FECHA], en la actualidad firme, consistente en el pago mensual de - euros en concepto de pensión de alimentos para el hijo menor.

Que desde que ha adquirido firmeza la sentencia que establece la obligación al progenitor de abonar el citado importe por el concepto indicado, y pese a las gestiones de mi principal, madre del hijo en común menor de edad, su actitud ha sido de total y completa despreocupación, por no mejor decir que se obstina en no pagar por el mero hecho de perjudicar a la madre del menor.

Que en la actualidad no ha ingresado en la cuenta consignada en el Tribunal cantidad alguna, por lo que adeuda un total de cinco mensualidades, todo ello sin perjuicio de que por su actitud mucho nos tememos que no tiene intención o propósito de realizar ingreso alguno en el futuro.

Que ante el incumplimiento reiterado del progenitor de las obligaciones de pago de las cantidades que le corresponden, y sin perjuicio de hacer efectivas sobre su patrimonio las cantidades debidas y no satisfechas, es por lo que con arreglo a lo dispuesto en el artículo 776.1.ª de la Ley de Enjuiciamiento Civil se interesa que por el Letrado de la Administración de Justicia de ese órgano se acuerde la imposición de multas coercitivas, que dada la actitud del progenitor se considera más que justificado se acuerden en su importe máximo, por lo que de conformidad con los porcentajes permitidos en el artículo 711 de la LEC y respecto a lo adeudado hasta la fecha, que asciende a la cantidad de -, que se corresponde a cinco mensualidades, se imponga una multa única del 50 por 100, y respecto a las sucesivas mensualidades que se vayan devengando se impongan multas mensuales que asciendan a un 20 por 100.

Incumplimiento de obligaciones no pecuniarias de carácter personalísimo

Que el progenitor igualmente incumple el régimen de visitas establecido en sentencia, por lo que nos encontramos ante un supuesto de incumplimiento de obligaciones no pecuniarias de carácter personalísimo, por lo que con arreglo a lo dispuesto en el artículo 776.2ª, interesa que se mantengan las multas coercitivas mensuales todo el tiempo que sea necesario más allá del plazo de un año establecido en el artículo 709 de la Ley de Enjuiciamiento Civil.

Por lo que,

AL TRIBUNAL SOLICITO: Que tenga por presentado este escrito, lo admita, tenga por interpuesta y formulada SOLICITUD DE IMPOSICIÓN DE MULTAS COERCITIVAS POR INCUMPLIMIENTO DE MEDIDAS, por realizadas las alegaciones vertidas en el presente escrito, y previos los trámites con arreglo a derecho, por el Letrado de la Administración de Justicia se acuerde mediante resolución motivada imponer a Don [NOMBRE Y APELLIDOS] POR INCUMPLIMIENTO DE MANERA REITERADA DE LAS OBLIGACIONES DE PAGO una multa única del 50 por 100 respecto a lo adeudada hasta la fecha, que asciende a la cantidad de - euros, y respecto a las sucesivas mensualidades que en concepto de alimentos se vayan devengando, que en la actualidad ascienden a la cantidad de - euros, sin perjuicio de las actualizaciones en función de las variaciones que se produzcan en el índice de precios al consumo, se impongan multas mensuales que asciendan a un 20 por 100; y POR INCUMPLIMIENTO DE OBLIGACIONES NO PECUNIARIAS DE CARÁCTER PERSONALÍSIMO se acuerde el mantenimiento de las multas coercitivas mensuales todo el tiempo que sea necesario más allá del plazo de un año establecido en el artículo 709 de la Ley de Enjuiciamiento Civil, dando a los autos el impulso procesal con arreglo a derecho.

Es de Justicia que insto en [LOCALIDAD] lugar y fecha

========================================================================
