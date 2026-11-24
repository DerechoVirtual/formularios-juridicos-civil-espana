---
name: solicitud-prueba-anticipada-testigos-antes-inicio-civ-1239
description: "Solicitud de prueba anticipada de testigos antes del inicio del proceso. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud de prueba anticipada de testigos antes del inicio del proceso

> Formulario **CIV-1239** del plugin **Medidas cautelares y diligencias preliminares** (`formularios-medidas-cautelares-civiles`) · Civil › Medidas cautelares y diligencias preliminares · normativa revisada el 24-11-2026.

## Qué es

Escrito de solicitud de prueba testifical anticipada, antes de iniciar el proceso (arts. 293 a 296 LEC), cuando existe riesgo de que un testigo esencial no pueda declarar después, por ejemplo por enfermedad grave. Se acompaña listado de preguntas y, por razón del estado del testigo, se pide su declaración domiciliaria (art. 364 LEC). El modelo toma como ejemplo la declaración del arquitecto director de una obra, ingresado en un hospital.

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud de prueba anticipada de testigos antes del inicio del proceso» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud de prueba anticipada de testigos antes del inicio del proceso” para mi caso». También puedes invocarla directamente con `/formularios-medidas-cautelares-civiles:solicitud-prueba-anticipada-testigos-antes-inicio-civ-1239`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-medidas-cautelares-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Medidas cautelares y diligencias preliminares) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (11 veces)
- [ ] DENOMINACIÓN SOCIAL (4 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] AÑO (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] DÍA (2 veces)
- [ ] HOSPITAL (2 veces)
- [ ] MES (2 veces)
- [ ] SEDE (2 veces)
- [ ] AÑADIR LAS DEMÁS PREGUNTAS QUE PROCEDAN.
- [ ] ENFERMEDAD
- [ ] HECHO SOBRE EL QUE SE INTERROGA
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] NOMBRE Y APELLIDOS DEL SOLICITANTE
- [ ] Nº
- [ ] PROMOTORES

## Normas que cita el formulario

- art. 293.2 LEC
- art. 51 LEC
- art. 293.1 LEC
- art. 293 LEC
- art. 364 LEC
- art. 295 LEC

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

Don/Doña [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, actuando en representación de [NOMBRE Y APELLIDOS DEL SOLICITANTE], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº], por medio de la presente formulo solicitud de práctica de prueba testifical anticipada, previa a la interposición de la demanda, de Don/Doña [NOMBRE Y APELLIDOS], con domicilio en [DOMICILIO], y DIGO:

HECHOS

ÚNICO.- Que mi representado/a encargó la construcción de una vivienda unifamiliar a la mercantil [DENOMINACIÓN SOCIAL], domiciliada en [DOMICILIO], tal y como resulta del contrato al efecto suscrito que se adjunta como documento n.º 1, encargándose de la dirección de las obras el arquitecto técnico Don/Doña [NOMBRE Y APELLIDOS] y el arquitecto superior Don/Doña [NOMBRE Y APELLIDOS].

Debido a lo que se estiman que son deficiencias en el proceso constructivo, esta parte tiene la intención de interponer la pertinente demanda frente a la constructora [DENOMINACIÓN SOCIAL], proceso en el que se considera va a ser esencial la declaración del arquitecto superior Don/Doña [NOMBRE Y APELLIDOS], que debería intervenir en calidad de testigo al estimarse que las deficiencias son debidas a la incorrecta terminación de los trabajos, según resulta del dictamen pericial que al efecto se ha elaborado por parte de Don/Doña [NOMBRE Y APELLIDOS], que se adjunta a este escrito como documento n.º 2.

El arquitecto Don/Doña [NOMBRE Y APELLIDOS] se halla afectado/a de una grave enfermedad de [ENFERMEDAD], hallándose internado/a en el hospital [HOSPITAL], tal y como se desprende de la certificación médica adjunta como documento n.º 3, motivo por el que se solicita que se proceda a la práctica de su testimonio por anticipado, recibiéndole declaración en dicho centro hospitalario a la vista del listado de preguntas que se adjunta y de aquel que interesare la parte frente a la que se tiene intención de interponer la demanda, y sin asistencia de las partes, dado el delicado estado de salud en el que se encuentra el testigo antes mencionado.

FUNDAMENTOS DE DERECHO

PRIMERO.- Competencia. Le corresponde a los Tribunales de Instancia de [SEDE], al ser los competentes para conocer el procedimiento principal (art. 293.2 LEC), ya que la mercantil demandada se encuentra domiciliada en este partido judicial (art. 51 LEC).

SEGUNDO.- Legitimación. Le corresponde a esta parte ante su condición de futura demandante en el pleito que se desea interponer (art. 293.1 LEC).

TERCERO.- Procedimiento. Es el previsto en los arts. 293 y siguientes de la LEC, operando en cuanto a la declaración domiciliaria del testigo lo establecido en el art. 364 LEC.

CUARTO.- Fondo de la petición. Ante las circunstancias concurrentes en el testigo y que se derivan de la documentación médica adjunta, así como por la esencialidad y procedencia de su declaración, se entiende que concurren los requisitos que para acordar la práctica de la prueba testifical anticipada se fijan en los arts. 293 y 294 LEC, habiéndose proporcionado la completa identificación de la parte que va a ser demandada con la finalidad de que pueda participar en la práctica de la prueba, tal y como establece el art. 295 LEC.

En base a lo anterior,

SUPLICO AL TRIBUNAL: Que tenga por presentado este escrito y documentos adjuntos al mismo y por comparecido/a al Procurador/a Don/Doña [NOMBRE Y APELLIDOS], en representación de Don/Doña [NOMBRE Y APELLIDOS], y en base a lo en él señalado se tenga a bien acordar la práctica de la prueba testifical de Don/Doña [NOMBRE Y APELLIDOS], a verificar en el Hospital [HOSPITAL], en el que se encuentra ingresado/a, dando traslado de la petición formulada a la entidad que se pretende demandar, [DENOMINACIÓN SOCIAL], a fin de que proceda a determinar, si así lo tuviere por conveniente, las preguntas a formular al testigo antes mencionado.

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma de Abogado/a y de Procurador/a.

LISTADO DE PREGUNTAS

Listado de preguntas que presenta el Procurador/a Don/Doña [NOMBRE Y APELLIDOS] a fin de que sean respondidas por el testigo Don/Doña [NOMBRE Y APELLIDOS]:

1) Diga que es cierto que usted fue el arquitecto director de las obras de construcción de una vivienda unifamiliar en [LOCALIDAD], de la que los promotores eran [PROMOTORES] y la constructora [DENOMINACIÓN SOCIAL].

2) Diga si es cierto [HECHO SOBRE EL QUE SE INTERROGA].

[AÑADIR LAS DEMÁS PREGUNTAS QUE PROCEDAN.]

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma de Abogado/a y de Procurador/a.
