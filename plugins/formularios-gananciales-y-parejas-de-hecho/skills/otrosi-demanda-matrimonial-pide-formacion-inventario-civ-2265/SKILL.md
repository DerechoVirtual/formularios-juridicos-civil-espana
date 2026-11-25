---
name: otrosi-demanda-matrimonial-pide-formacion-inventario-civ-2265
description: "Otrosí de la demanda matrimonial que pide la formación de inventario de la comunidad. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Otrosí de la demanda matrimonial que pide la formación de inventario de la comunidad

> Formulario **CIV-2265** del plugin **Gananciales, regímenes económicos y parejas de hecho** (`formularios-gananciales-y-parejas-de-hecho`) · Civil › Familia · normativa revisada el 25-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Otrosí de la demanda matrimonial que pide la formación de inventario de la comunidad» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Otrosí de la demanda matrimonial que pide la formación de inventario de la comunidad” para mi caso». También puedes invocarla directamente con `/formularios-gananciales-y-parejas-de-hecho:otrosi-demanda-matrimonial-pide-formacion-inventario-civ-2265`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-gananciales-y-parejas-de-hecho:indice`.

## Qué contiene esta skill

- `SKILL.md` (este fichero): qué es el formulario, para qué sirve, cómo se usa, los datos que pide, las normas que cita, los avisos de actualización y las instrucciones para Claude.
- `assets/formulario.md`: el formulario seco, tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…]. Es el texto que se rellena; no lleva explicaciones.
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Gananciales, regímenes económicos y parejas de hecho) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] COMPLETAR
- [ ] FECHA
- [ ] LUGAR
- [ ] NOMBRE Y APELLIDOS

## Normas que cita el formulario

- art. 1316 Código Civil
- art. 1344 CC

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

Notas al pie del formulario original:
(1) De los arts. 90 e), 91 y 95 C.C. se desprende que una de las consecuencias mediatas anudadas a las sentencias de separación, divorcio o nulidad, es la disolución y posterior liquidación del régimen económico, sin que, por lo mismo, con precedencia a dicho pronunciamiento estos efectos puedan acordarse como medidas previas o coetáneas, autorizándose únicamente la adopción de otras actuaciones meramente preventivas o precautorias -arts. 103 y 104 C.C.-.

La liquidación es, también, la derivación última del procedimiento -con o sin efectiva contradicción (arg. exart. 1394 C.C.- directamente encaminado a que se extinga o declare disuelto el régimen económico conyugal de acuerdo con lo establecido en la legislación civil aplicable, sin que el pronunciamiento jurisdiccional deba concernir, al propio tiempo, al vínculo matrimonial -v. gr., art. 1393, 1.º, 2.º y 4.º C.C.-.

Lo que parece no contemplar la LEC 1/2000 es la promoción de un litigio exclusivamente encaminado a liquidar el régimen económico matrimonial sin que exista desacuerdo entre los cónyuges a propósito de la extinción o disolución del hasta entonces existente, por convención o determinación legal, o por haberse disuelto aquél sin necesidad de pronunciamiento judicial que lo declare -fallecimiento del otro cónyuge- ni, en consecuencia, que se pueda interesar, junto con la demanda rectora de dicho proceso, la formación del inventario a que se refiere este precepto como medida de garantía.

Repárese que en cualquier momento, sea cual fuere el sistema matrimonial al que los cónyuges hayan decidido acogerse al inicio de su unión, pueden pactar que en adelante se disciplinen de modo distinto las relaciones económicas entre ambos, centrándose la controversia únicamente sobre los resultados del régimen extinguido (v. gr., art. 1392, 4.º C.C.). A su vez, el conflicto puede suscitarse entre el cónyuge supérstite y los herederos del premuerto con ocasión de liquidar el régimen extinguido ipso iure -y sin necesidad de resolución judicial- por el fallecimiento de la esposa o del marido.

La disposición contenida en el apdo. 1 del artículo 808 LEC 1/2000 debe entenderse, pues, completada también, con la referencia, deplorablemente omitida, a la demanda en que se solicite simple y exclusivamente la liquidación del régimen económico conyugal extrajudicialmente disuelto.

Problema distinto es el relativo a cuáles sean los bienes o derechos y, en su caso, deudas, cargas y responsabilidades que hayan de incluirse en el inventario y que vendrán determinados, en cada caso, por la disciplina sustantiva rectora del régimen económico de que se trate -vid., señaladamente, art. 1394 y Comentario al art. 811 LEC 1/2000-, y a la que habrá de atenerse la propuesta que necesariamente deberá presentar el solicitante a la luz del apdo. 2, junto con la correspondiente documentación.

Presentada la solicitud de liquidación junto con la propuesta unilateral de inventario -valorado, pese al silencio de la norma- y el oportuno soporte documental, por diligencia de Ordenación del Secretario, se citará a comparecencia a los cónyuges, o, en su caso, al solicitante y a los causahabientes del premuerto.


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
