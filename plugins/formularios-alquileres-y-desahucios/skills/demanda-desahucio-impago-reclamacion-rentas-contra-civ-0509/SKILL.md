---
name: demanda-desahucio-impago-reclamacion-rentas-contra-civ-0509
description: "Demanda de desahucio por impago y reclamación de rentas contra el inquilino y su fiador solidario. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de desahucio por impago y reclamación de rentas contra el inquilino y su fiador solidario

> Formulario **CIV-0509** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio verbal de desahucio que acumula pretensión recuperatoria del inmueble por falta de pago y reclamación de rentas o cantidades análogas vencidas y no pagadas contra arrendatario y fiador o avalista solidario. Adaptada a los requisitos incluidos en la Ley 12/2023, de 24 de mayo, por el derecho a la vivienda.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de desahucio por impago y reclamación de rentas contra el inquilino y su fiador solidario» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de desahucio por impago y reclamación de rentas contra el inquilino y su fiador solidario” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:demanda-desahucio-impago-reclamacion-rentas-contra-civ-0509`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (13 veces)
- [ ] LOCALIDAD (9 veces)
- [ ] FECHA (8 veces)
- [ ] NÚMERO (8 veces)
- [ ] IMPORTE (6 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] DOMICILIO (2 veces)
- [ ] LUGAR (2 veces)
- [ ] MES (2 veces)
- [ ] CALLE
- [ ] CORREO ELECTRÓNICO
- [ ] FECHAS
- [ ] FOLIO
- [ ] NOMBRE DEL NOTARIO
- [ ] Nº
- [ ] Nº DE CLÁUSULA
- [ ] Nº DE COLEGIADO/A
- [ ] Nº DE FINCA
- [ ] OTROS DATOS
- [ ] SEDE
- [ ] TELÉFONO
- [ ] TOMO

## Normas que cita el formulario

- art. 24.1 LEC
- art. 437.1 LEC
- art. 439.6 LEC
- art. 21.1 LOPJ
- art. 36.1 LEC
- art. 85.1 LOPJ
- art. 45 LEC
- art. 52.1.7.º LEC
- art. 438.5 LEC
- art. 250.1.1.º LEC
- art. 437.4.3.ª LEC
- art. 6.1.1.º LEC
- art. 7 LEC
- art. 252.2.ª LEC
- art. 23 LEC
- art. 3.k Ley 12/2023
- art. 439.7 LEC
- art. 5 Ley Orgánica 1/2025
- art. 1.124 CC
- art. 27.2 LAU
- art. 7.2 CC
- art. 1.555.1.º CC
- art. 17 LAU
- art. 27.1 LAU
- art. 1.830 CC
- art. 576 LEC
- art. 220.2 LEC
- art. 437.3 LEC
- art. 549.3 LEC
- art. 438.6 LEC

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales y de D./Dña. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], representación que acredito mediante escritura de poder otorgada a mi favor (existen tres posibilidades para otorgar el apoderamiento al Procurador de los Tribunales, conforme dispone el art. 24.1 LEC)

[OPCIONAL — opción en función de cómo se haya otorgado el poder]

[ELEGIR UNA OPCIÓN: Si el poder se otorga a través de la sede judicial electrónica / Si el poder se otorga mediante comparecencia apud acta / Si el poder se otorga ante Notario]

bajo la dirección letrada de D./Dña. [NOMBRE Y APELLIDOS], abogado/a en ejercicio, con despacho profesional abierto en [LOCALIDAD], colegiado nº [Nº DE COLEGIADO/A] del Ilustre Colegio de la Abogacía de [LOCALIDAD], ante el Tribunal comparezco y como mejor en Derecho proceda, DIGO:

Que mediante el presente escrito vengo a formular DEMANDA DE JUICIO VERBAL DE DESAHUCIO POR FALTA DE PAGO Y RECLAMACIÓN DE CANTIDADES DEBIDAS, contra D./Dña. [NOMBRE Y APELLIDOS], con domicilio, primero en [DOMICILIO]; y segundo, el domicilio laboral en [DOMICILIO]); con email [CORREO ELECTRÓNICO]; y con número de teléfono móvil [TELÉFONO].

Que esta parte asume el compromiso de recibir cualquier comunicación dirigida por la oficina judicial, durante toda la fase declarativa, e, incluso, en una eventual fase de ejecución por medios telemáticos, en términos del art. 399.1 II con relación al art. 437.1, ambos LEC, consignándose a estos efectos la siguiente dirección de correo electrónico y nº [Nº] de teléfono:

Todo ello de conformidad con los siguientes hechos y fundamentos de derecho:

HECHOS

PRIMERO.- Mi mandante es propietario del inmueble sito en [LOCALIDAD] e inscrito en el Registro de la Propiedad n.º [NÚMERO] de [LOCALIDAD], al Tomo [TOMO], Folio [FOLIO], Finca Registral [Nº DE FINCA], en virtud de escritura pública de [FECHA], otorgada en fecha [FECHA] ante el Notario de [LOCALIDAD], D./Dña. [NOMBRE Y APELLIDOS], con el número [NÚMERO] de su protocolo.

Se adjunta, como documento n.º [NÚMERO], copia de la nota simple de inscripción registral, dejando designados los archivos del Registro de la Propiedad n.º [NÚMERO] de [LOCALIDAD] y los del Notario D./Dña. [NOMBRE DEL NOTARIO], a los efectos probatorios oportunos.

SEGUNDO.- En fecha de [FECHA], mi representado suscribió contrato de arrendamiento de la vivienda descrita anteriormente con D./Dña. [NOMBRE Y APELLIDOS].

Asimismo, D./Dña. [NOMBRE Y APELLIDOS], firmó el mencionado contrato en su calidad de fiador solidario de D./Dña. [NOMBRE Y APELLIDOS]

Se adjunta, como documento n.º [NÚMERO], copia del mencionado contrato.

TERCERO.- Según la cláusula [Nº DE CLÁUSULA] del mencionado contrato, la renta quedó establecida en la cantidad de [IMPORTE] euros mensuales, debiendo efectuarse dicho pago en los cinco primeros días de cada mes mediante transferencia bancaria, en el número de cuenta reseñado en tal cláusula.

CUARTO.- El arrendatario ha dejado de pagar las rentas correspondientes a los meses de [MES] y [MES], por lo que su deuda al día de la fecha de la demanda asciende a [IMPORTE] euros ( [IMPORTE] €).

QUINTO.- A pesar de las gestiones amistosas realizadas para el cobro, los demandados no han satisfecho el crédito que se reclama haciendo caso omiso a los requerimientos de pago que se les han remitido por el abogado suscrito, y es preciso impetrar el auxilio judicial, lo que, efectivamente, se hace por medio del presente escrito.

Se acreditan estos extremos con los documentos nos. a [Nº DE DOCUMENTO] acreditativos de los requerimientos efectuados por burofax a los Sres. y [NOMBRE Y APELLIDOS], y la entrega de dichos requerimientos en su domicilios con fecha [FECHA] del presente año.

SEXTO.- A los efectos del art. 439.6 LEC se hace constar expresamente los siguientes hechos:

1.- Consta a esta parte que la vivienda sobre la que versa el arrendamiento es, desde que se entregaron las llaves conforme contrato y hasta la fecha, la vivienda habitual de la demandada, su marido y sus dos hijos menores de edad.

2.- Mi cliente sólo tiene en propiedad la vivienda objeto de alquiler, y el 50% de un segundo inmueble en la misma ciudad de [LOCALIDAD], calle [CALLE]. Este inmueble constituye su vivienda habitual junto con su marido y la hija menor de ambos. Se adjunta como documento n.º [NÚMERO] certificación del Registro de la Propiedad en la cual constan estos extremos.

SÉPTIMA.- La parte actora manifiesta que, previo a la presentación de la presente demanda, se han llevaron a cabo negociaciones con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad, y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria; incluyéndose entre las acciones realizadas el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución.

Finalmente, mi representado envío un requerimiento fehaciente al demandado con fecha [FECHA], fijando un plazo de 30 días naturales para llegar a un acuerdo amistoso, a través del abogado que firma este escrito, el cual fue contestado por el demandado por el mismo medio, rechazando el acuerdo/ habiendo sido solo posible un acuerdo parcial, viéndonos en la necesidad de acudir a la presente vía judicial, respecto a los extremos de la controversia en los que se mantiene la discrepancia.

Acompaño como documento nº [Nº DE DOCUMENTO], el requerimiento efectuado y como documento nº [Nº DE DOCUMENTO], la contestación del demandado.

A los anteriores hechos son de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN Y COMPETENCIA

La jurisdicción ordinaria es la única competente para el conocimiento de los juicios que se susciten en territorio español con arreglo a lo establecido en los tratados y convenios internacionales en los que España sea parte, en las normas de la Unión Europea y en las leyes españolas (art. 21.1 LOPJ y art. 36.1 LEC).

La competencia objetiva corresponde a la Sección Civil del Tribunal de Instancia según lo dispuesto en el art. 85.1 LOPJ y art. 45 LEC.

La competencia territorial asimismo corresponde, conforme al art. 52.1.7.º LEC, por cuanto el Tribunal es el del partido del lugar en que está sita la finca.

II.- PROCEDIMIENTO

La demanda deberá sustanciarse por las normas del juicio verbal, observándose las disposiciones contenidas en el art. 438.5 y 6 LEC para el juicio de desahucio, después de las reformas introducidas por la Ley 37/2011, de 10 de octubre, de medidas de agilización procesal; y de la Ley 4/2013, de 4 de junio, de medidas de flexibilización y fomento del mercado del alquiler de viviendas, a tenor de lo expresamente prevenido en el art. 250.1.1.º LEC, al tener por objeto pretensión recuperatoria de la posesión de la finca dada en arrendamiento.

III.- ACUMULACIÓN DE ACCIONES

En atención a la previsión expresa del art. 437.4.3.ª LEC, está legalmente admitida la acumulación objetiva de acciones en juicio verbal de las de desahucio por falta de pago y de reclamación de rentas o cantidades análogas vencidas y no pagadas, con independencia de la cantidad reclamada.

Se formula demanda contra el fiador solidario, a tenor de lo previsto en su inciso final, que dispone que " [OTROS DATOS] también podrán acumularse las acciones ejercitadas contra el fiador o avalista solidario previo requerimiento de pago no satisfecho".

IV.- CAPACIDAD Y LEGITIMACIÓN

Demandante y demandados, personas físicas, tienen capacidad para ser parte (art. 6.1.1.º LEC), titular de facultades y cargas del proceso, y asimismo plena capacidad procesal, al ser mayores de edad, sin limitación de ejercicio válido de derechos civiles, o para comparecer en juicio, en términos del art. 7 LEC, pretendiendo el actor y siendo pretendidos los demandado, en sus respectivos nombres y derechos.

Está legitimado activamente mi representado, de conformidad con lo dispuesto en el art. 10 párrafo 1.º, en relación con el art. 250.1.1.º LEC, en cuanto que propietario de la vivienda dada en renta y titular del crédito por el precio del arriendo y por las cantidades cuyo pago tienen asumido contractualmente los demandados, que a su vez lo están pasivamente en su condición de arrendatario y fiador solidario, respectivamente, de las cantidades reclamadas y, por tanto, deudores de las rentas y demás cantidades de pago debido, según lo pactado.

V.- CUANTÍA

Se hace constar que la cuantía de la demanda es de [IMPORTE] euros ( [IMPORTE] €), la correspondiente a la acción de desahucio, conforme a la anualidad de rentas de la regla 9.ª de art. 251, puesto que es de mayor valor entre las acumuladas (cfr.: art. 252.2.ª LEC).

VI.- POSTULACIÓN Y DEFENSA

Conforme a los arts. 23 y 31 LEC, se formula esta demanda por medio de Procurador de los Tribunales con poder general para pleitos y especial para percibir cantidades, con la dirección y firma de Letrado ejerciente colegiado.

VII.- EXIGENCIAS LEGALES DE LA ACCIÓN DE DESAHUCIO EJERCITADA

Tal y como se ha hecho constar en los hechos de la presente demanda, se cumplen con los requisitos exigidos en el art. 439.6 LEC. En primer lugar, mi mandante tiene constancia de que la vivienda arrendada constituye la vivienda habitual de la parte demandada.

En segundo lugar, la aquí demandante y arrendadora es la propietaria de la vivienda, y ostenta además el 50% de la titularidad de una segunda vivienda que constituye su propia vivienda habitual y la de su familia. En consecuencia, no ostenta la condición de gran tenedora de viviendas, según el art. 3.k) de la Ley 12/2023, de 24 de mayo, por el derecho a la vivienda.

Al no ostentar la indicada cualidad, no es preciso acreditar si la arrendataria está, o deja de estar, en situación de vulnerabilidad económica. En todo caso, a esta parte le consta que el contrato se ha venido cumpliendo, durante más de tres años, hasta el momento del primer impago que aquí se reclama, y no se conoce ninguna razón para pensar que D./Dña. [NOMBRE Y APELLIDOS] se encuentre en una situación o riesgo de exclusión social, conforme a la normativa autonómica que rige en la presente sede.

Por último, y también como consecuencia de la condición negativa expuesta, mi cliente no está obligada a acreditar que se ha sometido al procedimiento de conciliación o intermediación establecido por la Comunidad Autónoma de [LOCALIDAD], previsto en el art. 439.7 LEC.

VIII.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

IX.- ASUNTO DE FONDO

IX.1.- Sobre la falta de pago. Se ejercita pretensión resolutoria del arrendamiento fundada en la falta de pago de las rentas, como justa prestación por el disfrute de la vivienda cuyo uso se le confiere en virtud del arrendamiento (arts. 1.543, 1.554.1.º y 1.555.1.º CCiv). El impago de la merced arrendaticia autoriza al arrendador a promover el desahucio o pretensión recuperatoria del arrendador, dueño, usufructuario, u otro poseedor, de la finca, rústica o urbana, dada en arrendamiento —ordinario o financiero— o aparcería, una vez resuelto por incumplimiento en pronunciamiento judicial constitutivo (art. 250.1.1.º LEC).

El incumplimiento por cualquiera de las partes de las obligaciones resultantes del contrato dará derecho a la parte que hubiere cumplido las suyas a exigir el cumplimiento de la obligación o a promover la resolución del contrato de acuerdo con lo dispuesto en el art. 1.124 CCiv.

Asimismo el art. 27.2 letra a), de la LAU 1994 autoriza a resolver de pleno derecho el contrato por la falta de pago de la renta o en su caso de cualquiera de la cantidades cuyo pago haya asumido o corresponda al arrendatario; y todo ello en relación con el art. 7.2 CCiv en cuanto previene que la Ley no ampare el abuso de derecho o el ejercicio antisocial del mismo, y habiendo daño para tercero dará lugar a la correspondiente indemnización y a la adopción de las medidas judiciales que impidan la persistencia del abuso.

IX.2.- Sobre el impago de rentas vencidas. Del citado art. 1.555.1.º CCiv. resulta que el arrendatario está obligado a pagar el precio del arrendamiento en los términos convenidos, que es la renta cuya determinación regula, para los arrendamientos especiales de vivienda, el art. 17 LAU 1994, siendo alternativa genérica del art. 1.124 párrafo 2.º CCiv y del art. 27.1 LAU 1994 la acción de puro cumplimiento de la obligación contractual para la parte que hubiere cumplido su obligación.

Por otro lado, toda vez que el Sr. firma el contrato de arrendamiento como fiador solidario de la parte arrendataria, con el fin de garantizar el pago de las obligaciones que del mismo se deriven, y en aplicación de las disposiciones generales de las obligaciones (arts. 1.091, 1.100, 1.101, 1.108, 1.113, 1.124, 1.144, 1.822 CCiv y siguientes, y concordantes), y en virtud de lo establecido en el art. 1.834 en relación con el art. 1.830 CCiv, todos del Código Civil, éste deberá ser condenado al pago de las cantidades adeudadas en la condición que ostenta de deudor subsidiario.

IX.3.- Sobre la mora. Al haber incumplido el arrendatario la parte que le incumbía en el contrato, incurre en mora según se desprende de los arts. 1.100, 1.101, 1.108 y 1.124 CCiv, que a falta de pacto contractual específico, supone el devengo de intereses al tipo del legal del dinero desde la intimación de pago de rentas debidas al deudor demandado, por la interposición de la demanda.

Y conforme al art. 576 LEC, tendrá que abonar además los intereses legales por mora procesal desde el dictado de la sentencia condenatoria.

IX.4.- Por último, al amparo de lo dispuesto en el art. 220.2 LEC, se reclaman también expresamente las rentas debidas que se devenguen con posterioridad a la presentación de esta demanda hasta la entrega de la posesión efectiva de la finca.

La base para calcular las rentas futuras se fija para este pronunciamiento de un futurible el importe de la última mensualidad reclamada en la presente demanda.

X.- ENERVACIÓN

A tenor del art. 22.4 párrafo 2.º LEC, no es viable la enervación de la acción de desahucio, a pesar de que el arrendatario, requerido previamente a la celebración de la vista en los términos previstos en el art. 438.5 LEC pague o ponga a disposición del actor en la cuenta del Tribunal, o notarialmente, el importe de las cantidades que aquí se reclaman, y el de las que adeuden en el momento de dicho pago, toda vez que se ha ejercido precedentemente esta facultad por D./Dña. [NOMBRE Y APELLIDOS] dictándose auto de fecha [FECHA] en autos de juicio verbal n.º [NÚMERO] que se siguió en este Tribunal de Instancia, cuya copia testimoniada se acompaña como documento n.º [NÚMERO].

Por consiguiente, si D./Dña. [NOMBRE Y APELLIDOS] pretende nueva enervación, ante la comunicación a esta parte, se formulará oposición, debiéndose citar a las partes para celebrar la vista, donde se resolverá su improcedencia.

XI.- SOLICITUD ANTICIPADA DE LANZAMIENTO

De conformidad con el art. 437.3 "in fine" LEC, esta parte interesa desde esta misma demanda que se tenga por solicitada la ejecución del lanzamiento en la fecha y hora que se fije por el Tribunal a los efectos señalados en el art. 549.3 LEC, esto es, siendo suficiente dicha solicitud para que la sentencia condenatoria o el decreto que ponga fin al desahucio vaya a la ejecución directa, sin necesidad de ningún otro trámite para proceder al lanzamiento en el día y hora señalados en la propia sentencia o al ordenar la realización del requerimiento al demandado.

Conforme al art. 438.6 LEC en la resolución que se dicte teniendo por opuesto al demandado el Tribunal fijará día y hora para que tenga lugar, en su caso, el lanzamiento, que deberá producirse antes de treinta días desde la fecha de la vista, advirtiendo al demandado que, en caso de que la sentencia sea condenatoria y no se recurra, se procederá al lanzamiento en la fecha fijada, sin necesidad de notificación posterior.

XII.- COSTAS

Conforme al art. 394 LEC, las costas del procedimiento habrán de imponerse al demandado, si fuere vencido, y aunque se allanare, por su evidente mala fe, al haber forzado el proceso ante los intentos extrajudiciales, repetidos y fallidos, de cobro y mutuo disenso del contrato.

Por lo expuesto,

SUPLICO AL TRIBUNAL,

que teniendo por presentado este escrito con los documentos que lo acompañan y copia de todo ello, se tenga a bien admitirlos, y por interpuesta demanda de juicio verbal desahucio por falta de pago de la renta y acumulada reclamación de rentas y demás cantidades debidas, tras los trámites procesales oportunos, se requiera por el Letrado de la Administración de Justicia al demandado para que desaloje el inmueble y pague al actor la cantidad de [IMPORTE] euros, por término de diez días, conforme al art. 438.5 LEC, dictándose el correspondiente Decreto según el resultado de los requerimientos indicados, o en caso de formularse oposición en dicho plazo, tras la celebración de la oportuna vista, se dicte en su día sentencia por la que con estimación total de la demanda se declare haber lugar al desahucio, así como resuelto el contrato de arrendamiento, y se condene al arrendatario al pago de las cantidades adeudadas, de las que responderá también, de forma solidaria, el fiador D./Dña. [NOMBRE Y APELLIDOS], más la cantidad que resulte por las rentas debidas que se devenguen con posterioridad hasta la entrega de la posesión efectiva de la finca, con sus intereses, con expresa imposición de las costas procesales a la parte demandada.

Es justicia que pido en [LUGAR], a [FECHA].

PRIMER OTROSÍ DIGO, que se deja expresamente indicado que el arrendatario no ostenta la facultad de enervar la presente acción, de conformidad con lo dispuesto en el art. 439.3 en relación con lo dispuesto en el art. 22.4, ambos de la LEC.

SUPLICO AL TRIBUNAL. Que tenga hecha la anterior manifestación.

SEGUNDO OTROSÍ DIGO que, al amparo de lo previsto en el art. 438.6 LEC, se solicita que en la resolución que se dicte teniendo por opuesto al demandado se fije por el Tribunal el día y la hora para que tenga lugar, en su caso, el lanzamiento, advirtiendo al demandado que, celebrada la vista y dictada sentencia, de ser esta condenatoria y no se recurriera, se procederá a tal lanzamiento en la fecha fijada, sin necesidad de notificación posterior.

SUPLICO AL TRIBUNAL. Que tenga por efectuada la petición consignada, efectuando los requerimientos, advertencias y emplazamientos necesarios para su correcto cumplimiento.

TERCER OTROSÍ DIGO, que conforme autoriza el art. 437.3 LEC, expresamente queda interesado, para el caso de ser dictada resolución estimatoria de nuestra pretensión resolutoria del contrato, se ejecute la misma sin necesidad de ulterior petición, procediéndose al lanzamiento del demandado en la fecha y hora que se fijen por el Tribunal a los efectos señalados en el art. 549.3 LEC y sin que sea preciso plazo de espera para materializar el lanzamiento, conforme dispone el apartado 4 del indicado precepto.

SUPLICO DE NUEVO AL TRIBUNAL. Que tenga por interesada la ejecución del desahucio para el caso de ser dictada sentencia estimatoria de nuestra pretensión resolutoria.

Por ser de Justicia que pido en [LUGAR], a [FECHA].

Firma de Abogado/a	Firma de Procurador/a
