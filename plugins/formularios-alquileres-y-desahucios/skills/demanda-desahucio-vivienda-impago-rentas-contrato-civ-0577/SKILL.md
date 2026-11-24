---
name: demanda-desahucio-vivienda-impago-rentas-contrato-civ-0577
description: "Demanda de desahucio de vivienda por impago de rentas (contrato posterior a 1995), sin enervación. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de desahucio de vivienda por impago de rentas (contrato posterior a 1995), sin enervación

> Formulario **CIV-0577** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio verbal de desahucio en ejercicio de acción recuperatoria por falta de pago y de reclamación de las rentas impagadas y cantidades futuras. Se recoge la negativa de la enervación. Contrato posterior al 1 de enero de 1995.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de desahucio de vivienda por impago de rentas (contrato posterior a 1995), sin enervación» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de desahucio de vivienda por impago de rentas (contrato posterior a 1995), sin enervación” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:demanda-desahucio-vivienda-impago-rentas-contrato-civ-0577`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (9 veces)
- [ ] LOCALIDAD (6 veces)
- [ ] IMPORTE (5 veces)
- [ ] Nº DE DOCUMENTO (5 veces)
- [ ] FECHA (4 veces)
- [ ] DOMICILIO (2 veces)
- [ ] MES (2 veces)
- [ ] CALLE
- [ ] CORREO ELECTRÓNICO
- [ ] FECHAS
- [ ] LUGAR
- [ ] Nº
- [ ] Nº DE COLEGIADO/A
- [ ] NÚMERO
- [ ] SEDE
- [ ] TELÉFONO

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
- art. 7.1 LEC
- art. 27.2.a LAU
- art. 1.555.1.º CC
- art. 251 LEC
- art. 252.2.ª LEC
- art. 23 LEC
- art. 3.k Ley 12/2023
- art. 5 Ley Orgánica 1/2025
- art. 1.124 CC
- art. 7.2 CC
- art. 17 LAU
- art. 27.1 LAU
- art. 576 LEC
- art. 220.2 LEC
- art. 437.3 LEC
- art. 438.6 LEC
- art. 549.3 LEC
- art. 394 LEC

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

Que mediante el presente escrito vengo a formular DEMANDA DE JUICIO VERBAL DE DESAHUCIO POR FALTA DE PAGO y RECLAMACIÓN DE RENTAS DEBIDAS, contra D./Dña. [NOMBRE Y APELLIDOS], con domicilio, primero en [DOMICILIO]; y segundo, el domicilio laboral en [DOMICILIO]); con email [CORREO ELECTRÓNICO]; y con número de teléfono móvil [TELÉFONO].

Que esta parte asume el compromiso de recibir cualquier comunicación dirigida por la oficina judicial, durante toda la fase declarativa, e, incluso, en una eventual fase de ejecución por medios telemáticos, en términos del art. 399.1 II en relación al art. 437.1, ambos LEC, consignándose a estos efectos la siguiente dirección de correo electrónico y nº [Nº] de teléfono:

Todo ello de conformidad con los siguientes hechos y fundamentos de derecho:

HECHOS

PRIMERO.- Mi mandante, D./Dña. [NOMBRE Y APELLIDOS], es propietario de la vivienda sita en [LOCALIDAD]. Se acompaña el título de propiedad —escritura de compraventa— como documento n.º [Nº DE DOCUMENTO].

SEGUNDO.- El demandado D./Dña. [NOMBRE Y APELLIDOS], ocupa la antedicha vivienda en concepto de inquilino en virtud de contrato de arrendamiento celebrado en fecha [FECHA], por plazo de un año y renta mensual de [IMPORTE] euros ( €), el cual se ha venido prorrogando tácitamente. Se acompaña dicho contrato como documento n.º [Nº DE DOCUMENTO].

TERCERO.- El demandado D./Dña. [NOMBRE Y APELLIDOS], ha dejado de pagar las rentas correspondientes a los meses de [MES] y [MES], por lo que su deuda al día de la fecha de la demanda asciende a [IMPORTE] euros ( €).

CUARTO.- A pesar de las gestiones amistosas realizadas para el cobro, el demandado no ha satisfecho el crédito que se reclama haciendo caso omiso a los requerimientos que se le han remitido por el abogado suscrito, y es preciso impetrar el auxilio judicial, lo que, efectivamente, se hace por medio del presente escrito.

Se acreditan estos extremos con los documentos númerosy acreditativos del requerimiento efectuado por burofax al Sr./a. [NOMBRE Y APELLIDOS], y la entrega de dicho requerimiento en su domicilio con fecha [FECHA] del presente año.

QUINTO.- A los efectos del art. 439.6 LEC se hace constar expresamente los siguientes hechos:

1.- Consta a esta parte que la vivienda sobre la que versa el arrendamiento es, desde que se entregaron las llaves conforme contrato y hasta la fecha, la vivienda habitual de la demandada, su marido y sus dos hijos menores de edad.

2.- Mi cliente sólo tiene en propiedad la vivienda objeto de alquiler, y el 50% de un segundo inmueble en la misma ciudad de [LOCALIDAD], calle [CALLE]. Este inmueble constituye su vivienda habitual junto con su marido y la hija menor de ambos. Se adjunta como documento n.º [NÚMERO] certificación del Registro de la Propiedad en la cual constan estos extremos.

SEXTO.- La parte actora manifiesta que, previo a la presentación de la presente demanda, se han llevaron a cabo negociaciones con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad, y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria; incluyéndose entre las acciones realizadas el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución.

Finalmente, mi representado envío un requerimiento fehaciente al demandado con fecha [FECHA], fijando un plazo de 30 días naturales para llegar a un acuerdo amistoso, a través del abogado que firma este escrito, el cual fue contestado por el demandado por el mismo medio, rechazando el acuerdo/ habiendo sido solo posible un acuerdo parcial, viéndonos en la necesidad de acudir a la presente vía judicial, respecto a los extremos de la controversia en los que se mantiene la discrepancia.

Acompaño como documento nº [Nº DE DOCUMENTO], el requerimiento efectuado y como documento nº [Nº DE DOCUMENTO], la contestación del demandado.

A los anteriores hechos son de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN Y COMPETENCIA

I.1.-La jurisdicción ordinaria es la única competente para el conocimiento de los juicios que se susciten en territorio español con arreglo a lo establecido en los tratados y convenios internacionales en los que España sea parte, en las normas de la Unión Europea y en las leyes españolas (art. 21.1 LOPJ y art. 36.1 LEC).

I.2.- La competencia objetiva corresponde al Tribunal de Instancia según lo dispuesto en el art. 85.1º LOPJ y art. 45 LEC.

I.3.- La competencia territorial asimismo corresponde, conforme al art. 52.1.7.º LEC, por cuanto el Tribunal es el del partido del lugar en que está sita la finca.

II.- PROCEDIMIENTO.

La demanda deberá sustanciarse por las normas del juicio verbal, observándose las disposiciones contenidas en el art. 438.5 y 6 LEC para el juicio de desahucio, a tenor de lo expresamente prevenido en el art. 250.1.1.º LEC, al tener por objeto pretensión recuperatoria de la posesión de la finca dada en arrendamiento.

III.- ACUMULACIÓN DE ACCIONES.

En atención a la previsión expresa del art. 437.4.3.ª LEC, está legalmente admitida la acumulación objetiva de acciones en juicio verbal de las de desahucio por falta de pago y de reclamación de rentas o cantidades análogas vencidas y no pagadas, con independencia de la cantidad reclamada.

IV.- CAPACIDAD Y LEGITIMACIÓN

IV.1.-Demandante y demandado, personas físicas, tienen capacidad para ser parte (art. 6.1.1.º LEC), titular de facultades y cargas del proceso, y asimismo plena capacidad procesal, al ser mayores de edad, sin limitación de ejercicio válido de derechos civiles, o para comparecer en juicio, en términos del art. 7.1 LEC, pretendiendo el actor y siendo pretendido el demandado, en sus respectivos nombres y derechos.

IV.2.-Corresponde la legitimación activa a mi mandante por tener la posesión mediata de la finca a título de dueño y por haber celebrado el contrato de arrendamiento de vivienda con el demandado, por lo que es titular del derecho a resolver el contrato por incumplimiento, obteniendo la recuperación de la posesión inmediata, y a cobrar las rentas vencidas y no pagadas (arts. 1.546 y 1.569 CC y art. 27.2.a) LAU 1994).

La legitimación pasiva corresponde al demandado como arrendatario poseedor, conforme al art. 250.1.1.º LEC, y como deudor por impago de las rentas pactadas, según el art. 1.555.1.º CC.

V.- CUANTÍA.

Se hace constar que la cuantía de la demanda es de [IMPORTE] euros ( €), la correspondiente a la acción de desahucio, conforme a la anualidad de rentas de la regla 9.ª del art. 251 LEC, puesto que es de mayor valor entre las acumuladas (cfr.: art. 252.2.ª LEC).

VI.- POSTULACIÓN Y DEFENSA.

Conforme a los arts. 23 y 31 LEC, se formula esta demanda por medio de Procurador de los Tribunales con poder general para pleitos y especial para percibir cantidades, con la dirección y firma de Letrado ejerciente colegiado.

VII.- EXIGENCIAS LEGALES DE LA ACCIÓN DE DESAHUCIO EJERCITADA

Tal y como se ha hecho constar en los hechos de la presente demanda, se cumplen con los requisitos exigidos en el art. 439.6 LEC. En primer lugar, mi mandante tiene constancia de que la vivienda arrendada constituye la vivienda habitual de la parte demandada.

En segundo lugar, la aquí demandante y arrendadora es la propietaria de la vivienda, y ostenta además el 50% de la titularidad de una segunda vivienda que constituye su propia vivienda habitual y la de su familia. En consecuencia, no ostenta la condición de gran tenedora de viviendas, según el art. 3.k) de la Ley 12/2023, de 24 de mayo, por el derecho a la vivienda.

Por lo demás, desde la STC 26/2025, de 29 de enero, no es obligatorio presentar informe de vulnerabilidad ni acreditar mediación previa.

VIII.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

IX.- ASUNTO DE FONDO

IX.1.- Sobre la falta de pago. Se ejercita pretensión resolutoria del arrendamiento fundada en la falta de pago de las rentas, como justa prestación por el disfrute de la vivienda cuyo uso se le confiere en virtud del arrendamiento (arts. 1.543, 1.554.1.º y 1.555.1.º CC). El impago de la merced arrendaticia autoriza al arrendador a promover el desahucio o pretensión recuperatoria del arrendador, dueño, usufructuario, u otro poseedor, de la finca, rústica o urbana, dada en arrendamiento —ordinario o financiero— o aparcería, una vez resuelto por incumplimiento en pronunciamiento judicial constitutivo (art. 250.1.1.º LEC).

El incumplimiento por cualquiera de las partes de las obligaciones resultantes del contrato dará derecho a la parte que hubiere cumplido las suyas a exigir el cumplimiento de la obligación o a promover la resolución del contrato de acuerdo con lo dispuesto en el art. 1.124 CC.

Asimismo el art. 27.2.a) LAU 1994 autoriza a resolver de pleno derecho el contrato por la falta de pago de la renta o en su caso de cualquiera de las cantidades cuyo pago haya asumido o corresponda al arrendatario; y todo ello en relación con el art. 7.2 CC en cuanto previene que la Ley no ampare el abuso de derecho o el ejercicio antisocial del mismo, y habiendo daño para tercero dará lugar a la correspondiente indemnización y a la adopción de las medidas judiciales que impidan la persistencia del abuso.

IX.2.-Sobre el impago de rentas vencidas. Del citado art. 1.555.1.º CC resulta que el arrendatario está obligado a pagar el precio del arrendamiento en los términos convenidos, que es la renta cuya determinación regula, para los arrendamientos especiales de vivienda, el art. 17 LAU 1994, siendo alternativa genérica del art. 1.124 párrafo 2.º CC y del art. 27.1 LAU 1994 la acción de puro cumplimiento de la obligación contractual para la parte que hubiere cumplido su obligación.

IX.3.- Sobre la mora. Al haber incumplido el arrendatario la parte que le incumbía en el contrato, incurre en mora según se desprende de los arts. 1.100, 1.101, 1.108 y 1.124 CC, que a falta de pacto contractual específico, supone el devengo de intereses al tipo del legal del dinero desde la intimación de pago de rentas debidas al deudor demandado, por la interposición de la demanda.

Y conforme al art. 576 LEC, tendrá que abonar además los intereses legales por mora procesal desde el dictado de la sentencia condenatoria

IX.4.- Sobre la condena a futuro. El art. 220.2 LEC, en los casos de reclamaciones de rentas periódicas, cuando la acción de reclamación se acumule a la acción de desahucio, permite que, reclamándose expresamente, la sentencia, el auto o el decreto que haya de dictarse incluya la condena a satisfacer también las rentas debidas que se devenguen con posterioridad a la presentación de la demanda hasta la entrega de la posesión efectiva de la finca.

Asimismo, para el caso de que el demandado no atendiere al requerimiento de pago o no compareciese para oponerse o allanarse, o si el demandado atendiese al desalojo del inmueble sin formular oposición ni pagar la cantidad que reclamase, dispone el art. 438.5 párrafo 7.º LEC que el decreto dando por terminado el juicio de desahucio, impondrá las costas al demandado, e incluirá las rentas debidas que se devenguen con posterioridad a la presentación de la demanda hasta la entrega de la posesión efectiva de la finca.

La base para calcular las rentas futuras se fija para este pronunciamiento de un futurible el importe de la última mensualidad reclamada en la presente demanda.

X.- ENERVACIÓN.

A tenor del art. 22.4 párrafo 1.º LEC, no es viable la enervación de la acción de desahucio, a pesar de que el arrendatario, requerido previamente a la celebración de la vista en los términos previstos en el art. 438.5 LEC pague o ponga a disposición del actor en la cuenta del Tribunal, o notarialmente, el importe de las cantidades que aquí se reclaman, y el de las que adeuden en el momento de dicho pago, toda vez que se ha ejercido precedentemente esta facultad por D./Dña. [NOMBRE Y APELLIDOS] dictándose auto de fechaen autos de juicio verbal núm.que se siguió en este Tribunal de Instancia, cuya copia testimoniada se acompaña como documento n.º [Nº DE DOCUMENTO].

Por consiguiente, si el demandado pretende nueva enervación, ante la comunicación a esta parte, se formulará oposición, debiéndose citar a las partes para celebrar la vista, donde se resolverá su improcedencia.

XI.- SOLICITUD ANTICIPADA DE LANZAMIENTO.

Como previene el inciso último de art. 437.3 LEC, esta parte interesa que se tenga ya por solicitada la ejecución del lanzamiento en la fecha y hora que se fijará por el Tribunal, y, por tanto, no habrá de reiterarse la solicitud una vez firme la resolución que hubiera de dictarse.

Conforme al art. 438.6 LEC en la resolución que se dicte teniendo por opuesto al demandado el Tribunal fijará día y hora para que tenga lugar, en su caso, el lanzamiento, que deberá producirse antes de treinta días desde la fecha de la vista, advirtiendo al demandado que, en caso de que la sentencia sea condenatoria y no se recurra, se procederá al lanzamiento en la fecha fijada, sin necesidad de notificación posterior.

Asimismo, dispone el art. 549.3 LEC que en la sentencia condenatoria de desahucio por falta de pago de las rentas o cantidades debidas, o en el decreto que ponga fin al desahucio si no hubiera oposición al requerimiento, la solicitud de su ejecución en la demanda de desahucio será suficiente para la ejecución directa de dicha resolución, sin necesidad de ningún otro trámite para proceder al lanzamiento en el día y hora señalados en la propia sentencia o en la fecha que se hubiera fijado al ordenar la realización del requerimiento al demandado.

XII.- COSTAS.

Conforme al art. 394 LEC, las costas del procedimiento habrán de imponerse al demandado, si fuere vencido, y aunque se allanare, por su evidente mala fe, al haber forzado el proceso ante los intentos extrajudiciales, repetidos y fallidos, de cobro y mutuo disenso del contrato.

Por lo expuesto,

SUPLICO AL TRIBUNAL,

que teniendo por presentado este escrito con los documentos que lo acompañan y copia de todo ello, se tenga a bien admitirlos, y por interpuesta demanda de juicio verbal desahucio por falta de pago de la renta y acumulada reclamación de rentas y demás cantidades debidas:

1.º Que se requiera por el Letrado de la Administración de Justicia al demandado para que en el plazo de diez días desaloje el inmueble y pague al actor la cantidad de [IMPORTE], con advertencia de la imposibilidad de enervación.
2.º Que para el caso de que en dicho plazo no atienda el requerimiento ni comparezca ante éste para oponerse o allanarse, se dicte decreto dando por terminado el juicio de desahucio y se proceda al lanzamiento en la fecha fijada por el Tribunal.
3.º Que para el caso de que en dicho plazo atienda el requerimiento en cuanto al desalojo del inmueble sin formular oposición ni pagar la cantidad reclamada, se dicte decreto dando por terminado el procedimiento y se me dé traslado del mismo para que pueda instar por mera solicitud el despacho de ejecución de título judicial en cuanto al pago de las cantidades reclamadas.
4.º Que se cite a las partes para la celebración de eventual vista si el demandado comparece y se opone, pidiendo desde este momento, para el caso de oposición, se dicte sentencia por la que, estimando la demanda, se decrete el desahucio de la demandada respecto de la finca que viene ocupando, sita en [LOCALIDAD], con condena a la expedita entrega de la misma, y al pago de la cantidad de [IMPORTE] que adeuda hasta estos momentos, más la cantidad que resulte por las rentas debidas que se devenguen con posterioridad hasta la entrega de la posesión efectiva de la finca, con sus intereses, fijándose por el Tribunal día y hora para que tenga lugar, el lanzamiento, antes de treinta días desde la fecha de la vista, de modo que a su firmeza se proceda a tal lanzamiento, sin necesidad de notificación posterior, y pronunciamiento de reembolso de las costas.

Por ser de Justicia que pido en [LUGAR], a [FECHA].

Firma de Abogado/a	Firma de Procurador/a
