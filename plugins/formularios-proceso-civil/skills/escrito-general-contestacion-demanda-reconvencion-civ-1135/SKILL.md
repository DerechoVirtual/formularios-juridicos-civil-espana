---
name: escrito-general-contestacion-demanda-reconvencion-civ-1135
description: "Escrito general de contestación a la demanda con reconvención. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito general de contestación a la demanda con reconvención

> Formulario **CIV-1135** del plugin **Proceso civil: demandas, contestaciones, prueba y vista** (`formularios-proceso-civil`) · Civil › Escritos procesales (demanda, contestación, prueba, vista) · normativa revisada el 24-11-2026.

## Qué es

Escrito de contestación a la demanda, oponiéndose a la misma y formulando reconvención, dirigida al Tribunal de Instancia.

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito general de contestación a la demanda con reconvención» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito general de contestación a la demanda con reconvención” para mi caso». También puedes invocarla directamente con `/formularios-proceso-civil:escrito-general-contestacion-demanda-reconvencion-civ-1135`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-proceso-civil:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Proceso civil: demandas, contestaciones, prueba y vista) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] EXPONER EL MOTIVO (3 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] IMPORTE (2 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] FECHA
- [ ] HECHO QUE SE NIEGA
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] MOTIVO
- [ ] NOMBRE DE LA PARTE
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] PETICIÓN
- [ ] PRESTACIÓN DE HACER O NO HACER
- [ ] SEDE
- [ ] ÓRGANO O PERSONA

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

### Avisos de actualización (1) — se aplican en el texto, nunca se copian en el documento

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Notas al pie del formulario original:
(1) El demandado, haciendo uso de lo dispuesto en el artículo 155 de la Ley de Enjuiciamiento Civil, puede indicar un domicilio distinto a aquél en el que ha sido emplazado a los efectos de ser citado en él, y será el que vinculará al órgano judicial a estos efectos. En este caso se expresará en el encabezamiento: "Que para sucesivas comunicaciones con el demandado el domicilio que fija es … "

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

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a. de los Tribunales, en nombre y representación de [NOMBRE DEL REPRESENTADO/A], como acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], dirigido por el Letrado abajo firmante D./Dña. [NOMBRE Y APELLIDOS], con despacho profesional en [LOCALIDAD], ante el Tribunal comparezco y como mejor proceda en Derecho DIGO:

Que dentro del término concedido al efecto contestamos a la demanda y nos oponemos a la misma en base a los hechos y fundamentos de derecho que se expresarán, y al mismo tiempo presentamos demanda reconvencional contra la actora:

1º.- Apoyamos nuestra oposición a la demanda en base a los siguientes:

HECHOS

Negamos los hechos de la demanda en cuanto no se admitan expresamente en los siguientes.

PRIMERO.- De conformidad con el hecho primero de contrario.

SEGUNDO.- De conformidad con el hecho segundo de contrario.

TERCERO.- Se niega expresamente el correlativo de la demanda, en el sentido de que [HECHO QUE SE NIEGA], como se acredita con los documentos números [Nº DE DOCUMENTO] de la contestación a la demanda que se acompañan.

FUNDAMENTOS DE DERECHO

I, II.-

Conforme esta parte con la competencia y el tipo de procedimiento señalados por el actor en el correlativo de la demanda.

III, IV, V.-

De conformidad con los expuestos de contrario.

VI.- POSTULACIÓN Y DEFENSA

La parte esta representada por el Procurador/a. [NOMBRE Y APELLIDOS], legalmente habilitado según el artículo 23 de la L.E.C. y defendida por el Letrado que consta en el encabezamiento, artículo 31 de la L.E.C.

VII.- FUNDAMENTO LEGAL DE LA OPOSICIÓN

Los preceptos invocados por la parte contraria resultan inaplicables por [MOTIVO]

VIII.- COSTAS

Las costas deberán serle impuestas, de conformidad con el artículo 394 de la L.E.C., a la parte actora, de ser desestimada su demanda.

Por lo expuesto,

SUPLICO AL TRIBUNAL.

Que teniendo por presentado este escrito con los documentos y copias que le acompañan, lo admita y tenga por contestada en tiempo y forma la demanda y por opuesto a la misma, y previos los trámites correspondientes, incluso el recibimiento a prueba que desde ahora se solicita, dicte en su día sentencia por la que se desestime la demanda, absolviendo de sus pedimentos al demandado, con expresa imposición de costas a la actora.

2º.- Al propio tiempo esta parte formula demanda de RECONVENCIÓN contra la actora [NOMBRE DE LA PARTE] en solicitud del pronunciamiento que en el suplico se concretará, y que siguiendo las pautas establecidas en el artículo 406 de la Ley de Enjuiciamiento Civil, se basa en los siguientes:

HECHOS

))

PRIMERO.- [EXPONER EL MOTIVO]
SEGUNDO.- [EXPONER EL MOTIVO]
TERCERO.- [EXPONER EL MOTIVO]
FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN Y COMPETENCIA

Es Juez competente para conocer de la demanda reconvencional el que esté conociendo de la demanda principal.

II.- PROCEDIMIENTO

Conforme al artículo 409 de la L.E.C. la reconvención se sustanciará y resolverá al propio tiempo y en la misma forma que la cuestión principal del pleito y será resuelta con éste en la sentencia definitiva.

III.- LEGITIMACIÓN ACTIVA Y PASIVA

Las partes en la cuestión reconvencional son las mismas que en la demanda principal, pero con su papel invertido, esto es, el actor en la principal es aquí el demandado reconvencional, y el demandado es aquí demandante reconvencional.

IV.- CUANTÍA

Conforme al art. 253 de la L.E.C. cifro la cuantía de esta reconvención en [IMPORTE]

V.- POSTULACIÓN Y DEFENSA

Conforme a lo prevenido en los artículos 23 y 31 de la L.E.C. la demanda se formula por medio de escrito con Procurador/a. legalmente habilitado y bajo la dirección de Letrado; requisitos cumplidos por esta parte igualmente al contestar la demanda principal.

VI.- FUNDAMENTO LEGAL DE LA RECONVENCIÓN

VII.- COSTAS

Conforme al artículo 394 de la L.E.C. han de imponerse al demandado reconvencional.

Por lo expuesto,

SUPLICO AL TRIBUNAL.

Que teniendo por presentado este escrito y por formulada en tiempo y forma demanda reconvencional, la admita a trámite y previos los que le correspondan al juicio ordinario en el que se ha presentado, y con recibimiento del pleito a prueba que desde ahora se solicita, dicte sentencia en la que, además de la desestimación de la demanda principal formulada por [ÓRGANO O PERSONA] se estime la presente RECONVENCIÓN, declarando:

A) Se declare que [PETICIÓN]
B) Como consecuencia, se condene al demandado reconvencional a satisfacer a mi parte [IMPORTE] (o en su caso, a hacer o dejar de hacer tal cosa [PRESTACIÓN DE HACER O NO HACER])
C) Todo ello con imposición de las costas al demandado reconvencional.

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado	Firma del Procurador/a
