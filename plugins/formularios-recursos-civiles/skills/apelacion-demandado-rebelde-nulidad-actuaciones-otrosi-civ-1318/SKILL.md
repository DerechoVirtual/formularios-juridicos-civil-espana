---
name: apelacion-demandado-rebelde-nulidad-actuaciones-otrosi-civ-1318
description: "Apelación del demandado rebelde por nulidad de actuaciones, con otrosí subsidiario de prueba. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Apelación del demandado rebelde por nulidad de actuaciones, con otrosí subsidiario de prueba

> Formulario **CIV-1318** del plugin **Recursos civiles: reposición, apelación, casación y queja** (`formularios-recursos-civiles`) · Civil › Recursos · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **recursos**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Apelación del demandado rebelde por nulidad de actuaciones, con otrosí subsidiario de prueba» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Apelación del demandado rebelde por nulidad de actuaciones, con otrosí subsidiario de prueba” para mi caso». También puedes invocarla directamente con `/formularios-recursos-civiles:apelacion-demandado-rebelde-nulidad-actuaciones-otrosi-civ-1318`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-recursos-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Recursos civiles: reposición, apelación, casación y queja) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] DOMICILIO
- [ ] IMPORTE

## Normas que cita el formulario

- art. 459 LEC
- art. 155 LEC
- art. 247.3 LEC
- art. 460.3 LEC

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

(Tras el encabezamiento, se desarrollaría como primer motivo la infracción procesal que determina la nulidad de actuaciones)

PRIMERO.-Al amparo del art. 459 de la LEC, por infracción de las garantías procesales del proceso civil con vulneración de lo dispuesto en el art. 24 de la CE en cuanto al derecho fundamental a un proceso con todas las garantías, incurriéndose en los motivos de nulidad de pleno derecho del art. 166.1 y 225.5 de la LEC.

En esta apelación se insta la declaración de nulidad de los trámites posteriores al emplazamiento de esta parte para contestar a la demanda, por no haber tenido oportunidad procesal de denunciar dicha vulneración en la instancia que se siguió en rebeldía de esta parte, al haberse infringido el art. 155, 156 y 164 de la LEC y la jurisprudencia que los interpreta en orden a la comunicación edictal, pues se acudió a este medio subsidiario sin realizar averiguación alguna del domicilio de mi representado, cuando consta tanto en el padrón de habitantes del Ayuntamiento de esta localidad como en el Colegio profesional de Arquitectos al que mi representado pertenece que su domicilio se halla en [DOMICILIO] (acompaño como documentos números 1 y 2 certificado del Ayuntamiento y del Colegio de Arquitectos acreditativo de estos extremos).

En lugar de realizar las averiguaciones oportunas, el Tribunal, ante la diligencia negativa de emplazamiento en el domicilio facilitado por el demandante, acordó el emplazamiento edictal, lo que infringe los preceptos antes mencionados. Pero es que, además, existen razones para pensar que el demandante ha actuado de forma contraria a la buena fe procesal, pues facilitó un domicilio anterior de mi representado, existiendo motivos para deducir que conocía el actual domicilio, pues lo facilitó de forma novedosa y sin que se haya realizado ningún trámite de averiguación, al solicitar la notificación personal de la sentencia estimatoria dictada en la instancia, por lo cual desde este momento solicitamos para la contraparte la sanción prevenida en el art. 247.3 de la LEC.

(se razonará sobre el efecto indefensión y la imposibilidad de subsanación) La actuación judicial ha supuesto una vulneración del derecho de defensa de esta parte, pues mi representado se ha visto indefenso al no poder intervenir en la instancia, no siendo reparable tal infracción en esta alzada, puesto que se impide formular reconvención a esta parte, pues el actor le adeuda la cantidad de [IMPORTE] euros por los servicios profesionales que le prestó mi representado como consecuencia de la actuación que precisamente motiva su reclamación.

(se razona sobre los efectos pretendidos) De acuerdo a la grave infracción denunciada, entendemos que procede decretar la nulidad de todo lo actuado a partir del momento del emplazamiento en la instancia, debiendo retrotraerse las actuaciones a dicho momento procesal.

(Seguiría con la exposición de los motivos de fondo y suplico y en el otrosí)

OTROSÍ DIGO que, de forma subsidiaria a la petición de nulidad de actuaciones y para el caso de no acordarse la nulidad, al amparo de lo dispuesto en el art. 460.3 de la LEC, solicito el recibimiento a prueba en esta segunda instancia en base a haberse seguido el proceso en rebeldía no imputable a esta parte, con grave indefensión, tal como hemos expuesto ampliamente en el motivo primero del escrito de interposición, proponiendo la que se relaciona en el suplico por ser pertinente y útil al esclarecimiento de los hechos alegados.

Por lo expuesto, SUPLICO A LA SALA que se reciba el proceso a prueba en la segunda instancia, señalándose vista para su práctica y proponiendo los siguientes medios de prueba:

- INTERROGATORIO del demandante.

(Se relacionarían el resto de medios de prueba)

========================================================================
