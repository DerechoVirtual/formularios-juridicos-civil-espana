---
name: demanda-ordinaria-extinguir-derecho-arrendatario-sobre-civ-2423
description: "Demanda ordinaria para extinguir el derecho del arrendatario sobre una vivienda o local. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda ordinaria para extinguir el derecho del arrendatario sobre una vivienda o local

> Formulario **CIV-2423** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 25-11-2026.

## Qué es

Demanda de Juicio Declarativo Ordinario de cesación definitiva de las actividades ejercidas por el arrendatario y de extinción del contrato de arrendamiento urbano de vivienda o local, por la reiteración en el desarrollo de las actividades molestas, insalubre, peligrosas o ilícitas.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda ordinaria para extinguir el derecho del arrendatario sobre una vivienda o local» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda ordinaria para extinguir el derecho del arrendatario sobre una vivienda o local” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:demanda-ordinaria-extinguir-derecho-arrendatario-sobre-civ-2423`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- `SKILL.md` (este fichero): qué es el formulario, para qué sirve, cómo se usa, los datos que pide, las normas que cita, los avisos de actualización y las instrucciones para Claude.
- `assets/formulario.md`: el formulario seco, tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…]. Es el texto que se rellena; no lleva explicaciones.
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (17 veces)
- [ ] COMPLETAR (12 veces)
- [ ] FECHA (9 veces)
- [ ] CALLE (4 veces)
- [ ] NÚMERO (4 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] TELÉFONO (2 veces)
- [ ] FECHAS
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] PARTIDO JUDICIAL
- [ ] PISO
- [ ] ÓRGANO

## Normas que cita el formulario

- art. 36 LEC
- art. 45 LEC
- art. 52.1.8.º Ley 1/2000
- art. 23 LEC
- art. 249.1.8.º LEC
- art. 253.3 LEC
- art. 7.2 LPH
- art. 248.3 LEC
- art. 251 LEC
- art. 399.3 LEC
- art. 5 Ley Orgánica 1/2025
- art. 7.2 Ley 49/1960
- art. 394 LEC

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

- Al principio del formulario: La acción de cesación del art. 7.2 LPH no está exceptuada del requisito de procedibilidad (MASC) del art. 5 LO 1/2025.
- Al principio del formulario: Desde la LO 1/2025 el art. 7.3 LPH aplica el mismo cauce a las viviendas de uso turístico sin aprobación expresa de la comunidad.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Notas al pie del formulario original:
(1) El art. 7 de la Ley 49/1960, de 21 de julio de Propiedad Horizontal, ha sido dotado de nueva redacción a través del art. Cuarto de la Ley 8/1999, de 6 de abril (B.O.E. 8 de abril).

Al tratarse de un Juicio Declarativo Ordinario mediante el que se pretende la extinción del contrato de arrendamiento, le son aplicables las mismas particularidades comentadas para tal tipo de procesos en los formularios anteriores.

La determinación de la cuantía litigiosa en supuestos como el que se plantea en el formulario no es una cuestión precisamente sencilla, y bien podría sostenerse, inversamente a lo que se aduce en el formulario, que la cuantía debiera de fijarse conforme a las reglas 2.ª y 3.ª del art. 251 LEC 2000.

En cuanto a la medida cautelar de cesación existe la previsión específica de la misma en el art. 7.2 párrafo cuarto de la LPH 1960. Se trata de una norma de carácter especial que consideramos prevalece sobre la regulación general de las medidas cautelares contenida en el art. 721 y siguientes de la LEC 2000, si bien es cierto que medida semejante a la regulada en la LPH también podría obtenerse por la vía del art. 727.7.ª LEC 2000.

En relación a la cuantía, el R.D. 1417/2001, de 17 de diciembre (BOE de 27 de diciembre), solo convirtió a euros las cuantías originales de la LEC; los límites vigentes resultan de los arts. 249.2 y 250.2 LEC (15.000 euros).


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
