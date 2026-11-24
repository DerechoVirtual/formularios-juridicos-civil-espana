---
name: decreto-desestima-impugnacion-tasacion-costas-civ-1947
description: "Decreto que desestima la impugnación de la tasación de costas por honorarios excesivos. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Decreto que desestima la impugnación de la tasación de costas por honorarios excesivos

> Formulario **CIV-1947** del plugin **Resoluciones judiciales civiles: autos, decretos y diligencias** (`formularios-resoluciones-judiciales-civiles`) · Civil › Resoluciones judiciales (autos, decretos, providencias, diligencias) · normativa revisada el 24-11-2026.

## Qué es

DECRETO DE ORDENACIÓN SR./A LETRADO/A DE LA ADMINISTRACIÓN DE JUSTICIA ANTECEDENTES DE HECHO RAZONAMIENTOS JURÍDICOS PARTE DISPOSITIVA Firmas Decreto aprobando la tasación de costas practicada, con desestimación total de la impugnación efectuada por considerarse excesivos los honorarios de la Letrada.

Es un modelo de tipo **resoluciones judiciales (autos, decretos, providencias, diligencias)**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Decreto que desestima la impugnación de la tasación de costas por honorarios excesivos» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Decreto que desestima la impugnación de la tasación de costas por honorarios excesivos” para mi caso». También puedes invocarla directamente con `/formularios-resoluciones-judiciales-civiles:decreto-desestima-impugnacion-tasacion-costas-civ-1947`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-resoluciones-judiciales-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Resoluciones judiciales civiles: autos, decretos y diligencias) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] FECHA (3 veces)
- [ ] LUGAR (2 veces)
- [ ] COLEGIO
- [ ] GRUPO
- [ ] IMPORTE
- [ ] NÚMERO
- [ ] ÓRGANO

## Normas que cita el formulario

- art. 246.1 LEC
- art. 32 LEC
- art. 250.1.7.º LEC
- art. 251 LEC

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

DECRETO DE ORDENACIÓN SR./A LETRADO/A DE LA ADMINISTRACIÓN DE JUSTICIA

En [LUGAR], a [FECHA].

Sr./a Letrado/a de la Administración de Justicia [NOMBRE Y APELLIDOS]

ANTECEDENTES DE HECHO

PRIMERO

Practicada tasación de costas en los presentes Autos, se dispuso dar vista de la misma a las partes, por plazo común de diez días.

SEGUNDO

Por la parte demandada, bajo representación del Procurador de los Tribunales [NOMBRE Y APELLIDOS], se impugnó la tasación de costas por excesivos los honorarios de la Letrada D./Dña. [NOMBRE Y APELLIDOS], a la que se concedió audiencia, produciendo ésta escrito en que denegaba reducir sus honorarios como se reclamaba.

TERCERO

Conforme al art. 246.1 LEC, se acordó pasar testimonio de los Autos al Iltre. Colegio de Abogados de [COLEGIO] para que emitiera el oportuno dictamen, efectuado con el resultado que obra en autos.

RAZONAMIENTOS JURÍDICOS

PRIMERO

Se parte de la premisa de que los honorarios del abogado son regulables por el mismo, en cuanto profesional libre del arrendamiento de sus servicios técnico-jurídicos, con ribetes del mandato retribuido y otras figuras, típicas y atípicas, aunque se someten a un ulterior control judicial privilegiado, dentro del proceso D./Dña. [NOMBRE Y APELLIDOS] en que se devengaron, por razón de que los servicios en cuestión fueron su presupuesto procesal, es decir, condicionante de la validez de las actuaciones judiciales (o por lo menos un derecho especialmente protegido en el proceso ex art. 32 LEC).

Este control opera en el ámbito de la discreción, sin ser vinculantes los criterios colegiales, que son informados preceptivamente (art. 246.1 LEC) pero no de manera que vinculen, por más que tampoco se imponen a los abogados, cuyo precio por los servicios que prestan es libre, dado que son las normas de los Colegios meramente orientativas.

Por ello, no existe recurso devolutivo, a pesar de la importancia del interés económico litigioso que se baraje, como la puede haber cuando se trata de una inclusión o exclusión de costas con arreglo a determinadas normas jurídicas. En lo que es un arbitrio para que un contrato bilateral no quede a la voluntad de una parte, sin que se respeten los usos, las orientaciones corporativas, o la pura racionalidad, carecería de sentido, en cuanto al fondo, un control sucesivo sin apoyos jurídicos.

SEGUNDO

Es tesis repetidamente mantenida por el Tribunal el reputar prudente atenerse siempre a la regulación de las normas orientativas que publican los colegios profesionales, por cuanto contienen un consenso corporativo que facilita la composición previa entre los Letrado/as ejercientes, que eluden estas impugnaciones ante la certeza de unos criterios objetivos.

Ocurre, no obstante, que la base de cálculo de unos honorarios, en las normas colegiales asume, para aplicar la escala gradual orientativamente fijada e indiscutida, la cuantificación de los pleitos de la Ley procesal.

En cuanto que la acción específica de protección del derecho real inmobiliario inscrito por cauce del art. 250.1.7.º LEC, las normas colegiales, pendientes de adaptación, remiten al juicio ejecutivo, y éste al declarativo por la cuantía, con sus proporciones.

No hay previsión específica en el art. 251 LEC, y no hay más remedio que recurrir a los ordinales relativos a demandas que tienen por objeto ‘garantizar el disfrute de las facultades que se derivan del dominio’ (3.ª.1.º), que remiten a la cuantía de las de condena de dar, y ésta que fija el valor del interés litigioso en el del inmueble ‘conforme a los precios corrientes en el mercado o en la contratación de bienes de la misma clase’ (2.ª, párrafo 1.º).

En el caso, la titular del crédito en costas es propietaria, y una de las facultades del derecho de propiedad -la obra de rehabilitación frente a un ocupante que lo impedía- defendió victoriosa.

El valor actual del inmueble tiene como una tasa legal el valor asignado oficialmente (art. 251.2.ª, párrafo 2.º LEC), y la tasación asume la postura del Letrado/a que minuta, y que luego documentó en el acto de la vista, y frente a la inactividad del impugnante, la casa de [NOMBRE Y APELLIDOS] está valorada en Impuesto de Patrimonio en [IMPORTE] euros.

TERCERO

La desestimación total de la impugnación supone, por disponerlo el art. 246.4, párrafo 3.º LEC, la imposición de las costas de este incidente a la parte impugnante.

PARTE DISPOSITIVA

Se aprueba la tasación de costas practicada en estos autos, con fecha [FECHA], a instancias del Procurador/a [NOMBRE Y APELLIDOS], con desestimación total de la impugnación efectuada por la parte impugnante [ÓRGANO], siendo condenada dicha parte al pago de las costas del incidente.

Así lo acuerdo y firmo.

Es justicia de hacerse en [LUGAR], a [FECHA].

Firma del Letrado/a de la Administración de Justicia

Contra esta resolución cabe interponer recurso de revisión, mediante escrito ante el Tribunal que se presentará dentro de los cinco días hábiles siguientes al de notificación, y en el que deberá indicarse la infracción cometida a juicio del recurrente, y sin perjuicio del cual se llevará a efecto lo acordado.

Para interponer el recurso será necesario la constitución de un depósito de 25 euros, sin cuyo requisito no será admitido a trámite. El depósito se constituirá consignando dicho importe en la Cuenta de Depósitos y Consignaciones que este Tribunal tiene abierta en el grupo [GRUPO] con el número [NÚMERO], indicando en el campo concepto del resguardo de ingreso que se trata de un "Recurso" código 01-Revisión. La consignación deberá ser acreditada al interponer el recurso (disp. adic. 15ª de la LOPJ).

Están exentos de constituir el depósito para recurrir los incluidos en el apartado 5 de la disposición citada y quienes tengan reconocido el derecho a la asistencia jurídica gratuita.

========================================================================
