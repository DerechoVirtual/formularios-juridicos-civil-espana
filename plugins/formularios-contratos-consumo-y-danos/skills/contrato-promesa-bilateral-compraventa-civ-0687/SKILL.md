---
name: contrato-promesa-bilateral-compraventa-civ-0687
description: "Contrato de promesa bilateral de compraventa. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de promesa bilateral de compraventa

> Formulario **CIV-0687** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de promesa bilateral de compraventa» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de promesa bilateral de compraventa” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:contrato-promesa-bilateral-compraventa-civ-0687`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (14 veces)
- [ ] IMPORTE (12 veces)
- [ ] DNI/NIE (8 veces)
- [ ] LOCALIDAD (7 veces)
- [ ] FECHA (6 veces)
- [ ] NACIONALIDAD (4 veces)
- [ ] Nº (4 veces)
- [ ] LUGAR (2 veces)
- [ ] MARCA Y MODELO (2 veces)
- [ ] NOMBRE DE LA PARTE (2 veces)
- [ ] ASTILLERO
- [ ] AÑO
- [ ] BANDERA
- [ ] DATOS DE PERSONA ADICIONAL
- [ ] DESCRIPCIÓN DEL BIEN
- [ ] ESLORA
- [ ] FECHAS
- [ ] KILÓMETROS
- [ ] MANGA
- [ ] MARCA/MODELO
- [ ] MATRÍCULA
- [ ] MES
- [ ] Nº DE BASTIDOR
- [ ] Nº DE MOTORES
- [ ] Nº DE SERIE
- [ ] Nº WIN
- [ ] OBLIGACIONES FISCALES Y ADMINISTRATIVAS
- [ ] POTENCIA
- [ ] ÓRGANO

## Normas que cita el formulario

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

Promesa bilateral de venta y de compra, por la que ambas partes, puestas de acuerdo en la cosa y en el precio y no queriendo aun concertar la compraventa, adquieren el compromiso recíproco de que cualquiera de ellas podrá exigir de la contraria, dentro del plazo pactado, el cumplimiento del contrato

En [LUGAR], a [FECHA]
REUNIDOS

DE UNA PARTE,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
(Datos del PROMITENTE COMPRADOR)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, PROMITENTE COMPRADOR.

Y DE OTRA,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
(Datos del PROMITENTE VENDEDOR)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, PROMITENTE VENDEDOR.

INTERVIENEN

[ELEGIR UNA OPCIÓN: en caso de que todas las partes actúen en nombre y representación propia / si alguna de las partes actúa en su propio nombre y representación]

[OPCIONAL — si alguna de las partes actúa en nombre y representación de persona física o jurídica]
[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de:

[ELEGIR UNA OPCIÓN: Si se trata de persona física / Si se trata de una persona jurídica]

Ambas partes se reconocen mutuamente con capacidad suficiente para otorgar la presente PROMESA de COMPRAVENTA y, a tal fin,

MANIFIESTAN

I. Que el Promitente - vendedor es propietario, por el título que luego se dirá, de los siguientes bienes: [DESCRIPCIÓN DEL BIEN].

II. Que los referidos bienes se encuentran libres de cargas y arrendamientos y al corriente de pago de cualquier tipo de tasa, impuesto, contribución o arbitrio.

III. Que al momento de la firma del presente documento, dicho bien se encuentra en perfecto estado de conservación, uso y funcionamiento.

IV. Que el Promitente - comprador está interesado en la compra de los bienes descritos.

V. Que ambas partes han llegado a un acuerdo para la futura venta de los mencionados bienes en las condiciones que se establecen en las siguientes:

CLÁUSULAS

Primera.- Objeto

El Promitente - vendedor promete vender al Promitente - comprador, que promete comprar, los bienes que se relacionan en la manifestación anterior, en la condiciones que a continuación se establecen.

Segunda.- Precio

El precio por el que se efectuará la compraventa es de [IMPORTE]. Esta cantidad acordada en concepto de precio de la futura compraventa se ha fijado incluyendo el Impuesto sobre el Valor Añadido (IVA) que asimismo corresponde abonar al promitente comprador.

La suma de [IMPORTE] euros, es satisfecha en este acto por el Promitente - comprador en concepto de arras penitenciales, de acuerdo con lo previsto en el art. 1454 del Código Civil. En el momento de perfeccionarse la compraventa esta cantidad tendrá la consideración de pago a cuenta del total precio convenido, aunque hasta entonces conservará el mencionado carácter de arras penitenciales.

b) En el momento de perfeccionarse el contrato de compraventa será satisfecha por el Promitente - comprador la restante suma de [IMPORTE] euros.

Si la venta no se realizara por desistimiento del promitente comprador éste perderá la cantidad satisfecha en este acto en concepto de arras penitenciales.

Si quien desiste del contrato es el Promitente - vendedor, éste deberá devolver al Promitente - comprador la cantidad entregada en este acto más una cantidad igual en concepto de indemnización por el desistimiento.

Tercera.- Plazo para la celebración del contrato

La promesa se concede por un plazo máximo de que expira el [FECHA]

Cuarta.- Entrega y Posesión del bien

[ELEGIR UNA OPCIÓN: A la firma de la promesa / A la firma de la compraventa]

La falta de entrega de los bienes en el plazo señalado por causa distinta a caso fortuito, fuerza mayor o culpa del Promitente - comprador dará derecho a éste a optar entre resolver el contrato o exigir al Promitente - vendedor la entrega efectiva de los bienes y una indemnización igual a [IMPORTE] euros, por cada día de retraso.

Quinta.- Gastos e Impuestos

Todos los gastos e impuestos derivados del presente Contrato serán de cargo del promitente comprador, salvo aquellos que le correspondan al promitente vendedor de acuerdo a la legislación vigente o al presente Contrato.

Sexta.- Formalización

El documento privado de este Contrato será elevado a escritura pública, a petición de cualquiera de las Partes, mediante requerimiento fehaciente, ante el Notario o Notaria que dicha Parte designe. Los gastos correspondientes a esta formalización correrá a cargo de [NOMBRE DE LA PARTE].

Séptima.- Notificaciones

Las partes señalan como domicilios para la práctica de las notificaciones necesarias en la ejecución del presente contrato:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

[DATOS DE PERSONA ADICIONAL]

Octava.- Naturaleza del contrato y normativa aplicable

El presente contrato tiene naturaleza mercantil, rigiéndose por lo dispuesto en sus propias cláusulas y en lo en ellas no previsto por las disposiciones del Código de Comercio, Leyes especiales, los usos y costumbres mercantiles y, en su defecto, por lo establecido en el Código Civil.

Novena.- Fuero competente

[ELEGIR UNA DE LAS ALTERNATIVAS QUE SIGUEN Y SUPRIMIR LAS DEMÁS]

Ambas partes contratantes renuncian expresamente a su fuero sometiéndose a los Tribunales de [LOCALIDAD].

Para cuantas cuestiones o divergencias pudieran suscitarse en relación con el presente contrato, ambas partes establecen someterse al Arbitraje de Derecho de la Cámara de Comercio de [LOCALIDAD].

Y en prueba de conformidad con todo ello firman el presente documento por duplicado ejemplar y a un solo efecto en el lugar y fecha expresados en el encabezamiento.

PROMITENTE VENDEDOR

PROMITENTE COMPRADOR

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

70. Contrato de compraventa de [ELEGIR: vehículo a motor / motocicleta / embarcación]

REUNIDOS
INTERVIENEN
MANIFIESTAN
CLÁUSULAS
Firmas

Contrato por el que el vendedor se obliga a entregar un vehículo, ciclomotor, moto, o embarcación de segunda mano a cambio del pago de un precio por el comprador.

En [LUGAR], a [FECHA]
REUNIDOS

DE UNA PARTE,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
(Datos del VENDEDOR)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, VENDEDOR.

Y DE OTRA,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
(Datos del COMPRADOR)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, COMPRADOR.

INTERVIENEN

[ELEGIR UNA OPCIÓN: en caso de que todas las partes actúen en nombre y representación propia / si alguna de las partes actúa en su propio nombre y representación]

[OPCIONAL — si alguna de las partes actúa en nombre y representación de persona física o jurídica]
[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de:

[ELEGIR UNA OPCIÓN: Si se trata de persona física / Si se trata de una persona jurídica]

Ambas partes se reconocen mutuamente con capacidad suficiente para otorgar el presente contrato de compraventa de [ELEGIR: vehículo / ciclomotor / motocicleta / embarcación] y, a tal fin,

MANIFIESTAN

I. Que el vendedor es propietario [ELEGIR: del vehículo / del ciclomotor / de la motocicleta / de la embarcación] objeto de compraventa.

II. Que el comprador está interesado en adquirir la propiedad de dicho/a [ELEGIR: vehículo / ciclomotor / motocicleta / embarcación].

III. Que [ELEGIR: el vehículo / el ciclomotor / la motocicleta / la embarcación] tiene las siguientes características:

[OPCIONAL — incluir si procede]

(Vehículos y motos)

Marca y modelo: [MARCA Y MODELO].

Matrícula y nº [Nº] de bastidor: [Nº DE BASTIDOR].

Kilómetros en el momento de la compra: [KILÓMETROS].

Fecha de la primera matriculación: [FECHA].

[OPCIONAL — incluir si procede]

(Embarcaciones)

Astillero de construcción [ASTILLERO].

Modelo [MARCA/MODELO].

Año de construcción: [AÑO].

WIN [Nº WIN].

Bandera: [BANDERA].

Nº [Nº] de Registro / Matrícula [MATRÍCULA].

Eslora: [ESLORA].

Manga: [MANGA].

Nº motores: [Nº DE MOTORES].

Potencia: [POTENCIA].

Marca /Modelo motores: [MARCA Y MODELO].

NºSerie [Nº DE SERIE].

Equipada con las partes integrantes, pertenencias, equipos electrónicos y accesorios que se describen en documento separado y que las partes han consensuado con anterioridad a la firma del presente contrato.

IV. Que ambas partes puestas de acuerdo han convenido realizar un contrato de compraventa de [ELEGIR: vehículo / ciclomotor / motocicleta / embarcación] con arreglo a las siguientes:

CLÁUSULAS

Primera.- Objeto

El vendedor vende al comprador [ELEGIR: el automóvil / el ciclomotor / la motocicleta / la embarcación] de su propiedad anteriormente especificado por la cantidad de [IMPORTE] euros, sin incluir los impuestos correspondientes, que serán a cargo del comprador.

Segunda.- Garantía

[ELEGIR UNA OPCIÓN: Sin cargas / Con cargas]

Tercera.- Documentación

El vendedor se compromete a facilitar los distintos documentos relativos a [ELEGIR: el automóvil / el ciclomotor / la motocicleta / la embarcación], así como a firmar cuantos documentos aparte de éstos sean necesarios para que [ELEGIR: el automóvil / el ciclomotor / la motocicleta / la embarcación] quede correctamente inscrito a nombre del comprador en los correspondientes organismos públicos, siendo todos los gastos a cargo del comprador.

Cuarta.- Precio y forma de pago

El precio de la presente compraventa es de [IMPORTE] euros.

[OPCIONAL — incluir si procede]

(Cuando el pago de la totalidad del precio es anterior)

El vendedor manifiesta haber recibido la totalidad del precio indicado con anterioridad a este acto del comprador, sirviendo el presente documento como carta de pago.

[OPCIONAL — incluir si procede]

(Cuando el pago de la totalidad del precio es simultaneo)
[ELEGIR UNA OPCIÓN: En efectivo / Con cheque / Por transferencia]

[OPCIONAL — incluir si procede]

(Cuando el pago de la totalidad del precio es anterior y simultaneo)

Esta cantidad será satisfecha de la siguiente forma:

a) la cantidad de [IMPORTE], reconoce el vendedor haberla recibido del comprador con anterioridad a este acto.
b) la cantidad de [IMPORTE], es pagada en este acto por el comprador en efectivo (o mediante cheque bancario nominativo o transferencia) por valor de [IMPORTE] sirviendo el presente documento como carta de pago.

[OPCIONAL — incluir si procede]

(Cuando media aplazamiento del pago del precio)

Esta cantidad será pagada de la siguiente forma:

a) [IMPORTE] euros se entregan al vendedor en este acto por el comprador mediante [ÓRGANO] sirviendo el presente documento como carta de pago.
b) [IMPORTE] será satisfecha por el comprador en un total de [Nº] pagos, el primero de los cuales tendrá lugar el [FECHA].

Como garantía del abono del precio aplazado se libran - letras de cambio-números [Nº] por importe [IMPORTE] cada una de ellas y con vencimiento los días [FECHAS] de [MES] cada mes. Dichas letras de cambio son aceptadas en este acto por el comprador.

[ELEGIR UNA OPCIÓN: Con condición suspensiva / Con condición resolutoria]

Quinta.- Entrega

[ELEGIR UNA OPCIÓN: Gastos a cuenta del vendedor / Gastos a cuenta del comprador]

El lugar de entrega será el que decida [NOMBRE DE LA PARTE] en [LOCALIDAD] corriendo de cargo de los gastos que se originen por el traslado o transporte del [ELEGIR: del automóvil / del ciclomotor / de la motocicleta / dela embarcación] hasta el lugar de entrega.

Sexta. Vicios o defectos

[ELEGIR UNA OPCIÓN: Renuncia del comprador a reclamación / Salvo dolo o mala fe]

No existirá responsabilidad del vendedor por averías o deficiencias del [ELEGIR: del automóvil / del ciclomotor / de la motocicleta / de la embarcación] aparecidas con posterioridad a la entrega del mismo, cuando estas circunstancias se produzcan o vengan motivadas por un uso inadecuado o a consecuencia de fuerza mayor, robo, hurto, negligencia, accidente o falta del mantenimiento aconsejado por el fabricante.

[OPCIONAL — incluir si procede]

(Embarcaciones)

El comprador reconoce haber probado la embarcación y haber tenido la posibilidad de proceder a la realización de un informe pericial para conocer, por parte de un técnico, el estado de la misma.

Séptima. Seguros

El automóvil [ELEGIR: El ciclomotor / La motocicleta / La embarcación] dispone de seguro en vigor hasta [FECHA] y se encuentra al corriente respecto a las obligaciones derivadas de [OBLIGACIONES FISCALES Y ADMINISTRATIVAS].

Octava.- Conflictos

[ELEGIR UNA OPCIÓN: Arbitraje / Tribunales]

Y en prueba de conformidad, firman el presente contrato de compraventa, por triplicado, en la fecha y lugar arriba indicados.

COMPRADOR

VENDEDOR

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]
