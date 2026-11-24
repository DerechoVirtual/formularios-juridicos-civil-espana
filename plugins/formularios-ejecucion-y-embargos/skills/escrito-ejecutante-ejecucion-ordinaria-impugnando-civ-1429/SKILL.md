---
name: escrito-ejecutante-ejecucion-ordinaria-impugnando-civ-1429
description: "Escrito del ejecutante en la ejecución ordinaria impugnando la oposición por abusividad. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito del ejecutante en la ejecución ordinaria impugnando la oposición por abusividad

> Formulario **CIV-1429** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito del ejecutante en la ejecución ordinaria impugnando la oposición por abusividad» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito del ejecutante en la ejecución ordinaria impugnando la oposición por abusividad” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:escrito-ejecutante-ejecucion-ordinaria-impugnando-civ-1429`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] EXPONER LOS HECHOS (2 veces)
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] NOMBRE Y APELLIDOS
- [ ] Nº
- [ ] Nº DE PROCEDIMIENTO
- [ ] PORCENTAJE
- [ ] SEDE

## Normas que cita el formulario

- art. 560 LEC
- art. 557.1.7 LEC
- art. 3 RDLeg 1/2007
- art. 82 RDLeg 1/2007

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

- Junto a «…Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº]

Proceso de ejecución [Nº DE PROCEDIMIENTO]

AL TRIBUNAL

D. [NOMBRE Y APELLIDOS] Procurador de los Tribunales y de [NOMBRE DEL REPRESENTADO/A], según tengo acreditado en los autos arriba expresados, ante el Tribunal comparezco y DIGO:

Que, evacuando el traslado conferido, y de conformidad a lo dispuesto en el art. 560 de la LEC, IMPUGNO la oposición a la ejecución deducida de contrario, ello en base a los siguientes

HECHOS

PRIMERO [EXPONER LOS HECHOS] Se niega la procedencia del control de abusividad pretendido de contrario al amparo del artículo 557.1.7ª de la LEC por cuanto que el ejecutado carece de la condición de consumidor, no siéndole de aplicación las normas establecidas en la legislación de consumidores y usuarios.

Como indica la STS de 18 de junio de 2012, la normativa de consumo de transposición de las Directivas europeas, ahora integradas en el citado Real Decreto Legislativo 1/2007, de 16 de noviembre, considera consumidor al "destinatario final", en el sentido de que su intervención en las relaciones de consumo debe responder "a fines privados", ajenos a su actividad empresarial o profesional, y así la jurisprudencia comunitaria hace referencia a dichos fines cuando se refiere que el contrato debe satisfacer "las necesidades familiares o personales", o "a las propias necesidades del consumo privado de un individuo" (SSTJ CE de 17 de marzo 1998, C-45/1996, 11 de julio de 2002 y 20 de enero de 2005, C-464/2001).

En este caso, el contrato se concertó por mi representada con la entidad ejecutada, que carece de la condición de consumidor, puesto que el contrato tenía como objeto el empleo de los bienes para el ejercicio de su actividad empresarial, concretamente para la financiación del equipamiento y maquinaria que se refleja en el citado contrato, de manera que en ningún caso puede aplicarse la normativa de protección de consumidores y usuarios como se pretende de contrario.

SEGUNDO [EXPONER LOS HECHOS] Subsidiariamente, y para el improbable caso que se considerara que la entidad ejecutada ostenta la condición de consumidor, la cláusula impugnada, que establece los intereses remuneratorios al [PORCENTAJE] %, carece del carácter de abusiva, puesto que fue negociada individualmente con la entidad ejecutada y sigue los parámetros usuales en cuanto al precio del dinero en el momento en que se celebró el contrato. En este punto, es reiterada la jurisprudencia que expresa que para apreciar el carácter abusivo de una cláusula contractual se debe atender, además de a la naturaleza de los bienes o servicios objeto de contrato y a las circunstancias que concurren en el momento de su celebración, a las demás cláusulas del contrato y a los parámetros contenidos en las normas de derecho interno en relación con situaciones similares a la que se plantea; asimismo, en cuanto a las cláusulas de intereses remuneratorios, con carácter general se considera que dichos intereses forman parte del precio, de forma que las cláusulas no pueden declararse abusivas, debiendo limitarse el examen judicial al control de transparencia, siendo que en este caso la ejecutada negoció individualmente la cláusula y fue informada detalladamente del contenido del contrato.

Por este motivo, no existe abusividad, no pudiendo decretarse la nulidad pretendida de contrario.

A los anteriores hechos le son de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

Procedimiento

Artículo 560 de la LEC.

Impugnación de la oposición

Falta de la condición de consumidor: el artículo 3 del RDLeg 1/2007 establece que "son consumidores y usuarios las personas físicas o jurídicas que actúan en un ámbito ajeno a su actividad empresarial o profesional".

Impugnación de la oposición

Inexistencia de abusividad. Subsidiariamente, no se dan los requisitos de abusividad establecidos en los artículos 82 y 83 del citado RDLeg 1/2007.

Costas

Artículos 561.1.1º LECiv, imponiéndose al ejecutado al desestimarse la oposición.

Por lo expuesto,

SUPLICO AL TRIBUNAL: Tenga por presentado este escrito, con justificante de traslado a la parte contraria, se sirva admitirlo, teniendo por formulada, en tiempo y forma, impugnación a la oposición formulada de contrario, acordando desestimarla y mandar seguir la ejecución adelante, con imposición de costas al ejecutado.

Lugar y fecha

Firma abogado y procurador

========================================================================
