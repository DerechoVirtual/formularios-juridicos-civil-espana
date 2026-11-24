---
name: recurso-reposicion-contra-auto-deniega-despachar-civ-1501
description: "Recurso de reposición contra el auto que deniega despachar ejecución de un laudo arbitral. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Recurso de reposición contra el auto que deniega despachar ejecución de un laudo arbitral

> Formulario **CIV-1501** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Recurso de reposición del ejecutante contra el auto que deniega parcialmente el despacho de ejecución de un laudo arbitral por no incluir las costas del arbitraje impuestas en el propio laudo, alegando que forman parte de la cantidad líquida por la que procede despachar ejecución (arts. 517.2, 552 y 555.2 LEC y arts. 37.6 y 44 de la Ley 60/2003, de Arbitraje). Incluye otrosí de consignación del depósito para recurrir (formulario adaptado a la reforma procesal de la LO 1/2025).

Es un modelo de tipo **recursos**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Recurso de reposición contra el auto que deniega despachar ejecución de un laudo arbitral» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Recurso de reposición contra el auto que deniega despachar ejecución de un laudo arbitral” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:recurso-reposicion-contra-auto-deniega-despachar-civ-1501`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (5 veces)
- [ ] FECHA (2 veces)
- [ ] AÑO
- [ ] DÍA
- [ ] IMPORTE: 25
- [ ] LOCALIDAD
- [ ] MES
- [ ] NOMBRE Y APELLIDOS
- [ ] NOMBRE Y APELLIDOS O DENOMINACIÓN SOCIAL
- [ ] Nº
- [ ] Nº DE PROCEDIMIENTO
- [ ] SEDE

## Normas que cita el formulario

- art. 451 LEC
- art. 37.6 Ley 60/2003
- art. 72 LEC
- art. 575.1 LEC
- art. 555.2 LEC

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

- Junto a «…DIMIENTO] A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…ferenciados, ante el Tribunal comparezco y, como mejor proceda en derecho, DIGO:»: el original decía «parte demandante en los autos de proceso ordinario», lo que no concuerda con un proceso de ejecución; se ha corregido a «parte ejecutante».
- Junto a «…depósito exigido para interponer el recurso, por importe de [IMPORTE: 25] euros.»: comprobar que el importe del depósito y los apartados de la disposición adicional decimoquinta de la LOPJ siguen vigentes en la fecha de presentación y, en su caso, si el recurrente está exento.

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

PROCESO DE EJECUCIÓN NÚMERO [Nº DE PROCEDIMIENTO]

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

D./Dª [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales y de [NOMBRE Y APELLIDOS O DENOMINACIÓN SOCIAL], parte ejecutante en los autos de ejecución arriba referenciados, ante el Tribunal comparezco y, como mejor proceda en derecho, DIGO:

Que habiéndose notificado a esta representación auto de fecha [FECHA] por el que se deniega parcialmente el despacho de ejecución del laudo arbitral interesada en nuestra demanda, mediante el presente escrito, al amparo del artículo 552 en relación con los artículos 451 y 452 de la LEC, interpongo RECURSO DE REPOSICIÓN contra el citado auto, citando como infringidos los artículos 517.2 y 555.2 de la Ley de Enjuiciamiento Civil en relación con los artículos 37.6 y 44 de la Ley 60/2003, de Arbitraje, en base a los siguientes motivos:

PRIMERO.– El auto recurrido deniega parcialmente el despacho de ejecución, al no incluir la cantidad correspondiente a las costas incluidas en el laudo arbitral cuya ejecución se pretende.

En efecto, el laudo arbitral, en el pronunciamiento primero, condena al ejecutado a que abone a mi representado la cantidad de [IMPORTE] euros, en concepto de daños y perjuicios causados por el incumplimiento contractual, en tanto que en el pronunciamiento segundo literalmente se dispone: «SEGUNDO.– Asimismo se imponen las costas del presente procedimiento arbitral al demandado por un total de [IMPORTE] euros, que deberá abonar a la parte demandante».

Por tanto, la cantidad por la que se debe despachar ejecución es la de [IMPORTE] euros, correspondiente a la suma del principal y de los gastos y costas del arbitraje, por cuanto que el laudo arbitral condena expresamente al ejecutado a una cantidad dineraria determinada como derivada de lo estipulado en el propio Convenio Arbitral y en el artículo 37.6 de la Ley 60/2003, de Arbitraje.

La interpretación de las Audiencias Provinciales viene aceptando pacíficamente que los gastos y costas del arbitraje se integran en la cantidad por la que debe despacharse ejecución; así, el AAP Madrid de 18 de mayo de 2006 (recurso número 71/2006) indica que, del tenor literal del artículo 44 de la Ley de Arbitraje, en relación con los artículos 72, 517 y 552 de la LEC, ha de considerarse que las costas del arbitraje deben incluirse en el principal de lo reclamado en el despacho de ejecución, al margen de lo presupuestado para las costas e intereses del proceso de ejecución, donde ha de tomarse como límite el preceptuado en el artículo 575.1 de la LEC; en el mismo sentido, el AAP Madrid, Sección 11.ª, de 22 de octubre de 2006, rec. 481/2006, afirma que los gastos del arbitraje están sujetos al régimen del artículo 37.6 de la Ley de Arbitraje y por ello constituyen un pronunciamiento integrado en el fondo, que queda fuera de la verificación meramente formal del laudo que debe realizar el Juez antes de despachar la ejecución, pues establece dicho precepto que, con sujeción a lo acordado por las partes, los árbitros se pronunciarán en el laudo sobre las costas del arbitraje, que incluirán los honorarios y gastos de los árbitros y, en su caso, los honorarios y gastos de los defensores o representantes de las partes, el coste del servicio prestado por la institución administradora del arbitraje y los demás gastos originados en el procedimiento arbitral, de donde nace la legitimación del ejecutante para despachar ejecución a su favor por las cantidades reseñadas en el laudo, por ser la titular del derecho declarado, como consta en la parte dispositiva del laudo.

También en este caso, en el laudo cuya ejecución se pretende existen dos pronunciamientos de condena dineraria, ambos a favor de la parte ejecutante, el principal y el de reintegro de gastos y costas, como beneficiaria del mismo, tal y como autoriza el artículo 37.6 de la Ley 60/2003, de 23 de diciembre, de Arbitraje. De conformidad con lo dispuesto en el artículo 72 de la Ley de Enjuiciamiento Civil, es factible la acumulación subjetiva de acciones y su ejercicio simultáneo de varios contra uno, siempre que entre esas acciones exista un nexo por razón del título o causa de pedir que, además, en este caso nacen del mismo título; luego es factible la acumulación efectuada y así lo autoriza expresamente el artículo 555.2 de la LEC, que se cita como infringido, en tanto que permite la acumulación en procesos de ejecución que se sigan frente al mismo ejecutado.

Por ello, no hay inconveniente alguno en proceder a la ejecución simultánea de los créditos que nacen del mismo laudo frente al ejecutado. Es más, de este modo se evitaría la pluralidad de ejecuciones, con la multiplicidad de trámites que ello comporta y el mayor coste; de tal manera que no sólo no está vedada la acumulación por dichas normas, sino que es aconsejable tanto por razones de economía procesal como por el principio de tutela judicial efectiva.

Por este motivo solicitamos que se reponga la resolución recurrida, despachando ejecución en la forma pretendida en nuestra demanda ejecutiva.

En su virtud,

SUPLICO AL TRIBUNAL que, teniendo por presentado este escrito, se sirva admitirlo, tener por interpuesto recurso de reposición contra el auto de fecha [FECHA] y, en su virtud, se reponga el mismo, acordando el despacho de ejecución por el importe pretendido de [IMPORTE] euros de principal, con más la cantidad de [IMPORTE] euros en concepto de intereses y costas.

OTROSÍ DIGO que, de conformidad con lo dispuesto en los apartados 4 y 6 de la disposición adicional decimoquinta de la LOPJ, acompaño a este escrito resguardo de consignación, en la cuenta de Depósitos y Consignaciones abierta a nombre del Tribunal, del depósito exigido para interponer el recurso, por importe de [IMPORTE: 25] euros.

Por lo que,

SUPLICO AL TRIBUNAL que tenga por constituido el depósito, dejando interesada desde este momento su devolución para el caso de estimación total o parcial del recurso.

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO]

Firma Procurador: ______________________

Firma Abogado: ______________________
