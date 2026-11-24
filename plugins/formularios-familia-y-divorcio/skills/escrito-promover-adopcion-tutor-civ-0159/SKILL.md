---
name: escrito-promover-adopcion-tutor-civ-0159
description: "Escrito para promover la adopción por el tutor. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito para promover la adopción por el tutor

> Formulario **CIV-0159** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Todas las referencias a Juzgados contenidas en este documento se entenderán sustituidas por Tribunales de Instancia cuando estos se constituyan, conforme al régimen transitorio que prevé la DT 1ª LO 1/2025

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito para promover la adopción por el tutor» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito para promover la adopción por el tutor” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:escrito-promover-adopcion-tutor-civ-0159`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] Nº (7 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] AÑO (4 veces)
- [ ] Nº DE DOCUMENTO (4 veces)
- [ ] DÍA (3 veces)
- [ ] MES (3 veces)
- [ ] DESCRIPCIÓN DE LOS DOCUMENTOS (2 veces)
- [ ] NOMBRE DEL MENOR (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] CALLE
- [ ] COLEGIO
- [ ] DNI/NIE
- [ ] EDAD
- [ ] EXPONER LOS HECHOS
- [ ] LUGAR
- [ ] SEDE

## Normas que cita el formulario

- art. 1825 LEC
- art. 175.1 CC
- art. 175.3.3 CC
- art. 176.2.3 Código Civil
- art. 175 Código Civil
- art. 178 Código Civil

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

### Avisos de actualización (2) — se aplican en el texto, nunca se copian en el documento

- Junto a «…O 1/2025 A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] – PLAZA N.º [Nº]»: desde la LO 1/2025 los Tribunales de Instancia (Sección Civil) son la Sección Civil del Tribunal de Instancia (DA 1.ª y DT 1.ª).
- Junto a «…etrado en este tipo de procedimiento es opcional, conforme al art. 1825 LEC/1881»: La jurisdicción voluntaria de la LEC de 1881 está derogada; hoy rige la Ley 15/2015, de 2 de julio, de la Jurisdicción Voluntaria. Hay que citar el artículo equivalente.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Todas las referencias a Juzgados contenidas en este documento se entenderán sustituidas por Tribunales de Instancia cuando estos se constituyan, conforme al régimen transitorio que prevé la DT 1ª LO 1/2025


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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] – PLAZA N.º [Nº]

Los consortes D./Dª [NOMBRE Y APELLIDOS] y D./Dª [NOMBRE Y APELLIDOS], mayores de edad, con domicilio en [LOCALIDAD], calle [CALLE], nº [NÚMERO], pta., que señalan a los efectos de recibir notificaciones, y D.N.I. y [DNI/NIE], comparecen ante ese Tribunal con la asistencia del Letrado D./Dª [NOMBRE Y APELLIDOS], del Ilustre Colegio de Abogados de [COLEGIO], la asistencia de Letrado en este tipo de procedimiento es opcional, conforme al art. 1825 LEC/1881 y DICEN:

Que por medio del presente escrito promueven expediente de jurisdicción voluntaria para la CONSTITUCIÓN DE LA ADOPCIÓN de [NOMBRE DEL MENOR], con base en los siguientes

HECHOS

PRIMERO.- El adoptando [NOMBRE DEL MENOR], nació en [LOCALIDAD] el [DÍA] de [MES] de [AÑO], hijo de D. [NOMBRE Y APELLIDOS] y de Dª [NOMBRE Y APELLIDOS]

Se acompaña como DOCUMENTO Nº 1 certificación literal de la inscripción de nacimiento del menor expedida por el encargado del Registro Civil de [LOCALIDAD]

SEGUNDO.- Al sufrir sus padres un accidente automovilístico con fallecimiento de ambos, y tras los trámites legales pertinentes, mis mandantes fueron nombrados tutores del menor, por el Tribunal nº [NÚMERO] de [LOCALIDAD], en virtud de auto de fecha [DÍA] de [MES] de [AÑO] dictado en procedimiento de jurisdicción voluntaria número [Nº]/[AÑO], testimonio del cual se acompaña como DOCUMENTO Nº 2. Se acompaña igualmente, como DOCUMENTOS Nº 3 y Nº 4, certificados de defunción de los padres biológicos del menor, expedidos por el Encargado del Registro Civil de [LOCALIDAD],

TERCERO.- Desde que comenzamos a ejercer el cargo de tutores, momento en el cual el adoptando contaba con [Nº] años de edad, aquél ha convivido con nosotros y con el resto de nuestra familia, integrándose en ella como un miembro más, siendo nuestra voluntad consolidar esta situación mediante su adopción.

CUARTO.- Actualmente contamos respectivamente con [EDAD] y [Nº] años de edad cumplidos, mientras que el adoptando tiene [Nº] años de edad, como resulta del DOCUMENTO Nº 1 y de nuestro certificado de matrimonio que igualmente se acompaña como DOCUMENTO Nº 5. Por tanto, se cumplen los requisitos de edad exigidos a los adoptantes por el art. 175.1 CC.

Por otra parte, a los efectos de lo dispuesto en el artículo 175.3.3ª CC, se hace constar que ha sido aprobada la cuenta general justificativa de la tutela, acompañándose como DOCUMENTO Nº 6, testimonio de la correspondiente resolución judicial.

QUINTO.- Nuestra situación familiar es la siguiente [EXPONER LOS HECHOS]

Se acompañan como DOCUMENTOS Nº [Nº], [Nº DE DOCUMENTO] y [Nº DE DOCUMENTO] los siguientes: para acreditar las anteriores circunstancias [DESCRIPCIÓN DE LOS DOCUMENTOS]

SEXTO.- En cuanto a la situación laboral y económica de mis representados, a la que igualmente se alude en cumplimiento de las exigencias del art. 35.3 y 4 de la Ley de la Jurisdicción Voluntaria, sus trabajos, ingresos y bienes, son los siguientes:

Se acompañan como DOCUMENTOS Nº [Nº], [Nº DE DOCUMENTO] y [Nº DE DOCUMENTO] los siguientes: [DESCRIPCIÓN DE LOS DOCUMENTOS], para acreditar la situación laboral y los ingresos de los solicitantes, así como los bienes y derechos de su titularidad y los rendimientos que de ellos obtiene

Sin perjuicio de los documentos que se acompañan, se ofrece información testifical de las siguientes personas cuyo testimonio podrá recabarse, de considerarlo conveniente el Tribunal, en el momento procesal oportuno:

SÉPTIMO.- Los familiares más allegados del adoptando son los siguientes: y, tal y como ellos mismos están dispuestos a declarar en el momento en que el Tribunal los emplace a tal efecto, si lo considera conveniente, están conformes con la adopción solicitada.

Resultan aplicables a los anteriores hechos, los siguientes

FUNDAMENTOS DE DERECHO

I. COMPETENCIA.- Son competentes los Tribunales de Instancia (Sección Civil) de esta ciudad, por ser el del domicilio de los adoptantes conforme a lo dispuesto en el art. 33 de la Ley de Jurisdicción Voluntaria.

II. PROCEDIMIENTO.- Debe seguirse el procedimiento de jurisdicción voluntaria regulado en los artículos 33 y siguientes de la Ley de Jurisdicción Voluntaria.

III.LEGITIMACIÓN.- Los solicitantes están legitimados conforme a lo dispuesto en el art. 176.2.3ª del Código Civil y art. 34.3 de la Ley de Jurisdicción Voluntaria.

IV.FUNDAMENTOS DE FONDO.- El art. 175 del Código Civil en cuanto a los requisitos para la adopción, habiéndose aprobado la cuenta general justificativa de la tutela; los artículos 176 y 177 del citado texto legal y arts. 36 a 39 de la Ley de Jurisdicción Voluntaria, en cuanto a los requisitos que han de observarse en la tramitación del expediente, y los artículos 178 a 180 del Código Civil en cuanto a los efectos.

Por lo expuesto

SUPLICAMOS AL TRIBUNAL que teniendo por presentado este escrito con los documentos y copias que se acompañan, se sirva admitirlo, y tenga por promovido expediente de jurisdicción voluntaria en SOLICITUD DE CONSTITUCIÓN DE ADOPCIÓN de D./Dª [NOMBRE Y APELLIDOS] y tras recabar los consentimientos, asentimientos y practicar las audiencias y otras diligencias que legalmente proceda, se sirva dictar auto en el que constituya la adopción solicitada, designando como adoptantes a los cónyuges D./Dª [NOMBRE Y APELLIDOS] y D./Dª [NOMBRE Y APELLIDOS] y acuerde, en consecuencia, el cambio de apellidos del adoptado, librándose testimonio de la resolución, cuando sea firme, para su inscripción en el Registro Civil, junto con lo demás que en Derecho proceda.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma del Procurador	Firma y número del Letrado

========================================================================
