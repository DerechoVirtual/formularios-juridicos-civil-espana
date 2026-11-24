---
name: acta-notarial-notificacion-ruptura-requerimiento-dejar-civ-0081
description: "Acta notarial de notificación de ruptura y requerimiento para dejar sin efecto la escritura de unión. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Acta notarial de notificación de ruptura y requerimiento para dejar sin efecto la escritura de unión

> Formulario **CIV-0081** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Acta notarial de notificación de ruptura y requerimiento para dejar sin efecto la escritura de unión» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Acta notarial de notificación de ruptura y requerimiento para dejar sin efecto la escritura de unión” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:acta-notarial-notificacion-ruptura-requerimiento-dejar-civ-0081`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (8 veces)
- [ ] LOCALIDAD (7 veces)
- [ ] FECHA (5 veces)
- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] AÑO (2 veces)
- [ ] CALLE (2 veces)
- [ ] DNI/NIE (2 veces)
- [ ] CONCEPTO
- [ ] IMPORTE
- [ ] LETRA
- [ ] LUGAR
- [ ] MOTIVO
- [ ] NIF
- [ ] NOMBRE DEL NOTARIO
- [ ] Nº DE LEY
- [ ] Nº DE PROTOCOLO
- [ ] NÚMERO
- [ ] OTROS DATOS
- [ ] PISO
- [ ] PROFESIÓN
- [ ] PUERTA
- [ ] RELACIÓN CON EL DESTINATARIO
- [ ] SERIE
- [ ] VECINDAD CIVIL

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

Número

Acta de notificación y requerimiento

En [LOCALIDAD], mi residencia a [FECHA]

A) Comparecencia.-Ante mí, [NOMBRE DEL NOTARIO] Notario de [LOCALIDAD] del Ilustre Colegio Notarial de [LOCALIDAD] comparecen:

D. [NOMBRE Y APELLIDOS] de profesión [PROFESIÓN] mayor de edad, de vecindad civil [VECINDAD CIVIL] vecino de [LOCALIDAD], calle [CALLE], número [NÚMERO] DNI [DNI/NIE] y NIF [NIF] núm. letra [LETRA].

Interviene en su propio nombre. Me aseguro de su identidad por sus reseñados documentos.

Lo juzgo con capacidad legal suficiente e interés legítimo para esta acta.

B) Notificación y requerimiento.-Manifiesta el Sr. compareciente que es su voluntad irrevocable romper con la unión estable mantenida con D. [NOMBRE Y APELLIDOS], con DNI [DNI/NIE] y NIF núm. [Nº], con domicilio en [LOCALIDAD], calle [CALLE], núm. [Nº], piso [PISO] puerta [PUERTA] formalizada por escritura pública en fecha [FECHA] ante el Notario de [LOCALIDAD] D. núm. [Nº]/[AÑO] de su protocolo y revocar cualquier poder que hubiera otorgado a tu favor a lo largo de dicha unión. Manifiesta que esta voluntad ya ha sido expresada personalmente a D. [NOMBRE Y APELLIDOS] en fecha [FECHA] Y finaliza indicando que es acreedora de una compensación económica dado que [MOTIVO].

Me requiere para que notifique a D. [NOMBRE Y APELLIDOS] en su expresado domicilio, el contenido de la anterior exposición, a los efectos del art. de la Ley [Nº DE LEY]; proceda a requerir a mi vez al mismo para que deje D. sin efecto la escritura pública de constitución de la unión entable con la compareciente otorgada ante el Notario D. [NOMBRE Y APELLIDOS], en [LOCALIDAD] en fecha [FECHA], núm. [Nº] de su protocolo [Nº DE PROTOCOLO]; y abone a la compareciente la cantidad de [IMPORTE] euros mensuales, en concepto de [CONCEPTO]. Acepto el requerimiento.

C) Aprobación y autorización.-Hago al señor compareciente las reservas y advertencias legales. Advertido de la opción del artículo 193 del Reglamento Notarial, permito al señor compareciente, a su instancia, la lectura de esta acta.

Enterado el señor compareciente, según manifiesta, por la lectura que ha practicado y por mis explicaciones verbales, hace constar su consentimiento al contenido de esta acta. Y la firma. Del contenido de esta acta, extendida en [Nº] folios de papel timbrado notarial de serie [SERIE], números [Nº], yo, el Notario, doy fe.

Diligencia de notificación y requerimiento.- (Referida al acta núm. [Nº]/[AÑO], de mi protocolo general ordinario, que redacto en mi estudio según notas tomadas sobre el lugar.)

En [LUGAR], a [FECHA].

A las [Nº] horas me constituyo en el domicilio señalado por el requirente y, tras hacer saber mi condición de Notario y el objeto de mi presencia, entrego cédula con transcripción literal del acta y advertencia del derecho reglamentario a contestar, a la persona más idónea encontrada quien dijo ser [RELACIÓN CON EL DESTINATARIO], que se hizo cargo de la cédula [OTROS DATOS]. De todo lo cual, yo, el Notario, doy fe.

========================================================================
