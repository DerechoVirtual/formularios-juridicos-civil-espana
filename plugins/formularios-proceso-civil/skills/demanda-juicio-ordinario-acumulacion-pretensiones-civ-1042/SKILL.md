---
name: demanda-juicio-ordinario-acumulacion-pretensiones-civ-1042
description: "Demanda de juicio ordinario con acumulación de pretensiones incompatibles. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio ordinario con acumulación de pretensiones incompatibles

> Formulario **CIV-1042** del plugin **Proceso civil: demandas, contestaciones, prueba y vista** (`formularios-proceso-civil`) · Civil › Escritos procesales (demanda, contestación, prueba, vista) · normativa revisada el 24-11-2026.

## Qué es

Modelo de demanda de juicio ordinario en la que se acumulan acciones incompatibles, tales como cumplimiento por pago y resolución contractual con resarcimiento.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio ordinario con acumulación de pretensiones incompatibles» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio ordinario con acumulación de pretensiones incompatibles” para mi caso». También puedes invocarla directamente con `/formularios-proceso-civil:demanda-juicio-ordinario-acumulacion-pretensiones-civ-1042`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-proceso-civil:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Proceso civil: demandas, contestaciones, prueba y vista) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (14 veces)
- [ ] FECHA (7 veces)
- [ ] NÚMERO (7 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] CALLE (3 veces)
- [ ] IMPORTE EN LETRA (3 veces)
- [ ] MES (3 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] Nº (2 veces)
- [ ] AÑO
- [ ] COLEGIO
- [ ] DENOMINACIÓN SOCIAL
- [ ] ENTIDAD BANCARIA
- [ ] LUGAR
- [ ] NIF
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] Nº DE DOCUMENTO
- [ ] PORCENTAJE
- [ ] SEDE

## Normas que cita el formulario

- art. 330 LEC
- art. 54.2 LEC
- art. 52.2 LEC
- art. 10 LEC
- art. 23 LEC
- art. 249.2 LEC
- art. 251 LEC
- art. 252.2.ª LEC
- art. 5 Ley Orgánica 1/2025
- art. 73 LEC
- art. 1.255 CC
- art. 1.100 CC
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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Notas al pie del formulario original:
(1) Véase el Auto tras la audiencia previa, que declara la improcedencia de una pretensión acumulada y dispone la reanudación del procedimiento en cuanto a la otra

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, que actúa en nombre y representación de [NOMBRE DEL REPRESENTADO/A], CIF n.º [NIF], con domicilio social en [LOCALIDAD], calle [CALLE], n.º [NÚMERO], a cuya justificación aporto escritura de poder inscrito en el Registro Electrónico de Apoderamientos Judiciales con el nº [NÚMERO] y que se puede acreditar mediante consulta automatizada orientada al dato, por parte del órgano judicial al cual tengo el honor de dirigirme, acompañándose certificación electrónica del Registro Electrónico de Apoderamientos Judiciales como Documento nº [Nº DE DOCUMENTO] por si no es posible la consulta automatizada; ante el Tribunal y bajo la dirección letrada de D./Dña. [NOMBRE Y APELLIDOS], colegiada n.° [NÚMERO] del Ilustre Colegio de Abogados de [COLEGIO], comparezco y como mejor proceda, DIGO:

Que a medio del presente escrito formulo demanda de JUICIO ORDINARIO contra la COMUNIDAD DE PROPIETARIOS DE LA CASA N.º [NÚMERO] DE LA CALLE [CALLE] DE [LOCALIDAD], en base a los siguientes

HECHOS

PRIMERO

Con fecha [FECHA] la ahora demandada suscribió contrato de mantenimiento de los ascensores comunitarios con la entidad [DENOMINACIÓN SOCIAL], tal y como consta en el referido contrato que al presente se acompaña distinguido como documento n.º [NÚMERO].

SEGUNDO

La relación se mantuvo girando mi mandante los recibos correspondientes a las mensualidades del contrato de mantenimiento, la suma de [IMPORTE] xx [IMPORTE] euros ( [IMPORTE] euros), por cada uno de los dos ascensores que tiene, en concepto de mantenimiento o conservación, tal y como se pactó, y prestándose el servicio sin problemas.

Así se demostrará con la solicitud de la correspondiente información a la CAJA DE AHORROS [ENTIDAD BANCARIA], entidad financiera a través de la cual se abonaban por la comunidad los recibos por el mantenimiento, que se instrumentará como requerimiento de documental a tercero (art. 330 LEC), y con la aportación de las facturas giradas como consecuencia de arreglos realizados, tal y como puede apreciarse en los documentos, que a modo de ejemplo, se adjuntan distinguidos con los números [Nº] al [Nº], acompañadas de los correspondientes partes de asistencia firmados también por el cliente.

TERCERO

Desde el mes de [MES] de [AÑO], la Comunidad demandada dejó de abonar los recibos correspondientes al precio del contrato, y con fecha [FECHA], se remite una carta por parte de dicha demandada, en la que se notifica la resolución del contrato, tal y como consta en el original acompañado al presente como documento n.° [NÚMERO].

Como hemos expuesto precedentemente el contrato concertado lo fue para una duración de cinco años y renovable tácitamente por igual periodo de tiempo, hasta que cualquiera de las partes decidiera resolverlo, comunicándolo a la otra parte con una antelación mínima de 90 días, al vencimiento de cada periodo.

De esta forma, habiéndose prorrogado el referido contrato, resulta que el vencimiento correspondiente lo sería el [FECHA], con lo que se produce una resolución incorrecta de acuerdo con lo pactado.

CUARTO

Los beneficios que se dejan de obtener hasta la finalización contractual pactada es el porcentaje de las cuotas hasta fecha [FECHA], que corresponde a los medios suficientes que mi mandante ha debido tener dispuestos para poder proceder en todo momento a prestar el adecuado servicio al cliente, y ello le supone un desembolso que queda en descubierto desde el momento en que, de forma unilateral y sin fundamento alguno, procede la demandada a la resolución contractual en contra de lo estipulado.

Lucro cesante que se cifra en [IMPORTE] euros ( [IMPORTE] €), lo que supone el 50% de la cantidad a abonar hasta la finalización del contrato.

QUINTO

Mi representada dedujo papeleta de conciliación, a los efectos de cumplir el requisito de procedibilidad para la iniciación de la vía jurisdiccional, reclamando a la Comunidad demandada las cuotas impagadas desde [FECHA] hasta la fecha, y la indemnización calculada, dándose lugar el [FECHA] al acto sin avenencia ante el Juez de Paz de [LOCALIDAD], cuyo testimonio se adjunta como documento n.º 7.

La ausencia de voluntad de un arreglo amistoso, ha forzado este recurso a la tutela judicial.

A los precedentes hechos son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

I.- COMPETENCIA

No siendo válida la sumisión expresa contenida en el contrato suscrito por las partes, en virtud de lo que preceptúa el art. 54.2 LEC, y ya era jurisprudencia estable la irrenunciabilidad del fuero propio de los usuarios en contratos de consumo, resulta competente el Tribunal al que me dirijo por ser el del domicilio del prestatario, entidad sin personalidad jurídica, al tratarse de un contrato de prestación de servicios y por aplicación de lo dispuesto en el art. 52.2 LEC.

II.- LEGITIMACIÓN

Dispone el art. 10 LEC que serán consideradas partes legitimas quienes comparezcan y actúen en juicio como titulares de la relación jurídica u objeto litigioso, supuesto de legitimación ordinaria directa en las relaciones jurídicas, que es el del asunto.

La legitimación activa corresponde en el presente caso a mí mandante como titular del derecho de crédito derivado de un contrato bilateral que se pretende hacer valer, acreedora de las cantidades reclamadas, y la pasiva a la Comunidad de Propietarios demandada, como deudora de dicha suma en virtud de la relación contractual existente.

III.- REPRESENTACION PROCESAL Y DEFENSA TÉCNICA

Resulta preceptiva la intervención del suscrito Procurador/a en virtud de lo dispuesto en el art. 23 LEC, e igualmente es preceptiva la intervención de letrado, según dispone el art. 31 del mismo cuerpo legal, ninguno de los dos preceptos que prevea salvedad para un declarativo como el promovido.

IV.- PROCEDIMIENTO

Deberán seguirse los trámites previstos para el juicio ordinario, por ser la cuantía del presente proceso superior a 15.000 euros, según dispone el art. 249.2 LEC, y no llevar asignado cauce procesal por materia las pretensiones.

V.- CUANTÍA

La cuantía de la demanda a los efectos de lo dispuesto en los arts. 253 y ss. LEC, es la de [IMPORTE] euros ( [IMPORTE] €) en aplicación de la regla 1.ª del art. 251 LEC, según el cual, si se reclama una cantidad de dinero determinada, la cuantía de la demanda estará representada por dicha cantidad, en relación con el art. 252.2.ª LEC, que fija tal cantidad en la suma de las de las varias acciones acumuladas derivadas del mismo título.

VI.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

VII.- FONDO DE LA CUESTIÓN

Se plantea la presente acción en reclamación de los daños y perjuicios que la resolución unilateral del contrato de asistencia y mantenimiento referido produce para mi mandante, y la de pago de las prestaciones periódicas del mismo desde el mes [MES] hasta la fecha.

Dispone el art. 73 LEC que se admitirá por motivos procesales la acumulación de acciones siempre que el tribunal que deba entender de la acción principal posea jurisdicción y competencia por razón de la materia o por razón de la cuantía para conocer de la acumulada o acumuladas.

La indemnización que se reclama lo son como consecuencia de incumplimiento contractual por parte de la Comunidad demandada, que injustificadamente -es decir, sin incumplimiento de contrario- procedió a la resolución del contrato suscrito entre las partes antes del advenimiento del plazo establecido.

El contrato en cuestión se suscribió para una duración de 5 años, prorrogables por periodos iguales si cualquiera de las partes no comunicaba su decisión de resolverlo al menos con 90 días de antelación a su vencimiento.

No siendo este el supuesto, se produce un incumplimiento contractual que conlleva la aplicación del abono de la cantidad necesaria para satisfacer los daños y perjuicios que a la contratante actora produce esta resolución de carácter unilateral, que se traduce en el abono del 50% de los ingresos que la misma hubiese tenido de haber continuado el contrato vigente hasta su finalización, lo que asciende a [IMPORTE EN LETRA] yy [IMPORTE] euros.

Por otro lado, desde que se produjo el impago de la Comunidad el mes [MES] hasta la presentación de la demanda se ha devengado la cantidad de [IMPORTE] xx [IMPORTE] euros, que igualmente se reclaman.

El contrato se pactó libremente en virtud de lo dispuesto en el art. 1.255 CCiv, que consagra el principio de autonomía de la voluntad, no pudiéndose aducir de contrarío que la causa de -su incumplimiento se basa en que se trate de un contrato en el que las cláusulas estaban previamente establecidas, en ser un contrato tipo o de adhesión.

Corresponden intereses moratorios pacticios al tipo [PORCENTAJE] % anual desde el quinto día de cada mensualidad incorriente hasta la fecha de dictado de la presente, dado que el término es esencial, y corresponde una ‘mora solvendi’ constituida retroactiva o automáticamente ex art. 1.100 CCiv.

VIII.- COSTAS

Se impondrán las costas a la parte demandada, cuya eventual oposición será rechazada, en virtud de lo dispuesto en el art. 394 LEC, puesto que no es razonable que se repute que el caso presenta serias dudas de hechos o de derecho.

En su virtud,

SUPLICO AL TRIBUNAL

que, por presentado este escrito, con los documentos que lo acompañan y sus preceptivas copias, se sirva admitirlos, tenerme por parte en condición de demandante, por formulada demanda de Juicio Ordinario en reclamación de cantidad, y seguido que sea el procedimiento por sus regulares trámites, se dicte sentencia por la que, estimando la presente demanda, se declare la improcedencia de la resolución contractual llevada a cabo a la demandada, y consecuentemente el incumplimiento contractual por su parte, y se condene a la demandada COMUNIDAD DE PROPIETARIOS DE LA CASA N.° [NÚMERO] DE LA CALLE [CALLE] DE [LOCALIDAD] al abono de la cantidad reclamada de [IMPORTE EN LETRA] xx [IMPORTE] euros ( [IMPORTE] €), por las cuotas mensuales devengadas, mas los correspondientes intereses moratorios pactados, y la de [IMPORTE EN LETRA] yy [IMPORTE] euros ( [IMPORTE] €) por la indemnización como consecuencia de dicho incumplimiento, o subsidiariamente la suma que S.S.ª estime procedente, conforme a la fundamentación, y al abono de las costas causadas.

Es justicia de hacerse en [LUGAR], a [FECHA].

Firma del Abogado	Firma del Procurador/a
