---
name: oposicion-recurso-casacion-peticion-vista-civ-1324
description: "Oposición al recurso de casación con petición de vista. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Oposición al recurso de casación con petición de vista

> Formulario **CIV-1324** del plugin **Recursos civiles: reposición, apelación, casación y queja** (`formularios-recursos-civiles`) · Civil › Recursos · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Oposición al recurso de casación con petición de vista» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Oposición al recurso de casación con petición de vista” para mi caso». También puedes invocarla directamente con `/formularios-recursos-civiles:oposicion-recurso-casacion-peticion-vista-civ-1324`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-recursos-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Recursos civiles: reposición, apelación, casación y queja) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] Nº DE PROCEDIMIENTO (2 veces)
- [ ] NOMBRE DE LA PARTE
- [ ] ÓRGANO O PERSONA

## Normas que cita el formulario

- art. 477.1 LEC
- art. 485 LEC

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

Rollo [Nº DE PROCEDIMIENTO]

A LA SALA PRIMERA DEL TRIBUNAL SUPREMO

D. [NOMBRE Y APELLIDOS], Procurador de los Tribunales, en nombre y representación de D. [NOMBRE Y APELLIDOS], parte recurrida en el recurso de casación seguido ante la Sala con el número de Rollo [Nº DE PROCEDIMIENTO], ante la Excma. Sala comparezco y como mejor proceda en derecho DIGO:

1) Que en fecha [FECHA] se ha conferido traslado a esta parte del escrito de interposición del recurso de casación deducido por [NOMBRE DE LA PARTE] contra la sentencia de fecha [FECHA] dictada por la Audiencia Provincial de

2) Que evacuando el traslado conferido, por medio del presente escrito nos oponemos al recurso, en base a los siguientes

Motivos de oposición

PRIMERO.- En relación al correlativo primero del escrito de interposición del recurso de casación, el recurrente funda su recurso en la indebida aplicación del art. 42 del Estatuto de los Trabajadores al caso de autos, precepto éste que no puede fundar el recurso de casación en materia civil, ni tan siquiera ha sido aplicado en la sentencia recurrida.

El Alto Tribunal al que nos dirigimos ha reiterado que El recurso de casación por infracción de ley sólo puede fundarse en normas de Derecho sustantivo o material, no adjetivo o formal [SSTS 25 de octubre de 1990 ; 18 de febrero de 2003, rec. 3262/1997]. Dentro de esta categoría, también ha subrayado que para ser alegada como infringida una norma en casación civil es necesario que la misma sea una norma de derecho privado con categoría de ley o asimilada o complementaria de la misma (SSTS 2 de octubre de 1999, Rec. 149/1995; 20 de octubre de 1999, rec. 386/1995). Y, por último, en cuanto a su naturaleza, ha indicado que no cabe alegar la infracción de normas laborales como fundamento de un motivo de casación al cobijo del artículo 477.1 de la LEC [STS de 18 de febrero de 1993 ; 4 de marzo de 2002, rec. 3153/1996]. Esta doctrina jurisprudencial ha sido reiterada en el punto 3.3.d) del apartado III del Acuerdo del Pleno de la Sala Primera de 27 de enero de 2017 donde expresamente se establece que el recurso de casación civil no puede fundarse en normas administrativas, penales o laborales que no se pongan en relación con una norma civil, como en este supuesto.

En este caso, el recurrente alega la infracción del art. 42 del Estatuto de los Trabajadores, que no puede amparar el motivo, pero es que, además, en cuanto al fondo, tampoco resulta infringido pues la responsabilidad del recurrente surge de las normas civiles del arrendamiento de obra, específicas y correctamente aplicadas en las dos sentencias del Tribunal de Instancia y de la Audiencia, y no del hecho de la contratación de la actividad empresarial.

Por tanto, solicitamos la desestimación del motivo.

SEGUNDO.- (Se relacionarían correlativamente los otros motivos de oposición)

En base a lo anterior,

SUPLICO A LA SALA que tenga por presentado este escrito, con certificación de traslado y, en su virtud, desestime el recurso de casación interpuesto por [ÓRGANO O PERSONA] por los motivos expuestos, con imposición de costas al recurrente.

OTROSÍ DIGO que, al amparo de lo establecido en el art. 485 de la LEC, esta parte solicita la celebración de vista para la sustanciación del recurso, pues la misma es necesaria en aras a la resolución de la casación, atendida la complejidad de la cuestión sometida a debate, lo que hace exigible una exposición detallada al tribunal de las posiciones de las partes.

Por lo expuesto, SUPLICO A LA SALA que acuerde la celebración de vista en este recurso.

En L. y F.

(Firma Procurador y Abogado)

========================================================================
