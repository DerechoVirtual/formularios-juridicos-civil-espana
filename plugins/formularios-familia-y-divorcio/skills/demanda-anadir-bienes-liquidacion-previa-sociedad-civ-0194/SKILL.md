---
name: demanda-anadir-bienes-liquidacion-previa-sociedad-civ-0194
description: "Demanda para añadir bienes a una liquidación previa de la sociedad de gananciales. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda para añadir bienes a una liquidación previa de la sociedad de gananciales

> Formulario **CIV-0194** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Demanda ejercitando acción para adicionar al patrimonio ganancial de una previa liquidación de sociedad de gananciales bienes que al tiempo de formación del inventario eran desconocidos y cuyo conocimiento (o aparición) se produce en fecha posterior, por lo que no fueron reclamados para su inclusión en las operaciones divisorias en el anterior procedimiento liquidatorio

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda para añadir bienes a una liquidación previa de la sociedad de gananciales» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda para añadir bienes a una liquidación previa de la sociedad de gananciales” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-anadir-bienes-liquidacion-previa-sociedad-civ-0194`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] FECHA (4 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] SEDE (3 veces)
- [ ] DESCRIPCIÓN DEL BIEN (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NOMBRE DE LOS CÓNYUGES (2 veces)
- [ ] Nº DE PROCEDIMIENTO (2 veces)
- [ ] AÑO
- [ ] COLEGIO
- [ ] DENOMINACIÓN SOCIAL
- [ ] LUGAR
- [ ] MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO

## Normas que cita el formulario

- art. 45 LEC
- art. 50 LEC
- art. 253.1 LEC
- art. 251 LEC
- art. 249.2 LEC
- art. 5 Ley Orgánica 1/2025
- art. 1410 CC
- art. 1079 CC
- art. 394.1 LEC

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

### Avisos de actualización (3) — se aplican en el texto, nunca se copian en el documento

- Junto a «…MILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.
- Junto a «…[AÑO] llevadas a efecto en el Tribunal de Instancia, plaza n.º [NÚMERO], de esta»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, que actúa en nombre y representación de Doña [NOMBRE Y APELLIDOS], según consta debidamente acreditado en los autos de separación número [Nº DE PROCEDIMIENTO], bajo la dirección del Letrado ejerciente Don [NOMBRE Y APELLIDOS], colegiado n.º [NÚMERO] del Ilustre Colegio de Abogados de [COLEGIO], ante el Tribunal comparezco y, como mejor proceda en Derecho, DIGO:

Que en la representación que ostento, vengo a ejercitar ACCIÓN DE ADICIÓN O COMPLEMENTO a la LIQUIDACIÓN DE LA SOCIEDAD DE GANANCIALES formada con el demandado Don [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], aprobada en sentencia de separación matrimonial de mutuo acuerdo, con arreglo a los siguientes hechos y fundamentos jurídicos:

HECHOS

PRIMERO.- Que con fecha [FECHA], se dictó por el Tribunal de Instancia de [SEDE], plaza n.º [NÚMERO] sentencia de separación matrimonial de los cónyuges [NOMBRE DE LOS CÓNYUGES], en el seno de un procedimiento de mutuo acuerdo, que declaró disuelto el régimen económico matrimonial existente entre los mismos y aprobó el convenio regulador aportado a los autos, fechado el día [FECHA], en el que las partes procedieron a la liquidación del régimen conyugal de gananciales, sentencia que ha devenido firme.

Se acompaña como documento número [Nº DE DOCUMENTO] testimonio del convenio.

SEGUNDO.- En el citado convenio regulador, y entre otras estipulaciones, se procedió a formar inventario de los bienes integrantes de la sociedad legal de gananciales en su día constituida por los cónyuges [NOMBRE DE LOS CÓNYUGES] incluyendo en el activo tan sólo la vivienda sita en [LOCALIDAD], en tanto que el pasivo quedaba integrado por un préstamo bancario del que, en dicha fecha, quedaban por amortizar [IMPORTE] Sobre dichas bases se acordó adjudicar a la esposa el referido inmueble así como el pasivo, y a Don [NOMBRE Y APELLIDOS] la suma de

TERCERO.- Que por omisión no se incluyeron en el activo de la sociedad de gananciales los siguientes bienes [DESCRIPCIÓN DEL BIEN]; bienes que al tiempo de formación del inventario eran desconocidos para mi representada y cuyo conocimiento (o aparición) se produjo en fecha posterior, por lo que no fueron reclamados para su inclusión en las operaciones divisorias en el anterior procedimiento liquidatorio.

Para la acreditación de estos extremos se aporta el testimonio del resultado de las diligencias preliminares n.º [Nº DE PROCEDIMIENTO]/[AÑO] llevadas a efecto en el Tribunal de Instancia, plaza n.º [NÚMERO], de esta ciudad (documento número [Nº DE DOCUMENTO]).

La consecuencia de la omisión en el convenio de toda referencia a los mismos no es instar un nuevo proceso liquidatorio prescindiendo del precedente sino el ejercicio de la correspondiente acción de complemento o adición a la liquidación de gananciales ya efectuada, que habrá de limitarse a los bienes no incluidos en la liquidación ya practicada.

CUARTO.- Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento nº [Nº DE DOCUMENTO]

Pues bien, el demandado, secundado por el abogado de los servicios jurídicos de la empresa de aquél, y que redactó el convenio regulador, se ha negado a cualquier solución, y habida cuenta de que la acción que se está en la forzosidad de ejercitar tiene un plazo de prescripción, nos vemos obligados a acudir al Tribunal al que honro en dirigirme.

FUNDAMENTOS DE DERECHO

I.- COMPETENCIA.

Corresponde la competencia objetiva a los Tribunales de Instancia (arts. 45 LEC y 85.1º LOPJ) y la territorial al tribunal del lugar en que el demandado tiene su domicilio, conforme al fuero general de las personas físicas, establecido en el art. 50 LEC.

II.- LEGITIMACIÓN.

Corresponde a los cónyuges que fueron parte en el procedimiento de separación en que se acordó la liquidación de la sociedad de gananciales.

III.- CUANTÍA DEL PROCEDIMIENTO.

Cumpliendo lo prevenido en el art. 253.1 LEC, hacemos constar que la cuantía de esta demanda es [IMPORTE] euros, que se obtienen, en aplicación de la regla 12.ª del art. 251 LEC, del valor de los bienes cuya inclusión en la masa patrimonial se pretende, a cuyo efecto se acompaña certificación de los expertos inmobiliarios de la firma [DENOMINACIÓN SOCIAL].

IV.- PROCEDIMIENTO.

De conformidad con el art. 249.2 LEC, no existiendo un cauce especialmente previsto para las pretensiones que aquí se formulan, y siendo la cuantía superior a los 15.000 euros, el procedimiento que se debe seguir es el del juicio ordinario.

V.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

VI.- FONDO DEL ASUNTO.

Se ejercita acción de adición o complemento de bienes a una previa liquidación de gananciales, con amparo en lo previsto en el art. 1410 CCiv, por remisión general que hace a las reglas de la partición hereditaria en relación al art. 1079 CCiv, ambos del CCiv.

Es doctrina pacífica y asentada del Tribunal Supremo que la omisión voluntaria o involuntaria padecida con la no inclusión de un determinado bien en la liquidación de la sociedad de gananciales, con adjudicación de los bienes que la integraban, previo su inventario, carece de fuerza destructiva de la presunción de ganancialidad establecida, pues ni siquiera constituye acto propio vinculante, de manera que cuando se produce omisión de bienes en el inventario de la partición, lo que procede es su complemento o adición con los bienes omitidos (SSTS de 20 de noviembre de 1993, Rec. 3017/1991 y 25 de septiembre de 1995, Rec. 1121/1992) y el bien en conflicto sigue perteneciendo en copropiedad a ambos cónyuges.

El hecho de que en el convenio se haya omitido parte del activo no le quita eficacia y se mantiene subsistente, pues lo que procede es que se complete y adicione con lo olvidado, que es, vuelve a insistirse, lo que aquí se interesa con la demanda: ante la omisión voluntaria o involuntaria de bienes o valores, la solución que procede es su complemento y adición, y no habiéndose renunciado a ello por la parte actora, no vemos inconveniente en la adición o complemento de lo omitido, no habiendo operado el mecanismo de la prescripción.

VII.- COSTAS.

Conforme al principio del art. 394.1 LEC, del vencimiento objetivo, las costas irrogadas a esta parte se han de pronunciar a cargo del demandado.

SUPLICO AL TRIBUNAL

que teniendo por presentado este escrito con los documentos que lo acompañan y sus copias se sirva admitir uno y otros; en su virtud tener por interpuesta en la representación que ostento la presente demanda ejercitando acción de complemento o adición a la liquidación del régimen económico matrimonial de gananciales practicada, aprobada por el Tribunal de Instancia de [SEDE] por sentencia de fecha [FECHA], y seguido que sea el procedimiento oportuno, dicte resolución por la que se acuerde adicionar al inventario de bienes gananciales dentro de la partida correspondiente al activo del patrimonio ganancial los siguientes bienes: [DESCRIPCIÓN DEL BIEN], con imposición expresa de costas a la contraparte.

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a

========================================================================
