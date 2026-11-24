---
name: contrato-privado-arrendamiento-rustico-segun-derecho-civ-0511
description: "Contrato privado de arrendamiento rústico según el Derecho civil catalán. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato privado de arrendamiento rústico según el Derecho civil catalán

> Formulario **CIV-0511** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 24-11-2026.

## Qué es

Modelo de contrato privado de arrendamiento rústico conforme al Derecho civil catalán

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato privado de arrendamiento rústico según el Derecho civil catalán» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato privado de arrendamiento rústico según el Derecho civil catalán” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:contrato-privado-arrendamiento-rustico-segun-derecho-civ-0511`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] Nº (3 veces)
- [ ] ESTADO CIVIL (2 veces)
- [ ] FECHA (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] LUGAR (2 veces)
- [ ] NIF (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] DENOMINACIÓN SOCIAL
- [ ] DESCRIPCIÓN DEL BIEN
- [ ] DOMICILIO
- [ ] DÍA
- [ ] FECHAS
- [ ] LOCALIDAD
- [ ] MES
- [ ] Nº DE PARCELA
- [ ] Nº DE POLÍGONO
- [ ] SUCURSAL
- [ ] TÍTULO DE PROPIEDAD

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

### Avisos de actualización (0) — se aplican en el texto, nunca se copian en el documento

- Ninguno.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Modelo de contrato privado de arrendamiento rústico conforme al Derecho civil catalán


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

En [LUGAR], a [FECHA].

REUNIDOS

DE UNA PARTE,

Don/Doña [NOMBRE Y APELLIDOS], estado civil [ESTADO CIVIL], mayor de edad, con domicilio en.. [DOMICILIO], provisto de N.I.F. [NIF].

Y DE OTRA,

Don/Doña [NOMBRE Y APELLIDOS], estado civil [ESTADO CIVIL], mayor de edad, con domicilio en. [NÚMERO], provisto de N.I.F. [NIF].

INTERVIENEN

Don/Dña. [NOMBRE Y APELLIDOS], en su propio nombre y derecho, en lo sucesivo EL ARRENDADOR.

Don/Dña. [NOMBRE Y APELLIDOS], en su propio nombre y derecho, en lo sucesivo EL ARRENDATARIO.

Todas las partes, en el respectivo carácter con el que intervienen, se reconocen mutuamente la capacidad legal en Derecho necesaria para concertar el presente CONTRATO DE ARRENDAMIENTO RÚSTICO, y a tal efecto, libremente y de común acuerdo,

EXPONEN

Primero.- Que EL ARRENDADOR es propietario, en virtud de título de [TÍTULO DE PROPIEDAD], de la finca que a continuación se relaciona:

" [DESCRIPCIÓN DEL BIEN] " (Polígono [Nº DE POLÍGONO], parcela [Nº DE PARCELA], en [LOCALIDAD]), con una superficie aproximada de [Nº] hectáreas.

Segundo.- Que EL ARRENDATARIO está interesado en que se le arriende la finca anteriormente mencionada, por lo que las Partes, libremente y de común acuerdo, conciertan el presente CONTRATO DE ARRENDAMIENTO RÚSTICO con arreglo a las siguientes,

ESTIPULACIONES

I.- Objeto del contrato

EL ARRENDADOR arrienda al ARRENDATARIO, que tiene la condición de cultivador personal, la finca descrita en el exponiendo Primero del presente contrato.

II.- Aprovechamientos

EL ARRENDATARIO tiene derecho a determinar el tipo de cultivo, sin perjuicio de su obligación de devolver la finca al terminar el arriendo en el estado en que la recibió y de lo dispuesto sobre mejoras en el Código civil de Cataluña, pudiendo contratar siempre a su cargo, con completa indemnidad para la otra parte, a las personas que considere necesarias para ayudarle en la explotación.

El contrato de cultivo no se extiende a las edificaciones destinadas a vivienda que haya en la finca, pero sí a las otras construcciones, a la maquinaria y a las herramientas existentes.

III.- Duración del contrato

El presente arrendamiento se conviene y concierta por plazo inicial de siete años, en conformidad con el artículo 623.13.1 del Código civil de Cataluña.

IV.- Prórrogas

Transcurrido el plazo inicial de vigencia, el contrato se entenderá prorrogado por períodos de cinco años en cinco años. Tales prórrogas se sucederán indefinidamente en tanto una de las partes no comunique a la otra su voluntad de darlo por extinguido al menos un año antes del vencimiento.

EL ARRENDATARIO por su parte podrá renunciar a la duración del contrato o de la prórroga y abandonar el cultivo de la finca al término de cada año agrícola, notificándoselo al ARRENDADOR al menos con seis meses de antelación.

V.- Importe de la renta

El precio o renta inicial de este contrato se fija [IMPORTE] euros anuales ( [IMPORTE] €), pagaderos por años vencidos.

VI.- Pago de la renta

El pago se efectuará entre los días [FECHAS] y [DÍA] de cada mes de [MES] en la cuenta corriente n.º [NÚMERO] que EL ARRENDADOR tiene suscrita con la entidad [DENOMINACIÓN SOCIAL] en su sucursal [SUCURSAL].

VII.- Actualización de la renta

Transcurrido el primer año de vigencia del presente contrato, la renta pactada será actualizada cada año agrícola de acuerdo con el índice de precios percibidos agrarios publicada anualmente en el Diari Oficial de la Generalitat de Catalunya.

La renta actualizada será exigible al ARRENDATARIO a partir del mes siguiente a aquél en que EL ARRENDADOR se lo notifique por escrito, expresando el porcentaje de alteración aplicado. Se considerará valida la notificación hecha mediante anotación en el recibo de la anualidad precedente.

VIII.- Prohibición de subarriendo

EL ARRENDATARIO no podrá subarrendar la finca sin el consentimiento expreso del ARRENDADOR. Dicho consentimiento no será necesario cuando el subarriendo se efectúe a favor del cónyuge o de uno de los descendientes del ARRENDATARIO. No obstante, el subrogante y el subrogado notificarán fehacientemente al ARRENDADOR el subarriendo, en el plazo de [Nº] días hábiles a partir de su celebración.

IX.- Extinción

El contrato se extinguirá por las causas previstas en el Código civil de Cataluña.

X.- Seguro

Queda obligado EL ARRENDATARIO a suscribir seguro para el aseguramiento de los riesgos de la actividad de cultivo. Los gastos y primas que deba pagar EL ARRENDATARIO no podrán ser repercutidos en ningún caso al ARRENDADOR.

XI.- Incumplimiento contractual

En caso de incumplimiento, EL ARRENDADOR podrá instar el desahucio por falta de pago y serán de cargo del ARRENDATARIO todos los gastos y costas judiciales y extrajudiciales que origine su incumplimiento, incluso honorarios de Letrado y Procurador aunque la intervención de éstos no fuere preceptiva.

XII.- Sumisión a arbitraje

Para cuantas cuestiones o divergencias pudieran suscitarse en relación con el presente contrato, ambas partes establecen someterse al arbitraje de la Junta de Arbitraje y Mediación de Catalunya.

XIII.- Ley aplicable

El presente contrato tiene exclusivamente carácter civil y se regirá por sus propias cláusulas, y en lo en ellas no dispuesto, por lo previsto en los arts. 623.1 y ss. CCC, y demás leyes especiales aplicables.

XIV.- Notificaciones

Toda notificación que se efectúe entre las partes se hará por escrito y será entregada personalmente o de cualquier otra forma que certifique la recepción por la parte notificada en los respectivos domicilios indicados en el encabezamiento de este contrato.

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

Y en prueba de conformidad y aceptación de cuanto antecede, ambas partes firman los [Nº] folios del presente CONTRATO DE ARRENDAMIENTO RÚSTICO, extendido por duplicado y a un solo efecto, en la ciudad y fecha mencionados en el encabezamiento.

En [LUGAR], a [FECHA].

EL/LA ARRENDADOR/A:

EL/LA ARRENDATARIO/A
Don/Doña [NOMBRE Y APELLIDOS] Don/Doña [NOMBRE Y APELLIDOS]

========================================================================
