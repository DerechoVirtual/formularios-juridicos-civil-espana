---
name: recurso-apelacion-falta-jurisdiccion-tribunales-civiles-civ-1355
description: "Recurso de apelación por falta de jurisdicción de los tribunales civiles. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Recurso de apelación por falta de jurisdicción de los tribunales civiles

> Formulario **CIV-1355** del plugin **Recursos civiles: reposición, apelación, casación y queja** (`formularios-recursos-civiles`) · Civil › Recursos · normativa revisada el 24-11-2026.

## Qué es

Escrito de interposición de recurso de apelación fundado en la falta de jurisdicción de los tribunales del orden civil (arts. 459 y 66.2 LEC), reproduciendo la declinatoria desestimada en primera instancia. El modelo recoge dos motivos alternativos o acumulables: el primero, por corresponder el asunto a otro orden jurisdiccional (ejemplo: responsabilidad patrimonial de la Administración, contencioso-administrativo); el segundo, por sumisión de la cuestión litigiosa a arbitraje (Ley de Arbitraje). En el encabezamiento se hacen constar los pronunciamientos que se impugnan.

Es un modelo de tipo **recursos**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Recurso de apelación por falta de jurisdicción de los tribunales civiles» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Recurso de apelación por falta de jurisdicción de los tribunales civiles” para mi caso». También puedes invocarla directamente con `/formularios-recursos-civiles:recurso-apelacion-falta-jurisdiccion-tribunales-civiles-civ-1355`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-recursos-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Recursos civiles: reposición, apelación, casación y queja) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (11 veces)
- [ ] Nº (7 veces)
- [ ] Nº DE PROCEDIMIENTO (3 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] Nº DE CLÁUSULA (2 veces)
- [ ] AÑO
- [ ] CLASE DE CONTRATO
- [ ] DENOMINACIÓN SOCIAL
- [ ] DÍA
- [ ] EXPONER OTROS MOTIVOS.
- [ ] EXPRESAR LA DENUNCIA DE LA INFRACCIÓN EN LA INSTANCIA.
- [ ] HACER CONSTAR LOS PRONUNCIAMIENTOS QUE SE IMPUGNAN
- [ ] IMPORTE
- [ ] INSTITUCIÓN ARBITRAL
- [ ] MES
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] NOMBRE Y APELLIDOS O DENOMINACIÓN SOCIAL DEL APELANTE
- [ ] PROVINCIA
- [ ] RAZONAR SOBRE LA INFRACCIÓN PROCESAL.
- [ ] RAZONAR SOBRE LOS EFECTOS PRETENDIDOS.

## Normas que cita el formulario

- art. 458 LEC
- art. 459 LEC
- art. 9 LOPJ
- art. 66.2 LEC
- art. 9.4 LOPJ
- art. 39 LEC

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

- Junto a «…, 5 y 9 de la Ley de Arbitraje, y especialmente el citado artículo 11 de la ley.»: el original reproducía aquí también el texto del antiguo art. 11 de la Ley 36/1988 (renuncia tácita al arbitraje por cualquier gestión procesal distinta de proponer la declinatoria); comprobar la redacción vigente del art. 11 de la Ley 60/2003, de Arbitraje, antes de citarlo.

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

PROCESO NÚMERO [Nº DE PROCEDIMIENTO]

A LA AUDIENCIA PROVINCIAL DE [PROVINCIA]

Don/Doña [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, en nombre y representación de Don/Doña [NOMBRE Y APELLIDOS O DENOMINACIÓN SOCIAL DEL APELANTE], parte codemandada en este proceso seguido con el número [Nº DE PROCEDIMIENTO], según tengo acreditado en autos, ante el Tribunal comparezco y como mejor proceda en Derecho, DIGO:

1) Que en fecha [FECHA] se dictó sentencia en este proceso, la cual fue notificada a esta parte en fecha [FECHA].

2) Que entendiendo que dicha sentencia no es ajustada a derecho, dicho sea con los debidos respetos y en términos de defensa, por medio del presente escrito interpongo contra la misma RECURSO DE APELACIÓN, [HACER CONSTAR LOS PRONUNCIAMIENTOS QUE SE IMPUGNAN] impugnando todos sus pronunciamientos, tanto el condenatorio de mi representado/a al pago de la indemnización, como los relativos a intereses y costas.

3) Que, de conformidad con lo dispuesto en el art. 458 de la LEC, fundo el recurso de apelación en las siguientes

ALEGACIONES:

[ELEGIR UNA DE ESTAS ALTERNATIVAS (O INCLUIR AMBAS) Y SUPRIMIR LO QUE NO PROCEDA:]

— Motivo de falta de jurisdicción por corresponder el asunto a otro orden jurisdiccional.

PRIMERO.- Al amparo del art. 459 de la LEC, por infracción de lo dispuesto en el art. 9 de la LOPJ y 36 de la LEC, al carecer de jurisdicción los órganos del orden civil para el conocimiento de este asunto.

Este proceso se siguió en demanda de responsabilidad patrimonial contra el Ayuntamiento de [LOCALIDAD] y contra mi representada, la aseguradora [DENOMINACIÓN SOCIAL], en razón al funcionamiento de los servicios públicos, al haber colisionado el vehículo del demandante contra una valla que señalizaba unas obras efectuadas por cuenta del Ayuntamiento codemandado. [EXPRESAR LA DENUNCIA DE LA INFRACCIÓN EN LA INSTANCIA.] Esta parte, al entender competentes a los órganos del orden contencioso-administrativo, planteó en tiempo y forma la declinatoria de jurisdicción, que fue desestimada por auto de fecha [FECHA] (folio [Nº]), deduciéndose contra el mismo recurso de reposición en fecha [FECHA] por esta representación (folio [Nº]), que fue desestimado por auto de fecha [FECHA] (folio [Nº]), por lo que nos vemos en la necesidad de razonar sobre la falta de estos presupuestos procesales en la apelación contra la sentencia definitiva, tal como prescribe el art. 66.2 de la LEC.

[RAZONAR SOBRE LA INFRACCIÓN PROCESAL.] La resolución judicial se dicta faltando el esencial presupuesto de la jurisdicción para el conocimiento del asunto, con infracción de lo dispuesto en el art. 9.4 de la LOPJ, en su redacción dada por Ley Orgánica 19/2003, de 23 de diciembre, que expresamente atribuye al orden contencioso-administrativo el conocimiento de las pretensiones que se deduzcan en relación con la responsabilidad patrimonial de las Administraciones Públicas, incluso cuando, como en este caso, el interesado haya accionado directamente contra la aseguradora de la Administración, junto a la Administración respectiva.

En las resoluciones de instancia no se tuvieron en cuenta estos argumentos, oportunamente alegados, aplicándose el criterio de la vis attractiva, improcedente ante la existencia de norma orgánica de atribución expresa al orden jurisdiccional contencioso-administrativo.

[RAZONAR SOBRE LOS EFECTOS PRETENDIDOS.] De acuerdo con lo anterior, debe declararse la falta de jurisdicción, remitiendo al demandante al orden competente, y con imposición de costas de primera instancia.

— Motivo de falta de jurisdicción por sumisión a arbitraje.

SEGUNDO.- Infracción de los artículos 9 y 11 de la Ley de Arbitraje en relación con el artículo 39 de la LEC.

Este proceso se siguió en reclamación de daños y perjuicios instada por la actora derivada de un presunto incumplimiento del contrato de [CLASE DE CONTRATO] de fecha [FECHA], suscrito entre la demandante y mi representado/a, que fue aportado como documento nº [Nº] de la demanda. Esta parte entendía que existía sumisión a arbitraje, por lo que planteó en tiempo y forma la declinatoria de jurisdicción, que fue desestimada por auto de fecha [FECHA] (folio [Nº]), deduciéndose contra el mismo recurso de reposición en fecha [FECHA] por esta representación (folio [Nº]), que fue desestimado por auto de fecha [FECHA] (folio [Nº]), por lo que nos vemos en la necesidad de razonar sobre la falta de estos presupuestos procesales en la apelación contra la sentencia definitiva, tal como prescribe el art. 66.2 de la LEC.

En efecto, tal como es de ver en la cláusula [Nº DE CLÁUSULA] del citado contrato de fecha [FECHA], objeto de este proceso, las partes sometieron las controversias que se derivaran del mismo a arbitraje, según se desprende del tenor literal de dicha cláusula, que es el siguiente: «Las partes intervinientes acuerdan que todo litigio, cuestión o reclamación resultantes de la ejecución o interpretación del presente contrato u operación relacionada con él, directa o indirectamente, se resolverá definitivamente mediante arbitraje de Derecho, por un único árbitro, en el marco de la Corte de Arbitraje de [INSTITUCIÓN ARBITRAL], a la que se encomienda la administración del arbitraje y la designación de los árbitros de acuerdo con su Reglamento y Estatutos, sin más excepciones o derogaciones que las contempladas en la presente cláusula arbitral».

Por tanto, existiendo un convenio arbitral válido según establece el artículo 9 de la Ley de Arbitraje y tratándose de materia susceptible de arbitraje, ambas partes vienen obligadas a cumplir lo estipulado, impidiendo a los tribunales conocer la controversia sometida a arbitraje, tal como imperativamente dispone el artículo 11 de la Ley de Arbitraje, lo cual nos obliga a formular la presente declinatoria de jurisdicción. En este sentido, es de aplicación el artículo 9 de la Ley de Arbitraje en cuanto a la forma y contenido del convenio arbitral y el artículo 11.1 de la misma ley en cuanto a la falta de jurisdicción de los tribunales ordinarios, cuando establece: «1. El convenio arbitral obliga a las partes a cumplir lo estipulado e impide a los tribunales conocer de las controversias sometidas a arbitraje, siempre que la parte a quien interese lo invoque mediante declinatoria».

Ante el hecho de constar la sumisión de la cuestión litigiosa a arbitraje según la cláusula [Nº DE CLÁUSULA] del contrato que antes se ha transcrito, el conocimiento de este litigio no corresponde a la jurisdicción civil, siendo el fundamento de ello los arts. 1, 4, 5 y 9 de la Ley de Arbitraje, y especialmente el citado artículo 11 de la ley.

En este punto, como reitera la jurisprudencia, el poder de disposición de las partes en orden a la exclusión de los órganos jurisdiccionales del Estado en las materias de derecho disponible es prácticamente total, pudiendo citarse la STC 136/2010, entre las más recientes, que trata la conexión de esa facultad con el derecho fundamental a la tutela judicial efectiva, de modo que el convenio arbitral es apto para expresar «la voluntad de las partes de someter a arbitraje todas o algunas de las controversias que hayan surgido o puedan surgir respecto de una determinada relación, contractual o no contractual», todo lo cual determina la falta de jurisdicción de los tribunales civiles, por lo que debe declararse la falta de jurisdicción, remitiendo al demandante a los órganos competentes, y con imposición de costas de primera instancia.

[OPCIONAL — si ha lugar] TERCERO.- [EXPONER OTROS MOTIVOS.]

Por lo expuesto,

SUPLICO A LA SALA que tenga por interpuesto recurso de apelación contra la sentencia de fecha [FECHA], dictada en el proceso número [Nº DE PROCEDIMIENTO], con justificante de traslado a la otra parte que acompaño, y, previos los trámites legales, con remisión de las actuaciones a la Audiencia Provincial, a quien SUPLICO que estime el recurso interpuesto, declarando la falta de jurisdicción y remitiendo a las partes al orden [ELEGIR: contencioso-administrativo / jurisdiccional que corresponda] [OPCIONAL — hacer constar la pretensión revocatoria si se exponen otros motivos]. Solicitamos la imposición al demandante de las costas de primera instancia.

OTROSÍ PRIMERO DIGO que, de conformidad con lo dispuesto en los apartados 3.b) y 6 de la disposición adicional decimoquinta de la LOPJ, acompaño a este escrito resguardo de consignación en la cuenta de Depósitos y Consignaciones abierta a nombre del Tribunal del depósito exigido para interponer el recurso, por importe de [IMPORTE] euros.

SUPLICO AL TRIBUNAL que tenga por hecha la anterior manifestación a los efectos pertinentes y por constituido el depósito, dejando interesada su devolución para el caso de estimación total o parcial del recurso.

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma de Procurador/a y Abogado/a.
