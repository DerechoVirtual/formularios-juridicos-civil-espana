---
name: contrato-traspaso-local-negocio-civ-0496
description: "Contrato de traspaso de local de negocio. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de traspaso de local de negocio

> Formulario **CIV-0496** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 24-11-2026.

## Qué es

Contrato por el que el arrendatario o inquilino de un local de negocio (Cedente) transmite a un tercero (Cesionario) el conjunto de los derechos y obligaciones que le corresponden en virtud del contrato de arrendamiento firmado con el propietario del inmueble. De esta forma, el arrendatario (o cedente) desaparece del contrato de arrendamiento y el tercero (Cesionario) ocupa su lugar.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de traspaso de local de negocio» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de traspaso de local de negocio” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:contrato-traspaso-local-negocio-civ-0496`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (10 veces)
- [ ] IMPORTE (9 veces)
- [ ] DNI/NIE (5 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] Nº (3 veces)
- [ ] FECHA (2 veces)
- [ ] NACIONALIDAD (2 veces)
- [ ] Nº DE ANEXO (2 veces)
- [ ] ACTIVIDAD
- [ ] CALLE
- [ ] CONCEPTO DE LA REPERCUSIÓN
- [ ] DATOS REGISTRALES
- [ ] DIRECCIÓN
- [ ] LUGAR
- [ ] NOMBRE DE LA PARTE
- [ ] NÚMERO
- [ ] SUPERFICIE

## Normas que cita el formulario

- art. 32 Ley 29/1994
- art. 1851 Código Civil

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

Contrato por el que el arrendatario o inquilino de un local de negocio (Cedente) transmite a un tercero (Cesionario) el conjunto de los derechos y obligaciones que le corresponden en virtud del contrato de arrendamiento firmado con el propietario del inmueble. De esta forma, el arrendatario (o cedente) desaparece del contrato de arrendamiento y el tercero (Cesionario) ocupa su lugar.


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

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, CEDENTE.

Y DE OTRA,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, CESIONARIO.

INTERVIENEN

[ELEGIR UNA OPCIÓN: en caso de que todas las partes actúen en nombre y representación propia / si alguna de las partes actúa en su propio nombre y representación]

[OPCIONAL — si alguna de las partes actúa en nombre y representación de persona física o jurídica]
[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de:

[ELEGIR UNA OPCIÓN: Si se trata de persona física / Si se trata de una persona jurídica]

Ambas partes se reconocen mutuamente con capacidad suficiente para otorgar el presente contrato de cesión o traspaso de Local de Negocio, a tal fin,

MANIFIESTAN

I. Que el CEDENTE es arrendatario del local de negocio localizado en [DIRECCIÓN] con una superficie de [SUPERFICIE] El local se encuentra inscrito en el Registro de la Propiedad de:, con los siguientes datos: [DATOS REGISTRALES]. En adelante, este será denominado el "Local".

II. Que el contrato de arrendamiento sobre el Local fue celebrado el [FECHA], siendo la parte arrendadora en dicho contrato de arrendamiento y propietaria del Local: (en adelante, el "ARRENDADOR"). Se adjunta como Anexo al presente contrato una copia simple de dicho documento de arrendamiento.

III. Que el CEDENTE ejerce en el Local la siguiente actividad: y cuenta con todas las autorizaciones, permisos y/o licencias necesarios para el ejercicio de dicha actividad.

[ELEGIR UNA OPCIÓN: Al día en los pagos / Con deudas]

IV. Que el mobiliario, las existencias, los útiles y/o las instalaciones necesarias para la realización de la actividad descrita en la Manifestación anterior y situados en el propio local son propiedad del CEDENTE. Se incorpora al presente documento un Anexo de inventario de bienes muebles, con el mobiliario, las existencias, los útiles y/o las instalaciones existentes en el Local y su estado de uso y conservación al momento de firmarse este documento.

V. Que el CEDENTE está interesado en la cesión de su contrato de arrendamiento sobre el Local, así como del mobiliario, las existencias, los útiles y/o las instalaciones que se encuentran en el mismo, y tiene capacidad legal para la celebración de este contrato.

VI. Que el CEDENTE notificó al propietario-ARRENDADOR, por conducto del Notario de esta ciudad D./Dª [NOMBRE Y APELLIDOS], Acta número [NÚMERO] de su Protocolo que se adjunta como Anexo [Nº DE ANEXO], su decisión de traspasar el local y el precio del mismo, habiendo transcurrido más de días desde tal notificación sin que el arrendador haya efectuado comunicación alguna.

VII. Que el CESIONARIO está interesado en aceptar dicha cesión para dedicar el Local a un uso distinto de vivienda y, en concreto, para el mismo uso [ACTIVIDAD] que aquel que viene desarrollando el CEDENTE en el mismo.

VII. Que, habiendo llegado las Partes, libre y espontáneamente, a un acuerdo, formalizan el presente CONTRATO DE CESIÓN O TRASPASO DE LOCAL DE NEGOCIO, que se regirá bajo las siguientes:

CLÁUSULAS

Primero.- Objeto.

Que el CEDENTE da en traspaso al CESIONARIO [NOMBRE Y APELLIDOS], quien acepta y recibe, el local de negocio sito en de la finca número de la calle [CALLE] de [LOCALIDAD], descrito anteriormente., junto con los diversos elementos aludidos en la manifestación [Nº] y que figuran relacionados en el Anexo [Nº DE ANEXO], con todo cuanto le es inherente y accesorio.

Se hace constar que el recibo de alquiler que se satisface por el arrendamiento del local mencionado asciende a [IMPORTE] euros, de cuya suma, la cantidad de [IMPORTE] euros [IMPORTE] corresponde a renta más incrementos, la [IMPORTE] de euros [IMPORTE], a repercusiones por [CONCEPTO DE LA REPERCUSIÓN], y la de [IMPORTE] euros [IMPORTE] a IVA.

Segunda.- Subrogación

El CESIONARIO en este mismo acto entra en posesión del local de negocio traspasado y de los diversos elementos transmitidos subrogándose en todos los derechos y obligaciones que le correspondían al CEDENTE.

Tercera.- Puesta a disposición

El Local se pone a disposición del CESIONARIO en un estado adecuado al fin que se destina, mediante la entrega de las llaves. El CESIONARIO declara conocer perfectamente y aceptar la superficie y demás características del Local, incluyendo su mobiliario, existencias, útiles y/o instalaciones, así como su estado de uso y conservación y, en particular, el Certificado de Eficiencia Energética regulado en el Real Decreto 390/2021, de 1 de junio, por el que se aprueba el procedimiento básico para la certificación de la eficiencia energética de los edificios.

Cuarta.- Permisos y Licencias

El CESIONARIO se compromete a obtener y a mantener todas las autorizaciones, permisos y/o licencias que sean necesarios para la apertura del Local y el ejercicio de su actividad, y a pagar todos los impuesto, y/o contribución que emanen del ejercicio de la actividad en el Local.

No será causa de resolución del presente Contrato ni del Contrato de arrendamiento ni afectará en forma alguna a su validez los casos en los que el CESIONARIO pudiera ver denegada, suspendida o revocada alguna de las autorizaciones, permisos y/o licencias que sean necesarios para la apertura del Local y el ejercicio de su actividad en el mismo, salvo que la causa que origine tal denegación, suspensión o revocación sea imputable al CEDENTE o al ARRENDADOR respectivamente.

[ELEGIR UNA OPCIÓN: Si es a título gratuito / Cuando es a título oneroso]

[OPCIONAL — incluir si procede]

(Si se negocia incrementos de renta)

Sexta.- Incremento la renta

Al amparo del artículo 32 de la Ley 29/1994, de 24 de noviembre, de Arrendamientos Urbanos (LAU), el ARRENDADOR exige un incremento del [Nº] por ciento (%) de dicha renta, tal y como se establece en el documento firmado por el ARRENDADOR que se incorpora como Anexo al presente Contrato. Así, la renta que deberá satisfacer el CESIONARIO por el arrendamiento del Local asciende a [IMPORTE] (€), sin incluir el porcentaje que resulte de la aplicación, según la legislación vigente, del Impuesto sobre el Valor Añadido (IVA) que asimismo corresponde abonar al CESIONARIO.

.- Pago de la Renta

El CESIONARIO se compromete a realizar el pago de la renta cada mes, anticipadamente, dentro de los [Nº] primeros días del mes.

El pago de la renta se realizará mediante ingreso o transferencia bancaria al número de cuenta (IBAN): de la entidad bancaria: y cuyo titular es:. El comprobante de ingreso o transferencia servirá como comprobante o justificante del pago. No obstante, el ARRENDADOR emitirá y entregará al CESIONARIO la factura con el desglose de cantidades y conceptos que corresponda.

[OPCIONAL — incluir si procede]

(En caso de impago)

El incumplimiento por el CESIONARIO de la obligación de pago en el plazo fijado será motivo de resolución del Contrato de arrendamiento, debiendo en tal caso restituir inmediatamente el Local al ARRENDADOR, siendo por cuenta de aquella Parte los gastos que la resolución pudiera ocasionar, así como el interés de demora legalmente establecido, salvo acuerdo en contrario.

.- Fianza

El CESIONARIO hace entrega al CEDENTE de [IMPORTE] euros ( €) correspondientes a la cantidad que este último entregó al ARRENDADOR en concepto de fianza o depósito de garantía con el objetivo de garantizar, hasta donde alcanzara, el cumplimiento de sus obligaciones legales y contractuales.

El CEDENTE declara en este acto recibir dicha cantidad en la fecha y lugar mencionados en el encabezamiento, constituyendo el presente documento la más formal y solemne carta de pago que en derecho corresponda.

Esta fianza será devuelta al CESIONARIO una vez se haya comprobado el estado y condiciones en las que se entrega el Local al ARRENDADOR al finalizar el Contrato, así como el cumplimiento del resto de sus obligaciones, particularmente, del abono del importe total de la renta,

[OPCIONAL — incluir si procede]

(En caso de existir fiador solidario)

Con el fin de garantizar el cumplimiento de todas las obligaciones que emanan del Contrato de arrendamiento para el CESIONARIO, se constituye por la presente cláusula la figura del fiador personal y solidario que será asumido por: D./Dña. [NOMBRE Y APELLIDOS], con DNI/NIF núm. [DNI/NIE] y domicilio en [LOCALIDAD].

El FIADOR reconoce saber que su obligación será vinculante durante todo el período que dure el Contrato de arrendamiento. La responsabilidad del FIADOR estará vigente hasta que sean cumplidas todas las obligaciones del Contrato de arrendamiento, incluyendo las rentas, gastos de reparación y todo otro que el CESIONARIO deje pendiente y el ARRENDADOR deba satisfacer.

Asimismo, el FIADOR renuncia a los beneficios de orden y excusión y a lo dispuesto en el artículo 1851 del Código Civil. Por tanto, la acción para cobrar las cantidades garantizadas podrá dirigirse indistintamente contra el FIADOR y el CESIONARIO.

.- Escritura Pública

Cualquiera de las partes podrá elevar a escritura pública este contrato e inscribirlo en el Registro de la Propiedad siendo los gastos, que esta elevación a público e inscripción conlleve, asumidos por la Parte que lo promueva.

.- Notificaciones

Las partes señalan como domicilios para la práctica de las notificaciones necesarias en la ejecución del presente contrato:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

.- Protección de datos personales

Las Partes de este Contrato conocen y se obligan a cumplir la Ley Orgánica 3/2018, de 5 de diciembre, de Protección de Datos Personales y garantía de los derechos digitales y consienten la incorporación de sus datos personales en el fichero automatizado de la contraparte.

.- Gastos e Impuestos

Todos los impuestos, gastos judiciales o extrajudiciales originados a consecuencia de la celebración del presente contrato serán de cuenta del [NOMBRE DE LA PARTE].

.- Naturaleza del contrato y normativa aplicable

El presente contrato tiene naturaleza mercantil, rigiéndose por lo dispuesto en sus propias cláusulas y en lo en ellas no previsto por Ley 29/1994, de 24 de noviembre, de Arrendamientos Urbanos (LAU), las disposiciones Código de Comercio, leyes especiales y usos mercantiles que le sean aplicables, o en lo no previsto, por las disposiciones del Código Civil.

.- Fuero competente

[ELEGIR UNA OPCIÓN: Sometimiento a fuero judicial / Sometimiento a arbitraje]

Y en prueba de conformidad con todo ello firman el presente documento por duplicado ejemplar y a un solo efecto en el lugar y fecha expresados en el encabezamiento.

________________________________

EL CEDENTE

________________________________

EL CESIONARIO

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]
