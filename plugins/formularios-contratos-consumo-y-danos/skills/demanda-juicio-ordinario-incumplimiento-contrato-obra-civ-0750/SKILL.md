---
name: demanda-juicio-ordinario-incumplimiento-contrato-obra-civ-0750
description: "Demanda de juicio ordinario por incumplimiento de un contrato de obra a precio alzado. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio ordinario por incumplimiento de un contrato de obra a precio alzado

> Formulario **CIV-0750** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio ordinario ejercitando acción personal sobre incumplimiento de contrato de arrendamiento de obra por precio alzado con suministro de materiales.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio ordinario por incumplimiento de un contrato de obra a precio alzado» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio ordinario por incumplimiento de un contrato de obra a precio alzado” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:demanda-juicio-ordinario-incumplimiento-contrato-obra-civ-0750`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (7 veces)
- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] NÚMERO (6 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] DOMICILIO (2 veces)
- [ ] FECHA (2 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] CORREO ELECTRÓNICO
- [ ] DESCRIBIR
- [ ] LUGAR
- [ ] Nº
- [ ] Nº DE COLEGIADO/A
- [ ] SEDE
- [ ] TELÉFONO

## Normas que cita el formulario

- art. 24.1 LEC
- art. 399.1 LEC
- art. 21 LOPJ
- art. 85.1 LOPJ
- art. 50 LEC
- art. 10 LEC
- art. 23 LEC
- art. 5 Ley Orgánica 1/2025
- art. 1542 CC
- art. 1101 CC
- art. 1103 CC
- art. 253.1 LEC
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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] Q.P.T.R.C.»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Notas al pie del formulario original:
(1) A la hora de su acreditación, todos los poderes deben estar inscritos en el Registro Electrónico de Apoderamientos Judiciales (REAJ). Se supone que, para su acreditación, basta con la consulta (de dicho Registro) automatizada orientada al dato. Algo que está a disposición de cualquier Letrado de la Administración de Justicia. Sin embargo, dado que el art. 24.2 LEC, configura la certificación de dicha inscripción como vía subsidiaria de acreditación, para el caso de que el sistema no permita aquella consulta automatizada; se señala en el modelo que se acompaña certificación electrónica. El sistema permite emitir dicha certificación para quien inscribe el poder.

(2) El art. 155.3 LEC permite fijar expresar varios domicilios del demandado (el que aparezca en el padrón municipal o conste oficialmente a estos efectos; el que aparezca en Registro oficial o en publicaciones de colegios profesionales, si se trata de empresas o personas colegiadas; donde desarrolle su actividad profesional o laboral no ocasional; si es empresa mercantil, el domicilio de cualquiera de sus administradores, gerentes, o apoderados; o, si es asociación que consta en registro oficial; el domicilio del presidente, miembro o gestor de la Junta correspondiente). Cuando se señalen varios, indicará el orden a seguir para la notificación, con vistas al éxito de la misma.

(3) El art. 155.3 LEC configura una obligación adicional del demandante, consistente en aportar cuantos datos sean de utilidad para localizar al demandado: número de identificación fiscal o de extranjeros, nº [Nº] de teléfono o de fax, dirección de correo electrónico, o similares.

========================================================================

[NOTA DE REVISIÓN: requisito de procedibilidad del art. 5 LO 1/2025 — antes de presentar la demanda hay que intentar un medio adecuado de solución de controversias (MASC) y acreditarlo con la demanda (arts. 264.4.º y 399.3 LEC), salvo las materias excluidas del art. 5.2. Fuente: LO 1/2025, arts. 5 a 7 (BOE-A-2025-76).]


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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] Q.P.T.R.C.

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales y de D./Dña. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], representación que acredito mediante escritura de poder otorgada a mi favor (existen tres posibilidades para otorgar el apoderamiento al Procurador de los Tribunales, conforme dispone el art. 24.1 LEC)

[OPCIONAL — opción en función de cómo se haya otorgado el poder]

[ELEGIR UNA OPCIÓN: Si el poder se otorga a través de la sede judicial electrónica / Si el poder se otorga mediante comparecencia apud acta / Si el poder se otorga ante Notario]

bajo la dirección letrada de D./Dña. [NOMBRE Y APELLIDOS], abogado/a en ejercicio, con despacho profesional abierto en [LOCALIDAD], colegiado nº [Nº DE COLEGIADO/A] del Ilustre Colegio de la Abogacía de [LOCALIDAD], ante el Tribunal comparezco y como mejor en Derecho proceda, DIGO:

Que mediante el presente escrito vengo a formular DEMANDA DE JUICIO ORDIANRIO EN RECLAMACIÓN DE CANTIDAD [IMPORTE], contra D./Dña. [NOMBRE Y APELLIDOS], con domicilio, primero en [DOMICILIO]; y segundo, el domicilio laboral en [DOMICILIO]); con email [CORREO ELECTRÓNICO]; y con número de teléfono móvil [TELÉFONO]; todo ello de conformidad con los hechos y fundamentos de derecho que se especificarán.

Que esta parte asume el compromiso de recibir cualquier comunicación dirigida por la oficina judicial, durante toda la fase declarativa, e, incluso, en una eventual fase de ejecución por medios telemáticos, en términos del art. 399.1 II LEC, consignándose a estos efectos la siguiente dirección de correo electrónico y nº [Nº] de teléfono:

HECHOS

PRIMERO.- Mi mandante contrató con el demandado, que gira en el tráfico mercantil bajo la denominación " ", la reparación del tejado de la vivienda de su propiedad sita en

Se acompaña copia del referido contrato como documento n.º [NÚMERO], y factura acreditativa del pago de la reparación como documento n.º [NÚMERO]

SEGUNDO.- La incorrecta ejecución de la obra dio lugar a que, al poco tiempo, apareciesen filtraciones y humedades cada vez más graves, hasta el punto de que la obra realizada no sirve al objeto de la obra contratada, esto es la impermeabilización, y así siguen existiendo penetraciones de agua desde el exterior a la vivienda propiedad del actor (documento n.º [NÚMERO]), anomalías de las que ha tenido constante conocimiento el demandado (documentos números [Nº DE DOCUMENTO] y [Nº DE DOCUMENTO]).

TERCERO.- Se han intentado varias gestiones amistosas con el demandado, consistentes en [DESCRIBIR], siendo totalmente incumplidas las promesas de aquél, intentándose por esta parte actora llegar a un acuerdo para evitar el acudir a los Tribunales, conforme a la propuesta que le fue enviada por burofax de [FECHA], que no ha tenido contestación hasta la fecha (documento n.º [NÚMERO]) de modo que no ha quedado otra solución a mi mandante que ejercitar la oportuna acción en defensa de sus derechos.

FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN Y COMPETENCIA.

Los arts. 21 LOPJ y 36 LEC atribuyen con carácter general a la jurisdicción de nuestro Estado y al orden civil, el conocimiento de una materia como la presente.

Los arts. 85.1º LOPJ y 45 LEC, designan a los Tribunales de Instancia, como los órganos con la competencia específica objetiva y funcional para resolver estos pleitos.

Finalmente, el art. 50 LEC fija que la competencia territorial general, en el caso de personas físicas, será del órgano del lugar de su domicilio.

II.- TRAMITACIÓN.

En aplicación de los arts. 248.3, 249.2 y 251 LEC, y en atención a la cuantía reclamada que asciende a [IMPORTE] euros ( [IMPORTE] €), este pleito se tramitará por las normas de proceso declarativo llamado Juicio Ordinario.

III.- LEGITIMACIÓN, CAPACIDAD Y POSTULACIÓN.

El art. 10 LEC legitima para comparecer y actuar en juicio a los titulares de la relación jurídica o del objeto litigioso. En el caso de autos, actor y demandado se encuentran legitimadas activa y pasivamente para interponer y soportar la presente demanda, habida cuenta que por mi mandante se está ejercitando una acción personal derivada de la relación de arrendamiento de obra con suministro de materiales concertada. Ambas partes son mayores de edad y se encuentran en situación de pleno ejercicio de sus derechos civiles, en virtud de lo dispuesto en los arts. 6.1.1.º y 7.1 LEC.

En aplicación de los arts. 23 y 31 LEC, las partes comparecerán representadas por Procurador/a de los Tribunales y asistidas por Letrado en ejercicio, ambos habilitados ante el Tribunal.

IV.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

V.- FONDO DEL ASUNTO.

Se ejercita en esta demanda acción personal por incumplimiento de contrato de ejecución de obras, solicitando la cantidad de [IMPORTE] euros, importe al que alcanza el valor de las reparaciones a efectuar.

El contrato suscrito entre las partes conforma un arrendamiento de obra por precio alzado, con suministro de materiales, de los arts. 1542, 1544 y 1588 CCiv, cuyo concreto contenido, en cuanto a los elementos esenciales de la relación, el objeto y el precio, resulta del contrato y de la factura aportada, que pacíficamente abonó el actor y reconoce el demandado, asumiendo así la obra. De dicha factura resulta evidente que la reparación contratada en cuanto afectaba al tejado comprendía levantar teja, desescombrar, colocar onduline, teja nueva en los ríos y vieja de tapa.

Sobre esa base la habilidad de la obra contratada indudablemente comprendía la impermeabilización del tejado en su integridad, pues una de las misiones fundamentales de este elemento constructivo es precisamente impedir la entrada de aguas pluviales en el edificio. Para ello debe tejerse conforme a las normas constructivas un adecuado entramado de elementos impermeables y que canalicen debidamente las aguas para su evacuación.

Desde luego y a los efectos del presente pleito no puede deducirse que por la falta de una mención expresa no se comprenda en lo que realmente supone una restauración de los elementos impermeables del tejado (onduline y teja) el debido remate de los encuentros del onduline y teja con los paramentos que conforman el palomar, txoritoki o mansardas, pues ello equivaldría a estimar la posibilidad de contratar la reforma y sustitución de la cubierta, pero asumiendo que después resten vías de filtración de aguas en esos puntos críticos. Algo absurdo y fuera de toda lógica. Una cosa es contratar una mayor o menor calidad de materiales y otra muy distinta es cumplir un mínimo requerimiento técnico del elemento constructivo afectado por la obra. Si se contrata la reforma y sustitución de la cubierta con onduline y teja, indudablemente, además del adecuado ensamblaje de esos elementos, se contrata el correcto acabado y remate de todo ello, de tal suerte que no se filtre el agua, que en definitiva es la finalidad inmediata del elemento reparado o sustituido.

Sobre esta primera consideración y perfilado el objeto del contrato, en cuanto afecta a la cubierta, las deficiencias de que adolece el trabajo ejecutado se constatan con rotundidad en el informe pericial del Sr./a. que se acompaña como documento n.º [NÚMERO], quien examina el tejado y confirma la existencia de cuatro goteras cuyo origen en dos de ellas es la mala ejecución del encuentro entre los faldones del tejado y los palomares, mientras las otras dos lo tienen en la existencia de grietas por el mal anclaje de la antena de televisión y acometida del cable. Considera que el onduline hasta Donde comprobó está bien colocado, aunque la unión con los faldones no está bien ejecutada y la colocación de tela asfáltica no resuelve adecuadamente ese encuentro. Del mismo modo considera que los daños en el interior de la vivienda están directamente relacionados con las referidas goteras.

Con tal informe, debe concluirse que efectivamente el punto de incumplimiento contractual y deficiente aplicación de la lex artis, propia de la profesión del demandado, se contrae a los referidos remates, incluidos los de la antena y cables, que se revelan causantes de las filtraciones de agua y consecuentes daños en el interior.

Por esa razón el alcance de la responsabilidad en los términos del incumplimiento contractual que justifica la reclamación, sobre la base del art. 1101 CCiv, dada la naturaleza del contrato de obras cuya esencia obligacional impone al contratista el cumplimiento de la obra como un resultado eficaz en su destino y finalidad. Si se contrata la práctica renovación del tejado, es evidente, como ha quedado ya expuesto, que se persigue la eliminación y subsanación de deficiencias del mismo y la consecución de un elemento constructivo capaz de cumplir su misión y evitar la entrada de aguas.

Es razonable distinguir entre esa habilidad y cumplimiento de los requerimientos mínimos que la finalidad de la obra exigían y la imposición de mejoras más allá de lo efectivamente contratado. Sin embargo, en el supuesto de autos la solución regeneradora de las deficiencias en el encuentro del tejado y palomeras no se acredita mínimamente garantizada mediante solución distinta de la propuesta por el perito Sr./a. y por ello esa debe ser la referencia indemnizatoria, reparadora del incumplimiento. Incluida la que resulta de las goteras causadas en la base de la antena y acometida del cable, pues del mismo modo tales remates deben entenderse incluidos en el contenido obligacional, en cuanto su inadecuado estado o remate debió prevenirse en la integridad de la impermeabilización de la cubierta.

Modulada la diligencia exigible al demandado en los términos propios de la profesión y por ello deducida la responsabilidad resultante de la falta de cumplimiento de ese deber, pues omitió la diligencia que exigía la propia naturaleza de la obligación asumida en el contrato, debe responder de los daños causados conforme a lo dispuesto en los arts. 1103, 1104 y 1107 CCiv.

VI.- CUANTÍA.

Por así disponerlo el art. 253.1 LEC, se pone de manifiesto que la cuantía de esta demanda es de [IMPORTE] euros ( [IMPORTE] €), con arreglo a la regla 1.ª del art. 251 de dicha Ley, al reclamarse una cantidad de dinero determinada.

VII.- COSTAS.

En aplicación del art. 394.1 LEC deberán imponerse las costas a la parte demandada.

Por lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito con los documentos que acompaño y copias de todo ello, acuerde admitir a trámite la presente demanda, teniendo a quien comparece por parte, con la que se entenderán todas las ulteriores sucesivas diligencias, y dar traslado de la misma a la demandada, y seguido que sea el regular procedimiento, se dicte sentencia por la que se condene a D./Dña. [NOMBRE Y APELLIDOS] a abonar a mi representado la cantidad de [IMPORTE] euros, más lo que representen los intereses de mora desde la fecha de la interposición de la demanda, y con expresa imposición de costas al demandado.

Es justicia que pido en [LUGAR], a [FECHA].

OTROSÍ DIGO: Se acompaña a la demanda informe pericial (documento n.º [NÚMERO]) elaborado por el arquitecto técnico D./Dña. [NOMBRE Y APELLIDOS], cuya declaración en juicio se propone en este acto a los efectos correspondientes.

SUPLICO AL TRIBUNAL que, teniendo por causada la antecedente manifestación, se digne admitirla, y proveer lo conducente, en Justicia que reitero en lugar y fecha "ut supra".

Firma del Abogado/a	Firma del Procurador/a
