---
name: contrato-anticresis-sobre-inmueble-civ-0655
description: "Contrato de anticresis sobre un inmueble. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de anticresis sobre un inmueble

> Formulario **CIV-0655** del plugin **Propiedad, posesión, servidumbres e hipotecas** (`formularios-propiedad-y-derechos-reales`) · Civil › Propiedad y derechos reales · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de anticresis sobre un inmueble» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de anticresis sobre un inmueble” para mi caso». También puedes invocarla directamente con `/formularios-propiedad-y-derechos-reales:contrato-anticresis-sobre-inmueble-civ-0655`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-propiedad-y-derechos-reales:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Propiedad, posesión, servidumbres e hipotecas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (9 veces)
- [ ] LOCALIDAD (7 veces)
- [ ] DNI/NIE (4 veces)
- [ ] FECHA (4 veces)
- [ ] IMPORTE (4 veces)
- [ ] LINDEROS (4 veces)
- [ ] NACIONALIDAD (2 veces)
- [ ] DATOS DE PERSONA ADICIONAL
- [ ] DENOMINACIÓN SOCIAL
- [ ] LUGAR
- [ ] NOMBRE DE LA PARTE
- [ ] Nº
- [ ] REFERENCIA CATASTRAL
- [ ] SUPERFICIE

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

Por la anticresis el acreedor adquiere el derecho a percibir los frutos de un inmueble de su deudor, con la obligación de aplicarlos al pago de los intereses, si se debieren, y después al del capital de su crédito (art. 1881 Cc)

En [LUGAR], a [FECHA]
REUNIDOS

DE UNA PARTE,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
(Datos del CONSTITUYENTE)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, CONSTITUYENTE.

Y DE OTRA,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
(Datos del ACREEDOR)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, ACREEDOR.

INTERVIENEN

[ELEGIR UNA OPCIÓN: en caso de que todas las partes actúen en nombre y representación propia / si alguna de las partes actúa en su propio nombre y representación]

[OPCIONAL — si alguna de las partes actúa en nombre y representación de persona física o jurídica]
[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de:

[ELEGIR UNA OPCIÓN: Si se trata de persona física / Si se trata de una persona jurídica]

Ambas partes se reconocen mutuamente con capacidad suficiente para otorgar el presente contrato de ANTICRESIS y, a tal fin

MANIFIESTAN

I. Que D./Dña. [NOMBRE Y APELLIDOS], (en adelante, EL CONSTITUYENTE) es propietario de la finca sita en [LOCALIDAD] con la siguiente descripción:

Tiene una superficie de [SUPERFICIE]: Linda: al sur con [LINDEROS]; al norte con [LINDEROS], al oeste con [LINDEROS] y al este [LINDEROS]

Se halla inscrita en el Registro de la Propiedad de [LOCALIDAD], al .Le pertenece a título de dominio en virtud de la [ELEGIR: compra / donación / herencia] de fecha [FECHA], según consta en la inscripción núm. [Nº] de la finca.

La finca se halla libre de arrendamientos y cargas. Al corriente del pago de impuestos, tasas y contribuciones de todo tipo.

Identificación catastral [REFERENCIA CATASTRAL].

II. Que la entidad mercantil [DENOMINACIÓN SOCIAL] ( en adelante, el ACREEDOR) ostenta un crédito derivado de la escritura de préstamo de fecha [FECHA], otorgada ante el Notario de [LOCALIDAD] D./Dña. [NOMBRE Y APELLIDOS], por importe de [IMPORTE] euros de principal y de [IMPORTE] euros de intereses vencidos, del que es deudor el CONSTITUYENTE, según documento de liquidación que se incorpora como Anexo a este contrato. Dicha deuda devenga un interés adicional de % anual.

III. Que ambas partes convienen la celebración de un contrato de constitución de ANTICRESIS sobre la finca descrita en garantía de la deuda, con sujeción a las siguientes:

CLÁUSULAS

Primera.- Objeto

Por el presente contrato, EL CONSTITUYENTE se obliga a ceder la posesión y disfrute del inmueble señalado en la primera manifestación en favor de EL ACREEDOR, en calidad de anticresis, aplicando los frutos o rentas que produzca a la amortización del préstamo mencionado.

Segunda.- Términos

Las partes manifiestan que EL ACREEDOR ha prestado al CONSTITUYENTE la suma de [IMPORTE] euros (€), en dinero en efectivo, según documento aportado de fecha [FECHA].

La suma adeudada será devuelta por EL CONSTITUYENTE en el plazo señalado en el documento de préstamo referido.

Tercera.- Duración

Las partes acuerdan que EL CONSTITUYENTE concederá al ACREEDOR la posesión del inmueble mencionado en la manifestación primera, durante [ELEGIR: meses / años] contados a partir de la suscripción de la escritura pública.

Si en el plazo señalado anteriormente, el CONSTITUYENTYE no hubiese cumplido con la obligación de cancelar el total de su obligación dineraria, EL ACREEDOR podrá continuar en posesión del inmueble cedido en anticresis hasta la devolución total del monto otorgado en préstamo.

Cuarta.- Obligaciones y derechos del acreedor

El ACREEDOR tiene derecho a percibir los frutos del inmueble objeto de anticresis con la obligación de aplicarlos, en primer lugar, al pago de los intereses del crédito, y después al capital. Los intereses de la deuda se compensarán con los frutos de la finca dada en anticresis.

El ACREEDOR debe cumplir las obligaciones derivadas del contrato y en especial:

1. Administrar con diligencia el inmueble y dar a los frutos el destino pactado.
2. Preservar y cuidar el bien, sin realizar modificaciones sustanciales ni alterar su destino.
3. Indemnizar al CONSTITUYENTE por los daños sufridos en el inmueble por dolo o negligencia.
4. Pagar las contribuciones y cargas que pesen sobre la finca, así como los gastos necesarios para su conservación y reparación. Los gastos derivados de estos conceptos se deducirán de los frutos percibidos por el ACREEDOR.
5. Rendir cuentas sobre la administración y destino de los frutos al CONSTITUYENTE con periodicidad anual.
6. Restituir el bien al deudor una vez que se le pague íntegramente el crédito con sus intereses.

Quinta.- Obligaciones y derechos del constituyente

El CONSTITUYENTE tiene los derechos derivados de su condición de titular del inmueble, correlativos a los deberes del ACREEDOR, y debe cumplir con las obligaciones derivadas del contrato y en especial la de garantizar la pacífica posesión del inmueble por el ACREEDOR.

Sexta.- Cesión

EL ACREEDOR no podrá ceder a terceros el bien materia de anticresis, bajo ningún título, ni ceder su posición contractual, salvo que cuente con el consentimiento expreso y por escrito de EL CONSTITUYENTE

Séptima.- Devolución

EL ACREEDOR se obliga a desocupar y devolver el bien dado en garantía una vez que la deuda quede satisfecha

Octava.- Confidencialidad

Las partes se comprometen a no divulgar la información y documentación confidencial referente a la otra parte de la que hayan tenido conocimiento por razón de la ejecución del presente contrato, salvo las indispensables para su cumplimiento, y a mantenerla en secreto, incluso después de la finalización del mismo.

Ambas partes acuerdan tomar las medidas necesarias respecto a su personal e incluso terceros que puedan tener acceso a dichas información y documentación, a fin de garantizar la confidencialidad objeto de esta cláusula.

Novena.- Protección de datos

El acreedor reconoce que la legislación sobre protección de datos personales (ley orgánica 3/2018, de 5 de diciembre, de protección de datos personales y garantía de derechos digitales) establece una serie de obligaciones en el tratamiento de datos de carácter personal, entre las que destaca la prohibición de realizar cesiones de datos de carácter personal sin la correspondiente autorización del titular de los datos personales. A tal efecto, el acreedor:

a) únicamente accederá a los datos personales de clientes y demás personas físicas relacionadas con el constituyente si tal acceso fuese necesario para cumplir con los servicios objeto del presente contrato.
b) se compromete a:
- utilizar los datos de carácter personal a los que tenga acceso única y exclusivamente para cumplir con sus obligaciones contractuales para con el cliente.
- observar y adoptar cuantas medidas de seguridad sean necesarias para asegurar la confidencialidad, secreto e integridad de los datos de carácter personal a los que tenga acceso, así como a adoptar en el futuro cuantas medidas de seguridad sean exigidas por las leyes y reglamentos destinadas a preservar el secreto, confidencialidad e integridad en el tratamiento automatizado de datos personales.
- a no ceder en ningún caso a terceras personas los datos de carácter personal a los que tenga acceso, ni tan siquiera a efectos de su conservación.

Las obligaciones establecidas para el acreedor por la presente cláusula serán también de obligado cumplimiento para sus posibles empleados, colaboradores, tanto externos como internos, y subcontratistas, por lo que la entidad financiera responderá frente al cliente si tales obligaciones son incumplidas por tales empleados, colaboradores y subcontratistas.

El incumplimiento por parte de acreedor de cualesquiera de las obligaciones establecidas en la anterior cláusula de confidencialidad y en ésta de tratamiento de datos de carácter personal, generará una indemnización en favor del constituyente de [IMPORTE] euros, sin perjuicio de su derecho a resarcirse de los perjuicios que le sean causados y que superen la cuantía indicada.

La duración de las obligaciones de confidencialidad establecidas en el presente contrato será indefinida, manteniéndose en vigor con posterioridad a la finalización, por cualquier causa, de la relación entre la entidad financiera y el cliente.

Décima.- Notificaciones

Las partes señalan como domicilios para la práctica de las notificaciones necesarias en la ejecución del presente contrato:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

[DATOS DE PERSONA ADICIONAL]

Decimoprimera.- Impuestos

Todos los impuestos, gastos judiciales o extrajudiciales originados a consecuencia de la celebración del presente contrato serán de cuenta de [NOMBRE DE LA PARTE].

Decimosegunda.- Naturaleza del contrato y normativa aplicable

El presente contrato tiene naturaleza mercantil, rigiéndose por lo dispuesto en sus propias cláusulas y en su defecto, por lo dispuesto por la legislación mercantil y civil vigente, tanto española como de la Unión Europea que fuere de aplicación.

Decimocuarta.- Fuero competente

[ELEGIR UNA DE LAS ALTERNATIVAS QUE SIGUEN Y SUPRIMIR LAS DEMÁS]

Ambas partes contratantes renuncian expresamente a su fuero sometiéndose a los Tribunales de [LOCALIDAD].

Para cuantas cuestiones o divergencias pudieran suscitarse en relación con el presente contrato, ambas partes establecen someterse al Arbitraje de Derecho de la Cámara de Comercio de [LOCALIDAD].

Y en prueba de conformidad con todo ello firman el presente documento por duplicado ejemplar y a un solo efecto en el lugar y fecha expresados en el encabezamiento.

EL CONSTITUYENTE

EL ACREEDOR

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]
