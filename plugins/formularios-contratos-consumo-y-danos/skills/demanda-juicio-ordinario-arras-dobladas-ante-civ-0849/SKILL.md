---
name: demanda-juicio-ordinario-arras-dobladas-ante-civ-0849
description: "Demanda de juicio ordinario por las arras dobladas ante el desistimiento en la venta de un inmueble. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio ordinario por las arras dobladas ante el desistimiento en la venta de un inmueble

> Formulario **CIV-0849** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio ordinario en que se reclaman a los vendedores las arras dobladas por desistimiento de contrato de compraventa de un bien inmueble.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio ordinario por las arras dobladas ante el desistimiento en la venta de un inmueble» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio ordinario por las arras dobladas ante el desistimiento en la venta de un inmueble” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:demanda-juicio-ordinario-arras-dobladas-ante-civ-0849`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (14 veces)
- [ ] FECHA (7 veces)
- [ ] IMPORTE (5 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] Nº DE DOCUMENTO (5 veces)
- [ ] Nº (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] CALLE (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] IMPORTE EN CIFRA (2 veces)
- [ ] NOMBRE DE LA PARTE (2 veces)
- [ ] CORREO ELECTRÓNICO
- [ ] ENTIDAD BANCARIA
- [ ] FECHAS
- [ ] LUGAR
- [ ] Nº DE COLEGIADO/A
- [ ] PISO
- [ ] SEDE
- [ ] TELÉFONO

## Normas que cita el formulario

- art. 24.1 LEC
- art. 399.1 LEC
- art. 1.454 CC
- art. 85 LOPJ
- art. 45 LEC
- art. 50.1 LEC
- art. 7.1 LEC
- art. 5.2 LEC
- art. 23.1 LEC
- art. 31.1 LEC
- art. 399 LEC
- art. 249.1 LEC
- art. 251.1.ª LEC
- art. 5 Ley Orgánica 1/2025
- art. 1.091 CC
- art. 1.258 CC
- art. 217.3 LEC
- art. 1.256 CC
- art. 394.1 LEC

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

Notas al pie del formulario original:
(1) A la hora de su acreditación, todos los poderes deben estar inscritos en el Registro Electrónico de Apoderamientos Judiciales (REAJ). Se supone que, para su acreditación, basta con la consulta (de dicho Registro) automatizada orientada al dato. Algo que está a disposición de cualquier Letrado de la Administración de Justicia. Sin embargo, dado que el art. 24.2 LEC, configura la certificación de dicha inscripción como vía subsidiaria de acreditación, para el caso de que el sistema no permita aquella consulta automatizada; se señala en el modelo que se acompaña certificación electrónica. El sistema permite emitir dicha certificación para quien inscribe el poder.

(2) El art. 155.3 LEC permite fijar expresar varios domicilios del demandado (el que aparezca en el padrón municipal o conste oficialmente a estos efectos; el que aparezca en Registro oficial o en publicaciones de colegios profesionales, si se trata de empresas o personas colegiadas; donde desarrolle su actividad profesional o laboral no ocasional; si es empresa mercantil, el domicilio de cualquiera de sus administradores, gerentes, o apoderados; o, si es asociación que consta en registro oficial; el domicilio del presidente, miembro o gestor de la Junta correspondiente). Cuando se señalen varios, indicará el orden a seguir para la notificación, con vistas al éxito de la misma.

(3) El art. 155.3 LEC configura una obligación adicional del demandante, consistente en aportar cuantos datos sean de utilidad para localizar al demandado: número de identificación fiscal o de extranjeros, nº [Nº] de teléfono o de fax, dirección de correo electrónico, o similares.

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales y de D./Dña. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], representación que acredito mediante escritura de poder otorgada a mi favor (existen tres posibilidades para otorgar el apoderamiento al Procurador de los Tribunales, conforme dispone el art. 24.1 LEC)

[OPCIONAL — opción en función de cómo se haya otorgado el poder]

[ELEGIR UNA OPCIÓN: Si el poder se otorga a través de la sede judicial electrónica / Si el poder se otorga mediante comparecencia apud acta / Si el poder se otorga ante Notario]

bajo la dirección letrada de D./Dña. [NOMBRE Y APELLIDOS], abogado/a en ejercicio, con despacho profesional abierto en [LOCALIDAD], colegiado nº [Nº DE COLEGIADO/A] del Ilustre Colegio de la Abogacía de [LOCALIDAD], ante el Tribunal comparezco y como mejor en Derecho proceda, DIGO:

Que mediante el presente escrito vengo a formular DEMANDA DE JUICIO DECLARATIVO ORDINARIO EN RECLAMACIÓN DE CANTIDAD, contra D./Dña. [NOMBRE Y APELLIDOS], con domicilio, primero en [DOMICILIO]; y segundo, el domicilio laboral en [DOMICILIO]); con email [CORREO ELECTRÓNICO]; y con número de teléfono móvil [TELÉFONO]; todo ello de conformidad con los hechos y fundamentos de derecho que se especificarán.

Que esta parte asume el compromiso de recibir cualquier comunicación dirigida por la oficina judicial, durante toda la fase declarativa, e, incluso, en una eventual fase de ejecución por medios telemáticos, en términos del art. 399.1 II LEC, consignándose a estos efectos la siguiente dirección de correo electrónico y nº [Nº] de teléfono:

HECHOS

PRIMERO.- Mi mandante, a través de su administrador social único, D./Dña. [NOMBRE Y APELLIDOS], convino con los demandados un contrato de compraventa de la vivienda del piso [PISO] de la calle [CALLE], n.º [NÚMERO] de [LOCALIDAD], el [FECHA], que se plasmó en el documento que como n.º [Nº] se acompaña.

En el ordinal segundo de las disposiciones documentadas, extremo 1), párrafo segundo, se dijo que la compradora, hoy demandante, entregaba [IMPORTE] euros en el acto, ‘siendo dicha cantidad en concepto de arras penitenciales, conforme establece el art. 1.454 CCiv, pudiendo el vendedor desistir de la presente venta, devolviendo por duplicadas las arras al comprador [IMPORTE], o desistir el comprador, perdiendo la cantidad entregada en concepto de arras’.

SEGUNDO.- Dicho documento fue redactado por la Agencia de la Propiedad Inmobiliaria ‘ ‘, que era la encargada por los demandados para la gestión de venta, y antes de su firma se facilitó copia del modelo a esta parte, por lo que se supone que igualmente a los vendedores, firmándose el día de su fecha el original y dos copias en la oficina de dicha Agencia.

TERCERO.- Conforme se prueba con el respectivo documento original, que aportamos como documento n.º [Nº], con fecha [FECHA], la abogada de los demandados, Sr./a. [NOMBRE Y APELLIDOS], en nombre y como mandataria de sus clientes, como literalmente se dice, enteró al abogado de los actores, Sr./a [NOMBRE Y APELLIDOS], el cual suscribía recibo y se comprometía a hacerlo llegar a sus patrocinados, una notificación en forma de ‘la voluntad de mis representados de rescindir el contrato suscrito entre ellos, y [NOMBRE DE LA PARTE], con fecha [FECHA], haciendo uso de la facultad de desistir del referido contrato prevista en la cláusula segunda, condición 1.ª ".

En la carta se invitaba a que los compradores facilitaran número de cuenta bancaria o cualquier otro medio de pago acreditativo, para hacer efectivas las cantidades que debía reembolsar la parte vendedora.

CUARTO.- En carta que suscribía D./Dña. [NOMBRE Y APELLIDOS], demandado, el [FECHA], se afirmaba que ‘tal desistimiento es ajeno a nuestra voluntad, y está determinado principalmente porque tras haber sido asesorados en el Departamento de Vivienda del Gobierno Autonómico, la vivienda a transmitir, situada en la calle [CALLE], n.º [NÚMERO] de [LOCALIDAD], se halla acogida a la Ley de Viviendas de Protección Oficial. Por tanto, se encuentra sujeta a las prohibiciones y limitaciones derivada del régimen de viviendas de protección oficial, no siendo libre su venta en la actualidad’.

Se acompaña como documento n.º [Nº DE DOCUMENTO].

QUINTO.- Transcurridos ocho meses y medio desde la firma del documento privado, y después de variopintas discusiones entre los abogados de las partes, los demandados devolvieron a la compradora, mi patrocinada, los [IMPORTE] millones entregados por ésta, que tuvieron por espacio de ocho meses y medio, mediante ingreso en la cta. cte. n.º [NÚMERO] del Banco [ENTIDAD BANCARIA], aperturada por [NOMBRE Y APELLIDOS].

Se acompaña resguardo de abono como documento n.º [Nº DE DOCUMENTO].

SEXTO.- Han sido infructuosos todos los intentos de lograr avenencia de los vendedores a que cumplieran sus compromisos, aduciéndose por estos diversidad de excusas, por lo que en fecha [FECHA], mi poderdante remitió por conducto notarial carta en que se exigía a los demandados que doblaran la suma, que en concepto de contraprestación por haberse de allanar mi parte a la denuncia del contrato que se pactó, y el silencio ante la misma de los demandados es lo que justifica la ‘litis’.

Adjuntamos el acta notarial con carta y acuse de recibo como documento n.º [Nº DE DOCUMENTO].

A estos hechos le son de aplicación los siguientes:

SÉPTIMO.- La parte actora manifiesta que, previo a la presentación de la presente demanda, se han llevado a cabo negociaciones con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad, y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria; incluyéndose entre las acciones realizadas el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución.

Finalmente, mi representado envió un requerimiento fehaciente al demandado con fecha [FECHA], fijando un plazo de 30 días naturales para llegar a un acuerdo amistoso, a través del abogado que firma este escrito, el cual fue contestado por el demandado por el mismo medio, rechazando el acuerdo/ habiendo sido solo posible un acuerdo parcial, viéndonos en la necesidad de acudir a la presente vía judicial, respecto a los extremos de la controversia en los que se mantiene la discrepancia.

Acompaño como documento nº [Nº DE DOCUMENTO], el requerimiento efectuado y como documento nº [Nº DE DOCUMENTO], la contestación del demandado.

FUNDAMENTOS DE DERECHO

JURÍDICO PROCESALES

A) Subjetivos:

I.- COMPETENCIA

Sin duda en cuanto a la jurisdicción de los tribunales del Reino en su orden civil, le corresponde conocer de este asunto al Tribunal a quien tengo el honor de dirigirme por ser el de Instancia (art. 85 LOPJ y art. 45 LEC) del lugar del domicilio de los demandados, puesto que corresponde en fuero genérico de las personas físicas del art. 50.1 LEC, dado que no hay previsto otro específico para la materia o acción que se ejercita.

II.- PARTES

CAPACIDAD. Tanto la actora, mi patrocinada, como los dos demandados, la primera sociedad mercantil intitulada e inscrita, y los segundos personas físicas mayores de edad, respecto de las que no consta limitación de ejercicio de derechos civiles, detentan capacidad para ser parte (arts. 6.1.1.º y 3.º LEC), y capacidad procesal, o de obrar en este concreto juicio (art. 7.1 y 4 LEC).

LEGITIMACIÓN. Le corresponde la legitimación activa ordinaria directa (art. 10 párrafo 1.º LEC) a mi representada por su condición de compradora en el contrato objeto del pleito, titular del derecho de crédito, y ostentan los demandados la legitimación pasiva correlativa, por ser quienes tenían carácter de vendedores en el mismo contrato, y sobre los que pesa la obligación por haber desistido, a ambos a quienes afecta la pretensión indemnizatoria que se formula (art. 5.2 LEC), ya que a pesar de que cualquiera de los casados en régimen de gananciales puede defender los bienes e intereses comunes por vía de excepción (art. 1.385 párrafo 2.º CCiv), los dos codemandados fueron contratantes.

POSTULACIÓN. Esta parte, como será debido para la personación que convenga a la contraria, comparece por medio de Procurador/a de los Tribunales habilitado ante el tribunal (art. 23.1 LEC), y bajo la dirección del Letrado en ejercicio (art. 31.1 LEC).

B) Objetivos:

III PROCEDIMIENTO

El procedimiento a través del cual se ha de sustanciar la pretensiones el correspondiente al JUICIO ORDINARIO, conforme a los arts. 248 y 249.2 LEC, y se seguirá por los trámites de los arts. 399 a 436 LEC, puesto que es aplicable el criterio subordinado de la cuantía superior a 15.000 euros, dado que la materia no es de las listadas en el art. 249.1 LEC.

IV.- CUANTÍA

Se señala como cuantía de la demanda la de [IMPORTE] euros ([IMPORTE EN CIFRA] €), que integra la cantidad líquida reclamada conforme al art. 251.1.ª LEC.

V.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD. La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

JURIDICO SUSTANTIVOS

Se agita una acción de cumplimiento del pacto de facultativo desistimiento unilateral del contrato por el vendedor a cambio del pago de arras dobladas.

Validez del contrato. El contrato privado de compraventa fue redactado conforme a un modelo ‘ad hoc’ que preparó la Agencia de la Propiedad Inmobiliaria [NOMBRE Y APELLIDOS], lo cual, en absoluto puede servir para privar de efectos vinculantes a las estipulaciones del mismo. Prevenciones legales especiales hay, en protección de consumidores y usuarios, que se refieren a contratos de adhesión en las relaciones entre empresario y adherente, y no tiene nada qué ver con los modelos o formularios de contrato de los que puedan valerse los particulares para convenir, siendo además que precisamente los demandados fueron los que reclutaron dicha Agencia para la intermediación. El principio de Derecho (art. 6.1 en relación con art. 1.091 CCiv), es que los mayores de edad, sin que hayan sido incapacitados por sentencia firme, pueden contratar y se obligan con arreglo a toda la extensión consignada en art. 1.258 CCiv.

Si algún hecho impeditivo de la eficacia del contrato se alegara de contrario, a dicha parte correspondería la prueba (art. 217.3 LEC).

Si quien proporcionó el modelo de contrato e intermedió en la operación debió o no saber de algún aspecto técnico jurídico, o debió advertirlo a los vendedores, es algo perfectamente ajeno a la presente ‘litis’.

Interpretación. En el contrato existe una cláusula indubitada que pacta las arras del art. 1.454 CCiv, y si el canon hermenéutico de la voluntad realmente querida por los contratantes es cierto que se contempla en el art. 1.281 párrafo 2.º CCiv, es expresamente subsidiario de que los términos del contrato no sean suficientemente claros, principio de ‘in claris interpretatio non fit’ que subordina a todos los demás, y que no entran en juego más que si hay motivo para estimar que la voluntad aparente, que sea oscura, discrepa de la real. Además, la voluntad contractual prevalente es la concorde de los contratantes, y no la de uno de ellos, como pueden ser los vendedores en el caso, frente al tenor expreso y claro de una estipulación muy habitual, como la descrita en el fáctico.

Arras penitenciales. Hay que precisar los conceptos de resolución, rescisión y desistimiento, con relación al contrato, que son parcialmente diferentes, aunque es cierto que el mismo art. 1.454 CCiv, emplea el término de rescisión incorrectamente. Para lo que es menester aquí, debe tenerse en cuenta, que no tratamos de resolución contractual causal, ya que no ha habido denuncia de incumplimiento de obligaciones por ninguna de las partes, ni tampoco hay causa legal de rescisión, que es ajena al incumplimiento pero supone déficit de capacidad o fraudulencia en el Derecho común. Precisamente, se ha eludido incumplir por los vendedores mediante desistimiento, y lo que se denuncia es la obligación consecuente al contrato desistido, y no al cumplimiento del contrato.

El desistimiento es la resolución ‘ad nutum’ o sin una causa fundada en incumplimiento del contrato, que con el riesgo de la categoría científica no consagrada de los derechos potestativos, se ha dicho que es el derecho potestativo de resolución contractual por pacto [STS de 19 de junio de 1986], y que se regula en varias figuras contractuales típicas. En la compraventa no pertenece al contenido típico, pero se prevé como pacto posible en el citado precepto, y significa emitir una declaración de voluntad recepticia y eficaz cabalmente contraria a la que dio luz al contrato, retractándose y resolviéndolo.

Si se prueba un desistimiento o una ‘rescisión’ del art. 1.454 CCiv, con esas palabras, explicitado en documento que suscribió la abogada de los demandados, no tiene ningún sentido empeñarse en que los vendedores han actuado de buena fe, y aún que querían cumplir, porque ningún incumplimiento está en liza, habida cuenta que la facultad de desistir estaba pactada.

La doctrina jurisprudencial distingue en cuanto a las arras o señal de la compraventa, entre las confirmatorias, que suponen entrega de cosa o cantidad en signo de ratificación del contrato perfeccionado, las penitenciales, que suponen la misma entrega en previsión de una prerrogativa de desistimiento que se admite por las partes, y las penales, que se fijan en garantía de la indemnización de daños y perjuicios por el incumplimiento, sin autorización a la efectividad de un desistimiento [SSTS de 17 de febrero de 1982, 19 de octubre de 1984, 10 de marzo de 1986 ó 9 de marzo de 1989].

El contrato de autos expresa con claridad que se dieron arras penitenciales, y probado el desistimiento, procede declarar la obligación de los vendedores, de pago de otro tanto como la cantidad que entregó [NOMBRE Y APELLIDOS], y que le ha sido al fin devuelta.

Los demandados, en su discusión preprocesal, han aducido que las arras se pactaron para supuesto de desistimiento caprichoso, y no para imposibilidad de cumplir.

No puede aceptarse que la voluntad de los vendedores que, por sí y ante sí (en contravención del art. 1.256 CCiv), interpreten qué es lo caprichoso o no.

Las prohibiciones de disponer o las cargas de lo que se vende, tienen que ser conocidas y advertidas al comprador por el vendedor, ya que tocan a la capacidad contractual, la eficacia del negocio, y los vicios de cara a las acciones edilicias, siendo precisamente caprichoso concertar una compraventa con precio de [IMPORTE] euros, y de una vivienda, sin precaverse de la existencia de tales circunstancias, para ‘descubrirlas’ para cuando hay que transmitir el dominio, es decir, consumar la compraventa perfeccionada, y con precio parcialmente anticipado. De suyo, el vender sin mención de carga o prohibición de enajenar, que existiera, significaría un incumplimiento contractual radical de la compraventa. Retractarse, al comprobar una prohibición o gravamen, pues, es jurídicamente consecuencia caprichosa de la venta caprichosa, como no lo serían la pérdida de la cosa sin culpa, o las circunstancias sobrevenidas en los sujetos o el objeto, que no son ejemplos comparables. Lo que vedaba la compraventa, según la tesis de los demandados, era algo anterior a concertarla, y que no se advertía, ni se hacía desaparecer por el vendedor.

Por otro lado, en cuanto a la imposibilidad de cumplir, no se nos especifica qué impedía jurídicamente la venta, ya que lo que puede saberse de la normativa administrativa de viviendas de protección oficial, no indica prohibiciones, ni determinan nulidad del contrato, sino que son limitaciones del precio de venta, o derechos de adquisición preferente de la entidad gubernativa correspondiente.

En definitiva, el que no se intente acreditar perjuicio real de la actora, para nada interviene en la solución predicha de la condena a cumplir en este caso, puesto que ya se ha diferenciado, no es caso de arras como cláusula penal para acción de cumplimiento con indemnización de daños y perjuicios.

Intereses. El precio debido devenga intereses moratorios, al tipo legal, desde la constitución en mora por la intimación extrajudicial de [NOMBRE Y APELLIDOS], según se pide, y conforme a los arts. 1.100, 1.101 y 1.108 CCiv, ya que no hay problema de iliquidez.

COSTAS

Serán de cuenta de los codemandados, como previene el art. 394.1 LEC, consagrando el principio de vencimiento cuasiobjetivo para declarativos en primera instancia.

Por lo expuesto,

AL TRIBUNAL SUPLICO

que tenga por presentado este escrito, lo admita, y tenga por deducida DEMANDA DE JUICIO ORDINARIO en la representación que ostento de [NOMBRE DE LA PARTE] la admita frente a D./Dña. [NOMBRE Y APELLIDOS], y D./Dña. [NOMBRE Y APELLIDOS], a los que confiera traslado de la demanda para que la contesten, si fuera de su interés, luego reciba el pleito a prueba, y dicte en su día Sentencia por la que condene a los demandados a pagar a la entidad actora la cantidad deeuros (€ [IMPORTE EN CIFRA]), incrementada en los intereses calculados al tipo legal desde elhasta el dictado de la Sentencia, así como reintegren a la actora las costas del procedimiento.

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a
