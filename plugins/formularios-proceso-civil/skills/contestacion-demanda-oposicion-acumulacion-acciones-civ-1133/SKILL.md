---
name: contestacion-demanda-oposicion-acumulacion-acciones-civ-1133
description: "Contestación a la demanda con oposición a la acumulación de acciones planteada en la propia demanda. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contestación a la demanda con oposición a la acumulación de acciones planteada en la propia demanda

> Formulario **CIV-1133** del plugin **Proceso civil: demandas, contestaciones, prueba y vista** (`formularios-proceso-civil`) · Civil › Escritos procesales (demanda, contestación, prueba, vista) · normativa revisada el 24-11-2026.

## Qué es

Contestación a la demanda planteando oposición a la acumulación de acciones por tratarse de dos acciones, de responsabilidad extracontractual y de funcionamiento anormal de servicio público, cuyo enjuiciamiento corresponde a jurisdicciones diferentes, civil y contencioso-administrativa.

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contestación a la demanda con oposición a la acumulación de acciones planteada en la propia demanda» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contestación a la demanda con oposición a la acumulación de acciones planteada en la propia demanda” para mi caso». También puedes invocarla directamente con `/formularios-proceso-civil:contestacion-demanda-oposicion-acumulacion-acciones-civ-1133`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-proceso-civil:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Proceso civil: demandas, contestaciones, prueba y vista) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] CARRETERA NACIONAL
- [ ] FECHA
- [ ] FUNDAMENTOS
- [ ] HECHO QUE SE NIEGA
- [ ] IMPORTE
- [ ] IMPORTE EN CIFRA
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] NOMBRE DE LA PARTE
- [ ] NOMBRE DEL CUARTEL
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] PUNTO KILOMÉTRICO
- [ ] SEDE
- [ ] ÓRGANO O PERSONA

## Normas que cita el formulario

- art. 23 LEC
- art. 31 LEC
- art. 1.902 CC
- art. 394 LEC

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

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, en nombre y representación de [NOMBRE DEL REPRESENTADO/A], según acredito mediante escritura de poder inscrito en el Registro Electrónico de Apoderamientos Judiciales, a cuya justificación aporto certificación de dicho Registro como documento nº [Nº DE DOCUMENTO], dirigido por el Letrado abajo firmante D./Dña. [NOMBRE Y APELLIDOS], con despacho profesional en [LOCALIDAD], ante el Tribunal comparezco y como mejor proceda en Derecho DIGO:

Que mediante el presente escrito y dentro del término conferido, paso a contestar la demanda formulada de adverso, oponiéndome a la misma en base a los siguientes:

HECHOS

Esta parte niega los hechos alegados en la demanda, excepto los que expresamente se admitan en el presente escrito, y con carácter previo, se opone la indebida acumulación de acciones.

PRIMERO.- ACUMULACIÓN INDEBIDA DE ACCIONES

En la demanda formulada de contrario, se acumulan dos acciones cuyo enjuiciamiento corresponde a jurisdicciones diferentes. En efecto, la acción deducida contra D./Dña. [NOMBRE Y APELLIDOS] se basa en responsabilidad extracontractual y tiene su origen en los daños ocasionados al demandante, cuando a la salida de la curva existente en el punto kilométrico [PUNTO KILOMÉTRICO] de la carretera nacional [CARRETERA NACIONAL], tuvo que realizar una maniobra inesperada para salvar un camión estacionado irregularmente en el arcén, saliéndose fuera de la calzada y colisionando con la vivienda de su propiedad, causándole daños materiales tasados en [IMPORTE] euros ([IMPORTE EN CIFRA] €).

Asimismo, se dirige la demanda contra el Estado, por funcionamiento anormal de servicio público, puesto que se afirma que el vehículo conducido por D./Dña. [NOMBRE Y APELLIDOS] era militar y se hallaba aparcado dentro del recinto del cuartel de [NOMBRE DEL CUARTEL], sin la debida vigilancia, lo que motivó que el mencionado conductor se apropiara del vehículo y causara los daños.

Sin embargo, aunque ello fuera cierto, la indemnización por funcionamiento anormal de un servicio público corresponde enjuiciarla a la jurisdicción contencioso-administrativa y no a la civil, por lo cual, la condena solidaria que se solicita resulta inviable en esta jurisdicción.

SEGUNDO.- De conformidad con el hecho segundo de contrario.

TERCERO.- De conformidad con el hecho tercero de contrario.

CUARTO.- Se niega expresamente el correlativo de la demanda, en el sentido de que [HECHO QUE SE NIEGA], como se acredita con los documentos números [Nº DE DOCUMENTO] de la contestación a la demanda que se acompañan.

FUNDAMENTOS DE DERECHO

I, II, III, IV, V.-

Se admiten, a los meros efectos formales, los aducidos por la actora sobre jurisdicción, competencia, condición de parte procesal legítima y procedimiento aplicable, si bien, esta parte se opone a la acumulación de acciones formulada por la demandante.

VI.- POSTULACIÓN Y DEFENSA

La parte esta representada por el Procurador/a [NOMBRE Y APELLIDOS], legalmente habilitado según el art. 23 LEC y defendida por el Letrado que consta en el encabezamiento, art. 31 LEC.

VII.- FUNDAMENTO LEGAL DE LA OPOSICIÓN

A) ACUMULACIÓN INDEBIDA DE ACCIONES

Arts. 72 y 73.1 LEC.

Resulta improcedente la acumulación cuando se trate de acciones que nacen de diferente causa de pedir y dirigidas contra particulares y contra la Administración del Estado, fundada la primera en responsabilidad aquiliana, regulada en el art. 1.902 CCiv y la otra en funcionamiento anormal de un servicio público, por ser competente respecto a esta última la jurisdicción contencioso-administrativa, siendo inderogables las reglas de jurisdicción y competencia por razón de la materia.

B) En cuanto a la acción dirigida contra esta parte [NOMBRE DE LA PARTE] (se expresarán los razonamientos de la oposición) [FUNDAMENTOS]

VIII.- COSTAS

Las costas deberán serle impuestas, de conformidad con el art. 394 LEC, a la parte actora.

Por lo expuesto,

SUPLICO AL TRIBUNAL.

Que teniendo por presentado este escrito con los documentos y copias que le acompañan, lo admita y tenga por contestada en tiempo y forma la demanda y opuesto a la misma; y previos los trámites que corresponden, dicte en su día sentencia por la que se desestime la demanda presentada por [ÓRGANO O PERSONA], absolviendo de la misma a mi mandante, con expresa imposición de costas a la actora.

OTROSÍ DIGO. Que para su momento procesal oportuno solicito el recibimiento del pleito a prueba, a cuyos efectos designamos los archivos, protocolos y registros a que corresponden los documentos que hemos acompañado con la presente.

Es justicia debe hacerse en [LUGAR], a [FECHA].

Firma del Abogado	Firma del Procurador/a

========================================================================
