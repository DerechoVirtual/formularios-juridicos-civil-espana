---
name: escrito-solicitando-internamiento-no-voluntario-civ-0396
description: "Escrito solicitando el internamiento no voluntario por trastorno psíquico de una persona adulta. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito solicitando el internamiento no voluntario por trastorno psíquico de una persona adulta

> Formulario **CIV-0396** del plugin **Discapacidad y medidas de apoyo (Ley 8/2021)** (`formularios-discapacidad-y-medidas-de-apoyo`) · Civil › Capacidad y medidas de apoyo · normativa revisada el 24-11-2026.

## Qué es

Escrito solicitando el internamiento no voluntario por razón de trastorno psíquico de una persona mayor de edad.

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito solicitando el internamiento no voluntario por trastorno psíquico de una persona adulta» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito solicitando el internamiento no voluntario por trastorno psíquico de una persona adulta” para mi caso». También puedes invocarla directamente con `/formularios-discapacidad-y-medidas-de-apoyo:escrito-solicitando-internamiento-no-voluntario-civ-0396`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-discapacidad-y-medidas-de-apoyo:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Discapacidad y medidas de apoyo (Ley 8/2021)) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (12 veces)
- [ ] LOCALIDAD (7 veces)
- [ ] Nº DE DOCUMENTO (5 veces)
- [ ] CALLE (3 veces)
- [ ] Nº (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] COLEGIO
- [ ] FECHA
- [ ] LUGAR
- [ ] SEDE

## Normas que cita el formulario

- art. 45 LEC
- art. 763.1 LEC
- art. 6 LEC
- art. 763 LEC
- art. 757.1 LEC
- art. 763.3 LEC
- art. 211 CC
- art. 200 CC
- art. 763.4 LEC

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

D./Dña. [NOMBRE Y APELLIDOS], Procurador de los Tribunales, en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS], vecino de [LOCALIDAD] calle [CALLE], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], ante el Tribunal comparezco, bajo la dirección técnica de D./Dña. [NOMBRE Y APELLIDOS], Letrado del Ilustre Colegio de Abogados de [COLEGIO], con despacho profesional en [LOCALIDAD], y como mejor proceda en Derecho DIGO:

Que por medio del presente escrito solicito el acuerdo de internamiento no voluntario por razón de trastorno psíquico de D./Dña. [NOMBRE Y APELLIDOS], vecina de [LOCALIDAD], con domicilio en la calle [CALLE] nº [NÚMERO], internamiento para el que no está en condiciones de decidirlo por sí misma, en base a los siguientes

HECHOS

PRIMERO.- D./Dña. [NOMBRE Y APELLIDOS], hermana de mi representado, tiene la edad de [Nº] años, su estado civil es de viuda, y vive sola en [LOCALIDAD], calle [CALLE], nº [NÚMERO], siendo mi representado su único pariente.

Se acompaña la correspondiente certificación de nacimiento expedida por el Registro Civil de [LOCALIDAD], el Libro de Familia, y certificado de empadronamiento expedido por el Ayuntamiento de [LOCALIDAD] (DOCUMENTOS Nos [Nº DE DOCUMENTO]).

SEGUNDO.- Hace aproximadamente [Nº] meses mi representado recibió las quejas de los vecinos de la comunidad donde reside D./Dña. [NOMBRE Y APELLIDOS], en razón de las malas condiciones de salubridad de la vivienda de aquélla, que trascendía a la limpieza y salud del edificio, así como de otra parte, de episodios de agresión a personas en la escalera, atribuidos a la insania mental de D./Dña. [NOMBRE Y APELLIDOS], lo que ha motivado que se hayan levantado varios atestados por la Policía Local (DOCUMENTOS Nos [Nº DE DOCUMENTO] a [Nº DE DOCUMENTO]).

TERCERO.- Teniendo noticia de estos hechos, mi representado ha visitado en varias ocasiones a D./Dña. [NOMBRE Y APELLIDOS], coincidiendo la impresión causada con la manifestada anteriormente por los vecinos, y reparando en que aquélla presenta evidentes alteraciones psíquicas, por lo que se solicitó informe del Centro de Salud de [LOCALIDAD] En dicho informe se señala que la examinada padece síndrome esquizofrénico, con brotes de agresividad y autolíticos, así como manía persecutoria, que supone peligrosidad social, constatando su ingreso en el Centro en varias ocasiones. Se adjunta dictamen médico de la Dr./a. [NOMBRE Y APELLIDOS], en el que se consigna el historial de ingresos como DOCUMENTO Nº [Nº DE DOCUMENTO].

FUNDAMENTOS DE DERECHO

I.- COMPETENCIA.

La competencia para conocer de la autorización que se solicita corresponde al Tribunal de Instancia al que me dirijo, por ser éste el del lugar donde reside la persona afectada por el internamiento (art. 45 LEC en relación con el art. 763.1 LEC).

II.- CAPACIDAD.

Esta parte posee capacidad para la presente solicitud, según lo establecido en los artículos 6 y siguientes de la LEC.

III.- POSTULACIÓN Y DEFENSA.

Se cumplen con las normas de postulación procesal, ya que la solicitud se presenta por medio de Procurador legalmente habilitado para actuar ante los Tribunales de este partido, y bajo la dirección de Letrado en ejercicio que redacta y firma, conforme a lo dispuesto en los arts. 23.1 y 31.1 LEC.

IV.- LEGITIMACIÓN.

El art. 763 LEC no establece quiénes están legitimados para solicitar la autorización previa del internamiento, pero debe entenderse que lo están las mismas personas legitimadas para interponer la demanda para la adopción judicial de medidas de apoyo a una persona con discapacidad (art. 757.1 LEC).

Está legitimada pasivamente D./Dña. [NOMBRE Y APELLIDOS] por ser la persona afectada por la medida de internamiento.

V.- PROCEDIMIENTO.

El procedimiento a seguir viene recogido en el artículo 763.3 de la LEC, y exige como trámites necesarios la audiencia por el Tribunal de la persona afectada por la decisión, del Ministerio Fiscal y de cualquier otra persona cuya comparecencia se estime conveniente o se solicite por la parte afectada por la medida. Igualmente como trámites indispensables se imponen el examen por el Tribunal de la persona de cuyo internamiento se trata y oír el dictamen de un facultativo por él designado.

VI.- El objeto del procedimiento establecido en el art. 763 LEC es el internamiento no voluntario, por causa o razón de trastorno psíquico, de una persona que no está en condiciones de decidirlo por sí, siendo su antecedente histórico más inmediato la Ley 13/1983, de 24 de octubre, de reforma del CCiv en materia de tutela, que introdujo el art. 211 CC, en que se regulaba el internamiento del presunto incapaz, reformado en su párrafo 1.º, por la LO 1/1996, de 15 de enero, de Protección Jurídica del Menor.

La expresión trastorno psíquico tenía su equivalencia en el art. 200 CCiv -en su redacción anterior a la reforma de la Ley 8/2021, de 2 de junio- cuando se refiere a las enfermedades o deficiencias de carácter psíquico; no obstante, a diferencia del art. 200 CCiv, el art. 763 LEC no requiere que el trastorno psíquico sea persistente, sino que basta que el trastorno impida a quien lo padece decidir por sí su internamiento.

En el presente caso, los hechos llevan a entender que D./Dña. [NOMBRE Y APELLIDOS] requiere tratamiento médico en régimen de internamiento, por lo que, de acuerdo con el precepto arriba mencionado, debe concederse la autorización judicial para dicha medida, durante el tiempo que sea clínicamente necesaria la asistencia.

El art. 763.4 LEC precisa que los facultativos que atiendan al enfermo que debe quedar internado informarán periódicamente al Tribunal sobre la necesidad de mantener la medida, por lo menos cada seis meses, a no ser que proceda el alta clínica, sin que tenga que contemplarse en el presente caso una frecuencia de noticias más exigente, ya que la autorización es, por razón de los padecimientos de la internada, que evolucionan en degradación cronificada, indefinida.

Por lo expuesto,

SUPLICO AL TRIBUNAL

tenga por presentado este escrito junto con sus documentos y copias, se sirva admitirlo y tenerme por personado y parte en la representación que ostento y por realizadas las manifestaciones en él contenidas, y siguiendo los trámites legales oportunos, se disponga el internamiento indefinido de D./Dña. [NOMBRE Y APELLIDOS], hasta alta por indicación médica, en centro asistencial sanitario dedicado al tratamiento y cuidado de personas con anomalías psíquicas, que deberá tener informado al Tribunal semestralmente.

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a

========================================================================
