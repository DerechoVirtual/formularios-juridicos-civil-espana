---
name: oposicion-ejecucion-pluspeticion-derivada-clausula-civ-1438
description: "Oposición a la ejecución por pluspetición derivada de cláusula abusiva. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Oposición a la ejecución por pluspetición derivada de cláusula abusiva

> Formulario **CIV-1438** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Oposición a la ejecución por pluspetición derivada de cláusula abusiva» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Oposición a la ejecución por pluspetición derivada de cláusula abusiva” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:oposicion-ejecucion-pluspeticion-derivada-clausula-civ-1438`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (4 veces)
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] NOMBRE Y APELLIDOS
- [ ] Nº
- [ ] Nº DE DOCUMENTO
- [ ] NÚMERO
- [ ] SEDE

## Normas que cita el formulario

- art. 557.1.7 LEC
- art. 561.1.3 LEC
- art. 558 LEC
- art. 557.2 LEC

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

- Junto a «…ón número A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

Proceso de ejecución número

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

D. [NOMBRE Y APELLIDOS] Procurador de los Tribunales, en nombre y representación de [NOMBRE DEL REPRESENTADO/A], parte ejecutada en el procedimiento de ejecución arriba referenciado, según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], ante el Tribunal comparezco y como mejor proceda en Derecho DIGO:

Que, al amparo de lo dispuesto en los artículos 557.1.7 en relación 558 de la LEC, y dentro del plazo legal paso a formular la presente OPOSICIÓN A LA EJECUCIÓN por motivos de fondo consistente en pluspetición por nulidad parcial del contrato por abusividad, en base a los siguientes

HECHOS

PRIMERO.- La acción ejecutiva ejercitada en la presente demanda deriva de un presunto incumplimiento de pago de una póliza de préstamo bancario suscrita entre ejecutante y ejecutado, teniendo mi representado la condición de consumidor.

SEGUNDO.- La liquidación del ejecutante incluye la cantidad de [IMPORTE] euros en concepto de intereses moratorios, en aplicación de la cláusula número [NÚMERO] del contrato de préstamo.

Dicha cláusula es abusiva puesto que fija un interés moratorio equivalente al quíntuplo del interés legal del dinero, la cual determina su nulidad de pleno derecho, según han interpretando los tribunales de forma uniforme, citando por todas las SSAP de Tarragona de 10 de abril de 2012, rec. 640/2011 y de Alicante de 26 de julio de 2012, rec. 345/2011.

TERCERO.- Como indican las SSTJUE de 14 de junio de 2012, C-618/2010 y de 14 de marzo de 2013, C-415/2011, el juez debe controlar de oficio las cláusulas abusivas y, en el caso de intereses de demora, determinar si la cláusula de intereses de demora es abusiva contrastando el tipo de interés pactado con el tipo de interés legal y verificando que es adecuado para garantizar la realización de los objetivos que el interés de demora persigue, siendo que en este caso se incluyó en el contrato por la ejecutante con manifiesto abuso de derecho y supone un enriquecimiento injusto.

La nulidad de pleno derecho de la cláusula implica que deben excluirse de la deuda reclamada por el ejecutante la cantidad de [IMPORTE] euros en concepto de intereses de demora de conformidad a lo dispuesto en el artículo 561.1.3º de la LEC por inaplicación de la cláusula abusiva.

CUARTO.- La cantidad debida, por tanto es de [IMPORTE] euros, por principal e intereses remuneratorios, debiendo excluirse en todo caso los intereses de demora por abusivos.

QUINTO.- Se procede a realizar consignación de la cantidad efectivamente debida que es de [IMPORTE] Euros en la cuenta de depósitos y consignaciones de este Tribunal, a fin de que se proceda a su entrega al ejecutante y se proceda, de acuerdo con el artículo 558,1 LEC, a la suspensión de la ejecución en el resto de la cantidad reclamada.

A los anteriores hechos le son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

Procedimiento

Artículos 557, 558, 560 y 561 LEC sobre suspensión del curso de la ejecución en el supuesto de que formulada oposición por pluspetición se proceda a la consignación de las cantidades que se consideren debidas.

Legitimación

Artículo 538 LEC al ser parte ejecutada en el presente proceso de ejecución.

Oposición a la ejecución

Artículo 557.1.7ª y artículo 558 de la LEC fundada en la pluspetición. En cuanto a la oposición por abusividad, el citado apartado 7 del artículo 557.1 y la interpretación que se realiza en las SSTJUE de 14 de junio de 2012, C-618/2010 y 14 de marzo de 2013, C-415/2011, y en cuanto a la procedencia del motivo: AAP Madrid, Sección 11, 28 de Enero del 2013 (Recurso: 305/2012) y AAP Barcelona, Sección 14ª, 31 enero 2013 (Recurso 71/2012).

Suspensión del procedimiento ejecutivo

De acuerdo con lo establecido en el artículo 557.2 y 558 LEC, formulada la oposición y justificada la puesta a disposición del Tribunal para su inmediata entrega al ejecutante de la cantidad que se considera debida, se solicita la inmediata suspensión del curso de la ejecución dejando sin efecto los embargos y demás medidas de garantía acordadas. Se procede a la consignación en la cuenta de consignaciones y depósitos de este Tribunal de la cantidad efectivamente debida, cuestión acreditada mediante la aportación del resguardo justificativo del ingreso como documento

Costas

Artículo 561.2 de la LEC debiendo imponerse al ejecutante.

Por lo expuesto,

SUPLICO AL TRIBUNAL: Tenga por presentado este escrito con sus documentos y copias, sirviéndose admitirlos y unirlos a autos, teniendo por formulada, en tiempo y forma, OPOSICIÓN A LA EJECUCIÓN instada de contrario y, previa su sustanciación, se proceda a la suspensión inmediata del procedimiento ejecutivo, dejando sin efecto los embargos, y se estime la oposición formulada, inaplicando la cláusula declarada abusiva y reintegrando a mi mandante en la situación anterior a la ejecución, imponiéndose las costas a la ejecutante.

Lugar y fecha.

Firma abogado y procurador

========================================================================
