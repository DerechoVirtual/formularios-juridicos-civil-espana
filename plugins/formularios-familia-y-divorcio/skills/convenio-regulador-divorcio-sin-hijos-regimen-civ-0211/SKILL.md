---
name: convenio-regulador-divorcio-sin-hijos-regimen-civ-0211
description: "Convenio regulador de divorcio sin hijos con régimen de separación de bienes. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Convenio regulador de divorcio sin hijos con régimen de separación de bienes

> Formulario **CIV-0211** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Convenio regulador de un divorcio de mutuo acuerdo entre cónyuges sin hijos, casados en régimen de separación de bienes, que incluye el compromiso de extinguir el condominio sobre los bienes que tengan en común. Se acompaña a la solicitud o demanda de divorcio de mutuo acuerdo y se somete a ratificación ante la autoridad judicial (formulario adaptado a la reforma de la LO 1/2025).

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Convenio regulador de divorcio sin hijos con régimen de separación de bienes» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Convenio regulador de divorcio sin hijos con régimen de separación de bienes” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:convenio-regulador-divorcio-sin-hijos-regimen-civ-0211`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (8 veces)
- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] AÑO (4 veces)
- [ ] DÍA (4 veces)
- [ ] MES (4 veces)
- [ ] DOMICILIO (3 veces)
- [ ] DNI/NIE (2 veces)
- [ ] NOMBRE DEL NOTARIO (2 veces)
- [ ] Nº DE PROTOCOLO (2 veces)
- [ ] DOMICILIO CONYUGAL
- [ ] EL OTRO CÓNYUGE: NOMBRE Y APELLIDOS
- [ ] LA ESPOSA / EL ESPOSO: NOMBRE Y APELLIDOS
- [ ] MARCA
- [ ] MATRÍCULA
- [ ] MODELO
- [ ] PÁGINA
- [ ] TOMO

## Normas que cita el formulario

- art. 90 Código Civil

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

### Avisos de actualización (0) — se aplican en el texto, nunca se copian en el documento

- Ninguno.

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

CONVENIO REGULADOR DE DIVORCIO SIN HIJOS Y RÉGIMEN ECONÓMICO DE SEPARACIÓN ABSOLUTA DE BIENES

En la ciudad de [LOCALIDAD], a [DÍA] de [MES] de [AÑO]

REUNIDOS

DE UNA PARTE: D. [NOMBRE Y APELLIDOS], mayor de edad, vecino de [LOCALIDAD], con domicilio en [DOMICILIO] y D.N.I. núm. [DNI/NIE].

Y DE OTRA: Dª [NOMBRE Y APELLIDOS], mayor de edad, vecina de [LOCALIDAD], con domicilio en [DOMICILIO] y D.N.I. núm. [DNI/NIE].

INTERVIENEN

Ambos cónyuges en su propio nombre y representación, reconociéndose mutuamente la capacidad legal suficiente para otorgar el presente CONVENIO REGULADOR, y por vía de antecedentes

EXPONEN

PRIMERO.– Que los comparecientes contrajeron matrimonio civil en [LOCALIDAD], el día [DÍA] de [MES] de [AÑO], figurando dicho matrimonio inscrito en el Registro Civil de [LOCALIDAD], al tomo [TOMO], página [PÁGINA]. El matrimonio se contrajo bajo el régimen económico de separación de bienes, habiéndose otorgado capitulaciones matrimoniales el [DÍA] de [MES] de [AÑO] ante el Ilmo. Notario de [LOCALIDAD] D. [NOMBRE DEL NOTARIO], bajo el número [Nº DE PROTOCOLO] del orden de su protocolo.

SEGUNDO.– Que de dicho matrimonio no han nacido hijos, por lo que nada cabe decir a este respecto.

TERCERO.– El domicilio conyugal estuvo establecido en [DOMICILIO CONYUGAL].

CUARTO.– Por razones que no vienen al caso, los cónyuges han decidido hacer vidas independientes, solicitando de común acuerdo la disolución de su matrimonio.

QUINTO.– Que con objeto de cumplir los requisitos establecidos en el artículo 90 del Código Civil relativos a las exigencias y características que ha de tener el convenio regulador que acompañe a las demandas de divorcio de mutuo acuerdo, ambos cónyuges suscriben el presente convenio con base en las siguientes

ESTIPULACIONES

Del consentimiento

Por medio del presente convenio los esposos, de modo reflexionado y previo el asesoramiento que han creído conveniente, se ratifican en la decisión de proceder a la disolución del vínculo matrimonial.

Del mismo modo, establecen los efectos civiles de su divorcio conforme a las circunstancias y a lo dispuesto en el Código Civil.

Del domicilio

Ambos cónyuges se comprometen a respetar la libertad e independencia tanto profesional como personal del otro, así como la libre fijación de sus domicilios, sin intervenir ni inmiscuirse en modo alguno.

Del uso y disfrute del domicilio conyugal

Ambas partes acuerdan atribuir el uso y disfrute de la vivienda que ha sido el domicilio habitual a [LA ESPOSA / EL ESPOSO: NOMBRE Y APELLIDOS], puesto que [EL OTRO CÓNYUGE: NOMBRE Y APELLIDOS] tiene otra vivienda en plena propiedad.

De las medidas respecto de los hijos

No habiendo descendencia, no cabe pronunciamiento al respecto.

De las pensiones

Ambos cónyuges acuerdan no establecer pensión compensatoria alguna, ni equivalente en concepto alimenticio, a favor del otro, toda vez que ambos cónyuges obtienen ingresos equiparables y no se produce desequilibrio alguno entre la situación actual y la anterior.

Del régimen económico matrimonial: extinción del condominio o cese en la proindivisión

El matrimonio se contrajo, como ya se ha expuesto, bajo el régimen económico de separación de bienes, habiéndose otorgado capitulaciones matrimoniales el [DÍA] de [MES] de [AÑO] ante el Ilmo. Notario de [LOCALIDAD] D. [NOMBRE DEL NOTARIO], bajo el número [Nº DE PROTOCOLO] del orden de su protocolo, por lo que, al no existir patrimonio ganancial, no tienen nada que reclamarse al respecto.

[NOTA: la extinción del proindiviso es opcional; suprimir este apartado si no hay bienes en común.]

Extinción del proindiviso

No obstante, se procederá en el plazo máximo de [PLAZO MÁXIMO PARA OTORGAR LA ESCRITURA DE ESCISIÓN DE CONDOMINIO, SI HUBIERA BIENES EN PROINDIVISO] desde la fecha de hoy a otorgar escritura pública de división de cosa común respecto de la vivienda, así como a dividir el resto de bienes que mantienen en común y que se relacionan a continuación:

• La vivienda conyugal, sita en la localidad de [LOCALIDAD], calle [DOMICILIO]. En tanto no se proceda a la adjudicación del antedicho bien, cada propietario contribuirá según su coeficiente de propiedad al abono de todos los gastos y cargas inherentes a la propiedad, tales como préstamo hipotecario, IBI, gastos ordinarios y extraordinarios de Comunidad y seguro de la vivienda.

• El vehículo marca [MARCA], modelo [MODELO], matrícula [MATRÍCULA], propiedad por mitades de los suscribientes, será preferentemente adjudicado a [NOMBRE Y APELLIDOS], quien lo viene usando desde la compra del mismo y quien se hará cargo de todos los gastos inherentes al mantenimiento del vehículo.

Tanto el vehículo como el inmueble serán adjudicados en la misma fecha y en unidad de acto. La valoración de los mismos será dada por un perito tasador colegiado en el caso del inmueble y, para el vehículo, se acudirá a un concesionario oficial.

• Finalmente, respecto de las cuentas corrientes, valores e inversiones, los cuales comparten al 50 %, serán repartidos en ese mismo porcentaje, respetándose en todo caso las fechas de vencimiento.

Eficacia del convenio regulador

Los presentes acuerdos obligan a las partes, comprometiéndose a cumplirlos de buena fe desde la fecha de la firma del presente convenio regulador.

Asimismo, se comprometen a ratificarse en el presente convenio ante la autoridad judicial, junto con la solicitud de divorcio que, a tenor de la legislación vigente, solicitarán de mutuo acuerdo y cuyos gastos serán abonados por mitades, salvo en el supuesto de incumplimiento por una de las partes, en cuyo caso se hará cargo de la totalidad de las costas y gastos ocasionados.

En prueba de conformidad con todo lo acordado, firman los comparecientes el presente documento por triplicado y en todas sus hojas, en el lugar y fecha indicados en el encabezamiento, quedando un ejemplar para cada cónyuge y otro a los efectos de su aportación al Tribunal, junto con la solicitud de divorcio.

Fdo.: D. [NOMBRE Y APELLIDOS]

Fdo.: Dª [NOMBRE Y APELLIDOS]
