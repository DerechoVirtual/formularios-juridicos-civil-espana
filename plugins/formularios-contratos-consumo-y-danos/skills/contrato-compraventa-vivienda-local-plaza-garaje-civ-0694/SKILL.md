---
name: contrato-compraventa-vivienda-local-plaza-garaje-civ-0694
description: "Contrato de compraventa de vivienda, local o plaza de garaje. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de compraventa de vivienda, local o plaza de garaje

> Formulario **CIV-0694** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Contrato por el que el vendedor se obliga a entregar una vivienda, local o plaza de garaje, a cambio del pago de un precio por el comprador, con o sin arras.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de compraventa de vivienda, local o plaza de garaje» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de compraventa de vivienda, local o plaza de garaje” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:contrato-compraventa-vivienda-local-plaza-garaje-civ-0694`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] DNI/NIE (4 veces)
- [ ] IMPORTE (4 veces)
- [ ] LINDEROS (3 veces)
- [ ] DIRECCIÓN (2 veces)
- [ ] FECHA (2 veces)
- [ ] NACIONALIDAD (2 veces)
- [ ] CALLE
- [ ] IMPORTE EN LETRA
- [ ] LUGAR
- [ ] Nº
- [ ] NÚMERO
- [ ] PORCENTAJE

## Normas que cita el formulario

- art. 1.454 Código Civil
- art. 1455 CC

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

Contrato por el que el vendedor se obliga a entregar una vivienda, local o plaza de garaje, a cambio del pago de un precio por el comprador, con o sin arras.


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
Datos del COMPRADOR)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, EL COMPRADOR.

Y DE OTRA,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
(Datos del VENDEDOR)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, EL VENDEDOR.

INTERVIENEN

[ELEGIR UNA OPCIÓN: en caso de que todas las partes actúen en nombre y representación propia / si alguna de las partes actúa en su propio nombre y representación]

[OPCIONAL — si alguna de las partes actúa en nombre y representación de persona física o jurídica]
[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de:

[ELEGIR UNA OPCIÓN: Si se trata de persona física / Si se trata de una persona jurídica]

Ambas partes se reconocen mutuamente con capacidad suficiente para otorgar el presente contrato de COMPRAVENTA y, a tal fin,

EXPONEN

I. Que el vendedor es propietario de [ELEGIR: Establecimiento mercantil / piso / plaza de garaje] situado en [DIRECCIÓN] estando interesado en su venta.

II. Que el comprador está interesado en la compra de [ELEGIR: Establecimiento mercantil / piso / plaza de garaje] descrito en la manifestación anterior, en estado libre de cargas y de arrendamientos, con cuanto le sea principal, accesorio, integrante y dependiente, y al corriente de pago en toda clase de contribuciones, impuestos, tasas, autonómicas y municipales, y gastos de comunidad.

III. Que expuesto cuanto antecede, las partes convienen el otorgamiento del presente contrato de compraventa conforme a los pactos y cláusulas que se determinan a continuación:

CLÁUSULAS

Primera.- Objeto

El objeto del presente contrato es la compra del [ELEGIR: Establecimiento mercantil / piso / plaza de garaje] sito en [LOCALIDAD], de [DIRECCIÓN] con [Nº] metros cuadrados, totalmente diáfano, con fachada a [CALLE] por donde tiene su acceso y que linda, según se mira de frente por la derecha, con [LINDEROS], al fondo con [LINDEROS] y a la izquierda con [LINDEROS]. Le pertenece en virtud de escritura de compraventa otorgada ante el notario de D./Dña. [NOMBRE Y APELLIDOS], el [FECHA] y constituye la finca registral nº [NÚMERO] del Registro de la Propiedad de

- Se encuentra libre de:

• Cargas y gravámenes, según resulta de las manifestaciones del vendedor y de nota simple informativa que ha sido remitida en el día de hoy por el Registro de la Propiedad de [LOCALIDAD].
• Arrendatarios ocupantes o precaristas

- Al corriente en el pago de los gastos de comunidad (con una cuota sobre los elementos comunes del [PORCENTAJE]) y de todos los impuestos lo que queda acreditado mediante la entrega del justificante de pago de la comunidad y del IBI.

Se adjuntan como anexo a este contrato certificación emitida por el administrador de la comunidad de la que forma parte y copia del recibo de pago del impuesto de bienes inmuebles del ejercicio en curso.

[OPCIONAL — incluir si procede]

(Para fincas rústicas o urbanas)

- No constituye vivienda habitual de su familia ni de pareja de hecho.

Segunda.- Arras

En este acto el comprador entrega al vendedor, a cuenta del precio total y en concepto de arras penitenciales, la cantidad de [IMPORTE] euros ( €), en [ELEGIR: Efectivo metálico / cheque conformado / cheque bancario], pudiendo tanto el adquirente como el vendedor en concordancia con el artículo 1.454 del Código Civil, desistir de la compraventa en cualquier momento posterior a la firma del presente documento. En el caso de desistimiento por parte del adquirente, éste perderá las cantidades que hubiera puesto a disposición del vendedor en concepto de señal y pago a cuenta del precio. Si desistiera el vendedor el adquirente percibirá de ésta la cantidad que entrego, duplicada. El vendedor da por recibida la cantidad entregada en concepto de arras penitenciales otorgando mediante este documento formal carta de pago.

Tercera.- Precio

Las partes acuerdan como precio total de la venta el de [IMPORTE] euros ( € [IMPORTE EN LETRA]), del que deberá deducirse la cantidad hoy entregada en concepto de arras, y que se pagará de la siguiente forma:

a) En cuanto a [IMPORTE] euros, se corresponden con la cantidad hoy entregada en concepto de arras.
b) Y en cuanto a los restantes [IMPORTE] euros, correspondientes al pago de la parte del precio que queda pendiente, serán satisfechos al otorgamiento de la escritura pública de compraventa y entrega simultánea de llaves.

[OPCIONAL — incluir si procede]

(Si se fracciona el pago en varios plazos)

Expresamente se pacta que el impago total o parcial o el retraso en el pago de cualquiera de los plazos previstos a sus vencimientos, dará lugar a la resolución del contrato sin necesidad de requerimiento o notificación alguna, haciendo suyas la parte vendedora la totalidad de las cantidades que ya hubiesen percibido como cláusula penal e indemnización, sin que evite la resolución del contrato el pago ulterior por la compradora, y quedando por tanto libre la parte vendedora para otorgar nuevo contrato de venta sobre el objeto fijado en el presente.

Sin perjuicio de lo establecido en el párrafo precedente, el pago de la totalidad del precio aplazado es condición suspensiva de la transmisión del dominio, que se lo reserva expresamente el vendedor hasta que se verifique el total pago y, en su consecuencia, la parte compradora no podrá enajenar sin consentimiento de la vendedora.

Cuarta.- Entrega

El vendedor entrega y pone a disposición del comprador el [ELEGIR: Establecimiento mercantil / piso / plaza de garaje], aceptándolo el comprador y manifestando su plena satisfacción por la entrega de todos los componentes del mismo.

El vendedor se obliga a entregar el [ELEGIR: piso / local / plaza de garaje] con la cedula de habitabilidad y certificado de eficiencia energética conforme al Real Decreto 390/2021, de 1 de junio, por el que se aprueba el procedimiento básico para la certificación de la eficiencia energética de los edificios.

Quinta.- Gastos

Todos los gastos e impuestos excepto el Impuesto sobre Incremento de Valor de los Terrenos Urbanos, derivados de este otorgamiento, serán de cuenta exclusiva del comprador.

Sexta.- Fuero

Ambas partes contratantes renuncian expresamente a su fuero sometiéndose a los Tribunales de [LOCALIDAD]

[ELEGIR UNA OPCIÓN: Sin elección de notario por el comprador / Con elección de notario por el comprador / — y además elegir: Por cuenta de cada parte según Ley / Pacto de gastos conforme art. 1455 CC]

En prueba de aceptación y conformidad, y para que así conste, las partes suscriben el presente documento, por duplicado ejemplar y a un solo efecto, en el lugar y fecha arriba indicados.

_______________________________

VENDEDOR

_______________________________

COMPRADOR

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]
