---
name: solicitud-nulidad-actuaciones-sentencia-quien-debio-civ-1321
description: "Solicitud de nulidad de actuaciones de la sentencia por quien debió ser parte en el juicio. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud de nulidad de actuaciones de la sentencia por quien debió ser parte en el juicio

> Formulario **CIV-1321** del plugin **Recursos civiles: reposición, apelación, casación y queja** (`formularios-recursos-civiles`) · Civil › Recursos · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud de nulidad de actuaciones de la sentencia por quien debió ser parte en el juicio» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud de nulidad de actuaciones de la sentencia por quien debió ser parte en el juicio” para mi caso». También puedes invocarla directamente con `/formularios-recursos-civiles:solicitud-nulidad-actuaciones-sentencia-quien-debio-civ-1321`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-recursos-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Recursos civiles: reposición, apelación, casación y queja) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (6 veces)
- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] NOMBRE DEL REPRESENTADO/A (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] Nº DE PROCEDIMIENTO
- [ ] ÓRGANO JUDICIAL

## Normas que cita el formulario

- art. 241 LOPJ
- art. 228 LEC
- art. 238.3 LOPJ
- art. 241.2 LOPJ
- art. 228.2 LEC

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

- Junto a «…CIAL] Proceso [Nº DE PROCEDIMIENTO] A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

Tribunal [ÓRGANO JUDICIAL]

Proceso [Nº DE PROCEDIMIENTO]

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA

D. [NOMBRE Y APELLIDOS] Procurador de los Tribunales y de [NOMBRE DEL REPRESENTADO/A], actuando en nombre y representación de [NOMBRE DEL REPRESENTADO/A], parte demandada en los autos de proceso ordinario seguidos ante ese Tribunal con el número [NÚMERO], según consta en escritura de poder otorgada al efecto que acompaño y cuya devolución solicito previo testimonio en autos, ante el Tribunal comparezco y como mejor proceda en derecho DIGO:

Que habiendo tenido conocimiento esta parte de la sentencia dictada en los autos arriba expresados al haber sido notificada de la diligencia de lanzamiento de fecha [FECHA], por medio del presente escrito y al amparo de lo dispuesto en el art. 241 de la LOPJ y art. 228 de la LEC promuevo la NULIDAD DE ACTUACIONES en el mencionado proceso en base a los siguientes hechos y fundamentos:

PRIMERO.- (Antecedentes y cumplimiento de requisitos) El presente proceso se inició por demanda presentada por D. [NOMBRE Y APELLIDOS] contra D. [NOMBRE Y APELLIDOS], en reivindicación de la finca registral número [NÚMERO], habiéndose dictado sentencia de fecha [FECHA] por la que se estimaba la demanda, resultando que mi representada es propietaria pro indiviso de dicha finca.

En fecha [FECHA] se dicta auto de ejecución de sentencia, acordándose por el Tribunal el lanzamiento de la finca de los ocupantes, lo cual es notificado a esta representación en fecha [FECHA], tal como consta en autos, momento en que tiene conocimiento por primera vez del proceso y de la sentencia.

Por tanto, se cumplen los requisitos del art. 241 de la LOPJ y 228 de la LEC, puesto que mi representada, como titular de la finca, debió ser parte en el proceso, y en tanto que la petición se deduce dentro del plazo de veinte días desde que se conoció la sentencia y no haber transcurrido cinco años desde que la misma fue dictada, y al ser firme la sentencia no siendo susceptible de repararse el defecto por otro recurso.

SEGUNDO.- (Motivos de nulidad y hechos en que se basa) La nulidad que se solicita lo es al amparo del art. 24 de la CE y art. 238.3 de la LOPJ y 225.3 de la LEC, al haberse seguido el proceso sin audiencia ni contradicción de mi representada, cuando debió ser llamada al mismo como litisconsorte necesaria, al ser titular proindiviso de la finca reivindicada, según claramente resulta de la inscripción registral que acompañamos como documento número 1 de este escrito.

La infracción del principio de audiencia y contradicción claramente resulta de los siguientes hechos:

a) la parte demandante dirigió su demanda contra D. [NOMBRE Y APELLIDOS], titular del 50% de la propiedad proindiviso de la finca reinvidicada, obviando demandar a mi representada que era titular del otro 50%.

b) el demandado D. [NOMBRE Y APELLIDOS] y mi representada eran matrimonio al tiempo de adquirir la finca, pero posteriormente, en fecha [FECHA] con anterioridad a iniciarse este proceso, se separaron judicialmente, dictándose sentencia de separación en fecha [FECHA] Tal como se recoge en dicha sentencia el uso de la vivienda reivindicada fue atribuida a mi mandante e hijos (acompaño como documento número 2 testimonio de la sentencia de separación).

c) esta misma situación de separación del matrimonio y la mala relación personal entre el demandado y mi representada, explica que su ex cónyuge no le comunicara la interposición de la demanda, en represalia a que se adjudicara el uso a mi representada en la referida sentencia de separación, siendo además totalmente demostrativo de su mala fe el hecho que se allanara a la demanda interpuesta, a sabiendas que la vivienda no era de su exclusiva titularidad y que la estaban utilizando su ex cónyuge e hijos.

TERCERO.- (Fundamentos de la nulidad postulada) La nulidad de actuaciones que se postula resulta palmaria del relato del curso de proceso, por cuanto se han infringido los principios de audiencia y contradicción, habiéndose pronunciado la condena sin ser oída mi representada, con evidente mala fe, al menos, en la conducta del demandado.

Por tanto, existe una evidente situación de indefensión que debe dar lugar a la nulidad de las actuaciones, conforme a los arts. 225 y ss. de la LEC, reponiendo las actuaciones al momento que mi representada pueda contestar a la demanda y defenderse en el proceso.

Por lo expuesto es de justicia y,

SUPLICO AL TRIBUNAL que tenga por presentado este escrito y documento que se acompaña, por promovido incidente de nulidad de actuaciones practicadas en este proceso, y, previos los trámites legales, dicte resolución por la que declare la nulidad de lo actuado reponiendo las actuaciones al momento procesal en que mi representada pueda comparecer y actuar en el juicio.

(caso de solicitarse la suspensión de la ejecución) OTROSÍ DIGO que al amparo de lo dispuesto en el art. 241.2 de la LOPJ y art. 228.2 de la LEC solicito que se acuerde la suspensión del lanzamiento decretado, puesto que existe una sólida apariencia de buen derecho y se originaría un perjuicio irreparable de seguir adelante con el mismo, pues el inmueble es la vivienda habitual de mi representada y de sus dos hijos, por lo que de llevarse a cabo el mismo podría perder el recurso su finalidad.

SUPLICO AL TRIBUNAL que acuerde de conformidad.

En L. y F.

(Firma Procurador y Abogado)

========================================================================
