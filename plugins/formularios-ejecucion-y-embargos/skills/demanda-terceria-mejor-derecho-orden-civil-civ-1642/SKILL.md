---
name: demanda-terceria-mejor-derecho-orden-civil-civ-1642
description: "Demanda de tercería de mejor derecho en el orden civil. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de tercería de mejor derecho en el orden civil

> Formulario **CIV-1642** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Demanda de tercería de mejor derecho interpuesta en un procedimiento de ejecución, al ostentar un tercero un crédito contra el ejecutado, teniendo preferencia su derecho frente al acreedor ejecutante.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de tercería de mejor derecho en el orden civil» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de tercería de mejor derecho en el orden civil” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:demanda-terceria-mejor-derecho-orden-civil-civ-1642`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] PARTE DEMANDADA (5 veces)
- [ ] IMPORTE (4 veces)
- [ ] IMPORTE EN CIFRA (4 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] FECHA (2 veces)
- [ ] NOMBRE DEL SOLICITANTE (2 veces)
- [ ] Nº DE PROCEDIMIENTO (2 veces)
- [ ] CAUSA
- [ ] DESCRIPCIÓN DEL BIEN
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] Nº
- [ ] NÚMERO
- [ ] SEDE

## Normas que cita el formulario

- art. 599 LEC
- art. 85.1 LOPJ
- art. 614 LEC
- art. 615 LEC
- art. 437.1 LEC
- art. 5 Ley Orgánica 1/2025
- art. 620 LEC

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

D./Dña. [NOMBRE Y APELLIDOS] Procurador/a de los Tribunales, actuando en nombre y representación de [NOMBRE DEL REPRESENTADO/A], con domicilio en [LOCALIDAD] y D.N. I. número [NÚMERO], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], ante el Tribunal comparezco en los autos de procedimiento de ejecución número [Nº DE PROCEDIMIENTO], seguidos a instancia de [NOMBRE DEL SOLICITANTE] contra [PARTE DEMANDADA], y como mejor proceda en derecho DIGO:

Que siguiendo instrucciones de mi mandante formulo DEMANDA DE TERCERÍA DE MEJOR DERECHO frente a [PARTE DEMANDADA], parte ejecutante en el procedimiento de ejecución antes referido en el que interviene representada por el Procurador [NOMBRE Y APELLIDOS], y frente a [PARTE DEMANDADA], ejecutado en dicho procedimiento, demanda que se funda en los siguientes

HECHOS

PRIMERO.- El pasado día [FECHA] se dictó auto despachando ejecución a instancia de [NOMBRE DEL SOLICITANTE] contra [PARTE DEMANDADA] en reclamación de la cantidad de [IMPORTE] euros ([IMPORTE EN CIFRA] €) en concepto de principal, [IMPORTE] euros ([IMPORTE EN CIFRA] €) en concepto de intereses devengados hasta la fecha, más otros [IMPORTE] euros ([IMPORTE EN CIFRA] €) presupuestados provisionalmente para los intereses que puedan generarse durante la ejecución y las costas de ésta.

SEGUNDO.- Como consecuencia de la ejecución despachada se dictó decreto en el cual se embargaron los siguientes bienes propiedad del ejecutado [DESCRIPCIÓN DEL BIEN]

TERCERO.- Por el ejecutante se ha instado la realización de los bienes embargados al ejecutado, a fin de satisfacer el importe de las cantidades reclamadas con el producto obtenido por dicha realización.

CUARTO.- Mi representado ostenta a su favor un crédito contra el ejecutado que asciende a la cantidad de [IMPORTE] euros ([IMPORTE EN CIFRA] €) como consecuencia de [CAUSA] Se acompaña como documento número [Nº DE DOCUMENTO] el contrato del que resulta el crédito favorable a mi cliente.

De lo anterior se deduce que mi mandante ostenta el derecho a que su crédito sea satisfecho con preferencia al del acreedor ejecutante, por lo que se ve en la necesidad de interponer la presente demanda de tercería de mejor derecho.

QUINTO.- Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento nº [Nº DE DOCUMENTO]

A los anteriores hechos son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

I.- COMPETENCIA Y PROCEDIMIENTO.-

Aunque la Ley Procesal no diga nada al respecto, se entiende que, conforme a lo dispuesto en el artículo 599 de la LEC en relación con lo dispuesto en el art. 85.1º LOPJ, la tercería de mejor derecho habrá de interponerse ante el tribunal que conozca de la ejecución y se sustanciará por los cauces del juicio verbal (artículo 617.1).

II.- LEGITIMACION ACTIVA.-

Quien afirme que le corresponde un derecho a que su crédito sea satisfecho con preferencia al acreedor ejecutante tendrá legitimación activa para interponer demanda de tercería de mejor derecho, tal y como estipula el artículo 614 de la LEC. En esta situación se encuentra mi patrocinado por lo que se ve en la tesitura de promover esta demanda.

LEGITIMACION PASIVA.-

Según el artículo 617, la tercería de mejor derecho se sustanciará por los trámites del juicio verbal y se dirigirá siempre frente al acreedor ejecutante. El ejecutado podrá intervenir en el procedimiento de tercería con plenitud de derechos procesales y habrá de ser demandado cuando el crédito cuya preferencia alegue el tercerista no conste en un título ejecutivo, tal y como ocurre en el presente caso en el que se ha demandado tanto al acreedor ejecutante como al deudor ejecutado.

Por otro lado, como mi patrocinado no dispone de título ejecutivo en que conste su crédito, no podrá intervenir en la ejecución hasta que, en su caso, se estime la demanda (artículo 616.2).

III.- REQUISITOS FORMALES.-

Según advierte el artículo 614 de la LEC, no se admitirá demanda de tercería de mejor derecho si no se acompaña un principio de prueba del crédito que se afirma preferente. Y, en ningún caso, se permitirá segunda tercería de mejor derecho, que se funde en títulos o derechos que poseyera el que la interponga al tiempo de formular la primera.

Como se dijo en la exposición fáctica de esta demanda se acompaña como documento número 1 el contrato del que dimana el crédito a favor de mi representado.

IV.- REQUISITOS TEMPORALES.-

La tercería de mejor derecho procederá desde que se haya embargado el bien a que se refiera la preferencia, si esta fuere especial o desde que se despachare ejecución, si fuere general.

No se admitirá demanda de tercería de mejor derecho después de haberse entregado al ejecutante la suma obtenida mediante la ejecución forzosa o, en caso de adjudicación de los bienes embargados al ejecutante, después de que éste adquiera la titularidad de dichos bienes conforme a lo dispuesto en la legislación civil (artículo 615 de la LEC).

La demanda se formula en momento procesal hábil ya que no se ha realizado pago alguno al acreedor ejecutante.

V.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.-

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 en relación con el art. 437.1 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

VI.- ASPECTOS SUSTANTIVOS.-

La sentencia que se dicte en la tercería de mejor derecho resolverá sobre la existencia del privilegio y el orden en que los créditos deben ser satisfechos en la ejecución en que aquella sentencia recaiga, pero sin prejuzgar otras acciones que a cada uno pudiera corresponder, especialmente las de enriquecimiento (artículo 620.1).

La preferencia que afirma ostentar mi poderdante se fundamenta en los siguientes preceptos en materia de prelación de créditos:

VII.- COSTAS.-

deberán ser impuestas a los demandados en caso de que formulen oposición, de conformidad con lo dispuesto en el artículo 620 de la LEC.

En virtud de cuanto se ha expuesto,

SUPLICO AL TRIBUNAL:

que teniendo por presentado este escrito con los documentos que en él se mencionan, se me tenga por comparecido y parte en nombre de mi representado, entendiéndose conmigo las sucesivas actuaciones, y por formulada demanda de tercería de mejor derecho contra [PARTE DEMANDADA] y [NOMBRE Y APELLIDOS], ejecutante y ejecutado respectivamente en los autos de ejecución número [Nº DE PROCEDIMIENTO] seguidos ante este mismo Tribunal, que se tramitará en pieza separada por los cauces del juicio verbal, para que, tras los trámites procesales oportunos, se dicte auto en el que se declare la existencia de un privilegio a favor de mi patrocinado, que deberá ver satisfecho su crédito con preferencia al del ejecutante, debiéndose entregar a mi cliente, hasta cubrir el importe de su reclamación, las cantidades procedentes de la ejecución, una vez se hayan satisfecho al ejecutante las tres quintas partes de las costas causadas en ésta hasta el momento en que recaiga aquel auto, todo ello con expresa imposición de las costas a los demandados.

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a

========================================================================
