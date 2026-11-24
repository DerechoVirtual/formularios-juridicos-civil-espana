---
name: convenio-regulador-separacion-segun-derecho-civil-civ-0283
description: "Convenio regulador de separación según el Derecho civil de Cataluña. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Convenio regulador de separación según el Derecho civil de Cataluña

> Formulario **CIV-0283** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Convenio regulador de separación matrimonial conforme al Derecho Civil especial de Cataluña.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Convenio regulador de separación según el Derecho civil de Cataluña» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Convenio regulador de separación según el Derecho civil de Cataluña” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:convenio-regulador-separacion-segun-derecho-civil-civ-0283`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] ACUERDO ALCANZADO (12 veces)
- [ ] LOCALIDAD (10 veces)
- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] FECHA (4 veces)
- [ ] CALLE (3 veces)
- [ ] DATOS REGISTRALES (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] LUGAR (2 veces)
- [ ] Nº (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] NOMBRE DEL HIJO/A
- [ ] Nº DE CUENTA (IBAN)

## Normas que cita el formulario

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

Notas al pie del formulario original:
(1) Existe una guía y un modelo del plan de parentalidad, elaborados, con carácter meramente indicativo, y facilitados por la Dirección General de Derecho y Entidades Jurídicas de la Generalitat de Cataluña, en cumplimiento de la Disposición adicional 9.ª de la Ley 25/2010, de 29 de julio, del Libro II del Código civil de Cataluña, relativo a la persona y a la familia, que está disponible en la web del ICAB (véase modelo de plan de parentalidad).

(2) Si hubiera hermanos que no convivan en el mismo domicilio podrá también acordarse un régimen de relaciones personales entre ellos.

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

En [LUGAR], a [FECHA].

REUNIDOS

DE UNA PARTE,

D. [NOMBRE Y APELLIDOS], mayor de edad, vecino de [LOCALIDAD], calle [CALLE] y D.N.I. núm. [NÚMERO].

Y DE OTRA,

Dña. [NOMBRE Y APELLIDOS], mayor de edad, vecina de [LOCALIDAD], calle [CALLE] y D.N.I. núm. [NÚMERO].

MANIFIESTAN

I. Que los comparecientes contrajeron matrimonio [ELEGIR: civil / canónico], en la ciudad de [LOCALIDAD], el día [FECHA], figurando dicho matrimonio inscrito en el Registro Civil de [LOCALIDAD], [DATOS REGISTRALES].

II. Que de dicho matrimonio ha nacido y vive un hijo llamado [NOMBRE DEL HIJO/A], de [Nº] años de edad, inscrito en el Registro Civil de [LOCALIDAD], en el [DATOS REGISTRALES].

III. Que el régimen económico del matrimonio es el de separación de bienes, ya que por residencia y lugar de celebración del matrimonio la vecindad de los cónyuges es la catalana, no habiéndose otorgado nunca capitulaciones matrimoniales.

IV. Que debido a la situación de quiebra en la convivencia conyugal, ambos esposos acordaron suspender la misma con fecha [FECHA] e iniciar las actuaciones judiciales para legalizar esta situación.

V. Que formalizan este convenio regulador, de acuerdo con lo que disponen el artículo 233-2 del Código civil de Cataluña y de conformidad con los siguientes:

PACTOS

I.- SEPARACIÓN CONYUGAL.

Los cónyuges acuerdan separarse desde el momento de la firma de este convenio.

II.- PLAN DE PARENTALIDAD.

Los cónyuges acuerdan el siguiente plan de parentalidad para el ejercicio de las responsabilidades parentales con respecto a la guarda, cuidado y educación del hijo común, conforme a lo establecido en el art. 233-9 del Código Civil de Cataluña:

A) Decisiones relativas a la guarda y al lugar donde vivirá habitualmente el hijo [ACUERDO ALCANZADO].
B) Tareas de que debe responsabilizarse cada progenitor con relación a las actividades cotidianas del hijo [ACUERDO ALCANZADO].
C) Forma en que deben hacerse los cambios en la guarda [ACUERDO ALCANZADO].
D) Régimen de relación y comunicación con el hijo durante los períodos en que un progenitor no lo tenga con él [ACUERDO ALCANZADO].
E) Régimen de estancias del hijo con cada uno de los progenitores en períodos de vacaciones y en fechas especialmente señaladas para el hijo, para los progenitores o para su familia [ACUERDO ALCANZADO].
F) Decisiones relativas a la educación y a las actividades extraescolares, formativas y de tiempo libre [ACUERDO ALCANZADO].
G) Deberes de información y consulta entre los progenitores sobre la educación, la salud y el bienestar del hijo [ACUERDO ALCANZADO].
H) Decisiones relativas al cambio de domicilio y a otras cuestiones relevantes para el hijo [ACUERDO ALCANZADO].
I) Modificaciones, revisiones del plan y recurso a la mediación familiar [ACUERDO ALCANZADO].

III.- RÉGIMEN DE RELACIONES PERSONALES CON LOS ABUELOS (en su caso).

[OPCIONAL — incluir si procede]

Por lo que respecta al régimen de relaciones personales con los abuelos, se fija lo siguiente: [ACUERDO ALCANZADO].

IV.- ATRIBUCIÓN DEL USO DE LA VIVIENDA Y AJUAR FAMILIAR.

Se atribuye a Dña. [NOMBRE Y APELLIDOS] y su hijo el uso de la vivienda familiar sita en la calle [CALLE], así como el uso del ajuar familiar en ella existente.

V.- LIQUIDACIÓN DEL RÉGIMEN ECONÓMICO MATRIMONIAL Y DIVISIÓN DE LOS BIENES EN COMUNIDAD ORDINARIA INDIVISA.

[OPCIONAL — incluir si procede]

No procede acordar nada en relación a la liquidación del régimen económico matrimonial dado que el régimen económico que rige el matrimonio es el de separación de bienes.

[OPCIONAL — incluir si procede]

(Opción 2.ª. Puede incluirse una cláusula acordando la liquidación de la comunidad ordinaria de bienes ostentada por ambos cónyuges, en cuyo caso se indicará: [ACUERDO ALCANZADO])

"En cuanto a la liquidación del régimen económico matrimonial, los cónyuges reconocen no haber otorgado capitulaciones matrimoniales por lo que el matrimonio se rige por el régimen legal foral de separación de bienes establecido por el art. 231-10 del Código civil de Cataluña.

No obstante, ambos cónyuges son cotitulares en mitades y proindiviso de los inmuebles que se especificarán a continuación, y acuerdan extinguir, en la forma que se dirá, la comunidad indivisa existente hasta ahora:

1) Piso sito en [LOCALIDAD]
2) Piso sito en [LOCALIDAD]

A) La esposa, Doña [NOMBRE Y APELLIDOS], recibe la mitad indivisa, propiedad de su consorte, del piso sito en [LOCALIDAD], con la siguiente descripción registral:

B) El esposo, Don [NOMBRE Y APELLIDOS], recibe la mitad indivisa, propiedad de su consorte, del piso sito en [LOCALIDAD], con la siguiente descripción registral:

El presente convenio implica tradición de los mencionados condominios, sin que sea necesario proceder a posterior transferencia física a favor de los respectivos adquirentes en cuanto a la mitad indivisa propiedad del cedente en concepto de condueño, por cuanto aquéllos ya se hallaban en posesión y disfrute del bien, y a partir de este momento y conforme a lo aquí convenido, consolidan el pleno dominio de dichos bienes, por lo que ambas partes solicitan al Registrador de la Propiedad que en cada caso corresponda la inscripción de los presentes títulos, en cuanto implica la transmisión de la mitad indivisa de los bienes pertinentes al otro cónyuge.

El Ajuar, enseres, mobiliario y equipamiento de la vivienda familiar, ya han sido repartidos en lotes iguales, habiendo retirado el esposo en fechasu parte."

[OPCIONAL — incluir si procede]

(Opción 3.ª. En el caso de que existan bienes en comunidad ordinaria, y se quiera permanecer en la indivisión, puede indicarse: [ACUERDO ALCANZADO])

"El único patrimonio común de ambos cónyuges lo constituye el domicilio familiar, sito en [LOCALIDAD], acordando los cónyuges por el momento mantener la copropiedad del mismo."

VI.- ALIMENTOS Y GASTOS EXTRAORDINARIOS PARA EL HIJO MENOR.

En concepto de alimentos para el hijo, [ELEGIR: el padre / la madre] pagará una pensión mensual de [IMPORTE] euros que se actualizará anualmente de acuerdo con la variación del Índice de Precios al Consumo (IPC).

Los gastos extraordinarios del hijo, de naturaleza médica, no cubiertos por la Seguridad Social, y los relativos a los libros de texto y matrículas, serán abonados por mitad por ambos progenitores, y los relativos a gastos por clases extraordinarias de repaso, viajes escolares de los menores serán a cargo, por mitad, de ambos progenitores, siempre que previamente se haya prestado su conformidad o así vengan recomendados por el centro escolar, caso contrario serán sufragados por el progenitor que haya decidido su realización. Cualesquiera otros deberán ser pactados previamente.

VII.- PRESTACIÓN COMPENSATORIA A SATISFACER POR UNO DE LOS CÓNYUGES EN FAVOR DEL OTRO.

Se establece una pensión compensatoria mensual en favor de la esposa de [IMPORTE] euros que tendrá una duración de [Nº] años y se actualizará anualmente de acuerdo con la variación del IPC. Las cantidades que resultan de este pacto y del precedente se harán efectivas por mensualidades anticipadas antes del día 5 de cada mes, mediante el ingreso en la cuenta corriente [Nº DE CUENTA (IBAN)] de [NOMBRE Y APELLIDOS].

VIII.- COMPENSACIÓN ECONÓMICA POR RAZÓN DE TRABAJO.

[OPCIONAL — incluir si procede]

En su caso, si procede

"De acuerdo con lo que dispone el art. 232-5 del Código civil de Cataluña, el marido pagará a favor de la esposa una compensación deeuros por los años de convivencia y por la contribución de la esposa en casa y por los años que ha trabajado en el negocio familiar"

IX.- VIGENCIA DEL CONVENIO REGULADOR.

Ambas partes se comprometen a cumplir estos pactos desde este acto; se obligan a formular solicitud de separación judicial de común acuerdo y a ratificar la petición y este convenio.

En prueba de conformidad con todo lo acordado, firman los comparecientes el presente documento por triplicado y en todas sus hojas, en el lugar y fecha al principio indicados, quedando un ejemplar para cada cónyuge, y otro a los efectos de su aportación al Tribunal, junto con la demanda de separación.

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a

Firma del Procurador/a

D./Dña. [NOMBRE Y APELLIDOS] D./Dña. [NOMBRE Y APELLIDOS]
