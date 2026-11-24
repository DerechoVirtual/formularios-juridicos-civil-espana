---
name: solicitud-extender-inscripcion-marginal-sentencia-civ-0271
description: "Solicitud de extender la inscripción marginal de sentencia de divorcio de otro Estado de la UE. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud de extender la inscripción marginal de sentencia de divorcio de otro Estado de la UE

> Formulario **CIV-0271** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Demanda de solicitud de extensión de la inscripción marginal de la sentencia judicial de divorcio dictada por un Tribunal extranjero, de un Estado miembro de la Unión Europea.

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud de extender la inscripción marginal de sentencia de divorcio de otro Estado de la UE» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud de extender la inscripción marginal de sentencia de divorcio de otro Estado de la UE” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:solicitud-extender-inscripcion-marginal-sentencia-civ-0271`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (8 veces)
- [ ] FECHA (4 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] Nº (2 veces)
- [ ] PÁGINA (2 veces)
- [ ] SECCIÓN (2 veces)
- [ ] TOMO (2 veces)
- [ ] ÓRGANO JUDICIAL (2 veces)
- [ ] DNI/NIE
- [ ] ESTADO CIVIL
- [ ] LUGAR
- [ ] NÚMERO
- [ ] PETICIÓN

## Normas que cita el formulario

- No cita artículos concretos; Claude localizará las normas aplicables con Jurisprudenciator si el documento las necesita.

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

Demanda de solicitud de extensión de la inscripción marginal de la sentencia judicial de divorcio dictada por un Tribunal extranjero, de un Estado miembro de la Unión Europea.


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

AL JUEZ-ENCARGADO DEL REGISTRO CIVIL DE [LOCALIDAD]

D./Dña. [NOMBRE Y APELLIDOS], con DNI [DNI/NIE], mayor de edad, de estado [ESTADO CIVIL] y con domicilio en [LOCALIDAD], ante el Sr./a. Juez-Encargado del Registro Civil de [LOCALIDAD] comparezco y DIGO:

Que el solicitante se ve en el caso de formular solicitud de extensión de la correspondiente inscripción al margen de la inscripción principal de matrimonio obrante en el Registro Civil de [LOCALIDAD], Sección [SECCIÓN], Tomo [TOMO], página [PÁGINA], de la resolución dictada por la autoridad extranjera competente [ÓRGANO JUDICIAL] declarando la disolución del matrimonio inscrito en virtud de sentencia judicial de divorcio de fecha [FECHA]. [PETICIÓN], sentando al efecto los hechos siguientes:

HECHOS

PRIMERO.- El solicitante contrajo matrimonio civil con Dña. [NOMBRE Y APELLIDOS], en [LOCALIDAD], el día [FECHA]. Se acompaña la correspondiente certificación literal de matrimonio expedida por el Registro Civil de [LOCALIDAD] (DOCUMENTO N.º [NÚMERO]).

SEGUNDO.- Con fecha [FECHA]. se ha dictado resolución judicial por la autoridad extranjera competente [ÓRGANO JUDICIAL] que declara la disolución vincular por divorcio de dicho matrimonio, por lo que se solicita la aplicación del Reglamento (CE) n.º 2201/2003 del Consejo, de 27 de noviembre de 2003, relativo a la competencia, el reconocimiento y la ejecución de resoluciones judiciales en materia matrimonial y de responsabilidad parental, aplicable por razones de vigencia temporal, a fin de actualizar los datos del Registro Civil en el que consta inscrito el matrimonio disuelto, mediante su reconocimiento registral a través de la extensión de la oportuna inscripción marginal de divorcio.

Se acompaña, en cumplimiento del art. 37 del citado Reglamento, copia auténtica y traducida de dicha resolución extranjera así como un certificado expedido por el órgano jurisdiccional que dictó la resolución en los términos fijados en el formulario que figura como Anexo I del Reglamento comunitario (DOCUMENTOS NÚMEROS [Nº] y [Nº]).

A los anteriores hechos son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

I

La competencia para acordar la extensión de la inscripción marginal de la resolución extranjera de divorcio corresponde al Encargado del Registro Civil donde consta inscrito el matrimonio, conforme a lo dispuesto en el art. 76 LRC y arts. 263 a 265 RRC.

II

Dispone el art. 21, apartados 1 y 2 del Reglamento (CE) n.º 2201/2003 del Consejo, de 27 de noviembre de 2003, relativo a la competencia, el reconocimiento y la ejecución de resoluciones judiciales en materia matrimonial y de responsabilidad parental, que las resoluciones dictadas en un Estado miembro serán reconocidas en los demás Estados miembros sin necesidad de recurrir a procedimiento alguno.

En particular, en cuanto a su eficacia en relación con el Registro Civil, según se establece, no se requerirá ningún procedimiento especial para la actualización de los datos del Registro Civil de un Estado miembro sobre la base de las resoluciones en materia de divorcio, separación judicial o nulidad del matrimonio dictadas en otro estado miembro y que con arreglo a la legislación de este último ya no admitan recurso.

Por lo expuesto,

SOLICITA

al Encargado del Registro Civil de [LOCALIDAD] que teniendo por presentado este escrito con los documentos que lo acompañan, se sirva admitirlo a fin de que se registre esta solicitud en el Libro correspondiente y, en trámite de calificación registral, acuerde practicar la inscripción marginal de la resolución de divorcio del matrimonio inscrito en el Registro Civil de [LOCALIDAD], Sección [SECCIÓN], Tomo [TOMO], página [PÁGINA], a fin de proceder a su reconocimiento registral y actualización de datos registrales.

Es justo en [LUGAR], a [FECHA].

Firma

========================================================================
