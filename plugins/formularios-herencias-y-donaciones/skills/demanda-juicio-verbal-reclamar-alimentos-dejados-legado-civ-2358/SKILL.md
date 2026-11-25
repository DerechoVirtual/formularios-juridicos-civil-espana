---
name: demanda-juicio-verbal-reclamar-alimentos-dejados-legado-civ-2358
description: "Demanda de juicio verbal para reclamar los alimentos dejados en un legado. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio verbal para reclamar los alimentos dejados en un legado

> Formulario **CIV-2358** del plugin **Herencias, testamentos y donaciones** (`formularios-herencias-y-donaciones`) · Civil › Sucesiones y donaciones · normativa revisada el 25-11-2026.

## Qué es

Demanda de juicio verbal en reclamación de alimentos cuando la obligación incumplida nace de un legado de alimentos ordenado en testamento (art. 879 CC) a cargo del heredero; se pide el pago de las mensualidades debidas y de las que se devenguen, y la prestación de la asistencia ordenada por el testador.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio verbal para reclamar los alimentos dejados en un legado» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio verbal para reclamar los alimentos dejados en un legado” para mi caso». También puedes invocarla directamente con `/formularios-herencias-y-donaciones:demanda-juicio-verbal-reclamar-alimentos-dejados-legado-civ-2358`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-herencias-y-donaciones:indice`.

## Qué contiene esta skill

- `SKILL.md` (este fichero): qué es el formulario, para qué sirve, cómo se usa, los datos que pide, las normas que cita, los avisos de actualización y las instrucciones para Claude.
- `assets/formulario.md`: el formulario seco, tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…]. Es el texto que se rellena; no lleva explicaciones.
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Herencias, testamentos y donaciones) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (8 veces)
- [ ] IMPORTE (6 veces)
- [ ] NOMBRE Y APELLIDOS DEL/DE LA DEMANDADO/A (5 veces)
- [ ] FECHA (4 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] IMPORTE EN LETRA (3 veces)
- [ ] DNI/NIE (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL/DE LA TESTADOR/A (2 veces)
- [ ] COLEGIO NOTARIAL
- [ ] CORREO ELECTRÓNICO
- [ ] FECHA DE FALLECIMIENTO
- [ ] FECHAS
- [ ] MESES ADEUDADOS
- [ ] NOMBRE DEL NOTARIO
- [ ] NOMBRE Y APELLIDOS DEL/DE LA ABOGADO/A
- [ ] NOMBRE Y APELLIDOS DEL/DE LA DEMANDANTE
- [ ] NOMBRE Y APELLIDOS DEL/DE LA HEREDERO/A
- [ ] NOMBRE Y APELLIDOS DEL/DE LA PROCURADOR/A
- [ ] Nº DE PROTOCOLO
- [ ] NÚMERO
- [ ] SEDE
- [ ] TELÉFONO

## Normas que cita el formulario

- art. 68 Ley 1/2000
- art. 50.1 Ley 1/2000
- art. 153 Código Civil
- art. 5 Ley Orgánica 1/2025
- art. 142 Código Civil
- art. 879 Código Civil
- art. 858 CC
- art. 675 Código Civil
- art. 148 Código Civil
- art. 720 LEC
- art. 1615 LEC

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

### Avisos de actualización (5) — se aplican en el texto, nunca se copian en el documento

- Al principio del formulario: Competencia territorial: si la reclamación del legado se considera «cuestión hereditaria», es competente el tribunal del último domicilio del causante (art. 52.1.4.º LEC), fuero imperativo, y en juicio verbal no cabe sumisión (art. 54.1 LEC); compruébese antes de fundarla solo en el art. 50.1 LEC.
- Junto a «…misión (art. 54.1 LEC); compruébese antes de fundarla solo en el art. 50.1 LEC.]»: No se ha podido localizar la STSJ Cataluña de 3-11-1995 (sin comprobar); el Código de Sucesiones de Cataluña que cita fue derogado por la Ley 10/2008 (libro IV CCCat).
- Junto a «…cesiones de Cataluña que cita fue derogado por la Ley 10/2008 (libro IV CCCat).]»: Se mantiene la nota (1): sus referencias al régimen vigente (arts. 437.1 y 2, 438.1 y 10, 23 y 31 LEC) son correctas; el comentario doctrinal que sigue describe la redacción originaria de la LEC.
- Junto a «…N CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] QUE POR TURNO DE REPARTO CORRESPONDA»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…], a [FECHA]. Firma del/de la Abogado/a | Firma del/de la Procurador/a NOTAS (1)»: esta nota comenta la redacción originaria de la LEC 1/2000. En la vigente, el juicio verbal principia por demanda con el contenido y forma propios del juicio ordinario (art. 437.1 LEC); la demanda sucinta y los impresos normalizados quedan para los juicios verbales en que no se actúe con abogado y procurador (art. 437.2 LEC); el demandado contesta por escrito en diez días (art. 438.1 LEC), y la vista solo se celebra si el tribunal la considera pertinente (art. 438.10 LEC). El límite de postulación de los arts. 23 y 31 LEC es hoy de 2.000 euros. Las referencias que siguen a la «demanda sucinta» como regla general deben leerse con esa advertencia.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

- Ninguna.

### Flujo

1. **Paso 0**: comprueba Jurisprudenciator (arriba).
2. Lee entero `assets/formulario.md` (el formulario que vas a rellenar, en la carpeta de esta skill) y la parte de `../indice/marco.md` que afecte al caso. Limítate a la materia de este formulario: no añadas contenido ajeno a él.
3. Pide los datos de la lista en una sola tanda. Si un dato aparece varias veces, aclara a qué persona o acto corresponde cada vez. Lo que el usuario no sepa se queda como hueco visible con su etiqueta (p. ej. [FECHA]).
4. Resuelve cada [ELEGIR …] y cada [OPCIONAL …] según los hechos, y sustituye cualquier indicación entre paréntesis del formulario («(se describirá…)», «(indicar…)») por el contenido que corresponda. Redacta las partes que dependen del caso (hechos, motivos, descripción de bienes).
5. Aplica los avisos de actualización en el lugar que indican. Comprueba con `buscar_articulo` cada norma citada; si alguna ha cambiado, usa la redacción vigente. Si citas jurisprudencia, localízala con `buscar_sentencias` o `buscar_por_cita` y léela con `leer_sentencias`.
6. Antes de entregarlo, pasa `verificar_escrito` con las frases que citan normas o sentencias y corrige lo que señale.
7. **Documento final = el formulario tal cual, rellenado y limpio.**
   - Empieza exactamente por la primera línea de `assets/formulario.md` y sigue su estructura y su orden hasta la firma.
   - No pongas en el documento título, nombre del formulario o de la skill, código, encabezados, «Para qué sirve», leyendas, avisos, notas de uso, comentarios ni explicaciones. Tampoco marcas [ELEGIR…] u [OPCIONAL…]: ya están resueltas.
   - Formato Word (.docx, con la skill de Word disponible): **Times New Roman 11 pt** en todo el documento, **interlineado 1,15**, **texto justificado**, márgenes de 2,5 cm. Los rótulos del formulario (REUNIDOS, CLÁUSULAS, HECHOS, SUPLICO…) en su propia línea y en negrita, sin cambiar su texto.
8. En el chat (nunca dentro del documento): datos pendientes, partes redactadas por ti, normas y sentencias comprobadas con Jurisprudenciator (y, si algún dato sale de internet, cuál y su enlace) y, si es un escrito judicial o administrativo, el plazo y el órgano ante el que se presenta.

El resultado es un borrador para que lo revise un profesional antes de usarlo.
