---
name: contrato-arrendamiento-vivienda-habitual-civ-0538
description: "Contrato de arrendamiento de vivienda habitual. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de arrendamiento de vivienda habitual

> Formulario **CIV-0538** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de arrendamiento de vivienda habitual» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de arrendamiento de vivienda habitual” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:contrato-arrendamiento-vivienda-habitual-civ-0538`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (7 veces)
- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] NÚMERO (5 veces)
- [ ] Nº (4 veces)
- [ ] AÑO (3 veces)
- [ ] CALLE (3 veces)
- [ ] DÍA (3 veces)
- [ ] MES (3 veces)
- [ ] CORREO ELECTRÓNICO (2 veces)
- [ ] DNI/NIE (2 veces)
- [ ] ESTADO CIVIL (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] ENTIDAD BANCARIA
- [ ] FINCA
- [ ] FOLIO
- [ ] LIBRO
- [ ] LUGAR
- [ ] PISO
- [ ] PLAZO
- [ ] PORCENTAJE
- [ ] PROVINCIA
- [ ] PUERTA
- [ ] RÉGIMEN ECONÓMICO MATRIMONIAL
- [ ] TELÉFONO
- [ ] TOMO
- [ ] TÍTULO DE ADQUISICIÓN

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

D/Dª [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], vecino de [LOCALIDAD], con domicilio en C/ [CALLE], nº [NÚMERO], y portador de DNI [DNI/NIE]

De otra:

D/Dª [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], vecino de [LOCALIDAD], con domicilio en Avda. nº [NÚMERO] y portador de DNI numero [DNI/NIE]

[ELEGIR UNA OPCIÓN: Intervienen / En nombre y representación de alguien / En su propio nombre y derecho]

EXPONEN

PRIMERO Que EL ARRENDADOR es propietaria en régimen de plena propiedad y dominio del inmueble sito en [LOCALIDAD], calle [CALLE] número [NÚMERO] con una superficie de [Nº] metros cuadrados.

Cuota de [PORCENTAJE] % en el valor del bloque donde está ubicado la citada vivienda y elementos comunes.

Título: Adquirido por [TÍTULO DE ADQUISICIÓN] efectuada en virtud de escritura pública otorgada ante el Notario de [LOCALIDAD], D. el día [DÍA] de [MES] de [AÑO] número protocolo

Inscripción: Está inscrita en el Registro de la Propiedad número [NÚMERO] de [LOCALIDAD] en el tomo [TOMO], libro [LIBRO] folio [FOLIO], finca [FINCA]

Referencia catastral: según consta en la referencia del último recibo del Impuestos sobre bienes Inmuebles que queda unido a este documento por copia.

Cargas: La referida finca se encuentra libre de cargas y gravámenes, según nota simple expedida por el Registro de la Propiedad el día de hoy, y que se une a este documento

Arrendamientos: La referida finca no se encuentra arrendada y está libre de ocupantes e inquilinos.

Gastos de Comunidad: El inmueble se encuentra al corriente en el pago de los gastos de comunidad de propietarios del edificio al que la finca pertenece, de acuerdo con el certificado expedido por la administración del Inmueble que queda unido a este documento.

Régimen de Comunidad: Se rige por lo dispuesto en los Estatutos de la Comunidad de Propietarios autorizados en virtud de escritura pública otorgada ante el Notario de [LOCALIDAD] D. el día [DÍA] de [MES] de [AÑO] y que LOS ARRENDATARIOS declara conocer, así como por lo dispuesto en la Ley de Propiedad Horizontal.

SEGUNDO Que los ARRENDATARIOS, casados en régimen de [RÉGIMEN ECONÓMICO MATRIMONIAL], y padres de dos menores, necesitan ocupar una vivienda en la localidad donde se encuentra la que ha sido descrita, para establecer su domicilio conyugal.

TERCERO Que encontrándose las partes de acuerdo en el arrendamiento del inmueble suprareferido, suscriben el presente contrato con arreglo a las siguientes,

CLÁUSULAS

Objeto

Constituye el objeto del presente contrato el arrendamiento de la vivienda que ha sido descrita, para su utilización como domicilio familiar.

Los ARRENDATARIOS reconocen haber recibido la vivienda, en el momento de la suscripción del presente contrato, en perfecto estado de conservación y al corriente de las licencias, gastos e Impuestos.

Se acompaña como Anexo I del presente contrato, un inventario donde se describen los muebles y electrodomésticos instalados en la vivienda.

Domicilio conyugal

Los ARRENDATARIOS manifiestan que no tienen una vivienda que cubra su necesidad de establecer su domicilio conyugal.

Como consecuencia de lo anterior, es de su interés fijar su domicilio familiar en la vivienda que ha sido descrita.

Duración del contrato

La duración del presente contrato se pacta por un periodo de [Nº] años.

No obstante, llegado el día del vencimiento del contrato, este se prorrogará obligatoriamente por plazos anuales hasta que el arrendamiento alcance una duración mínima de cinco años, o de siete años si el arrendador fuese persona jurídica, salvo que el ARRENDATARIO manifieste al ARRENDADOR, con treinta días de antelación como mínimo a la fecha de terminación del contrato o de cualquiera de las prórrogas, su voluntad de no renovarlo.

En el supuesto de que transcurran los cinco años recién señalados, o los siete años si el arrendador fuese persona jurídica, y ninguna de las partes comunicará su voluntad de dar por terminado el contrato, con treinta días de antelación a la fecha del vencimiento, se prorrogará por un año más.

Precio del arrendamiento

Se fija una renta de [IMPORTE] euros mensuales, que habrán de ser abonados en el número de cuenta del ARRENDADOR, dentro de los primeros cinco días de cada mes, de manera anticipada.

El ARRENDADOR designa la cuenta número [NÚMERO] de la entidad bancaria [ENTIDAD BANCARIA], como lugar de pago de la renta.

La renta pactada será actualizada, anualmente, tomando como referencia la evolución del Índice General de Precios al Consumo del Instituto Nacional de Estadística, que sea publicada el mes anterior al vencimiento de cada año de contrato.

La actualización se practicará aplicando el porcentaje correspondiente al IPC recién referido, a la última renta en vigor.

Fianza

Los ARRENDATARIOS hacen entrega en este acto de la cantidad de [IMPORTE] euros, en concepto de fianza.

El ARRENDADOR se obliga a devolver el referido importe, una vez comprobado el buen estado de la vivienda, a la finalización del presente contrato, para lo cual se compromete a revisar la misma en el plazo máximo de una semana, desde que se produzca la extinción de la relación contractual.

Gastos

El importe del impuesto de bienes inmuebles, consumos de agua, gas, electricidad, teléfono [TELÉFONO], así como la adquisición, reparación o sustitución de los contadores de suministros, son de cuenta y cargo exclusivo de los ARRENDATARIOS, quienes podrán concertar con las respectivas compañías suministradoras todos o algunos de los suministros de que está dotado el inmueble.

El impago de los citados conceptos, dará derecho al ARRENDADOR a resolver el contrato por incumplimiento de los ARRENDATARIOS.

Uso de la vivienda arrendada

La vivienda que se arrienda constituirá el domicilio familiar de los ARRENDATARIOS, debiéndose destinarse a tal fin, lo que impide que pueda ser utilizada para cualquier otro uso que fuera distinto al que ha sido referido.

El incumplimiento de la presente clausula, otorga la posibilidad al ARRENDADOR de resolver el contrato de manera unilateral.

Los ARRENDATARIOS se obligan a observar los usos de buena vecindad, comprometiéndose a cumplir las normas de la Comunidad de Propietarios del edificio donde se encuentra su vivienda, así como los estatutos, que afirman conocer.

Obras

Queda prohibida la posibilidad de realizar obras por parte de los ARRENDATARIOS, salvo consentimiento previo, por escrito, del ARRENDADOR.

Las obras que fueran realizadas por los ARRENDATARIOS, quedarán en beneficio del inmueble, sin derecho a indemnización, salvo que fueran inconsentidas, y el ARRENDADOR exigiera la reposición de la vivienda a su estado anterior.

El ARRENDADOR se compromete a hacerse cargo de los gastos de mantenimiento de la vivienda y de sus instalaciones o servicios, en estado de habitabilidad, para servir al uso convenido.

No obstante, las reparaciones que sean necesarias por el uso ordinario, serán de exclusiva cuenta de los ARRENDATARIOS, al igual que las obras que deban realizarse a causa de un daño doloso o mal uso de la cosa arrendada.

Los ARRENDATARIOS deberán permitir la entrada al ARRENDADOR y a los gremios que éste contrate, para los supuestos en los que deba realizar obras de conservación en la vivienda.

Los ARRENDATARIOS comunicarán, de manera urgente, al ARRENDADOR, la necesidad de llevar a cabo obras que pudieran atenerle a éste, permitiendo su acceso para inspeccionar las mismas.

Subarriendo y cesion de arrendamiento

Los ARRENDATARIOS no podrán ceder ni subarrendar la vivienda, total o parcialmente, a terceras personas, salvo consentimiento previo, por escrito, del ARRENDADOR.

Derecho de adquisicion preferente

Los ARRENDATARIOS tendrán un derecho de adquisición preferente sobre la vivienda, habida cuenta de que establecen en la misma su domicilio familiar, y tienen una clara vocación de permanencia en el inmueble.

En el supuesto de que el ARRENDADOR deseara vender la vivienda objeto de contrato, se obliga a comunicar el precio de venta a los ARRENDATARIOS, que podrán igualar las ofertas de los eventuales compradores, para adquirir el inmueble que nos ocupa.

Al hilo de lo anterior, los ARRENDATARIOS tendrán un plazo máximo de [PLAZO], para expresar por escrito su voluntad de ejercer el derecho de adquisición preferente regulado en el presente contrato, desde que les sea comunicada por el ARRENDADOR la existencia de un comprador de la vivienda.

Una vez expresada dicha voluntad, los ARRENDATARIOS se comprometen a otorgar la oportuna escritura pública de compraventa, en los [Nº] días siguientes a la referida comunicación.

El derecho de adquisición preferente quedará extinguido cuando transcurra un año desde la terminación del contrato de arrendamiento.

[ELEGIR UNA OPCIÓN: Jurisdicción competente y ley aplicable / Sumisión a Tribunales sin cláusula penal en caso de no ejecución voluntaria de la sentencia / Jurisdicción competente y ley aplicable / Sumisión a Tribunales con cláusula penal en caso de no ejecución voluntaria de la sentencia / — y además elegir: Sumisión a arbitraje / Sin cláusula penal en caso de no ejecución voluntaria del laudo / Con cláusula penal en caso de no ejecución voluntaria del laudo]

Notificaciones

A efectos de toda comunicación o requerimiento que hayan de oír las partes en relación con el presente contrato, incluidos los judiciales, se tomará como domicilio del arrendador el señalado al inicio del presente contrato, es decir, calle [CALLE], núm. [Nº], piso [PISO], puerta [PUERTA], de la localidad/ciudad de [LOCALIDAD], provincia de [PROVINCIA], y como domicilio de los arrendatarios la vivienda arrendada.

De conformidad a lo dispuesto en el artículo 4.6 de la Ley de Arrendamientos Urbanos, las partes designan las siguientes direcciones electrónicas para realizar las notificaciones:

- Por el arrendador [CORREO ELECTRÓNICO]

- Por los arrendatarios [CORREO ELECTRÓNICO]

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata, y por un medio que garantice la recepción del mensaje.

Generalidades

El presente contrato anula y reemplaza cualquier contrato o acuerdo anterior entre las partes con el mismo objeto y sólo podrá ser modificado por un nuevo acuerdo firmado por ambas partes.

Si alguna de las cláusulas del presente contrato fuere declarada nula o inaplicable, dicha cláusula se considerará excluida del contrato, sin que implique la nulidad del mismo. En este caso las partes harán cuanto esté a su alcance para encontrar una solución equivalente que sea válida y que refleje debidamente sus intenciones.

Los encabezamientos de las distintas cláusulas lo son sólo a efectos informativos, y no afectarán, calificarán o ampliarán la interpretación de este Contrato.

Las partes, en la representación con la que intervienen en este acuerdo, una vez leído, aceptan respetar y cumplir formalmente todas las condiciones y compromisos recogidos en el mismo, y en prueba de conformidad con su íntegro contenido, firman por duplicado este documento, extendido en ……. folios de papel común cumplimentados por una sola cara, a un sólo efecto, en el lugar y fecha indicados en el encabezamiento.

Fdo. D/Dª [NOMBRE Y APELLIDOS]

(El ARRENDADOR)

Fdo. Dª/D [NOMBRE Y APELLIDOS] y D/Dª [NOMBRE Y APELLIDOS]

(Los ARRENDATARIOS)

========================================================================
