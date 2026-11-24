---
name: demanda-divorcio-conyuge-consentimiento-otro-convenio-civ-0101
description: "Demanda de divorcio de un cónyuge con el consentimiento del otro y convenio regulador. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de divorcio de un cónyuge con el consentimiento del otro y convenio regulador

> Formulario **CIV-0101** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de divorcio de un cónyuge con el consentimiento del otro y convenio regulador» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de divorcio de un cónyuge con el consentimiento del otro y convenio regulador” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-divorcio-conyuge-consentimiento-otro-convenio-civ-0101`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (9 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] Nº DE DOCUMENTO (4 veces)
- [ ] Nº DE COLEGIADO (2 veces)
- [ ] CALLE
- [ ] DÍA
- [ ] EDAD
- [ ] FECHA
- [ ] MES
- [ ] Nº
- [ ] Nº DE HIJOS
- [ ] RÉGIMEN ECONÓMICO
- [ ] SEDE
- [ ] TIPO DE MATRIMONIO (CIVIL / CANÓNICO)
- [ ] TOMO
- [ ] ÓRGANO

## Normas que cita el formulario

- art. 86 Código Civil
- art. 769 LEC
- art. 777 LEC
- art. 81 Código Civil

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

### Avisos de actualización (3) — se aplican en el texto, nunca se copian en el documento

- Junto a «…NCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE] Q.P.T.R.C.»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.
- Junto a «…m. [Nº] ========================================================================»: requisito de procedibilidad del art. 5 LO 1/2025 — antes de presentar la demanda hay que intentar un medio adecuado de solución de controversias (MASC) y acreditarlo con la demanda (arts. 264.4.º y 399.3 LEC), salvo las materias excluidas del art. 5.2. Fuente: LO 1/2025, arts. 5 a 7 (BOE-A-2025-76).

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

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE] Q.P.T.R.C.

D./Dña. [NOMBRE Y APELLIDOS] Procurador de los Tribunales, colegiado núm. [Nº DE COLEGIADO] en representación de Dña. [NOMBRE Y APELLIDOS] y de D. [NOMBRE Y APELLIDOS], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], con la dirección letrada de D./Dña. [NOMBRE Y APELLIDOS] Colegiado núm. [Nº DE COLEGIADO] ante el Tribunal comparezco y DIGO:

Que en la representación que ostento deduzco DEMANDA DE DIVORCIO PRESENTADA POR UNO DE LOS CÓNYUGES, CON EL CONSENTIMIENTO DEL OTRO de los cónyuges D. y Dña. [NOMBRE Y APELLIDOS], ejercitando la acción prevista en el artículo 86 del Código Civil, en base a los siguientes

HECHOS

PRIMERO.- D. y Dña. contrajeron matrimonio [TIPO DE MATRIMONIO (CIVIL / CANÓNICO)], en [LOCALIDAD] con fecha de [FECHA] según acredito mediante la certificación de la inscripción de matrimonio que se acompaña con documento número [Nº DE DOCUMENTO], inscrito en el Registro Civil de [LOCALIDAD], de la ciudad de [LOCALIDAD], al tomo [TOMO], página

SEGUNDO.- El régimen económico matrimonial es el de [RÉGIMEN ECONÓMICO].

TERCERO.- Del citado matrimonio ha habido [Nº DE HIJOS], [NOMBRE Y APELLIDOS] de [EDAD], según se justifica mediante [ÓRGANO] de nacimiento con [Nº DE DOCUMENTO]

CUARTO.- A causa de divergencias nacidas por motivos personales e íntimos que por su naturaleza no se considera necesario relatar, la continuación de la vida en común se ha hecho imposible así como la vida matrimonial y familiar.

QUINTO.- El último domicilio conyugal estuvo situado en la casa núm. calle [CALLE] de la ciudad de [LOCALIDAD]

SEXTO.- Los cónyuges han decido de común acuerdo solicitar el divorcio, adjuntando el oportuno CONVENIO REGULADOR, que se acompaña como documento número [Nº DE DOCUMENTO], donde se establecen las cláusulas por las que va a regirse los efectos de la separación.

A los anteriores hechos le son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

El artículo 86 del Código Civil, en cuanto que establece que el matrimonio se disuelve, por divorcio sea cual fuere la forma, a petición de uno de los cónyuges, de ambos o de uno con consentimiento de otro.

Artículo 117 Constitución Española, que asigna a los órganos judiciales españoles el ejercicio de la potestad jurisdiccional, juzgando y haciendo ejecutar lo juzgado, siendo competentes para conocer de las demandas de separación cuando

a) ambos cónyuges tengan la nacionalidad española

b) los cónyuges sean residentes en España.

c) uno de los cónyuges sea español y tenga su residencia habitual en España, cualquiera que sea la nacionalidad y residencia del otro.

Conforme con lo dispuesto en el artículo 769 de la LECiv, será Juez competente para conocer de los procesos de nulidad, separación y divorcio, el de Primera Instancia del lugar del domicilio conyugal, y en el caso de residir los cónyuges en diferentes partidos judiciales, será el Juez competente, a elección del demandante o de los cónyuges que soliciten la separación o el divorcio de mutuo acuerdo, el del último domicilio del matrimonio o el de residencia del demandado.

En el presente caso

a) ambos cónyuges tienen su residencia en la ciudad (partido judicial) sede del Tribunal al que se dirige la demanda.

b) el último domicilio conyugal estuvo situado en la ciudad (partido judicial) sede del Tribunal al que se dirige la demanda.

c) aunque el domicilio conyugal estuvo situado en lugar diferente al de la sede (partido judicial) del Tribunal al que se dirige la demanda, al residir allí uno de los cónyuges firmantes de esta demanda, ha sido elegida la competencia por ambos esposos.

Artículo 6 de la LECiv. Los esposos están legitimados activamente para ejercitar la acción personal de la separación.

El trámite a seguir es el establecido en el artículo 777 LECiv, que establece un procedimiento especial para los supuestos contemplados en los artículos 81 y 86 del Código Civil, cuando la petición de divorcio se pida por ambos cónyuges o por uno de ellos con el consentimiento del otro.

Existiendo hijos menores de edad, y de conformidad con lo establecido en los artículos 749 y 775.5 ambos de la LECiv, debe ser oído el Ministerio Fiscal.

Por todo lo cual,

SUPLICO AL TRIBUNAL: que, teniendo por presentado este escrito inicial, con los documentos y copias que se acompañan, y por instado de común acuerdo el divorcio del matrimonio existente entre doña [NOMBRE Y APELLIDOS] y don [NOMBRE Y APELLIDOS], se sirva admitirlo, seguir el trámite establecido en el artículo 777 LECiv, acordar la ratificación de los interesados en el convenio que se presenta, y, previa audiencia del Ministerio Fiscal, dictar sentencia por la que se acuerde la disolución del matrimonio por divorcio del matrimonio formado por los solicitantes, y aprobando el convenio regulador que se acompaña.

Es justicia que espero alcanzar del Tribunal al que me dirijo, en [LOCALIDAD] a [DÍA] de [MES]

Fdo. Letrado [NOMBRE Y APELLIDOS] Fdo Procurador

Coleg. núm. Coleg. núm. [Nº]

========================================================================
