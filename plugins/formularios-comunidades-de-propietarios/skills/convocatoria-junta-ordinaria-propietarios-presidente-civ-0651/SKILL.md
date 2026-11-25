---
name: convocatoria-junta-ordinaria-propietarios-presidente-civ-0651
description: "Convocatoria de junta ordinaria de propietarios por el presidente de la comunidad. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Convocatoria de junta ordinaria de propietarios por el presidente de la comunidad

> Formulario **CIV-0651** del plugin **Comunidades de propietarios** (`formularios-comunidades-de-propietarios`) · Civil › Propiedad horizontal · normativa revisada el 25-11-2026.

## Qué es

Escrito de comunicación de convocatoria de la Junta Ordinaria de Propietarios realizada por el presidente de la comunidad, incluyendo los puntos a tratar en el orden del día.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Convocatoria de junta ordinaria de propietarios por el presidente de la comunidad» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Convocatoria de junta ordinaria de propietarios por el presidente de la comunidad” para mi caso». También puedes invocarla directamente con `/formularios-comunidades-de-propietarios:convocatoria-junta-ordinaria-propietarios-presidente-civ-0651`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-comunidades-de-propietarios:indice`.

## Qué contiene esta skill

- `SKILL.md` (este fichero): qué es el formulario, para qué sirve, cómo se usa, los datos que pide, las normas que cita, los avisos de actualización y las instrucciones para Claude.
- `assets/formulario.md`: el formulario seco, tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…]. Es el texto que se rellena; no lleva explicaciones.
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Comunidades de propietarios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (2 veces)
- [ ] CALLE
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] MES
- [ ] Nº
- [ ] Nº DE PISO
- [ ] NÚMERO
- [ ] PUNTO DEL ORDEN DEL DÍA

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

Escrito de comunicación de convocatoria de la Junta Ordinaria de Propietarios realizada por el presidente de la comunidad, incluyendo los puntos a tratar en el orden del día.

Notas al pie del formulario original:
(1) A) Se acompañará a esta citación la correspondiente delegación en los siguientes términos:

«El propietario D./Dña. [NOMBRE Y APELLIDOS]..., del piso ..., local ..., garaje ..., etc., de la Comunidad de propietarios de la calle ..., nº [NÚMERO DE LA CALLE], de ..., concede autorización expresa a D./Dña. [NOMBRE Y APELLIDOS]..., con D.N.I. nº [DNI/NIE], para la asistencia, deliberación y votación en la Junta Ordinaria que se celebrará el día [FECHA]..., en el lugar y hora indicado en la correspondiente citación».

B) La Junta de Propietarios se reunirá al menos una vez al año para aprobar los presupuestos y cuentas y en las demás ocasiones en que lo considere conveniente el Presidente o lo pidan la cuarta parte de los propietarios, o un número de éstos que representen al menos el 25 por 100 de las cuotas de participación.

La convocatoria contendrá una relación de los propietarios que no estén al corriente en el pago de las deudas vencidas a la Comunidad y advertirá de la privación del derecho de voto.

Si a la reunión de la Junta no concurriesen, en primera convocatoria, la mayoría de los propietarios que representen a su vez, la mayoría de las cuotas de participación, se procederá a una segunda convocatoria de la misma, esta vez sin sujeción a quórum.

La citación para la Junta Ordinaria anual se hará, cuando menos, con seis días de antelación, y para las extraordinarias, con la que sea posible para que pueda llegar a conocimiento de todos los interesados. La Junta podrá reunirse válidamente aun sin la convocatoria del Presidente, siempre que concurran la totalidad de los propietarios y así lo decidan.

(2) Normativa aplicable

Artículos 15, 16 y 17 de la Ley 49/1960, de 21 de julio, de Propiedad Horizontal (LPH)

(3) Notas de interés

La convocatoria de una Junta de Propietarios puede efectuarse de varias formas, pero siempre y en todo caso se debe, para no incurrir en nulidad, convocar a todos los propietarios, por lo que en caso de posibles discrepancias debe hacerse por carta certificada o mejor por el sistema de burofax, de cuyo contenido queda perfecta constancia.

El día, hora y lugar de celebración, si es ordinaria o extraordinaria, así como los asuntos a tratar y cuándo es en primera y cuándo en segunda convocatoria, son otros de los elementos esenciales.

Son habituales las sentencias por las que se anulan Juntas de Propietarios, por no haberse convocado de acuerdo con lo establecido en el artículo 16 de la Ley 49/1960, de 21 de julio, de Propiedad Horizontal (LPH), o haber adoptado acuerdos en contra de lo regulado en el artículo 17.

La convocatoria tiene que hacerse si es de Junta Ordinaria, con un mínimo de seis días de antelación, de forma que entre el día de la convocatoria y el día de la Junta haya en medio seis días naturales como mínimo, y si es Extraordinaria, con aquella suficiente antelación, teniendo en cuenta su urgencia, que pueda justificar a los promotores que la han solicitado con un plazo suficientemente espacioso como para que llegue a conocimiento de todos y que todos puedan previamente a la reunión tener conocimiento de los asuntos a tratar. Se recomienda, salvo casos de urgencia, nunca hacerlo con menos de ocho días de intermedio entre la convocatoria y la reunión, salvo que como queda dicho existan motivos de urgencia.

La Junta puede ser convocada por el Presidente o incluso por los propietarios que representen un mínimo del 25 por 100 de todos los propietarios de la Comunidad o que representen el 25 por 100 de las cuotas de participación, pudiendo en estos dos últimos casos enviar ellos mismos la convocatoria.

También es válida la reunión, aún sin convocatoria si están presentes todos los propietarios, y así expresamente lo acuerdan. Es decir, no sólo es necesario que estén todos, sino que expresamente acuerden celebrar Asamblea y aprueben los asuntos concretos a tratar.

(4) Jurisprudencia de interés

— Audiencia Provincial de A Coruña, Sección 4ª, Sentencia 177/2014 de 5 Jun. 2014, Rec. 181/2014 "siendo las normas sobre convocatoria de Junta de naturaleza imperativa y necesario cumplimiento, según reiterada jurisprudencia del Tribunal Supremo."

— Tribunal Supremo, Sala Primera, de lo Civil, Sentencia de 12 Ene. 2012, rec. 1070/2009 "La jurisprudencia fijada por esta Sala, en torno a la aplicación del actual artículo 16.2 LPH, tal y como pone de relieve la parte recurrente, considera exigible que en el orden del día de la convocatoria de la junta de propietarios se fijen con claridad los asuntos objeto de debate, a fin de que todos los copropietarios tengan conocimiento de las materias que se van a tratar."

— Tribunal Supremo, Sala Primera, de lo Civil, Sentencia de 18 Mar. 2010, rec. 1403/2006: "Ahora bien, si, como se ha mencionado anteriormente, no resulta exigible un grado de detalle exhaustivo en el orden del día, de tal manera que en la Junta se pueda tratar cualquier cuestión que resulte consecuencia directa de lo expresado en aquél (...)"

— No obstante lo dispuesto en el artículo 15 de la L.P.H. se ha dado validez en resoluciones, como la de la A.P. de Madrid, de 2 de noviembre de 1992, a toda utilización de medios de comunicación que racionalmente permitan a los comuneros tener conocimiento de su celebración y asuntos a tratar, llegando a dar por válida la convocatoria, hecha a través de anuncios en el tablón colocado en la comunidad al efecto o por entrega de la citación en los buzones de los domicilios. (Sentencia A.P. de Ciudad Real de 11 de diciembre de 1995, Rec. 32/1995)

— Pueden convocar la Junta, si antes se ha solicitado al presidente la convocatoria y este no la ha realizado, los propietarios que representen la cuarta parte o, al menos, el 25 por 100 de las cuotas. Sentencia A.P. de Madrid de 16 de mayo de 2011: "Toda vez, para poder estimar al Sr. Abel válidamente elegido como Presidente de la Comunidad de Propietarios, y, por ende, poder representarla, de partida se hace preciso que la convocatoria de la Junta se hubiese llevado a cabo por el quórum de propietarios a que hace referencia el art. 16 LPH, a saber, la cuarta parte de los propietarios o un número de estos que representen al menos el 25 por 100 de las cuotas de participación."

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
