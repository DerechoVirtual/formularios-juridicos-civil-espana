---
name: contrato-compraventa-piso-construccion-pago-aplazado-civ-0840
description: "Contrato de compraventa de piso en construcción con pago aplazado y entrega diferida. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de compraventa de piso en construcción con pago aplazado y entrega diferida

> Formulario **CIV-0840** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Contrato de compraventa, con pago aplazado y entrega diferida al día de vencimiento de la última letra, cláusula penal, subrogación del comprador en la hipoteca contratada por el vendedor y obligación de elevación a escritura pública, de piso en construcción siendo el vendedor la sociedad constructora.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de compraventa de piso en construcción con pago aplazado y entrega diferida» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de compraventa de piso en construcción con pago aplazado y entrega diferida” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:contrato-compraventa-piso-construccion-pago-aplazado-civ-0840`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (11 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] DNI/NIE (4 veces)
- [ ] Nº (4 veces)
- [ ] FECHA (2 veces)
- [ ] NACIONALIDAD (2 veces)
- [ ] CALLE
- [ ] IMPORTE
- [ ] IMPORTE EN CIFRA
- [ ] LETRA
- [ ] LUGAR
- [ ] Nº DE PISOS
- [ ] Nº DE PISOS EN LETRA
- [ ] Nº DE PROTOCOLO
- [ ] PISO
- [ ] REFERENCIA CATASTRAL

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

En [LUGAR], a [FECHA]
REUNIDOS

DE UNA PARTE,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
Datos del VENDEDOR)

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

Ambas partes se reconocen mutuamente con capacidad suficiente para otorgar el presente contrato de COMPRAVENTA y, a tal fin,

EXPONEN

Primero.- Que D./D.ª [NOMBRE Y APELLIDOS] es propietaria de la finca sita en [LOCALIDAD], calle [CALLE], con una superficie de [Nº] metros cuadrados, y que estará compuesta por un bloque de [Nº DE PISOS EN LETRA] (número) [Nº DE PISOS] pisos, constando inscrita a su nombre y libre de cargas en el Registro de la Propiedad de [LOCALIDAD] mediante título de compraventa en escritura autorizada por el Notario de [LOCALIDAD] D./D.ª [NOMBRE Y APELLIDOS] en fecha [FECHA] y con número de protocolo [Nº DE PROTOCOLO], con referencia catastral [REFERENCIA CATASTRAL], promoviendo la construcción y venta de los mismos.

Segundo.- D./D.ª [NOMBRE Y APELLIDOS] vende el piso [PISO] letra [LETRA], ocupando una superficie de [Nº] metros cuadrados construidos y de [Nº] metros cuadrados útiles de la finca urbana ya referenciada en el exponendo primero a D./D.ª [NOMBRE Y APELLIDOS], quien está interesado en comprar y a su vez compra, en la cantidad de [IMPORTE] euros ([IMPORTE EN CIFRA] €).

Para la correcta identificación de la vivienda citada y de sus características se adjunta al presente contrato, la siguiente documentación:

— Plano de la vivienda y del conjunto residencial, donde se identifica la vivienda que se trasmite.
— Memoria descriptiva de las características técnicas de la construcción.
[ELEGIR UNA OPCIÓN: Elección de Notario por parte vendedora / Elección de Notario por parte compradora]

Cuarto.- Si llegado el día de vencimiento de la última Letra, fecha en la que se elevará a escritura pública con la correspondiente entrega de llaves del piso objeto de este contrato, no hubiesen sido satisfechas todas las Letras o quedaran pendientes más de dos, bien consecutivas o alternas, se faculta a la parte vendedora para a su opción exigir el cumplimiento del contrato o resolver el mismo, sin requerimiento previo, pudiendo la parte vendedora retener el [Nº] por ciento de lo entregado en concepto de daños y perjuicios, devolviendo el resto.

Quinto.- Si la parte vendedora incumpliese su obligación de entregar a la parte compradora la referida vivienda en la fecha estipulada y conforme a las condiciones y características convenidas, el presente contrato quedará resuelto, a menos que la parte compradora conceda un nuevo plazo para la entrega de la misma, transcurrido el cual sin realizar la referida entrega se entenderá en todo caso resuelto. En caso de resolución del contrato, la parte vendedora deberá devolver a la parte compradora las cantidades que ésta haya anticipado a cuenta del precio estipulado, incrementadas, de conformidad con lo establecido en la Disposición Adicional Primera de la Ley 38/1999.

Sexto.- Para el caso de que alguna de las partes no concurriera a la firma de la escritura pública y a efectuar el correspondiente pago y cobro, quien no sea culpable del incumplimiento podrá
reclamar a la otra parte los derechos y obligaciones del presente contrato y los daños y perjuicios que el retraso le ocasione
reclamar los daños y perjuicios que el incumplimiento de este contrato le ocasione desistiendo del mismo
 . Es decir en el caso de que no compareciere el Comprador perderá la cantidad entregada pudiendo el Vendedor pedir daños y perjuicios. Sin embargo si el que no compareciere es el Vendedor, el Comprador podrá pedir el cumplimiento del contrato y los perjuicios que se le causen.

[ELEGIR UNA OPCIÓN: En caso de que se pacten los gastos entre el comprador y el vendedor / En caso de que los gastos los asuma el comprador]

Octavo.- En este acto el vendedor hace expresa manifestación de que tiene en sus oficinas a disposición del público en general, y del comprador en particular, cuantos documentos e información viene obligado a suministrar de conformidad con las disposiciones que regulan la protección de los consumidores.

Asimismo, en el momento de otorgamiento, la vendedora entregará a la compradora el certificado de eficiencia energética del inmueble objeto del presente contrato, según el Real Decreto 390/2021, de 1 de junio, por el que se aprueba el procedimiento básico para la certificación de eficiencia energética de edificios.

[ELEGIR UNA OPCIÓN: Si pactan fuero / Si pactan someterse a arbitraje]

Y para que conste, firman por duplicado y a un solo efecto en el lugar y fecha ut supra.

VENDEDOR

COMPRADOR

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

ANEXO I PLANO DE LA VIVIENDA

ANEXO II MEMORIA DESCRIPTIVA

========================================================================
