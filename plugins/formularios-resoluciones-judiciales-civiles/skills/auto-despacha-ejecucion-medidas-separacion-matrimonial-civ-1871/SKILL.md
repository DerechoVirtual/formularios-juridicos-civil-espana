---
name: auto-despacha-ejecucion-medidas-separacion-matrimonial-civ-1871
description: "Auto que despacha ejecución de las medidas de separación matrimonial. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Auto que despacha ejecución de las medidas de separación matrimonial

> Formulario **CIV-1871** del plugin **Resoluciones judiciales civiles: autos, decretos y diligencias** (`formularios-resoluciones-judiciales-civiles`) · Civil › Resoluciones judiciales (autos, decretos, providencias, diligencias) · normativa revisada el 24-11-2026.

## Qué es

Auto despachando ejecución de medidas de separación matrimonial, advirtiendo al ejecutado que la ejecución despachada se entenderá ampliada automáticamente si en las fechas de vencimiento, no se hubieren consignado, a disposición del Tribunal en la Cuenta de Depósitos y Consignaciones, las cantidades correspondientes a las pensiones alimenticias pendientes de vencimiento.

Es un modelo de tipo **resoluciones judiciales (autos, decretos, providencias, diligencias)**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Auto que despacha ejecución de las medidas de separación matrimonial» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Auto que despacha ejecución de las medidas de separación matrimonial” para mi caso». También puedes invocarla directamente con `/formularios-resoluciones-judiciales-civiles:auto-despacha-ejecucion-medidas-separacion-matrimonial-civ-1871`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-resoluciones-judiciales-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Resoluciones judiciales civiles: autos, decretos y diligencias) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] AÑO (6 veces)
- [ ] IMPORTE (5 veces)
- [ ] FECHA (3 veces)
- [ ] MES (3 veces)
- [ ] LUGAR (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] DÍA
- [ ] Nº

## Normas que cita el formulario

- art. 517.2 LEC
- art. 776 LEC
- art. 549.2 LEC
- art. 551 LEC
- art. 546 LEC
- art. 578.2 LEC
- art. 155.3 LEC
- art. 551.4 LEC

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

Notas al pie del formulario original:
(1) En la práctica no parece que se esté empleando el art. 578 LEC para la ejecución de las medidas, provisionales o definitivas, por pensiones alimenticias o compensatorias de los procesos especiales matrimoniales, sino que se usa en negocios jurídicos con prestaciones aplazadas que son títulos ejecutivos extrajurisdiccionales, no obstante, lo cómodo que sería para el indicado servicio. Puede deberse a que no hay concierto en seguir los pasos de los modelos, que no parecen seriamente objetables. Desde luego, cuando el art. 578.2, párrafo 2.º LEC habla de liquidación final como condición de la solicitud ejecutiva, habrá de referirse a una prospección de la que resulte una vez se produzca el pago final de la prestación periódica toda, sin excluir pagos parciales. En cualquier caso, un despacho especial de la ejecución, y los aumentos de embargo (o mejoras de embargo, que significaría traba de otros bienes del ejecutado) por vencimientos ulteriores del débito, son siempre rogados.

========================================================================


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

Ilmo. Sr./a Magistrado-Juez D./Dña. [NOMBRE Y APELLIDOS]

En [LUGAR], a [DÍA] de [MES] de [AÑO].

ANTECEDENTES DE HECHO

ÚNICO.-

Por el/la Procurador/a Sr./a. [NOMBRE Y APELLIDOS], en nombre y representación de Doña [NOMBRE Y APELLIDOS], se ha presentado escrito que solicitaba el despacho de ejecución frente a Don [NOMBRE Y APELLIDOS], con fundamento en la siguiente resolución judicial l:

CLASE Y FECHA DE LA RESOLUCIÓN:

Auto de [FECHA], y sentencia de [FECHA].

JUICIO EN QUE HA SIDO DICTADA:

Pieza separada de medidas provisionales n.º [NÚMERO]/[AÑO] y autos principales de separación contenciosa n.º [NÚMERO]/[AÑO].

EJECUTANTE: Doña [NOMBRE Y APELLIDOS]

EJECUTADO: DON [NOMBRE Y APELLIDOS]

CANTIDAD OBJETO DE CONDENA: Pensiones mensuales actualizables conforme al IPC desde el mes [MES] de [AÑO].

CANTIDAD RECLAMADA: [IMPORTE] euros por principal, más [IMPORTE] euros para intereses y costas, con ampliación automática de los vencimientos mensuales.

FUNDAMENTOS DE DERECHO

PRIMERO.- Los títulos presentados llevan aparejada ejecución conforme a lo establecido en los nos. 1.º y 9.º del art. 517.2 LEC, en relación con el art. 776 LEC, siendo la cantidad líquida y determinable.

SEGUNDO.- El escrito reúne los requisitos legalmente establecidos del art. 549.2 LEC y los presupuestos procesales que exige el art. 551 LEC y, de conformidad con el examen que impone el art. 546 LEC, este tribunal se entiende competente. Adecuándose lo solicitado al título ejecutivo procede despachar la ejecución como se pide.

TERCERO.- Igualmente se acredita la concurrencia de los requisitos exigidos en el art. 578.2 LEC para solicitar la ampliación automática de la ejecución, al tratarse de obligación con prestaciones periódicas líquidas, habiéndose de aportar la liquidación final que en dicho precepto se prevé.

Vistas las normas citadas y demás de aplicación,

PARTE DISPOSITIVA

1.- Se despacha a instancias de Doña [NOMBRE Y APELLIDOS], parte ejecutante, ejecución frente a Don [NOMBRE Y APELLIDOS], parte ejecutada, por las siguientes cantidades:

[IMPORTE] euros en concepto de principal e intereses vencidos, por pensiones vencidas hasta el mes de [MES] de [AÑO]

euros en concepto de presupuesto para intereses de mora procesal y costas del proceso de ejecución. TOTAL [IMPORTE] euros ( [IMPORTE] €).

2.- Adviértase al ejecutado, de conformidad con lo dispuesto en el art. 578.2 LEC, que la ejecución despachada se entenderá ampliada automáticamente si, en las fechas de vencimiento, día quinto de cada mes, no se hubieren consignado, a disposición del Tribunal en la Cuenta de Depósitos y Consignaciones, las cantidades correspondientes a las pensiones alimenticias pendientes de vencimiento (es decir, la suma de seiscientos euros para cada plazo, actualizables anualmente conforme al IPC que publique el INE).

3.- Hágase saber a las partes que, con arreglo a lo establecido en el art. 155.3 LEC, si cambiasen su domicilio durante la sustanciación del proceso, lo deberán comunicar inmediatamente a la Oficina judicial.

5.- Notifíquese la presente resolución al ejecutado, con copia de la demanda ejecutiva, sin citación ni emplazamiento, para que en cualquier momento pueda personarse en la ejecución, entendiéndose, en tal caso, con él las ulteriores actuaciones.

Contra esta resolución no cabe la interposición de recurso alguno (art. 551.4 LEC), sin perjuicio de la oposición que, con arreglo a la Ley y dentro de los diez días siguientes al de notificación, pueda formular el ejecutado.

Así lo acuerdo, mando y firmo:

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Juez/a
