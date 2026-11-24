---
name: solicitud-medidas-cautelares-proceso-filiacion-civ-0191
description: "Solicitud de medidas cautelares en un proceso de filiación. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud de medidas cautelares en un proceso de filiación

> Formulario **CIV-0191** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud de medidas cautelares en un proceso de filiación» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud de medidas cautelares en un proceso de filiación” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:solicitud-medidas-cautelares-proceso-filiacion-civ-0191`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] ACTO O RESOLUCIÓN
- [ ] AÑO
- [ ] DÍA
- [ ] LUGAR
- [ ] MES
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] Nº DE DOCUMENTO
- [ ] NÚMERO

## Normas que cita el formulario

- art. 768 LEC
- art. 734 LEC
- art. 768.1 LEC
- art. 768.3 LEC
- art. 148 CC
- art. 142 Código Civil
- art. 9.7 CC
- art. 728 LEC
- art. 394.1 LEC
- art. 736.1 LEC

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

- Junto a «…CIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.

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

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA

Don [NOMBRE Y APELLIDOS], Procurador de los Tribunales, en nombre y representación de [NOMBRE DEL REPRESENTADO/A], según tengo acreditado en los autos de proceso de filiación número [NÚMERO] ante el Tribunal comparezco y como mejor proceda en Derecho DIGO:

Que en la representación que ostento y al amparo de lo dispuesto en el artículo 768 de la LEC, formulo solicitud de MEDIDAS CAUTELARES a favor de mi mandante, la cual baso en los siguientes

HECHOS

PRIMERO Que el procedimiento de reclamación de la filiación seguido contra [ACTO O RESOLUCIÓN] existen indicios manifiestos en orden a una relación paterno/materno filial entre demandante y demandado, generando el deber de alimentos que impone la legislación civil. La situación es especialmente urgente, habida cuenta que mi representado carece de medios de vida.

SEGUNDO Que como principio de prueba de las manifestaciones vertidas, se aporta a los autos el certificado de la pendencia de un juicio de desahucio por falta de pago en la vivienda en que reside el actor y certificación de la entidad pública en relación a la situación de desempleo, sin percibir ningún tipo de subsidio (documentos [Nº DE DOCUMENTO]).

A los efectos de audiencia, y al margen de lo recogido al respecto en el artículo 734 LEC, pueden testificar sobre los hechos relatados y sobre la precaria situación económica de mi mandante las siguientes personas [NOMBRE Y APELLIDOS].

A los anteriores Hechos le son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

Competencia

El artículo 768.2 de la Ley de Enjuiciamiento civil permite que reclamada judicialmente la filiación, el juzgador competente pueda acordar un derecho de alimentos provisionales a cargo del demandado y, en su caso, adoptar las medidas de protección referidas en el artículo 768.1 LEC.

Procedimiento

El procedimiento para la concesión de medidas cautelares en estos casos se establece en el artículo 768.3 LEC, según el cual se practicará la audiencia previa de las personas que pudieran resultar afectadas, siendo de aplicación lo dispuesto en los artículos 734 a 736 LEC, y sin que sea necesariamente exigible una caución al solicitante de las medidas. Debe matizarse, sin embargo, que la urgencia de la situación admite acordar las medidas solicitadas sin más trámites, mandando citar a los interesados a una comparecencia, a celebrar dentro de los diez días siguientes y en la que, tras oír las alegaciones de los comparecientes sobre la procedencia de las medidas adoptadas, resolverá el juzgador por medio de auto.

Derecho de alimentos entre parientes

Bajo la prerrogativa del artículo 39.3 de la Constitución, los artículos 142 a 153 del Código civil regulan el derecho de alimentos entre parientes, y cobra especial importancia el texto del artículo 148 CC, según el cual la obligación en dar alimentos será exigible desde que la persona que tenga derecho a percibirlos los necesitare para subsistir. En puridad, los artículos 142 y 143 del Código Civil comportan un efecto o consecuencia, producto de una previa declaración de la paternidad controvertida. Pero la esencia del derecho cautelar, orientado a ese fin a la vista de la presente demanda, supera la naturaleza asegurativa característica y tiende a la anticipatoria, en virtud del interés público que prima en esta materia.

El derecho de abono nace desde la fecha en que se interponga la demanda, que a la vista de los autos es de [IMPORTE] En atención de los preceptos citados, se pretende medida cautelar relativa a la condena solicitada, que lo es de una pensión alimenticia mensual de [IMPORTE] euros, para satisfacer las necesidades del demandante, que afirma ser hijo del demandado. La pensión indicada deberá incrementarse en la medida que lo haga el coste de la vida, y modificándose a la par que los ingresos del demandado. En su caso, también sería de aplicación el artículo 9.7 CC, en materia de Derecho internacional privado.

Peligro por la mora procesal. Apariencia de buen derecho. Caución

Que en tanto se solicitan medidas de protección contenidas en el artículo 768.1 LEC, como principio de prueba del peligro que corren en este momento los intereses personales y patrimoniales de mi representado, conviene reiterar que las facultades del falso padre supondrían una despatrimonialización del menor. Se cumplen en el presente caso las exigencias del artículo 728 LEC, que exigen periculum in mora y fumus boni iuri, matizándose la innecesariedad de la caución.

Costas procesales

Que con arreglo a lo dispuesto en el artículo 394.1 LEC, las costas procesales de la primera instancia se impondrán a la parte que haya visto rechazadas todas sus pretensiones, salvo que el tribunal aprecie, y así lo razone, que el caso presentaba serias dudas de hecho o de derecho. El proceder seguido para la concesión o denegación de la medida cautelar solicitada se acomoda a la regla de vencimiento aludida, en virtud del artículo 736.1 LEC.

Por lo expuesto,

AL TRIBUNAL SOLICITO: Que tenga por presentado este escrito con los documentos acompañados y copia de todo ello, lo admita, tenga por realizadas las manifestaciones vertidas; y que sin previa audiencia y demás trámites con arreglo a Derecho se acuerden las MEDIDAS CAUTELARES pretendidas en favor de mi representado, sin que se le requiera de caución alguna, con imposición a la parte adversa las costas procesales de este procedimiento, sin perjuicio de que tras la preceptiva comparecencia se ratifique lo acordado, dando a los autos el impulso procesal con arreglo a Derecho.

Es Justicia que insto en [LUGAR], a [DÍA] de [MES] de [AÑO].

Firmas de Letrado y Procurador.

========================================================================
