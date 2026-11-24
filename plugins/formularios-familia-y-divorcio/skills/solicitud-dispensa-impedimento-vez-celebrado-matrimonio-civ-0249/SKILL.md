---
name: solicitud-dispensa-impedimento-vez-celebrado-matrimonio-civ-0249
description: "Solicitud de dispensa de impedimento una vez celebrado el matrimonio. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud de dispensa de impedimento una vez celebrado el matrimonio

> Formulario **CIV-0249** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud de dispensa de impedimento una vez celebrado el matrimonio» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud de dispensa de impedimento una vez celebrado el matrimonio” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:solicitud-dispensa-impedimento-vez-celebrado-matrimonio-civ-0249`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (18 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] CALLE (2 veces)
- [ ] DNI/NIE (2 veces)
- [ ] FECHA (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] Nº DE DOCUMENTO
- [ ] SEDE
- [ ] TIPO DE IMPEDIMENTO

## Normas que cita el formulario

- art. 81 LJV
- art. 81.2 LJV
- art. 48 CC

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

- Junto a «…MILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.

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

D/Dª [NOMBRE Y APELLIDOS], mayor de edad, con domicilio en [LOCALIDAD], calle [CALLE], nº [NÚMERO], pta. y DNI nº [DNI/NIE] y D./Dª [NOMBRE Y APELLIDOS], mayor de edad, con domicilio en [LOCALIDAD], calle [CALLE], nº [NÚMERO], pta. y DNI nº [DNI/NIE], comparecen en este TRIBUNAL y como mejor proceda en Derecho, DICEN:

Que por medio del presente escrito y de acuerdo con lo dispuesto en el art. 48 del Código civil y arts. 81 y siguientes de la Ley de Jurisdicción Voluntaria, promueven PROCEDIMIENTO DE JURISDICCIÓN VOLUNTARIA PARA LA DISPENSA ULTERIOR DEL IMPEDIMENTO DE [TIPO DE IMPEDIMENTO] PARA CONTRAER MATRIMONIO, con base en los siguientes

HECHOS

PRIMERO .- D./Dª [NOMBRE Y APELLIDOS] y D./Dª [NOMBRE Y APELLIDOS] celebraron su matrimonio el día [FECHA], según consta inscrito en el Registro Civil de [LOCALIDAD]. Se acompaña como Documento nº [Nº DE DOCUMENTO], certificación de la citada inscripción de matrimonio.

SEGUNDO.- Entre D./Dª [NOMBRE Y APELLIDOS] y D./Dª [NOMBRE Y APELLIDOS] existía impedimento de parentesco para contraer matrimonio, según lo dispuesto en el artículo 47.2º del Código civil. En efecto, ambos son parientes colaterales en tercer grado por consanguinidad.

El árbol genealógico de los interesados es el siguiente:

D. es hijo de [NOMBRE Y APELLIDOS] y de [NOMBRE Y APELLIDOS]. Por vía paterna, es nieto de [NOMBRE Y APELLIDOS] y de [NOMBRE Y APELLIDOS], y por vía materna, nieto de [NOMBRE Y APELLIDOS] y de [NOMBRE Y APELLIDOS]. A su vez, es hermano de doble vínculo de [NOMBRE Y APELLIDOS], el cual es el padre de Dª..

Dª. es hija de [NOMBRE Y APELLIDOS], hermano de doble vínculo del solicitante, y de [NOMBRE Y APELLIDOS], teniendo por lo demás el mismo árbol genealógico en vía paterna. En vía materna, es nieta de [NOMBRE Y APELLIDOS] y de [NOMBRE Y APELLIDOS], sin relación de parentesco natural con los parientes de vía paterna.

Se acompañan, para acreditarlo, certificación de nacimiento de cada uno de ellos y certificación de nacimiento del padre/madre de D./Dª [NOMBRE Y APELLIDOS], como Documentos núms. 1 a 3. De donde resulta que su matrimonio está afectado por causa de nulidad.

TERCERO .- En el expediente matrimonial no se puso de manifiesto esta circunstancia por cuanto que en ningún momento los contrayentes fueron interrogados por este extremo, desconociendo que ello fuera impeditivo de su matrimonio.

CUARTO.- Existe justa causa para la dispensa del impedimento de parentesco, dada las circunstancias de la pareja:

QUINTO .- A fecha de hoy, no ha sido instada judicialmente la nulidad del matrimonio de los solicitantes.

Son aplicables a los referidos hechos los siguientes

FUNDAMENTOS DE DERECHO

PRIMERO.- COMPETENCIA. El art. 81 LJV establece que será competente para el conocimiento de este expediente el Tribunal de Instancia del domicilio o, en su defecto, de la residencia de cualquiera de los contrayentes.

SEGUNDO.- PROCEDIMIENTO El procedimiento a seguir en el presente supuesto es el de jurisdicción voluntaria, regulado en los artículos 81 a 84 de la LJV.

TERCERO.- LEGITIMACIÓN Están legitimados mis representados, según dispone el art. 81.2 LJV: Deberá promover este expediente el contrayente en quien concurra el impedimento para el matrimonio.

CUARTO.- DISPENSA DEL IMPEDIMENTO:- El art. 48 CC establece que el Juez podrá dispensar, con justa causa y a instancia de parte, mediante resolución previa dictada en expediente de jurisdicción voluntaria, los impedimentos de muerte dolosa del cónyuge o persona con la que hubiera estado unida por análoga relación de afectividad a la conyugal y de parentesco de grado tercero entre colaterales. La dispensa ulterior convalida, desde su celebración, el matrimonio cuya nulidad no haya sido instada judicialmente por alguna de las partes.

En virtud de lo expuesto,

SUPLICO AL TRIBUNAL: Que teniendo por presentado este escrito con los documentos que se acompañan, lo admita, teniendo por promovido EXPEDIENTE DE JURISDICCIÓN VOLUNTARIA, y tras practicar las audiencias legalmente exigidas, se digne dictar auto por el que, estimando lo solicitado, conceda a los solicitantes la DISPENSA ULTERIOR del impedimento de parentesco para contraer matrimonio, facilitándoles testimonio del citado auto.

En [LOCALIDAD] y [FECHA]

Firma de los solicitantes

========================================================================
