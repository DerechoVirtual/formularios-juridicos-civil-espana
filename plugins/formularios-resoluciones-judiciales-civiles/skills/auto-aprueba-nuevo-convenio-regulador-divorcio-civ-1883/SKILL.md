---
name: auto-aprueba-nuevo-convenio-regulador-divorcio-civ-1883
description: "Auto que aprueba el nuevo convenio regulador de divorcio con la estipulación modificada. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Auto que aprueba el nuevo convenio regulador de divorcio con la estipulación modificada

> Formulario **CIV-1883** del plugin **Resoluciones judiciales civiles: autos, decretos y diligencias** (`formularios-resoluciones-judiciales-civiles`) · Civil › Resoluciones judiciales (autos, decretos, providencias, diligencias) · normativa revisada el 24-11-2026.

## Qué es

Auto aprobando en su totalidad en convenio regulador propuesto por los cónyuges, mediante la modificación introducida en la estipulación no aprobada del primitivamente suscrito.

Es un modelo de tipo **resoluciones judiciales (autos, decretos, providencias, diligencias)**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Auto que aprueba el nuevo convenio regulador de divorcio con la estipulación modificada» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Auto que aprueba el nuevo convenio regulador de divorcio con la estipulación modificada” para mi caso». También puedes invocarla directamente con `/formularios-resoluciones-judiciales-civiles:auto-aprueba-nuevo-convenio-regulador-divorcio-civ-1883`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-resoluciones-judiciales-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Resoluciones judiciales civiles: autos, decretos y diligencias) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] FECHA (2 veces)
- [ ] LOCALIDAD
- [ ] LUGAR

## Normas que cita el formulario

- art. 90.a CC

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

- Junto a «…OS], Magistrado-Juez de la Sección de Familia, Infancia y Capacidad del Tribunal»: Denominación legal: Sección de Familia, Infancia y Capacidad. Si no existe en el partido, conoce la Sección Civil o la Única (art. 86.3-4 LOPJ). Fuente: LOPJ arts. 84.2.a) y 86 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…en interés de los hijos menores o personas con discapacidad con medidas de apoyo»: Desde la Ley 8/2021, de 2 de junio, no existe la incapacitación judicial ni la tutela de mayores de edad: donde el texto dice «incapacitado» debe entenderse persona con discapacidad que cuenta con medidas de apoyo (en su caso, curatela representativa). Fuente: Ley 8/2021.

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

D./Dña. [NOMBRE Y APELLIDOS], Magistrado-Juez de la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia de [LOCALIDAD].

ANTECEDENTES DE HECHO

PRIMERO.- En el presente procedimiento se dictó sentencia que concedió el divorcio del matrimonio formado por D [NOMBRE Y APELLIDOS] y Dña. [NOMBRE Y APELLIDOS]

Se hacía constar que en el matrimonio había dos hijos menores de edad.

La citada sentencia no aprobó en parte (estipulación II) el convenio presentado por los cónyuges.

SEGUNDO.- Notificada la sentencia, se concedió a los cónyuges un plazo de cinco días para que pudieran optar por continuar con la representación y defensa únicas o comparecer separadamente, ante lo que guardaron silencio, por lo que se consideró seguían con la asistencia técnica inicial única.

TERCERO.- Seguidamente se concedió a los cónyuges plazo de diez días para que pudieran presentar nuevo convenio que atendiera a los términos de la sentencia dictada, y en tiempo y forma por su mandataria procesal se ha presentado propuesta modificativa del convenio en fecha

CUARTO.- De la nueva propuesta de convenio se dio traslado al Ministerio Fiscal por plazo de cinco días para emisión de informe, que se ha recibido el [FECHA], y se une a los autos.

FUNDAMENTOS DE DERECHO

ÚNICO.-

Coincidiendo también en este caso con la opinión dictaminada por el Ministerio Fiscal, se reputa digna de aprobación la propuesta de modificación de la estipulación II del convenio regulador presentada, como no lo era en su versión primitiva. Ciertamente resulta óptimo que el régimen de comunicación, visita y estancia del padre que no guarda a sus hijos en potestad sea todo lo natural y flexible que surja de unas relaciones fluidas y normalizadas entre los ex cónyuges, y aunque tal parecía ser la costumbre en el matrimonio que se disuelve desde su separación (las diferencias eran de economía, y justificadas en un cambio laboral del marido, productor de las rentas familiares mayoritarias), nada excluye la eventualidad de futuros episodios de desacuerdo, o aún de posiciones propias de los hijos, según avancen en su edad y gobierno. Por ello, cuando la Ley se refiere a un ‘régimen’ (art. 90.a) CCiv), quiere que se convenga un estatuto de derechos y obligaciones mutuas dotado de certeza, para el supuesto hipotético de incumplimiento. Si se dejara todo a la avenencia cotidiana, faltaría régimen, porque no podría nunca fijarse el cumplimiento convenido, y ello repercutiría, no ya en la carencia de mecanismos correctores para el progenitor afectado, que no es el interés que puede proteger el Juzgador, sino para el interés y tutela de los mismos hijos menores.

PARTE DISPOSITIVA

Se aprueba en su totalidad en convenio regulador propuesto por los cónyuges, mediante la modificación introducida en la estipulación II del primitivamente suscrito.

Contra esta resolución, únicamente cabrá recurso si lo interpusiera el Ministerio Fiscal en interés de los hijos menores o personas con discapacidad con medidas de apoyo .

Así lo acuerdo, mando y firmo:

Firma del Juez/a

========================================================================
