---
name: auto-despacha-provisionalmente-via-apremio-solicitada-civ-2085
description: "Auto que despacha provisionalmente la vía de apremio solicitada por el ejecutante. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Auto que despacha provisionalmente la vía de apremio solicitada por el ejecutante

> Formulario **CIV-2085** del plugin **Resoluciones judiciales civiles: autos, decretos y diligencias** (`formularios-resoluciones-judiciales-civiles`) · Civil › Resoluciones judiciales (autos, decretos, providencias, diligencias) · normativa revisada el 24-11-2026.

## Qué es

Auto despachando provisionalmente la vía de apremio a instancias de la parte ejecutante y procediéndose al embargo de bienes y derechos de la ejecutada.

Es un modelo de tipo **resoluciones judiciales (autos, decretos, providencias, diligencias)**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Auto que despacha provisionalmente la vía de apremio solicitada por el ejecutante» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Auto que despacha provisionalmente la vía de apremio solicitada por el ejecutante” para mi caso». También puedes invocarla directamente con `/formularios-resoluciones-judiciales-civiles:auto-despacha-provisionalmente-via-apremio-solicitada-civ-2085`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-resoluciones-judiciales-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Resoluciones judiciales civiles: autos, decretos y diligencias) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (12 veces)
- [ ] IMPORTE (11 veces)
- [ ] DENOMINACIÓN SOCIAL (6 veces)
- [ ] IMPORTE EN CIFRA (6 veces)
- [ ] FECHA (4 veces)
- [ ] NÚMERO (3 veces)
- [ ] AÑO (2 veces)
- [ ] IMPORTE EN LETRA (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] SECCIÓN

## Normas que cita el formulario

- art. 244 LEC
- art. 533.3 LEC
- art. 528.3 LEC
- art. 533 LEC
- art. 549.2 LEC
- art. 551 LEC
- art. 524.2 LEC
- art. 575.1 LEC
- art. 589.1 LEC
- art. 584 LEC
- art. 527.4 LEC

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

SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA N.º [NÚMERO]

PROCEDIMIENTO

Número de identificación informático:

PARTES:

AUTO

Ilmo. Sr./a Magistrado-Juez, D./Dña. [NOMBRE Y APELLIDOS]

En la Villa de [LOCALIDAD], a [FECHA]

ANTECEDENTES DE HECHO

I.- Requerida de la devolución a D./Dña. [NOMBRE Y APELLIDOS], representada por el/la Procurador/a.. Sr./a. [NOMBRE Y APELLIDOS], de la cantidad de [IMPORTE] xx [IMPORTE EN CIFRA] percibida en la ejecución provisional por [DENOMINACIÓN SOCIAL] SEGUROS Y REASEGUROS [DENOMINACIÓN SOCIAL], S.A., representada por el Procurador/a. Sr./a [NOMBRE Y APELLIDOS], no ha cumplimentado la entrega, transcurrido el plazo que se concedió.

II.- Se ha practicado la tasación de costas satisfechas por la ejecutada en la ejecución provisional, que se trasladó conforme al art. 244 LEC a las partes, sin que se haya formulado impugnación, como acredita diligencia de ordenación de [FECHA].

III.- Se ha dictado decreto de fecha [FECHA] que liquida en cantidad de [IMPORTE] zz [IMPORTE EN CIFRA] los daños y perjuicios causados a la ejecutada por la ejecución provisional, el cual no ha sido apelado.

IV.- El Procurador/a. D./Dña. [NOMBRE Y APELLIDOS], en representación de [NOMBRE DEL REPRESENTADO/A] SEGUROS Y REASEGUROS [DENOMINACIÓN SOCIAL], S.A., ha presentado escrito que solicitaba el apremio en la misma ejecución provisional contra D./Dña. [NOMBRE Y APELLIDOS], por la devolución de la cantidad de [IMPORTE] xx [IMPORTE EN CIFRA], el reintegro de [IMPORTE] yy [IMPORTE EN CIFRA] como costas tasadas, e indemnización de [IMPORTE] zz [IMPORTE EN CIFRA] por daños y perjuicios liquidados, solicitando el embargo genéricamente.

V.- La resolución que fundamenta la solicitud es la siguiente:

Clase y fecha: Sentencia de [FECHA]

Tribunal: Sección [SECCIÓN] de la Audiencia Provincial de [LOCALIDAD]

Proceso: Juicio Ordinario nº [NÚMERO]/[AÑO]; Rollo Ordinario n.º [NÚMERO]/[AÑO]

Recurso pendiente: Recurso de casación ante la Sala I Tribunal Supremo

Ejecutante: SEGUROS Y REASEGUROS [DENOMINACIÓN SOCIAL], S.A.

Ejecutado: D./Dña. [NOMBRE Y APELLIDOS]

Cantidad objeto de apremio: pp [IMPORTE] euros ()

RAZONAMIENTOS JURÍDICOS

PRIMERO.- Despachada ejecución provisional de la sentencia de instancia, se ha dictado sentencia totalmente revocatoria en recurso de apelación, y siendo de condena al pago de dinero, ha sido aquélla sobreseída, pero no siendo firme la revocación, quien ha obtenido el pronunciamiento revocatorio a su favor puede pretender por la vía de apremio la devolución de las cantidades percibidas por la ejecutante, el reintegro de las costas de la ejecución provisional satisfechas, así como el resarcimiento de daños y perjuicios que dicha ejecución le hubiere ocasionado (art. 533.3 LEC), cabiendo al obligado a devolver, reintegrar e indemnizar la oposición a actuaciones concretas del apremio, en términos del art. 528.3 LEC.

SEGUNDO.- De conformidad con el citado art. 533 LEC, este Tribunal es competente, por haber sustanciado la ejecución provisional, y la parte solicitante acompaña a su demanda todos los documentos recogidos en los arts. 549.2 y 550 LEC, y así mismo reúne los presupuestos procesales exigidos por el art. 551 LEC, en relación con el art. 524.2 LEC, y la medida de embargo solicitada es la adecuada en una reclamación dineraria, por lo que procede despachar la vía de apremio contra la hasta ahora ejecutante.

TERCERO.- En cuanto a los intereses y costas del procedimiento de apremio, lo reclamado no excede del límite establecido en el art. 575.1 LEC, como previsión, ya que no supera el 30 por ciento de lo que se solicita devolver o reintegrar, sin perjuicio de ulterior liquidación.

CUARTO.- Habiéndose desatendido el requerimiento de devolución, y no cumplido el reintegro de costas tasadas, y la indemnización liquidada en incidente de los arts. 712 y ss. LEC, procede decretar directamente el embargo de bienes de la ejecutada en cantidad suficiente para cubrir las cantidades reclamadas al mismo tiempo que requerirla para que manifieste relacionadamente bienes y derechos suficientes en la forma prevista en el art. 589.1 LEC.

En virtud de lo expuesto,

PARTE DISPOSITIVA

1.- Se despacha provisionalmente la vía de apremio a instancias de [DENOMINACIÓN SOCIAL] SEGUROS Y REASEGUROS [DENOMINACIÓN SOCIAL], S.A., representada por el/la Procurador/a. de los Tribunales D./Dña. [NOMBRE Y APELLIDOS], parte ejecutante, frente a D./Dña. [NOMBRE Y APELLIDOS], representada por el/la Procurador/a. de los Tribunales D./Dña. [NOMBRE Y APELLIDOS], parte ejecutada, por las siguientes cantidades: xx [IMPORTE] euros () por devolución de cantidades percibidas; yy [IMPORTE] euros () por reintegro de costas tasadas; zz [IMPORTE] euros () por indemnización de daños y perjuicios; y [IMPORTE EN LETRA] pp [IMPORTE] euros () en concepto de intereses por demora y costas, sin perjuicio de ulterior definitiva liquidación.

2.- Procédase al embargo de bienes y derechos de la ejecutada D./Dña. [NOMBRE Y APELLIDOS], en cantidad suficiente para cubrir las responsabilidades reclamadas, que ascienden al total de [IMPORTE EN LETRA] oo [IMPORTE] euros ([IMPORTE EN CIFRA] €).

3.- Expídase mandamiento al Agente Judicial [NOMBRE Y APELLIDOS] para que asistido de LAJ u Oficial habilitado, proceda al embargo de bienes del ejecutado en cuanto sean suficientes para cubrir las sumas antes expresadas, observándose en la traba las prevenciones de los arts. 584 a 592 LEC.

4.- Requiérase a la parte ejecutada para que en el plazo máximo de diez días, manifieste en este Tribunal o ante la comisión judicial en el momento del embargo, relación de bienes y derechos suficientes para cubrir la cantidad por la que se apremia, con expresión, en su caso, de cargas y gravámenes, así como, en el caso de inmuebles, si están ocupados, por qué personas y con qué título, con apercibimiento de las sanciones que pueden imponérsele, cuando menos por desobediencia grave, en el supuesto de que no presente la relación, incluya en ella bienes que no sean suyos, excluya los propios susceptibles de embargo, o no desvele las cargas y gravámenes que sobre ellos pesaren, así como la posibilidad de imponérsele multas periódicas si no respondiere debidamente al requerimiento.

Así lo acuerdo, mando y firmo:

Firma del Juez/a

Contra este auto no cabe recurso, sin perjuicio de que el deudor pueda oponerse a las actuaciones ejecutivas concretas del procedimiento de apremio por la causa del art. 528.3 LEC (art. 527.4 'in fine' LEC).

========================================================================
