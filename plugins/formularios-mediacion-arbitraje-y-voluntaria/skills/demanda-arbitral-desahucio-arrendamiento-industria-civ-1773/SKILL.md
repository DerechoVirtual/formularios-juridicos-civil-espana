---
name: demanda-arbitral-desahucio-arrendamiento-industria-civ-1773
description: "Demanda arbitral de desahucio de un arrendamiento de industria. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda arbitral de desahucio de un arrendamiento de industria

> Formulario **CIV-1773** del plugin **Mediación, MASC, arbitraje y jurisdicción voluntaria** (`formularios-mediacion-arbitraje-y-voluntaria`) · Civil › Jurisdicción voluntaria, MASC, mediación y arbitraje · normativa revisada el 24-11-2026.

## Qué es

Demanda arbitral que presenta el arrendador ante una corte arbitral, en virtud de convenio arbitral incluido en el contrato, para solicitar la resolución de un contrato de arrendamiento de industria por impago de rentas, el desalojo de la finca y el pago de las cantidades adeudadas.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda arbitral de desahucio de un arrendamiento de industria» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda arbitral de desahucio de un arrendamiento de industria” para mi caso». También puedes invocarla directamente con `/formularios-mediacion-arbitraje-y-voluntaria:demanda-arbitral-desahucio-arrendamiento-industria-civ-1773`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-mediacion-arbitraje-y-voluntaria:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Mediación, MASC, arbitraje y jurisdicción voluntaria) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] DENOMINACIÓN DE LA CORTE ARBITRAL (7 veces)
- [ ] FECHA (4 veces)
- [ ] IMPORTE (3 veces)
- [ ] Nº DE PACTO (3 veces)
- [ ] DOMICILIO (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NOMBRE Y APELLIDOS O DENOMINACIÓN SOCIAL DEL DEMANDADO (2 veces)
- [ ] Nº DE CLÁUSULA (2 veces)
- [ ] AÑO
- [ ] CAUSA
- [ ] CORREO ELECTRÓNICO
- [ ] DATOS REGISTRALES
- [ ] DNI/NIE
- [ ] DOMICILIO DE LA FINCA
- [ ] DÍA
- [ ] FOLIO
- [ ] LIBRO
- [ ] MES
- [ ] MES Y AÑO
- [ ] NOMBRE Y APELLIDOS DEL DEMANDANTE
- [ ] NOMBRE Y APELLIDOS O DENOMINACIÓN SOCIAL
- [ ] Nº
- [ ] POLÍGONO
- [ ] REGISTRO
- [ ] TOMO
- [ ] TRANSCRIPCIÓN LITERAL DE LA CLÁUSULA ARBITRAL

## Normas que cita el formulario

- art. 9 Ley 60/2003
- art. 27.2.a Ley 29/1994
- art. 1108 Código Civil

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

A LA CORTE ARBITRAL DE [DENOMINACIÓN DE LA CORTE ARBITRAL]

Don/Doña [NOMBRE Y APELLIDOS DEL DEMANDANTE], con DNI [DNI/NIE], con domicilio en [DOMICILIO] (correo electrónico [CORREO ELECTRÓNICO]), el cual se designa a efectos de notificaciones, ante la Secretaría de la Corte de Arbitraje de [DENOMINACIÓN DE LA CORTE ARBITRAL], comparezco en nombre propio y, como mejor proceda en Derecho, DIGO:

1) Que en la cláusula [Nº DE CLÁUSULA] del contrato de arrendamiento de fecha [FECHA], suscrito con [NOMBRE Y APELLIDOS O DENOMINACIÓN SOCIAL DEL DEMANDADO] sobre la finca sita en [DOMICILIO DE LA FINCA], las partes someten a arbitraje todas las controversias que puedan surgir derivadas del incumplimiento del contrato de arrendamiento, encomendándose la administración del arbitraje y la designación de árbitros a la Corte Arbitral de [DENOMINACIÓN DE LA CORTE ARBITRAL], tal como se acredita mediante copia del documento suscrito, que se acompaña como DOCUMENTO Nº 1.

2) Que, al amparo de dicha cláusula, mediante el presente escrito formulo DEMANDA ARBITRAL contra [NOMBRE Y APELLIDOS O DENOMINACIÓN SOCIAL DEL DEMANDADO], con domicilio en [DOMICILIO], en solicitud de la resolución del contrato de arrendamiento de industria concertado en fecha [FECHA] [ELEGIR: por falta de pago de la renta / por expiración del plazo contractual / por otra causa: [CAUSA]].

La demanda arbitral que inicio mediante este escrito se funda en los siguientes

HECHOS

PRIMERO.– El demandante es propietario de la finca urbana sita en [LOCALIDAD], en el polígono industrial de [POLÍGONO], núm. [Nº], inscrita en el Registro de la Propiedad de [REGISTRO], Libro [LIBRO], Tomo [TOMO], Folio [FOLIO] (se adjunta copia de la escritura pública como DOCUMENTO Nº 2) [DATOS REGISTRALES].

SEGUNDO.– La citada finca fue cedida en arrendamiento para el ejercicio de actividad industrial por el demandante al demandado Don/Doña [NOMBRE Y APELLIDOS O DENOMINACIÓN SOCIAL] en virtud de contrato de fecha [FECHA], el cual ha sido aportado como DOCUMENTO Nº 1 de esta demanda, en el que se pactó una renta mensual de [IMPORTE] euros, actualizable anualmente en los términos que resultan de la cláusula [Nº DE CLÁUSULA] del contrato, siendo la renta actualmente vigente la de [IMPORTE] euros mensuales.

Conforme al pacto [Nº DE PACTO] del contrato, la renta es pagadera por meses anticipados, por lo que el demandante pasa al cobro los recibos en la cuenta corriente de la entidad bancaria designada por el arrendatario, dentro de los cinco primeros días de cada mes.

En el pacto [Nº DE PACTO] del contrato las partes convinieron someter la resolución de controversias a arbitraje, encomendándose la administración del arbitraje y la designación de árbitros a la Corte Arbitral de [DENOMINACIÓN DE LA CORTE ARBITRAL], siendo la cláusula del siguiente tenor literal: «[TRANSCRIPCIÓN LITERAL DE LA CLÁUSULA ARBITRAL]».

TERCERO.– Que desde el mes de [MES Y AÑO] la entidad bancaria ha devuelto impagados los recibos pasados al cobro por el demandante, tal como consta al dorso de los mismos, al parecer y según manifestación de la entidad bancaria, por [MOTIVO DE LA DEVOLUCIÓN: por ejemplo, falta de disponibilidad en la cuenta corriente / indicación expresa de su cliente].

Ante dicho incumplimiento, el demandante requirió por carta certificada al demandado en los términos que resultan del documento que se acompaña, apercibiéndole de que, de no proceder al abono de las rentas adeudadas, se formularía demanda arbitral ejercitando la acción de resolución del contrato, sin que hasta el momento de interponer la demanda se haya avenido a cumplir con la obligación pactada (se acompaña dicha carta como DOCUMENTO Nº 3).

A los anteriores hechos les son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

Capacidad y legitimación

Se dan los requisitos de legitimación activa y pasiva.

Competencia

Corresponde la competencia para conocer de la demanda a la Corte Arbitral a la que me dirijo en virtud del pacto de sumisión de las partes, habiendo convenido la sumisión de la controversia a arbitraje por convenio que cumple lo establecido en el artículo 9 de la Ley 60/2003, de 23 de diciembre, de Arbitraje, encomendando la administración del arbitraje a la Corte Arbitral de [DENOMINACIÓN DE LA CORTE ARBITRAL], conforme autoriza el artículo 14 de la misma ley.

Procedimiento

Es de aplicación el reglamento de la Corte Arbitral de [DENOMINACIÓN DE LA CORTE ARBITRAL], debiendo designarse un único árbitro que resolverá en Derecho, de acuerdo con el contenido del convenio arbitral recogido en el pacto número [Nº DE PACTO] del contrato.

Acción y pretensión

La pretensión que se ejercita queda amparada en el artículo 35 en relación con el artículo 27.2.a) de la Ley 29/1994, de 24 de noviembre, de Arrendamientos Urbanos, debiendo resolverse el contrato con las consecuencias derivadas del incumplimiento, que son el desalojo del inmueble y el pago de las cantidades debidas por el arrendatario en concepto de indemnización de daños y perjuicios, con más los intereses correspondientes, según dispone el artículo 1108 del Código Civil.

Dicha pretensión es procedente por incumplimiento de la obligación de pago del arrendatario, incluso en el caso de que se pague después de presentada esta demanda, tal como es doctrina jurisprudencial reiterada en las sentencias del Tribunal Supremo, Sala Primera, de 24 de julio de 2008 (recurso 508/2002) y de 26 de marzo de 2009 (recurso 1507/2004), entre otras.

Costas y gastos

Con arreglo a lo establecido en el artículo 37.6 de la Ley de Arbitraje, deben imponerse todas las costas y gastos derivados del arbitraje al demandado.

En virtud de lo expuesto, es de justicia y por ello

SOLICITA A LA CORTE ARBITRAL DE [DENOMINACIÓN DE LA CORTE ARBITRAL]: que tenga por formulada esta demanda, con sus copias, proceda al nombramiento de árbitro conforme al reglamento de la Corte y, tras los trámites correspondientes y de conformidad con lo expuesto en este escrito, dicte laudo declarando la resolución del contrato de arrendamiento de fecha [FECHA] por incumplimiento del demandado al no haber satisfecho la renta arrendaticia, condenándole:

1) Al desalojo de la finca arrendada, dejando la finca a disposición del arrendador.

2) A que indemnice al actor en la cantidad de [IMPORTE] euros, más los intereses legales, en concepto de rentas impagadas.

3) Al pago de todas las costas y gastos de este procedimiento.

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del demandante:
