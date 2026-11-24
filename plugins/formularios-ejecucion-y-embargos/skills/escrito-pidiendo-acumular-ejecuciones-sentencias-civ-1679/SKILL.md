---
name: escrito-pidiendo-acumular-ejecuciones-sentencias-civ-1679
description: "Escrito pidiendo acumular ejecuciones de sentencias contra un mismo deudor ante distintos tribunales. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito pidiendo acumular ejecuciones de sentencias contra un mismo deudor ante distintos tribunales

> Formulario **CIV-1679** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Escrito de un ejecutante, en una ejecución de título judicial, para solicitar la acumulación de los procesos de ejecución que se siguen frente a un mismo ejecutado ante distintos tribunales, cuando el deudor es insuficiente patrimonialmente y existe conexión entre los créditos, a fin de que se siga un solo proceso ejecutivo (art. 555.2 LEC).

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito pidiendo acumular ejecuciones de sentencias contra un mismo deudor ante distintos tribunales» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito pidiendo acumular ejecuciones de sentencias contra un mismo deudor ante distintos tribunales” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:escrito-pidiendo-acumular-ejecuciones-sentencias-civ-1679`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (5 veces)
- [ ] DENOMINACIÓN SOCIAL DEL EJECUTADO (4 veces)
- [ ] IMPORTE (4 veces)
- [ ] Nº DE PROCEDIMIENTO (4 veces)
- [ ] FECHA (3 veces)
- [ ] SEDE (3 veces)
- [ ] FIRMA (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL EJECUTANTE (2 veces)
- [ ] AÑO
- [ ] COLEGIO
- [ ] CONCEPTO DE LAS CANTIDADES
- [ ] DOMICILIO
- [ ] DÍA
- [ ] ENTIDAD
- [ ] MES
- [ ] NOMBRE Y APELLIDOS DEL EJECUTANTE EN ESTOS AUTOS
- [ ] NOMBRE Y APELLIDOS DEL LETRADO/A
- [ ] NOMBRE Y APELLIDOS DEL OTRO EJECUTANTE
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] Nº DE COLEGIADO

## Normas que cita el formulario

- art. 555.2 LEC

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

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, que actúa en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS DEL EJECUTANTE], según acredito mediante poder general para pleitos al efecto otorgado, que acepto y acompaño, y en el que constan todas las circunstancias personales del poderdante, con ruego de devolución previo testimonio en autos de copia bastante, bajo la dirección del/la Letrado/a D./Dña. [NOMBRE Y APELLIDOS DEL LETRADO/A], colegiado/a n.º [Nº DE COLEGIADO] del Ilustre Colegio de Abogados de [COLEGIO], con despacho abierto en [LOCALIDAD], calle [DOMICILIO], n.º [Nº], en autos de Ejecución de Título Judicial n.º [Nº DE PROCEDIMIENTO], comparezco y, como mejor en Derecho proceda, DIGO:

PRIMERO.– El presente procedimiento se refiere a la ejecución contra [DENOMINACIÓN SOCIAL DEL EJECUTADO] por el importe de las cantidades correspondientes a [CONCEPTO DE LAS CANTIDADES, p. ej., primas devengadas y no percibidas, así como indemnización por clientela a la resolución del contrato de agencia con aquella mercantil], que dieron lugar al Juicio Ordinario n.º [Nº DE PROCEDIMIENTO], promovido por D./Dña. [NOMBRE Y APELLIDOS DEL EJECUTANTE EN ESTOS AUTOS], en que se dictó sentencia firme de condena de fecha [FECHA], título por el que ha recaído auto que despacha ejecución el [FECHA] en el presente procedimiento, por principal de [IMPORTE] euros.

SEGUNDO.– Mi mandante formuló demanda contra [DENOMINACIÓN SOCIAL DEL EJECUTADO], igualmente por el importe de las cantidades correspondientes a [CONCEPTO DE LAS CANTIDADES] derivadas del contrato que también tenía concertado con esta sociedad, recayendo sentencia de condena de fecha [FECHA], por la que se ha deducido solicitud de ejecución, que ha dado lugar a la Ejecución de Título Judicial n.º [Nº DE PROCEDIMIENTO], seguida ante la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº], con fecha posterior a la de estos autos, en persecución de una cantidad por principal de [IMPORTE] euros.

Se acompañan copias testimoniadas de la sentencia firme, demanda ejecutiva y auto que despacha la ejecución como documentos n.º [Nº] a [Nº].

TERCERO.– Mi patrocinado tiene noticia de otras ejecuciones contra [DENOMINACIÓN SOCIAL DEL EJECUTADO], y es el caso que esta empresa ha cesado en su actividad, no conociéndose más bienes de su responsabilidad que los créditos frente a terceros, que han sido embargados por mi patrocinado después de haberlo sido en este proceso, de modo que, a la luz de las contestaciones a los oficios de retención de [ENTIDAD] de que hay constancia en estos autos, se evidencia por el momento una insuficiencia patrimonial de la deudora ejecutada. Ello, sumado a la conexión clara entre los créditos ejecutivos y a razones de economía de medios, aconsejan la reunión en una de ambas ejecuciones contra la deudora común.

CUARTO.– El art. 555.2 LEC autoriza, a instancia de cualquiera de los ejecutantes, a acordar la acumulación de los procesos de ejecución que se sigan frente a un mismo ejecutado cuando el Letrado de la Administración de Justicia competente en el proceso más antiguo lo considera más conveniente para la satisfacción de todos los acreedores ejecutantes.

Por lo expuesto,

SUPLICO AL TRIBUNAL

que, por presentado este escrito con los documentos anejos y copia de todo ello, se sirva admitir uno y otros, me tenga por comparecido/a y parte en la representación que ostento de D./Dña. [NOMBRE Y APELLIDOS DEL EJECUTANTE], entendiéndose conmigo las ulteriores diligencias, y por solicitada la acumulación de ejecuciones, se comunique por el medio más rápido a la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº], y, seguido que sea el oportuno procedimiento, se acuerde la acumulación de la Ejecución de Título Judicial n.º [Nº DE PROCEDIMIENTO] de que conoce aquél a la Ejecución de estos autos, formulando requerimiento de acumulación, a fin de que se siga un solo proceso ejecutivo para la satisfacción a D./Dña. [NOMBRE Y APELLIDOS DEL OTRO EJECUTANTE], ejecutante en estos autos, y a mi representado, por [DENOMINACIÓN SOCIAL DEL EJECUTADO], de la suma acumulada de ambos procedimientos, es decir, [IMPORTE] euros de principal, más [IMPORTE] euros que se tienen presupuestados para intereses y costas de los procedimientos ejecutivos.

Por ser de Justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Abogado/a: [FIRMA] Firma del Procurador/a: [FIRMA]
