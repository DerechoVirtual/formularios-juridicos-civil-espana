---
name: demanda-nulidad-acuerdo-mediacion-civ-1732
description: "Demanda de nulidad de un acuerdo de mediación. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de nulidad de un acuerdo de mediación

> Formulario **CIV-1732** del plugin **Mediación, MASC, arbitraje y jurisdicción voluntaria** (`formularios-mediacion-arbitraje-y-voluntaria`) · Civil › Jurisdicción voluntaria, MASC, mediación y arbitraje · normativa revisada el 24-11-2026.

## Qué es

Demanda de nulidad de acuerdo de mediación.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de nulidad de un acuerdo de mediación» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de nulidad de un acuerdo de mediación” para mi caso». También puedes invocarla directamente con `/formularios-mediacion-arbitraje-y-voluntaria:demanda-nulidad-acuerdo-mediacion-civ-1732`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-mediacion-arbitraje-y-voluntaria:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Mediación, MASC, arbitraje y jurisdicción voluntaria) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] AÑO (7 veces)
- [ ] DÍA (7 veces)
- [ ] IMPORTE (7 veces)
- [ ] MES (7 veces)
- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] FECHA
- [ ] LUGAR
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] Nº DE EXPEDIENTE
- [ ] PARTE DEMANDADA
- [ ] SEDE

## Normas que cita el formulario

- art. 23.4 Ley 5/2012
- art. 1265 Código Civil
- art. 1269 Código Civil
- art. 1303 Código Civil
- art. 23.4 LM
- art. 50 LEC
- art. 249.2 LEC
- art. 7.2 Ley 10/2012

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…LIDOS]: ========================================================================»: requisito de procedibilidad del art. 5 LO 1/2025 — antes de presentar la demanda hay que intentar un medio adecuado de solución de controversias (MASC) y acreditarlo con la demanda (arts. 264.4.º y 399.3 LEC), salvo las materias excluidas del art. 5.2. Fuente: LO 1/2025, arts. 5 a 7 (BOE-A-2025-76).

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D. [NOMBRE Y APELLIDOS] Procurador de los Tribunales, actuando en representación de [NOMBRE DEL REPRESENTADO/A], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño a este escrito, por medio de la presente, al amparo de lo dispuesto en el artículo 23.4 de la Ley 5/2012, de 6 de julio, de mediación en asuntos civiles y mercantiles, formulo demanda de impugnación del acuerdo de mediación de fecha [DÍA] de [MES] de [AÑO] alcanzado en expediente de mediación número [Nº DE EXPEDIENTE], demanda que dirijo contra D. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], en base a los siguientes

Hechos

Mi representado y el demandado iniciaron un procedimiento de mediación con motivo del accidente sufrido por el demandado cuando fue contratado por mi representado para realizar unas reparaciones en el tejado de su vivienda en fecha [DÍA] de [MES] de [AÑO] Al realizar los trabajos de reparación, el techo de la vivienda de mi representado cedió por su mal estado, cayendo el demandado al piso inferior y sufriendo lesiones.

Para dirimir la controversia, se siguió procedimiento de mediación ante el mediador D. [NOMBRE Y APELLIDOS], alcanzado las partes un acuerdo en virtud del cual mi representado se comprometía a indemnizar al demandado en la cantidad de [IMPORTE] euros por las lesiones sufridas (acompaño como documentos [Nº DE DOCUMENTO] copia del expediente de mediación y del acuerdo de mediación de fecha [DÍA] de [MES] de [AÑO]).

La impugnación de lo convenido en mediación viene originada por el dolo con que actuó el demandado al simular que las lesiones sufridas le incapacitaron completamente para su trabajo habitual, cuando lo cierto es que mi representado ha tenido conocimiento posterior que el demandado está trabajando en la empresa de construcción [DENOMINACIÓN SOCIAL], realizando el mismo trabajo para el que fue contratado y con una antigüedad anterior al inicio del procedimiento de mediación, lo que patentiza el dolo con el que ha actuado.

En efecto, la mala fe con que actuó el demandado se constata por la mera lectura del acuerdo de mediación acompañado como documento número [Nº DE DOCUMENTO], concretamente en el apartado tercero, cuando el demandado manifiesta expresamente que como consecuencia de las lesiones sufridas está impedido para realizar cualquier tipo de trabajo, habiendo solicitado la invalidez permanente ante el Instituto Nacional de la Seguridad Social, lo cual determinó que se fijara una indemnización por el elevado importe de [IMPORTE] euros por tratarse de lesiones que produjeron una «incapacidad permanente».

Mi representado, en la lícita creencia que el demandado actuaría con la exigible buena fe que debe informar su conducta, dio por ciertas las afirmaciones de que estaba totalmente impedido para trabajar, según las lesiones que constaban en el informe médico de fecha [DÍA] de [MES] de [AÑO] que aportó el demandado en el procedimiento de mediación, y lógicamente también creyó de buena fe que el demandado había solicitado la invalidez permanente como consecuencia de este desgraciado accidente, por lo cual otorgó su consentimiento a la pretensión del demandado a ser indemnizado dicho concepto, abonando la indemnización convenida en el acuerdo de mediación.

Sin embargo, tales hechos han resultado absolutamente falsos, puesto que el demandado está trabajando actualmente para la empresa [DENOMINACIÓN SOCIAL], incluso desde antes de iniciarse el procedimiento de mediación como acreditaremos oportunamente, y desde luego no tiene ninguna incapacidad para desarrollar su trabajo, como falsamente afirmó en el procedimiento de mediación.

De los hechos expuestos queda constatado que el consentimiento prestado por esta parte se obtuvo como consecuencia de la conducta dolosa del demandado, quien a sabiendas creó una apariencia de estar impedido para desarrollar su trabajo, simulando estar en situación de incapacidad permanente, con el único fin de ser indemnizado por mi representado, quien satisfizo la cantidad de [IMPORTE] euros por este concepto en cumplimiento del acuerdo de mediación.

Por este motivo, es de aplicación el art. 1265 del Código Civil que establece la nulidad del consentimiento prestado por dolo, siendo que la conducta del demandado reúne los dos requisitos de la conducta dolosa establecidos en el art. 1269 del Código Civil como son el subjetivo, o ánimo de perjudicar al actor, obteniendo una indemnización a la que no tenía derecho, y el objetivo, al simular consciente y deliberadamente una situación de incapacidad para su trabajo que no tenía.

Asimismo, y de conformidad a lo dispuesto en el art. 1303 y siguientes del Código Civil, el demandado debe indemnizar a esta parte por los daños y perjuicios sufridos que comprenden las cantidades ya satisfechas, que ascienden a [IMPORTE] euros, y el interés moratorio de dichas cantidades desde el [DÍA] de [MES] de [AÑO], fecha de la entrega, que asciende a [IMPORTE] euros.

Por lo expuesto, se ejercita acción de nulidad, conforme a lo dispuesto en el art. 23.4 de la LM, pretendiendo la indemnización de daños y perjuicios derivada de la conducta dolosa del demandado.

Fundamentos de derecho

Primero.– Competencia

Corresponde a las secciones civiles de los tribunales de instancia de [LOCALIDAD], conforme a lo dispuesto en los arts. 50 de la LEC y 85.1º LOPJ.

Segundo.– Procedimiento y cuantía

Debe seguirse el proceso ordinario conforme a lo dispuesto en el art. 249.2 de la LEC y siendo la cuantía de este proceso la de [IMPORTE] euros.

Tercero.– Legitimación

Le corresponde a esta parte la legitimación activa y la pasiva al demandado, conforme a lo que dispone el artículo 23.4 de la Ley 5/2012.

Cuarto.– Acción ejercitada

Es de aplicación lo dispuesto en el art. 23.4 de la Ley 5/2012 que establece que «contra lo convenido en el acuerdo de mediación sólo podrá ejercitarse la acción de nulidad por las causas que invalidan los contratos», lo que debe ser puesto en relación con lo dispuesto en los arts. 1265, 1269, 1270 y concordantes del Código Civil. El art. 1265 del C.Civil determina que «será nulo el consentimiento prestado por error, violencia, intimidación o dolo», a la vez que el art. 1269 del Código Civil establece que «hay dolo cuando, con palabras o maquinaciones insidiosas de parte de uno de los contratantes, es inducido el otro a celebrar un contrato que, sin ellas, no hubiera hecho».

Quinto.– Efectos

Articulos 1300 y siguientes del Código Civil.

Sexto.– Costas

Artículo 394 LEC, debiéndose imponer las costas al demandado por su mala fe.

En base a lo anterior,

SUPLICO AL TRIBUNAL que tenga por presentada la presente demanda con los documentos a ella adjuntos y sus copias, en la representación que ostento, y se tenga por formulada demanda de juicio ordinario contra [PARTE DEMANDADA] en impugnación del acuerdo de mediación de fecha [DÍA] de [MES] de [AÑO] y en su virtud, tras los trámites legales, se dicte sentencia por la que se declare la nulidad del acuerdo de mediación de fecha [DÍA] de [MES] de [AÑO] y se condene al demandado a indemnizar a mi representado en la cantidad de [IMPORTE] euros, con más los intereses correspondientes, todo ello con condena en costas al demandado.

[OPCIONAL — incluir si procede]

OTROSÍ DIGO Que estando la presente demanda sujeta al abono de la tasa por el ejercicio de la potestad jurisdiccional fijada por la Ley 10/2012, de 20 de noviembre, modificada por RDL 3/2013 y Ley 25/2015, de 28 julio, y desarrollada por Orden HAP/2662/2012, de 13 de diciembre, siendo mi representada personas jurídica no exenta de su pago, se acompaña a la presente demanda como documento nº [Nº DE DOCUMENTO] la correspondiente autoliquidación con el ejemplar para la Administración de Justicia debidamente validado y en el que consta el pago de la cantidad de 300 euros correspondiente a la cuota fija, sin que se incluya la cuota variable prevista en el artículo 7.2 de la Ley 10/2012 al haber sido declarado inconstitucional y nulo por la STC 140/2016, de 21 de julio.

En virtud de lo anterior,

SUPLICO AL TRIBUNAL que tenga por hecha la anterior manifestación a los efectos pertinentes y por acompañado el documento justificativo del abono de la tasa.

En [LUGAR], a [FECHA].

Abogado/a	Procurador/a

Fdo. D./Dña. [NOMBRE Y APELLIDOS]: Fdo. D./Dña. [NOMBRE Y APELLIDOS]:

========================================================================
