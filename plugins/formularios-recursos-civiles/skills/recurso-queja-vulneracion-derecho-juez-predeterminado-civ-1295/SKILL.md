---
name: recurso-queja-vulneracion-derecho-juez-predeterminado-civ-1295
description: "Recurso de queja por vulneración del derecho al juez predeterminado por la ley (art. 24 CE). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Recurso de queja por vulneración del derecho al juez predeterminado por la ley (art. 24 CE)

> Formulario **CIV-1295** del plugin **Recursos civiles: reposición, apelación, casación y queja** (`formularios-recursos-civiles`) · Civil › Recursos · normativa revisada el 24-11-2026.

## Qué es

Recurso de queja ante la Sala Primera del Tribunal Supremo contra el auto de la Audiencia Provincial que deniega tener por preparado o interpuesto el recurso de casación (arts. 494 y 495 LEC). El modelo alega que la Audiencia ha invadido la competencia de admisión del Tribunal Supremo, con infracción del art. 24 CE (juez predeterminado por la ley y derecho al recurso).

Es un modelo de tipo **recursos**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Recurso de queja por vulneración del derecho al juez predeterminado por la ley (art. 24 CE)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Recurso de queja por vulneración del derecho al juez predeterminado por la ley (art. 24 CE)” para mi caso». También puedes invocarla directamente con `/formularios-recursos-civiles:recurso-queja-vulneracion-derecho-juez-predeterminado-civ-1295`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-recursos-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Recursos civiles: reposición, apelación, casación y queja) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (7 veces)
- [ ] PROVINCIA (6 veces)
- [ ] FECHA (5 veces)
- [ ] ARTÍCULOS
- [ ] AÑO
- [ ] DÍA
- [ ] LEY
- [ ] LOCALIDAD
- [ ] MES
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] NOMBRE Y APELLIDOS O DENOMINACIÓN SOCIAL DEL RECURRENTE

## Normas que cita el formulario

- art. 494 LEC
- art. 477.2.3.º LEC
- art. 24 LEC
- art. 479.2 LEC
- art. 483.1 LEC
- art. 483 LEC
- art. 481 LEC
- art. 479 LEC
- art. 481.2 LEC
- art. 483.1.3.º LEC

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

- Al principio del formulario: el régimen del recurso de casación (arts. 477 a 483 LEC) fue modificado por el Real Decreto-ley 5/2023, de 28 de junio; el modelo se redactó conforme a la versión dada por la Ley 37/2011. Antes de usarlo, comprobar la redacción vigente de los arts. 477 a 483 y 494 LEC (en particular el control de admisión que corresponde a la Audiencia Provincial y el plazo de la queja) y ajustar las citas.

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

A LA SALA PRIMERA DEL TRIBUNAL SUPREMO

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales y de [NOMBRE Y APELLIDOS O DENOMINACIÓN SOCIAL DEL RECURRENTE], según acredito mediante copia electrónica del poder notarial de representación original que acompaño, la cual solicito se testimonie en autos con devolución del original, ante la Sala comparezco y, como mejor proceda en derecho,

DIGO:

1) Que el pasado día [FECHA] fue notificado a esta parte el auto de fecha [FECHA], dictado por la Sección [Nº] de la Audiencia Provincial de [PROVINCIA] en el Rollo de Apelación Civil n.º [Nº], por el que acordaba no admitir la interposición del recurso de casación deducido por esta parte; y, entendiendo dicho auto no ajustado a derecho, dicho sea en términos de defensa, y lesivo para los intereses de esta parte, mediante el presente escrito, al amparo de lo dispuesto en los arts. 494 y 495 de la LEC, interpongo RECURSO DE QUEJA contra la citada resolución, aportando con este escrito copia de la resolución recurrida, la cual fue notificada a esta parte en fecha [FECHA], tal como consta en la diligencia que por copia también acompaño.

2) La queja se interpone contra la denegación de la interposición del recurso de casación que había presentado esta parte, al amparo de lo dispuesto en el art. 477.2.3.º de la LEC, por presentar el recurso interés casacional, por cuanto la sentencia de la Audiencia Provincial de [PROVINCIA], dictada en el Rollo de Apelación [Nº], se oponía a la interpretación jurisprudencial del Tribunal Supremo en relación con los arts. [ARTÍCULOS] de la [LEY], así como se contradecía con la jurisprudencia de otras Audiencias Provinciales (acompaño como documento n.º [Nº] copia del escrito de interposición del recurso).

3) Al denegarse la interposición por la Audiencia Provincial de [PROVINCIA], se infringen los arts. 24 CE y 479, 481 y 483 de la LEC, a cuyo efecto alegamos los siguientes

MOTIVOS

PRIMERO.– Infracción del art. 24 de la CE, derecho fundamental al juez predeterminado por la ley, en relación con lo dispuesto en el art. 479.2 de la LEC.

La denegación de la interposición del recurso de casación entiende esta parte que infringe el derecho fundamental al juez predeterminado por la ley, establecido en el art. 24 de la CE, puesto que la Audiencia Provincial ha asumido las funciones del Tribunal Supremo, dictando una auténtica resolución de inadmisión del recurso de casación, que el art. 483.1 de la LEC reserva al órgano ad quem, una vez se ha presentado el escrito de interposición del recurso.

Tal como se desprende de la lectura del auto de inadmisión de fecha [FECHA], la Audiencia entró en el fondo del recurso, analizando si existe o no divergencia jurisprudencial con la sentencia recurrida, lo que es una decisión que corresponde exclusivamente al Tribunal Supremo, tal como dispone el art. 483 de la LEC, limitándose el control de admisión de la Audiencia a constatar que la resolución es recurrible y que el recurso se ha interpuesto en plazo, tal como se establece en el artículo 479.2 de la LEC. En este sentido, la simple lectura del auto pone de manifiesto que se invadió plenamente por la Audiencia Provincial de [PROVINCIA] la competencia en orden a la decisión de la admisión del recurso de casación, que corresponde al Tribunal Supremo, realizando un verdadero examen de fondo sobre la contradicción que se invocaba en nuestro escrito de interposición.

El derecho fundamental a la tutela judicial efectiva, en su vertiente del derecho al recurso, impide una interpretación extensiva de los supuestos de inadmisión, estableciendo requisitos adicionales no prevenidos por la ley para tener acceso al recurso. El art. 481 de la LEC únicamente exige que el escrito de interposición exprese la infracción legal que se considere cometida, exponiendo con la necesaria extensión sus fundamentos, y que se acompañe certificación de la sentencia impugnada y del texto de las sentencias que pongan de manifiesto la doctrina jurisprudencial o jurisprudencia contradictoria en que se funde el interés casacional que se alegue. Así lo hizo esta parte en su escrito de interposición, expresando las infracciones legales que considerábamos cometidas y las sentencias que ponían de manifiesto la jurisprudencia contradictoria que fundaba el interés casacional alegado por esta parte. Por este motivo, entendemos que la Sala ha infringido lo dispuesto en el art. 24 de la CE, al introducir elementos adicionales para la interposición del recurso y, consecuentemente, hay infracción de lo dispuesto en el art. 479 de la LEC.

SEGUNDO.– Infracción del art. 479.2 de la LEC en relación con lo dispuesto en el art. 481, con indefensión de esta parte.

El escrito de interposición del recurso de casación presentado por esta parte reunía los requisitos establecidos en el art. 481 de la LEC, citando la infracción legal que entendíamos cometida y las sentencias que ponían de manifiesto la contradicción en que se fundaba el interés casacional. Nuestro escrito de interposición razonaba sobre la doctrina jurisprudencial que se entendía vulnerada en la sentencia, tal como exige el art. 481.2 de la LEC, y como expresamente se reconoce en el auto recurrido en queja. Sin embargo, como se ha indicado anteriormente, el auto recurrido en queja entra en el fondo del asunto, indicando que no hay ajuste fáctico entre las sentencias invocadas como contradictorias y la recurrida. Precisamente, son estas cuestiones las que han de ser analizadas por el Tribunal ad quem, ya sea en el trámite de admisión conforme al art. 483.1.3.º de la LEC, ya sea en la resolución del recurso, con lo que la Sección [Nº] de la Audiencia Provincial de [PROVINCIA] ha ido más allá de lo permitido en el art. 479.2 de la LEC, al no limitarse a exigir los requisitos del art. 481 de la LEC, sino que también exige «poner de manifiesto el interés casacional». Ello origina una situación de indefensión a esta parte, proscrita por el art. 24 de la CE, puesto que se exige, en sede de admisión, manifestar un interés casacional que en ningún momento se establece en el art. 479 de la LEC. Por tanto, el auto recurrido va más allá de lo establecido en el art. 479.2 de la LEC, fundando el rechazo en la exigencia de otros requisitos adicionales del escrito de interposición, no revisables en sede de admisión por el tribunal a quo.

Por lo anterior,

SUPLICO A LA EXCMA. SALA PRIMERA DEL TRIBUNAL SUPREMO que tenga por interpuesto recurso de queja contra el auto de fecha [FECHA], dictado por la Sección [Nº] de la Audiencia Provincial de [PROVINCIA] en el Rollo de Apelación n.º [Nº], por el que se rechazaba la preparación del recurso de casación presentado por esta parte, y declare mal denegada la tramitación del recurso de casación y ordene a dicho tribunal que continúe la tramitación.

OTROSÍ PRIMERO DIGO: Que, por necesitarlo para otros usos, solicito la devolución de la copia electrónica del poder notarial de representación original y que quede testimonio de la misma en autos.

OTROSÍ SEGUNDO DIGO: Que, de conformidad con lo dispuesto en los apartados 3.a) y 6 de la disposición adicional decimoquinta de la LOPJ, acompaño a este escrito resguardo de consignación en la cuenta de Depósitos y Consignaciones abierta a nombre del Tribunal del depósito exigido para interponer el recurso, por importe de 30 euros.

Por lo que SUPLICO A LA EXCMA. SALA que tenga por constituido el depósito, dejando interesada desde este momento su devolución para el caso de estimación total o parcial del recurso.

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Procurador/a y Abogado/a
