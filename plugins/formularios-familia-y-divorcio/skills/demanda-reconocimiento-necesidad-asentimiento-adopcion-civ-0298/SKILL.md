---
name: demanda-reconocimiento-necesidad-asentimiento-adopcion-civ-0298
description: "Demanda de reconocimiento de necesidad de asentimiento en la adopción, con suspensión del expediente. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de reconocimiento de necesidad de asentimiento en la adopción, con suspensión del expediente

> Formulario **CIV-0298** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Demanda de reconocimiento de la necesidad de asentimiento en la adopción previa suspensión en el expediente de adopción seguido por el tribunal, con solicitud de medida provisional.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de reconocimiento de necesidad de asentimiento en la adopción, con suspensión del expediente» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de reconocimiento de necesidad de asentimiento en la adopción, con suspensión del expediente” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-reconocimiento-necesidad-asentimiento-adopcion-civ-0298`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] FECHA (6 veces)
- [ ] Nº (6 veces)
- [ ] NOMBRE DEL MENOR (5 veces)
- [ ] PROVINCIA (4 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] CALLE (2 veces)
- [ ] COLEGIO (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NOMBRE DE LA INSTITUCIÓN (2 veces)
- [ ] NOMBRE DEL CENTRO (2 veces)
- [ ] Nº DE EXPEDIENTE (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] LUGAR
- [ ] Nº DE COLEGIADO/A
- [ ] PLAZO
- [ ] SEDE

## Normas que cita el formulario

- art. 779 LEC
- art. 176.2 CC
- art. 749.1 LEC
- art. 23 LEC
- art. 753 LEC
- art. 748.7 LEC
- art. 780 LEC
- art. 177.2.2 CC
- art. 1.830 CC
- art. 176.2.3 CC
- art. 394.5 LEC
- art. 394 LEC

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

- Junto a «… LA SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Denominación legal: Sección de Familia, Infancia y Capacidad. Si no existe en el partido, conoce la Sección Civil o la Única (art. 86.3-4 LOPJ). Fuente: LOPJ arts. 84.2.a) y 86 (redacc. LO 1/2025, BOE-A-2025-76).

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

A LA SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales y de Dña. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], calle [CALLE], nº [NÚMERO], como acredito mediante la designación por turno de oficio efectuada por el Iltre. Colegio de Procuradores de [COLEGIO], previamente comunicada, bajo dirección de la letrado en ejercicio Dña. [NOMBRE Y APELLIDOS], con despacho abierto en esta localidad, calle [CALLE],nº [Nº], colegiada nº [Nº DE COLEGIADO/A] del Colegio de Abogados de [COLEGIO], ante el Tribunal comparezco y como mejor proceda en derecho, DIGO:

Que mediante el presente escrito, y dentro del plazo de [PLAZO] (no superior a veinte días) conferido mediante auto de fecha [FECHA], en expediente nº [Nº DE EXPEDIENTE] / seguido por ese Tribunal, deduzco demanda de reconocimiento de la necesidad de asentimiento a la adopción del menor [NOMBRE DEL MENOR] frente a la Diputación Foral de [PROVINCIA], y frente al Ministerio Fiscal, en base a los siguientes datos y consideraciones jurídicas:

HECHOS

PRIMERO.- Mi mandante es la madre del menor [NOMBRE DEL MENOR], que tienen en la actualidad [Nº] años de edad. Se acompaña certificado de nacimiento y libro de familia como DOCUMENTOS NÚMEROS [Nº] Y [Nº].

SEGUNDO.- Por razón de haber logrado mi mandante el cumplimiento alternativo de pena privativa de libertad, recaída en proceso penal en que se constató la grave y prolongada dependencia a opiáceos, mediante el tratamiento deshabituador en la Institución [NOMBRE DE LA INSTITUCIÓN], y haber fallecido su marido D [NOMBRE Y APELLIDOS], en fecha [FECHA], por no poder cuidar a su hijo [NOMBRE DEL MENOR], solicitó de la Diputación Foral de [PROVINCIA] que ésta asumiera la guarda, bajo forma de acogimiento residencial.

Se acompañan testimonio de la ejecutoria penal y auto de suspensión condicional de la pena (DOCUMENTOS NOS. Y [Nº]), certificado de la Institución [NOMBRE DE LA INSTITUCIÓN] (DOCUMENTO Nº [Nº DE DOCUMENTO]).

TERCERO.- Con fecha [FECHA], el Departamento de Acción Social de la citada Diputación Foral dictó resolución por la que se declaraba la situación legal de desamparo de los citados menores, asumiendo por ministerio de la ley la tutela de [NOMBRE DEL MENOR], quedando en acogimiento residencia bajo tutela del Director del Centro [NOMBRE DEL CENTRO] (DOCUMENTO Nº [Nº DE DOCUMENTO]).

CUARTO.- A escasos días de la precitada resolución, mi mandante fue convocada a la Notaría de [LOCALIDAD], donde como ha tenido ocasión de comprobar desdichadamente, suscribió su asentimiento a que su hijo menor fuera adoptado por D [NOMBRE Y APELLIDOS] y Dña. [NOMBRE Y APELLIDOS], de modo que quedaba tal menor en situación de acogimiento preadoptivo.

Así consta en el testimonio del expediente de adopción nº [Nº DE EXPEDIENTE] / que se aporta como DOCUMENTO Nº [Nº DE DOCUMENTO].

No obstante, mi representada creía tratarse de un trámite más para la efectividad del acogimiento residencial temporal.

QUINTO.- Con fecha [FECHA], se promovió por la Diputación Foral el indicado expediente de adopción, previa declaración de idoneidad de D [NOMBRE Y APELLIDOS] y Dña. [NOMBRE Y APELLIDOS], en el cual compareció mi representada mediante escrito de [FECHA], en que manifestaba su petición de que se le reconozca la necesidad de asentir a dicha adopción, lo que motivó que se admitiera por auto que concedía a esta parte, previa suspensión del expediente, [Nº] días para formular la presente demanda.

FUNDAMENTOS DE DERECHO

I.- COMPETENCIA

La competencia objetiva viene atribuida en esta población a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia. La competencia territorial corresponde al del domicilio de la entidad protectora, puesto que no se postula la extinción de la adopción, ya que todavía no se ha declarado (art. 779 LEC).

II.- LEGITIMACIÓN

Está legitimada activamente, de modo ordinario por situación jurídica, quien entabla la demanda, como madre del hijo menor respecto del que se sigue expediente de adopción. Legitimados pasivamente están la entidad pública que promovió el expediente, conforme arts. 176.2 CCiv y 1.829 LECiv 1881, y el Ministerio Fiscal (art. 749.1 LEC).

III.- POSTULACIÓN

Se formula la demanda mediante procuradora de los tribunales y con asistencia de letrada en ejercicio, a través de designación del turno de oficio por la concesión del derecho de asistencia jurídica gratuita (arts. 23, 31 y 750 LEC, y 15 y 18 LAJG)

IV.- PROCEDIMIENTO

El procedimiento se seguirá por los trámites del art. 781, por relación con el art. 753 LEC, que establece el juicio verbal con especialidades para estos asuntos relativos a menores (con contestación escrita), a tenor de art. 748.7º LEC.

V.- FONDO DEL ASUNTO

El objeto de este género de procesos es el control judicial de cumplirse con la precisión de que los padres de los menores respecto de los que se tramite expediente de adopción hayan asentido debidamente (art. 780 LEC, en relación con art. 177.2.2º CCiv).

Como quiera que mi patrocinada no se encuentra privada de la patria potestad sobre su hijo menor [NOMBRE DEL MENOR], ni tampoco incursa en causa legal, sino que la tiene suspendida por la declaración administrativa de desamparo y asunción de tutela por ministerio de la ley de la Diputación Foral de [PROVINCIA], que ejerce el Director del Centro [NOMBRE DEL CENTRO], todo ello a instancias de mi patrocinada por las lamentables circunstancias que atravesaba y en el demostración de la mínima responsabilidad que le permitía su toxicomanía cuando quedó viuda, y nada la inhabilita, ni de Derecho ni de hecho, para prestar su asentimiento a la adopción de su hijo, no es lícito que sea excluida de tal asentimiento, exigido por el art. 177.2.2º CCiv.

Si bien el asentimiento previo a la propuesta de la entidad pública de adopción, en documento público extrajudicial, resulta fórmula de cumplir con la exigencia legal, es menester que no esté viciada la voluntad del que asiente, como lo está al producirse la declaración de voluntad de una persona enferma a los pocos días de que se haya resuelva administrativamente -con arreglo a su desesperada petición- un acogimiento residencial, mientras que se le presenta un programa de acogimiento familiar preadoptivo.

Por añadidura, conforme al art. 1.830 CCiv, no tiene validez un asentimiento extrajudicial emitido antes de seis meses de la propuesta de adopción que da lugar a la incoación del expediente, y no cabe escamotear el asentimiento en el Tribunal sosteniendo que la propuesta no es necesaria y están designados nominalmente los adoptantes, dado que no se produce el supuesto legal de que el menor se halle acogido por tales con un año de antelación (art. 176.2.3º CCiv).

De tal manera, no hay óbice para se reconozca la necesidad de asentir por mi representada a la adopción de su hijo

VI.- COSTAS

De entre los privilegios de la Administración Pública, no se encuentra exenta (salvo para entidades gestoras de la Seguridad Social y algunos entes de utilidad pública, que lo que gozan es de gratuidad legal de justicia, y no de exención de ser condenadas, como es la del Ministerio Fiscal ex art. 394.5 LEC) de la aplicación del principio del vencimiento en punto a la costas procesales (art. 394 LEC).

Por todo lo expuesto,

SUPLICO AL TRIBUNAL

que teniendo por presentado este escrito con los documentos que lo acompañan, dentro del emplazamiento efectuado, se sirva admitir uno y otros, y tener por deducida demanda frente a la Diputación Foral de [PROVINCIA], promotora del expediente de adopción de que conoce ese Tribunal bajo nº [NÚMERO] /, y seguido que sea el oportuno procedimiento, con intervención del Ministerio Fiscal, se dicte sentencia que reconozca la necesidad del asentimiento de la demandante para la adopción de su hijo menor

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a

========================================================================
