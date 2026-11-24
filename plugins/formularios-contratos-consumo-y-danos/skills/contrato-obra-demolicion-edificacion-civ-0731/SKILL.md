---
name: contrato-obra-demolicion-edificacion-civ-0731
description: "Contrato de obra para la demolición de una edificación. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de obra para la demolición de una edificación

> Formulario **CIV-0731** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Modelo de contrato de ejecución de obras de demolición.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de obra para la demolición de una edificación» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de obra para la demolición de una edificación” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:contrato-obra-demolicion-edificacion-civ-0731`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] Nº (5 veces)
- [ ] DNI/NIE (4 veces)
- [ ] FECHA (3 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] NACIONALIDAD (2 veces)
- [ ] DESCRIPCIÓN DEL BIEN
- [ ] FORMA DE PAGO
- [ ] IMPORTE
- [ ] LUGAR
- [ ] PLAZO
- [ ] ÓRGANO

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

En [LUGAR], a [FECHA]
REUNIDOS

DE UNA PARTE,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
(Datos del CLIENTE)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, EL CLIENTE.

Y DE OTRA,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
(Datos de LA EMPRESA)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, LA EMPRESA.

INTERVIENEN

[ELEGIR UNA OPCIÓN: en caso de que todas las partes actúen en nombre y representación propia / si alguna de las partes actúa en su propio nombre y representación]

[OPCIONAL — si alguna de las partes actúa en nombre y representación de persona física o jurídica]
[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de:

[ELEGIR UNA OPCIÓN: Si se trata de persona física / Si se trata de una persona jurídica]

Ambas partes se reconocen mutuamente con capacidad suficiente para otorgar el presente contrato de EJECUCIÓN DE OBRAS DE DEMOLICIÓN y, a tal fin,

MANIFIESTAN

I.- EL CLIENTE es propietario del siguiente inmueble [DESCRIPCIÓN DEL BIEN] Tiene una superficie aproximada de [Nº] metros cuadrados, y un volumen a demoler de [Nº] metros cúbicos.

II.- LA EMPRESA tiene como actividad principal la ejecución de obras de demolición, y está al corriente en el cumplimiento de sus obligaciones fiscales y para con la Seguridad Social, e interesada en ejecutar las obras objeto del presente contrato.

III.- Que EL CLIENTE está interesado en contratar a LA EMPRESA para el desarrollo de un proyecto consistente en la demolición de obra/ derribo de finca, la cual se describe en el Anexo I al Contrato (en adelante EL PROYECTO).

IV.-Que considerando EL CLIENTE, que LA EMPRESA posee la capacidad precisa para efectuar EL PROYECTO que EL CLIENTE requiere, por cuanto puede disponer de la organización y de los medios necesarios para llevarlo a cabo, ambas partes han venido en pactar el presente Contrato DE EJECUCIÓN DE OBRAS DE DERRIBO, que acuerdan sujetar a las siguientes

CLÁUSULAS

PRIMERA.- Objeto del contrato

Por medio del presente, la contrata se compromete a ejecutar las obras de demolición del edificio descrito en la Manifestación Primera, ajustándose al Proyecto que se acompaña como Anexo I, redactado por el Arquitecto D. [NOMBRE Y APELLIDOS] y al estudio (o estudio básico) de seguridad y salud redactado por el técnico D. [NOMBRE Y APELLIDOS], encargo que recibe de la propiedad, y cuya ejecución acepta de conformidad con el contenido del presente contrato y bajo la dirección de dicho profesional.

SEGUNDA.- Duración

Las obras, que tendrán una duración máxima de [PLAZO], darán comienzo el día [FECHA], previa la firma del acta de replanteo, debiendo por tanto quedar concluidas el día [FECHA] La duración del presente contrato queda condicionada a la concesión de la LICENCIA DE DERRIBO que se requiere para su realización, tramitada ante [ÓRGANO] (datos de la licencia).

A partir del [Nº] día siguiente a la fecha pactada para la terminación de las obras, el contratista se verá penalizado a razón del % y día sobre el presupuesto de contrata, excluido IVA, salvo que el retraso se produzca por causa de fuerza mayor o cualquier otra circunstancia que no le sea imputable.

TERCERA.- Contraprestación

LA EMPRESA recibirá del CLIENTE como contraprestación por la ejecución del PROYECTO una remuneración de [IMPORTE] euros, incrementada por los gastos generados en la tramitación de la LICENCIA, los cuales necesariamente serán determinados ‘a posteriori’ por LA EMPRESA, siendo documentados con la presentación de las correspondientes facturas ya satisfechas por LA EMPRESA.

A estos efectos:

a) Serán de cuenta exclusiva del CLIENTE los honorarios de proyecto y dirección de obra, así como la tasa y el impuesto correspondiente para la obtención de la preceptiva licencia.
b) Serán de cuenta exclusiva de LA EMPRESA todos los trabajos necesarios, sin excepción alguna, para la ejecución de las obras, así como los materiales y elementos de toda índole que fueren precisos, y la realización y colocación del cartel de obras, de acuerdo con las directrices del órgano competente y con el diseño facilitado por la propiedad, así como el consumo de agua y energía eléctrica que precisen para la realización de su trabajo.

CUARTA.- Forma de pago

La cantidad de dinero mencionada anteriormente será abonada de la forma indicada a continuación, a partir de la fecha de inicio de la prestación:

[FORMA DE PAGO]

La factura incluirá, además del precio de los servicios antes referidos, los impuestos que legalmente deban repercutirse.

QUINTA.- Prestación del servicio

1) En virtud del presente Contrato, LA EMPRESA se compromete a realizar EL PROYECTO, con plena sujeción a la normativa vigente en la materia.

2) LA EMPRESA realizará todos los trámites exigidos por la Ordenanza Municipal del lugar que sean necesarios para la concesión de la LICENCIA. Los gastos ocasionados en la tramitación de la LICENCIA serán a cuenta del CLIENTE, siendo identificados como tales por LA EMPRESA en la factura del precio del PROYECTO.

3) LA EMPRESA, en el desempeño del PROYECTO, actuará diligentemente cumpliendo con las responsabilidades profesionales correspondientes y propias del sector. Asimismo, cumplirá la legislación vigente en la materia, en especial, en materia urbanística y medioambiental, tanto de carácter nacional como autonómica y local.

4) LA EMPRESA informará regularmente al CLIENTE de la marcha del PROYECTO.

5) Asimismo, por el presente Contrato LA EMPRESA se compromete a tener personas a disposición plena del CLIENTE para cualesquiera de las consultas que éste demande.

6) Durante la ejecución del PROYECTO y consiguientemente durante la vigencia del presente Contrato, será por cuenta de LA EMPRESA el personal necesario en la ejecución del PROYECTO, debiendo en todo momento cumplir estrictamente las obligaciones derivadas de la Legislación Laboral vigente.

7) EL CLIENTE se compromete a facilitar a LA EMPRESA toda la documentación necesaria sobre la finca que obre en su poder y sea exigida en el procedimiento de otorgamiento de la LICENCIA.

8) EL CLIENTE responderá de los gastos ocasionados en la tramitación de la licencia por LA EMPRESA, ante una eventual denegación de la misma por los órganos competentes a efecto.

9) Una vez terminadas las obras, LA EMPRESA queda obligada a desmontar, demoler y transportar fuera de la zona de la obra toda maquinaria inútil y todos los elementos, materiales y escombros resultantes de la demolición, debiendo entregar el solar expedito y limpio. Dichas operaciones se realizarán a su costa.

SEXTA.- Responsabilidad

La EMPRESA asume la total y exclusiva responsabilidad en relación con todos los operarios que emplee en la ejecución de las obras, cumpliendo exactamente todo lo previsto en la Ley de Prevención de Riesgos Laborales y demás normativa que la complementa y desarrolla, utilizando sus obreros el régimen legal de alto en los seguros sociales y debidamente asegurados contra accidentes de trabajo. Igualmente asume todas las responsabilidades laborales de Seguridad Social, económica, criminales y civiles, incluso los daños a terceros y especialmente a las propiedades colindantes, que pudieran derivarse de la realización de las obras y de todos los trabajos que ejecuten los elementos laborales.

La EMPRESA tiene suscrita una póliza de responsabilidad civil para hacer frente a las posibles indemnizaciones que pudieren derivarse de los trabajos a realizar. Copia de dicha póliza queda incorporada al presente contrato como Anexo [Nº].

SÉPTIMA.- Causas de resolución

Las partes aceptan que serán causas de terminación del Contrato, sin perjuicio de los daños y perjuicios que pudiesen corresponder:

a) Ante la eventual denegación de la necesaria LICENCIA DE OBRA MAYOR.
b) El vencimiento del plazo establecido en la cláusula segunda.
c) El incumplimiento por cualquiera de las partes de alguna de las obligaciones que le incumbe cumplir en virtud de este Contrato, siempre que dicho incumplimiento no se subsane en el plazo improrrogable de [Nº] días hábiles a contar desde la recepción de la necesaria notificación por parte de la parte incumplidora.
d) La quiebra o la solicitud de quiebra voluntaria o suspensión de pagos de cualquiera de las partes, o el hecho de que se hayan instado en contra de alguna de las partes juicios ejecutivos o decretado embargos preventivos u otras medidas cautelares que pongan de manifiesto la disminución de la solvencia económica o dificultades financieras para atender al normal cumplimiento de las obligaciones.
e) Las establecidas legalmente.
f) Las establecidas en el clausulado del presente Contrato.

OCTAVA.- Legislación aplicable y fuero competente

El presente contrato se rige por sus propias disposiciones y, en lo no previsto en ellas, por las normas del Código Civil relativas al contrato de arrendamiento de obras y servicios, y las generales de obligaciones y contratos y demás que le sean de aplicación.

En caso de controversia entre las partes surgida de este contrato, ambas, con renuncia expresa a su propio fuero se someten a la jurisdicción de los Tribunales de [LOCALIDAD].

Y, en prueba de conformidad con cuanto antecede, firman por duplicado en el lugar y fecha del encabezamiento.

EL CLIENTE

LA EMPRESA
