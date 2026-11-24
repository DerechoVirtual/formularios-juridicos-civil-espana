---
name: contrato-arras-penitenciales-facultad-desistir-civ-0800
description: "Contrato de arras penitenciales con facultad de desistir. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de arras penitenciales con facultad de desistir

> Formulario **CIV-0800** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de arras penitenciales con facultad de desistir» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de arras penitenciales con facultad de desistir” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:contrato-arras-penitenciales-facultad-desistir-civ-0800`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] LOCALIDAD (7 veces)
- [ ] FECHA (5 veces)
- [ ] IMPORTE (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] NOMBRE DEL REPRESENTADO/A (2 veces)
- [ ] Nº (2 veces)
- [ ] Nº DE PROTOCOLO (2 veces)
- [ ] CALLE
- [ ] DIRECCIÓN
- [ ] DOMICILIO
- [ ] FOLIO
- [ ] LIBRO
- [ ] LUGAR
- [ ] MES
- [ ] PLAZO
- [ ] TIPO DE INMUEBLE
- [ ] TOMO

## Normas que cita el formulario

- art. 1.454 Código Civil
- art. 1454 Código Civil

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

Reunidos

De una parte:

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda / unión de hecho], con documento nacional de identidad número

De otra:

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda / unión de hecho], vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número

Intervienen

D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de [NOMBRE DEL REPRESENTADO/A], en lo sucesivo "LA VENDEDORA", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D./Dña. [NOMBRE Y APELLIDOS], en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO], poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD] y vigente, según manifiesta.

D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de [NOMBRE DEL REPRESENTADO/A], en lo sucesivo "LA COMPRADORA", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D./Dña. [NOMBRE Y APELLIDOS], en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO], poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD] y vigente, según manifiesta.

Todas las partes, en el respectivo carácter con el que intervienen, se reconocen mutuamente la capacidad legal en Derecho necesaria para concertar el presente CONTRATO DE ARRAS PENITENCIALES, y a tal efecto, libremente y de común acuerdo,

Exponen

Primero.– Que LA VENDEDORA es titular en pleno dominio del inmueble sito en el municipio de [LOCALIDAD] ubicada en el número [NÚMERO] de la Calle [CALLE] que a continuación se describe:

– Inmueble [TIPO DE INMUEBLE] situado en [DIRECCIÓN] número [NÚMERO] de [LOCALIDAD], cuyos datos registrales son los siguientes: Finca número [NÚMERO], inscrita en el Tomo [TOMO], Libro [LIBRO], Folio [FOLIO], constando una superficie de [Nº] metros cuadrados útiles de dicha vivienda en la inscripción registral.
– Corresponde a LA VENDEDORA el 100% del pleno dominio de la totalidad de la finca.

Segundo.– Que el inmueble descrito en el Exponendo I de este documento se halla libre de cargas, al corriente de impuestos y de toda clase de pagos a la comunidad de propietarios, según manifiesta LA VENDEDORA.

Tercero.– Que ambas partes conciertan estas arras y la futura compraventa de la finca descrita en el Expositivo I, por lo que, de mutuo acuerdo, formalizan el presente contrato, el cual se regirá por las siguientes.

CLÁUSULAS

Precio.–

El precio de venta del inmueble descrito en el Exponendo primero se concreta de común acuerdo en la cantidad de [IMPORTE] euros ( €).

Ambas partes convienen que la firma de la escritura de compraventa y entrega de llaves tendrá lugar en fecha [FECHA] a determinar por la parte COMPRADORA entre la del otorgamiento de este contrato y el próximo día [FECHA] de [MES] de

A tal efecto, la parte COMPRADORA dirigirá requerimiento a la VENDEDORA para el otorgamiento de la escritura pública de compraventa. En dicha comunicación, que se remitirá a la dirección indicada en este documento, la parte COMPRADORA indicará la fecha, hora y lugar señalados para el otorgamiento de la escritura.

Entre el requerimiento y la fecha escogida deberá mediar un plazo de [PLAZO], al menos [Nº] días naturales.

La VENDEDORA otorgará la escritura de compraventa del inmueble, libre de cargas, a favor de COMPRADORA ante el Notario que designe ésta y aportará los títulos de propiedad inscritos y demás documentos precisos para tal otorgamiento.

Arras penitenciales.–

La PARTE COMPRADORA entrega en este acto a la PARTE VENDEDORA, en metálico, la suma de [IMPORTE] € sirviendo el presente documento como el más eficaz recibo y carta de pago.

La cantidad entregada lo es en concepto de arras penitenciales, conforme a lo dispuesto en el artículo 1.454 del Código Civil, sin perjuicio de que será descontada del total precio de compra pactado en la estipulación anterior, pudiendo rescindirse este contrato allanándose la COMPRADORA a perder las arras, o la VENDEDORA a devolverlas duplicadas.

En consecuencia, y de acuerdo al citado art. 1454 del Código Civil, si la compraventa no pudiera formalizarse antes del día señalado como término final en la estipulación anterior por causa imputable a la COMPRADORA, ésta perderá la cantidad entregada como señal, que quedará en beneficio de la VENDEDORA.

Si la compraventa no pudiera formalizarse antes del día señalado como término final por causa imputable a la VENDEDORA, ésta se obliga a devolver a la COMPRADORA el duplo del importe recibido como señal.

En el caso de formalizarse la compraventa, el resto del precio pactado que asciende a [IMPORTE] EUROS ( €), serán satisfechos por la PARTE COMPRADORA a la PARTE VENDEDORA, a la firma de la escritura pública.

Transmisión y entrega de la posesión del inmueble.–

En caso de formalizarse la compraventa, LA VENDEDORA hará entrega de la posesión de la finca objeto de este contrato a LA COMPRADORA en el acto del otorgamiento de la escritura con la entrega de llaves de la misma.

La vivienda se transmitirá libre de todo tipo de cargas y gravámenes y al corriente de pago de impuestos, arbitrios y gastos de Comunidad de Propietarios, así como libre de cualquier clase de ocupantes.

Gastos e impuestos.–

Todos los gastos e impuestos derivados de la compraventa serán abonados según ley.

Jurisdicción competente y ley aplicable.–

Para cuantas cuestiones o divergencias pudieran suscitarse en relación con el presente contrato, la competencia de los Tribunales que deban conocer del asunto se determinará de conformidad con los criterios de competencia objetiva, funcional y territorial legalmente aplicables.

El presente contrato tiene exclusivamente carácter civil y se regirá por sus propias cláusulas, y en lo en ellas no dispuesto, por lo previsto en el Código Civil y, demás leyes especiales.

Notificaciones.–

Toda notificación que se efectúe entre las partes se hará por escrito y será entregada personalmente o de cualquier otra forma que certifique la recepción por la parte notificada en los respectivos domicilios indicados en el encabezamiento de este Contrato.

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

Y en prueba de conformidad y aceptación de cuanto antecede, ambas partes firman los folios del presente CONTRATO DE ARRAS PENITENCIALES extendido por duplicado y a un solo efecto, en la ciudad y fecha mencionados en el encabezamiento.

Vendedor/a	Comprador/a

Ffo. D./Dña. [NOMBRE Y APELLIDOS]: Ffo. D./Dña. [NOMBRE Y APELLIDOS]:

========================================================================
