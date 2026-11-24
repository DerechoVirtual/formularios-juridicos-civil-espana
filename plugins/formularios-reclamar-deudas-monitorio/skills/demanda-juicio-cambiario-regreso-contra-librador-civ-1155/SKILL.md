---
name: demanda-juicio-cambiario-regreso-contra-librador-civ-1155
description: "Demanda de juicio cambiario por regreso contra el librador y directa contra el aceptante solidario. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio cambiario por regreso contra el librador y directa contra el aceptante solidario

> Formulario **CIV-1155** del plugin **Cobrar deudas: monitorio y cambiario** (`formularios-reclamar-deudas-monitorio`) · Civil › Monitorio y cambiario · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio cambiario sobre acción de regreso basada en una letra de cambio contra la mercantil libradora de la misma y solidariamente acción directa contra el aceptante.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio cambiario por regreso contra el librador y directa contra el aceptante solidario» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio cambiario por regreso contra el librador y directa contra el aceptante solidario” para mi caso». También puedes invocarla directamente con `/formularios-reclamar-deudas-monitorio:demanda-juicio-cambiario-regreso-contra-librador-civ-1155`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-reclamar-deudas-monitorio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Cobrar deudas: monitorio y cambiario) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] IMPORTE (5 veces)
- [ ] IMPORTE EN CIFRA (5 veces)
- [ ] Nº (4 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NOMBRE DE LA PARTE (2 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] DOMICILIO
- [ ] ENTIDAD BANCARIA
- [ ] FECHA
- [ ] FECHAS
- [ ] LUGAR
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] PARTE DEMANDADA

## Normas que cita el formulario

- art. 85.1 LOPJ
- art. 821.1 LEC
- art. 819 LEC
- art. 394 LEC

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

### Avisos de actualización (0) — se aplican en el texto, nunca se copian en el documento

- Ninguno.

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

AL TRIBUNAL

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a. de los Tribunales, en nombre y representación de la mercantil [NOMBRE DEL REPRESENTADO/A], como acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], ante el Tribunal comparezco y como mejor proceda en derecho, DIGO:

Que en la representación que ostento, y siguiendo las instrucciones de mi mandante, formulo demanda de Juicio Cambiario conjunta y solidariamente contra la mercantil [DENOMINACIÓN SOCIAL], con domicilio en [LOCALIDAD], en vía de regreso, por su condición de libradora de las cambiales que legitiman, y contra D./Dña. [NOMBRE Y APELLIDOS], domiciliado en [DOMICILIO], cuyo establecimiento profesional se haya sito en [LOCALIDAD], en vía directa, por su condición de aceptante de la misma; en reclamación de la cantidad de [IMPORTE] euros ([IMPORTE EN CIFRA] €) por principal, más intereses, gastos y costas procesales que se concretarán de seguido.

Dicha demanda se origina de los siguientes:

HECHOS

PRIMERO.- La entidad que represento es tenedora legítima de las letras de cambio que se acompañan como DOCUMENTOS NUMEROS [Nº] AL [Nº], por importe de [IMPORTE] euros ([IMPORTE EN CIFRA] €), vencimiento en fechas [FECHAS], las cuales fueron libradas por la sociedad [DENOMINACIÓN SOCIAL], a la orden de mi poderdante, y a cargo del otro demandado D./Dña. [NOMBRE Y APELLIDOS].

SEGUNDO.- Las antedichas letras de cambio extendidas a favor de mi mandante fueron endosadas por ésta a la Caja de Ahorros [ENTIDAD BANCARIA], que en las respectivas fechas de sus vencimientos las presentó para su pago al librado D./Dña. [NOMBRE Y APELLIDOS], quien no obstante haber aceptado debidamente dichas cambiales, no las hizo efectivas, por lo que la entidad bancaria domiciliataria extendió en el reverso de las letras la correspondiente nota de impago, conforme a lo prevenido en el art. 51 de la Ley Cambiaria y del Cheque.

TERCERO.- Ante el impago, la Caja de Ahorros tenedora cargó el importe de las letras en la cuenta de mi representada, al ser ésta quien se las había endosado, siendo devueltas, cargándose también los gastos correspondientes por el impago, siendo así la sociedad demandante legítima tenedora, según se ha manifestado.

Como DOCUMENTO NÚMERO [Nº DE DOCUMENTO] se adjunta nota de adeudo bancario de los gastos ocasionados par el cobro fallido, por un importe de [IMPORTE] euros ([IMPORTE EN CIFRA] €) que, adicionado al nominal de las letras impagadas, obtiene el total que por principal se reclama.

CUARTO.- Han resultado infructuosas las gestiones amistosas intentadas por mi mandante frente al aceptante y sociedad libradora para resarcirse del importe de su crédito. Se acompañan copias de telegramas y acuses de recibo remitidos al deudor (DOCUMENTOS NUMEROS [Nº] AL [Nº]).

A los anteriores hechos son de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

I.- COMPETENCIA.

Art. 820.pfo.2º LEC en relación con lo dispuesto en el art. 85.1º LOPJ, en cuanto se previene que será competente el Tribunal de Instancia del domicilio de cualquiera de los demandados, a elección del actor, cuando fueran obligados desde el mismo título, según es caso, y lo tuvieran diferente.

II.- LEGITIMACIÓN.

La legitimación activa corresponde a la sociedad demandante, que se afirma acreedora de lo que se reclama, a cuya orden fueron libradas por [NOMBRE DE LA PARTE], a cargo de D./Dña. [NOMBRE Y APELLIDOS], aceptante, las letras de cambio que son la base documental de la demanda así como tenedora legítima, una vez devueltas incobradas, conforme a los artículos 49, 50 y 57 de la Ley 19/85 de 16 de julio, Cambiaria y del Cheque (LCCh), mientras que la pasiva corresponde a los demandados por ser deudores de lo que se reclama, ya que [NOMBRE DE LA PARTE]. figura como libradora, y D./Dña. [NOMBRE Y APELLIDOS], como librado aceptante de la letra aportada.

Se aportan con la demanda las letras de cambio de las que es tenedor el titular de la acción cambiaria, conforme a la precisión de acreditación documental ‘in limine litis’ de la legitimación (art. 821.1 LEC).

III.- PROCEDIMIENTO.

El juicio cambiario, proceso declarativo especial y documental, de los arts. 819-27 LEC, al que se remite el art. 68 LCCh, reformado por Disposición Final 10ª.4 LEC, para cuando, como es el actual supuesto, se ejercita acción cambiaria al margen de la vía ordinaria común, conforme es opción ex art. 66 LCCh.

IV.- POSTULACIÓN Y DEFENSA.

Arts. 23 y 31 LEC, según los cuales no está excepcionado para el juicio cambiario que la comparecencia en juicio se efectúe por medio de Procurador, y bajo dirección y firma de Letrado.

V.- FONDO DEL ASUNTO.

Las letras de cambio, cuya regularidad formal resulta del cumplimiento de los requisitos legales de arts. 1 a 13 LCCh, facultan a su tenedor para el ejercicio de la acción directa, sin necesidad de protesto, contra el aceptante (art. 49.pfo.2º LCCh), y para el ejercicio de la acción de regreso, acreditándose la falta de pago, contra los endosantes, el librador y demás personas obligadas una vez advenido el vencimiento (art. 50 LCCh).

Tanto el protesto como la declaración denegatoria equivalente son medios suficientes para acreditar la falta de pago (art. 51 LCCh), figurando en el reverso de las letras adjuntadas la nota correspondiente a su impago puesta por el domiciliatario.

Los que han librado, aceptado, endosado o avalado una letra de cambio responden solidariamente frente al tenedor, teniendo el portador derecho a proceder contra todas estas personas individual o conjuntamente, sin que le sea indispensable observar el orden en que se hubieran obligado (art. 57 LCCH).

El art. 58 LCCh dispone que el tenedor podrá reclamar a la persona contra quien ejercite su acción: 1º El importe de la letra de cambio no aceptada o no pagada, con los intereses en ella indicados conforme al art. 6 LCCh. 2º Los réditos de la cantidad anterior devengados desde la fecha de vencimiento de la letra calculados al tipo de interés legal del dinero incrementado en dos puntos. 3º Los demás gastos, incluidos los del protesto y los de las comunicaciones.

VI.- COSTAS.

Deberán ser impuestas al demandado todas las costas procesales que se causen, aunque pagare en el acto del requerimiento (arts. 394 y 822 LEC).

Por lo expuesto,

SUPLICO AL TRIBUNAL,

que teniendo por presentado este escrito de demanda, acompañado de los documentos que legitiman, se sirva admitir uno y otros, teniéndome por parte en la representación que ostento, y mandando se sigan conmigo las sucesivas actuaciones, se tenga por deducido proceso especial cambiario por la cantidad de [IMPORTE] euros ([IMPORTE EN CIFRA] €) como principal, más la de [IMPORTE] euros ([IMPORTE EN CIFRA] €) que se calculan para intereses y costas, sin perjuicio de su ulterior liquidación, conjunta y solidariamente contra quienes se expresa:

En ejercicio de la acción de regreso, por su condición de libradora de las letras de cambio aportadas, contra [PARTE DEMANDADA], y en ejercicio de la acción directa, contra D./Dña. [NOMBRE Y APELLIDOS], en su condición de aceptante de las mismas

En su virtud, mande el Tribunal requerirles de pago a los deudores, por el orden que se ha indicado, y si no atendieran en el legal plazo de diez días, se haga efectivo y asegure embargo preventivo de bienes suficientes por las cantidades mentadas, y seguido que sea el juicio por sus trámites, se concluya despachando ejecución contra los demandados para pleno pago a la actora de las cantidades reclamadas, con expresa condena en costas y lo demás procedente,

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a
