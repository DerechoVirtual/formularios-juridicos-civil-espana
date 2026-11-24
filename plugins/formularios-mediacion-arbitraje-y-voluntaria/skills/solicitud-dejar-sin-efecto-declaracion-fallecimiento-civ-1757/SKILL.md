---
name: solicitud-dejar-sin-efecto-declaracion-fallecimiento-civ-1757
description: "Solicitud para dejar sin efecto la declaración de fallecimiento. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud para dejar sin efecto la declaración de fallecimiento

> Formulario **CIV-1757** del plugin **Mediación, MASC, arbitraje y jurisdicción voluntaria** (`formularios-mediacion-arbitraje-y-voluntaria`) · Civil › Jurisdicción voluntaria, MASC, mediación y arbitraje · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud para dejar sin efecto la declaración de fallecimiento» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud para dejar sin efecto la declaración de fallecimiento” para mi caso». También puedes invocarla directamente con `/formularios-mediacion-arbitraje-y-voluntaria:solicitud-dejar-sin-efecto-declaracion-fallecimiento-civ-1757`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-mediacion-arbitraje-y-voluntaria:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Mediación, MASC, arbitraje y jurisdicción voluntaria) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] AÑO (7 veces)
- [ ] DÍA (6 veces)
- [ ] LOCALIDAD (6 veces)
- [ ] MES (6 veces)
- [ ] CALLE
- [ ] COLEGIO
- [ ] FECHA
- [ ] LUGAR
- [ ] Nº
- [ ] Nº DE DOCUMENTO
- [ ] Nº DE PROCEDIMIENTO
- [ ] NÚMERO
- [ ] PROFESIÓN
- [ ] PÁGINA
- [ ] SEDE
- [ ] TOMO

## Normas que cita el formulario

- art. 197 Código Civil
- art. 75.1 LJV

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

D./Dª [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, en nombre y representación de D./Dª [NOMBRE Y APELLIDOS], mayor de edad, de profesión [PROFESIÓN], con domicilio en [LOCALIDAD], calle [CALLE], nº [NÚMERO], pta., según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño a este escrito, comparezco en este TRIBUNAL con la asistencia del Letrado D./D [NOMBRE Y APELLIDOS], del Ilustre Colegio de Abogados de [COLEGIO], y DIGO:

Que por medio del presente escrito y en la representación que ostento, me persono en el procedimiento de declaración de fallecimiento de mi representado, autos núm. [Nº DE PROCEDIMIENTO]/[AÑO], en solicitud de la REVOCACIÓN del decreto de fecha [DÍA] de [MES] de [AÑO], dictado por este Tribunal, por el que se le declara fallecido.

Esta solicitud se basa en los siguientes

HECHOS:

PRIMERO Mi representado, D./Dª [NOMBRE Y APELLIDOS], hijo de D. [NOMBRE Y APELLIDOS] y de Dª [NOMBRE Y APELLIDOS], nació en [LOCALIDAD] el día [DÍA] de [MES] de [AÑO], encontrándose su nacimiento inscrito en el Registro Civil de [LOCALIDAD], al Tomo [TOMO], Página [PÁGINA], tal y como se acredita mediante certificación expedida por el encargado de dicho Registro, que se acompaña como Documento nº [Nº DE DOCUMENTO] y DNI del mismo.

Su identidad y persona coincide pues con la del declarado fallecido por el auto de fecha [DÍA] de [MES] de [AÑO], dictado por este Tribunal.

SEGUNDO Mi representado se encontraba, por razones laborales, en [LOCALIDAD] en fecha [DÍA] de [MES] de [AÑO], cuando se produjo el tsunami que arrasó aquella zona y al que, por su gravedad, se dio un eco notable en los medios de comunicación. Tras dicho siniestro, no hubo noticias de mi representado en su ámbito cercano durante un plazo de [Nº] meses (o años), lo que dio lugar a que, a instancias de su cónyuge (o lo que proceda), se declarase su fallecimiento por este Tribunal en el auto antes citado, dándose lugar a la apertura de su sucesión mortis causa conforme a lo establecido en el artículo 196 del Código civil.

TERCERO Dado que mi representado está vivo, una vez confirmada su identidad, a cuyo efecto comparecerá ante el Letrado de la Administración de Justicia el día y hora que se señale, conforme dispone el art. 75.1 de la Ley de Jurisdicción Voluntaria, procede dejar sin efecto el auto de declaración de fallecimiento, con aplicación inmediata de lo dispuesto en el artículo 197 del Código Civil.

Son aplicables a los referidos hechos los siguientes.

FUNDAMENTOS DE DERECHO

PRIMERO. COMPETENCIA.-

Es competente el Letrado de la Administración de Justicia del Tribunal al que me dirijo, por haber sido el que ha tramitado la declaración de fallecimiento de mi representado.

SEGUNDO. PROCEDIMIENTO.-

Debe seguirse en este asunto el procedimiento prevenido en el art. 75.1 de la Ley de Jurisdicción Voluntaria que establece: Si se presentare alguna persona que dijese ser el declarado ausente o fallecido, el Letrado de la Administración de Justicia ordenará que sea identificada por los medios adecuados que podrá acordar de oficio o a instancia del interesado, convocando comparecencia a la que serán citados la persona presentada, el Ministerio Fiscal y todos los que hubieren intervenido en el expediente de declaración.

TERCERO. REVOCACIÓN DE LA DECLARACIÓN DE FALLECIMIENTO.

El segundo párrafo del citado art. 75.1 LJV establece que, terminada la comparecencia, el Letrado de la Administración de Justicia dictará decreto dentro de los tres días siguientes por el que se dejará sin efecto la resolución de declaración de fallecimiento cuando, como en el caso, se constate sin duda la identidad del declarado fallecido.

CUARTO.- EFECTOS.

Resulta aplicable el artículo 197 del Código civil que dispone: Si después de la declaración de fallecimiento se presentase el ausente o se probase su existencia, recobrará sus bienes en el estado en que se encuentren y tendrá derecho al precio de los que se hubieran vendido, o a los bienes que con este precio se hayan adquirido, pero no podrá reclamar de sus sucesores rentas, frutos ni productos obtenidos con los bienes de su sucesión, sino desde el día de su presencia o de la declaración de no haber muerto”.

En virtud de lo expuesto,

SUPLICO AL TRIBUNAL: Que teniendo por presentado este escrito con los documentos que se acompañan y copia de todo ello lo admita, teniendo por solicitada por el Procurador que suscribe, en nombre y representación de D./Dª [NOMBRE Y APELLIDOS], la REVOCACIÓN del auto de este Tribunal de fecha [FECHA] de [LOCALIDAD] de [LOCALIDAD] por el que se declara el fallecimiento de D./Dª [NOMBRE Y APELLIDOS] y, en consecuencia, se deje sin efecto el mismo, ordenando en la misma resolución, conforme a lo dispuesto en el artículo 197 del Código civil, que se restituya a mi representado sus bienes en el estado en que se encuentren, y, en su caso, el precio de los que se hubieren vendido o los que se hayan subrogado en su lugar, así como los frutos y rentas de sus bienes desde el día [DÍA] de [MES] de [AÑO], en que los poseedores de tales bienes tuvieron noticia de hallarse vivo mi representado o, en su defecto, desde la fecha en que se les dio traslado de este escrito o desde la fecha de la declaración de no haber muerto aquél.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma y número del Letrado	Firma del Procurador

========================================================================
