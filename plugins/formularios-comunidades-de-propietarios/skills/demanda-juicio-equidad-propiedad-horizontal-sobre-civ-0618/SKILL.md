---
name: demanda-juicio-equidad-propiedad-horizontal-sobre-civ-0618
description: "Demanda de juicio de equidad en propiedad horizontal sobre instalar contadores individuales de agua. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio de equidad en propiedad horizontal sobre instalar contadores individuales de agua

> Formulario **CIV-0618** del plugin **Comunidades de propietarios** (`formularios-comunidades-de-propietarios`) · Civil › Propiedad horizontal · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio de equidad en propiedad horizontal sobre instalar contadores individuales de agua» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio de equidad en propiedad horizontal sobre instalar contadores individuales de agua” para mi caso». También puedes invocarla directamente con `/formularios-comunidades-de-propietarios:demanda-juicio-equidad-propiedad-horizontal-sobre-civ-0618`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-comunidades-de-propietarios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Comunidades de propietarios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (6 veces)
- [ ] FECHA (4 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] AÑO
- [ ] DIRECCIÓN
- [ ] DÍA
- [ ] LUGAR
- [ ] MES
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] Nº
- [ ] Nº DE APARTADO
- [ ] SEDE

## Normas que cita el formulario

- art. 17 LPH
- art. 17.7 LPH
- art. 52.1.8.º LEC
- art. 85.1 LOPJ
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

D [NOMBRE Y APELLIDOS], Procurador de los Tribunales, actuando en representación de [NOMBRE DEL REPRESENTADO/A], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], por medio de la presente, al amparo de lo dispuesto en el artículo 17.7 de la Ley de Propiedad Horizontal, formulo demanda para que se resuelva en equidad en relación al acuerdo adoptado en el apartado [Nº DE APARTADO] de la Junta de Propietarios de fecha [FECHA], notificada a mi representado el día [FECHA], demanda que dirijo contra la Comunidad de Propietarios del edificio [DIRECCIÓN], con domicilio en [LOCALIDAD], y contra los propietarios contradictores D [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], D [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD] () en base a los siguientes

HECHOS

Mi mandante es titular de la vivienda sita en [LOCALIDAD], tal y como resulta de la escritura en virtud de la que la misma se adquirió y que se adjunta como documento n.º [NÚMERO] de esta demanda, vivienda integrada en la Comunidad de Propietarios demandada.

El pasado [FECHA] se celebró la Junta de la antes mencionada Comunidad en la que el punto del orden del día número [NÚMERO] debía resolverse sobre la instalación de contadores individuales de agua en cada una de las viviendas.

Dicha propuesta no fue aprobada en votación realizada en segunda convocatoria, al no alcanzarse las mayorías establecidas en el artículo 17 de la LPH.

Votaron en contra del citado acuerdo los propietarios expresados en el encabezamiento, en tanto que votaron a favor un 30% de los asistentes, entre los cuales se encuentra mi mandante, reflejándose su voto a favor en el acta al efecto levantada.

A efectos acreditativos del contenido del acuerdo y del resultado de la votación se adjunta como documento n.º [NÚMERO] copia del acta de tal Junta.

Por medio de la presente demanda se insta, al amparo de lo dispuesto en el artículo 17.7 de la LPH, que se resuelva en equidad al no haberse podido obtener la mayoría para la adopción del acuerdo.

En este caso, lo único pretendido es obtener autorización para individualizar el consumo de agua de cada vivienda mediante la instalación de contadores, lo cual no se realizó en su momento, pese a estar contemplado expresamente en los estatutos puesto que la cláusula 3 d) del título constitutivo establece que los servicios "pagarían los mismos de acuerdo con el consumo efectuado" (acompaño como documento número [Nº DE DOCUMENTO] copia del título constitutivo).

La más reciente jurisprudencia ha admitido la posibilidad de acudir al juicio de equidad en sustitución de la voluntad de la junta de propietarios, cuando la oposición suponga abuso de derecho por parte del propietario disconforme o ejercicio antisocial del mismo como sucede en el caso, en el que lo pretendido, individualización de los consumos de cada vivienda mediante la instalación de los correspondientes contadores, no supone perjuicio alguno para los propietarios que votaron en contra, que únicamente abonarán su propio consumo, y sí una mejora en el régimen de funcionamiento y convivencia que supone la propiedad horizontal, evitándose, de este modo, que se mantenga la situación abusiva y de privilegio que supone imponer a los copropietarios que no disfrutan del servicio el abono de los gastos de consumo de los que sí lo hacen (SSTS de 13 de marzo de 2003, rec. 2204/1997 y 19 de diciembre de 2008, rec. 389/2004, entre otras), y en este sentido mi representado se está viendo perjudicado notablemente puesto que sólo ocupa la vivienda en el periodo estival, como se acreditará en su día.

FUNDAMENTOS DE DERECHO

Competencia

Corresponde a los Tribunales de [LOCALIDAD], al ser el lugar en el que se encuentra la finca (art. 52.1.8.º LEC, en relación con lo dispuesto en el art. 85.1º LOPJ).

Legitimación

Le corresponde a esta parte la legitimación activa en su condición de propietario y al haber votado en contra del acuerdo impugnado, sin perjuicio de que al tratarse de un acuerdo ilegal, ni tan siquiera es necesario dicho requisito, en tanto que la legitimación pasiva corresponde a la Comunidad de Propietarios demandada y a los propietarios contradictores, que deben ser oídos, conforme a lo que dispone el artículo 17.7 de la LPH.

Procedimiento y cuantía

Debe seguirse el procedimiento previsto en el artículo 17.7 de la LPH, oyendo en comparecencia los contradictores previamente citados, y siendo la cuantía indeterminada.

Plazo

La demanda se deduce dentro del mes siguiente a la fecha de la segunda Junta.

Motivos de impugnación

Se insta que se resuelva en equidad sobre la cuestión planteada, supliendo la falta de un acuerdo de los que pueden adoptarse por mayoría, puesto que el objeto del acuerdo -la individualización de los consumos de cada vivienda mediante la instalación de los correspondientes contadores- es justo, no supone perjuicio alguno para los copropietarios, que únicamente abonarán su propio consumo, y constituye una mejora en el régimen de funcionamiento de la propiedad horizontal, evitándose, de este modo, que se mantenga la situación abusiva y de privilegio que supone imponer a los copropietarios que no disfrutan del servicio el abono de los gastos de consumo de los que sí lo hacen, como es el caso de mi representado, alegando en apoyo de esta interpretación las ya citadas SSTS 13 de marzo de 2003, rec. 2204/1997 y 19 de diciembre de 2008, rec. 389/2004.

En materia de costas el artículo 17.7 de la LPH en relación con el artículo 394 LEC, debiéndose imponer las costas a los demandados.

En base a lo anterior,

SUPLICO AL TRIBUNAL que tenga por presentada la presente demanda con los documentos a ella adjuntos y sus copias, en la representación que ostento, y se tenga por formulada demanda para que se resuelva en equidad el punto núm. [Nº] de la Junta de Propietarios de la Comunidad del edificio sito en [LOCALIDAD], celebrada el día [FECHA], y en su virtud, tras los trámites legales, se dicte sentencia por la que se apruebe el acuerdo de instalación individual de aparatos contadores, todo ello con condena en costas a los demandados.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

El Abogado El Procurador

========================================================================
