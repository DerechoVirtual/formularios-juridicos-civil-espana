---
name: estatutos-comunidad-propietarios-civ-0633
description: "Estatutos de una comunidad de propietarios. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Estatutos de una comunidad de propietarios

> Formulario **CIV-0633** del plugin **Comunidades de propietarios** (`formularios-comunidades-de-propietarios`) · Civil › Propiedad horizontal · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Estatutos de una comunidad de propietarios» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Estatutos de una comunidad de propietarios” para mi caso». También puedes invocarla directamente con `/formularios-comunidades-de-propietarios:estatutos-comunidad-propietarios-civ-0633`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-comunidades-de-propietarios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Comunidades de propietarios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (4 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] MES (3 veces)
- [ ] AÑO (2 veces)
- [ ] DÍA (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] ACTO O RESOLUCIÓN
- [ ] CALLE
- [ ] CARGO
- [ ] LIBRO
- [ ] LUGAR
- [ ] NOMBRE DE LA CALLE
- [ ] NOMBRE DE LA COMUNIDAD
- [ ] NOMBRE DEL EDIFICIO
- [ ] NOMBRE Y APELLIDOS DEL NOTARIO
- [ ] Nº DE DÍAS
- [ ] Nº DE ELEMENTOS
- [ ] PERIODICIDAD
- [ ] TOMO

## Normas que cita el formulario

- art. 392 Código Civil
- art. 396 Código Civil
- art. 13.2 LPH

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

ESTATUTOS DE LA COMUNIDAD DE PROPIETARIOS DEL EDIFICIO [NOMBRE DEL EDIFICIO] SITO EN EL NÚMERO [Nº] DE LA CALLE [NOMBRE DE LA CALLE] DE [LOCALIDAD]

La copropiedad del inmueble de la calle [CALLE] se regirá por los estatutos que a continuación se redactan y en especial por lo establecido en la escritura de División Horizontal de fecha [DÍA] de [MES] de [AÑO] ante el Notario [NOMBRE Y APELLIDOS DEL NOTARIO], que está debidamente inscrita en el Registro de la Propiedad de [LOCALIDAD], al tomo [TOMO], libro [LIBRO] de [LOCALIDAD], finca número [NÚMERO], inscripción número [NÚMERO] estando el edificio destinado a

Capítulo I. DISPOSICIONES GENERALES

Artículo 1: Ámbito de aplicación

Los presentes estatutos regulan el régimen de propiedad horizontal de cada uno de los pisos/departamentos/locales comerciales [Nº DE ELEMENTOS] que componen la Comunidad de Propietarios de [NOMBRE DE LA COMUNIDAD].

Artículo 2: Carácter obligatorio

Los presentes estatutos, así como el Reglamento de Régimen Interior son obligatorios para todos los copropietarios, actuales y futuros, y se acomodan a las normas contenidas en la Ley de Propiedad Horizontal y en los artículo 392 y siguientes del Código Civil, aplicables en lo no previsto en los mismos.

Capítulo II. DE LOS ELEMENTOS PRIVATIVOS Y COMUNES

Artículo 3: Elementos privativos

Es propiedad privativa del dueño o dueños de cada piso/departamento/locales comercia, todo cuanto se encuentre comprendido en el recinto o espacio que el mismo comprende. Quedan exceptuados las paredes maestras, las medianeras y los tubos o canalizaciones de agua y electricidad, aunque éstos pasen por el interior de las partes privativas.

Artículo 4: Elementos comunes

Son elementos comunes, además de los enumerados en el artículo 396 del Código Civil, los siguientes:

A modo enunciativo serán considerados también como elementos comunes los siguientes:

1. Los cimientos, paredes de carga y medianera, fachadas anterior y posterior, paredes de patios interiores y los tabiques que tengan por finalidad separar entidades.

2. Los pasos, corredores, patios y patinejos generales, la escalera y el vestíbulo de acceso a la misma, el portal y sus elementos decorativos e indicativos.

3. La cubierta, terrado o terrazas del inmueble, aun en el caso de que sean de utilización exclusiva de uno o varios propietarios.

4. Los pilares y vigas de sustentación de cada planta, el forjado de los pisos y la obra gruesa de los suelos.

5. Las piezas de decoración de las fachadas, portales y demás elementos comunes, incluida la pintura de la parte externa de las puertas de entrada a cada entidad y la exterior de todas las puertas, rejas, balconeras y ventanas.

6. La portería o local donde estará el portero o portera o el conserje y su cuarto de aseo correspondiente.

7. Los ascensores y montacargas así como sus instalaciones.

9. Las acometidas e instalaciones generales de suministros, en cuanto a electricidad hasta la caja de distribución y el pozo para la toma de tierra del conductor neutro; con respecto al agua, hasta la salida desde la batería de contadores divisionarios; los intercomunicadores o teléfonos interiores del inmueble, a excepción del aparato y la parte de instalación ubicada en el interior de cada entidad.

Artículo 5. Alcance del derecho de propiedad

Cada propietario tendrá la plena propiedad del piso/departamento/local comercial que haya adquirido, con las limitaciones que se establecen en la Ley, en la escritura de División Horizontal o en estos Estatutos.

Al propietario de cada entidad corresponde la propiedad exclusiva de cuantos elementos se hallen en el interior del departamento, y entre ellos: las puertas, ventanas, tabiques, enlucidos, pavimentos, pintura, canalizaciones hasta las conducciones generales ascendientes o descendentes, aseos e instalaciones sanitarias.

Artículo 6: Limitaciones de los propietarios

Obras

Sin perjuicio de las limitaciones que impone la Ley no podrá el propietario:

1) Alterar la configuración de puertas y ventanas, ni pintarlas de color distinto al existente o al que la comunidad acuerde.

2) Modificar en lo más mínimo la decoración y ornamentación de las fachadas interiores o exteriores.

3) Cubrir patios comunes y terrazas ni total ni parcialmente, sean o no privativas.

4) Instalar toldos o cortinas exteriores, sin el previo acuerdo de la Junta en cuanto a su forma y color.

5) Alterar la actual distribución de huecos exteriores a las fachadas o escaleras comunes o abrir otros nuevos, salvo lo reconocido a los personas con discapacidad y mayores de 70 años por Ley de 30 de mayo de 1995.

6) Instalar anuncios en las fachadas, o colocar objetos en las mismas. Quedan exceptuados de la prohibición de instalación de anuncios luminosos el dueño o dueños de los locales comerciales en planta baja, si bien se colocarán dentro del ámbito de la fachada que corresponde a cada local. Igualmente, queda prohibido, salvo en el lugar del portal del edificio destinado al efecto, la colocación de placas profesionales o comerciales. A tal efecto, deberá darse cuenta previamente al Presidente de la Comunidad, para que las mismas se ajusten a un mismo formato y modelo y, en consecuencia, conseguir de ese modo la estética propia y adecuada al portal del edificio.

7) Variar la estructura de su entidad en cuanto a la consolidación y seguridad de las partes comunes.

8) Dejar en el portal del inmueble, en los rellanos de la escalera o en cualquier parte común, cajones, fardos o mercancías durante más tiempo del que es necesario para la carga y descarga.

No obstante, la Junta por mayoría podrá levantar alguna de las prohibiciones indicadas, en los casos en que no haya perjuicio para el interés común.

Actividades

Cada propietario podrá ejercer la actividad que tenga por conveniente dentro de su piso/departamento/locales comercial, salvo las que produzcan cualquier tipo de ruido, olor, contaminación y en general las del artículo 7.2 de la Ley de Propiedad Horizontal, con las consecuencias previstas en dicho artículo.

Arrendamiento o cesión del uso de la vivienda

El propietario del piso o local deberá poner en conocimiento del Presidente y/o Administrador de la Comunidad el derecho de uso y habitación, usufructo, arrendamiento o cesión gratuita u onerosa efectuada a terceros, respondiendo el propietario solidariamente de los daños cometidos por el ocupante y personas que con él convivan.

En estos supuestos deberá hacerse constar al ocupante el contenido de estos Estatutos y del Reglamento de Régimen Interior, a fin de que tenga conocimiento de sus derechos y obligaciones, sin perjuicio de la responsabilidad del propietario a que se refiere el párrafo anterior.

Capítulo III. DE LAS MEJORAS Y VARIACIÓN DE CUOTAS

Artículo 7: Régimen de mayorías

Mejoras necesarias

Las mejoras o innovaciones necesarias requeridas para la adecuada conservación o habitabilidad del inmueble podrán ser exigidas por uno cualquiera de los propietarios, debiendo ser realizadas.

Mejoras no necesarias

Las innovaciones o mejoras no requeridas para la adecuada conservación y habitabilidad del inmueble, serán acordadas por mayoría del número de propietarios y estarán obligados a su pago todos ellos en proporción a su cuota respectiva.

Si su importe excediera de la cuota equivalente a tres mensualidades ordinarias de gastos comunes, los propietarios disidentes no estarán obligados a su pago, salvo que el disidente participe en el futuro en las ventajas de la innovación en cuyo caso deberá pagar la cuota actualizada.

Cualquier innovación o mejora que haga inservible una parte del edificio que fuere de uso o disfrute de uno solo o de alguno de los propietarios, precisará el consentimiento expreso previo de éste o éstos.

Artículo 8: Cuotas de participación

Para el adecuado sostenimiento del inmueble, sus servicios interiores y exteriores, cargas y responsabilidades que no sean susceptibles de individualización se atribuye a cada piso o local la siguiente cuota de participación, en relación al total de la finca:

Esta cuota de participación servirá de módulo para la participación en cargas y beneficios, por razón de la Comunidad, salvo lo establecido en el artículo siguiente.

Capítulo IV. DE LOS GASTOS Y CARGAS

Artículo 9: Gastos generales

Los gastos que se indican a continuación, con excepción de lo establecido en el artículo anterior, serán satisfechos de la siguiente forma:

1. Los gastos de material y administración, por partes iguales entre los copropietarios de pisos y locales.

2. Los gastos de limpieza de portal y escaleras y, en general, los que afecten a estos elementos comunes, serán satisfechos por partes iguales entre todos los copropietarios, con exclusión de los propietarios de locales que no dispongan de acceso por dichos elementos comunes.

3. Los gastos de calefacción conforme al coeficiente de propiedad, con exclusión de los locales que no dispongan de dicho servicio.

4. Los gastos correspondientes al consumo de electricidad de la escalera, conservación de sus instalaciones y reposición de bombillas serán sufragadas según la respectiva cuota (pero se excluyen del pago por no tener derecho al vestíbulo y escalera a los departamentos).

5. Los gastos de instalación, conservación y reparación de la antena o cualquier otra infraestructura común serán satisfechos por iguales partes entre todos los copropietarios del inmueble o de los que instaron su colocación. Quedan excluidos aquellos locales que no puedan técnicamente contar con tales servicios.

6. Cualquier tributo, de ámbito estatal, autonómico o local, que gravite directa y conjuntamente para toda la finca y no con carácter individual, será satisfecho según las bases liquidables que figuren en la declaración fiscal del edificio.

Artículo 10: Servicio de conserjería o portería

Los gastos inherentes al servicio de conserjería serán sufragados por los propietarios según su cuota de participación, salvo los propietarios de los pisos/departamentos/locales números [Nº], por lo que los mismos no hacen ni podrán hacer uso de este servicio.

Artículo 11: Servicio de ascensor

Los gastos correspondientes al servicio de ascensor, tales como gastos de conservación, reparaciones, consumo de fuerza o inspecciones de los organismos oficiales, se repartirán según su cuota entre los propietarios de todas los pisos/departamentos/locales comerciales menos los números [Nº], por lo que los mismos no hacen ni podrán hacer uso de este servicio.

Artículo 12: Servicio de montacargas

Los gastos correspondientes al servicio de montacargas, tales como gastos de conservación, reparaciones, consumo de fuerza o inspecciones de los organismos oficiales, se repartirán según su cuota entre los propietarios de todas los pisos/departamentos/locales comerciales menos los números [Nº], por lo que los mismos no hacen ni podrán hacer uso de este servicio.

Capítulo V. DE LOS ÓRGANOS DE REPRESENTACIÓN

Artículo 13: Junta de Propietarios

Facultades

Corresponden a la Junta de Propietarios las facultades que se transcriben:

a) Nombrar y remover a las personas que ejerzan los cargos mencionados en el artículo anterior y resolver las reclamaciones que los titulares de los pisos o locales formulen contra la actuación de aquéllos.

b) Aprobar el plan de gastos e ingresos previsibles y las cuentas correspondientes.

c) Aprobar los presupuestos y la ejecución de todas las obras de reparación de la finca, sean ordinarias o extraordinarias, y ser informada de las medidas urgentes adoptadas por el administrador, de conformidad con lo dispuesto en el artículo 20 de la Ley de Propiedad Horizontal.

d) Aprobar o reformar los estatutos y determinar las normas de régimen interior.

e) Conocer y decidir en los demás asuntos de interés general para la comunidad, acordando las medidas necesarias o convenientes para el mejor servicio común.

Constitución de la Junta

La Junta de Propietarios se reunirá por lo menos una vez al año cada mes de [MES], para aprobar los presupuestos y cuentas, designar los cargos de los órganos de gobierno y en las demás ocasiones que lo juzgue oportuno el Presidente o lo pida la cuarta parte de los propietarios o un número de éstos que represente al menos el veinticinco por ciento de las cuotas de participación.

La convocatoria la hará el Presidente y, en su defecto, los promotores de la reunión, con indicación detallada de los asuntos a tratar, hora, día y lugar de la Junta. Deberá entregarse la citación por escrito en el domicilio que hubiere designado cada propietario, y, en su defecto, en el piso perteneciente al mismo, acompañando los justificantes mediante copia de los motivos por los que se someten a la aprobación los asuntos del Orden del día. Se hará constar la relación de propietarios que no estén al corriente en el pago de las deudas con advertencia de la privación del derecho de voto según el artículo 15.2 de la Ley de Propiedad Horizontal.

La citación para la Junta ordinaria anual se hará cuando menos con seis días de anticipación, y para las extraordinarias con la que sea posible para que pueda llegar a conocimiento de los interesados.

Adopción de acuerdos

Cada propietario al corriente en el pago de las cuotas tendrá derecho al voto, que lo hará efectivo por sí o por su representante legal. La representación deberá acreditarse por poder o carta dirigida al Presidente, sin perjuicio de los supuestos en que la Ley establezca la necesidad de voto cualificado por coeficiente, según el artículo 17 de la Ley de Propiedad Horizontal.

Los acuerdos de la Junta de propietarios se sujetarán a las siguientes normas, computándose como favorables los votos de los notificados de la convocatoria que no se opusieran en el plazo de treinta días desde la notificación del acuerdo:

1. La unanimidad para la validez de los acuerdos que implique la aprobación o modificación de reglas contenidas en el título constitutivo de la propiedad o de los Estatutos.

2. Tres quintas partes de los propietarios que representen tres quintas partes de las cuotas para el establecimiento o supresión de portería, conserjería, vigilancia y servicios comunes. (El mismo quórum citado anteriormente para el arrendamiento de elementos comunes, más el consentimiento del propietario afectado si lo hubiese.)

3. Una tercera parte de los propietarios que sumen un tercio de las cuotas para la instalación o adaptación de sistemas de telecomunicación o nuevas energías. El propietario que no vote a favor no estará obligado a abonar importe alguno, salvo que solicitase acceso al nuevo servicio, debiendo abonar el importe que le hubiera correspondido más los intereses legales.

4. Mayoría de cuotas y de número de propietarios para la supresión de barreras arquitectónicas.

5. Para la validez del resto de los acuerdos no expresados en los párrafos anteriores, bastará en primera convocatoria el voto de la mayoría del total de los propietarios que a su vez represente la mayoría de las cuotas de participación.

En segunda convocatoria serán válidos los acuerdos adoptados por la mayoría de los asistentes, siempre que ésta represente a su vez más de la mitad del valor de las cuotas de los asistentes. Cuando la mayoría no pudiera lograrse por los procedimientos establecidos en los párrafos anteriores, podrá instarse dentro de los treinta días desde la segunda asamblea la intervención judicial en la forma que determina la Ley.

Los acuerdos de la Junta de Propietarios se reflejarán en el libro de actas, foliado y sellado por el Registro de la Propiedad en que está inscrito el total edificio. De cada sesión se extenderá un acta que será firmada por el Presidente y Secretario, y quien desee efectuarlo por convenir a sus intereses. El acta se notificará por correo certificado a quien lo solicite o en cualquier forma de la que quede constancia. Cualquiera de los propietarios podrá obtener certificación del acuerdo.

Artículo 14: El Presidente

El presidente será nombrado, entre los propietarios, mediante elección. El nombramiento se hará por mayoría simple siendo obligatoria su aceptación, sin perjuicio de la acción judicial que contempla el artículo 13.2 de la LPH.

Estarán exentos los mayores de 65 años, los enfermos crónicos y los residentes fuera de la localidad. El sistema podrá modificarse por acuerdo mayoritario de la Junta.

El Presidente podrá ostentar los cargos de Secretario y Administrador. Presidirá las reuniones y será el encargado de ejecutar o hacer cumplir sus acuerdos.

Artículo 15: El Vicepresidente

El Vicepresidente se nombrará por el mismo procedimiento que el establecido para la designación del Presidente.

Corresponde al Vicepresidente sustituir al presidente en los casos de ausencia, vacante o imposibilidad de éste, así como asistirlo en el ejercicio de sus funciones en los términos que establezca la Junta de propietarios.

Artículo 16: El Secretario

Al Secretario corresponde llevar o controlar la correspondencia, guardar durante cinco años los documentos, los libros sociales y de contabilidad y expedir certificaciones con el visto bueno del Presidente, así como guardar el Libro de Actas.

Artículo 17: El Administrador

Corresponden al Administrador:

1. Velar por el buen régimen de la casa, sus instalaciones y servicios, y hacer a estos efectos las oportunas advertencias y percibimientos a los titulares.

2. Preparar con la debida antelación y someter a la Junta, el plan de gastos previsibles y presupuestos proponiendo los medios necesarios para hacer frente a los mismos.

3. Atender a la conservación del edificio, advirtiendo si tiene conocimiento de las reparaciones ordinarias que haya que realizar y pudiendo en las extraordinarias adoptar medidas urgentes, dando inmediata cuenta a la Junta o en su caso a los propietarios.

4. Ejecutar los acuerdos adoptados en materia de obras y efectuar cobros y pagos que sean procedentes.

5. Todas las demás atribuciones que se confieran por la Junta

Capítulo VI. DEL FONDO DE RESERVA

Artículo 18: El Fondo de Reserva

El fondo de reserva para atender a las obras de reparación y conservación de la finca estará constituido por una cantidad mínima equivalente al 2,5% del presupuesto del primer ejercicio y alcanzará en los siguientes ejercicios el %, debiendo mantenerse este fondo en esta cuantía como obligatorio en todos los ejercicios, por lo que los gastos efectuados del mismo serán repuestos mediante nuevas derramas.

Capítulo VII. DE LAS OBLIGACIONES ECONÓMICAS DE LOS PROPIETARIOS

Artículo 19: Pago de las cuotas

Cada propietario está obligado a pagar el importe de la parte que le corresponda en los gastos e impuestos comunes, una vez fijada por la junta en proporción a la cuota de participación fijada en su título.

Al pago de estos gastos producidos en el último año y la parte vencida de la anualidad corriente, estará afecto el piso cualquiera que sea su propietario, siendo este débito a favor de la comunidad preferente a cualquier otro.

Las cantidades anuales que los propietarios deben abonar o satisfacer según el presupuesto ordinario, deberán abonarlos al administrador por [PERIODICIDAD] naturales dentro de los [Nº DE DÍAS] primeros días de cada (año, trimestre, mes).

El Administrador expedirá los recibos correspondientes contra la entrega de cualquier cantidad, siendo obligación de los propietarios exigir el recibo y que se especifique el destino de dicho pago.

Artículo 20: Impago de cuotas

En caso de impago de las cantidades que proceda abonar el Presidente o administrador si lo hubiera estarán autorizados para reclamar el pago por la vía judicial expidiéndose para ello certificación del acuerdo de la junta que con anterioridad haya sido notificado al propietario moroso de forma que quede constancia.

La cuota no satisfecha dentro de dicho plazo devengará, sin requerimiento alguno, por cada día de retraso en el pago del interés legal del dinero dividido por 365 días al año, a favor de la comunidad, sin perjuicio de los recargos a que su morosidad diere lugar en favor del Estado, Provincia o Municipio.

Capítulo VIII. DEL RÉGIMEN ECONÓMICO DE LA COMUNIDAD

Artículo 21: Cuentas de la Comunidad

Se llevará un libro de ingresos y gastos y se conservarán debidamente ordenados los justificantes de pago e ingresos.

Artículo 22: Cuenta corriente

La comunidad abrirá una cuenta corriente en Banco o Caja de la localidad a nombre de la Junta de propietarios. Para retirar cantidades de esta cuenta será necesario que los talones vayan firmados conjuntamente por el Presidente y [CARGO].

Artículo 23: Seguro de responsabilidad civil

El edificio estará asegurado contra [ACTO O RESOLUCIÓN], sin perjuicio de los seguros que cada propietario constituya sobre su piso.

La elección de la Compañía aseguradora y la determinación del capital necesario para cubrir el importe de su reconstrucción corresponderá a la Junta.

Capítulo IX. DE LAS AGRUPACIONES Y SEGREGACIONES

Artículo 24: Facultad de los propietarios

Los propietarios se reservan la facultad de agrupar las entidades, o segregarlas, creando nuevas de inferior o superior superficie, asignándoles los nuevos coeficientes que serán siempre la suma de los anteriores agrupados o segregados; incluso podrán agruparse y comunicarse de plantas contiguas.

En cualquier caso, las obras de comunicación deberán venir firmadas por un arquitecto que se hará responsable ante la comunidad de las consecuencias que la ejecución traiga consigo para las partes comunes del edificio.

Artículo 25: Prohibición de segregación

Los propietarios no podrán segregar o agrupar las fincas.

Capítulo X. DE LA EXTINCIÓN

Artículo 26: Causas de extinción

Serán causas de extinción de esta comunidad:

1) La agrupación de todas las entidades en una sola.

2) La destrucción o siniestro del edificio, pero observándose las siguientes normas:

a) Si la destrucción es parcial se destinarán las indemnizaciones del seguro, si éstas son suficientes, a la reconstrucción del edificio.

b) Si la destrucción es total o el importe del seguro sólo cubriese una cantidad inferior al 50 por 100 de la finca, se estará:

- A lo que por unanimidad acuerde la Junta extraordinaria convocada al efecto.

- A falta de acuerdo unánime se procederá a la venta de la finca mediante subasta notarial y su importe se adjudicará entre los propietarios en proporción a su cuota.

Capítulo XI. RÉGIMEN SUPLETORIO

Artículo 27: Régimen supletorio

En lo no previsto en este Estatuto se estará a lo dispuesto, de forma subsidiaria, en las normas de la Ley de Propiedad Horizontal y Código Civil.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

========================================================================
