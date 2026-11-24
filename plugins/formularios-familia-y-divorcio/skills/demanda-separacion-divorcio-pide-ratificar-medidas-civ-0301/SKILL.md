---
name: demanda-separacion-divorcio-pide-ratificar-medidas-civ-0301
description: "Demanda de separación o divorcio que pide ratificar medidas del Juzgado de Violencia sobre la Mujer. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de separación o divorcio que pide ratificar medidas del Juzgado de Violencia sobre la Mujer

> Formulario **CIV-0301** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Demanda de separación o divorcio, solicitando la ratificación de las medidas adoptadas por la Sección de Violencia sobre la Mujer o de Instrucción del Tribunal de Instancia, conforme a lo establecido en el art. 544 ter de la LECr.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de separación o divorcio que pide ratificar medidas del Juzgado de Violencia sobre la Mujer» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de separación o divorcio que pide ratificar medidas del Juzgado de Violencia sobre la Mujer” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-separacion-divorcio-pide-ratificar-medidas-civ-0301`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (6 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] Nº DE DOCUMENTO (4 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] DOCUMENTO QUE SE ADJUNTA
- [ ] EDAD
- [ ] EXPONER LOS HECHOS
- [ ] LUGAR
- [ ] MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] NOMBRE DEL HIJO/A 1
- [ ] NOMBRE DEL HIJO/A 2
- [ ] Nº
- [ ] ÓRGANO ADMINISTRATIVO

## Normas que cita el formulario

- art. 544 ter LEC
- art. 81 CC
- art. 86 CC
- art. 437 LEC
- art. 753 LEC
- art. 770 LEC
- art. 10.1 LEC
- art. 437.1 LEC
- art. 5 Ley Orgánica 1/2025
- art. 91 CC
- art. 394 LEC
- art. 773 LEC

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

- Junto a «…ENCIA SOBRE LA MUJER / SECCIÓN CIVIL / SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD]»: Denominación legal: Sección de Familia, Infancia y Capacidad. Si no existe en el partido, conoce la Sección Civil o la Única (art. 86.3-4 LOPJ). Fuente: LOPJ arts. 84.2.a) y 86 (redacc. LO 1/2025, BOE-A-2025-76).

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

AL TRIBUNAL DE INSTANCIA [ELEGIR: SECCIÓN DE VIOLENCIA SOBRE LA MUJER / SECCIÓN CIVIL / SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD]

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, en representación de D [NOMBRE Y APELLIDOS], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño a este escrito, ante el Tribunal, comparezco, y como mejor proceda en Derecho, DIGO:

Que con fecha [FECHA], por el Tribunal de Instancia [ELEGIR: Sección de Violencia sobre la Mujer / Sección de Instrucción] se dictó Auto acordando la orden de protección prevista en el art. 544 ter de la Ley de Enjuiciamiento Criminal, acordando las medidas civiles que constan en el mismo, el cual se acompaña como documento número 1 de la presente demanda.

Que dentro del plazo establecido en el párrafo 3 del apartado 7 del art. 544 ter de la LECr, por medio del presente escrito, promuevo DEMANDA DE [ELEGIR: SEPARACIÓN / DIVORCIO] contra el/la esposo/a de mi representado/a de conformidad con lo dispuesto en el art. 81 CCiv —para la separación—/art. 86 CCiv —para el divorcio—..

Que desde este momento anunciamos la solicitud de RATIFICACIÓN DE LAS MEDIDAS CIVILES adoptadas en el mencionado auto toda vez que las mismas, tal y como se va a pasar a razonar, son las más adecuadas para regir la nueva situación de [ELEGIR: separación / divorcio]

Todo ello de conformidad con los siguientes,

HECHOS

PRIMERO.- Dña. y D. contrajeron matrimonio canónico en [LOCALIDAD], el día [FECHA], a cuya acreditación se acompaña certificación expedida por el Registro Civil de [LOCALIDAD], como documento número [Nº DE DOCUMENTO].

SEGUNDO.- Del referido matrimonio nacieron y viven dos hijos, de nombres [NOMBRE DEL HIJO/A 1] y [NOMBRE DEL HIJO/A 2], menores de edad, que tienen [EDAD] y [Nº] años respectivamente, como se demuestra con sendas certificaciones registrales que se presentan como documentos números [Nº DE DOCUMENTO] y [Nº DE DOCUMENTO].

TERCERO.-

[OPCIONAL — incluir si procede]

[OPCIONAL — incluir si procede]

Que habiendo transcurrido tres meses desde la celebración del matrimonio mi representada/o ha decidido poner fin a la convivencia matrimonial.

CUARTO.- El régimen conyugal de bienes es el de sociedad de gananciales, por la vecindad de los consortes y no haberse otorgado nunca capitulaciones matrimoniales, siendo el domicilio conyugal herencia del demandado D. [NOMBRE Y APELLIDOS], y por lo tanto, bien privativo del mismo, teniendo conocimiento de que el demandado ha ido contrayendo innumerables deudas, que amenazan ese patrimonio.

QUINTO.- El demandado es funcionario del Ministerio de [ÓRGANO ADMINISTRATIVO], mientras que mi patrocinada carece de ingresos propios, y aún de cualificación profesional de cualquier tipo.

Se adjunta [DOCUMENTO QUE SE ADJUNTA], al objeto de demostrar las rentas de la unidad familiar, copias de la declaración —conjunta— del I.R.P.F. del año pasado y el anterior, como documentos números 6 y 7.

SEXTO.- [EXPONER LOS HECHOS])

SÉPTIMO.- Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento nº [Nº DE DOCUMENTO]

FUNDAMENTOS DE DERECHO

I.- Es competente el Tribunal de Instancia (Sección Civil/de Violencia/Familia) del lugar del domicilio conyugal conforme al art. 769.1, párrafo 1.º LEC

II.- El proceso adecuado es el del juicio verbal (arts. 437 LEC y ss.), como se diseña especialmente por el art. 753 LEC, y con las peculiaridades del art. 770 LEC para conocer de las demandas contenciosas de separación.

III.- Tiene la demandante legitimación activa ordinaria por hallarse en la situación jurídica de relación conyugal, como detenta la pasiva su marido demandado (art. 81 CCiv y art. 10.1 LEC), siendo el objeto del proceso principal la pretensión de separación conyugal y la adopción de medidas definitivas derivadas de la misma.

IV.- La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 en relación con el art. 437.1 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

V.- El fondo de la pretensión consiste en la declaración de separación conyugal (o divorcio) sin consenso de los cónyuges, a instancia de uno de ellos por existencia de un riesgo para la vida, la integridad física, la libertad, la integridad moral o libertad o indemnidad sexual del cónyuge demandante o de los hijos de ambos o de cualquiera de los miembros del matrimonio (o bien) por el mero transcurso de tres meses desde la celebración del matrimonio.

VI.- Conforme a los arts. 91 CCiv y 774 LEC, el Tribunal deberá pronunciarse en definitiva sobre las medidas que se solicitarán que se adopten con carácter de provisionales, acerca de los hijos, vivienda, alimentos, pensión compensatoria y régimen matrimonial de bienes, las cuales se pretenden igualmente como definitivas.

En tal sentido, esta parte pretende que sean ratificadas las medidas civiles adoptadas en la orden de protección dictada por el Tribunal de Instancia [ELEGIR: Sección de Instrucción / Sección de Violencia sobre la Mujer] con fecha [FECHA], y ello por cuanto

)

VII.- Las costas procesales deben ser impuestas a la parte demandada, por criterio del íntegro vencimiento, en atención al art. 394 LEC.

Y demás normas y jurisprudencia de general y pertinente aplicación.

SUPLICO AL TRIBUNAL.-

Que tenga por presentado este escrito de demanda y documentos que lo acompañan, los admita a trámite, y en su virtud, y previos los trámites legales, dicte sentencia por la que se declare [ELEGIR: la separación / el divorcio] del matrimonio formado por mi representado/a y [NOMBRE Y APELLIDOS], con la adopción de las siguientes medidas:

(Se reiterará la solicitud de las medidas adoptadas en sede penal con las ampliaciones que procedan respecto a pensión compensatoria)

OTROSÍ DIGO: Que esta parte interesa la adopción de medidas provisionales al amparo de lo dispuesto en el art. 773 de la LEC, y de conformidad a lo previsto en el tercer párrafo del apartado 7 del art. 544 ter de la Ley de Enjuiciamiento Criminal, se solicita como tales la ratificación de las medidas de carácter civil acordadas por el Tribunal de Instancia
Sección de Instrucción
Sección de Violencia sobre la Mujer
  mediante Auto de fecha [FECHA] por mantenerse las circunstancias que fueron tenidas en cuenta para acordarlas, como se recoge en los hechos de la demanda a los que nos remitimos.

SUPLICO AL TRIBUNAL que acuerde la RATIFICACIÓN DE LAS MEDIDAS DE CARÁCTER CIVIL acordadas por el Tribunal de Instancia [ELEGIR: Sección de Instrucción / Sección de Violencia sobre la Mujer] mediante Auto de fecha [FECHA].

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a

========================================================================
