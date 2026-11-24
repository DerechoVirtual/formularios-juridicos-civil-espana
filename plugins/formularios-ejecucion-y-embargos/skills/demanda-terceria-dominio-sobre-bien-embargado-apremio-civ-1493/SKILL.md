---
name: demanda-terceria-dominio-sobre-bien-embargado-apremio-civ-1493
description: "Demanda de tercería de dominio sobre bien embargado en apremio de la Agencia Tributaria. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de tercería de dominio sobre bien embargado en apremio de la Agencia Tributaria

> Formulario **CIV-1493** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Demanda de tercería de dominio sobre bien embargado en expediente administrativo de apremio por la Agencia Tributaria, y que tras los trámites procesales oportunos, se dicte auto que se pronuncie sobre la pertenencia a la parte actora del bien objeto de esta demanda, acordándose el alzamiento del embargo, así como de las medidas de garantía que pudieran haberse adoptado.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de tercería de dominio sobre bien embargado en apremio de la Agencia Tributaria» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de tercería de dominio sobre bien embargado en apremio de la Agencia Tributaria” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:demanda-terceria-dominio-sobre-bien-embargado-apremio-civ-1493`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] NÚMERO (5 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] FECHA (2 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] SEDE (2 veces)
- [ ] CALLE
- [ ] COLEGIO
- [ ] DNI/NIE
- [ ] DOMICILIO A EFECTOS DE NOTIFICACIONES
- [ ] LUGAR
- [ ] Nº
- [ ] Nº DE PROCEDIMIENTO
- [ ] PARTE DEMANDADA

## Normas que cita el formulario

- art. 52.1.15.º LEC
- art. 599 LEC
- art. 6.1.3.º LEC
- art. 7.4 LEC
- art. 595.1 LEC
- art. 600 LEC
- art. 595.3 LEC
- art. 120.1 Ley 30/1992
- art. 117.1 Real Decreto 939/2005
- art. 3.2 LO 1/2025
- art. 601 LEC

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

### Avisos de actualización (3) — se aplican en el texto, nunca se copian en el documento

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «… procedimiento tramitado ante el Tribunal de Instancia de [SEDE], plaza n.º [Nº]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).
- Junto a «…rídico de las Administraciones Públicas y del Procedimiento Administrativo Común»: La Ley 30/1992 está derogada; hoy rigen la Ley 39/2015 (procedimiento administrativo común) y la Ley 40/2015 (régimen jurídico del sector público). La Ley 39/2015 suprimió la reclamación previa a la vía judicial civil.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Notas al pie del formulario original:
(1) La Ley 39/2015, de 1 de octubre, del Procedimiento Administrativo Común de las Administraciones Públicas, aplicable a procesos iniciados después de su entrada en vigor, el 2 de octubre de 2016, suprime la reclamación administrativa previa a la vía judicial civil como requisito para al ejercicio de acciones fundadas en derecho privado contra una Administración Pública.

La exposición de motivos de la Ley 39/2015 dice que "de acuerdo con la voluntad de suprimir trámites que, lejos de constituir una ventaja para los administrados, suponían una carga que dificultaba el ejercicio de sus derechos, la ley no contempla ya las reclamaciones previas en vía civil y laboral, debido a la escasa utilidad práctica que han demostrado hasta la fecha y que, de este modo, quedan suprimidas".

========================================================================


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

D./Dña. [NOMBRE Y APELLIDOS], Procurador de los Tribunales, que actúa en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS], con DNI n.º [DNI/NIE], y domicilio en [LOCALIDAD], según se acredita con la copia del poder para pleitos que acepto, y oportunamente acompaño con ruego de devolución de la original previo testimonio bastante en autos, por necesitarse para otros usos, dirigido por la Letrada en ejercicio D./Dña. [NOMBRE Y APELLIDOS], colegiada n.º [NÚMERO] del Iltre. Colegio de Abogados de [COLEGIO], y despacho abierto en [LOCALIDAD], ante el Tribunal comparezco y como mejor en Derecho proceda, DIGO:

Que siguiendo instrucciones de mi mandante, por el presente escrito formulo demanda de tercería de dominio frente a la Agencia Estatal de la Administración Tributaria (AEAT), con domicilio a efectos de notificaciones en [DOMICILIO A EFECTOS DE NOTIFICACIONES], fundándola en los siguientes:

HECHOS

PRIMERO.- En expediente tramitado por la Unidad de Recaudación de la Administración de la AEAT de [LOCALIDAD], con el número [NÚMERO], se embargó, entre otros y como erróneamente perteneciente al ejecutado D./Dña. [NOMBRE Y APELLIDOS], el siguiente bien: plaza de aparcamiento n.º [NÚMERO] del inmueble de la calle [CALLE], n.º [NÚMERO] de

SEGUNDO.- La titularidad de dicha plaza de aparcamiento aparecía inscrita en el Registro de la Propiedad número [NÚMERO] de [LOCALIDAD], en fecha anterior al embargo, como de la propiedad del ejecutado D./Dña. [NOMBRE Y APELLIDOS], existiendo sobre dicho bien anotación preventiva de embargo, acordada en el procedimiento tramitado ante el Tribunal de Instancia de [SEDE], plaza n.º [Nº] con el número

Se acompaña como documento número [Nº DE DOCUMENTO] nota simple informativa expedida por el referido Registro.

TERCERO.- Con anterioridad a la fecha en que se dictó diligencia acordando el embargo de la referida plaza de aparcamiento en el citado expediente administrativo, la misma fue adquirida por mi mandante en la subasta judicial celebrada en el referido procedimiento, como acredito con el testimonio de la resolución que acompaño como documento número

Consecuentemente, al tiempo del embargo administrativo del bien, el propietario del mismo era mi mandante y no el Sr./a. [NOMBRE Y APELLIDOS], si bien es cierto que dicha transmisión no constaba inscrita en el Registro de la Propiedad, puesto que se presentó a inscripción en fecha posterior.

CUARTO.- Con carácter previo a la vía jurisdiccional se instó tercería en vía administrativa que fue desestimada por resolución de fecha [FECHA], como se acredita mediante documentos números

A los anteriores hechos son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

I.- COMPETENCIA.

Corresponde el conocimiento de la presente demanda al Tribunal al que me honro en dirigirme, conforme a lo establecido en el art. 52.1.15.º LEC, que fija la competencia territorial para tercerías de dominio, cuando el órgano embargante no es judicial sino administrativo, para el Tribunal del domicilio de éste, en relación con el art. 15 de la Ley de Asistencia Jurídica al Estado e Instituciones Públicas (L 52/1997 de 27 de noviembre), por ser el de la capital de la provincia donde tiene su domicilio el órgano administrativo que acordó el embargo.

II.- PROCEDIMIENTO.

El presente proceso habrá de sustanciarse por los trámites del juicio verbal, de acuerdo con lo que establece el art. 599 LEC.

III.- CAPACIDAD.

El demandante es persona física mayor de edad, con pleno ejercicio de derechos civiles (arts. 6.1.1.º y 7.1 LEC).

El demandado, organismo público perteneciente al sector estatal, es persona jurídico pública institucional con capacidad para ser parte (art. 6.1.3.º LEC), y capacidad procesal (art. 7.4 LEC).

IV.- LEGITIMACIÓN ACTIVA.

Podrá interponer tercería de dominio, en forma de demanda, quien, sin ser parte en la ejecución, afirme ser dueño de un bien embargado como perteneciente al ejecutado y que no ha adquirido de éste una vez trabado el embargo (art. 595.1 LEC). Mi representado está legitimado activamente por ser el legítimo propietario del bien embargado y no ser parte en el procedimiento de ejecución del que dimana la traba.

V.- LEGITIMACION PASIVA.

La demanda de tercería se interpone frente al acreedor ejecutante, organismo que acordó el embargo del bien mencionado, debiéndose notificar en todo caso la admisión a trámite de la demanda al ejecutado D./Dña. [NOMBRE Y APELLIDOS] a los efectos de lo establecido en el art. 600 LEC.

VI.- POSTULACIÓN.

En cuanto a la postulación es preceptiva en el presente proceso la intervención de Abogado habilitado para ejercer su profesión en el tribunal que conozca del asunto, y Procurador igualmente habilitado para actuar en el tribunal que conozca del juicio (arts. 23.1 y 31.1 LEC), acompañándose a este escrito la escritura de apoderamiento para pleitos y la identificación de los dichos profesionales.

La representación y defensa de la AEAT se atribuye por ministerio de la Ley (art. 1 L 52/1997 y 551.1 LOPJ) a los Abogados del Estado integrados en el Servicio Jurídico del Estado.

VII.- PROCEDIBILIDAD.

El art. 595.3 LEC exige que con la demanda de tercería de dominio se aporte un principio de prueba por escrito del fundamento de la pretensión del tercerista, como así se hace con el testimonio del decreto de adjudicación en subasta judicial que se acompaña como documento número

Se ha dado cumplimiento también a la exigencia relativa a la reclamación previa de tercería en vía administrativa que permite el ejercicio de la acción de tercería ante los tribunales de justicia (art. 120.1 Ley 30/1992, de 26 de noviembre, de Régimen Jurídico de las Administraciones Públicas y del Procedimiento Administrativo Común ; y art. 117.1 del Real Decreto 939/2005, de 29 de julio, por el que se aprueba el Reglamento General de Recaudación), como se acredita con los documentos números [Nº DE DOCUMENTO]

Por otro lado, conforme a lo dispuesto en el art. 3.2 LO 1/2025, la presente demanda no está sujeta al requisito de MASC, en cuanto se dirige contra una entidad pública como lo es en este caso la AEAT.

VIII.- ASPECTOS SUSTANTIVOS.

La tercería de dominio se ciñe a la pretensión del tercerista de que se alce el embargo del bien objeto de tercería, sin que pueda el ejecutante, y en su caso el ejecutado, pretender más que el mantenimiento del embargo o sujeción a la ejecución del bien objeto de tercería (art. 601 LEC).

El tribunal se pronunciará sobre la pertenencia del bien y la procedencia de su embargo a los únicos efectos de la ejecución en curso, sin que produzca efectos de cosa juzgada en relación con la titularidad del bien (art. 603, párrafo 1.º LEC).

Tal es doctrina ya consolidada [SSTS de 8 de febrero y 10 de junio de 1991, 24 de julio de 1992 y 2 de junio de 1994].

La pretensión ha de ser fundada en la titularidad del derecho de propiedad, u otro que, por disposición legal expresa, autorice a oponerse al embargo, o a la realización forzosa de un bien, como de pertenencia al ejecutado.

Se precisa la concurrencia de los elementos que la jurisprudencia ha venido exigiendo para la viabilidad de tal acción (SSTS de 22 de junio de 1995, rec. 721/1992, 19 de mayo de 1997, rec. 1439/1993, entre otras), y que se contraen en los extremos siguientes:

— que se demuestre que el título esgrimido es legítimo, es decir, que resulta suficiente para adquirir el dominio,
— que se identifique la cosa sobre que se pretende levantar el embargo, y
— que se acredite la condición de tercero del demandante.

En el supuesto de esta demanda, se alega y prueba la propiedad del inmueble embargado por mi mandante, a través de negocio jurídico de adjudicación en virtud de subasta judicial.

Por consiguiente, está acreditada la propiedad del bien embargado en el procedimiento administrativo en la fecha en que el embargo se acordó, la identidad con el trabado, y que el embargo se ha llevado a cabo para cubrir deudas de quien no era dueño cuando se produce la traba, por lo que siendo el tercerista persona que nada tiene que ver con la obligación contraída entre el ejecutado y la agencia tributaria y ajena por completo a la ejecución, debe alzarse el embargo trabado sobre el mismo.

IX.- COSTAS PROCESALES.

Las costas de este proceso deberán ser impuestas a la parte demandada, de conformidad con lo establecido en el art. 603, párrafo 2.º, en relación con los arts. 394 y ss. LEC.

En virtud de todo lo anterior,

SUPLICO AL TRIBUNAL:

que teniendo por presentado este escrito con los documentos que en él se mencionan, se me tenga por comparecido y parte en nombre de mi representado, entendiéndose conmigo las sucesivas actuaciones, y por formulada demanda de tercería de dominio frente a [PARTE DEMANDADA], ejecutante en el procedimiento administrativo de apremio [Nº DE PROCEDIMIENTO], que se tramitará en pieza separada por los cauces del juicio verbal; todo ello para que, tras los trámites procesales oportunos, se dicte auto que se pronuncie sobre la pertenencia a mi representado del bien objeto de esta demanda y se acuerde el alzamiento del embargo, así como de las medidas de garantía que pudieran haberse adoptado, con expresa imposición de las costas a la parte demandada si se opusiere a esta pretensión.

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a
