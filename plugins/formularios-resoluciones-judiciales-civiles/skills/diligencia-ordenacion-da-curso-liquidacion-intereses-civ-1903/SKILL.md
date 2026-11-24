---
name: diligencia-ordenacion-da-curso-liquidacion-intereses-civ-1903
description: "Diligencia de ordenación que da curso a la liquidación de intereses sin demanda ejecutiva previa. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Diligencia de ordenación que da curso a la liquidación de intereses sin demanda ejecutiva previa

> Formulario **CIV-1903** del plugin **Resoluciones judiciales civiles: autos, decretos y diligencias** (`formularios-resoluciones-judiciales-civiles`) · Civil › Resoluciones judiciales (autos, decretos, providencias, diligencias) · normativa revisada el 24-11-2026.

## Qué es

Diligencia de ordenación del Letrado de la Administración de Justicia dando traslado de la liquidación de intereses presentada a la parte ejecutada, para que pueda contestar lo que estime conveniente.

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Diligencia de ordenación que da curso a la liquidación de intereses sin demanda ejecutiva previa» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Diligencia de ordenación que da curso a la liquidación de intereses sin demanda ejecutiva previa” para mi caso». También puedes invocarla directamente con `/formularios-resoluciones-judiciales-civiles:diligencia-ordenacion-da-curso-liquidacion-intereses-civ-1903`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-resoluciones-judiciales-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Resoluciones judiciales civiles: autos, decretos y diligencias) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] DENOMINACIÓN SOCIAL (3 veces)
- [ ] FECHA (3 veces)
- [ ] IMPORTE (3 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] AÑO
- [ ] CALLE
- [ ] GRUPO
- [ ] LUGAR
- [ ] Nº

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

SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA N.º [NÚMERO]

Villa de [LOCALIDAD]

CALLE [CALLE] TELÉFONO:

N.I.G.:

Procedimiento: JUICIO ORDINARIO [Nº] / [AÑO]

Descripción de la pieza:

Procedimiento origen:

Demandante: Procurador/a:

Demandado: SEGUROS GENERALES [DENOMINACIÓN SOCIAL], S.A. Procurador/a:

DILIGENCIA.-

En la Villa de [LOCALIDAD], a [FECHA]

La extiendo yo, la LAJ para hacer constar que por el/la Procurador Sr./a. en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS], se ha presentado escrito solicitando la liquidación de intereses. Doy fe.

DILIGENCIA DE ORDENACIÓN

Letrado de la Administración de Justicia QUE LA DICTA: D./Dña [NOMBRE Y APELLIDOS]

En [LUGAR], a [FECHA]
Fecha:

1.- Por presentado el anterior escrito por el Procurador Sr/a [NOMBRE Y APELLIDOS], junto con justificante de haberse entregado copia al Procurador de la parte contraria personada, únase a los autos de su razón.

2.- En lo referente a la petición formulada e identificada bajo el ordinal 1, atendido que Seguros Generales [DENOMINACIÓN SOCIAL], S.A., con fecha [FECHA], y con el fin de recurrir en apelación la sentencia dictada, realizó dos consignaciones, una por importe de [IMPORTE] xxx. € y otra por importe de [IMPORTE] yyy [IMPORTE] €, coincidiendo la primera con el principal fijado en la sentencia y considerándose que la segunda es la cantidad presupuestada por la parte demandada para hacer frente a la condena de intereses, se concede a Seguros Generales [DENOMINACIÓN SOCIAL], S.A., un plazo de TRES días a fin de que manifieste lo que a su derecho convenga, apercibiéndole que en otro caso se procederá de conformidad con lo solicitado.

3.- No ha lugar a lo solicitado bajo los ordinales 2 y 3, debiéndose reiterar la petición, en su caso como demanda ejecutiva, una vez fijados los intereses.

4.- Dése traslado de la liquidación de intereses presentada a la parte ejecutada, para que, en el plazo de DIEZ DÍAS, pueda contestar lo que estime conveniente.

5.- Adviértase a dicha parte que se entenderá que presta su conformidad a la relación presentada por la parte ejecutante, si deja pasar el plazo sin evacuar el traslado, o si, se limita a negar genéricamente la existencia de intereses, sin contestar los puntos en que se discrepa de la relación presentada por el acreedor, ni expresa las razones y el alcance de la discrepancia.

En cualquiera de los casos anteriores, se aprobará la liquidación del ejecutante y se hará efectiva en la forma establecida para las condenas dinerarias.

Contra esta resolución cabe interponer recurso de reposición, mediante escrito ante el LAJ, que se presentará dentro de los cinco días hábiles siguientes al de notificación, y en el que deberá indicarse la infracción cometida a juicio del recurrente, sin perjuicio del cual se llevará a efecto lo acordado.

Para interponer el recurso será necesario la constitución de un depósito de 25 euros, sin cuyo requisito no será admitido a trámite. El depósito se constituirá consignando dicho importe en la Cuenta de Depósitos y Consignaciones que este Tribunal tiene abierta en el grupo [GRUPO] con el número [NÚMERO], indicando en el campo concepto del resguardo de ingreso que se trata de un "Recurso" código 00-Reposición. La consignación deberá ser acreditada al interponer el recurso (disp. adic. 15.ª de la LOPJ).

Están exentos de constituir el depósito para recurrir los incluidos en el apartado 5 de la disposición citada y quienes tengan reconocido el derecho a la asistencia jurídica gratuita.

Lo dispongo y firmo. Doy fe.

Firma del Letrado/a de la Administración de Justicia:

========================================================================
