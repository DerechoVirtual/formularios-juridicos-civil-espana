---
name: peticion-complemento-laudo-subsanar-omision-civ-1769
description: "Petición de complemento del laudo para subsanar una omisión. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Petición de complemento del laudo para subsanar una omisión

> Formulario **CIV-1769** del plugin **Mediación, MASC, arbitraje y jurisdicción voluntaria** (`formularios-mediacion-arbitraje-y-voluntaria`) · Civil › Jurisdicción voluntaria, MASC, mediación y arbitraje · normativa revisada el 24-11-2026.

## Qué es

Escrito dirigido a la institución arbitral solicitando el complemento de un laudo (art. 39.1.c de la Ley 60/2003, de Arbitraje) cuando éste ha omitido pronunciarse sobre una petición formulada y no resuelta, en este caso sobre las costas del arbitraje, de pronunciamiento preceptivo (art. 37.6). Debe presentarse en el plazo de diez días desde la notificación del laudo, salvo que las partes hayan pactado otro, y notificarse simultáneamente a la otra parte.

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Petición de complemento del laudo para subsanar una omisión» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Petición de complemento del laudo para subsanar una omisión” para mi caso». También puedes invocarla directamente con `/formularios-mediacion-arbitraje-y-voluntaria:peticion-complemento-laudo-subsanar-omision-civ-1769`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-mediacion-arbitraje-y-voluntaria:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Mediación, MASC, arbitraje y jurisdicción voluntaria) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (6 veces)
- [ ] IMPORTE (3 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] AÑO
- [ ] DÍA
- [ ] MES
- [ ] NOMBRE Y APELLIDOS
- [ ] NOMBRE Y APELLIDOS O DENOMINACIÓN SOCIAL
- [ ] Nº
- [ ] Nº DE FOLIOS
- [ ] Nº DE PROCEDIMIENTO ARBITRAL

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

A LA SECRETARÍA DE LA CORTE ARBITRAL DE [LOCALIDAD]

D./Dª [NOMBRE Y APELLIDOS], en nombre y representación de D./Dª [NOMBRE Y APELLIDOS O DENOMINACIÓN SOCIAL], parte demandante en este procedimiento arbitral seguido con el número [Nº DE PROCEDIMIENTO ARBITRAL], según tengo acreditado en el expediente, comparezco y, como mejor proceda en derecho, DIGO:

1) Que esta parte ha sido notificada en fecha [FECHA] del laudo arbitral de fecha [FECHA] dictado en el presente procedimiento arbitral, cuya parte dispositiva es del siguiente tenor literal: «[PARTE DISPOSITIVA DEL LAUDO: p. ej., Declaro resuelto el contrato de fecha [FECHA], debiendo el demandado indemnizar al actor en la cantidad de [IMPORTE] euros, en concepto de daños y perjuicios, impago de suministros y no renovación del aval bancario, suma que se incrementará en [IMPORTE] euros por cada día que pase desde la firma del presente Laudo hasta el momento en que la parte demandante obtenga la devolución de los bienes objeto del contrato]».

2) Que, entendiendo que se ha producido una omisión en el pronunciamiento del laudo sobre las costas del arbitraje, al amparo de lo dispuesto en el artículo 39.1.c) de la Ley de Arbitraje, por medio del presente escrito solicito COMPLEMENTO del citado laudo arbitral de fecha [FECHA], en base a los siguientes

MOTIVOS

PRIMERO.– Se dan los requisitos establecidos en el artículo 39 de la Ley de Arbitraje para la solicitud de complemento, puesto que la presente solicitud se deduce en el plazo de diez días desde la notificación del laudo en fecha [FECHA], remitiéndose notificación simultánea a la otra parte según consta por el burofax que acompaño como documento número [Nº].

SEGUNDO.– El complemento que se pretende se funda en el carácter preceptivo del pronunciamiento sobre las costas del arbitraje, según establece el artículo 37.6 de la Ley de Arbitraje, habiéndose pactado en el convenio arbitral, obrante en los folios [Nº DE FOLIOS] del procedimiento, que el laudo se pronunciaría sobre las costas del arbitraje, incluyendo los honorarios y gastos de los árbitros, así como los honorarios de los defensores o representantes de las partes y el coste del servicio y gastos del procedimiento.

Por tanto, el pronunciamiento del laudo arbitral sobre estos extremos es preceptivo, de manera que debe ser subsanado como se pretende en esta solicitud.

TERCERO.– Atendido lo anterior, y dado el carácter preceptivo del pronunciamiento sobre costas y gastos, solicitamos que se complemente el laudo, debiendo entenderse lógicamente de la motivación y del sentido de su parte dispositiva que deben imponerse al demandado las costas y gastos del arbitraje, fijando el importe a que ascienden, de [IMPORTE] euros, acreditado en el procedimiento.

Por lo expuesto,

SOLICITO que tenga por presentado este escrito, con justificante de notificación a la otra parte, solicitando complemento del laudo arbitral dictado en fecha [FECHA] en este procedimiento y, en su virtud, adicione al fallo el pronunciamiento sobre costas y gastos del arbitraje, fijando su importe y con imposición al demandado.

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO]

Firma representante: ______________________
