---
name: impugnacion-jura-cuentas-abogado-partidas-indebidas-civ-0754
description: "Impugnación de la jura de cuentas del abogado por partidas indebidas. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Impugnación de la jura de cuentas del abogado por partidas indebidas

> Formulario **CIV-0754** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Impugnación de la jura de cuentas del abogado por partidas indebidas» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Impugnación de la jura de cuentas del abogado por partidas indebidas” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:impugnacion-jura-cuentas-abogado-partidas-indebidas-civ-0754`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] IMPORTE (2 veces)
- [ ] SEDE (2 veces)
- [ ] AÑO
- [ ] DÍA
- [ ] FECHA
- [ ] LUGAR
- [ ] MES
- [ ] Nº DE DOCUMENTO

## Normas que cita el formulario

- art. 35 LEC
- art. 1967 Código Civil
- art. 34.2 LEC
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

Procedimiento de jura de cuentas número

AL LETRADO DE LA ADMINISTRACIÓN DE JUSTICIA DE [SEDE]

D. [NOMBRE Y APELLIDOS] Procurador de los Tribunales obrando en nombre y representación del demandado D [NOMBRE Y APELLIDOS] según acredito mediante designación apud-acta otorgada ante el Letrado de la Administración de Justicia de [SEDE], en el procedimiento de jura de cuentas núm. comparezco y como mejor proceda en derecho DIGO:

Que, mediante el presente escrito, y al amparo de lo previsto en el artículo 35 de la LEC, formulo impugnación a la jura de cuentas presentada por el Letrado D./Dña. [NOMBRE Y APELLIDOS] por INDEBIDAS en base a los siguientes

HECHOS

PRIMERO.- Mediante resolución de fecha [FECHA], por ese Tribunal se requirió a mi representado el pago de la cantidad de [IMPORTE] euros a la que asciende la minuta de honorarios presentada por el Letrado D./Dñ [NOMBRE Y APELLIDOS] que actuó en su defensa en el proceso núm

SEGUNDO.- Se impugna la minuta por cuanto que la misma incluye honorarios indebidos, puesto que los mismos fueron satisfechos por mi representado con anterioridad al inicio del proceso al haber hecho entrega al Letrado de una provisión de fondos por importe de [IMPORTE] euros, según acredito por los documentos [Nº DE DOCUMENTO] que acompaño, la cual cubre sobradamente la totalidad de los honorarios ahora reclamados, sin que se haga referencia alguna a la misma en el escrito del Abogado y sin que exista otra relación contractual con mi representado que pueda justificar la percepción de dicho importe.

TERCERO.- Se impugna asimismo la minuta presentada por cuanto han transcurrido más de tres años desde que finalizó el proceso por sentencia firme, de manera que se ha producido la prescripción de la acción para reclamar el pago de los honorarios, conforme a lo dispuesto en el artículo 1967 del Código Civil, sin que se haya producido acto alguno interruptivo de la prescripción.

CUARTO.- Subsidiariamente, esta parte se opone a la minuta de honorarios de referencia por cuanto incluye conceptos que se entienden indebidos y ello por cuanto se trata de actuaciones innecesarias y que no fueron autorizadas por esta parte, por lo que su pago no ha de ser a mi cargo. Las partidas impugnadas son:

()

A los anteriores hechos son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

PRIMERO.- Se acepta la competencia del Letrado de la Administración de Justicia al que me dirijo.

SEGUNDO.- En cuanto al procedimiento, es de aplicación lo dispuesto en el artículo 35 de la LEC en relación con los párrafos segundo y tercero del artículo 34.2 de la LEC, al impugnarse los honorarios por indebidos.

TERCERO.- En cuanto a la oposición, son procedentes los motivos alegados por esta parte, admitiéndose la posibilidad de excepcionar el pago, la prescripción conforme al artículo 1967 del Código Civil, y el hecho de no haberse devengado en el pleito los honorarios (STS 19 de junio de 2008, rec. 610/2001).

CUARTO.- En cuanto a las costas, es de aplicación lo dispuesto en el artículo 35 en relación con el artículo 394 de la LEC.

Por lo que,

SUPLICO que se tenga por presentado este escrito con sus copias, con justificante de traslado, y previos los trámites legales establecidos, se dicte decreto considerando como indebidos los honorarios incluidos en la minuta presentada por el Letrado D [NOMBRE Y APELLIDOS], con imposición de costas al citado Letrado.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma Abogado y Procurador

========================================================================
