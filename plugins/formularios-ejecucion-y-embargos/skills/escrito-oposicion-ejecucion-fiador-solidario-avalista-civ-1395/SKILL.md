---
name: escrito-oposicion-ejecucion-fiador-solidario-avalista-civ-1395
description: "Escrito de oposición a la ejecución del fiador solidario o avalista. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito de oposición a la ejecución del fiador solidario o avalista

> Formulario **CIV-1395** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Escrito de oposición a la ejecución por defectos procesales: carecer el ejecutado del carácter o representación con que se le demanda. Póliza mercantil en la que interviene un fiador solidario -ejecutado- que se opone a la demanda ejecutiva porque la póliza de crédito que sirve como título al efecto quedó extinguida al ser sustituida por otra nueva póliza de crédito en la que no se prestó el aval.

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito de oposición a la ejecución del fiador solidario o avalista» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito de oposición a la ejecución del fiador solidario o avalista” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:escrito-oposicion-ejecucion-fiador-solidario-avalista-civ-1395`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (11 veces)
- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] NÚMERO (4 veces)
- [ ] NOMBRE DE LA PARTE (3 veces)
- [ ] IMPORTE (2 veces)
- [ ] BENEFICIARIO
- [ ] COLEGIO
- [ ] CORREO ELECTRÓNICO
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] NOMBRE DEL SOLICITANTE
- [ ] Nº DE FAX
- [ ] SEDE
- [ ] TELÉFONO

## Normas que cita el formulario

- art. 1.204 CC
- art. 559.1.1.º LEC
- art. 1822 CC
- art. 559.2 LEC

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

Notas al pie del formulario original:
(1) La oposición al despacho de ejecución fundado en un título ejecutivo no judicial -como en definitiva es el supuesto objeto del presente formulario-, única y exclusivamente puede fundarse, bien en la concurrencia de alguno de los defectos procesales expresamente enumerados en el art. 559.1 LEC; bien, por motivos de fondo, en alguna de las causas taxativamente enumeradas en el art. 557.1 de la misma Ley.

En este punto, debe tenerse presente que la limitación de las causas de oposición a la ejecución fundada en títulos no judiciales pretende evitar -como expresamente se señala en la propia Exposición de Motivos de la Ley de Enjuiciamiento Civil- que se "convierta la oposición a la ejecución en una controversia semejante a la de un juicio declarativo plenario, con lo que podría frustrarse la tutela jurisdiccional ejecutiva". Y la razón de ello se encuentra -como en la propia Exposición de Motivos se explicita- en que se entienden "...los títulos ejecutivos extrajudiciales, no como un tercer género entre las sentencias y los documentos que sólo sirven como medios de prueba, sino como genuinos títulos ejecutivos, esto es, instrumentos que, por poseer ciertas características, permiten al Derecho considerarlos fundamento razonable de la certeza de una deuda, a los efectos del despacho de una verdadera ejecución forzosa...".

En el presente caso, la ejecutada sustenta su oposición en el motivo contemplado en el art. 559.1.1.º LEC ("...Carecer el ejecutado del carácter o representación con que se le demanda..."). Motivo que viene referido, en definitiva, a la legitimación del ejecutado para ser sujeto o parte pasiva del proceso de ejecución, conforme al título que le sirve de fundamento.

Carecer del carácter supone que se ha despachado ejecución contra quien no tiene legitimación, por la que el afectado (ejecutado) podrá alegar que no es él quien debe soportar la ejecución forzosa.

Desde esta perspectiva, ha de recordarse que, conforme a lo establecido por el art. 538.2 LEC, la ejecución únicamente puede despacharse:

1.º Frente a quien aparezca como deudor en el mismo título.

2.º Frente a quien, sin figurar como deudor en el título ejecutivo, responsa personalmente de la deuda por disposición legal o en virtud de afianzamiento acreditado mediante documento público.

3.º Frente a quien, sin figurar como deudor en el título ejecutivo, resulte ser propietario de los bienes especialmente afectos al pago de la deuda en cuya virtud se procede, siempre que tal afección derive de la Ley o se acredite mediante documento fehaciente.

Lo normal es que la demanda ejecutiva se dirija y la ejecución se despache contra quien figura en el título (art. 538.2.1.º LEC). Como la legitimación se deriva del título ejecutivo, sólo cabe la falta de carácter cuando no se es la persona a la que el título se refiere.

Cabe la posibilidad de que se despache ejecución contra persona ajena -"sin figurar como deudor en el título"- porque debe responder personalmente de la deuda por disposición legal o en virtud de afianzamiento mediante documento público (art. 538.2.2.º LEC).

La referencia a "disposición legal" no permite comprender aquellos supuestos en que la declaración de responsabilidad exige una declaración judicial en juicio contradictorio.

En cuanto al afianzamiento, para que proceda despachar ejecución contra el fiador es preciso que conste en documento público. El fiador podrá oponer, aparte de no tener el carácter de tal, y la no constancia en documento público, la extinción de la deuda o de la fianza, o la inexigibilidad de ésta.


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

D./Dña. [NOMBRE Y APELLIDOS], procurador/a de los Tribunales, actuando en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS], según acredito mediante escritura pública de poderes que solicito, una vez incorporada por copia en autos, me sea devuelta por precisarla para otros usos, ante el Tribunal comparezco bajo la dirección de D./Dña. [NOMBRE Y APELLIDOS], abogado/a colegiado n.º [NÚMERO] del Ilustre Colegio de Abogados de [COLEGIO], con despacho profesional abierto en [LOCALIDAD], teléfono [TELÉFONO], fax [Nº DE FAX], e-mail [CORREO ELECTRÓNICO], y como mejor proceda en derecho DIGO:

Que en nombre de mi poderdante me persono en los autos de ejecución seguidos a instancia de [NOMBRE DEL SOLICITANTE] y registrados con el número [NÚMERO], y por medio del presente escrito, dentro del término de diez días concedido al efecto, formulo OPOSICIÓN a la citada ejecución, dentro del plazo concedido al efecto, en virtud de los siguientes:

HECHOS

ÚNICO.-

Por auto de fecha [FECHA] se despachó ejecución contra mi mandante en reclamación del pago del importe de [IMPORTE] euros, más intereses y costas, con fundamento en una póliza de crédito concertada entre [NOMBRE DE LA PARTE] y [NOMBRE DE LA PARTE] con el aval solidario de D./Dña. [NOMBRE Y APELLIDOS], contra el que se dirige la acción, auto que le fue notificado el pasado día [FECHA].

Se aporta como documento n.º [NÚMERO] la póliza de crédito suscrita entre las citadas partes, e intervenida por Corredor de Comercio colegiado, de fecha [FECHA].

Pero obvia la ejecutante que la póliza de crédito que sirve como título al efecto quedó extinguida por mutuo acuerdo de las partes al ser sustituida por otra nueva póliza de crédito de fecha [FECHA], con idéntico contenido, en la que no se prestó el aval.

En virtud de la primera, de fecha [FECHA], [NOMBRE DE LA PARTE] abría un crédito de duración indefinida a favor de [BENEFICIARIO] hasta un límite máximo de [IMPORTE] euros que se haría efectivo para todo tipo de operación de comercio exterior mediante descuento o cualquier negociación de efectos, préstamos para financiación de capital circulante, así como cualquier operación de comercio exterior o de otro tipo, que realizara el acreditado con el banco. Por lo tanto, estamos ante un contrato de una naturaleza similar al de apertura de crédito en cuenta corriente.

El segundo contrato, de fecha [FECHA] tiene el mismo contenido y no hay ninguna mención a su acumulación al anterior, por lo que el banco se obliga a prestar su garantía y crédito a las operaciones producidas a partir de la misma. En consecuencia, y de acuerdo a la voluntad de las partes declarada por escrito, las operaciones se imputan a esta segunda póliza, que sustituye a la anterior y el crédito derivado no estaba garantizado por el demandado.

Estamos pues ante una novación extintiva por la que la anterior póliza de fecha [FECHA] fue sustituida por otra posterior de fecha [FECHA], a cuya justificación se acompaña como documento n.º [NÚMERO].

FUNDAMENTOS DE DERECHO

I.- Con carácter preliminar, negamos que sean de aplicación al presente caso los fundamentos de derecho alegados por el ejecutante.

II.- La novación que se pretende es una forma de extinción de las obligaciones mediante un contrato que deja sin efecto el anterior y pasa a crear una relación jurídica que la reemplaza. Tal efecto puede establecerse, por declaración expresa, o a través de una incompatibilidad de obligaciones (art. 1.204 CCiv) que implica una novación tácita, que es lo que se produce en este caso.

Es posible que la voluntad interna de la entidad bancaria fuera otra, pero hay que estar a la voluntad declarada de forma inequívoca con la firma de la segunda póliza con la que la primera es totalmente incompatible, por lo que se practicó una novación extintiva.

III.- El art. 559.1.1.º LEC dispone que el ejecutado podrá oponerse a la ejecución por carecer el ejecutado del carácter o representación con que se le demanda, defecto que se da en el presente caso.

En efecto, del contenido de los contratos se deduce la novación extintiva de la póliza avalada por el demandado que no puede extenderse sin su consentimiento expreso a la pactada en su sustitución, habida cuenta de los limites subjetivos de la eficacia de lo pactado (res inter alios acta), sin trascendencia a quien no ha sido parte en el contrato, y la accesoriedad de la fianza (ex art. 1822 CCiv).

IV.- En materia de costas procesales, a tenor de lo preceptuado en el art. 559.2, párrafo segundo LEC, deberán ser impuestas al ejecutante.

En virtud de todo lo expuesto,

SUPLICO AL TRIBUNAL:

Que tenga por presentado este escrito con sus copias y me tenga por comparecido y parte en la representación que ostento de D./Dña. [NOMBRE Y APELLIDOS] en el expresado procedimiento de ejecución y mandar que se entiendan conmigo las actuaciones que a partir de este momento se realicen, teniendo por formulada en tiempo y forma oposición a la ejecución despachada para que, tras la correspondiente tramitación, se dicte auto dejando sin efecto la ejecución despachada por auto de fecha [FECHA] y alce los embargos y medidas de garantía de la afección adoptadas en decreto de fecha [FECHA] con expresa imposición de las costas de la ejecución al ejecutante.

OTROSÍ DIGO: Que siendo el poder que acompaño general para pleitos y necesitándolo para otros usos procesales.

SUPLICO AL TRIBUNAL: Que previo su inserción por copia en autos, acuerde su desglose y devolución a esta parte.

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a
