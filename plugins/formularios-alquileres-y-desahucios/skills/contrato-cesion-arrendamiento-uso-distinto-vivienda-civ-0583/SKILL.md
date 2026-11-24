---
name: contrato-cesion-arrendamiento-uso-distinto-vivienda-civ-0583
description: "Contrato de cesión de arrendamiento para uso distinto de vivienda, con o sin existencias. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de cesión de arrendamiento para uso distinto de vivienda, con o sin existencias

> Formulario **CIV-0583** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 24-11-2026.

## Qué es

Contrato de cesión de contrato de arrendamiento para uso distinto de vivienda contemplando dos posibilidades: (i) incluyendo el arrendamiento tanto de maquinaria como de existencias; y (ii) sin el arrendamiento de existencias.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de cesión de arrendamiento para uso distinto de vivienda, con o sin existencias» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de cesión de arrendamiento para uso distinto de vivienda, con o sin existencias” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:contrato-cesion-arrendamiento-uso-distinto-vivienda-civ-0583`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (9 veces)
- [ ] IMPORTE (6 veces)
- [ ] IMPORTE EN CIFRA (6 veces)
- [ ] NÚMERO (5 veces)
- [ ] ESTADO CIVIL (3 veces)
- [ ] FECHA (3 veces)
- [ ] LUGAR (2 veces)
- [ ] NIF/DNI (2 veces)
- [ ] ACTIVIDAD
- [ ] PORCENTAJE
- [ ] PROFESIÓN

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

Contrato de cesión de contrato de arrendamiento para uso distinto de vivienda contemplando dos posibilidades: (i) incluyendo el arrendamiento tanto de maquinaria como de existencias; y (ii) sin el arrendamiento de existencias.

Notas al pie del formulario original:
(1) Los arrendamientos para uso distinto del de vivienda se rigen por la voluntad de las partes, en su defecto, por lo dispuesto en la Ley 29/1994 de 24 de noviembre de Arrendamientos Urbanos —concretamente para la cesión de contrato el artículo 32 LAU 1994— y, supletoriamente, por lo dispuesto en el Código Civil. Por lo tanto, se pueden incluir los pactos contractuales que las partes consideren oportunos con la limitación general del artículo 1255 CCiv.

========================================================================


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

En [LUGAR], a [FECHA].

REUNIDOS

DE UNA PARTE,

Don/Doña [NOMBRE Y APELLIDOS] (cedente), estado civil [ESTADO CIVIL], mayor de edad, con domicilio en.., número [NÚMERO], provisto de N.I.F.

Y DE OTRA,

Don/Doña [NOMBRE Y APELLIDOS], estado civil [ESTADO CIVIL], mayor de edad, con domicilio en. [NÚMERO], número [NÚMERO], provisto de N.I.F. [NIF/DNI]

[OPCIONAL — incluir si procede]

(Podrá también comparecer el arrendador)

Don/Doña [NOMBRE Y APELLIDOS] /Doña [NOMBRE Y APELLIDOS], [PROFESIÓN], estado civil [ESTADO CIVIL], mayor de edad, con domicilio en. [NÚMERO], número [NÚMERO], provisto de N.I.F. [NIF/DNI]

Ambas partes intervienen en su propio nombre y derecho, reconociéndose, como así lo verifican en este acto, la mutua capacidad legal necesaria para la formalización del presente documento y, con su expreso consentimiento,

EXPONEN

I.- Que Don/Doña [NOMBRE Y APELLIDOS] es arrendatario del siguiente local de negocio: Se adjunta copia de dicho contrato firmada por las partes.

El cedente viene ejerciendo sin interrupción la actividad de [ACTIVIDAD] en el local referenciado desde [FECHA], contando con todos los permisos legales y licencias para el ejercicio de la mencionada actividad, encontrándose al corriente en el pago de los tributos que gravan el ejercicio de la actividad.

La renta del arrendamiento, incrementada con las cantidades asimiladas a la misma, es de [IMPORTE] euros ([IMPORTE EN CIFRA] €) mensuales.

[OPCIONAL — en caso de cesión de contrato de arrendamiento con existencias]

Son de propiedad del cedente la maquinaria y existencias cuyo inventario consta en documento anexo, que firmado por las partes se acompaña.

Dichos bienes propiedad del cedente están libres de cargas y gravámenes y totalmente pagados.

II.- Que interesa a cedente y cesionario el traspaso del mencionado local de negocio, y sus existencias, y lo llevan a efecto de conformidad con las siguientes,

CLAUSULAS

PRIMERA.-

[OPCIONAL — en caso de cesión de contrato de arrendamiento con existencias]

Don/Doña [NOMBRE Y APELLIDOS] traspasa a Don/Doña [NOMBRE Y APELLIDOS] el local de negocio descrito en el apartado I del presente documento, con todas sus instalaciones y servicios. Se cede la propiedad al cesionario de la maquinaria y existencias a que se ha hecho referencia en el mismo apartado.

[OPCIONAL — en caso de cesión de contrato de arrendamiento sin existencias]

Don/Doña [NOMBRE Y APELLIDOS] traspasa a Don/Doña [NOMBRE Y APELLIDOS] el local de negocio descrito en el apartado I del presente documento, con todas sus instalaciones y servicios. La cesión únicamente comprende el local y sus servicios e instalaciones, pero no las existencias.

SEGUNDA .-

El cesionario deberá permanecer en el local, sin traspasarlo, el plazo mínimo de un año, destinándolo durante este tiempo, por lo menos, a negocios de la misma clase al que venía ejerciendo el cedente.

TERCERA .-

El precio del traspaso se fija en [IMPORTE] euros ([IMPORTE EN CIFRA] €), que se abonan por el cesionario al cedente en la siguiente forma:

Del precio total, corresponden [IMPORTE] euros ([IMPORTE EN CIFRA] €) al local de negocio y [IMPORTE] euros ([IMPORTE EN CIFRA] €) a la maquinaria y existencias.

De conformidad con lo convenido con la propiedad del local, el cesionario ha retenido la suma de [IMPORTE] euros ([IMPORTE EN CIFRA] €), para su entrega a la propiedad en concepto de participación en el precio del traspaso del local.

CUARTA .-

De conformidad con lo convenido con la propiedad la renta se aumentará con un [PORCENTAJE] %, con lo que la renta mensual ascenderá a [IMPORTE] euros ([IMPORTE EN CIFRA] €) mensuales.

QUINTA .-

En este acto toma posesión del local de negocio el cesionario asumiendo los derechos y obligaciones que correspondían al cedente derivados del contrato de arrendamiento del que trae causa este contrato. De igual forma, el cesionario toma posesión de la maquinaria y de las existencias.

SEXTA .-

El cedente se compromete a notificar de forma fehaciente a la propiedad la realización del traspaso, el precio percibido, el nombre y domicilio del cesionario, y que éste ha contraído la obligación de permanecer en el local, sin traspasarlo, durante un año, y destinarlo durante este tiempo, como mínimo, a negocios de la misma clase que los que venía ejerciendo el cedente.

SÉPTIMA .-

El cedente no asume ninguna responsabilidad por la prohibición o limitación del ejercicio de la actividad por las autoridades administrativas o judiciales.

Y leído el presente documento, ambas partes lo firman en señal de conformidad y ratificación de su contenido, haciéndolo por duplicado y a un sólo efecto.

En [LUGAR], a [FECHA].

Firma de EL/LA CEDENTE:

Firma de EL/LA CESIONARIA
