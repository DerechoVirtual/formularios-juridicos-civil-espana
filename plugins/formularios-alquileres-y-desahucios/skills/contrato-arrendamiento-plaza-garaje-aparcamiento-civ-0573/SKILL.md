---
name: contrato-arrendamiento-plaza-garaje-aparcamiento-civ-0573
description: "Contrato de arrendamiento de plaza de garaje o aparcamiento subterráneo. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de arrendamiento de plaza de garaje o aparcamiento subterráneo

> Formulario **CIV-0573** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 24-11-2026.

## Qué es

Contrato de arrendamiento de garaje o aparcamiento subterráneo, incluyendo las condiciones y circunstancias necesarias para llevar a cabo el arriendo, así como los derechos y obligaciones tanto del arrendador como del arrendatario.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de arrendamiento de plaza de garaje o aparcamiento subterráneo» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de arrendamiento de plaza de garaje o aparcamiento subterráneo” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:contrato-arrendamiento-plaza-garaje-aparcamiento-civ-0573`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (12 veces)
- [ ] DNI/NIE (4 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] CALLE (3 veces)
- [ ] FECHA (3 veces)
- [ ] Nº (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] LUGAR (2 veces)
- [ ] NACIONALIDAD (2 veces)
- [ ] ENTIDAD BANCARIA
- [ ] IMPORTE
- [ ] IMPORTE EN CIFRA
- [ ] Nº DE CUENTA (IBAN)
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

Notas al pie del formulario original:
(1) Al no quedar este contrato sujeto a las previsiones contenidas en la Ley de Arrendamientos Urbanos las partes pueden pactar la exclusión de la obligación de prestar fianza o la cuantía de la misma que estimen conveniente, así como la posibilidad de aval bancario u otra forma de garantía, siendo preciso que se haga constar tal exigencia de forma expresa.

========================================================================


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

Ambas partes se reconocen mutuamente con capacidad suficiente para otorgar el presente contrato de ARRENDAMIENTO DE GARAJE y, a tal fin,

EXPONEN

I.- Que D./Dña. [NOMBRE Y APELLIDOS] es dueño de un aparcamiento subterráneo sito en [LOCALIDAD], calle [CALLE] con una superficie de [Nº] metros cuadrados, y referenciado con el nº [NÚMERO] de plaza de garaje del inmueble, según escritura de compraventa otorgada ante el notario D./Dña. [NOMBRE Y APELLIDOS] de esta ciudad y con nº [Nº] de protocolo [FECHA].

II.- Que D./Dña. [NOMBRE Y APELLIDOS] solicita se le arriende el referenciado garaje en el apartado anterior, a lo que accede el arrendador, rigiéndose por lo dispuesto en este contrato y supletoriamente por las reglas del Código Civil y lo llevan a efecto de conformidad con las siguientes,

CLÁUSULAS

Primera.- D./Dña. [NOMBRE Y APELLIDOS], cede en arrendamiento a D./Dña. [NOMBRE Y APELLIDOS], el aparcamiento subterráneo referenciado en escritura como plaza de garaje nº [NÚMERO] de la calle [CALLE], descrito en el apartado I. del presente documento, quién, a su vez, acepta en calidad de arrendatario.

Segunda.- Este arrendamiento supone única y exclusivamente, el de aparcamiento, en las condiciones que en cláusulas sucesivas se fijarán, sin derecho por parte del arrendatario a la prestación de servicio complementario alguno.

Tercera.- Este arrendamiento se pacta por un plazo de [Nº] años, en el que el arrendatario tendrá en todo momento derecho, durante este período contractual, a ocupar el aparcamiento referenciado como plaza de garaje nº [NÚMERO], para estacionar y colocar su vehículo.

Transcurrido el plazo señalado, el contrato dejará de tener vigencia.

Cuarta.- El precio o renta inicial de este contrato se fija en [IMPORTE] euros ([IMPORTE EN CIFRA] €) mensuales, pagaderas por meses adelantados, del 1 al 7 de cada mes, en la siguiente forma de pago: En la cuenta bancaria que el arrendador tiene abierta en la Entidad Bancaria [ENTIDAD BANCARIA] sucursal [SUCURSAL] en la calle [CALLE] de esta capital con número de cuenta [Nº DE CUENTA (IBAN)],siendo documento acreditativo del pago en cualquiera de las modalidades bancarias en las que realice el ingreso.

[ELEGIR UNA OPCIÓN: Si se incluyen los gastos en el precio o renta inicial / Si no se incluyen los gastos en el precio o renta inicial]

El recibo total de la renta llevará el incremento del [PORCENTAJE] % del Impuesto sobre el Valor Añadido, o el porcentaje que sea obligado en cada momento, de éste o de cualquier otro impuesto.

Quinta.- El arrendador no responderá del robo, hurto o desaparición tanto del vehículo aparcado en mencionado garaje, como de cualquier clase de objetos que pudiera dejar el arrendatario en el interior del mismo.

Sexta.- El arrendatario se compromete a respetar y cumplir todas las normas que sobre garajes tiene recogidas la comunidad mediante reglamento y que en este acto se entrega al arrendatario copia de las mismas.

Séptima.- El no uso del garaje por el arrendatario sea cual fuere el tiempo transcurrido, no dará derecho a devolución alguna del precio pactado.

[ELEGIR UNA OPCIÓN: Cabe subrogación / No cabe cesión ni subarriendo]

Novena.- El arrendatario no tendrá derecho de adquisición preferente en el caso de que el arrendador vendiese el inmueble, si bien el adquirente se subrogará en la posesión del arrendador hasta la fecha de conclusión del contrato.

Décima.- La plaza de garaje se destinará exclusivamente al estacionamiento de vehículos, sin que quepa ocupar dicha plaza con otra clase de bienes o enseres.

[ELEGIR UNA OPCIÓN: Si se pacta fianza / Si no se pacta fianza]

Decimosegunda.- El arrendador está obligado a realizar todas las reparaciones necesarias a fin de conservar la plaza de garaje en estado de servir al uso a que se destina. Así como también, a requerir a la comunidad de propietarios, a instancia del arrendatario, a la realización de las obras necesarias que puedan necesitar los elementos comunes.

Decimotercera.- Ante las posibles controversias que pudieren surgir en relación con el presente contrato, las partes acuerdan someterse a la tutela de los Tribunales de [LOCALIDAD].

Y leído el presente documento, ambas partes lo firman en señal de conformidad y ratificación de su contenido, haciéndolo por duplicado y a un solo efecto.

En [LUGAR], a [FECHA].

ARRENDADOR

ARRENDATARIO

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]
