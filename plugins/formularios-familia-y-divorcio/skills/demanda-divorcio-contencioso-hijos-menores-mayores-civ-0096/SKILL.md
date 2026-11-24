---
name: demanda-divorcio-contencioso-hijos-menores-mayores-civ-0096
description: "Demanda de divorcio contencioso con hijos menores y mayores dependientes y petición de medidas. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de divorcio contencioso con hijos menores y mayores dependientes y petición de medidas

> Formulario **CIV-0096** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de divorcio contencioso con hijos menores y mayores dependientes y petición de medidas» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de divorcio contencioso con hijos menores y mayores dependientes y petición de medidas” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-divorcio-contencioso-hijos-menores-mayores-civ-0096`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (8 veces)
- [ ] FECHA (7 veces)
- [ ] LOCALIDAD (7 veces)
- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] Nº DE DOCUMENTO (6 veces)
- [ ] Nº (5 veces)
- [ ] C.P. (2 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] FECHAS (2 veces)
- [ ] Nº DE COLEGIADO/A (2 veces)
- [ ] RÉGIMEN ECONÓMICO (2 veces)
- [ ] CALLE
- [ ] CURSO ESCOLAR
- [ ] DÍA
- [ ] EDAD
- [ ] MARCA/MODELO
- [ ] MATRÍCULA
- [ ] MES
- [ ] MOTIVO
- [ ] Nº DE HIJOS
- [ ] PÁGINA
- [ ] SEDE
- [ ] TIPO DE MATRIMONIO (CIVIL / CANÓNICO)
- [ ] TOMO
- [ ] ÓRGANO O PERSONA

## Normas que cita el formulario

- art. 86 Código Civil
- art. 770 LEC
- art. 97 Código Civil
- art. 91 Código Civil
- art. 769.1 LEC
- art. 85.1 LOPJ
- art. 437.1 LEC
- art. 5 Ley Orgánica 1/2025
- art. 1392.3 Código Civil
- art. 445 LEC
- art. 103 Código Civil
- art. 773 LEC
- art. 771 LEC
- art. 749 LEC

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

- Junto a «… LA SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Denominación legal: Sección de Familia, Infancia y Capacidad. Si no existe en el partido, conoce la Sección Civil o la Única (art. 86.3-4 LOPJ). Fuente: LOPJ arts. 84.2.a) y 86 (redacc. LO 1/2025, BOE-A-2025-76).

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

A LA SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS] Procurador de los Tribunales colegiado/a número [Nº DE COLEGIADO/A] en nombre y representación de d/dña. con domicilio en [LOCALIDAD] C/Av/pz. CP [C.P.] a efecto de notificaciones, según acredito mediante escritura de poder inscrito en el Registro Electrónico de Apoderamientos Judiciales, a cuya justificación aporto certificación de dicho Registro como documento núm. 1, bajo la dirección letrada de d/dña. con número de colegiado [Nº DE COLEGIADO/A] ante el Tribunal comparezco y, como mejor proceda en derecho, DIGO:

Que en la representación que ostento deduzco DEMANDA CONTENCIOSA DE DIVORCIO, al amparo del artículo 86 del Código Civil, contra D./Dña. [NOMBRE Y APELLIDOS] con domicilio en [LOCALIDAD] C/ CP [C.P.] Tel. y, siguiendo los trámites señalados en el artículo 770 y siguientes de la LECiv, basando la misma en los siguientes:

HECHOS

PRIMERO.- D. [NOMBRE Y APELLIDOS] y dña., contrajeron matrimonio [TIPO DE MATRIMONIO (CIVIL / CANÓNICO)] en [LOCALIDAD] con fecha de [FECHA], inscrito en el registro Civil de dicha localidad, al tomo [TOMO], página [PÁGINA] Acredito dicho hecho mediante la certificación de la inscripción de matrimonio que se acompaña como documento núm. [Nº DE DOCUMENTO]

SEGUNDO.- El matrimonio se contrajo bajo el régimen de [RÉGIMEN ECONÓMICO]. En la actualidad el régimen económico matrimonial es el de [RÉGIMEN ECONÓMICO].

En prueba de ello se aporta como documento núm. [Nº DE DOCUMENTO].

TERCERO.- De dicha unión conyugal existe descendencia, concretamente [Nº DE HIJOS] hijos, de [Nº] años de edad y de [Nº] años de edad, llamados:

1. nacido en fecha de [FECHA]

2. nacido en fecha de [FECHA]

El segundo hijo, aun siendo mayor de edad, permanece en la vivienda familiar al no estar independizado económicamente, pues estudia [FECHA] estando en el curso [CURSO ESCOLAR] Se acreditan estos hechos por medio de la certificación del Ayuntamiento de [LOCALIDAD] en que ambos hijos aparecen empadronados en el domicilio familiar, como documentos números, así como los recibos de las respectivas matrículas.

Aportamos en prueba de ello como documento número [Nº DE DOCUMENTO] certificación de la inscripción de nacimiento.

CUARTO.- Que habiendo cesado las razones y sentimientos que dieron lugar al matrimonio y convivencia en común, y desaparecido la affectio maritalis que en su día existía entre los litigantes, mi representado ha decidido solicitar el divorcio, a que se refiere el artículo 86 del Código Civil.

Desde hace aproximadamente seis años y por desavenencias surgidas en el matrimonio, ambos esposos decidieron mutua y libremente separarse de hecho. Como consecuencia de ello, el demandado salió del domicilio conyugal sito en [LOCALIDAD] para trasladarse a vivir al domicilio que actualmente ocupa conviviendo desde entonces con dña., mientras mi representada y los hijos siguen ocupando la vivienda familiar.

QUINTO.- El domicilio conyugal se estableció desde el primer momento en la calle [CALLE] núm. [Nº] de esta ciudad, donde continúa. Se acredita este hecho mediante el certificado de empadronamiento expedido por el Ayuntamiento de [LOCALIDAD] que se acompaña como documento núm. Dicha vivienda pertenece en común y pro indiviso a ambos cónyuges que la adquirieron por escritura de [FECHA] como se demuestra con la copia simple, que se aporta como documento núm. [Nº DE DOCUMENTO]

SEXTO.- Que la custodia de los hijos menores de edad ha de corresponder a la madre, por haber sido ella la que siempre les ha atendido, y sobre todo en los últimos años, por el abandono afectivo del padre. Todo ello sin perjuicio del derecho de visitas que se establezca más adecuado por el Juzgador y con un régimen de patria potestad compartida.

Existiendo hijos menores de edad, a ellos corresponde el uso y disfrute de la vivienda familiar. Y dado que los hijos deben quedar bajo la custodia de la madre, será ésta la que ocupe el domicilio familiar, en virtud del interés más necesitado de protección.

SÉPTIMO.- Respecto a los bienes en común, existe un piso, que es el domicilio conyugal y un vehículo, marca [MARCA/MODELO] matrícula [MATRÍCULA]

OCTAVO.- Mi representada se encuentra en la actualidad sin trabajo ya que se ha dedicado toda su vida al cuidado de los hijos, del esposo y dedicación plena a la familia, por lo que nunca ha tenido trabajo remunerado ni tiene ningún tipo de cualificación especial, su edad es la de [EDAD] por lo que le será difícil encontrar empleo, y el matrimonio ha durado [Nº] años. Por el contrario el esposo trabaja en la empresa [DENOMINACIÓN SOCIAL], con unos ingresos mensuales [IMPORTE] euros.

NOVENO.-El matrimonio ha durado [Nº] años, produciendo su ruptura un evidente desequilibrio económico en tanto que [MOTIVO] y en virtud de lo preceptuado en el artículo 97 del Código Civil, procede que se otorgue la cantidad de [IMPORTE] euros a la esposa por tiempo indefinido, revalorizable anualmente conforme a los índice del IPC o el aumento de los ingresos del esposo.

DÉCIMO.- Que los gastos que se ocasionan en la alimentación y educación de los hijos oscilan sobre los [IMPORTE] euros mensuales, y además la ropa, libros, entretenimiento, y los gastos alicuotos de sostenimiento de la casa; debe fijarse una pensión por alimentos, conforme con el artículo 91 del Código Civil de [IMPORTE] euros.

UNDÉCIMO.-El hijo mayor de edad, aún no independizado económicamente, reside en la vivienda familiar y desea permanecer en compañía de la actora, como se acredita por la firma del documento que se adjunta y que será ratificado ante S.Sª.

Así mismo se acompaña poder para el mismo procurador que representa a la actora otorgado por dicho hijo.

DUODÉCIMO.- La parte actora manifiesta que, previo a la presentación de la presente demanda, se llevaron a cabo diversos esfuerzos de negociación con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad, y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria.

Entre las acciones realizadas, se incluyen el Intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución; así como la participación en reuniones llevadas a cabo los días [FECHAS], cuyos objetivos fueron buscar una conciliación respecto de las diferencias planteadas.

Se adjuntan como prueba copias de las comunicaciones enviadas y recibidas durante el proceso de negociación, incluidas cartas, correos electrónicos y/o actas de reuniones como documentos números [Nº DE DOCUMENTO].

Ambas partes finalmente, acudieron a un medio adecuado de solución de controversias, en cumplimiento de las disposiciones legales aplicables.

En este sentido, se participó en el procedimiento de mediación familiar ante el mediador Don/Dña [NOMBRE Y APELLIDOS], elegido por ambas partes, en fecha [FECHA], sin que se haya logrado un acuerdo definitivo.

A su justificación se adjunta acta de no conciliación emitida por [ÓRGANO O PERSONA], de fecha [FECHA], que acredita que las partes acudieron al medio adecuado de solución de controversias sin alcanzar un acuerdo como documento nº [Nº DE DOCUMENTO].

A los anteriores hechos le son de aplicación los siguientes,

FUNDAMENTOS DE DERECHO

Competencia. Artículo 769.1 LECiv y Ley 38/1988, de 28 de diciembre. De Demarcación y Planta Judicial. Al estar situado el último domicilio conyugal en esta ciudad es competente el Tribunal de primera Instancia al que me dirijo, según el artículo 769.1 LECiv, en relación con lo dispuesto en el art. 85.1º LOPJ, quedando atribuido a las Secciones de Familia por hallarse especializados en el conocimiento de esta materia.

Legitimación. Artículo 81.2 del Código Civil y Artículo 6 de la LECiv. La actora está legitimada, por ser el cónyuge del demandado, el cual por lo mismo, se encuentra legitimado pasivamente.

Jurisdicción. Artículo 117.3º de la Constitución Española, conforme con dicho artículo los órganos jurisdiccionales españoles serán competentes para conocer de la demanda de separación que se presenta al tener ambos cónyuges la nacionalidad española y residir en España.

Procedimiento. Artículo 770 LECiv. El presente proceso ha de sustanciarse por las normas establecidas en el artículo citado.

Cumplimiento de los requisitos de procedibilidad. La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC en relación con el art. 437.1 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

Fundamentos jurídicos de la demanda de divorcio.

a) Respecto a la acción que se ejercita.

Es la de divorcio prevista en el artículo 86 del Código Civil de divorcio. Sin necesidad de entrar en la intimidad conyugal y relaciones interpersonales íntimas de los cónyuges, la affectio maritalis ha quedado quebrada de forma irreversible.

b) Efectos personales y patrimoniales derivados del divorcio.

1. Artículo 91 y siguientes del Código Civil. Atribución de la guarda y custodia de los hijos menores a mi mandante y régimen compartido de patria potestad. El principio del favor filii determina que se atribuya a mi mandante la guarda y custodia de los hijos menores, pues es quien se viene encargando del cuidado de los mismos hasta la fecha.

2. Artículo 94 del Código Civil. Se deberá fijar el régimen de visitas a que tendrá derecho el otro cónyuge, que el Juzgador encuentre más adecuado.

3. Artículo 96 del Código Civil. Ha de concederse el uso de la vivienda familiar a mi representada y a sus hijos de conformidad con el artículo citado.

4. Artículos 91, 93 del Código Civil. Se solicita como pensión por alimentos para los hijos y levantamiento de las cargas familiares en la cuantía de [IMPORTE] euros, que deberán ser incrementadas anualmente conforme con el IPC o según los ingresos que experimente el otro cónyuge.

5. Artículo 97, se solicita una pensión compensatoria en la cuantía de [IMPORTE] euros por tiempo indefinido, al producir el divorcio un empeoramiento respecto de la situación anterior en su matrimonio, conforme con los parámetros establecidos en dicho precepto, es decir por

Esta petición viene presidida por los principios dispositivos y de rogación y cumple con la finalidad de evitar que la separación matrimonial produzca en uno de los cónyuges, desequilibrios económicos en relación de uno de los cónyuges con el otro. Todo ello sin perjuicio de ulterior liquidación de la sociedad conyugal, justificándose el desequilibrio por los siguientes motivos.

1.

2.

6. Artículo 95 en relación con el artículo 1392.3 del Código Civil. La sociedad de gananciales concluirá de pleno derecho cuando judicialmente se decrete el divorcio de los cónyuges.

Costas procesales.

Artículo 394 de la LECiv y artíuclo 1902 del Código Civil, que deberán ser impuestas a la demandada si se opusiere a esta justa demanda.

Representación y postulación.

Artículo 750.1 LECiv, en cuanto a la representación del actor y postulación de la presente demanda.

Al existir hijos menores de edad, ha de intervenir el Ministerio Fiscal.

Por todo lo expuesto,

SUPLICO AL TRIBUNAL: Que teniendo por presentada esta demanda con los documentos y copias que se acompañan, se sirva admitirla, teniéndome por parte en la representación acreditada y tener por solicitado el DIVORCIO de d./dña., de d./dña., al que se emplazará en la forma prescrita por la ley, y previos los trámites que procedan, dicte sentencia decretando:

1. Disolución por causa de divorcio del matrimonio por los hechos anteriormente indicados, y por las causas invocadas. Pudiendo los cónyuges fijar libremente su domicilio.

2. Se acuerde la revocación de los poderes que hayan podido otorgarse dichos cónyuges.

3. El establecimiento de una pensión alimenticia para los hijos de [IMPORTE] euros mensuales que serán ingresadas dentro de los cinco primeros días de cada mes en la cuenta núm. abierta a nombre de mi mandante en la entidad [DENOMINACIÓN SOCIAL], cantidad que será actualizada el primero de enero de cada año conforme con el IPC o variaciones que experimenten los ingresos del otro cónyuge.

4. Que la custodia de los hijos menores de edad [NOMBRE Y APELLIDOS] y [NOMBRE Y APELLIDOS], sea concedida a la esposa y madre, así como la patria potestad ordinaria con el régimen de patria potestad compartida.

5. Que se conceda al padre el derecho de visitas que sea oportuno y que fije en interés de los hijos el Juzgador.

6. La concesión a la actora de una pensión compensatoria en la cuantía de [IMPORTE] euros, y en doce mensualidades al año, desde la fecha de la sentencia por tiempo indefinido, que se incrementará conforme con el IPC a partir del uno de enero de cada año o variaciones que experimenten los ingresos del esposo.

7. Que la vivienda conyugal quede para el uso de los hijos menores de edad y de la actora, así como el ajuar y mobiliario, pudiendo retirar el esposo los efectos personales, todo ello bajo inventario.

8. Que se condene en costas al demandado, si se opusiera a lo pedido en esta demanda.

PRIMER OTROSÍ DIGO: De conformidad con el artículo 770 LECiv, en relación con lo dispuesto en el artículo 445 y siguientes de la LECiv, se solicita el recibimiento a prueba.

SUPLICO AL TRIBUNAL: Se sirva recibir a prueba el procedimiento en el momento procesal oportuno, practicando al que se proponga y sea declarada pertinente.

SEGUNDO OTROSÍ DIGO: Que de conformidad con lo establecido en el artículo 103 del Código Civil, en relación con el artículo 773 LECiv, se solicita la apertura de pieza separada de MEDIDAS PROVISIONALES, basándome en los siguientes:

HECHOS

ÚNICO.- Se dan por reproducidos íntegramente los hechos expresados en esta demanda.

Le son de aplicación los siguientes,

FUNDAMENTOS DE DERECHO

ÚNICO.-Arts. 102, 103 y siguientes del Código Civil, en relación con el artículo 773 LECiv.

Por lo cual,

SUPLICO AL TRIBUNAL: Que se cite a las partes a la comparecencia prevenida en la LECiv, y que se sustanciará conforme a lo dispuesto en el artículo 771 de la LECiv, y conforme a las medidas solicitadas en el cuerpo de este escrito se adopten mediante Auto provisionalmente hasta que recaiga sentencia en los autos principales.

TERCER OTROSÍ DIGO: Que de conformidad con lo establecido en el artículo 749 LECiv debe ser parte el Ministerio Fiscal al existir hijos menores de edad.

SUPLICO AL TRIBUNAL: tenga por realizada la anterior manifestación a los efectos legales oportunos.

Es justicia que pido en [LOCALIDAD] a [DÍA] de [MES] 2

Fdo. Letrado Fdo. Procurador

========================================================================
