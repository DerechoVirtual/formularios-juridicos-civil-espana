---
name: solicitud-propuesta-liquidacion-regimen-matrimonial-civ-0245
description: "Solicitud y propuesta de liquidación del régimen matrimonial por un cónyuge (Derecho foral aragonés). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud y propuesta de liquidación del régimen matrimonial por un cónyuge (Derecho foral aragonés)

> Formulario **CIV-0245** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud y propuesta de liquidación del régimen matrimonial por un cónyuge (Derecho foral aragonés)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud y propuesta de liquidación del régimen matrimonial por un cónyuge (Derecho foral aragonés)” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:solicitud-propuesta-liquidacion-regimen-matrimonial-civ-0245`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (20 veces)
- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] AÑO (2 veces)
- [ ] DÍA (2 veces)
- [ ] LUGAR (2 veces)
- [ ] MES (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] SEDE (2 veces)
- [ ] FECHA
- [ ] NOMBRE Y APELLIDOS DEL ABOGADO
- [ ] Nº
- [ ] Nº DE PROCEDIMIENTO
- [ ] OTROS DATOS

## Normas que cita el formulario

- art. 807 LEC
- art. 810.2 LEC

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

- Junto a «…Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Denominación legal: Sección de Familia, Infancia y Capacidad. Si no existe en el partido, conoce la Sección Civil o la Única (art. 86.3-4 LOPJ). Fuente: LOPJ arts. 84.2.a) y 86 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «….3-4 LOPJ). Fuente: LOPJ arts. 84.2.a) y 86 (redacc. LO 1/2025, BOE-A-2025-76).]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

D/Dª [NOMBRE Y APELLIDOS] Procurador de los Tribunales actuando en nombre y representación de D/Dª [NOMBRE Y APELLIDOS], según consta debidamente acreditado en los Autos de Separación contenciosa nº [Nº DE PROCEDIMIENTO], ante el Tribunal comparezco y como mejor proceda en Derecho DIGO:

Que en la representación que ostento, habiendo concluido el inventario y firme la resolución que declara disuelto el régimen de consorcio conyugal, vengo a solicitar LIQUIDACIÓN DEL RÉGIMEN ECONÓMICO MATRIMONIAL existente entre los cónyuges D/Dª [NOMBRE Y APELLIDOS], en base a los siguientes

HECHOS

PRIMERO.- Mi representada y D. formaban matrimonio cuyo régimen económico matrimonial era el de consorcio conyugal.

SEGUNDO.- En fecha [FECHA] se dictó por la Sección Civil/de Familia, Infancia y Capacidad del Tribunal de Instancia de [SEDE], plaza n.º [NÚMERO] sentencia de separación entre ambos, declarándose en la misma la disolución del régimen económico matrimonial y aprobándose el inventario por resolución firme de fecha

TERCERO.- La liquidación que se propone es la siguiente (Reproducir modelo de liquidación).

FUNDAMENTOS DE DERECHO

Competencia

De acuerdo con lo establecido en el artículo 807 LEC se atribuye legalmente al Tribunal de Instancia que hubiere conocido del proceso de separación que determina la disolución del régimen económico matrimonial.

Legitimación

La regulación de los artículos 258 y siguientes del Código de Derecho Foral de Aragón de régimen económico matrimonial y viudedad de Aragón señala como legitimado a cualquier cónyuge o partícipe.

Trámite

Se solicita que una vez firme la resolución definitiva del proceso de separación, acompañando propuesta de liquidación, en el que se expresan los reintegros entre partes y se forman lotes (art 810.2 LEC), siendo el régimen sustantivo del consorcio conyugal aragonés.

Deberá convocarse a las partes para que ante el Sr Letrado de la Administración de Justicia con admonición al adverso de que su injustificada comparecencia se considerará conformidad con lo que se propone (Art 810.4 LEC).

Por lo expuesto,

SUPLICO AL TRIBUNAL: que, teniendo por presentado este escrito con sus copias, se sirva admitirlo, teniendo por solicitada liquidación y división, iniciándose el procedimiento, citando a las partes, con traslado a la parte contraria de la propuesta de liquidación y adjudicación que se contiene en el cuerpo de este escrito, a fin de que se alcance un acuerdo, o en otro caso, se designe contador, y si fuere menester peritos, con advertencia al demandado de que si no comparece se le tendrá por conforme con la indicada propuesta.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma de Abogado y Procurador [NOMBRE Y APELLIDOS DEL ABOGADO]

MODELO DE PROPUESTA DE LIQUIDACIÓN (ARAGÓN)

De acuerdo al inventario aprobado, a cada cónyuge le corresponde la mitad del pasivo, esto es [IMPORTE] Euros y la mitad del pasivo que son [IMPORTE] Euros.

Se propone la siguiente adjudicación:

1. A D [NOMBRE Y APELLIDOS] se le adjudican los siguientes bienes:

El automóvil [IMPORTE] euros

La motocicleta [IMPORTE] euros

Las acciones [IMPORTE] euros

El bar cafetería [IMPORTE] euros - Deudas del negocio [IMPORTE] euros: [IMPORTE] euros

TOTAL [IMPORTE] euros

A Dª se le adjudican los siguientes bienes:

La vivienda [IMPORTE] euros - carga hipotecaria [IMPORTE] euros: [IMPORTE] euros.

El saldo de la cuenta bancaria nº [NÚMERO] de importe de [IMPORTE] euros.

TOTAL [IMPORTE] euros

De acuerdo con lo establecido en la regulación del consorcio conyugal determinando que existe un ACTIVO CONSORCIAL SUPERIOR al PASIVO la liquidación seguirá este orden:

1º.- Compensación de [IMPORTE] euros debidos por la masa común a los patrimonios privativos: En relación con el patrimonio de D. [NOMBRE Y APELLIDOS] en la cantidad de [IMPORTE] Euros y en relación con el patrimonio de Dª. en la cantidad de [IMPORTE] euros.

2º.- Imputación del saldo acreedor favorable a la comunidad en la respectiva participación en el consorcio del cónyuge deudor D. [NOMBRE Y APELLIDOS], hasta agotar su importe, salvo que opte por el reembolso en metálico o acuerde su pago mediante dación de bienes de los patrimonios privativos.

3º.- Pago a terceros de las deudas vencidas en importe de [IMPORTE] euros y aseguramiento de las pendientes con importe de [IMPORTE] euros.

4º.- Reintegro a cada uno de los patrimonios privativos del saldo acreedor resultante de la compensación del número 1, que se cifra, de acuerdo con los cálculos siguientes [OTROS DATOS] en la cantidad de [IMPORTE] Euros.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

========================================================================
