---
name: otrosi-pide-cese-provisional-actividad-proposicion-civ-1224
description: "Otrosí que pide el cese provisional de una actividad con proposición de prueba. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Otrosí que pide el cese provisional de una actividad con proposición de prueba

> Formulario **CIV-1224** del plugin **Medidas cautelares y diligencias preliminares** (`formularios-medidas-cautelares-civiles`) · Civil › Medidas cautelares y diligencias preliminares · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Otrosí que pide el cese provisional de una actividad con proposición de prueba» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Otrosí que pide el cese provisional de una actividad con proposición de prueba” para mi caso». También puedes invocarla directamente con `/formularios-medidas-cautelares-civiles:otrosi-pide-cese-provisional-actividad-proposicion-civ-1224`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-medidas-cautelares-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Medidas cautelares y diligencias preliminares) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (3 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] IMPORTE (2 veces)
- [ ] FECHA
- [ ] Nº DE PARCELA
- [ ] Nº DE POLÍGONO

## Normas que cita el formulario

- art. 727.7 LEC
- art. 732.2 LEC
- art. 723.1 LEC
- art. 721 LEC
- art. 733 LEC
- art. 728.2 LEC
- art. 728.1 LEC
- art. 727.7.ª LEC
- art. 732.3 LEC

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

OTROSÍ DIGO que, por medio del presente y al amparo de lo dispuesto en el artículo 727.7ª de la LEC, solicito la adopción de LA MEDIDA CAUTELAR DE CESE PROVISIONAL DE LA ACTIVIDAD DE CUSTODIA DE PERROS que llevan a cabo los demandados en las parcelas [Nº DE PARCELA] del polígono [Nº DE POLÍGONO] de [LOCALIDAD], absteniéndose de desarrollar una nueva actividad que pueda causar inmisiones en el domicilio de los actores en un radio de 500 metros, en base a los siguientes:

HECHOS

Que, tal como se ha relatado en la demanda, los actores están sufriendo una situación de grave trastorno psíquico y físico como consecuencia de las inmisiones procedentes de la actividad de custodia de perros realizada por los demandados, la cual puede considerarse ilícita, tal como se acredita por el informe pericial aportado como documento número [Nº DE DOCUMENTO], de donde se infiere claramente que se superan en exceso los niveles de ruido admitidos por las normas administrativas, especialmente en horario nocturno, que en todo caso son excesivos y gravemente molestos para los vecinos desde el punto de vista civil, habiéndose acreditado asimismo la ilicitud de la conducta que se imputa a los demandados, la cual aparece avalada por las órdenes administrativas dadas en orden al cese de la actividad denunciada, la última de ellas ratificada por la Sentencia del Tribunal Superior de Justicia de [LOCALIDAD], Sala de lo Contencioso-Administrativo, de fecha [FECHA], que se acompaña como documento número [Nº DE DOCUMENTO].

La injerencia de las inmisiones denunciadas, repetidas durante un largo período de tiempo, está alterando gravemente la convivencia personal y familiar en el ámbito privado del domicilio de mis representados, alteración que se incrementaría de no adoptarse la medida interesada, atendido el tiempo de duración del proceso, atendido el estado físico y psíquico en el que se encuentran mis representados como consecuencia de los ruidos continuos, según se acredita por el dictamen pericial que se acompaña como documento número [Nº DE DOCUMENTO], y como se acreditará oportunamente con la testifical que se propone de los vecinos de la finca colindante D. y D. [NOMBRE Y APELLIDOS], los cuales están sufriendo esta misma situación insostenible, al punto que de no adoptarse la medida solicitada se producirán gravísimos perjuicios para mis representados.

Para acreditar los anteriores hechos, y al amparo de lo que dispone el artículo 732.2 de la LEC, se acompañan a esta demanda los documentos en que esta parte funda su derecho, relacionados en los hechos de este otrosí, interesándose, además, la práctica de los siguientes medios probatorios en orden a justificar la concurrencia de los presupuestos para la adopción de la medida cautelar:

- TESTIFICAL, a fin de que se cite a D. [NOMBRE Y APELLIDOS] y a D. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], a efectos de que declaren sobre la concurrencia de los presupuestos para la adopción de la medida solicitada, en su condición de residentes en la finca colindante a la de mis representados y en la que se desarrolla la actividad de los demandados. Estos testigos comparecerán voluntariamente a la vista el día y hora que se señale.

A los anteriores hechos son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

Competencia

Le corresponde al Tribunal al que me dirijo ya que es aquel ante el que se ha presentado la demanda principal (art. 723.1 LEC).

Legitimación

Le corresponde a esta parte ante su condición de demandante en las presentes actuaciones (art. 721 LEC).

Procedimiento

Es el previsto en los arts. 733 y 734 LEC solicitando que la vista se celebre y la medida se adopte con la mayor urgencia dados los gravísimos perjuicios que están sufriendo mis representados.

Apariencia de buen derecho

Se deriva de la documentación adjunta a esta solicitud y en la que consta la ilicitud civil y administrativa de la actividad que están desarrollando los demandados (art. 728.2 LEC).

Peligro de mora

Se deriva de la grave alteración de la convivencia personal y familiar en el ámbito privado del domicilio de mis representados, y del estado físico y psíquico en el que se encuentran, tal como resuelta expuesto en los hechos de este otrosí, ya que solamente con la medida cautelar solicitada se podrá garantizar la efectividad de una eventual sentencia favorable que se pudiere dictar en beneficio de mi mandante (art. 728.1 LEC).

Medida interesada

Es la del cese provisional de la actividad de custodia de perros, absteniéndose de desarrollar una nueva actividad que pueda causar inmisiones en el domicilio del actor en un radio de 500 metros, fijada en el art. 727.7.ª de la LEC sobre las fincas propiedad de los demandados que se han relacionado en los hechos de este escrito.

Caución

Con fundamento en el art. 732.3 LEC se solicita sea fijada ésta en [IMPORTE] euros dadas las condiciones del crédito expuesto, la situación de los demandados y los posibles perjuicios que se les pudieren generar por ello.

En base a lo anterior,

SUPLICO AL TRIBUNAL: Que tenga por presentada la solicitud con los documentos acompañados y que, tras los trámites legales, incluida la práctica de la prueba que dejo interesada en el hecho tercero de este otrosí, acuerde el cese provisional de la actividad de custodia de perros sobre las fincas propiedad de los demandados que se han relacionado en los hechos de este escrito, absteniéndose de desarrollar una nueva actividad que pueda causar inmisiones en el domicilio de mis representados en un radio de 500 metros. De cara a la adopción de tal medida cautelar, se solicita asimismo que se tenga por ofrecida una caución de [IMPORTE] euros.

========================================================================
