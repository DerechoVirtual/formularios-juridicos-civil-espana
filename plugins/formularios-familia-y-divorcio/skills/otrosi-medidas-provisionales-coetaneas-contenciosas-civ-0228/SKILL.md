---
name: otrosi-medidas-provisionales-coetaneas-contenciosas-civ-0228
description: "Otrosí de medidas provisionales coetáneas contenciosas en demanda de nulidad, separación o divorcio. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Otrosí de medidas provisionales coetáneas contenciosas en demanda de nulidad, separación o divorcio

> Formulario **CIV-0228** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Otrosí de medidas provisionales coetáneas contenciosas en demanda de nulidad, separación o divorcio» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Otrosí de medidas provisionales coetáneas contenciosas en demanda de nulidad, separación o divorcio” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:otrosi-medidas-provisionales-coetaneas-contenciosas-civ-0228`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (5 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] Nº (4 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] AÑO
- [ ] CALLE
- [ ] DÍA
- [ ] ENTIDAD BANCARIA
- [ ] FECHA
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] MES
- [ ] NOMBRE DEL HIJO/A
- [ ] Nº DE HECHO
- [ ] NÚMERO
- [ ] PISO
- [ ] PUERTA

## Normas que cita el formulario

- art. 773 LEC
- art. 104 Código Civil
- art. 328 LEC

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

### Avisos de actualización (0) — se aplican en el texto, nunca se copian en el documento

- Ninguno.

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

OTROSÍ DIGO que, al amparo del artículo 773 de la LEC, y no habiéndose adoptado con anterioridad medidas provisionales en relación a la separación (o divorcio o nulidad) del matrimonio, por medio del presente escrito solicito la adopción de las MEDIDAS PROVISIONALES que se dirán contra el demandado D. [NOMBRE Y APELLIDOS] en base a los siguientes HECHOS Y FUNDAMENTOS:

HECHOS

Se dan por reproducidos los hechos de la demanda, debiendo destacarse los siguientes:

1) El matrimonio tiene un único hijo [NOMBRE DEL HIJO/A], de [Nº] años de edad, que convive con la madre en el domicilio conyugal, sito en la localidad de [LOCALIDAD], calle [CALLE], núm. [Nº], piso [PISO], puerta [PUERTA].
2) El demandado abandonó el domicilio en fecha [FECHA], y desde entonces lleva [Nº] meses sin aportar cantidad alguna para la alimentación y gastos diarios del hijo común, y sin visitarle ni relacionarse con él de ninguna forma.
3) El hijo del matrimonio está enormemente afectado por lo sucedido y corre peligro su equilibrio emocional, no siendo como documento núm. [NÚMERO], certificación de psiquiatra infantil que atiende al menor.
4) el esposo cuenta con importantes medios económicos, teniendo unas ganancias de [IMPORTE] euros mensuales, tal como se expuso y acreditó documentalmente en el hecho [Nº DE HECHO] de la demanda, sin perjuicio de la prueba que se propondrá en el siguiente otrosí. Por su parte, los medios económicos de los que dispone mi representada son eventuales dada la precariedad del trabajo, estando retribuido de manera insuficiente, dada su falta de cualificación profesional, su edad, y su estado de salud; a pesar de lo cual, procura, dentro de lo que su estado de salud le permite, realizar algunos trabajos de limpieza de carácter doméstico, en casas particulares, que le proporcionan algunos ingresos con los cuales apenas pueden subsistir madre e hijo.
5) Los gastos domésticos ordinarios ascienden a [IMPORTE] euros mensuales según se expuso y documentó ampliamente, debiendo satisfacerse la hipoteca de la vivienda por importe de [IMPORTE] euros mensuales.

En consecuencia, y no habiéndose solicitado anteriormente, solicitamos que se adopten las medidas provisionales siguientes con la admisión de la demanda, de conformidad con los hechos expuestos, debiendo decretarse provisionalmente la separación, atribuyendo a mi representada la guarda y custodia del menor, y a la madre e hijo el uso de la vivienda conyugal y de su correspondiente ajuar, estableciendo la obligación del esposo de contribuir a las cargas familiares y alimentos por importe de [IMPORTE] euros mensuales.

FUNDAMENTOS DE DERECHO

I.- Legitimación activa y pasiva. La ostentan las respectivas partes en su condición de cónyuges, en relación con los hechos y pretensiones formuladas. En especial, invoco el artículo 104 del Código Civil y el artículo 773 de la Ley de Enjuiciamiento Civil.

II.- Competencia. Artículos 769 y 773 de la Ley de Enjuiciamiento Civil.

III.- Medidas a adoptar. Artículo 104 del Código Civil y su remisión al artículo 103 del mismo.

IV.- Procedimiento. Artículo 773 en relación con el artículo 771 de la Ley de Enjuiciamiento Civil, al no haberse solicitado anteriormente la adopción de medidas provisionales.

V.- Intervención del Ministerio Fiscal: Artículo 749 de la LEC.

VI.- Demás normas concordantes y de aplicación: iura novit curia.

En su virtud,

SUPLICO AL TRIBUNAL: Que tenga por presentado este escrito con los documentos acompañados y sus copias; por interpuesta por el Procurador que suscribe, con quien se entiendan las sucesivas diligencias, en nombre y representación de Doña [NOMBRE Y APELLIDOS], con devolución de la escritura de poderes una vez quede testimonio en autos, demanda de MEDIDAS PROVISIONALES COETÁNEAS de separación conyugal (en su caso, nulidad o divorcio) contra Don [NOMBRE Y APELLIDOS]; y previos los trámites pertinentes, y con intervención del Ministerio Fiscal, dicte Auto por el que se acuerden las siguientes medidas:

a.-La separación provisional de los cónyuges, con revocación de consentimientos y poderes entre cónyuges que pudieran existir.

b.-Atribución a la madre de la guarda y custodia del menor, sin perjuicio de un régimen de comunicación y estancia entre padre e hijo, adecuado a las circunstancias del caso.

c.-Atribución a la madre y al hijo del matrimonio del uso de la vivienda conyugal y ajuar.

d.-La obligación del esposo de satisfacer en concepto de contribución a las cargas familiares y alimentos para el menor la cantidad de [IMPORTE] euros mensuales a pagar dentro de los cinco primeros días de cada mes, a ingresar en la cuenta núm. [Nº] que Doña [NOMBRE Y APELLIDOS] tiene abierta en la entidad financiera [ENTIDAD BANCARIA], actualizándose anualmente, conforme al Índice Oficial de Precios al Consumo para el conjunto Nacional.

OTROSÍ DIGO II: Que a los efectos de prueba en la comparecencia que debe celebrarse para la adopción de medidas provisionales interesa al derecho de esta parte que, al amparo de lo dispuesto en el artículo 328 de la LEC, se requiera al demandado para que exhiba las nóminas de salarios correspondientes al último año que percibe en la empresa [DENOMINACIÓN SOCIAL], así como las declaraciones tributarias de IRPF realizadas por el demandado correspondientes a los dos últimos ejercicios, no disponiendo de dichos documentos mi representada ni tan siquiera por copia simple, obrando en poder del demandado.

Por lo expuesto

SUPLICO AL TRIBUNAL: Que requiera al demandado, en la misma resolución en que se cite a las partes para la comparecencia, para que exhiba en dicho acto las nóminas de salarios correspondientes al último año que percibe en la empresa [DENOMINACIÓN SOCIAL], así como las declaraciones tributarias de IRPF realizadas por el demandado correspondientes a los dos últimos ejercicios.

Es justicia que insto en [LUGAR], a [DÍA] de [MES] de [AÑO].

========================================================================
