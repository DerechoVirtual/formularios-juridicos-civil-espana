---
name: demanda-juicio-ordinario-reclamar-honorarios-civ-0853
description: "Demanda de juicio ordinario para reclamar honorarios de asesoramiento jurídico por iguala. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio ordinario para reclamar honorarios de asesoramiento jurídico por iguala

> Formulario **CIV-0853** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio ordinario sobre reclamación de cantidad por los servicios de asesoramiento jurídico prestados en régimen de iguala.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio ordinario para reclamar honorarios de asesoramiento jurídico por iguala» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio ordinario para reclamar honorarios de asesoramiento jurídico por iguala” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:demanda-juicio-ordinario-reclamar-honorarios-civ-0853`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (12 veces)
- [ ] Nº DE DOCUMENTO (11 veces)
- [ ] DENOMINACIÓN SOCIAL (10 veces)
- [ ] FECHA (9 veces)
- [ ] IMPORTE EN CIFRA (9 veces)
- [ ] AÑO (7 veces)
- [ ] IMPORTE (6 veces)
- [ ] NÚMERO (6 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] MES (4 veces)
- [ ] SEDE (3 veces)
- [ ] COLEGIO (2 veces)
- [ ] NOMBRE DEL REPRESENTADO/A (2 veces)
- [ ] Nº (2 veces)
- [ ] CALLE
- [ ] DNI/NIE
- [ ] DOMICILIO
- [ ] EJERCICIO
- [ ] FECHAS
- [ ] LUGAR
- [ ] MESES IMPAGADOS
- [ ] MOTIVO
- [ ] Nº DE PROCEDIMIENTO
- [ ] PARTE DEMANDADA
- [ ] PLAZO
- [ ] PROVINCIA

## Normas que cita el formulario

- art. 399.1 LEC
- art. 9.2 LOPJ
- art. 36 LEC
- art. 45 LEC
- art. 85.1 LOPJ
- art. 51.1 LEC
- art. 6 LEC
- art. 10.1 LEC
- art. 5.1 LEC
- art. 31.1 LEC
- art. 23.1 LEC
- art. 249.2 LEC
- art. 5 Ley Orgánica 1/2025
- art. 1.089 Código Civil
- art. 1.100 Código Civil
- art. 394.1 LEC

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] Y SU PARTIDO Q.P.T.R.C.»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: Un solo TI por partido judicial (art. 84.1 LOPJ): sobra «de los de». Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).
- Junto a «… por la Sección de lo Social del Tribunal de Instancia de [SEDE], plaza n.º [Nº]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. «De los de» es residuo de los varios juzgados de una plaza. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] Y SU PARTIDO Q.P.T.R.C.

[NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, que actúa en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS], ambos mayores de edad, abogados, provistos de D.N.I. nos [DNI/NIE], con despacho abierto en [LOCALIDAD], como acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], ante el Tribunal comparecen y como mejor en derecho proceda, DICEN:

Que por medio del presente escrito deducen DEMANDA DE JUICIO ORDINARIO, en reclamación de cantidad contra la mercantil [DENOMINACIÓN SOCIAL], domiciliada en [DOMICILIO].

Que esta parte asume el compromiso de recibir cualquier comunicación dirigida por la oficina judicial, durante toda la fase declarativa, e, incluso, en una eventual fase de ejecución por medios telemáticos, en términos del art. 399.1 II LEC, consignándose a estos efectos la siguiente dirección de correo electrónico y nº [Nº] de teléfono:

Demanda que se basa en los siguientes hechos y fundamentos de derecho:

HECHOS

PRIMERO.- Que los que suscriben son Letradas en ejercicio del Iltre. Colegio de Abogados de [COLEGIO], habiéndose dedicado ininterrumpidamente a la abogacía, bajo diferentes circunstancias, desde el año [AÑO], la primera y [AÑO] la segunda, y contando desde el [FECHA], con despacho de libre ejercicio, que en la actualidad se encuentra en la calle [CALLE] de [LOCALIDAD] (Documentos nos. y [Nº DE DOCUMENTO]); estando constituidas a efectos colegiales en despacho colectivo (Doc. nº [NÚMERO]) y a efectos fiscales en sociedad civil (denominada [DENOMINACIÓN SOCIAL]), con C.I.F. nº [NÚMERO] (Doc. nº [NÚMERO]).

La actividad principal de su ejercicio, sin descartar un sector porcentualmente menor de dirección técnica en litigios, consiste en el asesoramiento, intermediación, representación y gestión de negocios ajenos, bien sea a empresas en régimen de iguala o a particulares en régimen de honorarios según minuta.

SEGUNDO.- El entonces director de asuntos sociales de la empresa [DENOMINACIÓN SOCIAL], D./Dña. [NOMBRE Y APELLIDOS], después de haber encargado diversos asuntos judiciales de su firma al despacho colectivo que integran mis patrocinadas a lo largo de [PLAZO], minutados en su día, planteó, a principios del año [AÑO], los problemas habituales de conflictividad laboral que conocía su empresa, y la conveniencia de una asistencia letrada permanente, decidiendo proponer la contratación de los servicios de asesoría jurídica de índole laboral y de seguridad social que ofertábamos, mediante el sistema de iguala mensual.

El [FECHA] se había otorgado a las demandantes poder general y especial para pleitos ante el Notario de Vitoria D./Dña. [NOMBRE Y APELLIDOS], nº [NÚMERO] de su protocolo general corriente, cuya reproducción se acompaña como documento nº [Nº DE DOCUMENTO].

El contrato luego celebrado de prestación de servicios profesionales con carácter indefinido, comprendía tanto el asesoramiento como la defensa y asistencia ante cualquier organismo o jurisdicción, incluso las reclamaciones extrajudiciales, y la fórmula remuneratoria periódica era fija y mensual, iniciándose según los libros de los demandantes, en [MES] de [AÑO] con la cifra de [IMPORTE] euros ([IMPORTE EN CIFRA] €) mensuales, a salvo suplido de desplazamiento y gastos, siendo el medio de pago cheque nominativo previo recibo girado a la empresa.

A su ilustración, se aportan dos juegos de minutas, y misivas en respuesta con el pago, correspondientes al primer dicho año [AÑO], haciendo documento nº [Nº DE DOCUMENTO].

TERCERO.- Durante casi tres años, como asesores de la empresa [DENOMINACIÓN SOCIAL], las dos abogadas demandantes han desenvuelto una actividad dentro de su competencia y función profesional, judicial y extrajudicial, aconsejando y siguiendo instrucciones a un tiempo, de D./Dña. [NOMBRE Y APELLIDOS], primero, y de D./Dña. [NOMBRE Y APELLIDOS], después, sucesivos directores de asuntos sociales de la firma, en numerosos temas de cierta importancia, cuya enumeración convertiría en interminable este cuerpo de demanda, y que además sería inmaterial para su objeto.

En cualquier caso, no tiene noticia el despacho que demanda de insatisfacción de parte de los antedichos directores por los servicios prestados, sino muy al contrario, lo cual también pudiendo resultar insustancial en esta ‘litis’, en definitiva corresponde quedar dicho.

CUARTO.- La iguala de [DENOMINACIÓN SOCIAL], se ha ido incrementado, según se pactó, en adaptación a la depreciación del signo monetario, y se elevaba para el ejercicio [EJERCICIO] a la cifra de [IMPORTE] euros ([IMPORTE EN CIFRA] €) (Documento nº [Nº DE DOCUMENTO]) que se giraba mediante recibo, con el correspondiente cargo del I.V.A. y eventuales gastos de desplazamiento.

En el mes de [MES] de [AÑO], se incrementó de forma extraordinaria a la cifra de [IMPORTE] euros ([IMPORTE EN CIFRA] €) mensuales, dado que [DENOMINACIÓN SOCIAL], decidió atribuir a los letrados demandantes la asesoría además de su filial sita en [LOCALIDAD] (provincia de [PROVINCIA]) denominada [DENOMINACIÓN SOCIAL], otorgándose otro poder general y especial para pleitos ante el Notario de Vitoria D./Dña. [NOMBRE Y APELLIDOS], el [FECHA], nº [NÚMERO] de su protocolo (Documento nº [Nº DE DOCUMENTO]). Se adjunta juego de facturas y carta con el cheque, como documento nº [Nº DE DOCUMENTO].

Para el año, se tenía acordado un incremento del%, siendo por consiguiente la iguala mensual deeuros (€ [IMPORTE EN CIFRA]).

Esta iguala, según lo dicho, se ha venido cobrando desde, ininterrumpidamente hasta la mensualidad de [MES], ambas inclusive, si bien nunca con una puntualidad excesiva, atribuida a problemas de tesorería.

Los recibos desde el mes dehan sido impagados, sin embargo de continuar desenvolviendo las actividades de asesoramiento y asistencia habituales a la empresa mis mandantes con toda normalidad.

QUINTO.- Tras múltiples llamadas telefónicas, se consiguió al fin averiguar que desde [FECHA], había nuevamente cambiado la directiva de la empresa, sin que tenga constancia esta parte si ha existido modificación de propietarios o de órganos de administración social, y por el jefe de personal se manifiesta la voluntad de resolver la relación de servicios por [MOTIVO],(el propio jefe de personal iba a ser despedido) con las abogadas actoras, entre otras consideraciones que no son del caso, y con el agradecimiento por las gestiones hasta entonces realizadas.

El [FECHA], D./Dña. [NOMBRE Y APELLIDOS] comparece en representación de [NOMBRE DEL REPRESENTADO/A], en un juicio de sanción laboral, instado por D./Dña. [NOMBRE Y APELLIDOS], Autos nº [Nº DE PROCEDIMIENTO] / seguidos por la Sección de lo Social del Tribunal de Instancia de [SEDE], plaza n.º [Nº] , en el que consiguió una conciliación, que se puede decir es la última actuación pública en cumplimiento del contrato de servicios de asesoría. Se demuestra mediante copia testimoniada del acta de conciliación, como documento nº [Nº DE DOCUMENTO].

SEXTO.- Comoquiera que la expresa decisión de [DENOMINACIÓN SOCIAL], se comunica, aún poco formalmente, a finales de enero, y hasta el día 28 del dicho mes y año se requieren los servicios, la resolución unilateral del contrato entre partes debe admitirse que la deuda pendiente con los demandantes alcanza hasta el pago de dicho mes.

Quedan pendientes, pues, los cinco recibos antedichos de [MESES IMPAGADOS] de cuyo importe total, que adiciona, además del principal y el I.V.A., un suplido de desplazamiento, ascendiendo aeuros (€ [IMPORTE EN CIFRA]). Se adjuntan como documentos nos.las facturas de minutas impagadas.

SÉPTIMO.- Que la deuda reseñada, nunca negada por la demandada, según se desprende de la falta de objeciones a los repetidos ‘faxes’ enviados a la empresa con cálculo del débito, no se ha visto liquidada en porción alguna, a pesar de los ofrecimientos de no exigir el pago total inmediato, ante una eventual carencia de liquidez.

Mis mandantes intentaron infructuosamente el contacto con el presunto nuevo abogado de la firma, V. A., colegiado de [LOCALIDAD] (‘fax’ documento nº [Nº DE DOCUMENTO]), y enviaron el día [FECHA] carta admonitoria, de la que se acusó recibo (Doc. nº [NÚMERO]), desatendida hasta la fecha, en la que se advertía de la lamentable formulación de la demanda judicial que ahora se produce.

OCTAVO.- La parte actora manifiesta que, previo a la presentación de la presente demanda, se han llevado a cabo negociaciones con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad, y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria; incluyéndose entre las acciones realizadas el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución.

Finalmente, mi representado envió un requerimiento fehaciente al demandado con fecha [FECHA], fijando un plazo de 30 días naturales para llegar a un acuerdo amistoso, a través del abogado que firma este escrito, el cual fue contestado por el demandado por el mismo medio, rechazando el acuerdo/ habiendo sido solo posible un acuerdo parcial, viéndonos en la necesidad de acudir a la presente vía judicial, respecto a los extremos de la controversia en los que se mantiene la discrepancia.

Acompaño como documento nº [Nº DE DOCUMENTO], el requerimiento efectuado y como documento nº [Nº DE DOCUMENTO], la contestación del demandado.

FUNDAMENTOS DE DERECHO

I.- COMPETENCIA.

Corresponde a la jurisdicción civil sin duda alguna el conocimiento de la cuestión que constituye el objeto del proceso (art. 9.2 LOPJ), sin elemento de extranjería (art. 36 LEC), y sin que se haya sometido a arbitraje.

En cuanto a la competencia objetiva corresponde al Tribunal de Instancia al que nos dirigimos conforme a lo establecido en el art. 45 LEC, en relación con lo dispuesto en el art. 85.1º LOPJ.

Es competente territorialmente el Tribunal al que tengo el honor de dirigirme en aplicación de la regla de competencia del art. 51.1 LEC, puesto que ejercitándose una acción personal sin especialidad en cuanto a fuero necesario, la ciudad de [LOCALIDAD] es al mismo tiempo domicilio social de [DENOMINACIÓN SOCIAL], y lugar del lugar de la relación jurídica, dado que la inmensa mayoría de la actividad judicial y extrajudicial en asesoría de la demandada se ha desenvuelto en ella.

II.- PRESUPUESTOS SUBJETIVOS DE LAS PARTES.

Las demandantes gozan de la plena capacidad, tanto para ser parte como capacidad procesal, que se deriva de su mayoría de edad y de estar en el pleno ejercicio de sus derechos civiles, artículos 6 y 7 de la LEC.

Tienen legitimación activa mis representados por ser titulares del crédito derivado de la relación de arrendamiento de servicios concertada, habiendo cumplido su prestación y no habiendo recibido el pago del precio, es decir, titulares del objeto de ‘litis’ (art. 10.1 LEC), y está legitimada pasivamente la demandada por ser la deudora de dicho pago, frente a la que se pide la tutela judicial (art. 5.1 LEC).

En cuanto a la postulación es preceptiva en el presente proceso la intervención de Abogado habilitado para ejercer su profesión en el tribunal que conozca del asunto, como lo son las mismas demandantes (art. 31.1 LEC), y también de Procurador/a igualmente habilitado para actuar en el tribunal que conozca del juicio (art. 23.1 de la LEC), acompañándose a esta demanda el apoderamiento electrónico del mismo.

III.- CUANTÍA Y PROCEDIMIENTO.

El presente proceso habrá de tramitarse por las normas del Juicio Ordinario, de acuerdo con lo que establece el artículo 249.2 LEC, fijándose su cuantía, tal y como exige el artículo 253.1, en la cantidad de [IMPORTE] euros ([IMPORTE EN CIFRA] €), que es la reclamada, sumada a los intereses moratorios liquidables, mediante simple operación aritmética, los que se devengaron desde [FECHA] hasta la presentación de esta demanda, al tipo legal del dinero (arts. 251.1ª y 252.2ª LEC).

IV.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

V.- FONDO DEL ASUNTO.

Según declara el art. 1.089 del Código Civil, que abre el Libro de obligaciones y contratos, ‘las obligaciones nacen de los contratos ‘ y añade el 1.091 ‘las obligaciones que nacen de los contratos tienen fuerza de ley entre las partes contratantes y deben cumplirse al tenor de los mismos’.

El Título II del dicho libro del Código comienza con el art. 1.254, que nos define el contrato: ‘ existe desde que una o varias personas consienten en obligarse, respecto de otra u otras, a dar alguna cosa o prestar algún servicio’.

En el art. 1.544, junto al contrato de ejecución de obra, se describe el contrato de arrendamiento de servicios: ‘En el arrendamiento de servicios, una de las partes se obliga a prestar a la otra un servicio por precio cierto’. Se trata pues, y a pesar del pobrísimo desarrollo de Derecho Positivo, de un contrato consensual, que se perfecciona por el mero consentimiento, bilateral por ser productor de obligaciones recíprocas, a título oneroso, conmutativo y sin requisito formalista alguno. Es de íntegra aplicación la norma del art. 1.278: ‘Los contratos serán obligatorios, cualquiera que sea la forma en que se hayan celebrado, siempre que en ellos concurran las condiciones esenciales para su validez’.

En el caso de Autos, desde que la representación de [NOMBRE DEL REPRESENTADO/A], confía en unas abogadas ejercientes la gestión de sus intereses, v. gr.: para asistencia en vistas de la Sección de lo Social del Tribunal de Instancia de [SEDE], representación de la empresa ante la administración pública, el percibo de cantidades del FOGASA en nombre de trabajadores, consejos sobre la negociación de convenio colectivo particular de empresa, y un larguísimo etc, a través del sistema de iguala mensual, contrata un riguroso arrendamiento de servicios profesionales en régimen de pago fijo periódico de honorarios.

El contrato, necesariamente oneroso (la presunción de remunerabilidad ha sido reiterada por la jurisprudencia desde antiguo ‘ex analogia’ art. 1.711 sobre el mandato), con un precio cierto, que empezó siendo de [IMPORTE] euros ([IMPORTE EN CIFRA] €), y se ha ido incrementando, modificando o actualizando hasta las [IMPORTE] euros ([IMPORTE EN CIFRA] €), según lo destacado en los hechos.

Cuando un Colegio profesional a que pertenece el prestatario del servicio tiene aprobadas unas normas de honorarios, incluso el silencio de las partes sobre el precio -que en nuestro supuesto no se da- estaría suficientemente suplido (Sentencia de la Sala 1ª del Tribunal Supremo de 7 de junio de 1.958). El sistema de asesoramiento jurídico de empresa en régimen de iguala, que se fundamenta en la libertad de pacto dentro del marco civil y mercantil, está explícitamente contemplado en las normas 38 y 39 de las orientativas del Iltre. Colegio de Abogados de [COLEGIO], y es uno de los sistemas retributivos del art. 26 del Estatuto General de la Abogacía aprobado por RD 135/2021 de 2 de marzo.

Así como en el arrendamiento de obra se persigue un resultado útil por precio alzado, en el de servicios se pretende el desenvolvimiento de una determinada actividad. En el caso de litigio no hay duda alguna de que se trata de lo segundo porque el resultado apetecible no está en la mano del que realiza el trabajo.

En definitiva, los demandantes cumplieron su obligación de ‘facere’, hasta el mismo final del mes [MES] de [AÑO] (art. 1.088 del Código), con toda la pericia de su profesión, por encima de la diligencia del buen padre de familia (art. 1.104), y excluyendo el mínimo atisbo de culpa del el aforismo clásico (‘peritia artis culpae enumerantur’).

Por el contrario, la demandada incumple su obligación principal, que es la de pagar la contraprestación, la de abonar cinco de las mensualidades acordadas hasta la definitiva resolución del contrato por voluntad unilateral de [DENOMINACIÓN SOCIAL], cosa que nunca se discute puede legítimamente hacer y así ha hecho.

VI.- INTERESES MORATORIOS.

De acuerdo con el art. 1.100 del Código Civil ‘Incurren en mora los obligados a entregar o hacer alguna cosa desde que el acreedor les exija extrajudicialmente el cumplimiento de su obligación ‘, y conforme al 1.108: ‘Si la obligación consistiere en el pago de una cantidad de dinero, y el deudor incurriere en mora, la indemnización de daños y perjuicios, consistirá a falta de convenio, en el interés legal’.

Por consiguiente, desde el, en que consta que la demandada recibe el último inexcusable requerimiento a través de correo del pago de honorarios de cinco meses, debe asimismo, como resarcimiento de perjuicios el interés legal del dinero hasta la fecha de definitivo pago.

VII.- COSTAS.

Deberán ser impuestas a la demandada en virtud del art. 394.1 LEC.

En virtud de lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito con sus copias y documentos que se acompañan, se sirva admitir uno y otras, y en la representación que ostento, se me tenga por personada y parte, entendiéndose conmigo los sucesivos trámites, y por formulada DEMANDA DE JUICIO ORDINARIO contra [PARTE DEMANDADA], se sirva dar traslado de la presente a la citada demandada, para que si a su derecho conviniera la conteste en tiempo y forma legales, y seguido que sea el pleito por sus demás trámites procesales, en su día se venga a dictar Sentencia por la que, estimando íntegramente la presente demanda CONDENE a la mercantil demandada:

1.- Al pago a las demandantes D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS] de la cantidad deeuros (€ [IMPORTE EN CIFRA]) en concepto de principal.
2.- Al pago adicional de lo que representen los intereses calculados al tipo legal del dinero desde elhasta el dictado de la sentencia, cuando comenzará el devengo de los procesales.
3.- Al pago de todas las costas de este juicio.

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a

========================================================================
