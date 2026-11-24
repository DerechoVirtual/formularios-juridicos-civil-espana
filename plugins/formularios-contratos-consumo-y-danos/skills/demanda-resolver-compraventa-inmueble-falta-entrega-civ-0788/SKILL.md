---
name: demanda-resolver-compraventa-inmueble-falta-entrega-civ-0788
description: "Demanda para resolver la compraventa de inmueble por falta de entrega del bien por la promotora. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda para resolver la compraventa de inmueble por falta de entrega del bien por la promotora

> Formulario **CIV-0788** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio ordinario sobre resolución de contrato de compraventa de inmueble por incumplimiento de entrega del bien de la promotora, con reparación de daños y perjuicios, codemandando a entidad bancaria avalista por cantidades entregadas a cuenta de la vivienda.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda para resolver la compraventa de inmueble por falta de entrega del bien por la promotora» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda para resolver la compraventa de inmueble por falta de entrega del bien por la promotora” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:demanda-resolver-compraventa-inmueble-falta-entrega-civ-0788`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (11 veces)
- [ ] NÚMERO (11 veces)
- [ ] FECHA (8 veces)
- [ ] ENTIDAD BANCARIA (5 veces)
- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] CALLE (3 veces)
- [ ] DENOMINACIÓN SOCIAL (3 veces)
- [ ] AÑO
- [ ] COLEGIO
- [ ] DESCRIPCIÓN DEL BIEN
- [ ] DOMICILIO
- [ ] LUGAR
- [ ] MES
- [ ] Nº DE DOCUMENTO
- [ ] PARTE DEMANDADA
- [ ] SEDE
- [ ] SUCURSAL

## Normas que cita el formulario

- art. 36 LEC
- art. 85 LOPJ
- art. 45 LEC
- art. 51 LEC
- art. 7.1 LEC
- art. 10 LEC
- art. 253.1 LEC
- art. 1.124 Código Civil
- art. 1124 Código Civil
- art. 1.152 CC
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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] QPTRC»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] QPTRC

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS], conforme acredito con escritura de poder inscrito en el Registro Electrónico de Apoderamientos Judiciales con el nº [NÚMERO], y con la asistencia del Letrado D./Dña. [NOMBRE Y APELLIDOS], del Ilustre Colegio de Abogados de [COLEGIO], cuyo despacho está abierto en esta población, calle [CALLE], ante la Sección Civil del Tribunal de Instancia que por turno de reparto corresponda, comparezco y, como mejor proceda en Derecho, DIGO:

Que por medio del presente escrito, en la representación que ostento, vengo a formular demanda de juicio ordinario, sobre resolución de contrato y condena a pago de cantidad, contra la entidad [DENOMINACIÓN SOCIAL], para ser citada en su oficina de [SUCURSAL], calle [CALLE], y contra la entidad CAJA DE AHORROS DEL [ENTIDAD BANCARIA], para ser citada en su sede [DOMICILIO], calle [CALLE], con base en los siguientes datos y razonamientos jurídicos:

HECHOS

PRIMERO.- Mi mandante y la entidad codemandada [DENOMINACIÓN SOCIAL], suscribieron en documento privado de fecha [FECHA], la compraventa de nueva vivienda, cuya descripción se transcribe a continuación:

« [DESCRIPCIÓN DEL BIEN] descripción, linderos, referencia registral ».

En el citado contrato se fijó como fecha de entrega de la vivienda, la segunda mitad del mes de [MES] de [AÑO] (cláusula n.º [NÚMERO]), y quedó fijado en la cláusula n.º [NÚMERO] que el precio de la compraventa era de [IMPORTE] euros ( €), el cual se aplazaba mediante abonos mensuales de [IMPORTE] euros ( €), después de un inicial pago alzado de otros [IMPORTE] euros ( €).

También se recoge la forma de pago y se relacionan los recibos para su presentación al cobro en la entidad bancaria codemandada [ENTIDAD BANCARIA], en los que se documentó el precio aplazado.

Por último, la estipulación sexta del referido contrato, en su último párrafo, establece para el supuesto de incumplimiento de la vendedora y la opción por la resolución de la compradora que "si la parte compradora optara por la resolución de pleno derecho de la presente compraventa, la parte vendedora deberá abonar a la compradora las cantidades recibidas en este acto de la compradora más otra cantidad equivalente al pago inicial, en concepto de cláusula penal".

Se acompaña el contrato como DOCUMENTO N.º [NÚMERO].

SEGUNDO.- La entidad bancaria codemandada CAJA DE AHORROS DEL [ENTIDAD BANCARIA] constituyó en la misma fecha un aval bancario a primer requerimiento por las cantidades que se irían entregando a cuenta de la vivienda en la forma referida, con objeto de garantizar el cumplimiento de la obligación de entrega del contrato.

Se adjunta como DOCUMENTO N.º [NÚMERO] el referido contrato de aval.

TERCERO.- En dicho acto, mi representado abonó a la vendedora la cantidad de [IMPORTE] euros (estipulación n.º [NÚMERO]), mas el IVA correspondiente.

Posteriormente, ha abonado un total de [IMPORTE] euros más IVA, a razón de [IMPORTE] euros más IVA al mes, durante 18 meses, en el periodo que va desde [FECHA] hasta [FECHA] Todo ello, hace un total de [IMPORTE] euros.

Se adjunta como DOCUMENTO N.º [NÚMERO] el bloque de los recibos bancarios que acreditan el pago de la cantidad inicial y de las 18 mensualidades posteriores referidas.

CUARTO.- Llegada la fecha pactada en el contrato privado para la entrega de la vivienda construida y el correspondiente otorgamiento de escritura pública, [DENOMINACIÓN SOCIAL]. informó verbalmente que por diversos problemas sufridos por la misma, en el marco de la actual situación de crisis global, las obras sufren un retraso de 6 meses, y no estarán listas para la entrega hasta el mes de

Puesto en contacto mi mandante con personal de la constructora, se le informa que no se ha solicitado todavía la licencia de primera ocupación, cuya concesión requiere un procedimiento que puede durar según las circunstancias de cada administración municipal concedente. Asimismo, personados en el lugar de la construcción, se observa, a primera vista, que el estado actual de las obras hace muy difícil que las mismas se terminen en el plazo de seis meses referido.

QUINTO.- Con fecha [FECHA], después de agotados los intentos de solución pacífica del asunto, y consolidada la certeza de que la promotora codemandada no iba a poder terminar la vivienda en un plazo razonable, se practicó requerimiento notarial ante D./Dña. [NOMBRE Y APELLIDOS], que lleva n.º [NÚMERO] de su protocolo general corriente, al cual aquella no respondió, y en el que, además de exigir la devolución de las cantidades entregadas, por resolución debida al incumplimiento radical de la entrega, se indicaba la reclamación de un importe equivalente a la cantidad inicial entregada, como cláusula penal, en indemnización de daños y perjuicios sufridos, derivados de la falta de recepción de la vivienda en el plazo previsto.

Con posterioridad, en fecha [FECHA], se practicó requerimiento notarial ante D./Dña. [NOMBRE Y APELLIDOS], que lleva n.º [NÚMERO] de su protocolo general corriente, frente a la avalista CAJA DE AHORROS DEL [ENTIDAD BANCARIA], para el pago de las cantidades entregadas a cuenta. Por la misma, se contestó que la causa de resolución alegada por mi mandante, no estaba prevista en el aval por ella otorgado.

Se acompañan las actas públicas de requerimiento como DOCUMENTOS N.º [NÚMERO] y [Nº DE DOCUMENTO], así como la contestación escrita del banco como DOCUMENTO N.º [NÚMERO].

FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN Y COMPETENCIA.

Los arts. 21 y ss. LOPJ y art. 36 LEC atribuyen con carácter general a la jurisdicción de nuestro Estado y al orden civil, el conocimiento de una materia como la presente.

El art. 85 LOPJ y art. 45 LEC, designan a las secciones civiles de los tribunales de instancia, como los órganos con la competencia específica objetiva y funcional para resolver estos pleitos.

Finalmente, el art. 51 LEC fija que la competencia territorial general, en el caso de personas jurídicas, será del órgano del lugar de su domicilio.

II.- PROCEDIMIENTO.

En aplicación de los arts. 248.3, 249.2 y 251.1.ª LEC, y en atención a la cuantía reclamada que asciende a [IMPORTE] EUROS, este pleito se tramitará por las normas de proceso declarativo llamado Juicio Ordinario.

III.- CAPACIDAD.

Conforme a los arts. 6.1.1.º y 3.º LEC tienen capacidad para ser parte las personas físicas y las jurídicas, y a tenor de arts. 7.1 y 4 LEC, detentan capacidad de obrar procesal, aquéllas mayores de edad no incapacitadas, y éstas constituidas legalmente a través de sus representantes necesarios.

IV.- LEGITIMACIÓN.

El art. 10 LEC legitima para comparecer y actuar en juicio, a los titulares de la relación jurídica o del objeto litigioso. En el caso de autos, el demandante y las demandadas, son los sujetos titulares de los contratos cuyo incumplimiento arraiga las acciones resolutorias y de condena que se ejercen, existiendo, pues, legitimación directa ordinaria. El demandante es titular del crédito derivado del reintegro de las cantidades entregadas y de los daños y perjuicios irrogados, habiendo cumplido su prestación. Están legitimadas pasivamente las demandadas por ser la primera el vendedor, deudor del pago de las cantidades recibidas y la cláusula penal; y la segunda como avalista en la entrega de las cantidades

V.- POSTULACIÓN.

En aplicación de los arts. 23.1 y 31.1 LEC, las partes comparecerán representadas por Procurador/a de los Tribunales y asistidas por Letrado en ejercicio, ambos habilitados ante el Tribunal.

VI.- CUANTÍA.

Cumpliendo la exigencia del art. 253.1 LEC, se cifra la cuantía de la demanda en la cantidad de [IMPORTE] euros ( €), correspondiente a la suma de cantidades entregadas que se reclaman, y la cláusula penal que también se reclama como indemnización.

VII.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda cumple con el requisito de procedibilidad exigido por la disp. adic. 7ª de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

VIII.- FUNDAMENTOS MATERIALES.

Se ejercita la acción resolutoria del contrato de compraventa por incumplimiento de la vendedora de la entrega en plazo del objeto de la misma, acumulando la acción de reclamación de cantidad correspondiente al precio pagado hasta la fecha, frente a la entidad bancaria avalista de la operación, y reclamación a la propia vendedora de la cláusula penal pactada. Todo ello, con arreglo a los siguientes razonamientos:

PRIMERO.- DE LA POSIBILIDAD DE INSTAR LA RESOLUCIÓN DEL CONTRATO.

La actitud mantenida por la promotora codemandada constituye un incumplimiento sustancial de las obligaciones asumidas mediante el contrato suscrito con fecha [FECHA], de acuerdo con la normativa aplicable. En tal sentido, dispone el artículo 1.124 del Código Civil que la facultad de resolver las obligaciones se entiende implícita en las recíprocas para el caso de que uno de los obligados no cumpliere lo que se le incumbe. El perjudicado podrá escoger entre exigir el cumplimiento o resolución de la obligación, con el resarcimiento de daños y abono de intereses en ambos casos.

La facultad resolutoria implícita reconocida en el art. 1.124 del Código Civil está sometida a una serie de requisitos que, tanto la doctrina como jurisprudencia vienen exigiendo para la aplicación de este precepto legal (por todas, pueden citarse las Sentencias de la Sala Primera del Tribunal Supremo de 23 de enero de 1990 y de 3 de junio de 1994, entre otras muchas) y son resumidos de forma muy clara en la Sentencia del Tribunal Supremo de 13 de mayo de 2004, rec. 1749/1998:

"Es doctrina de esta Sala, reiterada entre otras muchas, la de que para que la acción resolutoria implícita establecida en el párrafo primero del artículo 1124 del Código Civil pueda prosperar, es preciso que quien la alegue acredite en el proceso correspondiente, entre otros, los siguientes requisitos:

1º. La existencia de un vínculo contractual vigente entre quienes la concertaron (Sentencias de 10 de Diciembre de 1947 y 9 de Diciembre de 1948).
2º. La reciprocidad de las prestaciones estipuladas en el mismo (Sentencias de 28 de Septiembre de 1965 y 30 de Marzo de 1976) así como su exigibilidad (Sentencias de 6 de Julio de 1952 y 1 de Febrero de 1966).
3º. Que el demandado haya incumplido de forma grave las que le incumbían (Sentencias de 9 de Diciembre de 1960 y 18 de Noviembre de 1970), estando encomendada la apreciación de este incumplimiento al libre arbitrio de los Tribunales de instancia (Sentencias de 17 de Diciembre de 1976 y 17 de Febrero de 1977).
4º. Que semejante resultado se haya producido como consecuencia de una conducta obstativa de éste que, de modo indubitado, absoluto, definitivo e irreparable la origine, actuación que, entre otros medios probatorios, puede acreditarse por la prolongada inactividad o pasividad del deudor frente a los requerimientos de la otra parte contratante (Sentencia de 5 de Mayo de 1970).
5º. Que quien ejercite esta acción no haya incumplido las obligaciones que le concernian (Sentencias de 6 de Julio y 29 de Marzo de 1977)"

En el presente caso se cumplen todos los requisitos que facultan a mis mandantes para dar por resuelto el contrato de compraventa en aplicación de tal precepto:

a) Contrato vigente y de prestaciones recíprocas. El contrato que une a las partes es precisamente un contrato de construcción y entrega de una vivienda, en el que ambas partes contratantes se obligan al cumplimiento de una serie de deberes.
b) Incumplimiento de sus obligaciones por parte de la mercantil codemandada, puesto que la parte vendedora ha incumplido su obligación de construcción y entrega de la vivienda, siendo tal obligación absolutamente, prestación esencial en el contrato firmado por ambas partes contratantes, tal y como preceptúan los artículos 1.461 y 1.544 del Código Civil. Se ha producido una absoluta frustración de los legítimos intereses que llevaron a mi mandante a concluir el negocio.

No debe olvidarse que el rigor con el que se exigía la actitud dolosa y deliberadamente rebelde de la parte que incumple, para justificar la resolución, ha venido siendo notablemente atenuado por distintos pronunciamientos jurisprudenciales y de forma continuada (aunque en este caso, además, concurre), tal y como resume la Sentencia del Tribunal Supremo de 5 de abril de 2006, rec. 1980/1999.

SEGUNDO.- DE LOS EFECTOS DE LA RESOLUCIÓN CONTRACTUAL: RESTITUCIÓN DE LAS PRESTACIONES.

El efecto más inmediato que se deriva de la resolución del contrato es, aparte de quedar éste sin efecto, la obligada restitución recíproca de las prestaciones recibidas, y dado que mi representado nada ha recibido en virtud del contrato que se resuelve, nada debe restituir. Sin embargo, la parte demandada recibió inicialmente y en los distintos plazos pactados un total de [IMPORTE] euros, como parte del precio final acordado, cantidades que se deben restituir a mis mandantes de forma inmediata.

Si bien, en este caso, el contrato se encuentra garantizado por un aval específico otorgado por la entidad bancaria codemandada en relación a las cantidades entregadas a cuenta, de conformidad con la Disposición Adicional Primera de la Ley 38/1999 de Ordenación de la Edificación, reguladora de la percepción de cantidades a cuenta del precio durante la construcción de viviendas. En dicho precepto se prevé la garantía para la devolución de las cantidades entregadas y el interés legal del dinero vigente hasta el momento en que se haga efectiva la devolución, para el caso de que la construcción no se inicie o no llegue a buen fin en el plazo convenido para la entrega de la vivienda.

Habiéndose dirigido mi mandante contra la promotora, sin que haya devuelto las cantidades, se ha dirigido contra la entidad bancaria avalista, quien alega una falta de especificación de la causa de resolución, que no ampara la ley, pues la misma prevé la devolución cuando la construcción no llegue a buen fin; escenario que acontece en el presente caso, sin necesidad de que el contrato en cuestión lo recoja expresamente.

De esta forma, habiendo cumplido mi mandante con todas las prestaciones a las que venía obligado, debe condenarse a, en este caso la avalista, a devolver las cantidades entregadas más el interés legal desde cada uno de los pagos hasta su efectiva devolución.

TERCERO.- DE LOS EFECTOS DE LA RESOLUCIÓN CONTRACTUAL: INDEMNIZACIÓN DE LOS DAÑOS Y PERJUICIOS OCASIONADOS.

Como se ha referido, el artículo 1.124 del Código Civil prevé que el acreedor que sufra el incumplimiento de la contraparte en un contrato sinalagmático podrá, además de optar entre exigir el cumplimiento o la resolución del contrato reclamar los daños e intereses.

Es aplicable el art. 1.152 CCiv, que establece que ’en las obligaciones con cláusula penal, la pena sustituirá a la indemnización de daños y al abono de intereses en caso de falta de cumplimiento, si otra cosa no se hubiere pactado‘, y la doctrina al respecto de las arras penales [STS de 17 de febrero de 1982]. En el presente caso, habiéndose pactado expresamente tal posibilidad, procede reclamar a la promotora codemandada una cantidad equivalente al importe inicial entregado a la firma del contrato, que se cuantifica en [IMPORTE] euros.

IX.- COSTAS.

Las costas del presente procedimiento deberán ser impuestas a la parte demandada, con arreglo al art. 394.1 LEC, que recoge el principio objetivo del vencimiento en la materia por lo que respecta a los juicios declarativos en su primera instancia.

En atención a todo lo anterior es por lo que,

AL TRIBUNAL SUPLICO

que, teniendo por presentado este escrito de demanda junto con los documentos que se acompañan y copias simples de todo ello, se sirva admitir uno y otros, se me tenga por comparecida y parte, en la representación que ostento y con carácter de demandante, entendiéndose conmigo las ulteriores sucesivas diligencias, y por promovido juicio ordinario contra [PARTE DEMANDADA] y contra CAJA DE AHORROS DEL [ENTIDAD BANCARIA], se les confiera traslado, emplazándolas en legal forma de comparecencia, y eventual contestación y seguido que sea el oportuno procedimiento, en su día, se dicte sentencia en la que:

1. Se declare resuelto el contrato de compraventa concertado entre mi mandante y la codemandada en fecha [FECHA], respecto del bien inmueble que se determina en el cuerpo de este escrito, por causa de incumplimiento imputable a dicha demandada.
2. Se condene a la codemandadaal pago deeuros como cláusula penal por el incumplimiento en la entrega del bien.
3. Se condene a la codemandada CAJA DE AHORROS DEL, al pago deeuros, correspondientes a las cantidades entregadas a cuenta por mi mandante, más el interés legal desde cada uno de los pagos hasta su efectiva devolución.
4. Se condene a los codemandados al reembolso de las costas procesales.

Es justicia de hacerse en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a

========================================================================
