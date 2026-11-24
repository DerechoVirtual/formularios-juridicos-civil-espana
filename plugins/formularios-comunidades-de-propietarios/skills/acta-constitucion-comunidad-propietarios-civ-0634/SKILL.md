---
name: acta-constitucion-comunidad-propietarios-civ-0634
description: "Acta de constitución de una comunidad de propietarios. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Acta de constitución de una comunidad de propietarios

> Formulario **CIV-0634** del plugin **Comunidades de propietarios** (`formularios-comunidades-de-propietarios`) · Civil › Propiedad horizontal · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Acta de constitución de una comunidad de propietarios» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Acta de constitución de una comunidad de propietarios” para mi caso». También puedes invocarla directamente con `/formularios-comunidades-de-propietarios:acta-constitucion-comunidad-propietarios-civ-0634`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-comunidades-de-propietarios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Comunidades de propietarios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] PISO (5 veces)
- [ ] TIPO DE MAYORÍA (UNANIMIDAD...) (4 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] Nº (3 veces)
- [ ] AÑO
- [ ] CALLE
- [ ] DÍA
- [ ] ENTIDAD BANCARIA
- [ ] HORA
- [ ] IMPORTE
- [ ] MES
- [ ] NOMBRE DE LA CALLE
- [ ] Nº DE PROPIETARIOS
- [ ] NÚMERO
- [ ] PORCENTAJE
- [ ] SUCURSAL

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

Encabezado

ACTA DE LA COMUNIDAD DE PROPIETARIOS DEL EDIFICIO SITO EN [LOCALIDAD] DONDE LE CORRESPONDE EL NÚMERO [NÚMERO] DE [NOMBRE DE LA CALLE]

Relación de asistentes y representados

REUNIDOS

En [LOCALIDAD], a [DÍA], de [MES] de [AÑO], siendo las [HORA], se hallan reunidos los siguientes propietarios:

RELACIÓN DE ASISTENTES:

Local 1	D. cuota de participación %
Local 2	D. cuota de participación %
Piso 1º A	D. cuota de participación %
Piso 1º B	D. cuota de participación %
Piso 2º A	D. cuota de participación %
Piso 2º B	D. cuota de participación %
Piso 3º A	D. cuota de participación %
Piso 3º B	D. cuota de participación %

RELACIÓN DE REPRESENTADOS:

Local [Nº] representado por D. cuota de participación %

Piso [PISO] representado por D. cuota de participación %

Se hallan por lo tanto representados [Nº DE PROPIETARIOS] propietarios, que suman el [PORCENTAJE] por 100 del total de cuotas del edificio.

Orden del día

Se acuerdan nombrar para la redacción de la presente acta, como Secretario a D. [NOMBRE Y APELLIDOS] y para dirigir las deliberaciones a D.. [NOMBRE Y APELLIDOS]

El orden del día que se aprueba por unanimidad con todos los temas y asuntos relacionados con la puesta en funcionamiento de la Comunidad de Propietarios de acuerdo con la Ley de Propiedad Horizontal de 21 de julio de 1960 y las modificaciones posteriores.

Elección de cargos

Se acuerda por [TIPO DE MAYORÍA (UNANIMIDAD...)] que los órganos de gobierno de la comunidad sean la Junta de Propietarios, Presidente (nombrado por turno rotatorio de [Nº] meses entre todos los propietarios comenzando por la planta [PISO]), Vicepresidente, Secretario y Administrador, con las facultades que la Ley de Propiedad Horizontal les atribuye.

Los cargos de Secretario y Administrador serán desempeñados por [NOMBRE Y APELLIDOS]

Los aquí comparecientes a todos los efectos proceden a la declaración de constitución e inicio del funcionamiento de la Comunidad de Propietarios a cuyo efecto acuerdan:

1. Nombrar por [TIPO DE MAYORÍA (UNANIMIDAD...)] Presidente de la Comunidad a D. [NOMBRE Y APELLIDOS], propietario del piso [PISO]

2. Nombrar por [TIPO DE MAYORÍA (UNANIMIDAD...)] Secretario de la Comunidad a D. [NOMBRE Y APELLIDOS], propietario del piso [PISO]

3. Por [TIPO DE MAYORÍA (UNANIMIDAD...)] que el cargo de Administrador sea ejercido por [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], en la calle [CALLE], piso [PISO]

Ejercicio anual

El ejercicio anual será del 1 de enero al 31 de diciembre del año natural.

Legalización de libros

Se acuerda por unanimidad que el Administrador legalice en el Registro de la Propiedad el Libro de Actas y se transcriban en el mismo todas y cada una de las que se celebren de esta Comunidad de Propietarios. El Libro será guardado por el Secretario y tendrá obligación de entregarlo al Presidente que lo sea de la Comunidad tan pronto se lo solicite.

Apertura de cuenta corriente y provisión inicial

Se acuerda por unanimidad abrir una cuenta corriente en la Entidad [ENTIDAD BANCARIA], oficina de [SUCURSAL], la que se harán los pagos e ingresos de la Junta de Propietarios, en la que deberán realizarse el ingreso de las diferentes cuotas.

Se acuerda establecer una provisión inicial de fondos de [IMPORTE] euros, que se abonarán entre todos los propietarios en razón de sus cuotas de participación, designando a estos solos efectos al propietario D. [NOMBRE Y APELLIDOS] como Tesorero y depositario del fondo creado.

Copia de la escritura de obra nueva y división horizontal

Se acuerda por unanimidad facilitar a todos los propietarios de la finca una fotocopia de la Escritura de Obra Nueva y División Horizontal, de los Estatutos y normas especiales de comunidad, a efectos de que todos las conozcan y puedan consultarlas.

Número de identificació fiscal

Se acuerda por unanimidad que el Administrador solicite el correspondiente Número de Identificación Fiscal.

Otorgamiento de poderes

Se acuerda por unanimidad que el Presidente pueda otorgar poderes para pleitos, si ello fuera necesario, sin necesidad de acuerdo expreso de la Junta de Propietarios.

No habiendo más asuntos que tratar, se levantó la sesión, siendo las [Nº] horas del día indicado al principio.

Fdo.

(El Presidente)

Fdo.

(El Secretario)

========================================================================
