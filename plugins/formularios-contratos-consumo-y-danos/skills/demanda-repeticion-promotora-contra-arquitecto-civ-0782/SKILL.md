---
name: demanda-repeticion-promotora-contra-arquitecto-civ-0782
description: "Demanda de repetición de la promotora contra arquitecto, aparejador y constructora de la edificación. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de repetición de la promotora contra arquitecto, aparejador y constructora de la edificación

> Formulario **CIV-0782** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio ordinario por la que el promotor de un edificio, condenado en un procedimiento anterior por defectos constructivos a favor de la comunidad de propietarios, ejerce la acción de repetición o regreso (art. 1.145 del Código Civil) contra el arquitecto, el aparejador y la constructora que intervinieron en la obra y no fueron demandados por la comunidad.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de repetición de la promotora contra arquitecto, aparejador y constructora de la edificación» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de repetición de la promotora contra arquitecto, aparejador y constructora de la edificación” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:demanda-repeticion-promotora-contra-arquitecto-civ-0782`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (16 veces)
- [ ] FECHA (13 veces)
- [ ] IMPORTE (10 veces)
- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] FECHAS (5 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] DENOMINACIÓN SOCIAL (4 veces)
- [ ] DOMICILIO (4 veces)
- [ ] SEDE (4 veces)
- [ ] CALLE (3 veces)
- [ ] CAUSA 1 (3 veces)
- [ ] CAUSA 2 (3 veces)
- [ ] CAUSA 3 (3 veces)
- [ ] CAUSA 4 (3 veces)
- [ ] Nº DE PROCEDIMIENTO (3 veces)
- [ ] CORREO ELECTRÓNICO (2 veces)
- [ ] DENOMINACIÓN SOCIAL DE LA CONSTRUCTORA (2 veces)
- [ ] DENOMINACIÓN SOCIAL DEL PROMOTOR (2 veces)
- [ ] DOMICILIO PROFESIONAL (2 veces)
- [ ] IMPORTE TOTAL (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL APAREJADOR (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL ARQUITECTO (2 veces)
- [ ] TELÉFONO (2 veces)
- [ ] AÑO
- [ ] DENOMINACIÓN DE LA COMUNIDAD
- [ ] DESCRIPCIÓN DE LA OBRA
- [ ] DOMICILIO DEL EDIFICIO
- [ ] DOMICILIO SOCIAL
- [ ] DÍA
- [ ] FECHA DE LA LICENCIA
- [ ] MES
- [ ] MES Y AÑO DE FIN
- [ ] MES Y AÑO DE INICIO
- [ ] NOMBRE DEL NOTARIO
- [ ] NOMBRE Y APELLIDOS DEL ABOGADO/A
- [ ] NOMBRE Y APELLIDOS DEL PERITO
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] NOMBRE Y APELLIDOS, Nº DE COLEGIADO
- [ ] Nº DE COLEGIADO
- [ ] Nº DE PROTOCOLO

## Normas que cita el formulario

- art. 399.1 LEC
- art. 9.2 LOPJ
- art. 5 LEC
- art. 45 LEC
- art. 249.2 LEC
- art. 10 LEC
- art. 253.1 LEC
- art. 23 LEC
- art. 5 Ley Orgánica 1/2025
- art. 1.145 Código Civil
- art. 1.591 Código Civil
- art. 1.964 Código Civil
- art. 576 LEC
- art. 394.1 LEC
- art. 24.2 LEC
- art. 155.3 LEC

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…e abril de 1994, de 20 de julio de 2002 o de 27 de octubre de 2003, entre otras.»: tras la Ley 42/2015, el art. 1.964 del Código Civil fija en cinco años el plazo de prescripción de las acciones personales sin plazo especial, con régimen transitorio en su disposición transitoria quinta; comprobar el plazo aplicable al caso (y, en su caso, el art. 18 LOE) antes de presentar la demanda.

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

Q.P.T.R.C.

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales y de la mercantil [DENOMINACIÓN SOCIAL DEL PROMOTOR], con domicilio social en [DOMICILIO], representación que acredito mediante [ELEGIR LA OPCIÓN QUE CORRESPONDA SEGÚN CÓMO SE HAYA OTORGADO EL PODER; ver nota (1)]:

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— poder otorgado a través de la sede judicial electrónica, inscrito en el Registro Electrónico de Apoderamientos Judiciales, cuya certificación acompaño a este escrito.

— poder otorgado mediante comparecencia apud acta, inscrito en el Registro Electrónico de Apoderamientos Judiciales, cuya certificación acompaño a este escrito.

— escritura de poder otorgada a mi favor ante el Notario D./Dña. [NOMBRE DEL NOTARIO], con el número [Nº DE PROTOCOLO] de su protocolo, inscrita en el Registro Electrónico de Apoderamientos Judiciales, cuya certificación acompaño a este escrito.

bajo la dirección letrada de D./Dña. [NOMBRE Y APELLIDOS DEL ABOGADO/A], abogado/a en ejercicio, con despacho profesional abierto en [DOMICILIO PROFESIONAL], colegiado n.º [Nº DE COLEGIADO] del Ilustre Colegio de la Abogacía de [LOCALIDAD], ante el Tribunal comparezco y como mejor en Derecho proceda, DIGO:

Que mediante el presente escrito vengo a formular DEMANDA DE JUICIO ORDINARIO EN RECLAMACIÓN DE CANTIDAD de [IMPORTE] euros de principal, más los intereses que legalmente correspondan, contra el arquitecto D./Dña. [NOMBRE Y APELLIDOS DEL ARQUITECTO], con domicilio (ver nota (2)), primero en [DOMICILIO]; y segundo, el domicilio laboral en [DOMICILIO PROFESIONAL]; con (ver nota (3)) correo electrónico [CORREO ELECTRÓNICO] y con número de teléfono móvil [TELÉFONO]; contra el aparejador D./Dña. [NOMBRE Y APELLIDOS DEL APAREJADOR], con domicilio en [DOMICILIO]; y contra la mercantil constructora [DENOMINACIÓN SOCIAL DE LA CONSTRUCTORA], con domicilio en [DOMICILIO] y sede social en [DOMICILIO SOCIAL], todo ello de conformidad con los hechos y fundamentos de derecho que se especificarán.

Que esta parte asume el compromiso de recibir cualquier comunicación dirigida por la oficina judicial, durante toda la fase declarativa e, incluso, en una eventual fase de ejecución, por medios telemáticos, en los términos del art. 399.1, párrafo segundo, LEC, consignándose a estos efectos la siguiente dirección de correo electrónico y número de teléfono: [CORREO ELECTRÓNICO] / [TELÉFONO].

HECHOS

PRIMERO.– Mi mandante intervino, como promotor, en la construcción del edificio sito en [DOMICILIO DEL EDIFICIO], desarrollada entre los meses de [MES Y AÑO DE INICIO] y [MES Y AÑO DE FIN], con licencia de obra otorgada con fecha [FECHA]. Al efecto, se contrató:

— Con fecha [FECHA] se encarga al arquitecto D./Dña. [NOMBRE Y APELLIDOS] redactar el proyecto constructivo para la construcción de [DESCRIPCIÓN DE LA OBRA], el cual habría sido visado el [FECHA]. El mismo se habría ocupado también de la dirección facultativa de la obra desde su inicio, el [FECHA], hasta el [FECHA]. Se acompañan, como documentos n.º [Nº] y [Nº] de la demanda, copias del contrato y del proyecto constructivo.

— El [FECHA] se contrata al aparejador D./Dña. [NOMBRE Y APELLIDOS], quien se encargó de la dirección de ejecución de obra desde el inicio hasta el [FECHA]. Se aporta el contrato indicado como documento n.º [Nº] de la demanda.

— Con fecha [FECHA] se suscribe contrato con la empresa constructora [DENOMINACIÓN SOCIAL], que llevó a cabo la edificación; contrato que se adjunta también a esta demanda como documento n.º [Nº].

— También fue contratada el [FECHA] la empresa [DENOMINACIÓN SOCIAL], como organismo de control técnico para controlar la ejecución de aspectos relativos a la estructura y a la edificación. Dicha entidad no es demandada en el presente procedimiento. Se acompaña, como documento n.º [Nº] de la demanda, el citado contrato.

Como se ha dicho, mi mandante intervino como promotora, contratando a los profesionales relacionados, así como vendiendo las distintas viviendas y locales del edificio a los particulares que, posteriormente, conformaron la comunidad de propietarios del edificio [DENOMINACIÓN DE LA COMUNIDAD], que con fecha [FECHA] habría demandado a la promotora la cantidad de [IMPORTE] euros, siendo condenada ésta a su abono.

Debe reseñarse, respecto de cuanto se mantiene en el párrafo que antecede, que [DENOMINACIÓN SOCIAL DEL PROMOTOR], la entidad que represento, no realizó ningún tipo de labor efectiva en la obra, limitándose a la coordinación de los intervinientes citados.

SEGUNDO.– Al hilo de lo expuesto en el antecedente de hecho precedente, ha de tenerse en consideración que, con fecha [FECHA], la Comunidad de Propietarios del n.º [Nº] de la calle [CALLE] de [LOCALIDAD] interpuso una demanda de juicio ordinario exclusivamente contra mi mandante por su intervención como promotora en la construcción del edificio sito en la misma dirección. El citado procedimiento se tramitó ante la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº], como juicio ordinario n.º [Nº DE PROCEDIMIENTO].

La sentencia dictada en [ELEGIR: primera / segunda] instancia del referido procedimiento, de fecha [FECHA], estimó parcialmente la demanda y condenó a mi representada a abonar a la actora el importe de [IMPORTE] euros, más el interés legal incrementado en dos puntos desde la fecha de la resolución y hasta su completo pago, [ELEGIR: con / sin] imposición de costas. Se adjuntan como documentos n.º [Nº] y [Nº] copia de la referida sentencia y de la resolución en la cual se declara su firmeza.

TERCERO.– En cumplimiento del mencionado título judicial, con fecha [FECHA] mi mandante consignó en el Tribunal para pago la cantidad de [IMPORTE TOTAL] euros, correspondientes a [IMPORTE] euros de principal, [IMPORTE] euros de intereses [OPCIONAL — si ha lugar: y [IMPORTE] euros en concepto de costas]. Se adjunta resguardo de la consignación efectuada como documento n.º [Nº].

CUARTO.– Con el propósito de entablar la acción que aquí se ejercita, y sobre la base del informe pericial que se tuvo en cuenta para condenar a mi representada como promotora de la obra en el procedimiento referido, se encargó la emisión de un informe pericial al arquitecto D./Dña. [NOMBRE Y APELLIDOS DEL PERITO]. En el mismo, acompañado como documento n.º [Nº] de la demanda, se detalla la responsabilidad de los distintos agentes que han intervenido en el proceso de construcción del edificio en cuestión en relación con los vicios o deficiencias fijados como hechos probados en la sentencia condenatoria.

QUINTO.– Como se razonará en los fundamentos de derecho, no ha sido posible individualizar la concreta responsabilidad de los intervinientes demandados, considerándoseles obligados solidarios por su participación en el proyecto de edificación. Por ello, se les ha requerido de pago mediante distintos burofaxes individualizados enviados los días [FECHAS], de los que no se ha producido respuesta. Se acompañan, como bloque documental n.º [Nº], copias de dichas comunicaciones extrajudiciales.

En consecuencia, dado que todas las gestiones realizadas hasta el momento han sido infructuosas, mi mandante se ve obligado a solicitar el auxilio judicial para intentar recuperar las cantidades abonadas frente a los adquirentes de viviendas o locales con los que contrató directamente.

SEXTO.– Previamente a la presentación de la presente demanda, se llevaron a cabo diversos esfuerzos de negociación con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria.

Entre las acciones realizadas, se incluyen el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución; así como la participación en reuniones llevadas a cabo los días [FECHAS], cuyos objetivos fueron buscar una conciliación respecto de las diferencias planteadas.

Se adjuntan como prueba copias de las comunicaciones enviadas y recibidas durante el proceso de negociación, incluidas cartas, correos electrónicos y/o actas de reuniones, como documentos números [Nº].

A los presentes hechos son de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN Y COMPETENCIA.

De acuerdo con lo dispuesto en los arts. 9.2 y 21 LOPJ y el art. 5 LEC, el conocimiento del presente litigio corresponde al orden jurisdiccional civil y, en concreto, a las secciones civiles de los tribunales de instancia, en virtud de lo previsto en el art. 45 LEC.

Es competente territorialmente el Tribunal al que tenemos el honor de dirigirnos al tratarse del municipio en el que tienen fijado su domicilio los tres demandados, tal y como se expone en el encabezamiento y se desprende de los tres contratos en cuya virtud se reclama.

II.- PROCEDIMIENTO.

De conformidad con lo dispuesto en el art. 249.2 LEC, el presente procedimiento deberá seguirse por los trámites correspondientes al juicio ordinario, al tratarse de una reclamación dineraria de importe superior a 15.000 euros.

III.- LEGITIMACIÓN.

A partir de lo dispuesto en el art. 10 LEC, mi mandante ostenta legitimación activa como promotora de la obra y persona condenada a la reparación de defectos constructivos por sentencia dictada por la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº] en el procedimiento de juicio ordinario n.º [Nº DE PROCEDIMIENTO]. En este sentido, se reconoce tal legitimación genérica, para reclamar por los daños ocasionados, al promotor en las sentencias del Tribunal Supremo de 27 de abril de 1995 (rec. 676/1992), de 21 de junio de 1999 (rec. 3150/1994) y de 10 de diciembre de 2001 (rec. 2484/1996). Asimismo, para poder ejercitar la acción de repetición se precisa el pago de la cantidad que se reclama, como reflejo del tradicional principio solve et repete (sentencia del Tribunal Supremo de 20 de diciembre de 2007, rec. 3238/2000). Extremo cumplimentado por la consignación para pago realizada ante el órgano judicial designado.

La legitimación pasiva es ostentada por los demandados, como intervinientes en las obras por las que la actora fue condenada: el arquitecto D./Dña. [NOMBRE Y APELLIDOS], como redactor del proyecto y director facultativo de la obra; el aparejador D./Dña. [NOMBRE Y APELLIDOS], como director de ejecución de la obra; y la entidad [DENOMINACIÓN SOCIAL], como constructora del edificio.

IV.- CUANTÍA.

Cumplimentando la exigencia legal del art. 253.1 LEC, se concreta la cuantía del presente procedimiento en la cantidad de [IMPORTE] euros, como principal reclamado de manera solidaria a los tres codemandados.

V.- POSTULACIÓN.

Conforme disponen respectivamente los arts. 23 y 31 LEC, atendiendo a la cuantía y al procedimiento seguido, comparece esta parte asistida de Procurador/a que le representa y Letrado que le defiende, ambos debidamente colegiados y capacitados para actuar ante el Tribunal al cual tengo el honor de dirigirme.

VI.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4.º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

VII.- FONDO DEL ASUNTO.

a) Acción de repetición:

En la presente demanda se ejercita la acción de regreso habilitada en el art. 1.145 del Código Civil, al haber abonado mi representada la deuda declarada judicialmente frente a los compradores de los inmuebles, con quienes mantenía una relación contractual directa. Se dirige, de esta forma, la acción contra los demandados, con objeto de reclamar lo que les corresponde, que, como se verá, consiste en el pago de la totalidad de la deuda fijada judicialmente, al no haber intervenido mi mandante directamente en la obra.

Respecto a la posibilidad de ejercitar la acción de repetición, el Tribunal Supremo ha acogido la posibilidad de su ejercicio frente a los demás intervinientes de una forma reiterada en una clásica doctrina jurisprudencial, en la que destacan las sentencias de 25 de octubre de 1988, de 8 de mayo de 1991, de 11 de julio de 1992, de 10 de octubre de 1992, de 29 de septiembre de 1993 o de 22 de septiembre de 1994.

b) De la responsabilidad de los codemandados:

La responsabilidad de los demandados deriva de la tradicional regulación del art. 1.591 del Código Civil y de la Ley de Ordenación de la Edificación, Ley 38/1999, de 5 de noviembre (como regulación que adapta aquella al sector de la construcción actual), al ser la licencia de obra solicitada posterior al 6 de mayo de 2000 (en concreto, la misma se concede el [FECHA DE LA LICENCIA]). Así, aquel precepto legal exige, para que surja el nacimiento de la responsabilidad decenal: 1) que los responsables hayan participado en la construcción de un «edificio»; 2) que el edificio sufra ruina o defectos constructivos; 3) que la ruina se manifieste dentro de los diez años siguientes a la terminación del edificio; y 4) que la ruina se deba a vicios de la construcción, del suelo o de la dirección o a la falta del contratista a las condiciones del contrato.

Así, por ruina, tradicionalmente se ha venido incluyendo no solo la ruina total, sino también la parcial; así como no sólo la ruina física, sino también la funcional, de tal modo que se amplió el contenido de tal concepto a aquellos supuestos en los que las anomalías constructivas no ponen en peligro la solidez o estabilidad del edificio, pero sí la afectan hasta el punto de que la construcción resulta impropia para el uso y destino para el que se realizó. Es decir, se incluyeron también aquellos defectos que afectan a la calidad o condiciones de uso y habitabilidad, como las humedades (sentencias del Tribunal Supremo de 22 de julio de 1991 o de 31 de diciembre de 1992); el empleo de materiales defectuosos o técnicamente inadecuados para el fin previsto, los defectos en la cubierta del edificio, grietas y filtraciones de agua por utilización de mortero inadecuado (sentencia del Tribunal Supremo de 16 de junio de 1984), por ausencia del debido aislamiento o por mala impermeabilización (sentencia del Tribunal Supremo de 15 de octubre de 1990), o plazas de garaje con defectos que impiden su utilización (sentencia del Tribunal Supremo de 2 de octubre de 2003, rec. 4019/1997). Sin embargo, a partir de la idea de que esta interpretación tan laxa del término ruina ha llegado a distorsionar el verdadero espíritu del art. 1.591 del Código Civil, surge una corriente doctrinal que sustituye ese concepto excesivamente amplio, que ni tan siquiera exige el arruinamiento físico del edificio, por otro concepto, defectos en la construcción. Con el mismo se hace referencia a aquellos daños que aparecen a consecuencia de los defectos de la construcción, siempre que la gravedad de estos últimos permita calificar la obra como una obra en ruina. Así, cuando se habla de vicios de la construcción se hace referencia a la causa específica del defecto de la construcción. Es decir, el vicio es la causa, y el defecto el resultado, exigiéndose como requisitos de aquellos la existencia de defectos graves o ruinógenos. En esta línea, la doctrina y la jurisprudencia han venido distinguiendo entre los vicios o defectos ruinógenos que sí dan lugar a la aplicación del precepto y aquellos que se denominan no ruinógenos y que excluyen su aplicación, distinción ésta que posteriormente vino a recoger la LOE en su art. 17.

El segundo requisito que ha de concurrir para que sea susceptible de aplicar el art. 1.591 del Código Civil es que el vicio o defecto se manifieste dentro del plazo establecido, diez años contados desde que finalizó la construcción. Dicho plazo es el plazo de garantía de la buena construcción de la obra y no hay que confundirlo con el plazo de prescripción o de caducidad para ejercer la acción de reclamación. Se hace preciso, por tanto, que el vicio o defecto ruinógeno se ponga de manifiesto dentro de ese plazo de diez años, pues de no ser así no se podrá ejercer la acción exigiendo responsabilidad por la existencia de vicio ruinógeno cuando éste se haya manifestado transcurrido ese plazo de garantía, al entender que la misma ha precluido, siendo el actor el que ha de probar que el daño se produjo dentro de dicho plazo. Es decir, el vicio o defecto ha de hacerse evidente dentro de ese plazo de diez años, y una vez que se haya producido tal manifestación nace el plazo de prescripción para ejercer la acción. Vinculado con ello, se plantea el problema de determinar la fecha a partir de la cual ha de empezar a contar ese plazo de garantía de diez años: el día de la recepción de la obra o el de la conclusión de la obra. La LOE ha optado por seguir la primera y mayoritaria opción. En consecuencia, una vez entregada la obra es preciso que los defectos o vicios se pongan de manifiesto en ese plazo de garantía de diez años. Si así fuera, en el momento en que se produzca la aparición de los vicios ruinógenos, dentro del plazo de garantía, nace el plazo de prescripción para el ejercicio de la acción de reclamación, y que será de quince años según lo previsto en el art. 1.964 del Código Civil —en la redacción vigente hasta la reforma de la Ley 42/2015, de 5 de octubre— para las obligaciones que no tienen señalado un especial término en la ley. En tal sentido, sentencias del Tribunal Supremo de fechas 1 de octubre de 1992, de 6 de abril de 1994, de 20 de julio de 2002 o de 27 de octubre de 2003, entre otras.

El tercer requisito que ha de concurrir es que el defecto o vicio que aparezca en la obra tenga su origen o causa en una construcción viciosa de la obra. Es decir, ha de existir un nexo causal entre el vicio constructivo, que bien puede consistir en el proyecto, en la dirección técnica o en la ejecución material, y el defecto o daño del edificio. Sin tal relación de causalidad entre la ruina y las atribuciones de los profesionales no es exigible la responsabilidad decenal. Así, la jurisprudencia ha venido admitiendo que el demandado puede destruir la presunción de culpabilidad y de causalidad siempre que acredite que el defecto se produjo bien por un hecho del perjudicado, bien por el de un tercero ajeno o bien por caso fortuito o fuerza mayor.

Finalmente, otro de los requisitos que forzosamente ha de existir es que a consecuencia de esos vicios o defectos de la construcción surjan unos daños y perjuicios. Estos no han de confundirse con los propios vicios o defectos, en tanto que los daños y perjuicios son la consecuencia de la existencia de tales vicios o defectos, y porque el concepto de daño es más amplio al comprender todos los perjuicios que se deriven para el propietario, incluyendo el daño emergente, el lucro cesante e incluso el daño moral.

Sentado lo cual, la jurisprudencia ha venido entendiendo de forma mayoritaria e indubitada que el art. 1.591 del Código Civil establece una presunción «iuris tantum» de imputabilidad de la ruina, de tal modo que si la ruina se produce dentro del plazo de garantía de diez años cabe presumir la culpa del constructor, del arquitecto o de otros técnicos o profesionales, dependiendo de la clase de vicio que haya causado la ruina (así, las sentencias del Tribunal Supremo de 14 de noviembre de 1978; de 3 de octubre de 1979; de 30 de septiembre de 1983; de 27 de junio de 1994, rec. 2869/1991; de 19 de octubre de 1998, rec. 1850/1994; o de 11 de diciembre de 2002, rec. 1432/1997). En virtud de esta presunción, el demandante no tiene que probar la causa de la ruina, es decir, el nexo causal al que antes hicimos referencia, ni que dicha ruina se produjo por culpa del demandado. Al demandante le basta con probar el hecho de la ruina y, una vez que demuestre tal circunstancia y lo haga dentro del plazo de garantía, se presume que ese defecto procede de un vicio de la construcción, del suelo o de la dirección, y de ello nace una segunda presunción, esto es, se presume que el vicio se debe a la conducta culpable del contratista, el arquitecto o cualesquiera de los técnicos intervinientes. Se defiende esta presunción de culpabilidad por entender que la aparición de tales vicios nace del incumplimiento de la «lex artis» exigible a cada uno de los profesionales que intervinieron en la ejecución de la obra. Sin embargo, esta presunción de la culpa no impide que cada vez con más frecuencia la jurisprudencia haya venido admitiendo que los distintos profesionales que intervinieran en la obra puedan exonerarse de toda responsabilidad siempre que acrediten que actuaron con la diligencia que les era exigible. Este sistema viene a reconocer una cierta objetivación de la responsabilidad de estos profesionales vinculada a una inversión de la carga de la prueba o presunción de culpa, que trae su causa en consideraciones de orden público y en la importancia social de las edificaciones. Por ello, existe así una doble presunción de culpabilidad y de causalidad. De ello se deriva que el perjudicado únicamente ha de probar el daño sufrido y que éste se produjo dentro del plazo de garantía decenal, puesto que la doble presunción hace que sean los agentes intervinientes en la ejecución de la edificación los que han de probar la ausencia de responsabilidad en la causación de tales daños, siempre que para ello acrediten la inexistencia de nexo causal entre el vicio que se encuentre dentro de su esfera de actuación y la ruina. Se presume que la responsabilidad de ese daño es del agente, pero se admite prueba en contrario, de tal modo que puede probar que la ruina se debe a otros motivos, como mala conservación, culpa de un tercero, fuerza mayor o caso fortuito. Dicha doble presunción es aplicable únicamente respecto de los vicios ruinógenos, no así respecto a los no ruinógenos, en cuyo caso el demandante habrá de probar que el defecto tiene su origen en un vicio de la construcción y que ha sido causado por impericia del profesional.

En esta misma línea, el art. 1.591 del Código Civil diferencia tres clases de vicios, que servirán como criterios para poder imputar las distintas responsabilidades. Así, se refiere a los vicios de la construcción, de los que responderá el constructor, y los vicios de la dirección y del suelo, de los que responderá el arquitecto, de tal modo que cada uno de los profesionales responderá únicamente cuando la causa de la ruina tenga su origen en los vicios constructivos que recaigan en su esfera de actividad profesional, sin perjuicio de que en la práctica tal individualización resulta muchas veces imposible de realizar, en cuyo caso obliga a determinar la responsabilidad de todos los agentes intervinientes de forma conjunta. Sin embargo, hoy en día resulta insuficiente esa distinción, toda vez que no permite individualizar adecuadamente la culpa del arquitecto, puesto que se puede producir la intervención en la fase de dirección técnica de la obra de un segundo técnico como es el aparejador. Las funciones y obligaciones de estos dos técnicos están perfectamente diferenciadas, pero el problema se suscita en determinar quién de los dos es responsable.

Como en la realización de la construcción son varios, y cada vez más, los sujetos intervinientes, se plantea de qué forma y en qué grado debe distribuirse la responsabilidad entre ellos. En principio la respuesta es clara: una vez que se determine el vicio constructivo que causó la ruina o el defecto constructivo, la responsabilidad se imputa al profesional en cuya esfera de riesgo se encontrare el vicio, al entenderse que fue la violación de la «lex artis» de dicho profesional la que causó el vicio del que derivó tal ruina. Sin embargo, como se decía, esta determinación de la responsabilidad entre los distintos profesionales no resulta tan sencilla en la mayoría de los casos, y ello porque a veces no queda suficientemente demostrado qué clase de vicio causó la ruina, o cuando fueron varios los que la produjeron y, por tanto, concurre la culpa de varios profesionales. En estos casos, cuando no es posible individualizar en cada profesional el grado de responsabilidad, el Tribunal Supremo ha venido generalizando la aplicación de la responsabilidad solidaria entre tales profesionales, tanto cuando no es posible acreditar qué vicio causó la ruina como cuando no se puede establecer la cuota de participación de cada uno de los agentes en la producción de la ruina. Esta responsabilidad solidaria se ha convertido en la regla general, siempre que la individualización no sea posible, y ello inspirado en un principio de protección al perjudicado, constituyendo una garantía añadida para el mismo al quedar protegido de la insolvencia de cualquiera de los agentes responsables. De ello deriva otra consecuencia como es que no se exija la constitución de litisconsorcio pasivo necesario, bastando con que el perjudicado llame al proceso a cualquiera de los intervinientes de la obra, ello sin perjuicio de las acciones que entre éstos puedan ejercitar.

En consecuencia, en el presente caso nos encontramos con los siguientes intervinientes de la obra:

1.- D./Dña. [NOMBRE Y APELLIDOS DEL ARQUITECTO], en quien concurre la doble condición de técnico director y de técnico proyectista. De esta manera, su función es elaborar un proyecto adecuado para la construcción, interpretar y desarrollar el mismo y sus adaptaciones, detalles complementarios, modificaciones, correcciones, adaptaciones y soluciones a los problemas técnicos que vayan surgiendo, vigilando que el edificio se adecue al proyecto, realizando para ello funciones de inspección y control, y asegurándose de que se cumple en la edificación lo previsto en el proyecto respecto de formas, dimensiones, calidades y utilidad. Ello supone que ha de impartir al aparejador y al constructor las instrucciones y órdenes precisas para garantizar que la obra se ajusta a la previsión del proyecto, debiendo para ello asistir a la obra siempre que fuera preciso. En consecuencia, los vicios imputables a la dirección pueden obedecer, no sólo a un actuar positivo, emitiendo directrices o instrucciones técnicas incorrectas, sino también a una omisión o pasividad, referida a la falta de comprobación de que la obra se está llevando a cabo de acuerdo con las indicaciones técnicas reflejadas en el propio proyecto. Por ello, le son imputables, por esa falta de atención y vigilancia debidas a la ejecución de la obra, los defectos o vicios que suponen una desviación o desajuste respecto al proyecto correspondiente, incluida la idoneidad o inadecuación de los materiales empleados. En esta línea, las sentencias del Tribunal Supremo de 26 de octubre de 1984, de 5 de junio de 1986, de 9 de marzo de 1988 y de 12 de noviembre de 1992, entre otras.

En el presente caso, tal y como pone de relieve el informe pericial aportado, le son imputables los defectos apreciados en la sentencia que condenó a mi mandante por las siguientes causas:

— [CAUSA 1]

— [CAUSA 2]

— [CAUSA 3]

— [CAUSA 4]

2.- D./Dña. [NOMBRE Y APELLIDOS DEL APAREJADOR], como [ELEGIR: aparejador / arquitecto técnico]: la jurisprudencia lo ha incluido entre las personas responsables por su asimilación con el arquitecto. En un primer momento nació como subordinado de la figura del arquitecto, pero actualmente es una profesión completamente independiente de la de aquél, y goza de autonomía propia. Tradicionalmente, el aparejador es quien está a pie de obra, controlando la calidad de las técnicas y materiales constructivos. Así, sus obligaciones consisten en: 1.º ordenar y dirigir los trabajos de ejecución material de la obra, según lo previsto en el proyecto, las instrucciones del arquitecto y la lex artis; 2.º inspeccionar y ordenar la obra, vigilando los materiales de construcción y mezclas como morteros, argamasas, hormigones, cementos...; y 3.º vigilar la obra y los trabajos de ejecución material, debiendo por ello asistir a la obra y controlar los trabajos que en ella se ejecuten. Al respecto, se pronuncia la sentencia del Tribunal Supremo de 25 de octubre de 2006, rec. 86/2000, señalando que constituyen ineludibles deberes profesionales de los aparejadores la ejecución y vigilancia de las órdenes dadas por la dirección de la obra, procurando la perfecta realización de los trabajos y el empleo de los materiales adecuados por parte del contratista. En la misma línea, la sentencia del Tribunal Supremo de 10 de julio de 2011 señala que las actividades de inspeccionar, controlar y ordenar la correcta ejecución de la obra les vienen impuestas por ley, pues es el profesional que debe mantener más contactos directos, asiduos e inmediatos con el proceso constructivo. Por ello, su responsabilidad concurrente se impone y le alcanza, no sólo cuando se produce una mala ejecución de la obra, sino asimismo con una defectuosa dirección de la misma, así como por la responsabilidad derivada de las funciones que le son otorgadas: inspeccionar con la debida asiduidad los materiales, proporciones y mezclas; ordenar la ejecución material de la obra; vigilar que la obra se efectúa con sujeción al proyecto y a las buenas prácticas de la construcción; y observar las órdenes e instrucciones del arquitecto.

El informe pericial presentado imputa al aquí demandado responsabilidad en los defectos apreciados en la sentencia que condenó a mi mandante por las siguientes causas:

— [CAUSA 1]

— [CAUSA 2]

— [CAUSA 3]

— [CAUSA 4]

3.- La entidad [DENOMINACIÓN SOCIAL DE LA CONSTRUCTORA], como [ELEGIR: contratista / constructor], obligado a responder de los daños o defectos derivados de su impericia o falta de capacidad profesional en el marco de la ejecución de la obra; la cual debe acomodarse a la lex artis correspondiente, exigiéndose la estricta observancia del proyecto ideado y de las instrucciones que se dan en ejecución de aquel. En el presente caso, la responsabilidad de la mercantil codemandada se fundamenta en las siguientes causas que, en función de aquella, tienen relación con los vicios apreciados:

— [CAUSA 1]

— [CAUSA 2]

— [CAUSA 3]

— [CAUSA 4]

c) De las acciones de responsabilidad imputables:

Sobre la cuestión, el art. 17 LOE establece una clasificación tripartita de los daños materiales en el edificio que dan lugar a varias acciones de responsabilidad dotadas de diferentes plazos de garantía.

1.- Así, la primera de las garantías del art. 17.1 LOE la constituye la llamada responsabilidad decenal, la cual tendrá lugar cuando el daño material esté causado por vicios o defectos que afecten a la cimentación, los soportes, las vigas, los forjados, los muros de carga y otros elementos estructurales y, además, estos daños comprometan la resistencia mecánica y estabilidad del edificio.

2.- En segundo lugar, se refiere a la garantía trienal, en referencia a los daños que no alcanzan la gravedad de los anteriores, pero que afectan a la habitabilidad del edificio, entendiendo que hacen al edificio inútil o inservible para el destino que le es propio.

3.- Concluye el mencionado precepto legal refiriéndose a la llamada responsabilidad anual, que se refiere a los daños materiales causados al edificio por los vicios o defectos de ejecución que afecten a elementos de terminación o acabado de las obras. Esta acción es oponible únicamente frente al constructor, y se refiere a la falta de labores de perfeccionamiento o retoque de una obra, como pueden ser persianas que no cierren bien, baldosas agrietadas, parquet mal colocado, etc.

En el presente caso, los vicios determinados por sentencia son imputables de manera conjunta a los codemandados, en cuanto a que no se puede deslindar, como factores para su causación, la responsabilidad del arquitecto a la hora de diseñar un proyecto erróneo y dirigir la obra sin apercibirse de ello; la responsabilidad del aparejador agravando los defectos con una falta de vigilancia y suministro de informaciones genéricas; y la mala praxis a la hora de ejecutar los trabajos de manera directa. En consecuencia, tal individualización resulta muchas veces imposible de realizar, lo que determina la responsabilidad de todos los agentes intervinientes de forma conjunta.

Y en este sentido, dado que mi mandante se limitó a contratar y coordinar a los profesionales, sin intervención en la realización de la obra, en cuyo ámbito se generan los daños constatados, no puede responder por los mismos. Puesto que ha abonado el importe correspondiente a la reparación, en su condición de promotor vendedor, debe ser indemnizado por los tres codemandados, de manera solidaria, del importe principal de [IMPORTE] euros efectivamente pagados.

VIII.- DE LOS INTERESES.

El art. 1.145 del Código Civil, que sirve de fundamento a esta reclamación, determina que el deudor solidario que abonó el importe de la deuda puede reclamar al resto de deudores «la parte que a cada uno corresponda, con los intereses del anticipo». En consecuencia, la cantidad reclamada se incrementa en la cantidad de [IMPORTE] euros, abonados como intereses, para un total de [IMPORTE TOTAL] euros; los cuales además generarán intereses desde la fecha de reclamación extrajudicial. En este caso, los burofaxes fueron enviados con fechas [FECHAS], respectivamente, para los tres codemandados.

A falta de pacto expreso, esos intereses serán los intereses legales, si bien a partir de la fecha de la sentencia que se dicte en este procedimiento, y de conformidad con lo dispuesto en el art. 576 LEC, los intereses serán los correspondientes al interés legal incrementado en dos puntos.

IX.- COSTAS.

Las costas deberán ser impuestas a los demandados, en virtud del criterio del vencimiento recogido en el art. 394.1 LEC.

Por lo expuesto,

SUPLICO AL TRIBUNAL

que, habiendo por presentado este escrito con la documentación que se acompaña, se sirva admitirlos y, en su virtud, tenga por formulada demanda de juicio ordinario contra el arquitecto D./Dña. [NOMBRE Y APELLIDOS], con domicilio en la calle [CALLE] de [LOCALIDAD]; contra el aparejador D./Dña. [NOMBRE Y APELLIDOS], con domicilio en la calle [CALLE] de [LOCALIDAD], y contra la mercantil constructora [DENOMINACIÓN SOCIAL], previos los trámites pertinentes, dicte en su día sentencia por la que, estimándola, se condene solidariamente a los demandados a reembolsar a mi mandante la cantidad de [IMPORTE] euros, más los intereses legales devengados desde los días [FECHAS], respectivamente para los tres codemandados, hasta la fecha de la sentencia que se dicte; a partir de la cual se aplicará el interés legal incrementado en dos puntos. Asimismo, y para el caso de que se oponga a la demanda, siquiera parcialmente, deberán imponerse las costas procesales.

Por ser así de justicia, que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

OTROSÍ DIGO que, para el improbable supuesto de que alguno de los hechos descritos en la presente demanda fuera negado por el demandado, o que la autenticidad de alguno de los documentos aportados fuera impugnada de adverso, o que los documentos aportados se consideren insuficientes para acreditar los hechos de los que trae causa la presente reclamación, designamos, a efectos probatorios, los archivos de la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº] (tribunal que conoció de la causa contra la promotora), como juicio ordinario n.º [Nº DE PROCEDIMIENTO]. Por ser igualmente de justicia, que pido en el mismo lugar y fecha.

OTROSÍ SEGUNDO DIGO: Se acompaña a la demanda informe pericial (documento n.º [Nº]) elaborado por el arquitecto D./Dña. [NOMBRE Y APELLIDOS], cuya declaración en juicio se propone en este acto a los efectos correspondientes. Por ser igualmente de justicia, que pido en el mismo lugar y fecha.

Firma del Abogado/a: [NOMBRE Y APELLIDOS, Nº DE COLEGIADO]

Firma del Procurador/a: [NOMBRE Y APELLIDOS]

NOTAS EXPLICATIVAS

(1) Para su acreditación, todos los poderes deben estar inscritos en el Registro Electrónico de Apoderamientos Judiciales (REAJ). Basta, para su acreditación, con la consulta automatizada de dicho Registro, que está a disposición de cualquier Letrado de la Administración de Justicia. No obstante, dado que el art. 24.2 LEC configura la certificación de dicha inscripción como vía subsidiaria de acreditación, para el caso de que el sistema no permita aquella consulta automatizada, se señala en el modelo que se acompaña certificación electrónica. El sistema permite emitir dicha certificación a quien inscribe el poder.

(2) El art. 155.3 LEC permite expresar varios domicilios del demandado (el que aparezca en el padrón municipal o conste oficialmente a estos efectos; el que aparezca en registro oficial o en publicaciones de colegios profesionales, si se trata de empresas o personas colegiadas; donde desarrolle su actividad profesional o laboral no ocasional; si es empresa mercantil, el domicilio de cualquiera de sus administradores, gerentes o apoderados; o, si es asociación que consta en registro oficial, el domicilio del presidente, miembro o gestor de la junta correspondiente). Cuando se señalen varios, se indicará el orden a seguir para la notificación, con vistas al éxito de la misma.

(3) El art. 155.3 LEC configura una obligación adicional del demandante, consistente en aportar cuantos datos sean de utilidad para localizar al demandado: número de identificación fiscal o de extranjeros, número de teléfono o de fax, dirección de correo electrónico o similares.
