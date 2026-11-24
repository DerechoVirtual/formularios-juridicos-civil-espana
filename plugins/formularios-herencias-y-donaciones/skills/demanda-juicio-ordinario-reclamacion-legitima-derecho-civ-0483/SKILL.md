---
name: demanda-juicio-ordinario-reclamacion-legitima-derecho-civ-0483
description: "Demanda de juicio ordinario de reclamación de legítima en derecho común por preterición intencional. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio ordinario de reclamación de legítima en derecho común por preterición intencional

> Formulario **CIV-0483** del plugin **Herencias, testamentos y donaciones** (`formularios-herencias-y-donaciones`) · Civil › Sucesiones y donaciones · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio ordinario en ejercicio de acción de reclamación de legítima, en derecho común, por preterición intencional.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio ordinario de reclamación de legítima en derecho común por preterición intencional» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio ordinario de reclamación de legítima en derecho común por preterición intencional” para mi caso». También puedes invocarla directamente con `/formularios-herencias-y-donaciones:demanda-juicio-ordinario-reclamacion-legitima-derecho-civ-0483`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-herencias-y-donaciones:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Herencias, testamentos y donaciones) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (25 veces)
- [ ] FECHA (8 veces)
- [ ] LOCALIDAD (7 veces)
- [ ] NÚMERO (7 veces)
- [ ] AÑO (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] SEDE (2 veces)
- [ ] CORREO ELECTRÓNICO
- [ ] FECHA DEL TESTAMENTO
- [ ] LUGAR
- [ ] Nº
- [ ] Nº DE COLEGIADO/A
- [ ] Nº DE EXPEDIENTE
- [ ] TELÉFONO

## Normas que cita el formulario

- art. 24.1 LEC
- art. 399.1 LEC
- art. 85.1 LOPJ
- art. 52.1.4.º LEC
- art. 23 LEC
- art. 251 LEC
- art. 253.1 LEC
- art. 5 Ley Orgánica 1/2025
- art. 399 LEC
- art. 113 CC
- art. 806 CC
- art. 1056 CC
- art. 807 CC
- art. 813 CC
- art. 814 CC
- art. 815 CC
- art. 851 CC
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

- Junto a «…N CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] QUE POR TURNO DE REPARTO CORRESPONDA»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: Un solo TI por partido judicial (art. 84.1 LOPJ): sobra «de los de». Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Notas al pie del formulario original:
(1) A la hora de su acreditación, todos los poderes deben estar inscritos en el Registro Electrónico de Apoderamientos Judiciales (REAJ). Se supone que, para su acreditación, basta con la consulta (de dicho Registro) automatizada orientada al dato. Algo que está a disposición de cualquier Letrado de la Administración de Justicia. Sin embargo, dado que el art. 24.2 LEC, configura la certificación de dicha inscripción como vía subsidiaria de acreditación, para el caso de que el sistema no permita aquella consulta automatizada; se señala en el modelo que se acompaña certificación electrónica. El sistema permite emitir dicha certificación para quien inscribe el poder.

(2) El art. 155.3 LEC permite fijar expresar varios domicilios del demandado (el que aparezca en el padrón municipal o conste oficialmente a estos efectos; el que aparezca en Registro oficial o en publicaciones de colegios profesionales, si se trata de empresas o personas colegiadas; donde desarrolle su actividad profesional o laboral no ocasional; si es empresa mercantil, el domicilio de cualquiera de sus administradores, gerentes, o apoderados; o, si es asociación que consta en registro oficial; el domicilio del presidente, miembro o gestor de la Junta correspondiente). Cuando se señalen varios, indicará el orden a seguir para la notificación, con vistas al éxito de la misma.

(3) El art. 155.3 LEC configura una obligación adicional del demandante, consistente en aportar cuantos datos sean de utilidad para localizar al demandado: número de identificación fiscal o de extranjeros, nº [Nº] de teléfono o de fax, dirección de correo electrónico, o similares.

========================================================================

[NOTA DE REVISIÓN: requisito de procedibilidad del art. 5 LO 1/2025 — antes de presentar la demanda hay que intentar un medio adecuado de solución de controversias (MASC) y acreditarlo con la demanda (arts. 264.4.º y 399.3 LEC), salvo las materias excluidas del art. 5.2. Fuente: LO 1/2025, arts. 5 a 7 (BOE-A-2025-76).]


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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] QUE POR TURNO DE REPARTO CORRESPONDA

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales y de D./Dña. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], representación que acredito mediante escritura de poder otorgada a mi favor (existen tres posibilidades para otorgar el apoderamiento al Procurador de los Tribunales, conforme dispone el art. 24.1 LEC)

[OPCIONAL — opción en función de cómo se haya otorgado el poder]

[ELEGIR UNA OPCIÓN: Si el poder se otorga a través de la sede judicial electrónica / Si el poder se otorga mediante comparecencia apud acta / Si el poder se otorga ante Notario]

bajo la dirección letrada de D./Dña. [NOMBRE Y APELLIDOS], abogado/a en ejercicio, con despacho profesional abierto en [LOCALIDAD], colegiado nº [Nº DE COLEGIADO/A] del Ilustre Colegio de la Abogacía de [LOCALIDAD], ante el Tribunal comparezco y como mejor en Derecho proceda, DIGO:

Que mediante el presente escrito vengo a formular DEMANDA DE JUICIO DECLARATIVO ORDINARIO, contra D./Dña. [NOMBRE Y APELLIDOS], con domicilio, primero en [DOMICILIO]; y segundo, el domicilio laboral en [DOMICILIO]); con email [CORREO ELECTRÓNICO]; y con número de teléfono móvil [TELÉFONO]; en ejercicio de la acción que se concretará en el cuerpo del escrito y en el suplico, y todo ello de conformidad con los hechos y fundamentos de derecho que se desarrollarán a continuación.

Que esta parte asume el compromiso de recibir cualquier comunicación dirigida por la oficina judicial, durante toda la fase declarativa, e, incluso, en una eventual fase de ejecución por medios telemáticos, en términos del art. 399.1 II LEC, consignándose a estos efectos la siguiente dirección de correo electrónico y nº [Nº] de teléfono:

HECHOS

PRIMERO

La madre de mi representada, formuló el [FECHA] solicitud de inscripción del nacimiento de su hija, nacida el [FECHA], en la condición de hija de [NOMBRE Y APELLIDOS], ante el Encargado del Registro Civil de [LOCALIDAD], practicándose con audiencia del interesado, y después de la contradicción pertinente, la inscripción con fecha [FECHA] en el citado Registro en virtud de auto dictado en el marco del Expediente [Nº DE EXPEDIENTE] / [AÑO], quedando inscrita en la Sección 1.ª, Libro 8-9, página 13, como se acredita mediante la oportuna certificación, que se acompaña como documento n.º [NÚMERO].

SEGUNDO

D./Dña. [NOMBRE Y APELLIDOS] falleció en [LOCALIDAD] el [FECHA], como resulta del certificado de defunción que se acompaña como documento n.º [NÚMERO], dejando aparentemente un hijo, el demandado D./Dña. [NOMBRE Y APELLIDOS], habido de su matrimonio con D./Dña. [NOMBRE Y APELLIDOS], que le sobrevive viuda.

TERCERO

En testamento autorizado por la Notaria de [LOCALIDAD], D./Dña. [NOMBRE Y APELLIDOS], de fecha [FECHA], n.º [NÚMERO] de su protocolo general corriente, D./Dña. [NOMBRE Y APELLIDOS] instituyó único heredero a D./Dña. [NOMBRE Y APELLIDOS], sin perjuicio de que legaba el usufructo de una finca en pago de la cuota legal usufructuaria a D./Dña. [NOMBRE Y APELLIDOS] Acompañamos copia simple, haciendo documento n.º [NÚMERO].

En el testamento no se hacía mención de que el finado D./Dña. [NOMBRE Y APELLIDOS] tenía un hijo extramatrimonial.

CUARTO

Mi mandante ha llegado a saber de la muerte de D./Dña. [NOMBRE Y APELLIDOS], y de la adjudicación de la herencia al demandado, cuando se publicaron edictos en el Tribunal de Instancia de [SEDE], a propósito del expediente de dominio n.º [NÚMERO]/[AÑO], procedimiento del cual se aporta un testimonio como documento n.º 4

QUINTO

Mediante burofax de fecha [FECHA], mi representada exigió al demandado que se pusiera en contacto con el despacho de abogados que redactó la carta, a fin de debatir el pago de sus derechos como hija del finado D./Dña. [NOMBRE Y APELLIDOS], y hermana de vínculo sencillo, en la herencia del progenitor común, recibiendo contestación por la que se negaba el hecho de la filiación.

Se aporta la carta de reclamación, con su acuse de recibo, como documento n.º [NÚMERO], y la contestación como n.º [NÚMERO].

Finalmente, mi representado envió un requerimiento fehaciente al demandado con fecha [FECHA], fijando un plazo de 30 días naturales para llegar a un acuerdo amistoso, a través del abogado que firma este escrito, el cual fue contestado por el demandado por el mismo medio, rechazando el acuerdo, viéndonos en la necesidad de acudir a la presente vía judicial.

Acompaño como documento nº [Nº DE DOCUMENTO], el requerimiento efectuado y como documento nº [Nº DE DOCUMENTO], la contestación del demandado.

A los anteriores hechos son de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

I.- PRESUPUESTOS SUBJETIVOS

I.1. JURISDICCIÓN Y COMPETENCIA

Radicando la competencia genérica en el orden civil de la jurisdicción, detenta la competencia objetiva y funcional la Sección Civil del Tribunal de Instancia, por aplicación de lo dispuesto en los arts. 85.1 LOPJ y 45 LEC, y territorialmente es competente el Tribunal a que me dirijo, puesto que está prevenido el fuero territorial preceptivo específico para los juicios sobre cuestiones hereditarias, con arreglo a lo previsto en el art. 52.1.4.º LEC, del lugar del último domicilio del finado, siendo de este partido la población en que se hallaba la residencia donde murió D./Dña. [NOMBRE Y APELLIDOS]

I.2. CAPACIDAD Y LEGITIMACIÓN

Mi mandante D./Dña. [NOMBRE Y APELLIDOS] es persona física, mayor de edad, en pleno ejercicio de sus derechos civiles, así como lo es su medio-hermano demandado, D./Dña. [NOMBRE Y APELLIDOS], por lo que ambos tienen capacidad para ser parte y capacidad procesal ex arts. 6.1.1.º y 7.1 LEC.

Corresponde la legitimación activa directa a mi mandante, ya que es heredero forzoso legitimario, como hijo del causante, y está legitimado pasivamente de forma directa el demandado, en su condición de heredero testamentario.

Ciertamente, la viuda del causante es legataria en el mismo testamento, pero carece de legitimación pasiva, dado que no detenta institución como heredera en el testamento que, por la apreciación de la preterición del actor deba resultar reducida, sino que simplemente se le atribuye su cuota legal usufructuaria —no en abstracto, sino señalando bienes concretos para su pago—, y la viuda no puede ser afectada porque se estime o desestime la preterición del heredero forzoso: su cuota seguirá siendo de un tercio de la herencia. Como no se piden unos bienes determinados, asunto diferente será la computación y eventual complemento de legítima que pudiera proceder en ulterior juicio declarativo.

I.3. POSTULACIÓN Y DEFENSA

Conforme a los arts. 23 y 31 LEC se formula esta demanda por medio de representación a Procurador/a de los Tribunales con poder notarial para pleitos, y bajo dirección y firma de Letrado habilitado ante el Tribunal.

II.- PRESUPUESTOS OBJETIVOS

II.1. PROCEDIMIENTO

La presente demanda deberá sustanciarse por las normas del juicio ordinario, a tenor de lo prevenido en los arts. 248, 249.2 y 253.3 LEC, toda vez que ningún criterio de atribución preferente de la materia objeto del proceso resulta aplicable, puesto que la regla 12.ª del art. 251 LEC, referida a pleitos relativos a una herencia, se corresponde con condenas afectantes a los bienes o masas patrimoniales, y no a la mera declaración de ser heredero forzoso y el derecho a la legítima que constriñe los derechos hereditarios de los codemandados.

II.2. CUANTÍA

Cumpliendo lo prevenido en el art. 253.1 y 3 LEC, hacemos constar que la cuantía de esta demanda es indeterminada.

II.3. CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

II.4. REQUISITOS FORMALES

No aparecen, aparte de los requisitos genéricos de la demanda en juicio ordinario del art. 399 LEC, otros de carácter formal cuya falta, por el tipo de acción, invalidarían el proceso para pronunciarse sobre el fondo del asunto.

III.- FONDO DEL ASUNTO

A) FILIACIÓN.

Constatada la inscripción de nacimiento practicada en el Registro Civil de [LOCALIDAD], y por ende la filiación paterna y materna de mi representada, de conformidad con lo dispuesto en los arts. 113 CCiv, y 2, 3 y 4 de la Ley del Registro Civil, hace prueba del ‘status’ de filiación del nacido, y conforman un título de legitimación de dicho estado. Tal filiación inscrita goza no sólo de una presunción de exactitud en cuanto a su realidad, sino también de legalidad, entre tanto no se cancele o rectifique la inscripción. El art. 3 de la Ley del Registro Civil establece que no podrán impugnarse en juicio los hechos inscritos en el Registro sin que a la vez se inste la rectificación del asiento correspondiente.

B) PRETERICIÓN.

El antecedente en Derecho romano clásico de la institución legitimaria nace en una época concreta, cuando se vio con disfavor que el ‘pater familias’, no dejase nada —en cualquier forma— de su patrimonio hereditario, a determinadas personas ligadas a él por lazos íntimos. Se acoge entonces un deber ético de asistencia por razón de parentesco, que se proyecta sobre toda la herencia. Esta limitación a la libertad de testar, tuvo en el sentir social de Roma una concreta evolución jurídica, desde el Tribunal de los ‘Centumviri’, en los últimos tiempos de la República, exclusivamente para Roma, hasta la extensión de la acción de la ‘quaerella inofficiosi testamenti’, a los ‘civites’ que residían en las provincias; y esto por obra del Derecho Pretorio. Este modelo clásico del Derecho Romano configuraba una ‘pars bonorum’, y esa ‘quarella’ por el testamento inoficioso, que la vulneraba, podía producir, pero no siempre, la nulidad del testamento, cuando la privación de la porción legítima fuese ocasionada sin justa causa.

El art. 806 CCiv conceptúa legítima ‘la porción de bienes de que el testador no puede disponer por haberla reservado la Ley a determinados herederos, llamados por esto herederos forzosos’, planteándose la cuestión de su naturaleza jurídica, muy debatida en la doctrina: si es una porción de la herencia o conjunto patrimonial o ‘pars hereditatis’; una cuota ideal o valor o ‘pars valoris’; un cuota de valor en bienes concretos o ‘pars valoris bonorum’; o una porción de esos bienes concreto o ‘pars bonorum’. La STS de 26 de abril de 1997, Rec. 1689/1993, se ha decantado por la concepción de la legítima como ‘pars heredatis’, que ha de ser abonada con bienes de la herencia, ya que los legitimarios son cotitulares directos del activo hereditario, y no se les puede excluir de los bienes que lo integran, salvo en los supuestos expresamente previstos (cfr.: arts. 829, 838, 840 y párrafo 1.º del art. 1056 CCiv).

Los legitimarios, o herederos forzosos, aparecen descritos en el art. 807 CCiv: 1) Los hijos y descendientes respecto de sus padres y ascendientes; 2) A falta de los anteriores, los padres y ascendientes respecto de sus hijos y descendientes; y 3) El viudo o viuda en la forma y medida que establece este Código.

De la intangibilidad de la legítima trata, como institución de ‘Ius Cogens’, que se impone obligatoriamente al testador, el art. 813 CCiv, que establece que ‘el testador no podrá privar a los herederos de su legítima sino en los casos expresamente determinados por la Ley. Tampoco podrá imponer sobre ella gravamen, ni condición, ni sustitución de ninguna especie, salvo lo dispuesto en cuanto al usufructo del viudo’.

Y dicha intangibilidad aproxima la figura jurídica de la preterición (art. 814 CCiv) institución que fue modificada por la Ley 11/1981 de 13 de mayo, y siguiendo una orientación doctrinal —con antecedentes en las fuentes del Derecho Castellano—, distingue: entre la preterición intencional y la errónea o no intencional, señalando sus respectivos efectos.

La institución comentada, no se integra simplemente con el olvido u omisión, sino además requiere, que el heredero forzoso no haya percibido nada en concepto de legítima. Y es que, si algo hubiese tomado por tal razón el preterido, sólo podría ejercitar la acción de complemento de la legítima (art. 815 CCiv), pese a no haber sido mencionado dicho heredero forzoso en el testamento. Por otro lado, recogiendo la doctrina contenida en la anciana STS de 1 de julio de 1969, la desheredación y la preterición han de resultar exclusivamente del testamento, por ser ésta la expresión más solemne, de quien dispuso de sus bienes para después de su muerte.

Como expresa la más moderna STS de 7 de octubre de 2004, Rec. 1261/2001, la preterición protege al legitimario en la intangibilidad cuantitativa de su legítima. Como declaración de principio, el art. 814 CCiv comienza diciendo que la preterición de un heredero forzoso no perjudica la legítima, y termina previendo que, a salvo de las legítimas, tendrá preferencia en todo caso lo ordenado por el testador. De esta forma, la preterición del art. 814 CCiv, es una típica institución protectora de la legítima y puede ser definida como la omisión de los legitimarios en el testamento, sabiendo que existen —preterición intencional—, y sin que hayan recibido atribución alguna en concepto de legítima, pues si algo hubieran recibido lo que procedería es la acción de complemento aunque al legitimario no se le hubiera mencionado en el testamento.

Por otro lado, la preterición no intencional sólo puede presumirse cuando se deduzca sin dificultades esa falta de intención, esto es, cuando se trate de un error, de un mero defecto de trascripción o la preterición resulte del contenido de las propias disposiciones testamentarias sin que de su conjunto se deduzca que tal fuese la intención explícita del causante.

En el caso de autos es evidente que se da exactamente el concepto de preterición intencional: la omisión de un legitimario en el testamento, la hija demandante, Don/Doña [NOMBRE Y APELLIDOS], sabiendo que existe y que no ha recibido nada en concepto de legítima.

El efecto de la preterición intencional viene, como regla de principio, en el inicio del art. 814 CCiv: la preterición de un heredero forzoso (legitimario) no perjudica la legítima. Y siguiendo la STS de 9 de julio de 2002, Rec. 3383/2000, el efecto de la preterición intencional lo concreta el mismo art. 814: se reducirá la institución de heredero y se satisfará la legítima en la medida, en el presente caso, que establece el art. 808. Y como aclara la STS de 6 de abril de 1998, Rec. 301/1994, ello ha de comportar que la institución de heredero hecha, en favor del demandado D./Dña. [NOMBRE Y APELLIDOS], deba ser anulada, pero no en su totalidad sino en cuanto perjudique al heredero forzoso intencionalmente preterido —lo mismo que para la desheredación injusta (art. 851 CCiv)—. Nulidad de la institución de heredero, tan sólo en cuanto signifique perjuicio al preterido, con pervivencia de los legados, mejoras y demás disposiciones testamentarias en lo que no perjudiquen a la legítima de aquél. Del todo equivalente que cuando el testador conoce la existencia de un heredero forzoso, y sin embargo lo ignora en absoluto en el testamento, omitiéndolo en él (preterición), a que lo desherede sin expresión de causa, o con una contradicha y no es probada, o que no sea de las establecidas por la ley para desheredar.

La legítima no es la larga —dos tercios, conforme al art. 808, párrafo 1.º CCiv—, ya que la legítima de los hijos y descendientes son las dos terceras partes del haber hereditario del padre y de la madre, sin embargo de que podrán éstos disponer de una parte de las dos que forman la legítima, para aplicarla como mejora a sus hijos o descendientes, siendo la tercera parte restante de libre disposición. El derecho del preterido es a legítima estricta o corta, es decir, un tercio, ya que la voluntad del causante, soberano de su sucesión, fue el privarle del todo, aunque por ley se le atribuye una parte (legítima corta) que corresponde a lo que, dentro de su libre disposición (entre hijos) voluntariamente nunca le quiso atribuir, pero forzosamente corresponde. La normativa imperativa de la legítima no alcanza a aquella parte —la mejora— que sí es disponible, aunque la disponibilidad venga limitada al otro hijo o descendiente (SSTS de 6 de abril de 1998, Rec. 301/1994 ó 9 de julio de 2002, Rec. 3383/2000).

IV.- COSTAS

Conforme al principio del art. 394.1 LEC, del vencimiento objetivo, las costas irrogadas a esta parte en el juicio declarativo en la primera instancia se han de pronunciar a cargo del demandado.

Por todo lo expuesto,

SUPLICO AL TRIBUNAL

que teniendo por presentado este escrito, con sus copias y documentos que se acompañan, se sirva admitir uno y otros; en su virtud tener por interpuesta en la representación que ostento, la presente demanda de Juicio declarativo Ordinario contra D./Dña. [NOMBRE Y APELLIDOS], quien deberá ser emplazado a fin de que pueda contestar, si a su derecho le conviene, y previos los oportunos trámites legales, en su día dicte sentencia por la que se declare que mi patrocinada, Don/Doña [NOMBRE Y APELLIDOS] es heredera forzosa de su padre fallecido D./Dña. [NOMBRE Y APELLIDOS], acordando la reducción de la institución de heredero efectuada por el testador D./Dña. [NOMBRE Y APELLIDOS] a favor de su hijo D./Dña. [NOMBRE Y APELLIDOS], en el testamento otorgado en fecha [FECHA DEL TESTAMENTO], en cuanto perjudique los derechos, limitados a la legitima estricta, de mi patrocinada como heredera forzosa intencionalmente preterida, con expresa imposición de las costas procesales al demandado que se oponga.

OTROSÍ DIGO: Que siendo general para pleitos el poder que presenta la Procurador/a suscrita, y precisándolo para otros usos.

Por lo expuesto,

AL TRIBUNAL SUPLICO

que, teniendo por hecha la afirmación anterior, se acuerde el desglose de la copia auténtica del poder para pleitos y la devolución a esta parte.

Es Justo en el mismo lugar y fecha arriba indicados.

Es justicia de hacerse en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a
