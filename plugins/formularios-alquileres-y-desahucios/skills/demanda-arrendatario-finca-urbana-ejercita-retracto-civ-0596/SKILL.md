---
name: demanda-arrendatario-finca-urbana-ejercita-retracto-civ-0596
description: "Demanda del arrendatario de finca urbana que ejercita el retracto contra el comprador. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda del arrendatario de finca urbana que ejercita el retracto contra el comprador

> Formulario **CIV-0596** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 24-11-2026.

## Qué es

Modelo de demanda de juicio ordinario por la que se ejercita, por el arrendatario de una finca urbana, la acción de retracto frente al comprador, previo requerimiento notarial. A la demanda le acompaña el resguardo acreditativo de la consignación del precio de la compraventa, así como la caución que garantiza la consignación en cuanto a gastos debidos.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda del arrendatario de finca urbana que ejercita el retracto contra el comprador» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda del arrendatario de finca urbana que ejercita el retracto contra el comprador” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:demanda-arrendatario-finca-urbana-ejercita-retracto-civ-0596`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (11 veces)
- [ ] NÚMERO (5 veces)
- [ ] FECHA (3 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] IMPORTE (2 veces)
- [ ] CALLE
- [ ] FECHAS
- [ ] IMPORTE EN CIFRA
- [ ] LUGAR
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] SEDE

## Normas que cita el formulario

- art. 52.1.1.º LEC
- art. 36.1 LEC
- art. 13 LEC
- art. 266.2.º LEC
- art. 269.2 LEC
- art. 5 Ley Orgánica 1/2025
- art. 253.1 LEC
- art. 23 LEC
- art. 25 LAU
- art. 1.518 CC
- art. 1.521 CC
- art. 25.3 LAU
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

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a. de los Tribunales, en nombre y representación de [NOMBRE DEL REPRESENTADO/A], con domicilio en [LOCALIDAD], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], dirigido por Abogado ejerciente, D./Dña. [NOMBRE Y APELLIDOS], con despacho profesional en esta capital sito en [LOCALIDAD], ante el Tribunal comparezco y como mejor proceda en derecho, DIGO:

Que mediante el presente escrito y en nombre de mi mandante formulo demanda de juicio ordinario, sobre acción de retracto contra D./Dña. [NOMBRE Y APELLIDOS]

HECHOS

PRIMERO.- El demandante es arrendatario de la vivienda sita en esta población [LOCALIDAD], calle [CALLE], en virtud de contrato de arrendamiento, como se acredita con el documento n.º [NÚMERO].

SEGUNDO.- Con fecha [FECHA] el arrendador propietario de dicha vivienda, D./Dña. [NOMBRE Y APELLIDOS], ha notificado a mi mandante por carta certificada con acuse de recibo (documento n.º [NÚMERO]) que había vendido la finca arrendada, detallando los pormenores, precio y condiciones de la transmisión, así como las circunstancias personales del que era adquirente de dicha vivienda contra el cual se dirige esta demanda, D./Dña. [NOMBRE Y APELLIDOS]

TERCERO.- Mi patrocinado procedió a requerir notarialmente al comprador D./Dña. [NOMBRE Y APELLIDOS], de forma que se hacía constar que no se le había notificado ni anunciado la venta para poder ejercitar sus derechos de adquisición preferente, debiendo aceptar como cierto el hecho de la compra y el precio (Se adjunta copia auténtica del acta como documento n.º [NÚMERO]).

CUARTO.- Se ha procedido el mismo día de la interposición de este escrito a consignar el precio de la compraventa, así como la caución que garantiza la consignación en cuanto a gastos debidos, como se demuestra con el resguardo del abonaré realizado en la cuenta del Tribunal decano, que se adjunta como documento n.º [NÚMERO].

QUINTO.- La parte actora manifiesta que, previo a la presentación de la presente demanda, se han llevaron a cabo negociaciones con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad, y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria; incluyéndose entre las acciones realizadas el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución.

Finalmente, mi representado envío un requerimiento fehaciente al demandado con fecha [FECHA], fijando un plazo de 30 días naturales para llegar a un acuerdo amistoso, a través del abogado que firma este escrito, el cual fue contestado por el demandado por el mismo medio, rechazando el acuerdo/ habiendo sido solo posible un acuerdo parcial, viéndonos en la necesidad de acudir a la presente vía judicial, respecto a los extremos de la controversia en los que se mantiene la discrepancia.

Acompaño como documento nº [Nº DE DOCUMENTO], el requerimiento efectuado y como documento nº [Nº DE DOCUMENTO], la contestación del demandado.

A los anteriores hechos son de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN Y COMPETENCIA.

Es de aplicación el art. 52.1.1.º LEC, para la competencia territorial, en cuanto que se ejercita una acción real sobre bien inmueble, y el Tribunal al que me dirijo es el del lugar en que está sito aquél. Y en cuanto a la jurisdicción y competencia genérica y objetiva, citamos los arts. 9.2, 21.1 y 85.1 LOPJ y arts. 36.1 y 45 LEC.

II.- PROCEDIMIENTO.

Art. 249.1.7.º LEC, que ordena sustanciar las pretensiones de retracto de cualquier tipo a través del juicio ordinario.

III.- LEGITIMACIÓN ACTIVA Y PASIVA.

La legitimación activa corresponde a mi poderdante como titular del derecho de retracto, en su condición de arrendatario, y corresponde pasivamente al demandado, como adquirente del inmueble.

Respecto a la válida constitución de la relación jurídico procesal en los supuestos de ejercicio de la acción de retracto, la doctrina jurisprudencial, SSTS de 7 de mayo de 1927, 28 de abril de 1953, 11 de enero de 1977, 24 de mayo de 1986, 30 de enero de 1989, 11 de mayo de 1992, viene a establecer que esa acción real se ha de dirigir contra quien haya adquirido la cosa arrendada, ya que de prosperar el retracto se colocará el retrayente en el lugar del comprador, sin necesidad de otorgar nuevo contrato puesto que la compraventa no se resuelve sino que simplemente queda modificada subjetivamente por el cambio de la persona del comprador.

Solamente la existencia de transmisiones posteriores a la fecha de interposición de la demanda impone dirigirla conjuntamente contra los dos adquirentes, y al margen de la intervención voluntaria adhesiva que pueda pedir ex art. 13 LEC el vendedor.

IV.- PRESUPUESTOS PROCESALES.

Se han llenado, en atención al art. 266.2.º LEC los requisitos específicos de acreditación preliminar de la legitimación mediante determinados documentos, que son presupuesto de admisión (art. 269.2 LEC), y así se acompañan: el contrato de arrendamiento que constituye un principio de prueba del título en que se funda el derecho de retracto (documento n.º [NÚMERO]), y el documento que acredita haber consignado el precio que exige la ley y lo que se calcula para liquidación de gastos debidos.

La presente demanda cumple asimismo con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 de la LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

V.- CUANTÍA.

Cumpliendo lo prevenido en el art. 253.1 LEC, puesto que la importancia económica del pleito es determinable, hacemos constar que la cuantía de esta demanda es la de [IMPORTE] euros ([IMPORTE EN CIFRA] €), que resulta el precio de la vivienda consignado en la escritura pública de compraventa —superior al valor catastral—, en armonía con el art. 251.3.ª.4.º LEC.

VI.- POSTULACION Y DEFENSA.

Se cumplen en la presente demanda lo dispuesto en los arts. 23 y 31 LEC, en cuanto a la representación procesal mediante Procurador/a. de los Tribunales habilitado en el Tribunal y a la dirección técnica de Abogado colegiado, que elabora y suscribe la presente demanda.

VII.- FONDO DEL ASUNTO.

Se funda esta demanda en el art. 25 LAU 1994, en cuanto establece que en caso de venta de la vivienda arrendada tendrá el arrendatario derecho de adquisición preferente de la misma, especificándose en el apartado 3 que podrá el arrendatario ejercitar el derecho de retracto, con sujeción a lo dispuesto en el art. 1.518 CCiv, adquiriendo la finca con preferencia a cualquier otra persona por el precio indicado en la escritura pública indicada.

El derecho de retracto es un derecho de adquisición preferente que requiere para su ejercicio la previa concurrencia de una compraventa o dación en pago, y consiste en el derecho a favor de quien es tercero a dicho contrato que le autoriza a adquirir la cosa dada o vendida mediante la subrogación en el lugar del adquirente conforme al contrato, en las mismas condiciones estipuladas (cfr.: art. 1.521 CCiv), que la jurisprudencia viene entendiendo son cargas legales del derecho de propiedad por razones de interés general, aunque en beneficio de particulares.

La pretensión para la efectividad de tal derecho consiste en la de condena a la entrega del bien vendido, previa declaración del derecho preferente a adquirirlo y abono de su precio y demás gastos debidos.

El derecho de retracto supone reembolso al comprador del precio de venta, y además: a) los gastos del contrato y cualquier otro pago legítimo hecho para la venta, y b) los gastos necesarios y útiles hechos en la cosa vendida (arts. 1.518 y 1.525 CCiv), sin que haya obligación legal de reembolso de cantidad alguna por intereses de tal precio [STS de 14 de abril de 1989].

Se cumple en esta demanda y así resulta de la documental aportada que la pretensión se formula antes de que transcurra el plazo de caducidad a que se refiere el art. 25.3 LAU 1994 de treinta días naturales, a contar desde la notificación de la venta por el arrendador.

VIII.- COSTAS.

Conforme al art. 394 LEC las costas han de imponerse a la parte demandada.

Por lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentada esta demanda con sus documentos y copias la admita a trámite teniéndome por comparecido y parte en la representación que ostento; acordando dar traslado al demandado para que comparezca y la conteste, y previos los trámites legales de la audiencia previa y el acto del juicio, se dicte en su día sentencia por la que estimando la demanda, previa declaración del derecho de retracto del actor D./Dña. [NOMBRE Y APELLIDOS] sobre la vivienda descrita en el cuerpo de esta demanda, subrogado en la venta por D./Dña. [NOMBRE Y APELLIDOS] al demandado D./Dña. [NOMBRE Y APELLIDOS] en fechay por precio de [IMPORTE], condene a D./Dña. [NOMBRE Y APELLIDOS] a estar y pasar por dicha declaración, y a la entrega de dicha vivienda al demandante, librándose mandamientos, al Registro de la Propiedad para la inscripción del derecho del actor, y de devolución de la cuenta de consignaciones del Tribunal a D./Dña. [NOMBRE Y APELLIDOS], por el precio y gastos debidos que se liquiden.

Todo ello con expresa imposición de costas a la parte demandada, y lo demás que sea

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a

========================================================================
