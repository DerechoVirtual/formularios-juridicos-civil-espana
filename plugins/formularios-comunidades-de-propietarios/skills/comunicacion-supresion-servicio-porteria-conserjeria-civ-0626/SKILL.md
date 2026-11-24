---
name: comunicacion-supresion-servicio-porteria-conserjeria-civ-0626
description: "Comunicación de supresión del servicio de portería o conserjería. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Comunicación de supresión del servicio de portería o conserjería

> Formulario **CIV-0626** del plugin **Comunidades de propietarios** (`formularios-comunidades-de-propietarios`) · Civil › Propiedad horizontal · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Comunicación de supresión del servicio de portería o conserjería» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Comunicación de supresión del servicio de portería o conserjería” para mi caso». También puedes invocarla directamente con `/formularios-comunidades-de-propietarios:comunicacion-supresion-servicio-porteria-conserjeria-civ-0626`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-comunidades-de-propietarios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Comunidades de propietarios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (6 veces)
- [ ] AÑO (4 veces)
- [ ] DÍA (4 veces)
- [ ] MES (4 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] CALLE
- [ ] ENTIDAD BANCARIA
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] Nº
- [ ] NÚMERO
- [ ] SERIE

## Normas que cita el formulario

- art. 53.1.a Real Decreto Legislativo 1/1995
- art. 53.1.c ET

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

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Muy Sr/Sra. Mío/Mía,

Me dirijo a Vd. en mi condición de Presidente de la Comunidad de Propietarios del edificio sito en [LOCALIDAD], calle [CALLE] nº [NÚMERO], para comunicarle que esta Comunidad ha acordado en Junta celebrada el pasado día [DÍA] de [MES] de [AÑO], por mayoría superior a tres quintas partes del total de los propietarios y que a su vez representan las tres quintas partes de las cuotas de participación, la supresión del servicio de portería, todo ello al amparo del artículo 17.3 párrafo 1º.

Al hilo de lo anterior atendiendo a lo dispuesto en el artículo 53.1.a) del Real Decreto Legislativo 1/1995, de 24 de marzo, por el que se aprueba el Texto Refundido de la Ley del Estatuto de los Trabajadores, le comunico la extinción de su contrato de trabajo en virtud de lo contemplado en el art. 52.c) del estatuto de los Trabajadores, por las causas económicas y técnicas que a continuación se detallan:

I.- El excesivo coste económico que para esta Comunidad supone afrontar su retribución salarial y hacer frente a las cargas sociales correspondientes, que representa un coste total de [IMPORTE] €, correspondientes a su salario: [IMPORTE] € y contribución empresarial a la Seguridad Social: [IMPORTE] €.

II.- La instalación de un sistema de vídeo portero automático.

III.- La contratación de los servicios de limpieza y mantenimiento con una empresa de servicios, con un coste anual de [IMPORTE] €, lo que representa para la Comunidad un ahorro anual de [IMPORTE] €.

En consecuencia se procede a amortizar su puesto de trabajo con efectos a día [DÍA] de [MES] de [AÑO], poniendo a su disposición desde ese mismo día un cheque nominativo del Banco [ENTIDAD BANCARIA], nº [Nº] de serie [SERIE], la cantidad de [IMPORTE] € correspondiente a la indemnización de veinte días por año de servicio, prorrateándose por meses los períodos de tiempo inferiores a un año y con un máximo de doce mensualidades, conforme establece el art. 53.1.b) del Estatuto de los Trabajadores.

Asimismo, se le informa que durante el plazo de treinta días de preaviso, se le concede en virtud del artículo 53.1.c) del ET, una licencia de seis horas semanales con el fin de buscar nuevo empleo, sin pérdida de su retribución.

A la mayor brevedad posible le será remitida toda la documentación necesaria para realizar las gestiones tendentes a la percepción de la prestación por desempleo u otras que sean precisas.

Agradeciéndole sinceramente los servicios prestados, se despide atentamente,

Fdo.- D [NOMBRE Y APELLIDOS]

Presidente de la Comunidad de Propietarios

ACUSE DE RECIBO

Recibido el [DÍA] de [MES] de [AÑO]

Fdo. D. [NOMBRE Y APELLIDOS]

========================================================================
