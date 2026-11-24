---
name: auto-rechaza-medida-cautelar-anterior-juicio-no-civ-2094
description: "Auto que rechaza la medida cautelar anterior al juicio por no concurrir urgencia ni necesidad. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Auto que rechaza la medida cautelar anterior al juicio por no concurrir urgencia ni necesidad

> Formulario **CIV-2094** del plugin **Resoluciones judiciales civiles: autos, decretos y diligencias** (`formularios-resoluciones-judiciales-civiles`) · Civil › Resoluciones judiciales (autos, decretos, providencias, diligencias) · normativa revisada el 24-11-2026.

## Qué es

Auto que deniega la medida cautelar solicitada antes de la demanda (en el modelo, cese temporal del cobro de comisiones por una entidad bancaria, instado por una asociación de consumidores y usuarios) por no acreditarse razones de urgencia o necesidad que justifiquen anticipar la tutela cautelar (arts. 730.2 y 734 LEC).

Es un modelo de tipo **resoluciones judiciales (autos, decretos, providencias, diligencias)**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Auto que rechaza la medida cautelar anterior al juicio por no concurrir urgencia ni necesidad» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Auto que rechaza la medida cautelar anterior al juicio por no concurrir urgencia ni necesidad” para mi caso». También puedes invocarla directamente con `/formularios-resoluciones-judiciales-civiles:auto-rechaza-medida-cautelar-anterior-juicio-no-civ-2094`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-resoluciones-judiciales-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Resoluciones judiciales civiles: autos, decretos y diligencias) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] DENOMINACIÓN DE LA ASOCIACIÓN (2 veces)
- [ ] DENOMINACIÓN SOCIAL DE LA ENTIDAD BANCARIA (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] AÑO
- [ ] DESCRIPCIÓN
- [ ] DÍA
- [ ] FECHA
- [ ] IMPORTE
- [ ] MES
- [ ] Nº DE CUENTA
- [ ] Nº DE GRUPO

## Normas que cita el formulario

- art. 734 LEC
- art. 730.1 LEC
- art. 736 LEC

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

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Magistrado/a: [NOMBRE Y APELLIDOS]

ANTECEDENTES DE HECHO

PRIMERO.- Por el/la Procurador/a Sr./a [NOMBRE Y APELLIDOS], en nombre y representación de la Asociación de Consumidores y Usuarios [DENOMINACIÓN DE LA ASOCIACIÓN], se presentó solicitud de medida cautelar de abstención temporal de que [DENOMINACIÓN SOCIAL DE LA ENTIDAD BANCARIA] continúe cobrando el incremento de comisiones de mantenimiento de contratos de cuenta de ahorro a la vista conforme a la condición general que señala, para asegurar la efectividad de la pretensión que anuncia ejercitará en la demanda y que consistirá en la declaración de nulidad de la cláusula que contiene aquélla.

SEGUNDO.- La parte solicitante ha presentado como documental una relación de los contratos-tipo de depósito [DESCRIPCIÓN], así como ha ofrecido prueba testifical y pretende valerse del interrogatorio del contrario. Asimismo, se pretende la dispensa de la constitución de caución y, para caso de su exigencia, se ha ofrecido caución en cuantía de [IMPORTE] euros, bajo fórmula de aval de compañía de seguro de crédito.

TERCERO.- De la solicitud se confirió traslado a la parte contraria, [DENOMINACIÓN SOCIAL DE LA ENTIDAD BANCARIA], y se convocó por el/la Letrado/a de la Administración de Justicia a ambas partes a la celebración de la vista que previene el art. 734 LEC, a la que asistieron ambos interesados, y, ratificada la asociación solicitante, se alegó de adverso que no existe urgencia y, en todo caso, no reviste la medida cautelar una mínima apariencia de buen derecho, amén de que se trata de un asunto de discretas cifras de dinero en el que no hay mínimo riesgo de que la entidad bancaria no pueda restituir de inmediato.

Se practicó la prueba propuesta por ambas partes, previa su admisión y declaración de pertinencia, con el resultado que consta grabado y resumido en el acta.

RAZONAMIENTOS JURÍDICOS

ÚNICO.- El art. 730.1 LEC sienta como regla de principio que la solicitud de medidas cautelares se efectúe junto con la demanda principal, aunque asume la excepción en el art. 730.2 siguiente de que se solicite la tutela cautelar con anterioridad, condicionando tal posibilidad a que la parte solicitante acredite que concurren razones de urgencia o de necesidad que justifiquen alterar el criterio general, y en el presente caso, bien que se ha verificado un esfuerzo en acreditar la apariencia de buen derecho y el peligro de retardo inherente a la pretensión cuyo ejercicio se anuncia, no se ha llegado a justificar cumplidamente que concurre una específica razón de urgencia o de necesidad por la que no pueda esperarse a que la parte actora formule su demanda, ya que no se percibe nada irreparable que pueda acontecer con inminencia y el tema es de interpretación normativa, con consecuencias en el plano puramente pecuniario, sin que parezca que una situación mantenida previamente durante meses, si perdura un breve tiempo más (y con ello no se prejuzga que no deba perdurar), conduzca a estado digno de protección a los usuarios, ni se pueda dudar de la solvencia de la entidad bancaria afectada.

PARTE DISPOSITIVA

Se deniega la adopción de la medida cautelar solicitada por el/la Procurador/a de los Tribunales D./Dña. [NOMBRE Y APELLIDOS], en representación de la Asociación de Consumidores y Usuarios [DENOMINACIÓN DE LA ASOCIACIÓN], con imposición de costas procesales a la parte solicitante.

Contra esta resolución cabe interponer recurso de apelación para ante la Iltma. Audiencia Provincial, que deberá interponerse ante este órgano en el plazo de veinte días hábiles contados desde el siguiente de la notificación, exponiendo el apelante las alegaciones en que se base la impugnación, además de citar la resolución apelada y los pronunciamientos que impugna (arts. 455 y 458.2 LEC), siendo tal recurso de tramitación preferente, conforme al art. 736 LEC.

Para interponer el recurso será necesaria la constitución de un depósito de 50 euros, sin cuyo requisito no será admitido a trámite. El depósito se constituirá consignando dicho importe en la Cuenta de Depósitos y Consignaciones que este Tribunal tiene abierta en el grupo [Nº DE GRUPO] con el número [Nº DE CUENTA], indicando en el campo concepto del resguardo de ingreso que se trata de un "Recurso" código 02-Apelación. La consignación deberá ser acreditada al interponer el recurso (disp. adic. 15.ª de la LOPJ).

No están obligados a constituir el depósito para recurrir los declarados exentos en la disposición citada y quienes tengan reconocido el derecho a la asistencia jurídica gratuita.

Así lo acuerdo, mando y firmo:

Por ser de justicia, lo pido en [LOCALIDAD], a [FECHA].

Firma del/de la Magistrado/a:
