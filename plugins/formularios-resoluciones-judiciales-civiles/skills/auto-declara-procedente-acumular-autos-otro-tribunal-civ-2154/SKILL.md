---
name: auto-declara-procedente-acumular-autos-otro-tribunal-civ-2154
description: "Auto que declara procedente acumular autos de otro tribunal tras la impugnación de la contraparte. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Auto que declara procedente acumular autos de otro tribunal tras la impugnación de la contraparte

> Formulario **CIV-2154** del plugin **Resoluciones judiciales civiles: autos, decretos y diligencias** (`formularios-resoluciones-judiciales-civiles`) · Civil › Resoluciones judiciales (autos, decretos, providencias, diligencias) · normativa revisada el 24-11-2026.

## Qué es

Modelo de auto estimando procedente la solicitud de acumulación de autos de otro Tribunal, después de la impugnación de la contraparte.

Es un modelo de tipo **resoluciones judiciales (autos, decretos, providencias, diligencias)**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Auto que declara procedente acumular autos de otro tribunal tras la impugnación de la contraparte» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Auto que declara procedente acumular autos de otro tribunal tras la impugnación de la contraparte” para mi caso». También puedes invocarla directamente con `/formularios-resoluciones-judiciales-civiles:auto-declara-procedente-acumular-autos-otro-tribunal-civ-2154`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-resoluciones-judiciales-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Resoluciones judiciales civiles: autos, decretos y diligencias) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (13 veces)
- [ ] NÚMERO (3 veces)
- [ ] AÑO (2 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] FECHA (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NOMBRE DE LA PARTE (2 veces)
- [ ] Nº (2 veces)
- [ ] ACTO O RESOLUCIÓN
- [ ] LUGAR

## Normas que cita el formulario

- art. 75 LEC
- art. 76 LEC
- art. 77 LEC
- art. 78 LEC
- art. 78.2 LEC
- art. 451 LEC

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

AUTO

En [LUGAR], a [FECHA].

Juez Sr. [NOMBRE Y APELLIDOS]

ANTECEDENTES DE HECHO

PRIMERO

Por el Procurador/a D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS], se ha solicitado la acumulación a este procedimiento del Juicio Ordinario, seguido a instancias de D./Dña. [NOMBRE Y APELLIDOS], D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS] frente a [ACTO O RESOLUCIÓN], pendiente en este Tribunal, de los autos de Juicio Ordinario números [Nº] / [AÑO] y [Nº] / [AÑO], seguidos ante la Sección Civil del Tribunal de Instancia n.º [NÚMERO] y n.º [NÚMERO] de [LOCALIDAD], respectivamente, a instancias de [NOMBRE DE LA PARTE], sobre reclamación de cantidad, iniciados todos en fecha [FECHA], que se encuentran en trámite procesal de convocatoria para acto del juicio.

SEGUNDO

Pedida la acumulación, por el LAJ se ha comunicado la petición a los Tribunales afectados por el medio más rápido (fax, teléfono, telégrafo, o correo electrónico), y se ha dado traslado a las demás partes personadas en estos autos, para que en el plazo de diez días alegaran lo que estimaran pertinente sobre la acumulación solicitada, dentro de cuyo plazo la mercantil [DENOMINACIÓN SOCIAL] presentó escrito de alegaciones que impugnaba la petición.

RAZONAMIENTOS JURÍDICOS

PRIMERO

En los arts. 74 y ss. LEC se regula la posibilidad de acumulación de distintos autos, con la finalidad de sustanciarse todos en un solo procedimiento y ser resueltos por una misma sentencia, pero, siempre que lo solicite parte legítima (art. 75 LEC), que concurra causa que lo justifique (art. 76 LEC), que los procesos sean acumulables (art. 77 LEC), y finalmente, que no sea uno de los casos especialmente exceptuados (art. 78 LEC), circunstancias las anteriores que tienen que concurrir para poder acordar la acumulación.

SEGUNDO

En el presente caso, solicitan la acumulación quienes son demandantes en proceso de impugnación de acuerdo social adoptado en Junta Universal de accionistas de [DENOMINACIÓN SOCIAL], cual es quien les demanda en dos juicios de la misma clase, si bien de reclamación de cantidad, en que se dilucida una obligación societaria derivada del acuerdo de la Junta. La legitimación, acumulabilidad de los autos y causa por prejudicialidad civil son evidentes.

Aduce [NOMBRE DE LA PARTE] que sus demandas son anteriores en el tiempo, lo cual no hay modo de adverar, puesto que todas son de la misma fecha, y el reparto de los Tribunales de distintas poblaciones no tiene una diacronía correlativa, y ha de aplicarse la opción de quien solicita la acumulación, según residualmente asume el art. 79.2, párrafo 3.º LEC.

Por otro lado, no se trata de una fraudulenta alternativa a la acumulación inicial o sobrevenida de acciones, prohibida por el art. 78.2 y 3 LEC, desde que D./Dña. [NOMBRE Y APELLIDOS], por sí, y aun unido con D./Dña. [NOMBRE Y APELLIDOS], carecen de la titularidad de capital social mínimo para ganar la legitimación activa del art. 206 del texto refundido de la Ley de Sociedades de Capital, aprobado por Real Decreto Legislativo 1/2010, de 2 de julio, para impugnar el acuerdo de Junta, que han conseguido con la colaboración de D./Dña. [NOMBRE Y APELLIDOS], codemandante en estos autos. Por otra parte, no son demandados reconvinientes de acción impugnatoria, ya que exclusivamente opusieron como excepción de fondo la inválida celebración de la Junta Universal, ya que uno de los accionistas disidentes la abandonó antes de constituirse.

Vistos los artículos citados y demás de pertinente aplicación,

PARTE DISPOSITIVA

Se estima procedente la solicitud formulada por el Procurador/a de los Tribunales D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS], de acumular a estos autos los autos de juicio ordinario números/y/que se encuentran pendientes en las Secciones Civiles de los Tribunales de Instancia númerosyde, respectivamente.

Diríjase oficio a los Tribunales expresados, requiriéndoles la acumulación de los procesos indicados y su remisión a este Tribunal.

Al oficio se acompañará testimonio del presente auto, de las alegaciones de las partes, y de los escritos de demanda y contestación.

Así lo dispongo, mando y firmo.

Firma del Juez/a

Contra esta resolución cabe interponer recurso de reposición ante el mismo Tribunal, no obstante lo cual, se llevará a efecto lo acordado.

El recurso deberá interponerse por medio de escrito en el plazo de cinco días hábiles, contados desde el día siguiente de la notificación, con expresión de la infracción cometida a juicio del recurrente, sin cuyos requisitos no se admitirá (arts. 451 y 452 LEC).

Para interponer el recurso será necesario la constitución de un depósito de 25 euros, sin cuyo requisito no será admitido a trámite. El depósito se constituirá consignando dicho importe en la Cuenta de Depósitos y Consignaciones que este Tribunal tiene abierta en [LOCALIDAD] con el número [NÚMERO], indicando en el campo concepto del resguardo de ingreso que se trata de un "Recurso" código 00-Reposición. La consignación deberá ser acreditada al interponer el recurso (disp. adic. 15.ª de la LOPJ).

Están exentos de constituir el depósito para recurrir los incluidos en el apartado 5 de la disposición citada y quienes tengan reconocido el derecho a la asistencia jurídica gratuita

========================================================================
