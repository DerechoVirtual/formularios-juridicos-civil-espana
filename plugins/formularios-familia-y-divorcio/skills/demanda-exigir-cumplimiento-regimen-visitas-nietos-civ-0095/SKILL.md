---
name: demanda-exigir-cumplimiento-regimen-visitas-nietos-civ-0095
description: "Demanda para exigir el cumplimiento del régimen de visitas de los nietos con sus abuelos. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda para exigir el cumplimiento del régimen de visitas de los nietos con sus abuelos

> Formulario **CIV-0095** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda para exigir el cumplimiento del régimen de visitas de los nietos con sus abuelos» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda para exigir el cumplimiento del régimen de visitas de los nietos con sus abuelos” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-exigir-cumplimiento-regimen-visitas-nietos-civ-0095`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (17 veces)
- [ ] DOMICILIO A EFECTOS DE NOTIFICACIONES (3 veces)
- [ ] Nº (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] FECHA (2 veces)
- [ ] NOMBRE DEL MENOR (2 veces)
- [ ] TIPO Y Nº DE PROCEDIMIENTO (2 veces)
- [ ] AÑO
- [ ] DÍA
- [ ] LUGAR
- [ ] MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] MES
- [ ] Nº DE COLEGIADO/A
- [ ] Nº DE DOCUMENTO

## Normas que cita el formulario

- art. 155.2 Ley 1/2000
- art. 160 Código Civil
- art. 85.1 LOPJ
- art. 437.1 LEC
- art. 5 Ley Orgánica 1/2025
- art. 160 CC
- art. 110 Código Civil
- art. 158 CC

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

- Junto a «…A, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE Q.P.T.R.C.»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.

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

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE Q.P.T.R.C.

D./dña., Procurador/a de los Tribunales con número de colegiado/a [Nº DE COLEGIADO/A] y de don/dña., según escritura de poder para pleitos que acompaño al presente escrito de demanda para su inserción en los autos con devolución de su original por precisarlo para otros usos, ante el Tribunal comparezco y como mejor en Derecho proceda DIGO:

Que en la representación que ostento y siguiendo instrucciones de mi poderdante formulo DEMANDA DE JUICIO VERBAL contra doña [NOMBRE Y APELLIDOS], a fin de que se condene a la demandada a dar cumplimiento al régimen de visitas, estancia y comunicaciones acordado a favor de los abuelos maternos/paternos [NOMBRE Y APELLIDOS] del menor [NOMBRE DEL MENOR] en sentencia dictada en fecha [FECHA] por el Tribunal de Instancia al que me dirijo en procedimiento de separación matrimonial con número de autos [TIPO Y Nº DE PROCEDIMIENTO] y en su caso, se adopten las medidas que el Juzgador estime necesarias para la efectividad de lo peticionado.

A los efectos prevenidos en el artículo 399 en relación con el artículo 155.2 de la Ley 1/2000, de 7 de enero, de Enjuiciamiento Civil consigno los siguientes datos y circunstancias de identificación de la parte actora y de la parte demandada:

1.-DE LA PARTE ACTORA.

DÑA., con domicilio a efectos de notificaciones en [DOMICILIO A EFECTOS DE NOTIFICACIONES] y provista de D.N.I. número [NÚMERO]

D. [NOMBRE Y APELLIDOS], con domicilio a efectos de notificaciones en [DOMICILIO A EFECTOS DE NOTIFICACIONES] y provisto de D.N.I. número [NÚMERO]

La parte actora está representada por el/la Procurador/a de los Tribunales don/doña [NOMBRE Y APELLIDOS] y defendido/a por el Letrado/a D/Dña. [NOMBRE Y APELLIDOS] con domicilio profesional en

2.-DE LA PARTE DEMANDADA.

D/DÑA., con domicilio a efectos de notificaciones en [DOMICILIO A EFECTOS DE NOTIFICACIONES] y provista de D.N.I. número [NÚMERO]

Fundo la presente demanda en los siguientes hechos y fundamentos de derechos.

HECHOS

PRIMERO.- DEL DERECHO DE MIS MANDANTES EN LA PRESENTE CONTIENDA. Mis mandantes están legitimados para ejercitar el derecho reclamado en el presente litigio en su calidad de abuelos paternos del menor [NOMBRE DEL MENOR] de [Nº] años de edad, hijo de don [NOMBRE Y APELLIDOS] y de doña [NOMBRE Y APELLIDOS], siendo a su vez don/dña. hijo/a de mis representados.

Se adjuntan al presente escrito como documentos números 1 y 2 certificados literales de nacimiento del menor don [NOMBRE Y APELLIDOS] y de don [NOMBRE Y APELLIDOS] hijo de los actores.

SEGUNDO.- DE LOS PRONUNCIAMIENTOS DE LA SENTENCIA DE SEPARACIÓN MATRIMONIAL. En procedimiento de separación matrimonial instado por don [NOMBRE Y APELLIDOS], hijo de mis representados, contra doña [NOMBRE Y APELLIDOS] se adjudicó la guarda y custodia del hijo común del matrimonio a la madre, privándose el derecho de visitas y estancia al padre como consecuencia de la interposición de una querella por agresión sexual contra el mismo. Dicha circunstancia motivó que fueran dictados en sentencia de separación matrimonial los siguientes pronunciamientos a favor de los abuelos paternos:

• Régimen de visitas y estancia.

El menor podrá pasar con los abuelos paternos los fines de semana alternos desde las diez horas a las veintiuna horas del sábado y del domingo pernoctando en el domicilio familiar. En los períodos vacacionales los abuelos podrán tener consigo al menor durante quince días de las vacaciones de verano y una semana de las de Navidad, siendo los abuelos quienes elijan los días los años impares y la madre los años pares.

• Comunicaciones.

Los abuelos podrán comunicar telefónicamente con el menor cuantas veces lo consideren oportuno.

Se adjunta al presente escrito como documento número 3 testimonio de la sentencia de separación matrimonial en la que constan los pronunciamientos relativos al régimen de visitas, estancia y comunicaciones de los abuelos paternos.

TERCERO.- DEL INCUMPLIMIENTO DE LA MADRE DEL RÉGIMEN DE VISITAS, ESTANCIAS Y COMUNICACIONES DICTADO A FAVOR DE LOS ABUELOS PATERNOS. Los abuelos paternos llevan más de cinco meses sin comunicar con su nieto de [Nº] años de edad ante la incomprensible y arbitraria negativa de la madre/padre [NOMBRE Y APELLIDOS] a que el menor atienda sus llamadas telefónicas. Mis mandantes y el menor vienen siendo privados de cualquier tipo de contacto y relación personal, incumpliéndose el régimen de visita, estancia y comunicaciones dictado en sentencia de separación matrimonial.

Mis representados se han visto impelidos a interponer la presente acción ante la imposibilidad de llegar a un buen entendimiento con la madre del menor y en protección del interés del mismo, teniendo en consideración que con anterioridad a la separación matrimonial los abuelos mantenían una relación afectiva muy estrecha con su nieto al ser los encargados de recogerlo diariamente a la salida del colegio, quedándose a menudo a pernoctar en su domicilio familiar. Ni que decir cabe que dicha situación está causando a mis mandantes un daño emocional y personal que del mismo modo debe sufrir el menor.

Hallándose próximo el período vacacional de verano mis representados desean pasar los quince días acordados en sentencia de separación matrimonial con su nieto y evitar de este modo que persista la actual situación, en interés único y exclusivo del desarrollo personal, social y familiar del menor quien siempre había mostrado un cariño y afecto incondicional a sus abuelos.

Desconoce esta representación los motivos que llevan a la madre a privar a mis representados del derecho a disfrutar de su nieto, al carecer de justa causa para ello, si bien previamente a la interposición de la presente acción mis representados han unido todos sus esfuerzos para resolver familiarmente la situación planteada resultando del todo inútiles.

Estima esta representación que el derecho peticionado en la presente contienda es de cabal importancia para el menor no pudiendo este derecho ser impedido unilateral y caprichosamente por quien dispone de la guarda y custodia.

CUARTO.- SOBRE EL PROCESO DE NEGOCIACIÓN PREVIO Y MEDIOS DE SOLUCIÓN DE CONTROVERSIAS DE MANERA AMISTOSA Y EXTRAJUDICIAL. Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento nº [Nº DE DOCUMENTO]

A) FUNDAMENTOS DE DERECHO PROCESALES.

Capacidad de la parte actora y de la demandada

El artículo 6 apartado 1 de la Ley de Enjuiciamiento civil, titulado «la capacidad para ser parte» establece que «Podrán ser parte en los procesos ante los tribunales civiles: 1º. Las personas físicas», de lo que se infiere que tanto los actores como la demandada tienen capacidad para ser parte.

Legitimación activa y pasiva

La legitimación activa la ostentan mis mandantes por ser los abuelos paternos del menor, según se acredita mediante los certificados literales de nacimiento adjuntos al presente escrito de demanda como documentos números 1 y 2, y de conformidad con el artículo 160 del Código Civil.

La legitimación pasiva la ostenta la demandada por ser la madre del menor y la titular de la patria potestad y la guarda y custodia que está privando sin justa causa del disfrute del régimen de visitas, estancia y comunicaciones a los abuelos paternos y al nieto.

Postulación y defensa

Se cumplen con las normas de postulación ya que mi mandante comparece en el presente procedimiento representado por el Procurador de los Tribunales, tal y como ya se ha indicado en el encabezamiento del presente escrito y en virtud de los poderes que se acompañan, y bajo la dirección del letrado firmante conforme a lo dispuesto en los artículos 23 y 31 de la Ley de Enjuiciamiento Civil.

Requisitos formales

Se inicia el presente procedimiento por medio de demanda que reúne todos los requisitos exigidos en el artículo 399 de la Ley de Enjuiciamiento Civil y demás relativos a esta materia.

Jurisdicción

El orden jurisdiccional civil es el único competente para conocer de los negocios o demandas civiles que se susciten en territorio español, entre españoles, extranjeros y entre españoles y extranjeros, con arreglo a lo estipulado en la Ley Orgánica del Poder Judicial y en los tratados y convenios internacionales.

Competencia funcional

Es competente el Tribunal de Instancia para conocer el presente litigio, a tenor de lo estipulado en el artículo 45 de la Ley de Enjuiciamiento Civil, en relación con lo dispuesto en el art. 85.1º LOPJ.

Competencia territorial

Son competentes los Tribunales a los que me dirijo al ser los que tramitaron la separación matrimonial.

Clase de juicio

A tenor de lo establecido en el ordinal 12º del apartado primero del artículo 250 de la Ley de Enjuiciamiento Civil, el presente procedimiento al pretender la efectividad de los derechos reconocidos en el artículo 160 del Código Civil debe tramitarse por las normas relativas al Juicio Verbal con las peculiaridades dispuestas en el capítulo I del título I del libro IV de la Ley de Enjuiciamiento Civil.

Intervención del ministerio fiscal

Teniendo el nieto la edad de seis años de conformidad con el artículo 749 de la Ley de Enjuiciamiento Civil resulta preceptiva la intervención del Ministerio Fiscal «2. En los demás procesos a que se refiere este título será preceptiva la intervención del Ministerio Fiscal, siempre que alguno de los interesados en el procedimiento sea menor, incapacitado o esté en situación de ausencia legal».

Cumplimiento de los requisitos de procedibilidad

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC en relación con el art. 437.1 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

Costas

Las costas se impondrán a la parte cuyas pretensiones se hayan visto totalmente rechazadas, conforme establece el artículo 349 de la Ley de Enjuiciamiento Civil.

B) FUNDAMENTOS DE DERECHO SUSTANTIVO.

• SOBRE EL DERECHO DE LOS ABUELOS A RELACIONARSE CON EL NIETO. El párrafo segundo del artículo 160 del Código Civil modificado por la Ley 42/2003, de 21 de noviembre, dispone que «No podrán impedirse sin justa causa las relaciones personales del hijo con sus abuelos y otros parientes y allegados. En caso de oposición, el juez, a petición del menor, abuelos, parientes o allegados, resolverá atendidas las circunstancias».

Mis mandantes han peticionado a través de la presente demanda el reconocimiento del derecho regulado en el artículo 160 del Código Civil, no mediando justa causa que impida las relaciones personales de los abuelos con su nieto.

Es unánime el criterio jurisprudencial que protege el derecho de los abuelos a relacionarse con el nieto. Así, entre otras, se manifiestan las siguientes resoluciones: Sentencia del Tribunal Supremo de 23 de noviembre de 1999, rec. 1048/1995 y las en ella citadas de 11 de junio de 1996, rec. 3446/1991 y 17 de septiembre de 1996, rec. 2631/1992 y de 11 de junio de 1998, rec. 1474/1994.

Sentencia de la Audiencia Provincial núm. 317/2002 Zaragoza (Sección 4ª), de 20 mayo. «El derecho a comunicar con los nietos que asiste a los abuelos se asienta sólidamente en el artículo 160 CC, como se ha ocupado de señalar reiteradamente el TS en STS 7 abril 1994 11 junio 1996, 17 septiembre 1996, 11 junio 1998 y 23 noviembre 1999, siendo la última ocasión en que se ha ocupado de él el auto de fecha 3 mayo 2000.

Según la doctrina jurisprudencial que se contiene en dichas resoluciones este tipo de relaciones, que insertan beneficiosamente al menor en su entorno familiar completo, resultan más necesarias cuando de los ascendientes se trata, por su privilegiado grado de parentesco, dado que la personalidad se forja también entre las contradicciones que emanan, a veces de los planteamientos y opiniones de los parientes, siempre que revistan un carácter de normalidad, o sea, no respondan a patologías o ejemplos corruptores, sin que pueda afirmarse, por lo dicho anteriormente en cuanto a la apreciación probatoria realizada por las sentencias impugnadas, que la relación de los abuelos con el menor vaya a suponer un ejemplo corruptor.»

En cualquier caso, debe atenderse al interés fundamental del menor al resolver el litigio planteado primando, inclusive sobre su parecer, de conformidad con el artículo 39 de Constitución Española, artículos 110 y 154 del Código Civil, Ley Orgánica 1/1996 de Protección del Menor y la Declaración Universal de los Derechos del Niño, son de interés jurisprudencial las siguientes sentencias:

Sentencia de la Audiencia Provincial Zaragoza (Sección 4ª) 317/2002 de 20 mayo: "a lo dicho no puede ser opuesta la voluntad contraria de los menores afectados, pues es doctrina general que se mantiene en las resoluciones de la AP que el parecer del menor, aún cuando sea mayor de la edad en que la Ley impone su consulta, no ha de ser determinante de la decisión judicial en los asuntos que le afectan, pues ha de prevalecer su interés (SSAP Vizcaya12 septiembre 1995, Tarragona 2 octubre y 11 noviembre 1993, Barcelona 13 junio 1993, Álava 15 marzo 1993 y Salamanca 4 noviembre 1992).

AATS de 30 marzo 1999, rec. 646/1996 y 3 de mayo de 2000, rec. 971/1998 en el que se afirma que: "en cuanto a la alegación de que no debería obligarse a cumplir el derecho de los abuelos a relacionarse con el menor, como principio inspirador de todo lo relacionado con él, vincula al Juzgador, a todos los Poderes Públicos e, incluso, a los padres y ciudadanos, con reconocimiento pleno de la titularidad de derechos en los menores de edad y de una capacidad progresiva para ejercerlos, de manera que han de adoptarse aquellas medidas que sean más adecuadas a la edad del sujeto, para ir construyendo progresivamente el control acerca de su situación personal y proyección de futuro, evitando siempre que el menor pueda ser manipulado, buscando, por el contrario, su formación integral y su integración familiar y social, de manera que las medidas que los jueces pueden adoptar (art. 158 CC) se amplían a todo tipo de situaciones, incluso aunque excedan de las meramente paterno-filiales, con la posibilidad de que las adopten al inicio, en el curso o después de cualquier procedimiento conforme las circunstancias cambien y oyendo al menor, según se desprende de la Ley Orgánica 1/1996, de 15 de enero, de protección jurídica del menor, aplicable retroactivamente por mandato constitucional y por recoger el espíritu de cuantas convenciones internacionales vinculan a España (así, Convención de Naciones Unidas de 20 de noviembre de 1989, ratificada por instrumento de 30 de noviembre de 1990)".

• SOBRE EL EJERCICIO DE LA PATRIA POTESTAD POR PARTE DEL PROGENITOR QUE INCUMPLE EL RÉGIMEN DE VISITAS, ESTANCIA Y COMUNICACIONES. Esta representación desea poner de manifiesto que el ejercicio de la patria potestad comprende el deber de velar por los intereses de los hijos, siendo tal y como ha sido anteriormente puesto de manifiesto de excepcional importancia para el desarrollo personal, familiar y social del menor la relación de los mismos con los abuelos de ambas ramas familiares.

En su virtud,

AL TRIBUNAL SUPLICO: que teniendo por presentado este escrito junto con sus documentos adjuntos y la escritura de poder en la forma indicada en el encabezamiento, se sirva admitirlos y tenerme por comparecido en nombre y representación de don [NOMBRE Y APELLIDOS] y doña [NOMBRE Y APELLIDOS] y por formulada DEMANDA DE JUICIO VERBAL contra la demandada doña [NOMBRE Y APELLIDOS], emplazándola debidamente y, sustanciada por todos sus trámites y en méritos de los hechos y fundamentos de derecho alegados se dicte Sentencia por la que se condene a Dña. a cumplir con el régimen de visitas, estancia y comunicaciones dictado a favor de los abuelos paternos don [NOMBRE Y APELLIDOS] y doña [NOMBRE Y APELLIDOS] en sentencia de separación matrimonial de fecha [FECHA] dictada por el Tribunal de Instancia al que me dirijo en procedimiento de separación matrimonial número de autos [TIPO Y Nº DE PROCEDIMIENTO], tomándose para ello las medidas que el Juzgador estime más oportunas.

OTROSÍ DIGO PRIMERO.-En cumplimiento con lo dispuesto en el artículo 253 de la Ley de Enjuiciamiento Civil se fija la cuantía de la demanda en indeterminada por carecer el objeto de interés económico. Ello no obstante, se interesa se proceda a sustanciar el procedimiento por las normas del juicio verbal por remisión al ordinal 12º del apartado primero del artículo 250 de la Ley de Enjuiciamiento Civil.

AL TRIBUNAL SUPLICO.-Se tenga por realizada la anterior manifestación a los efectos legales oportunos.

OTROSÍ DIGO SEGUNDO.-Que siendo la voluntad de esta representación la de cumplir los requisitos exigidos por la Ley, intereso que de conformidad con el artículo 231 de la Ley de Enjuiciamiento Civil pueden ser subsanados los defectos en que incurran los actos procesales de esta parte.

AL TRIBUNAL SUPLICO.-Se tenga por efectuada la anterior manifestación a los efectos legales oportunos.

OTROSÍ DIGO TERCERO.-Que esta parte interesa el recibimiento a prueba en el momento procesal oportuno.

AL TRIBUNAL SUPLICO.-Que se tenga por efectuada la anterior manifestación a los efectos legales oportunos.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Fdo. Letrado. Fdo. Procurador.

Coleg. núm. Coleg. núm. [Nº]

========================================================================
