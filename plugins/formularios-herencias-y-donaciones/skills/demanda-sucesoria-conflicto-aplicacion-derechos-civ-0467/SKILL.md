---
name: demanda-sucesoria-conflicto-aplicacion-derechos-civ-0467
description: "Demanda sucesoria con conflicto de aplicación de derechos civiles forales o especiales. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda sucesoria con conflicto de aplicación de derechos civiles forales o especiales

> Formulario **CIV-0467** del plugin **Herencias, testamentos y donaciones** (`formularios-herencias-y-donaciones`) · Civil › Sucesiones y donaciones · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda sucesoria con conflicto de aplicación de derechos civiles forales o especiales» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda sucesoria con conflicto de aplicación de derechos civiles forales o especiales” para mi caso». También puedes invocarla directamente con `/formularios-herencias-y-donaciones:demanda-sucesoria-conflicto-aplicacion-derechos-civ-0467`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-herencias-y-donaciones:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Herencias, testamentos y donaciones) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (14 veces)
- [ ] NOMBRE Y APELLIDOS (10 veces)
- [ ] Nº DE DOCUMENTO (5 veces)
- [ ] AÑO (4 veces)
- [ ] TERRITORIO FORAL (4 veces)
- [ ] VECINDAD CIVIL (4 veces)
- [ ] FECHA (3 veces)
- [ ] Nº DE ARTÍCULO (2 veces)
- [ ] DÍA
- [ ] IMPORTE
- [ ] IMPORTE O CUOTA DE LEGÍTIMA
- [ ] LUGAR
- [ ] MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] MES
- [ ] SEDE

## Normas que cita el formulario

- art. 12.4 Código Civil
- art. 16.1.2 Código Civil
- art. 52.1.4 LEC
- art. 249.2 LEC
- art. 5 Ley Orgánica 1/2025
- art. 14 Código Civil
- art. 9.8 Código Civil
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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE Q.P.T.R.C.»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE Q.P.T.R.C.

D./Dña. [NOMBRE Y APELLIDOS] Procurador/a de los Tribunales, actuando en representación de D./Dña. [NOMBRE Y APELLIDOS], según se acredita por certificación del registro electrónico de apoderamientos judiciales que acompaño (o mediante designación apud acta ante el/la Letrado/a de la Administración de Justicia de [SEDE]), bajo la dirección letrada de D/Dª [NOMBRE Y APELLIDOS], Abogado/a del Iltre. Colegio de [LOCALIDAD], ante el Tribunal comparezco y como mejor en derecho proceda formulo demanda de juicio ordinario en ejercicio de acción de reclamación de los derechos legitimarios que corresponden a mi mandante D. [NOMBRE Y APELLIDOS] en la herencia de su padre D. [NOMBRE Y APELLIDOS], dirigiendo esta acción contra los herederos D. y D. [NOMBRE Y APELLIDOS], respectivamente, con domicilios sitos en [LOCALIDAD] y en [LOCALIDAD], en base a los siguientes hechos y fundamentos de derecho:

PRIMERO.- HECHOS

El pasado día [FECHA] falleció en la localidad de [LOCALIDAD] D. [NOMBRE Y APELLIDOS], padre de mi representado, quien había residido en el domicilio sito en [LOCALIDAD], de la localidad de [LOCALIDAD], ostentando la vecindad civil de [VECINDAD CIVIL] (acompaño como documentos números [Nº DE DOCUMENTO] certificado de defunción, títulos de propiedad de la vivienda donde residía el padre [NOMBRE Y APELLIDOS], facturas de electricidad, gas y agua correspondientes a los años [AÑO] a [AÑO]).

El finado [NOMBRE Y APELLIDOS], pese a haber residido de forma continuada en dicha vivienda, cuatro años antes de su fallecimiento, y con la finalidad que se expresará posteriormente, se había empadronado en la localidad de [LOCALIDAD], perteneciente al territorio foral de [TERRITORIO FORAL], habiendo manifestado ante el Encargado del Registro Civil de [LOCALIDAD] su voluntad de adquirir la vecindad civil foral de [VECINDAD CIVIL] (acompaño como documento número [Nº DE DOCUMENTO] certificación literal de nacimiento del finado D. [NOMBRE Y APELLIDOS]).

SEGUNDO.- La finalidad de realizar tal cambio de vecindad civil trae causa de las discrepancias con mi mandante, hijo del causante, quienes tenían una mala relación personal desde mucho tiempo atrás, si bien en modo alguno podía constituir causa de desheredación, lo cual llevó a su padre a trasladar ficticiamente su residencia al territorio foral de [TERRITORIO FORAL] con la finalidad de eludir las normas sobre la legítima del territorio de su residencia, de tal manera que pudo instituir como únicos herederos a sus demás descendientes amparado por la norma foral de regulación de la herencia, cometiendo de esta manera fraude a la ley en la adquisición de la vecindad civil.

La conducta fraudulenta se pone de manifiesto por las siguientes circunstancias:

1) El fallecido D. siempre ha residido en la localidad de [LOCALIDAD] como se acredita por los documentos aportados y se probará oportunamente en este proceso.

2) El empadronamiento realizado en el municipio de [LOCALIDAD], perteneciente al territorio foral de [TERRITORIO FORAL], tenía como único objeto adquirir la vecindad foral y poder testar a favor de los otros descendientes como se acredita por el hecho que el día después en que adquirió la vecindad de [VECINDAD CIVIL] por manifestación ante el Encargado del Registro Civil de [LOCALIDAD], otorgó el testamento donde se instituía como únicos herederos a los demandados (acompaño como documentos número [Nº DE DOCUMENTO] certificado del Registro de Últimas Voluntades y copia simple del testamento de fecha [FECHA] otorgado ante el Notario de [LOCALIDAD]).

3) Como se acreditará oportunamente, el fallecido D. nunca residió en la localidad de [LOCALIDAD], puesto que únicamente poseía un inmueble, precisamente donde se empadronó, el cual estaba alquilado desde el año [AÑO] (acompaño en este momento a efectos acreditativos como documentos [Nº DE DOCUMENTO] nota registral del citado inmueble y contrato de arrendamiento entre el fallecido y el arrendatario D. de fecha [FECHA]).

TERCERO.- El cambio de vecindad civil realizado por el causante de los demandados es un acto en fraude de ley, sancionado en el artículo 12.4 del Código Civil, puesto que con él se eluden las normas imperativas de aplicación del derecho interregional.

El artículo 16.1.2ª Código Civil, al establecer las normas sobre conflictos de leyes, se remite a lo dispuesto en el capítulo IV del Título preliminar, con la excepción de la aplicación de lo dispuesto en los apartados 1, 2 y 3 del Art. 12 del Código Civil sobre calificación, remisión y orden público". La consecuencia es clara: se aplica el artículo 12.4 del Código Civil en el derecho interregional, que establece que "se considerará como fraude de ley la utilización de una norma de conflicto con el fin de eludir una ley imperativa española".

La Sentencia del Tribunal Supremo de 5 abril 1994, en un caso muy similar, declaró efectuada en fraude de ley la adquisición de la vecindad foral por unos cónyuges que habían residido más de dos años en una villa sometida a este Derecho, otorgando dos días después sendos testamentos que declararon sometidos al Derecho foral, en los que nombraron herederos a sus nietos y separaron de la herencia expresamente a sus dos hijos, siendo que en este caso el "modus operandi" es el mismo, con el añadido de que la residencia del fallecido en la localidad era ficticia, de tal manera que en ningún caso pudo adquirir la vecindad civil foral.

CUARTO.- La existencia de fraude de ley conforme al artículo 12.4 del Código Civil no impide la aplicación de la norma que se ha tratado de eludir, tal como establece el artículo 6.4 del mismo Código, de tal manera que mi representado tiene el derecho a la legítima que le reconoce el artículo [Nº DE ARTÍCULO], norma eludida con la aplicación fraudulenta de la norma foral a la que se ha hecho referencia, de tal manera que deberá reconocerse el derecho de mi mandante a la legítima reclamada.

QUINTO.- Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento nº [Nº DE DOCUMENTO]

A los presentes Hechos les son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

Competencia

Corresponde a los Tribunales de [LOCALIDAD] al ser el lugar en el que el finado tuvo su último domicilio (artículo 52.1.4ª LEC).

Legitimación

Le corresponde activamente a esta parte en su condición de legitimario, y en la parte pasiva a los herederos del causante.

Procedimiento

Es el juicio ordinario con fundamento en el art. 249.2 LEC dado el importe de la legítima excede en todo caso de 15.000 € a partir de los que se deben seguir las reclamaciones por las normas del juicio ordinario.

Cumplimiento de los requisitos de procedibilidad

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

Fondo de la reclamación

El artículo 12.4 del Código Civil establece que "se considerará como fraude de ley la utilización de una norma de conflicto con el fin de eludir la aplicación de una norma imperativa española". El causante adquirió fraudulentamente la vecindad civil foral de [VECINDAD CIVIL], sin darse los requisitos del art. 14 del Código Civil, con la finalidad de aplicar el derecho foral de [TERRITORIO FORAL] a la sucesión, al amparo del artículo 9.8 del Código Civil, defraudando los derechos legitimarios de mi representado.

Fondo de la reclamación

El artículo 6.4 y 12.4 del Código Civil determinan la aplicación de los preceptos que se han eludido, artículos [Nº DE ARTÍCULO], y la consiguiente inaplicación de los preceptos de derecho foral sobre sucesiones.

Costas

En materia de costas el art. 394 LEC señala que las de primera instancia se imponen a la parte que vea en primera instancia rechazadas sus pretensiones

En base a lo anterior,

SUPLICO AL TRIBUNAL: tenga por presentada la presente demanda con los documentos a ella adjuntos y por parte en la representación que ostento y tras la pertinente tramitación se dicte por ese Tribunal sentencia por la que se declare el derecho de mi representado a la legítima que le corresponde [IMPORTE O CUOTA DE LEGÍTIMA], debiendo los demandados satisfacerla con cargo a la herencia, todo ello con imposición de costas a la parte demandada.

OTROSÍ PRIMERO DIGO.- Se fija la cuantía del presente procedimiento en [IMPORTE] euros.

En base a lo anterior

SUPLICO AL TRIBUNAL se tenga por efectuada la anterior manifestación a los efectos pertinentes.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma Procurador y Abogado

========================================================================
