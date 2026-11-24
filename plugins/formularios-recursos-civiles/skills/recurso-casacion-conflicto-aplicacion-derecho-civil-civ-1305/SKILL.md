---
name: recurso-casacion-conflicto-aplicacion-derecho-civil-civ-1305
description: "Recurso de casación por conflicto en la aplicación del Derecho civil foral o especial. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Recurso de casación por conflicto en la aplicación del Derecho civil foral o especial

> Formulario **CIV-1305** del plugin **Recursos civiles: reposición, apelación, casación y queja** (`formularios-recursos-civiles`) · Civil › Recursos · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **recursos**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Recurso de casación por conflicto en la aplicación del Derecho civil foral o especial» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Recurso de casación por conflicto en la aplicación del Derecho civil foral o especial” para mi caso». También puedes invocarla directamente con `/formularios-recursos-civiles:recurso-casacion-conflicto-aplicacion-derecho-civil-civ-1305`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-recursos-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Recursos civiles: reposición, apelación, casación y queja) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (4 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] TIPO Y Nº DE PROCEDIMIENTO (2 veces)
- [ ] AÑO
- [ ] CONTENIDO DEL FALLO
- [ ] DÍA
- [ ] LUGAR
- [ ] MES
- [ ] MOTIVO
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] NOMBRE Y APELLIDOS
- [ ] Nº
- [ ] Nº DE PROCEDIMIENTO
- [ ] NÚMERO
- [ ] SECCIÓN
- [ ] SEDE

## Normas que cita el formulario

- art. 477.1 LEC
- art. 249.2 LEC
- art. 480 LEC
- art. 448.2 LEC
- art. 479.3 LEC
- art. 621.46 Código Civil
- art. 10.5 Código Civil

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

- Junto a «…ia dictada el día [FECHA] por el Tribunal de Instancia de [SEDE], plaza n.º [Nº]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

Rollo núm [Nº DE PROCEDIMIENTO]

A LA SECCIÓN [SECCIÓN] DE LA AUDIENCIA PROVINCIAL DE [LOCALIDAD] PARA ANTE LA SALA PRIMERA DEL TRIBUNAL SUPREMO

D. [NOMBRE Y APELLIDOS], Procurador de los Tribunales y de [NOMBRE DEL REPRESENTADO/A], según tengo acreditado en autos, ante la Sala comparezco y como mejor proceda en derecho DIGO:

1) Que en fecha [FECHA] esta parte ha sido notificada de la sentencia de fecha [FECHA] dictada en el Rollo arriba expresado, por la que [CONTENIDO DEL FALLO]

2) Que entendiendo que dicha sentencia no es ajustada a derecho, dicho sea con los debidos respetos y en términos de defensa, por medio del presente escrito, al amparo de lo dispuesto en el artículo 477.1 de la LEC, interpongo contra la misma RECURSO DE CASACIÓN, fundado en la infracción de normas aplicables para resolver las cuestiones objeto del proceso, en base a las siguientes ALEGACIONES:

I. ADMISIBILIDAD DEL RECURSO

Que la sentencia dictada el por parte de esa Sección de la Audiencia Provincial de [LOCALIDAD] en resolución del recurso de apelación presentado por esta parte ante la sentencia dictada el día [FECHA] por el Tribunal de Instancia de [SEDE], plaza n.º [Nº] en los autos [TIPO Y Nº DE PROCEDIMIENTO] en proceso ordinario tramitado conforme al art. 249.2 de la LEC, por lo que es recurrible en casación, conforme dispone el art. 477.1 de la LEC y produce un evidente gravamen a esta parte.

El presente recurso se interpone dentro del plazo de veinte días establecido en el artículo 480 de la LEC, computados conforme al artículo 448.2 de la LEC.

Que, en cumplimiento de lo establecido en el art. 479.3 de la LEC, debemos indicar, dicho sea en términos de defensa y con los debidos respetos, que la referida sentencia vulnera los siguientes preceptos legales:

Primero.- Al amparo del art. 477.1 de la LEC por infracción de las normas aplicables para resolver las cuestiones objeto del proceso, por aplicación indebida del art. 16.1 y 10.5 del Código Civil y no aplicación del art. 621.46 del Código Civil de Cataluña.

Segundo.- Por infracción de los artículos 1095 en relación con los arts. 1462, 1464 y 1469, todos ellos del Código Civil y no aplicación del art. 621.46 del Código Civil de Cataluña.

Tercero.- [MOTIVO]

Los anteriores motivos se basan en los siguientes

II. FUNDAMENTOS DEL RECURSO

El primer motivo de casación invocado lo es por infracción legal de los arts. 16.1 en relación con el artículo 10.5 del Código Civil, en cuanto que la sentencia de segunda instancia aplica indebidamente las normas comunes del Código Civil, cuando el contrato está sujeto a las normas de derecho foral catalán y, más concretamente, al instituto de la lesión "ultradimidium" regulada en el art. 621.46 del Código Civil de Cataluña.

La sentencia de instancia fundamenta la aplicación de las normas del Código Civil en el hecho de que ninguno de los contratantes tiene vecindad civil catalana, concretamente el demandante es de vecindad valenciana en tanto que el demandado es de vecindad navarra. Sin embargo, en este caso, se ejercitaba la acción de rescisión de la compraventa sobre un inmueble sito en Cataluña, concretamente en [LOCALIDAD], por lo que es irrelevante la vecindad civil de los contratantes, y ello es así porque versando el tema litigioso sobre la rescisión de un contrato de compraventa por lesión "ultradimidium" rige como punto de conexión el de la situación de la cosa, es decir, será aplicable la normativa correspondiente recogida en el art. 621.46 del Código Civil de Cataluña.

Así lo dispone expresamente el artículo 10.5 del Código Civil, al cual se remite el artículo 16, apartado uno, párrafo primero, del Código Civil, con arreglo al que los conflictos de leyes que puedan surgir por la coexistencia de distintas legislaciones en el territorio español se resolverán según las normas contenidas en el Capítulo IV (Normas de Derecho Internacional Privado). En este punto, el artículo 10, apartado cinco, establece que, a falta de sometimiento expreso, se aplicará a los contratos relativos a bienes inmuebles la ley del lugar donde estén sitos, a diferencia del resto de obligaciones contractuales a las que se refiere el párrafo primero del mismo artículo 10.5. Por tanto, en el presente caso donde ninguna de las partes alega la sumisión expresa, ni la misma consta en modo alguno en el contrato, y estando el inmueble objeto de la enajenación onerosa se halla situado en territorio de Cataluña, debe aplicarse la legislación catalana con total independencia de la vecindad civil del comprador, lo cual se establece imperativamente en los mencionados artículos del Código Civil.

Por tanto, interesamos que se case la sentencia recurrida y se resuelva sobre la cuestión debatida en forma concorde a las normas legales aplicables al supuesto de autos, concretamente el art. 621.46 del Código Civil de Cataluña, tal como se interesa en el siguiente motivo.

El segundo motivo de casación invocado trae causa de la estimación del anterior, de manera que se produce infracción, por aplicación indebida, de los artículos 1095 en relación con los arts. 1462, 1464 y 1469, todos ellos del Código Civil, siendo aplicable al supuesto de autos el art. 621.46 del Código Civil de Cataluña.

En el presente caso, no estamos ante un supuesto de aplicación del contenido obligacional del contrato de compraventa civil común, sino de aplicación del régimen específico de la acción rescisoria contemplada en el artículo 621.46 del Código Civil de Cataluña al contrato de autos, lo que necesariamente implica la estimación de la pretensión sostenida por esta parte, puesto que es indubitado que mi representado ha sufrido una lesión superior en más de la mitad del precio justo, requisito éste que la jurisprudencia ha venido calificando como de naturaleza objetiva, tal como se recoge en las SSTSJ Cataluña de 4 de julio de 1994 y 25 de mayo de 2000, rec. 6/2000, entre otras, resultando acreditada tal lesión por la pericial practicada en estos autos, la cual valora los bienes conforme a su valor real o de mercado en el momento de la venta, según resulta aceptado en la sentencia dictada en primera instancia, siendo suficiente para que nazca la acción la perfección del contrato, aunque el mismo no haya sido consumado, según indicara la STSJ Cataluña 7 de octubre de 1991 .

En consecuencia, y por aplicación de la legislación foral catalana, procede estimar las pretensiones sostenidas por esta representación en su demanda, con revocación de las sentencias recurridas.

Por lo expuesto,

SUPLICO A LA SALA que tenga por presentado este escrito, junto con sus documentos y copias de todo ello, se sirva admitirlo, teniéndome por personado ante la Sala Primera del Tribunal Supremo y por interpuesto en tiempo y forma recurso de casación frente a la sentencia de esa Audiencia número [NÚMERO] de fecha [FECHA] dictada en los autos [TIPO Y Nº DE PROCEDIMIENTO], y previos los trámites legales oportunos y remisión de las actuaciones a la Sala Primera del Tribunal Supremo, se dicte por dicha Sala sentencia que declare haber lugar al recurso de casación y proceda a la casación y anulación de la sentencia de la Audiencia Provincial impugnada.

OTROSÍ PRIMERO DIGO que, de conformidad con lo dispuesto en los apartados 3.d) y 6 de la disposición adicional decimoquinta de la LOPJ acompaño a este escrito resguardo de consignación en la cuenta de Depósitos y Consignaciones abierta a nombre del Tribunal del depósito exigido para interponer el recurso por importe de 50 euros.

Por lo que, SUPLICO A LA SALA que tenga por constituido el depósito, dejando interesada desde este momento su devolución para el caso de estimación total o parcial del recurso.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma Procurador y Abogado

========================================================================
