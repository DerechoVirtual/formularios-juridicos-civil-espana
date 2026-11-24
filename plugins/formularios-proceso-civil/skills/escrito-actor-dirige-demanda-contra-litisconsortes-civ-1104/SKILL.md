---
name: escrito-actor-dirige-demanda-contra-litisconsortes-civ-1104
description: "Escrito del actor que dirige la demanda contra los litisconsortes señalados por el demandado. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito del actor que dirige la demanda contra los litisconsortes señalados por el demandado

> Formulario **CIV-1104** del plugin **Proceso civil: demandas, contestaciones, prueba y vista** (`formularios-proceso-civil`) · Civil › Escritos procesales (demanda, contestación, prueba, vista) · normativa revisada el 24-11-2026.

## Qué es

Escrito al Tribunal por el que el actor de un juicio declarativo ordinario, al amparo de lo previsto en el art. 420 LEC, y habiéndose alegado por el demandado en su contestación falta del debido litisconsorcio, dirige la demanda a los sujetos que el demandado considera que deben ser litisconsortes.

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito del actor que dirige la demanda contra los litisconsortes señalados por el demandado» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito del actor que dirige la demanda contra los litisconsortes señalados por el demandado” para mi caso». También puedes invocarla directamente con `/formularios-proceso-civil:escrito-actor-dirige-demanda-contra-litisconsortes-civ-1104`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-proceso-civil:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Proceso civil: demandas, contestaciones, prueba y vista) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] EXPONER EL MOTIVO (3 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] FECHA
- [ ] FUNDAMENTOS
- [ ] IMPORTE EN CIFRA
- [ ] LUGAR
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] NOMBRE DEL SOLICITANTE
- [ ] Nº
- [ ] NÚMERO
- [ ] PARTE DEMANDADA
- [ ] TIPO DE PROCEDIMIENTO

## Normas que cita el formulario

- art. 420 LEC
- art. 265.2 LEC
- art. 9.2 LOPJ
- art. 85.1 LOPJ
- art. 36 LEC
- art. 44 LEC
- art. 45 LEC
- art. 249 LEC
- art. 12 LEC
- art. 253 LEC
- art. 23 LEC
- art. 394 LEC

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

AL TRIBUNAL

D./Dña. [NOMBRE Y APELLIDOS], Procurador /a. de los Tribunales, en nombre de y representación de [NOMBRE DEL REPRESENTADO/A], según tengo acreditado en los autos de juicio declarativo ordinario número [NÚMERO], seguidos en este Tribunal a instancia de [NOMBRE DEL SOLICITANTE] contra [PARTE DEMANDADA], ante el Tribunal comparezco y, como mejor proceda en Derecho, DIGO:

Que al amparo de lo previsto en el art. 420 LEC, y habiéndose alegado por el demandado en su contestación falta del debido litisconsorcio, por medio de este escrito dirijo la demanda a [NOMBRE Y APELLIDOS], petición que justifico en base en los siguientes hechos y fundamentos jurídicos:

HECHOS

PRIMERO.- [EXPONER EL MOTIVO]
SEGUNDO.- [EXPONER EL MOTIVO]
TERCERO.- [EXPONER EL MOTIVO]
Como fundamento de los anteriores hechos se adjuntan a la presente demanda los siguientes DOCUMENTOS:

A) Con relación al HECHO PRIMERO, se adjunta como DOCUMENTO NÚM. [Nº DE DOCUMENTO]
B) En relación al HECHO SEGUNDO, se adjunta como DOCUMENTO NÚM. [Nº DE DOCUMENTO]
C) No teniendo a mi disposición el documento a que se hace referencia en el HECHO TERCERO, y de conformidad con el art. 265.2 LEC designo el protocolo del Notario

A los anteriores hechos, son aplicables los siguientes

FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN Y COMPETENCIA

A) JURISDICCIÓN

POTESTAD JURISDICCIONAL.- La potestad jurisdiccional se ejerce por los Jueces y Tribunales determinados por las leyes, según las normas de competencia y procedimiento que las mismas establezcan (art. 117.3 CE)

JURISDICCIÓN CIVIL.- Los Tribunales y Jueces del orden civil conocerán, además de las materias que les son propias, de todas aquellas que no estén atribuidas a otro orden jurisdiccional (art. 9.2 LOPJ).

Los Tribunales de Instancia conocerán en el orden civil, en primera instancia, de los juicios que no vengan atribuidos por esta ley a otros Tribunales (art. 85.1 LOPJ).

LÍMITES DE LA JURISDICCIÓN.- La extensión y límites de la jurisdicción de los Tribunales civiles españoles se determinará por lo dispuesto en la LOPJ y en los tratados y convenios internacionales en los que España sea parte (art. 36 LEC).

B) COMPETENCIA

PREDETERMINACIÓN LEGAL DE LA COMPETENCIA.- Para que los Tribunales civiles tengan competencia en cada caso se requiere que el conocimiento del pleito les esté atribuido por normas con rango de ley y anteriores a la incoación de las actuaciones de que se trate (art. 44 LEC).

COMPETENCIA OBJETIVA. TRIBUNALES DE INSTANCIA, SECCIÓN CIVIL.- Corresponde a dichos órganos jurisdiccionales, el conocimiento en primera instancia, de todos los asuntos civiles que por disposición legal expresa no se hallen atribuidos a otros Tribunales. Conocerán, asimismo, dichos Tribunales de los asuntos, actos, cuestiones y recursos que les atribuye la LOPJ (art. 45 LEC).

COMPETENCIA TERRITORIAL.-

[ELEGIR UNA OPCIÓN: SI EXISTE REGLA IMPERATIVA DE ATRIBUCIÓN DE COMPETENCIA.- / SI NO ES DE APLICACIÓN NINGUNA REGLA IMPERATIVA DE ATRIBUCIÓN DE COMPETENCIA Y EXISTE PACTO DE SUMISIÓN.- / SI NO EXISTE REGLA IMPERATIVA DE ATRIBUCIÓN DE COMPETENCIA NI PACTO DE SUMISIÓN.-]

II- [TIPO DE PROCEDIMIENTO]. PROCEDIMIENTO

Conforme a [Nº] del art. 249 LEC el procedimiento ajustado a derecho será el del juicio declarativo ordinario regulado en los arts. 399 a 436 de la misma Ley.

III.- CAPACIDAD Y REPRESENTACIÓN

IV.- LITISCONSORCIO

De acuerdo con el art. 12 LEC, cuando por razón de lo que sea objeto del juicio la tutela jurisdiccional solicitada sólo pueda hacerse efectiva frente a varios sujetos conjuntamente considerados, todos ellos habrán de ser demandados, como litisconsortes, salvo que la ley disponga expresamente otra cosa.

De acuerdo con el art. 420 LEC del mismo cuerpo legal, cuando el demandado haya alegado en la contestación falta del debido litisconsorcio, podrá el actor, en la audiencia, presentar escrito dirigiendo la demanda a los sujetos que el demandado considere que deben ser sus litisconsortes.

Declarado procedente el litisconsorcio, el Tribunal deberá ordenar el emplazamiento de los nuevos demandados para que contesten a la demanda, con suspensión de la audiencia.

V.- CUANTÍA

Conforme al art. 253 LEC cifro la cuantía de la presente demanda en [IMPORTE EN CIFRA], fijación que amparo en el siguiente fundamento [FUNDAMENTOS]

VI.- POSTULACIÓN Y DEFENSA

Conforme a lo previsto en los arts. 23 y 31 LEC, se presenta la demanda por medio de Procurador /a. legalmente habilitado y bajo dirección de Letrado firmante de la misma.

VII.- FONDO DE LA CUESTIÓN CONTROVERTIDA

VIII.- COSTAS

Conforme al art. 394 LEC, las costas han de imponerse a los demandados.

Por todo lo expuesto,

SUPLICO AL TRIBUNAL.

Tenga por presentado este escrito con las copias correspondientes, lo admita y declare procedente el litisconsorcio, ordenando emplazar a los nuevos demandados para que contesten a la demanda, con suspensión de la audiencia, dictándose en su día sentencia condenatoria contra los mismos, en los términos solicitados en la demanda, imponiéndoles asimismo las costas de esta instancia.

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a

========================================================================
