---
name: demanda-general-juicio-verbal-razon-cuantia-civ-1002
description: "Demanda general de juicio verbal por razón de la cuantía. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda general de juicio verbal por razón de la cuantía

> Formulario **CIV-1002** del plugin **Proceso civil: demandas, contestaciones, prueba y vista** (`formularios-proceso-civil`) · Civil › Escritos procesales (demanda, contestación, prueba, vista) · normativa revisada el 24-11-2026.

## Qué es

Modelo general de demanda de juicio verbal determinado por la cuantía (arts. 250 y 437 y siguientes LEC), con fundamentos de jurisdicción, competencia, procedimiento, capacidad, legitimación, cuantía, postulación y procedibilidad, y con otrosíes opcionales (representación, devolución de poder, medida cautelar, prueba, dictamen pericial, actos de comunicación y tasa judicial). Se adapta a cualquier pretensión sustituyendo los campos.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda general de juicio verbal por razón de la cuantía» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda general de juicio verbal por razón de la cuantía” para mi caso». También puedes invocarla directamente con `/formularios-proceso-civil:demanda-general-juicio-verbal-razon-cuantia-civ-1002`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-proceso-civil:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Proceso civil: demandas, contestaciones, prueba y vista) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (5 veces)
- [ ] DOMICILIO (4 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] ARTÍCULO (2 veces)
- [ ] FIRMA (2 veces)
- [ ] MEDIDA CAUTELAR SOLICITADA (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL PERITO (2 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] PROFESIÓN (2 veces)
- [ ] 251/252
- [ ] ACCIÓN EJERCITADA
- [ ] APARTADO
- [ ] AÑO
- [ ] DATOS Y CIRCUNSTANCIAS DE IDENTIFICACIÓN DEL DEMANDADO
- [ ] DATOS Y CIRCUNSTANCIAS DE IDENTIFICACIÓN DEL DEMANDANTE
- [ ] DENOMINACIÓN SOCIAL
- [ ] DOCUMENTO ORIGINAL QUE SE REQUIERE
- [ ] DOMICILIO PROFESIONAL
- [ ] DÍA
- [ ] FECHA
- [ ] FECHAS
- [ ] FUERO APLICABLE
- [ ] FUNDAMENTO DE LA CAPACIDAD
- [ ] HECHO PRIMERO
- [ ] HECHO SEGUNDO
- [ ] HECHO TERCERO
- [ ] IMPORTE
- [ ] IMPORTE DE LA CUOTA FIJA
- [ ] INDICAR LOS FUNDAMENTOS EN QUE SE BASA LA DEMANDA
- [ ] LUGARES
- [ ] MATERIA DE LA PERICIA
- [ ] MES
- [ ] NOMBRE Y APELLIDOS DEL ABOGADO/A
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] NORMA
- [ ] Nº DE COLEGIADO
- [ ] Nº DE REGLA
- [ ] OBJETO DE LA LITIS
- [ ] PARTE O ENTIDAD
- [ ] … y 6 datos más que aparecen una vez en el modelo

## Normas que cita el formulario

- art. 9.2 LOPJ
- art. 85.1 LOPJ
- art. 36 LEC
- art. 44 LEC
- art. 45 LEC
- art. 50 LEC
- art. 250 LEC
- art. 6 LEC
- art. 10 LEC
- art. 253 LEC
- art. 23 LEC
- art. 437.1 LEC
- art. 5 Ley Orgánica 1/2025
- art. 394 LEC
- art. 32.1 LEC
- art. 721 LEC
- art. 335.2 LEC
- art. 337.2 LEC
- art. 149 LEC
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

### Avisos de actualización (3) — se aplican en el texto, nunca se copian en el documento

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…e no vengan atribuidos por esta ley a otros órganos judiciales (art. 85.1 LOPJ).»: comprobar la numeración y redacción vigentes del art. 85 LOPJ tras la LO 1/2025.
- Junto a «…aber sido declarado inconstitucional y nulo por la STC 140/2016, de 21 de julio.»: comprobar el importe vigente de la cuota fija.

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

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, que actúa en nombre y representación de [ELEGIR: D./Dña. [NOMBRE Y APELLIDOS] / la mercantil [DENOMINACIÓN SOCIAL]] [DATOS Y CIRCUNSTANCIAS DE IDENTIFICACIÓN DEL DEMANDANTE], con domicilio en [DOMICILIO], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento n.º [Nº DE DOCUMENTO], a quien asiste el Letrado/a en ejercicio D./Dña. [NOMBRE Y APELLIDOS DEL ABOGADO/A], colegiado/a n.º [Nº DE COLEGIADO] del Ilustre Colegio de la Abogacía de [LOCALIDAD], con despacho abierto en esta localidad, calle [DOMICILIO PROFESIONAL] de [LOCALIDAD], ante el Tribunal comparezco y, como mejor proceda en Derecho, DIGO:

Que, en la representación que ostento, interpongo DEMANDA DE JUICIO VERBAL sobre [OBJETO DE LA LITIS], frente a [DATOS Y CIRCUNSTANCIAS DE IDENTIFICACIÓN DEL DEMANDADO], con domicilio en [DOMICILIO]. A efectos del primer emplazamiento del demandado, para el caso de que no sea hallado en dicho domicilio, se designan los siguientes lugares donde podrá intentarse la comunicación, por el siguiente orden: [LUGARES].

Se ejercita en la presente demanda la acción de [ACCIÓN EJERCITADA]. Fundamento la misma en los siguientes hechos y consideraciones jurídicas:

HECHOS

(Los hechos se expondrán de forma ordenada y clara, en párrafos separados y numerados, expresándose de igual forma los documentos que se aporten en relación con los mismos. También podrán formularse valoraciones o razonamientos. En su caso, también se describirá el proceso de negociación previo y los medios de solución de controversias de manera amistosa y extrajudicial.)

PRIMERO.– [HECHO PRIMERO]

SEGUNDO.– [HECHO SEGUNDO]

TERCERO.– [HECHO TERCERO]

VALORACIÓN FÁCTICA

[VALORACIONES O RAZONAMIENTOS SOBRE LOS HECHOS]

APORTACIÓN DE PRUEBA

A los efectos de acreditar el fundamento de las pretensiones que se deducen, acompaño:

DOCUMENTO N.º [Nº]: [DESCRIPCIÓN DEL DOCUMENTO, por ejemplo, licencia administrativa o escritura de compraventa] (ordinal primero)

DOCUMENTO N.º [Nº]: [DESCRIPCIÓN DEL DOCUMENTO, por ejemplo, certificación de organismo público] (ordinal segundo)

DOCUMENTO N.º [Nº]: [DESCRIPCIÓN DEL DOCUMENTO, por ejemplo, testimonio de diligencia preliminar practicada al amparo de lo dispuesto en el art. [ARTÍCULO] de la Ley [NORMA], o actas de requerimiento notarial de fechas [FECHAS]] (ordinal tercero)

DOCUMENTO N.º [Nº]: dictamen pericial de los daños y perjuicios causados a mi representado/a, emitido por el perito D./Dña. [NOMBRE Y APELLIDOS DEL PERITO]

A los anteriores hechos son aplicables los siguientes

FUNDAMENTOS DE DERECHO

I.– JURISDICCIÓN Y COMPETENCIA

A) JURISDICCIÓN

POTESTAD JURISDICCIONAL.– La potestad jurisdiccional se ejerce por los Tribunales determinados por las leyes, según las normas de competencia y procedimiento que las mismas establezcan (art. 117.3 CE).

JURISDICCIÓN CIVIL.– Los Tribunales del orden civil conocerán, además de las materias que les son propias, de todas aquellas que no estén atribuidas a otro orden jurisdiccional (art. 9.2 LOPJ).

Los Tribunales de Instancia conocerán en el orden civil, en primera instancia, de los juicios que no vengan atribuidos por esta ley a otros órganos judiciales (art. 85.1 LOPJ).

LÍMITES DE LA JURISDICCIÓN.– La extensión y límites de la jurisdicción de los Tribunales civiles españoles se determinará por lo dispuesto en la LOPJ y en los tratados y convenios internacionales en los que España sea parte (art. 36 LEC).

B) COMPETENCIA

PREDETERMINACIÓN LEGAL DE LA COMPETENCIA.– Para que los Tribunales civiles tengan competencia en cada caso se requiere que el conocimiento del pleito les esté atribuido por normas con rango de ley y anteriores a la incoación de las actuaciones de que se trate (art. 44 LEC).

COMPETENCIA OBJETIVA. TRIBUNALES DE INSTANCIA.– Corresponde a dichos órganos jurisdiccionales el conocimiento, en primera instancia, de todos los asuntos civiles que por disposición legal expresa no se hallen atribuidos a otros Tribunales. Conocerán, asimismo, dichos Tribunales de los asuntos, actos, cuestiones y recursos que les atribuye la LOPJ (art. 45 LEC).

COMPETENCIA TERRITORIAL.– Es competente el Tribunal al que nos dirigimos por [FUERO APLICABLE], según dispone el art. [ARTÍCULO] LEC. Las reglas de competencia territorial se determinan en los arts. 50 y siguientes LEC.

II.– PROCEDIMIENTO

Conforme al apartado [APARTADO] del art. 250 LEC, el procedimiento ajustado a derecho será el del juicio verbal regulado en los arts. 437 y siguientes de la misma Ley.

III.– CAPACIDAD Y REPRESENTACIÓN

La tienen demandante y demandada por [FUNDAMENTO DE LA CAPACIDAD], a tenor de lo dispuesto en los arts. 6 y 7 LEC. (Se consignarán las alegaciones que procedan sobre capacidad de las partes, representación de ellas o del procurador.)

IV.– LEGITIMACIÓN

Corresponde al demandante y demandado citados, según el art. 10 LEC, el primero por el derecho y acción que tiene para reclamar, y el segundo como obligado por su intervención en el negocio del que se trae causa y porque el pronunciamiento que en definitiva se pretende le atañe e interesa.

V.– CUANTÍA

Conforme al art. 253 LEC, cifro la cuantía de la presente demanda en [IMPORTE], fijación que amparo en el siguiente fundamento: [EXPRESAR JUSTIFICADAMENTE LA CUANTÍA DE LA DEMANDA, CALCULADA CONFORME A LAS REGLAS LEGALES DE LOS ARTS. 251 Y 252 LEC].

Deberán presentarse los documentos o dictámenes que acrediten el valor de la cosa litigiosa, calculada con arreglo a las reglas número/s [Nº DE REGLA] del/de los artículo/s [251/252] de dicha Ley.

VI.– POSTULACIÓN Y DEFENSA

Conforme a lo previsto en los arts. 23 y 31 LEC, se presenta la demanda por medio de Procurador legalmente habilitado y bajo dirección de Letrado firmante de la misma. (Véase el otrosí de representación para el supuesto en que no sea preceptiva la intervención de estos profesionales.)

VII.– CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4.º y 399.3 LEC, en relación con el art. 437.1 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

VIII.– FONDO DE LA CUESTIÓN CONTROVERTIDA

[INDICAR LOS FUNDAMENTOS EN QUE SE BASA LA DEMANDA]

IX.– COSTAS

Deberán ser impuestas a la demandada en virtud del principio cuasiobjetivo del vencimiento que rige en la primera instancia de los declarativos, a tenor del art. 394 LEC.

Por lo expuesto,

SUPLICO AL TRIBUNAL

que, habiendo por presentado este escrito de demanda con los documentos que lo acompañan y copias de uno y otros, los admita y me tenga por comparecido y parte en la representación que ostento y que acreditada dejo; y por promovido juicio verbal frente a las personas designadas en el encabezamiento, dé al mismo el curso señalado en la ley y, en su día, dicte sentencia en la que, estimando íntegramente la demanda:

a) Declare [PRONUNCIAMIENTO DECLARATIVO].

b) Ordene [PRONUNCIAMIENTO DE HACER O NO HACER].

c) Condene [PRONUNCIAMIENTO DE CONDENA].

Todo ello con imposición de las costas del juicio a la parte demandada.

[OPCIONAL — incluir si procede: OTROSÍ DE REPRESENTACIÓN]

OTROSÍ DIGO que esta parte viene a poner expresamente en conocimiento del órgano jurisdiccional, a los efectos que procedan, que, aun cuando para esta clase de procedimientos no resulta preceptiva la intervención de Letrado ni de Procurador, es intención de esta parte servirse de los referidos profesionales.

Por lo que,

SUPLICO AL TRIBUNAL que, teniendo por causada la anterior manifestación a los efectos del art. 32.1 LEC, se sirva proceder en su consecuencia.

[OPCIONAL — incluir si procede: OTROSÍ DE DEVOLUCIÓN DE PODER]

OTROSÍ DIGO. Que, por necesitar para otros usos la copia de escritura de poder acreditativa de la representación del suscrito Procurador, intereso y

SUPLICO AL TRIBUNAL se sirva acordar su desglose y devolución a esta parte, dejando en autos testimonio literal de la misma.

[OPCIONAL — incluir si procede: OTROSÍ DE MEDIDA CAUTELAR]

OTROSÍ DIGO. Que, al amparo de lo previsto en los arts. 721 y siguientes LEC, solicito del Tribunal la adopción de la medida cautelar de [MEDIDA CAUTELAR SOLICITADA] (véase el modelo general de medida cautelar solicitada junto con la demanda principal).

SUPLICO AL TRIBUNAL que adopte la medida cautelar de [MEDIDA CAUTELAR SOLICITADA].

[OPCIONAL — incluir si procede: OTROSÍ DE PRUEBA]

OTROSÍ DIGO: Que interesa al derecho de esta parte valerse para la vista de los siguientes medios de PRUEBA:

A) INTERROGATORIO del demandado D./Dña. [NOMBRE Y APELLIDOS].

B) DOCUMENTAL consistente en:

— que se remita oficio a [ORGANISMO, por ejemplo, la comisaría de la Policía Local de [LOCALIDAD]], a fin de que remita al Tribunal [DOCUMENTO, por ejemplo, el atestado n.º [Nº], elaborado por razón del accidente de tráfico acaecido el día [FECHA]];

— que se requiera a [PARTE O ENTIDAD], para aportación a la vista de [DOCUMENTO ORIGINAL QUE SE REQUIERE].

C) TESTIFICAL, para que se proceda a citar judicialmente a las siguientes personas para ser interrogadas en la vista:

D./Dña. [NOMBRE Y APELLIDOS], de profesión [PROFESIÓN], con domicilio en [DOMICILIO].

D./Dña. [NOMBRE Y APELLIDOS], de profesión [PROFESIÓN], con domicilio en [DOMICILIO].

SUPLICO AL TRIBUNAL que, teniendo por causada la precedente solicitud de prueba a los efectos oportunos, se digne ordenar todo lo conducente para su práctica.

[OPCIONAL — incluir si procede: OTROSÍ APORTANDO DICTAMEN PERICIAL]

OTROSÍ DIGO que interesa al derecho de esta parte valerse para el acto de la vista de la prueba pericial de [MATERIA DE LA PERICIA], a cuyo objeto se ha recabado y obtenido dictamen por escrito de [TITULACIÓN] D./Dña. [NOMBRE Y APELLIDOS DEL PERITO], que contiene fórmula de juramento atenida al art. 335.2 LEC, el cual se presenta con la demanda, con solicitud de que se cite judicialmente al autor, a fin de que concurra al acto de la vista, para esclarecer su pericia y sujetarse a las preguntas aclaratorias o adicionales que deseen formular las partes o S.S.ª, conforme al art. 337.2 LEC.

SUPLICO AL TRIBUNAL que, por causadas las manifestaciones precedentes a los oportunos efectos, se sirva proveer con arreglo a la Ley.

[OPCIONAL — incluir si procede: OTROSÍ DE ACTOS DE COMUNICACIÓN]

OTROSÍ DIGO: que, en aplicación de los arts. 149 y 152 LEC, interesa esta parte que los actos de comunicación sean realizados por el Procurador que suscribe.

SUPLICO AL TRIBUNAL que se dé traslado directo de los actos de comunicación a este Procurador para su diligenciamiento.

[OPCIONAL — incluir si procede: OTROSÍ DE TASA JUDICIAL (solo si la parte actora es persona jurídica no exenta)]

OTROSÍ DIGO: Que, estando la presente demanda sujeta al abono de la tasa por el ejercicio de la potestad jurisdiccional fijada por la Ley 10/2012, de 20 de noviembre, modificada por el Real Decreto-ley 3/2013, de 22 de febrero, y la Ley 25/2015, de 28 de julio, y por la Orden HAP/861/2015, de 7 de mayo, siendo mi representada persona jurídica no exenta, se acompaña a la presente demanda como documento n.º [Nº DE DOCUMENTO] la correspondiente autoliquidación, con el ejemplar para la Administración de Justicia debidamente validado y en el que consta el pago de la cantidad de [IMPORTE DE LA CUOTA FIJA] euros correspondiente a la cuota fija, sin que se incluya la cuota variable prevista en el art. 7.2 de la Ley 10/2012, al haber sido declarado inconstitucional y nulo por la STC 140/2016, de 21 de julio.

En virtud de lo anterior,

SUPLICO AL TRIBUNAL que tenga por hecha la anterior manifestación a los efectos pertinentes y por acompañado el documento justificativo del abono de la tasa.

Es justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Abogado/a: [FIRMA] Firma del Procurador/a: [FIRMA]
