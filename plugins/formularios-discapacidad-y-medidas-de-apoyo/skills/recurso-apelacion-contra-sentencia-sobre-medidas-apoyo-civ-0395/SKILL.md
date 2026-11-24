---
name: recurso-apelacion-contra-sentencia-sobre-medidas-apoyo-civ-0395
description: "Recurso de apelación contra la sentencia sobre medidas de apoyo a persona con discapacidad. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Recurso de apelación contra la sentencia sobre medidas de apoyo a persona con discapacidad

> Formulario **CIV-0395** del plugin **Discapacidad y medidas de apoyo (Ley 8/2021)** (`formularios-discapacidad-y-medidas-de-apoyo`) · Civil › Capacidad y medidas de apoyo · normativa revisada el 24-11-2026.

## Qué es

Escrito de interposición de recurso de apelación (arts. 458 y siguientes LEC) contra la sentencia dictada en un proceso de medidas judiciales de apoyo a persona con discapacidad (Ley 8/2021), cuando se estima que la medida acordada, por ejemplo una curatela representativa, no es proporcionada y debería sustituirse por otra menos intensa, como la guarda de hecho. El modelo está redactado con el motivo de error en la valoración de la prueba.

Es un modelo de tipo **recursos**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Recurso de apelación contra la sentencia sobre medidas de apoyo a persona con discapacidad» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Recurso de apelación contra la sentencia sobre medidas de apoyo a persona con discapacidad” para mi caso». También puedes invocarla directamente con `/formularios-discapacidad-y-medidas-de-apoyo:recurso-apelacion-contra-sentencia-sobre-medidas-apoyo-civ-0395`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-discapacidad-y-medidas-de-apoyo:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Discapacidad y medidas de apoyo (Ley 8/2021)) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (5 veces)
- [ ] Nº DE PROCEDIMIENTO (3 veces)
- [ ] AÑO
- [ ] CENTRO O EMPRESA
- [ ] CI
- [ ] DESCRIPCIÓN DE LA CONDICIÓN O PERTURBACIÓN
- [ ] DIAGNÓSTICO
- [ ] DÍA
- [ ] ESPECIALIDAD
- [ ] IMPORTE
- [ ] LOCALIDAD
- [ ] MES
- [ ] NOMBRE Y APELLIDOS
- [ ] NOMBRE Y APELLIDOS DE LA PERSONA REPRESENTADA
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] NOMBRES Y APELLIDOS
- [ ] NOMBRES Y APELLIDOS DE LOS CURADORES
- [ ] NOMBRES Y APELLIDOS DE QUIENES EJERCEN LA GUARDA
- [ ] Nº
- [ ] OTRAS LIMITACIONES CONSTATADAS EN EL INFORME
- [ ] PROVINCIA
- [ ] SEDE

## Normas que cita el formulario

- art. 458 LEC
- art. 268 Código Civil

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

PROCESO DE MEDIDAS DE APOYO A PERSONA CON DISCAPACIDAD Nº [Nº DE PROCEDIMIENTO]

A LA AUDIENCIA PROVINCIAL DE [PROVINCIA]

Don/Doña [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, en nombre y representación de Don/Doña [NOMBRE Y APELLIDOS DE LA PERSONA REPRESENTADA], parte demandada en el presente proceso de MEDIDAS DE APOYO A PERSONA CON DISCAPACIDAD núm. [Nº DE PROCEDIMIENTO], según tengo acreditado en autos, ante la Sala comparezco y como mejor proceda en Derecho, DIGO:

Que, mediante el presente escrito y en la indicada representación, interpongo, en el plazo conferido al efecto, y conforme a los arts. 458 y siguientes LEC, RECURSO DE APELACIÓN contra la sentencia de fecha [FECHA], notificada a esta parte en fecha [FECHA], en base a los siguientes

MOTIVOS

ÚNICO.- ERROR EN LA APRECIACIÓN DE LA PRUEBA.

En fecha [FECHA], en los autos [Nº DE PROCEDIMIENTO] seguidos ante la Sección [ELEGIR: Civil / de Familia, Infancia y Capacidad] del Tribunal de Instancia núm. [Nº] de [SEDE], se declaró a Don/Doña [NOMBRE Y APELLIDOS] afectado/a gravemente para ejercer la capacidad jurídica y de obrar, acordándose como medida la curatela con funciones representativas a favor de [NOMBRES Y APELLIDOS DE LOS CURADORES]. Se aporta como DOCUMENTO NÚM. 1 copia testimoniada de dicha sentencia.

Conforme dispone el artículo 268 del Código Civil, en la redacción dada por la Ley 8/2021, de 2 de junio, las medidas tomadas por la autoridad judicial en el procedimiento de provisión de apoyos serán proporcionadas a las necesidades de la persona que las precise, respetarán siempre la máxima autonomía de esta en el ejercicio de su capacidad jurídica y atenderán en todo caso a su voluntad, deseos y preferencias.

En nuestro caso concreto, nuestro mandante presenta [DESCRIPCIÓN DE LA CONDICIÓN O PERTURBACIÓN] con consecuencias jurídicas. Dicho estado viene caracterizado por los siguientes elementos:

a) Existencia de un trastorno cuya naturaleza y profundidad sean suficientes para justificar dichas repercusiones (criterio psicológico).

b) Permanencia o habitualidad del mismo (criterio cronológico).

c) Que como consecuencia del trastorno resulte la persona incapaz de satisfacer sus propios intereses, es decir, de gobernarse por sí misma.

Así consta acreditado en los informes médicos que, a pesar de no ser vinculantes para el juzgador, constituyen la base de la adopción de las medidas de apoyo, si bien el Juez se encuentra obligado legalmente a verificar personalmente el examen de la persona destinataria de estas medidas de apoyo.

Partiendo de lo que se acaba de referir, de acuerdo con el conjunto de la prueba practicada, nos encontramos con que el informe practicado por el Médico Forense especialista en [ESPECIALIDAD], de fecha [FECHA], señala que mi representado/a padece [DIAGNÓSTICO], con lenguaje y pensamiento coherentes, estado mental lúcido, sin apreciarse trastornos psicóticos ni depresivos. Conoce y asocia la moneda a un valor. Su cociente intelectual sería de [CI].

Así pues, se concluye que tiene un nivel aceptable dentro de su condición, se desenvuelve bien en los aspectos interpersonales y afectivos así como sociales, siendo vulnerable en el control de sus impulsos, en decisiones de trascendencia, en situaciones o conflictos globales [OPCIONAL — especificar: de tipo económico o mercantil] en los que necesita medidas de apoyo.

Ha quedado constatado que mi representado/a desempeña actividad laboral en [CENTRO O EMPRESA], por la que percibe un salario de [IMPORTE] euros mensuales.

En el informe referido se hace mención a que mi representado/a carece de los recursos necesarios para ser autosuficiente en aspectos propios del día a día [OPCIONAL — ejemplos: efectuar la compra diaria, moverse por la ciudad], así como [OTRAS LIMITACIONES CONSTATADAS EN EL INFORME].

Teniendo en cuenta las anteriores consideraciones, no puede considerarse a mi representado/a tributario/a de una situación de curatela, sino de una medida de apoyo como pueda ser la guarda de hecho de [NOMBRES Y APELLIDOS DE QUIENES EJERCEN LA GUARDA] en el ámbito patrimonial y en el campo personal, velando por el mantenimiento de los cuidados socio-sanitarios, con capacidad de decisión en relación con las medidas terapéuticas a adoptar en cada caso concreto.

Por todo lo expuesto,

A LA SALA SUPLICO: que tenga por interpuesto RECURSO DE APELACIÓN contra la sentencia de fecha [FECHA] y por hechas las alegaciones que se contienen, estime íntegramente el recurso de apelación, dictando sentencia en virtud de la cual se revoque la referida sentencia por la que se declaraba a mi representado/a sometido/a a la institución de curatela y, en su virtud, se dicte nueva sentencia por la que se declare como medida de apoyo a favor de mi representado/a la guarda de hecho de [NOMBRES Y APELLIDOS], en el ámbito patrimonial y en el campo personal, velando por el mantenimiento de los cuidados socio-sanitarios con capacidad de decisión en relación con las medidas terapéuticas a adoptar en cada caso concreto.

Es justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma de Abogado/a y de Procurador/a.
