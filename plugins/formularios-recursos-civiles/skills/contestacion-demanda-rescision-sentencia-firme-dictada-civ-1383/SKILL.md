---
name: contestacion-demanda-rescision-sentencia-firme-dictada-civ-1383
description: "Contestación a la demanda de rescisión de sentencia firme dictada en rebeldía. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contestación a la demanda de rescisión de sentencia firme dictada en rebeldía

> Formulario **CIV-1383** del plugin **Recursos civiles: reposición, apelación, casación y queja** (`formularios-recursos-civiles`) · Civil › Recursos · normativa revisada el 24-11-2026.

## Qué es

Modelo de escrito de contestación a la demanda de rescisión de sentencia firme dictada en rebeldía, oponiéndose a la misma.

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contestación a la demanda de rescisión de sentencia firme dictada en rebeldía» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contestación a la demanda de rescisión de sentencia firme dictada en rebeldía” para mi caso». También puedes invocarla directamente con `/formularios-recursos-civiles:contestacion-demanda-rescision-sentencia-firme-dictada-civ-1383`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-recursos-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Recursos civiles: reposición, apelación, casación y queja) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (17 veces)
- [ ] LOCALIDAD (7 veces)
- [ ] NÚMERO (4 veces)
- [ ] FECHA (3 veces)
- [ ] AÑO (2 veces)
- [ ] DÍA (2 veces)
- [ ] MES (2 veces)
- [ ] Nº (2 veces)
- [ ] Nº DE PROCEDIMIENTO (2 veces)
- [ ] ACCIDENTE O ENFERMEDAD
- [ ] DOMICILIO
- [ ] LUGAR
- [ ] Nº DE DOCUMENTO
- [ ] SEDE

## Normas que cita el formulario

- art. 265.2 LEC
- art. 23.1 LEC
- art. 31.1 LEC
- art. 501.3 LEC
- art. 773 LEC
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

D./Doña [NOMBRE Y APELLIDOS], Procurador de los Tribunales, que actúa en nombre y representación de Don/Dª, según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], dirigida por el Letrado en ejercicio abajo firmante D./Doña [NOMBRE Y APELLIDOS], con despacho profesional en [LOCALIDAD], ante el Tribunal comparezco en los autos de Juicio Ordinario nº [Nº DE PROCEDIMIENTO]/01, y como mejor proceda en Derecho, DIGO:

Que mediante el presente escrito y dentro del término conferido, paso a contestar la demanda de Juicio Ordinario sobre rescisión de sentencia firme formulada por D/Doña [NOMBRE Y APELLIDOS], oponiéndome a la misma en base a los siguientes:

HECHOS

PRIMERO

Nada que objetar al correlativo de la demanda

SEGUNDO

De conformidad con la existencia y tenor de la sentencia firme en proceso que inició esta parte, si bien el que el difunto D/Doña [NOMBRE Y APELLIDOS] fuera ignorante de la misma es un alegación que no se comparte, ya que en el anterior proceso por deslinde, fueron por mi mandante codemandados D/Doña [NOMBRE Y APELLIDOS] y D/Doña [NOMBRE Y APELLIDOS], hermano del causante del hoy actor, consocio que explotaba el mismo negocio, el que compareció como testigo en el proceso cuya sentencia se pide rescindir, por lo que puede racionalmente presumirse que el condenado rebelde tuvo conocimiento extraprocesal de la existencia del litigio, pues cuesta creerse que no se lo comunicara su hermano.

TERCERO

De acuerdo con los particulares del Juicio Ordinario en que se produjo la rebeldía del padre del actor, y que se desgranan en el correlativo, salvo que la opción por la citación edictal no tuvo nada de cómodo o antijurídico, ya que se desconocía la fórmula de localizar al demandado, y su domicilio era el que se consignó en la demanda, y donde tuvo lugar el emplazamiento, resultando irrelevantes las manifestaciones del portero de la finca, que no proporcionó un paradero.

A la demostración de que recurrió a solicitar edictos por ausencia de domicilio distinto del facilitado, se acompaña testimonio de la demanda de Juicio Verbal de deslinde nº [NÚMERO] /, que se siguió también en este Tribunal, en que mi representada codemandó a D/Doña [NOMBRE Y APELLIDOS] y su hermano, en el mismo domicilio, y el emplazamiento practicado, en fecha [FECHA], como documento nº1.

CUARTO

Se niega rotundamente lo aseverado en el correlativo ordinal de la demanda.

El causante del actor no estuvo realmente domiciliado en [DOMICILIO], siendo inauténtico el dato que se extrae del certificado de empadronamiento presentado de contrario.

De la certificación de la Compañía Telefónica enarbolada en la demanda se deduce que D [NOMBRE Y APELLIDOS] era titular de dicha línea telefónica desde el [DÍA] de [MES] de [AÑO], casi [Nº] años antes de que sufriese el [ACCIDENTE O ENFERMEDAD], que según el hijo, habría provocado su traslado a

Por otro lado, el D/Doña [NOMBRE Y APELLIDOS] compareció ante la Notaria de [LOCALIDAD] D/Doña [NOMBRE Y APELLIDOS] para otorgar poder general en favor de su hijo. Pues bien, en dicho acto -cuya celebración demuestra que la permanencia de D/Doña [NOMBRE Y APELLIDOS] en [LOCALIDAD] no era constante- el poderdante señaló como su domicilio el que se puso en la demanda de Juicio Ordinario nº [NÚMERO] /01, no el de [LOCALIDAD] (fotocopia como documento nº 2, protestando de hallarse original en el protocolo de la Notaria indicada, a los efectos del art. 265.2 LEC).

QUINTO

Disconformes con el correlativo, porque precisamente se emplazó por edictos a D/Doña [NOMBRE Y APELLIDOS], puesto que se trataba de una persona ausente del único domicilio conocido e incierto, una vez no hallado, por lo que lo cual la situación de rebeldía fue asumida por el interesado.

FUNDAMENTOS DE DERECHO

I, II

Conforme esta parte con la competencia y el tipo de procedimiento señalados por el actor en el correlativo de la demanda.

III y IV

De conformidad con los expuestos de contrario, acerca de la capacidad de las partes y su legitimación, siempre que se entienda que las legitimaciones, activa y pasiva son presupuestos procesales subjetivos, y que como comuneros los demandantes y mi representada, están de cara a la acción de división de cosa común, ambos mutuamente legitimados como requisito previo al fondo de la misma, y sólo detenta la activa quien pretende porque ha tomado la iniciativa, y la pasiva frente a quien se pretende.

V.- POSTULACIÓN Y DEFENSA

La demandada está representada por Procurador legalmente habilitado en el partido, según exige el art. 23.1 LEC, y defendida por el Letrado que consta en el encabezamiento (art. 31.1 LEC).

VI.- CUANTÍA

Si bien el demandado sólo puede impugnar la cuantía de la demanda si la correcta determinación, respecto de la verificada por el demandante, dimanaría una inadecuación de procedimiento, o alterara la posibilidad de recurso de casación, esta parte tiene que manifestar, a los efectos de que no tenga por consentido el interés litigioso en una eventual liquidación de costas, que no hay razón para entender que la cuantía de la demanda de rescisión es la de la del juicio cuya sentencia firme se ataca, ya que el objeto de este proceso, que es mero-procesal en el juicio rescindente, no supone pura declaración ni condena, sino que consiste en conseguir una constitución extintiva de la sentencia, y así dar paso al juicio rescisorio, por lo que se considera que la cuantía es inestimable, sin poderse determinar siquiera en términos relativos.

VII.- FONDO DEL ASUNTO

Se ejercita por el actor la causa de rescisión del art. 501.3º LEC, y para su estimación la doctrina jurisprudencial, además de los requisitos objetivos que marca el precepto, como antes se interpretó el art. 773 LECiv 1881, que concurra la exigencia subjetiva de no serle imputable al demandado la incomparecencia en juicio [STS de 3 de diciembre de 1985 (LA LEY10558-JF/0000) y STS 13 de abril de 1998], por el contrario del objetivismo que aduce la fundamentación jurídica de la demanda.

En punto a los presupuestos objetivos, el recurrente no ha presentado ninguna otra prueba documental, que un certificado de empadronamiento, que puede sencillamente conseguirse por el expediente de haberse inscrito el interesado en las oficinas municipales, causando baja en donde realmente se residía. Niguna otra prueba se anuncia del hecho, como es el de residir durante [Nº] años en un determinado lugar, que necesariamente ha de dejar abundantes rastros y vestigios. Por el contrario, se prueba documentalmente que fue emplazado en el Juicio Verbal nº [NÚMERO] /00 en el domicilio donde se intentó en el Juicio Ordinario nº [NÚMERO] /01, que el número de teléfono en [LOCALIDAD] ya entonces lo tenía contratado con la Compañía Telefónica, y que el [DÍA] de [MES] de [AÑO] compareció en la Notaría de [LOCALIDAD], manifestando ser su domicilio el antedicho.

En cuanto a los subjetivos, el hermano de D/Doña [NOMBRE Y APELLIDOS] era conocedor del pleito, puesto que prestó declaración como testigo, y debe presumirse, por el parentesco y los negocios en común, que enteró al hermando, por lo que si no comunicó al Tribunal que se hallaba imposibilitado por razón de enfermedad, y temporalmente en [LOCALIDAD], propiamente se colocó en situación de no defenderse, es decir, de indefensión pretextativa, y el derecho a la tutela judicial efectiva debe interpretarse de forma que se garanticen las leyes procesales sobre la rebeldía (STC 310/1993, de 25 de octubre). Por otra parte, si D/Doña [NOMBRE Y APELLIDOS] se hallaba definitivamente incapacitado, su hijo que ahora agita, debió promover su incapacitación y tutelarle compareciendo en juicio (STS de 22 de septiembre de 1997, rec. 2637/1993).

De cuanto antecede, se argumenta que el actor no probará que el demandado que es su causante se hallase en la situación definida por la concurrencia de los requisitos establecidos en el art. 501.3º LEC, por lo que la demanda de rescisión por el rebelde, entendida en sentido estricto, como lo hacía la jurisprudencia tradicional, no puede prosperar.

VIII.- COSTAS

Las costas deberán serle impuestas, de conformidad con el art. 394.1 LEC, a la parte actora, al proceder la desestimación de la demanda.

Por lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito con los documentos y copias que le acompañan, admita uno y otras, se me tenga por personado y parte en la representación que ostento, entendiéndose conmigo las sucesivas ulteriores diligencias, y teniendo por contestada en tiempo y forma la demanda instada por D/Doña [NOMBRE Y APELLIDOS], como sucesor de D/Doña [NOMBRE Y APELLIDOS], previos los trámites que corresponden, se dicte en su día sentencia por la que se desestime íntegramente la demanda presentada, declarando no haber lugar a rescindir la sentencia firme de [FECHA] recaída en autos de Juicio Ordinario nº [Nº DE PROCEDIMIENTO] /01, ni a oir en ellos a D/Doña [NOMBRE Y APELLIDOS], condenando a la parte actora en las costas procesales.

Por ser de Justicia que pido en [LUGAR], a [FECHA].

Firma de Abogado/a	Firma de Procurador/a

========================================================================
