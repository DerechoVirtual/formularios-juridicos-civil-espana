---
name: solicitud-mediacion-familiar-parte-cumplimiento-pacto-civ-0007
description: "Solicitud de mediación familiar por una parte en cumplimiento de un pacto previo de mediación. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud de mediación familiar por una parte en cumplimiento de un pacto previo de mediación

> Formulario **CIV-0007** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud de mediación familiar por una parte en cumplimiento de un pacto previo de mediación» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud de mediación familiar por una parte en cumplimiento de un pacto previo de mediación” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:solicitud-mediacion-familiar-parte-cumplimiento-pacto-civ-0007`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] CALLE (2 veces)
- [ ] CORREO ELECTRÓNICO (2 veces)
- [ ] DNI/NIE (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] LETRA (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] Nº (2 veces)
- [ ] PISO (2 veces)
- [ ] TELÉFONO (2 veces)
- [ ] AÑO
- [ ] DÍA
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] MES
- [ ] NOMBRE DE LA INSTITUCIÓN DE MEDIACIÓN
- [ ] Nº DE CLÁUSULA

## Normas que cita el formulario

- art. 16.1.b Ley 5/2012
- art. 16 Ley 5/2012

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

A LA INSTITUCIÓN DE MEDIACIÓN DE [NOMBRE DE LA INSTITUCIÓN DE MEDIACIÓN]

D. [NOMBRE Y APELLIDOS], mayor de edad, con DNI [DNI/NIE], y domiciliado en [DOMICILIO], C.P., calle [CALLE], núm. [Nº], piso [PISO], letra [LETRA], dirección electrónica [CORREO ELECTRÓNICO], y teléfono [TELÉFONO], en su propio nombre,

EXPONE

Que solicito la iniciación del procedimiento de mediación ante esa Institución, respecto de Dª [NOMBRE Y APELLIDOS], mayor de edad, con DNI [DNI/NIE], y domiciliado en [DOMICILIO], C.P., calle [CALLE], núm. [Nº], piso [PISO], letra [LETRA], dirección electrónica [CORREO ELECTRÓNICO], y teléfono [TELÉFONO], a fin de solucionar la controversia que se expone a continuación en relación a la división del inmueble que fue ganancial sito en [LOCALIDAD], el cual debía ser dividido por mitad en la forma en que convinieran las partes en plazo de seis meses, según los términos del acuerdo de liquidación de la sociedad de gananciales que se acompaña.

Que en la cláusula [Nº DE CLÁUSULA] del citado acuerdo, ambas partes pactaron que, de no llegarse a un acuerdo en la división del inmueble, y antes de instar el proceso judicial, someterían las controversias que pudieran plantearse en la ejecución a la mediación de la institución a la que me dirijo, por lo que, en virtud de lo dispuesto en el art. 16.1.b) de la Ley 5/2012 insto por medio de la presente la iniciación del procedimiento, haciendo constar expresamente que no se ha acudido a la vía judicial por esta parte ni tampoco he recibido comunicación alguna de haber sido demandado por la contraparte.

La controversia que se ha planteado entre las partes deriva de indivisibilidad del inmueble y del hecho de que las ofertas recibidas por el mismo son muy superiores a las que realiza la otra parte, quien pretende la adquisición del inmueble a un precio muy inferior al de tasación.

Que de conformidad con lo dispuesto en el art. 16 de la Ley 5/2012 esta parte acepta las prescripciones de procedimiento recogidas en los estatutos de la institución.

En virtud de lo expuesto,

SOLICITO DE LA INSTITUCIÓN, que tenga por formulada la presente y en su virtud, proceda a la iniciación del procedimiento de mediación, designando mediador y continuando el procedimiento conforme a las reglas de la institución, y a fin de resolver la controversia que dejo expuesta.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma del solicitante

========================================================================
