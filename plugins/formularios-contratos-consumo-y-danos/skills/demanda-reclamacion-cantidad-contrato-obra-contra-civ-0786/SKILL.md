---
name: demanda-reclamacion-cantidad-contrato-obra-contra-civ-0786
description: "Demanda de reclamación de cantidad por contrato de obra contra una sociedad civil irregular. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de reclamación de cantidad por contrato de obra contra una sociedad civil irregular

> Formulario **CIV-0786** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Demanda en reclamación de cantidad dirigida contra sociedad civil que por dedicarse al comercio debe considerarse mercantil irregular.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de reclamación de cantidad por contrato de obra contra una sociedad civil irregular» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de reclamación de cantidad por contrato de obra contra una sociedad civil irregular” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:demanda-reclamacion-cantidad-contrato-obra-contra-civ-0786`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (15 veces)
- [ ] IMPORTE (10 veces)
- [ ] Nº DE DOCUMENTO (9 veces)
- [ ] FECHA (8 veces)
- [ ] DENOMINACIÓN SOCIAL (7 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] Nº (2 veces)
- [ ] PORCENTAJE (2 veces)
- [ ] AÑO
- [ ] CALLE
- [ ] FECHAS
- [ ] LUGAR
- [ ] Nº DE PLAZOS
- [ ] SEDE

## Normas que cita el formulario

- art. 45 LEC
- art. 51.2 LEC
- art. 50.3 LEC
- art. 40 Código Civil
- art. 249.2 LEC
- art. 6.2 LEC
- art. 7.7 LEC
- art. 7.2 LEC
- art. 253 LEC
- art. 5 Ley Orgánica 1/2025
- art. 1.542 CC
- art. 1.544 CC
- art. 1.583 CC
- art. 117 Código de Comercio
- art. 116 Código de Comercio
- art. 39 TRLSC
- art. 1.665 Código Civil
- art. 1.677 Código Civil
- art. 127 Código de Comercio
- art. 128 Código de Comercio
- art. 129 Código de Comercio

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

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, en nombre y representación de la entidad [DENOMINACIÓN SOCIAL], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], dirigido por el Letrado abajo firmante D./Dña. [NOMBRE Y APELLIDOS], con despacho profesional en [LOCALIDAD], ante el Tribunal comparezco y como mejor proceda en Derecho DIGO:

Que, en la representación que ostento, interpongo demanda de juicio declarativo ordinario frente a la sociedad mercantil irregular [DENOMINACIÓN SOCIAL], en la persona de su administrador, D./Dña. [NOMBRE Y APELLIDOS] frente a este último como socio de la primera, y frente a sus otros tres socios D./Dña. [NOMBRE Y APELLIDOS], D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS], en reclamación de la cantidad de [IMPORTE] euros ( €).

Fundamento la misma en los siguientes hechos y consideraciones jurídicas:

HECHOS

PRIMERO.- La entidad [DENOMINACIÓN SOCIAL], contrató con mi mandante la realización de una obra de reforma integral del local anexo al establecimiento de hostelería que explota en la calle [CALLE] de [LOCALIDAD], mediante contrato firmado el [FECHA] por el administrador único de [DENOMINACIÓN SOCIAL], D./Dña. [NOMBRE Y APELLIDOS], y por quien afirmaba ser administrador social y representante legal de la codemandada, D./Dña. [NOMBRE Y APELLIDOS], también demandado en la presente litis. En el contrato se pactaba la realización de la obra de reforma conforme al proyecto elaborado por la arquitecta, D./Dña. [NOMBRE Y APELLIDOS], en el plazo de [Nº] meses, y por un precio presupuestado de 0 euros, abonando un [PORCENTAJE] al inicio de la obra y el resto con la entrega del local reformado. La demandada se encargaba del suministro de material. Se acompaña copia del referido contrato como documento nº [Nº DE DOCUMENTO].

SEGUNDO.- El primer pago, de [IMPORTE] euros se abonó correctamente, y las obras se realizaron sin ninguna incidencia, en los plazos previstos, según el proyecto indicado, y recibiendo los suministros pactados. Se acompaña, como documento nº [Nº DE DOCUMENTO], certificado de fin de obra elaborado por la arquitecta indicada, en el cual no se hace constar ninguna suerte de objeción en relación a las obras ejecutadas.

Tal escenario de normalidad se alteró, cuando mi mandante exigió el pago del [PORCENTAJE] del precio pactado, puesto que por el representante, D./Dña. [NOMBRE Y APELLIDOS], se puso de manifiesto las dificultades financieras que estaba atravesando la entidad codemandada, y la imposibilidad de abonar la cantidad íntegra en tal momento, solicitando un aplazamiento del pago pendiente.

TERCERO.- Tras varias conversaciones, el [FECHA] se pactó un nuevo calendario de pagos, mediante el cual se efectuaría un pago inmediato de [IMPORTE] euros, y el resto, [IMPORTE] euros, en [Nº DE PLAZOS] plazos mensuales de [IMPORTE] euros cada uno. Se adjunta como documento nº [Nº DE DOCUMENTO], dicho calendario de pago firmado por las mismas partes.

El pago de los [IMPORTE] euros se hizo en el plazo de tres días, mediante transferencia bancaria; si bien, transcurrido un mes no sólo se dejó de abonar el primer plazo mensual, sino que la parte demandada dejó de contestar a cualquier intento de puesta en contacto en solicitud de explicaciones. Mi mandante envió correo certificado exigiendo el abono de la parte impagada [IMPORTE], con advertencia del inicio de acciones legales, sin respuesta hasta la fecha. Se aporta copia de dicho correo como documento nº [Nº DE DOCUMENTO].

CUARTO.- Mi mandante se dirigió al Registro Mercantil para obtener datos necesarios con objeto de demandar correctamente a [DENOMINACIÓN SOCIAL], pero no encontró ningún tipo de inscripción de la misma. Teniendo únicamente los datos de quien obraba como representante legal, así como la dirección del establecimiento de hostelería, se solicitó ante el órgano judicial a quien tengo el honor de dirigirme la práctica de diligencias preliminares (tramitadas con el nº [Nº]/[AÑO]), que culminaran en la exhibición documental acordada mediante auto de fecha [FECHA]. De la misma se desprende que se trata de una entidad no inscrita en el Registro Mercantil, que funciona como una sociedad mercantil irregular, conformada por los otros cuatro codemandados, siendo D./Dña. [NOMBRE Y APELLIDOS] su administrador y representante, conforme al pacto privado de socios firmado por todos ellos en fecha [FECHA], el cual no ha sido inscrito en Registro Público alguno. Se aportan, como documentos nº [Nº DE DOCUMENTO] y [Nº DE DOCUMENTO], la mencionada resolución judicial, y el pacto entre socios facilitado en el marco de las indicadas diligencias preliminares.

QUINTO.- La parte actora manifiesta que, previo a la presentación de la presente demanda, se han llevado a cabo negociaciones con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad, y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria; incluyéndose entre las acciones realizadas el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución.

Finalmente, mi representado envío un requerimiento fehaciente al demandado con fecha [FECHA], fijando un plazo de 30 días naturales para llegar a un acuerdo amistoso, a través del abogado que firma este escrito, el cual fue contestado por el demandado por el mismo medio, rechazando el acuerdo/ habiendo sido solo posible un acuerdo parcial, viéndonos en la necesidad de acudir a la presente vía judicial, respecto a los extremos de la controversia en los que se mantiene la discrepancia.

Acompaño como documento nº [Nº DE DOCUMENTO], el requerimiento efectuado y como documento nº [Nº DE DOCUMENTO], la contestación del demandado.

A los anteriores hechos, son aplicables los siguientes

FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN Y COMPETENCIA

Es competente la Sección Civil del Tribunal de Instancia al que se dirige la presente demanda, por encontrarse en su partido judicial el domicilio de los demandados, así como el establecimiento explotado por ellos, mediante la sociedad irregular codemandada. Todo ello, por aplicación de lo dispuesto en los arts. 45, 50 y 51 de la LEC.

En este sentido, el art. 51.2 la LEC establece que los entes sin personalidad podrán ser demandados en el domicilio de sus gestores o en cualquier lugar en que desarrollen su actividad, lo cual es coherente con el fuero general de empresarios y profesionales del art. 50.3 de la LEC. Así, dicho precepto legal establece que en los litigios derivados de su actividad empresarial o profesional, también podrá ser competente el Tribunal del lugar donde se desarrolle dicha actividad y, si tuvieren establecimientos a su cargo en diferentes lugares, en cualquiera de ellos a elección del actor. Por último, ambos preceptos coinciden con lo dispuesto en el art. 40 del Código Civil, a partir del cual se entiende que para el ejercicio de los derechos y el cumplimiento de las obligaciones civiles, el domicilio de las personas naturales es el lugar de su residencia.

II.- PROCEDIMIENTO

El procedimiento ajustado a derecho será el del juicio declarativo ordinario regulado en los arts. 399 a 436 de la misma Ley, atendiendo a la cantidad reclamada que es de [IMPORTE] euros, en aplicación de lo dispuesto en el art. 249.2 de la LEC.

III.- CAPACIDAD Y REPRESENTACIÓN

En cuanto a la capacidad de la entidad codemandada, el art. 6.2 de la LEC dispone que "Sin perjuicio de la responsabilidad que, conforme a la ley, pueda corresponder a los gestores o a los partícipes, podrán ser demandadas, en todo caso, las entidades que, no habiendo cumplido los requisitos legalmente establecidos para constituirse en personas jurídicas, estén formadas por una pluralidad de elementos personales y patrimoniales puestos al servicio de un fin determinado". En el presente caso, la entidad [DENOMINACIÓN SOCIAL] es, como posteriormente se razonará, una sociedad mercantil irregular compuesta por varios socios que ponen su trabajo y patrimonio para la explotación del restaurante objeto de su actividad; sin que se haya constituido como una sociedad mercantil formal, cumpliendo los requisitos establecidos en la Ley de Sociedades de Capital. Asimismo, son demandados los socios de la misma al ser responsables, de manera solidaria, respecto a las deudas de la sociedad mercantil irregular, en la manera en que se dirá en el fundamento relativo al fondo de la acción ejercitada.

Por ello se dirige la demanda contra la entidad, y contra los cuatro socios, uno de los cuales es su representante conforme al pacto privado entre socios, y quien negoció y celebró con mi mandante el contrato de obra en cuya virtud se acciona. Así, el artículo 7.7 LEC señala que "Por las entidades sin personalidad a que se refiere el artículo 7.2 de la LEC comparecerán en juicio las personas que, de hecho o en virtud de pactos de la entidad, actúen en su nombre frente a terceros".

IV.- LEGITIMACIÓN

Corresponde al demandante la activa por ser la parte que ha cumplido sus obligaciones como contratista que ha ejecutado correctamente la obra, y la pasiva la tiene la parte demandada, en cuanto comitente o propietaria de la obra, que debe abonar en su integridad el precio pactado por ella.

V.- CUANTÍA

Conforme al art. 253 de la LEC cifro la cuantía de la presente demanda en [IMPORTE] euros, que es el importe de la cantidad que se reclama.

VI.- POSTULACIÓN Y DEFENSA

Conforme a lo previsto en los arts. 23 y 31 de la Ley de Enjuiciamiento Civil, se presenta la demanda por medio de Procurador/a legalmente habilitado y bajo dirección de Letrado firmante de la misma.

VII.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

VIII.- FONDO DE LA CUESTIÓN CONTROVERTIDA

1.- De la acción ejercitada:

Se ejercita acción de cumplimiento contractual en base a los artículos 1.089 y 1.091 del Código Civil, a partir del contrato de obra que ligó a las partes y que fue correctamente ejecutado por mi mandante. Así, el artículo 1.542 del CC, señala que el arrendamiento puede ser de obras o servicios; desarrollándolo el artículo 1.544 CC al establecer que en el arrendamiento de obras o servicios, una de las partes se obliga a ejecutar una obra o a prestar a la otra un servicio por precio cierto. Desde tan escueta regulación, así como de los artículos 1.583 CC y siguientes, la jurisprudencia del Tribunal Supremo ha diseñado y diferenciado los dos tipos de arrendamientos que se establecen, el de obra y el de servicios.

La STS de 3 de noviembre de 1983 establece la diferencia fundamental entre ambos contratos: si el arrendador se obliga a la prestación de servicios o de trabajo o de una actividad en sí misma, no al resultado que aquella prestación produce, el arrendamiento es de servicios y, en cambio, si se obliga a la prestación de un resultado sin consideración al trabajo que lo crea, el arrendamiento es de obra. Por ello, el arrendamiento de servicios es un contrato de mera actividad en el que existe un ‘intuitu personae’ pues se valoran las circunstancias personales de quien va a llevar a cabo los servicios. En cambio, el arrendamiento de obra es un contrato de resultado cuyos elementos reales son la obtención de ese resultado (opus consumatum et perfectum), y la fijación de un precio cierto que el comitente debe satisfacer en el momento de recibir el encargo encomendado.

En el contrato que nos ocupa, se pacta la obtención de un resultado (realización de la obra diseñada) a cambio de un precio cierto. Es un contrato de arrendamiento de obra correctamente ejecutado por mi mandante, que ha supuesto un beneficio para el comitente o propietario de la obra. Por ello, existe la obligación del pago en los términos pactados, sin que se pueda alegar de contrario ninguna suerte de ejecución defectuosa, que no ha sido, siquiera, insinuada en las negociaciones posteriores a la finalización de la obra, y que desembocaron en un segundo calendario de pago, también incumplido por la parte demandada.

El impago definitivo del precio, generaría un enriquecimiento injusto para el propietario de la obra, tal y como ha definido la tradicional doctrina del Tribunal Supremo definiendo sus elementos: a) un enriquecimiento por parte del demandado que sea injusto, representado por un aumento de su patrimonio; b) un empobrecimiento del actor representado por un daño positivo o un lucro frustrado que se encontraría reflejado en la falta de remuneración de su trabajo profesional; c) la inexistencia de un precepto legal que excluya la aplicación de este precepto (STS de 30 de septiembre de 1993, rec. 3004/1990). En el presente caso la obra ejecutada por mi mandante ha producido el resultado requerido por el comitente, en la manera reflejada en el contrato, sin que el contratista haya recibido el justo pago que ahora se ve obligado a reclamar por la vía judicial.

2.- De la sociedad mercantil irregular:

De esta forma, mi mandante, sin saberlo, contrató con una sociedad mercantil irregular que no había cumplido los requisitos legales para adoptar una forma específica. En este sentido, el artículo 117 del Código de Comercio determina la validez y obligatoriedad del contrato de compañía mercantil entre los que lo celebren, cualquiera que sea su forma. Si bien, faltando los requisitos de la escritura pública fundacional y la inscripción en el Registro Mercantil, la misma tiene el carácter de sociedad mercantil irregular, conforme se vienen interpretando los arts. 116, 117 y 119 del Código de Comercio y el art. 39 TRLSC 1/2010. La interpretación auténtica en este sentido, lo establece el art. 322.3 del Reglamento del Registro Mercantil, modificado por el Real Decreto 685/2005, de 10 de junio, sobre publicidad de resoluciones concursales

Al respecto, las STS, Sala 1ª, de 27-11-1998, rec. 3350/1995 y 8-06-1995 señalan que cuando no hay ni siquiera otorgamiento de escritura pública constitutiva, nos encontraríamos ante una sociedad sin personalidad jurídica. Si, en cambio, se da ésta pero no la inscripción en el Registro Mercantil, entonces sí hay personalidad jurídica y efectos -"ad extra"- y no se puede hablar en estos casos de una situación de semipersonalidad jurídica, sino más bien de personalidad controlada o condicionada conforme a la normativa de la sociedad en formación.

Y en esta línea, la STS de 25-10-1999, rec. 646/1995, enumera los requisitos necesarios para la existencia de un contrato de Sociedad conforme al art. 1.665 del Código Civil, unos elementos objetivos y subjetivos, a saber: aportaciones de actividades o bienes, que pasan a formar un patrimonio común, un fin común, y una "affectio societatis" o "animus contrahendi societatis". En consecuencia, para que tengamos una sociedad irregular sólo hará falta privarle de los requisitos de la regularidad. Así, se precisan:

- El elemento personal de los socios constituyentes, con capacidad para constituir una sociedad irregular, la cual es la misma que para la regular, pues la nulidad o anulabilidad de sus pactos internos se rigen por las reglas generales sobre capacidad -jurídica y de obrar- y legitimación. Como única excepción, el art. 1.677 del Código Civil establece que no pueden contraer sociedad universal entre sí las personas a quienes está prohibido otorgarse recíprocamente alguna donación o ventaja.
- El cual debe ir unido a la "affectio societatis": Este requisito subjetivo, intención de constituir la sociedad, es esencial, puede desprenderse a partir de los elementos objetivos, supone un "plus" añadido al simple consentimiento contractual [STS de 30-04-1986 y 21-02-1987], y consiste en la voluntad de unión paralela y dirigida a un mismo fin negocial (Sentencia Tribunal Supremo, Sala Primera, de lo Civil, de 8 Mar. 1995, Rec. 3527/1991), o voluntad de unión de una pluralidad de sujetos para correr en común ciertos riesgos [STS de 23-05-1989].
- Un elemento real consistente en un fin común: La entrega al fondo común, implica que lo aportado se hace común a todos los socios, con ánimo de lucro, o sea, el designio de partir la ganancia que se obtenga, ganancia que se habría obtenido por el empleo del fondo creado entre los respectivos socios. La Sentencia Tribunal Supremo, Sala Primera, de lo Civil, 285/2005 de 29 Abr. 2005, Rec. 4093/1998 dispone que en el Código Civil (arts. 1.665, 1.666 y 1.681 CC) se condiciona la existencia del contrato de sociedad a la de un fin común [STS de 17-03-1964 y 30-06-1972], que ha de ser promovido por los socios mediante una comunidad de contribución, la cual se logra con el cumplimiento de la obligación de aportar industria o bienes [STS de 23-05-1962; STS 24-10-1975; STS 17-02-1978; STS 10-02-1984; STS 19-11-1984].
- Al cual debe acompañarse un patrimonio común; si bien tal requisito se ha ido relativizando, tal y como disponen la Sentencia del Tribunal Supremo, Sala Primera, de lo Civil, 609/2005 de 15 Jul. 2005, Rec. 3995/1998 y de STS 14-07-2006, rec. 4435/1999 cuando indica que no es necesario que el fondo común o social se constituya con numerario o bienes determinados, pudiendo conformarse con aportaciones de trabajo.
- Por último, todo ello debe acompañarse del elemento formal, o, mejor dicho, de la ausencia de las formalidades legales. Sobre este punto las STS de 3-1-1992; STS 30-6-1995; STS 12-7-1996 y STS 5-2-1998.

En el presente caso, concurren todos los elementos reseñados: las cuatro personas físicas codemandadas pueden otorgarse recíprocamente donaciones o ventajas, decidieron en su momento formar una sociedad mediante un pacto privado, con objeto de explotar un restaurante, aportando dinero y su trabajo personal, sin que se hayan cumplimentado los requisitos para constituirse como sociedad mercantil regular.

3.- De la responsabilidad de los socios codemandados:

Nos encontramos en definitiva con una sociedad irregular con actividad mercantil, que ha de regirse 1º.- por las normas de la sociedad colectiva respecto de terceros, 2º.- por sus pactos entre los socios [art. 117 del Código de Comercio y STS de 21-04-1987; STS 20-02-1988, STS 16-03-1989 y STS 19-12-2006, rec. 342/2000) y, 3º.- en su defecto [STS de 20-02-1988, STS 8-07-1993 y STS 21-03-1998, rec. 3393/1994] las normas del Código de Comercio y, finalmente, las establecidas en el Código Civil.

De esta forma, rigiéndose la entidad codemandada por las normas de la sociedad colectiva frente a terceros; el efecto fundamental de la Sociedad Mercantil Irregular es, respecto aquellos que todos los socios, sean o no gestores de la misma, estarán obligados personal y solidariamente, con todos sus bienes, a las resultas de las operaciones que se hagan a nombre y por cuenta de la compañía (tal y como ordena el artículo 127 del Código de Comercio). Como quiera que la sociedad no tiene publicidad (al no haberse incorporado a registro público alguno) no es de aplicación el art. 128 Código de Comercio, conforme al cuál los socios no autorizados debidamente para usar de la firma social. no obligarán con sus actos y contratos a la compañía, aunque lo ejecuten a nombre de ésta y bajo su firma. Sí que lo es, en cambio, el art. 129 del Código de Comercio "Si la administración de las compañías colectivas no se hubiere limitado por un acto especial a alguno de los socios, todos tendrán la facultad de concurrir a la dirección y manejo de los negocios comunes, y los socios presentes se pondrán de acuerdo para todo contrato u obligación que interese a la sociedad" [STS de 21-6-1983; STS 20-2-1988; STS 3-4-1991; STS 9-3-1992; STS 8-7-1993; STS 25-11-1996, rec. 2954/1994 y STS 21-6-1998, rec. 911/1994].

Por ello, la demanda se dirige contra los cuatro socios, incluyendo al representante que firmó el contrato de ejecución de obra, quienes deberán responder solidariamente con su patrimonio de la deuda de la sociedad por ellos conformadas, sobre la que se ha razonado anteriormente.

IX.- INTERESES

Según lo dispuesto en los artículos 1.100 y 1.108 del Código Civil, proceden intereses legales de la cantidad reclamada desde la reclamación extrajudicial, operada por correo certificado, el [FECHA]; frente al cual no contestó la parte demandada.

X.- COSTAS

Conforme al artículo 394 de la L.E.C., las costas han de imponerse a la parte demandada.

Por lo expuesto,

SUPLICO AL TRIBUNAL.

Que habiendo por presentado este escrito de demanda con los documentos que lo acompañan y copias de uno y otros, los admita y me tenga por comparecido en parte en la representación que ostento y que acreditada dejo; y por promovido juicio declarativo ordinario frente a la sociedad mercantil irregular [DENOMINACIÓN SOCIAL], y frente a sus cuatro socios D./Dña. [NOMBRE Y APELLIDOS], D./Dña. [NOMBRE Y APELLIDOS], D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS]. Suplico que se acuerde dar traslado a los demandados para que comparezcan y la contesten, y previo los trámites legales, y recibimiento a prueba que desde ahora se interesa, se dicte en su día sentencia por la que estimando la demanda se condene a los demandados, de manera solidaria, a abonar a mi mandante la cantidad de [IMPORTE] euros ( €), incrementada con el interés legal desde el requerimiento extrajudicial operado el [FECHA].

Todo ello con imposición de las costas del juicio a la parte demandada.

Es justicia de hacerse en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a

========================================================================
