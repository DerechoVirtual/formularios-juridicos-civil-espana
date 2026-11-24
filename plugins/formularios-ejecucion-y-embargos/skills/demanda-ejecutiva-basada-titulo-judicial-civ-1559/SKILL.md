---
name: demanda-ejecutiva-basada-titulo-judicial-civ-1559
description: "Demanda ejecutiva basada en título judicial. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda ejecutiva basada en título judicial

> Formulario **CIV-1559** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda ejecutiva basada en título judicial» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda ejecutiva basada en título judicial” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:demanda-ejecutiva-basada-titulo-judicial-civ-1559`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (5 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] FECHA (2 veces)
- [ ] Nº (2 veces)
- [ ] SEDE (2 veces)
- [ ] TIPO Y Nº DE PROCEDIMIENTO (2 veces)
- [ ] ÓRGANO JUDICIAL (2 veces)
- [ ] BIENES A EMBARGAR
- [ ] LUGAR Y FECHA
- [ ] NÚMERO
- [ ] PROVINCIA

## Normas que cita el formulario

- art. 575 LEC
- art. 590 LEC
- art. 551.2.3 LEC
- art. 551.3.1 LEC
- art. 551.3.2 LEC

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

D. [NOMBRE Y APELLIDOS] Procurador de los Tribunales en representación de D. según consta acreditado en los Autos [TIPO Y Nº DE PROCEDIMIENTO] ante el Tribunal comparezco y como mejor en derecho proceda DIGO:

Que por medio de la presente demanda y en la meritada representación solicito la ejecución de la sentencia de fecha [FECHA] dictada por el Tribunal [ÓRGANO JUDICIAL] en los Autos [TIPO Y Nº DE PROCEDIMIENTO] formulados contra D. [NOMBRE Y APELLIDOS], con base en los siguientes:

HECHOS

PRIMERO.- Que en fecha de [FECHA] se dictó por parte del Tribunal [ÓRGANO JUDICIAL] sentencia (o resolución del Letrado de la Administración de Justicia) que condenaba a D. [NOMBRE Y APELLIDOS] al pago de [IMPORTE] euros en concepto de principal, más [IMPORTE] Euros en concepto de intereses y costas, cantidad que se incrementará, de acuerdo con lo establecido por el artículo 575 LEC, en [IMPORTE] Euros más, en concepto de intereses y costas que se prevé se devengarán durante el desarrollo de la ejecución.

SEGUNDO.- Que designo como bienes a embargar del ejecutado, teniéndolos por suficientes para cubrir el importe de la ejecución los siguientes [BIENES A EMBARGAR].

TERCERO.- Que desconociendo esta parte bienes que puedan ser objeto de embargo por parte de este Tribunal, al amparo de lo dispuesto en el artículo 590 LEC, esta parte solicita al Tribunal proceda a dirigirse a los efectos de determinación de la relación de bienes muebles e inmuebles, así como depósitos o imposiciones a plazo fijo que el ejecutado pueda tener a su nombre a los siguientes organismos:

1. Gerencia Territorial del Catastro de [LOCALIDAD]

2. Delegación Territorial de la Agencia Tributaria de [LOCALIDAD]

3. Registro de la Propiedad núm. [Nº] de [LOCALIDAD]

4. Jefatura Provincial de tráfico de [LOCALIDAD]

5. Caja de Ahorros Provincial de [PROVINCIA]

A los siguientes hechos les son de aplicación los siguientes

1. COMPETENCIA

Artículo 545.1.1º LEC. La competencia es de la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [NÚMERO] ante el cual se formula esta demanda, por ser el que conoció del asunto en primera instancia.

2. PROCEDIMIENTO

Artículo 548, procediéndose a despachar ejecución de la sentencia dentro de los veinte días posteriores a aquél en que la condena haya sido notificada al ejecutado.

Artículo 549 LEC en relación con el que debe ser el contenido de la demanda ejecutiva.

Artículos 551 a 554 LEC en relación al despacho de ejecución.

3. LEGITIMACIÓN

Artículo 517.2. LEC, en relación con los artículos 571 y ss. para la ejecución dineraria.

4. COSTAS

Artículo 539.2 LEC.

Por todo ello,

SUPLICO AL TRIBUNAL: Que teniendo por presentado este escrito con los documentos que lo acompañan y sus copias, se acuerde, sin necesidad de previo requerimiento al deudor, se dicte auto conteniendo la orden general de ejecución y despachando la misma, en el que conforme al artículo 551.2.3º LECiv fije la cantidad reclamada conforme a lo solicitado en la cantidad de [IMPORTE] euros en concepto de principal, más la cantidad de [IMPORTE] en concepto de intereses, gastos y costas.

OTROSÍ DIGO: Que, una vez dictado el auto general de ejecución y de conformidad con el art. 551.3.1º de la LEC, se solicita que por el Letrado de la Administración de Justicia responsable de la misma se dicte decreto procediéndose al embargo, sin previo requerimiento de pago del ejecutado por la cantidad indicada, de los bienes reseñados en el hecho segundo de esta demanda y que se estiman suficientes para cubrir las indicadas responsabilidades en su totalidad.

SUPLICO que se dicte decreto en el que se contengan las medidas que dejo interesadas.

OTROSÍ DIGO II: Que, una vez dictado el auto general de ejecución y de conformidad con el art. 551.3.2º de la LEC, se solicita que por el Letrado de la Administración de Justicia responsable de la misma se dicte decreto procediéndose a adoptar las medidas de localización y averiguación de bienes interesadas en el hecho tercero de esta demanda.

SUPLICO que se dicte decreto en el que se adopten las medidas que dejo interesadas.

Es justicia que pido en [LUGAR Y FECHA]

========================================================================
