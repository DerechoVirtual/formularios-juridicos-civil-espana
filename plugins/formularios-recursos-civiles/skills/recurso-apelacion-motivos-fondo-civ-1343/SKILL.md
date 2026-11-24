---
name: recurso-apelacion-motivos-fondo-civ-1343
description: "Recurso de apelación por motivos de fondo. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Recurso de apelación por motivos de fondo

> Formulario **CIV-1343** del plugin **Recursos civiles: reposición, apelación, casación y queja** (`formularios-recursos-civiles`) · Civil › Recursos · normativa revisada el 24-11-2026.

## Qué es

Escrito de interposición de recurso de apelación por el demandante contra sentencia desestimatoria (arts. 457 y siguientes LEC), fundado en motivos de fondo: error en la valoración de la prueba e infracción de la norma sustantiva. El modelo desarrolla, como ejemplo, una reclamación por accidente de circulación (art. 1902 del Código Civil) en la que la sentencia absuelve por entender no acreditado quién cruzó el semáforo en rojo.

Es un modelo de tipo **recursos**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Recurso de apelación por motivos de fondo» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Recurso de apelación por motivos de fondo” para mi caso». También puedes invocarla directamente con `/formularios-recursos-civiles:recurso-apelacion-motivos-fondo-civ-1343`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-recursos-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Recursos civiles: reposición, apelación, casación y queja) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (6 veces)
- [ ] FECHA (3 veces)
- [ ] Nº DE PROCEDIMIENTO (2 veces)
- [ ] AÑO
- [ ] CUERPO POLICIAL
- [ ] DÍA
- [ ] FECHA DE LA RESOLUCIÓN QUE ACTUALIZA LAS CUANTÍAS DEL BAREMO
- [ ] IMPORTE TOTAL
- [ ] LOCALIDAD
- [ ] MES
- [ ] NOMBRE Y APELLIDOS DEL APELANTE
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] NOMBRES Y APELLIDOS DE LOS TESTIGOS
- [ ] Nº
- [ ] PRONUNCIAMIENTO SOLICITADO
- [ ] PROVINCIA
- [ ] SEDE

## Normas que cita el formulario

- art. 458 LEC
- art. 1902 Código Civil
- art. 376 LEC
- art. 386 LEC
- art. 386.2 LEC
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

PROCESO NÚMERO [Nº DE PROCEDIMIENTO]

A LA AUDIENCIA PROVINCIAL DE [PROVINCIA]

Don/Doña [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, en nombre y representación de Don/Doña [NOMBRE Y APELLIDOS DEL APELANTE], parte demandante en este proceso seguido con el número [Nº DE PROCEDIMIENTO], según tengo acreditado en autos, ante el Tribunal comparezco y como mejor proceda en Derecho, DIGO:

1) Que en fecha [FECHA] se dictó sentencia en este proceso, la cual fue notificada a esta parte en fecha [FECHA].

2) Que entendiendo que dicha sentencia no es ajustada a derecho, dicho sea con los debidos respetos y en términos de defensa, por medio del presente escrito interpongo contra la misma RECURSO DE APELACIÓN, impugnando todos sus pronunciamientos, tanto el desestimatorio de la demanda como la condena en costas a mi representado/a.

3) Que, de conformidad con lo dispuesto en el art. 458 de la LEC, fundo el recurso de apelación en las siguientes

ALEGACIONES

PRIMERO.- Error en la valoración de la prueba e infracción del art. 1902 del Código Civil.

La sentencia de instancia absuelve al demandado por entender que no ha quedado acreditado cuál de los dos conductores rebasó el semáforo en fase roja, lo cual entendemos que constituye una conclusión fáctica derivada de una errónea valoración del resultado de la prueba practicada, como expondremos a continuación.

En efecto, la cuestión fáctica controvertida quedaba reducida a si el vehículo del demandado rebasó el semáforo en fase roja. En relación con este hecho se practicó prueba de interrogatorio de las partes, testifical de los testigos Sres. [NOMBRES Y APELLIDOS DE LOS TESTIGOS], cuyo resultado puede constatar la Sala, que tiene a su disposición el soporte de grabación de la vista, y documental, consistente en el atestado policial redactado por [CUERPO POLICIAL] que obra como documento número 1 de la demanda.

Entendemos que el resultado de esta prueba acredita claramente que fue el demandado quien rebasó el semáforo en fase roja, a diferencia de la sentencia de instancia, que aplica erróneamente las reglas de distribución de la carga de la prueba. Así, y ante las versiones ofrecidas contradictoriamente, tanto en los escritos alegatorios como en el juicio, en la prueba de interrogatorio de las partes, debemos acudir a la prueba testifical, donde los dos testigos propuestos por esta parte afirmaron rotundamente que el vehículo de mi representado/a rebasó el semáforo en fase verde, de lo que se concluye que el demandado rebasó el semáforo en fase roja. A la hora de valorar esta prueba, conforme a las reglas de la sana crítica a que se refiere el art. 376 de la LEC, debemos subrayar a la Sala que el testimonio de estas personas presenta plenas garantías de veracidad, por varias causas: por una parte, desde un primer momento se trata de testigos que se hallaban presentes en el lugar del accidente, y así consta expresamente su identidad en el atestado policial, concretamente en el folio número [Nº] del atestado, donde se refiere que estos testigos circulaban en sendos vehículos detrás del turismo de mi representado/a; y, por otra parte, estos testigos no tienen relación alguna con mi representado/a, siendo que además ni tan siquiera se conocen entre ellos. En cuanto al contenido del testimonio, ambos testigos afirmaron sin ningún tipo de dudas que vieron cómo el vehículo de mi representado/a rebasaba el semáforo cuando ya se hallaba en fase verde, de lo que se deriva claramente que fue el demandado el que rebasó el semáforo en fase roja.

Al respecto, el art. 386 de la LEC permite tener como probado este hecho, pues ha quedado totalmente demostrado que mi representado/a rebasó el semáforo en fase verde, por lo que es lógico deducir que el semáforo del demandado estaba en fase roja, pues es notorio que existe coordinación entre las señales luminosas. Aquí debe hacerse notar a la Sala que en ningún momento se propuso prueba de contrario tendente a desvirtuar tal conclusión, cuando desde el escrito inicial de demanda hemos mantenido la misma versión fáctica, limitándose el demandado a afirmar que tenía el semáforo en fase verde y sin proponer prueba de descargo como le autorizaba el art. 386.2 de la LEC, por lo que entendemos que el hecho ha quedado plenamente probado. En este punto, entendemos que la sentencia de instancia infringe este precepto, pues no lo aplicó en momento alguno, lo que determinó la desestimación de la demanda.

Partiendo de los anteriores hechos, son de plena aplicación los fundamentos de derecho alegados en nuestro escrito de demanda, debiéndose condenar al demandado por aplicación del art. 1902 del Código Civil, debiendo fijarse la cuantía de [IMPORTE TOTAL] euros en concepto de responsabilidad civil tal como solicitábamos en nuestro escrito de demanda, a razón de [IMPORTE] euros por los días de baja y de [IMPORTE] euros por las secuelas sufridas, incluyendo el grado de invalidez absoluta que se acredita de la prueba practicada; las cuantías por lesiones y secuelas están dentro de la aplicación del baremo con los incrementos señalados al tener mi defendido/a unos ingresos anuales de [IMPORTE] euros, hecho no controvertido; en orden al quantum de la indemnización tomamos las cuantías establecidas en la resolución de fecha [FECHA DE LA RESOLUCIÓN QUE ACTUALIZA LAS CUANTÍAS DEL BAREMO], de donde resulta la aplicación de una cuantía de [IMPORTE] euros por día impeditivo y la cantidad de [IMPORTE] euros señalada para las secuelas, teniendo en cuenta que las mismas le impiden el desarrollo de las tareas de cualquier profesión, por lo que la cantidad solicitada se ajusta plenamente a dicha resolución.

Respecto de las costas, ante la estimación total de las pretensiones de la demanda, que se considera procedente en caso de verse aceptado este recurso, se considera que las mismas deben imponerse en su integridad a la demandada (art. 394 LEC).

En base a lo anterior,

SUPLICO A LA SALA: que tenga por presentado este escrito con justificante de traslado a las demás partes, teniendo por interpuesto el recurso de apelación frente a la sentencia dictada por el Tribunal de Instancia de [SEDE] en las presentes actuaciones de fecha [FECHA] y, tras la pertinente tramitación y remisión de las actuaciones a la Ilma. Audiencia Provincial, se dicte por ésta sentencia en la que, declarando haber lugar al recurso de apelación presentado, se condene a la demandada a [PRONUNCIAMIENTO SOLICITADO], con imposición de las costas de instancia.

OTROSÍ PRIMERO DIGO que, de conformidad con lo dispuesto en los apartados 3.b) y 6 de la disposición adicional decimoquinta de la LOPJ, acompaño a este escrito resguardo de consignación en la cuenta de Depósitos y Consignaciones abierta a nombre del Tribunal del depósito exigido para interponer el recurso, por importe de [IMPORTE] euros.

SUPLICO A LA SALA que tenga por hecha la anterior manifestación a los efectos pertinentes y por constituido el depósito, dejando interesada su devolución para el caso de estimación total o parcial del recurso.

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma de Procurador/a y Abogado/a.
