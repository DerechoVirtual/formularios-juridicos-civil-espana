---
name: solicitud-ejecucion-cambiaria-falta-oposicion-deudor-civ-1183
description: "Solicitud de ejecución cambiaria por falta de oposición del deudor, con embargo de bien ganancial. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud de ejecución cambiaria por falta de oposición del deudor, con embargo de bien ganancial

> Formulario **CIV-1183** del plugin **Cobrar deudas: monitorio y cambiario** (`formularios-reclamar-deudas-monitorio`) · Civil › Monitorio y cambiario · normativa revisada el 24-11-2026.

## Qué es

Escrito solicitando el inicio de la ejecución de título cambiario al no haber deducido oposición el deudor dentro del plazo conferido tras la formulación de la demanda de juicio cambiario.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud de ejecución cambiaria por falta de oposición del deudor, con embargo de bien ganancial» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud de ejecución cambiaria por falta de oposición del deudor, con embargo de bien ganancial” para mi caso». También puedes invocarla directamente con `/formularios-reclamar-deudas-monitorio:solicitud-ejecucion-cambiaria-falta-oposicion-deudor-civ-1183`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-reclamar-deudas-monitorio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Cobrar deudas: monitorio y cambiario) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (14 veces)
- [ ] IMPORTE (7 veces)
- [ ] FECHA (6 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] NÚMERO (4 veces)
- [ ] AÑO (2 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] LUGAR (2 veces)
- [ ] NOMBRE DE LA PARTE (2 veces)
- [ ] Nº DE PABELLÓN (2 veces)
- [ ] Nº DE POLÍGONO (2 veces)
- [ ] Nº DE PROCEDIMIENTO (2 veces)
- [ ] CALLE
- [ ] DNI/NIE
- [ ] DOMICILIO
- [ ] FECHA DE VENCIMIENTO
- [ ] FOLIO
- [ ] LIBRO
- [ ] NOMBRE DEL LIBRADOR
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] SEDE
- [ ] TOMO

## Normas que cita el formulario

- art. 821 LEC
- art. 549.2 LEC
- art. 575.1 LEC
- art. 825 LEC
- art. 613.4 LEC
- art. 584 LEC
- art. 612.1 LEC
- art. 541 LEC

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
(1) Igual que en el juicio monitorio, la LEC ha considerado innecesaria o implícita la solicitud de apertura del proceso de ejecución en el juicio cambiario, desde la petición misma del inicio de éste. Lo mismo se considera innecesario el dictado de un título ejecutivo ‘ex proffeso’, y se produce por el complejo del título cambiario + resolución judicial que acuerda las medidas del art. 821 LEC + no oposición del deudor requerido. La idea es el despacho de ejecución automático, sin precisión de ninguna demanda ejecutiva. Y el art. 825, párrafo 2.º LEC remite para la sustanciación de la ejecución despachada a lo prevenido en la LEC para la de sentencias y resoluciones judiciales.

En algunos Tribunales, de todas las formas, se viene requiriendo la formulación de demanda ejecutiva, entendido que el tiempo verbal futuro en modo pasivo —’se despachará’— no supone actuación de oficio de suyo, y no cabe duda que una petición de inicio del proceso de ejecución, en cuanto que proceso distinto del declarativo especial sumario documental, es conveniente —en otro caso, debería producirse un escrito subsecuente al despacho de oficio—, a fin de determinar bienes del ejecutado susceptibles de embargo, interesar medidas de localización e investigación de patrimonio, o incluso pedir que la ejecución se dirija frente a los que aparecen en el título cambiario como deudores, por ejemplo avalistas, frente a los que deben responder conforme arts. 543 y 544 LEC, o pedir la notificación del embargo al cónyuge del deudor.

(2) Para la mejor comprensión del formulario, en la elaboración del mismo se han utilizado nombre y personas ficticias.

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

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales y de [NOMBRE DEL REPRESENTADO/A], como tengo debidamente acreditado mediante escritura de poder que obra en autos de juicio CAMBIARIO n.º [Nº DE PROCEDIMIENTO]/[AÑO], seguido en ese Tribunal frente a D./Dña. [NOMBRE Y APELLIDOS], a instancias de mi poderdante, comparezco y como mejor en Derecho proceda, DIGO:

Que interesa a mi patrocinada obtener la ejecución, con arreglo a los arts. 825 y 517 y ss. LEC, de título cambiario frente a D./Dña. [NOMBRE Y APELLIDOS], provisto de DNI n.º [DNI/NIE], domiciliado en [DOMICILIO], calle [CALLE], n.º [NÚMERO], siendo la empresa para la que trabaja [DENOMINACIÓN SOCIAL], sita en [LOCALIDAD], polígono [Nº DE POLÍGONO], pabellón [Nº DE PABELLÓN], lo cual se establece subsidiariamente para los actos de comunicación, si no fuere hallado en el domicilio, con base en los siguientes:

HECHOS

PRIMERO.- En la representación que ostento de [NOMBRE DE LA PARTE], formulé demanda de juicio cambiario contra D./Dña. [NOMBRE Y APELLIDOS], basada en un pagaré de fecha [FECHA] de [NOMBRE DEL LIBRADOR], n.º [NÚMERO], por importe de [IMPORTE] euros ( [IMPORTE] euros), que obra en autos.

SEGUNDO.- Con fecha [FECHA] se requirió de pago al deudor conforme a lo dispuesto en el art. 821 LEC, concediéndole plazo de diez días para deducir su oposición, sin que, en dicho plazo la haya deducido.

TERCERO.- D./Dña. [NOMBRE Y APELLIDOS] no ha satisfecho cantidad alguna a que viene obligado por el pagaré de referencia, y el art. 549.2 LEC autoriza a que la demanda ejecutiva se limite en estos casos a la solicitud de que se despache ejecución, identificando la resolución cuya ejecución se pretende, que es el auto de [FECHA], seguido del silencio del requerido.

CUARTO.- A la fecha de esta presentación, adeuda D./Dña. [NOMBRE Y APELLIDOS]

-Principal de [IMPORTE] euros ( euros)

-Intereses devengados sobre el principal desde el día de vencimiento, [FECHA DE VENCIMIENTO], al tipo legal del dinero incrementado en dos puntos, de [IMPORTE] euros ( euros)

Total por principal e intereses vencidos de [IMPORTE] euros ( euros)

Presupuesto para intereses por devengar y costas, dentro de los límites del art. 575.1 LEC: [IMPORTE] euros ( euros).

QUINTO.- El título jurisdiccional citado es ejecutivo, junto con el pagaré, con arreglo a lo dispuesto en el art. 825 LEC, por relación al art. 517.2. 1.º y 9.º, puesto que si transcurridos dies días desde el requerimiento de pago, el deudor no ha formulado demanda de oposición, debe despacharse ejecución por las cantidades reclamadas, y se trabará embargo si no se hubiere trabado o si se hubiere alzado.

SEXTO.- En la diligencia del día [FECHA] se decretó embargo de finca rústica a nombre de D./Dña. [NOMBRE Y APELLIDOS], sin que proceda, pues, acordar ahora el embargo, pero sí su aseguramiento mediante anotación preventiva de embargo en el Registro de la Propiedad de [LOCALIDAD], en la finca registral n.º [NÚMERO], inscrita al tomo [TOMO], libro [LIBRO], folio [FOLIO], librándose oportuno mandamiento a los efectos del art. 613.4 LEC.

SÉPTIMO.- Conforme a lo dispuesto en el art. 584 LEC, el embargo no debe exceder, salvo peligro para los fines de la ejecución, de bienes cuyo valor supere la cantidad por la que se despacha ejecución, pero la verificación de que la finca embargada es presuntivamente ganancial, y está sujeta a una hipoteca de la Caja de Ahorros de [LOCALIDAD], por importe de [IMPORTE] euros, cuya amortización se ignora, pero no puede ser grande por la fecha de constitución, y la realidad de su ubicación y superficie suponen, en términos del art. 612.1 LEC, circunstancias que permiten dudar de la suficiencia de los bienes embargados en relación con la exacción de la responsabilidad de D./Dña. [NOMBRE Y APELLIDOS], por lo que procede la mejora del embargo.

Se señalan para embargo a tal efecto los créditos de D./Dña. [NOMBRE Y APELLIDOS] frente a la empresa [DENOMINACIÓN SOCIAL], NIG n.º [NÚMERO], con sede en [LOCALIDAD], polígono [Nº DE POLÍGONO], pabellón [Nº DE PABELLÓN], por el precio facturado por su actividad de agente comercial afecto a la fecha de la traba, solicitándose como medida de garantía la orden de retención y puesta a disposición de las cantidades adeudadas en ese Tribunal.

Por todo lo expuesto,

SUPLICO AL TRIBUNAL

que, por presentado este escrito con sus copias, se sirva admitirlo, y por personada y parte en el proceso de ejecución en la representación que ostento de [NOMBRE DE LA PARTE], despache ejecución frente a D./Dña. [NOMBRE Y APELLIDOS], en razón de autos de juicio cambiario n.º [Nº DE PROCEDIMIENTO]/[AÑO], de que conocía el Tribunal, por cantidad deeuros (euros), correspondientes a principal e intereses vencidos deeuros, y la deeuros (euros), que se presupuestan provisionalmente para intereses y costas del procedimiento ejecutivo, todo ello sin perjuicio de la definitiva liquidación, y convertido el embargo preventivo ya trabado de finca rústica en embargo ejecutivo, se acuerde por el Letrado de la Administración de Justicia librar mandamiento de anotación preventiva al Registro de la Propiedad deen los términos indicados, y asimismo se acuerde mejorar el embargo mediante la traba de los derechos de crédito a la fecha de D./Dña. [NOMBRE Y APELLIDOS] respecto a la mercantil, con la orden de retención y puesta a disposición de su importe en la cuenta de depósitos y consignaciones del Tribunal.

Es Justicia de hacerse en [LUGAR], a [FECHA].

OTROSÍ DIGO: Que siendo D./Dña. [NOMBRE Y APELLIDOS] casado con D./Dña. [NOMBRE Y APELLIDOS], sin que consten capitulaciones matrimoniales que hayan apartado el régimen legal supletorio de gananciales, la ejecución se sigue a causa de deudas contraídas por el marido, pero de las que debe responder la sociedad de gananciales, siendo la finca rústica embragada bien presuntivamente ganancial conforme al Registro de la Propiedad, por lo que la mujer tiene derecho a oponerse a la ejecución o a solicitar la disolución de sociedad conyugal conforme a lo dispuesto en el art. 541 LEC.

En su virtud,

SUPLICO AL TRIBUNAL, que teniendo por causadas las manifestaciones anteriores a sus oportunos efectos, el Letrado de la Administración de Justicia se sirva notificar el embargo del inmueble asentado en el Registro de la Propiedad de [LOCALIDAD], a D./Dña. [NOMBRE Y APELLIDOS], esposa del ejecutado, y de su mismo domicilio, dándole traslado de esta demanda, y del auto que despache la ejecución, a los posibles efectos legales, como es Justicia que reitero en lugar y fecha ‘ut supra’.

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a
