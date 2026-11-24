---
name: oposicion-juicio-cambiario-indebida-acumulacion-accion-civ-1184
description: "Oposición en juicio cambiario por indebida acumulación de la acción cambiaria y la del contrato caus. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Oposición en juicio cambiario por indebida acumulación de la acción cambiaria y la del contrato caus

> Formulario **CIV-1184** del plugin **Cobrar deudas: monitorio y cambiario** (`formularios-reclamar-deudas-monitorio`) · Civil › Monitorio y cambiario · normativa revisada el 24-11-2026.

## Qué es

Oposición a juicio cambiario alegando que no procede la acumulación de acciones pretendida pues la acción acumulada, cumplimiento del contrato causal de la emisión de las letras de cambio, debe ventilarse en juicio ordinario y no en juicio cambiario.

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Oposición en juicio cambiario por indebida acumulación de la acción cambiaria y la del contrato caus» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Oposición en juicio cambiario por indebida acumulación de la acción cambiaria y la del contrato caus” para mi caso». También puedes invocarla directamente con `/formularios-reclamar-deudas-monitorio:oposicion-juicio-cambiario-indebida-acumulacion-accion-civ-1184`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-reclamar-deudas-monitorio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Cobrar deudas: monitorio y cambiario) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE DE LA PARTE (3 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] DESCRIPCIÓN DEL BIEN (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] AÑO
- [ ] C.P.
- [ ] CALLE
- [ ] COLEGIO
- [ ] FECHA
- [ ] LOCALIDAD
- [ ] NIF
- [ ] Nº DE DOCUMENTO
- [ ] SEDE

## Normas que cita el formulario

- art. 819 LEC
- art. 73.1.2.º LEC

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

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales y de D./Dña. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], código postal [C.P.], calle [CALLE], n.º [NÚMERO], CIF n.º [NIF], y las demás circunstancias constan en la escritura de poder inscrito en el Registro Electrónico de Apoderamientos Judiciales, a cuya justificación aporto certificación de dicho Registro como documento nº [Nº DE DOCUMENTO], bajo la dirección del Letrado ejerciente D./Dña. [NOMBRE Y APELLIDOS], colegiado n.º [NÚMERO] del Iltre. Colegio de Abogados de [COLEGIO], ante el Tribunal en autos de Juicio Cambiario n.º [NÚMERO]/[AÑO], a instancias de [NOMBRE DE LA PARTE], comparezco, y como mejor en Derecho proceda, DIGO:

Que habiéndose dado traslado del Auto de [FECHA], por el que se requiere por [NOMBRE DE LA PARTE], para pago en plazo de diez días, se deduce en tiempo y forma OPOSICIÓN AL JUICIO CAMBIARIO, de conformidad con los siguientes hechos y fundamentos de derecho.

HECHOS

PREVIO.- INADMISIBILIDAD DE LA ACUMULACIÓN DE ACCIONES PRETENDIDA.

La parte actora ejercita frente a nuestra representado una acción cambiaria por impago de dos letras de cambio, y simultáneamente, en el mismo proceso, una acción de cumplimiento del contrato causal de compraventa de [DESCRIPCIÓN DEL BIEN], suscrito entre partes, y para cuyo pago de precio en plazos consecutivos se instrumentaron, entre otras, las dos letras del caso.

Se aduce que el impago de dos cambiales a su vencimiento era suficiente para dar por resuelto el contrato de compraventa, con pérdida de las cantidades pagadas y recuperando [NOMBRE DE LA PARTE],. la propiedad y posesión de [DESCRIPCIÓN DEL BIEN], o para exigir el cumplimiento del contrato en todos sus términos, a elección de la parte vendedora.

Por ello, a la suma de [IMPORTE] euros que se reclama por impago del principal de la cambial, gastos de devolución, intereses y costas, se añade como reclamado por el suplico de la demanda la suma de [IMPORTE] euros, que se pide con el interés legal del dinero más dos puntos desde la fecha de interposición de la presente demanda y costas, por el resto del precio aplazado de la compraventa.

Es evidente que no procede la acumulación de acciones a este juicio cambiario. El ejercicio de la acción entablada a tenor del art. 819 LEC en relación con el art. 49, párrafo 2.º de la Ley Cambiaria y del Cheque, corresponde al juicio cambiario, según los arts. 819 y ss. LEC, mientras que el cumplimiento del contrato causal de la emisión de las letras de cambio, sin especialidad por materia, corresponde dilucidarse a través de un juicio ordinario por la cuantía (arts. 248 y 249.2 LEC).

Con arreglo al art. 73.1.2.º LEC, para que sea admisible la acumulación de acciones es preciso que las acumuladas no deban, por razón de la materia, ventilarse en juicios de diferente tipo, siendo el cambiario juicio especial, de sumariedad discutible, mientras que el ordinario es un juicio plenario común.

PRIMERO.-

========================================================================
