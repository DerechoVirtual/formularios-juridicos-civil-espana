---
name: decreto-cese-procurador-revocacion-poder-impugnada-civ-1930
description: "Decreto de cese del procurador por revocación del poder impugnada por él. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Decreto de cese del procurador por revocación del poder impugnada por él

> Formulario **CIV-1930** del plugin **Resoluciones judiciales civiles: autos, decretos y diligencias** (`formularios-resoluciones-judiciales-civiles`) · Civil › Resoluciones judiciales (autos, decretos, providencias, diligencias) · normativa revisada el 24-11-2026.

## Qué es

Decreto teniendo por cesado al Procurador por la revocación expresa o tácita del poder, la cual ha sido impugnada por el Procurador cesado.

Es un modelo de tipo **resoluciones judiciales (autos, decretos, providencias, diligencias)**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Decreto de cese del procurador por revocación del poder impugnada por él» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Decreto de cese del procurador por revocación del poder impugnada por él” para mi caso». También puedes invocarla directamente con `/formularios-resoluciones-judiciales-civiles:decreto-cese-procurador-revocacion-poder-impugnada-civ-1930`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-resoluciones-judiciales-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Resoluciones judiciales civiles: autos, decretos y diligencias) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] FECHA (4 veces)
- [ ] NÚMERO (4 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] ÓRGANO (2 veces)
- [ ] ACTO O RESOLUCIÓN
- [ ] AÑO
- [ ] GRUPO
- [ ] LUGAR
- [ ] NOMBRE DE LA PARTE

## Normas que cita el formulario

- art. 30.1.1.º LEC

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

PROCEDIMIENTO: Juicio Ordinario n.º [NÚMERO]/[AÑO]

Número de Identificación informática:

PARTES: Demandante [ÓRGANO]

Procurador

Demandado [NOMBRE DE LA PARTE]

Procurador

DECRETO DEL LETRADO DE LA ADMINISTRACIÓN DE JUSTICIA

En [LUGAR], a [FECHA].

El Sr. Letrado de la Administración de Justicia de la Sección Civil del Tribunal de Instancia n.º [NÚMERO].

ANTECEDENTES DE HECHO

Primero

Mediante comparecencia ante la Secretaría de este Tribunal de fecha [FECHA] la sociedad demandante en el presente proceso, S.L., confirió su representación procesal apud ‘acta’ al/a la Procurador/a de los Tribunales Don/Doña [NOMBRE Y APELLIDOS], al momento de interponer la demanda.

Segundo

Con fecha [FECHA], el/la Procurador/a de los Tribunales Don/Doña [NOMBRE Y APELLIDOS] presentó escrito por el que, acompañando poder de representación notarial de la mercantil demandante, solicitaba tener por cesado al anterior mandatario procesal, su compañero Don/Doña [NOMBRE Y APELLIDOS], del que se dio traslado a éste, que formuló alegaciones por las que impugnaba la existencia y validez de la nueva representación.

Tercero

Mediante diligencia de ordenación de fecha [FECHA], el tribunal acordó dar audiencia al otorgante de los respectivos poderes, al objeto de resolver sobre la cuestión planteada por la representación procesal de [DENOMINACIÓN SOCIAL], S.L., manifestando ésta lo que tuvo por conveniente en escrito presentado dentro del plazo conferido, y que se dan por reproducidos.

RAZONAMIENTOS JURÍDICOS

PRIMERO

Establece el art. 30.1.1.º LEC que cesará el Procurador en su representación por la revocación expresa o tácita del poder, una vez que conste en autos; entendiéndose revocado tácitamente el poder por el nombramiento posterior de otro Procurador que se haya personado en el asunto. Es decir, si el poder es una declaración de voluntad unilateral de valerse del representante técnico que marca la Ley, la declaración de voluntad contraria, de querer dejar de valerse del representante elegido, valdrá lo mismo en el proceso, cuando a éste acceda en la determinada forma correlativa a las posibilidades iniciales (escritura notarial, comparecencia ante el LAJ, o designación colegial). Pero se prevé la fórmula de declaración de voluntad presunta o tácita, por el acto propio concluyente de nombrar otro mandatario y que éste se persone en autos.

SEGUNDO

Trasladado un escrito de personación que acompañaba un nuevo poder de mandato procesal, éste notarial para pleitos, otorgado a favor del/de la Procurador/a Sr/Sra [NOMBRE Y APELLIDOS], el designado anteriormente, Procurador Sr./Sra. [NOMBRE Y APELLIDOS], mandatario por comparecencia ‘apud acta’, opuso a la revocación tácita que no existía el nuevo apoderamiento, y que no era válido, de existir, por cuanto demuestra documentalmente un pacto de irrevocabilidad.

En cuanto a la nueva representación, no puede dudarse que existe, porque el nuevo poder para pleitos se otorga por el consejero delegado de [DENOMINACIÓN SOCIAL], S.L., según consta autorizado por la fe pública notarial, siendo indiferente que el director gerente, con poder mercantil inscrito, otorgara anteriormente en comparecencia ‘apud acta’. Y en cuanto a la validez, es unánime la doctrina en negar eficacia al pacto de irrevocabilidad del poder para pleitos, por lo que, sin perjuicio de la acción de daños y perjuicios del Procurador contra [ACTO O RESOLUCIÓN], S.L., al haber incumplido su compromiso contractual de renuncia a la revocación, que está causalizada, en el plano del mandato procesal nada impide el cese del Procurador inicial.

Vistos los preceptos legales y jurisprudencia citados, y lo demás de general y pertinente aplicación

PARTE DISPOSITIVA

1.- Se tiene por personado y parte a la Procuradora de los Tribunales Don/Doña [NOMBRE Y APELLIDOS], en nombre y representación de la demandante [ÓRGANO], S.L., por revocación tácita de su poder, entendiéndose las sucesivas actuaciones procesales con la misma.

2.- Se tiene por cesado en el proceso al Procurador de los Tribunales Don/Doña [NOMBRE Y APELLIDOS].

3.- Se alza la suspensión del curso del presente juicio.

Así lo acuerda y firma, el Letrado de la Administración de Justicia:

Firma del Letrado/a de la Administración de Justicia:

La presente resolución no es firme, y contra la misma cabe interponer recurso de reposición, mediante escrito ante el LAJ que se presenta dentro de los cinco días hábiles siguientes al de notificación, y en el que deberá indicarse la infracción cometida a juicio del recurrente, y sin perjuicio del cual se llevará a efecto lo acordado.

Para interponer el recurso será necesario la constitución de un depósito de 25 euros, sin cuyo requisito no será admitido a trámite. El depósito se constituirá consignando dicho importe en la Cuenta de Depósitos y Consignaciones que este Tribunal tiene abierta en el grupo [GRUPO] con el número [NÚMERO], indicando en el campo concepto del resguardo de ingreso que se trata de un "Recurso" código 00-Reposición. La consignación deberá ser acreditada al interponer el recurso (disp. adic. 15.ª de la LOPJ).

Están exentos de constituir el depósito para recurrir los incluidos en el apartado 5 de la disposición citada y quienes tengan reconocido el derecho a la asistencia jurídica gratuita.

========================================================================
