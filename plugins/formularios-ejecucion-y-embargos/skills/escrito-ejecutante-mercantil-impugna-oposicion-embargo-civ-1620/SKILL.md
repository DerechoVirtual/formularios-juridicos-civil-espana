---
name: escrito-ejecutante-mercantil-impugna-oposicion-embargo-civ-1620
description: "Escrito del ejecutante mercantil que impugna la oposición al embargo en ejecución provisional. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito del ejecutante mercantil que impugna la oposición al embargo en ejecución provisional

> Formulario **CIV-1620** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Modelo de escrito de la mercantil ejecutante impugnando la oposición al embargo en la ejecución provisional y solicitando se acuerde la continuación de la ejecución.

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito del ejecutante mercantil que impugna la oposición al embargo en ejecución provisional» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito del ejecutante mercantil que impugna la oposición al embargo en ejecución provisional” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:escrito-ejecutante-mercantil-impugna-oposicion-embargo-civ-1620`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] DENOMINACIÓN SOCIAL (5 veces)
- [ ] FECHA (4 veces)
- [ ] AÑO (2 veces)
- [ ] LUGAR
- [ ] NOMBRE Y APELLIDOS
- [ ] Nº
- [ ] NÚMERO
- [ ] SEDE

## Normas que cita el formulario

- art. 529.2 LEC
- art. 528.3 LEC
- art. 1.911 CC
- art. 449 LEC
- art. 530.3 LEC

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a. de los Tribunales y de COMERCIAL [DENOMINACIÓN SOCIAL], S.L., según tengo acreditado en los autos de Juicio Ordinario n.º [NÚMERO]/[AÑO], pieza separada de Ejecución Provisional con número de registro n.º [Nº]/[AÑO], ante el Tribunal comparezco y como mejor en Derecho proceda, DIGO:

Que por medio del presente escrito, dentro del plazo de cinco días legalmente previsto, y que me ha sido concedido por diligencia de ordenación de fecha [FECHA], vengo a evacuar el traslado, y formulo manifestaciones para impugnar la oposición a la ejecución provisional formulada por la representación de DISTRIBUCIONES [DENOMINACIÓN SOCIAL], S.A., con arreglo al art. 529.2 LEC, efectuando las siguientes

ALEGACIONES

PRIMERA.- La parte ejecutada se opone al embargo trabado en su domicilio el [FECHA], aduciendo la inviabilidad en concreto de que, revocándose el fallo de la sentencia que se ejecuta provisionalmente, el pago a mi representada sea devuelto, para lo que pretende que, de lo consignado en la cuenta del Tribunal, según sus propios cálculos, sea entregado a la acreedora, mi mandante, la cantidad que la ejecutada prefiere, quedando el resto como caución.

Así se soslaya todo el régimen legal, y desde luego, se excusa el propio cauce de oposición tasada que dispone el art. 528.3 LEC, puesto que está previsto para alegar que una medida o actuación ejecutiva acordada que pueda causar una situación imposible de restaurar o de compensar económicamente mediante el resarcimiento de daños y perjuicios, en el caso improbable de que la Audiencia Provincial revoque la sentencia; y nada más normal que el embargo decretado por el tribunal en el auto de fecha [FECHA], por el que se despachó la ejecución provisional, dentro del procedimiento de apremio para obtener la satisfacción de una condena de carácter dinerario, con relación a una persona jurídico mercantil que demuestra obviamente contar con la liquidez adecuada para hacer frente al pago de la suma debida.

Mediante un laborioso esfuerzo exegético de la parte ejecutada, que esta parte le reconoce, se aborda una problemática que ha sido tenida en cuenta por el legislador de la novedosa ejecución provisional civil, que es la consideración de la solvencia del acreedor recurrente de la resolución que establece una obligación dineraria declarada, agudizada en el supuesto por tratarse la obligación de un importe de muy subida entidad, pero concluye de manera que, con mucha obviedad, adolece de vocación correctora de los mandatos legales explícitos.

Es claro, y así destila el apartado XVI de la Exposición de Motivos de LEC, que la ejecución provisional ex lege y sin prestación de caución está al servicio de un reforzamiento de la justicia civil de primera instancia y de la disuasión del derecho a ulteriores grados jurisdiccionales. Se opta por mejorar la posición, de cara a la efectividad de la tutela judicial dispensada, de quien la obtiene sin cosa juzgada, y a pesar de entablarse apelación o recurso extraordinario, puesto que se adelanta, con lo que disminuyen las posibilidades de insatisfacción de las sentencias, y se conjura la idea de una transacción del derecho amparado en sentencia, desdoro de lo jurisdiccional cuando se funda en lo insoportable para el justiciable vencedor de la espera e incertidumbre a la finalización de los morosos recursos civiles si no cuenta con economía holgada y abogados complacientes.

El argumento es de la mejor tradición del Derecho: la mayoría de las sentencias de instancia se confirman en ulterior grado. Así como se protege en el campo posesorio la apariencia, con tan rancia relevancia en las relaciones mercantiles, por razón de que el detentador material de cosas y derechos resulta en la inmensa mayoría de los casos su titular, se protege al justiciable que tiene una sentencia que le favorece como detentador de un derecho —el que puede claudicar en todo o parte—, porque casi siempre resulta ser de su incontestable titularidad.

El tamiz de una primera tutela judicial lanza el riesgo de la inefectividad de la tutela judicial en firme conforme principio ‘victus victori’. Quien pretendió en la instancia tenía el riesgo de no verse satisfecho aunque fuera titular del crédito, dado que la doctrina constitucional siempre ha recordado que el derecho a que se ejecute lo juzgado no equivale a un derecho a la solvencia del deudor —ésta procede de su universal patrimonio neto, presente o futuro ex art. 1.911 CCiv—, y una vez victoriosa la pretensión, para la segunda instancia o vía casacional, la satisfacción se urge para trasladar el riesgo al que recibió algún gravamen por la inicial victoria de la pretensión, en la medida precisa de tal gravamen. Debe tenerse en cuenta que sólo se logrará lanzar el dicho riesgo cuando el deudor —que por el momento así lo es siempre el ejecutado— pague (que aquí puede hacerlo, según se comprueba, pero no siempre ocurrirá).

SEGUNDA.- Esta parte sencillamente alega que no procede analizar su solvencia, y además tiene que aducir, sin admitir una inactividad, que la situación de postración de mi patrocinada ha sido provocada, muy esencialmente por la conducta de DISTRIBUCIONES [DENOMINACIÓN SOCIAL], S.A., según aparece en la sentencia que se ejecuta, que reconoce un activo que correspondería a la propiedad de COMERCIAL [DENOMINACIÓN SOCIAL], S.L., y que detenta aquella primera, pero que no se le ha reclamado por el momento.

Sería del todo injusto que quien ha procurado el hundimiento económico de una empresa, por comportamientos que, sólo en parte, han sido depurados en un proceso terminado con una importante condena pecuniaria —derecho en base al contrato incumplido por la contraparte— luego resultara de mejor condición que cualquier otro obligado al que se puede ejecutar provisionalmente, al socaire del déficit patrimonial de quien es acreedor. Sería abonar la prepotencia del incumplidor, y después de la antijuricidad de haber expulsado a la ejecutante del mercado, seguir manteniendo lo antijurídico con la utilización de sus recursos, por lo que se ve, muy amplios.

TERCERA.- Pero además, las medidas alternativas de ejecución que propone el condenado son de todo punto inaceptables, ya que en la práctica dejan a mi cliente en una situación de total desprotección y falta de garantías.

Confunde la ejecutada la caución como requisito de procedibilidad de un recurso —como los casos del art. 449 LEC, que expresamente dejan a salvo el derecho a la ejecución provisional—, en que se trata de asegurar el buen fin de la sentencia firme, con la caución del art. 530.3 LEC, que únicamente tiene sentido cuando la actividad ejecutiva concreta no sea posible sustituirla por otra actuación posible y de eficacia similar, puesto que en otro caso, no tendría sentido que se dispusiera que se deniegue la realización de la concreta actividad ejecutiva pero prosiga el procedimiento de apremio según lo previsto en la LEC.

La finalidad de toda ejecución, también de la provisional, es la satisfacción del acreedor ejecutante, y ninguna existe con la pura consignación cautelar, la cual no es opción de la medida ejecutiva alternativa a un embargo, sino ‘ultima ratio’ frente a la inexistencia de alternativas al embargo. Cosa que no ocurre en el caso, por hipótesis, ya que la parte ejecutada ha depositado toda la cantidad por la que se le procedería apremiar.

Por otro lado, la caución ofrecida por el opositor para responder de la demora en la ejecución es de todo punto insuficiente, ya que se consigna el 30% por encima del principal, y ello es precisamente lo que se ejecuta, y si en la prospección legal ello representa el consumo en conceptos ilíquidos, cuando ya se tiene que tener en cuenta la espera a una resolución de segunda instancia, o incluso casacional, debiera incrementarse.

Por lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito, y justificante de haberse verificado el traslado al Procurador/a. de la parte adversa, admita uno y otros, y en mérito a las manifestaciones vertidas, desestime la oposición a la ejecución provisional formulada por la representación de DISTRIBUCIONES [DENOMINACIÓN SOCIAL], S.A., y acuerde la continuación de la ejecución, con entrega a esta parte de la cantidad consignada como principal de la condena, y no sólo de la que ofrece la ejecutada, procediéndose a tasar las costas y liquidar los intereses devengados hasta la fecha de notificación del auto que así resuelva, en todo caso con imposición de las costas de este incidente a la parte que lo ha promovido.

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a

========================================================================
