---
name: demanda-juicio-ordinario-exigir-cumplimiento-contrato-civ-0751
description: "Demanda de juicio ordinario para exigir el cumplimiento de un contrato de suministro mercantil. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio ordinario para exigir el cumplimiento de un contrato de suministro mercantil

> Formulario **CIV-0751** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio declarativo ordinario por la que un fabricante o comprador, tras la interrupción unilateral e injustificada del suministro por parte de su proveedor, ejercita la acción de cumplimiento de un contrato de suministro mercantil (art. 1124 CC) para obtener la reanudación del suministro durante el plazo restante del contrato, reservándose la reclamación de daños y perjuicios.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio ordinario para exigir el cumplimiento de un contrato de suministro mercantil» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio ordinario para exigir el cumplimiento de un contrato de suministro mercantil” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:demanda-juicio-ordinario-exigir-cumplimiento-contrato-civ-0751`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (13 veces)
- [ ] DENOMINACIÓN DEL PROVEEDOR (4 veces)
- [ ] FECHA (4 veces)
- [ ] DENOMINACIÓN DEL COMPRADOR (3 veces)
- [ ] FECHA DE FIN (3 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] DENOMINACIÓN SOCIAL DE LA DEMANDADA (2 veces)
- [ ] DENOMINACIÓN SOCIAL DE LA DEMANDANTE (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] AÑO
- [ ] COLEGIO
- [ ] COMPONENTE O PRODUCTO SUMINISTRADO, CON SU MODELO
- [ ] COMUNIDAD AUTÓNOMA EXCLUIDA
- [ ] CORREO ELECTRÓNICO
- [ ] DÍA
- [ ] FECHA DE INICIO
- [ ] FECHAS
- [ ] IMPORTE
- [ ] IMPORTE EN LETRA
- [ ] LOCALIDAD
- [ ] MES
- [ ] NOMBRE Y APELLIDOS DEL LETRADO/A
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] Nº DE CLÁUSULA
- [ ] Nº DE COLEGIADO
- [ ] Nº DE HOJA
- [ ] Nº DE INSCRIPCIÓN
- [ ] PERIODICIDAD
- [ ] PLAZO
- [ ] PLAZOS DE ENTREGA
- [ ] PRINCIPALES CLIENTES
- [ ] PRODUCTO FABRICADO
- [ ] PROVINCIA
- [ ] SEDE
- [ ] TELÉFONO
- [ ] TOMO
- [ ] ÁMBITO DE IMPLANTACIÓN

## Normas que cita el formulario

- art. 399.1 LEC
- art. 85.1 LOPJ
- art. 45 LEC
- art. 51.1 LEC
- art. 253 LEC
- art. 249.1 LEC
- art. 23 LEC
- art. 5 Ley Orgánica 1/2025
- art. 1255 CC
- art. 1124 CC
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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] QUE POR TURNO CORRESPONDA»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…ma Ley, en aplicación de lo dispuesto en el apartado tercero del art. 249.1 LEC.»: el original remitía al «apartado tercero de dicho precepto»; comprobar la remisión exacta (art. 249.1.8.º o 249.2 LEC) según la redacción vigente.

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] QUE POR TURNO CORRESPONDA

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, en nombre y representación de la entidad [DENOMINACIÓN SOCIAL DE LA DEMANDANTE], a cuya justificación aporto escritura de poder inscrita en el Registro Electrónico de Apoderamientos Judiciales con el n.º [Nº DE INSCRIPCIÓN] y que se puede acreditar mediante consulta automatizada orientada al dato, por parte del órgano judicial al cual tengo el honor de dirigirme, acompañándose certificación electrónica del Registro Electrónico de Apoderamientos Judiciales como Documento n.º [Nº DE DOCUMENTO], por si no es posible la consulta automatizada, dirigido por el/la Letrado/a abajo firmante D./Dña. [NOMBRE Y APELLIDOS DEL LETRADO/A], con número de colegiado/a [Nº DE COLEGIADO] del Ilustre Colegio de la Abogacía de [COLEGIO], y con despacho profesional en [DOMICILIO], ante el Tribunal comparezco y como mejor proceda en Derecho,

DIGO

Que, en la representación que ostento, interpongo demanda de juicio declarativo ordinario ejercitando acción de cumplimiento de contrato de suministro mercantil contra la entidad [DENOMINACIÓN SOCIAL DE LA DEMANDADA], con domicilio en [DOMICILIO].

Que esta parte asume el compromiso de recibir cualquier comunicación dirigida por la oficina judicial, durante toda la fase declarativa e, incluso, en una eventual fase de ejecución, por medios telemáticos, en términos del art. 399.1 II LEC, consignándose a estos efectos la siguiente dirección de correo electrónico y n.º de teléfono: [CORREO ELECTRÓNICO] / [TELÉFONO].

Fundamento la misma en los siguientes hechos y consideraciones jurídicas:

HECHOS

PRIMERO.- Mi representada, [DENOMINACIÓN SOCIAL DE LA DEMANDANTE], tiene como objeto social [OBJETO SOCIAL: FABRICACIÓN DE [PRODUCTO FABRICADO]], con implantación en el mercado [ÁMBITO DE IMPLANTACIÓN], y contratos en vigor con [PRINCIPALES CLIENTES]. Se encuentra inscrita en el Registro Mercantil de [PROVINCIA], hoja [Nº DE HOJA], tomo [TOMO], presenta anualmente sus cuentas anuales y está al corriente en el pago de sus obligaciones fiscales. Se acompañan copias de los contratos en vigor, como bloque documental n.º [Nº]; certificación del Registro Mercantil en relación con la hoja registral abierta, como documento n.º [Nº]; copias de las últimas declaraciones tributarias, como bloque documental n.º [Nº]; y copias de los contratos con los principales clientes, como bloque documental n.º [Nº].

La demandada es titular de una cadena de establecimientos comerciales que se dedican a la venta y distribución en el territorio nacional de [COMPONENTE O PRODUCTO SUMINISTRADO, CON SU MODELO], componente esencial, por sus especificidades con las que es fabricado, de los productos que elabora mi patrocinada.

SEGUNDO.- Dado que la ahora demandada ostentaba la distribución exclusiva en España de dicho componente, atendiendo a la calidad del mismo y a la necesidad de poder ofrecer, de manera permanente, los productos a los clientes citados, mi cliente suscribió con la primera un contrato de distribución mercantil en fecha [FECHA], cuyas cláusulas más importantes son las siguientes:

1.ª) [DENOMINACIÓN DEL PROVEEDOR] venderá sus productos a [DENOMINACIÓN DEL COMPRADOR] por el precio fijado en la cláusula [Nº DE CLÁUSULA]. Los pagos se verificarán en tres plazos, a los [Nº] días, [Nº] días y [Nº] días desde la recepción de la mercancía.

2.ª) [DENOMINACIÓN DEL COMPRADOR] adquiere los productos en forma exclusiva y como único distribuidor a terceros. El pacto de distribución en exclusiva se extiende a todo el territorio nacional, excepto a la comunidad autónoma de [COMUNIDAD AUTÓNOMA EXCLUIDA].

3.ª) [DENOMINACIÓN DEL PROVEEDOR] se compromete a efectuar las entregas de los citados géneros en los siguientes plazos: [PLAZOS DE ENTREGA].

4.ª) [DENOMINACIÓN DEL COMPRADOR] se compromete a no vender en sus establecimientos otros géneros distintos de los adquiridos de [DENOMINACIÓN DEL PROVEEDOR]. Por otro lado, garantiza a [DENOMINACIÓN DEL PROVEEDOR] unas compras mínimas de [IMPORTE EN LETRA] euros ([IMPORTE] €) anuales.

5.ª) La duración del presente contrato será de [Nº] años, iniciándose en [FECHA DE INICIO] y concluyendo en [FECHA DE FIN].

Se acompaña el original del contrato celebrado entre las partes como documento n.º [Nº DE DOCUMENTO].

TERCERO.- Durante los últimos [Nº] años y hasta el mes pasado, el suministro ha sido regular, respetando escrupulosamente lo acordado, tal y como se acredita con los albaranes periódicos firmados por la demandada y que acompaño como bloque documental n.º [Nº].

CUARTO.- Sorprendentemente, y sin previo aviso, la demandada dejó de suministrar el pedido correspondiente al mes pasado, y que debería haberse entregado el pasado día [FECHA]. Mi representada ha tratado de ponerse en contacto con la misma por todos los medios, habiendo enviado hasta [Nº] burofaxes en requerimiento de que se reanude el suministro, pidiendo una explicación por la interrupción, que no se nos ha ofrecido. Se ha indicado que se dispone de reservas para seguir produciendo durante [PLAZO] más, si bien, de no recibir más suministros, la producción tendría que interrumpirse. Extremo que podría llevar a los principales clientes a acudir a otros productores, con pérdida de los contratos que se tienen, lo que supondría la paralización de la actividad de la demandante. Se adjuntan los burofaxes como bloque documental n.º [Nº], sin que se haya recibido respuesta.

QUINTO.- La parte actora manifiesta que, previamente a la presentación de la presente demanda, se han llevado a cabo negociaciones con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria; incluyéndose entre las acciones realizadas el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución.

Finalmente, ante la situación desesperada a la que se veía abocada mi patrocinada, se requirió notarialmente para la reanudación del suministro, fijando un plazo de 30 días naturales para llegar a un acuerdo amistoso, con advertencia de la interposición de la presente demanda, y con reserva de los perjuicios que se pudieran acabar ocasionando, advirtiendo de la elevada cantidad de los mismos. Se aporta acta de requerimiento notarial como documento n.º [Nº DE DOCUMENTO], en la que se certifica que, realizado el requerimiento en las oficinas de la demandada, nadie ofreció una respuesta ante la interrupción unilateral llevada a cabo.

A los anteriores hechos son aplicables los siguientes

FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN Y COMPETENCIA

Radicando la competencia genérica en el orden civil de la jurisdicción, detenta la competencia objetiva y funcional la Sección Civil del Tribunal de Instancia, por aplicación de lo dispuesto en el art. 85.1 LOPJ y art. 45 LEC. Asimismo, dado que se pretende el cumplimiento de un contrato de suministro suscrito con la entidad demandada, y puesto que la misma tiene su domicilio en el partido judicial del Tribunal al cual tengo el honor de dirigirme, su situación debe determinar la competencia territorial, conforme al art. 51.1 LEC.

II.- CAPACIDAD

Al tratarse de sociedades mercantiles inscritas en el Registro Mercantil, de conformidad con los arts. 20 y 33 del Texto Refundido de la Ley de Sociedades de Capital, aprobado por Real Decreto Legislativo 1/2010, de 2 de julio, tienen personalidad jurídica y, consiguientemente, capacidad para ser parte y capacidad para comparecer en juicio.

III.- LEGITIMACIÓN

Corresponde al demandante la activa por ser parte en el contrato suscrito, y la pasiva la tiene la demandada en cuanto ocupa la posición de contraparte contractual y ha verificado la interrupción en el suministro que se pretende reanudar.

IV.- CUANTÍA Y PROCEDIMIENTO

Conforme al art. 253 LEC, no es posible determinar, ni siquiera de manera relativa, la cuantía, atendiendo a la acción de cumplimiento ejercitada, sin reclamación de daños y perjuicios, cuya posibilidad se reserva mi mandante. Por todo ello, el procedimiento ajustado a derecho será el del juicio declarativo ordinario regulado en los arts. 399 a 436 de la misma Ley, en aplicación de lo dispuesto en el apartado tercero del art. 249.1 LEC.

V.- POSTULACIÓN Y DEFENSA

Conforme a lo previsto en los arts. 23 y 31 LEC, se presenta la demanda por medio de Procurador/a legalmente habilitado y bajo dirección de Letrado firmante de la misma.

VI.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4.º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

VII.- FONDO DE LA CUESTIÓN CONTROVERTIDA

A) Naturaleza del contrato que liga a las partes

El contrato de suministro que liga a las partes es una figura afín a la compraventa, en la cual, a cambio de un precio, en vez de entregar una cosa unitaria (de una sola vez o en actos distintos), la obligación de entrega se cumple de manera sucesiva y periódica, en este caso cada [PERIODICIDAD]. Al respecto, se pronuncia la Sentencia del Tribunal Supremo, Sala Primera, de lo Civil, n.º 79/2002, de 7 de febrero de 2002, Rec. 2676/1996, indicando que dicho contrato se regula por lo previsto por las partes, en aras al principio de autonomía de la voluntad (art. 1255 CC) y, en su defecto, por la normativa de la compraventa (arts. 1445 y ss. CC o, en su caso, si es mercantil, 325 y ss. CCom), y en último lugar, por las normas generales de las obligaciones y contratos. Sobre la cuestión, la doctrina jurisprudencial destaca la carencia de regulación legal del llamado contrato de suministro, que implica la necesidad de recurrir a las normas generales de las obligaciones y contratos, pues aunque sea afín a la compraventa en su forma de «con entregas repartidas o diferidas» no puede identificarse con ella. Así la doctrina mercantilista señala que la diferencia radica en que en el caso de venta con entregas repetidas, la prestación es única aunque su ejecución se fraccione en el tiempo, mientras que en el suministro no hay una prestación única, sino varias prestaciones autónomas ligadas entre sí de tal suerte que lo que importa no es tanto la suma de prestaciones como las prestaciones aisladas que se reiteran a lo largo del tiempo pactado. Mientras, en la venta con entregas repetidas hay una sola obligación y una sola prestación aunque ésta se divida en partes en el momento de la ejecución, en el suministro hay una pluralidad de prestaciones autónomas que se corresponden con una pluralidad de obligaciones derivadas todas de un contrato único. Por ello puede ser definido, siguiendo al Código italiano, art. 1539, como un contrato por el que una de las partes, empresa suministradora o proveedor, se obliga a cambio de un precio a realizar en favor de otra prestaciones periódicas continuas, cuya función es la satisfacción de necesidades continuas, para atender el interés duradero del acreedor. Su contenido es, por tanto, una serie de prestaciones duraderas o de ejecución continuada o sucesiva, que recuerda la vieja fórmula de los contratos «qui habent tractum sucessium et dependentiam de futuro», y cuya razón de ser está en el deseo de hallar satisfacción rápida, segura y económica a las necesidades en la vida moderna, que sería aleatorio y antieconómico satisfacer concertando un contrato distinto en cada momento en que surgiese una necesidad.

Asimismo, la relación contractual que nos ocupa ostenta un carácter mercantil, a partir de las necesidades constantes para su producción que mi mandante tiene, y que han venido siendo satisfechas de manera periódica por la sociedad demandada hasta el momento indicado de la interrupción. En esta línea, la Sentencia del Tribunal Supremo, Sala Primera, de lo Civil, n.º 340/2003, de 3 de abril de 2003, Rec. 2529/1997, señala que «Tanto si se considera que tal contrato es una variante de la compraventa, como si se lo califica como contrato distinto pero afín al mismo, se deben aplicar normas de éste, del Código de Comercio si es mercantil, como en el presente caso». En tal resolución se recuerda una constante línea jurisprudencial clásica al respecto, con cita, entre otras, de las sentencias del mismo tribunal de 20 de mayo de 1986, de 10 de septiembre de 1987, de 8 de julio de 1988 y de 28 de febrero de 1996, rec. 2257/1992.

B) Acción que se ejercita

En la presente demanda se ejercita una acción de cumplimiento del contrato de suministro mercantil de fecha [FECHA] firmado entre las partes, en vigor, y con una duración de [Nº] años más, hasta [FECHA DE FIN]. Se acude para ello a lo dispuesto en el art. 1124 CC, que dispone que «La facultad de resolver las obligaciones se entiende implícita en las recíprocas, para el caso de que uno de los obligados no cumpliese lo que le incumbe. El perjudicado podrá escoger entre exigir el cumplimiento o la resolución de la obligación con el resarcimiento de daños y abono de intereses en ambos casos. También podrá pedir la resolución, aun después de optar por el cumplimiento, cuando éste resultare imposible». En este sentido, mi mandante opta por exigir el cumplimiento de lo firmado, ante la imperiosa necesidad de su reanudación, a fin de mantener las relaciones comerciales con sus clientes, a riesgo de abocar a la paralización y eventual disolución de la misma. Repárese en que la propia esencia del contrato de suministro, su repetición en el tiempo en la forma que se haya pactado, conforma la necesidad de mi cliente que ahora se ve insatisfecha. Es decir, mi mandante se obligó contractualmente con la demandada para asegurar el suministro de un componente esencial del producto que ofrece (que además determina la calidad del mismo), de manera periódica, a fin de que sus principales clientes no se vean desatendidos en ningún momento. Repárese, en todo caso, en la dimensión de las referidas entidades clientes y la alta posibilidad de que cambien de suministrador, en cuanto perciban problemas en las entregas. Por todo ello, se realiza un último intento para reanudar un suministro vital para mi patrocinada, reservándonos la acción para reclamar los cuantiosos daños y perjuicios que se irrogarán, sin lugar a dudas, en el caso de que la interrupción se mantenga, u otras acciones que pudieran corresponder.

En todo caso, para el ejercicio de la presente acción, la SAP Barcelona, Sección 11.ª, de 29 de junio de 2007 (rec. 401/2007), exige, en primer lugar, la acreditación de la existencia de relaciones comerciales relacionadas con el proceso industrial en cuyo marco el suministro se ve interrumpido; lo que se puede comprobar con el contrato aportado y firmado por representantes de la demandada, así como con el bloque de albaranes periódicos que se acompañaron a la demanda, completado con las copias de los contratos en su día firmados con los principales clientes. En segundo lugar, debe probarse la interrupción unilateral del suministro, que se puede constatar con las reclamaciones extrajudiciales hechas a la demandada, en las cuales, precisamente, se imputa a la demandada una suspensión injustificada del mismo, y no obtienen ninguna respuesta en el sentido de ofrecer una realidad distinta de lo que se les está imputando.

VIII.- COSTAS

Conforme al art. 394 LEC, las costas han de imponerse a la demandada.

Por lo expuesto,

SUPLICO AL TRIBUNAL

Que habiendo por presentado este escrito de demanda con los documentos que lo acompañan y copias de uno y otros, los admita y me tenga por comparecido en parte en la representación que ostento y que acreditada dejo; y por promovido juicio declarativo ordinario frente a [DENOMINACIÓN SOCIAL DE LA DEMANDADA], acuerde dar traslado a la demandada para que comparezca y la conteste, y previos los trámites legales y recibimiento a prueba que desde ahora se interesa, se dicte en su día sentencia por la que, estimando la demanda, se condene a la demandada a reanudar el suministro en los términos expuestos en el contrato de suministro de fecha [FECHA], de la misma forma que se llevó a cabo hasta el día en que fue interrumpido, y durante el plazo que le resta al contrato, hasta el [FECHA DE FIN], con imposición de las costas a la demandada.

Es justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Abogado/a Firma del Procurador/a
