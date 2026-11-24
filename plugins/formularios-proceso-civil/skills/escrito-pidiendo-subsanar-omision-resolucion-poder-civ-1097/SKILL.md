---
name: escrito-pidiendo-subsanar-omision-resolucion-poder-civ-1097
description: "Escrito pidiendo subsanar la omisión de una resolución para poder cumplirla. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito pidiendo subsanar la omisión de una resolución para poder cumplirla

> Formulario **CIV-1097** del plugin **Proceso civil: demandas, contestaciones, prueba y vista** (`formularios-proceso-civil`) · Civil › Escritos procesales (demanda, contestación, prueba, vista) · normativa revisada el 24-11-2026.

## Qué es

Escrito de parte instando la subsanación de la omisión de que adolece la resolución para poder llevarla plenamente a efecto.

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito pidiendo subsanar la omisión de una resolución para poder cumplirla» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito pidiendo subsanar la omisión de una resolución para poder cumplirla” para mi caso». También puedes invocarla directamente con `/formularios-proceso-civil:escrito-pidiendo-subsanar-omision-resolucion-poder-civ-1097`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-proceso-civil:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Proceso civil: demandas, contestaciones, prueba y vista) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE DEL MENOR (5 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] FECHA (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] AÑO
- [ ] LUGAR
- [ ] Nº DE PROCEDIMIENTO
- [ ] SEDE

## Normas que cita el formulario

- art. 215.1 LEC
- art. 267 LOPJ
- art. 145 CC
- art. 214 LEC

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

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, que actúa en representación de D./Dña. [NOMBRE Y APELLIDOS], demandado en autos de Juicio Verbal n.º [Nº DE PROCEDIMIENTO]/[AÑO], instado por la actora Don/Doña [NOMBRE Y APELLIDOS], en representación legal de sus hijos menores en potestad [NOMBRE DEL MENOR], [NOMBRE DEL MENOR] y [NOMBRE DEL MENOR], comparezco y como mejor en Derecho proceda, DIGO:

Que por medio del presente escrito, y de conformidad con las previsiones del art. 215.1 LEC, por relación al art. 267 LOPJ, vengo a deducir solicitud de SUBSANACIÓN de sentencia, con base en las siguientes

ALEGACIONES

Primera

Ha sido notificada a esta parte sentencia de fecha [FECHA], dictada en los autos de referencia, por la que se declara la obligación de prestar alimentos en cuantía de [IMPORTE] yy [IMPORTE] euros mensuales a cada uno de los nietos de mi mandante, [NOMBRE DEL MENOR] y Z [NOMBRE DEL MENOR], y condena al pago a la ‘parte demandada’.

Segunda

Si bien la sentencia accede, acogiendo los argumentos de esta parte vertidos en el acto de la vista, a reducir drásticamente las cantidades que se solicitaban, el caso es que la condena no determina la proporción en que dichas pensiones alimenticias deben abonarse por los dos codemandados, habida cuenta que D./Dña. [NOMBRE Y APELLIDOS], ex esposa de mi patrocinado no asistió al juicio y fue declarada rebelde, siendo la obligación alimenticia mancomunada divisible, que tiene que repartirse conforme a los medios de fortuna de cada alimentante, en razón del art. 145 CCiv (Sentencia de la Audiencia Provincial de Asturias, Sección 6ª, de 18 Feb. 1999, Rec. 471/1998, Sentencia de la Audiencia Provincial de Sevilla, Sección 2ª, 20/2000 de 13 Ene. 2000, Rec. 2768/1999, Sentencia de la Audiencia Provincial de Vizcaya, Sección 4ª, 559/2004 de 12 Jul. 2004, Rec. 809/2003 o la Sentencia de la Audiencia Provincial de Barcelona, Sección 12ª, 529/2008 de 18 Jul. 2008, Rec. 65/2008), salvo anticipo del todo excepcional por urgente necesidad y circunstancias especiales.

La fijación de la proporción es carga de quien pretende, una vez aquilatado el caudal de cada alimentante demandado por la prueba en juicio, y es deber de congruencia de la sentencia.

Tercera

Según previene el art. 215.1 LEC, las omisiones o defectos de que pudieran adolecer sentencias y autos, y que fuere necesario remediar para llevar plenamente a efecto dichas resoluciones, podrán ser subsanados, mediante Auto, en los mismos plazos y por el mismo procedimiento establecido en el art. 214 LEC, es decir, a excitación de parte, como es caso, dentro de los dos días siguientes a la de notificación.

Por todo lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito, junto con el resguardo acreditativo de haber trasladado copia del mismo a la otra parte comparecida, se digne admitirlo, y en mérito a lo manifestado, proceda a subsanar la omisión de que adolece la sentencia, determinando la proporción en que deben contribuir al pago de las pensiones alimenticias objeto de la condena cada una de las partes codemandadas.

Es justicia de hacerse en [LUGAR], a [FECHA].

Firma del Abogado	Firma del Procurador/a

========================================================================
