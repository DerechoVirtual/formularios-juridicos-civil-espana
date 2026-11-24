---
name: conclusiones-orales-parte-juicio-ordinario-civ-0946
description: "Conclusiones orales de la parte en el juicio ordinario. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Conclusiones orales de la parte en el juicio ordinario

> Formulario **CIV-0946** del plugin **Proceso civil: demandas, contestaciones, prueba y vista** (`formularios-proceso-civil`) · Civil › Escritos procesales (demanda, contestación, prueba, vista) · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Conclusiones orales de la parte en el juicio ordinario» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Conclusiones orales de la parte en el juicio ordinario” para mi caso». También puedes invocarla directamente con `/formularios-proceso-civil:conclusiones-orales-parte-juicio-ordinario-civ-0946`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-proceso-civil:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Proceso civil: demandas, contestaciones, prueba y vista) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (6 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] FECHA (2 veces)
- [ ] NÚMERO (2 veces)

## Normas que cita el formulario

- art. 433 LEC
- art. 376 LEC
- art. 386 LEC
- art. 386.2 LEC
- art. 39 Ley 39/2015
- art. 1902 Código Civil

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

Proposición

Con la venia, y conforme a lo prevenido en el art. 433 de la LEC, esta defensa formula las siguientes conclusiones:

A la vista del desarrollo del proceso, la cuestión fáctica controvertida queda reducida a dos hechos, alegados en nuestro escrito de demanda, en los ordinales segundo y cuarto, es decir, si el vehículo del demandado rebasó el semáforo en fase roja y si el demandante ha quedado absolutamente incapacitado para cualquier tipo de trabajo como consecuencia de las lesiones sufridas en el accidente. No hay controversia, por ser admitido, que se produjo el accidente en el día de autos, así como en las lesiones sufridas por mi defendido, tanto en lo relativo a días de baja como a las secuelas.

En relación a que el vehículo conducido por el demandado efectivamente rebasó el semáforo en fase roja se ha practicado prueba de interrogatorio de las partes, testifical de los testigos Sres. y [NOMBRE Y APELLIDOS] y documental, consistente en el atestado policial redactado por la Guardia Civil que obra como documento número [Nº DE DOCUMENTO] de la demanda.

En relación a que mi mandante ha quedado absolutamente incapacitado para cualquier tipo de trabajo, se ha practicado prueba de interrogatorio de las partes, dictamen pericial del Médico D. [NOMBRE Y APELLIDOS] y documental pública consistente en resolución del INSS de fecha [FECHA], declarando la incapacidad permanente absoluta, que obra como documento número [Nº DE DOCUMENTO] de la demanda, y dictamen del Médico Forense emitido en diligencias previas número [NÚMERO] que se incorporó como documento número [Nº DE DOCUMENTO] de la demanda.

De la prueba practicada resultan totalmente acreditados los hechos alegados en nuestra demanda.

Así, y en relación a que el vehículo del demandado rebasó el semáforo en fase roja, ante las versiones ofrecidas contradictoriamente, tanto en los escritos alegatorios como en el juicio, en la prueba de interrogatorio de las partes, debemos acudir a la prueba testifical donde por los dos testigos propuestos por esta parte se ha afirmado rotundamente que el vehículo de mi representado rebasó el semáforo en fase verde, de lo que se concluye que el demandado rebasó el semáforo en fase roja. A la hora de valorar esta prueba, conforme a las reglas de la sana crítica a que se refiere el art. 376 de la LEC, debemos hacer notar a V.I. que el testimonio de estas personas presenta plenas garantías de veracidad, por varias causas: por una parte, y desde un primer momento se trata de testigos que se hallaban presentes en el lugar del accidente, y así consta expresamente su identidad en el atestado policial, concretamente en el folio número [NÚMERO] del atestado, donde se refiere que estos testigos circulaban en sendos vehículos detrás del turismo de mi representado; y, por otra parte, estos testigos no tienen relación alguna con mi representado, siendo que además ni tan siquiera se conocen entre ellos. En cuanto al contenido del testimonio, ambos testigos han afirmado sin ningún tipo de dudas que vieron cómo el vehículo de mi representado rebasaba el semáforo cuando ya se hallaba en fase verde, de lo que se deriva claramente que fue el demandado el que rebasó el semáforo en fase roja.

Al respecto, el art. 386 de la LEC permite tener como probado este hecho, pues ha quedado totalmente demostrado que mi representado rebasó el semáforo en fase verde, por lo que es lógico deducir que el semáforo del demandado estaba en fase roja, pues es notorio que existe coordinación entre las señales luminosas. Aquí debe hacerse notar a V.I. que en ningún momento se ha propuesto prueba de contrario tendente a desvirtuar tal conclusión, cuando desde el escrito inicial de demanda hemos mantenido la misma versión fáctica, limitándose el demandado a afirmar que tenía el semáforo en fase verde y sin proponer prueba de descargo como le autorizaba el art. 386.2 de la LEC, por lo que entendemos que el hecho ha quedado plenamente probado.

En relación al grado de incapacidad de mi representado, debemos partir de la presunción de validez de los actos administrativos, expresamente establecida en el art. 39 de la Ley 39/2015, de Procedimiento Administrativo Común de las Administraciones Públicas, lo cual hace que la declaración del INSS, declarando la incapacidad permanente absoluta de mi representado, constituya un elemento de prueba plenamente acreditativo de tal grado de incapacidad, que además ha resultado corroborado por los dictámenes periciales del perito Doctor [NOMBRE Y APELLIDOS] y del Médico Forense que concluyen que mi representado está incapacitado para todo tipo de trabajo.

Partiendo de los anteriores hechos, son de plena aplicación los fundamentos de derecho alegados en nuestro escrito de demanda, debiéndose condenar al demandado por aplicación del art. 1902 del Código Civil, debiendo fijarse la cuantía de [IMPORTE] euros en concepto de responsabilidad civil tal como solicitábamos en nuestro escrito de demanda, a razón de [IMPORTE] euros por los días de baja, de [IMPORTE] euros por las secuelas sufridas, incluyendo el grado de invalidez absoluta que se acredita de la prueba practicada; las cuantías por lesiones y secuelas están dentro de la aplicación del baremo con los incrementos señalados al tener mi defendido unos ingresos anuales de [IMPORTE] euros, hecho no controvertido; en orden al quantum de la indemnización tomamos las cuantías establecidas en la Resolución de fecha [FECHA], de donde resulta la aplicación de una cuantía de [IMPORTE] euros por día impeditivo y la cantidad de [IMPORTE] euros señalada para las secuelas, teniendo en cuenta que las mismas le impiden el desarrollo de las tareas de cualquier profesión, por lo que la cantidad solicitada se ajusta plenamente a dicha resolución.

Por lo expuesto, solicitamos sentencia estimatoria de conformidad al suplico de nuestra demanda.

========================================================================
