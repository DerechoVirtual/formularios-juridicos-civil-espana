---
name: contrato-ceden-derechos-hereditarios-civ-0455
description: "Contrato por el que se ceden derechos hereditarios. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato por el que se ceden derechos hereditarios

> Formulario **CIV-0455** del plugin **Herencias, testamentos y donaciones** (`formularios-herencias-y-donaciones`) · Civil › Sucesiones y donaciones · normativa revisada el 24-11-2026.

## Qué es

Contrato privado por el que un heredero (cedente) transmite a otra persona (cesionario), a cambio de un precio, los derechos que le corresponden en una herencia ya aceptada y liquidada fiscalmente pero todavía no partida. Incluye cláusulas de pago (al contado o aplazado), condición suspensiva, confidencialidad, sumisión a tribunales o a arbitraje y cláusula penal opcional (formulario adaptado a la reforma de la LO 1/2025).

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato por el que se ceden derechos hereditarios» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato por el que se ceden derechos hereditarios” para mi caso». También puedes invocarla directamente con `/formularios-herencias-y-donaciones:contrato-ceden-derechos-hereditarios-civ-0455`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-herencias-y-donaciones:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Herencias, testamentos y donaciones) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (9 veces)
- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] FECHA (6 veces)
- [ ] NÚMERO (6 veces)
- [ ] IMPORTE (4 veces)
- [ ] IMPORTE EN LETRA (3 veces)
- [ ] NOMBRE DEL NOTARIO (3 veces)
- [ ] Nº DE PROTOCOLO (3 veces)
- [ ] PORCENTAJE (3 veces)
- [ ] DNI/NIE (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] DÍA (2 veces)
- [ ] ENTIDAD (2 veces)
- [ ] IBAN (2 veces)
- [ ] NOMBRE Y APELLIDOS O DENOMINACIÓN SOCIAL (2 veces)
- [ ] SEDE (2 veces)
- [ ] SUCURSAL (2 veces)
- [ ] AÑO
- [ ] DERECHOS CEDIDOS
- [ ] DESCRIPCIÓN DE LOS BIENES Y DERECHOS
- [ ] MES
- [ ] NOMBRE Y APELLIDOS DE LOS DEMÁS HEREDEROS
- [ ] NOMBRE Y APELLIDOS DEL CAUSANTE
- [ ] PARENTESCO
- [ ] PARTE QUE LOS ASUME

## Normas que cita el formulario

- art. 1365 Código Civil
- art. 34 Ley 60/2003

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

CONTRATO DE CESIÓN DE DERECHOS HEREDITARIOS

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO]

REUNIDOS

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— Intervienen en nombre y representación de otra persona:

D./Dª [NOMBRE Y APELLIDOS], en nombre y representación de [NOMBRE Y APELLIDOS O DENOMINACIÓN SOCIAL], en lo sucesivo "EL CEDENTE", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D. [NOMBRE DEL NOTARIO], en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO].

D./Dª [NOMBRE Y APELLIDOS], en nombre y representación de [NOMBRE Y APELLIDOS O DENOMINACIÓN SOCIAL], en lo sucesivo "EL CESIONARIO", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D. [NOMBRE DEL NOTARIO], en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO].

Todas las partes, en el respectivo carácter con el que intervienen, se reconocen mutuamente la capacidad legal en Derecho necesaria para concertar el presente CONTRATO DE CESIÓN DE DERECHOS HEREDITARIOS, y a tal efecto, libremente y de común acuerdo,

— Intervienen en nombre y derecho propios:

D./Dª [NOMBRE Y APELLIDOS], con DNI/NIE [DNI/NIE] y domicilio en [DOMICILIO], en su propio nombre y derecho, en lo sucesivo "EL CEDENTE".

D./Dª [NOMBRE Y APELLIDOS], con DNI/NIE [DNI/NIE] y domicilio en [DOMICILIO], en su propio nombre y derecho, en lo sucesivo "EL CESIONARIO".

Todas las partes, en el respectivo carácter con el que intervienen, se reconocen mutuamente la capacidad legal en Derecho necesaria para concertar el presente CONTRATO DE CESIÓN DE DERECHOS HEREDITARIOS, y a tal efecto, libremente y de común acuerdo,

EXPONEN

PRIMERO.– Que EL CEDENTE es [PARENTESCO] de D./Dª [NOMBRE Y APELLIDOS DEL CAUSANTE], quien falleció en [LOCALIDAD] el día [FECHA], bajo testamento otorgado en fecha [FECHA] en [LOCALIDAD] ante el Notario D. [NOMBRE DEL NOTARIO], con el número de protocolo [Nº DE PROTOCOLO]. Que el causante instituyó herederos por partes iguales a EL CEDENTE, D./Dª [NOMBRE Y APELLIDOS], y a [NOMBRE Y APELLIDOS DE LOS DEMÁS HEREDEROS].

SEGUNDO.– La citada herencia ha sido liquidada del impuesto de sucesiones, pero no ha sido objeto de partición, no existiendo cargas ni deudas de que deba responder ni el caudal hereditario ni la que fue sociedad de gananciales del causante.

TERCERO.– Que son bienes y derechos de la herencia los siguientes: [DESCRIPCIÓN DE LOS BIENES Y DERECHOS].

CUARTO.– Que EL CESIONARIO se encuentra interesado en la cesión de los derechos hereditarios descritos en el anterior Exponendo.

Como quiera que ambas partes se encuentran interesadas en ello, de común acuerdo llevan a efecto el presente contrato con arreglo a las siguientes

CLÁUSULAS

Objeto

Por el presente contrato, EL CEDENTE cede al CESIONARIO los derechos descritos en los términos y condiciones que se detallan en el presente contrato.

Precio

El precio de la cesión de [DERECHOS CEDIDOS] descrita en el Exponendo primero se concreta en la cantidad de [IMPORTE EN LETRA] euros ([IMPORTE] €).

Pago del precio

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— Pago no aplazado.

El pago se efectuará el día [FECHA] en la cuenta corriente nº [IBAN] que EL CEDENTE tiene suscrita con la entidad [ENTIDAD] en su sucursal [SUCURSAL]. El retraso en más de [NÚMERO] días dará derecho al CEDENTE a exigir al CESIONARIO un interés moratorio del [PORCENTAJE] % respecto de cada uno de los pagos no satisfechos puntualmente. Si EL CESIONARIO se retrasara en el pago de dos plazos o en el pago del último, EL CEDENTE podrá optar entre exigir el pago de los plazos pendientes o resolver el contrato, con abono en ambos casos de las indemnizaciones que puedan corresponder.

— Pago aplazado.

El pago de las cantidades aplazadas del precio se efectuará en [NÚMERO] plazos sucesivos de [IMPORTE] euros cada uno de ellos, pudiendo EL CESIONARIO en cualquier momento anticipar el pago de los plazos pendientes con una reducción del [PORCENTAJE] % sobre cada uno de ellos.

El pago se efectuará el día [DÍA] de cada mes en la cuenta corriente nº [IBAN] que EL CEDENTE tiene suscrita con la entidad [ENTIDAD] en su sucursal [SUCURSAL]. El retraso en más de [NÚMERO] días dará derecho al CEDENTE a exigir al CESIONARIO un interés moratorio del [PORCENTAJE] % respecto de cada uno de los pagos no satisfechos puntualmente. Si EL CESIONARIO se retrasara en el pago de dos plazos o en el pago del último, EL CEDENTE podrá optar entre exigir el pago de los plazos pendientes o resolver el contrato, con abono en ambos casos de las indemnizaciones que puedan corresponder.

Condición suspensiva

La cesión se entiende hecha bajo condición suspensiva a favor del CEDENTE hasta el momento en que el importe total del precio haya sido satisfecho, esto es, hasta el día [FECHA].

Deber de confidencialidad

Las Partes se obligan a no revelar, ceder o transferir a terceros ninguna información referente a los negocios, clientes, operaciones, instalaciones, procedimientos, métodos, transacciones, "know-how", o cualquier otro aspecto relacionado con la actividad de la contraparte que pudieran conocer o hayan conocido con motivo de la celebración del presente contrato.

Gastos e impuestos

Todos los gastos e impuestos que se originen como consecuencia de la formalización, cumplimiento o extinción del presente contrato y de las obligaciones que de él se deriven serán de cargo de [PARTE QUE LOS ASUME]. Igualmente, los gastos judiciales que se ocasionen por incumplimiento del presente contrato serán por cuenta de la parte incumplidora, incluidos honorarios del Procurador y Abogado aunque sus intervenciones no fueran preceptivas.

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— Pacto de sumisión y ley aplicable, sin cláusula penal en caso de no ejecución voluntaria de la sentencia.

Para cuantas cuestiones o divergencias pudieran suscitarse en relación con el presente contrato, ambas partes establecen someterse a los Tribunales de [LOCALIDAD], en [SEDE], renunciando expresamente a su fuero propio si lo tuvieran.

El presente contrato tiene exclusivamente carácter civil y se regirá por sus propias cláusulas y, en lo en ellas no dispuesto, por lo previsto en el Código Civil y demás leyes especiales.

— Pacto de sumisión y ley aplicable, con cláusula penal en caso de no ejecución voluntaria de la sentencia.

Para cuantas cuestiones o divergencias pudieran suscitarse en relación con el presente contrato, ambas partes establecen someterse a los Tribunales de [LOCALIDAD], en [SEDE], renunciando expresamente a su fuero propio si lo tuvieran.

En el caso de que la parte o partes que hubieran resultado condenadas en el fallo de la sentencia no cumplieran voluntariamente con el fallo de la sentencia en el plazo de [NÚMERO] días, deberán abonar a quien le hubiera vencido en el pleito la cantidad de [IMPORTE EN LETRA] euros ([IMPORTE] €), sin perjuicio de la indemnización por daños y perjuicios que pudiera corresponderles.

El presente contrato tiene exclusivamente carácter civil y se regirá por sus propias cláusulas y, en lo en ellas no dispuesto, por lo previsto en el Código Civil y demás leyes especiales.

— Sumisión a arbitraje y ley aplicable, sin cláusula penal en caso de no ejecución voluntaria del laudo.

Para cuantas cuestiones o divergencias pudieran suscitarse en relación con el presente contrato, ambas partes establecen someterse al Arbitraje de Derecho de la Cámara de Comercio de [LOCALIDAD].

El presente contrato tiene exclusivamente carácter civil y se regirá por sus propias cláusulas y, en lo en ellas no dispuesto, por lo previsto en el Código Civil y demás leyes especiales.

— Sumisión a arbitraje y ley aplicable, con cláusula penal en caso de no ejecución voluntaria del laudo.

Para cuantas cuestiones o divergencias pudieran suscitarse en relación con el presente contrato, ambas partes establecen someterse al Arbitraje de Derecho de la Cámara de Comercio de [LOCALIDAD].

En el caso de que la parte o partes que hubieran resultado condenadas en el laudo no cumplieran voluntariamente con el fallo del mismo en el plazo de [NÚMERO] días, deberán abonar a quien le hubiera vencido en el pleito la cantidad de [IMPORTE EN LETRA] euros ([IMPORTE] €), sin perjuicio de la indemnización por daños y perjuicios que pudiera corresponderles.

El presente contrato tiene exclusivamente carácter civil y se regirá por sus propias cláusulas y, en lo en ellas no dispuesto, por lo previsto en el Código Civil y demás leyes especiales.

Notificaciones

Toda notificación que se efectúe entre las partes se hará por escrito y será entregada personalmente o de cualquier otra forma que certifique la recepción por la parte notificada en los respectivos domicilios indicados en el encabezamiento de este Contrato.

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

Generalidades

El presente contrato anula y reemplaza cualquier contrato o acuerdo anterior entre las partes con el mismo objeto y sólo podrá ser modificado por un nuevo acuerdo firmado por ambas partes.

Si alguna de las cláusulas del presente contrato fuere declarada nula o inaplicable, dicha cláusula se considerará excluida del contrato, sin que implique la nulidad del mismo. En este caso las partes harán cuanto esté a su alcance para encontrar una solución equivalente que sea válida y que refleje debidamente sus intenciones.

Los encabezamientos de las distintas cláusulas lo son sólo a efectos informativos, y no afectarán, calificarán o ampliarán la interpretación de este Contrato.

Y en prueba de conformidad y aceptación de cuanto antecede, ambas partes firman los [NÚMERO] folios del presente CONTRATO DE CESIÓN DE DERECHOS HEREDITARIOS, extendido por duplicado y a un solo efecto, en la ciudad y fecha mencionados en el encabezamiento.

Fdo. D./Dª [NOMBRE Y APELLIDOS] (EL CEDENTE)

Fdo. D./Dª [NOMBRE Y APELLIDOS] (EL CESIONARIO)

NOTAS DE USO

Al cumplimentar los datos de las partes: si el estado civil es el de casado, conviene expresar el régimen económico matrimonial y el nombre y apellidos del cónyuge, puesto que el Código Civil contempla la posibilidad de comprometer los bienes comunes o gananciales (artículo 1365 del Código Civil). Si se trata de una persona física que interviene en su propio nombre y derecho, es preciso hacer constar tal extremo; lo mismo sucede si interviene en representación de otra persona física, en cuyo caso será necesario describir la fuente de la que dimana su representación, ya sea legal o convencional. En el mismo sentido, si se trata de una persona física que actúa en beneficio de una sociedad de gananciales, de una sociedad civil irregular o de una comunidad de bienes, puesto que en estos casos no existe una personalidad jurídica diferente de la de los miembros que la integran.

Pago del precio: en el caso de que se trate de una transferencia internacional será preciso conocer el código SWIFT o BIC (8 u 11 dígitos alfanuméricos que contienen la identificación del nombre y oficina del banco y el país donde se encuentra). Recuérdese que la Ley 3/2004, de 29 de diciembre, por la que se establecen medidas de lucha contra la morosidad en las operaciones comerciales, establece la aplicación automática de un tipo de interés de demora, sin necesidad de aviso de vencimiento ni de intimación alguna por parte del acreedor. No obstante, el acreedor sólo podrá exigir el pago de los intereses de demora cuando haya cumplido con las obligaciones contractuales y legales que le incumbían y cuando el retraso en el pago no sea imputable a su conducta. Si se dan estas condiciones se devengará el interés de demora contractual o el fijado legalmente.

Sumisión a arbitraje: según el artículo 34 de la Ley 60/2003, de 23 de diciembre, de Arbitraje, los árbitros sólo decidirán en equidad si las partes les han autorizado expresamente para ello.
