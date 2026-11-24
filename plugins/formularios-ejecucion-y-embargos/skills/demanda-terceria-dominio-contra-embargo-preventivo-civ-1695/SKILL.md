---
name: demanda-terceria-dominio-contra-embargo-preventivo-civ-1695
description: "Demanda de tercería de dominio contra embargo preventivo de finca recibida en dación sin escritura. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de tercería de dominio contra embargo preventivo de finca recibida en dación sin escritura

> Formulario **CIV-1695** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Demanda de tercería de dominio respecto a la medida cautelar de embargo preventivo de finca adquirida en dación de pago y cuya transmisión no fue elevada a pública, y tras los trámites oportunos, dicte auto por el que se declare la pertenencia de la finca embargada a quien interpone este escrito.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de tercería de dominio contra embargo preventivo de finca recibida en dación sin escritura» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de tercería de dominio contra embargo preventivo de finca recibida en dación sin escritura” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:demanda-terceria-dominio-contra-embargo-preventivo-civ-1695`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (10 veces)
- [ ] DENOMINACIÓN SOCIAL (9 veces)
- [ ] FECHA (6 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] Nº DE DOCUMENTO (5 veces)
- [ ] NÚMERO (5 veces)
- [ ] AÑO (4 veces)
- [ ] Nº (4 veces)
- [ ] IMPORTE (3 veces)
- [ ] Nº DE PROCEDIMIENTO (2 veces)
- [ ] PARTE DEMANDADA (2 veces)
- [ ] SEDE (2 veces)
- [ ] CALLE
- [ ] COLEGIO
- [ ] DNI/NIE
- [ ] FOLIO
- [ ] LUGAR
- [ ] MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] Nº DE COLEGIADO/A
- [ ] Nº DE MODELO
- [ ] PISO
- [ ] TOMO

## Normas que cita el formulario

- art. 596.1 LEC
- art. 85.1 LOPJ
- art. 721.1 LEC
- art. 595 LEC
- art. 600 LEC
- art. 599 LEC
- art. 253.1 LEC
- art. 251 LEC
- art. 595.3 LEC
- art. 597 LEC
- art. 596 LEC
- art. 437.1 LEC
- art. 5 Ley Orgánica 1/2025
- art. 601 LEC
- art. 1.175 CC
- art. 429.8 LEC
- art. 1.923.4 CC
- art. 604 LEC

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
- Junto a «… [Nº DE PROCEDIMIENTO]/[AÑO] del Tribunal de Instancia de [SEDE], plaza n.º [Nº]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, que actúa en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS], con DNI nº [DNI/NIE], y domicilio en [LOCALIDAD], como acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], dirigido por el Letrado/a en ejercicio D./Dña. [NOMBRE Y APELLIDOS], colegiada nº [Nº DE COLEGIADO/A] del Iltre. Colegio de Abogados de [COLEGIO], y despacho abierto en [LOCALIDAD], ante el Tribunal comparezco en autos de Juicio Ordinario nº [Nº DE PROCEDIMIENTO]/[AÑO], y como mejor en Derecho proceda, DIGO:

Que siguiendo instrucciones de mi mandante, por el presente escrito formulo demanda de tercería de dominio respecto a la medida cautelar de embargo preventivo de finca acordada en los presentes autos, frente a [PARTE DEMANDADA], S.A., parte actora en este proceso, que postula representada por el Procurador de los Tribunales D./Dña. [NOMBRE Y APELLIDOS], en el que es parte demandada [DENOMINACIÓN SOCIAL], S.L., fundándola en los siguientes

HECHOS

PRIMERO.- Con fecha [FECHA], mi representado adquirió en documento privado el local sito en el piso [PISO] del nº [NÚMERO] de la calle [CALLE] de [LOCALIDAD], en pago de deuda de [IMPORTE] euros, que mantenía la mercantil [DENOMINACIÓN SOCIAL], S.L., demandada en el presente juicio, por precio de servicios prestados.

El inmueble figura inscrito en el Registro de la Propiedad de esta ciudad, como finca nº [NÚMERO], al folio [FOLIO], tomo [TOMO], a nombre de [DENOMINACIÓN SOCIAL], S.L.

En prueba de la primera afirmación se acompaña, señalado como doc. nº [Nº], original del contrato, que se denominaba de compraventa, otorgado entre nuestro representado y el que afirmaba ser gerente de [DENOMINACIÓN SOCIAL], S.L., con poderes de representación, D./Dña. [NOMBRE Y APELLIDOS].

SEGUNDO.- Habiendo quedado mi mandante para suscribir la escritura pública de transmisión el [FECHA], en la Notaría de D./Dña. [NOMBRE Y APELLIDOS], en [LOCALIDAD], acudió aquél y D./Dña. [NOMBRE Y APELLIDOS], pero fue incapaz de acreditar documentalmente su poder de representación de [NOMBRE DEL REPRESENTADO/A], S.L., por lo cual se levantó acta notarial de constancia y manifestaciones, entre las que dicho apoderado de la sociedad vendedora adveraba el contrato privado y concertaba la dación en pago, comprometiéndose a ratificarla por sí o con el representante legal de la mercantil.

A la demostración del hecho se acompaña copia auténtica del acta de [FECHA], nº [NÚMERO] del protocolo general corriente del dicho Notario, como doc. nº [Nº], que lleva copia signada del indicado contrato privado.

TERCERO.- Desde esa fecha, hace más de cinco años, mi representado viene usando el inmueble como su oficina, como acredita el hecho de que los recibos del impuesto de actividades económicas, y de suministro de luz, agua, gas, contribuciones urbanas e impuesto de basuras estén a su nombre en la dicha dirección.

Se acredita la anterior manifestación con los docs. nºa, consistentes en recibos de impuesto y suministros.

CUARTO.- Pese a que mi mandante adquirió el inmueble a cambio de un crédito cierto, lo cierto es que a fecha de hoy dicha transmisión no consta inscrita en el Registro de la Propiedad, pero sí se presentó autoliquidación del Impuesto de Transmisiones Patrimoniales y Actos Jurídicos Documentados, como acredita el modelo normalizado [Nº DE MODELO], que sigue a diligencia de compulsas del contrato privado y acta notarial ya referenciados, y que se acompaña como doc. nº [Nº], y se produjo el cambio en el catastro de urbana de la parcela a nombre de D./Dña. [NOMBRE Y APELLIDOS], como se demuestra con el recibo de impuesto de bienes inmuebles del último ejercicio, que se aporta como doc. nº [Nº DE DOCUMENTO].

QUINTO.- En repetidas ocasiones, mi representado ha exigido a [DENOMINACIÓN SOCIAL], S.L., la ratificación pública de la transmisión, sin que se haya negado el acto, pero tampoco procediendo a lo que se exigía. De suyo, desaparecida la mercantil de su domicilio el año [AÑO], se dirigió mi mandante al domicilio del administrador social que constaba en el Registro mercantil, con idéntico nulo resultado.

Se adjuntan, como docs. nos.a, tres cartas de las enviadas, sin contestación.

SEXTO.- Finalmente, mi representado se ha visto forzado a deducir demanda de juicio ordinario contra [PARTE DEMANDADA], S.L., a fin de que sea condenada a otorgar en documento público el negocio que ratifique la dación de pago de hace más de cinco años, o supla su voluntad el Tribunal, que ha dado lugar a autos nº [Nº DE PROCEDIMIENTO]/[AÑO] del Tribunal de Instancia de [SEDE], plaza n.º [Nº] .

Se aporta anexo testimonio de la demanda, auto de admisión, y providencia de citación a la audiencia previa con declaración de rebeldía de la demandada, como doc. nº [Nº DE DOCUMENTO].

SÉPTIMO.- Mi mandante solicitó medida cautelar de anotación preventiva de la demanda en el citado juicio ordinario nº [NÚMERO]/[AÑO] del Tribunal de [LOCALIDAD], que le fue concedida en auto de [FECHA] (se compaña testimonio como doc. nº [Nº DE DOCUMENTO]), y al proceder a cumplimentar el mandamiento, ha advertido que la finca se halla trabada con embargo preventivo a favor de la mercantil [DENOMINACIÓN SOCIAL], S.A., lo que provoca la interposición de la presente demanda.

OCTAVO.- Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento nº [Nº DE DOCUMENTO]

A los anteriores hechos son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

I.- COMPETENCIA.

Corresponde el conocimiento de la presente demanda al Tribunal, conforme a lo dispuesto en los arts. 596.1 y 599 LEC en relación con lo dispuesto en el art. 85.1º LOPJ, ya que la tercería de dominio ha de interponerse ante el tribunal que conozca del proceso del que sea instrumental el proceso cautelar, dado que en el embargo preventivo todavía no hay proceso ejecutivo, sino cautelar, con lo cual se resuelve en una regla la competencia genérica, y específica objetiva, funcional y territorial.

II.- CAPACIDAD.

El demandante es persona física mayor de edad, con pleno ejercicio de derechos civiles (arts. 6.1.1º y 7.1).

La demandada es sociedad mercantil, que goza de personalidad independiente y plena capacidad, tanto para ser parte como capacidad procesal, que se derivará de su regular constitución en escritura pública inscrita en el Registro Mercantil, y deberá comparecer por medio de sus legal representante, con arreglo a los arts. 6.1.3º y 7.4, siendo parte de proceso cautelar, como del principal ex art. 721.1 LEC.

III.- LEGITIMACIÓN.

Puede interponer tercería de dominio, desde que se haya efectuado el embargo de un bien, incluso preventivo (art. 596.1 LEC), en forma de demanda, quien, sin ser parte, afirma ser dueño de un bien embargado como perteneciente al demandado y que no ha adquirido de éste una vez trabado el embargo (art. 595 LEC), por lo que mi mandante está legitimado activamente por ser el propietario del bien embargado y ser tercero en el proceso del que dimana la traba.

La demanda de tercería se interpone frente al acreedor demandante, sin hacerlo frente al demandado, aparente propietario del bien embargado, puesto que el bien al que se refiere no ha sido por éste designado (art. 600 LEC), toda vez que es rebelde en este juicio ordinario.

IV.- POSTULACIÓN.

En cuanto a la postulación es preceptiva en el presente proceso la intervención de Abogado habilitado para ejercer su profesión en el tribunal que conozca del asunto, y Procurador igualmente habilitado para actuar en el tribunal que conozca del juicio (arts. 23.1 y 31.1 LEC), acompañándose a este escrito la escritura de apoderamiento para pleitos y la identificación de los dichos profesionales.

V.- PROCEDIMIENTO.

El presente proceso habrá de sustanciarse por los trámites del juicio verbal, de acuerdo con lo que establece el art. 599 LEC, formándose pieza separada del juicio ordinario, además de la de medidas cautelares.

VI.- CUANTÍA.

Cumpliendo con el deber de fijación en la demanda del interés económico litigioso del art. 253.1 LEC, se manifiesta que la cuantía del juicio asciende a [IMPORTE] euros ( [IMPORTE] €), que se corresponde con el valor catastral de la finca consignado en el recibo del impuesto sobre bienes inmuebles del pasado ejercicio, y que se ha adjunta como doc. nº [NÚMERO], siendo las reglas cuantificadoras las 2ª y 3ª del art. 251 LEC.

VII.- PROCEDIBILIDAD.

Justificación. El art. 595.3 LEC exige que con la demanda de tercería de dominio se aporte un principio de prueba por escrito del fundamento de la pretensión del tercerista, como así se hace con el acta notarial y documento de contrato privado de dación en pago de deuda de docs. nos. 1 y 2.

El demandante no ha interpuesto tercería anterior sobre el mismo bien (art. 597 LEC), sino una demanda de juicio ordinario para que se ordene judicialmente la elevación a pública de la adquisición de mi representado.

Tiempo. Esta tercería de dominio se interpone tempestivamente, puesto que cupiendo desde que se haya embargado el bien a que se refiera, aunque el embargo sea preventivo, no se deduce con posterioridad al momento en que, de acuerdo con lo dispuesto en la legislación civil, se producirá la transmisión del bien al acreedor o al tercero que lo adquiera en pública subasta, siendo que ni siquiera se ha formado todavía el título ejecutivo judicial, todo como determina el art. 596 LEC.

Cumplimiento de los requisitos de procedibilidad. La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 en relación con el art. 437.1 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

VIII.- ARGUMENTO DE FONDO.

Título de dominio. La tercería de dominio se ciñe a la pretensión del tercerista de que se alce el embargo del bien objeto de tercería, sin que pueda el ejecutante, y en su caso el ejecutado, pretender más que el mantenimiento del embargo o sujeción a la ejecución del bien objeto de tercería (art. 601 LEC).

El tribunal se pronunciará sobre la pertenencia del bien y la procedencia de su embargo a los únicos efectos de la ejecución en curso, sin que produzca efectos de cosa juzgada en relación con la titularidad del bien (art. 603.pfo.1º LEC).

Tal es doctrina ya consolidada [SSTS de 22 de julio de 1985, 2 de noviembre de 1987, 8 de febrero y 10 de junio de 1991, 24 de julio de 1992 y 2 de junio de 1994].

La pretensión ha de ser fundada en la titularidad del derecho de propiedad, u otro que, por disposición legal expresa, autorice a oponerse al embargo, o a la realización forzosa de un bien, como de pertenencia al ejecutado.

En el supuesto de esta demanda, se alega y prueba la propiedad del inmueble embargado por mi mandante, a través de negocio de dación en pago, realizado en fecha fehaciente, por acta notarial, por quien era apoderado de [DENOMINACIÓN SOCIAL], S.L., la titular registral, que no fue ratificado debidamente, pero que contenía el reconocimiento de una deuda de la mercantil que se extinguía con la transmisión de la oficina, que mi mandante D./Dña. [NOMBRE Y APELLIDOS] ha ocupado pacífica y públicamente desde hace más de cinco años.

La ‘datio pro soluto’ del art. 1.175 CCiv, es acto por el que el deudor transmite bienes de su propiedad a un acreedor, a fin de que aplique lo recibido a la extinción del crédito [SSTS de 2 de diciembre de 1994, 28 de junio, Rec. 2424/1993 y 14 de julio de 1997, Rec. 2257/1993].

El adquirente ha formulado demanda para que se otorgue documento que eleve a pública la transmisión, y en la que se ha acordado la anotación preventiva de la misma, asentada el [FECHA], pendiente la audiencia previa, y puesto que se ha declarado rebelde a [DENOMINACIÓN SOCIAL], S.L., el dictado de sentencia conforme al art. 429.8 LEC.

Por consiguiente, está acreditada la propiedad del bien embargado, la identidad con el trabado, y que el embargo se ha llevado a cabo para cubrir deudas de quien no era dueño cuando se produce la traba (, S.L.).

Anotación preventiva de embargo. La anotación preventiva de embargo sólo otorga rango preferente sobre los actos dispositivos celebrados, y sobre los créditos contraídos con posterioridad a la fecha de la propia anotación, y no en cuanto a los actos de disposición ni tampoco sobre los créditos anteriores que tienen una preferencia sobre el anotado (arts. 1.923.4º CCiv y 44 LH).

Pronunciamientos. Se pide, con arreglo al art. 604 LEC, que se alce el embargo, y la cancelación de la anotación preventiva en el Registro de la Propiedad, que se practicó para el aseguramiento de aquél.

IX.- COSTAS PROCESALES.

Las costas de este proceso deberán ser impuestas a la sociedad demandada, de conformidad con lo establecido en el art. 603.pfo.2º LEC, en relación con los arts. 394 y ss. LEC.

Por lo expuesto,

SUPLICO AL TRIBUNAL

que, por interpuesta la presente demanda, junto con los documentos que se acompañan, se digne admitirla, teniéndome por comparecida y parte en la representación que ostento en el presente juicio ordinario, entendiéndose conmigo las sucesivas actuaciones, y por formulada demanda de tercería de dominio contra el embargo preventivo acordado en los autos a favor de la mercantil [DENOMINACIÓN SOCIAL], S.A., y contra la misma, demandante en el proceso y sujeto activo del embargo preventivo, y tras los trámites oportunos dicte auto por el que se declare la pertenencia de la finca embargada a D./Dña. [NOMBRE Y APELLIDOS], y la improcedencia del embargo, a los únicos efectos de la medida cautelar acordada, y sin que produzca efectos de cosa juzgada en relación con la titularidad del bien, con cancelación de la anotación preventiva practicada en el Registro de la Propiedad, y expresa imposición de las costas al demandado.

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a

========================================================================
