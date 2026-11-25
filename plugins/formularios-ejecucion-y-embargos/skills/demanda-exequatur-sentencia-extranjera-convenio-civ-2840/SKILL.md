---
name: demanda-exequatur-sentencia-extranjera-convenio-civ-2840
description: "Demanda de exequátur de sentencia extranjera del Convenio de Bruselas con averiguación de bienes. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de exequátur de sentencia extranjera del Convenio de Bruselas con averiguación de bienes

> Formulario **CIV-2840** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 25-11-2026.

## Qué es

Demanda de reconocimiento y ejecución en España de sentencia extranjera dentro del ámbito del Convenio de Bruselas, solicitando la averiguación de bienes de la ejecutada. El Convenio de Bruselas fue sustituido progresivamente por el Reglamento (CE) n.º 44/2001, y actualmente por el Reglamento (UE) n.º 1215/2012 (conocido como Bruselas I bis), aplicable a acciones judiciales ejercitadas a partir del 10 de enero de 2015. A pesar de haber sido derogado por los reglamentos, el Convenio de 1968 sigue siendo aplicable en territorios de ultramar de ciertos Estados miembros que están excluidos del ámbito territorial de los Reglamentos (según el antiguo artículo 299 del Tratado CE).

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de exequátur de sentencia extranjera del Convenio de Bruselas con averiguación de bienes» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de exequátur de sentencia extranjera del Convenio de Bruselas con averiguación de bienes” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:demanda-exequatur-sentencia-extranjera-convenio-civ-2840`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- `SKILL.md` (este fichero): qué es el formulario, para qué sirve, cómo se usa, los datos que pide, las normas que cita, los avisos de actualización y las instrucciones para Claude.
- `assets/formulario.md`: el formulario seco, tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…]. Es el texto que se rellena; no lleva explicaciones.
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (14 veces)
- [ ] COMPLETAR (13 veces)
- [ ] FECHA (6 veces)
- [ ] Nº DE DOCUMENTO (4 veces)
- [ ] NÚMERO (3 veces)
- [ ] CALLE (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] PARTE DEMANDADA (2 veces)
- [ ] DENOMINACIÓN SOCIAL
- [ ] ESTADO MIEMBRO DE ORIGEN
- [ ] LUGAR
- [ ] NACIONALIDAD
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] NOMBRE Y APELLIDOS
- [ ] Nº DE PROCEDIMIENTO
- [ ] SEDE

## Normas que cita el formulario

- art. 545.3 LEC
- art. 538 LEC
- art. 539.1 LEC
- art. 549.1 LEC
- art. 575 LEC
- art. 590 LEC
- art. 5.3 Ley Orgánica 1/2025
- art. 576 LEC
- art. 539.2 LEC

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

### Avisos de actualización (3) — se aplican en el texto, nunca se copian en el documento

- Al principio del formulario: Rehecho: el Convenio de Bruselas de 1968 fue sustituido entre Estados miembros por el Reglamento (CE) 44/2001 y este por el Reglamento (UE) 1215/2012, que suprime el exequátur para acciones ejercitadas desde el 10-1-2015; la ejecución se pide directamente con la resolución y el certificado del art. 53.
- Junto a «… ejecución se pide directamente con la resolución y el certificado del art. 53.]»: Se suprime la nota de MASC: no es preciso para la demanda ejecutiva (art. 5.3 LO 1/2025). Para resoluciones de acciones anteriores al 10-1-2015 (Reglamento 44/2001), de Estados no miembros (Convenio de Lugano u otros) o de territorios del art. 68 del Reglamento, este modelo no sirve sin adaptarlo.
- Junto a «… de territorios del art. 68 del Reglamento, este modelo no sirve sin adaptarlo.]»: La competencia territorial se razona con el art. 545.3 LEC, porque la DF 25.ª LEC no fija un fuero propio para la ejecución; revísese en cada caso. El nombre del formulario («convenio de Bruselas») debe actualizarse.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Notas al pie del formulario original:
(1) Este modelo sirve para ejecutar en España resoluciones dictadas en otro Estado miembro de la Unión Europea en acciones judiciales ejercitadas a partir del 10 de enero de 2015 (Reglamento (UE) n.º 1215/2012), que se ejecutan sin necesidad de declaración de fuerza ejecutiva (exequátur).

Para las resoluciones dictadas a raíz de acciones ejercitadas antes de esa fecha sigue aplicándose el Reglamento (CE) n.º 44/2001 (artículo 66.2 del Reglamento (UE) n.º 1215/2012), que exige la previa declaración de ejecutividad. El Convenio de Bruselas de 1968 solo subsiste respecto de los territorios de los Estados miembros excluidos del Reglamento en virtud del artículo 355 del Tratado de Funcionamiento de la Unión Europea (artículo 68 del Reglamento). Para resoluciones de Estados que no son miembros de la Unión se estará al convenio internacional aplicable o, en su defecto, al exequátur de los artículos 41 y siguientes de la Ley 29/2015, de 30 de julio, de cooperación jurídica internacional en materia civil.


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
