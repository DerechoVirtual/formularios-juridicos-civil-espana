---
name: incidente-nulidad-actuaciones-proceso-hipotecario-civ-1280
description: "Incidente de nulidad de actuaciones en un proceso hipotecario por falta de citación. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Incidente de nulidad de actuaciones en un proceso hipotecario por falta de citación

> Formulario **CIV-1280** del plugin **Recursos civiles: reposición, apelación, casación y queja** (`formularios-recursos-civiles`) · Civil › Recursos · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Incidente de nulidad de actuaciones en un proceso hipotecario por falta de citación» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Incidente de nulidad de actuaciones en un proceso hipotecario por falta de citación” para mi caso». También puedes invocarla directamente con `/formularios-recursos-civiles:incidente-nulidad-actuaciones-proceso-hipotecario-civ-1280`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-recursos-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Recursos civiles: reposición, apelación, casación y queja) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (3 veces)
- [ ] AÑO (2 veces)
- [ ] FECHA (2 veces)
- [ ] NOMBRE DEL REPRESENTADO/A (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] DÍA
- [ ] LUGAR
- [ ] MES
- [ ] NOMBRE Y APELLIDOS
- [ ] Nº
- [ ] Nº DE DOCUMENTO
- [ ] Nº DE PROCEDIMIENTO
- [ ] ÓRGANO JUDICIAL

## Normas que cita el formulario

- art. 241 LOPJ
- art. 228 LEC
- art. 238.3 LOPJ
- art. 686.3 LEC
- art. 164 LEC
- art. 553 LEC
- art. 241.2 LOPJ
- art. 228.2 LEC

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

- Junto a «…ROCEDIMIENTO] A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA NÚMERO DE [LOCALIDAD]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

Tribunal [ÓRGANO JUDICIAL]

Proceso [Nº DE PROCEDIMIENTO]

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA NÚMERO DE [LOCALIDAD]

D. [NOMBRE Y APELLIDOS] Procurador de los Tribunales y de [NOMBRE DEL REPRESENTADO/A], actuando en nombre y representación de [NOMBRE DEL REPRESENTADO/A], parte ejecutada en el procedimiento de ejecución hipotecaria seguido ante ese Tribunal con el número [NÚMERO], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], ante el Tribunal comparezco y como mejor proceda en derecho DIGO:

Que habiendo tenido conocimiento esta parte de la tramitación del proceso hipotecario número [NÚMERO] contra mi representado, quien en ningún momento ha sido emplazado en los autos, por medio del presente escrito me persono en estos autos y, al amparo de lo dispuesto en el art. 241 de la LOPJ y art. 228 de la LEC, promuevo la NULIDAD DE ACTUACIONES en el mencionado proceso en base a los siguientes:

HECHOS Y FUNDAMENTOS

Alegamos la vulneración del derecho fundamental a la tutela judicial efectiva sin indefensión del artículo 24.1 de la CE, según resulta de los hechos que exponemos a continuación y que han motivado que el proceso hipotecario se haya seguido a espaldas de mi representado:

a) El presente procedimiento hipotecario se inició en fecha [FECHA], contra mi representado y en relación con la finca registral hipotecada núm. [Nº], inscrita en el Registro la Propiedad de [LOCALIDAD] En la demanda, la entidad demandante señaló como domicilio para la práctica del requerimiento de pago en el domicilio que constaba en la escritura de hipoteca y en el Registro de la Propiedad, que fue negativa, al tratarse de unas naves abandonadas. No obstante, constaba en el contrato de préstamo hipotecario otro domicilio de mi representado- el particular- donde se remitió por el Tribunal la convocatoria de subasta como se expresará posteriormente.

b) Ante esta diligencia negativa, por la entidad ejecutante, y pese a conocer que el domicilio particular de mi demandante era otro distinto, se interesó que las sucesivas notificaciones se practicaran por edictos, lo cual se acordó por el Tribunal, practicándose el requerimiento de pago y citación mediante edictos en la forma prevista en el art. 164 de la Ley de Enjuiciamiento Civil.

c) Mi representado tuvo conocimiento de la existencia de este procedimiento en fecha [FECHA], al serle remitida la convocatoria de subasta a su domicilio particular sito en [LOCALIDAD].

Por tanto, se cumplen los requisitos del art. 241 de la LOPJ al deducirse la petición dentro del plazo de veinte días desde que se conoció la existencia del procedimiento y al estar legitimado mi representado al ser parte ejecutado en el proceso, no siendo susceptible de repararse el defecto por otro recurso o remedio procesal.

La nulidad que se solicita lo es al amparo del art. 24.1 de la CE (vulneración del derecho a la tutela judicial efectiva sin indefensión) y arts. 238.3 de la LOPJ y 225.3º de la LEC, así como de la reiterada jurisprudencia que interpreta el remedio de la comunicación edictal como último instrumento, lo que determina que el proceso se siguiera con infracción del principio de contradicción, con evidente indefensión para esta parte.

La infracción resulta del "iter" procedimental seguido y que en síntesis es el siguiente:

a) Mi representado no fue emplazado ni requerido de pago en su domicilio real, pese a que en el contrato de préstamo hipotecario constaba otro domicilio, sin que se haya realizado ninguna diligencia previa a la comunicación edictal para emplazar a mi representado en su verdadero domicilio que constaba en autos.

b) La entidad ejecutante era conocedora de que mi representado tenía otro domicilio distinto, no actuando de buena fe cuando interesó la publicación de edictos al amparo de lo dispuesto en el art. 686.3 LEC.

c) La existencia de otro domicilio donde podía ser requerido mi representado queda constatada por el hecho que el órgano judicial remite la notificación de la fecha de la subasta al domicilio real de mi representado, momento en que éste conoce la existencia del proceso como se ha indicado, pero ya no puede formular oposición, quedando en una situación de indefensión.

La nulidad de actuaciones que se postula resulta palmaria del relato del curso de proceso, por cuanto se acudió al postrer remedio de la citación y notificación edictal, sin haber desplegado una actividad razonable para venir en conocimiento del domicilio del demandado, tal como se exige en el art. 164 de la LEC y en la interpretación que realiza la jurisprudencia del T.C. y del Tribunal Supremo, de forma reiterada.

Más concretamente, para el procedimiento hipotecario, el Tribunal Constitucional ha expresado repetidamente que es necesario que el órgano judicial agote los medios que tenga a su alcance para notificar al ejecutado la existencia del proceso en su domicilio real, de modo que, una vez que surjan dudas razonables de que el domicilio señalado en la escritura del préstamo hipotecario y que figura en el Registro sea el domicilio real del ejecutado, le es exigible que intente, en cumplimiento del deber de diligencia que en orden a la realización de los actos de comunicación procesal le impone el art. 24.1 CE, el emplazamiento personal del ejecutado en el domicilio que figure en las actuaciones, distinto del que consta en la escritura de préstamo hipotecario y en el Registro (SSTC 245/2006, de 24 de julio; 104/2008, de 15 de septiembre; y 28/2010, de 27 de abril).

Esta misma doctrina se ha aplicado tras la reforma operada por Ley 13/2009, expresando la STC 122/2013, de 20 de mayo, que debe realizarse una interpretación secundum constitutionem del art. 686.3 LEC, integrando su contenido, de forma sistemática, con el art. 553 LEC, precepto rector de la llamada al proceso de ejecución hipotecaria, y con la doctrina de este Tribunal en cuanto a la subsidiariedad de la comunicación edictal, la cual tiene su fuente directa en el derecho de acceso al proceso del art. 24.1 CE, de manera que la comunicación edictal en el procedimiento de ejecución hipotecaria sólo puede utilizarse cuando se hayan agotado los medios de averiguación del domicilio del deudor o ejecutado.

Por tanto, existe un defecto en la comunicación que impidió a mi representada el ejercicio de su derecho de defensa, al acudirse a la citación edictal, lo que originó que el proceso hipotecario se desarrollara a espaldas del demandado, ocasionando una evidente indefensión, y debe dar lugar a la nulidad de las actuaciones desde el momento anterior al requerimiento de pago, conforme a los arts. 225 y ss. de la LEC, para que mi representado pueda defenderse en el mismo.

Por lo expuesto es de justicia y,

SUPLICO AL TRIBUNAL que tenga por presentado este escrito y documento que se acompaña, por promovido incidente de nulidad de actuaciones practicadas en este proceso, y, previos los trámites legales, dicte resolución por la que declare la nulidad de lo actuado reponiendo las actuaciones al momento inmediatamente anterior al requerimiento de pago.

OTROSÍ DIGO que al amparo de lo dispuesto en el art. 241.2 de la LOPJ y art. 228.2 de la LEC solicito que se acuerde la suspensión del procedimiento de apremio iniciado contra mi representada, dejando sin efecto la subasta señalada, puesto que existe una sólida apariencia de buen derecho y se originaría un perjuicio irreparable de seguir adelante con la subasta que ya se ha señalado, y estando asegurado el crédito hipotecario mediante la anotación registral del mismo.

SUPLICO AL TRIBUNAL que acuerde de conformidad.

En [LUGAR], a [DÍA] de [MES] de [AÑO].l año [AÑO]

Firma de Abogado Firma de Procurador

========================================================================
