---
name: escrito-comunica-actos-violencia-genero-seccion-civil-civ-2707
description: "Escrito que comunica actos de violencia de género a la Sección Civil a efectos de inhibición. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito que comunica actos de violencia de género a la Sección Civil a efectos de inhibición

> Formulario **CIV-2707** del plugin **Escritos de trámite en el proceso civil** (`formularios-escritos-de-tramite-civiles`) · Civil › Escritos procesales (demanda, contestación, prueba, vista) · normativa revisada el 25-11-2026.

## Qué es

Escrito dirigido a la Sección Civil del Tribunal de Instancia, por el que se ponen en su conocimiento actos de violencia de género y se solicita se acuerde la inhibición del conocimiento del proceso a favor de la Sección de Violencia sobre la Mujer.

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito que comunica actos de violencia de género a la Sección Civil a efectos de inhibición» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito que comunica actos de violencia de género a la Sección Civil a efectos de inhibición” para mi caso». También puedes invocarla directamente con `/formularios-escritos-de-tramite-civiles:escrito-comunica-actos-violencia-genero-seccion-civil-civ-2707`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-escritos-de-tramite-civiles:indice`.

## Qué contiene esta skill

- `SKILL.md` (este fichero): qué es el formulario, para qué sirve, cómo se usa, los datos que pide, las normas que cita, los avisos de actualización y las instrucciones para Claude.
- `assets/formulario.md`: el formulario seco, tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…]. Es el texto que se rellena; no lleva explicaciones.
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Escritos de trámite en el proceso civil) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] NÚMERO (4 veces)
- [ ] FECHA (2 veces)
- [ ] COMPLETAR
- [ ] DESCRIBIR
- [ ] LUGAR
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] Nº DE COLEGIADO/A
- [ ] SEDE
- [ ] ÓRGANO

## Normas que cita el formulario

- art. 49 bis LEC
- art. 89.7 Ley Orgánica 6/1985

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [NÚMERO]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «… Violencia sobre la Mujer del Tribunal de Instancia, plaza n.º [NÚMERO], de esta»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Notas al pie del formulario original:
(1) El art. 89.6 LOPJ recoge las competencias civiles de las Secciones de Violencia sobre la Mujer de los Tribunales de Instancia, cuando concurran simultáneamente los requisitos enunciados en el art. 89.7 LOPJ.

(2) Conforme al número 7 del art. 2 de la Ley 27/2003, de 31 de julio, reguladora de la Orden de Protección de las víctimas de violencia doméstica: "Las medidas de naturaleza civil deberán ser solicitadas por la víctima o su representante legal, o bien por el Ministerio Fiscal cuando existan hijos menores o incapaces, siempre que no hubieran sido previamente acordadas por un órgano del orden jurisdiccional civil, y sin perjuicio de las medidas previstas en el art. 158 del Código Civil. Estas medidas podrán consistir en la atribución del uso y disfrute de la vivienda familiar, determinar el régimen de custodia, visitas, comunicación y estancia con los hijos, el régimen de prestación de alimentos, así como cualquier disposición que se considere oportuna a fin de apartar al menor de un peligro o de evitarle perjuicios. Las medidas de carácter civil contenidas en la orden de protección tendrán una vigencia temporal de 30 días. Si dentro de este plazo fuese incoado a instancia de la víctima o de su representante legal un proceso de familia ante la jurisdicción civil las medidas adoptadas permanecerán en vigor durante los treinta días siguientes a la presentación de la demanda. En este término las medidas deberán ser ratificadas, modificadas o dejadas sin efecto por el juez de primera instancia que resulte competente".

El Real Decreto 1309/2007 de 5 de octubre (BOE 23 de octubre), en la línea de actuación política de constitución de nuevos Juzgados, con la finalidad de que la planta judicial sea idónea para atender las necesidades de la Administración de Justicia, y garantizar a los ciudadanos la efectividad de la protección judicial de sus derechos, dispone la creación de 11 nuevos Juzgados de violencia sobre la mujer que entrarán en funcionamiento el 28 de diciembre de 2007. Con estas nuevas unidades judiciales se avanza el cumplimiento de la programación acordada para el año 2007, que se estableció en razón del volumen de litigiosidad de los órganos judiciales en funcionamiento y atendiendo a las disponibilidades presupuestarias.


### Flujo

1. **Paso 0**: comprueba Jurisprudenciator (arriba).
2. Lee entero `assets/formulario.md` (el formulario que vas a rellenar, en la carpeta de esta skill) y la parte de `../indice/marco.md` que afecte al caso. Limítate a la materia de este formulario: no añadas contenido ajeno a él.
3. Pide los datos de la lista en una sola tanda. Si un dato aparece varias veces, aclara a qué persona o acto corresponde cada vez. Lo que el usuario no sepa se queda como hueco visible con su etiqueta (p. ej. [FECHA]).
4. Resuelve cada [ELEGIR …] y cada [OPCIONAL …] según los hechos, y sustituye cualquier indicación entre paréntesis del formulario («(se describirá…)», «(indicar…)») por el contenido que corresponda. Redacta las partes que dependen del caso (hechos, motivos, descripción de bienes).
5. Aplica los avisos de actualización en el lugar que indican. Comprueba con `buscar_articulo` cada norma citada; si alguna ha cambiado, usa la redacción vigente. Si citas jurisprudencia, localízala con `buscar_sentencias` o `buscar_por_cita` y léela con `leer_sentencias`.
6. Antes de entregarlo, pasa `verificar_escrito` con las frases que citan normas o sentencias y corrige lo que señale.
7. **Documento final = el formulario tal cual, rellenado y limpio.**
   - Empieza exactamente por la primera línea de `assets/formulario.md` y sigue su estructura y su orden hasta la firma.
   - No pongas en el documento título, nombre del formulario o de la skill, código, encabezados, «Para qué sirve», leyendas, avisos, notas de uso, comentarios ni explicaciones. Tampoco marcas [ELEGIR…] u [OPCIONAL…]: ya están resueltas.
   - Formato Word (.docx, con la skill de Word disponible): **Times New Roman 11 pt** en todo el documento, **interlineado 1,15**, **texto justificado**, márgenes de 2,5 cm. Los rótulos del formulario (REUNIDOS, CLÁUSULAS, HECHOS, SUPLICO…) en su propia línea y en negrita, sin cambiar su texto.
8. En el chat (nunca dentro del documento): datos pendientes, partes redactadas por ti, normas y sentencias comprobadas con Jurisprudenciator (y, si algún dato sale de internet, cuál y su enlace) y, si es un escrito judicial o administrativo, el plazo y el órgano ante el que se presenta.

El resultado es un borrador para que lo revise un profesional antes de usarlo.
