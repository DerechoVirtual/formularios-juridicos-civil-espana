---
name: escritura-cese-proindivision-adjudicacion-entre-civ-0134
description: "Escritura de cese de proindivisión y adjudicación entre cónyuges en separación de bienes. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escritura de cese de proindivisión y adjudicación entre cónyuges en separación de bienes

> Formulario **CIV-0134** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escritura de cese de proindivisión y adjudicación entre cónyuges en separación de bienes» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escritura de cese de proindivisión y adjudicación entre cónyuges en separación de bienes” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:escritura-cese-proindivision-adjudicacion-entre-civ-0134`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (12 veces)
- [ ] Nº (9 veces)
- [ ] LOCALIDAD (7 veces)
- [ ] NÚMERO (7 veces)
- [ ] AÑO (5 veces)
- [ ] DÍA (5 veces)
- [ ] MES (5 veces)
- [ ] IMPORTE (3 veces)
- [ ] Nº DE PROTOCOLO (2 veces)
- [ ] CALLE
- [ ] CIRCUNSTANCIAS PERSONALES
- [ ] ESCALERA
- [ ] FOLIO
- [ ] LIBRO
- [ ] LINDEROS
- [ ] PLANTA
- [ ] PORCENTAJE (CENTÉSIMAS)
- [ ] PORCENTAJE (ENTEROS)
- [ ] REFERENCIA CATASTRAL
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

OTORGANTES: Los consortes DON/DOÑA [NOMBRE Y APELLIDOS] y DON/DOÑA [NOMBRE Y APELLIDOS]

NUMERO [NÚMERO]

CESE DE PROINDIVISIÓN Y ADJUDICACIÓN

En [LOCALIDAD], mi residencia, a [DÍA] de [MES] de [AÑO]

Ante mí, Notario de ésta Capital y su Ilustre Colegio,

COMPARECEN:

Los consortes DON/DOÑA [NOMBRE Y APELLIDOS] y DON/DOÑA [NOMBRE Y APELLIDOS], [CIRCUNSTANCIAS PERSONALES]

El régimen económico de su matrimonio es el de absoluta separación de bienes, por haberlo pactado en capitulaciones matrimoniales formalizadas en escritura autorizada por el Notario de [LOCALIDAD], DON/DOÑA [NOMBRE Y APELLIDOS], el día [DÍA] de [MES] de [AÑO], con número de protocolo

Constan sus circunstancias personales de sus manifestaciones.

INTERVIENEN:

Ambos en su propio nombre y derecho.

IDENTIFICO a ambos comparecientes a través de sus reseñados documentos de identidad, que me exhiben y compruebo, y tienen, a mi juicio, según intervienen, capacidad legal necesaria para otorgar la presente escritura de CESE DE PROINDIVISIÓN Y ADJUDICACIÓN, a cuyo fin:

EXPONEN

Que contrajeron matrimonio en [LOCALIDAD] el día [DÍA] de [MES] de [AÑO], que se inscribió en el Registro Civil de [LOCALIDAD], al tomo n° [Nº], página n° [Nº] de la Sección 2ª.

Que mediante escritura autorizada por el Notario de [LOCALIDAD], DON/DOÑA [NOMBRE Y APELLIDOS], el día [DÍA] de [MES] de [AÑO], con número de protocolo [Nº DE PROTOCOLO], disolvieron y liquidaron su sociedad conyugal y pactaron el régimen de absoluta separación de bienes; capitulaciones debidamente indicadas en el Registro Civil de [LOCALIDAD], al tomo n° [Nº], página n° [Nº] de la Sección 2ª.

Que mediante escritura autorizada por mí el día [DÍA] de [MES] de [AÑO], con número de protocolo [Nº DE PROTOCOLO], los comparecientes celebraron una compraventa en cuya virtud adquirieron la propiedad de la vivienda que a continuación se describe por iguales partes:

URBANA.- ENTIDAD NUMERO [NÚMERO] DE ORDEN DE PROPIEDAD HORIZONTAL.- VIVIENDA CON ACCESO POR EL ZAGUÁN DE LA CALLE [CALLE] Vivienda en [PLANTA] planta, de la escalera [ESCALERA], señalada su puerta con el número [NÚMERO] Consta de diferentes habitaciones y servicios. Mide una superficie útil de [Nº] metros y [Nº] decímetros cuadrados, y construida con elementos comunes de [Nº] metros y [Nº] decímetros cuadrados. Linda, mirando desde la calle de su situación: frente [LINDEROS]; derecha entrando,; izquierda entrando,; y fondo,

Esta vivienda tiene vinculada, como anejo inseparable, la propiedad de una participación indivisa de [PORCENTAJE (ENTEROS)] enteros [PORCENTAJE (CENTÉSIMAS)] centésimas por ciento ( %) en el local en planta de sótano, a la que corresponde el uso privativo, exclusivo y excluyente, de una plaza de garaje, señalada con el número [NÚMERO], lo que representa un aumento en su superficie útil de [Nº] metros cuadrados.

CUOTA DE PARTICIPACIÓN.- por ciento.

SITUACIÓN ARRENDATICIA.- Libre de arrendatarios y ocupantes, según aseguran.

CARGAS.- Al margen afecciones fiscales, libre de cargas, gravámenes y arrendamientos y al corriente en el pago de impuestos, arbitrios y contribuciones, así como de gastos de comunidad.

REFERENCIA CATASTRAL.- [REFERENCIA CATASTRAL], según certificación registral telemática, fotocopia de la cual, extendida en papel común, uno a la presente matriz.

VALOR: [IMPORTE] EUROS ( €).

TÍTULO: El indicado.

INSCRIPCIÓN: Inscrita en el Registro de la Propiedad nº [NÚMERO] de [LOCALIDAD], tomo [TOMO], libro [LIBRO] folio [FOLIO], finca nº [NÚMERO]

Que, interesando a los comparecientes cesar en la proindivisión actualmente existente sobre la vivienda descrita en el expositivo anterior y, desmereciendo el inmueble por su división, han decidido adjudicarlo a DON/DOÑA [NOMBRE Y APELLIDOS] a calidad de que éste/a abone el exceso en dinero a DON/DOÑA [NOMBRE Y APELLIDOS], lo cual llevan a efecto, con arreglo a las siguientes

ESTIPULACIONES

Los consortes DON/DOÑA [NOMBRE Y APELLIDOS] y DON/DOÑA [NOMBRE Y APELLIDOS] cesan en el condominio de la finca descrita en el expositivo segundo y proceden a la adjudicación de la misma, valorada en [IMPORTE] EUROS ( €), a DON/DOÑA [NOMBRE Y APELLIDOS], que pasa a ser dueña de la totalidad de aquélla.

Existiendo una diferencia de valor en la adjudicación de [IMPORTE] ( €), DON/DOÑA [NOMBRE Y APELLIDOS] satisface en este acto a su esposo/a la citada cantidad, mediante cheque bancario nominativo cuyo importe, según manifiesta, ha sido cargado a la cuenta corriente nº [NÚMERO] abierta a su nombre, otorgándose carta de pago, a salvo buen fin del efecto. Incorporo a esta matriz la correspondiente fotocopia del original exhibido.

Exención Fiscal

Se hace constar expresamente que la presente extinción de comunidad y consiguiente adjudicación está exenta del Impuesto sobre Transmisiones Patrimoniales y Actos Jurídicos Documentados.

Gastos

Los gastos derivados del otorgamiento de esta escritura serán satisfechos con arreglo a ley.

Solicitan del Sr. Registrador de la Propiedad correspondiente, la inscripción de la presente extinción de comunidad y adjudicación consiguiente, realizada en los términos expuestos.

OTORGAMIENTO Y AUTORIZACIÓN

Así lo dicen y otorgan los comparecientes ante mí, después de hacerles las reservas y advertencias legales pertinentes, en especial, las siguientes:

- La relativa a la obligación de presentar autoliquidación dentro del plazo de treinta días hábiles, so pena de incurrir en posible responsabilidad.

- La obligación contenida en la Ley del Catastro de 5 de marzo de 2004, modificada por la Ley 36/2006, de Medidas para la Prevención del Fraude Fiscal

- Respecto a los datos personales recogidos en el presente documento, debe tenerse en cuenta que el tratamiento de los mismos se ajustará a la LO 3/2018, de 5 de diciembre, de Protección de Datos de Carácter Personal y Garantía de los Derechos Digitales, en desarrollo y aplicación del Reglamento UE 2016/679, de 27 de abril, y que el interesado podrá ejercitar sus derechos de acceso, rectificación, cancelación, supresión (derecho al olvido), portabilidad, oposición y limitación del tratamiento de los datos (ARCO-POL) en los términos establecidos en los arts. 12 a 23 y 12 a 18 de los citados Reglamento y Ley Orgánica, respectivamente.

Leo a los comparecientes esta escritura previa advertencia del derecho que para hacerlo por sí les asiste. Se ratifican, prestan su consentimiento y, en prueba de conformidad, la firman conmigo, que doy fe de lo contenido en este instrumento público.

SIGUEN LAS FIRMAS DE LOS COMPARECIENTES.- SIGNADO: - RUBRICADOS Y SELLADO.

APLICACION ARANCEL DISPOSICIÓN ADICIONAL 3 LEY 8/89. BASES DE CÁLCULO: ARANCEL APLICABLE NÚMEROS:

- DERECHOS ARANCELARIOS -

() euros.-

SIGUEN DOCUMENTOS UNIDOS

========================================================================
