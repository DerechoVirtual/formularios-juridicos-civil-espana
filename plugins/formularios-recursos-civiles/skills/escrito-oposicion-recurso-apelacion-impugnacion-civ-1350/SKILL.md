---
name: escrito-oposicion-recurso-apelacion-impugnacion-civ-1350
description: "Escrito de oposición al recurso de apelación con impugnación de la sentencia. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito de oposición al recurso de apelación con impugnación de la sentencia

> Formulario **CIV-1350** del plugin **Recursos civiles: reposición, apelación, casación y queja** (`formularios-recursos-civiles`) · Civil › Recursos · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito de oposición al recurso de apelación con impugnación de la sentencia» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito de oposición al recurso de apelación con impugnación de la sentencia” para mi caso». También puedes invocarla directamente con `/formularios-recursos-civiles:escrito-oposicion-recurso-apelacion-impugnacion-civ-1350`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-recursos-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Recursos civiles: reposición, apelación, casación y queja) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (5 veces)
- [ ] FOLIO (3 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] ASEGURADORA
- [ ] DENOMINACIÓN SOCIAL
- [ ] SEDE
- [ ] TÍTULO DEL MOTIVO

## Normas que cita el formulario

- art. 461 LEC
- art. 459 LEC
- art. 9 LOPJ
- art. 66.2 LEC
- art. 9.4 LOPJ
- art. 394 LEC
- art. 394.2 LEC

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

Proceso número [NÚMERO]

A LA AUDIENCIA PROVINCIAL DE [LOCALIDAD]

D. [NOMBRE Y APELLIDOS], Procurador de los Tribunales, en nombre y representación de D. [NOMBRE Y APELLIDOS], parte demandada en este proceso seguido con el número [NÚMERO], según tengo acreditado en autos, ante la Sala comparezco y como mejor proceda en derecho DIGO:

1) Que esta representación ha sido emplazada en fecha [FECHA] para oposición e impugnación del recurso de apelación interpuesto de contrario, por lo que, de conformidad a lo dispuesto en el art. 461 de la LEC, mediante el presente escrito ME OPONGO AL RECURSO E IMPUGNO LA SENTENCIA dictada en este proceso.

2) [TÍTULO DEL MOTIVO] Que la oposición la fundamos en la improcedencia de los motivos de apelación sostenidos de contrario, en tanto que la impugnación de la sentencia se centra en dos extremos: 1) la impugnación de la desestimación de la declinatoria de jurisdicción que fue planteada oportunamente por esta parte; y 2) de forma subsidiaria, en relación al pronunciamiento sobre costas de la sentencia, al entender que no procede la imposición de las costas a esta parte.

Lógicamente, de estimarse la impugnación relativa a la declinatoria, no procedería entrar en el fondo del asunto; no obstante, y por razones de claridad expositiva, estructuramos de forma separada los motivos de oposición a los de impugnación, sin perjuicio de que la Sala los examine en el orden correspondiente.

De acuerdo a lo anterior, fundamos la oposición e impugnación en los siguientes MOTIVOS:

I. MOTIVOS DE OPOSICIÓN AL RECURSO

PRIMERO.- Nos oponemos al correlativo alegado por la parte apelante, que pretende una indemnización superior a la que fue fijada en la sentencia apelada.

En efecto, la indemnización fue fijada correctamente con arreglo al baremo aplicable para los accidentes derivados del uso y circulación de vehículos de motor, haciendo el Juez de instancia un recto ejercicio de los márgenes de discrecionalidad que le atribuye dicha norma, los cuales argumenta extensamente en la sentencia de instancia.

En el concreto punto impugnado, es decir, el incremento de la indemnización por la situación invalidez absoluta, la pretensión indemnizatoria se basa sobre un hecho que no resulta acreditado en la prueba practicada, y así se ha apreciado lógicamente por el Juez, porque las dos periciales practicadas concluyen que las lesiones y secuelas no le incapacitan de forma permanente, sino que únicamente originan una incapacidad parcial del 33%, acreditándose asimismo tal extremo por el hecho no controvertido que el demandante sigue desarrollando su trabajo habitual como administrativo de la empresa [DENOMINACIÓN SOCIAL] a tiempo parcial, lo que evidencia que no hay situación de invalidez absoluta.

II. MOTIVOS DE IMPUGNACIÓN DE LA SENTENCIA

PRIMERO.- Al amparo del art. 459 de la LEC, por infracción de lo dispuesto en el art. 9 de la LOPJ y 36 de la LEC, al carecer de jurisdicción los órganos del orden civil para el conocimiento de este asunto.

Este proceso se siguió en demanda de responsabilidad patrimonial contra el Ayuntamiento de [LOCALIDAD] y contra mi representada, la aseguradora [ASEGURADORA], en razón al funcionamiento de los servicios públicos, al haber colisionado el vehículo del demandante contra una valla que señalizaba unas obras efectuadas por cuenta del Ayuntamiento codemandado.

Esta parte, al entender competentes a los órganos del orden contencioso-administrativo, planteó en tiempo y forma la declinatoria de jurisdicción que fue desestimada por auto de fecha [FECHA] (folio [FOLIO]), deduciéndose contra el mismo recurso de reposición en fecha [FECHA] por esta representación (folio [FOLIO]), que fue desestimado por auto de fecha [FECHA] (folio [FOLIO]), por lo que nos vemos en la necesidad de razonar sobre la falta de estos presupuestos procesales en sede de impugnación de sentencia, tal como prescribe el art. 66.2 de la LEC.

La resolución judicial se dicta faltando el esencial presupuesto de la jurisdicción para el conocimiento del asunto, con infracción de lo dispuesto en el art. 9.4 de la LOPJ, en su redacción dada por Ley Orgánica 19/2003, de 23 de diciembre, que expresamente atribuye al orden contencioso-administrativo el conocimiento de las pretensiones que se deduzcan en relación con la responsabilidad patrimonial de las Administraciones Públicas, incluso cuando, como en este caso, el interesado haya accionado directamente contra la aseguradora de la Administración, junto a la Administración respectiva.

En las resoluciones de instancia no se tuvieron en cuenta estos argumentos, oportunamente alegados, aplicándose el criterio de la vis attractiva, improcedente ante la existencia de norma orgánica de atribución expresa al orden jurisdiccional contencioso-administrativo.

De acuerdo con lo anterior, debe estimarse la impugnación de la sentencia y declararse la falta de jurisdicción, revocando la de instancia remitiendo al demandante al orden competente, y con imposición de costas de primera instancia al actor.

SEGUNDO.- De forma subsidiaria, para el caso de no estimarse la falta de jurisdicción, impugnamos el pronunciamiento de costas de la primera instancia, por infracción del art. 394 de la LEC.

En relación a las costas procesales de la primera instancia, la sentencia apelada, en su Fundamento de Derecho Sexto, aun considerando que se da una estimación parcial de la demanda, impone las costas a esta parte y al codemandado de acuerdo con lo dispuesto en el artículo 394.2 de la Ley de Enjuiciamiento Civil, con base a «la actitud de la demanda de incumplir absolutamente su obligación de satisfacer la prestación indemnizatoria de la demandante, primero negando la realidad del accidente y subsidiariamente solicitando una rebaja en la cuantía por daños personales», que llevan a la Juzgadora a quo a estimar la existencia de méritos suficientes para apreciar temeridad en aquéllos.

Pues bien, la aseguradora que represento, apoyada en informes médicos aportados con el escrito de contestación, se opuso razonablemente a la petición indemnizatorio por la falta de relación de las lesiones y secuelas por las que el demandante solicitaba la indemnización con el accidente o el menor alcance de las mismas que se vio finalmente refrendada en la sentencia apelada, al menos en gran medida, resultando contradictorio el expresado razonamiento de la sentencia apelada con la afirmación, sin duda fundada, que hace en el Fundamento de Derecho Cuarto de que «las pretensiones indemnizatorias de la actora, son desorbitadas y no ajustadas a la realidad».

En esta tesitura entendemos que se ha infringido el art. 394.2 de la LEC, pues no hay temeridad en la conducta de esta parte, y que la solución adecuada es la de no hacer expresa imposición de las controvertidas costas procesales, abonando cada una de las partes las causadas a su instancia y las comunes por mitad.

Por tanto, interesamos la estimación del motivo de impugnación alegado con carácter subsidiario.

Por lo expuesto, solicitamos la revocación de la sentencia, con desestimación del recurso de apelación, declarándose la falta de jurisdicción con costas al actor o, en otro caso, que se revoque la sentencia únicamente en el pronunciamiento relativo a las costas de primera instancia, manteniendo el resto de sus pronunciamientos, todo ello con imposición de las costas de la apelación principal a la parte apelante.

En base a lo anterior,

SUPLICO A LA SALA: que tenga por presentado este escrito con justificante de traslado a las demás partes, teniéndome por opuesto al recurso de apelación frente a la sentencia dictada por la Sección Civil del Tribunal de Instancia de [SEDE] en las presentes actuaciones de fecha [FECHA] y por impugnada la sentencia, y tras la pertinente tramitación, se revoque la misma, declarando la falta de jurisdicción con imposición de costas al actor; o, en otro caso, se desestime el recurso de apelación interpuesto de contrario y se revoque la condena en costas, todo ello con imposición a la parte apelante de las costas ocasionadas en esta alzada.

En L. y F.

(Firma Procurador y Abogado)

========================================================================
