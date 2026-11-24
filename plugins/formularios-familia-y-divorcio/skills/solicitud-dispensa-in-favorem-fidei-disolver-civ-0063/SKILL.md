---
name: solicitud-dispensa-in-favorem-fidei-disolver-civ-0063
description: "Solicitud de dispensa in favorem fidei para disolver un matrimonio canónico con persona no bautizada. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud de dispensa in favorem fidei para disolver un matrimonio canónico con persona no bautizada

> Formulario **CIV-0063** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud de dispensa in favorem fidei para disolver un matrimonio canónico con persona no bautizada» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud de dispensa in favorem fidei para disolver un matrimonio canónico con persona no bautizada” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:solicitud-dispensa-in-favorem-fidei-disolver-civ-0063`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (6 veces)
- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] AÑO (3 veces)
- [ ] DÍA (2 veces)
- [ ] FECHA (2 veces)
- [ ] MES (2 veces)
- [ ] CALLE
- [ ] CORREO ELECTRÓNICO
- [ ] DNI/NIE
- [ ] LUGAR
- [ ] TELÉFONO

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

Dª [NOMBRE Y APELLIDOS], provista de DNI número [DNI/NIE], con domicilio en [LOCALIDAD], calle [CALLE], dirección e-mail [CORREO ELECTRÓNICO], número de teléfono [TELÉFONO], nacida en esta misma localidad el día [FECHA], y bautizada en la Iglesia Parrroquial de [LOCALIDAD], el día [FECHA], el ante Vuestra Santidad comparezco y

EXPONGO

El día [DÍA] de [MES] de [AÑO] contraje matrimonio canónico en la Parroquia de [LOCALIDAD] de la ciudad de [LOCALIDAD], con D. [NOMBRE Y APELLIDOS], musulmán, natural de [LOCALIDAD], quien mantiene domicilio en esta misma ciudad, C/

Adjunto como Doc. nº 1 Partida del Matrimonio celebrado con previa obtención de la oportuna dispensa del impedimento de disparidad de cultos.

Fue durante unas vacaciones estivales cuando conocí al que posteriormente se constituiría en mi marido. Él trabajaba en una ONG española y mantenía residencia en la localidad de [LOCALIDAD] Su vida, costumbres y comportamiento eran en apariencia completamente occidentalizados. Tras esas vacaciones del año 1998 formalizamos nuestro noviazgo sin que surgiese problema alguno en nuestra relación ni en cuanto a la posibilidad de seguir manteniendo mis prácticas religiosas.

Dado que tal relación funcionaba correctamente y estábamos enamorados, a iniciativa suya, decidimos contraer matrimonio si bien, a iniciativa mía, lo fue en forma canónica. Él no me planteó ningún problema a dicha posibilidad puesto que, pese a confesarse musulmán no tenía apariencia de ser practicante. Así, celebramos nuestro matrimonio y realizamos viaje de novios a su país de origen. Durante la estancia constaté que mi ya esposo sí parecía entonces mantener una práctica religiosa frecuente. Tras el viaje de novios conocimos la situación de embarazo en que me encontraba y fruto de la que nacieron nuestros hijos gemelos, [NOMBRE Y APELLIDOS] y [NOMBRE Y APELLIDOS] El nacimiento de los niños y la negativa rotunda de su padre a que fueran bautizados comenzó a alertarme sobre la realidad de mi marido. Empezó, entonces, a revelarse en él uno férrea resistencia a participar en cualquier acto religioso católico y negar la posibilidad de que en nuestro domicilio existiesen motivos religiosos, imágenes, Belén ni nada que tuviese relación con mis creencias.

Dicha situación mantuvo un crecimiento exponencial al punto de exigirme, ahora sí, la participación en las celebraciones de su culto y comenzar a plantearse el cambio de residencia familiar a su ciudad de origen. Todos estos cambios fueron acompañados de una trasformación en cuanto a la imagen occidental que antaño ofrecía. Ahora D. mostraba otro tipo de relación conmigo: exigía una completa sumisión y el mantenimiento de un tipo de vestimenta que él consideraba adecuada, me impedía consumir alcohol, etc.

Vista la situación y el agravamiento de la actitud mostrada decidí iniciar los trámites del divorcio, obteniendo resolución en febrero de [AÑO] tras un procedimiento judicial contencioso.

Adjunto como doc. nº 2 copia testimoniada de la sentencia de divorcio referida.

Liberada de la relación mantenida pude regresar a mis prácticas religiosas y afianzar mi Fe en el seno de La Iglesia. Hoy, transcurridos más de cinco años del divorcio, mantengo una relación afectiva con D. [NOMBRE Y APELLIDOS], arquitecto feligrés de mi misma parroquia teniendo intención de que nuestra relación pueda continuar mediante el matrimonio.

En virtud de cuanto queda expuesto,

SOLICITO de V.S., la concesión de la DISPENSA IN FAVOREM FIDEI y, en consecuencia, declare la disolución del matrimonio contraído con D. [NOMBRE Y APELLIDOS], a fin de poder seguir manteniendo mi vida y, en su caso, mi próximo matrimonio, dentro de la Fe cristiana y mantener la educación de mis hijos dentro de la misma.

OTROSÍ DIGO: Que al objeto de poder acreditar los hechos expuestos, propongo la declaración testifical de los siguientes testigos:

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firmado:

========================================================================
