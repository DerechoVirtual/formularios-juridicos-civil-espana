---
name: demanda-ejecutiva-gastos-extraordinarios-no-previstos-civ-1517
description: "Demanda ejecutiva de gastos extraordinarios no previstos en la resolución judicial. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda ejecutiva de gastos extraordinarios no previstos en la resolución judicial

> Formulario **CIV-1517** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Solicitud en demanda ejecutiva para la declaración de gasto extraordinario para que se despache ejecución forzosa por no estar expresamente previsto en la resolución judicial.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda ejecutiva de gastos extraordinarios no previstos en la resolución judicial» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda ejecutiva de gastos extraordinarios no previstos en la resolución judicial” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:demanda-ejecutiva-gastos-extraordinarios-no-previstos-civ-1517`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] NÚMERO (6 veces)
- [ ] FECHA (3 veces)
- [ ] NOMBRE DEL MENOR (2 veces)
- [ ] AÑO
- [ ] DENOMINACIÓN SOCIAL
- [ ] LUGAR
- [ ] Nº DE DOCUMENTO
- [ ] Nº DE PROCEDIMIENTO
- [ ] SECCIÓN
- [ ] SEDE

## Normas que cita el formulario

- art. 545.1 LEC
- art. 538 LEC
- art. 539.1 LEC
- art. 517.2.1.º LEC
- art. 549 LEC
- art. 550 LEC
- art. 576 LEC
- art. 539.2 LEC
- art. 776.4.ª LEC

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

D./Dña. [NOMBRE Y APELLIDOS], Procurador de los Tribunales, que actúa en nombre y representación de Doña [NOMBRE Y APELLIDOS], según tengo acreditado, junto con la dirección letrada y las circunstancias personales, en los autos de Juicio de divorcio n.º [Nº DE PROCEDIMIENTO]/[AÑO], seguidos a instancias de Doña Purificación [NOMBRE Y APELLIDOS] frente a Don [NOMBRE Y APELLIDOS], ante el Tribunal comparezco y como mejor proceda en Derecho, DIGO:

Que mediante el presente escrito formulo demanda ejecutiva contra Don [NOMBRE Y APELLIDOS], domiciliado en esta ciudad, n.º [NÚMERO], cuyas circunstancias constan en los autos principales, donde se halla personado, en reclamación de la cantidad deeuros (€), en concepto de principal,euros (€) en concepto de intereses devengados hasta la fecha, así como de otroseuros (€) presupuestados inicialmente para los intereses que puedan devengarse durante la ejecución y las costas de ésta, todo ello según resulta de los siguientes:

HECHOS

PRIMERO.- El día [FECHA] por el tribunal al que me dirijo se dictó sentencia de divorcio que en su parte dispositiva fijaba, entre otras medidas, la obligación de cada cónyuge al pago del 50% de los gastos extraordinarios del hijo menor de edad [NOMBRE DEL MENOR].

SEGUNDO.- Dicha sentencia fue recurrida en apelación por la actora, dictando la Sección [SECCIÓN] de la Audiencia Provincial sentencia de fecha [FECHA], que ratificó el referido pronunciamiento.

TERCERO.- Desde hace cuatro meses, ante las dificultades del menor en el habla y por indicación de su pediatra, [NOMBRE DEL MENOR] ha iniciado sesiones de logopeda, que se han venido repitiendo a razón de dos horas a la semana en módulos de media hora.

CUARTO.- Se ha requerido al padre del menor para que abone la mitad de los gastos derivados del necesario tratamiento, pues los mismos no están cubiertos por ninguna de las coberturas sanitarias de los progenitores, sin que se haya obtenido respuesta alguna.

Se acompañan testimonios de la sentencia de instancia y de la de apelación como documentos n.º [NÚMERO] y [Nº DE DOCUMENTO], el informe pediátrico como documento n.º [NÚMERO], las facturas del logopeda como bloque documental n.º [NÚMERO], así como los recibos de pago efectuados por la madre del menor, que también se acompañan como bloque documental n.º [NÚMERO]. Por último, se acompaña, como documento n.º [NÚMERO], el requerimiento de pago extrajudicial, desatendido por el ejecutado.

QUINTO.- Dado que no se han abonado por D. [NOMBRE Y APELLIDOS], las cantidades correspondientes al 50% de los gastos, me veo en la necesidad de formular demanda ejecutiva.

SEXTO.- Mi patrocinada tiene conocimiento de que el ejecutado está empleado por la Asesoría [DENOMINACIÓN SOCIAL] SL, con nómina fija que se domicilia en la cuenta bancaria del ejecutado.

FUNDAMENTOS DE DERECHO

I.- COMPETENCIA.

Según el art. 545.1 LEC, será competente para la ejecución de resoluciones judiciales, el tribunal que conoció del asunto en primera instancia.

Por eso se presenta esta demanda ante el Tribunal al que me honro en dirigirme, ya que fue quien conoció en primera instancia el proceso de divorcio.

II.- LEGITIMACIÓN.

Concurre legitimación ordinaria directa ejecutiva, activa y pasiva, según lo dispuesto en el art. 538 LEC, conforme al que es parte en el proceso de ejecución la persona o personas que piden y obtienen el despacho de la ejecución, y la persona o personas frente a las que ésta se despacha, añadiendo que sólo podrá despacharse ejecución a instancia de quien aparezca como acreedor en el título ejecutivo, y frente a quien aparezca como deudor en el mismo título.

Tratándose de la ejecución de unas resoluciones judiciales firmes, es obvio que mi patrocinada, como progenitor a quien se atribuyó la guarda del menor, y quien abonó en su integridad los gastos aquí reclamados, es el acreedor, y el demandado es el deudor, tal y como concluyen las partes dispositivas de las sentencias dictadas en el juicio.

III.- POSTULACIÓN.

Conforme a lo dispuesto en el art. 539.1 LEC, la demanda viene autorizada por abogado y procurador, ya que estamos ante la ejecución de una resolución dictada en un proceso en que es preceptiva la intervención de dichos profesionales, estando el apoderamiento documentado en el proceso de declaración.

IV.- TÍTULO DE EJECUCIÓN.

El art. 517.2.1.º LEC enumera como uno de los títulos que lleva aparejada ejecución la sentencia de condena firme.

V.- REQUISITOS FORMALES.

La presente demanda contiene todos los requisitos enumerados en el art. 549 LEC, ya que se ha indicado cual es el título en que se funda, la tutela ejecutiva que se pretende y la persona frente a la que se interesa el despacho de la ejecución, y los bienes del ejecutado susceptibles de embargo conocidos por mi poderdante. Por último, se acompaña a la demanda ejecutiva la documentación necesaria de la contemplada en el art. 550 LEC.

VI.- INTERESES.

Conforme a lo establecido en el art. 576 LEC, desde que fuere dictada sentencia en primera instancia, toda sentencia o resolución que condene al pago de una cantidad de dinero líquida determinará, a favor del acreedor, el devengo de un interés anual igual al del interés legal del dinero incrementado en dos puntos o el que corresponda por pacto de las partes o por disposición especial de la ley, lo cual debe entenderse desde el requerimiento de pago extrajudicial.

VII.- COSTAS.

En virtud de lo dispuesto en el art. 539.2 LEC en relación con el 583 LEC, las costas de esta ejecución deberán ser impuestas al ejecutado, ya que ha sido quien ha originado la necesidad de este procedimiento al no haber cumplido con lo establecido en las sentencias recaídas y en las tasaciones practicadas en las presentes actuaciones.

De conformidad con lo anteriormente expuesto,

SUPLICO AL TRIBUNAL

que, por presentado este escrito, con los documentos acompañados y copia de todo ello, se sirva admitir uno y otros, y en la representación que ostento se tenga por presentada demanda ejecutiva, ordenando se entiendan conmigo las sucesivas diligencias, y una vez examinados sus presupuestos, se despache ejecución frente a D.por el importe de la cantidad deeuros (€) en concepto de principal,euros (€) en concepto de intereses devengados hasta la fecha, más otroseuros (€) presupuestados provisionalmente para los intereses que puedan generarse durante la ejecución y las costas de ésta (TOTAL:euros), procediéndose, mediante decreto del Letrado de la Administración de Justicia y sin previo requerimiento de pago, a ordenar la retención del sueldo del ejecutado en cantidad suficiente para abonar las cantidades reclamadas. Todo ello con imposición de las costas derivadas de esta ejecución al ejecutado.

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a

OTROSÍ DIGO: De conformidad con el art. 776.4.ª LEC, y dado que en el fallo del título judicial que se trata de ejecutar se hace una referencia genérica a los gastos extraordinarios, se solicita que, con carácter previo a despachar ejecución, se declare expresamente que los gastos de logopeda revisten el concepto de gasto extraordinario, atendiendo al carácter no habitual de los mismos, al hecho de que se generan en atención a una disfunción en el habla del menor que no se pudo prever en su momento, y a su elevado importe. Deberá, por ello, darse traslado de esta solicitud al ejecutado para que en cinco días se posicione al respecto, se dé en virtud de su respuesta al mismo el curso señalado en la ley y, en su día, se dicte resolución declarando el referido carácter.

AL TRIBUNAL SUPLICO: Se sirva tener hecha la anterior manifestación y acuerde en consecuencia.

Reitero Justicia en lugar y fecha ut supra.

========================================================================
