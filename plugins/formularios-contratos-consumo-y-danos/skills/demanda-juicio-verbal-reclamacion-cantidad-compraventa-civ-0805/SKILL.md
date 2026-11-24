---
name: demanda-juicio-verbal-reclamacion-cantidad-compraventa-civ-0805
description: "Demanda de juicio verbal de reclamación de cantidad por compraventa, obra, contrato mixto o atípico. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio verbal de reclamación de cantidad por compraventa, obra, contrato mixto o atípico

> Formulario **CIV-0805** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio verbal de reclamación de cantidad por compraventa, obra, contrato mixto o atípico» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio verbal de reclamación de cantidad por compraventa, obra, contrato mixto o atípico” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:demanda-juicio-verbal-reclamacion-cantidad-compraventa-civ-0805`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (7 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] NÚMERO (4 veces)
- [ ] FECHA (3 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] NOMBRE DE LA PARTE (2 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] Nº DE FINCA (2 veces)
- [ ] CALLE
- [ ] LUGAR
- [ ] MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] Nº
- [ ] Nº DE FOLIO
- [ ] OBJETO DEL CONTRATO
- [ ] SEDE

## Normas que cita el formulario

- art. 51.1 LEC
- art. 85.1 LOPJ
- art. 250.2 LEC
- art. 437.1 LEC
- art. 5 Ley Orgánica 1/2025
- art. 1088 CC
- art. 1445 CC
- art. 1258 CC
- art. 394 LEC
- art. 7.2 Ley 10/2012
- art. 32 LEC
- art. 728 LEC
- art. 728.1 LEC
- art. 728.2 LEC
- art. 529.3 LEC
- art. 727.5 LEC
- art. 42.8 LH
- art. 732.2 LEC

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] Q.P.T.R.C.»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] Q.P.T.R.C.

D/Dª [NOMBRE Y APELLIDOS] Procurador/a de los Tribunales, en representación de la sociedad [DENOMINACIÓN SOCIAL], según acredito por certificación del registro electrónico de apoderamientos judiciales (o mediante designación apud acta ante el Letrado de la Administración de Justicia de [LOCALIDAD]) y copia digitalizada del poder de representación del poderdante que acompaño, bajo la dirección letrada de D/Dª. [NOMBRE Y APELLIDOS], Abogado/a del Iltre. Colegio de [LOCALIDAD], ante el Tribunal comparezco y como mejor en derecho proceda DIGO:

Que en la representación que ostento formulo demanda de juicio verbal de reclamación de cantidad de [IMPORTE] euros, solidariamente contra la entidad mercantil «A, SA», con domicilio social en esta ciudad, calle [CALLE], y contra la entidad mercantil «C, SA», la cual fundo en los siguientes:

Hechos

Primero.– Mi mandante es una empresa que se dedica a la fabricación de obras de carpintería metálica tales como puertas, ventanas, etc.

Mi principal y las entidades demandadas «A, SA» y «C, SA», la primera en su calidad de constructora y la segunda como promotora, suscribieron en fecha [FECHA] un contrato privado en virtud del cual mi representada se obligaba a entregar la carpintería para las ventanas de 20 viviendas y zonas comunes, por un importe de [IMPORTE].

Esta obligación, ya se había asumido frente a la demandada «A, SA», en virtud de otro contrato anterior que fue incumplido por la constructora y cuya exigibilidad se mantuvo en el contrato arriba indicado tal como es de ver en su cláusula 12ª la cual establece claramente que «en ningún caso se entenderá que este contrato sustituye al anterior de [OBJETO DEL CONTRATO], suscrito entre la entidad «A, SA» y «B, SA» salvo en lo expresamente pactado.»

Segundo.– En el pacto nº [NÚMERO] del contrato aportado como doc. nº 1, la entidad demandada «C, SA» en su calidad de promotora se obligaba al pago de las diversas sumas que pudiera adeudar la constructora garantizándose su cobro mediante retenciones a la constructora. Al mismo tiempo y a favor de mi mandante asumía la obligación de prestar un aval.

Tercero.– En fecha [FECHA], mi principal efectuó la entrega de las ventanas de los dos últimos pisos, tal como se había convenido en el contrato. Es el importe de esta última entrega el que se reclama en este proceso puesto que la promotora satisfizo el resto de la obra en los términos convenidos en el contrato. No obstante, presentada la factura nº [NÚMERO], correspondiente a la última entrega que fue plenamente aceptada por la entidad «C, SA», según albarán que se adjunta, no se procedió al pago del precio pactado (acompaño como doc. nº 3 copia del albarán y como doc. nº 4 copia de la citada factura).

Cuarto.– Verificado el impago, mi principal dirigió también una reclamación contra la constructora, la entidad «A, SA», la cual contestó al mismo indicando que la promotora había hecho uso de su derecho de retención (acompaño el requerimiento como doc. nº 5).

Quinto.– Mi principal al personarse en la obra ha tenido conocimiento de que se encuentra acabada y de que la promotora ha puesto a la venta las últimas viviendas, por lo que esta parte se ve en la necesidad de interesar que se adopte una medida cautelar a fin de evitar el riesgo de que se produzca la transmisión irrecuperable del dominio sobre dichos bienes y por consiguiente que se frustre la efectividad de la sentencia estimatoria de la pretensión de la demanda.

Sexto.- Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento nº [Nº DE DOCUMENTO]

Fundamentos de derecho procesal

Competencia.–

Son competentes los Tribunales de Instancia de esta ciudad, por ser el lugar del domicilio de las demandadas al amparo del art. 51.1 de la LEC, en relación con lo dispuesto en el art. 85.1º LOPJ.

Procedimiento.–

Teniendo en cuenta que la pretensión que se ejercita es una reclamación de cantidad su tramitación debe acomodarse a la clase de juicio que proceda por razón de la cuantía, que en este caso, al no exceder de 15.000 euros, es el juicio verbal (art. 250.2 de la LEC).

Cumplimiento de los requisitos de procedibilidad.–

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 en relación con el art. 437.1 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

Fundamentos de derecho sustantivo

Primero.– Mi representada está legitimada activamente, ya que es acreedora de la contraprestación y ha cumplido en tiempo y forma con sus obligaciones contractuales (arts. 1088 y 1089 del CC).

Segundo.– Los demandados están legitimados pasivamente; así, la entidad «A, SA» por ser la constructora de los edificios y quien encargó a mi principal la realización de las ventanas, y la entidad «C, SA», por ser la promotora de las viviendas y haber asumido solidariamente el pago de las cantidades adeudadas por la constructora en el contrato que acompaña a esta demanda.

Aunque mi mandante desconoce el estado de las relaciones entre la constructora «A, SA», y la promotora «C, SA», entiende que la obra ha sido entregada a la promotora, no sólo porque así se lo ha hecho saber la constructora al contestar al requerimiento sino porque sólo en este caso, se comprende que la promotora haya anunciado públicamente la venta de los últimos pisos.

Tercero.– Con independencia de que se califique el contrato como contrato de compraventa, de arrendamiento de obra o mixto, o incluso como un contrato atípico, mi principal ostenta la condición de acreedora puesto que ha cumplido con las obligaciones que resultaban de lo pactado y el contrato existe desde que una o varias personas consienten en obligarse, respecto de otra u otras, a dar alguna cosa o a prestar algún servicio (arts. 1445, 1544 y 1254 del CC) y obliga no sólo al cumplimiento de lo expresamente pactado sino también a todas las consecuencias que, según su naturaleza, sean conformes a la buena fe, al uso y a la ley (art. 1258 del CC).

Cuarto.– Cabe poner de relieve que el contrato que aquí se acompaña se celebró cuando la obra ya estaba a punto de finalizarse, y vino motivado por los continuos retrasos en el pago de la constructora que finalmente dejó de abonar a mi principal parte de las obras de carpintería metálica incumpliendo con ello el contrato.

Esta situación de insolvencia obligó a la promotora a asumir el pago del saldo pendiente, previa constitución a su favor de un derecho de retención. Por lo demás, para mayor garantía se dispuso la prestación por parte de la promotora de un aval que finalmente no se constituyó y que tenía la finalidad de evitar que la obra se paralizara por impago de la constructora a sus proveedores.

Costas

Al amparo del artículo 394 de la LEC, las costas deben imponerse a la parte cuyas pretensiones sean totalmente desestimadas.

Por todo lo expuesto,

SUPLICO AL TRIBUNAL: Tenga por presentado este escrito con los documentos acompañados y sus copias, lo admita, me tenga por comparecido y parte en la representación que ostento de [NOMBRE DE LA PARTE] entendiéndose conmigo las sucesivas diligencias. Y tenga por formulada demanda de juicio verbal civil en reclamación de la cantidad de [IMPORTE] euros contra las entidades demandadas [NOMBRE DE LA PARTE] cuyas demás circunstancias constan en el encabezamiento de este escrito y, tras emplazar a las demandadas y seguir los trámites correspondientes, dicte sentencia por la que se condene solidariamente a las demandadas a abonar la cantidad de [IMPORTE] euros más los intereses legales que procedan y a las costas del proceso.

[OPCIONAL — incluir si procede]

OTROSÍ PRIMERO DIGO.–Que estando la presente demanda sujeta al abono de la tasa por el ejercicio de la potestad jurisdiccional fijada por la Ley 10/2012, de 20 de noviembre, modificada por Real Decreto Ley 3/2013, de 22 de febrero, y Ley 25/2015, de 28 julio, y por Orden HAP/861/2015, de 7 de mayo, siendo mi representada persona jurídica no exenta, se acompaña a la presente demanda como documento nº [Nº DE DOCUMENTO] la correspondiente autoliquidación con el ejemplar para la Administración de Justicia debidamente validado y en el que consta el pago de la cantidad de 150 euros correspondiente a la cuota fija, sin que se incluya la cuota variable prevista en el artículo 7.2 de la Ley 10/2012 al haber sido declarado inconstitucional y nulo por la STC 140/2016, de 21 de julio.

SUPLICO AL TRIBUNAL: que tenga por hecha la anterior manifestación y por expresada la voluntad de subsanación de esta parte.

[OPCIONAL — incluir si procede]

OTROSÍ SEGUNDO DIGO: que se acompaña en anexo relación de documentos, debidamente foliados y con índice electrónico, para su debida localización y consulta.

SUPLICO AL TRIBUNAL tenga hecha esta manifestación a los efectos oportunos y por aportados los documentos relacionados en el anexo.

[OPCIONAL — incluir si procede]

OTROSÍ TERCERO DIGO: Que aun no siendo preceptiva la intervención de Procurador y Abogado, dado que la cuantía del proceso no excede de 2.000 euros, manifiesto mi intención de intervenir asistido por dichos profesionales, lo cual comunico al Tribunal en cumplimiento de lo establecido en el art. 32 de la LEC (en el caso de que la demanda no exceda de 2.000 euros, podrá la parte comparecer por sí misma, es decir, sin necesidad de estar asistida por Procurador y Abogado. Si fuera el caso, pero quiere que intervengan en el proceso dichos profesionales, deberá hacerlo constar en la demanda).

SUPLICO AL TRIBUNAL: que tenga por hecha la anterior manifestación y por expresada la voluntad de subsanación de esta parte.

[OPCIONAL — incluir si procede]

OTROSÍ CUARTO DIGO: Que solicito que en este juicio verbal se acuerde, bajo mi responsabilidad, la anotación preventiva de la demanda, ya que concurren los requisitos establecidos en el art. 728 de la LEC, en los términos que seguidamente pasamos a exponer.

a) Peligro por la mora procesal: La falta de liquidez de la constructora es evidente tal como viene reconocido en el contrato que se acompaña con esta demanda como doc. nº [NÚMERO] Así, en la estipulación [Nº] y como circunstancia preliminar se hace referencia a las relaciones entre la constructora «AAA, SA» y la actora, subcontratada para efectuar las obras de carpintería metálica así como a la existencia, en aquel momento, de cantidades impagadas por la contratista las cuales en el momento de la firma fueron abonadas por la promotora.

Esta situación era conocida por la promotora «XXX, SA», quien dado su interés en continuar las obras suscribió el contrato cuyo cumplimiento se pretende en este proceso y asumió solidariamente la obligación del pago de la deuda, para lo cual se reservaba un derecho de retención por las cantidades que debía abonar a la contratista. Y, para garantizar frente a mi mandante, el cumplimiento de su obligación, se comprometía a prestar un aval o fianza bancaria por importe de [IMPORTE]... euros, que finalmente no se ha constituido.

Acompaño a esta demanda la carta recibida por mi mandante en la que la promotora le comunica la imposibilidad de prestar el aval, por habérselo denegado la entidad bancaria «[DENOMINACIÓN SOCIAL], SA» con la que mantiene habituales relaciones bancarias (doc. nº 6).

El riesgo de que se produzca una insolvencia es aún mayor desde que la promotora ha modificado la publicidad inicial al anunciar la venta los dos últimos pisos de la promoción a precios más ventajosos por haber finalizado la construcción (así se acredita con el Acta notarial que acompaño a esta demanda como doc. nº 7).

Esta actividad conlleva el peligro de que si finalmente las viviendas fueran enajenadas a terceros antes de que recaiga sentencia definitiva, nos hallaríamos ante un supuesto de materialización de la transmisión del dominio con todas sus consecuencias creándose una situación jurídica difícilmente reversible que podría hacer perder a la sentencia su efectividad. Cabe recordar que el riesgo es aún mayor si se tiene en cuenta que mi principal, creyó de buena fe en la solvencia de la promotora y por esta razón cumplió con lo convenido pese a que ésta no prestó el aval o fianza por las cantidades objeto de este proceso tal como se había obligado en el contrato.

Lo dicho hasta ahora, sólo puede llevar a la conclusión de que se cumple el primer requisito en el art. 728.1 de la LEC, sin que se dé el caso de que se pretenda alterar situaciones de hecho consentidas por el solicitante durante largo tiempo, y que con arreglo al apartado segundo impedirían su adopción.

b) Apariencia de buen derecho. Mi mandante aporta con esta demanda, un principio de prueba documental de la que se desprende que la pretensión que se deduce en este proceso ha de prosperar, y en consecuencia, que seguidos los trámites procesales preceptivos, se dictará sentencia estimatoria de la demanda. Entendemos por lo tanto que concurre también este segundo requisito exigido en el art. 728.2 de la LEC.

c) Caución. Esta parte se ofrece a aportar aval bancario en los términos que establece el art. 529.3 de la LEC, en la cuantía de [IMPORTE] euros, por entender que este importe es suficiente para responder de los posibles daños y perjuicios que la adopción de la medida pudiera ocasionar en el patrimonio de las demandadas o en la que prudencialmente se determine por este Tribunal, dando así cumplimiento a la exigencia del 728.3 y 732.3 de la LEC, la cual se hará efectiva tan pronto se acuerde por el Tribunal.

d) Respecto a la medida interesada, esta parte considera que debe procederse a la anotación preventiva de demanda, en los términos que establece el art. 727.5 de la LEC en relación con el art. 42.8 de la LH y 139 de su Reglamento, a fin de que se tome razón de esta demanda en el folio registral de la finca inscrita en el Registro de la Propiedad de [LOCALIDAD], nº [NÚMERO] En efecto, tratándose de materiales suministrados para la construcción de las viviendas, entendemos aplicables estos preceptos pues, como pone de relieve la STS de 21 de julio de 2000, rec. 2883/1995, que a su vez, cita la STS de 21 de septiembre de 1987, el concepto amplio de crédito refaccionario, no queda limitado, «como entendía la doctrina tradicional, a un préstamo de dinero destinado a la construcción o reparación de un edificio, sino comprensivo de todo crédito causalmente conectado con obras de reparación, construcción o mejora de bienes». Cabe también citar la STS de 9 de julio de 1993, rec. 3494/1990, que considera créditos refaccionarios todos los que «hayan contribuido por modo directo al resultado de una construcción, reparación, conservación o mejora de un inmueble».

Por último, en cumplimiento de lo dispuesto en el art. 732.2 de la LEC acompañamos copia de los documentos nº 1, 2, 3, 4, 5 y 6, cuyos originales se aportan junto a la demanda, a fin de que debidamente testimoniados junto con esta demanda en la que, por otrosí, se solicita la adopción de la medida cautelar de anotación preventiva de demanda, se unan a la pieza separada de medidas cautelares, ya que acreditan los presupuestos que autorizan su adopción (si no se dispusiera de prueba documental o debiera proponerse además otros medios de prueba distintos, se ofrecerá por otrosí la práctica de estos medios que permitirán acreditar los presupuestos que autorizan la adopción de las medidas cautelares, pues para el demandante en este momento precluye la posibilidad de proponer prueba en el incidente).

SUPLICO AL TRIBUNAL: Tenga por solicitada la adopción de esta medida y tras los trámites oportunos se sirva acordar la anotación preventiva de esta demanda en el Registro de la Propiedad de [LOCALIDAD], respecto de las dos fincas nos [Nº DE FINCA] y [Nº DE FINCA], folios [Nº DE FOLIO], respectivamente, previa prestación de aval en la cuantía de [IMPORTE] euros o en la que el Tribunal acuerde prudencialmente.

[OPCIONAL — incluir si procede]

OTROSÍ QUINTO DIGO Que esta parte manifiesta su voluntad expresa de cumplir con todos los requisitos exigidos para la validez de la demanda y demás actos procesales ofrece la subsanación de forma inmediata de cualquier defecto en el que pudiera haber incurrido, a requerimiento del Tribunal, todo ello a los efectos prevenidos en el artículo 231 de la Ley de Enjuiciamiento Civil.

SUPLICO AL TRIBUNAL: que tenga por hecha la anterior manifestación y por expresada la voluntad de subsanación de esta parte.

En [LUGAR], a [FECHA].

Procurador/a	Abogado/a

Fdo. D. Dña. [NOMBRE Y APELLIDOS]: Fdo. D. Dña. [NOMBRE Y APELLIDOS]:

========================================================================
