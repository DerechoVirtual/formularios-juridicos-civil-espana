---
name: demanda-oposicion-declaracion-administrativa-desamparo-civ-0077
description: "Demanda de oposición a la declaración administrativa de desamparo de un menor (Derecho catalán). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de oposición a la declaración administrativa de desamparo de un menor (Derecho catalán)

> Formulario **CIV-0077** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Demanda de oposición a resolución administrativa por la que se declara la situación legal de desamparo de un menor, previa solicitud sucinta que ha recabado el expediente administrativo, conforme a Derecho Civil especial de Cataluña.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de oposición a la declaración administrativa de desamparo de un menor (Derecho catalán)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de oposición a la declaración administrativa de desamparo de un menor (Derecho catalán)” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-oposicion-declaracion-administrativa-desamparo-civ-0077`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (6 veces)
- [ ] NOMBRE DEL MENOR (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] CALLE
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] Nº
- [ ] SEDE

## Normas que cita el formulario

- art. 779 LEC
- art. 749.2 LEC
- art. 753 LEC
- art. 748.7.º LEC
- art. 253 LEC
- art. 3.2 LO 1/2025
- art. 780 LEC
- art. 228.2 Código Civil
- art. 105 Ley 14/2010
- art. 17.2 Ley Orgánica 1/1996
- art. 106 Ley 14/2010
- art. 394.4 LEC
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

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales y de D. y Dña. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], calle [CALLE], n.º [NÚMERO], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], ante el Tribunal comparezco y como mejor proceda en derecho, DIGO:

Que mediante el presente escrito, y dentro del plazo de diez días conferido mediante diligencia de ordenación de fecha [FECHA], deduzco demanda de oposición a la resolución de fecha [FECHA], dictada por la Dirección General de Atención a la Infancia y a la Adolescencia de la Generalitat de Cataluña, sobre protección del menor [NOMBRE DEL MENOR], en base a los siguientes datos y consideraciones jurídicas:

HECHOS

PRIMERO.- Mis mandantes son los padres del menor [NOMBRE DEL MENOR] que tiene en la actualidad [Nº] años de edad. Se acompañan certificados de nacimiento y Libro de familia como DOCUMENTOS NÚMEROS y [Nº DE DOCUMENTO].

SEGUNDO.- Con fecha [FECHA] la Dirección General de Atención a la Infancia y a la Adolescencia de la Generalitat de Cataluña dictó resolución por la que se declaraba la situación legal de desamparo del citado menor, asumiendo la tutela del mismo por ministerio de la Ley, en centro de acogida de la Generalitat (DOCUMENTO N.º [NÚMERO]).

TERCERO.- Mediante escrito de [FECHA], se expuso sucintamente al Tribunal que se pretendía negar el desamparo del hijo menor, impugnando el acto que lo decretaba, habiendo el Tribunal obtenido testimonio completo del expediente, que se ha traslado a mis mandantes (se adjunta testimonio como DOCUMENTO N.º [NÚMERO]).

CUARTO.- Mis mandantes no han tenido acceso precedente al expediente administrativo, que ahora se sabe que ha existido, como desvela su propia lectura, y en todo caso, niegan rotundamente todos los hechos recogidos en el mismo y en la resolución reseñada (se continuará rechazando las argumentaciones de la resolución administrativa).

FUNDAMENTOS DE DERECHO

I.- COMPETENCIA.

La competencia objetiva viene atribuida a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia de esta población. La competencia territorial corresponde al del domicilio de la entidad pública (art. 779 LEC).

II.- LEGITIMACIÓN.

Están legitimados activamente, de modo ordinario por situación jurídica, quienes entablan la demanda, como padres del menor declarado en desamparo (art. 780.1 párrafo 2.º LEC). Legitimados pasivamente están la entidad pública que dictó la resolución y el Ministerio Fiscal (art. 749.2 LEC).

III.- PROCEDIMIENTO.

El procedimiento se seguirá por los trámites del art. 780, que se remite al art. 753 LEC, que establece el juicio verbal con especialidades para estos asuntos relativos a menores, a tenor del art. 748.7.º LEC. No se precisa una vía administrativa previa (art. 113.1 Ley catalana 14/2010, de 27 de mayo, de los derechos y las oportunidades en la infancia y la adolescencia; y 780.1 LEC).

IV.- CUANTÍA.

Cumpliendo la admonición del art. 253 LEC, se manifiesta que la cuantía de la presente demanda resulta inestimable.

V.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD

Conforme a lo dispuesto en el art. 3.2 LO 1/2025, la presente demanda no está sujeta al requisito de MASC, en cuanto se dirige contra una entidad pública como lo es en este caso

VI.- FONDO DEL ASUNTO.

El objeto de este género de procesos es la fiscalización judicial de la declaración del desamparo de menores y la asunción de la tutela por ministerio de la Ley (art. 780 LEC).

La regulación de la protección de los menores en caso de desamparo en el Derecho Civil Catalán se encuentra recogida en el Capítulo VIII del Título II del Código Civil de Cataluña (arts. 228.1 a 228.9), que incorpora al libro segundo relativo a la persona y la familia de la Ley catalana 25/2010, de 29 de julio, los aspectos civiles de la derogada Ley 37/1991, de 30 de diciembre, sobre medidas de protección de los menores desamparados y de la adopción.

Dispone el art. 228.2 del Código Civil de Cataluña que la declaración de desamparo se rige por lo establecido por el Código y la legislación sobre la infancia y la adolescencia en lo que se refiere a los indicadores de desamparo, el procedimiento, el régimen de impugnación y la revisión por cambio de circunstancias.

Por su parte, el art. 105 de la Ley 14/2010, de 27 de mayo, de los derechos y las oportunidades en la infancia y la adolescencia contempla los supuestos en que se considera que el menor incurre en situación de desamparo, circunstancias que no concurren en este caso.

En nuestro sistema, corresponde a la Administración (en concreto a la Generalitat de Catalunya, mediante la Dirección General de Atención a la Infancia y a la Adolescencia) la competencia para la protección de los menores desamparados domiciliados o que se encuentren en Catalunya y, en consecuencia, también para interpretar prima facie y para declarar la concurrencia de los diversos conceptos jurídicos indeterminados en juego (cuál es el interés del concreto menor afectado y si se halla o no en situación de desamparo), así como para valorar la adecuación al caso de las medidas de protección, con pleno sometimiento al sistema normativo, incluidos los principios generales aplicables en esta materia (art. 103.1 CE), y sin incurrir en arbitrariedad (art. 9.3 CE). Y, por supuesto, corresponde a los órganos judiciales, y entre ellos específicamente a los de la jurisdicción civil (art. 22.quáter.d) LOPJ y arts. 779 y ss. LEC), verificar que, al actuar, aquélla lo hizo conforme a la ley en su conjunto y dentro del quantum de discrecionalidad que el sistema le otorga (art. 106.1 CE).

Por lo tanto, la determinación del desamparo obliga también al examen de las circunstancias del caso, especialmente por lo que se refiere a alguna de las causas previstas legalmente, como sucede con la relativa a la incapacidad o a la falta de medios suficientes por parte de la familia de origen para atender a las necesidades "morales" y "materiales" del menor, que contemplan con redacciones diferentes nuestra legislación.

Pero en todo caso, el incumplimiento de estos deberes debe provocar una ausencia de asistencia mínima, sean cuales sean las características y consecuencias de esta ausencia, siempre que se ajusten a las características previstas en el art. 105 de la Ley 14/2010, de 27 de mayo, de los derechos y las oportunidades en la infancia y la adolescencia. Por su parte, el art. 17.2 de la Ley Orgánica 1/1996, de 15 de enero, recoge una lista de situaciones que considera de riesgo social que justifiquen la apreciación de la situación de desamparo, pero indudablemente la asistencia moral y material de los menores en orden a la declaración de desamparo, ha de merecer una interpretación restrictiva, buscando un equilibrio entre el beneficio del menor y la protección de sus relaciones paterno-filiales, de tal manera que sólo se estime la existencia del desamparo cuando se acredite, efectivamente, el incumplimiento de unos mínimos de atención al menor, exigidos por la conciencia social más común.

En cualquier caso, mis mandantes no han sido notificados legalmente de la intervención administrativa como ordena el art. 106 de la Ley 14/2010, de 27 de mayo, de los derechos y las oportunidades en la infancia y la adolescencia, ni han tenido participación alguna en el expediente administrativo, por lo que han ignorado hasta la intercesión de ese Tribunal las causas del alejamiento forzoso de su hijo, y los efectos de suspensión de la potestad parental que se han producido. Se alega, pues, vulneración del art. 24 CE, ya que mis representados no han tenido oportunidad de ser oídos ni de utilizar los medios de prueba pertinentes para su defensa en el procedimiento administrativo.

VII.- COSTAS:

De entre los privilegios de la Administración Pública, no se encuentra exenta (salvo para entidades gestoras de la Seguridad Social y algunos entes de utilidad pública, que lo que gozan es de gratuidad legal de justicia, y no de exención de ser condenadas, como es la del Ministerio Fiscal ex art. 394.4 LEC) de la aplicación del principio del vencimiento en punto a la costas procesales (art. 394 LEC).

Por todo lo expuesto,

SUPLICO AL TRIBUNAL

que teniendo por presentado este escrito con los documentos que lo acompañan, dentro del emplazamiento efectuado, se sirva admitir uno y otros, y tener por promovida demanda de oposición a la resolución administrativa de desamparo del menor [NOMBRE DEL MENOR] de fecha [FECHA], y seguido que sea el oportuno procedimiento, se dicte sentencia que deje sin efecto dicha resolución y acuerde la entrega inmediata del menor a sus padres, en cuya potestad parental permanezcan, ordenando el inmediato reintegro de las funciones tutelares del menor, con expresa imposición de las costas procesales a la parte demandada

Es de Justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a

========================================================================
