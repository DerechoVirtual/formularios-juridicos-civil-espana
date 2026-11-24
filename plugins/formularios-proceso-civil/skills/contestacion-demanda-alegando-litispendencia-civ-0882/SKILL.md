---
name: contestacion-demanda-alegando-litispendencia-civ-0882
description: "Contestación a la demanda alegando litispendencia internacional (artículo 29 Bruselas I bis). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contestación a la demanda alegando litispendencia internacional (artículo 29 Bruselas I bis)

> Formulario **CIV-0882** del plugin **Proceso civil: demandas, contestaciones, prueba y vista** (`formularios-proceso-civil`) · Civil › Escritos procesales (demanda, contestación, prueba, vista) · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contestación a la demanda alegando litispendencia internacional (artículo 29 Bruselas I bis)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contestación a la demanda alegando litispendencia internacional (artículo 29 Bruselas I bis)” para mi caso». También puedes invocarla directamente con `/formularios-proceso-civil:contestacion-demanda-alegando-litispendencia-civ-0882`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-proceso-civil:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Proceso civil: demandas, contestaciones, prueba y vista) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FUNDAMENTOS (4 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] EXPONER LOS HECHOS (2 veces)
- [ ] Nº DE PROCEDIMIENTO (2 veces)
- [ ] ÓRGANO JUDICIAL (2 veces)
- [ ] AÑO
- [ ] COLEGIO
- [ ] DATOS DEL PROCEDIMIENTO
- [ ] DÍA
- [ ] FECHA
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] MES
- [ ] Nº DE COLEGIADO/A
- [ ] Nº DE DOCUMENTO
- [ ] NÚMERO
- [ ] TIPO Y Nº DE PROCEDIMIENTO

## Normas que cita el formulario

- art. 394 LEC

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

- Junto a «…SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA N.º [NÚMERO] de la ciudad de [LOCALIDAD]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

Contestación a la demanda en la que se plantea excepción de litispendencia internacional del artículo 29 del RB I bis.

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA N.º [NÚMERO] de la ciudad de [LOCALIDAD]

D. [NOMBRE Y APELLIDOS] Procurador de los Tribunales, en nombre y representación de D. [NOMBRE Y APELLIDOS], en virtud de apoderamiento apud acta/poder notarial según tengo acreditado en autos de juicio [Nº DE PROCEDIMIENTO] seguidos ante el Tribunal [ÓRGANO JUDICIAL] y asistido de la intervención del Letrado D. [NOMBRE Y APELLIDOS], Abogado del Ilustre Colegio de [COLEGIO], con número de colegiado [Nº DE COLEGIADO/A];

Comparezco ante el Tribunal [ÓRGANO JUDICIAL] en sede de Autos [TIPO Y Nº DE PROCEDIMIENTO] y como mejor proceda en Derecho, DIGO:

Que por el presente escrito, formulo CONTESTACIÓN A LA DEMANDA basada en los siguientes hechos y fundamentos de derecho:

HECHOS

Previo.—Que existe un pleito pendiente de resolución con el mismo objeto, partes y causa ante la Corte de Londres [DATOS DEL PROCEDIMIENTO] Dicha causa se inició por demanda de fecha [FECHA] y siendo su estado procesal (pendiente de admisión/admitida/) según consta en la documental que se acompaña.

Primero.— Con carácter subsidiario al anterior, que de ser estimado impediría la continuidad del proceso, en el ejercicio del derecho de defensa se contestan los hechos correlativos de la demanda que a continuación se relacionan.

Hechos conformes [EXPONER LOS HECHOS].

Negación de hechos [EXPONER LOS HECHOS] basada en los documentos siguientes [Nº DE DOCUMENTO].

FUNDAMENTOS DE DERECHO

Primero.— De orden procesal.

Legitimación [FUNDAMENTOS], capacidad para ser parte [FUNDAMENTOS], postulación procesal [FUNDAMENTOS], procedimiento [Nº DE PROCEDIMIENTO].

Se interesa del presente tribunal que estime la excepción de litispendencia internacional prevista en el artículo 29 del Reglamento 1215/2012, de 12 de diciembre de 2012, sobre competencia judicial, el reconocimiento y la ejecución de resoluciones judiciales en materia civil y mercantil, que impedirá la continuidad del presente procedimiento.

El Reglamento 1215/2012 o Reglamento de Bruselas 1 bises aplicable desde el punto de vista material por tratarse de un litigio cuyo objeto trata sobre reclamación de cantidad causada por incumplimiento de contrato. La materia contractual se contempla dentro del ámbito de aplicación del Reglamento en su artículo 1. Desde el punto de vista espacial, el artículo 29 del Reglamento 1215/2012 es de aplicación cuando los litigios a los que se refiere la excepción de litispendencia son conocidos por Tribunales de Estados parte del Reglamento antecitado (STJCE de Luxemburgo de 14 de octubre de 2004, C-39/2002, Mærsk Olie & Gas A/S v. M. de. Haan y W. de Boer), como ocurre en las presentes actuaciones.

El artículo 29 del Reglamento indica que: "1. Sin perjuicio de lo dispuesto en el artículo 31, apartado 2, cuando se formulen demandas con el mismo objeto y la misma causa entre las mismas partes ante órganos jurisdiccionales de Estados miembros distintos, el órgano jurisdiccional ante el que se formule la segunda demanda suspenderá de oficio el procedimiento en tanto no se declare competente el órgano jurisdiccional ante el que se interpuso la primera. 2. En los casos contemplados en el apartado 1, a instancia de un órgano jurisdiccional al que se haya sometido el litigio, cualquier otro órgano jurisdiccional al que se haya sometido el litigio informará sin demora al primero de la fecha en que se interpuso la demanda de conformidad con lo dispuesto en el artículo 32. 3. Cuando el órgano jurisdiccional ante el que se interpuso la primera demanda se declare competente, el órgano jurisdiccional ante el que se interpuso la segunda se abstendrá en favor de aquel".

Concurren todos los requisitos para apreciar la litispendencia internacional contemplada en el artículo 29 del Reglamento 1215/2012 por tratarse de demandas entre las mismas partes, con el mismo objeto y la misma causa. Estos conceptos deben ser definidos con arreglo a una interpretación autónoma, propia del Reglamento, según dictamina la jurisprudencia del Tribunal de Justicia de las Comunidades Europeas: entre otras, STJCE de 8 de diciembre de 1987, rec. 144/1986, Gubisch, STJCE de 6 de diciembre de 1994, C-406/1992, Tatry, STJCE de 20 de enero de 1994, C-129/1992, Owens, STJCE de 8 de mayo de 2003, C-111/2001, Gantner, STJCE de 14 de octubre de 2004, C-39/2002, Mærsk. Esta jurisprudencia, aunque referida al Convenio de Bruselas, es aplicable al caso de especie, pues el artículo 24 del Convenio de Bruselas de 27 de septiembre de 1968 es equivalente al artículo 29 del Reglamento 1215/2012 antes citado. La identidad de partes, objeto y causa debe recibir una interpretación amplia, por razones de economía procesal, al objeto de eliminar procesos paralelos en diversos países de la Unión Europea.

Según consta en la prueba documental que se acompaña, las partes personadas son las mismas en ambos procedimientos. En cuanto a la causa, ambos procesos han de considerarse idénticos pues iguales hechos y fundamentos jurídicos han sido invocados. La interpretación autónoma y amplia del objeto conduce a la identidad de los dos procesos puesto que la finalidad de las demandas es la misma; en aplicación de la teoría del núcleo común mantenida por la Jurisprudencia del TJCE, tiene el mismo objeto una demanda dirigida a declarar la existencia de responsabilidad que otra dirigida a declarar la ausencia de la misma.

Quedando acreditada la concurrencia material de los presupuestos legales establecidos por el artículo 29 del Reglamento de Bruselas 1 bis, debe acogerse la excepción procesal de litispendencia puesta de relieve por esta representación y, en su virtud, proceder al sobreseimiento del presente proceso dictándose Auto al efecto, tras los trámites que procedan, en el que se acuerde la inhibición del Juez de esta instancia a favor de la Corte de Londres [...], por ser quien primero ha tenido conocimiento de la demanda planteada por la actora y por haberse declarado competente.

Nota: Si en el iter procesal, el Tribunal extranjero todavía no se ha declarado competente para conocer del asunto, la parte interesará del juez español ante el que se interpuso la segunda demanda, la suspensión del procedimiento. Una vez acreditada la competencia del Tribunal extranjero, al juez español se le solicitará que, previo alzamiento de la suspensión, dicte auto de sobreseimiento e inhibición.

Segundo.— (Fundamentos de fondo [FUNDAMENTOS])

Tercero.— En cuanto a las costas, por aplicación del artículo 394 de la LEC corresponde la imposición de las mismas al demandante.

Por todo lo expuesto,

SUPLICO AL TRIBUNAL, que teniendo por presentada en forma y tiempo esta contestación a la demanda, la una a los autos de su razón; y tras los trámites que procedan, por apreciación de la excepción de litispendencia internacional en favor del demandado, dicte auto de sobreseimiento de las presentes actuaciones inhibiéndose a favor de la Corte de Londres [...], con expresa condena en costas al demandante.

OTROSÍ DIGO, que subsidiariamente al anterior suplico, tenga por contestada la demanda con oposición a lo solicitado por el demandante, y tras los trámites que procedan, dicte finalmente sentencia por la cual se acuerde la desestimación de las acciones emprendidas por la parte actora, con expresa condena en costas.

SUPLICO AL TRIBUNAL, que acuerde conforme se interesa en el precedente otrosí.

Es Justicia que pido en [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma y número del Letrado

Firma del Procurador

========================================================================
