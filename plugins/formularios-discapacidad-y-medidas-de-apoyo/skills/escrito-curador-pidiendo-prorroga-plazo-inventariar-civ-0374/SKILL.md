---
name: escrito-curador-pidiendo-prorroga-plazo-inventariar-civ-0374
description: "Escrito del curador pidiendo prórroga del plazo para inventariar los bienes del curatelado. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito del curador pidiendo prórroga del plazo para inventariar los bienes del curatelado

> Formulario **CIV-0374** del plugin **Discapacidad y medidas de apoyo (Ley 8/2021)** (`formularios-discapacidad-y-medidas-de-apoyo`) · Civil › Capacidad y medidas de apoyo · normativa revisada el 24-11-2026.

## Qué es

Escrito, dentro del expediente de jurisdicción voluntaria de la curatela, por el que el curador con facultades representativas solicita prórroga del plazo fijado para formar el inventario de los bienes de la persona sujeta a curatela, alegando una causa justificada (arts. 285 CC y 47 LJV).

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito del curador pidiendo prórroga del plazo para inventariar los bienes del curatelado» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito del curador pidiendo prórroga del plazo para inventariar los bienes del curatelado” para mi caso». También puedes invocarla directamente con `/formularios-discapacidad-y-medidas-de-apoyo:escrito-curador-pidiendo-prorroga-plazo-inventariar-civ-0374`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-discapacidad-y-medidas-de-apoyo:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Discapacidad y medidas de apoyo (Ley 8/2021)) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] AÑO (4 veces)
- [ ] DÍA (4 veces)
- [ ] MES (4 veces)
- [ ] Nº (4 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] NOMBRE Y APELLIDOS DE LA PERSONA SUJETA A CURATELA (2 veces)
- [ ] O DE FAMILIA, INFANCIA Y CAPACIDAD (2 veces)
- [ ] SEDE (2 veces)
- [ ] DNI/NIF
- [ ] DOMICILIO
- [ ] NOMBRE Y APELLIDOS
- [ ] NOMBRE Y APELLIDOS DEL CURADOR
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] Nº DE PROCEDIMIENTO
- [ ] PLAZO

## Normas que cita el formulario

- art. 285 Código Civil

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

- Junto a «…argo de los bienes de la persona en cuyo apoyo se haya establecido la curatela".»: el original citaba los apartados del art. 285 CC en numeración romana; comprobar su numeración y redacción vigentes antes de presentar.

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

SECCIÓN CIVIL [O DE FAMILIA, INFANCIA Y CAPACIDAD] DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

Expediente de Jurisdicción Voluntaria n.º [Nº DE PROCEDIMIENTO]

A LA SECCIÓN CIVIL [O DE FAMILIA, INFANCIA Y CAPACIDAD] DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

D./Dª [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, y de D./Dª [NOMBRE Y APELLIDOS DEL CURADOR], mayor de edad, con DNI/NIF [DNI/NIF] y domicilio en [DOMICILIO], como curador de D./Dª [NOMBRE Y APELLIDOS DE LA PERSONA SUJETA A CURATELA], ante el Tribunal comparezco y, como mejor proceda en Derecho,

DIGO:

Que por medio del presente escrito, con base en lo dispuesto en el art. 285 del Código Civil, SOLICITO PRÓRROGA DEL PLAZO FIJADO PARA REALIZAR EL INVENTARIO DE LOS BIENES DE LA PERSONA SUJETA A CURATELA, conforme a los siguientes

HECHOS

PRIMERO.- Fui nombrado curador con facultades representativas de D./Dª [NOMBRE Y APELLIDOS DE LA PERSONA SUJETA A CURATELA] por este Tribunal, por auto de fecha [DÍA] de [MES] de [AÑO], aceptando el cargo por acta de fecha [DÍA] de [MES] de [AÑO], tras lo cual se me dio posesión del mismo.

SEGUNDO.- Por resolución dictada el día [DÍA] de [MES] de [AÑO] fui requerido para la aportación del inventario de los bienes de la persona sujeta a curatela en el plazo máximo de [PLAZO] días.

TERCERO.- Encontrándose a punto de vencer el plazo para realizar el inventario, he tenido conocimiento, [MEDIO DE CONOCIMIENTO: p. ej., a través de una conversación telefónica mantenida con D./Dª [NOMBRE Y APELLIDOS], vecino/a de [LOCALIDAD]], localidad en que se halla ubicado [DESCRIPCIÓN DEL BIEN: p. ej., una antigua casa propiedad de la persona sujeta a curatela por haberla heredado de su padre], de los siguientes hechos: [DESCRIPCIÓN DE LOS HECHOS QUE JUSTIFICAN LA PRÓRROGA: p. ej., que en dicho inmueble podrían encontrarse diversos objetos de valor ocultos en una habitación, cuyo acceso podría pasar desapercibido a quienes no conocieran bien la casa].

CAUSA DE LA SOLICITUD.- Con el fin de comprobar la información recibida y completar, en su caso, el inventario, es conveniente que me traslade a [LOCALIDAD] y lo inspeccione personalmente, para lo cual necesito disponer de no menos de [Nº] días, lo que alego como causa en la que sustento mi solicitud de prórroga del plazo para realizar el inventario.

CUARTO.- En el caso de encontrarse los objetos valiosos a los que alude la información recibida y a la vista de sus características, es posible que los mismos no deban quedar en mi poder, sino que deban ser depositados en un establecimiento destinado a este efecto, conforme a lo dispuesto en el art. 285 del Código Civil.

Son aplicables a los hechos expuestos los siguientes

FUNDAMENTOS DE DERECHO

I.- Los apartados I y III del art. 285 del Código Civil, que regulan el plazo para hacer inventario de los bienes de la persona sujeta a curatela y la posibilidad de prórroga del mismo.

II.- El apartado IV del art. 285 del Código Civil, que dispone: "El dinero, alhajas, objetos preciosos y valores mobiliarios o documentos que, a juicio del Letrado de la Administración de Justicia, no deban quedar en poder del curador serán depositados en un establecimiento destinado a este efecto", añadiendo el apartado V del mismo artículo que "Los gastos que las anteriores medidas ocasionen correrán a cargo de los bienes de la persona en cuyo apoyo se haya establecido la curatela".

III.- El art. 47 de la Ley de la Jurisdicción Voluntaria, relativo a los trámites procesales relativos a la formación de inventario.

IV.- Iura novit curia y los demás que resulten procedentes.

En virtud de lo expuesto,

SUPLICO AL TRIBUNAL: Que, teniendo por presentado este escrito, se sirva admitirlo y, estimando lo que en él se solicita, acuerde el Letrado de la Administración de Justicia la prórroga del plazo inicialmente señalado para realizar el inventario de los bienes de la persona sujeta a curatela por [Nº] días adicionales, o los que considere convenientes a la vista de los hechos expuestos.

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma y número de colegiado del Letrado Firma del Procurador
