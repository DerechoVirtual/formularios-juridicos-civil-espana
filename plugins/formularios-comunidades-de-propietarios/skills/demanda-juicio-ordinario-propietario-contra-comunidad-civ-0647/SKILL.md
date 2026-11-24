---
name: demanda-juicio-ordinario-propietario-contra-comunidad-civ-0647
description: "Demanda de juicio ordinario de un propietario contra la comunidad por daños de elementos comunes. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio ordinario de un propietario contra la comunidad por daños de elementos comunes

> Formulario **CIV-0647** del plugin **Comunidades de propietarios** (`formularios-comunidades-de-propietarios`) · Civil › Propiedad horizontal · normativa revisada el 24-11-2026.

## Qué es

Escrito de demanda de juicio ordinario interpuesta por un propietario contra la Comunidad de Propietarios en reclamación de indemnización por los daños causados por las filtraciones de agua producidas en la vivienda del actor en régimen de propiedad horizontal.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio ordinario de un propietario contra la comunidad por daños de elementos comunes» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio ordinario de un propietario contra la comunidad por daños de elementos comunes” para mi caso». También puedes invocarla directamente con `/formularios-comunidades-de-propietarios:demanda-juicio-ordinario-propietario-contra-comunidad-civ-0647`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-comunidades-de-propietarios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Comunidades de propietarios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº DE DOCUMENTO (8 veces)
- [ ] FECHA (4 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] IMPORTE (2 veces)
- [ ] NOMBRE DE LA COMUNIDAD (2 veces)
- [ ] FECHAS
- [ ] IMPORTE EN LETRA
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] Nº
- [ ] NÚMERO
- [ ] PISO
- [ ] SEDE

## Normas que cita el formulario

- art. 9.2 LOPJ
- art. 36 LEC
- art. 44 LEC
- art. 85.1 LOPJ
- art. 52.1.8.º LEC
- art. 54.1 LEC
- art. 58 LEC
- art. 73.1 LEC
- art. 13.3 Ley 49/1960
- art. 253.1 LEC
- art. 252 LEC
- art. 5 Ley Orgánica 1/2025
- art. 10.1.a LPH
- art. 1.902 CC
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

### Avisos de actualización (1) — se aplican en el texto, nunca se copian en el documento

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Notas al pie del formulario original:
(1) Si la reparación se ha realizado y se reclama sólo el pago de los daños ocasionados, deberá acudirse al juicio declarativo verbal por mandato del art. 250.1.15º LEC.

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

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a. de los Tribunales y de D./Dña. [NOMBRE Y APELLIDOS], y a cuya justificación aporto escritura de poder inscrito en el Registro Electrónico de Apoderamientos Judiciales con el nº [NÚMERO] y que se puede acreditar mediante consulta automatizada orientada al dato, por parte del órgano judicial al cual tengo el honor de dirigirme, acompañándose certificación electrónica del Registro Electrónico de Apoderamientos Judiciales como Documento nº [Nº DE DOCUMENTO] por si no es posible la consulta automatizada, bajo la dirección Letrada del Abogado D./Dña. [NOMBRE Y APELLIDOS], comparezco ante el Tribunal y como en derecho mejor proceda, DIGO:

Que por medio del presente escrito formulo demanda de JUICIO ORDINARIO CONTRA LA COMUNIDAD DE PROPIETARIOS, EN LA PERSONA DE SU REPRESENTANTE LEGAL, A FIN DE QUE SE CONDENE AL DEMANDADO A REPARAR EL TEJADO COMUNITARIO Y A INDEMNIZAR CONEUROS (€ [IMPORTE EN LETRA]) QUE SON LOS DAÑOS CAUSADOS POR LAS FILTRACIONES DE AGUA PRODUCIDAS EN LA VIVIENDA PARTICULAR DE MI PATROCINADO DEL PISO

La demanda se basa en los siguientes:

HECHOS

PRIMERO.- Mi mandante es propietario de la vivienda del piso [PISO], perteneciente a la Comunidad de Propietarios [NOMBRE DE LA COMUNIDAD], sita en [LOCALIDAD], según se acredita con el título que se acompaña como documento número [Nº DE DOCUMENTO].

SEGUNDO.- Con fecha [FECHA], como consecuencia del deficiente estado del tejado comunitario, mi mandante observó en los techos de su vivienda, concretamente en el baño, cocina, pasillo y salón la existencia de grandes manchas de agua que llegaban incluso a las paredes laterales, e incluso siendo perceptible un goteo continuo de agua desde el techo del salón, que afectó a algunos muebles llegando al suelo y estropeando el parquet del mismo.

Se acredita con reportaje fotográfico, acta notarial y presupuesto de reparación de daños (documentos números [Nº DE DOCUMENTO]).

TERCERO.- Nada más advertir la descrita situación mi mandante comunicó a la Comunidad de Propietarios en la persona de su Presidente, a través de correo certificado, los desperfectos sufridos en su domicilio para que procediera a subsanarlos.

Adjunto copia como documento número [Nº DE DOCUMENTO] de la carta notificando los desperfectos al Presidente.

No obstante el daño ya se había producido, el Sr. Presidente de la Comunidad requirió el informe de un experto para verificar el origen de la avería, cuya conclusión es que la cubierta del edificio de la Comunidad de Propietarios demandada se halla en mal estado, con algún hueco abierto en el mismo, por el que entraba agua y que ese agua que entraba en el edificio pasaba a la vivienda de la parte demandante, dentro de la cual resultaron perjudicados bienes de la misma.

Ello consta en el informe técnico que se acompaña como documento número [Nº DE DOCUMENTO].

CUARTO.- Ante dicho informe, D./Dña. [NOMBRE Y APELLIDOS], Presidente de la Comunidad, se comprometió a reparar la avería causante del destrozo, y luego a abonar a mi patrocinado los daños producidos en la vivienda de su propiedad, según el presupuesto de reparación antes aludido, con cargo al presupuesto de la Comunidad.

QUINTO.- Han transcurrido [Nº] meses sin que se haya procedido a la reparación causante de la situación, a la vez que a subsanar los daños ocasionados, siendo infructuosas las gestiones para una solución amistosa.

En fecha [FECHA] fue remitido burofax al objeto de dejar constancia fehaciente de la reclamación formulada a la Comunidad. Se adjunta certificación del Servicio de Correos como documento número [Nº DE DOCUMENTO].

SEXTO.- La parte actora manifiesta que, a mayor abundamiento, previo a la presentación de la presente demanda, se han llevado a cabo negociaciones con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad, y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria; incluyéndose entre las acciones realizadas el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución.

Finalmente, mi representado envió un requerimiento fehaciente al demandado con fecha [FECHA], fijando un plazo de 30 días naturales para llegar a un acuerdo amistoso, a través del abogado que firma este escrito, el cual fue contestado por el demandado por el mismo medio, rechazando el acuerdo/ habiendo sido solo posible un acuerdo parcial, viéndonos en la necesidad de acudir a la presente vía judicial, respecto a los extremos de la controversia en los que se mantiene la discrepancia.

Acompaño como documento nº [Nº DE DOCUMENTO], el requerimiento efectuado y como documento nº [Nº DE DOCUMENTO], la contestación del demandado.

A los anteriores hechos son de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN Y COMPETENCIA

A) JURISDICCIÓN

POTESTAD JURISDICCIONAL. La potestad jurisdiccional se ejerce por los Jueces y Tribunales determinados por las leyes, según las normas de competencia y procedimiento que las mismas establezcan (art. 117.3 CE).

JURISDICCIÓN CIVIL. Los Tribunales del orden civil conocerán, además de las materias que les son propias, de todas aquellas que no estén atribuidas a otro orden jurisdiccional (art. 9.2 LOPJ).

ÁMBITO DE LA JURISDICCIÓN. La extensión y límites de la jurisdicción de los Tribunales civiles españoles se determinará por lo dispuesto en la LOPJ y en los tratados y convenios internacionales en los que España sea parte (art. 36 LEC), no existiendo en el presente asunto elemento ninguno de extranjería.

B) COMPETENCIA

PREDETERMINACIÓN LEGAL DE LA COMPETENCIA. Para que los Tribunales civiles tengan competencia en cada caso se requiere que el conocimiento del pleito les esté atribuido por normas con rango de ley y anteriores a la incoación de las actuaciones de que se trate (art. 44 LEC).

COMPETENCIA OBJETIVA.

Corresponde a las secciones civiles de los Tribunales de Instancia, puesto que no viene atribuida por Ley esta causa civil a otros Tribunales (arts. 85.1 LOPJ y 45 LEC).

COMPETENCIA TERRITORIAL.

Resulta competente el Tribunal a que me honro en dirigirme por ser del partido del lugar donde está sita la finca, conforme al mandato del art. 52.1.8.º LEC, que es fuero necesario (art. 54.1 LEC), controlable ‘ex officio iudicis’, a instancia del Letrado de la Administración de Justicia, en trámite de admisión de la demanda (art. 58 LEC).

II.- PROCEDIMIENTO.

Procede sustanciarse el proceso por los trámites del Juicio Ordinario conforme al art. 249.1.8.º, por tratarse cuestión en materia de propiedad horizontal, y no mera reclamación de cantidad, en base a la acumulación de acciones que permite el art. 73.1 LEC, al exigirse reparación de la avería y reclamación de cantidad por daños.

III.- LEGITIMACIÓN ACTIVA Y PASIVA.

La legitimación activa corresponde a mi mandante como propietario afectado. La legitimación pasiva corresponde a la Comunidad, siendo demandada en la persona de su Presidente, a tenor de lo dispuesto en el art. 13.3 Ley 49/1960, de 21 de julio, de Propiedad Horizontal (en adelante LPH) reformada por Ley 8/1999 de 6 de abril, en cuanto señala que el órgano de representación de la Comunidad en juicio y fuera del mismo, en los asuntos que afecten a la Comunidad, lo es el Presidente elegido de entre los propietarios.

IV.- CAPACIDAD Y REPRESENTACIÓN.

Mi mandante es persona física, mayor de edad, en pleno ejercicio de sus derechos civiles, que tiene capacidad para ser parte y para comparecer, por sí, en su propio nombre y derecho, en este juicio (art. 6.1.1.º y 7.1 LEC).

La Comunidad carece de personalidad jurídica, pero tiene capacidad para ser parte y capacidad procesal por específica disposición legal, a través de sus órganos (arts. 6.1.5.º y 7.6 LEC).

V.- CUANTÍA DE LA DEMANDA.

La cuantía de la demanda a los efectos de lo dispuesto en el art. 253.1 LEC es la de [IMPORTE] EUROS, en aplicación de la regla 2.ª del art. 252 LEC, que es la valoración para reparar los elementos propios y los daños casados, conforme el informe que acompaña a esta demanda.

De ahí procede la perceptividad de la representación por Procurador/a. y la defensa por abogado, conforme a los arts. 23.2.1.º y 31.2.1.º LEC.

VI.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

VII.- FUNDAMENTOS DE DERECHO MATERIALES O SOBRE EL FONDO DEL ASUNTO.

El art. 10.1.a) LPH, en cuanto obliga a la Comunidad a hacer las reparaciones necesarias para el adecuado mantenimiento y cumplimiento del deber de conservación del inmueble y de sus servicios e instalaciones comunes, incluyendo en todo caso, las necesarias para satisfacer los requisitos básicos de seguridad, habitabilidad y accesibilidad universal, con el complemento de indemnizar por los daños causados.

El art. 1.902 CCiv, que obliga a reparar el daño causado por acción u omisión.

Y el art. 1.907, que hace responsable al dueño del edificio por los daños causados por la falta de reparaciones necesarias.

VIII.- COSTAS.

Es preceptiva la condena en costas, incluso aunque se produzca allanamiento, toda vez que, en otro caso, sería un sistema fácil y abusivo esperar al proceso judicial para cumplir lo que antes le correspondía. Es claro que el demandado ha infringido la Ley y ni siquiera ha dado solución a la situación, a pesar de ser requerido previamente, por lo que entendemos existe temeridad y mala fe, conforme a lo dispuesto en los arts. 394 y 395 LEC.

Por lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito, se admita la demanda, y seguido el trámite de Ley, dicte en su día sentencia condenando a la Comunidad de Propietarios [NOMBRE DE LA COMUNIDAD] a llevar a cabo las reparaciones oportunas en el tejado de la Comunidad y a indemnizar a esta parte con la cantidad de [IMPORTE] euros ( €), en concepto de reparación por los daños causados, con expresa imposición de costas.

Por ser de Justicia que pido en [LUGAR], a [FECHA].

Firma de Abogado/a	Firma de Procurador/a
