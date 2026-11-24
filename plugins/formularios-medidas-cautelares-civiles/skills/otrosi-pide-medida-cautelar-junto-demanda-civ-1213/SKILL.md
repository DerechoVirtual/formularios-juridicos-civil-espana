---
name: otrosi-pide-medida-cautelar-junto-demanda-civ-1213
description: "Otrosí que pide una medida cautelar junto con la demanda. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Otrosí que pide una medida cautelar junto con la demanda

> Formulario **CIV-1213** del plugin **Medidas cautelares y diligencias preliminares** (`formularios-medidas-cautelares-civiles`) · Civil › Medidas cautelares y diligencias preliminares · normativa revisada el 24-11-2026.

## Qué es

Otrosí que se incluye en una demanda de impugnación de acuerdos de la junta de propietarios para solicitar, como medida cautelar, la suspensión de la ejecución del acuerdo impugnado (art. 727 LEC y art. 18 LPH), cuando su ejecución causaría daños difícilmente reparables (por ejemplo, unas obras en elementos comunes). Si la medida se pide junto con la demanda, se articula por otrosí, aportando con él los documentos que acrediten la apariencia de buen derecho y el peligro por la demora o ofreciendo otros medios de prueba.

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Otrosí que pide una medida cautelar junto con la demanda» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Otrosí que pide una medida cautelar junto con la demanda” para mi caso». También puedes invocarla directamente con `/formularios-medidas-cautelares-civiles:otrosi-pide-medida-cautelar-junto-demanda-civ-1213`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-medidas-cautelares-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Medidas cautelares y diligencias preliminares) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (6 veces)
- [ ] Nº (6 veces)
- [ ] IMPORTE (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] DENOMINACIÓN O DOMICILIO DE LA COMUNIDAD

## Normas que cita el formulario

- art. 727.11.ª LEC
- art. 732.2 LEC
- art. 723.1 LEC
- art. 721 LEC
- art. 733 LEC
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

OTROSÍ DIGO que, por medio del presente y al amparo de lo dispuesto en el artículo 727.11.ª de la LEC, en relación con el artículo 18 de la Ley de Propiedad Horizontal, solicito la adopción de la MEDIDA CAUTELAR DE SUSPENSIÓN DE LA EJECUCIÓN DE ACUERDO DE LA JUNTA GENERAL DE PROPIETARIOS de fecha [FECHA], en base a los siguientes

HECHOS

PRIMERO.– Se solicita la suspensión del acuerdo impugnado con la demanda, adoptado por la junta de propietarios de fecha [FECHA], bajo el punto [Nº] del orden del día de la junta, que fue aprobado por mayoría de los propietarios presentes en la junta, y que se refiere a [DESCRIBIR EL ACUERDO: p. ej., la autorización de obras en el inmueble para la instalación de un tubo de salida de humos y ventilación desde la planta sótano hasta el ático, el cual perfora varios forjados comunitarios y sigue por el patio comunitario], acuerdo cuya nulidad se solicita en esta demanda por no reunirse las mayorías necesarias legalmente establecidas y por causar un gravísimo perjuicio a mi representado, instándose la suspensión con carácter urgente.

SEGUNDO.– Que, tal como se ha relatado en la demanda, el acuerdo de la junta impugnado fue adoptado en [primera convocatoria], por [mayoría simple], sin respetar el régimen de mayorías establecido legalmente para la adopción de acuerdos que afectan a la estructura y elementos comunes del edificio, como es el caso ahora contemplado. Pero es que, además, el acuerdo es de imposible ejecución por cuanto las obras necesariamente van a determinar daños estructurales en el inmueble, y singularmente en la [vivienda/local] de mi representado, según se razona ampliamente en el informe pericial elaborado por el arquitecto D./Dña. [NOMBRE Y APELLIDOS] que se acompaña como documento n.º [Nº] de la demanda, y el cual concluye la irreparabilidad de los daños.

TERCERO.– En relación con lo expuesto en el hecho anterior, existe un evidente peligro en la demora, expresado claramente en el informe pericial acompañado como documento [Nº], puesto que la ejecución de las obras acordadas, atendido el estado físico y la antigüedad de la finca, puede ocasionar daños irreparables en la estructura. Razones de urgencia que se intensifican por cuanto las obras han sido iniciadas el pasado día [FECHA], tal como se acredita con el acta notarial de constancia acompañada a esta demanda como documento [Nº], en cuyas fotografías se puede comprobar el mal estado del edificio y la dimensión de las obras autorizadas por la junta.

CUARTO.– Para acreditar los anteriores hechos, y al amparo de lo que dispone el artículo 732.2 de la LEC, se acompañan a esta demanda los documentos en que esta parte funda su derecho, relacionados en los hechos de este otrosí, en especial el informe pericial elaborado por el arquitecto D./Dña. [NOMBRE Y APELLIDOS], que concluye que la realización de las obras puede producir daños estructurales en el inmueble, dado su estado, y en la [vivienda/local] de mi representado, acompañado como documento n.º [Nº], y el acta notarial de fecha [FECHA], donde se constata el inicio de las obras, lo cual hace urgente la adopción de la medida cautelar interesada.

A los anteriores hechos son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

COMPETENCIA

Le corresponde al Tribunal al que me dirijo, ya que es aquel ante el que se ha presentado la demanda principal (art. 723.1 LEC).

LEGITIMACIÓN

Le corresponde a esta parte ante su condición de demandante en las presentes actuaciones (art. 721 LEC).

PROCEDIMIENTO

Es el previsto en el art. 733 LEC, solicitando que la medida se adopte sin audiencia de los demandados (art. 733.2 LEC), pues concurren en este caso razones de urgencia, ya que las obras han comenzado y, de continuar su ejecución mientras se tramita la audiencia, podrían producirse daños irreparables en la estructura del inmueble, con el perjuicio que ello ocasionaría a mi mandante.

SUSPENSIÓN DEL ACUERDO DE LA COMUNIDAD DE PROPIETARIOS

El artículo 18.4 de la Ley de Propiedad Horizontal establece el carácter ejecutivo de los acuerdos adoptados por la comunidad de propietarios, salvo que se acuerde su suspensión cautelar. Siendo necesario, para que proceda la suspensión cautelar de dichos acuerdos en vía judicial, en cuanto medida cautelar que es, que concurran los requisitos que establece el artículo 728 de la Ley de Enjuiciamiento Civil, la apariencia de buen derecho y el peligro por mora procesal, al establecer que «el solicitante de medidas cautelares también habrá de presentar los datos, argumentos y justificaciones documentales que conduzcan a fundar, por parte del tribunal, sin prejuzgar el fondo del asunto, un juicio provisional e indiciario favorable al fundamento de su pretensión. En defecto de justificación documental, el solicitante podrá ofrecerla por otros medios»; y, por otro lado, un peligro de mora procesal, al disponer que «sólo podrán acordarse medidas cautelares si quien las solicita justifica que, en el caso de que se trate, podrían producirse durante la pendencia del proceso, de no adoptarse las medidas solicitadas, situaciones que impidieren o dificultaren la efectividad de la tutela que pudiere otorgarse en una eventual sentencia estimatoria».

APARIENCIA DE BUEN DERECHO

De la documental aportada se desprende que se cumple el requisito del denominado «fumus boni iuris», acreditándose de forma inicial o indiciaria la realidad del derecho mediante la aportación de elementos probatorios ciertos que determinan la creencia racional sobre su certeza, sin que ello, no obstante, prejuzgue la cuestión de fondo del litigio, siendo suficientes los elementos aportados por mi representado para constituir a tales efectos un principio de prueba eficaz, puesto que el propio contenido del acuerdo pone de manifiesto que se adoptó sin respetar mínimamente el régimen de mayorías legalmente exigido y el informe pericial aportado determina la imposibilidad de su cumplimiento, por cuanto las obras pueden provocar daños estructurales al inmueble dado su actual estado.

PELIGRO DE MORA

Se deriva de que la ejecución material de las obras autorizadas en el acuerdo impugnado causará, de forma irreparable, graves daños a la estructura del inmueble, así como a la [vivienda/local] de mi representado, según resulta relatado en los hechos de este otrosí, ya que solamente con la medida cautelar solicitada se podrá garantizar la efectividad de una eventual sentencia favorable que se pudiere dictar en beneficio de mi mandante (art. 728.1 LEC).

MEDIDA INTERESADA

Es la suspensión cautelar del acuerdo comunitario de fecha [FECHA], con fundamento en el citado artículo 18 de la Ley de Propiedad Horizontal.

CAUCIÓN

Con fundamento en el art. 732.3 LEC se solicita que ésta sea fijada en [IMPORTE] euros, dadas las condiciones del caso, la situación de los demandados y los posibles perjuicios que se les pudieren generar por ello.

En base a lo anterior,

SUPLICO AL TRIBUNAL: Que tenga por formulada la solicitud de tutela cautelar que se recoge en este otrosí y, sin audiencia de los demandados, acuerde la suspensión cautelar del acuerdo de fecha [FECHA], punto [Nº] del orden del día, adoptado en la junta de la Comunidad de Propietarios de [DENOMINACIÓN O DOMICILIO DE LA COMUNIDAD]. De cara a la adopción de tal medida cautelar, se solicita asimismo que se tenga por ofrecida una caución de [IMPORTE] euros.
