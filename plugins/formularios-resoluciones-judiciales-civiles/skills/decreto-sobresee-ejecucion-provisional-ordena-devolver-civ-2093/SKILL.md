---
name: decreto-sobresee-ejecucion-provisional-ordena-devolver-civ-2093
description: "Decreto que sobresee la ejecución provisional y ordena devolver lo cobrado tras revocarse la condena. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Decreto que sobresee la ejecución provisional y ordena devolver lo cobrado tras revocarse la condena

> Formulario **CIV-2093** del plugin **Resoluciones judiciales civiles: autos, decretos y diligencias** (`formularios-resoluciones-judiciales-civiles`) · Civil › Resoluciones judiciales (autos, decretos, providencias, diligencias) · normativa revisada el 24-11-2026.

## Qué es

Decreto emitido por el Letrado de la Administración de Justicia acordando el sobreseimiento de la ejecución provisional acordada y requiriendo a la ejecutante para que proceda a la devolución de la cantidad percibida al haberse dictado sentencia totalmente revocatoria en recurso de apelación.

Es un modelo de tipo **resoluciones judiciales (autos, decretos, providencias, diligencias)**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Decreto que sobresee la ejecución provisional y ordena devolver lo cobrado tras revocarse la condena» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Decreto que sobresee la ejecución provisional y ordena devolver lo cobrado tras revocarse la condena” para mi caso». También puedes invocarla directamente con `/formularios-resoluciones-judiciales-civiles:decreto-sobresee-ejecucion-provisional-ordena-devolver-civ-2093`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-resoluciones-judiciales-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Resoluciones judiciales civiles: autos, decretos y diligencias) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] FECHA (4 veces)
- [ ] DENOMINACIÓN SOCIAL (3 veces)
- [ ] NÚMERO (2 veces)
- [ ] GRUPO
- [ ] IMPORTE
- [ ] IMPORTE EN LETRA
- [ ] LOCALIDAD
- [ ] LUGAR

## Normas que cita el formulario

- art. 533.1 LEC
- art. 533 LEC
- art. 451 LEC

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

SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA N.º [NÚMERO]

PROCEDIMIENTO

Número de identificación informático:

PARTES:

DECRETO DEL LETRADO DE LA ADMINISTRACIÓN DE JUSTICIA

Sr. Letrado de la Administración de Justicia [NOMBRE Y APELLIDOS]

En la Villa de [LOCALIDAD], a [FECHA]

ANTECEDENTES DE HECHO

I.- A instancias de D./Dña. [NOMBRE Y APELLIDOS], representada por la Procurador/a Sr./a. [NOMBRE Y APELLIDOS], mediante auto de [FECHA] se acordó la ejecución provisional total de la sentencia dictada por este Tribunal el [FECHA], procediéndose a formar pieza separada.

II.- Revocada la sentencia a que se refiere el hecho anterior, por el/la Procurador/a Sr./a. [NOMBRE Y APELLIDOS], en nombre y representación de la [DENOMINACIÓN SOCIAL] SEGUROS Y REASEGUROS [DENOMINACIÓN SOCIAL], S.A., se ha presentado escrito que solicitaba el sobreseimiento de la ejecución provisional y la devolución de las cantidades satisfechas, costas de la instancia y resarcimiento de daños y perjuicios que calcula.

RAZONAMIENTOS JURÍDICOS

ÚNICO.-

Con arreglo al art. 533.1 LEC, despachada ejecución provisional de la sentencia de instancia, se ha dictado sentencia totalmente revocatoria en recurso de apelación, y siendo de condena al pago de dinero, procede sobreseer la ejecución provisional de la sentencia revocada, y faculta al que ha obtenido el pronunciamiento revocatorio a su favor para pretender por la vía de apremio la devolución de las cantidades percibidas por el ejecutante, y reintegro de las costas de la ejecución provisional satisfechas, así como el resarcimiento de daños y perjuicios que dicha ejecución le hubiere ocasionado.

En virtud de lo expuesto,

PARTE DISPOSITIVA

1.- Se acuerda el sobreseimiento de la ejecución provisional acordada a instancias de D./Dña. [NOMBRE Y APELLIDOS], representada por el/la Procurador/a de los Tribunales D./Dña. [NOMBRE Y APELLIDOS], frente a SEGUROS Y REASEGUROS [DENOMINACIÓN SOCIAL], S.A., representada por el Procurador/a de los Tribunales D./Dña. [NOMBRE Y APELLIDOS].

2.- Requiérase a D./Dña. [NOMBRE Y APELLIDOS], bajo apercibimiento de la vía de apremio a instancias de la parte ejecutada, para que en el plazo de los diez días hábiles siguientes a la notificación proceda a la devolución de la cantidad percibida, que asciende a [IMPORTE EN LETRA] xx [IMPORTE] euros.

3.- Confiérase traslado a la parte ejecutada de la relación de daños y perjuicios ocasionados en la ejecución provisional que efectúa la parte ejecutante, para que le sean resarcidos con arreglo al art. 533 LEC, a fin de que en el plazo de diez días, conteste lo que estime conveniente, con apercibimiento de que si deja pasar el plazo sin evacuar el traslado o se limita a negar genéricamente la existencia de daños y perjuicios, sin concretar los puntos en que discrepa de la relación presentada, ni expresar las razones y el alcance de la discrepancia, se entenderá que muestra su conformidad a los hechos alegados por el ejecutante.

4.- Practíquese, como se solicita por la parte ejecutada, la tasación de costas del juicio en la instancia, incluida ejecución provisional.

Así lo acuerdo y firmo:

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Letrado/a de la Administración de Justicia:

Contra esta resolución cabe recurso de reposición, que debe interponerse por escrito ante el LAJ en plazo de cinco días hábiles contados desde el siguiente al de notificación, con expresión de la infracción cometida a juicio del recurrente, no obstante, lo cual, se llevará a efecto lo acordado (arts. 451 y 452 LEC).

Para interponer el recurso será necesario la constitución de un depósito de 25 euros, sin cuyo requisito no será admitido a trámite. El depósito se constituirá consignando dicho importe en la Cuenta de Depósitos y Consignaciones que este Tribunal tiene abierta en el grupo [GRUPO] con el número [NÚMERO], indicando en el campo concepto del resguardo de ingreso que se trata de un "Recurso" código 00-Reposición. La consignación deberá ser acreditada al interponer el recurso (disp. adic. 15.ª de la LOPJ).

Están exentos de constituir el depósito para recurrir los incluidos en el apartado 5 de la disposición citada y quienes tengan reconocido el derecho a la asistencia jurídica gratuita.

========================================================================
