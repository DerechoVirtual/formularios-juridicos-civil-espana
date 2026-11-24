---
name: contrato-arrendamiento-corner-centro-comercial-civ-0536
description: "Contrato de arrendamiento de un corner en centro comercial con prohibición de cesión y subarriendo. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de arrendamiento de un corner en centro comercial con prohibición de cesión y subarriendo

> Formulario **CIV-0536** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 24-11-2026.

## Qué es

Contrato de arrendamiento para uso distinto del de vivienda de un pequeño espacio (corner) dentro de un centro comercial, con prohibición expresa de cesión y subarriendo sin consentimiento escrito del arrendador. Se usa cuando el propietario del centro comercial cede a un comerciante un espacio delimitado para su actividad.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de arrendamiento de un corner en centro comercial con prohibición de cesión y subarriendo» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de arrendamiento de un corner en centro comercial con prohibición de cesión y subarriendo” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:contrato-arrendamiento-corner-centro-comercial-civ-0536`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (5 veces)
- [ ] DÍA (4 veces)
- [ ] PORCENTAJE (4 veces)
- [ ] AÑO (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] DNI/NIE (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] ESTADO CIVIL (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] IMPORTE EN LETRA (2 veces)
- [ ] MES (2 veces)
- [ ] PORCENTAJE O LO QUE SE PACTE (2 veces)
- [ ] PROFESIÓN (2 veces)
- [ ] ACTIVIDAD A DESARROLLAR
- [ ] DESCRIPCIÓN Y UBICACIÓN DEL ESPACIO
- [ ] FECHA
- [ ] FOLIO
- [ ] FORMA DE PAGO
- [ ] NOMBRE Y APELLIDOS DE LA PERSONA AUTORIZADA
- [ ] NOMBRE Y APELLIDOS DE LA PERSONA DESIGNADA
- [ ] NOMBRE, APELLIDOS Y DNI/NIE DE LOS FIADORES
- [ ] Nº DE FINCA
- [ ] PLAZO
- [ ] RÉGIMEN DE PUBLICIDAD PACTADO
- [ ] TOMO
- [ ] TÍTULO DE ADQUISICIÓN
- [ ] ÍNDICE O LO QUE SE PACTE

## Normas que cita el formulario

- art. 1581 Código Civil
- art. 30 LAU
- art. 31 LAU
- art. 34 LAU

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

- Junto a «…contrato y, en las sucesivas anualidades, el que corresponda al último aplicado.»: la actualización de rentas por el IPC debe ajustarse a la normativa vigente en el momento de la firma (en particular, los límites aplicables a la actualización de rentas y los índices de referencia que se establezcan); comprobar antes de firmar.

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

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO]

REUNIDOS

DE UNA PARTE,

[D./Dª NOMBRE Y APELLIDOS DEL ARRENDADOR], estado civil [ESTADO CIVIL], mayor de edad, profesión [PROFESIÓN], vecino/a de [LOCALIDAD], con domicilio en la calle [DOMICILIO] n.º [NÚMERO] y D.N.I. n.º [DNI/NIE] (1)

Y DE OTRA,

[D./Dª NOMBRE Y APELLIDOS DEL ARRENDATARIO], estado civil [ESTADO CIVIL], mayor de edad, profesión [PROFESIÓN], vecino/a de [LOCALIDAD], con domicilio en la calle [DOMICILIO] n.º [NÚMERO] y D.N.I. n.º [DNI/NIE]

Ambas partes intervienen en su propio nombre y derecho, reconociéndose, como así lo verifican en este acto, la mutua capacidad legal necesaria para la formalización del presente documento y, con su expreso consentimiento,

EXPONEN

I.- Que [D./Dª NOMBRE Y APELLIDOS DEL ARRENDADOR] es dueño/a del centro comercial que a continuación se indica, como consecuencia de título de [TÍTULO DE ADQUISICIÓN], constando inscrito en el Registro de la Propiedad de [LOCALIDAD], Tomo [TOMO], Folio [FOLIO], Finca [Nº DE FINCA]. La finca está libre de cargas y gravámenes y al corriente en el pago de impuestos, según declara el arrendador en este acto.

II.- Que [D./Dª NOMBRE Y APELLIDOS DEL ARRENDATARIO] solicita se le arriende el espacio ubicado en [DESCRIPCIÓN Y UBICACIÓN DEL ESPACIO] del mencionado centro comercial, en lo sucesivo el CORNER, a lo que accede el arrendador y lo llevan a efecto de conformidad con las siguientes

CLÁUSULAS

PRIMERA.– [D./Dª NOMBRE Y APELLIDOS DEL ARRENDADOR] cede en arrendamiento a [D./Dª NOMBRE Y APELLIDOS DEL ARRENDATARIO] el CORNER descrito en el apartado I del presente documento, quien a su vez acepta en calidad de arrendatario.

Este contrato se regirá por lo convenido por las partes en el mismo y, en defecto de pacto, por las normas del Título III de la Ley 29/1994, de 24 de noviembre, de Arrendamientos Urbanos, y supletoriamente por las disposiciones del Código Civil.

SEGUNDA.– El CORNER objeto del presente contrato será destinado por el arrendatario con carácter exclusivo y excluyente a [ACTIVIDAD A DESARROLLAR]. El arrendatario no podrá darle un uso distinto sin la previa autorización por escrito del arrendador.

TERCERA.– El precio o renta inicial de este contrato se fija en [IMPORTE EN LETRA] euros ([IMPORTE] €) mensuales, pagaderos por meses anticipados, del [DÍA] al [DÍA] de cada mes, en la siguiente forma de pago: [FORMA DE PAGO].

Será de cargo y cuenta del arrendatario el pago del Impuesto sobre el Valor Añadido vigente en cada momento. El tipo del IVA para el año presente es del [PORCENTAJE] %, cuyo pago se realizará conjuntamente con el de la renta y de la misma forma.

Sin perjuicio de lo dispuesto anteriormente, la demora en el pago de la renta obligará al arrendatario a abonar al arrendador el tipo legal de interés del dinero ([PORCENTAJE O LO QUE SE PACTE]) calculado sobre la renta en vigor.

Si llegado el vencimiento del contrato, o de su prórroga o reconducción, y requerido el arrendatario para la entrega del inmueble no la llevare a cabo, independientemente de las acciones que correspondan al arrendador para el desalojo de la finca, el arrendatario abonará a éste, como cláusula penal, la renta duplicada ([PORCENTAJE O LO QUE SE PACTE]) más el interés legal durante el tiempo que dure dicha situación.

CUARTA.– El presente arrendamiento se conviene y concierta por plazo de [PLAZO], a contar desde la celebración del presente contrato.

Extinguido el contrato por expiración del término fijado, ambas partes convienen que, de no mediar notificación dándolo por resuelto, se producirá su prórroga por tácita reconducción por los plazos señalados en el artículo 1581 del Código Civil.

QUINTA.– La renta total que satisfaga el arrendatario será actualizada en la misma proporción que lo haga el Índice General de Precios al Consumo, Conjunto Nacional, ([ÍNDICE O LO QUE SE PACTE]) durante los doce meses inmediatamente anteriores a la fecha de cada actualización, tomando como mes de referencia para la primera actualización el que corresponda al último índice publicado en la fecha de celebración del contrato y, en las sucesivas anualidades, el que corresponda al último aplicado.

Sin perjuicio de lo dispuesto anteriormente, la renta se aumentará anualmente hasta un [PORCENTAJE] % en el caso de que mediante la aplicación del Índice de Precios al Consumo no llegara a ese porcentaje, y si dicho índice excediera del [PORCENTAJE] %, se aplicaría este último.

SEXTA.– Obras, reparaciones e inspección.

El arrendatario deberá realizar las obras de decoración y acondicionamiento del CORNER, previa aprobación del arrendador, respetando en todo caso la limitación de su perímetro así como la naturaleza y conservación del centro comercial. A este fin, el arrendatario entrega al arrendador, como Anexo I a este contrato, el plano y la memoria detallando las obras a realizar, que, habiendo sido examinadas por el arrendador, habrán de ser respetadas en su ejecución. Cualquier eventual modificación de las mismas habrá de contar necesariamente con el visto bueno del arrendador. A estos efectos se comunicarán dichos cambios mediante [MEDIO: fax / correo electrónico / burofax / otros], debiendo la arrendadora contestar en el plazo de [NÚMERO] días, entendiéndose el silencio como negativa.

Las partes, con expresa renuncia a lo dispuesto en el artículo 30 de la LAU 1994, convienen que las obras de conservación del CORNER serán del [ELEGIR: arrendatario / arrendador], si bien su ejecución se llevará a cabo por el arrendador, y a tal efecto el arrendatario deberá permitir la entrada en el corner al arrendador, o a la persona que le represente y a sus operarios, a los solos fines de comprobar el estado del mismo o ejecutar las reparaciones.

Igualmente, el arrendatario deberá informar al arrendador de cualquier reparación que sea necesaria en el CORNER, bien por desperfectos o por siniestro.

Asimismo, la arrendadora se reserva el derecho de inspeccionar el CORNER en cualquier momento, designando como persona autorizada a tal efecto a [NOMBRE Y APELLIDOS DE LA PERSONA AUTORIZADA].

SÉPTIMA.– El arrendatario renuncia expresamente al tanteo y al retracto arrendaticios, excluyéndose la aplicación al presente contrato de lo dispuesto en el artículo 31 de la LAU 1994.

OCTAVA.– Cesión y subarriendo.

Se prohíbe expresamente al arrendatario la cesión o subarriendo del inmueble arrendado, total o parcialmente, sin consentimiento escrito del arrendador.

Se prohíbe el cambio de actividad sin la precitada autorización.

NOVENA.– Al fallecimiento del arrendatario se extinguirá el contrato, no autorizándose la subrogación en el mismo.

DÉCIMA.– El arrendatario renuncia expresamente al derecho de indemnización del artículo 34 de la LAU 1994.

UNDÉCIMA.– En este acto, el arrendatario entrega al arrendador la cantidad de [IMPORTE EN LETRA] euros ([IMPORTE] €), importe igual al de dos mensualidades de renta, en concepto de fianza y garantía adicional, que será restituida, en su integridad o disminuida en la cantidad que sea necesaria en caso de daños, a la finalización de este contrato.

DUODÉCIMA.– Con independencia de la fianza en metálico, se constituyen en fiadores solidarios, con expresa renuncia al beneficio de excusión y división, del fiel cumplimiento de las obligaciones del contrato, los siguientes fiadores: [NOMBRE, APELLIDOS Y DNI/NIE DE LOS FIADORES].

DECIMOTERCERA.– El horario y calendario de apertura y cierre del CORNER se ajustará a los previstos para el centro comercial. Cada año el arrendador notificará al arrendatario dicho horario y calendario antes del [FECHA]. El horario y calendario para [AÑO] son los que constan en el Anexo II.

Queda prohibida la permanencia en el centro comercial o CORNER de cualquier persona, incluido el arrendatario, fuera de los horarios de apertura del centro comercial, excepto cuando se trate de aquéllas autorizadas para la satisfacción de los servicios comunes.

Las zonas comunes de servicios y accesos al CORNER podrán ser utilizadas por la arrendataria y su personal en los mismos términos que el personal de la arrendadora y el público en general.

DECIMOCUARTA.– El importe de suministro de electricidad y línea telefónica y acceso a Internet del CORNER se calculará mediante el cálculo efectuado por sus propios contadores y contratos con las correspondientes empresas suministradoras, y correrá a cargo del arrendatario.

En cuanto a la repercusión de gastos por zonas comunes y limpieza y mantenimiento del centro comercial, se acuerda [ELEGIR: que se halla incluido en el canon arrendaticio / que será repercutido por la arrendadora al arrendatario mediante desglose mensual y proporcional al coste total para la superficie del centro en relación con la superficie del CORNER, esto es, un [PORCENTAJE] % a fecha de la celebración del presente contrato].

DECIMOQUINTA.– [Nota: puede pactarse que el régimen de publicidad corra por cuenta de la arrendadora, o de la arrendataria, o un sistema mixto en que la arrendataria deba aprobar cualquier cambio en la misma en los mismos términos previstos para las obras u ornamentación del CORNER según la cláusula sexta.]

[RÉGIMEN DE PUBLICIDAD PACTADO].

La arrendataria se obliga a mantener iluminado su CORNER y rótulo durante las horas de apertura al público descritas en la cláusula decimotercera.

DECIMOSEXTA.– La arrendataria se obliga a regularizar y mantener legalmente al día la situación laboral del personal contratado para su CORNER, que se entenderá en todo caso contratado por dicha entidad y sin relación jurídica de ningún tipo con la arrendadora, que sólo extenderá a estos efectos su facultad de inspección y acceso a la documentación a fin de garantizar el cumplimiento por parte de dicha arrendataria de sus obligaciones en materia de contratación laboral. La arrendataria se obliga a mostrar cuantas veces sea preciso dicha documentación previo requerimiento de la arrendadora efectuado a través de la persona designada al efecto [NOMBRE Y APELLIDOS DE LA PERSONA DESIGNADA].

[Nota: puede pactarse, alternativamente, que el personal sea personal de la arrendadora y entonces sea ésta quien haya de cumplir las obligaciones en materia de Derecho Laboral.]

DECIMOSÉPTIMA.– Serán de cuenta del [ELEGIR: arrendatario / arrendador / lo que se pacte] el Impuesto sobre Bienes Inmuebles del CORNER y cualesquiera otros nuevos arbitrios, tasas, impuestos, contribuciones especiales, así como los tributos del Estado, Comunidad Autónoma, Provincia, Municipio o cualquier otro organismo oficial que se creasen o modificasen.

Y leído el presente documento, ambas partes lo firman en señal de conformidad y ratificación de su contenido, haciéndolo por duplicado y a un solo efecto.

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO]

Firma de EL/LA ARRENDADOR/A: ______________________

Firma de EL/LA ARRENDATARIO/A: ______________________

NOTA (1): La Ley de Arrendamientos Urbanos de 24 de noviembre de 1994 abandona la distinción tradicional entre arrendamientos de vivienda y arrendamientos de locales de negocio y asimilados, para diferenciar entre arrendamientos de vivienda (permanente) y arrendamientos para usos distintos al de vivienda (segunda residencia, de temporada, local de negocio, oficinas y despachos, almacenes, etc.), estableciendo que estos últimos se regirán por la voluntad de las partes y, en su defecto, por las normas del Título III de la Ley y, supletoriamente, por las normas sobre arrendamientos del Código Civil. Por lo tanto, únicamente entrará en juego lo dispuesto en el Título III si las partes no han pactado o lo han hecho insuficientemente sobre los elementos del contrato. En consecuencia, las partes podrán excluir cada uno de los supuestos que regula el Título III de la LAU si no quieren que les sean de aplicación al contrato dichas normas. En definitiva, la LAU deja al libre pacto de las partes todos los elementos del contrato de los arrendamientos para uso distinto del de vivienda, configurándose una regulación supletoria del libre pacto que permite también un amplio recurso al régimen del Código Civil.
