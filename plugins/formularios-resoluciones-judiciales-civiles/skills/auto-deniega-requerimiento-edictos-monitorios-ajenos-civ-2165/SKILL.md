---
name: auto-deniega-requerimiento-edictos-monitorios-ajenos-civ-2165
description: "Auto que deniega el requerimiento por edictos en monitorios ajenos a cuotas de propiedad horizontal. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Auto que deniega el requerimiento por edictos en monitorios ajenos a cuotas de propiedad horizontal

> Formulario **CIV-2165** del plugin **Resoluciones judiciales civiles: autos, decretos y diligencias** (`formularios-resoluciones-judiciales-civiles`) · Civil › Resoluciones judiciales (autos, decretos, providencias, diligencias) · normativa revisada el 24-11-2026.

## Qué es

Auto que deniega la posibilidad de requerir de pago al deudor de un proceso monitorio mediante edictos en procesos que no son de reclamación de cuotas de propiedad horizontal y acuerda el sobreseimiento.

Es un modelo de tipo **resoluciones judiciales (autos, decretos, providencias, diligencias)**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Auto que deniega el requerimiento por edictos en monitorios ajenos a cuotas de propiedad horizontal» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Auto que deniega el requerimiento por edictos en monitorios ajenos a cuotas de propiedad horizontal” para mi caso». También puedes invocarla directamente con `/formularios-resoluciones-judiciales-civiles:auto-deniega-requerimiento-edictos-monitorios-ajenos-civ-2165`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-resoluciones-judiciales-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Resoluciones judiciales civiles: autos, decretos y diligencias) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] FECHA (2 veces)
- [ ] GRUPO
- [ ] LUGAR
- [ ] NÚMERO
- [ ] PROVINCIA
- [ ] SEDE

## Normas que cita el formulario

- art. 164 LEC
- art. 815 LEC
- art. 816.1 LEC
- art. 815.2 LEC
- art. 21 LPH
- art. 9.1.h LPH
- art. 815.1 LEC
- art. 813 LEC
- art. 816.2 LEC

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

ANTECEDENTES DE HECHO

PRIMERO.- En diligencia de ordenación de [FECHA] se trasladó a la parte actora la imposibilidad de requerimiento al supuesto deudor D./Dña. [NOMBRE Y APELLIDOS], excitando a que se facilitara nuevo domicilio en el partido judicial, o se instara lo que a su derecho conviniera, bajo apercibimiento de sobreseimiento.

SEGUNDO.- Por el Procurador/a Sr./a [NOMBRE Y APELLIDOS], se ha presentado escrito que solicita comunicación edictal conforme art. 164 LEC. Por el Letrado/a de la Administración de Justicia se ha procedido a dar cuenta al Tribunal.

RAZONAMIENTOS JURÍDICOS

PRIMERO.- La doctrina interpretativa del novedoso juicio monitorio no es unánime a propósito de si cabe practicar el requerimiento de pago en general por medio de edictos, aunque muy mayoritariamente se desaprueba.

El Juez lo rechaza por razones dogmáticas y positivas: 1.- Dogmáticamente, el juicio monitorio significa una inversión del principio procesal tradicionalísimo de los juicios declarativos, conforme al que el silencio del demandado representaba el mero incumplimiento de una carga, y se presumía de Derecho que el citado o emplazado resistía la pretensión, de modo que no había allanamiento por rebeldía, ni tampoco conformidad con los hechos por los que se pedía tutela judicial (salvo excepciones en juicio de tercería). De suyo, cuando se ha regulado una "ficta contestatio" en declarativo (art. 43 del Decreto de 21 de noviembre de 1952, reformado por Ley 34/1984), se hacía dependiente de una comunicación por remisión personal.

La inversión del principio presume de Derecho en el juicio monitorio que el demandado reconoce el crédito que se le enarbola por su silencio, una vez requerido de pago y con aportación de un principio de prueba documental. Esta ficción legal no puede congeniar con el núcleo esencial de efectiva tutela judicial si, a su vez, se edifica sobre otra ficción legal, que indiscutiblemente resulta serlo la comunicación edictal, toda vez que se fingiría que el requerido ha leído el requerimiento en el tablón de anuncios de la Oficina Judicial, o en su caso, el Boletín Oficial o periódico que fuera.

El título ejecutivo en el monitorio es un complejo que forma la afirmación del crédito documentado (solicitud inicial), el decreto de admisión judicial de la petición y requerimiento de pago (art. 815 LEC), y el silencio del requerido, que se configura como consentimiento tácito (art. 816.1 LEC, aunque nada excluye que exista un consentimiento expreso), y no puede admitirse que el consentimiento tácito se produzca con un requerimiento por edictos, que no es argumento indirecto de conformidad con la deuda, sino argumento puramente ficticio, careciendo el documento que abre el proceso de cualquier fehaciencia.

SEGUNDO.- En el plano positivo, ocurre que el art. 815.2 LEC prevé expresamente la posibilidad de requerimiento de pago por medio de edictos para las reclamaciones de las Comunidades de propietarios respecto de gastos comunes, con que la falta de prevención expresa para el proceso monitorio genérico, según principio general hermenéutico del Derecho, si la ley calla, no quiere, porque cuando quiere, lo dice.

Y la salvedad del monitorio de propiedad horizontal supera la tacha de edificar una ficción sobre otra, porque el proceso del art. 21 LPH exige un requerimiento preprocesal al propietario con arreglo al art. 9.1.h) LPH, que comprende un deber comunitario de fijación de domicilio para notificaciones.

Asimismo, el art. 815.1 LEC al referirse a las formas del requerimiento en el monitorio genérico, se indica la "prevista en el artículo 161 de esta Ley", y por ende, no se remite a las previstas en las normas a las que el precepto, a su vez, pueda remitir.

Si la competencia territorial para conocer del juicio monitorio se fija (art. 813 LEC), en ausencia de domicilio o residencia conocidos del deudor, como es el caso, por el lugar donde el deudor pudiera ser hallado a efectos de requerimiento de pago por el tribunal, ello es indicativo de que, hasta que no se encuentre al supuesto deudor en un lugar en que se encuentre con cierta periodicidad o lapso de tiempo significativo, no habrá órgano competente para asumir el conocimiento del proceso.

En fin, con arreglo al art. 816.2 LEC, se lograría con el despacho de ejecución secundario de un requerimiento edictal, un título de ejecución judicial inasequible a la revisión, o a la rescisión por audiencia de rebelde, de mejor condición que una sentencia firme, promocionándose recurso de amparo ante el TC.

PARTE DISPOSITIVA

Se sobresee el presente proceso monitorio, por falta de localización de D./Dña. [NOMBRE Y APELLIDOS], sin perjuicio de que pueda ejercitar la actora, D./Dña. [NOMBRE Y APELLIDOS] su derecho en el proceso en juicio ordinario, como corresponda.

Así lo dispongo y firmo,

Firma de D./Dña. [NOMBRE Y APELLIDOS]	Firma del Juez de la Sección Civil del Tribunal de Instancia [SEDE]

MODO DE IMPUGNACIÓN: mediante recurso de APELACIÓN ante el Tribunal para ante la Ilma. Audiencia Provincial [PROVINCIA], por escrito de interposición en el plazo de VEINTE DÍAS, desde el siguiente a la notificación, limitado a manifestar la voluntad de recurrir y con expresión de los pronunciamientos que se impugnen.

Para interponer el recurso será necesario la constitución de un depósito de 50 euros, sin cuyo requisito no será admitido a trámite. El depósito se constituirá consignando dicho importe en la Cuenta de Depósitos y Consignaciones que este Tribunal tiene abierta en el grupo [GRUPO] con el número [NÚMERO], indicando en el campo concepto del resguardo de ingreso que se trata de un "Recurso" código 02-Apelación. La consignación deberá ser acreditada al interponer el recurso (disp. adic. 15ª de la LOPJ).

No están obligados a constituir el depósito para recurrir los declarados exentos en la disposición citada y quienes tengan reconocido el derecho a la asistencia jurídica gratuita.

========================================================================
