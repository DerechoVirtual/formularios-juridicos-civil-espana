---
name: demanda-juicio-ordinario-resolver-contrato-servicios-civ-0695
description: "Demanda de juicio ordinario para resolver un contrato de servicios con préstamo vinculado. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio ordinario para resolver un contrato de servicios con préstamo vinculado

> Formulario **CIV-0695** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio ordinario del consumidor que, tras el cierre o abandono por el prestador de un servicio (p. ej. tratamiento dental) financiado por un tercero, pide la resolución del contrato de servicios y, por vinculación, la del contrato de crédito vinculado (arts. 26 y 29 de la Ley 16/2011 de contratos de crédito al consumo), y la devolución de lo cobrado en exceso.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio ordinario para resolver un contrato de servicios con préstamo vinculado» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio ordinario para resolver un contrato de servicios con préstamo vinculado” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:demanda-juicio-ordinario-resolver-contrato-servicios-civ-0695`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (13 veces)
- [ ] FECHA (7 veces)
- [ ] DENOMINACIÓN SOCIAL DEL PRESTADOR DEL SERVICIO (6 veces)
- [ ] DENOMINACIÓN SOCIAL DE LA ENTIDAD FINANCIERA (5 veces)
- [ ] DOMICILIO (4 veces)
- [ ] IMPORTE (4 veces)
- [ ] FIRMA (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] AÑO
- [ ] CORREO ELECTRÓNICO
- [ ] DENOMINACIÓN SOCIAL DE LA PARTE DEMANDADA CONDENADA
- [ ] DENOMINACIÓN SOCIAL DE LA PARTE QUE LOS PERCIBIÓ
- [ ] DOMICILIO PROFESIONAL
- [ ] DÍA
- [ ] FECHAS
- [ ] MES
- [ ] NOMBRE Y APELLIDOS DEL DEMANDANTE
- [ ] NOMBRE Y APELLIDOS DEL LETRADO/A
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] Nº DE COLEGIADO
- [ ] SEDE
- [ ] TELÉFONO

## Normas que cita el formulario

- art. 399.1 LEC
- art. 85.1 LOPJ
- art. 6.1.3.º LEC
- art. 7.4 LEC
- art. 10 LEC
- art. 253 LEC
- art. 251.8.ª LEC
- art. 249.2 LEC
- art. 23 LEC
- art. 399 LEC
- art. 1.124 CC
- art. 26.2 Ley 16/2011
- art. 29.1 Ley 16/2011
- art. 1.257 CC
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

### Avisos de actualización (2) — se aplican en el texto, nunca se copian en el documento

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «… de [MES] de [AÑO]. Firma del Abogado/a: [FIRMA] Firma del Procurador/a: [FIRMA]»: requisito de procedibilidad (art. 5 LO 1/2025): antes de demandar hay que intentar un medio adecuado de solución de controversias y acreditarlo con la demanda, salvo las materias excluidas del art. 5.2.

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

[NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales y de [NOMBRE Y APELLIDOS DEL DEMANDANTE], con domicilio en [DOMICILIO], según acredito con la escritura de poder inscrita en el Registro Electrónico de Apoderamientos Judiciales, a cuya justificación aporto certificación de dicho Registro que acompaño como documento nº [Nº], y actuando bajo la dirección letrada de [NOMBRE Y APELLIDOS DEL LETRADO/A], colegiado/a n.º [Nº DE COLEGIADO] del Ilustre Colegio de Abogados de [LOCALIDAD], con despacho abierto en [DOMICILIO PROFESIONAL], ante el Tribunal comparezco y, como mejor proceda en derecho, DIGO:

Que en la indicada representación interpongo DEMANDA DE JUICIO ORDINARIO contra la mercantil [DENOMINACIÓN SOCIAL DEL PRESTADOR DEL SERVICIO], con domicilio en [DOMICILIO], y contra la entidad [DENOMINACIÓN SOCIAL DE LA ENTIDAD FINANCIERA], con domicilio en [DOMICILIO],

Que esta parte asume el compromiso de recibir cualquier comunicación dirigida por la oficina judicial, durante toda la fase declarativa e, incluso, en una eventual fase de ejecución, por medios telemáticos, en términos del art. 399.1 II LEC, consignándose a estos efectos la siguiente dirección de correo electrónico y número de teléfono: [CORREO ELECTRÓNICO] / [TELÉFONO].

Todo ello en base a los siguientes hechos y fundamentos de derecho:

HECHOS

PRIMERO.- La entidad demandada, [DENOMINACIÓN SOCIAL DEL PRESTADOR DEL SERVICIO], es una sociedad dedicada a la prestación de servicios de tratamiento dental y, en el ejercicio de tal actividad, en la publicidad emitida por esta entidad se ofrecía financiación para el pago del tratamiento en forma de pago aplazado del precio del mismo en [Nº] meses, sin mayores especificaciones. Se acompaña folleto publicitario como documento número [Nº].

SEGUNDO.- En fecha [FECHA] mi representado/a acudió al establecimiento de dicha demandada, sito en [DOMICILIO], y concertó un contrato de tratamiento dental. Junto con el contrato de prestación de servicios dentales se puso a la firma de mi representado/a un documento para la financiación del tratamiento, todo lo cual fue firmado por aquél/aquélla sin ninguna explicación por parte del centro más que el importe de los plazos a abonar y el número de cuenta donde hacer el ingreso. A mi representado/a solo se le entregó copia del contrato de prestación de los servicios de tratamiento dental, pero nada relativo a la financiación. Aportamos el contrato como documento número [Nº].

TERCERO.- El tratamiento comenzó el día [FECHA] y, transcurridos [Nº] meses, con fecha [FECHA], mi representado/a recibió una carta de la entidad demandada comunicándole que, por problemas de organización de la consulta, debían suspender el tratamiento durante una semana y se le avisaría en el momento de reanudarlo. Se aporta dicha carta como documento número [Nº].

Sin embargo, al cabo de unos días mi representado/a se encontró con el cierre físico y abandono de las instalaciones donde se desarrollaba el tratamiento, sin mediar aviso o noticia alguna.

CUARTO.- Mi representado/a dirigió varias reclamaciones mediante burofax con acuse de recibo al domicilio de la entidad demandada, [DENOMINACIÓN SOCIAL DEL PRESTADOR DEL SERVICIO], advirtiendo de que, en tanto no se reanudara el tratamiento, no se le pasara al cobro plazo alguno del precio del mismo, ninguna de las cuales fue contestada. Se aportan las reclamaciones enviadas como bloque documental número [Nº].

A la vista de este incumplimiento, mi representado/a dio orden a su banco para no atender el pago de los recibos que se le pasaran para pago de las cuotas o plazos pendientes.

QUINTO.- Hace [Nº] días mi representado/a recibió una comunicación por burofax de la entidad financiera codemandada, [DENOMINACIÓN SOCIAL DE LA ENTIDAD FINANCIERA], reclamándole el pago de las cuotas pendientes de abono del tratamiento. Puesto en contacto con esta entidad financiera, se le comunica que fue la citada entidad la que financió el tratamiento y quien adelantó el dinero a la clínica dental y que, por lo tanto, es la acreedora del pago del precio restante. Ante la manifestación de mi representado/a de que no había hablado, pactado ni firmado nada con esa entidad financiera, se le remitió una copia de la solicitud de financiación que había firmado con la clínica dental y en la que figuraba dicha entidad como financiadora. Aporto dicha solicitud como documento número [Nº].

SEXTO.- Como quiera que la citada entidad financiera ha anunciado que presentará demanda para reclamar judicialmente a mi representado/a las cuotas que restaban por pagar de la financiación del contrato de tratamiento dental, amenazando su inclusión en el registro de morosos, éste/ésta no tiene otra opción que formular la presente demanda en reclamación de la resolución por incumplimiento del contrato de prestación de servicios dentales y del contrato de financiación del mismo, por la vinculación de ambos.

Resultando que los servicios dentales ejecutados hasta su interrupción, con fecha [FECHA], ascienden a [IMPORTE] euros, importe del tratamiento realmente recibido, los pagos obtenidos en exceso por [DENOMINACIÓN SOCIAL DE LA PARTE QUE LOS PERCIBIÓ] ascienden a [IMPORTE] euros.

Se aportan justificantes de pago como bloque documental número [Nº].

SÉPTIMO.- La parte actora manifiesta que, previamente a la presentación de la presente demanda, se han llevado a cabo negociaciones con la parte demandada con el objetivo de cumplir el requisito de procedibilidad y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria, incluyéndose entre las acciones realizadas el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución (bloque documental número [Nº]).

Finalmente, mi representado/a envió requerimiento fehaciente a los demandados con fecha [FECHA], fijando un plazo de 30 días naturales para llegar a un acuerdo amistoso, a través del abogado que firma este escrito, el cual fue contestado por los codemandados por el mismo medio, rechazando el acuerdo, viéndonos en la necesidad de acudir a la presente vía judicial.

Acompaño como documento nº [Nº] el requerimiento efectuado y como documento nº [Nº] la contestación de los demandados.

FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN Y COMPETENCIA.

Radicando la competencia genérica en el orden civil de la jurisdicción, detenta la competencia objetiva y funcional la Sección Civil del Tribunal de Instancia, por aplicación de lo dispuesto en los arts. 85.1 LOPJ y 45 LEC. Asimismo, el domicilio de mi representado/a debe determinar la competencia territorial, conforme a los arts. 52.2 y 53.1 LEC.

II.- CAPACIDAD Y LEGITIMACIÓN.

Mi mandante es mayor de edad y se encuentra en situación de pleno ejercicio de sus derechos civiles, en virtud de lo dispuesto en los arts. 6.1.1.º y 7.1 LEC. Asimismo, los codemandados son personas jurídicas, cuya capacidad se reconoce en el art. 6.1.3.º LEC, derivándose su personalidad de su constitución en escritura pública inscrita en el Registro Mercantil, con la necesidad de comparecer en juicio por medio de sus representantes legales (art. 7.4 LEC).

Están legitimadas activa y pasivamente las partes, por ser los titulares de la relación jurídica discutida, siendo mi representado/a el consumidor que concertó el contrato de prestación de servicios de tratamiento dental y de financiación (art. 10 LEC).

III.- CUANTÍA Y PROCEDIMIENTO.

Conforme al art. 253 LEC, cifro la cuantía de la presente demanda en [IMPORTE] euros, correspondiente al total de lo debido, conforme a lo dispuesto en el art. 251.8.ª LEC.

Por todo ello, el procedimiento ajustado a derecho será el del juicio declarativo ordinario regulado en los arts. 399 a 436 de la misma Ley, atendiendo a la cuantía fijada, en aplicación de lo dispuesto en el art. 249.2 LEC.

IV.- POSTULACIÓN Y DEFENSA.

Conforme a los arts. 23 y 31 LEC se formula esta demanda a través de Procurador/a de los Tribunales con poder notarial para pleitos, y con dirección y firma de Letrado habilitado ante el Tribunal. Asimismo se cumplen los requisitos formales del art. 399 LEC.

V.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda cumple con el requisito de procedibilidad exigido por la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia, según se ha expuesto en el hecho séptimo y se acredita con los documentos aportados.

VI.- FONDO DE LA CUESTIÓN CONTROVERTIDA.

Se ejercita una acción de resolución por incumplimiento contractual contra la entidad [DENOMINACIÓN SOCIAL DEL PRESTADOR DEL SERVICIO], al amparo del art. 1.124 CC, con fundamento en el hecho indiscutible de haber cesado voluntariamente en el cumplimiento de su prestación, toda vez que dejó de prestar los servicios de tratamiento dental contratados desde el día [FECHA].

Acumuladamente con la anterior, se ejercita acción declarativa de la vinculación contractual entre el citado acuerdo de prestación de servicios de tratamiento dental y el de su financiación, concertado éste con [DENOMINACIÓN SOCIAL DE LA ENTIDAD FINANCIERA], y una acción resolutoria del mismo. Se fundamenta esta acción en el art. 26.2 de la Ley 16/2011, de 24 de junio, de contratos de crédito al consumo, que establece que "Sin perjuicio de lo dispuesto en el artículo 29, la ineficacia del contrato de consumo determinará también la ineficacia del contrato de crédito destinado a su financiación, con los efectos previstos en el artículo 23".

El art. 29.1 de la Ley 16/2011 señala que "Por contrato de crédito vinculado se entiende aquel en el que el crédito contratado sirve exclusivamente para financiar un contrato relativo al suministro de bienes específicos o a la prestación de servicios específicos y ambos contratos constituyen una unidad comercial desde un punto de vista objetivo".

Siguiendo en este punto a la Directiva 2008/48/CE, se elimina el requisito de la exclusividad (esto es, que el acuerdo entre el proveedor y el financiador en virtud del cual aquél ofrecía los servicios financieros de éste a sus clientes fuera en exclusiva), que había generado problemas con la anterior normativa. La Ley 62/2003, de 30 de diciembre, eliminó la necesidad de acuerdo en exclusiva en el caso de que se provean servicios de tracto sucesivo y prestación continuada. Igualmente, la jurisprudencia del Tribunal Supremo eliminó el requisito incluso para los contratos que se habían celebrado con anterioridad a la reforma (SSTS de 25 de noviembre de 2009, Rec. 1448/2005; 19 de febrero de 2010, Rec. 198/2005; y 1 de febrero de 2011, Rec. 1531/2006). Ahora, con la nueva Ley, solo se requiere que ambos contratos, el de adquisición de bienes o servicios y el de financiación, constituyan una unidad comercial desde el punto de vista objetivo.

Existe unidad comercial según el art. 3 n) ii) de la Directiva "cuando el proveedor del bien o el suministrador del servicio financian el crédito al consumo o, en el caso de que este sea financiado por un tercero, cuando el prestamista se sirve de la intervención del proveedor del bien o el suministrador del servicio en la preparación o celebración del contrato de crédito, o cuando los bienes específicos o la prestación de un servicio específico vienen expresamente indicados en el contrato de crédito".

Incorporado, como en el caso de autos, el tratamiento de asistencia dental a la propia financiación, como causa del mismo y razón única de la financiación concedida al paciente consumidor, es evidente que la entidad concedente del crédito lo hizo asumiendo las consecuencias dimanantes de tal expresa vinculación, lo que permite configurar ese crédito como un negocio ejecutivo o instrumental del de consumo, y debe concluirse que el prestatario es un consumidor indisociable de crédito y de consumo en una modalidad de tracto duradero y, en cuanto tal, no puede ser constreñido al cumplimiento de la contraprestación periódica desde el preciso instante en que el servicio deja de prestarse por el profesional. Es decir, el art. 1.257 CC no impide que, por virtud del nexo de conexión existente entre distintos contratos, la ineficacia de uno arrastre la del otro, dando lugar al fenómeno conocido como ineficacia en cadena o propagada (STS de 19 de febrero de 2010, Rec. 198/2005).

En el presente caso es indiscutible la existencia de un acuerdo entre prestador del servicio y prestamista, pues aquél utilizó documentación facilitada expresamente por ésta para captar el cliente para la financiadora, haciendo tal labor comercial siguiendo sus instrucciones y ofertando las condiciones que la entidad financiera había fijado para tales operaciones.

Dada esta vinculación, la ineficacia del contrato de prestación de servicios determina la resolución del de financiación, desde el momento en que se declara la resolución del contrato de prestación de servicios.

Respecto a las consecuencias derivadas de la resolución contractual, debe partirse de que toda resolución contractual tiene efectos retroactivos, de tal manera que las partes están obligadas a restituirse recíprocamente las prestaciones recibidas para lograr una situación igual a la que existía antes de la celebración del contrato, como si el negocio no se hubiere concluido, tal como afirma la STS de 9 de octubre de 2003, Rec. 4075/1997. Pero en supuestos como el presente, en el que los contratos son de tracto sucesivo o de larga duración, los efectos de la retroactividad se producen desde el momento del incumplimiento de las obligaciones de los contratos por la parte que ha motivado la resolución, porque de otra manera, es decir, si se retrotrajesen los efectos hasta el momento de celebración de los contratos, se produciría una situación de enriquecimiento injusto de una de las partes, lo cual no es jurídicamente admisible (SAP Madrid de 24 de junio de 2010, Rec. 607/2008, que cita las SSTS de 20 de abril de 1994, Rec. 1828/1991; 10 de julio de 1998, Rec. 1047/1994; 17 de abril de 2001, Rec. 927/1996; y 9 de octubre de 2003, Rec. 4227/1997, entre otras muchas), de tal forma que los efectos de la resolución del contrato, por ser de tracto sucesivo, deben producirse desde el incumplimiento de las obligaciones de una de las partes, siendo desde ese momento indebido el pago del precio de la prestación de los servicios, lo que es una consecuencia aplicable a la entidad financiera demandada de conformidad con lo dispuesto en el citado art. 26.2 de la Ley 16/2011, de 24 de junio, de contratos de crédito al consumo.

VII.- COSTAS.

En cuanto a las costas, se impondrán a las demandadas por criterio de vencimiento, en aplicación del art. 394 LEC.

Por lo expuesto,

SUPLICO AL TRIBUNAL

que tenga por presentado este escrito con sus documentos y copia de todo ello, y tenga por presentada DEMANDA DE JUICIO ORDINARIO contra las entidades [DENOMINACIÓN SOCIAL DEL PRESTADOR DEL SERVICIO] y [DENOMINACIÓN SOCIAL DE LA ENTIDAD FINANCIERA], emplazarlas en los domicilios indicados y, previos los trámites legales oportunos, dicte sentencia por la que:

a) DECLARE la resolución por incumplimiento del contrato de tratamiento dental concertado entre demandante y [DENOMINACIÓN SOCIAL DEL PRESTADOR DEL SERVICIO] a partir del [FECHA].

b) DECLARE la vinculación de dicho contrato y el de financiación suscrito con [DENOMINACIÓN SOCIAL DE LA ENTIDAD FINANCIERA], así como la resolución de éste último con efectos desde la misma fecha.

c) CONDENE a [DENOMINACIÓN SOCIAL DE LA PARTE DEMANDADA CONDENADA] a no girar más recibos posteriores a esta fecha contra el actor y a devolver al actor el importe de la cantidad percibida en exceso, que asciende a [IMPORTE] euros, más el interés legal desde la interposición de la demanda, así como a no incluirle en ningún fichero de morosos y, en su caso, a cancelar de forma definitiva cualquier asiento practicado en dichos registros relativo al actor y derivado de los contratos referidos.

Todo ello con expresa condena en costas a las demandadas.

Es justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Abogado/a: [FIRMA]	Firma del Procurador/a: [FIRMA]
