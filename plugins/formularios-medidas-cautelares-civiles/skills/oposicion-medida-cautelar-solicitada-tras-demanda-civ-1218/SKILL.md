---
name: oposicion-medida-cautelar-solicitada-tras-demanda-civ-1218
description: "Oposición a una medida cautelar solicitada tras la demanda. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Oposición a una medida cautelar solicitada tras la demanda

> Formulario **CIV-1218** del plugin **Medidas cautelares y diligencias preliminares** (`formularios-medidas-cautelares-civiles`) · Civil › Medidas cautelares y diligencias preliminares · normativa revisada el 24-11-2026.

## Qué es

Escrito de oposición del demandado a una medida cautelar acordada sin su audiencia y con posterioridad a la demanda (arts. 739 y siguientes LEC), por incumplimiento de los requisitos excepcionales del art. 730.4 LEC (hechos o circunstancias que justifiquen la petición tardía) y de los de apariencia de buen derecho y peligro en la demora. Incluye petición de daños y perjuicios, caución sustitutoria subsidiaria y costas (formulario adaptado a la reforma procesal de la LO 1/2025).

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Oposición a una medida cautelar solicitada tras la demanda» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Oposición a una medida cautelar solicitada tras la demanda” para mi caso». También puedes invocarla directamente con `/formularios-medidas-cautelares-civiles:oposicion-medida-cautelar-solicitada-tras-demanda-civ-1218`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-medidas-cautelares-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Medidas cautelares y diligencias preliminares) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (4 veces)
- [ ] AÑO (2 veces)
- [ ] MEDIDA CAUTELAR ADOPTADA (2 veces)
- [ ] DÍA
- [ ] ENTIDAD
- [ ] IMPORTE
- [ ] LOCALIDAD
- [ ] MES
- [ ] NOMBRE Y APELLIDOS
- [ ] NOMBRE Y APELLIDOS O DENOMINACIÓN SOCIAL
- [ ] Nº
- [ ] Nº DE DOCUMENTOS
- [ ] Nº DE PROCEDIMIENTO
- [ ] RAZONAR EN CADA CASO
- [ ] SEDE

## Normas que cita el formulario

- art. 739 LEC
- art. 730.4 LEC
- art. 736.2 LEC
- art. 723.1 LEC
- art. 740 LEC
- art. 728.2 LEC
- art. 741.2 LEC

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

- Junto a «…AUTELARES A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

PROCESO NÚMERO [Nº DE PROCEDIMIENTO]

PIEZA DE MEDIDAS CAUTELARES

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

D./Dª [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, en nombre y representación de [NOMBRE Y APELLIDOS O DENOMINACIÓN SOCIAL], parte demandada en el procedimiento arriba referenciado, según tengo acreditado en autos, ante el Tribunal comparezco y, como mejor proceda en Derecho, DIGO:

Que habiendo sido notificado de la medida cautelar de [MEDIDA CAUTELAR ADOPTADA] adoptada, sin audiencia de mi representado y en el curso de este proceso, por auto de fecha [FECHA], por medio del presente escrito, al amparo de lo dispuesto en el artículo 739 de la LEC y dentro del plazo establecido, formulo OPOSICIÓN A LA MEDIDA CAUTELAR decretada en base a los siguientes

HECHOS

Hechos relativos al incumplimiento de los requisitos del artículo 730.4 de la LEC

La adopción de la medida cautelar de [MEDIDA CAUTELAR ADOPTADA] decretada por el Tribunal al que me dirijo por auto de fecha [FECHA] no se ajusta al régimen procesal establecido en el artículo 730.4 en relación con el artículo 736.2 de la LEC, puesto que sólo de forma excepcional se permite que puedan solicitarse las medidas cautelares en un momento posterior a la demanda, pero siempre que se basen en hechos y circunstancias que justifiquen la solicitud en dicho momento, conforme a lo dispuesto en los artículos 730.4 y 736.2 de la LEC, tal como se declara reiteradamente en la doctrina interpretativa del precepto.

Del escrito presentado por la contraparte se deduce que los hechos y circunstancias alegados ya existían con anterioridad a decretarse la medida, puesto que se invoca la concertación de [HECHO INVOCADO: p. ej., una escritura de préstamo hipotecario] de fecha [FECHA], anterior a la demanda, y que era conocida por el solicitante al tiempo de decretarse la medida, por lo que no ha tenido lugar ninguna variación o modificación de hechos y circunstancias, y los extremos esgrimidos eran conocidos y pudieron ser alegados en la anterior vista que dio lugar a la adopción de la medida.

Por tanto, no se cumplen los requisitos establecidos en el artículo 730.4 en relación con el artículo 736.2 de la Ley de Enjuiciamiento Civil, preceptos que de forma pacífica se interpreta que sólo admiten hechos nuevos o desconocidos como justificativos de su adopción.

En apoyo de esta interpretación citamos la doctrina pacífica de las Audiencias Provinciales, recogida, entre otros, en los AAP Burgos 19 de mayo de 2004, rec. 236/2004; AAP Guipúzcoa 8 de junio de 2006, rec. 2435/2005 y AAP La Coruña 16 de enero de 2007, rec. 374/2006, según la cual la adopción de medidas cautelares después de la demanda tiene un carácter restrictivo, pues no sólo se opone al momento en que de ordinario se deben solicitar, que es el de la presentación de la demanda, según el artículo 730.1, sino que, además, el propio legislador restringe la posibilidad de pedirlas cuando dice que «sólo podrán solicitarse» si se dan determinados hechos y circunstancias. De ahí que la adopción de medidas cautelares después de la demanda no quepa hacerla sin un cierto carácter restrictivo, pues se oponen a la regla general de ser sólo admisibles junto con la presentación de la demanda principal, destacándose que la carga de justificar por qué el demandante pide las medidas cautelares con posterioridad a la demanda se impone a aquél por la ley, ya que ésta quiere que las medidas cautelares se soliciten, «de ordinario», con la demanda principal.

Pues bien, en este caso ni se razona por qué estos hechos, coetáneos con la demanda y sin que se alegue ni acredite que fueran desconocidos para la parte, sin embargo son pertinentes ahora y no entonces para establecer la medida cautelar, desde la idea de que, si en aquel momento anterior no se instó su adopción, ha de justificarse qué razón hay para que ahora sí sea procedente su petición, motivo que justifica la desestimación de la petición.

Incumplimiento de requisitos: apariencia de buen derecho y peligro en la demora

Además de no cumplirse los requisitos del artículo 730.4 de la LEC, la medida solicitada no se ajusta a los requisitos establecidos en los artículos 726 y 727 del mismo texto legal, puesto que no se dan los requisitos de apariencia de buen derecho y peligro en la demora ([RAZONAR EN CADA CASO]), puesto que los documentos aportados con la demanda en ningún caso ponen de manifiesto la existencia del incumplimiento contractual, y mi mandante es una persona solvente, teniendo bienes suficientes y liquidez para hacer frente al pago de las responsabilidades que pudieran derivarse, acompañando a este escrito, como documentos [Nº DE DOCUMENTOS], certificación del Registro, declaración de IRPF del último ejercicio de [AÑO] y certificación de la entidad bancaria [ENTIDAD] sobre cuentas y depósitos, que ponen de manifiesto la solvencia de mi representado, ocultada de contrario, de lo que también se deriva la improcedencia de adoptar la medida cautelar.

A los anteriores hechos le son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

Competencia

Le corresponde al Tribunal al que me dirijo, al estar conociendo del asunto en primera instancia (art. 723.1 LEC).

Legitimación

Le corresponde a esta parte, al ser la que se ve afectada por las medidas cautelares en su momento decretadas (art. 739 LEC).

Procedimiento

Es el previsto en los artículos 740 y siguientes de la LEC, al haberse adoptado las presentes medidas sin audiencia del demandado.

Apariencia de buen derecho

Es el primero y básico de los requisitos que no concurren, ya que la aportada por el instante de las medidas cautelares se ha visto desvirtuada por el pago efectuado por mi mandante (art. 728.2 LEC).

Peligro en la demora

No existe peligro derivado de la mora procesal al tratarse de un proceso de reclamación de cantidad respecto de un demandado plenamente solvente, sin que exista ningún indicio de que la medida sirva a la tutela cautelar que debe dirigirse.

Solicitud de daños y perjuicios

Al entender que el demandante ha interesado inadecuadamente las medidas cautelares, se solicita que, con fundamento en el artículo 741.2 de la LEC, se declare la condena al demandante a abonar a mi mandante los daños y perjuicios que en su momento y por los trámites previstos en los artículos 712 y siguientes se solicitarán, reteniendo mientras tanto el importe de la caución constituida por el instante.

Caución sustitutoria subsidiaria

Para el caso de que se desestime la oposición, se ofrece caución por importe de [IMPORTE] euros en sustitución de las medidas cautelares, que se prestará mediante aval bancario, y que se solicita por los perjuicios desproporcionados que ocasiona la medida acordada (arts. 746.2 y 747.1 LEC).

Costas

En materia de costas se solicita su imposición al instante de conformidad con lo previsto en el artículo 741.2 de la LEC.

1.– COMPETENCIA, PROCEDIMIENTO Y LEGITIMACIÓN. Artículos 739, 740 y 741 de la LEC.

2.– OPOSICIÓN A LA MEDIDA. Artículos 726, 728, 730.4 y 736.2 de la LEC, al no darse los requisitos establecidos en dichos preceptos según ha quedado expuesto.

3.– COSTAS. Artículo 741 de la LEC.

Por lo expuesto,

SUPLICO AL TRIBUNAL: Tenga por presentado este escrito, documentos y copias, se sirva admitirlos y unirlos a autos, teniendo por formulada, en tiempo y forma, oposición a la medida cautelar instada de contrario y, previa su sustanciación tras la práctica de la prueba que desde este momento se solicita, se alce la medida cautelar decretada en auto de fecha [FECHA], condenando en costas al demandante, así como al pago de los daños y perjuicios producidos como consecuencia de la adopción de la medida.

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO]

Firma Abogado: ______________________

Firma Procurador: ______________________
