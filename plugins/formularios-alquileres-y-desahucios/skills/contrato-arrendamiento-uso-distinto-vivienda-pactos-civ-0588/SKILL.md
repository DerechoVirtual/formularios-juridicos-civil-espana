---
name: contrato-arrendamiento-uso-distinto-vivienda-pactos-civ-0588
description: "Contrato de arrendamiento de uso distinto de vivienda con pactos sobre cesión y subarriendo. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de arrendamiento de uso distinto de vivienda con pactos sobre cesión y subarriendo

> Formulario **CIV-0588** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 24-11-2026.

## Qué es

Contrato de arrendamiento para uso distinto del de vivienda contemplando como opción la existencia de pactos específicos sobre cesión y subarriendo, así como la previsión de una cláusula de prohibición expresa de los mismos.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de arrendamiento de uso distinto de vivienda con pactos sobre cesión y subarriendo» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de arrendamiento de uso distinto de vivienda con pactos sobre cesión y subarriendo” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:contrato-arrendamiento-uso-distinto-vivienda-pactos-civ-0588`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] PORCENTAJE (6 veces)
- [ ] IMPORTE (4 veces)
- [ ] Nº (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] CONSECUENCIA PACTADA (2 veces)
- [ ] FECHA (2 veces)
- [ ] GASTOS A CARGO DEL ARRENDATARIO (2 veces)
- [ ] IMPORTE EN CIFRA (2 veces)
- [ ] LUGAR (2 veces)
- [ ] SERVICIOS Y SUMINISTROS (2 veces)
- [ ] TIPO DE INTERÉS (2 veces)
- [ ] ÍNDICE DE REFERENCIA (2 veces)
- [ ] ACTIVIDAD
- [ ] FOLIO
- [ ] LOCALIDAD
- [ ] NIF/DNI
- [ ] PLAZO
- [ ] TOMO

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

### Avisos de actualización (0) — se aplican en el texto, nunca se copian en el documento

- Ninguno.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Contrato de arrendamiento para uso distinto del de vivienda contemplando como opción la existencia de pactos específicos sobre cesión y subarriendo, así como la previsión de una cláusula de prohibición expresa de los mismos.

Notas al pie del formulario original:
(1) La Ley de Arrendamientos Urbanos de 24 de noviembre de 1994 abandona a la distinción tradicional entre arrendamientos de vivienda y arrendamientos de locales de negocio y asimilados, para diferenciar entre arrendamientos de vivienda (permanente) y arrendamientos para usos distintos al de vivienda (segunda residencia, de temporada, local de negocio, oficinas y despachos, almacenes, etc.), estableciendo que estos últimos se regirán por la voluntad de las partes y en su defecto por las normas del Título III de la Ley y, supletoriamente, por las normas sobre arrendamientos del Código Civil. Por lo tanto, únicamente entrará en juego lo dispuesto en el Título III si las partes no han pactado o lo han hecho insuficientemente sobre los elementos del contrato. En consecuencia las partes podrán excluir cada uno de los supuestos que regula el Título III de la LAU si no quieren que le sean de aplicación al contrato dichas normas. En definitiva, la LAU deja al libre pacto de las partes todos los elementos del contrato de los arrendamientos para uso distinto del de vivienda, configurándose una regulación supletoria del libre pacto que permite también un amplio recurso al régimen del Código Civil.

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

En [LUGAR], a [FECHA].

REUNIDOS

DE UNA PARTE,

Don/Doña [NOMBRE Y APELLIDOS], mayor de edad, con domicilio en.., número [NÚMERO], provisto de N.I.F.

Y DE OTRA,

Don/Doña [NOMBRE Y APELLIDOS], mayor de edad, con domicilio en. [NÚMERO], número [NÚMERO], provisto de N.I.F. [NIF/DNI]

Ambas partes intervienen en su propio nombre y derecho, reconociéndose, como así lo verifican en este acto, la mutua capacidad legal necesaria para la formalización del presente documento y, con su expreso consentimiento,

EXPONEN

I.- Que D./Dña. [NOMBRE Y APELLIDOS] es dueño de la finca que a continuación se indica, como consecuencia de título de compraventa, constando inscrita en el Registro de la Propiedad de [LOCALIDAD], Tomo [TOMO] Folio [FOLIO] Finca

La finca está libre de cargas y gravámenes y al corriente en el pago de impuestos, según declara el arrendador en este acto.

II.- Que el Sr./a. D./Dña. [NOMBRE Y APELLIDOS], solicita se le arriende el mencionado inmueble, a lo que accede el arrendador y lo llevan a efecto de conformidad con las siguientes,

CLAUSULAS

PRIMERA.- D./Dña. [NOMBRE Y APELLIDOS] cede en arrendamiento a D./Dña. [NOMBRE Y APELLIDOS] el inmueble descrito en el apartado I del presente documento, quien a su vez acepta en calidad de arrendatario.

Este contrato se regirá por lo convenido por las partes en el mismo y en defecto de pacto, por las normas del Título III de la Ley 29/1994 de 24 de noviembre, de Arrendamientos Urbanos y supletoriamente por las disposiciones del Código Civil.

SEGUNDA.- El inmueble objeto del presente contrato será destinado por el arrendatario con carácter exclusivo y excluyente a [ACTIVIDAD]

El arrendatario no podrá darle un uso distinto sin la previa autorización por escrito del arrendador.

TERCERA.- El precio o renta inicial de este contrato se fija en [IMPORTE] euros ([IMPORTE EN CIFRA] €) mensuales, pagaderas por meses anticipados, del [Nº] al [Nº] de cada mes, en la siguiente forma de pago:

Será de cargo y cuenta del arrendatario el pago del Impuesto sobre el Valor Añadido vigente en cada momento.

El tipo del IVA para el año presente es del [PORCENTAJE] %, cuyo pago se realizará conjuntamente con el de la renta y de la misma forma.

Sin perjuicio de lo dispuesto anteriormente, la demora en el pago de la renta obligará al arrendatario a abonar al arrendador el tipo legal de interés del dinero ( [TIPO DE INTERÉS] o lo que se pacte [TIPO DE INTERÉS]) calculado sobre la renta en vigor.

Si llegado el vencimiento del contrato, o de su prórroga o reconducción y requerido el arrendatario para la entrega del inmueble no la llevare a cabo, independientemente de las acciones que correspondan al arrendador para el desalojo de la finca, el arrendatario abonará a éste, como cláusula penal, la renta duplicada ( [IMPORTE] o lo que se pacte [IMPORTE]) más el interés legal durante el tiempo que dure dicha situación.

CUARTA.- El presente arrendamiento se conviene y concierta por plazo de [PLAZO], a contar desde la celebración del presente contrato.

Extinguido el contrato por expiración del término fijado, ambas parten convienen que, de no mediar notificación dándolo por resuelto, se producirá su prórroga por tácita reconducción por los plazos señalados en el artículo 1581 del Código Civil.

QUINTA.- La renta total que satisfaga el arrendatario será actualizada en la misma proporción que lo haga el Índice General de Precios al Consumo, Conjunto Nacional, ( [ÍNDICE DE REFERENCIA] o lo que se pacte [ÍNDICE DE REFERENCIA]) durante los doce meses inmediatamente anteriores a la fecha de cada actualización, tomando como mes de referencia para la primera actualización, el que corresponda al último índice publicado en la fecha de celebración del contrato y en las sucesivas anualidades el que corresponda al último aplicado.

Sin perjuicio de lo dispuesto anteriormente, la renta se aumentará anualmente hasta un [PORCENTAJE] % en el caso de que mediante la aplicación del Índice de Precios al Consumo no llegara a ese porcentaje, y si dicho índice excediera del [PORCENTAJE] %, se aplicaría este último.

SEXTA.- El arrendatario deberá conservar el inmueble arrendado en el estado en que se recibe durante el tiempo de duración del contrato.

Las partes, con expresa renuncia a lo dispuesto en el artículo 30 de la LAU 1994, convienen que las obras de conservación del inmueble arrendado y de los servicios, serán del arrendatario (o del arrendador, si así se pacta), si bien su ejecución se llevará a cabo por el arrendador, y a tal efecto el arrendatario deberá permitir la entrada en el inmueble arrendado al arrendador, o a la persona que le represente y a sus operarios, a los solos fines de comprobar el estado del inmueble arrendado o ejecutar las reparaciones.

SÉPTIMA.- El arrendatario renuncia expresamente al tanteo y al retracto arrendaticios, excluyéndose la aplicación al presente contrato de lo dispuesto en el artículo 31 de la LAU 1994.

OCTAVA.- La enajenación del inmueble arrendado dará lugar, bien sea a título oneroso o gratuito, a la extinción del contrato ( [CONSECUENCIA PACTADA] o a lo que se pacte [CONSECUENCIA PACTADA]) a los [Nº] días naturales siguientes en que el arrendador notifique la enajenación al arrendatario, sin derecho a indemnización.

NOVENA.- Cesión y subarriendo

[OPCIONAL — en caso de que se desee incluir prohibición expresa de cesión o subarriendo]

Se prohíbe expresamente al arrendatario la cesión o subarriendo del inmueble arrendado total o parcialmente, sin consentimiento escrito del arrendador.

Se prohíbe el cambio de actividad sin la precitada autorización.

[OPCIONAL — en caso de que se desee incluir pactos sobre cesión y subarriendo]

Se autoriza al arrendatario el traspaso a tercero del negocio mediante precio y sin existencias. El traspaso estará sujeto a las siguientes condiciones para su validez:

1) Deberá notificarse fehacientemente al arrendador con un mes de anterioridad a su realización. En dicha notificación se indicará el precio del traspaso y la persona del cesionario, pudiendo el arrendador ejercer el derecho de tanteo dentro del mencionado plazo, por el precio que se comunique. El incumplimiento del deber de notificación dará lugar a la resolución del contrato.
2) El cesionario asumirá el cumplimiento de las obligaciones pendientes del arrendatario, como consecuencia del contrato de arrendamiento.
3) El arrendatario responderá del cumplimiento de las obligaciones del cesionario frente al arrendador como consecuencia del contrato de arrendamiento.
4) El arrendador tendrá derecho a un [PORCENTAJE] % del precio del traspaso.
5) El arrendador tendrá derecho a elevar la renta un [PORCENTAJE] %.
6) No se permite el traspaso para el ejercicio de actividades docentes o para el ejercicio de actividades de la Administración pública.

Se autoriza al arrendatario a subarrendar a tercero el inmueble objeto del arrendamiento.

El arrendador tendrá derecho al [PORCENTAJE] % del importe de la renta del subarriendo.

El arrendatario responderá del cumplimiento de las obligaciones del subarrendatario frente al arrendador como consecuencia del contrato de subarriendo.

Se considera subarriendo si los accionistas actuales de la sociedad arrendataria dejaren de ser mayoritarios en dicha sociedad (se señalarán quienes son los titulares de las acciones y el número de éstas)

En caso de fusión, escisión, transformación o absorción se entenderá que ha habido traspaso, salvo que fuere por disposición legal.

No se permite el subarriendo para el ejercicio de actividades por la Administración Pública.

DÉCIMA.- Al fallecimiento del arrendatario se extinguirá el contrato, no autorizándose la subrogación en el mismo.

UNDÉCIMA.- El arrendatario renuncia expresamente al derecho de indemnización del artículo 34 de la LAU 1994.

DUODÉCIMA.- Todos los servicios y suministros del inmueble ( [SERVICIOS Y SUMINISTROS] o lo que se pacte [SERVICIOS Y SUMINISTROS]) individualizados o no, serán de cuenta del arrendatario, así como los gastos de su conservación, y los que ocasionen las reparaciones de los mismos, bien por interés justificado de la propiedad, bien por exigirse por la Ley o por las Compañías suministradoras.

DECIMOTERCERA.- En este acto, el arrendatario entrega al arrendador la cantidad de [IMPORTE] euros ([IMPORTE EN CIFRA] €), importe igual al de dos mensualidades de renta, en concepto de fianza y garantía adicional, que será restituida, en su integridad o disminuida en la cantidad que sea necesaria en caso de daños, a la finalización de este contrato.

DECIMOCUARTA.- Con independencia de la fianza en metálico, se constituyen en fiadores solidarios, con expresa renuncia al beneficio de excusión y división, del fiel cumplimiento de las obligaciones del contrato, los siguientes fiadores:

DECIMOQUINTA.- En este acto el arrendador entrega al arrendatario los juegos de llaves del mencionado inmueble, el cual se halla en perfecto estado de conservación, con todos sus servicios e instalaciones igualmente en perfecto estado de conservación y utilización.

DECIMOSEXTA.- Serán de cuenta del arrendatario ( [GASTOS A CARGO DEL ARRENDATARIO] o lo que se pacte [GASTOS A CARGO DEL ARRENDATARIO]) el Impuesto sobre bienes inmuebles de la finca arrendada y cualesquiera otros nuevos arbitrios, tasas, impuestos, contribuciones especiales, así como los tributos del Estado, Comunidad Autónoma, Provincia, Municipio o cualquier otro Organismo Oficial que se creasen o modificasen.

Y leído el presente documento, ambas partes lo firman en señal de conformidad y ratificación de su contenido, haciéndolo por duplicado y a un sólo efecto.

En [LUGAR], a [FECHA].

Firma de EL/LA ARRENDADOR/A:

Firma de LA ARRENDATARIA
