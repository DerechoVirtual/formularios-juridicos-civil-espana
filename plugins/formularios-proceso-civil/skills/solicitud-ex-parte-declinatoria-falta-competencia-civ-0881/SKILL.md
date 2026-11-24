---
name: solicitud-ex-parte-declinatoria-falta-competencia-civ-0881
description: "Solicitud ex parte de declinatoria por falta de competencia internacional (Bruselas I refundido). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud ex parte de declinatoria por falta de competencia internacional (Bruselas I refundido)

> Formulario **CIV-0881** del plugin **Proceso civil: demandas, contestaciones, prueba y vista** (`formularios-proceso-civil`) · Civil › Escritos procesales (demanda, contestación, prueba, vista) · normativa revisada el 24-11-2026.

## Qué es

ESCRITO DE SOLICITUD (EX PARTE) DE DECLINATORIA DE JURISDICCIÓN POR FALTA DE COMPETENCIA JUDICIAL INTERNACIONAL DE LOS TRIBUNALES ESPAÑOLES (RB1 -refundición-)

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud ex parte de declinatoria por falta de competencia internacional (Bruselas I refundido)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud ex parte de declinatoria por falta de competencia internacional (Bruselas I refundido)” para mi caso». También puedes invocarla directamente con `/formularios-proceso-civil:solicitud-ex-parte-declinatoria-falta-competencia-civ-0881`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-proceso-civil:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Proceso civil: demandas, contestaciones, prueba y vista) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] Nº DE PROCEDIMIENTO (3 veces)
- [ ] FECHA (2 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] SEDE (2 veces)
- [ ] ÓRGANO JUDICIAL (2 veces)
- [ ] AÑO
- [ ] CALLE
- [ ] COLEGIO
- [ ] DENOMINACIÓN SOCIAL
- [ ] DOMICILIO
- [ ] DÍA
- [ ] LUGAR
- [ ] MES
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] Nº DE COLEGIADO
- [ ] Nº DE COLEGIADO/A
- [ ] NÚMERO
- [ ] PAÍS
- [ ] TIPO Y Nº DE PROCEDIMIENTO

## Normas que cita el formulario

- art. 39 LEC
- art. 64 LEC
- art. 23.1 LEC
- art. 24.1 LEC
- art. 63.1 LEC
- art. 64.1 LEC
- art. 63.2 LEC
- art. 65 LEC
- art. 36 LEC

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

- Junto a «…rocedimiento n.º [NÚMERO] A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

Tribunal de Instancia de [SEDE]

Autos de Procedimiento n.º [NÚMERO]

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./D.ª [NOMBRE Y APELLIDOS] Procurador/a de los Tribunales, en nombre y representación de D./D.ª [NOMBRE Y APELLIDOS], en virtud de apoderamiento apud acta/poder notarial según tengo acreditado en Autos de juicio [Nº DE PROCEDIMIENTO] seguidos ante el Tribunal [ÓRGANO JUDICIAL] y asistido de la intervención del/de la Letrado/a D./D.ª [NOMBRE Y APELLIDOS], Abogado/a del Ilustre Colegio de [COLEGIO], con número de colegiado [Nº DE COLEGIADO/A];

Comparezco ante el Tribunal [ÓRGANO JUDICIAL] en sede de Autos [TIPO Y Nº DE PROCEDIMIENTO] a los únicos efectos del presente escrito, y como mejor proceda en Derecho,

DIGO:

Que por el presente escrito, y al amparo de los artículos 39 y 63 LEC, interpongo EXCEPCIÓN DE DECLINATORIA DE JURISDICCIÓN, en plazo legal y con los efectos de suspensión del presente procedimiento, hasta resolución del presente incidente, conforme dispone el artículo 64 LEC: «La declinatoria se habrá de proponer dentro de los diez primeros días del plazo para contestar a la demanda, y surtirá el efecto de suspender, hasta que sea resuelta, el plazo para contestar y el curso del procedimiento principal».

Esta excepción de declinatoria de jurisdicción es procedente con base a los siguientes

HECHOS

Primero.— Con fecha de [FECHA], mi representado ha sido notificado de la demanda del presente procedimiento civil, instada por la sociedad mercantil [DENOMINACIÓN SOCIAL] con sede social en España (c/ [CALLE]). Según manifiesta la demandante, la causa de la presente demanda obedece a la falta de pago de un contrato de compraventa internacional de mercaderías que fueron entregadas en [LOCALIDAD], en el domicilio de mi representado [NOMBRE DEL REPRESENTADO/A]. Por Auto de fecha [FECHA] fue admitida a trámite, en ausencia de foro de Competencia Judicial Internacional a favor de los Tribunales españoles de conformidad con la legislación vigente.

Segundo.— Como prueba de los hechos sobre los que se sustancia esta ausencia de competencia judicial, consta el propio contrato aportado por la demandante, en el que figura el domicilio de mi representado en Italia, la entrega de las mercancías en Italia, e igualmente es de hacer constar, que en el citado contrato no existe cláusula de sumisión expresa a Tribunales españoles o cualesquiera otros.

Además del contrato aportado por la demandante, esta representación aporta los siguientes documentos en prueba de los hechos que se manifiestan, [Nº DE DOCUMENTO]. Se aportan así los citados documentos, y con número de copias igual al de las partes presentes, para su debida unión a los Autos.

Sobre los hechos manifestados, así como de la excepción de jurisdicción que se ejerce por medio del presente escrito, son de aplicación los siguientes,

FUNDAMENTOS DE DERECHO

Primero. De orden procesal.

I. Legitimación, capacidad para ser parte y postulación procesal.

Debe tenerse por comparecida a la demandada en el presente procedimiento a los únicos efectos de oponer la excepción de declinatoria de jurisdicción, encontrándose debidamente postulada de conformidad con el artículo 23.1 LEC en la representación del/de la Procurador/a de los Tribunales, D./D.ª [NOMBRE Y APELLIDOS], legalmente habilitado/a, y bajo la preceptiva intervención letrada del/de la colegiado/a D./D.ª [NOMBRE Y APELLIDOS] todo ello conforme a los artículos 24.1 y 31 de la LEC.

La legitimación de la parte a la que represento, a los presentes efectos, deviene por ser la demandada en Autos de Juicio [...] y de conformidad con lo dispuesto en el artículo 63.1 LEC y, paralelamente, en el artículo 39 de la LEC.

La comparecencia ante el presente Tribunal, se realiza en plazo legal de diez días del artículo 64.1 LEC.

II. Competencia.

De conformidad con el artículo 63.2 LEC la competencia para resolver sobre la excepción de declinatoria de Jurisdicción corresponde al “mismo tribunal que esté conociendo del pleito y al que se considere carente de jurisdicción o de competencia ”. Siendo que en este Tribunal se siguen los autos de procedimiento [Nº DE PROCEDIMIENTO] contra mi representado, es por lo que resulta competente para resolver el presente incidente.

III. Tramitación.

Se denuncia la falta de jurisdicción del Tribunal que conoce de los presentes Autos, en legal plazo del artículo 64.1 LEC por lo que ha de admitirse la excepción de declinatoria internacional, debiendo seguirse los demás trámites legales regulados en el artículo 65 LEC.

IV. Efectos inmediatos.

Procede la inmediata suspensión de los Autos del procedimiento principal hasta la resolución de la presente excepción de declinatoria internacional, según dispone el artículo 64.1 LEC. Procede igualmente la suspensión del cómputo de los plazos producidos por la notificación de la demanda a mi representado.

Segundo. Sobre la falta de competencia judicial internacional.

La acción que ejerce la sociedad demandante contra mi representado deviene por supuesto incumplimiento y falta de ejecución del contrato de compraventa aportado a los presentes Autos. Consta en el mismo contrato que su objeto es la venta internacional de mercaderías, que han sido entregadas en [LOCALIDAD] según es de ver por el documento [Nº DE DOCUMENTO].

Dispone el artículo 36 de la LEC sobre la extensión y límites de la jurisdicción de los tribunales civiles españoles que ésta se determinará por lo dispuesto en “la Ley Orgánica del Poder Judicial y en los tratados y convenios internacionales en los que España sea parte". En su virtud, es de aplicación legal, en cuanto a la jurisdicción de los Tribunales españoles para conocer de la acción principal, el Reglamento (UE) nº 1215/2012 del Parlamento Europeo y del Consejo, de 12 de diciembre de 2012, relativo a la competencia judicial, el reconocimiento y la ejecución de resoluciones judiciales en materia civil y mercantil (Bruselas I -refundición-), siendo que consta que el domicilio del demandado que represento, está en [DOMICILIO]. Procede así su aplicación según indican los artículos 4, 5 y 6 del citado Reglamento.

La Competencia Judicial internacional para el conocimiento de la acción principal corresponde, en aplicación del foro general (artículos 4 a 6 del Reglamento), al Estado del domicilio del demandado, que es [PAÍS]. Tampoco existe competencia judicial internacional de los tribunales españoles en aplicación del foro especial por razón de la materia; en este sentido y según dispone el art. 7.1.a) del Reglamento 1215/2012, la competencia internacional para conocer de la acción de la demandante, corresponde a los Tribunales de [LOCALIDAD], por ser este Estado el lugar donde han sido entregadas las mercancías.

No concurre pacto de sumisión expresa en el contrato que permita sustentar la Competencia de los Tribunales españoles, según consta en la documental aportada a los presentes autos. Por otra parte, el ejercicio de la excepción de declinatoria de Jurisdicción por esta representación, no implica sumisión tácita a favor de los Tribunales españoles, por aplicación de lo dispuesto en el art. 26.1 del Reglamento 1215/2012 y la interpretación y aplicación del mismo por la Jurisprudencia del Tribunal de Justicia de la Unión Europea.

No existiendo foro legal alguno que permita sustentar la Jurisdicción de los Tribunales españoles para conocer de la acción principal de la demandante en los presentes Autos, procede, tras los trámites legales perceptivos, que este Tribunal dicte finalmente Auto por el cual acuerde su inhibición en la presente causa, por la falta de Competencia Judicial Internacional que denuncia esta representación, por medio del presente escrito.

Por todo ello, y en su virtud,

SUPLICO AL TRIBUNAL: Que teniendo por comparecida a la representación de D./D.ª [NOMBRE Y APELLIDOS] en los Autos de procedimiento [Nº DE PROCEDIMIENTO] y por medio del presente escrito, venga a admitir a trámite la presente Excepción de Declinatoria de Jurisdicción y tras los trámites que procedan, resuelva mediante Auto, su inhibición para conocer de la acción de la demandante, declinando así la competencia a favor de los Tribunales del Estado de [LOCALIDAD] por acoger los Fundamentos y alegaciones de esta representación.

OTROSÍ DIGO que, conforme indica el artículo 64.1 LEC, procede la inmediata suspensión de los Autos y del cómputo de sus plazos, sin que sea necesaria la prestación de caución alguna por esta representación.

II. SUPLICO AL TRIBUNAL acuerde conforme se interesa.

Es Justicia que pido en [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma y número del/ de la Letrado/a [Nº DE COLEGIADO] Firma del/de la Procurador/a

========================================================================
