---
name: comunicacion-inquilino-acoge-sistema-no-actualizacion-civ-2475
description: "Comunicación del inquilino que se acoge al sistema de no actualización de la renta. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Comunicación del inquilino que se acoge al sistema de no actualización de la renta

> Formulario **CIV-2475** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 25-11-2026.

## Qué es

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Comunicación del inquilino que se acoge al sistema de no actualización de la renta» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Comunicación del inquilino que se acoge al sistema de no actualización de la renta” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:comunicacion-inquilino-acoge-sistema-no-actualizacion-civ-2475`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- `SKILL.md` (este fichero): qué es el formulario, para qué sirve, cómo se usa, los datos que pide, las normas que cita, los avisos de actualización y las instrucciones para Claude.
- `assets/formulario.md`: el formulario seco, tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…]. Es el texto que se rellena; no lleva explicaciones.
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] FECHA

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

Notas al pie del formulario original:
(1) En aquellos casos en que fuera procedente la actualización de la renta regulada en el apartado 11 de la Disp. Trans. Segunda de la L. 29/1994, 24 nov., efectuado el preceptivo requerimiento fehaciente por el arrendador al arrendatario, éste, en el plazo de los treinta días naturales siguientes a su recepción podrá oponerse a dicha actualización. Las consecuencias que se anudan a dicha actitud son dos:

a) El fundamental ... ...y que hace que se nos antoje como harto improbable el que se haga uso de tal facultad por los arrendatarios... ... es que el contrato de arrendamiento quedará extinguido en el plazo de ocho años, aun cuando se produzca una subrogación, contándose dicho plazo a partir de la fecha de requerimiento fehaciente del arrendador.
b) Durante el plazo que reste de subsistencia del contrato, la renta que viniere abonando el inquilino hasta el momento, incrementada con las cantidades asimiladas a ella, sólo podrá actualizarse anualmente con la variación experimentada por el Índice General Nacional del Sistema de Índices de Precios de Consumo en los doce meses inmediatamente anteriores a la fecha de cada actualización.

Ello no significa que la renta y cantidades asimiladas pasen a integrar un nuevo concepto, sino que ambas formen la base de cálculo al objeto de aplicar la revisión. Por otro lado y tratando de la repercusión del coste de los servicios y suministros regulada en el apartado 10-5 de la Disposición Transitoria Segunda de la LAU 1994, Lozano Romeral y De Fuentes Bardají (en su obra Todo sobre la nueva Ley de Arrendamientos Urbanos, Ed. Praxis, S.A., 1994, pág. 317) sostienen que si no hubiera revalorización de renta, una interpretación literal de la Ley permitiría la exigencia de las cantidades asimiladas a la renta que ya se pagaran y, asimismo, los importes correspondientes a los servidos y suministros que se percibiesen por el arrendatario a partir de la entrada en vigor de la L.A.U. Esta posibilidad debe, sin embargo, entenderse contraria a la finalidad de la norma. Por ello, entendemos que la interpretación correcta de estos preceptos para este supuesto precluiría la aplicación del apartado 10-5 en tanto no hay revalorización de renta».

Llevando a la práctica cuanto dejamos dicho, pondremos el siguiente ejemplo:

- Fecha de contrato: 10 de marzo de 1967

Renta contrato	2.500 ptas. (15,03 euros)
Incrementos renta	4.600 ptas. (27,65 euros)
Obras	8.500 ptas. (51,09 euros)
Servicios y suministros	3.000 ptas. (18,03 euros)
Total recibo	18.600 ptas. (111,79 euros)

- Actualización anual (primer año):

IPC marzo/95 (114,290)

x 100 = 5,486%

IPC marzo/94 (108,346)

- Incremento:

18. 600 x 5,486% = 1.020 ptas. (6,13 euros)

- Recibo tras practicarse la actualización:

Renta contrato	2.500 ptas. (15,03 euros)
Incrementos renta	4.600 ptas. (27,65 euros)
Obras	8.500 ptas. (51,09 euros)
Servicios y suministros	3.000 ptas. (18,03 euros)
Actualización	1.020 ptas. (6,13 euros)
I.B.I.	ptas. (euros)
Total recibo	19.620 ptas. + I.B.I. (117,92 euros + I.B.I.)

Indudablemente, y a nuestro entender, lo que no puede hacerse es englobar todo el importe del recibo antiguo en uno nuevo, como si de una nueva renta se tratase, aplicarle a la misma el I.P.C. y a partir de ahí repercutir todos los conceptos autorizados por el apartado 10 de la Disp. Trans. Segunda, pues como es llano, se produciría una duplicidad de repercusiones al mantenerse las que históricamente se venían abonando y sumarle, por otro lado, las que se produjeren a partir del 1 de enero de 1995.


### Flujo

1. **Paso 0**: comprueba Jurisprudenciator (arriba).
2. Lee entero `assets/formulario.md` (el formulario que vas a rellenar, en la carpeta de esta skill) y la parte de `../indice/marco.md` que afecte al caso. Limítate a la materia de este formulario: no añadas contenido ajeno a él.
3. Pide los datos de la lista en una sola tanda. Si un dato aparece varias veces, aclara a qué persona o acto corresponde cada vez. Lo que el usuario no sepa se queda como hueco visible con su etiqueta (p. ej. [FECHA]).
4. Resuelve cada [ELEGIR …] y cada [OPCIONAL …] según los hechos, y sustituye cualquier indicación entre paréntesis del formulario («(se describirá…)», «(indicar…)») por el contenido que corresponda. Redacta las partes que dependen del caso (hechos, motivos, descripción de bienes).
5. Aplica los avisos de actualización en el lugar que indican. Comprueba con `buscar_articulo` cada norma citada; si alguna ha cambiado, usa la redacción vigente. Si citas jurisprudencia, localízala con `buscar_sentencias` o `buscar_por_cita` y léela con `leer_sentencias`.
6. Antes de entregarlo, pasa `verificar_escrito` con las frases que citan normas o sentencias y corrige lo que señale.
7. **Documento final = el formulario tal cual, rellenado y limpio.**
   - Empieza exactamente por la primera línea de `assets/formulario.md` y sigue su estructura y su orden hasta la firma.
   - No pongas en el documento título, nombre del formulario o de la skill, código, encabezados, «Para qué sirve», leyendas, avisos, notas de uso, comentarios ni explicaciones. Tampoco marcas [ELEGIR…] u [OPCIONAL…]: ya están resueltas.
   - Formato Word (.docx, con la skill de Word disponible): **Times New Roman 11 pt** en todo el documento, **interlineado 1,15**, **texto justificado**, márgenes de 2,5 cm. Los rótulos del formulario (REUNIDOS, CLÁUSULAS, HECHOS, SUPLICO…) en su propia línea y en negrita, sin cambiar su texto.
8. En el chat (nunca dentro del documento): datos pendientes, partes redactadas por ti, normas y sentencias comprobadas con Jurisprudenciator (y, si algún dato sale de internet, cuál y su enlace) y, si es un escrito judicial o administrativo, el plazo y el órgano ante el que se presenta.

El resultado es un borrador para que lo revise un profesional antes de usarlo.
