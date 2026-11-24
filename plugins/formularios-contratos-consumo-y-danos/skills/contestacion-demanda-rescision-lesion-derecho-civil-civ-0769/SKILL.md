---
name: contestacion-demanda-rescision-lesion-derecho-civil-civ-0769
description: "Contestación a la demanda de rescisión por lesión (Derecho civil catalán). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contestación a la demanda de rescisión por lesión (Derecho civil catalán)

> Formulario **CIV-0769** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Escrito de contestación a una demanda de rescisión por lesión de un contrato de compraventa, planteada al amparo del Derecho civil de Cataluña (lesión «ultra dimidium», arts. 621-46 y ss. del Código Civil de Cataluña), cuando el inmueble está situado fuera de Cataluña. Se opone la inaplicabilidad de la ley catalana (art. 10.5 CC) y, subsidiariamente, la inexistencia de lesión.

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contestación a la demanda de rescisión por lesión (Derecho civil catalán)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contestación a la demanda de rescisión por lesión (Derecho civil catalán)” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:contestacion-demanda-rescision-lesion-derecho-civil-civ-0769`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (2 veces)
- [ ] SEDE (2 veces)
- [ ] AÑO
- [ ] DÍA
- [ ] FECHA
- [ ] LOCALIDAD
- [ ] LOCALIDAD Y PROVINCIA DEL INMUEBLE
- [ ] MES
- [ ] NOMBRE Y APELLIDOS DEL ABOGADO/A
- [ ] NOMBRE Y APELLIDOS DEL DEMANDADO
- [ ] NOMBRE Y APELLIDOS DEL DEMANDANTE
- [ ] NOMBRE Y APELLIDOS DEL PERITO
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] Nº DE PROCEDIMIENTO

## Normas que cita el formulario

- art. 621 Código Civil
- art. 10.5 Código Civil
- art. 16.1 Código Civil
- art. 1290 Código Civil
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

### Avisos de actualización (2) — se aplican en el texto, nunca se copian en el documento

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…cual se establece imperativamente en los mencionados artículos del Código Civil.»: comprobar la redacción vigente del art. 10.5 CC y, si el contrato es posterior a la fecha de aplicación del Reglamento (CE) n.º 593/2008 (Roma I), su incidencia en la determinación de la ley aplicable.

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, actuando en representación de [NOMBRE Y APELLIDOS DEL DEMANDADO], según se acredita mediante [ELEGIR: copia electrónica del poder notarial de representación / apoderamiento apud acta otorgado ante el Letrado/a de la Administración de Justicia del Tribunal de [SEDE]] que se acompaña [y se solicita sea devuelta una vez testimoniada], y bajo la dirección letrada de D./Dña. [NOMBRE Y APELLIDOS DEL ABOGADO/A], ante la Sección Civil del Tribunal de Instancia, en el proceso declarativo n.º [Nº DE PROCEDIMIENTO], comparezco y, como mejor proceda en Derecho, DIGO:

Que, habiéndose dado traslado a esta parte de la demanda formulada por D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDANTE] en ejercicio de la acción de rescisión por lesión del contrato de compraventa concertado por ambas partes en fecha [FECHA], siguiendo instrucciones de mi poderdante, por medio del presente escrito y en nombre del mismo formulo, en tiempo y forma, CONTESTACIÓN A LA DEMANDA, la cual baso en los siguientes

HECHOS

PRIMERO.– Negamos los hechos relatados en el escrito de demanda, salvo aquellos que sean expresamente aceptados a lo largo de este escrito.

SEGUNDO.– Se acepta la celebración del contrato de compraventa sobre el inmueble, así como el precio y demás condiciones pactadas, pero se niega que sea de aplicación al contrato la legislación civil catalana y que exista lesión para el demandante, tal como se expresa a continuación.

TERCERO.– Con carácter previo a la cuestión de fondo sobre la falta de lesión que justifique la acción de rescisión, debe oponerse que el contrato de compraventa no está sujeto a las normas de derecho civil catalán, no siendo de aplicación el instituto de la lesión «ultra dimidium» regulada en los artículos 621-46 y siguientes del Código Civil de Cataluña.

El demandante pretende la aplicación de la legislación civil catalana con fundamento en que ambos contratantes tienen vecindad civil catalana. Sin embargo, en este caso lo que se ejercita es la acción de rescisión de la compraventa sobre un inmueble sito fuera de Cataluña, concretamente en [LOCALIDAD Y PROVINCIA DEL INMUEBLE], por lo que es irrelevante la vecindad civil de los contratantes, y ello es así porque, versando el tema litigioso sobre la rescisión de un contrato de compraventa por lesión «ultra dimidium», rige como punto de conexión el de la situación de la cosa, tal como dispone expresamente el artículo 10.5 del Código Civil, al cual se remite el artículo 16.1, párrafo primero, del Código Civil, con arreglo al cual los conflictos de leyes que puedan surgir por la coexistencia de distintas legislaciones en el territorio español se resolverán según las normas contenidas en el Capítulo IV (normas de Derecho internacional privado). En este punto, el artículo 10.5 establece que, a falta de sometimiento expreso, se aplicará a los contratos relativos a bienes inmuebles la ley del lugar donde estén sitos, a diferencia del resto de obligaciones contractuales a las que se refiere el párrafo primero del mismo artículo 10.5. Por tanto, en el presente caso, donde el demandante no alega la sumisión expresa, ni la misma consta en modo alguno en el contrato, y estando el inmueble objeto de la enajenación onerosa fuera del territorio de Cataluña, debe aplicarse la legislación común con total independencia de la vecindad civil de las partes, lo cual se establece imperativamente en los mencionados artículos del Código Civil.

CUARTO.– Por tanto, no procede la aplicación del régimen jurídico establecido en los artículos 621-46 y siguientes del Código Civil de Cataluña, siendo que la legislación común no anuda los efectos rescisorios a la pretensión actora, por lo que debe desestimarse la demanda.

QUINTO.– Subsidiariamente, y para el improbable caso de que se estimara la aplicación del régimen específico de la acción rescisoria contemplada en el artículo 621-46 del Código Civil de Cataluña al contrato de autos, no se dan los requisitos contemplados en el precepto, puesto que no existe una lesión superior en más de la mitad del precio justo, según resulta de la pericial practicada por el Arquitecto D./Dña. [NOMBRE Y APELLIDOS DEL PERITO], que se aporta como documento [Nº], la cual valora los bienes conforme a los criterios legales definidos en el artículo 621-46 del Código Civil de Cataluña, especialmente conforme a lo previsto en su párrafo primero, esto es, tomando como referencia el valor al tiempo de otorgarse el contrato y comparando con el precio de bienes de similares características en la localidad, lo cual no hace la pericial aportada por la parte actora, la cual se impugna desde este momento, que toma como referencia el valor actual de los bienes y hace una valoración desligada de cualquier parámetro comparativo.

De ello resulta que el precio pactado es [ELEGIR: levemente inferior / ajustado] al que resulta como justo precio, de modo que la demanda debe también desestimarse por este motivo.

FUNDAMENTOS DE DERECHO

I.– COMPETENCIA Y PROCEDIMIENTO.

Conformes con la competencia objetiva y territorial del Tribunal y el procedimiento adecuado escogido, compareciendo esta parte con la debida representación técnica y asistencia letrada.

II.– LEGISLACIÓN APLICABLE.

En cuanto al fondo, no es de aplicación el Código Civil de Cataluña, por cuanto se trata de un conflicto sobre un contrato relativo a un inmueble que radica fuera del territorio catalán, sin que exista sumisión expresa por las partes, de manera que, conforme al artículo 10.5, párrafo segundo, del Código Civil, es de aplicación la legislación común.

III.– ACCIÓN DE RESCISIÓN POR LESIÓN: FALTA DE REQUISITOS.

Conforme a lo argumentado, no es de aplicación el régimen de rescisión de los artículos 621-46 y siguientes del Código Civil de Cataluña, no dándose ninguno de los supuestos contemplados en la regulación común de los artículos 1290 y siguientes del Código Civil. Pero, aun aceptando la aplicación del régimen catalán, tampoco se daría el requisito esencial de la lesión en más de la mitad del justo precio calculado conforme a las reglas específicas establecidas en el artículo 621-46 del Código Civil de Cataluña.

IV.– COSTAS.

Las costas deben imponerse a la actora, de conformidad con lo dispuesto en el artículo 394 LEC.

Por todo lo expuesto,

SUPLICO AL TRIBUNAL: que, teniendo por presentado este escrito, con sus documentos y copias de todo ello, se sirva admitirlo y tenga por formulada CONTESTACIÓN A LA DEMANDA y, tras los trámites legales, dicte sentencia desestimatoria de la pretensión formulada de contrario, todo ello con expresa imposición de costas a la parte actora.

Es justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Abogado/a Firma del Procurador/a
