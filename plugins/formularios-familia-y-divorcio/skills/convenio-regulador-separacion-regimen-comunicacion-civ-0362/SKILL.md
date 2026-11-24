---
name: convenio-regulador-separacion-regimen-comunicacion-civ-0362
description: "Convenio regulador de separación con régimen de comunicación de los hijos con los abuelos. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Convenio regulador de separación con régimen de comunicación de los hijos con los abuelos

> Formulario **CIV-0362** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Convenio regulador de separación con régimen de comunicación de los hijos con los abuelos» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Convenio regulador de separación con régimen de comunicación de los hijos con los abuelos” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:convenio-regulador-separacion-regimen-comunicacion-civ-0362`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (9 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] FECHA (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] IMPORTE EN CIFRA (2 veces)
- [ ] Nº (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] COLEGIO
- [ ] DIRECCIÓN
- [ ] LUGAR
- [ ] NOMBRE DEL HIJO/A

## Normas que cita el formulario

- art. 81.1.º Código Civil

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

Notas al pie del formulario original:
(1) De conformidad con el artículo 90 CCiv, en la redacción dada por el art. 1.º.2 de la Ley 42/2003 de 21 de noviembre, al proponer los cónyuges en el convenio regulador un régimen de visitas y comunicación de los hijos comunes con sus abuelos, será aprobado judicialmente previa audiencia de los abuelos en cuestión, en la que éstos prestarán su consentimiento.

========================================================================


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

Convenio regulador de separación matrimonial estableciendo un régimen de comunicación de los hijos con sus abuelos.

En [LUGAR], a [FECHA].

REUNIDOS

DE UNA PARTE,

D. [NOMBRE Y APELLIDOS], mayor de edad, casado, con domicilio en [LOCALIDAD], provisto de D.N.I. número [NÚMERO]

Y DE OTRA,

Dña. [NOMBRE Y APELLIDOS], mayor de edad, casada, con domicilio en [LOCALIDAD], provista de D.N.I. número [NÚMERO]

Ambas partes recíprocamente se reconocen la suficiente capacidad legal y legitimación para llevar a efecto el presente convenio regulador de los efectos de su separación, de conformidad con lo establecido en los artículos 81.1.º y 90 del Código Civil, y a tal fin

EXPONEN

PRIMERO.- Que contrajeron matrimonio en [LOCALIDAD] el día [FECHA], inscrito en el Registro Civil de [LOCALIDAD]

SEGUNDO.- Que de dicho matrimonio han nacido y viven los siguientes hijos: de [Nº] años de edad y [NOMBRE DEL HIJO/A] de [Nº] años de edad.

TERCERO.- En el día de hoy, los esposos han otorgado ante el Notario/a del Ilustre colegio de [COLEGIO] D./D.ª [NOMBRE Y APELLIDOS], escritura de capitulaciones matrimoniales, en la que pactan el régimen de separación absoluta de bienes.

CUARTO.- Ante la situación de quiebra de la convivencia conyugal, los esposos han decidido libre y voluntariamente solicitar la separación por los trámites establecidos en el artículo 777 de la Ley de Enjuciamiento Civil, y a tal fin

ACUERDAN

I.- Guarda y custodia de los hijos: Los hijos quedan bajo la guarda y custodia de la madre, con la que convivirán. La patria potestad sobre los hijos será compartida por ambos progenitores.

II.- Comunicaciones, visitas y estancias:

II.1. Como régimen de visitas a favor del padre se establece el siguiente:

a) Semanal: El padre podrá tener consigo a los hijos un fin de semana de cada dos, de sábado por la mañana a domingo por la tarde, recogiéndolos y devolviéndolos en el domicilio de la madre, en horas que respeten el horario habitual de los niños.

Podrá igualmente tener consigo a los hijos una tarde entre semana, entre martes o jueves, a convenir entre los padres, recogiéndolos en el colegio, y depositándolos en el domicilio de la madre.

b) Periodos de vacaciones: Por Navidad, los hijos pasarán la mitad de sus vacaciones escolares con el padre y la mitad con la madre, rotando éstos anualmente el período que pasarán con cada uno, empezando este año con la primera porción con la madre y la segunda con el padre, sin perjuicio de intercambiarse el turno por acuerdo de los padres.

En Semana Santa, los hijos pasarán un año con el padre y otro con la madre en años alternos.

Durante el período de vacaciones de verano escolares, correspondiente a los meses de julio y agosto, pasarán los hijos un mes con el padre y otro con la madre, a convenir entre éstos con la suficiente antelación, y caso de desacuerdo, la madre elegirá los años pares y el padre los impares.

II.2. Como régimen de visitas a favor de los abuelos se establece el siguiente:

c) En general: En los fines de semana y periodos vacacionales en que al padre corresponda tener consigo a los hijos, si el mismo estuviera fuera de la localidad, como ocurre por motivos laborales, podrán encargarse de tener consigo a aquéllos los abuelos paternos, D. y D.ª [NOMBRE Y APELLIDOS], quienes les recogerán y devolverán en el domicilio de la madre, como sea de costumbre, pudiendo pasar estos periodos los menores en el domicilio, bien del padre, bien en el de los abuelos.
d) Semanal: Una tarde de la semana, de martes a jueves, aparte de la que haya elegido el padre por corresponderle, los abuelos paternos podrán tener en su compañía a los hijos del matrimonio, tomándolos a la salida del colegio y devolviéndolos antes de las 22.00 horas al domicilio de la madre.

II.3. Normas generales.

e) Se favorecerán las relaciones de los hijos del matrimonio, no sólo con los abuelos paternos, como se regula, sino con los parientes del padre, en especial, el hermano menor de la abuela paterna, Don [NOMBRE Y APELLIDOS] y su esposa, así como con la abuela materna Doña [NOMBRE Y APELLIDOS]
f) Las visitas pactadas como semanales ordinarias se suspenderán durante los periodos de vacaciones.
g) El padre o abuelo que se encuentre con los hijos del matrimonio permitirá y facilitará en todo momento la comunicación con cualquiera de los progenitores, otros abuelos, parientes y allegados de la familia, siempre que ésta no se produzca de forma caprichosa, injustificada o fuera de las horas normales para ello.
h) Cualquiera de los padres o abuelos que traslade a los menores de un lugar conocido a otro desconocido, lo comunicará a los demás, y dará también el nuevo teléfono, si lo hubiere.
i) En caso de enfermedad de los hijos del matrimonio, cualquiera de los progenitores deberá comunicárselo al otro, y en caso de estancia con los abuelos, comunicárselo a los dos padres, permitiendo la visita en el domicilio al padre o abuelo que lo interese y, en todo caso, deberá considerarse la opinión de padres y abuelos en lo relativo a médicos, tratamientos, hospitales, etc.
j) Los cónyuges se comprometen a interpretar este convenio tomando siempre en consideración el interés y protección de los menores, y a evitar cualquier actitud que afecte el cariño y respeto de los hijos hacia ambos padres, y hacia cualquiera de sus abuelos.

III.- Domicilio conyugal: Se atribuye a D.ª [NOMBRE Y APELLIDOS] y sus hijos el uso de la vivienda familiar sita en la [DIRECCIÓN], así como el uso del ajuar familiar en ella existente.

IV.- Alimentos a los hijos: Se fija la cantidad de [IMPORTE] euros ([IMPORTE EN CIFRA] €) mensuales en concepto de contribución del padre a los alimentos para sus hijos. Dicha cantidad será ingresada mensualmente, por meses anticipados, dentro de los cinco primeros días de cada mes, en la cuenta corriente que la esposa designe.

Esta cantidad será revisada anualmente en proporción a las variaciones del Indice de Precios al Consumo General que publique el Instituto Nacional de Estadística o cualquier otro organismo público que en el futuro pudiera cumplir análoga misión.

V.- Pensión compensatoria: D. abonará a D.ª [NOMBRE Y APELLIDOS] en concepto de pensión compensatoria la cantidad de [IMPORTE] euros ([IMPORTE EN CIFRA] €) mensuales. Dicha cantidad será ingresada mensualmente y revisada anualmente a tenor de lo establecido en el apartado anterior para los alimentos.

VI.- Liquidación de la sociedad de gananciales: Los esposos manifiestan no poseer más bienes de naturaleza ganancial que los muebles y enseres, cuyo reparto ya han convenido.

El presente convenio surte efectos entre las partes desde el día de hoy, y para que así conste, lo firman por duplicado en el lugar y fecha "ut supra".

Firma	Firma
D.	D.ª [NOMBRE Y APELLIDOS]
