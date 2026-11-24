---
name: demanda-contra-aseguradora-cobrar-indemnizacion-civ-0771
description: "Demanda contra la aseguradora para cobrar la indemnización de un siniestro de responsabilidad civil. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda contra la aseguradora para cobrar la indemnización de un siniestro de responsabilidad civil

> Formulario **CIV-0771** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda contra la aseguradora para cobrar la indemnización de un siniestro de responsabilidad civil» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda contra la aseguradora para cobrar la indemnización de un siniestro de responsabilidad civil” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:demanda-contra-aseguradora-cobrar-indemnizacion-civ-0771`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] ASEGURADORA (4 veces)
- [ ] IMPORTE (4 veces)
- [ ] FECHA (3 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] AÑO
- [ ] CAUSA
- [ ] DESCRIBIR
- [ ] DESCRIPCIÓN DE LOS DAÑOS
- [ ] DÍA
- [ ] LUGAR
- [ ] MES
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] Nº
- [ ] Nº DE CLÁUSULA
- [ ] SEDE

## Normas que cita el formulario

- art. 52.2 LEC
- art. 249.2 LEC
- art. 5 Ley Orgánica 1/2025
- art. 394 LEC
- art. 7.2 Ley 10/2012

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…curador ========================================================================»: requisito de procedibilidad del art. 5 LO 1/2025 — antes de presentar la demanda hay que intentar un medio adecuado de solución de controversias (MASC) y acreditarlo con la demanda (arts. 264.4.º y 399.3 LEC), salvo las materias excluidas del art. 5.2. Fuente: LO 1/2025, arts. 5 a 7 (BOE-A-2025-76).

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

D [NOMBRE Y APELLIDOS] Procurador de los Tribunales, actuando en representación de [NOMBRE DEL REPRESENTADO/A] según se acredita mediante apoderamiento apud-acta otorgado ante el Letrado de la Administración de Justicia de [LOCALIDAD] que acompaño (o mediante copia electrónica del poder notarial de representación informática [o digitalizada] que se acompaña y se solicita sea devuelta una vez testimoniada) por medio de la presente formulo demanda de juicio ordinario en ejercicio de acción de reclamación de cantidad por importe de [IMPORTE] euros contra la aseguradora [ASEGURADORA], con domicilio en [LOCALIDAD] en base a los siguientes

HECHOS

Que el pasado día [FECHA] mi representado sufrió un siniestro consistente en [DESCRIBIR] cuyo riesgo estaba cubierto por un seguro de responsabilidad civil en virtud de un contrato de seguro que tiene mi mandante suscrito con la aseguradora demandada [ASEGURADORA] y estando al corriente del pago de las primas al tiempo de ocurrir los hechos, cuya póliza y recibos acompaño como documentos número

El siniestro se produjo a las [Nº] horas del día [FECHA] como consecuencia de [CAUSA], causando daños cuya descripción es la siguiente [DESCRIPCIÓN DE LOS DAÑOS]

Los daños y perjuicios sufridos ascienden a la cantidad de [IMPORTE] euros según dictamen realizado por el perito D [NOMBRE Y APELLIDOS] que se acompaña como documento número [Nº DE DOCUMENTO] de la demanda.

Una vez acaecido el siniestro mi representado comunicó en tiempo y forma los daños sufridos y una estimación de los mismos a la compañía aseguradora y al no llegar a un acuerdo con la misma designaron los correspondientes peritos para que procedieran a elaborar un informe de valoración de los daños para proceder a la liquidación del siniestro.

En base a dicho informe se ha dirigido a la entidad aseguradora reclamación extrajudicialmente de la cantidad tasada cuyo escrito se acompaña como documento número [Nº DE DOCUMENTO] y al no ser atendido dicho requerimiento se procede a ejercitar acción judicial de reclamación contra la aseguradora solicitando indemnización por un siniestro en seguro de responsabilidad civil.

FUNDAMENTOS DE DERECHO

Competencia

El órgano judicial competente para el conocimiento de las acciones derivadas del contrato de seguro es el Tribunal de Instancia del domicilio del asegurado art. 52.2º LEC.

Legitimación

La legitimación activa le corresponde a esta parte en su condición de asegurado y la legitimación pasiva a la Compañía de Seguros [ASEGURADORA] en su condición de aseguradora.

Procedimiento

Es el juicio ordinario con fundamento en el artículo 249.2 LEC dado el importe del coste en concepto de daños y perjuicios.

Plazo

La acción que se deriva del contrato de seguro de daños se ejercita antes de que transcurran dos años desde que se produjo el siniestro, conforme a lo establecido en el artículo 25 de la Ley de Contrato de Seguro.

Cumplimiento de los requisitos de procedibilidad.

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

Fondo de la reclamación

La acción de reclamación solicitando la indemnización se hace en base a la Ley 50/1980, de 8 de octubre, de contrato de seguros, estableciendo el artículo 8 que " el asegurador está obligado a satisfacer la indemnización al término de las investigaciones y peritaciones necesarias para establecer la existencia del siniestro y, en su caso, el importe de los daños que resulten del mismo. En cualquier supuesto, el asegurador deberá efectuar, dentro de los cuarenta días a partir de la recepción de la declaración del siniestro, el pago del importe mínimo de lo que el asegurador pueda deber, según las circunstancias por el conocidas".

Asimismo, son de aplicación los artículos 23 y siguientes en relación al seguro de daños y la cláusula [Nº DE CLÁUSULA] del contrato de fecha [FECHA] en cuanto a la cobertura del riesgo.

Intereses por mora del asegurador

Es de aplicación el artículo 20 de la Ley de Contrato de Seguro, cuyo apartado 3 establece que "se entenderá que el asegurador incurre en mora cuando no hubiere cumplido su prestación en el plazo de tres meses desde la producción del siniestro o no hubiere procedido al pago del importe mínimo de lo que pueda deber dentro de los cuarenta días a partir de la recepción de la declaración del siniestro", debiendo imponerse el interés prevenido en el apartado 4 del mismo artículo cuando dispone que ."la indemnización por mora se impondrá de oficio por el órgano judicial y consistirá en el pago de un interés anual igual al del interés legal del dinero vigente en el momento en que se devengue, incrementado en el 50 %; estos intereses se considerarán producidos por días, sin necesidad de reclamación judicial. No obstante, transcurridos dos años desde la producción del siniestro, el interés anual no podrá ser inferior al 20 %".

En materia de costas el artículo 394 LEC señala que las de primera instancia se imponen a la parte que vea en primera instancia rechazadas sus pretensiones.

En base a lo anterior,

SUPLICO AL TRIBUNAL que tenga por presentada la presente demanda con los documentos a ella adjuntos y sus copias, y por parte en la representación que ostento y tras la pertinente tramitación se dicte por ese Tribunal sentencia en la que se condene a la aseguradora [ASEGURADORA] a indemnizar a mi principal la cantidad de [IMPORTE] euros, con más el interés de mora desde la fecha del siniestro, e imponiendo a la citada demandada el pago de las costas procesales.

OTROSÍ PRIMERO DIGO.-Se fija la cuantía del presente procedimiento en [IMPORTE] euros, importe reclamado en estas actuaciones.

En base a lo anterior,

OTROSÍ SEGUNDO DIGO.-Que estando la presente demanda sujeta al abono de la tasa por el ejercicio de la potestad jurisdiccional fijada por la Ley 10/2012, de 20 de noviembre, modificada por RDL 3/2013 y Ley 25/2015, de 28 julio, y desarrollada por Orden HAP/2662/2012, de 13 de diciembre, siendo mi representada personas jurídica no exenta de su pago, se acompaña a la presente demanda como documento nº [Nº DE DOCUMENTO] la correspondiente autoliquidación con el ejemplar para la Administración de Justicia debidamente validado y en el que consta el pago de la cantidad de 300 euros correspondiente a la cuota fija, sin que se incluya la cuota variable prevista en el artículo 7.2 de la Ley 10/2012 al haber sido declarado inconstitucional y nulo por la STC 140/2016, de 21 de julio.

En base a lo anterior,

SUPLICO AL TRIBUNAL que tenga por hecha la anterior manifestación a los efectos pertinentes y por acompañado el documento justificativo del abono de la tasa.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma Abogado Firma Procurador

========================================================================
