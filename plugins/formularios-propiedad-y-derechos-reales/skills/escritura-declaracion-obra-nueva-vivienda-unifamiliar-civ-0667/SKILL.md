---
name: escritura-declaracion-obra-nueva-vivienda-unifamiliar-civ-0667
description: "Escritura de declaración de obra nueva de vivienda unifamiliar. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escritura de declaración de obra nueva de vivienda unifamiliar

> Formulario **CIV-0667** del plugin **Propiedad, posesión, servidumbres e hipotecas** (`formularios-propiedad-y-derechos-reales`) · Civil › Propiedad y derechos reales · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escritura de declaración de obra nueva de vivienda unifamiliar» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escritura de declaración de obra nueva de vivienda unifamiliar” para mi caso». También puedes invocarla directamente con `/formularios-propiedad-y-derechos-reales:escritura-declaracion-obra-nueva-vivienda-unifamiliar-civ-0667`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-propiedad-y-derechos-reales:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Propiedad, posesión, servidumbres e hipotecas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (12 veces)
- [ ] LOCALIDAD (7 veces)
- [ ] LINDEROS (4 veces)
- [ ] NÚMERO (4 veces)
- [ ] CALLE (3 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] AÑO (2 veces)
- [ ] DÍA (2 veces)
- [ ] MES (2 veces)
- [ ] NIF/DNI (2 veces)
- [ ] PISO (2 veces)
- [ ] IMPORTE
- [ ] NOMBRE DEL COLEGIO PROFESIONAL
- [ ] NOMBRE DEL NOTARIO
- [ ] Nº DE BAÑOS
- [ ] Nº DE HABITACIONES

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

D. [NOMBRE Y APELLIDOS], mayor de edad, casado/soltero, vecino de [LOCALIDAD], con domicilio en [LOCALIDAD], en la calle [CALLE], número [NÚMERO], piso [PISO], letra, con D.N.I. número [NIF/DNI]

[ELEGIR UNA OPCIÓN: Intervienen / En nombre propio y derecho / En representación de alguien]

TIENEN

A mi juicio, la capacidad legal necesaria para formalizar esta escritura de DECLARACIÓN DE OBRA NUEVA, y a tal efecto,

EXPONEN

[ELEGIR UNA OPCIÓN: Propiedad única / Propietario persona física / Propietario persona jurídica / — y además elegir: Copropiedad / Propietarios personas físicas / Propietarios personas jurídicas]

Antecedentes

Que sobre el solar descrito y previas las correspondientes autorizaciones y bajo dirección técnica de D. se ha construido con la correspondiente licencia de obras una vivienda unifamiliar de [Nº] metros cuadrados totales, construidos con plantas sótano, bajas y altas, cuya obra nueva se describirá a continuación y de la cual se solicita su inscripción en el Registro de la Propiedad sin adeudar nada por lo ejecutado.

Declaración de obra nueva

Procede a la declaración de obra nueva sobre el solar citado, que quedará descrita de la siguiente forma:

VIVIENDA UNIFAMILIAR edificada sobre una porción de terreno sito en la localidad de [LOCALIDAD], con frente a la calle [CALLE] donde está señalada con los números [Nº] y [Nº]. Su solar ocupa una superficie de [Nº] metros cuadrados y se compone de Planta sótano destinada a garaje y trastero, con una superficie construida de [Nº] metros cuadrados; Planta baja, con una superficie construida de [Nº] metros cuadrados, destinada a cocina, comedor, habitación y baño; Planta primera destinada a [Nº DE HABITACIONES] habitaciones, [Nº DE BAÑOS] baños, con una superficie de [Nº] metros cuadrados.

Tejado con teja árabe con una superficie construida de [Nº] metros cuadrados.

Linda: por su frente, con [LINDEROS], donde le corresponde el número [NÚMERO]; por la derecha, entrando, con [LINDEROS] y [LINDEROS] donde le corresponden los números [Nº]; por la izquierda con [LINDEROS], y por el fondo con

Las coordenadas de referenciación geográfica de la porción de suelo ocupada por la edificación son

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

Bases para calculo del arancel, según lo dispuesto en de los Números [Nº] y [Nº] la cantidad de [IMPORTE] euros. Todo lo referido queda sujeto a las correcciones obligadas en su caso, como consecuencia de actuaciones complementarias y facultades comprobatorias, dentro de los términos y plazos establecidos por las disposiciones citadas.

Así lo dice y otorga el señor compareciente, quien enterado de su derecho a leer por sí este documento, procedo por su elección a la lectura del mismo, en cuyo contenido se ratifica y firma.

Y yo, el Notario, DOY FE de identificar a los señores comparecientes por medio de sus documentos nacionales de identidad y de todo lo demás contenido en este instrumento público, extendido en cincuenta y un folios de papel sellado, de serie PC, números:

========================================================================
