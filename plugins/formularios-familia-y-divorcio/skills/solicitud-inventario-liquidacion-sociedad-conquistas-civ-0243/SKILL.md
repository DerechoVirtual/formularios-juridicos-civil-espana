---
name: solicitud-inventario-liquidacion-sociedad-conquistas-civ-0243
description: "Solicitud de inventario en la liquidación de la sociedad de conquistas (Derecho foral navarro). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud de inventario en la liquidación de la sociedad de conquistas (Derecho foral navarro)

> Formulario **CIV-0243** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud de inventario en la liquidación de la sociedad de conquistas (Derecho foral navarro)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud de inventario en la liquidación de la sociedad de conquistas (Derecho foral navarro)” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:solicitud-inventario-liquidacion-sociedad-conquistas-civ-0243`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (18 veces)
- [ ] IMPORTE (9 veces)
- [ ] LOCALIDAD (9 veces)
- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] CALLE (4 veces)
- [ ] AÑO (3 veces)
- [ ] FOLIO (3 veces)
- [ ] LIBRO (3 veces)
- [ ] PISO (3 veces)
- [ ] PUERTA (3 veces)
- [ ] TOMO (3 veces)
- [ ] FECHA (2 veces)
- [ ] MARCA/MODELO (2 veces)
- [ ] SEDE (2 veces)
- [ ] C.P.
- [ ] COLOR
- [ ] DENOMINACIÓN SOCIAL
- [ ] DÍA
- [ ] ENTIDAD BANCARIA
- [ ] LUGAR
- [ ] MATRÍCULA
- [ ] MES
- [ ] NOMBRE DE LA URBANIZACIÓN
- [ ] NOMBRE Y APELLIDOS DEL ABOGADO
- [ ] Nº DE BASTIDOR

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

### Avisos de actualización (2) — se aplican en el texto, nunca se copian en el documento

- Junto a «…SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º LOS DE [LOCALIDAD]»: Denominación legal: Sección de Familia, Infancia y Capacidad. Si no existe en el partido, conoce la Sección Civil o la Única (art. 86.3-4 LOPJ). Fuente: LOPJ arts. 84.2.a) y 86 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…LIDOS] ante la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. «De los de» es residuo de los varios juzgados de una plaza. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º LOS DE [LOCALIDAD]

Don [NOMBRE Y APELLIDOS], Procurador de los Tribunales, actuando en nombre y representación de Don [NOMBRE Y APELLIDOS], según tengo acreditado en autos de separación conyugal núm. [Nº] del año [AÑO], y bajo la dirección letrada de Don [NOMBRE Y APELLIDOS] ante la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº] comparezco y, como mejor proceda en Derecho, DIGO:

1) Que en la indicada representación y a través del presente escrito, y habiéndose admitido la demanda de separación (o de nulidad o de divorcio o de disolución del régimen económico matrimonial) del matrimonio constituido por mi mandante y Doña [NOMBRE Y APELLIDOS], vecina de la localidad de [LOCALIDAD], calle [CALLE], núm. piso [PISO], puerta [PUERTA], código postal [C.P.], ambos de vecindad civil navarra, por medio del presente escrito solicito la FORMACIÓN DE INVENTARIO, de conformidad con lo dispuesto en el artículo 808 de la Ley de Enjuiciamiento Civil, concordantes y de pertinente aplicación.

2) Que a tal efecto acompaño propuesta de inventario de la sociedad conyugal de conquistas por el que se rige el citado matrimonio y documentos justificativos de sus diferentes partidas.

Por lo expuesto,

AL TRIBUNAL SUPLICO: Que tenga por presentado este escrito con la propuesta de inventario y documentos justificativos de sus diferentes partidas acompañados y sus copias, admita todo ello y, en su virtud, se proceda a la FORMACIÓN DE INVENTARIO, mandando citar al efecto a los cónyuges Don [NOMBRE Y APELLIDOS] y Doña [NOMBRE Y APELLIDOS], señalando día y hora, para que con el Letrado de la Administración de Justicia formalicen el inventario de esa comunidad matrimonial con arreglo al régimen de la sociedad conyugal de conquistas.

Es justicia que insto en [LUGAR], a [DÍA] de [MES] de [AÑO].

Firmas del Letrado y del Procurador [NOMBRE Y APELLIDOS DEL ABOGADO]

MODELO DE PROPUESTA DE INVENTARIO

PROPUESTA DE INVENTARIO

Que presenta Don [NOMBRE Y APELLIDOS], Procurador de los Tribunales, actuando en nombre y representación de Don [NOMBRE Y APELLIDOS], en procedimiento de separación conyugal contenciosa núm. [Nº], del año [AÑO], al amparo de lo dispuesto en el artículo 808.2 de la ley de Enjuiciamiento Civil.

ACTIVO DE LA SOCIEDAD

1.-VIVIENDA sita en la localidad de [LOCALIDAD], calle [CALLE], núm. [Nº], piso [PISO], puerta [PUERTA], de una superficie de [Nº] metros cuadrados, y que es la finca registral núm. [Nº], inscrita en el Registro de la Propiedad de [LOCALIDAD] al Tomo [TOMO], Libro [LIBRO], Folio [FOLIO], con un valor de tasación de [IMPORTE] euros, tal y como resulta de la valoración efectuada por la sociedad de tasación inmobiliaria

2.-PLAZA DE PARKING sita en la localidad de [LOCALIDAD], calle [CALLE], núm. [Nº], piso [PISO], puerta [PUERTA], de una superficie de [Nº] metros cuadrados, y que es la finca registral núm. [Nº], inscrita en el Registro de la Propiedad de [LOCALIDAD] al Tomo [TOMO], Libro [LIBRO], Folio [FOLIO], valorada en la cantidad de [IMPORTE] euros, tal y como resulta de la valoración efectuada por la sociedad de tasación inmobiliaria

3.-CHALÉ sito en la localidad de [LOCALIDAD], calle [CALLE], núm. [Nº], de la Urbanización [NOMBRE DE LA URBANIZACIÓN], de una superficie construida de [Nº] metros cuadrados, y que es la finca registral núm. [Nº], inscrita en el Registro de la Propiedad de [LOCALIDAD] al Tomo [TOMO], Libro [LIBRO], Folio [FOLIO], valorado en la cantidad de [IMPORTE] euros, tal y como resulta de la valoración efectuada por la sociedad de tasación inmobiliaria

4.-VEHÍCULO marca [MARCA/MODELO], modelo [MARCA/MODELO], número de bastidor [Nº DE BASTIDOR], con matrícula [MATRÍCULA], de color [COLOR], valorado según certificado emitido por el concesionario oficial de la marca en la localidad de [LOCALIDAD], en el importe de [IMPORTE] euros.

5.- CRÉDITO DE LA SOCIEDAD frente a los cónyuges por un importe de - euros

En prueba de las anteriores manifestaciones se acompañan las valoraciones antes mencionadas, señaladas como Documento núm. [Nº], Documento núm. [Nº], Documento núm. [Nº], Documento núm. [Nº], y documento núm. [Nº], respectivamente.

PASIVO DE LA SOCIEDAD

1.-HIPOTECA por importe de [IMPORTE] euros y vencimiento [FECHA], concedida por la entidad financiera [ENTIDAD BANCARIA], que grava la vivienda descrita en el apartado 1 del activo, y de la que, a fecha de hoy, y tal como consta en el certificado emitido por la citada entidad financiera que se acompaña como Documento núm. [Nº], queda todavía por pagar la suma de [IMPORTE] euros.

2.-PRÉSTAMO concedido por la financiera [DENOMINACIÓN SOCIAL] por importe de [IMPORTE] euros y vencimiento [FECHA], que grava el vehículo citado en el apartado 4 del activo, y del que todavía resta por pagar la cantidad de [IMPORTE] euros.

3.-CRÉDITO DE LOS CÓNYUGES frente a la sociedad por un importe de [IMPORTE] euros

4.-DEUDA DE LA SOCIEDAD respecto a

========================================================================
