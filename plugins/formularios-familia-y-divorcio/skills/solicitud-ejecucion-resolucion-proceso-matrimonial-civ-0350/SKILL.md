---
name: solicitud-ejecucion-resolucion-proceso-matrimonial-civ-0350
description: "Solicitud de ejecución de resolución de proceso matrimonial por impago de pensiones. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud de ejecución de resolución de proceso matrimonial por impago de pensiones

> Formulario **CIV-0350** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Escrito solicitando la ejecución de resolución judicial dictada en proceso matrimonial al haber dejado, el ejecutado, de abonar la pensión a la que está obligado.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud de ejecución de resolución de proceso matrimonial por impago de pensiones» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud de ejecución de resolución de proceso matrimonial por impago de pensiones” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:solicitud-ejecucion-resolucion-proceso-matrimonial-civ-0350`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (5 veces)
- [ ] FECHA (4 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] TIPO DE RESOLUCIÓN (3 veces)
- [ ] ACTO O RESOLUCIÓN (2 veces)
- [ ] AÑO
- [ ] DENOMINACIÓN SOCIAL
- [ ] DESCRIPCIÓN DE LOS BIENES
- [ ] DOCUMENTOS ACOMPAÑADOS
- [ ] LUGAR
- [ ] MES
- [ ] MOTIVO
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] Nº
- [ ] Nº DE ORDINAL
- [ ] Nº DE PROCEDIMIENTO
- [ ] SEDE
- [ ] TIPO Y Nº DE PROCEDIMIENTO

## Normas que cita el formulario

- art. 545.1 LEC
- art. 538 LEC
- art. 539.1 LEC
- art. 517.2 LEC
- art. 550 LEC
- art. 551 LEC
- art. 571 LEC
- art. 776 LEC
- art. 576 LEC
- art. 539.2 LEC
- art. 583 LEC
- art. 776.1.ª LEC
- art. 711 LEC

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

- Junto a «…MILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
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

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales y de [NOMBRE DEL REPRESENTADO/A], cuya representación tengo acreditada en los autos [TIPO Y Nº DE PROCEDIMIENTO], registrados con el número [Nº DE PROCEDIMIENTO], seguidos frente a [ACTO O RESOLUCIÓN], cuyos datos personales obran en las actuaciones, siguiendo instrucciones de mi mandante y como mejor proceda en derecho, DIGO:

Que mediante el presente escrito solicito la ejecución de la resolución dictada con fecha [FECHA], todo ello según resulta de los siguientes

HECHOS

PRIMERO.- El pasado día [FECHA] por el tribunal al que me dirijo se dictó [TIPO DE RESOLUCIÓN] que establecía que D. [NOMBRE Y APELLIDOS], en concepto de educación y alimentación de los hijos contribuiría en la cantidad de [IMPORTE] euros mensuales.

SEGUNDO.- El referido D. ha dejado de pagar las prestaciones económicas correspondientes a las mensualidades de [MES] de [AÑO], en adelante, que se adeudan en la cantidad de [IMPORTE] euros, por el concepto de [Nº] meses incumplidos.

TERCERO.- Mi patrocinado tiene conocimiento de que el ejecutado es titular de los siguientes bienes susceptibles de embargo [DESCRIPCIÓN DE LOS BIENES]. No obstante, los bienes enumerados no son suficientes para el fin de la ejecución.

CUARTO.- Dada la insuficiencia de los bienes del demandado conocidos por el ejecutante y susceptibles de embargo, procede oficiar a las siguientes entidades, registros y organismos, como medida de localización e investigación, a fin de localizar nuevos bienes del ejecutado sobre los que realizar la traba:

Creemos que los mencionados organismos, entidades y registros disponen de información sobre el patrimonio del ejecutado, ya que [MOTIVO]. Por otro lado, los datos cuya información se solicita no han podido ser obtenidos por esta parte pese a las múltiples gestiones y esfuerzos realizados a tal efecto, como se acredita con los documentos

FUNDAMENTOS DE DERECHO

I.- COMPETENCIA.

Según el art. 545.1 LEC, será competente para la ejecución de resoluciones judiciales y de transacciones y acuerdos judicialmente homologados o aprobados, el tribunal que conoció del asunto en primera instancia o el que homologó o aprobó la transacción o el acuerdo.

Por eso se presenta esta demanda ante el Tribunal al que gustosamente me dirijo, ya que fue quien dictó la sentencia que sirve de título para la presente ejecución.

II.- LEGITIMACIÓN.

El art. 538 LEC regula que es parte en el proceso de ejecución la persona o personas que piden y obtienen el despacho de la ejecución y la persona o personas frente a las que ésta se despacha.

III.- POSTULACIÓN.

Conforme a lo dispuesto en el art. 539.1 LEC, la demanda viene firmada por abogado y procurador, ya que estamos ante la ejecución de una resolución dictada en un proceso en que es preceptiva la intervención de dichos profesionales.

IV.- TÍTULO DE EJECUCIÓN.

El art. 517.2 ordinal [Nº DE ORDINAL] de la LEC enumera como uno de los títulos que lleva aparejada ejecución la [TIPO DE RESOLUCIÓN], como la que sirve de fundamento a esta demanda.

V.- REQUISITOS FORMALES.

La presente demanda contiene todos los requisitos enumerados en el art. 549 de la Ley Procesal Civil, ya que se ha indicado cual es el título en que se funda, la tutela ejecutiva que se pretende y las personas frente a las que se interesa el despacho de la ejecución, los bienes del ejecutado susceptibles de embargo conocidos por mi poderdante, así como las medidas de localización e investigación de otros bienes del ejecutado, dada la insuficiencia de los reseñados. Por último, se acompaña a la demanda ejecutiva la documentación necesaria de la contemplada en el art. 550 LEC [DOCUMENTOS ACOMPAÑADOS].

VI.- PROCEDIMIENTO.

El Tribunal despachará ejecución y el Letrado de la Administración de Justicia concretará las medidas ejecutivas, por los trámites de los arts. 551 a 554 LEC, en relación con los arts. 571 LEC y ss.; con las especialidades que se contienen en el art. 776 LEC para la ejecución forzosa de los pronunciamientos sobre medidas.

VII.- INTERESES.-

Conforme a lo establecido en el art. 576 LEC, desde que fuere dictada sentencia en primera instancia, toda sentencia o resolución que condene al pago de una cantidad de dinero líquida determinará, a favor del acreedor, el devengo de un interés anual igual al del interés legal del dinero incrementado en dos puntos o el que corresponda por pacto de las partes o por disposición especial de la ley.

VIII.- COSTAS.

En virtud de lo dispuesto en el art. 539.2 LEC en relación con el art. 583 LEC, las costas de esta ejecución deberán ser impuestas al ejecutado, ya que ha sido quien ha originado la necesidad de este procedimiento al no haber cumplido con lo establecido en la resolución recaída en las presentes actuaciones.

De conformidad con lo anteriormente expuesto,

SUPLICO AL TRIBUNAL:

Que teniendo por presentado este escrito con los documentos acompañados y copia de todo ello, se sirva admitirlo, y por comparecido al Procurador/a D./Dña. [NOMBRE Y APELLIDOS] en la representación que ostenta de Dña. [NOMBRE Y APELLIDOS], entendiéndose conmigo las sucesivas diligencias, y se tenga por solicitada la ejecución de la [TIPO DE RESOLUCIÓN] dictada por este Tribunal con fecha [FECHA], a cuyos efectos:

1.º) Se despache ejecución frente a [ACTO O RESOLUCIÓN] por el importe de la cantidad de [IMPORTE] euros en concepto de principal, más otros [IMPORTE] euros presupuestados provisionalmente para los intereses que puedan generarse durante la ejecución y las costas de ésta, en concepto de liquidación de las pensiones alimenticias atrasadas y debidas.
2.º) Se proceda por el Letrado de la Administración de Justicia, sin previo requerimiento de pago, al embargo de los bienes designados en la relación fáctica de esta demanda y a librar los correspondientes despachos para que las entidades, registros y organismos reseñados informen de otros posibles bienes del ejecutado, ya que los designados por el ejecutante son insuficientes para responder de las responsabilidades reclamadas, todo ello con la finalidad de que mi poderdante sea satisfecho conforme al fallo de la sentencia de la que esta ejecución dimana.
3.º) Para que en lo sucesivo quede asegurada la prestación, se retenga del salario que D. percibe de la empresa " [DENOMINACIÓN SOCIAL] " la cantidad de [IMPORTE] euros mensuales, hasta nueva revalorización, oficiándose a la citada empresa a fin de que remita ésta a la c/c del Banco
4.º) Se aperciba al ejecutado, conforme al art. 776.1.ª LEC, que de incumplir de manera reiterada las obligaciones de pago de cantidad que le corresponden podrán imponérsele por el Letrado de la Administración de Justicia multas coercitivas, con arreglo a lo dispuesto en el art. 711 LEC y sin perjuicio de hacer efectivas sobre su patrimonio las cantidades debidas y no satisfechas.

Todo ello con imposición de las costas derivadas de esta ejecución al ejecutado.

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a

========================================================================
