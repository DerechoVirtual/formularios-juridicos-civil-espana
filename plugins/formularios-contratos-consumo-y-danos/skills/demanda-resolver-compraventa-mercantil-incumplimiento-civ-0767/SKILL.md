---
name: demanda-resolver-compraventa-mercantil-incumplimiento-civ-0767
description: "Demanda para resolver una compraventa mercantil por incumplimiento del vendedor y reclamar cantidad. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda para resolver una compraventa mercantil por incumplimiento del vendedor y reclamar cantidad

> Formulario **CIV-0767** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio ordinario sobre resolución de contrato de compraventa mercantil por incumplimiento del vendedor y reclamación de cantidad

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda para resolver una compraventa mercantil por incumplimiento del vendedor y reclamar cantidad» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda para resolver una compraventa mercantil por incumplimiento del vendedor y reclamar cantidad” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:demanda-resolver-compraventa-mercantil-incumplimiento-civ-0767`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (19 veces)
- [ ] FECHA (13 veces)
- [ ] Nº (11 veces)
- [ ] LOCALIDAD (7 veces)
- [ ] Nº DE DOCUMENTO (7 veces)
- [ ] ACCIÓN EJERCITADA (3 veces)
- [ ] FECHAS (3 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] CALLE
- [ ] CORREO ELECTRÓNICO
- [ ] HOJA
- [ ] LUGAR
- [ ] Nº DE COLEGIADO/A
- [ ] Nº DE PROCEDIMIENTO
- [ ] NÚMERO
- [ ] PARTE DEMANDADA
- [ ] TELÉFONO
- [ ] TOMO
- [ ] ÓRGANO

## Normas que cita el formulario

- art. 24.1 LEC
- art. 399.1 LEC
- art. 45 LEC
- art. 1.1 LSC
- art. 251.1 LEC
- art. 249.2 LEC
- art. 23 LEC
- art. 5 Ley Orgánica 1/2025
- art. 1124 CC
- art. 1.124 CC
- art. 1124 Código Civil
- art. 1106 CC
- art. 1100 CC
- art. 63.2 CC
- art. 394 LEC
- art. 231 LEC

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE QUE POR TURNO CORRESPONDA»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE QUE POR TURNO CORRESPONDA

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales y de la entidad mercantil [DENOMINACIÓN SOCIAL], con domicilio social en [LOCALIDAD], representación que acredito mediante escritura de poder otorgada a mi favor (existen tres posibilidades para otorgar el apoderamiento al Procurador de los Tribunales, conforme dispone el art. 24.1 LEC)

[OPCIONAL — opción en función de cómo se haya otorgado el poder]

[ELEGIR UNA OPCIÓN: Si el poder se otorga a través de la sede judicial electrónica / Si el poder se otorga mediante comparecencia apud acta / Si el poder se otorga ante Notario]

bajo la dirección letrada de D./Dña [NOMBRE Y APELLIDOS], abogado/a en ejercicio, con despacho profesional abierto en [LOCALIDAD], colegiado nº [Nº DE COLEGIADO/A] del Ilustre Colegio de la Abogacía de [LOCALIDAD], ante el Tribunal comparezco y como mejor en Derecho proceda, DIGO:

Que, siguiendo instrucciones de mi mandante, vengo a interponer demanda DE JUICIO [Nº DE PROCEDIMIENTO], en ejercicio de la acción [ACCIÓN EJERCITADA], contra D./Dña [NOMBRE Y APELLIDOS], con domicilio, primero en [DOMICILIO]; y segundo, el domicilio laboral en [DOMICILIO]); con email [CORREO ELECTRÓNICO]; y con número de teléfono móvil [TELÉFONO]; en ejercicio de la acción de [ACCIÓN EJERCITADA], según se especificará en el cuerpo del escrito y en el suplico, y todo ello de conformidad con los siguientes hechos y fundamentos de derecho.

Que esta parte asume el compromiso de recibir cualquier comunicación dirigida por la oficina judicial, durante toda la fase declarativa, e, incluso, en una eventual fase de ejecución por medios telemáticos, en términos del art. 399.1 II LEC, consignándose a estos efectos la siguiente dirección de correo electrónico y nº [Nº] de teléfono:

Se ejercita en la presente demanda la acción de [ACCIÓN EJERCITADA]

Fundamento la misma en los siguientes hechos y consideraciones jurídicas:

HECHOS

PRIMERO.- Mi mandante es una entidad dedicada a la fabricación de todo tipo de utensilios de cocina, con domicilio social en su mismo centro de trabajo, sito en [LOCALIDAD]. Se encuentra inscrita en el Registro Mercantil de [LOCALIDAD], hoja [HOJA], tomo [TOMO] y está al corriente en el pago de sus obligaciones fiscales, como se acredita mediante [ÓRGANO] que se acompaña como documento n.º [Nº DE DOCUMENTO].

La demandada es una mercantil dedicada a la fabricación de todo tipo de contenedores para uso industrial, con domicilio social en el número [NÚMERO] de la calle [CALLE] de la localidad de [LOCALIDAD], tal y como consta en la certificación del Registro Mercantil unida a la demanda en su documento n.º [Nº DE DOCUMENTO].

SEGUNDO.- En fecha [FECHA], siguiendo las instrucciones indicadas en la página web de la demandada (cuya impresión se adjunta como documento n.º [Nº DE DOCUMENTO]), y previa consulta por correo electrónico y respuesta positiva al respecto, operadas ambas el mismo día; se realizó un pedido del contenedor HGF-9000 ofrecido en la propia web. Se aporta, como bloque documental n.º [Nº] el pedido en cuestión y los correos cruzados del mismo día.

TERCERO.- El contenedor en cuestión, se ajustaba a las necesidades productivas de mi mandante, tenía un precio de [IMPORTE] euros, de los cuales [IMPORTE] euros debían abonarse en los [Nº] días posteriores a hacer el pedido, y el resto a la entrega del producto, que se produciría en un plazo máximo de [Nº] meses, según se indicaba en la propia web. El pago a cuenta indicado se realizó el día [FECHA], mediante transferencia bancaria de la cual se acompaña justificante como documento n.º [Nº DE DOCUMENTO].

CUARTO.- En fecha [FECHA] se hizo un segundo pedido de otro contenedor, en esta ocasión el HGF-8500, de menor tamaño, por precio de [IMPORTE] euros, con el mismo sistema de pago con adelanto de [IMPORTE] euros. Se adjuntan pedido y correos de confirmación en bloque documental n.º [Nº], y justificante de transferencia bancaria realizada el [FECHA] como documento n.º [Nº DE DOCUMENTO].

QUINTO.- A día de hoy los contenedores no han sido entregados, sin mayor explicación, a pesar de los diversos contactos telefónicos mantenidos; razón por la que se envió burofax en fecha [FECHA] a la demandada comunicando la intención de resolver los dos contratos de venta y la devolución de los [IMPORTE] euros adelantados, sin haber obtenido tampoco respuesta alguna.

SEXTO.- Ante tal situación, mi mandante, se ha visto obligada a presentar esta demanda con objeto de resolver el contrato por incumplimiento contractual de la vendedora, reclamar la cantidad que se ha adelantado como precio a cuenta, así como los daños y perjuicios que se le han ocasionado. En este sentido, ante la necesidad de disponer de ambos contenedores, se han adquirido a una tercera entidad, dos unidades básicas, menos adecuadas a las necesidades de mi mandante, por un precio total de [IMPORTE] euros, a razón de [IMPORTE] euros cada uno de ellos. Se aportan copias de las facturas abonadas y transferencias bancarias como bloque documental n.º [Nº]. Se reclama, por ello, el sobreprecio abonado, [IMPORTE] euros, frente a los [IMPORTE] euros pactados con la demandada; sin perjuicio de que la utilidad de los dos contenedores adquiridos es inferior a la que debían prestar los inicialmente contratados.

SÉPTIMO.- La parte actora manifiesta que, previo a la presentación de la presente demanda, se han llevado a cabo negociaciones con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad, y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria; incluyéndose entre las acciones realizadas el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución.

Finalmente, mi representado envió un requerimiento fehaciente al demandado con fecha [FECHA], fijando un plazo de 30 días naturales para llegar a un acuerdo amistoso, a través del abogado que firma este escrito, el cual fue contestado por el demandado por el mismo medio, rechazando el acuerdo/ habiendo sido solo posible un acuerdo parcial, viéndonos en la necesidad de acudir a la presente vía judicial, respecto a los extremos de la controversia en los que se mantiene la discrepancia.

Acompaño como documento nº [Nº DE DOCUMENTO], el requerimiento efectuado y como documento nº [Nº DE DOCUMENTO], la contestación del demandado.

A los anteriores hechos, son aplicables los siguientes:

FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN Y COMPETENCIA

Es competente el Tribunal de Instancia del domicilio del demandado, por aplicación de lo dispuesto en los arts. 45 y 51 LEC A tal efecto, el domicilio social de la entidad demandada se encuentra en la localidad de [LOCALIDAD], dentro del partido judicial del órgano al que tengo el honor de dirigirme.

II.- CAPACIDAD

Al tratarse de sociedades de responsabilidad limitada inscritas en el Registro Mercantil, y de conformidad con los arts. 1.1 y 33 LSC 1/2010, ambas tienen personalidad jurídica, y consiguientemente capacidad para ser parte y capacidad para comparecer en juicio.

III.- LEGITIMACIÓN

Corresponde al demandante la activa por ser parte en el contrato suscrito y haber cumplido sus obligaciones contractuales como comprador, consistentes en pagar los anticipos pactados; y la pasiva la tiene la demandada en cuanto ocupa la posición vendedora y no ha entregado los contenedores encargados.

IV.- CUANTÍA

Conforme a los arts. 251.1 y 253 LEC cifro la cuantía de la presente demanda en [IMPORTE] euros ( euros de adelanto y [IMPORTE] euros por daños y perjuicios), que es el importe de la cantidad que se reclama.

V.- PROCEDIMIENTO

El procedimiento ajustado a derecho será el del juicio declarativo ordinario regulado en los arts. 399 a 436 de la misma Ley, atendiendo a la cantidad reclamada de [IMPORTE] euros, en aplicación de lo dispuesto en el art. 249.2 LEC.

VI.- POSTULACIÓN Y DEFENSA

Conforme a lo previsto en los arts. 23 y 31 LEC, se presenta la demanda por medio de Procurador/a legalmente habilitado y bajo dirección de Letrado firmante de la misma.

VII.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

VIII.- FONDO DE LA CUESTIÓN CONTROVERTIDA

A) Acciones que se ejercitan

En esta demanda se acumulan diversas acciones, al amparo de lo dispuesto en los arts. 71 y ss. LEC, en cuanto tienen su origen en el mismo incumplimiento contractual, se dirigen contra el mismo demandado y no son incompatibles.

Las acciones que se ejercitan son las siguientes: a) principalmente la acción de resolución contractual de las dos compraventas de fechas [FECHA] y [FECHA], en virtud de lo previsto en el art. 1124 CCiv, por incumplimiento contractual imputable a la entidad demandada; y derivada de ella b) acción de reclamación de cantidad al amparo de las disposiciones generales sobre contratación y compraventa mercantil, arts. 1089 y ss. CCiv y arts. 325 y ss. Ccom, reclamando las cantidades adelantadas y la correspondiente indemnización por los daños y perjuicios causados.

B) Resolución de los contratos de compraventa por incumplimiento de la parte demandada:

En la doble compraventa que nos ocupa, se ha producido un claro incumplimiento contractual por parte de la mercantil [DENOMINACIÓN SOCIAL] como parte vendedora, quien tras recibir el adelanto pactado, no ha entregado ninguno de los dos contenedores vendidos dentro del plazo de máximo consensuado, habiendo finalizado los periodos comprometidos de [Nº] meses los días [FECHAS] y [FECHA], respectivamente.

A día de hoy, transcurridos otros [Nº] meses en la primera venta, y casi [Nº] meses más en la segunda; a pesar de varios requerimientos telefónicos, y de la reclamación escrita, no se han entregado aquellos, ni existe ninguna previsión de que se entreguen; por lo que mi mandante se ha visto obligado a recurrir a otro vendedor y adquirir otros contenedores no tan adecuados, como los encargados, para las necesidades productivas previstas. Incumplimiento que contrasta con el cumplimiento de las prestaciones a las que se obligó mi principal, como compradora, esto es, el pago en el plazo de [Nº] días desde pedido de los dos adelantos pactados por importes de [IMPORTE] euros y [IMPORTE] euros respectivamente.

De esta forma, nos situamos en el escenario del art. 1.124 CCiv, que establece que la facultad de resolver las obligaciones se entiende implícita en las recíprocas para el caso de que uno de los obligados no cumpliere lo que le incumbe. El perjudicado podrá escoger entre exigir el cumplimiento o la resolución de la obligación, con el resarcimiento de los daños y abono de intereses en ambos casos.

En el presente caso, mi mandante opta por la resolución del contrato y acude a la vía judicial para su declaración, habida cuenta de la falta de respuesta, siquiera, a la posibilidad de una resolución consensuada entre las partes. Al respecto, la Sentencia del Tribunal Supremo de fechas 3 de marzo de 2.005 o la Sentencia del Tribunal Supremo, Sala Primera, de lo Civil, 864/2007 de 17 Jul. 2007, Rec. 2770/2000, las cuales señalan que cuando la declaración de resolución efectuada por una de las partes se impugna por la otra (o, como ocurren en el supuesto que nos ocupa, no se contesta, ignorándose), queda sometida al examen y sanción de los Tribunales, que habrán de declarar, en definitiva, bien hecha la resolución o, por el contrario, no ajustada a derecho, recogiendo la doctrina jurisprudencial contenida en Sentencias de 24-10-41, 28-1-43, 7-1-48 y 19-3-49.

Procediendo, de esta forma, el acceso a la vía judicial, el incumplimiento puesto de manifiesto frustra de manera absoluta el fin del contrato, consistente en que mi mandante tuviera a su disposición en un plazo razonable y dentro de los primeros [Nº] meses pactados, los contenedores deseados, en el marco de la concreta necesidad productiva que le llevó a comprar los mismos. Sobre la cuestión, la sentencia del Tribunal Supremo de fecha 23 de mayo de 2.003, rec. 3167/1997, la cual indica que "Existe por ello un propio y verdadero incumplimiento, en cuanto impide el fin normal del contrato, frustrando las legítimas expectativas de la parte, como señalan las sentencias de esta Sala de 27 de octubre de 1981, 11 de octubre de 1982 y 7 de marzo de 1983, aunque para la aplicación del art. 1124 del Código Civil no se exige ni requiere una tenaz y persistente resistencia obstativa al cumplimiento, bastando tan sólo con frustrar las legítimas aspiraciones de la contraparte -sentencia de 31 de mayo y 13 de noviembre de 1985- y determina la resolución la entrega de cosa inservible, con independencia de que la venta sea civil o mercantil -sentencias de 29 de febrero de 1988, 24 de mayo y 30 de septiembre de 1989, 29 de abril, 10 de noviembre de 1994 y 1 de diciembre de 1997".

En esta misma línea, la sentencia del Tribunal Supremo de fecha 13 de febrero de 2.009, rec. 1416/2004, al afirmar que "la jurisprudencia, a la hora de interpretar y aplicar el artículo 1124 del Código Civil, ha abandonado hace tiempo las posiciones que, de una u otra forma, exigían una reiterada y demostrada voluntad rebelde en el incumplimiento de las obligaciones contractuales, para atender al dato objetivo de la injustificada falta de cumplimiento, siempre que tenga la entidad suficiente para motivar la frustración del fin del contrato -Sentencias de 7 de mayo de 2003 y 18 de octubre de 2004 entre otras".

En consecuencia, se trata de un incumplimiento sustancial imputable únicamente a la parte demandada, que habilita la resolución contractual peticionada, de conformidad con la doctrina expuesta, a sensu contrario, en Sentencia del Tribunal Supremo, Sala Primera, 116/2010, de 4 Marzo 2010, rec.1982/2005, "como dijo la sentencia de 20 de diciembre de 1993 el incumplimiento que procede de ambas partes es situación que es resuelta por la doctrina de esta Sala en el sentido de que tratándose de negocios jurídicos sinalagmáticos, como es el de compraventa, el incumplimiento recíproco impide que pueda constituirse en causa de resolución vid., SS. 16-11-1979 y las muy numerosas en ella citadas, 23-1-1986, 16-4-1991, y las que en ella se indican, 16-5-1991"

C) Devolución de los anticipos e indemnización de daños y perjuicios:

La expresión que contiene el art. 1124 CCiv ("resarcimiento de daños y abono de perjuicios) es equivalente de indemnización de daños y perjuicios comprendiéndose tanto el daño emergente como el lucro cesante. Citamos en este sentido los arts. 1106 y 1107 CCiv.

De esta forma, procede devolver las cantidades adelantadas por importe global de [IMPORTE] euros ( euros abonados a cuenta en el primer contrato y [IMPORTE] euros abonados a cuenta en el segundo); así como el perjuicio derivado del mayor costo, euros, que supuso para mi mandante el acudir a un tercero, para adquirir unos contenedores menos adecuados que los previstos, sin perjuicio de que aquellos, se hayan entregado efectivamente a diferencia de éstos. Todo ello, hace que se reclame el principal de [IMPORTE] euros, a lo que habrá de añadirse, de conformidad con los arts. 1100, 1101, 1108, 1109 CCiv, y art. 63.2 CCom, los intereses moratorios a partir de la interpelación extrajudicial operada en fecha [FECHA]. Se trata, conforme a lo dispuesto en sentencia del Tribunal Supremo de 24 de febrero de 1.993 de "devolver las cantidades recibidas más sus intereses legales y abonar también a la actora los pagos e impuestos satisfechos por cuenta de los mismos, o sea, que se reintegra a las partes a la situación patrimonial anterior a la celebración del contrato y se computan los «gastos» útiles, lo cual es, en definitiva, una solución correcta".

IX.- COSTAS

Conforme al art. 394 LEC, las costas han de imponerse a la demandada.

Por lo expuesto,

SUPLICO AL TRIBUNAL.

Que habiendo por presentado este escrito de demanda con los documentos que lo acompañan y copias de uno y otros, los admita y me tenga por comparecido en parte en la representación que ostento y que acreditada dejo; y por promovido juicio declarativo ordinario frente a [PARTE DEMANDADA] acuerde dar traslado al demandado para que comparezca y la conteste, y previo los trámites legales y recibimiento a prueba que desde ahora se interesa se dicte en su día sentencia por la que estimando la demanda:

A) Se resuelvan los contratos de compraventa suscritos en fechas [FECHAS] y [FECHA] entre ambos litigantes.
B) Se condene a la entidad demandada, a que abone a mi mandante, la cantidad de [IMPORTE] euros ( €), por los pagos a cuenta realizado.
C) Se indemnicé a mi mandante en la cantidad de [IMPORTE] euros ( €) por los daños y perjuicios causados.
D) Se abonen a mi representado los intereses legales desde la reclamación extrajudicial operada el día [FECHA].

Todo ello con imposición de las costas del juicio a la parte demandada.

Es de Justicia que pido en [LUGAR], a [FECHA].

OTROSÍ DIGO.- Que esta parte ha intentado cumplir con todos los requisitos formales exigidos en la vigente LEC, manifestando su voluntad de subsanar cualquier defecto procesal en el que haya incurrido, a los efectos determinados en el art. 231 LEC.

DE NUEVO SUPLICO AL TRIBUNAL: Que se sirva tener por hecha la precedente manifestación de intenciones

En igual lugar y fecha

Firma del Abogado/a	Firma del Procurador/a
