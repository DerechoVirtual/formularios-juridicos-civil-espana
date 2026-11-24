---
name: recurso-apelacion-infraccion-normas-sustantivas-civ-1356
description: "Recurso de apelación por infracción de normas sustantivas de la sentencia. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Recurso de apelación por infracción de normas sustantivas de la sentencia

> Formulario **CIV-1356** del plugin **Recursos civiles: reposición, apelación, casación y queja** (`formularios-recursos-civiles`) · Civil › Recursos · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **recursos**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Recurso de apelación por infracción de normas sustantivas de la sentencia» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Recurso de apelación por infracción de normas sustantivas de la sentencia” para mi caso». También puedes invocarla directamente con `/formularios-recursos-civiles:recurso-apelacion-infraccion-normas-sustantivas-civ-1356`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-recursos-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Recursos civiles: reposición, apelación, casación y queja) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (4 veces)
- [ ] NÚMERO (3 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] LOCALIDAD
- [ ] Nº

## Normas que cita el formulario

- art. 458 LEC
- art. 459 LEC
- art. 209 LEC
- art. 465.2 LEC
- art. 219.3 LEC
- art. 219 LEC
- art. 465.3 LEC

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

Proceso número [NÚMERO]

A LA AUDIENCIA PROVINCIAL DE [LOCALIDAD]

D. [NOMBRE Y APELLIDOS], Procurador de los Tribunales, en nombre y representación de D. [NOMBRE Y APELLIDOS], parte demandante en este proceso seguido con el número [NÚMERO], según tengo acreditado en autos, ante el Tribunal comparezco y como mejor proceda en derecho DIGO:

1) Que en fecha [FECHA] se dictó sentencia en este proceso, la cual fue notificada a esta parte en fecha [FECHA]

2) Que entendiendo que dicha sentencia no es ajustada a derecho, dicho sea con los debidos respetos y en términos de defensa, por medio del presente escrito interpongo contra la misma RECURSO DE APELACIÓN, impugnando todos sus pronunciamientos, tanto el condenatorio de mi representado al pago de la indemnización, como los relativos a intereses y costas.

3) Que, de conformidad a lo dispuesto en el art. 458 de la LEC, fundo el recurso de apelación en las siguientes ALEGACIONES:

PRIMERO.- Al amparo del art. 459 de la LEC, por infracción de las normas de la sentencia, al haberse dictado con vulneración de lo dispuesto en los arts. 209 y 218 de la LEC, al incurrir en el vicio de incongruencia.

Esta parte solicitó en su demanda la resolución de contrato y los efectos derivados del incumplimiento que se recogen en el suplico, pretendiendo, de una parte, la devolución del vehículo vendido y, de otra, una indemnización por daños y perjuicios por importe de 1800 euros, los cuales se estimaban causados por el incumplimiento, tal como se relataba en el hecho tercero de la demanda, practicándose prueba en el proceso sobre este hecho.

La resolución judicial infringe lo dispuesto en los arts. 209 y 218 de la LEC, pues en la sentencia no se hace mención alguna a la indemnización solicitada en nuestra demanda, limitándose el fallo a dar por resuelto el contrato y condenar al demandando a la devolución del vehículo.

Ante tal omisión, esta parte solicitó oportunamente complemento de sentencia, dictándose auto de fecha [FECHA] por el cual el Tribunal no daba lugar al mismo indicando que se había desestimado implícitamente la petición. Sin embargo, como es de ver en la sentencia, tal desestimación implícita no se ha producido, pues ninguna referencia se hace a los motivos alegados por esta parte para solicitar la indemnización, ni a la prueba practicada, ni a la relación causal entre la resolución por incumplimiento del demandado y los daños alegados por esta parte.

Incluso, y prueba que no hubo desestimación implícita, el fallo de la sentencia hace constar la íntegra estimación de la demanda y la condena en costas al demandado, lo que pone de manifiesto que hubo una falta de respuesta a la pretensión indemnizatoria de esta parte.

De acuerdo a la grave infracción denunciada, entendemos que procede revocar la sentencia en este punto y, conforme al art. 465.2 de la LEC, resolver lo procedente sobre la cuestión objeto de debate, en la forma que exponemos en el siguiente apartado.

SEGUNDO.- La sentencia recurrida infringe lo dispuesto en el artículo 219.3 de la LEC cuando prohíbe que la condena se efectúe con reserva de liquidación en la ejecución, siendo que el fallo de la sentencia establece la obligación de mi representado de indemnizar al actor en la cantidad que se acredite en ejecución de sentencia, sin predeterminar ninguna base de cálculo en los fundamentos de la sentencia. Es más, en el fundamento [Nº] de la sentencia recurrida parece condicionarse el pago de la indemnización a que el actor acredite los daños en la fase de ejecución de sentencia, admitiéndose implícitamente que no lo ha hecho en la fase declarativa del proceso, por lo que es obvio que se está infringiendo el precepto invocado, colocando a mi mandante en una situación de absoluta indefensión.

La jurisprudencia ha reiterado que el artículo 219 de la LEC prohíbe las sentencias con reserva de liquidación y, con mayor razón, las condenas de carácter condicional, en que el pago de una cantidad indeterminada queda además sujeta al hecho de que la parte demandante acredite ciertos hechos en ejecución de sentencia, y en este sentido podemos citar la Sentencia de la Sala Primera del Tribunal Supremo de 10 de marzo de 2011, rec. 1998/2007.

De acuerdo a la grave infracción denunciada, entendemos que procede revocar la sentencia en este punto y, conforme al art. 465.3 de la LEC, resolver lo procedente sobre la cuestión objeto de debate, en la forma que exponemos en el siguiente apartado.

TERCERO.- Se argumenta sobre la decisión que debe adoptarse, haciendo las correspondientes alegaciones fácticas y jurídicas

Por lo expuesto, SUPLICO AL TRIBUNAL que tenga por interpuesto recurso de apelación contra la sentencia de fecha [FECHA] dictada en el proceso número [NÚMERO], con justificante de traslado a la otra parte que acompaño, y, previos los trámites legales, con remisión de las actuaciones a la Audiencia Provincial, a quien SUPLICO que estime el recurso interpuesto, revocando parcialmente la sentencia de instancia y condenando al demandado al pago de una indemnización de 1.800 euros a favor de mi representando, manteniendo el resto de pronunciamientos de la sentencia apelada.

OTROSÍ PRIMERO DIGO que, de conformidad con lo dispuesto en los apartados 3.b) y 6 de la disposición adicional decimoquinta de la LOPJ acompaño a este escrito resguardo de consignación en la cuenta de Depósitos y Consignaciones abierta a nombre del Tribunal del depósito exigido para interponer el recurso por importe de 50 euros.

SUPLICO AL TRIBUNAL que tenga por hecha la anterior manifestación a los efectos pertinentes y por acompañado el documento justificativo del abono de la tasa.

En L.y F.

Firma Procurador y Abogado.

========================================================================
