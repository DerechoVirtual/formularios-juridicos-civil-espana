---
name: solicitud-embargo-preventivo-bienes-presentada-tras-civ-1203
description: "Solicitud de embargo preventivo de bienes presentada tras la demanda principal. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud de embargo preventivo de bienes presentada tras la demanda principal

> Formulario **CIV-1203** del plugin **Medidas cautelares y diligencias preliminares** (`formularios-medidas-cautelares-civiles`) · Civil › Medidas cautelares y diligencias preliminares · normativa revisada el 24-11-2026.

## Qué es

Escrito por el que el demandante, una vez presentada la demanda principal y estando el proceso en curso, solicita el embargo preventivo de bienes del demandado porque éste pretende desprenderse de su patrimonio, de modo que la sentencia condenatoria al pago de una cantidad podría resultar ineficaz.

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud de embargo preventivo de bienes presentada tras la demanda principal» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud de embargo preventivo de bienes presentada tras la demanda principal” para mi caso». También puedes invocarla directamente con `/formularios-medidas-cautelares-civiles:solicitud-embargo-preventivo-bienes-presentada-tras-civ-1203`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-medidas-cautelares-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Medidas cautelares y diligencias preliminares) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS DEL DEMANDADO (5 veces)
- [ ] FECHA (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL DEMANDANTE (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR (2 veces)
- [ ] CLASE DE JUICIO
- [ ] CONCEPTO DE LA DEUDA
- [ ] EJEMPLO DE HECHOS A ADAPTAR AL CASO:
- [ ] MARCA, MODELO Y MATRÍCULA
- [ ] MEDIO O PORTAL INMOBILIARIO EN QUE SE PUBLICA EL ANUNCIO
- [ ] MEDIOS DE PRUEBA
- [ ] NOMBRE Y APELLIDOS DEL LETRADO
- [ ] Nº
- [ ] Nº DE COLEGIADO
- [ ] Nº DE PROCEDIMIENTO
- [ ] RELACIÓN DE DOCUMENTOS
- [ ] SEDE
- [ ] TELÉFONO

## Normas que cita el formulario

- art. 723.1 LEC
- art. 721 LEC
- art. 726 LEC
- art. 727.1.ª LEC
- art. 728.1 LEC
- art. 730.4 LEC
- art. 728 LEC
- art. 732.3 LEC
- art. 732.2 LEC

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR], Procurador de los Tribunales, en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDANTE], cuya representación tengo debidamente acreditada en los autos de juicio [CLASE DE JUICIO] n.º [Nº DE PROCEDIMIENTO] contra el demandado D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDADO], ante el Tribunal comparezco y, como mejor proceda en Derecho,

DIGO:

Que mediante el presente escrito formulo solicitud de embargo preventivo de bienes del demandado D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDADO], cuyas circunstancias personales constan en autos.

La pretensión de medida cautelar consistente en el embargo preventivo de bienes del demandado se basa en los siguientes

HECHOS

PRIMERO

A través de la demanda rectora de la presente litis, mi patrocinado D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDANTE] ejercita acción personal de condena pecuniaria frente a D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDADO], en reclamación de la cantidad de [IMPORTE] euros, importe a que ascendió [CONCEPTO DE LA DEUDA].

La realidad y subsistencia de la expresada deuda se acredita con los documentos que se acompañaron a la demanda y que no fueron oportunamente impugnados de adverso.

SEGUNDO

Después de presentada la demanda origen de este procedimiento, esta parte ha venido en conocimiento de que el demandado pretende desprenderse de los bienes que constituyen su patrimonio, con lo cual se sustraerían los mismos a la posible garantía de satisfacción del crédito que en este procedimiento se reclama contra el mismo.

[EJEMPLO DE HECHOS A ADAPTAR AL CASO:] A través de averiguaciones particulares y de manifestaciones recogidas por mi mandante en la portería del inmueble donde vive el demandado, esta parte ha podido enterarse de la puesta en venta de la casa que habita, que es de su propiedad. Esto se corrobora con el cartel de «Se vende piso. Razón tfno. [TELÉFONO]» que figura en el portal, y que se corresponde con el del demandado, tal como se ha podido verificar al llamar a dicho número.

Asimismo, figura un anuncio inequívoco en [MEDIO O PORTAL INMOBILIARIO EN QUE SE PUBLICA EL ANUNCIO], que aportamos con el presente escrito, en el que se dan los datos de ubicación de la vivienda en venta.

Igualmente, a través de averiguaciones particulares, esta parte ha podido enterarse de que hace escasas fechas el demandado ha procedido a vender el vehículo [MARCA, MODELO Y MATRÍCULA] de su propiedad, como se acredita con el certificado expedido por la Jefatura de Tráfico que acompañamos.

Estas circunstancias son, a juicio de esta parte, suficientemente reveladoras de una modificación sustancial de las circunstancias existentes al tiempo de iniciarse el proceso y que infunden sobrados motivos para creer que, de no adoptarse una pronta tutela precautoria, podrá ser ineficaz la sentencia estimatoria que se postula y espera obtener.

Hacemos constar que esta parte no conoce otros bienes con los que el demandado pueda hacer frente a la condena dineraria que en este pleito se solicita.

Para acreditar los extremos anteriores se acompañan los siguientes documentos: [RELACIÓN DE DOCUMENTOS] (en defecto de justificación documental, el peticionario podrá ofrecerla por otros medios).

[En general, deberán consignarse los hechos específicos aplicables al supuesto concreto, haciendo especial énfasis en que, de no adoptarse la medida cautelar —en este caso, embargo preventivo—, podrían producirse durante la pendencia del proceso principal situaciones que impidan o dificulten la efectividad de la tutela judicial pretendida, adjuntando los datos, argumentos y justificaciones documentales que conduzcan a fundar por parte del tribunal un juicio favorable al fundamento de su pretensión.]

FUNDAMENTOS DE DERECHO

I.- El artículo 723.1 LEC atribuye competencia para conocer de las solicitudes sobre medidas cautelares al Tribunal que esté conociendo del proceso principal.

II.- El artículo 721 LEC, en cuanto dispone que se podrá solicitar la adopción de las medidas cautelares que se consideren necesarias para asegurar la efectividad de la tutela judicial que pudiera otorgarse en la sentencia estimatoria que se dictase.

El artículo 726 LEC, en cuanto refiere las características de la medida cautelar que se solicite, resaltando en el presente caso no ser susceptible de sustitución por otra igualmente eficaz pero menos gravosa o perjudicial para el demandado.

La procedencia del embargo preventivo viene abonada por recaer sobre el solicitado una obligación de prestación pecuniaria (artículo 727.1.ª LEC).

III.- De los documentos presentados aparece inequívocamente la existencia y subsistencia del crédito ostentado por mi patrocinado frente a D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDADO], existiendo suficientes indicios de que, de no adoptarse inmediatamente la medida solicitada, podría quedar vacío de contenido el derecho de mi patrocinado, al estar desprendiéndose de los bienes que posee y no tener ninguna fuente de ingresos conocida (artículo 728.1 LEC).

IV.- La circunstancia de solicitarse la adopción de la medida en este momento obedece a que hasta el presente no constaban elementos que permitieran dudar fundadamente de la solvencia del demandado ni de circunstancias que comprometan gravemente la ejecución de la sentencia de condena (artículo 730.4 LEC).

V.- A los efectos dispuestos en el artículo 728 LEC, por esta parte se ofrece prestar la caución que por el Tribunal se señale para responder, de manera rápida y efectiva, de los daños y perjuicios que la adopción de la medida cautelar pudiera causar al patrimonio del demandado.

Igualmente, y conforme a lo que previene el artículo 732.3 LEC, hacemos constar que la caución que se ofrece lo es por la cantidad de [IMPORTE] euros, que es la señalada como cuantía en el escrito inicial por corresponderse con el principal e intereses vencidos que se reclaman, y cuya fianza se constituiría mediante [ELEGIR: aval bancario por plazo indefinido / otra forma de caución].

Por lo expuesto,

SUPLICO AL TRIBUNAL, que teniendo por presentado este escrito se sirva admitirlo, y tenga por formulada solicitud de medida cautelar de embargo preventivo de los bienes del demandado D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDADO], y, seguido el trámite legal, se dicte resolución dando lugar al mismo y acordándolo por la cuantía que se reclama como principal en la demanda, más la señalada prudencialmente por intereses y costas, señalando en su caso la caución a prestar por mi parte.

Es de justicia que pido en [LOCALIDAD], a [FECHA].

OTROSÍ DIGO que, a los efectos de lo prevenido en el artículo 732.2 LEC, y para el caso de que los documentos acompañados no se reputaran suficientes, esta parte ofrece los siguientes medios de prueba para acreditar los extremos en que se funda la pretensión: [MEDIOS DE PRUEBA].

En su virtud,

SUPLICO AL TRIBUNAL se sirva acordar de conformidad con lo interesado.

Reitero justicia en lugar y fecha ut supra.

Por ser de justicia que pido en [LOCALIDAD], a [FECHA].

Firma del Abogado/a: [NOMBRE Y APELLIDOS DEL LETRADO] — Col. n.º [Nº DE COLEGIADO]

Firma del Procurador/a: [NOMBRE Y APELLIDOS DEL PROCURADOR]

NOTAS DE USO

Una vez presentada la demanda o pendiente el recurso, el demandante deberá justificar adecuadamente una solicitud de medidas cautelares que no se presenta con la demanda o incluso antes de ésta. En este supuesto, además, tendrá que aclarar las razones de urgencia o de prevención para que se adopten sin oír al afectado.
