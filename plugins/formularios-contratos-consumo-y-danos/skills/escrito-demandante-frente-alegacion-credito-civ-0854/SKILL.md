---
name: escrito-demandante-frente-alegacion-credito-civ-0854
description: "Escrito del demandante frente a la alegación de un crédito compensable por el demandado. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito del demandante frente a la alegación de un crédito compensable por el demandado

> Formulario **CIV-0854** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Escrito dirigido al Tribunal de Instancia por el que el demandante se opone a la alegación del demandado de la existencia de crédito compensable, en un contrato de compraventa mercantil, por ser la devolución de las mercancías improcedente.

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito del demandante frente a la alegación de un crédito compensable por el demandado» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito del demandante frente a la alegación de un crédito compensable por el demandado” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:escrito-demandante-frente-alegacion-credito-civ-0854`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (7 veces)
- [ ] IMPORTE (4 veces)
- [ ] Nº DE DOCUMENTO (4 veces)
- [ ] Nº DE UNIDADES DEVUELTAS (3 veces)
- [ ] BIENES SUMINISTRADOS (2 veces)
- [ ] ACTIVIDAD
- [ ] BIENES QUE SE VENDEN
- [ ] HOJA
- [ ] IMPORTE EN CIFRA
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] NOMBRE DEL SOLICITANTE
- [ ] NOMBRE Y APELLIDOS
- [ ] Nº
- [ ] NÚMERO
- [ ] OBJETO DEL CONTRATO
- [ ] PARTE DEMANDADA
- [ ] SEDE
- [ ] TOMO
- [ ] ÓRGANO

## Normas que cita el formulario

- art. 2 CC
- art. 336 Código de Comercio
- art. 1.196 Código Civil

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS], Procurador de los Tribunales, en nombre de y representación de [NOMBRE DEL REPRESENTADO/A], según tengo acreditado en los autos de juicio declarativo ordinario número [NÚMERO], seguidos en este Tribunal a instancia de [NOMBRE DEL SOLICITANTE] contra [PARTE DEMANDADA], ante el Tribunal comparezco y, como mejor proceda en Derecho, DIGO:

Que por medio del presente escrito, al amparo de lo dispuesto en el artículo 408 de la L.E.C., vengo a contestar a la alegación de compensación de créditos formulada por el demandado, oponiéndome a la misma en base a los siguientes hechos y consideraciones jurídicas:

HECHOS

PRIMERO.- Mi patrocinado, tiene como objeto social [ACTIVIDAD] Se encuentra inscrita en el Registro Mercantil de [LOCALIDAD], hoja [HOJA], tomo [TOMO] y está al corriente en el pago de sus obligaciones fiscales, como se acredita mediante [ÓRGANO] que se acompaña como DOCUMENTO NÚM

La demandada es titular de una cadena de establecimientos comerciales que se dedican a la venta y distribución en el territorio nacional de [BIENES QUE SE VENDEN]

SEGUNDO.- Con fecha [FECHA] firmaron un contrato de compraventa de [OBJETO DEL CONTRATO]

Se acompaña el original del contrato celebrado entre las partes como DOCUMENTO NÚM. [Nº DE DOCUMENTO]

TERCERO.- En cumplimiento del mencionado contrato, mi representado envió una partida de [BIENES SUMINISTRADOS] con fecha [FECHA], por valor de [IMPORTE] euros ([IMPORTE EN CIFRA] €), según se acredita con los albaranes firmados por la demandada y que acompaño como DOCUMENTOS NÚM. [Nº DE DOCUMENTO]

CUARTO.- Versa la presente litis sobre la reclamación que hace mi patrocinado del precio de una partida de [BIENES SUMINISTRADOS], que suministró a la sociedad demandada en fecha [FECHA] El total importe de los envíos efectuados ascendió a [IMPORTE] euros, si bien mi representado aceptó de la compradora, hoy demandada, la devolución de [Nº DE UNIDADES DEVUELTAS] monturas, cuyo importe asciende a [IMPORTE] euros, que deducidas de la deuda pendiente, reducía la petición que se hacía en la demanda a la suma de [IMPORTE] euros.

QUINTO.- El demandado alega en su defensa que a la cantidad de monturas devueltas, hay que añadir otra devolución posterior de [Nº] unidades.

Pero oculta el demandado que la última devolución de las [Nº DE UNIDADES DEVUELTAS] monturas se efectuó en [FECHA], como se acredita con el DOCUMENTO NÚM. [Nº DE DOCUMENTO] que se adjunta, es decir un año después de la entrega inicial.

FUNDAMENTOS DE DERECHO

I.- COMPETENCIA, PROCEDIMIENTO Y LEGITIMACIÓN

Conforme esta parte con los razonamientos señalados por el demandado en cuanto a competencia, procedimiento y legitimación.

II.- COMPENSACIÓN DE DEUDAS

En primer lugar, se rechazan los invocados por la parte contraria, en cuanto resultan inaplicables a la presente cuestión.

En segundo lugar debe quedar establecida la naturaleza jurídica del contrato suscrito, que no es sino la de un contrato de compraventa mercantil, dada la condición de comerciantes de ambos litigantes y la finalidad de las ventas, calificadas como actos de comercio sujetos a las normas de contratación mercantil (artículo 2 CCo).

En consecuencia, debe desestimarse las alegaciones de la parte demandada puesto que se trata de un compraventa mercantil a la que le son de aplicación los arts. 336 y 342 del Código de Comercio y que la última devolución de las [Nº DE UNIDADES DEVUELTAS] monturas se efectuó en [FECHA], como se acredita con el DOCUMENTO NÚM. [Nº DE DOCUMENTO] que se adjunta, es decir un año después de la entrega inicial. Circunstancias éstas que puestas en relación con la necesaria celeridad que exige el tráfico mercantil, y que la legislación especializada sanciona en los artículos citados, cuyos perentorios plazos de reclamación fueron desconocidos por el demandado comprador, conducen a desestimar las oposiciones formuladas, y a dar lugar íntegramente a las peticiones contenidas en la demanda.

La devolución de las monturas de gafas efectuadas por el comprador con fecha [FECHA] no es aceptable, por ser totalmente extemporánea; declaración que necesariamente conduce a que se tenga en cuenta el núm. 4 del art. 1.196 del Código Civil, que exige como requisito indispensable para que proceda la compensación ‘que las dos deudas sean exigibles’. La devolución de los géneros es improcedente, resultando necesario concluir que el demandado no puede exigir el pago del precio de unas devoluciones no aceptadas, ni reconocida su legalidad. Y al no ser exigible una de las deudas que, según el demandado, debía formar parte de la compensación, los efectos de esta no pueden producirse.

III.- COSTAS

Por aplicación del mismo precepto invocado de adverso, procede la imposición de las costas al demandado.

Por todo lo expuesto,

SUPLICO AL TRIBUNAL.

Que tenga por presentado este escrito, en unión de los documentos que adjunto se acompañan, con sus copias, y por contestada la alegación de existencia de crédito compensable formulada por el demandado y previos los trámites legales, se sirva dictar sentencia estimando íntegramente la demanda, con expresa imposición de las costas de la litis a la contraria.

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a

========================================================================
