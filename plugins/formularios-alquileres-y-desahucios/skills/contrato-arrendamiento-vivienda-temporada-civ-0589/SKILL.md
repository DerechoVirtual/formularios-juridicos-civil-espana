---
name: contrato-arrendamiento-vivienda-temporada-civ-0589
description: "Contrato de arrendamiento de vivienda por temporada. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de arrendamiento de vivienda por temporada

> Formulario **CIV-0589** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 24-11-2026.

## Qué es

Contrato de arrendamiento de vivienda por temporada, en el que se concretan las condiciones, estipulaciones y circunstancias para llevar a cabo el contrato, así como los derechos y obligaciones tanto del arrendador como del arrendatario.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de arrendamiento de vivienda por temporada» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de arrendamiento de vivienda por temporada” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:contrato-arrendamiento-vivienda-temporada-civ-0589`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (12 veces)
- [ ] LOCALIDAD (6 veces)
- [ ] DNI/NIE (4 veces)
- [ ] DIRECCIÓN (3 veces)
- [ ] IMPORTE (3 veces)
- [ ] IMPORTE EN CIFRA (3 veces)
- [ ] FECHA (2 veces)
- [ ] LUGAR (2 veces)
- [ ] MES (2 veces)
- [ ] NACIONALIDAD (2 veces)
- [ ] NOMBRE DEL EDIFICIO (2 veces)
- [ ] Nº DE APARTAMENTO (2 veces)
- [ ] CALLE
- [ ] PERIODO DE OCUPACIÓN
- [ ] REFERENCIA CATASTRAL
- [ ] SERVICIOS INCLUIDOS
- [ ] TEMPORADA

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

Contrato de arrendamiento de vivienda por temporada, en el que se concretan las condiciones, estipulaciones y circunstancias para llevar a cabo el contrato, así como los derechos y obligaciones tanto del arrendador como del arrendatario.


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

En [LUGAR], a [FECHA]
REUNIDOS

DE UNA PARTE,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

(Datos del ARRENDADOR)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, ARRENDADOR.

Y DE OTRA,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

(Datos del ARRENDATARIO)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, ARRENDATARIO.

INTERVIENEN

[ELEGIR UNA OPCIÓN: en caso de que todas las partes actúen en nombre y representación propia / si alguna de las partes actúa en su propio nombre y representación]

[OPCIONAL — si alguna de las partes actúa en nombre y representación de persona física o jurídica]
[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de:

[ELEGIR UNA OPCIÓN: Si se trata de persona física / Si se trata de una persona jurídica]

Ambas partes se reconocen mutuamente con capacidad suficiente para otorgar el presente contrato de ARRENDAMIENTO DE VIVIENDA POR TEMPORADA y, a tal fin,

EXPONEN

I.- Que D./Dña. [NOMBRE Y APELLIDOS] es propietario del apartamento [Nº DE APARTAMENTO] del edificio conocido como [NOMBRE DEL EDIFICIO], sito en la [DIRECCIÓN] de la ciudad de [LOCALIDAD], el cual se encuentra debidamente amueblado, libre de cargas y gravámenes y al corriente en el pago de impuestos, según declara el arrendador en este acto, cuya referencia catastral se identifica [REFERENCIA CATASTRAL].

II.- Que D./Dña. [NOMBRE Y APELLIDOS] tiene una vivienda habitual y permanente en la ciudad de [LOCALIDAD], [DIRECCIÓN].

III.- Que D./Dña. [NOMBRE Y APELLIDOS] se encuentra interesado en alquilar el apartamento arriba mencionado, para la temporada de [TEMPORADA] del año en curso, que abarca el período comprendido entre los meses de [MES] y [MES].

IV.- Que las partes han convenido el arrendamiento del apartamento mencionado, otorgándose a dicho fin el presente contrato que lo llevan a efecto de conformidad con las siguientes,

ESTIPULACIONES

Primera.- D./Dña. [NOMBRE Y APELLIDOS] arrienda a D./Dña. [NOMBRE Y APELLIDOS], quien acepta, el apartamento descrito en el Expositivo I.- de este contrato y que es el [Nº DE APARTAMENTO] del edificio conocido como [NOMBRE DEL EDIFICIO], sito en la calle [CALLE] de la ciudad de [LOCALIDAD].

Segunda.- La ocupación del expresado apartamento será en las fechas comprendidas del [PERIODO DE OCUPACIÓN], ambas inclusive, por lo que llegado el día final de la vigencia no será objeto de prórroga, resolviéndose automáticamente.

Tercera.- El presente contrato constituye un arrendamiento para uso distinto de vivienda, de conformidad a lo establecido en la Ley 29/1994, de 24 de noviembre, de Arrendamientos Urbanos, no siendo el destino primordial del apartamento arrendado el cumplir la función de satisfacer la necesidad permanente de vivienda del arrendatario, por tener este su domicilio habitual y permanente en [LOCALIDAD], [DIRECCIÓN].

Cuarta.- El precio del presente arrendamiento se fija en la cantidad de [IMPORTE] euros ([IMPORTE EN CIFRA] €) por la temporada pactada, incluyendo en el precio de alquiler los servicios de [SERVICIOS INCLUIDOS], así como los muebles, objetos y enseres que se detallan en el inventario aparte, que es debidamente firmado por las partes y que se considera parte integrante de este contrato, al finalizar el alquiler el arrendatario se compromete a pagar la cantidad de [IMPORTE] euros ([IMPORTE EN CIFRA] €) por limpieza del mismo.

Quinta.- El arrendatario declara recibir el apartamento objeto de arriendo y los diversos muebles, objetos y enseres en el mismo existentes en perfecto estado y en las mismas condiciones deber entregarlos a la propiedad al término del arriendo, siendo de cuenta y cargo del arrendatario todas las reparaciones que hayan de realizarse, por daños causados, así como las reposiciones de cuantas perdidas o deterioros le sean imputables.

Sexta.- Los servicios de electricidad, agua, gas, teléfono y aquellos otros de que pudiera estar dotado el inmueble, serán de cuenta y cargo del arrendatario.

Séptima.- Al finalizar la temporada de arriendo, el arrendatario deber dejar a la libre disposición de la propiedad el apartamento arrendado, haciéndole entrega a esta de las llaves del mismo. De no efectuarse tal entrega, se considerará que la ocupación del arrendatario es precaria, autorizando expresamente ya desde ahora al arrendador para que pueda tomar posesión por su propia autoridad del apartamento objeto de este contrato. Cada día que pase de la terminación del contrato, devengará en favor del arrendador y tendrá que hacer efectivo el arrendatario una renta equivalente al duplo de un día de vigencia del arrendamiento.

Octava.- El arrendatario deposita la cantidad de [IMPORTE] euros ([IMPORTE EN CIFRA] €), en concepto de fianza, que servirán como anticipo de servicios como electricidad, teléfono, etc. o para responder de daños causados al apartamento, y que le serán devueltas al término del contrato si previas las deducciones que procedan por incumplimiento de lo estipulado en este contrato.

Y leído el presente documento, ambas partes lo firman en señal de conformidad y ratificación de su contenido, haciéndolo por duplicado y a un solo efecto.

En [LUGAR], a [FECHA].

ARRENDADOR

ARRENDATARIO
Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

========================================================================
