---
name: demanda-danos-perjuicios-franquiciado-tras-resolucion-civ-0693
description: "Demanda de daños y perjuicios del franquiciado tras la resolución del contrato de franquicia. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de daños y perjuicios del franquiciado tras la resolución del contrato de franquicia

> Formulario **CIV-0693** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio declarativo ordinario por la que el franquiciado, tras la resolución unilateral e injustificada del contrato de franquicia por el franquiciador antes del vencimiento del plazo pactado, reclama una indemnización de daños y perjuicios que comprende el lucro cesante, los gastos no amortizados (parte proporcional del canon de entrada) y la indemnización por clientela. Formulario adaptado a la reforma procesal de la LO 1/2025.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de daños y perjuicios del franquiciado tras la resolución del contrato de franquicia» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de daños y perjuicios del franquiciado tras la resolución del contrato de franquicia” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:demanda-danos-perjuicios-franquiciado-tras-resolucion-civ-0693`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (13 veces)
- [ ] Nº DE DOCUMENTO (12 veces)
- [ ] NÚMERO (10 veces)
- [ ] DENOMINACIÓN SOCIAL DE LA FRANQUICIADORA (4 veces)
- [ ] FECHA (4 veces)
- [ ] DENOMINACIÓN SOCIAL DE LA FRANQUICIADA (2 veces)
- [ ] DURACIÓN PACTADA (2 veces)
- [ ] IMPORTE TOTAL (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] MARCA (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] AÑO
- [ ] COMUNIDAD AUTÓNOMA
- [ ] CORREO ELECTRÓNICO
- [ ] DOCUMENTO ACREDITATIVO
- [ ] DOMICILIO
- [ ] DOMICILIO PROFESIONAL
- [ ] DÍA
- [ ] FECHAS
- [ ] IMPORTE EN LETRA
- [ ] MES
- [ ] NOMBRE DEL PERITO
- [ ] NOMBRE Y APELLIDOS DEL LETRADO
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR
- [ ] Nº DE HOJA
- [ ] Nº DE INSCRIPCIÓN
- [ ] Nº DE TOMO
- [ ] OBJETO SOCIAL
- [ ] PERIODO
- [ ] PRODUCTOS O SERVICIOS
- [ ] PROVINCIA
- [ ] SEDE
- [ ] TELÉFONO

## Normas que cita el formulario

- art. 399.1 LEC
- art. 45 LEC
- art. 85.1.º LOPJ
- art. 399 LEC
- art. 249.2 LEC
- art. 253 LEC
- art. 23 LEC
- art. 5 Ley Orgánica 1/2025
- art. 1101 Código Civil
- art. 62.1 Ley 7/1996
- art. 2 Real Decreto 201/2010
- art. 1100 Código Civil
- art. 63.2.º Código de Comercio
- art. 394 LEC

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

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR], Procurador/a de los Tribunales, en nombre y representación de la entidad [DENOMINACIÓN SOCIAL DE LA FRANQUICIADA], a cuya justificación aporto escritura de poder inscrita en el Registro Electrónico de Apoderamientos Judiciales con el nº [Nº DE INSCRIPCIÓN] y que se puede acreditar mediante consulta automatizada orientada al dato por parte del órgano judicial al cual tengo el honor de dirigirme, acompañándose certificación electrónica del Registro Electrónico de Apoderamientos Judiciales como documento nº [Nº DE DOCUMENTO] por si no fuera posible la consulta automatizada; dirigido por el letrado/a abajo firmante D./Dña. [NOMBRE Y APELLIDOS DEL LETRADO], con despacho profesional en [DOMICILIO PROFESIONAL], ante el Tribunal comparezco y, como mejor proceda en Derecho, DIGO:

Que, en la representación que ostento, interpongo demanda de juicio declarativo ordinario sobre reclamación de daños y perjuicios y otros particulares contra la entidad [DENOMINACIÓN SOCIAL DE LA FRANQUICIADORA], con domicilio en [DOMICILIO].

Que esta parte asume el compromiso de recibir cualquier comunicación dirigida por la oficina judicial, durante toda la fase declarativa e, incluso, en una eventual fase de ejecución, por medios telemáticos, en términos del art. 399.1 II LEC, consignándose a estos efectos la siguiente dirección de correo electrónico y número de teléfono: [CORREO ELECTRÓNICO] y [TELÉFONO].

Fundamento la misma en los siguientes hechos y consideraciones jurídicas:

HECHOS

PRIMERO.– Mi representada [DENOMINACIÓN SOCIAL DE LA FRANQUICIADA] tiene como objeto social [OBJETO SOCIAL]. Se encuentra inscrita en el Registro Mercantil de [PROVINCIA], hoja [Nº DE HOJA], tomo [Nº DE TOMO], y está al corriente en el pago de sus obligaciones fiscales, como se acredita mediante [DOCUMENTO ACREDITATIVO] que se acompaña como documento número [Nº DE DOCUMENTO].

La demandada es titular de una cadena de establecimientos comerciales dedicada a [ACTIVIDAD, por ejemplo la venta de productos de cosmética], con sede en [COMUNIDAD AUTÓNOMA], y que se ha extendido por todo el territorio nacional mediante el sistema de franquicias en determinadas ciudades, en el marco de un plan estratégico de expansión de la marca [MARCA], propiedad de la demandada.

SEGUNDO.– En concreto, por lo que atañe a mi cliente, en fecha [FECHA] se firmó entre ambas partes un contrato o acuerdo de franquicia, que se adjunta como documento número [Nº DE DOCUMENTO], en el cual la entidad [DENOMINACIÓN SOCIAL DE LA FRANQUICIADORA] cedía a la demandante el derecho a explotar la forma de comercialización de [PRODUCTOS O SERVICIOS], bajo la citada marca [MARCA], a cambio de un canon de entrada de [IMPORTE] euros y de una cantidad de [IMPORTE] euros al mes. En concreto, se cedía el uso de la marca, se transmitía el know-how relativo a la publicidad, tratamiento y venta de los distintos productos que se comercializan con la misma (recogidos en el manual de operaciones que se adjunta como documento número [Nº DE DOCUMENTO]) y se pasaba a proporcionar un apoyo continuado de asistencia comercial durante el plazo de [DURACIÓN PACTADA] que se fijaba en el contrato.

TERCERO.– El primer año del contrato transcurrió sin problemas ni incidentes a mencionar, cumpliendo ambas partes lo preceptuado. Se adjunta, como documento número [Nº DE DOCUMENTO], certificado bancario en el que se detallan los pagos realizados por mi patrocinada en cumplimiento de su obligación asumida. Si bien, a finales de [PERIODO], los suministros de los productos empezaron a demorarse en el tiempo y a enviarse en menor cantidad de la previamente solicitada. Asimismo, la rápida interlocución que, hasta entonces, se había mantenido entre las partes contratantes a los efectos de la prestación del apoyo continuado fue sustituida por falta de contestación de los mensajes de correo electrónico, en algunos casos, y por contestaciones genéricas y tardías, en otros. Se aporta bloque documental de correos electrónicos enviados, debidamente certificados con el correspondiente hash, como documento número [Nº DE DOCUMENTO], en el que se pueden observar las dudas planteadas, las escasas e insuficientes contestaciones y los correos posteriores planteando quejas, tampoco resueltas, sobre la cuestión.

CUARTO.– Finalmente, el pasado [FECHA], [NÚMERO] meses antes de que transcurriera el plazo fijado contractualmente, se recibió un burofax, cuya copia se adjunta como documento número [Nº DE DOCUMENTO], en el que se informaba de la resolución unilateral del contrato, con la justificación genérica, y sin mención de conductas concretas, de que se había hecho un uso indebido de la marca por mi mandante, absolutamente ajeno a la realidad.

Dicha resolución ha impedido a mi cliente seguir vendiendo productos amparados bajo tal marca, a los efectos de no incurrir en responsabilidad con el franquiciador y propietario de la marca. Lo que ha provocado la imposibilidad de generar ingresos en los citados [NÚMERO] meses que quedaban por cumplir del contrato, y que se cuantifican en la cantidad de [IMPORTE TOTAL] euros, correspondientes a:

1.– [IMPORTE] euros por los beneficios dejados de obtener, calculados conforme a la media de ingresos netos reales obtenidos con la venta de los productos en los primeros [NÚMERO] meses de vigencia del contrato. Se aporta al respecto, como documento número [Nº DE DOCUMENTO], informe pericial elaborado a fecha [FECHA] por el auditor de cuentas [NOMBRE DEL PERITO], tras analizar la documentación contable de mi mandante.

2.– [IMPORTE] euros por los gastos desembolsados para la venta del producto objeto de la franquicia, correspondientes a la parte proporcional del canon de entrada abonado, sobre la base de [NÚMERO] meses sin vigencia, para un total de [NÚMERO] meses pactados.

3.– [IMPORTE] euros por la pérdida de clientela durante el plazo no disfrutado, computado sobre el incremento anterior, en el mismo informe pericial.

QUINTO.– Con objeto de evitar la presente demanda, se requirió notarialmente para la reanudación del contrato por el plazo pactado, con advertencia de la interposición de la presente demanda, reclamando los perjuicios que se van a generar y se están generando. Se aporta acta de requerimiento notarial como documento número [Nº DE DOCUMENTO].

SEXTO.– La parte actora manifiesta que, previamente a la presentación de la presente demanda, se han llevado a cabo negociaciones con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria, incluyéndose entre las acciones realizadas el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución.

Finalmente, se requirió notarialmente a la demandada con fecha [FECHA] para la reanudación del contrato por el plazo pactado, con advertencia de la interposición de la presente demanda, reclamando los perjuicios que se van a generar y se están generando, fijando un plazo de 30 días naturales para llegar a un acuerdo amistoso, a través del abogado que firma este escrito, el cual fue contestado por la demandada por el mismo medio, [ELEGIR: rechazando el acuerdo / habiendo sido solo posible un acuerdo parcial], viéndonos en la necesidad de acudir a la presente vía judicial respecto a los extremos de la controversia en los que se mantiene la discrepancia.

Acompaño como documento nº [Nº DE DOCUMENTO] el requerimiento efectuado y como documento nº [Nº DE DOCUMENTO] la contestación de la demandada.

A los anteriores hechos son aplicables los siguientes

FUNDAMENTOS DE DERECHO

I.– Jurisdicción y competencia

Es competente la Sección Civil del Tribunal de Instancia del domicilio de la demandada, al que se dirige la presente demanda, por aplicación de lo dispuesto en los arts. 45 y 51 LEC, en relación con lo dispuesto en el art. 85.1.º LOPJ.

El domicilio social de la entidad demandada se encuentra en la ciudad de [LOCALIDAD], como resulta del documento número [Nº DE DOCUMENTO] que se acompaña, y se podrá comprobar con la certificación del Registro Mercantil, que se aportará en su momento a los autos, una vez expedida y retirada.

II.– Procedimiento

El procedimiento ajustado a Derecho será el del juicio declarativo ordinario regulado en los arts. 399 a 436 LEC, atendiendo a la cantidad reclamada, que es de [IMPORTE] euros, en aplicación de lo dispuesto en el art. 249.2 LEC.

III.– Capacidad

Al tratarse de sociedades mercantiles inscritas en el Registro Mercantil, de conformidad con los arts. 20 y 33 del texto refundido de la Ley de Sociedades de Capital, aprobado por Real Decreto Legislativo 1/2010, de 2 de julio, tienen personalidad jurídica y, consiguientemente, capacidad para ser parte y capacidad para comparecer en juicio.

IV.– Legitimación

Corresponde a la demandante la activa, por ser parte en el contrato suscrito y haber cumplido sus obligaciones contractuales como franquiciada, y la pasiva la tiene la demandada, en cuanto ocupa la posición de contraparte contractual y ha resuelto unilateralmente, y sin causa alguna, el contrato que nos ocupa, por lo que debe abonar los perjuicios ocasionados.

V.– Cuantía

Conforme al art. 253 LEC, cifro la cuantía de la presente demanda en [IMPORTE] euros, que es el importe de la cantidad que se reclama.

VI.– Postulación y defensa

Conforme a lo previsto en los arts. 23 y 31 LEC, se presenta la demanda por medio de procurador/a legalmente habilitado y bajo dirección del letrado firmante de la misma.

VII.– Cumplimiento de los requisitos de procedibilidad

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4.º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

VIII.– Fondo de la cuestión controvertida

A) Acción ejercitada

Se plantea una demanda de reclamación de cantidad, al amparo de lo dispuesto en los arts. 1101 y siguientes del Código Civil, por los perjuicios ocasionados con la resolución unilateral e injusta del contrato de franquicia, sin que haya transcurrido el plazo pactado contractualmente.

B) Del contrato de franquicia

El contrato que liga a las partes es el denominado contrato de franquicia, que tiene encaje legal en el art. 62.1 de la Ley 7/1996, de 15 de enero, de Ordenación del Comercio Minorista. En el mismo se define la actividad comercial en régimen de franquicia como aquella que se lleva a efecto en virtud de un acuerdo o contrato por el que una empresa, denominada franquiciadora, cede a otra, denominada franquiciada, el derecho a la explotación de un sistema propio de comercialización de productos o servicios. El art. 2 del Real Decreto 201/2010, de 26 de febrero, por el que se regula el ejercicio de la actividad comercial en régimen de franquicia y la comunicación de datos al registro de franquiciadores, profundiza en dicha definición legal indicando que se trata de un contrato en el cual una empresa, el franquiciador, cede a otra, el franquiciado, en un mercado determinado, a cambio de una contraprestación financiera directa, indirecta o ambas, el derecho a la explotación de una franquicia, sobre un negocio o actividad mercantil que el primero venga desarrollando anteriormente con suficiente experiencia y éxito, para comercializar determinados tipos de productos o servicios, y que comprende por lo menos:

a) El uso de una denominación o rótulo común u otros derechos de propiedad intelectual o industrial y una presentación uniforme de los locales o medios de transporte objeto del contrato.

b) La comunicación por el franquiciador al franquiciado de unos conocimientos técnicos o un saber hacer, que deberá ser propio, sustancial y singular, y

c) La prestación continua por el franquiciador al franquiciado de una asistencia comercial, técnica o ambas durante la vigencia del acuerdo; todo ello sin perjuicio de las facultades de supervisión que puedan establecerse contractualmente.

La definición legal ha sido construida con la interpretación del contrato por la jurisprudencia, de la que es ejemplo la STS de 9 de marzo de 2009 (recurso 2266/2003), que señala que se trata de un contrato en el que una de las partes, que es titular de una determinada marca, rótulo, patente, emblema, fórmula, método o técnica de fabricación o actividad industrial o comercial, otorga a la otra el derecho a utilizar, por un tiempo determinado y en una zona geográfica delimitada, bajo ciertas condiciones de control, aquello sobre lo que ostentaba la titularidad, contra la entrega de una prestación económica, que suele articularse normalmente mediante la fijación de un canon o porcentaje. Se trata, en consecuencia, de un negocio jurídico en el cual, según la STS de 15 de diciembre de 2006 (recurso 2239/2005), con cita de la STS de 21 de octubre de 2005 (754/2005), a cambio de un precio se cede el uso de un derecho de propiedad industrial, el «know how» o «saber cómo», consistente en el conocimiento o conjunto de conocimientos técnicos que no son de dominio público y que son necesarios para la fabricación o comercialización de un producto, para la prestación de un servicio o para la organización de una unidad o dependencia empresarial, por lo que procuran a quien los domina una ventaja sobre los competidores que se esfuerza en conservar evitando su divulgación. Y, asimismo, se proporciona una prestación continua por el franquiciador al franquiciado, consistente en una asistencia comercial o técnica durante la vigencia del contrato.

La resolución citada, con apoyo en la STJCE de 28 de enero de 1986 (caso «Pronuptia»), distingue el contrato de franquicia frente a los de suministro o de distribución de mercancías, en base a que:

a) el franquiciador debe transmitir su «know how», o asistencia o metodología de trabajo, aplicando sus métodos comerciales;

b) dicho franquiciador queda obligado a diseñar, dirigir y sufragar las campañas publicitarias realizadas para difundir el rótulo y la marca del franquiciador.

Asimismo, en aplicación del carácter de contrato atípico (anterior a la mencionada regulación legal), la citada resolución declara que se regirá, en primer lugar, por la voluntad de las partes plasmada en cláusulas y requisitos concretos que, fundados, sin duda, en relaciones de buena fe y mutua confianza, deben producir todos sus efectos y, para el caso de que hubiera lagunas, para interpretar su contenido será preciso recurrir a figuras de contratos típicos afines a dicha relación consensual atípica.

En el presente supuesto, queda fuera de toda duda que nos encontramos ante un contrato de franquicia, que mi mandante ha cumplido con todas y cada una de las obligaciones asumidas y que ha visto cómo, sin alegar siquiera una causa concreta, ni mucho menos acreditarla, la relación comercial termina [NÚMERO] meses antes de lo previsto, cuando se habían realizado una serie de gastos y se esperaban unos beneficios, en relación con el plazo de [DURACIÓN PACTADA] fijado desde un principio.

C) De los daños y perjuicios reclamados

Como ya se ha indicado, dado que el contrato ha finalizado, sin causa alguna, antes del periodo pactado, sin que se pueda atribuir ninguna suerte de incumplimiento a mi mandante, mediante la presente demanda se procede a reclamar los daños y perjuicios que la no continuación de la franquicia produce, tanto por lo que respecta a los gastos ocasionados o daño emergente como a la pérdida de ingresos generada o lucro cesante. Todo ello, con base en los arts. 1101 y siguientes del Código Civil.

A partir de todo ello, tal y como se recoge en la SAP Illes Balears de 9 de noviembre de 2011 (rec. 319/2011), procede la aplicación del régimen común del Código Civil, arts. 1306 y 1307: los beneficios dejados de obtener y los costes ocasionados en atención a la existencia del contrato, y que no se hayan podido amortizar. En el presente caso, precisamente, porque la relación comercial ha terminado antes de lo previsto. En la resolución citada se estudian en profundidad los daños y perjuicios que sufre, o puede sufrir, el franquiciado, con cita de la Sentencia del Tribunal Supremo, Sala Primera, de 4 de marzo de 1997 (Rec. 953/1993) o la Sentencia del Tribunal Supremo, Sala Primera, de 3 de julio de 1986, que han desarrollado una clásica doctrina jurisprudencial al respecto y que distingue entre cuatro conceptos:

1.– Los beneficios dejados de obtener y derivados de los contratos de exclusiva (lucro cesante). Se indica que su fundamento se encuentra en la propia indemnización del interés contractual positivo, esto es, en la necesidad de reponer al perjudicado en la situación en que se hallaría si el suceso dañoso no se hubiera producido, que fundamenta la indemnización. Se exige que se le indemnice también la ganancia que haya dejado de obtener. En el supuesto que nos ocupa, en función del periodo no disfrutado tras la extinción del contrato por resolución injustificada, atendiendo a los beneficios que verosímilmente se han dejado de percibir, constituyen lucro cesante. La doctrina jurisprudencial citada distingue entre dos tipos de períodos a tener en cuenta atendiendo a las circunstancias: el período restante de duración del contrato o el período de duración de la prohibición de competencia tras la extinción. Esta segunda opción obedece al hecho de que, aunque la resolución contractual tiene como efecto la liberación de las partes del contrato, el efecto liberatorio no afecta a las estipulaciones previstas en el contrato para el caso de extinción que producen sus efectos a partir de la misma. En el presente caso se reclama únicamente por el primero de los periodos, a partir de la media de los beneficios netos obtenidos en los [NÚMERO] primeros meses de la vida del contrato. Calculados conforme al informe pericial acompañado a la presente demanda, lo que ofrece una media de [IMPORTE] euros mensuales, para un total de [IMPORTE] euros por los [NÚMERO] meses que restaban por cumplir.

2.– Los gastos realizados por el distribuidor o cesionario en sus locales para representar dignamente al concedente o fabricante. Extremo que, en el escenario puesto de manifiesto, se residencia en el canon de entrada, por importe de [IMPORTE] euros, que se abonó en atención a los [NÚMERO] meses pactados y que debe devolverse en la cantidad de [IMPORTE] euros, correspondientes a los [NÚMERO] meses no disfrutados. Normalmente la justificación del canon varía de caso a caso en la práctica contractual. Pero suelen incluirse, como aquí ocurre, la valoración de los gastos que va a ocasionar al franquiciador, la asistencia prestada por él mismo o su personal durante el período entre la estipulación del contrato y la apertura del establecimiento o el acceso al valor acumulado por la red en términos de buen nombre de la marca y know-how acumulado por esta antes del ingreso en la misma. Prestaciones que no se han satisfecho, ni se van a satisfacer, en el periodo indicado. En consecuencia, se tratará de una prestación duradera parcialmente incumplida y el valor de la parte proporcional que corresponda al período de contrato no disfrutado como consecuencia de la resolución unilateral injustificada por parte del franquiciador deberá ser entregado al franquiciado en concepto de indemnización de daños y perjuicios por daño emergente.

3.– Los gastos y desembolsos que se haya tenido que efectuar por indemnizaciones (laborales o de otro tipo) al personal, cuando la empresa no puede continuar por la resolución unilateral llevada a cabo por el concedente, lo que representa que se ha producido el despido de los dependientes y auxiliares comerciales. Extremos que no acontecen en el supuesto en análisis. [OPCIONAL — adaptar si en el caso concurren estos gastos]

4.– El incremento de la clientela que, gracias a la labor del concesionario, ha experimentado su principal y supone que, extinguido el contrato, la cartera de clientes sigue disponiéndola el concedente. El supuesto de indemnización por clientela representa una indemnización compensatoria, que ha de distinguirse de la indemnización de perjuicios derivada de incumplimiento, cuyo alcance normalmente será más amplio (Sentencia del Tribunal Supremo, Sala Primera, de 27 de mayo de 1993, Rec. 2778/1990). El cálculo de la compensación no puede llevarse con olvido de los márgenes de beneficios obtenidos por el concesionario, pero teniéndose siempre en cuenta las reducciones que resulten procedentes. Se debe centrar la indemnización en la exclusiva función de captación y consolidación de clientela, con lo que se remuneraría, y parece lo más justo y equitativo, la específica labor de apertura y creación de mercados para los productos objeto de la distribución. Extremos que se tienen en cuenta en el informe pericial también adjuntado a la presente demanda y que cuantifica la indemnización en [IMPORTE] euros.

Todo lo cual suma la cantidad global de [IMPORTE TOTAL] euros, que viene a constituir el principal aquí reclamado, por todos los conceptos detallados.

D) Intereses

Citamos los arts. 1100, 1101, 1108 y 1109 del Código Civil y el art. 63.2.º del Código de Comercio, sobre pago de los intereses moratorios a partir de la interpelación judicial.

IX.– Costas

Conforme al art. 394 LEC, las costas han de imponerse a la demandada.

Por lo expuesto,

SUPLICO AL TRIBUNAL

Que, habiendo por presentado este escrito de demanda con los documentos que lo acompañan y copias de uno y otros, los admita y me tenga por comparecido y parte en la representación que ostento y que acreditada dejo; y por promovido juicio declarativo ordinario frente a [DENOMINACIÓN SOCIAL DE LA FRANQUICIADORA], acuerde dar traslado a la demandada para que comparezca y la conteste y, previos los trámites legales y recibimiento a prueba que desde ahora se interesa, se dicte en su día sentencia por la que, estimando la demanda:

A) Se condene a la demandada, [DENOMINACIÓN SOCIAL DE LA FRANQUICIADORA], a que abone a mi principal la cantidad de [IMPORTE EN LETRA] euros ([IMPORTE] euros) por los daños y perjuicios ocasionados.

B) Se abonen a mi representada los intereses legales desde la interposición de la demanda.

Todo ello con imposición de las costas del juicio a la parte demandada.

Es justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del abogado/a: [NOMBRE Y APELLIDOS] Firma del procurador/a: [NOMBRE Y APELLIDOS]
