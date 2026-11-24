---
name: demanda-eficacia-civil-resolucion-pontificia-civ-0260
description: "Demanda de eficacia civil de resolución pontificia de matrimonio rato y no consumado con medidas. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de eficacia civil de resolución pontificia de matrimonio rato y no consumado con medidas

> Formulario **CIV-0260** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Demanda para que se declare la eficacia civil de una resolución pontificia de dispensa sobre matrimonio rato y no consumado (art. 80 del Código Civil, art. 778 LEC y art. VI.2 del Acuerdo con la Santa Sede de 3 de enero de 1979), con petición de las medidas personales y patrimoniales derivadas.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de eficacia civil de resolución pontificia de matrimonio rato y no consumado con medidas» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de eficacia civil de resolución pontificia de matrimonio rato y no consumado con medidas” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-eficacia-civil-resolucion-pontificia-civ-0260`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (7 veces)
- [ ] FECHA (6 veces)
- [ ] IMPORTE (4 veces)
- [ ] DOMICILIO (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL OTRO CÓNYUGE (2 veces)
- [ ] AÑO
- [ ] DÍA
- [ ] EDAD
- [ ] FOLIO
- [ ] LUGAR DE CELEBRACIÓN
- [ ] MES
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] NOMBRE Y APELLIDOS Y DATOS PERSONALES DEL CÓNYUGE DEMANDANTE
- [ ] Nº
- [ ] RAZONES
- [ ] SEDE
- [ ] TOMO

## Normas que cita el formulario

- art. 80 Código Civil
- art. 22.3 LOPJ
- art. 769 LEC
- art. 85.1 LOPJ
- art. 778 LEC
- art. 90 Código Civil

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

- Junto a «…UNDAMENTOS DE DERECHO 1. JURISDICCIÓN Y COMPETENCIA. El artículo 22.3 de la LOPJ»: comprobar el artículo vigente de la LOPJ (arts. 22 y siguientes) que fundamenta la competencia internacional en materia matrimonial
- Junto a «… [LOCALIDAD], a [DÍA] de [MES] de [AÑO]. Firma del Abogado/a y del Procurador/a.»: requisito de procedibilidad (art. 5 LO 1/2025): antes de demandar hay que intentar un medio adecuado de solución de controversias y acreditarlo con la demanda, salvo las materias excluidas del art. 5.2.

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

A LA SECCIÓN [ELEGIR: CIVIL / DE FAMILIA, INFANCIA Y CAPACIDAD] DEL TRIBUNAL DE INSTANCIA DE [SEDE]

Don/Doña [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, en nombre y representación de [NOMBRE Y APELLIDOS Y DATOS PERSONALES DEL CÓNYUGE DEMANDANTE], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº], ante el Tribunal comparezco y como mejor proceda en Derecho, DIGO:

Que mediante el presente escrito deduzco DEMANDA EN SOLICITUD DE EFICACIA CIVIL de la Resolución Pontificia sobre matrimonio rato y no consumado dictada en fecha [FECHA] por el Tribunal eclesiástico de [LOCALIDAD], respecto del matrimonio formado por mi representado/a y Don/Doña [NOMBRE Y APELLIDOS DEL OTRO CÓNYUGE], con domicilio actual en [DOMICILIO]. La acción que se ejercita es la regulada en el artículo 80 del Código Civil, que basamos en los siguientes hechos y fundamentos de derecho:

HECHOS

PRIMERO.- Don/Doña [NOMBRE Y APELLIDOS] y Don/Doña [NOMBRE Y APELLIDOS] contrajeron matrimonio canónico en [LUGAR DE CELEBRACIÓN] el día [FECHA], siendo el mismo inscrito en el Registro Civil de [LOCALIDAD] al Folio [FOLIO], Tomo [TOMO], según consta en la certificación matrimonial que aporto como documento núm. 1.

SEGUNDO.- De dicha unión ha nacido un hijo/a que en la actualidad cuenta con [EDAD] años de edad, de cuya guarda y custodia se ha hecho cargo hasta la fecha mi mandante, recibiendo en concepto de pensión de alimentos la cantidad de [IMPORTE] euros mensuales y ocupando el domicilio conyugal, sito en [DOMICILIO], para su residencia y la del hijo común. Esta situación de hecho ha sido aceptada por ambos progenitores desde el momento en que se inició el proceso ante el Tribunal Eclesiástico.

TERCERO.- Con fecha [FECHA] el Tribunal Eclesiástico de [LOCALIDAD] dictó Resolución Pontificia de matrimonio rato y no consumado, confirmada por Decreto del Tribunal de la Rota con fecha [FECHA]. Acompañamos como documentos núms. 2 y 3 testimonio literal de la resolución dictada y del Decreto que la confirma.

CUARTO.- En relación con las medidas de orden personal y patrimonial derivadas de la ineficacia del matrimonio proceden las siguientes:

1. La atribución de la guarda y custodia del hijo menor a mi mandante.

2. El pago de una pensión de alimentos mensual de [IMPORTE] euros.

3. [ELEGIR: No se solicita pensión compensatoria por ser mi representado/a autosuficiente económicamente / Se solicita pensión compensatoria de [IMPORTE] euros mensuales por las razones siguientes: [RAZONES]].

4. La atribución del domicilio conyugal a mi mandante para su residencia y la del hijo menor.

A los anteriores hechos le son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

1. JURISDICCIÓN Y COMPETENCIA. El artículo 22.3 de la LOPJ determina que resultan competentes los órganos jurisdiccionales españoles por ser ambos cónyuges de nacionalidad española. El artículo 769 LEC, en relación con lo dispuesto en el art. 85.1º LOPJ, señala que corresponde conocer de la demanda a la Sección Civil del Tribunal de Instancia del domicilio conyugal ubicado en [LOCALIDAD] [OPCIONAL — si ha lugar: siendo competencia de la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia por hallarse especializada en dicha materia].

2. PROCEDIMIENTO. Artículos 775 y 778 LEC.

3. LEGITIMACIÓN. Artículo 778 LEC, siendo mi representado/a el legitimado por ser el cónyuge afectado por los hechos.

4. ADMISIBILIDAD DE LA DEMANDA. Artículo 770.1ª LEC, acompañando a la demanda certificación de la inscripción de matrimonio, así como los documentos en que mi representado/a funda su derecho.

5. ACCIÓN QUE SE EJERCITA. La de eficacia civil del artículo 778 LEC y del artículo VI.2 del Acuerdo con la Santa Sede de 3 de enero de 1979, ratificado por instrumento de 4 de diciembre de 1979.

6. MEDIDAS. Artículo 778.2 LEC y arts. 90 y siguientes del Código Civil.

Por todo lo expuesto,

SUPLICO AL TRIBUNAL: Tenga por presentado este escrito y documentos adjuntos y sus copias junto con el poder, cuya devolución se solicita por ser necesario para otros usos, teniéndome por parte en la representación acreditada y por formulada demanda de solicitud de eficacia civil de la resolución pontificia de matrimonio rato y no consumado dictada con fecha [FECHA] por el Tribunal eclesiástico de [LOCALIDAD] y ratificada por Decreto del Tribunal de la Rota de fecha [FECHA] y, previa audiencia de Don/Doña [NOMBRE Y APELLIDOS DEL OTRO CÓNYUGE] y del Ministerio Fiscal, dicte Auto declarando dicha resolución ajustada al Derecho del Estado, concediéndole efectos en el orden civil y acordando su inscripción en el Registro Civil de [LOCALIDAD], y adoptando las siguientes medidas:

1. La atribución de la guarda y custodia del hijo menor a mi mandante.

2. El pago de una pensión de alimentos mensual de [IMPORTE] euros.

3. La atribución del domicilio conyugal a mi mandante para su residencia y la del hijo menor.

Es justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Abogado/a y del Procurador/a.
