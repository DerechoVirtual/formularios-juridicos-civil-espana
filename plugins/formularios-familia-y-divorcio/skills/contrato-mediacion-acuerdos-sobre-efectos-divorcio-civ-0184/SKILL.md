---
name: contrato-mediacion-acuerdos-sobre-efectos-divorcio-civ-0184
description: "Contrato de mediación con acuerdos sobre los efectos del divorcio. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de mediación con acuerdos sobre los efectos del divorcio

> Formulario **CIV-0184** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de mediación con acuerdos sobre los efectos del divorcio» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de mediación con acuerdos sobre los efectos del divorcio” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:contrato-mediacion-acuerdos-sobre-efectos-divorcio-civ-0184`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (9 veces)
- [ ] AÑO (7 veces)
- [ ] DÍA (7 veces)
- [ ] MES (7 veces)
- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] CALLE (3 veces)
- [ ] IMPORTE (2 veces)
- [ ] NOMBRE DEL HIJO (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] DATOS REGISTRALES
- [ ] LUGAR

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

Contrato mediado en que se adoptan acuerdos destinados a regular los efectos del divorcio de las partes
Lugar y fecha
REUNIDOS
INTERVIENEN
MANIFIESTAN
ESTIPULACIONES
Firmas

CONTRATO MEDIADO EN QUE SE ADOPTAN ACUERDOS DESTINADOS A REGULAR LOS EFECTOS DEL DIVORCIO DE LAS PARTES

En [LUGAR], a [DÍA] de [MES] de [AÑO].

REUNIDOS

I) DON/DOÑA [NOMBRE Y APELLIDOS], mayor de edad, casado/a, vecino/a de [LOCALIDAD], con domicilio en la calle [CALLE], con D.N.I./N.I.F.

II) DON/DOÑA [NOMBRE Y APELLIDOS], mayor de edad, casado/a, vecino/a de [LOCALIDAD], con domicilio en la calle [CALLE], con D.N.I./N.I.F.

INTERVIENEN

Son consortes y actúan en su propio nombre y derecho, reconociéndose mutuamente la capacidad legal necesaria para pactar el siguiente contrato, a cuyo fin

MANIFIESTAN

Que contrajeron matrimonio [ELEGIR: civil / canónico] en [LOCALIDAD], el día [DÍA] de [MES] de [AÑO], que se halla inscrito en el Registro Civil de [LOCALIDAD], al

Que del referido matrimonio han nacido y viven dos hijos/as. El/La hijo/a, llamado/a [NOMBRE DEL HIJO], mayor de edad, nació el [DÍA] de [MES] de [AÑO] y su nacimiento fue inscrito en el Registro Civil de [LOCALIDAD], al [DATOS REGISTRALES] El/La hijo/a llamado/a [NOMBRE DEL HIJO], menor de edad, nació el día [DÍA] de [MES] de [AÑO], inscribiéndose su nacimiento en el Registro Civil de [LOCALIDAD], al

Que el matrimonio ha venido rigiéndose por el régimen legal supletorio de sociedad de gananciales, hasta el [DÍA] de [MES] de [AÑO], fecha en que los cónyuges pactaron el de absoluta separación de bienes, con disolución y liquidación de gananciales, mediante capitulaciones matrimoniales otorgadas ante el Notario de [LOCALIDAD], Don/Doña [NOMBRE Y APELLIDOS], con el número [NÚMERO] de su protocolo.

Que los cónyuges se hayan separados de hecho desde el día [DÍA] de [MES] de [AÑO], conviviendo cada uno en distintos domicilios, viviendo los hijos con su madre. Y que han decidido divorciarse.

Que los cónyuges, con el fin de gestionar del mejor modo posible los efectos de su proyectado divorcio, el día [DÍA] de [MES] de [AÑO] recurrieron al Servicio de Mediación Familiar de [LOCALIDAD] e iniciaron un proceso de mediación, actuando como profesional mediador Don/Doña [NOMBRE Y APELLIDOS] El objeto de la mediación comprendía los siguientes aspectos:

A) Sus responsabilidades parentales, incluyendo el ejercicio de la patria potestad sobre su hijo/a menor y la contribución a sus alimentos, así como los alimentos a favor del hijo mayor de edad, que carece de independencia económica.

B) La atribución del uso de la vivienda y ajuar familiar.

C) Las posibles compensaciones económicas entre cónyuges.

VI. Como resultado del proceso de mediación, las partes han llegado a una serie de acuerdos que formalizan en el presente contrato, de acuerdo con las siguientes

ESTIPULACIONES

De los hijos

El hijo/a menor habido/a del matrimonio, queda bajo la guarda y custodia de su madre, sin perjuicio de estar sujeto/a a la patria potestad de ambos progenitores.

Se establece en favor del padre el régimen de visitas siguiente:

A) Con carácter alterno, el padre recogerá al hijo/a, para tenerlo/a consigo, los fines de semana, desde las 9 horas del sábado hasta las 20 horas del domingo.

B) El padre será quien recogerá y devolverá al hijo/a, en las horas indicadas en el apartado anterior, en el domicilio de la madre, a la que avisará para recogerlo/a o dejarlo/a.

C) En relación con las vacaciones escolares de Navidad, Semana Santa y Pascua de Resurrección, al hijo/a pasará la mitad de las mismas con cada uno de los padres, correspondiendo, en caso de desacuerdo, la primera mitad del período al padre los años pares y la segunda los años impares. Durante las vacaciones quedará en suspenso el régimen de visitas del apartado A).

D) En cuanto a las vacaciones escolares de verano, al hijo/a permanecerá quince días con el padre y quince días con la madre, con el régimen de visitas del apartado A) en suspenso. Cada período de quince días deberá coincidir con el período de disfrute de vacaciones laborales del respectivo progenitor.

El resto de las vacaciones estivales, al hijo/a permanecerá con la madre con sujeción al régimen general de visitas del apartado A).

E) Para el disfrute de los períodos vacacionales será el padre quien recogerá y devolverá al hijo/a, haciéndolo la víspera del comienzo del período vacacional y devolviéndola al día siguiente del término antes de las doce horas. EI domicilio para recoger y devolver al hijo/a será aquél en que éste/a resida con su madre, aunque lo fuere accidentalmente.

F) Si por cualquier motivo el padre no pudiera tener consigo a su hijo/a durante todo o parte del período vacacional que le corresponda, de común acuerdo con su esposa y avisándola previamente, el hijo/a quedará en compañía de la madre.

G) Las comunicaciones entre padre e hijo/a que se establecen en el presente convenio estarán supeditadas a las necesidades escolares del hijo/a, enfermedades o prescripciones facultativas, causas de fuerza mayor, etc., en cuyo caso los cónyuges decidirán de común acuerdo lo que sea más beneficioso para al hijo/a.

Cualquier dolencia o enfermedad que pudiera padecer al hijo/a deberá ser notificada de inmediato por el cónyuge que lo/a tenga en su compañía al otro, pudiendo ser visitado/a sin limitación mientras dure la enfermedad.

H) Cualquier aspecto relacionado con la educación, docencia y formación del hijo/a, ya sea en colegio, campamentos o colonias especiales, deportes y otras actividades será decidido de común acuerdo entre los cónyuges, conforme a lo que sea mejor para el/la menor.

I) Los cónyuges se comunicarán el uno al otro el domicilio habitual y el teléfono al que pueden dejar avisos o noticias, así como la dirección donde vayan a residir en período de vacaciones.

J) EI régimen de visitas se establece en beneficio del/la menor y en atención a lo positivo que debe resultar para su rnaduración el trato con el progenitor no custodio, por lo que éste se compromete a tenerlo/a personalmente en su compañía los períodos correspondientes, y si por circunstancias excepcionales y esporádicas no pudiere cumplir con este deber personal de compañía, no encomendará el cuidado del/la menor a personas que no sean parientes consanguíneos dentro del segundo grado.

[ELEGIR UNA OPCIÓN: Ajuar familiar / A la esposa / A ambos cónyuges]

Vivienda

La vivienda que ha constituido el domicilio conyugal está sita en [LOCALIDAD], calle [CALLE] y pertenece a ambos cónyuges en proindiviso ordinario. Se atribuye el uso de esta vivienda al hijo/a menor y a su madre.

Liquidación del régimen económico

El matrimonio se rige en la actualidad por el régimen de absoluta separación de bienes, al haberlo acordado así los cónyuges en capitulaciones matrimoniales, por lo que no hay bienes que partir.

Cargas y alimentos

DON [NOMBRE Y APELLIDOS] establece como pensión de alimentos a favor de su hijo/a menor de edad, la suma de [IMPORTE] EUROS ( euros) mensuales, pagaderos por mensualidades anticipadas dentro de los cinco primeros días de cada mes en la cuenta bancaria que al efecto designe la esposa, cuya cantidad será actualizada anualmente conforme a la variación que experimente el Índice General Nacional del Sistema de Índices de Precios al Consumo.

Así mismo, DON [NOMBRE Y APELLIDOS] establece como pensión de alimentos a favor de su hijo/a mayor de edad, la suma de [IMPORTE] EUROS ( euros) mensuales, pagaderos por mensualidades anticipadas dentro de los cinco primeros días de cada mes en la cuenta bancaria nº [NÚMERO], de la que es titular el hijo/a, cuya cantidad será actualizada anualmente conforme a la variación que experimente el Índice General Nacional del Sistema de Índices de Precios al Consumo. Dicha pensión se establece por no contar el/la hijo/a con ingresos propios y encontrarse todavía en período de formación, viviendo en casa de su madre y será satisfecha mientras el/la hijo/a no finalice su formación por causa que no le sea imputable y carezca de medios de vida propios, conforme a lo establecido en los arts. 142 y ss. del Código civil.

[ELEGIR UNA OPCIÓN: Pensión compensatoria / Con pensión compensatoria / Sin pensión compensatoria]

Tramitación del divorcio

Este acuerdo será tramitado, por el abogado de las partes, como convenio regulador de los efectos de su divorcio en el procedimiento judicial que a tal efecto inicien, comprometiéndose los abajo firmantes a realizar cuanto fuere necesario para obtener la correspondiente sentencia de divorcio por el procedimiento de mutuo acuerdo, de tal manera que con la actuación de ambos se recoja el contenido de este documento, a cuyo fin se obligan a ratificar su contenido, como convenio regulador, por separado y a presencia judicial.

Así lo acuerdan y en prueba de conformidad firman ambas partes en el lugar y fecha indicados en el encabezamiento.

Firmas de las partes:

========================================================================
