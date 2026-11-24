---
name: escrito-solicitud-ejecucion-provisional-sentencia-civ-1445
description: "Escrito de solicitud de ejecución provisional de sentencia. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito de solicitud de ejecución provisional de sentencia

> Formulario **CIV-1445** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito de solicitud de ejecución provisional de sentencia» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito de solicitud de ejecución provisional de sentencia” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:escrito-solicitud-ejecucion-provisional-sentencia-civ-1445`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (19 veces)
- [ ] IMPORTE (4 veces)
- [ ] FECHA (3 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] Nº DE COLEGIADO (2 veces)
- [ ] TIPO DE PROCEDIMIENTO (2 veces)
- [ ] DÍA
- [ ] MES
- [ ] Nº DE COLEGIADO/A
- [ ] Nº DE PROCEDIMIENTO
- [ ] RÉGIMEN DE VISITAS

## Normas que cita el formulario

- art. 526 LEC
- art. 774.4 LEC
- art. 524.2 LEC
- art. 61 LEC
- art. 90 Código Civil
- art. 524 LEC

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA NÚMERO DE [LOCALIDAD]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA NÚMERO DE [LOCALIDAD]

Don/doña [NOMBRE Y APELLIDOS], Procurador de los Tribunales con número de colegiado [Nº DE COLEGIADO/A] y de don/doña [NOMBRE Y APELLIDOS], según tengo acreditado en los autos de [TIPO DE PROCEDIMIENTO], seguidos con el número [Nº DE PROCEDIMIENTO], como mejor proceda en derecho, ante el Tribunal comparezco y, DIGO:

Que de conformidad con lo dispuesto en el artículo 525.1.1 de la Ley de Enjuiciamiento Civil, solicito la ejecución provisional de determinados pronunciamientos de la sentencia de [FECHA] (nulidad, separación, divorcio), basándome en los siguientes hechos y fundamentos de derecho.

HECHOS

PRIMERO Con fecha [FECHA] se dictó sentencia en los autos de [TIPO DE PROCEDIMIENTO] seguidos en este Tribunal a instancia de doña [NOMBRE Y APELLIDOS] contra don [NOMBRE Y APELLIDOS], en cuyo fallo, se acuerda entre otros los siguientes pronunciamientos complementarios:

A) Que en concepto de levantamiento de las cargas familiares don [NOMBRE Y APELLIDOS] deberá entregar a doña [NOMBRE Y APELLIDOS], la cantidad de [IMPORTE] euros mensuales, ingresándola entre el uno al cinco de cada mes, en la cuenta bancaria que designe doña [NOMBRE Y APELLIDOS], actualizándose la citada cantidad anualmente conforme al IPC que publique el Instituto Nacional de Estadística.

B) Conceder a doña [NOMBRE Y APELLIDOS], la guarda y custodia de los hijos menores de edad, estableciendo a favor del padre el siguiente régimen de visitas [RÉGIMEN DE VISITAS]

C) La administración de los bienes gananciales a don [NOMBRE Y APELLIDOS] el cual deberá rendir cuentas de la marcha del negocio ganancial, cuando fuere requerido.

D) Se concede a doña [NOMBRE Y APELLIDOS] una pensión compensatoria de [IMPORTE] euros mensuales que don [NOMBRE Y APELLIDOS], deberá ingresar, antes del día cinco de cada mes, en la cuenta bancaria que designe doña [NOMBRE Y APELLIDOS], actualizándose la citada cantidad anualmente conforme al IPC que publique el Instituto Nacional de Estadística.

SEGUNDO Que la citada sentencia fue apelada por la parte contraria, dictándose providencia admitiéndose la apelación con fecha [FECHA]

TERCERO Que esta parte ofrece constituir aval bancario por la cantidad que estime SSª, aunque entendemos no debe exigirse cantidad alguna en virtud del artículo 526 LECiv.

A estos hechos, son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

I. El artículo 525.1.1 de la Ley de Enjuiciamiento Civil que regula la ejecución provisional de los pronunciamientos que regulen las obligaciones y relaciones patrimoniales relacionadas con lo que sea objeto principal del proceso, en relación con el art. 774.4 y 5 LEC.

II. El artículo 524.2 de la LECiv, que establece que: la ejecución provisional de sentencias de condena, que no sean firmes, se despachará y llevará a cabo, del mismo modo que la ejecución ordinaria, por el tribunal competente para la primera instancia.

III. La competencia para el conocimiento de la ejecución provisional solicitada corresponde al Tribunal que dictó la sentencia de conformidad con el artículo 61 de la LECiv.

IV. El artículo 90 del Código Civil, en cuanto que a la ejecución pueden aplicarse las normas de apremio.

V. Los artículos 524 y siguientes de la LECiv y la jurisprudencia aplicable en orden al procedimiento a seguir en la ejecución de las medidas que se solicitan.

Por todo lo cual,

SUPLICO AL TRIBUNAL: que habiendo por presentado este escrito, por el Procurador que suscribe, debiéndosele tener por parte en la representación que ostenta de Dña. [NOMBRE Y APELLIDOS], se sirva admitirlo, teniendo por instada la ejecución provisional de la sentencia respecto a los pronunciamientos

citados y previo los trámites legales se lleve a cabo la ejecución solicitada sobre los siguientes:

1º Poner bajo la custodia de doña [NOMBRE Y APELLIDOS] los hijos [NOMBRE Y APELLIDOS] y [NOMBRE Y APELLIDOS]

2º Poner a disposición de doña [NOMBRE Y APELLIDOS] y de los hijos citados, la vivienda familiar, procediéndose al desalojo de don [NOMBRE Y APELLIDOS] el cual solamente podrá llevarse consigo sus enseres personales.

3º El pago a doña [NOMBRE Y APELLIDOS] de la pensión compensatoria de [IMPORTE] euros mensuales.

4º El pago de la pensión por alimentos para los hijos citados a razón de [IMPORTE] euros por cada uno de ellos.

Es Justicia que pido en [LOCALIDAD] a [DÍA] de [MES]

Fdo. Letrado

Colegiado/a núm. [Nº DE COLEGIADO]

Fdo. Procurador

Colegiado núm. [Nº DE COLEGIADO]

========================================================================
