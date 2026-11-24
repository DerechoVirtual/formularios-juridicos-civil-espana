---
name: demanda-sucinta-desahucio-falta-pago-rentas-civ-0541
description: "Demanda sucinta de desahucio por falta de pago de las rentas. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda sucinta de desahucio por falta de pago de las rentas

> Formulario **CIV-0541** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 24-11-2026.

## Qué es

Parte HECHOS FUNDAMENTOS DE DERECHO Suplico de suspensión Otrosí de cuantía Otrosí para designar domicilio en caso de actos de comunicación y solicitud de práctica de requerimientos Otrosí de ejecución directa Otrosí de tasa Firmas

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda sucinta de desahucio por falta de pago de las rentas» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda sucinta de desahucio por falta de pago de las rentas” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:demanda-sucinta-desahucio-falta-pago-rentas-civ-0541`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº DE DOCUMENTO (7 veces)
- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] CALLE (3 veces)
- [ ] IMPORTE (3 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] MES Y AÑO (2 veces)
- [ ] Nº DE CLÁUSULA (2 veces)
- [ ] FECHA
- [ ] FOLIO
- [ ] LIBRO
- [ ] MES
- [ ] PISO
- [ ] PROVINCIA
- [ ] PUERTA
- [ ] TOMO

## Normas que cita el formulario

- art. 3 k) Ley 12/2023
- art. 22.4 LEC
- art. 439.4 LEC
- art. 438.5 LEC
- art. 441.5 LEC
- art. 439.6 LEC
- art. 394 LEC
- art. 438 LEC
- art. 251 LEC
- art. 155 LEC
- art. 161 LEC
- art. 549.3 LEC
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

### Avisos de actualización (1) — se aplican en el texto, nunca se copian en el documento

- Junto a «…a tasa. ========================================================================»: requisito de procedibilidad del art. 5 LO 1/2025 — antes de presentar la demanda hay que intentar un medio adecuado de solución de controversias (MASC) y acreditarlo con la demanda (arts. 264.4.º y 399.3 LEC), salvo las materias excluidas del art. 5.2. Fuente: LO 1/2025, arts. 5 a 7 (BOE-A-2025-76).

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

A LA SECCIÓN CIVIL DEL TRIBUNAL INSTANCIA

Don [NOMBRE Y APELLIDOS] Procurador de los Tribunales, en nombre y representación de Don [NOMBRE Y APELLIDOS], con domicilio en la calle [CALLE], de la localidad de [LOCALIDAD], provincia de [PROVINCIA], según acredito con la copia de copia electrónica del poder notarial de representación informática (o digitalizada) que se acompaña y cuya devolución solicito previa unión de testimonio a los autos, comparezco ante este Tribunal y DIGO:

Que en la representación que ostento formulo demanda ejercitando la pretensión de desahucio por falta de pago de la renta arrendaticia, contra Don [NOMBRE Y APELLIDOS] con domicilio en [LOCALIDAD], la cual fundo en los siguientes:

HECHOS

PRIMERO.- Mi mandante es propietario de la finca urbana sita en esta ciudad, calle [CALLE], nº [NÚMERO], piso [PISO], puerta [PUERTA] inscrita en el Registro de la Propiedad de [LOCALIDAD], Libro [LIBRO], Tomo [TOMO] Folio [FOLIO] (acompaño como documento número [Nº DE DOCUMENTO] copia auténtica del título expresado), la cual fue cedida en arrendamiento al demandado mediante contrato de fecha [FECHA], en el que se pactó una renta mensual de [IMPORTE] euros la cual es actualizable anualmente en los términos que resulta de la cláusula [Nº DE CLÁUSULA] del contrato, previa comunicación fehaciente al arrendatario, obligación que ha cumplido mi principal puntualmente. Conforme al pacto [Nº DE CLÁUSULA] del contrato, la renta y las cantidades a ella asimiladas son pagaderas por meses anticipados, por lo que mi mandante pasa al cobro los recibos en la cuenta corriente de la entidad bancaria designada por el arrendatario, dentro de los cinco primeros días de cada mes (acompaño copia del citado contrato como documento número [Nº DE DOCUMENTO]).

Mi mandante NO tiene la condición de gran tenedora de vivienda en los términos que establece el art. 3 k) de la Ley 12/2023, según se acredita por la certificación del Registro de la Propiedad donde figura la relación de propiedades de mi representada, que acompaño como documento número [Nº DE DOCUMENTO].

Según se recoge en el contrato, el inmueble SÍ constituye la vivienda habitual de la persona arrendataria.

SEGUNDO.- Que desde el mes de [MES], el demandado no ha pagado la renta arrendaticia, puesto que la entidad bancaria ha devuelto impagados los recibos pasados al cobro por mi representado, tal como consta al dorso de los mismos (acompaño como documentos [Nº DE DOCUMENTO] recibos impagados por el arrendatario).

En la actualidad el demandado adeuda las mensualidades de [MES Y AÑO] a [MES Y AÑO] que ascienden a un total de [IMPORTE] euros, sin perjuicio de las que vayan venciendo.

TERCERO.- Mi principal requirió por (carta certificado o por acto de conciliación, requerimiento notarial, etc…) al demandado en los términos que resulta del documento que acompaño, apercibiéndole que de no proceder al abono de las rentas adeudadas se ejercitaría la acción de desahucio por falta de pago, todo ello con indicación de lo establecido en el art. 22.4 de la LEC, sin que hasta el momento de interponer la demanda se haya avenido a cumplir con la obligación pactada (con arreglo a este precepto se puede requerir de pago con treinta días de antelación a la presentación de la demanda) (acompaño dicha carta como documento número [Nº DE DOCUMENTO]), por lo que, de conformidad a lo prevenido en el artículo 439.4 de la LEC se hace constar expresamente que no procede la enervación del deshaucio.

CUARTO.- Atendido el impago y la improcedencia de la enervación, se ejercita mediante la presente demanda la pretensión de desahucio por falta de pago al amparo de lo dispuesto en el art. 438.5 LEC, debiendo procederse por el Letrado de la Administración de Justicia a requerir al deudor para que en el plazo de diez días desaloje el inmueble (caso de haberse indicado la procedencia de la enervación se haría constar además: y, caso de pretender la enervación, para que pague al actor la totalidad de lo que deba o ponga a disposición de aquel en el tribunal o notarialmente el importe de las cantidades reclamadas en la demanda y las que adeude en el momento del pago enervador del desahucio), dando cumplimiento a lo dispuesto en el art. 441.5 de la LEC, dictando decreto acordando el desahucio para el caso de no atender el requerimiento o no comparecer el demandado, y siguiendo el juicio sus trámites en otro caso.

A los anteriores hechos son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

Los artículos 45, 47, 52 y 250.1.1ª de la LEC en cuanto a la competencia y procedimiento, debiendo seguirse por los trámites establecidos en el art. 438.5 y 6 LEC, practicándose el requerimiento por el Letrado de la Administración de Justicia previamente a la vista que se señale, dictándose decreto estimando la pretensión y acordando el lanzamiento para el caso de que el demandado no atienda el requerimiento ni se oponga, y continuando el juicio en otro caso.

El demandante tiene legitimación activa por ser el arrendador de la vivienda y el demandado está legitimado pasivamente por ostentar la cualidad de arrendatario tal como consta en el contrato aportado como documento número

A los efectos establecidos en el art. 439.6 de la LEC, se hace constar expresamente que:

-Mi representada es persona arrendadora que NO tiene la condición de gran tenedora de vivienda, según se acredita por la certificación del Registro de la Propiedad acompañada como número [NÚMERO].

-El inmueble constituye la vivienda habitual de la persona arrendataria, tal como consta en el contrato aportado como documento número [Nº DE DOCUMENTO].

Por lo demás, desde la STC 26/2025, de 29 de enero, en ningún caso es obligatorio presentar informe de vulnerabilidad ni acreditar mediación previa.

En cuanto al fondo, al tratarse de una finca urbana, es de aplicación el artículo 27.2.a) de la Ley de Arrendamientos Urbanos que faculta al arrendador a resolver el contrato de arrendamiento, entre otros casos, cuando el arrendatario incumpla su obligación de satisfacer la renta convenida o de las cantidades cuya obligación de pago haya asumido o corresponda al arrendatario

El artículo 22.4 en relación con el artículo 439.3 en cuanto a la improcedencia de la enervación tal como resulta expresado en el hecho tercero.

Al amparo del artículo 394 de la LEC, las costas deben imponerse a la parte cuyas pretensiones sean totalmente desestimadas.

Por todo lo expuesto,

SUPLICO AL TRIBUNAL: Que tenga por presentada esta demanda, con su copia y documentos que la acompañan, que la admita y que me tenga por personado y parte en la representación que ostento de Don [NOMBRE Y APELLIDOS] en virtud de la copia electrónica del poder notarial de representación informática (o digitalizada) general para pleitos cuya devolución intereso previa unión a los autos de copia testimoniada (o designa apud acta), que se entiendan conmigo las sucesivas diligencia, y que se tenga por formulada demanda en ejercicio de la pretensión de desahucio por falta de pago de la renta de la vivienda objeto de este proceso, contra Don [NOMBRE Y APELLIDOS], y que por el Letrado de la Administración de Justicia se admita la demanda, y:

1) se requiera al demandado en los términos que indican el art. 438.5 LEC, y en el caso de no atender el requerimiento o no comparecer para oponerse o allanarse, se dicte decreto dando por terminado el juicio y se procederá a su inmediato lanzamiento, sin necesidad de notificación posterior, fijando día y hora exacta para el lanzamiento para el caso de que no hubiera oposición, y solicitando su ejecución directa por medio de otrosí en esta demanda.

2) para el caso de oposición, tras el señalamiento y celebración de la vista con citación al demandado en legal forma con los apercibimientos establecidos en los apartados 5 y 6 del art. 438 LEC, se dicte la resolución que proceda estimando la demanda de desahucio por falta de pago de la renta, se declare resuelto el contrato objeto de este proceso y se proceda al lanzamiento del demandado, solicitando su ejecución directa por otrosí en esta demanda.

3) Que se impongan las costas al demandado.

OTROSÍ PRIMERO DIGO: Que fijo la cuantía del proceso en [IMPORTE] euros, que se corresponde con la renta anual, por aplicación de la regla 9º del art. 251 de la LEC.

SUPLICO AL TRIBUNAL: Tenga por efectuada la anterior manifestación a todos los efectos legales que procedan.

OTROSÍ SEGUNDO DIGO: Que al amparo del apartado 3 del art. 155 de la LEC designo como domicilio del demandado, a efectos de actos de comunicación, el de la vivienda arrendada sita en la calle [CALLE], nº [NÚMERO], de esta Ciudad, al no haberse señalado otro domicilio para actos de comunicación en el contrato, interesando asimismo, al amparo del primer párrafo del apartado tercero del artículo 161 de la LEC y teniendo en cuenta que el domicilio donde se ha de practicar la comunicación es la vivienda arrendada al demandado, si en el momento de practicar la comunicación no se encontrare allí dicho destinatario, se efectúe la entrega a cualquier empleado o familiar mayor de 14 años, que se encuentre en ese lugar, o al conserje de la finca, si lo tuviere, advirtiendo al receptor que está obligado a entregar la copia de la resolución o la cédula al destinatario de ésta o a darle aviso, si sabe su paradero.

OTROSÍ TERCERO DIGO: Que, de conformidad a lo dispuesto en el artículo 549.3 de la LEC intereso que se proceda a la ejecución directa de la sentencia condenatoria o decreto que ponga fin al desahucio que en su momento se dicten, procediendo al lanzamiento en el día y hora exacta señalados en la propia sentencia o en la fecha que se hubiere fijado al ordenar la realización del requerimiento al demandado.

OTROSÍ CUARTO: (Caso de personas jurídicas no exentas) Que estando la presente demanda sujeta al abono de la tasa por el ejercicio de la potestad jurisdiccional fijada por la Ley 10/2012, de 20 de noviembre, modificada por Real Decreto Ley 3/2013, de 22 de febrero, y Ley 25/2015, de 28 julio, y por Orden HAP/861/2015, de 7 de mayo, siendo mi representada persona jurídica no exenta, se acompaña a la presente demanda como documento nº [Nº DE DOCUMENTO] la correspondiente autoliquidación con el ejemplar para la Administración de Justicia debidamente validado y en el que consta el pago de la cantidad de 150 euros correspondiente a la cuota fija, sin que se incluya la cuota variable prevista en el artículo 7.2 de la Ley 10/2012 al haber sido declarado inconstitucional y nulo por la STC 140/2016, de 21 de julio.

En virtud de lo anterior,

SUPLICO AL TRIBUNAL: que tenga por hecha la anterior manifestación a los efectos pertinentes y por acompañado el documento justificativo del abono de la tasa.

========================================================================
