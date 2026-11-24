---
name: demanda-ejecutiva-sentencia-firme-anula-clausula-suelo-civ-1396
description: "Demanda ejecutiva de sentencia firme que anula la cláusula suelo y ordena devolver cantidades. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda ejecutiva de sentencia firme que anula la cláusula suelo y ordena devolver cantidades

> Formulario **CIV-1396** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Demanda de ejecución de sentencia que declara nulidad de cláusula suelo con obligación de devolución de cantidades entregadas de más por aplicación de la citada cláusula declarada nula por abusiva.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda ejecutiva de sentencia firme que anula la cláusula suelo y ordena devolver cantidades» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda ejecutiva de sentencia firme que anula la cláusula suelo y ordena devolver cantidades” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:demanda-ejecutiva-sentencia-firme-anula-clausula-suelo-civ-1396`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (11 veces)
- [ ] FECHA (5 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] PARTE DEMANDADA (2 veces)
- [ ] DENOMINACIÓN SOCIAL
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] MES
- [ ] NÚMERO
- [ ] SECCIÓN
- [ ] SEDE

## Normas que cita el formulario

- art. 545.1 LEC
- art. 539.1 LEC
- art. 576 LEC
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

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a. de los Tribunales y de D./Dña. [NOMBRE Y APELLIDOS], cuya representación tengo acreditada en los autos de juicio ordinario sobre nulidad de cláusula suelo incorporada a contrato de préstamo hipotecario, registrados con el número [NÚMERO], seguidos frente a la entidad [DENOMINACIÓN SOCIAL], cuyos datos personales obran en las actuaciones, siguiendo instrucciones de mi mandante y como mejor proceda en derecho, DIGO:

Que mediante el presente escrito formulo DEMANDA EJECUTIVA contra [PARTE DEMANDADA], en reclamación de la cantidad de [IMPORTE] euros ( €) en concepto de principal, [IMPORTE] euros ( €) en concepto de intereses vencidos, así como de otros [IMPORTE] euros ( €) presupuestados inicialmente para los intereses que puedan devengarse durante la ejecución y las costas de ésta, todo ello según resulta de los siguientes:

HECHOS

PRIMERO.- El pasado día [FECHA] por el tribunal al que me dirijo se dictó sentencia cuyo fallo es del siguiente tenor literal:

"1º Debo declarar y declaro la nulidad de la condición general de la contratación descrita en el hecho primero de la demanda (cláusula suelo), es decir, de la cláusula del contrato de préstamo que establece un límite a la variación del tipo de interés, por tener el carácter de abusiva.

2º Debo condenar y condeno a la entidad, a eliminar dicha condición del contrato de préstamo hipotecario suscrito entre las partes.

3º Debo condenar y condeno a la entidad demandada a la devolución a los prestatarios de la cantidad deeuros que han sido abonados de más como consecuencia de la aplicación de la referida cláusula, con sus intereses legales devengados desde la fecha de cada cobro.

4º Debo condenar y condeno a la entidad demandada a devolver a los prestatarios todas aquellas cantidades que estos vayan pagando de más por la aplicación de la referida cláusula suelo, durante la tramitación de este procedimiento, con sus intereses legales devengados desde la fecha de cada cobro y hasta la resolución definitiva del pleito.

5º Todo ello, con imposición de las costas del presente procedimiento a la parte demandada condenada."

SEGUNDO.- Dicha sentencia ha devenido firme tras la desestimación del recurso de apelación fallado por la Sección [SECCIÓN] de la Audiencia Provincial de [LOCALIDAD], habiendo transcurrido más de veinte días desde que se notificó la resolución de condena al demandado.

TERCERO.- Dado que hasta la fecha no se han abonado por la entidad condenada las cantidades fijadas en la sentencia dictada en las presentes actuaciones, me veo en la necesidad de formular demanda ejecutiva.

CUARTO.- Mi patrocinado tiene conocimiento de que el ejecutado es titular de los siguientes bienes susceptibles de embargo:

QUINTO.- De conformidad con la sentencia que se ejecuta, la liquidación de las cantidades e intereses que en la misma se fijan, se efectúa conforme al siguiente cálculo:

BASES DE LIQUIDACIÓN

Capital inicial préstamo: [IMPORTE] euros.

Plazo inicial: años

Fecha de firma de la hipoteca:

Tipo de interés inicial: %

Revisión Semestral

Con el Euribor del mes de [MES]

Diferencial aplicable: %

Suelo: %

Cuota con suelo [IMPORTE] euros

Cuota sin suelo [IMPORTE] euros

LIQUIDACIÓN

Cantidades cobradas en aplicación del tipo mínimo por encima del interés variable más el diferencial fijado desde el a [FECHA] ascienden la suma de [IMPORTE] euros, reconocidos en sentencia, según el siguiente desglose:

Fecha abono	Importe	Intereses devengados

Cantidades cobradas en aplicación del tipo mínimo por encima del interés variable más el diferencial fijado desde [FECHA] a [FECHA] ascienden a [IMPORTE] euros, según el siguiente desglose:

Fecha abono	Importe	Intereses devengados

TOTAL:

FUNDAMENTOS DE DERECHO

I.- COMPETENCIA.

Según el art. 545.1 LEC, será competente para la ejecución de resoluciones judiciales y de transacciones y acuerdos judicialmente homologados o aprobados, el tribunal que conoció del asunto en primera instancia o el que homologó o aprobó la transacción o el acuerdo.

Por eso se presenta esta demanda ante el Tribunal al que gustosamente me dirijo, ya que fue quien dictó la sentencia de condena que sirve de título para la presente ejecución.

II.- LEGITIMACIÓN.

El art. 538 de la Ley de ritos regula que es parte en el proceso de ejecución la persona o personas que piden y obtienen el despacho de la ejecución y la persona o personas frente a las que ésta se despacha, añadiendo que sólo podrá despacharse ejecución a instancia de quien aparezca como acreedor en el título ejecutivo, entre otros, frente a quien aparezca como deudor en el mismo título.

Tratándose de la ejecución de una sentencia firme de condena, es obvio que mi patrocinado es el acreedor y el demandado es el deudor, tal y como concluye la parte dispositiva de la sentencia dictada en el juicio del que dimana esta demanda ejecutiva.

III.- POSTULACIÓN.

Conforme a lo dispuesto en el art. 539.1 LEC, la demanda viene firmada por abogado y Procurador/a., ya que estamos ante la ejecución de una resolución dictada en un proceso en que es preceptiva la intervención de dichos profesionales.

IV.- TÍTULO DE EJECUCIÓN.

El art. 517.2 ordinal 1.º LEC enumera como uno de los títulos que lleva aparejada ejecución la sentencia de condena firme, como la que sirve de fundamento a esta demanda.

V.- REQUISITOS TEMPORALES.

La resolución de condena se ha notificado al ejecutado hace más de veinte días (art. 548) y la demanda ejecutiva se ha interpuesto sin que hayan transcurrido los cinco años siguientes a la firmeza de la sentencia, que el art. 518 fija como de caducidad de la acción ejecutiva.

VI.- REQUISITOS FORMALES.

La presente demanda contiene todos los requisitos enumerados en el art. 549 de la Ley Procesal Civil, ya que se ha indicado cual es el título en que se funda, la tutela ejecutiva que se pretende y las personas frente a las que se interesa el despacho de la ejecución, así como los bienes del ejecutado susceptibles de embargo conocidos por mi poderdante. Por último se acompaña a la demanda ejecutiva la documentación necesaria de la contemplada en el art. 550 del mismo texto legal.

VII.- INTERESES.

Conforme a lo establecido en el art. 576 LEC, desde que fuere dictada sentencia en primera instancia, toda sentencia o resolución que condene al pago de una cantidad de dinero líquida determinará, a favor del acreedor, el devengo de un interés anual igual al del interés legal del dinero incrementado en dos puntos o el que corresponda por pacto de las partes o por disposición especial de la ley.

VIII.- COSTAS.

En virtud de lo dispuesto en el art. 539.2 en relación con el 583 LEC, las costas de esta ejecución deberán ser impuestas al ejecutado, ya que ha sido quien ha originado la necesidad de este procedimiento al no haber cumplido con lo establecido en la sentencia recaída en las presentes actuaciones.

De conformidad con lo anteriormente expuesto,

SUPLICO AL TRIBUNAL:

Que teniendo por presentado este escrito con los documentos acompañados y copia de todo ello, se sirva admitirlo, ordenando se entiendan conmigo las sucesivas diligencias y en nombre de mi patrocinado se tenga por presentada demanda ejecutiva para que, una vez examinados los requisitos y presupuestos procesales, el título ejecutivo y los actos de ejecución que se solicitan, así como la propia competencia, se despache ejecución frente a [PARTE DEMANDADA] por el importe de la cantidad de [IMPORTE] euros ( €) en concepto de principal, [IMPORTE] euros ( €) en concepto de intereses devengados hasta la fecha, más otros [IMPORTE] euros ( €) presupuestados provisionalmente para los intereses que puedan generarse durante la ejecución y las costas de ésta, procediéndose, sin previo requerimiento de pago, al embargo de las cuentas propias de la entidad demandada designadas en la relación fáctica de esta demanda, en concreto sobre la cuenta abierta en el Banco de España, todo ello con la finalidad de que mi poderdante sea satisfecho conforme al fallo de la sentencia de la que esta ejecución dimana. Todo ello con imposición de las costas derivadas de esta ejecución al ejecutado.

Por ser de Justicia que pido en [LUGAR], a [FECHA].

Firma de Abogado/a	Firma de Procurador/a
