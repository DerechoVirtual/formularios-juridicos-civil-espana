---
name: general-queja-civ-1285
description: "General (queja). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# General (queja)

> Formulario **CIV-1285** del plugin **Recursos civiles: reposición, apelación, casación y queja** (`formularios-recursos-civiles`) · Civil › Recursos · normativa revisada el 24-11-2026.

## Qué es

Escrito por el que se interpone recurso de queja frente a la denegación de la admisión a trámite de recurso de apelación o casación

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «General (queja)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “General (queja)” para mi caso». También puedes invocarla directamente con `/formularios-recursos-civiles:general-queja-civ-1285`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-recursos-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Recursos civiles: reposición, apelación, casación y queja) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (4 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] TIPO DE RECURSO (2 veces)
- [ ] COLEGIO
- [ ] CONTENIDO DE LA RESOLUCIÓN
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] Nº DE COLEGIADO
- [ ] SECCIÓN
- [ ] ÓRGANO O PERSONA

## Normas que cita el formulario

- art. 495.1 LEC

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

[ELEGIR UNA DE LAS ALTERNATIVAS QUE SIGUEN Y SUPRIMIR LAS DEMÁS]

A la Sección [SECCIÓN] de la Audiencia Provincial de [LOCALIDAD]

A la Sala de lo Civil del Tribunal Supremo

A la Sala de lo Civil y Penal del Tribunal Superior de Justicia

D./Doña [NOMBRE Y APELLIDOS], Procurador de los Tribunales, en nombre y representación de D./Doña [NOMBRE Y APELLIDOS], conforme acredito con la copia de escritura de poder que se acompaña al presente escrito, bajo la dirección técnica del Letrado D./Doña [NOMBRE Y APELLIDOS], colegiado num. [Nº DE COLEGIADO] del Ilustre Colegio de Abogados de [COLEGIO], como mejor proceda en Derecho, DIGO:

Que siguiendo expresas instrucciones de mi mandante, por medio del presente escrito me persono en tiempo y forma ante la Sala a la que tengo el honor de dirigirme, e INTERPONGO RECURSO DE QUEJA frente a la denegación de la admisión a trámite del recurso de [TIPO DE RECURSO] formulado por esta parte contra la resolución de fecha [FECHA] dictada por [ÓRGANO O PERSONA], en los autos

El recurso interpuesto se funda en las siguientes:

ALEGACIONES

PRIMERA.- El órgano 'a quo' dictó resolución por la que acordó [CONTENIDO DE LA RESOLUCIÓN], y considerándose dicha resolución desfavorable y perjudicial para los intereses de esta parte, presentó escrito de interposición de recurso de [TIPO DE RECURSO], siendo denegado mediante auto de fecha [FECHA], cuya copia se acompaña al presente, conforme dispone el art. 495.1 LEC, y frente a este auto, dentro del plazo de diez días desde la notificación, se interpone recurso de queja.

SEGUNDA.- El presente recurso de queja se fundamenta en la indebida denegación del recurso intentado por esta parte, basándose en los motivos siguientes:

Por todo lo cual,

SUPLICO A LA SALA, que tenga por presentado este escrito junto con sus copias, teniéndome por personado en nombre de quien comparezco, entendiéndose conmigo las sucesivas diligencia, y por interpuesto en tiempo y forma RECURSO DE QUEJA contra la resolución de fecha [FECHA], en el que, una vez seguidos sus trámites legales, se dicte resolución ordenando al órgano 'a quo' que continúe con la tramitación del recurso indebidamente denegado.

OTROSÍ DIGO, que se acompaña a este escrito resguardo acreditativo del pago del depósito de 30 euros en la Cuenta de Depósitos y Consignaciones del Tribunal al que se dirige, conforme exige la disposición adicional 15.ª LOPJ, por lo que,

SUPLICO AL TRIBUNAL

Que tenga por causada la manifestación anterior a los efectos oportunos.

Por ser de Justicia que pido en [LUGAR], a [FECHA].

Firma de Abogado/a	Firma de Procurador/a

========================================================================
