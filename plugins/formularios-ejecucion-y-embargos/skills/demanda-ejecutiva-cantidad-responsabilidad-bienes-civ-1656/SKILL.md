---
name: demanda-ejecutiva-cantidad-responsabilidad-bienes-civ-1656
description: "Demanda ejecutiva por cantidad con responsabilidad de bienes gananciales. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda ejecutiva por cantidad con responsabilidad de bienes gananciales

> Formulario **CIV-1656** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Demanda ejecutiva al Tribunal de Instancia que por turno corresponda, en reclamación de cantidad siendo responsables bienes gananciales, tras no haber abonado determinadas cuotas de un contrato mercantil de préstamo.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda ejecutiva por cantidad con responsabilidad de bienes gananciales» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda ejecutiva por cantidad con responsabilidad de bienes gananciales” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:demanda-ejecutiva-cantidad-responsabilidad-bienes-civ-1656`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (7 veces)
- [ ] IMPORTE EN CIFRA (7 veces)
- [ ] FECHA (4 veces)
- [ ] Nº DE DOCUMENTO (4 veces)
- [ ] NÚMERO (4 veces)
- [ ] DESCRIPCIÓN DEL BIEN (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] PARTE DEMANDADA (2 veces)
- [ ] LUGAR
- [ ] MES
- [ ] MOTIVO
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] Nº
- [ ] Nº DE CUOTAS IMPAGADAS
- [ ] PACTOS DEL CONTRATO
- [ ] SEDE

## Normas que cita el formulario

- art. 572 LEC
- art. 545.3 LEC
- art. 85.1 LOPJ
- art. 539.1 LEC
- art. 517 LEC
- art. 520 LEC
- art. 1.091 Código Civil
- art. 1.089 Código Civil
- art. 51 Código de Comercio
- art. 50 Código de Comercio
- art. 311 Código de Comercio
- art. 1.108 Código Civil
- art. 539.2 LEC

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

### Avisos de actualización (2) — se aplican en el texto, nunca se copian en el documento

- Junto a «…NCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE] Q.P.T.R.C.»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.

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

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE] Q.P.T.R.C.

D./Dña. [NOMBRE Y APELLIDOS] Procurador/a. de los Tribunales, actuando en nombre y representación de [NOMBRE DEL REPRESENTADO/A], con domicilio en [LOCALIDAD] y D.N.I. número [NÚMERO], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], ante el Tribunal comparezco y como mejor proceda en derecho DIGO:

Que en la representación que ostento formulo DEMANDA EJECUTIVA contra [PARTE DEMANDADA], con domicilio en [LOCALIDAD], casado en régimen de gananciales con [NOMBRE Y APELLIDOS], con el mismo domicilio que el anterior, en reclamación de la cantidad de [IMPORTE] euros ([IMPORTE EN CIFRA] €) en concepto de principal e intereses ordinarios y moratorios vencidos, más otros [IMPORTE] euros ([IMPORTE EN CIFRA] €) presupuestados provisionalmente para hacer frente a los intereses que, en su caso, puedan devengarse durante la ejecución y a las costas de ésta, demanda que formulo con base en los siguientes

HECHOS

PRIMERO.- Con fecha [FECHA] y con intervención de Corredor de Comercio colegiado, el ahora demandado suscribió con mi patrocinado un contrato de préstamo con garantía personal por importe de [IMPORTE] euros ([IMPORTE EN CIFRA] €), a pagar en [Nº] cuotas, siendo el vencimiento pactado el día [FECHA]

Se aporta como documento n.º [NÚMERO], la póliza original de dicho contrato mercantil de préstamo.

Igualmente se adjunta como documento n.º [NÚMERO] la certificación acreditativa de la conformidad de dicha póliza con los asientos del libro registro del Corredor de Comercio colegiado interviniente y de la fecha de éstos.

SEGUNDO.- De entre los pactos contenidos en dicho contrato interesa ahora destacar los siguientes [PACTOS DEL CONTRATO] (se suele reseñar pacto de vencimiento anticipado, intereses)

TERCERO.- El deudor dejó de pagar a partir del mes de [MES], adeudando en total [Nº DE CUOTAS IMPAGADAS] cuotas y han resultado infructuosas las gestiones amistosas realizadas por mi mandante para que aquél abonara la deuda, por lo que mi representado, de acuerdo con lo pactado por las partes en el contrato, ha considerado vencido el préstamo y ha procedido a determinar, a fecha [FECHA], la deuda reclamable que asciende a la cantidad de [IMPORTE] euros ([IMPORTE EN CIFRA] €).

Se acompañan como documentos números [Nº DE DOCUMENTO] y [Nº DE DOCUMENTO], el saldo resultante de la liquidación efectuada por mi poderdante con la aplicación correspondiente a los intereses devengados hasta la fecha, al que se refiere el número 2 del art. 572 de la LEC, así como el documento fehaciente que acredita haberse practicado la liquidación en la forma pactada por las partes en el propio título ejecutivo, conforme a lo dispuesto en el art. 573 del mismo texto legal.

CUARTO.- Dando cumplimiento a lo regulado en el último párrafo del art. 572.2, acompaño como documento n.º [NÚMERO], telegrama acreditativo de haber notificado previamente al ejecutado la cantidad exigible resultante de la liquidación.

QUINTO.-.- Mi patrocinado tiene conocimiento de que el ejecutado es titular junto con su cónyuge de los siguientes bienes de carácter ganancial susceptibles de embargo [DESCRIPCIÓN DEL BIEN] Dado que frente a la deuda contraída por el ejecutado deben responder los bienes gananciales, el embargo de tales bienes habrá de notificarse al otro cónyuge. No obstante, los bienes enumerados no son suficientes para el fin de la ejecución.

SEXTO.- Dada la insuficiencia de los bienes del demandado conocidos por el ejecutante y susceptibles de embargo, procede oficiar a las siguientes entidades, registros y organismos, como medida de localización e investigación, a fin de localizar nuevos bienes del ejecutado sobre los que realizar la traba:

Creemos que los mencionados organismos, entidades y registros disponen de información sobre el patrimonio del ejecutado, ya que [MOTIVO]. Por otro lado, los datos cuya información se solicita no han podido ser obtenidos por esta parte pese a las múltiples gestiones y esfuerzos realizados a tal efecto, lo que acredito mediante los documentos números [Nº DE DOCUMENTO] remitidos y no contestados.

[OPCIONAL — incluir si procede]

(En su caso:)

En el caso de que fueran infructuosas las averiguaciones y pese a que la ejecución se sigue a causa de deudas propias del ejecutado, que está casado en régimen de gananciales, dada la insuficiencia de los bienes del deudor, deberán embargarse los siguientes bienes comunes [DESCRIPCIÓN DEL BIEN] Por lo tanto, el embargo de dichos bienes habrá de notificarse al cónyuge del demandado.

FUNDAMENTOS DE DERECHO

I.- COMPETENCIA.-

Conforme a lo dispuesto en el art. 545.3 de la LEC que se remite a los artículos 50 y 51 de dicha Ley, en relación con lo dispuesto en el art. 85.1º LOPJ, será competente para la ejecución fundada en el título contemplado en el ordinal 5.º del art. 517.2, el Tribunal de Instancia del domicilio del demandado.

II.- LEGITIMACIÓN.-

El art. 538 de la Ley de ritos regula que es parte en el proceso de ejecución la persona o personas que piden y obtienen el despacho de la ejecución y la persona o personas frente a las que ésta se despacha, añadiendo que sólo podrá despacharse ejecución a instancia de quien aparezca como acreedor en el título ejecutivo frente a, entre otros, quien aparezca como deudor en el mismo título.

En el presente caso, mi representado es acreedor frente al ejecutado de un crédito dinerario derivado de un contrato de préstamo mercantil, por lo que tienen legitimación activa y pasiva, respectivamente.

El art. 541.2 dispone que cuando la ejecución se siga a causa de deudas contraídas por uno de los cónyuges pero de las que deba responder la sociedad de gananciales, la demanda ejecutiva podrá dirigirse contra el cónyuge deudor, pero el embargo de bienes gananciales habrá de notificarse al cónyuge, dándole traslado de la demanda y del auto que despache ejecución a fin de que, dentro del plazo ordinario, pueda oponerse a la ejecución.

[OPCIONAL — incluir si procede]

(En su caso:)

El art. 541.3 establece que si la ejecución se siguiere a causa de deudas propias de uno de los cónyuges y se persiguiesen bienes comunes a falta de o por insuficiencia de los privativos, el embargo de aquéllos habrá de notificarse al cónyuge no deudor.

III.- POSTULACIÓN.-

Conforme a lo dispuesto en el art. 539.1 de la LEC, la demanda viene firmada por abogado y Procurador/a., ya que es preceptiva la intervención de dichos profesionales.

IV.- TÍTULO.-

El art. 517 de la LEC dispone que la acción ejecutiva deberá fundarse en un título que tenga aparejada ejecución, encontrándose entre éstos las pólizas de los contratos mercantiles firmadas por las partes y por corredor de comercio colegiado que las intervenga, con tal que se acompañe certificación en la que dicho corredor acredite la conformidad de la póliza con los asientos de su libro registro y la fecha de éstos.

Por otro lado, la cantidad reclamada excede de 300 euros, cumpliéndose el requisito contemplado en el art. 520 de la LEC.

V.- REQUISITOS FORMALES.-

La presente demanda contiene todos los requisitos enumerados en el art. 549 de la Ley Procesal Civil, ya que se ha indicado cual es el título en que se funda, la tutela ejecutiva que se pretende y las personas frente a las que se interesa el despacho de la ejecución, los bienes del ejecutado susceptibles de embargo conocidos por mi poderdante, así como las medidas de localización e investigación de otros bienes del ejecutado, dada la insuficiencia de los reseñados. Por último se acompaña a la demanda ejecutiva la documentación necesaria de la contemplada en el art. 550 del mismo texto legal.

VI.- FONDO DEL ASUNTO.-

Al presente supuesto son aplicables los siguientes preceptos de carácter sustantivo:

— El art. 1.091 del Código Civil en relación con el 1.254 del mismo texto legal, en cuanto se establece que las obligaciones que nacen de los contratos tienen fuerza de ley entre las partes y existe contrato desde que hay consentimiento en obligarse.
— El art. 1.089 del Código Civil en relación con el art. 51 del Código de Comercio, en cuanto a la validez y eficacia en juicio de las obligaciones nacidas de los contratos mercantiles.
— El art. 50 del Código de Comercio en relación con el art. 2 del mismo Código, que establecen que los contratos mercantiles se regirán por la dispuesto en el mismo, en su defecto por los usos de comercio y a falta de ambos por el Derecho común.
— Los artículos 62 y 63 del Código mercantil con respecto a la exigibilidad de las obligaciones mercantiles.
— El art. 311 del Código de Comercio en cuanto a la calificación como mercantil del contrato de préstamo
— Los artículos 315, 316 y 317 del tan citado Código, con respecto a la posibilidad de pactar el interés del préstamo y a su exigibilidad, así como a la capitalización de intereses líquidos y no satisfechos.
— El art. 1.108 del Código Civil conforme al cual la indemnización a favor del acreedor en las obligaciones de pagar una cantidad de dinero, si el deudor incurre en mora, consiste en el pago de los intereses convenidos.

VII.- COSTAS.-

En virtud de lo dispuesto en el art. 539.2 en relación con el 583 de la LEC, las costas de esta ejecución deberán ser impuestas al ejecutado, ya que ha sido quien ha originado la necesidad de este procedimiento al no haber cumplido con lo establecido en el contrato suscrito por las partes en que se basan las presentes actuaciones.

De conformidad con lo anteriormente expuesto,

SUPLICO AL TRIBUNAL:

Que teniendo por presentado este escrito con los documentos acompañados y copia de todo ello, se sirva admitirlo, ordenando se entiendan conmigo las sucesivas diligencias y en nombre de mi patrocinado se tenga por presentada demanda ejecutiva para que, una vez examinados los requisitos y presupuestos procesales, el título ejecutivo y los actos de ejecución que se solicitan, así como la propia competencia, se despache ejecución frente a [PARTE DEMANDADA] por el importe de la cantidad de [IMPORTE] euros ([IMPORTE EN CIFRA] €) en concepto de principal, [IMPORTE] euros ([IMPORTE EN CIFRA] €) en concepto de intereses devengados hasta la fecha, más otros [IMPORTE] euros ([IMPORTE EN CIFRA] €) presupuestados provisionalmente para los intereses que puedan generarse durante la ejecución y las costas de ésta, procediéndose a requerir de pago al deudor y si no pagase en el acto, el tribunal procederá al embargo de los bienes designados en la relación fáctica de esta demanda y a librar los correspondientes despachos para que las entidades, registros y organismos reseñados informen de otros posibles bienes del ejecutado, ya que los designados por el ejecutante son insuficientes para responder de las responsabilidades reclamadas, todo ello con la finalidad de que mi poderdante sea satisfecho en la totalidad de la deuda de la que esta ejecución dimana. Todo ello con imposición de las costas derivadas de esta ejecución al ejecutado.

Es de Justicia que pido en [LUGAR], a [FECHA].

OTROSI DIGO.- Siendo la deuda contraída exclusivamente por el demandado pero debiendo responder de ella la sociedad de gananciales INTERESO que el embargo de bienes gananciales se notifique al cónyuge de aquél, dándole traslado de la demanda ejecutiva y del auto que despache ejecución a fin de que, dentro del plazo ordinario, pueda oponerse a la ejecución.

[OPCIONAL — incluir si procede]

OTROSI DIGO.- Siendo la deuda propia y exclusiva del demandado, pero teniéndose que perseguir bienes comunes dada la insuficiencia de los bienes privativos, INTERESO que se notifique el embargo de aquéllos al cónyuge del ejecutado.

Es justicia que reitero en el Lugar y fecha indicados.

Firma de Abogado/a	Firma de Procurador/a

========================================================================
