---
name: demanda-arbitral-materia-transporte-civ-1770
description: "Demanda arbitral en materia de transporte. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda arbitral en materia de transporte

> Formulario **CIV-1770** del plugin **Mediación, MASC, arbitraje y jurisdicción voluntaria** (`formularios-mediacion-arbitraje-y-voluntaria`) · Civil › Jurisdicción voluntaria, MASC, mediación y arbitraje · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda arbitral en materia de transporte» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda arbitral en materia de transporte” para mi caso». También puedes invocarla directamente con `/formularios-mediacion-arbitraje-y-voluntaria:demanda-arbitral-materia-transporte-civ-1770`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-mediacion-arbitraje-y-voluntaria:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Mediación, MASC, arbitraje y jurisdicción voluntaria) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (5 veces)
- [ ] FECHA (4 veces)
- [ ] IMPORTE (4 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] AÑO
- [ ] CALLE
- [ ] DESCRIBIR
- [ ] DNI/NIE
- [ ] DÍA
- [ ] LOCALIDAD DE DESTINO
- [ ] LOCALIDAD DE ORIGEN
- [ ] LUGAR
- [ ] MES
- [ ] Nº DE PROCEDIMIENTO
- [ ] PARTE DEMANDADA

## Normas que cita el formulario

- art. 38 Ley 16/1987
- art. 1.101 Código Civil
- art. 1.107 Código Civil

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

Procedimiento arbitral número

A LA JUNTA ARBITRAL DE [LOCALIDAD]

D./Dª [NOMBRE Y APELLIDOS], con D.N.I. [DNI/NIE], con domicilio en calle [CALLE] de [LOCALIDAD], el cual se designa a efectos de notificaciones, ante la Secretaría de la Junta Arbitral de [LOCALIDAD] comparezco en nombre propio y como mejor proceda en derecho DIGO:

Que habiéndose conferido traslado para que deduzca demanda en el procedimiento arbitral número [Nº DE PROCEDIMIENTO], mediante el presente escrito formulo DEMANDA ARBITRAL contra [PARTE DEMANDADA] con domicilio en [LOCALIDAD], en solicitud de [FECHA] indemnización de daños y perjuicios derivados del incumplimiento contrato de transporte terrestre de fecha [FECHA],

La demanda arbitral que inicio mediante este escrito se funda en los siguientes

HECHOS

PRIMERO.- El pasado día [FECHA], el demandante concertó con el demandado D. [NOMBRE Y APELLIDOS], contrato de transporte terrestre con el objeto de trasladar las mercancías consistentes en [DESCRIBIR] por carretera desde [LOCALIDAD DE ORIGEN] hasta [LOCALIDAD DE DESTINO], fijando un precio de [IMPORTE] euros, y teniendo las mercancías trasladadas un valor declarado de [IMPORTE] euros.

SEGUNDO.- El día [FECHA] se llevó a cabo el transporte por la empresa del demandado, llegando la mercancía a su destino deteriorada y en estado inservible.

El motivo por el cual pereció la mercancía es que el embalaje interior en el transporte fue manifiestamente insuficiente, al no reunir las condiciones necesarias para la conservación los camiones propiedad del demandado, tal como consta en el informe emitido por el perito D. [NOMBRE Y APELLIDOS] que acompaño como documento número

TERCERO.- Ante la imposibilidad de alcanzar acuerdo amistoso y habiendo convenido las partes someter la controversia ante esa Junta Arbitral, por medio del presente escrito se formula reclamación a fin de que el demandado indemnice al solicitante en la cantidad de [IMPORTE] euros, importe del valor de la mercancía perecida al no reunir el embalaje los requisitos necesarios para efectuar el transporte de este tipo de mercancía.

A los anteriores hechos le son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

Capacidad y legitimación

Se dan los requisitos de legitimación activa y pasiva

Competencia

Corresponde la competencia para conocer de demanda a la Junta Arbitral a que me dirijo en virtud de lo previsto en el art. 38 de la Ley 16/1987 de Ordenación de los Transportes Terrestres y en el art. 6 de su Reglamento. En cuanto al límite de cuantía no resulta aplicable en el presente caso ya que existe cláusula de sometimiento expreso a las Juntas Arbitrales, firmada por ambas partes.

Procedimiento

Es de aplicación la Ley y Reglamento antes expresados y, supletoriamente, las disposiciones de la Ley de Arbitraje.

Acción y pretensión

La pretensión que se ejercita queda amparada en los artículos 355, 361, 362 y 363 todos ellos del Código de Comercio que determinan la responsabilidad y obligaciones del transportista, en el artículo 1.101 del Código Civil que establece la responsabilidad contractual de indemnizar los daños y perjuicios ocasionados, y en el art. 1.107 del Código Civil en virtud del cual los daños y perjuicios de que responda el deudor han de ser consecuencia necesaria de su falta de cumplimiento.

Costas y gastos

Con arreglo a lo establecido en el art. 37.6 de la Ley de Arbitraje, deben imponerse todas las costas y gastos derivados del arbitraje al demandado.

En virtud de lo expuesto, es de justicia y por ello

SOLICITA A LA JUNTA ARBITRAL DE [LOCALIDAD] que tenga por formulada esta demanda, con sus copias y, tras los trámites correspondientes y de conformidad a lo expuesto en este escrito, dicte laudo condenado al transportista demandado a que indemnice al actor en la suma de [IMPORTE] Euros en concepto de daños y perjuicios producidos a la mercancía directamente derivados del incumplimiento denunciado, así como al pago de todas las costas y gastos de este procedimiento

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma del demandante

========================================================================
