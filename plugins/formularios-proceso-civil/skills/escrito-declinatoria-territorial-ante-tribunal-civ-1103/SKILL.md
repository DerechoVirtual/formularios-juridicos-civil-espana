---
name: escrito-declinatoria-territorial-ante-tribunal-civ-1103
description: "Escrito de declinatoria territorial ante el tribunal del domicilio del demandado (juicio verbal). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito de declinatoria territorial ante el tribunal del domicilio del demandado (juicio verbal)

> Formulario **CIV-1103** del plugin **Proceso civil: demandas, contestaciones, prueba y vista** (`formularios-proceso-civil`) · Civil › Escritos procesales (demanda, contestación, prueba, vista) · normativa revisada el 24-11-2026.

## Qué es

Escrito interponiendo cuestión de competencia territorial por declinatoria ante el Tribunal del lugar del demandado, en autos de Juicio Verbal.

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito de declinatoria territorial ante el tribunal del domicilio del demandado (juicio verbal)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito de declinatoria territorial ante el tribunal del domicilio del demandado (juicio verbal)” para mi caso». También puedes invocarla directamente con `/formularios-proceso-civil:escrito-declinatoria-territorial-ante-tribunal-civ-1103`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-proceso-civil:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Proceso civil: demandas, contestaciones, prueba y vista) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NÚMERO (4 veces)
- [ ] SEDE (4 veces)
- [ ] AÑO (3 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] CALLE (2 veces)
- [ ] FECHA (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] Nº DE PROCEDIMIENTO (2 veces)
- [ ] ENTIDAD BANCARIA
- [ ] LUGAR
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] Nº

## Normas que cita el formulario

- art. 63.2 LEC
- art. 63.1 LEC
- art. 65 LEC
- art. 64.1 LEC
- art. 54.1 LEC
- art. 250.2 LEC
- art. 54.2 LEC
- art. 52.2 LEC

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

- Junto a «… n.º [NÚMERO]/[AÑO] que sigue el Tribunal de Instancia de [SEDE], plaza n.º [Nº]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

AL TRIBUNAL DE INSTANCIA DE [SEDE] Q.P.T.R.C.

D./Dña. [NOMBRE Y APELLIDOS], Procurador de los Tribunales y de [NOMBRE DEL REPRESENTADO/A] D./Dña. [NOMBRE Y APELLIDOS], según consta mediante el apoderamiento ‘apud acta’ otorgado en la Secretaría del Tribunal; dirigido el poderdante por la Letrado en ejercicio D./Dña. [NOMBRE Y APELLIDOS], colegiada n.º [NÚMERO], del Iltre. Colegio de [LOCALIDAD], con despacho abierto en [LOCALIDAD], calle [CALLE]; ante el Tribunal comparezco y como mejor proceda en derecho, DIGO:

Que en la representación que ostento, vengo a interponer cuestión de competencia territorial por Declinatoria en autos de Juicio Verbal n.º [NÚMERO]/[AÑO] que sigue el Tribunal de Instancia de [SEDE], plaza n.º [Nº] , en base a los siguientes

HECHOS

PRIMERO

Mediante decreto del Letrado de la Administración de Justicia de fecha [FECHA], en autos de juicio verbal n.º [Nº DE PROCEDIMIENTO]/[AÑO], de que conoce el Tribunal de Instancia n.ºde, instados por la entidad bancaria [ENTIDAD BANCARIA], mi principal ha sido emplazado frente a una acción personal por incumplimiento derivada de una póliza mercantil de préstamo al consumo para la adquisición de un vehículo de motor de segunda mano.

Se aporta copia del emplazamiento con la demanda y documentos acompañados, entre los que obra la citada póliza (documento n.º 1).

SEGUNDO

Como se desprende de la lectura de la cláusula octava de la póliza en cuestión, se introdujo por la entidad que la redactó una ‘sumisión’ expresa al fuero de los Tribunales de

TERCERO

Que el lugar de domicilio de mi mandante es el de esta ciudad. calle [CALLE] n.º [NÚMERO]

Se acompaña certificado de empadronamiento, con su antigüedad, como documento n.º [NÚMERO].

FUNDAMENTOS DE DERECHO

I.- El presente escrito se presenta ante el Tribunal del domicilio del demandado, conforme a la prevención del art. 63.2 ‘in fine’ LEC, que ha de remitirse al día siguiente por oficio AL TRIBUNAL DE INSTANCIA DE [SEDE], que conoce de la demanda, sin perjuicio de comunicarlo por el medio más rápido posible de forma inmediata.

II.- Conforme a lo dispuesto en el art. 63.1 LEC, mi mandante está legitimado para proponer esta cuestión de competencia, puesto que es el demandado en el proceso principal.

III.- Procede, como cauce procesal, la presente declinatoria, según trámite del art. 65 LEC, habida cuenta que es el único para denunciar la falta de competencia de todo tipo (art. 63.1, párrafo 2.º LEC).

IV.- El planteamiento de la declinatoria, dentro de los cinco primeros días posteriores a la citación para la vista, debe producir el efecto de suspender el curso del juicio verbal, como establece el art. 64.1 LEC.

V.- Si ya la jurisprudencia última venía sentando que la renuncia al fuero propio por la autorización legal de sumisión expresa tendría que tener en cuenta la facultad de declarar nula la cláusula abusiva del contrato de adhesión, el caso es que el art. 54.1 ‘in fine’ LEC considera inválida la sumisión expresa o tácita en los asuntos que deban decidirse por el juicio verbal.

Y si se interpretara que la referencia legal es a los juicios verbales por la materia, y no a los que la cuantía asigna trámite ex art. 250.2 LEC, de todas formas, el art. 54.2 LEC invalida la sumisión expresa contenida en contratos de adhesión, o que contengan condiciones generales impuestas por una de las partes, o que se hayan celebrado con consumidores y usuarios.

VI.- Conforme al art. 52.2 LEC hay regla imperativa de competencia territorial en materia de contratos destinados a financiación de bienes muebles, conforme a la que es competente el tribunal del domicilio del prestatario, al cual se designa en cumplimiento del art. 63.1, párrafo 2.º LEC.

Por lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito con sus copias, admita uno y otras, y haberme por comparecido en la representación que ostento, ordenando se entiendan conmigo las diligencias y notificaciones que procedan, se sirva remitirpor el medio de comunicación más rápido posible la presente declinatoria al Tribunal de Instancia de [SEDE], sin perjuicio de remitírsele por oficio el día de mañana, a fin de que se tenga por promovida cuestión de competencia territorial, se suspenda el curso del Juicio Verbal n.º [Nº DE PROCEDIMIENTO]/[AÑO] de referencia, y en definitiva, se produzca la inhibición a favor de estos Tribunales de Instancia, con emplazamiento de las partes ante los mismos, haciendo expresa condena en costas procesales a quien se opusiera a tal pretensión.

Es justicia de hacerse en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a

========================================================================
