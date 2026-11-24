---
name: contestacion-pide-seguir-divorcio-mutuo-acuerdo-civ-0348
description: "Contestación que pide seguir el divorcio por mutuo acuerdo aportando convenio regulador. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contestación que pide seguir el divorcio por mutuo acuerdo aportando convenio regulador

> Formulario **CIV-0348** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Escrito, en trámite de contestación a la demanda de divorcio, solicitando se proceda a transformar el procedimiento al establecido para las solicitudes de divorcio de común acuerdo por ambos cónyuges, o por uno de ellos con el consentimiento del otro. Se aporta convenio regulador, posteriormente no aprobado por estipular un régimen genérico de comunicaciones y visitas del padre a los hijos menores.

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contestación que pide seguir el divorcio por mutuo acuerdo aportando convenio regulador» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contestación que pide seguir el divorcio por mutuo acuerdo aportando convenio regulador” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:contestacion-pide-seguir-divorcio-mutuo-acuerdo-civ-0348`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (10 veces)
- [ ] NÚMERO (5 veces)
- [ ] FECHA (4 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] CALLE (2 veces)
- [ ] LUGAR (2 veces)
- [ ] Nº (2 veces)
- [ ] IMPORTE
- [ ] LIBRO
- [ ] NOMBRE DEL HIJO/A
- [ ] Nº DE PROCEDIMIENTO

## Normas que cita el formulario

- art. 90 CC
- art. 770.5 LEC
- art. 777 LEC

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

AL TRIBUNAL

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales que actúa en nombre y representación de Dña. [NOMBRE Y APELLIDOS], como tengo acreditado en autos de Juicio de Divorcio nº [Nº DE PROCEDIMIENTO] / promovidos a mi instancia, y asimismo de D [NOMBRE Y APELLIDOS], que ha sido el demandado, a virtud de escritura de poder para pleitos que aceptado acompaño, con ruego de devolución previo testimonio bastante en actuaciones, ante el Tribunal comparezco y como mejor proceda en Derecho, DIGO:

Al recibir la demanda de divorcio D [NOMBRE Y APELLIDOS], reanudó sus contactos con la esposa demandante, que se habían interrumpido tiempo antes, a propósito de la actualización de las condiciones de su relación y situación de los hijos comunes, decididos a disolver el vínculo conyugal, y bajo asesoramiento del/la Letrado/a D./Dña. [NOMBRE Y APELLIDOS], y las dos partes han llegado a suscribir el correspondiente convenio regulador de divorcio, con el contenido del art. 90 CCiv.

Al no constituir causas materiales la Ley para la extinción del vínculo matrimonial por divorcio, fuera de la libre voluntad de los cónyuges, ahora hacen suya la voluntad del demandante a no seguir casado ambos cónyuges, bajo la misma representación y defensa.

Conforme al art. 770.5ª LEC, en cualquier momento del proceso, concurriendo los requisitos señalados en el art. 777 LEC, las partes pueden solicitar que continúe el procedimiento por los trámites que se establecen en este artículo, como es el caso.

Por todo lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito con la propuesta de convenio regulador acompañado, y por conforme entre partes la pretensión principal de la demanda, admitida con sus documentos, se proceda a transformar el procedimiento al establecido para las solicitudes de divorcio de común acuerdo por ambos cónyuges, o por uno de ellos con el consentimiento del otro, llevando su curso a dictar sentencia que declare la disolución por divorcio del matrimonio de mis representados D [NOMBRE Y APELLIDOS] y Dña. [NOMBRE Y APELLIDOS], con los efectos inherentes y homologación de las medidas del convenio regulador aportado.

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a

CONVENIO REGULADOR DE DIVORCIO

En [LUGAR], a [FECHA].

REUNIDOS

DE UNA PARTE,

D, mayor de edad, casado, con domicilio en [LOCALIDAD], calle [CALLE], número [NÚMERO], provisto de D.N.I. número [NÚMERO]

Y DE OTRA,

Dña. [NOMBRE Y APELLIDOS], mayor de edad, casada, con domicilio en [LOCALIDAD], calle [CALLE], número [NÚMERO], provista de D.N.I. número [NÚMERO]

Ambas partes actúan en su propio nombre y derecho, y recíprocamente se reconocen la capacidad legal y legitimación para llevar a efecto el presente convenio regulador de los efectos de su divorcio, y a tal fin,

EXPONEN

PRIMERO.- Que los suscritos contrajeron matrimonio canónico en [LOCALIDAD] el día [FECHA], inscrito en el Registro Civil de [LOCALIDAD] al folio nº [NÚMERO] del Libro [LIBRO] de la Sección

SEGUNDO.- Que de dicho matrimonio han nacido y viven los siguientes hijos: de [Nº] años de edad, y [NOMBRE DEL HIJO/A] de [Nº] años de edad, bajo la potestad de sus padres.

TERCERO.- Que los cónyuges contratantes están separados de hecho por mutuo acuerdo, habiéndolo documentado en escritura pública de fecha [FECHA], que disolvió el régimen de gananciales, liquidándolo posteriormente, y es su intención solicitar judicialmente el divorcio, y a tal fin,

ACUERDAN

I.- Guarda y custodia de los hijos: Los hijos quedan bajo la guarda y custodia de la madre, con la que convivirán. La patria potestad sobre los hijos será compartida por ambos progenitores.

II.- Cuidado de los hijos, comunicación y estancias: El padre podrá estar en compañía de sus hijos cuando lo estime conveniente siempre que preavise a la madre manteniendo la costumbre practicada hasta la fecha.

III.- Alimentos a los hijos: Se fija la cantidad de [IMPORTE] euros mensuales en concepto de contribución del padre a los alimentos para sus hijos. Dicha cantidad será ingresada mensualmente, por meses anticipados, dentro de los cinco primeros días de cada mes, en la cuenta corriente que la esposa designe.

Esta cantidad será revisada anualmente en proporción a las variaciones del Indice de Precios al Consumo General que publique el Instituto Nacional de Estadística o cualquier otro organismo público que en el futuro pudiera cumplir análoga misión.

IV.- Compensación por desequilibrio: Ambos cónyuges manifiestan que pueden atender a sus propias necesidades con sus respectivos ingresos, por lo que no es preciso que se fije cantidad alguna en concepto de pensión.

V.- Liquidación de la sociedad de gananciales: Los esposos manifiestan no poseer más bienes de naturaleza ganancial que los que en su día convinieron repartir.

El presente convenio surte efectos entre las partes desde el día de hoy, y para que así conste, lo firman por duplicado en el lugar y fecha "ut supra".

Firma de Don [NOMBRE Y APELLIDOS].	Firma de Doña [NOMBRE Y APELLIDOS]

========================================================================
