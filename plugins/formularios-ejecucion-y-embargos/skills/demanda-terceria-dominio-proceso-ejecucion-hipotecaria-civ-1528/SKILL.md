---
name: demanda-terceria-dominio-proceso-ejecucion-hipotecaria-civ-1528
description: "Demanda de tercería de dominio en un proceso de ejecución hipotecaria. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de tercería de dominio en un proceso de ejecución hipotecaria

> Formulario **CIV-1528** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de tercería de dominio en un proceso de ejecución hipotecaria» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de tercería de dominio en un proceso de ejecución hipotecaria” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:demanda-terceria-dominio-proceso-ejecucion-hipotecaria-civ-1528`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NPA (4 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] Nº DE PROCEDIMIENTO (3 veces)
- [ ] Nº (2 veces)
- [ ] AÑO
- [ ] COLEGIO
- [ ] DESCRIPCIÓN DEL BIEN
- [ ] DÍA
- [ ] FECHA
- [ ] FINCA
- [ ] FOLIO
- [ ] LIBRO
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] MES
- [ ] Nº DE COLEGIADO
- [ ] Nº DE DOCUMENTO
- [ ] PARTE DEMANDADA
- [ ] SEDE
- [ ] TOMO
- [ ] ÓRGANO

## Normas que cita el formulario

- art. 696 LEC
- art. 596 LEC
- art. 599 LEC
- art. 595 LEC
- art. 600 LEC
- art. 5 Ley Orgánica 1/2025
- art. 593 LEC
- art. 1 LEC
- art. 313 LH
- art. 603.2 LEC

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

- Junto a «…DIMIENTO] A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
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

PROCEDIMIENTO DE EJECUCIÓN HIPOTECARIA Nº [Nº DE PROCEDIMIENTO]

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

D/Dª [NOMBRE Y APELLIDOS] Procurador de los Tribunales y de D/Dª [NOMBRE Y APELLIDOS], tal y como consta debidamente acreditado en la copia electrónica del poder notarial de representación informática (o digitalizada) que se acompaña, bajo la dirección Letrada de D/Dª [NOMBRE Y APELLIDOS], Colegiado/a [Nº DE COLEGIADO] en el Iltre. Colegio de Abogados de [COLEGIO], ante este Tribunal comparezco y como mejor proceda en Derecho, DIGO:

Que siguiendo instrucciones de mi mandante, por medio del presente escrito interpongo demanda de tercería de dominio en el procedimiento de ejecución hipotecaria al margen referenciado, todo ello al amparo de los artículos 594 y ss. y 696 LEC, contra las partes ejecutante [ÓRGANO] y ejecutada [NPA], en base a los siguientes

HECHOS

PRIMERO.- En fecha [FECHA] esta parte ha tenido constancia de que se sigue procedimiento de ejecución hipotecaria [Nº DE PROCEDIMIENTO] en relación con el inmueble [DESCRIPCIÓN DEL BIEN], inscrito en el Registro de la Propiedad núm. [Nº] de [LOCALIDAD] al Tomo [TOMO], libro [LIBRO], folio [FOLIO], finca [FINCA].

SEGUNDO.- El referido inmueble no es propiedad del deudor ejecutado, sino de mi mandante. Al amparo del contenido del artículo 696 LEC se aporta como DOCUMENTO NÚM. 1 copia simple de escritura pública Notarial de fecha anterior a la constitución de la garantía hipotecaria sobre dicho inmueble, así como DOCUMENTO NÚM. 2 certificación registral de vigencia del asiento de dominio a favor de mi mandante.

TERCERO.- La situación concurrente deviene como consecuencia de una doble inmatriculación del referido inmueble la que ha posibilitado la constitución de la hipoteca sobre él.

CUARTO.- La presente demanda de tercería de dominio se, interpone de acuerdo con lo establecido en el apartado 2 del artículo 596 LEC con anterioridad al momento en que se produzca la transmisión del bien al acreedor o al tercero que lo adquiera en pública subasta.

A los anteriores hechos le son de aplicación los siguientes

QUINTO.- Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento nº [Nº DE DOCUMENTO]

FUNDAMENTOS DE DERECHO

I. COMPETENCIA Y PROCEDIMIENTO

El órgano al que nos dirigimos es competente en base a lo establecido en el artículo 599 LEC por ser el que se encuentra conociendo del procedimiento de ejecución hipotecaria.

El procedimiento a seguir, de acuerdo con lo establecido en el artículo 599 LEC es el juicio declarativo ordinario.

II. LEGITIMACIÓN

Mi mandante se encuentra legitimado activamente en cuanto es propietario del inmueble objeto del presente procedimiento conforme con lo establecido en el artículo 595 LEC.

De acuerdo con el párrafo 1º del artículo 600 LEC la legitimación pasiva corresponde a [NPA] y a [NPA], que respectivamente son ejecutante y ejecutado en el procedimiento de ejecución hipotecaria.

III. MOMENTO HÁBIL PARA LA PRESENTACIÓN DE LA DEMANDA

El artículo 596 LEC establece como dies a quo para la presentación aquel en que se verifica la traba y dies ad quem antes de la adjudicación en pago y entrega al ejecutante.

CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

V. PROPIEDAD DEL INMUEBLE EJECUTADO

El artículo 696 LEC determina la aportación con la demanda de la certificación de dominio anterior a la hipoteca, certificación de la inscripción registral a favor del tercerista y certificación de vigencia, es decir de no extinción ni cancelación registral del asiento de dominio, documentos que han sido adjuntados a la presente demanda.

Por aplicación analógica de los artículos 593 y 594 LEC esta situación es contraria a la ley.

VI. PROTECCIÓN REGISTRAL

Los artículos 1 y 38 LEC protegen a mi mandante, titular registral del inmueble objeto de ejecución. Dicha protección opera a pasar de la doble inmatriculación respecto de la cual, de acuerdo con lo establecido en el artículo 313 LH se han activado las acciones legales para su eliminación.

VII. COSTAS

Se impondrán a la parte demandada de conformidad con lo establecido en el artículo 603.2 LEC.

Por todo ello,

AL TRIBUNAL SUPLICO: Tenga por presentado este escrito, lo admita a trámite, teniendo por formulada, en tiempo y forma, demanda de tercería de dominio contra [PARTE DEMANDADA] y [NPA], ejecutante y ejecutado en el procedimiento de ejecución hipotecaria [Nº DE PROCEDIMIENTO]. Se tenga a esta parte por personada en nombre de mi mandante y tras la tramitación legalmente establecida, previo traslado a los demandados, se proceda a dictar auto en el que se determine la pertenencia del bien a mi representado y la imposibilidad de continuar con el procedimiento de ejecución hipotecaria, con imposición de costas a los demandados.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma de Abogado y de Procurador.

========================================================================
