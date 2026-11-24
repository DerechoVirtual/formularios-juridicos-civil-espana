---
name: auto-suspende-ejecucion-laudo-arbitral-previa-civ-1878
description: "Auto que suspende la ejecución del laudo arbitral previa prestación de caución. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Auto que suspende la ejecución del laudo arbitral previa prestación de caución

> Formulario **CIV-1878** del plugin **Resoluciones judiciales civiles: autos, decretos y diligencias** (`formularios-resoluciones-judiciales-civiles`) · Civil › Resoluciones judiciales (autos, decretos, providencias, diligencias) · normativa revisada el 24-11-2026.

## Qué es

Auto acordando la suspensión de la ejecución del laudo arbitral, la cual será efectiva en cuanto la parte ejecutada preste la caución señalada.

Es un modelo de tipo **resoluciones judiciales (autos, decretos, providencias, diligencias)**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Auto que suspende la ejecución del laudo arbitral previa prestación de caución» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Auto que suspende la ejecución del laudo arbitral previa prestación de caución” para mi caso». También puedes invocarla directamente con `/formularios-resoluciones-judiciales-civiles:auto-suspende-ejecucion-laudo-arbitral-previa-civ-1878`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-resoluciones-judiciales-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Resoluciones judiciales civiles: autos, decretos y diligencias) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] IMPORTE (5 veces)
- [ ] NÚMERO (3 veces)
- [ ] AÑO (2 veces)
- [ ] SECCIÓN (2 veces)
- [ ] SEDE (2 veces)
- [ ] ACTO O RESOLUCIÓN
- [ ] FECHA
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] NOMBRE DE LA PARTE
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] Nº

## Normas que cita el formulario

- art. 529.3 LEC
- art. 533 LEC

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

- Junto a «…SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

Tfno.: Fax:

N.I.G.: N.I.G.:

Ejecución Título Judicial n.º [NÚMERO]/[AÑO]

Demandante: D./Dña. [NOMBRE Y APELLIDOS]

Abogado/a: D./Dña. [NOMBRE Y APELLIDOS] Procurador: D./Dña. [NOMBRE Y APELLIDOS]

Demandada: [NOMBRE DE LA PARTE].

Abogado/a: D./Dña. [NOMBRE Y APELLIDOS] Procurador: D./Dña. [NOMBRE Y APELLIDOS]

AUTO

Ilmo. Sr./a. D./Dña. [NOMBRE Y APELLIDOS], Magistrado-Juez de la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [NÚMERO]

En [LUGAR], a [FECHA].

ANTECEDENTES DE HECHO

PRIMERO.- En la presente ejecución de laudo arbitral, el Procurador Sr./a., en nombre y representación de [NOMBRE DEL REPRESENTADO/A]., parte ejecutada, ha solicitado la suspensión de la ejecución por alegar que estaba pendiente en la Sección [SECCIÓN] de la Audiencia Provincial de [LOCALIDAD] juicio verbal en que ejercía acción de anulación contra el laudo objeto de la ejecución.

Se ofrece prestar caución bastante en cuantía de [IMPORTE] ww [IMPORTE] ( €), y forma de aval bancario o de compañía de seguros.

SEGUNDO.- De la solicitud se ha concedido traslado a la parte ejecutante, que ha formulado escrito de alegaciones, oponiéndose a la suspensión.

FUNDAMENTOS DE DERECHO

PRIMERO.- Sentado el principio por Ley 60/2003 de 23 de diciembre, de Arbitraje (LA), que el título que lleva aparejado ejecución es el laudo arbitral, aunque no sea firme, su art. 45.1 contempla que, si contra el laudo se haya ejercitado acción de anulación, el ejecutado puede solicitar del tribunal competente la suspensión, siempre que ofrezca caución por el valor de la condena más los daños y perjuicios derivados de la demora en la ejecución del laudo.

SEGUNDO.- En el presente supuesto ha quedado acreditado, por testimonio aportado con la solicitud, que el laudo ejecutivo está pendiente de resolución de la acción ejercitada por el solicitante contra aquél en autos de Juicio de Anulación n.º [NÚMERO]/[AÑO] que se siguen en la Sección [SECCIÓN] de la Audiencia Provincial de

Así mismo, la parte ejecutada ha ofrecido prestar caución en una de las formas previstas en el art. 529.3 LEC, al que remite el propio art. 45.1 LA.

En cuanto a la cuantía, se estima por el Tribunal que el valor del crédito pecuniario que es objeto de ejecución, y los intereses legales del tiempo en que se presume se invertirá en el proceso de la anulación, puede evaluarse en [IMPORTE] ss [IMPORTE] ( €).

TERCERO.- A la luz de lo expuesto, no hay argumento para denegar la suspensión de la presente ejecución, a condición y en el momento de que se constituya la fianza en la forma y cuantía anteriormente indicadas, hasta que recaiga resolución en el proceso de anulación, cuando se resolverá por el Letrado de la Administración de Justicia alzar la suspensión o sobreseer la ejecución con los efectos prevenidos en los arts. 533 y 534 LEC.

Lógicamente, la suspensión determina la revocación de las medidas de apremio ya adoptadas, en tanto que no parece deban quedar subsistentes los embargos o adoptarse medidas de garantía de tales, cuando al propio tiempo presta caución el patrimonio del ejecutado.

PARTE DISPOSITIVA

1.- Se acuerda la suspensión de la ejecución del laudo arbitral promovida por la Procurador/a Sr./a [NOMBRE Y APELLIDOS], en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS], frente a [ACTO O RESOLUCIÓN].

2.- Dicha suspensión será efectiva en cuanto la parte ejecutada preste la siguiente caución:

Forma: Aval solidario y de duración indefinida y pagadero a primer requerimiento emitido por entidad de crédito o sociedad de garantía recíproca.

Cuantía: ss [IMPORTE] ( €).

3.- Una vez prestada caución, álcense los embargos decretados en el auto de despacho de ejecución, librándose entonces oficios a la entidad a que se ordenó retención de cantidades, dejándola sin efecto.

Así lo acuerdo, mando y firmo:

Firma de Juez/a

Esta resolución se notificará a las partes, con advertencia de que contra la misma no cabe recurso ordinario alguno (art. 45.1 "in fine" LA).

========================================================================
