---
name: solicitud-liquidacion-regimen-participacion-propuesta-civ-0106
description: "Solicitud de liquidación del régimen de participación y propuesta de liquidación (Derecho catalán). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud de liquidación del régimen de participación y propuesta de liquidación (Derecho catalán)

> Formulario **CIV-0106** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud de liquidación del régimen de participación y propuesta de liquidación (Derecho catalán)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud de liquidación del régimen de participación y propuesta de liquidación (Derecho catalán)” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:solicitud-liquidacion-regimen-participacion-propuesta-civ-0106`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (24 veces)
- [ ] IMPORTE (8 veces)
- [ ] AÑO (5 veces)
- [ ] MES (3 veces)
- [ ] Nº (3 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] FECHA (2 veces)
- [ ] DÍA
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] SEDE

## Normas que cita el formulario

- art. 232 Código Civil
- art. 807 LEC
- art. 806 LEC
- art. 437.1 LEC
- art. 5 Ley Orgánica 1/2025
- art. 232 CC
- art. 232.20.3 CC

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

- Junto a «…Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Denominación legal: Sección de Familia, Infancia y Capacidad. Si no existe en el partido, conoce la Sección Civil o la Única (art. 86.3-4 LOPJ). Fuente: LOPJ arts. 84.2.a) y 86 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «….3-4 LOPJ). Fuente: LOPJ arts. 84.2.a) y 86 (redacc. LO 1/2025, BOE-A-2025-76).]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. «De los de» es residuo de los varios juzgados de una plaza. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

Don [NOMBRE Y APELLIDOS], Procurador de los Tribunales, actuando en nombre y representación de Don [NOMBRE Y APELLIDOS], según tengo debidamente acreditado en autos de separación conyugal núm. [Nº] del año [AÑO], bajo la dirección letrada de Don [NOMBRE Y APELLIDOS], comparezco ante la Sección Civil del Tribunal de Instancia nº (o de Familia) de los de [LOCALIDAD] y, como mejor proceda en Derecho, DIGO:

Que en la citada representación procesal solicito la LIQUIDACIÓN DEL RÉGIMEN ECONÓMICO MATRIMONIAL DE PARTICIPACIÓN EN LAS GANANCIAS habido entre mi representado y Doña [NOMBRE Y APELLIDOS], en base a los siguientes

HECHOS

Que el día [FECHA], del mes [MES], del año [AÑO], los esposos, de vecindad civil catalana, otorgaron escritura pública de constitución por la que establecieron el régimen económico de participación en las ganancias al 50%, constando en dicha escritura que se acompaña como documento número [Nº DE DOCUMENTO] el patrimonio inicial de cada cónyuge.

Que el día [FECHA], del mes [MES] del año [AÑO], ha recaído sentencia núm. [Nº] del año [AÑO], en la actualidad firme, que ha disuelto el citado régimen de participación, y así consta en autos.

Que según consta en la propuesta de liquidación que se acompaña a la presente solicitud como documento [Nº DE DOCUMENTO], la diferencia entre el patrimonio inicial y el final de los cónyuges arroja, en ambos casos, un resultado positivo, y siendo mayor el resultado obtenido por Don [NOMBRE Y APELLIDOS] que el obtenido por Doña [NOMBRE Y APELLIDOS], procede, de conformidad con lo establecido en el artículo 232-21 y concordantes del Código Civil de Cataluña, que, en concepto de liquidación del régimen, Don [NOMBRE Y APELLIDOS] entregue a Doña [NOMBRE Y APELLIDOS] la cantidad de [IMPORTE] euros, que es la mitad de la diferencia entre el valor del incremento de D. [NOMBRE Y APELLIDOS] y el de Dª [NOMBRE Y APELLIDOS].

A los anteriores hechos son de aplicación los siguientes

Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento nº [Nº DE DOCUMENTO]

FUNDAMENTOS DE DERECHO

Competencia

Es competente el Tribunal al que me dirijo, conforme a lo dispuesto en el artículo 807 de la LEC.

Procedimiento

La disposición adicional tercera, apartado 2, del CC de Cataluña se remite al procedimiento establecido en los artículos 806 y 811 de la LEC, siendo de aplicación éste último precepto al régimen de participación.

Cumplimiento de los requisitos de procedibilidad

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC en relación con el art. 437.1 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

Liquidación del régimen

Son de aplicación los artículos 232-18 (inicio de la liquidación); 232-19 (determinación del patrimonio final), y 232-20 (determinación del patrimonio inicial) del Código Civil de Cataluña.

Determinación del crédito

El artículo 232-21 del CC de Cataluña establece que, en defecto de pacto, el crédito de participación se determina con las siguientes reglas: a) si únicamente uno de los cónyuges ha obtenido un incremento patrimonial, calculado por la diferencia entre el patrimonio final y el inicial, el otro o sus sucesores tienen derecho a la mitad del valor de este incremento; b) si ambos cónyuges han obtenido un incremento patrimonial, quien haya obtenido menos, o sus sucesores, tienen derecho a la mitad de la diferencia entre el valor de su propio incremento y el del otro cónyuge; y c) si ninguno de los cónyuges ha obtenido un incremento patrimonial, no existe crédito de participación.

Por lo expuesto,

SUPLICO AL TRIBUNAL: Que tenga por presentado este escrito con los documentos acompañados y sus copias; admita todo ello; por formulada por el Procurador que suscribe, en nombre y representación de Don [NOMBRE Y APELLIDOS], SOLICITUD DE LIQUIDACIÓN DEL RÉGIMEN MATRIMONIAL DE PARTICIPACIÓN habido entre mi representado y Doña [NOMBRE Y APELLIDOS]; acuerde señalar la comparecencia prevista en el artículo 811.3 y 4 de la Ley de Enjuiciamiento Civil; y habiendo, acuerdo, se levante la correspondiente acta, y se ejecute lo acordado, señalándose, en caso contrario, la vista a que se refiere el artículo 811.5 de la misma Ley procesal, continuando los trámites por el juicio verbal, en el que se dicte sentencia de conformidad con lo interesado en el extremo Quinto del presente escrito, es decir, que en concepto de liquidación del régimen, Don [NOMBRE Y APELLIDOS] entregue a Doña [NOMBRE Y APELLIDOS] la cantidad de [IMPORTE] euros, que es la mitad de la diferencia entre los respectivos incrementos de patrimonio, dando a los autos el impulso procesal con arreglo a derecho..

Es justicia que insto en [LUGAR], a [DÍA] de [MES] de [AÑO].

Firmas de Letrado y Procurador.

MODELO DE PROPUESTA DE LIQUIDACIÓN EN RÉGIMEN DE PARTICIPACIÓN

CÁLCULO DE PATRIMONIOS INICIAL Y FINAL

El patrimonio inicial de Don [NOMBRE Y APELLIDOS] está estimado en un importe total de [IMPORTE] euros, según valoración en el momento de la extinción ( art. 232.20.3 CCCat) según la relación de bienes y derechos, y deducidas las obligaciones y cargas, que se recogen en la escritura de constitución (en su caso, se incluirían los bienes expresados en el artículo 232-20.2 CCCat).

El patrimonio final de Don [NOMBRE Y APELLIDOS] se estima en un total de [IMPORTE] euros, conforme a la relación de bienes y derechos, y deducidas las obligaciones, que se relacionan a continuación.

(se relacionarán y acreditarán documentalmente los activos y deudas, conforme al artículo 232-19 del Código Civil de Cataluña)

La diferencia entre el patrimonio inicial y el final arroja un incremento de [IMPORTE] euros.

El patrimonio inicial de Doña [NOMBRE Y APELLIDOS] está estimado en un importe total de [IMPORTE] euros, según valoración en el momento de la extinción ( art. 232.20.3 CCCat), de acuerdo a la relación de bienes y derechos, y deducidas las obligaciones y cargas, que se recogen en la escritura de constitución (en su caso, se incluirían los bienes expresados en el artículo 232-20.2 CCCat).

El patrimonio final de Doña [NOMBRE Y APELLIDOS] se estima en un total de [IMPORTE] euros, conforme a la relación de bienes y derechos, y deducidas las obligaciones, que se relacionan a continuación.

(se relacionarán y acreditarán documentalmente los activos y deudas, conforme al artículo 232-19 del Código Civil de Cataluña)

La diferencia entre el patrimonio inicial y el final arroja un incremento de ... euros.

PROPUESTA DE LIQUIDACIÓN

Puesto que la diferencia entre el patrimonio inicial y el final de los cónyuges arroja, en ambos casos, un resultado positivo, siendo mayor el resultado obtenido por Don [NOMBRE Y APELLIDOS] que el obtenido por Doña [NOMBRE Y APELLIDOS], procede, de conformidad con lo establecido en el artículo 232-21 del Código Civil de Catauña, que, en concepto de liquidación del régimen, Don [NOMBRE Y APELLIDOS] entregue a Doña [NOMBRE Y APELLIDOS] la cantidad de [IMPORTE] euros, que es la mitad de la diferencia entre el valor del incremento de D. [NOMBRE Y APELLIDOS] con el de Dª [NOMBRE Y APELLIDOS].

========================================================================
