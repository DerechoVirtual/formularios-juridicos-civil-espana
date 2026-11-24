---
name: recurso-apelacion-contra-auto-estima-oposicion-civ-1427
description: "Recurso de apelación contra el auto que estima la oposición por abusividad en ejecución hipotecaria. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Recurso de apelación contra el auto que estima la oposición por abusividad en ejecución hipotecaria

> Formulario **CIV-1427** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **recursos**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Recurso de apelación contra el auto que estima la oposición por abusividad en ejecución hipotecaria» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Recurso de apelación contra el auto que estima la oposición por abusividad en ejecución hipotecaria” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:recurso-apelacion-contra-auto-estima-oposicion-civ-1427`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (4 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] MES (3 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] Nº (2 veces)
- [ ] Nº DE CLÁUSULA (2 veces)
- [ ] ACTO O RESOLUCIÓN
- [ ] AÑO
- [ ] DESCRIBIR
- [ ] DÍA
- [ ] OTROS DATOS

## Normas que cita el formulario

- art. 695.4 LEC
- art. 693 LEC
- art. 693.2 LEC
- art. 24 Ley 5/2019

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

A LA AUDIENCIA PROVINCIAL DE [LOCALIDAD]

Don/Doña [NOMBRE Y APELLIDOS] Procurador/a de los Tribunales, actuando en nombre y representación de don/doña [NOMBRE Y APELLIDOS], como tengo debidamente acreditado en procedimiento ejecución hipotecaria /, seguido contra [ACTO O RESOLUCIÓN], y bajo la dirección Letrada de [NOMBRE Y APELLIDOS], ante la Sala comparezco y, como mejor proceda en derecho, DIGO:

1) Que esta parte ha sido notificada de la resolución dictada en forma de Auto de fecha [FECHA], notificada el siguiente día [FECHA], recaída en las presentes actuaciones [OTROS DATOS],y estimando la misma gravosa para los intereses de mi mandante, dicho sea en términos de defensa, dentro del plazo legalmente establecido y al amparo de lo establecido en el artículo 695.4 de la LEC, por medio del presente escrito INTERPONGO contra la misma RECURSO DE APELACIÓN para ante la Audiencia Provincial de [LOCALIDAD].

2) Que impugno concretamente el pronunciamiento relativo a [DESCRIBIR] a la denegación del despacho de ejecución por considerar que la cláusula [Nº DE CLÁUSULA] del contrato es abusiva y nula.

3) Que fundamento el recurso de apelación en las siguientes:

ALEGACIONES

PRIMERA.- Que el Auto recurrido dispone que la cláusula [Nº DE CLÁUSULA] del contrato de préstamo hipotecario es abusiva y nula por lo que se procede a denegar el despacho de ejecución.

La cláusula en cuestión contempla el vencimiento anticipado de la obligación en caso de impago del capital del préstamo hipotecario, concertado con el demandado persona física sobre vivienda, si bien el contrato se había suscrito antes de la reforma del artículo 693 de la LEC, operada por Ley 5/2019, de 15 de marzo.

Mi representada, tras la entrada en vigor de la Ley 5/2019, ha cumplido lo prescrito en el art. 24 de la citada Ley, a cuyo contenido se remite expresamente el art. 693.2 de la LEC, de manera que dio por vencido anticipadamente el préstamo hipotecario, que se encuentra en la [ELEGIR: primera / segunda] mitad de su duración, cuando el prestatario dejó de abonar los plazos comprendidos desde el mes de [MES] y hasta el mes de [MES], que superan las [Nº] mensualidades exigidas por el citado art. 24 de la Ley 5/2019. Asimismo, mi representada acompañó a la demanda el requerimiento notarial efectuado al deudor, con concesión de un mes para su cumplimiento, y con la advertencia de reclamación del total del préstamo en caso de impago.

Por tanto, se dan los requisitos del art. 24 de la Ley 5/2019 para que se produzca el vencimiento anticipado por cuanto que: a) el prestatario se encontraba en mora en el pago de una parte del capital del préstamo en los plazos indicados anteriormente; b) la cuantía de las cuotas vencidas y no satisfechas superaban las [Nº] mensualidades exigidas atendido que la mitad de duración en que se encuentra el préstamo expresado al momento del vencimiento anticipado; y c) mi representada requirió de pago el pasado día [FECHA] al prestatario concediéndole un plazo de un mes para su cumplimiento y advirtiéndole de que, de no ser atendido, se reclamaría el reembolso total adeudado del préstamo.

En consecuencia, la demanda que interpuso esta parte fue plenamente respetuosa con el vigente artículo 693 de la LEC, respetando lo establecido en el citado art. 24 de la Ley 5/2019, por lo que no puede apreciarse el carácter abusivo del vencimiento anticipado ejercitado por mi representada.

SEGUNDA.- Que a la vista de lo anteriormente expuesto, a esta parte le interpone el presente recurso de apelación contra el auto que acuerda el sobreseimiento de la ejecución hipotecaria de fecha [FECHA], interesando su revocación y, en su lugar, se acuerde continuar la ejecución despachada por los trámites legalmente prevenidos.

En su virtud,

SUPLICO A LA SALA: Que teniendo por presentado este escrito y por hechas las alegaciones en él contenidas, lo admita, y tenga por interpuesto el recurso de apelación contra el auto que acuerda el sobreseimiento de la ejecución hipotecaria de fecha [DÍA] de [MES] de [AÑO], en tiempo y forma, impugnando todos los pronunciamientos de la parte dispositiva, y previos los trámites pertinentes ordene la remisión de los autos a la Superioridad para que seguido el recurso por sus trámites, en su día dicte resolución revocando íntegramente la apelada y declare que no ha lugar al sobreseimiento de la ejecución hipotecaria por inexistencia de abusividad, acordando en su lugar continuar la ejecución despachada.

OTROSÍ DIGO que, de conformidad con lo dispuesto en los apartados 3.b) y 6 de la disposición adicional decimoquinta de la LOPJ acompaño a este escrito como documento número resguardo de consignación en la cuenta de Depósitos y Consignaciones abierta a nombre del Tribunal del depósito exigido para interponer el recurso por importe de 50 euros.

Es Justicia que insto en [LOCALIDAD]

Firma de Letrado Firma de Procurador

========================================================================
