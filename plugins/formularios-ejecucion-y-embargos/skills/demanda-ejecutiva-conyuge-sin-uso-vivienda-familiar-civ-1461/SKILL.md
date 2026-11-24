---
name: demanda-ejecutiva-conyuge-sin-uso-vivienda-familiar-civ-1461
description: "Demanda ejecutiva para que el cónyuge sin uso de la vivienda familiar arrendada la abandone. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda ejecutiva para que el cónyuge sin uso de la vivienda familiar arrendada la abandone

> Formulario **CIV-1461** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda ejecutiva para que el cónyuge sin uso de la vivienda familiar arrendada la abandone» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda ejecutiva para que el cónyuge sin uso de la vivienda familiar arrendada la abandone” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:demanda-ejecutiva-conyuge-sin-uso-vivienda-familiar-civ-1461`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] AÑO (8 veces)
- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] MES (6 veces)
- [ ] DÍA (5 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] CALLE (3 veces)
- [ ] Nº (3 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] COLEGIO
- [ ] FECHAS
- [ ] LUGAR
- [ ] SEDE

## Normas que cita el formulario

- art. 15 LAU
- art. 703.1.s LEC
- art. 703.3 LEC

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

### Avisos de actualización (3) — se aplican en el texto, nunca se copian en el documento

- Junto a «…Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).
- Junto a «…2666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.
- Junto a «…CIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA NÚMERO DE [LOCALIDAD]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº]

Procedimiento: /

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA NÚMERO DE [LOCALIDAD]

D./Dª [NOMBRE Y APELLIDOS], Procurador de los Tribunales, en nombre y representación de D./Dª [NOMBRE Y APELLIDOS], representación que tengo acreditada en autos, bajo la dirección técnica de D./Dª [NOMBRE Y APELLIDOS], Letrado del Ilustre Colegio de Abogados de [COLEGIO], ante el Tribunal comparezco y como mejor proceda en Derecho, DIGO:

Que por medio del presente escrito y siguiendo instrucciones expresas de mi representado/a, formulo DEMANDA EJECUTIVA contra D./Dª [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], calle [CALLE], nº [NÚMERO], pta., según el título ejecutivo que luego se dirá, en reclamación de las responsabilidades que se concretan en el suplico de esta demanda ejecutiva.

La demanda se interpone con base en los siguientes

HECHOS

TÍTULO EJECUTIVO: El título en que se funda la presente demanda es la SENTENCIA dictada en fecha [DÍA] de [MES] de [AÑO] en autos de separación (o de divorcio) seguidos ante este Tribunal con el número [Nº]/[AÑO], testimonio de la cual se acompaña como Documento nº [Nº DE DOCUMENTO]

PRESTACIÓN INCUMPLIDA.- En dicha sentencia se atribuyó el uso de la vivienda familiar, sita en [LOCALIDAD], calle [CALLE], nº [NÚMERO], pta., a mi representado/a y a los hijos comunes del matrimonio que quedaron bajo su guarda.

La citada vivienda es propiedad de D./Dª [NOMBRE Y APELLIDOS], que la cedió en arrendamiento al/a la demandado/a mediante contrato celebrado con el/la mismo/a en fecha [DÍA] de [MES] de [AÑO] Se acompaña copia del citado contrato como Documento nº [Nº DE DOCUMENTO]

Pese a que mi representado/a ha requerido, por vía extrajudicial, al/a la demandado/a en diversas ocasiones para que abandonase la vivienda, en cumplimiento de la sentencia cuya ejecución ahora se solicita, éste no ha atendido a tales requerimientos y continúa ocupando la misma. Se acompañan, como Documentos nos y [Nº DE DOCUMENTO], sendos burofaxes remitidos por mi representado/a al/a la demandado/a en fechas [FECHAS] de [MES] de [AÑO] y [DÍA] de [MES] de [AÑO], solicitándole que dejara libre la vivienda.

Por lo anterior, se solicita a este Tribunal que proceda a ejecutar la sentencia en que se atribuyó el uso de la vivienda familiar a mi mandante y requiera al/a la demandado/a para que abandone la misma y la deje a disposición de quien tiene derecho a su uso de acuerdo con la sentencia ejecutada.

En relación con lo anterior, procede que el Tribunal notifique a la arrendadora del inmueble, D./Dª [NOMBRE Y APELLIDOS], la atribución del uso de la vivienda, por sentencia judicial, a mi representado/a, de modo que continúe con éste/a la relación arrendaticia (para el caso de que el título por el que se posee la vivienda familiar sea el arrendamiento).

Los Hechos expuestos se basan en los siguientes

FUNDAMENTOS DE DERECHO

Es competente el Tribunal al que me dirijo, por ser el órgano judicial que conoció del asunto en primera instancia. Así resulta de los artículos 45, 61 y 545.1 de la Ley de Enjuiciamiento Civil.

La acción ejercitada mediante la presente demanda es la acción ejecutiva fundada en título que lleva aparejada ejecución, en este caso, una sentencia de condena firme, conforme al artículo 517. 1º y 2º de la Ley de Enjuiciamiento Civil.

Resulta aplicable el artículo 704.1 de la Ley de Enjuiciamiento Civil, que dispone: "Ocupantes de inmuebles que deban entregarse.

1. Cuando el inmueble cuya posesión se deba entregar fuera vivienda habitual del ejecutado o de quienes de él dependan, el Letrado de la Administración de Justicia les dará un plazo de un mes para desalojarlo. De existir motivo fundado, podrá prorrogarse dicho plazo un mes más.

Transcurridos los plazos señalados, se procederá de inmediato al lanzamiento, fijándose la fecha de éste en la resolución inicial o en la que acuerde la prórroga".

Dispone el artículo 776 de la Ley de Enjuiciamiento Civil que la ejecución forzosa de los pronunciamientos sobre medidas se sustanciará con arreglo a lo dispuesto en el Libro III de esa Ley, con las especialidades que el mismo precepto señala, lo que remite a los artículos 517 y ss y a los artículos 699 y ss., sobre ejecución no dineraria.

Corresponde la legitimación activa a mi representado/a en virtud del art. 538 y concordantes de la Ley de Enjuiciamiento Civil; y la pasiva al/a la demandado/a, conforme a los mismos preceptos.

Actúa el/la ejecutante representado/a por Procurador y bajo la dirección técnica de Letrado, tal y como exige el artículo 539 de la Ley de Enjuiciamiento Civil.

DERECHO SUSTANTIVO.- Resultan aplicables los artículos 90, 96 y concordantes del Código civil (en el caso de encontrarse sujetos los cónyuges, por razón de su vecindad civil, a algún Derecho autonómico, se citarán las normas correspondientes que regulen la atribución del uso de la vivienda habitual en los procesos de crisis matrimonial). Y el art. 15 LAU/1994.

Procede imponer las costas al/a la ejecutado/a conforme a lo establecido en los artículos 539.2 y 561 de la Ley de Enjuiciamiento Civil.

"Iura novit curia", y cuantos otros resulten de aplicación.

En virtud de lo expuesto:

SUPLICO AL TRIBUNAL: Que teniendo por presentado este escrito, con los documentos y copias que se acompañan, lo admita, tenga al Procurador que suscribe por comparecido y parte en la representación que acredita, y por interpuesta DEMANDA EJECUTIVA contra D./Dª [NOMBRE Y APELLIDOS], con el fin de hacer cumplir la sentencia de fecha [DÍA] de [MES] de [AÑO], dictada por este Tribunal en autos de separación (o de divorcio) número [Nº]/[AÑO], y en concreto la obligación, impuesta en ella, de entrega de la vivienda familiar a mi representado/a, y estimando lo que en esta demanda se solicita, se despache ejecución y se requiera al/a la ejecutado/a para que en el plazo de un mes desaloje la vivienda, sin perjuicio de que pueda retirar de ella, antes de abandonarla, sus objetos personales, a cuyos efectos requerirá al/a la ejecutado/a el Letrado de la Administración de Justicia, conforme a lo dispuesto en el artículo 703.1.segundo inciso LEC, y se señale por este Tribunal fecha y hora para proceder al inmediato lanzamiento del/de la ejecutado/a, sin necesidad de requerimiento previo, si no desaloja la vivienda en el plazo indicado al efecto, adoptándose cuantas medidas sean necesarias para ello a su costa, con imposición expresa de las costas de esta ejecución si no se allana a las pretensiones de esta demanda.

PRIMER OTROSÍ DIGO: Que igualmente solicito que se notifique a D./Dª [NOMBRE Y APELLIDOS], como arrendadora de la vivienda litigiosa, con domicilio en [LOCALIDAD], calle [CALLE], nº [NÚMERO], pta., la atribución judicial del uso de la vivienda familiar a mi representado/a, acompañando testimonio de la sentencia en que se realiza tal atribución, todo ello a los efectos del artículo 15 de la Ley de Arrendamientos Urbanos de 1994 (para el caso de que el título por el que se posee la vivienda familiar sea el arrendamiento).

SEGUNDO OTROSÍ DIGO: Que igualmente solicito que, en el caso de apreciarse, en el momento del eventual lanzamiento, desperfectos en la vivienda originados por el/la ejecutado/a, acuerde el Tribunal la retención y constitución en depósito de bienes suficientes de aquél, para responder de los daños y perjuicios causados, en los términos del artículo 703.3 LEC.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma y número del Letrado	Firma del Procurador

========================================================================
