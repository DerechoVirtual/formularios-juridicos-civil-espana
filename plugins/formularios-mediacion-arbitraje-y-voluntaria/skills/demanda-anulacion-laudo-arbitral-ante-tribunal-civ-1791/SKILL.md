---
name: demanda-anulacion-laudo-arbitral-ante-tribunal-civ-1791
description: "Demanda de anulación de laudo arbitral ante el Tribunal Superior de Justicia. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de anulación de laudo arbitral ante el Tribunal Superior de Justicia

> Formulario **CIV-1791** del plugin **Mediación, MASC, arbitraje y jurisdicción voluntaria** (`formularios-mediacion-arbitraje-y-voluntaria`) · Civil › Jurisdicción voluntaria, MASC, mediación y arbitraje · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de anulación de laudo arbitral ante el Tribunal Superior de Justicia» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de anulación de laudo arbitral ante el Tribunal Superior de Justicia” para mi caso». También puedes invocarla directamente con `/formularios-mediacion-arbitraje-y-voluntaria:demanda-anulacion-laudo-arbitral-ante-tribunal-civ-1791`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-mediacion-arbitraje-y-voluntaria:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Mediación, MASC, arbitraje y jurisdicción voluntaria) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (11 veces)
- [ ] LOCALIDAD (9 veces)
- [ ] DENOMINACIÓN SOCIAL (6 veces)
- [ ] FECHA (5 veces)
- [ ] NÚMERO (4 veces)
- [ ] CALLE (2 veces)
- [ ] Nº (2 veces)
- [ ] AÑO
- [ ] DOMICILIO
- [ ] LUGAR
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] PROFESIÓN
- [ ] TELÉFONO

## Normas que cita el formulario

- art. 40 Ley 60/2003
- art. 73.1.c LOPJ
- art. 399 LEC
- art. 3 TRLGDCU
- art. 13 Ley 11/2022
- art. 79 Ley 7/1985
- art. 330 LEC

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

### Avisos de actualización (0) — se aplican en el texto, nunca se copian en el documento

- Ninguno.

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

Demanda, dirigida al Tribunal Superior de Justicia, en ejercicio de acción de anulación de laudo arbitral por haber resuelto los árbitros sobre cuestiones que no pueden ser objeto de arbitraje.

A LA SALA DE LO CIVIL DEL TRIBUNAL SUPERIOR DE JUSTICIA DE LA COMUNIDAD AUTÓNOMA DE [LOCALIDAD]

D./DÑA. [NOMBRE Y APELLIDOS], Procurador de los Tribunales, en representación de [NOMBRE DEL REPRESENTADO/A], según acredito mediante escritura de poder que acompaño en forma, bajo la dirección del Letrado abajo firmante D./DÑA. [NOMBRE Y APELLIDOS], colegiado con n.º [NÚMERO] en el Iltre. Colegio de Abogado/as de [LOCALIDAD], con despacho profesional abierto en [LOCALIDAD]; comparezco ante la Sala y DIGO:

Que con fecha [FECHA] le ha sido notificado a esta parte el Laudo de fecha [FECHA], recaído en el expediente [Nº] / [Nº] de la Junta Arbitral de Consumo de [LOCALIDAD].

Que estimando esta parte, dicho sea con el mayor respeto y en mérito de defensa, que dicho Laudo no es ajustado a Derecho y por ello notablemente perjudicial para los intereses de mi patrocinado, es por lo que, por medio del presente escrito, en tiempo hábil y forma legal, se ejercita ACCIÓN DE ANULACIÓN DEL LAUDO al amparo de los arts. 40 a 42 de la Ley 60/2003, de 23 de diciembre, de Arbitraje (en adelante, LA), frente a D./Dña. [NOMBRE Y APELLIDOS] mayor de edad, casado —en su caso—, de profesión [PROFESIÓN], con domicilio en: [DOMICILIO]; y con número de teléfono/fax [TELÉFONO].

Fundamento la misma en los siguientes hechos y consideraciones jurídicas:

HECHOS

PRIMERO.- D./Dña. [NOMBRE Y APELLIDOS] presentó escrito de solicitud de arbitraje a través de la UCA-UCE Unión de Consumidores de [LOCALIDAD], que la remitió a la Junta Arbitral de Consumo de

SEGUNDO.- Estando adherida la mercantil [DENOMINACIÓN SOCIAL] al sistema arbitral de consumo regulado por el RD 713/2024, de 23 de julio, la Junta Arbitral de Consumo de [LOCALIDAD] tuvo por formalizado el convenio y tramitó el expediente en el que se reclamaba la retirada de una línea telefónica situada por encima del parapeto de la vivienda de D./DÑA. [NOMBRE Y APELLIDOS] y que se restaurara la fachada, reclamando la reparación de los desperfectos ocasionados en la fachada del inmueble del reclamante, la retirada del cable y la canalización subterránea del mismo.

TERCERO.- El Colegio Arbitral con fecha [FECHA] emitió Laudo resolviendo estimar la pretensión de D./DÑA. [NOMBRE Y APELLIDOS] debiendo proceder la Compañía [DENOMINACIÓN SOCIAL], a la canalización subterránea y a reparar los defectos de la fachada.

FUNDAMENTOS DE DERECHO

A) JURÍDICO PROCESALES

I.- COMPETENCIA. Es competente la Sala a la que tenemos el honor de dirigirnos, conforme a los arts. 73.1.c) LOPJ, y 8.5 LA.

II.- PLAZO. La acción se interpone por medio de escrito motivado dentro del plazo de los dos meses días siguientes a la notificación del Laudo (art. 41.4 LA), dado que no se ha solicitado ulterior corrección, aclaración o complemento.

III.- CAPACIDAD Y LEGITIMACIÓN. Mi mandante tiene capacidad para ser parte por ministerio de la ley, como persona jurídico mercantil constituida e inscrita con arreglo al Derecho español, y la capacidad procesal o para comparecer en juicio corresponde a sus representantes legales (arts. 6.1.3.º y 7.4 LEC).

El demandado es persona física, mayor de edad, en pleno ejercicio de sus derechos civiles, por lo que tiene capacidad para ser parte y capacidad procesal ex arts. 6.1.1.º y 7.1 LEC,

Ambas partes están legitimadas en el presente procedimiento, mi mandante en concepto de condenado por el laudo y la contraparte en concepto de reclamante.

IV.- PROCEDIMIENTO. El del juicio verbal con las matizaciones del art. 42.1 LA, lo que implica comparecencia mediante Procurador y dirigida la parte técnicamente por Letrado, al no incurrirse en la salvedad de los arts. 23.2.1.º y 31.2.1.º LEC, dado el valor de la demanda por el importe de la condena del Laudo.

Asimismo esta demanda reúne los requisitos del art. 399 LEC, acompañando además los documentos justificativos de la pretensión, del convenio arbitral, constituido mediante régimen de arbitraje de consumo, y del laudo impugnado, y proponiendo prueba.

V.- COSTAS. Aplicación del criterio del vencimiento objetivo.

B) JURÍDICO MATERIALES

Las alegaciones jurídico-materiales que fundamentan esta demanda se refieren a las siguientes cuestiones, al amparo de las letras e) y f) del apartado 1 del art. 41 LA.

El laudo del expediente n.º [NÚMERO]/[AÑO], notificado el día [FECHA] ES NULO por dos órdenes de razones:

1.º ES NULO POR HABER RESUELTO LOS ÁRBITROS SOBRE CUESTIONES QUE NO PUEDEN SER OBJETO DE ARBITRAJE.

Antes de entrar en el desarrollo concreto de nuestra argumentación, conviene traer a colación que, en la Ley de Arbitraje, la anulación del laudo, respecto de la que se destierra su denominación de recurso, técnicamente incorrecta, se trata de un proceso de impugnación de la validez del laudo por motivos tasados, los cuales, como regla general, no han de permitir la revisión del fondo de la decisión de los árbitros. Y tales, como destaca el apartado VIII de la propia Exposición de Motivos, son un elenco, distribuidos entre los apreciables de oficio o sólo a instancia de parte, inspirado en la Ley Modelo elaborada por la UNCITRAL de 21 de junio de 1985, recomendada por la Asamblea General de la ONU 40/72 de 11 de diciembre de 1985.

El caso concreto que traemos mediante la presente demanda, consiste en la solicitud de reparación de los daños sufridos en la fachada del inmueble propiedad del reclamante, como consecuencia de la retirada de un cable telefónico, así como la retirada del cable que atraviesa el vuelo de aquella y que se obligue a realizar su instalación mediante canalización subterránea.

Pues bien, toda la norma reguladora del arbitraje está en relación con los consumidores y usuarios, a quienes les da cabida en sus arbitrajes. Mediante el mandato constitucional recogido en el art. 51.1 de nuestra Constitución, ‘Los poderes públicos garantizarán la defensa de los consumidores y usuarios, protegiendo, mediante procedimientos eficaces, la seguridad, la salud y los legítimos intereses económicos de los mismos’.

Ello está en consonancia con los criterios de la Unión Europea (STC 71/1982 de 30 de noviembre de 1982, rec. 86/1982). Clarificadora es la STC 88/1986 de 1 de julio de 1986, rec. 352/1983, donde se dice que "la defensa de los consumidores y usuarios hace referencia a una situación en la que aquellos aparecen como destinatarios de unos productos ofrecidos por la empresas, productos cuyas condiciones de oferta se pretende regular protegiendo, como indica el art. 51.1 de la Constitución, la seguridad, la salud y los legítimos intereses económicos".

A partir del mandato constitucional, y para dar cumplimiento al mismo, se promulga primero la Ley 26/1984, de 19 de julio, General para la Defensa de los Consumidores y Usuarios —derogada por el Texto Refundido de la Ley General para la Defensa de los Consumidores y Usuarios, aprobado por Real Decreto Legislativo 1/2007, de 16 de noviembre—; después la Ley 36/1988, de 5 de diciembre, de Arbitraje —derogada por la Ley 60/2003, de 23 de diciembre—; y por último el Real Decreto 713/2024, de 23 de julio, por el que se aprueba el Reglamento que regula el Sistema Arbitral de Consumo.

El art. 1.2 del citado Real Decreto establece que "Mediante el arbitraje de consumo los órganos arbitrales resuelven de forma extrajudicial, con carácter vinculante y ejecutivo para las partes, los litigios, nacionales o transfronterizos, dirigidos a empresarios y que son sometidos a su decisión por consumidores o usuarios residentes en la Unión Europea al considerar que existe una vulneración de sus derechos legal o contractualmente reconocidos".

El objeto del arbitraje se concreta así en lo relativo a los derechos de los consumidores, lo que presupone que exista una relación de consumo, con base en una relación de derecho privado, contractual o extracontractual, en la que una persona física o jurídica aparece como destinataria final. El consumidor y usuario, definido en la ley, es la persona física que actúa con un propósito ajeno a su actividad comercial, empresarial, oficio o profesión (art. 3 TRLGDCU). Esto es, que interviene en las relaciones de consumo con fines privados, contratando bienes y servicios como destinatario final, sin incorporarlos, ni directa, ni indirectamente, en procesos de producción, comercialización o prestación a terceros. Consecuentemente, el objeto del arbitraje de consumo, es decir, el ámbito de aplicación material tiene como primer presupuesto la existencia entre las partes de una relación de derecho privado, contractual o extracontractual, dirigida a la adquisición utilización o disfrute de bienes y servicios, suministrados por una empresa, profesional o la Administración, que da lugar a una relación de consumo respecto de la cual una persona física o jurídica aparece como destinataria final, y por lo que es considerada a los efectos de la Ley como consumidora o usuaria. Como segundo presupuesto puede señalarse no estar comprendida dentro las materias que la propia normativa excluye de su ámbito (art. 2 del Real Decreto).

Pues bien, sentadas las bases conceptuales de lo que se entiende por las leyes precitadas, como consumidores y usuarios, y traído al caso objeto de la presente acción de anulación, es evidente que el carácter con el que el Sr./a., reclama, no coincide con el concepto de usuario del servicio telefónico, es decir, el derecho objeto de su reclamación es el de propiedad, y no el derecho que pueda derivarse de su cualidad de usuario de aquel servicio.

La pretensión de D./DÑA. [NOMBRE Y APELLIDOS] de retirada del cable y reparación de la fachada, concedida en el laudo, excede del ámbito del arbitraje de consumo, por cuanto a dicha parte no puede conceptuársele como consumidor o usuario respecto de lo interesado, ya que no tiene su fundamento en la adquisición y utilización o disfrute como destinatario final del servicio o actividad desplegado por

Los cables telefónicos son los portadores del soporte por donde circula la energía necesaria para llegar al destinatario final del servicio, servicio que se presta por mi representada y se usa por el reclamante, a través de la utilización del terminal o aparato telefónico. Todo lo que se derive de ese uso, estará el cliente legitimado para reclamar a quien contrató tal prestación y se obligó a ello, como es [DENOMINACIÓN SOCIAL], pero, evidentemente, el usuario no puede, utilizando esta condición, reclamar a quien le presta el servicio para proteger su derecho de propiedad sobre un inmueble.

Así, el señor que compra una botella de leche, no se le ocurrirá reclamar con su carácter de consumidor, a la empresa que suministra aquella, porque el camión que transportaba las cajas del citado producto, para llevarlo al supermercado y ponerlo a disposición de aquel, se salió de la calzada y precipitándose sobre su vivienda, la derribó. Como tampoco reclamaría con su carácter de usuario del servicio de correos, al cartero que ejerciendo sus funciones de repartidor de correspondencias y dirigiéndose al domicilio de aquel, tiene un accidente en carretera con el titular de ese domicilio.

Los ejemplos expuestos, aunque puedan parecer ridículos, son clarificadores por su analogía con el caso del reclamante, pues mi representada, para poder prestar el servicio telefónico tiene que transportar ese servicio a través de sus cables para ponerlo a disposición del usuario, y poder proceder a su utilización o consumo. Sin embargo, el reclamante utiliza su cualidad de usuario para proteger un derecho (el de propietario de un inmueble) que nada tiene que ver con la prestación del servicio telefónico, y sí, con el transporte de la materia prima de aquel servicio telefónico (corriente eléctrica que circula sobre un soporte de metal), y es ese transporte el que supuestamente daña su derecho de propiedad, no el propio consumo. Pero es que además, el cable que atraviesa el vuelo de su vivienda tiene una capacidad de 100 pares, es decir, cien abonados, y no precisamente el par que le da servicio a él mismo.

En definitiva, al hilo de lo expuesto, tenemos que concluir, como ya se alegó en la vista arbitral, que la Junta Arbitral no es competente para conocer de la reclamación, pues el reclamante no ejerce su pretensión desde su posición de usuario por una defectuosa prestación del servicio telefónico contratado. Resultando que el Laudo que se recurre en NULO, por haber resuelto los árbitros puntos que no pueden ser objeto de arbitraje.

2.º.- ES NULO POR SER CONTRARIO AL ORDEN PÚBLICO.

En relación con la obligación de realizar canalización subterránea del cable que atraviesa el vuelo del inmueble del reclamante, entiende esta parte que los árbitros no tienen competencia para obligar a mi representada la realización de la instalación de aquel modo.

El ‘orden público’ es un concepto indeterminado, habiendo declarado el Tribunal Constitucional, entre otras en Sentencia de 13 de febrero de 1985 que infringe el orden público quien conculca los derechos fundamentales y libertades públicas garantizadas por la Constitución, lo que se concreta en la conculcación de los derechos y libertades individuales sociales o colectivos e impide y menoscaba el normal desenvolvimiento de las instituciones, por lo que, en definitiva, son las libertades o derechos fundamentales de las personas los que los Tribunales han de tutelar, como dispone el art. 7 de la Ley Orgánica del Poder Judicial.

El laudo dictado por la Junta Arbitral de [LOCALIDAD] infringe el orden público porque vulnera el principio de seguridad jurídica reconocido en el art. 9 de nuestra Constitución, excediéndose a la hora de resolver la cuestión sometida a su consideración, obligando a [DENOMINACIÓN SOCIAL], a enterrar el tendido telefónico.

En este sentido, la posibilidad de canalización subterránea está sometida a las normas urbanísticas municipales, conforme a las previsiones del art. 13 de la Ley 11/2022, de 28 de junio, General de Telecomunicaciones. Es claro que la vía pública integra el dominio público municipal (arts. 79 de la Ley 7/1985, de 2 de abril, de Bases de Régimen Local; 74 del Real Decreto Legislativo 781/1986, de 18 de abril, por el que se aprueba el Texto Refundido de Disposiciones Vigentes en materia de Régimen Local; y 3 del Reglamento de Bienes de las Corporaciones Locales, aprobado por Real Decreto 1372/1986 de 13 de junio).

Por consiguiente, el Colegio Arbitral carece de competencias para obligar a [DENOMINACIÓN SOCIAL], a realizar una canalización subterránea ya que la misma supone utilización de la vía pública y lo contrario significaría, además, invadir competencias municipales. Lo que está también en relación con el art. 2.1 LA, al ser ello una materia sobre las que las partes no tienen poder disposición, como es el bien público por donde se tendría que canalizar.

Por lo expuesto,

SUPLICO A LA SALA:

Que teniendo por presentado este escrito con sus copias y documentos, se digne admitir uno y otros, se sirva tener a mi representada como comparecida y parte en calidad de demandante de juicio verbal en reclamación de anulación de laudo arbitral frente a D./Dña. [NOMBRE Y APELLIDOS], de manera que seguido el oportuno procedimiento, venga a dictar sentencia que declare la nulidad plena del laudo arbitral consignado al principio de este escrito, dejándolo sin efecto alguno, y condenando en costas a la parte demandada que se opusiere.

Por ser de Justicia que pido en [LUGAR], a [FECHA].

OTROSÍ PRIMERO DIGO: Se solicita la celebración de vista, como autoriza el art. 42.1.c) LA.

SUPLICO A LA SALA: Que, teniendo por causada la manifestación anterior a los efectos oportunos, se sirva señalar por el Letrado de la Administración de Justicia la celebración de vista, como es procedente en Justicia que reitero.

OTROSÍ SEGUNDO DIGO: Que interesa al derecho de esta parte valerse para el acto de la vista de los siguientes medios de

PRUEBA

I.- INTERROGATORIO DE LA PARTE CONTRARIA, a fin de que sea citado D./Dña. [NOMBRE Y APELLIDOS], con los apercibimientos legales de poder ser tenidos por ciertos los hechos relevantes en que tuvo intervención personal y que le perjudiquen, en supuesto de inasistencia o de respuestas evasivas o inconcluyentes

II.- DOCUMENTAL privada, consistente en que se tengan por unidos a las actuaciones los documentos acompañados con este escrito de demanda, y asimismo, de acuerdo con el art. 330 LEC, se solicite de los miembros del Colegio arbitral intervinientes la entrega de todas las actuaciones llevadas a cabo, y que no se han entregado a esta parte.

III.- PERICIAL, de un técnico de telecomunicaciones [NOMBRE Y APELLIDOS], lo cual se articulará en el acto de la vista.

IV.- TESTIFICAL, a fin de que sean citados judicialmente los siguientes individuos:

Representante necesario de la entidad [DENOMINACIÓN SOCIAL], con domicilio en [LOCALIDAD], calle [CALLE], n.º [NÚMERO]

D./Dña. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], calle [CALLE], n.º [NÚMERO]

SUPLICO A LA SALA: Que teniendo por causadas las anteriores manifestaciones a los efectos oportunos, se digne ordenar lo conducente a la rápida y eficaz práctica de lo interesado, como es Justicia que reitero en lugar y fecha ‘ut supra’.

Firma de Abogado/a	Firma de Procurador/a

========================================================================
