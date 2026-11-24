---
name: oposicion-ejecutar-impago-pensiones-alegando-mayoria-civ-1506
description: "Oposición a ejecutar el impago de pensiones alegando la mayoría de edad e independencia del hijo. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Oposición a ejecutar el impago de pensiones alegando la mayoría de edad e independencia del hijo

> Formulario **CIV-1506** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Escrito de oposición del progenitor ejecutado a la ejecución forzosa de una sentencia de divorcio por impago de la pensión de alimentos de un hijo, alegando que el hijo es mayor de edad, ha alcanzado independencia económica y no convive con el progenitor ejecutante, de modo que ya no concurren los requisitos del art. 93, párrafo segundo, del Código Civil. Se presenta dentro del plazo concedido tras el despacho de ejecución.

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Oposición a ejecutar el impago de pensiones alegando la mayoría de edad e independencia del hijo» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Oposición a ejecutar el impago de pensiones alegando la mayoría de edad e independencia del hijo” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:oposicion-ejecutar-impago-pensiones-alegando-mayoria-civ-1506`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] MES Y AÑO (2 veces)
- [ ] NOMBRE DEL HIJO (2 veces)
- [ ] Nº (2 veces)
- [ ] AÑO
- [ ] DENOMINACIÓN DE LAS EMPRESAS
- [ ] DOMICILIO
- [ ] DÍA
- [ ] LOCALIDAD
- [ ] MES
- [ ] NOMBRE Y APELLIDOS
- [ ] NOMBRE Y APELLIDOS DEL EJECUTADO
- [ ] NOMBRE Y APELLIDOS DEL EJECUTANTE
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] NOMBRE Y APELLIDOS, Nº DE COLEGIADO
- [ ] Nº DE PROCEDIMIENTO
- [ ] SEDE

## Normas que cita el formulario

- art. 93 Código Civil
- art. 7 Código Civil
- art. 142 Código Civil
- art. 556 LEC
- art. 559.3 LEC

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

PROCEDIMIENTO DE DIVORCIO N.º [Nº DE PROCEDIMIENTO]

A LA SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

[NOTA: si en la sede no existe Sección de Familia, Infancia y Capacidad, dirigir el escrito a la Sección Civil o a la Sección Única del Tribunal de Instancia que conozca del asunto.]

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS DEL EJECUTADO], parte ejecutada en el procedimiento de ejecución arriba referenciado, según tengo acreditado en autos, ante el Tribunal comparezco y como mejor proceda en Derecho, DIGO:

Que, dentro del plazo concedido, paso a formular OPOSICIÓN A LA EJECUCIÓN instada de contrario, alegando que mi representado/a está cumpliendo puntualmente lo ordenado en la sentencia, ello en base a los siguientes

HECHOS

Nos oponemos a la demanda ejecutiva instada de contrario, puesto que, si bien es cierto que la sentencia fijó una pensión en concepto de alimentos para el hijo [NOMBRE DEL HIJO], lo cierto es que el hijo ya es mayor de edad y no reside con la madre/el padre desde la fecha en que se reclama la pensión alimenticia, haciendo vida independiente y trabajando de forma temporal en diferentes empresas, como se expondrá seguidamente.

Concretamente, el hijo común [NOMBRE DEL HIJO] ha desarrollado trabajos en las empresas [DENOMINACIÓN DE LAS EMPRESAS] desde el mes de [MES Y AÑO] hasta el mes de [MES Y AÑO], siendo mayor de edad, independiente económicamente y no residiendo en el entorno del progenitor ejecutante, puesto que su domicilio es el de [DOMICILIO], es decir, distinto del de dicho progenitor (acompaño como documentos n.º [Nº] contratos de trabajo del hijo común, nóminas y certificado de empadronamiento).

Frente a la alegación del/de la ejecutante de que no se ha instado modificación de las medidas establecidas en la sentencia, debemos alegar que, según viene manteniendo de modo reiterado la jurisprudencia, tratándose de hijos mayores de edad, la efectividad de la obligación alimenticia a través del cauce habilitado por los artículos 517 y siguientes de la Ley de Enjuiciamiento Civil ha de quedar necesariamente supeditada, en el entorno de los procedimientos matrimoniales, a la subsistencia de los requisitos al efecto exigidos en el párrafo segundo del artículo 93 del Código Civil, esto es, la falta de autonomía pecuniaria del hijo y la convivencia del mismo con uno de sus progenitores. Entenderlo de otro modo, obligando al deudor, en este caso a mi mandante, a acudir a un procedimiento declarativo para conseguir la extinción de la obligación preestablecida, supondría, por el mantenimiento en el ínterin de la vigencia de tal medida, otorgar amparo judicial a una conducta procesal de manifiesto abuso de derecho por parte del progenitor que reclama, en vía ejecutiva, la efectividad de un deber respecto del que ya no concurren los condicionantes que determinaron su inicial sanción judicial, lo que viene expresamente prohibido por el artículo 7 del Código Civil, generando además una situación de enriquecimiento sin causa respecto de quien, por lo expuesto, ya no se encuentra amparado por el título de cuya ejecución se trata, lo que además atrae necesariamente a tales hipótesis las previsiones excluyentes del artículo 559.3 de la Ley de Enjuiciamiento Civil.

De otro lado, y en lo que concierne también a la vigencia del derecho alimenticio, no puede prescindirse, tratándose de hijos mayores de edad, de las previsiones de carácter general al respecto contenidas en los artículos 142 y siguientes del Código Civil, a los que expresamente se remite el artículo 93, párrafo segundo, estableciendo el citado artículo 142 que los alimentos comprenden también la educación e instrucción del alimentista, tras su mayoría de edad, cuando no haya terminado su formación por causa que no le sea imputable.

Bajo estas premisas fácticas, en su incardinación en las citadas previsiones legales, debe desestimarse la pretensión sostenida por el/la ejecutante.

A los anteriores hechos les son aplicables los siguientes

FUNDAMENTOS DE DERECHO

Procedimiento

Artículo 776 LEC, en relación con los artículos 556 y 560 de la LEC.

Legitimación

Artículo 556.1 LEC, al ser parte ejecutada en el presente proceso de ejecución.

Oposición a la ejecución

Por motivos de fondo, al amparo del art. 559.3 de la LEC, en relación con los artículos 93 y 142 del Código Civil.

Costas

Han de imponerse al/a la ejecutante de conformidad con los artículos 539.2 y 559.2.2 LEC.

En su virtud,

SUPLICO AL TRIBUNAL: Tenga por presentado este escrito, documentos y copias, se sirva admitirlos y unirlos a autos, teniendo por formalizada, en tiempo y forma, oposición a la demanda ejecutiva instada por [NOMBRE Y APELLIDOS DEL EJECUTANTE] contra mi mandante y, previa sustanciación, estime la oposición deducida y proceda a dictar auto dejando sin efecto la ejecución despachada, condenando en costas al/a la ejecutante.

OTROSÍ DIGO que, tratándose de una controversia fáctica respecto de la cual es necesaria la práctica de prueba, además de la documental aportada, se interesa que por el Tribunal se acuerde la celebración de vista para sustanciar la oposición.

Por lo que SUPLICO AL TRIBUNAL que acuerde la celebración de vista.

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma Abogado: [NOMBRE Y APELLIDOS, Nº DE COLEGIADO]

Firma Procurador: [NOMBRE Y APELLIDOS]
