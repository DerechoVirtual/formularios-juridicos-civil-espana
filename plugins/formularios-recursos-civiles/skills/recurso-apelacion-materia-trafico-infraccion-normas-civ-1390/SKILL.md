---
name: recurso-apelacion-materia-trafico-infraccion-normas-civ-1390
description: "Recurso de apelación en materia de tráfico por infracción de normas y garantías procesales. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Recurso de apelación en materia de tráfico por infracción de normas y garantías procesales

> Formulario **CIV-1390** del plugin **Recursos civiles: reposición, apelación, casación y queja** (`formularios-recursos-civiles`) · Civil › Recursos · normativa revisada el 24-11-2026.

## Qué es

Escrito de interposición de recurso de apelación ante el Tribunal de Instancia sobre responsabilidad derivada de la circulación de vehículos a motor, basado en infracción de normas y garantías procesales, llegando a provocar indefensión, y vulneración de las reglas sobre la carga de la prueba en la sentencia, así como la consideración de haberse producido un enriquecimiento injusto por la reparación del vehículo siniestrado.

Es un modelo de tipo **recursos**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Recurso de apelación en materia de tráfico por infracción de normas y garantías procesales» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Recurso de apelación en materia de tráfico por infracción de normas y garantías procesales” para mi caso». También puedes invocarla directamente con `/formularios-recursos-civiles:recurso-apelacion-materia-trafico-infraccion-normas-civ-1390`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-recursos-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Recursos civiles: reposición, apelación, casación y queja) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (6 veces)
- [ ] FECHA (4 veces)
- [ ] ASEGURADORA
- [ ] AÑO
- [ ] FALLO DE LA SENTENCIA
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] NOMBRE Y APELLIDOS
- [ ] Nº DE PROCEDIMIENTO

## Normas que cita el formulario

- art. 458.1 LEC
- art. 217 LEC
- art. 217.2 LEC
- art. 217.7 LEC
- art. 276 LEC

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

- Junto a «…A LA SECCIÓN CIVIL DE LA AUDIENCIA PROVINCIAL DE [LOCALIDAD]»: La AP no tiene «Sección Civil» como denominación legal: se cita la Sección por su número (p. ej. «A LA SECCIÓN [ ] DE LA AUDIENCIA PROVINCIAL DE [ ]»). Fuente: LOPJ arts. 80 y 82 (Audiencia Provincial, sin cambio de denominación).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Notas al pie del formulario original:
(1) A pesar de que el art. 459 LEC se titula "Apelación por infracción de normas o garantías procesales", no existe en realidad un recurso de apelación diferente, sino que las infracciones procesales y los motivos de fondo o de Derecho material se deducen, al igual que en la instancia, en los mismos escritos alegatorios, y se resuelven en la misma resolución (art. 465.3 y 4 LEC), por el contrario de lo que está proyectado para la vía de recursos extraordinarios (casación o infracción procesal), si bien tampoco aquí es por el momento operativa una dicotomía (ver temas correspondientes). Aunque nada impide que el recurso de apelación se circunscriba a un defecto formal, lo normal será que se aleguen igualmente, motivos de fondo, bien porque, como en el caso, la sentencia de apelación resolverá el fondo, aunque estime la violación de normas procesales de aplicación en la sentencia apelada, bien para caso de desestimación de dicha violación.

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

A LA SECCIÓN CIVIL DE LA AUDIENCIA PROVINCIAL DE [LOCALIDAD]

D./Dña. [NOMBRE Y APELLIDOS] Procurador/a de los Tribunales, que actúa en nombre y representación de la Compañía de Seguros [ASEGURADORA], según ya queda acreditado en autos de juicio ordinario n.º [Nº DE PROCEDIMIENTO]/[AÑO], en los mismos comparezco y como mejor en Derecho proceda, DIGO:

Que el pasado día [FECHA] se me ha notificado la sentencia de fecha [FECHA], recaída en las presentes actuaciones, por la que se acuerda [FALLO DE LA SENTENCIA], y estimando la misma gravosa para los intereses de mi mandante, dicho sea en términos de defensa, dentro del plazo de veinte días legalmente establecido en el art. 458.1 LEC, INTERPONGO RECURSO DE APELACIÓN contra dicha resolución.

REQUISITOS PROCESALES

I

Se presenta este escrito de interposición ante ese Tribunal, que es el competente para conocer del recurso de apelación, con arreglo al art. 458.1 LEC.

II

Se presenta este escrito de interposición dentro del plazo de veinte días contados desde el día siguiente a la notificación de la resolución impugnada (art. 458.1 y 3 LEC).

III

Mi representado/a está legitimado/a, en tanto que parte que niega su obligación de reparación tal y como se fijó crédito de la parte actora, y tiene perjuicio o gravamen por la resolución impugnada, puesto que se condena al cumplimiento, mediante el pago de una indemnización (arts. 10 y 448.1 LEC).

IV

Las exigencias de postulación se llenan para este escrito de interposición, ya que se comparece mediante Procurador de los Tribunales, y asistido de abogado en ejercicio, ambos colegiados y habilitados para ejercer ante el Tribunal (arts. 23.1 y 31.1 LEC).

FUNDAMENTOS DEL RECURSO

INFRACCIÓN PROCESAL

Vulneración de las reglas sobre la carga de la prueba.

La sentencia de instancia ha utilizado equivocadamente, dicho sea con todo respeto, las reglas de distribución del onus probandi, que se explayan en el art. 217 LEC, y que como se sabe, entran en liza cuando existe un vacío probatorio.

Ciertamente, en el precedente juicio de faltas quien debía acreditar el hecho incriminable de la conducción descuidada con resultado lesivo, y la participación en el mismo del conductor del automóvil, era el acusador, por el amparo de la presunción de inocencia, que es inculpabilidad interina por derecho subjetivo constitucional (art. 24.2 CE).

Pero, al ejercitarse la acción civil ex quasi delictio en el orden civil, no se invierten los términos, y no es el material agente del daño quien ha de probar su propia y exquisita diligencia, como por exégesis jurisprudencial del régimen de los arts. 1.902 y ss. CC, mantiene la sentencia, dado que la jurisprudencia es firme en que la objetivación de la culpa aquiliana, incluso con introducción prudencial de la responsabilidad por riesgo creado, no resulta aplicable a los accidentes de circulación con daños mutuos.

En estas colisiones del tráfico viario el régimen de la responsabilidad civil es el subjetivo tradicional, en que ha de demostrarse, además de un daño y una relación de causalidad adecuada, la intervención de algún género de culpa o negligencia en el actuar de quien cabe reciba la obligación de reparar.

La conducta negligente es hecho constitutivo de la pretensión actora, conforme al art. 217.2 LEC, y no cabe concebir el hecho, por otra parte negativo y de imposible prueba (facilidad probatoria ex art. 217.7 LEC), de la diligencia en practicar el giro con intermitencia activada y antes de iniciada la maniobra de adelantamiento, como el hecho impeditivo de una responsabilidad objetivizada con esa mínima atenuación.

FUNDAMENTOS DE FONDO

Primero.-/

Segundo.- Enriquecimiento injusto por la reparación de vehículo siniestrado.

En el capítulo de daños en el vehículo de motor del actor, se reclama el cumplimiento mediante restitución de hacer, como principal la reparación del mismo, que asciende a [IMPORTE] euros, según presupuesto que presenta la demanda, y como subsidiaria, la adquisición de un vehículo de iguales características técnicas para sustituir al siniestrado.

En este ámbito que es el tradicional de la culpa aquiliana, la indemnización persigue la íntegra reposición del patrimonio del perjudicado, a fin de situarlo en el mismo nivel que tuviera antes del daño, y lógicamente, ni peor ni mejor.

Cuando el bien lesionado conoce distintos valores, según se utilice el prisma subjetivo de la utilidad del uso que reporta al usuario, o el prisma objetivo del valor que tendría en el mercado.

Con los automóviles y motocicletas ocurre que la divergencia entre el valor en uso y el valor en cambio es muy grande con pequeño paso del tiempo, y si se resarce al damnificado con el costo de reparar su vehículo se le indemniza o repone en su situación patrimonial subjetiva, mientras que si se le resarce con el valor venal, se le atribuye lo que hubiera obtenido en el caso de venta.

El criterio de cumplimiento in natura restituyendo un vehículo de las características del que no se repara, cuenta con las máximas posibilidades de fracaso, porque no se trata de condiciones técnicas teóricas y de antigüedad, lo que ya de suyo es complicado, sino de condiciones concretas, por lo que es una vía desechable.

El criterio jurisprudencial atinado es atender a la decisión del perjudicado puesta en relación con la diferencia crematística entre el coste de reparación y el valor venal, con lo que se conjugan lo objetivo de la deuda del responsable con lo subjetivo del crédito del lesionado.

La sentencia recurrida se equivoca al no seguir esta doctrina de las Audiencias: Si en principio, no cabe que quien sufre daño reparable se vea indirectamente expropiado del vehículo que, de no haberse producido el accidente, seguiría usando con normalidad, dado que el valor venal es de mercado y el actor no se prueba quisiera vender su automóvil, hay que ponderar la distancia entre el precio de una reparación integral, y el que el perjudicada haya efectivamente invertido en reparar.

En el caso, es tamaña la distancia entre el presupuesto de reparación y el valor en cambio del vehículo que, sin haberse procedido a sufragar la reparación del vehículo -de cuyo uso feliz e inexcusable se protesta-, no puede reconocerse la cantidad pedida, conjurando que el damnificado aproveche la ocasión del siniestro para obtener una liquidez a fin de cambiar de automóvil o para destinarla a fines diversos.

Esta corrección conviene en el asunto, si bien prudencialmente se admitiera en la contestación a la demanda, se incremente el valor venal del vehículo en un 20% de afección, y puesto que de las aclaraciones de la pericial técnica del Sr. obtenemos que el valor venal de la motocicleta a la fecha del siniestro es de [IMPORTE] euros, el resarcimiento justo asciende a [IMPORTE] euros.

En su virtud,

SUPLICO A LA AUDIENCIA PROVINCIAL

Que, teniendo por presentado este escrito con su copia, y documento acompañado, de lo que se ha dado traslado al Procurador de la parte contraria en la forma que previene el art. 276 LEC, se sirva tener por INTERPUESTO recurso de apelación contra la sentencia de fecha [FECHA] y. seguido que sea el legal procedimiento, dicte sentencia que revoque la de instancia, y resolviendo sobre la cuestión que es objeto de proceso, desestime en su integridad la demanda, o subsidiariamente, determine que la obligación de mi mandante se limita al pago de [IMPORTE] euros, sin intereses moratorios.

Es Justicia de hacerse en [LUGAR], a [FECHA].

OTROSÍ PRIMERO DIGO, que se acompaña a este escrito resguardo acreditativo del pago del depósito de 50 euros en la Cuenta de Depósitos y Consignaciones del Tribunal al que se dirige, conforme exige la disposición adicional 15.ª LOPJ, por lo que,

SUPLICO AL TRIBUNAL que tenga por causada la manifestación anterior a los efectos oportunos.

OTROSÍ SEGUNDO DIGO que de acuerdo con lo prescrito en el artículo 449.3 de la Ley de Ritos, al encontrarnos ante un proceso en que se pretende la condena a indemnizar daños y perjuicios derivados de la circulación de vehículos de motor, se acredita mediante la aportación del correspondiente resguardo de ingreso en la Cuenta de Depósitos y Consignaciones judiciales, haber constituido depósito del importe de la condena, que asciende a la suma de [IMPORTE] euros, más los intereses y recargos exigibles, que se calculan en [IMPORTE] euros, por lo que nuevamente,

SUPLICO AL TRIBUNAL que tenga por hecha la anterior manifestación a los oportunos efectos.

Firma de Abogado/a	Firma de Procurador/a
