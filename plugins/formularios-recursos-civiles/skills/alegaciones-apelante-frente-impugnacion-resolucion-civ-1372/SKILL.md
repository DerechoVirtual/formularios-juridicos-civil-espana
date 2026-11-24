---
name: alegaciones-apelante-frente-impugnacion-resolucion-civ-1372
description: "Alegaciones del apelante frente a la impugnación de la resolución apelada. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Alegaciones del apelante frente a la impugnación de la resolución apelada

> Formulario **CIV-1372** del plugin **Recursos civiles: reposición, apelación, casación y queja** (`formularios-recursos-civiles`) · Civil › Recursos · normativa revisada el 24-11-2026.

## Qué es

Receptor INADMISIBILIDAD DEL RECURSO DE APELACIÓN IMPUGNACIÓN SOBRE CUANTIFICACIÓN DE LA INDEMNIZACIÓN DE LA CONDENA APORTACIÓN DOCUMENTAL DEL RECURSO PRUEBA EN SEGUNDA INSTANCIA COSTAS SUPLICO A LA SALA SUPLICO A LA AUDIENCIA PROVINCIAL Firmas Escrito de alegaciones de la parte recurrente al escrito de impugnación presentado por el apelado ante el recurso de apelación admitido, basado en la no constitución del depósito estipulado legalmente, impugnando a su vez la cuantificación de la indemnización de la condena, así como la aportación de nueva documentación en el recurso.

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Alegaciones del apelante frente a la impugnación de la resolución apelada» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Alegaciones del apelante frente a la impugnación de la resolución apelada” para mi caso». También puedes invocarla directamente con `/formularios-recursos-civiles:alegaciones-apelante-frente-impugnacion-resolucion-civ-1372`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-recursos-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Recursos civiles: reposición, apelación, casación y queja) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] AÑO (2 veces)
- [ ] FECHA (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] ASEGURADORA
- [ ] DÍA
- [ ] LUGAR
- [ ] MES
- [ ] Nº DE PROCEDIMIENTO

## Normas que cita el formulario

- art. 449.3 LEC
- art. 576 LEC
- art. 449.6 LEC
- art. 231 LEC
- art. 460.1 LEC
- art. 271.1 LEC
- art. 336 LEC
- art. 285.2 LEC
- art. 460.2.2.ª LEC
- art. 394.1 LEC
- art. 398.1 LEC

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

A LA SALA

D./Doña [NOMBRE Y APELLIDOS], Procurador de los Tribunales, que actúa en nombre y representación de la Compañía de Seguros [ASEGURADORA], cuya representación tengo debidamente acreditada, ante la Sala comparezco en el juicio ordinario n.º [Nº DE PROCEDIMIENTO]/[AÑO] y, como mejor proceda en Derecho, DIGO:

Que dentro del plazo legal conferido al efecto por la Sala a esta parte mediante providencia de fecha [FECHA], formalizo escrito de manifestaciones frente a la impugnación de la resolución apelada por esta parte:

PRIMERA.- INADMISIBILIDAD DEL RECURSO DE APELACIÓN

La contraparte sostiene que no se ha cumplido la prevención del art. 449.3 LEC, dado que, al interponer el recurso se ha constituido depósito de cantidad de [IMPORTE] euros, que calcula inferior a la suma del importe de la condena, que asciende a [IMPORTE] euros, y de los intereses al tipo del 20% anual desde [DÍA] de [MES] de [AÑO] hasta la fecha de notificación de sentencia.

En primer lugar, tiene que mantenerse que los intereses a que condena la sentencia, son hasta el definitivo pago, por lo que para consignar los devengados como requisito de admisibilidad del recurso, tendremos que atenernos a la fecha de dictado de la misma, puesto que con posterioridad los intereses son procesales hasta el pago, como es el criterio del art. 576 LEC.

En segundo lugar, el cálculo de la parte actora discrepa del de esta parte en que se toman días naturales, pero si la Sala tuvo por bien interpuesto el recurso, a excitación del Tribunal, conforme a la posibilidad de subsanación del art. 449.6 LEC, manifestado voluntad de cumplir (art. 231 LEC), se ingresará la cifra que se diga, que en todo caso será muy pequeña.

Debe tenerse en cuenta que, conforme a la doctrina constitucional (SSTC 344/1993 y 119/1994), la equivocación de escasa cuantía respecto del importe exacto que debiera depositarse, no autoriza a inadmitir el recurso de apelación, por desproporción absoluta entre el fin perseguido con la norma y el efecto que se provocaría, interpretándose en desfavor del derecho al recurso, dentro de la efectiva tutela judicial.

SEGUNDA.- IMPUGNACIÓN SOBRE CUANTIFICACIÓN DE LA INDEMNIZACIÓN DE LA CONDENA

La impugnación de la sentencia apelada debate la exclusión del ‘quantum’ de la indemnización concedida de pedimentos que se hicieron en la demanda, y debe mantenerse el acierto en este punto del/a Juez/a ‘a quo’, siempre para supuesto de partir de la responsabilidad del asegurado de mi mandante.

1.- No se niega que las dolencias psiquiátricas sean indemnizables, pero al no resultar aparentes, su diagnóstico tiene que proceder de un serio informe de médico especialista, después de las correspondientes pruebas indiciarias en la ciencia analítica.

A falta de constancia de tales, y puesto que el perito Dr [NOMBRE Y APELLIDOS] informó que el síndrome postraumático era una pura referencia del sujeto analizado, la conclusión de la sentencia, al eliminarlo como lesión permanente, ya que no se objetiva, es la única adecuada.

2.- Por lo que toca a las cicatrices dictaminadas es evidente que el perjuicio estético ligero del Capítulo especial debe ser el fijado de un punto básico, puesto que las cicatrices se encuentran cerca de la rodilla de la pierna derecha, lo cual no puede decirse que suponga demérito para un joven camarero de ningún tipo, o pérdida de autoestima, no resultando exageradas, y precisamente por su hiperpigmentación es que suponen un valor mínimo de perjuicio estético, que en otro caso, no tendrían en absoluto.

3.- La sentencia recurrida rechaza justamente el factor corrector por incapacidad permanente parcial, puesto que el demandante no ha quedado impedido para sus labores profesionales, ni reducido el rendimiento que puede obtener con su ocupación de camarero, ni se le ha dictaminado un sufrimiento especial para su trabajo. No se percibe de dónde pueden extraer la demanda o el escrito de impugnación semejante resultado de déficit respecto de lo normal en las tareas propias de un camarero, a menos que proceda de una siniestra descripción del síndrome de estrés postraumático que no se ha objetivado.

4.- Respecto de la eventual compensación de culpas, nos remitimos a lo manifestado en el escrito de interposición.

TERCERA.- APORTACIÓN DOCUMENTAL DEL RECURSO

Si el art. 460.1 LEC prevé que puedan acompañarse al escrito de interposición del recurso de apelación los documentos que se encuentren en alguno de los casos previstos en el art. 270, que pudieran haberse aportado anterior al juicio o vista, si entonces se conocieran o hubieran producido, y por ende cuando se han conocido o producido después de la sentencia que se apela, a pesar de que no se haga expresión de una resolución judicial del art. 271.1 LEC, puesto que su momento, aún más extraordinario, de aportación en la instancia, es hasta la sentencia, resulta lógico que también pueda acompañarse con el escrito de interposición, si se dicta o notifica después de recaída dicha sentencia apelada, como es el caso.

La relación con el objeto del proceso debe entenderse en sentido lo suficientemente amplio como para arropar que se acompañe una decisión del órgano funcionalmente competente en el asunto que, resolviendo un punto que se debate en este recurso -tipo de los intereses de mora especial cuando no se ha pagado en dos años desde el siniestro-, si bien ajeno al mismo, alcanza una conclusión influyente por su lógica y autoridad.

CUARTA.- PRUEBA EN SEGUNDA INSTANCIA

Cuando se propuso la pericia psiquiátrica por la parte actora en la instancia, que ahora se pretende reproducir en segunda instancia, y se admitió la prueba, se formuló recurso de reposición por dos razones, la una porque el método de designación judicial se considera supletorio de la pericia documentada a instancia de parte con el primer escrito expositivo (art. 336 LEC), puesto que tratándose de un dictamen que versaría sobre el estado psicofísico del actor, y habiendo multitud de profesionales dispuestos, nada indicaba tener que recurrir al órgano judicial para la designación, por el contrario de lo que acontecía con la postura de la demandada, a cuyos requerimientos de examen por médicos especializados que reclutara mi mandante siempre se ha negado el actor; y la otra, porque si se había de designar un perito médico a instancias de esta parte, cuya objeto de pericia amplió la contraparte con preguntas sobre el aspecto del síndrome psíquico que se alega, carecía de sentido complicar el proceso con otra prueba eventualmente distorsionadora.

Se salvó el derecho a reproducir la cuestión en esta alzada conforme al art. 285.2 LEC, por lo que aquí se solicita la denegación por innecesaria de la prueba, que enerva la aplicación del art. 460.2.2.ª LEC, debiéndose tener en cuenta que el actor no protestó ante la falta de nueva designación de perito psiquiátrico en diligencias finales, puesto que todavía no conocía el dictamen del perito médico que sí lo emitió, y que al no gustar de su opinión científica, se pretende tentar mejor suerte en sede de apelación, tentativa que deberá abortar el Tribunal ‘a quo’.

QUINTA.- COSTAS

Las costas de la impugnación deben ser impuestas al demandante recurrido que apela por adhesión, aplicando el criterio del vencimiento del art. 394.1 LEC, al que se remite el art. 398.1 LEC.

En virtud de cuanto antecede,

SUPLICO A LA SALA

Que, teniendo por presentado este escrito en tiempo y forma, se sirva admitirlo y tener por deducida las precedentes alegaciones frente a la impugnación de la sentencia apelada por esta parte, y

SUPLICO A LA AUDIENCIA PROVINCIAL

Que, seguido que sea el legal procedimiento, dicte sentencia que desestime en su integridad la impugnación de la sentencia apelada que formula el actor, y estime el recurso de apelación interpuesto por esta parte en los términos en que se formuló, con imposición de las costas al recurrido impugnante.

Por ser de Justicia que pido en [LUGAR], a [FECHA].

Firma de Abogado/a	Firma de Procurador/a

========================================================================
