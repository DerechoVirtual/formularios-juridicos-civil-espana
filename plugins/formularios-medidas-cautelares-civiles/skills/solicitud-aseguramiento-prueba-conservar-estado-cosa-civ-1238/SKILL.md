---
name: solicitud-aseguramiento-prueba-conservar-estado-cosa-civ-1238
description: "Solicitud de aseguramiento de prueba para conservar el estado de una cosa mueble. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud de aseguramiento de prueba para conservar el estado de una cosa mueble

> Formulario **CIV-1238** del plugin **Medidas cautelares y diligencias preliminares** (`formularios-medidas-cautelares-civiles`) · Civil › Medidas cautelares y diligencias preliminares · normativa revisada el 24-11-2026.

## Qué es

Escrito de solicitud de aseguramiento de prueba, previo a la demanda, consistente en conservar el estado de una cosa mueble para poder practicar después una prueba pericial (arts. 297 y 298 LEC), designando un depositario que retire el bien del poder de quien lo retiene. El modelo toma como ejemplo un vehículo retenido en un taller por una reparación defectuosa.

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud de aseguramiento de prueba para conservar el estado de una cosa mueble» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud de aseguramiento de prueba para conservar el estado de una cosa mueble” para mi caso». También puedes invocarla directamente con `/formularios-medidas-cautelares-civiles:solicitud-aseguramiento-prueba-conservar-estado-cosa-civ-1238`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-medidas-cautelares-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Medidas cautelares y diligencias preliminares) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] DOMICILIO (6 veces)
- [ ] DENOMINACIÓN SOCIAL (4 veces)
- [ ] MATRÍCULA (3 veces)
- [ ] NOMBRE DEL TALLER (3 veces)
- [ ] NOMBRE DEL DEPOSITARIO (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] Nº (2 veces)
- [ ] SEDE (2 veces)
- [ ] AÑO
- [ ] DEFECTOS CONSTATADOS
- [ ] DÍA
- [ ] FECHA
- [ ] LOCALIDAD
- [ ] MES
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] NOMBRE Y APELLIDOS DEL SOLICITANTE

## Normas que cita el formulario

- art. 1600 Código Civil
- art. 51 LEC
- art. 297.1 LEC
- art. 297 LEC

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

Don/Doña [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, actuando en representación de [NOMBRE Y APELLIDOS DEL SOLICITANTE], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº], por medio de la presente formulo solicitud de aseguramiento de prueba consistente en conservar el estado en el que se encuentra [BIEN; EJEMPLO: el vehículo matrícula [MATRÍCULA]], que se encuentra en [LUGAR; EJEMPLO: el taller [NOMBRE DEL TALLER] sito en [DOMICILIO]], previo a la interposición de la demanda a interponer frente a la entidad [DENOMINACIÓN SOCIAL], con domicilio en [DOMICILIO], y DIGO:

HECHOS

ÚNICO.- Que mi representado/a encargó la realización de una reparación en el vehículo de su propiedad matrícula [MATRÍCULA], tal y como resulta de la certificación de la Jefatura Provincial de Tráfico que se adjunta como documento n.º [Nº], reparación que fue encargada a la entidad [DENOMINACIÓN SOCIAL], domiciliada en [DOMICILIO] y que es titular del taller [NOMBRE DEL TALLER] sito en [DOMICILIO].

El pasado [FECHA] se avisó a mi principal de la realización de la reparación, indicándole que el vehículo estaba a su disposición. Constituido en el taller, se constató por mi principal que la reparación no se había realizado correctamente ya que [DEFECTOS CONSTATADOS]. A pesar de esta manifestación, los responsables del taller indicaron que la reparación se había llevado a cabo en forma correcta, negándose a verificar las objeciones que mi principal les había puesto de manifiesto.

Ante esta actitud, mi principal se negó a abonar el importe de la reparación ante el incumplimiento contractual del taller, negándose éste a entregar el vehículo arguyendo que lo retenían en prenda para el cobro de los trabajos realizados y con fundamento en el art. 1600 del Código Civil.

Ante ello, mi mandante tiene la intención de dirigirse judicialmente frente al taller en reclamación de los daños y perjuicios que la irregular reparación del vehículo le ha generado, algo para lo que es esencial el mantenimiento del vehículo en el mismo estado en el que se encontraba al tiempo en el que mi mandante lo recibió, con la finalidad de proceder en el seno del correspondiente proceso a practicar la pertinente prueba pericial.

Es por ello que se interesa como medida de aseguramiento de la prueba que se deposite el vehículo de mi principal en poder de [NOMBRE DEL DEPOSITARIO], al que se designa como depositario, autorizándole para que, con la pertinente orden judicial, proceda a retirar el vehículo de mi principal del taller sito en [DOMICILIO] y del que es titular la mercantil [DENOMINACIÓN SOCIAL], ya que es la medida que garantizará el mantenimiento del vehículo en el mismo estado en el que se encuentra en la actualidad y sin intervenciones de tal mercantil. Solamente de esta forma se estima que podrá garantizarse el resultado de la prueba pericial que ulteriormente se pueda practicar.

FUNDAMENTOS DE DERECHO

PRIMERO.- Competencia. Le corresponde a los Tribunales de Instancia de [SEDE], al ser los competentes para conocer el procedimiento principal (arts. 297.3 y 293.2 LEC), ya que la mercantil demandada se encuentra domiciliada en este partido judicial (art. 51 LEC).

SEGUNDO.- Legitimación. Le corresponde a esta parte ante su condición de futura demandante en el pleito que se desea interponer (art. 297.1 LEC).

TERCERO.- Procedimiento. Es el previsto en los arts. 297 y siguientes de la LEC.

CUARTO.- Fondo de la petición. Ante las circunstancias antes expuestas, se estima que la medida interesada tiene por finalidad garantizar el resultado de una prueba esencial a practicar en el proceso que se pretende interponer y cuyo objeto se ha delimitado, resultando el mismo imposible sin esta medida de aseguramiento. Es por ello que se considera que concurren los requisitos que para acordar el aseguramiento de prueba interesado se fijan en los arts. 297 y 298 LEC.

En base a lo anterior,

SUPLICO AL TRIBUNAL: Que tenga por presentado este escrito y documentos adjuntos al mismo y por comparecido/a al Procurador/a Don/Doña [NOMBRE Y APELLIDOS], en representación de Don/Doña [NOMBRE Y APELLIDOS], y en base a lo en él señalado se tenga a bien acordar como medida de aseguramiento de prueba el depósito del vehículo de mi principal, matrícula [MATRÍCULA], en poder de [NOMBRE DEL DEPOSITARIO], al que se designa como depositario, autorizándole para que, con la pertinente orden judicial, proceda a retirar el mencionado vehículo del taller [NOMBRE DEL TALLER], sito en [DOMICILIO], y del que es titular la mercantil [DENOMINACIÓN SOCIAL].

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma de Abogado/a y de Procurador/a.
