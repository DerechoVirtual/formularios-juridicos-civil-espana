---
name: requerimiento-comprador-resolver-compraventa-inmueble-civ-0699
description: "Requerimiento del comprador para resolver la compraventa de inmueble e indemnizar daños y perjuicios. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Requerimiento del comprador para resolver la compraventa de inmueble e indemnizar daños y perjuicios

> Formulario **CIV-0699** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Requerimiento del comprador para resolver la compraventa de inmueble e indemnizar daños y perjuicios» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Requerimiento del comprador para resolver la compraventa de inmueble e indemnizar daños y perjuicios” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:requerimiento-comprador-resolver-compraventa-inmueble-civ-0699`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (6 veces)
- [ ] FECHA (4 veces)
- [ ] Nº DE CLÁUSULA (2 veces)
- [ ] AÑO
- [ ] DESCRIPCIÓN DEL BIEN
- [ ] DOMICILIO
- [ ] DÍA
- [ ] LUGAR
- [ ] MES
- [ ] NOMBRE Y APELLIDOS
- [ ] Nº
- [ ] PLAZO

## Normas que cita el formulario

- art. 1124 Código Civil

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

D. [NOMBRE Y APELLIDOS]

Domicilio [DOMICILIO]

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Muy Sr. Mío:

Me dirijo a Vd. en mi condición de comprador en el contrato de compraventa suscrito con Vd. como vendedor en fecha [FECHA], para la adquisición de la vivienda [DESCRIPCIÓN DEL BIEN], para comunicarle a todos los efectos, en aplicación de lo dispuesto en el artículo 1124 del Código Civil, mi voluntad de resolver de pleno derecho el citado contrato por haber incumplido Vd. grave e injustificadamente el plazo de entrega que habíamos pactado para el día [FECHA] en la cláusula [Nº DE CLÁUSULA] del citado contrato.

Este incumplimiento es esencial, ya que, tal como consta en la citada cláusula [Nº DE CLÁUSULA], el cumplimiento del plazo de entrega estaba condicionado al de la venta de mi anterior vivienda habitual, la cual a su vez me obligué a entregar el día [FECHA], de tal manera que, al haber llegado el día convenido sin que Vd. me haya entregado la vivienda, me he visto en la obligación de arrendar otra vivienda, con el pago de una renta arrendaticia de [IMPORTE] euros mensuales.

Por mi parte, se han cumplido escrupulosamente todas y cada una de las obligaciones asumidas en el citado contrato, habiendo entregado la cantidad de [IMPORTE] euros correspondientes a la entrada en el momento de suscribir el contrato privado y habiéndole requerido para que otorgara escritura y me entregara la vivienda adquirida según lo pactado hasta en dos ocasiones, una primera vencido el plazo de entrega y la segunda transcurridos treinta días desde el vencimiento, sin que haya recibido respuesta por parte de Vd.

En consecuencia, y en virtud de lo establecido en el citado artículo 1124 del Código Civil, mediante el presente escrito le comunico la resolución de pleno derecho del mencionado contrato de compraventa de vivienda de fecha [FECHA], reclamándole el resarcimiento de daños y perjuicios en cantidad total de [IMPORTE] euros, con más la que se devengue conforme a lo que expongo a continuación, y por los siguientes conceptos:

- la cantidad de [IMPORTE] euros, con más los intereses legales desde la entrega, en concepto de devolución de la cantidad entregada a la firma del contrato.

- la cantidad de [IMPORTE] euros correspondiente a [Nº] mensualidades de renta de la vivienda que me he visto en la obligación de arrendar por causa exclusiva del incumplimiento del plazo de entrega que habíamos pactado y que le es imputable a Vd.

- Y la cantidad que se devengue, a razón de [IMPORTE] euros mensuales, por las rentas arrendaticias que me vea obligado a satisfacer en caso de que Vd. no atienda este requerimiento.

De no atender el requerimiento en plazo de [PLAZO], sin más trámites, me veré en la obligación de iniciar las acciones que estime pertinentes en defensa de mis derechos.

Sin otro particular le saluda y queda a su disposición.

Firma del comprador
