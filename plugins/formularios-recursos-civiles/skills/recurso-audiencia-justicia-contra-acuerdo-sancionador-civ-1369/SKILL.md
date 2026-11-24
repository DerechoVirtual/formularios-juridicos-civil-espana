---
name: recurso-audiencia-justicia-contra-acuerdo-sancionador-civ-1369
description: "Recurso de audiencia en justicia contra el acuerdo sancionador por vulnerar la buena fe procesal. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Recurso de audiencia en justicia contra el acuerdo sancionador por vulnerar la buena fe procesal

> Formulario **CIV-1369** del plugin **Recursos civiles: reposición, apelación, casación y queja** (`formularios-recursos-civiles`) · Civil › Recursos · normativa revisada el 24-11-2026.

## Qué es

Recurso de audiencia en justicia ante el Tribunal que dictó acuerdo sancionador por vulneración de la buena fe procesal adoptado en el mismo procedimiento.

Es un modelo de tipo **recursos**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Recurso de audiencia en justicia contra el acuerdo sancionador por vulnerar la buena fe procesal» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Recurso de audiencia en justicia contra el acuerdo sancionador por vulnerar la buena fe procesal” para mi caso». También puedes invocarla directamente con `/formularios-recursos-civiles:recurso-audiencia-justicia-contra-acuerdo-sancionador-civ-1369`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-recursos-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Recursos civiles: reposición, apelación, casación y queja) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (7 veces)
- [ ] LUGAR (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] IMPORTE
- [ ] NOMBRE O UBICACIÓN DE LA COMUNIDAD
- [ ] Nº
- [ ] SEDE

## Normas que cita el formulario

- art. 556 LOPJ
- art. 247.3 LEC
- art. 557 LOPJ
- art. 241.1 LOPJ

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Notas al pie del formulario original:
(1) No deja de ser debatible que el régimen procedimental de la imposición de sanciones por vulneración de la buena fe procesal, que no se establece en el art. 247 LEC, se corresponda con las correcciones disciplinarias, y sea de aplicación el art. 557 LOPJ, y por ende, ese Título V del Libro VII de dicha Ley, pensadas, como sanciones administrativas para corregir a profesionales, y no a las partes, y no por la conducta procesal, sino por desobedecer o faltar al respeto al tribunal en actuación forense, no asistir ante éste, o incumplir los deberes de representación o defensa. En todo caso, si la sanción procesal se merece en muchos casos de dilaciones abusivas, tiene poco sentido recargar al órgano sancionador con la apertura de un expediente, con alegaciones previas al acuerdo, recurso de audiencia en justicia, y una alzada.

En cualquier caso, parece que el expediente sancionador, una vez notificadas todas las partes de su apertura, se entiende solamente entre la parte sancionada y el tribunal o tribunales sancionadores.

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales y de D./Dña. [NOMBRE Y APELLIDOS], cuyas circunstancias constan en autos de juicio de división de patrimonio nº [Nº]/02, ante el Tribunal comparezco y como mejor en Derecho proceda, DIGO:

Que el día [FECHA], se ha notificado a esta parte acuerdo del Tribunal al que me dirijo, el cual forma parte del Auto de [FECHA] anterior, por medio del que impone a esta parte la multa de [IMPORTE] euros, por vulneración del principio de buena fe procesal, frente al que, dentro del plazo de cinco días del art. 556 LOPJ, formulo RECURSO DE AUDIENCIA EN JUSTICIA, con base en las siguientes

ALEGACIONES

PRIMERA

El Auto en que se impone la sanción es resolutorio de escrito de aclaración del de fecha [FECHA], que resolviera solicitud de nulidad de actuaciones planteada por esta parte con relación a las que han seguido a la providencia que tuvo por no comparecida a la Comunidad de Propietarios de [NOMBRE O UBICACIÓN DE LA COMUNIDAD], razonando simplemente que se trata una aclaración pedida sin fundamento, y de vocación clara dilatoria, que hace incurrir en mala fe procesal, sancionable ex art. 247.3 LEC.

SEGUNDA

Falta de previa audiencia.

La sanción pecuniaria por estimarse vulnerada la buena fe procesal se trata de una corrección disciplinaria, a la que debe aplicarse, por remisión del art. 557 LOPJ, el régimen del Título V del Libro VII LOPJ, de modo que está prevista un acta secretarial que hace de pliego de cargos, y de la que debe darse traslado al sujeto pasivo antes de resolver el órgano judicial mediante acuerdo gubernativo.

El Derecho sancionador de naturaleza administrativa requiere la previa audiencia del administrado, lo cual se ha omitido en este caso, por lo que debe anularse la sanción impuesta.

TERCERA

Inexistencia de mala fe procesal.

Esta parte considera que no ha conculcado el deber de buena fe procesal, puesto que si hubiera creído que el Auto cuya aclaración se solicitaba no precisaba de ninguna, tampoco se hubiera solicitado, y la falta de sintonía entre la comprensión de esta parte y de quien resuelve no permite hacer supuesto de la cuestión.

Por otro lado, la intencionalidad meramente dilatoria no tiene sentido presumirla de una aclaración que se solicita al de dos días de la notificación, y precisamente contra un Auto que resulta irrecurrible (art. 241.1 LOPJ), de modo que, no suspendido el proceso, ha podido haber algún acto superfluo a juicio de S.Sª., pero no una dilación -ya que no hay un plazo de recurso que supuestamente se dilata mediante este expediente aclaratorio-, debiendo significarse, con todo respeto que el presente juicio de partición hereditaria se ha prolongado indebidamente por sucesivos errores de trámite, que ha denunciado esta parte a través de varios recursos de reposición estimados (se señalan los Autos de fechas [FECHA] y [FECHA]).

CUARTA

Irrelevancia del juicio de intenciones.

La buena fe procesal es un concepto jurídico indeterminado que apunta a deberes de veracidad, probidad y lealtad en el proceso, que no pueden calificarse por una culpa o voluntad maliciosa (vid. SSTS de 12 de marzo, rec. 1788/1995, y 15 de abril de 1998, rec. 637/1994) adivinada en el litigante, como puede pensarse de que la sanción impuesta califique de ‘treta’ a la solicitud de aclaración, sino que es algo objetivo, por alejarse la parte procesal de un estándar de actuación correcta, y no es el caso.

QUINTA

Ausencia de perjuicio.

Por último, si el criterio de proporcionalidad de la sanción del art. 247.3 LEC se individualiza expresamente conforme a los perjuicios al procedimiento o a las demás partes, la solicitud de aclaración ningún perjuicio puede derivar, careciendo la misma del menor atisbo de desconsideración para con el tribunal, ante al que se formula protesta de no haberla nunca abrigado.

En virtud de lo expuesto,

SUPLICO AL TRIBUNAL

que, por presentado este escrito, se digne tener por hechas las manifestaciones precedentes, y en mérito a las mismas, deje sin efecto la resolución sancionadora dictada en el Auto de

Es Justicia de hacerse en [LUGAR], a [FECHA].

Es justicia de hacerse en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a
