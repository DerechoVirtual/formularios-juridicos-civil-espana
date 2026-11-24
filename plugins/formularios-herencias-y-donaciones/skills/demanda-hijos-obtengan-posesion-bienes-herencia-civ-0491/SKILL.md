---
name: demanda-hijos-obtengan-posesion-bienes-herencia-civ-0491
description: "Demanda para que los hijos obtengan la posesión de los bienes de la herencia. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda para que los hijos obtengan la posesión de los bienes de la herencia

> Formulario **CIV-0491** del plugin **Herencias, testamentos y donaciones** (`formularios-herencias-y-donaciones`) · Civil › Sucesiones y donaciones · normativa revisada el 24-11-2026.

## Qué es

Demanda para adquirir la posesión de los bienes procedentes de la herencia por los hijos, ya que la posesión de la finca heredada de su padre y adjudicada en proindiviso ordinario por mitades iguales, no está siendo poseída por nadie a título de dueño o usufructuario.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda para que los hijos obtengan la posesión de los bienes de la herencia» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda para que los hijos obtengan la posesión de los bienes de la herencia” para mi caso». También puedes invocarla directamente con `/formularios-herencias-y-donaciones:demanda-hijos-obtengan-posesion-bienes-herencia-civ-0491`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-herencias-y-donaciones:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Herencias, testamentos y donaciones) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (10 veces)
- [ ] Nº DE DOCUMENTO (5 veces)
- [ ] FECHA (4 veces)
- [ ] NÚMERO (4 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] DENOMINACIÓN SOCIAL
- [ ] FECHAS
- [ ] IMPORTE
- [ ] IMPORTE EN CIFRA
- [ ] LUGAR
- [ ] SEDE

## Normas que cita el formulario

- art. 266.3.º LEC
- art. 437.1 LEC
- art. 5 Ley Orgánica 1/2025
- art. 440 CC
- art. 661 CC
- art. 441.1 LEC

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

D./Dña. [NOMBRE Y APELLIDOS] Procurador de los Tribunales, en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS], con domicilio en (, según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], a quien asiste el Letrado en ejercicio abajo firmante D./Dña. [NOMBRE Y APELLIDOS], con despacho profesional en [LOCALIDAD], ante el Tribunal comparezco y como mejor proceda en Derecho, DIGO:

Que en la representación que ostento, formulo DEMANDA DE JUICIO VERBAL PARA ADQUIRIR LA POSESIÓN RESPECTO DE LOS BIENES, PROCEDENTES DE LA HERENCIA de D./Dña. [NOMBRE Y APELLIDOS], que se basa en los siguientes:

HECHOS

PRIMERO

El padre de mis mandantes falleció en [LOCALIDAD] en fecha [FECHA], habiendo otorgado testamento abierto ante el Notario de [LOCALIDAD], en fecha [FECHA], de protocolo n.º [NÚMERO] (se acredita ello mediante certificado de defunción y copia auténtica del documento notarial, como los documentos nos. y [Nº DE DOCUMENTO])

SEGUNDO

Los bienes relictos son los que figuran en el inventario que, como documento n.º [NÚMERO], se adosa a este escrito, entre los que se encuentra la siguiente finca:

TERCERO

La finca antes descrita fue adjudicada a mis mandantes en proindiviso ordinario por mitades iguales partes en la partición de la herencia (se adjunta escritura de manifestación y aceptación de herencia, con partición e hijuelas, como documento n.º [NÚMERO])

CUARTO

La expresada finca la ha poseído desde siempre el padre de mis mandantes a título de dueño, y en la actualidad nadie la posee a título de dueño o usufructuario.

QUINTO

El valor de la finca en cuestión conforme los precios corrientes en el mercado, asciende a la cantidad de [IMPORTE] euros ([IMPORTE EN CIFRA] €) (se acompaña tasación pericial de la agencia [DENOMINACIÓN SOCIAL], como documento n.º [NÚMERO]).

SEXTO

La parte actora manifiesta que, previo a la presentación de la presente demanda, se han llevado a cabo negociaciones con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad, y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria; incluyéndose entre las acciones realizadas el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución (documentos números [Nº DE DOCUMENTO]).

Finalmente, mi representado envió un requerimiento fehaciente al demandado con fecha [FECHA], fijando un plazo de 30 días naturales para llegar a un acuerdo amistoso, a través del abogado que firma este escrito, el cual fue contestado por el demandado por el mismo medio, rechazando el acuerdo, viéndonos en la necesidad de acudir a la presente vía judicial.

Acompaño como documento nº [Nº DE DOCUMENTO], el requerimiento efectuado y como documento nº [Nº DE DOCUMENTO], la contestación del demandado.

A los anteriores hechos son de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN Y COMPETENCIA

El conocimiento del asunto compete al Tribunal al que nos dirigimos, por ser el del lugar del último domicilio del finado D./Dña. [NOMBRE Y APELLIDOS], y D./Dña. [NOMBRE Y APELLIDOS] donde está sita la finca en cuestión (arts. 52.1.1.º y 4.º LEC).

II.- PROCEDIMIENTO

Art. 250.1.3.º LEC, que dispone la tramitación de la pretensión como modalidad del juicio verbal, en que es preceptiva la intervención de procurador y abogado según los arts. 23.1 y 31.1 LEC.

III.- LEGITIMACIÓN

Mis representados son herederos voluntarios del finado poseedor de la finca descrita, cuya legitimación activa se acredita documentalmente con la fehaciencia de la muerte del causante, su título de sucesión ‘mortis causa’ y la transmisión singular a los demandantes, así como ofreciendo la información testifical que exige la ley (art. 266.3.º LEC).

IV.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 en relación con el art. 437.1 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

V.- FONDO DEL ASUNTO

El art. 440 CCiv establece que la posesión de los bienes hereditarios se entiende transmitida al heredero sin interrupción y desde el momento de la muerte del causante, en el caso de que llegue a adirse la herencia, posesión civilísima que supone que, por ministerio de la Ley, una vez que se acepta, expresa o tácitamente, se produce la sucesión sin solución de continuidad en la posesión de los bienes hereditarios que ya venía poseyendo el "de cuius", aún sin acto material alguno de ocupación, como singularidad de la sucesión universal del art. 661 CCiv y en su tutela se establece una pretensión de tutela sumaria que modaliza el juicio verbal, con dos fases, una sin contradicción, de puesta en posesión y publicación de ésta, y otra, eventual, contradictora, si comparece algún opositor (art. 441.1 LEC).

VI.- CUANTÍA DE LA DEMANDA

Se corresponde con el valor del inmueble cuya posesión se reclama (art. 251.2.ª y 3.ª.5.º LEC)

Por lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito, con sus documentos y copias, se sirva admitirlo, previos los trámites legales, se dicte Auto que otorgue la posesión de la finca descrita en el ordinal segundo de los hechos de esta demanda, sin perjuicio de mejor derecho, llevando a cabo las actuaciones conducentes a tal efecto, y se ordene luego la publicación por edictos, que se insertarán en un lugar visible de la sede del Tribunal, en el Boletín Oficial de esta Provincia, y en uno de los periódicos de mayor circulación en la misma, instando a los interesados a comparecer y reclamar, mediante contestación a la demanda, en plazo de cuarentas días, si consideran tener mejor derecho que los demandantes, librándose a esta parte testimonio de dicho Auto y de las diligencias practicadas en su cumplimiento.

OTROSÍ DIGO: Que a los efectos de la información testifical solicitada de conformidad con el art. 266.3.º LEC, esta parte propone los siguientes testigos:

D./Dña. [NOMBRE Y APELLIDOS],

D./Dña. [NOMBRE Y APELLIDOS], y

D./Dña. [NOMBRE Y APELLIDOS], los cuales deberán ser citados para comparecer voluntariamente ante el Tribunal en el día y hora que se les señale.

Por lo expuesto,

SUPLICO AL TRIBUNAL

que teniendo por hechas las anteriores manifestaciones, y por solicitada información testifical que requiere la ley, acuerde lo conducente a su práctica.

Por ser de Justicia que pido en [LUGAR], a [FECHA].

Firma de Abogado/a	Firma de Procurador/a

========================================================================
