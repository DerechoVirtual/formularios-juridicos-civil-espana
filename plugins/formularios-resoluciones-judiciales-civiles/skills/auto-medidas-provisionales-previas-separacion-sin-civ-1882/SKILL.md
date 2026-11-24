---
name: auto-medidas-provisionales-previas-separacion-sin-civ-1882
description: "Auto de medidas provisionales previas a la separación sin hijos y sin acuerdo entre las partes. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Auto de medidas provisionales previas a la separación sin hijos y sin acuerdo entre las partes

> Formulario **CIV-1882** del plugin **Resoluciones judiciales civiles: autos, decretos y diligencias** (`formularios-resoluciones-judiciales-civiles`) · Civil › Resoluciones judiciales (autos, decretos, providencias, diligencias) · normativa revisada el 24-11-2026.

## Qué es

Auto acordando medidas provisionales previas a la demanda de separación del matrimonio, sin que exista conformidad entre las partes y no habiendo hijos en el matrimonio.

Es un modelo de tipo **resoluciones judiciales (autos, decretos, providencias, diligencias)**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Auto de medidas provisionales previas a la separación sin hijos y sin acuerdo entre las partes» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Auto de medidas provisionales previas a la separación sin hijos y sin acuerdo entre las partes” para mi caso». También puedes invocarla directamente con `/formularios-resoluciones-judiciales-civiles:auto-medidas-provisionales-previas-separacion-sin-civ-1882`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-resoluciones-judiciales-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Resoluciones judiciales civiles: autos, decretos y diligencias) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (9 veces)
- [ ] CALLE
- [ ] FECHA
- [ ] IMPORTE
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] MES
- [ ] MOTIVO
- [ ] NÚMERO
- [ ] PISO
- [ ] PORCENTAJE

## Normas que cita el formulario

- art. 771 LEC
- art. 104 CC
- art. 771.4 LEC

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

- Junto a «… Magistrado/a-Juez/a de la Sección de Familia, Infancia y Capacidad del Tribunal»: Denominación legal: Sección de Familia, Infancia y Capacidad. Si no existe en el partido, conoce la Sección Civil o la Única (art. 86.3-4 LOPJ). Fuente: LOPJ arts. 84.2.a) y 86 (redacc. LO 1/2025, BOE-A-2025-76).

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

AUTO

En [LUGAR], a [FECHA].

D./Dña. [NOMBRE Y APELLIDOS], Magistrado/a-Juez/a de la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia de [LOCALIDAD]

ANTECEDENTES DE HECHO

PRIMERO.- Por Dña. se ha presentado escrito que solicita la adopción de medidas provisionales previas a la demanda que se propone promover frente a D. [NOMBRE Y APELLIDOS], sobre separación del matrimonio, acompañando doce documentos.

SEGUNDO.- Presentada la solicitud el LAJ ha convocado a los cónyuges a una comparecencia, para la que han sido citados con las advertencias previstas en la Ley.

TERCERO.- A la comparecencia han asistido la solicitante Dña. [NOMBRE Y APELLIDOS], representada por el Procurador de los Tribunales D./Dña. [NOMBRE Y APELLIDOS], dirigida por el/la Letrado/a D./Dña. [NOMBRE Y APELLIDOS], y su esposo D. [NOMBRE Y APELLIDOS], representado por el Procurador de los Tribunales D./Dña. [NOMBRE Y APELLIDOS], y asistido por el Letrado D./Dña. [NOMBRE Y APELLIDOS], habiéndose intentado el acuerdo a que se refiere el párrafo 1.º del apartado 2 del art. 771 LEC sin avenencia y practicado en dos sesiones sucesivas la prueba propuesta y admitida como pertinente.

FUNDAMENTOS DE DERECHO

PRIMERO.- Dispone el art. 104 CCiv que el cónyuge que se proponga demandar la nulidad, la separación o el divorcio del matrimonio, puede solicitar del juez que adopte, con carácter previo, los efectos y las medidas que los arts. 102 y 103 del mismo texto legal prevén para la efectiva admisión de la demanda; los que quedarán sin efecto si la demanda no se presenta dentro del plazo de treinta días.

SEGUNDO.- A su vez el art. 771 LEC establece que, presentada la solicitud, el LAJ convocará a los cónyuges a una comparecencia, en la que se intentará un acuerdo de las partes, y si no se lograra oído en su caso, el Ministerio Fiscal, se oirán las alegaciones de los cónyuges y se practicará la prueba que propongan y se estime pertinente, resolviéndose lo procedente mediante auto, procedimiento que ha sido cumplido en el presente caso.

TERCERO.- No habiendo acuerdo entre los cónyuges respecto de las medidas, oídas sus alegaciones y examinadas las circunstancias concurrentes, así como los datos suministrados, [MOTIVO] procede acordar los efectos y las medidas que luego se dirán.

PARTE DISPOSITIVA

1.- Se acuerda la separación provisional de los cónyuges D. y Dña. [NOMBRE Y APELLIDOS], cesando la presunción de convivencia conyugal.

2.- Se declaran revocados los consentimientos y poderes que cualquiera de los cónyuges hubiera otorgado a favor del otro, cesando la posibilidad de vincular los bienes privativos del otro cónyuge en el ejercicio de la potestad doméstica.

3.- Se confiere el uso exclusivo de la vivienda familiar sita en la calle [CALLE], n.º [NÚMERO], piso [PISO] a la solicitante, así como del ajuar doméstico en ella existente, debiendo permanecer el otro cónyuge apartado de la vivienda.

4.- D. habrá de contribuir al levantamiento de las cargas familiares con una cantidad del [PORCENTAJE] % de los ingreso netos mensuales que por cualquier concepto perciba desde el mes de [MES], con carácter periódico, que se liquidará en ejecución de esta resolución, momento en el que se fijarán las bases para su actualización, con un mínimo de [IMPORTE] euros mensuales, y que habrá de ingresarse por anticipado, dentro de los cinco primeros días de cada mes, en la cuenta corriente o libreta de ahorro, que al efecto designe la receptora.

Dicha cantidad se actualizará anualmente, con efectos de primero de enero de cada año, en proporción a las variaciones que experimenten los índices de precio al consumo, según el Instituto Nacional de Estadística u organismo que le sustituya.

Los cuatro efectos y medidas sólo subsistirán si dentro de los treinta días siguientes a su adopción se presenta la demanda anunciada de separación del matrimonio.

Así lo acuerdo, mando y firmo:

Firma del Juez:

Esta resolución es firme y contra la misma no cabe recurso alguno (art. 771.4 LEC).

========================================================================
