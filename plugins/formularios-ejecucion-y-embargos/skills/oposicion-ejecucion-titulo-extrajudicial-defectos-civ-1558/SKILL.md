---
name: oposicion-ejecucion-titulo-extrajudicial-defectos-civ-1558
description: "Oposición a la ejecución de título extrajudicial por defectos procesales (nulidad del despacho). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Oposición a la ejecución de título extrajudicial por defectos procesales (nulidad del despacho)

> Formulario **CIV-1558** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Oposición a la ejecución de título extrajudicial por defectos procesales (nulidad del despacho)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Oposición a la ejecución de título extrajudicial por defectos procesales (nulidad del despacho)” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:oposicion-ejecucion-titulo-extrajudicial-defectos-civ-1558`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] SEDE (3 veces)
- [ ] Nº DE PROCEDIMIENTO (2 veces)
- [ ] FECHA
- [ ] LOCALIDAD
- [ ] NOMBRE DE LA PARTE
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] Nº
- [ ] NÚMERO

## Normas que cita el formulario

- art. 559.1.3 LEC
- art. 572 LEC
- art. 557.2 LEC
- art. 517 LEC

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

- Junto a «…IA [SEDE] A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

PROCEDIMIENTOS DE EJECUCIÓN Nº [Nº DE PROCEDIMIENTO]

TRIBUNAL DE INSTANCIA [SEDE]

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

D. [NOMBRE Y APELLIDOS] Procurador de los Tribunales, en nombre y representación de [NOMBRE DEL REPRESENTADO/A], tutor de D. [NOMBRE Y APELLIDOS], parte ejecutada en el procedimiento de ejecución arriba referenciado, según acredito mediante apoderamiento apud acta otorgado ante el Letrado de la Administración de Justicia de [LOCALIDAD], ante el Tribunal comparezco y como mejor proceda en Derecho DIGO:

Que dentro del plazo de diez días señalado por la Ley paso a formular OPOSICIÓN A LA EJECUCIÓN instada basada en defectos procesales, al amparo del art. 559.1.3º de la LEC por nulidad radical del despacho de ejecución, ello en base a los siguientes:

HECHOS

PRIMERO.- La Póliza de arrendamiento financiero destinada a la compra de vehículo a motor (leasing) que pretende ejecutarse fue intervenida por el Notario D. [NOMBRE Y APELLIDOS], según se hace constar en la demanda ejecutiva.

No obstante, tal contrato está viciado de nulidad por cuanto mi representado ha sido declarado discapacitado en fecha [FECHA], en el expediente de provisión de medidas judiciales de apoyo a personas con discapacidad [Nº DE PROCEDIMIENTO] seguido por la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [NÚMERO], aportándose testimonio de Auto firme expedido por dicho Tribunal, como DOCUMENTO NÚM. 1.

SEGUNDO.- El artículo 572 LEC, así como el 573.1.3º LEC establecen que la entidad acreedora deberá notificar previamente al deudor o fiador la cantidad exigible resultante de la liquidación y, de no practicarse ésta, el documento carece de fuerza ejecutiva, siendo de aplicación la causa de oposición establecida en el artículo 559.1.3º LEC.

Teniendo en cuenta que de la póliza de arrendamiento financiero destinada a la compra de vehículo a motor (leasing) sólo se ha notificado el saldo deudor a mi principal, sin que se haya procedido a la notificación al resto de los deudores solidarios, coloca a esta parte en una situación de absoluta indefensión que genera una nulidad radical del título por defecto extrínseco al no haberse realizado la comunicación del saldo deudor a la totalidad de deudores solidarios.

A los anteriores hechos le son aplicables los siguientes

1. PROCEDIMIENTO.

Artículos 556, 557 y 559 de la LEC, debiendo suspenderse el curso de la ejecución conforme dispone el art. 557.2 de la LEC.

2. LEGITIMACIÓN

Artículo 556.1 LEC, al ser parte ejecutada en el presente proceso de ejecución.

3. OPOSICIÓN A LA EJECUCIÓN.

A. Arts. 559.1.2º respecto de la nulidad del despacho de ejecución por falta de capacidad del ejecutado y 1261 y ss. CC en el sentido de ser nulo el contrato suscrito por falta de capacidad del ejecutado.

Artículo 559.3º, redactado por Ley 42/2015, respecto de la nulidad radical del despacho de la ejecución por no cumplir el documento presentado los requisitos legales exigidos para llevar aparejada ejecución, establecidos en los arts. 517, 571, 572 y 573 LEC

4. COSTAS

Han de imponerse al ejecutante de conformidad con los artículos 539.2 y 559.2.2 LEC.

En su virtud,

SUPLICO AL TRIBUNAL: Tenga por presentado este escrito, documentos y copias, se sirva admitirlos y unirlos a autos, teniendo por formalizada, en tiempo y forma, oposición a la demanda ejecutiva instada por [NOMBRE DE LA PARTE] contra mi mandante, y previa sustanciación, con suspensión de la ejecución, estime la oposición deducida y proceda a dictar auto dejando sin efecto la ejecución despachada, condenando en costas al ejecutante.

Lugar y fecha.

Abogado y Procurador.

========================================================================
