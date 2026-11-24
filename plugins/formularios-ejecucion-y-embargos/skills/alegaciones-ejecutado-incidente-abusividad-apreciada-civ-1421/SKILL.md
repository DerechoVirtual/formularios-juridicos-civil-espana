---
name: alegaciones-ejecutado-incidente-abusividad-apreciada-civ-1421
description: "Alegaciones del ejecutado en el incidente de abusividad apreciada de oficio. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Alegaciones del ejecutado en el incidente de abusividad apreciada de oficio

> Formulario **CIV-1421** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Escrito del ejecutado (consumidor) por el que, tras recibir la demanda ejecutiva y la providencia que le da traslado, formula alegaciones en el incidente de control de oficio del carácter abusivo de cláusulas del título ejecutivo (vencimiento anticipado e intereses moratorios), conforme al art. 552.1 LEC, solicitando la denegación del despacho de ejecución o, subsidiariamente, la inaplicación de la cláusula de intereses moratorios.

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Alegaciones del ejecutado en el incidente de abusividad apreciada de oficio» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Alegaciones del ejecutado en el incidente de abusividad apreciada de oficio” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:alegaciones-ejecutado-incidente-abusividad-apreciada-civ-1421`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] CLÁUSULA (2 veces)
- [ ] FIRMA (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL EJECUTADO (2 veces)
- [ ] Nº DE PROCEDIMIENTO (2 veces)
- [ ] AÑO
- [ ] DÍA
- [ ] FECHA
- [ ] IMPORTE
- [ ] LOCALIDAD
- [ ] MES
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] Nº DE CLÁUSULA
- [ ] Nº DE DOCUMENTO
- [ ] Nº DE PLAZA
- [ ] PORCENTAJE
- [ ] SEDE

## Normas que cita el formulario

- art. 552.1 LEC
- art. 693.2 LEC
- art. 20 Ley 16/2011
- art. 114.I LH

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

Proceso de ejecución [Nº DE PROCEDIMIENTO]

AL TRIBUNAL

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales y de [NOMBRE Y APELLIDOS DEL EJECUTADO], actuando en representación de [NOMBRE Y APELLIDOS DEL EJECUTADO], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], en el procedimiento de ejecución número [Nº DE PROCEDIMIENTO], seguido contra mi representado, comparezco y como mejor proceda en Derecho DIGO:

1) Que en fecha [FECHA] mi representado ha sido notificado de la demanda ejecutiva y de la providencia en la que se le da traslado para que alegue sobre la posible abusividad de las cláusulas [CLÁUSULA] y [CLÁUSULA] del título ejecutivo.

2) Que mediante el presente escrito me persono en el proceso de ejecución y, evacuando el traslado conferido, de conformidad con lo dispuesto en el art. 552.1 de la LEC, formulo alegaciones sobre el carácter abusivo de las referidas cláusulas, en base a los siguientes

HECHOS Y FUNDAMENTOS

PRIMERO.- La primera de las cláusulas referidas en la providencia es la de vencimiento anticipado, cuyo pacto es totalmente abusivo por cuanto que el acreedor, al amparo de esta cláusula, ha declarado vencida toda la deuda por el impago de uno solo de los plazos [AJUSTAR AL CASO: número de plazos impagados], lo cual supone un grave desequilibrio para mi representado. Al respecto, debe tenerse en cuenta que la legislación ha introducido un periodo mínimo de impago para atemperar las consecuencias desproporcionadas de la aplicación de este tipo de cláusulas, que ni tan siquiera ha sido respetado por el acreedor y, en este sentido, en el ámbito de los préstamos y créditos hipotecarios, el artículo 693.2 de la LEC condiciona el vencimiento total en caso de falta de pago al impago de doce o quince plazos mensuales según el contrato se encuentre, respectivamente, en la primera o segunda mitad de su duración.

Por tanto, la cláusula de vencimiento anticipado que se pretende hacer valer para la ejecución de un inmueble de uso residencial en contrato concertado con mi representado, como consumidor persona física, es nula por abusiva, por lo que debe denegarse la ejecución por este motivo.

Por tanto, debe declararse la abusividad de esta cláusula y, por ello, denegar el despacho de ejecución al no poder considerarse vencida la deuda por nulidad de la misma.

SEGUNDO.- La segunda de las cláusulas referidas en la providencia es la de intereses moratorios pactada en la cláusula [Nº DE CLÁUSULA] del título ejecutivo, que fija un interés moratorio del [PORCENTAJE] %.

Como indican las SSTJUE de 14 de junio de 2012, C-618/10, y de 14 de marzo de 2013, C-415/11, el juez debe controlar de oficio las cláusulas abusivas y, en el caso de intereses de demora, determinar si la cláusula es abusiva contrastando el tipo de interés pactado con el tipo de interés legal y verificando que es adecuado para garantizar la realización de los objetivos que el interés de demora persigue, siendo que en este caso se incluyó en el contrato por el ejecutante con manifiesto abuso de derecho y supone un enriquecimiento injusto y, en este sentido, excede desproporcionadamente los parámetros legales manejados en la materia, como son los del artículo 20 de la Ley 16/2011, de 24 de junio, de contratos de crédito al consumo, y del artículo 114.III de la Ley Hipotecaria, en su redacción dada por la Ley 5/2019, de 15 de marzo, reguladora de los contratos de crédito inmobiliario. En este punto, el Tribunal Supremo ya se había pronunciado sobre la abusividad de los intereses moratorios que excedieran en más de dos puntos del remuneratorio (tres en la nueva legislación de 2019) en los préstamos con garantía real y, en relación con los límites del art. 114.III LH en la redacción de la Ley 1/2013, ya había indicado que dicho precepto no puede servir como derecho supletorio tras la declaración de abusividad de la cláusula de intereses moratorios conforme a la normativa sobre protección de consumidores, de manera que la declaración de nulidad por abusividad afecta al exceso respecto del interés remuneratorio pactado (STS de 18 de febrero de 2016, rec. 2211/2014).

En este caso, la cláusula de intereses moratorios supone un incremento desproporcionado en contraste con el interés remuneratorio, que excede ampliamente de los límites establecidos anteriormente expuestos, de manera que debe declararse nula por abusiva.

La nulidad de pleno derecho de la cláusula implica que deben excluirse de la deuda reclamada por el ejecutante la cantidad de [IMPORTE] euros en concepto de intereses de demora, por inaplicación de la cláusula abusiva.

Por lo expuesto,

SUPLICO AL TRIBUNAL: Tenga por presentado este escrito, con justificante de traslado a la parte contraria, se sirva admitirlo, teniendo por formuladas las presentes alegaciones en tiempo y forma y, en virtud de lo expuesto, acuerde declarar nulas por abusivas las cláusulas expresadas y denegar el despacho de ejecución o, subsidiariamente, inaplicar la cláusula de intereses moratorios.

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Abogado/a: [FIRMA] Firma del Procurador/a: [FIRMA]
