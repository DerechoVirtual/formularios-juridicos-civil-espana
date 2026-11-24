---
name: demanda-ejecutiva-basada-escritura-publica-prestamo-civ-1495
description: "Demanda ejecutiva basada en escritura pública de préstamo. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda ejecutiva basada en escritura pública de préstamo

> Formulario **CIV-1495** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Demanda ejecutiva basada en título no judicial (primera copia ejecutiva de una escritura pública de préstamo) contra el deudor que ha dejado de pagar. Pide el requerimiento de pago y, si no paga, el embargo de los bienes señalados y los oficios a entidades y registros para localizar otros bienes, por ser insuficientes los conocidos por el ejecutante.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda ejecutiva basada en escritura pública de préstamo» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda ejecutiva basada en escritura pública de préstamo” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:demanda-ejecutiva-basada-escritura-publica-prestamo-civ-1495`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (7 veces)
- [ ] Nº (7 veces)
- [ ] IMPORTE EN LETRA (5 veces)
- [ ] DOMICILIO (2 veces)
- [ ] FECHA (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL EJECUTADO (2 veces)
- [ ] Nº DE COLEGIADO (2 veces)
- [ ] PORCENTAJE (2 veces)
- [ ] AÑO
- [ ] DNI/NIF
- [ ] DÍA
- [ ] INDICAR BIENES
- [ ] INDICAR ENTIDADES, REGISTROS Y ORGANISMOS
- [ ] MES
- [ ] NOMBRE DEL NOTARIO
- [ ] NOMBRE Y APELLIDOS DEL ABOGADO/A
- [ ] NOMBRE Y APELLIDOS DEL EJECUTANTE
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] Nº DE PROTOCOLO
- [ ] SEDE

## Normas que cita el formulario

- art. 545.3 LEC
- art. 85.1.º LOPJ
- art. 538 LEC
- art. 539.1 LEC
- art. 517.1 LEC
- art. 6 Ley 36/2006
- art. 517.2.4.º Ley 1/2000
- art. 517.2.4.º LEC
- art. 520 LEC
- art. 549 LEC
- art. 1091 Código Civil
- art. 1089 Código Civil
- art. 1740 Código Civil
- art. 1753 Código Civil
- art. 1108 Código Civil
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

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, colegiado/a n.º [Nº DE COLEGIADO], actuando en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS DEL EJECUTANTE], con domicilio en [DOMICILIO] y DNI/NIF [DNI/NIF], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento n.º [Nº], bajo la dirección letrada de D./Dña. [NOMBRE Y APELLIDOS DEL ABOGADO/A], colegiado/a n.º [Nº DE COLEGIADO], ante el Tribunal comparezco y, como mejor proceda en derecho, DIGO:

Que, en la representación que ostento, formulo DEMANDA EJECUTIVA BASADA EN TÍTULO NO JUDICIAL contra D./Dña. [NOMBRE Y APELLIDOS DEL EJECUTADO], con domicilio en [DOMICILIO], en reclamación de la cantidad de [IMPORTE EN LETRA] euros ([IMPORTE] €) en concepto de principal e intereses ordinarios y moratorios vencidos, más otros [IMPORTE EN LETRA] euros ([IMPORTE] €) presupuestados provisionalmente para hacer frente a los intereses que, en su caso, puedan devengarse durante la ejecución y a las costas de ésta, demanda que formulo con base en los siguientes

HECHOS

PRIMERO.– Con fecha [FECHA], el ahora demandado suscribió con mi patrocinado un contrato de préstamo por importe de [IMPORTE] euros, a devolver en [Nº] cuotas iguales el último día de los [Nº] meses siguientes a la firma del contrato.

Dicho préstamo se elevó a escritura pública autorizada por el Notario de [LOCALIDAD] D./Dña. [NOMBRE DEL NOTARIO], con fecha [FECHA] y n.º [Nº DE PROTOCOLO] de los de su protocolo.

Se aporta como documento n.º [Nº] la primera copia de dicha escritura, expedida con mención de su carácter ejecutivo.

SEGUNDO.– En la citada escritura se pactó como interés remuneratorio un [PORCENTAJE] % del importe total del préstamo, que asciende a la suma de [IMPORTE] euros, a abonar junto con el último de los plazos de devolución estipulados, e igualmente un interés de demora del [PORCENTAJE] % anual. De entre los pactos contenidos en dicha escritura interesa también destacar que el impago de cualquier mensualidad daría lugar a dar por vencida la obligación por completo y a la exigibilidad de las cantidades vencidas no satisfechas, así como del resto de la deuda, con los intereses de demora pactados (cláusula n.º [Nº]).

TERCERO.– Al no haberse satisfecho por el deudor ninguno de los plazos de devolución pactados, pese a las gestiones amistosas realizadas, mi mandante ha considerado vencido el préstamo, ejercitando la facultad convenida en la cláusula citada y requiriendo notarialmente al deudor para que abonara la deuda, de acuerdo con lo pactado por las partes.

Se acompaña como documento n.º [Nº] el acta notarial de requerimiento de pago.

CUARTO.– Mi patrocinado tiene conocimiento de que el ejecutado es titular de los siguientes bienes susceptibles de embargo: [INDICAR BIENES]. No obstante, los bienes enumerados no son suficientes para el fin de la ejecución.

QUINTO.– Dada la insuficiencia de los bienes del demandado conocidos por el ejecutante y susceptibles de embargo, procede oficiar a las siguientes entidades, registros y organismos, como medida de localización e investigación, a fin de localizar nuevos bienes del ejecutado sobre los que realizar la traba: [INDICAR ENTIDADES, REGISTROS Y ORGANISMOS].

Creemos que los mencionados organismos, entidades y registros disponen de información sobre el patrimonio del ejecutado, ya que [INDICAR LAS RAZONES POR LAS QUE SE CONSIDERA QUE ESAS ENTIDADES TIENEN INFORMACIÓN]. Por otro lado, los datos cuya información se solicita no han podido ser obtenidos por esta parte pese a las múltiples gestiones y esfuerzos realizados a tal efecto, por lo que será necesario que se ejecuten de inmediato las medidas de localización y averiguación solicitadas, ya que cualquier demora podría frustrar el buen fin de la ejecución. Se aportan los documentos n.º [Nº] que acreditan que se ha solicitado la citada información y se ha denegado.

FUNDAMENTOS DE DERECHO

I.– COMPETENCIA.

Conforme a lo dispuesto en el art. 545.3 de la LEC, que se remite a los artículos 50 y 51 de dicha ley, en relación con lo dispuesto en el art. 85.1.º LOPJ, será competente para la ejecución fundada en el título contemplado en el ordinal 4.º del art. 517.2 el Tribunal de Instancia del lugar de cumplimiento de la obligación, que consta como domicilio de pago en la escritura pública que constituye el título ejecutivo.

II.– LEGITIMACIÓN.

El art. 538 de la LEC regula que es parte en el proceso de ejecución la persona o personas que piden y obtienen el despacho de la ejecución y la persona o personas frente a las que ésta se despacha, añadiendo que sólo podrá despacharse ejecución a instancia de quien aparezca como acreedor en el título ejecutivo frente a, entre otros, quien aparezca como deudor en el mismo título.

En el presente caso, mi representado es acreedor frente al ejecutado de un crédito dinerario derivado de un contrato de préstamo, por lo que tienen legitimación activa y pasiva, respectivamente.

III.– POSTULACIÓN.

Conforme a lo dispuesto en el art. 539.1 de la LEC, la demanda viene firmada por abogado y procurador, ya que es preceptiva la intervención de dichos profesionales.

IV.– TÍTULO.

El art. 517.1 de la LEC dispone que la acción ejecutiva deberá fundarse en un título que tenga aparejada ejecución, encontrándose entre éstos «las escrituras públicas, con tal que sea primera copia; o si es segunda que esté dada en virtud de mandamiento judicial y con citación de la persona a quien deba perjudicar, o de su causante, o que se expida con la conformidad de todas las partes» (art. 517.2, ordinal 4.º).

No obstante el tenor literal del citado precepto, el art. 17.1, párrafo cuarto, de la Ley del Notariado, según la redacción dada al mismo por el art. 6 de la Ley 36/2006, de 29 de noviembre, de medidas para la prevención del fraude fiscal, dispone que «es primera copia el traslado de la escritura matriz que tiene derecho a obtener por primera vez cada uno de los otorgantes. A los efectos del artículo 517.2.4.º de la Ley 1/2000, de 7 de enero, de Enjuiciamiento Civil, se considerará título ejecutivo aquella copia que el interesado solicite que se expida con tal carácter», introduciendo una norma de indudable carácter procesal con la que, por lo tanto, debe integrarse el art. 517.2.4.º LEC, puesto que la ya citada Ley 36/2006 tiene carácter ordinario y, por lo tanto, es del mismo rango que la Ley de Enjuiciamiento Civil, y puede modificar y completar esta norma procesal, lo que el Reglamento Notarial viene a completar en su art. 233, matizando que «en la copia de toda escritura que contenga obligaciones exigibles en juicio, deberá hacerse constar si se expide o no con eficacia ejecutiva y, en su caso, y de tener este carácter, que con anterioridad no se le ha expedido copia con eficacia ejecutiva», exigiendo así que quien pretenda la expedición de la copia de la escritura pública precise la finalidad que persigue con la misma (AAP Castellón, Secc. 3.ª, de 1 de febrero de 2008, rec. 538/2007), y este documento expedido con eficacia ejecutiva es el que se acompaña a la demanda.

Por otro lado, la cantidad reclamada excede de 300 euros, cumpliéndose el requisito contemplado en el art. 520 de la LEC.

V.– REQUISITOS FORMALES.

La presente demanda contiene todos los requisitos enumerados en el art. 549 de la LEC, ya que se ha indicado cuál es el título en que se funda, la tutela ejecutiva que se pretende y las personas frente a las que se interesa el despacho de la ejecución, los bienes del ejecutado susceptibles de embargo conocidos por mi poderdante, así como las medidas de localización e investigación de otros bienes del ejecutado, dada la insuficiencia de los reseñados. Por último, se acompaña a la demanda ejecutiva la documentación necesaria de la contemplada en el art. 550 del mismo texto legal.

VI.– FONDO DEL ASUNTO.

Al presente supuesto son aplicables los siguientes preceptos de carácter sustantivo:

— El art. 1091 del Código Civil, en relación con el art. 1254 del mismo texto legal, en cuanto se establece que las obligaciones que nacen de los contratos tienen fuerza de ley entre las partes y existe contrato desde que hay consentimiento en obligarse.

— El art. 1089 del Código Civil, en cuanto a la validez y eficacia en juicio de las obligaciones nacidas de los contratos.

— El art. 1740 del Código Civil, en cuanto a la definición del contrato de préstamo.

— El art. 1753 del Código Civil, con respecto a la obligación del deudor de satisfacer la cantidad prestada, en los términos convenidos, devolviendo al acreedor otro tanto.

— El art. 1108 del Código Civil, conforme al cual la indemnización a favor del acreedor en las obligaciones de pagar una cantidad de dinero, si el deudor incurre en mora, consiste en el pago de los intereses convenidos.

VII.– COSTAS.

En virtud de lo dispuesto en el art. 539.2 en relación con el 583 de la LEC, las costas de esta ejecución deberán ser impuestas al ejecutado, ya que ha sido quien ha originado la necesidad de este procedimiento al no haber cumplido con lo establecido en el contrato suscrito por las partes en que se basan las presentes actuaciones.

De conformidad con lo anteriormente expuesto,

SUPLICO AL TRIBUNAL:

Que, teniendo por presentado este escrito con los documentos acompañados y copia de todo ello, se sirva admitirlo, ordenando se entiendan conmigo las sucesivas diligencias y, en nombre de mi patrocinado, se me tenga por comparecido y parte y por presentada demanda ejecutiva para que, una vez examinados los requisitos y presupuestos procesales, el título ejecutivo y los actos de ejecución que se solicitan, así como la propia competencia, se despache ejecución frente a D./Dña. [NOMBRE Y APELLIDOS DEL EJECUTADO] por la cantidad de [IMPORTE EN LETRA] euros ([IMPORTE] €) en concepto de principal, [IMPORTE EN LETRA] euros ([IMPORTE] €) en concepto de intereses devengados hasta la fecha, más otros [IMPORTE EN LETRA] euros ([IMPORTE] €) presupuestados provisionalmente para los intereses que puedan generarse durante la ejecución y las costas de ésta, y que no supera el límite legal del 30 % de lo reclamado, sin perjuicio de ulterior liquidación, procediéndose a requerir de pago al deudor y, si no pagase en el acto, el tribunal procederá al embargo de los bienes designados en la relación fáctica de esta demanda y a librar los correspondientes despachos para que las entidades, registros y organismos reseñados informen de otros posibles bienes del ejecutado, ya que los designados por el ejecutante son insuficientes para responder de las responsabilidades reclamadas, todo ello con la finalidad de que mi poderdante sea satisfecho en la totalidad de la deuda de la que esta ejecución dimana. Todo ello con imposición de las costas derivadas de esta ejecución al ejecutado.

Por ser de justicia, que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Abogado/a Firma del Procurador/a
