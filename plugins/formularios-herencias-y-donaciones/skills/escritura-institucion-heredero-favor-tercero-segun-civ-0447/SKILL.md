---
name: escritura-institucion-heredero-favor-tercero-segun-civ-0447
description: "Escritura de institución de heredero a favor de un tercero según el Derecho aragonés. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escritura de institución de heredero a favor de un tercero según el Derecho aragonés

> Formulario **CIV-0447** del plugin **Herencias, testamentos y donaciones** (`formularios-herencias-y-donaciones`) · Civil › Sucesiones y donaciones · normativa revisada el 24-11-2026.

## Qué es

Escritura notarial de sucesión paccionada aragonesa por la que dos instituyentes designan heredero a un tercero para después de sus días (institución en favor de tercero), con pactos sobre disposición de bienes, revocación y reservas. Se usa cuando se quiere ordenar la sucesión por pacto, sin transmitir los bienes en vida.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escritura de institución de heredero a favor de un tercero según el Derecho aragonés» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escritura de institución de heredero a favor de un tercero según el Derecho aragonés” para mi caso». También puedes invocarla directamente con `/formularios-herencias-y-donaciones:escritura-institucion-heredero-favor-tercero-segun-civ-0447`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-herencias-y-donaciones:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Herencias, testamentos y donaciones) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (7 veces)
- [ ] Nº (6 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] AÑO (3 veces)
- [ ] DESCRIPCIÓN DEL BIEN (3 veces)
- [ ] DÍA (3 veces)
- [ ] ENTIDAD (3 veces)
- [ ] MES (3 veces)
- [ ] NOMBRE DEL NOTARIO (3 veces)
- [ ] Nº DE CUENTA (3 veces)
- [ ] CALLE (2 veces)
- [ ] FOLIO (2 veces)
- [ ] LIBRO (2 veces)
- [ ] MARCA Y MODELO (2 veces)
- [ ] NOMBRE Y APELLIDOS DE LA MADRE (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL HIJO/A (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL INSTITUYENTE 1 (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL INSTITUYENTE 2 (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL PADRE (2 veces)
- [ ] Nº DE BASTIDOR (2 veces)
- [ ] Nº DE FINCA (2 veces)
- [ ] Nº DE PLANTAS (2 veces)
- [ ] Nº DE PROTOCOLO (2 veces)
- [ ] PORCENTAJE (2 veces)
- [ ] REFERENCIA CATASTRAL (2 veces)
- [ ] SUPERFICIE (2 veces)
- [ ] TOMO (2 veces)
- [ ] CLASE
- [ ] COLEGIO NOTARIAL
- [ ] DENOMINACIÓN SOCIAL
- [ ] DESCRIPCIÓN DE LA CARGA
- [ ] DESCRIPCIÓN DE LOS BIENES
- [ ] EXPLICAR LA CONDICIÓN
- [ ] NOMBRE Y APELLIDOS DEL CÓNYUGE
- [ ] NOMBRE Y APELLIDOS DEL DESCENDIENTE DEL INSTITUIDO
- [ ] NOMBRE Y APELLIDOS DEL INSTITUIDO
- [ ] NÚMEROS
- [ ] SERIE

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

### Avisos de actualización (1) — se aplican en el texto, nunca se copian en el documento

- Junto a «…e Protección de Datos Personales y garantía de los derechos digitales (LOPDGDD).»: el original remitía a los ficheros automatizados de la Orden del Ministerio de Justicia 484/2003, de 19 de febrero, hoy desplazada por el RGPD y la LOPDGDD; se ha adaptado la advertencia. Comprobar la cláusula informativa de protección de datos vigente en el protocolo de la notaría.

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

SUCESIÓN PACCIONADA. INSTITUCIÓN EN FAVOR DE TERCERO (ARAGÓN)

En [LOCALIDAD], mi residencia, a [DÍA] de [MES] de [AÑO].

Ante mí, [NOMBRE DEL NOTARIO], Notario/a del Ilustre Colegio de Notarios de [COLEGIO NOTARIAL],

[COMPARECENCIA: identificar a los otorgantes con nombre y apellidos, DNI/NIE, domicilio, estado civil y capacidad, según el protocolo notarial.]

DICEN

INSTITUYENTE 1

Que D./Dña. [NOMBRE Y APELLIDOS DEL INSTITUYENTE 1] es hijo/a de los consortes D. [NOMBRE Y APELLIDOS DEL PADRE], [ELEGIR: fallecido / que vive], y D.ª [NOMBRE Y APELLIDOS DE LA MADRE], [ELEGIR: fallecida / que vive]; estando casado/a en únicas nupcias con D.ª/D. [NOMBRE Y APELLIDOS DEL CÓNYUGE], de cuyo matrimonio tiene [Nº] hijos, llamados [NOMBRE Y APELLIDOS DEL HIJO/A] y [NOMBRE Y APELLIDOS DEL HIJO/A].

Que D./Dña. [NOMBRE Y APELLIDOS DEL INSTITUYENTE 1] es propietario/a de los siguientes bienes: [OPCIONAL — no es necesario describirlos, porque la transmisión se produce tras el fallecimiento del instituyente]

A) Inmueble sito en [LOCALIDAD], calle [CALLE], número [Nº], con una superficie de [SUPERFICIE] metros cuadrados, distribuidos en [Nº DE PLANTAS] plantas.

Cuota de [PORCENTAJE] % en el valor del bloque donde está ubicada la citada vivienda y elementos comunes.

Título: adquirido por [TÍTULO: compraventa / herencia / donación / otro], efectuada en virtud de escritura pública otorgada ante el Notario de [LOCALIDAD], D./Dña. [NOMBRE DEL NOTARIO], el día [DÍA] de [MES] de [AÑO], número [Nº DE PROTOCOLO] de su protocolo.

Inscripción: está inscrita en el Registro de la Propiedad número [Nº] de [LOCALIDAD], en el tomo [TOMO], libro [LIBRO], folio [FOLIO], finca [Nº DE FINCA].

Referencia catastral: [REFERENCIA CATASTRAL], según consta en la referencia del último recibo del Impuesto sobre Bienes Inmuebles.

Cargas: la referida finca se encuentra [ELEGIR: libre de cargas y gravámenes / gravada con las siguientes cargas: DESCRIPCIÓN DE LAS CARGAS].

B) Vehículo [MARCA Y MODELO], con número de bastidor [Nº DE BASTIDOR].

C) Participaciones en la mercantil [DENOMINACIÓN SOCIAL], sociedad de responsabilidad limitada.

D) Cuenta corriente nº [Nº DE CUENTA] de la entidad bancaria [ENTIDAD].

E) Cuenta corriente nº [Nº DE CUENTA] de la entidad bancaria [ENTIDAD].

INSTITUYENTE 2

Que D./Dña. [NOMBRE Y APELLIDOS DEL INSTITUYENTE 2] es hijo/a de los consortes D. [NOMBRE Y APELLIDOS DEL PADRE] y D.ª [NOMBRE Y APELLIDOS DE LA MADRE], [ELEGIR: fallecidos ambos / que vive(n)].

Que D./Dña. [NOMBRE Y APELLIDOS DEL INSTITUYENTE 2] es propietario/a de los siguientes bienes:

A) Inmueble sito en [LOCALIDAD], calle [CALLE], número [Nº], con una superficie de [SUPERFICIE] metros cuadrados, distribuidos en [Nº DE PLANTAS] plantas.

Cuota de [PORCENTAJE] % en el valor del bloque donde está ubicada la citada vivienda y elementos comunes.

Título: adquirido por [TÍTULO: compraventa / herencia / donación / otro], efectuada en virtud de escritura pública otorgada ante el Notario de [LOCALIDAD], D./Dña. [NOMBRE DEL NOTARIO], el día [DÍA] de [MES] de [AÑO], número [Nº DE PROTOCOLO] de su protocolo.

Inscripción: está inscrita en el Registro de la Propiedad número [Nº] de [LOCALIDAD], en el tomo [TOMO], libro [LIBRO], folio [FOLIO], finca [Nº DE FINCA].

Referencia catastral: [REFERENCIA CATASTRAL], según consta en la referencia del último recibo del Impuesto sobre Bienes Inmuebles.

Cargas: la referida finca se encuentra [ELEGIR: libre de cargas y gravámenes / gravada con las siguientes cargas: DESCRIPCIÓN DE LAS CARGAS].

B) Vehículo [MARCA Y MODELO], con número de bastidor [Nº DE BASTIDOR].

C) Cuenta corriente nº [Nº DE CUENTA] de la entidad bancaria [ENTIDAD].

OTORGAN

Que, en uso de la facultad que les otorga el Decreto Legislativo 1/2011, de 22 de marzo, del Gobierno de Aragón, por el que se aprueba, con el título de «Código del Derecho Foral de Aragón», el Texto Refundido de las Leyes civiles aragonesas, deciden otorgar la presente escritura de institución de heredero en favor de tercero, a tenor de las siguientes

ESTIPULACIONES

Objeto

Ambos comparecientes instituyen heredero, para después de sus días, a D./Dña. [NOMBRE Y APELLIDOS DEL INSTITUIDO], quien no podrá aceptar hasta que fallezcan los instituyentes, y lo hacen de acuerdo con los siguientes pactos:

a) La institución es para después de los días de los instituyentes, es decir, no se transmite en el presente acto ninguno de los bienes de los instituyentes.

b) La institución abarca todo el patrimonio de los instituyentes a su fallecimiento, incluidos bienes, derechos y obligaciones.

c) Los instituyentes podrán disponer libremente de sus bienes, pero necesitarán recabar el consentimiento de los instituidos para llevar a cabo donaciones.

d) Cabe la revocación unilateral de la presente sucesión paccionada por las causas legales, y en el supuesto de que se cumpla la siguiente condición: [EXPLICAR LA CONDICIÓN].

Reservas

Los instituyentes deciden realizar las siguientes reservas:

a) D./Dña. [NOMBRE Y APELLIDOS] reserva para su cónyuge el usufructo sobre el siguiente bien: [DESCRIPCIÓN DEL BIEN], limitando su derecho de viudedad.

b) D./Dña. [NOMBRE Y APELLIDOS] reserva el siguiente bien: [DESCRIPCIÓN DEL BIEN], para sus descendientes.

c) D./Dña. [NOMBRE Y APELLIDOS] reserva los siguientes bienes: [DESCRIPCIÓN DE LOS BIENES], para disponer libremente de ellos mediante testamento.

d) D./Dña. [NOMBRE Y APELLIDOS] reserva su facultad de disposición sobre el siguiente bien: [DESCRIPCIÓN DEL BIEN], al objeto de constituir la siguiente carga sobre el mismo: [DESCRIPCIÓN DE LA CARGA].

e) Ambos designan a D./Dña. [NOMBRE Y APELLIDOS DEL DESCENDIENTE DEL INSTITUIDO], descendiente del instituido, como heredero de los bienes objeto de la presente institución, para el supuesto de que este les premuera.

RESERVAS Y ADVERTENCIAS LEGALES

Reservas y advertencias legales.- Se las realizo a los comparecientes, en especial las de carácter fiscal y registral.

Advierto también del tratamiento de los datos personales de los otorgantes, que se efectuará conforme al Reglamento (UE) 2016/679 (RGPD) y a la Ley Orgánica 3/2018, de 5 de diciembre, de Protección de Datos Personales y garantía de los derechos digitales (LOPDGDD).

De conformidad con el art. 6 de la Ley Orgánica 3/2018, de 5 de diciembre, se entiende por consentimiento del afectado toda manifestación de voluntad libre, específica, informada e inequívoca por la que este acepta, ya sea mediante una declaración o una clara acción afirmativa, el tratamiento de datos personales que le conciernen. Cuando se pretenda fundar el tratamiento de los datos en el consentimiento del afectado para una pluralidad de finalidades será preciso que conste de manera específica e inequívoca que dicho consentimiento se otorga para todas ellas. No podrá supeditarse la ejecución del contrato a que el afectado consienta el tratamiento de los datos personales para finalidades que no guarden relación con el mantenimiento, desarrollo o control de la relación contractual.

La finalidad del tratamiento es facilitar la tramitación y seguimiento de esta escritura.

Es responsable del tratamiento, de su seguridad y confidencialidad, el Notario titular de esta notaría.

Lectura.- Permito a los señores comparecientes la lectura de esta escritura, porque así lo solicitan después de advertidos de la opción del artículo 193 del Reglamento Notarial.

Consentimiento.- Enterados, según dicen, por la lectura que han practicado y por mis explicaciones verbales, los señores comparecientes hacen constar libremente su consentimiento al contenido de la escritura.

Firma.- Y la firman.

Autorización.- Yo, el Notario, compruebo que este otorgamiento se adecúa a la legalidad y a la voluntad debidamente informada y expresada ante mí; y con el contenido de esta escritura, extiendo en [Nº] folios de papel timbrado notarial de la clase [CLASE], serie [SERIE], números [NÚMEROS]. DOY FE.

Firmas

NOTAS DE AYUDA

Se pueden pactar limitaciones: recabar consentimiento, no poder disponer de determinados bienes.

Los bienes de los que no se haya dispuesto mediante testamento pasarán a ser parte de la institución.

Puede el instituyente establecer que, en el caso de que el instituido le premuera sin descendientes, los bienes que le fueron transmitidos mediante la presente escritura le reviertan.
