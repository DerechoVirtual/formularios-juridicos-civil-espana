---
name: oposicion-medida-cautelar-ofrecimiento-caucion-civ-1219
description: "Oposición a una medida cautelar con ofrecimiento de caución sustitutoria. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Oposición a una medida cautelar con ofrecimiento de caución sustitutoria

> Formulario **CIV-1219** del plugin **Medidas cautelares y diligencias preliminares** (`formularios-medidas-cautelares-civiles`) · Civil › Medidas cautelares y diligencias preliminares · normativa revisada el 24-11-2026.

## Qué es

Escrito de oposición del demandado a una medida cautelar (embargo preventivo) acordada con la admisión de la demanda y sin su audiencia (arts. 739 y siguientes LEC), por falta de apariencia de buen derecho y de peligro en la demora, con ofrecimiento subsidiario de caución sustitutoria (arts. 746 y 747 LEC), solicitud de daños y perjuicios y costas (formulario adaptado a la reforma procesal de la LO 1/2025).

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Oposición a una medida cautelar con ofrecimiento de caución sustitutoria» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Oposición a una medida cautelar con ofrecimiento de caución sustitutoria” para mi caso». También puedes invocarla directamente con `/formularios-medidas-cautelares-civiles:oposicion-medida-cautelar-ofrecimiento-caucion-civ-1219`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-medidas-cautelares-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Medidas cautelares y diligencias preliminares) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (7 veces)
- [ ] IMPORTE (3 veces)
- [ ] MEDIDA CAUTELAR ADOPTADA (2 veces)
- [ ] Nº DE DOCUMENTOS (2 veces)
- [ ] AÑO
- [ ] DÍA
- [ ] LOCALIDAD
- [ ] MES
- [ ] NOMBRE Y APELLIDOS
- [ ] NOMBRE Y APELLIDOS O DENOMINACIÓN SOCIAL
- [ ] Nº
- [ ] Nº DE PROCEDIMIENTO
- [ ] SEDE

## Normas que cita el formulario

- art. 739 LEC
- art. 728 LEC
- art. 728.2 LEC
- art. 723.1 LEC
- art. 740 LEC
- art. 741.2 LEC

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

- Junto a «…AUTELARES A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

PROCESO NÚMERO [Nº DE PROCEDIMIENTO]

PIEZA DE MEDIDAS CAUTELARES

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

D./Dª [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, en nombre y representación de [NOMBRE Y APELLIDOS O DENOMINACIÓN SOCIAL], parte demandada en el procedimiento arriba referenciado, según tengo acreditado en autos, ante el Tribunal comparezco y, como mejor proceda en Derecho, DIGO:

Que habiendo sido notificado de la medida cautelar de [MEDIDA CAUTELAR ADOPTADA] adoptada, con la admisión de la demanda y sin audiencia de mi representado, por auto de fecha [FECHA], por medio del presente escrito, al amparo de lo dispuesto en el artículo 739 y siguientes de la LEC y dentro del plazo establecido, formulo OPOSICIÓN A LA MEDIDA CAUTELAR decretada en base a los siguientes

HECHOS

Nos oponemos a la medida cautelar de [MEDIDA CAUTELAR ADOPTADA] decretada por el Tribunal al que me dirijo por auto de fecha [FECHA], por cuanto que no se dan los requisitos necesarios para su adopción de apariencia de buen derecho y peligro en la demora, expresados en el artículo 728 de la LEC.

Incumplimiento de requisitos: apariencia de buen derecho

En cuanto a la apariencia de buen derecho, el artículo 728.2 de la LEC impone al solicitante la carga de fundar y acreditar indiciariamente la apariencia de buen derecho de su pretensión, siendo que en este caso los hechos relatados, que expresamente negamos, y la justificación aportada no permiten apreciar la apariencia de buen derecho (fumus boni iuris), ya que el demandante sostiene que el precio de los suministros por él verificados no le ha sido satisfecho en el periodo comprendido entre [FECHA] y [FECHA], sin que aporte otros documentos que unos albaranes, elaborados unilateralmente, sin venir autorizados por firma alguna, y que además no se corresponden en absoluto con los géneros entregados.

Además, negamos rotundamente que mi representado no abonara los suministros en el periodo comprendido entre [FECHA] y [FECHA], como se alega en la demanda, puesto que se han venido realizando puntualmente los pagos de los suministros recibidos, tal como se acredita por los justificantes de transferencias verificadas a la cuenta de la entidad instante de las medidas, que acompañamos como documentos [Nº DE DOCUMENTOS] de este escrito de oposición.

Debe subrayarse que estas transferencias se corresponden todas ellas al periodo en que el demandante concreta el impago, todo lo cual desvirtúa cualquier apariencia de buen derecho en la petición del demandante.

Incumplimiento de requisitos: peligro en la demora

Además de no cumplirse los requisitos de apariencia de buen derecho, tampoco hay peligro en la demora, negando expresamente el relato fáctico del solicitante, puesto que los documentos aportados con la demanda en ningún caso ponen de manifiesto la existencia del mínimo riesgo de insolvencia o iliquidez de mi representado.

Al contrario, no existe peligro en la demora dada la solvencia de mi representado, teniendo bienes suficientes y liquidez para hacer frente al pago de las responsabilidades que pudieran derivarse, acompañando a este escrito, como documentos [Nº DE DOCUMENTOS], certificación de las cuentas anuales de los dos últimos ejercicios, que ponen de manifiesto la solvencia de mi representado, ocultada de contrario, de lo que también se deriva la improcedencia de adoptar la medida cautelar.

Ofrecimiento de caución sustitutoria subsidiaria

En el improbable caso de desestimarse la oposición, esta parte ofrece subsidiariamente la prestación de caución sustitutoria de la medida de embargo preventivo adoptada, ofreciendo aval bancario por importe de [IMPORTE] euros, por cuanto dicha medida sustitutoria satisface suficientemente el interés cautelar del demandante y la medida de embargo produce una disfunción en la actividad patrimonial de mi representado, cuya actividad económica es [ACTIVIDAD ECONÓMICA: p. ej., la venta de inmuebles que promociona], que resulta perjudicada de forma desproporcionada por el embargo trabado.

A los anteriores hechos le son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

Competencia

Le corresponde al Tribunal al que me dirijo, al estar conociendo del asunto en primera instancia (art. 723.1 LEC).

Legitimación

Le corresponde a esta parte, al ser la que se ve afectada por las medidas cautelares en su momento decretadas (art. 739 LEC).

Procedimiento

Es el previsto en los artículos 740 y siguientes de la LEC, al haberse adoptado las presentes medidas sin audiencia del demandado.

Apariencia de buen derecho

Es el primero y básico de los requisitos que no concurren, ya que la aportada por el instante de las medidas cautelares se ha visto desvirtuada por el pago efectuado por mi mandante (art. 728.2 LEC).

Peligro en la demora

No existe peligro derivado de la mora procesal al tratarse de un proceso de reclamación de cantidad respecto de un demandado plenamente solvente, sin que exista ningún indicio de que la medida sirva a la tutela cautelar que debe dirigirse.

Solicitud de daños y perjuicios

Al entender que el demandante ha interesado inadecuadamente las medidas cautelares, se solicita que, con fundamento en el artículo 741.2 de la LEC, se declare la condena al demandante a abonar a mi mandante los daños y perjuicios que en su momento y por los trámites previstos en los artículos 712 y siguientes se solicitarán, reteniendo mientras tanto el importe de la caución constituida por el instante.

Caución sustitutoria subsidiaria

Para el caso de que se desestime la oposición, se ofrece caución por importe de [IMPORTE] euros en sustitución de las medidas cautelares, que se prestará mediante aval bancario, y que se solicita por los perjuicios desproporcionados que ocasiona la medida acordada (arts. 746.2 y 747.1 LEC).

Costas

En materia de costas se solicita su imposición al instante de conformidad con lo previsto en el artículo 741.2 de la LEC.

En base a lo anterior,

SUPLICO AL TRIBUNAL que tenga por presentado escrito con los documentos a él anejos y copias, tenga por comparecida a esta parte y formulada oposición a la medida preventiva de embargo acordada por ese Tribunal en auto de [FECHA] y, previa la tramitación pertinente, se sirva alzarla dejándola sin efecto y expidiendo los mandamientos pertinentes para la cancelación de la anotación decretada, condenando asimismo al actor al pago de los daños y perjuicios irrogados a mi mandante como consecuencia de la medida cautelar, con expresa condena en costas al instante. De forma subsidiaria, de no estimarse la pretensión principal, se solicita que se tenga por ofrecida caución sustitutoria de las medidas por importe de [IMPORTE] euros y, tras seguirse el trámite procedimental, se acepte la petición.

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO]

Firma Abogado: ______________________

Firma Procurador: ______________________
