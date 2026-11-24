---
name: demanda-juicio-ordinario-cobro-lo-indebido-civ-0765
description: "Demanda de juicio ordinario por cobro de lo indebido. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio ordinario por cobro de lo indebido

> Formulario **CIV-0765** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio ordinario por cobro de lo indebido» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio ordinario por cobro de lo indebido” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:demanda-juicio-ordinario-cobro-lo-indebido-civ-0765`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (18 veces)
- [ ] Nº DE DOCUMENTO (4 veces)
- [ ] AÑO (3 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] FECHA (2 veces)
- [ ] PORCENTAJE (2 veces)
- [ ] CALLE
- [ ] DÍA
- [ ] EXPONER LOS HECHOS
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] MES
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] Nº DE CLÁUSULA
- [ ] NÚMERO
- [ ] SEDE

## Normas que cita el formulario

- art. 10.1 LOPJ
- art. 1896 Código Civil
- art. 51.1 LEC
- art. 85.1 LOPJ
- art. 5 Ley Orgánica 1/2025
- art. 1895 Código Civil
- art. 394 LEC
- art. 251 LEC
- art. 7.2 Ley 10/2012

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE Q.P.T.R.C.»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…curador ========================================================================»: requisito de procedibilidad del art. 5 LO 1/2025 — antes de presentar la demanda hay que intentar un medio adecuado de solución de controversias (MASC) y acreditarlo con la demanda (arts. 264.4.º y 399.3 LEC), salvo las materias excluidas del art. 5.2. Fuente: LO 1/2025, arts. 5 a 7 (BOE-A-2025-76).

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE Q.P.T.R.C.

D./Dña. [NOMBRE Y APELLIDOS] Procurador/a de los Tribunales, actuando en representación de [NOMBRE DEL REPRESENTADO/A] según se acredita por certificación del registro electrónico de apoderamientos judiciales que acompaño (o mediante designación apud acta ante el/la Letrado/a de la Administración de Justicia de [SEDE]), y bajo la dirección letrada de D./Dña [NOMBRE Y APELLIDOS], Abogado/a del Colegio de [LOCALIDAD], ante el Tribunal comparezco y como mejor en derecho proceda formulo demanda de juicio ordinario en ejercicio de la acción de restitución por cobro de lo indebido contra la entidad [DENOMINACIÓN SOCIAL], con domicilio en en base a los siguientes

HECHOS

Se ejercita la acción en reclamación de la cantidad de [IMPORTE] euros que fueron percibidos indebidamente por la entidad demandada como consecuencia del pago del precio en el contrato de compraventa, según se expondrá seguidamente.

En fecha [FECHA], se otorgó ante el Notario Sr. D [NOMBRE Y APELLIDOS] escritura pública de compraventa, en virtud de la cual la entidad demandada [DENOMINACIÓN SOCIAL] vendió a mi representado el local ubicado en la planta baja de la edificación sita en la calle [CALLE], número [NÚMERO] por el precio de [IMPORTE] euros (se acompaña como documento número [Nº DE DOCUMENTO] copia auténtica de la citada escritura de compraventa).

Como es de ver en la cláusula [Nº DE CLÁUSULA] del citado contrato, se establecía un concreto calendario de pagos, que mi representado cumplió puntualmente: [IMPORTE] euros como señal y parte de pago en el momento de la firma; euros en el primer trimestre de [AÑO], y el resto, [IMPORTE] euros, en el segundo trimestre de [AÑO], pactándose un precio alzado de [IMPORTE] euros más [IMPORTE] euros en concepto de IVA.

Mi representado abonó las cantidades en los plazos convenidos según acredito por recibos de cobro acompañados como documentos [Nº DE DOCUMENTO]

De acuerdo con tales hechos, es claro que existe un cálculo erróneo en el IVA aplicable, puesto que se aplicó el tipo del [PORCENTAJE] %, en lugar del tipo del [PORCENTAJE] %, lo que supuso un cobro adicional de [IMPORTE] euros en concepto de IVA por parte de la vendedora, el cual no responde a causa justa, al carecer de una expresa disposición legal al respecto y asimismo por no concurrir negocio jurídico válido que lo autorice, pues el IVA debe aplicarse sobre el precio global pactado, que fue de [IMPORTE] euros, no pudiendo constituir un enriquecimiento injusto para la entidad demandante.

En consecuencia, el pago por mi representado de la cantidad de [IMPORTE] euros ahora reclamada, constituía un pago indebido, al carecer de causa justa, pues el importe del IVA real fue de [IMPORTE] euros, en lugar del de [IMPORTE] euros que constaba en el contrato.

(concurrencia de los presupuestos que determinan la procedencia de la acción) En este caso, concurren los presupuestos que determinan la procedencia del cobro de lo indebido cuando se recibe alguna cosa que no había derecho a cobrar y que por error ha sido indebidamente integrada, como expresa el artículo 1895 del Código civil, puesto que se realizó un pago en favor de la parte demandada que ésta no tenía derecho a cobrar, puesto que se hacía en concepto de una percepción tributaria indebida por referirse a un tipo no aplicable a la compraventa. Aunque la controversia deba resolverse aplicando normas tributarias, es competente el orden jurisdiccional civil, puesto que se trata de un conflicto entre particulares acerca del carácter indebido o no de un determinado pago, la cual, sin embargo, tiene como presupuesto la resolución de la cuestión de carácter administrativo-tributario, cual es la determinación del tipo aplicable de IVA, para lo cual ostenta competencia prejudicial el órgano al que me dirijo conforme a lo establecido en el artículo 10.1 de la LOPJ.

Además, no existe dificultad alguna en resolver prejudicialmente la cuestión administrativa planteada, toda vez que la Administración tributaria certifica el importe de IVA efectivamente abonado por esta transacción y el tipo aplicable a la liquidación, en la certificación que aporto como documento número

Por tanto, mi representado realizó un pago adicional de [IMPORTE] euros en concepto de IVA, que la entidad vendedora no tenía derecho a percibir, concurriendo, en consecuencia, los requisitos establecidos por la jurisprudencia (entre otras, SSTS de 1 de junio de 2005, 27 de octubre de 2005, 18 de noviembre de 2005, 6 de febrero de 2006, 15 de marzo de 2006 y 8 de enero de 2007) para que pueda prosperar la acción de repetición de lo indebido como son: 1) pago efectivo hecho con la intención de extinguir la deuda; y 2) error por parte del que hizo el pago o inexistencia de la obligación a que responde la atribución patrimonial solvendi causa [en pago]. La pretensión de restitución del enriquecimiento sin causa responde en este caso a la existencia de un aumento patrimonial definido como aquel que tiene su fundamento en una actividad o comportamiento realizado con la finalidad de ejecutar un plan jurídico obligatorio inexistente. Mi representado ha realizado un desplazamiento patrimonial para cumplimiento de una obligación negocial de subvenir mediante sustitución a una obligación tributaria, que resultó inexistente en la cuantía adicional de [IMPORTE] euros, lo que priva de causa al desplazamiento patrimonial y determina la necesidad de la restitución.

(Gestiones extrajudiciales y pretensión [EXPONER LOS HECHOS]) Ante lo patente del error, mi mandante se ha dirigido en numerosas ocasiones a la entidad demandada, quien ha hecho caso omiso reiteradamente. Finalmente, el pasado día [FECHA] mi representado dirigió a la entidad demandada escrito de reclamación extrajudicial por importe de [IMPORTE] euros, remitido por conducto notarial, sin que hasta el día de la fecha se haya dado respuesta alguna (acompaño como documento número [Nº DE DOCUMENTO] acta de reclamación notarial).

Ello nos obliga a interponer esta acción en vía judicial, debiendo tomarse en consideración la conducta omisiva de la entidad demandada, que pone de manifiesto su mala fe, en orden al devengo de intereses e imposición de costas, y debiendo indemnizarse a mi representado en la cantidad percibida indebidamente por la entidad demandada que asciende a [IMPORTE] euros, con más los intereses legales conforme a lo establecido en el artículo 1896 del Código Civil.

FUNDAMENTOS DE DERECHO

Jurisdicción y competencia

Corresponde la jurisdicción al orden civil, ostentando competencia prejudicial en el caso, según ha reiterado el TS en Sentencias de 27 de septiembre de 2000, rec. 2908/1995 y 29 de junio de 2006, rec. 3762/1999, siendo objetiva y territorialmente el Tribunal al que me dirijo, con fundamento en el artículo 51.1 de la LEC, en relación con lo dispuesto en el art. 85.1º LOPJ.

Legitimación

Le corresponde a esta parte la legitimación activa al haber realizado el pago indebido, correspondiendo la legitimación pasiva a la entidad demandada, quien se ha enriquecido sin causa con el cobro de lo indebido.

Procedimiento

Es el juicio ordinario con fundamento en el art. 249,2 dado el importe reclamado de [IMPORTE] euros que excede de los 15.000 € a partir de los que se deben seguir las reclamaciones por las normas del juicio ordinario.

Cumplimiento de los requisitos de procedibilidad

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

Requisitos de la acción de cobro de lo indebido

Es de aplicación el artículo 1895 del Código Civil que dispone que "cuando se recibe alguna cosa que no había derecho a cobrar, y que por error ha sido indebidamente entregada, surge la obligación de restituirla", habiendo interpretado, entre otras, la STS de 6 de marzo de 2007, rec. 706/2000 que pueda prosperar la acción de repetición de lo indebido es necesario que exista un pago efectivo hecho con la intención de extinguir la deuda; y error por parte del que hizo el pago o inexistencia de la obligación a que responde la atribución patrimonial en pago, circunstancias que concurren en el presente caso.

Intereses

Es de aplicación el artículo 1896 del Código Civil que establece que el que acepta un pago indebido, si hubiera procedido de mala fe, deberá abonar el interés legal cuando se trate de capitales, o los frutos percibidos o debidos percibir cuando la cosa recibida los produjere.

En materia de costas el artículo 394 LEC señala que las de primera instancia se imponen a la parte que vea en primera instancia rechazadas sus pretensiones.

En base a lo anterior,

SUPLICO AL TRIBUNAL que tenga por presentada la presente demanda con los documentos a ella adjuntos y sus copias, y tras la pertinente tramitación, se dicte por ese Tribunal sentencia en que se condene a la entidad demandada a indemnizar a mi representado en la cantidad de [IMPORTE] euros, con más el interés legal desde la fecha del cobro indebido, con imposición de costas a la demandada.

OTROSÍ PRIMERO DIGO.- Se fija la cuantía de este procedimiento en [IMPORTE] euros, de conformidad a lo que dispone el artículo 251, regla 12ª, de la LEC.

OTROSÍ SEGUNDO DIGO.-Que estando la presente demanda sujeta al abono de la tasa por el ejercicio de la potestad jurisdiccional fijada por la Ley 10/2012, de 20 de noviembre, modificada por RDL 3/2013 y Ley 25/2015, de 28 julio, y desarrollada por Orden HAP/2662/2012, de 13 de diciembre, siendo mi representada personas jurídica no exenta de su pago, se acompaña a la presente demanda como documento nº [Nº DE DOCUMENTO] la correspondiente autoliquidación con el ejemplar para la Administración de Justicia debidamente validado y en el que consta el pago de la cantidad de 300 euros correspondiente a la cuota fija, sin que se incluya la cuota variable prevista en el artículo 7.2 de la Ley 10/2012 al haber sido declarado inconstitucional y nulo por la STC 140/2016, de 21 de julio.

En virtud de lo anterior,

SUPLICO AL TRIBUNAL se tenga por efectuada la anterior manifestación a los efectos pertinentes y por acompañado el documento justificativo del abono de la tasque tenga por hecha la anterior manifestación a los efectos pertinentes y por acompañado el documento justificativo del abono de la tasa.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma Abogado	Firma Procurador

========================================================================
