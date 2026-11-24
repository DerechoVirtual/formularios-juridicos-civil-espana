---
name: demanda-anulacion-laudo-arbitral-nulidad-convenio-civ-1765
description: "Demanda de anulación de laudo arbitral por nulidad del convenio arbitral. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de anulación de laudo arbitral por nulidad del convenio arbitral

> Formulario **CIV-1765** del plugin **Mediación, MASC, arbitraje y jurisdicción voluntaria** (`formularios-mediacion-arbitraje-y-voluntaria`) · Civil › Jurisdicción voluntaria, MASC, mediación y arbitraje · normativa revisada el 24-11-2026.

## Qué es

Demanda ante la Sala de lo Civil y de lo Penal del Tribunal Superior de Justicia para ejercitar la acción de anulación de un laudo arbitral por inexistencia o invalidez del convenio arbitral (art. 41.1.a de la Ley 60/2003, de Arbitraje) y por no haberse respetado el procedimiento convenido (art. 41.1.d), típica en arbitrajes derivados de contratos de adhesión con consumidores. Debe presentarse en el plazo de dos meses desde la notificación del laudo (formulario adaptado a la reforma procesal de la LO 1/2025).

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de anulación de laudo arbitral por nulidad del convenio arbitral» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de anulación de laudo arbitral por nulidad del convenio arbitral” para mi caso». También puedes invocarla directamente con `/formularios-mediacion-arbitraje-y-voluntaria:demanda-anulacion-laudo-arbitral-nulidad-convenio-civ-1765`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-mediacion-arbitraje-y-voluntaria:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Mediación, MASC, arbitraje y jurisdicción voluntaria) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (9 veces)
- [ ] DENOMINACIÓN (5 veces)
- [ ] DENOMINACIÓN SOCIAL (5 veces)
- [ ] Nº (5 veces)
- [ ] IMPORTE (4 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] Nº DE DOCUMENTOS (3 veces)
- [ ] DOMICILIO (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL DEMANDANTE (2 veces)
- [ ] Nº DE CLÁUSULA (2 veces)
- [ ] AÑO
- [ ] COMUNIDAD AUTÓNOMA
- [ ] DENOMINACIÓN SOCIAL DE LA DEMANDADA
- [ ] DENOMINACIÓN SOCIAL DE LA EMPRESA DEMANDADA
- [ ] DÍA
- [ ] MES
- [ ] Nº DE PROCEDIMIENTO ARBITRAL
- [ ] OTROS MOTIVOS, SI LOS HUBIERA
- [ ] PRODUCTO

## Normas que cita el formulario

- art. 23 LEC
- art. 42 Ley 60/2003
- art. 41.4 Ley 60/2003
- art. 90.1 TRLGDCU
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

- Junto a «…a de Abogado: ______________________ Firma de Procurador: ______________________»: requisito de procedibilidad (art. 5 LO 1/2025): antes de demandar hay que intentar un medio adecuado de solución de controversias y acreditarlo con la demanda, salvo las materias excluidas del art. 5.2.

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

A LA SALA DE LO CIVIL Y DE LO PENAL DEL TRIBUNAL SUPERIOR DE JUSTICIA DE [COMUNIDAD AUTÓNOMA]

Don/Doña [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, en nombre y representación de [NOMBRE Y APELLIDOS DEL DEMANDANTE], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño a este escrito, comparezco ante este Tribunal y DIGO:

Que en la representación que ostento formulo demanda en ejercicio de la acción de anulación contra el laudo arbitral dictado por la Asociación de Arbitraje de [LOCALIDAD] en fecha [FECHA] en el procedimiento arbitral número [Nº DE PROCEDIMIENTO ARBITRAL], contra el demandado [DENOMINACIÓN SOCIAL DE LA EMPRESA DEMANDADA], con domicilio en [DOMICILIO], la cual fundo en los siguientes

HECHOS

PRIMERO.– Por medio de esta demanda se ejercita la acción de anulación del laudo arbitral arriba expresado, que se acompaña como documento número [Nº] de la demanda, con fundamento en los siguientes motivos: a) al amparo del artículo 41.1.a) de la Ley de Arbitraje, por inexistencia o nulidad del convenio arbitral; b) al amparo del artículo 41.1.d) de la misma Ley, por no respetarse el procedimiento arbitral convenido; c) [OTROS MOTIVOS, SI LOS HUBIERA].

En efecto, el laudo arbitral que se impugna trae causa de una inexistente relación contractual con la empresa de [SECTOR: p. ej., telefonía móvil] demandada [DENOMINACIÓN SOCIAL], tal como se expondrá seguidamente, motivo por el cual no se puede aportar el convenio arbitral por inexistente, si bien aportamos como documento número [Nº] el folleto promocional, elaborado unilateralmente por la demandada y sin firma alguna que lo autorice, en el que se ha fundado el procedimiento arbitral.

SEGUNDO.– En fecha [FECHA], mi representado recibió una carta remitida por la Asociación de Arbitraje [DENOMINACIÓN], mediante la que se le comunicaba que la empresa demandada [DENOMINACIÓN SOCIAL] había solicitado la tramitación de un procedimiento arbitral en reclamación de [IMPORTE] euros (se acompaña como documento [Nº] copia de la citada carta).

Mi representado, no teniendo ningún tipo de relación comercial con la empresa demandada [DENOMINACIÓN SOCIAL], no dio importancia a la referida carta, al considerar que podría tratarse de un error.

Es de observar que en la citada carta en ningún momento se mencionaba la posibilidad de mi representado de instar la resolución de la controversia por medio de un arbitraje de consumo.

TERCERO.– Al cabo de dos meses y, más concretamente, en fecha [FECHA], mi representado recibió un burofax remitido por la Asociación de Arbitraje [DENOMINACIÓN], notificándosele la aceptación del arbitraje por dicha asociación y adjuntándole la solicitud de arbitraje, un contrato promocional de [PRODUCTO: p. ej., terminales de telefonía móvil] con convenio arbitral y una relación de usuarios, donde figura el nombre de mi representado, con fecha de baja [FECHA], sin que conste ninguna firma que autorice el contrato (como documentos [Nº DE DOCUMENTOS] se adjunta copia de dicho burofax y los documentos que se remitieron con dicha comunicación).

CUARTO.– Tras realizar diferentes gestiones con la empresa demandada y con la empresa [DENOMINACIÓN SOCIAL DE LA EMPRESA CON LA QUE TIENE CONTRATADO EL SERVICIO], en la cual tiene el alta del servicio, se comunicó a mi mandante que el tema estaba arreglado.

Sin embargo, y de forma sorprendente, mediante carta recibida por mi representado el día [FECHA] le fue notificado el laudo arbitral ahora impugnado, dictado con fecha [FECHA] en el expediente número [Nº] por la Asociación de Arbitraje de [LOCALIDAD], por el que se declara que mi representado ha incumplido el contrato y debe satisfacer a [DENOMINACIÓN SOCIAL DE LA DEMANDADA], en concepto de daños y perjuicios causados por dicho incumplimiento, la cantidad de [IMPORTE] euros, así como el pago de las costas del procedimiento arbitral, que ascienden a [IMPORTE] euros (como documentos [Nº DE DOCUMENTOS] se adjuntan copia del laudo cuya nulidad se interesa y resguardo de notificación recibida en fecha [FECHA]).

A los anteriores hechos son de aplicación los siguientes

FUNDAMENTOS DE DERECHO PROCESAL

Jurisdicción y competencia

Es competente para conocer de la acción de anulación del laudo la Sala de lo Civil y de lo Penal del Tribunal Superior de Justicia de la Comunidad Autónoma donde aquél se hubiere dictado, según dispone el artículo 8.5 de la Ley de Arbitraje, redactado por la Ley 11/2011.

Capacidad y representación

Las partes están capacitadas para entablar la presente relación jurídico procesal conforme a los artículos 6 y siguientes de la Ley de Enjuiciamiento Civil, reuniéndose los requisitos de postulación de los artículos 23 y 31 de la LEC.

Procedimiento

De acuerdo con lo dispuesto en el artículo 42 de la Ley 60/2003, de Arbitraje, modificado por la Ley 11/2011, corresponde seguir el procedimiento por los cauces del juicio verbal, con las especialidades allí establecidas.

Plazo

Conforme a lo dispuesto en el artículo 41.4 de la Ley 60/2003, de Arbitraje, la acción de nulidad del laudo se ejercita dentro de los dos meses desde la notificación del mismo a mi representado en fecha [FECHA].

FUNDAMENTOS DE DERECHO SUSTANTIVO

Inexistencia e invalidez del convenio arbitral

FONDO DEL ASUNTO: MOTIVOS DE ANULACIÓN

El artículo 41.1 de la Ley de Arbitraje, en su apartado a), establece como causa de nulidad del laudo arbitral la inexistencia del convenio arbitral o su invalidez.

En este sentido, el folleto promocional de la empresa demandada y la relación de abonados unilateralmente reflejados en ella (documentos [Nº DE DOCUMENTOS] de los que se acompañan a la demanda) son los documentos que supuestamente contienen el convenio arbitral que ha dado origen al laudo que se impugna.

Sin embargo, en ningún momento ha sido firmado ni aceptado por mi representado, ni ha otorgado consentimiento alguno de sumisión a arbitraje, por lo que el laudo dictado es nulo de pleno derecho por la inexistencia de convenio arbitral, de conformidad con el precepto anteriormente citado.

En efecto, el supuesto convenio arbitral se incorpora al dorso del folleto promocional y no se encuentra firmado por ninguna de las partes, ni hay dato alguno del que pueda deducirse que fuera siquiera objeto de negociación alguna, y no ya aceptado, sino incluso leído, no entendiéndose, en definitiva, respaldado el convenio en cuestión por un consentimiento bilateral y cierto, ni por un asentimiento claro, preciso y determinante para ambas partes de someter sus diferencias y vicisitudes contractuales a un arbitraje ni de acatarlo; voluntad inequívoca a la que aluden para su validez, entre otras, las SSTS de 11 de diciembre de 1999, rec. 864/1995, o de 6 de febrero de 2003, rec. 1588/1997, en la que se ha declarado que «Según resulta tanto del artículo 6.2 de la Ley de Arbitraje de 1988 como del artículo 2.2 del Convenio de Nueva York sobre reconocimiento y ejecución de sentencias arbitrales extranjeras, de 10 de junio de 1958, lo decisivo para la validez del convenio arbitral no es tanto la firma de las partes o la utilización de determinadas fórmulas como la prueba de la voluntad inequívoca de las partes contractuales de someter sus controversias a arbitraje, siendo destacable en este sentido cómo la jurisprudencia más reciente de esta Sala se pronuncia en contra de las "fórmulas sacramentales" como condicionantes de la validez de las cláusulas de sumisión a arbitraje (SSTS 13 de julio de 2001, rec. 1739/1996 y 18 de marzo de 2002, rec. 2551/1996) y a favor, en cambio, del criterio respetuoso con la voluntad de las partes».

Pero, además, nos hallaríamos ante un consumidor (mi representado) que habría celebrado un contrato predispuesto en el que se incorpora el convenio arbitral, por lo que habría de concluirse en todo caso que es nulo de pleno derecho y, por tanto, debe tenerse por no puesto según la regulación establecida en el texto refundido de la Ley General para la Defensa de los Consumidores y Usuarios, aprobado por el Real Decreto Legislativo 1/2007, de 16 de noviembre, porque la cláusula no consta que haya sido negociada individualmente, pues el contrato es un impreso empleado por la empresa y en él aparece la cláusula arbitral formando parte del mismo, siendo la misma en todos los casos, por lo que reúne el carácter de condición general; la remisión al arbitraje no es obviamente a una institución pública, como son las Juntas Arbitrales de Consumo, sino a una asociación de carácter privado, y la cláusula perjudica claramente a los intereses del consumidor y el justo equilibrio de los derechos y obligaciones de las partes, y en este sentido el artículo 90.1 del TRLGDCU establece que es una cláusula abusiva y, por ello, nula de pleno derecho conforme a lo dispuesto en el artículo 83 del mismo texto legal.

Por tanto, aun cuando se hubiera dado el caso de que mi representado hubiera aceptado el convenio arbitral, que como queda demostrado en el apartado anterior no ha sido así, dicho convenio sería inválido, puesto que es evidente que la cláusula [Nº DE CLÁUSULA] del contrato promocional de [PRODUCTO] para particulares es una cláusula de adhesión, y se contiene en unas condiciones generales impuestas por el suministrador, y además dicho contrato se habría celebrado con un consumidor, por lo que, al amparo del artículo 41.1.a) de la Ley de Arbitraje, concurre la causa de nulidad del laudo arbitral, al ser inválido el convenio arbitral, si es que pudiera considerarse que existe.

Ilicitud del procedimiento arbitral

El artículo 41.1 de la Ley de Arbitraje, en su apartado d), establece como causa de anulación que el procedimiento arbitral no se haya ajustado al acuerdo de las partes.

Subsidiariamente, caso de que, en contra de lo que queda demostrado e impugnado en el anterior motivo, pudiera considerarse como existente y válido el supuesto convenio arbitral que se recoge en el documento [Nº], es indudable que el mismo establece, en la cláusula [Nº DE CLÁUSULA], una cuestión previa al inicio del arbitraje, recogiendo que «si el demandado es un consumidor, con carácter previo a iniciarse el arbitraje, le comunicará por correo certificado y le otorgará un plazo de 15 días naturales anunciando la posibilidad que tiene de iniciar el arbitraje de consumo para hacer valer sus derechos y, en el caso de que el consumidor inste el arbitraje de consumo, la Asociación de Arbitraje [DENOMINACIÓN] archivará el expediente».

Es obvio que ello no se ha cumplido, puesto que en la carta remitida a mi representado por la Asociación de Arbitraje [DENOMINACIÓN] en ningún momento se le hace referencia alguna a la posibilidad que tiene de iniciar el arbitraje de consumo para hacer valer sus derechos.

Es por ello que se ha iniciado un procedimiento arbitral contraviniendo los requisitos contenidos en el propio convenio arbitral, motivo por el cual, tanto el laudo como el procedimiento son nulos de pleno derecho, por concurrir la causa de nulidad contenida en el artículo 41.1.d) de la Ley de Arbitraje.

Costas

Al amparo del artículo 394 de la LEC, las costas deben imponerse a la parte cuyas pretensiones sean totalmente desestimadas.

Por todo lo expuesto,

SUPLICO AL TRIBUNAL: Tenga por presentado este escrito, la copia electrónica del poder notarial de representación (informática o digitalizada) y demás documentos, junto con las copias que se acompañan, a las que se dará el curso legal, lo admita, me tenga por comparecido y parte en la representación que ostento de [NOMBRE Y APELLIDOS DEL DEMANDANTE], entendiéndose conmigo las sucesivas diligencias. Y tenga por formulada demanda de juicio verbal civil en ejercicio de la acción de anulación del laudo arbitral de fecha [FECHA] dictado por la Asociación de Arbitraje [DENOMINACIÓN] contra la demandada [DENOMINACIÓN SOCIAL], cuyas demás circunstancias personales constan en el encabezamiento de este escrito, y, tras los trámites correspondientes, con celebración de vista que expresamente solicito, dicte sentencia por la que se declare la nulidad del expresado laudo arbitral, condenando a la parte demandada al pago de las costas del proceso.

OTROSÍ PRIMERO DIGO: Que intereso la devolución del poder general para pleitos por precisarlo para otro menester, quedando en los autos copia debidamente testimoniada.

OTROSÍ SEGUNDO DIGO: Que la cuantía del pleito es de [IMPORTE] euros.

OTROSÍ TERCERO DIGO: Que, de conformidad con lo establecido en el artículo 42.1 de la Ley de Arbitraje, esta parte solicita la celebración de vista, proponiendo los siguientes medios de prueba para que se practiquen en la misma:

1) DOCUMENTAL, dando por reproducidos los documentos acompañados en el escrito de demanda.

2) TESTIFICAL de D./Dª [NOMBRE Y APELLIDOS], representante de la empresa [DENOMINACIÓN SOCIAL], con la que tiene contrato mi representado, interesando que sea citado a la vista judicialmente en su domicilio sito en [DOMICILIO].

SUPLICO AL TRIBUNAL que tenga hechas las anteriores manifestaciones a los efectos legales que procedan y acuerde de conformidad.

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO]

Firma de Abogado: ______________________

Firma de Procurador: ______________________
