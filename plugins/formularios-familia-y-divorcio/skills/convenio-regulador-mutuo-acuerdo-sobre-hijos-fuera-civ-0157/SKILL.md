---
name: convenio-regulador-mutuo-acuerdo-sobre-hijos-fuera-civ-0157
description: "Convenio regulador de mutuo acuerdo sobre hijos fuera de matrimonio y de pareja estable (Cataluña). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Convenio regulador de mutuo acuerdo sobre hijos fuera de matrimonio y de pareja estable (Cataluña)

> Formulario **CIV-0157** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Convenio regulador de mutuo acuerdo sobre hijos fuera de matrimonio y de pareja estable (Cataluña)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Convenio regulador de mutuo acuerdo sobre hijos fuera de matrimonio y de pareja estable (Cataluña)” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:convenio-regulador-mutuo-acuerdo-sobre-hijos-fuera-civ-0157`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] AÑO (2 veces)
- [ ] DÍA (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] MES (2 veces)
- [ ] LUGAR
- [ ] NOMBRE DEL CENTRO
- [ ] NOMBRE DEL MENOR

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

En [LUGAR], a [DÍA] de [MES] de [AÑO].

DICEN

Que, como consecuencia de las relaciones habidas entre ambos, los comparecientes son los progenitores del menor [NOMBRE DEL MENOR], nacido en [LOCALIDAD] el día [DÍA] de [MES] de [AÑO].

Que nunca han tenido entre ambos una relación afectiva estable.

Que ambos han acordado proponer para su homologación, y en lo que respecta a las relaciones parentales con su hijo/a, de acuerdo con lo establecido en el artículo 233.9 del Código civil catalán, los siguientes:

PACTOS

Decisiones relativas a la guarda y al lugar de residencia (Art. 233-9.2a)

Los padres acuerdan la guarda compartida del hijo menor, cuya distribución se llevará a cabo por periodos de semanas alternas, viviendo el hijo en el domicilio de cada uno de los progenitores de acuerdo con el periodo establecido.

Tareas de las que se responsabilizará cada progenitor relativas a las actividades cotidianas del menor. (Art. 233-9.2b)

Mientras no se acuerde lo contrario, los progenitores son los principales responsables del cuidado del hijo común, y cada uno se hará cargo, por él mismo o a través de otras personas por él designadas, de las tareas domésticas necesarias para el cuidado del hijo menor mientras lo tenga en su compañía.

Igualmente, cada progenitor se hará cargo, por sí mismo o mediante otras personas que designe, de llevar al menor a su centro escolar y a las actividades extraescolares, así como de recogerlo mientras esté en su compañía.

Forma en que se realizarán los cambios en la guarda. Art. 233-9.2c).

Los intercambios se llevarán a cabo los domingos de cada semana a las 20 hs en el domicilio del progenitor donde el menor vaya a residir dicha semana, lugar al que tendrá que llevarlo el progenitor que lo haya tenido en su compañía la semana anterior.

Si un progenitor, por cualquier causa, no pudiera hacer efectiva la guarda que tiene asignada, es responsable de encontrar un sistema alternativo de guarda para el menor.

Igualmente, el progenitor que solicite un cambio en la guarda es responsable de cualquier gasto adicional que pueda derivarse del citado cambio.

Régimen de relación y comunicación con los hijos durante los periodos en que un progenitor no lo tenga en su compañía. (Art. 233-9.2d).

Dada la alternancia pactada en el presente régimen de guarda y custodia, el progenitor con quien no esté el hijo durante la semana correspondiente, podrá comunicarse con él por teléfono, siempre y cuando se respete el horario de descanso del menor, del otro progenitor, y si es el caso, del resto de la familia.

Régimen de estancia del menor con cada progenitor en días festivos, vacaciones y fechas señaladas. (Art. 233-9.2e).

1) Vacaciones de verano:

Con independencia del progenitor a quien pueda corresponder la guarda del menor, cada progenitor podrá tenerlo en su compañía la mitad de los periodos vacacionales escolares de verano. En defecto de acuerdo el padre lo tendrá en su compañía el primer periodo los años pares y la madre los impares.

Al finalizar el periodo vacacional, el reinicio habitual del régimen de guarda semanal le corresponderá al progenitor que no haya estado con el menor en el último periodo vacacional.

2) Vacaciones de Navidad:

Cada progenitor tendrá al menor en su compañía la mitad de los periodos vacacionales escolares de Navidad. En defecto de acuerdo el padre lo tendrá en su compañía el primer periodo los años pares y la madre los impares.

Al finalizar el periodo vacacional, el reinicio habitual del régimen de guarda semanal le corresponderá al progenitor que no haya estado con el menor en el último periodo vacacional.

3) Vacaciones de invierno/Semana Blanca

Cada progenitor tendrá al menor en su compañía la mitad de las vacaciones de invierno. En defecto de acuerdo el padre lo tendrá en su compañía la primera parte de la semana los años pares y la madre los impares.

Al finalizar el periodo vacacional, el reinicio habitual del régimen de guarda semanal le corresponderá al progenitor que no haya estado con el menor en el último periodo vacacional.

4) Vacaciones de Semana Santa:

Cada progenitor tendrá al menor en su compañía la mitad de las vacaciones de Semana Santa. En defecto de acuerdo el padre lo tendrá en su compañía la primera parte de dicho periodo vacacional escolar los años pares y la madre los impares.

Al finalizar el periodo vacacional, el reinicio habitual del régimen de guarda semanal le corresponderá al progenitor que no haya estado con el menor en el último periodo vacacional.

5) Días señalados

En los días de cumpleaños del menor o de los progenitores, prevalecerá el acuerdo al que lleguen, y a falta de acuerdo se aplicará el régimen de comunicación y relaciones previsto con carácter general.

6) Vacaciones y viajes con el menor

Cada progenitor puede viajar con el menor durante los periodos que el mismo esté bajo su guarda, comunicándolo previamente al otro progenitor.

El progenitor que tenga el pasaporte o documentación preceptiva del menor lo deberá facilitar al otro progenitor.

Decisiones relativas a la educación y a las actividades extraescolares, formativas y de ocio (Art. 233-9.2f).

Los progenitores han acordado que el menor cursará sus estudios en el Colegio [NOMBRE DEL CENTRO]

Mientras los hijos residan con cualquier progenitor, éste podrá autorizar que participen en las actividades que no requieran organización previa, así como en las actividades sociales y de ocio propias de su edad.

Se requerirá el acuerdo de ambos progenitores para inscribir al menor en cualquier actividad deportiva o de cualquier otro tipo que requieran un entrenamiento especial mientras el hijo se encuentre en compañía del otro progenitor.

Deberes de información y consulta entre los progenitores en relación con los hijos. (Art. 233-9.2g)

Cada progenitor debe informar al otro de los aspectos relativos a la salud, educación y ocio del menor.

Ambos progenitores se deberán intercambiar y tendrán acceso a los documentos relevantes del menor.

Toda información relativa al menor se habrá de intercambiar entre los progenitores, quienes en ningún caso podrán utilizar al menor como mensajero para transmitir información, plantear preguntas o proponer cambios.

Decisiones relativas al cambio de domicilio y otras cuestiones relevantes para el menor. (Art. 233-9.2h)

Cada progenitor habrá de comunicar al otro, con un preaviso mínimo de treinta días su intención de cambiar de domicilio.

Si el cambio de domicilio de un progenitor es incompatible con el régimen de guarda o de visitas establecido, los progenitores habrán de revisar el acuerdo del presente plan de parentalidad con la finalidad de alcanzar un acuerdo que se adapte lo mejor posible a las necesidades del menor.

El menor permanecerá con el progenitor que permanezca en el domicilio inicial hasta que los progenitores alcancen un acuerdo alternativo.

Si un progenitor tiene conocimiento de cualquier enfermedad, accidente, hospitalización o cualquier otra circunstancia que afecte a la salud del menor, debe comunicarlo inmediatamente al otro progenitor.

Modificaciones, revisión del plan y recurso a la mediación familiar

Los progenitores acuerdan el recurso a la mediación familiar en el supuesto de que la aplicación del plan provoque diferencias entre los progenitores, o deba modificarse su contenido con la finalidad de adaptarlo a las nuevas necesidades de las diferentes etapas de la vida de los hijos o a las nuevas circunstancias de los progenitores.

Alimentos

Los progenitores, dado el régimen de custodia compartida, abonarán los gastos corrientes de alimentación del menor en los periodos que convivan con él.

Por lo que respecta al resto de gastos de naturaleza ordinaria de éste incluidos en los alimentos, tales como gastos de comedor del colegio, ropa, calzado, libros de texto, matriculas, material escolar, etc. serán igualmente abonados por mitad por ambos progenitores.

A dichos efectos los progenitores procederán a aperturar una cuenta bancaria con régimen de disposición mancomunada en la que ingresarán la cantidad de DOSCIENTOS EUROS MENSUALES cada uno de ellos, y desde la que se abonarán los gastos de la menor, domiciliándose en la misma el importe de la mensualidad del comedor escolar.

Dicha cantidad será actualizada anualmente con arreglo al I.P.C. general que se publique por el Instituto Nacional de Estadística u organismo que en su defecto le sustituya.

Por lo que respecta a los gastos extraordinarios del menor, los padres acuerdan abonarlos por mitad. Tendrán consideración de tales, entre otros necesarios, los gastos médicos no cubiertos por la Seguridad Social, los de ortodoncia, óptica, ortopedia, logopedia, psicología y cualquier otro gasto de tipo médico o farmacológico que no estuviere amparado por las coberturas de la Seguridad Social; así mismo los padres acuerdan considerar gastos extraordinarios los de actividades extraescolares de la menor, que serán abonados por mitad siempre que exista acuerdo entre ellos al igual que ocurrirá con aquellos otros gastos extraordinarios que los progenitores consideren convenientes para la menor.

Relaciones con los abuelos

El menor se relacionará con los abuelos paternos y maternos en durante los periodos que se encuentre en compañía de sus respectivos progenitores.

Ambas partes se comprometen a realizar los actos necesarios y a suscribir cuantos documentos públicos y privados sean preceptivos para cumplir y ejecutar los acuerdos a que han llegado en el presente documento.

Leído por ambas partes, lo encuentran conforme y se afirman, ratifican y firman en [LOCALIDAD] en el día de la fecha.

Firma progenitor

Firma progenitora

========================================================================
