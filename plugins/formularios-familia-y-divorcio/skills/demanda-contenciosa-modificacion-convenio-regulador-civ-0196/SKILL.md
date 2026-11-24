---
name: demanda-contenciosa-modificacion-convenio-regulador-civ-0196
description: "Demanda contenciosa de modificación del convenio regulador para extinguir la pensión compensatoria. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda contenciosa de modificación del convenio regulador para extinguir la pensión compensatoria

> Formulario **CIV-0196** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Demanda contenciosa de modificación de medidas definitivas por la que el cónyuge obligado al pago solicita que se declare la extinción de la pensión compensatoria fijada en el convenio regulador del divorcio, por haber cesado la causa que la motivó (desaparición del desequilibrio económico). Se usa cuando, pasado el tiempo, han cambiado sustancialmente las circunstancias económicas de ambos ex cónyuges.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda contenciosa de modificación del convenio regulador para extinguir la pensión compensatoria» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda contenciosa de modificación del convenio regulador para extinguir la pensión compensatoria” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-contenciosa-modificacion-convenio-regulador-civ-0196`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS DE LA DEMANDADA (7 veces)
- [ ] AÑO (6 veces)
- [ ] DÍA (6 veces)
- [ ] IMPORTE (6 veces)
- [ ] MES (6 veces)
- [ ] Nº DE DOCUMENTO (6 veces)
- [ ] NOMBRE Y APELLIDOS DEL DEMANDANTE (5 veces)
- [ ] Nº (5 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] SEDE (3 veces)
- [ ] FECHA (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] CALLE
- [ ] DENOMINACIÓN SOCIAL
- [ ] DOMICILIO
- [ ] IMPORTE EN CIFRAS
- [ ] NOMBRE Y APELLIDOS DEL ABOGADO/A
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] Nº DE DOCUMENTOS
- [ ] Nº DE PROCEDIMIENTO
- [ ] ORDINAL DE LA CLÁUSULA
- [ ] PRESTACIÓN O SUBSIDIO DE DESEMPLEO
- [ ] SECCIÓN

## Normas que cita el formulario

- art. 81 CC
- art. 770 LEC
- art. 775.2 LEC
- art. 23 LEC
- art. 437.1 LEC
- art. 5 Ley Orgánica 1/2025
- art. 90 CC
- art. 775.1 LEC
- art. 101 Código Civil
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

- Junto a «…d: sustituir el encabezamiento por «A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

A LA SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD DEL TRIBUNAL DE INSTANCIA DE [SEDE]

[OPCIONAL — si en el partido judicial no existe Sección de Familia, Infancia y Capacidad: sustituir el encabezamiento por «A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»]

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDANTE], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], y que es dirigido por el Letrado/a D./Dña. [NOMBRE Y APELLIDOS DEL ABOGADO/A], ejerciente en el Ilustre Colegio de la Abogacía de [LOCALIDAD], y con despacho abierto en [LOCALIDAD], calle [CALLE] n.º [Nº], ante el Tribunal comparezco y, como mejor proceda en Derecho, DIGO:

Que mediante el presente escrito formulo DEMANDA DE MODIFICACIÓN DE MEDIDAS DEFINITIVAS contra D./Dña. [NOMBRE Y APELLIDOS DE LA DEMANDADA], cuyo domicilio es [DOMICILIO], basándola en los siguientes hechos y fundamentos de derecho:

HECHOS

PRIMERO.- D./Dña. [NOMBRE Y APELLIDOS DE LA DEMANDADA] y mi representado se hallan divorciados en virtud de sentencia firme de fecha [DÍA] de [MES] de [AÑO], dictada por la Sección [SECCIÓN] del Tribunal de Instancia número [Nº] de [SEDE], en los autos de divorcio de mutuo acuerdo n.º [Nº DE PROCEDIMIENTO]. En dicha sentencia, que es firme, se aprobaba en su integridad el convenio suscrito por ambas partes con fecha [FECHA]. El contenido del convenio no ha sido modificado por ninguna otra resolución.

Se acompaña testimonio de la resolución judicial y el convenio regulador como documentos n.º [Nº DE DOCUMENTO] y [Nº DE DOCUMENTO].

SEGUNDO.- En el citado convenio regulador, teniendo en cuenta las circunstancias concurrentes, se establecía en la cláusula [ORDINAL DE LA CLÁUSULA]: «D./Dña. [NOMBRE Y APELLIDOS] abonará a D./Dña. [NOMBRE Y APELLIDOS] en concepto de pensión compensatoria la cantidad de [IMPORTE] euros ([IMPORTE EN CIFRAS] €) mensuales. Dicha cantidad será ingresada mensualmente y revisada anualmente a tenor de lo establecido en el apartado anterior para los alimentos».

Las partes han efectuado las actualizaciones correspondientes de las pensiones fijadas en el referido convenio regulador de divorcio, ascendiendo en la actualidad la pensión compensatoria a favor de D./Dña. [NOMBRE Y APELLIDOS DE LA DEMANDADA] a [IMPORTE] euros mensuales.

TERCERO.- Han transcurrido [Nº] años desde que se fijó la pensión compensatoria a favor de la demandada en el convenio de divorcio y la situación actual de D./Dña. [NOMBRE Y APELLIDOS DE LA DEMANDADA] y de D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDANTE] ha variado sustancialmente, desapareciendo el desequilibrio que se producía para D./Dña. [NOMBRE Y APELLIDOS DE LA DEMANDADA] en el momento de la ruptura del matrimonio y que justificó la fijación de una pensión compensatoria.

Ciertamente, ambos contrajeron matrimonio muy jóvenes y, en el momento del divorcio, producido cuando habían transcurrido [Nº] años de convivencia, la esposa carecía de ingresos económicos propios. Por el contrario, D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDANTE] disponía de un puesto de trabajo remunerado en la empresa [DENOMINACIÓN SOCIAL], percibiendo unos ingresos netos de [IMPORTE] euros.

Mas en la actualidad la demandada percibe de forma regular y continuada una pensión por [CLASE DE PENSIÓN: p. ej., incapacidad permanente absoluta] por una cuantía mensual, prorrateadas las [Nº] pagas que cobra al año, de [IMPORTE] euros mensuales. Dicho extremo se acredita mediante el/los documento(s) núm(s). [Nº DE DOCUMENTOS] de los que acompañan a la demanda.

Por el contrario, D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDANTE] fue despedido/a en fecha [FECHA], encontrándose actualmente en situación de desempleo, hecho que se acredita mediante documento nº [Nº DE DOCUMENTO]. Desde el [DÍA] de [MES] de [AÑO] hasta el [DÍA] de [MES] de [AÑO], el demandante ha pasado a percibir una cantidad de [IMPORTE] euros en concepto de [PRESTACIÓN O SUBSIDIO DE DESEMPLEO] y, desde el [DÍA] de [MES] de [AÑO] hasta el [DÍA] de [MES] de [AÑO], la cantidad percibida se ha reducido a [IMPORTE] euros, como acredita la certificación que se acompaña como documento n.º [Nº DE DOCUMENTO].

CUARTO.- Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS: mediación / conciliación privada / opinión neutral de persona experta independiente / oferta vinculante confidencial / negociación directa, con o sin abogado / proceso de Derecho colaborativo / otra actividad negociadora reconocida en esta u otras leyes, estatales o autonómicas], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento nº [Nº DE DOCUMENTO] [DOCUMENTO QUE ACREDITA QUE SE HA ACUDIDO AL MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS].

A los anteriores hechos son de aplicación los siguientes,

FUNDAMENTOS DE DERECHO

I.- COMPETENCIA.

Conforme a lo establecido en el art. 769.1, párrafo 2.º LEC, como fuero de competencia territorial residual, la residencia última de la demandada fija la circunscripción del órgano competente para conocer del procedimiento de modificación de medidas.

II.- LEGITIMACIÓN.

La legitimación activa y pasiva para intervenir en el procedimiento corresponde a ambos cónyuges (arts. 81, 86, 90 y 91 CCiv).

III.- PROCEDIMIENTO.

La modificación de las medidas definitivas tiene asignado el procedimiento previsto en el art. 770 LEC, o lo que es lo mismo, los trámites del procedimiento principal de separación y divorcio, de conformidad con el art. 775.2 LEC, dado que no son de mutuo acuerdo ni propuestas por un cónyuge con el consentimiento del otro.

IV.- POSTULACIÓN Y DEFENSA.

Conforme a lo previsto en los arts. 23 y 31 LEC, se presenta la demanda por medio de Procurador legalmente habilitado y bajo dirección de Letrado firmante de la misma.

V.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4.º y 399.3, en relación con el art. 437.1 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

VI.- FUNDAMENTOS DE DERECHO MATERIALES O SOBRE EL FONDO DEL ASUNTO.

Los arts. 90 y 91 CCiv señalan que las medidas que el Juez acuerde en defecto de acuerdo, o las convenidas por los cónyuges, podrán ser modificadas judicialmente o por nuevo convenio cuando se alteren sustancialmente las circunstancias, prevención que es presupuesto de este proceso, según la mención explícita del art. 775.1 LEC.

El artículo 101 del Código Civil señala que el derecho a la pensión se extingue por el cese de la causa que lo motivó, y teniendo en cuenta que la causa que justificó la fijación de la pensión fue el desequilibrio económico entre ambos cónyuges, hoy día es evidente que este desequilibrio ya no existe entre D./Dña. [NOMBRE Y APELLIDOS DE LA DEMANDADA] y mi representado, sino que, muy al contrario, es D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDANTE] quien actualmente cuenta con escasos medios de vida.

VII.- COSTAS.

No hay razón para inaplicar el principio del vencimiento en punto a costas procesales, en armonía con el art. 394 LEC, a fin de que esta parte salga indemne de que se le reconozca su derecho frente a la resistencia de la demandada.

En su virtud,

SUPLICO AL TRIBUNAL

Que, habiendo por presentado este escrito junto con los documentos y copias que se acompañan, se sirva admitirlo, teniéndome por parte en la representación que acredito y por formulada demanda de modificación de medidas definitivas, y previos los trámites legales, se dicte sentencia declarando la extinción de la pensión compensatoria señalada a favor de D./Dña. [NOMBRE Y APELLIDOS DE LA DEMANDADA], con expresa condena en costas a la parte demandada.

Es justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Abogado/a | Firma del Procurador/a

NOTAS DE AYUDA

Requisito de procedibilidad: las partes pueden cumplir el requisito de procedibilidad que con carácter general exige la LO 1/2025 mediante mediación, conciliación privada, la opinión neutral de una persona experta independiente, si se formula una oferta vinculante confidencial o si se emplea cualquier otro tipo de actividad negociadora reconocida en esta u otras leyes, estatales o autonómicas, tales como la negociación directa (con o sin abogado) o un proceso de Derecho colaborativo. Debe especificarse el documento que acredita que se ha acudido a uno de estos medios.
