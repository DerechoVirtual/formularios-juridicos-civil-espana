---
name: demanda-oposicion-resolucion-administrativa-proteccion-civ-0329
description: "Demanda de oposición a resolución administrativa de protección de menores tras recabar el expediente. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de oposición a resolución administrativa de protección de menores tras recabar el expediente

> Formulario **CIV-0329** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Demanda de oposición a resolución administrativa en materia de protección de menores, previa solicitud sucinta que ha recabado el expediente administrativo.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de oposición a resolución administrativa de protección de menores tras recabar el expediente» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de oposición a resolución administrativa de protección de menores tras recabar el expediente” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-oposicion-resolucion-administrativa-proteccion-civ-0329`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE DEL MENOR (6 veces)
- [ ] FECHA (5 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] Nº (2 veces)
- [ ] CALLE
- [ ] EDAD
- [ ] LUGAR
- [ ] SEDE

## Normas que cita el formulario

- art. 779 LEC
- art. 749.2 LEC
- art. 753 LEC
- art. 748.7.º LEC
- art. 780.1 LEC
- art. 253 LEC
- art. 3.2 LO 1/2025
- art. 780 LEC
- art. 161 CC
- art. 160 LO 1/1996
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

Que mediante el presente escrito, y dentro del plazo de diez días conferido mediante diligencia de ordenación de fecha [FECHA], deduzco demanda de oposición a la resolución dictada por la Delegación Territorial de [LOCALIDAD] del Departamento de Acción Social de la Comunidad Autónoma de [LOCALIDAD], sobre protección de los menores [NOMBRE DEL MENOR] y [NOMBRE DEL MENOR], en base a los siguientes datos y consideraciones jurídicas:

HECHOS

PRIMERO.- Mis mandantes son los padres de los menores [NOMBRE DEL MENOR] y [NOMBRE DEL MENOR] que tienen en la actualidad [EDAD] y [Nº] años de edad respectivamente. Se acompañan certificados de nacimiento y Libro de familia como DOCUMENTOS NÚMEROS [Nº], [Nº DE DOCUMENTO] y [Nº DE DOCUMENTO].

SEGUNDO.- Con fecha [FECHA] la Delegación Territorial de [LOCALIDAD] del Departamento de Acción Social dictó resolución por la que se declaraba la situación legal de desamparo de los citados menores, asumiendo la tutela de los mismos por ministerio de la Ley, quedando en acogimiento residencial (DOCUMENTO N.º [NÚMERO]).

TERCERO.- Mediante escrito de [FECHA], se expuso sucintamente al Tribunal que se pretendía negar el desamparo de los hijos menores y asimismo la necesidad de convertirlos en pupilos de la Administración, impugnando el acto que lo decretaba, habiendo el Tribunal obtenido testimonio completo del expediente, que se ha traslado a mis mandantes (Se adjunta testimonio como DOCUMENTO N.º [NÚMERO]).

CUARTO.- Mis mandantes no han tenido acceso precedente al expediente administrativo, que ahora se sabe que ha existido, como desvela su propia lectura, y en todo caso, niegan rotundamente todos los hechos recogidos en el mismo y en la resolución reseñada.

FUNDAMENTOS DE DERECHO

I.- COMPETENCIA

La competencia objetiva viene atribuida a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia de esta población. La competencia territorial corresponde al del domicilio de la entidad pública (art. 779 LEC).

II.- LEGITIMACIÓN

Están legitimados activamente, de modo ordinario por situación jurídica, quienes entablan la demanda, como padres de los menores declarados en desamparo (art. 780.1 párrafo 2.º LEC). Legitimados pasivamente están la entidad pública que dictó la resolución y el Ministerio Fiscal (art. 749.2 LEC).

III.- PROCEDIMIENTO

El procedimiento se seguirá por los trámites del art. 780, que se remite al art. 753 LEC, que establece el juicio verbal con especialidades para estos asuntos relativos a menores, a tenor del art. 748.7.º LEC. No se precisa una vía administrativa previa (art. 780.1 LEC).

IV.- CUANTÍA

Cumpliendo la admonición del art. 253 LEC, se manifiesta que la cuantía de la presente demanda resulta inestimable.

V.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD

Conforme a lo dispuesto en el art. 3.2 LO 1/2025, la presente demanda no está sujeta al requisito de MASC, en cuanto se dirige contra una entidad pública como lo es en este caso la

VI.- FONDO DEL ASUNTO

El objeto de este género de procesos es la fiscalización judicial de la declaración del desamparo de menores y la asunción de la tutela por ministerio de la Ley (art. 780 LEC).

Pretensión principal: Se considera como situación de desamparo la que se produce de hecho a causa del incumplimiento, o del imposible o inadecuado ejercicio de los deberes de protección establecidos por las leyes para la guarda de los menores, cuando éstos queden privados de la necesaria asistencia moral o material, circunstancias que no concurren en este caso (art. 172.1 párrafo 2.º CCiv).

En cualquier caso, mis mandantes no han sido notificados legalmente como ordena el art. 172.1 párrafo 1.º CCiv de la intervención administrativa, ni han tenido participación alguna en el expediente administrativo, por lo que han ignorado hasta la intercesión de ese Tribunal las causas del alejamiento forzoso de sus hijos, y los efectos de suspensión de la patria potestad que se han producido. Se alega, pues, vulneración del artículo 24 CE, ya que mis representados no han tenido oportunidad de ser oídos ni de utilizar los medios de prueba pertinentes para su defensa en el procedimiento administrativo.

Pretensión subsidiaria: Conforme al art. 172.ter.2 CCiv, el acogimiento residencial que se tiene acordado, busca el interés de los menores, y procurará, cuando no es contrario al mismo, la reinserción en la propia familia, y ello es la base esencial que debe guiar la regulación del derecho de los padres a visitar y relacionarse con sus hijos menores, atendidas las circunstancias y el interés del menor, como previene el art. 161 CCiv, dado que el dicho derecho de relación personal no puede negarse de raíz y apriorísticamente, aunque se consolide la decisión que suspende la patria potestad (no lo haría ni cuando se privara de ésta por sentencia), a tenor del art. 160 precedente, LO 1/1996, de 15 de enero, de protección jurídica del menor, Convención de Naciones Unidas de 20 de noviembre de 1989 sobre derechos del niño, ratificada por España el 30 de noviembre de 1990, y la doctrina jurisprudencia ampliatoria a las figuras de abuelos o allegados (SSTS de 11 de junio de 1996, Rec. 3446/1991 ó 23 de noviembre de 1999, Rec. 1048/1995).

Es por lo que, ante la absoluta falta de mención de la resolución administrativa, se pide la regulación del régimen más amplio de visitas, como subsidiario de la revocación del acogimiento forzoso, de modo que las vacantes del calendario escolar sea el parámetro de comunicación, visita y estancia con los padres demandantes.

VII.- COSTAS

De entre los privilegios de la Administración Pública, no se encuentra exenta (salvo para entidades gestoras de la Seguridad Social y algunos entes de utilidad pública, que lo que gozan es de gratuidad legal de justicia, y no de exención de ser condenadas, como es la del Ministerio Fiscal ex art. 394.4 LEC) de la aplicación del principio del vencimiento en punto a la costas procesales (art. 394 LEC).

Por todo lo expuesto,

SUPLICO AL TRIBUNAL

que teniendo por presentado este escrito con los documentos que lo acompañan, dentro del emplazamiento efectuado, se sirva admitir uno y otros, y tener por promovida demanda de oposición a la resolución administrativa de desamparo de los menores [NOMBRE DEL MENOR] y [NOMBRE DEL MENOR] de fecha [FECHA], y seguido que sea el oportuno procedimiento, se dicte sentencia que deje sin efecto dicha resolución y acuerde la entrega inmediata de los menores a sus padres, en cuya potestad permanezcan, o subsidiariamente, establezca un régimen de comunicación, visita y estancia de los menores con los demandantes lo más amplio posible, que incluya todos los periodos de descanso escolar.

Es de Justicia que pido en [LUGAR], a [FECHA].

========================================================================
