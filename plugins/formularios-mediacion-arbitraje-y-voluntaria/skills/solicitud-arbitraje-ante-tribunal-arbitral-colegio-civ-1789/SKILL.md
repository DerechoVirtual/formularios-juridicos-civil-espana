---
name: solicitud-arbitraje-ante-tribunal-arbitral-colegio-civ-1789
description: "Solicitud de arbitraje ante el Tribunal Arbitral del Colegio de Abogados. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud de arbitraje ante el Tribunal Arbitral del Colegio de Abogados

> Formulario **CIV-1789** del plugin **Mediación, MASC, arbitraje y jurisdicción voluntaria** (`formularios-mediacion-arbitraje-y-voluntaria`) · Civil › Jurisdicción voluntaria, MASC, mediación y arbitraje · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud de arbitraje ante el Tribunal Arbitral del Colegio de Abogados» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud de arbitraje ante el Tribunal Arbitral del Colegio de Abogados” para mi caso». También puedes invocarla directamente con `/formularios-mediacion-arbitraje-y-voluntaria:solicitud-arbitraje-ante-tribunal-arbitral-colegio-civ-1789`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-mediacion-arbitraje-y-voluntaria:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Mediación, MASC, arbitraje y jurisdicción voluntaria) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] DENOMINACIÓN SOCIAL (7 veces)
- [ ] FECHA (6 veces)
- [ ] IMPORTE (6 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] NOMBRE DE LA PARTE (4 veces)
- [ ] Nº (3 veces)
- [ ] ACTO O RESOLUCIÓN (2 veces)
- [ ] ACTIVIDAD
- [ ] DIRECCIÓN
- [ ] FECHAS
- [ ] LUGAR
- [ ] NOMBRE Y APELLIDOS
- [ ] Nº DE COLEGIADO/A
- [ ] Nº DE DOCUMENTO
- [ ] Nº DE FAX
- [ ] TELÉFONO
- [ ] ÓRGANO O PERSONA

## Normas que cita el formulario

- No cita artículos concretos; Claude localizará las normas aplicables con Jurisprudenciator si el documento las necesita.

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

Escrito solicitando arbitraje al Tribunal Arbitral del Ilustre Colegio de Abogado/as en cumplimiento con lo dispuesto en el Reglamento de Arbitraje de dicho Colegio Profesional, siendo la cuestión que pretende resolverse la del incumplimiento de la obligación de no competencia acordada entre ambas sociedades solicitantes y que ha sido incumplida por una de ellas.

SOLICITUD DE ARBITRAJE

Que se formula ante el Tribunal Arbitral del Iltre. Colegio de Abogado/as de [LOCALIDAD] en cumplimiento con lo dispuesto en el Reglamento de Arbitraje del Colegio de Abogado/as de [LOCALIDAD], en atención a los siguientes

EXTREMOS

1) Solicitantes del arbitraje. Solicitan el arbitraje del Tribunal Arbitral las siguientes partes:

a) [DENOMINACIÓN SOCIAL], lo que se acredita mediante copia autorizada y apostillada del acuerdo de la referida sociedad de cambio de denominación social y modificación de estatutos sociales, así como certificación apostillada emitida por la Cámara de Comercio de [LOCALIDAD], documentos que junto con las correspondientes traducciones se acompañan señaladas de DOCUMENTOS NÚMEROS [Nº] a
b) [DENOMINACIÓN SOCIAL], lo que se acredita mediante la copia de las escrituras de reelección de cargos y modificación de denominación social que se acompañan señaladas de DOCUMENTOS NÚMEROS [Nº] a

2) Abogado/a encargado de la defensa. El Abogado/a encargado de la defensa es [NOMBRE Y APELLIDOS], Colegiado/a número [Nº DE COLEGIADO/A] del Iltre. Colegio de Abogado/as de [LOCALIDAD] con domicilio profesional en el despacho [DIRECCIÓN] con teléfono [TELÉFONO], fax [Nº DE FAX] y email

3) Nombre y domicilio de las demás partes. Las pretensiones de los solicitantes se ejercen contra [ACTO O RESOLUCIÓN] con domicilio en [LOCALIDAD]

4) Breve descripción del contrato de que deriva la cuestión que pretende resolverse. Ambas sociedades solicitantes del arbitraje, esto es, [DENOMINACIÓN SOCIAL] y [DENOMINACIÓN SOCIAL], suscribieron, respectivamente, en fechas [FECHAS] y [FECHA], sendos contratos en virtud de los cuales [NOMBRE DE LA PARTE] se obligó a no efectuar actividad comercial o industrial alguna de naturaleza similar a las que ejercían las citadas sociedades durante un periodo de cinco años cuya vigencia finalizaba el [FECHA], obligación que asumió [NOMBRE DE LA PARTE] a cambio del pago por parte de las sociedades de la cantidad de [IMPORTE] euros ( € [IMPORTE]).

La cuestión que pretende resolverse mediante el arbitraje es el incumplimiento de la citada obligación de no competencia de [NOMBRE DE LA PARTE] frente a ambas sociedades solicitantes, A este respecto, [NOMBRE DE LA PARTE] ha incumplido esos pactos en tanto que ha participado o gestionado varias empresas que han llevado a cabo y cuyo objeto social era de naturaleza similar a las de [DENOMINACIÓN SOCIAL], concretamente la venta de artículos relativos a la [ACTIVIDAD] durante los años en que la citada prohibición se hallaba vigente, además de haber contratado a trabajadores de [DENOMINACIÓN SOCIAL], actividad igualmente prohibida por los mencionados pactos.

5) Pretensiones de los solicitantes. El incumplimiento del pacto suscrito por [ÓRGANO O PERSONA], descrito en el anterior extremo, faculta a los solicitantes a pretender la devolución del precio pagado por el citado pacto, esto es, la cantidad de [IMPORTE] euros ( € [IMPORTE]), más el abono de los intereses legales devengados por tal cantidad, que, en este momento ascienden a más de [IMPORTE] euros ( € [IMPORTE]), más el abono de los daños y perjuicios cuya cuantificación se efectuará en el momento procesal oportuno, por no ser posible la determinación por ahora del daño sufrido, y, finalmente, el abono de las costas o gastos legales.

6) Sometimiento al arbitraje, convenio arbitral y modalidad de arbitraje. Los solicitantes y la parte demandada suscribieron un convenio arbitral para dirimir cualquier conflicto que se derivara en relación con el contrato en el que se acordó el pacto de no competencia, esto es, en el contrato de fecha [FECHA] (PACTO [Nº] del mismo), el cual originó el posterior contrato de fecha [FECHA] Ello se acredita mediante aportación del contrato de fecha [FECHA], que se acompaña señalado de DOCUMENTO NÚMERO [Nº DE DOCUMENTO] En cuanto a la modalidad del arbitraje, se solicita que los árbitros diriman la cuestión litigiosa con sujeción a derecho designándose para la resolución del conflicto tres árbitros, según lo acordado en el convenio arbitral suscrito por las partes.

Por todo lo expuesto,

A ESTE TRIBUNAL ARBITRAL SOLICITO:

que tenga por presentado este escrito, por solicitada la apertura del procedimiento arbitral por las compañías [DENOMINACIÓN SOCIAL] contra [ACTO O RESOLUCIÓN] por los motivos y con las pretensiones expuestas, y, previos los trámites pertinentes, acuerde admitir la iniciación del procedimiento arbitral, con los demás pronunciamientos inherentes.

Por ser de Justicia que pido en [LUGAR], a [FECHA].

Firma	Firma

========================================================================
