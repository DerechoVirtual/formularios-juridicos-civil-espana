---
name: auto-despacha-ejecucion-sentencia-firme-condena-pago-civ-2092
description: "Auto que despacha ejecución de sentencia firme de condena al pago de cantidad. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Auto que despacha ejecución de sentencia firme de condena al pago de cantidad

> Formulario **CIV-2092** del plugin **Resoluciones judiciales civiles: autos, decretos y diligencias** (`formularios-resoluciones-judiciales-civiles`) · Civil › Resoluciones judiciales (autos, decretos, providencias, diligencias) · normativa revisada el 24-11-2026.

## Qué es

Auto por el que se despacha la ejecución de sentencia de condena firme sobre reclamación de cantidad, más intereses ordinarios y moratorios vencidos y otra suma presupuestada provisionalmente para intereses y costas (arts. 517, 548, 549 y 551 LEC).

Es un modelo de tipo **resoluciones judiciales (autos, decretos, providencias, diligencias)**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Auto que despacha ejecución de sentencia firme de condena al pago de cantidad» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Auto que despacha ejecución de sentencia firme de condena al pago de cantidad” para mi caso». También puedes invocarla directamente con `/formularios-resoluciones-judiciales-civiles:auto-despacha-ejecucion-sentencia-firme-condena-pago-civ-2092`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-resoluciones-judiciales-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Resoluciones judiciales civiles: autos, decretos y diligencias) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (4 veces)
- [ ] IMPORTE EN LETRA (4 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] AÑO (2 veces)
- [ ] DÍA
- [ ] FECHA
- [ ] LOCALIDAD
- [ ] MES
- [ ] NOMBRE Y APELLIDOS / DENOMINACIÓN SOCIAL DEL EJECUTADO
- [ ] Nº DE PROCEDIMIENTO
- [ ] TRANSCRIPCIÓN DE LA PARTE DISPOSITIVA

## Normas que cita el formulario

- art. 517.1 LEC
- art. 548 LEC
- art. 549.2 LEC
- art. 520 LEC
- art. 580 LEC
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

Magistrado/a: [NOMBRE Y APELLIDOS]

ANTECEDENTES DE HECHO

ÚNICO.- Por el/la Procurador/a D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS], se formuló demanda ejecutiva, que fue registrada con el número [Nº DE PROCEDIMIENTO] / [AÑO], frente a D./Dña. [NOMBRE Y APELLIDOS], en reclamación de la cantidad de [IMPORTE EN LETRA] euros ([IMPORTE] €) en concepto de principal e intereses devengados hasta la fecha, más otros [IMPORTE EN LETRA] euros ([IMPORTE] €) presupuestados provisionalmente para hacer frente a los intereses que, en su caso, puedan devengarse durante la ejecución y las costas de ésta. Fundamentaba su petición en la sentencia firme dictada por este Tribunal en fecha [FECHA], cuya parte dispositiva era del tenor literal siguiente: [TRANSCRIPCIÓN DE LA PARTE DISPOSITIVA].

FUNDAMENTOS DE DERECHO

PRIMERO.- Conforme al art. 517.1 de la LEC, la acción ejecutiva deberá fundarse en un título que lleve aparejada ejecución, enumerando el apartado 2 de dicho precepto cuáles son tales títulos. En el ordinal 1.º de dicho precepto aparece la sentencia de condena firme.

SEGUNDO.- El art. 548 LEC establece que el tribunal no despachará ejecución de resoluciones judiciales o arbitrales o de convenios aprobados judicialmente dentro de los veinte días posteriores a aquél en que la resolución de condena o de aprobación del convenio haya sido notificada al ejecutado.

TERCERO.- Cuando el título de ejecución sea una sentencia o resolución dictada por tribunal competente para conocer la ejecución, la demanda ejecutiva podrá limitarse a la solicitud de que se despache la ejecución, identificando la sentencia o resolución cuya ejecución se pretenda (art. 549.2 LEC). Tampoco se establece para estos casos el límite mínimo de 300 euros fijado en el art. 520 LEC, ni será necesario requerir previamente de pago al ejecutado (art. 580 LEC), por lo que podrán llevarse a efecto de inmediato las medidas de localización y averiguación de bienes del ejecutado.

PARTE DISPOSITIVA

SE ACUERDA: Tener por presentado el anterior escrito con los documentos acompañados y, en consecuencia, despáchese la ejecución frente a [NOMBRE Y APELLIDOS / DENOMINACIÓN SOCIAL DEL EJECUTADO] por la cantidad de [IMPORTE EN LETRA] euros ([IMPORTE] €) en concepto de principal e intereses ordinarios y moratorios vencidos, más otros [IMPORTE EN LETRA] euros ([IMPORTE] €) presupuestados provisionalmente para hacer frente a los intereses que, en su caso, puedan devengarse durante la ejecución y a las costas de ésta.

Notifíquese este auto con copia de la demanda ejecutiva al ejecutado, sin citación ni emplazamiento, para que en cualquier momento pueda personarse en la ejecución, entendiéndose con él, en tal caso, las ulteriores actuaciones.

Lo acuerdo, mando y firmo.

Firma del/de la Magistrado/a:

Contra esta resolución no cabe recurso, conforme al art. 551.4 de la LEC, sin perjuicio de la oposición que pueda formular el ejecutado dentro de los diez días siguientes a su notificación.
