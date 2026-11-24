---
name: contestacion-fiscal-demanda-oposicion-resolucion-civ-0281
description: "Contestación del Fiscal a demanda de oposición a resolución administrativa de protección de menores. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contestación del Fiscal a demanda de oposición a resolución administrativa de protección de menores

> Formulario **CIV-0281** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Escrito de contestación del Ministerio Fiscal a la demanda de oposición a una resolución administrativa en materia de protección de menores (declaración de desamparo), en el que se solicita que se confirme la resolución de la entidad pública (arts. 172 CC y 780 y 753 LEC).

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contestación del Fiscal a demanda de oposición a resolución administrativa de protección de menores» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contestación del Fiscal a demanda de oposición a resolución administrativa de protección de menores” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:contestacion-fiscal-demanda-oposicion-resolucion-civ-0281`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (5 veces)
- [ ] DENOMINACIÓN (3 veces)
- [ ] FECHA (2 veces)
- [ ] AÑO
- [ ] DÍA
- [ ] ENTIDAD PÚBLICA COMPETENTE EN MATERIA DE PROTECCIÓN DE MENORES
- [ ] FIRMA
- [ ] MES
- [ ] NOMBRE DEL MENOR
- [ ] NOMBRE Y APELLIDOS
- [ ] NOMBRE Y APELLIDOS DEL FISCAL
- [ ] Nº DE PROCEDIMIENTO
- [ ] PROVINCIA
- [ ] SEDE

## Normas que cita el formulario

- art. 753 LEC
- art. 172 CC
- art. 154 CC

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

### Avisos de actualización (2) — se aplican en el texto, nunca se copian en el documento

- Junto a «…MILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.

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

El Fiscal [NOMBRE Y APELLIDOS DEL FISCAL], en autos de juicio n.º [Nº DE PROCEDIMIENTO] sobre oposición a resolución administrativa en materia de protección de menores, comparece y dice:

Que evacua el traslado que le ha sido conferido conforme a lo dispuesto en el art. 753 LEC, contestando a la demanda deducida de contrario y oponiéndose a la misma, sirviendo de base a esta contestación los siguientes

HECHOS

ÚNICO.–

El Ministerio Fiscal no puede rechazar ni aceptar los hechos relatados en la demanda, dado que no le consta que sean ciertos los alegados por lo que al objeto de la pretensión se refiere, debiendo probarlos la parte actora conforme la Ley exige, pero solo admitirá, en cumplimiento de su función, aquellos que se comprueben debidamente probados con arreglo a la Ley.

FUNDAMENTOS DE DERECHO

I

Se muestra conformidad con la competencia del Tribunal; no hay motivos para dudar de la capacidad procesal de [ELEGIR: el demandante / la demandante], [ELEGIR: el cual está legitimado / la cual está legitimada]; el procedimiento es el adecuado y comparece [ELEGIR: el actor / la actora] con la debida representación técnica y asistencia letrada, sin que se hayan desoído las exigencias formales para la demanda.

II

La situación de desamparo definida en el art. 172 CC no resulta de la ausencia de progenitores, sino que se anuda a la falta de la necesaria asistencia moral o material de los menores de edad y se produce, con carácter general, cuando los padres infringen los deberes propios de la patria potestad contenidos en el art. 154 del referido texto legal.

En tal sentido, siguiendo reiterada jurisprudencia, el derecho que asiste a los padres respecto de sus hijos menores y, dentro de él, el específico de la guarda y tutela, viene incluso entre los que la doctrina denomina derechos-función, en los que la especial naturaleza que les otorga su carácter social, que trasciende al ámbito meramente privado, hace que su ejercicio se constituya no en meramente facultativo para su titular, sino en obligatorio para quien lo ostente, toda vez que su adecuado cumplimiento lleva unas finalidades sociales, en este caso el interés familiar, que le hacen especialmente preciado para el ordenamiento jurídico (STS de 11 de octubre de 1991). Como también ha declarado el Alto Tribunal, constitucionalmente se impone a los padres y a los poderes públicos el deber de dispensar una protección especial a quienes, por razones de edad, no están en condiciones de valerse por sí mismos o de procurar su autogobierno, erigiéndose la patria potestad en la institución protectora del menor por excelencia, y cuyo contenido está formado más por deberes que por derechos, sin que el carácter familiar de la patria potestad excluya que el legislador, teniendo en cuenta las razones que justifican una especial protección de los menores, prevenga la intervención judicial en esa institución protectora, así como la del Ministerio Fiscal y la entidad pública administrativa (STS de 31 de diciembre de 1995).

Pues bien, el art. 172 CC considera en situación de desamparo «la que se produce de hecho, a causa del incumplimiento, o del imposible o inadecuado ejercicio de los deberes de protección establecidos por las leyes para la guarda de los menores, cuando estos queden privados de la necesaria asistencia moral o material». Para apreciar la situación de desamparo se han de examinar minuciosamente las circunstancias específicas de cada caso concreto, teniendo en cuenta fundamentalmente el interés del menor, sin desconocer la necesaria protección de la situación familiar a que pertenece dicho menor, por lo que se hace necesario estimar que la asistencia moral y material de los menores, en orden a la declaración de desamparo, ha de merecer una interpretación de sus relaciones paterno-filiales, de forma que se estima la existencia de desamparo cuando se acredite efectivamente el incumplimiento de unos mínimos de atención al menor exigidos por la conciencia social más común.

Efectivamente, la patria potestad debe entenderse, al menos desde una consideración estrictamente jurídica, como una institución primordialmente dirigida a prestar la necesaria protección, en un sentido muy amplio, de los hijos sometidos a ella, y así ha de inferirse de la regulación que de la misma se contiene en el Código Civil, resultando de obligada cita lo que dispone en su primera parte el art. 154 CC, cuando expresa que «la patria potestad, como responsabilidad parental, se ejercerá siempre en interés de los hijos, y comprende los siguientes deberes y facultades: 1.º Velar por ellos, tenerlos en su compañía, alimentarlos, educarlos y procurarles una formación integral», de modo que el art. 158 siguiente prescribe que «el Juez, a instancia del propio hijo, de cualquier pariente o del Ministerio Fiscal, dictará: las medidas convenientes para asegurar la prestación de alimentos y proveer a las futuras necesidades del hijo», no siendo tampoco ocioso remitirse a lo dispuesto en el art. 142 del mismo texto respecto del concepto de alimentos: «Se entiende por alimentos todo lo que es indispensable para el sustento, habitación, vestido y asistencia médica. Los alimentos comprenden también la educación e instrucción del alimentista mientras sea menor de edad y aun después cuando no haya terminado su formación por causa que no le sea imputable», debiendo resaltarse de igual modo el significado de aquel término –indispensable–, que es igual a todo aquello que es necesario que suceda porque no se puede dispensar o excusar, deberes aquellos de tan gran importancia que el legislador no duda en considerar en situación de desamparo legal al menor respecto del que no se cumplan los mismos, siendo de destacar, conforme al art. 172 CC, que la situación de desamparo ya no solo se origina en el supuesto de incumplimiento de los antedichos deberes, sino que es suficiente en los supuestos de «inadecuado ejercicio» cuando los menores estén privados de la necesaria asistencia moral o material, en cuyo caso la protección debe ser encomendada a la entidad pública correspondiente.

La situación de desamparo fue declarada en fecha [FECHA] y de lo actuado resulta evidente que a tal fecha el cumplimiento por parte de [ELEGIR: la progenitora / el progenitor] de [NOMBRE Y APELLIDOS] de sus deberes era imposible o inadecuado.

Así se infiere del contenido de los múltiples informes que obran documentados en el expediente administrativo, emitidos por los servicios correspondientes de protección de menores: [RELACIÓN DE INFORMES, por ejemplo: el del Equipo Técnico del Servicio de Protección de Menores de [LOCALIDAD], en el que se califica la situación de desprotección absoluta; el del servicio de Neonatología del Hospital [DENOMINACIÓN] de [LOCALIDAD], en el que se informa del hecho del nacimiento del menor con síndrome de abstinencia; el de la Trabajadora Social del Ayuntamiento de [LOCALIDAD], en el que se informa de los hábitos de consumo del progenitor; el de [DENOMINACIÓN] del Equipo de recepción, estudio y diagnóstico de casos, en el que se alude a su personalidad agresiva pese a que se reconoce el inicio del proceso de desintoxicación; el de [DENOMINACIÓN] del Programa de Intervención Familiar del Ayuntamiento de [LOCALIDAD], en el que se insiste en la actitud agresiva; o el propio informe del Centro Comarcal de Drogodependientes, en el cual se destaca la personalidad antisocial, agresivo-sádica de [ELEGIR: el demandante / la demandante], la existencia de rasgos de un trastorno paranoide y la presencia de un pensamiento psicótico.] (Adáptese a los informes que consten realmente en el expediente administrativo.)

Con independencia de que la valoración sobre la corrección de la decisión adoptada ha de hacerse en relación con el momento en que se dicta y no atendiendo a hechos posteriores, no fue en consecuencia la toxicomanía la única razón de tal decisión, sino que sin duda influyó la personalidad agresiva y los rasgos paranoides y psicóticos detectados en el informe médico.

El favor filii, principio que debe primar en este tipo de resoluciones, aconseja evitar cualquier situación de riesgo que para el desarrollo integral del menor se pudiera presentar, y este fin primordial no puede sacrificarse por el deseo, el interés legítimo o la motivación que para la desintoxicación del progenitor la simple existencia y tenencia del menor puedan representar.

Por lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito y por formulada en tiempo y forma contestación a la demanda, se digne admitirla a trámite y conceder a los autos su curso legal, hasta el dictado de sentencia por la que se declare ajustada a Derecho la resolución dictada el día [FECHA] por [ENTIDAD PÚBLICA COMPETENTE EN MATERIA DE PROTECCIÓN DE MENORES] de [PROVINCIA], que declaraba la situación de desamparo [ELEGIR: del menor / de la menor] [NOMBRE DEL MENOR], confirmando íntegramente dicha resolución.

Es justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Fiscal: [FIRMA]
