---
name: demanda-completar-adicionar-particion-herencia-civ-0409
description: "Demanda para completar o adicionar la partición de la herencia. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda para completar o adicionar la partición de la herencia

> Formulario **CIV-0409** del plugin **Herencias, testamentos y donaciones** (`formularios-herencias-y-donaciones`) · Civil › Sucesiones y donaciones · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda para completar o adicionar la partición de la herencia» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda para completar o adicionar la partición de la herencia” para mi caso». También puedes invocarla directamente con `/formularios-herencias-y-donaciones:demanda-completar-adicionar-particion-herencia-civ-0409`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-herencias-y-donaciones:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Herencias, testamentos y donaciones) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (18 veces)
- [ ] FECHA (7 veces)
- [ ] Nº DE DOCUMENTO (5 veces)
- [ ] IMPORTE (4 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] AÑO
- [ ] DESCRIPCIÓN DEL BIEN
- [ ] DÍA
- [ ] FINCA
- [ ] LUGAR
- [ ] MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] MES
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] NÚMERO
- [ ] SEDE
- [ ] VECINDAD CIVIL

## Normas que cita el formulario

- art. 1079 Código Civil
- art. 52.1.4.º LEC
- art. 85.1 LOPJ
- art. 249.2 LEC
- art. 251 LEC
- art. 5 Ley Orgánica 1/2025
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

D [NOMBRE Y APELLIDOS] Procurador de los Tribunales, actuando en representación de [NOMBRE DEL REPRESENTADO/A], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], al amparo de lo dispuesto en el artículo 1079 del Código Civil, formulo demanda de juicio ordinario en ejercicio de la acción de adición o complemento de la herencia en relación al inmueble [DESCRIPCIÓN DEL BIEN], titularidad del causante D [NOMBRE Y APELLIDOS], la cual dirijo contra el coheredero D [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD] en base a los siguientes

HECHOS

Se ejercita en la presente demanda la acción de adición del inmueble sito en [LOCALIDAD], a la herencia del causante D [NOMBRE Y APELLIDOS], el cual fue omitido pese a ser de su titularidad, y su existencia en el haber hereditario era totalmente desconocida por mi representado al momento de realizarse la partición, tal como se expondrá en esta demanda.

Mi mandante es hijo del causante D [NOMBRE Y APELLIDOS], de vecindad civil [VECINDAD CIVIL], fallecido el día [FECHA], y de Dª [NOMBRE Y APELLIDOS], fallecida anteriormente en fecha [FECHA], según resulta de las certificaciones de nacimiento, matrimonio y defunción que se adjuntan como documentos n.º [NÚMERO] El matrimonio tuvo otro hijo, D [NOMBRE Y APELLIDOS], hermano de mi representado y ahora demandado.

En fecha [FECHA], el causante D [NOMBRE Y APELLIDOS] otorgó testamento instituyendo herederos universales a mi mandante y a su hermano (acompaño como documento número [Nº DE DOCUMENTO] copia auténtica del citado testamento).

En fecha [FECHA], por los herederos se otorgó escritura de aceptación, división y adjudicación de la herencia del causante D [NOMBRE Y APELLIDOS] ante el Notario D [NOMBRE Y APELLIDOS]

En la citada escritura se recogen el inventario de los bienes de la herencia que eran los siguientes:

Dichos bienes fueron adjudicados a los herederos con la siguiente distribución:

Acompaño como documento número [Nº DE DOCUMENTO] copia auténtica de la escritura de adjudicación de herencia otorgada en fecha [FECHA]

Tal como se ha expresado anteriormente, en la herencia no se incluyó un inmueble titularidad del causante, el cual era totalmente desconocido para mi representado al momento de realizarse la partición, cuya descripción es la siguiente:

Dicho inmueble fue adquirido por el causante a D [NOMBRE Y APELLIDOS], por contrato privado de compraventa de fecha [FECHA], redactado con la intervención de dos testigos, D [NOMBRE Y APELLIDOS] y D [NOMBRE Y APELLIDOS], y el mismo era totalmente desconocido para mi representado hasta que recientemente tuvo conocimiento de dicha adquisición, al encontrar el referido contrato entre los papeles del difunto, realizando diferentes averiguaciones que le dan la certeza de que dicha finca pertenecía al causante como se expondrá seguidamente (acompaño como documento [Nº DE DOCUMENTO] el referido contrato privado de compraventa).

Tras venir en conocimiento del contrato de compraventa de la citada finca, mi representado realizó diferentes averiguaciones con el vendedor y los testigos, teniendo conocimiento que la compraventa se efectuó efectivamente por precio de [IMPORTE] euros y que el causante D [NOMBRE Y APELLIDOS] había arrendado la finca en cuestión a D [NOMBRE Y APELLIDOS] en fecha [FECHA], percibiendo una renta mensual de [IMPORTE] euros, que el arrendatario satisfizo al causante hasta su fallecimiento, y que posteriormente ha seguido pagando al ahora demandado D [NOMBRE Y APELLIDOS], hermano de mi representado, pero que no es titular de la finca en cuestión, habiendo ocultado a mi representado cualquier mención sobre esta finca y su pertenencia al causante.

De hecho, mi representado sólo ha podido conocer la existencia de esta finca en el patrimonio del causante con ocasión de haber ocupado recientemente la casa familiar que le correspondió en la partición realizada, habiendo encontrado entonces el contrato aportado y tomado conocimiento de la titularidad del inmueble.

Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento nº [Nº DE DOCUMENTO]

Atendido lo anterior, y ante la negativa del demandado a una solución amistosa del asunto, mi mandante se ve en la obligación de ejercitar la presente acción de adición o complemento de la partición de la herencia a fin de que se adicione la finca antes descrita a la herencia del causante D [NOMBRE Y APELLIDOS], de conformidad a lo que dispone el artículo 1079 del Código Civil, debiendo realizarse la correspondiente partición del inmueble omitido.

FUNDAMENTOS DE DERECHO

Competencia

Corresponde a los Tribunales de Instancia de [LOCALIDAD] al ser del lugar del último domicilio del finado con fundamento en el artículo 52.1.4.º LEC, en relación con lo dispuesto en el art. 85.1º LOPJ.

Legitimación

Le corresponde a esta parte en su condición de heredero del causante y miembro de la comunidad hereditaria, correspondiendo la legitimación pasiva al demandado.

Procedimiento

Es el juicio ordinario con fundamento en el artículo 249.2 de la LEC dado el valor del inmueble asciende a [IMPORTE] euros, calculado conforme a lo dispuesto en los apartados 2 y 3 del artículo 251 de la LEC.

Cumplimiento de los requisitos de procedibilidad.

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

Acción de adición o complemento de la partición

Es de aplicación el artículo 1079 del Código Civil que establece: "La omisión de alguno o algunos objetos o valores de la herencia no da lugar a que se rescinda la partición por lesión, sino a que se complete o adicione con los objetos o valores omitidos".

Este precepto lo que contempla es la acción de adición o complemento de la partición, que es una acción distinta a la de rescisión de la partición; en este sentido se ha pronunciado el Tribunal Supremo en Sentencia de 12 de diciembre de 2005, en la que razona "que las atribuciones mal valoradas deben resolverse por la vía de la rescisión y las omisiones de bienes o valores por el camino de la adición o complemento de la partición". Y en este mismo sentido la Sentencia de fecha 12 de junio de 2008, Rec. 520/2001, razona que " la omisión de alguno o algunos objetos o valores de la herencia no da lugar a que se rescinda la partición por lesión, sino a que se complete o adicione con los objetos o valores omitidos".

En materia de costas el artículo 394 LEC señala que las de primera instancia se imponen a la parte que vea rechazadas sus pretensiones.

En base a lo anterior,

SUPLICO al Tribunal que tenga por presentada la presente demanda, con los documentos a ella adjuntos y con sus copias, por parte en la representación que ostento y tras la pertinente tramitación se dicte por ese Tribunal sentencia en la que se acuerde la adición o complemento de la partición efectuada de la herencia de su padre D [NOMBRE Y APELLIDOS], con la inclusión de la finca [FINCA], en término municipal de [LOCALIDAD], condenando al demandado a estar y pasar por dicha declaración, e imponiendo al referido demandado el pago de las costas ocasionadas en este proceso.

OTROSÍ DIGO.-Se fija la cuantía del presente procedimiento en [IMPORTE] euros, de conformidad a lo dispuesto en el artículo 251 y 252 de la Ley de Enjuiciamiento Civil.

En base a lo anterior,

SUPLICO AL TRIBUNAL se tenga por efectuada la anterior manifestación a los efectos pertinentes.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma Abogado	Firma Procurador

========================================================================
