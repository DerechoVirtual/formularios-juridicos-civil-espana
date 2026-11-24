---
name: solicitud-propuesta-liquidacion-regimen-matrimonial-civ-0242
description: "Solicitud y propuesta de liquidación del régimen matrimonial por un cónyuge (foral vasca). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud y propuesta de liquidación del régimen matrimonial por un cónyuge (foral vasca)

> Formulario **CIV-0242** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Escrito por el que uno de los cónyuges, una vez formado el inventario y disuelto el régimen económico matrimonial de comunicación foral (País Vasco), presenta la propuesta de liquidación del régimen y de división del remanente, conforme al artículo 810 de la Ley de Enjuiciamiento Civil.

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud y propuesta de liquidación del régimen matrimonial por un cónyuge (foral vasca)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud y propuesta de liquidación del régimen matrimonial por un cónyuge (foral vasca)” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:solicitud-propuesta-liquidacion-regimen-matrimonial-civ-0242`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] IMPORTE (4 veces)
- [ ] AÑO (3 veces)
- [ ] RELACIÓN E IMPORTE (3 veces)
- [ ] NOMBRE Y APELLIDOS DEL OTRO CÓNYUGE (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL REPRESENTADO (2 veces)
- [ ] Nº DE PROCEDIMIENTO (2 veces)
- [ ] RELACIÓN Y DESCRIPCIÓN DETALLADA DE LOS BIENES (2 veces)
- [ ] SEDE (2 veces)
- [ ] DÍA
- [ ] LOCALIDAD
- [ ] MES
- [ ] NOMBRE Y APELLIDOS DEL CÓNYUGE
- [ ] NOMBRE Y APELLIDOS DEL LETRADO
- [ ] Nº

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

A LA SECCIÓN [ELEGIR: CIVIL / DE FAMILIA, INFANCIA Y CAPACIDAD] DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

Don/Doña [NOMBRE Y APELLIDOS DEL PROCURADOR], Procurador de los Tribunales, actuando en nombre y representación de [ELEGIR: Don / Doña] [NOMBRE Y APELLIDOS DEL REPRESENTADO], según tengo debidamente acreditado en autos núm. [Nº DE PROCEDIMIENTO] del año [AÑO], y bajo la dirección letrada de [ELEGIR: Don / Doña] [NOMBRE Y APELLIDOS DEL LETRADO], ante la Sección [ELEGIR: Civil / de Familia, Infancia y Capacidad] del Tribunal de Instancia de [SEDE], comparezco y, como mejor proceda en Derecho, DIGO:

Que concluido el inventario y una vez firme la resolución que declara disuelto el régimen económico matrimonial de mi poderdante con su [ELEGIR: esposa / esposo] [NOMBRE Y APELLIDOS DEL OTRO CÓNYUGE], en virtud de la propuesta de inventario previamente presentada por el mismo, procede, a petición de cualquiera de los cónyuges, la liquidación del expresado régimen económico matrimonial de comunicación foral.

Por lo que, y de conformidad con lo dispuesto en el artículo 810 de la Ley de Enjuiciamiento Civil, acompaño con el presente escrito la propuesta de liquidación del expresado régimen económico matrimonial con la división del remanente entre los interesados.

En su virtud,

AL TRIBUNAL SUPLICO: Que teniendo por presentado este escrito con la propuesta de liquidación que le acompaña con sus copias, se sirva admitirlo y, en su virtud, previos los trámites con arreglo a Derecho, acuerde señalar el día y hora en que los cónyuges, [ELEGIR: Don / Doña] [NOMBRE Y APELLIDOS DEL CÓNYUGE] y [ELEGIR: Don / Doña] [NOMBRE Y APELLIDOS DEL OTRO CÓNYUGE], deberán comparecer ante el Letrado de la Administración de Justicia al objeto de alcanzar un acuerdo y, en su defecto, designar contador y, en su caso, peritos, para la práctica de las operaciones divisorias, dando a los autos el impulso procesal con arreglo a Derecho.

Es justicia que insto en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firmas del Letrado y del Procurador

MODELO DE PROPUESTA DE LIQUIDACIÓN

PROPUESTA DE LIQUIDACIÓN

Que presenta [ELEGIR: Don / Doña] [NOMBRE Y APELLIDOS DEL PROCURADOR], Procurador de los Tribunales, actuando en nombre y representación de [ELEGIR: Don / Doña] [NOMBRE Y APELLIDOS DEL REPRESENTADO], en procedimiento de [ELEGIR: separación / divorcio / nulidad] [ELEGIR: contencioso / de mutuo acuerdo] núm. [Nº DE PROCEDIMIENTO], del año [AÑO], al amparo de lo dispuesto en el artículo 810.2 de la Ley de Enjuiciamiento Civil.

Pago por deudas a terceros: [RELACIÓN E IMPORTE]

Reintegros e indemnizaciones debidas a [ELEGIR: Don / Doña] [NOMBRE Y APELLIDOS]: [RELACIÓN E IMPORTE]

Reintegros e indemnizaciones debidas a [ELEGIR: Don / Doña] [NOMBRE Y APELLIDOS]: [RELACIÓN E IMPORTE]

Remanente: [IMPORTE]

ADJUDICACIONES QUE SE PROPONEN

LOTE a favor de [ELEGIR: Don / Doña] [NOMBRE Y APELLIDOS], compuesto de los siguientes bienes: [RELACIÓN Y DESCRIPCIÓN DETALLADA DE LOS BIENES]

Valor total del mismo: [IMPORTE]

LOTE a favor de [ELEGIR: Don / Doña] [NOMBRE Y APELLIDOS], compuesto de los bienes que a continuación se indican: [RELACIÓN Y DESCRIPCIÓN DETALLADA DE LOS BIENES]

Valor total del mismo: [IMPORTE]

DIFERENCIA

Diferencia a favor de [ELEGIR: Don / Doña] [NOMBRE Y APELLIDOS]: [IMPORTE]

Entrega de dicho importe por [ELEGIR: Don / Doña] [NOMBRE Y APELLIDOS], a [ELEGIR: Don / Doña] [NOMBRE Y APELLIDOS], en compensación de la diferencia en el valor de las adjudicaciones.
