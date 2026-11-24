---
name: solicitud-embargo-preventivo-instancia-parte-civ-1211
description: "Solicitud de embargo preventivo a instancia de parte en un procedimiento arbitral. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud de embargo preventivo a instancia de parte en un procedimiento arbitral

> Formulario **CIV-1211** del plugin **Medidas cautelares y diligencias preliminares** (`formularios-medidas-cautelares-civiles`) · Civil › Medidas cautelares y diligencias preliminares · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud de embargo preventivo a instancia de parte en un procedimiento arbitral» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud de embargo preventivo a instancia de parte en un procedimiento arbitral” para mi caso». También puedes invocarla directamente con `/formularios-medidas-cautelares-civiles:solicitud-embargo-preventivo-instancia-parte-civ-1211`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-medidas-cautelares-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Medidas cautelares y diligencias preliminares) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (8 veces)
- [ ] Nº DE DOCUMENTO (6 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] Nº DE PROCEDIMIENTO (3 veces)
- [ ] FECHA (2 veces)
- [ ] AÑO
- [ ] DESCRIPCIÓN DEL BIEN
- [ ] DÍA
- [ ] LUGAR
- [ ] MARCA/MODELO
- [ ] MATRÍCULA
- [ ] MES
- [ ] NOMBRE DE LA ASOCIACIÓN
- [ ] NOMBRE DE LOS ACREEDORES
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] NOMBRE Y APELLIDOS
- [ ] Nº
- [ ] Nº DE CLÁUSULA
- [ ] SEDE

## Normas que cita el formulario

- art. 722 LEC
- art. 15 Ley 60/2003
- art. 730.2 LEC
- art. 733.2 LEC
- art. 728.1 LEC
- art. 732.3 LEC

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

D. [NOMBRE Y APELLIDOS] Procurador de los Tribunales, actuando en representación de [NOMBRE DEL REPRESENTADO/A], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño a este escrito, ante el Tribunal comparezco y como mejor proceda en derecho, DIGO:

Que al amparo de lo dispuesto en el artículo 722 de la LEC, por medio de la presente solicito la adopción de la medida cautelar de embargo preventivo de bienes contra D con domicilio en [LOCALIDAD], parte demandada en el procedimiento arbitral seguido a instancias de mi representado que se dirá, en base a los siguientes:

HECHOS

PRIMERO En fecha [FECHA] mi representado concertó contrato de compraventa y ejecución de obra correspondiente a dos viviendas sobre sendas fincas con el demandado D en fecha [FECHA], fijando como precio el de [IMPORTE] euros que debía abonarse en [Nº] plazos, a razón de [IMPORTE] euros cada uno, debiendo entregarse las dos viviendas, terminadas y libres de cargas, en fecha

En la cláusula [Nº DE CLÁUSULA] del contrato, las partes acordaban, conforme al art. 9 de la Ley de Arbitraje, someter todas las controversias derivadas del contrato, encomendando la administración del arbitraje y designación de árbitros a la Asociación

Mi representado cumplió con sus obligaciones contractuales, realizando los pagos puntualmente al demandado, entregando la cantidad total de [IMPORTE] euros, pero el demandado incumplió sus obligaciones, estando en la actualidad sin finalizar las edificaciones pese a haber transcurrido en exceso el plazo pactado, lo cual llevó a mi mandante a iniciar el procedimiento arbitral ante la Asociación [NOMBRE DE LA ASOCIACIÓN], el cual se sigue con el número de expediente [Nº DE PROCEDIMIENTO], habiendo interpuesto la correspondiente demanda en el día de hoy.

A efectos acreditativos, acompaño como documentos [Nº DE DOCUMENTO], contrato de compraventa, recibos de los pagos realizados, acta notarial de fecha donde se describe la situación de las obras no finalizadas, solicitud de arbitraje, resoluciones dictadas en el procedimiento arbitral y demanda interpuesta en el citado procedimiento arbitral.

SEGUNDO En base a los anteriores hechos, nos vemos en la obligación de solicitar la tutela cautelar del órgano jurisdiccional al que nos dirigimos, al concurrir circunstancias que determinan su urgencia y necesidad, puesto que, de no adoptarse, puede impedirse la realización del derecho de mi mandante en el procedimiento arbitral iniciado.

Al respecto, como se ha indicado, mi representado ha realizado pagos al demandado, a cuenta del precio de las fincas adquiridas, por un importe total de [IMPORTE] euros, a los que habría que añadir el correspondiente I.V.A., sin recibir ninguna contraprestación y sin que la otra parte cumpliera sus obligaciones y sin que previsiblemente pueda cumplirlas, puesto que las fincas se encuentran gravadas con cargas de gran entidad, tal como se expondrá a continuación.

TERCERO La considerable cantidad dineraria entregada por mi representado a cuenta del precio no podrá ser recuperada, ni tan siquiera en parte, si no se adoptan medidas cautelares con la mayor urgencia, puesto que mi representado, al solicitar información registral sobre las fincas que el demandado le vendió, ha comprobado que las fincas adquiridas y otras de la misma promoción titularidad del demandado, se encuentran gravadas con hipotecas y anotaciones de embargos a favor de otros acreedores, concretamente [NOMBRE DE LOS ACREEDORES], con lo cual hay un peligro cierto de que dichos gravámenes puedan ser ejecutados y no pueda ser cumplida la obligación del demandado de entrega de las fincas adquiridas, libres de cargas, a la parte compradora (acompaño como documentos [Nº DE DOCUMENTO] notas expedidas por el Registro de la Propiedad de [LOCALIDAD] donde se constatan las cargas de las fincas adquiridas y otras titularidad del demandado), siendo también previsible que no pueda recuperar el dinero entregado a cuenta caso de no adoptarse las medidas cautelares.

Asimismo, esta parte ha podido comprobar que el demandado se encuentra en una situación de iliquidez, tal y como se deriva de las últimas cuentas anuales depositadas en el Registro Mercantil tal, según resulta del documento nº [Nº DE DOCUMENTO] que se une a esta solicitud, constándole únicamente la titularidad del vehículo camión, marca [MARCA/MODELO] matrícula [MATRÍCULA], matriculado en [LOCALIDAD] según certificación de la Jefatura Provincial de Tráfico de que se adjunta como documento nº [Nº DE DOCUMENTO]

FUNDAMENTOS DE DERECHO

Competencia

Le corresponde al Tribunal al que me dirijo ya que es el competente con fundamento en el art. 722 y 724 LEC al ser en ese partido en el que el laudo debe ser ejecutado.

Legitimación

El artículo 722 dispone: "Podrá pedir al Tribunal medidas cautelares quien acredite ser parte de convenio arbitral con anterioridad a las actuaciones arbitrales. También podrá pedirlas quien acredite ser parte de un proceso arbitral pendiente en España; o, en su caso, haber pedido la formalización judicial a que se refiere el artículo 15 de la Ley 60/2003, de 23 de diciembre, de Arbitraje; o en el supuesto de un arbitraje institucional, haber presentado la debida solicitud o encargo a la institución correspondiente según su Reglamento".

Por tanto, le corresponde la legitimación activa a esta parte en su condición de acreedor y demandante en el procedimiento arbitral número [Nº DE PROCEDIMIENTO], estando legitimado pasivamente el demandado (art. 722 LEC), estableciendo el artículo 11.3 de la Ley de Arbitraje que "el convenio arbitral no impedirá a ninguna de las partes, con anterioridad a las actuaciones arbitrales o durante su tramitación, solicitar de un tribunal la adopción de medidas cautelares ni a éste concederlas".

Procedimiento

Es el previsto en el art. 730.2 LEC al interesarse la adopción de la medida cautelar son carácter previo a la interposición de la demanda y sin audiencia del demandado (art. 733.2 LEC) pues concurren en este caso razones de urgencia ya que ante la existencia de embargos y cargas sobre las fincas adquiridas y la situación de iliquidez del demandado frente a la que se solicitan las medidas cautelares en cualquier momento pueden ejecutarse las fincas, e incluso el demandado puede deshacerse de sus bienes y desaparecer del tráfico con el perjuicio que ello ocasionaría a mi mandante que no vería satisfecho el importe de su crédito, ni siquiera parcialmente.

Apariencia de buen derecho

Se deriva de la documentación adjunta a esta solicitud y en la que consta el puntual cumplimiento de los pagos a que venía obligado mi mandante en el contrato concertado con el demandado, según se acredita documentalmente en los documentos [Nº DE DOCUMENTO], así como el incumplimiento de las obligaciones del demandado, según consta en el acta notarial asimismo acompañada a esta solicitud como documento

Peligro de mora

Se deriva de todos los elementos expuestos, habiendo entregado mi representado la mayor parte del precio pactado, sin estar finalizadas las viviendas pese al transcurso del plazo fijado en el contrato, por las cargas que pesan sobre las fincas, y por la deficiente situación económica en la que se encuentra el demandad ya que solamente con la medida cautelar solicitada se podrá garantizar la efectividad de una eventual sentencia favorable que se pudiere dictar en beneficio de mi mandante (art. 728.1 LEC).

Medida interesada

Es la del embargo preventivo de bienes para asegurar la cantidad cuya condena se pretende en el procedimiento arbitral por importe de [IMPORTE] euros satisfecho por mi representado, interesando que se tome anotación de embargo sobre las fincas titularidad del demandado que se relacionan en el otrosí y que constan en las notas del Registro de la Propiedad acompañadas como documento número [Nº DE DOCUMENTO] En el presente caso concurren los requisitos necesarios para la adopción de la medida "inaudita parte", al haberse justificado razones de urgencia y necesidad.

Caución

Con fundamento en el art. 732.3 LEC se solicita sea fijada ésta en [IMPORTE] euros dadas las circunstancias fácticas, la situación del demandado y los posibles perjuicios que se le pudieren generar por ello, teniendo en cuenta que el demandado ha percibido una considerable cantidad de dinero de la que se ha aprovechado sin contraprestación alguna a cambio, y porque además, al existir ya gravámenes anteriores sobre las fincas cuya anotación de embargo se solicita, los perjuicios que pueda generar la nueva medida quedan garantizados con la caución ofrecida.

En base a lo anterior,

SUPLICO AL TRIBUNAL que tenga por presentado escrito con los documentos a él anejos y copias, tenga por comparecido a esta parte y acuerde el embargo preventivo de los bienes titularidad del demandado que se relacionan en el otrosí de esta solicitud para asegurar la ejecución de las pretensiones de condena por importe de [IMPORTE] euros sostenidas en el procedimiento arbitral número [Nº DE PROCEDIMIENTO], solicitando que se acuerde el embargo sin audiencia del demandado al concurrir motivos de urgencia. Asimismo se interesa que en caso de decretarse se acuerde la anotación preventiva del embargo decretado dirigiendo el pertinente mandamiento al Registro de la Propiedad de [LOCALIDAD] e interesando que se remita el mismo por fax por razones de urgencia (número de fax). De cara a la adopción de tal medida cautelar se solicita asimismo que se tenga por ofrecida una caución de [IMPORTE] euros.

OTROSÍ DIGO que designo como fincas titularidad del demandado para proceder a su embargo preventivo, las siguientes:

1) Vivienda, señalada con el número, planta Inscrita en el Registro de la Propiedad de Tomo, Libro, Folio, Finca registral

2) Vivienda [DESCRIPCIÓN DEL BIEN]

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma de abogado y procurador

========================================================================
