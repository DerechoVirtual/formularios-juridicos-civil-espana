---
name: auto-acuerda-medida-cautelar-sin-oir-antes-demandado-civ-1797
description: "Auto que acuerda una medida cautelar sin oír antes al demandado. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Auto que acuerda una medida cautelar sin oír antes al demandado

> Formulario **CIV-1797** del plugin **Resoluciones judiciales civiles: autos, decretos y diligencias** (`formularios-resoluciones-judiciales-civiles`) · Civil › Resoluciones judiciales (autos, decretos, providencias, diligencias) · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **resoluciones judiciales (autos, decretos, providencias, diligencias)**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Auto que acuerda una medida cautelar sin oír antes al demandado» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Auto que acuerda una medida cautelar sin oír antes al demandado” para mi caso». También puedes invocarla directamente con `/formularios-resoluciones-judiciales-civiles:auto-acuerda-medida-cautelar-sin-oir-antes-demandado-civ-1797`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-resoluciones-judiciales-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Resoluciones judiciales civiles: autos, decretos y diligencias) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] FECHA (4 veces)
- [ ] DENOMINACIÓN SOCIAL (3 veces)
- [ ] IMPORTE EN CIFRA (3 veces)
- [ ] LUGAR (3 veces)
- [ ] IMPORTE (2 veces)
- [ ] ACTO O RESOLUCIÓN

## Normas que cita el formulario

- art. 28.3 Ley 12/1992
- art. 733 LEC
- art. 726 LEC
- art. 727 LEC
- art. 728 LEC
- art. 575 LEC
- art. 739 LEC

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

Resolución que acuerda la adopción de la medida cautelar de embargo preventivo de bienes solicitada en el proceso principal de reclamación de cantidades por comisiones impagadas e indemnización del art. 28.3 Ley 12/92, sobre el contrato de agencia (LAG), por clientela conseguida.

AUTO

En [LUGAR], a [FECHA].

En [LUGAR], a [FECHA].

Juez Sr./a [NOMBRE Y APELLIDOS]

ANTECEDENTES DE HECHO

PRIMERO

Por la Procurador/a Sr./a [NOMBRE Y APELLIDOS], en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS], se ha solicitado la adopción de la medida cautelar de embargo preventivo, para asegurar la efectividad de la pretensión formulada en el proceso principal frente a [ACTO O RESOLUCIÓN], S.A., de reclamación de cantidades por comisiones impagadas e indemnización del art. 28.3 de la Ley 12/1992, sobre el contrato de agencia (LAG), por clientela conseguida a la sociedad representada.

SEGUNDO

La dicha parte solicitante ha presentado como documental el contrato mercantil de agente comercial de fecha [FECHA], once contratos intermediados por él y las correspondientes facturas, así como los siguientes certificados del Registro Mercantil y del Registro de la Propiedad:

Asimismo ha ofrecido la prestación de caución suficiente para responder de los daños y perjuicios que pudieran derivarse de la adopción de la medida.

TERCERO

En la solicitud referida, la parte actora ha pedido se acuerde la medida cautelar sin dar previamente audiencia a la parte demandada, por las razones expuestas en la fundamentación de aquélla.

RAZONAMIENTOS JURIDICOS

PRIMERO

El principio general del proceso cautelar es la exigencia de la previa audiencia de la parte demandada o contradicción simultánea, si bien el art. 733 LEC admite que excepcionalmente pueda acordarse sin la dicha audiencia cuando concurran razones de urgencia o cuando la audiencia pudiera comprometer el buen fin de la medida.

En caso de tal salvedad, habrá que razonar, según se hará, la concurrencia de los requisitos para la adopción de la medida, y los motivos para prescindir de la audiencia previa del demandado.

Se estima concurren estos últimos por la confluencia de documentación que acredita un empleo de la personalidad jurídica abusiva a fin de que [DENOMINACIÓN SOCIAL], S.A. quede sin su actividad de distribución sin mengua de los intereses de sus titulares y con perjuicio de sus acreedores; así como de la documentación que acredita la ausencia de bienes libres de responsabilidad, estando los que restan amenazados con ser vendidos en condiciones sospechosas.

SEGUNDO

La batería de preceptos de los arts. 726 a 728 LEC, regula un régimen en la adopción de medidas cautelares, cual el siguiente:

Características: Que la medida solicitada sea alguna de las previstas en el art. 727 LEC o cualquier otra actuación directa o indirecta sobre bienes o persona del demandado, siempre que reúna las características señaladas de temporalidad, provisionalidad, instrumentalidad, susceptibilidad de modificación y alzamiento, y posible sustitución por otras menos onerosas para el demandado (art. 726 LEC), y en todo caso resulte idónea y congruente con la pretensión cuya efectividad se desea asegurar.

Presupuestos: Que la parte solicitante acredite el peligro de mora procesal, es decir, el riesgo de la demora o la infructuosidad de la tutela judicial que en su día pudiera merecerse (‘periculum in mora’), y que le asiste una apariencia de buen derecho, es decir que, sin prejuzgar el fondo del asunto, sea positivo el juicio indiciario de la existencia del derecho reclamado (‘fumus boni iuris’). Para la ejecución de la medida que proceda, es menester que la parte solicitantes ofrezca caución suficiente para responder de forma rápida y eficaz, de los daños y perjuicios que pudieran ocasionarse (art. 728 LEC).

TERCERO

Los elementos documentales que aporta el demandante acreditan preliminarmente ese juicio provisional e indiciario favorable al fundamento de la pretensión principal, que es punto medio entre la pura incertidumbre y la certeza plena que sólo se podrá alcanzar formalmente al término del proceso, y el peligro de retraso resulta demostrado sencillamente por la certificación registral, puesto que de no adoptarse la medida, durante la pendencia del proceso, la sociedad demandada quedará despatrimonializada, impidiéndose la efectividad de la tutela que pudiera otorgarse en la eventual sentencia estimatoria, sin que en este peligro se haya colocado por su negligencia el demandante, según apuntilla el art. 728.1, párrafo 2.º LEC.

CUARTO

Análogamente que para el embargo ejecutivo (art. 575 LEC), al que remite el art. 738.2, párrafo 1.º LEC, se habrá de determinar la cantidad que con el embargo preventivo se tiene que asegurar por la suma de las comisiones líquidas, incluyendo los intereses de mora devengados al interponerse la demanda, y la indemnización resolutoria; esta cantidad es la de [IMPORTE] por los conceptos indicados.

Con dicha referencia, la cuantía, forma y plazo de la caución requerida, atendiendo a la importancia real de la pretensión que se quiere asegurar, al fundamento del derecho reclamado, y a la efectividad y cuantía de los posibles daños y perjuicios derivados de la ejecución de la medida, se estima procedente la cuantía de [IMPORTE] euros ([IMPORTE EN CIFRA] €), puesto que se procura sencillamente una dificultad de venta, y los bienes ya están gravados, siendo su valor estimado no excesivamente amplio para cubrir el débito.

La caución se prestará en la modalidad ofrecida y en plazo que se señala.

PARTE DISPOSITIVA

Estimando la solicitud de adopción de medida cautelar formulada por el Procurador/a D./Dña. [NOMBRE Y APELLIDOS], en nombre y presentación de D./Dña. [NOMBRE Y APELLIDOS], sin previa audiencia de la parte demandada, se acuerda el embargo preventivo de bienes de responsabilidad de [DENOMINACIÓN SOCIAL], S.A. por la cantidad que se reclama deeuros (€ [IMPORTE EN CIFRA]).

La anterior medida cautelar no se ejecutará en tanto que la parte demandante no preste la caución por importe deeuros (€ [IMPORTE EN CIFRA]), en forma de aval bancario, en el plazo de cinco días hábiles desde la notificación.

Se imponen las costas del incidente a la parte demandada.

Contra la presente resolución no cabe recurso alguno, pero [DENOMINACIÓN SOCIAL], S.A., parte demandada, podrá formular oposición a la medida acordada en el plazo de veinte días contados desde la notificación de este auto por alguna de las causas expresadas en el art. 739 LEC.

Así lo acuerdo, mando y firmo:

Por ser de Justicia que pido en [LUGAR], a [FECHA].

Firma de Abogado/a	Firma de Procurador/a
