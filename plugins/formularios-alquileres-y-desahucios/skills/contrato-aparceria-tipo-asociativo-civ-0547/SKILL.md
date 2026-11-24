---
name: contrato-aparceria-tipo-asociativo-civ-0547
description: "Contrato de aparcería de tipo asociativo. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de aparcería de tipo asociativo

> Formulario **CIV-0547** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de aparcería de tipo asociativo» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de aparcería de tipo asociativo” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:contrato-aparceria-tipo-asociativo-civ-0547`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] ACTIVIDAD (3 veces)
- [ ] IMPORTE (3 veces)
- [ ] Nº (3 veces)
- [ ] OBJETO DEL CONTRATO (3 veces)
- [ ] DOMICILIO (2 veces)
- [ ] ESTADO CIVIL (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] Nº DE PARCELA (2 veces)
- [ ] Nº DE POLÍGONO (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] PARAJE O MUNICIPIO (2 veces)
- [ ] AÑO
- [ ] DÍA
- [ ] LUGAR
- [ ] MES

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

[ELEGIR UNA OPCIÓN: Intervienen / En representación / Nombre propio]

Manifiestan

PRIMERO.- Que D. se dedica a [ACTIVIDAD], está interesada en [OBJETO DEL CONTRATO] y cuenta con las siguientes fincas rústicas:

-"" (Polígono [Nº DE POLÍGONO], parcela [Nº DE PARCELA], en [PARAJE O MUNICIPIO]), con una superficie aproximada de [Nº] hectáreas

-"" (Polígono [Nº DE POLÍGONO], parcela [Nº DE PARCELA], en [PARAJE O MUNICIPIO]), con una superficie aproximada de [Nº] hectáreas

SEGUNDA.- Que D. se dedica a [ACTIVIDAD], está interesada en [OBJETO DEL CONTRATO] y cuenta con las instalaciones, maquinarias, utensilios y aperos descritos en el Anexo I, que puede poner a disposición de la explotación conjunta;

TERCERO.- Que D. se dedica a [ACTIVIDAD], está interesada en [OBJETO DEL CONTRATO] y cuenta con las instalaciones, maquinarias, utensilios y aperos descritos en el Anexo I, que puede poner a disposición de la explotación conjunta;

CUARTO.- A la luz de sus actividades, capacidades y objetivos, según se describen arriba, las Partes desean constituir una explotación agrícola que será conducida con arreglo a las siguientes:

CLÁUSULAS

Objeto

Las Partes acuerdan unir los recursos y esfuerzos mencionados en el Expositivo de este contrato mediante la constitución de una explotación agrícola en régimen de aparcería asociativa.

Aportaciones

La explotación agrícola estará constituida por las aportaciones efectuadas por cada una de las partes según el Exponendo primero, cuya valoración y participación en la explosión final quedan valoradas en la siguiente proporción:

Parte A % Capital aportado: [IMPORTE] euros

Parte B % Capital aportado: [IMPORTE] euros

Parte C % Capital aportado: [IMPORTE] euros

Normas de funcionamiento interno de la explotación

Las Partes acuerdan adoptar las normas de funcionamiento interno de la explotación que se adjuntan como Anexo II.

Organización y gestión

Las Partes acuerdan ser responsables, respectivamente, de proveer u organizar los siguientes servicios técnicos o comerciales dentro del alcance de las actividades de la explotación:

Los costes del personal de apoyo que realice trabajos para la explotación serán asumidos por las partes en proporción a sus respectivas aportaciones.

Restricción a la transmisibilidad

Una Parte no cederá, pignorará o de cualquier forma transmitirá los derechos sobre la totalidad o parte de su participación en la explotación sin la aprobación unánime por escrito de las demás.

Si las Partes aprueban la cesión, ésta estará sujeta a que el tercero acuerde incondicionalmente por escrito adherirse a todos los términos del presente Acuerdo.

Garantías personales

Las Partes no estarán obligadas a otorgar garantías por ningún préstamo concedido a la explotación. Si ellas acuerdan hacerlo, dichas garantías serán otorgadas en la misma proporción a sus respectivas aportaciones. Las obligaciones de las Partes bajo cualesquiera de dichas garantías serán (en la medida de lo posible) individuales, y, si una reclamación es hecha bajo una de dichas garantías contra una Parte, esa Parte tendrá derecho a recibir aportes de las otras Partes en cantidades tales que aseguren que la obligación total bajo esa garantía sea asumida por las Partes en proporción a su participación.

Extinción

Causas de la terminación

El contrato de aparcería asociativa terminará mediante acuerdo unánime de las Partes, por cumplimiento de los objetivos inicialmente propuestos o por haber devenido estos imposibles de cumplir.

Consecuencias de la extinción

A la terminación del contrato de aparcería asociativa las Partes tomarán todas las medidas necesarias para liquidar la explotación y para distribuir o vender sus activos. En particular, las Partes adoptarán las siguientes medidas:

a) Terminar todas las relaciones legales de la explotación con terceros;

b) Vender los activos de la explotación adquiridos por la explotación al mejor precio posible;

c) Liquidar las deudas de la explotación;

e) Al final de la liquidación, distribuir cualquier remanente en efectivo a las Partes de conformidad con sus aportaciones.

Confidencialidad

Las Partes se obligan a no revelar, ceder o transferir a terceros ninguna información referente a los negocios, clientes, operaciones, instalaciones, cuentas o finanzas de las demás, ni sus procedimientos, métodos, transacciones, "know-how", o cualquier otro aspecto relacionado con sus actividades que pudieran conocer o hayan conocido con motivo del presente contrato.

Derechos de propiedad intelectual e industrial

A la terminación del contrato de aparcería, cada Parte tendrá el derecho no-exclusivo para usar cualquier derecho de Propiedad Intelectual o Industrial que pudiera corresponder por razón de la explotación.

Cualquier explotación comercial de tales derechos por licencia o cesión a un tercero, requerirá, sin embargo, de la aprobación de todas las Partes.

Buena fe y deber de promover el interés de la explotación

Cada Parte usará todos los esfuerzos razonables para promover los mejores intereses de la explotación y para consultarse íntegramente sobre todos los asuntos que afecten sustancialmente el desarrollo de los negocios de la misma.

Cuando se requiera el consentimiento o la aprobación de una Parte bajo este Acuerdo o en el curso de la explotación, dicho consentimiento o aprobación no serán retenidos sin una justificación razonable.

Cada parte actuará de buena fe hacia las otras Partes y hacia la explotación con el fin de dar cumplimiento al espíritu de este Acuerdo, así como para promover el éxito del contrato de aparcería asociativa.

Gastos e impuestos

Todos los gastos e impuestos que se originen como consecuencia de la formalización, cumplimiento o extinción del presente contrato y de las obligaciones que de él se deriven serán de cargo de la parte

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

Y en prueba de conformidad y aceptación de cuanto antecede, ambas partes firman los [Nº] folios del presente CONTRATO DE APARCERÍA ASOCIATIVA extendido por duplicado y a un solo efecto, en la ciudad y fecha mencionados en el encabezamiento.

Fdo. Don [NOMBRE Y APELLIDOS]

()

Fdo. Don [NOMBRE Y APELLIDOS]

()

========================================================================
