---
name: cuestion-incidental-previo-pronunciamiento-falta-civ-0927
description: "Cuestión incidental de previo pronunciamiento por falta de capacidad del demandante. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Cuestión incidental de previo pronunciamiento por falta de capacidad del demandante

> Formulario **CIV-0927** del plugin **Proceso civil: demandas, contestaciones, prueba y vista** (`formularios-proceso-civil`) · Civil › Escritos procesales (demanda, contestación, prueba, vista) · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Cuestión incidental de previo pronunciamiento por falta de capacidad del demandante» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Cuestión incidental de previo pronunciamiento por falta de capacidad del demandante” para mi caso». También puedes invocarla directamente con `/formularios-proceso-civil:cuestion-incidental-previo-pronunciamiento-falta-civ-0927`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-proceso-civil:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Proceso civil: demandas, contestaciones, prueba y vista) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] Nº DE DOCUMENTO
- [ ] Nº DE PROCEDIMIENTO
- [ ] SEDE

## Normas que cita el formulario

- art. 391.1.º LEC
- art. 388 LEC
- art. 7 LEC
- art. 392.1 LEC

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

- Junto a «…MILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.

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

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D. [NOMBRE Y APELLIDOS], Procurador de los Tribunales, actuando en representación de [NOMBRE DEL REPRESENTADO/A], según consta acreditado en el proceso ordinario número [NÚMERO] que se sigue ante ese Tribunal, comparezco y como proceda en Derecho DIGO:

- Que al amparo de lo dispuesto en el art. 391.1.º de la LEC, y habiéndose producido un hecho que afecta a la capacidad del demandante D. [NOMBRE Y APELLIDOS], mediante el presente escrito planteo la CUESTIÓN DE PREVIO PRONUNCIAMIENTO DE FALTA DE CAPACIDAD DEL DEMANDANTE en base a los siguientes:

HECHOS

PRIMERO.- Tal como se relataba en el hecho tercero de nuestro escrito de contestación el demandante D. estaba sujeto a un proceso de adopción de medidas judiciales de apoyo a personas con discapacidad seguido en la Sección Civil del Tribunal de Instancia número [NÚMERO], autos número [Nº DE PROCEDIMIENTO], a instancias del Ministerio Fiscal.

Con posterioridad a la celebración de la audiencia previa en este juicio ordinario, el pasado día [FECHA] recayó sentencia en el referido proceso por la cual se constituía el régimen de curatela del demandante, debiendo estar representado por el curador en todos los actos que realice, siendo designado curador D………….., con facultades de representación plena. Dicha sentencia es firme, al no haber sido recurrida por ninguna de las partes (acompaño como documento número [Nº DE DOCUMENTO] testimonio de la referida sentencia de fecha [FECHA] dictada por el Tribunal número [NÚMERO], expresándose en el testimonio por el Letrado de la Administración de Justicia que dicha sentencia es firme).

A los anteriores hechos, son de aplicación los siguientes:

Fundamentos de derecho

I. En cuanto al procedimiento, los arts. 388, 390 y 393 de la LEC, debiendo sustanciarse por los trámites prevenidos en los referidos preceptos, con suspensión del curso de las actuaciones.

II. En cuanto a su procedencia, el art. 391.1.º de la LEC, en tanto que se trata de un hecho acaecido con posterioridad a la audiencia previa.

III. En cuanto al fondo, los arts. 7 y 9 de la LEC, que determinan la finalización del proceso por falta de capacidad procesal del demandante, como efecto de las medidas judiciales de apoyo decretadas por la sentencia antes mencionada y al no haber comparecido el curador, quien ostenta facultades de representación plena, para la continuación del proceso iniciado por la persona con discapacidad.

Por lo expuesto, AL TRIBUNAL SUPLICO que, con admisión de este escrito y documentos acompañados con justificante de traslado, tenga por planteado incidente de previo pronunciamiento y, previos los trámites legales con suspensión de las actuaciones, dicte auto poniendo fin al proceso por falta de capacidad del demandante, y con imposición al mismo de las costas causadas.

OTROSÍ DIGO que, de conformidad a lo establecido en el art. 392.1 de la LEC, propongo la práctica de los siguientes medios de prueba: 1. Documental pública, dando por reproducido el documento acompañado con este escrito, consistente en testimonio de la sentencia de fecha [FECHA] con expresión de su firmeza.

AL TRIBUNAL SUPLICO que admita la prueba propuesta por esta parte en relación a este incidente.

En L. y F.

(Firma Procurador y Abogado)

========================================================================
