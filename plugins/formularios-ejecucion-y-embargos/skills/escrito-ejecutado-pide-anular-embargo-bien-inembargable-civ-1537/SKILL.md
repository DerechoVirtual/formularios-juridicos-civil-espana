---
name: escrito-ejecutado-pide-anular-embargo-bien-inembargable-civ-1537
description: "Escrito del ejecutado que pide anular el embargo de un bien inembargable. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito del ejecutado que pide anular el embargo de un bien inembargable

> Formulario **CIV-1537** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito del ejecutado que pide anular el embargo de un bien inembargable» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito del ejecutado que pide anular el embargo de un bien inembargable” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:escrito-ejecutado-pide-anular-embargo-bien-inembargable-civ-1537`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (9 veces)
- [ ] Nº (6 veces)
- [ ] MARCA/MODELO (3 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] SEDE (3 veces)
- [ ] ENTIDAD BANCARIA (2 veces)
- [ ] AÑO
- [ ] LUGAR Y FECHA
- [ ] NOMBRE DE LA EDITORIAL
- [ ] NOMBRE DEL PERIÓDICO
- [ ] Nº DE DOCUMENTO
- [ ] Nº DE PROCEDIMIENTO
- [ ] PERÍODO

## Normas que cita el formulario

- art. 606.2 LEC

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º LOS DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…IDOS], ante la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. «De los de» es residuo de los varios juzgados de una plaza. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º LOS DE [SEDE]

Don [NOMBRE Y APELLIDOS], Procurador de los Tribunales, actuando en nombre y representación de Don [NOMBRE Y APELLIDOS], como tengo debidamente acreditado en procedimiento de ejecución núm. [Nº DE PROCEDIMIENTO] del año [AÑO], y bajo la dirección Letrada de Don [NOMBRE Y APELLIDOS], ante la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº] comparezco y, como mejor proceda en derecho, DIGO:

Que en la indicada representación y por medio del presente escrito intereso la NULIDAD DEL EMBARGO TRABADO SOBRE UN BIEN INEMBARGABLE, al amparo de lo dispuesto en el artículo 606.2 de la Ley de Enjuiciamiento Civil, en base a las siguientes

ALEGACIONES

PRIMERA.- BIENES INEMBARGABLES.

Que a fin y efecto de garantizar un mínimo vital al embargado y a su familia el artículo 606.2 LEC, contempla como bienes inembargables pertenecientes exclusivamente al ejecutado los instrumentos que sean necesarios para el ejercicio de su profesión, cuando su valor no guarde proporción con el importe de la deuda reclamada.

SEGUNDA.- PROFESIÓN DE MI PRINCIPAL.

Mi principal ejerce la profesión de periodista por cuenta propia y la de escritor.

En relación con la profesión de periodista por cuenta propia colabora diariamente con el periódico [NOMBRE DEL PERIÓDICO] de tirada nacional, por lo que recibe una retribución mensual de [IMPORTE] euros.

En prueba de lo manifestado acompaño certificado de historia laboral, como Documento núm. [Nº], y certificado de bases de Bases de Cotización de Regímenes especiales [PERÍODO], como Documento núm. [Nº], expedidos por la Tesorería General de la Seguridad Social.

Igualmente acompaño certificado de la entidad financiera [ENTIDAD BANCARIA], como Documento núm. [Nº], en virtud del cual queda acreditado que mensualmente mi mandante cobra a través de la citada entidad las facturas que expide por las colaboraciones que diariamente realiza en el periódico antes citado. Así mismo acompaño las facturas expedidas en los últimos doce meses como Documentos núms. a [Nº DE DOCUMENTO].

En relación con la profesión de escritor significar que viene publicando con una periodicidad casi anual un libro de novela, habiéndose comprometido con la editorial [NOMBRE DE LA EDITORIAL] a publicar tres novelas en los próximos cinco años, habiendo percibido en concepto de adelanto la cantidad de [IMPORTE] euros. En prueba de lo manifestado acompaño documento acreditativo del citado compromiso, como Documento núm. [Nº], así como certificado de la entidad financiera [ENTIDAD BANCARIA], como Documento núm. [Nº], en virtud del cual queda acreditado el importe percibido por el concepto de adelanto antes referido.

TERCERA.- BIENES EMBARGADOS.

Los bienes que se han embargado a mi principal en su condición de ejecutado son un ordenador portátil marca [MARCA/MODELO] con un valor venal de [IMPORTE] euros, un ordenador de sobremesa marca [MARCA/MODELO], con un valor venal de [IMPORTE] euros, una impresora marca [MARCA/MODELO], con un valor venal de [IMPORTE] euros, el mobiliario de su estudio consiente en una mesa de trabajo, tres sillas, dos estanterías, todo ello con un valor venal de [IMPORTE] euros, así como los libros que le sirven de documentación para sus novelas y colaboraciones en el periódico antes mencionado, con un valor aproximado de [IMPORTE] euros.

CUARTA.- VALOR INSTRUMENTOS NECESARIOS PARA EL EJERCICIO DE LA PROFESIÓN.

Los bienes embargados son de naturaleza mueble que directamente y de forma indispensable son necesarios para el desempeño de su profesión, y su valor total que asciende a [IMPORTE] euros no guarda proporción con la cuantía de la deuda reclamada que es de [IMPORTE] euros, por lo que al amparo de lo dispuesto en el artículo 606.2 LEC han de quedar exentos del embargo.

Por lo que

AL TRIBUNAL SUPLICO: Que tenga por presentado este escrito con los documentos acompañados (en su caso, y sus copias), lo admita, por realizadas las manifestaciones vertidas en el cuerpo del presente escrito, y previos los trámites con arreglo a derecho resuelva decretar la NULIDAD DEL EMBARGO TRABADO sobre los bienes relacionados en la alegación tercera, por ser todos ellos de naturaleza mueble, por ser directamente y de forma indispensable necesarios para el desempeño de la profesión de mi mandante y por no guardar proporción con la cuantía de la deuda reclamada, todo ello al amparo del artículo 606.2 LEC la finalidad del cual es garantizar un mínimo vital al embargado y a su familia, con expresa declaración de mala fe y condena en costas, dando a los autos el impulso procesal con arreglo a derecho.

Es Justicia que insto en [LUGAR Y FECHA].

Firmas de Letrado y Procurador.

========================================================================
