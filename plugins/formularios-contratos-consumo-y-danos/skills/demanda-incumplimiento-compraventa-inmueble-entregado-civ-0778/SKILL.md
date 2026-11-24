---
name: demanda-incumplimiento-compraventa-inmueble-entregado-civ-0778
description: "Demanda por incumplimiento de compraventa de inmueble entregado con menor cabida de la pactada. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda por incumplimiento de compraventa de inmueble entregado con menor cabida de la pactada

> Formulario **CIV-0778** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio ordinario ejercitando acción de incumplimiento contractual en compraventa de vivienda por menor cabida real de la pactada en contrato

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda por incumplimiento de compraventa de inmueble entregado con menor cabida de la pactada» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda por incumplimiento de compraventa de inmueble entregado con menor cabida de la pactada” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:demanda-incumplimiento-compraventa-inmueble-entregado-civ-0778`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (8 veces)
- [ ] IMPORTE (6 veces)
- [ ] Nº DE DOCUMENTO (6 veces)
- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] FECHA (3 veces)
- [ ] FECHAS (2 veces)
- [ ] PARTE DEMANDADA (2 veces)
- [ ] CALLE
- [ ] COLEGIO
- [ ] DENOMINACIÓN SOCIAL
- [ ] DESCRIPCIÓN DEL BIEN
- [ ] FOLIO
- [ ] LIBRO
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] PORCENTAJE
- [ ] SEDE
- [ ] SUCURSAL
- [ ] TOMO

## Normas que cita el formulario

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
- art. 403.1 LEC
- art. 253.1 LEC
- art. 251.1.ª LEC
- art. 5 Ley Orgánica 1/2025
- art. 1461 CC
- art. 1124 CC
- art. 1101 CC
- art. 1469 Código Civil
- art. 1101 Código Civil
- art. 1469 CC
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

### Avisos de actualización (2) — se aplican en el texto, nunca se copian en el documento

- Junto a «…NCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE] Q.P.T.R.C.»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.

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

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE] Q.P.T.R.C.

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS], como acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], y con la asistencia del Letrado D./Dña. [NOMBRE Y APELLIDOS], del Ilustre Colegio de Abogados de [COLEGIO], cuyo despacho está abierto en esta población, calle [CALLE], ante la Sección Civil del Tribunal de Instancia que por turno de reparto corresponda, comparezco y, como mejor proceda en Derecho, DIGO:

Que siguiendo expresas instrucciones de quien ostento representación, por medio del presente escrito formulo DEMANDA DE JUICIO ORDINARIO, que dirijo contra [PARTE DEMANDADA], para ser citada en su oficina de [SUCURSAL], calle

La demanda se basa en los siguientes

HECHOS

PRIMERO.- Mi mandante y la demandada, suscribieron en documento privado de fecha [FECHA], que se aporta como documento número [Nº DE DOCUMENTO], la compraventa del inmueble sito en

El contrato de compraventa se concertó sobre planos, que fueron entregados por la vendedora, en los que figuraba una superficie de [Nº] metros cuadrados.

Finalizada la construcción, dicha compraventa se elevó a escritura pública, practicándose la oportuna inscripción en el Registro de la Propiedad de [LOCALIDAD], al tomo [TOMO], folio [FOLIO], del libro [LIBRO], con fecha

Se acompaña copia simple de la escritura de compraventa y del plano, y nota simple registral acreditativa de la superficie de la vivienda como documentos números

SEGUNDO.- El precio de la compraventa quedó fijado en la cantidad de [IMPORTE] euros, de los cuales [IMPORTE] euros se entregaron a la firma del contrato. El resto del precio, ascendente a la suma de [IMPORTE] euros, quedó aplazado para ser satisfecho en el momento de otorgamiento de la escritura, tal y como resulta de la copia simple de la escritura que se acompaña con la demanda.

TERCERO.- Posteriormente, una vez tomada posesión de la vivienda, mi representado pudo constatar que de los [Nº] metros cuadrados pactados, la vivienda adquirida únicamente constaba de [Nº] metros cuadrados, esto es, [Nº] metros cuadrados menos de los concertados; concretamente el comedor tenía que tener [Nº] metros cuadrados útiles, siendo que en realidad únicamente cuenta con [Nº] metros cuadrados, lo que supone una merma en la pieza principal de la vivienda de más de [Nº] metros.

CUARTO.- Habida cuenta que mi representado ha satisfecho en su integridad el precio fijado para la venta, y la sociedad vendedora no cumplido la obligación de entrega en la forma pactada en el contrato de compraventa, es por lo que solicita, en concepto de indemnización, que el mismo se reajuste o se disminuya de manera proporcional a juicio de peritos, que da lugar a una rebaja o disminución del [PORCENTAJE] % del precio abonado por su compra.

Se acompaña como documento número [Nº DE DOCUMENTO] dictamen pericial de la sociedad de tasación inmobiliaria [DENOMINACIÓN SOCIAL], suscrito por el Arquitecto Técnico D./Dña. [NOMBRE Y APELLIDOS], del que resulta que el precio de dichos [Nº] metros cuadrados es de [IMPORTE] euros, que se reclaman en la presente demanda.

QUINTO.- A pesar de las gestiones amistosas realizadas extrajudicialmente por mi mandante para resolver el problema derivado del incumplimiento de sus obligaciones por la vendedora, ello no ha sido posible, y es preciso impetrar el auxilio judicial, lo que, efectivamente, se hace por medio del presente escrito.

Se acreditan estos extremos con los documentos números [Nº DE DOCUMENTO] y [Nº DE DOCUMENTO] acreditativos del requerimiento efectuado por burofax a [NOMBRE Y APELLIDOS], y la entrega de dicho requerimiento en su domicilio con fecha [FECHA] del presente año.

A los anteriores hechos son de aplicación los siguientes:

SEXTO.- Interesa a esta parte destacar que, previamente a la presentación de la presente solicitud, se llevaron a cabo diversos esfuerzos de negociación con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad, y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria.

Entre las acciones realizadas, se incluyen el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución; así como la participación en reuniones llevadas a cabo los días [FECHAS], cuyos objetivos fueron buscar una conciliación respecto de las diferencias planteadas.

Se adjuntan como prueba copias de las comunicaciones enviadas y recibidas durante el proceso de negociación, incluidas cartas, correos electrónicos y/o actas de reuniones como documentos números [Nº DE DOCUMENTO].

FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN Y COMPETENCIA.

Con arreglo a los preceptos que se contienen en el art. 117 de la Constitución, art. 21 LOPJ y art. 36 LEC, la jurisdicción ordinaria del Reino de España es la única competente para conocer de los negocios o demandas civiles que se susciten en territorio español entre españoles, además de que los órganos jurisdiccionales son los competentes en defecto de sumisión expresa o tácita y aunque el demandado no tuviera su domicilio en España, en materia de obligaciones contractuales, cuando la obligación objeto de la demanda se haya cumplido o deba cumplirse en España [art. 22 quinquies.a) LOPJ].

El conocimiento del litigio pertenece a la materia del orden jurisdiccional civil (art. 9.2 LOPJ), y le corresponde la competencia específica objetiva a los Tribunales de Instancia, en cuanto por disposición legal expresa no viene atribuido a otros Tribunales (art. 85.1 LOPJ y art. 45 LEC).

Corresponde el conocimiento del juicio a la Sección Civil del Tribunal de Instancia que por reparto corresponda (art. 68 LEC) de los de esta ciudad, al que me dirijo en aplicación del art. 51.1 LEC, por ser el lugar del domicilio de la entidad demandada, amén de que aquí nació la relación jurídica entre las partes.

II.- CAPACIDAD.

Conforme a los arts. 6.1.1.º y 3.º LEC tienen capacidad para ser parte las personas físicas y las jurídicas, y a tenor de los arts. 7.1 y 4 LEC, detentan capacidad de obrar procesal, aquéllas mayores de edad no incapacitadas, y éstas constituidas legalmente a través de sus representantes necesarios.

III.- LEGITIMACIÓN.

El art. 10 LEC legitima para comparecer y actuar en juicio, a los titulares de la relación jurídica o del objeto litigioso. En el caso de autos, demandante y demandado, son los sujetos titulares del contrato cuyo incumplimiento arraiga la acción que se ejerce, existiendo, pues, legitimación directa ordinaria. La legitimación activa de mi representado resulta indiscutible en su calidad de comprador de una finca con una superficie menor de la convenida y corresponde la pasiva a la demandada como parte vendedora de dicho contrato.

IV.- PROCEDIMIENTO.

El interés económico de la demanda supera la suma de 15.000 euros, por lo que al no tener la presente contienda una tramitación especial "ratione materiae", será de aplicación lo dispuesto en los arts. 248.3, 249.2 y 254.1 LEC, debiendo ventilarse por el juicio ordinario, regulado en el Título II del Libro II LEC (arts. 399 y ss. LEC), debiendo asimismo secundarse las Disposiciones Comunes a los Procesos Declarativos previstas en el Título I de dicho Libro (arts. 248 y ss. LEC).

V.- POSTULACIÓN Y DEFENSA.

Se cumplen con las normas de postulación procesal, ya que la demanda se presenta por medio de Procurador/a legalmente habilitado para actuar ante los tribunales de este partido, y bajo la dirección de Letrado en ejercicio que redacta y firma, conforme a lo dispuesto en los arts. 23.1 y 31.1 LEC.

VI.- REQUISITOS FORMALES.

Se inicia el proceso por medio de demanda que reúne todos los requisitos exigidos en el art. 399 LEC, sin que existan otras exigencias especiales de procedibilidad, y no estando prevista legalmente una acreditación preliminar de la legitimación o principio de prueba del derecho, por lo que, competente el tribunal, deberá aquélla admitirse, a tenor de los arts. 403.1 y 404 LEC.

VII.- CUANTÍA.

Cumpliendo la exigencia del art. 253.1 LEC, se cifra la cuantía de la demanda en la cantidad de [IMPORTE] euros, que integra la cantidad líquida reclamada conforme al art. 251.1.ª LEC.

VIII.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

IX.- FUNDAMENTO MATERIAL DE LA TUTELA.

Se ejercita en la presente demanda acción declarativa sobre incumplimiento contractual o cumplimiento defectuoso, con fundamento en la obligación de la entrega debida de la vivienda (art. 1461, inciso primero CCiv), que tiene encaje en las previsiones generales del art. 1124 CCiv.

En relación a las consecuencias de este incumplimiento, es de aplicación el art. 1101 y concordantes CCiv regulador de las consecuencias del incumplimiento genérico de obligaciones derivadas de un contrato al establecer que quedan sujetos a la indemnización de daños y perjuicios los que contravinieran el tenor de sus obligaciones.

En este caso, la sociedad vendedora no cumplió la obligación de entrega en la forma pactada en el contrato de compraventa, produciéndose así un incumplimiento o un cumplimiento inexacto, imperfecto o deficiente de las obligaciones asumidas por cuanto el inmueble construido no se ajustó íntegramente a las características pactadas, y al entregarse menor superficie de la convenida se incurre en incumplimiento.

Y en este sentido, como se cuida de precisar la STS de 30 de enero de 1998, Rec. 81/1994«... Que los artículos 1469 y 1470 se refieren a la venta a razón de un precio por unidad de medida, es sancionado por la jurisprudencia de esta Sala, en concreto por lo manifestado en la emblemática Sentencia de 31 octubre 1992 cuando en ellas se dice que "los artículos 1469 y 1470 del Código Civil contienen una específica regulación del error en el contrato de compraventa, cuando este error rebase sobre la cabida de la cosa vendida de tal forma que las partes atribuyen una mayor o menor cabida a la finca objeto del contrato, regulación especial que afecta únicamente a aquellos contratos en el que el precio se haya fijado por unidad de medida y no en un tanto alzado, requiriéndose además que se trate de inmuebles determinados y que se exprese en el contrato su cabida". Sentencia, que por otra parte tiene su antecedente en la de 12 de diciembre de 1991. Todo ello significa que en la presente "litis" ha habido un incumplimiento genérico de obligaciones derivadas de un contrato, por lo que la norma vigente de aplicación será la especificada en los artículos 1101 del Código Civil y concordantes, en especial con lo ordenado en el artículo 1256 de dicho Cuerpo Legal. Por lo que para la efectividad de las acciones emanadas de dicho incumplimiento, él instituto de la prescripción deberá tener el amplio plazo de quince años que se establece con carácter general».

En el mismo sentido, la STS de 27 de julio de 1992 precisa que «... Por otra parte, resulta inaplicable al caso el art. 1469 CC invocado en el motivo, ya que tal precepto contempla la existencia de una divergencia entre lo convenido y la realidad física del bien objeto del contrato que implica un error en el consentimiento, que no se da cuando esa divergencia es debida, como en el presente supuesto, a una actuación del vendedor que implica un inexacto cumplimiento de la obligación de entrega, ya que, como dice la S. 26-11-62, esta Sala ha tenido ocasión de puntualizar en la S. 26-5-56, que las reglas especiales de los arts. 1469 a 1472, no se refieren a la hipótesis de una diferencia entre la cantidad efectiva del inmueble en el momento de la conclusión del contrato y la cantidad entregada y, por tanto, a un inexacto cumplimiento de la obligación de entregar; efectivamente, la reducción voluntaria de la cabida de la cosa vendida por el vendedor da lugar a la aplicación del art. 1124, en cualquiera de las dos opciones que se reconocen a favor del comprador, y así las SS. 24-9-86 y 13-10-87 establecen que "el hecho de que la vendedora hubiera reducido en más de un quince por ciento la cabida de la vivienda acordada, se estima como incumplimiento de contrato, dando paso a la acción derivada del art. 1124 que autoriza la restitución de la prestación y el resarcimiento de daños y perjuicios».

X.- COSTAS.

Las costas del presente proceso deberán ser impuestas a la parte demandada, en la medida de que deben resultar estimadas la totalidad de nuestras pretensiones, conforme al principio del vencimiento que destaca el art. 394.1 LEC, en lo que respecta a los juicios declarativos en su primera instancia.

En atención a todo lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito de demanda junto con los documentos que se acompañan y copias simples de todo ello, se sirva admitir uno y otros, se me tenga por comparecida y parte, en la representación que ostento y con carácter de demandante, entendiéndose conmigo las ulteriores sucesivas diligencias, y por promovido juicio ordinario contra [PARTE DEMANDADA]., se le confiera traslado emplazándole en legal forma de comparecencia, y eventual contestación y seguido que sea el oportuno procedimiento, en su día, se dicte sentencia por la que:

a) Se declare la existencia de un incumplimiento contractual en la compraventa de la vivienda [DESCRIPCIÓN DEL BIEN], al haber entregado la parte demandada menos superficie útil de la pactada.
b) Se condene a la entidad demandada a abonar al demandante la cantidad de [IMPORTE] euros más el interés legal del dinero desde la fecha de la reclamación judicial.

Todo ello con expresa condena en costas del presente procedimiento.

Es justicia de hacerse en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a

========================================================================
