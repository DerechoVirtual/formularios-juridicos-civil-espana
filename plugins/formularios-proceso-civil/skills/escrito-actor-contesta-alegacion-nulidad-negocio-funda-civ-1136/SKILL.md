---
name: escrito-actor-contesta-alegacion-nulidad-negocio-funda-civ-1136
description: "Escrito del actor que contesta a la alegación de nulidad del negocio en que funda su pretensión. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito del actor que contesta a la alegación de nulidad del negocio en que funda su pretensión

> Formulario **CIV-1136** del plugin **Proceso civil: demandas, contestaciones, prueba y vista** (`formularios-proceso-civil`) · Civil › Escritos procesales (demanda, contestación, prueba, vista) · normativa revisada el 24-11-2026.

## Qué es

Escrito del actor en un juicio declarativo ordinario por el que contesta a la alegación del demandado de nulidad del contrato en que se funda la demanda (compraventa privada de una finca rústica), por dolo que afectaría al precio, defendiendo la plena validez del negocio y solicitando que se estime íntegramente la demanda.

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito del actor que contesta a la alegación de nulidad del negocio en que funda su pretensión» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito del actor que contesta a la alegación de nulidad del negocio en que funda su pretensión” para mi caso». También puedes invocarla directamente con `/formularios-proceso-civil:escrito-actor-contesta-alegacion-nulidad-negocio-funda-civ-1136`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-proceso-civil:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Proceso civil: demandas, contestaciones, prueba y vista) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (4 veces)
- [ ] Nº (4 veces)
- [ ] FECHA (3 veces)
- [ ] FIRMA (2 veces)
- [ ] NOMBRE O DENOMINACIÓN SOCIAL DEL ACTOR (2 veces)
- [ ] AÑO
- [ ] DESCRIPCIÓN DE LA FINCA
- [ ] DÍA
- [ ] LOCALIDAD
- [ ] MES
- [ ] NOMBRE O DENOMINACIÓN SOCIAL DEL DEMANDADO
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] NOMBRE Y APELLIDOS DEL VENDEDOR
- [ ] Nº DE PROCEDIMIENTO
- [ ] SEDE

## Normas que cita el formulario

- art. 1088 Código Civil
- art. 1254 Código Civil
- art. 1445 Código Civil
- art. 1269 Código Civil

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, en nombre y representación de [NOMBRE O DENOMINACIÓN SOCIAL DEL ACTOR], según tengo acreditado en los autos de juicio declarativo ordinario n.º [Nº DE PROCEDIMIENTO], seguidos en este Tribunal a instancia de [NOMBRE O DENOMINACIÓN SOCIAL DEL ACTOR] contra [NOMBRE O DENOMINACIÓN SOCIAL DEL DEMANDADO], ante el Tribunal comparezco y, como mejor proceda en Derecho, DIGO:

Que, dentro del plazo que al efecto me ha sido conferido, por medio del presente escrito vengo a contestar a la alegación, formulada por el demandado, de nulidad del contrato en que se funda la pretensión deducida por esta parte en la demanda, oponiéndome a la misma en base a los siguientes hechos y consideraciones jurídicas:

HECHOS

PRIMERO.– En fecha [FECHA], mi representado/a y el demandado suscribieron contrato privado de compraventa, en virtud del cual mi mandante adquirió la propiedad de la finca [DESCRIPCIÓN DE LA FINCA].

SEGUNDO.– El precio de la compraventa se fijó en [IMPORTE] euros, de los cuales [IMPORTE] euros fueron recibidos por el vendedor con anterioridad a la firma del contrato de compraventa, como se acredita con el recibo firmado por el demandado que se acompaña como DOCUMENTO N.º [Nº].

El resto del precio, es decir, [IMPORTE] euros, quedó aplazado para ser pagado por mi representado/a, sin abono de intereses, en [Nº] plazos mensuales de [IMPORTE] euros cada uno, resultando saldada dicha cantidad pendiente con fecha [FECHA], circunstancia que se acredita con los recibos firmados por el vendedor D./Dña. [NOMBRE Y APELLIDOS DEL VENDEDOR] y que se acompañan como DOCUMENTOS N.º [Nº] a [Nº].

TERCERO.– Es cierto que el valor de las fincas objeto del contrato cuya nulidad se postula es mínimamente superior al precio pactado; pero no pueden ocultarse ni dejar de considerarse las siguientes circunstancias:

A) En primer lugar, eran fincas rústicas, arrendadas muchas de ellas con rentas muy bajas, lo que no deja de ser un obstáculo o freno para su disposición, contando o no con el interés de los arrendatarios o colonos, algunos de los cuales, según propia confesión de la contestación a la demanda, eran tan antiguos como los propietarios. A ello no obsta que, con arreglo a la Ley de Arrendamientos Rústicos, tuvieran a la sazón las fincas ya carácter de suelo urbano, pues los arrendatarios o colonos estaban allí y de alguna manera habrían de ser resueltos los contratos, con las indemnizaciones correspondientes.

B) En efecto, hubo conversaciones independientes de las que llevaron al otorgamiento del contrato cuya nulidad se pretende, pero las ofertas no eran más elevadas que la que cristalizó.

C) Es normal, público y notorio que, cuando está en venta un bien inmueble con un valor determinado, puede haber, en muchos casos, dificultades para su realización y, cuando por las circunstancias que sean hay dificultades para hacerlo, lógicamente los precios bajan.

CUARTO.– El contrato de compraventa es plenamente válido al concurrir los requisitos necesarios de consentimiento, objeto y causa, sin que haya existido actuación dolosa o engaño alguno, habiéndose conducido las partes por las normas que la buena fe requiere en materia de contratación.

FUNDAMENTOS DE DERECHO

I.– COMPETENCIA, PROCEDIMIENTO Y LEGITIMACIÓN

Conforme esta parte con los razonamientos señalados por el demandado en cuanto a competencia, procedimiento y legitimación.

II.– El art. 1088 y siguientes del Código Civil, que regulan las obligaciones.

III.– El art. 1254 y siguientes del Código Civil, que regulan los contratos.

IV.– El art. 1445 del Código Civil dice que «Por el contrato de compra y venta uno de los contratantes se obliga a entregar una cosa determinada y el otro a pagar por ella un precio cierto, en dinero o signo que lo represente».

V.– El contrato de compraventa es plenamente válido al concurrir los requisitos necesarios de consentimiento, objeto y causa. No se ha acreditado que el consentimiento se prestase por error, violencia, intimidación o dolo. Como dice el art. 1269 del Código Civil, para que se aprecie dolo es preciso que medien palabras o maquinaciones insidiosas por parte de uno de los contratantes, de modo tal que el otro sea inducido a realizar un contrato que, sin tales palabras o maquinaciones insidiosas, no hubiera hecho.

Nada de ello acontece en la compraventa que nos ocupa. Y la STS de 22 de enero de 1988 afirma que, partiendo de que el dolo no se presume y debe ser acreditado por quien lo alega, no puede admitirse por meras conjeturas o deducciones.

Si ponemos en conexión el concepto y los requisitos que jurisprudencialmente se exigen para apreciar la existencia de ese vicio de la voluntad (así se ha dicho que el dolo, según cabe desprender de la redacción del art. 1269, comprende no sólo la insidia directa inductora del error en el otro contratante, sino también la reticencia del que calla o no advierte cuando tenía el deber de informar, que exige la buena fe; y, para su concurrencia, son precisos los siguientes requisitos: 1.º) una maquinación engañosa o una conducta insidiosa, que tanto puede consistir en una conducta activa como omisiva (reticencia en la omisión de hechos), dirigida a provocar la declaración negocial, que determine la voluntad de la otra parte a realizar el negocio que de otro modo no hubiese realizado; 2.º) que esa voluntad quede viciada por haberse emitido sin la natural libertad y conocimiento, a causa del engaño, coacción u otra insidiosa influencia; 3.º) que sea grave, es decir, que recaiga sobre la sustancia de la cosa que constituye el objeto negocial o sobre las condiciones que hubieran motivado su celebración, si se trata de anular el contrato; y 4.º) que no haya sido causado por un tercero ni empleado por las dos partes contratantes [SSTS de 27 de enero de 1988 o de 29 de marzo de 1994]); y si esta doctrina se pone en conexión con el supuesto debatido, aparece claro que los hoy litigantes suscribieron con fecha [FECHA] un contrato privado de compraventa plenamente válido. El demandado vendió la finca por no estar en condiciones, por razón de edad avanzada, de atenderla.

Si el demandado vendió la finca es porque en aquel momento le interesó, con independencia de que, de cara al mercado inmobiliario, su actitud fuera reprochable.

VI.– COSTAS

Por aplicación del mismo precepto invocado de adverso, procede la imposición de las costas al demandado.

Por todo lo expuesto,

SUPLICO AL TRIBUNAL.

Que tenga por presentado este escrito, en unión de los documentos que se acompañan, con sus copias, y por contestada la alegación de nulidad del negocio jurídico en que se funda la demanda formulada por el demandado y, previos los trámites legales, se sirva dictar sentencia estimando íntegramente la demanda, con expresa imposición de las costas de la litis a la contraria.

Es justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Abogado/a: [FIRMA] Firma del Procurador/a: [FIRMA]
