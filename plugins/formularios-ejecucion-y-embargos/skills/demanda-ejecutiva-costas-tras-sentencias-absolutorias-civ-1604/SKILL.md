---
name: demanda-ejecutiva-costas-tras-sentencias-absolutorias-civ-1604
description: "Demanda ejecutiva de costas tras sentencias absolutorias conformes en instancia y apelación. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda ejecutiva de costas tras sentencias absolutorias conformes en instancia y apelación

> Formulario **CIV-1604** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Modelo de demanda ejecutiva en reclamación de las costas procesales más los intereses legales devengados, así como solicitando el embargo de un bien inmueble del ejecutado.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda ejecutiva de costas tras sentencias absolutorias conformes en instancia y apelación» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda ejecutiva de costas tras sentencias absolutorias conformes en instancia y apelación” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:demanda-ejecutiva-costas-tras-sentencias-absolutorias-civ-1604`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (9 veces)
- [ ] IMPORTE (7 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] NÚMERO (4 veces)
- [ ] CALLE DEL PASEO (3 veces)
- [ ] Nº (3 veces)
- [ ] SECCIÓN (3 veces)
- [ ] FOLIO (2 veces)
- [ ] NOMBRE DE LA PARTE (2 veces)
- [ ] SEDE (2 veces)
- [ ] TOMO (2 veces)
- [ ] AÑO
- [ ] DENOMINACIÓN SOCIAL
- [ ] HOJA
- [ ] LIBRO
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] NIF
- [ ] Nº DE LEY
- [ ] Nº DE PROCEDIMIENTO
- [ ] PARTE DEMANDADA
- [ ] PORCENTAJE

## Normas que cita el formulario

- art. 576 LEC
- art. 545.1 LEC
- art. 538 LEC
- art. 539.1 LEC
- art. 517.2.1.º LEC
- art. 242.1 LEC
- art. 549 LEC
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

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, que actúa en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS], según tengo acreditado, junto con la dirección letrada y las circunstancias personales, en los autos de Juicio ordinario n.º [Nº DE PROCEDIMIENTO]/[AÑO], seguidos a instancias de la mercantil [DENOMINACIÓN SOCIAL], ante el Tribunal comparezco y como mejor proceda en Derecho, DIGO:

Que mediante el presente escrito formulo demanda ejecutiva contra [PARTE DEMANDADA]., domiciliada en esta ciudad, Paseo de [CALLE DEL PASEO], cuyas circunstancias constan en los autos principales, D./Dña. [NOMBRE Y APELLIDOS] de se halla personada, en reclamación de la cantidad deeuros (€), en concepto de principal,euros (€) en concepto de intereses devengados hasta la fecha, así como de otroseuros (€) presupuestados inicialmente para los intereses que puedan devengarse durante la ejecución y las costas de ésta, todo ello según resulta de los siguientes:

HECHOS

PRIMERO.- El día [FECHA] por el tribunal al que me dirijo se dictó sentencia absolutoria que en su parte dispositiva condenaba al pago de las costas procesales a la parte demandante, [NOMBRE DE LA PARTE].

SEGUNDO.- Dicha sentencia fue recurrida en apelación por la actora, dictando la Sección [SECCIÓN] de la Audiencia Provincial sentencia de fecha [FECHA], que igualmente condenaba al pago de las costas procesales a [NOMBRE DE LA PARTE].

TERCERO.- Ambas condenas ilíquidas adquirieron firmeza cuando se notificó la resolución de condena de apelación al demandado, contra la que no cabía recurso ordinario alguno.

CUARTO.- Practicadas a solicitud de esta parte las tasaciones de costas en ambas instancias por las respectivas Secretarías, de la Sección [SECCIÓN] de la Audiencia Provincial y del Tribunal al que me dirijo, de fechas [FECHA] y [FECHA], respectivamente, se trasladaron a la contraparte, sin que impugnara, aprobándose mediante decreto de fecha [FECHA].

Se acompañan testimonios de la Audiencia como documento n.º [NÚMERO], y de las actuaciones de ese Tribunal como documento n.º [NÚMERO].

QUINTO.- Dado que no se han abonado por la sociedad condenada las cantidades fijadas en las liquidaciones aprobadas para las precitadas sentencias, me veo en la necesidad de formular demanda ejecutiva.

La tasación de segunda instancia asciende a un total de [IMPORTE] euros, habiendo devengado intereses legales del art. 576 LEC desde el [FECHA] hasta el presente en cantidad de [IMPORTE] euros (tipo de interés legal [PORCENTAJE] anual, según Disposición Adicional [Nº] de la Ley [Nº DE LEY], incrementado en dos puntos, sobre el capital en [Nº] días), y de la primera instancia a un total de [IMPORTE] euros, que han devengado desde el [FECHA] hasta el día de hoy [IMPORTE] euros (mismo tipo indicado sobre el capital en [Nº] días).

Ambas suman: principal de [IMPORTE] euros; intereses devengados de [IMPORTE] euros. Total crédito hasta la presentación de la demanda de [IMPORTE] euros

SEXTO.- Mi patrocinado tiene conocimiento de que la ejecutada -sociedad de responsabilidad limitada constituida el [FECHA], e inscrita en el Registro Mercantil de [LOCALIDAD], al tomo [TOMO], folio [FOLIO], hoja [HOJA], C.I.F. [NIF], con domicilio en Paseo de [CALLE DEL PASEO], y cuyo administrador general único es D./Dña. [NOMBRE Y APELLIDOS], resulta titular del siguiente bien inmueble susceptible de embargo:

FINCA URBANA. Local comercial del Paseo de [CALLE DEL PASEO], inscrita como n.º [NÚMERO], al folio [FOLIO] vto., libro [LIBRO], tomo [TOMO] de la Sección [SECCIÓN], moderna, del Registro de la Propiedad n.º [NÚMERO] de los de [SEDE].

FUNDAMENTOS DE DERECHO

I.- COMPETENCIA.

Según el art. 545.1 LEC, será competente para la ejecución de resoluciones judiciales, el tribunal que conoció del asunto en primera instancia.

Por eso se presenta esta demanda ante el Tribunal al que me honro en dirigirme, ya que fue quien conoció en primera instancia el proceso con las sentencias que sirven de título para la presente ejecución.

II.- LEGITIMACIÓN.

Concurre legitimación ordinaria directa ejecutiva, activa y pasiva, según lo dispuesto en el art. 538 LEC, conforme al que es parte en el proceso de ejecución la persona o personas que piden y obtienen el despacho de la ejecución, y la persona o personas frente a las que ésta se despacha, añadiendo que sólo podrá despacharse ejecución a instancia de quien aparezca como acreedor en el título ejecutivo, y frente a quien aparezca como deudor en el mismo título.

Tratándose de la ejecución de unas resoluciones judiciales firmes, es obvio que mi patrocinado es el acreedor y la demandada es la deudora, tal y como concluyen las partes dispositivas de las sentencias dictadas en el juicio.

III.- POSTULACIÓN.

Conforme a lo dispuesto en el art. 539.1 de la LEC, la demanda viene autorizada por abogado y procurador, ya que estamos ante la ejecución de una resolución dictada en un proceso en que es preceptiva la intervención de dichos profesionales, estando el apoderamiento documentado en el proceso de declaración.

IV.- TÍTULO DE EJECUCIÓN.

El art. 517.2.1.º LEC enumera como uno de los títulos que lleva aparejada ejecución la sentencia de condena firme, así como el art. 517.2.9.º a las demás resoluciones judiciales que legalmente llevan aparejada ejecución, estableciendo el art. 242.1 LEC, que cuando hubiere condena en costas, luego que sea firme, se procederá a su exacción por el procedimiento de apremio, previa su tasación.

V.- REQUISITOS FORMALES.

La presente demanda contiene todos los requisitos enumerados en el art. 549 LEC, ya que se ha indicado cual es el título en que se funda, la tutela ejecutiva que se pretende y la persona frente a la que se interesa el despacho de la ejecución, los bienes del ejecutado susceptibles de embargo conocidos por mi poderdante, así como las medidas de localización e investigación de otros bienes del ejecutado, dada la insuficiencia de los reseñados. Por último se acompaña a la demanda ejecutiva la documentación necesaria de la contemplada en el art. 550 del mismo texto legal.

VI.- INTERESES.

Conforme a lo establecido en el art. 576 LEC, desde que fuere dictada sentencia en primera instancia, toda sentencia o resolución que condene al pago de una cantidad de dinero líquida determinará, a favor del acreedor, el devengo de un interés anual igual al del interés legal del dinero incrementado en dos puntos o el que corresponda por pacto de las partes o por disposición especial de la ley, lo cual debe entenderse desde la resolución judicial firme que liquida la condena ilíquida.

VII.- COSTAS.

En virtud de lo dispuesto en el art. 539.2 en relación con el 583 LEC, las costas de esta ejecución deberán ser impuestas a la ejecutada, ya que ha sido quien ha originado la necesidad de este procedimiento al no haber cumplido con lo establecido en las sentencias recaídas y en las tasaciones practicadas en las presentes actuaciones.

De conformidad con lo anteriormente expuesto,

SUPLICO AL TRIBUNAL

que, por presentado este escrito, con los documentos acompañados y copia de todo ello, se sirva admitir uno y otros, y en la representación que ostento se tenga por presentada demanda ejecutiva, ordenando se entiendan conmigo las sucesivas diligencias, y una vez examinados sus presupuestos, se despache ejecución frente apor el importe de la cantidad deeuros (€) en concepto de principal,euros (€) en concepto de intereses devengados hasta la fecha, más otroseuros (€) presupuestados provisionalmente para los intereses que puedan generarse durante la ejecución y las costas de ésta (TOTAL:euros), procediéndose, sin previo requerimiento de pago, al embargo del bien inmueble designado en la relación fáctica de esta demanda, librando mandamientos de anotación en el Registro de la Propiedad, todo ello con imposición de las costas derivadas de esta ejecución a la ejecutada.

Es justicia de hacerse en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a

========================================================================
