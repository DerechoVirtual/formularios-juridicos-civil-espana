---
name: demanda-desahucio-impago-rentas-vivienda-sin-civ-0579
description: "Demanda de desahucio por impago y rentas de vivienda, sin enervación por requerimiento fehaciente. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de desahucio por impago y rentas de vivienda, sin enervación por requerimiento fehaciente

> Formulario **CIV-0579** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio verbal de desahucio por falta de pago de la renta del arrendamiento de una vivienda en finca urbana, así como de las cuotas mensuales de la comunidad de propietarios por gastos generales y reclamación de cantidades debidas, interpuesta por el usufructuario vitalicio de la misma. No puede el arrendatario enervar la acción por haber sido requerido fehacientemente de pago con treinta días de antelación a la presentación de la demanda sin haber satisfecho las rentas en el momento de presentación de la misma.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de desahucio por impago y rentas de vivienda, sin enervación por requerimiento fehaciente» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de desahucio por impago y rentas de vivienda, sin enervación por requerimiento fehaciente” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:demanda-desahucio-impago-rentas-vivienda-sin-civ-0579`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (8 veces)
- [ ] FECHA (7 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] Nº DE DOCUMENTO (5 veces)
- [ ] NÚMERO (5 veces)
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
- art. 250.1.1.º LEC
- art. 251 LEC
- art. 252.2.ª LEC
- art. 253 LEC
- art. 5 Ley Orgánica 1/2025
- art. 17 LAU
- art. 27.1 LAU
- art. 27.2.a LAU
- art. 3.k Ley 12/2023

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

Todo ello de conformidad con los siguientes:

HECHOS

PRIMERO.- Mi mandante es usufructuario vitalicio de una vivienda sita en esta ciudad, calle [CALLE], número [NÚMERO] Se acompaña el título consistente en la escritura de manifestación y aceptación de herencia, como documento n.º [NÚMERO].

SEGUNDO.- La demandada D./Dña. [NOMBRE Y APELLIDOS] ocupa dicha vivienda en concepto de inquilina en virtud de contrato de arrendamiento celebrado en fecha [FECHA], en la que se pactó una renta mensual que asciende a la cifra de [IMPORTE], que son a cargo del arrendatario las cuotas de contribución de la comunidad de propiedad horizontal, y un interés por mora en el pago a partir del quinto día anticipado de cada mes del [PORCENTAJE] % anual. Se adjunta dicho contrato como documento n.º [NÚMERO].

TERCERO.- La demandada ha dejado de pagar las rentas correspondientes a los meses [MESES IMPAGADOS], a razón de [IMPORTE] euros mensuales, así como las cuotas mensuales de la comunidad de propietarios por gastos generales que ascienden a la cantidad de [IMPORTE] euros (se adjunta copia del acta de la Junta de Propietarios de fecha [FECHA], así como el recibo devuelto por la entidad bancaria, como documentos números [Nº DE DOCUMENTO] y [Nº DE DOCUMENTO]), a lo que debe adicionarse el cálculo del interés moratorio, y todo ello hace un total de [IMPORTE] euros.

CUARTO.- Presentados al cobro los recibos con las cantidades que se reseñan en el ordinal tercero, no fueron atendidos, ni tampoco los repetidos e insistentes intentos de cobro ulteriores (se aporta carta de fecha [FECHA], en la que se solicita el inmediato pago de la deuda, como documento n.º [NÚMERO]).

QUINTO.- Mi mandante requirió de pago al demandado mediante carta certificada con acuse de recibo que fue recibida por el demandado en fecha [FECHA] Se acompañan como documentos números [Nº DE DOCUMENTO] justificantes de dicha carta certificada y el acuse de recibo firmado, señalando a los oportunos efectos los archivos del Servicio de Correos y Telégrafos; por lo que se indica expresamente que el demandado NO PODRÁ ENERVAR LA ACCIÓN.

(Si se ha requerido notarialmente de pago se indicará "Mi mandante requirió notarialmente al demandado, en fecha [FECHA], reclamando las cantidades reseñadas en el ordinal tercero. Ello se acredita con la primera copia de acta de requerimiento notarial, que se acompaña como documento númeroseñalándose igualmente a los oportunos efectos el protocolo del Notario Sr./a.")

SEXTO.- A los efectos del art. 439.6 LEC se hace constar expresamente los siguientes hechos:

1.- Consta a esta parte que la vivienda sobre la que versa el arrendamiento es, desde que se entregaron las llaves conforme contrato y hasta la fecha, la vivienda habitual de la demandada, su marido y sus dos hijos menores de edad.

2.- Mi cliente sólo tiene en propiedad la vivienda objeto de alquiler, y el 50% de un segundo inmueble en la misma ciudad de [LOCALIDAD], calle [CALLE]. Este inmueble constituye su vivienda habitual junto con su marido y la hija menor de ambos. Se adjunta como documento n.º [NÚMERO] certificación del Registro de la Propiedad en la cual constan estos extremos.

SÉPTIMO.- La parte actora manifiesta que, previo a la presentación de la presente demanda, se han llevaron a cabo negociaciones con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad, y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria; incluyéndose entre las acciones realizadas el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución.

Finalmente, mi representado envío un requerimiento fehaciente al demandado con fecha [FECHA], fijando un plazo de 30 días naturales para llegar a un acuerdo amistoso, a través del abogado que firma este escrito, el cual fue contestado por el demandado por el mismo medio, rechazando el acuerdo/ habiendo sido solo posible un acuerdo parcial, viéndonos en la necesidad de acudir a la presente vía judicial, respecto a los extremos de la controversia en los que se mantiene la discrepancia.

Acompaño como documento nº [Nº DE DOCUMENTO], el requerimiento efectuado y como documento nº [Nº DE DOCUMENTO], la contestación del demandado.

FUNDAMENTOS DE DERECHO

I

Art. 52.1.7.º LEC, sobre competencia territorial del Tribunal de Instancia a que me dirijo, por ser del lugar en que está sita la finca objeto de la acción de desahucio.

II

Art. 250.1.1.º LEC, sobre la sustanciación de la pretensión recuperatoria de la posesión de la finca dada en arrendamiento, a través del cauce del juicio verbal, observándose las disposiciones contenidas en el art. 438.5 y 6 LEC para el juicio de desahucio.

III

Art. 437.4.3.ª LEC, que admite la acumulación objetiva de acciones en juicio verbal de la de desahucio de finca por falta de pago y de reclamación de rentas o cantidades análogas vencidas y no pagadas, con independencia de la cantidad reclamada.

IV

Art. 10 párrafo 1.º, en relación con el art. 250.1.1.º LEC, en armonía con lo cual está legitimado activamente mi representado en cuanto que usufructuario vitalicio de la vivienda dada en renta y titular del crédito por el precio del arriendo y por las cantidades cuyo pago tiene asumido contractualmente la arrendataria, y lo está pasivamente la demandada, en cuanto que poseedora de la vivienda por contrato de arrendamiento, y deudora de las rentas y demás cantidades de pago debido, según lo pactado.

Tratándose de un juicio verbal por razón de la materia y no por razón de la cuantía, conforme a los arts. 23.1 y 31.1 LEC, es preceptiva la intervención de procurador de los tribunales y de abogado en ejercicio, ambos habilitados ante el Tribunal, estando identificados representante y director letrado en el encabezamiento de la demanda.

V

Regla 9.ª del art. 251 LEC en lo tocante a la cuantía de la demanda por la acción recuperación del inmueble, justificando que la anualidad de renta asciende a [IMPORTE] euros ( [IMPORTE] €), la de superior valor al acumularse como principales y derivadas del mismo título la recuperatoria y la de reclamación de rentas y cantidades debidas (art. 252.2.ª LEC), lo que se deja expreso por imperio del art. 253 LEC.

VI

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

VII

Art. 1.555.1.º CCiv, conforme al que el arrendatario está obligado a pagar el precio del arrendamiento en los términos convenidos; art. 17 LAU 1994, que regula la determinación de la renta en los arrendamientos especiales de vivienda; art. 1.124 párrafo 2.º CCiv y art. 27.1 LAU 1994, que previene la acción de cumplimiento de la obligación contractual para la parte que hubiere cumplido su obligación.

Arts. 1.100.1.º y 1.108 CCiv, a propósito del interés moratorio, por declararlo el contrato y establecer su cuantificación.

VIII

Arts. 1.556 CCiv, que contempla la acción resolutoria por incumplimiento, y art. 27.2.a) LAU 1994 según el que el arrendador podrá resolver de pleno derecho el contrato por causa de la falta de pago de la renta o de cualquiera de las cantidades cuyo pago haya asumido o corresponda al arrendatario.

IX

Art. 22.4 párrafo 2.º LEC, a tenor del cual no podrá el arrendatario enervar la acción si ha sido requerido fehacientemente de pago con treinta días de antelación a la presentación de la demanda sin haber satisfecho las rentas en el momento de presentación de la misma.

X

Tal y como se ha hecho constar en los hechos de la presente demanda, se cumplen con los requisitos exigidos en el art. 439.6 LEC de la acción de desahucio ejercitada. En primer lugar, mi mandante tiene constancia de que la vivienda arrendada constituye la vivienda habitual de la parte demandada.

En segundo lugar, la aquí demandante y arrendadora es la propietaria de la vivienda, y ostenta además el 50% de la titularidad de una segunda vivienda que constituye su propia vivienda habitual y la de su familia. En consecuencia, no ostenta la condición de gran tenedora de viviendas, según el art. 3.k) de la Ley 12/2023, de 24 de mayo, por el derecho a la vivienda.

Por otro lado, desde la STC 26/2025, de 29 de enero, no es obligatorio presentar informe de vulnerabilidad ni acreditar mediación previa.

XI

Art. 394.1 LEC, que instaura un principio cuasiobjetivo de abono de las costas procesales por vencimiento, siendo que el asunto deducido no encierra dudas de hecho ni de Derecho.

En virtud de lo expuesto,

SUPLICO AL TRIBUNAL,

que teniendo por presentado este escrito con los documentos que lo acompañan y copia de todo ello, se tenga a bien admitirlos, y por interpuesta demanda de desahucio por falta de pago de la renta y acumulada reclamación de rentas y demás cantidades debidas, vencidas y no pagadas:

1.º Que se requiera por el Letrado de la Administración de Justicia al demandado para que en el plazo de diez días desaloje el inmueble y pague al actor la cantidad de [IMPORTE], con advertencia de la imposibilidad de enervación.
2.º Que para el caso de que en dicho plazo no atienda el requerimiento ni comparezca ante éste para oponerse o allanarse, se dicte decreto dando por terminado el juicio de desahucio y se proceda al lanzamiento en la fecha fijada por el Tribunal.
3.º Que para el caso de que en dicho plazo atienda el requerimiento en cuanto al desalojo del inmueble sin formular oposición ni pagar la cantidad reclamada, se dicte decreto dando por terminado el procedimiento y se me dé traslado del mismo para que pueda instar por mera solicitud el despacho de ejecución de título judicial en cuanto al pago de las cantidades reclamadas.
4.º Que se cite las partes para la celebración de eventual vista si el demandado comparece y se opone, pidiendo desde este momento, para el caso de oposición, se dicte sentencia por la que, estimando la demanda, se decrete el desahucio de la demandada respecto de la vivienda que viene ocupando, sita en [LOCALIDAD], con condena a la expedita entrega de la misma, y al pago de la cantidad de [IMPORTE], más sus intereses moratorios, y los procesales de la ley, con expresa imposición de las costas del juicio.

Por ser de Justicia que pido en [LUGAR], a [FECHA].

Firma de Abogado/a	Firma de Procurador/a
