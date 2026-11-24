---
name: testamento-reconocimiento-hijo-extramatrimonial-civ-0424
description: "Testamento con reconocimiento de hijo extramatrimonial. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Testamento con reconocimiento de hijo extramatrimonial

> Formulario **CIV-0424** del plugin **Herencias, testamentos y donaciones** (`formularios-herencias-y-donaciones`) · Civil › Sucesiones y donaciones · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Testamento con reconocimiento de hijo extramatrimonial» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Testamento con reconocimiento de hijo extramatrimonial” para mi caso». También puedes invocarla directamente con `/formularios-herencias-y-donaciones:testamento-reconocimiento-hijo-extramatrimonial-civ-0424`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-herencias-y-donaciones:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Herencias, testamentos y donaciones) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (10 veces)
- [ ] LOCALIDAD (6 veces)
- [ ] AÑO (4 veces)
- [ ] DÍA (4 veces)
- [ ] MES (4 veces)
- [ ] Nº (4 veces)
- [ ] NOMBRE DE LOS HIJOS (2 veces)
- [ ] CALLE
- [ ] IMPORTE
- [ ] NIF/DNI
- [ ] Nº DE HIJOS
- [ ] NÚMERO
- [ ] PROFESIÓN
- [ ] PÁGINA
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

TESTAMENTO DE DON/DOÑA [NOMBRE Y APELLIDOS]

NÚMERO [NÚMERO]

En [LOCALIDAD], mi residencia, a [DÍA] de [MES] de [AÑO], siendo las [Nº] horas y [Nº] minutos.

Ante mí, Notario de esta Capital y su Ilustre Colegio,

COMPARECE:

DON/DOÑA [NOMBRE Y APELLIDOS], mayor de edad, nacido/a el día [DÍA] de [MES] de [AÑO], de profesión [PROFESIÓN], natural de [LOCALIDAD] y vecino/a de [LOCALIDAD], con domicilio en calle [CALLE], núm. [Nº], y con D.N.I. número [NIF/DNI]

Constan sus circunstancias personales de sus manifestaciones.

Interviene en su propio nombre y derecho.

Identifico al/a la compareciente a través de su D.N.I., que me exhibe.

Declara que sabe y puede leer este testamento,

Tiene, a mi juicio, según interviene, capacidad legal necesaria para otorgar TESTAMENTO ABIERTO, a cuyo fin:

EXPONE

I.- Que nació en [LOCALIDAD], el día [DÍA] de [MES] de [AÑO]; y que es hijo/a de los consortes Don [NOMBRE Y APELLIDOS] fallecido o "que vive", y Doña [NOMBRE Y APELLIDOS], que vive (o fallecida).

II.- Está casado/a en [ELEGIR: primeras / segundas] nupcias con Don/Doña [NOMBRE Y APELLIDOS], de cuyo matrimonio tiene [Nº DE HIJOS] hijos, llamados [NOMBRE DE LOS HIJOS]

III.- Que ordena su última voluntad con sujeción a las siguientes:

CLÁUSULAS:

Reconoce como hijo extramatrimonial suyo a [NOMBRE Y APELLIDOS], nacido en [LOCALIDAD], el día [DÍA] de [MES] de [AÑO], inscrito en el Registro Civil de [LOCALIDAD], tomo [TOMO], página [PÁGINA], como hijo de padre desconocido y de Doña [NOMBRE Y APELLIDOS], soltera. En virtud de este reconocimiento el hijo pasará a llamarse

Lega a su cónyuge, Don/Doña [NOMBRE Y APELLIDOS] el tercio de libre disposición en pleno dominio, sin perjuicio de la cuota vidual usufructuaria que por Ley le corresponde.

Instituye herederos universales por partes iguales a sus hijos [NOMBRE DE LOS HIJOS] y a los demás que pudiera tener en el futuro, a los que sustituye vulgarmente, caso de premoriencia o incapacidad, por sus respectivos descendientes.

Nombra Comisario-Contador-Partidor y Albacea a Don/Doña [NOMBRE Y APELLIDOS] y, en caso de premoriencia del designado, a Don/Doña [NOMBRE Y APELLIDOS], con las más amplias facultades legales y en especial con la facultad de liquidar junto con el cónyuge viudo la sociedad conyugal, entregar legados y conmutar el usufructo del cónyuge viudo de acuerdo con éste, señalando como plazo para el ejercicio de su cargo el legal establecido, con prórroga por dos años más.

INFORMACIÓN DE DATOS.

Respecto a los datos personales recogidos en el presente documento, debe tenerse en cuenta que el tratamiento de los mismos se ajustará a la LO 3/2018, de 5 de diciembre, de Protección de Datos de Carácter Personal y Garantía de los Derechos Digitales, en desarrollo y aplicación del Reglamento UE 2016/679, de 27 de abril, y que el interesado podrá ejercitar sus derechos de acceso, rectificación, cancelación, supresión (derecho al olvido), portabilidad, oposición y limitación del tratamiento de los datos (ARCO-POL) en los términos establecidos en los arts. 12 a 23 y 12 a 18 de los citados Reglamento y Ley Orgánica, respectivamente.

OTORGAMIENTO:

Así lo dice y otorga el/la compareciente ante mí.

AUTORIZACIÓN:

Leo en voz alta e íntegramente el contenido de este testamento, previa advertencia del derecho que para hacerlo por sí asiste al/a la otorgante, que renuncia a ello y en prueba de conformidad, lo firma conmigo.

Y yo, el Notario, DOY FE de haberle identificado de la forma expresada, de haber observado la unidad de acto y demás formalidades legales, de que presta libremente su consentimiento y de todo lo demás consignado en este testamento, extendido en [Nº] folios de papel timbrado del Estado, exclusivo para documentos notariales de la serie y números

SIGUE LA FIRMA DEL TESTADOR/A.

=SIGNADO.- = RUBRICADOS Y SELLADO.

APLICACIÓN ARANCEL.- DISPOSICIÓN ADICIONAL 3 LEY 8/89. BASES DE CÁLCULO: ARANCEL APLICABLE: DERECHOS ARANCELARIOS: [IMPORTE] euros.-

========================================================================
