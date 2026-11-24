---
name: auto-acuerda-sucesion-procesal-subrogacion-cesion-civ-1912
description: "Auto que acuerda la sucesión procesal por subrogación o cesión del crédito ejecutivo. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Auto que acuerda la sucesión procesal por subrogación o cesión del crédito ejecutivo

> Formulario **CIV-1912** del plugin **Resoluciones judiciales civiles: autos, decretos y diligencias** (`formularios-resoluciones-judiciales-civiles`) · Civil › Resoluciones judiciales (autos, decretos, providencias, diligencias) · normativa revisada el 24-11-2026.

## Qué es

Auto que acuerda la sucesión procesal por causa de subrogación o cesión de crédito ejecutivo, con cambio de posición de parte entre cofiadores.

Es un modelo de tipo **resoluciones judiciales (autos, decretos, providencias, diligencias)**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Auto que acuerda la sucesión procesal por subrogación o cesión del crédito ejecutivo» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Auto que acuerda la sucesión procesal por subrogación o cesión del crédito ejecutivo” para mi caso». También puedes invocarla directamente con `/formularios-resoluciones-judiciales-civiles:auto-acuerda-sucesion-procesal-subrogacion-cesion-civ-1912`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-resoluciones-judiciales-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Resoluciones judiciales civiles: autos, decretos y diligencias) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (9 veces)
- [ ] FECHA (7 veces)
- [ ] ENTIDAD BANCARIA (4 veces)
- [ ] NOMBRE DEL REPRESENTADO/A (3 veces)
- [ ] LUGAR (2 veces)
- [ ] ACTO O RESOLUCIÓN
- [ ] DENOMINACIÓN SOCIAL
- [ ] IMPORTE
- [ ] NOMBRE DE LA PARTE
- [ ] NÚMERO

## Normas que cita el formulario

- art. 1.210 CC
- art. 17 LEC
- art. 517.2.5.º LEC
- art. 1.844 CC
- art. 1.845 CC
- art. 1.837 CC
- art. 1.138 CC

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
(1) En el supuesto de que se resolviera en sentido denegatorio, habida cuenta de que existen opositores a la sucesión procesal, coherente con los razonamientos que fueran -para lo que sirven los expresados en el escrito de oposición- la parte dispositiva sería algo semejante a:

‘1.- No se accede a que el Procurador de los Tribunales D. [NOMBRE Y APELLIDOS]..., comparezca en nombre y representación de X..., en calidad de sucesor procesal del Banco..., S.A., en la posición de parte ejecutante.

2.- Alzada la suspensión del proceso, constando la plena satisfacción del Banco..., S.A., se decreta el final de la ejecución, con archivo de actuaciones.

3.- Quedan a salvo las relaciones jurídico materiales del transmitente y adquirente del crédito ejecutado, así como con relación a los deudores solidarios’.

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

AUTO

En [LUGAR], a [FECHA].

Juez/a Sr./Sra. [NOMBRE Y APELLIDOS]

ANTECEDENTES DE HECHO

PRIMERO

Se ha despachado por este Tribunal ejecución de póliza mercantil de préstamo a instancias del [ENTIDAD BANCARIA], representado por el/la Procurador/a Sr./Sra. [NOMBRE Y APELLIDOS], por Auto de [FECHA], contra [ACTO O RESOLUCIÓN], deudora principal por débito de treinta y seis mil euros y otros diez mil ochocientos, que se calcularon para intereses de demora procesal y costas, y contra los avalistas solidarios [NOMBRE Y APELLIDOS], [NOMBRE Y APELLIDOS] y [NOMBRE Y APELLIDOS].

SEGUNDO

Con fecha [FECHA], el/la Procurador/a Sr./Sra. se personó en nombre y representación de [NOMBRE DEL REPRESENTADO/A], con escrito en que se pide la sucesión procesal en la posición ejecutante del Banco [ENTIDAD BANCARIA], contra los codeudores [NOMBRE Y APELLIDOS] y [NOMBRE Y APELLIDOS], por haber pagado al Banco cuarenta y seis mil ochocientos euros, y haber aceptado expresamente éste la subrogación del crédito, y a los efectos del presente juicio ejecutivo.

TERCERO

En diligencia de ordenación de [FECHA], se confirió audiencia a todos los ejecutados para que se pronunciaran sobre la petición del antedicho escrito, teniéndose al Procurador que lo presentó como mandataria de los que se pretenden nuevos ejecutantes, y requiriéndose a los representantes legales del [ENTIDAD BANCARIA], a fin de que ratificaran en la integridad del escrito que se aportó a los autos.

CUARTO

El [FECHA], el/la Procurador/a Sr./Sra. se personó en nombre y representación de [NOMBRE DEL REPRESENTADO/A] y [NOMBRE DE LA PARTE], y así se le tuvo por personado y parte en diligencia de ordenación del día [FECHA] siguiente, alegando en contra de la sucesión procesal.

RAZONAMIENTOS JURÍDICOS

PRIMERO

La transformación, unión o sucesión afectante a quienes inicialmente figuran como acreedores o como obligados en el título ejecutivo, puede afectar tanto a ejecutantes como a ejecutados por el hecho de la muerte, que provoca la sucesión ‘mortis causa’; a los ejecutantes por la cesión de créditos litigiosos (arts. 1.526 y siguientes y 1.535 CCiv) o subrogación en el crédito que se presume con generalidad para diversas fórmulas del pago total (art. 1.210 CCiv), y se establece por mandato legal en otras de pago total o parcial (cesiones de contrato sin ‘trilateralidad’ por disposición del legislador: art. 43 Ley Contrato de Seguro para las compañías de seguros; art. 33.4 Estatuto de los Trabajadores, para el FOGASA, etc); y a los ejecutados, mediante el convenio expromisorio, el contrato de asunción de deuda y la delegación (arts. 1.203, 1.205 y 1.206 CCiv), y por imperativo legal, por ejemplo, la sucesión de empresa para el contrato laboral y sus relaciones instrumentales del art. 44 Estatuto de los Trabajadores.

La previsión procesal para estas posibilidades se encuentra en el supuesto del art. 17 LEC, en general, para la sucesión procesal por transmisión del objeto litigioso, y en particular, para caso de dicha transmisión antes de despachada ejecución y una vez formado el título ejecutivo, ya que la jurisprudencia nunca ha interpretado como terminación del litigio la transmisión de su objeto, sino como viabilidad de la continuación mediante la sucesión ‘inter vivos’ en la titularidad de una posición jurídico-procesal.

SEGUNDO

Lo que viene postulado en este proceso de ejecución no es una sucesión por tercero ajeno al pleito, sino por una parte procesal, y además con alteración de la posición de quien es litisconsorte pasivo, canjeándose la de un ejecutado por la de ejecutante.

Aunque no sea algo corriente, entendiéndose el proceso como vehículo para dispensar la tutela judicial efectiva, a falta de un obstáculo de Derecho positivo y orden público, desde una perspectiva general no se percibe por qué el proceso debe descolgarse de la composición de intereses extraprocesal, pereciendo en casos como el presente, si normas sustantivas amparan el cambio de titularidades en las relaciones obligatorias.

En cuanto a la relación obligatoria que vincula al deudor principal con los fiadores solidarios que han hecho pago completo al acreedor, conforme a los arts. 1.210.3.º, 1.212 y 1.839 CCiv, no es dudoso que se ha producido la subrogación del título de crédito del ejecutante, con el derecho ínsito de ejecutividad, a tenor del art. 517.2.5.º LEC, y con la afección patrimonial, especializada ‘in re’ a las resultancias del proceso que representaría el embargo, como derecho frente a todos.

TERCERO

Y en cuanto a la relación de confianza que vincula al deudor solidario, debe partirse de la premisa de que el art. 1.844 CCiv, al establecer el derecho del cofiador que haya pagado a reclamar del resto de cofiadores la parte que proporcionalmente les corresponda satisfacer, instaura también una subrogación en el crédito, lo que es distinto al derecho de reembolso, que nacería con el pago, previa extinción de la deuda primitiva, y que legitimaría sólo en una acción de regreso.

El que el derecho del cofiador que paga no es el mismo que existía antes del pago al acreedor (ya que sólo puede reclamar la parte de cada cofiador), no es argumento, dado que la subrogación opera mediante la adquisición por el cofiador del derecho del acreedor contra el deudor con todos sus accesorios, entre los que se halla la fianza, de manera que se produce una confusión parcial (arts.1.193 y 1.194 CCiv) extintiva del derecho previo al pago en el exceso de la cuota de cada cofiador.

En último lugar, en consonancia con la idea del art. 17.2 párrafo 2.º LEC, que indica no acceder la sucesión procesal cuando se acredite que hay derechos o defensas que, en relación con lo que es objeto del juicio, solamente puedan hacerse valer contra la parte transmitente, admitiendo la subrogación del crédito ejecutivo, los medios de defensa de los cofiadores se amplían, a pesar del tenor del art. 1.845 CCiv, pues aparecen las resistencias que pueden haber surgido del pago, del negocio de fianza o de confianza, o las personales entre quien pasa a ejecutar y los cofiadores.

Por ello, se reabrirá el plazo para la eventual oposición de los ejecutados al despacho de la ejecución, con arreglo a los arts. 557 y ss. LEC.

CUARTO

La deuda ejecutiva, que permanece frente a SS [DENOMINACIÓN SOCIAL], S.L., frente a los cofiadores como ejecutados solidariamente se debe reducir en una tercera parte del principal, ya que un cofiador reclama contra dos que no pagaron, debido ello a una confusión parcial, y al juego del art. 1.837 CCiv en relación con el art. 1.138 CCiv, que en el caso supone reducir la deuda ejecutiva a 24.000 euros, y consecuentemente la cifra presupuestada para intereses, costas y gastos a 7.200 euros, decretándose la reducción de los embargos en dicha cuantía.

Por lo expuesto,

PARTE DISPOSITIVA

1.- Se tiene por personado y parte al Procurador/a de los Tribunales D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de [NOMBRE DEL REPRESENTADO/A], en calidad de sucesor procesal en la posición de parte ejecutante, entendiéndose con dicho mandatario todos los sucesivos ulteriores trámites, ocupando en el proceso la misma posición que ocupaba el, a todos los efectos.

2.- Manteniéndose la reclamación ejecutiva frente a, se declara extinguida la parte proporcional que le correspondía satisfacer ade la deuda ejecutiva, reduciéndose la deuda ejecutiva despachada contray, a la cantidad de [IMPORTE], másque se calculan provisionalmente para intereses y costas del procedimiento ejecutivo, sin perjuicio de ulterior definitiva liquidación, y reduciéndose asimismo los embargos a dicha responsabilidad.

3.- Se declara cesada la representación procesal del [ENTIDAD BANCARIA], y la condición de parte de éste.

4.- Se alza la suspensión del proceso, concediéndose plazo legal al Procurador de los Tribunales D./Dña. [NOMBRE Y APELLIDOS], para que, si de su interés fuere, formalice oposición al despacho de ejecución en nombre dey

Contra esta resolución cabe interponer recurso de reposición, mediante escrito ante este Tribunal que deberá presentarse dentro de los cinco días hábiles siguientes al de notificación, y en el que deberá indicarse la infracción cometida a juicio del recurrente, y sin perjuicio del cual se llevará a efecto lo acordado.

Para interponer el recurso será necesario la constitución de un depósito de 25 euros, sin cuyo requisito no será admitido a trámite. El depósito se constituirá consignando dicho importe en la Cuenta de Depósitos y Consignaciones que este Tribunal tiene abierta en el grupo Banesto (Banco Español de Crédito) con el número [NÚMERO], indicando en el campo concepto del resguardo de ingreso que se trata de un "Recurso" código 00-Reposición. La consignación deberá ser acreditada al interponer el recurso (disp. adic. 15.ª de la LOPJ).

Están exentos de constituir el depósito para recurrir los incluidos en el apartado 5 de la disposición citada y quienes tengan reconocido el derecho a la asistencia jurídica gratuita

Así lo acuerdo, mando y firmo

En [LUGAR], a [FECHA].

Firma del Juez
