---
name: contrato-cesion-solar-cambio-vivienda-local-garaje-civ-0656
description: "Contrato de cesión de un solar a cambio de vivienda, local y garaje futuros. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de cesión de un solar a cambio de vivienda, local y garaje futuros

> Formulario **CIV-0656** del plugin **Propiedad, posesión, servidumbres e hipotecas** (`formularios-propiedad-y-derechos-reales`) · Civil › Propiedad y derechos reales · normativa revisada el 24-11-2026.

## Qué es

Modelo de contrato de cesión de solar a cambio de construcción futura.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de cesión de un solar a cambio de vivienda, local y garaje futuros» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de cesión de un solar a cambio de vivienda, local y garaje futuros” para mi caso». También puedes invocarla directamente con `/formularios-propiedad-y-derechos-reales:contrato-cesion-solar-cambio-vivienda-local-garaje-civ-0656`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-propiedad-y-derechos-reales:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Propiedad, posesión, servidumbres e hipotecas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (8 veces)
- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] FECHA (5 veces)
- [ ] OTROS DATOS (5 veces)
- [ ] DNI/NIE (4 veces)
- [ ] Nº (4 veces)
- [ ] CALLE (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] NACIONALIDAD (2 veces)
- [ ] PLAZO (2 veces)
- [ ] ACTIVIDAD
- [ ] DATOS REGISTRALES
- [ ] DESCRIPCIÓN DEL BIEN
- [ ] FORMA DE PAGO
- [ ] LUGAR
- [ ] NOMBRE DEL NOTARIO
- [ ] Nº DE PLANTAS
- [ ] REFERENCIA CATASTRAL
- [ ] SUPERFICIE
- [ ] TÍTULO DE ADQUISICIÓN

## Normas que cita el formulario

- art. 1279 CC
- art. 1462.2 CC

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

Modelo de contrato de cesión de solar a cambio de construcción futura.


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
(Datos del CEDENTE)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, EL CEDENTE.

Y DE OTRA,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
(Datos del CESIONARIO)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, EL CESIONARIO.

INTERVIENEN

[ELEGIR UNA OPCIÓN: en caso de que todas las partes actúen en nombre y representación propia / si alguna de las partes actúa en su propio nombre y representación]

[OPCIONAL — si alguna de las partes actúa en nombre y representación de persona física o jurídica]
[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de:

[ELEGIR UNA OPCIÓN: Si se trata de persona física / Si se trata de una persona jurídica]

Se reconocen mutuamente con capacidad suficiente para otorgar el presente contrato de CESIÓN DE SOLAR A CAMBIO DE CONSTRUCCIÓN FUTURA y a tal fin,

MANIFIESTAN

I.- Que el CESIONARIO tiene como actividad principal [ACTIVIDAD].

II.- Que el CEDENTE es titular de la siguiente finca: solar sito en [LOCALIDAD], calle [CALLE], con una superficie comprobada de [Nº] metros cuadrados, de los cuales [Nº] metros cuadrados son edificables. Consta de [DESCRIPCIÓN DEL BIEN].

El CESIONARIO manifiesta conocer la ubicación física de la finca, su cabida, linderos y resto de características que la conforman, así como las condiciones urbanísticas del inmueble, las cuales acepta.

Datos registrales: Inscrita en el Registro de la Propiedad de [LOCALIDAD], [DATOS REGISTRALES].

Datos catastrales: [REFERENCIA CATASTRAL].

Título: Pertenece al CEDENTE por título de [TÍTULO DE ADQUISICIÓN] (compraventa, permuta, herencia, etc.) [OTROS DATOS].

Cargas y gravámenes: la finca anteriormente descrita se encuentra libre de cargas y gravámenes (o, en su caso, describir las existentes).

III.-Que el CESIONARIO tiene interés en la adquisición de la finca descrita en la manifestación anterior para la ejecución de un edificio de viviendas, consistente en garajes subterráneos, planta baja y [Nº DE PLANTAS] plantas de alzado, con fachada a la calle [CALLE], según proyecto a desarrollar por el/la Arquitecto/a D./Dña. [NOMBRE Y APELLIDOS] o la persona designada por EL CESIONARIO que le sustituya, en su caso.

IV.- Por todo lo anterior, ambas partes han tenido a bien convenir la cesión de la finca descrita a cambio de la adjudicación de una parte de la construcción a edificar en dicho solar, en las condiciones que luego se dirán, y todo ello de conformidad con las siguientes

ESTIPULACIONES

Primera.- EL CEDENTE transmite, a título de permuta con la construcción que se dirá, el solar descrito en la manifestación II a favor del CESIONARIO, con todos sus derechos, en concepto de libre de cargas y gravámenes, y al corriente de pago de cualesquiera gastos e impuestos.

Las partes se obligan a la evicción y saneamiento, conforme a Derecho, de los bienes objeto de permuta.

Segunda.- En contraprestación a la cesión a que se obliga el CEDENTE, el CESIONARIO se obliga a:

a) realizar cuantos trámites y actuaciones sean precisos para obtener la correspondiente licencia urbanística necesaria para la construcción del EDIFICIO mencionado en la manifestación III, de conformidad con los Memoria y Planos redactados por el/la Arquitecto/a D./Dña. [NOMBRE Y APELLIDOS] o la persona designada por el CESIONARIO que le sustituya, y que se acompañan al presente documento como Anexo I.
b) Construir el EDIFICIO mencionado en la manifestación III atendiendo a lo indicado y al proyecto que redacte el arquitecto y sea aprobado por el Ayuntamiento de [LOCALIDAD].
c) Entregar y transmitir al CEDENTE o a la persona, física o jurídica, que por éste se designe, del dominio de los siguiente inmuebles pertenecientes al EDIFICIO de nueva construcción a levantar sobre el solar:

Piso de superficie [Nº] metros cuadrados.

Local comercial de superficie [SUPERFICIE].

Una plaza de garaje.

El acabado y calidad de los materiales de los bienes a entregar por el CESIONARIO deberán ajustarse a las recogidas en la memoria de calidades que constan en el Anexo.

Su valor, a efectos del presente contrato, se fijará en el momento de otorgamiento de la escritura pública de compraventa, atendiendo al precio de mercado o a los precios que la entidad compradora haya fijado para la promoción y venta de los pisos que formarán parte del edificio.

Tercera.- Todos los gastos y desembolsos que, por cualquier concepto ocasionen la obtención de las licencias, redacción de proyecto y construcción de dicho edificio, cualquiera que sea su clase, correrán a cargo del CESIONARIO. En particular, son de cuenta del CESIONARIO los gastos e impuestos que lleve aparejada la escritura de cesión y permuta del solar, los gastos de escritura de obra nueva y división horizontal, los permisos de obras y avales para la concesión de las licencias, mano de obra, materiales, licencias y demás permisos, seguridad social, seguros de la construcción, honorarios de facultativos y técnicos, (demolición del edificio existente, en su caso), construcción del nuevo edificio y en general todas las que sean precisas, convenientes o necesarias, hasta terminar las obras y por razón de las mismas, hasta la entrega de las unidades registrales que le corresponden al CEDENTE.

Se hace constar de forma expresa que el CEDENTE queda exonerado de cualesquiera responsabilidad que pudiere derivarse de la construcción referida, y en especial, por razón de los empleados del CESIONARIO y cualesquiera otros subcontratados para la construcción del EDIFICIO.

El resto de los gastos e impuestos que se originen por la presente operación serán pagados conforme a la Ley,

Cuarta.- Los plazos en los que el CESIONARIO se obliga a llevar a cabo la construcción del EDIFICIO son los siguientes:

a) Fecha de inicio de las obras: antes del día [FECHA].
b) Fecha de finalización de las obras: antes del día [FECHA].
c) Fecha de entrega de las viviendas, locales comerciales y plazas de garaje: antes del día [FECHA].

El CESIONARIO deberá comunicar la finalización de las obras al CEDENTE con un plazo no superior a [PLAZO] desde la finalización de las mismas.

Quinta.- Las partes se obligan a otorgar la correspondiente escritura pública de permuta con reserva de dominio/con condición resolutoria ante el Notario D./Dña. [NOMBRE DEL NOTARIO], en el plazo máximo de un mes a contar desde la obtención de la licencia municipal de obras para la construcción del referido EDIFICIO, momento en que se producirá la efectiva entrega de la posesión de la finca al CESIONARIO.

En dicha escritura figurará la vivienda, local y plaza de garaje que corresponderá al CEDENTE, de forma que, en su día, éstos consten desde el primer momento titulados a su nombre, ya que con dicha escritura de permuta y con la declaración de obra nueva y división horizontal se instrumentará la posesión jurídica del pleno dominio a nombre del CEDENTE.

El CESIONARIO podrá por sí solo otorgar las escrituras de obra nueva en construcción y constitución de la propiedad horizontal, siempre que exista coincidencia en la descripción de los elementos individuales que consten en las mismas con los anteriormente reseñados.

El CESIONARIO no podrá enajenar ni gravar, sin el consentimiento del CEDENTE, la vivienda, local comercial y plaza de garaje descritos en la cláusula Segunda

Con la inscripción de la escritura de obra nueva y división horizontal en el Registro de la Propiedad, se constatará la titularidad jurídica de dichas fincas a nombre del CEDENTE.

La efectiva entrega de la posesión de la vivienda, local y plaza de garaje al CEDENTE, descrita en el apartado c) de la Estipulación Segunda, se realizará en el plazo máximo de 15 días hábiles a contar desde la recepción definitiva de la obra, salvo que para esa fecha el Ayuntamiento de [LOCALIDAD] no haya concedido aún la cédula de habitabilidad, en cuyo caso la entrega podrá demorarse hasta la concesión de dicha cédula, si bien el CESIONARIO se compromete a realizar todas las gestiones necesarias para su obtención, evitando la demora injustificada. Del mismo modo, también se entregará la documentación necesaria para la ocupación de la vivienda, los boletines de instaladores de los servicios públicos de agua, luz, gas, teléfono, así como los seguros de responsabilidad civil que garanticen durante diez, tres y un año las contingencias que se describen en el artículo 17 de la Ley 38/99, de Ordenación de la Edificación y que el CESIONARIO declara conocer con anterioridad a este momento por ser una norma que afecta directamente a su profesión y actividad.

La entrega al CEDENTE del piso, local comercial y plaza de garaje entregados como contraprestación a la presente permuta se efectuará en perfecto estado de uso, y libres de toda carga y gravamen, inquilinos y precaristas.

Sexta.- El presente contrato se resolverá por el incumplimiento de cualquiera de las partes de cualquiera de las cláusulas del mismo. El incumplimiento deberá notificarse a la otra parte desde el momento en que se conozca el mismo, mediante burofax, en el domicilio señalado en el encabezamiento, poniendo de relieve el motivo de la resolución y concediendo un plazo de diez días para su subsanación. Si transcurrido ese plazo no se subsanara el incumplimiento, la parte no incumplidora podrá resolver el contrato.

Asimismo, el CEDENTE queda facultado para la resolución si el CESIONARIO incurre en causa de disolución, concurso de acreedores o estado de insolvencia antes de la firma de la escritura de compraventa y permuta, o en cualquier otra causa que le lleve a la pérdida de su personalidad jurídica.

Igualmente podrá resolverlo en caso de paralización de las obras durante un plazo superior a [PLAZO].

Asimismo, serán causas objetivas de resolución del contrato el mutuo acuerdo de las partes o la imposibilidad sobrevenida de cumplir con lo pactado en el presente contrato por causas ajenas a la voluntad de las partes de forma definitiva o por un término superior a dos años desde el término pactado para su ejecución y entrega.

En estos dos últimos casos el CEDENTE recuperará la titularidad del solar, debiendo indemnizar [IMPORTE].

Séptima.- Las partes, para cualquier cuestión que se derivara del presente contrato, se someten, con renuncia expresa a su propio fuero si lo tuvieren, a los Tribunales de [LOCALIDAD].

Y para que así conste, suscriben el presente contrato por duplicado ejemplar y a un solo efecto, en el lugar y fecha arriba indicados.

Memoria y Planos del EDIFICIO a construir en el SOLAR, redactados y firmados por el/la Arquitecto/a D./Dña. [NOMBRE Y APELLIDOS]

No es extraño encontrar este tipo de operaciones en las que un promotor adquiere un solar y la contraprestación que satisface por dicha adquisición consiste en la entrega, al cedente del solar, de alguna de las viviendas, locales, garajes, etc. que se construirán sobre el mismo.

En cuanto a su naturaleza jurídica, existe cierta discrepancia entre la doctrina científica más autorizada y la Jurisprudencia. Mientras la primera le da el tratamiento de contrato de permuta con prestación subordinada de obra, la segunda reiteradamente lo ha calificado como un contrato atípico do ut des, si bien con ciertos rasgos de la permuta, y no subsumible en ninguna de las figuras del Código Civil.

La permuta no es necesario que conste por escrito, estableciéndose en el art. 1279 CC la facultad de las partes de compelerse recíprocamente para formalizarla por escrito desde que haya intervenido el consentimiento y demás requisitos necesarios para su validez. No obstante, al tratarse de permuta de inmuebles, es aconsejable que se firmen ante Notario o, en caso de constar en documento privado, que se eleve éste a escritura pública para poder ser objeto de inscripción en el Registro de la Propiedad.

Por tanto si para que opere el traspaso dominical es necesario en nuestro CC que exista título y modo, es claro que aquél contrato es, sea cual sea su naturaleza, título suficiente para operar aquélla transmisión, como así acaeció al otorgarse la pertinente escritura pública, que pasó a convertirse ya, aparte de la posesión material [OTROS DATOS] en tradición instrumental prevista en el art. 1462.2 CC, de modo que ese instrumento luego permitiría que el Registro de la Propiedad publicase aquélla titularidad [OTROS DATOS] La sentencia del (TS de 9 de octubre de 1997) explica cómo puede darse en estos contratos la transmisión de la propiedad del solar, a diferencia de la obra a construir, respecto de la que [OTROS DATOS] de esa misma escritura no es posible inferir que su otorgamiento equivalga al cumplimiento del requisito de la tradición o modo de adquirir respecto a la cosa que se obligó a entregar la compradora como parte del precio [OTROS DATOS] porque en realidad tratábase de la entrega de una cosa futura, inexistente en el momento de perfeccionarse el contrario, de tal manera que el pacto, al versar sobre una cosa speratae, aunque esté determinada, sólo produce efectos obligaciones entre las partes contratantes, requiriéndose para que pueda desplegar efectos traslativos de domino sobre la obra, como dice la Sentencia de esta Sala de 15 de junio de 1992, que, una vez terminada, medie el inexcusable requisito de la entrega o traditio". (AP 17-2-2004)

La Comunidad Autónoma de Cataluña cuenta con regulación expresa relativa a este contrato, al que denomina de cesión de finca o de edificabilidad a cambio de construcción futura (arts. 621.58 y ss. Código Civil de Cataluña).

Téngase en cuenta que, tratándose de bienes inmuebles se precisará escritura pública para su acceso al Registro de la Propiedad. Pues bien, a partir del 1 de diciembre de 2006, fecha de entrada en vigor de la Ley 36/2006, de 29 de noviembre, de medidas de prevención contra el fraude fiscal por la que se modifica, entre otras, la Ley del Notariado, establece la obligatoriedad de la consignación del Número de Identificación Fiscal (NIF) y de los medios de pagoempleados en las escrituras notariales relativas a actos y contratos sobre bienes inmuebles. La efectividad de estas prescripciones queda garantizada al fijarse como requisito necesario para la inscripción en el Registro de la Propiedad de tales escrituras.

Sobre la forma de registrar las adquisiciones de solares a cambio de construcciones futuras realizadas por empresas inmobiliarias y la cesión de solares y edificaciones realizadas en aplicación de la normativa urbanística, véase (Consulta ICAC 8/15)

( Es aconsejable incluir un plano del solar).

OPCIÓN DE RESERVA DE DOMINIO: No obstante el CEDENTE se reserva el dominio del solar hasta que se formalice la escritura pública correspondiente a la presente permuta (o bien, hasta el día en que se formalice la entrega de la construcción que se señala en la cláusula siguiente), pudiendo solicitarse la inscripción de esta reserva de dominio en el Registro de la Propiedad.

OPCIÓN DE CONDICIÓN RESOLUTORIA (art. 13 RH): La presente permuta está condicionada a que por parte del CESIONARIO se cumplan los requisitos de edificación y entrega del piso, local comercial y plaza de garajes que se detallan en la cláusula siguiente. Por lo tanto, la propiedad del suelo queda afectada al cumplimiento de las estipulaciones pactadas en este contrato, que tendrán el carácter de condiciones resolutorias expresas, pudiendo solicitarse su inscripción en el Registro de la Propiedad.

OPCIÓN DE CONDICIÓN SUSPENSIVA: La perfección y eficacia de esta permuta se halla sujeta al cumplimiento de la condición suspensiva de que se obtenga la licencia municipal del Ayuntamiento de [LOCALIDAD] a favor del CESIONARIO a que se refiere la estipulación Segunda a) para la construcción del EDIFICIO que en la misma se cita. El plazo de pendencia de la citada condición finaliza el [FECHA], de modo que, si llegado el mismo no se hubiere cumplido esta condición suspensiva, el presente contrato perderá su eficacia, sin que el CESIONARIO pueda reclamar al CEDENTE ninguna cantidad por razón de los gastos que hasta entonces hubiere efectuado.

OPCIÓN (para el caso de que se estime que los bienes permutados vayan a ser de diferente valor): El valor del solar entregado en permuta se considera que es de [IMPORTE] euros.

OPCIONES:

Las fincas serán elegidas libremente por el CEDENTE, con derecho preferente a cualquier otra persona que tenga intención de adquirir la propiedad de cualquiera de las viviendas, locales, y plazas de garaje que se van a construir; o bien puede pactarse, si se cuenta con los proyectos y planos, cuáles serán las fincas concretas objeto de la permuta.

OPCIONES:

En su caso, la diferencia de valores entre los bienes inmuebles objeto de la permuta se apreciará a fecha de la entrega del piso, local y plaza de garaje descritos, y se compensará con dinero que deberá de ser satisfecho por la parte cuyo bien resulte de valor superior en el plazo máximo de [Nº] días a contar desde la fecha de dicha entrega mediante escritura de ante Notario [FORMA DE PAGO] (detallar forma de pago y sujeto a favor del que, en cada caso, deba realizarse el pago).

A partir del 1 de diciembre de 2006, fecha de entrada en vigor de la Ley 36/2006, de 29 de noviembre, de medidas de prevención contra el fraude fiscal por la que se modifica, entre otras, la Ley del Notariado, establece la obligatoriedad de la consignación del Número de Identificación Fiscal (NIF) y de los medios de pago empleados en las escrituras notariales relativas a actos y contratos sobre bienes inmuebles. La efectividad de estas prescripciones queda garantizada al fijarse como requisito necesario para la inscripción en el Registro de la Propiedad de tales escrituras.

(OPCIONAL: excepto todos los gastos derivados de la permuta del piso, local comercial y plaza de garaje, respecto de los cuales el CESIONARIO asume la obligación de abonar los gastos de otorgamiento de la escritura, así como el IVA que grava la transmisión, quedando libre el CEDENTE de abonar cualquier gasto por los conceptos indicados).

OPCIÓN para el caso de que en el solar permutado exista alguna edificación que deba ser demolida: El CESIONARIO demolerá por su cuenta y riesgo el edificio existente en el solar descrito en la manifestación II.

OPCIÓN: En garantía del cumplimiento de las obligaciones de transmisión y adjudicación de la titularidad del piso, local comercial y plaza de garaje a favor de la parte vendedora, así como de su entrega de la posesión jurídica y material totalmente terminados y dispuestos para su uso, el CESIONARIO entregará, simultáneamente al otorgamiento de la escritura de compraventa y permuta del solar, un aval bancario por un importe equivalente al valor de la vivienda, local comercial y plaza de garaje, que se determinará atendiendo al valor de mercado y precio fijado para la promoción de las viviendas. Dicho aval deberá ser solidario, a primer requerimiento y con renuncia expresa a los beneficios de división y exclusión. El aval se cancelará y quedará sin efecto el día en que sean entregados la vivienda, loca y plaza de garaje al CEDENTE, completamente libres de cargas y gravámenes y cumplidos los demás requisitos establecidos, en particular la entrega en el plazo establecido en este contrato.
