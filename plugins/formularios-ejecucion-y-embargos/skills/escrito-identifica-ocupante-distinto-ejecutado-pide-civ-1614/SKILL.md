---
name: escrito-identifica-ocupante-distinto-ejecutado-pide-civ-1614
description: "Escrito que identifica a un ocupante distinto del ejecutado y pide declarar que no puede permanecer. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito que identifica a un ocupante distinto del ejecutado y pide declarar que no puede permanecer

> Formulario **CIV-1614** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Escrito del ejecutante hipotecario indicando la existencia y la identidad de la persona que ocupa la finca apremiada en ejecución hipotecaria, la cual no es tercer poseedor que se haya acreditado frente a la ejecutante, y solicitando que se declare por el tribunal, antes de anunciarse la subasta, que no tiene derecho a permanecer en la finca.

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito que identifica a un ocupante distinto del ejecutado y pide declarar que no puede permanecer» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito que identifica a un ocupante distinto del ejecutado y pide declarar que no puede permanecer” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:escrito-identifica-ocupante-distinto-ejecutado-pide-civ-1614`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] NÚMERO (2 veces)
- [ ] AÑO
- [ ] DATOS REGISTRALES
- [ ] FECHA
- [ ] FOLIO
- [ ] LUGAR
- [ ] NOMBRE DE LA PARTE
- [ ] Nº
- [ ] SEDE
- [ ] TOMO

## Normas que cita el formulario

- art. 661.2 LEC
- art. 675.3 LEC
- art. 691.4 LEC

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

Notas al pie del formulario original:
(1) El art. 661 LEC prevé una notificación al ocupante de inmueble apremiado, que puede producirse a instancias de ejecutante, y de una solicitud de éste para que se declare que carece de derecho a ocupar, una vez enajenado el inmueble en la ejecución. Parece que, si es el ejecutante quien entera al Tribunal ejecutor de la existencia e identidad de un ocupante, no se limitará a pedir la notificación a éste para que presente su título, que en definitiva, nada le beneficiará de cara a la subasta, sino como en el modelo, pedirá la declaración judicial mediante convocatoria de vista, que absorbe el plazo para presentar el título del ocupante.

========================================================================


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

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales y de la [NOMBRE DE LA PARTE], cuyos datos constan en los autos de Ejecución de título extrajudicial nº [Nº]/[AÑO], en la misma comparezco y como mejor en Derecho proceda, DIGO:

PRIMERO.-Mi representado/a es ejecutante de la finca hipotecada del demandado D./Dña. [NOMBRE Y APELLIDOS], nº [NÚMERO], al folio [FOLIO], del tomo [TOMO] de [DATOS REGISTRALES], inscrita en el Registro de la Propiedad nº [NÚMERO] de

SEGUNDO.-Mi representado/a tiene conocimiento, por la diligencia de requerimiento judicial de pago, de que el piso propiedad del ejecutado, sito en la finca registral de referencia, se halla en la actualidad ocupado por quien dice llamarse [NOMBRE Y APELLIDOS], y que no es tercer poseedor que se haya acreditado frente a la ejecutante.

TERCERO.-Establece el art. 661.2 LEC que el ejecutante podrá pedir que, antes de anunciarse la subasta, el Tribunal declare que el ocupante u ocupantes no tienen derecho a permanecer en el inmueble, una vez que éste se haya enajenado en la ejecución, petición que se tramitará con arreglo a lo establecido en el art. 675.3 LEC, y a la que deberá accederse cuando los ocupantes puedan considerarse de mero hecho o sin título suficiente. Declaración judicial que se hará constar en el anuncio de la subasta

Todas prevenciones de la subasta de bienes inmuebles, que resultan de aplicación a la subasta de bienes hipotecados, con arreglo al art. 691.4 LEC.

Por lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito, se sirva admitirlo, y en mérito a lo manifestado, notifique a [NOMBRE Y APELLIDOS], con domicilio en la vivienda de la finca ejecutada, la existencia de la ejecución, y seguido que sea el oportuno procedimiento, dicte auto por el que declare que dicho ocupante no tiene derecho a permanecer en el inmueble, una vez que se haya enajenado en la presente ejecución hipotecaria, como se hará constar en el anuncio de la subasta.

Es de Justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a
