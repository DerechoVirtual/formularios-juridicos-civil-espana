---
name: testamento-mejora-labrar-poseer-segun-derecho-gallego-civ-0432
description: "Testamento con mejora de labrar y poseer según el Derecho gallego. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Testamento con mejora de labrar y poseer según el Derecho gallego

> Formulario **CIV-0432** del plugin **Herencias, testamentos y donaciones** (`formularios-herencias-y-donaciones`) · Civil › Sucesiones y donaciones · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Testamento con mejora de labrar y poseer según el Derecho gallego» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Testamento con mejora de labrar y poseer según el Derecho gallego” para mi caso». También puedes invocarla directamente con `/formularios-herencias-y-donaciones:testamento-mejora-labrar-poseer-segun-derecho-gallego-civ-0432`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-herencias-y-donaciones:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Herencias, testamentos y donaciones) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (9 veces)
- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] NÚMERO (3 veces)
- [ ] AÑO (2 veces)
- [ ] DÍA (2 veces)
- [ ] ENTIDAD BANCARIA (2 veces)
- [ ] MES (2 veces)
- [ ] CLASE
- [ ] CULTIVO
- [ ] DENOMINACIÓN SOCIAL
- [ ] FINCA
- [ ] FOLIO
- [ ] LIBRO
- [ ] MARCA/MODELO
- [ ] NOMBRE DE LA EXPLOTACIÓN
- [ ] NOMBRE DEL NOTARIO
- [ ] Nº DE BASTIDOR
- [ ] Nº DE HIJOS
- [ ] SERIE
- [ ] SUPERFICIE
- [ ] TIPO DE VEHÍCULO
- [ ] TOMO
- [ ] TÍTULO DE ADQUISICIÓN

## Normas que cita el formulario

- art. 6 Ley Orgánica 3/2018

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

En [LOCALIDAD], mi residencia, a [DÍA] de [MES] de [AÑO]

Ante mí [NOMBRE DEL NOTARIO], Notario/a del Ilustre Colegio de Notarios de [LOCALIDAD]

DICE

Que D. es hijo/a de los consortes D. [NOMBRE Y APELLIDOS], fallecido, y D.ª [NOMBRE Y APELLIDOS], que vive; estando casado en únicas nupcias con D.ª/D. [NOMBRE Y APELLIDOS], de cuyo matrimonio tiene [Nº DE HIJOS] hijos, llamados [NOMBRE Y APELLIDOS] y [NOMBRE Y APELLIDOS].

Que D. es propietario de los siguientes bienes:

A) Finca rústica sita en [LOCALIDAD], parcela [Nº], polígono [Nº]

Constituye una unidad de explotación agrícola denominada [NOMBRE DE LA EXPLOTACIÓN], que se dedica a la plantación de [CULTIVO].

Extensión: Tiene una superficie de [SUPERFICIE], y linda al Norte con parcela [Nº], polígono [Nº], al Sur y al Este con parcela [Nº], polígono [Nº], y al Oeste con parcela [Nº], polígono

Título: Adquirida por [TÍTULO DE ADQUISICIÓN] efectuada en virtud de escritura pública otorgada ante el Notario de [LOCALIDAD], D. el día [DÍA] de [MES] de [AÑO] número protocolo

Inscripción: Está inscrita en el Registro de la Propiedad número [NÚMERO] de [LOCALIDAD] en el tomo [TOMO] libro [LIBRO] folio [FOLIO] finca [FINCA]

Cargas: La referida finca se encuentra libre de cargas y gravámenes, y no posee arrendatarios.

B) Vehículo [TIPO DE VEHÍCULO] marca [MARCA/MODELO] con número de bastidor [Nº DE BASTIDOR]

C) Participaciones en la mercantil [DENOMINACIÓN SOCIAL] de responsabilidad limitada.

D) Cuenta corriente nº [NÚMERO] de la entidad bancaria [ENTIDAD BANCARIA]

E) Cuenta corriente nº [NÚMERO] de la entidad bancaria [ENTIDAD BANCARIA]

Que en uso de la facultad recogida en la Ley 2/2006, de 14 de junio, de Derecho Civil de Galicia, decide otorgar testamento mediante el que ejercita el poder testatorio que le confirió su esposa y dispone de sus propios bienes, con arreglo a las siguientes

CLÁUSULAS

Institución herederos

D. instituye herederos, por iguales partes, a sus hijos, D. y D. [NOMBRE Y APELLIDOS], de todos sus bienes, a excepción del descrito en la letra A), del apartado segundo, que será objeto de legado.

Legado 1

D. lega a su esposa Dª., el usufructo universal vitalicio de los bienes de la herencia, a salvo del descrito en la letra A), del apartado segundo, que será objeto de legado, eximiéndole de prestar fianza.

La presente disposición quedará sin efecto, en el supuesto de que su esposa vuelva a contraer matrimonio, tras su fallecimiento.

Legado 2

D. lega a su hijo D. [NOMBRE Y APELLIDOS], la explotación agrícola descrita en el apartado segundo, letra A), junto con la maquinaria dedicada a la misma.

Tal y como prescribe el Derecho Civil de Galicia, las parcelas que conforman la explotación, resultan indivisibles, y es voluntad del testador que se mantengan en manos de uno sólo de sus hijos, para preservar la referida indivisibilidad.

Hecha pues la mejora de labrar y poseer, en favor de uno de sus hijos, éste deberá desarrollar la actividad agrícola que ha sido descrita, puesto que de lo contrario, el legado quedará revocado, repartiéndose la finca entre el resto de herederos, por partes iguales.

Reservas y advertencias legales

Se las realizo al compareciente, en especial, las de carácter fiscal y registral.

Advierto también sobre la incorporación de datos a los ficheros automatizados regulados en la Orden del Ministerio de Justicia 484/2003, de 19 de febrero.

De conformidad con el art. 6º de la Ley Orgánica 3/2018, de 5 de diciembre, de Protección de Datos Personales y garantía de los derechos digitales, se entiende por consentimiento del afectado toda manifestación de voluntad libre, específica, informada e inequívoca por la que éste acepta, ya sea mediante una declaración o una clara acción afirmativa, el tratamiento de datos personales que le conciernen. Cuando se pretenda fundar el tratamiento de los datos en el consentimiento del afectado para una pluralidad de finalidades será preciso que conste de manera específica e inequívoca que dicho consentimiento se otorga para todas ellas. No podrá supeditarse la ejecución del contrato a que el afectado consienta el tratamiento de los datos personales para finalidades que no guarden relación con el mantenimiento, desarrollo o control de la relación contractual.

La finalidad de esta incorporación es facilitar la tramitación y seguimiento de esta escritura.

Es responsable del fichero, de su seguridad y confidencialidad, el Notario titular de esta notaría.

Lectura

Permito al señor compareciente la lectura de esta escritura, porque así lo solicita después de advertido de la opción del artículo 193 del Reglamento Notarial.

Consentimiento

Enterado, según dice, por la lectura que ha practicado y por mis explicaciones verbales, el señor compareciente hace constar libremente su consentimiento al contenido de la escritura.

Firma

Y la firma.

Autorización

Yo, el Notario, compruebo que este otorgamiento se adecúa a la legalidad, y a la voluntad debidamente informada y expresada ante mi; y con el contenido de esta escritura, extiendo en [Nº] folios de papel timbrado notarial de la clase [CLASE] serie [SERIE] números [Nº] DOY FE.

========================================================================
