---
name: demanda-declarar-ilegales-cuotas-participacion-civ-0628
description: "Demanda para declarar ilegales las cuotas de participación en elementos comunes y redistribuirlas. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda para declarar ilegales las cuotas de participación en elementos comunes y redistribuirlas

> Formulario **CIV-0628** del plugin **Comunidades de propietarios** (`formularios-comunidades-de-propietarios`) · Civil › Propiedad horizontal · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio ordinario de un propietario contra el resto de copropietarios de una comunidad en régimen de propiedad horizontal para que se declare la ilegalidad de las cuotas de participación en los elementos comunes (porque no se corresponden con el aprovechamiento real que cada propietario hace de ellos) y se redistribuyan. Se usa cuando la Junta ha rechazado la modificación, que exige unanimidad (art. 17.6 LPH).

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda para declarar ilegales las cuotas de participación en elementos comunes y redistribuirlas» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda para declarar ilegales las cuotas de participación en elementos comunes y redistribuirlas” para mi caso». También puedes invocarla directamente con `/formularios-comunidades-de-propietarios:demanda-declarar-ilegales-cuotas-participacion-civ-0628`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-comunidades-de-propietarios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Comunidades de propietarios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (17 veces)
- [ ] PORCENTAJE (12 veces)
- [ ] AÑO (5 veces)
- [ ] IMPORTE (5 veces)
- [ ] FECHA (4 veces)
- [ ] IDENTIFICACIÓN (4 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] DENOMINACIÓN O DOMICILIO DE LA COMUNIDAD (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] ARCHIVO O PROTOCOLO
- [ ] CARRETERA
- [ ] DESCRIBIR LA VIVIENDA DE MAYOR SUPERFICIE
- [ ] DESCRIBIR LOS ELEMENTOS COMUNES QUE NO USA
- [ ] DÍA
- [ ] FECHAS
- [ ] IDENTIFICACIÓN DE LA VIVIENDA
- [ ] IDENTIFICACIÓN DE LAS VIVIENDAS DE CADA DEMANDADO
- [ ] IDENTIFICACIÓN DEL PROPIETARIO DE MAYOR SUPERFICIE
- [ ] MES
- [ ] NOMBRE Y APELLIDOS DEL ABOGADO/A
- [ ] NOMBRE Y APELLIDOS DEL DEMANDADO 1
- [ ] NOMBRE Y APELLIDOS DEL DEMANDADO 2
- [ ] NOMBRE Y APELLIDOS DEL DEMANDADO 3
- [ ] NOMBRE Y APELLIDOS DEL DEMANDANTE
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] REPETIR PARA CADA VIVIENDA DE LA COMUNIDAD
- [ ] REPETIR PARA TODOS LOS DEMÁS COPROPIETARIOS
- [ ] SEDE

## Normas que cita el formulario

- art. 9.2 LOPJ
- art. 36 LEC
- art. 44 LEC
- art. 85.1 LOPJ
- art. 45 LEC
- art. 52.1.8.º LEC
- art. 54.1 LEC
- art. 58 LEC
- art. 17.6 LPH
- art. 18.2 LPH
- art. 253.3 LEC
- art. 5 Ley Orgánica 1/2025
- art. 14 LPH
- art. 5 LPH
- art. 394 LEC
- art. 265 LEC

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

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales y de D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDANTE], como se acredita debidamente con escritura de poder que se acompaña, bajo la dirección letrada del Abogado/a D./Dña. [NOMBRE Y APELLIDOS DEL ABOGADO/A], comparece ante el Tribunal y, como en derecho mejor proceda, DICE:

Que por medio del presente escrito formulo demanda de JUICIO ORDINARIO frente a D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDADO 1], D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDADO 2], D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDADO 3] [REPETIR PARA TODOS LOS DEMÁS COPROPIETARIOS], residentes en la Comunidad de Propietarios [DENOMINACIÓN O DOMICILIO DE LA COMUNIDAD], sita en [DOMICILIO], [LOCALIDAD], en las viviendas [IDENTIFICACIÓN DE LAS VIVIENDAS DE CADA DEMANDADO], respectivamente; en solicitud de declaración de ilegalidad de las cuotas de participación de los propietarios en los elementos comunes de la referida comunidad de propiedad horizontal y la correlativa modificación de las cuotas de participación de todos ellos y de mi mandante.

La demanda se basa en los siguientes

HECHOS

PRIMERO.– Mi mandante es propietario/a de la vivienda [IDENTIFICACIÓN DE LA VIVIENDA], situada en la comunidad de propietarios demandada, según se acredita con el título que se acompaña como documento n.º [Nº]. Tal inmueble fue adquirido por contrato de compraventa firmado el [FECHA] y elevado a escritura pública el [FECHA]. Se adjuntan los contratos como documentos n.º [Nº] y [Nº].

SEGUNDO.– El título constitutivo de la comunidad de propietarios, otorgado con anterioridad a la adquisición de la vivienda por mi mandante, fijó una cuota de participación del inmueble en relación con los elementos comunes del [PORCENTAJE] %, que es idéntica para [Nº] de las [Nº] viviendas que conforman aquella, ostentando la vivienda [IDENTIFICACIÓN] un [PORCENTAJE] %. El reparto de cuotas se hace, exclusivamente, en función de la superficie de cada una de las viviendas, tal y como se observa en el título constitutivo, cuya copia se acompaña como documento n.º [Nº].

TERCERO.– La vivienda de mi mandante está situada en [DESCRIBIR LA SITUACIÓN: p. ej., la parte sur de la urbanización, con acceso directo a la carretera [CARRETERA], al encontrarse a la misma altura]. En cambio, el resto de las viviendas están situadas [DESCRIBIR: p. ej., sobre una colina, en un nivel superior al de la carretera, con un desnivel de [Nº] metros]. Se aporta a la demanda plano de la urbanización como documento n.º [Nº], en el que se pueden observar tales extremos.

CUARTO.– De esta forma, y con objeto de [DESCRIBIR LA OBRA O SERVICIO COMÚN: p. ej., comunicar el grueso de la urbanización con la carretera, así como acometer la toma de agua y electricidad], fue preciso realizar una compleja obra, que necesita constantes reparaciones ante la dificultad de salvar el importante desnivel referido. Los gastos, tanto de la obra inicial, repercutida en cuotas mensuales a los copropietarios, como de las reparaciones periódicas, son sustanciosos. Se adjunta bloque documental n.º [Nº] en el que se puede constatar unos gastos iniciales de [IMPORTE] euros y unos gastos periódicos en ascenso de [IMPORTE] euros en [AÑO], de [IMPORTE] euros en [AÑO] y de [IMPORTE] euros en [AÑO]. Mi mandante abonó el importe de [IMPORTE] euros que le correspondían por el ejercicio de [AÑO], con arreglo a la cuota de participación que aquí se combate, tal y como se aprecia en el extracto bancario que se aporta como documento n.º [Nº], haciendo constar su disconformidad con la misma mediante burofax enviado al presidente de la comunidad de propietarios, el cual se acompaña como documento n.º [Nº].

QUINTO.– Mi mandante planteó en la junta [ELEGIR: ordinaria / extraordinaria] celebrada el [FECHA] la petición de modificación de su cuota de participación, al no hacer uso [DESCRIBIR LOS ELEMENTOS COMUNES QUE NO USA], siendo rechazada la misma al votar en contra todos los propietarios presentes en la junta, con excepción de la propia actora. Se acompaña, como documento n.º [Nº], copia del acta de la junta.

SEXTO.– La parte actora manifiesta que, previamente a la presentación de la presente demanda, se han llevado a cabo negociaciones con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria, incluyéndose entre las acciones realizadas el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución.

Finalmente, mi representado envió un requerimiento fehaciente a los demandados con fecha [FECHA], fijando un plazo de 30 días naturales para llegar a un acuerdo amistoso, a través del abogado que firma este escrito, el cual fue contestado por los demandados por el mismo medio, [ELEGIR: rechazando el acuerdo / habiendo sido solo posible un acuerdo parcial], viéndonos en la necesidad de acudir a la presente vía judicial respecto a los extremos de la controversia en los que se mantiene la discrepancia.

Acompaño como documento n.º [Nº] el requerimiento efectuado y como documento n.º [Nº] la contestación de los demandados.

A los anteriores hechos son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

I.– JURISDICCIÓN Y COMPETENCIA

A) JURISDICCIÓN

Potestad jurisdiccional. La potestad jurisdiccional se ejerce por los Jueces y Tribunales determinados por las leyes, según las normas de competencia y procedimiento que las mismas establezcan (art. 117.3 CE).

Jurisdicción civil. Los Tribunales del orden civil conocerán, además de las materias que les son propias, de todas aquellas que no estén atribuidas a otro orden jurisdiccional (art. 9.2 LOPJ).

Ámbito de la jurisdicción. La extensión y límites de la jurisdicción de los Tribunales civiles españoles se determinará por lo dispuesto en la LOPJ y en los tratados y convenios internacionales en los que España sea parte (art. 36 LEC), no existiendo en el presente asunto elemento alguno de extranjería.

B) COMPETENCIA

Predeterminación legal de la competencia. Para que los Tribunales civiles tengan competencia en cada caso se requiere que el conocimiento del pleito les esté atribuido por normas con rango de ley y anteriores a la incoación de las actuaciones de que se trate (art. 44 LEC).

Competencia objetiva. Corresponde a las secciones civiles de los tribunales de instancia, puesto que no viene atribuida por ley esta causa civil a otros Jueces o Tribunales (art. 85.1 LOPJ y art. 45 LEC).

Competencia territorial. Resulta competente el Tribunal a que me honro en dirigirme por ser del partido del lugar donde está sita la finca, conforme al mandato del art. 52.1.8.º LEC, que es fuero necesario (art. 54.1 LEC), controlable de oficio en trámite de admisión de la demanda (art. 58 LEC).

II.– PROCEDIMIENTO

Procede sustanciar el proceso por los trámites del juicio ordinario, conforme a los arts. 248.3 y 249.1.8.º LEC, por tratarse de acción que permite a mi mandante la Ley de Propiedad Horizontal (en adelante, LPH).

III.– LEGITIMACIÓN ACTIVA Y PASIVA

La legitimación activa corresponde a mi mandante, quien ha intentado tal alteración en junta de propietarios y, al no obtener la necesaria unanimidad exigida por el art. 17.6 LPH, acude a la vía judicial con arreglo a lo dispuesto en el art. 5 del mismo texto legal. En este sentido, las sentencias del Tribunal Supremo de 5 de julio de 2005 (Rec. 489/1999) y de 29 de enero de 2007 (Rec. 347/2000) reconocen esta legitimación, una vez se plantea y se deniega la cuestión en junta de propietarios. Aunque no se exija para esta acción, ni para la concreta impugnación de acuerdos de juntas en que se fijen o modifiquen las cuotas de participación en elementos comunes, conforme al art. 18.2 LPH, se hace constar que mi mandante se encuentra al corriente del pago de las cuotas de la comunidad, habiendo realizado el último pago con expresa protesta en relación con el porcentaje que aquí se discute.

La legitimación pasiva corresponde a todos los demás copropietarios, dado que la pretendida reducción de la cuota de mi mandante afectará a todos ellos automáticamente, al suponer un incremento correlativo de la de cada uno. Así, si se precisa la unanimidad de todos los propietarios para lograr un acuerdo comunitario que modifique las cuotas, atendiendo a la especial afectación de tal cuestión en la vida comunitaria, es lógico colegir que todos ellos tienen que ser demandados a los efectos de no ocasionarles indefensión, dado que su cuota se verá afectada por las resultas del litigio, tal y como razonó la sentencia de la Audiencia Provincial de Alicante de 9 de septiembre de 2005 (Rec. 862/2004). Y ello sin que sea preciso demandar a la comunidad de propietarios como tal.

IV.– CUANTÍA DE LA DEMANDA

La cuantía de la demanda, a los efectos de lo dispuesto en el artículo 253.3 LEC, es INDETERMINADA, al pretenderse una corrección de las cuotas de participación en elementos comunes que no tiene una traducción económica concreta.

De ahí procede la preceptividad de la representación por Procurador/a y la defensa por abogado, conforme a los arts. 23.1 y 31.1 LEC.

V.– CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4.º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

VI.– FUNDAMENTOS DE DERECHO MATERIALES O SOBRE EL FONDO DEL ASUNTO

1) De la posibilidad de modificar las cuotas de participación.

La fijación de la cuota de participación de cada uno de los propietarios en los elementos comunes de la propiedad horizontal es una de las cuestiones claves en la vida de la comunidad, dado que viene a reflejar el concreto aprovechamiento que cada particular hace del elemento común y, por ende, su correspondiente obligación de contribuir a su mantenimiento. Extremos que pueden venir fijados en el título constitutivo inicial, pero que deben ser aceptados por los distintos propietarios, siendo susceptibles de ser modificados por la voluntad de los mismos. Es decir, es una cuestión clave en el marco de la convivencia de una comunidad de propiedad horizontal, que se encuentra sometida a la voluntad de la junta de propietarios, con arreglo al art. 14 LPH, siendo ésta el órgano esencial en la especial forma de propiedad que nos ocupa.

Sometimiento, de esta forma, a la voluntad comunitaria, que no impide que dicha fijación de cuotas pueda ser revisada, bien por los propios propietarios (con ese requisito extremo de unanimidad del art. 17.6 LPH) o, de manera subsidiaria, por el órgano judicial correspondiente, a petición de uno o varios propietarios. Al respecto, una pacífica doctrina jurisprudencial, de la que son ejemplos, entre otras, las sentencias del Tribunal Supremo de 2 de marzo de 1989, de 10 de diciembre de 1990, de 2 de febrero de 1991, de 3 de marzo de 1994 y de 6 de mayo de 1997.

2) De la ilegalidad de las cuotas actuales.

Pues bien, en el presente caso, con anterioridad a la llegada de mi mandante a la comunidad se fijaron unas cuotas de participación, invariadas hasta la fecha, que no guardan una justa correlación con el aprovechamiento que cada vivienda hace de los elementos comunes, habiéndose concretado aquellas exclusivamente sobre la base de la superficie de cada vivienda, prescindiendo de manera absoluta de la situación de cada inmueble en la comunidad de propiedad horizontal. De esta forma, mi mandante contribuye a los gastos comunes en un [PORCENTAJE] % junto con otras [Nº] viviendas de igual superficie, y [DESCRIBIR LA VIVIENDA DE MAYOR SUPERFICIE], con el doble de extensión, lo hace en un [PORCENTAJE] %.

Recuérdese, en este punto, que el art. 5, párrafo segundo, LPH remite para la fijación de tales cuotas a distintos criterios: la superficie útil de cada piso o local en relación con el total del inmueble, su emplazamiento interior o exterior, su situación y el uso que se presuma racionalmente que va a efectuarse de los servicios o elementos comunes. Criterios que la doctrina jurisprudencial define como «numerus apertus» (sentencia de la Audiencia Provincial de Álava, Sección 1.ª, n.º 410/2007, de 28 de diciembre de 2007, Rec. 371/2007), entendiéndose enumerados los más habituales en este ámbito, lo que no implica que no se pueda acudir a otros, en relación con las características especiales de cada comunidad de propiedad horizontal en concreto.

A la hora de fijar las cuotas de esta comunidad, como se ha dicho, se atendió de manera exclusiva a la superficie de cada vivienda, sin recurrir a cualquier otro criterio, cuando, conforme al plano aportado, la comunidad tiene unas características especiales que conforman una distinción absoluta entre la vivienda de mi mandante y las del resto de los aquí codemandados. Así, la vivienda de la parte actora [DESCRIBIR SU SITUACIÓN: p. ej., se encuentra a escasos metros de la carretera general, sin que precise transitar por la vía de acceso a la colina para llegar al inmueble]. En este punto, [DESCRIBIR LOS ELEMENTOS COMUNES QUE NO USA O QUE NO EXISTEN: p. ej., no existe ningún elemento común de ocio o de reunión en la urbanización]. Asimismo, mi mandante tiene en su inmueble acceso a la red pública de aguas y a la electricidad, pero las toma directamente de la red general, sin que aproveche la canalización especial que se hizo para salvar el importante desnivel referido, que tantas reparaciones exige.

En consecuencia, sin participar en el uso de esos elementos, que conllevan aproximadamente un [PORCENTAJE] % de los gastos comunes, mi mandante participa en los mismos en idéntica proporción a otros [Nº] propietarios, al tener las viviendas la misma superficie, y en la mitad de lo que lo hace [IDENTIFICACIÓN DEL PROPIETARIO DE MAYOR SUPERFICIE], quien tiene una vivienda el doble de grande. Se solicita, por ello, la declaración de ilegalidad de las cuotas, al no corresponderse con el aprovechamiento que, en concreto, mi mandante hace de los elementos comunes, en contraposición con el resto de comuneros.

3) De la correcta fijación de las mismas.

La declaración de ilegalidad deberá venir acompañada de una redistribución de las cuotas conforme a un criterio más justo que adecue aquellas al concreto aprovechamiento de cada propietario, lógica pretendida por el legislador en el mencionado art. 5 LPH. Extremo que se pretendió negociar por mi mandante en la junta reflejada en los antecedentes, habiéndose negado en redondo todos los codemandados a siquiera iniciar una serie de conversaciones al respecto, de forma que se pudieran pactar unos porcentajes distintos a los que aquí se impugnan.

Por ello, se propone una modificación proporcional al aprovechamiento real en cada caso. Si mi mandante aprovecha un [PORCENTAJE] % de los gastos comunes (el [PORCENTAJE] % de ellos se dirige a mantener los elementos comunes que realmente no usa), deberá contribuir en esa proporción frente al resto de comuneros. Y así, si hay otros [Nº] propietarios que aprovechan todos los elementos comunes, deberían contribuir todos ellos en un [PORCENTAJE] %, salvo el propietario de la vivienda [IDENTIFICACIÓN], que lo haría en un [PORCENTAJE] %, quedando un porcentaje a la parte actora de un [PORCENTAJE] %, proporcional a los elementos comunes de los que disfruta.

En definitiva, se solicita, como pronunciamiento adicional, que se modifiquen las cuotas en los porcentajes expuestos.

VII.– COSTAS

Conforme al art. 394 LEC, todas las costas han de imponerse a los demandados, en tanto que se opongan y sean vencidos.

Por lo expuesto,

SUPLICO AL TRIBUNAL

Que, teniendo por presentado este escrito, se admita la demanda frente a los demandados reseñados en el encabezamiento del presente escrito y, seguido el trámite de ley, dicte en su día sentencia por la cual:

1.– Se declare la ilegalidad de las actuales cuotas de participación de los propietarios en los elementos comunes de la Comunidad de Propietarios [DENOMINACIÓN O DOMICILIO DE LA COMUNIDAD], sita en [DOMICILIO], [LOCALIDAD].

2.– Se proceda a modificar dichas cuotas de participación, quedando definitivamente fijadas como a continuación se describe:

— Vivienda [IDENTIFICACIÓN], [PORCENTAJE] %.

— Vivienda [IDENTIFICACIÓN], [PORCENTAJE] %.

[REPETIR PARA CADA VIVIENDA DE LA COMUNIDAD]

3.– Se impongan las costas a los demandados.

OTROSÍ DIGO: Que esta parte señala los archivos o protocolos de [ARCHIVO O PROTOCOLO] (referentes a aquellos documentos que no han podido ser acompañados con la demanda), sin perjuicio de otros medios de prueba que sean procedentes según la contestación de los demandados, conforme previenen los apartados 2 y 3 del artículo 265 de la LEC.

SUPLICO AL TRIBUNAL se tenga por hecha la anterior manifestación a los efectos procesales oportunos.

SEGUNDO OTROSÍ DIGO: Que, siendo el poder general para pleitos y necesitándolo para otros usos, SUPLICO AL TRIBUNAL que, una vez tomada nota en los autos, sea desglosado y devuelto a esta parte.

Por ser de justicia, que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Abogado/a Firma del Procurador/a

NOTAS DE AYUDA

(1) En la práctica judicial, para redistribuir las cuotas hay que demandar a todos los propietarios de la comunidad, y no a ésta en sí. Esto es un problema, dado que, si hay muchos comuneros y todos vienen con su abogado y procurador, hay un riesgo de costas grande. Pero la jurisprudencia es muy clara y tiene lógica además: si se rebaja la cuota propia, se aumentan las de los demás.

(2) Se exige también plantear la cuestión en junta de propietarios, para permitir que los vecinos la acepten por unanimidad, entendiendo el recurso judicial como subsidiario, cuando se rechace.

(3) El formulario recoge un caso extremo, que habrá que adecuar en cada caso concreto con las especiales circunstancias de esa desigualdad en los aprovechamientos, interpretando con lógica el art. 5 LPH, para proponer la distribución de cuotas que se desee. Aquí incluso se podrían solicitar pronunciamientos subsidiarios, que deberá decidir el usuario.
