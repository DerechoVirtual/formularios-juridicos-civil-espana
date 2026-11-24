---
name: alegacion-demandante-hecho-nueva-noticia-audiencia-civ-0977
description: "Alegación del demandante de un hecho de nueva noticia en la audiencia previa, y oposición. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Alegación del demandante de un hecho de nueva noticia en la audiencia previa, y oposición

> Formulario **CIV-0977** del plugin **Proceso civil: demandas, contestaciones, prueba y vista** (`formularios-proceso-civil`) · Civil › Escritos procesales (demanda, contestación, prueba, vista) · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Alegación del demandante de un hecho de nueva noticia en la audiencia previa, y oposición» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Alegación del demandante de un hecho de nueva noticia en la audiencia previa, y oposición” para mi caso». También puedes invocarla directamente con `/formularios-proceso-civil:alegacion-demandante-hecho-nueva-noticia-audiencia-civ-0977`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-proceso-civil:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Proceso civil: demandas, contestaciones, prueba y vista) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (2 veces)
- [ ] LOCALIDAD

## Normas que cita el formulario

- art. 426.4 LEC
- art. 286.4 LEC

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

Con la venia, al amparo de lo dispuesto en el art. 426.4 de la LEC, para alegar un hecho que ha conocido esta parte con posterioridad a la presentación de la demanda como es que la finca reivindicada ha sido objeto de expropiación parcial como consecuencia de las obras de urbanización, y por este motivo el demandado ha percibido una indemnización de 8.300 euros. Este hecho se produjo hace dos años, tal como se desprende de la certificación del Secretario del Ayuntamiento de [LOCALIDAD] de fecha [FECHA], que aportamos en este acto como documento número 1. El hecho resultaba desconocido para esta parte hasta el pasado día 12 de diciembre cuando fue notificada de tal extremo por los servicios del Catastro, como consecuencia de procederse a la revisión de la valoración catastral de la finca; acompañamos como documento número 2 la notificación cursada de fecha [FECHA]; asimismo, debe tenerse en cuenta que el demandado nunca puso en conocimiento de esta parte la expropiación parcial de la finca, ni en el acto de conciliación cuya acta acompañamos como documento número 4 de la demanda, ni en el escrito de contestación, lo cual abunda en que esta parte no era conocedora de este hecho.

Por lo expuesto, solicitamos que se admita el nuevo hecho alegado, así como los documentos que ahora aportamos, y, en su virtud, se tenga por modificada la pretensión sostenida por esta parte, en el sentido que el demandado deberá indemnizar a mi mandante en la cantidad de 8.300 euros, más el interés legal desde esta interpelación, importe del justiprecio percibido con la expropiación de la finca reivindicada, manteniendo el resto de peticiones formuladas en nuestro escrito de demanda.

Para oponernos al hecho ahora alegado por la parte actora porque el mismo ya era conocido con anterioridad a formular la demanda, no sólo porque las obras de urbanización de la zona ya fueron realizadas hace más de un año, y estaban a la vista de la demandante, sino también porque así lo alegamos en el acto de conciliación, pese a que el acta únicamente refleje que fue sin avenencia. Al respecto, queremos significar que incorporamos al acta de conciliación nuestras alegaciones escritas, que figuran en el expediente, donde se indicaba que se había expropiado una porción de finca, y al efecto esta parte anuncia que propondrá la prueba documental correspondiente que acreditará esta alegación. Para el caso que S.S.ª entendiera que se trata de un hecho de nueva noticia, nos oponemos asimismo a la pretensión ahora introducida, puesto que supone una alteración sustancial del objeto del proceso, de forma que el demandante debe hacer valer su derecho en un nuevo proceso declarativo, y no en éste cuyo objeto exclusivo era el ejercicio de la acción reivindicatoria.

Se tiene por formulado el hecho de nueva noticia, y a la vista del resultado de la prueba cuya proposición se anuncia por el demandado, se resolverá sobre la procedencia de tomarlo en consideración conforme dispone el art. 286.4 de la LEC.

========================================================================
