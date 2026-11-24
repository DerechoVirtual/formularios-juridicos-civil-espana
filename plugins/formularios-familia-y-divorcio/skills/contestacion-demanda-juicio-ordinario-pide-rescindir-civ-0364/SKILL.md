---
name: contestacion-demanda-juicio-ordinario-pide-rescindir-civ-0364
description: "Contestación a demanda de juicio ordinario que pide rescindir la liquidación de gananciales. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contestación a demanda de juicio ordinario que pide rescindir la liquidación de gananciales

> Formulario **CIV-0364** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Contestación a la demanda de juicio ordinario dirigido al Tribunal de Instancia, de rescisión de liquidación de gananciales. El demandado se opone a la misma por entender que la comunidad no era de gananciales sino pro indiviso y por la inexistencia de lesión.

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contestación a demanda de juicio ordinario que pide rescindir la liquidación de gananciales» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contestación a demanda de juicio ordinario que pide rescindir la liquidación de gananciales” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:contestacion-demanda-juicio-ordinario-pide-rescindir-civ-0364`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (12 veces)
- [ ] NÚMERO (9 veces)
- [ ] FECHA (8 veces)
- [ ] LOCALIDAD (8 veces)
- [ ] IMPORTE (7 veces)
- [ ] Nº DE DOCUMENTO (6 veces)
- [ ] DENOMINACIÓN SOCIAL (4 veces)
- [ ] Nº (3 veces)
- [ ] ENTIDAD BANCARIA (2 veces)
- [ ] APELLIDOS
- [ ] AÑO
- [ ] LUGAR
- [ ] MES
- [ ] SEDE

## Normas que cita el formulario

- art. 1.074 CC
- art. 1.435.3 CC
- art. 1.443 CC
- art. 1.290 CC
- art. 1074 CC
- art. 406 CC
- art. 394 LEC
- art. 339.2 LEC

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

- Junto a «…MILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.
- Junto a «…que recayó sentencia de la Sección de Familia, Infancia y Capacidad del Tribunal»: Denominación legal: Sección de Familia, Infancia y Capacidad. Si no existe en el partido, conoce la Sección Civil o la Única (art. 86.3-4 LOPJ). Fuente: LOPJ arts. 84.2.a) y 86 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…6 (redacc. LO 1/2025, BOE-A-2025-76).] de Instancia, plaza n.º [NÚMERO], de esta»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales y de D./Dña. [NOMBRE Y APELLIDOS], cuya representación acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], a fin de que conste en autos de Juicio Ordinario n° [Nº] / [AÑO], comparezco y como mejor en derecho proceda, DIGO:

Que por medio del presente escrito, en la representación que ostento, me persono y muestro parte en el presente procedimiento para CONTESTAR LA DEMANDA, lo que hago en tiempo y forma, y para OPONERME a la misma, en base a los siguientes hechos y fundamentos de Derecho:

HECHOS

PRIMERO.- Al correlativo. Se dice que el matrimonio contraído entre los contendientes tuvo lugar en [LOCALIDAD], el [FECHA].

Lo expuesto es cierto, y hacemos nuestro el documento que se adjunta para acreditarlo con la demanda, el certificado literal de inscripción de matrimonio.

Igualmente se dice que el citado matrimonio fue contraído bajo el régimen legal de gananciales, remitiendo para demostrar el extremo al documento antes citado.

Pero, de dicho documento, precisamente se prueba QUE LOS CONTENDIENTES SE HALLABAN SEPARADOS, por sentencia firme dictada por el Tribunal de Instancia n° [Nº] de [LOCALIDAD], de [FECHA], desde

De tal evidencia se desprende que la sociedad de gananciales se extinguió, por Ley, por lo que los contendientes desde dicha fecha se regían por el RÉGIMEN LEGAL DE ABSOLUTA SEPARACIÓN DE BIENES.

Este extremo es esencial en este procedimiento y se oculta a lo largo de toda la demanda.

SEGUNDO.- Al correlativo. De un matrimonio que se dice unido se pasa a un divorcio, que se obtuvo en razón a una separación judicial precedente al amparo de la interposición de demanda de separación de los cónyuges con precedencia de más de un año, como así se acredita del propio documento nº [Nº DE DOCUMENTO] que se adjunta con la demanda y que hacemos nuestro.

Fundado en una ganancialidad inexistente, a las fechas del reparto que hicieron los esposos en el convenio regulador, según su conveniencia y voluntad, se concluye con la siguiente estipulación:

" Se reconoce expresamente por los firmantes que la aludida división de bienes no causa exceso de adjudicación a ninguna de las partes "

TERCERO.- Al correlativo. Es cierto que el convenio regulador se hizo de mutuo acuerdo entre los cónyuges y por el Letrado D./Dña. [NOMBRE Y APELLIDOS] Ignacio [APELLIDOS], y teniendo la esposa el consejo de su actual Letrado con la que le une amistad.

Nadie puede poner en tela de juicio la honradez del proceder del citado Letrado, quien conociendo perfectamente la Ley, lo que hizo fue un reparto entre cónyuges que ya estaban separados pero habían convivido después de la separación, a los efectos de mejorar a la esposa, y evitar las inconveniencias fiscales en divisiones de proindivisos que afectan a inmuebles o valores mobiliarios de sociedades mercantiles.

El citado Letrado aconsejó a quienes él conocía que se encontraban separados judicialmente, pero que mantenían una convivencia, que para adjudicar a la esposa el domicilio conyugal, comprado por ambos después de la separación, lo más barato era hacer figurar una aparente ganancialidad y así obviar los gastos de donaciones y adjudicaciones de proindivisos.

Por ello, en dicho convenio regulador, el citado Letrado omite los usuales exponendos referidos al régimen económico matrimonial.

Por lo tanto, es inveraz que el convenio fuese de liquidación y adjudicación de bienes gananciales, puesto que A TAL FECHA NO HABÍA BIENES GANANCIALES en absoluto, sino bienes adquiridos por uno y otro cónyuge, y bienes adquiridos por ambos, en comunidad ordinaria.

CUARTO.- Al correlativo. Demostrado el divorcio que conlleva una precedente separación judicial, que operó, nada menos, que el [FECHA], fecha a partir de la cual NO EXISTÍA RÉGIMEN LEGAL DE SOCIEDAD DE BIENES GANANCIALES sino ABSOLUTA SEPARACIÓN DE BIENES, la liquidación que se hizo en el convenio regulador no fue de una inexistente sociedad de gananciales, y los bienes que se incluyen fueron adquiridos DESPUÉS DE LA EXTINCIÓN DEL RÉGIMEN MATRIMONIAL.

QUINTO.- Con lo ya manifestado, y que se demuestra desde documentos de la parte adversa, ya quedaría contestada la demanda, y no obstante, por elemental norma de defensa, vamos a contestar debidamente lo que refiere la adversa al amparo del convenio que analiza en el correlativo que nos ocupa.

ACTIVO

A) INVENTARIO DE BIENES INMUEBLES

1.- El primer bien que se recoge en el inventario es el bien que motiva dicha liquidación, pues el Letrado conocía muy bien que el orden de inventario no se inicia por los inmuebles.

Es el domicilio que fuera adquirido por ambos cónyuges tras su separación, inscrito a nombre de ambos, y que por tanto exigía una división de cosa común cara y contraria a la voluntad de los cónyuges, quienes deseaban que la vivienda se ‘regalara’ a la propiedad exclusiva de la esposa, que quedaba con los hijos comunes.

Esa vivienda tenía un valor superior a los [IMPORTE] euros en que se evaluó, y esta parte desde ahora impugna el documento nº [Nº DE DOCUMENTO] de la demanda, en que se presenta dictamen del Agente de la Propiedad Inmobiliaria D./Dña. [NOMBRE Y APELLIDOS]

2.- La finca rústica de ‘La Igareda’, en [LOCALIDAD] era otro proindiviso formal, adquirido con dinero privativo de mi mandante que no tenía a tales fechas, ni lo tiene en la actualidad, un chalet, como se pinta en la demanda, sino una pequeña construcción, sin permiso de habitabilidad y constituía una auténtica cabaña.

Impugnamos el citado documento nº [Nº DE DOCUMENTO], dictamen pericial que refleja, con absoluta falta de verdad, la situación de dicho inmueble en la actualidad, y no a las fechas en el que se procedió a su "división" a favor de mi mandante, volviendo a insistir, que lo realmente importante, no es la valoración de los bienes inventariados sino su naturaleza jurídica.

B) INVENTARIO DE BIENES MUEBLES

3.- El derecho de las tres mil participaciones sociales en [DENOMINACIÓN SOCIAL] fue adquirido por mi mandante, con el evidente carácter privativo y por ello en la misma demanda tan sólo se refiere a su valoración para intentar sostener una rescisión por lesión absolutamente impensable.

Tales valoraciones se hicieron, se reitera, pues de un lado se pretendía repartirse entre cónyuges los bienes adquiridos en proindiviso después de su separación y como quiera que se quiso adjudicar a la esposa el domicilio conyugal más la cantidad de [IMPORTE] euros, como más adelante se indicará, se hubo de incluir ficticiamente ciertos bienes, de carácter privativo del esposo, para compensar adjudicaciones y evitar divisiones de cosas comunes que perjudicarían a la esposa, pues los inmuebles se habían adquirido a nombre de ambos, y LAS ACCIONES DEL NEGOCIO DEL ESPOSO SE HABÍAN ADQUIRIDO AL SÓLO NOMBRE Y DERECHO DE ÉSTE.

Las tres mil participaciones sociales siempre fueron privativas del esposo por las siguientes obvias razones:

-Fueron suscritas con posterioridad a la separación, o lo que es igual cuando ya se había extinguido "ope legis" la sociedad de gananciales.
-Se suscribieron a nombre, únicamente, del esposo, a diferencia de los inmuebles que se suscribieron a nombre de ambos cónyuges.

En cualquier de los casos, se impugna el dictamen de valoración que como documento nº [Nº DE DOCUMENTO] de la demanda se aporta a título de pericial, acompañándose informe del auditor censor jurado de cuentas D./Dña. [NOMBRE Y APELLIDOS], que concluye una valoración ponderada al principio de la actividad real de la empresa, y no sólo con base en el balance de situación de las últimas cuentas anuales (DOC Nº [NÚMERO]).

4.- Nada se objeta a la valoración de las doscientas cincuenta participaciones de [DENOMINACIÓN SOCIAL].

5.- El ajuar doméstico, naturalmente era de mayor valor al señalado pero, se insiste, su naturaleza era privativa del esposo, pues era él quien lo había adquirido y abonado después de la disolución de la sociedad de bienes gananciales, con dinero privativo suyo.

Tampoco se incluía en el inventario "amañado" que se hizo, las acciones que en proindiviso tenían los esposos y que meses antes se vendieron, adjudicándose el precio obtenido de las mismas a la esposa y adjudicando a ésta la titularidad exclusiva de una cuenta bancaria que figuraba abierta a nombre de los dos y en la que obraban depositados los valores en proindiviso.

Se acompaña certificación del BANCO [ENTIDAD BANCARIA], (DOC. Nº [NÚMERO]) en que se documenta el reparto, o mejor dicho la adjudicación graciosa, por medio de lo que la esposa se embolsó [IMPORTE] euros, más los saldos de la cuenta que conjuntamente mantenía con mi mandante, conforme demuestra la certificación de la CAJA DE AHORROS [ENTIDAD BANCARIA], que se adjunta como DOC Nº [NÚMERO].

PASIVO

El Convenio señalaba que no existía pasivo alguno.

En la demanda se dice que el domicilio conyugal mantenía un pasivo de [IMPORTE] euros en garantía de un préstamo recibido por la empresa en la que participaba privativamente mi mandante.

Se hace referencia a una certificación registral, en la que a las fechas que se emite existía la citada inscripción de hipoteca, si bien tal hipoteca se había cancelado, aunque todavía no estaba asentada la cancelación.

Adjunto la oportuna certificación del Registro de la Propiedad de [LOCALIDAD], como DOC Nº [NÚMERO], que acredita la evidencia de la CANCELACIÓN DE DICHO CRÉDITO CON FECHA [FECHA] DE [MES] DE

SEXTO.- Al correlativo. En ningún caso cabe adicionar bienes que no son gananciales, ni en ningún caso cabe lesión sobre bienes que no son gananciales.

En lo afectante a la vivienda de [LOCALIDAD], la misma se adquirió en proindivisión.

Según admite la demanda, dicho bien fue vendido, y del precio el esposo le dio a su esposa [IMPORTE] euros, y él recibió [IMPORTE] euros.

Este inmueble no se inventarió en el reparto que se hizo en el sedicente convenio de liquidación, conociéndolo ambas partes, pues también se pretendía venderlo por ambos cónyuges, extinguir así su proindivisión, y mejorar a la esposa en el reparto del precio común.

Así fue, porque con fecha inmediatamente siguiente al convenio regulador se hizo el documento privado que se adjunta de adverso, que suscribió la actora, y el resultado le fue beneficioso en [IMPORTE] euros.

Adjuntamos el contrato privado de venta del piso como DOC Nº [NÚMERO].

SÉPTIMO.- Al correlativo. La mala fe en este conflicto se encuentra con claridad del lado de la demandante, que es quien oculta una separación judicial, oculta una disolución de bienes gananciales, [Nº] AÑOS ANTES DEL CONVENIO, y pretende la rescisión.

La adversa ha solicitado dinero a cambio de no iniciar este proceso, y naturalmente mi mandante no ha aceptado pagar por eludir una pretensión que en ningún caso puede prosperar.

Lo que sí es cierto es que se ha deducido esta demanda cuando en ejecución de la sentencia de divorcio se han dado diversas reclamaciones sin que en ninguna de ella se nombrase la pretendida rescisión por lesión.

Nos remitimos al juicio de modificación de medidas definitivas por alteración sustancial de circunstancias, en que recayó sentencia de la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia, plaza n.º [NÚMERO], de esta plaza (nº [NÚMERO] /), en que se fijó pensión alimenticia dispar de la probada por el convenio regulador, sin mención alguna al aspecto patrimonial entre los casados, que no se mentaba por la actora, toda vez que se contrató sobre ello de toda conformidad (DOC Nº [NÚMERO]).

FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN Y COMPETENCIA.

La admitimos a los meros efectos procesales, si bien señalamos, desde ahora, que la presente demanda constituye un intento de provocar un error judicial con evidente designio de obtener un lucro.

II.- LEGITIMACIÓN.

La propia demandante reconoce que su perjuicio y su legitimación deriva "de la liquidación de la sociedad de gananciales" por lo que en base a tal falta genuidad resulta evidente que carece de legitimación activa, en el sentido de esa posición jurídica habilitante para que frente a mi poderdante se pueda postular la tutela judicial del caso, lo que condiciona negativamente el dictado de la sentencia, como cuestión preliminar al fondo, y que impone la desestimación por ausencia de legitimación activa, toda vez que la sociedad de gananciales se disolvió el [FECHA], y por tanto los bienes adquiridos por los esposos con posterioridad a tal fecha, lo fueron bajo una separación de bienes legal, y en su razón, los bienes escriturados a nombre de ambos lo eran en proindiviso y los bienes adquiridos a nombre de uno de ellos lo eran de carácter privativo de su titular formal.

III.- PROCEDIMIENTO Y CUANTÍA.

Lo admitimos a efectos formales, debiendo significar que no se señala la cuantía de la reclamación, adición o lesión, lo cuál también constituye una maniobra inteligente para evitar o cuanto menos poder discutir las costas.

IV.- POSTULACIÓN.

Se comparece como exigen arts. 23.1 y 31.1 LEC, representado D./Dña. [NOMBRE Y APELLIDOS] por Procurador/a de los Tribunales habilitado en este partido judicial, y con la dirección del Letrado que consta en el encabezamiento, ejerciente en el Iltre. Colegio de Abogados de

V.- FONDO DEL ASUNTO

No hacen al caso los preceptos que se citan en el correlativo y fundamentalmente el art. 1.074 CCiv, a que reenvía el art. 1.410, toda vez que tal aplicación sólo cabe cuando se deriva de una liquidación de bienes gananciales y como queda reiteradamente expuesto y acreditado, tras la separación judicial de [FECHA], no hubo ningún bien de carácter ganancial.

La "liquidación" que los esposos hicieron en el convenio regulador no fue otra cosa que una división de cosas comunes, y unas donaciones a favor de la esposa, encubierto bajo la apariencia de una ganancialidad, que se empleó para evitar gastos y mejorar a la esposa.

Es un dato inapartable que la separación conyugal por sentencia firme disuelve de Derecho todo régimen matrimonial comunitario [STS de 14 de abril de 1992], y produce el establecimiento de la separación de bienes (art. 1.435.3º CCiv), sin que la reconciliación de los cónyuges en caso de separación personal produzca efecto de alterarlo (art. 1.443 CCiv).

Sostener que la sociedad de gananciales que se dice liquidar en el convenio regulador tenía su vigencia en la realidad práctica, a pesar de las normas, es inviable, ya que produce una evidente mixtificación entre los derechos y deberes de contenido no económico del matrimonio y el régimen económico con el que éste siempre debe contar, no pudiéndose sentenciar al margen de un mandato legal imperativo con la aceptación de un estado de puro hecho, y precisamente para acoger una acción que no se dispensa más que en un supuesto legal concreto, que es el de la liquidación de gananciales.

La sociedad de gananciales que es el régimen legal supletorio, no destila de ninguna esencia de la institución matrimonial ‘per se’. Existe por ley, en defecto de otra voluntad de los cónyuges, y desaparece por ley en determinados supuestos, sin que nada impida que los cónyuges puedan pactarla de nuevo en capitulaciones matrimoniales. En Navarra y Aragón el régimen legal es muy poco diferente -régimen de conquistas, o el de muebles y adquisiciones, respectivamente-, y en Derecho especial genérico de Cataluña y Baleares lo es totalmente, ya que rige la separación de bienes. Ello no tiene qué ver con los derechos y obligaciones de la institución matrimonial: convivencia, asistencia y socorro mutuo, etc, ni con los que derivan de la filiación u otro parentesco.

El que los litigantes hayan vuelto a convivir como cualquier matrimonio poco después de separarse legalmente, haya sido o no una reconciliación efectiva -que desde luego no se hizo pública, ni enteró a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia-, por explícita voluntad legal carece de efectos en el plano económico, como por explícita voluntad legal el matrimonio de los vecinos civiles en la mayoría de la península, sin que lo contraríen formalmente los interesados -en escritura pública- tuvo unos efectos económicos y no otros. Por ello, resulta inconducente demostrar indicios de ‘normalidad’ del matrimonio para sostener que el matrimonio ‘reconstruido’ conlleva la sociedad de gananciales, dado que no se puede razonar como connatural este régimen de bienes, sino simplemente se establece o extingue por voluntad legal, en defecto de la voluntad de los casados. Hay que recordar que la separación de bienes no elude el régimen matrimonial primario y el deber de levantamiento de las cargas familiares, y por supuesto, que los cónyuges adquieran bienes en común, o contraten entre sí.

El convenio regulador de autos, que contiene una sedicente liquidación de comunidad de gananciales, cualquiera que sea la razón por la que se calificó así lo que jurídicamente no podía serlo en términos técnicos, y que respaldara el Abogado D./Dña. [NOMBRE Y APELLIDOS], aunque haya sido homologado judicialmente e incorporado como válido a la sentencia que decretó el divorcio de los esposos, no deja de ser un contrato especial típico entre los que lo suscriben, que autorregulan sus intereses.

Lógicamente, pudiera acordarse su nulidad por algún vicio de consentimiento, como podría ser el error inexcusable de la esposa, o las maquinaciones dolosas del esposo, pero la rescindibilidad contractual es una excepción puntual de nuestro sistema jurídico, que cabalmente parte de la base de que el negocio jurídico es válido (cfr.: art. 1.290 CCiv).

Y en el pleito se ejerce precisamente la pretensión de rescisión por lesión al amparo del art. 1074 CCiv, que se trata de una facultad del contratante que se basa en una regla de contabilidad objetiva.

Y la rescisión por lesión en la liquidación de la sociedad de gananciales es posible por remisión a las normas de la partición y liquidación de la herencia, de modo que no tiene sentido aducir una facultad contemplada para un presupuesto normativo, totalmente excepcional y objetiva, respecto de un negocio que, cualquiera que sea el tenor inadecuado que lleve, no es el de dicho presupuesto.

La liquidación de un régimen legal de participación, o de un régimen comunitario pacticio, así como la división de cosa común, no son rescindibles por lesión, ya proceda de un contrato privado, ya proceda de una acción ante los tribunales (en procedimiento de art. 806 y ss. de nueva LEC, o en declarativo), dado que no hay previsión legal al respecto, más que para la partición hereditaria y de la sociedad de gananciales.

De suyo, cuando el art. 406 CCiv reenvía para la partición entre los partícipes en la comunidad de bienes o proindiviso ordinario, a las reglas concernientes a la división de la herencia, se tiene adoctrinado por la Sala I TS que no cualquier precepto de la Sección 2º, Capítulo VII, Título III, del Libro III CCiv, puede aplicarse sin limitación a comunidades ‘romanas’ sino que es un régimen supletorio en lo que no se oponga o contradiga el sistema de estas instituciones [STS de 31 de octubre de 1989 ], ‘a fortiori’ concluiremos que las peculiaridades de los efectos de las particiones hereditarias, la rescisión por lesión y la responsabilidad por deudas hereditarias, no son utilizables más que concretamente en la partición de una ‘postganancialidad’.

Abundantemente, y por corresponder a los esfuerzos alegatorios estériles de la demanda, el ámbito de una acción rescisoria, que es por definición de la mayor objetividad, pues se basa en un nuevo cálculo de datos previos, incluso si se admitiera que una comunidad de ciertos bienes, todos adquiridos en supuesta indivisión por mitades partes, se inventarió, valoró y liquidó con adjudicación a los dos comuneros, de todas las maneras no evidencia lesión, por lo que habría de desecharse la demanda.

La demandante sostiene que el inmueble que se adjudicó está correctamente valorado, si bien se le transfirió con carga, mientras que el ajuar doméstico que también ha recibido se halla asimismo sobrevalorado, y por el contrario, las participaciones de [DENOMINACIÓN SOCIAL]., y una finca rústica con cabaña en un pueblo de [LOCALIDAD], que tomó de la comunidad el demandado, se encontraba claramente infravalorado.

Y el asunto es que la prueba pericial de la demanda es inservible para demostrar tales cosas:

El dictamen del A.P.I. Sr./a. [NOMBRE Y APELLIDOS], resulta de parámetros puramente externos, es decir, sin examen del estado del interior de la vivienda, y por ende, sin poderse verificar muebles y enseres, así como las mejoras y situación de conservación, refiriéndose a una media del valor homologado de la superficie del predio y de la vivienda edificada en la misma, en su estado actual, y sin que el tasador sepa cuál fuera su estado en el momento del documento divisorio, siendo que en la escritura de adquisición no aparece casa alguna, y es la misma demanda la que admite que hubo una cabaña, que luego se ha ido transformando en una suerte de pequeño chalet, concreto estado de transformación que no es veraz ahora, cuanto más se dividió su propiedad.

El dictamen de [FECHA]. es puramente contable, se atiene a un examen de la cuentas anuales registradas de una mercantil inscrita, y si ello tiene valor en muchos ámbitos, no se puede admitir que lo tenga para valorar realmente a estos efectos discutidos unas participaciones en una empresa familiar -como por diversos conductos se demostrará, con dos titulares, que son los que trabajan y sus respectivas compañeras- de cuya actividad, estado real, y perspectivas, el que informa sobre la cuentas expresamente dice nada saber.

Por otra parte, ningún esfuerzo de prueba se dirige a infravalorar el ajuar doméstico, y la alegación de permanencia de cargas hipotecarias sobre la vivienda adjudicada a la actora es anodina, ya que está certificada la amortización por la entidad prestataria, y su cancelación registral operó con cargo al demandado.

Por cuanto toca a la división del piso de [LOCALIDAD], en nada perjudicó a la actora, que recibió más de la mitad de su precio en venta, y tampoco hay razón para incluirlo en una nueva liquidación de bienes comunes.

En fin, se acredita una división de proindivisos al margen del convenio regulador del asunto, y adquisiciones privadas por cada casado de dinero y valores mobiliarios, en el punto concreto de minusvalor de la adjudicación que asumió la actora, y nada se prueba cabal para aquilatar la cuarta parte respecto de la del demandado, y aunque no es rescindible el contrato divisorio, de serlo, tampoco procedería declararlo.

VI.- COSTAS.

El principio del vencimiento objetivo que se invoca de adverso, asentado en el art. 394 LEC, debe emplearse para pronunciar las costas del juicio a cargo de la parte actora, por haberse de desestimar en su integridad la demanda.

Por lo expuesto,

AL TRIBUNAL SUPLICO

que, teniendo por presentado este escrito, lo admita, me tenga por comparecido y parte en la representación que ostento, y por deducida, CONTESTACIÓN a la demanda interpuesta por D./Dña. [NOMBRE Y APELLIDOS] y seguido que sea todo el oportuno procedimiento, se sirva dictar en su día Sentencia por la que se desestime íntegramente la demanda, absolviendo al demandado, y pronuncie el abono de las costas procesales a cargo de la parte demandante.

Es justicia que pido en [LUGAR], a [FECHA].

OTROSÍ PRIMERO DIGO: Se han impugnado expresamente los dictámenes periciales emitidos por el Agente de la Propiedad Inmobiliaria D./Dña. [NOMBRE Y APELLIDOS], y por [NOMBRE Y APELLIDOS]., que se documentan y acompañan con la demanda, presentándose por esta parte, acerca del valor de las participaciones de [DENOMINACIÓN SOCIAL], dictamen del auditor censor jurado de cuentas D./Dña. [NOMBRE Y APELLIDOS] (DOC Nº [NÚMERO]).

Pero de acuerdo con lo dispuesto en el art. 339.2 LEC, interesa al derecho de esta parte designación judicial de perito, un Agente de la Propiedad Inmobiliaria, a fin de que valore el precio de mercado de la vivienda familiar, de [LOCALIDAD], en la fecha de la liquidación de autos, siendo ello pertinente y útil para el objeto litigioso, tanto en la medida que el dictamen pericial de la contraparte discute el valor de dicho inmueble adjudicado a la actora, como en la medida que esta parte no tiene acceso a la dicha vivienda, que no sólo es propiedad atribuída a la esposa, sino que detenta derecho de uso y disfrute exclusivo con la guarda de los hijos menores. Si se valorara la finca sólo por su aspecto externo y metros cuadrados de la zona, se incurriría en el mismo vicio que faculta para impugnar la pericia de contrario al documento nº [Nº DE DOCUMENTO] de la demanda.

OTROSÍ SEGUNDO DIGO: Que siendo general para pleitos el poder que presenta el Procurador/a suscrito, y precisándolo para otros usos.

Por lo expuesto,

AL TRIBUNAL SUPLICO que, teniendo por hechas las afirmaciones anteriores, y por presentada prueba pericial, y anunciada su proposición de prueba, proceda a designación judicial del perito indicado conforme al art. 339.2 LEC, así como se acuerde el desglose de la copia auténtica del poder para pleitos y la devolución a esta parte.

Es Justo en el mismo lugar y fecha arriba indicados.

Firma del Abogado	Firma del Procurador/a

========================================================================
