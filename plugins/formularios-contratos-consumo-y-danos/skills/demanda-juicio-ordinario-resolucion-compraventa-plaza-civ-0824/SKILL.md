---
name: demanda-juicio-ordinario-resolucion-compraventa-plaza-civ-0824
description: "Demanda de juicio ordinario de resolución de compraventa de plaza de garaje por incumplimiento. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio ordinario de resolución de compraventa de plaza de garaje por incumplimiento

> Formulario **CIV-0824** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio ordinario en ejercicio de la acción resolutoria (arts. 1124 y 1101 CC) de un contrato de compraventa de plaza de garaje por incumplimiento del vendedor (entrega de cosa inhábil para su fin, «aliud pro alio»), con devolución de las cantidades entregadas como precio y de los gastos soportados.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio ordinario de resolución de compraventa de plaza de garaje por incumplimiento» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio ordinario de resolución de compraventa de plaza de garaje por incumplimiento” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:demanda-juicio-ordinario-resolucion-compraventa-plaza-civ-0824`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº DE DOCUMENTO (6 veces)
- [ ] IMPORTE (5 veces)
- [ ] DENOMINACIÓN SOCIAL DE LA VENDEDORA (3 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] NOMBRE Y APELLIDOS DEL DEMANDANTE (3 veces)
- [ ] AÑO (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] DÍA (2 veces)
- [ ] MES (2 veces)
- [ ] NOMBRE DEL NOTARIO (2 veces)
- [ ] Nº DE PROTOCOLO (2 veces)
- [ ] SUPERFICIE (2 veces)
- [ ] SUPERFICIE REAL (2 veces)
- [ ] COLEGIO
- [ ] CORREO ELECTRÓNICO
- [ ] DATOS REGISTRALES
- [ ] DENOMINACIÓN SOCIAL
- [ ] DIRECCIÓN DEL INMUEBLE
- [ ] NOMBRE Y APELLIDOS DEL LETRADO/A
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] Nº DE COLEGIADO
- [ ] Nº DE DOCUMENTOS
- [ ] Nº DE PLAZA
- [ ] SEDE
- [ ] TELÉFONO

## Normas que cita el formulario

- art. 24.1 LEC
- art. 24.2 LEC
- art. 399.1 LEC
- art. 21 LOPJ
- art. 36 LEC
- art. 9.2 LOPJ
- art. 85.1 LOPJ
- art. 45 LEC
- art. 68 LEC
- art. 51.1 LEC
- art. 7.1 LEC
- art. 10 LEC
- art. 399 LEC
- art. 403.3 LEC
- art. 253.1 LEC
- art. 251.1.ª LEC
- art. 5 Ley Orgánica 1/2025
- art. 1124 CC
- art. 1101 CC
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

### Avisos de actualización (4) — se aplican en el texto, nunca se copian en el documento

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…ido o deban cumplirse en España (art. 22 de la Ley Orgánica del Poder Judicial).»: el original citaba el art. 22.3 LOPJ; comprobar el artículo equivalente en la redacción vigente de los arts. 22 ter y siguientes LOPJ para la competencia internacional en materia de obligaciones contractuales.
- Junto a «…sal, y éstas constituidas legalmente, a través de sus representantes necesarios.»: el original aludía a «no incapacitadas»; adaptado a la terminología de la Ley 8/2021. Comprobar la redacción vigente del art. 7 LEC.
- Junto a «…s declarativos previstas en el título I de dicho libro (arts. 248 y siguientes).»: comprobar el umbral de cuantía vigente para el juicio verbal y el ordinario conforme a la redacción actual de los arts. 249 y 250 LEC.

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales y de D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDANTE], con domicilio en [DOMICILIO], representación que acredito mediante:

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]
— poder otorgado a mi favor a través de la sede judicial electrónica (inscrito en el Registro Electrónico de Apoderamientos Judiciales), cuya certificación acompaño como documento n.º [Nº DE DOCUMENTO];
— poder otorgado mediante comparecencia apud acta ante el Letrado de la Administración de Justicia, inscrito en el Registro Electrónico de Apoderamientos Judiciales, cuya certificación acompaño como documento n.º [Nº DE DOCUMENTO];
— escritura de poder otorgada a mi favor ante el Notario D./Dña. [NOMBRE DEL NOTARIO], con n.º de protocolo [Nº DE PROTOCOLO], inscrita en el Registro Electrónico de Apoderamientos Judiciales, cuya certificación acompaño como documento n.º [Nº DE DOCUMENTO];

(Existen tres posibilidades para otorgar el apoderamiento al Procurador de los Tribunales, conforme dispone el art. 24.1 LEC. Todos los poderes deben estar inscritos en el Registro Electrónico de Apoderamientos Judiciales para su acreditación; basta, en principio, la consulta automatizada del Registro por el Letrado de la Administración de Justicia, y la certificación de la inscripción es la vía subsidiaria del art. 24.2 LEC, por lo que el modelo acompaña la certificación electrónica.)

bajo la dirección letrada de D./Dña. [NOMBRE Y APELLIDOS DEL LETRADO/A], abogado/a en ejercicio, con despacho profesional abierto en [LOCALIDAD], colegiado/a n.º [Nº DE COLEGIADO] del Ilustre Colegio de la Abogacía de [COLEGIO], ante el Tribunal comparezco y, como mejor en Derecho proceda, DIGO:

Que mediante el presente escrito vengo a formular DEMANDA DE JUICIO ORDINARIO contra la mercantil [DENOMINACIÓN SOCIAL DE LA VENDEDORA], para ser citada en su oficina de [DOMICILIO], en ejercicio de la acción que se concretará en el cuerpo del escrito y en el suplico, y todo ello de conformidad con los siguientes hechos y fundamentos de Derecho.

Que esta parte asume el compromiso de recibir cualquier comunicación dirigida por la oficina judicial, durante toda la fase declarativa e, incluso, en una eventual fase de ejecución por medios telemáticos, en términos del art. 399.1, párrafo segundo, LEC, consignándose a estos efectos la siguiente dirección de correo electrónico y número de teléfono: [CORREO ELECTRÓNICO] / [TELÉFONO].

HECHOS

PRIMERO.– Con fecha [DÍA] de [MES] de [AÑO], D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDANTE], como parte compradora, y la mercantil [DENOMINACIÓN SOCIAL DE LA VENDEDORA], como parte vendedora, celebraron contrato de compraventa de la plaza de garaje n.º [Nº DE PLAZA], sita en [DIRECCIÓN DEL INMUEBLE], inscrita en el Registro de la Propiedad de [LOCALIDAD], finca registral n.º [DATOS REGISTRALES], por el precio de [IMPORTE] euros, [ELEGIR: elevado a escritura pública ante el Notario D./Dña. [NOMBRE DEL NOTARIO], con n.º de protocolo [Nº DE PROTOCOLO] / formalizado en documento privado]. Se aporta como documento n.º [Nº DE DOCUMENTO].

SEGUNDO.– La parte compradora ha abonado a la vendedora la totalidad del precio pactado, [IMPORTE] euros, además de los gastos notariales, fiscales y registrales por importe de [IMPORTE] euros, según justificantes que se aportan como documentos n.os [Nº DE DOCUMENTOS].

TERCERO.– Conforme a lo estipulado entre las partes, la plaza de garaje debía tener [SUPERFICIE] metros cuadrados útiles. Una vez recibida la plaza, se comprobó que en realidad solo mide [SUPERFICIE REAL] metros cuadrados, por lo que no es apta para albergar convenientemente un vehículo medio, uso para el que fue vendida, sino únicamente motocicletas o bicicletas, según resulta del informe técnico que se aporta como documento n.º [Nº DE DOCUMENTO].

CUARTO.– [REQUERIMIENTOS Y GESTIONES PREVIAS A LA VENDEDORA PARA LA SUBSANACIÓN O RESOLUCIÓN, CON SUS FECHAS Y RESPUESTA, SI LAS HUBO.]

QUINTO.– [GESTIONES NEGOCIADORAS PREVIAS PARA CUMPLIR EL REQUISITO DE PROCEDIBILIDAD: medio adecuado de solución de controversias utilizado, fecha y resultado, con el documento que lo acredita (documento n.º [Nº DE DOCUMENTO]).]

A los anteriores hechos son de aplicación los siguientes,

FUNDAMENTOS DE DERECHO

I.– JURISDICCIÓN Y COMPETENCIA.

Con arreglo a los preceptos que se contienen en el art. 117 de la Constitución, el art. 21 LOPJ y el art. 36 LEC, la jurisdicción ordinaria del Reino de España es la única competente para conocer de los negocios o demandas civiles que se susciten en territorio español entre españoles, además de que los órganos jurisdiccionales españoles son competentes, en materia de obligaciones contractuales, cuando éstas hayan nacido o deban cumplirse en España (art. 22 de la Ley Orgánica del Poder Judicial).

El conocimiento del litigio pertenece a la materia del orden jurisdiccional civil (art. 9.2 LOPJ), y le corresponde la competencia objetiva a las secciones civiles de los tribunales de instancia, en cuanto por disposición legal expresa no viene atribuido a otros tribunales (art. 85.1 LOPJ y art. 45 LEC).

Corresponde el conocimiento del juicio al Tribunal de Instancia que por reparto corresponda (art. 68 LEC) de los de esta ciudad, al que me dirijo en aplicación del art. 51.1 LEC, por ser el lugar del domicilio de la entidad demandada, [DENOMINACIÓN SOCIAL], amén de que aquí nació la relación jurídica entre las partes.

II.– CAPACIDAD.

Conforme a los arts. 6.1.1.º y 3.º LEC, tienen capacidad para ser parte las personas físicas y las jurídicas, y a tenor de los arts. 7.1 y 4 LEC, detentan capacidad de obrar procesal aquéllas mayores de edad que no precisen medidas de apoyo para el ejercicio de su capacidad jurídica en el ámbito procesal, y éstas constituidas legalmente, a través de sus representantes necesarios.

III.– LEGITIMACIÓN.

El art. 10 LEC legitima para comparecer y actuar en juicio a los titulares de la relación jurídica o del objeto litigioso. En el caso de autos, demandante y demandada son los sujetos titulares del contrato cuyo incumplimiento fundamenta la acción resolutoria que se ejerce, existiendo, pues, legitimación directa ordinaria. La legitimación activa de mi representado/a resulta indiscutible en su calidad de comprador/a y corresponde la pasiva a la demandada como parte vendedora de dicho contrato.

IV.– PROCEDIMIENTO.

El interés económico de la demanda supera la suma de 15.000 euros, por lo que, al no tener la presente contienda una tramitación especial «ratione materiae», será de aplicación lo dispuesto en los arts. 248.3, 249.2 y 254.1 LEC, debiendo ventilarse por el juicio ordinario, regulado en el título II del libro II LEC (arts. 399 y siguientes), debiendo asimismo secundarse las disposiciones comunes a los procesos declarativos previstas en el título I de dicho libro (arts. 248 y siguientes).

V.– POSTULACIÓN Y DEFENSA.

Se cumplen las normas de postulación procesal, ya que la demanda se presenta por medio de Procurador/a legalmente habilitado/a para actuar ante los tribunales de este partido, y bajo la dirección de Letrado en ejercicio que redacta y firma, conforme a lo dispuesto en los arts. 23.1 y 31.1 LEC.

VI.– REQUISITOS FORMALES.

Se inicia el proceso por medio de demanda que reúne todos los requisitos exigidos en el art. 399 LEC, sin que existan otras exigencias especiales de procedibilidad, y no estando prevista legalmente una acreditación preliminar de la legitimación o principio de prueba del derecho, por lo que, competente el tribunal, deberá aquélla admitirse, a tenor de los arts. 403.3 y 404 LEC.

VII.– CUANTÍA.

Cumpliendo la exigencia del art. 253.1 LEC, se cifra la cuantía de la demanda en la cantidad de [IMPORTE] euros, que integra la cantidad líquida reclamada conforme al art. 251.1.ª LEC.

VIII.– CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4.º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

IX.– FUNDAMENTO MATERIAL DE LA TUTELA.

Se ejercita la acción resolutoria del art. 1124 CCiv, en relación con el art. 1101 de dicho texto legal.

Estamos en presencia de un caso de entrega de cosa distinta por inadecuada («aliud pro alio») a causa de un cumplimiento anómalo, por haber sido vendido un objeto que resulta, al menos, inhábil para el objetivo o fin propuesto en la compraventa. El «aliud pro alio», consagrado en nuestra jurisprudencia como figura autónoma, permite acudir a la protección que dispensan los citados preceptos.

Con un criterio funcional, se ha de relacionar la figura del «aliud pro alio» con la inadecuación (con el no servir) de la cosa entregada para el fin o uso que determinó su adquisición. El vendedor ha de entregar la cosa con las condiciones precisas para que pueda ser utilizada según su destino, lo que se pone en conexión con una noción de la prestación amplia que alcanza a las cualidades de la cosa que debían entenderse garantizadas por ser precisas para la finalidad o empleo a que se iba a destinar aquélla, que el vendedor conocía en este caso perfectamente.

Con carácter general, destaca la doctrina jurisprudencial que el incumplimiento contractual por prestación diversa a la acordada tiene lugar cuando se da la inhabilidad del objeto y consiguiente insatisfacción total del comprador, que posibilita la sanción de los arts. 1101 y 1124 CCiv (STS de 17 de febrero de 1994). Así, la STS de 5 de noviembre de 1993 sostiene que habría de definir la existencia de la pretensión diversa como la entrega de una cosa distinta a la pactada, y como el incumplimiento por inhabilidad del objeto, o por insatisfacción del comprador.

En el caso de autos, estamos claramente ante un supuesto que la jurisprudencia califica de «aliud pro alio», en el que se entiende que se ha verificado un completo incumplimiento de la obligación de entrega de la cosa por parte del vendedor, al entender que el defecto de que adolece la cosa afecta enteramente a su sustancia, es decir, a sus cualidades esenciales, que la hacen inservible para cumplir el objeto y la finalidad para la que fue adquirida. El vendedor hace entrega de cosa esencialmente diversa con respecto a las condiciones que fueron pactadas, de tal modo que la cosa pasa a ser absolutamente inservible; circunstancia ante la cual la jurisprudencia otorga la consecuencia jurídica de resolución del contrato, ex art. 1124 CCiv.

Nos encontramos con que la plaza de garaje litigiosa no es apta para albergar convenientemente un vehículo medio (uso para el que fue vendida), pues solo caben motos o bicicletas, debiendo tener, conforme a lo estipulado entre las partes, [SUPERFICIE] metros cuadrados útiles y en realidad solo mide [SUPERFICIE REAL] metros cuadrados, por lo que el incumplimiento de la demandada resulta patente.

Ahora bien, la entidad demandada incumplió no solo con su obligación de entregar una plaza de aparcamiento acorde con las previsiones contractuales de medida, sino también con las características que naturalmente han de tener a fin de poder ser utilizada para el fin que le es propio. Pero es que, además, al margen de cualquier estipulación que pudiera contener el contrato (que aquí las contiene), resulta que, como dice la STS de 24 de septiembre de 1986, la plaza de garaje deberá entenderse que ha de ser apta para albergar automóviles de tipo medio, o un vehículo de tipo medio o normal, dice la citada resolución, por lo que, cuando esto no se cumple, es obvio que habrá de entenderse incumplida la obligación de entrega de la cosa; incluso la STS de 15 de julio de 1987 indica que en el concepto jurídico que ha de darse a la expresión «plaza de garaje» va implícito no solo la existencia de un espacio para el estacionamiento, sino también la de otro para aparcar con holgura, sin necesidad de molestas maniobras de marcha atrás y adelante, más un acceso al local adecuado.

Es clara y reiterada la jurisprudencia del Tribunal Supremo en materia de compraventa de plazas de garaje; por todas, la STS de 16 de marzo de 1995, rec. 3515/1991, que declara que «es esencial la adecuación que las plazas han de reunir respecto al fin que les es propio y para el que se adquirieron, lo que comprende tanto las dimensiones necesarias para hacerlas aptas de albergue de automóviles de uso ordinario, como los elementos superficiales accesorios que permitan las maniobras adecuadas y suficientes de los mismos dentro de los locales, lo que comporta la obligación de entregar apto el inmueble y a la plena utilidad del comprador, para permitir el uso normal de las plazas adjudicadas. En razón a ello se estima situación de incumplimiento contractual cuando el espacio no se ajusta, en dimensiones, accesos y conveniente uso, a lo previsto negocialmente»; los compradores «no están en las condiciones de utilizar "civilitas" lo que compraron, por tratarse de prestación distinta, que comporta la inhabilidad de su destino».

Sentado lo cual, y aquilatando la doctrina acuñada por el Alto Tribunal en lo que concierne a la obligación de entrega que compete al vendedor (SSTS de 8 de febrero de 2003, rec. 1875/1997, o de 10 de junio de 2013, rec. 1652/2010), la desviación en la utilidad de la plaza enajenada ha de ser evaluada en el contexto del incumplimiento del contrato, ya que nos encontramos en presencia de la entrega de cosa diversa o «aliud pro alio» que conlleva la frustración plena de la finalidad perseguida por el contrato en cuestión, y ello al detectarse un incumplimiento total y absoluto por la inhabilidad del objeto para reportar al adquirente aquella utilidad que motivó su adquisición, con la consiguiente insatisfacción del interés de los compradores, con lo cual dicho supuesto se enmarca de lleno en el régimen de las previsiones establecidas en los arts. 1101 y 1124 CCiv, y ello no puede ser de otra manera toda vez que nos hallamos ante una situación de entrega de cosa distinta de la pactada, existiendo un íntegro incumplimiento por inhabilidad o ineptitud del objeto vendido, que resulta objetivamente inadecuado para el fin convenido por las partes al concertar el contrato de compraventa de su razón, máxime cuando la conformación material exhibida en el momento actual por el bien raíz litigioso implica la evidencia de un óbice sustancial e insoslayable al regular disfrute del objeto vendido, precisamente en función de la peculiaridad del mismo, que requiere unas condiciones de idoneidad y aptitud que permitan el estacionamiento cotidiano y normalizado del automóvil ocupante de la precitada plaza de aparcamiento.

X.– COSTAS.

Las costas del presente proceso deberán ser impuestas a la parte demandada, en la medida en que deben resultar estimadas la totalidad de nuestras pretensiones, conforme al principio del vencimiento que destaca el art. 394.1 LEC en lo que respecta a los juicios declarativos en su primera instancia.

En atención a todo lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito de demanda junto con los documentos que se acompañan y copias simples de todo ello, se sirva admitir uno y otros, se me tenga por comparecido/a y parte, en la representación que ostento y con carácter de demandante, entendiéndose conmigo las ulteriores sucesivas diligencias, y por promovido juicio ordinario contra [DENOMINACIÓN SOCIAL DE LA VENDEDORA], se le confiera traslado emplazándole en legal forma de comparecencia y eventual contestación y, seguido que sea el oportuno procedimiento, en su día se dicte sentencia en la que se declare resuelto el contrato de compraventa estipulado entre la parte actora y la demandada respecto del bien inmueble que se determina en el escrito de demanda, y la obligación de ésta de devolver a D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDANTE] las cantidades entregadas en concepto de precio de venta, así como de abonarle los gastos notariales, fiscales y registrales soportados, por importe todo ello de [IMPORTE] euros, más los intereses legales desde la interpelación judicial.

En todo caso, se pronuncie el reintegro de las costas con cargo a la parte demandada.

Es justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Abogado/a Firma del Procurador/a
