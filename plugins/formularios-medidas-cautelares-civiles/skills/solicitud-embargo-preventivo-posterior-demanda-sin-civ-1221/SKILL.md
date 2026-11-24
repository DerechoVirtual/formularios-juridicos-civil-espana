---
name: solicitud-embargo-preventivo-posterior-demanda-sin-civ-1221
description: "Solicitud de embargo preventivo posterior a la demanda y sin audiencia del demandado. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud de embargo preventivo posterior a la demanda y sin audiencia del demandado

> Formulario **CIV-1221** del plugin **Medidas cautelares y diligencias preliminares** (`formularios-medidas-cautelares-civiles`) · Civil › Medidas cautelares y diligencias preliminares · normativa revisada el 24-11-2026.

## Qué es

Escrito del demandante solicitando, ya iniciado el proceso ordinario y sin audiencia del demandado, la medida cautelar de embargo preventivo de bienes, al amparo del art. 730.4 LEC, por hechos nuevos o sobrevenidos que justifican la petición tardía (por ejemplo, embargos trabados a otros acreedores y situación de iliquidez del deudor). Incluye apariencia de buen derecho, peligro en la demora, caución y designación de bienes (formulario adaptado a la reforma procesal de la LO 1/2025).

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud de embargo preventivo posterior a la demanda y sin audiencia del demandado» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud de embargo preventivo posterior a la demanda y sin audiencia del demandado” para mi caso». También puedes invocarla directamente con `/formularios-medidas-cautelares-civiles:solicitud-embargo-preventivo-posterior-demanda-sin-civ-1221`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-medidas-cautelares-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Medidas cautelares y diligencias preliminares) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (10 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] FECHA (3 veces)
- [ ] Nº DE PROCEDIMIENTO (3 veces)
- [ ] Nº (2 veces)
- [ ] Nº DE DOCUMENTOS (2 veces)
- [ ] AÑO
- [ ] DESCRIPCIÓN Y DATOS REGISTRALES
- [ ] DÍA
- [ ] FOLIO
- [ ] LIBRO
- [ ] MES
- [ ] NOMBRE Y APELLIDOS
- [ ] NOMBRE Y APELLIDOS O DENOMINACIÓN SOCIAL
- [ ] Nº DE FAX
- [ ] Nº DE FINCA
- [ ] NÚMERO
- [ ] PLANTA
- [ ] SEDE
- [ ] TOMO
- [ ] TRIBUNAL
- [ ] TRIBUNALES

## Normas que cita el formulario

- art. 730.4 LEC
- art. 723.1 LEC
- art. 721 LEC
- art. 733.2 LEC
- art. 728.2 LEC
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

- Junto a «…DIMIENTO] A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

NOTA DE USO: el artículo 730.4 de la LEC dispone que, con posterioridad a la presentación de la demanda o pendiente recurso, sólo podrá solicitarse la adopción de medidas cautelares cuando la petición se base en hechos y circunstancias que justifiquen la solicitud en esos momentos. Por tanto, en la petición ha de hacerse constar en cada caso los hechos nuevos o desconocidos, o la modificación de circunstancias que determinan que la petición no se hubiera realizado anteriormente con la presentación de la demanda. Jurisprudencia: la petición de medidas cautelares sólo puede basarse en hechos desconocidos al hacerse aquella o posteriores a la misma (AAP La Coruña, de 16 de enero de 2007, y de 25 de junio de 2008; AAP Guipúzcoa, Sección 2.ª, de 8 de junio de 2006).

PROCESO ORDINARIO NÚMERO [Nº DE PROCEDIMIENTO]


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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

D./Dª [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, actuando en representación de [NOMBRE Y APELLIDOS O DENOMINACIÓN SOCIAL], según tengo acreditado en los autos de proceso ordinario número [Nº DE PROCEDIMIENTO] seguidos ante ese Tribunal, comparezco y, como mejor proceda en derecho, DIGO:

Que por medio del presente, al amparo de lo dispuesto en el artículo 730.4 de la LEC, solicito la MEDIDA CAUTELAR de embargo preventivo de bienes del demandado en cantidad suficiente para cubrir las responsabilidades que pudieran derivarse de este proceso, por importe de [IMPORTE] euros, en base a los siguientes

HECHOS

PRIMERO.– La presente demanda se sigue por incumplimiento del contrato de fecha [FECHA], derivado del impago de [OBJETO DEL IMPAGO: p. ej., diversas entregas de material de construcción], reclamándose la cantidad de [IMPORTE] euros, más los intereses desde [FECHA].

Aun cuando con nuestra demanda no se solicitaron medidas cautelares, han sobrevenido nuevos hechos y circunstancias que determinan la necesidad y urgencia de adoptarlas, puesto que en otro caso no podrá ser efectiva la tutela que se pretende por esta parte.

Las circunstancias nuevas que concurren y que fundan la petición de la medida cautelar de embargo preventivo con posterioridad a la demanda derivan del hecho de que ha tenido conocimiento esta parte de que el pasado día [FECHA] se despachó ejecución forzosa contra el demandado en el proceso número [Nº DE PROCEDIMIENTO] seguido ante el Tribunal [TRIBUNAL], trabándose embargo de los bienes del demandado para responder de la cantidad de [IMPORTE] euros de principal y de [IMPORTE] euros en concepto de intereses y costas y, en concreto, se ha tomado anotación registral del embargo sobre [BIENES EMBARGADOS: p. ej., los cuatro pisos] titularidad del demandado.

A efectos acreditativos, acompañamos como documentos número [Nº DE DOCUMENTOS] certificaciones del Registro de la Propiedad de [LOCALIDAD], donde constan la titularidad de los inmuebles, los datos del proceso de ejecución y el importe de la traba.

Habiendo tenido conocimiento de estos hechos y tras diferentes gestiones, esta representación tiene noticia de que el demandado está en una situación de iliquidez, estando pendientes otras [NÚMERO] demandas judiciales en los Tribunales [TRIBUNALES], reclamándole las cantidades de [IMPORTE] euros y [IMPORTE] euros, respectivamente, tal como se acredita por los documentos número [Nº DE DOCUMENTOS] que acompañamos, consistentes en copias de las demandas y auto de admisión de los referidos procesos.

SEGUNDO.– Estos nuevos hechos justifican la pretensión cautelar que ahora se formula al amparo del artículo 730.4 de la LEC, puesto que el embargo de los bienes del demandado en el proceso de ejecución número [Nº DE PROCEDIMIENTO] modifica sustancialmente la situación fáctica que existía al momento de interponerse la demanda, lo cual nos lleva a solicitar que se adopte urgentemente la medida cautelar de embargo preventivo, puesto que es necesaria para la efectividad del derecho instado por esta parte ante la jurisdicción.

A los anteriores hechos son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

Competencia

Le corresponde al Tribunal al que me dirijo, ya que es el competente por estar conociendo del asunto en primera instancia, con fundamento en el artículo 723.1 de la LEC.

Legitimación

Le corresponde a esta parte en su condición de actor principal en el presente proceso (art. 721 LEC).

Procedimiento

Es el previsto en el artículo 730.4 de la LEC, el cual establece que «Con posterioridad a la presentación de la demanda o pendiente recurso sólo podrá solicitarse la adopción de medidas cautelares cuando la petición se base en hechos y circunstancias que justifiquen la solicitud en esos momentos. Esta solicitud se sustanciará conforme a lo prevenido en el presente Capítulo». Atendido lo anterior, y siendo urgente la adopción de la medida, se interesa que la misma se decrete sin audiencia del demandado (art. 733.2 LEC), pues concurren en este caso razones de urgencia concretadas en los embargos ya decretados sobre las fincas del demandado y en la pendencia de otras reclamaciones.

Presupuesto de la solicitud posterior a la demanda

Concurre asimismo el presupuesto establecido en el artículo 730.4 de la LEC, al fundarse esta petición en hechos nuevos o sobrevenidos, habiendo interpretado los Tribunales de forma uniforme que la petición de medidas cautelares con posterioridad a la presentación de la demanda sólo puede basarse en hechos desconocidos al hacerse aquella o posteriores a la misma (AAP La Coruña, de 16 de enero de 2007, rec. 374/2006, y de 25 de junio de 2008, rec. 559/2007; AAP Guipúzcoa, Sección 2.ª, de 8 de junio de 2006, rec. 2435/2005).

Apariencia de buen derecho

Se deriva de la documentación adjunta a la demanda y en la que consta el crédito del que es titular esta parte (art. 728.2 LEC).

Peligro de mora

Se deriva de la situación económica en la que se encuentra el demandado, habiéndose trabado embargo de sus bienes y teniendo pendientes otras reclamaciones, ya que solamente con la medida cautelar solicitada se podrá garantizar la efectividad de una eventual sentencia favorable que se pudiere dictar en beneficio de mi mandante (art. 728.1 LEC).

Medida interesada

Es la del embargo preventivo de los bienes para asegurar la ejecución de la sentencia de condena que pudiera dictarse, interesándose que se proceda al embargo de bienes suficientes para cubrir la cantidad reclamada de [IMPORTE] euros, y que la medida se adopte sin audiencia del demandado.

Caución

Con fundamento en el artículo 732.3 de la LEC se solicita que sea fijada ésta en [IMPORTE] euros, dadas las condiciones del crédito expuesto, la situación del demandado y los posibles perjuicios que se le pudieren generar por ello.

En base a lo anterior,

SUPLICO AL TRIBUNAL que tenga por presentado escrito con los documentos a él anejos y copias, y acuerde el embargo preventivo de los bienes titularidad del demandado que se relacionan en el otrosí de esta solicitud para asegurar la ejecución de las pretensiones de condena por importe de [IMPORTE] euros sostenidas en este proceso, solicitando que se acuerde el embargo sin audiencia del demandado al concurrir motivos de urgencia. Asimismo se interesa que, en caso de decretarse, se acuerde la anotación preventiva del embargo decretado, dirigiendo el pertinente mandamiento al Registro de la Propiedad de [LOCALIDAD] e interesando que se remita el mismo por [ELEGIR: vía telemática / fax (número [Nº DE FAX])] por razones de urgencia. De cara a la adopción de tal medida cautelar se solicita asimismo que se tenga por ofrecida una caución de [IMPORTE] €.

OTROSÍ DIGO que designo como fincas titularidad del demandado para proceder a su embargo preventivo las siguientes:

1) Vivienda señalada con el número [Nº], planta [PLANTA], inscrita en el Registro de la Propiedad de [LOCALIDAD], Tomo [TOMO], Libro [LIBRO], Folio [FOLIO], Finca registral [Nº DE FINCA].

2) Vivienda [DESCRIPCIÓN Y DATOS REGISTRALES].

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO]

Firma Abogado: ______________________

Firma Procurador: ______________________
