---
name: auto-adopta-medida-cautelar-solicitada-junto-demanda-civ-2102
description: "Auto que adopta una medida cautelar solicitada junto con la demanda. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Auto que adopta una medida cautelar solicitada junto con la demanda

> Formulario **CIV-2102** del plugin **Resoluciones judiciales civiles: autos, decretos y diligencias** (`formularios-resoluciones-judiciales-civiles`) · Civil › Resoluciones judiciales (autos, decretos, providencias, diligencias) · normativa revisada el 24-11-2026.

## Qué es

Resolución que acuerda adoptar la medida cautelar de supresión temporal de la eficacia y anotación preventiva en el Registro de Condiciones Generales, para asegurar la efectividad de la pretensión formulada en el proceso principal, consistente en la condena de cesación de la cláusula del contrato de adhesión en cuestión, o su modificación subsidiaria.

Es un modelo de tipo **resoluciones judiciales (autos, decretos, providencias, diligencias)**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Auto que adopta una medida cautelar solicitada junto con la demanda» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Auto que adopta una medida cautelar solicitada junto con la demanda” para mi caso». También puedes invocarla directamente con `/formularios-resoluciones-judiciales-civiles:auto-adopta-medida-cautelar-solicitada-junto-demanda-civ-2102`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-resoluciones-judiciales-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Resoluciones judiciales civiles: autos, decretos y diligencias) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (3 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] FECHA
- [ ] GRUPO
- [ ] LUGAR
- [ ] NÚMERO

## Normas que cita el formulario

- art. 734 LEC
- art. 726 LEC
- art. 727 LEC
- art. 735 LEC
- art. 728.3 LEC
- art. 735.2 LEC

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

Juez Sr./a [NOMBRE Y APELLIDOS]

ANTECEDENTES DE HECHO

PRIMERO

Por el Procurador/a Sr./a [NOMBRE Y APELLIDOS], en nombre y representación del Colegio de Administradores de Fincas Urbanas de [LOCALIDAD], se ha solicitado la adopción de la medida cautelar de supresión temporal de la eficacia y anotación preventiva en el Registro de Condiciones Generales, respecto de la cláusula décima de unos contratos de adhesión sobre mantenimiento de ascensores o montacoches, para asegurar la efectividad de la pretensión formulada en el proceso principal frente a la mercantil [DENOMINACIÓN SOCIAL], S.A., consistente en la condena de cesación de la cláusula décima del contrato de adhesión en cuestión, o su modificación subsidiaria.

SEGUNDO

La parte solicitante ha presentado como documental el contrato-tipo, la certificación negativa de estar inscrita la condición, así como el dictamen de conciliación de del Registrador de Condiciones Generales, y avanzó en su petición de medidas queriendo valerse de la prueba del interrogatorio del contrario.

Asimismo, se pretende la dispensa de la constitución de caución, y para caso de su exigencia, se ha ofrecido la prestación de caución suficiente para responder de los daños y perjuicios que pudieran derivarse de la adopción de la medida.

TERCERO

De la solicitud se dio traslado a la parte contraria, S.A., y se convocó por el LAJ a ambas partes a la celebración de la vista que previene el art. 734 LEC, a la que asistieron todos los interesados personados, y ratificada la parte actora, se alegó de adverso la falta de capacidad procesal de la demandante, la ausencia de legitimación activa, que no existe peligro de retraso y que no es la medida útil y congruente con la pretensión del juicio principal.

Se practicó la prueba propuesta por ambas partes, previa su admisión y declaración de pertinencia, con el resultado que consta grabado y resumido en el acta.

RAZONAMIENTOS JURÍDICOS

PRIMERO

La batería de preceptos de los arts. 726 a 728 LEC, regula un régimen en la adopción de medidas cautelares, cual el siguiente:

Características: Que la medida solicitada sea alguna de las previstas en el art. 727 LEC o cualquier otra actuación directa o indirecta sobre bienes o persona del demandado, siempre que reúna las características señaladas de temporalidad, provisionalidad, instrumentalidad, susceptibilidad de modificación y alzamiento, y posible sustitución por otras menos onerosas para el demandado (art. 726 LEC), y en todo caso resulte idónea y congruente con la pretensión cuya efectividad se desea asegurar.

Presupuestos: Que la parte solicitante acredite el peligro de mora procesal, es decir, el riesgo de la demora o la infructuosidad de la tutela judicial que en su día pudiera merecerse (‘periculum in mora’), y que le asiste una apariencia de buen derecho, es decir que, sin prejuzgar el fondo del asunto, sea positivo el juicio indiciario de la existencia del derecho reclamado (‘fumus boni iuris’). Para la ejecución de la medida que proceda, es menester que la parte solicitantes ofrezca caución suficiente para responder de forma rápida y eficaz, de los daños y perjuicios que pudieran ocasionarse.

SEGUNDO.- De los elementos que aportó la parte actora, de las alegaciones y actuaciones practicadas en la vista, y de lo probado, se desprende que en el presente caso no puede dudarse de la concurrencia de los requisitos legales expresados, dentro de la admisión generalizada de la tutela jurisdiccional cautelar, de modo que procede acordar, en armonía con el art. 735 LEC, la medida cautelar solicitada

TERCERO.- En lo tocante a la caución, sin que se hayan demostrado circunstancias especiales que militen en contra del principio de exigencia de caución para la tutela cautelar civil del art. 728.3 LEC, la entidad económica de la aplicación de la cláusula debatida y la repercusión social discreta, amén de tocar el patrimonio de consumidores y usuarios a través de una estructura comunitaria -comunidades de propiedad horizontal- con fondos de reserva preestablecidos legalmente, aconsejan no acceder a la dispensa para el Colegio peticionario.

Relativo a la cuantía, forma y plazo de la caución exigible, con atención a la importancia real de la pretensión principal que se quiera asegurar, al fundamento indiciario de la nulidad contractual alegada, y al importe de los eventuales daños y perjuicios derivados de la ejecución de la medida, se estiman procedentes las condiciones que constarán en la parte dispositiva de esta resolución.

PARTE DISPOSITIVA

Se accede a la solicitud de la demanda del/de la Procurador/a de los Tribunales D./Dña. [NOMBRE Y APELLIDOS], en representación del Colegio de Administradores de Fincas Urbanas de [LOCALIDAD], y se acuerda la supresión temporal de la eficacia de la cláusula décima del contrato de adhesión de mantenimiento de ascensores o montacoches fijada por [DENOMINACIÓN SOCIAL], S.A., y su anotación preventiva en el Registro de Condiciones Generales.

La anterior medida cautelar no se ejecutará en tanto que la parte solicitante no preste la caución por importe deeuros (€), en forma de aval bancario o de compañía de seguros, en el plazo de cinco días hábiles desde la notificación.

Se imponen las costas del incidente a la parte demandada.

La presente resolución no es firme, por cuanto puede interponerse recurso de apelación para ante la Iltma. Audiencia Provincial en el plazo de veinte días hábiles contados desde el siguiente de la notificación, mediante escrito ante este Tribunal, exponiendo el apelante las alegaciones en que se base la impugnación, además de citar la resolución apelada y los pronunciamientos que impugna (arts. 455 y 458.2 LEC), careciendo tal recurso de efectos suspensivos de lo acordado, conforme al art. 735.2 'in fine' LEC.

Para interponer el recurso será necesaria la constitución de un depósito de 50 euros, sin cuyo requisito no será admitido a trámite. El depósito se constituirá consignando dicho importe en la Cuenta de Depósitos y Consignaciones que este Tribunal tiene abierta en el grupo [GRUPO] con el número [NÚMERO], indicando en el campo concepto del resguardo de ingreso que se trata de un "Recurso" código 02-Apelación. La consignación deberá ser acreditada al interponer el recurso (disp. adic. 15.ª de la LOPJ).

No están obligados a constituir el depósito para recurrir los declarados exentos en la disposición citada y quienes tengan reconocido el derecho a la asistencia jurídica gratuita.

Así lo acuerdo, mando y firmo

Lo acuerda, manda y firma el Ilmo. Sr./a:

Juez de Instrucción de [LOCALIDAD]

Firma del Juez:

========================================================================
