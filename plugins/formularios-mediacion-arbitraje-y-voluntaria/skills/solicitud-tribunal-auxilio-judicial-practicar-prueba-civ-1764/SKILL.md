---
name: solicitud-tribunal-auxilio-judicial-practicar-prueba-civ-1764
description: "Solicitud al tribunal de auxilio judicial para practicar prueba en un arbitraje. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud al tribunal de auxilio judicial para practicar prueba en un arbitraje

> Formulario **CIV-1764** del plugin **Mediación, MASC, arbitraje y jurisdicción voluntaria** (`formularios-mediacion-arbitraje-y-voluntaria`) · Civil › Jurisdicción voluntaria, MASC, mediación y arbitraje · normativa revisada el 24-11-2026.

## Qué es

Escrito deduciendo petición de asistencia judicial a la práctica de prueba en el procedimiento arbitral, con pluralidad de árbitros.

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud al tribunal de auxilio judicial para practicar prueba en un arbitraje» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud al tribunal de auxilio judicial para practicar prueba en un arbitraje” para mi caso». También puedes invocarla directamente con `/formularios-mediacion-arbitraje-y-voluntaria:solicitud-tribunal-auxilio-judicial-practicar-prueba-civ-1764`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-mediacion-arbitraje-y-voluntaria:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Mediación, MASC, arbitraje y jurisdicción voluntaria) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] MEDIO DE PRUEBA (2 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] Nº DE PROCEDIMIENTO (2 veces)
- [ ] AÑO
- [ ] DESCRIBIR
- [ ] DÍA
- [ ] FECHA
- [ ] LUGAR
- [ ] MES
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] NOMBRE Y APELLIDOS DEL ABOGADO
- [ ] SEDE

## Normas que cita el formulario

- art. 364.2 LEC
- art. 85.1 LOPJ
- art. 364 LEC

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

D. [NOMBRE Y APELLIDOS] Procurador de los Tribunales, actuando en representación de [NOMBRE DEL REPRESENTADO/A] según se acredita mediante copia electrónica del poder notarial de representación informática (o digitalizada) que se acompaña y se solicita sea devuelta una vez testimoniada (o en virtud de apoderamiento apud acta que se otorgará ante la Secretaría de ese Tribunal), ante el Tribunal comparezco y como mejor proceda en derecho, DIGO:

Que, al amparo de lo dispuesto en el artículo 33 de la Ley de Arbitraje, por medio del presente escrito solicito ASISTENCIA JUDICIAL para la práctica de la prueba [MEDIO DE PRUEBA] en el procedimiento arbitral número [Nº DE PROCEDIMIENTO] en base a los siguientes

HECHOS

Que mi representado es parte [ELEGIR: demandante / demandada] en el procedimiento arbitral número [Nº DE PROCEDIMIENTO] seguido ante la Corte Arbitral de [LOCALIDAD], en cuya tramitación propuso prueba consistente en [DESCRIBIR], la cual fue admitida por resolución de los árbitros de fecha [FECHA], en la cual se autorizaba a esta parte para solicitar la asistencia judicial necesaria para llevarla a cabo (acompaño como documentos [Nº DE DOCUMENTO], copia de los particulares del procedimiento arbitral referidos a la constitución del arbitraje, proposición y admisión de prueba).

La citada prueba admitida no puede ser llevada a cabo de propia autoridad por los árbitros, atendida su naturaleza y dado que la prueba debe practicarse en el domicilio del testigo por enfermedad, motivo por el cual se insta la asistencia judicial en la práctica de la prueba [MEDIO DE PRUEBA] (contenido de la práctica de la prueba que se solicita…), solicitando del tribunal que practique por sí la prueba de acuerdo con los interrogatorios escritos previos aportados por esta parte y la contraria en el procedimiento arbitral que se acompañan a este escrito, conforme autoriza el artículo 364.2 de la LEC (acompaño como documentos [Nº DE DOCUMENTO] certificación de los interrogatorios de preguntas).

FUNDAMENTOS DE DERECHO

Competencia.- Le corresponde a los Tribunales de Instancia de esta ciudad al ser los del lugar en que se ha de prestar la asistencia (artículo 8.2 Ley Arbitraje, en relación con lo dispuesto en el art. 85.1º LOPJ).

Requisitos. Se dan los requisitos del artículo 33 de la Ley de Arbitraje para la asistencia judicial por haberse acordado la admisión de la prueba en el procedimiento arbitral, haber aprobado los árbitros la asistencia judicial y ser necesaria dicha asistencia del órgano jurisdiccional para que la prueba pueda practicarse.

Procedimiento.- Son de aplicación las reglas específicas de los medios de prueba cuya práctica se interesa, operando en cuanto a la declaración domiciliaria del testigo lo establecido en el art. 364 LEC.

En base a lo anterior,

SUPLICO AL TRIBUNAL que tenga por presentado este escrito y documentos adjuntos al mismos y por comparecido al Procurador D. [NOMBRE Y APELLIDOS], en representación de D. [NOMBRE Y APELLIDOS] y en base a lo en él señalado se tenga a bien proceder a la práctica de la prueba testifical de D. a verificar en su domicilio sito en [LOCALIDAD] conforme a los interrogatorios de preguntas que acompaño, bajo la exclusiva dirección del Tribunal, solicitando desde este momento la entrega a esta representación del testimonio de las actuaciones llevadas a cabo.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma Abogado [NOMBRE Y APELLIDOS DEL ABOGADO] Firma Procurador

========================================================================
