---
name: escrito-tercero-evitar-embargo-vivienda-habitual-civ-1448
description: "Escrito de tercero para evitar el embargo de su vivienda habitual. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito de tercero para evitar el embargo de su vivienda habitual

> Formulario **CIV-1448** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Escrito con el que un tercero, al que el Letrado de la Administración de Justicia ha comunicado la inminencia del embargo de un inmueble, se opone a la traba alegando que el bien es suyo y constituye su vivienda habitual, al amparo del art. 593 LEC.

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito de tercero para evitar el embargo de su vivienda habitual» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito de tercero para evitar el embargo de su vivienda habitual” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:escrito-tercero-evitar-embargo-vivienda-habitual-civ-1448`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] AÑO (3 veces)
- [ ] DÍA (3 veces)
- [ ] MES (3 veces)
- [ ] Nº DE PROCEDIMIENTO (3 veces)
- [ ] IDENTIFICACIÓN DEL BIEN (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL EJECUTADO (2 veces)
- [ ] COLEGIO DE ABOGADOS
- [ ] DNI/NIE
- [ ] DOMICILIO
- [ ] LOCALIDAD
- [ ] NOMBRE Y APELLIDOS DEL EJECUTANTE
- [ ] NOMBRE Y APELLIDOS DEL LETRADO
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] NOMBRE Y APELLIDOS DEL TERCERO
- [ ] Nº
- [ ] PROFESIÓN
- [ ] SEDE

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

### Avisos de actualización (1) — se aplican en el texto, nunca se copian en el documento

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

D./Dª [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, en nombre y representación de D./Dª [NOMBRE Y APELLIDOS DEL TERCERO], mayor de edad, de profesión [PROFESIÓN], con domicilio en [DOMICILIO], y DNI/NIE [DNI/NIE], cuya representación acreditaré mediante comparecencia apud acta cuando sea requerido para ello [ELEGIR: (sin más) / "representación que acredito mediante copia de poder especial para pleitos que ruego me sea devuelta una vez testimoniada en autos por necesitarla para otros usos"], comparezco en los autos de procedimiento de ejecución número [Nº DE PROCEDIMIENTO], seguidos en este Tribunal a instancia de D./Dª [NOMBRE Y APELLIDOS DEL EJECUTANTE], en calidad de parte ejecutante, contra D./Dª [NOMBRE Y APELLIDOS DEL EJECUTADO], en calidad de parte ejecutada, con la asistencia del Letrado D./Dª [NOMBRE Y APELLIDOS DEL LETRADO], del Ilustre Colegio de Abogados de [COLEGIO DE ABOGADOS], y DIGO:

Que por medio del presente escrito y en la representación que ostento, formulo ESCRITO DE OPOSICIÓN A QUE SE TRABE EMBARGO del siguiente inmueble: [IDENTIFICACIÓN DEL BIEN: descripción y, en su caso, datos registrales], en el procedimiento de ejecución antes citado, con base en los siguientes

HECHOS

PRIMERO.- Ante este Tribunal se siguen autos de procedimiento de ejecución núm. [Nº DE PROCEDIMIENTO] contra D./Dª [NOMBRE Y APELLIDOS DEL EJECUTADO].

SEGUNDO.- Mediante diligencia de ordenación de fecha [DÍA] de [MES] de [AÑO], el Letrado de la Administración de Justicia, en aplicación de lo dispuesto en el art. 593.2 de la Ley de Enjuiciamiento Civil, ordenó que se hiciera saber a mi representado/a la inminencia de la traba, en el referido procedimiento, del siguiente inmueble: [IDENTIFICACIÓN DEL BIEN], por tener motivos fundados para sospechar que podría pertenecerle a él/ella y no al ejecutado, como en efecto así es.

TERCERO.- Aunque mi representado/a no ha procedido a solicitar la inscripción de su titularidad sobre el referido bien en el Registro de la Propiedad, puede acreditar su propiedad mediante documento privado de compraventa de fecha [DÍA] de [MES] de [AÑO], copia compulsada del cual se acompaña como DOCUMENTO Nº 1. Puede, asimismo, acreditar que el citado bien constituye su vivienda habitual, según resulta del certificado de empadronamiento que igualmente se acompaña como DOCUMENTO Nº 2.

CUARTO.- Por ello, dentro del plazo concedido en la diligencia de ordenación antes citada, solicitamos que no se trabe el embargo del bien de referencia.

Resultan aplicables a los anteriores hechos los siguientes

FUNDAMENTOS DE DERECHO

ÚNICO.- El art. 593 de la Ley de Enjuiciamiento Civil, que dispone:

"Pertenencia al ejecutado. Prohibición de alzamiento de oficio del embargo.

1. Para juzgar sobre la pertenencia al ejecutado de los bienes que se proponga embargar, el Letrado de la Administración de Justicia, sin necesidad de investigaciones ni otras actuaciones, se basará en indicios y signos externos de los que razonablemente pueda deducir aquélla.

2. Cuando por percepción directa o por manifestaciones del ejecutado o de otras personas, el Letrado de la Administración de Justicia tuviera motivos racionales para entender que los bienes que se propone trabar pueden pertenecer a un tercero, ordenará mediante diligencia de ordenación que se le haga saber la inminencia de la traba. Si, en el plazo de cinco días, el tercero no compareciere o no diere razones, el Letrado de la Administración de Justicia dictará decreto mandando trabar los bienes, a no ser que las partes, dentro del mismo plazo concedido al tercero, hayan manifestado su conformidad en que no se realice el embargo. Si el tercero se opusiere razonadamente al embargo aportando, en su caso, los documentos que justifiquen su derecho, el Letrado de la Administración de Justicia, previo traslado a las partes por plazo común de cinco días, remitirá los autos al Tribunal para que resuelva lo que proceda.

3. Tratándose de bienes cuyo dominio sea susceptible de inscripción registral, se ordenará, en todo caso, su embargo a no ser que el tercero acredite ser titular registral mediante la correspondiente certificación del Registrador, quedando a salvo el derecho de los eventuales titulares no inscritos, que podrá ejercitarse contra quien y como corresponda.

No obstante lo dispuesto en el párrafo anterior, cuando el bien de cuyo embargo se trate sea la vivienda familiar del tercero y éste presentare al Tribunal el documento privado que justifique su adquisición, el Letrado de la Administración de Justicia dará traslado a las partes y, si éstas, en el plazo de cinco días, manifestaren su conformidad en que no se realice el embargo, el Letrado de la Administración de Justicia se abstendrá de acordarlo."

Por lo expuesto,

SUPLICO AL TRIBUNAL: Que, teniendo por presentado este escrito con los documentos que lo acompañan y copia de todo ello, lo admita y dé traslado a las partes en el procedimiento de ejecución núm. [Nº DE PROCEDIMIENTO] que se sigue ante este Tribunal, emplazándolas el Letrado de la Administración de Justicia para que, en un plazo de cinco días, manifiesten si están conformes con que no se trabe el embargo del bien [IDENTIFICACIÓN DEL BIEN], por corresponder su propiedad al abajo firmante y, además, constituir su vivienda habitual, absteniéndose de acordar el embargo si, en el citado plazo, manifiestan su conformidad a ello; y de no ser manifestada tal conformidad, remita el Letrado de la Administración de Justicia los autos al Tribunal para que resuelva lo que proceda.

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma y número de colegiado del Letrado Firma del Procurador
