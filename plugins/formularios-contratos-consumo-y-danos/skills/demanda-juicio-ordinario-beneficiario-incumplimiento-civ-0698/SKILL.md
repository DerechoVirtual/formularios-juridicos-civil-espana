---
name: demanda-juicio-ordinario-beneficiario-incumplimiento-civ-0698
description: "Demanda de juicio ordinario del beneficiario por incumplimiento de un seguro de accidentes. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio ordinario del beneficiario por incumplimiento de un seguro de accidentes

> Formulario **CIV-0698** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio ordinario del beneficiario de un seguro de accidentes contra la aseguradora que rehúsa pagar el capital por fallecimiento (p. ej. infarto de miocardio desencadenado por estrés laboral) alegando que la causa no es un accidente a efectos del art. 100 LCS. Reclama el capital y los intereses del art. 20 LCS.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio ordinario del beneficiario por incumplimiento de un seguro de accidentes» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio ordinario del beneficiario por incumplimiento de un seguro de accidentes” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:demanda-juicio-ordinario-beneficiario-incumplimiento-civ-0698`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (8 veces)
- [ ] NOMBRE Y APELLIDOS DEL ASEGURADO (4 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] MES (3 veces)
- [ ] SEDE (3 veces)
- [ ] AÑO (2 veces)
- [ ] DENOMINACIÓN SOCIAL DE LA ASEGURADORA (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] FECHA (2 veces)
- [ ] FIRMA (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] CIRCUNSTANCIAS EN LAS QUE SE PRODUJO EL FALLECIMIENTO
- [ ] CONTENIDO DE LA CONTESTACIÓN
- [ ] CORREO ELECTRÓNICO
- [ ] DOMICILIO PROFESIONAL
- [ ] DÍA
- [ ] EL ASEGURADO / LA ASEGURADA
- [ ] EMPLEADOR
- [ ] NOMBRE Y APELLIDOS DEL DEMANDANTE
- [ ] NOMBRE Y APELLIDOS DEL LETRADO/A
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] Nº DE INSCRIPCIÓN
- [ ] Nº DE PROCEDIMIENTO
- [ ] Nº DE PÓLIZA
- [ ] PROFESIÓN
- [ ] TELÉFONO

## Normas que cita el formulario

- art. 399.1 LEC
- art. 100 LCS
- art. 9.2 LOPJ
- art. 45 LEC
- art. 85.1 LOPJ
- art. 68 LEC
- art. 52.2 LEC
- art. 24 LCS
- art. 6.1.3.º LEC
- art. 7.4 LEC
- art. 1 LCS
- art. 251 LEC
- art. 1790 CC
- art. 1254 CC
- art. 18 LCS
- art. 20 LCS
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

### Avisos de actualización (2) — se aplican en el texto, nunca se copian en el documento

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «… de [MES] de [AÑO]. Firma del Abogado/a: [FIRMA] Firma del Procurador/a: [FIRMA]»: requisito de procedibilidad (art. 5 LO 1/2025): antes de demandar hay que intentar un medio adecuado de solución de controversias y acreditarlo con la demanda, salvo las materias excluidas del art. 5.2.

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

[NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, en nombre y representación de [NOMBRE Y APELLIDOS DEL DEMANDANTE], con domicilio en [LOCALIDAD], calle [DOMICILIO], según acredito con la escritura de poder inscrita en el Registro Electrónico de Apoderamientos Judiciales con el nº [Nº DE INSCRIPCIÓN]; asistido/a por el Letrado/a en ejercicio abajo firmante [NOMBRE Y APELLIDOS DEL LETRADO/A], con despacho profesional en [DOMICILIO PROFESIONAL], ante el Tribunal comparezco y como mejor proceda en Derecho, DIGO:

Que mediante el presente escrito interpongo DEMANDA DE JUICIO ORDINARIO en reclamación de cantidad contra la entidad [DENOMINACIÓN SOCIAL DE LA ASEGURADORA], domiciliada en [DOMICILIO].

Que esta parte asume el compromiso de recibir cualquier comunicación dirigida por la oficina judicial, durante toda la fase declarativa e, incluso, en una eventual fase de ejecución, por medios telemáticos, en términos del art. 399.1 II LEC, consignándose a estos efectos la siguiente dirección de correo electrónico y número de teléfono: [CORREO ELECTRÓNICO] / [TELÉFONO].

Sirvan a la misma los siguientes:

HECHOS

PRIMERO.- Mi representado/a tiene la condición de beneficiario/a de la póliza de seguro de accidentes n.º [Nº DE PÓLIZA], cuya copia se acompaña señalada como documento número [Nº].

Dicha póliza fue suscrita por [ELEGIR: su difunto esposo / su difunta esposa / su difunto familiar], [NOMBRE Y APELLIDOS DEL ASEGURADO], en la que se concertó un capital de [IMPORTE] euros para el riesgo en caso de fallecimiento por accidente.

SEGUNDO.- Con fecha [FECHA], [NOMBRE Y APELLIDOS DEL ASEGURADO], [PROFESIÓN] que prestaba sus servicios para [EMPLEADOR], falleció a causa de [CAUSA DEL FALLECIMIENTO, p. ej. infarto agudo de miocardio] que sufrió cuando [CIRCUNSTANCIAS EN LAS QUE SE PRODUJO EL FALLECIMIENTO], lo que se produjo bajo una evidente situación de ansiedad y estrés.

Se acompañan, señalados como documento número [Nº], certificado médico de defunción en el que se hace constar la causa de la muerte, la hora del óbito y la edad del fallecido, y como documento número [Nº] testimonio de la sentencia recaída en el procedimiento n.º [Nº DE PROCEDIMIENTO] seguido ante la Sección de lo Social del Tribunal de Instancia de [SEDE], que reconocía como laboral el accidente ocurrido al trabajador.

TERCERO.- Comunicado el siniestro objeto de cobertura a la entidad aseguradora y haciendo llegar a ésta la oportuna reclamación, la misma denegó el pago de la indemnización debida alegando "que el fallecimiento del asegurado no está cubierto en la póliza contratada, ya que la causa del fallecimiento no puede calificarse de accidental a los efectos del art. 100 LCS".

Se acompaña como documento número [Nº] la carta que, bajo la referencia "Asunto", la demandada hizo llegar a mi principal, y en la que, reconociendo tácitamente la condición de asegurado de [NOMBRE Y APELLIDOS DEL ASEGURADO] y la de beneficiario/a de mi principal, le deniega el pago de la cantidad asegurada.

CUARTO.- El Letrado que firma esta demanda dirigió a la demandada la carta que se acompaña señalada como documento número [Nº].

En esa carta se requería a la aseguradora para que procediese a hacer efectiva a mi mandante la correspondiente indemnización y así evitar una reclamación judicial; es la actitud de silencio de la demandada lo que motiva la presente reclamación judicial.

Finalmente, mi representado/a envió un requerimiento fehaciente a la demandada con fecha [FECHA], que fue contestado por la entidad ahora demandada en los siguientes términos: [CONTENIDO DE LA CONTESTACIÓN].

Acompaño como DOCUMENTO NÚM. [Nº] el requerimiento efectuado y como DOCUMENTO NÚM. [Nº] la contestación de la demandada.

A los hechos anteriores son de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN Y COMPETENCIA.

Sobre materia de la competencia genérica del orden civil de la jurisdicción (art. 9.2 LOPJ), tiene la competencia objetiva y funcional (art. 45 LEC, en relación con lo dispuesto en el art. 85.1 LOPJ) la Sección Civil del Tribunal de Instancia de [SEDE] que por turno de reparto corresponda (art. 68 LEC), y la territorial, puesto que el domicilio del demandante se halla en la localidad de [LOCALIDAD] (art. 52.2 LEC y art. 24 LCS).

II.- CAPACIDAD.

Mi mandante es persona física, mayor de edad, en pleno ejercicio de sus derechos civiles, por lo que tiene capacidad para ser parte y capacidad procesal ex arts. 6.1.1.º y 7.1 LEC, como lo es la entidad demandada, [DENOMINACIÓN SOCIAL DE LA ASEGURADORA], persona jurídico-mercantil con capacidad para ser parte que se reconoce en el art. 6.1.3.º LEC, debiendo comparecer en juicio por medio de sus representantes legales (art. 7.4 LEC).

III.- LEGITIMACIÓN.

La legitimación activa corresponde a mi representado/a por su condición de beneficiario/a en la póliza de seguros suscrita por [EL ASEGURADO / LA ASEGURADA] con la mercantil demandada, que ostenta la correlativa legitimación pasiva como entidad aseguradora y parte del contrato de seguro, al amparo de lo dispuesto por el art. 1 LCS y en cuanto deudora por incumplimiento de sus obligaciones contractuales al no haber indemnizado a mi representado/a por el siniestro producido.

IV.- PROCEDIMIENTO.

El juicio ordinario a que se refieren los arts. 248, 249.2 y 399 y ss. LEC, por ser la cuantía reclamada superior a 15.000 euros.

V.- CUANTÍA.

La cuantía de la demanda asciende al importe reclamado, conforme a la regla 1.ª del art. 251 LEC, por lo que no quedan excepcionados los litigantes de representación técnica y defensa letrada con Procurador/a y Abogado/a habilitados ante el tribunal (arts. 23.1 y 31.1 LEC).

VI.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda cumple con el requisito de procedibilidad exigido por la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia, según se ha expuesto en el hecho cuarto y se acredita con los documentos aportados.

VII.- FONDO DEL ASUNTO.

Se ejercita acción de cumplimiento contractual de un seguro de accidentes, seguro contratado por [NOMBRE Y APELLIDOS DEL ASEGURADO] con la compañía demandada, lo que constituye un contrato de seguro mercantil conforme al art. 1 LCS, con los caracteres bien definidos de tratarse de un pacto bilateral, consensual, oneroso y aleatorio (art. 1790 CC), que reúne las condiciones de ser un efectivo convenio de adhesión, entendiéndose por tal aquél en que una de las partes, que suele ser la aseguradora, adopta y mantiene una posición de prevalencia frente a la otra, el asegurado, reflejada en la redacción del pacto, en cuanto que las cláusulas, sobre todo las condiciones generales, no son producto de un previo concierto de voluntades para generarlas y expresarlas en el documento, sino que vienen prefijadas de antemano, aun siempre con carácter genérico y común para todos los seguros de un determinado ramo o tipo. La voluntad del asegurado se manifiesta más bien adhesiva que decisiva plena y deliberadamente. La bilateralidad añora con predominio a la necesaria bilateralidad que como principio general se consagra en los arts. 1254 y 1255 CC. En la póliza suscrita constan los accidentes corporales y, en consonancia con el art. 100 LCS, ampara la muerte causada por lesiones corporales o muerte debida a un accidente que proceda de causa fortuita, espontánea, externa, violenta o independiente, de lo que está excluido el infarto de miocardio, al decir de la aseguradora. Sin embargo, existe un consolidado cuerpo de doctrina jurisprudencial que establece la posibilidad de entender el infarto de miocardio dentro de ese conjunto de accidentes del art. 100 LCS; así podemos citar como primera de estas sentencias la de 7 de abril de 1986, seguida por la de 27 de marzo de 1989, que deja abierta la posibilidad de poder admitirse como eventos causantes de gravísimas y fatales cardiopatías las causas externas e inmediatas procedentes de estrés, siempre que la relación que establece violencia moral, estrés-muerte esté debidamente adverada por la pertinente prueba. Postura que reitera la sentencia de 28 de febrero de 1991, y ello porque, como también recoge la sentencia del Alto Tribunal de 27 de noviembre de 1991, es del acervo cultural común el conocimiento de que los infartos de miocardio pueden ser congénitos o sobrevenidos, por causas externas y adversas, sin un proceso constatado previo, presentándose de forma súbita, inesperada y desagradablemente sorpresiva con efectos mortales ineludibles. Estas causas las originan con mucha frecuencia el estrés emocional o ambiental, el exceso de trabajo, la angustia, preocupaciones, responsabilidades excesivas, estados de ansiedad, así como los cambios en el ritmo de vida que impone la convivencia social y otras similares incrementadoras de la tensión arterial, que, al actuar violentamente, con independencia de causas físicas y patológicas, en relación psíquica-causal se manifiesta en forma de violencia moral-anímica, que origina el proceso desencadenante del infarto. Esta conclusión está adverada por rigurosos estudios científicos, entre ellos los de Jenkis y Rafe, y las estadísticas mortuorias de los países civilizados. Por consiguiente, podemos afirmar que la jurisprudencia, siguiendo los estudios realizados y la experiencia social y común, ha dejado sentado que dentro del concepto de accidente del art. 100 LCS se incluye el infarto de miocardio, siempre y cuando éste no se deba a enfermedad previa constatada o a anomalía congénita igualmente probada, sino que conste en autos que, no concurriendo esas posibilidades, el finado estaba en una situación de estrés emocional o ambiental, exceso de trabajo, subida de tensión arterial, etc., es decir, con causas externas que han producido ese fatal desenlace.

Lo cierto es que el "estrés" es, según la definición que da el Diccionario de la Real Academia Española, una "tensión provocada por situaciones agobiantes que originan reacciones psicosomáticas o trastornos psicológicos a veces graves"; es decir, no se trata de una enfermedad en sí misma, sino de un factor de riesgo que puede provocar una enfermedad o incluso desencadenar un proceso que conduzca a la muerte, por lo que en términos forenses se denomina "infarto sordo".

Y en este sentido, la doctrina jurisprudencial viene declarando, de forma directa o por razonamiento contrario (Sentencias de 5 de marzo de 1992, 23 de octubre de 1997, 20 de junio de 2000, 5 de junio de 2001, 14 de noviembre de 2002 y 11 de noviembre de 2003, Rec. 296/1998, entre otras), que, si bien el infarto de miocardio no está comprendido en los supuestos del art. 100 LCS, salvo estipulación, sin embargo debe comprenderse dentro del seguro de accidentes cuando tenga su génesis en una causa externa; y a tal efecto se ha tomado en consideración la causa inmediata consistente en la presión y el "estrés" consecuencia del aumento de trabajo (Sentencia de 14 de junio de 1994), el esfuerzo físico en el desarrollo del trabajo para el que se hallaba capacitado (Sentencia de 27 de diciembre de 2001, Rec. 2943/1996) y el esfuerzo y tensiones en el desempeño del trabajo (Sentencia de 27 de febrero de 2003, Rec. 2006/1997).

Causa externa y ajena a la voluntad del agente (asegurado) cuya concurrencia se constata en el caso enjuiciado.

Además, no consta por otra parte que el fallecido padeciera ninguna patología o enfermedad cardíaca, ni que se le advirtiese algún factor de riesgo, por lo que ha de concluirse que su fallecimiento fue accidental, y no producto de una dolencia o enfermedad cardíaca o de factores endógenos, de manera que el fallecimiento fue, en todo caso, accidental y encuentra acomodo en la definición que de accidente da el art. 100 LCS: "lesión corporal que deriva de una causa violenta, súbita, externa y ajena a la intencionalidad del asegurado, que produzca invalidez temporal o permanente, o muerte".

Así se desprende bien a las claras del informe médico acompañado como documento número [Nº], realizado de forma casual en el mes de [MES] (siendo el fallecimiento en el mes de [MES] de [AÑO]) con ocasión de un episodio esporádico de cefalea, que dice "que tanto el estudio analítico como los controles tensionales posteriores fueron normales".

Y de lo que no cabe la menor duda es que el asegurador, conocido el siniestro, está obligado a satisfacer la indemnización "al término de las investigaciones y peritaciones necesarias para establecer la existencia del siniestro y, en su caso, el importe de los daños que resulten del mismo", según previene el art. 18 LCS.

VIII.- INTERESES.

Deben reconocerse a mi patrocinado/a los del régimen especial del art. 20 LCS al haber incurrido en mora la entidad aseguradora demandada (reglas 4.ª y 6.ª).

Dichos intereses deberán devengarse desde la fecha del siniestro, sin que resulte objetable la aplicación al caso enjuiciado de lo previsto en la regla 8.ª del art. 20 LCS, pues con anterioridad a la presentación de la demanda la aseguradora demandada ya tuvo acceso a todos los datos y documentos que podían racionalmente conducir a la conclusión de que el fallecimiento del asegurado se produjo por accidente y no por enfermedad y, entre ellos, la sentencia de la Sección de lo Social del Tribunal de Instancia que, aun no vinculante, por tratarse de otra jurisdicción y no haber sido parte en el procedimiento la aquí demandada, sí establecía con claridad, con valor de hecho probado, una conexión causal entre el trabajo que venía desarrollando el asegurado (factor externo) y el fallecimiento, por lo que la aseguradora demandada pudo haber efectuado las comprobaciones oportunas a fin de determinar lo justo de la reclamación que se le hacía, máxime cuando ni siquiera ofreció ni consignó por lo menos una cuantía establecida como seguro principal en caso de fallecimiento por cualquier causa, y no trató por todos los medios de que se aceptara por la actora una cantidad bastante inferior incluso a ésta, cuando sabía perfectamente que no existía ocultación alguna en el estado de salud del asegurado.

IX.- COSTAS.

Conforme al art. 394 LEC, las costas procesales han de imponerse a la parte demandada.

En virtud de lo expuesto,

SUPLICO AL TRIBUNAL

que tenga por presentado este escrito con sus documentos y copias de todo ello, teniéndome por comparecido y parte en la representación que ostento, y ordenando se entiendan conmigo las sucesivas actuaciones, se sirva admitir a trámite la demanda de juicio ordinario que se interpone y, una vez seguido el procedimiento por todos sus trámites, se venga a dictar sentencia que condene a la entidad aseguradora demandada a abonar a la actora la cantidad de [IMPORTE] euros, así como los intereses previstos en el art. 20 LCS devengados desde la fecha del siniestro, con costas procesales.

Es justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Abogado/a: [FIRMA]	Firma del Procurador/a: [FIRMA]
