---
name: demanda-desahucio-local-impago-ofrecimiento-civ-0582
description: "Demanda de desahucio de local por impago, con ofrecimiento de transacción sobre las rentas. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de desahucio de local por impago, con ofrecimiento de transacción sobre las rentas

> Formulario **CIV-0582** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio verbal de desahucio por falta de pago de la renta del arrendamiento de un local (inmueble con destino diferente al de vivienda) así como de las cuotas de contribución de la comunidad de propiedad horizontal con ofrecimiento a la inquilina de condonación de la mitad de las cantidades debidas si ésta desaloja voluntariamente el inmueble dentro del mes después de que se le notifique la presente demanda. La misma se interpone por el usufructuario vitalicio del local.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de desahucio de local por impago, con ofrecimiento de transacción sobre las rentas» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de desahucio de local por impago, con ofrecimiento de transacción sobre las rentas” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:demanda-desahucio-local-impago-ofrecimiento-civ-0582`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] IMPORTE (6 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] FECHA (4 veces)
- [ ] Nº DE DOCUMENTO (4 veces)
- [ ] NÚMERO (3 veces)
- [ ] DOMICILIO (2 veces)
- [ ] CALLE
- [ ] CORREO ELECTRÓNICO
- [ ] FECHAS
- [ ] LUGAR
- [ ] MESES IMPAGADOS
- [ ] Nº
- [ ] Nº DE COLEGIADO/A
- [ ] SEDE
- [ ] TELÉFONO

## Normas que cita el formulario

- art. 24.1 LEC
- art. 437.1 LEC
- art. 438.5 LEC
- art. 250.1.1.º LEC
- art. 251 LEC
- art. 5 Ley Orgánica 1/2025
- art. 35 LAU
- art. 27.2.a LAU
- art. 21 LEC
- art. 549 LEC

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

Que mediante el presente escrito vengo a formular DEMANDA DE JUICIO VERBAL DE DESAHUCIO POR FALTA DE PAGO CON OFERTA DE COMPROMISO CON EFECTO DE TRANSACCIÓN DE CANTIDADES DEBIDAS, contra D./Dña. [NOMBRE Y APELLIDOS], con domicilio, primero en [DOMICILIO]; y segundo, el domicilio laboral en [DOMICILIO]); con email [CORREO ELECTRÓNICO]; y con número de teléfono móvil [TELÉFONO].

Que esta parte asume el compromiso de recibir cualquier comunicación dirigida por la oficina judicial, durante toda la fase declarativa, e, incluso, en una eventual fase de ejecución por medios telemáticos, en términos del art. 399.1 II en relación al art. 437.1, ambos LEC, consignándose a estos efectos la siguiente dirección de correo electrónico y nº [Nº] de teléfono:

Todo ello de conformidad con los siguientes hechos y fundamentos de derecho:

HECHOS

PRIMERO.- Mi mandante es dueño del local sito en esta ciudad, calle [CALLE], n.º [NÚMERO], que se ha fijado como lugar de comunicación procesal con la demandada, y que se dedica a negocio de Bar-Degustación.

Se acompaña el título consistente en nota del Registro de la Propiedad de [LOCALIDAD], como documento n.º [NÚMERO].

SEGUNDO.- La demandada D./Dña. [NOMBRE Y APELLIDOS]. ocupa dicha inmueble con destino diferente al de vivienda en concepto de arrendataria en virtud de contrato de arrendamiento celebrado en fecha [FECHA], en la que se pactó una renta mensual que asciende a la cifra de [IMPORTE] euros, siendo a cargo del arrendatario las cuotas de contribución de la comunidad de propiedad horizontal, y habiéndose un interés por mora en el pago a partir del quinto día anticipado de cada mes del 10% anual. Se adjunta dicho contrato como documento n.º [NÚMERO].

TERCERO.- La demandada ha dejado de pagar las rentas correspondientes a los meses [MESES IMPAGADOS], a razón de [IMPORTE] euros mensuales, así como las cuotas mensuales de la comunidad de propietarios por gastos generales que ascienden a la cantidad de [IMPORTE] euros (se adjuntan copia del acta de la Junta de Propietarios de fecha [FECHA], así como el recibo devuelto por la entidad bancaria, como documentos números [Nº DE DOCUMENTO] y [Nº DE DOCUMENTO]), a lo que debe adicionarse el cálculo del interés moratorio, y todo ello hace un total de [IMPORTE] euros.

CUARTO.- Mi mandante está dispuesto, dada la insuficiencia de recursos que manifiesta la demandada, y el interés en poner el local en el mercado para otro tipo de negocio, a asumir el compromiso de condonada D./Dña. [NOMBRE Y APELLIDOS] la mitad de la predicha deuda pendiente, lo cual hacen [IMPORTE] euros, así como las costas de este juicio, siempre a condición de que la arrendataria desaloje voluntariamente el inmueble dentro de los quince días después de que se le notifique la presente demanda.

QUINTO.- La parte actora manifiesta que, previo a la presentación de la presente demanda, se han llevado a cabo negociaciones con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad, y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria; incluyéndose entre las acciones realizadas el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución.

Finalmente, mi representado envío un requerimiento fehaciente al demandado con fecha [FECHA], fijando un plazo de 30 días naturales para llegar a un acuerdo amistoso, a través del abogado que firma este escrito, el cual fue contestado por el demandado por el mismo medio, rechazando el acuerdo/ habiendo sido solo posible un acuerdo parcial, viéndonos en la necesidad de acudir a la presente vía judicial, respecto a los extremos de la controversia en los que se mantiene la discrepancia.

Acompaño como documento nº [Nº DE DOCUMENTO], el requerimiento efectuado y como documento nº [Nº DE DOCUMENTO], la contestación del demandado.

FUNDAMENTOS DE DERECHO

I

Art. 52.1.7.º LEC, sobre competencia territorial del Tribunal de Instancia a que me dirijo, por ser del lugar en que está sita la finca objeto de la acción de desahucio.

II

Art. 250.1.1.º LEC, sobre la sustanciación de la pretensión recuperatoria de la posesión de la finca dada en arrendamiento, a través del cauce del juicio verbal, observándose las disposiciones contenidas en el art. 438.5 y 6 LEC para el juicio de desahucio.

III

Art. 10 párrafo 1.º, en relación con el art. 250.1.1.º LEC, en armonía con lo cual está legitimado activamente mi representado en cuanto que propietario del local dado en arrendamiento y titular del crédito por el precio del arriendo y por las cantidades cuyo pago tiene asumido contractualmente la arrendataria, y lo está pasivamente la demandada, en cuanto que poseedora de dicho local por contrato de arrendamiento, y deudora de las rentas y demás cantidades de pago debido, según lo pactado.

Tratándose de un juicio verbal por razón de la materia y no por razón de la cuantía, conforme a los arts. 23.1 y 31.1 LEC, es preceptiva la intervención de procurador de los tribunales y de abogado en ejercicio, ambos habilitados ante el Tribunal, estando identificados representante y director letrado en el encabezamiento de la demanda.

IV

Regla 9.ª del art. 251 LEC en lo tocante a la cuantía de la demanda por la acción de recuperación del inmueble, determinándola en lo que suma la anualidad de renta del contrato.

V

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

VI

Art. 1.555.1.º CCiv, conforme al que el arrendatario está obligado a pagar el precio del arrendamiento en los términos convenidos; art. 1.124 párrafo 2.º CCiv que previene la acción de cumplimiento de la obligación contractual para la parte que hubiere cumplido su obligación.

Arts. 1.100.1.º y 1.108 CCiv, a propósito del interés moratorio, por declararlo el contrato y establecer su cuantificación.

VII

Art. 1.556 CCiv, que contempla la acción resolutoria por incumplimiento, y art. 35 LAU 1994 en relación con el art. 27.2.a) LAU 1994 según el que el arrendador podrá resolver de pleno derecho el contrato por causa de la falta de pago de la renta o de cualquiera de las cantidades cuyo pago haya asumido o corresponda al arrendatario.

VIII

Art. 22.4 párrafo 2.º LEC, a tenor del cual es de aplicación la enervación de la acción de desahucio, por cuanto el arrendatario no ha enervado el desahucio en una ocasión anterior, ni ha sido requerido de pago fehacientemente

IX

Art. 437.3 LEC, el cual autoriza desde la reforma auspiciada por la Ley 19/2009, de 23 de noviembre, de medidas de fomento y agilización procesal del alquiler y de la eficiencia energética de los edificios, que en las demandas de desahucio de finca urbana por falta de pago de rentas o cantidades adeudadas asimiladas, a que el actor asuma el compromiso de condonar todo o parte de las deuda y las costas, fijando cantidad concreta, condicionándolo a que el arrendatario desaloje dentro del plazo que también concrete, que no sea inferior a quince días desde la notificación de la demanda.

Art. 438.5 LEC, conforme al que si el demandante ha expresado en su demanda que asume el compromiso a que se refiere el apartado 3 del art. 437, se pondrá de manifiesto al demandado en el requerimiento previo a la eventual vista que se señale, y la aceptación de este compromiso equivaldrá a un allanamiento con los efectos del art. 21 LEC.

El propio precepto en su apartado 4 indica que en la resolución que se dicte teniendo por opuesto al demandado debe anticiparse la fecha del lanzamiento para el caso de que se haya de dictar sentencia, y sea estimatoria, no recurriendo la condena el demandado, y a expensas de la solicitud ejecutiva del art. 549 LEC.

Art. 447.1 párrafo 2.º LEC, según el que si no cumpliere el demandado allanado, se llevará a término el lanzamiento dentro de los quince días siguientes, sin trámite previo alguno, puesto que en previsión de que no se verifique por el arrendatario el desalojo voluntario en el plazo señalado, se habrá de fijar con carácter subsidiario día y hora en que tendrá lugar, en su caso, el lanzamiento directo del demandado, que se llevará a término sin necesidad de ulteriores trámites en un plazo no superior en los quince días desde la finalización del periodo voluntario de desalojo.

X

Art. 394.1 LEC, que instaura un principio cuasiobjetivo de abono de las costas procesales por vencimiento, siendo que el asunto deducido no encierra dudas de hecho ni de Derecho.

En virtud de lo expuesto,

SUPLICO AL TRIBUNAL,

que teniendo por presentado este escrito con los documentos que lo acompañan y copia de todo ello, se tenga a bien admitirlos, y por interpuesta demanda de desahucio de local urbano por falta de pago de la rentas y cantidades vencidas y no pagadas:

1.º Que se requiera por el Letrado de la Administración de Justicia al demandado para que en el plazo de diez días desaloje el inmueble, con posibilidad de enervación, que ejercitada, deberá comunicarse a esta parte actora, y advirtiendo en el requerimiento a D./Dña. [NOMBRE Y APELLIDOS] de que se ofrece el compromiso de condonar la mitad de la deuda en cantidad de [IMPORTE], a condición de que desaloje voluntariamente en el plazo de quince días desde la notificación de esta demanda, de modo que si acepta el compromiso, se dicte resolución que homologue la transacción; y para el caso de que en dicho plazo no atienda el requerimiento ni comparezca ante éste formulando oposición, se dicte decreto dando por terminado el juicio de desahucio y se proceda al lanzamiento en la fecha fijada por el Tribunal.
2.º Que se cite a las partes para la celebración de eventual vista si el demandado comparece y se opone, pidiendo desde este momento, para el caso de oposición, se dicte sentencia por la que, estimando la demanda, se decrete el desahucio de la demandada respecto del local que viene ocupando, sito en [LOCALIDAD], con expresa imposición de las costas del juicio en tal caso.

Por ser de Justicia que pido en [LUGAR], a [FECHA].

Firma de Abogado/a	Firma de Procurador/a
