---
name: auto-seccion-violencia-sobre-mujer-requiere-inhibicion-civ-1844
description: "Auto de la Sección de Violencia sobre la Mujer que requiere de inhibición a la Sección de Familia. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Auto de la Sección de Violencia sobre la Mujer que requiere de inhibición a la Sección de Familia

> Formulario **CIV-1844** del plugin **Resoluciones judiciales civiles: autos, decretos y diligencias** (`formularios-resoluciones-judiciales-civiles`) · Civil › Resoluciones judiciales (autos, decretos, providencias, diligencias) · normativa revisada el 24-11-2026.

## Qué es

Auto de la Sección de Violencia sobre la Mujer del Tribunal de Instancia requiriendo de inhibición a la Sección de Familia del Tribunal de Instancia que está conociendo del proceso matrimonial en el que concurren los requisitos del párrafo tercero del art. 89.7 de la Ley Orgánica del Poder Judicial, determinantes de su competencia.

Es un modelo de tipo **resoluciones judiciales (autos, decretos, providencias, diligencias)**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Auto de la Sección de Violencia sobre la Mujer que requiere de inhibición a la Sección de Familia» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Auto de la Sección de Violencia sobre la Mujer que requiere de inhibición a la Sección de Familia” para mi caso». También puedes invocarla directamente con `/formularios-resoluciones-judiciales-civiles:auto-seccion-violencia-sobre-mujer-requiere-inhibicion-civ-1844`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-resoluciones-judiciales-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Resoluciones judiciales civiles: autos, decretos y diligencias) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (5 veces)
- [ ] FECHA (2 veces)
- [ ] Nº DE PROCEDIMIENTO (2 veces)
- [ ] SEDE (2 veces)
- [ ] DOCUMENTOS A TESTIMONIAR
- [ ] LUGAR
- [ ] MOTIVO
- [ ] NOMBRE DE LAS PARTES
- [ ] NOMBRE DEL SOLICITANTE
- [ ] NOMBRE Y APELLIDOS

## Normas que cita el formulario

- art. 49 bis.3 LEC
- art. 89.7 LOPJ

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

- Junto a «…e género. SEGUNDO.- Por la Sección de Familia, Infancia y Capacidad del Tribunal»: Denominación legal: Sección de Familia, Infancia y Capacidad. Si no existe en el partido, conoce la Sección Civil o la Única (art. 86.3-4 LOPJ). Fuente: LOPJ arts. 84.2.a) y 86 (redacc. LO 1/2025, BOE-A-2025-76).

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

En la ciudad de [LOCALIDAD], a [FECHA]

ANTECEDENTES DE HECHO

PRIMERO.- En este Tribunal se sigue el procedimiento número [Nº DE PROCEDIMIENTO] iniciado a instancia de [NOMBRE DEL SOLICITANTE] como consecuencia de la posible comisión de un acto de violencia de género.

SEGUNDO.- Por la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia de esta capital se está conociendo del proceso matrimonial de [NOMBRE DE LAS PARTES] entre el sujeto pasivo de tales hechos y la persona que presuntamente aparece como autora de los mismos, y así ha sido conocido por este Tribunal en virtud de [LOCALIDAD].

FUNDAMENTOS DE DERECHO

PRIMERO.- De conformidad con lo dispuesto en el art. 49 bis.3º LEC, cuando un Juez de Violencia sobre la Mujer que esté conociendo de una causa penal por violencia de género tenga conocimiento de la existencia de un proceso civil, y verifique la concurrencia de los requisitos del art. 89.7 LOPJ, requerirá de inhibición al Tribunal Civil, el cual deberá acordar de inmediato su inhibición y la remisión de los autos al órgano requirente.

SEGUNDO.- En el presente supuesto, concurren todos y cada uno de los requisitos establecidos en dicho precepto por cuanto que [MOTIVO].

TERCERO.- De conformidad con lo expuesto, procede requerir de inhibición a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia a fin de que sea este Tribunal el que conozca de la demanda de [LOCALIDAD] de [LOCALIDAD].

En atención a lo expuesto,

DISPONGO.-

Requerir de inhibición al Tribunal de Instancia [SEDE] de esta capital a fin de que remita las actuaciones correspondientes al procedimiento número [Nº DE PROCEDIMIENTO] cuya competencia corresponde a este Tribunal, de conformidad con lo fundamentado en la presente resolución.

Acompáñese a la presente resolución testimonio de [DOCUMENTOS A TESTIMONIAR].

Notifíquese la presente resolución al Ministerio Fiscal y a las partes personadas haciéndoles saber que la misma no es firme, pudiendo interponerse recurso de reforma y subsidiario de apelación ante este mismo Tribunal y en el plazo de los tres días siguientes a su notificación, o recurso de apelación dentro de los veinte días siguientes a su notificación, previa constitución del depósito previsto legalmente, que será exigible únicamente a la acusación popular.

Así lo acuerda, manda y firma,

Es justicia que pido en [LUGAR], a [FECHA].

Firma de D./Dña. [NOMBRE Y APELLIDOS] Magistrado-Juez del Tribunal de Instancia de [SEDE] de [LOCALIDAD]

========================================================================
