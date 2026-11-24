---
name: demanda-modificacion-medidas-definitivas-proceso-civ-0124
description: "Demanda de modificación de las medidas definitivas de un proceso matrimonial (Derecho catalán). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de modificación de las medidas definitivas de un proceso matrimonial (Derecho catalán)

> Formulario **CIV-0124** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de modificación de las medidas definitivas de un proceso matrimonial (Derecho catalán)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de modificación de las medidas definitivas de un proceso matrimonial (Derecho catalán)” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-modificacion-medidas-definitivas-proceso-civ-0124`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] IMPORTE (4 veces)
- [ ] Nº (3 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] SEDE (3 veces)
- [ ] AÑO (2 veces)
- [ ] FECHA (2 veces)
- [ ] FECHA DE LA SENTENCIA (2 veces)
- [ ] MES (2 veces)
- [ ] CALLE
- [ ] DÍA
- [ ] EDAD DEL HIJO
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] PISO
- [ ] PUERTA

## Normas que cita el formulario

- art. 233 Código Civil
- art. 233 CC
- art. 769 LEC
- art. 775 LEC
- art. 437.1 LEC
- art. 5 Ley Orgánica 1/2025

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

### Avisos de actualización (4) — se aplican en el texto, nunca se copian en el documento

- Junto a «…MILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.
- Junto a «…n [NOMBRE Y APELLIDOS] ante la Sección Civil del Tribunal de Instancia de [SEDE]»: Un solo TI por partido judicial (art. 84.1 LOPJ): sobra «de los de». Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).
- Junto a «…curador ========================================================================»: requisito de procedibilidad del art. 5 LO 1/2025 — antes de presentar la demanda hay que intentar un medio adecuado de solución de controversias (MASC) y acreditarlo con la demanda (arts. 264.4.º y 399.3 LEC), salvo las materias excluidas del art. 5.2. Fuente: LO 1/2025, arts. 5 a 7 (BOE-A-2025-76).

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

Don [NOMBRE Y APELLIDOS] Procurador de los Tribunales, en la representación que ostento de D [NOMBRE Y APELLIDOS], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], y bajo la dirección Letrada de Don [NOMBRE Y APELLIDOS] ante la Sección Civil del Tribunal de Instancia de [SEDE] que por turno de reparto corresponda (o Sección de Familia, Infancia y Capacidad o de Violencia sobre la Mujer) comparezco y como mejor proceda en Derecho, DIGO:

Que siguiendo instrucciones de mi poderdante, al amparo de lo dispuesto en el artículo 233-7 del Código Civil de Cataluña, por medio del presente escrito, solicito MODIFICACIÓN DE LAS MEDIDAS DEFINITIVAS acordadas en la sentencia de fecha [FECHA DE LA SENTENCIA], contra Doña [NOMBRE Y APELLIDOS], vecina de la localidad de [LOCALIDAD], con domicilio en calle [CALLE], núm. [Nº], piso [PISO], puerta [PUERTA], la cual baso en los siguientes

HECHOS

En virtud de sentencia firme de divorcio fechada el día [FECHA], del mes [MES], del año [AÑO], dictada por la Sección Civil del Tribunal de Instancia (o Familia) núm. [Nº] de los de [SEDE], en autos /, se acordó la disolución por divorcio del matrimonio de mis representados, fijando, entre otras medidas definitivas y por lo que ahora interesa, una prestación compensatoria a satisfacer por mi representado a la demandada por importe de [IMPORTE] euros mensuales, actualizables conforme al índice del IPC, de forma vitalicia.

Para adoptar la medida cuya modificación ahora se pretende se tomó en consideración que el matrimonio no tenía hijos y que la esposa se había dedicado a las labores domésticas durante todo el tiempo de la convivencia.

Esta situación ha variado sustancialmente de forma sobrevenida, pues mi representado, tras divorciarse, inició una relación de pareja estable con Dª, habiendo tenido dos hijos con posterioridad a dictarse la sentencia de divorcio, en la actualidad de [EDAD DEL HIJO] y [Nº] años de edad, los cuales debe alimentar mi representado y que inciden negativamente en su capacidad económica, originándole nuevos gastos familiares ( acompaño como documentos [Nº DE DOCUMENTO] escritura de constitución de unión estable y certificado de nacimiento de los hijos). E

Por otra parte, también ha incidido en su capacidad económica las sucesivas rebajas salariales que se han venido produciendo en el ámbito de su empresa pública, lo cual ha supuesto una mengua considerable de los ingresos de mi representado en este período, viéndose reducidas las retribuciones percibidas al tiempo del divorcio en la cantidad de [IMPORTE] euros mensuales ( acompaño como documentos [Nº DE DOCUMENTO] certificado de la empresa donde se relacionan las retribuciones correspondientes a los años)

A la vista de dichas circunstancias sobrevenidas, verdaderamente transcendentes, fundamentales y permanentes, que le impiden hacer frente a la pensión compensatoria fijada en la sentencia, y no imputables en ningún caso a la voluntad de mi representado, instamos, al amparo de los artículos 233-7 y 233-18 del CC de Cataluña, la modificación de la pensión compensatoria que debe satisfacer mi representado, proponiendo la de [IMPORTE] euros mensuales, como más ajustada a las nuevas circunstancias concurrentes.

(caso de mediación) A fin de solventar la controversia mi representado intentó llegar a un acuerdo extrajudicial con la demandada, iniciando un proceso de mediación ante la entidad en fecha [FECHA], no habiendo podido lograrse un acuerdo, por lo que se está en el caso de solicitar que la modificación se retrotraiga a la fecha de inicio del proceso de mediación, según dispone el artículo 233-7.3 del Código Civil de Cataluña.

A los anteriores Hechos le son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

Competencia. Es competente el Tribunal al que me dirijo conforme a lo dispuesto en el artículo 769 de la LEC.

Procedimiento. Debe seguirse el procedimiento de modificación de medidas establecido en el artículo 775 de la LEC, el cual remite al artículo 770 del mismo texto legal.

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC en relación con el art. 437.1 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

Modificación de medidas. Es de aplicación el artículo 233-7 del CC de Cataluña que dispone que "las medidas ordenadas en un proceso matrimonial pueden modificarse mediante una resolución judicial posterior, si varían sustancialmente las circunstancias concurrentes en el momento de dictarlas". En el caso de la prestación compensatoria, es de aplicación el artículo 233-18 del mismo texto legal que establece que "la prestación compensatoria fijada en forma de pensión sólo puede modificarse para disminuir su importe si mejora la situación económica de quien la percibe o empeora la de quien la paga", añadiendo el apartado 2 que "para determinar la capacidad económica del deudor deben tenerse en cuenta sus nuevos gastos familiares y debe darse prioridad al derecho de alimentos de todos sus hijos".

Costas. Artículo 394 de la LEC.

En su virtud

SUPLICO AL TRIBUNAL: Que tenga por presentado este escrito con los documentos acompañados y sus copias; admita todo ello; por interpuesta solicitud de modificación de medidas definitivas por el Procurador que suscribe, en nombre y representación de Don [NOMBRE Y APELLIDOS], y, tras los trámites legales, acuerde la modificación de la medida definitiva de pensión compensatoria fijada en la sentencia de fecha [FECHA DE LA SENTENCIA], fijando en su lugar una pensión por importe de [IMPORTE] euros mensuales (caso de intento de mediación, retrotrayendo sus efectos a la fecha de inicio del procedimiento de mediación). Todo ello con condena en costas a la parte demandada, si concurrieren las circunstancias previstas en el artículo 394 de la Ley de Enjuiciamiento Civil.

Es justicia que insto en [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma de Abogado y Procurador

========================================================================
