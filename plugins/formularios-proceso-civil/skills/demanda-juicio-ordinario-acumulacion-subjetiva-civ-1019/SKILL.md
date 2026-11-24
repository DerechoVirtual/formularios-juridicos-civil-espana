---
name: demanda-juicio-ordinario-acumulacion-subjetiva-civ-1019
description: "Demanda de juicio ordinario con acumulación subjetiva de acciones por daños de circulación. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio ordinario con acumulación subjetiva de acciones por daños de circulación

> Formulario **CIV-1019** del plugin **Proceso civil: demandas, contestaciones, prueba y vista** (`formularios-proceso-civil`) · Civil › Escritos procesales (demanda, contestación, prueba, vista) · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio ordinario de reclamación de daños y perjuicios ocasionados con motivo de la circulación de vehículos a motor. Acumulación subjetiva de acciones.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio ordinario con acumulación subjetiva de acciones por daños de circulación» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio ordinario con acumulación subjetiva de acciones por daños de circulación” para mi caso». También puedes invocarla directamente con `/formularios-proceso-civil:demanda-juicio-ordinario-acumulacion-subjetiva-civ-1019`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-proceso-civil:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Proceso civil: demandas, contestaciones, prueba y vista) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (15 veces)
- [ ] IMPORTE EN CIFRA (12 veces)
- [ ] NOMBRE Y APELLIDOS (9 veces)
- [ ] ASEGURADORA (5 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] MARCA/MODELO (4 veces)
- [ ] Nº (4 veces)
- [ ] FECHA (3 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] DOMICILIO (2 veces)
- [ ] MATRÍCULA (2 veces)
- [ ] AÑO
- [ ] CALLE
- [ ] CIRCUNSTANCIAS DEL CASO
- [ ] CORREO ELECTRÓNICO
- [ ] DESGLOSE DE GASTOS DE ASISTENCIA
- [ ] FECHAS
- [ ] IMPORTE EN LETRA
- [ ] LESIONES
- [ ] LUGAR
- [ ] LUGAR DEL SINIESTRO
- [ ] NOMBRE DE LA CLÍNICA
- [ ] Nº DE COLEGIADO/A
- [ ] Nº DE DÍAS
- [ ] SEDE

## Normas que cita el formulario

- art. 24.1 LEC
- art. 399.1 LEC
- art. 52.1.9.º LEC
- art. 54.1 LEC
- art. 85.1 LOPJ
- art. 10 LEC
- art. 76 LCS
- art. 5 Ley Orgánica 1/2025
- art. 403 Ley 1/2000
- art. 1.902 CC
- art. 72 LEC
- art. 20 LCS
- art. 20.6.º LCS
- art. 253.1 LEC
- art. 23 LEC
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

### Avisos de actualización (1) — se aplican en el texto, nunca se copian en el documento

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales y de D./Dña. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], representación que acredito mediante escritura de poder otorgada a mi favor (existen tres posibilidades para otorgar el apoderamiento al Procurador de los Tribunales, conforme dispone el art. 24.1 LEC)

[OPCIONAL — opción en función de cómo se haya otorgado el poder]

[ELEGIR UNA OPCIÓN: Si el poder se otorga a través de la sede judicial electrónica / Si el poder se otorga mediante comparecencia apud acta / Si el poder se otorga ante Notario]

bajo la dirección letrada de D./Dña. [NOMBRE Y APELLIDOS], abogado/a en ejercicio, con despacho profesional abierto en [LOCALIDAD], colegiado nº [Nº DE COLEGIADO/A] del Ilustre Colegio de la Abogacía de [LOCALIDAD], ante el Tribunal comparezco y como mejor en Derecho proceda, DIGO:

Que mediante el presente escrito vengo a formular DEMANDA DE JUICIO ORDINARIO EN RECLAMACIÓN DE DAÑOS Y PERJUICIOS OCASIONADOS CON MOTIVO DE LA CIRCULACIÓN DE VEHÍCULOS DE MOTOR, contra D./Dña. [NOMBRE Y APELLIDOS], con domicilio, primero en [DOMICILIO]; y segundo, el domicilio laboral en [DOMICILIO]); con email [CORREO ELECTRÓNICO]; y con número de teléfono móvil ( indicar si solo es conductor, o propietario, o conductor y propietario) y contra la Compañía de Seguros [ASEGURADORA], con domicilio social en [LOCALIDAD], calle [CALLE], número [NÚMERO]; todo ello de conformidad con los hechos y fundamentos de derecho que se especificarán.

Que esta parte asume el compromiso de recibir cualquier comunicación dirigida por la oficina judicial, durante toda la fase declarativa, e, incluso, en una eventual fase de ejecución por medios telemáticos, en términos del art. 399.1 II LEC, consignándose a estos efectos la siguiente dirección de correo electrónico y nº [Nº] de teléfono:

HECHOS

PRIMERO

El demandante es propietario del vehículo marca [MARCA/MODELO], modelo [MARCA/MODELO], con matrícula [MATRÍCULA], dejando a efectos probatorios designado el archivo de la Jefatura Provincial de Tráfico de [LOCALIDAD], encontrándose asegurado con la Compañía de Seguros [ASEGURADORA] con el n.º [Nº] de póliza

SEGUNDO

El demandado D./Dña. [NOMBRE Y APELLIDOS] lo es en su condición de propietario del vehículo marca [MARCA/MODELO], modelo [MARCA/MODELO], con matrícula [MATRÍCULA], extremo que también se demostrará, de ser necesario, con la misma remisión que antecedentemente se ha efectuado, y resulta ser además el conductor de tal automóvil en fecha

TERCERO

El demandado D./Dña. [NOMBRE Y APELLIDOS] tenía suscrito un contrato de seguro, en relación con el vehículo de que es titular, con la Entidad [ASEGURADORA], póliza número [NÚMERO], en vigor al momento de ocurrir el accidente, y por el cual se cubría la responsabilidad civil a que se refiere el art. 1 del Texto Refundido de la Ley sobre Responsabilidad Civil y Seguro en la Circulación de Vehículos a Motor, y tanto hasta los límites del aseguramiento obligatorio como por encima de los mismos hasta [IMPORTE]. Por tanto, la entidad demandada lo es en su condición de asegurador que asumió el cumplimiento de la obligación de indemnizar.

CUARTO

El día [FECHA], sobre las [Nº] horas, y cuando circulaba por [LUGAR DEL SINIESTRO]

QUINTO

Como consecuencia de los hechos descritos se han ocasionado diversos daños materiales y corporales. En cuanto a los primeros, se reclama el coste de la reparación total del vehículo, que asciende a la cantidad de [IMPORTE] euros ( € [IMPORTE EN LETRA]), más los gastos de grúa por transporte desde el lugar del accidente al taller de reparación por la cantidad de [IMPORTE] euros ([IMPORTE EN CIFRA] €), según se acredita con las correspondientes facturas que se acompañan (documentos nos. [Nº DE DOCUMENTO])

Por lo que respecta a los daños corporales, mi representado ha permanecido [Nº] días de baja, de los cuales [Nº DE DÍAS] ha estado hospitalizado en la clínica [NOMBRE DE LA CLÍNICA], causándosele [LESIONES], según se acredita con el oportuno informe médico (documento n.º [NÚMERO])

SEXTO

Previamente a la presentación de la presente demanda, se han llevado a cabo negociaciones con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad, y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria; incluyéndose entre las acciones realizadas el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución (documentos números [Nº DE DOCUMENTO]).

Finalmente, con anterioridad a la presentación de la demanda se ha requerido de pago a los demandados en el procedimiento, mediante sendos telegramas de fecha [FECHA], que se acompañan como documentos números [Nº DE DOCUMENTO], sin que por ninguno de ellos se haya hecho efectiva la indemnización reclamada.

FUNDAMENTOS DE DERECHO

I.- COMPETENCIA

El art. 52.1.9.º LEC fija, con carácter indisponible (art. 54.1 LEC), la competencia territorial en este tipo de procesos, atribuyéndoselos al tribunal del lugar en que se causaron los daños, siendo la competencia objetiva y funcional del Tribunal de Instancia (art. 85.1º LOPJ, y 45 y 61 LEC).

II.- PROCEDIMIENTO

Los arts. 248, 249.2 y 399 y ss. LEC sobre la procedencia del juicio declarativo ordinario instado.

III.- LEGITIMACIÓN

Está legitimado activamente mi representado por ser quien ha sufrido los daños materiales y corporales consecuencia del siniestro (art. 10 LEC)

Está legitimado pasivamente el demandado D./Dña. [NOMBRE Y APELLIDOS] por ser el quien se señala como conductor y propietario del vehículo y por tanto, agente de los daños causados, e igualmente la Compañía de Seguros codemandada [ASEGURADORA] por conocerse tiene suscrito con el propietario del vehículo un contrato de seguro de responsabilidad civil derivada del uso y circulación de vehículos de motor, en vigor al tiempo de ocurrir el accidente, conforme al art. 76 LCS.

IV.- Cumplimiento de los requisitos de procedibilidad

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

Asimismo, se acompañan los documentos que acreditan la presentación de la reclamación al asegurador y la respuesta motivada emitida por éste rechazando el siniestro, presupuesto de admisión de la demanda conforme al art. 7.8 TRLRCSCVM), que dispone que "No se admitirán a trámite, de conformidad con el artículo 403 de la Ley 1/2000, de 7 de enero, de Enjuiciamiento Civil, las demandas en las que no se acompañen los documentos que acrediten la oferta o respuesta motivada, si se hubiese emitido por el asegurador o, en caso de no haberse emitido, la reclamación previa al asegurador, que no requerirá cuantificación".

V.- FUNDAMENTOS JURÍDICO-MATERIALES

1.- En esta demanda se ejercita la acción que nace de la obligación legal dimanante de la intervención de culpa o negligencia del art. 1.902 CCiv, en el régimen de responsabilidad subjetivista para obtener la indemnización correspondiente por los daños y perjuicios ocasionados por un accidente de circulación, y al propio tiempo, la acción que nace de la obligación legal de responder, en régimen cuasiobjetivo, por socialización del riesgo en este tipo de actividad —tráfico viario—, en base a la noción de riesgo creado, conforme al art. 1 del Texto Refundido de la Ley sobre Responsabilidad Civil y Seguro en la Circulación de Vehículos a Motor.

La primera acción exige que, producido un daño, se demuestre la relación de causalidad adecuada como consecuencia de una acción u omisión culposa, requisitos que se cumplen en este caso, mientras que la segunda, sin que falte tampoco el daño resarcible y el nexo causal, elimina el requisito de culpabilidad en punto a los daños corporales, aunque no totalmente, puesto que en tal caso, también cabe probar que los mismos fueron debidos únicamente a la culpa o negligencia del perjudicado, o a fuerza mayor ajena a la conducción. Por ello, dado que no es posible ningún reproche de culpa o negligencia a la víctima, siendo la conducta del demandado la única determinante de los daños ocasionados, sobre él recae la obligación indemnizatoria.

Actuar culposo del demandado que sirve igualmente para determinar su responsabilidad respecto a los daños materiales.

En este caso [CIRCUNSTANCIAS DEL CASO]

2.- El art. 7 del Texto Refundido de la LRCSCVM establece que el asegurador deberá satisfacer al perjudicado el importe de los daños sufridos en su persona y en sus bienes, el cual tendrá acción directa para exigirlo. Esta posibilidad aparece recogida de manera generalizada en el art. 76 LCS.

3.- La demanda se dirige frente a los dos obligados, planteándose así una acumulación inicial de pretensiones subjetiva al amparo del art. 72 LEC, que se fundamenta en la identidad de los hechos existente entre las mismas y que lleva a una dualidad de sujetos a ocupar la posición jurídica de parte demandada.

4.- Cuantificación de los daños.

4.1- Daños corporales: el anexo del Texto Refundido de la Ley sobre Responsabilidad Civil y Seguro en la Circulación de Vehículos a Motor, fija el sistema para la valoración de los daños y perjuicios causados a las personas en accidente de circulación. Para el año [AÑO], las cuantías de las indemnizaciones por muerte, lesiones permanentes e incapacidad permanente son:
A) Indemnización por incapacidad temporal.(En su caso)

Días de baja durante estancia hospitalaria:

Indemnización diaria [IMPORTE] euros ([IMPORTE EN CIFRA] €). Son [IMPORTE] euros ([IMPORTE EN CIFRA] €).

Días de baja sin estancia hospitalaria:

Indemnización diaria [IMPORTE] euros ([IMPORTE EN CIFRA] €). Son [IMPORTE] euros ([IMPORTE EN CIFRA] €).

Factores de corrección (Se indicarán los factores de corrección y el porcentaje aplicable)

Total por incapacidad [IMPORTE] euros ([IMPORTE EN CIFRA] €).

B) Indemnización por lesión permanente.(En su caso)

Concreción de las lesiones permanentes:

Puntos asignados:

Valor de los puntos en [IMPORTE] euros:

Factores de corrección:

Total por lesiones: [IMPORTE] euros ([IMPORTE EN CIFRA] €).

C) Además se satisfarán en todo caso los gastos de asistencia médica y hospitalaria.
[DESGLOSE DE GASTOS DE ASISTENCIA]

Total por gastos de asistencia [IMPORTE] euros ([IMPORTE EN CIFRA] €).

4.2- Daños materiales: Los daños que se prueban se rigen por principio de indemnidad o "restitutio in integrum", por lo que la reparación viene fijada por los efectivamente sufridos.

Los gastos de reparación del vehículo ascienden a la cantidad de [IMPORTE] euros ([IMPORTE EN CIFRA] €), y los de traslado al taller en grúa, a la de [IMPORTE] euros ([IMPORTE EN CIFRA] €).

VI.- MORA

El art. 9 del Texto Refundido de la LRCSCVM establece que cuando el asegurador incurriese en mora en el cumplimiento de su prestación, la indemnización de daños y perjuicios debidos por el asegurador se regirá por lo dispuesto en el art. 20 LCS, con las peculiaridades contenidas en dicho precepto.

Al no haber procedido el asegurador al pago de la prestación, ni haber consignado ésta judicialmente en el plazo de tres meses desde la producción del siniestro, ni en dinero ni mediante aval solidario u otro medio que garantice inmediata disponibilidad, y no concurriendo ninguna causa que justifique esa falta de satisfacción de la indemnización, procede la imposición de un interés moratorio sobre la indemnización debida, igual al interés legal del dinero vigente en el momento del devengo, incrementado en el 50%, puesto que no han trasncurrido más de dos años.

El término inicial del cómputo de intereses es el de la fecha del siniestro, conforme a lo establecido en el art. 20.6.º LCS, momento que resulta aquí plenamente aplicable puesto que

VII.- CUANTÍA DE LA DEMANDA

La cuantía de la demanda a los efectos de lo dispuesto en el art. 253.1 de la LEC es la de [IMPORTE] euros ([IMPORTE EN CIFRA] €), en aplicación de la regla 1.ª del art. 251, según el cual si se reclama una cantidad de dinero determinada, la cuantía de la demanda estará representada por dicha cantidad.

De ahí procede la preceptividad de la representación por Procurador/a y la defensa por Abogado, conforme a los arts. 23 y 31 LEC.

VIII.- COSTAS

El art. 394.1 LEC establece que se impondrán al litigante cuyas pretensiones hayan sido totalmente rechazadas, por lo que, no existiendo ninguna circunstancia de dudas de hecho o de derecho, siendo masiva la jurisprudencia al respecto, no se justificaría la no aplicación de la regla general, deben serle impuestas a los demandados condenados en la sentencia.

Por lo expuesto,

SUPLICO AL TRIBUNAL

que teniendo por presentado este escrito, con los documentos y las copias que se acompañan, se sirva admitirlo, tener por comparecido y parte al Procurador/a de los Tribunales D./Dña. [NOMBRE Y APELLIDOS] en la representación que ostento, entendiéndose conmigo las sucesivas diligencias, y por interpuesta demanda de juicio ordinario en reclamación de daños y perjuicios ocasionados con motivo de la circulación de vehículos de motor, y seguido que sea el procedimiento por sus trámites, se venga a dictar sentencia por la que se condene a que D./Dña. [NOMBRE Y APELLIDOS], y la Compañía de Seguros [ASEGURADORA], indemnicen conjunta y solidariamente al demandante en la cantidad de [IMPORTE] euros ([IMPORTE EN CIFRA] €), más lo que representen los intereses por mora, que en el caso de la Compañía de Seguros se fijará en el tipo de interés anual igual al legal del dinero vigente en el momento del devengo, incrementado en un 50%, desde la fecha del siniestro y hasta el efectivo definitivo pago, imponiéndose a los demandados las costas procesales.

Es justicia de hacerse en [LUGAR], a [FECHA].

Firma del Abogado	Firma del Procurador/a
