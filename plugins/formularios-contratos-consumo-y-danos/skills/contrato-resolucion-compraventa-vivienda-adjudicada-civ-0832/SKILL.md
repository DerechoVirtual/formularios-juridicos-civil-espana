---
name: contrato-resolucion-compraventa-vivienda-adjudicada-civ-0832
description: "Contrato de resolución de compraventa de vivienda adjudicada a otro, con restitución y mejora. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de resolución de compraventa de vivienda adjudicada a otro, con restitución y mejora

> Formulario **CIV-0832** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Contrato de restitución de una vivienda adquirida por contrato privado al haber sido adjudicada con anterioridad a otra persona. Rescisión del contrato a cambio de una cantidad de dinero por las mejoras hechas en la vivienda.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de resolución de compraventa de vivienda adjudicada a otro, con restitución y mejora» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de resolución de compraventa de vivienda adjudicada a otro, con restitución y mejora” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:contrato-resolucion-compraventa-vivienda-adjudicada-civ-0832`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] NÚMERO (4 veces)
- [ ] CALLE (3 veces)
- [ ] DENOMINACIÓN SOCIAL (3 veces)
- [ ] FECHA (3 veces)
- [ ] IMPORTE (3 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] ESTADO CIVIL (2 veces)
- [ ] IMPORTE EN CIFRA (2 veces)
- [ ] AÑO
- [ ] DÍA
- [ ] LETRA
- [ ] LUGAR
- [ ] MES
- [ ] MUNICIPIO
- [ ] NIF/DNI
- [ ] Nº
- [ ] PISO

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

En [LUGAR], a [DÍA] de [MES] de [AÑO].

REUNIDOS

DE UNA PARTE,

D. [NOMBRE Y APELLIDOS], mayor de edad, [ESTADO CIVIL] (estado civil), con domicilio en [LOCALIDAD], calle [CALLE], número [NÚMERO], provisto de N.I.F. número [NÚMERO]

Y DE OTRA PARTE

D. [NOMBRE Y APELLIDOS], mayor de edad, [ESTADO CIVIL] (estado civil), en nombre y representación de la Empresa constructora [DENOMINACIÓN SOCIAL], con domicilio social en [LOCALIDAD], calle [CALLE], número [NÚMERO], provisto de N.I.F. número [NIF/DNI]

Ambas partes recíprocamente se reconocen la suficiente capacidad legal y legitimación, para llevar a efecto el presente contrato, acreditando su identidad por los documentos indicados, actuando en nombre y representación propia, y que de común acuerdo se regirán por todo lo establecido libre y voluntariamente en el mismo en virtud de las siguientes:

MANIFESTACIONES

PRIMERA.- Que D. adquirió, a D. [NOMBRE Y APELLIDOS], como representante de la constructora [DENOMINACIÓN SOCIAL] y mediante documento privado, la vivienda sita en el término municipal de [MUNICIPIO], calle [CALLE], nº [NÚMERO] piso [PISO] letra [LETRA], que ocupa una superficie de [Nº] metros cuadrados, por la cantidad de [IMPORTE] euros, tal como se muestra con la copia del contrato privado que se adjunta a este escrito.

SEGUNDA.- Que en tal momento, se entregaron las llaves de la mencionada vivienda con el objeto de que D [NOMBRE Y APELLIDOS] realizase cuantas mejoras requiriese y todo ello a cargo del adquirente.

TERCERA.- Que con fecha [FECHA], el comprador D. recibió telegrama con acuse de recibo por el que se le comunicaba por parte de dicha constructora el error material habido en la venta de la vivienda, pues ya había sido adjudicada con anterioridad a D. [NOMBRE Y APELLIDOS]

CUARTA.- Que D. había realizado durante ese lapso de tiempo una serie de mejoras en el inmueble tales como cambio del sistema eléctrico, así como nuevas instalaciones sanitarias y de calefacción y aire acondicionado, mejoras que alcanzan la suma de [IMPORTE] euros ([IMPORTE EN CIFRA] €), tal como acredita con la presentación de las facturas aportadas a este escrito.

QUINTA.- Que D. está dispuesto a rescindir el contrato privado de fecha [FECHA], por lo que, de común acuerdo fijan los siguientes,

PACTOS

I.- D. y D. [NOMBRE Y APELLIDOS] en nombre y representación de la empresa constructora [DENOMINACIÓN SOCIAL], rescinden el contrato privado de compraventa de la vivienda descrita en la manifestación primera de fecha [FECHA], recuperando éste último la posesión del inmueble en perfecto estado, con las mejoras efectuadas en la misma a costa del primitivo adquirente.

II.- D. recibe el inmueble a su entera satisfacción, entregando como contrapartida la cantidad de [IMPORTE] euros ([IMPORTE EN CIFRA] €) a que asciende la suma de las mejoras efectuadas por D. [NOMBRE Y APELLIDOS], sirviendo la firma de la presente como eficaz carta de pago.

III.- Ambas partes, con renuncia de su fuero propio si lo tuvieren, se someten expresamente a los Tribunales de [LOCALIDAD] para la interpretación o cualquier cuestión litigiosa que derive de este contrato.

Y para que conste, firman por duplicado y a un solo efecto en el lugar y fecha ‘ut supra’.

========================================================================
