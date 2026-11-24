---
name: demanda-juicio-ordinario-resolver-contrato-franquicia-civ-0688
description: "Demanda de juicio ordinario para resolver un contrato de franquicia. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio ordinario para resolver un contrato de franquicia

> Formulario **CIV-0688** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio ordinario formulada por el franquiciador contra el franquiciado que ha dejado de pagar las liquidaciones mensuales, para que se declare resuelto el contrato de franquicia por incumplimiento, se le condene al pago de las cantidades adeudadas, a la devolución de los manuales y del know how y a cesar en el uso de la marca, con indemnización de daños y perjuicios. Formulario adaptado a la reforma procesal de la LO 1/2025.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio ordinario para resolver un contrato de franquicia» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio ordinario para resolver un contrato de franquicia” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:demanda-juicio-ordinario-resolver-contrato-franquicia-civ-0688`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (7 veces)
- [ ] FECHA (6 veces)
- [ ] IMPORTE (6 veces)
- [ ] MARCA (6 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] ACTIVIDAD (2 veces)
- [ ] AÑO (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] DÍA (2 veces)
- [ ] MES (2 veces)
- [ ] NIF (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] PERIODO (2 veces)
- [ ] SEDE (2 veces)
- [ ] ARTÍCULO
- [ ] DENOMINACIÓN SOCIAL DE LA FRANQUICIADA
- [ ] DENOMINACIÓN SOCIAL DE LA FRANQUICIADORA
- [ ] DURACIÓN
- [ ] IMPORTE DE LA CUOTA FIJA
- [ ] LOCALIDAD
- [ ] MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] NOMBRE DEL PERITO
- [ ] NOMBRE Y APELLIDOS DEL LETRADO
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR
- [ ] Nº DE ANTECEDENTE
- [ ] PLAZO
- [ ] PRECIO O CANON
- [ ] PRÓRROGA
- [ ] TEXTO

## Normas que cita el formulario

- art. 45 Ley 1/2000
- art. 85.1 LOPJ
- art. 51.1 LEC
- art. 249.2 LEC
- art. 1089 Código Civil
- art. 1091 Código Civil
- art. 1258 Código Civil
- art. 1255 Código Civil
- art. 1124 Código Civil
- art. 1100 Código Civil
- art. 41.1.a Ley 17/2001
- art. 5 Ley 3/2004
- art. 394 LEC
- art. 7.2 Ley 10/2012

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

### Avisos de actualización (2) — se aplican en el texto, nunca se copian en el documento

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…aber sido declarada inconstitucional y nula por la STC 140/2016, de 21 de julio.»: comprobar la cuantía vigente de la cuota fija de la tasa.

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

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR], Procurador/a de los Tribunales, actuando en representación de la entidad [DENOMINACIÓN SOCIAL DE LA FRANQUICIADORA], con domicilio en [DOMICILIO] y NIF [NIF], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], ante el Tribunal comparezco con la asistencia de letrado/a D./Dña. [NOMBRE Y APELLIDOS DEL LETRADO], y como mejor proceda en Derecho, DIGO:

Que mediante el presente escrito formulo demanda de juicio ordinario en ejercicio de acción resolutoria del contrato de fecha [FECHA] y otras que en súplica se concretarán, frente a la mercantil [DENOMINACIÓN SOCIAL DE LA FRANQUICIADA], domiciliada en [DOMICILIO] y con NIF [NIF]. Baso la presente demanda en los siguientes hechos y fundamentos de Derecho:

HECHOS

PRIMERO.– La demandante y la demandada son empresas dedicadas al servicio de [ACTIVIDAD], tanto para particulares como para otras empresas.

El [DÍA] de [MES] de [AÑO], mi representada y la demandada suscribieron un contrato de franquicia por el que la primera, titular de la marca [MARCA], cedía a la franquiciada el uso de la marca en las condiciones de tiempo y espacio pactadas en el referido contrato, que se acompaña como DOCUMENTO Nº [Nº DE DOCUMENTO], y que son las siguientes:

Fecha de efectos: [FECHA]
Duración: [DURACIÓN]
Prórroga: [PRÓRROGA]
Precio: [PRECIO O CANON]
Otras condiciones: [TEXTO]

SEGUNDO.– Como consecuencia de dicho contrato, la franquiciada demandada se integró en la red de franquicia para la explotación del negocio de [ACTIVIDAD] promovida por la franquiciadora.

Como se reconoce en el contrato, en su antecedente [Nº DE ANTECEDENTE], en el momento de la firma se entregaron a la demandada los manuales de procedimiento y las instrucciones operativas complementarias que fijan la red de franquicias y todo el material que constituye el «know how».

TERCERO.– En lo que aquí interesa, en cumplimiento del referido contrato, se emitieron por mi mandante las siguientes liquidaciones mensuales, según lo pactado: [PERIODO] por importe de [IMPORTE], [PERIODO] por importe de [IMPORTE], etc. En prueba de ello se acompañan las liquidaciones emitidas como DOCUMENTOS Nº [Nº] y [Nº].

Estas liquidaciones fueron impagadas por la franquiciada en sus respectivas fechas de vencimiento.

CUARTO.– Debido al impago descrito en el hecho anterior, mi representada dirigió [NÚMERO] requerimientos a la demandada para que cumpliera sus obligaciones contractuales. En el último de estos requerimientos se informaba claramente a la demandada de que, si no cumplía en el plazo de [PLAZO] con el pago de la cantidad a que venía obligada, la hoy actora daría por resuelto el contrato de franquicia.

En prueba de lo expuesto se acompañan los burofaxes y el requerimiento remitido por conducto notarial que se identifican como DOCUMENTOS Nº [Nº] y [Nº].

QUINTO.– La franquiciada hizo caso omiso a los requerimientos efectuados, por lo que, mediante comunicación escrita de fecha [FECHA], se comunicó la resolución del contrato de franquicia y se reclamó nuevamente el pago de las cantidades adeudadas, así como la devolución de los manuales de procedimiento y las instrucciones operativas complementarias que fijan la red de franquicias y todo el material que constituye el «know how».

En prueba de ello se acompaña como DOCUMENTO Nº [Nº] el requerimiento notarial remitido en dicha fecha.

SEXTO.– La franquiciada no solo no abonó las cantidades adeudadas, sino que siguió haciendo uso de la marca [MARCA], pese a los múltiples requerimientos para que cesase en él.

El perjuicio sufrido por mi mandante por el ilícito uso de su marca por parte de la demandada asciende a la cantidad de [IMPORTE]. En prueba de ello se acompaña como DOCUMENTO Nº [Nº] el informe pericial elaborado por [NOMBRE DEL PERITO].

Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como DOCUMENTO Nº [Nº].

Ante la falta de respuesta satisfactoria por parte de la demandada, mi representada se ve en la obligación de instar la presente acción resolutoria de contrato y de reclamación de cantidad.

A los anteriores hechos resultan de aplicación los siguientes

FUNDAMENTOS DE DERECHO

-I-

Jurisdicción y competencia. Son de aplicación al caso el artículo 117 de la Constitución Española, los artículos 21, 22.1 y 85.1 de la Ley Orgánica del Poder Judicial y el artículo 36 de la Ley de Enjuiciamiento Civil, que determinan la jurisdicción ordinaria como la única competente para conocer de los negocios o demandas civiles que se susciten en territorio español entre españoles, entre extranjeros y entre españoles y extranjeros con arreglo a lo establecido en la Ley Orgánica del Poder Judicial y en los tratados y convenios internacionales en los que España sea parte. A su vez, dichos órganos son competentes con carácter exclusivo, en materia de obligaciones contractuales, cuando estas hayan nacido o deban cumplirse en España (artículo 22.3 de la Ley Orgánica del Poder Judicial). El conocimiento de este litigio corresponde a los Tribunales de Instancia, en cuanto por disposición legal expresa no viene atribuido a otros Tribunales (artículo 45 de la Ley 1/2000, en relación con lo dispuesto en el artículo 85.1 LOPJ).

Corresponde el conocimiento del juicio a la Sección Civil del Tribunal de Instancia que por reparto corresponda (artículo 68 de la Ley de Enjuiciamiento Civil) de [SEDE], a la que me dirijo en aplicación del artículo 51.1 LEC al ser el domicilio de la demandada.

-II-

Procedimiento. El procedimiento será el previsto para el juicio ordinario, conforme señala el artículo 249.2 LEC, al ser la cuantía reclamada superior a 15.000 euros.

-III-

Capacidad para ser parte y capacidad procesal. La tienen la actora y la demandada, conforme establecen los artículos 6 y 7 de la Ley de Enjuiciamiento Civil.

-IV-

Legitimación. Activa: a tenor del artículo 10 de la Ley de Enjuiciamiento Civil, la legitimación de mi representada deriva de su condición de titular de la relación jurídica de franquicia, en la posición de franquiciadora, según contrato de fecha [FECHA]. Pasiva: corresponde a la demandada como parte de las relaciones contractuales, en la posición de franquiciada.

-V-

Postulación y defensa. Se cumplen las normas procesales de postulación, ya que la demanda se presenta por medio de procurador legalmente habilitado y bajo la dirección de letrado firmante de la misma, conforme a lo dispuesto en los artículos 23 y 31 de la Ley de Enjuiciamiento Civil.

-VI-

Acumulación de acciones. Se acumulan por la actora las acciones de resolución contractual, reclamación de cantidad, obligación de dar, cesación y de indemnización de daños y perjuicios, que se derivan frente a la demandada por los mismos hechos, acumulación permitida por el artículo 71.2 de la Ley de Enjuiciamiento Civil.

-VII-

Cuantía. Por así exigirlo el apartado 1.º del artículo 253 de la Ley de Enjuiciamiento Civil, se pone de manifiesto que la cuantía de esta demanda es de [IMPORTE] euros, calculada con arreglo a la regla 2.ª del artículo 252 de la Ley de Enjuiciamiento Civil.

-VIII-

Fondo de la reclamación. Resulta de aplicación el artículo 1089 del Código Civil, según el cual: «Las obligaciones nacen de la ley, de los contratos y cuasi contratos, y de los actos y omisiones ilícitos o en que intervenga cualquier género de culpa o negligencia.» Así como el artículo 1091 del Código Civil: «Las obligaciones que nacen de los contratos tienen fuerza de ley entre las partes contratantes, y deben cumplirse a tenor de los mismos.»

De conformidad con el artículo 1258 del Código Civil, que dice: «Los contratos se perfeccionan por el mero consentimiento, y desde entonces obligan, no sólo al cumplimiento de lo expresamente pactado, sino también a todas las consecuencias que, según su naturaleza, sean conformes a la buena fe, al uso y a la ley.»

El artículo 1255 del Código Civil establece la libre regulación de las relaciones contractuales, fijando unos límites: «Los contratantes pueden establecer los pactos, cláusulas y condiciones que tengan por conveniente, siempre que no sean contrarios a las leyes, a la moral ni al orden público.»

En cuanto a la configuración del contrato de franquicia, el Tribunal Supremo (Sala de lo Civil, Sección 1.ª), en Sentencia núm. 145/2009, de 9 de marzo, dice: «La doctrina jurisprudencial de esta Sala se refiere al contrato de franquicia en varias Sentencias: 15 de mayo de 1985 -que alude al contrato de "franchising" y lo caracteriza por la autorización que el concedente da al concesionario para utilizar la marca, generalmente internacional, integrándolo en su red de comercialización-; 23 de octubre de 1989 -con ocasión de un supuesto en que franquiciador y franquiciado se reprochan recíproco incumplimiento contractual-, 27 de septiembre de 1996, Rec. 3545/1992; 21 de octubre de 1996, Rec. 3664/1991 -en relación con un caso de extinción del contrato por expiración del plazo prorrogado-; 4 de marzo de 1997, Rec. 953/1993, y 30 de abril de 1998, Rec. 373/1994. La sentencia de 27 de septiembre de 1996, Rec. 3545/1992, cuya doctrina es reproducida en lo fundamental en la Sentencia de 30 de abril de 1998, Rec. 373/1994, califica el contrato de franquicia de atípico; recoge una definición de la doctrina (como "aquel que se celebra entre dos partes jurídica y económicamente independientes, en virtud del cual una de ellas -franquiciador- otorga a la otra -franquiciado- el derecho a utilizar bajo determinadas condiciones de control, y por un tiempo y zona delimitados, una técnica en la actividad industrial o comercial o de prestación de servicios del franquiciado, contra entrega por éste de una contraprestación económica"); y, siguiendo a la Sentencia del TJCE de 28 de enero de 1986 (caso "Pronuptia"), la diferencia de los contratos de suministro o de distribución de mercancías, en que: a) el franquiciador debe transmitir su "know-how", o asistencia o metodología de trabajo, aplicando sus métodos comerciales; y, b) que dicho franquiciador queda obligado a diseñar, dirigir y sufragar las campañas publicitarias, realizadas para difundir el rótulo y la marca del franquiciador. Asimismo, en aplicación del carácter de contrato atípico, declara que se regirá, en primer lugar, por la voluntad de las partes plasmada en cláusulas y requisitos concretos que, fundados, sin duda, en relaciones de buena fe y mutua confianza, deben producir todos sus efectos, y para el caso de que hubiera lagunas, para interpretar su contenido, será preciso recurrir a figuras de contratos típicos afines a dicha relación consensual atípica. Y, por último, la Sentencia de 4 de marzo de 1997, Rec. 953/1993 (sobre resolución contractual por incumplimiento) dice que la característica fundamental de la modalidad de contrato denominada de franquicia o "franchising" es que "una de las partes, que es titular de una determinada marca, rótulo, patente, emblema, fórmula, método o técnica de fabricación o actividad industrial o comercial, otorga a la otra el derecho a utilizar, por un tiempo determinado y en una zona geográfica delimitada, bajo ciertas condiciones de control, aquello sobre lo que ostentaba la titularidad, contra la entrega de una prestación económica, que suele articularse normalmente mediante la fijación de un canon o porcentaje". (En el mismo sentido se pronuncia la sentencia de 16 de marzo de 2007, Rec. 740/2000).»

-IX-

El artículo 1124 del Código Civil dice: «La facultad de resolver las obligaciones se entiende implícita en las recíprocas, para el caso de que uno de los obligados no cumpliere lo que le incumbe. El perjudicado podrá escoger entre exigir el cumplimiento o la resolución de la obligación, con el resarcimiento de daños y abono de intereses en ambos casos. También podrá pedir la resolución, aun después de haber optado por el cumplimiento, cuando éste resultare imposible. El Tribunal decretará la resolución que se reclame, a no haber causas justificadas que le autoricen para señalar plazo. Esto se entiende sin perjuicio de los derechos de terceros adquirentes, con arreglo a los artículos 1295 y 1298 y a las disposiciones de la Ley Hipotecaria.»

La moderna jurisprudencia afirma que la facultad resolutoria de los contratos «puede ejercitarse en nuestro ordenamiento, no sólo en la vía judicial sino mediante declaración no sujeta a forma y dirigida a la otra parte, a reserva de que sean los Tribunales quienes examinen y sancionen su procedencia cuando es impugnada, bien negando el incumplimiento, bien rechazando la oportunidad de extinguir el contrato» (Sentencia del Tribunal Supremo 399/2007, de 27 de marzo). Y que «no cabe desconocer la existencia de poderes que permiten al sujeto en una situación singular prevista en la norma legal o establecida por los contratantes en lícito ejercicio del principio de autonomía negocial, ocasionar por su exclusiva voluntad un determinado efecto jurídico, sea constitutivo, modificativo o cancelatorio de la relación, poniendo término a la misma en este último caso; derechos o facultades que se actúan normalmente no por medio de una acción, sino de una declaración de voluntad recepticia que genera el efecto deseado una vez producida la notificación del destinatario, de suerte que la intervención de los organismos jurisdiccionales sólo es menester cuando el afectado discuta la eficacia de la declaración potestativa, salvo supuestos excepcionales» (sentencias del Tribunal Supremo 1048/2004, de 27 de octubre, y 700/2005, de 3 de octubre).

Para facultar la resolución unilateral en las obligaciones recíprocas, a instancia de quien no incumplió o incumplió justificadamente, la jurisprudencia exige que el incumplimiento revista cierta entidad, y así la sentencia 210/2008, de 14 de marzo, exige el incumplimiento grave de «una obligación principal dentro de la economía del contrato»; y, en la 223/2011, de 12 de abril, con cita de numerosas anteriores, que se trate de un incumplimiento caracterizado como «verdadero y propio», «grave», «esencial», «que tenga importancia y trascendencia para la economía de los interesados o entidad suficiente para impedir la satisfacción económica de las partes o bien genere la frustración del fin del contrato», «la frustración de las legítimas expectativas o aspiraciones o la quiebra de la finalidad económica o frustración del fin práctico». En este caso es más que patente el incumplimiento grave por parte de la demandada, ya que ha incumplido su obligación principal, que consiste en el pago del precio pactado, siendo este incumplimiento reiterado (se adeudan [NÚMERO] mensualidades) y habiéndose constatado su voluntad rebelde, al no haberse atendido ninguno de los previos requerimientos que se le han dirigido.

-X-

Los artículos 1100, 1101, 1124 y 1258 del Código Civil, en cuanto a la procedencia de la resolución del contrato por incumplimiento y la responsabilidad contractual derivada: los contratos obligan no solo al cumplimiento de lo expresamente pactado, sino también a todas las consecuencias que, según su naturaleza, sean conformes a la buena fe, al uso y a la ley, por lo que es incuestionable que la franquiciada debe cumplir su obligación de pago en los términos pactados, y si no lo hace no cumple estrictamente el contrato, incumplimiento que debe ser sancionado con la resolución, por ser de carácter grave, y debiendo indemnizar los daños y perjuicios derivados del incumplimiento.

-XI-

De conformidad con el artículo 41.1.a) y b) de la Ley 17/2001, de 7 de diciembre, de Marcas, el titular cuyo derecho de marca sea lesionado podrá reclamar en la vía civil la cesación de los actos que violen su derecho y la indemnización de los daños sufridos.

El artículo 43 de dicha norma establece los criterios para fijar dicha indemnización.

-XII-

Procede el abono de los intereses del artículo 5 de la Ley 3/2004, de 29 de diciembre, por la que se establecen medidas de lucha contra la morosidad en las operaciones comerciales, desde los respectivos vencimientos de las cantidades liquidadas.

Subsidiariamente deberá ser condenada la demandada al pago del interés legal desde la reclamación extrajudicial, y ello en aplicación de los artículos 1100 y [ARTÍCULO] del Código Civil.

-XIII-

En materia de costas, el artículo 394 LEC señala que las de primera instancia se imponen a la parte que vea rechazadas sus pretensiones.

En base a lo anterior,

SUPLICO AL TRIBUNAL que tenga por presentada la presente demanda con los documentos a ella adjuntos y por parte en la representación que ostento y, tras la pertinente tramitación, se dicte sentencia por la que:

a) Se declare resuelto el contrato de fecha [FECHA] suscrito entre las partes por incumplimiento de la entidad demandada.

b) Se condene a la entidad demandada a abonar a mi mandante la cantidad de [IMPORTE] euros, incrementada con los intereses del artículo 5 de la Ley 3/2004 o, subsidiariamente, con los intereses legales desde la reclamación extrajudicial.

c) Se condene a la demandada a entregar a mi mandante los manuales de procedimiento y las instrucciones operativas complementarias que fijan la red de franquicias y todo el material que constituye el «know how», propiedad de mi mandante.

d) Se declare que la demandada ha estado haciendo un uso ilícito de la marca [MARCA] desde el [FECHA] y, en consecuencia:

d.1) Se condene a la demandada a cesar en la utilización de la marca [MARCA].

d.2) Se condene a la demandada a retirar y entregar a mi mandante cualquier rótulo, material comercial o de escritorio en que aparezca la marca [MARCA].

d.3) Se condene a la demandada a indemnizar a mi mandante en la cantidad de [IMPORTE] euros por el uso indebido de la marca [MARCA].

e) Se condene a la demandada al pago de las costas del procedimiento.

OTROSÍ DIGO.– Que estando la presente demanda sujeta al abono de la tasa por el ejercicio de la potestad jurisdiccional fijada por la Ley 10/2012, de 20 de noviembre, modificada por el RDL 3/2013 y la Ley 25/2015, de 28 de julio, y desarrollada por la Orden HAP/2662/2012, de 13 de diciembre, siendo mi representada persona jurídica no exenta de su pago, se acompaña a la presente demanda como documento nº [Nº DE DOCUMENTO] la correspondiente autoliquidación, con el ejemplar para la Administración de Justicia debidamente validado y en el que consta el pago de la cantidad de [IMPORTE DE LA CUOTA FIJA] euros correspondiente a la cuota fija, sin que se incluya la cuota variable prevista en el artículo 7.2 de la Ley 10/2012 al haber sido declarada inconstitucional y nula por la STC 140/2016, de 21 de julio.

En virtud de lo anterior,

SUPLICO AL TRIBUNAL que tenga por hecha la anterior manifestación a los efectos pertinentes y por acompañado el documento justificativo del abono de la tasa.

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del abogado: [NOMBRE Y APELLIDOS] Firma del procurador: [NOMBRE Y APELLIDOS]
