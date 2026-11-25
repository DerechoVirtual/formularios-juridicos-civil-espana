---
name: reclamacion-extrajudicial-previa-conductor-circulaba-civ-2624
description: "Reclamación extrajudicial previa al conductor que circulaba sin seguro. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Reclamación extrajudicial previa al conductor que circulaba sin seguro

> Formulario **CIV-2624** del plugin **Accidentes, seguros y responsabilidad civil** (`formularios-accidentes-y-responsabilidad-civil`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 25-11-2026.

## Qué es

Escrito de reclamación previa a la reclamación de cantidad contra el conductor del vehículo que carecía de seguro de responsabilidad civil obligatorio en accidente de circulación. Corresponde al Consorcio de Compensación de Seguros la indemnización por los daños ocasionados hasta el límite cuantitativo del aseguramiento obligatorio.

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Reclamación extrajudicial previa al conductor que circulaba sin seguro» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Reclamación extrajudicial previa al conductor que circulaba sin seguro” para mi caso». También puedes invocarla directamente con `/formularios-accidentes-y-responsabilidad-civil:reclamacion-extrajudicial-previa-conductor-circulaba-civ-2624`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-accidentes-y-responsabilidad-civil:indice`.

## Qué contiene esta skill

- `SKILL.md` (este fichero): qué es el formulario, para qué sirve, cómo se usa, los datos que pide, las normas que cita, los avisos de actualización y las instrucciones para Claude.
- `assets/formulario.md`: el formulario seco, tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…]. Es el texto que se rellena; no lleva explicaciones.
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Accidentes, seguros y responsabilidad civil) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] COMPLETAR (4 veces)
- [ ] IMPORTE (3 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] FECHA (2 veces)
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] NOMBRE Y APELLIDOS
- [ ] NÚMERO

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

### Avisos de actualización (1) — se aplican en el texto, nunca se copian en el documento

- Al principio del formulario: Antes de demandar al Consorcio debe intentarse además un medio adecuado de solución de controversias o actividad negociadora (art. 5 LO 1/2025), salvo para la demanda ejecutiva (art. 5.3).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Escrito de reclamación previa a la reclamación de cantidad contra el conductor del vehículo que carecía de seguro de responsabilidad civil obligatorio en accidente de circulación. Corresponde al Consorcio de Compensación de Seguros la indemnización por los daños ocasionados hasta el límite cuantitativo del aseguramiento obligatorio.

Notas al pie del formulario original:
(1) El texto refundido de la Ley sobre Responsabilidad Civil y Seguro en la Circulación de Vehículos a Motor, establece en su artículo 11 una serie de supuestos en los que la obligación de indemnizar, en las condiciones previstas en esta Ley y sólo hasta los límites del aseguramiento obligatorio, corresponde al Consorcio de Compensación de Seguros. Entre esos supuestos destacamos los siguientes:

a) (letra e del art. 11.1) Indemnizar los daños a las personas y en los bienes cuando la entidad española aseguradora del vehículo con estacionamiento habitual en España hubiera sido declarada judicialmente en concurso o, habiendo sido disuelta y encontrándose en situación de insolvencia, estuviera sujeta a un procedimiento de liquidación intervenida o ésta hubiera sido asumida por el propio Consorcio de Compensación de Seguros.

b) (letra c del art. 11.1) Indemnizar los daños, a las personas y en los bienes, ocasionados en España por un vehículo que esté asegurado y haya sido objeto de robo o robo de uso. El artículo 8 del Reglamento del seguro obligatorio de responsabilidad civil en la circulación de vehículos a motor, excluye de la cobertura del seguro obligatorio de los daños a las personas y en los bienes causados por un vehículo robado, entendiéndose por tal la conducta tipificada como robo y robo de uso en los artículos 237 y 244.

c) (letra b.i del art. 11.1) Indemnizar los daños en las personas y en los bienes, ocasionados con un vehículo que tenga su estacionamiento habitual en España, así como los ocasionados dentro del territorio español a personas con residencia habitual en España o a bienes de su propiedad situados en España con un vehículo con estacionamiento habitual en un tercer país no firmante del Acuerdo entre las oficinas nacionales de seguros de los Estados miembros del Espacio Económico Europeo y de otros Estados asociados, en ambos casos cuando dicho vehículo no esté asegurado.

d) (letra a del art. 11.1) Indemnizar a quienes hubieran sufrido daños en sus personas, por siniestros ocurridos en España, en aquellos casos en que el vehículo causante sea desconocido. No obstante, si como consecuencia de un accidente causado por un vehículo desconocido se hubieran derivado daños personales significativos, el Consorcio de Compensación de Seguros habrá de indemnizar también los eventuales daños en los bienes derivados del mismo accidente. En este último caso, podrá fijarse reglamentariamente una franquicia no superior a 500 euros. Se consideran daños personales significativos la muerte, la incapacidad permanente o la incapacidad temporal que requiera, al menos, una estancia hospitalaria superior a tres días.

El Consorcio de Compensación de Seguros ajustará su actividad al Ordenamiento Jurídico Privado, según dispone su Estatuto aprobado por Real Decreto Legislativo 7/2004, de 29 de octubre. En consecuencia, la reclamación judicial que deba efectuarse ante este organismo no se efectuará ante la Jurisdicción Contencioso-Administrativa, sino ante la Civil.

Por ello, la indemnización derivada de un accidente de circulación deberá reclamarse por los trámites del juicio declarativo civil que corresponda por cuantía, con las especialidades previstas en el artículo 20.b) de su Estatuto, que obliga a acreditar fehacientemente que el Consorcio fue requerido judicial o extrajudicialmente de pago, y que desde dicho requerimiento transcurrió un plazo de tres meses sin haber sido atendido. Los formularios siguientes contienen modelos de reclamación previa a presentar al Consorcio de Compensación, cuya copia sellada por dicho organismo deberá acompañarse a la demanda de juicio declarativo (formularios "Demanda de juicio ordinario en reclamación de cantidad contra el causante de un vehículo que conducía careciendo de seguro" al "Demanda de juicio ordinario en reclamación de cantidad contra el conductor de un vehículo, cuya compañía aseguradora fue declarada en concurso o, habiendo sido disuelta y encontrándose en situación de insolvencia, estuviese sujeta a un procedimiento de liquidación intervenida o esta hubiera sido asumida por el Consorcio de Compensación de Seguros")

Por otro lado, cuando habiendo finalizado un procedimiento penal sin sentencia condenatoria, si se dictó auto de cuantía máxima (art. 13 del texto refundido) y la indemnización corresponde al Consorcio de Compensación de Seguros, al interponer la demanda ejecutiva (art. 517.2.8.º LEC), de conformidad con el artículo 20.b) de su Estatuto, deberemos acreditar fehacientemente que el Consorcio fue requerido judicial o extrajudicialmente de pago, y que desde dicho requerimiento transcurrió un plazo de tres meses sin haber sido atendido (formulario "Escrito de demanda formulado por el titular de un auto ejecutivo con cargo al Seguro Obligatorio del Automóvil (SOA)").

(2) Ver formulario "Demanda de juicio ordinario en reclamación de cantidad contra el causante de un vehículo que conducía careciendo de seguro"


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
