---
name: oposicion-apelacion-motivos-procesales-materia-trafico-civ-1388
description: "Oposición a la apelación por motivos procesales en materia de tráfico. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Oposición a la apelación por motivos procesales en materia de tráfico

> Formulario **CIV-1388** del plugin **Recursos civiles: reposición, apelación, casación y queja** (`formularios-recursos-civiles`) · Civil › Recursos · normativa revisada el 24-11-2026.

## Qué es

Escrito de oposición al recurso de apelación interpuesto, basado en infracción procesal en la sentencia al considerar que el principio de prueba incumbe al actor en responsabilidad civil en materia de tráfico, y en infracciones de carácter material.

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Oposición a la apelación por motivos procesales en materia de tráfico» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Oposición a la apelación por motivos procesales en materia de tráfico” para mi caso». También puedes invocarla directamente con `/formularios-recursos-civiles:oposicion-apelacion-motivos-procesales-materia-trafico-civ-1388`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-recursos-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Recursos civiles: reposición, apelación, casación y queja) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] ASEGURADORA
- [ ] AÑO
- [ ] LUGAR
- [ ] Nº DE PROCEDIMIENTO

## Normas que cita el formulario

- art. 461.1 LEC
- art. 217.2 LEC
- art. 394.1 LEC
- art. 398.1 LEC
- art. 276 LEC

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

A LA AUDIENCIA PROVINCIAL DE [LOCALIDAD]

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales en nombre de D./Dña. [NOMBRE Y APELLIDOS], cuya representación tengo debidamente acreditada, ante la Sala comparezco en el juicio ordinario n.º [Nº DE PROCEDIMIENTO]/[AÑO] y, como mejor proceda en Derecho, DIGO:

Que dentro del plazo legal conferido al efecto por el Tribunal a esta parte mediante diligencia de ordenación de fecha [FECHA], formalizo escrito de oposición al recurso de apelación, con base en las siguientes

ALEGACIONES

PRESUPUESTO PROCESAL

Siendo por quien comparezco parte actora en el proceso, que ha obtenido sentencia parcialmente estimatoria, es procedente presentar ante el Tribunal el escrito de oposición al recurso de apelación interpuesto por la parte demandada aseguradora [ASEGURADORA], dentro del plazo de diez días, legitimada ex art. 461.1 LEC.

OPOSICIÓN SOBRE INFRACCIÓN PROCESAL EN SENTENCIA

Funda el recurso su denuncia de haberse vulnerado el principio de que la prueba incumbía al actor en el subjetivismo que debe imperar en la responsabilidad civil en materia de tráfico.

Dicha tesis olvida que nos hallamos ante un supuesto de lesiones personales, acogido al régimen que surgió de la Ley 122/1962 de 24 de diciembre, de Uso y Circulación de Vehículos de Motor, que desconectó de los principios heredados por nuestro Código Civil desde la "Lex Aquilia", e introdujo la responsabilidad civil objetivizada para el asegurador obligatorio, en tanto que preceptuó la obligación del asegurador de reparar los daños corporales causados con motivo de la circulación al perjudicado, hasta el límite cuantitativo vigente en cada momento, con fundamento en el riesgo de la circulación viaria y el principio de asegurabilidad, y no en la culpa, si bien el régimen del Código, subjetivista, se ha corregido también jurisprudencialmente hacia la objetivación.

En el ámbito del seguro obligatorio del automóvil, la reparación del perjudicado se busca a ultranza, y se ha creado un mecanismo de socialización del riesgo, en la actualidad contenido en el art. 1 del Texto refundido de la Ley sobre responsabilidad civil y seguro en la circulación de vehículos a motor, aprobado Real Decreto Legislativo 8/2004, de 29 de octubre ("objetivo atenuado" —STS de 12 de mayo de 1992 —, o "cuasi objetivo" —STS de 12 de julio de 1989 —).

Debe tenerse siempre en cuenta que, si ya en general el régimen de los arts. 1.902 y ss. CC viene asumiendo en la doctrina aplicativa de muchos ámbitos una prudencial responsabilidad por riesgo, en el ejercicio de la acción directa derivada del seguro obligatorio, opera siempre el mecanismo de inversión de la carga de la prueba, la exigencia de la acreditación exarcebada del agotamiento de la diligencia debida, y la prescindibilidad de que se hayan respetado los reglamentos de seguridad en la circulación viaria en orden a calificar, de forma que solo procede denegar la indemnización correspondiente cuando la aseguradora del vehículo productor del daño pruebe cumplidamente que el accidente ocurrió por culpa única, entendida como exclusiva y excluyente, de la víctima.

Consecuencia de lo anterior es que cualquier indeterminación en orden a la causa y circunstancias específicas del accidente necesariamente perjudicará a la aseguradora, y no a la víctima o derechohabientes, puesto que precisamente la atribución de la carga de la prueba no tiene otro efecto que hacer recaer las consecuencias adversas de su falta sobre la parte a quien corresponde la misma, de conformidad con la regla general del art. 217.2 LEC.

La utilización de vehículos a motor, de otra parte, supone generar un importante peligro para terceros usuarios de las vías públicas. En razón a ello, por una parte, se instaura el precitado sistema de responsabilidad cuasi objetivo y, por otro, se impone un régimen jurídico en la utilización de los vehículos a motor de la que se deriva la exigencia de un escrupuloso respeto de las normas de circulación y un control absoluto del vehículo, rigiendo el llamado principio de seguridad o conducción dirigida, formulado ahora en el artículo 10.2 de la Ley de Seguridad Vial, en virtud del cual el conductor debe utilizar el vehículo con la diligencia, precaución y atención necesarias para evitar todo daño, propio o ajeno, cuidando de no poner en peligro, tanto a sí mismo como a los demás ocupantes del vehículo y al resto de usuarios de la vía, especialmente a aquellos cuyas características les hagan más vulnerables. En aplicación de este principio, la jurisprudencia ha establecido que el mismo "obliga a prevenir, hasta donde humanamente es posible, el defectuoso comportamiento de los demás usuarios de la vía pública" (STS de 15 de octubre de 1977).

OPOSICIÓN SOBRE INFRACCIONES MATERIALES

/

COSTAS

Ha de desestimarse el recurso de apelación, por lo que las costas serán impuestas al recurrente, de conformidad con el art. 394.1 LEC, al que se remite el art. 398.1 LEC.

En virtud de cuanto antecede,

SUPLICO A LA SALA

Que, teniendo por presentado este escrito en tiempo y forma, que se ha trasladado en términos del art. 276 LEC al Procurador de la parte recurrente, se sirva admitirlo y tener por deducida OPOSICIÓN al recurso de apelación interpuesto por la parte demandada, y se remitan los autos a la Audiencia Provincial de [LOCALIDAD], previo emplazamiento legal para comparecer ante la misma, y

SUPLICO A LA AUDIENCIA PROVINCIAL que, seguido que sea el legal procedimiento, dicte sentencia que lo desestime íntegramente, confirmando la sentencia recurrida en todos sus extremos

Por ser de Justicia que pido en [LUGAR], a [FECHA].

Firma de Abogado/a	Firma de Procurador/a

========================================================================
