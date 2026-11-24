---
name: demanda-propietario-suspender-obra-nueva-hecha-sin-civ-0612
description: "Demanda de un propietario para suspender una obra nueva hecha sin consentimiento de la comunidad. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de un propietario para suspender una obra nueva hecha sin consentimiento de la comunidad

> Formulario **CIV-0612** del plugin **Comunidades de propietarios** (`formularios-comunidades-de-propietarios`) · Civil › Propiedad horizontal · normativa revisada el 24-11-2026.

## Qué es

Demanda al Tribunal de Instancia de suspensión de obra nueva. La demanda se interpone por el propietario de una vivienda contra la Comunidad de Propietarios de la que forma parte ante la realización en los elementos comunes de obras inconsentidas, concretamente, por introducir en las obras proyectadas y aprobadas por la Junta de Propietarios, modificaciones no aprobadas consistentes en:1º) La apertura de un hueco de ventana en la fachada común al viento norte del inmueble, al piso bajo derecha; 2º) La modificación externa ampliatoria hacia terreno común de una cochera o garaje del mismo bajo derecha;3º) La construcción de un balcón en el piso primero derecha en fachada común al viento este; y 4º) Una acera que quiere rodear la casa, también al este, que tiene más anchura de un metro, sobre terreno común, y que ciega un patio común de desagüe.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de un propietario para suspender una obra nueva hecha sin consentimiento de la comunidad» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de un propietario para suspender una obra nueva hecha sin consentimiento de la comunidad” para mi caso». También puedes invocarla directamente con `/formularios-comunidades-de-propietarios:demanda-propietario-suspender-obra-nueva-hecha-sin-civ-0612`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-comunidades-de-propietarios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Comunidades de propietarios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] DENOMINACIÓN DE LA COMUNIDAD (7 veces)
- [ ] LOCALIDAD (7 veces)
- [ ] Nº DE DOCUMENTO (7 veces)
- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] NÚMERO (5 veces)
- [ ] FECHA (4 veces)
- [ ] Nº (4 veces)
- [ ] CALLE (2 veces)
- [ ] FECHAS
- [ ] IMPORTE
- [ ] LUGAR
- [ ] PUERTA
- [ ] SEDE

## Normas que cita el formulario

- art. 45 LEC
- art. 85.1 LOPJ
- art. 52.1.1.º LEC
- art. 51.2 LEC
- art. 250.1.5 LEC
- art. 1.631 LEC
- art. 250.1.5.º LEC
- art. 251.11.ª LEC
- art. 5 Ley Orgánica 1/2025
- art. 18.1 LPH
- art. 394.1 LEC
- art. 339 LEC
- art. 356 LEC

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

D./Dña. [NOMBRE Y APELLIDOS], Procurador de los Tribunales, que actúa en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS], provista de D.N.I. número [NÚMERO], con domicilio en [LOCALIDAD] (indicar datos y circunstancias de identificación del demandante) [NOMBRE Y APELLIDOS], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], a quien asiste el Letrado en ejercicio abajo firmante D./Dña. [NOMBRE Y APELLIDOS], con despacho profesional en [LOCALIDAD], ante el Tribunal comparezco y como mejor proceda en Derecho, DIGO:

Que por medio del presente escrito vengo a formular DEMANDA DE SUSPENSIÓN DE OBRA NUEVA, contra la COMUNIDAD DE PROPIETARIOS DE LAS CASAS SEÑALADAS CON NÚMEROS [Nº] y [Nº] y [Nº] DE LA CALLE [CALLE] DE [LOCALIDAD],en base a los siguientes hechos y consideraciones jurídicas:

HECHOS

PRIMERO.- Mi mandante es propietaria de la vivienda sita en planta alta, puerta [PUERTA], de la casa n.º [NÚMERO], de la calle [CALLE] de la localidad de [LOCALIDAD], formando parte de la Comunidad de propiedad horizontal [DENOMINACIÓN DE LA COMUNIDAD], a cuya demostración adjunto copia de la escritura de compraventa como documento n.º [NÚMERO].

Dicha Comunidad forma parte de la Comunidad demandada de las casas números [Nº], constituida el [FECHA], a fin de gestionar la titularidad común de todo el bloque de edificios y urbanización (se aporta copia del acta de constitución como documento n.º [NÚMERO]).

SEGUNDO.- La Comunidad demandada, aprovechándose de que la Comunidad [DENOMINACIÓN DE LA COMUNIDAD], de la que forma parte el piso de la actora, así como las otras dos Comunidades, habían aprobado en Junta de Propietarios la ejecución de obras en elementos comunes con su distribución porcentual de contribución al gasto, procedió a ejecutar las mismas, pero introduciendo modificaciones en la obra proyectada, las cuales no estaban aprobadas; a estas modificaciones, una vez que tuvo conocimiento la actora, se opuso. (Se adjunta cartas recibidas por el Administrador de la Comunidad [DENOMINACIÓN DE LA COMUNIDAD], que se le certificaron por el servicio de correos, constando los acuses de recibo, como documentos números [Nº DE DOCUMENTO] y [Nº DE DOCUMENTO]).

TERCERO.- Las alteraciones inconsentidas que suponen obra nueva, la cual no está concluida, son:

1.º) La apertura de un hueco de ventana en la fachada común al viento norte del inmueble, al piso bajo derecha.
2.º) La modificación externa ampliatoria hacia terreno común de una cochera o garaje del mismo bajo derecha.
3.º) La construcción de un balcón en el piso primero derecha en fachada común al viento este, y
4.º) Una acera que quiere rodear la casa, también al este, que tiene más anchura de un metro, sobre terreno común, y que ciega un patio común de desagüe.

Se aporta a su acreditación material fotográfico disponible por actuación de la Policía Local, a requerimiento de la Sección de Instrucción del TI, en base a las diligencias abiertas por denuncia de esta parte, como documento n.º [NÚMERO].

Que tales obras no son de las autorizadas, se prueba con el proyecto aportado a la Delegación de Vivienda de [LOCALIDAD], y el adjunto a la licencia de obras del Ayuntamiento de [LOCALIDAD], que son anexos documentos números [Nº DE DOCUMENTO] y [Nº DE DOCUMENTO].

CUARTO.- La parte actora manifiesta que, previo a la presentación de la presente demanda, se han llevado a cabo negociaciones con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad, y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria; incluyéndose entre las acciones realizadas el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución.

Finalmente, mi representado envió un requerimiento fehaciente al demandado con fecha [FECHA], fijando un plazo de 30 días naturales para llegar a un acuerdo amistoso, a través del abogado que firma este escrito, el cual fue contestado por el demandado por el mismo medio, rechazando el acuerdo/ habiendo sido solo posible un acuerdo parcial, viéndonos en la necesidad de acudir a la presente vía judicial, respecto a los extremos de la controversia en los que se mantiene la discrepancia.

Acompaño como documento nº [Nº DE DOCUMENTO], el requerimiento efectuado y como documento nº [Nº DE DOCUMENTO], la contestación del demandado.

FUNDAMENTOS DE DERECHO

I.- COMPETENCIA.

La competencia objetiva corresponde a la Sección Civil del Tribunal de Instancia (art. 45 LEC, en relación con lo dispuesto en el art. 85.1º LOPJ), y la territorial al del lugar en que está sito el inmueble objeto de acción real, conforme al art. 52.1.1.º LEC, que de todas las maneras es la sede la comunidad demandada, atendiendo al art. 51.2 LEC.

II.- PROCEDIMIENTO.

El prescrito en los arts. 437 y ss. LEC, según asignación por la materia del art. 250.1.5º LEC.

Aunque donde se acomete la obra nueva no es algo ajeno a la demandante, resulta mayoritaria la doctrina de las sentencias de las Audiencias Provinciales que reputaba la elección del cauce procesal, entre los desaparecidos interdictos de obra nueva, retener o recobrar, una alternativa del justiciable, por la literalidad del derogado art. 1.631 LECiv 1881, por historia, por economía procesal, por tutela judicial efectiva y porque no se consagre el absurdo de permitir la demolición (retener y recobrar) en un juicio sumario que no es posible en la obra nueva, lo que luego sería catastrófico si en un plenario posterior se demostrare el "ius aedificandi".

III.- PARTES.

Mi representada se encuentra legitimada activamente por ser coposeedora de los elementos comunes del edificio en el cual posee privativamente, a título de propietaria, su vivienda, y en cuanto a la legitimación pasiva corresponde a la Comunidad demandada, por se quien ordena ejecutar la obra nueva que altera tales elementos sin consentimiento comunitario, por quien comparecerá su Presidente.

Desde siempre se ha reconocido la legitimación de los comuneros en beneficio de los derechos de la comunidad, siendo de aplicación la conocida doctrina, por ejemplo resumida en STS de 16 de abril de 1996, rec. 3130/1992.

La jurisprudencia ha venido reiteradamente proclamando que la pretensión de suspensión de obra nueva, que no define el precepto contenido en el art. 250.1.5.º LEC, como no lo hacían los contenidos en los arts. 1.663 y ss. LECiv 1881 derogada, sobre interdicto de obra nueva, corresponde a un declarativo cautelar y sumario, que ampara el dominio o cualquier otro derecho de naturaleza real, es decir, no estrictamente posesorio, enderezado a obtener un acuerdo provisional, manteniendo el "status quo ante" frente al autor de una obra de la que se predica una eventual lesión jurídica, inminente por signos concluyentes, cuya resolución tratará de evitar, tanto los perjuicios que la demolición total ulterior pueda producir, como que se frustre el futuro proceso respecto al derecho que a las partes pueda asistir.

Tratándose de un juicio verbal por razón de la materia y no por razón de la cuantía, conforme a los arts. 23.1 y 31.1 LEC, es preceptiva la intervención de procurador de los tribunales y de abogado en ejercicio, ambos habilitados ante el Tribunal, estando identificados representante y director letrado en el encabezamiento de la demanda.

IV.- CUANTÍA DE LA DEMANDA.

La cuantía de la demanda se calcula en [IMPORTE] euros, dado que el interés económico, por el objeto sumario del proceso no es el importe de la obra nueva, ni el del derecho de copropiedad afectado, sino la prestación de hacer en que consiste la suspensión que se pide (art. 251.11.ª LEC), que es de difícil medida en términos absolutos, pero en todo caso se estima supone, dado que la decisión sobre la suspensión (la prosecución definitiva resulta eventual, y ajena al proceso) representa en principio la pérdida del precio por esa porción de obra no presupuestada.

V.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

VI.- FONDO DEL ASUNTO.

Si bien existe un acuerdo de Junta de Propietarios de la Comunidad XX, a la que pertenece mi mandante, de fecha [FECHA], pacífico para las partes, que conviene la realización de obras de rehabilitación del edificio, y un proyecto de ejecución visado, y una licencia de obras, y un presupuesto con detalle, todo lo cual conoció y conoce la demandante, pues incluso suscribió el acuerdo inicial, y en idéntica fecha se confirió representación al Presidenta de la Comunidad demandada, que agrupa las Comunidades [DENOMINACIÓN DE LA COMUNIDAD], [DENOMINACIÓN DE LA COMUNIDAD] y [DENOMINACIÓN DE LA COMUNIDAD], para gestionar subvención reglamentaria al Departamento de Vivienda de [LOCALIDAD], y el [NOMBRE Y APELLIDOS] firmó, junto al resto de comuneros, la solicitud documentada, en ninguna parte se encuentran las partidas correspondientes a los cuatro puntos innovadores consignados en el ordinal tercero de los hechos de este escrito.

Resulta indiscutible que la obra nueva toca elementos comunes por naturaleza, pero al margen de que no puede conculcarse la unanimidad requerida por LPH para su modificación (art. 17.6), lo que quedará al margen de esta "litis", y ante la constancia de que ha sido ordenada por el Presidente de la Comunidad demandada, ha de condenarse a que soporte la definitiva confirmación de que ha de quedar suspendida su ejecución, procediendo luego, en su caso, las acciones en juicio plenario.

La doctrina de apelación, ya clásicamente, negó la posibilidad de acudir a la suspensión de obra nueva cuando existen acuerdos de las Juntas de Propietarios (SAP Zaragoza de 25 de septiembre de 1.969; Pontevedra de 13 de noviembre de 1.978; Barcelona de 5 de noviembre de 1.982; Lugo de 26 de noviembre de 1.985; y Huelva de 10 de abril de 1.991), por ser de "ius cogens" la aplicación del cauce a seguir para la impugnación de los acuerdos comunitarios, carácter necesario de orden público que se predica del art. 18.1 LPH, y que veda la acción interdictal como medio de ataque a un acuerdo comunitario. Pero el caso es de acuerdo que la actora no debate, del que no es disidente, ni lo impugna, sino de que, a espaldas de cualquier acuerdo comunitario, el Presidente de la Comunidad demandada aprovecha una obra consentida para introducir otras por la vía de hecho.

Existe, pues, una obra nueva no terminada, que es la que se puede y debe suspender, puesto que la construcción no ha llegado a un estado constructivamente acabado en su totalidad, y su prosecución es capaz de ocasionar perjuicio a mi principal.

Los elementos comunes innovados, que no están en absoluto acabados, ocasionan un evidente daño a mi patrocinada, puesto que por su descripción, y conforme al informe fotográfico, es la vecina más directamente afectada por la apertura de huecos y saledizos, amén de que, como copropietaria, se ve privada de porciones de elementos comunes y el correcto funcionamiento de un patio común.

VII.- COSTAS.

Debe imponerse el pago de las costas procesales a la Comunidad demandada por criterio del vencimiento del art. 394.1 LEC.

Por todo cuanto antecede,

SUPLICO AL TRIBUNAL

que, teniendo por presentada esta demanda, con sus copias y documentos que acompaño, se digne admitir una y otros, tenerme por comparecido y parte en la representación que ostento de D./Dña. [NOMBRE Y APELLIDOS], entendiéndose conmigo las sucesivas diligencias y por deducida demanda de suspensión sumaria de obra nueva, se dicte resolución que acuerde ordenar inmediatamente al dueño de la obra, Comunidad de Propietarios de [DENOMINACIÓN DE LA COMUNIDAD], que suspenda la obra descrita en el ordinal tercero de los hechos de la demanda, en el estado en que se encuentre, de modo que por el Letrado de la Administración de Justicia se acuerde dar traslado a la parte demandada para que comparezca y la conteste, siguiendo la tramitación legal asignada, después de la que se dicte sentencia en la que se condene definitivamente al demandado a la suspensión de la dicha obra, con pago de las costas de este proceso.

OTROSÍ DIGO: Que interesa al derecho de esta parte que se proceda a la designación judicial de un perito, arquitecto técnico, por resultar perfectamente pertinente y útil que emita dictamen sobre la especificación de las obras extralimitadas respecto de las autorizadas por las Comunidades de Propietarios, su valor, y los perjuicios que ocasionan a los elementos comunes, debiendo pronunciarse al respecto la contraparte si se opusiera a la demanda, cuando se le traslade (cfr.: arts. 339 y 347 LEC).

Igualmente, se interesa que el Tribunal disponga, para antes que se dé traslado para la contestación a la demanda, el reconocimiento judicial de la obra nueva concurrente con el pericial del perito que se designe, todo ello de conformidad con los arts. 441.2 párrafo 1.º "in fine", en relación con el art. 356 LEC.

SUPLICO AL TRIBUNAL que se sirva tener por hechas las anteriores solicitudes a los efectos legales oportunos, acordando precaver lo conducente a la rápida y eficaz práctica de los medios probatorios prevenidos, con lo demás que sea procedente en

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a
