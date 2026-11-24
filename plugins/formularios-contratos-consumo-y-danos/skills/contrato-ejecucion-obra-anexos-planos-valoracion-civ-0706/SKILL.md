---
name: contrato-ejecucion-obra-anexos-planos-valoracion-civ-0706
description: "Contrato de ejecución de obra con anexos de planos y valoración. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de ejecución de obra con anexos de planos y valoración

> Formulario **CIV-0706** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Contrato de ejecución de obra por el que un contratista se obliga a ejecutar una obra a cambio de un precio cerrado, con calendario de pagos, plazo de ejecución con penalización por demora, prohibición de subcontratar, garantía de resultados, resolución y sumisión a arbitraje de equidad.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de ejecución de obra con anexos de planos y valoración» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de ejecución de obra con anexos de planos y valoración” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:contrato-ejecucion-obra-anexos-planos-valoracion-civ-0706`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] DENOMINACIÓN SOCIAL DEL CONTRATISTA (6 veces)
- [ ] IMPORTE (5 veces)
- [ ] Nº DE DOCUMENTO (5 veces)
- [ ] DENOMINACIÓN SOCIAL DEL COMITENTE (4 veces)
- [ ] DÍA (4 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] Nº (4 veces)
- [ ] AÑO (3 veces)
- [ ] DOMICILIO (3 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] MES (3 veces)
- [ ] NACIONALIDAD (3 veces)
- [ ] DATOS REGISTRALES: FOLIO, TOMO GENERAL DEL LIBRO DE SOCIEDADES, HOJA (2 veces)
- [ ] NOMBRE Y APELLIDOS / DENOMINACIÓN SOCIAL DEL COMITENTE (2 veces)
- [ ] NOMBRE Y APELLIDOS / DENOMINACIÓN SOCIAL DEL CONTRATISTA (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL CÓNYUGE (2 veces)
- [ ] PROVINCIA (2 veces)
- [ ] CALLE Y NÚMERO
- [ ] DENOMINACIÓN SOCIAL
- [ ] DESCRIPCIÓN DE LA OBRA
- [ ] IMPORTE EN LETRA
- [ ] NIF
- [ ] NOMBRE DEL NOTARIO
- [ ] NOMBRE Y APELLIDOS DEL REPRESENTANTE
- [ ] Nº DE PROTOCOLO
- [ ] OTROS DOCUMENTOS
- [ ] PLAZO DE GARANTÍA
- [ ] RELACIÓN DE PLANOS Y DOCUMENTOS TÉCNICOS
- [ ] VALORACIÓN DETALLADA DE LA OBRA

## Normas que cita el formulario

- No cita artículos concretos; Claude localizará las normas aplicables con Jurisprudenciator si el documento las necesita.

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

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

REUNIDOS

DE UNA PARTE (repetir el párrafo si hay varias personas en esta parte),

[NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero/a / casado/a / divorciado/a / separado/a / viudo/a], de nacionalidad [NACIONALIDAD], con domicilio en [DOMICILIO], y [ELEGIR: DNI / pasaporte] número [Nº DE DOCUMENTO].

[OPCIONAL — incluir si procede: en caso de estado civil casado/a]

Casado/a con [NOMBRE Y APELLIDOS DEL CÓNYUGE], mayor de edad, con [ELEGIR: DNI / pasaporte] número [Nº DE DOCUMENTO], en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

Y DE OTRA (repetir el párrafo si hay varias personas en esta parte),

[NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero/a / casado/a / divorciado/a / separado/a / viudo/a], de nacionalidad [NACIONALIDAD], con domicilio en [DOMICILIO], y [ELEGIR: DNI / pasaporte] número [Nº DE DOCUMENTO].

[OPCIONAL — incluir si procede: en caso de estado civil casado/a]

Casado/a con [NOMBRE Y APELLIDOS DEL CÓNYUGE], mayor de edad, con [ELEGIR: DNI / pasaporte] número [Nº DE DOCUMENTO], en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

INTERVIENEN

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— Todas las partes en su propio nombre y representación.

— [NOMBRE Y APELLIDOS], en su propio nombre y representación (repetir por cada parte que actúe en nombre propio).

— [NOMBRE Y APELLIDOS DEL REPRESENTANTE], en nombre y representación de (repetir por cada representado):

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— (Si se trata de persona física) [NOMBRE Y APELLIDOS], mayor de edad, de nacionalidad [NACIONALIDAD], domiciliado/a en [DOMICILIO], con [ELEGIR: DNI / pasaporte] número [Nº DE DOCUMENTO].

— (Si se trata de una persona jurídica) La compañía mercantil denominada [DENOMINACIÓN SOCIAL], domiciliada en [LOCALIDAD], calle [CALLE Y NÚMERO], con NIF núm. [NIF], inscrita en el Registro Mercantil de [PROVINCIA] [DATOS REGISTRALES: FOLIO, TOMO GENERAL DEL LIBRO DE SOCIEDADES, HOJA]. Hace uso de las facultades conferidas a su favor en calidad de [ELEGIR: administrador único / administrador solidario / consejero delegado / apoderado] de la sociedad indicada, cargo para el que fue nombrado/a en escritura otorgada ante el notario de [LOCALIDAD], [NOMBRE DEL NOTARIO], el [DÍA] de [MES] de [AÑO], con el número de orden de su protocolo [Nº DE PROTOCOLO], que causó inscripción en el Registro Mercantil de [PROVINCIA] [DATOS REGISTRALES: FOLIO, TOMO GENERAL DEL LIBRO DE SOCIEDADES, HOJA].

Ambas partes se reconocen mutuamente con capacidad suficiente para otorgar el presente contrato de EJECUCIÓN DE OBRA y, a tal fin,

EXPONEN

Que han convenido realizar un contrato de ejecución de obra, el cual se regirá de acuerdo con las condiciones y pactos que se establecen en las siguientes

CLÁUSULAS

PRIMERA.- Objeto.

Constituye el objeto del presente contrato [DESCRIPCIÓN DE LA OBRA] (repetir el párrafo por cada obra o fase).

En todo caso, la obra a realizar se ajustará a las descripciones (planos y demás documentos) recogidos en el anexo I del presente contrato.

SEGUNDA.- Precio.

El precio total de la obra es de [IMPORTE] euros, a tenor de la valoración que se acompaña en el anexo II. En el precio se entienden incluidos todos los conceptos que integran o pueden integrar el coste, tales como salarios, transportes, cargas sociales, materiales consumibles, dietas por cualquier concepto y gravámenes de todo tipo.

Asimismo, el precio indicado se entiende cerrado, no pudiendo sufrir revisiones por diferencias de coste de materiales ni por aumento de la mano de obra. El impuesto sobre el valor añadido no está incluido en el precio.

TERCERA.- Pago.

El pago del precio se realizará de la siguiente forma:

a) [IMPORTE] euros, a cuenta del valor total, que se entregan en el presente acto por [NOMBRE Y APELLIDOS / DENOMINACIÓN SOCIAL DEL COMITENTE] a [NOMBRE Y APELLIDOS / DENOMINACIÓN SOCIAL DEL CONTRATISTA], quien los recibe a su entera satisfacción, sirviendo este documento como carta de pago de la expresada cantidad.

b) El resto, hasta el total pago de la cantidad debida, [IMPORTE] euros ([IMPORTE EN LETRA] euros), mediante [Nº] abonos mensuales de [IMPORTE] euros, de [DÍA] a [DÍA] de [MES] de [AÑO].

CUARTA.- Plazo de ejecución.

La empresa [DENOMINACIÓN SOCIAL DEL CONTRATISTA] se compromete a realizar la referida obra en el plazo de [Nº] meses, contados a partir de la firma del presente contrato.

Si, llegada la fecha prevista para la terminación de la obra, ésta no hubiera sido concluida, se establece una cláusula penal de indemnización de [IMPORTE] euros por día de demora, indemnización que deberá ser deducida de la cantidad a pagar en la última factura.

QUINTA.- Ejecución directa.

La empresa [DENOMINACIÓN SOCIAL DEL CONTRATISTA] se compromete a ejecutar por sí misma la obra contratada, no pudiendo subcontratarla a terceros sin previa y específica autorización de la empresa [DENOMINACIÓN SOCIAL DEL COMITENTE].

SEXTA.- Obligaciones de las partes.

La empresa [DENOMINACIÓN SOCIAL DEL CONTRATISTA] asume las siguientes obligaciones:

a) Suministrar toda la mano de obra especializada y auxiliar necesaria para la realización de la obra.

b) Aportar el utillaje, maquinaria, accesorios y materiales necesarios para la ejecución de los trabajos contratados.

c) Permitir y favorecer las inspecciones que en cualquier momento desee efectuar la empresa [DENOMINACIÓN SOCIAL DEL COMITENTE].

d) Informar a la empresa contratante sobre cualquier circunstancia que altere el programa de trabajo previsto o la calidad de la obra a realizar.

Por su parte, la empresa [DENOMINACIÓN SOCIAL DEL COMITENTE] entregará a la empresa [DENOMINACIÓN SOCIAL DEL CONTRATISTA] toda la documentación necesaria para una correcta interpretación y ejecución del trabajo. A saber:

a) Planos.

b) Especificaciones técnicas.

c) [OTROS DOCUMENTOS]

SÉPTIMA.- Obligaciones laborales, fiscales y de Seguridad Social.

La empresa [DENOMINACIÓN SOCIAL DEL CONTRATISTA], que por la presente manifiesta estar al día en sus obligaciones fiscales, con la Seguridad Social y con sus propios trabajadores, asume la responsabilidad plena para el pago de cuantas obligaciones se deriven de las relaciones de trabajo que tenga establecidas con el personal que desempeñe los servicios contratados.

OCTAVA.- Garantía.

La empresa [DENOMINACIÓN SOCIAL DEL CONTRATISTA] garantiza durante el plazo de [PLAZO DE GARANTÍA] los resultados de la obra realizada, de tal forma que la misma cumpla con todas las funcionalidades requeridas, comprometiéndose a subsanar cualquier defecto o anomalía de funcionamiento que pueda surgir durante ese plazo.

NOVENA.- Resolución.

La empresa [DENOMINACIÓN SOCIAL DEL COMITENTE] se reserva el derecho a resolver el presente contrato y suspender momentáneamente los trabajos, mediante notificación por escrito con [Nº] días de antelación, siempre que se den motivos de incumplimiento de plazos o defectos de calidad.

DÉCIMA.- Legislación aplicable y arbitraje.

Las partes contratantes se atendrán con carácter preferente a lo dispuesto en el presente contrato y, en su defecto, a lo establecido en el Código Civil y demás normas de aplicación.

Cualquier controversia que surja entre las partes y que no sea resuelta entre las mismas de forma amistosa será finalmente decidida mediante arbitraje de equidad y conforme a las normas contenidas en la Ley 60/2003, de 23 de diciembre, de Arbitraje.

Y en prueba de conformidad con cuanto antecede, se firma el presente contrato, compuesto de [Nº] folios, por duplicado y a un solo efecto, en el lugar y fecha antes indicados.

Firmado: [NOMBRE Y APELLIDOS / DENOMINACIÓN SOCIAL DEL COMITENTE]	Firmado: [NOMBRE Y APELLIDOS / DENOMINACIÓN SOCIAL DEL CONTRATISTA]

ANEXO I

Planos y demás documentos: [RELACIÓN DE PLANOS Y DOCUMENTOS TÉCNICOS]

ANEXO II

Valoración de la obra: [VALORACIÓN DETALLADA DE LA OBRA]
