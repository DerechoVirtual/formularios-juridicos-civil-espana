---
name: demanda-resolver-compraventa-inmueble-retraso-entrega-civ-0787
description: "Demanda para resolver la compraventa de inmueble por retraso en la entrega y recuperar lo pagado. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda para resolver la compraventa de inmueble por retraso en la entrega y recuperar lo pagado

> Formulario **CIV-0787** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio ordinario del comprador de un inmueble adquirido sobre plano contra la entidad promotora vendedora, para obtener la resolución del contrato por incumplimiento del plazo de entrega, la devolución de las cantidades anticipadas y los intereses legales como indemnización por la mora.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda para resolver la compraventa de inmueble por retraso en la entrega y recuperar lo pagado» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda para resolver la compraventa de inmueble por retraso en la entrega y recuperar lo pagado” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:demanda-resolver-compraventa-inmueble-retraso-entrega-civ-0787`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (9 veces)
- [ ] IMPORTE (6 veces)
- [ ] Nº (6 veces)
- [ ] DENOMINACIÓN SOCIAL (3 veces)
- [ ] Nº DE CLÁUSULA (3 veces)
- [ ] DOMICILIO (2 veces)
- [ ] FECHAS (2 veces)
- [ ] PLAZO PACTADO (2 veces)
- [ ] SEDE (2 veces)
- [ ] AÑO
- [ ] BENEFICIARIO
- [ ] COLEGIO DE ABOGADOS
- [ ] DOMICILIO PROFESIONAL
- [ ] DÍA
- [ ] LOCALIDAD
- [ ] MES
- [ ] MES Y AÑO
- [ ] NIF
- [ ] NOMBRE Y APELLIDOS DEL DEMANDANTE
- [ ] NOMBRE Y APELLIDOS DEL LETRADO
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR
- [ ] Nº DE CLÁUSULAS
- [ ] Nº DE COLEGIADO
- [ ] Nº DE INSCRIPCIÓN
- [ ] PLAZO
- [ ] PORCENTAJE

## Normas que cita el formulario

- art. 5 Ley Orgánica 1/2025
- art. 1.124 Código Civil
- art. 1.113 Código Civil
- art. 1.101 Código Civil

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

Don/Doña [NOMBRE Y APELLIDOS DEL PROCURADOR], Procurador/a de los Tribunales, que actúa en nombre y representación de Don/Doña [NOMBRE Y APELLIDOS DEL DEMANDANTE], con domicilio en [DOMICILIO], conforme a escritura de poder inscrita en el Registro Electrónico de Apoderamientos Judiciales con el nº [Nº DE INSCRIPCIÓN], y asistido/a del Letrado/a en ejercicio Don/Doña [NOMBRE Y APELLIDOS DEL LETRADO], colegiado/a n.º [Nº DE COLEGIADO] del Ilustre Colegio de Abogados de [COLEGIO DE ABOGADOS], con despacho abierto en [DOMICILIO PROFESIONAL], ante el Tribunal comparezco y, como mejor proceda en Derecho, DIGO:

Que por medio del presente escrito, en la representación que ostento, vengo a formular demanda de juicio ordinario sobre resolución de contrato y condena al pago de cantidad contra la entidad mercantil [DENOMINACIÓN SOCIAL], con NIF [NIF] y domicilio en [DOMICILIO], con base en los siguientes datos y razonamientos jurídicos:

HECHOS

PRIMERO.– Mi mandante y la entidad mercantil demandada suscribieron en documento privado de fecha [FECHA], que se aporta como DOCUMENTO Nº [Nº], la compraventa sobre plano del inmueble que se describe en la estipulación primera del referido contrato.

SEGUNDO.– En el citado contrato quedó fijado en la cláusula [Nº DE CLÁUSULA] que el precio de la compraventa era de [IMPORTE] euros, que se aplazaba mediante abonos mensuales de [IMPORTE] euros, después de un inicial pago alzado de una parte sustancial del precio de otros [IMPORTE] euros.

En cumplimiento de la citada cláusula, mi principal ha realizado pagos a cuenta desde el mes de [MES Y AÑO] por importe de [IMPORTE] euros, mediante transferencia en cuenta a favor de [BENEFICIARIO], como se acredita con los DOCUMENTOS Nº [Nº] de esta demanda.

TERCERO.– En la cláusula [Nº DE CLÁUSULA], referida a la entrega y formalización de la compraventa, se estipulaba expresamente que la entrega de la vivienda se efectuaría en el plazo de [PLAZO PACTADO: por ejemplo, dieciocho meses], «[TRANSCRIPCIÓN LITERAL DE LA CLÁUSULA: por ejemplo, plazo concedido por la Administración, entregando los bienes en perfectas condiciones para su uso y ocupación]».

CUARTO.– Habiendo transcurrido más del doble del plazo de entrega pactado por las partes conforme a las cláusulas del contrato de compraventa, el día [FECHA] mi representado/a comunicó a la entidad demandada su voluntad de renunciar a la compra de la vivienda por incumplimiento esencial del contrato, solicitando la devolución de las cantidades entregadas, más sus intereses. La entidad demandada manifestó la imposibilidad de cumplir sus obligaciones por motivos ajenos a su voluntad, alegó que era el demandante quien no había cumplido con el pago del precio estipulado y mostró su conformidad con la resolución del contrato, pero con la retención al demandante del [PORCENTAJE] % del precio pactado.

Se aportan como DOCUMENTOS Nº [Nº] y [Nº] copia del escrito dirigido a la demandada de fecha [FECHA], con su acuse de recibo, y la contestación de la entidad fechada el [FECHA].

QUINTO.– En fecha [FECHA] el actor, al objeto de dejar constancia fehaciente, notificó a la entidad demandada por requerimiento notarial la resolución del contrato y la reclamación de la devolución de la cantidad anticipada a cuenta del precio, sin que hasta ahora haya obtenido respuesta alguna, no dejando más alternativa a esta parte que la vía judicial.

Se aporta copia del requerimiento notarial no atendido por la demandada como DOCUMENTO Nº [Nº].

SEXTO.– Interesa a esta parte actora dejar constancia de que, previamente a la presentación de la presente demanda, se llevaron a cabo diversos esfuerzos de negociación con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria.

Entre las acciones realizadas se incluyen el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución, así como la participación en reuniones llevadas a cabo los días [FECHAS], cuyo objetivo fue buscar una conciliación respecto de las diferencias planteadas.

Se adjuntan como prueba copias de las comunicaciones enviadas y recibidas durante el proceso de negociación, incluidas cartas, correos electrónicos y, en su caso, actas de reuniones, como DOCUMENTOS Nº [Nº].

A los anteriores hechos son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

I.– JURISDICCIÓN Y COMPETENCIA.

Con arreglo a los preceptos contenidos en el artículo 117 de la Constitución, el artículo 21 de la Ley Orgánica del Poder Judicial y el artículo 36 de la Ley de Enjuiciamiento Civil, la jurisdicción ordinaria del Reino de España es la única competente para conocer de los negocios o demandas civiles que se susciten en territorio español entre españoles, además de que los órganos jurisdiccionales son competentes, en defecto de sumisión expresa o tácita y aunque el demandado no tuviera su domicilio en España, en materia de obligaciones contractuales, cuando la obligación objeto de la demanda se haya cumplido o deba cumplirse en España [artículo 22 quinquies a) de la Ley Orgánica del Poder Judicial].

El conocimiento del litigio pertenece a la materia del orden jurisdiccional civil (artículo 9.2 de la Ley Orgánica del Poder Judicial), y corresponde la competencia objetiva a las secciones civiles de los tribunales de instancia, en cuanto por disposición legal expresa no viene atribuido a otros tribunales (artículo 85.1 de la Ley Orgánica del Poder Judicial y artículo 45 de la Ley de Enjuiciamiento Civil).

Corresponde el conocimiento del juicio a la Sección Civil del Tribunal de Instancia que por reparto corresponda (artículo 68 de la Ley de Enjuiciamiento Civil) de los de [SEDE], al que me dirijo en aplicación del artículo 51.1 de la Ley de Enjuiciamiento Civil, por ser el lugar del domicilio de la entidad demandada, [DENOMINACIÓN SOCIAL], amén de que aquí nació la relación jurídica entre las partes.

II.– CAPACIDAD.

Conforme al artículo 6.1.1.º y 3.º de la Ley de Enjuiciamiento Civil tienen capacidad para ser parte las personas físicas y las jurídicas, y a tenor del artículo 7.1 y 4 de la misma ley, tienen capacidad de obrar procesal las personas que se hallen en el pleno ejercicio de sus derechos civiles, y las personas jurídicas constituidas legalmente a través de sus representantes necesarios.

III.– LEGITIMACIÓN.

El artículo 10 de la Ley de Enjuiciamiento Civil legitima para comparecer y actuar en juicio a los titulares de la relación jurídica u objeto litigioso. En el caso de autos, demandante y demandada son los sujetos titulares del contrato cuyo incumplimiento fundamenta la acción resolutoria que se ejerce, existiendo, pues, legitimación directa ordinaria. La legitimación activa de mi representado/a resulta indiscutible en su calidad de comprador, y corresponde la pasiva a la demandada como parte vendedora de dicho contrato.

IV.– PROCEDIMIENTO.

El interés económico de la demanda supera la suma de 15.000 euros, por lo que, al no tener la presente contienda una tramitación especial por razón de la materia, será de aplicación lo dispuesto en los artículos 248.3, 249.2 y 254.1 de la Ley de Enjuiciamiento Civil, debiendo ventilarse por el juicio ordinario, regulado en el Título II del Libro II de la Ley de Enjuiciamiento Civil (artículos 399 y siguientes), debiendo asimismo seguirse las disposiciones comunes a los procesos declarativos previstas en el Título I de dicho Libro (artículos 248 y siguientes).

V.– POSTULACIÓN Y DEFENSA.

Se cumplen las normas de postulación procesal, ya que la demanda se presenta por medio de procurador/a legalmente habilitado/a para actuar ante los tribunales de este partido, y bajo la dirección de letrado en ejercicio que la redacta y firma, conforme a lo dispuesto en los artículos 23.1 y 31.1 de la Ley de Enjuiciamiento Civil.

VI.– REQUISITOS FORMALES.

Se inicia el proceso por medio de demanda que reúne todos los requisitos exigidos en el artículo 399 de la Ley de Enjuiciamiento Civil, sin que existan otras exigencias especiales de procedibilidad y no estando prevista legalmente una acreditación preliminar de la legitimación o principio de prueba del derecho, por lo que, siendo competente el tribunal, deberá admitirse a tenor de los artículos 403.1 y 404 de la misma ley.

VII.– CUANTÍA.

Cumpliendo la exigencia del artículo 253.1 de la Ley de Enjuiciamiento Civil, se cifra la cuantía de la demanda en la cantidad de [IMPORTE] euros, que integra la cantidad líquida reclamada conforme al artículo 251.1.ª de la misma ley.

VIII.– CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda cumple con los requisitos de procedibilidad exigidos por los artículos 264.4.º y 399.3 de la Ley de Enjuiciamiento Civil, así como con lo dispuesto en el artículo 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

IX.– FUNDAMENTO MATERIAL DE LA TUTELA.

Se ejercita acción resolutoria, con fundamento en el artículo 1.124 del Código Civil, del contrato de compraventa suscrito el [FECHA], por medio del cual el demandante compró sobre plano a la demandada [DESCRIPCIÓN DEL INMUEBLE: por ejemplo, una vivienda unifamiliar] a construir sobre un solar propiedad de esta, solicitando la devolución de las cantidades entregadas según contrato como parte del precio de dicha vivienda.

Sobre la base contractual de lo pactado en la cláusula [Nº DE CLÁUSULA] del contrato, que se reseña en el ordinal tercero del cuerpo de la demanda, a cuyo tenor la entrega de la vivienda se efectuaría en el plazo de [PLAZO PACTADO], así como de lo que se desprende de la interpretación conjunta de las demás, especialmente de las cláusulas [Nº DE CLÁUSULAS], no habiéndose pactado en el contrato, que fue redactado por la parte vendedora demandada, prórroga ni excepción alguna al plazo de entrega de la vivienda, y sí una penalización por incumplimiento del vendedor (que la parte actora opta por no reclamar), no puede llegarse a otra conclusión que la de que el plazo de entrega era el de [PLAZO PACTADO] en cualquier caso, y que lo que se desprende de dicha cláusula es que la entidad demandada contaba, en la fecha de suscribir el contrato de compraventa, con la licencia administrativa de obras que, además, había fijado el plazo de ejecución de las mismas en [PLAZO], por lo que no puede acogerse el razonamiento de que ahora la demandada (sorprendiendo la buena fe del comprador) diga que el plazo de ejecución empezaba a contarse desde la fecha de concesión de una licencia con la que no contaba (o le fue suspendida), lo que tuvo que haberse consignado expresamente en el contrato si existía algún problema con ella, pues, en tal caso, estaríamos ante una verdadera condición resolutoria (artículo 1.113 del Código Civil). Además, no se puede entender que ello no le es imputable, precisamente porque sí lo es, ya que solo a un proceder doloso o, cuando menos, culposo cabe achacar el comenzar a construir sin contar con licencia o hacerlo sin sujetarse a los términos de la misma, lo que ha motivado la paralización de las obras. Ello es más grave si cabe si se tiene en cuenta que acoger tal razonamiento supondría aceptar un desequilibrio importante en las respectivas contraprestaciones de las partes, pues mientras el comprador quedaba sujeto a unos plazos ciertos y bien determinados para atender el pago de los sucesivos plazos en que se debía abonar el precio de la vivienda, para el vendedor el plazo de ejecución quedaría sin prefijar, quedando no solo sujeto a lo que pudiera decidir un tercero sino que, aparte de ser contrario a lo dispuesto en los artículos 1.256, 1.284, 1.285 y 1.288 del Código Civil, así como a lo dispuesto en su artículo 1.128 respecto de las obligaciones a plazo, contraviene los derechos reconocidos por los artículos 80.1.c) y 83 del texto refundido de la Ley General para la Defensa de los Consumidores y Usuarios, aprobado por Real Decreto Legislativo 1/2007, de 16 de noviembre, sobre el justo equilibrio que debe existir entre los derechos y obligaciones de las partes y la nulidad de las cláusulas abusivas.

En consecuencia, la falta de concesión de la licencia de obras frustra las justas expectativas del comprador, ya que ha transcurrido más del doble del tiempo establecido en el contrato para la realización de la obra, desde la firma del mismo hasta la interposición de la demanda, estando la obra paralizada, mientras que el comprador ha cumplido con las entregas de dinero pactadas, incluso en exceso, por lo que está en su derecho de pedir la resolución del contrato con la consiguiente devolución de las cantidades entregadas, más la indemnización correspondiente de los daños y perjuicios por mora, ex artículo 1.101 del Código Civil, que se concreta en los intereses legales de la suma entregada a contar desde el día siguiente a la fecha en que debió producirse la entrega de la vivienda, el día [FECHA].

X.– COSTAS.

Las costas del presente proceso deberán ser impuestas a la parte demandada, en la medida en que deben resultar estimadas la totalidad de nuestras pretensiones, conforme al principio del vencimiento que destaca el artículo 394.1 de la Ley de Enjuiciamiento Civil en lo que respecta a los juicios declarativos en primera instancia.

En atención a todo lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito de demanda junto con los documentos que se acompañan y copias simples de todo ello, se sirva admitir uno y otros, se me tenga por comparecido/a y parte, en la representación que ostento y con carácter de demandante, entendiéndose conmigo las ulteriores diligencias, y por promovido juicio ordinario contra [DENOMINACIÓN SOCIAL], se le confiera traslado emplazándole en legal forma, y seguido que sea el oportuno procedimiento, en su día se dicte sentencia en la que, estimando la presente demanda:

1.º) Se declare resuelto el contrato de compraventa de fecha [FECHA], estipulado entre la parte actora y la demandada, respecto del bien inmueble que se determina en el escrito de demanda.

2.º) Se condene a la entidad demandada a reintegrar y pagar al actor la suma de [IMPORTE] euros que tiene percibidos de este.

3.º) Se condene a la entidad demandada, en concepto de daños y perjuicios por mora, a abonar al actor los intereses legales de dicha suma computados desde el [FECHA].

4.º) En todo caso, se pronuncie el reintegro de las costas con cargo a la parte demandada.

Es justicia que se hace en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Abogado/a: Firma del Procurador/a:
