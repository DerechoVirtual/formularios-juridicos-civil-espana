---
name: oposicion-ejecucion-resolucion-judicial-motivos-fondo-civ-1563
description: "Oposición a la ejecución de resolución judicial por motivos de fondo (pago). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Oposición a la ejecución de resolución judicial por motivos de fondo (pago)

> Formulario **CIV-1563** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Escrito de oposición a la ejecución de una resolución judicial por motivos de fondo (arts. 556 y siguientes LEC), en el supuesto de pago o dación en pago acreditados documentalmente. La oposición suspende el curso de la ejecución conforme al art. 557.1 LEC y permite solicitar vista.

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Oposición a la ejecución de resolución judicial por motivos de fondo (pago)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Oposición a la ejecución de resolución judicial por motivos de fondo (pago)” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:oposicion-ejecucion-resolucion-judicial-motivos-fondo-civ-1563`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (3 veces)
- [ ] FECHA (2 veces)
- [ ] Nº (2 veces)
- [ ] AÑO
- [ ] DÍA
- [ ] EJECUTADO
- [ ] EJECUTANTE
- [ ] LOCALIDAD
- [ ] MES
- [ ] NOMBRE Y APELLIDOS
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] NOMBRE Y APELLIDOS O DENOMINACIÓN SOCIAL DEL EJECUTADO
- [ ] Nº DE PROCEDIMIENTO
- [ ] RELACIÓN DE BIENES
- [ ] RELACIÓN DE LOS MEDIOS DE PRUEBA
- [ ] SEDE

## Normas que cita el formulario

- art. 557.1 LEC
- art. 560 LEC
- art. 7.2 Ley 10/2012

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

- Junto a «…DIMIENTO] A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

PROCEDIMIENTO EJECUTIVO [Nº DE PROCEDIMIENTO]

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

Don/Doña [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, en nombre y representación de [NOMBRE Y APELLIDOS O DENOMINACIÓN SOCIAL DEL EJECUTADO], parte ejecutada en el procedimiento de ejecución arriba referenciado, según acredito mediante copia electrónica del poder notarial de representación (o digitalizada) que acompaño y cuya devolución solicito, previo testimonio en autos, ante el Tribunal comparezco y como mejor proceda en Derecho, DIGO:

Que dentro del plazo legal paso a formular la presente OPOSICIÓN A LA EJECUCIÓN despachada por auto de fecha [FECHA] por motivos de fondo, con base en los siguientes

HECHOS

PRIMERO.- El ejecutado Don/Doña [NOMBRE Y APELLIDOS] suscribió póliza de crédito en cuenta corriente, en virtud de la cual podía disponer como cantidad máxima mensual la cantidad de [IMPORTE] euros, estipulándose, asimismo, que tanto los intereses deudores como acreedores se liquidarían al cumplirse cada período de liquidación, siendo adeudados respectivamente en dicha cuenta. Se aporta como DOCUMENTO NÚM. 1 la referida póliza.

SEGUNDO.- Se nos dice de contrario que con fecha [FECHA], al realizarse la liquidación de intereses, resultó que el demandado no procedió a abonar, conforme a lo pactado, su importe en la citada cuenta corriente, procediéndose al vencimiento anticipado de la póliza, presentando un saldo deudor de [IMPORTE] euros.

TERCERO.- Lo cierto es que al vencimiento del plazo el ejecutado le entregó los siguientes bienes muebles de su propiedad: [RELACIÓN DE BIENES], acordándose en acta notarial que se aporta como DOCUMENTO NÚM. 2 que los mismos se entregaban en concepto de liquidación de la cantidad debida en todos los conceptos en virtud de la suscripción con la entidad financiera ejecutante de dicha póliza de crédito en cuenta corriente.

CUARTO.- De lo expuesto se deduce que ha existido un pago documentado que extingue cualquier deuda del ejecutado con el ejecutante.

A los anteriores hechos le son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

1. PROCEDIMIENTO. Artículos 556, 557, 560 y 561 LEC, con suspensión del curso de la ejecución de conformidad con el artículo 557.1 LEC.

2. LEGITIMACIÓN. Artículo 556 LEC, al ser el ejecutado parte en el proceso de ejecución.

3. OPOSICIÓN A LA EJECUCIÓN. Pago. Artículo 557.1.1ª LEC en relación con los artículos 1156 y siguientes, 1145 y siguientes y 1281 y siguientes del Código Civil. La dación en pago es considerada jurisprudencialmente, entre otras, STS de 14 de julio de 1997, rec. 2257/1993, como un negocio jurídico cuya regulación ha de adecuarse analógicamente a las normas de la compraventa, por lo que el deudor transmite al acreedor unos bienes con la finalidad de pago.

4. COSTAS. Deben imponerse al ejecutante, de conformidad con lo dispuesto en los artículos 539.2 y 561.2 LEC.

Por lo expuesto,

SUPLICO AL TRIBUNAL: Tenga por presentado este escrito, documentos y copias, se sirva admitirlo, unirlo a autos, teniendo por formalizada, en tiempo y forma, oposición a la demanda ejecutiva instada por [EJECUTANTE] contra [EJECUTADO] y, previa su sustanciación, con suspensión de la ejecución, se estime dicha oposición y se dicte auto declarando que no procede la ejecución, con imposición de costas al ejecutante.

[OPCIONAL — si ha lugar]

OTROSÍ PRIMERO DIGO: de conformidad con el artículo 560 LEC se solicita la celebración de la vista pública a fin de que se realice la prueba que a continuación se detalla: [RELACIÓN DE LOS MEDIOS DE PRUEBA].

SUPLICO AL TRIBUNAL: Se proceda a la celebración de la vista pública solicitada al efecto de la práctica de la totalidad de la prueba propuesta.

[OPCIONAL — incluir si el ejecutado es persona jurídica no exenta de tasa]

OTROSÍ SEGUNDO DIGO: Que estando el presente escrito sujeto al abono de la tasa por el ejercicio de la potestad jurisdiccional fijada por la Ley 10/2012, de 20 de noviembre, y desarrollada por Orden HAP/2662/2012, de 13 de diciembre, siendo mi representada persona jurídica no exenta de su pago, se acompaña como documento nº [Nº] la correspondiente autoliquidación con el ejemplar para la Administración de Justicia debidamente validado y en el que consta el pago de la cantidad de [IMPORTE] euros correspondiente a la cuota fija [OPCIONAL — si ha lugar: con la bonificación del 10% por la utilización de medios telemáticos], sin que se incluya la cuota variable prevista en el artículo 7.2 de la Ley 10/2012 al haber sido declarado inconstitucional y nulo por la STC 140/2016, de 21 de julio.

En virtud de lo anterior,

SUPLICO AL TRIBUNAL que tenga por hecha la anterior manifestación a los efectos pertinentes y por acompañado el documento justificativo del abono de la tasa.

[LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma de Abogado/a y de Procurador/a.
