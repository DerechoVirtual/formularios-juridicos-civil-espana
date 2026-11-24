---
name: demanda-juicio-verbal-contra-aseguradora-incumplir-civ-0737
description: "Demanda de juicio verbal contra la aseguradora por incumplir el seguro de defensa jurídica. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio verbal contra la aseguradora por incumplir el seguro de defensa jurídica

> Formulario **CIV-0737** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Demanda en reclamación de cantidad contra una compañía de seguros fundada en el incumplimiento por la misma del contrato de seguro de defensa jurídica concertado con el demandante.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio verbal contra la aseguradora por incumplir el seguro de defensa jurídica» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio verbal contra la aseguradora por incumplir el seguro de defensa jurídica” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:demanda-juicio-verbal-contra-aseguradora-incumplir-civ-0737`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (9 veces)
- [ ] FECHA (6 veces)
- [ ] NÚMERO (5 veces)
- [ ] IMPORTE (4 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] Nº DE DOCUMENTO (4 veces)
- [ ] CALLE (3 veces)
- [ ] ASEGURADORA (2 veces)
- [ ] MARCA/MODELO (2 veces)
- [ ] DENOMINACIÓN SOCIAL
- [ ] DESCRIPCIÓN DE LOS DAÑOS
- [ ] DIRECCIÓN
- [ ] DOMICILIO
- [ ] LUGAR
- [ ] MATRÍCULA
- [ ] MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] Nº
- [ ] Nº DE CLÁUSULA
- [ ] SEDE

## Normas que cita el formulario

- art. 9.2 LOPJ
- art. 45 LEC
- art. 85.1 LOPJ
- art. 68 LEC
- art. 52.2 LEC
- art. 10 LEC
- art. 437.1 LEC
- art. 5 Ley Orgánica 1/2025
- art. 1.089 CC
- art. 76 a) Ley 50/1980
- art. 1.100 CC
- art. 394 LEC
- art. 309 LEC

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
- Junto a «…o dispuesto en el art. 85.1º LOPJ) la Sección Civil del Tribunal de Instancia de»: Un solo TI por partido judicial (art. 84.1 LOPJ): sobra «de los de». Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Notas al pie del formulario original:
(1) Se indicarán todos los domicilios del deudor que se conozcan, y si no, el del lugar donde pueda ser hallado a efectos del requerimiento.


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

D./Dña. [NOMBRE Y APELLIDOS], Procurador de los Tribunales, en nombre y representación de [NOMBRE DEL REPRESENTADO/A], con domicilio en esta villa, calle [CALLE], n.º [NÚMERO], según acredito con la escritura de poder inscrito en el Registro Electrónico de Apoderamientos Judiciales, a cuya justificación aporto certificación de dicho Registro como documento nº [Nº DE DOCUMENTO]; asistido por el Letrado en ejercicio abajo firmante D./Dña. [NOMBRE Y APELLIDOS], con despacho profesional en [LOCALIDAD], ante el Tribunal comparezco y como mejor proceda en Derecho, DIGO:

Que mediante el presente escrito interpongo DEMANDA DE JUICIO VERBAL en reclamación de cantidad, contra la compañía anónima de seguros [ASEGURADORA], domiciliada en [DOMICILIO] c./ [DIRECCIÓN] n.º [NÚMERO], con base en los siguientes:

HECHOS

PRIMERO

El pasado [FECHA] mi mandante, como titular del vehículo marca [MARCA/MODELO] modelo [MARCA/MODELO] y matrícula [MATRÍCULA] suscribió una póliza de seguro obligatorio de responsabilidad civil con la compañía demandada.

Entre las cláusulas que forman parte de las Condiciones Generales/Particulares de dicha póliza destaca la señalada con el número [NÚMERO] en la que se recoge un contrato de seguro de defensa jurídica por el que la demandada se comprometía a hacerse cargo de los gastos en que pudiera incurrir mi representado (el asegurado) como consecuencia de su intervención en un procedimiento administrativo, judicial o arbitral y/o a prestarle o abonarle los servicios de asistencia jurídica, tanto judicial como extrajudicial hasta un límite de 15.000 euros.

Mi patrocinado se halla al corriente en el pago de las primas correspondientes a dicha póliza.

Acredito dichos extremos con los documentos números [Nº DE DOCUMENTO] que se acompañan a este escrito de demanda.

SEGUNDO

Con fecha [FECHA], cuando circulaba con su vehículo, mi representado se vio involucrado en un accidente de tráfico al colisionar dicho vehículo con el de D./Dña. [NOMBRE Y APELLIDOS], también asegurado por la Compañía demandada, como demuestra el documento que acompaño con el número

TERCERO

A consecuencia de dicho siniestro mi representado sufrió los siguientes daños en su persona: y en su vehículo [DESCRIPCIÓN DE LOS DAÑOS]

Acredito los mismos con los siguientes documentos:

CUARTO

Del mencionado siniestro y de sus correspondientes consecuencias mi representado dio oportuno parte a su Compañía Aseguradora [ASEGURADORA], la demandada, a fin de que ésta tramitase las diligencias pertinentes para la indemnización a mi mandante por los daños sufridos en el mismo.

No obstante, dado que la Compañía Aseguradora de mi mandante lo era también del titular del vehículo que provocó el siniestro, surgió entre el demandante y la demandada un conflicto de intereses que dio lugar a que mi representado, en ejercicio del derecho a la libre elección de abogado que se recoge en la Cláusula [Nº DE CLÁUSULA] del contrato, designó como tal al letrado D./Dña. [NOMBRE Y APELLIDOS] para que defendiera sus intereses, lo que se puso en conocimiento de la demandada.

QUINTO

Tras sucesivas conversaciones con la demandada el susodicho abogado consiguió un acuerdo extrajudicial con la citada Compañía de Seguros por el que ésta se obligaba a abonar a mi representado la cantidad de [IMPORTE] euros en concepto de indemnización por los daños sufridos en el citado accidente de circulación. Dicha cantidad fue abonada en la c/c de mi mandante abierta en la entidad [DENOMINACIÓN SOCIAL] el día [FECHA] como acredita el documento que acompaño como número

SEXTO

Por las gestiones efectuadas hasta el efectivo abono de la mentada indemnización a mi representado D./Dña. [NOMBRE Y APELLIDOS], el abogado, giró una minuta en la que se detallaba que sus honorarios ascendían a la cantidad de [IMPORTE] euros, copia de la cual adjunto como documento número

SÉPTIMO

Mi representado procedió al pago de la referida minuta el día [FECHA], mediante transferencia bancaria, como demuestra el documento número [Nº DE DOCUMENTO] de los que se unen a esta demanda.

OCTAVO

A la demandada se le ha reclamado el pago a mi mandante de las cantidades por este satisfechas al Letrado D./Dña. [NOMBRE Y APELLIDOS], habiendo resultado inútil cualquiera de las gestiones amistosas realizadas, por lo que se ve mi patrocinada en la necesidad de acudir al auxilio jurisdiccional.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento nº [Nº DE DOCUMENTO]

A los anteriores hechos son de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN Y COMPETENCIA

Sobre materia de la competencia genérica del orden civil de la jurisdicción (art. 9.2 LOPJ), tiene la competencia objetiva y funcional (art. 45 LEC, en relación con lo dispuesto en el art. 85.1º LOPJ) la Sección Civil del Tribunal de Instancia de esta villa, que por turno de reparto corresponda (art. 68 LEC), y la territorial, puesto que el domicilio del demandante se halla en la localidad de [LOCALIDAD] (art. 52.2 LEC).

II.- PROCEDIMIENTO

El juicio verbal a que se refieren los arts. 248, 250.2 y 437 y ss. LEC.

III.- LEGITIMACIÓN

Como titulares de la relación jurídica litigiosa que actúan como partes (art. 10 LEC), la legitimación activa corresponde a la demandante por ser la parte que ha cumplido sus obligaciones como asegurado en el contrato de seguro de defensa jurídica, y la pasiva la tiene la demandada en cuanto sujeta a la obligación de abonar el importe de los gastos ocasionados por dicha defensa jurídica a mi representada.

IV.- CUANTÍA

La cuantía de este litigio es de [IMPORTE] euros.

De ahí procede la preceptividad de la representación por procurador y la defensa por abogado, conforme a los arts. 23.2.1º y 31.2.1º LEC.

V.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 en relación con el art. 437.1 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

VI.- MATERIALES O SOBRE EL FONDO DEL ASUNTO

El art. 1.089 CCiv establece que las obligaciones nacen de la Ley, de los contratos y otros supuestos; estas obligaciones nacidas de los contratos son recogidas en el art. 1.091 del mismo Texto previniendo que las mismas tienen fuerza de Ley entre las partes y habrán de ser cumplidas a tenor de los mismos.

Los arts. 76 a) a 76 g), de la Ley 50/1980, de 8 de octubre, de contrato de seguro, en los que se regula el contrato de seguro de defensa jurídica, que de acuerdo con el art. 76 c) ‘deberá ser objeto de un contrato independiente, y aunque en el párrafo siguiente del mismo art. prevé la posibilidad de incluirse en capítulo aparte en una póliza única, es preciso en este supuesto, se especifique el contenido de la defensa jurídica garantizada, y la prima que le corresponde’ (TS de 20 de abril de 2000, Rec. 1927/1995), como ocurre en el presente supuesto.

Con respecto a esta modalidad contractual la SAP Almería de 22 de enero de 2001, Rec. 266/2000, señala que ‘El art. 76,a) de la Ley de Contrato de Seguro, introducido por la Ley 21/90 de 19 Dic., para adaptar el derecho Español a la directiva 88/357/CEE, sobre libertad de Servicios en seguros distintos al de vida, regula el seguro de defensa jurídica como aquel en virtud del cual se obliga el asegurador, dentro de los límites establecidos en la Ley en el contrato, a hacerse cargo de los gastos en que pueda incurrir el asegurado como consecuencia de su intervención en un procedimiento administrativo, judicial o arbitral a prestarle los servicios de asistencia jurídica, tanto judicial como extrajudicial con las exclusiones que prevé el art. 76 b).

El art. 76 d) de la referida Ley de Contrato de Seguro, regula el derecho del asegurado a la libre elección de Procurador y Abogado que le representen y defienda en cualquier clase de procedimiento, sin embargo, coincidiendo con la demandada, debe señalarse que ello no supone, una libertad absoluta del asegurado para obrar frente a la compañía aseguradora como tenga por conveniente, sino que al no extenderse la garantía de defensa jurídica más allá de los límites establecidos en la Ley y en el contrato, el derecho a la libertad de elección de los profesionales que representen y defiendan al asegurado en cualquier clase de procedimiento, se encuentra condicionado a la oportunidad del mismo y a la existencia de desavenencias o conflicto de intereses entre asegurador y asegurado, tal como resulta, tanto del propio art. 76 a) de la Ley cuando dice que el asegurador se obliga a hacerse cargo de los gastos en que pueda incurrir el asegurado como consecuencia de su intervención en un procedimiento judicial y "a prestarle los servicios jurídicos judicial o extrajudicial", como del art. 76, f), que reconoce el derecho de información al asegurado en caso de conflicto o desavenencia’.

Se cita el art. 1.100 CCiv, en cuanto a la aplicación de la mora, intimada la demandada desde fecha [FECHA], para hacer frente a la responsabilidad que se reclama, y el 1.108 del mismo Texto que previene que si el deudor incurre en mora, y no habiendo pacto en contrario, la indemnización de daños y perjuicios consistirá en el interés legal.

VII.- COSTAS

Conforme al art. 394 LEC, las costas procesales han de imponerse a la parte demandada.

Por lo expuesto,

SUPLICO AL TRIBUNAL

que tenga por presentado este escrito con sus documentos y copias de todo ello, teniéndome por comparecido y parte en la representación que ostento, y ordenando se entiendan conmigo las sucesivas actuaciones; se sirva admitir a trámite la demanda de juicio verbal que se interpone, acuerde dar traslado al demandado para que comparezca y la conteste, y seguido el juicio por sus trámites, se venga a dictar sentencia que condene al demandado al pago de la cantidad de [IMPORTE] euros que se reclama como principal, más los intereses moratorios correspondientes devengados desde la fecha de interposición de la demanda, con costas procesales.

Es de Justicia que se pide en [LUGAR], a [FECHA].

OTROSÍ PRIMERO DIGO: Que interesa al derecho de esta parte valerse para el acto de la vista de los siguientes medios de PRUEBA:

I.- INTERROGATORIO DE LA PARTE CONTRARIA, a fin de que sea citado D./Dña. [NOMBRE Y APELLIDOS], como representante legal de la sociedad demandada, que intervino personalmente en los hechos que justifican la demanda, conforme al art. 309 LEC.

II.- TESTIFICAL, a fin de que sean citados judicialmente los siguientes individuos:

D./Dña. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], calle [CALLE], n.º [NÚMERO]

D./Dña. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], calle [CALLE], n.º [NÚMERO]

OTROSÍ SEGUNDO DIGO: A los efectos prevenidos por el art. 155.2, párrafo 1.º ‘in fine’ LEC, habiéndose designado dos domicilios de la demandada, interesa esta parte se efectúe primeramente el emplazamiento en el domicilio de esta villa, segundo de los designados, y supletoriamente, en el domicilio social, de la localidad

OTROSÍ TERCERO DIGO: Que esta parte asume el compromiso de recibir cualquier comunicación dirigida por la oficina judicial, durante toda la fase declarativa, e, incluso, en una eventual fase de ejecución por medios telemáticos, en términos del art. 399.1 II en relación al art. 437.1, ambos LEC, consignándose a estos efectos la siguiente dirección de correo electrónico y nº [Nº] de teléfono:

En su virtud,

SUPLICO AL TRIBUNAL que, teniendo por causadas las anteriores manifestaciones a los efectos oportunos, se digne acordar conforme se solicita.

Reitero Justicia en lugar y fecha ‘ut supra’.

Firma del Abogado/a	Firma del Procurador/a
