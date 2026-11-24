---
name: oposicion-embargo-ejecucion-provisional-inactividad-civ-1621
description: "Oposición al embargo en ejecución provisional por inactividad real de la empresa ejecutante. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Oposición al embargo en ejecución provisional por inactividad real de la empresa ejecutante

> Formulario **CIV-1621** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Modelo de escrito de oposición al embargo acordado en la ejecución provisional pecuniaria por inexistencia real de actividad mercantil de la ejecutante y de su solvencia, alegando insolvencia.

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Oposición al embargo en ejecución provisional por inactividad real de la empresa ejecutante» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Oposición al embargo en ejecución provisional por inactividad real de la empresa ejecutante” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:oposicion-embargo-ejecucion-provisional-inactividad-civ-1621`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (9 veces)
- [ ] IMPORTE EN LETRA (7 veces)
- [ ] NÚMERO (6 veces)
- [ ] DENOMINACIÓN SOCIAL (5 veces)
- [ ] FECHA (4 veces)
- [ ] AÑO (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] LUGAR
- [ ] SEDE
- [ ] TIPO DE SUMINISTRO

## Normas que cita el formulario

- art. 528.3 LEC
- art. 530.3 LEC
- art. 528 LEC
- art. 744.1 LEC
- art. 528.2.2.º LEC
- art. 393.3 LEC

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

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a. de los Tribunales, que actúa en nombre y representación de DISTRIBUCIONES, S.A., cuyas circunstancias constan como parte demandada en el Juicio Ordinario n.º [NÚMERO]/[AÑO], en la pieza separada de Ejecución Provisional n.º [NÚMERO]/[AÑO], comparezco y como mejor en Derecho proceda, DIGO:

Que con fecha [FECHA] se practicó diligencia de embargo en el domicilio de mi mandante, a raíz del auto de este Tribunal que despachó la ejecución provisional de [LOCALIDAD] de [LOCALIDAD] anterior, contra la que se deduce OPOSICIÓN, con arreglo al art. 528.3 LEC, planteando como medida alternativa la de consignación, sin entrega más que parcial, en la cuenta del Tribunal de todo lo adeudado conforme a la sentencia de instancia.

Se argumenta con las siguientes:

ALEGACIONES

PRIMERA.- Mi representada resultó condenada en sentencia de [FECHA] en el Juicio Ordinario de referencia, al pago a COMERCIAL [DENOMINACIÓN SOCIAL], S.L., de la cantidad de [IMPORTE] xx [IMPORTE] euros, más intereses devengados desde la interposición de la demanda al tipo legal, y costas, que ha sido recurrida en apelación, para cuyo coactivo cumplimiento está despachada la ejecución provisional, y se practicó embargo en la fecha señalada.

Inmediatamente, mi representada ha efectuado la consignación de [IMPORTE EN LETRA] ss [IMPORTE] euros, en la cuenta del Tribunal, para oponernos al embargo.

Se acompaña, como documento n.º [NÚMERO], resguardo de ingreso en la entidad bancaria depositaria.

SEGUNDA.- Esta parte reconoce una deuda de reparación para con la demandante, pero no la que exageradamente se cuantifica en la sentencia, sea dicho con el debido respeto, y en realidad que deriva de un dictamen pericial contable errado en sus bases, por lo que ha acudido a la segunda instancia, sin perjuicio de que está dispuesta a pagar, de manera definitiva, la importante cifra de [IMPORTE EN LETRA] oo [IMPORTE] euros, que se reconocen adeudar.

Se plantea, para el resto de lo consignado, un efecto paralizador del pago provisional.

La estimación tiene que basarse legalmente en la concurrencia de absoluta imposibilidad de restaurar la situación anterior a la ejecución o de compensar económicamente al ejecutado mediante el ulterior resarcimiento de daños y perjuicios en caso de ser revocada la condena (art. 528.3, párrafo 1.º LEC). Concurrente dicha condición, debe aceptarse la medida alternativa para la revocación del embargo, por ser posible y de eficacia similar a la previamente adoptada, o caso contrario, se optaría por fijar caución suficiente para responder de la demora de la ejecución (art. 530.3 LEC).

La medida alternativa de arts. 528 y 530 LEC es una disyuntiva de la caución.

Es decir, si no cabe sustituir el acto ejecutivo atacado por la oposición por otro, no prosigue la ejecución provisional sino que se sustituye por la caución que habría de responder tanto de la deuda que sería de pagar forzosamente entonces, como del retardo previsible en saldarla, es decir, se canjea el pago actual al acreedor, con paralización ejecutiva, por el pago futuro -incluido precio por demora- bajo las debidas garantías.

Y en tal sentido, una consignación es caución adecuada, según resulta de los términos expresos del art. 529.3, párrafo 2.º LEC.

TERCERA.- El sistema de la LEC parte de la inteligencia de que la ejecución pecuniaria, en sí misma, no es susceptible de originar un perjuicio de imposible reparación, por lo que no se autoriza la oposición a la ejecución en su conjunto sino sólo a actividades ejecutivas concretas. En realidad, el desplazamiento patrimonial que entraña un pago dinerario forzoso es siempre esencialmente compensable por un desplazamiento de signo contrario. Lo que quizás puede causar un perjuicio irrestañable sea una actuación sobre determinados bienes para llevarlos a la venta pública, como se deduce de que se instaure la carga de señalar por el opositor medidas alternativas, y sólo si son inviables o inefectivas, ofrecer caución.

El asunto es, ¿La imposibilidad de la ‘restitutio’ como causa autorizatoria de plantear una medida alternativa en que piensa el legislador puede tocar el capítulo de la solvencia del ejecutante?

Desde luego, unas causas que autorizarían oposición en base a la verosimilitud de un éxito, total o parcial, del recurso de apelación (que no sería algo descabellada, porque por ejemplo se prevé implícitamente como causa autorizatoria del mantenimiento de medidas cautelares a pesar de la absolución plena en el art. 744.1 LEC), o en base a las dudas sobre la solvencia del que tiene el pronunciamiento de condena a su favor, no están previstas en la norma.

Y sin embargo, ello no implica necesariamente que la absoluta insolvencia deba dejar indiferente al ejecutor.

Como se ha dicho, que se trabe un saldo bancario de mi patrocinada, que tiene líneas de crédito abiertas, para entregárselas a la acreedora, nunca originará perjuicios irreparables desde el punto de vista de que no pueda volver ‘in natura’ al patrimonio del ejecutado algo -dinero- que se extrajo coactivamente del mismo, por hipótesis, ya que el dinero en circulación es ingente, pero, en realidad, si se atiende al texto de la norma, como se habla de que la actuación ejecutiva no pueda compensarse económicamente en el caso de revocación de la sentencia, ello es algo inconcebible, en términos abstractos, puesto que siempre existe la posibilidad de cumplimiento por equivalente en dinero.

Así ello, o bien se asume una hermeneusis extremadamente restringida, según la cual el único supuesto que encajaría como viabilizador de oposición sería aquel de raros efectos colaterales o indirectos ajenos a la obligación que se ejecuta derivados de la actuación ejecutiva en la esfera jurídica del ejecutado -hipótesis de laboratorio por desaparición de la empresa como efecto indeseado de la traba, daño moral indirecto, etc -, según han pensado algunos tratadistas, o bien se entiende que, pese a no explicitarlo la ley, se debe admitir como causa de oposición la imposibilidad en concreto de una futurible compensación de los daños y perjuicios para el caso de revocación, y por ende, un juicio sobre insolvencia del ejecutante.

La ejecutoriedad de los actos administrativos asienta esa virtualidad extrema de la presunción de legitimidad en una institucional solvencia de respuesta patrimonial para cuando los Tribunales establecen la última palabra en el asunto que sea, y como el derecho al recurso, una vez legalizado, pertenece al contenido esencial de la efectiva tutela judicial, y la jurisprudencia más interesante nace de las minoritarias sentencias de apelación o casación que son revocatorias, opina esta parte que no puede dejarse con radicalidad de examinar la oposición por insolvencia de quien ejecuta provisionalmente.

Es verdad que la Exposición de Motivos de la LEC declara asumir el peligro derivado de ejecutantes insolventes, pero el ejecutor civil tiene apoyo normativo para no asumir la insolvencia probada y completa, que no es peligro sino seguridad de recobro, y que sería un supuesto de imposibilidad absoluta -en concreto, no en abstracto- de compensar el daño de que el ejecutado pierda una porción o todo su patrimonio.

CUARTA.- Ocurre que los arts. 528.3 y 530.3 LEC hablan de absoluta imposibilidad, que es más que la extrema dificultad de que se habla para la oposición a la ejecución provisional de sentencias de condena no dineraria del art. 528.2.2.º LEC y 530.2 LEC, y equivale a la prueba cumplida de la insolvencia actual y completa del ejecutante.

El trámite de la Ley no parece pensar más que en la prueba que sea exclusivamente de documentos que aporte el interesado.

Como los que obran en autos no están en la mesa del Juez, puesto que se decide en pieza separada de un proceso que ha sido elevado al Tribunal ‘ad quem’ del recurso devolutivo, se acompaña copia de documentos de la misma probanza del Juicio Ordinarios (nos. a [Nº DE DOCUMENTO]), de los que resulta que Comercial [DENOMINACIÓN SOCIAL], S.L., carece de actividad (interrogatorio de parte transcrito del soporte técnico audiovisual del juicio, n.º [NÚMERO]), y de libros de contabilidad desde hace cinco años (certificación del Registro Mercantil, n.º [NÚMERO]), puesto que tiene renunciada la prestación de suministros de [TIPO DE SUMINISTRO] (nos. y [Nº DE DOCUMENTO]), en que perseveraba intentando prestar los concurrentes con mi mandante, y el auditor censor jurado de cuentas Sr./a. [NOMBRE Y APELLIDOS], que precisamente sirvió de base técnica de la liquidación del lucro cesante de la acreedora, aclaró su dictamen pericial en el sentido de no haberse valido de cuentas oficiales de contabilidad de la sociedad limitada, puesto que se le manifestó carecía de las mismas (n.º [NÚMERO]).

Si la ejecutante deseara contraprobar su solvencia actual, deberá no sólo meramente manifestarlo, probarlo.

La cuestión es que se considera probado documentalmente la radical y plena insolvencia de la ejecutante, que es una persona jurídica sin patrimonio a la espera de una cuantiosa suma, que por el momento le corresponde en ‘status’ en cierta medida claudicante, de lo que resulta que toda medida ejecutiva que conduzca a transferirle dinero del patrimonio de la ejecutada aboca a la absoluta imposibilidad en concreto de una ulterior compensación íntegra, si se produce la claudicación del derecho, razón por la que debe admitirse la caución ofrecida y voluntariamente constituida por mi patrocinada.

QUINTA.- En cuanto a la suficiencia de la caución por consignación de efectivo, de [IMPORTE EN LETRA] ss [IMPORTE] euros abarca el 30% por encima de la cantidad por la que se despachó ejecución provisional, por principal ( [IMPORTE EN LETRA] xx [IMPORTE] euros) e intereses entonces vencidos ( [IMPORTE EN LETRA] yy [IMPORTE] euros), lo que se reputa bastante, tanto para garantizar el pago como para indemnizar la demora en verificarse, porque es dicho porcentaje el criterio del presupuesto legal para intereses y costas del art. 575.1, párrafo 1.º LEC, y porque es presumible, por el movimiento de asuntos en la Audiencia Provincial, que la solución final de la controversia en apelación no demorará más del año.

En virtud de lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito con los documentos que lo acompañan, junto con el justificante del traslado al representante procesal de la parte contraria, se sirva admitirlo, y seguido que sea el legal procedimiento, estimando la oposición a la medida concreta ejecutiva de embargo en bienes del patrimonio de DISTRIBUCIONES [DENOMINACIÓN SOCIAL], S.A., ejecutada, trabado a solicitud de COMERCIAL [DENOMINACIÓN SOCIAL], S.L., ejecutante, dicte auto que declare no haber lugar a que prosiga la ejecución provisional, y acuerde alzar el embargo, y teniéndose por ofrecida y constituida caución bastante mediante la consignación judicial de [IMPORTE EN LETRA] ss [IMPORTE] euros, se apruebe para responder del pago por la ejecutada del principal de condena de la sentencia de [FECHA], intereses legales devengados y que se devenguen, así como costas procesales irrogadas y que se irroguen, hasta resolución firme, con entrega inmediata a la parte ejecutante de [IMPORTE EN LETRA] oo [IMPORTE] euros, imponiendo las costas del presente incidente a la ejecutada, si impugnara esta oposición.

Es justicia que pido en [LUGAR], a [FECHA].

OTROSÍ DIGO: Para el supuesto de que S.S.ª, directamente, o a la luz de la eventual impugnación de la contraparte, considere que es precisa una prueba adicional contradictoria acerca de la real actividad y solvencia de Comercial [DENOMINACIÓN SOCIAL], S.L., con requerimiento documental a terceros, o testifical,

SUPLICO AL TRIBUNAL que, teniendo por causada la antecedente manifestación, se convoque a las partes, por analogía del trámite incidental del art. 393.3 LEC, a vista de juicio verbal, con lo demás que proceda en Justicia que reitero en lugar y fecha ‘ut supra’.

Firma del Abogado/a	Firma del Procurador/a

========================================================================
