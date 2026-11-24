---
name: decreto-faculta-ejecutante-adquirir-cosas-genericas-civ-2040
description: "Decreto que faculta al ejecutante a adquirir cosas genéricas a costa del ejecutado y embarga bienes. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Decreto que faculta al ejecutante a adquirir cosas genéricas a costa del ejecutado y embarga bienes

> Formulario **CIV-2040** del plugin **Resoluciones judiciales civiles: autos, decretos y diligencias** (`formularios-resoluciones-judiciales-civiles`) · Civil › Resoluciones judiciales (autos, decretos, providencias, diligencias) · normativa revisada el 24-11-2026.

## Qué es

Auto acordando facultar al ejecutante para que adquiera, a costa del ejecutado, las cosas genéricas o indeterminadas objeto de ejecución y decretando el embargo de bienes propiedad del ejecutado y que han sido reseñados en el escrito del ejecutante, en cuanto sean suficientes para pagar la adquisición.

Es un modelo de tipo **resoluciones judiciales (autos, decretos, providencias, diligencias)**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Decreto que faculta al ejecutante a adquirir cosas genéricas a costa del ejecutado y embarga bienes» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Decreto que faculta al ejecutante a adquirir cosas genéricas a costa del ejecutado y embarga bienes” para mi caso». También puedes invocarla directamente con `/formularios-resoluciones-judiciales-civiles:decreto-faculta-ejecutante-adquirir-cosas-genericas-civ-2040`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-resoluciones-judiciales-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Resoluciones judiciales civiles: autos, decretos y diligencias) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (4 veces)
- [ ] IMPORTE (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] DESCRIBIR
- [ ] DESCRIPCIÓN DEL BIEN
- [ ] GRUPO
- [ ] LUGAR
- [ ] NÚMERO
- [ ] PLAZO

## Normas que cita el formulario

- art. 702.1 LEC

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

DECRETO DEL LETRADO/A DE LA ADMINISTRACIÓN DE JUSTICIA

En [LUGAR], a [FECHA].

Sr./a Letrado de la Administración de Justicia [NOMBRE Y APELLIDOS]

ANTECEDENTES DE HECHO

PRIMERO.- El pasado día [FECHA] se dictó auto despachando ejecución con la finalidad de que el ejecutado hiciera entrega al ejecutante de cosas genéricas o indeterminadas consistentes en [DESCRIBIR], de acuerdo con lo ordenado en la sentencia firme dictada por este Tribunal en fecha [FECHA]. En dicha resolución se dio al ejecutado un plazo de [PLAZO] para cumplir con lo estipulado en la sentencia.

SEGUNDO.- Ha transcurrido el plazo concedido al ejecutado para cumplir con la obligación de entrega, sin que hasta la fecha se haya dado cumplimiento a lo dispuesto en las resoluciones mencionadas. Ante tal circunstancia el ejecutante presentó escrito en fecha [FECHA], en el que solicitaba que se le faculte para adquirir, a costa del ejecutado, las cosas genéricas o indeterminadas objeto de la presente ejecución, ordenándose al mismo tiempo el embargo de bienes suficientes para pagar la adquisición.

FUNDAMENTOS DE DERECHO

PRIMERO.- Como se ha indicado en los antecedentes de hecho, el ejecutado D./Dña. [NOMBRE Y APELLIDOS] no ha cumplido la sentencia voluntariamente ya que no procedió a la entrega de los bienes a lo que fue condenado, ni tampoco ha atendido el requerimiento formulado al efecto, lo que ha dado lugar a que la parte cuya pretensión prosperó haya solicitado que se le autorice a costa de aquél a adquirir los bienes siguientes [DESCRIPCIÓN DEL BIEN], que debieron ser entregados por el ejecutado.

SEGUNDO.- Procede acceder a su petición porque concurren las exigencias legales contenidas en el artículo 702.1 de la LEC, ya que, además de la no entrega, el objeto u objetos referidos son de naturaleza genérica, lo que significa falta de individualización o determinación, por lo que pueden ser sustituidos por otros iguales mediante su compra. En consecuencia, se autoriza al ejecutante a que pueda adquirir, a costa del condenado a la entrega, los referidos bienes, acordando a su vez el embargo de bienes de este último en cantidad de [IMPORTE], a la que podrá ascender la adquisición de aquéllos de conformidad con la documentación aportada por el ejecutante, acreditativa, aunque solo sea por aproximación, de cuál pueda ser el precio de compra de los mismos. Adquisición de la que deberá dar cuenta justificada.

PARTE DISPOSITIVA

En atención a todo lo anterior SE ACUERDA tener por presentado el anterior escrito que se unirá a los autos de su razón y, en su virtud, se faculta al ejecutante para que adquiera, a costa del ejecutado, las cosas genéricas o indeterminadas consistentes en

Se decreta el embargo de bienes propiedad del ejecutado y que han sido reseñados en el escrito del ejecutante, en cuanto sean suficientes para pagar la adquisición, calculada en [IMPORTE] euros ( €) y de la que, una vez llevada a efecto, dará cuenta justificada el ejecutante.

Así lo acuerdo y firmo:

Firma del Letrado/a de la Administración de Justicia:

Contra esta resolución cabe interponer recurso de reposición, mediante escrito ante el LAJ que se presenta dentro de los cinco días hábiles siguientes al de notificación, y en el que deberá indicarse la infracción cometida a juicio del recurrente, y sin perjuicio del cual se llevará a efecto lo acordado.

Para interponer el recurso será necesario la constitución de un depósito de 25 euros, sin cuyo requisito no será admitido a trámite. El depósito se constituirá consignando dicho importe en la Cuenta de Depósitos y Consignaciones que este Tribunal tiene abierta en el grupo [GRUPO] con el número [NÚMERO], indicando en el campo concepto del resguardo de ingreso que se trata de un "Recurso" código 00-Reposición. La consignación deberá ser acreditada al interponer el recurso (disp. adic. 15.ª de la LOPJ).

Están exentos de constituir el depósito para recurrir los incluidos en el apartado 5 de la disposición citada y quienes tengan reconocido el derecho a la asistencia jurídica gratuita.

========================================================================
