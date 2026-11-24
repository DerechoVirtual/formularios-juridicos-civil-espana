---
name: recurso-casacion-interes-casacional-generico-civ-1367
description: "Recurso de casación por interés casacional genérico. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Recurso de casación por interés casacional genérico

> Formulario **CIV-1367** del plugin **Recursos civiles: reposición, apelación, casación y queja** (`formularios-recursos-civiles`) · Civil › Recursos · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **recursos**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Recurso de casación por interés casacional genérico» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Recurso de casación por interés casacional genérico” para mi caso». También puedes invocarla directamente con `/formularios-recursos-civiles:recurso-casacion-interes-casacional-generico-civ-1367`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-recursos-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Recursos civiles: reposición, apelación, casación y queja) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (10 veces)
- [ ] Nº DE PROCEDIMIENTO (4 veces)
- [ ] AÑO (2 veces)
- [ ] DESCRIBIR (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] MES (2 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] DÍA
- [ ] FALLO DE LA SENTENCIA
- [ ] FUNDAMENTOS
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] NOMBRE Y APELLIDOS
- [ ] NORMA INFRINGIDA
- [ ] Nº
- [ ] Nº DE ARTÍCULO
- [ ] NÚMERO
- [ ] NÚMERO DE CARACTERES
- [ ] PETICIÓN
- [ ] SECCIÓN

## Normas que cita el formulario

- art. 477 LEC
- art. 480 LEC
- art. 448.2 LEC
- art. 481.6 LEC
- art. 477.3 LEC
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

### Avisos de actualización (2) — se aplican en el texto, nunca se copian en el documento

- Junto a «…CIA PROVINCIAL DE [LOCALIDAD] PARA ANTE LA SALA DE LO CIVIL DEL TRIBUNAL SUPREMO»: Errata. La Audiencia Provincial no cambia de denominación. Fuente: LOPJ arts. 80 y 82 (Audiencia Provincial, sin cambio de denominación).
- Al principio del formulario: Errata. Fuente: LOPJ arts. 80 y 82 (Audiencia Provincial, sin cambio de denominación).

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

Rollo n.º [Nº DE PROCEDIMIENTO]/[AÑO]

A LA SECCIÓN [SECCIÓN] DE LA ILMA. AUDIENCIA PROVINCIAL DE [LOCALIDAD] PARA ANTE LA SALA DE LO CIVIL DEL TRIBUNAL SUPREMO

D. [NOMBRE Y APELLIDOS] Procurador de los Tribunales, actuando en representación de [NOMBRE DEL REPRESENTADO/A] según viene acreditado en los presentes autos, comparezco y como mejor proceda en derecho DIGO:

1) Que en fecha [FECHA] esta parte ha sido notificada de la sentencia de fecha [FECHA] dictada en el Rollo arriba expresado, por la que [FALLO DE LA SENTENCIA]. Frente a dicha sentencia se dedujo solicitud de complemento siendo desestimada por auto de fecha [FECHA], notificado en fecha [FECHA].
2) Que entendiendo que dicha sentencia no es ajustada a derecho, dicho sea con los debidos respetos y en términos de defensa, por medio del presente escrito, al amparo de lo dispuesto en el art. 477 de la LEC, interpongo contra la misma RECURSO DE CASACIÓN por interés casacional, en la modalidad del apartado [Nº] consistente en [DESCRIBIR], en base a los siguientes presupuestos de admisibilidad y motivos:

I. Admisibilidad del recurso

Primero.– El presente recurso se deduce contra la sentencia dictada por la Audiencia Provincial en fecha [FECHA], que produce un evidente gravamen a esta parte al desestimar sus pretensiones, impugnando todos sus pronunciamientos.

Segundo.– El supuesto que habilita la presentación es que la resolución del recurso presenta interés casacional por oposición a la jurisprudencia del Tribunal Supremo, como se fundamentará ampliamente, al amparo de lo dispuesto en el apartado 3 del artículo 477 de la LEC,

Tercero.– El presente recurso se interpone dentro del plazo de veinte días establecido en el artículo 480 de la LEC, computados conforme al artículo 448.2 de la LEC.

Cuarto.– El recurso presenta interés casacional puesto que la sentencia impugnada se opone a la doctrina jurisprudencial del Tribunal Supremo (o se pronuncia sobre una cuestión en la que existe jurisprudencia contradictoria de las Audiencias Provinciales), infrigiendo los arts. de la Ley [NORMA INFRINGIDA], y la doctrina jurisprudencial en interpretación de dichos preceptos recogida en la S.T.S. de [FECHA], de [FECHA] y de 16 de [MES] según se fundamentará seguidamente.

Quinto.– De conformidad a lo dispuesto en el artículo 481.6 de la LEC, así como en cumplimiento del Acuerdo de la Sala de Gobierno del Tribunal Supremo de fecha 8 de septiembre, se incorpora carátula del recurso y se acompaña poder para pleitos, certificación de la sentencia y texto de las que se aducen como fundamento del interés casacional, y resguardo de constitución del depósito para recurrir (documentos número [Nº DE DOCUMENTO] a [Nº DE DOCUMENTO])

II. Motivos del recurso

I.– Encabezamiento: El primer motivo se interpone al amparo de lo dispuesto en el art. 477.3 de la LEC, por infracción del artículo [Nº DE ARTÍCULO] del Código Civil, al oponerse a la doctrina jurisprudencial establecida por la Excma. Sala recogida, entre otras, en las SSTS núm [NÚMERO], de fecha [FECHA], dictada en Recurso [Nº DE PROCEDIMIENTO] y núm [Nº DE PROCEDIMIENTO], de fecha [FECHA], dictada en el Recurso núm [Nº DE PROCEDIMIENTO], resultando infringido el citado precepto por cuanto que

II.– Desarrollo del motivo: El motivo se funda en [FUNDAMENTOS]

Esta cuestión fue discutida en la instancia y afecta a la ratio decidendi de la sentencia recurrida presentando interés casacional por cuanto que

La sentencia recurrida prescinde totalmente de la interpretación uniforme de la Sala Primera sobre el precepto infringido, estableciendo unas conclusiones jurídicas totalmente incompatibles con la doctrina jurisprudencial de la Sala Primera, tal como ha quedado expuesto.

Sobre esta base, solicitamos que se reitere la doctrina jurisprudencial sobre [DESCRIBIR]

Es por ello que se pretende, con estimación del recurso de casación, que se case la sentencia impugnada, revocando las sentencias de primera y segunda instancia, con desestimación de la demanda, e imposición de costas a las actoras del proceso de instancia, en aplicación de lo dispuesto en el art. 394 de la LEC.

Procede por ello casar la resolución impugnada, y en aplicación de la interpretación expuesta, resolver sobre el caso, acordando que

En base a lo anterior,

SUPLICO A LA SALA: Que tenga por presentado este escrito con la certificación del traslado previo a las demás partes teniendo por interpuesto el recurso de casación por interés casacional frente a la sentencia dictada por la Sección de la Audiencia Provincial de [LOCALIDAD] en las presentes actuaciones de fecha [FECHA] y tras la pertinente tramitación y remisión de las actuaciones al Tribunal Supremo, se dicte por éste esta sentencia en la que declarando haber lugar al recurso de casación, casando la sentencia impugnada, y se realicen los siguientes pronunciamientos:

1) Se reitere la doctrina jurisprudencial sobre la interpretación del art. del Código Civil, declarando que [PETICIÓN].
2) Se casen las sentencias dictadas en primera y segunda instancia, y se acuerdo la desestimación de la demanda, con imposición de costas a la parte actora en primera instancia

[OPCIONAL — incluir si procede]

OTROSÍ PRIMERO DIGO que, de conformidad con lo dispuesto en los apartados 3.d) y 6 de la disposición adicional decimoquinta de la LOPJ acompaño a este escrito resguardo de consignación en la cuenta de Depósitos y Consignaciones abierta a nombre del Tribunal del depósito exigido para interponer el recurso por importe de 50 euros.

Por lo que, SUPLICO A LA SALA que tenga por constituido el depósito, dejando interesada desde este momento su devolución para el caso de estimación total o parcial del recurso.

De conformidad con lo dispuesto en el Acuerdo de la Sala de Gobierno del TS de 8 de septiembre de 2023, el Abogado firmante CERTIFICA que el presente escrito tiene [NÚMERO DE CARACTERES]. caracteres con espacio.

a [DÍA] de [MES] de [AÑO]

Abogado/a	Procurador/a

Firmado: D./Dña: Firmado: D./Dña:

========================================================================
