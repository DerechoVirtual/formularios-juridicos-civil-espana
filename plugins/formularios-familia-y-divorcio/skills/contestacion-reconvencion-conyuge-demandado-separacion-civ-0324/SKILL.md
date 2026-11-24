---
name: contestacion-reconvencion-conyuge-demandado-separacion-civ-0324
description: "Contestación a la reconvención del cónyuge demandado en separación matrimonial contenciosa. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contestación a la reconvención del cónyuge demandado en separación matrimonial contenciosa

> Formulario **CIV-0324** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Escrito de contestación a la reconvención formulada por el cónyuge demandado en procedimiento de separación matrimonial.

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contestación a la reconvención del cónyuge demandado en separación matrimonial contenciosa» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contestación a la reconvención del cónyuge demandado en separación matrimonial contenciosa” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:contestacion-reconvencion-conyuge-demandado-separacion-civ-0324`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE DE LA EMPRESA (3 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] Nº (3 veces)
- [ ] FECHA (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] AÑO
- [ ] ESPECIALIDAD DE INGENIERÍA TÉCNICA
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] NOMBRE DEL HIJO/A

## Normas que cita el formulario

- art. 86 CC
- art. 81.2.º CC
- art. 770.2.ª LEC
- art. 91 CC
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

AL TRIBUNAL

Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, que actúa en nombre y representación de D [NOMBRE Y APELLIDOS], como tengo debidamente acreditado en autos en autos de Juicio de Separación matrimonial nº [NÚMERO] / promovido a su instancia contra Dña. [NOMBRE Y APELLIDOS], ante el Tribunal comparezco y como mejor proceda en Derecho, DIGO:

Que, en la representación que ostento y dentro del plazo legal, vengo a CONTESTAR A LA RECONVENCIÓN formulada de contrario, con base a los siguientes datos y consideraciones jurídicas.

HECHOS

PRIMERO.- No se debate la existencia del matrimonio, y la presencia y edad del hijo menor común, y sin discutir tampoco la separación de hecho desde [FECHA], la discrepancia a propósito de cuál sea la conducta de uno u otro de los casados con relación a dicho hijo, y sus déficits, carece de relevancia en nuestro sistema en que, tanto la vida en común como la extinción del vínculo matrimonial no depende más que de la voluntad de los cónyuges.

SEGUNDO.- Nada de incierto, ni falto de integridad tiene la versión de la demanda, en cuanto que la existencia de [NOMBRE DEL HIJO/A], hijo común de los casados, de [Nº] años de edad, resulta perfectamente prescindible en este proceso, ya que terminó sus estudios en el año [AÑO], y no convive realmente con la demandada, contando con sus propios ingresos.

Acompañamos copia compulsada del título de ingeniero técnico de [ESPECIALIDAD DE INGENIERÍA TÉCNICA], como documento n.º [NÚMERO], impugnando expresamente el certificado municipal de convivencia, cuya fecha posterior a la demanda resulta expresiva.

Por consiguiente, no hay un deber alimenticio a cargo de mi representado, según pretende la demanda reconvencional.

TERCERO.- No se coincide con el ordinal cuarto de la contestación de la demanda, ya que si el hijo menor padece una enfermedad crónica, ni se trata de algo que precise de un cuidado tan obsesivo como se pinta, ni la permanente atención de la madre es factible que se produzca, al tener que atender su consulta, ni en fin el padre pretende más que comunicar con el hijo, dentro de respetar todas las condiciones de su crianza, entre las que se cuentan los requerimientos de salud.

CUARTO.- En relación con el quinto ordinal de los hechos de la contestación de la demanda, no niega mi mandante que presta servicios retribuidos para [NOMBRE DE LA EMPRESA], obteniendo rentas extremadamente por debajo de las que declara la demandada, que ni siquiera son todas, según acontece con quien puede trabajar por su cuenta.

A los anteriores hechos son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

I.- Lógicamente conformes con la competencia objetiva y territorial del Tribunal, la legitimación de los cónyuges, y el procedimiento adecuado escogido, y compareciendo las partes con la debida representación técnica y asistencia letrada, se asume que se han cumplido las exigencias formales para que se amplíe el objeto por acumulación sobrevenida de acciones (inserción endógena) de arts. 406 y 770.2º LEC.

II.- El fondo de la pretensión de la reconvención es que se declare, con extinción del matrimonio, el divorcio, y en efecto, el sistema del art. 86 CCiv, por relación al régimen de la separación no consensual del art. 81.2.º CCiv, impone la prevalencia del derecho a no permanecer casado sobre el derecho, distinto y autónomo, al puro cese de la vida en común, con las consecuencias respectivas de la separación conyugal.

Por lo tanto, así como es una de las exclusivas causas de reconvención del elenco del art. 770.2.ª LEC, no cabe más que asumir que, además y por encima de la separación que esta parte pretende, procede decretar judicialmente el divorcio.

Sin embargo, no puede hablarse en puridad de un allanamiento parcial (existe otra pretensión reconvencional), ya que conforme a los arts. 91 y 106 CCiv y 774 LEC, el Tribunal deberá pronunciarse en definitiva sobre las determinadas medidas, que es el meollo del proceso, y ya sean de la separación postulada por esta parte, y en su concreto tenor, o sean de la resultancia del divorcio, conforme al tenor de las solicitadas de contrario, existe divergencia.

No la hay en cuanto a la atribución de la guarda y custodia del hijo menor por la madre, pero carece de todo fundamento el postular que se prive a mi representado de la patria potestad, y aun que se elimine o posponga ‘sine die’ el principal objeto del juicio para mi mandante, que es no verse desvinculado de la educación del hijo y poder expresarle su cariño con un adecuado régimen de comunicación.

Por lo que toca a la pensión alimenticia, huelga extenderse en mayores razonamientos acerca de la realidad de que al hijo no le falta el nivel de vida envidiable que deriva de los ingresos de su madre, médico odontóloga, con clínica dental céntrica en la localidad, de las más reconocidas y caras,

Y en fin, respecto de la pensión alimenticia para el hijo de [Nº] años de edad, ingeniero técnico de [NOMBRE DE LA EMPRESA], desde hace [Nº] años, que no convive realmente con su madre, y que reside en [LOCALIDAD], trabajando para [NOMBRE DE LA EMPRESA], según se demostrará por vía testifical, dado que el empleo pertenece a la fraudulenta y extendida ‘economía sumergida’

III.- Las costas procesales deben ser impuestas a la parte demandada, al ver desestimadas sus precisas pretensiones, con arreglo al art. 394 LEC

Por todo lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito y por formulada en tiempo y forma contestación a la demanda reconvencional, se digne admitirla a trámite junto con los documentos de fondo acompañados, y previo el procedimiento que le corresponda, se venga dictar sentencia por la que, con declaración del divorcio del matrimonio, se desestime la reconvención, se absuelva libremente a la demandante de lo que en la misma se pide en cuanto a las medidas definitivas, con expresa condena en costas de la parte demandada.

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a

========================================================================
