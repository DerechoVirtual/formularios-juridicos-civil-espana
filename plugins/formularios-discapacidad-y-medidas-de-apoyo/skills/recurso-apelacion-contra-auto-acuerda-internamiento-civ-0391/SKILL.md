---
name: recurso-apelacion-contra-auto-acuerda-internamiento-civ-0391
description: "Recurso de apelación contra el auto que acuerda el internamiento. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Recurso de apelación contra el auto que acuerda el internamiento

> Formulario **CIV-0391** del plugin **Discapacidad y medidas de apoyo (Ley 8/2021)** (`formularios-discapacidad-y-medidas-de-apoyo`) · Civil › Capacidad y medidas de apoyo · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **recursos**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Recurso de apelación contra el auto que acuerda el internamiento» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Recurso de apelación contra el auto que acuerda el internamiento” para mi caso». También puedes invocarla directamente con `/formularios-discapacidad-y-medidas-de-apoyo:recurso-apelacion-contra-auto-acuerda-internamiento-civ-0391`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-discapacidad-y-medidas-de-apoyo:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Discapacidad y medidas de apoyo (Ley 8/2021)) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (10 veces)
- [ ] FECHA (4 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] MOTIVO (2 veces)
- [ ] Nº (2 veces)
- [ ] TIPO DE PRUEBA (2 veces)
- [ ] LUGAR Y FECHA
- [ ] MEDIOS DE PRUEBA
- [ ] NOMBRE DEL HOSPITAL
- [ ] SUPUESTO DEL ART. 270 LEC

## Normas que cita el formulario

- art. 394.1 LEC
- art. 270 LEC

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

Don [NOMBRE Y APELLIDOS], Procurador de los Tribunales, actuando en nombre y representación de Don [NOMBRE Y APELLIDOS], según consta acreditado en autos, ante la Sección Civil de la Audiencia Provincial de [LOCALIDAD] comparezco y, como mejor proceda en Derecho, DIGO:

Que a través del presente escrito, y en virtud del traslado conferido por providencia de fecha [FECHA] por la que se tenía por interpuesto el recurso de apelación, interpongo en tiempo y forma RECURSO DE APELACIÓN contra el auto de fecha [FECHA] en virtud del cual se autoriza el internamiento de Don [NOMBRE Y APELLIDOS], en procedimiento /, el cual baso en las siguientes

ALEGACIONES

PRIMERA.- Esta representación entiende, dicho sea con los debidos respetos y en estrictos términos de defensa, que la resolución recurrida no es ajustada a derecho y ello en virtud de los motivos que a continuación se expondrán.

SEGUNDA.- En contra de lo manifestado por el solicitante del internamiento, no existe un diagnóstico de esquizofrenia residual crónica, sino otro totalmente distinto. El solicitante ha utilizado una valoración médica que prescindió totalmente de los antecedentes clínicos del paciente, y que tuvo lugar cuando la misma fue ingresada en el Hospital [NOMBRE DEL HOSPITAL]. Sin embargo, quien pretende el internamiento olvida decir que el diagnóstico fue modificado cuando los facultativos dispusieron del historial médico de la paciente, y el tiempo de ingreso permitió un estudio clínico en profundidad, así como advertir que el día de ingreso Don [NOMBRE Y APELLIDOS] sufría los efectos de una intoxicación alcohólica, mezclada con diferentes fármacos en dosis nocivas.

A efectos probatorios se acompañan antecedentes clínicos como Documento núm. [Nº], diagnóstico realizado con posterioridad a la vista de los antecedentes clínicos como Documento núm. [Nº DE DOCUMENTO].

TERCERA.- En fecha [FECHA] el médico psiquiatra Don [NOMBRE Y APELLIDOS] ha diagnosticado que Don [NOMBRE Y APELLIDOS] sufre una psicosis afectiva bipolar recurrente, que corresponde a la antigua psicosis maníaco depresiva, excluyendo la demencia orgánica. A efectos probatorios se acompaña el citado informe psiquiátrico como Documento núm. [Nº DE DOCUMENTO].

La naturaleza de esta enfermedad entraña la reversibilidad completa entre las dos fases y también la posibilidad de su repetición. En el informe psiquiátrico aportado con este escrito, el médico informante indica que, en la actualidad, han desaparecido los síntomas de la enfermedad. Se trata de una total recuperación de las capacidades mentales volitivas de mi representado, siendo en este tiempo totalmente capaz para regir tanto su persona como sus bienes. La reiteración de los episodios sufridos en el pasado, sean depresivos o maníacos, no es imposible, pero sí muy poco probable, sobre todo a la vista de que el interno cumple con las prescripciones médicas, habiendo comprendido la enfermedad que padece. Una vez dado de alta en el Hospital arriba citado no se han repetido los hechos que narra el solicitante del internamiento. Los mismos son ciertos, pero también anteriores al aludido ingreso y tratamiento de recuperación realizado. Es menester continuar con las pruebas analíticas de los niveles de litio cada seis meses para garantizar la adecuada toma y absorción, a la vez que resulta aconsejable la revisión médica mensual, o en un menor período de tiempo cuando lleguen los cambios de estación.

Mientras este tratamiento tenga lugar, como ocurre en el presente, la vida del paciente sólo resultaría perjudicada con medidas más agresivas, como lo es la privación de libertad en un centro de sanidad mental.

CUARTA.- A mayor abundamiento, Don [NOMBRE Y APELLIDOS] ha solicitado en fechas recientes nuevos informes psiquiátricos, que han sido expedidos y certificados por los Doctores Don [NOMBRE Y APELLIDOS] y Don [NOMBRE Y APELLIDOS], de reconocido prestigio en el campo de la salud mental, que corroboran lo más arriba indicado, que en prueba de lo manifestado se acompañan como Documentos núms. y [Nº DE DOCUMENTO], respectivamente.

QUINTA.- A la vista del relato fáctico realizado, es innecesario proceder al internamiento que se pretende, y por consiguiente resulta preciso denegar la autorización judicial requerida por el solicitante, a quien deben imponerse las costas procesales causadas en este procedimiento, de conformidad con el criterio del vencimiento regulado en el artículo 394.1 LEC.

SEXTA.- Al amparo de lo prevenido en el artículo 460.1 de la Ley de Enjuiciamiento Civil, se solicita que los documentos acompañados al presente escrito de interposición del recurso de apelación sean admitidos por encontrarse en los casos previstos en el artículo 270 LEC, en concreto [SUPUESTO DEL ART. 270 LEC].

SÉPTIMA.- Asimismo y al amparo de lo prevenido en el artículo 460.2 de la Ley de Enjuiciamiento Civil, se solicita se reciba el pleito a prueba en esta segunda instancia, para la práctica de los medios de prueba siguientes:

[MEDIOS DE PRUEBA]

En su virtud,

SUPLICO A LA SALA: Que habiendo por presentado este escrito con las manifestaciones en él contenidas y sus copias, se sirva admitirlo, lo una a los autos de su razón y en sus méritos tenga por interpuesto en tiempo y forma RECURSO DE APELACIÓN, en su día preparado, contra el Auto de internamiento de fecha [FECHA] y previos los trámites legales oportunos, acuerde la remisión de los autos a la Superioridad, para que seguido el recurso por todos sus trámites, en su día se dicte la pertinente resolución en virtud de la cual se estime íntegramente el presente recurso de apelación y se revoque el Auto ahora recurrido estimando íntegramente las alegaciones invocadas por esta representación, y en consecuencia declare ser innecesario proceder al internamiento de [NOMBRE Y APELLIDOS], así como la autorización judicial requerida por el solicitante, imponiendo las costas causadas en este procedimiento a quien solicitó el internamiento no voluntario de mi mandante, de conformidad con el criterio del vencimiento regulado en el artículo 394.1 LEC, con todos los pronunciamientos favorables que le son inherentes.

OTROSÍ DIGO I: Que al amparo de lo dispuesto en el artículo 460 de la Ley de Enjuiciamiento Civil se acompaña como documento núm. [Nº], por [MOTIVO], y asimismo se solicita la práctica de la prueba [TIPO DE PRUEBA], por [MOTIVO].

Por lo que,

A LA SALA SOLICITO: Que se tenga por propuesto el medio de prueba de que intenta valerse esta parte, se declare procedente, otorgándose el recibimiento a prueba en la segunda instancia para su práctica, remitiéndose el oportuno exhorto para la práctica de la prueba [TIPO DE PRUEBA].

Otrosí digo II

OTROSÍ DIGO II: Que interesa al derecho de esta parte la celebración de vista pública.

Por lo que,

AL TRIBUNAL SOLICITO: Que acuerde de conformidad con lo interesado.

Es justicia que insto en [LUGAR Y FECHA].

Firmas de Letrado y Procurador

========================================================================
