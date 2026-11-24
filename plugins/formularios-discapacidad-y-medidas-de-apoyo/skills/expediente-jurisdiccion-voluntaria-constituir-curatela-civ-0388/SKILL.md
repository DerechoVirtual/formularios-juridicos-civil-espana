---
name: expediente-jurisdiccion-voluntaria-constituir-curatela-civ-0388
description: "Expediente de jurisdicción voluntaria para constituir curatela de menor emancipado (Cataluña). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Expediente de jurisdicción voluntaria para constituir curatela de menor emancipado (Cataluña)

> Formulario **CIV-0388** del plugin **Discapacidad y medidas de apoyo (Ley 8/2021)** (`formularios-discapacidad-y-medidas-de-apoyo`) · Civil › Capacidad y medidas de apoyo · normativa revisada el 24-11-2026.

## Qué es

Escrito de iniciación de un expediente de jurisdicción voluntaria en el que un menor emancipado solicita la constitución de la curatela y el nombramiento de curador para completar su capacidad en un acto concreto (por ejemplo, la venta de un inmueble), conforme al Código Civil de Cataluña.

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Expediente de jurisdicción voluntaria para constituir curatela de menor emancipado (Cataluña)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Expediente de jurisdicción voluntaria para constituir curatela de menor emancipado (Cataluña)” para mi caso». También puedes invocarla directamente con `/formularios-discapacidad-y-medidas-de-apoyo:expediente-jurisdiccion-voluntaria-constituir-curatela-civ-0388`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-discapacidad-y-medidas-de-apoyo:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Discapacidad y medidas de apoyo (Ley 8/2021)) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] DOMICILIO (4 veces)
- [ ] DOMICILIO DEL INMUEBLE (3 veces)
- [ ] FECHA (3 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] NOMBRE Y APELLIDOS DEL TESTIGO (2 veces)
- [ ] SEDE (2 veces)
- [ ] AÑO
- [ ] CORREO ELECTRÓNICO
- [ ] DOMICILIO PROFESIONAL
- [ ] DÍA
- [ ] EDAD
- [ ] LOCALIDAD
- [ ] MES
- [ ] NOMBRE Y APELLIDOS DE LA PERSONA PROPUESTA
- [ ] NOMBRE Y APELLIDOS DE LA PERSONA PROPUESTA COMO CURADOR
- [ ] NOMBRE Y APELLIDOS DEL CURADOR
- [ ] NOMBRE Y APELLIDOS DEL LETRADO
- [ ] Nº
- [ ] PARENTESCO O RELACIÓN CON EL SOLICITANTE
- [ ] PARENTESCO Y NOMBRE DE LOS FAMILIARES
- [ ] TELÉFONO

## Normas que cita el formulario

- art. 223 Código Civil
- art. 211 Código Civil
- art. 222 Código Civil
- art. 43 Ley 15/2015

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

- Junto a «…MILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.

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

[NOMBRE Y APELLIDOS], [ELEGIR: actuando en su propio nombre y representación / actuando por medio de procurador], menor de edad emancipado por resolución de fecha [FECHA], y bajo la dirección letrada de [NOMBRE Y APELLIDOS DEL LETRADO], al amparo de lo dispuesto en el artículo 223-5 del Código Civil de Cataluña, ante la Sección Civil del Tribunal de Instancia de [SEDE] que por turno de reparto corresponda, comparezco y, como mejor proceda en Derecho, DIGO:

Que mediante el presente escrito promuevo expediente de jurisdicción voluntaria para el NOMBRAMIENTO DE CURADOR que complemente mi capacidad en [ASUNTO PARA EL QUE SE SOLICITA EL NOMBRAMIENTO: por ejemplo, la venta de la vivienda sita en [DOMICILIO DEL INMUEBLE], heredada de mis padres], en base a los siguientes

HECHOS

PRIMERO.– Que el solicitante tiene [EDAD] años de edad, estando en situación de emancipación otorgada por resolución judicial de fecha [FECHA], habiendo fallecido sus padres en fecha [FECHA]. Se acompañan como DOCUMENTOS Nº [Nº] testimonio de la resolución judicial y certificados de defunción.

SEGUNDO.– Como consecuencia del fallecimiento de sus padres y a fin de [FINALIDAD: por ejemplo, continuar con sus estudios], el solicitante se ve en la obligación de [ACTO PARA EL QUE SE REQUIERE EL COMPLEMENTO DE CAPACIDAD: por ejemplo, enajenar la vivienda sita en [DOMICILIO DEL INMUEBLE], heredada de sus padres], acto que requiere el complemento de capacidad a que se refiere el artículo 211-12 del Código Civil de Cataluña, por lo que es necesario solicitar la constitución de la curatela y el nombramiento de curador, tal como establece el artículo 223-5 del mismo cuerpo legal, por ser precisa la intervención de curador en dicho acto.

TERCERO.– En relación con el nombramiento, y no habiendo realizado los padres del solicitante ningún acto de delación voluntaria, respecto a lo establecido en el artículo 222-10 del Código Civil de Cataluña el solicitante hace constar que [DESCRIPCIÓN DE LA SITUACIÓN FAMILIAR: por ejemplo, es hijo único, han fallecido sus padres y abuelos, y tiene como familiares más próximos a [PARENTESCO Y NOMBRE DE LOS FAMILIARES]], manteniendo una especial relación afectiva con [NOMBRE Y APELLIDOS DE LA PERSONA PROPUESTA COMO CURADOR], con quien actualmente convive, por lo que es indudable que defenderá los intereses del solicitante como si fueran propios.

[Nota de ayuda: en el asunto se expresará el acto concreto para el que se necesita el curador; los documentos que se acompañan se relacionarán por su número.]

FUNDAMENTOS DE DERECHO

Competencia

Son competentes los Tribunales de Instancia de esta ciudad, por ser el del domicilio del menor, conforme a lo dispuesto en el artículo 43 de la Ley 15/2015, de 2 de julio, de la Jurisdicción Voluntaria.

Procedimiento

Debe seguirse el procedimiento de jurisdicción voluntaria regulado en los artículos 44 y siguientes de la Ley de la Jurisdicción Voluntaria.

Legitimación

Esta parte está legitimada conforme a lo dispuesto en el artículo 223-5 del Código Civil de Cataluña.

Fundamentos de fondo

El artículo 223-5 del Código Civil de Cataluña establece que la curatela de los menores emancipados solo debe constituirse, a instancia de estos, cuando sea precisa la intervención del curador, siendo de aplicación el régimen jurídico de la tutela en lo que no se oponga al régimen de la curatela, debiendo procederse al nombramiento de curador conforme al artículo 222-10, de acuerdo con la voluntad, preferencias y deseos del solicitante, quien solicita que sea nombrado [NOMBRE Y APELLIDOS DE LA PERSONA PROPUESTA], [PARENTESCO O RELACIÓN CON EL SOLICITANTE].

Por lo expuesto,

AL TRIBUNAL SUPLICO: Que tenga por presentado este escrito con los documentos que se acompañan, lo admita, y tenga por promovido expediente de jurisdicción voluntaria de constitución de curatela y nombramiento de curador del solicitante, y practicadas las diligencias oportunas, incluida la información testifical que se interesa en el otrosí y con intervención del Ministerio Fiscal, y previos los demás trámites con arreglo a Derecho, dicte resolución en la que se nombre curador a [NOMBRE Y APELLIDOS DEL CURADOR] para que complemente la capacidad del solicitante en [ACTO: por ejemplo, la venta de la vivienda sita en [DOMICILIO DEL INMUEBLE], de su propiedad].

OTROSÍ PRIMERO DIGO: que a efectos de comunicaciones designo el domicilio del letrado firmante de este escrito, sito en [DOMICILIO PROFESIONAL], así como su dirección de correo electrónico [CORREO ELECTRÓNICO] y su número de teléfono [TELÉFONO].

SUPLICO AL TRIBUNAL: que tenga por hecha la citada designación.

OTROSÍ SEGUNDO DIGO: que, para acreditar la certeza de los hechos relatados, solicito que sean oídos los familiares del solicitante [NOMBRE Y APELLIDOS], con domicilio en [DOMICILIO], y [NOMBRE Y APELLIDOS], con domicilio en [DOMICILIO], y asimismo ofrezco los siguientes testigos:

– [NOMBRE Y APELLIDOS DEL TESTIGO], con domicilio en [DOMICILIO].

[OPCIONAL — incluir si procede]
– [NOMBRE Y APELLIDOS DEL TESTIGO], con domicilio en [DOMICILIO].

SUPLICO AL TRIBUNAL: que tenga por propuestos a los testigos indicados, admitiendo la testifical ofrecida, comprometiéndose esta parte a que comparezcan en el día y hora que se señale [ELEGIR: / o, en su caso, solicitando que sean citados judicialmente para la práctica de la diligencia].

Es justicia que insto en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del solicitante y del letrado
