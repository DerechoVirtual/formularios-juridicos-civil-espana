---
name: escrito-jurisdiccion-voluntaria-exigir-exhibicion-civ-1706
description: "Escrito de jurisdicción voluntaria para exigir la exhibición de libros contables. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito de jurisdicción voluntaria para exigir la exhibición de libros contables

> Formulario **CIV-1706** del plugin **Mediación, MASC, arbitraje y jurisdicción voluntaria** (`formularios-mediacion-arbitraje-y-voluntaria`) · Civil › Jurisdicción voluntaria, MASC, mediación y arbitraje · normativa revisada el 24-11-2026.

## Qué es

Por medio del presente escrito, y de conformidad con el art. 112 de la Ley 15/2015, de 2 de julio, de la Jurisdicción Voluntaria se promueve expediente en solicitud de exhibición de libros contables.

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito de jurisdicción voluntaria para exigir la exhibición de libros contables» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito de jurisdicción voluntaria para exigir la exhibición de libros contables” para mi caso». También puedes invocarla directamente con `/formularios-mediacion-arbitraje-y-voluntaria:escrito-jurisdiccion-voluntaria-exigir-exhibicion-civ-1706`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-mediacion-arbitraje-y-voluntaria:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Mediación, MASC, arbitraje y jurisdicción voluntaria) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] AÑO (4 veces)
- [ ] FECHA (3 veces)
- [ ] CALLE
- [ ] DENOMINACIÓN SOCIAL
- [ ] LO
- [ ] LUGAR
- [ ] NOMBRE COMERCIAL
- [ ] Nº DE DOCUMENTO
- [ ] NÚMERO
- [ ] OTROS DATOS
- [ ] PROVINCIA
- [ ] SEDE
- [ ] ZONA GEOGRÁFICA

## Normas que cita el formulario

- art. 112 Ley 15/2015
- art. 32.2 Código de Comercio
- art. 114 LJV
- art. 2 Código de Comercio
- art. 113.1 LJV
- art. 32.3 Código de Comercio
- art. 112 LJV
- art. 114.2 LJV

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
(1) La exigencia de abogado y procurador para plantear expediente de jurisdicción voluntaria variará, según el art 3.2 LJV, en función del expediente de que se trate, y la exigencia legal al respecto. En el supuesto específico del presente escrito, el art. 113.2 de la Ley de Jurisdicción Voluntaria exige de manera preceptiva la intervención de Abogado y Procurador para la solicitud en análisis.


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

A LA SECCIÓN DE LO MERCANTIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, en nombre y representación de la entidad [DENOMINACIÓN SOCIAL] SL [OTROS DATOS], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], como mejor proceda en derecho comparezco y DIGO:

Que por medio del presente escrito, y de conformidad con el art. 112 de la Ley 15/2015, de 2 de julio, de la Jurisdicción Voluntaria (en lo sucesivo, LJV), promuevo expediente en solicitud de exhibición de libros contables. Todo ello, en base a los siguientes

Hechos y consideraciones jurídicas:

1º) Que mi mandante es proveedor de artículos deportivos en la zona de [ZONA GEOGRÁFICA], de [PROVINCIA], y mantiene un contrato de suministro periódico, de fecha [FECHA], con D./Dña. [NOMBRE Y APELLIDOS], comerciante con establecimiento abierto al público en [LO], calle [CALLE], nº [NÚMERO], con el nombre comercial de [NOMBRE COMERCIAL]. En los últimos tres años, la facturación por dicho suministro ha supuesto un 60% del total del negocio de mi representado, convirtiéndose, de esta forma, en el cliente más importante.

2º) Que el próximo [FECHA] debe renovarse el contrato de suministro, y D./Dña. [NOMBRE Y APELLIDOS] impone, o quiere imponer, una rebaja de casi la mitad en el precio de los productos, para continuar con la relación comercial. Y ello, con el argumento de la precaria situación económica del citado negocio generada con la crisis sufrida en el sector en los últimos dos años.

3º) Dado que esa drástica rebaja del precio de los suministros supondrá una reducción de los ingresos de mi mandante, que no se puede adecuar a su coste de adquisición, y pondrá en riesgo su situación económica; es interés de éste revisar la contabilidad de D./Dña. [NOMBRE Y APELLIDOS], para comprobar tal extremo, y poder negociar, o aceptar tal sacrificio, con conocimiento de la situación real de su cliente más importante. Se reúne, en este sentido, la condición de interesado exigida en el art. 32.2 del Código de Comercio, para solicitar la exhibición de libros y documentos. A los efectos de cumplir con las exigencias de tal precepto legal, se señala expresamente la voluntad de revisar el libro de inventario y cuentas anuales correspondiente a los ejercicios de [AÑO] y [AÑO].

4º) Se acude, por ello, al expediente previsto en los arts. 112 y ss. LJV, cumpliendo con los requisitos exigidos en su art. 114 LJV, al hacer constar el derecho o interés legítimo de mi representada, con especificación de los asientos a examinar, y el objeto y finalidad de la solicitud. La misma se dirige frente al propio D./Dña. [NOMBRE Y APELLIDOS], quien opera en el mercado en su propio nombre, reuniendo los requisitos de comerciante previstos en el art. 2 del Código de Comercio, y quien está obligado a llevar una contabilidad ordenada conforme al art. 25.1 del mismo texto legal.

5º) Que es competente el Tribunal al que me dirijo conforme al art. 113.1 LJV, al encontrarse en su partido judicial el establecimiento a cuya contabilidad se refieren los libros cuya revisión se pretende.

6º) Se acompañan a esta solicitud copia del contrato de suministro, copia de las cuentas anuales de mi mandante, donde se puede comprobar la importancia de D./Dña. [NOMBRE Y APELLIDOS] en su cartera de clientes, y comunicación de este último exigiendo la citada reducción del precio.

Por todo lo expuesto, al amparo del art. 32.3 del Código de Comercio, y del art. 112 LJV,

SOLICITO AL TRIBUNAL

Que teniendo por presentado este escrito y documentos que lo acompañan y por promovido expediente de jurisdicción voluntaria para la exhibición de libros de contabilidad, y previo el traslado a D./Dña. [NOMBRE Y APELLIDOS]; se cite a las partes a la comparecencia judicial prevista en el art. 114.2 LJV, a fin de que se autorice el examen del libro de inventario y cuentas anuales de aquel, relativo a los ejercicios de [AÑO] y [AÑO].

Por ser de Justicia que pido en [LUGAR], a [FECHA].

Firma de Abogado/a	Firma de Procurador/a
