---
name: peticion-reanudar-divorcio-separacion-contenciosos-civ-0138
description: "Petición de reanudar divorcio o separación contenciosos suspendidos y convertirlos en mutuo acuerdo. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Petición de reanudar divorcio o separación contenciosos suspendidos y convertirlos en mutuo acuerdo

> Formulario **CIV-0138** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Petición de reanudar divorcio o separación contenciosos suspendidos y convertirlos en mutuo acuerdo» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Petición de reanudar divorcio o separación contenciosos suspendidos y convertirlos en mutuo acuerdo” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:peticion-reanudar-divorcio-separacion-contenciosos-civ-0138`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] AÑO (7 veces)
- [ ] Nº (6 veces)
- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] DÍA (4 veces)
- [ ] MES (4 veces)
- [ ] NÚMERO (2 veces)
- [ ] SEDE (2 veces)
- [ ] CALLE
- [ ] COLEGIO
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] PROFESIÓN

## Normas que cita el formulario

- art. 770.5 LEC
- art. 770.7 LEC
- art. 90 CC
- art. 777 LEC

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

- Junto a «…Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [NÚMERO]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.
- Junto a «…Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
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

Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [NÚMERO]

Divorcio/Separación Contencioso/a número [Nº]/[AÑO]

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

D./Dª [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, en nombre y representación de D./Dª [NOMBRE Y APELLIDOS], mayor de edad, de profesión [PROFESIÓN], con domicilio en [LOCALIDAD], calle [CALLE], nº [NÚMERO], pta., cuya representación tengo acreditada en Autos de Divorcio/Separación Contencioso/a número [Nº]/[AÑO], comparezco ante este TRIBUNAL con la asistencia del Letrado D. /Dª [NOMBRE Y APELLIDOS], del Ilustre Colegio de Abogados de [COLEGIO], y DIGO:

Que por medio del presente escrito y en la representación que ostento, contando con el consentimiento de D./Dª [NOMBRE Y APELLIDOS], conforme a lo dispuesto en el art. 770.5 LEC, solicito el TRÁNSITO DE LAS PRESENTES ACTUACIONES A LOS TRÁMITES PREVISTOS EN EL ARTICULO 777 para procedimientos instados de mutuo acuerdo o por un cónyuge con consentimiento del otro, con base en los siguientes

HECHOS

Por escrito de fecha [DÍA] de [MES] de [AÑO], las partes solicitaron, de común acuerdo, la suspensión del procedimiento contencioso de divorcio/separación número [Nº]/[AÑO], conforme al art. 770.7 LEC, para someterse a procedimiento de mediación.

El Letrado de la Administración de Justicia suspendió, a tales efectos, el procedimiento mediante decreto de fecha [DÍA] de [MES] de [AÑO], por un plazo de [Nº] días.

El citado procedimiento de mediación, seguido por las partes con la intervención de D./Dª [NOMBRE Y APELLIDOS], como profesional mediador, culminó con los acuerdos de aquéllas relativos a los puntos que, conforme al art. 90 CC constituyen el contenido mínimo del convenio regulador, que quedaron reflejados en el Acta final de la mediación, de fecha [DÍA] de [MES] de [AÑO] en la que, así mismo, se hizo constar el acuerdo de las partes en el sentido de solicitar el tránsito del proceso de Divorcio/Separación a los trámites del art. 777 LEC, lo cual realizan por medio del presente escrito.

A tales efectos, se acompaña, como DOCUMENTO ÚNICO, PROPUESTA DE CONVENIO REGULADOR, suscrito por las partes con base en los acuerdos adoptados como resultado del citado proceso de mediación.

Resultan aplicables a los hechos expuestos los siguientes

FUNDAMENTOS DE DERECHO

Artículo 19, apartados 1 y 4 LEC: "1. Los litigantes están facultados para disponer del objeto del juicio y podrán renunciar, desistir del juicio, allanarse, someterse a mediación o a arbitraje y transigir sobre lo que sea objeto del mismo, excepto cuando la ley lo prohíba o establezca limitaciones por razones de interés general o en beneficio de tercero. ()

4. Asimismo, las partes podrán solicitar la suspensión del proceso, que será acordada por el Letrado de la Administración de Justicia mediante decreto siempre que no perjudique al interés general o a tercero y que el plazo de la suspensión no supere los sesenta días."

Art. 770, apartados 5 y 7 LEC, que disponen: "5. En cualquier momento del proceso, concurriendo los requisitos señalados en el artículo 777, las partes podrán solicitar que continúe el procedimiento por los trámites que se establecen en dicho artículo. ()

7. Las partes de común acuerdo podrán solicitar la suspensión del proceso de conformidad con lo previsto en el artículo 19.4 de esta Ley, para someterse a mediación."

Art. 777 LEC, que regula los trámites del procedimiento de Separación o divorcio solicitados de mutuo acuerdo o por uno de los cónyuges con el consentimiento del otro.

En virtud de lo expuesto,

SUPLICO AL TRIBUNAL que tenga por presentado este escrito con la propuesta de Convenio Regulador que se acompaña, lo admita y estimando la pretensión formulada conforme al art. 770.5 LEC, acuerde que se alce la suspensión decretada y se prosiga el procedimiento según lo dispuesto en el artículo 777 LEC y, previos los trámites legales pertinentes, entre ellos, la ratificación de las partes por separado ante este Tribunal, dicte, en su día, sentencia de Divorcio/Separación por la que apruebe en su integridad el Convenio Regulador presentado, ordenando la inscripción de esta sentencia en el Registro Civil de

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma y nº [Nº] del Letrado

Firma del Procurador

========================================================================
