---
name: demanda-ordinaria-rescision-particion-hereditaria-civ-0477
description: "Demanda ordinaria de rescisión de partición hereditaria por lesión en la valoración de bienes. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda ordinaria de rescisión de partición hereditaria por lesión en la valoración de bienes

> Formulario **CIV-0477** del plugin **Herencias, testamentos y donaciones** (`formularios-herencias-y-donaciones`) · Civil › Sucesiones y donaciones · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio ordinario en ejercicio de rescisión de la partición por lesión derivada de la valoración de los bienes hereditarios cuando fueron adjudicados.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda ordinaria de rescisión de partición hereditaria por lesión en la valoración de bienes» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda ordinaria de rescisión de partición hereditaria por lesión en la valoración de bienes” para mi caso». También puedes invocarla directamente con `/formularios-herencias-y-donaciones:demanda-ordinaria-rescision-particion-hereditaria-civ-0477`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-herencias-y-donaciones:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Herencias, testamentos y donaciones) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (17 veces)
- [ ] LOCALIDAD (12 veces)
- [ ] NÚMERO (9 veces)
- [ ] IMPORTE (8 veces)
- [ ] FECHA (6 veces)
- [ ] Nº DE DOCUMENTO (6 veces)
- [ ] IMPORTE EN CIFRA (3 veces)
- [ ] DOMICILIO (2 veces)
- [ ] FINCA (2 veces)
- [ ] FOLIO (2 veces)
- [ ] LIBRO (2 veces)
- [ ] TOMO (2 veces)
- [ ] APELLIDOS
- [ ] CALLE
- [ ] COMUNIDAD AUTÓNOMA
- [ ] CORREO ELECTRÓNICO
- [ ] DENOMINACIÓN SOCIAL
- [ ] ENTIDAD BANCARIA
- [ ] FECHA DE LA ESCRITURA
- [ ] IMPORTE EN LETRA
- [ ] LUGAR
- [ ] NOMBRE DE LA FIRMA TASADORA
- [ ] Nº
- [ ] Nº DE COLEGIADO/A
- [ ] SEDE
- [ ] TELÉFONO

## Normas que cita el formulario

- art. 24.1 LEC
- art. 399.1 LEC
- art. 85.1 LOPJ
- art. 52.1.4.º LEC
- art. 23 LEC
- art. 253.1 LEC
- art. 251 LEC
- art. 5 Ley Orgánica 1/2025
- art. 399 LEC
- art. 1.074 CC
- art. 400 CC
- art. 404 CC
- art. 1.077 CC
- art. 394.1 LEC
- art. 1.077 Código Civil
- art. 335.2 LEC

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

- Junto a «…N CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] QUE POR TURNO DE REPARTO CORRESPONDA»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] QUE POR TURNO DE REPARTO CORRESPONDA

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales y de D./Dña. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], representación que acredito mediante escritura de poder otorgada a mi favor (existen tres posibilidades para otorgar el apoderamiento al Procurador de los Tribunales, conforme dispone el art. 24.1 LEC)

[OPCIONAL — opción en función de cómo se haya otorgado el poder]

[ELEGIR UNA OPCIÓN: Si el poder se otorga a través de la sede judicial electrónica / Si el poder se otorga mediante comparecencia apud acta / Si el poder se otorga ante Notario]

bajo la dirección letrada de D./Dña. [NOMBRE Y APELLIDOS], abogado/a en ejercicio, con despacho profesional abierto en [LOCALIDAD], colegiado nº [Nº DE COLEGIADO/A] del Ilustre Colegio de la Abogacía de [LOCALIDAD], ante el Tribunal comparezco y como mejor en Derecho proceda, DIGO:

Que mediante el presente escrito vengo a formular DEMANDA DE JUICIO DECLARATIVO ORDINARIO, contra D./Dña. [NOMBRE Y APELLIDOS], con domicilio, primero en [DOMICILIO]; y segundo, el domicilio laboral en [DOMICILIO]); con email [CORREO ELECTRÓNICO]; y con número de teléfono móvil [TELÉFONO]; en ejercicio de la acción que se concretará en el cuerpo del escrito y en el suplico, y todo ello de conformidad con los hechos y fundamentos de derecho que se desarrollarán a continuación.

Que esta parte asume el compromiso de recibir cualquier comunicación dirigida por la oficina judicial, durante toda la fase declarativa, e, incluso, en una eventual fase de ejecución por medios telemáticos, en términos del art. 399.1 II LEC, consignándose a estos efectos la siguiente dirección de correo electrónico y nº [Nº] de teléfono:

HECHOS

PRIMERO

Mi representada es hija de D./Dña. [NOMBRE Y APELLIDOS], y Don/Doña [NOMBRE Y APELLIDOS], habidos en el matrimonio, como lo es el demandado, D./Dña. [NOMBRE Y APELLIDOS], hermanos de doble vínculo.

Se acompañan certificados registrales de nacimiento y matrimonio, como documentos números [Nº DE DOCUMENTO] a [Nº DE DOCUMENTO].

SEGUNDO

D./Dña. [NOMBRE Y APELLIDOS] falleció viuda en [LOCALIDAD], el día [FECHA], sin que se hubiera liquidado la sociedad de gananciales, ni manifestado expresamente la herencia de D./Dña. [NOMBRE Y APELLIDOS], fallecido previamente el día [FECHA]

Se aportan certificados de defunción como documentos números [Nº DE DOCUMENTO] y [Nº DE DOCUMENTO].

TERCERO

A la muerte predicha, todo el patrimonio conocido de los padres de demandante y demandado era la vivienda unifamiliar y garaje sitos en [LOCALIDAD], que se hallaba gravada con una hipoteca pendiente de amortizar por importe de [IMPORTE] euros ([IMPORTE EN CIFRA] €).

Se acompañan certificaciones del Registro de la Propiedad de [LOCALIDAD], de la finca [FINCA], inscrita al libro [LIBRO] de [LOCALIDAD], tomo [TOMO], folio [FOLIO], y de la finca [FINCA], inscrita al libro [LIBRO] de [LOCALIDAD], tomo [TOMO], folio [FOLIO], como documentos números [Nº DE DOCUMENTO] y [Nº DE DOCUMENTO], así como certificación de la entidad financiera acreedora hipotecaria [ENTIDAD BANCARIA], como documento n.º [NÚMERO].

CUARTO

Puesto que los padres indicados de mi representada y del demandado D./Dña. [NOMBRE Y APELLIDOS] no habían otorgado testamento, mediante acta autorizada ante el Notario de [LOCALIDAD], Don/Doña [NOMBRE Y APELLIDOS], con fecha [FECHA], n.º [NÚMERO] de su protocolo, se declararon herederos abintestato por mitades iguales partes de los bienes relictos.

Se aporta copia como documento n.º 9.

QUINTO

Igualmente las dos partes, mediante escritura otorgada ante la misma Notario de [LOCALIDAD], D./Dña. [NOMBRE Y APELLIDOS], con fecha [FECHA], n.º [NÚMERO] de su protocolo acordaron la manifestación y aceptación de la herencia, y la partición de la vivienda unifamiliar y garaje mencionados, que valoraron en [IMPORTE] euros ([IMPORTE EN CIFRA] €), teniendo en cuenta la hipoteca pendiente de amortizar.

A tal efecto, y como pago de sus respectivos haberes en la disuelta comunidad hereditaria, convinieron, de una parte, adjudicar el pleno dominio del citado inmueble al demandado D./Dña. [NOMBRE Y APELLIDOS], y, de otra, abonar a la actora, mi mandante, en compensación de su cuota, la suma de [IMPORTE] euros ([IMPORTE EN CIFRA] €), explícitamente como ‘diferencia entre el valor del cincuenta por ciento de la finca y el cincuenta por ciento del importe pendiente de amortizar del préstamo en cuya garantía se constituyó la hipoteca que pesa sobre la finca’.

Se acompaña copia como documento n.º [NÚMERO].

SEXTO

Mi representada ha evidenciado más tarde la existencia de un error objetivo en la valoración de los citados inmuebles que conformaba la herencia de los padres. Resulta que el valor real de la mentada vivienda unifamiliar a la fecha en que se otorgó la escritura de partición, era muy superior al que allí se hizo figurar pues cuando menos tenía un valor de [IMPORTE] euros.

A su acreditación, se aporta informe de valoración del Departamento de Vivienda del Gobierno Autonómico de [COMUNIDAD AUTÓNOMA], como documento n.º [NÚMERO], y también dictamen pericial elaborado por el Agente de la propiedad inmobiliaria de la mercantil [DENOMINACIÓN SOCIAL] SL, que hace documento n.º [NÚMERO].

Ello supone que, descontando del mismo la carga hipotecaria existente en ese momento - euros- su valor neto era de [IMPORTE] euros, de los que la mitad correspondían a mi patrocinada, dada su cuota de participación en el caudal relicto, según reza la propia escritura. Como tan solo recibió la cantidad de [IMPORTE] euros, resulta más que evidente que sufrió una lesión en más de una cuarta parte.

SÉPTIMO

Después de numerosos intentos de solución extrajudicial, con plena información de las tasaciones efectuadas, mi representada formuló requerimiento notarial al demandado en fecha [FECHA], a fin de que se designara de mutuo acuerdo un tasador para que determinara si el desfase valorativo era tal cual se tenía detectado, o su precisa medida, sin que se recibiera contestación, por lo que se ha forzado a acudir a los tribunales.

Se aporta la carta, con su acuse de recibo, como documento n.º [NÚMERO].

A los anteriores hechos son de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

I.- PRESUPUESTOS SUBJETIVOS

I.1. JURISDICCIÓN Y COMPETENCIA

Radicando la competencia genérica en el orden civil de la jurisdicción, detenta la competencia objetiva y funcional la Sección Civil del Tribunal de Instancia, por aplicación de lo dispuesto en los arts. 85.1 LOPJ y 45 LEC, y territorialmente es competente el Tribunal a que me dirijo, puesto que está prevenido el fuero territorial preceptivo específico para los juicios sobre cuestiones hereditarias, con arreglo a lo previsto en el art. 52.1.4.º LEC, del lugar del último domicilio del finado, siendo de este partido la población en que se hallaba la residencia D./Dña. [NOMBRE Y APELLIDOS] de murió Doña María

I.2. CAPACIDAD Y LEGITIMACIÓN

Mi mandante es persona física, mayor de edad, en pleno ejercicio de sus derechos civiles, así como lo es su hermano, D./Dña. [NOMBRE Y APELLIDOS] Antonio [APELLIDOS], por lo que todos tienen capacidad para ser parte y capacidad procesal ex arts. 6.1.1.º y 7.1 LEC.

Corresponde la legitimación activa directa originaria a mi mandante, ya que es heredera que se sujetó a la partición cuya rescisión se pretende, y está legitimado pasivamente el demandado, en su condición de única otra parte en dicha partición, igualmente como coheredero.

I.3. POSTULACIÓN Y DEFENSA

Conforme a los arts. 23 y 31 LEC se formula esta demanda por medio de representación a Procurador/a de los Tribunales con poder notarial para pleitos, y bajo dirección y firma de Letrado habilitado ante el Tribunal.

II.- PRESUPUESTOS OBJETIVOS

PROCEDIMIENTO

La presente demanda deberá sustanciarse por las normas del juicio ordinario, a tenor de lo prevenido en los arts. 248 y 249.2 LEC, toda vez que ningún criterio de atribución preferente de la materia objeto del proceso resulta aplicable, y se reclama sobre una masa patrimonial cuyo valor excede, con mucho, de los 15.000 euros.

II.2. CUANTÍA

Cumpliendo lo prevenido en el art. 253.1 LEC, hacemos constar que la cuantía de esta demanda asciende a [IMPORTE] euros ( [IMPORTE EN LETRA] xx [IMPORTE] €), por aplicación de la regla 12.ª del art. 251 LEC, referida a pleitos relativos a una herencia, cuyos bienes, las fincas que se consignan en el cuerpo de este escrito, vienen valoradas en la prueba pericial acompañada.

II.3. CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

II.4. REQUISITOS FORMALES

No aparecen, aparte de los requisitos genéricos de la demanda en juicio ordinario del art. 399 LEC, otros de carácter formal cuya falta, por el tipo de acción, invalidarían el proceso para pronunciarse sobre el fondo del asunto.

III.- FONDO DEL ASUNTO

Ejercita mi patrocinada una acción de rescisión por lesión.

Dispone el art. 1.074 CCiv, dentro de los preceptos reguladores de la partición hereditaria, que podrán también ser rescindidas las particiones por causa de lesión en más de la cuarta parte, atendido el valor de las cosas cuando fueron adjudicadas.

No es el acto particional un contrato oneroso de compraventa, ni otro transaccional, sino un particular negocio jurídico dirigido a la extinción de una comunidad, a la que son aplicables no las disposiciones sobre la compraventa sino las especiales sobre la división de la cosa común, contenidas en los arts. 400 a 406 CCiv, siempre teniendo en cuenta, que doctrina y jurisprudencia reputan la naturaleza de la comunidad hereditaria, incluida la postganancialidad, como una comunidad ordinaria de los antiguos bienes comunes pertenecientes al causante, pero sin que ello signifique que a cada heredero le quede atribuida una mitad proindiviso sobre cada uno de los bienes que integran la masa en liquidación, sino que detentan una cuota ‘in abstracto’ sobre el universo patrimonial común subsistente en tanto se mantenga dicha comunidad hereditaria, y hasta que realizadas las oportunas operaciones divisorias y liquidatorias, se materialice en una parte individualizada concreta de bienes para cada uno.

Los dos hijos herederos, puesto que la vivienda que constituía la herencia era esencialmente indivisible, convinieron en adjudicar la misma a uno de ellos e indemnizar al otro con una suma de dinero, posibilidad contemplada en el art. 404 CCiv. Pero para el éxito de esta acción rescisoria no resulta relevante el hecho de que los partícipes inicialmente hayan alcanzaran un acuerdo válido y eficaz, puesto que si la sola validez del acto, implicando un consentimiento libre de vicios, impidiera corregir la lesión económica, es obvio que serían totalmente inútiles las normas legales que la acogen.

La acción de rescisión, a diferencia de la anulación, parte de la existencia de un negocio jurídico válido por reunir todos los requisitos precisos para ello, es decir, parte de la inexistencia de vicio de consentimiento (error, dolo, violencia o intimidación), siendo razón bastante para proceder a la rescisión [SSTS de 18 de mayo de 1992 ó 13 de junio de 1992, entre otras] el que exista un error en la valoración de los bienes atendido el momento de su división y adjudicación, y que se haya producido una lesión en más de una cuarta parte, esto es, un desequilibrio económico entre lo atribuido o adjudicado a cada participe en la cuantía indicada en el art. 1.074 CCiv.

El hecho de que Doña Francisca, la actora, haya suscrito y consentido la escritura de partición y la valoración que en ella se hizo constar, no implica una renuncia al ejercicio de la acción de rescisión por lesión ni tampoco vulnera la doctrina de los actos propios. Esta acción, como ya dijimos, está prevista en la ley para reparar agravios económicos sufridos en la partición y no porque exista un vicio de consentimiento en los que la llevan a cabo. La jurisprudencia ha venido entendiendo que la doctrina que prohíbe ir contra los propios actos es incompatible con el ejercicio de esta acción por rescisión, y que sólo si existe una renuncia clara, terminante o deducida de hechos o actuaciones de interpretación unívoca, como no es el caso, no sería posible ejercitar la acción de rescisión (véanse por todas, las SSTS de 6 de marzo de 2003 (rec. 2289/1997) y 17 de mayo de 2004 (rec. 1443/2000)).

Sobre la lesión en el avalúo de las fincas en cuestión, el dictamen pericial del Sr./a. es contundente, y se apoya en el informe del Departamento de Vivienda de

En cuanto a la consecuencia jurídica de la declaración de lesión en más de la cuarta parte, ineficaz la partición, se produce un derecho de opción del heredero demandado, que conforme al art. 1.077 CCiv, podrá optar entre indemnizar el daño, en dinero o en las mismas fincas que se valoraron con perjuicio de la actora, o consentir que se proceda a nueva partición. En el caso presente, siendo dos las partes del negocio particional, una perjudicada, la actora, y otra que ha percibido más de lo justo, el demandado, ambas se verán afectadas por el fallo, pero éste debe dejar a salvo la opción del segundo, como así se pide.

En el supuesto que la propiedad hereditaria adjudicada de manera ineficaz haya producido frutos o rentas, liquidando el estado posesorio, corresponderían por mitad a mi representada, de modo que se compensarán con las cuotas de amortización del préstamo hipotecario que ha satisfecho el demandado.

En fin, con arreglo al art. 38, párrafo 2.º LH, con arreglo al que no pueden ejercitarse acciones contradictorias del dominio de inmuebles o derechos reales inscritos, sin que, previamente o a la vez, se entable demanda de nulidad o cancelación de la inscripción a favor de persona o entidad determinada, se ha de pedir la rectificación de los asientos registrales de las fincas reseñadas. De aparecer inscritas a la titularidad exclusiva del demandado, deberán volver al dominio indiviso.

IV.- COSTAS

Conforme al principio del art. 394.1 LEC, del vencimiento objetivo, las costas irrogadas a esta parte en el juicio declarativo en la primera instancia se han de pronunciar a cargo del demandado.

Por todo lo expuesto,

SUPLICO AL TRIBUNAL

que teniendo por presentado este escrito, con sus copias y documentos que se acompañan, se sirva admitir uno y otros; en su virtud tener por interpuesta en la representación que ostento, la presente demanda de Juicio declarativo Ordinario contra D./Dña. [NOMBRE Y APELLIDOS], quien deberá ser emplazado a fin de que pueda contestar, si a su derecho le conviene, y previos los oportunos trámites legales, en su día dicte sentencia por la que se declare la rescisión por lesión de la partición practicada en su día en la escritura pública de fecha [FECHA DE LA ESCRITURA], otorgada ante la Notaria de [LOCALIDAD], númerode protocolo, retornando la situación de indivisión de los inmuebles que allí se describen con su terreno a la situación de indivisión precedente, librándose al Registro de la Propiedad delos oportunos mandamientos para la rectificación de los asientos, compensándose los frutos y rentas de los inmuebles con las cuotas hipotecarias pagadas por el demandado, todo ello, sin perjuicio de la opción que al demandado confiere el art. 1.077 del Código Civil, con expresa imposición de las costas procesales a la parte demandada.

Es justicia de hacerse en [LUGAR], a [FECHA].

OTROSÍ PRIMERO DIGO: Que siendo general para pleitos el poder que presenta la Procurador/a suscrita, y precisándolo para otros usos.

OTROSÍ SEGUNDO DIGO: Que se aporta el documento n.º [NÚMERO], a título de prueba pericial de tasación de inmuebles, emitido por el Agente de la Propiedad Inmobiliaria Sr./a. [NOMBRE Y APELLIDOS], de la firma especializada [NOMBRE DE LA FIRMA TASADORA], con domicilio en [LOCALIDAD], calle [CALLE], n.º [NÚMERO], y que lleva la promesa que impone el art. 335.2 LEC, articulándose en su momento procesal oportuno la solicitud de presencia del perito en acto del juicio.

Por lo expuesto,

AL TRIBUNAL SUPLICO

que, teniendo por hechas las afirmaciones anteriores, se acuerde tener por presentado dictamen pericial, y se proceda al desglose de la copia auténtica del poder para pleitos y la devolución a esta parte.

Es Justo en el mismo lugar y fecha arriba indicados.

Firma del Abogado/a	Firma del Procurador/a
