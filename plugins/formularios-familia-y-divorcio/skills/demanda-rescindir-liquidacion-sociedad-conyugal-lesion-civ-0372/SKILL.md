---
name: demanda-rescindir-liquidacion-sociedad-conyugal-lesion-civ-0372
description: "Demanda para rescindir la liquidación de la sociedad conyugal por lesión en más de la cuarta parte. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda para rescindir la liquidación de la sociedad conyugal por lesión en más de la cuarta parte

> Formulario **CIV-0372** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio ordinario sobre rescisión de la liquidación de una sociedad conyugal de bienes por sufrir uno de los cónyuges lesión en más de la cuarta parte y sobre complemento respecto del importe de un inmueble enajenado. Se acompañan dictámenes periciales.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda para rescindir la liquidación de la sociedad conyugal por lesión en más de la cuarta parte» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda para rescindir la liquidación de la sociedad conyugal por lesión en más de la cuarta parte” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-rescindir-liquidacion-sociedad-conyugal-lesion-civ-0372`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (21 veces)
- [ ] IMPORTE (19 veces)
- [ ] Nº DE DOCUMENTO (16 veces)
- [ ] NOMBRE Y APELLIDOS (14 veces)
- [ ] FECHA (12 veces)
- [ ] Nº (10 veces)
- [ ] NÚMERO (9 veces)
- [ ] DENOMINACIÓN SOCIAL (5 veces)
- [ ] AÑO (4 veces)
- [ ] CALLE (4 veces)
- [ ] DOMICILIO (4 veces)
- [ ] NOMBRE DEL NOTARIO (4 veces)
- [ ] LETRA (2 veces)
- [ ] SEDE (2 veces)
- [ ] SUPERFICIE (2 veces)
- [ ] CORREO ELECTRÓNICO
- [ ] ENTIDAD BANCARIA
- [ ] FINCA
- [ ] IMPORTE EN CIFRA
- [ ] IMPORTE EN LETRA
- [ ] LIBRO
- [ ] LUGAR
- [ ] MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] MES
- [ ] Nº DE COLEGIADO/A
- [ ] Nº DE PROCEDIMIENTO
- [ ] Nº DE PROTOCOLO
- [ ] PROVINCIA
- [ ] TELÉFONO
- [ ] TOMO
- [ ] ÓRGANO O PERSONA

## Normas que cita el formulario

- art. 24.1 LEC
- art. 399.1 LEC
- art. 90 Código Civil
- art. 265.2 LEC
- art. 85.1 LOPJ
- art. 45 LEC
- art. 50.1 LEC
- art. 10 LEC
- art. 253.1 LEC
- art. 251 LEC
- art. 23 LEC
- art. 399 LEC
- art. 5 Ley Orgánica 1/2025
- art. 1.074 CC
- art. 1.410 CC
- art. 1291.1 CC
- art. 1.077 CC
- art. 1.079 CC
- art. 394.1 LEC
- art. 1.077 Código Civil

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] QUE POR TURNO CORRESPONDA»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…ENTO] / por la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Notas al pie del formulario original:
(1) A la hora de su acreditación, todos los poderes deben estar inscritos en el Registro Electrónico de Apoderamientos Judiciales (REAJ). Se supone que, para su acreditación, basta con la consulta (de dicho Registro) automatizada orientada al dato. Algo que está a disposición de cualquier Letrado de la Administración de Justicia. Sin embargo, dado que el art. 24.2 LEC, configura la certificación de dicha inscripción como vía subsidiaria de acreditación, para el caso de que el sistema no permita aquella consulta automatizada; se señala en el modelo que se acompaña certificación electrónica. El sistema permite emitir dicha certificación para quien inscribe el poder.

(2) A la luz del art. 807 LEC, si el Tribunal ante el que se ha seguido el proceso de separación o divorcio es el competente funcionalmente, por ‘antecedencia’, para la liquidación del régimen conyugal de bienes comunitario, parece que lo será para conocer de la demanda de rescisión por lesión de la liquidación ya efectuada en convenio regulador, o a través del procedimiento de arts. 806 a 811 LEC, si bien el juicio sería igualmente el ordinario.

(3) El art. 155.3 LEC permite fijar expresar varios domicilios del demandado (el que aparezca en el padrón municipal o conste oficialmente a estos efectos; el que aparezca en Registro oficial o en publicaciones de colegios profesionales, si se trata de empresas o personas colegiadas; donde desarrolle su actividad profesional o laboral no ocasional; si es empresa mercantil, el domicilio de cualquiera de sus administradores, gerentes, o apoderados; o, si es asociación que consta en registro oficial; el domicilio del presidente, miembro o gestor de la Junta correspondiente). Cuando se señalen varios, indicará el orden a seguir para la notificación, con vistas al éxito de la misma.

(4) El art. 155.3 LEC configura una obligación adicional del demandante, consistente en aportar cuantos datos sean de utilidad para localizar al demandado: número de identificación fiscal o de extranjeros, nº [Nº] de teléfono o de fax, dirección de correo electrónico, o similares.

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] QUE POR TURNO CORRESPONDA

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales y de D./Dña. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], representación que acredito mediante escritura de poder otorgada a mi favor (existen tres posibilidades para otorgar el apoderamiento al Procurador de los Tribunales, conforme dispone el art. 24.1 LEC)

[OPCIONAL — opción en función de cómo se haya otorgado el poder]

[ELEGIR UNA OPCIÓN: Si el poder se otorga a través de la sede judicial electrónica / Si el poder se otorga mediante comparecencia apud acta / Si el poder se otorga ante Notario]

bajo la dirección letrada de D./Dña. [NOMBRE Y APELLIDOS], abogado/a en ejercicio, con despacho profesional abierto en [LOCALIDAD], colegiado nº [Nº DE COLEGIADO/A] del Ilustre Colegio de la Abogacía de [LOCALIDAD], ante el Tribunal comparezco y como mejor en Derecho proceda, DIGO:

Que mediante el presente escrito y en ejercicio de la pretensión de RESCISIÓN DE LA LIQUIDACIÓN DE LA SOCIEDAD DE GANANCIALES, prevista en los artículos 1.073 y 1.074 del Código Civil, interpongo DEMANDA de JUICIO DECLARATIVO ORDINARIO, contra D./Dña. [NOMBRE Y APELLIDOS], con domicilio, primero en [DOMICILIO]; y segundo, el domicilio laboral en [DOMICILIO]); con email [CORREO ELECTRÓNICO]; y con número de teléfono móvil [TELÉFONO]; todo ello de conformidad con los hechos y fundamentos de derecho que se especificarán.

Que esta parte asume el compromiso de recibir cualquier comunicación dirigida por la oficina judicial, durante toda la fase declarativa, e, incluso, en una eventual fase de ejecución por medios telemáticos, en términos del art. 399.1 II LEC, consignándose a estos efectos la siguiente dirección de correo electrónico y nº [Nº] de teléfono:

HECHOS

PRIMERO.- Mi mandante Doña [NOMBRE Y APELLIDOS] y el demandado D./Dña. [NOMBRE Y APELLIDOS], contrajeron matrimonio el día [FECHA], en [LOCALIDAD], bajo el régimen legal de gananciales.

Se acredita este extremo mediante el documento n°1, consistente en el certificado de matrimonio expedido por el Registro Civil.

SEGUNDO.- A finales del año [AÑO] el demandado confesó a mi mandante que mantenía relaciones con otra mujer, y no era feliz en su matrimonio, por lo que la esposa, sometida primero a una gran tensión emocional, y luego sumida en depresión, aceptó iniciar procedimiento de separación.

El [FECHA] se formuló demanda de divorcio de mutuo acuerdo, siendo tramitado el juicio por los abogados de la empresa en que desempeña cargo directivo el esposo.

TERCERO.- El abogado D./Dña. [NOMBRE Y APELLIDOS], redactó el convenio regulador, que incluía la liquidación de la sociedad de gananciales, siendo el demandado el que facilitó a aquél la documentación necesaria relativa a los títulos de propiedad de los bienes gananciales reflejados en dicho convenio, y quien, de forma exclusiva, asignó las valoraciones a los bienes, así como propuso la forma de adjudicación de los bienes.

CUARTO.- Con fecha [FECHA] se dictó sentencia de divorcio en autos nº [Nº DE PROCEDIMIENTO] / por la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº] , decretándose la disolución por CAUSA DE DIVORCIO del matrimonio formado por mi patrocinada y el demandado.

El convenio regulador suscrito por los cónyuges el [FECHA], es aprobado conforme se recoge en el Fundamento de Derecho segundo, al no estimarse dañoso para los hijos menores, ni gravemente perjudicial para ninguno de los cónyuges, de conformidad con lo dispuesto en el artículo 90 del Código Civil. Se acompañan como documentos n° [Nº DE DOCUMENTO] y [Nº DE DOCUMENTO] copia de la sentencia y del convenio regulador suscrito por las partes.

QUINTO.- En la liquidación practicada se produce una lesión en los derechos de mi mandante, superior a la cuarta parte, como consecuencia de una manifiesta infravaloración de los bienes que le fueron adjudicados al demandado.

A continuación, describimos los bienes inventariados, y los datos que evidencian el muy superior valor real de cada uno de ellos en relación con el que se les atribuye en la liquidación.

ACTIVO

A) INVENTARIO DE BIENES INMUEBLES

1.- Urbana: Vivienda número [NÚMERO], letra [LETRA], en el término de [LOCALIDAD], hoy casa nº [NÚMERO] de calle [CALLE] Tiene una superficie útil de [Nº] m2.

Título: Este bien inmueble pertenece a la sociedad de gananciales, conforme resulta de escritura otorgada en [LOCALIDAD], el [FECHA], ante el Notario D./Dña. [NOMBRE DEL NOTARIO], nº xx [Nº DE PROTOCOLO] de su protocolo.

Se acompaña, haciendo documento nº [Nº DE DOCUMENTO], certificado del Registro de la Propiedad de [LOCALIDAD], en que figura como finca [FINCA], al libro [LIBRO] de [LOCALIDAD], tomo [TOMO], folio

Cargas: HIPOTECA, Inscripción nº [NÚMERO] a favor del BANCO [ENTIDAD BANCARIA], en garantía de un préstamo recibido por TTT [DENOMINACIÓN SOCIAL], respondiendo la finca de [IMPORTE] euros, según escritura otorgada en [LOCALIDAD], bajo la fe del Notario D./Dña. [NOMBRE DEL NOTARIO], con nº [NÚMERO] de su protocolo.

Consta en la certificación registral predicha, y se aporta dictamen pericial elaborado por el Agente de la Propiedad Inmobiliaria D./Dña. [NOMBRE Y APELLIDOS], como documento nº [Nº DE DOCUMENTO], en que se detalla la situación de la finca a fecha [FECHA], con sus características y precio.

Valor dado a efectos de liquidación: de [IMPORTE] euros.

Respecto de este bien, manifestamos nuestra conformidad con su valoración, ya que se trata de una vivienda de más de veinte años, cuyo valor de mercado en el momento de la disolución de la sociedad de gananciales realizada en el año [AÑO] era el que se le otorgó.

A efectos de establecer la realidad de la evaluación respecto de este bien, se acredita mediante el dictamen previamente mencionado, en el que se determina que el valor de la vivienda a fecha del mes de [MES] del año en curso asciende a [IMPORTE] euros, dos años más tarde de la adjudicación, efectuándose una ponderación por la evolución última del mercado inmobiliario totalmente objetivada.

2.- Predio rústico denominado ‘, sito en el lugar de [LOCALIDAD], término de [LOCALIDAD], del municipio de [LOCALIDAD] Tiene una superficie de [SUPERFICIE] áreas, [SUPERFICIE] centiáreas, con una cabaña para aperos de labranza de [Nº] m2 en planta aproximadamente.

Título: Este bien pertenece a la sociedad de gananciales al haber sido adquirido constante el matrimonio por compraventa que consta en documento privado de fecha [FECHA], del que se acompaña copia como documento nº [Nº DE DOCUMENTO], sin que se conozca que se haya procedido a la inscripción, por falta de tracto registral. Esta libre de cargas.

Valor dado a efectos de liquidación: de [IMPORTE] euros.

Respecto de este bien inmueble, se manifiesta que ha sido claramente infravalorado, porque sobre el terreno descrito, al socaire de rehabilitar la cabaña existente en el momento de la compra, cuyo local ha quedado como trastero, se ha edificado una vivienda unifamiliar con planta baja con vestíbulo, cocina, salón-comedor, y cuarto de baño, y planta alta bajo cubierta con tres habitaciones, distribuidor y otro cuarto de baño, siendo la superficie edificada de [Nº] m2 y útil de [Nº] m2, lo cual obviamente ha incrementado su valor sobre el precio de compra y sobre el asignado a efectos de liquidación.

Puede alcanzar un valor del orden de [IMPORTE] euros a la fecha de realizarse la liquidación de la sociedad, con arreglo al informe técnico y fotografías que ilustran sobre el estado de la "cabaña" convertida en vivienda unifamiliar, y que constan en el dictamen pericial precitado como documento nº [Nº DE DOCUMENTO].

La diferencia existente entre el valor dado a este bien en el convenio regulador y el valor real supone del orden de [FECHA] de euros.

B) INVENTARIO DE BIENES MUEBLES

3.- Tres mil participaciones sociales de treinta euros de valor nominal cada una de ellas de la entidad mercantil denominada [DENOMINACIÓN SOCIAL], domiciliada en [DOMICILIO], c/ [CALLE], con C.I.F. nº [NÚMERO], constituida en [LOCALIDAD] el [FECHA] en escritura otorgada ante el Notario D./Dña. [NOMBRE DEL NOTARIO], con el nº [NÚMERO] de su protocolo.

Titulo de adquisición y cargas: Pertenece este bien a la sociedad legal de gananciales, según se hace constar, por haberlas suscrito el demandado constante matrimonio, en la citada escritura fundacional, y que se encuentran libre de cargas. Se acompaña copia de la inscripción en el Registro Mercantil de [LOCALIDAD] (documento nº [Nº DE DOCUMENTO]), así como copia de las cuentas anuales de la mercantil correspondientes al ejercicio del año [AÑO] (documento nº [Nº DE DOCUMENTO]).

Valor dado a efectos de liquidación: El valor dado a estas participaciones sociales en la liquidación es de [IMPORTE] euros.

En relación con el valor de las participaciones sociales de [DENOMINACIÓN SOCIAL], se acompaña dictamen de valoración pericial, emitido por la empresa de auditoría y censura jurada de cuentas [DENOMINACIÓN SOCIAL], con arreglo a la que, en el período anual correspondiente al momento de realizarse la liquidación de Gananciales, al 31 de diciembre de [AÑO], ascendía a [IMPORTE] euros, siendo conforme al porcentaje de participación del esposo en la sociedad la valoración a efectos de Liquidación de [IMPORTE] euros, más de doce veces superior a la que se consignó en su momento.

A los oportunos efectos probatorios, aportamos el mencionado dictamen pericial, como documento nº [Nº DE DOCUMENTO], del que resulta una diferencia existente entre el valor concedido a este bien en el convenio regulador y el valor real que supone del orden de [IMPORTE] euros.

4.- Doscientas cincuenta participaciones sociales de seis euros de valor nominal cada una de ellas de la entidad denominada [DENOMINACIÓN SOCIAL], domiciliada en [DOMICILIO], c/ [CALLE], con C.I.F. nº [NÚMERO], constituida en [LOCALIDAD] el [FECHA] en escritura otorgada ante el Notario D./Dña. [NOMBRE DEL NOTARIO], con el nº [NÚMERO] de su protocolo.

Titulo de adquisición y cargas: Pertenece este bien a la sociedad legal de gananciales, según se hace constar, por haberlas suscrito el demandado constante matrimonio, en la citada escritura fundacional.

Se acompaña inscripción registral como documento nº [Nº DE DOCUMENTO].

Valor dado a efectos de liquidación: El valor dado a estas participaciones sociales en la liquidación es de [IMPORTE] euros.

Respecto de este bien, manifestamos nuestra conformidad con su valoración.

La mercantil se encuentra sin actividad.

5.- Ajuar doméstico, que se valora en el convenio regulador en [IMPORTE] euros.

Este valor, al contrario de los casos anteriores, resulta anormalmente elevado, puesto que se trata de una cifra caprichosa, cuya única finalidad era la de cuadrar las adjudicaciones según estaba preestablecido en una liquidación claramente lesiva para mi representada.

Debe tenerse en cuenta que, según las normas de valoración fiscal, el ajuar doméstico se valora de modo que la cantidad consignada se correspondería con valor patrimonial superior a los [IMPORTE] euros, que es prácticamente el doble que el real de los bienes partibles.

PASIVO

6.- Deudas. El convenio regulador hace constar que no hay deudas de la comunidad de bienes ganancial, y sin embargo, está ya reseñada la carga hipotecaria que gravitaba sobre el inmueble inventariado en el apartado A.1, la vivienda conyugal.

SEXTO.- Los valores reales de las adjudicaciones efectuadas a cada uno de los cónyuges, conforme a los documentos aportados y los dos dictámenes periciales que se adjuntan, de A.P.I. y de auditoría de empresas, permiten afirmar que, por evidente infravaloración de la mayoría de los bienes inventariados sobre los que se practica la liquidación de la sociedad de gananciales, se ha producido una lesión en más de la cuarta parte de los derechos adjudicados a mi patrocinada.

De todas las maneras, además se relata que hay otro inmueble ganancial omitido en el inventario del convenio regulador, que en este punto venimos a poner de manifiesto:

7.- Urbana. Piso [Nº], letra [LETRA] del bloque n° [Nº] sita en [LOCALIDAD], [LOCALIDAD] ( [PROVINCIA]), con una superficie útil de [Nº] m2. Libre de cargas.

Plaza de garaje situado en la planta sótano del bloque nº [NÚMERO] del mismo edificio, señalado con el n° [Nº].

Título: Perteneció a la sociedad de gananciales por haberse adquirido constante matrimonio. Así resulta de escritura otorgada arte el Notario de [LOCALIDAD] D./Dña. [NOMBRE Y APELLIDOS], de (documento nº [Nº DE DOCUMENTO]).

En relación con este bien, hemos de referir que el mismo no figura dentro de la liquidación practicada en el convenio regulador, siendo objeto de un acuerdo extrajudicial reservado de los esposos en el momento de la interposición de la demanda de divorcio, por el que se establecía a favor de mi mandante una cantidad fija de [IMPORTE] euros, la cual percibiría en el momento en que se realizara la venta del inmueble.

Se acompaña para su acreditación copia del acuerdo como documento nº [Nº DE DOCUMENTO].

El inmueble fue vendido con fecha [FECHA] por un valor de [IMPORTE EN LETRA] de euros, de los cuales le fue entregado a mi mandante lo pactado, y aparentemente, según el precio que se hizo figurar en el contrato público, percibió [IMPORTE] euros el demandado (se adjunta fotocopia de la escritura de compraventa de [LOCALIDAD], como documento nº [Nº DE DOCUMENTO], señalando el protocolo del Notario de D./Dña. [NOMBRE Y APELLIDOS], a los efectos del art. 265.2 LEC, por si se impugnara de adverso).

SÉPTIMO.- Los hechos relacionados no dejan lugar a duda sobre la inequívoca mala fe del demandado en la elaboración de la partición del haber ganancial, y hasta el último momento, mi poderdante ha intentado negociar una solución extrajudicial que permitiera restablecer de alguna manera aceptable la lesión patrimonial causada, sin tener que incurrir en un largo y costoso acudimiento a los Tribunales, que el demandado está en mucha mejor condición económica para soportar, frente a la escasas posibilidades de su ex esposa.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento nº [Nº DE DOCUMENTO]

El demandado, secundado por el abogado de los servicios jurídicos de la empresa de aquél, y que redactó el convenio regulador, se ha negado a cualquier solución, y habida cuenta de que la acción que se está en la forzosidad de ejercitar tiene un plazo de caducidad, nos vemos obligados a acudir al Tribunal al que honro en dirigirme.

A los anteriores hechos son de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN Y COMPETENCIA.

Radicando la competencia genérica en el orden civil de la jurisdicción, detenta la competencia objetiva y funcional la Sección Civil del Tribunal de Instancia, por aplicación de lo dispuesto en el art. 85.1º LOPJ y art. 45 LEC, y puesto que no está prevenido un fuero territorial preceptivo específico, con arreglo a lo previsto en el art. 50.1 LEC, resulta territorialmente competente el Tribunal a que me dirijo, puesto que es el del partido del lugar donde tiene su domicilio el demandado.

II.- CAPACIDAD Y LEGITIMACIÓN.

Tanto mi mandante como el demandado son personas físicas, mayores de edad, en pleno ejercicio de sus derechos civiles, por lo que tienen capacidad para ser parte y capacidad procesal ex arts. 6.1.1º y 7.1 LEC.

Corresponde la legitimación activa directa a mi mandante, ya que según el art. 10 LEC, es titular de un derecho subjetivo, por cuanto que es la parte perjudicada en la liquidación de la sociedad de gananciales que se constituyó como consecuencia de su matrimonio con el demandado, quien por dicha razón, al ser la otra parte contratante, correlativamente beneficiada, también está legitimado pasivamente.

III.- PROCEDIMIENTO.

La presente demanda deberá sustanciarse por las normas del juicio ordinario, a tenor de lo prevenido en los arts. 248 y 249.2 LEC, toda vez que el criterio de atribución preferente de la materia objeto del proceso resulta inaplicable, al carecer de especialidad típica la de éste, y cumplir entonces el criterio de cuantía, que supera los 15.000 euros.

IV.- CUANTÍA.

Cumpliendo lo prevenido en el art. 253.1 LEC, hacemos constar que la cuantía de esta demanda es de [IMPORTE] euros ([IMPORTE EN CIFRA] €), con arreglo a la regla 12ª, en relación con la regla 8ª del art. 251 LEC, puesto se trata de pleito relativo a un conjunto o masa patrimonial separada, instándose la ineficacia del título obligacional derivado de la división de copropiedad, siendo que, como se ha justificado en el fáctico, el valor de los bienes y derechos incluidos asciende a la cantidad de [IMPORTE] euros.

V.- POSTULACIÓN Y DEFENSA.

Conforme a los arts. 23 y 31 LEC se formula esta demanda a través de Procurador/a de los Tribunales con poder notarial para pleitos, y con dirección y firma de Letrado habilitado ante el Tribunal. Asimismo se cumplen los requisitos formales del art. 399 LEC.

VI.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

VII.- FONDO DE LA CUESTIÓN CONTROVERTIDA

A) Se ejercita principalmente la acción de rescisión de la partición efectuada con ocasión de la liquidación de la sociedad de gananciales del matrimonio formado por la demandante D./Dña. [NOMBRE Y APELLIDOS], y el demandado D./Dña. [NOMBRE Y APELLIDOS], por causa de lesión en más de la cuarta parte.

La actora y el demandado pusieron fin a su convivencia matrimonial mediante divorcio instado de común acuerdo, presentando el obligado convenio regulador de la separación, ello elaborado por abogado de la empresa del esposo, de la confianza de éste. En dicho convenio, en punto a la liquidación del régimen económico ganancial de su matrimonio, se formó inventario, expresó avalúo y determinó el haber líquido partible, procediéndose a una adjudicación a cada cónyuge de bienes concretos, sin asunción de deudas, que no se hacían constar. El convenio fue aprobado en la sentencia de divorcio por estimar el Tribunal que dicho convenio regulador amparaba suficientemente los intereses de los menores para la actualidad, y era muy adaptable al futuro cambio de circunstancias.

En la partición, los copartícipes que la llevan a cabo especifican y concretan en bienes y derechos la cuota abstracta que les corresponde en la titularidad del patrimonio ganancial, pues una vez producida su disolución, la sociedad de gananciales no se atomiza en tantas comunidades como bienes y derechos haya. Es el patrimonio idealmente pensado como una unidad aunque integrado por un conjunto heterogéneo de bienes, derechos y obligaciones, el que está sujeto a una cotitularidad de los cónyuges o sus herederos hasta que no finaliza el estado de indivisión con la partición. Este negocio jurídico no es una transacción (STS de 8 de marzo de 1995, Rec. 3598/1991), las partes nada discuten sobre sus derechos en la titularidad, y aceptan transformar sus cuotas en ella en titularidad sobre objetos singulares por propias conveniencias. Lo mismo que todo contrato, la partición es el resultado de un equilibrio de intereses, una composición de los mismos.

Tal y como tiene reiteradamente manifestado la jurisprudencia, a la liquidación de gananciales le resultan de aplicación las normas de rescisión de las operaciones particionales, y en concreto la del art. 1.074 CCiv, dada la genérica y omnicomprensiva remisión que efectúa el art. 1.410 CCiv, sin que a ello pueda oponérsele la exclusión que hace el art. 1291.1º y 2º CCiv, de los contratos onerosos, pues esa no es la naturaleza de la liquidación, y sin que a ello obste que haya ocurrido con ocasión de un convenio regulador de la separación matrimonial (STS de 26 de enero de 1993, Rec. 2186/1990).

Respecto de la procedencia de la acción de rescisión, y no de nulidad, la doctrina de la Sala I TS afirma que todos los vicios del consentimiento producen la nulidad, mientras que la lesión de la cuarta parte produce la acción de rescisión del consentimiento válido, libremente prestado, es decir, parte de un contrato válido en que se ha atribuido a una parte en menos lo que represente más de la cuarta parte respecto de lo atribuido a la contraria.

Por este motivo, se asevera que es indiferente para que prospere la acción de rescisión por lesión, el hecho de que la escritura de liquidación se haya otorgado, con el consentimiento de la actora, quien podía desconocer los bienes integrantes del patrimonio conyugal, la valoración real de los bienes, o ser víctima de un hipotético engaño producido por la otra parte, cuando consintió y suscribió la división de gananciales.

Tampoco puede hacerse derivar del hecho del otorgamiento de la escritura de liquidación, una renuncia a la acción de rescisión, sino que en la liquidación, cada uno de los cónyuges tiene derecho a la mitad del valor de los bienes que integran la sociedad de gananciales, y como se ha reiterado, ‘las renuncias han de ser claras y terminantes, deducidas de hechos o actuaciones de interpretación unívoca, no dudosa’.

Por lo acreditado, el valor liquido del patrimonio ganancial en el momento de su distribución ascendía a [IMPORTE] euros, en el que a la esposa le correspondía la mitad.

Como a la misma se le adjudicaron los bienes por valor de [IMPORTE] euros, percibió con una merma de lo que debía percibir de [IMPORTE] euros.

Detectada la lesión objetiva, a través de la prueba en el proceso, corresponderá determinarla en el fallo (STS de 25 de febrero de 1980), y conceder entonces al demandado el derecho de opción del art. 1.077 CCiv, entre indemnizar el daño a mi patrocinada, o consentir a que se proceda a nueva partición.

B) Según es doctrina [por ejemplo, STS de 22 de febrero de 1994 ], la omisión de algún objeto o valor de la partición, no autoriza a rescindirla por lesión, ni puede fundarse ésta en operación valorativa de contabilidad con relación a objetos que no se incluyeron en la partición.

Sin embargo, nada obsta para acumular una acción de complemento del art. 1.079 CCiv, y puesto que el inmueble a que se ha hecho referencia en el ordinal sexto salió con posterioridad a la liquidación del conjunto de gananciales, con desigualitaria asignación a cada cónyuge (mi mandante recibió una cantidad fija pactada de antemano), corresponde incluir el valor en venta del bien ganancial, por principio de subrogación real, y computar las atribuciones consolidadas del mismo por cada copartícipe.

VIII.- COSTAS.

Conforme al principio del art. 394.1 LEC, del vencimiento objetivo, las costas irrogadas a esta parte en el juicio declarativo en la primera instancia se han de pronunciar a cargo del demandado.

Por todo ello,

SUPLICO AL TRIBUNAL

que teniendo por presentado este escrito, con sus copias, documentos y pericias que se acompañan, se sirva admitir uno y otros; en su virtud tener por interpuesta en la representación que ostento la presente demanda de Juicio declarativo Ordinario contra D./Dña. [NOMBRE Y APELLIDOS], quien deberá ser emplazado en legal forma, y previos los oportunos trámites legales, en su día se sirva dictar sentencia por la que:

1°.- Se declare la rescisión de la liquidación de la sociedad de gananciales por lesión en más de la cuarta parte de los bienes adjudicados a la demandante.
2°.- Se declare la nulidad o ineficacia de las transmisiones de bienes o derechos adjudicados al demandado, en cuanto se vean afectadas por el anterior pronunciamiento.
3°.- Se determine la cuantía exacta de la lesión respecto de los bienes gananciales liquidados, a fin de que el demandado pueda ejercitar, con relación a los mismos, la opción que le confiere el artículo 1.077 del Código Civil.
4°.- Se declare la obligación de adicionar en la nueva liquidación que se practique el bien ganancial omitido, por el precio de su venta subrogado, que asciende a la cantidad deeuros.
5°.- Se condene en costas al demandado.

Es Justicia de hacerse en [LUGAR], a [FECHA].

OTROSÍ PRIMERO DIGO: Se acompañan dictámenes periciales, con arreglo a los arts. 335 y 336.1 LEC, el que hace documento nº [Nº DE DOCUMENTO], emitido por el Agente de la Propiedad Inmobiliaria D./Dña. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], calle [CALLE], y el que hace documento nº [Nº DE DOCUMENTO], elaborado por [ÓRGANO O PERSONA], empresa de auditoría y censura jurada de cuentas, con domicilio social en [LOCALIDAD], calle

OTROSÍ SEGUNDO DIGO: Que siendo general para pleitos el poder que presenta el Procurador/a suscrito, y precisándolo para otros usos.

Por lo expuesto,

AL TRIBUNAL SUPLICO que, teniendo por hechas las afirmaciones anteriores, y por presentadas pruebas periciales, se admitan y quede anunciada su proposición como prueba, así como que acuerde el desglose de la copia auténtica del poder para pleitos y la devolución a esta parte.

Es Justo en el mismo lugar y fecha arriba indicados.

Firma del Abogado/a	Firma del Procurador/a
