---
name: demanda-ejecutiva-reclamar-deudas-garantizadas-prenda-civ-1531
description: "Demanda ejecutiva para reclamar deudas garantizadas con prenda. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda ejecutiva para reclamar deudas garantizadas con prenda

> Formulario **CIV-1531** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda ejecutiva para reclamar deudas garantizadas con prenda» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda ejecutiva para reclamar deudas garantizadas con prenda” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:demanda-ejecutiva-reclamar-deudas-garantizadas-prenda-civ-1531`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (7 veces)
- [ ] FECHA (5 veces)
- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] Nº (5 veces)
- [ ] IMPORTE (4 veces)
- [ ] DESCRIPCIÓN DEL BIEN (3 veces)
- [ ] AÑO (2 veces)
- [ ] DÍA (2 veces)
- [ ] LUGAR (2 veces)
- [ ] MES (2 veces)
- [ ] NOMBRE DEL REPRESENTADO/A (2 veces)
- [ ] AÑOS
- [ ] CUOTAS IMPAGADAS
- [ ] DENOMINACIÓN SOCIAL
- [ ] FINCA
- [ ] FOLIO
- [ ] LIBRO
- [ ] NPA
- [ ] Nº DE DOCUMENTO
- [ ] Nº DE PROTOCOLO
- [ ] OBLIGACIÓN GARANTIZADA
- [ ] SEDE
- [ ] TOMO

## Normas que cita el formulario

- art. 681 LEC
- art. 685.2 LEC
- art. 57 LH
- art. 686.2 LEC
- art. 684.1.4 LEC
- art. 538 LEC
- art. 685 LEC
- art. 688 LEC
- art. 656.1 LEC
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

D/Dª [NOMBRE Y APELLIDOS] Procurador de los Tribunales y de [NOMBRE DEL REPRESENTADO/A], según consta en copia electrónica del poder notarial de representación informática (o digitalizada) que se acompaña (o bien mediante comparecencia Apud Acta) y cuya devolución se interesa una vez testimoniada en autos, bajo la dirección letrada de [NOMBRE Y APELLIDOS], Abogado del Iltre. Colegio de [LOCALIDAD], ante el Tribunal comparezco y como mejor proceda en Derecho DIGO:

Que en la representación que ostento promuevo procedimiento judicial sumario al amparo de lo establecido en el artículo 681 LEC ejercitando la acción referente a los frutos [DESCRIPCIÓN DEL BIEN] que posteriormente se detallarán frente al deudor hipotecario (pasarán a detallarse sus datos identificativos y domicilio), todo ello en base a los siguientes

HECHOS

PRIMERO.- Préstamo Hipotecario.

En fecha [FECHA] mi representada concedió a los demandados un préstamo hipotecario por la suma de [IMPORTE] Euros, según consta en copia simple de la Escritura de constitución de préstamo hipotecario suscrita ante el Notario de [LOCALIDAD] D/Dª [NOMBRE Y APELLIDOS] con el número de protocolo [Nº DE PROTOCOLO] que se aporta como DOCUMENTO NÚM. 1, así como en Nota de inscripción en el Registro de la Propiedad núm. [Nº] de [LOCALIDAD] al Tomo [TOMO], Libro [LIBRO], Folio [FOLIO], finca [FINCA] que se aporta como DOCUMENTO NÚM. 2.

En virtud del referido préstamo los demandados recibían en fecha [FECHA] a su entera satisfacción de mi representada la cantidad de [IMPORTE] Euros, mediante un abono en la cuenta corriente núm. [Nº] de la entidad [DENOMINACIÓN SOCIAL] de la que eran titulares los demandados, reconociéndose deudores del mismo y obligándose a devolverlo y a satisfacer intereses sobre las cantidades pendientes de devolución, todo ello en el modo y condiciones y con las demás obligaciones que se estipularon.

De conformidad a lo dispuesto en el art. 685.2 de la LEC se hace constar que mi representada es gran tenedora de vivienda, pero el inmueble no constituye la vivienda habitual del deudor, al carecer de la condición de vivienda puesto que, tal como se recoge en la escritura, se trata de un local comercial que no reúne las mínimas condiciones de habitabilidad exigidas legalmente.

SEGUNDO.- En el referido préstamo hipotecario en su cláusula segunda constaba que:

«En garantía de la obligación principal de [OBLIGACIÓN GARANTIZADA] y sin perjuicio de la responsabilidad personal, D/Dª [NOMBRE Y APELLIDOS] constituyó prenda sobre (se procede a relacionar además de las circunstancias generales contenidas en la escritura o en la póliza), las especificadas en el artículo 57 LHMPSD, es decir; 1º.-La inscripción de los bienes que se pignoran, con expresión de su naturaleza, cantidad, calidad, estado y demás circunstancias que contribuyan a individualizarlos o identificarlos. 2º.-Determinación, en su caso, del inmueble en que se situaren esos bienes por su origen, aplicación, almacenamiento o depósito. 3º.-La obligación del dueño de conservarlos y de tenerlos a disposición del acreedor, para que éste pueda en cualquier momento inspeccionarlos y comprobar la existencia y estado de los mismos, en la forma pactada o en su defecto, conforme al art. 63. 4º.-Los seguros concertados, con referencia a la póliza correspondiente».

TERCERO.- Si bien por parte del demandado durante los años [AÑOS] se ha producido un cumplimiento de pago puntual de las cuotas hipotecarias, a partir de fecha [FECHA] y por razones que se desconocen, se dejan de abonar las mismas ascendiendo a fecha de hoy la cantidad adeudada a la cantidad de [IMPORTE] Euros, por impago de las siguientes cuotas: [CUOTAS IMPAGADAS].

CUARTO.- Ante dichos incumplimientos manifiestos y reiterados esta parte procedió en fecha [FECHA] a realizar todo tipo de gestiones pertinentes para el cobro de las cantidades adeudas sin éxito. Se aporta requerimiento de pago en el domicilio del deudor efectuado el pasado día [FECHA], cumpliéndose con lo establecido en el artículo 686.2 LEC de la misma manera el requerimiento se ha practicado con al menos diez días de antelación a la presentación de la demanda de ejecución, de acuerdo con el artículo 686.2 LEC en relación con el 581.2 LEC.

No siendo atendido el citado requerimiento, se formula la presente demanda al objeto de lograr el cobro de las cantidades garantizadas y que a continuación pasan a ser detalladas:

A los anteriores hechos le son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

I. COMPETENCIA

De acuerdo con el artículo 684.1.4º LEC la competencia objetiva corresponderá a los Jueces de Instancia de [LOCALIDAD] y la territorial a [LOCALIDAD], por haberse pactado en la escritura aportada como DOCUMENTO NÚM. 1, de acuerdo con lo establecido en el artículo 684.1.4º LEC.

II. PROCEDIMIENTO

Artículo 681 y ss.

III. PARTES Y LEGITIMACIÓN

De acuerdo con el artículo 538 LEC la activa corresponde a mi representado en su calidad de acreedor hipotecario.

Respecto a la legitimación pasiva el artículo 685 LEC establece que corresponderá contra el prestatario en su calidad de deudor hipotecario.

Mi representada es gran tenedora de vivienda, pero el inmueble no tiene la condición de vivienda y, en consecuencia, no puede ser la residencia habitual del deudor.

IV. ACCIÓN

Artículos 681, 682 y 685 LEC.

Artículos 52 y ss. LHMPSD.

Por todo lo expuesto,

SUPLICO AL TRIBUNAL: Tenga por presentado este escrito con sus copias y documentos adjuntos y previo testimonio del poder de representación en autos, se proceda a la devolución del original por ser necesario para otros usos, dándose a las copias el curso legal, teniendo por comparecido y parte en la representación que ostento al Procurador [NOMBRE Y APELLIDOS] en la representación de [NOMBRE DEL REPRESENTADO/A], teniendo por promovido procedimiento judicial sumario de los artículos 681 LEC en relación con el bien [DESCRIPCIÓN DEL BIEN] cuyas características aparecen referenciadas en el expositivo segundo de la presente demanda, propiedad de [NPA], en reclamación de [IMPORTE] Euros que se corresponden con los siguientes conceptos: (capital, intereses, costas). Así y previos los trámites establecidos se proceda a despachar ejecución contra el deudor ejecutado y, en caso de no procederse al pago, se continúe el procedimiento mediante la pública subasta del bien [DESCRIPCIÓN DEL BIEN] Descrito precedentemente, para que con el producto obtenido se proceda a pagar a mi representado de las cantidades que se le adeudan y se liquiden los demás intereses y costas generados por la presente ejecución.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

OTROSÍ DIGO que, de acuerdo con lo establecido en el artículo 688 LEC deberá procederse a la reclamación del Registrador de la Propiedad núm. [Nº] de [LOCALIDAD], la certificación que contenga los extremos a que se refiere el artículo 656.1 LEC y en la que se haga constar que la carga hipotecaria a favor de mi representado se haya subsistente.

Por ello,

SUPLICO AL TRIBUNAL: que se proceda al libramiento del correspondiente mandamiento al Registro de la propiedad núm. [Nº] de [LOCALIDAD] al objeto de que proceda a expedir la certificación establecida en el artículo 688 LEC y se proceda ha realizar anotación marginal en la inscripción de la hipoteca en la que se constate el libramiento de la misma indicando fecha y procedimiento a que está referida.

OTROSÍ DIGO.- Que estando la presente demanda sujeta al abono de la tasa por el ejercicio de la potestad jurisdiccional fijada por la Ley 10/2012, de 20 de noviembre, modificada por RDL 3/2013 y Ley 25/2015, de 28 julio, y desarrollada por Orden HAP/2662/2012, de 13 de diciembre, siendo mi representada personas jurídica no exenta de su pago, se acompaña a la presente demanda como documento nº [Nº DE DOCUMENTO] la correspondiente autoliquidación con el ejemplar para la Administración de Justicia debidamente validado y en el que consta el pago de la cantidad de 200 euros correspondiente a la cuota fija, sin que se incluya la cuota variable prevista en el artículo 7.2 de la Ley 10/2012 al haber sido declarado inconstitucional y nulo por la STC 140/2016, de 21 de julio.

En virtud de lo anterior,

SUPLICO AL TRIBUNAL: que tenga por hecha la anterior manifestación a los efectos pertinentes y por acompañado el documento justificativo del abono de la tasa.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

========================================================================
