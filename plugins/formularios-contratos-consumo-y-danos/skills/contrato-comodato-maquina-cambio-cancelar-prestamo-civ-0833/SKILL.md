---
name: contrato-comodato-maquina-cambio-cancelar-prestamo-civ-0833
description: "Contrato de comodato de una máquina a cambio de cancelar un préstamo personal. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de comodato de una máquina a cambio de cancelar un préstamo personal

> Formulario **CIV-0833** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Contrato de comodato de una máquina por el que el propietario (comodante) la cede al comodatario para su uso en un taller, y con ello se cancela un préstamo personal que el comodante debía al comodatario. Regula las condiciones de uso, los gastos, la valoración de la máquina para caso de pérdida o deterioro, la duración y la sumisión a tribunales.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de comodato de una máquina a cambio de cancelar un préstamo personal» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de comodato de una máquina a cambio de cancelar un préstamo personal” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:contrato-comodato-maquina-cambio-cancelar-prestamo-civ-0833`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS DEL COMODATARIO (7 veces)
- [ ] NOMBRE Y APELLIDOS DEL COMODANTE (5 veces)
- [ ] LOCALIDAD, CALLE Y NÚMERO (3 veces)
- [ ] ESTADO CIVIL (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] IMPORTE EN LETRA (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NIF (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] ACTIVIDAD
- [ ] AÑO
- [ ] DENOMINACIÓN DEL TALLER
- [ ] DÍA
- [ ] FECHA
- [ ] MES
- [ ] Nº
- [ ] PLAZO

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

### Avisos de actualización (1) — se aplican en el texto, nunca se copian en el documento

- Al principio del formulario: el comodato es esencialmente gratuito (art. 1740 del Código Civil); pactar como contraprestación la cancelación de una deuda puede aproximar el contrato al arrendamiento o a una dación de uso en pago. Conviene valorar la calificación jurídica y redactar con cuidado las cláusulas quinta y séptima.

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

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO]

REUNIDOS

DE UNA PARTE, D./Dña. [NOMBRE Y APELLIDOS DEL COMODANTE], mayor de edad, [ESTADO CIVIL], con domicilio en [LOCALIDAD, CALLE Y NÚMERO], provisto de N.I.F. número [NIF].

Y DE OTRA PARTE, D./Dña. [NOMBRE Y APELLIDOS DEL COMODATARIO], mayor de edad, [ESTADO CIVIL], con domicilio en [LOCALIDAD, CALLE Y NÚMERO], provisto de N.I.F. número [NIF].

Ambas partes recíprocamente se reconocen la suficiente capacidad legal y legitimación para llevar a efecto el presente contrato de comodato, acreditando su identidad por los documentos indicados, actuando en nombre y representación propia, y que de común acuerdo se regirán por todo lo establecido libre y voluntariamente en el contenido de las siguientes:

ESTIPULACIONES

Primera.- Que D./Dña. [NOMBRE Y APELLIDOS DEL COMODANTE] es propietario de la máquina [DESCRIPCIÓN DE LA MÁQUINA OBJETO DE ESTE COMODATO: marca, número de serie, potencia y demás características técnicas], destinada a [UTILIDAD DE LA MÁQUINA: materiales que recicla, fabrica o compone, etc.], y que entrega a D./Dña. [NOMBRE Y APELLIDOS DEL COMODATARIO], en perfecto estado de funcionamiento y conservación. Que dicha máquina se entrega y se recibe en calidad de comodante y comodatario respectivamente.

Segunda.- Que D./Dña. [NOMBRE Y APELLIDOS DEL COMODATARIO] recibe la máquina descrita en la anterior estipulación, en este acto a su entera satisfacción sin tener ninguna observación negativa que hacer, en cuanto a su funcionamiento y conservación, y manifiesta estar interesado en tenerla para utilizarla en el taller [DENOMINACIÓN DEL TALLER] sito en [LOCALIDAD, CALLE Y NÚMERO], destinado a la actividad de [ACTIVIDAD] y del cual es propietario.

Tercera.- D./Dña. [NOMBRE Y APELLIDOS DEL COMODATARIO] podrá utilizar la máquina de referencia para uso exclusivo suyo, dándole la finalidad de funcionamiento en la actividad que se desarrolla en su taller, sin que pueda ser cedida, vendida, arrendada o traspasada a terceras personas.

Cuarta.- D./Dña. [NOMBRE Y APELLIDOS DEL COMODATARIO] utilizará la máquina de referencia sin que esto le suponga ningún gasto por el uso de la misma, estando obligado única y exclusivamente a satisfacer los gastos que ocasiona el traslado y montaje, al igual que los que suponga en su día la devolución hasta que quede instalada en perfecto estado de funcionamiento en su lugar de origen, y hará efectivos igualmente aquellos gastos que la máquina requiera en su conservación y reparaciones propias del uso.

Quinta.- D./Dña. [NOMBRE Y APELLIDOS DEL COMODANTE] (comodante) reconoce y manifiesta expresamente que debe la cantidad de [IMPORTE EN LETRA] euros ([IMPORTE] €) a D./Dña. [NOMBRE Y APELLIDOS DEL COMODATARIO] (comodatario), como consecuencia de un préstamo personal que se llevó a cabo con fecha [FECHA] y por consiguiente anterior a este contrato y que, ante la imposibilidad de poderle hacer efectiva dicha cantidad y con el fin de saldar la deuda, cede en comodato la máquina de referencia, con el consentimiento y a plena satisfacción de las dos partes en las condiciones establecidas en las anteriores y posteriores estipulaciones, considerándose, una vez se dé por finalizado este contrato, que la deuda ha quedado saldada y finiquitada.

Sexta.- Los contratantes aceptan la valoración que la máquina tiene efectuada por medio de tasación de persona especializada y en calidad de peritos de plena confianza de las partes y que asciende a [IMPORTE EN LETRA] euros ([IMPORTE] €), con el propósito de que D./Dña. [NOMBRE Y APELLIDOS DEL COMODATARIO], comodatario en este contrato, hará efectivo el importe de la misma a D./Dña. [NOMBRE Y APELLIDOS DEL COMODANTE], comodante, en los supuestos de que la máquina se pierda, deteriore o quede inservible para el uso y fin en el que se ha entregado, siendo obligatorio satisfacer dicha cantidad, aunque la causa que lo motivare no sea imputable al comodatario, si bien deduciría la parte de la deuda que quedase pendiente, estableciéndose para ello un plazo de [PLAZO].

Séptima.- El presente contrato se establece por un período de [Nº] [ELEGIR: años / meses], y una vez hayan transcurrido, se devolverá la máquina ya referenciada a D./Dña. [NOMBRE Y APELLIDOS DEL COMODANTE], comodante de este contrato, cancelándose por tanto la deuda existente y sin tener los contratantes nada que pedirse ni reclamarse respectivamente.

Octava.- Ambas partes, con renuncia de su fuero propio si lo tuvieren, se someten expresamente a los Tribunales de [LOCALIDAD] para la interpretación o cualquier cuestión litigiosa que derive de este contrato.

Y para que conste, firman por duplicado y a un solo efecto en el lugar y fecha «ut supra».

COMODATARIO: D./Dña. [NOMBRE Y APELLIDOS]

COMODANTE: D./Dña. [NOMBRE Y APELLIDOS]
