---
name: escrito-interposicion-apelacion-conflicto-aplicacion-civ-1284
description: "Escrito de interposición de apelación por conflicto de aplicación del Derecho civil catalán. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito de interposición de apelación por conflicto de aplicación del Derecho civil catalán

> Formulario **CIV-1284** del plugin **Recursos civiles: reposición, apelación, casación y queja** (`formularios-recursos-civiles`) · Civil › Recursos · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **recursos**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito de interposición de apelación por conflicto de aplicación del Derecho civil catalán» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito de interposición de apelación por conflicto de aplicación del Derecho civil catalán” para mi caso». También puedes invocarla directamente con `/formularios-recursos-civiles:escrito-interposicion-apelacion-conflicto-aplicacion-civ-1284`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-recursos-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Recursos civiles: reposición, apelación, casación y queja) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (3 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] AÑO
- [ ] DÍA
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] MES
- [ ] NOMBRE DEL MENOR
- [ ] NÚMERO
- [ ] PROFESIÓN

## Normas que cita el formulario

- art. 458 LEC
- art. 9.2 Código Civil
- art. 111 Código Civil
- art. 14 Código Civil
- art. 107 Código Civil
- art. 16 Código Civil
- art. 14.5.2 Código Civil
- art. 233 Código Civil

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

A LA AUDIENCIA PROVINCIAL DE [LOCALIDAD]

D [NOMBRE Y APELLIDOS]., Procurador de los Tribunales, en nombre y representación de D. [NOMBRE Y APELLIDOS], parte demandada en este proceso seguido con el número [NÚMERO], según tengo acreditado en autos, ante la Sala comparezco y como mejor proceda en derecho DIGO:

1) Que en fecha [FECHA] se dictó sentencia en este proceso, la cual fue notificada a esta parte en fecha

2) Que entendiendo que dicha sentencia no es ajustada a derecho, dicho sea con los debidos respetos y en términos de defensa, por medio del presente escrito interpongo contra la misma RECURSO DE APELACIÓN, (se harían constar los pronunciamientos que se impugnan) impugnando los siguientes pronunciamientos: a) Atribución de la guarda y custodia del hijo menor a la esposa; b) Régimen de visitas excesivamente restringido a dos fines de semana mensuales alternos, sin justificación alguna

3) Que, de conformidad a lo dispuesto en el art. 458 de la LEC, fundo el recurso de apelación en las siguientes

ALEGACIONES:

Infracción legal de los arts. 14 y 16 en relación con el artículo 9.2 y 107 del Código Civil y artículo 111-3 del Código Civil de Cataluña, en cuanto que la sentencia aplica indebidamente las normas comunes del Código Civil, cuando es de aplicación el Código Civil de Cataluña, puesto que ambos cónyuges son de vecindad civil catalana.

El art. 14 del Código Civil indica que la sujeción al derecho civil común o especial o foral se determina por la vecindad civil, en tanto que el artículo 9.2 del mismo texto legal en relación con el artículo 107 del Código Civil establecen que la separación y el divorcio se regirán por la Ley nacional común de los cónyuges en el momento de la presentación de la demanda; a falta de nacionalidad común, por la Ley de la residencia habitual común del matrimonio en dicho momento y, en defecto de ésta, por la Ley de la última residencia habitual común del matrimonio si uno de los cónyuges aún reside habitualmente en dicho Estado, lo cual es de aplicación a los conflictos entre derecho común y foral o especial, según dispone el artículo 16 del Código Civil.

En el presente caso ha quedado acreditado que ambos cónyuges se casaron en Cataluña en fecha [FECHA], donde adquirieron su vivienda familiar y nació su hija en fecha

En la época de la separación de las partes, trabajaban en Cataluña, el marido como [PROFESIÓN] y la esposa como

Todo ello conduce a acreditar que las partes viven desde hace mucho más de diez años en Cataluña, por lo que de conformidad al art. 14.5.2º del Código Civil, tienen vecindad civil catalana y por tanto, es de aplicación el Código Civil de Cataluña a los efectos del divorcio.

En la sentencia se aplica el Código Civil común, fundado erróneamente en el hecho de que ninguno de los cónyuges tiene vecindad civil catalana, basado en el mero dato del nacimiento fuera de la Comunidad Autónoma de Cataluña, sin tener en cuenta las normas invocadas sobre vecindad civil ni tampoco la residencia continuada de los cónyuges en esta Comunidad Autónoma.

Por tanto, interesamos que se revoque la sentencia recurrida y se resuelva sobre la cuestión debatida aplicando las normas del Código Civil de Cataluña, tal como se interesa en los siguientes motivos.

Infracción, por inaplicación, del artículo 233-10 al no establecerse la guarda compartida solicitada por esta parte, dándose los requisitos del artículo 233-11.

La atribución de la guarda individual realizada a favor de la demandante Dª se ha realizado con preterición de la preferencia legal en el Código Civil de Cataluña por la guarda compartida, la cual se solicitaba por esta parte, aportando el plan de parentalidad en cuanto a la forma de ejercerse.

La prueba practicada pone de manifiesto que se dan los requisitos del artículo 233-11 del Código Civil de Cataluña para la guarda compartida, estableciendo el artículo 233-10, apartado 2, una preferencia por el régimen de guarda compartida por estimarse más favorable a los hijos menores, ya que permite una convivencia continuada con ambos progenitores, si bien por períodos sucesivos en el tiempo, con lo que se evita la ruptura afectiva que siempre se da en los casos de guarda individual. La propia sentencia recurrida, aun aceptando la capacitación de los padres, la vinculación afectiva de cada uno de ellos con sus hijos, la existencia de actividades compartidas y la actitud positiva del padre en relación a los hijos, la cual se desprende claramente de la pericial practicada y de la exploración del menor, atribuye la guarda individual a la madre, obviando de esta forma el interés del menor y la preferencia establecida en el citado artículo 233-10 del Código Civil de Cataluña, el cual resulta infringido.

Por ello, se solicita la revocación del pronunciamiento de otorgamiento de la guarda individual a la madre, solicitando que se establezca el régimen de guarda compartida por ser de interés para el menor, tal como se propuso por esta parte en el plan de parentalidad presentado con nuestra contestación a la demanda.

(en su caso se relacionarían otros motivos)

Por lo expuesto,

,

SUPLICO A LA SALA: Tenga por presentado este escrito y justificante del traslado de copias lo una a autos, y por interpuesto y formalizado, en tiempo y forma, recurso de apelación contra la sentencia dictada con fecha [FECHA] y, tras los trámites legales, A LA SALA SUPLICO que dicte resolución revocatoria de la dictada en la instancia en los siguientes extremos:

1) Se deje sin efecto la atribución de la guardia y custodia del hijo menor [NOMBRE DEL MENOR], estableciéndose la guarda compartida en la forma propuesta en el plan de parentalidad acompañado con nuestro escrito de demanda.

2) (se harían constar otras pretensiones en su caso)

OTROSÍ PRIMERO DIGO que, de conformidad con lo dispuesto en los apartados 3.b) y 6 de la disposición adicional decimoquinta de la LOPJ acompaño a este escrito resguardo de consignación en la cuenta de Depósitos y Consignaciones abierta a nombre del Tribunal del depósito exigido para interponer el recurso por importe de 50 euros.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma Procurador y Abogado

========================================================================
