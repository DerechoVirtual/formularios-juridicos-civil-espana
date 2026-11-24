---
name: demanda-revision-sentencia-firme-recuperacion-civ-1329
description: "Demanda de revisión de sentencia firme por recuperación de documentos decisivos. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de revisión de sentencia firme por recuperación de documentos decisivos

> Formulario **CIV-1329** del plugin **Recursos civiles: reposición, apelación, casación y queja** (`formularios-recursos-civiles`) · Civil › Recursos · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de revisión de sentencia firme por recuperación de documentos decisivos» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de revisión de sentencia firme por recuperación de documentos decisivos” para mi caso». También puedes invocarla directamente con `/formularios-recursos-civiles:demanda-revision-sentencia-firme-recuperacion-civ-1329`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-recursos-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Recursos civiles: reposición, apelación, casación y queja) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (9 veces)
- [ ] FECHA (7 veces)
- [ ] Nº DE PROCEDIMIENTO (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] IMPORTE (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] PARTE DEMANDADA (2 veces)
- [ ] SEDE (2 veces)
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] NOMBRE DEL SOLICITANTE
- [ ] Nº
- [ ] Nº DE DOCUMENTO

## Normas que cita el formulario

- art. 510 LEC
- art. 510.1 LEC
- art. 509 LEC
- art. 514 LEC
- art. 511 LEC
- art. 512 LEC
- art. 513 LEC

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

### Avisos de actualización (2) — se aplican en el texto, nunca se copian en el documento

- Junto a «…dictada por la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).
- Junto a «…bogado) ========================================================================»: requisito de procedibilidad del art. 5 LO 1/2025 — antes de presentar la demanda hay que intentar un medio adecuado de solución de controversias (MASC) y acreditarlo con la demanda (arts. 264.4.º y 399.3 LEC), salvo las materias excluidas del art. 5.2. Fuente: LO 1/2025, arts. 5 a 7 (BOE-A-2025-76).

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

A LA SALA DE CIVIL DEL TRIBUNAL SUPREMO

D. [NOMBRE Y APELLIDOS], Procurador de los Tribunales, actuando en nombre y representación de [NOMBRE DEL REPRESENTADO/A], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], asistido por el Abogado D. [NOMBRE Y APELLIDOS], ante la Sala comparezco y como mejor proceda en derecho DIGO:

Que mediante el presente escrito, al amparo de lo dispuesto en los arts. 509 y ss. de la LEC, formulo DEMANDA DE REVISIÓN DE LA SENTENCIA dictada por la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº] en fecha [FECHA] en autos de proceso ordinario seguidos con el número [NÚMERO] contra [PARTE DEMANDADA] (datos del demandante en la instancia) al concurrir el motivo primero del art. 510 de la LEC, por haberse recobrado un documento decisivo de los que no se pudo disponer por fuerza mayor o por obra de la referida parte demandante, en base a los siguientes,

HECHOS

PRIMERO.- La sentencia firme cuya revisión se pretende se dictó en fecha [FECHA] en los autos de proceso ordinario número [Nº DE PROCEDIMIENTO] seguidos ante el Tribunal de Instancia [SEDE] constando como parte demandante D. [NOMBRE Y APELLIDOS] y parte demandada mi representada.

El proceso tenía como objeto la reclamación de [IMPORTE] euros en concepto de rentas de la industria arrendada a mi representada, sita en [LOCALIDAD], quien por contrato de fecha [FECHA] había arrendado dicha industria a D. [NOMBRE Y APELLIDOS], quien había fallecido en fecha

El demandante D. afirmó ser heredero de D. [NOMBRE Y APELLIDOS], aportando testamento otorgado a su favor en fecha [FECHA] ante el Notario D. [NOMBRE Y APELLIDOS], motivo por el cual en ningún momento se pudo cuestionar por esta parte su legitimación activa.

El referido proceso finalizó por sentencia de fecha [FECHA] en la que se condenaba a mi representado al pago de [IMPORTE] euros al demandante, tal como se solicitaba en la demanda.

SEGUNDO.- Con posterioridad a dictarse sentencia firme, en fecha [FECHA], mi representado ha sido emplazado en autos número [Nº DE PROCEDIMIENTO] seguidos a instancia de [NOMBRE DEL SOLICITANTE], en reclamación de la misma cantidad y por idéntico concepto (acompañamos como documento número 1 testimonio de la demanda y como documento número 2 testimonio de la diligencia de emplazamiento).

Con motivo del emplazamiento y desde esa fecha, mi mandante conoce la existencia de un testamento ológrafo otorgado por D. [NOMBRE Y APELLIDOS], con posterioridad al testamento aportado por la contraparte, en virtud del cual se declaró heredero a D. [NOMBRE Y APELLIDOS], el cual fue protocolizado en la Notaría de [LOCALIDAD], de conformidad a lo acordado en autos de jurisdicción voluntaria número [NÚMERO] (acompañamos como documentos número 3 y 4 testimonio del testamento ológrafo y del acta notarial de protocolización, señalando expresamente estos documentos como decisivos para el desarrollo del proceso).

Se trata de un documento decisivo, pues lógicamente constata la falta de legitimación activa del demandante en los autos de los que trae causa esta revisión, quien en ningún momento mencionó la controversia latente sobre la herencia del arrendador, y que obviamente era totalmente desconocida para esta parte.

TERCERO.- La presente demanda se formula al amparo del motivo primero del art. 510 de la LEC, al haberse ganado la sentencia injustamente, como se constata de la obtención de un documento decisivo cual es el testamento ológrafo antes mencionado y la declaración de heredero antes referida, que condiciona absolutamente el pronunciamiento de la sentencia cuya revisión se pretende, pues podría evidenciar la falta de legitimación activa del demandante.

Se dan los requisitos del art. 510.1 de la LEC, según han sido interpretados reiteradamente por la doctrina de ese Alto Tribunal, puesto que han sido obtenidos después de pronunciada la sentencia, son documentos decisivos y no se ha podido disponer de ellos por obra de la contraparte quien en ningún momento mencionó el conflicto sobre la herencia, cuando fácilmente se constata de la comprobación de fechas que el mismo ya era conocido al tiempo de interponerse la demanda.

CUARTO.- Mi representada, con anterioridad a la interposición de la presente demanda, ha depositado la cantidad de 300 euros en la cuenta de depósitos y consignaciones de la Sala, según se acredita por el resguardo que se acompaña a la presente demanda.

A los anteriores hechos son de aplicación los siguientes,

FUNDAMENTOS DE DERECHO

I. Jurisdicción, competencia y procedimiento: En cuanto a la jurisdicción y competencia, es competente la Sala a la que me dirijo conforme al art. 509 de la LEC al ser controvertida en el proceso una materia de derecho civil común, debiendo sustanciarse conforme a lo dispuesto en el art. 514 de la LEC.

II. Legitimación activa y pasiva: Está legitimado activamente la parte demandante de la revisión, conforme al art. 511 de la LEC, al haber resultado condenada en la sentencia firme impugnada, y lo está pasivamente el demandado por ser la parte actora en el proceso de instancia.

III. Plazo de interposición: La revisión se solicita dentro de los plazos del art. 512 de la LEC, al no haber transcurrido cinco años desde la fecha de publicación de la sentencia ni tres meses desde el día [FECHA], fecha en que conoció el testamento ológrafo y la declaración de heredero a favor de D. [NOMBRE Y APELLIDOS], tal como se ha relatado en el hecho segundo.

IV. Depósito: Mi mandante acompaña resguardo acreditativo del depósito conforme establece el art. 513 de la LEC.

V. Motivos de revisión: La revisión se solicita al amparo del ordinal 1º del art. 510 de la LEC al haberse recobrado, después de pronunciado el fallo, un documento decisivo cual es el testamento ológrafo que revocaba el esgrimido por el demandante en el proceso, no habiendo podido disponer de este documento por obra del mismo, quien silenció su existencia, esgrimiendo un título testamentario que a la postre resultó revocado.

Por lo expuesto es de justicia y

SUPLICO A LA EXCMA. SALA que tenga por presentada esta demanda de revisión de la sentencia dictada por la Sección Civil del Tribunal de Instancia número [NÚMERO] en autos de proceso ordinario número [Nº DE PROCEDIMIENTO] contra [PARTE DEMANDADA] y, tras los trámites legales, dicte sentencia por la que rescinda la sentencia impugnada, condenando a las partes a estar y pasar por tal declaración, con devolución del depósito constituido para recurrir.

OTROSÍ DIGO que, teniendo esta parte la intención de solicitar la suspensión de la ejecución de la sentencia cuya revisión se pretende, interesa a su derecho que se acuerde la expedición de testimonio de la demanda y auto de admisión a tales efectos, haciendo entrega de los mismos a esta representación.

Por lo que SUPLICO A LA EXCMA. SALA acuerde de conformidad.

En L. y F.

(Firma Procurador y Abogado)

========================================================================
