---
name: solicitud-nulidad-actuaciones-sentencia-falta-citacion-civ-1320
description: "Solicitud de nulidad de actuaciones de la sentencia por falta de citación a juicio. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud de nulidad de actuaciones de la sentencia por falta de citación a juicio

> Formulario **CIV-1320** del plugin **Recursos civiles: reposición, apelación, casación y queja** (`formularios-recursos-civiles`) · Civil › Recursos · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud de nulidad de actuaciones de la sentencia por falta de citación a juicio» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud de nulidad de actuaciones de la sentencia por falta de citación a juicio” para mi caso». También puedes invocarla directamente con `/formularios-recursos-civiles:solicitud-nulidad-actuaciones-sentencia-falta-citacion-civ-1320`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-recursos-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Recursos civiles: reposición, apelación, casación y queja) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (12 veces)
- [ ] PROVINCIA (3 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NOMBRE DEL REPRESENTADO/A (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] FECHAS
- [ ] IMPORTE
- [ ] Nº DE PROCEDIMIENTO
- [ ] NÚMERO
- [ ] ÓRGANO JUDICIAL

## Normas que cita el formulario

- art. 241 LOPJ
- art. 228 LEC
- art. 238.3 LOPJ
- art. 164 LEC
- art. 241.2 LOPJ
- art. 228.2 LEC

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

- Junto a «…CIAL] Proceso [Nº DE PROCEDIMIENTO] A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

Tribunal [ÓRGANO JUDICIAL]

Proceso [Nº DE PROCEDIMIENTO]

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA

D. [NOMBRE Y APELLIDOS] Procurador de los Tribunales y de [NOMBRE DEL REPRESENTADO/A], actuando en nombre y representación de [NOMBRE DEL REPRESENTADO/A], parte demandada en los autos de juicio verbal seguidos ante ese Tribunal con el número [NÚMERO], según consta en copia electrónica del poder notarial de representación informática (o digitalizada) otorgada al efecto que acompaño y cuya devolución solicito previo testimonio en autos, ante el Tribunal comparezco y como mejor proceda en derecho DIGO:

Que habiendo tenido conocimiento esta parte de la sentencia dictada en los autos arriba expresados al haber sido notificada del auto despachando ejecución por diligencia de fecha [FECHA], por medio del presente escrito y al amparo de lo dispuesto en el art. 241 de la LOPJ y art. 228 de la LEC promuevo la NULIDAD DE ACTUACIONES en el mencionado proceso en base a los siguientes hechos y fundamentos:

PRIMERO.- (Antecedentes y cumplimiento de requisitos) El presente proceso se inició por demanda presentada por D. [NOMBRE Y APELLIDOS] contra mi representada, habiéndose celebrado juicio sin el conocimiento de mi representado y dictándose sentencia de fecha [FECHA] que condenaba al demandado a indemnizar al actor en la cantidad de [IMPORTE] euros.

Tanto la citación para juicio como la sentencia se comunicaron a esta parte mediante edictos publicados en el BOP de [PROVINCIA] en fechas [FECHAS] y [FECHA] respectivamente.

Esta parte ignoraba todas estas actuaciones procesales hasta que el pasado día [FECHA] tuvo conocimiento de la ejecución seguida al entenderse con su representante la diligencia de embargo consecuente con la ejecución de la sentencia condenatoria.

Por tanto, se cumplen los requisitos del art. 241 de la LOPJ al deducirse la petición dentro del plazo de veinte días desde que se conoció la sentencia y no haber transcurrido cinco años desde que la misma fue dictada, al estar legitimado mi representada al ser parte demandada en el proceso y resultar condenado en la sentencia y al ser firme la sentencia no siendo susceptible de repararse el defecto por otro recurso.

SEGUNDO.- (Motivos de nulidad y hechos en que se basa) La nulidad que se solicita lo es al amparo del art. 24 de la CE y art. 238.3 de la LOPJ, así como de la reiterada jurisprudencia que interpreta el remedio de la comunicación edictal como último instrumento, lo que determina que el proceso se siguiera con infracción del principio de contradicción, con evidente indefensión para esta parte.

La infracción resulta del iter procedimental seguido y que en síntesis es el siguiente:

a) la parte demandante solicitó en su demanda que se citara al demandado en el domicilio sito en [LOCALIDAD], practicándose la citación por medio de correo certificado con acuse de recibo a la dirección señalada en la demanda.

b) en fecha [FECHA] se devuelve sin cumplimentar la citación por el servicio de correos, por lo que se dicta providencia de fecha [FECHA] en la que se requiere al actor para que designe nuevo domicilio en plazo de diez días.

c) el demandante presenta escrito en fecha [FECHA] en el que manifiesta desconocer otro domicilio, ante lo cual el Tribunal acuerda la citación por edictos sin hacer ninguna otra averiguación por providencia de fecha [FECHA] y publicándose los edictos en el BOP de [PROVINCIA] de fecha

d) El día [FECHA] se celebra el acto de juicio, dictándose sentencia de fecha [FECHA] que es notificada al demandado por medios de edictos publicados en el BOP de [PROVINCIA] de fecha

e) Por auto de fecha [FECHA] se despacha ejecución de la sentencia dictada en este proceso, practicándose diligencia de embargo en fecha [FECHA] en el nuevo domicilio que facilitó el demandante en su escrito solicitando la ejecución, siendo que en este momento es la primera vez que el demandado tiene conocimiento de la existencia del proceso.

TERCERO.- (Fundamentos de la nulidad postulada) La nulidad de actuaciones que se postula resulta palmaria del relato del curso de proceso, por cuanto se acudió al postrer remedio de la citación y notificación edictal, sin haber desplegado una actividad razonable para venir en conocimiento del domicilio del demandado, tal como se exige en el art. 164 de la LEC y en la interpretación que realiza la jurisprudencia del TC y del Tribunal Supremo, de forma reiterada, como así lo recogen las SSTC 18/1995, de 3 de julio; 155/1995, de 24 de octubre; STS 12 de junio de 2003, rec. 3205/1997.

De acuerdo a la citada doctrina jurisprudencial, el intento fallido de notificación no justifica sin más el acudir a la citación edictal, como en este caso se ha producido, siendo que además ni tan siquiera se intentó la entrega personal en el domicilio inicialmente designado.

Lo cierto es que el domicilio designado era el anterior de mi representada, habiéndose trasladado a las dependencias de su actual domicilio sito en [LOCALIDAD], lo cual se hubiera constatado fácilmente de haberse intentado la entrega personal, pues estaba debidamente indicado mediante carteles que lo publicitaban en el anterior domicilio. Pero es que, además, el cambio de domicilio fue debidamente inscrito en el Registro Mercantil, tal como se constata de la nota simple que aporto como documento número 1, por lo que de haberse practicado esta diligencia de carácter elemental fácilmente se hubiera podido practicar la comunicación personal.

La propia parte demandante ha podido conocer posteriormente el domicilio de mi representada, puesto que lo facilitó al Tribunal posteriormente al instar la ejecución de la sentencia. Sin entrar en las intenciones de la parte demandante, lo cierto es que parece lógico deducir que no desplegó la mínima actividad diligente en el momento de facilitar el domicilio del demandado.

Por tanto, existe un defecto en la comunicación que impidió a mi representada el ejercicio de su derecho de defensa, al acudirse a la citación edictal, lo que originó que el juicio se desarrollara a espaldas del demandado, ocasionando una evidente indefensión, y debe dar lugar a la nulidad de las actuaciones desde el momento anterior a la citación al juicio, conforme a los arts. 225 y ss. de la LEC, para que mi representada pueda defenderse en el mismo.

Por lo expuesto es de justicia y,

SUPLICO AL TRIBUNAL que tenga por presentado este escrito y documento que se acompaña, por promovido incidente de nulidad de actuaciones practicadas en este proceso, y, previos los trámites legales, dicte resolución por la que declare la nulidad de lo actuado reponiendo las actuaciones al momento inmediatamente anterior a la citación para juicio.

(caso de solicitarse la suspensión de la ejecución) OTROSÍ DIGO que al amparo de lo dispuesto en el art. 241.2 de la LOPJ y art. 228.2 de la LEC solicito que se acuerde la suspensión del procedimiento de apremio iniciado contra mi representada, puesto que existe una sólida apariencia de buen derecho y se originaría un perjuicio irreparable de seguir adelante con la subasta que ya se ha señalado, siendo que es el único inmueble que posee mi representada donde desarrolla su actividad y la suspensión no incide sobre la posibilidad de continuar la ejecución si la petición de mi mandante fuera desestimada, al haberse asegurado la traba mediante la anotación registral de la misma.

SUPLICO AL TRIBUNAL que acuerde de conformidad.

En L. y F.

(Firma Procurador y Abogado)

========================================================================
