---
name: reposicion-ejecutante-contra-sobreseimiento-ejecucion-civ-1393
description: "Reposición del ejecutante contra el sobreseimiento de la ejecución provisional por revocación. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Reposición del ejecutante contra el sobreseimiento de la ejecución provisional por revocación

> Formulario **CIV-1393** del plugin **Recursos civiles: reposición, apelación, casación y queja** (`formularios-recursos-civiles`) · Civil › Recursos · normativa revisada el 24-11-2026.

## Qué es

Recurso de reposición del ejecutante contra el auto que se sobresee la ejecución provisional al existir sentencia revocatoria de la condena dineraria.

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Reposición del ejecutante contra el sobreseimiento de la ejecución provisional por revocación» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Reposición del ejecutante contra el sobreseimiento de la ejecución provisional por revocación” para mi caso». También puedes invocarla directamente con `/formularios-recursos-civiles:reposicion-ejecutante-contra-sobreseimiento-ejecucion-civ-1393`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-recursos-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Recursos civiles: reposición, apelación, casación y queja) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (4 veces)
- [ ] IMPORTE (3 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] APELLIDOS
- [ ] AÑO
- [ ] DENOMINACIÓN SOCIAL
- [ ] LUGAR
- [ ] NÚMERO
- [ ] SECCIÓN
- [ ] SEDE

## Normas que cita el formulario

- art. 533 LEC
- art. 497.2 LEC
- art. 477.2 LEC
- art. 535.2 LEC
- art. 533.1 LEC

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a. de los Tribunales y de D./Dña. [NOMBRE Y APELLIDOS], ejecutante cuyas demás circunstancias ya constan en la pieza separada de ejecución provisional de autos de juicio ordinario n.º [NÚMERO]/[AÑO], comparezco, y como mejor en Derecho proceda, DIGO:

Que con fecha [FECHA] se nos ha notificado decreto por el que se sobresee la ejecución provisional promovida por esta parte, y se le requiere la devolución de la cantidad de [IMPORTE] xx [IMPORTE] euros, a la vez que se ordena la tasación de costas, y concede trámite a petición de la sociedad ejecutada de resarcimiento de daños y perjuicios.

Que dentro del plazo de los cinco días siguientes a la notificación, se formula RECURSO DE REPOSICIÓN contra el indicado auto de [FECHA], expresando haber infringido, a juicio de esta parte, el art. 533 LEC, en base a las siguientes:

ALEGACIONES

PRIMERA.- Inexistencia actual de resolución revocatoria

El art. 533 LEC resulta aplicable a partir de la constancia en el proceso de una revocación del pronunciamiento de condena dineraria que se ejecuta provisionalmente, y la ejecutada RR SEGUROS Y REASEGUROS [DENOMINACIÓN SOCIAL], S.A., únicamente aporta testimonio de la sentencia dictada por la Sección [SECCIÓN] de la Audiencia Provincial, que esta parte también conoce, pero la que no se acredita haber sido notificada al codemandado, asegurado de la adversa, D./Dña. [NOMBRE Y APELLIDOS] ROGELIO [APELLIDOS], en situación de rebeldía procesal, por lo que, sin estar legalmente notificada a todas las partes, conforme al art. 497.2 LEC, la sentencia carece de eficacia jurídica, no siendo ni ejecutiva ni ejecutoria.

SEGUNDA.- Ausencia de firmeza de la revocación

El mismo art. 533 LEC distingue, en orden a los efectos sobre la ejecución provisional, que la sentencia revocatoria sea o no firme.

Pues bien, ante la sentencia de la Audiencia Provincial ha sido interpuesto recurso de casación por motivo de tener la resolución interés casacional del art. 477.2 LEC, que está pendiente de resolver, como se demuestra con testimonio del escrito de interposición y copia de la diligencia de ordenación de la Secretaría de la Sección respectiva que lo deja en la mesa del Magistrado ponente, que acompañan al presente escrito.

En consecuencia, hasta que no conste que la Audiencia Provincial tiene por interpuesto el recurso de casación, por analogía a lo que ocurre cuando la ejecución provisional es de una condena en segunda instancia (art. 535.2 LEC), no se podrá conocer si procede una devolución provisional o definitiva.

TERCERA.- Pluspetición

Con independencia de contestar al traslado por la solicitud de fijación de daños y perjuicios ocasionados por la ejecución provisional, tiene que censurarse igualmente que el art. 533.1 LEC previene el reintegro de las costas de la ejecución provisional que el ejecutado hubiese satisfecho, y no cualesquiera costas procesales, siendo que la aseguradora ejecutada no ha satisfecho cantidad alguna por costas de la ejecución provisional, que adeuda por su imposición legal y por la condena decretada en el auto que zanjó la oposición al embargo.

CUARTA.- Requisito de admisibilidad del recurso

Se acompaña a este escrito justificante acreditativo del depósito efectuado por importe de [IMPORTE] euros, en la cuenta de depósitos y consignaciones del Tribunal, conforme dispone la DA 15.ª LOPJ.

Por lo expuesto,

SUPLICO AL Letrado de la Administración de Justicia que,

teniendo por presentado este escrito, con los documentos anejos, resguardo acreditativo del pago del depósito, y justificante de haber efectuado el traslado al Procurador/a. de la contraparte, se sirva admitir el Recurso de Reposición frente al decreto de fecha [FECHA], y previo su regular trámite, se acuerde haber lugar a reponer, dejando sin efecto el sobreseimiento de la ejecución provisional, y requerimientos y traslados efectuados a mi mandante, con lo demás que resulte procedente en Justicia de hacerse en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a

========================================================================
