---
name: auto-declara-privativa-deuda-da-conyuge-no-deudor-civ-2127
description: "Auto que declara privativa la deuda y da al cónyuge no deudor la opción de disolver los gananciales. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Auto que declara privativa la deuda y da al cónyuge no deudor la opción de disolver los gananciales

> Formulario **CIV-2127** del plugin **Resoluciones judiciales civiles: autos, decretos y diligencias** (`formularios-resoluciones-judiciales-civiles`) · Civil › Resoluciones judiciales (autos, decretos, providencias, diligencias) · normativa revisada el 24-11-2026.

## Qué es

Auto que declara que de la deuda ejecutiva no responden los bienes gananciales del matrimonio del ejecutado por ser una deuda privativa de éste, y concede al cónyuge no deudor la opción de pedir la disolución de la sociedad de gananciales o consentir que continúe el embargo sobre los bienes comunes (arts. 541 y 561 LEC; arts. 1.365, 1.366 y 1.373 CC).

Es un modelo de tipo **resoluciones judiciales (autos, decretos, providencias, diligencias)**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Auto que declara privativa la deuda y da al cónyuge no deudor la opción de disolver los gananciales» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Auto que declara privativa la deuda y da al cónyuge no deudor la opción de disolver los gananciales” para mi caso». También puedes invocarla directamente con `/formularios-resoluciones-judiciales-civiles:auto-declara-privativa-deuda-da-conyuge-no-deudor-civ-2127`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-resoluciones-judiciales-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Resoluciones judiciales civiles: autos, decretos y diligencias) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS DEL EJECUTADO (6 veces)
- [ ] NOMBRE Y APELLIDOS DEL CÓNYUGE (4 veces)
- [ ] AÑO (3 veces)
- [ ] DENOMINACIÓN SOCIAL DEL EJECUTANTE (3 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] ACTIVIDAD PROFESIONAL (2 veces)
- [ ] DÍA (2 veces)
- [ ] FECHA (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] MES (2 veces)
- [ ] NIG
- [ ] Nº DE CUENTA
- [ ] Nº DE GRUPO
- [ ] Nº DE PROCEDIMIENTO
- [ ] PARTES
- [ ] PROFESIÓN
- [ ] SEDE

## Normas que cita el formulario

- art. 1.365.2.º Código Civil
- art. 1.366 Código Civil
- art. 1.401 Código Civil
- art. 1.544 Código Civil
- art. 561.3 LEC
- art. 697 LEC

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

- Al principio del formulario: el modelo parte de un supuesto de responsabilidad civil derivada de delito cometido por un profesional sanitario en el ejercicio de su profesión; los razonamientos jurídicos del primer y segundo fundamentos deben adaptarse al título y a la naturaleza de la deuda del caso concreto.

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

Procedimiento: Ejecución de Título Judicial n.º [Nº DE PROCEDIMIENTO] / [AÑO]

Número de Identificación Informática: [NIG]

Partes: [PARTES]

AUTO

Ilmo./a. Sr./a. Magistrado/a D./Dña. [NOMBRE Y APELLIDOS]

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

ANTECEDENTES DE HECHO

PRIMERO.- Habiéndose embargado, a instancias de la ejecutante, [DENOMINACIÓN SOCIAL DEL EJECUTANTE], representada por el/la Procurador/a Sr./a [NOMBRE Y APELLIDOS], sueldos del cónyuge del ejecutado D. [NOMBRE Y APELLIDOS DEL EJECUTADO], los cuales son bienes gananciales, se acordó por decreto de fecha [FECHA], notificándoselo a dicho cónyuge, junto con la demanda ejecutiva y el auto que despachó la ejecución.

SEGUNDO.- En tiempo y forma se personó en los autos dicho cónyuge, Dña. [NOMBRE Y APELLIDOS DEL CÓNYUGE], representada por el/la Procurador/a Sr./a [NOMBRE Y APELLIDOS], deduciendo oposición por no responder los bienes gananciales de la deuda ejecutiva.

TERCERO.- Se confirió traslado del escrito de oposición conforme al art. 560, párrafo 1.º LEC, produciendo escrito de alegaciones la parte ejecutante, la cual solicitó vista, que tuvo lugar el [DÍA] de [MES] de [AÑO], con asistencia de ejecutante y cónyuge del ejecutado, y cuyo tenor consta grabado en soporte técnico audiovisual.

FUNDAMENTOS DE DERECHO

PRIMERO.- En este asunto estamos en presencia de una obligación civil de resarcimiento cuyo título es la comisión de un delito en el ejercicio de [ACTIVIDAD PROFESIONAL] por D. [NOMBRE Y APELLIDOS DEL EJECUTADO], [PROFESIÓN].

Ciertamente, D. [NOMBRE Y APELLIDOS DEL EJECUTADO] no cometió el delito con la intención de obtener un beneficio patrimonial directo, como sucede con delitos como el hurto, la estafa, la apropiación indebida, etc.; es decir, el resultado dañoso por sí mismo no proporciona un beneficio necesario e inmediato a su patrimonio privativo o ganancial, sino que más bien el daño tuvo lugar "con ocasión" de una actividad, [ACTIVIDAD PROFESIONAL], desarrollada en beneficio personal y de su sociedad de gananciales.

Pudiera pensarse, por tanto, que nos encontramos ante el supuesto del artículo 1.365.2.º del Código Civil, que responsabiliza directamente a los bienes gananciales de las deudas contraídas por un cónyuge en el ejercicio ordinario de la profesión, pero, si bien [EJEMPLO: la atención a un paciente es ejercicio ordinario de la profesión médica], no es menos cierto que un acto (omisión en este caso) apto para ocasionar responsabilidad penal y civil difícilmente podría reputarse como ejercicio ordinario de la profesión, además de que la expresión "deudas contraídas" está pensada para el ámbito negocial, esto es, para los actos de administración y disposición encaminados directamente a procurar el lícito y ordenado desarrollo de la profesión.

La referencia a la actividad comercial, en el párrafo último del precepto, que remite al Código de Comercio, abona esta interpretación.

SEGUNDO.- Por tanto, el supuesto no encaja en el artículo 1.365.2.º del Código Civil, y por ser una obligación no negocial debemos examinar si es de aplicación el artículo 1.366 del Código Civil, con arreglo al cual "las obligaciones extracontractuales de un cónyuge, consecuencia de su actuación en beneficio de la sociedad conyugal o en el ámbito de la administración de los bienes serán de la responsabilidad y cargo de aquélla, salvo si fuesen debidas a dolo o culpa grave del cónyuge deudor".

El título de la reclamación de la parte ejecutante es la responsabilidad civil derivada de la comisión de un delito, lo que constituye responsabilidad extracontractual en sentido amplio, que entendemos comprendida en el art. 1.366 del Código Civil. El precepto distingue la responsabilidad civil derivada de la actuación en beneficio de la sociedad conyugal y la que no lo es, y diferencia también, dentro de la primera, la que es debida a dolo o culpa grave del deudor y la que no lo es.

Como nos encontramos en el supuesto del beneficio de la sociedad de gananciales, según se ha indicado, la responsabilidad del patrimonio común dependerá del grado de culpa del deudor, y como se ha señalado que el caso, desde una perspectiva puramente civil, es también de culpa grave, la deuda indemnizatoria será privativa del deudor D. [NOMBRE Y APELLIDOS DEL EJECUTADO], el cual responderá con sus bienes privativos y con los gananciales adjudicados en la liquidación.

Cierto es que la sociedad de gananciales puede haberse enriquecido con la actuación profesional del esposo, pero la sentencia penal (que, no lo olvidemos, es el título del que deriva este procedimiento) nada dice al respecto, porque el modo concreto de cómo debe de pagar el deudor es una cuestión puramente civil y, además, el art. 1.366 del Código Civil es claro al respecto para el caso de dolo o culpa grave.

Por tanto, el artículo 1.401 del Código Civil no es de aplicación, ya que la deuda de D. [NOMBRE Y APELLIDOS DEL EJECUTADO] es privativa del mismo y no pertenece al pasivo de la sociedad de gananciales; como tampoco es de aplicación el art. 1.544 del Código Civil, ya que el título de la condena al pago de la responsabilidad civil no es el incumplimiento de un contrato sino la condena penal derivada de un ilícito sancionado extracontractualmente, por lo que la pretensión de Dña. [NOMBRE Y APELLIDOS DEL CÓNYUGE] ha de ser estimada.

TERCERO.- Compete imponer las costas procesales a la parte ejecutante, con arreglo al art. 561.3 in fine LEC.

Vistas las normas citadas y demás de aplicación,

PARTE DISPOSITIVA

1.- Se declara que de la deuda ejecutiva en el proceso de ejecución promovido por [DENOMINACIÓN SOCIAL DEL EJECUTANTE] frente a D. [NOMBRE Y APELLIDOS DEL EJECUTADO] no responden los bienes gananciales del matrimonio del ejecutado y Dña. [NOMBRE Y APELLIDOS DEL CÓNYUGE].

2.- Notifíquese a Dña. [NOMBRE Y APELLIDOS DEL CÓNYUGE], con advertencia de que dispone del plazo de quince días [OPCIONAL — si ha lugar] (o el que se arbitre) para manifestar ante este Tribunal si desea que se proceda a la disolución de la sociedad de gananciales, en cuyo caso el embargo se concretará en la cuota que correspondiera a su esposo en los bienes comunes, o bien consiente que continúe el embargo y apremio sobre los bienes gananciales que se han embargado y embarguen, entendiéndose que, si no hace manifestación alguna en el referido plazo, se considerará que consiente el embargo de bienes comunes.

3.- Se condena en las costas del incidente a la parte promotora de la ejecución, [DENOMINACIÓN SOCIAL DEL EJECUTANTE].

Contra la presente resolución cabe recurso de apelación, que se interpondrá ante el mismo órgano en el plazo de los veinte días siguientes al de notificación, exponiendo el apelante las alegaciones en que se base la impugnación, además de citar la resolución apelada y los pronunciamientos que impugna, pudiendo la parte ejecutante pedir el mantenimiento del embargo y sus medidas de garantía, y que se adopten las que procedan conforme al art. 697 LEC, siempre que preste caución suficiente para asegurar la indemnización que pueda corresponder al tercero opuesto en la ejecución en caso de que se confirme la presente resolución.

Para interponer el recurso será necesaria la constitución de un depósito de 50 euros, sin cuyo requisito no será admitido a trámite. El depósito se constituirá consignando dicho importe en la Cuenta de Depósitos y Consignaciones que este Tribunal tiene abierta en el grupo [Nº DE GRUPO] con el número [Nº DE CUENTA], indicando en el campo concepto del resguardo de ingreso que se trata de un "Recurso" código 02-Apelación. La consignación deberá ser acreditada al interponer el recurso (disp. adic. 15.ª de la LOPJ).

No están obligados a constituir el depósito para recurrir los declarados exentos en la disposición citada y quienes tengan reconocido el derecho a la asistencia jurídica gratuita.

Así lo acuerdo, mando y firmo:

Por ser de justicia, lo pido en [LOCALIDAD], a [FECHA].

Firma del/de la Magistrado/a:
