---
name: declinatoria-ejecucion-sentencia-matrimonial-falta-civ-2871
description: "Declinatoria en la ejecución de sentencia matrimonial por falta de competencia objetiva y funcional. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Declinatoria en la ejecución de sentencia matrimonial por falta de competencia objetiva y funcional

> Formulario **CIV-2871** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 25-11-2026.

## Qué es

Escrito promoviendo declinatoria en la ejecución forzosa ordinaria de sentencia matrimonial, alegando la falta de competencia objetiva y funcional del Tribunal ante el que se ha iniciado ésta, al ser el Juez que dictó la sentencia el competente para conocer del trámite de ejecución forzosa.

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Declinatoria en la ejecución de sentencia matrimonial por falta de competencia objetiva y funcional» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Declinatoria en la ejecución de sentencia matrimonial por falta de competencia objetiva y funcional” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:declinatoria-ejecucion-sentencia-matrimonial-falta-civ-2871`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- `SKILL.md` (este fichero): qué es el formulario, para qué sirve, cómo se usa, los datos que pide, las normas que cita, los avisos de actualización y las instrucciones para Claude.
- `assets/formulario.md`: el formulario seco, tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…]. Es el texto que se rellena; no lleva explicaciones.
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] COMPLETAR (3 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] SEDE (3 veces)
- [ ] AÑO (2 veces)
- [ ] FECHA (2 veces)
- [ ] CALLE
- [ ] COLEGIO
- [ ] CORREO ELECTRÓNICO
- [ ] DESCRIBIR
- [ ] LOCALIDAD
- [ ] Nº
- [ ] Nº DE COLEGIADO/A
- [ ] TELÉFONO

## Normas que cita el formulario

- art. 84.2 a) LOPJ

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

### Avisos de actualización (4) — se aplican en el texto, nunca se copian en el documento

- Al principio del formulario: El art. 46 LEC sigue remitiendo al art. 98 LOPJ, hoy sin contenido; la especialización resulta del art. 86 LOPJ.
- Junto a «…]/[AÑO] SOBRE [DESCRIBIR] A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…ncia dictada por la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. «De los de» es residuo de los varios juzgados de una plaza. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).
- Junto a «… objetiva corresponde a la Sección de Familia, Infancia y Capacidad del Tribunal»: Denominación legal: Sección de Familia, Infancia y Capacidad. Si no existe en el partido, conoce la Sección Civil o la Única (art. 86.3-4 LOPJ). Fuente: LOPJ arts. 84.2.a) y 86 (redacc. LO 1/2025, BOE-A-2025-76).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Notas al pie del formulario original:
(1) LA DECLINATORIA EN LA EJECUCIÓN FORZOSA. GENERAL.

La declinatoria, tanto en los procesos declarativos como en los de ejecución, en los términos en que aparece concebida en la vigente ley de enjuiciamiento civil, opera como un remedio al alcance de la parte demandada o de cuantos otros pudieran ser parte legítima en el juicio ya promovido, orientado a denunciar la posible falta de jurisdicción o de competencia, ya objetiva, ya territorial, del órgano que estuviere conociendo del asunto.

La declinatoria, desde luego, deberá proponerse ante el órgano jurisdiccional que estuviese conociendo del asunto, habiendo desaparecido en la vigente legislación la posibilidad de denunciar la falta de competencia del órgano que estuviera conociendo del asunto no ante éste sino ante aquél que se considera por la parte como competente (la vieja inhibitoria), si bien, de conformidad con los artículos 65 y 547 de la Ley de Enjuiciamiento Civil también podrá presentarse ante el domicilio del demandado (art. 63).

La declinatoria en la ejecución forzosa habrá de interponerse dentro del plazo de cinco días siguientes a aquél en que ha recibido la primera notificación del proceso de ejecución, debiendo entenderse que nos hallamos ante un plazo preclusivo de forma tal que no planteada durante el mismo la declinatoria, no podrá sostenerse con posterioridad (art. 547).

El efecto inmediato de su interposición será el de suspender el curso del plazo para plantear el incidente de oposición hasta tanto sea resuelta, debiendo computarse a efectos de contabilizar el plazo para plantear el incidente de oposición (respecto del que se conceden diez días), una vez el procedimiento se reanude el que ya hubiere transcurrido.

COMPETENCIA OBJETIVA Y FUNCIONAL EN LA EJECUCIÓN FORZOSA

La falta de competencia objetiva y funcional en el órgano jurisdiccional que estuviera conociendo del asunto, que podrá ser apreciada de oficio, es también circunstancia que puede denunciarse por el demandado, debiendo servirse para ello de la correspondiente interposición de la declinatoria. Es lógico que se excluya de esa posibilidad al demandante por cuanto es éste quien ha escogido el órgano jurisdiccional al interponer su demanda ejecutiva.

Así pues, la parte demandada podrá denunciar la falta de competencia objetiva y funcional en el órgano jurisdiccional que estuviera conociendo del asunto, empleando para ello la declinatoria en tiempo y forma.


### Flujo

1. **Paso 0**: comprueba Jurisprudenciator (arriba).
2. Lee entero `assets/formulario.md` (el formulario que vas a rellenar, en la carpeta de esta skill) y la parte de `../indice/marco.md` que afecte al caso. Limítate a la materia de este formulario: no añadas contenido ajeno a él.
3. Pide los datos de la lista en una sola tanda. Si un dato aparece varias veces, aclara a qué persona o acto corresponde cada vez. Lo que el usuario no sepa se queda como hueco visible con su etiqueta (p. ej. [FECHA]).
4. Resuelve cada [ELEGIR …] y cada [OPCIONAL …] según los hechos, y sustituye cualquier indicación entre paréntesis del formulario («(se describirá…)», «(indicar…)») por el contenido que corresponda. Redacta las partes que dependen del caso (hechos, motivos, descripción de bienes).
5. Aplica los avisos de actualización en el lugar que indican. Comprueba con `buscar_articulo` cada norma citada; si alguna ha cambiado, usa la redacción vigente. Si citas jurisprudencia, localízala con `buscar_sentencias` o `buscar_por_cita` y léela con `leer_sentencias`.
6. Antes de entregarlo, pasa `verificar_escrito` con las frases que citan normas o sentencias y corrige lo que señale.
7. **Documento final = el formulario tal cual, rellenado y limpio.**
   - Empieza exactamente por la primera línea de `assets/formulario.md` y sigue su estructura y su orden hasta la firma.
   - No pongas en el documento título, nombre del formulario o de la skill, código, encabezados, «Para qué sirve», leyendas, avisos, notas de uso, comentarios ni explicaciones. Tampoco marcas [ELEGIR…] u [OPCIONAL…]: ya están resueltas.
   - Formato Word (.docx, con la skill de Word disponible): **Times New Roman 11 pt** en todo el documento, **interlineado 1,15**, **texto justificado**, márgenes de 2,5 cm. Los rótulos del formulario (REUNIDOS, CLÁUSULAS, HECHOS, SUPLICO…) en su propia línea y en negrita, sin cambiar su texto.
8. En el chat (nunca dentro del documento): datos pendientes, partes redactadas por ti, normas y sentencias comprobadas con Jurisprudenciator (y, si algún dato sale de internet, cuál y su enlace) y, si es un escrito judicial o administrativo, el plazo y el órgano ante el que se presenta.

El resultado es un borrador para que lo revise un profesional antes de usarlo.
