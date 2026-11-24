---
name: demanda-juicio-verbal-rectificacion-hechos-domicilios-civ-0923
description: "Demanda de juicio verbal de rectificación de hechos con domicilios para notificaciones. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio verbal de rectificación de hechos con domicilios para notificaciones

> Formulario **CIV-0923** del plugin **Proceso civil: demandas, contestaciones, prueba y vista** (`formularios-proceso-civil`) · Civil › Escritos procesales (demanda, contestación, prueba, vista) · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio verbal de rectificación de hechos con domicilios para notificaciones» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio verbal de rectificación de hechos con domicilios para notificaciones” para mi caso». También puedes invocarla directamente con `/formularios-proceso-civil:demanda-juicio-verbal-rectificacion-hechos-domicilios-civ-0923`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-proceso-civil:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Proceso civil: demandas, contestaciones, prueba y vista) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] NOMBRE O DENOMINACIÓN (4 veces)
- [ ] FECHA (3 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] NOMBRE DE LA AGENCIA (3 veces)
- [ ] NOMBRE DEL DIARIO (3 veces)
- [ ] PÁGINA (3 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] PROVINCIA (2 veces)
- [ ] SECCIÓN (2 veces)
- [ ] CALLE
- [ ] DOMICILIO
- [ ] LUGAR Y FECHA
- [ ] MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] OTROS DATOS
- [ ] SEDE

## Normas que cita el formulario

- art. 4 Ley Orgánica 2/1984
- art. 6 Ley Orgánica 2/1984
- art. 1 LO 2/1984
- art. 5.2 LO 2/1984
- art. 2 LO 2/1984
- art. 437.1 LEC
- art. 5 Ley Orgánica 1/2025
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

Don [NOMBRE Y APELLIDOS], mayor de edad, con domicilio en la calle [CALLE], de la localidad de [LOCALIDAD], provincia de [PROVINCIA], comparezco ante este Tribunal y DIGO:

Que en mi propio nombre y derecho formulo demanda de juicio verbal de rectificación contra Don [NOMBRE Y APELLIDOS], director del diario «[NOMBRE O DENOMINACIÓN]» y contra Don [NOMBRE Y APELLIDOS], editor de dicha publicación, ambos con domicilio en la calle, de la localidad de [LOCALIDAD], provincia de [PROVINCIA], la cual fundo en los siguientes:

HECHOS

Primero.- Que el pasado [FECHA] apareció en la sección de [LOCALIDAD], página [PÁGINA] del diario [NOMBRE DEL DIARIO] una información titulada «[NOMBRE O DENOMINACIÓN]», firmada por «[NOMBRE O DENOMINACIÓN]», en la que se aludía directamente a mi persona al indicar la noticia que «[NOMBRE O DENOMINACIÓN]». Acompaño como doc. nº 1 un ejemplar de diario.

Segundo.- Los hechos anteriormente descritos no responden a la realidad pues pese a lo que se desprende objetivamente de la información difundida el texto publicado no se corresponde con la noticia suministrada por la Agencia de noticias [NOMBRE DE LA AGENCIA], de la que se desprende que [OTROS DATOS] (Aporto teletipo íntegro de la citada Agencia [NOMBRE DE LA AGENCIA] como documento nº 2).

Tercero.- La publicación de una información inexacta, en los términos que aquí se ha producido, comportó un descrédito público y privado evidente para mi persona por lo que al día siguiente de la publicación remití al director del diario por correo certificado con acuse de recibo [Nº DE DOCUMENTO], un escrito solicitando la rectificación de los hechos inexactos en el sentido que es de ver en el mismo.

Cuarto.- Pese a los términos claros y precisos en que solicité la rectificación, el director del medio de comunicación publicó en el diario de fecha [FECHA] una rectificación que ni se ajusta a la realidad ni a lo establecido en la Ley. Acompaño como doc. nº 5 el ejemplar en el que se publicó la supuesta rectificación.

Quinto.- Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento nº [Nº DE DOCUMENTO]

FUNDAMENTOS DE DERECHO PROCESAL

COMPETENCIA

Es competente el Tribunal de Instancia de esta Ciudad, por ser el de mi domicilio, al amparo del art. 4 de la Ley Orgánica 2/1984, de 26 de marzo, reguladora del Derecho de Rectificación.

PROCEDIMIENTO

Con arreglo a lo establecido en el art. 6 de la Ley Orgánica 2/1984, en relación con el art. 249.1.2º y 250.1.9º de la LEC, el juicio se tramitará conforme a lo establecido en la LEC para los juicios verbales, con las especialidades contenidas en la LO 2/1984.

LEGITIMACIÓN

Ostento legitimación activa por mi condición de perjudicado ya que mi nombre fue expresamente citado en la información inveraz e inexacta al amparo del art. 1 de la LO 2/1984.

El demandado Don [NOMBRE Y APELLIDOS], es el director del medio de comunicación en el que se difundió dicha información, tal como es de ver en la página [PÁGINA] del ejemplar que se acompaña a la presente (art. 5.2 de la LO 2/1984). También demando al editor, puesto que es doctrina mayoritaria de las Audiencias la que considera que, además del Director, debe ser demandado el editor de la publicación (SAP de Valladolid, de 22 de marzo de 2007, rec. 44/2007, y las que en ella se citan).

PRESUPUESTOS PROCESALES

El art. 2 de la LO 2/1984, regula los requisitos que deben observarse en el ejercicio del derecho de rectificación. Teniendo en cuenta que la publicación apareció el día [FECHA] he dado cumplimiento a la exigencia legal de remitir la solicitud de rectificación al director del medio de comunicación dentro de los siete días naturales siguientes al de la publicación o difusión. Asimismo los documentos 3, 4 y 5 dejan constancia de que el director del diario recibió mi solicitud de rectificación así como de la fecha de su recepción.

Un examen del escrito de rectificación evidencia que la rectificación se limitaba a los hechos de la información cuya rectificación interesaba, sin que su extensión excediera sustancialmente de la información ni se cuestionaran alegaciones subjetivas o juicios de valor del autor.

Pese a ello, el director del medio de comunicación no se ajustó a lo solicitado ya que la publicación ni respeta íntegramente mi solicitud ni ha sido realizada con relevancia semejante a aquella primera noticia que se difundió. En efecto, mientras que la noticia se publicó en la página [PÁGINA], Sección [SECCIÓN], la rectificación se publicó en la última página y dentro de la Sección [SECCIÓN] Además se han incluido comentarios y apostillas con lo que incumple aún más la obligación que le impone la Ley, tal como se aprecia en el doc. nº 5.

La acción de rectificación se ejercita dentro del plazo de siete días hábiles siguientes a la fecha en que se publicó la rectificación que no ha respetado, como se ha dicho, lo establecido en los arts. 2 y 3 de la LO 2/1984.

CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 en relación con el art. 437.1 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

Primero.- El derecho de rectificación viene regulado en la Ley Orgánica 2/1984, de 26 de marzo, y complementa la tutela y protección de otros derechos fundamentales que resultan lesionados en el ejercicio del derecho de información.

Segundo.- El Tribunal Constitucional, nos dice en su Sentencia de 22 de diciembre de 1986, rec. 1045/1985, entre otras, que el llamado derecho de rectificación regulado en la LO 2/1984, de 26 marzo, consiste en la facultad otorgada a toda persona, natural o jurídica, de «rectificar la información difundida, por cualquier medio de comunicación social, de hechos que le aludan, que considere inexactos y cuya divulgación pueda causarle perjuicio» (art. 1 de la LO 2/1984).

Tercero.- Este derecho se satisface mediante la publicación íntegra y gratuita de la rectificación, referida exclusivamente a los hechos de la información difundida, en los términos y en la forma que la Ley señala puesto que como dice la STC arriba citada, el derecho de rectificación es un medio de que dispone la persona aludida para prevenir o evitar el perjuicio que una determinada información pueda irrogarle en su honor o en cualesquiera otros derechos o intereses legítimos, cuando considere que los hechos lesivos mencionados en la misma no son exactos.

Cuarto.- Al no haber rectificado el director la información inexacta en los términos que interesé en mi escrito de rectificación, cuyo texto cumplía con las exigencias establecidas en los artículos 2 y 3 de la Ley, me veo en la obligación de ejercitar la acción de rectificación.

En efecto, como nos dice la SAP de Valladolid, de 22 de marzo de 2007, rec. 44/2007, no se da cumplimiento a esta rectificación cuando el texto publicado contiene comentarios con el fin de desmentir nuevamente lo que la empresa editora considera como rectificación, como sucede en este caso, según se observa de la copia aportada que contiene añadidos que se corresponden con comentarios subjetivos, subrayados en rojo, y que nada tienen que ver con la rectificación solicitada.

Quinto.- Además y aunque la noticia parece dar a entender lo contrario, el teletipo de la Agencia [NOMBRE DE LA AGENCIA], que se cita en el texto publicado, acredita suficientemente que nada tuve que ver con los hechos difundidos, por lo que la alusión a mi persona no responde a la verdad.

Al respecto, cabe añadir que el Tribunal Constitucional se ha pronunciado sobre la diligencia exigible en la comprobación de la información en el sentido de que «el deber de diligencia en la comprobación razonable de la veracidad de la información, que hace prevalente el derecho de información frente a los derechos de la personalidad contemplados en el art. 18.1 CE, no se satisface con la pura y genérica remisión a fuentes indeterminadas, que en ningún caso liberan al autor del cumplimiento de dicho deber, pues, al asumir y transmitir a la opinión pública la noticia, también asume personalmente su veracidad o inveracidad, en cuanto a la que la obligación de contrastar la verosimilitud de la noticia es una obligación personal de cada informador, que es quien está ejerciendo el derecho, y por lo tanto, es a aquel al que incumbe no exceder de sus límites, y evitar la propagación de noticias, que, aún procediendo de sedicentes fuentes bien informadas, no se ha preocupado de contrastar con diligencia razonable » (STC de 12 de noviembre de 1990, rec. 803/1988).

COSTAS

Al amparo del artículo 394 de la LEC, las costas deben imponerse a la parte cuyas pretensiones sean totalmente desestimadas.

Por todo lo expuesto,

SUPLICO AL TRIBUNAL: Tenga por presentado este escrito y demás documentos junto con las copias que se acompañan a las que se dará el curso legal, lo admita, me tenga por comparecido y parte en mi propio nombre y derecho, entendiéndose conmigo las sucesivas diligencias. Y tenga por formulada demanda de juicio verbal civil sobre ejercicio del derecho de rectificación, contra Don [NOMBRE Y APELLIDOS], y Don [NOMBRE Y APELLIDOS], director y editor, respectivamente, del medio de comunicación en el que se difundió la información inexacta y, tras los trámites legales, dicte sentencia por la que se dé lugar a esta demanda y se ordene los demandados que publiquen en el diario [NOMBRE DEL DIARIO], la rectificación en el sentido que interesé en mi escrito de rectificación cursado por correo certificado con acuse de recibo, imponiéndose a los demandados las costas del proceso.

OTROSÍ PRIMERO DIGO: Que designo como domicilio a efectos de notificaciones el sito en esta ciudad [DOMICILIO], disponiendo asimismo de fax nº [NÚMERO] al cual puede dirigir el Tribunal los actos de comunicación.

OTROSÍ SEGUNDO DIGO: Que asimismo designo como domicilio de los demandados la sede del diario [NOMBRE DEL DIARIO], en esta ciudad. Debo manifestar que los demandados disponen también de fax nº [NÚMERO], según se observa en la contraportada del diario, lo cual comunico al Tribunal a los efectos legales procedentes.

En [LUGAR Y FECHA].

========================================================================
