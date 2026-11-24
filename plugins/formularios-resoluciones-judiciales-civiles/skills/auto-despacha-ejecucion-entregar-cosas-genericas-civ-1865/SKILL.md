---
name: auto-despacha-ejecucion-entregar-cosas-genericas-civ-1865
description: "Auto que despacha ejecución para entregar cosas genéricas o indeterminadas. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Auto que despacha ejecución para entregar cosas genéricas o indeterminadas

> Formulario **CIV-1865** del plugin **Resoluciones judiciales civiles: autos, decretos y diligencias** (`formularios-resoluciones-judiciales-civiles`) · Civil › Resoluciones judiciales (autos, decretos, providencias, diligencias) · normativa revisada el 24-11-2026.

## Qué es

Auto por el que se despacha ejecución de una sentencia firme de condena a entregar cosas genéricas o indeterminadas, requiriendo al ejecutado para que las entregue en el plazo señalado, con el apercibimiento de que el ejecutante podrá adquirirlas a su costa y de embargo de bienes suficientes (arts. 517, 548 y 702 y ss. LEC).

Es un modelo de tipo **resoluciones judiciales (autos, decretos, providencias, diligencias)**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Auto que despacha ejecución para entregar cosas genéricas o indeterminadas» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Auto que despacha ejecución para entregar cosas genéricas o indeterminadas” para mi caso». También puedes invocarla directamente con `/formularios-resoluciones-judiciales-civiles:auto-despacha-ejecucion-entregar-cosas-genericas-civ-1865`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-resoluciones-judiciales-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Resoluciones judiciales civiles: autos, decretos y diligencias) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS DEL EJECUTADO (3 veces)
- [ ] AÑO (2 veces)
- [ ] DÍA (2 veces)
- [ ] MES (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL EJECUTANTE (2 veces)
- [ ] PLAZO DE ENTREGA (2 veces)
- [ ] COSAS A ENTREGAR
- [ ] COSAS GENÉRICAS O INDETERMINADAS A ENTREGAR
- [ ] FIRMA
- [ ] INDICAR LO QUE HA DE ENTREGAR
- [ ] LOCALIDAD
- [ ] NOMBRE Y APELLIDOS
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] Nº DE PROCEDIMIENTO
- [ ] PARTE DISPOSITIVA DE LA SENTENCIA

## Normas que cita el formulario

- art. 517 LEC
- art. 551.4 LEC

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

### Avisos de actualización (0) — se aplican en el texto, nunca se copian en el documento

- Ninguno.

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

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Juez/a Sr./Sra. [NOMBRE Y APELLIDOS]

ANTECEDENTES DE HECHO

ÚNICO.– Por el/la Procurador/a D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS DEL EJECUTANTE], se formuló demanda ejecutiva, que fue registrada con el número [Nº DE PROCEDIMIENTO], frente a D./Dña. [NOMBRE Y APELLIDOS DEL EJECUTADO], con la finalidad de que el ejecutado hiciera entrega al ejecutante de [COSAS GENÉRICAS O INDETERMINADAS A ENTREGAR].

Fundamentaba su petición en la sentencia firme dictada por este Tribunal en fecha [DÍA] de [MES] de [AÑO], cuya parte dispositiva era del tenor literal siguiente: «[PARTE DISPOSITIVA DE LA SENTENCIA]».

FUNDAMENTOS DE DERECHO

PRIMERO.– Para que proceda despachar ejecución a instancia de la parte que ha obtenido sentencia estimatoria de su pretensión es preciso que se cumplan las exigencias legales contenidas en los arts. 517 y 548 LEC, en virtud de los cuales es preciso que exista sentencia de condena firme y que hayan transcurrido veinte días desde que aquella se hubiera notificado al condenado sin que el mismo procediera al cumplimiento voluntario y extrajudicial.

SEGUNDO.– En este caso concreto la representación de D./Dña. [NOMBRE Y APELLIDOS DEL EJECUTANTE] ha solicitado el despacho de ejecución porque el condenado a la entrega de [COSAS A ENTREGAR] no ha cumplido de forma voluntaria en el plazo antes referido, pese a haberle notificado la sentencia, que es firme; comprobadas las alegaciones de la parte, procede acceder a su petición, acordando el requerimiento al ejecutado D./Dña. [NOMBRE Y APELLIDOS DEL EJECUTADO] para que proceda a cumplir el contenido de la sentencia entregando al ejecutante [INDICAR LO QUE HA DE ENTREGAR], en el plazo de [PLAZO DE ENTREGA], bajo el apercibimiento de que, si no lo hiciera, a instancia del ejecutante se podrá acordar por el LAJ la puesta a disposición del mismo de aquellas, o se le podrá facultar para que las adquiera a su costa, al ser aquellas de naturaleza genérica o indeterminada que se pueden comprar en el mercado, ordenando asimismo el embargo de bienes suficientes para pagar la adquisición, de la que el ejecutante no obstante habrá de dar cuenta justificada.

PARTE DISPOSITIVA

En atención a todo lo anterior, SE ACUERDA: tener por presentado el anterior escrito con los documentos acompañados y, en consecuencia, despáchese ejecución frente a [NOMBRE Y APELLIDOS DEL EJECUTADO], a quien se requiere para que en el plazo de [PLAZO DE ENTREGA] entregue al ejecutante [INDICAR LO SOLICITADO POR EL EJECUTANTE QUE INTEGRE LA CONDENA DEL EJECUTADO], con el apercibimiento de que, en el caso de que no lleve a cabo la entrega en el término concedido, el ejecutante podrá instar que por el LAJ se le ponga en posesión de las cosas debidas o que se le faculte para que las adquiera, a costa del ejecutado, ordenando al mismo tiempo el embargo de bienes suficientes para pagar la adquisición, de la que el ejecutante dará cuenta justificada.

Notifíquese este auto con copia de la demanda ejecutiva al ejecutado, sin citación ni emplazamiento, para que en cualquier momento pueda personarse en la ejecución, entendiéndose con él, en tal caso, las ulteriores actuaciones.

Así lo acuerdo, mando y firmo.

Firma del Juez/a: [FIRMA]

Contra esta resolución no cabe recurso, conforme al art. 551.4 LEC, sin perjuicio de la oposición que pueda formular el ejecutado dentro de los diez días siguientes a su notificación.
