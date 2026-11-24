---
name: escritura-declaracion-obra-nueva-division-horizontal-civ-0638
description: "Escritura de declaración de obra nueva y división horizontal. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escritura de declaración de obra nueva y división horizontal

> Formulario **CIV-0638** del plugin **Comunidades de propietarios** (`formularios-comunidades-de-propietarios`) · Civil › Propiedad horizontal · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escritura de declaración de obra nueva y división horizontal» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escritura de declaración de obra nueva y división horizontal” para mi caso». También puedes invocarla directamente con `/formularios-comunidades-de-propietarios:escritura-declaracion-obra-nueva-division-horizontal-civ-0638`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-comunidades-de-propietarios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Comunidades de propietarios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (25 veces)
- [ ] LINDEROS (16 veces)
- [ ] LOCALIDAD (7 veces)
- [ ] Nº DE TRASTERO (7 veces)
- [ ] NÚMERO (7 veces)
- [ ] CALLE (6 veces)
- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] Nº DE PARCELA (5 veces)
- [ ] Nº DE GARAJE (3 veces)
- [ ] Nº DE TRASTEROS (3 veces)
- [ ] AÑO (2 veces)
- [ ] DÍA (2 veces)
- [ ] MES (2 veces)
- [ ] Nº DE PORTAL (2 veces)
- [ ] PISO (2 veces)
- [ ] SUPERFICIE (2 veces)
- [ ] COORDENADAS GEORREFERENCIADAS
- [ ] IMPORTE
- [ ] NIF/DNI
- [ ] NOMBRE DEL COLEGIO PROFESIONAL
- [ ] NOMBRE DEL NOTARIO
- [ ] Nº DE COLEGIADO/A
- [ ] Nº DE GARAJES
- [ ] Nº DE PLAZAS DE APARCAMIENTO
- [ ] PLANTA

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

En [LOCALIDAD], mi residencia, a [DÍA] de [MES] De [AÑO]

Ante mí [NOMBRE DEL NOTARIO], Notario/a del Ilustre Colegio de Notarios de Baleares y al efecto de otorgar escritura de constitución de Fundación.

COMPARECE/N:

D. [NOMBRE Y APELLIDOS], mayor de edad, casado/soltero, vecino de [LOCALIDAD], con domicilio en [LOCALIDAD], en la calle [CALLE], número [NÚMERO], piso [PISO], letra, con D.N.I. número [NIF/DNI]

D. [NOMBRE Y APELLIDOS], mayor de edad, casado/soltero, vecino de [LOCALIDAD], con domicilio en [LOCALIDAD], en la calle [CALLE], número [NÚMERO], piso [PISO], letra, con D.N.I. número [NÚMERO] como Arquitecto Técnico-Director de la Obra, Colegiado con el número [Nº DE COLEGIADO/A] en el Colegio

[ELEGIR UNA OPCIÓN: Intervienen / En nombre propio y derecho / En representación de alguien]

TIENEN

Tienen a mi juicio, según intervienen, la capacidad legal necesaria para formalizar la presente escritura de DECLARACIÓN DE OBRA NUEVA, Y CONSTITUCIÓN EN RÉGIMEN DE PROPIEDAD HORIZONTAL, y al efecto,

EXPONEN

[ELEGIR UNA OPCIÓN: Propiedad única / Propietario persona física / Propietario persona jurídica / — y además elegir: Copropiedad / Propietario personas físicas / Propietarios personas jurídicas]

OTORGAN

Declaración de obra nueva

Descripción general

Sobre la parcela descrita, bajo proyecto y dirección de obra de [NOMBRE Y APELLIDOS], [NOMBRE Y APELLIDOS] ha construido a sus expensas, con la pertinente licencia otorgada por el Ayuntamiento de [LOCALIDAD] (testimonio de la cual dejo incorporada a la presente escritura) la siguiente edificación:

Edificio situado en calle [CALLE] de (localidad), portal núm. [Nº],

Compuesto por [Nº] viviendas, [Nº DE GARAJES] garajes y [Nº DE TRASTEROS] trasteros, siendo cada uno de estos garajes y trasteros un anejo inseparable de su vivienda. Ocupa una superficie construida en planta baja de [Nº] metros cuadrados, que es igual a la superficie que ocupa en la parcela sobre la que se en encuentra construido y linda al norte y al este con terreno de cesión al ayuntamiento, al sur con la calle [CALLE] y al oeste con la calle [CALLE]; consta el edificio de una planta de sótano, destinada a garajes y trasteros; planta baja, destinada a viviendas, y portal de acceso a las viviendas; y tres plantas altas destinadas a viviendas.

Superficie [SUPERFICIE]. Cuyas coordenadas de referenciación geográfica que ocupa la edificación son [COORDENADAS GEORREFERENCIADAS]

Superficie

Ocupa el conjunto las siguientes superficies:

-La planta de sótano donde se localizan las parcelas de garaje ocupa una superficie construida de 411,42 metros cuadrados no computables a efectos urbanísticos.

-BLOQUE O CUERPO EDIFICATORIO:

a) En planta baja una superficie construida de [Nº] metros cuadrados

b) En planta primera una superficie construida de [Nº] metros cuadrados.

c) En planta segunda una superficie construida de [Nº] metros cuadrados.

d) En planta tercera una superficie construida de [Nº] metros cuadrados.

Todo ello hace un total de superficie construida de [Nº] metros cuadrados y una superficie útil aproximada para la totalidad de los elementos susceptibles de aprovechamiento independiente de metros cuadrados.

Linda el conjunto urbano, al Norte, Sur, Este y Oeste como la parcela sobre la que se ha construido. La edificación en el solar ocupa una superficie construida de 225,27 metros cuadrados.

Distribución del edificio

El edificio se distribuye del modo siguiente:

Sótano

Una PLANTA DE SÓTANO destinada a plazas o parcelas de aparcamiento (en número total de [Nº DE PLAZAS DE APARCAMIENTO]) y trasteros (en número total de [Nº DE TRASTEROS]).

Los accesos a la planta de sótano se realizan del modo siguiente:

Para vehículos, mediante una rampa ubicada en el borde Suroeste de la parcela, con acceso rodado desde la carretera de la calle [CALLE]. Y, para personas: 1.- A través del ascensor del portal del edificio; 2.- A través de un acceso peatonal que se encuentra en la puerta de acceso rodado a la planta de sótano; 3.- A través de una escalera de acceso peatonal a la planta de sótano a la que se accede desde la planta baja.

La planta de sótano se distribuye, con sus correspondientes zonas de tránsito y rodadura en [Nº] plazas de aparcamiento, numeradas del [Nº] al [Nº], inclusive, todas ellas abiertas y [Nº DE TRASTEROS] trasteros, numerados del [Nº] al [Nº], ambos inclusive. Tanto las plazas de aparcamiento como los trasteros son anejos de las viviendas. Todo lo cual se ubica dentro de la zona indicada del modo siguiente:

LAS PARCELAS numeradas del [Nº] al [Nº], ambas inclusive, se ubican a lo largo del lindero sur del edificio, a la derecha según se accede por el vial rodado y se encuentran ubicadas entre los trasteros [Nº DE TRASTERO] y [Nº DE TRASTERO], y el acceso rodado a la planta de sótano. Las parcelas [Nº DE PARCELA] a [Nº DE PARCELA], ambas inclusive, se ubican a lo largo del lindero norte del edificio, y se encuentran ubicadas entre los trasteros [Nº DE TRASTERO] y [Nº DE TRASTERO], y el límite de la planta de sótano. La parcela [Nº DE PARCELA] se ubica en el lindero norte del edificio, entre el límite de la planta de sótano y la caja de escaleras de acceso.

En cuanto a los TRASTEROS, aquellos señalados con los números [Nº] se ubican entre el muro de contención y la parcela de garaje número [NÚMERO] Los trasteros [Nº DE TRASTERO], por su parte, se encuentran ubicados entre la parcela de garaje y el distribuidor y cuarto de contadores de la luz.

Los cuartos de contadores de luz y agua se encuentran entre el trastero [Nº DE TRASTERO], y la caja del ascensor y de las escaleras.

Un recinto cerrado que es un elemento común, situado en el lindero sur del edificio, que linda con garajes [Nº DE GARAJE] y con trasteros [Nº DE TRASTERO]

Un piezómetro situado en el pasillo común entre el garaje [Nº DE GARAJE] y [Nº DE GARAJE], que está formado por un pozo de sondeo de pequeño diámetro, con arqueta circular que permite el acceso con el fin de permitir la recogida de muestras de las aguas subterráneas.

Se ubica también en esta planta el armario de telecomunicaciones o R.I.T.I, que da servicio a todo el edificio, y que se encuentra junto al trastero 5.

Planta baja

LA PLANTA BAJA, está destinada a viviendas. Y se distribuye en:

-El núcleo del portal que se compone de vestíbulo del portal, distribuidor, caja de escaleras, caja de ascensor, buzones y tres viviendas, denominadas según su posición según se accede a la planta baja por el portal y mirando de frente, de izquierda a derecha: A, B Y C.

-PLANTA PRIMERA, está destinada a viviendas. Contiene tres viviendas, señalada de izquierda a derecha subiendo la escalera: A, B Y C

-PLANTA SEGUNDA, está destinada a viviendas. Contiene tres viviendas, señalada de izquierda a derecha subiendo la escalera: A, B Y C

-PLANTA TERCERA, está destinada a viviendas. Contiene tres viviendas, señalada de izquierda a derecha subiendo la escalera: A, B Y C. Esta planta a su vez tiene los contadores de gas y el R.I.T.S.

Servidumbres

El sótano de este portal tiene una servidumbre de paso al sótano de la Parcela [Nº DE PARCELA], parcela donde se encuentra el conjunto de [Nº] viviendas. En consecuencia el sótano de este portal [Nº DE PORTAL] es predio sirviente, siendo dominante la planta de sótano [Nº DE PORTAL] de la parcela [Nº DE PARCELA] de [Nº] viviendas libres. Esta situación se podrá modificar mediante instrumento jurídico que en su día se determine

Propiedad horizontal

El edificio anteriormente descrito, está sujeto al Régimen de la Ley de Propiedad Horizontal, que se constituye formalmente en este acto, por lo cual, se describe, las partes del mismo susceptibles de propiedad privativa, que son las siguientes:

Elemento número UNO.- Vivienda señalada con la letra de la Planta [PLANTA]; tiene una superficie construida incluso con participación en elementos comunes de [Nº] metros cuadrados y útil aproximada de [Nº] metros cuadrados; linda: al Norte, con [LINDEROS]; al Sur, con [LINDEROS]; y al Oeste, con [LINDEROS]; y al Este Sur,

Este elemento tiene como anejo el uso privativo de dos zonas de terreno libre de edificación, que son un jardín y una terraza. El jardín situado en la zona norte de la vivienda, que tiene una superficie útil aproximada de [Nº] metros, linda: al Norte con [LINDEROS], al Sur con [LINDEROS] anejo en uso a esta vivienda, al Este [LINDEROS]; y al oeste con [LINDEROS]. La terraza situada en la zona sur, este y norte, que tiene una superficie útil aproximada de metros, linda: al Norte con [LINDEROS], al Sur con [LINDEROS] anejo en uso a esta vivienda, al Este con [LINDEROS]; y al oeste con

Y así mismo, tiene vinculada como anejo la parcela de garaje número [NÚMERO], situada en planta de sótano; tiene una superficie útil aproximada de [SUPERFICIE] y al Norte con [LINDEROS], al Sur con [LINDEROS] anejo en uso a esta vivienda, al Este con [LINDEROS]; y al oeste con

Y así mismo, tiene vinculado como anejo el trastero número [NÚMERO], situado en planta de sótano; tiene una superficie útil aproximada de [Nº] metros cuadrados y linda: al Norte con [LINDEROS], al Sur con [LINDEROS] anejo en uso a esta vivienda, al Este con [LINDEROS]; y al oeste con

Dicho elemento tiene una participación en los elementos comunes del conjunto del inmueble de %.

Elemento número DOS.-

Elemento número TRES.-

Licencia de edificación y certificación de técnico competente

Al objeto de dar cumplimiento a la legislación vigente el señor compareciente me exhibe Licencia de obras correspondiente al edificio objeto de la presente escritura, concedida por el Ayuntamiento de [LOCALIDAD], por medio de la Comisión de Gobierno de [DÍA] de [MES] de [AÑO], fotocopia de la cual, previamente cotejada con su original por el infrascrito notario queda unida a la presente escritura.

D. [NOMBRE Y APELLIDOS], como Arquitecto director de la obra, adscritos al Colegio [NOMBRE DEL COLEGIO PROFESIONAL], con el número [NÚMERO], certifica que la descripción de la Obra Nueva en construcción, declarada en esta escritura, se ajusta al Proyecto para el que se obtuvo la Licencia.

Seguro decenal

Al objeto de dar cumplimiento a la Ley 38/1999, de 5 de Noviembre de Ordenación de la Edificación, el compareciente acompañará con el final de obra, certificación expedida por la entidad aseguradora, acreditativa de la constitución y vigencia del contrato, así como los recibos de los pagos de dicho seguro. Testimonio de los cuales quedaran unido al acta final de obra.

Inscripción

Y que, por último, solicitan del señor Registrador de la Propiedad, la inscripción de la presente escritura.

Plano

Quedan unidos a la presente escritura [Nº] planos representativos de las plantas del edificio.

RESERVAS Y ADVERTENCIAS LEGALES

Hago las reservas y advertencias legales y, a efectos fiscales, las relativas a las obligaciones y responsabilidades que incumben a las parte en su aspecto material, formal y sancionador y a las consecuencias de toda índole que se derivarían de la inexactitud de sus declaraciones. Advierto, en especial, de la obligaciones contenidas en cuanto al plazo de presentación de esta escritura a liquidación, afección de la finca al pago del Impuesto y responsabilidades en caso de no presentación, y de las consecuencias de la aplicación de la Ley 8/1.989, señalando que las liquidaciones correspondientes a esta escritura sobre la base del valor declarado en la misma ascienden: por los conceptos y tipos de la misma aplicables, a la cantidad correspondiente a la cuota tributaria:

Bases para calculo del arancel, según lo dispuesto en los Números [Nº] y [Nº] la cantidad de [IMPORTE] euros. Todo lo referido queda sujeto a las correcciones obligadas en su caso, como consecuencia de actuaciones complementarias y facultades comprobatorias, dentro de los términos y plazos establecidos por las disposiciones citadas.

Así lo dice y otorga el señor compareciente, quien enterado de su derecho a leer por sí este documento, procedo por su elección a la lectura del mismo, en cuyo contenido se ratifica y firma.

Y yo, el Notario, DOY FE de identificar a los señores comparecientes por medio de sus documentos nacionales de identidad y de todo lo demás contenido en este instrumento público, extendido en cincuenta y un folios de papel sellado, de serie PC, números:

========================================================================
