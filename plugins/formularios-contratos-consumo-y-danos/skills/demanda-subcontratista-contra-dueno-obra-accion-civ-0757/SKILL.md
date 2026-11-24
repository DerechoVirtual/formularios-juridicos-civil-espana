---
name: demanda-subcontratista-contra-dueno-obra-accion-civ-0757
description: "Demanda del subcontratista contra el dueño de la obra por la acción directa del artículo 1597 CC. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda del subcontratista contra el dueño de la obra por la acción directa del artículo 1597 CC

> Formulario **CIV-0757** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio ordinario con la que el subcontratista (o quien puso su trabajo y materiales en una obra) reclama su crédito directamente al propietario o comitente de la obra, hasta el límite de lo que éste adeude al contratista, al amparo de la acción directa del art. 1597 del Código Civil.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda del subcontratista contra el dueño de la obra por la acción directa del artículo 1597 CC» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda del subcontratista contra el dueño de la obra por la acción directa del artículo 1597 CC” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:demanda-subcontratista-contra-dueno-obra-accion-civ-0757`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº DE DOCUMENTO (9 veces)
- [ ] IMPORTE (8 veces)
- [ ] DENOMINACIÓN SOCIAL DE LA DEMANDADA (5 veces)
- [ ] DENOMINACIÓN SOCIAL DEL CONTRATISTA (5 veces)
- [ ] FECHA (5 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] FIRMA (2 veces)
- [ ] AÑO
- [ ] CORREO ELECTRÓNICO
- [ ] DENOMINACIÓN SOCIAL DEL DEMANDANTE
- [ ] DIRECCIÓN DE LA OBRA
- [ ] DOMICILIO
- [ ] DOMICILIO DEL DESPACHO
- [ ] DÍA
- [ ] FECHAS
- [ ] MES
- [ ] NOMBRE Y APELLIDOS DEL ABOGADO/A
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] Nº DE INSCRIPCIÓN
- [ ] SEDE
- [ ] TELÉFONO
- [ ] TIPO DE TRABAJOS

## Normas que cita el formulario

- art. 1597 Código Civil
- art. 399.1 LEC
- art. 85.1 LOPJ
- art. 45 LEC
- art. 51.1 LEC
- art. 6.1.3.º LEC
- art. 7.4 LEC
- art. 1597 CC
- art. 10 LEC
- art. 253 LEC
- art. 251.1.ª LEC
- art. 249.2 LEC
- art. 23 LEC
- art. 5 Ley Orgánica 1/2025
- art. 1100 CC
- art. 63.2.º Código de Comercio
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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] QUE POR TURNO CORRESPONDA»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] QUE POR TURNO CORRESPONDA

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, en nombre y representación de la entidad [DENOMINACIÓN SOCIAL DEL DEMANDANTE], a cuya justificación aporto escritura de poder inscrito en el Registro Electrónico de Apoderamientos Judiciales con el nº [Nº DE INSCRIPCIÓN] y que se puede acreditar mediante consulta automatizada orientada al dato, por parte del órgano judicial al cual tengo el honor de dirigirme, acompañándose certificación electrónica del Registro Electrónico de Apoderamientos Judiciales como Documento nº [Nº DE DOCUMENTO] por si no es posible la consulta automatizada, dirigido por el Letrado abajo firmante D./Dña. [NOMBRE Y APELLIDOS DEL ABOGADO/A], con despacho profesional en [DOMICILIO DEL DESPACHO], ante el Tribunal comparezco y como mejor proceda en Derecho DIGO:

Que, en la representación que ostento, interpongo demanda de juicio declarativo ordinario ejercitando la acción directa prevista en el art. 1597 del Código Civil contra la entidad [DENOMINACIÓN SOCIAL DE LA DEMANDADA], con domicilio en [DOMICILIO] ([LOCALIDAD]).

Que esta parte asume el compromiso de recibir cualquier comunicación dirigida por la oficina judicial, durante toda la fase declarativa e, incluso, en una eventual fase de ejecución, por medios telemáticos, en términos del art. 399.1 II LEC, consignándose a estos efectos la siguiente dirección de correo electrónico y nº de teléfono: [CORREO ELECTRÓNICO] y [TELÉFONO].

Fundamento la misma en los siguientes hechos y consideraciones jurídicas:

HECHOS

PRIMERO.- Mi cliente fue subcontratada el [FECHA] por la entidad [DENOMINACIÓN SOCIAL DEL CONTRATISTA] para la realización de diversos trabajos de [TIPO DE TRABAJOS, p. ej. carpintería] con suministro de material en la obra sita en [DIRECCIÓN DE LA OBRA] de la localidad de [LOCALIDAD], propiedad de la entidad [DENOMINACIÓN SOCIAL DE LA DEMANDADA], por un precio fijo de [IMPORTE] euros, más el importe de los materiales necesarios hasta un máximo de [IMPORTE] euros, previa su justificación. Se acompaña copia del contrato como documento n.º [Nº DE DOCUMENTO].

SEGUNDO.- [DENOMINACIÓN SOCIAL DEL CONTRATISTA] había contratado, a su vez, a [DENOMINACIÓN SOCIAL DE LA DEMANDADA] para [OBJETO DE LA OBRA, p. ej. edificar un complejo de oficinas] en la citada obra, conforme al contrato que se adjunta como documento n.º [Nº DE DOCUMENTO].

TERCERO.- Mi mandante ha desarrollado, durante el periodo comprendido entre [FECHA] y [FECHA], los trabajos contratados en el plazo pactado, sin que, hasta la fecha, se haya advertido por ninguna de las dos entidades la existencia de defectos o necesidad de subsanación alguna. Por ello, y en virtud de los precios concertados, se han emitido las facturas que se aportan como documentos n.º [Nº DE DOCUMENTO] y [Nº DE DOCUMENTO], por un importe total de [IMPORTE] euros: [IMPORTE] euros por los trabajos realizados, conforme a lo pactado, y [IMPORTE] euros por los materiales suministrados.

CUARTO.- Con fecha [FECHA] se envió burofax a la propietaria de la obra, [DENOMINACIÓN SOCIAL DE LA DEMANDADA], en reclamación del importe indicado, después de que [DENOMINACIÓN SOCIAL DEL CONTRATISTA] comunicara por correo electrónico su imposibilidad de hacer frente al pago. Se aporta copia de la referida comunicación como documento n.º [Nº DE DOCUMENTO], frente a la cual no se ha obtenido respuesta alguna hasta la fecha. Asimismo, se adjunta copia del referido correo electrónico como documento n.º [Nº DE DOCUMENTO].

Asimismo, la parte actora manifiesta que, previo a la presentación de la presente demanda, se han llevado a cabo negociaciones posteriores con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria, incluyéndose entre las acciones realizadas el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución.

Finalmente, mi representada envió un requerimiento fehaciente a la demandada con fecha [FECHA], fijando un plazo de 30 días naturales para llegar a un acuerdo amistoso, a través del abogado que firma este escrito, el cual fue contestado por la demandada por el mismo medio, [ELEGIR: rechazando el acuerdo / habiendo sido solo posible un acuerdo parcial], viéndonos en la necesidad de acudir a la presente vía judicial, respecto a los extremos de la controversia en los que se mantiene la discrepancia.

Acompaño como documento nº [Nº DE DOCUMENTO] el requerimiento efectuado y como documento nº [Nº DE DOCUMENTO] la contestación de la demandada.

A los anteriores hechos, son aplicables los siguientes:

FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN Y COMPETENCIA

En cuanto a la competencia objetiva, el art. 85.1 LOPJ y el art. 45 LEC designan a los Tribunales de Instancia como los órganos con la competencia específica, objetiva y funcional para resolver estos pleitos.

Asimismo, el Tribunal al que tengo el honor de dirigirme es competente territorialmente, pues a su partido judicial corresponde el domicilio de la demandada, conforme al art. 51.1 LEC.

II.- CAPACIDAD

Al tratarse de [ELEGIR: sociedades de responsabilidad limitada / sociedades anónimas / sociedades de capital], su capacidad se reconoce en el art. 6.1.3.º LEC, derivándose su personalidad de su constitución en escritura pública inscrita en el Registro Mercantil, con la necesidad de comparecer en juicio por medio de sus representantes legales (art. 7.4 LEC).

III.- LEGITIMACIÓN

Corresponde a mi cliente la activa por haber sido contratada por entidad previamente contratada por la demandada, propietaria de la obra, frente a la cual se ejercita la pretensión contenida en este escrito (art. 1597 CC y art. 10 LEC).

IV.- CUANTÍA Y PROCEDIMIENTO

Conforme al art. 253 LEC cifro la cuantía de la presente demanda en [IMPORTE] euros, correspondiente al principal reclamado, según dispone el art. 251.1.ª LEC.

Por todo ello, el procedimiento ajustado a derecho será el del juicio declarativo ordinario regulado en los arts. 399 a 436 de la misma Ley, atendiendo a la cuantía fijada, en aplicación de lo dispuesto en el art. 249.2 LEC.

V.- POSTULACIÓN Y DEFENSA

Conforme a lo previsto en los arts. 23 y 31 LEC, se presenta la demanda por medio de Procurador/a legalmente habilitado y bajo dirección de Letrado firmante de la misma.

VI.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4.º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

VII.- FONDO DE LA CUESTIÓN CONTROVERTIDA

A) Acciones ejercitadas

En esta demanda se ejercita la acción directa de la cual dispone el subcontratista de una obra frente al propietario de la misma, conforme a lo dispuesto en el art. 1597 CC: «Los que ponen su trabajo y materiales en una obra ajustada alzadamente por el contratista, no tienen acción contra el dueño de ella sino hasta la cantidad que éste adeude a aquél cuando se hace la reclamación».

Dicho precepto habilita la posibilidad de que un subcontratista, como ocurre en este caso con mi mandante, que ha realizado directamente trabajos en una obra, pueda dirigir su reclamación de cantidad frente a la parte que le ha contratado o, cuando le convenga, frente al propietario de la obra. Y ello de manera indistinta, pudiendo dirigir aquella frente a quien considera efectivo, que es lo que aquí ocurre al no apreciar posibilidad de cobro del precio de los trabajos frente a [DENOMINACIÓN SOCIAL DEL CONTRATISTA]. Al respecto, la SAP Barcelona de 2 de marzo de 2006 indica que, «aunque quien ha realizado la obra puede reclamar el pago correspondiente al contratista que se obligó a ello, actuando contra el otro contratante y respetando así el principio de relatividad de los contratos, el Código Civil permite el ejercicio de la acción directa contra el dueño de la obra, entendiéndose que ambas obligaciones son solidarias, de suerte que el subcontratista puede dirigirse indistintamente contra uno u otro, aunque el comitente o dueño de la obra solamente responderá hasta el límite que el precepto señala (SSTS de 29 de abril de 1991, 11 de octubre de 1994, 2 de julio de 1997, 22 de diciembre de 1999, 6 de junio y 27 de julio de 2000). Añade que la doctrina del Tribunal Supremo arranca con sentencias como las de 11 de junio de 1928, 15 de octubre de 1915 o 29 de junio de 1936, y se reitera posteriormente, refiriendo la eficacia protectora de los derechos del último eslabón de la cadena, formado por quienes al fin y a la postre, poniendo su trabajo o sus materiales, son los verdaderos artífices de la obra y no ven satisfechos sus créditos por aquél o aquéllos que directamente les hubiera contratado. Compendio de esa jurisprudencia del artículo 1597 es la STS de 2 de julio de 1997, si bien, tras destacar los caracteres de la acción directa contemplada en dicho artículo como una excepción al principio de relatividad del contrato, en ella se atiende a la realidad social de nuestros días, con la frecuente aparición de subcontratos encadenados, para justificar la aplicación de la acción directa del artículo 1597 del Código Civil con planteamientos distintos a los que se enfrentó el Código Civil del año 1889. La razón de ser de esta norma y el tratamiento privilegiado que supone se ha encontrado en criterios de equidad, en la necesidad de evitar el enriquecimiento injusto, en la protección de un derecho a manera de refacción, o una especie de subrogación general derivada del principio de que "el deudor de mi deudor es también deudor mío"».

En definitiva, se trata de evitar el enriquecimiento injusto del propietario de la obra, protegiendo los derechos de los subcontratados, último eslabón de la cadena de construcción, conformado por quienes ponen su trabajo personal y que vienen a ser los verdaderos artífices de la obra.

B) De los requisitos de la acción directa

De esta forma, conforme a jurisprudencia inconcusa que resume la STS de 26 de septiembre de 2008, se desprenden los siguientes requisitos, que concurren en el presente caso:

1.- Están legitimados para reclamar los que ponen su trabajo y materiales en la obra. Los primeros son todos aquellos que llevan a cabo prestaciones de hacer, entendidas en sentido amplio, destinadas a la obra; no sólo los que están unidos al contratista por una relación laboral, sino también los que lo están por una relación civil de servicios, o incluso de gestión, por lo que han de entenderse incluidos los subcontratistas (SSTS, Sala Primera, de 15 de marzo de 1990, 29 de abril de 1991, 11 de octubre de 1994 y 2 de julio de 1997, rec. 2267/1993). Así ocurre con mi cliente, quien ha efectuado [TIPO DE TRABAJOS] con correlativo suministro de material.

2.- Pasivamente legitimado está el dueño de la obra y, en determinados casos, cuando existen varias subcontratas, el subcontratante. En el caso de existir una pluralidad de personas pasivamente legitimadas (pluralidad de comitentes, comitentes y promotores o subcomitentes), la acción podrá dirigirse contra cualquiera de ellos (SSTS, Sala Primera, de 11 de octubre de 1994 y de 2 de julio de 1997, rec. 2267/1993). No existe problema en la obra de la que arranca la presente reclamación, pues la acción se dirige contra la propietaria de la obra, que contrató al subcontratante de mi mandante.

3.- Al tratarse de una acción directa, el subcontratista se hace inmune a las excepciones que el titular de la obra pudiera tener frente al contratista (vicios o defectos que le fueran imputables, por ejemplo, o los pactos entre el contratista y el promotor de exclusión del art. 1597 CC), toda vez que se ejercita contra quien se aprovecha o beneficia del trabajo y materiales puestos en ella. Asimismo, como se ha indicado, no consta ninguna objeción de la propietaria al trabajo realizado, habiéndolo recibido a satisfacción.

4.- El dueño o el contratista principal sólo podrá alegar, y demostrar (pues, por una inversión derivada de la facilidad probatoria, a él le corresponde la carga de dicha prueba, según doctrina establecida en la STS, Sala Primera, 290/2004, de 19 de abril de 2004, rec. 1625/1998) el pago, ya que así lo dice el precepto, de modo que, acreditada la inexistencia de deuda a su cargo, la acción directa queda sin sustento. Resulta por tanto imprescindible, como presupuesto necesario para el ejercicio de esta acción, la existencia de un crédito del contratista contra el comitente o dueño de la obra, crédito que ha de existir y ser exigible en el momento de procederse a la reclamación judicial o extrajudicial. Así lo viene entendiendo el Tribunal Supremo en las SSTS, Sala Primera, de 28 de mayo de 1999, rec. 3219/1994; 67/2002, de 31 de enero de 2002, rec. 2850/1996; o 729/2009, de 20 de noviembre de 2009, rec. 2363/2004; que considera que, si hay una cadena de contrato de obra y subcontratos de la misma, desaparece la acción directa cuando uno de los contratantes o subcontratantes no debe nada al siguiente, rompiéndose así la cadena. En nuestro caso, cuando la demandada es requerida de pago directo, su deuda con la entidad [DENOMINACIÓN SOCIAL DEL CONTRATISTA] era real, cierta y exigible por un importe muy superior al crédito de la demandante.

5.- Aun siendo cierto que el art. 1597 CC sólo se refiere a los contratos de obra por ajuste alzado, la razón de ser de esta limitación consiste en dotar de certeza y seguridad jurídica al límite cuantitativo de la responsabilidad que consagra. Si bien, la presente doctrina es igualmente aplicable en las obras contratadas por precio fijo por unidad de obra, aunque en estos supuestos pueda limitarse la garantía del dueño de la obra o comitente a cada una de las partes o fases de la obra objeto de contratación (STS, Sala Primera, 640/2010, de 14 de octubre de 2010, rec. 1821/2006). Posibilidad con encaje en el contrato firmado por mi cliente, con un precio alzado por la obra y un importe de los materiales, según factura justificada.

6.- Una vez ejercitada esta acción contra el dueño de la obra o el subcontratante, éste a quien debe abonar su importe es al reclamante que intervino en el proceso constructivo y no a la contratista principal. Ello no es más que una consecuencia de la naturaleza solidaria de la responsabilidad del dueño de la obra y contratista para con los subcontratistas de este último que intervienen en la misma (STS de 14 de marzo de 2004).

Por todo ello, y en virtud de los preceptos legales citados y la jurisprudencia que nos ocupa, al concurrir todos los requisitos indicados en el presente caso, procede condenar a la demandada a abonar a mi mandante el principal reclamado, por importe de [IMPORTE] euros.

C) Intereses

Citamos los arts. 1100, 1101, 1108 y 1109 CC y el art. 63.2.º del Código de Comercio, sobre pago de los intereses moratorios a partir de la interpelación judicial.

VIII.- COSTAS

Conforme al art. 394 LEC, las costas han de imponerse a la demandada.

Por lo expuesto,

SUPLICO AL TRIBUNAL:

Que habiendo por presentado este escrito de demanda con los documentos que lo acompañan y copias de uno y otros, los admita y me tenga por comparecido y parte en la representación que ostento y que acreditada dejo; y por promovido juicio declarativo ordinario frente a [DENOMINACIÓN SOCIAL DE LA DEMANDADA], acuerde dar traslado a la demandada para que comparezca y la conteste y, previos los trámites legales y recibimiento a prueba que desde ahora se interesa, se dicte en su día sentencia por la que, estimando la demanda, se condene a la demandada a abonar a mi mandante la cantidad de [IMPORTE] euros, más intereses legales desde la fecha de la primera reclamación extrajudicial.

Todo ello con imposición de las costas del juicio a la parte demandada.

Es justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Abogado/a: [FIRMA] Firma del Procurador/a: [FIRMA]
