---
name: recurso-reposicion-contra-diligencia-exige-tasa-civ-1281
description: "Recurso de reposición contra la diligencia que exige la tasa judicial por falta de hecho imponible. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Recurso de reposición contra la diligencia que exige la tasa judicial por falta de hecho imponible

> Formulario **CIV-1281** del plugin **Recursos civiles: reposición, apelación, casación y queja** (`formularios-recursos-civiles`) · Civil › Recursos · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **recursos**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Recurso de reposición contra la diligencia que exige la tasa judicial por falta de hecho imponible» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Recurso de reposición contra la diligencia que exige la tasa judicial por falta de hecho imponible” para mi caso». También puedes invocarla directamente con `/formularios-recursos-civiles:recurso-reposicion-contra-diligencia-exige-tasa-civ-1281`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-recursos-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Recursos civiles: reposición, apelación, casación y queja) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] AÑO
- [ ] DÍA
- [ ] LOCALIDAD
- [ ] MES
- [ ] NOMBRE Y APELLIDOS
- [ ] ÓRGANO JUDICIAL

## Normas que cita el formulario

- art. 2 Ley 10/2012
- art. 2.e Ley 10/2012
- art. 3.1 Ley 10/2012
- art. 451 LEC

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

Juicio número [NÚMERO]

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA Nº [NÚMERO] DE [LOCALIDAD]

D. [NOMBRE Y APELLIDOS] Procurador de los Tribunales, actuando en representación de según viene acreditado en los presentes autos, como mejor proceda en derecho por medio de la presente paso a formular recurso de reposición frente a la diligencia de ordenación de fecha [FECHA], la cual fue notificada a esta parte el pasado día, por la que se requiere de subsanación a mi representado para que aporte justificante de pago de la tasa, citando como infringidos los artículos 2 y 3 de la Ley 10/2012, de 20 de noviembre, basándola en las siguientes

ALEGACIONES

PRIMERO.- La diligencia de ordenación impugnada se estima que infringe lo dispuesto en el art. 2.e) de la Ley 10/2012, de 20 de noviembre, por cuanto que el presente recurso está fuera del ámbito del hecho imponible que constituye el pago de la tasa por el ejercicio de la potestad jurisdiccional (en cada caso, se alegaría el supuesto) al interponerse un recurso de apelación contra un auto definitivo y no contra una sentencia.

El artículo 2.e) de la Ley 10/2012 establece que constituye el hecho imponible de la tasa "la interposición de recursos de apelación contra sentencias y de casación en el orden civil y contencioso-administrativo", de manera que no entran en la definición legal del hecho imponible los recursos de apelación interpuestos contra autos, como en el caso ahora contemplado.

La falta de inclusión del supuesto de hecho en el ámbito del hecho imponible de la tasa, determina que mi representado en modo alguno pueda considerarse como sujeto pasivo conforme al artículo 3.1 de la citada Ley 10/2012, por cuanto que no ha realizado el hecho imponible definido en el artículo 2 de la misma Ley.

La diligencia de ordenación recurrida se limita a requerir de subsanación para presentación del modelo de autoliquidación, sin más razonamiento, cuando lo cierto es que la interposición del presente recurso queda fuera del ámbito del hecho imponible, habiéndose cumplido por lo demás el requisito de constitución de depósito establecido en la disposición adicional decimoquinta de la LOPJ.

Es por ello que con fundamento en los arts. 451 y 452 LEC formulo el presente recurso de reposición, interesando que se revoque la citada resolución y en su lugar se acuerde continuar con la tramitación del recurso de apelación interpuesto.

En base a lo anterior,

SUPLICO que tenga por presentado este escrito, teniendo por interpuesto recurso de reposición frente a la diligencia de ordenación dictada el día [FECHA] por el Letrado de la Administración de Justicia del Tribunal [ÓRGANO JUDICIAL], solicitando que, tras la tramitación pertinente se deje la misma sin efecto, acordando en su lugar la admisión del recurso interpuesto por esta representación, continuando su tramitación por el cauce prevenido legalmente.

En, a [DÍA] de [MES] de [AÑO]

Firma Abogado y Procurador

========================================================================
