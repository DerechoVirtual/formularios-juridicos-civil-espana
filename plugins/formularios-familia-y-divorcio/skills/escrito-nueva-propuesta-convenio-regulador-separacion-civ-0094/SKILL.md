---
name: escrito-nueva-propuesta-convenio-regulador-separacion-civ-0094
description: "Escrito con nueva propuesta de convenio regulador de separación o divorcio. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito con nueva propuesta de convenio regulador de separación o divorcio

> Formulario **CIV-0094** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito con nueva propuesta de convenio regulador de separación o divorcio» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito con nueva propuesta de convenio regulador de separación o divorcio” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:escrito-nueva-propuesta-convenio-regulador-separacion-civ-0094`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (9 veces)
- [ ] IMPORTE (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] DESCRIBIR
- [ ] ENTIDAD BANCARIA
- [ ] FECHA
- [ ] Nº
- [ ] Nº DE COLEGIADO/A
- [ ] Nº DE CUENTA (IBAN)
- [ ] NÚMERO
- [ ] SEDE
- [ ] TIPO DE PROCEDIMIENTO

## Normas que cita el formulario

- art. 154 Código Civil

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

D./Dña. [NOMBRE Y APELLIDOS] Procurador de los Tribunales, con número de colegiado/a [Nº DE COLEGIADO/A] en representación de dña. y don [NOMBRE Y APELLIDOS] según tengo acreditado en los autos de [TIPO DE PROCEDIMIENTO] (separación/divorcio), ante el Tribunal comparezco y DIGO:

Que conforme a lo requerido en la providencia de fecha [FECHA] se adjunta como doc. número [NÚMERO] 1, nueva propuesta de convenio sobre [DESCRIBIR] a los efectos de su aprobación judicial.

ESTIPULACIONES:

Iº. Se acuerda la suspensión de la vida en común de los cónyuges.

2º. Don [NOMBRE Y APELLIDOS] establece su domicilio en [LOCALIDAD] y doña [NOMBRE Y APELLIDOS] lo hace en [LOCALIDAD]. Todo cambio de domicilio por cualquiera de los cónyuges habrá de ser comunicado al otro, para poder hacer viable lo dispuesto en el presente convenio sobre el régimen de visitas, comunicación y estancia de los progenitores con sus hijos.

3º.Los hijos quedarán sujetos a la patria potestad de ambos progenitores, actuando éstos siempre en beneficio de los hijos, de acuerdo con su personalidad, velando por ellos, teniéndolos en su compañía, alimentándolos, educándolos, procurándoles una formación integral, así como representándolos y administrándoles sus bienes, ello conforme a lo establecido en el art.154 del Código Civil.

4º Los hijos [NOMBRE Y APELLIDOS] y [NOMBRE Y APELLIDOS] vivirán con don/dña., en el domicilio fijado para éste/a, atribuyéndosele a d/dña. la guarda y custodia de los hijos.

5º.El uso de la vivienda y del ajuar familiar se otorgan, por el presente documento, a don/dña., por ser a quien se le atribuye la guarda y custodia de los hijos.

6º.El régimen de visitas, comunicación y estancia de [NOMBRE Y APELLIDOS] y [NOMBRE Y APELLIDOS] con d/doña [NOMBRE Y APELLIDOS] será:

7º.La pensión alimenticia que corresponde satisfacer a d/dña. es de [IMPORTE] euros mensuales por hijo, siendo la suma total de [IMPORTE] euros mensuales. Dicha cantidad será actualizada anualmente, desde la fecha de firma del presente convenio regulador, conforme al IPC, según se acredite por certificación del Instituto Nacional de Estadística.

Las cantidades deberán ser ingresadas en el número de cuenta [Nº DE CUENTA (IBAN)] abierta a nombre de d/dña. en la Entidad Bancaria [ENTIDAD BANCARIA]

8º.Los gastos extraordinarios de los hijos, entendiendo como tales los gastos médicos, quirúrgicos o farmacéuticos, que no estén cubiertos por la seguridad social, los cubrirán al 50% cada progenitor.

Cualquier otro gasto habrá de consensuarse por los progenitores, debiendo constar autorización por escrito.

Y en prueba de su conformidad, firman la presente Propuesta de Convenio Regulador de Separación.

Por lo cual,

SUPLICO AL TRIBUNAL: Tenga por presentado este escrito y documentos y, sus copias, lo una a autos, dándose a las copias el curso legal, y previa ratificación de los cónyuges dicte auto aprobando este tribunal la nueva propuesta en el sentido interesado.

Fdo. Letrado Fdo. Procurador

Coleg. núm. Coleg. núm. [Nº]

========================================================================
