---
name: demanda-separacion-divorcio-modifica-medidas-dictadas-civ-0135
description: "Demanda de separación o divorcio que modifica las medidas dictadas por Violencia sobre la Mujer. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de separación o divorcio que modifica las medidas dictadas por Violencia sobre la Mujer

> Formulario **CIV-0135** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Demanda de separación o divorcio presentada por la víctima ante la Sección de Violencia sobre la Mujer del Tribunal de Instancia que ya dictó una orden de protección, en la que se pide modificar las medidas civiles acordadas en ella (art. 544 ter LECrim) y se proponen las medidas provisionales y definitivas.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de separación o divorcio que modifica las medidas dictadas por Violencia sobre la Mujer» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de separación o divorcio que modifica las medidas dictadas por Violencia sobre la Mujer” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-separacion-divorcio-modifica-medidas-dictadas-civ-0135`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] AÑO (6 veces)
- [ ] DÍA (6 veces)
- [ ] MES (6 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] DETALLE Y JUSTIFICACIÓN DE SU PROCEDENCIA (4 veces)
- [ ] DOMICILIO (3 veces)
- [ ] SEDE (3 veces)
- [ ] NOMBRE Y APELLIDOS DE LA DEMANDANTE (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL DEMANDADO (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL HIJO/A (2 veces)
- [ ] COLEGIO DE ABOGADOS
- [ ] DETALLE DE LOS HECHOS
- [ ] DETALLE DE TODAS LAS MEDIDAS QUE SE SOLICITAN CON CARÁCTER DEFINITIVO
- [ ] NOMBRE Y APELLIDOS DEL LETRADO
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] Nº
- [ ] Nº DE DOCUMENTO
- [ ] PROFESIÓN
- [ ] RELACIÓN DE DOCUMENTOS

## Normas que cita el formulario

- art. 81 Código Civil
- art. 86 Código Civil
- art. 91 Código Civil
- art. 158 Código Civil

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

### Avisos de actualización (3) — se aplican en el texto, nunca se copian en el documento

- Junto a «…isionales previas, al amparo del artículo 772 de la Ley de Enjuiciamiento Civil.»: comprobar el reparto competencial vigente entre las Secciones de Violencia sobre la Mujer y las Secciones de Familia, Infancia y Capacidad conforme a la LO 1/2025 y a la normativa de violencia de género aplicable en la sede de que se trate.
- Junto a «…os procesos derivados de crisis familiares en casos de violencia sobre la mujer.»: comprobar la cita del art. 89.9 LOPJ y el art. 5.2 de la LO 1/2025 en la redacción vigente, por si ha variado la numeración.
- Junto a «…s o dejadas sin efecto por el Juez de primera instancia que resulte competente."»: el texto transcrito del art. 544 ter.7 LECrim y la terminología («capacidad judicialmente modificada», «Juez de primera instancia») deben contrastarse con la redacción vigente tras la Ley 8/2021 y la LO 1/2025.

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

A LA SECCIÓN DE VIOLENCIA SOBRE LA MUJER DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

D./Dª [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, en nombre y representación de Dª [NOMBRE Y APELLIDOS DE LA DEMANDANTE], mayor de edad, de profesión [PROFESIÓN], con domicilio en [DOMICILIO], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], comparezco ante este Tribunal con la asistencia del Letrado D./Dª [NOMBRE Y APELLIDOS DEL LETRADO], del Ilustre Colegio de Abogados de [COLEGIO DE ABOGADOS], y DIGO:

Que por medio del presente escrito y en la representación que ostento, interpongo, conforme al [ELEGIR: art. 81 del Código Civil, si se trata de separación / art. 86 del Código Civil, si se trata de divorcio], demanda de [ELEGIR: SEPARACIÓN / DIVORCIO] contra D./Dª [NOMBRE Y APELLIDOS DEL DEMANDADO], mayor de edad, con domicilio en [DOMICILIO], cónyuge de mi representada, en la que, entre otros extremos, solicitaremos la MODIFICACIÓN DE LAS MEDIDAS CIVILES adoptadas en auto de fecha [DÍA] de [MES] de [AÑO], dictado por este Tribunal conforme a lo dispuesto en el art. 544 ter de la Ley de Enjuiciamiento Criminal, por el que se dictó orden de protección para mi representada como víctima de violencia de género, testimonio del cual se acompaña como DOCUMENTO Nº 1.

La presente demanda se basa en los siguientes

HECHOS

PRIMERO.- Mi representada y su esposo contrajeron matrimonio en forma [ELEGIR: civil / canónica] en [LOCALIDAD], con fecha [DÍA] de [MES] de [AÑO], debidamente inscrito en el Registro Civil de [LOCALIDAD], [DATOS REGISTRALES: Sección, Tomo, Página]. Se acompaña, como DOCUMENTO Nº 2, certificación literal de la inscripción de matrimonio expedida por el Registro Civil.

SEGUNDO.- De dicha unión matrimonial ha nacido y vive un hijo/a, llamado/a [NOMBRE Y APELLIDOS DEL HIJO/A], nacido/a en [LOCALIDAD] el [DÍA] de [MES] de [AÑO], constando el nacimiento inscrito en el Registro Civil de [LOCALIDAD], [DATOS REGISTRALES: Sección, Tomo, Página]. Se acompaña, como DOCUMENTO Nº 3, certificación literal de la inscripción de nacimiento expedida por el Registro Civil.

TERCERO.- El domicilio conyugal, según se acredita con el certificado de empadronamiento que se acompaña como DOCUMENTO Nº 4, ha estado situado en [DOMICILIO].

CUARTO.- El régimen económico del matrimonio es el legal de [RÉGIMEN ECONÓMICO MATRIMONIAL: p. ej., sociedad de gananciales].

QUINTO.- [OPCIONAL — incluir si procede: si no han transcurrido tres meses desde la celebración del matrimonio] Habiendo transcurrido menos de tres meses desde la celebración del matrimonio, mi representada ha sufrido los siguientes episodios de violencia que ponen en riesgo su integridad física y emocional y su libertad, así como la de su hijo/a antes citado/a: [DETALLE DE LOS HECHOS].

SEXTO.- Dichos actos de violencia de género dieron lugar a que, por Auto de fecha [DÍA] de [MES] de [AÑO], la Sección de Violencia sobre la Mujer del Tribunal de Instancia de [SEDE], conforme a lo dispuesto en el art. 544 ter de la Ley de Enjuiciamiento Criminal, dictara orden de protección para mi representada como víctima de violencia de género. Como ya se ha dicho, se acompaña testimonio del citado Auto como DOCUMENTO Nº 1.

[OPCIONAL — incluir si procede: si no han transcurrido tres meses desde la celebración del matrimonio]

De ahí que se interponga la presente demanda sin haber transcurrido aún tres meses desde que se celebró el matrimonio, tal y como permite el art. 81 del Código Civil.

SÉPTIMO.- En el referido Auto se acordaron las medidas civiles que constan en el mismo. Dichas medidas no resultan las más convenientes para regir los efectos de la separación/divorcio que ahora se solicita, por lo que se pide su sustitución por las que a continuación se detallan para que rijan mientras se sustancia el procedimiento: [DETALLE DE LAS MEDIDAS PROVISIONALES A ADOPTAR, ESPECIFICANDO LAS QUE DEBEN RATIFICARSE Y LAS QUE HAN DE MODIFICARSE].

OCTAVO.- Se proponen las siguientes medidas definitivas destinadas a regular la situación tras la sentencia firme de separación/divorcio:

a) En cuanto a las medidas personales respecto del hijo/a común, [NOMBRE Y APELLIDOS DEL HIJO/A], se proponen las siguientes: [DETALLE Y JUSTIFICACIÓN DE SU PROCEDENCIA].

b) En cuanto al uso de la vivienda y ajuar familiares, se proponen las siguientes: [DETALLE Y JUSTIFICACIÓN DE SU PROCEDENCIA].

c) En cuanto a los alimentos para el hijo/a común y la contribución a las cargas del matrimonio, se proponen las siguientes: [DETALLE Y JUSTIFICACIÓN DE SU PROCEDENCIA].

d) En cuanto a la compensación económica por desequilibrio, se propone la siguiente: [DETALLE Y JUSTIFICACIÓN DE SU PROCEDENCIA].

Se acompañan los DOCUMENTOS que corresponda: [RELACIÓN DE DOCUMENTOS].

Resultan aplicables a los citados hechos los siguientes

FUNDAMENTOS DE DERECHO

COMPETENCIA.- Es competente la Sección de Violencia sobre la Mujer del Tribunal de Instancia de [SEDE] a la que se dirige la presente demanda, por ser aquella en la que se tramitaron las medidas provisionales previas, al amparo del artículo 772 de la Ley de Enjuiciamiento Civil.

PROCEDIMIENTO.- La presente demanda debe sustanciarse por los trámites del juicio verbal, en virtud de lo dispuesto en el artículo 753 de la Ley de Enjuiciamiento Civil, con las peculiaridades del artículo 770 de la misma Ley.

CAPACIDAD.- Ambas partes tienen capacidad para ser parte, conforme a lo dispuesto en los artículos 6 y siguientes de la Ley de Enjuiciamiento Civil.

LEGITIMACIÓN.- Están legitimados activa y pasivamente la demandante y el demandado, como cónyuges cuya separación/divorcio se solicita, conforme a los arts. 81 (u 86, si se trata de divorcio) del Código Civil y al art. 10 de la Ley de Enjuiciamiento Civil.

REPRESENTACIÓN Y DEFENSA.- La demandante comparece representada y defendida, respectivamente, por el Procurador y el Letrado que constan en el encabezamiento de este escrito, de acuerdo con lo dispuesto en los artículos 23.1 y 31.1 de la Ley de Enjuiciamiento Civil.

CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.- La presente demanda no está sujeta al previo intento de resolución de controversias en vía no jurisdiccional, por cuanto el art. 89.9 de la Ley Orgánica del Poder Judicial excluye de los medios adecuados de solución de controversias los procesos derivados de crisis familiares en casos de violencia sobre la mujer.

DERECHO SUSTANTIVO.- Art. 81 del Código Civil, según el cual: "Se decretará judicialmente la separación, cualquiera que sea la forma de celebración del matrimonio:

1. A petición de ambos cónyuges o de uno con el consentimiento del otro, una vez transcurridos tres meses desde la celebración del matrimonio. A la demanda se acompañará una propuesta de convenio regulador redactada conforme al artículo 90 de este Código.

2. A petición de uno solo de los cónyuges, una vez transcurridos tres meses desde la celebración del matrimonio. No será preciso el transcurso de este plazo para la interposición de la demanda cuando se acredite la existencia de un riesgo para la vida, la integridad física, la libertad, la integridad moral o libertad e indemnidad sexual del cónyuge demandante o de los hijos de ambos o de cualquiera de los miembros del matrimonio.

A la demanda se acompañará propuesta fundada de las medidas que hayan de regular los efectos derivados de la separación."

(O, en el caso de solicitarse el divorcio, el art. 86 del Código Civil.)

En relación con las medidas definitivas cuya adopción se solicita, debe atenderse al art. 91 del Código Civil y al art. 774 de la Ley de Enjuiciamiento Civil.

En relación con las medidas provisionales adoptadas en el Auto por el que se dictó orden de protección de mi representada, el art. 544 ter.7 de la Ley de Enjuiciamiento Criminal dispone: "Las medidas de naturaleza civil deberán ser solicitadas por la víctima o su representante legal, o bien por el Ministerio Fiscal, cuando existan hijos menores o personas con la capacidad judicialmente modificada, determinando su régimen de cumplimiento y, si procediera, las medidas complementarias a ellas que fueran precisas, siempre que no hubieran sido previamente acordadas por un órgano del orden jurisdiccional civil, y sin perjuicio de las medidas previstas en el artículo 158 del Código Civil. Cuando existan menores o personas con capacidad judicialmente modificada que convivan con la víctima y dependan de ella, el Juez deberá pronunciarse en todo caso, incluso de oficio, sobre la pertinencia de la adopción de las referidas medidas.

Estas medidas podrán consistir en la atribución del uso y disfrute de la vivienda familiar, determinar el régimen de guarda y custodia, visitas, comunicación y estancia con los menores o personas con la capacidad judicialmente modificada, el régimen de prestación de alimentos, así como cualquier disposición que se considere oportuna a fin de apartarles de un peligro o de evitarles perjuicios.

Las medidas de carácter civil contenidas en la orden de protección tendrán una vigencia temporal de 30 días. Si dentro de este plazo fuese incoado a instancia de la víctima o de su representante legal un proceso de familia ante la jurisdicción civil, las medidas adoptadas permanecerán en vigor durante los treinta días siguientes a la presentación de la demanda. En este término las medidas deberán ser ratificadas, modificadas o dejadas sin efecto por el Juez de primera instancia que resulte competente."

Pretendemos que sean parcial o totalmente modificadas las medidas civiles adoptadas en el Auto antes citado por el que se dictó orden de protección de mi representada como víctima de violencia de género, por resultar más adecuadas las propuestas en el presente escrito, tal y como se ha justificado detalladamente en los Hechos de esta demanda.

COSTAS.- Procede imponer al demandado el pago de las costas, en virtud de lo dispuesto en el art. 394 de la Ley de Enjuiciamiento Civil.

IURA NOVIT CURIA y cuantos resulten de pertinente aplicación.

Por lo expuesto,

SUPLICO A LA SECCIÓN: Que, tras admitir este escrito con los documentos que lo acompañan y sus copias, tenga por interpuesta por el Procurador que suscribe, con quien se solicita se entiendan las sucesivas diligencias, DEMANDA DE [ELEGIR: SEPARACIÓN MATRIMONIAL / DIVORCIO], en nombre y representación de Dª [NOMBRE Y APELLIDOS DE LA DEMANDANTE], contra D./Dª [NOMBRE Y APELLIDOS DEL DEMANDADO]; y, previos los trámites legales que procedan, dicte sentencia en la que, estimando íntegramente la demanda, declare la [ELEGIR: SEPARACIÓN MATRIMONIAL / DIVORCIO] y determine, como medidas o efectos derivados de la misma, los siguientes: [DETALLE DE TODAS LAS MEDIDAS QUE SE SOLICITAN CON CARÁCTER DEFINITIVO].

OTROSÍ DIGO: Que esta parte interesa la adopción de medidas provisionales conforme a lo dispuesto en el art. 773 de la Ley de Enjuiciamiento Civil. En relación con las mismas, y en atención a lo previsto en el art. 544 ter.7 de la Ley de Enjuiciamiento Criminal, se solicita la modificación de las adoptadas en el Auto en que se dictó la orden de protección de fecha [DÍA] de [MES] de [AÑO], por esta Sección, en los siguientes términos: [DETALLE DE LAS MEDIDAS PROVISIONALES A ADOPTAR, ESPECIFICANDO LAS QUE DEBEN RATIFICARSE Y LAS QUE HAN DE MODIFICARSE].

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma y número de colegiado del Letrado Firma del Procurador
