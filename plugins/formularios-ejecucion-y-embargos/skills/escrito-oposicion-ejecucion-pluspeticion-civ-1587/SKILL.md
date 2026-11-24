---
name: escrito-oposicion-ejecucion-pluspeticion-civ-1587
description: "Escrito de oposición a la ejecución por pluspetición. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito de oposición a la ejecución por pluspetición

> Formulario **CIV-1587** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Escrito de oposición a la ejecución por pluspetición (art. 557.1.3.ª LEC): el ejecutado alega que se reclaman cantidades ya pagadas, pone a disposición del tribunal la cantidad que reconoce deber para obtener la suspensión de la ejecución, y pide que se declare que no procede la ejecución, con costas al ejecutante.

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito de oposición a la ejecución por pluspetición» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito de oposición a la ejecución por pluspetición” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:escrito-oposicion-ejecucion-pluspeticion-civ-1587`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE EN LETRA (5 veces)
- [ ] IMPORTE EN NÚMERO (5 veces)
- [ ] AÑO (4 veces)
- [ ] DÍA (4 veces)
- [ ] MES (4 veces)
- [ ] FIRMA (2 veces)
- [ ] CLASE DE JUICIO
- [ ] DNI/NIE
- [ ] DOMICILIO
- [ ] LOCALIDAD
- [ ] NOMBRE O DENOMINACIÓN DEL EJECUTADO
- [ ] NOMBRE O DENOMINACIÓN DEL EJECUTANTE
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] NOMBRE Y APELLIDOS O DENOMINACIÓN DEL EJECUTADO
- [ ] Nº
- [ ] Nº DE PROCEDIMIENTO
- [ ] Nº DE PROCEDIMIENTO DE EJECUCIÓN
- [ ] SEDE
- [ ] VENCIMIENTOS

## Normas que cita el formulario

- art. 557.1.3.ª LEC
- art. 560 LEC
- art. 561.3 LEC

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

- Junto a «…gaciones. A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

NOTAS PRÁCTICAS: La alegación exclusiva de la pluspetición como causa de oposición no suspende el curso de la ejecución, salvo que se ponga a disposición del Tribunal, para su entrega por el Letrado de la Administración de Justicia al ejecutante, la cantidad que el ejecutado considera debida. El plazo de formalización de la oposición es de 10 días desde la notificación del despacho de ejecución. Podrá solicitarse la celebración de vista en el escrito de oposición a la ejecución y en el de impugnación a la oposición. En los casos de ejecuciones dinerarias por saldo de operaciones o de intereses variables, el ejecutado podrá interesar que el Letrado de la Administración de Justicia encargado de la ejecución designe, mediante diligencia de ordenación, perito para que emita dictamen sobre el importe de la deuda, del que se dará traslado a las partes para que en cinco días presenten alegaciones.


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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS O DENOMINACIÓN DEL EJECUTADO], con domicilio en [DOMICILIO] y D.N.I. número [DNI/NIE], según tengo acreditado en los autos de juicio [CLASE DE JUICIO] seguidos ante este Tribunal con número de registro [Nº DE PROCEDIMIENTO] y de los que dimana el presente procedimiento de ejecución, comparezco y como mejor proceda en derecho DIGO:

Que en nombre de mi poderdante me persono en los autos de ejecución seguidos a instancia de [NOMBRE O DENOMINACIÓN DEL EJECUTANTE] y registrados con el número [Nº DE PROCEDIMIENTO DE EJECUCIÓN], y por medio del presente escrito formulo OPOSICIÓN a la citada ejecución, dentro del plazo concedido al efecto, en virtud de los siguientes

HECHOS

PRIMERO.– Por auto de fecha [DÍA] de [MES] de [AÑO] se despachó ejecución contra mi cliente en reclamación de la cantidad de [IMPORTE EN LETRA] euros ([IMPORTE EN NÚMERO] €) en concepto de principal e intereses devengados hasta la fecha, más otros [IMPORTE EN LETRA] euros ([IMPORTE EN NÚMERO] €) presupuestados provisionalmente para hacer frente a los intereses que, en su caso, puedan devengarse durante la ejecución y las costas de esta, auto que le fue notificado el pasado día [DÍA] de [MES] de [AÑO], por lo que el presente escrito se ha presentado dentro del término de diez días concedido al efecto para formular oposición.

SEGUNDO.– El motivo de la oposición es la equivocada imputación de impagos que se hace a mi representado/a en la demanda ejecutiva, la cual incurre en pluspetición, al incluir cantidades ya abonadas al ejecutante.

En efecto, el pasado día [DÍA] de [MES] de [AÑO] se efectuó un ingreso en la cuenta del ejecutante por importe de [IMPORTE EN LETRA] euros ([IMPORTE EN NÚMERO] €), que cubre las cantidades reclamadas correspondientes a los vencimientos de [VENCIMIENTOS], acompañándose como documento número 1 el resguardo de la mencionada consignación.

Por lo tanto, mi representado/a no adeuda la cantidad que reclama el ejecutante, sino la de [IMPORTE EN LETRA] euros ([IMPORTE EN NÚMERO] €), que se reconoce como debida, correspondiente a [CONCEPTO, por ejemplo, las últimas mensualidades de la vigencia del contrato].

TERCERO.– Esta parte pone a disposición del Tribunal, para su inmediata entrega al ejecutante, la cantidad de [IMPORTE EN LETRA] euros ([IMPORTE EN NÚMERO] €), por reconocerla como debida, a efectos de la suspensión de la ejecución despachada contra mi mandante, acompañando justificante de ingreso en efectivo, realizado en tal concepto en la cuenta de depósitos y consignaciones de este Tribunal, con identificación del presente procedimiento, el cual se une al presente escrito como documento número 2.

FUNDAMENTOS DE DERECHO

I.– Negamos que sean de aplicación al presente caso los fundamentos de derecho alegados por el ejecutante.

II.– Es causa de oposición a la ejecución, contemplada en el art. 557.1.3.ª LEC, la pluspetición, que deberá sustanciarse conforme a lo dispuesto en el art. 560 LEC, observándose en la tramitación las especialidades recogidas en el art. 558 del citado texto legal. De ahí que, acogiéndose a la posibilidad legal que recoge este último precepto, se solicite la inmediata entrega al ejecutante de la cantidad reconocida como debida y la suspensión de la ejecución mientras se tramita el incidente de oposición.

III.– En materia de costas procesales, a tenor de lo preceptuado en el art. 561.3 LEC, deberán ser impuestas al ejecutante.

En virtud de todo lo expuesto,

SUPLICO AL TRIBUNAL:

que tenga por presentado este escrito con sus copias y me tenga por comparecido/a y parte en la representación que ostento de [NOMBRE O DENOMINACIÓN DEL EJECUTADO] en el expresado procedimiento de ejecución y mande que se entiendan conmigo las actuaciones que a partir de este momento se realicen, teniendo por formulada, en tiempo y forma, oposición a la ejecución despachada y, admitiendo la cantidad puesta a disposición del Tribunal como reconocida, proceda a su entrega inmediata al ejecutante y acuerde consecuentemente la suspensión de la ejecución, para que, tras la correspondiente tramitación, se dicte auto declarando que no procede la ejecución, dejando esta sin efecto y mandando alzar los embargos y las medidas de garantía de la afección que se hubieran adoptado, reintegrándose al ejecutado a la situación anterior al despacho de la ejecución, con imposición de las costas al ejecutante.

Es de Justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

OTROSÍ DIGO que, conforme al art. 560 LEC, interesa al derecho de esta parte la celebración de vista, por lo que se solicita del Tribunal que se señale un día para su celebración dentro de los diez días siguientes a la conclusión del trámite de impugnación a este escrito de oposición.

Es justicia que reitero en lugar y fecha ut supra.

Firma del Abogado/a: [FIRMA] Firma del Procurador/a: [FIRMA]
