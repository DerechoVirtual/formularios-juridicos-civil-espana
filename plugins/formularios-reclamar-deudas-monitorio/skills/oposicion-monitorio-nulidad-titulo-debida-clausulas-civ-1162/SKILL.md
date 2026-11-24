---
name: oposicion-monitorio-nulidad-titulo-debida-clausulas-civ-1162
description: "Oposición al monitorio por nulidad del título debida a cláusulas abusivas. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Oposición al monitorio por nulidad del título debida a cláusulas abusivas

> Formulario **CIV-1162** del plugin **Cobrar deudas: monitorio y cambiario** (`formularios-reclamar-deudas-monitorio`) · Civil › Monitorio y cambiario · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Oposición al monitorio por nulidad del título debida a cláusulas abusivas» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Oposición al monitorio por nulidad del título debida a cláusulas abusivas” para mi caso». También puedes invocarla directamente con `/formularios-reclamar-deudas-monitorio:oposicion-monitorio-nulidad-titulo-debida-clausulas-civ-1162`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-reclamar-deudas-monitorio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Cobrar deudas: monitorio y cambiario) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NÚMERO (3 veces)
- [ ] FECHA (2 veces)
- [ ] SEDE (2 veces)
- [ ] AÑO
- [ ] DÍA
- [ ] IMPORTE
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] MES
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] NOMBRE Y APELLIDOS
- [ ] Nº DE CLÁUSULA
- [ ] PORCENTAJE

## Normas que cita el formulario

- art. 815 LEC
- art. 815.4 LEC
- art. 813 LEC
- art. 85.1 LOPJ

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

- Junto a «…dimiento monitorio número A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

Procedimiento monitorio número

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D. [NOMBRE Y APELLIDOS], Procurador de los Tribunales, actuando en representación de [NOMBRE DEL REPRESENTADO/A], según resulta de la designación apud acta otorgada ante el Letrado de la Administración de Justicia de [SEDE] que acompaño, ante el Tribunal y como mejor proceda en Derecho DIGO:

1) Que en fecha [FECHA] mi representado ha ha sido requerido de pago en el proceso monitorio seguido ante ese Tribunal con el número [NÚMERO] a instancias de [LOCALIDAD] en reclamación de [IMPORTE] euros.

2) Que no estando en adeudar la cantidad reclamada por el demandante, por medio del presente escrito y dentro del plazo de veinte días establecido en el artículo 815 de la LEC, formulo OPOSICIÓN al requerimiento de pago alegando sucintamente los siguientes

HECHOS

PRIMERO.- El requerimiento de pago que se ha verificado con mi representado tiene su origen en el presunto impago del contrato de préstamo al consumo suscrito en fecha [FECHA] con la entidad demandante.

El citado préstamo se concertó para realizar unas obras de rehabilitación en la vivienda habitual de mi representado quien ostenta la condición de consumidor.

Pese a que la reclamación de la deuda realizada por el peticionario se fundaba en un contrato entre un empresario y un consumidor, el requerimiento de pago se hizo por decreto, sin dar cuenta al juez para que pueda apreciar el posible carácter abusivo de las cláusulas del contrato, de manera que se infringe el art. 815.4 de la LEC, lo cual determina la procedencia de la oposición que ahora se formula.

SEGUNDO.- La deuda reclamada no es existente, por cuanto que dicho contrato está viciado de nulidad puesto que la pretensión de la entidad demandante se ampara en las cláusulas número [NÚMERO] del contrato, que son abusivas y por ello nulas.

En concreto, la cláusula número [NÚMERO] establece unos intereses de demora anuales del [PORCENTAJE] % automáticamente devengables respecto de las cantidades no satisfechas a su vencimiento, sin necesidad de realizar ningún tipo de reclamación.

La cláusula [Nº DE CLÁUSULA] de dicho contrato confiere a la entidad bancaria la facultad unilateral de declarar exigible la totalidad del préstamo en el caso de que alguno de los plazos pactados venciera sin que el deudor hubiese cumplido su obligación de pago de una parte del capital o de los intereses del préstamo.

Dichas cláusulas, no negociadas individualmente con mi representado, limitan los derechos del consumidor y deben considerarse abusivas y por ende nulas de pleno derecho, según lo dispuesto en el artículo 83 de la Ley de Consumidores y Usuarios, determinando la ineficacia del contrato, y más en concreto la aplicación de la cláusula abusiva de vencimiento anticipado determina la improcedencia de la petición, por lo que la reclamación formulada es contraria a derecho.

FUNDAMENTOS DE DERECHO

Jurisdicción y competencia

Se acepta la del Tribunal al que me dirijo con fundamento en el art. 813 de la LEC, en relación con lo dispuesto en el art. 85.1º LOPJ.

Oposición y procedimiento

Se funda en la nulidad del título por abusividad, de conformidad a lo dispuesto en los artículos 82 y 83 de la Ley de Consumidores y Usuarios, invocando asimismo la Directiva comunitaria 93/13/CEE y la interpretación de las SSTJUE de 14 de junio de 2012, C-618/2010 y 14 de marzo de 2013, C-415/2011, siendo ésta la razón sucinta que se alega con fundamento en los artículo 815 y 818 de la LEC.

En base a lo anterior,

SUPLICO AL TRIBUNAL se tenga por presentado este escrito con sus documentos y justificante de traslado, se sirva admitirlo y tener por formulada oposición al requerimiento de pago efectuado con mi representado, debiendo resolverse la controversia en el juicio que corresponda en su caso, y dictándose decreto poniendo fin al proceso monitorio.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma abogado y procurador

========================================================================
