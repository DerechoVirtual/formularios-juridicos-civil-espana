---
name: contestacion-demanda-ordinaria-conforme-hechos-opuesta-civ-0949
description: "Contestación a la demanda ordinaria conforme en los hechos y opuesta en los fundamentos de derecho. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contestación a la demanda ordinaria conforme en los hechos y opuesta en los fundamentos de derecho

> Formulario **CIV-0949** del plugin **Proceso civil: demandas, contestaciones, prueba y vista** (`formularios-proceso-civil`) · Civil › Escritos procesales (demanda, contestación, prueba, vista) · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contestación a la demanda ordinaria conforme en los hechos y opuesta en los fundamentos de derecho» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contestación a la demanda ordinaria conforme en los hechos y opuesta en los fundamentos de derecho” para mi caso». También puedes invocarla directamente con `/formularios-proceso-civil:contestacion-demanda-ordinaria-conforme-hechos-opuesta-civ-0949`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-proceso-civil:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Proceso civil: demandas, contestaciones, prueba y vista) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] AÑO (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] DÍA
- [ ] FECHA
- [ ] MES
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] Nº
- [ ] Nº DE PROCEDIMIENTO
- [ ] SEDE
- [ ] TIPO DE PROCEDIMIENTO

## Normas que cita el formulario

- art. 249.2 LEC
- art. 394 LEC

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

- Junto a «…TO]/[AÑO] A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
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

Juicio [TIPO DE PROCEDIMIENTO] n.º [Nº DE PROCEDIMIENTO]/[AÑO]

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

D/Dª. [NOMBRE Y APELLIDOS] Procurador/a de los Tribunales, actuando en representación de [NOMBRE DEL REPRESENTADO/A] según se acredita mediante certificación del registro electrónico de apoderamientos judiciales que acompaño comparezco en el presente procedimiento en el que se emplazó a mi representada el pasado [FECHA] y por medio de la presente paso a contestar a la demanda interpuesta contra mi principal en base a los siguientes:

HECHOS

ÚNICO.-Se aceptan la totalidad de los hechos expuestos en la demanda y referentes a la problemática de un contrato de trabajo temporal que había celebrado ya la demandante con su trabajador D. [NOMBRE Y APELLIDOS] al tiempo de contratar los servicios de mi principal, contrato que fue prorrogado por mi mandante y que una vez concluida la relación entre las partes motivó el que por la jurisdicción social fuere declarado como de duración indefinida lo que comportó el que se debiere abonar una indemnización por despido improcedente. Dicho contrato así como las prórrogas del mismo y el resultado de la actuación de la jurisdicción social son aceptados por esta parte.

FUNDAMENTOS DE DERECHO

PRIMERO.- Procedimiento.-Se acepta la tramitación de la causa por los trámites del juicio ordinario con fundamento en el art. 249.2 LEC y asumiendo las alegaciones en este sentido vertidas en el escrito de demanda.

SEGUNDO.- Fondo de la reclamación.-La parte actora imputa a mi principal por las prórrogas del contrato que verificó la conversión del mismo en de duración indefinida, si bien se estima que dicho contrato ya era de duración indefinida cuando mi principal se hizo cargo del mismo y de sus prórrogas ya que en él no se indicaban las concretas circunstancias del mercado, acumulación de tareas o exceso de pedidos que justifican tal contratación temporal según el art. 15.1.b) del Estatuto de los Trabajadores. En tal sentido la STS Sala de lo Social 14 marzo 1997, rec. 1571/1996, dijo que en este tipo de contratos la especificación clara y precisa que justifica esta temporalidad es la expresión de las circunstancias objetivas que constituyen la causa propia del contrato. Ciertamente, lo decisivo es que concurra la causa para la validez del contrato, por ello la falta de forma escrita no transforma por sí sola el contrato temporal en indefinido, siempre que exista prueba en contrario que acredite la naturaleza temporal del mismo. Pero cuando falta la forma escrita, o ésta carece del elemento esencial de la expresión de la causa exigida y se carece de prueba que acredite la existencia de la causa de temporalidad, el contrato deviene en indefinido. Dado que en este caso fue esta carencia la que atribuyó al contrato la condición de indefinido y la misma se produjo antes de la contratación de mi principal se estima que ninguna responsabilidad cabe al mismo atribuir en esta causa.

TERCERO.- En materia de costas el art. 394 LEC.

En base a lo anterior,

SUPLICO AL TRIBUNAL: que tenga por presentado este escrito junto con sus copias, teniendo a esta parte por personada en las presentes actuaciones entendiéndose conmigo las siguientes diligencias y por contestada a la demanda interpuesta contra mi principal y tras la pertinente tramitación se sirva dictar sentencia por la que se desestime la demanda presentada contra mi principal con imposición de costas al demandante.

OTROSÍ PRIMERO DIGO que se acompaña en anexo relación de documentos, debidamente foliados y con índice electrónico, para su debida localización y consulta.

SUPLICO AL TRIBUNAL tenga hecha esta manifestación a los efectos oportunos y por aportados los documentos relacionados en el anexo.

OTROSÍ SEGUNDO DIGO Que esta parte manifiesta su voluntad expresa de cumplir con todos los requisitos exigidos para la validez de la demanda y demás actos procesales ofrece la subsanación de forma inmediata de cualquier defecto en el que pudiera haber incurrido, a requerimiento del Tribunal, todo ello a los efectos prevenidos en el artículo 231 de la Ley de Enjuiciamiento Civil.

SUPLICO AL TRIBUNAL: que tenga por hecha la anterior manifestación y por expresada la voluntad de subsanación de esta parte.

a [DÍA] de [MES] de [AÑO]

Firma Abogado	Firma Procurador

========================================================================
