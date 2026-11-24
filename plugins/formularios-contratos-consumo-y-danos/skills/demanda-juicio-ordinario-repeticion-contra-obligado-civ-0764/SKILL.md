---
name: demanda-juicio-ordinario-repeticion-contra-obligado-civ-0764
description: "Demanda de juicio ordinario de repetición contra el obligado cuando pagó un tercero. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio ordinario de repetición contra el obligado cuando pagó un tercero

> Formulario **CIV-0764** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio ordinario de repetición contra el obligado cuando pagó un tercero» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio ordinario de repetición contra el obligado cuando pagó un tercero” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:demanda-juicio-ordinario-repeticion-contra-obligado-civ-0764`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (7 veces)
- [ ] DENOMINACIÓN SOCIAL (5 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] Nº DE DOCUMENTO (4 veces)
- [ ] FECHA (3 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] SEDE (2 veces)
- [ ] AÑO
- [ ] DÍA
- [ ] LUGAR
- [ ] MES

## Normas que cita el formulario

- art. 1158 Código Civil
- art. 1108 Código Civil
- art. 50 LEC
- art. 85.1 LOPJ
- art. 5 Ley Orgánica 1/2025
- art. 1100 Código Civil
- art. 394 LEC
- art. 251 LEC
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

D [NOMBRE Y APELLIDOS] Procurador de los Tribunales, actuando en representación de según se acredita mediante apoderamiento apud-acta otorgado ante el Letrado de la Administración de Justicia de [SEDE] que acompaño (o mediante copia electrónica del poder notarial de representación informática [o digitalizada] que se acompaña y se solicita sea devuelta una vez testimoniada), y bajo la dirección letrada de D [NOMBRE Y APELLIDOS], Abogado del Colegio de [LOCALIDAD], por medio de la presente formulo demanda de juicio ordinario en ejercicio de la acción de repetición por el pago realizado por mi representado por cuenta del demandado, demanda que dirijo contra D [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD] en base a los siguientes

PRIMERO HECHOS

Se ejercita la acción para que el demandado reembolse a mi representado la cantidad de [IMPORTE] euros que fueron abonados a la entidad acreedora [DENOMINACIÓN SOCIAL] por cuenta del mismo y en pago de una deuda contraída por el demandado derivada del contrato de fecha

El referido pago por cuenta del demandado trae causa del interés de mi representado en el cumplimiento de la deuda contraída por el demandado con la entidad acreedora [DENOMINACIÓN SOCIAL], puesto que previamente, en fecha [FECHA], habían concertado un contrato en virtud del cual el demandado D [NOMBRE Y APELLIDOS] se comprometía a entregar a mi representado los armarios y muebles que se describen en el contrato que sea acompaña como documento número [Nº DE DOCUMENTO], pactándose un precio de [IMPORTE] euros, el cual se abonó en su totalidad en el momento de la firma del contrato

En el curso de la ejecución del contrato, mi representado tuvo conocimiento que el demandado tenía dificultades económicas, habiéndole manifestado éste que la entidad acreedora [DENOMINACIÓN SOCIAL] no le suministraría más madera si no abonaba las facturas pendientes, por lo que en este caso no podría cumplir el encargo. Ante dicha situación, y ante la posibilidad cierta de que el demandado no cumpliera el contrato suscrito con mi representada, mi mandante se puso en contacto con la entidad acreedora, abonando la deuda pendiente, tal como se expone seguidamente.

Mi representado, tras entrevistarse con el gerente de la entidad acreedora, y ante la eventualidad cierta de que la empresa dejara de suministrarle el material, llegó a un acuerdo para liquidar las cantidades adeudadas por el demandado.

En efecto, mi representado pagó la cantidad de [IMPORTE] euros por cuenta del demandado D, que éste adeudaba a la entidad [DENOMINACIÓN SOCIAL] por los suministros de madera realizados en el periodo comprendido entre los meses de (se acompañan como documentos número [Nº DE DOCUMENTO] recibos de cobro del acreedor donde consta el concepto de pago por cuenta del demandado D).

En este caso, concurren los presupuestos que determinan la procedencia de la acción de repetición o reembolso, puesto que mi representado está amparado por el artículo 1158, párrafo segundo, del Código Civil, para reclamar al deudor el importe de lo satisfecho, habiendo reiterado el Tribunal Supremo, en Sentencias 15 de octubre de 1959, 30 de junio de 1966 y 5 de marzo de 2001, entre otras, que quien paga teniendo interés en el cumplimiento en la obligación, en beneficio del deudor, tiene derecho a reclamar la cantidad satisfecha.

En este caso, mi representado tenía interés en el cumplimiento de la obligación por cuanto que el pago de los suministros a la entidad [DENOMINACIÓN SOCIAL] incidía directamente en cumplimiento del contrato de fecha [FECHA], suscrito con la demandada, quien debía transformar la materia objeto de suministro para cumplir el contrato concertado con mi representada.

La acción de repetición que se ejercita confiere a mi representado todos los derechos que el acreedor tuviere contra el deudor, puesto que tenía un interés legítimo en el cumplimiento de la obligación, debiendo ser reembolsado de las cantidades satisfechas.

Una vez realizado el pago, mi representado se ha dirigido en numerosas ocasiones al deudor reclamando la deuda, remitiendo burofax en fecha [FECHA], que se acompaña como documento número [Nº DE DOCUMENTO], en el cual se le requería formalmente de pago, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial, habiendo hecho caso omiso el demandado.

Ello nos obliga a interponer esta acción en vía judicial, debiendo tomarse en consideración la conducta omisiva del demandado, en orden al devengo de intereses e imposición de costas, y debiendo indemnizarse a mi representado en la cantidad satisfecha por su cuenta que asciende a [IMPORTE] euros, con más los intereses legales conforme a lo establecido en el artículo 1108 del Código Civil.

FUNDAMENTOS DE DERECHO

Competencia

Corresponde la competencia objetiva y territorial al Tribunal al que me dirijo, con fundamento en el artículo 50 de la LEC, en relación con lo dispuesto en el art. 85.1º LOPJ.

Legitimación

Le corresponde a esta parte la legitimación activa al haber realizado el pago por cuenta del demandado, correspondiendo la legitimación pasiva a éste, quien está obligado a reintegrar el importe de lo satisfecho por su cuenta.

Procedimiento

Es el juicio ordinario con fundamento en el art. 249.2 dado el importe reclamado de [IMPORTE] euros que excede de los 15.000 € a partir de los que se deben seguir las reclamaciones por las normas del juicio ordinario.

Cumplimiento de los requisitos de procedibilidad

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

Requisitos de la acción de repetición o reembolso

Es de aplicación el artículo 1158 del Código Civil que dispone que "Puede hacer el pago cualquier persona, tenga o no interés en el cumplimiento de la obligación, ya lo conozca y lo apruebe, o ya lo ignore el deudor. El que pagare por cuenta de otro podrá reclamar del deudor lo que hubiese pagado, a no haberlo hecho contra su expresa voluntad. En este caso sólo podrá repetir del deudor aquello en que le hubiera sido útil el pago", habiendo interpretado, entre otras, la SSTS de 16 de diciembre de 1985 y 8 de mayo de 1992 que el art. 1158.2 se refiere a las personas que voluntariamente pagan deudas ajenas y el deudor a que se alude en el precepto es el real y verdadero, el obligado al pago, que el pago realizado por el tercero favorece, quedando sujeto a la obligación de reembolso.

Intereses

Son de aplicación los artículos 1100, 1101 y 1108 del Código Civil.

En materia de costas el artículo 394 LEC señala que las de primera instancia se imponen a la parte que vea en primera instancia rechazadas sus pretensiones.

En base a lo anterior,

SUPLICO AL TRIBUNAL que tenga por presentada la presente demanda con los documentos a ella adjuntos y sus copias, y tras la pertinente tramitación, se dicte por ese Tribunal sentencia en que se condene al demandado a indemnizar a mi representado en la cantidad de [IMPORTE] euros, con más los intereses legales correspondientes, con imposición de costas al demandado.

OTROSÍ PRIMERO DIGO.- Se fija la cuantía de este procedimiento en [IMPORTE] euros, de conformidad a lo que dispone el artículo 251 de la LEC.

OTROSÍ SEGUNDO DIGO.-Que estando la presente demanda sujeta al abono de la tasa por el ejercicio de la potestad jurisdiccional fijada por la Ley 10/2012, de 20 de noviembre, modificada por RDL 3/2013 y Ley 25/2015, de 28 julio, y desarrollada por Orden HAP/2662/2012, de 13 de diciembre, siendo mi representada personas jurídica no exenta de su pago, se acompaña a la presente demanda como documento nº [Nº DE DOCUMENTO] la correspondiente autoliquidación con el ejemplar para la Administración de Justicia debidamente validado y en el que consta el pago de la cantidad de 300 euros correspondiente a la cuota fija, sin que se incluya la cuota variable prevista en el artículo 7.2 de la Ley 10/2012 al haber sido declarado inconstitucional y nulo por la STC 140/2016, de 21 de julio.

En virtud de lo anterior,

SUPLICO AL TRIBUNAL que tenga por hecha la anterior manifestación a los efectos pertinentes y por acompañado el documento justificativo del abono de la tasa.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma Abogado	Firma Procurador

========================================================================
