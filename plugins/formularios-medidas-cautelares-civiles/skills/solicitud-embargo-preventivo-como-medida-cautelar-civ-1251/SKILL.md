---
name: solicitud-embargo-preventivo-como-medida-cautelar-civ-1251
description: "Solicitud de embargo preventivo como medida cautelar en un procedimiento arbitral. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud de embargo preventivo como medida cautelar en un procedimiento arbitral

> Formulario **CIV-1251** del plugin **Medidas cautelares y diligencias preliminares** (`formularios-medidas-cautelares-civiles`) · Civil › Medidas cautelares y diligencias preliminares · normativa revisada el 24-11-2026.

## Qué es

Escrito de solicitud de medida cautelar de embargo preventivo ante el tribunal civil para asegurar la efectividad de la pretensión que se formulará en un procedimiento arbitral (arts. 11.3 de la Ley 60/2003 de Arbitraje y 721 y siguientes LEC), cuando ya se ha promovido la designación judicial de árbitro.

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud de embargo preventivo como medida cautelar en un procedimiento arbitral» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud de embargo preventivo como medida cautelar en un procedimiento arbitral” para mi caso». También puedes invocarla directamente con `/formularios-medidas-cautelares-civiles:solicitud-embargo-preventivo-como-medida-cautelar-civ-1251`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-medidas-cautelares-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Medidas cautelares y diligencias preliminares) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (13 veces)
- [ ] LOCALIDAD (12 veces)
- [ ] DENOMINACIÓN SOCIAL DE LA PARTE CONTRARIA (8 veces)
- [ ] MES (5 veces)
- [ ] AÑO (3 veces)
- [ ] DÍA (3 veces)
- [ ] IMPORTE (3 veces)
- [ ] FIRMA (2 veces)
- [ ] FOLIO (2 veces)
- [ ] LIBRO (2 veces)
- [ ] Nº DE FINCA (2 veces)
- [ ] NÚMERO DE LA CLÁUSULA (2 veces)
- [ ] TOMO (2 veces)
- [ ] DENOMINACIÓN SOCIAL DEL SOLICITANTE
- [ ] DOMICILIO
- [ ] IMPORTE EN LETRA
- [ ] IMPORTE EN NÚMERO
- [ ] NIF
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] Nº DE COLEGIADO
- [ ] Nº DE DOCUMENTO
- [ ] Nº DE PROCEDIMIENTO
- [ ] SEDE

## Normas que cita el formulario

- art. 9.2 LOPJ
- art. 85.1 LOPJ
- art. 722 LEC
- art. 727 LEC
- art. 726 LEC
- art. 728.1 LEC
- art. 728 LEC
- art. 732.2 LEC

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

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, que actúa en nombre y representación de [DENOMINACIÓN SOCIAL DEL SOLICITANTE], domiciliada en [LOCALIDAD], calle [DOMICILIO], con N.I.F. n.º [NIF], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento n.º [Nº DE DOCUMENTO], bajo la dirección del/de la Letrado/a en ejercicio, habilitado/a ante el Tribunal, del Ilustre Colegio de la Abogacía de [LOCALIDAD] (n.º [Nº DE COLEGIADO]), en los autos de Medida Cautelar Previa n.º [Nº DE PROCEDIMIENTO] comparezco y, como mejor en Derecho proceda, DIGO (véase nota 1):

Por medio del presente escrito, en la representación que ostento, vengo a deducir petición de medida cautelar de embargo preventivo para asegurar la efectividad de la pretensión que se formulará en procedimiento arbitral, cuya designación judicial de árbitro se ha promovido, con arreglo a la Ley 60/2003, de 23 de diciembre, de Arbitraje (LA), frente a [DENOMINACIÓN SOCIAL DE LA PARTE CONTRARIA], con base en las siguientes:

ALEGACIONES

PRIMERA.– Esta parte mantiene relaciones comerciales con la mercantil [DENOMINACIÓN SOCIAL DE LA PARTE CONTRARIA], que se han sujetado en todo momento a lo establecido en el contrato de [TIPO DE CONTRATO, por ejemplo, suministro de materiales para obra] suscrito entre las partes con fecha [DÍA] de [MES] de [AÑO], que, señalado como doc. n.º 1, se acompaña al presente escrito.

En el pacto [NÚMERO DE LA CLÁUSULA] del contrato las partes acordaron textualmente que, para la solución de cualquier cuestión litigiosa derivada del mismo, las partes se sometían a arbitraje de [ELEGIR: equidad / derecho] según lo establecido en la Ley 60/2003, de 23 de diciembre, de Arbitraje, y que, en caso de discrepancia respecto a la designación del árbitro, cualquiera de las partes podría instar el nombramiento de árbitro ante los tribunales.

SEGUNDA.– [DENOMINACIÓN SOCIAL DE LA PARTE CONTRARIA] adeuda a nuestro mandante la cantidad de [IMPORTE] euros, por [CONCEPTO DE LA DEUDA, por ejemplo, el precio de varios artículos defectuosos servidos entre los meses de [MES] y [MES] del presente año, pero facturados conforme a pedido y abonados contra efectos aceptados previamente].

Se acompaña cuadro explicativo de los objetos o conceptos reclamados, la fecha de pedido, de entrega, de factura, y sumatorios parciales y totales.

Están respaldados los datos por fotocopias de los documentos n.os [Nº] a [Nº].

TERCERA.– Al no ponerse de acuerdo las partes respecto de la liquidación de esta deuda, ni existiendo tampoco acuerdo respecto a la designación del árbitro que pudiera dirimir el conflicto surgido, nuestra representada no ha tenido más remedio que solicitar la designación judicial del árbitro, de conformidad con el art. 15 LA.

Así se acredita mediante el doc. n.º [Nº], que se acompaña, consistente en copia testimoniada del escrito presentado ante el Tribunal de Instancia de [LOCALIDAD] instando el nombramiento de árbitro para que dirima [ELEGIR: en equidad / en derecho] el conflicto surgido.

[OPCIONAL — incluir si procede: En todo caso, los artículos suministrados inservibles han sido devueltos a [DENOMINACIÓN SOCIAL DE LA PARTE CONTRARIA], por lo que tiene los bienes y su precio.]

CUARTA.– Nuestra representada ha tenido conocimiento de que la mercantil [DENOMINACIÓN SOCIAL DE LA PARTE CONTRARIA] ha vendido a terceras personas la parte más importante de su patrimonio conocido, que radicaba en [LOCALIDAD]. Así se acredita mediante la certificación del Registro de la Propiedad de [LOCALIDAD] que, señalada como doc. n.º [Nº], acompaño al presente escrito. Por otro lado, [DENOMINACIÓN SOCIAL DE LA PARTE CONTRARIA] ha cerrado el establecimiento mercantil que tenía abierto en [LOCALIDAD] (se acompañan dos actas notariales levantadas en horario comercial y en dos semanas consecutivas, que acreditan el cierre del establecimiento, como docs. n.os [Nº] y [Nº]). Además, la citada mercantil ha procedido a insertar anuncios en la prensa local ofertando la venta del inmueble cuyo embargo preventivo solicitamos, cuyas copias acompañamos señaladas como docs. n.os [Nº] y [Nº].

En la actualidad, y según ha podido averiguar nuestra representada, la sociedad deudora solo es titular de la finca registral n.º [Nº DE FINCA], inscrita al tomo [TOMO], libro [LIBRO], folio [FOLIO], tal y como se acredita mediante el doc. n.º [Nº], consistente en certificación del Registro de la Propiedad de [LOCALIDAD]. Teniendo en cuenta la celeridad con que se han producido las ventas anteriormente señaladas, y dado que existe un peligro cierto y real de que la citada mercantil se despatrimonialice totalmente durante la pendencia del proceso arbitral, haciendo con ello irrealizable (por carecer de otros bienes conocidos) el laudo que se dicte, procede la adopción de la medida cautelar solicitada, consistente en el embargo preventivo de la finca acabada de señalar.

FUNDAMENTOS DE DERECHO

I.– COMPETENCIA

No resulta dudosa la competencia genérica del orden civil de la jurisdicción para adoptar medida cautelar del procedimiento arbitral cuyo objeto pertenece a dicha materia (art. 9.2 LOPJ).

En cuanto a la competencia específica, la objetiva, funcional y territorial se resuelve en una sola regla, conforme a la cual es competente el Tribunal de Instancia del lugar en el que el laudo deba ser ejecutado y, en su defecto, el del lugar donde la medida cautelar deba producir su eficacia (arts. 8.3 LA y 724, párrafo primero, LEC, en relación con lo dispuesto en el art. 85.1 LOPJ), supuesto que se encuentra pendiente un procedimiento arbitral. En el presente supuesto, el laudo ha de ser ejecutado en el municipio de [LOCALIDAD], lugar en el que radica el inmueble objeto de la medida solicitada.

II.– PARTES

Quien acredite ser parte en convenio arbitral con anterioridad a las actuaciones arbitrales, las partes en proceso arbitral pendiente que han presentado solicitud o encargo a una institución o, como en el caso, que hayan pedido la designación judicial de árbitro, están legitimadas procesalmente para pedir de los tribunales medidas cautelares (art. 722, párrafo primero, LEC), y lo están en sentido material como partes contratantes en el contrato entre sociedades en cuya cláusula [NÚMERO DE LA CLÁUSULA] se encuentra el compromiso arbitral que ha dado lugar a la solicitud.

III.– PROCEDIMIENTO

La medida solicitada es alguna de las previstas en el art. 727 LEC, concretamente la 1.ª del precepto, que reúne los rasgos de temporalidad, provisionalidad, instrumentalidad, susceptibilidad de modificación y alzamiento, y posible sustitución por otras menos onerosas para el demandado (art. 726 LEC), y en todo caso resulta idónea y congruente con la pretensión cuya efectividad se desea asegurar.

El caso es de embargo preventivo en aseguramiento del resultado del procedimiento arbitral cuya formalización judicial se ha promovido.

IV.– PRESUPUESTOS MATERIALES

Conforme al art. 11.3 LA, el convenio arbitral no puede impedir que las partes, con anterioridad a las actuaciones arbitrales o durante su tramitación, soliciten de los tribunales competentes la adopción de medidas cautelares, ni que estos las acuerden.

Art. 728 LEC. La parte solicitante debe acreditar el peligro de mora procesal, es decir, el riesgo de la demora o la infructuosidad de la tutela judicial que en su día pudiera merecerse (periculum in mora), y que le asiste una apariencia de buen derecho, es decir, que, sin prejuzgar el fondo del asunto, sea positivo el juicio indiciario de la existencia del derecho reclamado (fumus boni iuris).

— Fumus boni iuris. Los elementos documentales que se aportan por el solicitante acreditan preliminarmente ese juicio provisional e indiciario favorable al fundamento de la pretensión principal, que es punto medio entre la pura incertidumbre y la certeza plena que solo se podrá alcanzar formalmente al término del procedimiento arbitral.

— Periculum in mora. El peligro de retraso resulta demostrado sencillamente por la constancia de la enajenación acelerada de activos inmuebles por [DENOMINACIÓN SOCIAL DE LA PARTE CONTRARIA], el cierre del establecimiento en [LOCALIDAD] y el anuncio de la venta de la última finca de propiedad de aquella, y puesto que, de no adoptarse la medida, durante la pendencia del proceso de formalización judicial y hasta la emisión del laudo arbitral, la deudora puede despatrimonializarse sin dificultad, impidiéndose la efectividad de la tutela que pudiera otorgarse a la firmeza de tal laudo, sin que en este peligro se haya colocado por su negligencia la parte solicitante, según destaca el art. 728.1, párrafo segundo, LEC.

— Caución. Para la ejecución de la medida es menester que esta parte solicitante ofrezca caución suficiente para responder, de forma rápida y eficaz, de los daños y perjuicios que pudieran ocasionarse (art. 728 LEC). Los criterios para determinar su cuantía, forma y plazo son la importancia real de la pretensión que se quiere asegurar, que es cumplimiento de obligación pecuniaria de suma conocida, y el fundamento del derecho reclamado, que ya ha quedado expreso, por lo que estima esta parte procedente la caución de [IMPORTE EN LETRA] euros ([IMPORTE EN NÚMERO] €), suficiente, sin perjuicio de lo que determine S.S.ª.

La caución se ofrece prestar en la modalidad de aval bancario, solidario, de duración indefinida y pagadero a primer requerimiento por entidad de crédito, a resultas de este proceso, para el plazo que conceda el Tribunal.

En su virtud,

SUPLICO AL TRIBUNAL

que, por presentado este escrito, junto con los documentos que se acompañan y copia de todo ello, se me tenga por comparecido/a y parte en la representación que ostento, se sirva admitirlo y, estimando la solicitud de adopción de medida cautelar del procedimiento de designación judicial de árbitro que se tiene instada, se acuerde el embargo preventivo de la finca n.º [Nº DE FINCA], al tomo [TOMO], libro [LIBRO], folio [FOLIO], del Registro de la Propiedad n.º [Nº] de [LOCALIDAD], de titularidad de [DENOMINACIÓN SOCIAL DE LA PARTE CONTRARIA], por la cantidad de [IMPORTE] euros, bajo la caución que se ofrece, de [IMPORTE] euros, mediante aval bancario, o la de cuantía y forma que determine S.S.ª.

Es de Justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

OTROSÍ PRIMERO DIGO: Esta solicitante señala expresamente como prueba de la que se vale los documentos acompañados con este escrito (art. 732.2 LEC), específicamente los numerados del 2 al [Nº] como demostración material del crédito, y los que llevan números [Nº] a [Nº] como acreditación de la insolvencia y del fraude del sujeto pasivo de la medida solicitada.

SUPLICO AL TRIBUNAL que, teniendo por causada la anterior manifestación a los efectos oportunos, se digne resolver de conformidad con lo interesado, como es Justicia de hacerse en lugar y fecha ut supra.

Por ser de Justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Abogado/a: [FIRMA] Firma del Procurador/a: [FIRMA]

NOTA 1

El escrito es perfectamente aplicable al caso de conflicto cuya efectividad de solución arbitral deba cautelarse, bien porque, en lugar de designación judicial de árbitros, se acredite ser parte de convenio arbitral con anterioridad a las actuaciones arbitrales, se haya efectuado solicitud o encargo a determinada institución, o bien porque las actuaciones arbitrales ya estén en trámite.

Lo que ocurre es que la Ley de Arbitraje (art. 23) prevé la potestad de los árbitros de adoptar medidas cautelares, exigiendo en su caso caución al solicitante, siempre que no lo excluya el convenio arbitral o el procedimiento ad hoc que esté acordado. Entonces, una solicitud semejante, menos formal y sin prevenciones legales expresas, se podría hacer al árbitro. La resolución arbitral cautelar se sujeta a anulación y ejecución forzosa como un laudo.

También podría incluirse en el escrito la oferta de caución con aportación de la misma (consignando una cifra, adjuntando el aval, etc.), pero no parece que se exija por los arts. 728.3 y 732.3 LEC y, puesto que la suma y el modo de la caución es determinación del tribunal, que además puede denegar sencillamente la medida, resulta más conducente la no aportación y estar preparado para cumplir el mandato condicional del tribunal en cuanto se notifique la decisión. Lo único que imposibilita la estimación de la medida es la negativa rotunda por el sujeto activo al deber de prestar caución.
