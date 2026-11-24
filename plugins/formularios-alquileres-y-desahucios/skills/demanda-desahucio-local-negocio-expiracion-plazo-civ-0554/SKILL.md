---
name: demanda-desahucio-local-negocio-expiracion-plazo-civ-0554
description: "Demanda de desahucio de local de negocio por expiración del plazo del contrato. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de desahucio de local de negocio por expiración del plazo del contrato

> Formulario **CIV-0554** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 24-11-2026.

## Qué es

Parte HECHOS FUNDAMENTOS DE DERECHO Suplico de presentación de demanda Otrosí de cuantía Otrosí para designar domicilio en caso de actos de comunicación y solicitud de práctica de requerimiento Otrosí de Vigentecitadisposición adicional quinta de la LEC Otrosí sobre las circunstancias de enervación correlativo al fundamento de la demanda Otrosí de compromiso de condonación toital o parcial correlativo al fundamento de la demanda Otrosí de Tasa Suplico Firmas

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de desahucio de local de negocio por expiración del plazo del contrato» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de desahucio de local de negocio por expiración del plazo del contrato” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:demanda-desahucio-local-negocio-expiracion-plazo-civ-0554`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] CALLE (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] AÑO
- [ ] DÍA
- [ ] FOLIO
- [ ] LIBRO
- [ ] LUGAR
- [ ] MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] MES
- [ ] Nº
- [ ] Nº DE CLÁUSULA
- [ ] PLAZO
- [ ] TOMO

## Normas que cita el formulario

- art. 250.1.1 LEC
- art. 437.1 LEC
- art. 5 Ley Orgánica 1/2025
- art. 1566 Código Civil
- art. 1566 CC
- art. 437 LEC
- art. 394 LEC
- art. 251 LEC
- art. 155 LEC
- art. 161 LEC
- art. 21 LEC
- art. 7.2 Ley 10/2012

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE Q.P.T.R.C.»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE Q.P.T.R.C.

Don [NOMBRE Y APELLIDOS], Procurador de los Tribunales, en nombre y representación de Don [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], según acredito con la copia electrónica del poder notarial de representación informática (o digitalizada) general para pleitos que acompaño y cuya devolución solicito previa unión a los autos de testimonio suficiente, por ser necesaria para otros usos ( o mediante apoderamiento apud-acta otorgado ante el Letrado de la Administración de Justicia que acompaño), ante el Tribunal comparezco y DIGO:

Que formulo demanda de juicio verbal de resolución de contrato de arrendamiento por expiración del plazo contractual contra Don [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], y fundo mi pretensión en los siguientes:

HECHOS

Primero.- Mi mandante es usufructuario (o es dueño, ostenta un derecho de posesión de la finca o es causahabiente de los anteriores) de la finca urbana sita en esta ciudad, calle [CALLE], nº [NÚMERO] inscrita en el Registro de la Propiedad de [LOCALIDAD], Libro [LIBRO], Tomo [TOMO] Folio [FOLIO] Adjunto copia de la escritura pública, como doc. nº 1.

Segundo.- El local de negocio sito en los bajos de la citada finca, y descrito en la escritura como «Entidad B- local » fue cedido por mi principal en arrendamiento al demandado en virtud de contrato de fecha

Este arrendamiento se pactó durante un plazo de cinco años y vencía, transcurrido el plazo, en la fecha de celebración del contrato por ser ésta la en que se puso el local a disposición del arrendatario. En la cláusula [Nº DE CLÁUSULA] se hizo constar expresamente que transcurrido el plazo finalizaría el contrato, sin perjuicio de que ambas partes, de común acuerdo, pudieran prorrogar la relación arrendaticia o celebrar nuevo contrato. Adjunto contrato de arrendamiento como doc. nº 2.

Tercero.- Que mi representado no tiene interés en prorrogar el contrato ni en celebrar otro nuevo por lo que con más de un mes de antelación a su vencimiento se puso en contacto con el demandado a fin de hacerle saber la próxima finalización y la obligación de éste de poner a disposición de mi principal el citado local, libre, vacuo y expedito (acompaño copia del requerimiento notarial - o acto de conciliación, etc.- como doc. nº 3).

Cuarto.- No obstante el demandado ha hecho caso omiso a esta pretensión y se ha negado a poner a disposición del arrendador el citado local a la fecha de la finalización, por lo que mi principal se ve obligado a interponer esta demanda.

Quinto.- Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento nº [Nº DE DOCUMENTO]

A estos hechos son de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

Primero.- La pretensión que se ejercita queda amparada en el art. 250.1.1ª de la LEC que tutela la recuperación de la posesión de una finca, dada en arrendamiento, por expiración del plazo contractual y que conforme al mismo precepto se seguirá por los trámites del juicio verbal.

Segundo.- Corresponde la competencia para conocer de esta clase de procesos al Tribunal de Instancia del lugar en que se halle la finca a tenor de lo establecido en el artículo 45, 47 y 52.1.7º de la LEC, al cual me dirijo.

Tercero.- El demandante tiene legitimación activa por ser el arrendador de la vivienda y el demandado está legitimado pasivamente por ostentar la cualidad de arrendatario tal como consta en el contrato aportado como documento nº 2.

Cuarto.- La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC en relación con el art. 437.1 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

Quinto.- Al tratarse de un arrendamiento para uso distinto del de vivienda la duración es la pactada en el contrato, de acuerdo con lo que dispone la Ley 29/1994, de 24 de noviembre, debiéndose estar, pues, a lo establecido en el art. 1566 del Código Civil tal como viene interpretado por la SAP de Málaga, de 3 de mayo de 2007, rec. 77/2007, por aplicación de los artículos 1566 y 1581 del CC es necesario el requerimiento previo a la acción judicial para que se ponga fin a la tácita reconducción, con cita de la STS de 15 de octubre de 1996, rec. 4027/1992, y las que en ella se citan de 14 de junio de 1984 y 21 de febrero de 1985. Conforme a este precepto mi mandante requirió con más de un mes de antelación al arrendatario a fin de poner en su conocimiento su intención de dar por extinguido el arrendamiento y evitar la tácita reconducción.

Por otra parte el hecho de que durante el tiempo que ha transcurrido, desde la expiración del plazo y la presentación de la demanda, el arrendatario haya venido satisfaciendo las cantidades correspondientes a la renta abonada durante la vigencia del contrato no implica que se haya prorrogado el arrendamiento, pues la STS de 10 de mayo de 1950 declara que los actos posteriores al requerimiento que priven de efecto al mismo, deben constar, como en toda renuncia de derechos, de modo claro e inequívoco, extremos que aquí no concurren.

Respecto al hecho de que el arrendador siga cobrando una o más mensualidades cabe afirmar que no es equiparable a una renuncia al derecho del arrendador a dar por extinguido el contrato de arrendamiento [SSTS de 27 de mayo de 1968 y de 2 de marzo de 1993, rec. 2415/1990], ya que con estos ingresos se evita el enriquecimiento injusto de una de las partes a costa de la otra, puesto que mientras no desalojen los arrendatarios el local o vivienda son ellos quienes tienen la posesión del objeto arrendado y no el arrendador. En este sentido podemos citar la SAP de Granada, de 11 de junio de 2001, rec. 220/2001.

Sexto.- Al amparo del apartado 3 del artículo 437 de la LEC, el arrendador anuncia en esta demanda que asume el compromiso de condonar al arrendatario toda la deuda (o parte de la deuda si fuera el caso), que asciende a la cantidad de [IMPORTE] euros, así como las costas, siempre que el arrendatario desaloje voluntariamente la vivienda dejándola vacua, libre y expedita a disposición de mi mandante dentro del plazo de [Nº] días ( no inferior a quince días), lo que deberá ponerse de manifiesto al demandado en el requerimiento que se realice para manifestar su aceptación a este compromiso, lo cual equivaldrá a un allanamiento.

Séptimo.- Con arreglo a lo establecido en el art. 394 de la LEC procede imponer las costas de este proceso a la parte demandada en tanto que es la actitud del demandado de no cumplir con lo pactado la que obliga a esta parte a presentar la demanda.

Por cuanto antecede:

SUPLICO AL TRIBUNAL: Que tenga por presentada esta demanda, con su copia y documentos que la acompañan, que la admita y que me tenga por personado y parte en la representación que ostento de Don [NOMBRE Y APELLIDOS] en virtud de la copia electrónica del poder notarial de representación informática (o digitalizada) general para pleitos cuya devolución intereso previa unión a los autos de copia testimoniada (o designa apud acta), que se entiendan conmigo las sucesivas diligencias y que se tenga por formulada demanda de juicio verbal de desahucio por expiración del plazo contractual del local objeto de este proceso, contra Don [NOMBRE Y APELLIDOS], y que se señale día y hora para la celebración del juicio verbal con citación al demandado, apercibiéndole de que no comparecer a la vista se declarará el deshaucio sin más trámites y que queda citado para recibir la notificación de la sentencia el sexto día siguiente al señalada para la vista, señalando asimismo día y hora para que tenga lugar, en su caso, el lanzamiento, así como que, en su día, se dicte sentencia por la que se estime esta demanda de desahucio por expiración del plazo contractual de cinco años, se declare resuelto el contrato de arrendamiento objeto de este proceso y se condene al demandado a dejar libre y expedito y a disposición de mi mandante el local de negocio arrendado, con apercibimiento de lanzamiento si no lo llevara a cabo y con expresa imposición de costas.

OTROSÍ PRIMERO DIGO: Que fijo la cuantía del proceso en [IMPORTE] euros, cantidad que corresponde a una anualidad de renta por aplicación de la regla 9ª del art. 251 de la LEC.

OTROSÍ SEGUNDO DIGO: Que al amparo del segundo párrafo del art. 155 designo como domicilio del demandado a efectos de comunicación, el del local arrendado.

OTROSÍ TERCERO DIGO: Que al amparo del apartado 3 del art. 155 de la LEC designo como domicilio del demandado, a efectos de actos de comunicación, el de la local arrendado sito en la calle [CALLE], nº [NÚMERO], de esta Ciudad, al no haberse señalado otro domicilio para actos de comunicación en el contrato, interesando asimismo, al amparo del primer párrafo del apartado tercero del artículo 161 de la LEC y teniendo en cuenta que el domicilio donde se ha de practicar la comunicación es el inmueble arrendado al demandado, si en el momento de practicar la comunicación no se encontrare allí dicho destinatario, se efectúe la entrega a cualquier empleado o familiar mayor de 14 años, que se encuentre en ese lugar, o al conserje de la finca, si lo tuviere, advirtiendo al receptor que está obligado a entregar la copia de la resolución o la cédula al destinatario de ésta o a darle aviso, si sabe su paradero.

OTROSÍ CUARTO DIGO: Que al amparo de la disposición adicional quinta de la LEC, intereso de la Oficina de Señalamiento Inmediato que entregue al Procurador de esta parte las citaciones y cédulas que expida con el fin de realizar los actos de comunicación a costa de esta parte en los términos que la norma citada dispone que, una vez cumplimentadas, serán aportadas ante el Tribunal al que por turno corresponda el conocimiento de esta demanda

SUPLICO AL TRIBUNAL: Que tenga que acuerde de conformidad.

OTROSÍ QUINTO DIGO: Que habiendo adquirido mi mandante en la demanda el compromiso de condonar al arrendatario toda la deuda reclamada, incluso las rentas no vencidas hasta el momento mismo del desalojo voluntario de la vivienda, y de las costas, con la condición de que dicho desalojo voluntario que tenga lugar en el plazo no inferior a quince días y no superior a [PLAZO] a contar desde que se le notifique la demanda, al amparo del apartado 3 del art. 437 la LEC, intereso que se requiera al demandado a fin de que manifieste si acepta este compromiso con la indicación de que su aceptación equivaldrá a un allanamiento con los efectos del art. 21 de la LEC, condonación que comprenderá la cuantía señalada en el Fundamento de Derecho sexto de esta demanda.

OTROSÍ SEXTO.-Que estando la presente demanda sujeta al abono de la tasa por el ejercicio de la potestad jurisdiccional fijada por la Ley 10/2012, de 20 de noviembre, modificada por Real Decreto Ley 3/2013, de 22 de febrero, y Ley 25/2015, de 28 julio, y por Orden HAP/861/2015, de 7 de mayo, siendo mi representada persona jurídica no exenta, se acompaña a la presente demanda como documento nº [Nº DE DOCUMENTO] la correspondiente autoliquidación con el ejemplar para la Administración de Justicia debidamente validado y en el que consta el pago de la cantidad de 150 euros correspondiente a la cuota fija, sin que se incluya la cuota variable prevista en el artículo 7.2 de la Ley 10/2012 al haber sido declarado inconstitucional y nulo por la STC 140/2016, de 21 de julio.

En virtud de lo anterior,

SUPLICO AL TRIBUNAL: que tenga por hecha la anterior manifestación a los efectos pertinentes y por acompañado el documento justificativo del abono de la tasa.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma Abogado Firma Procurador

========================================================================
