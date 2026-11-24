---
name: demanda-juicio-ordinario-resolver-suministro-exclusiva-civ-0738
description: "Demanda de juicio ordinario para resolver un suministro con exclusiva y reclamar cantidad. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio ordinario para resolver un suministro con exclusiva y reclamar cantidad

> Formulario **CIV-0738** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio declarativo ordinario de un proveedor contra su distribuidor por incumplimiento de un contrato de suministro mercantil con pacto de exclusiva: acumula la reclamación del precio de las mercancías impagadas, la resolución del contrato (art. 1124 CC), la indemnización de daños y perjuicios y los intereses legales. Adaptada a la LO 1/2025.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio ordinario para resolver un suministro con exclusiva y reclamar cantidad» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio ordinario para resolver un suministro con exclusiva y reclamar cantidad” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:demanda-juicio-ordinario-resolver-suministro-exclusiva-civ-0738`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (12 veces)
- [ ] Nº (11 veces)
- [ ] IMPORTE EN LETRA (9 veces)
- [ ] FECHA (8 veces)
- [ ] Nº DE DOCUMENTO (8 veces)
- [ ] DENOMINACIÓN DEL DISTRIBUIDOR (6 veces)
- [ ] DENOMINACIÓN DEL PROVEEDOR (4 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] DENOMINACIÓN SOCIAL DE LA DEMANDADA (3 veces)
- [ ] DOMICILIO (3 veces)
- [ ] DENOMINACIÓN SOCIAL DE LA DEMANDANTE (2 veces)
- [ ] Nº DE CLÁUSULA (2 veces)
- [ ] AÑO
- [ ] BASES DE CUANTIFICACIÓN
- [ ] COLEGIO
- [ ] COMUNIDAD AUTÓNOMA EXCLUIDA
- [ ] CORREO ELECTRÓNICO
- [ ] DOCUMENTO ACREDITATIVO
- [ ] DÍA
- [ ] FECHA DE FIN
- [ ] FECHA DE INICIO
- [ ] FECHAS
- [ ] MARCAS COMPETIDORAS
- [ ] MES
- [ ] NOMBRE DEL NOTARIO
- [ ] NOMBRE Y APELLIDOS DEL LETRADO/A
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] Nº DE COLEGIADO
- [ ] Nº DE DOCUMENTOS
- [ ] Nº DE HOJA
- [ ] OBJETO SOCIAL
- [ ] PERIODO
- [ ] PLAZOS DE ENTREGA
- [ ] PRODUCTOS
- [ ] PROVINCIA
- [ ] SEDE
- [ ] TELÉFONO
- [ ] TOMO

## Normas que cita el formulario

- art. 24.1 LEC
- art. 399.1 LEC
- art. 36 Ley 3/1991
- art. 45 LEC
- art. 85.1.º LOPJ
- art. 249.2 LEC
- art. 253 LEC
- art. 5 Ley Orgánica 1/2025
- art. 1124 CC
- art. 1255 CC
- art. 1106 CC
- art. 1100 CC
- art. 63.2.º CC
- art. 394 LEC
- art. 24.2 LEC

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] QUE POR TURNO CORRESPONDA»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales y de la mercantil [DENOMINACIÓN SOCIAL DE LA DEMANDANTE], con domicilio en [DOMICILIO], representación que acredito mediante escritura de poder otorgada a mi favor (el art. 24.1 LEC prevé tres formas de otorgar el apoderamiento al Procurador),

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— (Si el poder se otorga a través de la sede judicial electrónica).- mediante comparecencia electrónica, a través de la sede judicial electrónica e inscrito en el Registro Electrónico de Apoderamientos Judiciales; y a cuya justificación acompaño certificación de dicho Registro aportada como Documento n.º [Nº DE DOCUMENTO], y que se puede acreditar mediante consulta automatizada orientada al dato, por parte del órgano judicial al cual tengo el honor de dirigirme.

— (Si el poder se otorga mediante comparecencia apud acta).- mediante comparecencia personal apud acta ante el Tribunal Decano de [LOCALIDAD], posteriormente inscrito en el Registro Electrónico de Apoderamientos Judiciales; y a cuya justificación acompaño certificación de dicho Registro aportada como Documento n.º [Nº DE DOCUMENTO], y que se puede acreditar mediante consulta automatizada orientada al dato, por parte del órgano judicial al cual tengo el honor de dirigirme.

— (Si el poder se otorga ante Notario).- mediante escritura de poder otorgada a mi favor, ante el Notario/Notaria [NOMBRE DEL NOTARIO], con Notaría sita en [LOCALIDAD]. El poder se inscribió en el Registro Electrónico de Apoderamientos Judiciales; lo cual justifico mediante certificación de dicho Registro aportada como Documento n.º [Nº DE DOCUMENTO], y que se puede acreditar mediante consulta automatizada orientada al dato, por parte del órgano judicial al cual tengo el honor de dirigirme.

bajo la dirección letrada de D./Dña. [NOMBRE Y APELLIDOS DEL LETRADO/A], abogado/a en ejercicio, con despacho profesional abierto en [DOMICILIO], colegiado n.º [Nº DE COLEGIADO] del Ilustre Colegio de la Abogacía de [COLEGIO], ante el Tribunal comparezco y como mejor en Derecho proceda,

DIGO

Que mediante el presente escrito vengo a formular DEMANDA DE JUICIO DECLARATIVO ORDINARIO SOBRE RESOLUCIÓN DE CONTRATO, RECLAMACIÓN DE CANTIDAD Y OTROS PARTICULARES, contra la entidad [DENOMINACIÓN SOCIAL DE LA DEMANDADA], con domicilio en [DOMICILIO]; todo ello de conformidad con los hechos y fundamentos de derecho que se especificarán.

Que esta parte asume el compromiso de recibir cualquier comunicación dirigida por la oficina judicial, durante toda la fase declarativa e, incluso, en una eventual fase de ejecución, por medios telemáticos, en términos del art. 399.1 II LEC, consignándose a estos efectos la siguiente dirección de correo electrónico y n.º de teléfono: [CORREO ELECTRÓNICO] / [TELÉFONO].

HECHOS

PRIMERO.- Mi patrocinada, [DENOMINACIÓN SOCIAL DE LA DEMANDANTE], tiene como objeto social [OBJETO SOCIAL]. Se encuentra inscrita en el Registro Mercantil de [PROVINCIA], hoja [Nº DE HOJA], tomo [TOMO] y está al corriente en el pago de sus obligaciones fiscales, como se acredita mediante [DOCUMENTO ACREDITATIVO] que se acompaña como DOCUMENTO N.º [Nº DE DOCUMENTO].

La demandada es titular de una cadena de establecimientos comerciales que se dedican a la venta y distribución en el territorio nacional de [PRODUCTOS].

SEGUNDO.- Interesando a ambas partes el establecimiento de relaciones comerciales, ya que mi representada podía vender su producción en la mayor parte del territorio nacional y la demandada adquiría un producto de reconocida calidad, con fecha [FECHA] firmaron un contrato del que destacamos, por ser relevante para la resolución del presente litigio, las siguientes cláusulas:

1.ª) [DENOMINACIÓN DEL PROVEEDOR] venderá sus productos a [DENOMINACIÓN DEL DISTRIBUIDOR] por el precio fijado en la cláusula [Nº DE CLÁUSULA]. Los pagos se verificarán en tres plazos, a los [Nº] días, [Nº] días y [Nº] días desde la recepción de la mercancía.

2.ª) [DENOMINACIÓN DEL DISTRIBUIDOR] adquiere los productos en forma exclusiva y como único distribuidor a terceros. El pacto de distribución en exclusiva se extiende a todo el territorio nacional, excepto a la comunidad autónoma de [COMUNIDAD AUTÓNOMA EXCLUIDA].

3.ª) [DENOMINACIÓN DEL PROVEEDOR] se compromete a efectuar las entregas de los citados géneros en los siguientes plazos: [PLAZOS DE ENTREGA].

4.ª) [DENOMINACIÓN DEL DISTRIBUIDOR] se compromete a no vender en sus establecimientos otros géneros distintos de los adquiridos de [DENOMINACIÓN DEL PROVEEDOR]. Por otro lado, garantiza a [DENOMINACIÓN DEL PROVEEDOR] unas compras mínimas de [IMPORTE EN LETRA] euros ([IMPORTE] €) anuales.

5.ª) La duración del presente contrato será de [Nº] años, iniciándose en [FECHA DE INICIO] y concluyendo en [FECHA DE FIN].

Se acompaña el original del contrato celebrado entre las partes como DOCUMENTO N.º [Nº DE DOCUMENTO].

TERCERO.- En cumplimiento del mencionado contrato, mi representada envió la primera entrega con fecha [FECHA], por valor de [IMPORTE EN LETRA] euros ([IMPORTE] €), según se acredita con los albaranes firmados por la demandada y que acompaño como DOCUMENTOS N.º [Nº DE DOCUMENTOS].

CUARTO.- La demandada no verificó el primero de los pagos estipulados, enviando en fecha [FECHA] una carta a mi representada en que aducía problemas transitorios de liquidez y manifestaba su convencimiento en liquidar la deuda en un plazo no superior a quince días. Sin embargo, en fecha [FECHA] la demandada únicamente verificó el pago de [IMPORTE EN LETRA] euros ([IMPORTE] €), remitiendo otra carta a mi principal en la que manifestaba que el resto de la cantidad debida, esto es [IMPORTE], no se abonaba pues el Departamento de control de calidad había rechazado varios lotes de géneros servidos.

Mi patrocinada contestó dicha carta en fecha [FECHA], manifestando su disconformidad y solicitando de la demandada una solución amistosa.

Se acompañan dichas cartas como DOCUMENTOS N.º [Nº], [Nº], [Nº] y [Nº], respectivamente.

QUINTO.- Estando mi mandante dispuesta, como así hizo, a continuar con el cumplimiento de las obligaciones asumidas contractualmente, preparó la segunda entrega, que tuvo lugar en la fecha pactada, esto es el [FECHA], a pesar de que se encontraba pendiente de pago una cantidad de [IMPORTE EN LETRA] euros ([IMPORTE] €), con la confianza de que, ante su regular cumplimiento, se solucionara el problema.

Pero lejos de atemperar su conducta a los cánones de la buena fe, la demandada solo hizo efectivo el importe de parte del suministro, restándole por pagar [IMPORTE EN LETRA] euros ([IMPORTE] €). Esto dio lugar a sendas comunicaciones entre la demandada y mi patrocinada, sin que justificara su incumplimiento en motivo razonable. A tales efectos, acompaño como DOCUMENTOS N.º [Nº] los albaranes de entrega y comunicaciones entre los litigantes sobre el precio que faltaba por satisfacer. Por tanto, la cantidad que se adeuda a mi representada es de [IMPORTE EN LETRA] euros ([IMPORTE] €).

SEXTO.- La demandada, no limitándose a los incumplimientos expuestos, ha ignorado las obligaciones contraídas, vendiendo en sus establecimientos géneros de otras marcas de la competencia como [MARCAS COMPETIDORAS], con lo que se han perjudicado las expectativas de mi patrocinada de ver aumentados los pedidos de la demandada ante la demanda de sus productos, que debía ir en aumento, en lugar de detenerse en la cifra mínima pactada.

A tales efectos acompaño como DOCUMENTOS N.º [Nº] actas de requerimiento notarial en las que se certifica cómo durante [PERIODO] la demandada vendió en sus establecimientos géneros que no eran de mi principal. Y como DOCUMENTO N.º [Nº] testimonio de la diligencia preliminar practicada al amparo de lo dispuesto en el art. 36 de la Ley 3/1991, de 10 de enero, de Competencia Desleal.

SÉPTIMO.- Mi patrocinada se ha visto obligada por todo ello a presentar esta demanda no solo para que se declare el incumplimiento contractual, sino para reclamar la cantidad que se le adeuda, así como para que se le satisfaga la cantidad por los daños y perjuicios que se le van a ocasionar por la resolución contractual que se insta.

La resolución contractual le produce un daño extraordinario por cuanto se verá obligada a buscar nuevos comerciantes para la venta de sus productos en el mercado. Y ello con gran rapidez, puesto que sus fábricas se encuentran en pleno rendimiento y el escaso tiempo que resta hasta la próxima temporada le impide crear una nueva red de distribución. Por tanto, se cifran las pérdidas en [IMPORTE EN LETRA] euros ([IMPORTE] €), partiendo de las cifras mínimas comprometidas contractualmente con [DENOMINACIÓN DEL DISTRIBUIDOR].

OCTAVO.- La parte actora manifiesta que, previamente a la presentación de la presente demanda, se han llevado a cabo negociaciones con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria; incluyéndose entre las acciones realizadas el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución.

Finalmente, mi representada envió un requerimiento fehaciente a la demandada con fecha [FECHA], fijando un plazo de 30 días naturales para llegar a un acuerdo amistoso, a través del abogado que firma este escrito, el cual fue contestado por la demandada por el mismo medio, [ELEGIR: rechazando el acuerdo / habiendo sido solo posible un acuerdo parcial], viéndonos en la necesidad de acudir a la presente vía judicial, respecto a los extremos de la controversia en los que se mantiene la discrepancia.

Acompaño como documento n.º [Nº DE DOCUMENTO] el requerimiento efectuado y como documento n.º [Nº DE DOCUMENTO] la contestación de la demandada.

A los anteriores hechos son aplicables los siguientes

FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN Y COMPETENCIA

Es competente la Sección Civil del Tribunal de Instancia del domicilio del demandado, al que se dirige la presente demanda, por aplicación de lo dispuesto en los arts. 45 y 51 LEC, en relación con lo dispuesto en el art. 85.1.º LOPJ.

El domicilio social de la entidad demandada se encuentra en la ciudad de [LOCALIDAD], como resulta del DOCUMENTO N.º [Nº DE DOCUMENTO] que se acompaña, y se podrá comprobar con la certificación del Registro Mercantil, que se aportará en su momento a los autos, una vez expedida y retirada.

II.- PROCEDIMIENTO

El procedimiento ajustado a derecho será el del juicio declarativo ordinario regulado en los arts. 399 a 436 de la misma Ley, atendiendo a la cantidad reclamada, que es de [IMPORTE] euros, en aplicación de lo dispuesto en el art. 249.2 LEC.

III.- CAPACIDAD

Al tratarse de sociedades mercantiles inscritas en el Registro Mercantil, de conformidad con los arts. 20 y 33 del Texto Refundido de la Ley de Sociedades de Capital, aprobado por Real Decreto Legislativo 1/2010, de 2 de julio, tienen personalidad jurídica y, consiguientemente, capacidad para ser parte y capacidad para comparecer en juicio.

IV.- LEGITIMACIÓN

Corresponde al demandante la activa por ser parte en el contrato suscrito y haber cumplido sus obligaciones contractuales como vendedor, y la pasiva la tiene el demandado en cuanto ocupa la posición de contraparte contractual y ha venido realizando los actos contrarios a las obligaciones asumidas.

V.- CUANTÍA

Conforme al art. 253 LEC cifro la cuantía de la presente demanda en [IMPORTE] euros, que es el importe de la cantidad que se reclama.

VI.- POSTULACIÓN Y DEFENSA

Conforme a lo previsto en los arts. 23 y 31 de la Ley de Enjuiciamiento Civil, se presenta la demanda por medio de Procurador/a legalmente habilitado y bajo dirección de Letrado firmante de la misma.

VII.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4.º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

VIII.- FONDO DE LA CUESTIÓN CONTROVERTIDA

A) Acciones que se ejercitan

En esta demanda se acumulan diversas acciones, al amparo de lo dispuesto en los arts. 71 y ss. LEC, en cuanto tienen su origen en el mismo incumplimiento contractual, se dirigen contra el mismo demandado y no son incompatibles.

Las acciones que se ejercitan son las siguientes: a) Reclamación de cantidad al amparo de las disposiciones generales sobre contratación y compraventa mercantil, arts. 1089 y ss. CC y arts. 325 y ss. CCom; y b) Acción de resolución contractual, en virtud de lo previsto en el art. 1124 CC, con la subsiguiente indemnización por los daños y perjuicios causados.

B) Reclamación de cantidad por impago de las mercancías

Con carácter preliminar debe establecerse la calificación jurídica del contrato suscrito entre las partes. Ciertamente se trata de un contrato atípico de suministro, de naturaleza mercantil, dada la condición de empresarios de los litigantes y la finalidad de las ventas.

La doctrina jurisprudencial destaca la carencia de regulación legal del llamado contrato de suministro, que implica la necesidad de recurrir a las normas generales de las obligaciones y contratos, pues aunque sea afín a la compraventa en su forma de «con entregas repartidas o diferidas» no puede identificarse con ella; así la doctrina mercantilista señala que la diferencia radica en que en el caso de venta con entregas repetidas, la prestación es única aunque su ejecución se fraccione en el tiempo, mientras que en el suministro no hay una prestación única, sino varias prestaciones autónomas ligadas entre sí de tal suerte que lo que importa no es tanto la suma de prestaciones como las prestaciones aisladas que se reiteran a lo largo del tiempo pactado. Mientras en la venta con entregas repetidas hay una sola obligación y una sola prestación aunque ésta se divida en partes en el momento de la ejecución, en el suministro hay una pluralidad de prestaciones autónomas que se corresponden con una pluralidad de obligaciones derivadas todas de un contrato único. Por ello puede ser definido, siguiendo al Código italiano, art. 1539, como un contrato por el que una de las partes, empresa suministradora o proveedor, se obliga a cambio de un precio a realizar en favor de otra prestaciones periódicas continuas, cuya función es la satisfacción de necesidades continuas, para atender el interés duradero del acreedor. Su contenido es, por tanto, una serie de prestaciones duraderas o de ejecución continuada o sucesiva, que recuerda la vieja fórmula de los contratos «qui habent tractum sucessium et dependentiam de futuro», y cuya razón de ser está en el deseo de hallar satisfacción rápida, segura y económica a las necesidades en la vida moderna, que sería aleatorio y antieconómico satisfacer concertando un contrato distinto en cada momento en que surgiese una necesidad.

A tal fin, se regulará en primer lugar por las normas específicamente pactadas, conforme a lo establecido en el art. 1255 CC, y en defecto de pacto o estipulación, teniendo presente el desarrollo de la relación comercial, según establece la doctrina legal, han de aplicarse en el caso concreto las normas propias de la compraventa mercantil de los arts. 325 y ss. CCom, puesto que la calificación de suministro determina la aplicación, por vía supletoria y última, de los preceptos reguladores de la compraventa.

Establecido lo anterior, la obligación principal de [DENOMINACIÓN DEL DISTRIBUIDOR] es pagar el precio, sin que pueda exculparse por una presunta presencia de vicios, no reclamados en tiempo oportuno, al tener, dada la naturaleza mercantil del tráfico, unos plazos de caducidad muy cortos que, en definitiva y de admitirse su existencia, lo que se plantea a meros efectos dialécticos, resultarían conculcados.

C) Resolución contractual por incumplimiento unilateral de las obligaciones derivadas del pacto de exclusiva

El art. 1124 CC establece que la facultad de resolver las obligaciones se entiende implícita en las recíprocas para el caso de que uno de los obligados no cumpliere lo que le incumbe. El perjudicado podrá escoger entre exigir el cumplimiento o la resolución de la obligación, con el resarcimiento de daños y abono de intereses en ambos casos.

En el supuesto litigioso, conjuntamente con las obligaciones de suministro y pago de las mercancías, se contempla un pacto de exclusiva mediante el que [DENOMINACIÓN DEL DISTRIBUIDOR] se obligaba a vender en sus establecimientos exclusivamente los géneros de mi patrocinada (CLÁUSULA [Nº DE CLÁUSULA]).

La doctrina jurisprudencial, sentada en la STS de 22 de marzo de 1988, en torno al llamado pacto de exclusiva ha sentado las siguientes conclusiones:

1) Que dicho pacto, examinado por la jurisprudencia a partir de la sentencia de 23 de marzo de 1921 y definido en las de 29 de octubre de 1955 y 31 de diciembre de 1970, al orientarse en el sentido de evitar la concurrencia en el mercado, entraña una restricción a la libertad comercial de los contratantes que, como tal, no debe interpretarse en sentido amplio, sino limitado;

2) Que dado el intuitu personae que juega en los contratos de distribución de productos con pacto de exclusiva, por la repercusión que en el patrimonio de cada contratante puede ocasionar la inactividad o falta de diligencia del otro, se suele acompañar en la práctica mercantil, cuando se concierta sin fijación de plazo, de una cláusula de resolución «ad nutum» con exención de resarcimiento de daños y perjuicios, que actúa como válvula de seguridad para compensarles del riesgo que mutuamente corren.

Examinando el caso concreto, aparece que dicha válvula de seguridad no se pactó. En cambio, frente al incumplimiento de la demandada de su obligación de venta en exclusiva, mi representada ha cumplido diligentemente sus obligaciones contractuales derivadas del contrato de suministro y del pacto de distribución en exclusiva. Por lo tanto, podrá instarse, al amparo del art. 1124 CC, la resolución judicial conjuntamente con la indemnización de los daños y perjuicios causados a mi principal.

D) Indemnización de daños y perjuicios

La expresión que contiene el art. 1124 CC («resarcimiento de daños y abono de intereses») es equivalente de indemnización de daños y perjuicios, comprendiéndose tanto el daño emergente como el lucro cesante. Citamos en este sentido los arts. 1106 y 1107 CC.

Siendo las bases para su cuantificación las siguientes: [BASES DE CUANTIFICACIÓN], aportando al efecto los documentos que las acreditan.

E) Intereses

Citamos los arts. 1100, 1101, 1108 y 1109 CC y el art. 63.2.º CCom, sobre pago de los intereses moratorios a partir de la interpelación judicial.

IX.- COSTAS

Conforme al art. 394 LEC, las costas han de imponerse a la parte demandada.

Por lo expuesto,

SUPLICO AL TRIBUNAL

Que habiendo por presentado este escrito de demanda con los documentos que lo acompañan y copias de uno y otros, los admita y me tenga por comparecido en parte en la representación que ostento y que acreditada dejo; y por promovido juicio declarativo ordinario frente a [DENOMINACIÓN SOCIAL DE LA DEMANDADA], acuerde dar traslado a la demandada para que comparezca y la conteste, y previos los trámites legales y recibimiento a prueba que desde ahora se interesa, se dicte en su día sentencia por la que, estimando la demanda:

A) Se condene a la demandada, [DENOMINACIÓN SOCIAL DE LA DEMANDADA], a que abone a mi principal la cantidad de [IMPORTE EN LETRA] euros ([IMPORTE] €), por las mercancías servidas y que han resultado impagadas.

B) Se resuelva el contrato suscrito en fecha [FECHA] entre ambos litigantes.

C) Se indemnice a mi principal en la cantidad de [IMPORTE EN LETRA] euros ([IMPORTE] €) por los daños y perjuicios causados.

D) Se abonen a mi representada los intereses legales desde la interposición de la demanda.

Todo ello con imposición de las costas del juicio a la parte demandada.

Es justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Abogado/a Firma del Procurador/a

NOTA DE AYUDA

(1) Acreditación del poder: todos los poderes deben estar inscritos en el Registro Electrónico de Apoderamientos Judiciales (REAJ). Para su acreditación basta, en principio, la consulta automatizada orientada al dato de dicho Registro, que está a disposición de cualquier Letrado de la Administración de Justicia. Dado que el art. 24.2 LEC configura la certificación de la inscripción como vía subsidiaria, para el caso de que el sistema no permita aquella consulta, el modelo prevé que se acompañe certificación electrónica, que el sistema permite emitir a quien inscribe el poder.
