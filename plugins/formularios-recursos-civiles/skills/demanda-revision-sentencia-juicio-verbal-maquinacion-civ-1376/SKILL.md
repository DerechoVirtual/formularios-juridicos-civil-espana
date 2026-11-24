---
name: demanda-revision-sentencia-juicio-verbal-maquinacion-civ-1376
description: "Demanda de revisión de sentencia de juicio verbal por maquinación fraudulenta. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de revisión de sentencia de juicio verbal por maquinación fraudulenta

> Formulario **CIV-1376** del plugin **Recursos civiles: reposición, apelación, casación y queja** (`formularios-recursos-civiles`) · Civil › Recursos · normativa revisada el 24-11-2026.

## Qué es

Modelo de demanda de juicio de revisión de sentencia dictada en Juicio Verbal por maquinación fraudulenta, de acuerdo con lo establecido en el art. 56.1 LOPJ y 509 LEC.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de revisión de sentencia de juicio verbal por maquinación fraudulenta» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de revisión de sentencia de juicio verbal por maquinación fraudulenta” para mi caso». También puedes invocarla directamente con `/formularios-recursos-civiles:demanda-revision-sentencia-juicio-verbal-maquinacion-civ-1376`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-recursos-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Recursos civiles: reposición, apelación, casación y queja) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (12 veces)
- [ ] NOMBRE Y APELLIDOS (10 veces)
- [ ] LOCALIDAD (9 veces)
- [ ] NÚMERO (5 veces)
- [ ] AÑO (4 veces)
- [ ] IMPORTE (3 veces)
- [ ] SEDE (3 veces)
- [ ] Nº DE PROCEDIMIENTO (2 veces)
- [ ] COLEGIO
- [ ] DATOS DE LA SENTENCIA
- [ ] DÍA
- [ ] FINALIDAD PERSEGUIDA
- [ ] FOLIO
- [ ] LIBRO
- [ ] LUGAR
- [ ] MES
- [ ] NOMBRE DE LA COMUNIDAD
- [ ] NOMBRE DE LA PARTE
- [ ] NOMBRE DEL CAMINO
- [ ] Nº
- [ ] Nº DE DOCUMENTO
- [ ] TOMO

## Normas que cita el formulario

- art. 155.3 LEC
- art. 156.4 LEC
- art. 496 LEC
- art. 56.1 LOPJ
- art. 478 LEC
- art. 511 LEC
- art. 31.1 LEC
- art. 23.1 LEC
- art. 514 LEC
- art. 253.1 LEC
- art. 512 LEC
- art. 513.1 LEC
- art. 510.1.4.º LEC
- art. 1.796.4.º LEC

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

- Junto a «…que conoció la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. «De los de» es residuo de los varios juzgados de una plaza. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).
- Junto a «…rador/a ========================================================================»: requisito de procedibilidad del art. 5 LO 1/2025 — antes de presentar la demanda hay que intentar un medio adecuado de solución de controversias (MASC) y acreditarlo con la demanda (arts. 264.4.º y 399.3 LEC), salvo las materias excluidas del art. 5.2. Fuente: LO 1/2025, arts. 5 a 7 (BOE-A-2025-76).

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

A LA SALA DE LO CIVIL DEL TRIBUNAL SUPREMO

D./Doña [NOMBRE Y APELLIDOS], Procurador de los Tribunales, que actúa en nombre y representación de D./Doña [NOMBRE Y APELLIDOS], mayor de edad, casado, con domicilio en [LOCALIDAD], según se acredita mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], dirigido por la Letrada en ejercicio D./Doña [NOMBRE Y APELLIDOS], colegiada n.º [NÚMERO] del Iltre. Colegio de Abogados de [COLEGIO], y despacho abierto en [LOCALIDAD], ante la SALA comparezco, y como mejor en Derecho proceda, DIGO:

Que por medio del presente escrito, y siguiendo las instrucciones de mi representado vengo a deducir demanda de REVISIÓN de la sentencia de fecha [DÍA] de [MES] de [AÑO], dictada en el Juicio Verbal n.º [Nº DE PROCEDIMIENTO]/[AÑO], por la Sección Civil del Tribunal de Instancia n.ºde los de [SEDE], con base en los siguientes:

HECHOS

PRIMERO

Por la Comunidad de Propietarios [NOMBRE DE LA COMUNIDAD] se formuló demanda de juicio verbal, el [FECHA] contra D./Doña [NOMBRE Y APELLIDOS], titular de la finca del Registro de la Propiedad de dicha localidad, n.º [NÚMERO], al folio [FOLIO], del tomo [TOMO], libro [LIBRO] de [LOCALIDAD], en reclamación de la cantidad de [IMPORTE] euros, correspondientes a diversos conceptos de derrama, intereses legales, y costas.

En la demanda se hacía constar que al demandado era imposible que se le designara domicilio o residencia, y sin perjuicio de que el Tribunal se dirigiera a los registros, organismos y entidades a que se refiere el art. 155.3 LEC, no teniendo domicilio para notificaciones designado a la Comunidad, se solicitaba comunicación en el piso, o la edictal conforme a los arts. 156.4 y 164 LEC.

Se aporta certificación registral de la finca referida como documento n.º 1, y testimonio de la demanda como documento n.º 2.

SEGUNDO

Registrado el procedimiento con el n.º [NÚMERO]/[AÑO] por el Juez de Primera Instancia n.º [NÚMERO] de [LOCALIDAD], en diligencia de ordenación de [FECHA], se acordó requerir a la demandante de subsanación, por término de cuatro días, a fin de que aportara el último domicilio del demandado, que constara en archivos o registros públicos, a lo que dicha parte actora, cumpliendo el requerimiento, manifiestó que el único dato domiciliario, que constaba en la inscripción registral, se correspondía con una dirección totalmente ignorada en la actualidad, y faltaba cualquier otro.

Se acompaña testimonio de la citada diligencia como documento n.º 3, y de las respuesta pretendidamente subsanatoria como documento n.º 4.

TERCERO

Admitida la demanda por decreto/auto de [FECHA], se mandó obtener certificación del padrón municipal de [LOCALIDAD], y remitida respuesta negativa a la averiguación domiciliaria, en diligencia de ordenación de [FECHA], se mandó citar para el acto de la vista al entonces demandado, mi patrocinado, fijando la copia del dicho decreto/auto en el tablón de anuncios de la Oficina Judicial, y llegado el día de la vista, e incomparecido D./Doña [NOMBRE Y APELLIDOS], se le declaró en rebeldía, conforme al art. 496 LEC.

Se adjuntan, como documentos nos. 5, 6, 7, y 8, particulares testimoniados del dicho decreto/auto, respuesta oficial, diligencia, y acta de la vista.

CUARTO

Sin que, por cierto, figure constancia alguna como es obligado, de la exposición y permanencia en el tablón referido de la citación a la vista, el [FECHA], el Tribunal dictó sentencia condenatoria, solicitando la actora el [FECHA], la notificación por edictos en el BOP, a lo que se accedió en proveído de

Se acompañan copias testimoniadas de la sentencia y solicitud de notificación edictal como documentos nos. 9 y 10.

QUINTO

Por diligencia de [FECHA], sin previa diligencia de exposición y fechas, por el Letrado de la Administración de Justicia se certifica haber transcurrido el plazo para poder interponer el recurso de apelación, y en decreto de la misma fecha se declara firme la sentencia, y se previene a las partes lo que a su derecho convenga.

Es documento n.º 11 la copia del folio de actuaciones con la diligencia y decreto mentados.

SEXTO

Por escrito de la entonces parte actora de [NOMBRE DE LA PARTE], con base en sentencia, se interesa su ejecución, y se pide embargo, expresándose, por medio de otrosí, que ‘a través del Registro de la Propiedad n.º [NÚMERO] de [LOCALIDAD], donde hay bienes a su nombre, he podido averiguar un nuevo domicilio en [LOCALIDAD], Camino Viejo de [NOMBRE DEL CAMINO] ‘, ante lo que se despacha ejecución de título judicial en auto de [FECHA], ordenándose que se hiciera la notificación al demandado, mi patrocinado, a través del Servicio Común de Actos de Comunicación y Ejecución (SCACE) de [LOCALIDAD], en el domicilio indicado.

Se acompañan el escrito de parte y auto del Tribunal, como documentos nos. 12 y 13.

SÉPTIMO

El [FECHA], se notificaron despacho de ejecución y embargo, lo cual se entendió con la esposa de D./Doña [NOMBRE Y APELLIDOS], el ahora demandante, que el día [FECHA] siguiente compareció en las actuaciones suscitando la nulidad de actuaciones del proceso desde la admisión a trámite de la demanda, que fue inadmitido en providencia de

Se aportan testimonios de la diligencia de notificación y embargo, de la solicitud de parte, y de la citada providencia, que son documentos nos. 14, 15 y 16.

OCTAVO

El domicilio en que se practicó el acto ejecutivo es el mismo que figura en la inscripción registral de la finca que pertenece a la Comunidad de propietarios demandada, del que se ha aportado certificación como documento n.º 1, si bien con el cambio de nombre de la calle y de numeración habidos por el transcurso del tiempo, lo cual conocía quien demandaba, y que en la otra finca -del domicilio actual- de posterior inscripción, y en otro de los Registros de la capital, viene actualizado, lo cual sólo se ha preferido sacar a la luz con la demanda ejecutiva, después de la sentencia firme en rebeldía.

Se acompaña certificación de la Comisión Permanente del Ayuntamiento de [LOCALIDAD], conforme a la que se establece la identidad entre la dirección antigua y la actual, canjeada por su Acuerdo de fecha [FECHA] (documento n.º 17).

NOVENO

El domicilio en cuestión fue comunicado a la Comunidad de propietarios, a efectos de todas las notificaciones, mediante carta certificada con acuse recibo, dirigida al Administrador D./Doña [NOMBRE Y APELLIDOS], de manera que la manifestación de no haberse hecho dicha designación no es cierta.

Se aporta la carta con el acuse devuelto por el Servicio de Correos, como documento n.º 18.

FUNDAMENTOS DE DERECHO

I.- COMPETENCIA

Corresponde el conocimiento de la presente demanda que pretende la revisión de una sentencia firme, a la Sala de lo Civil del Tribunal Supremo, de acuerdo con lo establecido en el art. 56.1 LOPJ y 509 LEC.

La jurisprudencia del TS ha sentado la doctrina de que para determinar la competencia del Tribunal, respecto de una Sala de lo Civil y Penal de Tribunal Superior de Justicia, ha de estarse a la materia sobre que versó el proceso, con relación al art. 478 LEC; y como en el caso el objeto del Juicio Verbal fue una reclamación de cantidad con base en Derecho común, y sin ninguna incidencia del Derecho foral o especial de la Comunidad Autónoma, la competencia funcional para conocer de la demanda de revisión civil es de la Sala I TS (SSTS de 15 de diciembre de 1994, rec. 505/1993, 17 de abril de 1996, rec. 3565/1994, entre otras).

II.- CAPACIDAD

El demandante D./Doña [NOMBRE Y APELLIDOS] goza de la plena capacidad, tanto para ser parte como capacidad procesal, que se deriva de su mayorÌa de edad y de estar en el pleno ejercicio de sus derechos civiles, como persona física, ex arts. 6.1.1.º y 7.1 LEC.

III.- LEGITIMACIÓN

Mi mandante está activamente legitimado para el ejercicio de la presente acción, de acuerdo al art. 511 LEC al ser la parte perjudicada por la sentencia firme dictada y concurrir, por tanto, el gravamen que exige la Ley, ya que D./Doña [NOMBRE Y APELLIDOS] fue condenado en la sentencia firme que se desea rescindir, al pago de la cantidad de [IMPORTE], que junto con intereses y costas son el crédito por el que se ha trabado embargo de su patrimonio.

IV.- POSTULACIÓN

Es preceptiva en el presente proceso la intervención de asistencia letrada habilitada ante el Tribunal, conforme al art. 31.1 LEC, y de representante técnico igualmente habilitado en la Villa de Madrid —art. 23.1 LEC—, acompañándose a este escrito la escritura de apoderamiento, y redactando y firmando esta demanda el abogado que se identifica.

V.- PROCEDIMIENTO

El presente juicio de revisión debe sustanciarse por las normas del art. 514 LEC, que diseña un procedimiento especial en que, admitida la demanda, se solicitará por el Letrado de la Administración de Justicia la remisión de todas las actuaciones del pleito cuya sentencia se impugna, y emplazará de contestación por veinte días a las partes de aquél. o sus causahabientes, y expirado el plazo, con o sin contestación, se seguirá el trámite del juicio verbal, en que emitirá informe el Ministerio Fiscal.

VI.- CUANTÍA

Si se sostiene que la pretensión mero-procesal de rescisión de la sentencia firme es la que fija la cuantía de la demanda, tal se reputa inestimable, y si se sostiene que la cuantía, relativamente determinada, obedece al interés litigioso del proceso cuya sentencia se impugna, será la misma que se determinó entonces de [IMPORTE] euros, con lo que se cumple con la exigencia del art. 253.1 LEC.

VII.- PRESUPUESTOS DE ADMISIÓN

Se presenta la demanda dentro del plazo de interposición del art. 512 LEC, puesto que ni han transcurrido los cinco años que establece la Ley como límite para la solicitud de revisión desde la fecha de publicación de la sentencia que se pretende impugnar, ni resulta de aplicación el plazo de caducidad de los tres meses que, la Ley señala para el ejercicio de la acción revisoria por falsedad de documento fundamental.

Se acredita mediante abonaré bancario en la cuenta de consignaciones de la Sala del depósito de 300 euros que la Ley exige en su art. 513.1 LEC.

VIII.- CAUSA DE REVISIÓN

Concurre la causa de revisión del art. 510.1.4.º LEC puesto que se ganó contra mi representado el juicio verbal [Nº DE PROCEDIMIENTO] / [AÑO], de que conoció la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº] [DATOS DE LA SENTENCIA] en virtud de maquinación frudulenta.

La revisión contra sentencias dictadas por el orden jurisdiccional civil, si bien puede encontrar remotos antecedentes en instituciones tan antiguas como la "restitutio in integrum" del Derecho Romano y en la vieja legislación de Las Partidas, ni fue objeto de regulación en la primera Ley de Enjuiciamiento Civil de 1855, ni tampoco se recogió en la Ley orgánica provisional de 18 de junio de 1870. Su regulación en el Título XXII del Libro II de la LECiv 1881 apoyaba su naturaleza ajena al genuino recurso, pese a intitularse como "recurso de revisión" y figurar a continuación del recurso de casación como de carácter extraordinario, y ello porque procede precisamente contra sentencias que han ganado firmeza, contra las que, por definición legal, no cabe recurso alguno, ni ordinario, ni extraordinario, bien por su mero dictado, o por haber sido consentida por las partes. Ello ha motivado que la doctrina procesal lo haya motejado de remedio extraordinario y rescisorio, o como una acción autónoma que da lugar a un proceso especial. Así, el nuevo régimen de los arts. 509 y ss. LEC elude el vocablo ‘recurso’ para este proceso.

En cualquier caso, al margen del ‘nomen iuris’, la jurisprudencia califica el proceso de revisión como una vía para la impugnación de una sentencia que ha ganado firmeza, que procede tan sólo por concretas y específicas causas, tasadas legalmente dentro de un "numerus clausus",y que no implica en modo alguno una nueva instancia y, que por su carácter excepcional no puede ser objeto de una interpretación extensiva, pues ello afectaría a la inseguridad de las situaciones reconocidas y de los derechos declarados en resoluciones firmes, lo que implicaría el gravísimo quebranto del principio de autoridad de cosa juzgada, y de la seguridad jurídica y de la misma certeza del Derecho.

Dentro de la aplicación ‘ad restringenda’, según la copiosa jurisprudencia al respecto de la causa revisoria de la cosa juzgada invocada, de términos casi idénticos al viejo art. 1.796.4.º LECiv 1881, cualquier maniobra encaminada a dificultar e impedir llegue a conocimiento del demandado el planteamiento del juicio, encaja dentro del concepto de maquinación fraudulenta, con quebranto del derecho de defensa que asiste a todo justiciable, ya que se llega al fallo por medio de argucia, artificio o ardid encaminado a impedir que el demandado tenga oportunidad de defenderse.

Lo que exige la doctrina legal es un nexo causal adverado entre hechos que por sí mismos evidencian un proceder malicioso y la resolución judicial combatida [SSTS de 8 de junio de 1992 y STS 20 de octubre de 1998, rec. 2775/1997].

Y en el supuesto de autos ha existido una ocultación maliciosa del domicilio de mi mandante D. [NOMBRE Y APELLIDOS], que no sólo constaba en la inscripción de la finca perteneciente a la Comunidad de propietarios demandante —si bien con un cambio posterior de denominación de la calle y denominación—, sino que había sido facilitado por el comunero al Administrador de la Comunidad.

La parte actora en el juicio donde recae la sentencia impugnada, manifestó al Tribunal ignorar el domicilio del demandado, y aun más, indicó que la única referencia domiciliaria era la de la inscripción registral que no se correspondía con una localización conocida en la actualidad. Sin embargo, una vez lograda por esa falacia la citación edictal, la rebeldía, y la sentencia sin oposición, la parte actora, trocada en ejecutante, ya sí manifiesta haber obtenido un domicilio, desde otra finca registrada, en otro de los Registros de la Propiedad de

El órgano judicial esmera su tutela al exigir ‘in limine’ una investigación del paradero, que en todo caso se disfraza por la parte actora, consiguiéndose el resultado apetecido por ésta, a pesar de la diligencia, que no podía saber del cambio de nombres del callejero, ni que tal parte debía tener conocimiento del domicilio para notificaciones de la propiedad horizontal.

Hay, pues, argucia o engaño por el litigante vencedor, con consciente y voluntario aprovechamiento para [FINALIDAD PERSEGUIDA], soslayando el domicilio del demandado y la comunicación por remisión de la citación a la vista, procurar un obstáculo a la defensa, garantizándose torcidamente el éxito en sentencia. La inconcurrencia a la vista es causa eficiente del fallo de la sentencia cuya revisión se pide, como de su lectura resalta, y tal inconcurrencia procede de la ignorancia provocada en el demandado de la convocatoria de dicha vista, derivada de una grave irregularidad procesal. La indefensión en estos casos resulta notoria, ya que se impide contestar y se asegura que la sentencia resulte estimatoria [SSTS de 5 de julio de 1994 y 15 de abril de 1996, rec. 3107/1992].

Si la Presidencia de la Comunidad alegara el desconocimiento de lo que se hizo saber al Administrador, es algo que no excusa la imputación.

En virtud de lo expuesto,

SUPLICO A LA SALA que, teniendo por presentado este escrito, con sus copias y documentos acompañados, y por interpuesta demanda de revisión, se digne admitirla, y seguido que sea su regular trámite, dicte sentencia por la que se estime procedente la revisión pedida de la sentencia dedede, rescindiéndola, con devolución de los autos a la Sección Civil del Tribunal de Instancia n.ºde los de [SEDE], de donde proceden, a fin de que las partes usen de su derecho según les convenga.

Por ser de Justicia que pido en [LUGAR], a [FECHA].

Firma de Abogado/a	Firma de Procurador/a

========================================================================
