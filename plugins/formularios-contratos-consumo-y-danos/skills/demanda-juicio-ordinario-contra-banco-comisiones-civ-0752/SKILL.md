---
name: demanda-juicio-ordinario-contra-banco-comisiones-civ-0752
description: "Demanda de juicio ordinario contra el banco por comisiones por descubiertos y efectos devueltos. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio ordinario contra el banco por comisiones por descubiertos y efectos devueltos

> Formulario **CIV-0752** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio declarativo ordinario de un cliente contra una entidad bancaria para reclamar la devolución de las comisiones por descubierto y por devolución de efectos impagados cargadas en una cuenta corriente vinculada a un contrato de descuento de efectos mercantiles, sin respaldo contractual (falta de pacto, de servicio efectivamente prestado y de consentimiento), con intereses legales y, subsidiariamente, declaración de nulidad de cualquier cláusula que se alegue de contrario.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio ordinario contra el banco por comisiones por descubiertos y efectos devueltos» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio ordinario contra el banco por comisiones por descubiertos y efectos devueltos” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:demanda-juicio-ordinario-contra-banco-comisiones-civ-0752`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (9 veces)
- [ ] Nº DE DOCUMENTO (7 veces)
- [ ] FECHA (5 veces)
- [ ] DENOMINACIÓN SOCIAL DE LA ENTIDAD BANCARIA (4 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] DOMICILIO (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL DEMANDANTE (2 veces)
- [ ] Nº (2 veces)
- [ ] AÑO
- [ ] CLASE DE CONTRATO
- [ ] COLEGIO
- [ ] CORREO ELECTRÓNICO
- [ ] DÍA
- [ ] FECHA DE LA RECLAMACIÓN EXTRAJUDICIAL
- [ ] IMPORTE EN LETRA
- [ ] MES
- [ ] NOMBRE Y APELLIDOS DEL LETRADO/A
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] Nº DE CLÁUSULA
- [ ] Nº DE COLEGIADO
- [ ] Nº DE CONTRATO
- [ ] Nº DE CUENTA
- [ ] SEDE
- [ ] TELÉFONO

## Normas que cita el formulario

- art. 399.1 LEC
- art. 85.1.º LOPJ
- art. 51.1 LEC
- art. 6.1.3.º LEC
- art. 7.4 LEC
- art. 253.1 LEC
- art. 251.1.ª LEC
- art. 23 LEC
- art. 399 LEC
- art. 5 Ley Orgánica 1/2025
- art. 1262.1.º CC
- art. 1101 CC
- art. 394.1 LEC

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

### Avisos de actualización (5) — se aplican en el texto, nunca se copian en el documento

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] QUE POR TURNO CORRESPONDA»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…ts. 248 y 249.2 LEC, toda vez que la cuantía del proceso excede de 15.000 euros.»: comprobar el umbral de cuantía del juicio verbal (art. 250.2 LEC) y la remisión del art. 249 LEC en su redacción vigente tras la LO 1/2025.
- Junto a «…to n.º [Nº DE DOCUMENTO] (burofax y demás comunicaciones de reclamación previa).»: el original se limitaba a citar la «DA 7.ª» de la LO 1/2025; comprobar la cita y el medio adecuado de solución de controversias efectivamente utilizado.
- Junto a «…y la Ley 7/1998, de 13 de abril, sobre Condiciones Generales de la Contratación.»: comprobar la vigencia actual de la Orden EHA/2899/2011 y de las circulares del Banco de España aplicables a las comisiones y descubiertos, así como la normativa sectorial posterior.
- Junto a «… precisión y transparencia para su correcta comprensión por la parte adherente».»: la Ley 26/1988 citada en la sentencia está derogada por la Ley 10/2014, de 26 de junio, de ordenación, supervisión y solvencia de entidades de crédito; comprobar el artículo equivalente en esta última y en su normativa de desarrollo.

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] QUE POR TURNO CORRESPONDA

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales y de D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDANTE], como acredito en virtud de escritura de poder inscrita en el Registro Electrónico de Apoderamientos Judiciales que acompaño como documento n.º [Nº DE DOCUMENTO], bajo la dirección letrada de D./Dña. [NOMBRE Y APELLIDOS DEL LETRADO/A], abogado/a ejerciente, n.º [Nº DE COLEGIADO] del Ilustre Colegio de la Abogacía de [COLEGIO], con despacho abierto en [LOCALIDAD], calle [DOMICILIO], ante el Tribunal comparezco y como mejor proceda en Derecho,

DIGO

Que por medio del presente escrito paso a interponer demanda de juicio ordinario contra la entidad [DENOMINACIÓN SOCIAL DE LA ENTIDAD BANCARIA], con sucursal abierta en la calle [DOMICILIO] de [LOCALIDAD], ejercitando acción de reclamación de cantidad por comisiones cobradas ilegalmente.

Que esta parte asume el compromiso de recibir cualquier comunicación dirigida por la oficina judicial, durante toda la fase declarativa e, incluso, en una eventual fase de ejecución, por medios telemáticos, en términos del art. 399.1 II LEC, consignándose a estos efectos la siguiente dirección de correo electrónico y n.º de teléfono: [CORREO ELECTRÓNICO] / [TELÉFONO].

Sirvan a la misma los siguientes hechos y consideraciones de derecho:

HECHOS

PRIMERO.- El [FECHA], mi mandante D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDANTE] concertó con la entidad bancaria aquí demandada un contrato de cuenta corriente con n.º [Nº DE CUENTA], asociado a un segundo contrato de descuento de efectos mercantiles con n.º [Nº DE CONTRATO]. La operativa de ambos consistía en el ingreso de una serie de fondos por parte del cliente, para poder girar efectos cambiarios frente a la cuenta, pactándose intereses remuneratorios de las cantidades ingresadas e intereses moratorios para el supuesto de que el saldo fuera negativo. Se acompaña copia del contrato referido como documento n.º [Nº DE DOCUMENTO].

SEGUNDO.- El contrato se ha desarrollado, o por lo menos es la percepción que tenía hasta la fecha mi cliente, con normalidad en los [Nº] años de vida del mismo, ingresando en el mismo diversas cantidades y girando innumerables efectos cambiarios, en el marco de la actividad por él desarrollada, que eran abonados por la entidad bancaria. Lógicamente, en dicho periodo de tiempo y como consecuencia de impagos de clientes o puntuales periodos de iliquidez, han concurrido momentos muy ocasionales en los que la cuenta corriente no ha tenido fondos y ha ofrecido un saldo negativo, lo que ha sido rápidamente repuesto, pudiendo coincidir con una presentación de efectos cambiarios cuyo impago generó la devolución de los mismos. Si bien, como se ha dicho, todo ello ha sido convenientemente reintegrado, con el correspondiente abono de los intereses pactados como consecuencia de la demora.

En este sentido, la entidad demandada no ha hecho uso, en ningún momento, de la facultad resolutoria del contrato, recogida en su cláusula [Nº DE CLÁUSULA], en virtud de algún eventual incumplimiento del mismo por mi cliente. Y, asimismo, a fecha de la presente demanda la cuenta corriente presenta un saldo positivo de [IMPORTE] euros, tras la imputación de las cantidades dispuestas y adelantadas por el banco en el pasado trimestre. Se adjunta copia de extracto bancario a fecha [FECHA] como documento n.º [Nº DE DOCUMENTO], en el cual se pueden comprobar todos estos extremos.

TERCERO.- Si bien lo que se percibía por mi mandante como un correcto funcionamiento del contrato no respondía a la realidad, tal y como se ha puesto de manifiesto tras comprobar la cadena de cargos imputados ilícitamente, de los que se ha apercibido en fechas recientes. De esta forma, tras detectar un cargo de comisión de [IMPORTE] euros por descubierto en [FECHA], en una rutinaria comprobación de un extracto bancario, se solicitó de la entidad bancaria una relación pormenorizada de todos los movimientos efectuados desde el inicio del contrato en [FECHA]. La sorpresa de mi mandante ha sido total al verificar que, en el marco del movimiento global de fondos del contrato, que supera los [IMPORTE] euros, se han venido cargando una serie de comisiones del estilo indicado, de [IMPORTE] euros, por descubiertos en la cuenta, cada día que el saldo se mantuviera en negativo, o cuando era devuelto un efecto cambiario. El importe global, tras el cargo de, concretamente, [Nº] comisiones, asciende a [IMPORTE] euros. Se acompaña relación de todos los movimientos efectuados en la cuenta, reseñando todas y cada una de las comisiones (el resalte es realizado por esta parte), como documento n.º [Nº DE DOCUMENTO].

CUARTO.- Puesto que el contrato no recogía ninguna previsión específica de este tipo de comisiones, se envió el [FECHA] burofax a la entidad bancaria, cuya copia se adjunta como documento n.º [Nº DE DOCUMENTO], requiriendo información sobre dichas comisiones, su eventual cobertura contractual desconocida para esta parte, y solicitando su devolución. Hasta la fecha no se tiene conocimiento de contestación alguna por parte de [DENOMINACIÓN SOCIAL DE LA ENTIDAD BANCARIA].

A los anteriores hechos son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN Y COMPETENCIA

Radicando la competencia genérica en el orden civil de la jurisdicción, sobre la base de la reclamación de cantidades, detenta la competencia objetiva y funcional la Sección Civil del Tribunal de Instancia, por aplicación de lo dispuesto en los arts. 85.1.º LOPJ y 45 LEC. Asimismo, y puesto que la demandada tiene sucursal abierta al público en el partido judicial del Tribunal al cual tengo el honor de dirigirme, su situación debe determinar la competencia territorial, conforme al art. 51.1 LEC.

II.- CAPACIDAD Y LEGITIMACIÓN

Mi mandante es mayor de edad y se encuentra en situación de pleno ejercicio de sus derechos civiles, en virtud de lo dispuesto en los arts. 6.1.1.º y 7.1 LEC. Asimismo, la demandada es persona jurídica, cuya capacidad se reconoce en el art. 6.1.3.º LEC, derivándose su personalidad de su constitución en escritura pública inscrita en el Registro Mercantil, con la necesidad de comparecer en juicio por medio de sus representantes legales (art. 7.4 LEC).

Corresponde la legitimación activa directa a mi mandante, dado que es parte en el contrato en virtud del cual se reclama a la demandada. En cuanto a la legitimación pasiva, corresponde a la entidad bancaria [DENOMINACIÓN SOCIAL DE LA ENTIDAD BANCARIA], como parte del contrato de [CLASE DE CONTRATO] en cuestión, que ha cobrado las comisiones cuya devolución se peticiona.

III.- PROCEDIMIENTO

La presente demanda deberá sustanciarse por las normas del juicio ordinario, a tenor de lo prevenido en los arts. 248 y 249.2 LEC, toda vez que la cuantía del proceso excede de 15.000 euros.

IV.- CUANTÍA

Cumpliendo lo prevenido en el art. 253.1 LEC, se hace constar que la cuantía de la demanda se concreta en [IMPORTE] euros, con arreglo al art. 251.1.ª LEC, puesto que se trata del principal reclamado.

V.- POSTULACIÓN Y DEFENSA

Conforme a los arts. 23 y 31 LEC se formula esta demanda a través de Procurador/a de los Tribunales con poder para pleitos, y con dirección y firma de Letrado habilitado ante el Tribunal. Asimismo, se cumplen los requisitos formales del art. 399 LEC.

VI.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD

La presente demanda cumple con el requisito de procedibilidad exigido por el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia, en relación con la disposición adicional séptima de dicha Ley, en los términos acreditados con el documento n.º [Nº DE DOCUMENTO] (burofax y demás comunicaciones de reclamación previa).

VII.- FONDO DE LA CUESTIÓN CONTROVERTIDA

1) De los contratos de cuenta corriente y descuento de efectos mercantiles pactados entre las partes

En el presente caso se ejercita la acción de reclamación de las cantidades cobradas sin respaldo contractual, que se cuantifica en el importe de [IMPORTE] euros. En este sentido, nos encontramos ante dos contratos de cuenta corriente y de descuento de efectos mercantiles, mediante los cuales mi cliente lograba un medio de pago a sus clientes a través de efectos cambiarios que se cargaban en la cuenta corriente, en la cual, a su vez, se mantenían fondos suficientes para todo ello. Asimismo, las cantidades ingresadas en la entidad bancaria ofrecían un interés remuneratorio, penalizando los descubiertos con un interés moratorio pactado entre las partes.

Dichos contratos se hallan regulados por todo un conjunto de normas jurídicas integrado por el denominado derecho bancario o legislación bancaria, que regula la organización de las entidades de crédito, su régimen de transparencia y actuación y el régimen de sus crisis financieras, destacando la Ley 13/1994, de 1 de junio, de autonomía del Banco de España, que le confiere la potestad de dictar circulares en materia monetaria y no monetaria, así como la Ley 10/2014, de 26 de junio, de ordenación, supervisión y solvencia de entidades de crédito, y la Orden EHA/2899/2011, de 28 de octubre, de transparencia y protección del cliente de servicios bancarios. Asimismo, en materia específica de contratos bancarios, es de aplicación la normativa general de los contratos contenida en el Código Civil y en el Código de Comercio, completada por la legislación especial en materia de información y documentación de la contratación bancaria y de protección de los consumidores, como son fundamentalmente el Real Decreto Legislativo 1/2007, de 16 de noviembre, que aprueba el texto refundido de la Ley General para la Defensa de los Consumidores y Usuarios y otras leyes complementarias, y la Ley 7/1998, de 13 de abril, sobre Condiciones Generales de la Contratación.

2) De la inexistencia de pacto alguno sobre las comisiones cobradas

En consecuencia, el cargo de las comisiones cuya devolución se pretende debía ampararse en un pacto contractual asumido por las partes, contenido en el contrato de adhesión que suscribió, en su momento, mi mandante. Si bien, en el presente caso tal pacto no existe, como puede comprobarse en la copia íntegra del contrato aportada como documento n.º [Nº DE DOCUMENTO], en el cual no se hace mención alguna al respecto.

Sobre la cuestión se pronuncia la sentencia de la Audiencia Provincial de Cádiz de 3 de junio de 2010, Rec. 147/2009, que exige que toda comisión «debe haber sido pactada en forma por las partes para su validez y eficacia, por así desprenderse de dos normas jurídicas fundamentales reguladoras de la disciplina de los contratos que nos ocupan, cuáles son: por un lado la Ley 26/1988 de Disciplina e Intervención de las Entidades de Crédito, en su artículo 48.2, exige que estos contratos se formalicen por escrito y que los mismos reflejen de forma explícita y con la necesaria claridad los compromisos contraídos por las partes, aunque la sanción por el incumplimiento por parte de la entidad bancaria de estos requisitos no es la nulidad del contrato; así como, por otro lado, la Ley reguladora de las Condiciones Generales de la Contratación, claramente aplicable a los contratos que nos ocupan, en cuanto los mismos contienen condiciones generales a las que la otra parte simplemente se adhiere, ley que exige que la cláusula o condición general se haya pactado expresamente por las partes, y no sólo eso, sino además que sea clara y precisa, de suerte que en caso de incumplimiento de estos requisitos la sanción será la no incorporación o en su caso la nulidad de la cláusula en cuestión. Dicha ley lo que trata es de garantizar que el adherente conozca o al menos haya tenido oportunidad de conocer las condiciones generales en el momento de celebración del contrato y que éstas resulten lo suficientemente comprensibles, considerando tales cláusulas como incluidas en el contrato sólo cuando el adherente acepte su incorporación al mismo y sea firmado éste por todos los contratantes, o en todo caso, no haya duda sobre la aceptación de tales cláusulas por parte de los contratantes. En consecuencia, el requisito que nos ocupa relativo a que la cláusula reguladora de la comisión bancaria haya sido pactada en forma, por un lado excluye todas aquellas comisiones de origen exclusivamente unilateral, exigiéndose que las mismas nazcan del previo convenio o acuerdo entre las partes, expreso en el sentido de indubitado, acuerdo que además, desde este punto de vista formal, exige que en su contenido reúna los requisitos de claridad, precisión y transparencia para su correcta comprensión por la parte adherente».

Esta necesidad de respaldo contractual específico es reiterada por la sentencia de la Audiencia Provincial de Las Palmas de 2 de febrero de 2011, Rec. 142/2008, en la línea jurisprudencial recogida ampliamente en la sentencia de la Audiencia Provincial de Salamanca de 6 de octubre de 2009, Rec. 232/2009. La misma exige, para la plena validez en derecho de una cláusula reguladora de una comisión bancaria: 1.º) que dicha cláusula haya sido pactada en forma; 2.º) que obedezca a un servicio efectivamente prestado o un gasto habido; y 3.º) que dicho servicio haya sido aceptado o solicitado por el cliente.

Continúa señalando dicha resolución que «Como igualmente hemos dicho, la ley de condiciones generales de la contratación, como también la citada ley de disciplina e intervención de las entidades de crédito, exigen que además las cláusulas del contrato bancario reguladoras de una comisión bancaria respondan a servicios efectivamente prestados, como no podía ser de otro modo si no queremos dar al traste con toda la regulación contenida con carácter general sobre los contratos en los artículos 1254 y siguientes del código civil, en el primero de los cuales tan sólo se declara existente un contrato cuando una parte se obliga respecto de otra a hacer una cosa o prestar algún servicio, estableciendo el artículo 1258 que desde su perfección los contratos obligan no sólo a lo expresamente pactado, sino también a todas las consecuencias que según su naturaleza sean conformes a la buena fe, al uso y a la ley, como lo es desde luego que, si se pacta una comisión a favor de una de las partes del contrato, dicha comisión obedezca a la prestación de un servicio real por dicha parte, indicando finalmente el artículo 1261.2.º del mismo cuerpo legal que no hay contrato si no concurren, entre otros, el requisito de un objeto cierto que sea materia del contrato, inexistente si se pacta una comisión a cambio de un servicio que no es real. Y por último, la citada legislación exige que el servicio haya sido aceptado o solicitado por el cliente, como tampoco podría ser de otro modo sobre la base de los citados artículos del código civil reguladores de los contratos, uno de cuyos requisitos esenciales, el primero y principal, es el consentimiento o aceptación de lo pactado por las partes».

En el supuesto que nos ocupa, no concurre ninguno de los requisitos exigidos jurisprudencialmente. Por un lado, y como se ha dicho, mi mandante nunca pactó, solicitó o aceptó ninguna cláusula expresa que previera la aplicación de las comisiones por descubierto o devolución de efectos. En segundo lugar, el descubierto o saldo negativo no ha generado ningún gasto específico para el banco, ni ha precisado de ningún servicio efectivamente prestado. Simplemente los descubiertos concurren ocasionalmente, y la demandada pasa a prestar dinero, en el marco de la actividad inherente al sector bancario, cobrando un interés moratorio que el cliente ya ha abonado y que, repárese, es diferente de las comisiones cargadas. Es decir, mientras el interés remunera una utilización de un capital del banco durante un concreto periodo de tiempo, la comisión se cobra por un mero consentimiento de dicha disposición, respecto a la cual la entidad bancaria se muestra pasiva, a la espera de que se reintegre la cantidad, se reitera, con los intereses derivados de su utilización. Extremos que son aplicables a la devolución de efectos por falta de fondos, que generan una simple negativa al pago, sin servicio concreto prestado por la parte demandada.

3) De la nulidad de cualquier cláusula eventual, por ausencia absoluta de consentimiento y la falta de convalidación posterior

Para el caso de que la parte demandada alegue cualquier suerte de cláusula contenida en condiciones generales, página web o documento ajeno al contrato, debe reiterarse que en ningún momento ha concurrido la voluntad expresa de mi cliente para aceptar el pago de comisiones adicionales a los intereses moratorios. Dicha cláusula desconocida adolecería de uno de los requisitos esenciales de cualquier contrato, el consentimiento, conforme al art. 1262.1.º CC, por causa no ya de vicio del mismo, sino de su absoluta ausencia. Extremo que debería abocar al órgano judicial a quien tengo el honor de dirigirme a declarar la nulidad de tal eventualidad, en virtud de lo dispuesto en el art. 1300 del mencionado texto legal.

Siendo evidente la falta de consentimiento expreso, tampoco puede argumentarse de contrario la concurrencia del mismo en su modalidad tácita. Repárese en este punto que mi cliente reacciona inmediatamente tras conocer el cobro de dichas comisiones, reclamando información y solicitando su devolución; y, finalmente, ante el silencio de la demandada, interpone la presente demanda. En este sentido, el corto espacio de tiempo transcurrido en el referido proceso no puede ser considerado como consentimiento de las comisiones en cuestión, sino que responde al lógico asesoramiento (mi mandante no es profesional del derecho), estudio del caso y diseño de la estrategia a seguir para revertir la situación que aquí se denuncia.

Así, debe recordarse, en primer lugar, que el conocimiento de tal situación no equivale al consentimiento, tal y como el Tribunal Supremo señala reiteradamente en una constante y clásica doctrina jurisprudencial (entre otras, Sentencias de 16 de octubre de 1964, 10 de marzo de 1995 o 19 de diciembre de 1990). Al respecto, esta última resolución, con cita de las de 3 de febrero de 1962 y 27 de enero de 1964, señala que el conocimiento de los actos no supone el consentimiento y no tiene trascendencia jurídica el retraso en el ejercicio de la demanda, porque quien está legitimado para ello es dueño de su acción mientras no pueda oponérsele la prescripción por el transcurso del tiempo necesario a tal efecto. Asimismo, ya en la clásica sentencia de 9 de noviembre de 1959, se indicaba que el conocimiento, acto de valor lógico sometido a las leyes del pensar, no es identificable con el consentimiento, acto de valor volitivo o de voluntad gobernado por el derecho.

En segundo lugar, la también clásica sentencia dictada el 25 de enero de 1961 determinaba que el consentimiento tácito exige la realidad de un acto que ponga de relieve el deseo o voluntad del agente, no teniendo tal alcance el mero conocimiento, que es enterarse de algo, pero no permiso o conformidad. La sentencia de 8 de febrero de 1964 exige que aquél sea claro, terminante e inequívoco, y las dictadas los días 10 y 14 de junio de 1963 añaden la característica de actos concluyentes. Tal línea jurisprudencial se mantiene de manera constante, siendo complementada por la más moderna doctrina de los actos propios, al respecto de la cual la Sentencia del Tribunal Supremo de 22 de octubre de 2003, Rec. 4074/1997, señala que los mismos deben realizarse con la finalidad de crear, modificar o extinguir algún derecho, causando estado y definiendo inalterablemente la situación jurídica de su autor (Sentencias de 12 de julio de 1990 y 11 de marzo de 1991), y han de ser tales actos concluyentes y definitivos (Sentencias de 16 de febrero de 1988, 25 de enero y 6 de noviembre de 1990, 11 de marzo, 14 de mayo y 27 de noviembre de 1991), siendo además necesario que el acto se presente como solemne, preciso, claro, determinante y perfectamente delimitado, y no ambiguo ni inconcreto (Sentencia de 10 de noviembre de 1992, rec. 962/1990).

4) Devolución de las cantidades y subsidiaria declaración de nulidad

En consecuencia, al no haber admitido en ningún momento mi mandante el cobro de las cantidades cargadas en cuenta, y haber reaccionado inmediatamente a su descubrimiento, procede devolver la cantidad global de [IMPORTE] euros cobrada ilegalmente, con arreglo a lo dispuesto en el art. 1101 CC. En este sentido, la entidad bancaria ha incumplido su contrato, contraviniendo lo pactado, debiendo devolver lo cargado de más, con los intereses legales desde la fecha de la reclamación extrajudicial, por aplicación de los arts. 1100 y 1108 del mismo texto legal.

VIII.- COSTAS

La parte demandada soportará el reintegro de todas las costas del juicio por el principio cuasiobjetivo de vencimiento del art. 394.1 LEC, para declarativos en primera instancia.

SUPLICO AL TRIBUNAL

Que teniendo por presentado este escrito de demanda junto con los documentos que se acompañan y copias simples de todo ello, se sirva admitirlo a trámite, se me tenga por comparecido y parte demandante en el proceso y en la representación que ostento, entendiéndose conmigo las sucesivas diligencias, por promovido el correspondiente juicio ordinario, acordando conferir traslado de la demanda y documentos con ella presentados a la entidad [DENOMINACIÓN SOCIAL DE LA ENTIDAD BANCARIA], emplazándola en legal forma y, previos los trámites oportunos, en su día se dicte sentencia por la que se condene a la parte demandada a pagar a la actora la cantidad de [IMPORTE EN LETRA] euros ([IMPORTE] €), con intereses legales desde [FECHA DE LA RECLAMACIÓN EXTRAJUDICIAL], y declaración subsidiaria de nulidad de la eventual cláusula que se pueda alegar de contrario; con expresa condena en costas a la misma.

Es justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Abogado/a Firma del Procurador/a
