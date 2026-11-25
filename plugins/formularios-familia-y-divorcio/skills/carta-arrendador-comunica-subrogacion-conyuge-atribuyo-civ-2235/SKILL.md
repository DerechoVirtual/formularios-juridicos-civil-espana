---
name: carta-arrendador-comunica-subrogacion-conyuge-atribuyo-civ-2235
description: "Carta al arrendador que comunica la subrogación del cónyuge al que se atribuyó la vivienda familiar. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Carta al arrendador que comunica la subrogación del cónyuge al que se atribuyó la vivienda familiar

> Formulario **CIV-2235** del plugin **Familia: separación, divorcio y medidas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 25-11-2026.

## Qué es

Carta dirigida al arrendatario de vivienda comunicándole la subrogación del cónyuge al que ha resultado atribuida la vivienda familiar en virtud de sentencia firme recaída en procedimiento de separación, divorcio o nulidad matrimonial.

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Carta al arrendador que comunica la subrogación del cónyuge al que se atribuyó la vivienda familiar» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Carta al arrendador que comunica la subrogación del cónyuge al que se atribuyó la vivienda familiar” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:carta-arrendador-comunica-subrogacion-conyuge-atribuyo-civ-2235`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- `SKILL.md` (este fichero): qué es el formulario, para qué sirve, cómo se usa, los datos que pide, las normas que cita, los avisos de actualización y las instrucciones para Claude.
- `assets/formulario.md`: el formulario seco, tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…]. Es el texto que se rellena; no lleva explicaciones.
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: separación, divorcio y medidas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] COMPLETAR (4 veces)
- [ ] FECHA (3 veces)
- [ ] NÚMERO (2 veces)
- [ ] CALLE
- [ ] PISO
- [ ] PUERTA

## Normas que cita el formulario

- art. 15 Ley 29/1994
- art. 90 Código Civil

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

- Junto a «… de Instancia [ELEGIR: SECCIÓN CIVIL / SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD]»: Denominación legal: Sección de Familia, Infancia y Capacidad. Si no existe en el partido, conoce la Sección Civil o la Única (art. 86.3-4 LOPJ). Fuente: LOPJ arts. 84.2.a) y 86 (redacc. LO 1/2025, BOE-A-2025-76).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Notas al pie del formulario original:
(1) SOLICITUD DE NOTIFICACIÓN DE LA ATRIBUCIÓN DEL USO DE LA VIVIENDA ARRENDADA POR EL CÓNYUGE NO TITULAR

Cuando la atribución del uso se realiza respecto de una vivienda que se encuentra arrendada y se otorga el uso al cónyuge no titular del contrato de arrendamiento hay que tener en cuenta el artículo 12, relativo al desistimiento y vencimiento en caso de matrimonio o convivencia del arrendatario y el artículo 15, al referirse a los efectos de la separación, divorcio o nulidad del matrimonio del arrendatario, ambos de la Ley de Arrendamientos Urbanos..

Este último, permite la continuidad en el arrendamiento del cónyuge que no es titular del contrato cuando judicialmente se le ha concedido el uso y disfrute de la vivienda familiar, siempre que se reúnan los siguientes requisitos:

1. La existencia de una resolución judicial que contenga un pronunciamiento en el que se acuerde conceder el uso y disfrute de la vivienda familiar al cónyuge no titular.
2. La notificación de la resolución judicial al arrendador. Esta notificación ha de ser fehaciente, es decir, por cualquier medio que permita dejar constancia de su realización (vía notarial, correo certificado con acuse de recibo, haciendo constar en la tarjeta de éste el hecho de la notificación, acto de conciliación, por vía de ejecución ...).
3. Que la notificación se practique dentro del plazo de dos meses desde que fue notificada la resolución judicial al cónyuge no titular.
4. Que se acompañe al requerimiento copia de la resolución judicial o de la parte de la misma que afecte al uso de la vivienda. No es necesario acompañar el contenido íntegro de la resolución, sino sólo la parte dispositiva en que se acuerde la concesión del derecho sobre el uso de la vivienda.

La notificación podrá solicitarse que se realice a través del Tribunal, pero el hecho de que se limite su práctica al plazo de dos meses puede dar lugar a que no se realice dentro del mismo haciendo peligrar su eficacia.


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
