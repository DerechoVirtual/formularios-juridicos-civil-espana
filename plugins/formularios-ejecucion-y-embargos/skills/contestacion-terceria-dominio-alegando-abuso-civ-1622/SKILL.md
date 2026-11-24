---
name: contestacion-terceria-dominio-alegando-abuso-civ-1622
description: "Contestación a tercería de dominio alegando abuso de personalidad jurídica y fraude de acreedores. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contestación a tercería de dominio alegando abuso de personalidad jurídica y fraude de acreedores

> Formulario **CIV-1622** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Escrito de contestación a la demanda de tercería de dominio alegando el abuso de personalidad jurídica y el fraude de acreedores para que se levante el velo del tercero.

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contestación a tercería de dominio alegando abuso de personalidad jurídica y fraude de acreedores» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contestación a tercería de dominio alegando abuso de personalidad jurídica y fraude de acreedores” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:contestacion-terceria-dominio-alegando-abuso-civ-1622`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (27 veces)
- [ ] DENOMINACIÓN SOCIAL (13 veces)
- [ ] FECHA (7 veces)
- [ ] Nº (6 veces)
- [ ] AÑO (4 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] IMPORTE (3 veces)
- [ ] IMPORTE EN CIFRA (3 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] DIRECCIÓN
- [ ] DÍA
- [ ] LUGAR
- [ ] MES
- [ ] NOMBRE DE LA PARTE
- [ ] Nº DE PROCEDIMIENTO
- [ ] SECCIÓN
- [ ] SEDE
- [ ] ÓRGANO

## Normas que cita el formulario

- art. 589 LEC
- art. 659 LEC
- art. 595.3 LEC
- art. 600 LEC
- art. 255.1 LEC
- art. 1.111 CC
- art. 1.911 CC
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

### Avisos de actualización (2) — se aplican en el texto, nunca se copian en el documento

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, que actúa en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS], según tengo acreditado mediante copia de la escritura de poder que se acompañó y cuya copia está testimoniada en los autos principales de Ejecución de título judicial n.º [NÚMERO]/[AÑO], seguidos a mi instancia contra D./Dña. [NOMBRE Y APELLIDOS] y otros, en la pieza de Tercería de Dominio n.º [Nº]/[AÑO], ante el Tribunal comparezco y como mejor proceda en Derecho DIGO:

Que mediante el presente escrito y dentro del término conferido por decreto de [FECHA], paso a contestar la demanda detercería de dominio formulada de adverso, oponiéndome a la misma en base a los siguientes:

HECHOS

PRIMERO.- Mi mandante, como medio de pago del precio de una ejecución de obra, obtuvo letra de cambio de una sociedad comitente, [DENOMINACIÓN SOCIAL] S.L., avalada solidariamente por los cuatro socios de la misma, entre los que se contaba D./Dña. [NOMBRE Y APELLIDOS]

Incobrada, y avanzándosele por los avalistas al acreedor que no cobraría, confió en que la Jurisdicción no tolerase tal resultado, e interpuso juicio cambiario contra todos los firmantes de la letra, al que dieron en oponerse dos de los demandados, uno de los cuales era el citado D./Dña. [NOMBRE Y APELLIDOS], con resistencias de corte puramente dilatorio.

Dictada sentencia de [FECHA], por el Tribunal al que me dirijo, que desestimaba la oposición, dio en recurrir en apelación uno de los deudores, e impugnó también D./Dña. [NOMBRE Y APELLIDOS], cosechando ambos el predecible fracaso frente a una acción cambiaria directa, y se dictó sentencia firme de la Sección [SECCIÓN] de la Audiencia Provincial de [LOCALIDAD], de fecha [FECHA].

En ejecución del fallo se procedió a pasar a la vía de apremio por un crédito de principal de [IMPORTE] euros ([IMPORTE EN CIFRA] €), vencido hace más [Nº] años.

SEGUNDO.- Mediaba embargo de una vivienda en el Paseo de [DIRECCIÓN], n.º [NÚMERO], de [LOCALIDAD], de titularidad registral de D./Dña. [NOMBRE Y APELLIDOS], que es la finca objeto de la tercería, en cuyo aseguramiento se procedió a practicar anotación preventiva el [FECHA], y se instó el avalúo del inmueble para venta pública.

Previamente, se acordó requerir la certificación de cargas del Registrador, a cuyo tenor, obrante en autos principales, y cuya copia se acompaña, como DOCUMENTO NÚMERO [Nº DE DOCUMENTO], y conforme a la que consta que, al momento de emitirse la certificación el dominio de la finca ya se había inscrito a favor de la demandante [ÓRGANO], S.L., en base a la aportación que efectuó D./Dña. [NOMBRE Y APELLIDOS] a tal mercantil en virtud de la escritura que se aporta con la demanda de tercería.

TERCERO.- [DENOMINACIÓN SOCIAL], S.L. a cuyo favor consta transferida la propiedad inscrita del inmueble embargado, es pura forma para conseguir que el inmueble sea viable que escape de la agresión de los acreedores ‘burlados’, ya lo sean de la persona física que es su voluntad, ya lo sean de la misma persona jurídica.

La finca es, durante [Nº] años, de la sociedad conforme a los libros del Registro Mercantil, y de la persona física conforme a los del Registro de la Propiedad: si se embarga a la sociedad, no puede anotarse en la finca, y si se anota en la finca, se libra con la tercería de dominio.

La patente intención defraudatoria se capta por poderosos indicios.

CUARTO.- [DENOMINACIÓN SOCIAL], S.L. es una sociedad mercantil por acciones que fundaron D./Dña. [NOMBRE Y APELLIDOS], ejecutado en los autos de que dimana esta tercería, y el padre de éste, D./Dña. [NOMBRE Y APELLIDOS]

1.- La vivencia del Sr./a [NOMBRE Y APELLIDOS] no consta a esta parte, y ya en la constitución — — contaba [Nº] años, y estaba lógicamente jubilado, por lo que, dada la edad y parentesco, se trata de una sociedad virtualmente unipersonal (si no lo es en sentido material y riguroso, a cuya comprobación se requerirá la exhibición del libro de accionistas).

2.- El capital social asciende a [IMPORTE] euros ([IMPORTE EN CIFRA] €), del que suscribió el 95% D./Dña. [NOMBRE Y APELLIDOS],y el 5% restante el padre, desembolsado íntegramente, la parte mayoritaria mediante la aportación de la vivienda embargada, lo que corrobora la textura de sociedad patrimonial familiar.

3.- El ejecutado, D./Dña. [NOMBRE Y APELLIDOS], en su momento, cuando se inició el litigio, y hasta ahora, tiene la vivienda aportada a la S.L. como su domicilio particular, por lo que no sirve a ninguno de los fines del objeto social (art. 2 de los Estatutos), más que en el sentido de domicilio de quien presta servicios a terceros (D./Dña. [NOMBRE Y APELLIDOS], arquitecto técnico), que es eventualmente el negocio, al tiempo, de persona física y jurídica.

3.- D./Dña. [NOMBRE Y APELLIDOS], es el administrador general único desde la constitución, reelegido (autolegido) por tiempo indefinido desde [FECHA]

4.- El valor de la vivienda que capitaliza la sociedad se fijó de mutuo acuerdo, sin tasación de experto, por D./Dña. [NOMBRE Y APELLIDOS] y su padre, en una aproximada cuarta parte de su precio de mercado más prudente.

5.- Si se repasan las que -sean imagen fiel como pretenden o no- de las cuentas anuales del ejercicio, S.L. es instrumental de la facturación de los servicios profesionales de D./Dña. [NOMBRE Y APELLIDOS], que es el único asalariado, y para proteger formalmente de agresiones un capital inmovilizado particular (la vivienda), y mobiliario (valores no admitidos a cotización, que se contabilizan en más de [IMPORTE] euros ([IMPORTE EN CIFRA] €)).

6.- Por último, ante el requerimiento de manifestación de bienes realizado a D./Dña. [NOMBRE Y APELLIDOS] conforme al art. 589 LEC, éste respondió que las acciones en [DENOMINACIÓN SOCIAL], S.L. las había donado en póliza mercantil a su hija menor, de [Nº] años de edad, con reserva de enajenación y gravamen.

Me remito a las constancias documentales en autos, a las oficinas censales de [LOCALIDAD], y a los libros del Registro Mercantil de [LOCALIDAD], aportando certificación registral de las inscripciones habidas de [DENOMINACIÓN SOCIAL], S.L., COMO DOCUMENTO NÚMERO [Nº DE DOCUMENTO].

QUINTO.- Hasta tal punto se confunde [DENOMINACIÓN SOCIAL], S.L. y D./Dña. [NOMBRE Y APELLIDOS], que el poder para pleitos con el que comparece su Procuradora en la tercería de dominio es el mismo que el que sirvió para comparecer en el juicio cambiario.

Y hasta tal punto se rebasa el deseo evidente de dejar sin sentido el ejercicio jurisdiccional del crédito, que prevalece el perjuicio sobre la pura solicitud de alzamiento del embargo. Tal alzamiento no se pidió hace meses, cuando D./Dña. [NOMBRE Y APELLIDOS] lo conocía perfectamente, puesto que con él se entendió en [FECHA], cuando había otros acreedores anotados y no se había inscrito el dominio de la S.L., y tampoco se pidió al comunicarse en [DÍA] de [MES] de [AÑO] por el Registrador de la Propiedad la emisión de la certificación de cargas con arreglo a los arts. 659 y 660 LEC.

Se espera a que el ejecutante incurra en el costo de la peritación para el avalúo, y de las publicaciones de los edictos de la subasta, con la finalidad obvia de que mi poderdante, no sólo no cobre su crédito sino que pretenderlo le reporte un gasto mayor.

La suspensión del apremio, por sí, ya que no se sujeta a posible caución de daños y perjuicios por el tercerista, provoca el daño.

FUNDAMENTOS DE DERECHO

I.- COMPETENCIA Y PROCEDIMIENTO.

Debe mostrarse conformidad con la competencia, genérica y objetiva del Tribunal a que se ha dirigido la entidad actora, y asimismo con que el proceso adecuado es el juicio ordinario (verbal, desde la reforma operada por la Ley 37/2011, de 10 de octubre, de medidas de agilización procesal), señalado por la actora en el correlativo de la demanda.

II.- LEGITIMACIÓN.

Está legitimado activamente en proceso de tercería de dominio quien afirma ser dueño o titular de derecho que, por disposición legal expresa, pueda oponerse al embargo de un bien, o a su realización forzosa, como de pertenencia al ejecutante, sin ser parte en este proceso, y que no afirma serlo después del embargo (en cuyo caso sería un tercer poseedor), de manera que en este sentido meramente procesal que, por excepción, se trata de una afirmación que ha de documentarse ‘in limine litis’ (art. 595.3 LEC), estaría legitimada [DENOMINACIÓN SOCIAL], S.L., aunque no detenta el derecho enervante del embargo, como se verá.

La legitimación pasiva procesal viene marcada en la norma mediante un litisconsorcio pasivo voluntario, en el que se halla el ejecutante, DX [NOMBRE DE LA PARTE] (art. 600 LEC).

III.- CUANTÍA.

Esta parte no puede enfrentarse a la cuantificación que hace la demanda del interés litigioso, conforme al valor catastral del año pasado que tiene fijada la Hacienda, dado que el art. 255.1 LEC, sólo habilita para impugnar la cuantía cuando la determinación inadecuada provocara la elección indebida del cauce procesal, o viabiliza la recurribilidad en casación, ninguna de las dos cosas que ocurre.

IV.- FORMALISMO Y REALIDAD: DOCTRINA DEL LEVANTAMIENTO DEL VELO DE LAS PERSONAS JURÍDICAS

El Derecho patrimonial del liberalismo, del que procede nuestro ordenamiento vigente, permitió un gran avance material y económico respecto de la situación del Antiguo Régimen, pero se funda en la libre transmisión de la propiedad como liberación de gravámenes y en el ejercicio jurisdiccional del crédito, cuya base es esencialmente formalista, tanto en cuanto a la naturaleza del domino (teoría del título y el modo, ‘traditio’ ideal, del documento público), como de las preferencias de los créditos (privilegio de las garantías reales, exclusión de la afección general por la especial, publicidad registral -recientemente, también la mobiliaria- o por la clásica por la posesión, prioridad por otorgamiento de la titulación), de lo que surge una desazonante incoherencia, derivada de la extrema facilidad para preconstituir una titulación, una prueba, una transmisión, o un pago, fraudulenta para daño de terceros (otros acreedores, el cónyuge, los legitimarios, el fisco, etc), o en general, apartada de la realidad de hecho.

La Jurisdicción cumple la función difícil de conciliar un sistema patrimonial que sustenta intereses privados en base a razones formales con valores universales de justicia objetiva, que es mínima moralidad, idoneidad pública, y en definitiva, subordinación a la realidad de la apariencia creada por la titulación formal.

El Derecho civil puramente formal es algo que se sostiene porque no se lleva a sus últimas consecuencias, en la medida que siempre está la tutela judicial para que se proceda a sospechar de la verosimilitud de los títulos, y resucite la causa ante la publicidad —sistema de orígenes ciertos, cuyo progresismo no se niega, en cuanto que unifica e ideologiza el Derecho patrimonial—, como la última protección ‘crítica’ de los terceros, excepcional y compleja.

Existen vías de control jurisdiccional empleables frente a enajenaciones fraudulentas o abusivas de los propietarios, forjadas en la solidarización impropia o de garantía, legal o jurisprudencial, del débito (responsabilidad aquiliana, acciones edilicias, vicios ruinógenos en la construcción, unidad de empresa, subrogación contractual, etc), que aquí no tocan, pero las de inefectividad del título, sin matices específicos para especialidades de órdenes jurisdiccionales que viven en íntima conexión con Derechos sustantivos de fisonomía peculiar (social y administrativo), pueden resumirse:

1.º) Conminación penal de las preparaciones dolosas de una insolvencia (esencialmente, alzamiento de bienes del art. 257 CP); 2.º) Nulidad por la teoría de la simulación y causa inexistente o ilícita de los negocios jurídicos; 3.º) Ineficacia de los negocios jurídicos bilaterales sinalagmáticos por inequivalencia notoria de prestaciones, desde las medidas de la Ley Azcárate de 1908, recientemente derogada, hasta las modernas medidas de tutela de consumidores y usuarios que impone el Derecho europeo comunitario derivado (depuración de la competitividad); 4.º) Principio pauliano, que abarca la propia acción revocatoria del art. 1.111 CCiv, las acciones de retroacción concursal (v.gr.: arts. 226 y ss. del Texto refundido de la Ley Concursal, aprobado por Real Decreto Legislativo 1/2020, de 5 de mayo), y la presunción de ‘consulium fraudis’ en la desproporción económica del contrato que es título en tercería de dominio o de mejor derecho; 5.º) Construcción del negocio fiduciario, cada vez con más vigencia en el campo del mercado crediticio mercantil; 6.º) Doctrina del levantamiento del velo de la personalidad jurídica.

El supuesto de autos es paradigma de lo que autoriza a levantar el velo de la personalidad de [DENOMINACIÓN SOCIAL], S.L., que no es nada diferente que la persona natural D./Dña. [NOMBRE Y APELLIDOS], ejecutado en el proceso principal, y además que autoriza hacerlo, no ya como protección de mi patrocinado ejecutante, sino de la misma ética y función del proceso ejecutivo, y la seriedad del ejercicio jurisdiccional del crédito, una vez que se ha debatido en dos instancias (suscitado el proceso cognoscitivo por oposición al juicio cambiario, y tramitada la apelación).

La mercantil demandante en juicio de tercería no tiene en realidad la condición de tercero en la ejecución que se sigue, por aplicación de la doctrina del levantamiento del velo (‘disregard’ o ‘lifting the veil’).

Esta doctrina pretende corregir en determinadas circunstancias en uso torticero de ciertas figuras o fórmulas jurídicas, sin afectar al derecho de propiedad, la autonomía patrimonial, o la personalidad jurídica, puesto que el peligro no se halla en esta última, sino en una concepción de la misma que se caracterice por un hermetismo intangible y lo formal como absoluta suficiencia jurídica.

La doctrina cuenta con un apoyo jurisprudencial ya profuso (por citar las SSTS del preciso ámbito de las tercerías de dominio formuladas por sociedades que, levantado el velo, se decreta que son la misma persona ejecutada: 28 de abril 1988, Sentencia del Tribunal Supremo, Sala Primera, de lo Civil, de 24 Dic. 1988, 2 de abril de 1990, 12 de noviembre de 1991, 16 de marzo, Sentencia del Tribunal Supremo, Sala Primera, de lo Civil, Sentencia de 15 Abr. 1992 y 24 de abril de 1992, Sentencia del Tribunal Supremo, Sala Primera, de lo Civil, de 11 Nov. 1995, Rec. 1460/1992, Sentencia del Tribunal Supremo, Sala Primera, de lo Civil, de 25 Feb. 1997, Rec. 809/1993, 31 de enero, 30 de mayo de 1998 y Sentencia del Tribunal Supremo, Sala Primera, de lo Civil, de 9 Nov. 1998, Rec. 1825/1994, 22 de febrero de 1998 y Sentencia del Tribunal Supremo, Sala Primera, de lo Civil, de 11 Oct. 1999, Rec. 504/1995), y un cimiento sólido en los principios preceptuados en el Título Preliminar del Código Civil: art. 7.1, que impone la buena fe, art. 3.2 que asume la equidad, art. 7.2 que rechaza el abuso de derecho y el ejercicio antisocial del mismo, y el art. 6.4, que prohíbe el fraude de ley.

En el caso de autos resulta evidente que [DENOMINACIÓN SOCIAL], S.L., y D./Dña. [NOMBRE Y APELLIDOS] son una sola cosa, confundiéndose la personalidad y los patrimonios: [DENOMINACIÓN SOCIAL], S.L., no tiene funcionamiento real independiente de su socio virtualmente único y administrador general único (el ejecutado cuyo bien se embargó, puesto que el 95% se ha donado a una hija menor, en condiciones vinculadas, y el 5% sería del abuelo, de edad provecta, caso de vivir), ni hay voluntad independiente, ni la personalidad es efectivamente distinta

[NOMBRE Y APELLIDOS], S.L. es un puro instrumento para actuar en el tráfico mercantil, en la medida que cabría aseverar que se trata, no ya de una unidad formal sino real, dado que el domicilio particular es el social, el capital es de la persona ejecutada y precisamente desembolsado por vía de la valoración del inmueble que resulta tal domicilio.

[NOMBRE Y APELLIDOS], S.L., sirve, como el Tribunal comprobará con la acreditación de los indicios del ordinal cuarto de los hechos, que se provoca lo que la jurisprudencia ha llegado a denominar en casos como el de autos -si se repasan los antecedentes, aún menos llamativos, porque intervienen más personas- simbiosis jurídica entre la sociedad tercerista y los ejecutados: ‘ la simbiosis existente entre la entidad demandante de tercería y el matrimonio demandado hace imposible distinguir en la práctica la figura del tercero ‘ [STS de 2 de abril de 1990], o ‘ la demandante no tiene carácter de tercero, dada la coincidencia de elementos personales, revelada al levantar el velo jurídico de ambas sociedades ‘ (STS de 22 de febrero de 1999, rec. 869/1998).

La consecuencia del desenmascaramiento de la realidad jurídica es desvelar una inconsistencia de la personalidad independiente de la sociedad, de tal manera que no cabe hablar de propiedad de la sociedad y propiedad del socio, de lo que surge como corolario, en el ámbito de la tercería de dominio que, siendo el bien que se aduce titularidad por aportación de [DENOMINACIÓN SOCIAL], S.L., embargado como de pertenencia de D./Dña. [NOMBRE Y APELLIDOS], nada ilícito se provoca, y debe seguir adelante la ejecución con desestimación de la demanda del pretendido tercero que carece de legitimación ‘ad causam’ para conseguir el alzamiento del embargo.

La doctrina del levantamiento del velo en el presente caso responde al supuesto del fraude de la ley que reconoce la capacidad jurídica de las personas morales, puesto que al amparo de la norma de cobertura del Derecho de sociedades se persigue con claridad un fin elusivo del cumplimiento de una norma imperativa, que es la responsabilidad universal del deudor con todos sus bienes presentes y futuros del art. 1.911 CCiv, lo cual se hace abusando de las formas (la personalidad independiente no existe cuando el sujeto se aparta en la realidad del funcionamiento independiente —formación de la voluntad y confusión patrimonial—), defraudando el fin de las normas (en perjuicio del acreedor, pero también del proceso ejecutivo, que es potestad estatal), y con notable mala fe, puesto que se espera al último momento para lograr la suspensión de la subasta —fin de todas las maneras lucrado— cuando el conocimiento de la vía de apremio era perfecto y muy anterior.

Si el acto de aportación al capital social fundacional de [DENOMINACIÓN SOCIAL], S.L. del inmueble de D./Dña. [NOMBRE Y APELLIDOS], embargado a favor del proceso ejecutivo que sigue esta parte, persigue un resultado contrario al ordenamiento jurídico, debe considerarse realizado en fraude de ley, y por consiguiente (art. 6.4CCiv), la tutela judicial que aquí se pide es la declaración de que no está impedida la correcta aplicación de la norma eludida (art. 1.911CCiv), esto es, la responsabilidad patrimonial universal del socio-administrador-dueño la sociedad mercantil, D./Dña. [NOMBRE Y APELLIDOS], de forma que nunca ha salido válidamente de tal responsabilidad.

Aunque la demanda de tercería pide que se estime, y dice que la finca es propiedad de [DENOMINACIÓN SOCIAL], S.L., en realidad no expresa qué es el pronunciamiento que solicita del Tribunal, lo que debe completarse con la doctrina jurisprudencial que establece el ámbito de resolución posible de la tercería de dominio, el cual no puede ser más que declarar la pertenencia de un bien y la improcedencia del embargo a los únicos efectos de la ejecución en curso, sin pasar en autoridad de cosa juzgada la titularidad del bien.

Así se reclama la íntegra congruente desestimación de la tercería, lo que consiste en que se considere que la vivienda, que es finca urbana descrita en la demanda, no pertenece a, S.L. a los únicos efectos del proceso de ejecución n.º [Nº DE PROCEDIMIENTO]/[AÑO], y procede su embargo como se trabó y aseguró registralmente, sin perjuicio de la titularidad definitiva, que no es objeto de debate.

V.- COSTAS.

Las costas procesales deberán ser impuestas a la entidad demandante, conforme al criterio cuasiobjetivo del art. 394.1 LEC, como procede según remisión por el art. 603, párrafo 2.º LEC.

En su virtud,

SUPLICO AL TRIBUNAL

que teniendo por presentado este escrito con sus documentos y copias, se sirva admitir uno y otros, y se tenga a mi representado por opuesto a la tercería de dominio, y por contestada la demanda y, seguido el proceso por todos sus trámites, se venga a dictar auto íntegramente desestimatorio de los pedimentos deducidos en la demanda, manteniendo la traba y prosiguiendo el proceso de ejecución, con expresa imposición de costas a la parte actora.

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a

========================================================================
