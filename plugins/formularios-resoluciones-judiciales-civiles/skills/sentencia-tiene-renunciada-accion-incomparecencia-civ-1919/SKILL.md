---
name: sentencia-tiene-renunciada-accion-incomparecencia-civ-1919
description: "Sentencia que tiene por renunciada la acción por incomparecencia de los sucesores del actor. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Sentencia que tiene por renunciada la acción por incomparecencia de los sucesores del actor

> Formulario **CIV-1919** del plugin **Resoluciones judiciales civiles: autos, decretos y diligencias** (`formularios-resoluciones-judiciales-civiles`) · Civil › Resoluciones judiciales (autos, decretos, providencias, diligencias) · normativa revisada el 24-11-2026.

## Qué es

Sentencia que tiene por renunciado de su acción al sucesor emplazado por causa de muerte del actor, que no comparece.

Es un modelo de tipo **resoluciones judiciales (autos, decretos, providencias, diligencias)**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Sentencia que tiene por renunciada la acción por incomparecencia de los sucesores del actor» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Sentencia que tiene por renunciada la acción por incomparecencia de los sucesores del actor” para mi caso». También puedes invocarla directamente con `/formularios-resoluciones-judiciales-civiles:sentencia-tiene-renunciada-accion-incomparecencia-civ-1919`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-resoluciones-judiciales-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Resoluciones judiciales civiles: autos, decretos y diligencias) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (13 veces)
- [ ] FECHA (7 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] AÑO
- [ ] DENOMINACIÓN SOCIAL
- [ ] GRUPO
- [ ] LUGAR
- [ ] Nº
- [ ] Nº DE PROCEDIMIENTO
- [ ] NÚMERO
- [ ] OBJETO DEL PROCEDIMIENTO
- [ ] SEDE

## Normas que cita el formulario

- art. 16.2 LEC
- art. 20.1 LEC
- art. 394 LEC

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

- Junto a «…o/a-Juez de la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. «De los de» es residuo de los varios juzgados de una plaza. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

En la Villa de [LOCALIDAD], a [FECHA]

Habiendo visto D./Dña. [NOMBRE Y APELLIDOS], Magistrado/a-Juez de la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº] [LOCALIDAD] y su partido, los presentes autos de Juicio Ordinario n.º [Nº DE PROCEDIMIENTO]/[AÑO], cuyo objeto es [OBJETO DEL PROCEDIMIENTO], seguidos entre partes, de la una como demandante D./Dña. [NOMBRE Y APELLIDOS], representado por la Procurador/a de los Tribunales D./Dña. [NOMBRE Y APELLIDOS], y asistido por la Letrado/a D./Dña. [NOMBRE Y APELLIDOS], y de la otra como demandada la mercantil [DENOMINACIÓN SOCIAL], representada por el Procurador/a de los Tribunales D./Dña. [NOMBRE Y APELLIDOS], y asistida del Letrado D./Dña. [NOMBRE Y APELLIDOS], ha pronunciado.

En nombre de S.M. El Rey

la siguiente SENTENCIA

ANTECEDENTES DE HECHO

Primero

En el curso de este proceso, la parte demandada produjo escrito de [FECHA], en que acreditaba que había muerto la parte actora, D./Dña. [NOMBRE Y APELLIDOS], en [LOCALIDAD], el [FECHA].

Segundo

No habiéndose personado sus sucesores en el plazo señalado en la ley, se hizo saber por la parte demandada que identificaba como sucesora a la supuesta viuda del finado, D./Dña. [NOMBRE Y APELLIDOS], proporcionando su domicilio, y pedía se le notificara la existencia del proceso, emplazándola para comparecer en el plazo de diez días.

Tercero

En diligencia de ordenación de [FECHA], se acordó de conformidad con lo solicitado por la parte demandada, y el [FECHA] se notificó a D./Dña. [NOMBRE Y APELLIDOS] la existencia de este juicio, sin que haya comparecido en el plazo que se le concedió, como delata la diligencia de constancia de fecha [FECHA].

Cuarto

En la sustanciación del presente juicio se han observado las formalidades que prescribe la Ley.

FUNDAMENTOS DE DERECHO

PRIMERO

Conforme al art. 16.2 LEC, constando el fallecimiento de un litigante se permitirá a las demás partes pedir, previa identificación de los sucesores y de sus domicilios, que se les emplace para comparecer en el proceso, y el 16.3, que tratándose del demandante, y sus sucesores no quisieran comparecer, se entenderá que la parte demandante renuncia a la acción ejercitada.

SEGUNDO

En el presente supuesto, la parte fallecida ha sido la actora, y la sucesora, que es legalmente su viuda D.//Dña. [NOMBRE Y APELLIDOS], sin aducir ninguna razón por la que no haya de tenérsele por tal, tampoco ha deseado comparecer en el juicio, puesto que, habiendo sido citada y emplazada para personarse en el plazo legal de diez días, ha dejado expirar el plazo sin haberlo verificado, por lo que procede dictar sentencia que tenga por renunciada a la parte actora de la acción ejercitada, con arreglo al art. 20.1 LEC.

TERCERO

En la instancia de los procesos declarativos rige, en punto a costas procesales, el principio cuasiobjetivo del vencimiento del art. 394 LEC, conforme al que la parte que ha visto rechazadas todas sus pretensiones debe ser condenada a su reembolso a la parte adversa, como ocurre con quien renuncia a la acción.

VISTOS los preceptos y jurisprudencia citados, y lo demás de general y pertinente aplicación, en ejercicio de la potestad jurisdiccional que emana de la soberanía popular,

FALLO

Con íntegra desestimación de la demanda deducida en su día por D./Dña. [NOMBRE Y APELLIDOS], que representaba el/la Procurador/a de los Tribunales D./Dña. [NOMBRE Y APELLIDOS], contra, representada por el/la Procurador/a de los Tribunales D./Dña. [NOMBRE Y APELLIDOS], debo tener, como tengo, por renunciada la pretensión ejercitada.

Absuelvo libremente a la mercantil demandada de los pedimentos que se le dirigían en el presente juicio.

Se imponen a la parte demandante las costas procesales causadas.

Notifíquese a las partes personadas y a la sucesora del que fuera demandante, con advertencia de que cabe recurso de apelación para ante la Ilma. Audiencia Provincial de [LOCALIDAD], que se interpondrá mediante escrito ante este Tribunal que se presente dentro de los veinte días hábiles siguientes al de notificación, exponiendo el apelante las alegaciones en que se base la impugnación, además de citar la resolución apelada y los pronunciamientos que impugna.

Para interponer el recurso será necesario la constitución de un depósito de 50 euros, sin cuyo requisito no será admitido a trámite. El depósito se constituirá consignando dicho importe en la Cuenta de Depósitos y Consignaciones que este Tribunal tiene abierta en el grupo [GRUPO] con el número [NÚMERO], indicando en el campo concepto del resguardo de ingreso que se trata de un "Recurso" código 02-Apelación. La consignación deberá ser acreditada al interponer el recurso (disp. adic. 15.ª de la LOPJ).

No están obligados a constituir el depósito para recurrir los declarados exentos en la disposición citada y quienes tengan reconocido el derecho a la asistencia jurídica gratuita.

Así, por esta mi sentencia, definitivamente juzgando, lo pronuncio, mando y firmo.

En [LUGAR], a [FECHA].

Firma del Juez:

PUBLICACIÓN: Leída y publicada fue la anterior sentencia por el Magistrado que la dictó, estando constituido en audiencia pública el día de la fecha. Doy fe.

Firma del Letrado de la Administración de Justicia

========================================================================
