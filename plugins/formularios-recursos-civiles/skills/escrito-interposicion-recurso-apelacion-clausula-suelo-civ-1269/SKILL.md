---
name: escrito-interposicion-recurso-apelacion-clausula-suelo-civ-1269
description: "Escrito de interposición de recurso de apelación por cláusula suelo. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito de interposición de recurso de apelación por cláusula suelo

> Formulario **CIV-1269** del plugin **Recursos civiles: reposición, apelación, casación y queja** (`formularios-recursos-civiles`) · Civil › Recursos · normativa revisada el 24-11-2026.

## Qué es

Escrito interponiendo recurso de apelación contra sentencia desestimatoria de la nulidad de la cláusula suelo.

Es un modelo de tipo **recursos**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito de interposición de recurso de apelación por cláusula suelo» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito de interposición de recurso de apelación por cláusula suelo” para mi caso». También puedes invocarla directamente con `/formularios-recursos-civiles:escrito-interposicion-recurso-apelacion-clausula-suelo-civ-1269`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-recursos-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Recursos civiles: reposición, apelación, casación y queja) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (6 veces)
- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] MEDIO DE PRUEBA (4 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] LUGAR (2 veces)
- [ ] MINUTO DE LA GRABACIÓN (2 veces)
- [ ] DENOMINACIÓN SOCIAL
- [ ] EJERCICIO
- [ ] Nº DE FOLIOS
- [ ] Nº DE PROCEDIMIENTO
- [ ] NÚMERO

## Normas que cita el formulario

- art. 458.1 LEC
- art. 448.1 LEC
- art. 3 TRLGDCU
- art. 276 LEC
- art. 460 LEC
- art. 464 LEC

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

Notas al pie del formulario original:
(1) Téngase en cuenta que, excluida la condición de consumidor solo podrá abordarse el examen del control de incorporación de la cláusula desde la perspectiva de las condiciones generales de la contratación.

En este sentido, la STS de 3 de junio de 2016 excluye la aplicación del control de transparencia en la contratación entre empresarios; según el Alto Tribunal el legislador ha reservado el plus de protección que implica el control de transparencia de las cláusulas de adhesión a los contratos celebrados con consumidores, debiendo en otro caso limitarse al control de incorporación, que se limita a la transparencia documental o gramatical de la cláusula.

(2) La sentencia del Pleno del Tribunal Supremo de 25 de marzo de 2015 limita la retroactividad de la nulidad de las cláusulas suelo a los pagos de intereses efectuados en aplicación de ella posteriores a la fecha de publicación de la sentencia de 9 de mayo de 2013.


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

Don/Doña [NOMBRE Y APELLIDOS], Procurador de los Tribunales, actuando en nombre de Don/Doña [NOMBRE Y APELLIDOS] y Don/Doña [NOMBRE Y APELLIDOS], cuya representación tengo acreditada en los autos de juicio ordinario [Nº DE PROCEDIMIENTO], seguidos a instancia de esta parte contra la entidad [DENOMINACIÓN SOCIAL], ante el Tribunal comparezco y como mejor proceda en derecho DIGO:

Que, mediante el presente escrito y en la indicada representación interpongo, en el plazo conferido al efecto, y conforme a los arts. 458 y ss. LEC, RECURSO DE APELACIÓN contra Sentencia de fecha [FECHA], notificada a esta parte en fecha [FECHA].

REQUISITOS PROCESALES

I.- Se presenta este escrito de interposición ante ese Tribunal, que es el competente para conocer del recurso, con arreglo al art. 458.1 LEC.

II.- Se presenta este escrito de interposición dentro del plazo de veinte días contados desde el día siguiente a la notificación de la resolución impugnada (art. 458.1 y 3 LEC).

III.- Esta parte se halla legitimada por afectarle desfavorablemente la resolución impugnada, conforme exige el art. 448.1 LEC.

IV.- Las exigencias de postulación se llenan para este escrito de interposición, ya que está comparecida esta parte mediante Procurador de los Tribunales, y asistida de abogado en ejercicio, ambos colegiados y habilitados para ejercer ante el Tribunal (arts. 23.1 y 31.1 LEC).

FUNDAMENTOS DEL RECURSO

ÚNICO

Por infracción, en concepto de interpretación errónea y consecuente inaplicación, de los arts. 3 y 4 del Texto Refundido de la Ley General para la Defensa de los Consumidores y Usuarios, aprobado por Real Decreto Legislativo 1/2007, de 16 Noviembre (TRLGDCU), que eran aplicables para resolver la cuestión objeto de debate, ya que la sentencia de instancia niega la condición de consumidores de los demandantes en base a la alegación de la parte demandada de que no son consumidores medios y que el inmueble fue adquirido como inversión empresarial, y la valoración del resultado probatorio, no permite dichas conclusiones.

Así, dispone el art. 3 TRLGDCU que "A efectos de esta ley y sin perjuicio de lo dispuesto expresamente en sus libros tercero y cuarto, son consumidores o usuarios las personas físicas que actúen con un propósito ajeno a su actividad comercial, empresarial, oficio o profesión. Son también consumidores a efectos de esta norma las personas jurídicas y las entidades sin personalidad jurídica que actúen sin ánimo de lucro en un ámbito ajeno a una actividad comercial o empresarial". Añade a ello el art. 4 de dicho texto legal que "A efectos de lo dispuesto en esta norma, se considera empresario a toda persona física o jurídica, ya sea privada o pública, que actúe directamente o a través de otra persona en su nombre o siguiendo sus instrucciones, con un propósito relacionado con su actividad comercial, empresarial, oficio o profesión".

De este modo, resulta ser el destino del préstamo o crédito el que determina si el cliente, la persona física y/o jurídica que suscribe el mismo con la entidad bancaria, ha actuado en un ámbito ajeno o no al empresarial, y en el presente caso, aunque los demandantes hubiesen adquirido la vivienda como inversión o para alquilarla, no se puede considerar por ello que actúen en un ámbito empresarial o profesional y por lo tanto ha de considerarse a los mismos como consumidores a los efectos de la aplicación de la normativa tuitiva de los mismos, tal como señala, entre otras, la SAP Pontevedra de 14 de octubre de 2014, rec. 377/2014, en su Fundamento de Derecho Segundo, en el que se declara que si esa actividad de arrendamiento de un bien a terceros "no forma parte del conjunto de las actividades comerciales o empresariales de quien lo realiza, éste podrá seguir siendo considerado consumidor con arreglo a la normativa vigente, en la medida en que no opera la circunstancia de exclusión incluida en el art. 3.1", añadiendo que "el ánimo de lucro no es un requisito que excluya de la protección de las normas específicas a los consumidores, siempre que la actividad no resulte habitual o forme parte de su profesión u oficio".

A este respecto señalar que según consta en la escritura aportada por la parte actora (documento n.º [NÚMERO] de la demanda) el préstamo se destinó a la adquisición de una vivienda unifamiliar con su terreno unido sita en [LOCALIDAD], y que el demandante, Don/Doña [NOMBRE Y APELLIDOS], con estudios de diplomado en empresariales y de profesión profesor y jefe de estudios de un colegio, y su mujer Don/Doña [NOMBRE Y APELLIDOS] solicitaron la subrogación en el préstamo hipotecario inicial del promotor para la adquisición de su vivienda habitual, si bien tienen también un apartamento en [LOCALIDAD], pero que no la adquirieron con fines de inversión sino que usan habitualmente dicha vivienda, que Don/Doña [NOMBRE Y APELLIDOS] no solicitó asesoramiento financiero y lleva trabajando en el colegio más de 20 años y no se dedica a temas empresariales ni inmobiliarios, todo lo cual no fue desmentido por los testigos propuestos por la entidad bancaria (minutos [MINUTO DE LA GRABACIÓN] y [MINUTO DE LA GRABACIÓN] de la grabación del juicio que consta en autos), y consta confirmado en la documentación obrante en autos (folios [Nº DE FOLIOS]), consistente en certificado del colegio en el que trabaja el demandante y certificado de la AEAT en el que consta que el demandante no se encontraba dado de alta en el censo de actividades económicas en el ejercicio [EJERCICIO], no constando indicio alguno en autos de que el inmueble adquirido no constituya la vivienda habitual de los demandantes.

Pues bien, siendo el destino del préstamo el que determina si la persona física ha actuado en un ámbito ajeno o no al empresarial y en atención a tales declaraciones y documentación, ha de declararse que los demandantes ostentan la condición de consumidores y, en consecuencia, es de aplicación el TRLGDCU.

Por lo expuesto,

SUPLICO A LA SALA

Que, teniendo por presentado este escrito con su copia, y documento/s acompañado/s, de lo que se ha dado traslado al Procurador de la parte contraria en la forma que previene el art. 276 LEC, se sirva tener por INTERPUESTO RECURSO DE APELACIÓN contra la resolución de fecha [FECHA] y,

SUPLICO A LA AUDIENCIA PROVINCIAL

Que, seguido que sea el legal procedimiento, dicte sentencia que revoque la de instancia, y resolviendo sobre la cuestión que es objeto de proceso, estime en su integridad la demanda, declarando la nulidad de la cláusula suelo contenida en el contrato de préstamo con garantía hipotecaria de fecha [FECHA], por abusiva y condenando a la demandada a restituir las cantidades abonadas por la parte demandante como consecuencia de la aplicación de dicha cláusula desde la fecha de publicación de la sentencia del TS de 9 de mayo de 2013, rec. 485/2012, y todo ello con imposición de las costas causadas a la demandada.

Es de Justicia que pido en [LUGAR], a [FECHA],

OTROSÍ PRIMERO DIGO, que se acompaña a este escrito resguardo acreditativo del pago del depósito de 50 euros en la Cuenta de Depósitos y Consignaciones del Tribunal al que se dirige, conforme exige la disposición adicional 15.ª LOPJ, por lo que,

SUPLICO A LA SALA

Que tenga por causada la manifestación anterior a los efectos oportunos.

[OPCIONAL — incluir si procede]

OTROSÍ SEGUNDO DIGO que conforme a lo regulado en el art. 460 LEC, se interesa la práctica en segunda instancia de las siguientes PRUEBAS:

— [MEDIO DE PRUEBA], que fue propuesta y admitida en la primera instancia pero, por causa no imputable a mi representación, no pudo practicarse ni siquiera como diligencia final.
— [MEDIO DE PRUEBA], que fue indebidamente denegada en la primera instancia, habiéndose formulado la oportuna protesta en la vista.
— [MEDIO DE PRUEBA], ya que se refiere a hechos de relevancia para la decisión del pleito ocurridos después del comienzo del plazo para dictar sentencia en la primera instancia.
— [MEDIO DE PRUEBA], puesto que se refiere a hechos de relevancia para la decisión del pleito ocurridos antes del plazo para dictar sentencia, y de los que esta parte ha tenido conocimiento con posterioridad, como ha quedado justificado en las alegaciones formuladas en este escrito.

En virtud de lo expuesto,

A LA SALA SUPLICO

Que se tenga por solicitada la práctica de las pruebas señaladas en la segunda instancia.

[OPCIONAL — incluir si procede]

OTROSÍ TERCERO DIGO que de conformidad con lo dispuesto en el art. 464 LEC solicito que se acuerde la celebración de vista pública.

SUPLICO A LA AUDIENCIA PROVINCIAL

Que teniendo por causada la manifestación anterior a los efectos oportunos, se sirva acordar de conformidad, como es procedente en Justicia que reitero.

Por ser de Justicia que pido en [LUGAR], a [FECHA].

Firma de Abogado/a	Firma de Procurador/a
