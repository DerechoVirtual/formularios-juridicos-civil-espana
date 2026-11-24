---
name: solicitud-embargo-gananciales-contra-conyuge-deuda-civ-1676
description: "Solicitud de embargo de gananciales contra un cónyuge por deuda privativa anterior al matrimonio. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud de embargo de gananciales contra un cónyuge por deuda privativa anterior al matrimonio

> Formulario **CIV-1676** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Escrito del ejecutante, en una ejecución de título extrajudicial (p. ej., póliza de préstamo) dirigida sólo contra uno de los cónyuges por una deuda privativa (anterior al matrimonio), en el que, no habiendo bienes privativos suficientes, se solicita el embargo de bienes gananciales titularidad del otro cónyuge, que responden subsidiariamente, con notificación al cónyuge titular y anotación preventiva en el Registro de la Propiedad.

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud de embargo de gananciales contra un cónyuge por deuda privativa anterior al matrimonio» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud de embargo de gananciales contra un cónyuge por deuda privativa anterior al matrimonio” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:solicitud-embargo-gananciales-contra-conyuge-deuda-civ-1676`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (10 veces)
- [ ] FOLIO (4 veces)
- [ ] LIBRO (4 veces)
- [ ] Nº (4 veces)
- [ ] Nº DE FINCA (4 veces)
- [ ] TOMO (4 veces)
- [ ] NOMBRE Y APELLIDOS DEL CÓNYUGE (3 veces)
- [ ] AÑO (2 veces)
- [ ] DÍA (2 veces)
- [ ] FIRMA (2 veces)
- [ ] MES (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL EJECUTADO (2 veces)
- [ ] DENOMINACIÓN SOCIAL DEL EJECUTANTE
- [ ] DESCRIPCIÓN DE LOS BIENES
- [ ] FECHA
- [ ] LAS FINCAS O LA FINCA
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] Nº DE PROCEDIMIENTO
- [ ] SEDE

## Normas que cita el formulario

- art. 593.3 LEC
- art. 590 LEC
- art. 1347.3.º CC
- art. 1356 CC
- art. 541.3 LEC
- art. 1373 CC
- art. 629.1 LEC
- art. 549.1.3.º LEC

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…día por los medios electrónicos o telemáticos que correspondan (art. 629.1 LEC).»: el original preveía la remisión «por fax»; comprobar en el texto vigente del art. 629.1 LEC el medio de remisión del mandamiento.

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, que actúa en nombre y representación de [DENOMINACIÓN SOCIAL DEL EJECUTANTE], como tengo debidamente acreditado en autos de Ejecución de Título Extrajudicial n.º [Nº DE PROCEDIMIENTO], en los mismos comparezco y, como mejor en Derecho proceda, DIGO:

PRIMERO.– La ejecución despachada a instancia de esta parte frente a D./Dña. [NOMBRE Y APELLIDOS DEL EJECUTADO] se funda en póliza de préstamo para la adquisición de un vehículo de motor, en la que figura como deudor, de fecha [DÍA] de [MES] de [AÑO].

SEGUNDO.– Habiéndose intentado el embargo del vehículo de motor financiado, resulta que su titularidad ha sido transmitida a tercero, conforme deniega el Registro de Bienes Muebles la anotación preventiva, por lo que se ha alzado el embargo conforme al art. 593.3 LEC.

Se acompaña la denegación del asiento registral como documento n.º [Nº], remitiéndonos a la providencia en autos de fecha [FECHA].

TERCERO.– El ejecutado contrajo matrimonio con D./Dña. [NOMBRE Y APELLIDOS DEL CÓNYUGE] poco después de suscribir la póliza de préstamo, no constando que los cónyuges hayan disuelto el régimen económico matrimonial supletorio legal de gananciales mediante capitulaciones.

Se acompaña certificación del Encargado del Registro Civil de [LOCALIDAD] como documento n.º [Nº].

CUARTO.– El ejecutado no consta que sea titular de bienes privativos de ningún tipo, habiendo resultado negativas las averiguaciones practicadas de conformidad con el art. 590 LEC.

QUINTO.– D./Dña. [NOMBRE Y APELLIDOS DEL CÓNYUGE] consta como propietario/a de [DESCRIPCIÓN DE LOS BIENES], que aparecen como fincas n.º [Nº DE FINCA], al folio [FOLIO], tomo [TOMO], libro [LIBRO] de [LOCALIDAD], y n.º [Nº DE FINCA], al folio [FOLIO], tomo [TOMO], libro [LIBRO] de [LOCALIDAD], del Registro de la Propiedad de [LOCALIDAD], habiéndolas adquirido estando casado/a, por lo que son bienes gananciales conforme a los arts. 1347.3.º y 1361 CC, incluso si se estuviere pagando el precio aplazado (art. 1356 CC), por lo que se solicita su embargo para hacer frente a la deuda por la que se sigue la ejecución, subsidiaria o indirectamente, a falta de bienes privativos del deudor, para hacer frente a una deuda antematrimonial.

Se acompañan notas simples del Registro de la Propiedad de [LOCALIDAD] como documentos n.º [Nº] y [Nº].

SEXTO.– De conformidad con el art. 541.3 LEC, puesto que se sigue ejecución por deuda privativa de un cónyuge y no hay bienes privativos del deudor, el embargo de bienes gananciales habrá de notificarse al otro cónyuge, a fin de que tenga la oportunidad de pedir la disolución de la sociedad conyugal, según previenen los arts. 1373 y 1374 CC.

SÉPTIMO.– Corresponde, como medida de garantía del embargo de inmuebles, la expedición de sendos mandamientos de anotación preventiva al Registro de la Propiedad de [LOCALIDAD], que habrán de remitirse el mismo día por los medios electrónicos o telemáticos que correspondan (art. 629.1 LEC).

En su virtud,

SUPLICO AL TRIBUNAL

que, por presentado el presente escrito con sus copias y documentos acompañados, se sirva admitir uno y otros y, por causadas las manifestaciones precedentes a sus oportunos efectos, declare, mediante decreto del Letrado de la Administración de Justicia, el embargo de [LAS FINCAS O LA FINCA] n.º [Nº DE FINCA], al folio [FOLIO], tomo [TOMO], libro [LIBRO] de [LOCALIDAD], y n.º [Nº DE FINCA], al folio [FOLIO], tomo [TOMO], libro [LIBRO] de [LOCALIDAD], del Registro de la Propiedad de [LOCALIDAD], para responder de la cantidad por la que se ha despachado la ejecución, como bienes gananciales que responden subsidiariamente del crédito contra el consorcio conyugal con el ejecutado D./Dña. [NOMBRE Y APELLIDOS DEL EJECUTADO], notificando el embargo a la titular D./Dña. [NOMBRE Y APELLIDOS DEL CÓNYUGE], y acordándose librar los oportunos mandamientos de anotación preventiva, que serán remitidos en el día y entregados a esta mandataria procesal para su diligenciamiento.

Por ser de Justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Abogado/a: [FIRMA] Firma del Procurador/a: [FIRMA]

NOTA ACLARATORIA: El modelo se corresponde con peticiones de embargo posteriores a la demanda ejecutiva, si bien lo común puede ser que se formulen en ésta, con arreglo al art. 549.1.3.º LEC. De todas formas, en el supuesto de casado que figura solo como legitimado pasivo de la ejecución, las mismas menciones serían las procedentes, es decir: determinar la existencia de sociedad de gananciales al momento del nacimiento de la deuda ejecutiva, el carácter ganancial del bien cuyo embargo se pide y la condición de la deuda, consorcial (responsabilidad directa del patrimonio común, por lo menos externa o provisional) o privativa (responsabilidad exclusivamente indirecta o subsidiaria del patrimonio común).
