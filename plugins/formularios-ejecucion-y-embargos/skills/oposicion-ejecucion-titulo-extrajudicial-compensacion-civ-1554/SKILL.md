---
name: oposicion-ejecucion-titulo-extrajudicial-compensacion-civ-1554
description: "Oposición a la ejecución de título extrajudicial por compensación. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Oposición a la ejecución de título extrajudicial por compensación

> Formulario **CIV-1554** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Oposición a la ejecución de título extrajudicial por compensación» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Oposición a la ejecución de título extrajudicial por compensación” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:oposicion-ejecucion-titulo-extrajudicial-compensacion-civ-1554`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (3 veces)
- [ ] Nº DE PROCEDIMIENTO (3 veces)
- [ ] IMPORTE (2 veces)
- [ ] LOCALIDAD
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] NOMBRE Y APELLIDOS
- [ ] Nº
- [ ] SEDE
- [ ] ÓRGANO JUDICIAL
- [ ] ÓRGANO O PERSONA

## Normas que cita el formulario

- art. 557.1.2 LEC
- art. 557 LEC
- art. 1196 CC
- art. 560 LEC

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

- Junto a «…DIMIENTO] A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

PROCEDIMIENTO DE EJECUCIÓN [Nº DE PROCEDIMIENTO]

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

D. [NOMBRE Y APELLIDOS] Procurador de los Tribunales, en nombre y representación de [NOMBRE DEL REPRESENTADO/A], parte ejecutada en el procedimiento de ejecución arriba referenciado,según acredito mediante apoderamiento apud acta otorgado ante el Letrado de la Administración de Justicia de [LOCALIDAD], ante el Tribunal comparezco y como mejor proceda en Derecho DIGO:

Que dentro del plazo legal paso a formular OPOSICIÓN A LA EJECUCIÓN despachada por auto de fecha [FECHA], al amparo de lo dispuesto en el art. 557.1.2ª LEC,con base a los siguientes:

HECHOS

PRIMERO.-La cantidad que se reclama en la demanda en ejecución de póliza de contrato mercantil formulada de contrario [Nº DE PROCEDIMIENTO] y que asciende a la cantidad de [IMPORTE] Euros, se ve compensada por la deuda reconocida en la sentencia dictada por el Tribunal [ÓRGANO JUDICIAL] de fecha [FECHA] dimanante del procedimiento declarativo [Nº DE PROCEDIMIENTO] instado por el ejecutado y objeto de notificación al mismo en fecha [FECHA] frente al ejecutante y que asciende a la cantidad de [IMPORTE] Euros, importe superior al reclamado en la presente litis, se aporta testimonio de la sentencia aludida como DOCUMENTO NÚM. 1.

A los anteriores hechos le son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

PRIMERO.- PROCEDIMIENTO. Son de aplicación los artículos 557, 560 y 561 LEC, debiendo suspenderse la ejecución conforme dispone el apartado 2 del citado art. 557 LEC.

SEGUNDO.- LEGITIMACIÓN. Artículo 538 LEC al ser parte ejecutada en el pre-sente proceso de ejecución.

TERCERO.- OPOSICIÓN A LA EJECUCIÓN. Artículo 557.1.2ª LEC, que establece como causa de oposición a la ejecución fundada en títulos no judiciales ni arbitrales la compensación de crédito líquido que resulte de documento que tenga fuerza ejecutiva. Por su parte, el artículo 1196 CC establece los requisitos de necesaria concurrencia para que opere la compensación concurriendo todos y cada uno al caso concreto: 1. Que cada uno de los obligados lo esté principalmente y sea a la vez acreedor del otro. 2. Que ambas deudas consistan en una cantidad de dinero. 3. Que las dos deudas estén vencidas. 4. Que sean líquidas y exigibles. 5. Que sobre ninguna de ellas haya retención o contienda promovida por terceras personas y notificada oportunamente al deudor.

CUARTO.- COSTAS. Artículo 561.2 de la LEC debiendo imponerse al ejecutante.

Por lo expuesto,

SUPLICO AL TRIBUNAL: Tenga por presentado este escrito con los documentos adjuntos y sus copias, se sirva admitirlos y unirlos a los autos, teniendo por formulada OPOSICIÓN A LA DEMANDA EJECUTIVA formulada por [ÓRGANO O PERSONA] contra mi principal, dictándose por el Letrado de la Administración de Justicia diligencia de ordenación en la que se acuerde la inmediata suspensión de la ejecución despachada y, tras los trámites legales, se acuerde dejar sin efecto la ejecución despachada, mandando el inmediato alzamiento de los embargos acordados y reintegrando a mi mandante en la posición anterior a la ejecución, imponiendo las costas al ejecutante.

OTROSÍ PRIMERO DIGO: de conformidad con el artículo 560 LEC se solicita la celebración de la vista pública a fin de que se realice la prueba que a continuación se detalla:

Se relacionarán los medios de prueba

SUPLICO AL TRIBUNAL: Se proceda a la celebración de la vista pública solicitada al efecto de la práctica de la totalidad de la prueba propuesta, señalándose por el Letrado de la Administración de Justicia día y hora para su celebración.

========================================================================
