---
name: recurso-proceso-lleva-aparejado-lanzamiento-escrito-civ-1337
description: "Recurso en proceso que lleva aparejado el lanzamiento (escrito). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Recurso en proceso que lleva aparejado el lanzamiento (escrito)

> Formulario **CIV-1337** del plugin **Recursos civiles: reposición, apelación, casación y queja** (`formularios-recursos-civiles`) · Civil › Recursos · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **recursos**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Recurso en proceso que lleva aparejado el lanzamiento (escrito)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Recurso en proceso que lleva aparejado el lanzamiento (escrito)” para mi caso». También puedes invocarla directamente con `/formularios-recursos-civiles:recurso-proceso-lleva-aparejado-lanzamiento-escrito-civ-1337`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-recursos-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Recursos civiles: reposición, apelación, casación y queja) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (8 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] CONCEPTO DE LA RECLAMACIÓN
- [ ] IMPORTE
- [ ] LOCALIDAD
- [ ] Nº
- [ ] Nº DE ARTÍCULO
- [ ] Nº DE DOCUMENTO
- [ ] Nº DE PROCEDIMIENTO
- [ ] NÚMERO
- [ ] SEDE

## Normas que cita el formulario

- art. 458 LEC
- art. 459 LEC
- art. 183 LEC
- art. 33 LEC
- art. 22.4 LEC
- art. 449.1 LEC

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

- Junto a «…Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº]

Proceso [Nº DE PROCEDIMIENTO]

AL TRIBUNAL

D. [NOMBRE Y APELLIDOS] Procurador de los Tribunales y de D. [NOMBRE Y APELLIDOS], cuya representación tengo acreditada en el proceso arriba expresado, comparezco y como mejor proceda en Derecho, digo lo siguiente:

1) Que en fecha [FECHA] se me ha notificado la sentencia de fecha [FECHA] recaída en los presentes autos y no encontrándola ajustada a derecho, dicho sea con los debidos respetos y en términos de defensa, por medio del presente escrito interpongo contra la misma RECURSO DE APELACIÓN, para ante la Audiencia Provincial de [LOCALIDAD], impugnando todos sus pronunciamientos en cuanto al lanzamiento, indemnización, intereses y costas.

2) Que, de conformidad a lo dispuesto en el art. 458 de la LEC, fundo el recurso de apelación en las siguientes ALEGACIONES:

PRIMERA.- Al amparo del art. 459 de la LEC, por infracción de las garantías del proceso civil con vulneración de lo dispuesto en el art. 24 de la CE en cuanto al derecho fundamental a un proceso con todas las garantías.

Mi representado dedujo solicitud de asistencia jurídica gratuita el día [FECHA], siendo denegado en resolución oral dictada en el mismo acto del juicio, sin notificarse dicha resolución en ningún momento a mi representado y celebrándose el mismo en fecha [FECHA] sin la asistencia de mi representado, dándose lugar al lanzamiento por este motivo. Mi representado no tuvo ninguna posibilidad de impugnar esta resolución, por cuanto tras su solicitud realizada por comparecencia en fecha [FECHA], no fue notificado en ningún momento de la denegación, celebrándose el juicio sin su asistencia, de forma que sólo ha tenido conocimiento de esta circunstancia cuando le fue notificada la sentencia.

La resolución judicial infringe lo dispuesto en el art. 183 de la LEC y 24 CE, pues la solicitud se ajustaba perfectamente a los requisitos del art. 33 de la LEC, siendo denegada de forma indebida por el Tribunal.

La actuación judicial ha supuesto una vulneración del derecho de defensa de esta parte, pues mi representado se ha visto totalmente indefenso al no poder intervenir en el juicio.

De acuerdo a la grave infracción denunciada, entendemos que procede decretar la nulidad de todo lo actuado al momento de la celebración del juicio, debiendo retrotraerse las actuaciones a dicho momento procesal.

SEGUNDO.- En cuanto al fondo, infracción del art. 22.4 de la LEC, procedencia de la enervación de la acción.

La sentencia de instancia decreta el lanzamiento sin más trámite, sin tener en cuenta que concurrían las circunstancias establecidas en el art. 22.4 de la LEC para declarar enervada la acción. En la demanda se hizo constar que mi representado ya había hecho uso de la enervación en una ocasión anterior, siendo que tal extremo no es cierto puesto que, tal como se relata en la misma demanda, la actuación anterior a que se refiere el demandante fue un requerimiento notarial para el pago de rentas realizado varios meses antes, el cual fue atendido en tiempo y forma por mi representado en fecha [FECHA], sin que se llegara a iniciar actuación judicial alguna. Por tanto, ésta es la primera vez que se ejercita la acción de desahucio contra mi representado, constando además que mi representado consignó las rentas debidas en el tribunal el mismo día que dedujo su solicitud de asistencia jurídica gratuita, de forma que se dan los requisitos del art. 22.4 de la LEC para declarar enervada la acción.

Partiendo de lo anterior, procede revocar la declaración de desahucio y lanzamiento, debiendo acordarse tener por enervada la acción. Respecto de las costas, ante la estimación parcial de las pretensiones de la demanda que se considera procedente en caso de verse aceptado este recurso se considera que las mismas no deben imponerse a mi representado (art [Nº DE ARTÍCULO]. 394 LEC).

Por lo expuesto, SUPLICO AL TRIBUNAL que tenga por interpuesto recurso de apelación contra la sentencia de fecha [FECHA] dictada en el proceso número [NÚMERO], con justificante de traslado a la otra parte que acompaño, y, previos los trámites legales, remita las actuaciones a la Audiencia Provincial, a quien SUPLICO que estime el recurso interpuesto, declarando la nulidad de todo lo actuado desde el momento de la celebración del juicio, y acordando la retroacción de las actuaciones a dicho momento procesal; subsidiariamente, solicitamos que se revoque la sentencia y, en su lugar, se declare enervada la acción de desahucio, todo ello sin imposición de costas en ambos casos.

OTROSÍ PRIMERO DIGO que, en cumplimiento de lo dispuesto en el art. 449.1 y 2 de la LEC esta parte ha consignado las cantidades correspondientes a las rentas vencidas correspondientes al periodo reclamado y a la tramitación del proceso, según al contrato de arrendamiento suscrito en fecha [FECHA]. [CONCEPTO DE LA RECLAMACIÓN], que hasta este momento ascienden a [IMPORTE] euros, manifestando su voluntad de abonar las que venzan sucesivamente durante la sustanciación del recurso. Acompaño como documento número [Nº DE DOCUMENTO] resguardo acreditativo de la consignación en la cuenta de depósitos y consignaciones del Tribunal al que me dirijo.

Para el caso que el Tribunal no considerara suficiente el cumplimiento de los requisitos, esta parte manifiesta expresamente su voluntad de cumplir los requisitos legales, depositando las cantidades correspondientes con arreglo a derecho.

OTROSÍ SEGUNDO DIGO que, de conformidad con lo dispuesto en los apartados 3.b) y 6 de la disposición adicional decimoquinta de la LOPJ acompaño a este escrito resguardo de consignación en la cuenta de Depósitos y Consignaciones abierta a nombre del Tribunal del depósito exigido para interponer el recurso por importe de 50 euros.

En virtud de lo anterior,

SUPLICO AL TRIBUNAL: que tenga por hecha la anterior manifestación a los efectos pertinentes.

En L. y F.

(Firma de Procurador y Abogado)

========================================================================
