---
name: solicitud-arbitraje-consumo-viaje-combinado-civ-1776
description: "Solicitud de arbitraje de consumo por un viaje combinado. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud de arbitraje de consumo por un viaje combinado

> Formulario **CIV-1776** del plugin **Mediación, MASC, arbitraje y jurisdicción voluntaria** (`formularios-mediacion-arbitraje-y-voluntaria`) · Civil › Jurisdicción voluntaria, MASC, mediación y arbitraje · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud de arbitraje de consumo por un viaje combinado» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud de arbitraje de consumo por un viaje combinado” para mi caso». También puedes invocarla directamente con `/formularios-mediacion-arbitraje-y-voluntaria:solicitud-arbitraje-consumo-viaje-combinado-civ-1776`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-mediacion-arbitraje-y-voluntaria:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Mediación, MASC, arbitraje y jurisdicción voluntaria) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (9 veces)
- [ ] IMPORTE (7 veces)
- [ ] FECHA (4 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] Nº DE DOCUMENTO (4 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] CALLE
- [ ] CORREO ELECTRÓNICO
- [ ] DESTINO
- [ ] Nº DE CLÁUSULA
- [ ] Nº DE FAX

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

D./Dª. [NOMBRE Y APELLIDOS], con D.N.I. y D./Dª. [NOMBRE Y APELLIDOS], con D.N.I., con domicilio en calle [CALLE] de [LOCALIDAD] (correo electrónico [CORREO ELECTRÓNICO] o fax [Nº DE FAX]), el cual se designa a efectos de notificaciones, en nombre propio EXPONEMOS:

1) Que mediante el presente escrito formulamos reclamación contra la empresa [DENOMINACIÓN SOCIAL] con domicilio en [LOCALIDAD] por importe de [IMPORTE] euros como consecuencia del incumplimiento del contrato de fecha [FECHA], en cuya cláusula [Nº DE CLÁUSULA] consta que la reclamación será resuelta a través del arbitraje de Consumo, tal como se acredita mediante copia del documento suscrito que se acompaña como número 1.

2) Que a los efectos del art. 57 del Texto Refundido de Ley General para la Defensa de los Consumidores y Usuarios, de 16 de noviembre de 2007 y el artículo 1 del Real Decreto 713/2024, de 23 de julio, por el que se aprueba el Reglamento que regula el Sistema Arbitral de Consumo, nos sometemos a la decisión arbitral prevista por estos preceptos, y acepto expresamente el cumplimiento del laudo emitido para la resolución de la cuestión litigiosa planteada en esta solicitud. Asimismo, manifestamos que no hemos interpuesto reclamación por el mismo asunto en otra Junta Arbitral, ni en sede judicial.

La reclamación arbitral que inicio mediante este escrito se funda en los siguientes:

HECHOS Y FUNDAMENTOS

Tal como consta en el contrato aportado, el día [FECHA] se concertó con la empresa reclamada un contrato de viaje combinado de [Nº] días de duración al destino vacacional [DESTINO], el cual incluía los vuelos de ida y vuelta, traslado en destino, alojamiento y media pensión, pactándose un precio por los citados servicios por importe de [IMPORTE] euros, que fueron satisfechos por el reclamante según acredito mediante recibo de pago que acompaño como documento número 2.

Según lo pactado en el contrato el viaje debía iniciarse el día [FECHA] a las [Nº] horas, siguiendo un plan de vuelo con enlace en el aeropuerto de [LOCALIDAD], donde, tras tres horas de espera, se tomaría un vuelo hacia el destino vacacional, teniendo prevista su llegada a las [Nº] horas del día [FECHA], siendo que el vuelo hacia el destino llegó efectivamente a las [Nº] horas del día siguiente, tras pernoctar los reclamantes en el aeropuerto de enlace, como se relata a continuación.

La reclamación se funda en el incumplimiento contractual de la empresa reclamada, ya que, como se ha indicado, el vuelo de ida llegó al destino un día después del contratado, como consecuencia del retraso de más de [Nº] horas en la salida del aeropuerto de partida, lo cual obligó al reclamante y a su familia a pernoctar en el aeropuerto de enlace, tras sufrir diversas vicisitudes que se exponen a continuación.

El retraso fue originado, según versión de la empresa reclamada, por una avería en el avión que debía partir del aeropuerto de origen, tal como consta en la contestación realizada por dicha empresa a la reclamación realizada por los que suscribimos que acompañamos como documento número

No obstante las explicaciones dadas por la empresa reclamada, éste era un claro supuesto previsible para la misma por lo que no puede ser considerado fuerza mayor, ni exonerarla al entrar en el ámbito de sus obligaciones la correcta ejecución del viaje en todas sus fases; así, el artículo 162.1 del Texto Refundido de la Ley de Consumidores y Usuarios establece que el viajero tendrá derecho a una reducción del precio adecuada por cualquier periodo durante el cual haya habido falta de conformidad, a menos que el organizador o el minorista demuestren que la falta de conformidad es imputable al viajero", añadiendo el párrafo segundo del citado precepto que "el viajero tendrá derecho a recibir una indemnización adecuada del organizador o, en su caso, del minorista por cualquier daño o perjuicio que sufra como consecuencia de cualquier falta de conformidad. La indemnización se abonará sin demora indebida". En todo caso, y conforme a las previsiones del artículo 162.2 de la misma Ley, debe ser la empresa reclamada quien pruebe la concurrencia de acontecimientos que no pueden ser previstos o superados.

En nuestro caso, el retraso en la salida en el aeropuerto de origen supuso la pérdida de avión en el aeropuerto de enlace que debía llevarnos al destino vacacional, lo cual nos obligó a nuevas esperas, recogida de maletas, traslados suplementarios, pernoctar en hotel y nueva facturación para coger el vuelo a destino, con pérdida de un día completo de vacaciones.

A efectos acreditativos de lo expuesto acompañamos los siguientes documentos: reclamaciones formuladas en el aeropuerto de origen y enlace (documentos número [Nº DE DOCUMENTO]), bonos de hotel en la ciudad del aeropuerto de enlace (documento [Nº DE DOCUMENTO]), reclamación formulada a la empresa reclamada (documento [Nº DE DOCUMENTO]), contestación de la empresa reclamada a la reclamación formulada (documento [Nº DE DOCUMENTO])

Como consecuencia de este incumplimiento contractual imputable a la empresa prestadora de los servicios, los reclamantes sufrieron los siguientes daños y perjuicios objeto de esta reclamación:

1) La llegada a destino el día posterior al pactado supuso la pérdida de un día completo y efectivo de estancia en el destino vacacional para el reclamante y su familia, por lo que se reclama por este concepto la cantidad de [IMPORTE] euros, es decir, un [Nº] por ciento del viaje, que corresponde al coste proporcional de un día sobre el precio total del viaje.

2) En el aeropuerto de enlace, los reclamantes estuvieron durante más de [Nº] horas hasta que se les asignó nuevo vuelo y se les facilitó hotel para pernoctar. Durante la estancia en el aeropuerto de enlace, tuvieron que hacerse cargo de los costes de almuerzo y cena por importe de [IMPORTE] euros, que se acreditan por los recibos que se acompañan como documentos

3) Tras una espera de más de [Nº] horas en el aeropuerto de origen, al llegar al aeropuerto de enlace, el reclamante y su familia tuvieron que recoger el equipaje porque se había perdido el vuelo de enlace como consecuencia del retraso, teniendo que sufrir una espera de más de [Nº] horas hasta que se asignó nuevo vuelo. Asimismo, tuvieron que realizar la recogida de equipaje para poder pernoctar en el hotel facilitado por la Compañía aérea.

Al día siguiente, y para tomar el vuelo hacia destino, tuvieron que facturar el equipaje nuevamente, con las esperas correspondientes.

Todo ello supuso graves molestias y sufrimiento para el reclamante y su familia, por lo que se reclama la cantidad de [IMPORTE] euros por los daños morales sufridos por la pérdida del enlace, carreras en el aeropuerto, espera en aeropuerto de origen, espera por cambio de vuelo y devolución de equipajes, traslados suplementarios, deshacer y hacer el equipaje para pernoctar y espera para nuevo embarque al día siguiente.

En consecuencia, se solicita la cantidad total de [IMPORTE] euros por la pérdida de un día vacacional, gastos adicionales y daños morales, la cual deberá ser satisfecha por la empresa reclamada por cuanto estos daños y perjuicios han sido irrogados por el incumplimiento contractual de ésta, cantidad que deberá incrementarse en los intereses legales correspondientes.

En virtud de lo expuesto, es de justicia y por ello

SOLICITA A LA JUNTA ARBITRAL que tenga por formulada esta reclamación y, tras los trámites legales y de conformidad a lo expuesto en este escrito, dicte laudo condenando a la empresa [DENOMINACIÓN SOCIAL] a indemnizar a quien suscribe en la cantidad de [IMPORTE] euros, con más los intereses legales correspondientes, por los hechos y en virtud de los fundamentos que dejo expuestos en la presente solicitud.

Firmado:

========================================================================
