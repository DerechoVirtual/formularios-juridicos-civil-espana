---
name: demanda-ejecucion-provisional-sentencia-condena-no-civ-1690
description: "Demanda de ejecución provisional de sentencia de condena no dineraria. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de ejecución provisional de sentencia de condena no dineraria

> Formulario **CIV-1690** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Demanda de ejecución provisional, sin prestación de caución, de una sentencia de condena no dineraria dictada en primera instancia y recurrida en apelación, para que el condenado cumpla en sus propios términos el fallo sin esperar a la resolución del recurso (arts. 524 y ss. LEC).

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de ejecución provisional de sentencia de condena no dineraria» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de ejecución provisional de sentencia de condena no dineraria” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:demanda-ejecucion-provisional-sentencia-condena-no-civ-1690`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] CLASE Y Nº DE JUICIO (2 veces)
- [ ] FECHA (2 veces)
- [ ] FIRMA (2 veces)
- [ ] NOMBRE O DENOMINACIÓN SOCIAL DEL EJECUTADO (2 veces)
- [ ] Nº DE PROCEDIMIENTO (2 veces)
- [ ] AÑO
- [ ] DÍA
- [ ] IMPORTE
- [ ] LOCALIDAD
- [ ] MES
- [ ] NOMBRE O DENOMINACIÓN SOCIAL DEL EJECUTANTE
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] RELACIÓN DE BIENES
- [ ] SEDE
- [ ] TRANSCRIBIR EL FALLO DE LA SENTENCIA

## Normas que cita el formulario

- art. 526 LEC
- art. 524.2 LEC
- art. 538 LEC
- art. 539 LEC
- art. 525 LEC

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales y de [NOMBRE O DENOMINACIÓN SOCIAL DEL EJECUTANTE], conforme a la representación acreditada en los autos de juicio [CLASE Y Nº DE JUICIO], seguidos con el número de registro [Nº DE PROCEDIMIENTO], ante el Tribunal comparezco y, como mejor proceda en Derecho, DIGO:

Que por medio del presente escrito, y siguiendo instrucciones de mi mandante, formulo DEMANDA DE EJECUCIÓN PROVISIONAL frente a [NOMBRE O DENOMINACIÓN SOCIAL DEL EJECUTADO], en virtud de los siguientes

HECHOS

PRIMERO.– El pasado día [FECHA] recayó sentencia en los autos de juicio [CLASE Y Nº DE JUICIO], seguidos con el número de registro [Nº DE PROCEDIMIENTO] en el Tribunal al que tengo el honor de dirigirme, cuya parte dispositiva dice literalmente: «[TRANSCRIBIR EL FALLO DE LA SENTENCIA]».

Se acompaña certificación de la citada sentencia y demás particulares necesarios para su ejecución.

SEGUNDO.– La sentencia antes mencionada fue apelada por la parte condenada por considerarla lesiva a sus intereses.

TERCERO.– Con fecha [FECHA] se ha notificado a esta parte diligencia de ordenación teniendo por interpuesto recurso de apelación contra la sentencia dictada en estos autos. Por lo tanto, con el fin de que no se irroguen nuevos perjuicios a mi patrocinado a causa de la lógica dilación que lleva consigo la tramitación de la apelación, es por lo que se solicita la ejecución provisional de la sentencia.

FUNDAMENTOS DE DERECHO

I.– COMPETENCIA.

Según el art. 526 LEC, quien haya obtenido un pronunciamiento a su favor en sentencia de condena dictada en primera instancia podrá, sin simultánea prestación de caución, pedir y obtener su ejecución provisional, conforme a lo previsto en los artículos siguientes, ante el Tribunal competente para la primera instancia (art. 524.2 LEC).

II.– LEGITIMACIÓN.

El art. 526 LEC legitima para solicitar la ejecución provisional a «quien haya obtenido un pronunciamiento a su favor en sentencia de condena dictada en primera instancia».

Por otro lado, el art. 538 LEC regula quiénes son partes y sujetos de la ejecución forzosa, estando en el presente supuesto legitimado activamente mi poderdante por ser el acreedor de la obligación que se reclama y haber obtenido a su favor sentencia de condena frente al deudor condenado, quien por esta causa ostenta la legitimación pasiva.

III.– POSTULACIÓN.

Al tratarse de la ejecución provisional de una sentencia dictada en un proceso en el que es preceptiva la intervención de abogado y procurador, la presente demanda viene firmada por dichos profesionales, de conformidad con lo dispuesto en el art. 539 LEC.

IV.– PROCEDENCIA.

Al ser la sentencia de condena y no estar incluida en los supuestos enumerados en el art. 525 LEC, procede que se despache la ejecución provisional, ya que la solicitud se ha formulado con posterioridad a la notificación de la resolución de tener por interpuesto el recurso de apelación y antes de que se haya resuelto dicho recurso.

En virtud de todo lo anterior,

SUPLICO AL TRIBUNAL

que se tenga por presentada esta demanda y, previos los trámites legalmente previstos, se despache ejecución provisional de la sentencia contra [NOMBRE O DENOMINACIÓN SOCIAL DEL EJECUTADO], requiriendo al ejecutado para que, dentro del plazo que el Tribunal estime adecuado, cumpla en sus propios términos lo establecido en la parte dispositiva de la sentencia que se ejecuta, bajo los apercibimientos legales.

Es de Justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

OTROSÍ DIGO que, para asegurar el pago de las eventuales indemnizaciones y costas de la ejecución, se acuerde por el Tribunal el embargo de bienes del ejecutado en cantidad de [IMPORTE] euros, señalándose a tal fin como bienes a embargar: [RELACIÓN DE BIENES].

Es justicia que reitero en lugar y fecha ut supra.

Firma del Abogado/a: [FIRMA] Firma del Procurador/a: [FIRMA]
