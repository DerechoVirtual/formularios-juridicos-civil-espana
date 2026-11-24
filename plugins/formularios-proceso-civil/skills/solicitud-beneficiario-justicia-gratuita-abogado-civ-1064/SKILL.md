---
name: solicitud-beneficiario-justicia-gratuita-abogado-civ-1064
description: "Solicitud del beneficiario de justicia gratuita de abogado y procurador de oficio en verbal. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud del beneficiario de justicia gratuita de abogado y procurador de oficio en verbal

> Formulario **CIV-1064** del plugin **Proceso civil: demandas, contestaciones, prueba y vista** (`formularios-proceso-civil`) · Civil › Escritos procesales (demanda, contestación, prueba, vista) · normativa revisada el 24-11-2026.

## Qué es

Escrito del demandante, beneficiario de la justicia gratuita, solicitando la inmediata designación de oficio de procurador y abogado para su representación y defensa para todos los trámites del juicio verbal a pesar de no ser preceptiva su intervención en el proceso al haber comunicado la parte contraria que actuará defendida por abogado y representada por procurador.

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud del beneficiario de justicia gratuita de abogado y procurador de oficio en verbal» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud del beneficiario de justicia gratuita de abogado y procurador de oficio en verbal” para mi caso». También puedes invocarla directamente con `/formularios-proceso-civil:solicitud-beneficiario-justicia-gratuita-abogado-civ-1064`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-proceso-civil:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Proceso civil: demandas, contestaciones, prueba y vista) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NÚMERO (3 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] AÑO
- [ ] CALLE
- [ ] COLEGIO
- [ ] FECHA
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] Nº DE PROCEDIMIENTO
- [ ] SEDE

## Normas que cita el formulario

- art. 545.1 LOPJ
- art. 545.3 LEC
- art. 32.4 LEC
- art. 28 LEC

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

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, provista de D.N.I. n.º [NÚMERO], con domicilio en [LOCALIDAD], calle [CALLE], n.º [NÚMERO], en autos de juicio verbal n.º [Nº DE PROCEDIMIENTO]/[AÑO], ante el Tribunal comparezco y como mejor en Derecho proceda, DIGO:

Habiendo justificado el demandante la solicitud del reconocimiento del derecho de asistencia jurídica gratuita, que motivó la suspensión del curso del proceso, por el Servicio de Orientación Jurídica del Iltre. Colegio de Abogados de [COLEGIO], se ha comunicado que no se nombra abogado y procurador, a pesar de estimarse la solicitud, por no ser preceptiva la intervención en el presente proceso (se acompaña la resolución como documento n.º [NÚMERO]), ante lo que se formulan las siguientes

ALEGACIONES

PRIMERA

Los justiciables pueden venir representados por procurador y dirigidos por abogado a través de dos diferentes vías: La común, que es la contratación libre del apoderado y defensor de entre los profesionales de cada Colegio habilitados ante el tribunal (arts. 545.1 LOPJ y 33.1 LEC), y la del turno de oficio, mediante la petición a los Colegios profesionales para que designen procurador que represente y abogado que defienda (art. 545.3 LEC).

La primera vía puede emplearse tanto para contratar postulantes preceptivos como para contratar los que, por excepción (arts. 23.2 y 31.2 LEC), no lo son en el proceso civil, pero de los que desea valerse el particular que, lógicamente, les retribuirá.

La segunda vía no puede emplearse cuando la asistencia de abogado y procurador no sea preceptiva en cualquier caso, sino sólo cuando la parte contraria haya comunicado al tribunal que actuará defendida por abogado y representada por procurador (art. 33.2, párrafo 1.º LEC), como ha ocurrido en el presente caso con la parte demandada, después de la presentación de la demanda por quien suscribe.

SEGUNDA

En principio, el derecho a la asistencia jurídica gratuita no comprende la gratuidad de la representación procesal y defensa letrada que resultan facultativas, pero el art. 6.3 LAJG prevé que la intervención de tales profesionales se incluya en el contenido material del derecho cuando ‘sea expresamente requerido por el Tribunal o Tribunal mediante auto motivado para garantizar la igualdad de las partes en el proceso’.

Cuando el art. 32.4 LEC ordena participar noticia del art. 6.3 LAJG ‘a fin de que puedan realizar la solicitud correspondiente’, se refiere a que la parte sepa que el procurador y abogado pueden resultar exentos de retribución por el cliente si se tiene derecho a la asistencia jurídica gratuita, de modo que tiene que solicitarlo, y ello determinará la suspensión del proceso hasta que se designen procurador y abogado provisionalmente de oficio por los Colegios profesionales, sin que se vaya a declarar en tal trámite, ni la gratuidad, por supuesto, ni tampoco la extensión de ésta a la representación y defensa técnicas.

TERCERA

El derecho a la defensa letrada no es renunciable, aunque se permita legalmente elegir entre la autodefensa o la defensa técnica en determinados minoritarios supuestos de juicios sencillos, de escasa cuantía, o actuaciones urgentes, lo que significa dejar su puntual ejercicio a la disponibilidad de las partes, pero cuando el justiciable carece de recursos económicos para sufragar un abogado de su elección, y la autodefensa se revela insuficiente y perjudicial para sus derechos e intereses legítimos en el proceso, no puede excusarse la provisión de abogado de oficio, según es doctrina constitucional inconcusa: STC 161/1985 de 29 de noviembre, STC 47/1987 de 22 de abril, STC 178/1991 de 19 de septiembre, STC 162/1993 de 18 de mayo, STC 175/1994 de 7 de junio, STC 51/1996 de 26 de marzo, STC 92/1996 de 27 de mayo o STC 152/00 de 12 de junio.

La comparecida observa la insuficiencia y perjuicio predecible de no contar con abogado, por lo que procede requerirlo, y en tal caso, la conveniencia, de cara a la representación pasiva procesal (art. 28 LEC), de asistirse de procurador, por igualdad de armas, dado que recibirá procurador y abogado ya cuando tiene presentada la demanda, y no ha podido tener el asesoramiento en el trance de demandar, mientras que el demandado la ha tenido en el de contestar.

En virtud de lo expuesto,

AL TRIBUNAL SUPLICO

que, por presentado este escrito con el documento adjunto, se digne admitirlo, y en mérito a lo manifestado, se acuerde requerir la inmediata designación de oficio de procurador de los tribunales y abogado para la representación y defensa de la demandante, D./Dña. [NOMBRE Y APELLIDOS]., titular del derecho a la asistencia jurídica gratuita para todos los trámites del presente juicio verbal,

Es justicia de hacerse en [LUGAR], a [FECHA].

Firma del Interesado/a

========================================================================
