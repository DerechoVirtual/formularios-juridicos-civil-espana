---
name: sentencia-divorcio-mutuo-acuerdo-tras-transformar-civ-1886
description: "Sentencia de divorcio de mutuo acuerdo tras transformar el contencioso, sin aprobar una cláusula. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Sentencia de divorcio de mutuo acuerdo tras transformar el contencioso, sin aprobar una cláusula

> Formulario **CIV-1886** del plugin **Resoluciones judiciales civiles: autos, decretos y diligencias** (`formularios-resoluciones-judiciales-civiles`) · Civil › Resoluciones judiciales (autos, decretos, providencias, diligencias) · normativa revisada el 24-11-2026.

## Qué es

Sentencia declarando disuelto por divorcio el matrimonio y aprobando el convenio regulador propuesto por las partes, a excepción de lo estipulado en la cláusula relativa al régimen de comunicación y estancias del padre con los hijos menores, debiendo presentar otro que estipule un régimen preciso y bilateral.

Es un modelo de tipo **resoluciones judiciales (autos, decretos, providencias, diligencias)**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Sentencia de divorcio de mutuo acuerdo tras transformar el contencioso, sin aprobar una cláusula» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Sentencia de divorcio de mutuo acuerdo tras transformar el contencioso, sin aprobar una cláusula” para mi caso». También puedes invocarla directamente con `/formularios-resoluciones-judiciales-civiles:sentencia-divorcio-mutuo-acuerdo-tras-transformar-civ-1886`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-resoluciones-judiciales-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Resoluciones judiciales civiles: autos, decretos y diligencias) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (14 veces)
- [ ] FECHA (8 veces)
- [ ] AÑO
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] NOMBRE DE LOS MENORES
- [ ] NOMBRE Y APELLIDOS DEL MAGISTRADO
- [ ] Nº
- [ ] NÚMERO
- [ ] SEDE

## Normas que cita el formulario

- art. 777 LEC
- art. 90 CC
- art. 86 CC
- art. 777.2 LEC
- art. 91 CC
- art. 777.8 LEC
- art. 458.2 LEC

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

- Junto a «…ado-Juez de la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

En [LUGAR], a [FECHA].

Vistos por D./Dña. [NOMBRE Y APELLIDOS], Magistrado-Juez de la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº] [NOMBRE Y APELLIDOS DEL MAGISTRADO], los presentes autos de juicio de divorcio, seguida en autos n.º [NÚMERO]/[AÑO], a instancias de D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, en nombre y representación de Doña [NOMBRE Y APELLIDOS] y Don [NOMBRE Y APELLIDOS], asistidos del/la Letrado/a D./Dña. [NOMBRE Y APELLIDOS], ha pronunciado en nombre de S.M. El Rey de España la siguiente

SENTENCIA

ANTECEDENTES DE HECHO

PRIMERO.- Doña [NOMBRE Y APELLIDOS], bajo representación procesal del/la Procurador/a Sr./a [NOMBRE Y APELLIDOS], interpuso el [FECHA] demanda de divorcio contra su esposo, Don [NOMBRE Y APELLIDOS], de fecha [FECHA], alegando las circunstancias que justificaban el mantenimiento de la pensión de alimentos del padre para los hijos y compensatoria para la actora, suplicando se disolviera el matrimonio por divorcio y se aprobaran medidas semejantes a un convenio privado de separación extrajudicial.

SEGUNDO.- Por decreto/auto de [FECHA], se admitió a trámite la demanda, emplazándose a la parte demandada para contestación, y sin expirar el plazo, comparecieron ambos cónyuges con la misma mandataria procesal, Procurador/a Sr./a. [NOMBRE Y APELLIDOS], presentando convenio regulador firmado por las dos partes, con solicitud de la transformación del proceso al trámite del art. 777 LEC.

TERCERO.- Por diligencia de ordenación de [FECHA] se dispuso conceder el trámite solicitado al proceso y la citación de las partes para la ratificación por separado, con traslado al Ministerio Fiscal, y ratificado, se concedió audiencia a los hijos comunes menores de edad afectados.

CUARTO.- Emitido informe por el Ministerio Fiscal en su plazo de cinco días, oficiado el [FECHA], en providencia del día [FECHA] siguiente, estimándose suficiente la documentación presentada e innecesaria la práctica de prueba, quedaron los autos en la mesa del Juzgador para dictar la sentencia que procede en este proceso, que ha respetado las normas formales que prescribe la Ley.

FUNDAMENTOS DE DERECHO

PRIMERO.- En escritura pública de [FECHA], los cónyuges Doña [NOMBRE Y APELLIDOS] y Don [NOMBRE Y APELLIDOS] pactaron la separación de hecho y, disolviendo el régimen de bienes, procedieron a su liquidación, junto con el establecimiento de medidas en convenio regulador. Pasados los años, la esposa formula demanda de divorcio, de manera que en el curso del proceso se presenta nuevo convenio regulador que reúne los requisitos y formalidades prescritos en el art. 90 CCiv.

Habida cuenta de que, según el art. 86 CCiv, en relación con lo dispuesto en el art. 81 de dicho texto legal únicamente se exige el transcurso del plazo de tres meses desde la celebración del matrimonio, concurren todos los requisitos objetivos para declarar la disolución por divorcio del matrimonio de los litigantes.

SEGUNDO.- Como quiera que se acompañaron con la demanda los documentos que exige el art. 777.2 LEC, debe procederse al examen judicial, conforme al último inciso del art. 91 CCiv y arts. 775.2 y 777.9 LEC, de las medidas definitivas que representan las cláusulas del convenio regulador. Según la opinión del Ministerio Fiscal y lo que se extrae de la audiencia de los menores, no se considera homologable la estipulación II del convenio regulador presentado, habida cuenta de que deja al albur de una de las partes la efectiva existencia de unas comunicaciones y estancias de los hijos menores con el padre no custodio, lo que no es un puro derecho subjetivo del mismo, sino un derecho-deber de la patria potestad y un interés requerido para el crecimiento de la personalidad de los menores [NOMBRE DE LOS MENORES].

Vistos los preceptos legales citados, y cualesquiera otros de general y pertinente aplicación, ejerciendo la potestad jurisdiccional que emana de la soberanía popular

FALLO

Que estimando la solicitud del/la Procurador/a de los Tribunales D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de Doña [NOMBRE Y APELLIDOS] y Don [NOMBRE Y APELLIDOS], declaro disuelto por divorcio el matrimonio de dichos cónyuges.

Se aprueba el convenio regulador propuesto por las partes, a excepción de lo estipulado en la cláusula II debiendo presentar otro que estipule un régimen de comunicación y estancias del padre con los hijos menores preciso y bilateral, en sustitución de la citada estipulación.

Esta sentencia es firme en cuanto a la declaración de divorcio, por lo que se librará oficio al Encargado del Registro Civil de [LOCALIDAD], al que se acompañará testimonio, a fin de que proceda a anotar la parte dispositiva en la correspondiente inscripción de matrimonio.

En cuanto al convenio regulador, las partes tendrán que presentar uno nuevo en el plazo de diez días, computado una vez finalizado el plazo para optar entre la representación y defensa únicas o separadas.

Contra la presente resolución sólo puede interponer recurso de apelación el Ministerio Fiscal en interés de los hijos menores (art. 777.8 LEC). El recurso se interpondrá ante este Tribunal, en el plazo de veinte días hábiles a contar desde el siguiente a la notificación, exponiendo las alegaciones en que se base la impugnación, además de citar la resolución apelada y los pronunciamientos que impugna (art. 458.2 LEC).

Así por esta mi sentencia, definitivamente juzgando en la instancia, lo pronuncio, mando y firmo.

Firma del Juez/a

========================================================================
