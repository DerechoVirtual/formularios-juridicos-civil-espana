---
name: demanda-rectificar-error-inscripcion-nacimiento-civ-0177
description: "Demanda para rectificar un error en la inscripción de nacimiento en el Registro Civil. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda para rectificar un error en la inscripción de nacimiento en el Registro Civil

> Formulario **CIV-0177** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda para rectificar un error en la inscripción de nacimiento en el Registro Civil» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda para rectificar un error en la inscripción de nacimiento en el Registro Civil” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-rectificar-error-inscripcion-nacimiento-civ-0177`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (9 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] AÑO (2 veces)
- [ ] FECHA (2 veces)
- [ ] CALLE
- [ ] COLEGIO
- [ ] DÍA
- [ ] LIBRO
- [ ] LUGAR
- [ ] MES
- [ ] Nº
- [ ] PROVINCIA
- [ ] SEDE

## Normas que cita el formulario

- art. 781 bis Ley 1/2000
- art. 52.1.17 LEC
- art. 85.1 LOPJ
- art. 753 LEC
- art. 3.2 LO 1/2025

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

D./Dña. [NOMBRE Y APELLIDOS] Procurador/a de los Tribunales, en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, soltero/a, con domicilio en la calle [CALLE] de [LOCALIDAD] provincia de [PROVINCIA], provisto de D.N.I. núm. [Nº], según acredito mediante la oportuna escritura de poder que acompaño, con el ruego de que, previo testimonio en autos, me sea devuelta por necesitarla para otros usos, y bajo la dirección letrada de D./Dña. [NOMBRE Y APELLIDOS] abogado/a del Ilustre Colegio de Abogados de [COLEGIO], ante este Tribunal comparezco y, como mejor proceda en Derecho,

DIGO

Que mediante el presente escrito solicito la apertura de juicio ordinario civil con el fin de promover la rectificación del acta de nacimiento, dirigiendo la demanda contra el Ministerio Fiscal, con base en los siguientes:

HECHOS

De acuerdo con el acta de nacimiento de quien suscribe, de fecha [FECHA] que obra en el libro [LIBRO] del año [AÑO] en el Registro Civil de [LOCALIDAD], mi madre de nombre [NOMBRE Y APELLIDOS] y quien consideraba ser mi padre de nombre [NOMBRE Y APELLIDOS] me registraron bajo el nombre [NOMBRE Y APELLIDOS], con el primer apellido de cada uno en reconocimiento de filiación matrimonial. Se aporta como Documento núm. 1 certificación literal de nacimiento.

Mediante sentencia firme de fecha [FECHA] se declaró probado que mi padre biológico no era quien figura en el Registro inscrito como tal, hoy divorciado de mi madre, sino D. [NOMBRE Y APELLIDOS]; circunstancia ésta que resultó probada en el marco de un proceso judicial de reclamación de filiación no matrimonial con impugnación de la contraria interpuesto como consecuencia de ser conocedor tras su divorcio de su esterilidad. Se aporta como Documento núm.2 testimonio de la sentencia judicial firme referida.

A estos hechos le son aplicables los siguientes:

FUNDAMENTOS DE DERECHO

El art. 90 de la LRC establece que los asientos están bajo la salvaguarda de los Tribunales y su rectificación se efectuará en virtud de resolución judicial firme de conformidad con lo previsto en el artículo 781 bis de la Ley 1/2000, de 7 de enero, de Enjuiciamiento Civil. El art. 52.1.17 de la LEC en relación con el art. 85.1º LOPJ establece, en cuanto a la competencia territorial, que será competente el Tribunal de Instancia de la capital de provincia del domicilio del recurrente.

El art. 781 bis en relación con el art. 753 de la LEC, debiendo sustanciarse el procedimiento por los trámites del juicio verbal con las especialidades establecidas en dichos preceptos.

En su virtud,

Conforme a lo dispuesto en el art. 3.2 LO 1/2025, la presente demanda no está sujeta al requisito de MASC, en cuanto se dirige contra una entidad pública como lo es en este caso el Ministerio Fiscal.

SUPLICO que teniendo por presentado este escrito con sus copias y documentos, se sirva admitirlos, me tenga por personado como parte en este procedimiento y acreditada la representación que ostento se entienda conmigo para las siguientes actuaciones, se sirva admitir a trámite la demanda de juicio verbal de solicitud de rectificación de error en la inscripción de nacimiento del Registro Civil de [LOCALIDAD] y en su día, previa práctica de las pruebas que considere oportunas, dicte sentencia acordando la solicitada rectificación en el sentido solicitado.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Fdo. Procurador/a	Fdo. Letrado/a
D./Dña. [NOMBRE Y APELLIDOS] D./Dña. [NOMBRE Y APELLIDOS]

========================================================================
