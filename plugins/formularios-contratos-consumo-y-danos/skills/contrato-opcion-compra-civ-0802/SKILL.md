---
name: contrato-opcion-compra-civ-0802
description: "Contrato de opción de compra. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de opción de compra

> Formulario **CIV-0802** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Contrato en virtud del cual una parte (concedente) concede a otra (optante) la facultad exclusiva de decidir la celebración o no de otro principal de compraventa, que habrá de realizarse en plazo cierto, y en unas determinadas condiciones, pudiendo ir también acompañado del pago de una prima por parte del optante.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de opción de compra» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de opción de compra” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:contrato-opcion-compra-civ-0802`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (5 veces)
- [ ] NÚMERO (5 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] Nº (4 veces)
- [ ] AÑO (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] DÍA (2 veces)
- [ ] ESTADO CIVIL (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] MES (2 veces)
- [ ] CALLE
- [ ] DIRECCIÓN
- [ ] FECHA
- [ ] FOLIO
- [ ] LIBRO
- [ ] LUGAR
- [ ] Nº DE CLÁUSULA
- [ ] TIPO DE INMUEBLE
- [ ] TOMO

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

En [LUGAR], a [DÍA] de [MES] de [AÑO].

REUNIDOS

De una parte:

D [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número [NÚMERO]

De otra:

D [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número [NÚMERO]

[ELEGIR UNA OPCIÓN: Intervienen / En nombre de alguien / Nombre propio]

EXPONEN

PRIMERO.- Que LA CONCEDENTE es titular en pleno dominio del inmueble sito en el municipio de [LOCALIDAD] ubicada en el número [NÚMERO] de la Calle [CALLE] que a continuación se describe:

· Inmueble [TIPO DE INMUEBLE] situado en [DIRECCIÓN] número [NÚMERO] de [LOCALIDAD], cuyos datos registrales son los siguientes: Finca número [NÚMERO], inscrita en el Tomo [TOMO], Libro [LIBRO], Folio [FOLIO], constando una superficie de [Nº] metros cuadrados útiles de dicha vivienda en la inscripción registral.

· Corresponde a LA CONCEDENTE el 100% del pleno dominio de la totalidad de la finca.

SEGUNDO.- Que el inmueble descrito en el Exponendo I de este documento se halla libre de cargas, al corriente de impuestos y de toda clase de pagos a la comunidad de propietarios, según manifiesta LA CONCEDENTE.

TERCERO.- Que LA OPTANTE está interesada en adquirir en un futuro próximo el inmueble descrito en el Exponendo Primero.

CUARTO.- Que estando LA CONCEDENTE interesada en la venta y LA OPTANTE en la compra de la finca descrita en el Exponendo Primero, ambas partes, de mutuo acuerdo, formalizan el presente CONTRATO DE OPCIÓN DE COMPRA, el cual se regirá por las siguientes

CLÁUSULAS

Objeto

LA CENDENTE concede a LA OPTANTE, que acepta en el presente acto, un derecho de opción de compra sobre la finca antes descrita.

El OPTANTE declara expresamente que conoce la situación física y jurídica del inmueble objeto del presente contrato.

[ELEGIR UNA OPCIÓN: Valor de la opción / Al contado / Aplazado]

Plazo para el ejercicio de la opción

EL OPTANTE deberá ejercer su derecho de opción de compra dentro del plazo máximo de [Nº] días/meses/años, contados a partir de la fecha de celebración del presente contrato.

En el supuesto de que el OPTANTE ejercitase su derecho de opción de compra, deberá hacerlo mediante requerimiento al CONCEDENTE del que quede constancia escrita. La opción no se entenderá ejercitada si en el acto de la firma de la escritura de compraventa EL OPTANTE no entregase el pago dinerario previsto en [Nº DE CLÁUSULA] y garantizase con condición resolutoria expresa las cantidades aplazadas.

Transcurrido dicho plazo, sin que se ejercite en su totalidad el derecho adquirido, la opción caducará de pleno derecho, sin necesidad de requerimiento o aviso de clase alguno.

Precio de la venta

Ambas partes, de mutuo acuerdo, fijan el precio de venta en la cantidad de [IMPORTE] euros ( €), más los impuestos que graven dicha transmisión. La forma de pago del precio será la siguiente:

1. euros ( €), que se entregan en este acto en concepto de valor de la opción, y cuyo importe se imputará al precio de venta.

2. euros ( €), en el momento de la formalización de la correspondiente escritura pública de compraventa.

3. La cantidad restante, en [Nº] plazos mensuales consecutivos, siendo el primero de ellos el día [DÍA] de [MES] de [AÑO].

Cláusula de reserva de dominio de la futura venta

La futura venta se entenderá hecha con reserva de dominio a favor de LA CONCEDENTE hasta el momento en que el importe total del presente contrato de compraventa haya sido satisfecho, esto es, hasta el día [FECHA]

La cláusula de reserva de dominio a favor de LA CONCEDENTE quedará automáticamente extinguida en el momento en que LA OPTANTE haya satisfecho la totalidad de la contraprestación a la que estaba obligada, momento en que el bien pasará a ser de plena propiedad de LA OPTANTE sin limitación alguna.

Cargas y gravámenes

En el caso de ejercitarse la opción, el bien deberá entregarse libre de cargas y gravámenes, por lo que EL CONCEDENTE deberá cancelar cualquier carga que pudiera existir con anterioridad a la firma de la escritura de compraventa, inclusive las que le correspondan por motivos urbanísticos.

Inscripción del derecho de opción de compra en el registro

Cualquiera de las partes podrá solicitar con.. días de antelación como mínimo, la elevación a público de este contrato para que tenga acceso al Registro de la Propiedad y garantice el derecho del OPTANTE frente a terceros.

El solicitante de la elevación a escritura pública designará día y Notario del término municipal de [LOCALIDAD] ante el que se deberá firmar el mencionado documento público.

Los gastos de la elevación a Escritura Pública, serán de cargo de [ELEGIR: el optante / el concedente / ambas partes]

Incumplimiento del contrato

Si el CONCEDENTE no otorgara la escritura de venta, deberá abonar al OPTANTE la cantidad de [IMPORTE] euros ( €), además de devolver la cantidad recibidas por razón del presente contrato.

Gastos e impuestos

Todos los gastos e impuestos que se originen como consecuencia de la formalización, cumplimiento o extinción del presente contrato y de las obligaciones que de él se deriven serán de cargo de

Igualmente, los gastos judiciales que se ocasionen por incumplimiento del presente contrato serán por cuenta de la parte incumplidora, incluidos honorarios del Procurador y Abogado aunque sus intervenciones no fueran preceptivas.

Jurisdicción competente y ley aplicable

Para cuantas cuestiones o divergencias pudieran suscitarse en relación con el presente contrato, la competencia de los Tribunales que deban conocer del asunto se determinará de conformidad con los criterios de competencia objetiva, funcional y territorial legalmente aplicables.

El presente contrato tiene exclusivamente carácter civil y se regirá por sus propias cláusulas, y en lo en ellas no dispuesto, por lo previsto en el Código Civil y, demás leyes especiales.

[ELEGIR UNA OPCIÓN: Sumisión a tribunales / Sin cláusula penal / Con cláusula penal / — y además elegir: Sumisión a arbitraje / Sin cláusula penal / Con cláusula penal]

Notificaciones

Toda notificación que se efectúe entre las partes se hará por escrito y será entregada personalmente o de cualquier otra forma que certifique la recepción por la parte notificada en los respectivos domicilios indicados en el encabezamiento de este Contrato.

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

Generalidades

El presente contrato anula y reemplaza cualquier contrato o acuerdo anterior entre las partes con el mismo objeto y sólo podrá ser modificado por un nuevo acuerdo firmado por ambas partes.

Si alguna de las cláusulas del presente contrato fuere declarada nula o inaplicable, dicha cláusula se considerará excluida del contrato, sin que implique la nulidad del mismo. En este caso las partes harán cuanto esté a su alcance para encontrar una solución equivalente que sea válida y que refleje debidamente sus intenciones.

Los encabezamientos de las distintas cláusulas lo son sólo a efectos informativos, y no afectarán, calificarán o ampliarán la interpretación de este Contrato.

Y en prueba de conformidad y aceptación de cuanto antecede, ambas partes firman los [Nº] folios del presente CONTRATO DE OPCIÓN DE COMPRA, extendido por duplicado y a un solo efecto, en la ciudad y fecha mencionados en el encabezamiento.

Fdo. Don [NOMBRE Y APELLIDOS]

(La Optante)

Fdo. Don [NOMBRE Y APELLIDOS]

(La Concedente)

========================================================================
