---
name: solicitud-notario-testamento-abierto-persona-civ-0423
description: "Solicitud al notario de testamento abierto de una persona judicialmente incapacitada. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud al notario de testamento abierto de una persona judicialmente incapacitada

> Formulario **CIV-0423** del plugin **Herencias, testamentos y donaciones** (`formularios-herencias-y-donaciones`) · Civil › Sucesiones y donaciones · normativa revisada el 24-11-2026.

## Qué es

Escrito dirigido a un Notario por quien ejerce la representación o el apoyo de una persona con discapacidad, a instancia de ésta, solicitando que se tramite el otorgamiento de su testamento abierto notarial y que se recabe el informe de profesionales sobre su capacidad para testar cuando la resolución judicial no se pronuncie sobre ello.

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud al notario de testamento abierto de una persona judicialmente incapacitada» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud al notario de testamento abierto de una persona judicialmente incapacitada” para mi caso». También puedes invocarla directamente con `/formularios-herencias-y-donaciones:solicitud-notario-testamento-abierto-persona-civ-0423`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-herencias-y-donaciones:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Herencias, testamentos y donaciones) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] AÑO (3 veces)
- [ ] DÍA (3 veces)
- [ ] MES (3 veces)
- [ ] NOMBRE Y APELLIDOS DE LA PERSONA CON DISCAPACIDAD (3 veces)
- [ ] DNI/NIF (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL REPRESENTANTE LEGAL O APOYO (2 veces)
- [ ] COLEGIO NOTARIAL
- [ ] DOMICILIO
- [ ] NOMBRE DEL NOTARIO

## Normas que cita el formulario

- art. 665 Código Civil

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

- Al principio del formulario: el original estaba redactado conforme al régimen anterior a la Ley 8/2021 (persona «incapacitada judicialmente», patria potestad prorrogada o rehabilitada, tutela, y designación obligatoria de dos facultativos por el Notario conforme a la redacción antigua del art. 665 CC). Se ha adaptado la terminología al régimen vigente (persona con discapacidad con medidas de apoyo); el art. 665 CC, en su redacción actual, atribuye al Notario la valoración de la capacidad para testar y le permite recabar informe de facultativos cuando lo considere necesario. Comprobar la redacción literal vigente del precepto antes de presentar.

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

A D./Dª [NOMBRE DEL NOTARIO], NOTARIO DEL ILUSTRE COLEGIO NOTARIAL DE [COLEGIO NOTARIAL]

D./Dª [NOMBRE Y APELLIDOS DEL REPRESENTANTE LEGAL O APOYO], vecino/a de [LOCALIDAD], con domicilio en [DOMICILIO], y DNI/NIF [DNI/NIF], que actúa como [ELEGIR: curador con facultades representativas / progenitor con patria potestad prorrogada o rehabilitada, conforme a la sentencia aplicable / otra figura de apoyo] de su [ELEGIR: hijo/a / persona apoyada], D./Dª [NOMBRE Y APELLIDOS DE LA PERSONA CON DISCAPACIDAD], con la misma vecindad y domicilio y DNI/NIF [DNI/NIF],

EXPONE

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— I. Que D./Dª [NOMBRE Y APELLIDOS DE LA PERSONA CON DISCAPACIDAD] fue objeto de resolución judicial firme de fecha [DÍA] de [MES] de [AÑO], rehabilitándose la patria potestad, de la que soy único titular por haber fallecido anteriormente el otro progenitor. Acompaño testimonio de dicha resolución.

— I. Que D./Dª [NOMBRE Y APELLIDOS DE LA PERSONA CON DISCAPACIDAD] fue objeto de resolución judicial firme de fecha [DÍA] de [MES] de [AÑO], en la que fui nombrado/a [ELEGIR: tutor/a / curador/a]. Acompaño testimonio de dicha resolución.

II. Que en la citada resolución no existe pronunciamiento expreso acerca de la capacidad para testar de mi [ELEGIR: hijo/a / pupilo/a / persona apoyada].

III. Que mi [ELEGIR: hijo/a / pupilo/a / persona apoyada] desea hacer testamento, tal y como me ha manifestado. Por ello, a instancia del mismo/a, me dirijo a usted para que se lleven a cabo los trámites legales necesarios al efecto.

En virtud de lo expuesto,

SOLICITO: Que, de acuerdo con lo establecido en el art. 665 del Código Civil, valore la capacidad de mi representado/a para el otorgamiento de testamento y, si lo considera necesario, designe los facultativos de su confianza que emitan informe acerca de sus facultades en orden al otorgamiento del mismo. Caso de resultar acreditada su capacidad, solicito que autorice el otorgamiento de su testamento abierto, fijando día y hora a tal efecto.

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma: [NOMBRE Y APELLIDOS DEL REPRESENTANTE LEGAL O APOYO]
