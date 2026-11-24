---
name: escrito-oposicion-motivos-fondo-ejecucion-auto-cuantia-civ-1419
description: "Escrito de oposición por motivos de fondo a la ejecución con auto de cuantía máxima. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito de oposición por motivos de fondo a la ejecución con auto de cuantía máxima

> Formulario **CIV-1419** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Escrito del ejecutado de oposición a la demanda ejecutiva por motivos de fondo (concretamente sobre el auto de cuantía máxima), apreciando la concurrencia de culpas o responsabilidad compartida.

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito de oposición por motivos de fondo a la ejecución con auto de cuantía máxima» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito de oposición por motivos de fondo a la ejecución con auto de cuantía máxima” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:escrito-oposicion-motivos-fondo-ejecucion-auto-cuantia-civ-1419`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (4 veces)
- [ ] NÚMERO (2 veces)
- [ ] ASEGURADORA
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] MARCA Y MATRÍCULA DEL VEHÍCULO
- [ ] NOMBRE DE LA PARTE
- [ ] NOMBRE DEL SOLICITANTE
- [ ] NOMBRE Y APELLIDOS
- [ ] NORMAS INFRINGIDAS
- [ ] Nº DE DOCUMENTO
- [ ] SEDE

## Normas que cita el formulario

- art. 1.968.2.º CC
- art. 556.3.1.ª LEC
- art. 556.3.3.ª LEC
- art. 557.1.3.ª LEC

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS] Procurador/a de los Tribunales, en nombre y representación de la Compañía de Seguros [ASEGURADORA], con domicilio en [LOCALIDAD] y C.I.F. número [NÚMERO], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], ante el Tribunal comparezco y como mejor proceda en derecho DIGO:

Que en nombre de mi poderdante me persono en los autos de ejecución seguidos a instancia de [NOMBRE DEL SOLICITANTE] y registrados con el número [NÚMERO], y por medio del presente escrito formulo OPOSICIÓN a la citada ejecución, dentro del plazo concedido al efecto, en virtud de los siguientes

HECHOS

PRIMERO.- Antes de entrar a examinar los hechos base de la ejecución que se acordó por auto de fecha [FECHA], procede indicar que ha transcurrido el plazo de un año establecido en el art. 1.968.2.º CCiv para la prescripción de la acción dirigida a exigir la responsabilidad civil derivada de culpa o negligencia porque el accidente tuvo lugar, según consta en el procedimiento, el día [FECHA] y la demanda ejecutiva se interpuso el día [FECHA], mediando entre ambas fechas más de un año.

SEGUNDO.- Entrando a examinar las alegaciones de contrario, procede manifestar en primer lugar nuestra total discrepancia con la versión de los hechos formulada ya que si el accidente tuvo lugar fue por culpa exclusiva del ejecutante que conducía ese día el vehículo [MARCA Y MATRÍCULA DEL VEHÍCULO] (narrar los hechos). Concurre por tanto la causa de oposición prevista en el art. 556.3.1.ª LEC, consistente en culpa exclusiva de la víctima.

TERCERO.- En el supuesto de que se considerara que el accidente no tuvo lugar por culpa exclusiva del ejecutante, sino por haber intervenido en cierta medida el vehículo asegurado por mi representada, deberá declararse la responsabilidad compartida en cuanto a que el ejecutante incumplió las normas básicas de precaución exigibles a todo conductor en base al principio de confianza en la circulación, además de haber infringido las siguientes normas de tráfico [NORMAS INFRINGIDAS], siendo ínfima la participación del conductor del vehículo asegurado en esta entidad y, en todo caso, solo determinante del incremento de los daños.

De conformidad con lo expuesto, sería apreciable la causa de oposición contemplada en el art. 556.3.3.ª LEC, concurrencia de culpas.

CUARTO.- Por último manifestar que la reclamación formulada en concepto de secuela por perjuicio estético es de todo punto exagerada, de acuerdo con el baremo aplicable, ya que le corresponderían menos puntos de los asignados por la ejecutante, si tenemos en cuenta que

De conformidad con estas alegaciones, para el supuesto de que no se estimaran las causas anteriormente opuestas, concurriría la de pluspetición contemplada en el art. 557.1.3.ª LEC.

FUNDAMENTOS DE DERECHO

I.- Negamos que sean de aplicación al presente caso los fundamentos de derecho alegados por el ejecutante.

II.- Damos por reproducidos los preceptos legales citados en los hechos enumerados en este escrito de oposición a la ejecución despachada.

Por otro lado, de conformidad con lo establecido en los arts. 556.3 y 557.2, la oposición del ejecutado suspenderá la ejecución.

III.- Las costas procesales, a tenor de lo preceptuado en el art. 561.2, deberán ser impuestas al ejecutante.

En virtud de todo lo expuesto,

SUPLICO AL TRIBUNAL:

que tenga por presentado este escrito con sus copias y me tenga por comparecido y parte en la representación que ostento de [NOMBRE DE LA PARTE] en el expresado procedimiento de ejecución y mandar que se entiendan conmigo las actuaciones que a partir de este momento se realicen, teniendo por formulada en tiempo y forma oposición a la ejecución despachada, suspendiéndose el curso de la misma, para que, tras la correspondiente tramitación, se dicte auto declarando que no procede la ejecución dejando ésta sin efecto y mandando alzar los embargos y las medidas de garantía de la afección que se hubieran adoptado, reintegrándose al ejecutado a la situación anterior al despacho de la ejecución, con imposición de las costas al ejecutante.

Es de Justicia que pido en [LUGAR], a [FECHA].

OTROSÍ DIGO.- Que interesa al derecho de esta parte la celebración de vista, por lo que se solicita del Tribunal que se señale un día para su celebración dentro de los diez días siguientes a la conclusión del trámite de impugnación a este escrito de oposición

Es justicia que reitero en lugar y fecha indicados.

Firma del Abogado/a	Firma del Procurador/a

========================================================================
