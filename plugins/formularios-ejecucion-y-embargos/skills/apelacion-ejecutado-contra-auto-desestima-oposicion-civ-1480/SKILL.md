---
name: apelacion-ejecutado-contra-auto-desestima-oposicion-civ-1480
description: "Apelación del ejecutado contra el auto que desestima la oposición (auto de cuantía máxima). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Apelación del ejecutado contra el auto que desestima la oposición (auto de cuantía máxima)

> Formulario **CIV-1480** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **recursos**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Apelación del ejecutado contra el auto que desestima la oposición (auto de cuantía máxima)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Apelación del ejecutado contra el auto que desestima la oposición (auto de cuantía máxima)” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:apelacion-ejecutado-contra-auto-desestima-oposicion-civ-1480`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (4 veces)
- [ ] IMPORTE (3 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] ASEGURADORA
- [ ] AÑO
- [ ] DÍA
- [ ] FOLIO
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] MES
- [ ] MINUTOS DE LA GRABACIÓN
- [ ] NÚMERO

## Normas que cita el formulario

- art. 561.3 LEC
- art. 458 LEC
- art. 556.3.1 LEC
- art. 556.3.2 LEC
- art. 561.1 LEC

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

- Junto a «…A LA SECCIÓN CIVIL DE LA AUDIENCIA PROVINCIAL DE [LOCALIDAD]»: La AP no tiene «Sección Civil» como denominación legal: se cita la Sección por su número (p. ej. «A LA SECCIÓN [ ] DE LA AUDIENCIA PROVINCIAL DE [ ]»). Fuente: LOPJ arts. 80 y 82 (Audiencia Provincial, sin cambio de denominación).

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

D. [NOMBRE Y APELLIDOS], Procurador de los Tribunales, en nombre y representación de la aseguradora [ASEGURADORA], parte ejecutada en este proceso seguido con el número [NÚMERO], según tengo acreditado en autos, ante el Tribunal comparezco y como mejor proceda en derecho DIGO:

1) Que en fecha [FECHA] se ha dictado auto desestimando la oposición a la ejecución despachada por auto de fecha [FECHA], el cual ha sido notificado a esta parte en fecha

2) El auto que se impugna es apelable directamente al amparo del art. 561.3 de la LEC.

3) Al amparo del citado precepto, entendiendo que dicha resolución no es ajustada a derecho, dicho sea con los debidos respetos y en términos de defensa, por medio del presente escrito interpongo contra la misma RECURSO DE APELACIÓN impugnando el pronunciamiento desestimatorio de la oposición a la ejecución, así como el correlativo de mandar seguir la ejecución adelante, y la imposición de costas a esta parte.

4) Y que, de conformidad a lo dispuesto en el art. 458 de la LEC, fundo el recurso de apelación en los siguientes

MOTIVOS

Error en la valoración de la prueba e infracción de los artículos 1 del RDLeg. 8/2004 en relación con el artículo 556.3.1º de la LEC al concurrir culpa exclusiva de la víctima.

.El auto desestimando la oposición formulada por esta parte de una errónea aplicación de las reglas de distribución de la carga de la prueba, teniendo en cuenta que se trata de un supuesto de colisión de vehículos, por lo que no son de aplicación las reglas de inversión de la carga de la prueba por la realización de una actividad de riesgo, por cuanto tanto el ejecutante como el asegurado de mi representada conducían su vehículo, produciéndose la colisión.

Partiendo de lo anterior, no puede pretenderse como hace la resolución recurrida que sea esta parte quien acredite que el vehículo contrario saltó el semáforo en fase roja, puesto que ello supone una infracción de las reglas del "onus probandi", según resulta de la interpretación jurisprudencial. Por el contrario, de la prueba practicada en el acto de la vista puede concluirse sin dificultad que fue el vehículo del ejecutante el que no respetó la fase roja del semáforo, puesto que así se afirma por el testigo D [NOMBRE Y APELLIDOS], tanto en el atestado como en la declaración prestada en el acto de la vista, afirmando que "se percató que el vehículo del ejecutante, que circulaba delante del suyo, rebasó el semáforo cuando ya estaba en fase de roja, produciéndose seguidamente la colisión" (minutos [MINUTOS DE LA GRABACIÓN] de la grabación del juicio). Por su parte, no hay ningún elemento que permita afirmar que el asegurado de mi representada no desplegara toda la diligencia necesaria para evitar el accidente, siendo que se vio sorprendido por el vehículo del ejecutante, el cual rebasó el semáforo en fase roja a una velocidad excesiva, según se desprende del informe técnico obrante en folio [FOLIO] del atestado y de la misma declaración del testigo presencial.

Por tanto, la culpa del perjudicado es única y exclusiva, reuniendo los requisitos que determinan la exoneración de responsabilidad en el ámbito del seguro obligatorio, puesto que conducta de la víctima reúne los requisitos de unicidad, totalidad o excluyente y exclusividad, en el origen del daño, al no existir participación negligente de otro o, cuando menos, por cuanto su acción debe anula o impide la apreciación de otras conductas culposas de otros intervinientes, por lo que se interesa, con carácter principal, la revocación del auto impugnado, dejando sin efecto la ejecución despachada.

Subsidiariamente, infracción del artículo 1.1 del RDLeg. 8/2004 en relación con el artículo 556.3.2º de la LEC al no aplicar la moderación por culpa concurrente del perjudicado.

Partiendo de los hechos expuestos en el motivo anterior, y una vez que por la Sala se valore nuevamente la prueba y aun en el improbable caso que no se apreciara culpa exclusiva del perjudicado, es indudable que concurre una culpa de éste en la producción del siniestro que debe determinar la moderación de la indemnización, tal como establece el artículo 1.1 del RDLeg. 8/2004, el cual dispone que si concurrieran la negligencia del conductor y la del perjudicado, se procederá a la equitativa moderación de la responsabilidad y al reparto en la cuantía de la indemnización, atendida la respectiva entidad de las culpas concurrentes.

Como se ha indicado, de no estimarse la anterior alegación de culpa exclusiva, es indudable que la conducta del perjudicado contribuyó de forma principal y decisivamente al resultado lesivo, por lo que se pretende, de forma subsidiaria, que se aprecie la concurrencia de una culpa concurrente del perjudicado que se concreta en un 80%, debiendo indemnizar mi representada en el 20% a ella imputable, debiendo revocarse parcialmente la resolución apelada en este sentido.

Infracción de los criterios de valoración recogidos en el Anexo de la Ley 35/2015, de 22 de septiembre, de reforma del sistema para la valoración de los daños y perjuicios causados a las personas en accidentes de circulación.

Para el caso que se desestime el motivo relativo a la culpa exclusiva del perjudicado, debemos impugnar el importe de la indemnización por incapacidad temporal, fijado en [IMPORTE] euros, puesto que no se ajusta a los criterios vinculantes del Baremo recogido en el Anexo de la Ley 35/2015, de tal manera que deben ajustarse las cuantías tanto en el caso de que la Sala estime el motivo de concurrencia de culpas como en el caso de que se desestimen los motivos anteriores.

Se funda este motivo en el hecho de que, tanto en el auto de cuantía máxima como el auto desestimando la oposición, en la indemnización por incapacidad temporal se incluyo la cantidad de [IMPORTE] euros en concepto de lucro cesante, siendo que en este caso no se cumplen los requisitos establecidos en el art. 143.1 del RDLeg. 8/2004 que establece que la indemnización por pérdida o disminución de dedicación a las tareas del hogar es incompatible con el resarcimiento de los gastos generados por la sustitución de tales tareas.

En este caso, ya se contempla la cantidad de [IMPORTE] euros por sustitución de la perjudicada, de lo que resulta del todo improcedente la fijación de la indemnización por lucro cesante, interesando que se revoque la resolución en este sentido para el caso en que se entienda que la ejecución debe seguir adelante.

En consecuencia, y de forma principal, solicitamos que se revoque la resolución impugnada, estimando la oposición y dejando sin efecto la ejecución despachada, con imposición de las costas de la oposición al ejecutante, todo ello de conformidad a lo prevenido en el art. 561.1 de la LEC. De forma subsidiaria, solicitamos la revocación parcial del auto por apreciar concurrencia de culpas y por improcedencia del concepto de lucro cesante en la indemnización por daños personales, con el pronunciamiento revocatorio inherente respecto a la imposición de costas de la oposición.

Por lo expuesto,

SUPLICO A LA SALA: Que tenga por presentado este escrito, con justificante de traslado, teniendo por interpuesto el recurso de apelación frente al auto dictado el pasado día [FECHA] en las presentes actuaciones de fecha [FECHA] y tras la pertinente tramitación y remisión de las actuaciones a la Ilma. Audiencia Provincial, se dicte por ésta auto en el que, declarando haber lugar al recurso de apelación, estime la oposición formulada por esta parte, y acordando dejar sin efecto la ejecución despachada, con imposición al ejecutante de las costas de la oposición, o, subsidiariamente, estime parcialmente la oposición en el sentido interesado en el escrito, sin imposición de costas.

OTROSÍ DIGO que de conformidad con lo dispuesto en los apartados 3.b) y 6 de la disposición adicional decimoquinta de la LOPJ acompaño a este escrito resguardo de consignación en la cuenta de Depósitos y Consignaciones abierta a nombre del Tribunal del depósito exigido para interponer el recurso por importe de 50 euros.

Por lo que, SUPLICO AL TRIBUNAL que tenga por presentado justificante de liquidación de la tasa y por constituido el depósito, dejando interesada desde este momento su devolución para el caso de estimación total o parcial del recurso.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma Procurador y Abogado

========================================================================
