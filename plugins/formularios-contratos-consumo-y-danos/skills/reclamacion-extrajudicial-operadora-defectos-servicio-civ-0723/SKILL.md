---
name: reclamacion-extrajudicial-operadora-defectos-servicio-civ-0723
description: "Reclamación extrajudicial a la operadora por defectos en el servicio de telefonía. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Reclamación extrajudicial a la operadora por defectos en el servicio de telefonía

> Formulario **CIV-0723** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Reclamación extrajudicial a la operadora por defectos en el servicio de telefonía» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Reclamación extrajudicial a la operadora por defectos en el servicio de telefonía” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:reclamacion-extrajudicial-operadora-defectos-servicio-civ-0723`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (4 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] Nº (2 veces)
- [ ] AÑO
- [ ] DENOMINACIÓN SOCIAL
- [ ] DIRECCIÓN
- [ ] DOMICILIO
- [ ] DÍA
- [ ] MES
- [ ] NIF
- [ ] Nº DE TELÉFONO
- [ ] ÓRGANO

## Normas que cita el formulario

- art. 15.2 Real Decreto 899/2009

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

Compañía telefónica [DENOMINACIÓN SOCIAL]

Servicio de atención al cliente [DIRECCIÓN]

Nombre del abonado/reclamante [ÓRGANO]

Número de abonado [Nº]

NIF [NIF]

Domicilio [DOMICILIO]

Reclamación

Muy Srs. Míos:

Me dirijo a Vds. con el objeto de presentar reclamación formal por los reiterados incumplimientos de los niveles mínimos o estándares de calidad en la prestación del servicio de telefonía fija (o móvil) que tengo concertado con su compañía (adjunto fotocopia del contrato o, en su caso, de una factura/recibo bancario a efectos probatorios).

El incumplimiento de los mencionados estándares o parámetros de calidad exigibles por el abonado o consumidor a la compañía prestadora de servicios de telefonía normativamente establecidos consisten:

— en el hecho de que en el período de tiempo comprendido entre el día [FECHA] y el día [FECHA] he sufrido [Nº] interrupciones de una duración variable en la conexión a la red telefónica [Nº DE TELÉFONO] (esto para el caso de telefonía fija)

— no dispongo de la cobertura a la que Vds. se han obligado contractualmente en la zona [LOCALIDAD], de conformidad con el mapa de cobertura que acompaña al contrato en el que se ha formalizado la obligación de prestación del servicios concertado/en el período de tiempo comprendido entre el día [FECHA] y el día [FECHA] (esto para el caso de telefonía móvil).

La interrupción temporal no ha sido motivada por ninguna de las causas siguientes, a las que se hace referencia en el artículo 15.2 del Real Decreto 899/2009, de 22 de mayo, por el que se aprueba la carta de derechos del usuario de los servicios de comunicaciones electrónicas (Boe del 30):

a) Incumplimiento grave por los abonados de las condiciones contractuales, en especial en caso de fraude o mora en el pago que dará lugar a la aplicación de la suspensión temporal e interrupción de los artículos 19 y 20, respectivamente. En todo caso, la suspensión temporal o interrupción afectará únicamente al servicio en el que se hubiera producido el fraude o mora en el pago.

b) Por los daños producidos en la red debido a la conexión por el abonado de equipos terminales que no hayan evaluado la conformidad, de acuerdo con la normativa vigente.

c) Incumplimiento del código de conducta por parte de un usuario que preste servicios de tarificación adicional, cuando la titularidad del contrato de abono corresponda a este último.

Efectivamente, el Real Decreto 899/2009, de 22 de mayo, por el que se aprueba la carta de derechos del usuario de los servicios de comunicaciones electrónicas (Boe del 30), en su artículo 3, establece los derechos de los usuarios finales de servicios de comunicaciones electrónicas, lo cuales serán titulares, además de los derechos establecidos en el artículo 8 del texto refundido de la Ley General para la Defensa de los Consumidores y Usuarios y otras leyes complementarias, aprobado por el Real Decreto Legislativo 1/2007, de 16 de noviembre, de los siguientes derechos, en las condiciones establecidas en este Real Decreto: (…)

e) Derecho a la continuidad del servicio, y a una indemnización en caso de interrupciones.

Y en el artículo 15 de ese Real Decreto se desarrolla el derecho a indemnización por la interrupción temporal del servicio telefónico disponible al público en los siguientes términos:

1. Cuando, durante un período de facturación, un abonado sufra interrupciones temporales del servicio telefónico disponible al público, el operador deberá indemnizar con una cantidad que será, al menos, igual a la mayor de las dos siguientes:

a) El promedio del importe facturado por todos los servicios interrumpidos durante los tres meses anteriores a la interrupción, prorrateado por el tiempo que haya durado la interrupción. En caso de una antigüedad inferior a tres meses, se considerará el importe de la factura media en las mensualidades completas efectuadas o la que se hubiese obtenido en una mensualidad estimada de forma proporcional al período de consumo efectivo realizado.

b) Cinco veces la cuota mensual de abono o equivalente vigente en el momento de la interrupción, prorrateado por el tiempo de duración de ésta.

El operador estará obligado a indemnizar automáticamente al abonado, en la factura correspondiente al período inmediato al considerado cuando la interrupción del servicio suponga el derecho a una indemnización por importe superior a 1 euro. En la factura correspondiente se hará constar la fecha, duración y cálculo de la cuantía de la indemnización que corresponde al abonado.

En el caso de abonados sujetos a modalidades prepago, el correspondiente ajuste en el saldo se realizará en un plazo no superior al del resto de abonados.

En interrupciones por causas de fuerza mayor, el operador se limitará a compensar automáticamente al abonado con la devolución del importe de la cuota de abono y otras independientes del tráfico, prorrateado por el tiempo que hubiera durado la interrupción.

El contrato de abono del servicio telefónico deberá recoger los términos y condiciones en que se dará cumplimiento a esta obligación.

La interrupción temporal no ha sido motivada por ninguna de las causas siguientes, a las que se hace referencia en el artículo 15.2 del Real Decreto 899/2009, de 22 de mayo, por el que se aprueba la carta de derechos del usuario de los servicios de comunicaciones electrónicas (Boe del 30):

a) Incumplimiento grave por los abonados de las condiciones contractuales, en especial en caso de fraude o mora en el pago que dará lugar a la aplicación de la suspensión temporal e interrupción de los artículos 19 y 20, respectivamente. En todo caso, la suspensión temporal o interrupción afectará únicamente al servicio en el que se hubiera producido el fraude o mora en el pago.

b) Por los daños producidos en la red debido a la conexión por el abonado de equipos terminales que no hayan evaluado la conformidad, de acuerdo con la normativa vigente.

c) Incumplimiento del código de conducta por parte de un usuario que preste servicios de tarificación adicional, cuando la titularidad del contrato de abono corresponda a este último.

Efectivamente, el Real Decreto 899/2009, de 22 de mayo, por el que se aprueba la carta de derechos del usuario de los servicios de comunicaciones electrónicas (Boe del 30), en su artículo 3, establece los derechos de los usuarios finales de servicios de comunicaciones electrónicas, lo cuales serán titulares, además de los derechos establecidos en el artículo 8 del texto refundido de la Ley General para la Defensa de los Consumidores y Usuarios y otras leyes complementarias, aprobado por el Real Decreto Legislativo 1/2007, de 16 de noviembre, de los siguientes derechos, en las condiciones establecidas en este Real Decreto: (…)

e) Derecho a la continuidad del servicio, y a una indemnización en caso de interrupciones.

Y en el artículo 15 de ese Real Decreto se desarrolla el derecho a indemnización por la interrupción temporal del servicio telefónico disponible al público en los siguientes términos:

1. Cuando, durante un período de facturación, un abonado sufra interrupciones temporales del servicio telefónico disponible al público, el operador deberá indemnizar con una cantidad que será, al menos, igual a la mayor de las dos siguientes:

a) El promedio del importe facturado por todos los servicios interrumpidos durante los tres meses anteriores a la interrupción, prorrateado por el tiempo que haya durado la interrupción. En caso de una antigüedad inferior a tres meses, se considerará el importe de la factura media en las mensualidades completas efectuadas o la que se hubiese obtenido en una mensualidad estimada de forma proporcional al período de consumo efectivo realizado.

b) Cinco veces la cuota mensual de abono o equivalente vigente en el momento de la interrupción, prorrateado por el tiempo de duración de ésta.

El operador estará obligado a indemnizar automáticamente al abonado, en la factura correspondiente al período inmediato al considerado cuando la interrupción del servicio suponga el derecho a una indemnización por importe superior a 1 euro. En la factura correspondiente se hará constar la fecha, duración y cálculo de la cuantía de la indemnización que corresponde al abonado.

En el caso de abonados sujetos a modalidades prepago, el correspondiente ajuste en el saldo se realizará en un plazo no superior al del resto de abonados.

En interrupciones por causas de fuerza mayor, el operador se limitará a compensar automáticamente al abonado con la devolución del importe de la cuota de abono y otras independientes del tráfico, prorrateado por el tiempo que hubiera durado la interrupción.

El contrato de abono del servicio telefónico deberá recoger los términos y condiciones en que se dará cumplimiento a esta obligación.

Por todo lo expuesto, SOLICITO:

adopten las medidas necesarias que pongan fin a los defectos en la prestación de los servicios de telefonía que les he contratado y procedan a indemnizarme automáticamente en la factura correspondiente al período inmediato al considerado con una cantidad que será, al menos, igual a la mayor de las dos anteriormente reproducidas.

En [LOCALIDAD], a [DÍA] de [MES] 20 [AÑO]

Fdo:
