---
name: demanda-ejecucion-hipotecaria-sobre-inmueble-civ-1484
description: "Demanda de ejecución hipotecaria sobre un inmueble. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de ejecución hipotecaria sobre un inmueble

> Formulario **CIV-1484** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de ejecución hipotecaria sobre un inmueble» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de ejecución hipotecaria sobre un inmueble” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:demanda-ejecucion-hipotecaria-sobre-inmueble-civ-1484`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (12 veces)
- [ ] Nº (10 veces)
- [ ] FECHA (8 veces)
- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] NÚMERO (7 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] AÑO (4 veces)
- [ ] MES (3 veces)
- [ ] Nº DE CLÁUSULA (3 veces)
- [ ] SEDE (3 veces)
- [ ] Nº DE COLEGIADO/A (2 veces)
- [ ] AÑOS (PERIODO)
- [ ] COLEGIO
- [ ] CUOTAS IMPAGADAS
- [ ] DENOMINACIÓN SOCIAL
- [ ] DESCRIPCIÓN DEL BIEN
- [ ] DOMICILIO
- [ ] DÍA
- [ ] FINCA
- [ ] FOLIO
- [ ] LIBRO
- [ ] LUGAR
- [ ] NOMBRE DE LA PARTE
- [ ] Nº DE DOCUMENTO
- [ ] Nº DE PROTOCOLO
- [ ] OTROS DATOS
- [ ] SUCURSAL
- [ ] TOMO

## Normas que cita el formulario

- art. 681 LEC
- art. 575 LEC
- art. 684.1.1 LEC
- art. 85.1 LOPJ
- art. 129 LH
- art. 682.2 LEC
- art. 682.3 LEC
- art. 538 LEC
- art. 1876 CC
- art. 104 LH
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

### Avisos de actualización (3) — se aplican en el texto, nunca se copian en el documento

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).
- Junto a «…Iltre. Colegio de Abogados de [COLEGIO], ante el Tribunal de Instancia de [SEDE]»: Un solo TI por partido judicial (art. 84.1 LOPJ): sobra «de los de». Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

Don/Doña [NOMBRE Y APELLIDOS] Procurador de los Tribunales, en nombre y representación de don/doña [NOMBRE Y APELLIDOS], según acredito mediante apoderamiento apud acta otorgado ante el Letrado de la Administración de Justicia de la Oficina de [SUCURSAL] que acompaño, bajo la dirección Letrada de [NOMBRE Y APELLIDOS], Abogado colegiado núm [Nº DE COLEGIADO/A] del Iltre. Colegio de Abogados de [COLEGIO], ante el Tribunal de Instancia de [SEDE] que por turno de reparto corresponda comparezco y, como mejor proceda en Derecho, DIGO:

Que en la indicada representación, y siguiendo instrucciones de mi mandante, por medio del presente escrito promuevo DEMANDA DE EJECUCIÓN BIENES HIPOTECADOS al amparo de los artículos 681 y ss de la LEC contra el deudor hipotecario [NOMBRE Y APELLIDOS] la cual baso en los siguientes

PRIMERO.- HECHOS

Préstamo hipotecario

Que en fecha [FECHA] mi representada concedió a los demandados un préstamo hipotecario por la suma de [IMPORTE] euros, según consta en copia simple de la escritura de constitución de préstamo hipotecario suscrita ante el Notario de la localidad de [LOCALIDAD], don/doña [NOMBRE Y APELLIDOS] con el número de protocolo [Nº DE PROTOCOLO] de año [AÑO] que se aporta como DOCUMENTO Nº 1, así como en Nota de inscripción en el Registro de la Propiedad núm [NÚMERO] de [LOCALIDAD] al Tomo [TOMO], Libro [LIBRO], Folio [FOLIO], finca [FINCA], que se aporta como DOCUMENTO Nº 2.

Que en virtud del referido préstamo los demandados recibían en fecha [FECHA] a su entera satisfacción de mi representada la cantidad de [IMPORTE] euros, mediante un abono en la cuenta corriente núm [NÚMERO] de la entidad [DENOMINACIÓN SOCIAL] de la que eran titulares los demandados, reconociéndose deudores del mismo y obligándose a devolverlo y a satisfacer intereses sobre las cantidades pendientes de devolución, todo ello en el modo y condiciones y con las demás obligaciones que se estipularon.

SEGUNDO.- CLÁUSULAS

A) AMORTIZACIÓN.

En el referido préstamo hipotecario consta en el EXPOSITIVO SEGUNDO, relativo a la AMORTIZACIÓN que:

"La parte prestataria se obligaba solidariamente a devolver el principal del préstamo y a satisfacer los intereses pactados en la estipulación PRIMERA en el plazo de [Nº] meses, contados desde el día uno del mes siguiente a esta fecha mediante el pago de cuotas fijas mensuales vencidas comprensivas de capital e intereses por importe, inicialmente de [IMPORTE] euros calculada al tipo inicialmente previsto. Los vencimientos serán el día uno de cada mes, siendo el primer vencimiento con fecha [FECHA] y el último con fecha [FECHA].

Excepcionalmente, el primer día del segundo mes siguiente a esta fecha, es decir, el día del vencimiento de la primera cuota, vencerán también y deberán satisfacer los intereses devengados desde el día de la firma al último del mes, calculados al tipo inicial pactado y conforme al primer párrafo de la cláusula tercera".

B) GARANTÍA HIPOTECARIA.

En el referido préstamo hipotecario consta en el EXPOSITIVO [Nº], relativo a la GARANTÍA HIPOTECARIA que:

"La finca objeto de hipoteca [DESCRIPCIÓN DEL BIEN] (se procederá a su descripción: cabida, cuota, título, cargas, situación arrendaticia etc.).

La ejecución de este préstamo podrá realizarse por el banco acreedor por cualquiera de los procedimientos establecidos en la Ley 1/2000, de 7 de enero, de Enjuiciamiento Civil, especialmente en sus artículos 517, 520, 549, 550, 572, 573 y 574.

Se fija como domicilio de la parte prestataria a efectos de requerimientos y notificaciones la finca que se hipoteca.

Se establece como precio en que los interesados tasan la finca la cantidad de [IMPORTE] euros, según tasación realizada conforme al Real Decreto 716/2009, de 24 de abril, por el que se desarrollan determinados aspectos de la Ley 2/1981, de 25 de marzo, de regulación del mercado hipotecario y otras normas del sistema hipotecario y financiero".

C) INTERESES.

En el referido préstamo hipotecario consta en el EXPOSITIVO [Nº], relativo a la INTERESES que:

"La cantidad prestada desde esta fecha a favor del banco el interés nominal inicial será del [Nº] por ciento anual, pagadero de la forma que se indica en la estipulación segunda".

La fórmula utilizada para obtener, a partir del tipo de interés nominal, el importe de los intereses devengados diariamente es la siguiente:

I= C. r. d/36000

Siendo:

C= capital pendiente de amortizar.

R= nominal anual pactado.

I= interés del recibo.

D= tiempo en días efectivamente transcurridos.

D) INTERÉS VARIABLE.

En el referido préstamo hipotecario consta en el EXPOSITIVO [Nº], relativo al TIPO INTERÉS VARIABLE que:

"El interés que debe pagar la parte prestataria en los vencimientos periódicos hasta el día [FECHA] del mes [MES], del año [AÑO], será el tipo inicialmente pactado.

A partir del día [FECHA] del mes [MES], del año [AÑO] y sucesivamente con periodicidad semestral durante toda la vida del préstamo, el tipo de interés a pagar por el prestatario será revisado al alza o a la baja, tomándose como índice la referencia interbancaria a un año (euríbor), índice de referencia oficial para los préstamos hipotecarios, a tipo variable, destinados a la adquisición de vivienda, que con periodicidad mensual se publica en el BOE.

El índice aplicable será el que corresponda al último publicado en la fecha en la que vaya a realizarse la revisión. Para la realización de estos cálculos, no se efectuará en los índices de referencia ningún ajuste o conversión, aún cuando dichos índices correspondan a operaciones cuya periodicidad de pagos será distinta a la de los vencimientos pactados en esta escritura o incluya conceptos que estén previstos como concepto independiente en el préstamo objeto de este contrato.

Para determinar el tipo de interés aplicable, al índice de referencia se le adicionará un diferencial de [Nº] puntos".

E) INTERESES DE DEMORA.

En el referido préstamo hipotecario consta en el EXPOSITIVO [Nº], relativo al INTERESES DE DEMORA que:

"Las cantidades no satisfechas por la parte prestataria a su vencimiento devengarán a favor del banco el interés de demora, que será superior en [Nº] puntos porcentuales al tipo de interés anual ordinario que corresponda en cada momento, sin necesidad de requerimiento alguno y pagadero en su caso al hacerse efectivo cualquier concepto vencido e impagado, gozando este devengo de preferencia frente a los demás".

La fórmula utilizada para obtener los intereses de demora es la siguiente:

D= B.r.t/36000

Siendo:

B= base de devengo (capital más intereses del recibo vencido).

r= tipo de interés de demora.

D= demora percibida.

t=tiempo en días efectivamente transcurridos.

F) RESOLUCIÓN ANTICIPADA.

En el referido préstamo hipotecario consta en el EXPOSITIVO [Nº], relativo a la RESOLUCIÓN ANTICIPADA que:

"El banco podrá declarar vencida la obligación y proceder contra la finca hipotecada y simultáneamente contra la parte prestataria si se incumplieran por la misma cualquiera de las obligaciones contraídas y especialmente en los siguientes casos:

a) Por causas generales establecidas en la ley.

b) Por falta de pago en sus vencimientos de una parte cualquiera del capital del préstamo o de sus intereses, salvo lo que establezca la legislación vigente".

En el referido contrato de garantía hipotecaria constan una serie de cuestiones a las que se debe hacer mención:

a) La cláusula núm [NÚMERO] señala que "el domicilio fijado por el deudor a los efectos de práctica de requerimientos y notificaciones es " [DOMICILIO].

b) La cláusula núm [NÚMERO] señala que "a los efectos del ejercicio de la acción hipotecaria directa contra el inmueble sobre el que se constituye la garantía hipotecaria, las partes proceden a darle un valor de tasación, de acuerdo con la valoración que del mismo ha realizado el arquitecto técnico don/doña [NOMBRE Y APELLIDOS], perteneciente al Colegio de arquitectos técnicos de [LOCALIDAD], colegiado núm [Nº DE COLEGIADO/A], en la cantidad de [IMPORTE] euros, precio que servirá como tipo para la eventual subasta.

c) La cláusula núm [NÚMERO] determina que "producido el impago de cualquiera de las cantidades del préstamo hipotecario".

TERCERO.- IMPAGO CUOTAS.

Que si bien por parte del demandado durante los años [AÑOS (PERIODO)] se ha producido un cumplimiento de pago puntual de las cuotas hipotecarias, a partir de fecha [FECHA] y por razones que se desconocen, se dejan de abonar las mismas ascendiendo a fecha de hoy la cantidad adeudada a la cantidad de [IMPORTE] euros, por impago de las siguientes cuotas: [CUOTAS IMPAGADAS]. Ante dichos incumplimientos manifiestos y reiterados esta parte procedió en fecha [FECHA] a realizar todo tipo de gestiones pertinentes para el cobro de las cantidades adeudas sin éxito.

CUARTO.- DEUDA RECLAMADA.

La deuda que se reclama asciende a [IMPORTE] euros, que se corresponden con el principal de la deuda que asciende a [IMPORTE] euros y con los intereses devengados, de acuerdo con las cláusula [Nº DE CLÁUSULA] y la cláusula [Nº DE CLÁUSULA], ambas del referido préstamo hipotecario. A esta cantidad deberá añadírsele la cantidad de [IMPORTE] euros correspondientes a los intereses de demora, de acuerdo con la cláusula [Nº DE CLÁUSULA], así como las costas que se generen en esta ejecución, de acuerdo con lo establecido en el artículo 575 de la LEC.

Igualmente se solicita que la ejecución sea dirigida de forma exclusiva contra el bien hipotecado sin que esta petición afecte a la posibilidad de que se pueda solicitar y conceder que se despache ejecución por una cantidad mayor que la garantizada con la hipoteca.

A los anteriores hechos le son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

Se tienen por reproducidos los preceptos legales alegados en el cuerpo del presente escrito.

Competencia

En referencia a la competencia, lo será la Sección Civil del Tribunal de Instancia de [SEDE] por ser ésta la localidad en la que radica el bien hipotecado objeto de este procedimiento de ejecución, de acuerdo con lo establecido en el artículo 684.1.1º de la LEC, en relación con lo dispuesto en el art. 85.1º LOPJ.

Procedimiento

El procedimiento aplicable, es el previsto en los artículos 129 y 130 LH y 681 y ss LEC, por tratarse de le ejecución directa y exclusiva de un bien hipotecado, y se han cumplido las condiciones establecidas en el artículo 682.2 de la LEC referidas a la fijación en la escritura de constitución de la hipoteca tanto del precio que servirá de tipo a la subasta en su caso como del domicilio del deudor a efectos de requerimientos y notificaciones, quedando constancia registral de ambas circunstancias conforme al artículo 682.3 de la LEC.

Legitimación

Legitimado activamente se encuentra mi representado por ser el acreedor de la deuda garantizada con hipoteca (art. 538 de la LEC).

La legitimación pasiva corresponde a los demandados por ser las personas que figuran como deudores y ser los copropietarios del bien hipotecado.

Derecho sustantivo

En cuanto a los fundamentos sustantivos, serán de aplicación los artículos 1876 y ss CC, así como los artículos 104 y 105 de la LH de los cuales resulta que la hipoteca sujeta directa e indirectamente los bienes sobre los que se impone, con independencia de quien sea su poseedor, al cumplimiento de la obligación para la que fue constituida.

Costas

Sobre costas, será de aplicación lo dispuesto en los artículos 394, 539.2 y 583.2 de la LEC.

Por lo expuesto,

SUPLICO AL TRIBUNAL: Que tenga por presentado este escrito, lo admita a trámite y, en su virtud, me tenga por comparecido y parte en la representación que ostento de [NOMBRE DE LA PARTE], teniendo por promovida DEMANDA DE EJECUCIÓN HIPOTECARIA frente a D/Dª [NOMBRE Y APELLIDOS], al objeto de exigir el pago de la deuda garantizada con el bien hipotecado y que asciende a la cantidad de [IMPORTE] euros (principal más intereses ordinarios), más [IMPORTE] euros en concepto de intereses moratorios, más la cantidad de [IMPORTE] euros para cubrir el resto de intereses de demora y las costas generadas por este procedimiento; y previos los trámites con arreglo a derecho se proceda a despachar ejecución contra el deudor ejecutado y, en caso de no procederse al pago, se continúe el procedimiento mediante la pública subasta del bien hipotecado, para que con el producto obtenido se proceda a pagar a mi representado las cantidades que se le adeudan y se liquiden los demás intereses y costas generados por la presente ejecución.

OTROSÍ DIGO: Que de acuerdo con lo establecido en el artículo 688 de la LEC deberá procederse a la reclamación del Registrador de la Propiedad núm [NÚMERO] de [LOCALIDAD], la certificación que contenga los extremos a que se refiere el artículo 656.1 de la LEC y en la que se haga constar que la carga hipotecaria a favor de mi representado se haya subsistente.

Por ello,

SUPLICO AL TRIBUNAL: Que se proceda al libramiento del correspondiente mandamiento al Registro de la Propiedad núm [NÚMERO] de [LOCALIDAD], al objeto de que proceda a expedir la certificación establecida en el artículo 688 de la LEC y se proceda a realizar anotación marginal en la inscripción de la hipoteca, en la que se constate el libramiento de la misma indicando fecha y procedimiento a que está referida.

OTROSÍ DIGO.- Que estando la presente demanda sujeta al abono de la tasa por el ejercicio de la potestad jurisdiccional fijada por la Ley 10/2012, de 20 de noviembre, modificada por RDL 3/2013 y Ley 25/2015, de 28 julio, y desarrollada por Orden HAP/2662/2012, de 13 de diciembre, siendo mi representada personas jurídica no exenta de su pago, se acompaña a la presente demanda como documento nº [Nº DE DOCUMENTO] la correspondiente autoliquidación con el ejemplar para la Administración de Justicia debidamente validado y en el que consta el pago de la cantidad de 200 euros correspondiente a la cuota fija [OTROS DATOS], sin que se incluya la cuota variable prevista en el artículo 7.2 de la Ley 10/2012 al haber sido declarado inconstitucional y nulo por la STC 140/2016, de 21 de julio.

En virtud de lo anterior,

SUPLICO AL TRIBUNAL: que tenga por hecha la anterior manifestación a los efectos pertinentes y por acompañado el documento justificativo del abono de la tasa.

Es Justicia que insto en [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma de abogado y procurador

========================================================================
