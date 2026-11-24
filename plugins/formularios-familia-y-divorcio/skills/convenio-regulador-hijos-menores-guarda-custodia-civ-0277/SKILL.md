---
name: convenio-regulador-hijos-menores-guarda-custodia-civ-0277
description: "Convenio regulador con hijos menores y guarda y custodia exclusiva (propuesta). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Convenio regulador con hijos menores y guarda y custodia exclusiva (propuesta)

> Formulario **CIV-0277** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Propuesta de convenio regulador de separación o divorcio, con hijos menores de edad y reconocimiento de la atribución de la guarda y custodia exclusiva a la madre, y liquidación de la sociedad de gananciales.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Convenio regulador con hijos menores y guarda y custodia exclusiva (propuesta)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Convenio regulador con hijos menores y guarda y custodia exclusiva (propuesta)” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:convenio-regulador-hijos-menores-guarda-custodia-civ-0277`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (17 veces)
- [ ] CALLE (12 veces)
- [ ] FECHA (11 veces)
- [ ] IMPORTE (10 veces)
- [ ] LOCALIDAD (9 veces)
- [ ] DENOMINACIÓN SOCIAL (7 veces)
- [ ] NÚMERO (7 veces)
- [ ] Nº (4 veces)
- [ ] DATOS REGISTRALES (2 veces)
- [ ] REFERENCIA CATASTRAL (2 veces)
- [ ] SUCURSAL (2 veces)
- [ ] LUGAR
- [ ] NOMBRE DE LA SUCURSAL
- [ ] NOMBRE DEL FONDO

## Normas que cita el formulario

- art. 90 Código Civil
- art. 81 Código Civil
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

En [LUGAR], a [FECHA].

REUNIDOS

DE UNA PARTE,

D. [NOMBRE Y APELLIDOS], mayor de edad, vecino de [LOCALIDAD], calle [CALLE], y [ELEGIR: DNI / pasaporte] n.º [NÚMERO].

Y DE OTRA,

Dña. [NOMBRE Y APELLIDOS], mayor de edad, vecina de [LOCALIDAD], calle [CALLE], y [ELEGIR: DNI / pasaporte] n.º [NÚMERO].

Ambas partes intervienen en su propio nombre y derecho, y se reconocen recíprocamente la suficiente capacidad legal y legitimación para otorgar la presente PROPUESTA DE CONVENIO REGULADOR, de conformidad con lo establecido en el artículo 90 del Código Civil.

EXPONEN

1. Que los comparecientes contrajeron matrimonio [ELEGIR: civil / canónico], en la ciudad de [LOCALIDAD], el día [FECHA], figurando dicho matrimonio inscrito en el Registro Civil de [LOCALIDAD].

2. Que de dicho matrimonio han nacido y viven loshijos llamados:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

[NOMBRE Y APELLIDOS], de [Nº] años de edad [FECHA], inscrito en el Registro Civil de [LOCALIDAD], en el [DATOS REGISTRALES].

3. Debido a la situación de quiebra en la convivencia conyugal, ambos esposos acordaron suspender la misma con fecha [FECHA].

4. El régimen económico matrimonial es [ELEGIR: el de gananciales / el legal foral / convencional]
el de gananciales
el legal fora*ou*l convencional que se hubiera acordado, identificando en este caso las capitulaciones matrimoniales en que se hubiese estipulado).

5. En cumplimiento de lo establecido en [ELEGIR: el apartado 1.º del artículo 81 del Código Civil -separación- / el artículo 86 en relación con el artículo 81.1.º del Código Civil -divorcio-], y en el apartado 2.º del artículo 777 de la Ley de Enjuiciamiento Civil, se acompañará la presente propuesta, a la demanda de [ELEGIR: separación / divorcio solicitados de mutuo acuerdo o por uno de los cónyuges con el consentimiento del otro], para su aprobación por la autoridad judicial, y a tal fin:

ACUERDAN

I.- Patria potestad

La patria potestad se ejercerá conjuntamente por ambos progenitores, actuando siempre en beneficio de sus hijos y de acuerdo con su personalidad. No obstante, serán válidos los actos realizados por cualquiera de ellos en situaciones de urgente necesidad, poniendo los hechos inmediatamente en conocimiento del otro.

II.- Guarda y custodia de los hijos

La guarda y custodia de los hijos se atribuye a la madre, con la que convivirán (o en su caso al padre, sin perjuicio de que quepa la posibilidad de convenir una guarda y custodia compartida).

III.- Comunicaciones y estancias

III.1. El padre podrá estar en compañía de sus hijos de la manera siguiente:

a) Semanal: El padre podrá tener consigo a los hijos un fin de semana de cada dos, de sábado por la mañana a domingo por la tarde, recogiéndolos y devolviéndolos en el domicilio de la madre, en horas que respeten el horario habitual de los niños.

Podrá igualmente tener consigo a los hijos una tarde entre semana, entre martes o jueves, a convenir entre los padres, recogiéndolos en el colegio, y depositándolos en el domicilio de la madre.

b) Periodos de vacaciones: Por Navidad, los hijos pasarán la mitad de sus vacaciones escolares con el padre y la mitad con la madre, rotando éstos anualmente el período que pasarán con cada uno, empezando este año con la primera porción con la madre y la segunda con el padre, sin perjuicio de intercambiarse el turno por acuerdo de los padres.

En Semana Santa, los hijos pasarán un año con el padre y otro con la madre en años alternos.

Durante el período de vacaciones de verano escolares, correspondiente a los meses de julio y agosto, pasarán los hijos un mes con el padre y otro con la madre, a convenir entre éstos con la suficiente antelación, y caso de desacuerdo, la madre elegirá los años pares y el padre los impares.

III.2. Como régimen de visitas a favor de los abuelos se establece el siguiente (si se considera necesario):

c) En general: En los fines de semana y periodos vacacionales en que al padre corresponda tener consigo a los hijos, si el mismo estuviera fuera de la localidad, como ocurre por motivos laborales, podrán encargarse de tener consigo a aquéllos los abuelos paternos, D. y D.ª [NOMBRE Y APELLIDOS], quienes les recogerán y devolverán en el domicilio de la madre, como sea de costumbre, pudiendo pasar estos periodos los menores en el domicilio, bien del padre, bien en el de los abuelos.
d) Semanal: Una tarde de la semana, de martes a jueves, aparte de la que haya elegido el padre por corresponderle, los abuelos paternos podrán tener en su compañía a los hijos, tomándolos a la salida del colegio y devolviéndolos antes de las 22.00 horas al domicilio de la madre.

III.3. Normas generales.

e) Se favorecerán las relaciones de los hijos, no sólo con los abuelos paternos, como se regula, sino con los parientes del padre, en especial, el hermano menor de la abuela paterna, D. [NOMBRE Y APELLIDOS] y su esposa, así como con la abuela materna D.ª [NOMBRE Y APELLIDOS].
f) Las visitas pactadas como semanales ordinarias se suspenderán durante los periodos de vacaciones.
g) El padre o abuelo que se encuentre con los hijos permitirá y facilitará en todo momento la comunicación con cualquiera de los progenitores, otros abuelos, parientes y allegados de la familia, siempre que ésta no se produzca de forma caprichosa, injustificada o fuera de las horas normales para ello.
h) Cualquiera de los padres o abuelos que traslade a los menores de un lugar conocido a otro desconocido, lo comunicará a los demás, y dará también el nuevo teléfono, si lo hubiere.
i) En caso de enfermedad de los hijos, cualquiera de los progenitores deberá comunicárselo al otro, y en caso de estancia con los abuelos, comunicárselo a los dos padres, permitiendo la visita en el domicilio al padre o abuelo que lo interese y, en todo caso, deberá considerarse la opinión de padres y abuelos en lo relativo a médicos, tratamientos, hospitales, etc.
j) Los progenitores se comprometen a interpretar este convenio tomando siempre en consideración el interés y protección de los menores, y a evitar cualquier actitud que afecte el cariño y respeto de los hijos hacia ambos padres, y hacia cualquiera de sus abuelos.

IV.- Atribución del uso de la vivienda familiar

Se atribuye a D.ª [NOMBRE Y APELLIDOS] y sus hijos el uso de la vivienda familiar sita en la calle [CALLE], así como el uso del ajuar familiar en ella existente (o en su caso al padre, por ser a quien corresponde la guarda y custodia de los hijos).

V.- Alimentos y sustento de los hijos menores de edad

Se fija la cantidad de [IMPORTE] euros ( €) mensuales en concepto de contribución del padre (o en su caso la madre) a los alimentos para sus hijos. Dicha cantidad será ingresada mensualmente, por meses anticipados, dentro de los cinco primeros días de cada mes, en la cuenta corriente núm. [Nº] de la entidad [DENOMINACIÓN SOCIAL], oficina [SUCURSAL], sita en la calle [CALLE].

Esta cantidad será revisada anualmente en proporción a las variaciones del Índice de Precios al Consumo General que publique el Instituto Nacional de Estadística o cualquier otro organismo público que en el futuro pudiera cumplir análoga misión.

Los gastos extraordinarios de los hijos, de naturaleza médica, no cubiertos por la Seguridad Social, y los relativos a los libros de texto y matrículas, serán abonados por mitad por ambos progenitores, y los relativos a gastos por clases extraordinarias de repaso, viajes escolares de los menores serán a cargo, por mitad, de ambos progenitores, siempre que previamente se haya prestado su conformidad o así vengan recomendados por el centro escolar, caso contrario serán sufragados por el progenitor que haya decidido su realización. Cualesquiera otros deberán ser pactados previamente.

El préstamo hipotecario que grava la vivienda familiar será abonado mensualmente por mitad por ambos cónyuges. A tal efecto D./D.ª [NOMBRE Y APELLIDOS], ingresará la cantidad correspondiente en la c/c núm. [Nº] de la entidad [DENOMINACIÓN SOCIAL], oficina [SUCURSAL], sita en la calle [CALLE], hasta la total amortización de la referida carga.

VI.- Compensación por desequilibrio

Ambos cónyuges manifiestan que pueden atender a sus propias necesidades con sus respectivos ingresos, por lo que no es preciso que se fije cantidad alguna en concepto de pensión.

(o bien indicar la pensión que se estime conveniente que puede señalarse con carácter temporal: "D. abonará a D.ª [NOMBRE Y APELLIDOS] en concepto de pensión compensatoria la cantidad de [IMPORTE] euros (€) mensuales. Dicha cantidad será ingresada mensualmente y revisada anualmente a tenor de lo establecido en el apartado anterior para los alimentos.")

VII.- Liquidación del régimen económico matrimonial (en su caso)

Los comparecientes acuerdan la disolución del régimen económico matrimonial, y su liquidación conforme a las siguientes reglas:

A) INVENTARIO

Activo:

1º. Bienes muebles:

[OPCIONAL — incluir si procede]

- acciones de la entidad [DENOMINACIÓN SOCIAL], sita en la calle [CALLE] a nombre de D./D.ª [NOMBRE Y APELLIDOS], cuyo valor a fecha [FECHA] es de: [IMPORTE] €.

[OPCIONAL — incluir si procede]

- Fondo de inversión [NOMBRE DEL FONDO] número [NÚMERO] de la entidad [DENOMINACIÓN SOCIAL] sita en la calle [CALLE] a nombre de D./D.ª [NOMBRE Y APELLIDOS], cuyo importe a fecha [FECHA] es de: [IMPORTE] €.

[OPCIONAL — incluir si procede]

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

- Cuenta Corriente número [NÚMERO] de la entidad [DENOMINACIÓN SOCIAL], sucursal [NOMBRE DE LA SUCURSAL], sita en la calle [CALLE] a nombre de D./D.ª [NOMBRE Y APELLIDOS], cuyo importe a fecha [FECHA] es de: [IMPORTE] €.

2º. Bienes inmuebles:

- Vivienda que constituye el domicilio familiar, sita en la calle [CALLE].

Título.- Les corresponde a los comparecientes por compra, constante el matrimonio, a [NOMBRE Y APELLIDOS], según escritura pública otorgada ante el Notario de [LOCALIDAD], el día [FECHA], con el n.º [NÚMERO] de su protocolo.

Inscripción. Inscrita en el Registro de la Propiedad n.º [NÚMERO] de [LOCALIDAD] al l.

Cargas: Se halla gravada con la hipoteca que se describe en el pasivo.

Ref. Catastral: [REFERENCIA CATASTRAL].

Valoración: Se valora, según tasación solicitada por ambos cónyuges, en la cantidad de [IMPORTE] €.

[OPCIONAL — incluir si procede]

- Vivienda sita en la calle [CALLE].

Título. Les corresponde a los comparecientes por compra, constante el matrimonio, a [NOMBRE Y APELLIDOS], según escritura pública otorgada ante el Notario de [LOCALIDAD], el día [FECHA], con el n.º [NÚMERO] de su protocolo.

Inscripción. Inscrita en el Registro de la Propiedad nº [Nº]. de [LOCALIDAD] al [DATOS REGISTRALES].

Cargas: Se halla libre.

Ref. Catastral: [REFERENCIA CATASTRAL].

Valoración: Se valora, según tasación solicitada por ambos cónyuges, en la cantidad de [IMPORTE] €.

Pasivo:

[OPCIONAL — incluir si procede]

- Préstamo con garantía hipotecaria sobre la vivienda que se describe en el n.º 5 del activo, a favor de la entidad [DENOMINACIÓN SOCIAL] sita en la calle [CALLE], cuyo importe no satisfecho a fecha [FECHA] es de: [IMPORTE] €.

[OPCIONAL — incluir si procede]

- Préstamo personal concedido por la entidad [DENOMINACIÓN SOCIAL] sita en la calle [CALLE], cuyo importe pendiente de pago a fecha [FECHA] es de: [IMPORTE] €.

B) EL TOTAL DE LOS BIENES INVENTARIADOS DEDUCIDO EL PASIVO DEL ACTIVO DE LA SOCIEDAD IMPORTA LA CANTIDAD DE: [IMPORTE] €.

C) LIQUIDACIÓN Y REPARTO

A D./D.ª [NOMBRE Y APELLIDOS] se le adjudica:

a) La copropiedad al 50 % de la finca descrita en los bienes del activo.

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

b) El importe total de los depósitos en Bolsa y del Fondo de Inversiones, descritos en elactivo.

[OPCIONAL — incluir si procede]

c) El importe total de la cuenta corriente descrita en el activo.

[OPCIONAL — incluir si procede]

d) Corresponde al adjudicatario el abono total del préstamo personal descrito en el pasivo.

A D./D.ª [NOMBRE Y APELLIDOS] se le adjudica:

a) La copropiedad al 50% de la finca descrita en el activo, en régimen de uso y disfrute, hasta que los menores alcancen independencia económica, en cuyo momento, salvo acuerdo en contrario de prórroga, se procederá a su venta.

[OPCIONAL — incluir si procede]

b) La propiedad total de la finca descrita en el activo.

[OPCIONAL — incluir si procede]

c) El importe total de la cuenta corriente descrita en el activo.

En prueba de conformidad con todo lo acordado, firman los comparecientes el presente documento por triplicado y en todas sus hojas, en el lugar y fecha al principio indicados, quedando un ejemplar para cada cónyuge, y otro a los efectos de su aportación al Tribunal, junto con la demanda de [ELEGIR: separación / divorcio].

Firma

Firma

D. Dña. [NOMBRE Y APELLIDOS]

========================================================================
