---
name: decreto-revoca-encargo-persona-entidad-especializada-civ-2080
description: "Decreto que revoca el encargo a persona o entidad especializada por transcurso del plazo. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Decreto que revoca el encargo a persona o entidad especializada por transcurso del plazo

> Formulario **CIV-2080** del plugin **Resoluciones judiciales civiles: autos, decretos y diligencias** (`formularios-resoluciones-judiciales-civiles`) · Civil › Resoluciones judiciales (autos, decretos, providencias, diligencias) · normativa revisada el 24-11-2026.

## Qué es

Auto revocando el encargo de realización de los bienes embargados encomendado a persona o entidad especializada, por haber transcurrido seis meses sin que se haya llevado a cabo, debiendo aplicarse la caución ofrecida a los fines de la ejecución.

Es un modelo de tipo **resoluciones judiciales (autos, decretos, providencias, diligencias)**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Decreto que revoca el encargo a persona o entidad especializada por transcurso del plazo» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Decreto que revoca el encargo a persona o entidad especializada por transcurso del plazo” para mi caso». También puedes invocarla directamente con `/formularios-resoluciones-judiciales-civiles:decreto-revoca-encargo-persona-entidad-especializada-civ-2080`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-resoluciones-judiciales-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Resoluciones judiciales civiles: autos, decretos y diligencias) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (4 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] IMPORTE (2 veces)
- [ ] IMPORTE EN CIFRA (2 veces)
- [ ] LUGAR (2 veces)
- [ ] GRUPO
- [ ] NÚMERO

## Normas que cita el formulario

- art. 634 LEC
- art. 641.5 LEC

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

Notas al pie del formulario original:
(1) Téngase en cuenta que desde la reforma procesal operada por LO 1/2025, aplicable a procesos incoados desde el 3 de abril de 2025, se elimina el régimen de enajenación por medio de persona o entidad especializada como un medio autónomo de realización de bienes embargados, modificando a tal efecto el art. 636 LEC que ahora establece que en defecto de acuerdo entre las partes para la realización de los bienes embargados se procede directamente a su subasta judicial.

No obstante, se mantiene la posibilidad de realizar los bienes mediante acuerdo de realización, pero a falta de acuerdo la enajenación de los bienes embargados se llevará a cabo mediante subasta judicial, desapareciendo, en este caso, el mecanismo de «Enajenación por medio de persona o entidad especializada».

Así, el acuerdo del ejecutante, ejecutado y quien acredite interés directo en la ejecución podrán convenir el modo de realización más eficaz de los bienes hipotecados, pignorados o embargados, frente a los que se dirige la ejecución, incluida la realización por persona o entidad especializada. Este acuerdo se produce ahora extrajudicialmente, eliminándose el trámite de comparecencia ante el Letrado/a de la Administración de Justicia para convenir la forma de realización de los bienes.

El acuerdo entre ejecutante y ejecutado, lo aprobará el LAJ mediante decreto y suspenderá la ejecución respecto del bien o bienes objeto del acuerdo.

El LAJ también aprobará el acuerdo si incluyere la conformidad expresa de sujetos, distintos de ejecutante y ejecutado, a quienes afectare.

En el supuesto de que se acuerde la realización mediante subasta extrajudicial, por persona o entidad especializada, el LAJ aprobará la transmisión tras verificar el cumplimiento de la normativa de ordenación del comercio minorista, reguladora de la venta en pública subasta.

Cuando el convenio de realización se refiera a bienes susceptibles de inscripción registral será necesaria, para su aprobación, la conformidad expresa de los acreedores y terceros poseedores que hubieran inscrito o anotado sus derechos en el Registro correspondiente con posterioridad al gravamen que se ejecuta.

Acreditado el cumplimiento del acuerdo de realización de los bienes, el letrado/a de la Administración de Justicia sobreseerá la ejecución respecto del bien o bienes a los que se refiriera la ejecución.

Si el acuerdo no se cumpliere dentro del plazo pactado o, por cualquier causa, no se lograse la satisfacción del ejecutante en los términos convenidos, podrá éste pedir que se alce la suspensión de la ejecución y se proceda a la subasta, en la forma prevista en esta ley.

Las normas sobre subsistencia y cancelación de cargas serán aplicables también cuando se transmita la titularidad de inmuebles hipotecados o embargados.

Las enajenaciones deberán ser aprobadas por el letrado/a de la Administración de Justicia mediante decreto, previa comprobación de que la transmisión del bien se produjo con conocimiento, por parte del adquirente, de la situación registral que resulte de la certificación de cargas, y con el consentimiento expreso de los acreedores y terceros poseedores que hubieran inscrito o anotado sus derechos en el Registro correspondiente con posterioridad al gravamen que se ejecuta.

Aprobada la transmisión, se estará a lo dispuesto para la subasta de inmuebles en lo que se refiere a la distribución de las sumas recaudadas, inscripción del derecho del adquirente y mandamiento de cancelación de cargas.

Será mandamiento bastante para el Registro de la Propiedad el testimonio del decreto por el que se apruebe la transmisión del bien.

Consecuentemente, desde la entrada en vigor de la reforma por LO 1/2025, se suprime la sección 4ª que comprende los arts. 641 y 642 LEC referidos a la realización por persona o entidad especializada y subsistencia y cancelación de cargas, ya que su regulación se integra sustancialmente en el art. 640 LEC.

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

DECRETO DEL LETRADO DE LA ADMINISTRACIÓN DE JUSTICIA

En [LUGAR], a [FECHA].

Sr./Sra. Letrado de la Administración de Justicia [NOMBRE Y APELLIDOS]

ANTECEDENTES DE HECHO

PRIMERO.- Con fecha [FECHA] se dictó auto despachando ejecución contra los bienes de D./Dña. [NOMBRE Y APELLIDOS], en reclamación de la cantidad de [IMPORTE] euros ([IMPORTE EN CIFRA] €) en concepto de principal e intereses devengados hasta la fecha, más otros [IMPORTE] euros ([IMPORTE EN CIFRA] €) presupuestados provisionalmente para hacer frente a los intereses que, en su caso, puedan devengarse durante la ejecución y las costas de ésta.

SEGUNDO.- Como consecuencia de la ejecución despachada, y previo decreto, se embargaron los siguientes bienes del ejecutado: (se exceptúan los comprendidos en los artículos 634 y 635 de la LEC)

TERCERO.- A petición del [ELEGIR: ejecutante / del ejecutado con consentimiento del ejecutante], se acordó por diligencia de ordenación de fecha [FECHA] que la realización de los bienes embargados se efectuara por [NOMBRE Y APELLIDOS], a quien se concedió un plazo de seis meses para ejecutar el encargo.

CUARTO.- Han transcurrido los seis meses concedidos sin que la realización de los bienes se haya llevado a cabo.

FUNDAMENTOS DE DERECHO

PRIMERO.- Según se ha relatado en los antecedentes de hecho, ha transcurrido en exceso el plazo de seis meses concedido para que la entidad designada llevara a cabo la realización de bienes, y no sólo no la ha practicado, sino que no ha formulado ninguna alegación tendente a su justificación, conforme a lo dispuesto en el art. 641.5 LEC

SEGUNDO.- De conformidad con el precepto referido, procede revocar el encargo realizado en su día, aplicando la caución a los fines de la ejecución ante la falta de acreditación por parte de la entidad de no haberse podido llevar a cabo por causa no imputable a la misma.

PARTE DISPOSITIVA

SE ACUERDA REVOCAR el encargo de realización de los bienes embargados encomendado a [NOMBRE Y APELLIDOS], por haber transcurrido seis meses sin que se haya llevado a cabo, debiendo aplicarse la caución ofrecida a los fines de la ejecución.

Contra esta resolución cabe interponer recurso de revisión, mediante escrito ante el Tribunal que se presenta dentro de los cinco días hábiles siguientes al de notificación, y en el que deberá indicarse la infracción cometida a juicio del recurrente, y sin perjuicio del cual se llevará a efecto lo acordado.

Para interponer el recurso será necesario la constitución de un depósito de 25 euros, sin cuyo requisito no será admitido a trámite. El depósito se constituirá consignando dicho importe en la Cuenta de Depósitos y Consignaciones que este Tribunal tiene abierta en el grupo [GRUPO] con el número [NÚMERO], indicando en el campo concepto del resguardo de ingreso que se trata de un "Recurso" código 00-Revisión. La consignación deberá ser acreditada al interponer el recurso (disp. adic. 15.ª de la LOPJ).

Están exentos de constituir el depósito para recurrir los incluidos en el apartado 5 de la disposición citada y quienes tengan reconocido el derecho a la asistencia jurídica gratuita.

Así lo acuerdo y firmo.

Por ser de Justicia que pido en [LUGAR], a [FECHA].

Firma del Letrado/a de la Administración de Justicia:
