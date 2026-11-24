---
name: solicitud-jurisdiccion-voluntaria-abuelos-asuman-civ-0045
description: "Solicitud de jurisdicción voluntaria para que los abuelos asuman la guarda y custodia de los menores. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud de jurisdicción voluntaria para que los abuelos asuman la guarda y custodia de los menores

> Formulario **CIV-0045** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud de jurisdicción voluntaria para que los abuelos asuman la guarda y custodia de los menores» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud de jurisdicción voluntaria para que los abuelos asuman la guarda y custodia de los menores” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:solicitud-jurisdiccion-voluntaria-abuelos-asuman-civ-0045`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (6 veces)
- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] Nº DE DOCUMENTO (6 veces)
- [ ] DNI/NIE (4 veces)
- [ ] AÑO (3 veces)
- [ ] DÍA (3 veces)
- [ ] MES (3 veces)
- [ ] CALLE (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] TOMO (2 veces)
- [ ] COLEGIO
- [ ] SEDE

## Normas que cita el formulario

- art. 769.3 LEC
- art. 87.1 a) LJV
- art. 158 CC
- art. 23 LEC

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

- Junto a «…MILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Denominación legal: Sección de Familia, Infancia y Capacidad. Si no existe en el partido, conoce la Sección Civil o la Única (art. 86.3-4 LOPJ). Fuente: LOPJ arts. 84.2.a) y 86 (redacc. LO 1/2025, BOE-A-2025-76).

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

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales en nombre y representación de D. y Dña. [NOMBRE Y APELLIDOS], mayores de edad, casados, con DNI [DNI/NIE] y [DNI/NIE], respectivamente, y domicilio en [LOCALIDAD], calle [CALLE], nº [NÚMERO], pta., según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño a este escrito, comparezco en este TRIBUNAL con la asistencia del Letrado D./Dª [NOMBRE Y APELLIDOS], del Ilustre Colegio de Abogados de [COLEGIO], y DIGO:

Que por medio del presente escrito y en la representación que ostento, interpongo EXPEDIENTE DE JURISDICCIÓN VOLUNTARIA EN SOLICITUD DE GUARDA Y CUSTODIA DE SU NIETO/A [NOMBRE Y APELLIDOS], por mis mandantes, arriba indicados, conforme a lo dispuesto en el artículo 158 del Código civil, contra los progenitores del/de la menor, D. y Dña. [NOMBRE Y APELLIDOS], mayores de edad, casados, con DNI [DNI/NIE] y [DNI/NIE], respectivamente, y domicilio en [LOCALIDAD], calle [CALLE], nº [NÚMERO], pta. La presente demanda se basa en los siguientes

HECHOS

Los progenitores contrajeron matrimonio civil en [LOCALIDAD], en fecha [DÍA] de [MES] de [AÑO], que consta inscrito en el Registro Civil de dicha localidad, al Tomo [TOMO], Página

Se acompaña como DOCUMENTO Nº [Nº DE DOCUMENTO], con el fin de acreditar este extremo, certificación de matrimonio expedida por el Encargado del Registro Civil.

De dicho matrimonio nació un/a hijo/a, en fecha [DÍA] de [MES] de [AÑO], llamado/a [NOMBRE Y APELLIDOS], cuyo nacimiento consta inscrito en el Registro Civil de [LOCALIDAD], al Tomo [TOMO], Página

Se acompaña como DOCUMENTO Nº [Nº DE DOCUMENTO], con el fin de acreditar este extremo, certificación de la inscripción de nacimiento expedida por el Encargado del Registro Civil.

Los progenitores del/de la menor se encuentran recluidos en prisión por tráfico de estupefacientes, a la espera del juicio correspondiente. Con la finalidad de acreditar dicho extremo, se adjunta copia del auto de la Sección de lo Penal del TI de [LOCALIDAD], de fecha [DÍA] de [MES] de [AÑO], ordenando el ingreso en prisión de ambos progenitores como DOCUMENTO Nº [Nº DE DOCUMENTO]

El/La menor, desde el ingreso en prisión de sus progenitores, ha quedado al cuidado de mis mandantes, sus abuelos maternos, habiendo fallecido los abuelos paternos.

Se acompaña como DOCUMENTO Nº [Nº DE DOCUMENTO], certificación de la inscripción de nacimiento de la madre del/de la menor, expedida por el Encargado del registro Civil de [LOCALIDAD], para acreditar la condición de abuelos maternos de mis mandantes.

Y se acompaña, como DOCUMENTOS Nº [Nº DE DOCUMENTO] y Nº [Nº DE DOCUMENTO], certificados de defunción de los abuelos paternos, expedidos por el Encargado del registro Civil de

A los anteriores hechos son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

Competencia. Es competente el Tribunal al que me dirijo, por corresponder al lugar del último domicilio común de los progenitores, conforme al artículo 769.3 LEC

Capacidad y legitimación. La capacidad procesal de las partes deriva de lo dispuesto en los arts. 6.1 y 7.1 de la Ley de Enjuiciamiento Civil. La legitimación activa de mis mandantes deriva de su condición de abuelos de los menores cuya guarda y custodia reclaman. La legitimación pasiva la ostentan los demandados en su condición de padres de los menores y titulares de la patria potestad sobre los mismos

Procedimiento. El procedimiento aplicable es el previsto en la Jurisdicción voluntaria, concretamente el articulo 87.1 a) LJV, con intervención preceptiva del Ministerio Fiscal, tal y como prevé el artículo 158 CC en la nueva redacción dada por la Ley 8/2021 de 2 de junio

Representación y defensa. Los demandantes comparecen representados y defendidos, respectivamente, por el Procurador y el Letrado que constan en el encabezamiento de este escrito, de acuerdo con lo dispuesto en los artículos 23 y 31 LEC.

Derecho sustantivo. El art. 158 CC en la nueva redacción dada por la Ley 8/2021, de 2 de junio, permite al Juez adoptar las medidas necesarias en protección del menor, en cualquier procedimiento.

Como señala la SAP Asturias, núm. 333/2007, de 17 de septiembre de 2007, "la patria potestad, guarda y custodia y demás instituciones de protección de la infancia, son instituciones cuya finalidad es cumplir adecuadamente la función social inherente a la patria potestad cual es la de asegurar una formación integral y una integración en un entorno familiar y social lo más normalizado posible que la posibilite, de ahí que cuando la misma no es ejercida adecuadamente por los padres se faculta a los jueces a adoptar al, inicio, en el curso o al finalizar cualquier procedimiento, las medidas más adecuadas para lograr estos derechos", entre las cuales puede encontrarse la atribución de la guarda y custodia del menor a los abuelos cuando así convenga a aquél.

En virtud de lo expuesto,

SUPLICO AL TRIBUNAL: Que tenga por presentado este escrito de demanda, con las copias y los documentos que lo acompañan y se sirva admitirlo, teniéndome por parte en la representación que ostento, y por formulada DEMANDA en EXPEDIENTE DE JURISDICCIÓN VOLUNTARIA en solicitud de guarda y custodia de los referidos menores A FAVOR DE LOS ABUELOS, ante la imposibilidad de los progenitores de ejercitar la misma en interés del menor, y dicte, en su día, previo los trámites legales oportunos y la práctica de pruebas que considere pertinentes, sentencia por la que se acuerde otorgar la guarda y custodia de los menores en favor de mis mandantes. Es Justicia que pido en

Firma del/de la Procurador/a	Firma y número del/de la Letrado/a

========================================================================
