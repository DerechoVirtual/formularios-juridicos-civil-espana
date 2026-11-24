---
name: contrato-transaccion-poner-fin-pleito-ya-iniciado-civ-0728
description: "Contrato de transacción para poner fin a un pleito ya iniciado. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de transacción para poner fin a un pleito ya iniciado

> Formulario **CIV-0728** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de transacción para poner fin a un pleito ya iniciado» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de transacción para poner fin a un pleito ya iniciado” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:contrato-transaccion-poner-fin-pleito-ya-iniciado-civ-0728`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (10 veces)
- [ ] DENOMINACIÓN SOCIAL (9 veces)
- [ ] IMPORTE (4 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] MES (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] CALLE
- [ ] DÍA
- [ ] FECHA
- [ ] FECHA DE LA ENTREGA
- [ ] NOMBRE DEL REPRESENTADO/A

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

- Junto a «…UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD)»: La LO 15/1999 y su Reglamento (RD 1720/2007) fueron sustituidos por el Reglamento (UE) 2016/679 (RGPD) y la LO 3/2018, de 5 de diciembre (LOPDGDD). Fuente: LO 3/2018, disposición derogatoria única.

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

En [LOCALIDAD], a [DÍA] de [MES] 20

ANTECEDENTES

I. Como consecuencia de las relaciones comerciales de suministro habidas en el último año entre don [NOMBRE Y APELLIDOS] y la entidad [DENOMINACIÓN SOCIAL], han surgido diferentes controversias sobre la siguiente cuestión: calidad de parte de los géneros vendidos por la entidad [DENOMINACIÓN SOCIAL] en las últimas tres entregas de prendas de vestir en el domicilio de don

II. Don [NOMBRE Y APELLIDOS] se ha negado a abonar cantidad alguna del precio de las tres últimas entregas indicadas. El precio de dichas entregas era el siguiente:

• 1ª entrega de [FECHA DE LA ENTREGA]: 4.500 euros;

• 2ª entrega de [IMPORTE]: euros;

• 3ª entrega de [IMPORTE], [IMPORTE] euros.

La cantidad total adeudada es, pues, de 16.300 euros.

III. La entidad [DENOMINACIÓN SOCIAL], a través de sus legales representantes, ha interpuesto juicio declarativo ordinario de menor cuantía contra don [NOMBRE Y APELLIDOS], que en la actualidad se tramita ante la Plaza de la Sección de lo Civil del Tribunal de Instancia número [NÚMERO], de la ciudad de [LOCALIDAD], con el número de autos 000000/2007. En la actualidad, las partes están citadas para comparecencia al acto de audiencia previa al juicio (previsto en el artículo 414 de la Ley de Enjuiciamiento Civil de 2000) el día [FECHA] de [MES] de 200

IV. Los comparecientes, con el firme propósito de poner fin al litigio ya entablado, formalizan contrato de transacción, solventando todas las controversias existentes entre ellos hasta el día de la fecha, renunciando a la continuación de cualquier acción judicial en relación con los hechos indicados en los antecedentes I y II y, señaladamente, al procedi- miento indicado en el antecedente III.

V. Ambas partes se proponen, además, solicitar la homologación judicial de la presente transacción conforme a lo previsto en los artículos 19 y 415 de la Ley de Enjuiciamiento Civil de 2000.

VI. Mediante el presente contrato de transacción que aquí y ahora se formaliza, adoptan las siguientes,

CLÁUSULAS

La entidad [DENOMINACIÓN SOCIAL] se compromete en este acto a retirar toda la mercancía correspondiente a la segunda entrega a su completo cargo, cuenta y riesgo en el domicilio de don [NOMBRE Y APELLIDOS], sito en la ciudad de [LOCALIDAD], calle [CALLE], número

La retirada de la mercancía tendrá lugar dentro de diez días naturales a contar desde la notificación de la homologación judicial del presente documento. De no ser así y pasados dichos diez días sin que la entidad [DENOMINACIÓN SOCIAL] cumpla con esta obligación, don [NOMBRE Y APELLIDOS], quedará en libertad para disponer libremente de tales géneros.

La entidad [DENOMINACIÓN SOCIAL] declara en este acto haber revisado en el domicilio de don [NOMBRE Y APELLIDOS] la mercancía indicada; reconoce expresamente que se corresponde con la entregada el 3 noviembre 2006 y que se encuentra ya debidamente embalada en el citado domicilio a su disposición.

En este acto, don [NOMBRE Y APELLIDOS] abona la cantidad total de [IMPORTE] euros, que la entidad [DENOMINACIÓN SOCIAL] declara recibir íntegramente. Sirva este documento como justificante y recibo de total pago de dicha cantidad.

Ambas partes declaran expresamente que no tienen nada más que reclamarse entre sí a consecuencia de las relaciones comerciales consignadas en los antecedentes del presente contrato, dando por zanjada aquí y ahora y para el futuro toda contienda entre ambas a consecuencia de tales hechos.

Tanto la entidad [DENOMINACIÓN SOCIAL], como don [NOMBRE Y APELLIDOS], se comprometen a comparecer al acto de audiencia previa ante la Plaza de la Sección de lo Civil del Tribunal de Instancia número [NÚMERO], en autos de juicio ordinario de menor cuantía número 0000000/2007, debidamente representados y, si es a través de procurador de los tribunales, mediante poder especial, tal como exige para transigir el artículo 25.2 de la Ley de Enjuiciamiento Civil de 2000, a los fines de manifestar haber llegado a un acuerdo y solicitar de la Plaza que homologue lo acordado en el presente documento, a cuyo efecto, será presentado para su ratificación en la Plaza por la representación procesal de la entidad [DENOMINACIÓN SOCIAL] (demandante en el proceso) que expresamente se compromete a presentarlo en la Plaza de la Sección de lo Civil del Tribunal de Instancia el día de la comparecencia a la audiencia previa.

Ambas partes declaran tener capacidad jurídica y de obrar suficiente y poder de disposición para esta transacción.

Cada una de las partes abonará las costas causadas a su instancia hasta ahora y de aquí hasta que obtenga firmeza el auto de homologación judicial de la transacción. Las costas comunes (de haberlas), serán abonadas por mitad.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

Y, en prueba de conformidad y para que conste a los efectos oportunos, firman el presente documento por triplicado y a un solo efecto en el lugar y fecha indicados al principio.

Don [NOMBRE Y APELLIDOS] Don [NOMBRE Y APELLIDOS] En representación de [NOMBRE DEL REPRESENTADO/A]
