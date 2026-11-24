---
name: demanda-terceria-dominio-conyuge-deudor-bien-privativo-civ-1446
description: "Demanda de tercería de dominio del cónyuge del deudor por bien privativo embargado. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de tercería de dominio del cónyuge del deudor por bien privativo embargado

> Formulario **CIV-1446** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Demanda de tercería de dominio que interpone el cónyuge del deudor ejecutado para obtener el alzamiento del embargo trabado sobre un bien que le pertenece con carácter privativo (por ejemplo, adquirido por donación), en un régimen de sociedad de gananciales.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de tercería de dominio del cónyuge del deudor por bien privativo embargado» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de tercería de dominio del cónyuge del deudor por bien privativo embargado” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:demanda-terceria-dominio-conyuge-deudor-bien-privativo-civ-1446`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] AÑO (4 veces)
- [ ] DÍA (4 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] MES (4 veces)
- [ ] NOMBRE Y APELLIDOS DEL EJECUTADO (4 veces)
- [ ] Nº DE DOCUMENTO (4 veces)
- [ ] NOMBRE Y APELLIDOS DEL EJECUTANTE (3 veces)
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A (3 veces)
- [ ] Nº DE PROCEDIMIENTO (2 veces)
- [ ] COLEGIO DE ABOGADOS
- [ ] DNI/NIE
- [ ] DOCUMENTO QUE ACREDITA EL INTENTO DE SOLUCIÓN EXTRAJUDICIAL
- [ ] DOMICILIO
- [ ] IDENTIFICACIÓN DEL BIEN EMBARGADO
- [ ] INDICAR EL MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] NOMBRE DEL NOTARIO
- [ ] NOMBRE Y APELLIDOS DEL DONANTE
- [ ] NOMBRE Y APELLIDOS DEL LETRADO
- [ ] NOMBRE Y APELLIDOS DEL TERCERISTA
- [ ] Nº
- [ ] Nº DE PROTOCOLO
- [ ] PROFESIÓN
- [ ] SEDE

## Normas que cita el formulario

- art. 600 LEC
- art. 1346.2.º Código Civil
- art. 5 Ley Orgánica 1/2025
- art. 1911 Código Civil
- art. 348 Código Civil

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

- Junto a «… demanda. A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «… se resolverá por el tribunal que dictó la orden general y despacho de la misma.»: comprobar en el texto vigente del art. 599 LEC el tipo de juicio por el que se sustancia la tercería (ordinario o verbal), pues el original era contradictorio en este punto (la súplica hablaba de juicio ordinario y la cita del art. 599 de juicio verbal); unificar la súplica con esa redacción.

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

[OPCIONAL — incluir si procede: nota para el profesional, a suprimir antes de presentar] Téngase en cuenta en el Fundamento de Derecho sobre legitimación que, de acuerdo con el art. 600 LEC, la tercería de dominio podrá interponerse también frente al ejecutado cuando el bien al que se refiera haya sido por él designado; y que, aunque no se haya dirigido la demanda frente al ejecutado, podrá éste intervenir en el procedimiento con los mismos derechos procesales que las partes de la tercería, a cuyo fin se le notificará en todo caso la admisión a trámite de la demanda.

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

D./Dª [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, en nombre y representación de D./Dª [NOMBRE Y APELLIDOS DEL TERCERISTA], mayor de edad, de profesión [PROFESIÓN], con domicilio en [DOMICILIO], y DNI/NIE [DNI/NIE], cuya representación acreditaré mediante comparecencia apud acta cuando sea requerido para ello [ELEGIR: (sin más) / "representación que acredito mediante copia de poder especial para pleitos que ruego me sea devuelta una vez testimoniada en autos por necesitarla para otros usos"], comparezco en los autos de procedimiento de ejecución número [Nº DE PROCEDIMIENTO], seguidos en este Tribunal a instancia de D./Dª [NOMBRE Y APELLIDOS DEL EJECUTANTE] contra D./Dª [NOMBRE Y APELLIDOS DEL EJECUTADO], con la asistencia del Letrado D./Dª [NOMBRE Y APELLIDOS DEL LETRADO], del Ilustre Colegio de Abogados de [COLEGIO DE ABOGADOS], y DIGO:

Que por medio del presente escrito y en la representación que ostento, formulo DEMANDA DE TERCERÍA DE DOMINIO contra D./Dª [NOMBRE Y APELLIDOS DEL EJECUTANTE], en calidad de parte ejecutante en el procedimiento antes referido, en el que interviene representada por el Procurador D./Dª [NOMBRE Y APELLIDOS DEL PROCURADOR/A], y contra D./Dª [NOMBRE Y APELLIDOS DEL EJECUTADO], en calidad de parte ejecutada en el mismo procedimiento, en el que, a su vez, interviene representada por el Procurador D./Dª [NOMBRE Y APELLIDOS DEL PROCURADOR/A].

[OPCIONAL — incluir si procede: si la demanda se dirige también contra el ejecutado]

De acuerdo con el art. 600 LEC, la tercería de dominio podrá interponerse también frente al ejecutado cuando el bien al que se refiera haya sido por él designado.

La presente demanda se basa en los siguientes

HECHOS

PRIMERO.- En fecha [DÍA] de [MES] de [AÑO], este Tribunal dictó auto por el que se despachó ejecución frente a D./Dª [NOMBRE Y APELLIDOS DEL EJECUTADO], cónyuge de mi representado/a, decretándose el embargo, entre otros, del siguiente bien: [IDENTIFICACIÓN DEL BIEN EMBARGADO].

SEGUNDO.- Mi representado/a y el ejecutado contrajeron matrimonio [ELEGIR: civil / canónico] en [LOCALIDAD], en fecha [DÍA] de [MES] de [AÑO], debidamente inscrito en el Registro Civil de [LOCALIDAD], [DATOS REGISTRALES: Sección, Tomo, Página], estando sujeto su matrimonio al régimen legal de sociedad de gananciales por ostentar ambos vecindad de Derecho común y no haber otorgado capitulaciones matrimoniales.

Se acompaña, como DOCUMENTO Nº [Nº DE DOCUMENTO], certificación literal de matrimonio expedida por el Registro Civil.

TERCERO.- El bien antes citado pertenece a mi representado/a con carácter privativo, conforme a lo dispuesto en el art. 1346.2.º del Código Civil, por haberlo adquirido mediante donación efectuada en su favor por [ELEGIR: su padre / su madre / otra persona] D./Dª [NOMBRE Y APELLIDOS DEL DONANTE], formalizada en escritura pública otorgada en fecha [DÍA] de [MES] de [AÑO], ante D./Dª [NOMBRE DEL NOTARIO], Notario de [LOCALIDAD], con número de protocolo [Nº DE PROTOCOLO].

Se acompaña, como DOCUMENTO Nº [Nº DE DOCUMENTO], copia de la citada escritura para acreditar la naturaleza privativa del bien.

CUARTO.- Mi representado/a no es parte en la ejecución que se tramita ni debe responder con sus bienes privativos de la deuda ejecutada, por lo cual procede alzar el embargo practicado sobre el indicado bien.

QUINTO.- Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial. En este sentido, se acudió a [INDICAR EL MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como DOCUMENTO Nº [Nº DE DOCUMENTO] [DOCUMENTO QUE ACREDITA EL INTENTO DE SOLUCIÓN EXTRAJUDICIAL].

Resultan aplicables a los anteriores hechos los siguientes

FUNDAMENTOS DE DERECHO

I. COMPETENCIA Y PROCEDIMIENTO.- Es competente el Tribunal al que me dirijo, por ser el que dictó la orden general de ejecución y despacho de la misma, y deben seguirse los trámites que para la tercería de dominio establece el artículo 599 de la Ley de Enjuiciamiento Civil, que dispone que la tercería de dominio habrá de interponerse ante el Letrado de la Administración de Justicia responsable de la ejecución y se resolverá por el tribunal que dictó la orden general y despacho de la misma.

II. LEGITIMACIÓN.- Corresponde la legitimación activa a mi representado/a, según lo dispuesto en el art. 595 de la Ley de Enjuiciamiento Civil, por ser el dueño del bien embargado, con carácter privativo, desde fecha anterior a la práctica del embargo y no ser parte ejecutada ni responsable de la deuda.

Está legitimado pasivamente el acreedor ejecutante, así como el deudor ejecutado por haber sido designado por él el bien al que se refiere la presente tercería.

III. REQUISITOS ADJETIVOS Y MOMENTO PROCESAL HÁBIL.- Dispone el art. 595.3 de la Ley de Enjuiciamiento Civil que, con la demanda de tercería de dominio, se aporte un principio de prueba por escrito del fundamento de la pretensión del tercerista. En la presente demanda este principio de prueba viene constituido por la escritura de donación que se acompaña como DOCUMENTO Nº [Nº DE DOCUMENTO].

Asimismo, se interpone la presente demanda en momento procesal hábil, en atención a lo dispuesto en el art. 596 de la Ley de Enjuiciamiento Civil, de acuerdo con el cual la tercería de dominio podrá interponerse desde que se haya embargado el bien o bienes a que se refiera, aunque el embargo sea preventivo, sin que pueda hacerse con posterioridad al momento en que, de acuerdo con lo dispuesto en la legislación civil, se produzca la transmisión del bien al acreedor o al tercero que lo adquiera en pública subasta.

En cuanto a la prohibición de segundas o ulteriores tercerías, téngase en cuenta lo establecido en el art. 597 de la Ley de Enjuiciamiento Civil.

IV. CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.- La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4.º y 399.3, en relación con el art. 437.1 de la Ley de Enjuiciamiento Civil, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

V. DERECHO SUSTANTIVO.- La tercería de dominio se plantea frente a un embargo indebido, cuyo alzamiento se persigue (cfr. art. 601 de la Ley de Enjuiciamiento Civil). En concreto, es la vía procesal articulada por la Ley para solicitar el alzamiento del embargo practicado sobre bienes que no pertenecen al ejecutado, sino a un tercero, de modo coherente con el principio de responsabilidad patrimonial consagrado en el art. 1911 del Código Civil y con los arts. 348, 349 y concordantes del Código Civil, que regulan el derecho de propiedad.

Puede suceder, en efecto, que se embarguen determinados bienes como si perteneciesen al ejecutado cuando en realidad su titularidad corresponde a otra persona. Se ha producido un error en la atribución de la titularidad de los bienes. Para permitir al tercero, verdadero propietario de los bienes, defender su derecho, la Ley ha articulado un mecanismo específico: la tercería de dominio.

Tratándose de cónyuges cuyo matrimonio se rija por la sociedad de gananciales, está admitida la procedencia de la tercería de dominio, aunque la deuda tenga carácter ganancial, cuando el bien embargado sea, no común, sino privativo del cónyuge del ejecutado y, por tanto, no esté afecto a responsabilidad.

Conforme al art. 603 de la Ley de Enjuiciamiento Civil, el auto que resuelva la tercería de dominio se pronunciará sobre la pertenencia del bien y la procedencia de su embargo a los únicos efectos de la ejecución en curso, sin que produzca efectos de cosa juzgada en relación con la titularidad del bien.

VI. COSTAS.- Procede imponerlas al/a los demandados en los términos del art. 603 de la Ley de Enjuiciamiento Civil, en relación con los artículos 394 y siguientes de la misma Ley.

VII. IURA NOVIT CURIA y cuantos resulten de pertinente aplicación.

Por lo expuesto,

SUPLICO AL TRIBUNAL: Que, teniendo por presentado este escrito con los documentos que lo acompañan y copia de todo ello, me tenga por comparecido y parte en la representación que ostento, entendiéndose conmigo las sucesivas diligencias, lo admita y tenga por interpuesta DEMANDA DE TERCERÍA DE DOMINIO contra D./Dª [NOMBRE Y APELLIDOS DEL EJECUTANTE], parte ejecutante en los autos de ejecución núm. [Nº DE PROCEDIMIENTO] que se siguen ante este Tribunal, y contra D./Dª [NOMBRE Y APELLIDOS DEL EJECUTADO], parte ejecutada en los mismos autos, que habrá de sustanciarse en pieza separada por los trámites legalmente previstos y, previo traslado a la parte contraria y demás trámites legales, dicte auto en que se pronuncie sobre la pertenencia del bien a mi representado/a y acuerde, en consecuencia, el alzamiento del embargo sobre el citado bien, así como de las medidas de garantía que, en su caso, se hubiesen adoptado, con expresa imposición de costas al/a los demandado/s.

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma y número de colegiado del Letrado Firma del Procurador
