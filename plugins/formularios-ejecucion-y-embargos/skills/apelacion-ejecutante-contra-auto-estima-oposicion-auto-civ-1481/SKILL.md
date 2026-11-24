---
name: apelacion-ejecutante-contra-auto-estima-oposicion-auto-civ-1481
description: "Apelación del ejecutante contra el auto que estima la oposición (auto de cuantía máxima). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Apelación del ejecutante contra el auto que estima la oposición (auto de cuantía máxima)

> Formulario **CIV-1481** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Recurso de apelación del ejecutante contra el auto que estima la oposición a la ejecución de un auto de cuantía máxima (accidente de circulación, seguro obligatorio). El auto es apelable directamente (art. 561.3 LEC). El modelo alega error en la valoración de la prueba e infracción del art. 1 del texto refundido de la Ley sobre responsabilidad civil y seguro en la circulación de vehículos a motor; adáptense los hechos al caso.

Es un modelo de tipo **recursos**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Apelación del ejecutante contra el auto que estima la oposición (auto de cuantía máxima)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Apelación del ejecutante contra el auto que estima la oposición (auto de cuantía máxima)” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:apelacion-ejecutante-contra-auto-estima-oposicion-auto-civ-1481`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (4 veces)
- [ ] AÑO (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] Nº DE PROCEDIMIENTO (2 veces)
- [ ] VEHÍCULO (2 veces)
- [ ] DESCRIBIR LA INFRACCIÓN O CIRCUNSTANCIA ATRIBUIDA A LA VÍCTIMA
- [ ] DÍA
- [ ] IMPORTE
- [ ] MES
- [ ] NOMBRE Y APELLIDOS DEL EJECUTANTE
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] Nº
- [ ] SEDE

## Normas que cita el formulario

- art. 561.3 LEC
- art. 458 LEC
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

### Avisos de actualización (2) — se aplican en el texto, nunca se copian en el documento

- Junto a «…DIMIENTO] A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: el original se encabezaba «A la Audiencia Provincial»; el escrito de interposición de la apelación se presenta ante el órgano que dictó la resolución recurrida (art. 458 LEC), que remitirá los autos a la Audiencia Provincial.

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

Proceso de ejecución n.º [Nº DE PROCEDIMIENTO]

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS DEL EJECUTANTE], parte ejecutante en este proceso seguido con el número [Nº DE PROCEDIMIENTO], según tengo acreditado en autos, ante el Tribunal comparezco y, como mejor proceda en derecho, DIGO:

1) Que en fecha [FECHA] se ha dictado auto estimando la oposición a la ejecución despachada por auto de fecha [FECHA], el cual ha sido notificado a esta parte en fecha [FECHA].

2) El auto que se impugna es apelable directamente al amparo del art. 561.3 de la LEC.

3) Al amparo del citado precepto, entendiendo que dicha resolución no es ajustada a derecho, dicho sea con los debidos respetos y en términos de defensa, por medio del presente escrito interpongo contra la misma RECURSO DE APELACIÓN, impugnando el pronunciamiento estimatorio de la oposición a la ejecución y la imposición de costas a esta parte.

4) Y que, de conformidad con lo dispuesto en el art. 458 de la LEC, fundo el recurso de apelación en los siguientes

MOTIVOS

PRIMERO.– Error en la valoración de la prueba.

El auto estimando la oposición formulada por la parte ejecutada parte de una errónea valoración de la prueba practicada, al no tener en cuenta que las reglas de distribución de la carga probatoria están informadas por el principio de responsabilidad por riesgo o de inversión de la carga de la prueba en los supuestos en que, como el presente, el resultado lesivo viene producido por una actividad susceptible de generar un riesgo para las personas, como lo es la conducción de un vehículo de motor.

Como se ha venido reiterando en la doctrina jurisprudencial, quien crea un riesgo con su actividad u obtiene beneficio de la existencia del riesgo mismo, sea o no lucrativo, debe extremar todas las precauciones y agotar los medios para evitar la concurrencia de aquellas circunstancias que cabe controlar y pueden generar daños efectivos. Por ello, en estos casos ha de tener lugar la inversión de la carga de la prueba, que obliga a quien produce el riesgo o se beneficia del mismo a demostrar que en la producción del resultado dañoso, derivado causalmente de ese riesgo, no ha tenido ninguna actuación negligente, al haber obrado con la mayor y más atenta diligencia y prudencia, o bien que el suceso se debió a caso fortuito, fuerza mayor o lo produjo el exclusivo actuar imprudente de la víctima (SSTS de 11 de febrero de 1992; de 10 de marzo de 1994, rec. 1391/1991; de 22 de enero de [AÑO], rec. 1950/1992; y de 8 de octubre de 1996, rec. 2656/1992, entre otras muchas).

Pues bien, en este caso, en la valoración que se realiza en la resolución de instancia no se toma en cuenta el criterio rector de valoración probatoria antes expresado. De las declaraciones prestadas en la vista por los agentes de la Policía Local de [LOCALIDAD] no cabe concluir que la causa directa e inmediata del accidente haya sido la negligente conducción de mi representado al circular con su [VEHÍCULO] en el carril reservado al sentido contrario, por cuanto el conductor del automóvil manifestó a los agentes que se percató de que el [VEHÍCULO] circulaba invadiendo su carril, si bien perdió el control del vehículo al realizar una maniobra evasiva incorrecta, debido al exceso de velocidad con que circulaba, según se desprende del mismo atestado y de la declaración de los agentes en el acto de la vista.

Por lo tanto, y si bien es cierto que [DESCRIBIR LA INFRACCIÓN O CIRCUNSTANCIA ATRIBUIDA A LA VÍCTIMA], en ningún momento consta de forma fehaciente que lo hiciera invadiendo el carril contrario, puesto que en todo momento ha indicado que lo hacía por el arcén, por lo que no se ha probado la culpa exclusiva de la víctima, ni tan siquiera concurrencia de culpas, ya que, aun cuando no circulase en el sentido de la marcha, lo cierto es que ese hecho no ha sido el causante del accidente, puesto que en ningún momento llegó a ocupar el carril reservado a los vehículos que transitaban en dirección contraria; y la prueba de dicha invasión correspondía acreditarla a la parte ejecutada, que es la que la alegó.

[ADAPTAR ESTE APARTADO A LOS HECHOS Y A LA PRUEBA PRACTICADA EN EL CASO CONCRETO.]

SEGUNDO.– Infracción del artículo 1 del texto refundido de la Ley sobre responsabilidad civil y seguro en la circulación de vehículos a motor.

En conclusión, y atendidos los hechos que resultan de la prueba practicada, cabe concluir que existe una errónea valoración de la prueba practicada en la resolución de instancia, con infracción de lo dispuesto en el párrafo segundo del art. 1 del texto refundido de la Ley sobre responsabilidad civil y seguro en la circulación de vehículos a motor (Real Decreto Legislativo 8/2004, de 29 de octubre), que dispone que, en el caso de daños a las personas, de la responsabilidad sólo quedará exonerado el conductor cuando pruebe que los daños fueron debidos únicamente a la conducta o la negligencia del perjudicado o a fuerza mayor extraña a la conducción o al funcionamiento del vehículo, elementos éstos que no han resultado en modo alguno acreditados, ni tan siquiera en relación con una presunta culpa concurrente de la víctima.

En consecuencia, solicitamos que se revoque la resolución impugnada, desestimando la oposición y mandando seguir adelante la ejecución, con imposición de las costas de la oposición al ejecutado, todo ello de conformidad con lo prevenido en el art. 561.1 de la LEC.

Por lo expuesto,

SUPLICO AL TRIBUNAL: Que tenga por presentado este escrito, con justificante de traslado, teniendo por interpuesto el recurso de apelación frente al auto dictado por el Tribunal en las presentes actuaciones de fecha [FECHA] y, tras la pertinente tramitación y remisión de las actuaciones a la Audiencia Provincial, se dicte por ésta auto en el que, declarando haber lugar al recurso de apelación, desestimando la oposición deducida de contrario y acordando mandar seguir adelante la ejecución despachada, con imposición al ejecutado de las costas de la oposición.

OTROSÍ PRIMERO DIGO: Que, al amparo de lo dispuesto en el art. 561.3 de la LEC, esta parte solicita que se mantengan los embargos y medidas de garantía en tanto se sustancia la apelación, comprometiéndose a prestar la caución que el tribunal estime suficiente para asegurar la indemnización que pueda corresponder al ejecutado, considerando que, en las circunstancias que se dan en este proceso, podría ascender a [IMPORTE] euros, sin perjuicio de que el tribunal fije otra diferente, la cual será prestada en todo caso por esta parte.

Por lo que SUPLICO AL TRIBUNAL: Acuerde de conformidad.

OTROSÍ SEGUNDO DIGO: Que, de conformidad con lo dispuesto en los apartados 3.b) y 6 de la disposición adicional decimoquinta de la LOPJ, acompaño a este escrito resguardo de consignación en la cuenta de Depósitos y Consignaciones abierta a nombre del Tribunal del depósito exigido para interponer el recurso, por importe de 50 euros.

Por lo que SUPLICO AL TRIBUNAL que tenga por constituido el depósito, dejando interesada desde este momento su devolución para el caso de estimación total o parcial del recurso.

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Abogado/a Firma del Procurador/a
