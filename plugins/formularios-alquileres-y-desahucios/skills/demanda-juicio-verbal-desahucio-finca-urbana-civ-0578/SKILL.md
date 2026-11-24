---
name: demanda-juicio-verbal-desahucio-finca-urbana-civ-0578
description: "Demanda de juicio verbal de desahucio de finca urbana por vencimiento del plazo del contrato. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio verbal de desahucio de finca urbana por vencimiento del plazo del contrato

> Formulario **CIV-0578** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio verbal de desahucio en ejercicio de acción recuperatoria por expiración del término convenido, con solicitud inicial de fijación del lanzamiento.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio verbal de desahucio de finca urbana por vencimiento del plazo del contrato» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio verbal de desahucio de finca urbana por vencimiento del plazo del contrato” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:demanda-juicio-verbal-desahucio-finca-urbana-civ-0578`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (9 veces)
- [ ] FECHA (6 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] NÚMERO (5 veces)
- [ ] CALLE (4 veces)
- [ ] Nº DE DOCUMENTO (4 veces)
- [ ] IMPORTE (2 veces)
- [ ] Nº (2 veces)
- [ ] SEDE (2 veces)
- [ ] DOMICILIO
- [ ] FECHAS
- [ ] LUGAR
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] PARTE DEMANDADA
- [ ] PISO

## Normas que cita el formulario

- art. 439.6 LEC
- art. 9.2 LOPJ
- art. 36 LEC
- art. 39 LEC
- art. 45 LEC
- art. 85.1 LOPJ
- art. 52.1.7.º LEC
- art. 250.1.1.º LEC
- art. 251 LEC
- art. 3.k Ley 12/2023
- art. 5 Ley Orgánica 1/2025
- art. 9 LAU
- art. 10 LAU
- art. 437.3 LEC
- art. 549.3 LEC
- art. 549.4 LEC
- art. 394.1 LEC
- art. 399.1 LEC

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] Q.P.T.R.C.»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «… de desahucio del que conoció el Tribunal de Instancia de [SEDE], plaza n.º [Nº]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. «De los de» es residuo de los varios juzgados de una plaza. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] Q.P.T.R.C.

D./Dña. [NOMBRE Y APELLIDOS],Procurador de los Tribunales, que actúa en nombre y representación de [NOMBRE DEL REPRESENTADO/A], Organismo Autónomo Local, domiciliado en [DOMICILIO], calle [CALLE], cuyas circunstancias obran en la escritura de poder inscrito en el Registro Electrónico de Apoderamientos Judiciales, a cuya justificación aporto certificación de dicho Registro como documento nº [Nº DE DOCUMENTO]; y dirigida por el Letrado D./Dña. [NOMBRE Y APELLIDOS], con despacho abierto en [LOCALIDAD], ante el Tribunal comparezco y como mejor en derecho proceda, DIGO:

Que por medio del presente escrito deduzco DEMANDA DE JUICIO VERBAL, en reclamación de recuperación de finca urbana por expiración del término contractual, contra D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con D.N.I. n.º [NÚMERO], cuyos demás datos personales ignora esta parte, y con domicilio en [LOCALIDAD], calle [CALLE], con base en los siguientes:

HECHOS

PRIMERO.- La entidad actora es arrendadora de la vivienda sita en el piso [PISO] de la casa señalada con el n.º [NÚMERO] de la calle [CALLE] de [LOCALIDAD], y el demandado resulta ser el arrendatario, en virtud de contrato de arrendamiento suscrito por ambos el [FECHA].

Se acompaña el contrato privado como documento n.º [NÚMERO].

SEGUNDO.- El indicado arrendamiento tenía prevista una duración de un año, si bien, vencido dicho plazo, de no mediar notificación por la arrendadora que denunciara la finalización del contrato con tres meses de antelación al término, se previó la tácita reconducción por periodos idénticos a la periodicidad del pago de renta, es decir, por meses, y hasta el definitivo requerimiento de extinción del contrato sucesivamente novado (así, cláusula 5.ª del contrato aportado).

TERCERO.- El [FECHA] mi mandante requirió mediante telegrama con acuse de recibo al demandado para el desalojo de la vivienda arrendada, haciendo éste caso omiso, por lo que se instó juicio de desahucio del que conoció el Tribunal de Instancia de [SEDE], plaza n.º [Nº] , el cual dictó sentencia desestimatoria de fecha [FECHA].

Se acompaña como documento n.º [NÚMERO] testimonio de la sentencia, en que constan los hechos.

CUARTO.-Desde el pasadocarece el arrendatario de prerrogativa legal para mantenerse en la posesión del inmueble, por lo que else dirigió a D./Dña. [NOMBRE Y APELLIDOS] comunicación del fin del contrato de arrendamiento y requerimiento de desalojo mediante carta instrumentada por el Notario de [LOCALIDAD], D./Dña. [NOMBRE Y APELLIDOS], constando la diligencia de acuse de recibo.

Se demuestra con copia auténtica del acta notarial, que hace documento n.º [Nº DE DOCUMENTO].

QUINTO.- El caso es que D./Dña. [NOMBRE Y APELLIDOS] persevera en la ocupación de la vivienda arrendada, aduciendo que no sabe si tiene o no derecho, y motivos familiares, por lo que, cumplidos los deberes formales, se halla mi patrocinada en la tesitura de formular esta demanda.

SEXTO.- A los efectos del art. 439.6 LEC se hace constar expresamente los siguientes hechos:

1.- Consta a esta parte que la vivienda sobre la que versa el arrendamiento es, desde que se entregaron las llaves conforme contrato y hasta la fecha, la vivienda habitual de la demandada, su marido y sus dos hijos menores de edad.

2.- Mi cliente sólo tiene en propiedad la vivienda objeto de alquiler, y el 50% de un segundo inmueble en la misma ciudad de [LOCALIDAD], calle [CALLE]. Este inmueble constituye su vivienda habitual junto con su marido y la hija menor de ambos. Se adjunta como documento n.º [NÚMERO] certificación del Registro de la Propiedad en la cual constan estos extremos.

SÉPTIMO.- La parte actora manifiesta que, previo a la presentación de la presente demanda, se han llevaron a cabo negociaciones con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad, y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria; incluyéndose entre las acciones realizadas el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución.

Finalmente, mi representado envío un requerimiento fehaciente al demandado con fecha [FECHA], fijando un plazo de 30 días naturales para llegar a un acuerdo amistoso, a través del abogado que firma este escrito, el cual fue contestado por el demandado por el mismo medio, rechazando el acuerdo/ habiendo sido solo posible un acuerdo parcial, viéndonos en la necesidad de acudir a la presente vía judicial, respecto a los extremos de la controversia en los que se mantiene la discrepancia.

Acompaño como documento nº [Nº DE DOCUMENTO], el requerimiento efectuado y como documento nº [Nº DE DOCUMENTO], la contestación del demandado.

FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN Y COMPETENCIA.

No hay cuestión acerca de que corresponde a la jurisdicción civil el conocimiento de la cuestión que constituye el objeto del proceso (art. 9.2 LOPJ), sin que exista elemento de extranjería (art. 36 LEC), ni se haya sometido a arbitraje (art. 39 LEC).

En cuanto a la competencia objetiva corresponde al Tribunal de instancia al que nos dirigimos conforme a lo establecido en el art. 45 LEC, en relación con el art. 85.1º LOPJ.

Es asimismo competente el Tribunal desde el punto de vista territorial, al ser de este partido el lugar en que está sita la finca objeto del proceso (art. 52.1.7.º LEC).

II.- PARTES.

La capacidad para ser parte y la capacidad procesal de obrar, vienen definidas para las personas jurídica mercantil, cual la sociedad anónima demandada, de capital y tutela pública, por su constitución y registración, en los arts. 6.1.3.º y 7.4 LEC, así las reconoce la ley a las personas físicas mayores de edad, sin incapacitación decretada, cual D./Dña. [NOMBRE Y APELLIDOS], en los arts. 6.1.1.º y 7.1 LEC.

Tiene legitimación activa mi representada por cuanto ostenta contractualmente la condición de arrendadora de la finca de autos, y está legitimado pasivamente el demandado por ser el poseedor de la finca como titular arrendatario, todo según los arts. 5.2, 10.pfo. 1.º y 250.1.1.º LEC.

Tratándose de un juicio verbal por razón de la materia y no por razón de la cuantía, conforme a los arts. 23.1 y 31.1 LEC, es preceptiva la intervención de procurador de los tribunales y de abogado en ejercicio, ambos habilitados ante el Tribunal, estando identificados representante y director letrado en el encabezamiento de la demanda.

III.- PROCEDIMIENTO Y CUANTÍA.

Se ejerce pretensión recuperatoria de la posesión de la finca urbana dada en arrendamiento por expiración del plazo fijado contractualmente, lo cual pertenece, en el criterio de preferencia de asignación material a uno de los procesos civiles declarativos comunes, al trámite del juicio verbal, con arreglo a la prevención del art. 250.1.1.º LEC.

La cuantía del litigio se gradúa conforme a la regla 9.ª del art. 251 LEC, puesto que no es de reclamación de cantidad, en el importe de una anualidad de renta, cualquiera que sea la periodicidad con que ésta aparezca fijada en el contrato, la que asciende al monto de [IMPORTE] euros ( [IMPORTE] €).

IV.- DE LAS EXIGENCIAS LEGALES DE LA ACCIÓN DE DESAHUCIO EJERCITADA

Tal y como se ha hecho constar en los hechos de la presente demanda, se cumplen con los requisitos exigidos en el art. 439.6 LEC. En primer lugar, mi mandante tiene constancia de que la vivienda arrendada constituye la vivienda habitual de la parte demandada.

En segundo lugar, la aquí demandante y arrendadora es la propietaria de la vivienda, y ostenta además el 50% de la titularidad de una segunda vivienda que constituye su propia vivienda habitual y la de su familia. En consecuencia, no ostenta la condición de gran tenedora de viviendas, según el art. 3.k) de la Ley 12/2023, de 24 de mayo, por el derecho a la vivienda.

Por lo demás, desde la STC 26/2025, de 29 de enero, no es obligatorio presentar informe de vulnerabilidad ni acreditar mediación previa.

V.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

VI.- FONDO DEL ASUNTO.

El contrato de arrendamiento de vivienda del caso, concertado en [FECHA], no pactó prórroga forzosa a instancias del arrendatario, y sí un plazo de duración de un año, con tácita reconducción mensual expresa.

Así, bajo régimen del TR 1964 y el R. Decreto-Ley 2/1985 de 30 de abril (Decreto Boyer), superado el primer año de posesión por D./Dña. [NOMBRE Y APELLIDOS] de la vivienda arrendada, entró el contrato en tácita reconducción, por meses consecutivos, consentida por la entidad arrendadora (art. 9 R. Decreto-Ley 2/1985, y arts. 1.566 y 1.581 CCiv), situación en que entró en vigor el 1 de enero de 1995 la nueva LAU 1994, y por ello, conforme a la Disposición Transitoria 1.ª, la tácita reconducción primera, en lugar de ser mensual, fue por tres años, como plazo vinculante para el arrendador y facultativo para el arrendatario, éste que pudo manifestar su voluntad de concluir el contrato cada anualidad en la forma y con los requisitos del art. 9 LAU 1994.

Como D./Dña. [NOMBRE Y APELLIDOS] persistió en el goce pacífico de la vivienda después de los tres años posteriores a la entrada en vigor de la LAU 1994, se planteó una duda interpretativa, sobre si el contrato se reconduciría entonces por plazos sucesivos de tres años, lo que no se compadece con una prevención de Derecho transitorio, o si al iniciarse un nuevo contrato bajo régimen de la LAU 1994, y no llevar plazo, se sometería al mínimo legal de tres años, lo cual desequilibraría a las partes de forma incompatible con la finalidad del nuevo sistema legal, o en fin, que el contrato reconducido con la entrada en vigor de la LAU 1994, diferente del inicial, decaídos el plazo y las garantías accesorias, así como las cláusulas contrarias al Derecho necesario de la legislación locativa especial para el arriendo de viviendas, se sujeta al régimen del art. 10 LAU 1994, con lo que se produce una prórroga por plazos anuales, hasta un máximo de tres, salvo que el arrendatario manifieste al arrendador con un mes de antelación a la fecha de terminación de cualquiera de las anualidades su voluntad de no renovar el contrato.

Esta última exégesis es la mayoritaria en la doctrina de apelación (Sentencia de la Audiencia Provincial de Las Palmas, Sección 4ª, 12/2000 de 11 Ene. 2000, Rec. 909/1999, Sentencia de la Audiencia Provincial de Les Illes Balears, Sección 4ª, 368/2000 de 29 May. 2000, Rec. 480/1999, Sentencia de la Audiencia Provincial de Vizcaya, Sección 5ª, 386/2001 de 30 Abr. 2001, Rec. 219/2000), y en ese sentido se falló en el proceso antecedente en que fueron partes las del actual juicio, aún cuando la sentencia fuese desestimatoria, por razón de que, al requerirse de desalojo al arrendatario en marzo de 1999, si había vencido la primera prórroga anual el 9 de enero, había surgido ya un nuevo periodo anual a voluntad del arrendatario, que expiraría el día correlativo de enero de 2000.

Ahora bien, ya el 10 de enero de 2001, agotados los tres plazos de prórroga anual, cada mes para el siguiente, en que opera la tácita reconducción ordinaria del CCiv, al que se remite la DT 1.ª LAU 1994, la arrendadora puede conminar al desalojo al arrendatario, según ha sido caso fehacientemente.

VII.- SEÑALAMIENTO ANTICIPADO DE LANZAMIENTO.

De conformidad con el art. 437.3 "in fine" LEC, esta parte interesa desde esta misma demanda que se tenga por solicitada la ejecución del lanzamiento en la fecha y hora que se fije por el Tribunal a los efectos señalados en el art. 549.3 LEC, esto es, siendo suficiente para que la sentencia condenatoria vaya a la ejecución directa, sin necesidad de ningún otro trámite para proceder al lanzamiento en el día y hora señalados en la propia sentencia, o en la fecha que se hubiera fijado al ordenar la citación al demandado.

Según previene el art. 549.4 LEC, no será de aplicación para dicha ejecución directa el plazo de espera legal de veinte días del art. 548 del propio texto legal.

VIII.- COSTAS.

Deberán ser impuestas al demandado en virtud del principio cuasiobjetivo del vencimiento que rige en la primera instancia de los declarativos, a tenor del art. 394.1 LEC.

En virtud de lo expuesto,

SUPLICO AL TRIBUNAL

que tenga por presentado este escrito con los documentos al mismo acompañados, y copias de todo ello, se admita por el Letrado de la Administración de Justicia, teniéndome por personado y por formulada DEMANDA DE JUICIO DE DESAHUCIO POR EXPIRACIÓN DEL PLAZO CONTRACTUAL contra [PARTE DEMANDADA] y a tenor de lo expuesto, previa observación de los trámites legales, dicte sentencia estimatoria por la que:

1. Resuelva el contrato de arrendamiento.
2. Condene al demandado a desalojar la finca y ponerla a disposición del actor con apercibimiento de lanzamiento.
3. Imponga las costas al demandado.

OTROSÍ PRIMERO DIGO que de conformidad a lo establecido en el art. 437.3 "in fine" LEC en relación al art. 549.3 LEC esta parte interesa desde esta misma demanda que, para el caso de que la sentencia que se dictare fuera estimatoria, se proceda al lanzamiento en el día y hora señalados en la propia sentencia o en la fecha que se hubiera fijado al ordenar la citación al demandado, acordando su ejecución directa.

SUPLICO AL TRIBUNAL que tenga por hecha la anterior manifestación y por interesada la ejecución del lanzamiento en el caso de que la sentencia fuera estimada.

OTROSÍ SEGUNDO DIGO: Que esta parte asume el compromiso de recibir cualquier comunicación dirigida por la oficina judicial, durante toda la fase declarativa, e, incluso, en una eventual fase de ejecución por medios telemáticos, en términos del art. 399.1 II LEC, consignándose a estos efectos la siguiente dirección de correo electrónico y nº [Nº] de teléfono:

Por lo expuesto,

AL TRIBUNAL NUEVAMENTE SUPLICO que, teniendo por hechas las afirmaciones anteriores, se admitan y provea en consecuencia.

Por ser de Justicia que pido en [LUGAR], a [FECHA].

Firma de Abogado/a	Firma de Procurador/a

========================================================================
