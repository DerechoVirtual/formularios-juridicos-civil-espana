---
name: apelacion-trafico-error-factico-e-infraccion-material-civ-1389
description: "Apelación de tráfico por error fáctico e infracción material, con vista (pleito previo al 20-3-2024). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Apelación de tráfico por error fáctico e infracción material, con vista (pleito previo al 20-3-2024)

> Formulario **CIV-1389** del plugin **Recursos civiles: reposición, apelación, casación y queja** (`formularios-recursos-civiles`) · Civil › Recursos · normativa revisada el 24-11-2026.

## Qué es

Escrito de interposición de recurso de apelación ante el Tribunal de Instancia sobre responsabilidad derivada de la circulación de vehículos a motor en cuanto a la valoración de la actividad probatoria, inaplicación del Código de Circulación, inaplicación indebida del baremo anexo a LRCSVM e interpretación errónea del artículo 20 de la Ley de Contrato de Seguro, solicitando celebración de vista y aportando resolución judicial dictada con posterioridad al acto del juicio, notificada después de la sentencia de instancia. Régimen anterior al RDL 6/2023, aplicable a procesos incoados con anterioridad al 20/03/2024.

Es un modelo de tipo **recursos**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Apelación de tráfico por error fáctico e infracción material, con vista (pleito previo al 20-3-2024)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Apelación de tráfico por error fáctico e infracción material, con vista (pleito previo al 20-3-2024)” para mi caso». También puedes invocarla directamente con `/formularios-recursos-civiles:apelacion-trafico-error-factico-e-infraccion-material-civ-1389`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-recursos-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Recursos civiles: reposición, apelación, casación y queja) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] FECHA (6 veces)
- [ ] IMPORTE (4 veces)
- [ ] AÑO (3 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] Nº (2 veces)
- [ ] ASEGURADORA
- [ ] FALLO DE LA SENTENCIA
- [ ] LUGAR
- [ ] MATRÍCULA
- [ ] Nº DE PROCEDIMIENTO
- [ ] SECCIÓN
- [ ] SEDE
- [ ] ÓRGANO

## Normas que cita el formulario

- art. 458.1 LEC
- art. 316.1 LEC
- art. 1.103 CC
- art. 2.3 CC
- art. 20.8.º LCS
- art. 20.4.º LCS
- art. 398.2 LEC
- art. 276 LEC
- art. 464.2 LEC

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

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, que actúa en nombre y representación de la Compañía de Seguros [ASEGURADORA], según ya queda acreditado en autos de juicio ordinario n.º [Nº DE PROCEDIMIENTO]/[AÑO], en los mismos comparezco y como mejor en Derecho proceda DIGO:

Que el pasado día [FECHA] se me ha notificado la sentencia de fecha [FECHA], recaída en las presentes actuaciones, por la que se acuerda [FALLO DE LA SENTENCIA], y estimando la misma gravosa para los intereses de mi mandante, dicho sea en términos de defensa, dentro del plazo de veinte días legalmente establecido en el art. 458.1 LEC, INTERPONGO RECURSO DE APELACIÓN contra dicha resolución.

REQUISITOS PROCESALES

I

Se presenta este escrito de interposición ante ese Tribunal, que es el tribunal que ha dictado la sentencia que se recurre, con arreglo al art. 458.1 LEC.

II

Se presenta este escrito de interposición dentro del plazo de veinte días contados desde el día siguiente a la notificación de la resolución impugnada (art. 458.1 y 3 LEC).

III

Mi representada está legitimada, en tanto que parte que niega su obligación de reparación tal y como se fijó crédito de la parte actora, y tiene perjuicio o gravamen por la resolución impugnada, puesto que se condena al cumplimiento, mediante el pago de una indemnización (arts. 10 y 448.1 LEC).

IV

Las exigencias de postulación se llenan para este escrito de interposición, ya que está comparecida esta parte mediante Procurador de los Tribunales, y asistida de abogado en ejercicio, ambos colegiados y habilitados para ejercer ante el Tribunal (arts. 23.1 y 31.1 LEC), y en el momento que cambie la competencia funcional, al notificarse la resolución que ordene la remisión de los autos a la Audiencia Provincial de [LOCALIDAD], se personará esta parte con el Procurador/a D./Dña. [NOMBRE Y APELLIDOS], habilitado ante dicho órgano.

FUNDAMENTOS DEL RECURSO

PRIMERO.- Valoración de la actividad probatoria.

La impugnación de la resolución apelada se basa en la respetuosa disconformidad de esta parte con que se extraiga la versión fáctica de las manifestaciones en su confesión judicial de la parte actora, que ciertamente tuvo necesaria intervención personal en los hechos que son objeto del litigio, ya que fue quien conducía el ciclomotor que colisionó contra el automóvil que aseguraba mi mandante, pero que le son enteramente beneficiosos, cual el dato de que el vehículo matrícula [MATRÍCULA], que guiaba D./Dña. [NOMBRE Y APELLIDOS], al que intentaba rebasar, procedió a girar a su izquierda en una intersección sin accionar el intermitente, y que circulaba en paralelo, con lo que infringe la regla del art. 316.1 LEC, y no se conjuga con otro medio probatorio válido.

Y es que la otra única apoyatura probatoria valorada es la pericial técnica del carrocero Sr./a. [NOMBRE Y APELLIDOS], que aventura que la entidad de los daños en el lateral del vehículo que conducía el codemandado D./Dña. [NOMBRE Y APELLIDOS], son compatibles con un golpe longitudinal desde atrás hacia delante, y no con golpe localizado y no con la marca longitudinal que hubiera deparado, puesto que tal razonamiento se extrapola indebidamente a que los vólidos iban en paralelo y el que deseaba girar colisionó al de su izquierda.

Las máximas de experiencia conllevan admitir que, yendo como era cierto, el ciclomotor detrás del automóvil, al intentar aquél rebasar a quien regularmente ya había alcanzado la posición de giro, golpeó de atrás adelante desde la puerta trasera hasta el piloto del lado izquierdo del que recibió, que no provocó, el impacto.

En el precedente juicio de faltas en que resultó absuelto D./Dña. [NOMBRE Y APELLIDOS], cabalmente se argumentó la carencia de prueba sobre que no se hubiera realizado la pertinente señalización luminosa para el giro a la izquierda, o de que el ciclomotor hubiera ya alcanzado la posición paralela al automóvil que procedía a adelantar, cuando éste giró.

SEGUNDO.- Inaplicación del Código de Circulación (RD [Nº] / [AÑO])

Desde el primer término de la contestación a la demanda se ha insistido en que, a pesar de que la versión del actor no es verídica, ni verosímil, y en cualquier caso, no se prueba, a su vez, está por sus mismas alegaciones acreditada la infracción reglamentaria del conductor del ciclomotor que demanda, dado que el art. del Código de Circulación señala que los ciclomotores deberán circulara por el arcén o el lado derecho de la calzada.

Obviamente, si se demanda por un golpe desde el costado derecho del ciclomotor, cuando se asevera que se pretendía adelantar a un turismo, y porque éste giraba a la izquierda, se está confesando que el ciclomotor circulaba por el centro de la calzada.

Comoquiera que el ciclomotor no puede adelantar, lo que se prueba es la imprudencia de su conductor, que recibió perjuicio por su propia exclusiva culpa.

En todo caso, es evidente una concausa relevante que debiera suponer siempre, para el improbable supuesto de ratificarse la obligación de mi mandante, una compensación de culpas, empleando la doctrina acerca de la mitigación de la cuantía desde el art. 1.103 CC, y las propias previsiones del Baremo anexo TRLRCSCVM, y que esta parte cifra en el descuento del 75%, por la máxima indiligencia y descuido del que guiaba el ciclomotor.

TERCERO.- Aplicación indebida del Baremo anexo a TRLRCSCVM.

Con carácter subsidiario, se pidió en la contestación a la demanda, que para la hipótesis improbable de que se fijara la responsabilidad de mi representada, se denegase el cálculo del quantum indemnizatorio que se pedía en la demanda.

1.-En primer lugar, no puede aplicarse el Baremo aprobado para el año [AÑO], en que se presenta la demanda, ni tampoco el que estaba en vigor cuando se hizo el cálculo en la petición de responsabilidades civiles del precedente juicio de faltas, sino en todo caso, el que estaba en vigor cuando se produjo el siniestro, que es el hecho causante de la obligación reparatoria, puesto que el régimen de tasa legal, que lleva su actualización anual mediante Resolución de la Dirección General de Seguros, enerva la consideración de deuda de valor que deba verse liquidada a la pura prudencia judicial, viniendo el nominalismo corregido por un sistema especial de devengo de intereses moratorios. Por otro lado, si no se aplica en Baremo de 1998, en cuyos últimos días acaeció el siniestro, se produciría una retroactividad de norma que no lo prevé (art. 2.3 CC), puesto que hasta entonces los días de baja se tasaban legalmente con arreglo a dos conceptos, sin punto intermedio, que eran los de curación, y los de ingreso hospitalario, mientras que aquí se pretende con base a concepto de posterior introducción normativa, que es la curación que incapacita para tareas habituales o que no lo hace.

Por consiguiente, han de ser [IMPORTE] euros el valor del día de baja sin ingreso hospitalario.

2.-Si bien se expurgan de la reclamación del demandante lesiones permanentes que decían aquejarle, y que de la pericial médica de designación judicial no resultan, en cuanto a las que se tienen por acreditadas, se utilizan la puntuación media del arco del Baremo, sin que se motive la razón para ello, cuando la graduación, a la luz del mismo informe del Dr./a.

De todas formas, la sentencia no aplica la fórmula del Baremo adecuadamente, ya que multiplica los puntos de indemnización básica por el valor del punto que proporciona la demanda, y si no puede ser, porque obedece a norma posterior a la vigente en el momento del siniestro, de todas formas, debe atenderse a la Tabla II en que el valor del punto es progresivo, y no el mismo, según se incrementan los puntos, además de la clasificación del perjudicado atendiendo a la edad.

Igualmente es menester aplicar la fórmula del Baremo, por ser varias las lesiones permanentes a las que se asigna puntuación, excluyendo los puntos por perjuicio estético, que simplemente se sumará, y que siendo el mínimo del perjuicio ligero del Capítulo especial de la Tabla VI no es objeto de comentario crítico.

3.- En último término, aunque la sentencia deniega el factor corrector por incapacidad permanente parcial, lo reconoce por ingresos económicos, y no consta en autos más constancia que el perjudicado trabajaba de camarero en el Restaurante [ÓRGANO], pero no está demostrado cuáles sean sus ingresos netos por trabajo reales, y no se considera posible ponderar un porcentaje en el tramo hasta el 10% de incrementos de la puntuación de lesiones, siquiera el mínimo, a falta de justificación de que en el periodo de referencia existían rentas del trabajo superiores a [IMPORTE] euros.

CUARTO.- Interpretación errónea del art. 20 Ley de Contrato de Seguro.

En el fallo de la sentencia recurrida se condena al pago de intereses moratorios al tipo del 20% desde la fecha del siniestro, habiéndose razonado en el fundamento de derecho [Nº], que han transcurrido más de dos años desde aquélla.

En primer lugar, esta parte, al negar obligación, no puede haberse constituido en mora, pero si la obligación se declarara, conforme al art. 20.8.º LCS, concurriría una causa justificada que hace inimputable el no haber resarcido, cual la provocación de un juicio penal pleito, en que D./Dña. [NOMBRE Y APELLIDOS], mi asegurado, resultó absuelto, pretendiendo un reclamación indemnizatoria abusiva, lo que dispensará de que la iliquidez del crédito puede jugar para devengo de intereses

En segundo lugar, si han transcurrido más de dos años, sólo puede atribuirse a la conducta del supuesto perjudicado que, no conformándose con instar un proceso penal, acudió a la segunda instancia frente a la sentencia absolutoria, y en cualquier caso, los términos literales del art. 20.4.º LCS, no dejan lugar a dudas de que el interés del tipo del 20% no corre más que desde la fecha en que se traspasan esos dos años de demora, es decir, desde [FECHA], mientras que el periodo previo corre al tipo de interés legal dinero incrementado en el cincuenta por ciento.

QUINTO.- Costas.

En caso de estimación total o parcial del recurso, cada una de las partes se haría cargo de sus costas de esta apelación (art. 398.2 LEC).

En su virtud,

SUPLICO A TRIBUNAL

Que, teniendo por presentado este escrito con su copia, y documento acompañado, de lo que se ha dado traslado al Procurador de la parte contraria en la forma que previene el art. 276 LEC, se sirva tener por INTERPUESTO recurso de apelación contra la sentencia de fecha [FECHA], y se remitan los autos a la Audiencia Provincial de [LOCALIDAD], previo emplazamiento legal para comparecer ante la misma, y

SUPLICO A LA AUDIENCIA PROVINCIAL que, seguido que sea el legal procedimiento, dicte sentencia que revoque la de instancia, absolviendo libremente a esta parte, o con carácter subsidiario, reduzca la condena, en base a la concurrencia de culpas, y a los términos de cálculo conforme al Baremo alegados, sin que existan intereses de mora especial, y en todo caso, que sólo sean del tipo anual del 20% para el devengo del periodo desde el [FECHA] hasta que deba producirse el pago.

Es Justicia de hacerse en [LUGAR], a [FECHA].

OTROSÍ PRIMERO DIGO, que se acompaña a este escrito resguardo acreditativo del pago del depósito de 50 euros en la Cuenta de Depósitos y Consignaciones del Tribunal al que se dirige, conforme exige la disposición adicional 15.ª LOPJ, por lo que,

SUPLICO AL TRIBUNAL que tenga por causada la manifestación anterior a los efectos oportunos.

OTROSÍ SEGUNDO DIGO que de acuerdo con lo prescrito en el artículo 449.3 de la Ley de Ritos, al encontrarnos ante un proceso en que se pretende la condena a indemnizar daños y perjuicios derivados de la circulación de vehículos de motor, se acredita mediante la aportación del correspondiente resguardo de ingreso en la Cuenta de Depósitos y Consignaciones judiciales, haber constituido depósito del importe de la condena, que asciende a la suma de [IMPORTE] euros, más los intereses y recargos exigibles, que se calculan en [IMPORTE] euros, por lo que nuevamente,

SUPLICO AL TRIBUNAL que tenga por hecha la anterior manifestación a los oportunos efectos.

OTROSÍ TERCERO DIGO: Se acompaña al escrito de interposición testimonio del auto dictado por la Sección [SECCIÓN] de la Audiencia Provincial, en que conociendo de apelación contra auto del mismo Tribunal, que acordó no reponer el de despacho de ejecución, revoca la resolución de liquidar intereses al tipo del 20% anual desde la fecha del siniestro, debiendo hacerse desde que pasaron dos años sin pago.

El documento es resolución judicial dictada con posterioridad al acto del juicio, y notificada después de la sentencia de instancia, que se entiende debe ser aceptada por la interpretación integrada de los arts. 271 y 463.1 LEC.

OTROSÍ CUARTO DIGO: Se solicita la celebración de vista, como autoriza el art. 464.2 LEC.

SUPLICO A LA AUDIENCIA PROVINCIAL que, teniendo por causadas las manifestaciones antecedentes a los efectos oportunos, se sirva admitir la unión del documento acompañado, así como señalar la celebración de vista, como es procedente en Justicia que reitero.

OTROSÍ QUINTO DIGO, que de acuerdo con la Disposición Transitoria Segunda del Real Decreto-Ley 6/2023, el presente recurso se interpone ante el Tribunal que ha dictado la resolución objeto de recurso por ser aplicable la tramitación vigente al momento en que fue presentada la demanda y ser esta anterior a la reforma que entró en vigor el 20/03/2024, por lo que SOLICITO, tenga por realizada tal manifestación.

Firma de Abogado/a	Firma de Procurador/a

========================================================================
