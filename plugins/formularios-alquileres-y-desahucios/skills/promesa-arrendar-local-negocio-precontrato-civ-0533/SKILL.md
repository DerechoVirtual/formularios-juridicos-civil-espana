---
name: promesa-arrendar-local-negocio-precontrato-civ-0533
description: "Promesa de arrendar un local de negocio (precontrato). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Promesa de arrendar un local de negocio (precontrato)

> Formulario **CIV-0533** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Promesa de arrendar un local de negocio (precontrato)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Promesa de arrendar un local de negocio (precontrato)” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:promesa-arrendar-local-negocio-precontrato-civ-0533`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (6 veces)
- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] NÚMERO (5 veces)
- [ ] CALLE (3 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] ESTADO CIVIL (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] CARGO
- [ ] DATOS REGISTRALES
- [ ] DESCRIPCIÓN DEL BIEN
- [ ] DOMICILIO
- [ ] MEDIO DE PAGO

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

Precontrato o promesa de arrendamiento de local de negocio, incluyendo las condiciones, estipulaciones y circunstancias necesarias para llevar a cabo el arrendamiento, así como los derechos y obligaciones de las partes.

En [LOCALIDAD], a [FECHA],

REUNIDOS

DE UNA PARTE,

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, [ESTADO CIVIL], con domicilio en [LOCALIDAD], calle [CALLE], provisto de N.I.F. número [NÚMERO],

Y DE OTRA,

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, [ESTADO CIVIL], con domicilio en [LOCALIDAD], calle [CALLE], provisto de N.I.F. número [NÚMERO],

INTERVIENEN

El primero, como [CARGO] en nombre y representación de la sociedad denominada [DENOMINACIÓN SOCIAL], constituida por escritura pública otorgada el [FECHA] ante el Notario de [LOCALIDAD] D./Dña. [NOMBRE Y APELLIDOS] con el número [NÚMERO] de su protocolo, domiciliada en [DOMICILIO] calle [CALLE] y con N.I.F número [NÚMERO]. Está autorizado para la celebración de este acto, en virtud del poder que dicha sociedad le tiene conferido en escritura pública otorgada el [FECHA] ante el Notario de [LOCALIDAD] D./Dña. [NOMBRE Y APELLIDOS] con el número [NÚMERO] de su protocolo. Inscrita en [DATOS REGISTRALES], de nacionalidad española, es designada en adelante en este documento como LA PARTE PROMITENTE ARRENDADORA.

El segundo, en su propio nombre y derecho, y será designado en el presente contrato como LA PARTE PROMITENTE ARRENDATARIA.

Reconociéndose mutuamente, según intervienen, plena capacidad legal para contratar y obligarse, de sus libres y espontáneas voluntades

DICEN

I.- Que LA PARTE PROMITENTE ARRENDADORA es dueña, en pleno dominio y sin limitación alguna, del local comercial cuya descripción es la siguiente, en adelante denominado EL LOCAL:

[DESCRIPCIÓN DEL BIEN]

II.- Que en la actualidad, EL LOCAL se halla arrendado a la entidad [DENOMINACIÓN SOCIAL], finalizando esta relación arrendaticia el próximo día [FECHA].

III.- Que LA PARTE PROMITENTE ARRENDADORA está interesada en arrendar EL LOCAL a partir de la fecha en que pueda ser ocupado, una vez extinguido el contrato indicado en el anterior Expositivo II, y LA PARTE PROMITENTE ARRENDATARIA en concertar dicho arrendamiento, estando ambas partes de acuerdo en las condiciones esenciales y necesarias para la perfección del futuro contrato, que se relacionarán en la cláusula TERCERA del presente contrato.

Y de conformidad con lo precedente, los comparecientes convienen en otorgar el presente contrato de promesa de arrendamiento con arreglo a las siguientes

CLÁUSULAS

PRIMERA.- LA PARTE PROMITENTE ARRENDADORA se compromete a arrendar en su día EL LOCAL descrito en el Expositivo I a LA PARTE PROMITENTE ARRENDATARIA quien a su vez se obliga a perfeccionar el pretendido contrato de arrendamiento.

SEGUNDA.- La PARTE PROMITENTE ARRENDADORA se obliga ante LA PARTE PROMITENTE ARRENDATARIA a no arrendar EL LOCAL a un tercero, hasta la perfección del futuro contrato de arrendamiento.

TERCERA.- Las condiciones esenciales de dicha futura relación arrendaticia son las siguientes:

ENTRADA EN VIGOR: [FECHA].

OBJETO DEL CONTRATO: EL LOCAL

RENTA MENSUAL: [IMPORTE] € ( euros)

ACTUALIZACIÓN DE LA RENTA: Cada 1 de enero según IPC

FORMA DE PAGO: [MEDIO DE PAGO].

DURACIÓN: años.

CONSERVACIÓN Y REPARACIÓN: De conformidad a la Ley de Arrendamientos Urbanos

FIANZA: Dos mensualidades

CUARTA.- En el presente acto, LA PARTE PROMITENTE ARRENDATARIA. entrega a LA PARTE PROMITENTE ARRENDADORA la cantidad de [IMPORTE] € ( euros) en concepto garantía de la reserva de EL LOCAL, con la predeterminación de su ulterior destino o aplicación a fianza legal en el momento de la firma del contrato y la correlativa devolución por LA PARTE PROMITENTE ARRENDADORA de no llegarse éste a suscribir por causas a ella imputable sin derecho a ninguna otra reclamación.

QUINTA.- El plazo de validez de la promesa de arrendamiento se fija hasta el día [FECHA] Si transcurrido el indicado plazo las partes no han llegado a suscribir el citado arrendamiento, salvo prórroga expresa por mutuo acuerdo, el presente contrato quedará sin valor ni efecto a partir de ese momento, debiendo LA PARTE PROMITENTE ARRENDADORA devolver a LA PARTE PROMITENTE ARRENDATARIA la cantidad íntegra entregada en virtud de la cláusula CUARTA anterior, y quedando LA PARTE PROMITENTE ARRENDADORA libre para negociar con cualquier tercero.

Firma de EL/LA ARRENDADOR/A:

Firma de LA ARRENDATARIA
D./Dña. [NOMBRE Y APELLIDOS] D./Dña. [NOMBRE Y APELLIDOS]

========================================================================
