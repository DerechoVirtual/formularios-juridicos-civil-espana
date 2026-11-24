---
name: oposicion-e-impugnacion-apelacion-trafico-motivos-civ-1391
description: "Oposición e impugnación de la apelación de tráfico por motivos materiales y falta de consignación. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Oposición e impugnación de la apelación de tráfico por motivos materiales y falta de consignación

> Formulario **CIV-1391** del plugin **Recursos civiles: reposición, apelación, casación y queja** (`formularios-recursos-civiles`) · Civil › Recursos · normativa revisada el 24-11-2026.

## Qué es

Escrito de oposición e impugnación de parte al recurso de apelación interpuesto sobre responsabilidad derivada de circulación de vehículos a motor, solicitando su inadmisibilidad al no haber acreditado la consignación, y oponiéndose al mismo por valoración de la actividad probatoria, concurrencia de culpas, inaplicación del baremo y de los intereses del artículo 20 de le Ley de Contrato de Seguro.

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Oposición e impugnación de la apelación de tráfico por motivos materiales y falta de consignación» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Oposición e impugnación de la apelación de tráfico por motivos materiales y falta de consignación” para mi caso». También puedes invocarla directamente con `/formularios-recursos-civiles:oposicion-e-impugnacion-apelacion-trafico-motivos-civ-1391`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-recursos-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Recursos civiles: reposición, apelación, casación y queja) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (10 veces)
- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] Nº (4 veces)
- [ ] ASEGURADORA (3 veces)
- [ ] FECHA (3 veces)
- [ ] AÑO
- [ ] EXPONER LOS HECHOS
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] Nº DE PROCEDIMIENTO
- [ ] PORCENTAJE
- [ ] SEDE

## Normas que cita el formulario

- art. 461.1 LEC
- art. 458.3 LEC
- art. 449.3 LEC
- art. 449.6 LEC
- art. 231 LEC
- art. 20 LCS
- art. 20.4.º LCS
- art. 461.3 LEC
- art. 460.1 LEC
- art. 270 LEC
- art. 271 LEC
- art. 394.1 LEC
- art. 398.1 LEC
- art. 398.2 LEC
- art. 276 LEC
- art. 460.2.2.ª LEC
- art. 342.2 LEC

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

- Junto a «…A LA SECCION CIVIL DE LA AUDIENCIA PROVINCIAL DE [LOCALIDAD]»: La AP no tiene «Sección Civil» como denominación legal: se cita la Sección por su número. Fuente: LOPJ arts. 80 y 82 (Audiencia Provincial, sin cambio de denominación).

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

A LA SECCION CIVIL DE LA AUDIENCIA PROVINCIAL DE [LOCALIDAD]

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales en nombre de D./Dña. [NOMBRE Y APELLIDOS], cuya representación tengo debidamente acreditada en autos de juicio ordinario n.º [Nº DE PROCEDIMIENTO]/[AÑO], ante la Sala comparezco y, como mejor proceda en Derecho DIGO:

Que dentro del plazo legal conferido al efecto por el Tribunal a esta parte mediante diligencia de ordenación de fecha [FECHA], formalizo escrito de oposición al recurso de apelación, así como de impugnación de la resolución apelada, con base en las siguientes:

ALEGACIONES

PRESUPUESTO PROCESAL

Siendo por quien comparezco parte actora en el proceso, que ha obtenido sentencia parcialmente estimatoria, se reúnen los presupuestos subjetivos y objetivos para presentar ante la Sala el escrito de oposición al recurso de apelación interpuesto por la parte demandada aseguradora [ASEGURADORA], junto con la impugnación de la propia sentencia, ya que esta parte está debidamente comparecida, hallándose legitimada en lo que le ha sido desfavorable la resolución recurrida, con arreglo al art. 461.1 LEC.

INADMISIBILIDAD DEL RECURSO DE APELACIÓN

Aunque la Sala tuvo por interpuesto el recurso de apelación al que por medio del presente escrito se muestra oposición, de conformidad con el art. 458.3 LEC, se alega la inadmisibilidad de la apelación para ante la Iltma. Audiencia, por defecto de la consignación, que debió ser arreglada a la prevención del art. 449.3 LEC, dado que, al interponer el recurso la compañía de seguros [ASEGURADORA] condenada no acreditó más que haber constituido depósito de cantidad de [IMPORTE] euros, mientras que el importe de la condena asciende a [IMPORTE] euros, y los intereses al tipo del 20% anual desde [FECHA] hasta la fecha de notificación de sentencia, son de [IMPORTE] euros, faltando del depósito debido la cantidad de [IMPORTE] euros.

Se trata de un requisito de admisibilidad del recurso, y si el art. 449.6 LEC prevé mecanismo de subsanación de la carencia de acreditación del depósito, cuando el recurrente hubiera manifestado voluntad de cumplir (art. 231 LEC), en el caso, lo que falta es el depósito pleno, y no su acreditación.

OPOSICIÓN AL RECURSO DE APELACIÓN

PRIMERO.- Valoración de la actividad probatoria.

Debe mostrarse la más radical discrepancia con la censura que verifica el recurso de la parte demandada acerca de la valoración probatoria efectuada de la confesión judicial de mi mandante, y de la pericial del Sr./Sra. [NOMBRE Y APELLIDOS], puesto que ni fueron las únicas pruebas que se ponderan, ni de la conjunta y libre valoración de todas las practicadas, puede concluirse de manera distinta a como se hace en la sentencia.

Se olvida el recurrente de la prueba testifical de los agentes de la policía local de números profesionales [Nº] y [Nº], así como del atestado levantado, con su croquis, y conclusiones sobre probable evolución del accidente.

No puede argumentarse desde los parámetros del precedente juicio de faltas en que resultó absuelto D./Dña. [NOMBRE Y APELLIDOS], ya que en el mismo no declararon dichos testigos, y debidamente citados a instancias de esta parte, habiéndose comunicado con precedencia a la vista que no podrían comparecer por encontrarse de vacaciones, se decidió no suspender el acto, a pesar de la protesta formulada, lo que no se corrigió en vía de apelación.

Conforme a tales testimonios resulta contundentemente desvirtuada la tesis de la demandada, en el sentido que se declara probado en la sentencia recurrida que [EXPONER LOS HECHOS]

SEGUNDO.- Concurrencia de culpas.

En cuanto a la prohibición de adelantamiento por los ciclomotores, debe tenerse en cuenta que la carretera en cuestión carece de arcén, según puede comprobarse en el croquis que consta en el atestado policial, y el que deban circular dichos vehículos preferentemente por la derecha de la vía, que es lo que dice el precepto reglamentario citado por la contraparte, no equivale necesariamente a que, si es necesario rebasar a otro vehículo en la marcha, por la razón que fuera, deba desatenderse la regla general de hacerlo por la izquierda.

La sentencia entiende que la negligencia del conductor del automóvil, al arrollar al ciclomotor que estaba a su altura a la izquierda, intentando progresar en una vía sin arcén, y cuando iban los automóviles en larga caravana, sin avisar aquél de la intención de cambiar de sentido con señal lumínica, absorbe plenamente la supuesta imprudencia objetiva del que guiaba el ciclomotor.

Así como para excusar la prudencia debida en el campo de la responsabilidad civil no basta el cumplimiento de los reglamentos de seguridad, tampoco el objetivo incumplimiento intranscendente por el perjudicado puede arraigarla.

En todo caso, como aventura la parte contraria, de asumirse la relevancia de la infracción de mi representado, se trataría de una concausa insignificante que, en compensación de culpas, conforme a las mismas previsiones del Baremo anexo TRLRCSCVM que aduce la parte adversa, no podría conducir más que al descuento del 25% de la indemnización debida, porque la indiligencia capital fue del chófer del vehículo codemandado.

TERCERO.- Aplicación del Baremo.

Debiéndose ratificar la fijación de la indemnidad de mi representada, sin perjuicio de que el cálculo del quantum indemnizatorio será objeto de recurso de apelación por trámite de la impugnación adhesiva, defendiendo la cantidad que se pidió en la demanda, se ha de salir al paso de las objeciones inaceptables de la parte condenada.

1.-En primer lugar, si la deuda de reparación es de valor, y se liquida a través de este proceso, si bien puede admitirse que el Derecho sustantivo aplicable es el de la fecha del siniestro, y por ello no se produce en la aplicación del régimen jurídico del Baremo ninguna retroactividad por utilizarse en la sentencia los valores de la demanda para días de incapacidad temporal que inhabilita para el desempeño de tareas habituales, dado que la tasa legal regía a finales de 1998 como cuando calculó esta parte en la demanda, no puede admitirse que el valor que ahora se liquida tenga que ajustarse a los precios de 1998.

El régimen especial de intereses moratorios no tiene por misión, o por lo menos no es la principal, corregir el nominalismo de los valores tasados, ya que puede no resultar de utilización, y si el Baremo se actualiza o canjea anualmente, el resarcimiento tasado conforme a la Ley para determinado pretium doloris de la curación deberá ser el del momento en que se concede, o por lo menos, como en la sentencia, el que se pide, al cálculo del Baremo en vigor que hizo el demandante perjudicado.

2.- En cuanto al cálculo de resarcimiento con uso de los valores medios de puntos básicos por lesiones permanentes, ello pertenece al arbitrio judicial, que considera, por el contrario de la opinión interesada de la demandada que, si la pericia médica de la traumatóloga Dr./a. [NOMBRE Y APELLIDOS], no adjetiva los diagnósticos, ello no significa que deban emplearse los valores inferiores.

3.- Por lo que toca al factor de corrección por ingresos de trabajo personal, está documentada en autos la base reguladora de las prestaciones de incapacidad temporal que satisfizo el I.N.S.S. por accidente no laboral, lo que, junto a la constancia de la profesión del demandante, a falta de la autoliquidación de IRPF que se solicitó en periodo probatorio, y para mejor proveer, sin que llegara al proceso, demuestra unos rendimientos brutos de [IMPORTE], que indiciariamente llevan a un neto que supera la barrera del Baremo de [IMPORTE] euros, y nuevamente el arbitrio judicial considera justo un porcentaje en el tramo hasta el 10% de incremento de la puntuación de lesiones, que resulta prudente.

CUARTO.- Intereses del art. 20 de la Ley de Contrato de Seguro (LCS).

En el fallo de la sentencia recurrida, en punto a la condena al pago de intereses moratorios al tipo del 20% desde la fecha del siniestro, se atiene a la estricta aplicación del art. 20 LCS 50/80 .

No existe causa justificada alguna para que la aseguradora condenada no atendiera a su obligación, ya que debió consignar en el plazo de los tres meses desde el siniestro la cantidad que considerara deber como mínimo. Si precisamente ha negado hasta ahora la obligación, el haber sido declarada acertadamente por la sentencia, conlleva que se le repute constituida en mora especial automática o retroactiva desde el hecho causante, sin que tenga la menor incidencia el juicio de faltas previamente instado por esta parte, como era su derecho, dado que la evitación de devengo de intereses no se produjo en dicho proceso tampoco con arreglo a la norma, ni existe ningún abuso en intentar la condena penal que no se logró por carencia de pruebas que derruyeran la presunción de inocencia.

Por lo que toca al tipo de interés, si han transcurrido más de dos años, según correctamente mantiene la sentencia recurrida, no puede ser nunca inferior al 20% anual y desde la fecha del accidente. El haberse transvasado los dos años por cuanto ha existido un proceso penal previo, no es ningún argumento, ya que la posibilidad de depositar una indemnización siempre ha estado en mano de la deudora. Por otra parte, el art. 20.4.º LCS 50/80, en su primer párrafo establece el régimen especial de estos intereses moratorios, en cuanto al dies a quo -fecha del siniestro-, fórmula de devengo -diario-, sistema de constitución -legal, sin necesidad de intimación, y sujeto a principio de oficialidad-, y añade el tipo anual del rédito, que es el interés legal dinero incrementado en el cincuenta por ciento. El segundo párrafo del mismo precepto conforma una exasperación del tipo, hasta no menos del 20% anual cuando no se haya pagado después de dos años, pero para nada altera el sistema de devengo o la fecha inicial del mismo.

OPOSICIÓN A LA APORTACIÓN DOCUMENTAL DEL APELANTE

De conformidad con el art. 461.3 LEC, siendo el momento de alegar acerca de la admisibilidad de los documentos aportados y de las pruebas propuestas por la contraparte, debe destacarse que el art.460.1 LEC prevé que puedan acompañarse al escrito de interposición del recurso de apelación los documentos que se encuentren en alguno de los casos previstos en el art. 270 LEC, y que no hayan podido aportarse en primera instancia, es decir, documentos nuevos, de nueva noticia para la parte, o que no haya podido obtener, a pesar de su diligencia, y que haya señalado en la demanda. Su momento extraordinario de aportación en la instancia es el anterior al juicio o vista.

En ninguna parte se autoriza la aportación de las resoluciones judiciales o de autoridad administrativa del art. 271 LEC, como pretende la aseguradora demandada, que debe rechazarse de plano.

De todas formas, una resolución judicial recaída en un proceso diferente, porque tenga algún parecido con el presente, no es documento que se conecte con el objeto de la apelación, sino que, a lo sumo, constituye noticia de un criterio o precedente, que no doctrina jurisprudencial, lo cual pertenece a las alegaciones de parte para apoyar su postura, y no al elenco probatorio de autos.

IMPUGNACIÓN DE LA SENTENCIA APELADA

Cálculo de la indemnización baremada de las lesiones probadas.

El objeto de la impugnación de la sentencia apelada se ciñe a la determinación del quantum de la indemnización debida, puesto que se recorta respecto de las peticiones de la demanda en dos puntos principales:

1.- Se ha eliminado la valoración de las lesiones permanentes de mi mandante el capítulo relativo al síndrome de estrés postraumático padecido, con fundamento en la ausencia de calificación en el informe del médico forense que actuó en la Sección de Instrucción del Tribunal de Instancia de [SEDE] en el juicio por delito breve previo, y haberse excusado el perito médico de designación judicial, traumatólogo, de dictaminar a propósito, por reputar los síntomas referenciales.

Esta parte pidió pericia médica de psiquiatra especialista en valoración del daño, y no se ha practicado, habiéndose admitido, sin causa imputable al proponente, por lo que se pedirá la práctica en segunda instancia.

De todas las maneras, esta lesión se entiende está probada, porque se documenta con certificados médicos, y no debe admitirse que se valore en [Nº] puntos, como síndrome psiquiátrico del Capítulo I -Cabeza- de la Tabla VI

2.- Asimismo, se valoran la cicatrices dictaminadas de mi poderdante con el mínimo del perjuicio ligero del Capítulo especial de perjuicio estético, y es a juicio de esta parte, muy patente que, por la edad del actor, por la ubicación en zona corporal que muy habitualmente está a la vista, por el oficio del afectado en el que no es indiferente la apariencia física, y por la longitud, forma, y diacromía de las cicatrices, ha de asumirse que el perjuicio, si se considera ligero, deberá serlo en el máximo de cuatro puntos.
3.- La sentencia deniega el factor corrector por incapacidad permanente parcial, sin mayor razonamiento, y tal concepto, que se define en la Tabla IV del Baremo como el correspondiente al lesionado con "secuelas permanentes que limiten parcialmente la ocupación o actividad habitual, sin impedir la realización de las tareas fundamentales de la misma" consiste en que, sin quedar impedido el perjudicado para sus labores profesionales, el rendimiento obtenible, o el padecimiento y dificultad para el trabajo, se hayan visto reducidos o incrementados, respectivamente, de manera predeciblemente irreversible, en una proporción que le coloca en situación de déficit respecto de un trabajador normal, con la consiguiente repercusión en el empleo y los ingresos laborales. No debe identificarse con la acreditación de la incapacidad permanente parcial de Seguridad Social, que por su indemnización a tanto alzado y total compatibilidad con el trabajo, resulta extraña y de rara concesión en el sistema público.

A la luz de lo dictaminado como lesiones permanentes, para un camarero de [Nº] años de edad, hay que estimar procurada una incapacidad como se describe.

4.- Si se utiliza la fórmula cálculo -que no es incorrecta la de la sentencia, al redondearse las fracciones decimales que se obtienen- para lesiones permanentes concurrentes básicas, arroja un montante de [IMPORTE] euros, que tiene que incrementarse con los cuatro puntos de perjuicio estético y a este resultado, sumar el [PORCENTAJE] % de factor de corrección por ingresos, y [IMPORTE] de euros, de factor de corrección por incapacidad permanente parcial, llegando a la cifra de [IMPORTE] euros, que es la condena ajustada a Derecho, que se reitera en la segunda instancia.

COSTAS PROCESALES

Como debe inadmitirse el recurso, lo cual equivale a la desestimación, o en todo caso, habrá de desestimarse, las costas serán impuestas al recurrente inicial, según establece el art. 394.1 LEC, al que se remite el art. 398.1 LEC, de modo que en el supuesto de que sólo se desestimara parcialmente, por aplicación de una compensación de culpas, cada una de las partes se haría cargo de sus costas de este recurso conjunto (art. 398.2 LEC), sin alterarse el pronunciamiento de primera instancia.

En virtud de cuanto antecede,

SUPLICO A LA SALA

Que, teniendo por presentado este escrito en tiempo y forma, que se ha trasladado en términos del art. 276 LEC al Procurador de la parte recurrente, se sirva admitirlo y tener por deducida OPOSICIÓN al recurso de apelación interpuesto, e IMPUGNACIÓN de la sentencia apelada, y previo traslado de esta última a la apelante inicial, a fin de que tenga ocasión de manifestar lo que a su derecho convenga en plazo legal, seguido que sea el legal procedimiento, dicte auto que inadmita el recurso de apelación inicial, o para el caso de que se admita, dicte sentencia que lo desestime en su integridad, o subsidiariamente, aplique una compensación del 25% de la indemnización debida, y estimando la impugnación deducida por esta parte, se determine la indemnización de pago conjunto y solidario de los demandados en la cantidad de [IMPORTE] euros, más los intereses moratorios, que siempre serán del tipo del 20% anual desde la fecha del siniestro hasta el definitivo pago, para la compañía de seguros [ASEGURADORA], todo ello con imposición de las costas al recurrente.

Por ser de Justicia que pido en [LUGAR], a [FECHA].

Firma de Abogado/a	Firma de Procurador/a

OTROSÍ DIGO: Que interesa al derecho de esta parte valerse para esta segunda instancia de la práctica del siguiente medio de PRUEBA:

PERICIAL médica, de un doctor en psiquiatría, especialista en valoración del daño corporal, a través de designación por el Tribunal de apelación, a fin de que se dictamine sobre el diagnóstico de síndrome de estrés postraumático que aqueja al demandante, en los términos que se consignan en el pliego que se unió al acta de la audiencia previa de fecha

Al amparo del art. 460.2.2.ª LEC, procede porque fue prueba propuesta y admitida en primera instancia que, por la renuncia a aceptar el cargo sucesiva de los dos peritos designados -pese a que se consideró injustificada por el Letrado de la Administración de Justicia conforme al art. 342.2 LEC-, no pudo practicarse, ni siquiera como diligencia final.

SUPLICO A LA AUDIENCIA PROVINCIAL que, teniendo por causada la antecedente manifestación a los efectos oportunos, se digne resolver accediendo al acto de prueba solicitado, señalando vista para su práctica, como es procedente en Justicia que reitero en lugar y fecha ut supra.

========================================================================
