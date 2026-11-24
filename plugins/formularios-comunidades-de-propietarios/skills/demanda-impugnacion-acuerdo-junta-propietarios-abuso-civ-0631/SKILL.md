---
name: demanda-impugnacion-acuerdo-junta-propietarios-abuso-civ-0631
description: "Demanda de impugnación de un acuerdo de la junta de propietarios por abuso de derecho (Cataluña). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de impugnación de un acuerdo de la junta de propietarios por abuso de derecho (Cataluña)

> Formulario **CIV-0631** del plugin **Comunidades de propietarios** (`formularios-comunidades-de-propietarios`) · Civil › Propiedad horizontal · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de impugnación de un acuerdo de la junta de propietarios por abuso de derecho (Cataluña)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de impugnación de un acuerdo de la junta de propietarios por abuso de derecho (Cataluña)” para mi caso». También puedes invocarla directamente con `/formularios-comunidades-de-propietarios:demanda-impugnacion-acuerdo-junta-propietarios-abuso-civ-0631`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-comunidades-de-propietarios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Comunidades de propietarios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (4 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] NÚMERO (4 veces)
- [ ] AÑO
- [ ] DIRECCIÓN
- [ ] DÍA
- [ ] LUGAR
- [ ] MES
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] NOMBRE Y APELLIDOS
- [ ] Nº
- [ ] Nº DE DOCUMENTO

## Normas que cita el formulario

- art. 52.1.8.º LEC
- art. 249.1.7.º LEC
- art. 553 CC
- art. 394 LEC
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

### Avisos de actualización (1) — se aplican en el texto, nunca se copian en el documento

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE Q.P.T.R.C.»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE Q.P.T.R.C.

D [NOMBRE Y APELLIDOS] Procurador de los Tribunales, actuando en representación de [NOMBRE DEL REPRESENTADO/A] según se acredita mediante apoderamiento apud-acta otorgado ante el Letrado de la Administración de Justicia de [LOCALIDAD] que acompaño (o mediante copia electrónica del poder notarial de representación informática [o digitalizada] que se acompaña y se solicita sea devuelta una vez testimoniada) por medio de la presente formulo demanda de juicio ordinario de impugnación del acuerdo adoptado en el apartado [Nº] de la Junta de Propietarios de fecha [FECHA], notificada a mi representado el día [FECHA], demanda que dirijo contra la Comunidad de Propietarios del edificio [DIRECCIÓN], con domicilio en [LOCALIDAD] en base a los siguientes

PRIMERO.- HECHOS

Mi mandante es titular de la vivienda sita en [LOCALIDAD] tal y como resulta de la escritura en virtud de la que la misma se adquirió y que se adjunta como documento n.º [NÚMERO] de esta demanda, vivienda integrada en la Comunidad de Propietarios demandada.

SEGUNDO.- El pasado [FECHA] se celebró la Junta de la antes mencionada Comunidad en la que el punto del orden del día número [NÚMERO] se adoptó el siguiente acuerdo

En la votación del acuerdo, mi mandante formuló voto en contra, reflejándose en el acta al efecto levantada esta circunstancia, no obstante lo que el acuerdo se aprobó. A tal efecto se adjunta como documento n.º [NÚMERO] copia del acta de tal Junta.

TERCERO.- El citado acuerdo constituye un manifiesto abuso de derecho por parte de los copropietarios que lo adoptaron, atendidas las circunstancias, puesto que el contenido del acuerdo de prohibir el acceso de perros al ascensor implica una gratuita privación del derecho de mi representado a poder acceder a su vivienda con su animal de compañía, a la vez que el hecho de que accediera el perro al ascensor no produce perjuicio alguno para los demás copropietarios, no constando ningún tipo de incidencia que justifique la adopción de este acuerdo.

La jurisprudencia viene reiterando que constituye abuso de derecho la adopción de acuerdos que sean gravemente perjudiciales para algún copropietario, aunque su derecho no esté protegido por alguna especial prerrogativa jurídica cuando, como en este caso, no existe ningún perjuicio ni beneficio propio, por lo que es indudable que el acuerdo únicamente obedece a la intención de producir un perjuicio a un tercero, en este caso mi representado.

FUNDAMENTOS DE DERECHO

Competencia

Corresponde a los Tribunales de [LOCALIDAD] al ser el lugar en el que se encuentra la finca (art. 52.1.8.º LEC).

Procedimento y cuantía

Es el juicio ordinario con fundamento en el artículo 249.1.7.º LEC al ser una demanda referente a una reclamación que un comunero formula frente a una comunidad de propietarios de un edificio en régimen de propiedad horizontal, siendo la cuantía indeterminada.

Legitimación

Le corresponde a esta parte la legitimación activa en su condición de propietario y al haber votado en contra del acuerdo impugnado, estando al corriente del pago de las cuotas, en tanto que la legitimación pasiva corresponde a la Comunidad de Propietarios demandada, conforme a lo que dispone el artículo 553-31, apartados 2 y 3, del CC de Cataluña.

Requisitos de tiempo

La presente acción se ejercita en el plazo establecido en el artículo 553-31, apartado 4, del CC de Cataluña.

Cumplimiento de los requisitos de procedibilidad

Entiende esta parte, como ya se pronunció la Audiencia Provincial de Zaragoza, en su auto nº 206/2025, de 6 de octubre, que no cabe exigir el cumplimiento del requisito del MASC en las demandas de impugnación de acuerdos de la junta de propietarios dado el carácter imperativo de las normas aplicables al caso.

Motivos de impugnación

La acción que se ejercita es la de impugnación de acuerdos de la Junta de una Comunidad de Propietarios constituida en régimen de propiedad horizontal por adoptarse un acuerdo que, dadas las circunstancias, implica un abuso de derecho, al amparo de lo que dispone el artículo 553-31, apartado 1.a), del CC de Cataluña.

En cuanto a la apreciación del abuso del derecho, las SSTS 10 de febrero de 1998, rec. 349/1994 y 30 de junio de 1998, rec. 1122/1994 expresan que el ejercicio de un derecho es abusivo cuando se produce en el ejercicio de un derecho pero produce un daño antisocial o inmoral en un interés de tercero, cuando la actuación del titular obedece al deseo de producir un perjuicio a un tercero sin obtener un beneficio propio.

En materia de costas el artículo 394 LEC señala que las de primera instancia se imponen a la parte que vea en primera instancia rechazadas sus pretensiones.

En base a lo anterior,

SUPLICO AL TRIBUNAL que tenga por presentada la presente demanda con los documentos a ella adjuntos y sus copias, en la representación que ostento, y se tenga por formulada demanda de acción de impugnación del acuerdo núm [NÚMERO] adoptado por la Junta de Propietarios de la Comunidad del edificio sito en celebrada el día [FECHA] y en su virtud se dicte sentencia por la que se declare nulo y sin ningún valor el acuerdo antes mencionado, todo ello con condena en costas a la Comunidad demandada.

OTROSÍ I DIGO.-Que estando la presente demanda sujeta al abono de la tasa por el ejercicio de la potestad jurisdiccional fijada por la Ley 10/2012, de 20 de noviembre, modificada por RDL 3/2013 y Ley 25/2015, de 28 julio, y desarrollada por Orden HAP/2662/2012, de 13 de diciembre, siendo mi representada personas jurídica no exenta de su pago, se acompaña a la presente demanda como documento nº [Nº DE DOCUMENTO] la correspondiente autoliquidación con el ejemplar para la Administración de Justicia debidamente validado y en el que consta el pago de la cantidad de 300 euros correspondiente a la cuota fija, sin que se incluya la cuota variable prevista en el artículo 7.2 de la Ley 10/2012 al haber sido declarado inconstitucional y nulo por la STC 140/2016, de 21 de julio.

En virtud de lo anterior,

SUPLICO AL TRIBUNAL: que tenga por hecha la anterior manifestación a los efectos pertinentes y por acompañado el documento justificativo del abono de la tasa

OTROSÍ II DIGO: Que estando la presente demanda sujeta al pago de la tasa por la prestación de servicios personales y materiales en el ámbito de la administración de la Administración de Justicia, regulada por Decreto Ley de Cataluña 1/2014, de 3 de junio, por el que se modifica el Texto refundido de la Ley de tasas y precios públicos de la Generalidad de Cataluña, aprobado por el Decreto legislativo 3/2008, de 25 de junio, y de conformidad a lo previsto en los arts. 3 y 4.1 de la Orden JUS/303/2014, de 13 de octubre, esta parte anuncia su intención de presentar la correspondiente autoliquidación e ingreso en el plazo de un mes, una vez hayan transcurrido 10 días naturales desde la fecha de la recuperación por parte del órgano judicial del escrito iniciador del procedimiento o del incidente, que previenen los citados preceptos.

En virtud de lo anterior,

SUPLICO AL TRIBUNAL: que tenga por hecha la anterior manifestación a los efectos pertinentes.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

El Abogado /El Procurador

========================================================================
