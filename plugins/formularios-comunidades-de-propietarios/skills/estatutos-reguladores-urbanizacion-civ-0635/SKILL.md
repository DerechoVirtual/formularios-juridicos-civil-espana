---
name: estatutos-reguladores-urbanizacion-civ-0635
description: "Estatutos reguladores de una urbanización. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Estatutos reguladores de una urbanización

> Formulario **CIV-0635** del plugin **Comunidades de propietarios** (`formularios-comunidades-de-propietarios`) · Civil › Propiedad horizontal · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Estatutos reguladores de una urbanización» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Estatutos reguladores de una urbanización” para mi caso». También puedes invocarla directamente con `/formularios-comunidades-de-propietarios:estatutos-reguladores-urbanizacion-civ-0635`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-comunidades-de-propietarios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Comunidades de propietarios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº DE BLOQUE (6 veces)
- [ ] Nº (4 veces)
- [ ] DIRECCIÓN (3 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] AÑO (2 veces)
- [ ] DÍA (2 veces)
- [ ] MES (2 veces)
- [ ] NOMBRE DE LA URBANIZACIÓN (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] ACTO O RESOLUCIÓN
- [ ] CARGO
- [ ] LIBRO
- [ ] LUGAR
- [ ] NOMBRE DE LA CALLE
- [ ] NOMBRE Y APELLIDOS DEL NOTARIO
- [ ] Nº DE BLOQUES
- [ ] Nº DE PARCELAS
- [ ] Nº DE VOCALES
- [ ] TOMO

## Normas que cita el formulario

- art. 396 Código Civil
- art. 392 Código Civil
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

ESTATUTOS DE LA URBANIZACIÓN [NOMBRE DE LA URBANIZACIÓN] SITA EN EL NÚMERO [Nº] DE LA CALLE [NOMBRE DE LA CALLE] DE [LOCALIDAD]

La Urbanización [NOMBRE DE LA URBANIZACIÓN] se regirá por los estatutos que a continuación se redactan y en especial por lo establecido en la escritura de División Horizontal de fecha [DÍA] de [MES] de [AÑO] ante el Notario [NOMBRE Y APELLIDOS DEL NOTARIO], que está debidamente inscrita en el Registro de la Propiedad de [LOCALIDAD], al tomo [TOMO], libro [LIBRO] de [LOCALIDAD], finca número [NÚMERO], inscripción número [NÚMERO] estando el edificio destinado a (viviendas/locales/comerciales/_industriales/aparcamiento)

Capítulo I. DISPOSICIONES GENERALES

Artículo 1: Ámbito de aplicación

Los presentes Estatutos regulan los servicios y elementos comunes del resto de la finca matriz, una vez segregadas las [Nº DE PARCELAS] parcelas destinadas a bloques, constituyendo una copropiedad ordinaria, al amparo de los artículos 396 y concordantes del Código Civil, que serán aplicables siempre con carácter supletorio a las normas de la Ley de Propiedad Horizontal, conforme a lo dispuesto en su artículo 24.

Artículo 2: Carácter obligatorio

Los presentes estatutos, así como el Reglamento de Régimen Interior son obligatorios para todos los copropietarios, actuales y futuros, y se acomodan a las normas contenidas en la Ley de Propiedad Horizontal y en los artículo 392 y siguientes del Código Civil, aplicables en lo no previsto en los mismos.

Capítulo II. DE LOS ELEMENTOS PRIVATIVOS Y COMUNES

Artículo 3: Cuotas de participación

Para el adecuado sostenimiento de los servicios, cargas y responsabilidades que no corresponden individualmente a los bloques se atribuyen las siguientes cuotas de participación:

-Bloque [Nº DE BLOQUE], %

-Bloque [Nº DE BLOQUE], %

-Bloque [Nº DE BLOQUE], %

-Bloque [Nº DE BLOQUE], %

Esta cuota de participación servirá de módulo para la participación en cargas y beneficios, así como a efectos de cómputo de votaciones.

Artículo 4: Elementos comunes

Son elementos comunes, los siguientes:

A) La vivienda del encargado de la urbanización, situada en [DIRECCIÓN]

B) La caseta de guarda, situada a la entrada de la urbanización.

C) La piscina y todas sus instalaciones complementarias, situada en [DIRECCIÓN]

D) Las pistas de tenis, situadas entre los bloques [Nº DE BLOQUE] y [Nº DE BLOQUE] de la urbanización.

E) La zona infantil de juegos, situada en [DIRECCIÓN]

F) Los jardines y viales, que ocupan una extensión aproximada de [Nº] metros cuadrados.

G) El alumbrado público de la urbanización.

H) El resto de servicios e instalaciones que pueda tener la urbanización, hasta alcanzar el resto de la finca matriz de un total de [Nº] metros cuadrados, que no corresponden de forma individual a ningún bloque, y los que puedan existir en el futuro por acuerdo de la Junta Rectora.

Capítulo III. DE LOS GASTOS Y CARGAS

Artículo 5: Gastos generales

Los gastos ocasionados por el mantenimiento y administración de los elementos y servicios comunes serán satisfechos conforme a la cuota de participación de cada bloque señalada en el artículo tercero y se abonarán dentro de los [Nº] días a partir de su emisión.

Será condición previa, tanto para los presupuestos ordinarios como extraordinarios, la aprobación por la Junta Rectora.

Capítulo IV. DE LOS ÓRGANOS DE GOBIERNO

Artículo 6: Junta Rectora

Composición

La copropiedad será dirigida por una Junta Rectora que estará compuesta por los presidentes de las comunidades de cada uno de los [Nº DE BLOQUES] bloques que integran esta Urbanización.

De entre ellos se elegirá un Presidente, un Vicepresidente y [Nº DE VOCALES] Vocales, que compondrán, junto con el Secretario y el Administrador, la Comisión Directiva.

Facultades

La competencia de los órganos de gobierno de la comunidad agrupada únicamente se extiende a los elementos inmobiliarios, viales, instalaciones y servicios comunes. Sus acuerdos no podrán menoscabar en ningún caso las facultades que corresponden a los órganos de gobierno de las comunidades de propietarios integradas en la agrupación de comunidades.

Funcionamiento

La Junta Rectora se reunirá cuando así lo considere el Presidente o, en caso de ausencia o enfermedad, el Vicepresidente. También podrá ser convocada directamente por los Presidentes de los bloques que representen al menos el 25% de cuotas de participación o la cuarta parte de las fincas de la Urbanización. Debe celebrarse como mínimo una Junta anual para la aprobación de cuentas y presupuestos y para la renovación de la Comisión Directiva. Esta Junta tendrá lugar dentro de los tres primeros meses de cada año, debiendo presentarse las cuentas cerradas al 31 de diciembre del año anterior. También podrán celebrarse todas las Juntas extraordinarias que sean necesarias, previa convocatoria por alguna de las personas antes señaladas.

La convocatoria de las Juntas será siempre por escrito, con indicación de los asuntos a tratar, el lugar, día y hora de la reunión, y con un mínimo de siete días de antelación para las juntas ordinarias y dos días para las extraordinarias. En la misma citación se consignará la primera y segunda convocatoria, con una diferencia mínima de treinta minutos.

La Junta podrá celebrarse en primera convocatoria cuando estén presentes, al menos, la mitad de los Presidentes que a su vez sumen más del 50% de las cuotas de participación; en segunda convocatoria bastará la asistencia global del 25% de Presidentes y de cuotas.

Adopción de acuerdos

Los acuerdos de la Junta de propietarios se sujetarán a las siguientes normas: computándose como favorables los votos de los notificados de la convocatoria que no se opusieran en el plazo de treinta días desde la notificación del acuerdo:

1. La unanimidad para la validez de los acuerdos que implique la aprobación o modificación de reglas contenidas en el título constitutivo de la propiedad o de los Estatutos.

2. Tres quintas partes de los integrantes que representen tres quintas partes de las cuotas para el establecimiento o supresión de portería, conserjería, vigilancia y servicios comunes.

3. Una tercera parte de los integrantes que sumen un tercio de las cuotas para la instalación o adaptación de sistemas de telecomunicación o nuevas energías. Los integrantes que no voten a favor no estarán obligado a abonar importe alguno, salvo que solicitase acceso al nuevo servicio, debiendo abonar el importe que le hubiera correspondido más los intereses legales.

4. Mayoría de cuotas y de número de integrantes para la supresión de barreras arquitectónicas.

5. Para la validez del resto de los acuerdos no expresados en los párrafos anteriores, bastará en primera convocatoria el voto de la mayoría del total de los integrantes que a su vez represente la mayoría de las cuotas de participación.

En segunda convocatoria serán válidos los acuerdos adoptados por la mayoría de los asistentes, siempre que ésta represente a su vez más de la mitad del valor de las cuotas de los asistentes. Cuando la mayoría no pudiera lograrse por los procedimientos establecidos en los párrafos anteriores, podrá instarse dentro de los treinta días desde la segunda asamblea la intervención judicial en la forma que determina la Ley.

Los acuerdos de la Junta se reflejarán en el libro de actas, foliado y sellado por el Registro de la Propiedad en que está inscrito el total edificio. De cada sesión se extenderá un acta que será firmada por el Presidente y Secretario, y quien desee efectuarlo por convenir a sus intereses. El acta se notificará por correo certificado a quien lo solicite o en cualquier forma de la que quede constancia. Cualquiera de los propietarios podrá obtener certificación del acuerdo.

Artículo 7: El Presidente

El presidente será nombrado, entre los integrantes, mediante elección. El nombramiento se hará por mayoría simple siendo obligatoria su aceptación, sin perjuicio de la acción judicial que contempla el artículo 13.2 de la LPH.

Estarán exentos los mayores de 65 años, los enfermos crónicos y los residentes fuera de la localidad. El sistema podrá modificarse por acuerdo mayoritario de la Junta.

El Presidente podrá ostentar los cargos de Secretario y Administrador. Presidirá las reuniones y será el encargado de ejecutar o hacer cumplir sus acuerdos.

Artículo 8: El Vicepresidente

El Vicepresidente se nombrará por el mismo procedimiento que el establecido para la designación del Presidente.

Corresponde al Vicepresidente sustituir al presidente en los casos de ausencia, vacante o imposibilidad de éste, así como asistirlo en el ejercicio de sus funciones en los términos que establezca la Junta de propietarios.

Artículo 9: El Secretario

Al Secretario corresponde llevar o controlar la correspondencia, guardar durante cinco años los documentos, los libros sociales y de contabilidad y expedir certificaciones con el visto bueno del Presidente, así como guardar el Libro de Actas.

Artículo 10: El Administrador

El cargo de Administrador podrá ser asignado a persona ajena a la copropiedad conforme a lo dispuesto en el Artículo 13 de la Ley de Propiedad Horizontal.

Corresponden al Administrador:

1. Velar por el buen régimen de la casa, sus instalaciones y servicios, y hacer a estos efectos las oportunas advertencias y percibimientos a los titulares.

2. Preparar con la debida antelación y someter a la Junta, el plan de gastos previsibles y presupuestos proponiendo los medios necesarios para hacer frente a los mismos.

3. Atender a la conservación de la urbanización, advirtiendo si tiene conocimiento de las reparaciones ordinarias que haya que realizar y pudiendo en las extraordinarias adoptar medidas urgentes, dando inmediata cuenta a la Junta o en su caso a los propietarios.

4. Ejecutar los acuerdos adoptados en materia de obras y efectuar cobros y pagos que sean procedentes.

5. Todas las demás atribuciones que se confieran por la Junta

Capítulo V. DEL FONDO DE RESERVA

Artículo 11: El Fondo de Reserva

El fondo de reserva para atender a las obras de reparación y conservación de la urbanización estará constituido por una cantidad mínima equivalente al 2,5% del presupuesto del primer ejercicio y alcanzará en los siguientes ejercicios el %, debiendo mantenerse este fondo en esta cuantía como obligatorio en todos los ejercicios, por lo que los gastos efectuados del mismo serán repuestos mediante nuevas derramas.

RÉGIMEN ECONÓMICO DE LA COMUNIDAD

Artículo 12: Cuentas de la Comunidad

Se llevará un libro de ingresos y gastos y se conservarán debidamente ordenados los justificantes de pago e ingresos.

Artículo 13: Cuenta corriente

La urbanización abrirá una cuenta corriente en Banco o Caja de la localidad a nombre de la Junta de propietarios. Para retirar cantidades de esta cuenta será necesario que los talones vayan firmados conjuntamente por el Presidente y [CARGO].

Artículo 14: Seguro de responsabilidad civil

La urbanización estará asegurada contra [ACTO O RESOLUCIÓN], sin perjuicio de los seguros que cada propietario constituya sobre su piso.

La elección de la Compañía aseguradora y la determinación del capital necesario para cubrir el importe de su reconstrucción corresponderá a la Junta.

RÉGIMEN SUPLETORIO

Artículo 15: Régimen supletorio

En lo no previsto en este Estatuto se estará a lo dispuesto, de forma subsidiaria, en las normas de la Ley de Propiedad Horizontal y Código Civil.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

========================================================================
