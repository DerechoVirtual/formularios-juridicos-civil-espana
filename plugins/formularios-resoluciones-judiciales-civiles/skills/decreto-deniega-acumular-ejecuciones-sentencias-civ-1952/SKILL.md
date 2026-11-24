---
name: decreto-deniega-acumular-ejecuciones-sentencias-civ-1952
description: "Decreto que deniega acumular ejecuciones de sentencias seguidas ante distintos tribunales. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Decreto que deniega acumular ejecuciones de sentencias seguidas ante distintos tribunales

> Formulario **CIV-1952** del plugin **Resoluciones judiciales civiles: autos, decretos y diligencias** (`formularios-resoluciones-judiciales-civiles`) · Civil › Resoluciones judiciales (autos, decretos, providencias, diligencias) · normativa revisada el 24-11-2026.

## Qué es

Decreto del/de la Letrado/a de la Administración de Justicia por el que se deniega la solicitud de acumular ejecuciones que se siguen ante distintos órganos judiciales frente a un mismo deudor ejecutado, por resultar la acumulación más perjudicial para el acreedor ejecutante (art. 555.2 LEC).

Es un modelo de tipo **resoluciones judiciales (autos, decretos, providencias, diligencias)**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Decreto que deniega acumular ejecuciones de sentencias seguidas ante distintos tribunales» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Decreto que deniega acumular ejecuciones de sentencias seguidas ante distintos tribunales” para mi caso». También puedes invocarla directamente con `/formularios-resoluciones-judiciales-civiles:decreto-deniega-acumular-ejecuciones-sentencias-civ-1952`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-resoluciones-judiciales-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Resoluciones judiciales civiles: autos, decretos y diligencias) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] AÑO (4 veces)
- [ ] Nº DE PROCEDIMIENTO (3 veces)
- [ ] SEDE (3 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] FECHA (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] Nº (2 veces)
- [ ] DÍA
- [ ] MES
- [ ] NIG
- [ ] Nº DE CUENTA
- [ ] Nº DE GRUPO
- [ ] PARTES

## Normas que cita el formulario

- art. 555.2 LEC
- art. 610 LEC

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

SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

Procedimiento: Ejecución de Título no Judicial n.º [Nº DE PROCEDIMIENTO] / [AÑO]

Número de Identificación Informática: [NIG]

Partes: [PARTES]

DECRETO DEL/DE LA LETRADO/A DE LA ADMINISTRACIÓN DE JUSTICIA

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Sr./a. Letrado/a de la Administración de Justicia [NOMBRE Y APELLIDOS]

HECHOS

PRIMERO.- Por el/la Procurador/a de los Tribunales Sr./a [NOMBRE Y APELLIDOS], en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS], se ha presentado escrito en solicitud de la acumulación de esta ejecución a la siguiente:

Tribunal en que se tramita: Sección Civil del Tribunal de Instancia n.º [Nº] de los de [SEDE]

Número: [Nº DE PROCEDIMIENTO] / [AÑO]

Parte ejecutante: D./Dña. [NOMBRE Y APELLIDOS]

Parte ejecutada: [DENOMINACIÓN SOCIAL]

Fecha de presentación de demanda ejecutiva: [FECHA]

SEGUNDO.- De dicha solicitud se ha dado traslado a las partes personadas en esta ejecución para que en el plazo de diez días alegaran lo que estimaran pertinente sobre la acumulación solicitada, dentro de cuyo plazo no se produjo escrito de la representación de D./Dña. [NOMBRE Y APELLIDOS], ejecutante, por el que se opusiera a dicha acumulación.

FUNDAMENTOS DE DERECHO

PRIMERO.- Regula el art. 555.2 LEC la acumulación de ejecuciones que se siguen frente al mismo deudor ejecutado, siendo los acreedores ejecutantes distintos, disponiendo que se procederá a la acumulación si el/la Letrado/a de la Administración de Justicia competente en el proceso más antiguo lo considera más conveniente para la satisfacción de todos los acreedores ejecutantes.

En el presente caso, se estima que no procede acceder a la acumulación solicitada porque se reputa no concurrir esa exigencia legal de conveniencia, sino, muy al contrario, perjuicio para el acreedor ejecutante en este proceso y confusión de embargos. Debe tenerse en cuenta que no hay previsión legal de un convenio entre acreedores ejecutantes para el reparto del resultado del apremio, y que las sumas recaudadas en esta ejecución no alcanzan a satisfacer toda la suma de créditos ejecutivos. Habiéndose trabado embargo de derechos de [DENOMINACIÓN SOCIAL] en esta ejecución y en la que se pide que se acumule, en distintas fechas y por distintas cantidades, no habiendo una prioridad de orden registral, y siendo las fechas de las sentencias que son títulos ejecutivos jurisdiccionales de precedencia en el tiempo inversa a la de precedencia de la incoación del despacho de ejecución (es decir, más antigua esta ejecución por sentencia de condena más moderna, ya que no fue recurrida), se produce un fenómeno de preferencia material crediticia, siendo de naturaleza aparentemente idéntica los créditos de los ejecutantes que habrían de acumular sus pretensiones, sólo solventable a través del mecanismo de tercería. Además, las ejecuciones de que se hace eco el solicitante de la acumulación contribuyen a apuntar la existencia de créditos ejecutivos preferentes en calidad y anteriores en el tiempo, por lo que es verosímil que aparezcan embargos intermedios entre el de esta ejecución y el de la ulterior.

Procede, pues, denegar la acumulación de ejecuciones frente a la mercantil sin suficiente solvencia, y recomendar reembargo o embargo del sobrante ex arts. 610 y 611 LEC.

SEGUNDO.- Nada excluye la imposición de las costas procesales al promotor del incidente por el criterio general del vencimiento.

Vistas las normas citadas y demás de aplicación,

PARTE DISPOSITIVA

1.- SE DENIEGA la solicitud formulada por el/la Procurador/a de los Tribunales Sr./a [NOMBRE Y APELLIDOS], de acumular a esta ejecución la que se encuentra en la Sección Civil del Tribunal de Instancia n.º [Nº] de los de [SEDE], con el n.º [Nº DE PROCEDIMIENTO] / [AÑO], las cuales continuarán sustanciándose separadamente.

2.- Se pronuncia el reintegro de las costas a cargo de la parte solicitante.

Contra esta resolución cabe interponer recurso de reposición, mediante escrito ante el/la Letrado/a de la Administración de Justicia que se presenta dentro de los cinco días hábiles siguientes al de notificación, y en el que deberá indicarse la infracción cometida a juicio del recurrente, y sin perjuicio del cual se llevará a efecto lo acordado.

Para interponer el recurso será necesaria la constitución de un depósito de 25 euros, sin cuyo requisito no será admitido a trámite. El depósito se constituirá consignando dicho importe en la Cuenta de Depósitos y Consignaciones que este Tribunal tiene abierta en el grupo [Nº DE GRUPO] con el número [Nº DE CUENTA], indicando en el campo concepto del resguardo de ingreso que se trata de un "Recurso" código 00-Reposición. La consignación deberá ser acreditada al interponer el recurso (disp. adic. 15.ª de la LOPJ).

Están exentos de constituir el depósito para recurrir los incluidos en el apartado 5 de la disposición citada y quienes tengan reconocido el derecho a la asistencia jurídica gratuita.

Así lo acuerdo y firmo:

Por ser de justicia, lo pido en [LOCALIDAD], a [FECHA].

Firma del Letrado/a de la Administración de Justicia:
