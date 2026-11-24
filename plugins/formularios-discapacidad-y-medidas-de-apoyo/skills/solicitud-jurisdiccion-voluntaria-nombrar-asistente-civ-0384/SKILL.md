---
name: solicitud-jurisdiccion-voluntaria-nombrar-asistente-civ-0384
description: "Solicitud de jurisdicción voluntaria para nombrar asistente (Derecho civil catalán). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud de jurisdicción voluntaria para nombrar asistente (Derecho civil catalán)

> Formulario **CIV-0384** del plugin **Discapacidad y medidas de apoyo (Ley 8/2021)** (`formularios-discapacidad-y-medidas-de-apoyo`) · Civil › Capacidad y medidas de apoyo · normativa revisada el 24-11-2026.

## Qué es

Solicitud de expediente de jurisdicción voluntaria para que se nombre un asistente a una persona mayor de edad que, por una discapacidad que no la incapacita, necesita ayuda para cuidar de sí misma o de sus bienes, conforme al Derecho civil de Cataluña (arts. 226-1 y siguientes del Código Civil de Cataluña).

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud de jurisdicción voluntaria para nombrar asistente (Derecho civil catalán)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud de jurisdicción voluntaria para nombrar asistente (Derecho civil catalán)” para mi caso». También puedes invocarla directamente con `/formularios-discapacidad-y-medidas-de-apoyo:solicitud-jurisdiccion-voluntaria-nombrar-asistente-civ-0384`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-discapacidad-y-medidas-de-apoyo:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Discapacidad y medidas de apoyo (Ley 8/2021)) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS DEL ASISTENTE PROPUESTO (4 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] SEDE (3 veces)
- [ ] DOMICILIO (2 veces)
- [ ] PORCENTAJE (2 veces)
- [ ] AÑO
- [ ] CORREO ELECTRÓNICO
- [ ] DÍA
- [ ] EDAD
- [ ] ENTIDAD COMPETENTE
- [ ] ESPECIALIDAD
- [ ] MES
- [ ] NOMBRE Y APELLIDOS DEL ABOGADO/A
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] NOMBRE Y APELLIDOS DEL SOLICITANTE
- [ ] NOMBRE Y APELLIDOS DEL TESTIGO
- [ ] Nº
- [ ] PERSONAS QUE SE EXCLUYEN
- [ ] PROPONER LOS DEMÁS TESTIGOS

## Normas que cita el formulario

- art. 226 Código Civil

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

### Avisos de actualización (4) — se aplican en el texto, nunca se copian en el documento

- Junto a «…MILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.
- Junto a «…licito que sea definido conforme al artículo 226-2 del Código Civil de Cataluña.»: comprobar el texto vigente de los arts. 226-1 y siguientes del Código Civil de Cataluña, modificados tras la reforma de 2021 en materia de apoyos a personas con discapacidad, y su encaje con la Ley 8/2021.
- Junto a «…ntaria regulado en la Ley 15/2015, de 2 de julio, de la Jurisdicción Voluntaria.»: el original remitía a los arts. 1811 y siguientes de la LEC de 1881, hoy sustituidos por la Ley 15/2015; comprobar el capítulo concreto aplicable al nombramiento de asistente.

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

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS DEL SOLICITANTE], mayor de edad, [actuando en su propio nombre / a través de Procurador/a D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A]] y bajo la dirección letrada de D./Dña. [NOMBRE Y APELLIDOS DEL ABOGADO/A], al amparo de lo dispuesto en el artículo 226-1 del Código Civil de Cataluña, ante la Sección Civil del Tribunal de Instancia de [SEDE] que por turno de reparto corresponda comparezco y, como mejor proceda en Derecho, DIGO:

Que mediante el presente escrito promuevo expediente de jurisdicción voluntaria para NOMBRAMIENTO DE ASISTENTE, de acuerdo con lo establecido en los artículos 226-1 y siguientes del Código Civil de Cataluña, en base a los siguientes

HECHOS

PRIMERO.– Que el solicitante tiene [EDAD] años de edad, padeciendo una discapacidad no incapacitante de sus facultades físicas o psíquicas, por cuanto [RAZONAR EN CADA CASO; p. ej., está afecto/a de un retraso mental leve que le produce una discapacidad psíquica del [PORCENTAJE] %], según resulta del informe médico del Dr./Dra. [NOMBRE Y APELLIDOS], especialista en [ESPECIALIDAD], que se acompaña como documento número [Nº], y de la resolución de [ENTIDAD COMPETENTE] que reconoce dicho grado de discapacidad en un [PORCENTAJE] %.

SEGUNDO.– El solicitante vive en la actualidad solo/a, teniendo como familia a [PARIENTES, p. ej., dos sobrinos, D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS]], los cuales residen en la localidad de [LOCALIDAD], con quienes apenas tiene relación.

En su vida diaria está atendido personalmente por D./Dña. [NOMBRE Y APELLIDOS DEL ASISTENTE PROPUESTO], con quien mantiene estrechos vínculos personales y afectivos, y quien se preocupa constantemente por el bienestar del solicitante.

TERCERO.– En consonancia con ello, y de conformidad con lo que dispone el artículo 226-1 del Código Civil de Cataluña, es voluntad expresa del solicitante que sea nombrado asistente D./Dña. [NOMBRE Y APELLIDOS DEL ASISTENTE PROPUESTO], excluyendo en todo caso a [PERSONAS QUE SE EXCLUYEN], con los que no tiene ninguna relación ni se han preocupado nunca del solicitante.

CUARTO.– En cuanto al contenido de la asistencia, solicito que sea definido conforme al artículo 226-2 del Código Civil de Cataluña.

FUNDAMENTOS DE DERECHO

COMPETENCIA

Son competentes los Tribunales de Instancia de [SEDE], por ser el del domicilio del solicitante.

PROCEDIMIENTO

Debe seguirse el procedimiento de jurisdicción voluntaria regulado en la Ley 15/2015, de 2 de julio, de la Jurisdicción Voluntaria.

LEGITIMACIÓN

Esta parte está legitimada conforme a lo dispuesto en el art. 226-1 del Código Civil de Cataluña.

FUNDAMENTOS DE FONDO

El art. 226-1 del Código Civil de Cataluña establece que la persona mayor de edad que lo necesite para cuidar de sí misma o de sus bienes puede solicitar a la autoridad judicial el nombramiento de un asistente, debiendo procederse al nombramiento conforme al artículo 226-2, solicitando que sea nombrado asistente D./Dña. [NOMBRE Y APELLIDOS DEL ASISTENTE PROPUESTO], persona que está procurando todos los cuidados al solicitante, con el contenido establecido en el artículo 226-2 y acordando la inscripción del nombramiento en el Registro Civil.

Por lo expuesto,

SUPLICO AL TRIBUNAL: Que tenga por presentado este escrito con los documentos que se acompañan, lo admita y tenga por promovido expediente de jurisdicción voluntaria de nombramiento de asistente del solicitante y, practicadas las diligencias oportunas, incluida la información testifical que se interesa en el otrosí y con intervención del Ministerio Fiscal, y previos los demás trámites con arreglo a Derecho, dicte resolución en la que se nombre asistente a D./Dña. [NOMBRE Y APELLIDOS DEL ASISTENTE PROPUESTO], con las funciones que se determinen conforme al artículo 226-2 del Código Civil de Cataluña, y acordando la inscripción del nombramiento en el Registro Civil de [LOCALIDAD].

OTROSÍ PRIMERO DIGO: Que, a efectos de comunicaciones, designo el domicilio del letrado firmante de este escrito, sito en [DOMICILIO], así como la dirección de correo electrónico del mismo, [CORREO ELECTRÓNICO].

SUPLICO AL TRIBUNAL: Tenga por hecha la citada designación de domicilio.

OTROSÍ SEGUNDO DIGO: Que, para acreditar la certeza de los hechos relatados, ofrezco los siguientes testigos:

— D./Dña. [NOMBRE Y APELLIDOS DEL TESTIGO], con domicilio en [DOMICILIO].

[PROPONER LOS DEMÁS TESTIGOS]

SUPLICO AL TRIBUNAL: Tenga por propuestos a los testigos indicados, admitiendo la testifical ofrecida, comprometiéndose esta parte a que comparezcan en el día y hora que se señale (o, en su caso, solicitando que sean citados judicialmente para la práctica de la diligencia).

Es justicia que insto en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del solicitante y del letrado/a
