---
name: contrato-arrendamiento-vivienda-avalista-clausula-civ-0506
description: "Contrato de arrendamiento de vivienda con avalista o cláusula de garantía del inquilino. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de arrendamiento de vivienda con avalista o cláusula de garantía del inquilino

> Formulario **CIV-0506** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 24-11-2026.

## Qué es

Contrato de arrendamiento de vivienda con avalista o con cláusula de garantía para el cumplimiento de las obligaciones por parte del arrendatario, con inclusión de cláusulas y condiciones genéricas así como de los derechos y obligaciones de ambas partes. Adaptado al Real Decreto-Ley 7/2019, de 1 de marzo, de medidas urgentes en materia de vivienda y alquiler (contratos posteriores a 6 de marzo de 2019).

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de arrendamiento de vivienda con avalista o cláusula de garantía del inquilino» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de arrendamiento de vivienda con avalista o cláusula de garantía del inquilino” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:contrato-arrendamiento-vivienda-avalista-clausula-civ-0506`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (14 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] CALLE (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] ESTADO CIVIL (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] PROFESIÓN (2 veces)
- [ ] DATOS REGISTRALES
- [ ] FECHA
- [ ] LUGAR
- [ ] NOMBRE DE LA SUCURSAL
- [ ] Nº
- [ ] Nº DE CUENTA (IBAN)

## Normas que cita el formulario

- art. 9 LAU
- art. 10 LAU
- art. 21 LAU
- art. 36.5 LAU
- art. 1.851 Código Civil

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

En [LUGAR], a [FECHA].

REUNIDOS

DE UNA PARTE,

D./Dña. [NOMBRE Y APELLIDOS], estado civil [ESTADO CIVIL], mayor de edad, profesión [PROFESIÓN], vecino de [LOCALIDAD], con domicilio en la calle [CALLE] y D.N.I. nº [NÚMERO].

Y DE OTRA,

D./Dña. [NOMBRE Y APELLIDOS], estado civil [ESTADO CIVIL], mayor de edad, profesión [PROFESIÓN], vecino de [LOCALIDAD], con domicilio en la calle [CALLE] y D.N.I. nº [NÚMERO].

Ambas partes intervienen en su propio nombre y derecho, reconociéndose, como así lo verifican en este acto, la mutua capacidad legal necesaria para la formalización del presente documento, y, con su expreso consentimiento

EXPONEN

I.- Que D./Dña. [NOMBRE Y APELLIDOS] es dueño de la finca que a continuación se indica, como consecuencia de título de compraventa, constando inscrita en el Registro de la Propiedad de [LOCALIDAD], al [DATOS REGISTRALES], de la casa sita en [LOCALIDAD], Calle [CALLE], con una superficie de [Nº] metros cuadrados, lindando a la izquierda con la finca propiedad de D./Dña. [NOMBRE Y APELLIDOS], a la derecha con la finca propiedad de D./Dña. [NOMBRE Y APELLIDOS], estando libre de cargas y gravámenes y al corriente en el pago de impuestos, según declara el arrendador en este acto.

II.- Que el D./Dña. [NOMBRE Y APELLIDOS], solicita se le arriende el mencionado inmueble, a lo que accede el arrendador y lo llevan a efecto de conformidad con las siguientes,

CLÁUSULAS

Primera.- D./Dña. [NOMBRE Y APELLIDOS], cede en arrendamiento a D./Dña. [NOMBRE Y APELLIDOS], el piso descrito en el apartado I. del presente documento, quien a su vez acepta en calidad de arrendatario.

Segunda.- El presente arrendamiento se conviene y concierta por plazo de UN AÑO, a contar desde la celebración del presente contrato, prorrogable, a voluntad de la arrendataria, por periodos anuales sucesivos hasta un periodo de cinco años en total, conforme al régimen previsto en el artículo 9 LAU 1994.

Tercera.- De conformidad con el artículo 10 LAU 1994, una vez transcurrido este plazo de cinco años (o de siete años si el arrendador fuese persona jurídica), si ninguna de las partes notifica a la otra, al menos con cuatro meses de antelación, su voluntad de no renovarlo, el contrato se prorrogará obligatoriamente por plazos anuales hasta un máximo de tres años más, salvo que el arrendatario manifieste al arrendador con un mes de antelación a la fecha de terminación de cualquiera de las anualidades, su voluntad de no renovar.

Al contrato prorrogado le seguirá siendo de aplicación el régimen establecido en el presente contrato.

Finalizada la duración pactada y, en su caso, la de las prórrogas sucesivas, el arrendatario deberá aban

D./Dña. [NOMBRE Y APELLIDOS] ar el inmueble, sin necesidad de requerimiento expreso del arrendador, dejándolo en el mismo estado en que se encontraba al ocuparlo, con la excepción del desgaste debido al uso habitual de la vivienda.

Cuarta.- El precio o renta inicial de este contrato se fija en [IMPORTE] euros ( €) mensuales, pagaderas por meses adelantados, del 1 al 7 de cada mes, en la siguiente forma de pago: En la cuenta bancaria que el arrendador tiene abierta en la entidad bancaria sucursal [NOMBRE DE LA SUCURSAL] en la calle de esta capital con número de cuenta [Nº DE CUENTA (IBAN)], documento acreditativo del pago en cualquiera de las modalidades bancarias en las que realice el ingreso conforme a la Ley de Arrendamientos Urbanos.

Quinta.- En este acto, el arrendatario entrega, al arrendador, la cantidad de [IMPORTE] euros ( €), importe igual al de una mensualidad de renta, en concepto de fianza y garantía adicional, que será restituida, en su integridad o disminuirá en la cantidad que sea necesaria en caso de daños, a la finalización de este contrato.

La existencia de ésta fianza, no será obstáculo para que la parte arrendadora pueda instar el desahucio por falta de pago, ni facultará al arrendatario al impago de alguna mensualidad de renta. La fianza no devengará interés a favor del arrendatario, quedando facultada la parte arrendadora para practicar la liquidación hacedera según los perjuicios que hubieren causado.

Sexta.- En este acto el arrendador entrega al arrendatario los juegos de llaves del mencionado inmueble, el cual se halla en perfecto estado de conservación, con todos sus servicios igualmente en perfecto estado de conservación y utilización.

Séptima.- Son obligaciones del arrendatario:

1.- Pagar la renta que proceda conforme a lo convenido en este contrato.
2.- Usar el inmueble para la actividad de vivienda.
3.- Pagar los gastos de suministros tales como luz, agua, gas o teléfono que correspondan al inmueble arrendado. así como los generados para el adecuado sostenimiento del inmueble, sus servicios, tributos, cargas, etc.
4.- Permitir la entrada de la parte arrendadora o representantes suyos o administrador, para todo cuanto guarde relación con el inmueble.
5.- Extinguido el arriendo por cualquier causa, el arrendatario devolverá la posesión del piso en buen estado, con las mejoras que en su caso se hagan y que quedarán en beneficio de la propiedad, sin indemnización.
6.- El arrendatario podrá realizar en la vivienda cuyo uso se le cede, las obras que considere necesarias para su instalación, pero en ningún caso podrá alterar la configuración de la vivienda o provocar o contribuir a disminuir su estabilidad o seguridad, para cuyas obras necesitará consentimiento expreso y por escrito del arrendador. y todo ello de conformidad con los artículos 21, 22, 23, 24 y 26 de la LAU 1994.

Octava.- La renta será revisada anualmente de acuerdo con la variación porcentual experimentada por el Índice General Nacional del Sistema de Índices de Precios de Consumo en un período de doce meses inmediatamente anteriores a la fecha de cada actualización, tomando como mes de referencia para la primera actualización el que corresponda al último índice que estuviera publicado en la fecha de celebración del contrato, y en las sucesivas el que corresponda al último aplicado.

Publicado el índice correspondiente al mes de la actualización, el arrendador comunicará al arrendatario de forma fehaciente su voluntad de actualizar la renta conforme a lo establecido legalmente, expresando la cantidad en que se fija la renta revisada, y adjuntando certificación del Instituto Nacional de Estadística.

La base sobre la que se efectuará la citada revisión será la renta que se pague el mes inmediatamente anterior a la fecha de revisión.

Novena.- D./Dña. [NOMBRE Y APELLIDOS], provisto de D.N.I. número [NÚMERO],y presente en este acto, se constituye en fiador o avalista de las obligaciones contraídas por el arrendatario, D./Dña. [NOMBRE Y APELLIDOS], con el arrendador, por todo lo estipulado en este contrato, obligándose solidariamente con el arrendatario al cumplimiento de las obligaciones arrendaticias y especialmente al pago de la renta, así como a cualquier cantidad económica que se derive del presente contrato o por disposición legal, y conservación del buen estado de la vivienda por toda la duración del contrato, con la limitación establecida en el artículo 36.5 LAU 1994, con renuncia expresa a los beneficios de excusión, división, firmando conjuntamente con el arrendatario este contrato en prueba de aceptación y conformidad, y a tal efecto, acepta de antemano cualquier prórroga o renovación que el arrendador pudiera conceder, sea cual sea la forma en que se instrumente la misma, sin que, en consecuencia, la concesión de la indicada prórroga o renovación pueda producir los efectos establecidos en el artículo 1.851 del Código Civil.

Décima.- Las partes acuerdan que no habrá derecho de subrogación en caso de fallecimiento del arrendatario cuando este tenga lugar transcurridos los tres primeros años de duración del arrendamiento.

Undécima.- En caso de incumplimiento, serán de cargo del arrendatario todos los gastos y costas judiciales y extrajudiciales que origine su incumplimiento, incluso honorarios de Letrado y Procurador aunque la intervención de éstos no fuere preceptiva.

Duodécima.- Cualquiera de las partes podrá solicitar la inscripción del presente arrendamiento en el Registro de la Propiedad, gasto que correrá a cargo del que lo solicite.

Decimotercera.- En cumplimiento de lo dispuesto en el Real Decreto 390/2021, de 1 de junio, por el que se aprueba el procedimiento básico para la certificación de la eficiencia energética de los edificios, se pone a disposición del arrendatario en este acto el certificado de eficiencia energética, emitido por técnico competente.

Decimocuarta.- En todo lo no previsto en el presente contrato, se acudirá a lo dispuesto en el Título II de la Ley de Arrendamientos Urbanos de 24 de Noviembre de 1.994.

Y leído el presente documento, ambas partes lo firman en señal de conformidad y ratificación de su contenido, haciéndolo por duplicado y a un solo efecto.

EL/LA ARRENDADOR/A:

EL/LA ARRENDATARIO/A:
D./Dña. [NOMBRE Y APELLIDOS] D./Dña. [NOMBRE Y APELLIDOS]

EL AVALISTA:

D./Dña. [NOMBRE Y APELLIDOS]

========================================================================
