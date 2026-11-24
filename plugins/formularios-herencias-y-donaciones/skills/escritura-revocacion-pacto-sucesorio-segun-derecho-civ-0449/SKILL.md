---
name: escritura-revocacion-pacto-sucesorio-segun-derecho-civ-0449
description: "Escritura de revocación de pacto sucesorio según el Derecho aragonés. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escritura de revocación de pacto sucesorio según el Derecho aragonés

> Formulario **CIV-0449** del plugin **Herencias, testamentos y donaciones** (`formularios-herencias-y-donaciones`) · Civil › Sucesiones y donaciones · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escritura de revocación de pacto sucesorio según el Derecho aragonés» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escritura de revocación de pacto sucesorio según el Derecho aragonés” para mi caso». También puedes invocarla directamente con `/formularios-herencias-y-donaciones:escritura-revocacion-pacto-sucesorio-segun-derecho-civ-0449`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-herencias-y-donaciones:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Herencias, testamentos y donaciones) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (10 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] NÚMERO (4 veces)
- [ ] AÑO (3 veces)
- [ ] DÍA (3 veces)
- [ ] MES (3 veces)
- [ ] ENTIDAD BANCARIA (2 veces)
- [ ] NOMBRE DEL HIJO/A (2 veces)
- [ ] Nº (2 veces)
- [ ] CALLE
- [ ] CIRCUNSTANCIA QUE PERMITE LA REVOCACIÓN
- [ ] CLASE
- [ ] DENOMINACIÓN SOCIAL
- [ ] FINCA
- [ ] FOLIO
- [ ] LIBRO
- [ ] MARCA/MODELO
- [ ] NOMBRE DEL NOTARIO
- [ ] NOMBRE Y APELLIDOS DEL NOTARIO
- [ ] Nº DE BASTIDOR
- [ ] Nº DE HIJOS
- [ ] PORCENTAJE
- [ ] SERIE
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

SUCESIÓN PACCIONADA. REVOCACION UNILATERAL ARAGÓN

En [LOCALIDAD], mi residencia, a [DÍA] de [MES] De [AÑO]

Ante mí [NOMBRE DEL NOTARIO], Notario/a del Ilustre Colegio de Notarios de [LOCALIDAD]

DICE

Que D [NOMBRE Y APELLIDOS] es hijo/a de los consortes D. [NOMBRE Y APELLIDOS], fallecido, y D.ª [NOMBRE Y APELLIDOS], que vive; estando casado en únicas nupcias con D.ª/D. [NOMBRE Y APELLIDOS], de cuyo matrimonio tiene [Nº DE HIJOS] hijos, llamados [NOMBRE DEL HIJO/A] y [NOMBRE DEL HIJO/A].

Que D [NOMBRE Y APELLIDOS] instituyó heredero de presente a D [NOMBRE Y APELLIDOS] mediante escritura pública otorgada ante el Notario D [NOMBRE Y APELLIDOS DEL NOTARIO] el pasado [DÍA] de [MES] de [AÑO] con número de protocolo

Que se incorpora fotocopia de la refereida escritura pública a esta matriz.

Que D [NOMBRE Y APELLIDOS] transmitió mediante la referida institucion de heredero de presente, los siguientes bienes a D [NOMBRE Y APELLIDOS]

A Inmueble sito en [LOCALIDAD], calle [CALLE] número [NÚMERO] con una superficie de metros cuadrados, distribuidos en dos plantas.

Cuota de [PORCENTAJE] % en el valor del bloque donde está ubicado la citada vivienda y elementos comunes.

Título: Adquirido por [TÍTULO DE ADQUISICIÓN] efectuada en virtud de escritura pública otorgada ante el Notario de [LOCALIDAD], D. el día [DÍA] de [MES] de [AÑO] número protocolo

Inscripción: Está inscrita en el Registro de la Propiedad número [NÚMERO] de [LOCALIDAD] en el tomo [TOMO] libro [LIBRO] folio [FOLIO] finca [FINCA]

Referencia catastral: según consta en la referencia del último recibo del Impuestos sobre bienes Inmuebles.

Cargas: La referida finca se encuentra libre de cargas y gravámenes.

B Vehículo [TIPO DE VEHÍCULO] marca [MARCA/MODELO] con número de bastidor [Nº DE BASTIDOR]

C Participaciones en la mercantil [DENOMINACIÓN SOCIAL] de responsabilidad limitada.

D Cuenta corriente nº [NÚMERO] de la entidad bancaria [ENTIDAD BANCARIA]

E Cuenta corriente nº [NÚMERO] de la entidad bancaria [ENTIDAD BANCARIA]

Que en la escritura de institución de heredero de presente se recogió la posibilidad de revocar unilateralmente el pacto, en el supuesto de que concurriese la siguiente circunstancia [CIRCUNSTANCIA QUE PERMITE LA REVOCACIÓN].

ESTIPULACIONES

Objeto

Que en uso de la facultad que le otorga el Decreto Legislativo 1/2011, de 22 de marzo del Gobierno de Aragón, denominado "Código del Derecho Foral de Aragón", decide revocar unilateralmente la escritura de institución de heredero de presente que ha sido descrita, de manera íntegra, dejándola sin efecto, y recuperando la propiedad de los bienes transmitidos en su día mediante la misma.

Notificacion fehaciente

Que D [NOMBRE Y APELLIDOS] me requiere para que notifique el contenido de la presente escritura de revocación unilateral de pacto sucesorio a D [NOMBRE Y APELLIDOS] cuyos datos constan en la escritura de institución de heredero de presente cuya fotocopia se une a la matriz.

RESERVAS Y ADVERTENCIAS LEGALES

Se las realizo a los comparecientes, en especial, las de carácter fiscal y registral.

Advierto también sobre la incorporación de datos a los ficheros automatizados regulados en la Orden del Ministerio de Justicia 484/2003, de 19 de febrero.

De conformidad con el art. 6º de la Ley Orgánica 3/2018, de 5 de diciembre, de Protección de Datos Personales y garantía de los derechos digitales, se entiende por consentimiento del afectado toda manifestación de voluntad libre, específica, informada e inequívoca por la que éste acepta, ya sea mediante una declaración o una clara acción afirmativa, el tratamiento de datos personales que le conciernen. Cuando se pretenda fundar el tratamiento de los datos en el consentimiento del afectado para una pluralidad de finalidades será preciso que conste de manera específica e inequívoca que dicho consentimiento se otorga para todas ellas. No podrá supeditarse la ejecución del contrato a que el afectado consienta el tratamiento de los datos personales para finalidades que no guarden relación con el mantenimiento, desarrollo o control de la relación contractual.

La finalidad de esta incorporación es facilitar la tramitación y seguimiento de esta escritura.

Es responsable del fichero, de su seguridad y confidencialidad, el Notario titular de esta notaría.

Lectura.-

Permito a los señores comparecientes la lectura de esta escritura, porque así lo solicitan después de advertidos de la opción del artículo 193 del Reglamento Notarial.

Consentimiento.-

Enterados, según dicen, por la lectura que han practicado y por mis explicaciones verbales, los señores comparecientes hacen constar libremente su consentimiento al contenido de la escritura.

Firma.-

Y la firman.

Autorización.-

Yo, el Notario, compruebo que este otorgamiento se adecúa a la legalidad, y a la voluntad debidamente informada y expresada ante mi; y con el contenido de esta escritura, extiendo en [Nº] folios de papel timbrado notarial de la clase [CLASE] serie [SERIE] números [Nº] DOY FE.

Firmas

========================================================================
