---
name: contrato-cesion-uso-precario-civ-0665
description: "Contrato de cesión de uso en precario. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de cesión de uso en precario

> Formulario **CIV-0665** del plugin **Propiedad, posesión, servidumbres e hipotecas** (`formularios-propiedad-y-derechos-reales`) · Civil › Propiedad y derechos reales · normativa revisada el 24-11-2026.

## Qué es

Contrato de precario de un inmueble: el propietario cede gratuitamente el uso de una vivienda a un familiar, sin plazo determinado y con facultad de recuperarla cuando lo desee, con obligaciones de conservación y gastos a cargo del precarista. Incluye alternativas de sumisión a tribunales o a arbitraje, con o sin cláusula penal (formulario adaptado a la reforma de la LO 1/2025).

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de cesión de uso en precario» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de cesión de uso en precario” para mi caso». También puedes invocarla directamente con `/formularios-propiedad-y-derechos-reales:contrato-cesion-uso-precario-civ-0665`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-propiedad-y-derechos-reales:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Propiedad, posesión, servidumbres e hipotecas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (12 veces)
- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] NÚMERO (6 veces)
- [ ] NOMBRE DEL NOTARIO (4 veces)
- [ ] AÑO (3 veces)
- [ ] DÍA (3 veces)
- [ ] MES (3 veces)
- [ ] Nº DE PROTOCOLO (3 veces)
- [ ] CALLE (2 veces)
- [ ] DNI/NIE (2 veces)
- [ ] FECHA (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] IMPORTE EN LETRA (2 veces)
- [ ] INSTITUCIÓN ARBITRAL (2 veces)
- [ ] NOMBRE Y APELLIDOS O DENOMINACIÓN SOCIAL (2 veces)
- [ ] SEDE (2 veces)
- [ ] CALLE/AVENIDA
- [ ] DATOS REGISTRALES
- [ ] FOLIO
- [ ] LIBRO
- [ ] Nº
- [ ] Nº DE FINCA
- [ ] PARENTESCO
- [ ] PORCENTAJE
- [ ] REFERENCIA CATASTRAL
- [ ] SUPERFICIE
- [ ] TOMO

## Normas que cita el formulario

- art. 34 Ley 60/2003
- art. 1750 Código Civil
- art. 1750 CC

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

CONTRATO DE PRECARIO DE INMUEBLE

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO]

REUNIDOS

De una parte:

D./Dª [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero/a / casado/a / divorciado/a / separado/a / viudo/a], vecino/a de [LOCALIDAD], con domicilio en C/ [CALLE], nº [NÚMERO], y portador/a de DNI [DNI/NIE].

De otra:

D./Dª [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero/a / casado/a / divorciado/a / separado/a / viudo/a], con domicilio en [CALLE/AVENIDA] nº [NÚMERO] y portador/a de DNI número [DNI/NIE].

INTERVIENEN

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— En nombre y representación de otra persona:

D./Dª [NOMBRE Y APELLIDOS], en nombre y representación de [NOMBRE Y APELLIDOS O DENOMINACIÓN SOCIAL], en lo sucesivo «LA PROPIEDAD», en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D. [NOMBRE DEL NOTARIO], en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO].

D./Dª [NOMBRE Y APELLIDOS], en nombre y representación de [NOMBRE Y APELLIDOS O DENOMINACIÓN SOCIAL], en lo sucesivo «EL PRECARISTA», en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D. [NOMBRE DEL NOTARIO], en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO].

Todas las partes, en el respectivo carácter con el que intervienen, se reconocen mutuamente la capacidad legal en Derecho necesaria para concertar el presente CONTRATO DE PRECARIO DE INMUEBLE, y a tal efecto, libremente y de común acuerdo,

— En su propio nombre y derecho:

D./Dª [NOMBRE Y APELLIDOS], en su propio nombre y derecho, en lo sucesivo «LA PROPIEDAD».

D./Dª [NOMBRE Y APELLIDOS], en su propio nombre y derecho, en lo sucesivo «EL PRECARISTA».

Todas las partes, en el respectivo carácter con el que intervienen, se reconocen mutuamente la capacidad legal en Derecho necesaria para concertar el presente CONTRATO DE PRECARIO DE INMUEBLE, y a tal efecto, libremente y de común acuerdo,

EXPONEN

Primero.– Que la PROPIEDAD es propietaria, en régimen de plena propiedad y dominio, del inmueble sito en [LOCALIDAD], calle [CALLE] número [NÚMERO], con una superficie de [SUPERFICIE] metros cuadrados.

Cuota de [PORCENTAJE] % en el valor del bloque donde está ubicada la citada vivienda y elementos comunes.

Título: adquirido por [TÍTULO: compraventa / herencia / donación...], efectuada en virtud de escritura pública otorgada ante el Notario de [LOCALIDAD] D. [NOMBRE DEL NOTARIO] el día [DÍA] de [MES] de [AÑO], número de protocolo [Nº DE PROTOCOLO].

Inscripción: está inscrita en el Registro de la Propiedad número [Nº] de [LOCALIDAD], en el tomo [TOMO], libro [LIBRO], folio [FOLIO], finca [Nº DE FINCA] [DATOS REGISTRALES].

Referencia catastral: [REFERENCIA CATASTRAL], según consta en la referencia del último recibo del Impuesto sobre Bienes Inmuebles, que queda unido a este documento por copia.

Cargas: la referida finca se encuentra libre de cargas y gravámenes, según nota simple expedida por el Registro de la Propiedad el día de hoy, y que se une a este documento.

Arrendamientos: la referida finca no se encuentra arrendada y está libre de ocupantes e inquilinos.

Gastos de Comunidad: el inmueble se encuentra al corriente en el pago de los gastos de comunidad de propietarios del edificio al que la finca pertenece, de acuerdo con el certificado expedido por la administración del inmueble que queda unido a este documento.

Régimen de Comunidad: se rige por lo dispuesto en los Estatutos de la Comunidad de Propietarios autorizados en virtud de escritura pública otorgada ante el Notario de [LOCALIDAD] D. [NOMBRE DEL NOTARIO] el día [DÍA] de [MES] de [AÑO], y que el PRECARISTA declara conocer, así como por lo dispuesto en la Ley de Propiedad Horizontal.

Segundo.– Que el PRECARISTA, [PARENTESCO CON LA PROPIEDAD, p. ej. nieto/a], necesita ocupar una vivienda en la localidad donde se encuentra ubicado el inmueble que ha sido descrito, como consecuencia de [MOTIVO: p. ej., su próximo enlace matrimonial / inicio de convivencia more uxorio].

Tercero.– Que, habida cuenta de que la PROPIEDAD no necesita ocupar su vivienda, y fruto de la relación familiar que une a ambas partes, es voluntad de la misma ceder gratuitamente al PRECARISTA el uso de dicha vivienda, por medio del presente documento, lo que llevan a efecto con arreglo a las siguientes

CLÁUSULAS

Objeto.– Constituye el objeto del presente contrato la cesión gratuita del uso de la vivienda supradescrita, de la PROPIEDAD al PRECARISTA, quien acepta en su favor la referida cesión, en concepto de precario.

El PRECARISTA manifiesta que va a establecer en la referida vivienda su domicilio habitual y permanente en esta ciudad, que es el objetivo perseguido con la firma del presente contrato.

La vivienda se encuentra en perfecto estado de uso y conservación, y en disposición de servir al fin indicado.

Se acompaña como Anexo I del presente contrato un inventario donde se describen los muebles que se hallan en la vivienda.

La cesión de uso se hace de manera gratuita, habida cuenta de la relación familiar que une a las partes, siendo el PRECARISTA [PARENTESCO] de la PROPIEDAD.

El presente contrato no genera ningún otro derecho para las partes que el que expresamente ha sido recogido en la presente estipulación.

Obligaciones de los precaristas.– En virtud del presente contrato, el PRECARISTA se obliga a:

1. Conservar debidamente la vivienda, instalaciones, ajuar y servicios, siendo de su cuenta y cargo las reparaciones que sean necesarias a tal fin.

2. Utilizar la vivienda como domicilio habitual y permanente, no pudiendo modificar su uso y causa de ocupación.

3. No alquilar la vivienda, ni cederla, ya sea total o parcialmente.

4. No realizar obras sin el previo consentimiento, por escrito, de la PROPIEDAD.

5. Respetar las normas de la Comunidad y los Estatutos del edificio donde se halla la vivienda.

6. Informar a la PROPIEDAD, de manera inmediata, de cualquier problema que pudiera afectar al inmueble.

Gastos.– Serán de cuenta del PRECARISTA los gastos que se produzcan por los consumos individuales de agua, luz, gas, teléfono y cuantos otros se lleguen a instalar en la vivienda.

No obstante, la liquidación de los referidos gastos no podrá considerarse, de ninguna manera, como pago de una renta.

La PROPIEDAD seguirá haciéndose cargo de los gastos relativos a las cuotas de la comunidad de propietarios y de las derramas que pudieran acordarse.

Seguro.– El PRECARISTA contratará un seguro que resulte satisfactorio para la PROPIEDAD y que cubra el riesgo de daños o pérdida que pueda sufrir la vivienda durante todo el período de vigencia del presente contrato.

El PRECARISTA proporcionará a la PROPIEDAD, a su solicitud, pruebas de la existencia de dicho seguro. La cobertura incluirá, entre otros aspectos, los daños provocados por incendios, agua, fenómenos naturales y robo.

Duración del contrato.– Las partes no establecen un plazo concreto de duración del contrato, comprometiéndose el PRECARISTA a dejar libre la vivienda, siempre que la PROPIEDAD le comunique su voluntad de recuperar su uso, con al menos [PLAZO DE PREAVISO: dos meses] de antelación, para que éste pueda trasladar su domicilio habitual.

El PRECARISTA podrá, asimismo, dejar la vivienda libre cuando lo considere oportuno, obligándose a entregar las llaves a la PROPIEDAD el mismo día en que deje de usar la misma.

La terminación del presente contrato no devengará indemnización alguna para las partes.

Jurisdicción competente y ley aplicable.–

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— Sumisión a Tribunales sin cláusula penal en caso de no ejecución voluntaria de la sentencia.

Para cuantas cuestiones o divergencias pudieran suscitarse en relación con el presente contrato, ambas partes establecen someterse a los Tribunales de [LOCALIDAD], en [SEDE], renunciando expresamente a su fuero propio si lo tuvieran.

El presente contrato tiene carácter civil y se regirá por sus propias cláusulas y, en lo en ellas no dispuesto, por lo previsto en el Código Civil y demás leyes especiales.

— Sumisión a Tribunales con cláusula penal en caso de no ejecución voluntaria de la sentencia.

Para cuantas cuestiones o divergencias pudieran suscitarse en relación con el presente contrato, ambas partes establecen someterse a los Tribunales de [LOCALIDAD], en [SEDE], renunciando expresamente a su fuero propio si lo tuvieran.

En el caso de que la parte o partes que hubieran resultado condenadas en el fallo de la sentencia no cumplieran voluntariamente con el fallo de la sentencia en el plazo de [NÚMERO] días, deberán abonar a quien le hubiera vencido en el pleito la cantidad de [IMPORTE EN LETRA] euros ([IMPORTE] €), sin perjuicio de la indemnización por daños y perjuicios que pudiera corresponderles.

El presente contrato tiene carácter civil y se regirá por sus propias cláusulas y, en lo en ellas no dispuesto, por lo previsto en el Código Civil y demás leyes especiales.

Sumisión a arbitraje.–

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— Sin cláusula penal en caso de no ejecución voluntaria del laudo.

Para cuantas cuestiones o divergencias pudieran suscitarse en relación con el presente contrato, ambas partes establecen someterse al Arbitraje de Derecho de [INSTITUCIÓN ARBITRAL] de [LOCALIDAD]. Según el artículo 34 de la Ley 60/2003, de 23 de diciembre, de Arbitraje, los árbitros sólo decidirán en equidad si las partes les han autorizado expresamente para ello.

El presente contrato tiene carácter civil y se regirá por sus propias cláusulas y, en lo en ellas no dispuesto, por lo previsto en el Código Civil y demás leyes especiales.

— Con cláusula penal en caso de no ejecución voluntaria del laudo.

Para cuantas cuestiones o divergencias pudieran suscitarse en relación con el presente contrato, ambas partes establecen someterse al Arbitraje de Derecho de [INSTITUCIÓN ARBITRAL] de [LOCALIDAD]. Según el artículo 34 de la Ley 60/2003, de 23 de diciembre, de Arbitraje, los árbitros sólo decidirán en equidad si las partes les han autorizado expresamente para ello.

En el caso de que la parte o partes que hubieran resultado condenadas en el laudo no cumplieran voluntariamente con el fallo del mismo en el plazo de [NÚMERO] días, deberán abonar a quien le hubiera vencido en el pleito la cantidad de [IMPORTE EN LETRA] euros ([IMPORTE] €), sin perjuicio de la indemnización por daños y perjuicios que pudiera corresponderles.

El presente contrato tiene carácter civil y se regirá por sus propias cláusulas y, en lo en ellas no dispuesto, por lo previsto en el Código Civil y demás leyes especiales.

Notificaciones.– Toda notificación que se efectúe entre las partes se hará por escrito, y será entregada personalmente o de cualquier otra forma que certifique la recepción por la parte notificada, en los respectivos domicilios indicados en el encabezamiento de este Contrato.

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

Generalidades.– El presente contrato anula y reemplaza cualquier contrato o acuerdo anterior entre las partes con el mismo objeto y sólo podrá ser modificado por un nuevo acuerdo firmado por ambas partes.

Si alguna de las cláusulas del presente contrato fuere declarada nula o inaplicable, dicha cláusula se considerará excluida del contrato, sin que implique la nulidad del mismo. En este caso las partes harán cuanto esté a su alcance para encontrar una solución equivalente que sea válida y que refleje debidamente sus intenciones.

Los encabezamientos de las distintas cláusulas lo son sólo a efectos informativos, y no afectarán, calificarán o ampliarán la interpretación de este Contrato.

Las partes, en la representación con la que intervienen en este acuerdo, una vez leído, aceptan respetar y cumplir formalmente todas las condiciones y compromisos recogidos en el mismo y, en prueba de conformidad con su íntegro contenido, firman por duplicado este documento, extendido en [NÚMERO] folios de papel común cumplimentados por una sola cara, a un solo efecto, en el lugar y fecha indicados en el encabezamiento.

La propiedad: Fdo. D./Dª [NOMBRE Y APELLIDOS]

El/la precarista: Fdo. D./Dª [NOMBRE Y APELLIDOS]

NOTAS DE USO

La figura del precario no aparece expresamente regulada en el Código Civil. La mayoría de los autores consideran que el artículo 1750 del Código Civil, referente al comodato, lo regula, puesto que el precario vendría a ser una variedad del comodato que se diferencia de éste en la indeterminación del periodo en el que se cede algo; o, dicho de otro modo, el cedente puede reclamar la devolución del bien cuando desee al precarista. La diferencia entre el contrato de comodato y el de precario es precisamente la indefinición del plazo de la cesión: en el comodato (art. 1750 CC) se establece un plazo de duración; en el precario, el cedente puede recuperar el bien cuando lo desee.

Sobre los intervinientes: si se trata de una persona física que interviene en su propio nombre y derecho, es preciso hacer constar tal extremo. Lo mismo sucede si interviene en representación de otra persona física o jurídica; en este caso será necesario describir la fuente de la que dimana su representación, ya sea legal o convencional. En el mismo sentido si se trata de una persona física que actúa en beneficio de una sociedad de gananciales, de una sociedad civil irregular o de una comunidad de bienes, puesto que en estos casos no existe una personalidad jurídica diferente de la de los miembros que la integran.

Artículo 250.1.2.º de la Ley de Enjuiciamiento Civil, relativo al ámbito del juicio verbal: la recuperación de una finca cedida en precario siempre se ventilará a través del juicio verbal.
