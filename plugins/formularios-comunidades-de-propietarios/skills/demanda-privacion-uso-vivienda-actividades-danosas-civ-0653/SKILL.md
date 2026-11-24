---
name: demanda-privacion-uso-vivienda-actividades-danosas-civ-0653
description: "Demanda de privación del uso de vivienda por actividades dañosas o prohibidas en la comunidad. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de privación del uso de vivienda por actividades dañosas o prohibidas en la comunidad

> Formulario **CIV-0653** del plugin **Comunidades de propietarios** (`formularios-comunidades-de-propietarios`) · Civil › Propiedad horizontal · normativa revisada el 24-11-2026.

## Qué es

Escrito de demanda de juicio declarativo ordinario por el que el presidente de una Comunidad de Propietarios ejercita frente a un copropietario la acción de cesación de actividades prohibidas, dañosas o ilícitas en la propiedad horizontal con privación del uso de la vivienda por llevar a cabo éste en su piso trapicheo o menudeo de droga, lo que ha revertido en una conducta violenta del mismo frente a sus vecinos. La demanda ha sido precedida de un requerimiento notarial de cese inmediato de la referida actividad que fue desatendido por el demandado.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de privación del uso de vivienda por actividades dañosas o prohibidas en la comunidad» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de privación del uso de vivienda por actividades dañosas o prohibidas en la comunidad” para mi caso». También puedes invocarla directamente con `/formularios-comunidades-de-propietarios:demanda-privacion-uso-vivienda-actividades-danosas-civ-0653`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-comunidades-de-propietarios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Comunidades de propietarios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº DE DOCUMENTO (11 veces)
- [ ] NÚMERO (8 veces)
- [ ] FECHA (5 veces)
- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] CALLE (3 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] FECHAS
- [ ] LETRA
- [ ] LUGAR
- [ ] Nº
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
- art. 13.3 LPH
- art. 7.2 LPH
- art. 35 CC
- art. 25 LEC
- art. 23 LEC
- art. 5 Ley Orgánica 1/2025
- art. 330 LEC
- art. 704 LEC
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
(1) El Decreto 2414/1961, de 30 de noviembre, por el que se aprueba el Reglamento de actividades molestas, insalubres, nocivas y peligrosas ha sido derogado por el número 1 de la disposición derogatoria única de la Ley 34/2007, de 15 de noviembre, de calidad del aire y protección de la atmósfera. Téngase en cuenta, no obstante, que la citada disposición mantendrá su vigencia en aquellas comunidades y ciudades autónomas que no tengan normativa aprobada en la materia, en tanto no se dicte dicha normativa.

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

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a. de los Tribunales, que actúa en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS], en su condición de Presidente de la Comunidad de Propietarios del edificio señalado con el n.º [NÚMERO] de la calle [CALLE] de [LOCALIDAD],según acredito con la copia de escritura de poder que se me otorgó y acompaño, con ruego de que se devuelva previo testimonio en autos, bajo la dirección técnica del Letrado en ejercicio D./Dña. [NOMBRE Y APELLIDOS], con despacho profesional en esta capital sito en [LOCALIDAD], ante el Tribunal comparezco y como mejor proceda en Derecho, DIGO:

Que mediante el presente escrito y en nombre de mi mandante formulo demanda de juicio ordinario, sobre acción de cesación de actividades prohibidas, dañosas o ilícitas con privación del uso de la vivienda; contra

Ordenados y separados, hacemos constar los siguientes:

HECHOS

PRIMERO.- Mi mandante es Presidente de la Comunidad de Propietarios del edificio señalado con el n.º [NÚMERO], de la calle [CALLE], según consta en el acta de la Junta de Propietarios que se acompaña como documento n.º [NÚMERO] y certificación de vigencia expedida por el Secretario como documento n.º [NÚMERO].

SEGUNDO.- El demandado D./Dña. [NOMBRE Y APELLIDOS] es arrendatario de la vivienda sita en dicho edificio, planta [PISO] letra [LETRA] teniendo la propiedad de la misma un coeficiente de [Nº] por ciento de participación en los elementos comunes; así resulta de las manifestaciones del dueño en Junta de propietarios de fecha [FECHA], conforme certificación del Libro de Actas que expide el Secretario (documento n.º [NÚMERO]), a expensas de que se requiera la acreditación documental de quien la posea.

TERCERO.- Las actividades del demandado en la referida vivienda consisten en el ‘trapicheo’ al menudeo de droga a toxicómanos, lo que ha revertido en una conducta violenta del mismo frente a sus vecinos, lo que ha sido objeto de diversas denuncias ante la jurisdicción penal, lo que ha motivado que se hayan seguido varios procedimientos en los que ha sido imputado, sin que se sepa de condena por el momento (documentos números [Nº DE DOCUMENTO], [Nº DE DOCUMENTO] y [Nº DE DOCUMENTO]). Asimismo ha tenido que ser requerida la presencia policial por algunos vecinos ante las alteraciones del orden y la convivencia producidas por el trasiego de toxicómanos al domicilio del demandado según acreditamos con las copias de denuncias e informes de la Policía Municipal (documentos [Nº DE DOCUMENTO], [Nº DE DOCUMENTO] y [Nº DE DOCUMENTO]).

CUARTO.- Vista la situación, la Junta de la Comunidad acordó en su sesión general del día [FECHA] requerir al demandado para que cesara inmediatamente en las referidas actividades molestas, peligrosas e inmorales (documento n.º [NÚMERO]). Tal requerimiento se llevó a efecto notarialmente (documento n.º [NÚMERO]), haciendo caso omiso el demandado, que ha sido objeto de posteriores denuncias (documentos [Nº DE DOCUMENTO] y [Nº DE DOCUMENTO]).

QUINTO.- El fecha [FECHA], la Junta de propietarios, especialmente convocada al efecto, acordó facultar al Presidente para la interposición de demanda para la cesación de las actividades en cuestión y para conseguir el inmediato desalojo de su protagonista, procediendo a contratar los profesionales precisos al efecto (copia del acta como documento [Nº DE DOCUMENTO]).

SEXTO.- La parte actora manifiesta que, previo a la presentación de la presente demanda, se han llevado a cabo negociaciones con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad, y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria; incluyéndose entre las acciones realizadas el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución.

Finalmente, mi representado envió un requerimiento fehaciente al demandado con fecha [FECHA], fijando un plazo de 30 días naturales para llegar a un acuerdo amistoso, a través del abogado que firma este escrito, el cual fue contestado por el demandado por el mismo medio, rechazando el acuerdo/ habiendo sido solo posible un acuerdo parcial, viéndonos en la necesidad de acudir a la presente vía judicial, respecto a los extremos de la controversia en los que se mantiene la discrepancia.

Acompaño como documento nº [Nº DE DOCUMENTO], el requerimiento efectuado y como documento nº [Nº DE DOCUMENTO], la contestación del demandado.

A los anteriores hechos son de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN Y COMPETENCIA

A) JURISDICCIÓN.

POTESTAD JURISDICCIONAL. La potestad jurisdiccional se ejerce por los Jueces y Tribunales determinados por las leyes, según las normas de competencia y procedimiento que las mismas establezcan (art. 117.3 CE).

JURISDICCIÓN CIVIL. Los Tribunales del orden civil conocerán, además de las materias que les son propias, de todas aquellas que no estén atribuidas a otro orden jurisdiccional (art. 9.2 LOPJ).

ÁMBITO DE LA JURISDICCIÓN. La extensión y límites de la jurisdicción de los Tribunales civiles españoles se determinará por lo dispuesto en la LOPJ y en los tratados y convenios internacionales en los que España sea parte (art. 36 LEC), no existiendo en el presente asunto elemento ninguno de extranjería.

B) COMPETENCIA

PREDETERMINACIÓN LEGAL DE LA COMPETENCIA. Para que los Tribunales civiles tengan competencia en cada caso se requiere que el conocimiento del pleito les esté atribuido por normas con rango de ley y anteriores a la incoación de las actuaciones de que se trate (art. 44 LEC).

COMPETENCIA OBJETIVA.

Corresponde a las secciones civiles de los tribunales de instancia, puesto que no viene atribuida por Ley esta causa civil a otros Tribunales (art. 85.1 LOPJ y 45 LEC).

COMPETENCIA TERRITORIAL.

Resulta competente el Tribunal a que me honro en dirigirme por ser del partido del lugar donde está sita la finca, conforme al mandato del art. 52.1.8.º LEC, que es fuero necesario (art. 54.1 LEC), controlable ‘ex officio iudicis’, a instancia del Letrado de la Administración de Justicia, en trámite de admisión de la demanda (art. 58 LEC).

II.- PROCEDIMIENTO

Conforme al número 8.º del art. 249.1 de la Ley de Enjuiciamiento Civil el procedimiento ajustado a derecho, por tratarse de acción que otorga a la Junta de propietarios la Ley de propiedad Horizontal, será el del juicio declarativo ordinario regulado en los arts. 399 a 436 de la misma Ley.

III.- LEGITIMACIÓN ACTIVA Y PASIVA

En cuanto a la activa corresponde a mi mandante, en general, a tenor del art. 13.3 LPH, y en particular, conforme al art. 7.2 párrafo 3.º LPH, que señala que si el infractor persistiere en su conducta (después de requerido de cese), previa autorización de la Junta de propietarios, debidamente convocada al efecto, podrá entablar contra él acción de cesación.

En cuanto a la legitimación pasiva corresponde al demandado conforme al mismo art. 7.2 LPH, puesto que la acción de cesación está prevista contra el condómino en propiedad horizontal, así como contra el ocupante del piso o local, siendo que en el presente caso se legitima pasivamente a un arrendatario.

IV.- CAPACIDAD Y REPRESENTACIÓN

Mi mandante es el representante legal de la entidad sin personalidad que es la Comunidad de propietarios del edificio señalado con n.º [NÚMERO] de la calle [CALLE] de [LOCALIDAD], por lo que detentando capacidad para ser parte por ministerio de la ley dicha comunidad, la capacidad procesal, o para comparecer en juicio, corresponde a su Presidente (arts. 6.1.5.º y 7.6 LEC).

La Comunidad carece de personalidad, pero corresponde a una entidad compleja que se asemeja a las personas jurídicas civiles conforme al art. 35 CCiv, más allá de los meros actos de conjunto (STS de 14 de mayo de 1992 ), que actúa mediante representación cuasiorgánica, en la que el Presidente sustituye formalmente la voluntad de la entidad, en los asuntos que le afectan.

El demandado es persona física, mayor de edad, soltero, cuya limitación de capacidad de obrar se ignora, que será parte por sí, con capacidad para comparecer en este juicio (art. 6.1.1.º y 7.1 LEC), siempre que cumpla los oportunos requisitos de postulación para oponerse a la presente demanda.

V.- POSTULACIÓN Y DEFENSA

El actor ha otorgado poder notarial al Procurador/a. de los Tribunales que encabeza este escrito, habilitado en el partido del Tribunal, cuya copia auténtica se ha aportado, general para pleitos (art. 25 LEC), siendo redactada y firmada la demanda por la abogada ejerciente colegiada que dirige el asunto y se identifica en el encabezamiento, según resulta preceptivo conforme a los arts. 23 y 31 LEC.

VI.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

VII.- FUNDAMENTOS MATERIALES

El art. 7.2 LPH resulta la norma de referencia, en cuanto que las actividades desarrolladas y que sigue desarrollando el demandado en el inmueble perteneciente a la copropiedad están expresamente prohibidas por los estatutos, y son ilícitas, como molestas e insalubres conforme al Reglamento de Actividades Molestas, Insalubres, Nocivas y Peligrosas aprobado por Decreto 2414/1961, de 30 de noviembre, por lo menos en cuanto a la existencia de evidentes elementos contrarios a la salud y la presencia continua de personas inmersas o próximas a la delincuencia. No se trata de avasallar la presunción de inocencia por un grave delito —el demandado ha sido detenido en tres ocasiones— sino de señalar, como se documenta, la continua evidencia de posesión y consumo de estupefacientes fuera del ámbito de la intimidad.

La conducta reiterada, después de numerosísimos intentos de arreglo extrajudicial, dio lugar según lo previsto legalmente, al apercibimiento fehaciente para que cesara en las mismas, y habiendo sido desatendido este requerimiento y reiterada la conducta proscrita, el Presidente convocó expresamente al efecto Junta de propietarios extraordinaria, a la que acudió el dueño del piso, quien informó de sus intentos baldíos por reconducir la situación y el absentismo en reclamar a su inquilino, habida cuenta de la renta ridícula que debe percibir y no percibe, y anteriores episodios litigiosos, y en la que se acordó por unanimidad la interposición de demanda para la cesación y privación del uso.

Se insta la acción que justifica este procedimiento, con la pretensión de que se prive al demandado y a quien con él conviva, del uso del piso y sus añadidos, y como quiera que la posibilidad legal de privación alcanza a los tres años, y dada la gravedad de los hechos, así como la contumacia del demandado, en tanto que el contrato de arrendamiento (cuya exhibición se pedirá en su momento conforme al art. 330 LEC) tiene plazo que expira al de dos años, se pide la privación definitiva de los derechos posesorios arrendaticios, con obligación de desalojo en términos del art. 704 LEC.

VIII.- COSTAS.

Conforme al art. 394 LEC las costas han de imponerse a la parte demandada, por principio objetivo del vencimiento

Por lo expuesto,

SUPLICO AL TRIBUNAL

que teniendo por presentado este escrito y documentos que le acompañan, con sus copias, lo admita a trámite, me tenga por comparecido y parte, y admita a trámite la demanda que se formula, acordando conferir traslado de la misma al demandado D./Dña. [NOMBRE Y APELLIDOS] emplazándole para que en término de veinte días comparezca y la conteste, y seguido el juicio por sus trámites, se dicte en definitiva sentencia por la que estimando la demanda, se condene al demandado al cese de las actividades que justifican la demanda, con la privación del uso del piso de referencia y sus añadidos durante el plazo de dos años, declarando extinguido el contrato de arrendamiento de vivienda que disfruta y el desalojo en plazo legal, bajo apercibimiento de ser lanzado, con expresa imposición de costas procesales y demás que sea procedente,

Por ser de Justicia que pido en [LUGAR], a [FECHA].

Firma de Abogado/a	Firma de Procurador/a
