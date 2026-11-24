---
name: demanda-juicio-ordinario-resolver-arrendamiento-civ-0524
description: "Demanda de juicio ordinario para resolver el arrendamiento de industria y recuperar el local. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio ordinario para resolver el arrendamiento de industria y recuperar el local

> Formulario **CIV-0524** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio ordinario del arrendador de una industria o negocio en funcionamiento (local, marca, maquinaria, mobiliario y clientela) contra la arrendataria que no devuelve la posesión al expirar el plazo pactado: solicita declarar extinguido el contrato, recuperar el local y todos los elementos materiales e inmateriales del negocio, y reclamar las rentas que se devenguen hasta el efectivo desalojo (arts. 1.542 y ss. y 1.569.1.ª CC).

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio ordinario para resolver el arrendamiento de industria y recuperar el local» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio ordinario para resolver el arrendamiento de industria y recuperar el local” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:demanda-juicio-ordinario-resolver-arrendamiento-civ-0524`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº DE DOCUMENTO (9 veces)
- [ ] FECHA (5 veces)
- [ ] Nº DE ANEXO (4 veces)
- [ ] FECHA DE EXPIRACIÓN (3 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] DENOMINACIÓN SOCIAL DE LA ARRENDATARIA (2 veces)
- [ ] FECHA DEL CONTRATO (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] PLAZO (2 veces)
- [ ] ACTIVIDAD: POR EJEMPLO, LA REPARACIÓN DE AUTOMÓVILES
- [ ] ANTELACIÓN
- [ ] AÑO
- [ ] CORREO ELECTRÓNICO
- [ ] DENOMINACIÓN SOCIAL DE LA ARRENDADORA
- [ ] DIRECCIÓN DEL LOCAL
- [ ] DOMICILIO
- [ ] DÍA
- [ ] FECHAS
- [ ] MARCA
- [ ] MES
- [ ] NOMBRE Y APELLIDOS DEL LETRADO/A
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] Nº DE DOCUMENTOS
- [ ] ORDEN: PRIMER
- [ ] PROVINCIA
- [ ] SEDE
- [ ] TELÉFONO

## Normas que cita el formulario

- art. 399.1 LEC
- art. 85 LOPJ
- art. 51.1 LEC
- art. 52.1.7.º LEC
- art. 6.1.3.º LEC
- art. 7.4 LEC
- art. 253 LEC
- art. 251.9.ª LEC
- art. 250.1.1.º LEC
- art. 249.2 LEC
- art. 23 LEC
- art. 5 Ley Orgánica 1/2025
- art. 1.569.1.ª CC
- art. 1.566 CC
- art. 219 LEC
- art. 63.2 CC
- art. 394 LEC
- art. 50 LEC

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

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, en nombre y representación de la entidad [DENOMINACIÓN SOCIAL DE LA ARRENDADORA], según acredito mediante escritura de poder inscrita en el Registro Electrónico de Apoderamientos Judiciales, a cuya justificación aporto certificación de dicho Registro que acompaño como documento n.º [Nº DE DOCUMENTO], dirigida por el/la Letrado/a abajo firmante D./Dña. [NOMBRE Y APELLIDOS DEL LETRADO/A], con despacho profesional en [LOCALIDAD], ante el Tribunal comparezco y, como mejor proceda en Derecho, DIGO:

Que, en la representación que ostento, interpongo demanda de juicio declarativo ordinario sobre desahucio de arrendamiento de industria, resolución de contrato, restitución de posesión y otros particulares contra la entidad [DENOMINACIÓN SOCIAL DE LA ARRENDATARIA], con domicilio en [LOCALIDAD], calle [DOMICILIO].

Que esta parte asume el compromiso de recibir cualquier comunicación dirigida por la oficina judicial, durante toda la fase declarativa e, incluso, en una eventual fase de ejecución, por medios telemáticos, en los términos del art. 399.1, párrafo segundo, LEC, consignándose a estos efectos la siguiente dirección de correo electrónico y n.º de teléfono: [CORREO ELECTRÓNICO] / [TELÉFONO].

Fundamento la misma en los siguientes hechos y consideraciones jurídicas:

HECHOS

PRIMERO.- Mi mandante es una entidad dedicada a [ACTIVIDAD: POR EJEMPLO, LA REPARACIÓN DE AUTOMÓVILES] que ha puesto en marcha [NÚMERO] establecimientos en la provincia de [PROVINCIA] y alrededores, habiendo procedido a alquilar [NÚMERO] de ellos a diversas mercantiles, en la modalidad de arrendamiento de industria, una vez que el negocio se encontraba en funcionamiento. Se aporta copia de los estatutos sociales como documento n.º [Nº DE DOCUMENTO], en el que se puede observar el objeto social de la actora, y, como documento n.º [Nº DE DOCUMENTO], relación de establecimientos con indicación de si están arrendados o no y la fecha del respectivo contrato.

SEGUNDO.- En el presente caso, se trata del [ORDEN: PRIMER] establecimiento arrendado mediante contrato de fecha [FECHA], por un plazo de [PLAZO], extremo este último que se ha venido repitiendo en los arrendamientos posteriores. Tal y como se puede observar en la copia del contrato que se acompaña como documento n.º [Nº DE DOCUMENTO], se arrendó, con una renta mensual de [IMPORTE] euros, tanto el inmueble sito en [DIRECCIÓN DEL LOCAL], como la marca "[MARCA]" inscrita a favor de mi mandante, las máquinas relacionadas en el anexo n.º [Nº DE ANEXO], el mobiliario inventariado en el anexo n.º [Nº DE ANEXO] y la clientela generada en el tiempo que el negocio llevaba en funcionamiento. Como anexos n.º [Nº DE ANEXO] y [Nº DE ANEXO] del mismo contrato se aportan copias de las correspondientes inscripciones registrales del inmueble y de la marca.

TERCERO.- Si bien las rentas pactadas se han venido abonando con regularidad, el plazo fijado para el arrendamiento ha transcurrido sin que exista acuerdo entre mi mandante y la parte arrendataria para continuar con la relación contractual, puesto que no existe consenso sobre la renta a fijar para los próximos años, a pesar de diversas negociaciones mantenidas al efecto.

CUARTO.- A pesar de ello, la parte aquí demandada se niega a devolver la posesión del negocio, manteniéndose en las instalaciones y continuando con la actividad en marcha. Por ello, con fecha [FECHA], más de un mes antes de terminar el plazo en su día pactado, se envió burofax a la parte arrendataria comunicando la intención de no continuar con la relación contractual e interesando el desalojo del local y la devolución consiguiente de todos los elementos del negocio. Se aporta copia de la referida comunicación como documento n.º [Nº DE DOCUMENTO], frente a la cual no se ha obtenido respuesta alguna hasta la fecha.

Interesa a esta parte actora manifestar que, previamente a la presentación de la presente demanda, se han llevado a cabo negociaciones con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria, incluyéndose entre las acciones realizadas el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución.

Se adjuntan como prueba copias de las comunicaciones enviadas y recibidas durante el proceso de negociación, incluidas cartas, correos electrónicos y/o actas de reuniones, como documentos números [Nº DE DOCUMENTOS].

Finalmente, mi representada envió un requerimiento fehaciente a la demandada con fecha [FECHA], fijando un plazo de 30 días naturales para llegar a un acuerdo amistoso, a través del abogado que firma este escrito, el cual fue contestado por la demandada por el mismo medio, rechazando el acuerdo, viéndonos en la necesidad de acudir a la presente vía judicial.

Acompaño como documento n.º [Nº DE DOCUMENTO] el requerimiento efectuado y como documento n.º [Nº DE DOCUMENTO] la contestación de la demandada.

A los anteriores hechos son aplicables los siguientes

FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN Y COMPETENCIA

En cuanto a la competencia objetiva, los arts. 85 LOPJ y 45 LEC designan a las secciones civiles de los tribunales de instancia como los órganos con la competencia específica, objetiva y funcional para resolver estos pleitos.

Asimismo, el Tribunal al que tengo el honor de dirigirme es competente territorialmente, pues a su partido judicial corresponde el domicilio de la demandada, conforme al art. 51.1 LEC, sin perjuicio de que también en el mismo se encuentre el negocio y el inmueble objeto del arrendamiento que se trata de resolver, según el art. 52.1.7.º LEC.

II.- CAPACIDAD

Al tratarse de sociedades mercantiles, su capacidad se reconoce en el art. 6.1.3.º LEC, derivándose su personalidad de su constitución en escritura pública inscrita en el Registro Mercantil, con la necesidad de comparecer en juicio por medio de sus representantes legales (art. 7.4 LEC).

III.- LEGITIMACIÓN

Corresponde a mi cliente la activa por ser parte arrendadora en el contrato suscrito, y la pasiva la tiene la demandada en cuanto ocupa la posición de arrendataria que no tiene derecho a continuar en la posesión al haberse cumplido el plazo pactado.

IV.- CUANTÍA Y PROCEDIMIENTO

Conforme al art. 253 LEC, cifro la cuantía de la presente demanda en [IMPORTE] euros, correspondiente a una anualidad de renta, según dispone el art. 251.9.ª LEC.

Asimismo, tratándose de una resolución de contrato de arrendamiento en el que se cede un negocio, y no el mero uso de un local, no entra en juego la aplicación de la norma prevista en el art. 250.1.1.º LEC, que remite al juicio verbal, tal y como disponen la sentencia de la Audiencia Provincial de Barcelona de 30 de octubre de 2008, rec. 214/2008, y la sentencia de la Audiencia Provincial de Valencia de 11 de noviembre de 2011, rec. 578/2011. En esta misma línea, la sentencia de la Audiencia Provincial de Asturias de 22 de abril de 2008, rec. 367/2007, señala que "en estos arrendamientos lo determinante es el negocio o industria instalada en las dependencias arrendadas. Por ello y puesto que en la demanda la cuantía se fijó en seis mil euros el procedimiento adecuado sería el ordinario que es, además, el que debe seguirse en caso de duda pues ofrece mayores garantías, según ha mantenido reiterada Jurisprudencia (S. 14.10.89, 10.01.90, 18.06.91, 10.10.91 etc.)".

Por todo ello, el procedimiento ajustado a derecho será el del juicio declarativo ordinario regulado en los arts. 399 a 436 de la misma Ley, atendiendo a la cuantía fijada, en aplicación de lo dispuesto en el art. 249.2 LEC.

V.- POSTULACIÓN Y DEFENSA

Conforme a lo previsto en los arts. 23 y 31 LEC, se presenta la demanda por medio de Procurador/a legalmente habilitado/a y bajo dirección del Letrado firmante de la misma.

VI.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4.º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

VII.- FONDO DE LA CUESTIÓN CONTROVERTIDA

A) Acciones ejercitadas:

En esta demanda se acumulan diversas acciones, al amparo de lo dispuesto en los arts. 71 y ss. LEC, en cuanto tienen su origen en el mismo incumplimiento contractual, se dirigen contra la misma demandada y no son incompatibles.

Las acciones que se ejercitan son las siguientes: a) principalmente, la acción de desahucio por expiración del término para resolver el contrato de arrendamiento de industria de fecha [FECHA DEL CONTRATO], al haber expirado el plazo concertado, con correlativa recuperación de la posesión del negocio; y, derivada de ella, b) acción de reclamación de cantidad al amparo de las disposiciones generales sobre contratación y arrendamiento de industria, arts. 1.089 y ss. y 1.542 y ss. CC, reclamando las rentas que se devenguen durante el procedimiento en marcha, con reserva de la eventual indemnización por los daños y perjuicios causados.

B) Del arrendamiento de industria:

Como se ha indicado, nos encontramos ante un arrendamiento de industria, que supera el esquema tradicional del arrendamiento de local de negocio, al haberse cedido el uso, como consta en el contrato aportado, del propio inmueble, mobiliario, máquinas, marca registrada y de la clientela generada. Extremos todos ellos tenidos en cuenta para fijar la renta que se ha venido cobrando durante la vigencia del contrato. Realidad que se encuadra en la definición clásica de aquél como un modelo de contrato mediante el cual un empresario o profesional alquila la explotación de su empresa a otro empresario o profesional, produciéndose una cesión del uso de los elementos productivos de una empresa por un tiempo determinado. Es un contrato de alquiler en el cual el objeto del mismo es un conjunto de elementos industriales o empresariales que conforman una empresa y que el empresario propietario de los mismos (el arrendador) cede a otro empresario para que los explote (el arrendatario).

Al respecto, la sentencia del Tribunal Supremo de 25 de marzo de 2011, rec. 1904/2007, con cita de la sentencia del mismo Tribunal de 18 de marzo de 2009, rec. 665/2003, declara: "Según destacada doctrina científica no cabe confundir el arrendamiento de un local de negocio para que el arrendatario establezca su propio negocio, con el de negocio en funcionamiento, pues aquí se alquilan una serie de elementos -la empresa, las instalaciones, la clientela, etc.-, entre los que se encuentra el local, que ha de quedar fuera de la Ley arrendaticia, toda vez que, como dice el Texto Refundido de la Ley de 1964, donde la exclusión es tajante, lo que se alquila es "una unidad patrimonial con vida propia y susceptible inmediatamente de ser explotada o pendiente de meras formalidades administrativas". Aunque algunos autores han manifestado la integración de los arrendamientos de industria el régimen de la presente Ley, pues si el legislador lo hubiera querido, debió determinar la exclusión de forma expresa, como en el Texto Refundido de 1964; pero no obstante esta observación, de la interpretación del artículo 3 de la Ley de 1994 se desprende que no cabe equiparar el arrendamiento para una actividad industrial, que crea el arrendatario en el local objeto de la locación, con el hecho de arrendar una industria en pleno funcionamiento y con los elementos precisos para ello".

En este mismo sentido, la sentencia del Tribunal Supremo de 7 de julio de 2006, rec. 4040/1999, con cita de la sentencia de 21 de febrero de 2000, rec. 1548/1995, y de una clásica doctrina jurisprudencial, razona que "la doctrina de esta Sala relativa a la distinción entre los arriendos de local de negocio y los de industria es absolutamente diáfana, destacando que mientras en los primeros se cede el elemento inmobiliario, es decir, un espacio construido y apto para que en él se explote el negocio, en los segundos el objeto contractual está determinado por una doble composición integradora, por un lado el local, como soporte material y, por otro, el negocio o empresa instalada y que se desarrolla en el mismo, con los elementos necesarios para su explotación, conformando un todo patrimonial. En este sentido cabe citar las sentencias de 13 y 21 de diciembre de 1990, 20 de septiembre de 1991, 19 y 25 de mayo de 1992, 17 de abril y 10 de mayo de 1993, 22 de noviembre de 1994 y 8 de junio de 1998, entre otras". En parecidos términos, la sentencia de 8 de junio de 1998 afirma que "la jurisprudencia mantenida de esta Sala de Casación Civil viene proclamando que los arriendos de locales para negocio se diferencian de los propios de industria, en que en los primeros lo que se cede es el elemento inmobiliario, en cambio, en los segundos (arrendamientos especiales), el objeto contractual está determinado por una doble composición integradora; por un lado, el local, como soporte material y, por otro, el negocio o empresa instalada y que se desarrolla en el mismo, con los elementos necesarios para su explotación, conformando un todo patrimonial autónomo, sin que sea preciso que el arrendador aporte necesariamente todos los enseres y menajes para la comercialización de la actividad negocial a desarrollar, pues pueden ser ampliados o mejorados con los que aporte el arrendatario, incluso ser sustituidos, sin que ello afecte a la calificación y naturaleza del contrato como de locación industrial (sentencias de 20 de septiembre de 1991, 19 de mayo de 1992, 17 de abril de 1993, 10 de mayo de 1993 y 22 de noviembre de 1994)", y la sentencia de 25 de abril de 1997 considera existente un arrendamiento de industria en cuanto "se cedió todo lo necesario para el funcionamiento inmediato del negocio, a lo que nada afectan las adquisiciones posteriores por razones de utilidad o conveniencia, pues es el uso de la industria ya instalada, con elementos coordinados para su inmediata puesta en marcha, lo que constituye, según reiterada y constante doctrina de esta Sala, la unidad patrimonial con vida propia determinante del concepto jurídico de industria susceptible de ser inmediatamente explotada o pendiente para serlos de meras formalidades administrativas; y nada importa que el anexo con inventario se perdiese o que, realmente no llegase en el caso concreto a levantarse, porque sí hay supuestos en que se le dio gran transcendencia, según las pruebas practicadas, puede no tenerla en otros, dado que, cual señala la sentencia de 13 de diciembre de 1990, la suficiencia o insuficiencia de los elementos trasmitidos será una simple cuestión de hecho, a menudo de carácter técnico, pero siempre de libre apreciación de los Tribunales de instancia, que, cual señala la sentencia de 8 de julio de 1986, obtienen la calificación de arrendamiento como de industria de los presupuestos fácticos obrantes en el proceso y ello constituye materia no revisable en casación, que sólo tiene por objeto el confrontar si, dados unos hechos que han quedado incólumes, las consecuencias jurídicas obtenidas son las adecuadas según el ordenamiento jurídico".

C) De la normativa aplicable:

En consecuencia, tratándose, sin género de dudas, de un arrendamiento de industria, debe acudirse a la normativa prevista en el Código Civil, en sus arts. 1.542 a 1.574, sin que pueda entrar en juego la normativa especial de la Ley de Arrendamientos Urbanos, aplicable a los arrendamientos de inmuebles, sin más, con distinción entre viviendas y usos distintos al de vivienda. Es decir, la mencionada legislación especial no hace referencia expresa al arrendamiento de industria, por lo que no resultaría procedente, en ningún caso, una interpretación amplia en la idea de que, implícitamente, los incluye, dado que la Ley abarca lo que prevé expresamente, refiriéndose en todo caso a fincas urbanas, dejando la regulación del arrendamiento cuestionado en manos de quien ya lo tenía, la legislación civil común.

Sobre la cuestión se ha pronunciado el Tribunal Supremo de manera pacífica, siendo un claro exponente de tal doctrina su sentencia de 18 de marzo de 2009, rec. 665/2003, con cita de la sentencia de 16 de enero de 1987. Se indica que los arrendamientos de industria se encuentran excluidos de la Ley de Arrendamientos Urbanos y, por ende, no son susceptibles para el ejercicio de la acción de retracto, con recuerdo de una línea jurisprudencial clásica de la que son ejemplos las sentencias de 7 de diciembre de 1953, 30 de enero de 1956, 12 de junio de 1967, 17 de marzo de 1970, 23 de diciembre de 1978, 21 de mayo de 1984, 16 de enero de 1987, 6 de marzo de 1987, 30 de septiembre de 1991 y 22 de abril de 1992. Se concluye en la indicada resolución que el arrendamiento de industria queda sometido a la disciplina del Código Civil, y que la doctrina jurisprudencial indicada, aunque se refiere a la Ley de Arrendamientos Urbanos de 1964, es extrapolable a la vigente ley de 1994, la cual no resulta de aplicación.

D) De la expiración del término:

Por ello, entra en juego lo dispuesto en el art. 1.569.1.ª CC, que permite al arrendador desahuciar judicialmente al arrendatario cuando expire el término convencional. En el presente caso, el contrato de fecha [FECHA DEL CONTRATO] recogió un plazo pactado de [PLAZO], que expiró el pasado [FECHA DE EXPIRACIÓN], sin que resulte aplicable la tácita reconducción del art. 1.566 CC, al haber precedido requerimiento extrajudicial para el desalojo y devolución del negocio por parte de mi mandante con [ANTELACIÓN] de antelación a la referida fecha y, desde luego, no haber consentido en ningún caso la continuación durante el plazo de quince días señalado legalmente. Y así, independientemente de que han existido negociaciones para continuar con el arrendamiento, al no fructificar las mismas ha quedado clara y evidente la voluntad del propietario del negocio de recuperar el mismo y no continuar con la cesión de su uso.

E) De los efectos de la resolución contractual:

Procede, por todo ello, declarar la resolución del contrato por expiración del término, a fecha [FECHA DE EXPIRACIÓN]; condenando a la entidad demandada a devolver a mi cliente el negocio arrendado, dejando libres y expeditos los locales y a disposición de la actora, así como la explotación de la industria, cesando en las actividades de la misma, con devolución de elementos, maquinaria, enseres y herramientas que quedaron comprendidas en el arrendamiento, según los anexos del contrato, adjuntados al documento n.º [Nº DE DOCUMENTO] de la demanda.

Asimismo, y dado que en el momento de redacción de la presente demanda han transcurrido [NÚMERO] días desde la indicada fecha sin devolución de la posesión, y que es previsible que la parte demandada continúe en la misma situación durante el transcurso del procedimiento, que se condene a la misma a abonar las rentas pactadas que se vayan generando hasta que se verifique el desalojo, haciendo expresa reserva de la reclamación respecto a los daños y perjuicios que se puedan ocasionar, tanto por daño emergente como por lucro cesante, que no se pueden concretar en la presente sede, al carecer de las bases de liquidación que exige el art. 219 LEC, dado que se desconoce la fecha concreta en la que se devolverá la posesión interesada, momento en el cual podrán calcularse aquéllos.

F) Intereses:

Citamos los arts. 1.100, 1.101, 1.108 y 1.109 CC y el art. 63.2 CCom sobre pago de los intereses moratorios a partir de la interpelación judicial.

VIII.- COSTAS

Conforme al art. 394 LEC, las costas han de imponerse a la demandada.

Por lo expuesto,

SUPLICO AL TRIBUNAL.

Que, habiendo por presentado este escrito de demanda con los documentos que lo acompañan y copias de uno y otros, los admita y me tenga por comparecido/a y parte en la representación que ostento y que acreditada dejo; y por promovido juicio declarativo ordinario frente a [DENOMINACIÓN SOCIAL DE LA ARRENDATARIA], acuerde dar traslado a la demandada para que comparezca y la conteste, y, previos los trámites legales y recibimiento a prueba que desde ahora se interesa, se dicte en su día sentencia por la que, estimando la demanda, declare:

1.º) Que el contrato de arrendamiento de industria otorgado por las partes en [FECHA], expiró el día [FECHA DE EXPIRACIÓN], a partir de cuya fecha la demandada viene detentando los locales y la industria que fueron objeto del arrendamiento.

2.º) Que, consecuentemente, condene a la entidad demandada a devolver a mi cliente el negocio arrendado, dejando libres y expeditos los locales y a disposición de la actora, así como la explotación de la industria, cesando en las actividades de la misma, con devolución de elementos, maquinaria, enseres y herramientas que quedaron comprendidas en el arrendamiento, según los anexos del contrato, adjuntados al documento n.º [Nº DE DOCUMENTO] de la demanda.

3.º) Que la demandada ha incurrido en mora desde el [FECHA], al no devolver a la actora todo lo arrendado, que retiene como precarista, siendo responsable de los daños y perjuicios causados, tanto por daño emergente como por lucro cesante, que se determinarán en período probatorio o en ejecución de sentencia, así como de las rentas pactadas que se devenguen hasta la efectiva devolución de la posesión.

Todo ello con imposición de las costas del juicio a la parte demandada.

Es justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Abogado/a Firma del Procurador/a

NOTAS EXPLICATIVAS (suprimir antes de presentar el escrito):

En el modelo se opta por acudir a la vía de la expiración del plazo, y no la de falta de pago de la renta (las dos causas habituales de resolución), puesto que lo común en este tipo de casos es que se pague la renta y se quiera seguir con el negocio arrendado (que da beneficios), cuando la propietaria-arrendadora busca un nuevo contrato con una renta más alta, una vez que se cumple el término pactado.

La cuestión del procedimiento está resuelta: es juicio ordinario (aunque hay jurisprudencia antigua de Audiencias Provinciales que acudía al verbal); y la normativa aplicable es el Código Civil. La única duda es la competencia territorial. El art. 52.1.7.º LEC habla del Tribunal donde radique la finca, pero pareciera que, con el mismo criterio de no acudir al juicio verbal, se entiende que no es aplicable al procedimiento para resolver el arrendamiento de industria (en atención a esa mayor complejidad de arrendar un negocio, frente al arriendo de un bien inmueble, que es a lo que se refiere el precepto). En cuyo caso quedarían las cláusulas generales de los arts. 50 y 51 LEC y el domicilio del demandado. En cualquier caso, se hacen coincidir los dos en el supuesto (lo que acontecerá en la mayoría de los casos, en los que la demandada, si es persona jurídica, hace constar su domicilio en el mismo lugar que tiene el negocio).

Por último, se incluye reclamación de cantidad por las rentas que se vayan generando, que podrá utilizarse para reclamar todo lo que se adeude en cada caso concreto, siempre con el límite de poder fijar las bases de liquidación del art. 219 LEC y, si no, con reserva de acciones, como se hace constar.
