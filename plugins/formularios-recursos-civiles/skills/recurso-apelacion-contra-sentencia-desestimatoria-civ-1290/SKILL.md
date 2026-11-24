---
name: recurso-apelacion-contra-sentencia-desestimatoria-civ-1290
description: "Recurso de apelación contra sentencia desestimatoria en un proceso declarativo de tráfico. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Recurso de apelación contra sentencia desestimatoria en un proceso declarativo de tráfico

> Formulario **CIV-1290** del plugin **Recursos civiles: reposición, apelación, casación y queja** (`formularios-recursos-civiles`) · Civil › Recursos · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **recursos**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Recurso de apelación contra sentencia desestimatoria en un proceso declarativo de tráfico» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Recurso de apelación contra sentencia desestimatoria en un proceso declarativo de tráfico” para mi caso». También puedes invocarla directamente con `/formularios-recursos-civiles:recurso-apelacion-contra-sentencia-desestimatoria-civ-1290`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-recursos-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Recursos civiles: reposición, apelación, casación y queja) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (7 veces)
- [ ] FECHA (4 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] AÑO
- [ ] DÍA
- [ ] FOLIO
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] MES
- [ ] Nº
- [ ] NÚMERO
- [ ] PRONUNCIAMIENTOS IMPUGNADOS
- [ ] SEDE

## Normas que cita el formulario

- art. 458 LEC
- art. 1902 Código Civil
- art. 1902 CC
- art. 1 Real Decreto Legislativo 8/2004
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

### Avisos de actualización (2) — se aplican en el texto, nunca se copian en el documento

- Junto a «…A LA SECCIÓN CIVIL DE LA AUDIENCIA PROVINCIAL DE [LOCALIDAD]»: La AP no tiene «Sección Civil» como denominación legal: se cita la Sección por su número (p. ej. «A LA SECCIÓN [ ] DE LA AUDIENCIA PROVINCIAL DE [ ]»). Fuente: LOPJ arts. 80 y 82 (Audiencia Provincial, sin cambio de denominación).
- Junto a «…dictada por la sección civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

A LA SECCIÓN CIVIL DE LA AUDIENCIA PROVINCIAL DE [LOCALIDAD]

D [NOMBRE Y APELLIDOS], Procurador de los Tribunales, en nombre y representación de D [NOMBRE Y APELLIDOS], parte demandante en este proceso seguido con el número [NÚMERO], según tengo acreditado en autos, ante la Sala comparezco y como mejor proceda en derecho DIGO:

1) Que en fecha [FECHA] se dictó sentencia en este proceso, la cual fue notificada a esta parte en fecha [FECHA]

2) Que entendiendo que dicha sentencia no es ajustada a derecho, dicho sea con los debidos respetos y en términos de defensa, por medio del presente escrito interpongo contra la misma RECURSO DE APELACIÓN (se harían constar los pronunciamientos que se impugnan [PRONUNCIAMIENTOS IMPUGNADOS]) impugnando todos sus pronunciamientos, tanto el desestimatorio de la demanda como la condena en costas a mi representado.

3) Que, de conformidad a lo dispuesto en el art. 458 de la LEC, fundo el recurso de apelación en los siguientes

MOTIVOS

Error en la valoración de la prueba. Inaplicación del principio de inversión de la carga de la prueba.

La sentencia de instancia absuelve a los demandados por entender que no ha quedado acreditado que concurriera culpa en el conductor del vehículo, si bien aceptando que la realidad del siniestro y el resultado lesivo.

Sin embargo, la sentencia infringe la reiterada doctrina que invierte la carga de la prueba cuando, como en este caso, el demandado realizaba una actividad de conducción, potencialmente peligrosa, en el curso de la cual atropelló a mi representado. Como se ha venido reiterando en la doctrina jurisprudencial, quien crea un riesgo con su actividad u obtiene beneficio de la existencia del riesgo mismo, sea o no lucrativo, debe extremar todas las precauciones y agotar los medios para evitar la concurrencia de aquellas circunstancias que cabe controlar y pueden generar daños efectivos. Por ello, tiene dicho reiteradamente el Tribunal Supremo que, en estos casos, ha de tener lugar la inversión de la carga de la prueba, que obliga a quien produce el riesgo o se beneficia del mismo a demostrar que en la producción del resultado dañoso, derivado causalmente de ese riesgo, no ha tenido ninguna actuación negligente, al haber obrado con la mayor y más atenta diligencia y prudencia, o que bien que el suceso se debió a caso fortuito, fuerza mayor o lo produjo el exclusivo actuar imprudente de la víctima.

Pues bien, en este caso, en la valoración que se realiza en la resolución de instancia no se toma en cuenta el criterio rector de valoración probatoria antes expresado, afirmándose en la sentencia que "no consta que el demandante cruzara por el paso de peatones habilitado al efecto", motivo en el que se funda la desestimación, cuando lo cierto es que de las huellas de frenada del vehículo reflejadas en el informe técnico de los agentes de la Guardia Civil (folio [FOLIO]), así como de la velocidad estimada del turismo, se desprende claramente que fue el conductor quien no adoptó las medidas de precaución necesarias en el ejercicio de su actividad de conducción, por lo que la sentencia recurrida llega a una conclusión fáctica derivada de una errónea valoración del resultado de la prueba practicada, al no tomar en consideración los diferentes elementos probatorios practicados en la instancia y al aplicar el principio de inversión de la carga de la prueba que rige en esta materia, según reiterada doctrina jurisprudencial.

En efecto, del resultado de la prueba se acredita claramente que fue el demandado quien no adoptó las medidas de precaución necesarias ante la presencia del peatón, circulando con exceso de velocidad, y no respetando el paso de peatones por el que cruzaba. Ninguna prueba existe de que mi representado cruzara por fuera del paso de cebra, de manera que imponer la carga de la prueba al demandante sobre este extremo infringe el principio de inversión, rector en la materia.

Por todo ello, se solicita la íntegra revocación de la sentencia, al existir responsabilidad del demandado, y por ende de la aseguradora, en estos hechos, de acuerdo a la correcta valoración de la prueba practicada.

Infracción de los artículos 1 y 6 del Real Decreto Legistativo 8/2004, de 29 de octubre, en relación con el artículo 1902 del Código Civil.

Partiendo de los anteriores hechos, son de plena aplicación los fundamentos de derecho alegados en nuestro escrito de demanda, al amparo de lo dispuesto en el art. 1902 del CC en relación con el artículo 1 del Real Decreto Legislativo 8/2004, de 29 de octubre, por el que se aprueba el texto refundido de la Ley sobre responsabilidad civil y seguro en la circulación de vehículos a motor, de tal manera que es el conductor demandado el responsable del siniestro, en virtud del riesgo creado por la conducción del vehículo, debiendo indemnizar de los daños causados a personas o bienes con motivo de la circulación debidos exclusivamente a su falta de diligencia al no haber concurrido culpa o negligencia de clase alguna por parte del perjudicado ni fuerza mayor extraña a la conducción o al funcionamiento del vehículo. Asimismo, y conforme al art. 6 del texto refundido de la Ley sobre responsabilidad civil y seguro en la circulación de vehículos a motor, mi representado tiene acción directa contra la entidad aseguradora, debiéndose declarar la responsabilidad solidaria de ambos con las consecuencias indemnizatorias postuladas en nuestro escrito de demanda.

De acuerdo a lo solicitado y al resultado de la prueba practicada en primera instancia, debe fijarse la cuantía de [IMPORTE] euros en concepto de responsabilidad civil, a razón de [IMPORTE] euros por los días de baja, de [IMPORTE] euros por las secuelas sufridas, incluyendo el grado de invalidez absoluta que se acredita de la prueba practicada; las cuantías por lesiones y secuelas están dentro de la aplicación del baremo con los incrementos señalados al tener mi defendido unos ingresos anuales de [IMPORTE] euros, hecho no controvertido; en orden al quantum de la indemnización tomamos las cuantías establecidas en la Resolución de fecha [FECHA], de donde resulta la aplicación de una cuantía de [IMPORTE] euros por día impeditivo y la cantidad de [IMPORTE] euros señalada para las secuelas, teniendo en cuenta que las mismas le impiden el desarrollo de las tareas de cualquier profesión, por lo que la cantidad solicitada se ajusta plenamente a dicha resolución.

Respecto de las costas del proceso de instancia, ante la estimación total de las pretensiones de la demanda que se considera procedente en caso de verse aceptado este recurso, las mismas deben imponerse en su integridad a la demandada (art. 394 LEC).

En base a lo anterior,

SUPLICO A LA SALA que tenga por presentado este escrito con justificante de traslado a las demás partes, teniendo por interpuesto el recurso de apelación frente a la sentencia dictada por la sección civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº] , en las presentes actuaciones de fecha [FECHA] y tras la pertinente tramitación, se dicte por esta Ilma. Audiencia Provincial sentencia en la que declarando haber lugar al recurso de apelación presentado, revocando la sentencia de instancia y acordando la estimación de la demanda deducida por mi representado, condenando a los demandados a indemnizar solidariamente a mi principal en la cantidad de [IMPORTE] euros, con más los intereses correspondientes, con imposición de las costas de instancia a los citados demandados.

OTROSÍ PRIMERO DIGO que, de conformidad con lo dispuesto en los apartados 3.b) y 6 de la disposición adicional decimoquinta de la LOPJ acompaño a este escrito resguardo de consignación en la cuenta de Depósitos y Consignaciones abierta a nombre del Tribunal del depósito exigido para interponer el recurso por importe de 50 euros.

SUPLICO A LA SALA que tenga por hecha la anterior manifestación a los efectos pertinentes y por acompañado el documento justificativo del abono de la tasa.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma Procurador y Abogado

========================================================================
