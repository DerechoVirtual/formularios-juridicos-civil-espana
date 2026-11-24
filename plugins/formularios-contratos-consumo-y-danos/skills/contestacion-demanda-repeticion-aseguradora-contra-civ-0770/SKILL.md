---
name: contestacion-demanda-repeticion-aseguradora-contra-civ-0770
description: "Contestación a la demanda de repetición de la aseguradora contra el asegurado. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contestación a la demanda de repetición de la aseguradora contra el asegurado

> Formulario **CIV-0770** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contestación a la demanda de repetición de la aseguradora contra el asegurado» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contestación a la demanda de repetición de la aseguradora contra el asegurado” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:contestacion-demanda-repeticion-aseguradora-contra-civ-0770`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (4 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] ASEGURADORA
- [ ] AÑO
- [ ] DÍA
- [ ] FUNDAMENTOS
- [ ] LUGAR
- [ ] MES
- [ ] Nº DE DOCUMENTO
- [ ] NÚMERO
- [ ] OTROS DATOS
- [ ] SEDE

## Normas que cita el formulario

- art. 394 LEC

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

- Junto a «…clarativo número [NÚMERO] A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

Proceso declarativo número [NÚMERO]

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

Don/Dª [NOMBRE Y APELLIDOS], Procurador de los Tribunales, en la representación que ostento de D [NOMBRE Y APELLIDOS], según acredito mediante escritura de poderes que acompaño para su unión a los autos mediante testimonio, previo cotejo y devolución del original, y bajo la dirección Letrada de Don [NOMBRE Y APELLIDOS] ante el Tribunal en el proceso declarativo arriba expresado comparezco y, como mejor proceda en Derecho, DIGO:

Que habiéndose dado traslado a esta parte de la demanda formulada por la aseguradora [ASEGURADORA] en ejercicio de la acción de repetición prevenida en el artículo el art. 10 del Texto Refundido de la Ley sobre responsabilidad civil y seguro en la circulación de vehículos a motor (LRCSCVM), siguiendo instrucciones de mi poderdante por medio del presente escrito y en nombre del mismo formulo en tiempo y forma CONTESTACIÓN A LA DEMANDA, la cual baso en los siguientes

HECHOS

Nos oponemos a los hechos relatados en el escrito de demanda, si bien se acepta que se produjo el siniestro el día [FECHA] en el qu se vió implicado el vehículo conducido por mi representado, y que existía una relación de aseguramiento del vehículo concertada con la aseguradora demandante. En cuanto a los demás hechos, se niegan expresamente salvo en los concretos extremos que resulten reconocidos en este escrito de contestación.

Con carácter previo debemos alegar la prescripción de la acción de repetición por cuanto que ha transcurrido en exceso el plazo de un año desde el día [FECHA] en que la aseguradora demandante hizo pago de la indemnización al perjudicado.

El criterio interpretativo vigente en la doctrina de las Audiencias Provinciales es que el artículo 10 de la LRCSCVM, en los casos en que el daño causado fuese debido a la conducción bajo la influencia de bebidas alcohólicas, no condiciona en modo alguno el ejercicio del derecho de repetición a una previa condena penal por un delito de tal naturaleza. En consecuencia, por tanto, la declaración penal de responsabilidad no constituye presupuesto necesario para el ejercicio de la citada acción de repetición [FUNDAMENTOS], por lo que tampoco entonces quedaría interrumpido el plazo de prescripción de la acción civil por la pendencia del proceso penal en el que se discuten las posibles responsabilidades del conductor al circular bajo la influencia de bebidas alcohólicas. Nos encontramos, por tanto, ante el ejercicio de una acción, que tiene establecido un especial plazo a contar desde el momento de que la aseguradora paga a los perjudicados, y que dada su naturaleza constituye una acción distinta de la acción nacida de culpa o negligencia extracontractual, así como de la nacida "ex delicto". Así lo vienen interpretando mayoritariamente las Audiencias Provinciales debiendo citarse las SAP Barcelona (Sección 14ª) de 24 de octubre de 2008, rec. 87/2008; SAP Palencia de 8 de noviembre de 2006, rec. 343/2006; y SAP Asturias de 16 de octubre de 2006, rec. 376/2006.

En este caso, tal como se expresa en la demanda, la aseguradora realizó el pago al perjudicado el día [FECHA] e interpuso la demanda el día [FECHA], por lo que había transcurrido en exceso el plazo de un año que la citada normativa prevé. Por tanto, la demanda debe ser desestimada por estar prescrita la acción ejercitada.

En cuanto al fondo, tampoco puede prosperar la acción en tanto que la póliza concertada por mi representado con la aseguradora demandante tenía una cobertura suplementaria por seguro voluntario, tal como se desprende del contenido de la misma en el documento número [Nº DE DOCUMENTO] aportado con la demanda [OTROS DATOS], no estando excluidos los riesgos derivados del artículo 10 de la LRCSCVM, por lo que la facultad de repetición queda excluida por la existencia de un seguro voluntario suplementario donde no se ha excluido el riesgo derivado de las conductas previstas en el citado artículo 10. En la interpretación de las Audiencias se viene entiendo que el seguro voluntario no sólo supone un plus de garantía cuantitativa, sino también cualitativa, de tal manera que ese aseguramiento voluntario amplia la cobertura a supuestos excluídos por dicho seguro, que es precisamente la razón de ser de su contratación complementaria, con recargos importantes en las primas que debe pagar el tomador del seguro.

Por todo ello, la demanda también ha de ser desestimada en cuanto al fondo.

FUNDAMENTOS DE DERECHO

Competencia, legitimación y procedimiento

Conformes con la competencia objetiva y territorial del Tribunal, la legitimación "ad procesum", y el procedimiento adecuado escogido, compareciendo esta parte con la debida representación técnica y asistencia letrada.

Prescripción

En cuanto al ejercicio de la acción, nos oponemos por estar prescrita al haber transcurrido más de un año desde que se hizo pago de la indemnización al perjudicado, tal como se establece en el artículo 10 de la LRCSCVM.

Improcedencia de la acción de repetición

En cuanto al fondo, y si bien la aseguradora haga pago de la indemnización, tiene la facultad de instar un proceso posterior para repetir en los casos previstos en el art. 10 de la LRCSCVM, ello es improcedente cuando, como en este caso, existe una cobertura adicional suplementaria o seguro voluntario donde no se ha excluido la cobertura por las citadas conductas.

Las costas deben imponerse a la actora, de conformidad con lo dispuesto en el artículo 394 LEC.

Por todo lo expuesto,

SUPLICO AL TRIBUNAL que teniendo por presentado este escrito, con sus documentos, y copias de todo ello, se sirva admitirlo, y tenga por formulada CONTESTACIÓN A LA DEMANDA y, tras los trámites legales, dicte Sentencia desestimatoria de la pretensión formulada de contrario, todo ello con expresa imposición de costas a la parte actora.

Es justicia que pido en [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma Procurador y Abogado

========================================================================
