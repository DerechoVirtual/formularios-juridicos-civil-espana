---
name: convenio-regulador-matrimonio-mixto-entre-espanol-civ-0215
description: "Convenio regulador de un matrimonio mixto entre español y extranjero. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Convenio regulador de un matrimonio mixto entre español y extranjero

> Formulario **CIV-0215** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Convenio regulador de un matrimonio mixto entre español y extranjero» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Convenio regulador de un matrimonio mixto entre español y extranjero” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:convenio-regulador-matrimonio-mixto-entre-espanol-civ-0215`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (5 veces)
- [ ] AÑO (4 veces)
- [ ] MES (4 veces)
- [ ] NOMBRE DEL HIJO/A (4 veces)
- [ ] DÍA (3 veces)
- [ ] LUGAR DE RESIDENCIA DEL MENOR (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] Nº (2 veces)
- [ ] DOMICILIO
- [ ] LUGAR
- [ ] Nº DE LEY
- [ ] RÉGIMEN DE ALIMENTOS
- [ ] RÉGIMEN DE PATRIA POTESTAD

## Normas que cita el formulario

- No cita artículos concretos; Claude localizará las normas aplicables con Jurisprudenciator si el documento las necesita.

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

CONVENIO REGULADOR MATRIMONIO MIXTO (ESPAÑOL -EXTRANJERO)

En [LUGAR], a [DÍA] de [MES] de [AÑO].

INTERVIENEN

Ambos en su propio nombre y derecho, reconociéndose mutuamente capacidad legal suficiente para otorgar el presente CONVENIO REGULADOR, y por vía de antecedentes,

EXPONEN

PRIMERO Que contrajeron matrimonio civil, el día [DÍA] de [MES] de [AÑO] en la Municipalidad Distrital de [LOCALIDAD]

SEGUNDO Que de dicha unión ha nacido un hijo, [NOMBRE DEL HIJO/A] el día [DÍA] de [MES] de [AÑO]

TERCERO El último domicilio conyugal estuvo establecido en [DOMICILIO], inmueble propiedad de [NOMBRE Y APELLIDOS] y sobre la que los firmantes reconocen no ostentar derecho alguno.

CUARTO Que el matrimonio, se encuentran separados desde el mes de [MES] de [AÑO] de forma ininterrumpida, y que para regularizar su situación han decidido solicitar de común acuerdo la separación de cuerpo y divorcio. Durante este tiempo el menor ha residido en [LUGAR DE RESIDENCIA DEL MENOR].

QUINTO Que con objeto de cumplir los requisitos relativos a las exigencias y características que ha de tener el convenio regulador que acompañe a las demandas de separación de mutuo acuerdo, ambos cónyuges suscriben el presente convenio con base en las siguientes:

ESTIPULACIONES

[ELEGIR UNA OPCIÓN: Domicilio / Vivienda domicilio conyugal es propiedad / Vivienda domicilio conyugal es arrendada]

Guarda y custodia de los hijos

La guarda y custodia del hijo menor [NOMBRE DEL HIJO/A], por acuerdo de ambos cónyuges se atribuye al [ELEGIR: padre / madre] La razón de ser de esta decisión estriba en las mejores condiciones de vida de que puede disfrutar el menor en [LUGAR DE RESIDENCIA DEL MENOR], especialmente si tenemos en cuenta los problemas físicos y psíquicos que padece desde su nacimiento.

En todo caso, el progenitor mientras dure la custodia, se compromete a escribir mail todas las semanas informando al progenitor no custodio sobre los aspectos cotidianos de la vida de menor y cuantas novedades pudieran ir aconteciendo. Igualmente, le enviará periódicamente fotos de [NOMBRE DEL HIJO/A], especialmente aquellas que tengan relación con acontecimientos puntuales, tales como cumpleaños, navidades, excursiones, viajes o similares. Todo ello sin perjuicio de las comunicaciones personales directas que se puedan establecer entre madre e hijo al menos una vez al mes, a través de web cam o de teléfono. Respecto de la patria potestad, es de ambos padres.

Régimen de visitas

El progenitor no custodio podrá visitar al menor durante [Nº] días al año, días que se fijarán de común acuerdo por ambos progenitores. Las visitas se efectuarán en la localidad donde el menor resida habitualmente. Dada la distancia física que separa [LOCALIDAD] de [LOCALIDAD], el régimen de visitas deberá ser interpretado con criterios de flexibilidad y buena fe, dado que se contempla como un derecho del menor.

En todo caso, se trata de un régimen de visitas abierto acordado en función de la distancia física que separa al progenitor no custodio del menor. No obstante, si en algún momento tales circunstancias cambiaran los firmantes se comprometen a revisar el régimen de visitas para facilitar y favorecer la comunicación progenitor no custodio-hijo.

En cualquier caso, cuando se produzcan las visitas del progenitor no custodio, el menor estará en compañía de una persona de su entorno habitual.

[ELEGIR UNA OPCIÓN: Pensión alimenticia / Con pensión alimenticia / Sin pensión alimenticia / — y además elegir: Pensión compensatoria / Sin desequilibrio entre las partes / Con desequilibrio entre las partes / — y además elegir: Régimen económico matrimonial / Con disolución del régimen matrimonial / Sin disolución del régimen matrimonial]

Sumisión

Ambos cónyuges se comprometen a presentar este Convenio antes los tribunales de [LOCALIDAD] Q.P.T.R.C. para someterlo a aprobación judicial, junto con la demanda de solicitud de separación de mutuo acuerdo y a ratificarlo.

Leído el documento por ambas partes, se ratifican en el mismo los cónyuges, que seguidamente lo firman en el fecha y lugar arriba indicados, manifestando también estar dispuestos a ratificarlo en el Tribunal, a presencia judicial, en la correspondiente causa de separación, que a tenor de la legislación vigente solicitarán de mutuo acuerdo.

Apoderamiento

Que, por convenir a mi derecho, el cónyuge D. otorga poder especial a mi APODERAD0 a fin de que en mi nombre y representación pueda iniciar el proceso de separación convencional y divorcio ulterior de conformidad a la ley [Nº DE LEY] que regula el procedimiento no contencioso de la separación convencional y divorcio ulterior en las Notarias, Tribunales y Municipalidades así como su reglamento, solicitud que interpondrá conjuntamente con su esposa Doña [NOMBRE Y APELLIDOS]

El poder se otorga a los únicos efectos de apoderar al poderdado para que la separación convencional y ulterior divorcio se rija única y exclusivamente por las cláusulas y condiciones establecidas en el presente convenio matrimonial.

En consecuencia el apoderado podrá asistir a la audiencia notarial, judicial y Municipal que se señale oportunamente donde manifiesten o no la voluntad de ratificarse en la solicitud de separación convencional en tales términos; de igual forma podrá solicitar el divorcio ulterior una vez transcurrido el plazo de dos meses señalado en la ley.----

Que, así mismo, el apoderado podrá asistir a la audiencia de conciliación emitida por un centro de conciliación extrajudicialmente donde se especifique el régimen de ejercicio de la patria potestad [RÉGIMEN DE PATRIA POTESTAD], alimentos [RÉGIMEN DE ALIMENTOS], tenencia y de visitas de nuestro menor hijo [NOMBRE DEL HIJO/A] de [Nº] años de edad, en consonancia con el convenio matrimonial. El otorgamiento de las facultades especiales se rige por el principio de la literalidad No se presume la existencia de facultades especiales no conferidas explícitamente.

El apoderado podrá solicitar la inscripción del divorcio notarial, judicial o Municipal ante el Registro Nacional de identidad (RENIEC) y Municipalidad correspondiente así como los Registros Públicos de [LOCALIDAD] pudiendo solicitar y recabar ante las indicadas entidades la partida de matrimonio correspondiente con la anotación del divorcio notarial, judicial o Municipal.

========================================================================
