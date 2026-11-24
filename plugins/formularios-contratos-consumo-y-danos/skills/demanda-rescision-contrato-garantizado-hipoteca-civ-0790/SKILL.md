---
name: demanda-rescision-contrato-garantizado-hipoteca-civ-0790
description: "Demanda de rescisión de un contrato garantizado con hipoteca. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de rescisión de un contrato garantizado con hipoteca

> Formulario **CIV-0790** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio ordinario en que un acreedor ejercita la acción rescisoria (pauliana) contra un contrato de préstamo con garantía hipotecaria celebrado por su deudor en fraude de acreedores, con solicitud de rescisión del contrato y cancelación de la inscripción registral (artículos 1290, 1291.3.º y 1294 y siguientes del Código Civil).

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de rescisión de un contrato garantizado con hipoteca» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de rescisión de un contrato garantizado con hipoteca” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:demanda-rescision-contrato-garantizado-hipoteca-civ-0790`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (12 veces)
- [ ] NOMBRE Y APELLIDOS DEL DEUDOR (6 veces)
- [ ] FECHA (5 veces)
- [ ] IMPORTE (4 veces)
- [ ] SEDE (4 veces)
- [ ] DOMICILIO (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] AÑO
- [ ] CLASE DE PROCESO
- [ ] COLEGIO DE ABOGADOS
- [ ] CONCEPTO DE LA DEUDA
- [ ] DATOS REGISTRALES
- [ ] DENOMINACIÓN
- [ ] DENOMINACIÓN SOCIAL
- [ ] DENOMINACIÓN SOCIAL DE LA ENTIDAD
- [ ] DENOMINACIÓN SOCIAL DE LA ENTIDAD ACREEDORA HIPOTECARIA
- [ ] DÍA
- [ ] FECHAS
- [ ] MES
- [ ] NOMBRE DEL NOTARIO
- [ ] NOMBRE Y APELLIDOS DEL LETRADO
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR
- [ ] NOMBRE Y APELLIDOS O DENOMINACIÓN SOCIAL DEL DEMANDANTE
- [ ] Nº DE PROCEDIMIENTO
- [ ] Nº DE PROTOCOLO
- [ ] PERIÓDICO
- [ ] PLAZO

## Normas que cita el formulario

- art. 1299 Código Civil
- art. 1111 Código Civil
- art. 5 Ley Orgánica 1/2025
- art. 1291.3.º Código Civil
- art. 1294 Código Civil
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

Don/Doña [NOMBRE Y APELLIDOS DEL PROCURADOR], Procurador/a de los Tribunales, actuando en nombre y representación de Don/Doña [NOMBRE Y APELLIDOS O DENOMINACIÓN SOCIAL DEL DEMANDANTE], según acredito por [ELEGIR: certificación del registro electrónico de apoderamientos judiciales que acompaño / designación apud acta ante el Letrado de la Administración de Justicia de [SEDE]], bajo la dirección letrada de Don/Doña [NOMBRE Y APELLIDOS DEL LETRADO], Abogado/a del Ilustre Colegio de [COLEGIO DE ABOGADOS], ante el Tribunal comparezco y, como mejor proceda en Derecho, DIGO:

Que en virtud del presente escrito formulo demanda de rescisión del contrato de préstamo y constitución de hipoteca de fecha [FECHA] contra Don/Doña [NOMBRE Y APELLIDOS DEL DEUDOR], con domicilio en [DOMICILIO], y contra la entidad [DENOMINACIÓN SOCIAL DE LA ENTIDAD ACREEDORA HIPOTECARIA], con domicilio en [DOMICILIO], amparándome en los artículos 1290 y 1291.3.º del Código Civil, la cual baso en los siguientes

HECHOS

PRIMERO.– Mi representado/a ejercita la acción rescisoria en su condición de acreedor del codemandado Don/Doña [NOMBRE Y APELLIDOS DEL DEUDOR], quien en fecha [FECHA] concertó con mi representado/a [CONTRATO ORIGEN DEL CRÉDITO: por ejemplo, un contrato de suministro de mercancías], dejando de abonar la cantidad de [IMPORTE] euros en concepto de [CONCEPTO DE LA DEUDA], adeudándose a fecha de hoy la citada cantidad con más los intereses legales.

A efectos de justificar estos extremos fácticos se acompaña como DOCUMENTO Nº 1 el contrato suscrito en fecha [FECHA], como DOCUMENTOS Nº [Nº] a [Nº] las facturas impagadas por el codemandado, y como DOCUMENTO Nº [Nº] testimonio del [ELEGIR: auto despachando ejecución / resolución que declara la deuda] por esta deuda contra el citado codemandado, dictado por el Tribunal de Instancia de [SEDE] en autos de [CLASE DE PROCESO] número [Nº DE PROCEDIMIENTO].

SEGUNDO.– Pese a la existencia de la deuda relatada en el apartado anterior, el codemandado Don/Doña [NOMBRE Y APELLIDOS DEL DEUDOR] concertó con la entidad codemandada [DENOMINACIÓN SOCIAL] un contrato de préstamo y constitución de hipoteca, el cual se celebró ante el Notario Don/Doña [NOMBRE DEL NOTARIO], el día [FECHA], con número de protocolo [Nº DE PROTOCOLO], habiéndose procedido a la inscripción del mismo en el Registro de la Propiedad (se acompaña como DOCUMENTO Nº [Nº] nota simple del Registro de la Propiedad número [Nº] de [LOCALIDAD], donde consta la inscripción de la hipoteca en garantía de [IMPORTE] euros de principal, intereses y costas) [DATOS REGISTRALES].

La celebración del citado contrato priva a mi representado/a y a todos los demás acreedores de cualquier posibilidad de perseguir los bienes del codemandado, puesto que el inmueble objeto del contrato, [DESCRIPCIÓN: por ejemplo, lugar donde desarrolla su actividad mercantil], es el único bien de su titularidad. Por otra parte, [CIRCUNSTANCIAS DE INSOLVENCIA: por ejemplo, la falta de actividad comercial del deudor desde hace aproximadamente seis meses y su conocida y pública situación de insolvencia], llevan a deducir lógicamente que el contrato se ha celebrado en fraude de acreedores, tal como expondremos a continuación.

TERCERO.– El contrato cuya rescisión se pretende produce un perjuicio manifiesto a mi representado/a, habida cuenta de que el deudor carece de otros bienes, ha dejado de realizar cualquier actividad comercial o mercantil y el importe de la hipoteca que ahora grava el único inmueble de su propiedad hace totalmente imposible la realización del bien, en atención a que el valor en venta del mismo es notoriamente inferior al del importe garantizado por el crédito hipotecario.

En estas circunstancias, existen diferentes elementos que ponen de manifiesto que el contrato se celebró para defraudar a los acreedores del codemandado Don/Doña [NOMBRE Y APELLIDOS DEL DEUDOR], lo cual era conocido por el acreedor hipotecario codemandado, quien se beneficia singularmente por la alteración en la prelación de créditos que se provoca con el negocio.

Los elementos que ponen de manifiesto el fraude son los siguientes:

1) El deudor venía realizando su actividad comercial en el local hipotecado, siendo conocido en toda la zona que hace aproximadamente [PLAZO] que ha cerrado el local y ha dejado de realizar actividad alguna; tal como se aprecia en el acta notarial que se acompaña como DOCUMENTO Nº [Nº], el local está cerrado, apreciándose en la puerta del mismo un anuncio de oferta de alquiler de la inmobiliaria [DENOMINACIÓN]; igualmente, la inmobiliaria está ofreciendo en alquiler dicho negocio en la prensa local, tal como se acredita por los anuncios del periódico [PERIÓDICO] correspondientes a los días [FECHAS], que se acompañan como DOCUMENTOS Nº [Nº] a [Nº].

2) Las dificultades económicas del codemandado eran de sobra conocidas en la zona y sin duda lo eran también por la entidad hipotecaria, puesto que la sucursal donde se concertó el préstamo se encuentra [CIRCUNSTANCIA DE PROXIMIDAD: por ejemplo, en la misma calle que el negocio del codemandado, escasamente a doscientos metros], por lo que lógicamente era conocido por la entidad bancaria que el negocio había cerrado y que difícilmente podía hacerse frente por el deudor hipotecante a las cuotas del préstamo.

3) La situación financiera del codemandado debía ser de sobra conocida por dicha entidad, puesto que, tal como se aprecia en las facturas aportadas con esta demanda como DOCUMENTOS Nº [Nº] a [Nº], las mismas se domiciliaron en una cuenta corriente que el demandado poseía en la entidad acreedora codemandada, por lo que es lógico pensar que existía una relación comercial que permitía conocer a la entidad hipotecaria que el deudor se encontraba en una situación de insolvencia de hecho.

4) El importe del capital del préstamo concedido es notoriamente superior al valor del inmueble, lo cual determina que, de hecho, la entidad bancaria será la única que podrá satisfacerse de la deuda, puesto que, de ejecutarse la hipoteca, no existirá capital sobrante para los demás acreedores.

5) El beneficio del codemandado con esta operación es más que evidente, puesto que ha obtenido un capital, que puede ocultar fácilmente, disponiendo del mismo, a cambio de «perder» el local, que iba a ser embargado de forma inminente por las deudas contraídas, si bien, de no realizar esta operación, no hubiera podido obtener ningún capital por cuanto ha dejado un montante de deudas muy superior al valor del local, como acreditaremos en el momento procesal oportuno.

CUARTO.– De lo expuesto anteriormente resulta patente el cumplimiento de los requisitos para el ejercicio de la acción de rescisión del contrato, reiterados jurisprudencialmente y resumidos en la sentencia del Tribunal Supremo de 17 de julio de 2006 (recurso 2954/1999), la cual los enumera del siguiente modo: 1. La existencia de un crédito anterior en favor del accionante y en contra del que enajena o grava la cosa; 2. Realización de un acto en virtud del cual salga el bien del patrimonio del que lo enajena; 3. El propósito defraudatorio en perjuicio del acreedor; y 4. Ausencia de todo otro medio que no sea la rescisión de la enajenación para obtener la reparación del perjuicio inferido al acreedor.

Tales requisitos se dan en el presente caso, puesto que es evidente que se trata de un negocio concertado en fraude de los acreedores y que deja a mi representado/a sin posibilidad de perseguir la cantidad que se le adeuda, careciendo mi mandante de otro medio para cobrar su crédito y deduciéndose la acción en el plazo de cuatro años establecido en el artículo 1299 del Código Civil, motivos por los cuales se ejercita la presente acción rescisoria, solicitando que se rescinda el contrato y se cancele la inscripción registral, a fin de reintegrar el inmueble al patrimonio del deudor y que pueda responder de las deudas contraídas con anterioridad por el codemandado Don/Doña [NOMBRE Y APELLIDOS DEL DEUDOR].

QUINTO.– Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS AL QUE LAS PARTES SE HAN SOMETIDO EN CUMPLIMIENTO DEL REQUISITO DE PROCEDIBILIDAD DE LA LO 1/2025], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como DOCUMENTO Nº [Nº] [DOCUMENTO QUE ACREDITA QUE SE HA ACUDIDO A UN MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS].

A los anteriores hechos les son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

Competencia

Corresponde a los Tribunales de [SEDE] al ser el lugar en el que tienen su domicilio los demandados (artículo 51 de la Ley de Enjuiciamiento Civil).

Legitimación

Le corresponde a esta parte su condición de acreedor del codemandado (artículos 1111 y 1291 del Código Civil).

Procedimiento

Es el juicio ordinario con fundamento en el artículo 249.2 de la Ley de Enjuiciamiento Civil, dado el importe reclamado de [IMPORTE] euros, que excede de los 15.000 euros a partir de los cuales deben seguirse las reclamaciones por las normas del juicio ordinario.

Cumplimiento de los requisitos de procedibilidad

La presente demanda cumple con los requisitos de procedibilidad exigidos por los artículos 264.4.º y 399.3 de la Ley de Enjuiciamiento Civil, así como con lo dispuesto en el artículo 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

Fondo de la reclamación

Al tratarse de un contrato en fraude de acreedores que produce un perjuicio a los mismos, debe rescindirse el contrato conforme al artículo 1291.3.º del Código Civil, cumpliéndose los requisitos de subsidiariedad de la acción (artículo 1294 del Código Civil) y de ejercicio de la misma en el plazo de cuatro años (artículo 1299 del Código Civil), procediendo la cancelación del asiento registral. La rescisión es procedente conforme a la doctrina jurisprudencial recogida en las sentencias del Tribunal Supremo de 10 de abril de 1995 (recurso 551/1992), 16 de enero de 2001 (recurso 2828/1998), 27 de junio de 2002 (recurso 69/1997) y 13 de mayo de 2004 (recurso 1993/1998).

Costas

En materia de costas, el artículo 394 de la Ley de Enjuiciamiento Civil señala que las de primera instancia se imponen a la parte que vea rechazadas sus pretensiones, siendo evidente la mala fe y temeridad con la que han actuado los codemandados.

En base a lo anterior,

SUPLICO AL TRIBUNAL: que tenga por presentada la presente demanda con los documentos a ella adjuntos y por parte en la representación que ostento, y tras la pertinente tramitación dicte sentencia por la que se rescinda el contrato de préstamo y constitución de garantía hipotecaria celebrado por los codemandados [NOMBRE Y APELLIDOS DEL DEUDOR] y [DENOMINACIÓN SOCIAL DE LA ENTIDAD] en fecha [FECHA], ordenando la cancelación de la inscripción registral del mismo, todo ello con imposición de costas a los demandados, con expresa declaración de temeridad, dando a los autos el impulso procesal con arreglo a Derecho.

OTROSÍ DIGO: [OPCIONAL — incluir si procede: personas jurídicas no exentas] que estando la presente demanda sujeta al abono de la tasa por el ejercicio de la potestad jurisdiccional fijada por la Ley 10/2012, de 20 de noviembre, y desarrollada por la Orden HAP/2662/2012, de 13 de diciembre, siendo mi representado/a persona jurídica no exenta de su pago, se acompaña a la presente demanda como DOCUMENTO Nº [Nº] la correspondiente autoliquidación con el ejemplar para la Administración de Justicia debidamente validado y en el que consta el pago de la cantidad de [IMPORTE] euros correspondiente a la cuota fija [OPCIONAL — en su caso: de la que se detrae la bonificación del 10% por la utilización de medios telemáticos], sin que se incluya la cuota variable prevista en el artículo 7.2 de la Ley 10/2012 al haber sido declarada inconstitucional y nula por la sentencia del Tribunal Constitucional 140/2016, de 21 de julio.

SUPLICO AL TRIBUNAL: que tenga por hecha la anterior manifestación a los efectos pertinentes y por acompañado el documento justificativo del abono de la tasa.

Es justicia que insto en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firmas del Abogado y del Procurador
