---
name: peticion-monitorio-gastos-comunes-impagados-comunidad-civ-1157
description: "Petición de monitorio por gastos comunes impagados de una comunidad, con abogado y procurador. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Petición de monitorio por gastos comunes impagados de una comunidad, con abogado y procurador

> Formulario **CIV-1157** del plugin **Cobrar deudas: monitorio y cambiario** (`formularios-reclamar-deudas-monitorio`) · Civil › Monitorio y cambiario · normativa revisada el 24-11-2026.

## Qué es

Escrito de petición inicial de proceso monitorio, presentado por la comunidad de propietarios (con abogado y procurador) contra un propietario moroso, para reclamar los gastos comunes vencidos y no satisfechos, con solicitud de embargo preventivo para el caso de oposición (art. 21 de la Ley de Propiedad Horizontal).

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Petición de monitorio por gastos comunes impagados de una comunidad, con abogado y procurador» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Petición de monitorio por gastos comunes impagados de una comunidad, con abogado y procurador” para mi caso». También puedes invocarla directamente con `/formularios-reclamar-deudas-monitorio:peticion-monitorio-gastos-comunes-impagados-comunidad-civ-1157`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-reclamar-deudas-monitorio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Cobrar deudas: monitorio y cambiario) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (8 veces)
- [ ] Nº (5 veces)
- [ ] FECHA (4 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] CALLE (3 veces)
- [ ] MES Y AÑO (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR (2 veces)
- [ ] PISO (2 veces)
- [ ] DNI/NIE
- [ ] ESTADO CIVIL
- [ ] FECHAS
- [ ] NOMBRE Y APELLIDOS DEL DEUDOR
- [ ] NOMBRE Y APELLIDOS DEL LETRADO
- [ ] Nº DE COLEGIADO
- [ ] PORCENTAJE
- [ ] PROFESIÓN
- [ ] SEDE

## Normas que cita el formulario

- art. 9.1.e Ley 49/1960
- art. 813 LEC
- art. 5 Ley Orgánica 1/2025
- art. 812.1 LEC
- art. 21 LPH
- art. 21.3 LPH
- art. 21.5 LPH
- art. 394 LEC
- art. 21.4 LPH
- art. 812 Ley 1/2000
- art. 21 Ley 49/1960
- art. 217.2 LEC

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

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR], Procurador de los Tribunales, en nombre y representación de la Comunidad de Propietarios del inmueble sito en [LOCALIDAD], calle [CALLE], número [Nº], en méritos de la copia de escritura de poder otorgado por la misma, ante el Tribunal comparezco y, como mejor proceda en Derecho,

DIGO:

Que en nombre de mi representada insto proceso monitorio contra D./Dña. [NOMBRE Y APELLIDOS DEL DEUDOR], con DNI [DNI/NIE], mayor de edad, estado civil [ESTADO CIVIL], de profesión [PROFESIÓN] y con domicilio a efectos de notificaciones y citaciones en [LOCALIDAD], calle [CALLE], número [Nº], piso [PISO].

Se ampara esta solicitud en el supuesto del art. 812.2.2.º de la Ley de Enjuiciamiento Civil y tiene por objeto que el demandado pague a la comunidad a la que represento la cantidad de [IMPORTE] euros, que adeuda en concepto de gastos de comunidad vencidos, reclamados y no satisfechos, y [IMPORTE] euros más de gastos efectuados para el requerimiento de pago de dicha deuda.

Se apoya esta pretensión en los siguientes

HECHOS

PRIMERO.- El demandado es titular propietario del piso [PISO] de la finca sita en [LOCALIDAD], calle [CALLE], número [Nº], al que corresponde, según escritura y estatutos, una participación del [PORCENTAJE]% en los elementos comunes y, por lo tanto, en la obligación de pago de los gastos comunes de mantenimiento y conservación (art. 9.1.e) de la Ley 49/1960, de 21 de julio, de Propiedad Horizontal, LPH).

En aplicación de dicho porcentaje se han ido estableciendo las cantidades que a cada miembro de la Comunidad corresponde pagar, resultando que, al día de la fecha, el demandado no ha satisfecho las cuotas correspondientes a los meses de [MES Y AÑO] a [MES Y AÑO], ambos inclusive, que suman un total de [IMPORTE] euros.

SEGUNDO.- Ante la reticencia del demandado en su dejación de pago, se llevó la cuestión al orden del día de la Junta celebrada en fecha [FECHA], en la que se acordó proceder judicialmente contra el demandado para el cobro de dicha cantidad, en caso de que la misma no fuera satisfecha, facultándose al Presidente/a para entablar el proceso monitorio correspondiente y, asimismo, para otorgar poderes a Abogados y Procuradores con la misma finalidad.

Que, aunque el demandado conoce la deuda y los acuerdos de la Junta por remisión de copia de las actas, en fecha [FECHA] la Comunidad le notificó dicha deuda por carta notarial, con la advertencia de que, de no pagar en el plazo de quince días, sería exigida por vía judicial, sin que hasta el momento haya procedido a la satisfacción de la deuda, requerimiento que supuso gastos a la Comunidad en la cantidad de [IMPORTE] euros.

Se acompañan al presente: la liquidación certificada de la deuda, que se notificó fehacientemente al deudor según el justificante que se adjunta a la misma, y nota de los gastos ocasionados por dicho requerimiento; certificación del acta de la Junta expedida por el Secretario de la Comunidad, que lleva el visto bueno del Presidente, en la que se aprueba la liquidación de la deuda previa a su notificación al demandado; y certificación de la Junta en la que se confirió facultades al Presidente para proceder judicialmente y nombrar Abogados y Procuradores.

TERCERO.- La parte actora manifiesta que, previo a la presentación de la presente demanda, se han llevado a cabo negociaciones con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria, incluyéndose entre las acciones realizadas el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución.

Finalmente, mi representada envió un requerimiento fehaciente al demandado con fecha [FECHA], fijando un plazo de 30 días naturales para llegar a un acuerdo amistoso, a través del abogado que firma este escrito, el cual fue contestado por el demandado por el mismo medio, [ELEGIR: rechazando el acuerdo / habiendo sido solo posible un acuerdo parcial], viéndonos en la necesidad de acudir a la presente vía judicial respecto a los extremos de la controversia en los que se mantiene la discrepancia.

Acompaño como documento n.º [Nº] el requerimiento efectuado y como documento n.º [Nº] la contestación del demandado.

FUNDAMENTOS DE DERECHO

COMPETENCIA:

Conforme al art. 813 LEC, corresponde exclusivamente el conocimiento de este proceso a la Sección Civil del Tribunal de Instancia del domicilio del demandado, que es también en este caso el del lugar donde se halla la finca.

PROCEDIMIENTO:

Corresponde el monitorio regulado en los arts. 812 y ss. LEC.

CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD:

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4.º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

MATERIALES O DE FONDO:

Se exige el pago de deuda dineraria, determinada, vencida y exigible (art. 812.1 LEC). Se acreditan los requisitos del art. 812.2.2.º (certificación de impago de las cuotas devengadas por gastos comunes) y los de la Ley de Propiedad Horizontal (art. 21 LPH, según la redacción dada por la Ley 10/2022, de 14 de junio) en cuanto al acuerdo de la Junta de propietarios para proceder judicialmente contra el deudor y las facultades conferidas al Presidente para actuar en su nombre y otorgar poderes al efecto a favor de Procuradores y Abogados.

Consta asimismo la notificación y requerimiento previos hechos al demandado (art. 21.3 LPH).

INTERVENCIÓN DE ABOGADO Y PROCURADOR:

Se presenta esta demanda por medio de Abogado y Procurador, conforme autoriza el art. 21.5 LPH.

COSTAS:

Las costas han de imponerse a la parte demandada en los términos previstos por el art. 21.5 LPH y el art. 394 LEC.

Por lo expuesto,

SUPLICO AL TRIBUNAL, que, teniendo por presentado este escrito, lo admita y tenga por promovido proceso monitorio y, teniéndome por comparecido y parte, ordene que se entiendan conmigo las sucesivas actuaciones, y mande formular requerimiento de pago al deudor de la cantidad de [IMPORTE] euros y, en caso de desatención del mismo y previa petición de parte, dicte auto despachando ejecución, en su caso, por dicha cantidad como principal, más los intereses procesales, gastos y costas a que diere lugar el proceso ejecutivo.

OTROSÍ DIGO: Que, de conformidad con lo previsto en el artículo 21.4 LPH, para el caso de que el demandado se oponga a la petición inicial de este proceso monitorio, procede el embargo preventivo de la finca por el importe de [IMPORTE] euros, para hacer frente a la cantidad reclamada, de [IMPORTE] euros, y la presupuestada para intereses y costas, de [IMPORTE] euros. Los datos son [INDICAR LOS DATOS REGISTRALES, QUE NORMALMENTE SERÁN LOS DE LA FINCA OBJETO DE LA DEUDA, AUNQUE NADA IMPIDE QUE PUEDA SER OTRA DIFERENTE, PUESTO QUE EL ART. 21.4 LPH SE REFIERE EN GENERAL A BIENES DEL DEUDOR].

OTROSÍ DIGO: Que se acuerde en consecuencia, conforme a lo solicitado, salvo que aporte garantía suficiente, a tenor del apartado 4, párrafo 2.º, del citado precepto legal.

Por ser de justicia que pido en [LOCALIDAD], a [FECHA].

Firma del Abogado/a: [NOMBRE Y APELLIDOS DEL LETRADO] — Col. n.º [Nº DE COLEGIADO]

Firma del Procurador/a: [NOMBRE Y APELLIDOS DEL PROCURADOR]

NOTAS DE USO

1. Normativa aplicable: arts. 812 a 818 de la Ley 1/2000, de 7 de enero, de Enjuiciamiento Civil; art. 21 de la Ley 49/1960, de 21 de julio, de Propiedad Horizontal.

2. Jurisprudencia de interés.

Sentencia de la Audiencia Provincial de Valencia de 30 de septiembre de 2011, rec. 321/2011:

Falta de legitimación activa por carecer el administrador de la representación de la comunidad: conforme al artículo 21 de la Ley de Propiedad Horizontal, las obligaciones derivadas del artículo 9, apartados e) y f), de la propia ley deberán cumplirse por el propietario de la vivienda o local en el tiempo y forma determinados por la Junta, facultando al presidente o al administrador de la comunidad, si así lo acordase aquélla, a exigirlo judicialmente a través del proceso monitorio. Conforme a la documentación aportada al procedimiento monitorio, la Junta de propietarios acordó, entre otros temas, liquidar la deuda que mantiene el propietario demandado con la comunidad, así como demandar al mismo, autorizando al presidente y al administrador, indistintamente, para que en nombre y representación de la comunidad contraten los servicios de abogado y procurador, sea preceptiva o no su intervención. En consecuencia, permitiendo la ley que sea el administrador el que exija en nombre de la comunidad el pago de deudas que mantenga el comunero con ella, y resultando probado que quien actuó en nombre de la sociedad administradora fue designado administrador, procede reputarlo facultado para otorgar poderes a procuradores en representación de la comunidad para el inicio del procedimiento monitorio cuya oposición determinó la incoación del juicio verbal, con desestimación del motivo de recurso.

Documentación apta para la admisión de la solicitud monitoria: de acuerdo con lo dispuesto en el artículo 812 de la Ley de Enjuiciamiento Civil, en relación con los artículos 814 y 815, se exige para el supuesto que nos ocupa que la deuda se acredite mediante certificación de impago de cantidades debidas en concepto de gastos comunes de comunidades de propietarios de bienes inmuebles urbanos, lo que lleva al artículo 21 de la Ley de Propiedad Horizontal, conforme al cual la utilización del procedimiento monitorio requerirá la previa certificación del acuerdo de la Junta aprobando la liquidación de la deuda con la comunidad de propietarios por quien actúe como secretario de la misma, con el visto bueno del presidente, siempre que tal acuerdo haya sido notificado a los propietarios afectados en la forma establecida en el artículo 9, esto es, en el domicilio designado por el propietario a tal efecto o, en su defecto, en el propio piso o local perteneciente a la comunidad, surtiendo plenos efectos las notificaciones entregadas al ocupante del mismo. No puede exigirse más documentación que la dicha por el legislador, no siendo necesario aportar las actas levantadas con ocasión de otras Juntas en las que se adoptaron acuerdos de ejecución de obras, ni de las que resulte la cuota de participación en elementos comunes, ni documental acreditativa de la notificación de acuerdos a los diversos propietarios obligados en virtud de ellos, ni el título constitutivo de la propiedad horizontal.

Impugnación del acuerdo liquidatorio: adoptado el acuerdo liquidatorio de la deuda, compete al propietario disidente la impugnación del mismo a través del procedimiento legalmente establecido (artículo 18 de la Ley de Propiedad Horizontal), en el que habrá de interesar la suspensión del acto con carácter cautelar (apartado 4 del propio precepto) para paliar los efectos ejecutivos del acuerdo adoptado, sin que le sea dable pretender en el procedimiento de reclamación de la deuda suspender tales efectos por los motivos que debió hacer valer como demandante en aquél. Consecuentemente, alegaciones tales como las de exención en el pago de gastos derivados de ascensor, patio, carencia de acceso directo al zaguán, consideración de los gastos como de mera ornamentación, instalación de servicios cuyo pago exceda de tres mensualidades o falta de notificación de acuerdos adoptados en Junta de los que deriven las concretas partidas integrantes del saldo deudor cuyo pago se exige, han de ser desestimadas sin entrar siquiera a conocer de ellas, por no ser éste el procedimiento en el que han de ventilarse.

Sentencia de la Audiencia Provincial de A Coruña de 8 de julio de 2009, rec. 382/2009:

A los efectos de admisión a trámite de la petición monitoria, el juez únicamente ha de comprobar, so pena de desnaturalizar el procedimiento, si con la petición monitoria se han presentado documentos que, integrados con las alegaciones del acreedor sobre el origen y cuantía de la deuda, constituyen un principio de prueba acreditativo de la realidad de la misma, sin que pueda exigirse, en este momento procesal, una justificación plena de la existencia o certeza del crédito. Lo que pide el legislador es una aportación documental significativa de una «buena apariencia jurídica de la deuda». La prueba plena es necesaria para la condena del deudor; pero, en este primer trance del procedimiento, únicamente se resuelve sobre la admisión de la petición monitoria. Si el deudor se opusiera a la reclamación, se remitiría a las partes al juicio declarativo verbal u ordinario procedente por razón de la cuantía, en el cual el actor deberá justificar debidamente, con rigurosidad procesal, los hechos constitutivos de su pretensión pecuniaria, pues la insuficiencia o deficiencia probatoria sobre ellos correrá en su contra, según las reglas distributivas de la carga de la prueba del art. 217.2 LEC.

La técnica monitoria documental se fundamenta no solo en la aportación de un principio de prueba, sino también, y especialmente, en la falta de exteriorización de la oposición del deudor a la reclamación que se le efectúa, bajo expreso apercibimiento de que, si no alega nada en su contra, el juez dictará auto despachando ejecución sobre sus bienes.

Los documentos a los que se refiere el art. 812, es decir, los que constituyan el principio de prueba de la buena apariencia jurídica de la deuda que se reclama, no conforman una relación cerrada o numerus clausus, sino una relación abierta o numerus apertus, en la cual se ejemplifican supuestos que el legislador considera idóneos a tales efectos, sin excluir otros. Los documentos base del monitorio son de lo más heterogéneo: pueden ser públicos o privados, bilaterales o unilateralmente creados por el promovente, hallarse suscritos o no por el deudor, plasmados en papel o en cualquier soporte físico, pues lo fundamental es que sean constitutivos o sugerentes de una apariencia de deuda.
