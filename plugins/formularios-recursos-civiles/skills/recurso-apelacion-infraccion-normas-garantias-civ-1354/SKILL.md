---
name: recurso-apelacion-infraccion-normas-garantias-civ-1354
description: "Recurso de apelación por infracción de normas o garantías procesales. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Recurso de apelación por infracción de normas o garantías procesales

> Formulario **CIV-1354** del plugin **Recursos civiles: reposición, apelación, casación y queja** (`formularios-recursos-civiles`) · Civil › Recursos · normativa revisada el 24-11-2026.

## Qué es

Escrito de interposición de recurso de apelación contra sentencia civil fundado en la infracción de normas o garantías procesales (art. 459 LEC), con vulneración del derecho a un proceso con todas las garantías (art. 24 CE). El modelo desarrolla, como ejemplo, la celebración del juicio pese a haberse solicitado su suspensión por enfermedad grave del abogado, y pide la nulidad de actuaciones con retroacción. En el encabezamiento de las alegaciones deben constar los pronunciamientos que se impugnan.

Es un modelo de tipo **recursos**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Recurso de apelación por infracción de normas o garantías procesales» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Recurso de apelación por infracción de normas o garantías procesales” para mi caso». También puedes invocarla directamente con `/formularios-recursos-civiles:recurso-apelacion-infraccion-normas-garantias-civ-1354`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-recursos-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Recursos civiles: reposición, apelación, casación y queja) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (12 veces)
- [ ] Nº (8 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] Nº DE PROCEDIMIENTO (2 veces)
- [ ] SEDE (2 veces)
- [ ] AÑO
- [ ] CLASE DE PROCESO
- [ ] DÍA
- [ ] EXPONER OTROS MOTIVOS.
- [ ] HORA
- [ ] IMPORTE
- [ ] MES
- [ ] NIG
- [ ] NOMBRE Y APELLIDOS DEL APELANTE
- [ ] NOMBRE Y APELLIDOS DEL LETRADO/A
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] PROVINCIA
- [ ] RAZONAR SOBRE EL EFECTO DE INDEFENSIÓN.
- [ ] RAZONAR SOBRE LA VULNERACIÓN PROCESAL.
- [ ] RAZONAR SOBRE LOS EFECTOS PRETENDIDOS.
- [ ] TRANSCRIPCIÓN DEL FALLO

## Normas que cita el formulario

- art. 455 LEC
- art. 458 LEC
- art. 448.2 LEC
- art. 215.5 LEC
- art. 459 LEC
- art. 183 LEC
- art. 452 LEC
- art. 135 LEC
- art. 231 LEC

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

A LA AUDIENCIA PROVINCIAL DE [PROVINCIA]

Don/Doña [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, actuando en representación de Don/Doña [NOMBRE Y APELLIDOS DEL APELANTE], según acredito mediante certificación de apoderamiento electrónico que acompaño, bajo la dirección letrada de Don/Doña [NOMBRE Y APELLIDOS DEL LETRADO/A], comparezco y como mejor proceda en Derecho, DIGO:

1) Que en fecha [FECHA] esta parte ha sido notificada de la Sentencia número [Nº], de fecha [FECHA], dictada por la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº], en autos de proceso [CLASE DE PROCESO] número [Nº DE PROCEDIMIENTO] (NIG [NIG]), de la que se acompaña copia.

[OPCIONAL — incluir en caso de aclaración o complemento] Frente a dicha sentencia se dedujo solicitud de complemento, siendo desestimada por auto de fecha [FECHA], notificado en fecha [FECHA].

2) Que entendiendo que dicha sentencia no es ajustada a derecho, dicho sea con los debidos respetos y en términos de defensa, por medio del presente escrito, al amparo de lo dispuesto en los arts. 455 y 458 de la LEC, interpongo contra la misma RECURSO DE APELACIÓN, impugnando todos sus pronunciamientos, en base a los siguientes presupuestos de admisibilidad y alegaciones:

I. ADMISIBILIDAD DEL RECURSO

PRIMERO.- El presente recurso se deduce contra la citada sentencia dictada por la Sección Civil del Tribunal de Instancia número [Nº] en fecha [FECHA], cuyo fallo es del tenor literal siguiente: [TRANSCRIPCIÓN DEL FALLO].

SEGUNDO.- La sentencia es recurrible en apelación, según lo dispuesto en el art. 455 de la LEC.

TERCERO.- El presente recurso se interpone ante el tribunal competente para conocer del mismo, dentro del plazo de veinte días establecido en el artículo 458 de la LEC, computados conforme al artículo 448.2 de la LEC [OPCIONAL — si procede: en relación con el artículo 215.5 LEC], habiéndose constituido el depósito para recurrir tal como se expresa en el otrosí de este escrito.

CUARTO.- Por medio del presente recurso se impugnan todos los pronunciamientos de la sentencia apelada, tanto el de condena a mi representado/a, como el de intereses y costas.

II. ALEGACIONES

De conformidad con lo dispuesto en el art. 458 de la LEC, fundo el recurso de apelación en las siguientes

ALEGACIONES:

PRIMERA.- Al amparo del art. 459 de la LEC, por infracción de las garantías procesales del proceso civil con vulneración de lo dispuesto en el art. 24 de la CE en cuanto al derecho fundamental a un proceso con todas las garantías.

Esta parte solicitó la suspensión del juicio celebrado en fecha [FECHA] por la imposibilidad de asistencia de su abogado, al estar ingresado en el hospital de [LOCALIDAD] aquejado de una dolencia grave, lo que fue denegado por el Juez a quo, privándose de esta forma de la posibilidad de defenderse en el juicio. [EXPRESAR LA DENUNCIA DE LA INFRACCIÓN EN LA INSTANCIA, CON CITA DE LOS FOLIOS.] Esta parte, al ser notificada de la denegación de la suspensión, interpuso recurso de reposición contra la mencionada providencia en fecha [FECHA], tal como consta en folio [Nº], el cual fue denegado por auto de fecha [FECHA] al entender que se presentaba extemporáneamente. En fecha [FECHA] esta parte presentó escrito de protesta, reservándose el derecho a reproducir la cuestión en segunda instancia, tal como consta en folio [Nº].

[RAZONAR SOBRE LA VULNERACIÓN PROCESAL.] La resolución judicial infringe lo dispuesto en el art. 183 de la LEC, pues la solicitud se ajustaba perfectamente a los requisitos legales y estaba plenamente justificada, según se infiere de la documentación acompañada obrante en folios [Nº] del proceso, de donde se infiere claramente la imposibilidad del abogado de esta parte de asistir a la vista. Por otra parte, la resolución del recurso de reposición infringe lo que dispone el art. 452 de la LEC, pues se presentó en plazo, ya que la notificación se produjo el día [FECHA], según obra en folio [Nº], y el recurso se presenta en fecha [FECHA] a las [HORA] horas, esto es, dentro del quinto día según lo dispuesto en el art. 135 de la LEC.

[RAZONAR SOBRE EL EFECTO DE INDEFENSIÓN.] La actuación judicial ha supuesto una vulneración del derecho de defensa de esta parte, pues mi representado/a se ha visto indefenso/a al no poder intervenir en el juicio y no poder practicar la prueba admitida, impidiéndole asimismo formular conclusiones. En este sentido, el Tribunal Constitucional ha precisado, entre otras, en las sentencias 130/1986 y 237/1988, que, cuando alguna de las partes en un litigio solicita razonadamente la suspensión de la vista o del juicio, el Tribunal competente no puede ignorar su petición y llevar a cabo la actuación judicial sin resolver motivadamente acerca de su solicitud, si con ello perjudica sus derechos de defensa. La razón estriba en que en todo proceso judicial debe respetarse el derecho de defensa contradictoria de las partes contendientes mediante la oportunidad de alegar y probar procesalmente sus derechos o intereses, sin que pueda justificarse la resolución judicial inaudita parte más que en el caso de incomparecencia por voluntad expresa o tácita, o por negligencia imputable a las partes; por lo que no es válido celebrar sin más la vista o la actuación oral de que se trate ignorando la petición de suspensión, siendo que la enfermedad del Abogado es considerada causa justa de suspensión, habiendo afirmado el Tribunal Supremo en sentencia de 28 de enero de 2008, con cita de las SSTC 101/2001, de 23 de abril, y 143/2001, de 18 de junio, que «la celebración de la vista sin la participación de las partes implica la omisión de una formalidad esencial que determina la indefensión, salvo que esta sea imputable al mismo justiciable, como es la privación o limitación de cualesquiera medios legales de defensa de su propia posición dentro del proceso, lo que ciertamente ocurre cuando falta la plena posibilidad de contradecir».

[RAZONAR SOBRE LOS EFECTOS PRETENDIDOS.] De acuerdo con la grave infracción denunciada, entendemos que procede decretar la nulidad de todo lo actuado a partir de la celebración del juicio, debiendo retrotraerse las actuaciones a dicho momento procesal.

[OPCIONAL — incluir si ha lugar] SEGUNDA.- [EXPONER OTROS MOTIVOS.]

Por lo expuesto,

SUPLICO A LA AUDIENCIA PROVINCIAL que tenga por interpuesto recurso de apelación contra la sentencia de fecha [FECHA], dictada por la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº], en el proceso número [Nº DE PROCEDIMIENTO], con justificante de traslado a la otra parte que acompaño, y, previos los trámites legales, dicte sentencia por la que estime el recurso interpuesto, declarando la nulidad de todo lo actuado a partir de la celebración del juicio y acordando la retroacción de las actuaciones a dicho momento procesal [OPCIONAL — completar la pretensión].

OTROSÍ PRIMERO DIGO que, de conformidad con lo dispuesto en los apartados 3.b) y 6 de la disposición adicional decimoquinta de la LOPJ, acompaño a este escrito resguardo de consignación en la cuenta de Depósitos y Consignaciones abierta a nombre del Tribunal del depósito exigido para interponer el recurso, por importe de [IMPORTE] euros.

Por lo que SUPLICO A LA SALA que tenga por constituido el depósito, dejando interesada desde este momento su devolución para el caso de estimación total o parcial del recurso.

OTROSÍ SEGUNDO DIGO que acompaño los siguientes documentos referenciados mediante índice electrónico:

Documento número 1: certificación de apoderamiento electrónico.

Documento número 2: copia de la sentencia impugnada, que contiene firma electrónica que la identifica (o código seguro de verificación).

Documento número 3: resguardo de depósito para recurrir.

SUPLICO A LA SALA que tenga por aportados los citados documentos.

OTROSÍ TERCERO DIGO que esta parte manifiesta su voluntad de cumplir los requisitos exigidos por la LEC para la interposición del recurso de apelación, por lo que solicita que le sea concedido el oportuno trámite de subsanación, en el caso de haber cometido algún defecto, de conformidad con lo dispuesto en el art. 231 de la LEC.

SUPLICO A LA SALA que tenga por hechas las manifestaciones y acuerde de conformidad.

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma de Procurador/a y Abogado/a.
