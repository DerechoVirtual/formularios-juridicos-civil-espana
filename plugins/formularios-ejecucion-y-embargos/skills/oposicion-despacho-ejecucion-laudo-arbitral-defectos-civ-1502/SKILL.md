---
name: oposicion-despacho-ejecucion-laudo-arbitral-defectos-civ-1502
description: "Oposición al despacho de ejecución de un laudo arbitral por defectos procesales. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Oposición al despacho de ejecución de un laudo arbitral por defectos procesales

> Formulario **CIV-1502** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Escrito mediante el cual la parte ejecutada se opone al despacho de ejecución de un laudo arbitral alegando defectos procesales (falta de personalidad o de representación del ejecutado y nulidad del laudo por referirse a materia no susceptible de arbitraje, en el ejemplo, un arrendamiento de vivienda). Se presenta dentro del plazo concedido tras el despacho de la ejecución (arts. 556 y 559 LEC).

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Oposición al despacho de ejecución de un laudo arbitral por defectos procesales» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Oposición al despacho de ejecución de un laudo arbitral por defectos procesales” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:oposicion-despacho-ejecucion-laudo-arbitral-defectos-civ-1502`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A (2 veces)
- [ ] AÑO
- [ ] DENOMINACIÓN SOCIAL
- [ ] DÍA
- [ ] EXPONER, EN SU CASO, OTROS MOTIVOS DE OPOSICIÓN QUE PROCEDAN
- [ ] FECHA
- [ ] FECHA DEL LAUDO
- [ ] MES
- [ ] NOMBRE DEL NOTARIO
- [ ] NOMBRE Y APELLIDOS DEL ABOGADO/A, Nº DE COLEGIADO
- [ ] NOMBRE Y APELLIDOS O DENOMINACIÓN SOCIAL DEL EJECUTADO
- [ ] Nº
- [ ] Nº DE DOCUMENTO
- [ ] Nº DE PROCEDIMIENTO
- [ ] PLAZO, EN AÑOS
- [ ] SEDE

## Normas que cita el formulario

- art. 559 LEC
- art. 22.4 LEC

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

- Junto a «…E PROCEDIMIENTO] A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA N.º [Nº] DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

[OPCIONAL — si ha lugar: téngase en cuenta que en el hecho segundo se desarrollará el motivo concreto de nulidad que proceda en cada caso.]

Procedimiento de ejecución n.º [Nº DE PROCEDIMIENTO]

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA N.º [Nº] DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, en nombre y representación de [NOMBRE Y APELLIDOS O DENOMINACIÓN SOCIAL DEL EJECUTADO], parte ejecutada en el procedimiento de ejecución arriba referenciado, según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño a este escrito, ante el Tribunal comparezco y como mejor proceda en Derecho, DIGO:

Que dentro del plazo concedido a esta parte, y al amparo de lo dispuesto en el artículo 559 de la LEC, formulo OPOSICIÓN A LA EJECUCIÓN DEL LAUDO ARBITRAL DICTADO EN FECHA [FECHA DEL LAUDO] por defectos procesales y ello en base a los siguientes

HECHOS

PRIMERO.– Que el ejecutante demanda a mi principal como representante legal de la sociedad [DENOMINACIÓN SOCIAL], condenada en el laudo arbitral objeto de ejecución, sin que el mismo tenga dicho carácter, teniendo en cuenta que desde hace más de [PLAZO, EN AÑOS] años mi mandante no ostenta cargo de representación alguno en la sociedad, ya que dejó de ostentar el cargo de administrador único y socio desde [FECHA], tal y como se acredita mediante la aportación de la escritura pública otorgada ante el Notario de [LOCALIDAD] D./Dña. [NOMBRE DEL NOTARIO], que se aporta como documento número [Nº DE DOCUMENTO].

SEGUNDO.– Caso de no apreciarse el anterior motivo, se alega la nulidad radical del laudo por referirse a materia no susceptible de arbitraje conforme a lo dispuesto en el artículo 2 de la Ley de Arbitraje, lo cual determina la nulidad radical del laudo.

En este caso, el laudo se refiere a la resolución de un contrato de arrendamiento urbano sobre la vivienda ocupada por mi representado por falta de pago de la renta, donde la jurisprudencia viene pronunciándose sobre su inadmisibilidad (AAP Madrid, Sección 19.ª, de 18 de enero de 2011) y, en todo caso, sobre la inadmisión del arbitraje de equidad en estos supuestos (AAP Madrid, Sección 11.ª, de 7 de marzo de 2011, rec. 345/2010, y de 24 de febrero de 2011, rec. 329/2010; Sección 20.ª, de 12 de abril de 2011, rec. 26/2011, y de 24 de febrero de 2011, rec. 777/2010; y Sección 21.ª, de 8 de febrero de 2011, rec. 665/2010, entre otros).

En este caso, se despacha ejecución sobre un laudo dictado en arbitraje de equidad en materia de resolución del contrato de arrendamiento de vivienda, donde es de aplicación el régimen legal imperativo de la legislación arrendaticia, por cuanto que se pretende proteger una de las necesidades básicas de la persona, que encuentra incluso protección constitucional (artículo 47 de la Constitución), estableciéndose un régimen imperativo para ciertas materias afectantes a ese contrato de arrendamiento de vivienda y con la previsión imperativa de la facultad de enervación que se concede al arrendatario (artículo 22.4 LEC) con un contenido preciso, legalmente predeterminado, tanto en su contenido como en el tiempo de su ejercicio.

Por eso, la norma que prevé la enervación no es susceptible de modulación alguna, ni aunque por equidad pudiera resultar adecuado introducir algún tipo de modificación a su contenido. Y por ello mismo, no cabría la posibilidad de arbitraje de equidad, pues, con independencia de cómo se desarrollara éste, no entran en las funciones del árbitro lo que, de no ser por aquella imperatividad, sería lo natural: la decisión en equidad, esto es, según lo que considere más justo, sin sujeción a norma legal alguna.

TERCERO.– [EXPONER, EN SU CASO, OTROS MOTIVOS DE OPOSICIÓN QUE PROCEDAN].

A los anteriores hechos le son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

Procedimiento

Artículos 556 y 559 de la LEC.

Legitimación

Artículo 556.1 LEC, al ser parte ejecutada en el presente proceso de ejecución.

Oposición a la ejecución

Artículo 559.1.1.º LEC, alegándose los siguientes motivos:

a) Falta de personalidad del ejecutado por no tener el carácter o representación con que se le demanda.

b) Nulidad radical del despacho de ejecución, por no cumplir el documento presentado los requisitos establecidos legalmente.

Costas

Artículo 559.2 LEC, imponiéndose al ejecutante debido a su mala fe y temeridad.

Por lo expuesto,

SUPLICO AL TRIBUNAL: Tenga por presentado este escrito, documentos y copias, se sirva admitirlos y unirlos a autos, teniendo por formulada, en tiempo y forma, oposición a la demanda ejecutiva instada de contrario y, previa su sustanciación, estime la oposición deducida y proceda a dictar auto dejando sin efecto la ejecución despachada, condenando en costas al ejecutante.

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma Abogado: [NOMBRE Y APELLIDOS DEL ABOGADO/A, Nº DE COLEGIADO]

Firma Procurador: [NOMBRE Y APELLIDOS DEL PROCURADOR/A]
