---
name: recurso-infraccion-procesal-anterior-reforma-rdl-5-2023-civ-1297
description: "Recurso por infracción procesal anterior a la reforma del RDL 5 de 2023. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Recurso por infracción procesal anterior a la reforma del RDL 5 de 2023

> Formulario **CIV-1297** del plugin **Recursos civiles: reposición, apelación, casación y queja** (`formularios-recursos-civiles`) · Civil › Recursos · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **recursos**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Recurso por infracción procesal anterior a la reforma del RDL 5 de 2023» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Recurso por infracción procesal anterior a la reforma del RDL 5 de 2023” para mi caso». También puedes invocarla directamente con `/formularios-recursos-civiles:recurso-infraccion-procesal-anterior-reforma-rdl-5-2023-civ-1297`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-recursos-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Recursos civiles: reposición, apelación, casación y queja) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (6 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] Nº DE MOTIVO (2 veces)
- [ ] AÑO
- [ ] CONTENIDO DE LA RESOLUCIÓN
- [ ] DÍA
- [ ] INFRACCIÓN PROCESAL
- [ ] LUGAR
- [ ] MES
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] NOMBRE Y APELLIDOS
- [ ] NORMA INFRINGIDA
- [ ] Nº
- [ ] OTROS DATOS
- [ ] SEDE
- [ ] TIPO Y Nº DE PROCEDIMIENTO

## Normas que cita el formulario

- art. 477 LEC
- art. 470.1 LEC
- art. 448.2 LEC
- art. 215.5 LEC
- art. 469 LEC
- art. 469.1 LEC
- art. 473.2 LEC

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

- Junto a «…tada el por la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

A LA SECCIÓN DE LA ILMA. AUDIENCIA PROVINCIAL DE PARA ANTE LA SALA DE LO CIVIL DEL TRIBUNAL SUPREMO ( O LA SALA DE LO CIVIL Y PENAL DEL TRIBUNAL SUPERIOR DE JUSTICIA DE)

D. [NOMBRE Y APELLIDOS] Procurador de los Tribunales, actuando en representación de [NOMBRE DEL REPRESENTADO/A] según viene acreditado en los presentes autos, comparezco y como mejor proceda en derecho

DIGO:

PRIMERO: Que en fecha [FECHA] esta parte ha sido notificada de la sentencia de fecha [FECHA] dictada en el Rollo arriba expresado, por la que [CONTENIDO DE LA RESOLUCIÓN] Frente a dicha sentencia se dedujo solicitud de complemento siendo desestimada por auto de fecha [FECHA], notificado en fecha

SEGUNDO: Que entendiendo que dicha sentencia no es ajustada a derecho, dicho sea con los debidos respetos y en términos de defensa, por medio del presente escrito interpongo contra la misma RECURSO POR INFRACCIÓN PROCESAL, en base a las siguientes ALEGACIONES:

I. ADMISIBILIDAD DEL RECURSO

Carácter recurrible de la resolución

El presente recurso se deduce contra la sentencia dictada por la Audiencia Provincial en fecha [FECHA], que desestima el recurso de apelación de esta parte y deja sin efecto determinados pronunciamientos de la sentencia de instancia, la cual es resolución recurrible en infracción procesal sin formular casación, conforme al apartado 2º de la disposición adicional decimosexta de la LEC, al estar comprendida en el apartado 1º ( ó 2º) del artículo 477 de la LEC y produce un evidente gravamen a esta parte.

Cumplimiento del plazo

El presente recurso se interpone dentro del plazo de veinte días establecido en el artículo 470.1 de la LEC, computados conforme al artículo 448.2 de la LEC ( en su caso, en relación con el artículo 215.5 LEC).

Motivo o motivos de recurso y denuncia previa en la instancia

Que la sentencia dictada el [FECHA] por parte de esa Sección de la Audiencia Provincial de [LOCALIDAD] en resolución del recurso de apelación presentado por esta parte ante la sentencia dictada el por la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº] en los autos [TIPO Y Nº DE PROCEDIMIENTO] se estima que incurre en [INFRACCIÓN PROCESAL], lo que implica la posible concurrencia del motivo [Nº DE MOTIVO] del art 469,1 de la LEC en relación con el artículo, habiendo solicitado esta parte oportunamente la subsanación, según consta en [OTROS DATOS].

II. MOTIVOS DEL RECURSO

(Se desarrollarían los motivos anunciados dentro de los contemplados en el artículo 469.1 de la LEC..) Al amparo del motivo [Nº DE MOTIVO] del art. 469.1 de la LEC, por infracción de [NORMA INFRINGIDA] (se expondrían las alegaciones..)

()

De acuerdo a las infracciones denunciadas, entendemos que procede anular la resolución recurrida y ordenar que se repongan las actuaciones al momento del falta, conforme al art. 473.2 de la LEC.

En base a lo anterior,

SUPLICO A LA SALA: Que tenga por presentado este escrito con la certificación del traslado previo a las demás partes teniendo por interpuesto recurso extraordinario por infracción procesal frente a la sentencia dictada por esa Sección de la Ilma. Audiencia Provincial de [LOCALIDAD] de fecha [FECHA] y tras la pertinente tramitación y remisión de las actuaciones al Tribunal Supremo (o en su caso, al Tribunal Superior de Justicia de), se dicte por éste esta sentencia en la que declarando haber lugar al recurso por infracción procesal presentado se anule la sentencia en su momento dictada ordenando que la Audiencia Provincial proceda a dictar una nueva sentencia.

OTROSÍ PRIMERO DIGO que, de conformidad con lo dispuesto en los apartados 3.c) y 6 de la disposición adicional decimoquinta de la LOPJ acompaño a este escrito resguardo de consignación en la cuenta de Depósitos y Consignaciones abierta a nombre del Tribunal del depósito exigido para interponer el recurso por importe de 50 euros.

Por lo que, SUPLICO A LA SALA que tenga por constituido el depósito, dejando interesada desde este momento su devolución para el caso de estimación total o parcial del recurso.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma Abogado/Firma Procurador

========================================================================
