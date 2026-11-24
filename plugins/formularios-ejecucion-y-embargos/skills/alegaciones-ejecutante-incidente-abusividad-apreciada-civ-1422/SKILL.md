---
name: alegaciones-ejecutante-incidente-abusividad-apreciada-civ-1422
description: "Alegaciones del ejecutante en el incidente de abusividad apreciada de oficio. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Alegaciones del ejecutante en el incidente de abusividad apreciada de oficio

> Formulario **CIV-1422** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Alegaciones del ejecutante en el incidente de abusividad apreciada de oficio» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Alegaciones del ejecutante en el incidente de abusividad apreciada de oficio” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:alegaciones-ejecutante-incidente-abusividad-apreciada-civ-1422`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº DE CLÁUSULA (2 veces)
- [ ] PORCENTAJE (2 veces)
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] NOMBRE Y APELLIDOS
- [ ] NÚMERO
- [ ] SEDE

## Normas que cita el formulario

- art. 552.1 LEC
- art. 20 Ley 16/2011

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

Sección Civil del Tribunal de Instancia núm.de [SEDE]

Proceso de ejecución

AL TRIBUNAL

D. [NOMBRE Y APELLIDOS], Procurador de los Tribunales y de [NOMBRE DEL REPRESENTADO/A], según tengo acreditado en los autos arriba expresados, ante el Tribunal comparezco y DIGO:

Que, evacuando el traslado conferido sobre posible abusividad de las cláusulas [Nº DE CLÁUSULA] y [Nº DE CLÁUSULA] del título ejecutivo, y de conformidad a lo dispuesto en el art. 552.1 de la LEC, mediante el presente escrito me opongo a la declaración de abusividad, en base a los siguientes

HECHOS Y FUNDAMENTOS

PRIMERO.- La primera de las cláusulas recogida en la providencia, que establece los intereses remuneratorios al [PORCENTAJE] %, carece del carácter de abusiva, puesto que fue negociada individualmente con la entidad ejecutada y sigue los parámetros usuales en cuanto al precio del dinero en el momento en que se celebró el contrato. En este punto, es reiterada la jurisprudencia que expresa que para apreciar el carácter abusivo de una cláusula contractual se debe atender, además de a la naturaleza de los bienes o servicios objeto de contrato y a las circunstancias que concurren en el momento de su celebración, a las demás cláusulas del contrato y a los parámetros contenidos en las normas de derecho interno en relación con situaciones similares a la que se plantea; asimismo, en cuanto a las cláusulas de intereses remuneratorios, con carácter general se considera que dichos intereses forman parte del precio, de forma que las cláusulas no pueden declararse abusivas, debiendo limitarse el examen judicial al control de transparencia, siendo que en este caso la ejecutada negoció individualmente la cláusula y fue informada detalladamente del contenido del contrato.

Por este motivo, no existe abusividad, por lo que nos oponemos a la declaración de nulidad.

SEGUNDO.- La segunda de las cláusulas referida en la providencia es la de intereses moratorios pactada en el número [NÚMERO] del título ejecutivo que fija un interés moratorio del [PORCENTAJE] %.

Tampoco esta cláusula puede entenderse como abusiva, puesto que este interés es equivalente a dos veces y media el interés legal actual, lo que en modo alguno supone un grave desequilibrio para el consumidor, es proporcionado y se ajusta plenamente a los parámetros legales manejados en la materia como son los del artículo 20 de la Ley 16/2011, de 24 de junio, de contratos de crédito al consumo, y del artículo 114.III de la Ley Hipotecaria, en su redacción por Ley 5/2019, de 15 marzo, de contratos de crédito inmobiliario.

Por tanto, nos oponemos asimismo a que se declare la abusividad de esta cláusula.

Por lo expuesto,

SUPLICO AL TRIBUNAL: Tenga por presentado este escrito, con justificante de traslado a la parte contraria, se sirva admitirlo, teniendo por formuladas las presentes alegaciones en tiempo y forma, y en virtud de lo expuesto acuerde despachar ejecución en los términos interesados en nuestra demanda.

Lugar y fecha

Firma abogado y procurador.

========================================================================
