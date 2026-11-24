---
name: alquiler-instalaciones-deportivas-contrato-civ-0499
description: "Alquiler de instalaciones deportivas (contrato). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Alquiler de instalaciones deportivas (contrato)

> Formulario **CIV-0499** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Alquiler de instalaciones deportivas (contrato)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Alquiler de instalaciones deportivas (contrato)” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:alquiler-instalaciones-deportivas-contrato-civ-0499`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (6 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] NÚMERO (4 veces)
- [ ] ACTIVIDAD (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] NOMBRE DEL EVENTO (2 veces)
- [ ] PORCENTAJE (2 veces)
- [ ] AÑO
- [ ] CALLE
- [ ] DENOMINACIÓN SOCIAL
- [ ] DESCRIPCIÓN DEL BIEN
- [ ] DÍA
- [ ] ESTADO CIVIL
- [ ] FECHA
- [ ] FOLIO
- [ ] HORA
- [ ] LIBRO
- [ ] LUGAR
- [ ] MES
- [ ] Nº DE FINCA
- [ ] TOMO

## Normas que cita el formulario

- art. 1.851 Código Civil

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

- Junto a «…UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD)»: La LO 15/1999 y su Reglamento (RD 1720/2007) fueron sustituidos por el Reglamento (UE) 2016/679 (RGPD) y la LO 3/2018, de 5 de diciembre (LOPDGDD). Fuente: LO 3/2018, disposición derogatoria única.

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

D D [NOMBRE Y APELLIDOS], mayor de edad, de estado civil, vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número [NÚMERO]

[ELEGIR UNA OPCIÓN: Intervienen / Si intervienen en nombre y representación de alguien / Opción 1: Si intervienen en nombre y representación de alguien / Si intervienen en su propio nombre y derecho / Opción 2: Si intervienen en su propio nombre y derecho]

EXPONEN

Que LA ARRENDADORA es propietaria en régimen de plena propiedad y dominio de las instalaciones deportivas sitas en [LOCALIDAD], calle [CALLE] número [NÚMERO] con una superficie de [Nº] metros cuadrados inscrito en el Registro de la Propiedad de [LOCALIDAD] en el Tomo [TOMO], Libro [LIBRO], Folio [FOLIO], Finca [Nº DE FINCA] e inscripción número

Las Instalaciones comprenden instalación deportiva denominada [DESCRIPCIÓN DEL BIEN], sus instalaciones eléctricas, vestuarios, gradas, parqueaderos, accesos, y sistemas de seguridad.

Que LA ARRENDATARIA es una sociedad dedicada a [ACTIVIDAD], que busca por el bienestar social de la comunidad, especialmente de sus dependientes, asociados, y empleados, estando interesada en desarrollar la actividad deportiva [ACTIVIDAD] en las instalaciones LA ARRENDADORA, beneficiándose de la infraestructura global que se pone a disposición de LA ARRENDATARIA.

Como quiera que ambas partes se encuentran interesadas en el arrendamiento de las Instalaciones supra referidas, ambas partes de común acuerdo llevan a efecto el presente contrato con arreglo a las siguientes:

CLÁUSULAS

Objeto

Constituye el objeto del presente contrato el arrendamiento de las Instalaciones deportivas, así como sus vestuarios, casilleros, instalaciones eléctricas, gradas, aparcamientos y sistemas de seguridad, para que este último desarrolle bajo su propio riesgo el evento denominado [NOMBRE DEL EVENTO] cuyas características se encuentran definidas en el Anexo I de este contrato.

LA ARRENDATARIA tendrá derecho al uso de [Nº] plazas de aparcamiento, los accesos a las Instalaciones y la infraestructura general del espacio objeto de arrendamiento.

Precio

LA ARRENDADORA recibirá la cantidad de [IMPORTE] EUROS ( €) por el alquiler de las instalaciones deportivas en aquellos casos en que el evento a realizar supere la cantidad de [IMPORTE] personas y sea inferior a

A la firma del presente contrato, se entregará en concepto de depósito, el 50% del importe total del arrendamiento concertado. En caso de cancelación del arrendamiento de las instalaciones, por parte del arrendatario, éste perderá el importe de dicho depósito pero la arrendataria podrá solicitar un único cambio de fecha del mismo evento que le concederá el arrendador siempre que esté disponible, pudiendo la Arrendadora aplicarla a los gastos generales por tal anulación.

Obligaciones de la arrendataria

LA ARRENDATARIA se compromete a cumplir con diligencia todas las obligaciones contenidas en el presente contrato y todas aquellas que se desprendan del normal cumplimiento y ejecución del contrato, entre las cuales especialmente se encuentran:

1. Desarrollo de la prestación exclusiva del evento deportivo detallado en el Anexo I de este contrato, por su cuenta y riesgo y bajo su vigilancia y control, siendo de su exclusiva responsabilidad la invitación, ejecución, terminación y liquidación.

2. Indemnizar a LA ARRENDADORA por cualquier daño o perjuicio que le pudiera causar a éste, con motivo o desarrollo del presente contrato, en todos los eventos en que el daño fuese causado por éste, sus dependientes o los participantes del evento.

3. Acatar los reglamentos internos y cumplir con la organización, disciplina y medidas de seguridad establecidas por LA ARRENDADORA que se adjuntan como Anexo II.

4. Desarrollar el evento dentro de los horarios autorizados por LA ARRENDADORA

5. LA ARRENDATARIA responderá ante los participantes del evento por cualquier inconformidad y perjuicio causados por éste, salvaguardando de cualquier tipo de responsabilidad a EL CONCEDENTE

6. Restituir las Instalaciones en las mismas condiciones de recibo, salvo el deterioro natural por uso a la terminación del evento, suscribiendo la respectiva acta de entrega.

7. Pagar a LA ARRENDADORA la remuneración acordada por el uso de las Instalaciones en las condiciones y plazos previstos en el presente contrato.

8. Presentar para aprobación de LA ARRENDADORA cualquier tipo de publicidad del evento, previa difusión del mismo, debiendo atender la regulación de imagen institucional de LA ARRENDADORA

9. Asumir la custodia y guarda de los bienes de su propiedad que sean utilizados en el evento objeto de este contrato.

10. Implementar y desarrollar todas las condiciones de seguridad sobre los bienes, las actividades y operaciones ejecutadas en virtud del presente contrato.

Obligaciones de la arrendadora

LA ARENDADORA se compromete a cumplir con diligencia todas las obligaciones contenidas en el presente contrato y todas aquellas que se desprendan del normal cumplimiento y ejecución del contrato, entre las cuales especialmente se encuentran:

1. Permitir y propiciar el uso de la instalación deportiva y la infraestructura global para el desarrollo del evento denominado [NOMBRE DEL EVENTO] el cual se realizará por EL CONCESIONARIO en forma independiente y autónoma por su cuenta y riesgo.

2. Comunicar por escrito y con mínimo [Nº] días de anticipación cualquier modificación que se presente en los horarios de acceso a las áreas entregadas en concesión.

3. Designar un Supervisor, para la revisión de la actividad y la suscripción del acta de entrega.

4. Estudiar y autorizar los medios publicitarios del evento presentados por LA ARRENDATARIA

5. Realizar la revisión del área objeto de concesión al momento de entregar, reportando los defectos que se observen en la misma al momento de la culminación del evento.

Horario del evento

El horario del evento acordado entre las partes, para la prestación de la actividad deportiva, es de [HORA] a [Nº] horas del día [FECHA], fecha en la cual se encontrará en funcionamiento la instalación deportivas.

Promocion comercial

La promoción comercial del evento se encontrara a cargo de LA ARRENDATARIA previa coordinación con la persona o personas que para este fin exclusivo, determine LA ARRENDADORA. Todo anuncio publicitario, documento o medio visual o sonoro que cumpla con tal finalidad, deberá ser previamente aprobada por LA ARRENDADORA para asegurar el buen uso de la imagen institucional

Control de acceso

LA ARRENDADORA se reserva el derecho de controlar la entrada y salida de bienes, por parte de LA ARRENDATARIA o de cualquiera de los empleados, dependientes o participantes del evento. Por ello, LA ARRENDATARIA deberá informar a LA ARRENDADORA, las personas invitadas al evento así como los bienes objeto de su propiedad que ingresarán a las instalaciones de LA ARRENDADORA, para el desarrollo del presente contrato.

Fianza

LA ARRENDATARIA debe hacer entrega a LA ARRENDADORA en concepto de fianza, de un [PORCENTAJE] % del importe del arrendamiento.

La fianza le será devuelta a LA ARRENDADATARIA en el plazo de [Nº] días contados a partir del momento de la devolución de la habitación arrendada una vez cumplidas por LA ARRENDATARIA las obligaciones contraídas, a cuya responsabilidad queda afectada, así como al resarcimiento de daños y perjuicios, sirviendo este documento como formal carta de pago. Dicha fianza no devengará intereses.

Queda establecido que bajo ningún concepto LA ARRENDATARIA podrá canjear la fianza depositada en este acto por ninguna mensualidad de alquiler, ni cualquier otro pago inherente al presente contrato de arrendamiento.

Avalista/fiador

D.(nombres y apellidos), provisto de D.N.I. número [NÚMERO] y presente en este acto, se constituye en fiador/avalista de las obligaciones contraídas por LA ARRENDATARIA con LA ARRENDADORA, obligándose solidariamente con LA ARRENDATARIA al cumplimiento de las obligaciones arrendaticias y especialmente al pago de la renta, así como a cualquier cantidad económica que se derive del presente contrato o por disposición legal, y a la conservación del buen estado de las Instalaciones por toda la duración del contrato, con renuncia expresa a los beneficios de excusión, división.

A tal efecto, acepta de antemano cualquier prórroga o renovación que LA ARRENDADORA pudiera conceder, sea cual sea la forma en que se instrumente la misma, sin que, en consecuencia, la concesión de la indicada prórroga o renovación pueda producir los efectos establecidos en el artículo 1.851 del Código Civil.

Seguro

LA ARRENDATARIA contratará un seguro que resulte satisfactorio para LA ARRENDADORA y que cubra el riesgo de daños o pérdida que pueda sufrir las Instalaciones durante todo el periodo de vigencia del presente contrato.

Honorarios del mediador inmobiliario

En este arrendamiento ha intervenido como mediador la entidad [DENOMINACIÓN SOCIAL]

Mediante el presente contrato se fijan los honorarios por la intervención de la referida entidad en el [PORCENTAJE] % de la renta de un año.

El precio fijado se pagará por la parte arrendadora y por la arrendataria por mitad e iguales partes.

Resolución del contrato

El incumplimiento de las obligaciones que resulten del presente contrato facultará a la parte que cumpla los suyos a exigir a la otra su cumplimiento, o, a su elección, a resolver el contrato, con abono en ambos casos de la indemnización por daños y perjuicios que proceda.

Gastos e Impuestos

Todos los gastos e impuestos que se originen como consecuencia del evento, así como la obtención de las licencias y permisos necesarios para su celebración serán de cargo de la parte arrendataria.

Igualmente, los gastos judiciales que se ocasionen por incumplimiento del presente contrato serán por cuenta de la parte incumplidora, incluidos honorarios del Procurador y Abogado aunque sus intervenciones no fueran preceptivas.

Jurisdicción competente y ley aplicable

El conocimiento de los litigios relativos a que diera lugar la interpretación y/o ejecución del presente contrato corresponderá al Tribunal de Instancia del lugar en que se halle la finca.

El presente contrato tiene carácter civil, se regirá por sus propias cláusulas, y en lo en ellas no dispuesto, por lo previsto en el Código Civil y demás leyes especiales.

Notificaciones

Toda notificación que se efectúe entre las partes se hará por escrito y será entregada personalmente o de cualquier otra forma que certifique la recepción por la parte notificada en los respectivos domicilios indicados en el encabezamiento de este Contrato.

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

Generalidades

El presente contrato anula y reemplaza cualquier contrato o acuerdo anterior entre las partes con el mismo objeto y sólo podrá ser modificado por un nuevo acuerdo firmado por ambas partes.

Si alguna de las cláusulas del presente contrato fuere declarada nula o inaplicable, dicha cláusula se considerará excluida del contrato, sin que implique la nulidad del mismo. En este caso las partes harán cuanto esté a su alcance para encontrar una solución equivalente que sea válida y que refleje debidamente sus intenciones.

Los encabezamientos de las distintas cláusulas lo son sólo a efectos informativos, y no afectarán, calificarán o ampliarán la interpretación de este Contrato.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

Y en prueba de conformidad y aceptación de cuanto antecede, ambas partes firman los [Nº] folios del presente CONTRATO DE ALQUILER INSTALACIONES DEPORTIVAS, extendido por duplicado y a un solo efecto, en la ciudad y fecha mencionados en el encabezamiento.

Fdo. Don [NOMBRE Y APELLIDOS]

(La Arrendadora)

Fdo. Don [NOMBRE Y APELLIDOS]

(La Arrendataria)
