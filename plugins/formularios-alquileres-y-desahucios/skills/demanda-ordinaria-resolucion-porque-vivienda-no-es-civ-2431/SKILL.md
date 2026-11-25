---
name: demanda-ordinaria-resolucion-porque-vivienda-no-es-civ-2431
description: "Demanda ordinaria de resolución porque la vivienda no es la residencia permanente del inquilino. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda ordinaria de resolución porque la vivienda no es la residencia permanente del inquilino

> Formulario **CIV-2431** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 25-11-2026.

## Qué es

Demanda de juicio declarativo ordinario con la que el arrendador pide la resolución del contrato de arrendamiento de vivienda porque esta ha dejado de destinarse a satisfacer la necesidad de vivienda del arrendatario (está desocupada y con signos de abandono), causa de resolución de pleno derecho del art. 27.2.f) de la Ley 29/1994, de Arrendamientos Urbanos.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda ordinaria de resolución porque la vivienda no es la residencia permanente del inquilino» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda ordinaria de resolución porque la vivienda no es la residencia permanente del inquilino” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:demanda-ordinaria-resolucion-porque-vivienda-no-es-civ-2431`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- `SKILL.md` (este fichero): qué es el formulario, para qué sirve, cómo se usa, los datos que pide, las normas que cita, los avisos de actualización y las instrucciones para Claude.
- `assets/formulario.md`: el formulario seco, tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…]. Es el texto que se rellena; no lleva explicaciones.
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (14 veces)
- [ ] LOCALIDAD (12 veces)
- [ ] FECHA (6 veces)
- [ ] NOMBRE Y APELLIDOS DEL DEMANDADO/A (5 veces)
- [ ] CALLE (3 veces)
- [ ] NOMBRE Y APELLIDOS DEL DEMANDANTE (3 veces)
- [ ] TELÉFONO (3 veces)
- [ ] AÑO (2 veces)
- [ ] CORREO ELECTRÓNICO (2 veces)
- [ ] DNI/NIE (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] MES (2 veces)
- [ ] NOMBRE DEL NOTARIO (2 veces)
- [ ] PISO (2 veces)
- [ ] SEDE (2 veces)
- [ ] COLEGIO
- [ ] DENOMINACIÓN DE LAS COMPAÑÍAS SUMINISTRADORAS
- [ ] DESCRIPCIÓN DEL TÍTULO DE PROPIEDAD
- [ ] DOMICILIO ACTUAL DEL DEMANDADO
- [ ] DOMICILIO LABORAL
- [ ] DOMICILIO PROFESIONAL
- [ ] DÍA
- [ ] FECHAS
- [ ] NOMBRE DEL ABOGADO/A
- [ ] NOMBRE DEL PROCURADOR/A
- [ ] NOMBRE Y APELLIDOS DEL ABOGADO/A
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] Nº DE COLEGIADO
- [ ] Nº DE FAX
- [ ] Nº DE PROTOCOLO
- [ ] OFICINA JUDICIAL

## Normas que cita el formulario

- art. 24.1 LEC
- art. 399.1 LEC
- art. 299.2 LEC
- art. 265.2 LEC
- art. 27.2.f Ley 29/1994
- art. 36 LEC
- art. 45 LEC
- art. 52.1.7.º LEC
- art. 23 LEC
- art. 249.1.6.º LEC
- art. 253 LEC
- art. 251 LEC
- art. 5 Ley Orgánica 1/2025
- art. 2.1 Ley 29/1994
- art. 394 LEC
- art. 24.2 LEC
- art. 155.3 LEC

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

- Al principio del formulario: Se mantiene la nota sobre la redacción de los arts. 2.1, 7 y 27.2.f) LAU dada por el RDL 29/2026: la aplicable depende de la fecha del contrato.
- Junto a «… LEC. Son de aplicación, por tanto, los artículos 399 y siguientes de dicha Ley.»: en su redacción vigente, el art. 249.1.6.º LEC exceptúa también los asuntos arrendaticios en los que sea posible valorar la cuantía del objeto del procedimiento, que siguen el cauce que corresponda según las reglas generales (juicio verbal si la cuantía no excede de 15.000 euros, art. 250.2 LEC; juicio ordinario si la excede, art. 249.2 LEC). Comprobar el cauce procedente a la vista de la cuantía fijada en el fundamento VI.
- Junto a «… sigue que ha de ponerse fin al contrato de arrendamiento formalizado en su día.»: la redacción vigente de los arts. 2.1, 7 y 27.2.f) LAU, dada por el Real Decreto-ley 29/2026 (en vigor desde el 8 de octubre de 2026), habla de «necesidad de vivienda» y de «vivienda habitual», sin el adjetivo «permanente» que empleaba la redacción anterior; comprobar la redacción aplicable al contrato según su fecha y el régimen transitorio de dicha norma.

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
