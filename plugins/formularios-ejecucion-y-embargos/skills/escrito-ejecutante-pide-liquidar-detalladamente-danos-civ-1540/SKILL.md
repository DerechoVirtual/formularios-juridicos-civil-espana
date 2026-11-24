---
name: escrito-ejecutante-pide-liquidar-detalladamente-danos-civ-1540
description: "Escrito del ejecutante que pide liquidar detalladamente daños y perjuicios (arts. 713 y ss. LEC). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito del ejecutante que pide liquidar detalladamente daños y perjuicios (arts. 713 y ss. LEC)

> Formulario **CIV-1540** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Escrito solicitando la liquidación de los daños y perjuicios sufridos, conforme a los artículos 713 y siguientes de la LEC.

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito del ejecutante que pide liquidar detalladamente daños y perjuicios (arts. 713 y ss. LEC)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito del ejecutante que pide liquidar detalladamente daños y perjuicios (arts. 713 y ss. LEC)” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:escrito-ejecutante-pide-liquidar-detalladamente-danos-civ-1540`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] IMPORTE (4 veces)
- [ ] SEDE (3 veces)
- [ ] FECHA (2 veces)
- [ ] Nº (2 veces)
- [ ] AÑO
- [ ] LUGAR Y FECHA
- [ ] Nº DE DOCUMENTO
- [ ] OBLIGACIÓN CONTRACTUAL

## Normas que cita el formulario

- art. 713 LEC

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
- Junto a «…on [NOMBRE Y APELLIDOS], ante el Tribunal de Instancia de [SEDE], plaza n.º [Nº]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. «De los de» es residuo de los varios juzgados de una plaza. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

Don [NOMBRE Y APELLIDOS], Procurador de los Tribunales y de Don [NOMBRE Y APELLIDOS], según tengo acreditado en el procedimiento de ejecución de condena dineraria núm. [Nº] del año [AÑO], seguido contra Don [NOMBRE Y APELLIDOS], y bajo la dirección Letrada de Don [NOMBRE Y APELLIDOS], ante el Tribunal de Instancia de [SEDE], plaza n.º [Nº] comparezco y, como mejor proceda en Derecho, DIGO:

Que habiendo resultado condenado Don [NOMBRE Y APELLIDOS] en virtud de la Sentencia firme de fecha [FECHA] que constituye el título que se ejecuta en el presente procedimiento de ejecución, al pago de los daños y perjuicios causados a mi principal por el incumplimiento en tiempo y forma de la prestación a la que venía obligado el ejecutado y debiendo determinarse en la presente ejecución la cantidad que por tales conceptos debe satisfacer la contraparte, se está en el caso de proceder en la forma prevista en el artículo 713 de la LEC.

Que a estos efectos, como quedó acreditado en la sentencia, la negativa de la demandada a cumplir con el contrato de fecha [FECHA], que le obligaba a [OBLIGACIÓN CONTRACTUAL], ha provocado que mi mandante, que ya tenía concertados una multitud de contratos de compraventa con sus clientes, no haya podido atenderlos, por lo que le ha perjudicado gravemente su reputación y provocado unas pérdidas que ascienden al importe de [IMPORTE] euros, dado que en los referidos contratos se estipuló en la cláusula 5ª una penalización para el caso de que no se entregase la mercancía en la fecha estipulada.

Que en prueba de la manifestado acompañamos dictamen realizado por el auditor de cuentas Don [NOMBRE Y APELLIDOS], como Documento núm. [Nº DE DOCUMENTO] que analiza toda la documentación relativa a los contratos de mi representado, que obran, además, en autos, y que acreditan la pérdida sufrida, que asciende a la cantidad de [IMPORTE] euros, constando en dicho informe la relación detallada de los daños y perjuicios a que se refiere el artículo 713 LEC.

Que en concepto de lucro cesante se reclama la cantidad de [IMPORTE] euros, tal como se analiza y cuantifica en el dictamen acompañado, al dejar de percibir el ejecutante el margen de beneficio que se aplica en la venta de estos productos.

Que en todo caso las citadas cantidades habrán de ser incrementadas en el interés legal del dinero, lo que totaliza la suma de [IMPORTE] euros, que es la que se propone como valor total de los daños y perjuicios irrigados por la conducta incumplidora del ejecutado.

En su virtud,

AL TRIBUNAL SUPLICO: Que teniendo por presentado este escrito junto con los documentos acompañados (en su caso, y copia de todo), haya por interesada la determinación judicial de los daños y perjuicios a los que resultó condenada la parte ejecutada en la resolución judicial que constituye el título ejecutivo, y admitida que sea se confiera traslado a la parte ejecutada para que en el plazo de diez días conteste lo que estime conveniente, y seguido el trámite en la forma prevista en el artículo 714 y siguientes de la Ley de Enjuiciamiento Civil, dicte en su día Auto por el que fije la cantidad determinada en el importe señalado en la relación acompañada al presente escrito.

Es justicia que insto en [LUGAR Y FECHA].

Firmas de Letrado y Procurador.

========================================================================
