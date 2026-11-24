---
name: recurso-apelacion-contra-sentencia-proceso-menores-civ-1306
description: "Recurso de apelación contra la sentencia de un proceso de menores. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Recurso de apelación contra la sentencia de un proceso de menores

> Formulario **CIV-1306** del plugin **Recursos civiles: reposición, apelación, casación y queja** (`formularios-recursos-civiles`) · Civil › Recursos · normativa revisada el 24-11-2026.

## Qué es

Escrito de interposición y fundamentación del recurso de apelación contra la sentencia dictada en un proceso sobre guarda y custodia, régimen de visitas y alimentos de un hijo menor, impugnando los pronunciamientos que se consideren contrarios al interés del menor.

Es un modelo de tipo **recursos**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Recurso de apelación contra la sentencia de un proceso de menores» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Recurso de apelación contra la sentencia de un proceso de menores” para mi caso». También puedes invocarla directamente con `/formularios-recursos-civiles:recurso-apelacion-contra-sentencia-proceso-menores-civ-1306`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-recursos-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Recursos civiles: reposición, apelación, casación y queja) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (5 veces)
- [ ] FECHA (4 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] Nº DE PROCEDIMIENTO (2 veces)
- [ ] AÑO
- [ ] CARGO
- [ ] DÍA
- [ ] LOCALIDAD
- [ ] MES
- [ ] NOMBRE DEL MENOR
- [ ] NOMBRE Y APELLIDOS DEL APELANTE
- [ ] NOMBRE Y APELLIDOS DEL OTRO PROGENITOR
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR
- [ ] Nº
- [ ] PROVINCIA
- [ ] RELACIÓN DE LAS PRUEBAS QUE SE SOLICITAN EN SEGUNDA INSTANCIA
- [ ] SEDE

## Normas que cita el formulario

- art. 92 Código Civil
- art. 94 Código Civil
- art. 91 Código Civil

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

- Junto a «…de Alicante, Sección 6.ª, de 5 de julio de 2004 (recurso 256/2004), entre otras.»: las dos sentencias del Tribunal Supremo constaban en el original solo con referencia editorial; completar con número de recurso o ECLI antes de citarlas.
- Junto a «… la sentencia en este extremo, fijando una pensión de [IMPORTE] euros mensuales.»: el original citaba «141 ss CC» para los alimentos entre parientes; se ha escrito «142 y siguientes», comprobar la numeración exacta de los artículos que se deseen invocar.

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

[Nota de ayuda: en el encabezamiento de las alegaciones se harán constar los pronunciamientos que se impugnan.]

A LA SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº], PARA SU REMISIÓN A LA AUDIENCIA PROVINCIAL DE [PROVINCIA]

Don/Doña [NOMBRE Y APELLIDOS DEL PROCURADOR], Procurador/a de los Tribunales, en representación de Don/Doña [NOMBRE Y APELLIDOS DEL APELANTE], en autos [Nº DE PROCEDIMIENTO] instados por mi mandante contra Don/Doña [NOMBRE Y APELLIDOS DEL OTRO PROGENITOR], comparezco y DIGO:

1) Que en fecha [FECHA] se dictó sentencia en este proceso, la cual fue notificada a esta parte en fecha [FECHA].

2) Que, entendiendo que dicha sentencia no es ajustada a Derecho, dicho sea con los debidos respetos y en términos de defensa, por medio del presente escrito interpongo contra la misma RECURSO DE APELACIÓN, impugnando los siguientes pronunciamientos: 1) Atribución de la guarda y custodia del hijo menor a [ELEGIR: la madre / el padre]; 2) Régimen de visitas [DESCRIPCIÓN DEL RÉGIMEN IMPUGNADO: por ejemplo, excesivamente restringido a dos fines de semana mensuales alternos, sin justificación alguna]; y 3) Prestación de alimentos en la cuantía de [IMPORTE] euros.

3) Que, de conformidad con lo dispuesto en el artículo 458 de la Ley de Enjuiciamiento Civil, fundo el recurso de apelación en las siguientes

ALEGACIONES

PRIMERA.– Infracción del artículo 92 del Código Civil y demás preceptos concordantes, y vulneración del principio de interés del menor.

La atribución realizada a [ELEGIR: la demandante / el demandante] Doña/Don [NOMBRE Y APELLIDOS] se ha realizado sin tener presentes ni las preferencias del menor ni los dictámenes del equipo técnico judicial y del perito Don/Doña [NOMBRE Y APELLIDOS], [ESPECIALIDAD: por ejemplo, psicólogo especializado en esta materia].

En efecto, en la legislación civil se establece como criterio prioritario a la hora de adoptar cualquier medida el del interés de los hijos menores. La jurisprudencia ha venido aplicando dicho criterio de interés del menor como prevalente a la hora de adoptar decisiones sobre la patria potestad, guarda, custodia y visitas de los hijos comunes. Así, se viene indicando que el principio rector en esta materia es el criterio del beneficio del menor o «favor filii», el cual es esencial a la hora de adoptar las medidas: sentencias del Tribunal Supremo de 11 de octubre de 1991 y de 12 de febrero de 1992; sentencia de la Audiencia Provincial de Alicante, Sección 6.ª, de 5 de julio de 2004 (recurso 256/2004), entre otras.

En este caso, entendemos que la decisión judicial no valora las concretas circunstancias que concurren en el grupo familiar, en especial [CIRCUNSTANCIAS: por ejemplo, la mala relación del menor con el progenitor al que se atribuye la guarda], sin tener en cuenta el dato fundamental de cómo se desenvuelve la vida del menor en el ámbito de uno u otro progenitor, todo lo cual ha quedado totalmente acreditado en la exploración del menor y en los dictámenes periciales emitidos en autos, siendo que la solución adoptada va en contra de la propia voluntad del menor y de su deseo libremente expresado.

Por ello, solicitamos la revocación del pronunciamiento, acordando en su lugar que se atribuya la guarda y custodia del menor a mi representado/a, fijando el régimen de visitas y la obligación de pensión alimenticia del otro progenitor en los términos interesados en nuestra demanda.

SEGUNDA.– Subsidiariamente, caso de no atribuirse la guarda y custodia a mi representado/a, la sentencia infringe el artículo 94 del Código Civil en relación con el régimen de visitas.

El régimen establecido de [RÉGIMEN ESTABLECIDO: por ejemplo, dos fines de semana alternos al mes] no se adecua al principio del interés del menor que debe presidir su adopción, cuando resulta que se han solicitado [RÉGIMEN SOLICITADO: por ejemplo, todos los fines de semana y los jueves de cada semana], sin que se haya señalado ningún régimen especial para las vacaciones estivales, restringiendo de forma totalmente injustificada el derecho del menor a comunicarse y relacionarse con mi representado/a.

En consecuencia, interesamos la revocación del pronunciamiento y que se establezca el régimen de visitas propuesto por esta parte en su escrito de demanda.

TERCERA.– Asimismo, de forma subsidiaria, para el caso de no estimarse el primer motivo, alegamos la vulneración de lo dispuesto en los artículos 91, 93 y 142 y siguientes del Código Civil sobre la prestación de alimentos.

Los ingresos de mi mandante se han reducido desde [FECHA], fecha en que [CIRCUNSTANCIA LABORAL: por ejemplo, fue recolocado por la empresa en la que presta sus servicios en el cargo de [CARGO], debido a la reestructuración de personal que practicó la empresa], pasando a percibir unos emolumentos mensuales de [IMPORTE] euros.

Por tanto, interesamos también la revocación de la sentencia en este extremo, fijando una pensión de [IMPORTE] euros mensuales.

Por lo expuesto,

SUPLICO A LA SALA: que tenga por presentado este escrito y justificante del traslado de copias, lo una a autos, y por interpuesto y formalizado, en tiempo y forma, recurso de apelación contra la sentencia dictada con fecha [FECHA] en el juicio [Nº DE PROCEDIMIENTO], seguido a instancia de [NOMBRE Y APELLIDOS] contra [NOMBRE Y APELLIDOS], al que se dará la oportuna tramitación.

A LA SALA SUPLICO: que dicte resolución revocatoria de la dictada en la instancia en los siguientes extremos:

1) Se deje sin efecto la atribución de la guarda y custodia del hijo menor [NOMBRE DEL MENOR], otorgándose la misma a mi mandante, fijando el correspondiente régimen de visitas a favor del otro progenitor y su obligación de satisfacer una pensión mensual de [IMPORTE] euros en concepto de alimentos del menor.

2) Subsidiariamente respecto del punto 1, si se mantuviera la guarda y custodia en favor del otro progenitor, se fije un régimen de visitas consistente en [RÉGIMEN DE VISITAS SOLICITADO: por ejemplo, fines de semana alternos y periodos vacacionales por mitad].

3) Subsidiariamente respecto del punto 1, si se mantuviera la guarda y custodia en favor del otro progenitor, se fije una pensión mensual por alimentos por importe de [IMPORTE] euros.

OTROSÍ PRIMERO DIGO: que se solicita, de acuerdo con lo establecido en los artículos 460 y 752 de la Ley de Enjuiciamiento Civil, LA PRÁCTICA DE LAS SIGUIENTES PRUEBAS: [RELACIÓN DE LAS PRUEBAS QUE SE SOLICITAN EN SEGUNDA INSTANCIA].

A LA SALA SUPLICO: que se acuerde el recibimiento a prueba en segunda instancia y la práctica de las pruebas en la correspondiente vista.

OTROSÍ SEGUNDO DIGO: que, de conformidad con lo dispuesto en los apartados 3.b) y 6 de la disposición adicional decimoquinta de la Ley Orgánica del Poder Judicial, acompaño a este escrito resguardo de consignación en la cuenta de Depósitos y Consignaciones abierta a nombre del Tribunal del depósito exigido para interponer el recurso, por importe de 50 euros [OPCIONAL — si ha lugar: no procede el depósito si el recurrente tiene reconocido el derecho a la asistencia jurídica gratuita o es el Ministerio Fiscal].

SUPLICO AL TRIBUNAL: que tenga por constituido el depósito, dejando interesada desde este momento su devolución para el caso de estimación total o parcial del recurso.

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Abogado/a Firma del Procurador/a
