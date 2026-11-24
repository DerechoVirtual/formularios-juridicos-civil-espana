---
name: escrito-ejecutado-pidiendo-declarar-abusiva-nula-civ-1436
description: "Escrito del ejecutado pidiendo declarar abusiva y nula una cláusula en la ejecución hipotecaria. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito del ejecutado pidiendo declarar abusiva y nula una cláusula en la ejecución hipotecaria

> Formulario **CIV-1436** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Escrito de oposición del ejecutado (consumidor) a una ejecución hipotecaria ya despachada, dentro del plazo de diez días del art. 556.1 LEC, fundada en el carácter abusivo de determinadas cláusulas del préstamo (en el modelo, intereses moratorios), con petición de suspensión, inaplicación de las cláusulas, reducción de la cantidad reclamada y condena en costas al ejecutante (art. 695.1.4.ª LEC).

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito del ejecutado pidiendo declarar abusiva y nula una cláusula en la ejecución hipotecaria» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito del ejecutado pidiendo declarar abusiva y nula una cláusula en la ejecución hipotecaria” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:escrito-ejecutado-pidiendo-declarar-abusiva-nula-civ-1436`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº DE CLÁUSULA (9 veces)
- [ ] IMPORTE (3 veces)
- [ ] NOMBRE Y APELLIDOS DEL EJECUTADO (3 veces)
- [ ] FIRMA (2 veces)
- [ ] Nº DE PLAZA (2 veces)
- [ ] Nº DE PROCEDIMIENTO (2 veces)
- [ ] SEDE (2 veces)
- [ ] AÑO
- [ ] DENOMINACIÓN SOCIAL O NOMBRE DEL EJECUTANTE
- [ ] DÍA
- [ ] LOCALIDAD
- [ ] MES
- [ ] NOMBRE Y APELLIDOS DEL ABOGADO/A
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] PORCENTAJE
- [ ] TRANSCRIBIR LITERALMENTE LAS CLÁUSULAS IMPUGNADAS

## Normas que cita el formulario

- art. 695.1.4.ª LEC
- art. 556.1 LEC
- art. 83 Real Decreto Legislativo 1/2007
- art. 1258 Código Civil
- art. 695.2 LEC
- art. 83.1 Real Decreto Legislativo 1/2007
- art. 539.2 LEC

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

SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº DE PLAZA]

Proceso de ejecución hipotecaria número [Nº DE PROCEDIMIENTO]

AL TRIBUNAL

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, actuando en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS DEL EJECUTADO], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño a este escrito, en procedimiento de ejecución hipotecaria [Nº DE PROCEDIMIENTO], y bajo la dirección letrada de D./Dña. [NOMBRE Y APELLIDOS DEL ABOGADO/A], seguido contra mi mandante y a instancia de [DENOMINACIÓN SOCIAL O NOMBRE DEL EJECUTANTE], comparezco ante la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº DE PLAZA], y, como mejor proceda en derecho, DIGO:

Que habiendo sido notificado a mi principal auto despachando ejecución en el procedimiento arriba expresado, mediante el presente escrito, y al amparo de lo previsto en el artículo 695.1.4.ª de la LEC, en la representación que ostento de D./Dña. [NOMBRE Y APELLIDOS DEL EJECUTADO], en tiempo y forma, dentro del plazo de diez días previsto en el artículo 556.1 de la LEC, paso a formular OPOSICIÓN A LA EJECUCIÓN HIPOTECARIA despachada sobre el bien hipotecado POR EL CARÁCTER ABUSIVO DE LAS CLÁUSULAS [Nº DE CLÁUSULA] Y [Nº DE CLÁUSULA] DEL CONTRATO DE PRÉSTAMO HIPOTECARIO, la cual baso en los siguientes

HECHOS

PRIMERO.- Las cláusulas número [Nº DE CLÁUSULA] y [Nº DE CLÁUSULA] del contrato de préstamo hipotecario por el que se ha despachado ejecución son del siguiente tenor literal: [TRANSCRIBIR LITERALMENTE LAS CLÁUSULAS IMPUGNADAS].

SEGUNDO.- Las referidas cláusulas contractuales están incluidas en el ámbito de aplicación de la Directiva 93/13/CEE y producen un grave desequilibrio entre el consumidor y la entidad acreedora, incurriendo en un supuesto de nulidad por abusividad, puesto que la cláusula número [Nº DE CLÁUSULA], que fija los intereses moratorios en un [PORCENTAJE] %, [ADAPTAR AL CASO: el quíntuplo del interés legal actual], supone un grave desequilibrio para el consumidor a la vez que supone un ilícito enriquecimiento para la entidad bancaria, que aplica unos intereses desproporcionados, y en este sentido se han pronunciado sobre cláusulas similares la SAP Zaragoza (Sección 5.ª) de 8 de mayo de 2012, rec. 68/2012; la SAP Burgos (Sección 2.ª) de 30 de marzo de 2010, rec. 307/2010; y la SAP Vizcaya (Sección 4.ª) de 26 de octubre de 2010, rec. 307/2010, entre otras muchas.

TERCERO.- Los efectos de la declaración de nulidad de las cláusulas deben ser los de dejarlas sin aplicación, lo cual implica la improcedencia de seguir con la ejecución derivada de su vigencia por importe de [IMPORTE] euros.

El artículo 83.1 del texto refundido de la Ley General para la Defensa de los Consumidores y Usuarios, redactado por la Ley 3/2014, de 27 de marzo, establece que «las cláusulas abusivas serán nulas de pleno derecho y se tendrán por no puestas. A estos efectos, el Juez, previa audiencia de las partes, declarará la nulidad de las cláusulas abusivas incluidas en el contrato, el cual, no obstante, seguirá siendo obligatorio para las partes en los mismos términos, siempre que pueda subsistir sin dichas cláusulas». Además, en su redacción dada por la Ley 5/2019, de 15 de marzo, reguladora de los contratos de crédito inmobiliario, se indica que «Las condiciones incorporadas de modo no transparente en los contratos en perjuicio de los consumidores serán nulas de pleno derecho». Habiendo interpretado el TJUE que las cláusulas abusivas deben ser inaplicadas, sin que pueda modificarse o integrarse el contenido de las mismas, ha declarado en la STJUE de 14 de junio de 2012, C-618/10, que el artículo 83 del Real Decreto Legislativo 1/2007 se opone al derecho comunitario en tanto que atribuye al juez nacional, cuando éste declara la nulidad de una cláusula abusiva contenida en un contrato celebrado entre un profesional y un consumidor, la facultad de integrar dicho contrato modificando el contenido de la cláusula abusiva. En el mismo sentido, la STS de 22 de abril de 2015, rec. 2351/2012, indica que la consecuencia de la apreciación de la abusividad de una cláusula es la supresión de tal cláusula, sin que el juez pueda aplicar la norma supletoria que el Derecho nacional prevea a falta de estipulación contractual, y sin que pueda integrarse el contrato mediante los criterios establecidos, en el Derecho español, en el art. 1258 del Código Civil, salvo que se trate de una cláusula necesaria para la subsistencia del contrato en beneficio del consumidor, lo que no es el caso de las cláusulas que establecen el interés de demora, cuya supresión solo conlleva la minoración de la cantidad a pagar por el consumidor al profesional o empresario.

A los anteriores hechos son de aplicación los siguientes,

FUNDAMENTOS DE DERECHO

Competencia

De acuerdo con lo referido de contrario en cuanto a la competencia de este Tribunal para conocer de la presente ejecución y, en consecuencia, de su oposición.

Procedimiento

El artículo 695.1.4.ª de la LEC regula la oposición a la ejecución, debiendo seguirse el procedimiento establecido en el referido precepto, con suspensión de la ejecución de conformidad con el artículo 695.2 LEC.

Legitimación

De acuerdo con lo mencionado de contrario, en cuanto al planteamiento de la relación jurídico procesal, en particular los artículos 685 y 695.1 de la LEC, al ser parte ejecutada en el presente proceso ejecutivo.

Fundamentación jurídica de la oposición a la ejecución

Con arreglo a lo dispuesto en el artículo 695.1.4.ª de la LEC, en los procedimientos de ejecución hipotecaria se admitirá la oposición del ejecutado fundada en el carácter abusivo de una cláusula contractual que constituya el fundamento de la ejecución o que hubiese determinado la cantidad exigible. En este caso, las cláusulas [Nº DE CLÁUSULA] y [Nº DE CLÁUSULA] del contrato son abusivas y por ende nulas de pleno derecho, de conformidad con lo dispuesto en el artículo 83.1 del Real Decreto Legislativo 1/2007, debiendo ser inaplicadas, sin que pueda modificarse o integrarse el contenido de las mismas y, en consecuencia, procede reducir la cantidad por la que fue despachada ejecución a [IMPORTE] euros.

Costas

De acuerdo con lo dispuesto en el artículo 539.2 LEC, estimada esta oposición procederá la imposición de las costas a la parte ejecutante.

Por lo expuesto,

SUPLICO AL TRIBUNAL: Que tenga por presentado este escrito con sus documentos adjuntos y copia de todo ello, me tenga por comparecido y parte en la representación que ostento de D./Dña. [NOMBRE Y APELLIDOS DEL EJECUTADO] y por formulada OPOSICIÓN A LA EJECUCIÓN DESPACHADA SOBRE BIEN HIPOTECADO POR ABUSIVIDAD DE LAS CLÁUSULAS [Nº DE CLÁUSULA] Y [Nº DE CLÁUSULA] DEL CONTRATO, al amparo de lo previsto en el artículo 695.1.4.ª de la LEC, y admitida la misma, con suspensión de la ejecución, convoque a las partes a la celebración de la comparecencia prevista en el artículo 695.2 de la LEC y, celebrada que sea la misma, dicte resolución en forma de auto por el que, estimando la oposición formulada, mande inaplicar las citadas cláusulas y reducir el importe de la cantidad a [IMPORTE] euros, con imposición de las costas de la presente oposición a la parte ejecutante.

Es Justicia que insto en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Letrado/a: [FIRMA] Firma del Procurador/a: [FIRMA]
