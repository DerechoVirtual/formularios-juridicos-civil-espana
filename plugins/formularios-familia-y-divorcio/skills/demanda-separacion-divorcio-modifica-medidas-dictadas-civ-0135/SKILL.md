---
name: demanda-separacion-divorcio-modifica-medidas-dictadas-civ-0135
description: "Demanda de separación o divorcio que modifica las medidas dictadas por Violencia sobre la Mujer. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de separación o divorcio que modifica las medidas dictadas por Violencia sobre la Mujer

> Formulario **CIV-0135** del plugin **Familia: separación, divorcio y medidas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 25-11-2026.

## Qué es

Demanda de separación o divorcio presentada por la víctima ante la Sección de Violencia sobre la Mujer del Tribunal de Instancia que ya dictó una orden de protección, en la que se pide modificar las medidas civiles acordadas en ella (art. 544 ter LECrim) y se proponen las medidas provisionales y definitivas.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de separación o divorcio que modifica las medidas dictadas por Violencia sobre la Mujer» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de separación o divorcio que modifica las medidas dictadas por Violencia sobre la Mujer” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-separacion-divorcio-modifica-medidas-dictadas-civ-0135`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- `SKILL.md` (este fichero): qué es el formulario, para qué sirve, cómo se usa, los datos que pide, las normas que cita, los avisos de actualización y las instrucciones para Claude.
- `assets/formulario.md`: el formulario seco, tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…]. Es el texto que se rellena; no lleva explicaciones.
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: separación, divorcio y medidas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] AÑO (6 veces)
- [ ] DÍA (6 veces)
- [ ] MES (6 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] DETALLE Y JUSTIFICACIÓN DE SU PROCEDENCIA (4 veces)
- [ ] DOMICILIO (3 veces)
- [ ] SEDE (3 veces)
- [ ] NOMBRE Y APELLIDOS DE LA DEMANDANTE (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL DEMANDADO (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL HIJO/A (2 veces)
- [ ] COLEGIO DE ABOGADOS
- [ ] DETALLE DE LOS HECHOS
- [ ] DETALLE DE TODAS LAS MEDIDAS QUE SE SOLICITAN CON CARÁCTER DEFINITIVO
- [ ] NOMBRE Y APELLIDOS DEL LETRADO
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] Nº
- [ ] Nº DE DOCUMENTO
- [ ] PROFESIÓN
- [ ] RELACIÓN DE DOCUMENTOS

## Normas que cita el formulario

- art. 81 Código Civil
- art. 86 Código Civil
- art. 91 Código Civil
- art. 158 Código Civil

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

### Avisos de actualización (3) — se aplican en el texto, nunca se copian en el documento

- Junto a «…isionales previas, al amparo del artículo 772 de la Ley de Enjuiciamiento Civil.»: comprobar el reparto competencial vigente entre las Secciones de Violencia sobre la Mujer y las Secciones de Familia, Infancia y Capacidad conforme a la LO 1/2025 y a la normativa de violencia de género aplicable en la sede de que se trate.
- Junto a «…os procesos derivados de crisis familiares en casos de violencia sobre la mujer.»: comprobar la cita del art. 89.9 LOPJ y el art. 5.2 de la LO 1/2025 en la redacción vigente, por si ha variado la numeración.
- Junto a «…s o dejadas sin efecto por el Juez de primera instancia que resulte competente."»: el texto transcrito del art. 544 ter.7 LECrim y la terminología («capacidad judicialmente modificada», «Juez de primera instancia») deben contrastarse con la redacción vigente tras la Ley 8/2021 y la LO 1/2025.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

- Ninguna.

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
