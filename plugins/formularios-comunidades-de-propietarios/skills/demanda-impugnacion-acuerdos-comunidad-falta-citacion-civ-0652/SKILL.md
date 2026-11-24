---
name: demanda-impugnacion-acuerdos-comunidad-falta-citacion-civ-0652
description: "Demanda de impugnación de acuerdos de la comunidad por falta de citación a la junta. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de impugnación de acuerdos de la comunidad por falta de citación a la junta

> Formulario **CIV-0652** del plugin **Comunidades de propietarios** (`formularios-comunidades-de-propietarios`) · Civil › Propiedad horizontal · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio ordinario por la que un propietario impugna un acuerdo de la junta de propietarios en régimen de propiedad horizontal al que no fue citado (art. 16.2 LPH) y que es contrario a la ley por modificar el título constitutivo sin unanimidad (art. 18.1.a LPH): en el modelo, la apertura de una segunda puerta en los paramentos del elevador de vehículos de un garaje para dar salida directa a ciertas parcelas.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de impugnación de acuerdos de la comunidad por falta de citación a la junta» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de impugnación de acuerdos de la comunidad por falta de citación a la junta” para mi caso». También puedes invocarla directamente con `/formularios-comunidades-de-propietarios:demanda-impugnacion-acuerdos-comunidad-falta-citacion-civ-0652`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-comunidades-de-propietarios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Comunidades de propietarios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (8 veces)
- [ ] DOMICILIO (4 veces)
- [ ] AÑO (3 veces)
- [ ] DÍA (3 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] MES (3 veces)
- [ ] FECHA (2 veces)
- [ ] FIRMA (2 veces)
- [ ] Nº DE APARTADO (2 veces)
- [ ] Nº DE PARCELAS (2 veces)
- [ ] COLEGIO
- [ ] CONTENIDO DEL ACUERDO IMPUGNADO
- [ ] DENOMINACIÓN SOCIAL DE LA CONSTRUCTORA
- [ ] IMPORTE
- [ ] NOMBRE Y APELLIDOS DEL DEMANDANTE
- [ ] NOMBRE Y APELLIDOS DEL LETRADO/A
- [ ] NOMBRE Y APELLIDOS DEL PRESIDENTE/A
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] Nº DE COLEGIADO
- [ ] Nº DE DOCUMENTO
- [ ] PISO
- [ ] PORCENTAJE
- [ ] SEDE

## Normas que cita el formulario

- art. 265.2 LEC
- art. 9.2 LOPJ
- art. 36 LEC
- art. 44 LEC
- art. 85.1 LOPJ
- art. 52.1.8.º LEC
- art. 54.1 LEC
- art. 58 LEC
- art. 18.1 LPH
- art. 249.1 LEC
- art. 18.2 LPH
- art. 13.3 LPH
- art. 25 LEC
- art. 23 LEC
- art. 16.2 LPH
- art. 18 LPH
- art. 17.6 LPH
- art. 253.1 LEC
- art. 394 LEC
- art. 16.4 LPH
- art. 6 Código Civil

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

### Avisos de actualización (4) — se aplican en el texto, nunca se copian en el documento

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…e solución de controversias de la LO 1/2025 para la Ley de Propiedad Horizontal.»: requisito de procedibilidad (art. 5 LO 1/2025): antes de demandar hay que intentar un medio adecuado de solución de controversias y acreditarlo con la demanda, salvo las materias excluidas del art. 5.2. Comprobar, según el criterio de la Audiencia Provincial del territorio, si la impugnación de acuerdos de propiedad horizontal queda o no exceptuada, y mantener o suprimir este fundamento en consecuencia.
- Junto a «…je, cosa que obviamente no es imputable a nadie más que al titular del vehículo.»: comprobar la redacción vigente del art. 17 LPH (reformas de 2013 y 2019) para el apartado exacto que exige unanimidad para modificar el título constitutivo o los estatutos y para las mayorías en materia de accesibilidad.
- Junto a «…a Provincial, que desde la óptica del recurso de casación resultan inatacables».»: las sentencias reproducidas son anteriores a las reformas de la LPH de 2013 y 2019 y a la Ley 8/2021; comprobar su vigencia doctrinal y los preceptos citados antes de invocarlas.

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

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, que actúa en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDANTE], con domicilio en [LOCALIDAD], calle [DOMICILIO], número [Nº], piso [PISO], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento n.º [Nº DE DOCUMENTO]; siendo la dirección letrada de D./Dña. [NOMBRE Y APELLIDOS DEL LETRADO/A], abogado/a del Ilustre Colegio de [COLEGIO] con número de colegiado [Nº DE COLEGIADO], con despacho profesional abierto en [LOCALIDAD], sito en [DOMICILIO], ante el Tribunal comparezco y, como mejor proceda en Derecho, DIGO:

Que mediante el presente escrito y en nombre de mi principal vengo a formular demanda de juicio declarativo ordinario en materia de propiedad horizontal contra la Comunidad de Propietarios de la casa señalada con el número [Nº] de la calle [DOMICILIO]; demanda en la que se ejercita la acción de impugnación de acuerdos comunitarios.

Conforme a lo señalado en el art. 399 de la Ley de Enjuiciamiento Civil, se hacen constar los siguientes

HECHOS

PRIMERO.– Mi mandante es propietario de la vivienda sita en [DOMICILIO], a la que corresponde un coeficiente de participación del [PORCENTAJE] % como integrante de la Comunidad demandada. (Se acompaña como documento n.º [Nº] el título consistente en la escritura de compraventa).

SEGUNDO.– La Comunidad de propietarios demandada tiene por legal representante a D./Dña. [NOMBRE Y APELLIDOS DEL PRESIDENTE/A], que ostenta el cargo de Presidente/a por su nombramiento vigente desde la Junta de fecha [FECHA]. (Se acompaña como documento n.º [Nº] certificación obtenida del libro de actas, y se señalan el mismo y los archivos de la Comunidad a los efectos del art. 265.2 LEC).

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— TERCERO.– Con fecha [DÍA] de [MES] de [AÑO] se celebró Junta de propietarios, en la que se tomó el acuerdo, entre otros, de abrir en las paredes traseras de fábrica del edificio que contienen el elevador de vehículos a las parcelas de garaje de las plantas de sótano, a fin de practicar una segunda puerta para tal elevador y permitir la salida directa desde el mismo a las parcelas números [Nº DE PARCELAS], cuyo tenor literal es el del acta que me ha sido remitida y que se acompaña como documento n.º [Nº].

— TERCERO.– Con fecha [DÍA] de [MES] de [AÑO] se celebró Junta de propietarios, en la que se tomó el acuerdo de [CONTENIDO DEL ACUERDO IMPUGNADO], cuyo tenor literal es el del acta que se acompaña como documento n.º [Nº].

CUARTO.– Por causas que esta parte desconoce, mi mandante no fue citado a la celebración de la Junta, por lo que, evidentemente, no pudo asistir a la misma ni manifestar su oposición frente al apartado [Nº DE APARTADO] precitado de los acuerdos tomados en dicha Junta, por lo que lo hace por medio de la presente demanda, manifestando su total oposición al referido acuerdo.

QUINTO.– Mi patrocinado se encuentra al corriente de pago de las deudas vencidas con la Comunidad de Propietarios, lo que se acredita a través de los recibos que se adjuntan como documento n.º [Nº].

FUNDAMENTOS DE DERECHO

I.– JURISDICCIÓN Y COMPETENCIA

A) JURISDICCIÓN.

POTESTAD JURISDICCIONAL. La potestad jurisdiccional se ejerce por los Jueces y Tribunales determinados por las leyes, según las normas de competencia y procedimiento que las mismas establezcan (art. 117.3 CE).

JURISDICCIÓN CIVIL. Los Tribunales del orden civil conocerán, además de las materias que les son propias, de todas aquellas que no estén atribuidas a otro orden jurisdiccional (art. 9.2 LOPJ).

ÁMBITO DE LA JURISDICCIÓN. La extensión y límites de la jurisdicción de los Tribunales civiles españoles se determinará por lo dispuesto en la LOPJ y en los tratados y convenios internacionales en los que España sea parte (art. 36 LEC), no existiendo en el presente asunto elemento ninguno de extranjería.

B) COMPETENCIA

PREDETERMINACIÓN LEGAL DE LA COMPETENCIA. Para que los Tribunales civiles tengan competencia en cada caso se requiere que el conocimiento del pleito les esté atribuido por normas con rango de ley y anteriores a la incoación de las actuaciones de que se trate (art. 44 LEC).

COMPETENCIA OBJETIVA. Corresponde a las secciones civiles de los tribunales de instancia, puesto que no viene atribuida por ley esta causa civil a otros tribunales (arts. 85.1 LOPJ y 45 LEC).

COMPETENCIA TERRITORIAL. Resulta competente el Tribunal al que me honro en dirigirme por ser del partido del lugar donde está sita la finca, conforme al mandato del art. 52.1.8.º LEC, que es fuero necesario (art. 54.1 LEC), controlable de oficio, a instancia del Letrado de la Administración de Justicia, en trámite de admisión de la demanda (art. 58 LEC).

II.– PROCEDIMIENTO

De acuerdo con lo previsto en el art. 18.1 LPH y conforme al número 8.º del art. 249.1 LEC, el procedimiento ajustado a Derecho, por tratarse de acción que otorga a los propietarios la Ley de Propiedad Horizontal, será el del juicio declarativo ordinario regulado en los arts. 399 a 436 de la misma ley.

III.– LEGITIMACIÓN ACTIVA Y PASIVA

La legitimación activa corresponde a mi mandante conforme a lo previsto en el art. 18.2 LPH, en cuanto reconoce legitimación al propietario para impugnar los acuerdos contrarios a las leyes cuando hubiera estado ausente por cualquier causa.

La legitimación pasiva corresponde a la Comunidad por ser la que tomó el acuerdo que se impugna, siendo demandada en la persona de su Presidente/a, a tenor de lo dispuesto en el art. 13.3 LPH, en cuanto señala que el órgano de representación de la Comunidad, en juicio y fuera del mismo, en los asuntos que afecten a la Comunidad, lo es el Presidente elegido de entre los propietarios.

IV.– CAPACIDAD Y REPRESENTACIÓN

Mi mandante es persona física, mayor de edad, en pleno ejercicio de sus derechos civiles, que tiene capacidad para ser parte y para comparecer, por sí, en su propio nombre y derecho, en este juicio (arts. 6.1.1.º y 7.1 LEC).

La Comunidad carece de personalidad jurídica, pero tiene capacidad para ser parte y capacidad procesal por específica disposición legal, a través de sus órganos (arts. 6.1.5.º y 7.6 LEC).

V.– POSTULACIÓN Y DEFENSA

El actor ha otorgado poder notarial al Procurador/a de los Tribunales que encabeza este escrito, habilitado en el partido del Tribunal, cuya copia auténtica se ha aportado, general para pleitos (art. 25 LEC), siendo redactada y firmada la demanda por el/la abogado/a ejerciente colegiado/a que dirige el asunto y se identifica en el encabezamiento, según resulta preceptivo conforme a los arts. 23 y 31 LEC.

VI.– CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD

La presente demanda no está sujeta al previo intento de resolución de controversias en vía no jurisdiccional, por tratarse de la impugnación judicial de un acuerdo de la comunidad de propietarios, habiendo determinado la doctrina de apelación que la propia junta equivale a una actividad negociadora y no son exigibles los medios adecuados de solución de controversias de la LO 1/2025 para la Ley de Propiedad Horizontal.

VII.– FUNDAMENTOS MATERIALES

La presente acción tiene su fundamento en el art. 16.2 LPH, que exige la previa convocatoria a la Junta de propietarios, con entrega de citación escrita en el domicilio designado por cada propietario y, en su defecto, en el piso a él perteneciente.

Asimismo, los acuerdos de las Juntas serán impugnables, según lo dispuesto en el apartado primero, letra a), del art. 18 LPH, cuando sean contrarios a la Ley, y lo son aquellos que se adopten para modificar el título constitutivo sin unanimidad.

El acuerdo tomado por la Comunidad en ausencia de esta parte va contra la regla de unanimidad de los acuerdos que representan alteración del título constitutivo o de los estatutos (art. 17.6 LPH), dado que no supone el establecimiento de un servicio común nuevo, ni los que disfrutan las parcelas n.º [Nº DE PARCELAS] de los sótanos de garaje padecen discapacidad de ningún tipo, sino que, para el servicio ya existente de elevador-descensor de automóviles, se desea modificar un elemento común (paramento de tabicación de los sótanos en que se encaja dicho aparato), al solo fin de dar acceso exclusivo a sus parcelas a dos copropietarios que, al parecer, cuentan con vehículos de motor de dimensiones tales que no pueden acceder por el vial común que utilizan todos los usuarios del garaje, cosa que obviamente no es imputable a nadie más que al titular del vehículo.

VIII.– CUANTÍA DE LA DEMANDA.

En cumplimiento del art. 253.1 LEC, puesto que la cuantía litigiosa resulta indirectamente determinable, se hace constar que la cuantía de esta demanda es la de [IMPORTE] euros, ya que se pretende una prestación de no hacer, no personalísima, cuyo costo de reposición es el indicado, y a tal acreditación se aporta presupuesto de «[DENOMINACIÓN SOCIAL DE LA CONSTRUCTORA]» como documento n.º [Nº].

IX.– COSTAS.

Conforme al art. 394 LEC, las costas han de imponerse a la parte demandada, por el principio objetivo del vencimiento.

Por lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito, con los documentos y copias que le acompañan, mande formar autos en los que se me tenga por comparecido/a y parte en nombre de quien comparezco y, teniendo por deducida demanda de juicio ordinario, la admita a trámite y confiera traslado de la misma al demandado, con entrega de las copias presentadas, emplazándole para que comparezca en autos y la conteste, siguiendo el pleito su curso con celebración de las audiencias previstas, y en definitiva se llegue a dictar sentencia por la que, estimando íntegramente la demanda, se declare la nulidad del acuerdo tomado en la Junta de Propietarios de la Comunidad demandada de fecha [FECHA], señalado en su apartado [Nº DE APARTADO], cuyo contenido se consigna en el hecho tercero, dejándolo sin efecto alguno, con expresa imposición de costas procesales a la parte demandada, y demás que proceda.

Por ser de Justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Abogado/a: [FIRMA] Firma del Procurador/a: [FIRMA]

NORMATIVA APLICABLE

— Artículos 13 y siguientes de la Ley 49/1960, de 21 de julio, sobre propiedad horizontal.

— Ley 1/2000, de 7 de enero, de Enjuiciamiento Civil.

JURISPRUDENCIA DE INTERÉS

— Sentencia del Tribunal Supremo de 29 de octubre de 2010, rec. 1077/2006:

«(...) En estos momentos, la jurisprudencia de esta Sala, conforme recuerda la Sentencia de 18 de marzo de 2010, rec. 1403/2006, ha fijado una interpretación más ajustada a las previsiones legislativas del artículo 16 de la Ley de Propiedad Horizontal, de tal forma que se distingue entre "aquéllas ilegalidades que por afectar estrictamente al régimen de propiedad horizontal se encuentran sometidas a la normativa del art. 16.4 LPH y a las que, por ende, es aplicable la sanción por el transcurso del plazo de caducidad, de aquellas otras infracciones que por atentar a la esencia de la institución, contravenir disposiciones imperativas o prohibitivas sin estar legalmente previsto un efecto distinto, o conculcar las reglas de la moral o el orden público, o implicar fraude de ley, determinan la nulidad radical e insubsanable" (SSTS de 10 de marzo de 1997; 5 de mayo de 2000; 14 de febrero de 2002, rec. 2984/1996; 10 de noviembre de 2004, rec. 3047/1998; 30 de diciembre de 2005, rec. 1786/1999, y 20 de noviembre de 2006, rec. 4775/1999, entre otras, en recursos núm. 1183/1993, 2246/1995, 2984/1996, 3047/1998, 1786/1999 y 4775/1999, respectivamente).

La STS de 17 de diciembre de 2009, rec. 1550/2005, a su vez, dispone lo siguiente: "Los acuerdos adoptados por la Comunidad de Propietarios sí debe considerarse que afectan y vinculan a los demandados, porque pese a que se adopta un acuerdo de modificación del sistema establecido en el Título Constitutivo para concretar la contribución de cada propietario al coste de instalación del ascensor por mayoría cualificada, cuando dicha decisión hubiera requerido unanimidad, lo cierto es que la jurisprudencia del Tribunal Supremo viene señalando como doctrina más asentada que los acuerdos así adoptados serían meramente anulables, y por tanto convalidados por su ratificación ulterior y por la falta de impugnación de los mismos en el plazo legalmente determinado, propugnando dicha doctrina jurisprudencial (SSTS de 10 de marzo de 1997, rec. 1409/1993; 7 de junio de 1997, rec. 1865/1993; 9 de diciembre de 1997, rec. 3105/1993; 5 de mayo de 2000, rec. 5183/1994, y 7 de marzo de 2002, rec. 3142/1996, entre otras), un criterio flexible en armonía con las directrices de la Ley de Propiedad Horizontal, entre ellas el logro de una convivencia normal y pacífica presidida por la idea de justicia y la atención a las necesidades de la colectividad". En idéntico sentido se manifiestan las SSTS de 25 de enero de 2005, rec. 3501/1998; 28 de febrero de 2005, rec. 3819/1998; 30 de diciembre de 2005, rec. 1786/1999, y 18 de abril de 2007, rec. 1317/2000.

Esta última, en su fundamento de derecho tercero, párrafo segundo, dice lo siguiente:

"La doctrina jurisprudencial que, con alguna excepción, cita la sentencia de la Audiencia (SSTS de 24 de septiembre de 1991, 26 de junio de 1993, rec. 2468/1990, 7 de junio de 1997, rec. 1865/1993, y 26 de junio de 1998, rec. 1596/1994) sobre la distinción entre nulidad radical y anulabilidad en materia de propiedad horizontal es, como recuerda la sentencia de 5 de mayo de 2000, la que se viene manteniendo como más acertada por la moderna doctrina de esta Sala. Más recientemente las sentencias de 7 de marzo de 2002, 25 de enero de 2005 y 30 de diciembre de 2005 explican las diferencias entre nulidad y anulabilidad, sujeta a caducidad, y recuerdan que la jurisprudencia posterior a las sentencias que se invocan en el recurso se definió claramente por considerar meramente anulables los acuerdos que entrañasen infracción de algún precepto de la Ley de Propiedad Horizontal o de los Estatutos de la respectiva Comunidad, quedando reservada la más grave calificación de nulidad radical o absoluta solamente para aquellos otros acuerdos que, por infringir cualquier otra Ley imperativa o prohibitiva que no tenga establecido un efecto distinto para el caso de contravención, o por ser contrarios a la moral o el orden público, o por implicar un fraude de Ley, hayan de ser conceptuados nulos de pleno derecho, conforme al párrafo 3.º del artículo 6 del Código Civil, y por tanto insubsanables por el transcurso del tiempo (...). Es razón por la que no es posible reprochar a la sentencia recurrida la infracción denunciada en el recurso, puesto que se sustenta en una línea jurisprudencial ya superada. Antes al contrario, el criterio sostenido no sólo es el correcto, sino el mismo que se mantiene tras la redacción dada por Ley 8/1999, de 6 de abril, en el sentido de someter la impugnación de acuerdos contrarios a la Ley o a los Estatutos de la Comunidad de Propietarios a las reglas contenidas en la Ley de Propiedad Horizontal, con un plazo más amplio y el añadido de nuevos supuestos de impugnación y el abandono de la exigencia de la unanimidad para determinados acuerdos».

— Sentencia del Tribunal Supremo de 22 de diciembre de 2010, rec. 1574/2006:

«(...) la doctrina de esta Sala, que ya ha tenido oportunidad de pronunciarse respecto a la compatibilidad del derecho de servidumbre con la ocupación de una parte de un bien privativo a fin de instalar un ascensor. La STS de 18 de diciembre de 2008, rec. 880/2004, califica como servidumbre esta ocupación y declara: "Por lo que hace mención a la constitución de una nueva servidumbre, a tenor del artículo 17 será suficiente la simple mayoría para la supresión de las 'barreras arquitectónicas' que dificulten el acceso y la movilidad de las personas con discapacidad; esta regla permite a la Comunidad imponer esa servidumbre para la creación de servicios de interés general y cuando el acuerdo de la Junta reúna los presupuestos legales, con el oportuno resarcimiento de daños y perjuicios."

En definitiva, la instalación de un ascensor en una comunidad de vecinos que carece de este servicio, considerado como de interés general, permite la constitución de una servidumbre para tal fin, incluso cuando suponga la ocupación de parte de un espacio privativo, siempre que concurran las mayorías exigidas legalmente para la adopción de tal acuerdo. No obstante ser ésta la afirmación que defiende el recurrente, y concurriendo aparentemente estos presupuestos en el supuesto que es examinado, el motivo no puede prosperar. La ocupación de un espacio privativo, en el que difícilmente concurrirá el consentimiento del vecino afectado, no puede suponer una privación del derecho de propiedad al extremo de suponer una pérdida de habitabilidad y funcionalidad de su espacio privativo. En el presente caso la Audiencia Provincial ha declarado, tras examinar las pruebas practicadas, que la constitución de la servidumbre en los términos en que fue aprobada en la Junta de Comunidad "supone la total privación de dicho espacio, con una repercusión total en la actual configuración del local, menoscabando, incluso, las expectativas de aprovechamiento económico del local, ya que no solo se le privaría de un importante volumen, sino que precisamente por dicha circunstancia las posibilidades de organización del espacio interior del local se verían seriamente afectadas, con merma evidente de sus posibilidades de explotación". Tal conclusión fáctica no puede ser rebatida a través del recurso de casación, como así pretende el recurrente, que expresamente contradice, al argumentar que son contrarias, de modo patente y manifiesto, a las pruebas practicadas, especialmente a las pruebas periciales que han sido presentadas. Su contrariedad con el resultado probatorio únicamente la pudo hacer valer a través del recurso extraordinario por infracción procesal, sin que sea admisible su impugnación mediante el recurso de casación, que únicamente puede fundarse en la vulneración de normas de naturaleza sustantiva pero sin alterar los elementos de hecho que han sido fijados por la Audiencia Provincial, que desde la óptica del recurso de casación resultan inatacables».
