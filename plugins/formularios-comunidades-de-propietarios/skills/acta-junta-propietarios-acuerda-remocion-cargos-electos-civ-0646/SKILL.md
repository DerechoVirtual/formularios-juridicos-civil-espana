---
name: acta-junta-propietarios-acuerda-remocion-cargos-electos-civ-0646
description: "Acta de junta de propietarios que acuerda la remoción de cargos electos. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Acta de junta de propietarios que acuerda la remoción de cargos electos

> Formulario **CIV-0646** del plugin **Comunidades de propietarios** (`formularios-comunidades-de-propietarios`) · Civil › Propiedad horizontal · normativa revisada el 25-11-2026.

## Qué es

Acta de Junta de Propietarios acordando la remoción del administrador de la Comunidad.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Acta de junta de propietarios que acuerda la remoción de cargos electos» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Acta de junta de propietarios que acuerda la remoción de cargos electos” para mi caso». También puedes invocarla directamente con `/formularios-comunidades-de-propietarios:acta-junta-propietarios-acuerda-remocion-cargos-electos-civ-0646`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-comunidades-de-propietarios:indice`.

## Qué contiene esta skill

- `SKILL.md` (este fichero): qué es el formulario, para qué sirve, cómo se usa, los datos que pide, las normas que cita, los avisos de actualización y las instrucciones para Claude.
- `assets/formulario.md`: el formulario seco, tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…]. Es el texto que se rellena; no lleva explicaciones.
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Comunidades de propietarios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (12 veces)
- [ ] LETRA (2 veces)
- [ ] Nº (2 veces)
- [ ] PORCENTAJE (2 veces)
- [ ] FECHA
- [ ] LOCALIDAD
- [ ] MANIFESTACIONES DEL ADMINISTRADOR
- [ ] MANIFESTACIONES DEL VECINO
- [ ] NÚMERO
- [ ] PISO
- [ ] PROPIETARIOS Y CUOTAS A FAVOR

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

### Avisos de actualización (0) — se aplican en el texto, nunca se copian en el documento

- Ninguno.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Acta de Junta de Propietarios acordando la remoción del administrador de la Comunidad.

Notas al pie del formulario original:
(1) Corresponde a la Junta de propietarios la labor de remover de su cargo al administrador. El régimen jurídico de la remoción o destitución del Administrador es el mismo que el del resto de cargos de la Comunidad: mediante un acuerdo de la Junta de Propietarios, convocada en sesión extraordinaria, el Administrador de la Comunidad, antes de que finalice su mandato, puede ser destituido de su cargo (SAP de Madrid de 4 julio 2000).

Incluso un Administrador que haya sido nombrado por tiempo indefinido, puede ser removido de su cargo, exista o no justa causa, por la Junta de Propietarios, conforme al art. 13.7 LPH.

La existencia de un pacto en el que se establezca que el Administrador no puede ser removido de su cargo hasta que transcurra un determinado periodo de tiempo o hasta que finalice su mandato, es nulo y no surte ninguna clase de efectos. La Comunidad de Propietarios podría cesar libremente, cuando lo estimase oportuno, al Administrador.

La mayoría de la doctrina considera que la remoción del Administrador también se puede realizar en una Junta de Propietarios ordinaria, siempre que en el orden del día de la convocatoria aparezca, de forma clara y precisa, el tema de la destitución del Administrador, con la finalidad de que éste pueda manifestar en ella lo que estime oportuno (téngase en cuenta que el artículo 14.a) LPH incluye entre las potestades de la junta general, sin diferenciar entre ordinarias y extraordinarias, la de nombrar y remover a las personas que ostenten los cargos previstos en la Ley).

El Preámbulo de la LPH afirma que el cargo de administrador es amovible. Pese a ello, no establece las causas específicas de remoción del cargo de Administrador. Por tanto, para la destitución del Administrador bastará con un acuerdo mayoritario de la Junta de Propietarios, reunida en sesión ordinaria o extraordinaria, sin necesidad de fundar la citada decisión en causa alguna (SAP de Málaga de 2 de febrero de 1998, rec. 851/1997).

Debe tenerse en cuenta que nada impide a los copropietarios establecer en los estatutos de la Comunidad causas específicas de remoción del cargo de Administrador. La desidia, los comportamientos negligentes o resolver los asuntos de forma favorable a sus intereses particulares, son ejemplos de causas que pueden incluirse en los estatutos para el cese del Administrador.

La validez de las cláusulas contenidas en los estatutos de la Comunidad que modifican el régimen de mayorías previsto por la LPH para la remoción del Administrador, exigiendo mayorías cualificadas o incluso la unanimidad, es más que discutible. Considerando que la autonomía de la voluntad de los copropietarios no puede modificar el régimen de mayorías establecido en el art. 17 LPH la fijación de otras mayorías en los estatutos iría contra el interés general y el buen funcionamiento de la Comunidad de Propietarios.

La cuestión más relevante en materia de remoción del Administrador es determinar si el Administrador tiene derecho a reclamar alguna indemnización cuando se le destituye sin causa justificada. En la doctrina y en la jurisprudencia existen tesis contrapuestas:

— Un sector doctrinal afirma que al ser un cargo de libre remoción por parte de la Comunidad, ésta, en principio, no deberá indemnizar al Administrador cesado (SAP de Barcelona de 15 de abril de 1999).

— Por el contrario, otro sector defiende que en determinados casos, la Comunidad de Propietarios sí tiene que abonar una indemnización al Administrador cesado. Existirá obligación de abonar una indemnización al Administrador que ha sido destituido antes de cumplirse el tiempo pactado cuando: el cargo de Administrador sea remunerado, la destitución se produzca sin justa causa, o cuando se realice sin respetar el plazo de preaviso pactado; y cuando la destitución haya ocasionado perjuicios al Administrador. Véase, como ejemplo, STS de 8 de abril de 1991, SSAP de Málaga de 2 de febrero de 1998, rec. 851/1997 y 15 de marzo de 1999, ó SAP de Guipúzcoa de 3 de marzo de 1998.

No obstante, debe reconocerse al Administrador el derecho a ser indemnizado por la remuneración correspondiente a los meses dejados de percibir desde que fue cesado en su cargo en Junta de Propietarios antes del vencimiento de la relación contractual renovada, salvo que se acreditara el incumplimiento de sus funciones y obligaciones.

El Administrador destituido está obligado a entregar al Presidente toda la documentación relacionada con la Comunidad de Propietarios, no pudiendo retenerla en su poder hasta que la Comunidad abone las cantidades que le adeuda (SAP de Barcelona de 15 de abril de 1999, rec. 493/1998).

La resolución de contratos de la Comunidad, y entre ellos el que la liga con el Administrador de Fincas, en principio requiere una mayoría simple.

No obstante, ello es así siempre que se pretenda simplemente rescindir el contrato con esa persona concreta, pero no la supresión del servicio, es decir, se rompe el vínculo contractual con el Administrador, pero se va a contratar a otro.

Por el contrario, si de lo que se trata es de suprimir el servicio en sí, se requerirá la mayoría cualificada de 3/5 contemplada en el art. 17.3 LPH, al tratarse de servicios comunes de interés general.

Finalmente, respecto a la contribución de los disidentes en el pago de las indemnizaciones, la doctrina del Tribunal Supremo es clara en el sentido de establecer que los gastos judiciales que se produzcan en litigios con terceros son a cargo de todos los integrantes de la Comunidad de propietarios. Se trata de un supuesto de responsabilidad de la Comunidad a la que ésta debe hacer frente con todos los fondos y créditos a su favor (art. 22.1 LPH). Por lo tanto, está dentro de lo establecido en el art. 9.1 e), contribuir, con arreglo a la cuota de participación fijada en el título o a lo especialmente establecido, a los gastos generales para el adecuado sostenimiento del inmueble, sus servicios, cargas y responsabilidades que no sean susceptibles de individualización.

========================================================================


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
