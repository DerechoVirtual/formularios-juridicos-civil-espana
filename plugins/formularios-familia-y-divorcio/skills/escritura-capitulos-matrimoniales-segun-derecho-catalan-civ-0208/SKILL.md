---
name: escritura-capitulos-matrimoniales-segun-derecho-catalan-civ-0208
description: "Escritura de capítulos matrimoniales según el Derecho catalán. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escritura de capítulos matrimoniales según el Derecho catalán

> Formulario **CIV-0208** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Escritura notarial de capítulos matrimoniales en Cataluña por la que los cónyuges (o futuros cónyuges) pactan el régimen económico de su matrimonio, aquí el de comunidad de bienes, con relación de bienes privativos, administración, responsabilidad por deudas e inscripción en el Registro Civil. Pueden otorgarse antes o después del matrimonio.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escritura de capítulos matrimoniales según el Derecho catalán» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escritura de capítulos matrimoniales según el Derecho catalán” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:escritura-capitulos-matrimoniales-segun-derecho-catalan-civ-0208`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (8 veces)
- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] Nº (6 veces)
- [ ] AÑO (4 veces)
- [ ] DÍA (4 veces)
- [ ] MES (4 veces)
- [ ] NOMBRE DEL NOTARIO (3 veces)
- [ ] Nº DE PROTOCOLO (3 veces)
- [ ] CALLE (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] ENTIDAD (2 veces)
- [ ] ESTADO CIVIL (2 veces)
- [ ] FOLIO (2 veces)
- [ ] LIBRO (2 veces)
- [ ] NIF (2 veces)
- [ ] Nº DE CUENTA (2 veces)
- [ ] Nº DE FINCA (2 veces)
- [ ] PORCENTAJE (2 veces)
- [ ] REFERENCIA CATASTRAL (2 veces)
- [ ] SUPERFICIE (2 veces)
- [ ] TOMO (2 veces)
- [ ] VECINDAD CIVIL (2 veces)
- [ ] CLASE
- [ ] COLEGIO NOTARIAL
- [ ] DENOMINACIÓN SOCIAL
- [ ] MARCA
- [ ] MODELO
- [ ] NOMBRE Y APELLIDOS DEL COMPARECIENTE 1
- [ ] NOMBRE Y APELLIDOS DEL COMPARECIENTE 2
- [ ] Nº DE BASTIDOR
- [ ] Nº DE PLANTAS
- [ ] NÚMEROS
- [ ] SERIE

## Normas que cita el formulario

- art. 232 Ley 25/2010

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

### Avisos de actualización (3) — se aplican en el texto, nunca se copian en el documento

- Junto a «…ibro segundo del Código civil de Cataluña, relativo a la persona y a la familia.»: el original citaba «los artículos 232.30 y siguientes»; comprobar en el libro segundo del Código civil de Cataluña la numeración exacta del régimen de comunidad de bienes elegido y su redacción vigente.
- Junto a «…fidencial y reservado, y sin perjuicio de las remisiones autorizadas por la ley.»: el original citaba la Orden del Ministerio de Justicia 484/2003 y la Ley Orgánica 3/2018 (LOPDGDD) [NOTA DE REVISIÓN: La LO 15/1999 y su Reglamento (RD 1720/2007) fueron sustituidos por el Reglamento (UE) 2016/679 (RGPD) y la LO 3/2018, de 5 de diciembre (LOPDGDD). Fuente: LO 3/2018, disposición derogatoria única.], ambas desplazadas por el RGPD y la LOPDGDD; se ha adaptado la advertencia. Comprobar la cláusula informativa de protección de datos vigente en el protocolo de la notaría.
- Junto a «…ambos contrayentes tienen vecindad civil catalana, rige la separación de bienes.»: el original añadía que «a falta de capítulos rige el consorcio conyugal», lo que contradice la regla anterior (en Cataluña, a falta de pacto, rige la separación de bienes); se ha suprimido esa frase.

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

Número: [Nº DE PROTOCOLO]

En la ciudad de [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Ante mí, [NOMBRE DEL NOTARIO], Notario del Ilustre Colegio de [COLEGIO NOTARIAL],

COMPARECEN

De una parte, D./Dña. [NOMBRE Y APELLIDOS DEL COMPARECIENTE 1], mayor de edad, de estado civil [ESTADO CIVIL], con domicilio en [DOMICILIO], vecindad civil [VECINDAD CIVIL], y NIF número [NIF].

Y de la otra, D./Dña. [NOMBRE Y APELLIDOS DEL COMPARECIENTE 2], mayor de edad, de estado civil [ESTADO CIVIL], con domicilio en [DOMICILIO], vecindad civil [VECINDAD CIVIL], y NIF número [NIF].

INTERVIENEN

Ambos en su propio nombre y derecho. Me aseguro de su identidad por la exhibición de los reseñados documentos nacionales de identidad.

Y les juzgo, a mi juicio, con capacidad legal para el otorgamiento de esta escritura y, a tal efecto,

EXPONEN

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]
— Si se otorgan antes del matrimonio: ÚNICO.- Que tienen la intención de contraer matrimonio entre sí en próximas fechas, motivo por el que suscriben los presentes capítulos matrimoniales con arreglo a las siguientes
— Si se otorgan después del matrimonio: ÚNICO.- Que el día [DÍA] de [MES] de [AÑO] contrajeron matrimonio, inscrito en el Registro Civil de [LOCALIDAD], y que suscriben los presentes capítulos matrimoniales con arreglo a las siguientes

ESTIPULACIONES

Comparecientes

Los comparecientes acuerdan que al [ELEGIR: proyectado / celebrado] matrimonio se le aplique el régimen de comunidad de bienes regulado en los artículos 232-30 y siguientes de la Ley 25/2010, de 29 de julio, del libro segundo del Código civil de Cataluña, relativo a la persona y a la familia.

Bienes

Son bienes privativos de cada cónyuge, que continuarán ostentando dicha condición:

A) D./Dña. [NOMBRE Y APELLIDOS] es propietario/a en régimen de plena propiedad y dominio del inmueble sito en [LOCALIDAD], calle [CALLE], número [Nº], con una superficie de [SUPERFICIE] metros cuadrados, distribuidos en [Nº DE PLANTAS] plantas.

Cuota de [PORCENTAJE] % en el valor del bloque donde está ubicada la citada vivienda y elementos comunes.

Título: adquirido por [TÍTULO: compraventa / herencia / donación / otro], efectuada en virtud de escritura pública otorgada ante el Notario de [LOCALIDAD], D./Dña. [NOMBRE DEL NOTARIO], el día [DÍA] de [MES] de [AÑO], número [Nº DE PROTOCOLO] de su protocolo.

Inscripción: está inscrita en el Registro de la Propiedad número [Nº] de [LOCALIDAD], en el tomo [TOMO], libro [LIBRO], folio [FOLIO], finca [Nº DE FINCA].

Referencia catastral: [REFERENCIA CATASTRAL], según consta en la referencia del último recibo del Impuesto sobre Bienes Inmuebles.

Cargas: la referida finca se encuentra [ELEGIR: libre de cargas y gravámenes / gravada con las siguientes cargas: DESCRIPCIÓN DE LAS CARGAS].

B) D./Dña. [NOMBRE Y APELLIDOS] es propietario/a del vehículo [MODELO], marca [MARCA], con número de bastidor [Nº DE BASTIDOR].

C) D./Dña. [NOMBRE Y APELLIDOS] es titular de [Nº] participaciones en la mercantil [DENOMINACIÓN SOCIAL], sociedad de responsabilidad limitada.

D) D./Dña. [NOMBRE Y APELLIDOS] es propietario/a de la cuenta corriente nº [Nº DE CUENTA] de la entidad bancaria [ENTIDAD].

E) D./Dña. [NOMBRE Y APELLIDOS] es propietario/a del inmueble sito en [LOCALIDAD], calle [CALLE], número [Nº], con una superficie de [SUPERFICIE] metros cuadrados.

Cuota de [PORCENTAJE] % en el valor del bloque donde está ubicada la citada vivienda y elementos comunes.

Título: adquirido por [TÍTULO: compraventa / herencia / donación / otro], efectuada en virtud de escritura pública otorgada ante el Notario de [LOCALIDAD], D./Dña. [NOMBRE DEL NOTARIO], el día [DÍA] de [MES] de [AÑO], número [Nº DE PROTOCOLO] de su protocolo.

Inscripción: está inscrita en el Registro de la Propiedad número [Nº] de [LOCALIDAD], en el tomo [TOMO], libro [LIBRO], folio [FOLIO], finca [Nº DE FINCA].

Referencia catastral: [REFERENCIA CATASTRAL], según consta en la referencia del último recibo del Impuesto sobre Bienes Inmuebles.

Cargas: la referida finca se encuentra [ELEGIR: libre de cargas y gravámenes / gravada con las siguientes cargas: DESCRIPCIÓN DE LAS CARGAS].

F) D./Dña. [NOMBRE Y APELLIDOS] es propietario/a de la cuenta corriente nº [Nº DE CUENTA] de la entidad bancaria [ENTIDAD].

Administración común

Los comparecientes mantendrán la administración individual sobre sus bienes privativos, debiendo responder con los mismos de las deudas que provengan de la tenencia de estos.

A partir del otorgamiento de la presente escritura, las ganancias que se obtengan por cualquiera de los cónyuges tendrán la condición de comunes, así como los bienes que se adquieran constante el matrimonio.

Los comparecientes administrarán los bienes comunes conjuntamente, o individualmente con el consentimiento del otro.

Deudas y obligaciones

Los comparecientes responderán de los gastos familiares a partes iguales entre ellos y de manera solidaria ante terceras personas.

Los comparecientes podrán contraer obligaciones con cargo a la comunidad de bienes y satisfacer los gastos familiares con dichos bienes.

Registro civil

Cualquiera de los comparecientes podrá inscribir la presente escritura en el Registro Civil.

OTORGAMIENTO Y AUTORIZACIÓN

Reservas y advertencias legales.- Se las realizo a los comparecientes, en especial las de carácter fiscal y registral.

Advierto también del tratamiento de los datos personales de los otorgantes, que se efectuará conforme al Reglamento (UE) 2016/679 (RGPD) y a la Ley Orgánica 3/2018, de 5 de diciembre, de Protección de Datos Personales y garantía de los derechos digitales (LOPDGDD). Los comparecientes consienten que sus datos personales sean tratados en esta notaría, conservándose con carácter confidencial y reservado, y sin perjuicio de las remisiones autorizadas por la ley.

La finalidad del tratamiento es facilitar la tramitación y seguimiento de esta escritura.

Es responsable del tratamiento, de su seguridad y confidencialidad, el Notario titular de esta notaría.

Lectura.- Permito a los señores comparecientes la lectura de esta escritura, porque así lo solicitan después de advertidos de la opción del artículo 193 del Reglamento Notarial.

Consentimiento.- Enterados, según dicen, por la lectura que han practicado y por mis explicaciones verbales, los señores comparecientes hacen constar libremente su consentimiento al contenido de la escritura.

Firma.- Y la firman.

Autorización.- Yo, el Notario, compruebo que este otorgamiento se adecúa a la legalidad y a la voluntad debidamente informada y expresada ante mí; y con el contenido de esta escritura, extiendo en [Nº] folios de papel timbrado notarial de la clase [CLASE], serie [SERIE], números [NÚMEROS]. DOY FE.

Firmas

NOTAS DE AYUDA

Los capítulos matrimoniales se pueden otorgar antes o después del matrimonio.

Existen diversos regímenes económicos: separación de bienes, asociación a compras y mejoras, agermanament, participación en las ganancias, etc. En el supuesto de no otorgar capítulos matrimoniales, y si ambos contrayentes tienen vecindad civil catalana, rige la separación de bienes.

En el supuesto de que los bienes privativos fueran insuficientes para satisfacer las deudas que han sido comentadas, el acreedor podrá solicitar el embargo de bienes comunes, pero el otro cónyuge podrá solicitar la disolución de la comunidad de bienes, para que este solo afecte a la parte del deudor.
