---
name: auto-da-terminado-juicio-cambiario-despacha-ejecucion-civ-2105
description: "Auto que da por terminado el juicio cambiario y despacha ejecución con embargo ya practicado. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Auto que da por terminado el juicio cambiario y despacha ejecución con embargo ya practicado

> Formulario **CIV-2105** del plugin **Resoluciones judiciales civiles: autos, decretos y diligencias** (`formularios-resoluciones-judiciales-civiles`) · Civil › Resoluciones judiciales (autos, decretos, providencias, diligencias) · normativa revisada el 24-11-2026.

## Qué es

Auto declarando finalizado el juicio cambiario y despachando ejecución, con embargo de bienes ya practicado.

Es un modelo de tipo **resoluciones judiciales (autos, decretos, providencias, diligencias)**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Auto que da por terminado el juicio cambiario y despacha ejecución con embargo ya practicado» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Auto que da por terminado el juicio cambiario y despacha ejecución con embargo ya practicado” para mi caso». También puedes invocarla directamente con `/formularios-resoluciones-judiciales-civiles:auto-da-terminado-juicio-cambiario-despacha-ejecucion-civ-2105`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-resoluciones-judiciales-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Resoluciones judiciales civiles: autos, decretos y diligencias) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (8 veces)
- [ ] NÚMERO (3 veces)
- [ ] ACTO O RESOLUCIÓN (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] AÑO
- [ ] FECHA
- [ ] LUGAR
- [ ] NOMBRE DE LA PARTE
- [ ] NOMBRE DEL REPRESENTADO/A

## Normas que cita el formulario

- art. 821 LEC
- art. 825 LEC
- art. 556 LEC
- art. 553.2 LEC
- art. 823 LEC

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

Formulario actualizado conforme a Ley 16/2022, de 5 de septiembre, de reforma del texto refundido de la Ley Concursal, vigente desde 26 de septiembre de 2022.

Notas al pie del formulario original:
(1) Esta resolución es firme, y contra la misma no cabe recurso alguno, a tenor del art. 551.2 LEC, sin perjuicio de que el deudor pueda oponerse a la ejecución despachada dentro de los diez días siguientes a la notificación, por alguno de los motivos procesales y de fondo de la LEC, con los efectos previstos en su art. 556.2 LEC.

(2) El juicio cambiario se inicia por una verdadera demanda, en que se pide la ejecución para caso de producirse el presupuesto legal, y se prevé un embargo preventivo que, o bien estará pendiente, de modo que no se puede finalizar el juicio sin más, o bien estará practicado, de modo que no puede quedar indefinidamente vigente como tal medida cautelar especial.

Por ello, este auto se dicta de oficio, una vez transcurrido el plazo del requerimiento al deudor, sin perjuicio de que lógicamente nada impide que el demandante pueda solicitar el despacho de ejecución.

El modelo parte de la premisa de un embargo preventivo realizado, pero puede darse el caso de que no se haya realizado -por ejemplo, porque no se han hallado bienes del deudor-, y en tal caso, no se convierte el embargo preventivo en ejecutivo, sino que se decretará el embargo como en un despacho de ejecución cualquiera.

========================================================================


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

SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA N.º [NÚMERO]

PROCEDIMIENTO: Juicio Cambiario n.º [NÚMERO]/[AÑO]

Número de Identificación Informático:

PARTES:

AUTO

Ilmo. Sr./a. Magistrado-Juez/a D./Dña. [NOMBRE Y APELLIDOS]

En [LUGAR], a [FECHA].

ANTECEDENTES DE HECHO

PRIMERO.- Que ante este Tribunal se ha seguido juicio cambiario n.º [NÚMERO] a instancias de [NOMBRE DE LA PARTE] contra [ACTO O RESOLUCIÓN], en reclamación de la cantidad de [IMPORTE] euros ( [IMPORTE] €) como principal, y de [IMPORTE] euros ( [IMPORTE] €) en concepto de intereses de mora y costas del proceso, calculadas provisionalmente, sin perjuicio de ulterior definitiva liquidación, en el que se dictó auto que acordaba requerir de pago al deudor, por plazo de diez días, así como el embargo preventivo de sus bienes para asegurar las cantidades reclamadas.

SEGUNDO.- Se ha llevado a efecto el requerimiento de pago, habiendo transcurrido el plazo concedido al deudor sin que el mismo se haya personado, ni pagado, ni demandado de oposición; habiéndose llevado a efecto asimismo el embargo preventivo acordado.

RAZONAMIENTOS JURÍDICOS

PRIMERO.- Habiéndose cumplido los presupuestos para la admisión del juicio cambiario, mediante la adopción de las medidas de requerimiento de pago y embargo preventivo para caso de no atenderse al requerimiento en el plazo legal de diez días, conforme al art. 821 LEC, y verificándose en este momento nuevamente la competencia del Tribunal y la corrección formal de la letra de cambio legitimadora, no se ha producido el pago ni deducido demanda de oposición por el deudor.

SEGUNDO.- Se está en el caso de despachar ejecución conforme previene el art. 825 LEC, por la cantidad reclamada como principal, más la que se tiene calculada por intereses y costas, constituyendo la letra de cambio aportada título, como dispone el art. 66 de la Ley Cambiaria y del Cheque, y debe despacharse la ejecución conforme a lo dispuesto para la de sentencias y resoluciones judiciales y arbitrales, es decir, sin previo requerimiento de pago, y limitada la oposición a los motivos prevenidos en el art. 556 LEC, con oportuna notificación al ejecutado para que, según dispone el art. 553.2 LEC, en cualquier momento pueda personarse en la ejecución, por medio de Abogado y Procurador.

TERCERO.- Igualmente, procede llevar a efecto el embargo preventivo trabado como ejecutivo, previo a la vía de apremio que regula la nueva Ley procesal civil en su Libro III, ya que sólo se traba embargo ejecutivo, conforme al art. 825 LEC, cuando no se hubiera podido practicar antes en el juicio cambiario, o hubiera sido alzado por la previsión del art. 823 LEC.

En su virtud,

PARTE DISPOSITIVA

1.- Se declara finalizado el presente juicio cambiario.

2.- Se despacha, a instancias del Procurador/a. Sr/a. [NOMBRE Y APELLIDOS], en nombre y representación de [NOMBRE DEL REPRESENTADO/A], parte ejecutante, ejecución contra [ACTO O RESOLUCIÓN], parte ejecutada, por la cantidad principal de [IMPORTE] euros ( [IMPORTE] €), más los intereses moratorios conforme al título, que incrementa en la cantidad de [IMPORTE] euros ( [IMPORTE] €), prevista para hacer frente a la liquidación de los devengados y que puedan devengarse durante la ejecución, además que para pago de las costas de ésta, ejecución que se sustanciará conforme a lo previsto para la ejecución de las resoluciones judiciales o arbitrales.

Regístrese la ejecución como proceso de ejecución.

3.- Se decreta que los bienes embargados preventivamente se realizarán, a instancia de la parte demandante, conforme a lo previsto en la Ley para el procedimiento de apremio.

Así lo dispongo, mando y firmo.

Firma del Juez/a:
