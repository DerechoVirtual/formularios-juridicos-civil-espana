---
name: escritura-publica-eleva-publico-acuerdos-mediacion-civ-1755
description: "Escritura pública que eleva a público los acuerdos de una mediación familiar. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escritura pública que eleva a público los acuerdos de una mediación familiar

> Formulario **CIV-1755** del plugin **Mediación, MASC, arbitraje y jurisdicción voluntaria** (`formularios-mediacion-arbitraje-y-voluntaria`) · Civil › Jurisdicción voluntaria, MASC, mediación y arbitraje · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escritura pública que eleva a público los acuerdos de una mediación familiar» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escritura pública que eleva a público los acuerdos de una mediación familiar” para mi caso». También puedes invocarla directamente con `/formularios-mediacion-arbitraje-y-voluntaria:escritura-publica-eleva-publico-acuerdos-mediacion-civ-1755`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-mediacion-arbitraje-y-voluntaria:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Mediación, MASC, arbitraje y jurisdicción voluntaria) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (13 veces)
- [ ] AÑO (2 veces)
- [ ] DÍA (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] MES (2 veces)
- [ ] Nº (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] CIRCUNSTANCIAS PERSONALES

## Normas que cita el formulario

- art. 25.1.I Ley 5/2012
- art. 25 Ley 5/2012
- art. 11 Ley 5/2012
- art. 9 Ley 5/2012

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

OTORGANTES: Los consortes DON/DOÑA [NOMBRE Y APELLIDOS] y DON/DOÑA [NOMBRE Y APELLIDOS] y el profesional mediador DON/DOÑA [NOMBRE Y APELLIDOS]

NÚMERO [NÚMERO]

ESCRITURA DE CONTRATO MEDIADO

En [LOCALIDAD], mi residencia, a [DÍA] de [MES] de [AÑO]

Ante mí, Notario de ésta Capital y su Ilustre Colegio,

COMPARECEN:

Como partes mediadas: Los consortes DON/DOÑA [NOMBRE Y APELLIDOS] y DON/DOÑA [NOMBRE Y APELLIDOS], [CIRCUNSTANCIAS PERSONALES].

Como parte mediadora: DON/DOÑA [NOMBRE Y APELLIDOS], con número [NÚMERO] en el Registro de mediadores de [LOCALIDAD].

Constan sus circunstancias personales de sus manifestaciones.

INTERVIENEN:

Todos ellos en su propio nombre y derecho. La persona/s mediadora/s sólo a los efectos de reconocer su intervención como tal/es en el proceso de mediación del que derivan los acuerdos que ahora se elevan a escritura pública y la autenticidad de su firma, que se legitimará, en los documentos que se protocolizan. (En el caso de que intervengan; intervención que, como ya hemos dicho, no es preceptiva, conforme al art. 25.1.II de la Ley 5/2012, de 6 de julio, de mediación en asuntos civiles y mercantiles).

IDENTIFICO a los comparecientes a través de sus reseñados documentos de identidad, que me exhiben y compruebo, y tienen, a mi juicio, según intervienen, capacidad legal necesaria para otorgar la presente escritura de ELEVACIÓN A PÚBLICO DE ACUERDO ADOPTADO EN PROCESO DE MEDIACIÓN FAMILIAR, a cuyo fin:

EXPONEN:

Que DON/DOÑA [NOMBRE Y APELLIDOS] y DON/DOÑA [NOMBRE Y APELLIDOS], se sometieron a un proceso de mediación familiar guiado, como parte mediadora por DON/DOÑA [NOMBRE Y APELLIDOS], en las condiciones reflejadas en el Acta inicial, de fecha [DÍA] de [MES] de [AÑO], copia de la cual se protocoliza en esta matriz, estando sometido el citado proceso de mediación a la Ley 5/2012, de 6 de julio, de mediación en asuntos civiles y mercantiles

Que tras celebrarse las sesiones previstas, se ha alcanzado un acuerdo parcial relativo a la siguiente cuestión: guarda y custodia del/de la hija menor de la pareja, cuyo contenido es el siguiente:

"GUARDA Y CUSTODIA DEL HIJO/A COMÚN: El hijo/a menor de edad, quedará bajo la guarda y custodia compartida de ambos progenitores, que ostentan la titularidad de su patria potestad, por considerar este sistema el más adecuado para el buen desarrollo, educación y equilibrio emocional del hijo/a, lo que se llevará a efecto de conformidad a cuanto sigue:

1.- El padre y la madre acuerdan expresamente que cuantas decisiones sean necesarias en cuestiones que afecten directa o indirectamente al/a la menor, serán consultadas y decididas por ambos progenitores. Entre estas cuestiones quedan incluidas las que conciernan al hijo/a referentes a elección de colegio, clases particulares, actividades extraescolares, cursos en el extranjero, viajes o salidas al extranjero en el que no vayan acompañados por algún progenitor, tratamientos médicos o intervenciones quirúrgicas, etc.

Cuando el hijo/a menor de edad, se encuentren bajo la custodia de uno (guarda y custodia) u otro progenitor (régimen de visitas y estancias), deberán informarse mutuamente y de manera inmediata de cualquier circunstancia que acontezca respecto del/de la menor y que tenga carácter relevante y muy especialmente de cualquier enfermedad, favoreciendo y facilitando el contacto. Igualmente, ambos progenitores tendrán derecho a estar informados del rendimiento escolar, para lo cual, tendrán pleno derecho a asistir y recibir cuanta información requieran del Colegio donde asista el/la menor.

2.- La guarda y custodia se atribuye al padre y a la madre por periodos alternativos de una semana, comenzando por el padre (o madre). No se computan los meses de Julio y Agosto, por corresponder a estancias vacacionales.

3.- En el periodo en que un progenitor tenga la guarda y custodia del/de la menor, se establece para el otro el siguiente régimen de visitas:

Durante la Semana fuera de períodos vacacionales.

Fines de semana.

El/La menor estará con el progenitor que no tenga la guarda los domingos desde las 9 h., recogiéndolo en el domicilio del progenitor que tenga la guarda, y se encargará de llevarlo al colegio los lunes por la mañana.

De lunes a viernes.

El/La menor estará con el progenitor que no tenga la guarda un día entre semana —de no acordar otra cosa ambos progenitores, será el miércoles— desde la salida del colegio, o en su defecto las 17 horas hasta las 21 horas, momento en el que será reintegrado en el domicilio del progenitor que tenga la guarda y custodia del/de la menor esa semana.

Días festivos y puentes escolares fuera de períodos vacacionales.

Se distribuirán por mitad entre al padre y la madre. En caso de desacuerdo sobre la concreta distribución, la madre (o el padre) tendrá preferencia para elegir si el menor permanece con ella (o él) o con el padre (o la madre) el primer festivo o puente que se presente. El siguiente, el/la menor permanecerá con el otro progenitor y a partir de ahí se irán alternando las estancias con uno y otro. Los puentes no se dividirán, salvo que ambos progenitores acuerden lo contrario.

Vacaciones de Navidad, Semana Santa y Verano.

Las vacaciones escolares de Navidad, Semana Santa y Verano, serán repartidas por mitad entre los progenitores, correspondiendo a la madre (o al padre) la primera mitad los años pares y la segunda los impares, y al padre (o a la madre) a la inversa, salvo que ambos acuerden otro reparto diferente, haciéndose las siguientes puntualizaciones:

Primera. La recogida del/de la menor será a las 11 horas del primer día de vacaciones y finalizará a las 21 horas del último día que corresponda al que disfruta del primer periodo, o las 21 horas del último día de las vacaciones escolares al que disfrute del segundo periodo.

Segunda. En las vacaciones de Navidad, en todo caso, con independencia de a qué progenitor corresponda cada periodo se considerarán aparte los siguientes días: Nochebuena, que corresponderá al padre (o a la madre), y Navidad, que corresponderá a la madre (o al padre).

Tercera. Las vacaciones de verano comprenderán los meses de Julio y Agosto, y se distribuirán en cuatro quincenas, correspondiendo al padre (o a la madre) elegir en los años impares las dos quincenas que estará con el/la menor, y a la madre (o al padre) en los pares, pudiendo ser consecutivas las referidas quincenas.

Comunicaciones telefónicas.

Ambos progenitores podrán comunicarse telefónicamente con su hijo/a con total libertad, respetándose para este tipo de comunicación el horario de descanso o estudio del/de la menor, y para el caso de que en periodo de vacaciones escolares se marchara de viaje, ambos progenitores se facilitarán un teléfono de contacto o colaborarán en que el/la menor efectúe la pertinente llamada telefónica. Todo ello se llevará a efecto, dentro de criterios de flexibilidad y atendiendo siempre, prioritariamente, al interés del/de la hijo/a."

Que el citado acuerdo consta en el Acta final del proceso de mediación, copia de la cual se protocoliza en esta matriz.

Que, conforme con lo dispuesto en los artículos 25 y siguientes de la Ley 5/2012, de 6 de julio, de mediación en asuntos civiles y mercantiles, las partes mediadas, DON/DOÑA [NOMBRE Y APELLIDOS] y DON/DOÑA [NOMBRE Y APELLIDOS], han decidido ELEVAR A ESCRITURA PÚBLICA EL ACUERDO OBJETO DE MEDIACIÓN, lo cual llevan a efecto, con arreglo a las siguientes:

ESTIPULACIONES:

DON/DOÑA [NOMBRE Y APELLIDOS] y DON/DOÑA [NOMBRE Y APELLIDOS], conforme a lo previsto en el artículo 25 de la Ley 5/2012, de 6 de julio, acuerdan la elevación a escritura pública del acuerdo objeto de mediación transcrito en el expositivo II, ratificándose en el mismo, dotándolo así de fuerza ejecutiva, de conformidad con lo dispuesto en la Ley.

GASTOS: Los gastos derivados de la presente escritura serán satisfechos con arreglo a ley.

TESTIMONIO DE LEGITIMACIÓN DE FIRMAS:

Los comparecientes, en mi presencia, reconocen como suyas las firmas que obran en las Actas inicial y final del proceso de mediación protocolizadas en esta matriz, por lo que yo, el Notario, las legitimo.

REQUERIMIENTO AL MEDIADOR:

Requerido por el autorizante, manifiesta que reúne las condiciones para ejercer como mediador previstas en el artículo 11 de la Ley 5/2012, de 6 de julio, sin que, tal y como exige el artículo 13 de la misma Ley, existan circunstancias que hayan podido afectar a su imparcialidad o generar un conflicto de intereses con las personas mediadas.

ADVERTENCIAS:

Advierto a las partes mediadora y mediadas del deber de confidencialidad que pesa sobre ellas con sus excepciones, conforme al artículo 9 de la Ley 5/2012, de 6 de julio, con la responsabilidad que puede derivar de su incumplimiento.

Les advierto, así mismo, de la caducidad de la acción ejecutiva fundada en el acuerdo de mediación prevista en el Artículo 518 de la Ley de Enjuiciamiento Civil, redactado según la Ley 5/2012, de 6 de julio.

CONTROL DE LEGALIDAD:

Conforme a lo previsto en el artículo 25 de la Ley 5/2012, de 6 de julio, yo, el Notario, declaro cumplidos los requisitos exigidos por la citada Ley y que el contenido del acuerdo mediado no es contrario a Derecho.

DOCUMENTOS PROTOCOLIZADOS:

- Acta inicial del procedimiento de mediación.

- Acta final del procedimiento de mediación.

OTORGAMIENTO Y AUTORIZACIÓN:

Así lo dicen y otorgan los comparecientes ante mí, después de hacerles las reservas y advertencias legales pertinentes, especialmente las fiscales.

Respecto a los datos personales recogidos en el presente documento, debe tenerse en cuenta que el tratamiento de los mismos se ajustará a la LO 3/2018, de 5 de diciembre, de Protección de Datos de Carácter Personal y Garantía de los Derechos Digitales, en desarrollo y aplicación del Reglamento UE 2016/679, de 27 de abril, y que el interesado podrá ejercitar sus derechos de acceso, rectificación, cancelación, supresión (derecho al olvido), portabilidad, oposición y limitación del tratamiento de los datos (ARCO-POL) en los términos establecidos en los arts. 12 a 23 y 12 a 18 de los citados Reglamento y Ley Orgánica, respectivamente.

Leo a los comparecientes esta escritura, previa advertencia del derecho que para hacerlo por sí les asiste, al que renuncian. Se ratifican, prestan su consentimiento y, en prueba de conformidad, la firman conmigo, que doy fe de lo contenido en este instrumento público, de que el consentimiento de los otorgantes-mediados ha sido libremente prestado y de que el otorgamiento se adecua a la legalidad.

De todo lo cual, extendido en [Nº] folios de papel timbrado del Estado, exclusivo para documentos notariales de la serie y números [Nº], yo el Notario, DOY FE.

SIGUEN LAS FIRMAS DE LOS COMPARECIENTES.- SIGNADO: .- RUBRICADO Y SELLADO.

APLICACION ARANCEL:

========================================================================
