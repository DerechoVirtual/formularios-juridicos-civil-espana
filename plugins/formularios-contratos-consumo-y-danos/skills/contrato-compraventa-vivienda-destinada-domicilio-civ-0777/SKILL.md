---
name: contrato-compraventa-vivienda-destinada-domicilio-civ-0777
description: "Contrato de compraventa de vivienda destinada a domicilio familiar. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de compraventa de vivienda destinada a domicilio familiar

> Formulario **CIV-0777** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de compraventa de vivienda destinada a domicilio familiar» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de compraventa de vivienda destinada a domicilio familiar” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:contrato-compraventa-vivienda-destinada-domicilio-civ-0777`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (6 veces)
- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] Nº (5 veces)
- [ ] NÚMERO (4 veces)
- [ ] AÑO (3 veces)
- [ ] DÍA (3 veces)
- [ ] MES (3 veces)
- [ ] CALLE (2 veces)
- [ ] DNI/NIE (2 veces)
- [ ] ESTADO CIVIL (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] FINCA
- [ ] FOLIO
- [ ] LIBRO
- [ ] LUGAR
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

PRIMERO Que EL VENDEDOR es propietaria en régimen de plena propiedad y dominio del inmueble sito en [LOCALIDAD], calle [CALLE] número [NÚMERO] con una superficie de [Nº] metros cuadrados.

Cuota de % en el valor del bloque donde está ubicado la citada vivienda y elementos comunes.

Título: Adquirido por [TÍTULO DE ADQUISICIÓN] efectuada en virtud de escritura pública otorgada ante el Notario de [LOCALIDAD], D. el día [DÍA] de [MES] de [AÑO] número protocolo

Inscripción: Está inscrita en el Registro de la Propiedad número [NÚMERO] de [LOCALIDAD] en el tomo [TOMO], libro [LIBRO] folio [FOLIO], finca [FINCA]

Referencia catastral: según consta en la referencia del último recibo del Impuestos sobre bienes Inmuebles que queda unido a este documento por copia.

Cargas: La referida finca se encuentra libre de cargas y gravámenes, según nota simple expedida por el Registro de la Propiedad el día de hoy, y que se une a este documento

Arrendamientos: La referida finca no se encuentra arrendada y está libre de ocupantes e inquilinos.

Gastos de Comunidad: El inmueble se encuentra al corriente en el pago de los gastos de comunidad de propietarios del edificio al que la finca pertenece, de acuerdo con el certificado expedido por la administración del Inmueble que queda unido a este documento.

Régimen de Comunidad: Se rige por lo dispuesto en los Estatutos de la Comunidad de Propietarios autorizados en virtud de escritura pública otorgada ante el Notario de [LOCALIDAD] D. el día [DÍA] de [MES] de [AÑO] y que EL COMPRADOR declara conocer, así como por lo dispuesto en la Ley de Propiedad Horizontal.

SEGUNDO Que el COMPRADOR, tiene dos hijos menores con D/Dª [NOMBRE Y APELLIDOS], y necesitan ocupar una vivienda en la localidad donde se encuentra ubicado el inmueble supradescrito, para establecer su domicilio conyugal.

TERCERO Que habida cuenta de que el VENDEDOR conviene en vender al COMPRADOR la vivienda objeto del presente contrato, las partes deciden llevar a efecto su acuerdo con arreglo a las siguientes,

ESTIPULACIONES

Objeto

Constituye el objeto del presente contrato la compraventa del inmueble descrito en el Exponendo Primero, con cuanto sea inherente o accesorio.

El COMPRADOR declara que la vivienda será destinada, exclusivamente, a su utilización como domicilio conyugal, estableciendo en ella su residencia habitual y permanente.

Fruto de ello resultará de aplicación la normativa del Código Civil relativa a las viviendas familiares, pese a que se trata de un bien privativo del COMPRADOR.

[ELEGIR UNA OPCIÓN: Entrega / En el momento del contrato / Entrega / Entrega en el otorgamiento de la escritura pública]

Precio

Las partes acuerdan que el precio de la vivienda ascienda a [IMPORTE] euros.

[ELEGIR UNA OPCIÓN: Forma de pago / En el momento de la firma / Forma de pago / Pago aplazado]

Elevacion a escritura pública

Las partes acuerdan otorgar la correspondiente escritura pública de compraventa, en un plazo máximo de [Nº] días, en la Notaría que el COMPRADOR decida.

El COMPRADOR deberá comunicar al VENDEDOR con una antelación mínima de [Nº] días, la fecha, la hora y el lugar donde se llevara a cabo la elevación a escritura pública del presente contrato de compraventa.

Los gastos e impuestos que se deriven del otorgamiento de escritura pública de compraventa, serán abonados por el COMPRADOR, salvo la plusvalía municipal, que será liquidada por el VENDEDOR.

A la fecha de otorgamiento de la escritura pública de compraventa, la vivienda deberá encontrarse libre de cargas, al corriente de todos los gastos (comunidad de propietarios, impuestos y tasas municipales,…), y sin inquilinos.

Una vez que se eleve a público el contrato de compraventa, todos los gastos que se generen serán de cuenta del COMPRADOR, salvo aquellos que procedan de la comunidad de propietarios del edificio donde se encuentra la vivienda, y se hayan aprobado con anterioridad a la compraventa (derramas).

Resolución del contrato

El Contrato podrá resolverse por las siguientes causas:

1. Por voluntad de cualquiera de las partes cuando medie incumplimiento grave de las obligaciones pactadas.

2. Por acuerdo de las partes por escrito.

En cualquier caso, la parte que pretenda resolver el presente contrato alegando incumplimiento de la contraparte, deberá requerirle al cumplimiento de la obligación de forma fehaciente, otorgándole un plazo de [Nº] días a la parte incumplidora, para que pueda subsanar dicho incumplimiento.

Transcurrido el citado plazo sin que los incumplimientos hubiesen sido subsanados, el perjudicado podrá ejercitar la mencionada facultad.

Cláusula penal

En caso de resolución del contrato por causa imputable al COMPRADOR, el VENDEDOR no estará obligado a la devolución de las cantidades satisfechas hasta ese momento, cantidades que se considerarán indemnización por daños y perjuicios, fijándose además una suma adicional de [IMPORTE] €, como indemnización que el COMPRADOR deberá abonar al VENDEDOR.

La resolución del contrato legitimará al VENDEDOR a tomar plena posesión del inmueble por sus propios medios, sin necesidad de previa declaración judicial, ni de autoridad alguna, renunciando el COMPRADOR de modo expreso a oponerse de modo alguno a la actuación en este sentido del VENDEDOR.

En el supuesto de que la resolución contractual sea culpa del VENDEDOR, éste deberá devolver al COMPRADOR el doble de las cantidades percibidas hasta ese momento, suma que comprende la indemnización por daños y perjuicios como consecuencia del incumplimiento contractual.

[ELEGIR UNA OPCIÓN: Jurisdicción competente y ley aplicable / Jurisdicción a Tribunales sin cláusula penal en caso de no ejecución voluntaria de la sentencia / Sumisión a Tribunales con cláusula penal en caso de no ejecución voluntaria de la sentencia / — y además elegir: Sumisión a arbitraje / Sin cláusula penal en caso de no ejecución voluntaria del laudo / Arbitraje / Con cláusula penal en caso de no ejecución voluntaria del laudo]

Notificaciones

Toda notificación que se efectúe entre las partes se hará por escrito, y será entregada personalmente, o de cualquier otra forma que certifique la recepción por la parte notificada, en los respectivos domicilios indicados en el encabezamiento de este Contrato.

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata, y por un medio que garantice la recepción del mensaje.

Generalidades

El presente contrato anula y reemplaza cualquier contrato o acuerdo anterior entre las partes con el mismo objeto y sólo podrá ser modificado por un nuevo acuerdo firmado por ambas partes.

Si alguna de las cláusulas del presente contrato fuere declarada nula o inaplicable, dicha cláusula se considerará excluida del contrato, sin que implique la nulidad del mismo. En este caso las partes harán cuanto esté a su alcance para encontrar una solución equivalente que sea válida y que refleje debidamente sus intenciones.

Los encabezamientos de las distintas cláusulas lo son sólo a efectos informativos, y no afectarán, calificarán o ampliarán la interpretación de este Contrato.

Las partes, en la representación con la que intervienen en este acuerdo, una vez leído, aceptan respetar y cumplir formalmente todas las condiciones y compromisos recogidos en el mismo, y en prueba de conformidad con su íntegro contenido, firman por duplicado este documento, extendido en [Nº] folios de papel común cumplimentados por una sola cara, a un sólo efecto, en el lugar y fecha indicados en el encabezamiento.

Fdo. D/Dª [NOMBRE Y APELLIDOS]

(El VENDEDOR)

Fdo. Dª/D [NOMBRE Y APELLIDOS]

(El COMPRADOR)

========================================================================
