---
name: demanda-desahucio-impago-reclamacion-rentas-vivienda-civ-0581
description: "Demanda de desahucio por impago y reclamación de rentas de vivienda, con posibilidad de enervación. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de desahucio por impago y reclamación de rentas de vivienda, con posibilidad de enervación

> Formulario **CIV-0581** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 24-11-2026.

## Qué es

Demanda interpuesta por propietario de una vivienda, al Tribunal de Instancia, de juicio verbal de desahucio por falta de pago de la renta de la finca urbana arrendada, así como como de las cuotas mensuales de la comunidad de propietarios por gastos generales que la inquilina se obligó a satisfacer, y reclamación de las cantidades debidas; siendo posible la enervación.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de desahucio por impago y reclamación de rentas de vivienda, con posibilidad de enervación» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de desahucio por impago y reclamación de rentas de vivienda, con posibilidad de enervación” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:demanda-desahucio-impago-reclamacion-rentas-vivienda-civ-0581`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (9 veces)
- [ ] FECHA (6 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] Nº DE DOCUMENTO (4 veces)
- [ ] NÚMERO (4 veces)
- [ ] CALLE (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] CORREO ELECTRÓNICO
- [ ] FECHAS
- [ ] LUGAR
- [ ] MESES IMPAGADOS
- [ ] Nº
- [ ] Nº DE COLEGIADO/A
- [ ] PORCENTAJE
- [ ] SEDE
- [ ] TELÉFONO

## Normas que cita el formulario

- art. 24.1 LEC
- art. 437.1 LEC
- art. 439.6 LEC
- art. 438.5 LEC
- art. 437.3 LEC
- art. 250.1.1 LEC
- art. 437.4.3 LEC
- art. 250.1.1.º LEC
- art. 251 LEC
- art. 252.2.ª LEC
- art. 253 LEC
- art. 3.K Ley 12/2023
- art. 5 Ley Orgánica 1/2025
- art. 1.555.1 CC
- art. 17 LAU
- art. 1.124 CC
- art. 1.556 CC
- art. 27.2.a LAU
- art. 220 LEC
- art. 439.3 LEC
- art. 22.4 LEC
- art. 394.1 LEC
- art. 22.5 LEC

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] Q.P.T.R.C.»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Notas al pie del formulario original:
(1) A la hora de su acreditación, todos los poderes deben estar inscritos en el Registro Electrónico de Apoderamientos Judiciales (REAJ). Se supone que, para su acreditación, basta con la consulta (de dicho Registro) automatizada orientada al dato. Algo que está a disposición de cualquier Letrado de la Administración de Justicia. Sin embargo, dado que el art. 24.2 LEC, configura la certificación de dicha inscripción como vía subsidiaria de acreditación, para el caso de que el sistema no permita aquella consulta automatizada; se señala en el modelo que se acompaña certificación electrónica. El sistema permite emitir dicha certificación para quien inscribe el poder.

(2) El art. 155.3 LEC permite fijar expresar varios domicilios del demandado (el que aparezca en el padrón municipal o conste oficialmente a estos efectos; el que aparezca en Registro oficial o en publicaciones de colegios profesionales, si se trata de empresas o personas colegiadas; donde desarrolle su actividad profesional o laboral no ocasional; si es empresa mercantil, el domicilio de cualquiera de sus administradores, gerentes, o apoderados; o, si es asociación que consta en registro oficial; el domicilio del presidente, miembro o gestor de la Junta correspondiente). Cuando se señalen varios, indicará el orden a seguir para la notificación, con vistas al éxito de la misma.

(3) El art. 155.3 LEC configura una obligación adicional del demandante, consistente en aportar cuantos datos sean de utilidad para localizar al demandado: número de identificación fiscal o de extranjeros, nº [Nº] de teléfono o de fax, dirección de correo electrónico, o similares.

========================================================================


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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] Q.P.T.R.C.

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales y de D./Dña. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], representación que acredito mediante escritura de poder otorgada a mi favor (existen tres posibilidades para otorgar el apoderamiento al Procurador de los Tribunales, conforme dispone el art. 24.1 LEC)

[OPCIONAL — opción en función de cómo se haya otorgado el poder]

[ELEGIR UNA OPCIÓN: Si el poder se otorga a través de la sede judicial electrónica / Si el poder se otorga mediante comparecencia apud acta / Si el poder se otorga ante Notario]

bajo la dirección letrada de D./Dña. [NOMBRE Y APELLIDOS], abogado/a en ejercicio, con despacho profesional abierto en [LOCALIDAD], colegiado nº [Nº DE COLEGIADO/A] del Ilustre Colegio de la Abogacía de [LOCALIDAD], ante el Tribunal comparezco y como mejor en Derecho proceda, DIGO:

Que mediante el presente escrito vengo a formular DEMANDA DE JUICIO VERBAL DE DESAHUCIO POR FALTA DE PAGO y RECLAMACIÓN DE CANTIDADES DEBIDAS, contra D./Dña. [NOMBRE Y APELLIDOS], con domicilio, primero en [DOMICILIO]; y segundo, el domicilio laboral en [DOMICILIO]); con email [CORREO ELECTRÓNICO]; y con número de teléfono móvil [TELÉFONO].

Que esta parte asume el compromiso de recibir cualquier comunicación dirigida por la oficina judicial, durante toda la fase declarativa, e, incluso, en una eventual fase de ejecución por medios telemáticos, en términos del art. 399.1 II en relación al art. 437.1, ambos LEC, consignándose a estos efectos la siguiente dirección de correo electrónico y nº [Nº] de teléfono:

Todo ello de conformidad con los siguientes hechos y fundamentos de derecho:

HECHOS

PRIMERO.- Mi mandante es propietaria de una vivienda sita en esta ciudad, calle [CALLE], heredada de sus padres en fecha [FECHA]. Se acompaña el título consistente en la escritura de manifestación y aceptación de herencia, como documento n.º [NÚMERO].

SEGUNDO.- La demandada D./Dña. [NOMBRE Y APELLIDOS] ocupa dicha vivienda en concepto de inquilina en virtud de contrato de arrendamiento celebrado en fecha [FECHA], en la que se pactó una renta mensual que asciende a la cifra de [IMPORTE], y según el cual son a cargo de la parte arrendataria las cuotas de contribución de la comunidad de propiedad horizontal, y está previsto un interés por mora en el pago a partir del quinto día anticipado de cada mes del [PORCENTAJE] % anual. Se adjunta dicho contrato como documento n.º [NÚMERO].

A los efectos del art. 439.6 LEC se hace constar expresamente los siguientes hechos:

1.- Consta a esta parte que la vivienda sobre la que versa el arrendamiento es, desde que se entregaron las llaves conforme contrato y hasta la fecha, la vivienda habitual de la demandada, su marido y sus dos hijos menores de edad.

2.- Mi cliente sólo tiene en propiedad la vivienda objeto de alquiler, y el 50% de un segundo inmueble en la misma ciudad de [LOCALIDAD], calle [CALLE]. Este inmueble constituye su vivienda habitual junto con su marido y la hija menor de ambos. Se adjunta como documento n.º [NÚMERO] certificación del Registro de la Propiedad en la cual constan estos extremos.

TERCERO.- La demandada ha dejado de pagar las rentas correspondientes a los meses [MESES IMPAGADOS], a razón de [IMPORTE] euros mensuales, así como las cuotas mensuales de la comunidad de propietarios por gastos generales que ascienden a la cantidad de [IMPORTE] euros (se adjunta copia del acta de la Junta de Propietarios de fecha [FECHA], así como el recibo devuelto por la entidad bancaria, como documentos números [Nº DE DOCUMENTO] y [Nº DE DOCUMENTO]), a lo que debe adicionarse el cálculo del interés moratorio, y todo ello hace un total de [IMPORTE] euros.

CUARTO.- Presentados al cobro los recibos con las cantidades que se reseñan en el ordinal tercero, no fueron atendidos, ni tampoco los repetidos e insistentes intentos de cobro ulteriores (se aporta carta de fecha [FECHA], en la que se solicita el inmediato pago de la deuda, como documento n.º [NÚMERO]). En relación a este extremo, se hace constar expresamente que la demandada PODRÁ ENERVAR LA ACCIÓN DE RECUPERACIÓN DE LA POSESIÓN DE LA FINCA, si requerido previamente a la celebración de la vista en los términos previstos en el art. 438.5 LEC paga al actor o pone a su disposición en el Tribunal o notarialmente, dentro del plazo conferido en el requerimiento, el importe de las cantidades reclamadas, y el de las que adeude en el momento de dicho pago. A estos efectos, se hace también constancia que mi mandante no asume el compromiso del art. 437.3 LEC, y manifiesta su voluntad de cobrar todas las cantidades debidas por la parte demandada.

QUINTO.- La parte actora manifiesta que, previo a la presentación de la presente demanda, se han llevaron a cabo negociaciones con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad, y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria; incluyéndose entre las acciones realizadas el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución.

Finalmente, mi representado envío un requerimiento fehaciente al demandado con fecha [FECHA], fijando un plazo de 30 días naturales para llegar a un acuerdo amistoso, a través del abogado que firma este escrito, el cual fue contestado por el demandado por el mismo medio, rechazando el acuerdo/ habiendo sido solo posible un acuerdo parcial, viéndonos en la necesidad de acudir a la presente vía judicial, respecto a los extremos de la controversia en los que se mantiene la discrepancia.

Acompaño como documento nº [Nº DE DOCUMENTO], el requerimiento efectuado y como documento nº [Nº DE DOCUMENTO], la contestación del demandado.

FUNDAMENTOS DE DERECHO

I.- Sobre la competencia

Art. 52.1.7.º LEC, sobre competencia territorial del Tribunal de Instancia a que me dirijo, por ser del lugar en que está sita la finca objeto de la acción de desahucio.

II.- Sobre el procedimiento a seguir

De conformidad con lo dispuesto en el art. 250.1.1º LEC, y dado que una de las acciones que se ejercita consiste en la pretensión recuperatoria de la posesión de la finca dada en arrendamiento, procede acordar el cauce del juicio verbal, con todas las especialidades contenidas en el art. 438.5 y 6 LEC para el juicio de desahucio.

III.- De la acumulación de acciones

En la presente demanda se acumulan objetivamente las acciones de desahucio de finca por falta de pago y de reclamación de rentas o cantidades análogas vencidas y no pagadas, tal y como permite expresamente el art. 437.4.3ª LEC.

Asimismo, tal y como se he expuesto en el cuerpo fáctico de este escrito, se hace constar, a todos los efectos legales, que mi mandante no asume la posibilidad facultativa prevista en el art. 437.3 LEC, en relación con las acciones acumuladas. Es decir, quiere cobrar todas las cantidades adeudadas, y no asume el compromiso de condonar al arrendatario todo o parte de la deuda y de las costas, con expresión de cantidad alguna; condicionado al desalojo voluntario de la finca dentro de ningún plazo.

IV.- De las partes

Art. 10 párrafo 1.º, en relación con el art. 250.1.1.º LEC, en armonía con lo cual está legitimado activamente mi representado en cuanto que propietaria de la vivienda dada en alquiler y titular del crédito por el precio del arriendo y por las cantidades cuyo pago tiene asumido contractualmente la arrendataria, y lo está pasivamente la demandada, en cuanto que poseedora de la vivienda por contrato de arrendamiento, y deudora de las rentas y demás cantidades de pago debido, según lo pactado.

Tratándose de un juicio verbal por razón de la materia y no por razón de la cuantía, conforme a los arts. 23.1 y 31.1 LEC, es preceptiva la intervención de procurador de los tribunales y de abogado en ejercicio, ambos habilitados ante el Tribunal, estando identificados representante y director letrado en el encabezamiento de la demanda.

V.- De la cuantía

Regla 9.ª del art. 251 LEC en lo tocante a la cuantía de la demanda por la acción recuperación del inmueble, justificando que la anualidad de renta asciende a [IMPORTE] euros ( €), la de superior valor al acumularse como principales y derivadas del mismo título la recuperatoria y la de reclamación de rentas y cantidades debidas (art. 252.2.ª LEC), lo que se deja expreso por imperio del art. 253 LEC.

VI.- De las exigencias legales de la acción de desahucio ejercitada

Tal y como se ha hecho constar en los hechos de la presente demanda, se cumplen con los requisitos exigidos en el art. 439.6 LEC. En primer lugar, mi mandante tiene constancia de que la vivienda arrendada constituye la vivienda habitual de la parte demandada.

En segundo lugar, la aquí demandante y arrendadora es la propietaria de la vivienda, y ostenta además el 50% de la titularidad de una segunda vivienda que constituye su propia vivienda habitual y la de su familia. En consecuencia, no ostenta la condición de gran tenedora de viviendas, según el art. 3.K) de la Ley 12/2023, de 24 de mayo, por el derecho a la vivienda.

VIII.- Del cumplimiento de los requisitos de procedibilidad

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

IX.- Del fondo del asunto

Las partes se encuentran vinculadas por el contrato de arrendamiento, en cuyo marco, y según el art. 1.555.1º CCiv, la parte arrendataria está obligada a pagar el precio del arrendamiento en los términos convenidos y libremente pactado, conforme el art. 17 LAU 1994, para los arrendamientos especiales de vivienda. Asimismo, en virtud de lo que disponen los arts. 1.124 párrafo 2º CCiv y 27.1 LAU 1994, que previene la acción de cumplimiento o la resolución de la obligación contractual, para la parte que hubiere cumplido su obligación. Y específicamente, y en este sentido, el art. 1.556 CCiv, que contempla la acción resolutoria por incumplimiento. Como norma especial, el art. 27.2.a) LAU 1994, a tenor del cual el arrendador podrá resolver de pleno derecho el contrato por causa de la falta de pago de la renta o de cualquiera de las cantidades cuyo pago haya asumido o corresponda al arrendatario.

En consecuencia, se debe un total de [IMPORTE] euros, por todos los conceptos reclamados, las rentas impagadas y las cuotas de comunidad. A lo que se deberá añadir el interés legal del dinero, a partir de lo dispuesto en los arts. 1.100.1º y 1.108 CCiv. Y finalmente, se reclaman las rentas y demás conceptos que se puedan devengar hasta la recuperación efectiva de la posesión del inmueble por parte de mi mandante, con arreglo a la posibilidad de condena a futuro prevista en el art. 220 LEC. La base para calcular las rentas futuras se fija para este pronunciamiento, el importe de la última mensualidad reclamada.

X.- De la enervación de las acciones ejercitadas

Conforme mandato legal del art. 439.3 LEC, se señala expresamente que la parte arrendataria puede enervar la acción de desahucio ejercitada, si, requerida previamente a la celebración de la vista en los términos previstos en el art. 438.5 LEC, paga a mi mandante o pone a su disposición en la cuenta del Tribunal, o notarialmente, dentro del plazo conferido en el requerimiento, el importe de las cantidades reclamadas, recuérdese, por cuantía de [IMPORTE] euros, y el de las que adeude en el momento de dicho pago; conforme el art. 22.4 LEC.

A tal efecto, se reseña que es la primera vez, en la vida del contrato de alquiler en virtud del cual se acciona, que se ejercita esta acción, por lo que sería la primera enervación en este caso.

XI.- De las actuaciones posteriores a la admisión de la demanda

Al ejercitarse, de manera acumulada, la acción de desahucio, se interesa que, conforme a lo dispuesto en el art. 438.5 y 6 LEC, tras la admisión de la demanda y previo a la eventual vista a celebrar; por parte del Letrado de la Administración de Justicia del Tribunal a quien tengo el honor de dirigirme:

1.- Se requiera a la arrendataria para que desaloje la vivienda en diez días y pague a mi mandante las cantidades adeudadas.

2.- Que en dicho requerimiento se exprese el día y la hora para la celebración de vista, en caso de oposición del demandado respecto al pago o concurrencia de los requisitos de enervación; y el día y la hora exactos para para el lanzamiento, en caso de que no exista dicha oposición.

3.- Que se exprese también que, en el caso en que la demandada solicite asistencia jurídica gratuita, deberá hacerlo en los tres días siguientes, con la advertencia de que la falta de oposición al requerimiento supondrá la prestación de su consentimiento a la resolución del contrato de arrendamiento que le vincula con el arrendador.

4.- Que se indique que, de mediar oposición, si no comparece a la vista, se declarará el desahucio sin más trámites, quedará citada para recibir la notificación de la sentencia que se dicte el sexto día siguiente, y se fijará día y hora exactas para que tenga lugar, en su caso, el lanzamiento, que deberá verificarse antes de treinta días desde vista, advirtiendo que, si la sentencia fuese condenatoria y no se recurriera, se procederá al lanzamiento en el día y la hora fijadas, sin necesidad de notificación posterior.

XII.- De las costas

Procederá la condena en costas de la arrendataria, con arreglo a lo que previene el art. 394.1 LEC, que instaura un principio cuasi objetivo de abono de las costas procesales por vencimiento, dado que el asunto deducido no encierra dudas de hecho ni de Derecho.

Asimismo, para el caso de que el demandado no atendiere al requerimiento de pago o no compareciese para oponerse o allanarse, o si el demandado atendiese al desalojo del inmueble sin formular oposición ni pagar la cantidad que reclamase, dispone el art. 438.5 párrafo 7º LEC que el decreto dando por terminado el juicio de desahucio, impondrá las costas al demandado, e incluirá las rentas debidas que se devenguen con posterioridad a la presentación de la demanda hasta la entrega de la posesión efectiva de la finca.

Finalmente, si se enervara la acción por la arrendataria, conforme ordena el art. 22.5 LEC, aquella será condenada al pago de las costas devengadas, salvo que las rentas y cantidades debidas no se hubiesen cobrado por causas imputables al arrendador.

En virtud de lo expuesto,

SUPLICO AL TRIBUNAL,

que teniendo por presentado este escrito con los documentos que lo acompañan y copia de todo ello, se tenga a bien admitirlos, y por interpuesta demanda de desahucio por falta de pago de la renta y acumulada reclamación de rentas y demás cantidades debidas, vencidas y no pagadas:

1.º Que se requiera por el Letrado de la Administración de Justicia al demandado para que en el plazo de diez días desaloje el inmueble y pague al actor la cantidad de [IMPORTE], advirtiendo de la posibilidad de enervación, y ejercitada, comunicándose a esta parte actora.
2.º Que para el caso de que en dicho plazo no atienda el requerimiento ni comparezca ante éste para oponerse o allanarse, se dicte decreto dando por terminado el juicio de desahucio y se proceda al lanzamiento en la fecha fijada por el Tribunal.
3.º Que para el caso de que en dicho plazo atienda el requerimiento en cuanto al desalojo del inmueble sin formular oposición ni pagar la cantidad reclamada, se dicte decreto dando por terminado el procedimiento y se me dé traslado del mismo para que pueda instar por mera solicitud el despacho de ejecución de título judicial en cuanto al pago de las cantidades reclamadas.
4.º Que se cite a las partes para la celebración de eventual vista si el demandado comparece y se opone, pidiendo desde este momento, para el caso de oposición, se dicte sentencia por la que, estimando la demanda, se decrete el desahucio de la demandada respecto de la vivienda que viene ocupando, sita en [LOCALIDAD], con condena a la expedita entrega de la misma, y al pago de la cantidad de [IMPORTE], más lo que representen las rentas devengadas en adelante y hasta la efectiva entrega de la posesión de la finca, más sus intereses moratorios, y los procesales de la ley, con expresa imposición de las costas del juicio.
5.º Que por último, de mediar oposición y si no comparece a la vista convocada, se declarará el desahucio sin más trámites, quedará citada para recibir la notificación de la sentencia que se dicte el sexto día siguiente, y se fijará día y hora exactas para que tenga lugar, en su caso, el lanzamiento, que deberá verificarse antes de treinta días desde vista, advirtiendo que, si la sentencia fuese condenatoria y no se recurriera, se procederá al lanzamiento en el día y la hora fijadas, sin necesidad de notificación posterior.

Por ser de Justicia que pido en [LUGAR], a [FECHA].

Firma de Abogado/a	Firma de Procurador/a
