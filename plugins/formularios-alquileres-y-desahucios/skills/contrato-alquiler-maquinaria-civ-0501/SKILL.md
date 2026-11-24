---
name: contrato-alquiler-maquinaria-civ-0501
description: "Contrato de alquiler de maquinaria. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de alquiler de maquinaria

> Formulario **CIV-0501** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 24-11-2026.

## Qué es

Contrato mediante el cual una persona (arrendador) cede a otra (arrendatario) el goce o uso de un bien mueble (maquinaria) por un tiempo determinado y a cambio del pago de una renta.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de alquiler de maquinaria» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de alquiler de maquinaria” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:contrato-alquiler-maquinaria-civ-0501`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] PLAZO (6 veces)
- [ ] DNI/NIE (4 veces)
- [ ] IMPORTE (3 veces)
- [ ] FECHA (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NACIONALIDAD (2 veces)
- [ ] USO DE LA MÁQUINA (2 veces)
- [ ] ACCESORIOS
- [ ] ACTIVIDAD
- [ ] AÑO
- [ ] DESCRIPCIÓN DEL BIEN
- [ ] DÍA
- [ ] LUGAR
- [ ] NOMBRE DE LA PARTE
- [ ] NÚMERO
- [ ] OTROS DATOS
- [ ] SERIE

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

Contrato mediante el cual una persona (arrendador) cede a otra (arrendatario) el goce o uso de un bien mueble (maquinaria) por un tiempo determinado y a cambio del pago de una renta.


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

En [LUGAR], a [FECHA]
REUNIDOS

DE UNA PARTE,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
(Datos del ARRENDADOR)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, ARRENDADOR.

Y DE OTRA,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
(Datos del ARRENDATARIO)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, ARRENDATARIO.

INTERVIENEN

[ELEGIR UNA OPCIÓN: en caso de que todas las partes actúen en nombre y representación propia / si alguna de las partes actúa en su propio nombre y representación]

[OPCIONAL — si alguna de las partes actúa en nombre y representación de persona física o jurídica]
[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de:

[ELEGIR UNA OPCIÓN: Si se trata de persona física / Si se trata de una persona jurídica]

Ambas partes se reconocen mutuamente con capacidad suficiente para otorgar el presente contrato de ARRENDAMIENTO DE MAQUINARIA y, a tal fin,

EXPONEN

I.- Que el Arrendador es el propietario de la maquinaria o herramienta y objeto de este contrato y que tiene las siguientes características:

Nombre de marca y descripción de la máquina [DESCRIPCIÓN DEL BIEN].

Número de modelo o serie [SERIE].

Año de fabricación [AÑO].

Accesorios [ACCESORIOS].

Otros [OTROS DATOS].

II.- Que el Arrendatario quiere alquilar la máquina o herramienta para uso profesional o personal en [ACTIVIDAD]:

III.- Que este arrendamiento comprende la máquina o herramienta y sus accesorios.
IV.- Que la máquina o herramienta se utilizará [USO DE LA MÁQUINA]

V.- Que el Arrendador y el Arrendatario han alcanzado un acuerdo en virtud del cual se someten a las siguientes:

CLÁUSULAS

Primera.- Objeto

El presente contrato tiene por objeto el arrendamiento sin operador de la máquina que se relaciona en expositivo I del presente contrato.

El arrendador, legítimo titular de los bienes objeto del presente contrato, cede su uso y disfrute en correcto estado de funcionamiento, seguridad y con todos sus accesorios al arrendatario, quien los recibe manifestando su conformidad.

Segunda.- Entrega

En este mismo acto, el arrendador hace entrega del conjunto de los bienes muebles objeto del Contrato, poniéndolo en poder y posesión del arrendatario, que lo recibe. A partir de esta entrega, la PARTE ARRENDATARIA se hace cargo de las responsabilidades derivadas de su tenencia y uso.

En este mismo acto, el arrendador hace entrega del conjunto de los bienes muebles objeto del Contrato, poniéndolo en poder y posesión del arrendatario, que lo recibe. A partir de esta entrega, la PARTE ARRENDATARIA se hace cargo de las responsabilidades derivadas de su tenencia y uso.

La puesta a disposición de la maquinaria arrendada transmite el deber de guardia y custodia al arrendatario o a la persona autorizada por él, durante la vigencia del contrato quien asume toda la responsabilidad de su conservación

El arrendatario reconoce haber recibido el bien en perfecto estado de conservación manifestando su total conformidad con el mismo obligándose a devolverlo en igual estado, a salvo de los deterioros normales producidos por el uso.

Tercera.- Uso y destino

La maquinaria objeto de este Contrato será destinada por el arrendatario única y exclusivamente al siguiente uso o destino: [USO DE LA MÁQUINA].

Dicho uso no podrá ser modificado sin el consentimiento previo, expreso y por escrito del Arrendador.

Igualmente, el arrendatario se obliga a no realizar ningún uso o disposición de la maquinaria que sea de carácter ilícito, o contraria a la Ley, la moral o el orden público, o que de cualquier otro modo pueda acarrear lesión o daños a terceras personas, cosas, o al propio bien.

La maquinaria objeto de este contrato solo puede ser utilizada por el personal autorizado de [NOMBRE DE LA PARTE].

El [ELEGIR: Arrendatario / Arrendador] es responsable de que las personas que utilicen la herramienta o maquinaria estén debidamente cualificadas para ello. También de que estos usuarios la utilicen siempre en circunstancias óptimas de trabajo.

En caso de modificaciones del personal autorizado, el [ELEGIR: arrendador / arrendatario] deberá comunicar dicha circunstancia de modo fehaciente en el plazo de [PLAZO].

[OPCIONAL — incluir si procede]

(Si se determina el lugar de uso y el derecho de inspección)

El Arrendatario está obligado a utilizar el bien exclusivamente en la obra o ubicación indicadas en el Contrato y además tendrá la obligación de dejar comprobar al Arrendador el estado de la máquina o herramienta en todo momento.

El incumplimiento de cualquiera de estos requisitos será motivo de resolución del contrato debiendo el arrendatario devolver la máquina a su propietario.

Cuarta.- Reparaciones

Serán de cuenta y cargo del arrendatario todas las reparaciones ordinarias y extraordinarias que este necesite durante el período de vigencia del Contrato. Para ello, el arrendatario deberá notificarlo al arrendador con carácter previo a la realización de cualquiera de estas reparaciones, salvo casos de urgencia

El arrendatario se compromete a acatar las normas que indique el Arrendador para siempre tener la máquina o la herramienta en perfectas condiciones.

Quinta.- Duración

El arrendamiento se pacta por el plazo de [PLAZO], a contar desde la entrega del conjunto de los bienes objeto de este contrato, finalizando automáticamente el día [FECHA].

[OPCIONAL — incluir si procede]

(Si se acuerdan prórrogas)

El plazo de presente contrato se acuerda y pacta por un tiempo de [PLAZO], pudiendo prorrogarse, a voluntad de las partes, y de común acuerdo, por períodos anuales. Llegado el día del vencimiento, si una de las partes decidiera rescindir el presente contrato unilateralmente, antes de la fecha pactada para su vencimiento, habrá de comunicárselo a la otra parte, al menos con [PLAZO] de anticipación, en caso contrario, el presente contrato se prorrogará y la renta pactada se revisará, aumentándose o disminuyéndose, según los índices ponderados de vida que publique el Instituto Nacional de Estadística u Organismo que pueda sustituirle.

[OPCIONAL — incluir si procede]

(Vencimiento anticipado)

Tanto el arrendatario como el arrendador tendrán derecho a desistir anticipadamente del Contrato. La Parte que desista deberá notificarlo, expresamente y por escrito, a la otra con como mínimo de [PLAZO] de antelación.

No obstante, ambas Partes son conscientes de que el ejercicio del derecho de desistimiento aquí otorgado sin respetar el preaviso indicado podría acarrear el pago de una indemnización por daños y perjuicios o de una penalidad.

En cualquier caso, a la finalización del contrato el arrendatario deberá devolver el conjunto de bienes muebles alquilados al arrendador, respetando lo dispuesto en el presente documento.

Sexta.- Precio

El precio o renta que se pacta es de [IMPORTE] euros, pagadera por meses adelantados del [DÍA] al de cada mes.

Las mensualidades pactadas en concepto de canon arrendaticio serán satisfechas por el arrendatario en la cuenta corriente nº [NÚMERO] del arrendador.

El precio se fija por un máximo de ocho horas de trabajo diarias. Las horas que sobrepasen la jornada laboral (ocho horas), se incrementará a la facturación, teniendo en cuenta las horas trabajadas. Las jornadas de doble o triple turno deberán comunicarse al arrendador, para controlar el mantenimiento y conservación de la máquina.

El arrendador recibe en este acto y fecha la cantidad de [IMPORTE] euros correspondientes a la primera de las mensualidades, surtiendo el presente documento efectos de carta de pago en cuanto a su importe.

El incumplimiento por el arrendatario de la obligación de pago de la renta en el plazo fijado será motivo de resolución del Contrato, debiendo en tal caso restituir inmediatamente el conjunto de bienes al arrendador, siendo por cuenta del arrendatario los gastos que la resolución pudiera ocasionar, así como el interés de demora legalmente establecido incluidos los honorarios de abogado y procurador [ELEGIR: sin son / aunque no fuesen] preceptivos.

[OPCIONAL — incluir si procede]

Séptima.- Fianza

El arrendatario entrega al arrendador la cantidad de [IMPORTE] euros, en concepto de fianza y garantía adicional, que será restituida, en su integridad o mermando la cantidad que sea necesaria en caso de daños, a la finalización de este contrato. La existencia de ésta fianza no será obstáculo para que el arrendador pueda instar la resolución del contrato en caso de falta de pago. La fianza no devengará interés a favor del arrendatario, quedando facultado el arrendador para practicar la liquidación hacedera según los perjuicios que se hubieren causado en la máquina arrendada.

.- Extras, gastos suplidos no incluidos

[ELEGIR UNA OPCIÓN: Todos a cargo del arrendatario / Algunos a cargo del arrendatario)]

.- Subarriendo y cesión

Se prohíbe a la ARRENDATARIA ceder, subrogar, subarrendar o efectuar cualquier otro tipo de transmisión, total o parcial, de la máquina objeto del presente contrato.

.- Seguros

[ELEGIR UNA OPCIÓN: Suscrito por el arrendador / Suscrito por el arrendatario]

.- Responsabilidad frente a terceros

El arrendatario se hace directa y exclusivamente responsable, y exime de toda responsabilidad al arrendador, por los daños que puedan ocasionarse a personas o cosas y sean derivados de la utilización correcta o incorrecta de la maquinaria arrendada, sin perjuicio de las acciones que pudieran corresponderle frente a terceros.

.- Concurso, secuestro o embargo

En caso de concurso de acreedores de la ARRENDATARIA, secuestro, embargo o cualquier otro acto procedente de organismos administrativos o judiciales o de particulares que pretendan perturbar la posesión o dominio de la máquina objeto del presente contrato, la ARRENDATARIA se compromete a efectuar las oportunas manifestaciones sobre la existencia del presente contrato de arrendamiento, señalando su posición de simple usuario, y obligándose a comunicarlo a la ARRENDADORA de manera fehaciente en el plazo de [PLAZO], para que ésta pueda proceder a la defensa de sus derechos. En estos casos la ARRENDADORA podrá resolver el presente contrato de manera unilateral y sin preaviso..

.- Robo y otras contingencias

El arrendador se obliga a notificar inmediatamente a la policía o a las autoridades pertinentes en caso de robo, pérdida, incendio, daños causados por animales u otros perjuicios y a obtener un atestado o informe certificado de las circunstancias en las que se produjo el incidente. Asimismo, se compromete a informar al arrendador de cualquier contingencia que afecte a la maquinaria.

.- Causas de resolución del contrato

El contrato se extinguirá en los supuestos siguientes:

-Por el transcurso del plazo de duración del Contrato en los términos establecidos en la cláusula 5.
-Por mutuo acuerdo de las partes.
- Por incumplimiento de las obligaciones de pago del arrendatario, en cuyo caso el presente documento sirve como autorización expresa del arrendatario para que el arrendador proceda a la retirada de la maquinaria y accesorios arrendados, cualquiera que sea el lugar donde ese material se encuentre.

En todo caso el arrendatario estará obligado a abonar la totalidad del precio del arrendamiento vencido y no pagado, con sus intereses moratorios correspondientes. Igualmente serán de cuenta del arrendatario los gastos en que incurra el arrendador por la retirada de la máquina y sus accesorios.

.- Confidencialidad

El arrendatario se obliga a no revelar, ceder o transferir a terceros ninguna información referente a los negocios, clientes, operaciones, instalaciones, cuentas o finanzas del a arrendador, ni sus procedimientos, métodos, transacciones, "know-how", o cualquier otro aspecto relacionado con la actividad de dicha entidad que pueda conocer o haya conocido con motivo de la prestación de servicios prevista en el presente contrato.

El arrendatario se responsabilizará de que las personas que están a su cargo se sujeten a las limitaciones establecidas en esta cláusula.

El incumplimiento de este compromiso conllevará la obligación de indemnizar los daños y perjuicios causados.

.- Formalización

Cualquiera de las partes podrá elevar a escritura pública este contrato e inscribirlo en el Registro de la Propiedad siendo los gastos, que esta elevación a público e inscripción conlleve, asumidos por la Parte que lo promueva.

.- Notificaciones

Las partes señalan como domicilios para la práctica de las notificaciones necesarias en la ejecución del presente contrato:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

[NOMBRE Y APELLIDOS]

.- Protección de datos personales

Las Partes de este Contrato conocen y se obligan a cumplir la Ley Orgánica 3/2018, de 5 de diciembre, de Protección de Datos Personales y garantía de los derechos digitales y consienten la incorporación de sus datos personales en el fichero automatizado de la contraparte.

.- Gastos e Impuestos

Todos los impuestos, gastos judiciales o extrajudiciales originados a consecuencia de la celebración del presente contrato serán de cuenta del [ELEGIR: arrendador / arrendatario].

.- Naturaleza del contrato y normativa aplicable

El presente contrato tiene naturaleza mercantil, rigiéndose por lo dispuesto en sus propias cláusulas y en lo en ellas no previsto por las disposiciones Código de Comercio, leyes especiales y usos mercantiles que le sean aplicables, o en lo no previsto, por las disposiciones del Código Civil.

.- Fuero competente

[ELEGIR UNA OPCIÓN: Tribunales / Cláusula de arbitraje]

Y en prueba de conformidad con todo ello firman el presente documento por duplicado ejemplar y a un solo efecto en el lugar y fecha expresados en el encabezamiento.

EL ARRENDADOR

EL ARRENDATARIO

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]
