---
name: contrato-ceden-fincas-precario-civ-0663
description: "Contrato por el que se ceden fincas en precario. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato por el que se ceden fincas en precario

> Formulario **CIV-0663** del plugin **Propiedad, posesión, servidumbres e hipotecas** (`formularios-propiedad-y-derechos-reales`) · Civil › Propiedad y derechos reales · normativa revisada el 24-11-2026.

## Qué es

Contrato por el que el propietario de unas fincas rústicas cede su uso gratuito y revocable a otra persona (precarista) para destinarlas al cultivo, sin renta y sin plazo fijo, con obligación de devolverlas cuando se le requiera. Se usa para formalizar cesiones de tierras por amistad o necesidad, evitando que se confundan con un arrendamiento.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato por el que se ceden fincas en precario» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato por el que se ceden fincas en precario” para mi caso». También puedes invocarla directamente con `/formularios-propiedad-y-derechos-reales:contrato-ceden-fincas-precario-civ-0663`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-propiedad-y-derechos-reales:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Propiedad, posesión, servidumbres e hipotecas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL PROPIETARIO (2 veces)
- [ ] Nº (2 veces)
- [ ] Nº DE PARCELA (2 veces)
- [ ] Nº DE POLÍGONO (2 veces)
- [ ] PARAJE (2 veces)
- [ ] SUPERFICIE (2 veces)
- [ ] AÑO
- [ ] DÍA
- [ ] IMPORTE
- [ ] LOCALIDAD
- [ ] MES
- [ ] NOMBRE Y APELLIDOS DEL PRECARISTA
- [ ] PLAZO
- [ ] SEDE
- [ ] TÉRMINO MUNICIPAL

## Normas que cita el formulario

- art. 452 Código Civil

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

- Junto a «…RMAS: El Propietario: [NOMBRE Y APELLIDOS] | El Precarista: [NOMBRE Y APELLIDOS]»: la cesión es en precario (gratuita y revocable a voluntad del cedente). Si se pactara un plazo cierto o una contraprestación, podría calificarse de arrendamiento rústico (Ley 49/2003, de Arrendamientos Rústicos); comprobar la calificación antes de firmar.

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

CONTRATO DE CESIÓN DE FINCAS EN PRECARIO

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

EXPONEN

I. Que D./Dña. [NOMBRE Y APELLIDOS DEL PROPIETARIO], como consecuencia de [TÍTULO: compraventa / herencia / donación / otro], es dueño/a de las fincas que a continuación se relacionan, estando todas ellas libres de cargas y gravámenes y al corriente en el pago de impuestos:

Término municipal de [TÉRMINO MUNICIPAL]

Nº de polígono | Nº de parcela | Superficie (m2) | Paraje
[Nº DE POLÍGONO] | [Nº DE PARCELA] | [SUPERFICIE] | [PARAJE]
[Nº DE POLÍGONO] | [Nº DE PARCELA] | [SUPERFICIE] | [PARAJE]

II. Que, debido a la buena amistad que mantienen D./Dña. [NOMBRE Y APELLIDOS DEL PROPIETARIO] (en lo sucesivo, «El Propietario») y D./Dña. [NOMBRE Y APELLIDOS DEL PRECARISTA] (en lo sucesivo, «El Precarista»), y dada la necesidad de tierras de cultivo que este último tiene, para sí y su familia, han concertado y convenido la cesión gratuita de dichos bienes, y lo hacen de acuerdo con las siguientes

CLÁUSULAS

Cesión de uso gratuita

I. El Propietario cede gratuitamente al Precarista el uso de las fincas descritas en el Exponendo Primero.

II. El Precarista no abonará al Propietario ninguna cantidad en concepto de renta, pues la cesión que se hace es gratuita, originada por las relaciones de amistad que existen entre ellos y debida a la necesidad apremiante de consecución de superficie de cultivo del primero.

III. Las fincas objeto de este contrato serán destinadas al cultivo de [CULTIVO: p. ej., cereal], no pudiendo el Precarista, sin autorización expresa, cambiar la explotación, y pudiendo contratar, siempre a su cargo y con completa indemnidad para la otra parte, a las personas que considere necesarias para ayudarle en la explotación.

IV. Todas las fincas descritas en el Exponendo Primero serán sembradas al menos una vez cada [Nº] años, no pudiendo dejar ninguna de ellas yerma (sin sembrar) por más tiempo.

Prohibición de subarriendo

El Precarista no podrá subarrendar ni ceder en explotación las fincas cedidas.

Devolución de las fincas cedidas

I. A partir del momento en que se haga cualquier requerimiento por parte del Propietario para recuperar la posesión del bien cedido en precario, el Precarista dispondrá del plazo de [PLAZO] para recoger la cosecha sembrada y dejar a disposición del Propietario y en perfecto estado la finca que este desee, o la totalidad de las fincas cuyo uso y explotación se cede en este contrato.

II. Si al finalizar la cesión existieran frutos pendientes, el Precarista tendrá sobre ellos los derechos que, según el artículo 452 del Código Civil, corresponden al poseedor de buena fe.

Incumplimiento de la obligación de devolución de las fincas cedidas

I. Si, practicado el requerimiento, el Precarista no devolviera los terrenos cedidos en el plazo estipulado, deberá abonar al Propietario:

a) Una suma igual a [IMPORTE] euros por día de ocupación no consentida, en concepto de pena convencional derivada del incumplimiento.

b) Los intereses legales que correspondan hasta la fecha de su pago efectivo.

II. Igualmente, el incumplimiento de la obligación de abandono de los terrenos establecida en la estipulación anterior conllevará la pérdida de todo derecho que el Precarista pudiera tener sobre los frutos pendientes y sobre las mejoras útiles y voluntarias que hubiera realizado durante el tiempo en que estuvo vigente la cesión.

III. El Precarista que hubiera incumplido la obligación de devolución de las fincas objeto de este contrato responderá, además, de cualquier pérdida o deterioro que las mismas sufrieran, incluso por causa de fuerza mayor.

Gastos de conservación y mejoras

I. Los gastos de conservación necesarios para mantener los terrenos cedidos en estado de servir para el aprovechamiento o explotación a que han sido destinados al concertar el contrato serán de cuenta y cargo del Precarista.

II. No le serán abonables al Precarista las mejoras útiles y voluntarias que realice, cualquiera que sea su naturaleza; pero, finalizada la cesión, podrá llevarse las obras en que consista la mejora si son individualizables sin menoscabo de la finca y si el Propietario no prefiere abonar el importe de lo gastado.

III. Los gastos del Impuesto sobre Bienes Inmuebles de naturaleza rústica y del arreglo de caminos correrán a cargo del Propietario, ya que no hay una voluntad de lucro en la cesión de las fincas.

IV. El Precarista renuncia a los beneficios futuros de derechos sobre las fincas que pudiera obtener, como llevar sembrándolas más de [Nº] años o las subvenciones de las Administraciones agrarias estatal, autonómica o de la Unión Europea.

Gastos judiciales y extrajudiciales

Serán de cuenta y cargo del Precarista todos los gastos, judiciales y extrajudiciales, que origine cualquier incumplimiento de este contrato, incluidos los honorarios de letrado y procurador aunque la intervención de estos no fuera preceptiva.

Cláusula de sumisión expresa

Para cuantas cuestiones o divergencias pudieran suscitarse en relación con el presente contrato, ambas partes acuerdan someterse a los tribunales de [SEDE], renunciando expresamente al fuero propio si lo tuvieran.

Y en prueba de conformidad y aceptación de cuanto antecede, ambas partes suscriben por duplicado y a un solo efecto cada una de las hojas de que se compone el presente CONTRATO DE CESIÓN DE FINCAS EN PRECARIO en el lugar y fecha indicados en el encabezamiento.

FIRMAS:

El Propietario: [NOMBRE Y APELLIDOS] | El Precarista: [NOMBRE Y APELLIDOS]
