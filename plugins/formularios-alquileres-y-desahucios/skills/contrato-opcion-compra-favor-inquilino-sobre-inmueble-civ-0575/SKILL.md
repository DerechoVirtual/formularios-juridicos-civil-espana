---
name: contrato-opcion-compra-favor-inquilino-sobre-inmueble-civ-0575
description: "Contrato de opción de compra a favor del inquilino sobre el inmueble arrendado. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de opción de compra a favor del inquilino sobre el inmueble arrendado

> Formulario **CIV-0575** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 24-11-2026.

## Qué es

Contrato de opción de compra a inquilino sobre un bien inmueble ya arrendado anteriormente, incluyéndose tanto los presupuestos, estipulaciones y circunstancias para el cumplimiento del mismo, así como los derechos y obligaciones del concedente y del optante.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de opción de compra a favor del inquilino sobre el inmueble arrendado» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de opción de compra a favor del inquilino sobre el inmueble arrendado” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:contrato-opcion-compra-favor-inquilino-sobre-inmueble-civ-0575`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (19 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] DNI/NIE (4 veces)
- [ ] FECHA (4 veces)
- [ ] IMPORTE (4 veces)
- [ ] IMPORTE EN CIFRA (4 veces)
- [ ] NACIONALIDAD (2 veces)
- [ ] NOMBRE DE LA PARTE (2 veces)
- [ ] Nº (2 veces)
- [ ] DATOS REGISTRALES
- [ ] INICIO DEL CÓMPUTO DEL PLAZO
- [ ] LUGAR
- [ ] MUNICIPIO
- [ ] Nº DE LETRAS DE CAMBIO
- [ ] Nº DE PROTOCOLO
- [ ] PROVINCIA

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

(Datos de UNA PARTE)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, [NOMBRE DE LA PARTE].

Y DE OTRA,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

(Datos de OTRA PARTE)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, [NOMBRE DE LA PARTE].

INTERVIENEN

[ELEGIR UNA OPCIÓN: en caso de que todas las partes actúen en nombre y representación propia / si alguna de las partes actúa en su propio nombre y representación]

[OPCIONAL — si alguna de las partes actúa en nombre y representación de persona física o jurídica]
[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de:

[ELEGIR UNA OPCIÓN: Si se trata de persona física / Si se trata de una persona jurídica]

Ambas partes recíprocamente se reconocen la suficiente capacidad legal y legitimación para llevar a efecto el presente contrato, acreditando su identidad por los documentos indicados, actuando en nombre y representación propia, y de común acuerdo manifiestan las siguientes:

ESTIPULACIONES

Primera.- Que D./D.ª [NOMBRE Y APELLIDOS], es propietario del inmueble sito en el término municipal de [MUNICIPIO] provincia de [PROVINCIA], con una superficie de [Nº] metros cuadrados, lindando a la izquierda con la vivienda propiedad de D./D.ª [NOMBRE Y APELLIDOS], a la derecha con la vivienda propiedad de D./D.ª [NOMBRE Y APELLIDOS], constando inscrita a su nombre y libre de cargas en el Registro de la Propiedad de [LOCALIDAD], al [DATOS REGISTRALES], y le pertenece por título de compraventa (o donación) en escritura autorizada por el Notario de [LOCALIDAD] D./D.ª [NOMBRE Y APELLIDOS] en fecha [FECHA] y con número de protocolo [Nº DE PROTOCOLO].

Segunda.- Que la vivienda descrita se halla arrendada al aquí compareciente D./D.ª [NOMBRE Y APELLIDOS] desde el día [FECHA], tal como consta en el contrato de arrendamiento suscrito entre ambas partes.

Tercera.- Que D./D.ª [NOMBRE Y APELLIDOS] está interesado en vender el inmueble descrito en la estipulación primera, y con tal fin, ofrece su venta al arrendatario D./D.ª [NOMBRE Y APELLIDOS], quien a su vez acepta, bajo las condiciones y circunstancias que al efecto exponen a continuación en virtud de los siguientes:

PACTOS

I.- D./D.ª [NOMBRE Y APELLIDOS] concede subscribir la opción de compra sobre la finca urbana ya referenciada en la primera estipulación a D./D.ª [NOMBRE Y APELLIDOS], quien en la actualidad la ocupa en calidad de arrendatario o inquilino.

II.- La opción de compra deberá ejercitarse por el beneficiario de la opción en un plazo máximo de [Nº] meses o años [INICIO DEL CÓMPUTO DEL PLAZO], fijándose en este momento como precio total de compra el de [IMPORTE] euros ([IMPORTE EN CIFRA] €).

III.- El presente contrato no obstaculizará ni servirá de pretexto para el impago de las rentas mensuales que se vienen abonando en concepto de alquiler, debiendo abonar el optante en el momento en que ejercite su derecho, la cantidad de [IMPORTE] euros ([IMPORTE EN CIFRA] €) que se considerarán entregadas a cuenta del precio total, abonándose el resto de [IMPORTE] euros ([IMPORTE EN CIFRA] €) en vencimientos mensuales consecutivos cada día [FECHA] de cada mes en cuantía de [IMPORTE] euros ([IMPORTE EN CIFRA] €), mediante la aceptación en este momento de [Nº DE LETRAS DE CAMBIO] letras de cambio por igual importe.

IV.- En caso de que no fuese ejercitada la opción de compra por D./D.ª [NOMBRE Y APELLIDOS] en dicho término, quedará el presente contrato resuelto, sin efectos o valor alguno.

Cuarta.- Durante la vigencia del presente contrato, el concedente no podrá enajenar o gravar la finca descrita, así como ofrecer una opción a tercera persona, debiendo permanecer en la misma situación jurídica en la que se encuentra actualmente.

Quinta.- El presente contrato es inscribible en el Registro de la Propiedad, debiendo correr la parte compradora con todos los gastos de escrituración que origine su elevación, así como los actos posteriores a la finalización del mismo.

Sexta.- Ambas partes, con renuncia de su fuero propio si lo tuvieren, se someten expresamente a los Tribunales de [LOCALIDAD] para la interpretación o cualquier cuestión litigiosa que derive de este contrato.

Y para que conste, firman por duplicado y a un solo efecto en el lugar y fecha ‘ut supra’.

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

========================================================================
