---
name: declinatoria-falta-competencia-territorial-propuesta-civ-0920
description: "Declinatoria por falta de competencia territorial propuesta por el demandado en juicio verbal. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Declinatoria por falta de competencia territorial propuesta por el demandado en juicio verbal

> Formulario **CIV-0920** del plugin **Proceso civil: demandas, contestaciones, prueba y vista** (`formularios-proceso-civil`) · Civil › Escritos procesales (demanda, contestación, prueba, vista) · normativa revisada el 24-11-2026.

## Qué es

Escrito del demandado que, dentro de los diez primeros días del plazo para contestar, propone declinatoria por falta de competencia territorial ante el propio tribunal que conoce de un juicio verbal (arts. 63 a 65 LEC), indicando el tribunal que considera competente y suspendiendo el curso del proceso principal. En los juicios verbales no cabe sumisión expresa ni tácita (art. 54.1 LEC). El modelo toma como ejemplo una reclamación de cantidad derivada de una compraventa con domicilio del demandado en otro partido judicial.

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Declinatoria por falta de competencia territorial propuesta por el demandado en juicio verbal» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Declinatoria por falta de competencia territorial propuesta por el demandado en juicio verbal” para mi caso». También puedes invocarla directamente con `/formularios-proceso-civil:declinatoria-falta-competencia-territorial-propuesta-civ-0920`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-proceso-civil:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Proceso civil: demandas, contestaciones, prueba y vista) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (10 veces)
- [ ] IMPORTE (3 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] Nº (3 veces)
- [ ] NOMBRE Y APELLIDOS DEL DEMANDADO (2 veces)
- [ ] SEDE (2 veces)
- [ ] AÑO
- [ ] CALLE
- [ ] DÍA
- [ ] MES
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] Nº DE PROCEDIMIENTO
- [ ] OBJETO DE LA COMPRAVENTA: DESCRIPCIÓN, MARCA Y MODELO
- [ ] OBJETO DISTINTO DEL PACTADO: DESCRIPCIÓN
- [ ] OBJETO ENTREGADO

## Normas que cita el formulario

- art. 63.2 LEC
- art. 250.2 LEC
- art. 50.1 LEC
- art. 64 LEC
- art. 65 LEC
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

- Junto a «…DIMIENTO] A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

JUICIO VERBAL Nº [Nº DE PROCEDIMIENTO]

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

Don/Doña [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, en nombre y representación de Don/Doña [NOMBRE Y APELLIDOS DEL DEMANDADO], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño a este escrito, comparezco ante este Tribunal a los solos efectos de proponer en forma cuestión de competencia mediante declinatoria en el procedimiento que se sigue ante el mismo con el número arriba referenciado sobre reclamación de cantidad, y como mejor proceda en Derecho, DIGO:

HECHOS

PRIMERO.- Que se ejercita en este proceso una acción de reclamación de cantidad en virtud del contrato privado de compraventa de fecha [FECHA], del que se desprende que el actor, por su condición de vendedor, venía obligado a entregar [OBJETO DE LA COMPRAVENTA: DESCRIPCIÓN, MARCA Y MODELO], asumiendo el comprador la obligación de pagar el precio de [IMPORTE] euros. Tal como consta en el referido contrato, el domicilio de mi representado/a está en la localidad de [LOCALIDAD], calle [CALLE]. Acompaño copia del citado contrato como documento nº 1 del índice electrónico.

En el momento de formalizar el contrato mi mandante entregó la cantidad de [IMPORTE] euros en concepto de arras, pactándose el pago del resto del precio convenido en [Nº] entregas de [IMPORTE] euros cada una de ellas, a pagar el [FECHA], el [FECHA], el [FECHA] y el [FECHA].

Al mismo tiempo se pactó que el vendedor pondría el objeto de la compraventa a disposición del comprador dentro de los cinco días siguientes a la fecha en que se hubiera satisfecho el segundo pago aplazado y en todo caso antes del [FECHA].

SEGUNDO.- Mi mandante cumplió con sus obligaciones efectuando los dos primeros pagos en las fechas indicadas, tal como se acredita con los recibos que se acompañan como documentos nº 2 y 3 del índice electrónico. No obstante, el [FECHA] el vendedor le entregó [OBJETO DISTINTO DEL PACTADO: DESCRIPCIÓN], la cual por otra parte alcanza en el mercado de segunda mano un valor inferior al fijado en la compraventa.

TERCERO.- Que ante dicho incumplimiento mi mandante intentó resolver el problema extrajudicialmente, mediante gestiones amistosas que resultaron infructuosas, por lo que puso a disposición del vendedor el objeto entregado, se negó a efectuar los pagos no vencidos y reclamó los anteriores así como el doble de la suma entregada en concepto de paga y señal.

CUARTO.- Que el pasado [FECHA] mi mandante fue emplazado/a para contestar a la demanda en el juicio verbal arriba expresado por plazo de veinte días.

FUNDAMENTOS DE DERECHO

1º) Conforme al artículo 63.2 de la LEC, la declinatoria debe proponerse ante el mismo Tribunal que esté conociendo del asunto y que se considere que carece de competencia territorial, solicitándole que se separe de su conocimiento y que remita los autos al Tribunal que tenga competencia territorial para enjuiciar el asunto.

2º) En este caso, la cuestión controvertida no tiene asignada por razón de la materia una tramitación especial, de modo que el trámite a seguir es el del juicio verbal por no exceder la cuantía litigiosa de la prevista en el artículo 250.2 de la LEC.

3º) El artículo 54.1 prohíbe la sumisión expresa y la tácita en los asuntos que deban decidirse por medio de juicio verbal, como es el caso, por la razón antes dicha.

4º) La demanda tiene por objeto una reclamación de cantidad que no tiene asignada una tramitación especial por razón de la materia. En consecuencia, rige el fuero general del domicilio del demandado, por aplicación del artículo 50.1 de la LEC, domicilio que, tal como se desprende del hecho primero de este escrito, se halla fuera de este partido judicial.

5º) Atendido que la declinatoria que mediante este escrito se propone se funda en la falta de competencia territorial y que ésta no viene impuesta por normas imperativas, procede indicar el Tribunal al que, por considerarlo territorialmente competente, deberán remitirse las actuaciones, y que es el Tribunal de Instancia de [SEDE], al residir el demandado en dicha ciudad, todo ello al amparo de los arts. 63.1 y 65.4 de la LEC.

6º) Que en cumplimiento del presupuesto establecido en el artículo 64 de la LEC esta proposición se hace dentro de los diez primeros días del plazo para contestar a la demanda, por lo que procede suspender el curso del proceso principal durante la tramitación del incidente.

7º) Asimismo, acompaño a este escrito los documentos a que se refiere el artículo 65 de la LEC, en concreto: fotocopia del DNI, el contrato de compraventa, los recibos expedidos por el vendedor que acreditan el pago parcial del precio en los términos contenidos, es decir, el [FECHA] y el [FECHA], así como copia del albarán de entrega de [OBJETO ENTREGADO] (documentos número [Nº] del índice electrónico), los cuales constituyen un principio de prueba en los que se funda la declinatoria, junto con las copias para los demás litigantes.

8º) Procede la imposición de las costas causadas en este incidente a la parte demandante, ya que el actor era conocedor de la falta de competencia territorial de este Tribunal, al amparo del art. 394 de la LEC.

Por todo lo expuesto,

SUPLICO AL TRIBUNAL: Tenga por presentado este escrito y documentos con justificante de traslado, y copias para el Ministerio Fiscal, me tenga por comparecido/a y parte en la representación que acredito de Don/Doña [NOMBRE Y APELLIDOS DEL DEMANDADO], a los efectos de proponer cuestión de competencia territorial, acordándose que se entiendan con esta representación las sucesivas diligencias, así como que se tenga por promovida cuestión de competencia territorial por declinatoria y, previos los trámites legales, con suspensión del curso del procedimiento principal, se dicte por este Tribunal auto mediante el cual se inhiba del conocimiento en favor de los Tribunales de la misma clase de la localidad de [LOCALIDAD], acordando remitirle los autos con emplazamiento de las partes para que comparezcan ante él en el plazo de diez días; todo ello con expresa condena en costas al demandante.

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma de Abogado/a y Procurador/a.
