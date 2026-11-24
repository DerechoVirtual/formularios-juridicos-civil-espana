---
name: demanda-ejecutiva-dineraria-laudo-arbitral-civ-1503
description: "Demanda ejecutiva dineraria de un laudo arbitral. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda ejecutiva dineraria de un laudo arbitral

> Formulario **CIV-1503** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda ejecutiva dineraria de un laudo arbitral» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda ejecutiva dineraria de un laudo arbitral” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:demanda-ejecutiva-dineraria-laudo-arbitral-civ-1503`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (7 veces)
- [ ] IMPORTE (5 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] PROVINCIA (3 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] SEDE (2 veces)
- [ ] AÑO
- [ ] CALLE
- [ ] DESCRIPCIÓN DEL BIEN
- [ ] DÍA
- [ ] LUGAR
- [ ] MES
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] Nº
- [ ] Nº DE PROCEDIMIENTO
- [ ] NÚMERO
- [ ] OTROS DATOS
- [ ] PERIODICIDAD
- [ ] ÓRGANO O PERSONA

## Normas que cita el formulario

- art. 550.1.1 LEC
- art. 575 LEC
- art. 575.1 LEC
- art. 590 LEC
- art. 85.1 LOPJ
- art. 553.2 LEC
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

Don [NOMBRE Y APELLIDOS] Procurador de los Tribunales, en nombre y representación de [NOMBRE DEL REPRESENTADO/A], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño a este escrito, comparezco ante este Tribunal y DIGO:

Que por medio del presente formulo DEMANDA EJECUTIVA del laudo arbitral de fecha [FECHA] dictado por [ÓRGANO O PERSONA] en el procedimiento arbitral seguido entre mi representado y D. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], calle [CALLE], con base en los siguientes:

HECHOS

PRIMERO.- Que en fecha de [FECHA], por la Corte de la localidad de [LOCALIDAD] se dictó laudo arbitral en procedimiento [Nº DE PROCEDIMIENTO], seguido entre mi representado y el demandado D. [NOMBRE Y APELLIDOS], cuya parte dispositiva es la siguiente: "Estimo la demanda arbitral deducida por D.contra D.condeno al demandado a que indemnice al actor en la cantidad de [IMPORTE] euros, más los intereses legales, así como al pago de todas las costas y gastos de este procedimiento".

El citado procedimiento arbitral fue seguido en virtud del convenio arbitral de fecha [FECHA] suscrito entre las partes [OTROS DATOS] donde, en relación con el contrato de arrendamiento de servicios de fecha [FECHA], en el cual convenían someten a arbitraje todas las controversias que puedan surgir derivadas del incumplimiento del contrato de arrendamiento, encomendándose la administración del arbitraje y la designación de árbitros a la Corte Arbitral de

En ejecución del citado convenio se dictó el expresado laudo de fecha [FECHA], el cual fue notificado a las partes en fecha [FECHA]

A los efectos establecidos en el artículo 550.1.1º de la LEC se acompañan como documentos [Nº DE DOCUMENTO] el laudo arbitral de fecha [FECHA] cuya ejecución se pretende, el convenio arbitral y las diligencias de notificación del laudo a las partes extendidas por la Secretaría de la Corte.

SEGUNDO.- De conformidad con el laudo, se interesa que se despache ejecución contra del demandado D. [NOMBRE Y APELLIDOS], debiendo hacer pago de [IMPORTE] euros en concepto de principal e intereses moratorios y vencidos, más la cantidad de [IMPORTE] euros, de acuerdo con lo establecido por el artículo 575 LEC, en concepto de intereses y costas que se prevé se devengarán durante el desarrollo de la ejecución (debiéndose tener en cuenta que dicha cantidad no podrá exceder del treinta por ciento de la que se reclame en la demanda, sin perjuicio de la posterior liquidación, aunque, excepcionalmente podrá rebasarse dicho límite si ele ejecutante justifica una previsible mayor duración del proceso ejecutivo, de acuerdo con lo establecido en el artículo 575.1 LECiv).

TERCERO.- Que designo como bienes a embargar del ejecutado, teniéndolos por suficientes para cubrir el importe de la ejecución los siguientes [DESCRIPCIÓN DEL BIEN]

CUARTO.- Que desconociendo esta parte bienes que puedan ser objeto de embargo por parte de este Tribunal, al amparo de lo dispuesto en el artículo 590 LECiv, esta parte solicita al Tribunal proceda a dirigirse a los efectos de determinación de la relación de bienes muebles e inmuebles, así como depósitos o imposiciones a plazo fijo que el ejecutado pueda tener a su nombre a los siguientes organismos:

1.- Gerencia Territorial del Catastro de [PROVINCIA]

2.- Delegación Territorial de la Agencia Tributaria de [PROVINCIA]

3.- Registro de la Propiedad nº [NÚMERO] de [LOCALIDAD]

4.- Jefatura Provincial de tráfico de [LOCALIDAD]

5.- Caja de Ahorros Provincial de [PROVINCIA]

A los siguientes hechos le son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

Competencia

Artículo 545.2 LEC, en relación con lo dispuesto en el art. 85.1º LOPJ. La competencia es de la Sección Civil del Tribunal de Instancia de [SEDE], ante el cual se formula esta demanda, por ser el correspondiente al lugar en que se ha dictado el laudo que se pretende ejecutar.

Legitimación

Artículo 517 LEC., en relación con los artículos 571 y ss para la ejecución dineraria.

Título ejecutivo

Artículo 517.2.2ª: Sólo tendrán aparejada ejecución los siguientes títulos:

Procedimiento

Artículo 548 LEC, procediéndose a despachar ejecución de la sentencia una vez transcurridos los veinte días establecidos en el precepto desde la notificación.

Artículo 549 LEC en relación con el que debe ser el contenido de la demanda ejecutiva.

Artículo 550.1.1º LEC en relación a los documentos que deben acompañarse.

Artículos 551 a 554 LEC en relación al despacho de ejecución.

Costas

Artículo 539.2 LEC.

Por todo ello,

SUPLICO AL TRIBUNAL: que teniendo por presentado este escrito con los documentos que lo acompañan y sus copias y previo traslado al deudor según lo establecido en el artículo 553.2 LEC, se acuerde, sin necesidad de previo requerimiento al deudor, se proceda a despachar ejecución por la cantidad de [IMPORTE] euros en concepto de principal e intereses vencidos, más la cantidad de [IMPORTE] en concepto de intereses y costas devengados constante el proceso de ejecución, así como se proceda al embargo de los bienes de D. reseñados en el cuerpo de este escrito en cantidad suficiente para cubrir las responsabilidades reclamadas y con su producto se proceda a realizar completo pago por todos los conceptos reclamados al ejecutante.

OTROSÍ DIGO.- Que estando la presente demanda sujeta al abono de la tasa por el ejercicio de la potestad jurisdiccional fijada por la Ley 10/2012, de 20 de noviembre, modificada por RDL 3/2013 y Ley 25/2015, de 28 julio, y desarrollada por Orden HAP/2662/2012, de 13 de diciembre, siendo mi representada personas jurídica no exenta de su pago, se acompaña a la presente demanda como documento nº [Nº DE DOCUMENTO] la correspondiente autoliquidación con el ejemplar para la Administración de Justicia debidamente validado y en el que consta el pago de la cantidad de 200 euros correspondiente a la cuota fija [PERIODICIDAD], sin que se incluya la cuota variable prevista en el artículo 7.2 de la Ley 10/2012 al haber sido declarado inconstitucional y nulo por la STC 140/2016, de 21 de julio.

En virtud de lo anterior,

SUPLICO AL TRIBUNAL: que tenga por hecha la anterior manifestación a los efectos pertinentes y por acompañado el documento justificativo del abono de la tasa.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma Abogado Firma Procurador

========================================================================
