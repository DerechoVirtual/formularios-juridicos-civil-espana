---
name: escrito-demandado-opone-compensacion-relaciones-civ-0916
description: "Escrito del demandado que opone compensación por relaciones comerciales con el actor en verbal. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito del demandado que opone compensación por relaciones comerciales con el actor en verbal

> Formulario **CIV-0916** del plugin **Proceso civil: demandas, contestaciones, prueba y vista** (`formularios-proceso-civil`) · Civil › Escritos procesales (demanda, contestación, prueba, vista) · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito del demandado que opone compensación por relaciones comerciales con el actor en verbal» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito del demandado que opone compensación por relaciones comerciales con el actor en verbal” para mi caso». También puedes invocarla directamente con `/formularios-proceso-civil:escrito-demandado-opone-compensacion-relaciones-civ-0916`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-proceso-civil:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Proceso civil: demandas, contestaciones, prueba y vista) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (5 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] FECHA (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] DENOMINACIÓN SOCIAL
- [ ] DESCRIPCIÓN DEL BIEN
- [ ] LUGAR Y FECHA
- [ ] Nº DE DOCUMENTO
- [ ] Nº DE RECIBO
- [ ] SEDE

## Normas que cita el formulario

- art. 250.2 LEC
- art. 438.3 LEC
- art. 1195 Código Civil
- art. 1202 Código Civil
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

- Junto a «…Juicio verbal nº [NÚMERO] A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

Juicio verbal nº [NÚMERO]

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

Don [NOMBRE Y APELLIDOS] Procurador de los Tribunales, en nombre y representación de Don [NOMBRE Y APELLIDOS],según acredito mediante copia electrónica del poder notarial de representación digitalizada que acompaño, comparezco ante este Tribunal y como mejor proceda en derecho, y DIGO:

Que habiéndose dado traslado a esta parte de la demanda de juicio verbal formulada por D. [NOMBRE Y APELLIDOS] en reclamación de [IMPORTE] euros, siguiendo instrucciones de mi poderdante por medio del presente escrito y en nombre del mismo formulo en tiempo y forma CONTESTACIÓN A LA DEMANDA en la que opongo la existencia de crédito compensable, en virtud de los siguientes,

HECHOS

PRIMERO.- La acción que se ejercita en este proceso es una acción de reclamación de cantidad derivada de las relaciones comerciales que habitualmente mantienen el actor y el demandado, pretendiendo el demandante que mi representado le indemnice en la cantidad de [IMPORTE] euros

Esta parte admite, como expone la demanda que mi mandante efectuó el pedido que figura en el documento nº [Nº DE DOCUMENTO] cuyo importe no ha sido satisfecho. No obstante, entiende que existen razones que justifican el impago, las cuales seguidamente se expondrán.

SEGUNDO.- En una fecha anterior, mi mandante efectuó un pedido de [DESCRIPCIÓN DEL BIEN], tal como figura en la hoja de pedido nº [NÚMERO], habiendo recibido el género en la fecha que consta en el albarán de entrega. No obstante, el género recibido no se correspondía con el que figuraba en el pedido por lo que mi principal se puso en contacto con el suministrador y acordaron su devolución. Acompaño a dichos efectos doc. nº 1 del índice electrónico, que se corresponde con la hoja de pedido y doc. nº 2 del índice electrónico expedido por la empresa de mensajería [DENOMINACIÓN SOCIAL], en el cual consta la entrega del género devuelto y su recepción en la empresa del actor.

Pese a dicha devolución, en fecha [FECHA], el actor remitió a mi mandante la factura correspondiente, por lo que mi principal se puso en contacto con él, con el fin de que procediera a anular la factura pues se había devuelto el género, de común acuerdo con el vendedor. La parte actora, como no podía ser de otro modo, se avino a dicha reclamación y comunicó a mi mandante que la factura quedaría anulada. Acompaño copia de las comunicaciones habidas entre las partes por medio de fax, como doc. nº 3, 4 y 5 del índice electrónico.

TERCERO.- No obstante el actor, durante el mes de agosto, pasó de nuevo el recibo al cobro que fue satisfecho, por error, por la entidad bancaria de mi representado. Esta cantidad no ha sido devuelta ni compensada a mi principal a pesar de las múltiples gestiones realizadas. Adviértase que la cantidad indebidamente cobrada es inferior a la que ahora se reclama, según se desprende del doc. nº 5.

CUARTO.- En fecha [FECHA], mi representado efectuó nuevo pedido, que es el que figura en la hoja de pedido acompañado con la demanda y constituye el objeto del proceso iniciado por el demandante. Tan pronto recibió la factura observó que no constaba el abono previo, por lo que mi principal se puso, de nuevo, en contacto con el actor el cual manifestó que ya lo resolvería rectificando la factura y pasando al cobro el recibo por la diferencia.

Pese a ello, el actor ni rectificó la factura ni ajustó la cantidad en el recibo sino que pasó al cobro un recibo por la totalidad del importe que constaba en la hoja de pedido y factura antes dichas (doc. 2 y 3). Mi mandante ante esta evidente mala fe, remitió de nuevo un fax al actor y al no recibir respuesta ordenó a su entidad bancaria que devolviera el recibo impagado a su procedencia, comunicándole asimismo por fax, que mientras no rectificara la factura y el recibo correspondiente no procedería al pago de la suma adeudada, por entender que ésta era notablemente inferior a la reclamada. Acompaño el citado fax con su acuse de recibo como doc. nº 6.

FUNDAMENTOS DE DERECHO

PRIMERO.- COMPETENCIA Y PROCEDIMIENTO: Se acepta la competencia del Tribunal y la tramitación de la causa por los tramites del juicio verbal con fundamento en el art 250.2 LEC y asumiendo las alegaciones en este sentido vertidas en el escrito de demanda.

SEGUNDO.- EXISTENCIA DE CRÉDITO COMPENSABLE. El art. 438.3 de la LEC, determina los requisitos para que el demandado pueda oponer un crédito compensable. Como es de ver en los hechos arriba expuestos nos hallamos ante una acción de reclamación de cantidad, que se tramita como juicio verbal al amparo del art. 250.2 de la LEC, ya que no tiene asignada una tramitación especial.

En este caso, la cuantía del crédito es inferior a la cantidad reclamada pues mi mandante opone compensación parcial de la deuda reclamada, en la cantidad de [IMPORTE] euros, que resulta de la diferencia entre lo reclamado y la cantidad entregada previamente por error y que debe entenderse entregada a cuenta de la cantidad que en este proceso se reclama, al darse los requisitos del art. 1195 y siguientes del Código Civil, para que pueda operar la compensación parcial de la deuda. Exige el CC para que los créditos puedan ser compensables que cada uno de los obligados lo esté principalmente y, a su vez, sea acreedor principal del otro; que las deudas consistan en cantidad de dinero, estén vencidas, sean líquidas y exigibles y que sobre ninguna de ellas haya retención o contienda promovida por terceras personas y notificada oportunamente al deudor. Su efecto es extinguir una y otra deuda en la cantidad concurrente según el art. 1202 del Código Civil.

Como pone de relieve la STS de 30 de diciembre de 1999, rec. 223/1995, la compensación, ya sea legal o judicial, procede «cuando existe la posibilidad de un trasvase económico entre personas recíprocamente acreedoras y deudoras». Por su parte, la STS de 8 de marzo de 2000, rec. 1777/1995, nos dice que la compensación impide la reclamación del acreedor contra su deudor cuando aquél es, a su vez, deudor del segundo.

TERCERO.- COSTAS: Procede imponer las costas a la parte actora, conforme al art. 394 de la LEC, pues no sólo ha iniciado una acción a la que no tiene derecho, sino que además la pretensión ante los Tribunales era innecesaria, pues ya se ha acreditado que mi mandante se ofreció a pagar la deuda -inferior, por supuesto, a la que se reclama- tan pronto el actor cumpliera con sus obligaciones como comerciante: rectificar la factura, pues no hay que olvidar que los efectos de dicho documento trascienden de la esfera mercantil -ya que afectan al ámbito tributario- y pasase al cobro un recibo por la diferencia. La buena fe de mi principal es aún más evidente cuando, como se expone en el otrosí segundo de este escrito, ofrece una consignación por la cantidad que considera adeudar.

Por todo lo expuesto,

SUPLICO AL TRIBUNAL: Tenga por presentado este escrito con los documentos que se acompañan con justificante de traslado, se me tenga por comparecido en la representación que acredito de Don [NOMBRE Y APELLIDOS] en el juicio verbal referenciado al margen y por contestada a la demanda interpuesta contra mi principal y tras la pertinente tramitación se sirva dictar sentencia por la que se declare compensada la parte de la deuda por el abono del recibo [Nº DE RECIBO] en la cantidad de [IMPORTE] euros y se absuelva de la demanda a mi principal al haber satisfecho, junto a la consignación, la totalidad de la deuda reclamada ya que no ha habido mora del deudor sino del acreedor, con expresa condena en costas al demandante.

OTROSÍ PRIMERO DIGO: Como quiera que mi principal reconoce adeudar la suma de [IMPORTE] euros, y tiene la intención de efectuar una consignación por dicha cantidad, interesa que al tiempo de admitir este escrito se comunique el número de cuenta de consignaciones de este Tribunal, con el fin de que, una vez verificada, acuerde el mismo, en el momento procesal oportuno, ofrecer esta suma al actor y tenga por efectuado el completo pago de la cantidad reclamada.

OTROSÍ SEGUNDO DIGO: que esta parte interesa la celebración de vista al existir controversia sobre los hechos y ser necesaria la práctica de prueba para la resolución de este proceso.

En [LUGAR Y FECHA].

========================================================================
