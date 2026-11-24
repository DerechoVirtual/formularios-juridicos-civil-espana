---
name: escrito-ejecutado-pide-cese-administracion-judicial-civ-1533
description: "Escrito del ejecutado que pide el cese de la administración judicial por mala gestión del ejecutante. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito del ejecutado que pide el cese de la administración judicial por mala gestión del ejecutante

> Formulario **CIV-1533** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito del ejecutado que pide el cese de la administración judicial por mala gestión del ejecutante» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito del ejecutado que pide el cese de la administración judicial por mala gestión del ejecutante” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:escrito-ejecutado-pide-cese-administracion-judicial-civ-1533`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] SEDE (3 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] AÑO
- [ ] FECHA
- [ ] LUGAR Y FECHA
- [ ] Nº
- [ ] Nº DE COLEGIADO
- [ ] Nº DE PROCEDIMIENTO

## Normas que cita el formulario

- art. 679 LEC
- art. 677 LEC
- art. 394 LEC

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

### Avisos de actualización (2) — se aplican en el texto, nunca se copian en el documento

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º LOS DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…LIDAD] ante la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. «De los de» es residuo de los varios juzgados de una plaza. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º LOS DE [SEDE]

Don [NOMBRE Y APELLIDOS], Procurador de los Tribunales y Don [NOMBRE Y APELLIDOS] y de [LOCALIDAD], según tengo debidamente acreditado en el procedimiento de ejecución dineraria núm. [Nº DE PROCEDIMIENTO] del año [AÑO], seguido contra Don [NOMBRE Y APELLIDOS], y bajo la dirección Letrada de Don [NOMBRE Y APELLIDOS], colegiado núm. [Nº DE COLEGIADO] del Ilustre Colegio Abogados de [LOCALIDAD] ante la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº] comparezco y, como mejor proceda en Derecho, DIGO:

Que habiendo sido conferida en su día al ejecutante y de conformidad con el artículo 676, de la Ley de Enjuiciamiento civil la administración de la finca embargada en los presentes Autos propiedad de mi representado interesa a mi mandante, de conformidad con el artículo 680 de la Ley de Enjuiciamiento Civil se proceda al ALZAMIENTO DE LA ADMINISTRACIÓN POR DEFECTUOSA ADMINISTRACIÓN DEL EJECUTANTE, lo que fundo en los siguientes

HECHOS

El pasado día [FECHA] se dictó decreto por el Letrado de la Administración de Justicia de ese órgano por el que se entregaba al ejecutante en administración para pago la finca propiedad de mi representado embargada en los presentes autos cuya descripción es la siguiente

El ejecutante, desde el inicio de la entrega de la finca, ha venido incumpliendo de forma manifiesta sus obligaciones, ejercitando de forma torticera la función de administración, sin que haya aplicado ninguna cantidad para el pago del principal, intereses y costas de la ejecución.

Así, por una parte, pese al tiempo transcurrido desde que se constituyó la administración, el ejecutante no ha rendido cuentas en ningún momento, pese a haber sido requerido por el Letrado de la Administración de Justicia a instancias de esta parte.

Por otra parte, ninguna cantidad se ha aplicado al pago de la deuda que justificó la adopción de la medida, por lo que es obvio que mantener esta medida no tiene ningún sentido por no cumplir la finalidad para la que fue constituida.

Si bien es cierto que la LEC sólo hace mención de las sanciones que pueden imponerse al ejecutado y a los terceros que obstaculicen el ejercicio de la administración, es evidente que el tribunal competente también puede acordar la extinción de la administración si comprueba que el administrador incumple gravemente las obligaciones de su cargo, entre las que tiene un valor primordial la rendición de cuentas, dado que nos indica la evolución del importe de la deuda durante la administración, lo cual ha sido incumplido reiteradamente por el ejecutante pese a los requerimientos formulados. En este caso, debemos subrayar que no estamos ante una discrepancia sobre la rendición de cuentas, sino ante un incumplimiento grave y reiterado de sus obligaciones por parte del ejecutante-administrador. Asimismo, y dado el carácter antieconómico de la medida, debe acordarse la finalización de la administración cuando, como en este caso, compruebe que no existe posibilidad de liquidar la deuda por esa vía, a la vista del rendimiento económico del bien o bienes administrados.

A los anteriores hechos son de aplicación los siguientes,

FUNDAMENTOS DE DERECHO

LEGITIMACIÓN, COMPETENCIA Y PROCEDIMIENTO. El art. 679 de la LEC establece que todas las cuestiones que puedan surgir entre acreedor y ejecutado con motivo de la administración de las fincas embargadas se sustanciarán ante el tribunal que autorizó la ejecución por los trámites del juicio verbal.

FUNDAMENTOS SUSTANTIVOS. El artículo 677 de la LEC, en cuanto a la diligencia que debe emplearse en la administración, el 678 de la LEC en cuanto a la obligación de rendir cuentas.

COSTAS. Deben imponerse al ejecutante si se opone a la pretensión sostenida por esta parte, conforme al art. 394 de la LEC.

Por lo que,

AL TRIBUNAL SUPLICO que, tenga por presentado este escrito, con justificante de traslado, y en sus méritos tenga por planteada la controversia sobre alzamiento de la administración del bien embargado y, previos los trámites legales, acuerde dar por finalizada la administración, reponiendo a mi mandante en la posesión del mismo, con los demás pronunciamientos inherentes, con imposición de las costas de este incidente a la parte actora.

Es justicia que pido en [LUGAR Y FECHA]

========================================================================
