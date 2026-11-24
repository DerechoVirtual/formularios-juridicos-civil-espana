---
name: alegaciones-ejecutado-tasacion-pericial-aportando-civ-1532
description: "Alegaciones del ejecutado a la tasación pericial aportando dictamen contradictorio. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Alegaciones del ejecutado a la tasación pericial aportando dictamen contradictorio

> Formulario **CIV-1532** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Escrito de alegaciones a la valoración pericial efectuada en el procedimiento de ejecución, solicitando se aprecie el informe que se acompaña y se dicte resolución en la que determine la valoración definitiva de los bienes a efectos de la ejecución.

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Alegaciones del ejecutado a la tasación pericial aportando dictamen contradictorio» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Alegaciones del ejecutado a la tasación pericial aportando dictamen contradictorio” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:alegaciones-ejecutado-tasacion-pericial-aportando-civ-1532`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] IMPORTE (3 veces)
- [ ] SEDE (3 veces)
- [ ] AÑO
- [ ] LUGAR Y FECHA
- [ ] Nº
- [ ] Nº DE PROCEDIMIENTO

## Normas que cita el formulario

- art. 639 LEC
- art. 639.4 LEC
- art. 639.3 LEC

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
- Junto a «…Don [NOMBRE Y APELLIDOS] ante el Tribunal de Instancia de [SEDE], plaza n.º [Nº]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. «De los de» es residuo de los varios juzgados de una plaza. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

Don [NOMBRE Y APELLIDOS], Procurador de los Tribunales, actuando en nombre y representación de Don [NOMBRE Y APELLIDOS], según tengo debidamente acreditado en los Autos de procedimiento de ejecución núm. [Nº DE PROCEDIMIENTO] del año [AÑO] seguidos ante este Tribunal a instancia de Don [NOMBRE Y APELLIDOS] y contra mi principal, y bajo la dirección Letrada de Don [NOMBRE Y APELLIDOS] ante el Tribunal de Instancia de [SEDE], plaza n.º [Nº] comparezco y, como mejor proceda en Derecho, DIGO:

Que por medio del presente escrito y en la representación que ostento formulo OPOSICIÓN A LA TASACIÓN REALIZADA POR EL PERITO JUDICIAL, al amparo de lo dispuesto en el artículo 639.4 de la Ley de Enjuiciamiento civil, y dentro de los cinco días desde que el perito ha entregado la valoración de los bienes, pasando a realizar las siguientes

ALEGACIONES

PRIMERA.- Que la valoración del bien embargado efectuada por el perito no es ajustada a derecho al no haberse realizado por su precio de mercado, tal como prescribe el apartado tres del artículo 639 de la LEC.

Tal como se constata del contenido del dictamen, no se ha realizado la valoración del bien embargado por el precio de mercado, puesto que se está valorando el bien con métodos de valoración previstos en la legislación para las expropiaciones o actuaciones urbanísticas, cuando es taxativo el mandato del art. 639 de la LEC en el sentido de que la valoración del bien ha de realizarse por el precio de mercado.

Para desvirtuar el dictamen practicado por el perito designado judicialmente, y conforme autoriza el art. 639.4 de la LEC, acompaño como Documento núm. Uno informe suscrito por el perito tasador D. [NOMBRE Y APELLIDOS], en el que se expresa la valoración económica del bien objeto de avalúo, en función exclusivamente del precio de mercado del inmueble, resultando un importe de [IMPORTE] euros, que solicitamos que se fije como valoración definitiva a efectos de ejecución.

SEGUNDA.- Asimismo, nos oponemos al valor tasado por el perito designado judicialmente, por cuanto, tratándose de bienes inmuebles, la valoración económica ha de realizarse sin tener en cuenta las cargas y gravámenes que pesan sobre ellos, tal como expresamente dispone el art. 639.3 de la LEC.

Dicha prescripción resulta infringida en la valoración final del dictamen, por cuanto se reducen las cargas y gravámenes que pesan sobre el inmueble, lo cual no debe realizarse en el dictamen según dispone el art. 639.3 de la LEC, sin perjuicio de lo dispuesto en el art. 666.

Por tanto, solicitamos que se determine como valoración definitiva el importe de [IMPORTE] euros, que es el que resulta acreditado conforme a las alegaciones realizadas por esta parte.

Por lo expuesto,

SUPLICO al Letrado de la Administración de Justicia del órgano al que me dirijo que habiendo presentado en tiempo el presente escrito con los documentos acompañados y con justificante de traslado a la otra parte, lo admita, tenga por realizadas las manifestaciones vertidas en el cuerpo del presente escrito, por formulada OPOSICIÓN A LA TASACIÓN REALIZADA POR EL PERITO JUDICIAL, y previos los trámites legales, dicte decreto determinando la valoración definitiva a efectos de ejecución, fijando la cantidad de [IMPORTE] euros.

Es justicia que pido en [LUGAR Y FECHA]

========================================================================
