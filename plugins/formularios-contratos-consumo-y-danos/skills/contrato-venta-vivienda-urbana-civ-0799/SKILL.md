---
name: contrato-venta-vivienda-urbana-civ-0799
description: "Contrato de venta de una vivienda urbana. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de venta de una vivienda urbana

> Formulario **CIV-0799** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de venta de una vivienda urbana» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de venta de una vivienda urbana” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:contrato-venta-vivienda-urbana-civ-0799`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (11 veces)
- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] Nº (5 veces)
- [ ] NÚMERO (5 veces)
- [ ] AÑO (4 veces)
- [ ] DÍA (4 veces)
- [ ] MES (4 veces)
- [ ] DOMICILIO (2 veces)
- [ ] ESTADO CIVIL (2 veces)
- [ ] FECHA (2 veces)
- [ ] FOLIO (2 veces)
- [ ] LIBRO (2 veces)
- [ ] NOMBRE DEL REPRESENTADO/A (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL NOTARIO (2 veces)
- [ ] Nº DE PROTOCOLO (2 veces)
- [ ] TOMO (2 veces)
- [ ] CALLE
- [ ] FINCA
- [ ] IMPORTE
- [ ] LUGAR
- [ ] NOMBRE DEL ARRENDATARIO
- [ ] Nº DE FINCA
- [ ] OBJETO DE LA RECLAMACIÓN

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

INTERVIENEN

D [NOMBRE Y APELLIDOS], en nombre y representación de [NOMBRE DEL REPRESENTADO/A], en lo sucesivo "LA VENDEDORA", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D [NOMBRE Y APELLIDOS DEL NOTARIO], en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO], poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD] y vigente, según manifiesta.

D [NOMBRE Y APELLIDOS], en nombre y representación de [NOMBRE DEL REPRESENTADO/A], en lo sucesivo "LA COMPRADORA", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D [NOMBRE Y APELLIDOS DEL NOTARIO], en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO], poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD] y vigente, según manifiesta.

Todas las partes, en el respectivo carácter con el que intervienen, se reconocen mutuamente la capacidad legal en Derecho necesaria para concertar el presente CONTRATO DE COMPRAVENTA DE VIVIENDA URBANA, y a tal efecto, libremente y de común acuerdo,

[ELEGIR: Exponen]

PRIMERO.- Que LA VENDEDORA es propietaria en régimen de plena propiedad y dominio del inmueble sito en [LOCALIDAD], calle [CALLE] número [NÚMERO] con una superficie de [Nº] metros cuadrados inscrito en el Registro de la Propiedad de [LOCALIDAD] en el Tomo [TOMO], Libro [LIBRO], Folio [FOLIO], Finca [Nº DE FINCA] e inscripción número [NÚMERO], en el que se desarrolla la actividad de

Cuota de % en el valor del bloque donde está ubicado el citado local y elementos comunes.

Título: Adquirido por efectuada en virtud de escritura pública otorgada ante el Notario de [LOCALIDAD], D. el día [DÍA] de [MES] de [AÑO] número protocolo

Inscripción: Está inscrita en el Registro de la Propiedad número [NÚMERO] de [LOCALIDAD] en el tomo [TOMO], libro [LIBRO] folio [FOLIO], finca [FINCA]

Referencia catastral: según consta en la referencia del último recibo del Impuestos sobre bienes Inmuebles que queda unido a este documento por copia.

Cargas: La referida finca se encuentra libre de cargas y gravámenes, según nota simple expedida por el Registro de la Propiedad el día de hoy, y que se une a este documento.

Arrendamientos: La referida finca no se encuentra arrendada y está libre de ocupantes e inquilinos.

Gastos de Comunidad: El inmueble se encuentra al corriente en el pago de los gastos de comunidad de propietarios del edificio al que la finca pertenece, de acuerdo con el certificado expedido por la administración del Inmueble que queda unido a este documento.

Régimen de Comunidad: Se rige por lo dispuesto en los Estatutos de la Comunidad de Propietarios autorizados en virtud de escritura pública otorgada ante el Notario de [LOCALIDAD] D. el día [DÍA] de [MES] de [AÑO] y que la parte compradora declara conocer, así como por lo dispuesto en la Ley de Propiedad Horizontal.

Hipotecada

CLÁUSULAS

Objeto

Constituye el objeto del presente contrato la compraventa de la vivienda descrita en el Exponendo Primero en pleno dominio, libre de cargas y arrendamientos, al corriente en el pago de los gastos generales de la comunidad de propietarios a cuyos efectos se aporta certificación del secretario administrador con el Vº Bº del presidente y con cuantos derechos le correspondan de acuerdo con la Ley de Propiedad Horizontal.

Precio

El precio de la venta de la vivienda descrita en el Exponendo primero se concreta en la cantidad de [IMPORTE] euros (€).

[ELEGIR UNA OPCIÓN: Forma de pago / En firma del contrato / Subrogación de hipoteca / — y además elegir: Entrega / Con escritura pública / Firma del contrato]

Situación arrendaticia

LA COMPRADORA queda subrogada en los derechos y obligaciones derivados del contrato de arrendamiento del inmueble vigente entre LA VENDEDORA y [NOMBRE DEL ARRENDATARIO], cuyos términos y condiciones figuran en el Anexo I del presente contrato.

Reserva de usufructo a favor de la vendedora

Ambas partes de común acuerdo establecen un usufructo en favor de LA VENDEDORA de la referida finca por un plazo de [Nº] años.

Vencido dicho plazo, se levantará el usufructo, entrando LA COMPRADORA en posesión del uso y disfrute de la misma en calidad de dueña que es, sin sujeción a usufructo alguno.

EVICCIÓN (Contienda pendiente)

LA COMPRADORA conoce que LA VENDEDORA ha tenido que sustanciar un procedimiento judicial contrata un tercero que pretendía reclamar [OBJETO DE LA RECLAMACIÓN], que es objeto de este contrato.

LA VENDEDORA responderá solamente de la posesión legal pero no de la posesión pacífica. LA COMPRADORA acepta la limitación establecida por LA VENDEDORA a su derecho de saneamiento.

Pacto de retro

LA VENDEDORA se reserva el derecho a recuperar la cosa vendida reembolsando a LA COMPRADORA el precio de la venta y los gastos necesarios y útiles, incluidos impuestos y demás gastos notariales y registrales, hechos en la cosa vendida, y siendo de cuenta de la parte vendedora todos los gastos que origine la retroventa.

Este derecho podrá ser ejercitado por LA VENDEDORA en el plazo de [Nº] años a contar desde la firma del presente contrato.

Transcurrido el indicado plazo sin que por la parte vendedora se haya retraído, LA COMPRADORA adquirirá irrevocablemente el dominio del inmueble vendido.

Resolución del contrato

El Contrato podrá resolverse por las siguientes causas:

1. Por voluntad de cualquiera de las Partes cuando medie incumplimiento grave de las obligaciones pactadas.

2. Por acuerdo de las Partes por escrito.

3. La extinción de la personalidad jurídica de cualquiera de las Partes o la suspensión de pagos, quiebra, concurso o embargo de bienes de alguna de ellas a menos que se garantice de cualquier forma la deuda.

En cualquier caso, la Parte que pretenda resolver el presente Contrato alegando incumplimiento de la contraparte, deberá requerirle al cumplimiento de la obligación de forma fehaciente, otorgándole un plazo de [Nº] días a la Parte incumplidora para que pueda subsanar dicho incumplimiento. Transcurrido dicho plazo sin que los incumplimientos hubiesen sido subsanados, el perjudicado podrá ejercitar la mencionada facultad.

En el supuesto de que los incumplimientos fueren de imposible subsanación en el plazo de 30 días, el perjudicado podrá ejercitar directamente la facultad opción, sin necesidad de remitir, previamente, el antedicho requerimiento.

La resolución del contrato por esta causa producirá los mismos efectos que el incumplimiento de la obligación de pago en lo que a recuperación de la maquinaria e indemnización de los daños y perjuicios respecta.

Elevación a escritura pública

La escritura pública de compraventa se otorgará al primer requerimiento de cualquiera de las partes, comprometiéndose LA VENDEDORA a comparecer a dicho otorgamiento para hacer constar en la escritura pública el consentimiento prestado para la venta de la vivienda objeto de este contrato.

La escritura pública se otorgará ante el Notario que acuerden la parte [ELEGIR: compradora / vendedora]

En todo caso la escritura pública deberá otorgarse antes del próximo día [DÍA] de [MES] de [AÑO].

De no comparecer alguna de las partes al otorgamiento de la escritura pública, podrá la parte que haya requerido para ello ejercitar las acciones judiciales tendentes a solicitar el referido otorgamiento. En este caso, la parte que no haya comparecido a dicho otorgamiento quedará obligada a indemnizar a la otra parte en una cantidad equivalente el importe de los gastos que se hayan derivado del ejercicio de dichas acciones, así como al pago de los daños y perjuicios que dicho incumplimiento hayan causado al requirente.

Gastos e impuestos

Será de cuenta de LA VENDEDORA el impuesto sobre incremento del valor de los terrenos (Plusvalía municipal).

Será de cargo de LA COMPRADORA los gastos de otorgamiento de la escritura pública de compraventa así como los gastos derivados de la expedición de la primera copia y sucesivas de la escritura pública, el importe del Impuesto de Transmisiones Patrimoniales, al que está sujeto esta compraventa y al pago de los gastos derivados de la inscripción en el Registro de la Propiedad.

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

Y en prueba de conformidad y aceptación de cuanto antecede, ambas partes firman los [Nº] folios del presente CONTRATO DE COMPRAVENTA DE VIVIENDA, extendido por duplicado y a un solo efecto, en la ciudad y fecha mencionados en el encabezamiento.

Fdo. Don [NOMBRE Y APELLIDOS]

(La VENDEDORA)

Fdo. Don [NOMBRE Y APELLIDOS]

(La COMPRADORA)

========================================================================
