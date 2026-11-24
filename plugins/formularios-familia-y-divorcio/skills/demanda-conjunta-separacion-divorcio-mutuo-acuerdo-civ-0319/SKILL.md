---
name: demanda-conjunta-separacion-divorcio-mutuo-acuerdo-civ-0319
description: "Demanda conjunta de separación o divorcio de mutuo acuerdo con distintas opciones legales. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda conjunta de separación o divorcio de mutuo acuerdo con distintas opciones legales

> Formulario **CIV-0319** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Demanda de separación o divorcio interpuesta de mutuo acuerdo por ambos cónyuges contemplando diversas opciones legales.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda conjunta de separación o divorcio de mutuo acuerdo con distintas opciones legales» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda conjunta de separación o divorcio de mutuo acuerdo con distintas opciones legales” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-conjunta-separacion-divorcio-mutuo-acuerdo-civ-0319`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (17 veces)
- [ ] NÚMERO (6 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] CALLE (2 veces)
- [ ] COLEGIO (2 veces)
- [ ] DIRECCIÓN (2 veces)
- [ ] FECHA (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NOMBRE DEL HIJO/A (2 veces)
- [ ] DOMICILIO
- [ ] EDAD
- [ ] LUGAR
- [ ] NOMBRE DEL PODERDANTE
- [ ] Nº
- [ ] RÉGIMEN ECONÓMICO MATRIMONIAL

## Normas que cita el formulario

- art. 777 LEC
- art. 777.3 LEC

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

- Junto a «…TANCIA [ELEGIR: (SECCIÓN CIVIL) / (SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD)] DE»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Notas al pie del formulario original:
(1) La competencia objetiva por razón de la materia corresponde a los Tribunales de Instancia —art. 85.1º LOPJ— y, en las poblaciones donde existan, a los órganos especializados de Familia, en aplicación de los arts. 46 LEC y 96 LOPJ en relación con el artículo 2 del RD 1322/81 de 3 de julio.

(2) Véase Propuesta de convenio regulador de separación o divorcio.

========================================================================

[NOTA DE REVISIÓN: requisito de procedibilidad del art. 5 LO 1/2025 — antes de presentar la demanda hay que intentar un medio adecuado de solución de controversias (MASC) y acreditarlo con la demanda (arts. 264.4.º y 399.3 LEC), salvo las materias excluidas del art. 5.2. Fuente: LO 1/2025, arts. 5 a 7 (BOE-A-2025-76).]


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

AL TRIBUNAL DE INSTANCIA [ELEGIR: (SECCIÓN CIVIL) / (SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD)] DE

[ELEGIR UNA DE LAS ALTERNATIVAS QUE SIGUEN Y SUPRIMIR LAS DEMÁS]

A petición de ambos cónyuges

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, que actúa en nombre y representación de los esposos D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS],
según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO]
cuya representación procesal intereso se verifique por comparecencia apud acta ante el/la Letrado/a de la Administración de Justicia el día y hora que se señale al efecto
[NOMBRE Y APELLIDOS], bajo dirección del Letrado/a D./Dña. [NOMBRE Y APELLIDOS], colegiado/a n.º [NÚMERO] del Iltre. Colegio de Abogados de [COLEGIO], cuyo despacho se abre en [DIRECCIÓN], calle [CALLE], ante el Tribunal comparezco y como mejor en Derecho proceda, DIGO:

Que por medio del presente escrito y siguiendo instrucciones de mis mandantes vengo a formular demanda de [ELEGIR: SEPARACIÓN MATRIMONIAL / DIVORCIO] DE MUTUO ACUERDO de los cónyuges arriba indicados, a la que se acompaña PROPUESTA DE CONVENIO REGULADOR, con base en los siguientes:

A petición de uno de los cónyuges con el consentimiento del otro

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, que actúa en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS], [NOMBRE DEL PODERDANTE]
según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO]
cuya representación procesal intereso se verifique por comparecencia apud acta ante el/la Letrado/a de la Administración de Justicia el día y hora que se señale al efecto
[NOMBRE Y APELLIDOS], bajo dirección del Letrado/a D./Dña. [NOMBRE Y APELLIDOS], colegiado/a n.º [NÚMERO] del Iltre. Colegio de Abogados de [COLEGIO], cuyo despacho se abre en [DIRECCIÓN], calle [CALLE], ante el Tribunal comparezco y como mejor en Derecho proceda, DIGO:

Que por medio del presente escrito y en la meritada representación que ostento de mi mandante, formulo en nombre del mismo, y con la conformidad [ELEGIR: del esposo / de la esposa] D./Dña. [NOMBRE Y APELLIDOS], demanda de [ELEGIR: SEPARACIÓN MATRIMONIAL / DIVORCIO] DE MUTUO ACUERDO, a la que se acompaña PROPUESTA DE CONVENIO REGULADOR, con base en los siguientes:

HECHOS

Primero.- D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS] contrajeron [ELEGIR: matrimonio canónico / matrimonio civil] en [LOCALIDAD], el día [FECHA], a cuya acreditación se acompaña certificación expedida por el Registro Civil de [LOCALIDAD], como DOCUMENTO N.º [NÚMERO].

Desde la celebración de dicho matrimonio ha transcurrido, por tanto, un período de tiempo superior a los tres meses.

Segundo.- Del referido matrimonio nacieron y viven dos hijos varones, de nombres [NOMBRE DEL HIJO/A] y [NOMBRE DEL HIJO/A], menores de edad, que tienen [EDAD] y [Nº] años de edad, respectivamente, como se demuestra con sendas certificaciones registrales que hacen DOCUMENTOS N.º [NÚMERO] y [Nº DE DOCUMENTO].

Tercero.- El matrimonio fue celebrado bajo el régimen legal de [RÉGIMEN ECONÓMICO MATRIMONIAL], siendo el último domicilio común [DOMICILIO].

[ELEGIR UNA OPCIÓN: En caso de separación / En caso de divorcio / En caso de divorcio precedido de separación judicial]

Conforme a lo exigido por el apartado 2 del art. 777 LEC, se adjunta al presente escrito, como DOCUMENTO N.º [NÚMERO], propuesta de convenio regulador firmada por ambos cónyuges así como el acuerdo final alcanzado en el procedimiento de mediación familiar en el que los cónyuges han participado.

A los anteriores hechos son de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

[ELEGIR UNA OPCIÓN: En el último domicilio común / En el domicilio de cualquiera de los solicitantes]

II.- Procedimiento

La acción debe tramitarse conforme a lo establecido en el art. 777 LEC, que es el procedimiento adecuado para conocer de las peticiones de [ELEGIR: separación de mutuo acuerdo, o de un cónyuge con el consentimiento del otro / divorcio de mutuo acuerdo, o de un cónyuge con el consentimiento del otro].

[ELEGIR UNA OPCIÓN: A petición de ambos cónyuges / A petición de uno de los cónyuges con el consentimiento del otro / — y además elegir: En caso de separación / En caso de divorcio / En caso de divorcio precedido de separación judicial]

En virtud de lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito con los documentos que se acompañan y sus copias, se digne admitirlos, y se tenga por formulada DEMANDA DE [ELEGIR: SEPARACIÓN MATRIMONIAL / DIVORCIO] DE MUTUO ACUERDO entre los cónyuges D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS], entendiéndose conmigo las sucesivas diligencias, y previo los pertinentes trámites, los cónyuges sean requeridos por el Letrado de la Administración de Justicia para que comparezcan y se ratifiquen por separado, con intervención del Ministerio Fiscal, dictándose en su día Sentencia por la que se declare la [ELEGIR: separación legal del matrimonio / disolución del matrimonio por divorcio], con todos los efectos legales inherentes a esta declaración, aprobándose el convenio regulador aportado.

[OPCIONAL — incluir si procede]

(En caso de solicitud de uno de los cónyuges con el consentimiento del otro)

OTROSÍ DIGO: Que la presente demanda de [ELEGIR: separación / divorcio] se presenta de acuerdo también con D./Dña. [NOMBRE Y APELLIDOS], que a tenor de lo dispuesto en el art. 777.3 LEC, se ratificará en el contenido de dicha demanda aparte su conformidad prestada en el DOCUMENTO N.º [NÚMERO].

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a

D./Dña. [NOMBRE Y APELLIDOS] D./Dña. [NOMBRE Y APELLIDOS]
