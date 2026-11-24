---
name: demanda-juicio-ordinario-reclamar-precio-impagado-civ-0735
description: "Demanda de juicio ordinario para reclamar el precio impagado de una compraventa. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio ordinario para reclamar el precio impagado de una compraventa

> Formulario **CIV-0735** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio declarativo ordinario por la que el vendedor reclama el precio impagado de una compraventa mercantil (en el modelo, una máquina), dirigida a la Sección Civil del Tribunal de Instancia y adaptada a la LO 1/2025 (requisito de procedibilidad). Se usa cuando el comprador ha recibido la cosa y no paga el saldo pendiente y la cuantía exige juicio ordinario.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio ordinario para reclamar el precio impagado de una compraventa» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio ordinario para reclamar el precio impagado de una compraventa” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:demanda-juicio-ordinario-reclamar-precio-impagado-civ-0735`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº DE DOCUMENTO (8 veces)
- [ ] IMPORTE (6 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] DÍA (4 veces)
- [ ] MES (4 veces)
- [ ] AÑO (3 veces)
- [ ] DOMICILIO (3 veces)
- [ ] IMPORTE EN LETRA (3 veces)
- [ ] CORREO ELECTRÓNICO (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL DEMANDADO (2 veces)
- [ ] TELÉFONO (2 veces)
- [ ] ACTIVIDAD
- [ ] COLEGIO
- [ ] DOMICILIO DEL ESTABLECIMIENTO
- [ ] DOMICILIO LABORAL
- [ ] FECHA
- [ ] FECHAS
- [ ] IMPORTE TOTAL EN LETRA
- [ ] MARCA
- [ ] MODELO
- [ ] NOMBRE DEL NOTARIO
- [ ] NOMBRE Y APELLIDOS DEL DEMANDANTE
- [ ] NOMBRE Y APELLIDOS DEL LETRADO/A
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] Nº DE COLEGIADO
- [ ] SEDE

## Normas que cita el formulario

- art. 24.1 LEC
- art. 399.1 LEC
- art. 45 LEC
- art. 85.1.º LOPJ
- art. 249.2 LEC
- art. 6 LEC
- art. 251.1 LEC
- art. 5 Ley Orgánica 1/2025
- art. 1445 Código Civil
- art. 1124 Código Civil
- art. 1100 Código Civil
- art. 1168 Código Civil
- art. 394 LEC
- art. 24.2 LEC
- art. 1225 Código Civil
- art. 155.3 LEC

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] QUE POR TURNO CORRESPONDA»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] QUE POR TURNO CORRESPONDA

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales y de D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDANTE], con domicilio en [DOMICILIO], representación que acredito mediante escritura de poder otorgada a mi favor (el art. 24.1 LEC prevé tres formas de otorgar el apoderamiento al Procurador),

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— (Si el poder se otorga a través de la sede judicial electrónica).- mediante comparecencia electrónica, a través de la sede judicial electrónica e inscrito en el Registro Electrónico de Apoderamientos Judiciales; y a cuya justificación acompaño certificación de dicho Registro aportada como Documento n.º [Nº DE DOCUMENTO], y que se puede acreditar mediante consulta automatizada orientada al dato, por parte del órgano judicial al cual tengo el honor de dirigirme.

— (Si el poder se otorga mediante comparecencia apud acta).- mediante comparecencia personal apud acta ante el Tribunal Decano de [LOCALIDAD], posteriormente inscrito en el Registro Electrónico de Apoderamientos Judiciales; y a cuya justificación acompaño certificación de dicho Registro aportada como Documento n.º [Nº DE DOCUMENTO], y que se puede acreditar mediante consulta automatizada orientada al dato, por parte del órgano judicial al cual tengo el honor de dirigirme.

— (Si el poder se otorga ante Notario).- mediante escritura de poder otorgada a mi favor, ante el Notario/Notaria [NOMBRE DEL NOTARIO], con Notaría sita en [LOCALIDAD]. El poder se inscribió en el Registro Electrónico de Apoderamientos Judiciales; lo cual justifico mediante certificación de dicho Registro aportada como Documento n.º [Nº DE DOCUMENTO], y que se puede acreditar mediante consulta automatizada orientada al dato, por parte del órgano judicial al cual tengo el honor de dirigirme.

bajo la dirección letrada de D./Dña. [NOMBRE Y APELLIDOS DEL LETRADO/A], abogado/a en ejercicio, con despacho profesional abierto en [DOMICILIO], colegiado n.º [Nº DE COLEGIADO] del Ilustre Colegio de la Abogacía de [COLEGIO], ante el Tribunal comparezco y como mejor en Derecho proceda,

DIGO

Que mediante el presente escrito vengo a formular DEMANDA DE JUICIO DECLARATIVO ORDINARIO y RECLAMACIÓN DE CANTIDAD, contra D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDADO], con domicilio, primero, en [DOMICILIO] de [LOCALIDAD] [OPCIONAL — si ha lugar: ; y segundo, el domicilio laboral en [DOMICILIO LABORAL] de [LOCALIDAD]]; con email [CORREO ELECTRÓNICO] y con número de teléfono móvil [TELÉFONO]; en ejercicio de la acción de [ACCIÓN EJERCITADA: cumplimiento de contrato / reclamación de cantidad], según se especificará en el cuerpo del escrito y en el suplico, y todo ello de conformidad con los siguientes hechos y fundamentos de derecho.

Que esta parte asume el compromiso de recibir cualquier comunicación dirigida por la oficina judicial, durante toda la fase declarativa e, incluso, en una eventual fase de ejecución, por medios telemáticos, en términos del art. 399.1 II LEC, consignándose a estos efectos la siguiente dirección de correo electrónico y n.º de teléfono: [CORREO ELECTRÓNICO] / [TELÉFONO].

HECHOS

PRIMERO.- El demandado explota en esta ciudad, en la calle [DOMICILIO DEL ESTABLECIMIENTO], un establecimiento dedicado a la industria de [ACTIVIDAD].

SEGUNDO.- Para atender a las necesidades de su negocio, con fecha [DÍA] de [MES] de [AÑO], el demandado adquirió de mi representado una máquina inyectora marca [MARCA], modelo [MODELO], por el precio de [IMPORTE EN LETRA] euros ([IMPORTE] €). El pago debería realizarse entregando en el acto a cuenta [IMPORTE] euros y el resto el [DÍA] de [MES] de aquel mismo año, con una cláusula penitencial de pérdida de la primera suma si no se llevaba a efecto la operación.

Se acompaña como DOCUMENTO N.º [Nº DE DOCUMENTO] el contrato de compraventa en el que consta el importe, condiciones y plazos estipulados.

TERCERO.- La entrega de la maquinaria se efectuó en fecha [DÍA] de [MES] de [AÑO] a entera satisfacción de la parte demandada, «pintada y repasada», haciéndose constar que el comprador recibía el objeto vendido después de haberlo examinado y tras realizar demostración previa a su entrega, haciéndose las pertinentes pruebas de funcionamiento por el técnico habitual y verificándose que la maquinaria funcionaba con normalidad y se acomodaba a las condiciones estipuladas en el contrato.

Se acompaña para acreditar los anteriores extremos el albarán de entrega firmado por el demandado como DOCUMENTO N.º [Nº DE DOCUMENTO].

CUARTO.- Conforme a lo estipulado y a fin de que el demandado abonara el saldo pendiente, mi patrocinado giró a su cargo una letra por el referido importe, que fue devuelta impagada, ocasionando con ello los correspondientes gastos. Todo ello se acredita con el BLOQUE DOCUMENTAL N.º [Nº DE DOCUMENTO].

QUINTO.- El demandado ha dejado de satisfacer la cantidad de [IMPORTE EN LETRA] euros ([IMPORTE] €), de los [IMPORTE TOTAL EN LETRA] euros a que ascendía el importe total de la compra.

SEXTO.- La parte actora manifiesta que, previamente a la presentación de la presente demanda, se han llevado a cabo negociaciones con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria; incluyéndose entre las acciones realizadas el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución.

Finalmente, mi representado envió un requerimiento fehaciente al demandado con fecha [FECHA], fijando un plazo de 30 días naturales para llegar a un acuerdo amistoso, a través del abogado que firma este escrito, el cual fue contestado por el demandado por el mismo medio, [ELEGIR: rechazando el acuerdo / habiendo sido solo posible un acuerdo parcial], viéndonos en la necesidad de acudir a la presente vía judicial, respecto a los extremos de la controversia en los que se mantiene la discrepancia.

Acompaño como documento n.º [Nº DE DOCUMENTO] el requerimiento efectuado y como documento n.º [Nº DE DOCUMENTO] la contestación del demandado.

SÉPTIMO.- A la vista del tiempo transcurrido, sin que al día de la fecha el demandado haya satisfecho la cantidad adeudada a mi representado, y habiendo sido infructuosas las gestiones extrajudiciales previamente intentadas para el cobro de la misma, nos vemos obligados a acudir a la vía judicial.

A los anteriores hechos son aplicables los siguientes

FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN Y COMPETENCIA

Es competente la Sección Civil del Tribunal de Instancia del domicilio del demandado, al que se dirige la presente demanda, por aplicación de lo dispuesto en los arts. 45 y 50 de la LEC, en relación con lo dispuesto en el art. 85.1.º LOPJ.

II.- PROCEDIMIENTO

El procedimiento ajustado a derecho será el del juicio declarativo ordinario regulado en los arts. 399 a 436 de la misma Ley, atendiendo a la cantidad reclamada, que es de [IMPORTE] euros, en aplicación de lo dispuesto en el art. 249.2 de la LEC.

III.- CAPACIDAD Y REPRESENTACIÓN

Tanto el demandante como el demandado tienen capacidad para ser parte y capacidad procesal, conforme a los artículos 6 y 7 de la LEC.

[OPCIONAL — si ha lugar: consignar las alegaciones que procedan sobre capacidad de las partes, representación de ellas o del Procurador/a.]

IV.- LEGITIMACIÓN

Corresponde al demandante la activa por ser la parte que ha cumplido sus obligaciones como vendedor al entregar la cosa objeto del contrato, y la pasiva la tiene el demandado en cuanto obligado como comprador a satisfacer el precio convenido.

V.- CUANTÍA

Conforme a los arts. 251.1 y 253 de la LEC cifro la cuantía de la presente demanda en [IMPORTE] euros, que es el importe de la cantidad que se reclama.

VI.- POSTULACIÓN Y DEFENSA

Conforme a lo previsto en los arts. 23 y 31 de la Ley de Enjuiciamiento Civil, se presenta la demanda por medio de Procurador/a legalmente habilitado y bajo dirección de Letrado firmante de la misma.

VII.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4.º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

VIII.- FONDO DE LA CUESTIÓN CONTROVERTIDA

Se ejercita acción de cumplimiento contractual en base a los siguientes preceptos:

Artículo 1089 del Código Civil en cuanto establece que las obligaciones nacen de la Ley, de los contratos y otros supuestos; estas obligaciones nacidas de los contratos son recogidas en el art. 1091 del mismo Texto previniendo que las mismas tienen fuerza de Ley entre las partes y habrán de ser cumplidas a tenor de los mismos.

Según el artículo 1445 del Código Civil, por el contrato de compra y venta uno de los contratantes se obliga a entregar una cosa determinada y el otro a pagar por ella un precio cierto en dinero o signo que lo represente, y el artículo 1450 señala que la venta se perfeccionará entre comprador y vendedor, y será obligatoria para ambos, si hubieren convenido en la cosa objeto del contrato y en el precio.

En el presente caso queda patente la perfección y consumación del contrato, pues hubo acuerdo y aceptación en la cosa y en el precio, y solamente una de las partes, mi mandante, ha cumplido lo pactado, por lo que el incumplimiento de la obligación de pago por parte del demandado nos obliga a presentar esta demanda, con cita asimismo del art. 1124 del Código Civil, que en su párrafo segundo concede al perjudicado por el incumplimiento en las obligaciones sinalagmáticas la facultad de exigir el cumplimiento o la resolución de la obligación con resarcimiento de daños y abono de intereses en ambos casos.

Citamos los artículos 1100, 1101 y 1108 del Código Civil en cuanto a la mora y a la exigencia de indemnización por daños y perjuicios.

En cuanto a los gastos extrajudiciales que ocasione el pago, serán de cuenta del deudor con arreglo al art. 1168 del Código Civil.

IX.- COSTAS

Conforme al artículo 394 de la LEC, las costas han de imponerse a la parte demandada.

Por lo expuesto,

SUPLICO AL TRIBUNAL

Que habiendo por presentado este escrito de demanda con los documentos que lo acompañan y copias de uno y otros, los admita y me tenga por comparecido en parte en la representación que ostento y que acreditada dejo; y por promovido juicio declarativo ordinario frente a D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDADO], acuerde dar traslado al demandado para que comparezca y la conteste, y previos los trámites legales y recibimiento a prueba que desde ahora se interesa, se dicte en su día sentencia por la que, estimando la demanda, se condene al demandado a abonar a mi mandante la cantidad de [IMPORTE EN LETRA] euros ([IMPORTE] €), incrementada con el interés legal desde la interposición de la demanda.

Todo ello con imposición de las costas del juicio a la parte demandada.

Es justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Abogado/a Firma del Procurador/a

NOTAS DE AYUDA

(1) Acreditación del poder: todos los poderes deben estar inscritos en el Registro Electrónico de Apoderamientos Judiciales (REAJ). Para su acreditación basta, en principio, la consulta automatizada orientada al dato de dicho Registro, que está a disposición de cualquier Letrado de la Administración de Justicia. Dado que el art. 24.2 LEC configura la certificación de la inscripción como vía subsidiaria, para el caso de que el sistema no permita aquella consulta, el modelo prevé que se acompañe certificación electrónica, que el sistema permite emitir a quien inscribe el poder.

(2) Notas de interés: para esta reclamación podrá acudirse también al juicio monitorio, siendo los documentos el contrato y la letra; y, en base a ésta última, puede plantearse un juicio cambiario si la letra reúne todos los requisitos legales. Debe tenerse en cuenta, por otro lado, que la acción cambiaria puede ejercitarse también en un proceso declarativo, con el efecto que ello puede tener en materia de prescripción.

(3) Normativa aplicable: Código Civil, artículos 1089, 1091, 1100, 1101, 1108, 1124, 1168, 1445 y 1450. Ley 1/2000, de 7 de enero, de Enjuiciamiento Civil, artículos 6, 7, 23, 31, 45, 50, 249.2, 251.1, 253, 394 y 399 a 436.

(4) Jurisprudencia de interés: Sentencia de la Audiencia Provincial de Badajoz, Sección 3.ª, n.º 29/2012, de 26 de enero de 2012, Rec. 334/2011: «En este tipo de relaciones negociales la prueba documental suele estar constituida por facturas y albaranes; la factura es un documento privado, emitido por una sola de las partes y, por lo tanto, no puede tener plena eficacia probatoria; la jurisprudencia, en cuanto al valor probatorio que se ha de reconocer a las facturas unilateralmente expedidas por la parte actora, en las que no consta el reconocimiento por el deudor a quien perjudican, niega que tengan valor por sí solas (Sentencias de la Audiencia Provincial de Murcia de 25 abril 1994 y de la Audiencia Provincial de Albacete de 18 mayo 1998). La factura no es un documento regulado en el C.Comercio, pero aparece en el art. 10.1.b) de la Ley General de Defensa de los Consumidores y Usuarios de 1984 como "documento acreditativo de la operación" que contiene la relación de los bienes adquiridos y de su importe y que hace prueba contra el adquirente si la acepta. Así la factura cobra eficacia probatoria a favor del comprador si éste la retiene en su poder; o a favor del vendedor, si es reconocida por el comprador, o si van acompañadas de los albaranes que en la práctica mercantil se firman por el comprador tras la entrega de la cosa vendida o servicio prestado. Los albaranes no aparecen regulados en la legislación mercantil, sin embargo constituyen habituales usos de comercio que vienen a agilizar la negociación mercantil. El albarán es sólo un elemento instrumental de prueba que sirve para acreditar lo que realmente interesa, esto es, la realidad de un contrato o por ser más precisos, la realidad de su cumplimiento (Sentencia de la Audiencia Provincial de Córdoba de 12 marzo 2001). La Jurisprudencia del Tribunal Supremo establece que las facturas, por si solas no constituyen prueba plena y eficaz en orden a acreditar la realidad de un determinado suministro o servicio y ni tampoco para probar la certeza de una deuda. Solamente cuando se ponen en relación con otros medios de prueba, resultan eficaces en tal sentido, pero siempre valorando en cada caso los hechos concretos objeto de enjuiciamiento con marginación por tanto de su conceptuación como un criterio de aplicación automática e inmediata (SSTS 30 septiembre 1991 y 17 diciembre 1992, rec. 1269/1991). Señala igualmente la Sentencia del Tribunal Supremo de 2 abril 1994, con cita de otras en igual sentido, que la falta de adveración en el proceso de un documento privado no le priva en absoluto de valor y procede ser tomado en consideración, ponderando su grado de credibilidad atendidas las circunstancias del debate. A partir de tales premisas analizamos las alegaciones del recurrente, consistentes en error en la apreciación de la prueba al admitir como válidos unos albaranes cuya firma se desconoce. El motivo resulta inadmisible, en aplicación del art. 1225 del Código Civil, de un análisis objetivo y desapasionado de la prueba se llega al razonable convencimiento de la autenticidad de los documentos que se acompañan con la demanda y a la realidad de su suscripción por parte de la demandada.»

(5) Domicilio del demandado: el art. 155.3 LEC permite expresar varios domicilios del demandado (el que aparezca en el padrón municipal o conste oficialmente a estos efectos; el que aparezca en registro oficial o en publicaciones de colegios profesionales, si se trata de empresas o personas colegiadas; donde desarrolle su actividad profesional o laboral no ocasional; si es empresa mercantil, el domicilio de cualquiera de sus administradores, gerentes o apoderados; o, si es asociación que consta en registro oficial, el domicilio del presidente, miembro o gestor de la Junta correspondiente). Cuando se señalen varios, se indicará el orden a seguir para la notificación, con vistas al éxito de la misma.

(6) El art. 155.3 LEC configura una obligación adicional del demandante, consistente en aportar cuantos datos sean de utilidad para localizar al demandado: número de identificación fiscal o de extranjeros, n.º de teléfono, dirección de correo electrónico o similares.
