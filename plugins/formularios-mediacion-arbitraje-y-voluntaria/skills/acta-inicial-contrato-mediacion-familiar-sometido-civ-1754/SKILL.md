---
name: acta-inicial-contrato-mediacion-familiar-sometido-civ-1754
description: "Acta inicial o contrato de mediación familiar sometido al Derecho valenciano. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Acta inicial o contrato de mediación familiar sometido al Derecho valenciano

> Formulario **CIV-1754** del plugin **Mediación, MASC, arbitraje y jurisdicción voluntaria** (`formularios-mediacion-arbitraje-y-voluntaria`) · Civil › Jurisdicción voluntaria, MASC, mediación y arbitraje · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Acta inicial o contrato de mediación familiar sometido al Derecho valenciano» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Acta inicial o contrato de mediación familiar sometido al Derecho valenciano” para mi caso». También puedes invocarla directamente con `/formularios-mediacion-arbitraje-y-voluntaria:acta-inicial-contrato-mediacion-familiar-sometido-civ-1754`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-mediacion-arbitraje-y-voluntaria:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Mediación, MASC, arbitraje y jurisdicción voluntaria) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] AÑO (3 veces)
- [ ] IMPORTE (3 veces)
- [ ] Nº (3 veces)
- [ ] DÍA (2 veces)
- [ ] MES (2 veces)
- [ ] LUGAR
- [ ] LUGAR DE LAS SESIONES
- [ ] Nº DE SESIONES

## Normas que cita el formulario

- art. 13.5 Ley 5/2012
- art. 8 Ley 24/2018

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

ACTA INICIAL O CONTRATO DE MEDIACIÓN FAMILIAR SUJETA AL DERECHO VALENCIANO

En [LUGAR], a [DÍA] de [MES] de [AÑO].l año [AÑO]

REUNIDOS:

Los consortes DON/DOÑA [NOMBRE Y APELLIDOS] y DON/DOÑA [NOMBRE Y APELLIDOS], como sujetos mediados.

Y DON/DOÑA [NOMBRE Y APELLIDOS], como profesional mediador.

Ambas partes intervienen en su propio nombre y derecho y se reconocen la capacidad legal suficiente para celebrar el presente CONTRATO DE MEDIACIÓN y a tal efecto,

EXPONEN

DON/DOÑA [NOMBRE Y APELLIDOS] y DON/DOÑA [NOMBRE Y APELLIDOS], que son cónyuges, atravesando su matrimonio por una situación crítica que ha provocado su decisión de solicitar el divorcio y para intentar aproximar posturas y e intentar acordar la organización de los efectos del mismo, han decidido, tras una sesión informativa celebrada en fecha [DÍA] de [MES] de [AÑO] en que se les informó acerca de las características básicas de la mediación, someterse a un proceso de mediación, orientado como persona mediadora, por DON/DOÑA [NOMBRE Y APELLIDOS], que acepta ejercer tal función, conforme a las siguientes

ESTIPULACIONES

OBJETO DE LA MEDIACIÓN:

LUGAR E IDIOMA: Las sesiones de mediación se celebrarán en [LUGAR DE LAS SESIONES]. El/Los idioma/s que se utilizará/n será el/los siguiente/s:

COSTE DE LA MEDIACIÓN Y DISTRIBUCIÓN DEL MISMO:

Redacción del contrato de mediación: [IMPORTE] euros.

Coste por sesión: [IMPORTE] euros.

Otros gastos: [IMPORTE] euros.

Cualquier otro gasto no incluido en los anteriores, p.ej., honorarios de otras personas que asistan como consultores a las sesiones de mediación, deberán ser acordados por las partes.

Las partes deben satisfacer por partes iguales o en la proporción que las partes acuerden los costes de la mediación, con independencia de que se alcance o no un acuerdo como consecuencia de ésta.

Si la persona mediadora lo considera necesario, podrá solicitar una provisión de fondos. Si las partes o alguna de ellas no realizaran en plazo la provisión de fondos solicitada, el mediador podrá dar por concluida la mediación. No obstante, si alguna de las partes no hubiere realizado su provisión, el mediador, antes de acordar la conclusión, lo comunicará a la otra parte, por si tuviere interés en suplirla dentro del plazo que hubiera sido fijado, sin perjuicio de su derecho de reintegro frente a la contraparte.

DESARROLLO DEL PROCEDIMIENTO DE MEDIACIÓN: El número de sesiones inicialmente previstas es de: [Nº DE SESIONES], que se desarrollarán a lo largo de un plazo máximo de [Nº] meses, prorrogable por un plazo máximo de dos meses cuando se aprecie la posibilidad de llegar a acuerdos y así se solicite por las partes.

Cada una de las sesiones tendrá una duración aproximada de [Nº] minutos. Por acuerdo de las partes mediadora y mediadas podrá modificarse durante el desarrollo de la mediación el programa de actuaciones y la duración máxima prevista para el desarrollo del procedimiento.

PRINCIPIOS POR LOS QUE SE RIGE LA MEDIACIÓN Y DERECHOS Y OBLIGACIONES DE LAS PARTES:

1) La mediación es voluntaria. Nadie está obligado a mantenerse en el procedimiento de mediación ni a concluir un acuerdo, pudiendo desistir de aquél en cualquier momento.

Si el mediador desiste de la mediación, deberá entregar un acta a las partes en la que conste su renuncia.

En cualquier caso, el mediador deberá abandonar la mediación cuando concurran circunstancias que afecten a su imparcialidad, en especial, aquéllas a las que se refiere el art. 13.5 de la Ley 5/2012, de 6 de julio, de mediación en asuntos civiles y mercantiles, salvo que tras informar de estas circunstancias a las personas mediadas asegure poder mediar con total imparcialidad y siempre que las partes lo consientan y lo hagan constar expresamente. Esta obligación persistirá a lo largo de todo el proceso de mediación.

2) Las personas mediadas intentarán el procedimiento pactado de buena fe, antes de acudir a la jurisdicción o a otra solución extrajudicial y actuarán entre sí conforme a los principios de lealtad y respeto mutuo.

En concreto, durante el tiempo en que se desarrolle la mediación las partes no podrán ejercitar contra las otras partes ninguna acción judicial o extrajudicial en relación con su objeto, con excepción de la solicitud de las medidas cautelares u otras medidas urgentes imprescindibles para evitar la pérdida irreversible de bienes y derechos.

3) Se garantiza la intervención de las partes en el procedimiento de mediación con plena igualdad de oportunidades, manteniendo el equilibrio entre sus posiciones y el respeto hacia los puntos de vista por ellas expresados, sin que el mediador pueda actuar en perjuicio o interés de cualquiera de ellas.

El mediador tiene la obligación de revelar cualquier circunstancia que pueda afectar a su imparcialidad o bien generar un conflicto de intereses.

4) El/La mediador/a, además de imparcial, debe ser neutral, permitiendo a las partes en conflicto alcanzar por sí mismas un acuerdo de mediación, sin proponer él/ella las soluciones.

Si las partes lo consideran necesario y siempre conforme al principio de buena fe, podrán solicitar que se suspenda el procedimiento para pedir asesoramiento especializado sobre cuestiones que surjan o sean objeto de debate o diálogo a lo largo del proceso de mediación.

En ningún caso ofrecerá el mediador asesoramiento o consejo legal o de otro tipo.

5) El procedimiento de mediación, así como toda la información y documentación que se utilice o se derive de la misma, tienen carácter confidencial. El deber de confidencialidad se extiende a todas las personas e instituciones públicas o privadas que intervengan en la mediación, incluyendo a la persona mediadora y a las partes intervinientes. La confidencialidad de la mediación y su contenido implica que las personas que hayan participado en el procedimiento no pueden ser obligadas a declarar o aportar documentación en un proceso judicial o en un arbitraje sobre la información o documentación que hubieran podido obtener o utilizar durante el transcurso de la mediación conforme al art. 8 de la Ley 24/2018 de 5 de diciembre, reguladora de la mediación en el ámbito de la Comunidad Valenciana, salvo que el levantamiento de la debida reserva sea compatible con la legislación vigente respecto al secreto profesional o exista aceptación expresa de las partes.

Las personas mediadas se comprometen a no citar al mediador como testigo en procedimiento judicial ni administrativo relacionado, directa o indirectamente, con el objeto de la mediación.

En todo caso, no estará sujeta a este deber de confidencialidad la información obtenida que no sea personalizada y se utilice para finalidades de formación o investigación, comporte una amenaza para la vida o la integridad física o psíquica de una persona, o dé conocimiento de un posible hecho delictivo.

6) Las partes deberán prestar colaboración y apoyo permanente a la actuación del mediador, manteniendo la adecuada deferencia hacia su actividad. Esta colaboración incluye facilitar la información necesaria sobre las cuestiones objeto del conflicto, sin perjuicio de la obligada reserva que recae sobre el mediador y la/s otra/s persona/s mediada/s.

7) Las personas mediadoras y las partes han de asistir siempre personalmente a las reuniones de mediación. Sólo excepcionalmente las partes podrán acudir representadas mediante escrito acreditativo de la representación.

Con carácter excepcional, la mediación se podrá desarrollar, total o parcialmente, a través de medios electrónicos, informáticos y telemáticos, siempre que se garantice la identidad de las personas intervinientes y el respeto a los principios esenciales de la mediación. Reglamentariamente, podrán establecerse determinados procedimientos que por su escasa entidad o limitada cuantía se desarrollen preferentemente por medios telemáticos.

8) El mediador, que carece de poder decisorio, facilitará la comunicación entre las partes y velará porque dispongan de la información y el asesoramiento suficientes, abriendo las posibilidades de diálogo que favorezcan la búsqueda en común del acuerdo por los sujetos mediados.

9) El mediador desarrollará una conducta activa tendente a lograr el acercamiento entre las partes, con respeto a los principios recogidos en la Ley 24/2018 de 5 de diciembre, reguladora de la mediación en el ámbito de la Comunidad Valenciana.

10) El incumplimiento de sus obligaciones por el mediador generará la consiguiente responsabilidad civil, con obligación de indemnizar los daños y perjuicios producidos.

11) Finalizado el proceso de mediación, las partes mediadas y mediadora firmarán un acta final, en la que manifestarán si se han alcanzado o no acuerdos totales o parciales y, en su caso, el contenido de éstos. Dichos acuerdos podrán ser sometidos, si resulta procedente, a aprobación judicial.

12) Cualquiera de las personas mediadas podrá solicitar que los acuerdos, en su caso, alcanzados, se formalicen en escritura pública, a los efectos dispuestos en los artículos 25 y ss. de la Ley 5/2012, de 6 de julio, de mediación en asuntos civiles y mercantiles.

Así lo declaran y asumen voluntariamente las partes mediadas y para que conste, se extiende y firma esta acta con un ejemplar para cada una de ellas, a un solo efecto, en el lugar y fecha indicados en el encabezamiento.

Firma de las personas mediadas Firma y nº [Nº] de Registro de la persona/s mediadoras

========================================================================
