---
name: clausula-sumision-arbitraje-contratos-entre-partes-civ-1794
description: "Cláusula de sumisión a arbitraje en los contratos entre las partes. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Cláusula de sumisión a arbitraje en los contratos entre las partes

> Formulario **CIV-1794** del plugin **Mediación, MASC, arbitraje y jurisdicción voluntaria** (`formularios-mediacion-arbitraje-y-voluntaria`) · Civil › Jurisdicción voluntaria, MASC, mediación y arbitraje · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Cláusula de sumisión a arbitraje en los contratos entre las partes» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Cláusula de sumisión a arbitraje en los contratos entre las partes” para mi caso». También puedes invocarla directamente con `/formularios-mediacion-arbitraje-y-voluntaria:clausula-sumision-arbitraje-contratos-entre-partes-civ-1794`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-mediacion-arbitraje-y-voluntaria:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Mediación, MASC, arbitraje y jurisdicción voluntaria) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- El modelo no tiene campos marcados: Claude te preguntará lo que necesite según el caso.

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

Cláusula .- Arbitraje

Cláusula de arbitraje anexa a los contratos suscritos entre las partes para resolución de cualquier discrepancia que pudieran existir entre ellas.

Cláusula .- Arbitraje

Las partes acuerdan someterse al laudo arbitral que en su caso dicte, en arbitraje de [ELEGIR: derecho / equidad], en resolución a cualquier discrepancia que pueda existir entre las partes en la interpretación, ejecución, disolución, liquidación o posible contradicción con otros contratos entre ellas. Este arbitraje se regirá por lo dispuesto en la Ley 60/2003, de 23 de diciembre, de arbitraje, o norma posterior que la sustituya.

El convenio arbitral:

* Puede adoptar alguna de estas formas:
— Acuerdo independiente, o
— Cláusula incorporada a un contrato.

Para esta modalidad se prevén las siguientes reglas especiales:

• Si está contenido en un contrato de adhesión, la validez de dicho convenio y su interpretación se rigen por lo dispuesto en las normas aplicables a ese tipo de contrato.
• Se considera incorporado al acuerdo entre las partes el convenio arbitral que conste en un documento al que éstas se hayan remitido en cualquiera de las formas previstas en el párrafo siguiente.

Se trata de la denominada ‘cláusula arbitral por referencia‘, es decir, la que no consta en el documento contractual principal, sino en un documento separado, pero se entiende incorporada al contenido del primero por la referencia que en él se hace al segundo.

* Debe constar por escrito, en un documento firmado por las partes o en un intercambio de cartas, telegramas, télex, fax u otros medios de telecomunicación que dejen constancia del acuerdo.

Se considera cumplido este requisito cuando el convenio arbitral conste y sea accesible para su ulterior consulta en soporte electrónico, óptico o de otro tipo.

* No obstante lo anterior, se establece la siguiente presunción: se considera que hay convenio arbitral cuando en un intercambio de escritos de demanda y contestación su existencia sea afirmada por una parte y no negada por la otra.
* Si se trata de arbitraje internacional, el convenio arbitral será válido y la controversia será susceptible de arbitraje si:
— cumplen los requisitos establecidos por las normas jurídicas elegidas por las partes para regir el convenio arbitral, o
— por las normas jurídicas aplicables al fondo de la controversia, o
— por el derecho español.

Se opta, por tanto, por una solución inspirada en un principio de conservación o criterio más favorable a la validez del convenio arbitral. De este modo, basta que el convenio arbitral sea válido con arreglo a cualquiera de los tres regímenes jurídicos señalados.

Respecto a las normas han de aplicarse a la resolución del fondo de la controversia, se establecen los siguientes criterios:

1.º) La premisa es la libertad de las partes.

Los árbitros deben:

— decidir con arreglo a las estipulaciones del contrato y además,
— tener en cuenta los usos aplicables.
2.º) Se invierte la regla que la Ley 36/1988 contenía a favor del arbitraje de equidad. En la nueva ley los árbitros sólo deciden en equidad si las partes les han autorizado expresamente para ello.

Para el arbitraje internacional se establecen las siguientes reglas especiales:

* Si las partes indican las normas jurídicas aplicables, los árbitros deben decidir la controversia de conformidad con ellas.

Se entiende que toda indicación del derecho u ordenamiento jurídico de un Estado determinado se refiere, a menos que se exprese lo contrario, al derecho sustantivo de ese Estado y no a sus normas de conflicto de leyes.

* Si las partes no indican las normas jurídicas aplicables, los árbitros deben aplicar las que estimen apropiadas.

También cabe remisión al reglamento o normas de alguna institución arbitral.

========================================================================
