---
name: encargo-arbitraje-institucion-arbitral-virtud-convenio-civ-1792
description: "Encargo de arbitraje a institución arbitral en virtud de convenio arbitral. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Encargo de arbitraje a institución arbitral en virtud de convenio arbitral

> Formulario **CIV-1792** del plugin **Mediación, MASC, arbitraje y jurisdicción voluntaria** (`formularios-mediacion-arbitraje-y-voluntaria`) · Civil › Jurisdicción voluntaria, MASC, mediación y arbitraje · normativa revisada el 24-11-2026.

## Qué es

Escrito de encargo de arbitraje al Tribunal de la Cámara de Comercio, Industria y Navegación solicitando se dicte laudo por virtud del cual determine la cantidad que le es debida a la parte que formula el encargo de arbitraje por presentar el intercambiador, objeto del contrato de suministro suscrito entre ambas partes, un defecto.

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Encargo de arbitraje a institución arbitral en virtud de convenio arbitral» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Encargo de arbitraje a institución arbitral en virtud de convenio arbitral” para mi caso». También puedes invocarla directamente con `/formularios-mediacion-arbitraje-y-voluntaria:encargo-arbitraje-institucion-arbitral-virtud-convenio-civ-1792`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-mediacion-arbitraje-y-voluntaria:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Mediación, MASC, arbitraje y jurisdicción voluntaria) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] DENOMINACIÓN SOCIAL (11 veces)
- [ ] NÚMERO (9 veces)
- [ ] LOCALIDAD (6 veces)
- [ ] FECHA (3 veces)
- [ ] CALLE (2 veces)
- [ ] AÑO
- [ ] BENEFICIARIO
- [ ] DOMICILIO
- [ ] IMPORTE
- [ ] LUGAR
- [ ] MARCA/MODELO
- [ ] NOMBRE O UBICACIÓN DE LA OBRA
- [ ] NOMBRE Y APELLIDOS
- [ ] ÓRGANO

## Normas que cita el formulario

- No cita artículos concretos; Claude localizará las normas aplicables con Jurisprudenciator si el documento las necesita.

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

Escrito de encargo de arbitraje al Tribunal de la Cámara de Comercio, Industria y Navegación solicitando se dicte laudo por virtud del cual determine la cantidad que le es debida a la parte que formula el encargo de arbitraje por presentar el intercambiador, objeto del contrato de suministro suscrito entre ambas partes, un defecto.


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

AL TRIBUNAL ARBITRAL DE LA CAMARA DE COMERCIO INDUSTRIA Y NAVEGACION DE [LOCALIDAD]

D./DÑA. [NOMBRE Y APELLIDOS], mayor de edad, industrial, provisto de D.N.I. nº [NÚMERO], con domicilio en [LOCALIDAD], calle [CALLE], nº [NÚMERO], en calidad de consejero delegado de [DENOMINACIÓN SOCIAL], representación que acredito con la copia auténtica de la escritura que eleva a público el nombramiento y poder societario, debidamente inscrito en el Registro Mercantil, que se adjunta como doc. nº [NÚMERO], ante el TRIBUNAL DE LA CÁMARA DE COMERCIO, INDUSTRIA Y NAVEGACIÓN DE [LOCALIDAD], comparezco y DIGO:

Que en la representación que ostento vengo a formular encargo de arbitraje institucional frente a la mercantil [DENOMINACIÓN SOCIAL], con C.I.F. B 48, domiciliada en [DOMICILIO], calle [CALLE], nº [NÚMERO], con base en los siguientes:

HECHOS

PRIMERO.- La actividad mercantil de nuestra representada tiene por objeto la ejecución de trabajados relacionados con la industria de calderería y calefacción. Desde el año [AÑO] mi representada mantiene relaciones comerciales con [DENOMINACIÓN SOCIAL], a fin de surtirnos específicamente de artículos de las casas italianas [DENOMINACIÓN SOCIAL] y [DENOMINACIÓN SOCIAL], para las obras civiles que conciertan nuestros servicios, como es ejemplo contrato de fecha [FECHA] que, señalado como doc. n.º [NÚMERO], se acompaña al presente escrito.

En el pacto undécimo de dicho contrato es del tenor siguiente:

«Para la solución de cualquier cuestión derivada de la interpretación o aplicación del presente contrato que pueda resultar controvertida, las partes se someten al arbitraje institucional del Tribunal Arbitral de la Cámara de Comercio, Industria y Navegación de [LOCALIDAD], encargándole la designación de árbitros y administración del arbitraje de acuerdo con su reglamento, y siendo el Arbitraje, de equidad o Derecho, como aparezca en dicho reglamento, y siempre exceptuadas de esta sumisión las cuestiones previamente decididas judicialmente, que no sean de libre disposición, o de carácter laboral».

SEGUNDO.- De conformidad a lo establecido en la cláusula cuarta del contrato, y como forma de pago por el suministro de un intercambiador de aire/agua marca [MARCA/MODELO] (destinado a la obra de [NOMBRE O UBICACIÓN DE LA OBRA]) mi mandante abonaba el 50% de su valor, mediante entrega de letra de cambio con vencimiento a sesenta días de la fecha de pedido, aceptado a favor de [BENEFICIARIO]., previamente al envío del producto, y quedando el otro 50% pendiente de pago en metálico cuando se recibiera éste.

TERCERO.- El intercambiador efectivamente fue recibido el [FECHA], pero de inmediato los técnicos que debían instalarlo en la obra referida, se apercibieron de la defectuosidad de la pieza, por lo que el departamento de pedidos se pudo en comunicación con [DENOMINACIÓN SOCIAL], a fin de enterar a esta empresa de que el producto iba a devolverse a su cargo, y que salvo el envío de otro en perfectas condiciones, ni se iba a proceder a entrega de metálico, y se reclamaba no ponerse en circulación el efecto de [IMPORTE] euros ( €) hasta que se repusiera el material adquirido.

que en un primer momento adujo la situación por la que atraviesa tal mercantil en los últimos tres meses, como obstativa de retornar la letra, luego ha pasado a negar la inhabilidad de la pieza, para terminar lanzando la responsabilidad al fabricante [ÓRGANO], de tal manera que mi patrocinada hubo de comprar otro intercambiador a la firma [DENOMINACIÓN SOCIAL], y el que fue devuelto, no ha sido recogido por la suministradora, estándose a la espera de tener que abonar la mitad del precio instrumentado en la letra a su inminente vencimiento.

A la demostración de estos datos, se adjunta la carta con la que se facilitó la letra de cambio, que la identifica, como doc. nº [NÚMERO], el albarán de entrega del intercambiador, doc. nº [NÚMERO], y el cargo de la compañía [DENOMINACIÓN SOCIAL] por el transporte de la misma pieza, ida y vuelta, a [LOCALIDAD], domicilio social de [LOCALIDAD], doc. nº [NÚMERO], así como factura de [DENOMINACIÓN SOCIAL], acreditativa de la compra de otro intercambiador semejante, que se acompaña como doc. nº [NÚMERO].

CUARTO.- En esta tesitura, mi mandante no tiene más remedio que presentar la solicitud o encargo a la institución arbitral prevista en el contrato, para que, según su reglamento, dicte laudo por virtud del cual determine la cantidad que le es debida a nuestro mandante, por atender a un efecto que no obedece a precio que no corresponde pagar, determinando al mismo tiempo que el artículo servido y rechazado no era aptos para su instalación, y ello atendiendo a los estándares de calidad de costumbre, es decir, por resuelto el contrato de compraventa o suministro.

Asimismo se considera que el importe de la letra, que injustamente financia a SUMINISTROS [DENOMINACIÓN SOCIAL], S.A., debe reintegrarse con la indemnización correlativa del interés devengado desde la entrega al tipo legal incrementado en dos puntos, que es el que devengaría por impago de la cambial, que no responde a un negocio causal válido.

En su virtud,

SOLICITO AL TRIBUNAL ARBITRAL

que, teniendo por presentado este escrito con los documentos que se acompañan, y por instado el encargo arbitral, se sirva admitirlo, y concediendo traslado a la reclamada [DENOMINACIÓN SOCIAL], designe árbitro y administre el encargo de arbitraje de conformidad con su Reglamento, de modo que se dicte en definitiva laudo, que obligue a estar y pasar a la reclamada por el abono a mi representada de la cantidad que se ha especificado.

Por ser de Justicia que pido en [LUGAR], a [FECHA].

Firma	Firma

========================================================================
