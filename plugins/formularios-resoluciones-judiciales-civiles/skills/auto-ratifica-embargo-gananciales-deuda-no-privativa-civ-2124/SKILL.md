---
name: auto-ratifica-embargo-gananciales-deuda-no-privativa-civ-2124
description: "Auto que ratifica el embargo de gananciales por deuda no privativa derivada de accidente de tráfico. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Auto que ratifica el embargo de gananciales por deuda no privativa derivada de accidente de tráfico

> Formulario **CIV-2124** del plugin **Resoluciones judiciales civiles: autos, decretos y diligencias** (`formularios-resoluciones-judiciales-civiles`) · Civil › Resoluciones judiciales (autos, decretos, providencias, diligencias) · normativa revisada el 24-11-2026.

## Qué es

Auto declarando que la deuda ejecutiva en el proceso de ejecución es responsabilidad de los bienes gananciales del matrimonio del ejecutado y de su esposa, ratificando el embargo del sueldo de la esposa para responder de la satisfacción del crédito ejecutivo, procediendo continuar el apremio.

Es un modelo de tipo **resoluciones judiciales (autos, decretos, providencias, diligencias)**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Auto que ratifica el embargo de gananciales por deuda no privativa derivada de accidente de tráfico» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Auto que ratifica el embargo de gananciales por deuda no privativa derivada de accidente de tráfico” para mi caso». También puedes invocarla directamente con `/formularios-resoluciones-judiciales-civiles:auto-ratifica-embargo-gananciales-deuda-no-privativa-civ-2124`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-resoluciones-judiciales-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Resoluciones judiciales civiles: autos, decretos y diligencias) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (13 veces)
- [ ] FECHA (5 veces)
- [ ] ASEGURADORA (3 veces)
- [ ] AÑO (3 veces)
- [ ] LUGAR (2 veces)
- [ ] Nº (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] DÍA
- [ ] GRUPO
- [ ] MES
- [ ] SEDE

## Normas que cita el formulario

- art. 1.366 CC
- art. 217.7 LEC
- art. 561.1.1.ª LEC

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

- Junto a «…ió la Sección de Instrucción del Tribunal de Instancia de [SEDE], plaza n.º [Nº]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA

Procedimiento: Ejecución de Título Judicial n.º [Nº]/[AÑO]

Número de Identificación Informática:

Partes:

AUTO

Ilmo. Sr./a. Magistrado-Juez D./Dña. [NOMBRE Y APELLIDOS]

En [LUGAR], a [FECHA].

ANTECEDENTES DE HECHO

PRIMERO.- Habiéndose embargado a instancias de la ejecutante Compañía de Seguros [ASEGURADORA]., representada por la Procurador/a Sr./a. [NOMBRE Y APELLIDOS], sueldos del cónyuge del ejecutado Don [NOMBRE Y APELLIDOS], los cuales son bienes gananciales, se acordó por decreto de fecha [FECHA], notificándoselo a dicho cónyuge, junto con la demanda ejecutiva y el auto que despachó la ejecución.

SEGUNDO.- En tiempo y forma se personó en los autos dicho cónyuge, Doña [NOMBRE Y APELLIDOS], representada por el Procurador Sr [NOMBRE Y APELLIDOS], deduciendo oposición por no responder los bienes gananciales de la deuda ejecutiva.

TERCERO.- Se confirió traslado del escrito de oposición conforme al art. 560, párrafo 1.º LEC, produciendo escrito de alegaciones la parte ejecutante, la cual solicitó vista, que tuvo lugar el [DÍA] de [MES] de [AÑO], con asistencia de ejecutante y cónyuge del ejecutado, y cuyo tenor consta grabado en soporte técnico audiovisual.

FUNDAMENTOS DE DERECHO

PRIMERO.- Reclamó la Compañía de Seguros [ASEGURADORA] a su asegurado Don [NOMBRE Y APELLIDOS], por razón del reembolso de indemnización abonada a un perjudicado como consecuencia de accidente de circulación que dio lugar a Juicio de Faltas n.º [NÚMERO]/[AÑO], de que conoció la Sección de Instrucción del Tribunal de Instancia de [SEDE], plaza n.º [Nº] , con base en el clausulado de la póliza de seguros que vinculaba a las partes, y se dictó en este Tribunal sentencia de [FECHA] firme, cuya ejecución se solicitó y despachó en auto de [FECHA], y ante el embargo de bienes gananciales, se opone Doña [NOMBRE Y APELLIDOS] en escrito que se limita a negar la responsabilidad de tales por la deuda a cuyo pago se condenó a su esposo, sin discutir la vigencia de la sociedad de gananciales, y sin probar hecho especial alguno.

SEGUNDO.- Es unánime la doctrina que afirma que dentro del debatido art. 1.366 CCiv, se incluyen todas las actuaciones derivadas del tráfico de vehículos de motor, máxime después de la reforma llevada a cabo por la LO 3/1989 de 21 junio, de actualización del CP, despenalizando las conductas derivadas de dicho tráfico y encajándolas, como no podía ser menos, en los arts. 1.902 y 1.903 CC, cobijo tradicional de la responsabilidad extracontractual.

Dicha inclusión deviene obligada aunque se trate de una actividad: la de la conducción de un vehículo, de la que, normalmente y a salvo de actividades de tipo profesional, no puede predicarse que tenga como finalidad directa la obtención de un lucro patrimonial, porque el citado art. 1.366 habla no sólo de que se actúe en el ámbito de la administración de los bienes, sino que también se refiere a una actuación en beneficio de la sociedad conyugal; término este lo suficientemente amplio como para encuadrar en él actividades que no persigan necesariamente obtener rendimientos patrimoniales en sentido estricto para el consorcio.

Pero, en cualquier caso, hallándonos en materia de culpa extracontractual, el principio de facilitación de la prueba (art. 217.7 LEC) obliga al tribunal a imponer la carga de probar a los miembros del consorcio ganancial el que la actuación del cónyuge culpable excedía de tales límites, lo que ni tan siquiera se ha intentado, limitándose la cónyuge no ejecutada a negar la responsabilidad con el patrimonio común.

TERCERO.- El principio objetivista del vencimiento, que inspira el art. 561.1.1.ª ‘in fine’ LEC, fuerza la condena en costas de la parte opuesta.

Vistas las normas citadas y demás de aplicación,

PARTE DISPOSITIVA

1.- Se desestima la pretensión de Doña [NOMBRE Y APELLIDOS], representada por el procurador de los Tribunales Sr./a. [NOMBRE Y APELLIDOS], de que se declara que la deuda ejecutiva en el proceso de ejecución promovido por la Compañía de Seguros [ASEGURADORA]., frente a Don [NOMBRE Y APELLIDOS], no es responsabilidad de los bienes gananciales del matrimonio del ejecutado y Doña [NOMBRE Y APELLIDOS].

2.- Se ratifica el embargo del sueldo de Doña [NOMBRE Y APELLIDOS] para responder de la satisfacción del crédito ejecutivo, procediendo continuar el apremio.

3.- Se condena en las costas del incidente a Doña [NOMBRE Y APELLIDOS].

Contra la presente resolución cabe recurso de apelación, que se interpondrá ante el mismo órgano en el plazo de los veinte días siguientes al de notificación, exponiendo el apelante las alegaciones en que se base la impugnación, además de citar la resolución apelada y los pronunciamientos que impugna, sin que tenga la interposición del recurso efecto de suspender la ejecución.

Para interponer el recurso será necesario la constitución de un depósito de 50 euros, sin cuyo requisito no será admitido a trámite. El depósito se constituirá consignando dicho importe en la Cuenta de Depósitos y Consignaciones que este Tribunal tiene abierta en el grupo [GRUPO] con el número [NÚMERO], indicando en el campo concepto del resguardo de ingreso que se trata de un "Recurso" código 02-Apelación. La consignación deberá ser acreditada al interponer el recurso (disp. adic. 15.ª de la LOPJ).

No están obligados a constituir el depósito para recurrir los declarados exentos en la disposición citada y quienes tengan reconocido el derecho a la asistencia jurídica gratuita.

Así lo acuerdo, mando y firmo:

Por ser de Justicia que pido en [LUGAR], a [FECHA].

Firma del/de la Letrado/a de la Administración de Justicia:

========================================================================
