---
name: escritura-aportacion-bien-sociedad-gananciales-civ-0133
description: "Escritura de aportación de un bien a la sociedad de gananciales. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escritura de aportación de un bien a la sociedad de gananciales

> Formulario **CIV-0133** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Escritura pública por la que uno de los cónyuges, casados en régimen de gananciales, aporta a la sociedad de gananciales un inmueble de su propiedad privativa (en este modelo, la vivienda familiar), con atribución de carácter ganancial y sin asignación de cuotas, con la finalidad de contribuir a las cargas del matrimonio.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escritura de aportación de un bien a la sociedad de gananciales» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escritura de aportación de un bien a la sociedad de gananciales” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:escritura-aportacion-bien-sociedad-gananciales-civ-0133`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (5 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] NÚMERO (4 veces)
- [ ] AÑO (2 veces)
- [ ] DNI/NIE (2 veces)
- [ ] DÍA (2 veces)
- [ ] IMPORTE EN LETRA (2 veces)
- [ ] MES (2 veces)
- [ ] NOMBRE DEL NOTARIO (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL CÓNYUGE APORTANTE (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL OTRO CÓNYUGE (2 veces)
- [ ] Nº DE FINCA (2 veces)
- [ ] ARANCEL APLICABLE
- [ ] BASES DE CÁLCULO
- [ ] COLEGIO NOTARIAL
- [ ] DOMICILIO
- [ ] FOLIO
- [ ] LIBRO
- [ ] NOMBRE Y APELLIDOS DEL PRIMER CÓNYUGE
- [ ] NOMBRE Y APELLIDOS DEL SEGUNDO CÓNYUGE
- [ ] Nº
- [ ] Nº DE INSCRIPCIÓN
- [ ] Nº DE PROTOCOLO
- [ ] TOMO

## Normas que cita el formulario

- art. 1.323 Código Civil

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

- Junto a «…to y a la doctrina de la sentencia del Tribunal Supremo de 2 de octubre de 2001.»: comprobar el apartado exacto del art. 45.I.B) del texto refundido (RDLeg 1/1993) que recoge la exención de las aportaciones a la sociedad conyugal y que la doctrina citada sigue vigente.

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

NÚMERO [Nº DE PROTOCOLO]

ESCRITURA DE APORTACIÓN A LA SOCIEDAD DE GANANCIALES

En [LOCALIDAD], mi residencia, a [DÍA] de [MES] de [AÑO].

Ante mí, [NOMBRE DEL NOTARIO], Notario del Ilustre Colegio Notarial de [COLEGIO NOTARIAL],

COMPARECEN

Los consortes D./Dña. [NOMBRE Y APELLIDOS DEL PRIMER CÓNYUGE] y D./Dña. [NOMBRE Y APELLIDOS DEL SEGUNDO CÓNYUGE], mayores de edad, vecinos de [LOCALIDAD], con domicilio en [DOMICILIO], y con DNI/NIF [DNI/NIE] y [DNI/NIE], respectivamente.

Declaran que su régimen económico matrimonial es el legal de la sociedad de gananciales.

Les identifico con los documentos reseñados, que compruebo tienen la fotografía y firma coincidentes con las de sus titulares.

Sus datos resultan de la documentación que me exhiben y de sus manifestaciones.

INTERVIENEN en su propio nombre y derecho.

Les juzgo con capacidad legal suficiente para este acto y, al efecto,

DICEN

PRIMERO.- D./Dña. [NOMBRE Y APELLIDOS DEL CÓNYUGE APORTANTE], que es propietario/a, con carácter privativo, del pleno dominio de la siguiente finca:

DESCRIPCIÓN.- [DESCRIPCIÓN DE LA FINCA: DENOMINACIÓN, SITUACIÓN, CALLE Y NÚMERO, PLANTA, SUPERFICIE, LINDEROS, CUOTA DE PARTICIPACIÓN EN ELEMENTOS COMUNES, ETC.]. Se valora dicha finca en la cantidad de [IMPORTE EN LETRA] EUROS ([IMPORTE] €).

INSCRIPCIÓN.- Inscrita en el Registro de la Propiedad de [LOCALIDAD], al tomo [TOMO], libro [LIBRO], folio [FOLIO], finca número [Nº DE FINCA].

TÍTULO.- Le pertenece a dicho/a señor/a, con carácter privativo, por el título de [ELEGIR: compraventa / otro título que proceda], formalizada mediante escritura autorizada el día [DÍA] de [MES] de [AÑO] por D./Dña. [NOMBRE DEL NOTARIO], Notario/a de [LOCALIDAD], la cual causó la inscripción [Nº DE INSCRIPCIÓN] de la citada finca registral número [Nº DE FINCA].

REFERENCIA CATASTRAL.- Los comparecientes manifiestan que los datos catastrales referentes a la finca objeto de esta escritura se hallan reflejados en el certificado catastral telemático descriptivo y gráfico, que dejo unido a la presente. A instancia de los exponentes, hago constar yo, el Notario, que dejo incorporado el certificado por mí obtenido por medios telemáticos, en cumplimiento de lo dispuesto en el art. 170 del Reglamento Notarial y en el art. 3.2 del texto refundido de la Ley del Catastro Inmobiliario (Real Decreto Legislativo 1/2004). Habiéndose cumplido la obligación de aportar la referencia catastral, les hago saber que no será preciso hacer la correspondiente declaración de alteración catastral ante el Catastro.

CARGAS Y ARRIENDOS.- Libre de unas y otros, así como al corriente en el pago de los gastos de comunidad.

IMPUESTO SOBRE BIENES INMUEBLES.- A los efectos del art. 64 del texto refundido de la Ley Reguladora de las Haciendas Locales, hacen constar los comparecientes que el inmueble está al corriente del pago del Impuesto sobre Bienes Inmuebles. Advierto a los comparecientes que los bienes inmuebles quedan afectos al pago de toda cuota tributaria pendiente y me eximen de solicitar previa información sobre las deudas pendientes que por tal impuesto afecten al inmueble.

INFORMACIÓN REGISTRAL.- A los efectos del contenido del art. 175 del Reglamento Notarial, yo, el Notario, hago constar que [ELEGIR: he accedido por vía telemática a los asientos registrales de la finca descrita / por imposibilidad técnica no he podido acceder por vía telemática a los asientos registrales de la finca descrita, por lo que, conforme establece el apartado 4.º de dicho art. 175 del Reglamento Notarial, he solicitado del Registro de la Propiedad información registral por otro medio, obtenida de dicho Registro, alusiva a la finca descrita, en la que constan todas las circunstancias de petición e información adecuadas]. Hago la advertencia expresa a los otorgantes de que prevalece sobre la manifestación de los comparecientes la situación registral existente con anterioridad a la presentación en el Registro de la Propiedad de la copia autorizada o telemática de esta escritura. La descripción del inmueble, su titularidad y situación de cargas, en la forma expresada en los párrafos anteriores, resulta de las manifestaciones del aportante, del título de propiedad que me exhibe y de la nota simple del Registro de la Propiedad que yo, el Notario, tengo a la vista e incorporo a la presente como parte integrante de la misma.

VALOR a efectos de la aportación: [IMPORTE EN LETRA] EUROS ([IMPORTE] €).

SEGUNDO.- Expuesto cuanto antecede, formalizan el siguiente

CONTRATO

D./Dña. [NOMBRE Y APELLIDOS DEL CÓNYUGE APORTANTE], de conformidad con lo previsto en el art. 1.323 del Código Civil, por tratarse del domicilio conyugal y familiar, con la calidad de afección a todos los efectos económico-matrimoniales, APORTA A SU SOCIEDAD CONYUGAL con D./Dña. [NOMBRE Y APELLIDOS DEL OTRO CÓNYUGE] el pleno dominio de la finca descrita en el antecedente primero de esta escritura, con todos cuantos usos, derechos y servidumbres le sean inherentes, que quedan con carácter ganancial para ambos cónyuges y sin atribución de cuotas.

D./Dña. [NOMBRE Y APELLIDOS DEL OTRO CÓNYUGE] ACEPTA Y CONSIENTE la aportación a la sociedad de gananciales.

Esta aportación se hace con la finalidad exclusiva de contribuir a las cargas del matrimonio.

Aseveran los citados esposos que tendrán en cuenta la aportación aquí realizada al momento de liquidarse su sociedad conyugal.

SOLICITUD FISCAL.- Los otorgantes solicitan la exención del Impuesto sobre Transmisiones Patrimoniales y Actos Jurídicos Documentados con arreglo al art. 45.I.B).12 del texto refundido del Impuesto y a la doctrina de la sentencia del Tribunal Supremo de 2 de octubre de 2001.

Los comparecientes ACEPTAN Y APRUEBAN esta escritura y sus efectos.

Hago las reservas y advertencias legales oportunas, en especial, y a efectos fiscales, advierto de las obligaciones y responsabilidades tributarias que incumben a las partes en su aspecto material, formal y sancionador, y de las consecuencias de toda índole que se derivarían de la inexactitud de sus declaraciones, especialmente las del art. 14.7 del texto refundido de la Ley del Impuesto sobre Transmisiones Patrimoniales y Actos Jurídicos Documentados, de la afección de los bienes al pago de dicho impuesto, la obligación de presentación a autoliquidación en el plazo de treinta días hábiles y las responsabilidades en caso de incumplimiento. También advierto de las obligaciones tributarias materiales y formales que se deriven de la transmisión en relación con el Impuesto sobre el Incremento de Valor de los Terrenos de Naturaleza Urbana.

PROTECCIÓN DE DATOS.- Respecto a los datos personales recogidos en el presente documento, debe tenerse en cuenta que el tratamiento de los mismos se ajustará al Reglamento (UE) 2016/679, de 27 de abril (RGPD), y a la Ley Orgánica 3/2018, de 5 de diciembre, de Protección de Datos Personales y garantía de los derechos digitales, y que el interesado podrá ejercitar sus derechos de acceso, rectificación, supresión, portabilidad, oposición y limitación del tratamiento de los datos en los términos establecidos en los arts. 12 a 23 del citado Reglamento y en los arts. 12 a 18 de la citada Ley Orgánica.

OTORGAMIENTO Y AUTORIZACIÓN

Les hice de palabra las demás reservas y advertencias legales, así como que los datos recabados para la redacción de esta escritura y su facturación y seguimiento posterior forman parte de los ficheros existentes en la Notaría, utilizándose para las remisiones posteriores de obligado cumplimiento legal. Los datos serán tratados y protegidos según la legislación notarial, el Reglamento (UE) 2016/679 y la Ley Orgánica 3/2018, pudiendo su titular ejercer los derechos reconocidos en dichas normas. Les advertí del derecho que tienen a leer esta escritura por sí mismos, del que [ELEGIR: usaron / no usaron], haciéndolo además yo, el Notario, íntegramente y en alta voz, prestando su consentimiento los comparecientes, que firman conmigo. Y yo, el Notario, DOY FE de que el consentimiento ha sido libremente prestado y de que el otorgamiento se adecua a la legalidad y a la voluntad debidamente informada de los otorgantes, y de todo lo demás contenido en este instrumento público, extendido sobre [NÚMERO] folios de papel de uso exclusivamente notarial, el presente y los [NÚMERO] anteriores en orden correlativo, de la misma serie. Están las firmas de los comparecientes y mi sello, signo, firma y rúbrica.

DOCUMENTOS UNIDOS: [RELACIÓN DE DOCUMENTOS UNIDOS: TESTIMONIO DE CERTIFICACIONES DEL CATASTRO, RECIBOS DEL IBI, NOTA SIMPLE, ETC.]

SIGUEN LAS FIRMAS DE LOS COMPARECIENTES. SIGNADO, RUBRICADO Y FIRMADO POR MÍ. ESTÁ EL SELLO DE MI NOTARÍA.

APLICACIÓN DE ARANCEL. DISPOSICIÓN ADICIONAL 3.ª DE LA LEY 8/1989. BASES DE CÁLCULO: [BASES DE CÁLCULO]

ARANCEL APLICABLE: [ARANCEL APLICABLE]

DERECHOS ARANCELARIOS sin IVA: [IMPORTE] euros; cuota de IVA: [IMPORTE] euros; total factura: [IMPORTE] euros.

ES PRIMERA COPIA LITERAL de su matriz con la que concuerda fielmente y donde queda anotada. La expido a instancias de D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS], en [NÚMERO] folios de papel exclusivo para documentos notariales, números [Nº] y los [NÚMERO] siguientes, el mismo día de su autorización. DOY FE.
