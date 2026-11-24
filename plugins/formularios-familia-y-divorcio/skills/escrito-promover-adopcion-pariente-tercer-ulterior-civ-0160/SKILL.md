---
name: escrito-promover-adopcion-pariente-tercer-ulterior-civ-0160
description: "Escrito para promover la adopción de un pariente en tercer o ulterior grado colateral. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito para promover la adopción de un pariente en tercer o ulterior grado colateral

> Formulario **CIV-0160** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Todas las referencias a Juzgados contenidas en este documento se entenderán sustituidas por Tribunales de Instancia cuando estos se constituyan, conforme al régimen transitorio que prevé la DT 1ª LO 1/2025

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito para promover la adopción de un pariente en tercer o ulterior grado colateral» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito para promover la adopción de un pariente en tercer o ulterior grado colateral” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:escrito-promover-adopcion-pariente-tercer-ulterior-civ-0160`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (9 veces)
- [ ] Nº DE DOCUMENTO (8 veces)
- [ ] LOCALIDAD (6 veces)
- [ ] Nº (4 veces)
- [ ] NÚMERO (4 veces)
- [ ] NOMBRE DEL MENOR (3 veces)
- [ ] AÑO (2 veces)
- [ ] CALLE (2 veces)
- [ ] DÍA (2 veces)
- [ ] MES (2 veces)
- [ ] COLEGIO
- [ ] EDAD
- [ ] FECHA DEL AUTO
- [ ] LUGAR
- [ ] OTROS DATOS
- [ ] SEDE

## Normas que cita el formulario

- art. 175.1 CC
- art. 176.2.1 Código Civil
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

### Avisos de actualización (1) — se aplican en el texto, nunca se copian en el documento

- Junto a «…O 1/2025 A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] – PLAZA N.º [Nº]»: desde la LO 1/2025 los Tribunales de Instancia (Sección Civil) son la Sección Civil del Tribunal de Instancia (DA 1.ª y DT 1.ª).

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

Los consortes D./Dª [NOMBRE Y APELLIDOS], y D./Dª [NOMBRE Y APELLIDOS], mayores de edad, con domicilio en [LOCALIDAD], calle [CALLE], nº [NÚMERO] pta., que señalan a efecto de notificaciones, y D.N.I. y respectivamente, comparecemos ante el Tribunal, con la asistencia del Letrado D/Dª [NOMBRE Y APELLIDOS], del Ilustre Colegio de Abogados de [COLEGIO], y DECIMOS:

Que por medio del presente escrito promueven expediente de jurisdicción voluntaria para la CONSTITUCIÓN DE LA ADOPCIÓN de [NOMBRE DEL MENOR], con base en los siguientes.

HECHOS

PRIMERO.- El adoptando [NOMBRE DEL MENOR], nació en [LOCALIDAD] el [DÍA] de [MES] de [AÑO], encontrándose determinada, tan sólo, su filiación materna, que corresponde a Dª

Se acompaña como DOCUMENTO Nº 1 certificación literal de nacimiento del menor expedida por el encargado del Registro Civil de [LOCALIDAD]

SEGUNDO.- La madre del menor, que se veía incapaz de atender a su hijo y deseaba llevar una vida libre de ataduras, marchó al extranjero hace ahora [Nº] años, encontrándose desde entonces en paradero desconocido, sin que se hayan tenido noticias suyas en su entorno familiar, dejando a su hijo bajo la guarda de hecho de sus abuela materna Dª [NOMBRE Y APELLIDOS], que le ha venido prestando los cuidados y atenciones debidos.

Con base en los hechos anteriores, se solicitó y obtuvo declaración de fallecimiento de la madre del menor, por auto de fecha [FECHA DEL AUTO], dictado por el Tribunal de Instancia (Sección Civil, plaza n.º [NÚMERO]) en procedimiento de jurisdicción voluntaria número [NÚMERO], testimonio del cual se acompaña como DOCUMENTO Nº [Nº DE DOCUMENTO]

TERCERO.- La guardadora de hecho, es así mismo, madre de D./Dª [NOMBRE Y APELLIDOS], solicitante, junto con su cónyuge, de la adopción y tío/tía, por tanto, del menor. El parentesco que une a D./Dª [NOMBRE Y APELLIDOS] con el menor -es su tío/a carnal- y el afecto que le profesa, así como los estrechos lazos que ha mantenido siempre con su madre, guardadora de aquél, han creado unos vínculos que le mueve, en el momento presente, junto con su cónyuge, como ya se ha dicho, y de conformidad con la abuela y guardadora de hecho, a solicitar la adopción del menor.

Se acompañan como DOCUMENTOS Nos y [Nº DE DOCUMENTO], certificado de matrimonio de los solicitantes, expedido por el Encargado del Registro Civil de [LOCALIDAD], y certificado de nacimiento del/de la citado/a tío/tía del menor, expedido por el Encargado del Registro Civil de [LOCALIDAD], para acreditar el referido parentesco.

CUARTO.- Los solicitantes cuentan respectivamente con [EDAD] y [Nº] años de edad cumplidos, mientras que el adoptando tiene [Nº] años de edad, como resulta de los DOCUMENTOS Nº [Nº DE DOCUMENTO] y Nº [Nº DE DOCUMENTO] antes citados [OTROS DATOS] Por tanto, se cumplen los requisitos de edad exigidos a los adoptantes por el art. 175.1 CC.

QUINTO.- La situación familiar de los solicitantes de la adopción es la siguiente:

Se acompañan como DOCUMENTOS Nos, [Nº DE DOCUMENTO] y [Nº DE DOCUMENTO] los siguientes: para acreditar las anteriores circunstancias por ejemplo, Libro de familia, etc.

SEXTO.- En cuanto a su situación laboral y económica, los trabajos, ingresos y bienes de los solicitantes, son los siguientes:

Se acompañan como DOCUMENTOS Nos, [Nº DE DOCUMENTO] y [Nº DE DOCUMENTO] los siguientes: para acreditar la situación laboral y los ingresos de los solicitantes, así como los bienes y derechos de su titularidad y los rendimientos que de ellos obtiene entre ellos se puede incluir la declaración de la renta del año anterior, certificados de nóminas, notas simples informativas del Registro de la Propiedad, etc.

Sin perjuicio de los documentos que se acompañan, se ofrece información testifical de las siguientes personas, cuyo testimonio podrá recabar el Tribunal, de considerarlo conveniente, en el momento procesal oportuno: se identifica a los testigos propuestos, con sus nombres y apellidos, domicilio y número de DNI

SÉPTIMO.- La abuela y guardadora de hecho del adoptando, Dª [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], calle [CALLE], nº [NÚMERO], pta., tal y como ella misma está dispuesta a declarar en el momento en que el Tribunal la emplace a tal efecto, está conformes con la adopción solicitada. No existen, por otra parte, otros parientes allegados del menor.

Resultan aplicables a los anteriores hechos, los siguientes

FUNDAMENTOS DE DERECHO

I. COMPETENCIA. Son competentes los Tribunales de Instancia (Sección Civil) de esta ciudad, por ser el del domicilio del adoptante, conforme a lo dispuesto en el art. 33 de la Ley de Jurisdicción Voluntaria.

II. PROCEDIMIENTO.- Debe seguirse el procedimiento de jurisdicción voluntaria regulado en los artículos 33 y siguientes de la Ley de Jurisdicción Voluntaria.

De acuerdo con el art. 8 de la Ley de la Jurisdicción Voluntaria, “Las disposiciones de la Ley de Enjuiciamiento Civil serán de aplicación supletoria a los expedientes de jurisdicción voluntaria en todo lo no regulado por la presente Ley”.

III. LEGITIMACIÓN.-Los solicitantes están legitimados conforme a lo dispuesto en el art. 176.2.1ª del Código Civil y art. 34.3 de la Ley de Jurisdicción Voluntaria.

IV. FUNDAMENTOS DE FONDO.-El art. 175 del Código Civil en cuanto a los requisitos para la adopción; los artículos 176 y 177 del citado texto legal y arts. 36 a 39 de la Ley de Jurisdicción Voluntaria, en cuanto a los requisitos que han de observarse en la tramitación del expediente, y los artículos 178 a 180 del Código Civil en cuanto a los efectos.

Por lo expuesto

SUPLICAMOS AL TRIBUNAL que teniendo por presentado este escrito con los documentos y copias que se acompañan, se sirva admitirlo, y tenga por promovido expediente de jurisdicción voluntaria en SOLICITUD DE CONSTITUCIÓN DE ADOPCIÓN de [NOMBRE DEL MENOR] y tras recabar los consentimientos, asentimientos y practicar las audiencias y demás diligencias que legalmente proceda, incluida la información testifical que dejo interesada, y con la preceptiva intervención del Ministerio Fiscal, se sirva dictar Auto en el que constituya la adopción solicitada, designando como adoptantes a los cónyuges D./Dª [NOMBRE Y APELLIDOS] y D./Dª [NOMBRE Y APELLIDOS] y acuerde, en consecuencia, el cambio de apellidos del adoptado, librándose testimonio de la resolución, cuando sea firme, para su inscripción en el Registro Civil, junto con lo demás que en Derecho proceda.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma de los Solicitantes	Firma y número del Letrado

========================================================================
