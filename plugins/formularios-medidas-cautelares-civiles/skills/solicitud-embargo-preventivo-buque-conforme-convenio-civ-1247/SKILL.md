---
name: solicitud-embargo-preventivo-buque-conforme-convenio-civ-1247
description: "Solicitud de embargo preventivo de buque conforme al Convenio de 10 de mayo de 1952. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud de embargo preventivo de buque conforme al Convenio de 10 de mayo de 1952

> Formulario **CIV-1247** del plugin **Medidas cautelares y diligencias preliminares** (`formularios-medidas-cautelares-civiles`) · Civil › Medidas cautelares y diligencias preliminares · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud de embargo preventivo de buque conforme al Convenio de 10 de mayo de 1952» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud de embargo preventivo de buque conforme al Convenio de 10 de mayo de 1952” para mi caso». También puedes invocarla directamente con `/formularios-medidas-cautelares-civiles:solicitud-embargo-preventivo-buque-conforme-convenio-civ-1247`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-medidas-cautelares-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Medidas cautelares y diligencias preliminares) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (5 veces)
- [ ] BANDERA (3 veces)
- [ ] DENOMINACIÓN SOCIAL (3 veces)
- [ ] NOMBRE DEL BUQUE (3 veces)
- [ ] PUERTO (3 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] MATRÍCULA (2 veces)
- [ ] MUELLE (2 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] AÑO
- [ ] DIQUE
- [ ] DÍA
- [ ] MES
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] NOMBRE Y APELLIDOS
- [ ] SEDE

## Normas que cita el formulario

- art. 730.2 LEC
- art. 733.2 LEC
- art. 728.1 LEC
- art. 727.11.ª LEC

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

D. [NOMBRE Y APELLIDOS] Procurador de los Tribunales, actuando en representación de [NOMBRE DEL REPRESENTADO/A], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], por medio de la presente solicito medida cautelar de embargo del buque [NOMBRE DEL BUQUE] de bandera [BANDERA] y matrícula [MATRÍCULA] que se encuentra en el dique [DIQUE] del puerto de [PUERTO] y del que el armador es la mercantil [DENOMINACIÓN SOCIAL] de nacionalidad con domicilio en [LOCALIDAD] en base a los siguientes:

HECHOS

ÚNICO.-Que mi mandante prestó a la mercantil [DENOMINACIÓN SOCIAL] titular del buque [NOMBRE DEL BUQUE] de bandera [BANDERA] y que en el momento actual se encuentra atracado en el muelle [MUELLE] del puerto de [PUERTO] unos suministros por importe de [IMPORTE] Euros tal y como se desprende de los documentos [Nº DE DOCUMENTO] que se adjuntan, no abonándolos. Es por ello que esta parte tiene la intención de demandar a dicha mercantil para su abono si bien ante la presencia del buque en puerto y de cara a garantizar la efectividad de la reclamación que se va a entablar se solicita se acuerde de forma inmediata inaudita parte y antes de la interposición de la demanda el embargo preventivo del buque antes mencionado:

FUNDAMENTOS DE DERECHO

PRIMERO.- Competencia.-Le corresponde a este tribunal conforme a lo dispuesto en el art. 471 de la Ley de Navegación Marítima que será competente para decretar el embargo preventivo de un buque, el tribunal que tenga competencia objetiva para conocer de la pretensión principal o el del puerto o lugar en que se encuentre el buque o aquel al que se espera que el buque arribe, a elección del actor que solicita la adopción de la medida cautelar.

SEGUNDO.- Procedimiento.-Es el previsto en el art. 730.2 LEC al interesarse la adopción de la medida cautelar son carácter previo a la interposición de la demanda y sin audiencia del demandado (art. 733.2 LEC), de conformidad a lo establecido en el art. 470 de la Ley de Navegación Marítima.

TERCERO.- Naturaleza y regulación de la medida.- El art. 470.1 de la Ley de Navegación Marítima dispone que la medida cautelar de embargo preventivo de buques, tanto nacionales como extranjeros, se regulará por el Convenio Internacional sobre el Embargo Preventivo de Buques, hecho en Ginebra el 12 de marzo de 1999, por lo dispuesto en esta ley y, supletoriamente, por lo establecido en la Ley 1/2000, de 7 de enero, de Enjuiciamiento Civil. Dicha medida conllevará necesariamente la inmovilización del buque en el puerto donde se encuentre.

CUARTO.- Cumplimiento de los requisitos.-Se cumplen los requisitos establecidos en los artículos 472 y siguientes de la Ley de Navegación Marítima en relación con el citado Convenio de Ginebra de 1999 al invocarse un crédito marítimo de los contenidos en el art. 1 del referido Convenio, alegándose asimismo la causa que lo motiva y se ejercita respecto del buque que resulta embargable conforme a lo dispuesto en el art. 3 del mismo Convenio, presumiéndose que concurre el peligro por mora procesal y la urgencia de que tratan los artículos 728, 730.2 y 733.2 de la Ley de Enjuiciamiento Civil, según dispone el art. 476 de la Ley de Navegación Marítima.

QUINTO.- Peligro de mora.-Se deriva de la propia condición del bien sobre el que se solicita la medida de embargo que es un buque que en cualquier momento puede abandonar el puerto siendo el bien básico con cargo al que se puede garantizar el crédito de mi principal (art. 728.1 LEC).

SEXTO.- Medida interesada.-Es la del embargo preventivo de buques extranjeros por créditos marítimos conforme determina la Ley 14/2014, de 24 de julio, de Navegación Marítima, dictada para la efectividad en territorio español del Convenio de Ginebra de 12 de marzo de 1999 que en su art. 1.º indica que para dictar tal medida precaucional de garantía bastará que se alegue el derecho o créditos reclamados y la causa que los motiva, exigiendo en tal caso fianza en cantidad suficiente para responder de los daños, perjuicios y costas que puedan ocasionarse, siendo el concreto crédito fundamento de la reclamación el crédito marítimo a que se refiere el Convenio de Bruselas antes mencionado en su art. 1.1.l) que califica de crédito marítimo "Las mercancías, materiales, provisiones, combustibles, equipo (incluidos los contenedores) suministrados o servicios prestados al buque para su explotación, gestión, conservación o mantenimiento" (art. 727.11.ª LEC).

SÉPTIMO.- Caución.-Con fundamento en el art. 472 de la Ley de Navegación Marítima se solicita sea fijada ésta en [IMPORTE] Euros dadas las condiciones de derecho expuesto y los posibles perjuicios que se le pudieren generar por ello.

En base a lo anterior,

SUPLICO AL TRIBUNAL: Que tenga por presentado escrito con los documentos a él anejos y copias, tenga por comparecido a esta parte y acuerde el embargo del buque [NOMBRE DEL BUQUE] de bandera [BANDERA] y matrícula [MATRÍCULA] propiedad de la mercantil [DENOMINACIÓN SOCIAL] que se encuentra en el muelle [MUELLE] del puerto de [PUERTO] por el crédito marítimo que mi principal ostenta en la cantidad de [IMPORTE] Euros más la cantidad de [IMPORTE] Euros que prudencialmente se fijan para intereses y costas. De cara a su efectividad se solicita que se dirija oficio a la Autoridad marítima competente, para que se inmovilice el buque mediante guardia adecuada o por el medio que dicha Autoridad estime idóneo para impedir que el buque se haga a la mar. Esta medida cautelar se solicita que se acuerde con carácter previo a la presentación de la demanda que se verificará ante los Tribunales de [LOCALIDAD] en el plazo marcado por el art. 7 del Convenio de Bruselas y sin audiencia del demandado al concurrir motivos de urgencia. De cara a la adopción de tal medida cautelar se solicita asimismo que se tenga por ofrecida una caución de [IMPORTE] Euros.

a [DÍA] de [MES] de [AÑO]

Firma Abogado	Firma Procurador

========================================================================
