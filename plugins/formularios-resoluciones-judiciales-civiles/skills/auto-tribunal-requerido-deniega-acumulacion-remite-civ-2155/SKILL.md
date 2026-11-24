---
name: auto-tribunal-requerido-deniega-acumulacion-remite-civ-2155
description: "Auto del tribunal requerido que deniega la acumulación y remite los autos al tribunal superior. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Auto del tribunal requerido que deniega la acumulación y remite los autos al tribunal superior

> Formulario **CIV-2155** del plugin **Resoluciones judiciales civiles: autos, decretos y diligencias** (`formularios-resoluciones-judiciales-civiles`) · Civil › Resoluciones judiciales (autos, decretos, providencias, diligencias) · normativa revisada el 24-11-2026.

## Qué es

Auto del Tribunal requerido de acumulación, denegándola por estimarla improcedente para el juicio que se sigue en dicho Tribunal y trasladando los autos al Tribunal superior.

Es un modelo de tipo **resoluciones judiciales (autos, decretos, providencias, diligencias)**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Auto del tribunal requerido que deniega la acumulación y remite los autos al tribunal superior» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Auto del tribunal requerido que deniega la acumulación y remite los autos al tribunal superior” para mi caso». También puedes invocarla directamente con `/formularios-resoluciones-judiciales-civiles:auto-tribunal-requerido-deniega-acumulacion-remite-civ-2155`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-resoluciones-judiciales-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Resoluciones judiciales civiles: autos, decretos y diligencias) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NÚMERO (6 veces)
- [ ] AÑO (3 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] SEDE (3 veces)
- [ ] NOMBRE DE LA PARTE (2 veces)
- [ ] ACTO O RESOLUCIÓN
- [ ] DENOMINACIÓN SOCIAL
- [ ] FECHA
- [ ] GRUPO
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] Nº
- [ ] Nº DE PROCEDIMIENTO

## Normas que cita el formulario

- art. 91 LEC
- art. 77.1 LEC
- art. 93.1 LEC

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

- Junto a «…PRIMERO Por la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. «De los de» es residuo de los varios juzgados de una plaza. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

AUTO

En [LUGAR], a [FECHA].

Ilmo. Sr./a. Magistrado- Juez D./Dña. [NOMBRE Y APELLIDOS]

ANTECEDENTES DE HECHO

PRIMERO

Por la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº] , se ha requerido la remisión al mismo del presente juicio verbal n.º [NÚMERO]/[AÑO], promovido por D./Dña. [NOMBRE Y APELLIDOS] frente a [ACTO O RESOLUCIÓN], sobre responsabilidad civil, para su acumulación al que se sigue en dicho Tribunal como juicio ordinario bajo el n.º [NÚMERO]/[AÑO], promovido por [NOMBRE DE LA PARTE],frente a D./Dña. [NOMBRE Y APELLIDOS], también sobre responsabilidad civil.

SEGUNDO

Recibidos el oficio acompañado dicho oficio del testimonio de los antecedentes que el Tribunal requirente determinó como bastantes para dar a conocer la causa por la que se decretó la acumulación, se dio traslado a las partes personadas en los presentes autos.

TERCERO

Por la demandada [NOMBRE DE LA PARTE] se formuló alegaciones, en legales tiempo y forma, oponiéndose a la acumulación por no ser posible acumular declarativos de distinta clase, como un juicio verbal a un juicio ordinario, las cuales constan en el incidente.

FUNDAMENTOS DE DERECHO

PRIMERO

Con arreglo al art. 91 LEC transcurrido el plazo de instrucción de cinco días de las partes no personadas en el proceso ante el tribunal requirente, el tribunal dictará auto aceptando o denegando el requerimiento de acumulación.

Manifiesta la mercantil demandada [DENOMINACIÓN SOCIAL] que no procede la acumulación acordada por la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [NÚMERO], dado que se pretende la de este juicio verbal a un juicio ordinario, y siendo lo que se reclama cantidad de 890 euros, y domiciliada la actora en esta plaza, de resultar íntegramente estimada la demanda en un juicio verbal, no tendría que reintegrar, como costas debidas, el gasto de profesionales no preceptivos, como lo tendría que hacer en un juicio ordinario.

Dispone el art. 77.1 LEC que sólo procederá la acumulación de procesos declarativos que se sustancien por los mismos trámites, o cuya tramitación pueda unificarse sin pérdida de derechos procesales, resultando en el caso que si se unificara este juicio verbal al trámite del juicio ordinario del Tribunal requirente, se haría pechar a la demandada opuesta ante este requerido con una complejidad, dilación y costo por el proceso que le privaría de sus derechos, no compartiéndose la tesis de la resolución del órgano requirente sobre que es viable acumular un juicio verbal al ordinario, que se sustanciará por los trámites del segundo, de mayores garantías, y no a la inversa, puesto que si así fuera el criterio legal se hubiera expresado.

SEGUNDO

Conforme a lo dispuesto en el art. 93.1 LEC, se comunicará la no aceptación de la acumulación al tribunal requirente, con el que se deferirá la decisión definitiva al tribunal, que con arreglo al art. 93.2, será el inmediato superior común a requirente y requerido.

Vistos los preceptos legales citados y demás de pertinente aplicación.

PARTE DISPOSITIVA

1.- Se deniega el requerimiento de acumulación formulado por la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [NÚMERO], para la remisión al mismo del presente juicio, por estimarla improcedente para el juicio que se sigue en dicho Tribunal con el n.º [NÚMERO]/[AÑO].

2.- Comuníquese al Tribunal requirente la denegación, a fin de que remita, a la mayor brevedad, a la Ilma. Audiencia Provincial de [LOCALIDAD], testimonio bastante de las actuaciones para la resolución de la discrepancia planteada.

3.- Remítase a dicho tribunal superior, y a los mismos fines, testimonio de los siguientes particulares: presente incidente, demanda y documentos que la acompañan, y presentes autos de juicio verbal [Nº DE PROCEDIMIENTO], de lo que se desprende la incompetencia territorial del Tribunal requirente.

4.- Emplácese a las partes para que, en el plazo improrrogable de cinco días puedan comparecer ante dicho tribunal y alegar por escrito lo que consideren conviene a su derecho.

Así lo acuerdo, mando y firmo:

Firma del Juez:

Contra la presente resolución cabe interponer, en el plazo de cinco días siguientes al de notificación de la presente, recurso de reposición ante el mismo Tribunal, mediante escrito que debe expresar la infracción cometida a juicio del recurrente, y que carecerá de efectos suspensivos.

Para interponer el recurso será necesario la constitución de un depósito de 25 euros, sin cuyo requisito no será admitido a trámite. El depósito se constituirá consignando dicho importe en la Cuenta de Depósitos y Consignaciones que este Tribunal tiene abierta en el grupo [GRUPO] con el número [NÚMERO], indicando en el campo concepto del resguardo de ingreso que se trata de un "Recurso" código 00-Reposición. La consignación deberá ser acreditada al interponer el recurso (disp. adic. 15.ª de la LOPJ).

Están exentos de constituir el depósito para recurrir los incluidos en el apartado 5 de la disposición citada y quienes tengan reconocido el derecho a la asistencia jurídica gratuita

========================================================================
