---
name: demanda-juicio-ordinario-nulidad-compraventa-civ-0821
description: "Demanda de juicio ordinario de nulidad de compraventa por simulación absoluta. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio ordinario de nulidad de compraventa por simulación absoluta

> Formulario **CIV-0821** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio ordinario por la que un acreedor ejercita la acción de nulidad de un contrato de compraventa por simulación absoluta (inexistencia de causa, arts. 1275 y 1276 CC) frente al deudor y el comprador, cuando el deudor ha transmitido su único bien relevante para eludir el pago de la deuda; incluye otrosí de medida cautelar de anotación preventiva de demanda.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio ordinario de nulidad de compraventa por simulación absoluta» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio ordinario de nulidad de compraventa por simulación absoluta” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:demanda-juicio-ordinario-nulidad-compraventa-civ-0821`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº DE DOCUMENTO (13 veces)
- [ ] LOCALIDAD (6 veces)
- [ ] NOMBRE Y APELLIDOS DEL DEUDOR (6 veces)
- [ ] IMPORTE (5 veces)
- [ ] FECHA (4 veces)
- [ ] AÑO (2 veces)
- [ ] CORREO ELECTRÓNICO (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] DÍA (2 veces)
- [ ] FIRMA (2 veces)
- [ ] MES (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL COMPRADOR (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL DEMANDANTE (2 veces)
- [ ] Nº DE TELÉFONO (2 veces)
- [ ] SEDE (2 veces)
- [ ] ACTIVIDAD
- [ ] CLASE DE JUICIO
- [ ] DOMICILIO DEL INMUEBLE
- [ ] DOMICILIO LABORAL
- [ ] DOMICILIO PROFESIONAL
- [ ] FECHA O PERÍODO
- [ ] FECHAS
- [ ] IMPORTE EN LETRA
- [ ] IMPORTE EN NÚMERO
- [ ] NOMBRE DEL NOTARIO
- [ ] NOMBRE Y APELLIDOS DEL ABOGADO/A
- [ ] NOMBRE Y APELLIDOS DEL PRIMER DEMANDADO
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] NOMBRE Y APELLIDOS DEL SEGUNDO DEMANDADO
- [ ] NOMBRE Y APELLIDOS DEL VENDEDOR
- [ ] Nº DE COLEGIADO
- [ ] Nº DE PROCEDIMIENTO

## Normas que cita el formulario

- art. 24.1 LEC
- art. 399.1 LEC
- art. 85.1 LOPJ
- art. 45 LEC
- art. 50.1 LEC
- art. 253.1 LEC
- art. 251 LEC
- art. 23 LEC
- art. 399 LEC
- art. 5 Ley Orgánica 1/2025
- art. 1276 CC
- art. 1218 CC
- art. 1275 CC
- art. 633 CC
- art. 1300 Código Civil
- art. 1261 Código Civil
- art. 1275 Código Civil
- art. 633 Código Civil
- art. 394.1 LEC
- art. 723.1 LEC
- art. 733 LEC
- art. 727.5.ª LEC
- art. 42 LH
- art. 73 LH
- art. 721.1 LEC
- art. 726.1.1.ª LEC
- art. 731 LEC
- art. 726.1.2.ª LEC
- art. 728.2 LEC
- art. 728.1 LEC

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

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales y de D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDANTE], con domicilio en [DOMICILIO], representación que acredito mediante escritura de poder otorgada a mi favor (existen tres posibilidades para otorgar el apoderamiento al Procurador de los Tribunales, conforme dispone el art. 24.1 LEC; véase nota 1):

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]
— (Si el poder se otorga a través de la sede judicial electrónica) mediante comparecencia electrónica, a través de la sede judicial electrónica, e inscrito en el Registro Electrónico de Apoderamientos Judiciales; y a cuya justificación acompaño certificación de dicho Registro aportada como Documento n.º [Nº DE DOCUMENTO], y que se puede acreditar mediante consulta automatizada orientada al dato, por parte del órgano judicial al cual tengo el honor de dirigirme.
— (Si el poder se otorga mediante comparecencia apud acta) mediante comparecencia personal apud acta ante el Tribunal de Instancia de [LOCALIDAD], posteriormente inscrito en el Registro Electrónico de Apoderamientos Judiciales; y a cuya justificación acompaño certificación de dicho Registro aportada como Documento n.º [Nº DE DOCUMENTO], y que se puede acreditar mediante consulta automatizada orientada al dato, por parte del órgano judicial al cual tengo el honor de dirigirme.
— (Si el poder se otorga ante Notario) mediante escritura de poder otorgada a mi favor ante el Notario/Notaria [NOMBRE DEL NOTARIO], con Notaría sita en [LOCALIDAD]. El poder se inscribió en el Registro Electrónico de Apoderamientos Judiciales; lo cual justifico mediante certificación de dicho Registro aportada como Documento n.º [Nº DE DOCUMENTO], y que se puede acreditar mediante consulta automatizada orientada al dato, por parte del órgano judicial al cual tengo el honor de dirigirme.

Actúo bajo la dirección letrada de D./Dña. [NOMBRE Y APELLIDOS DEL ABOGADO/A], abogado/a en ejercicio, con despacho profesional abierto en [DOMICILIO PROFESIONAL], colegiado/a n.º [Nº DE COLEGIADO] del Ilustre Colegio de la Abogacía de [LOCALIDAD]. Ante el Tribunal comparezco y, como mejor en Derecho proceda, DIGO (véanse notas 2 y 3):

Que mediante el presente escrito vengo a formular DEMANDA DE JUICIO ORDINARIO contra D./Dña. [NOMBRE Y APELLIDOS DEL PRIMER DEMANDADO] y D./Dña. [NOMBRE Y APELLIDOS DEL SEGUNDO DEMANDADO], con domicilio (véase nota 4), en primer lugar, en [DOMICILIO] y, en segundo lugar, el domicilio laboral en [DOMICILIO LABORAL]; con correo electrónico [CORREO ELECTRÓNICO] (véase nota 5) y con número de teléfono móvil [Nº DE TELÉFONO]; en ejercicio de la acción de nulidad de contrato por simulación absoluta, según se especificará en el cuerpo del escrito y en el suplico, y todo ello de conformidad con los siguientes hechos y fundamentos de derecho.

Que esta parte asume el compromiso de recibir cualquier comunicación dirigida por la oficina judicial, durante toda la fase declarativa e, incluso, en una eventual fase de ejecución por medios telemáticos, en los términos del art. 399.1, párrafo segundo, LEC, consignándose a estos efectos la siguiente dirección de correo electrónico y número de teléfono: [CORREO ELECTRÓNICO] y [Nº DE TELÉFONO].

HECHOS

PRIMERO.– Mi mandante, D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDANTE], ha venido dedicándose a [ACTIVIDAD], remontándose las relaciones comerciales con el demandado D./Dña. [NOMBRE Y APELLIDOS DEL DEUDOR] a [FECHA O PERÍODO].

SEGUNDO.– Como consecuencia de las relaciones comerciales descritas, mantenidas entre mi representado/a y D./Dña. [NOMBRE Y APELLIDOS DEL DEUDOR], este adeuda a mi principal la cantidad de [IMPORTE] euros. El importe total de dicha cantidad resulta de los documentos números [Nº DE DOCUMENTO] acompañados a la presente.

TERCERO.– Habiendo intentado sin éxito una solución amistosa, al objeto de reclamar dicha cantidad, mi mandante envió un requerimiento por conducto notarial al demandado en reclamación de la deuda pendiente, cuya copia asimismo se aporta como documento número [Nº DE DOCUMENTO].

CUARTO.– No obstante el requerimiento formalmente realizado con fecha [FECHA], no atendido por el demandado, antes de reclamar judicialmente, mi mandante propuso, incluso, un acuerdo de aplazamiento de pago no aceptado por el demandado, como es muestra la carta dirigida por el actor y la contestación de D./Dña. [NOMBRE Y APELLIDOS DEL DEUDOR], que se aportan como documentos números [Nº DE DOCUMENTO].

En dicha contestación fue cuando el demandado aseguró a mi mandante que la empresa no iba bien, careciendo en ese momento de liquidez, siendo el único bien el local donde la empresa desarrolla su actividad.

QUINTO.– Finalmente, ante la patente falta de voluntad de pago del demandado, mi mandante promovió proceso para reclamar las cantidades adeudadas, que se tramitó como autos n.º [Nº DE PROCEDIMIENTO] de juicio [CLASE DE JUICIO], dictando sentencia la Sección Civil del Tribunal de Instancia de [SEDE], en la que se condena al deudor al pago a mi mandante de la cantidad de [IMPORTE] euros. Se acompaña como documento número [Nº DE DOCUMENTO] testimonio de la sentencia.

SEXTO.– Con fecha [FECHA], mi mandante ha tenido conocimiento de que el demandado había transferido el local en que estaba instalada la empresa, sito en [DOMICILIO DEL INMUEBLE], al otro codemandado, D./Dña. [NOMBRE Y APELLIDOS DEL COMPRADOR], mediante contrato de compraventa celebrado el [FECHA], siendo el comprador [RELACIÓN DEL COMPRADOR CON EL VENDEDOR, por ejemplo, su hermano], que carece de ingresos estables (como se acreditará en su momento a través de la prueba que esta parte interese) que le permitieran adquirir dicho local, cuyo precio, según se advierte de la certificación del Registro en la que aparece la referencia del título que causa inscripción, aportada como documento número [Nº DE DOCUMENTO], fue de [IMPORTE] euros, cantidad que además no se encuentra en el patrimonio de D./Dña. [NOMBRE Y APELLIDOS DEL DEUDOR].

El precio que se hace figurar no existió pero, en todo caso, es desproporcionadamente bajo, como se consigna en el dictamen pericial designado como documento número [Nº DE DOCUMENTO].

SÉPTIMO.– Resulta palmario que la citada compraventa resultaba ser inexistente y que solo se pretendió con ella transmitir fraudulentamente el local en que estaba instalada la empresa al otro codemandado, para sustraerlo del patrimonio de D./Dña. [NOMBRE Y APELLIDOS DEL DEUDOR] y así eludir sus compromisos económicos con el actor, en concreto la responsabilidad que en el futuro sobre el inmueble debía recaer.

OCTAVO.– La parte actora manifiesta que, previamente a la presentación de la presente demanda, se han llevado a cabo negociaciones con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron conforme a los principios de buena fe, con la intención de alcanzar una solución satisfactoria; incluyéndose entre las acciones realizadas el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución.

Finalmente, mi representado/a envió un requerimiento fehaciente al demandado con fecha [FECHA], fijando un plazo de 30 días naturales para llegar a un acuerdo amistoso, a través del abogado que firma este escrito, el cual fue contestado por el demandado por el mismo medio, [ELEGIR: rechazando el acuerdo / habiendo sido solo posible un acuerdo parcial], viéndonos en la necesidad de acudir a la presente vía judicial respecto a los extremos de la controversia en los que se mantiene la discrepancia.

Acompaño como documento n.º [Nº DE DOCUMENTO] el requerimiento efectuado y como documento n.º [Nº DE DOCUMENTO] la contestación del demandado.

A los anteriores hechos son de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

I.– JURISDICCIÓN Y COMPETENCIA

Radicando la competencia genérica en el orden civil de la jurisdicción, detenta la competencia objetiva y funcional la Sección Civil del Tribunal de Instancia, por aplicación de lo dispuesto en el art. 85.1 LOPJ y el art. 45 LEC, y puesto que no está prevenido un fuero territorial preceptivo específico, con arreglo a lo previsto en el art. 50.1 LEC resulta territorialmente competente el Tribunal a que me dirijo, puesto que es el del partido del lugar donde tiene su domicilio el demandado.

II.– CAPACIDAD Y LEGITIMACIÓN

Tanto mi mandante como los demandados son personas físicas, mayores de edad, en pleno ejercicio de sus derechos civiles, por lo que tienen capacidad para ser parte y capacidad procesal, ex arts. 6.1.1.º y 7.1 LEC.

Corresponde la legitimación activa directa a mi mandante, por cuanto ha acreditado su legítimo interés en la nulidad del contrato en cuestión y se ha visto perjudicado por los efectos del mismo. Así lo entiende la STS de 24 de febrero de 1986: «Según reiterada doctrina jurisprudencial, siendo la simulación absoluta un supuesto de inexistencia contractual, en cuanto es significativo de la falta de consentimiento exigido por el núm. 1.º del art. 1.261 del C. civil, la acción tendente a su declaración compete a toda persona que tenga interés en ella».

En cuanto a la legitimación pasiva, corresponde a todos aquellos que pudieran verse afectados por la resolución que en su día se dicte; en este caso, no solo el vendedor, que trata de desentenderse de la responsabilidad patrimonial, sino también el comprador, que intervino en el negocio simulado que se impugna.

III.– PROCEDIMIENTO

La presente demanda deberá sustanciarse por las normas del juicio ordinario, a tenor de lo prevenido en los arts. 248 y 249.2 LEC, toda vez que el criterio de atribución preferente de la materia objeto del proceso resulta inaplicable, al carecer de especialidad típica la de este, y cumplir entonces el criterio de cuantía, que supera los 15.000 euros.

IV.– CUANTÍA

Cumpliendo lo prevenido en el art. 253.1 LEC, hacemos constar que la cuantía de esta demanda es de [IMPORTE EN LETRA] euros ([IMPORTE EN NÚMERO] €), con arreglo a la regla 3.ª, 2.º, en relación con la regla 2.ª del art. 251 LEC, puesto que el local objeto de la compraventa tiene un valor de mercado de [IMPORTE] euros, lo que acredita mediante el dictamen pericial que se acompaña como documento número [Nº DE DOCUMENTO].

V.– POSTULACIÓN Y DEFENSA

Conforme a los arts. 23 y 31 LEC, se formula esta demanda a través de Procurador/a de los Tribunales con poder para pleitos, y con dirección y firma de Letrado habilitado ante el Tribunal. Asimismo se cumplen los requisitos formales del art. 399 LEC.

VI.– CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4.º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

VII.– FONDO DE LA CUESTIÓN CONTROVERTIDA

De acuerdo con el art. 1276 CC, el contrato de compraventa celebrado entre D./Dña. [NOMBRE Y APELLIDOS DEL VENDEDOR] y D./Dña. [NOMBRE Y APELLIDOS DEL COMPRADOR] es nulo por inexistencia de causa, al existir simulación absoluta, habida cuenta de que, como esta parte acreditará en fase probatoria, no existió pago del precio, no obstante lo manifestado en la escritura pública de compraventa, que, de acuerdo con el art. 1218 CC, solo hace prueba frente a mi mandante del hecho que motivó su otorgamiento, de los intervinientes y de cuáles fueron sus manifestaciones.

El precio que se fijaba en el contrato que causa la última inscripción en la finca cuya vida registral se aporta como documento número [Nº DE DOCUMENTO] de esta demanda, además de extraordinariamente bajo, nunca se pagó. Ello implica falta de causa y, por ende, inexistencia del contrato, ya que no hubo contrato verdadero.

La simulación, que se caracteriza dentro de la disciplina de la causa del negocio, consiste en el vicio del consentimiento que supone discrepancia entre la voluntad real y la declarada, lo cual lleva aparejada la sanción prevenida en los arts. 1275 y 1276 CC y, en consecuencia, imperativa declaración de nulidad (STS de 18 de julio de 1989), al faltar la imprescindible causa, a menos que se acredite, debajo de la aparente, la existencia de otra causa verdadera y lícita.

La compraventa de autos fue un negocio ficticio, cuyo interés exclusivo era ser dicho contrato medio de elusión del pago de las deudas de D./Dña. [NOMBRE Y APELLIDOS DEL DEUDOR] con el actor, y sin que mediara precio real ni efectiva entrega de la posesión del inmueble por el presunto transmitente. En la simulación absoluta no existe propósito negocial alguno, siendo todo una mera apariencia engañosa, urdida con determinada finalidad ajena al negocio que se finge (STS de 19 de julio de 1984), que en el supuesto resulta evidente. En el contrato no aparece la causa que nominalmente se expresa, puesto que responde a otra finalidad jurídica (STS de 1 de julio de 1988), sin que se precise para su apreciación la prueba de una finalidad defraudatoria (STS de 15 de marzo de 1995), aunque aquí es patente el deseo de eludir compromisos económicos, teniendo declarado la jurisprudencia que el negocio con falta de causa es inexistente (STS de 23 de mayo de 1980) y que la falsedad de la causa equivale a su no existencia.

Esta simulación absoluta, que da lugar a un negocio jurídico que carece de causa, es la catalogación de la compraventa en que no ha habido precio, según inveterada doctrina de la Sala Primera del Tribunal Supremo (SSTS de 24 de febrero de 1986, 16 de abril de 1986, 5 de marzo de 1987, 4 de mayo de 1987, 29 de septiembre de 1988, 29 de noviembre de 1989, 1 de octubre de 1990, 1 de octubre de 1991, 24 de octubre de 1992, 7 de febrero de 1994, 24 de mayo de 1995 y 26 de marzo de 1997, rec. 1075/1993).

Para el supuesto hipotético de que se calificara la compraventa como simulación relativa, la cual se percibe cuando el negocio aparente o simulado encubre otro real o disimulado (que sería la donación), colorem habet, substantiam vero alteram, que usualmente solo se ha considerado para donaciones remuneratorias disfrazadas y no las puras, se alega la nulidad radical por defecto de forma ad solemnitatem del art. 633 CC, excepción notoria del espiritualismo del ordenamiento, insubsanable e imprescriptible (SSTS de 3 de marzo de 1995, rec. 3367/1991; 13 de noviembre de 1997, rec. 166/1994, o 19 de junio de 1999, rec. 3129/1994).

Ha de repetirse, como asimismo tiene declarado la jurisprudencia, que son grandes las dificultades que entraña la prueba plena de la simulación de los contratos, por el natural empeño que ponen los contratantes en hacer desaparecer todos los vestigios de la simulación y por aparentar que el contrato es cierto y efectivo reflejo de la realidad, lo cual obligará, como en la práctica totalidad de los casos, a inferir la simulación de la prueba indirecta de las presunciones judiciales (SSTS de 24 de abril de 1984, 13 de octubre de 1987, 26 de abril de 1991, 28 de abril y 29 de julio de 1993), sin que se oponga a la existencia de simulación el hecho de que el contrato se documentara en escritura pública, pues la fe pública notarial no alcanza a la certeza intrínseca de lo que en ella se constata, ni a la intención o propósito de los contratantes (SSTS de 24 de julio de 1992 y 13 de marzo de 1997, rec. 1319/1993).

Un análisis desapasionado y objetivo de los elementos probatorios que obrarán en el juicio, por presencia (evaluación de precio, circunstancias concomitantes) o ausencia (falta de movimiento de numerario o transacción bancaria), conducirá a la conclusión avanzada.

VIII.– En cuanto a la interposición en plazo de la presente demanda, debemos señalar que la acción de nulidad de los contratos ejercitada en el presente procedimiento es imprescriptible (SSTS de 9 de diciembre de 1951, 3 de octubre de 1962, 20 de diciembre de 1975, 19 de mayo y 22 de diciembre de 1981, 15 de febrero de 1982, 13 de febrero y 20 de diciembre de 1985, 6 de junio de 1986, 19 de julio de 1989, entre otras).

La más reciente STS 974/2006, de 28 de septiembre, rec. 4315/1999, es también clara en esta cuestión: «En referencia a la nulidad de los contratos tratada en el artículo 1300 del Código Civil, la Sentencia del Tribunal Supremo de 27 de abril de 1997 declara que tal precepto solo es aplicable a los supuestos en que existe verdadero contrato por reunir los requisitos del artículo 1261 del Código Civil, pero no cuando por simulación absoluta hay inexistencia de causa y total privación de efectos contractuales según el artículo 1275 del Código Civil (Sentencia de 5 de noviembre de 1981). En idéntico sentido se pronuncia la Sentencia de 23 de julio de 1993. La Sentencia del Tribunal Supremo de 28 de mayo de 1996, rec. 2808/1992, también declara que siendo exacto que la jurisprudencia ha permitido en bastantes ocasiones admitir una donación bajo la forma de compraventa, ello ha sido generalmente en supuestos de donaciones remuneratorias, pero no en las puras y simples, para las cuales es rigurosa la jurisprudencia, según la cual para que exista donación han de concurrir los requisitos del artículo 633 del Código Civil, y no cabe entender que hubiera aceptación a la donación cuando no se alega por los demandados, quienes tampoco acreditan ni la causa de la gratuidad ni el "animus donandi". En igual sentido la Sentencia de 13 de noviembre de 1997, rec. 166/1994».

IX.– COSTAS

La parte demandada soportará el reintegro de todas las costas del juicio por el principio cuasiobjetivo de vencimiento del art. 394.1 LEC para declarativos en primera instancia.

Por todo lo expuesto,

SUPLICO AL TRIBUNAL:

que, teniendo por presentado este escrito de demanda junto con los documentos que se acompañan y copias simples de todo ello, se sirva admitirlo a trámite, se me tenga por comparecido/a y parte demandante en el proceso y en la representación que ostento, entendiéndose conmigo las sucesivas diligencias, por promovido el correspondiente juicio ordinario en ejercicio de la acción de nulidad de contrato por falta de causa contra D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS], acordando conferirles traslado de la demanda y documentos con ella presentados, emplazándolos en legal forma y, previos los trámites oportunos, en su día se dicte sentencia por la que se declare la nulidad, por inexistencia derivada de simulación absoluta, del contrato de compraventa en escritura pública relatado en el cuerpo de esta demanda, por tratarse de un negocio jurídico simulado y de exclusiva finalidad ilícita en perjuicio del demandante, decretándose asimismo la cancelación en el Registro de la Propiedad de las inscripciones y anotaciones producidas como consecuencia de la referida compraventa simulada, al ser declarado nulo el título patrimonial en cuya virtud se hicieron, con expresa condena en costas a los demandados.

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

PRIMER OTROSÍ DIGO.– Esta parte solicita la adopción de la MEDIDA CAUTELAR DE ANOTACIÓN PREVENTIVA DE DEMANDA, con fundamento en los siguientes:

HECHOS

ÚNICO.– Se reproducen los hechos y las valoraciones sobre los mismos que se han dejado expresados en el cuerpo de la demanda principal, si bien conviene tener presente, a los efectos de la presente solicitud de medida cautelar de anotación preventiva de demanda, que los demandados han comenzado a realizar gestiones para transmitir de nuevo el inmueble sobre el que versa el proceso, y la adquisición con carácter de irreivindicable por un tercero protegido registralmente haría imposible la tutela efectiva de la sentencia que pudiera recaer.

FUNDAMENTOS DE DERECHO

I.– COMPETENCIA

Conforme al art. 723.1 LEC, corresponde resolver esta petición a la Sección Civil del Tribunal de Instancia al que me dirijo, puesto que el proceso cautelar que se inicia con la demanda del proceso del que resulta instrumental es competencia funcional del órgano competente para conocer del proceso principal, como se ha razonado que lo es.

II.– PROCEDIMIENTO

La solicitud de medida cautelar se sustancia, tratándose de procedimiento ordinario con audiencia del adverso, conforme a los arts. 733 a 738 LEC.

III.– MEDIDA SOLICITADA

Se solicita una medida cautelar resultado de la relación de los arts. 727.5.ª LEC y 42.1 de la Ley Hipotecaria (LH), de anotación preventiva de demanda.

Conforme al art. 727.5.ª LEC, podrá acordarse la medida cautelar de anotación preventiva de demanda cuando esta se refiera a bienes o derechos susceptibles de inscripción en Registros públicos; y el art. 42 LH faculta para pedir anotación preventiva de sus derechos en el Registro de la Propiedad al que demandare en juicio la propiedad de bienes inmuebles o la constitución, declaración, modificación o extinción de cualquier derecho real.

Haciendo uso de la facultad expresada, se solicita la anotación preventiva de esta demanda, debiendo el mandamiento judicial para esta anotación expresar las circunstancias que deba esta contener, según resulten de los títulos y documentos aportados al pleito, a tenor de lo dispuesto en el art. 73 LH.

Justificación: Con objeto de asegurar la efectividad de la tutela judicial que pudiera otorgarse en la sentencia estimatoria que se dictare (art. 721.1 LEC), de modo que no pueda verse impedida o dificultada por situaciones producidas durante la pendencia del proceso correspondiente (art. 726.1.1.ª LEC), hay posibilidad de acordar, respecto de los bienes y derechos de la parte demandada, medidas cautelares, que serán provisionales, instrumentales al proceso iniciado (art. 731 LEC), variables conforme al principio rebus sic stantibus y siempre proporcionadas (art. 726.1.2.ª LEC).

Presupuestos: La cuestión objeto del proceso principal se corresponde con el ejercicio de una acción personal, y no real, por la que se pretende en esencia que se decrete que el contrato de compraventa en escritura pública otorgada ante notario por ambos demandados es nulo de pleno derecho por simulación absoluta o inexistencia de causa, o por ampararse en causa ilícita o reprobable.

Ahora bien, resulta evidente su trascendencia registral, de manera que, según entiende esta parte, nada impide, acreditada más que indiciariamente la apariencia de buen derecho a que se refiere el art. 728.2 LEC, la adopción de esta medida.

En este sentido, el AAP Baleares, Secc. 3.ª, Auto 3/2003, de 10 de enero, rec. 658/2002, declara que «la anotación preventiva de demanda, contemplada como medida cautelar específica en el artículo 727.5.ª de la Ley de Enjuiciamiento Civil cuando se refiera a bienes o derechos susceptibles de inscripción en Registros públicos, tiene, según la jurisprudencia, un doble contenido: el procesal, conforme al cual se asegura que la sentencia que en su día recaiga tendrá la misma eficacia que si hubiera dictado ya en el día en que la anotación se practica, y el contenido sustantivo, a través del cual se consigue la ventaja que proporciona el principio de prioridad registral si el actor obtiene sentencia favorable (STS de 18 de noviembre de 1993, rec. 916/1991). Ahora bien, al venir regulada en la Ley Hipotecaria (artículo 42), las condiciones y procedimiento para poder ser solicitada, acordada e inscrita en el Registro de la Propiedad vienen reguladas en dicha Ley, al decir el artículo citado que "podrán pedir anotación preventiva de sus respectivos derechos en el Registro correspondiente […] el que demandare en juicio la propiedad de bienes inmuebles, o la constitución, declaración, modificación o extinción de cualquier derecho real", dicción literal que limita la anotación preventiva de demanda al ejercicio de una acción real pero, actualmente, superada por la doctrina de la Dirección General de los Registros y del Notariado en el sentido de permitir la anotación preventiva de demanda en ejercicio de acciones de crédito o personales con trascendencia real (RRDGRN de 6 de julio y 29 de septiembre de 1962 y 24 y 25 de junio de 1991, por todas), pero siempre que la sentencia que se dicte sea capaz de producir una inscripción en el Registro público que modifique su contenido, precisamente porque, como señala la doctrina científica, su función es evitar que, mientras se sustancia el proceso, se causen en el propio Registro inscripción o inscripciones contrarias o irreversibles que hagan imposible la inscripción o inscripciones que causaría la ejecución de sentencia».

El periculum in mora (art. 728.1 LEC) viene específicamente propiciado por los efectos de la fe pública registral que ampara a quien asiente el dominio o derecho real sobre el inmueble litigioso que puede haber adquirido durante la pendencia del proceso principal (arts. 32 y 34 LH).

Presupuesto de la ejecución de la medida cautelar (art. 728.3 LEC): se ofrece prestar la caución que al efecto prudencialmente se señale para indemnizar los perjuicios que de la anotación puedan seguirse a los demandados caso de ser absueltos, y que se considera puede ascender a [IMPORTE] euros (teniendo en cuenta el alcance limitado de la anotación preventiva de demanda, alcance que, entre otras, se recoge en la STS de 18 de noviembre de 1993, rec. 916/1991, en la que se señala que la anotación «no produce cierre registral, como ya destacó la Dirección General de los Registros en su resolución de 4-7-1919, puesto que los derechos a que se refiere pueden ser objeto de transmisiones aunque, como se ha dicho, subordinadas al resultado del proceso y efectos de la anotación pendiente»), prefiriéndose la fórmula de aval bancario a primer requerimiento por tiempo indefinido, con las condiciones que fije S.S.ª, oídas las partes.

Prueba: De conformidad con el art. 732.2, párrafo tercero, LEC, se propone la práctica de prueba documental y de interrogatorio de la parte contraria para la acreditación de los presupuestos de la medida cautelar, señalándose como documentos los que acompañan la demanda principal.

En su virtud,

SUPLICO AL TRIBUNAL

que, teniendo por recibida solicitud de medida cautelar, se digne admitirla y se convoque por el Letrado de la Administración de Justicia a las partes para la vista, seguido que sea el oportuno trámite, practicándose la prueba que se propone, dicte Auto por el que se disponga, previa la prestación de la caución por la actora en la cuantía y forma que se señale, la anotación preventiva de la presente demanda, librándose al efecto el correspondiente mandamiento al Registro de la Propiedad de [LOCALIDAD], con entrega a esta parte para su diligenciado, todo ello con imposición de las costas del proceso cautelar a la parte contraria, si se resistiere a la adopción de la medida.

SEGUNDO OTROSÍ DIGO.– Que esta parte ha intentado cumplir con todos los requisitos formales exigidos en la vigente LEC, manifestando su voluntad de subsanar cualquier defecto procesal en el que haya incurrido, a los efectos determinados en el art. 231 LEC.

DE NUEVO SUPLICO AL TRIBUNAL que se sirva tener por hecha la precedente manifestación de intenciones.

Es justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Abogado/a: [FIRMA] Firma del Procurador/a: [FIRMA]

NOTAS DE AYUDA

(1) A la hora de su acreditación, todos los poderes deben estar inscritos en el Registro Electrónico de Apoderamientos Judiciales (REAJ). Se supone que, para su acreditación, basta con la consulta automatizada orientada al dato de dicho Registro, que está a disposición de cualquier Letrado de la Administración de Justicia. Sin embargo, dado que el art. 24.2 LEC configura la certificación de dicha inscripción como vía subsidiaria de acreditación, para el caso de que el sistema no permita aquella consulta automatizada, se señala en el modelo que se acompaña certificación electrónica. El sistema permite emitir dicha certificación a quien inscribe el poder.

(2) Normativa aplicable:
— Código Civil: arts. 633, 1218, 1261, 1275, 1276.
— Ley 1/2000, de 7 de enero, de Enjuiciamiento Civil: arts. 6, 7, 23, 31, 45, 50.1, 231, 248, 249.2, 251, 253, 394, 399 a 436, 721.1, 723.1, 726.1, 727.5.ª, 728, 731, 732.2, 733 a 738.
— Ley Hipotecaria (texto refundido aprobado por Decreto de 8 de febrero de 1946): arts. 32, 34, 42, 73.

(3) Jurisprudencia de interés:
— Tribunal Supremo, Sala Primera, Sentencia 199/2012, de 26 de marzo de 2012, rec. 279/2009.
— Tribunal Supremo, Sala Primera, Sentencia 1394/2006, de 11 de enero de 2007, rec. 5281/1999.
— Tribunal Supremo, Sala Primera, Sentencia 496/2008, de 29 de mayo de 2008, rec. 1048/2001.
— Audiencia Provincial de las Illes Balears, Secc. 3.ª, Auto 3/2003, de 10 de enero de 2003, rec. 658/2002.

(4) El art. 155.3 LEC permite expresar varios domicilios del demandado (el que aparezca en el padrón municipal o conste oficialmente a estos efectos; el que aparezca en un registro oficial o en publicaciones de colegios profesionales, si se trata de empresas o personas colegiadas; donde desarrolle su actividad profesional o laboral no ocasional; si es empresa mercantil, el domicilio de cualquiera de sus administradores, gerentes o apoderados; o, si es asociación que consta en registro oficial, el domicilio del presidente, miembro o gestor de la Junta correspondiente). Cuando se señalen varios, se indicará el orden a seguir para la notificación, con vistas al éxito de la misma.

(5) El art. 155.3 LEC configura una obligación adicional del demandante, consistente en aportar cuantos datos sean de utilidad para localizar al demandado: número de identificación fiscal o de extranjeros, número de teléfono, dirección de correo electrónico o similares.
