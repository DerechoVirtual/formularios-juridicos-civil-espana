---
name: impugnacion-ejecutante-oposicion-motivos-fondo-civ-1561
description: "Impugnación del ejecutante a la oposición por motivos de fondo en ejecución de título judicial. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Impugnación del ejecutante a la oposición por motivos de fondo en ejecución de título judicial

> Formulario **CIV-1561** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Escrito del ejecutante por el que impugna la oposición a la ejecución de título judicial formulada por el ejecutado por motivos de fondo (art. 560 LEC). La impugnación debe formularse en el plazo de cinco días desde que se notifique la resolución sobre los motivos procesales o, en otro caso, desde el traslado del escrito de oposición, y en ella puede solicitarse la celebración de vista (art. 560, párrafo segundo, LEC). El modelo desarrolla, como ejemplo, la oposición del ejecutado basada en la caducidad de la acción ejecutiva respecto de una sentencia anterior a la LEC de 2000.

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Impugnación del ejecutante a la oposición por motivos de fondo en ejecución de título judicial» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Impugnación del ejecutante a la oposición por motivos de fondo en ejecución de título judicial” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:impugnacion-ejecutante-oposicion-motivos-fondo-civ-1561`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] AÑO
- [ ] DÍA
- [ ] FECHA
- [ ] LOCALIDAD
- [ ] MES
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] NOMBRE Y APELLIDOS O DENOMINACIÓN SOCIAL DEL EJECUTANTE
- [ ] Nº
- [ ] Nº DE PROCEDIMIENTO
- [ ] RELACIÓN DE MEDIOS DE PRUEBA
- [ ] SEDE

## Normas que cita el formulario

- art. 560 LEC
- art. 518 LEC
- art. 1964 Código Civil

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

- Junto a «…n autos, de quince años conforme a lo dispuesto en el art. 1964 del Código Civil»: el art. 1964 CC fue modificado por la Ley 42/2015, que redujo a cinco años el plazo de las acciones personales sin plazo especial, con régimen transitorio en la DT 5ª del Código Civil; comprobar el plazo aplicable al caso concreto

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

PROCESO DE EJECUCIÓN [Nº DE PROCEDIMIENTO]

SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

AL TRIBUNAL

Don/Doña [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales y de [NOMBRE Y APELLIDOS O DENOMINACIÓN SOCIAL DEL EJECUTANTE], según tengo acreditado en los autos arriba expresados, ante el Tribunal comparezco y DIGO:

Que, evacuando el traslado conferido, y de conformidad con lo dispuesto en el art. 560 de la LEC, IMPUGNO la oposición a la ejecución deducida de contrario, ello en base a los siguientes

HECHOS

PRIMERO.- Se niega la concurrencia de caducidad en el caso de autos, por cuanto la sentencia objeto de esta ejecución fue dictada en fecha [FECHA], es decir, con anterioridad a la vigencia de la Ley de Enjuiciamiento Civil de 2000, de tal manera que no es de aplicación el plazo de caducidad del art. 518 de la LEC, por cuanto dicho precepto no tiene carácter retroactivo.

Así se ha entendido de forma uniforme por la jurisprudencia de las Audiencias Provinciales, citándose en apoyo de nuestra tesis interpretativa el AAP de Santa Cruz de Tenerife, de 8 de noviembre de 2004, rec. 379/2004; el AAP de Castellón, Sección 2ª, de 9 de diciembre de 2004, rec. 145/2004; y el AAP de Asturias, Sección 1ª, de 11 de febrero de 2005, rec. 716/2003, que señalan pacíficamente que el plazo de caducidad de cinco años establecido en el art. 518 de la LEC no es aplicable a las sentencias dictadas antes de la entrada en vigor de la misma, bajo la vigencia de la LEC de 1881. Por tanto, es de aplicación en este caso el plazo de prescripción genérico para las acciones personales, que es la que se ejercitó en autos, de quince años conforme a lo dispuesto en el art. 1964 del Código Civil , siendo obvio que la acción ejecutiva se ha ejercitado dentro del precitado plazo.

[ADAPTAR ESTE HECHO A LOS MOTIVOS DE OPOSICIÓN QUE EL EJECUTADO HAYA ALEGADO EN SU ESCRITO]

A los anteriores hechos le son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

1. PROCEDIMIENTO. Artículo 560 LEC.

2. IMPUGNACIÓN DE LA OPOSICIÓN. Artículos 2 y 1964 del Código Civil y disposición final vigésima primera de la LEC.

3. COSTAS. Artículo 561.1.1ª LEC, imponiéndose al ejecutado debido a su mala fe y temeridad.

Por lo expuesto,

SUPLICO AL TRIBUNAL: Tenga por presentado este escrito, con justificante de traslado a la parte contraria, se sirva admitirlo, teniendo por formulada, en tiempo y forma, impugnación a la oposición formulada de contrario, acordando desestimarla y mandar seguir la ejecución adelante, con imposición de costas al ejecutado.

[OPCIONAL — incluir si se solicita vista] OTROSÍ DIGO: Que, conforme al párrafo segundo del artículo 560 LEC, se solicita la celebración de vista para la práctica de la prueba que se propone: [RELACIÓN DE MEDIOS DE PRUEBA].

[LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma de Abogado/a y de Procurador/a.
