---
name: auto-continua-proceso-pese-incomparecencia-sucesores-civ-1918
description: "Auto que continúa el proceso pese a la incomparecencia de los sucesores. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Auto que continúa el proceso pese a la incomparecencia de los sucesores

> Formulario **CIV-1918** del plugin **Resoluciones judiciales civiles: autos, decretos y diligencias** (`formularios-resoluciones-judiciales-civiles`) · Civil › Resoluciones judiciales (autos, decretos, providencias, diligencias) · normativa revisada el 24-11-2026.

## Qué es

Auto acordando la continuación del juicio, no obstante, la incomparecencia de los sucesores de la parte demandante en el proceso fallecida, debidamente emplazados. Documento adapatado a la reforma orgánica de la LO 1/2025.

Es un modelo de tipo **resoluciones judiciales (autos, decretos, providencias, diligencias)**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Auto que continúa el proceso pese a la incomparecencia de los sucesores» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Auto que continúa el proceso pese a la incomparecencia de los sucesores” para mi caso». También puedes invocarla directamente con `/formularios-resoluciones-judiciales-civiles:auto-continua-proceso-pese-incomparecencia-sucesores-civ-1918`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-resoluciones-judiciales-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Resoluciones judiciales civiles: autos, decretos y diligencias) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] FECHA
- [ ] GRUPO
- [ ] LUGAR
- [ ] NÚMERO
- [ ] TRÁMITE PROCESAL

## Normas que cita el formulario

- art. 16.2 LEC
- art. 20.3 LEC
- art. 155 LEC

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

Auto acordando la continuación del juicio, no obstante, la incomparecencia de los sucesores de la parte demandante en el proceso fallecida, debidamente emplazados.

Documento adapatado a la reforma orgánica de la LO 1/2025.

Notas al pie del formulario original:
(1) La otra alternativa, sería la resolución contraria a la prosecución del juicio, a pesar de la solicitud de parte demandada, y que consiste en decreto del Letrado de la Administración de Justicia que tendría a la parte actora por desistida.

========================================================================


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

AUTO

En [LUGAR], a [FECHA].

Juez Sr./Sra. [NOMBRE Y APELLIDOS]

ANTECEDENTES DE HECHO

PRIMERO

Iniciado este proceso ha fallecido la parte actora, D./Dña. [NOMBRE Y APELLIDOS], como acreditó la demandada, mediante la aportación del correspondiente certificado de defunción.

SEGUNDO

Señalada D./Dña. [NOMBRE Y APELLIDOS], como cónyuge del finado y heredera aparente del actor, las gestiones realizadas no han conllevado poderla localizar, no obstante lo cual, la parte demandada ha manifestado que interesa la continuación del juicio.

FUNDAMENTOS DE DERECHO

PRIMERO

Conforme al art. 16.2 LEC, constando el fallecimiento de un litigante, se permitirá a las demás partes pedir, previa identificación de los sucesores y de sus domicilios, que se les emplace para comparecer en el proceso, y el 16.3 párrafo 2.º, que tratándose del demandante, si no fuera posible identificar o localizar a los sucesores, se entenderá que ha habido desistimiento, salvo que el demandado se opusiera, en cuyo caso el Juez resolverá lo que estime oportuno (art. 20.3 "in fine" LEC).

SEGUNDO

En el caso presente ha fallecido la parte actora, y a la demandada no le ha sido viable llegar a localizar a los sucesores, habiendo manifestado su propósito de continuar el juicio, razón por la que procede resolver sobre si continuará o no.

TERCERO

El efecto general de la inidentificación de sucesores del actor que ha muerto, o identificados, como es el caso, que no se localizan, consiste en tener a la parte por desistida de la pretensión, lo que representa un efecto procesal débil respecto de la renuncia -acto capital que requiere en principio una voluntad del litigante, expresa o presunta, que implica el enteramiento de su posición y cargas en el proceso-, ya que permite volver a plantear la acción en la forma que se estime conveniente en otro proceso, mientras que el derecho no se haya extinguido (STS de 18 de marzo de 1994, rec. 1129/1991).

No obstante, se viabiliza por la norma que se postule la continuación del juicio por la parte demandada a fin de que se obtenga resolución en cuanto al fondo, que por autoridad de cosa juzgada material negativa, impida volver al objeto del litigio, ya que el derecho a tal resolución de fondo forma parte del contenido esencial de la efectiva tutela judicial, tanto del demandante como del demandado, desde la litispendencia.

En evitación de indefensiones, no cabría apoyar el efecto especial ante la mera ignorancia de sucesores concretos, o la carencia de emplazamiento por remisión a domicilio, sino después de agotados los mecanismos de los arts. 155 y 156 LEC, para averiguar la localización de los presuntos legitimados activos. Y, en fin, se requeriría que la pretensión y resistencia estén avanzados en cuanto a su delimitación definitiva e intento probatorio, como acontece una vez superada la fase de audiencia previa.

Dándose los precitados presupuestos, y ficticia la voluntad rebelde de los sucesores del actor por su citación edictal, que se publicará en medios de difusión, débese estimar la prosecución del juicio.

PARTE DISPOSITIVA

Acuerdo la continuación del presente juicio, no obstante la incomparecencia de los sucesores de D./Dña. [NOMBRE Y APELLIDOS], parte demandante en el proceso.

Se alza la suspensión, convocándose a los litigantes al acto del juicio ( o trámite que proceda [TRÁMITE PROCESAL])

Firma del Juez/a

Esta resolución se notificará a las partes y a los sucesores del actor por vía edictal, con advertencia de que cabe interponer recurso de reposición, mediante escrito ante el Tribunal que deberá presentarse dentro de los cinco días hábiles siguientes al de notificación, y en el que deberá indicarse la infracción cometida a juicio del recurrente, y sin perjuicio del cual se llevará a efecto lo acordado.

Para interponer el recurso será necesario la constitución de un depósito de 25 euros, sin cuyo requisito no será admitido a trámite. El depósito se constituirá consignando dicho importe en la Cuenta de Depósitos y Consignaciones que este Tribunal tiene abierta en el grupo [GRUPO] con el número [NÚMERO], indicando en el campo concepto del resguardo de ingreso que se trata de un "Recurso" código 00-Reposición. La consignación deberá ser acreditada al interponer el recurso (disp. adic. 15.ª de la LOPJ).

Están exentos de constituir el depósito para recurrir los incluidos en el apartado 5 de la disposición citada y quienes tengan reconocido el derecho a la asistencia jurídica gratuita.
