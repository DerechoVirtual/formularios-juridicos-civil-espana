---
name: solicitud-arbitraje-consumo-facturacion-telefonia-civ-1786
description: "Solicitud de arbitraje de consumo por la facturación de telefonía. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud de arbitraje de consumo por la facturación de telefonía

> Formulario **CIV-1786** del plugin **Mediación, MASC, arbitraje y jurisdicción voluntaria** (`formularios-mediacion-arbitraje-y-voluntaria`) · Civil › Jurisdicción voluntaria, MASC, mediación y arbitraje · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud de arbitraje de consumo por la facturación de telefonía» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud de arbitraje de consumo por la facturación de telefonía” para mi caso». También puedes invocarla directamente con `/formularios-mediacion-arbitraje-y-voluntaria:solicitud-arbitraje-consumo-facturacion-telefonia-civ-1786`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-mediacion-arbitraje-y-voluntaria:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Mediación, MASC, arbitraje y jurisdicción voluntaria) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (6 veces)
- [ ] DENOMINACIÓN SOCIAL (4 veces)
- [ ] MES (4 veces)
- [ ] Nº DE DOCUMENTO (4 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] CALLE (2 veces)
- [ ] FECHA (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] Nº (2 veces)
- [ ] CORREO ELECTRÓNICO
- [ ] DNI/NIE
- [ ] Nº DE FAX
- [ ] NÚMERO

## Normas que cita el formulario

- art. 1 Real Decreto 713/2024

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

A LA JUNTA ARBITRAL DE CONSUMO DE [LOCALIDAD]

D./Dª. [NOMBRE Y APELLIDOS], con D.N.I., legal representante de la persona/consumidor, con D.N.I [DNI/NIE], lo cual acredito mediante el documento adjunto acompañado como número 1, con domicilio en calle [CALLE] de [LOCALIDAD] (correo electrónico [CORREO ELECTRÓNICO] o fax [Nº DE FAX]), el cual se designa a efectos de notificaciones, en nombre de la persona/consumidor que representa EXPONE:

1) Que mediante el presente escrito formulo reclamación contra la Compañía XXX [DENOMINACIÓN SOCIAL] con domicilio en [LOCALIDAD] por importe de [IMPORTE] euros como consecuencia del exceso de facturación telefónica girada en los meses [MES] a

2) La empresa reclamada está adherida al Sistema Arbitral de Consumo.

3) Que a los efectos del art. 57 del Texto Refundido de Ley General para la Defensa de los Consumidores y Usuarios, de 16 de noviembre de 2007 y el artículo 1 del Real Decreto 713/2024, de 23 de julio, por el que se aprueba el Reglamento que regula el Sistema Arbitral de Consumo, me someto a la decisión arbitral prevista por estos preceptos, y acepto expresamente el cumplimiento del laudo emitido para la resolución de la cuestión litigiosa planteada en esta solicitud. Asimismo manifiesta que no ha interpuesto reclamación por el mismo asunto en otra Junta Arbitral, ni en sede judicial.

La reclamación arbitral que inicio mediante este escrito se funda en los siguientes:

HECHOS Y FUNDAMENTOS

El día [FECHA] concerté un contrato de suscripción a tarifa plana con la empresa telefónica reclamada, interviniendo en su nombre el Sr. [NOMBRE Y APELLIDOS], quien figura en el contrato como delegado comercial de la reclamada (acompaño como documento número [Nº DE DOCUMENTO] contrato de suscripción a tarifa plana suscrito entre el solicitante y el delegado comercial de la reclamada).

Desde este momento debe advertirse que el contrato era de los denominados de adhesión, apareciendo firmado únicamente en su anverso, y sin obrar firma alguna en su reverso en cuanto a las posibles cláusulas de exclusión que pudieran ser objeto de aplicación.

En el contrato concertado se hacía consta la modalidad de contratación, fijándose un precio del servicio por importe de [IMPORTE] euros mensuales más IVA, reseñándose los distintos teléfonos de mi propiedad que estaban incluidos en la contratación. En cumplimiento de lo pactado, procedí a dar de baja el servicio telefónico con mi anterior suministradora [DENOMINACIÓN SOCIAL] tal como justifico con los documentos número [Nº DE DOCUMENTO] que acompaño.

En fecha [FECHA] la reclamada giró una factura de [IMPORTE] euros por el consumo realizado en los meses de [MES] a [MES], sin aplicar dicha tarifa plana y aplicando sus precios ordinarios de facturación, lo cual motiva la presente reclamación (acompaño como documentos [Nº] copias de las facturas controvertidas).

Dichas facturas fueron cargadas en mi cuenta número [NÚMERO], habiendo hecho efectivo el importe de [IMPORTE] euros (acompaño como documento [Nº DE DOCUMENTO] certificado de la entidad bancaria sobre el abono de las facturas).

Ante este irregular proceder de la entidad reclamada, formulé la oportuna reclamación, recibiendo como respuesta, tras múltiples gestiones, que existía una exclusión de la tarifa plana para los profesionales que está expresada en las cláusulas del anverso del contrato (se acompañan como documentos [Nº] copias de la reclamación formulada y contestación de la entidad reclamada).

La reclamación se funda en que no ostento la calidad de profesional y, además, la empresa reclamada ha incumplido lo dispuesto en el art. 61 y preceptos concordantes del Texto Refundido de la Ley de Consumidores y Usuarios, así como en el art. 7 de la Ley de Condiciones Generales de la Contratación.

Así, por una parte, no ostento la condición de profesional, por cuanto que los teléfonos contratados son para uso particular. De hecho, el despacho profesional para el que trabajo está sito en la calle [CALLE], siendo titularidad de la sociedad [DENOMINACIÓN SOCIAL], la cual lógicamente tiene contratado su propio servicio telefónico. Acredito este extremo mediante certificado expedido por dicha sociedad que acompaño como documento

Por otra parte, en el folleto publicitario entregado por el delegado comercial de la empresa reclamada, donde se ofertaban y publicitaban los servicios en régimen de tarifa plana, en ningún momento se excluía a los profesionales (acompaño como documento [Nº DE DOCUMENTO] copia del folleto publicitario), por lo que por aplicación del citado art. 61 del RDLeg. 1/2007, la reclamada quedaba vinculada a la oferta publicitada.

Por último, la condición general de exclusión de la tarifa plana en el caso de profesionales no ha quedado válidamente incorporada al contrato, al no haber sido firmada, siendo necesario conforme al art. 5 de la Ley de Condiciones Generales de la Contratación.

La aplicación de dichos preceptos determina la aplicación de la tarifa plana en cumplimiento del contrato suscrito, manifestando expresamente que en ningún momento he sido informado ni por la empresa reclamada ni por su delegado que los teléfonos pertenecientes a profesionales estaban excluidos del ámbito del contrato.

Como consecuencia del recto cumplimiento del contrato, reclamo la cantidad total de [IMPORTE] euros que resultan de detraer el importe del precio pactado en facturación por la modalidad de tarifa plana del importe indebidamente percibido por la empresa reclamada en la facturación de los meses [MES] la cual deberá ser satisfecha por la empresa reclamada, cantidad que deberá incrementarse en los intereses legales correspondientes.

En virtud de lo expuesto, es de justicia y por ello

SOLICITA A LA JUNTA ARBITRAL que tenga por formulada esta reclamación y, tras los trámites legales y de conformidad a lo expuesto en este escrito, dicte laudo condenando a la empresa [DENOMINACIÓN SOCIAL] a indemnizar a quien suscribe en la cantidad de [IMPORTE] euros, con más los intereses legales correspondientes, por los hechos y en virtud de los fundamentos que dejo expuestos en la presente solicitud.

Firmado:

========================================================================
