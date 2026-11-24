---
name: contrato-alimentos-favor-hijo-patria-potestad-civ-0358
description: "Contrato de alimentos a favor de hijo con patria potestad prorrogada. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de alimentos a favor de hijo con patria potestad prorrogada

> Formulario **CIV-0358** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Contrato de alimentos (arts. 1791 a 1797 del Código Civil) por el que una asociación se obliga a prestar alojamiento, manutención y asistencia integral a una persona con discapacidad, a cambio de un capital que transmiten sus progenitores y representantes legales. Se usa para asegurar el cuidado vitalicio de un hijo con discapacidad cuando se prevé que los padres no podrán atenderlo.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de alimentos a favor de hijo con patria potestad prorrogada» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de alimentos a favor de hijo con patria potestad prorrogada” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:contrato-alimentos-favor-hijo-patria-potestad-civ-0358`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (11 veces)
- [ ] DENOMINACIÓN DE LA ASOCIACIÓN (8 veces)
- [ ] LOCALIDAD (7 veces)
- [ ] NOMBRE Y APELLIDOS DEL ALIMENTISTA (7 veces)
- [ ] AÑO (4 veces)
- [ ] DÍA (4 veces)
- [ ] MES (4 veces)
- [ ] DNI/NIE (3 veces)
- [ ] IMPORTE (3 veces)
- [ ] TERRITORIO (3 veces)
- [ ] CALLE Y NÚMERO (2 veces)
- [ ] DENOMINACIÓN DE LA RESIDENCIA (2 veces)
- [ ] IMPORTE EN LETRA (2 veces)
- [ ] Nº (2 veces)
- [ ] PROFESIÓN (2 veces)
- [ ] COMUNIDAD AUTÓNOMA
- [ ] DATOS REGISTRALES
- [ ] DESCRIPCIÓN PRECISA, CON VALORACIÓN Y DATOS REGISTRALES
- [ ] DESCRIPCIÓN Y VALORACIÓN
- [ ] EMPRESA VALORADORA
- [ ] ESTADO CIVIL
- [ ] Nº DE INSCRIPCIÓN
- [ ] SEDE

## Normas que cita el formulario

- art. 12 Ley 41/2003

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

- Al principio del formulario: el original hablaba de «patria potestad prorrogada en virtud de sentencia de incapacitación»; conforme a la Ley 8/2021 se ha sustituido por la referencia a las medidas de apoyo judicialmente acordadas. Comprobar el tipo de medida (curatela representativa, defensor judicial, etc.), las facultades de representación que atribuye la resolución y si el negocio requiere autorización judicial (arts. 287 y 288 CC), así como la forma notarial necesaria para los bienes inmuebles.

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

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO]

CONCURREN

DE UNA PARTE,

Don [NOMBRE Y APELLIDOS], mayor de edad, profesión [PROFESIÓN], y provisto de D.N.I. n.º [DNI/NIE], y Doña [NOMBRE Y APELLIDOS], mayor de edad, profesión [PROFESIÓN], y provista de D.N.I. n.º [DNI/NIE], matrimonio, con domicilio en [LOCALIDAD], calle [CALLE Y NÚMERO] n.º [Nº].

Y DE OTRA,

Don [NOMBRE Y APELLIDOS], mayor de edad, estado civil [ESTADO CIVIL], abogado, con despacho profesional en [LOCALIDAD], calle [CALLE Y NÚMERO], y provisto de D.N.I. n.º [DNI/NIE].

INTERVIENEN

Los dos primeros en su propio nombre y derecho, cónyuges por matrimonio [ELEGIR: canónico / civil] celebrado el [DÍA] de [MES] de [AÑO], y en la representación legal que ostentan de D./Dña. [NOMBRE Y APELLIDOS DEL ALIMENTISTA], su hijo/a común, persona con discapacidad con medidas de apoyo acordadas por resolución dictada por la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº], en fecha [DÍA] de [MES] de [AÑO].

El último, en calidad de secretario del Consejo rector de la Asociación [DENOMINACIÓN DE LA ASOCIACIÓN] de Ayuda a las Personas con Discapacidad de [LOCALIDAD], inscrita bajo n.º [Nº DE INSCRIPCIÓN] en el Registro de Asociaciones de [COMUNIDAD AUTÓNOMA], apoderado específicamente para este acto, como consta en certificación de la Junta de Consejo de [DÍA] de [MES] de [AÑO], la cual se incorpora al presente.

EXPONEN

I.- Los comparecidos, y en la calidad que intervienen, se reconocen mutuamente capacidad y representación para otorgar el presente contrato.

II.- Los progenitores de Don/Doña [NOMBRE Y APELLIDOS DEL ALIMENTISTA], en el interés de su mejor asistencia, y garantizando para el futuro quien vele por el mismo, tienen intención de concertar un CONTRATO DE ALIMENTOS en su favor.

III.- Por virtud de este contrato, la ASOCIACIÓN [DENOMINACIÓN DE LA ASOCIACIÓN], que se denominará alimentante, se obliga a proporcionar las prestaciones que se especificarán a Don/Doña [NOMBRE Y APELLIDOS DEL ALIMENTISTA], denominado alimentista, a cambio de la transmisión por Don [NOMBRE Y APELLIDOS] y Doña [NOMBRE Y APELLIDOS] del capital que también se reseña.

IV.- El contrato se regirá por lo prevenido en los artículos 1.791 a 1.797 del Código Civil, en la redacción que les concediera el artículo 12 de la Ley 41/2003, de 18 de noviembre, de protección patrimonial de las personas con discapacidad, en todo lo que no contravenga las siguientes:

ESTIPULACIONES

Primera.- Prestaciones para el alimentista

1.1. Los alimentos convencionales que se obliga a prestar la ASOCIACIÓN [DENOMINACIÓN DE LA ASOCIACIÓN], consistirán en el alojamiento, manutención, y asistencia integral de Don/Doña [NOMBRE Y APELLIDOS DEL ALIMENTISTA] en la Residencia asistida [DENOMINACIÓN DE LA RESIDENCIA], de [LOCALIDAD], con inclusión de todos los servicios de la misma, ya se dispensen mediante el abono de la tarifa ordinaria de hospedaje o no, en la reposición de su vestuario de conformidad con los usos y costumbres del lugar, así como en una asignación por meses anticipados para gastos menores de [IMPORTE EN LETRA] euros ([IMPORTE] €), actualizable cada primero de año conforme la evolución del índice de precios al consumo del territorio de [TERRITORIO], publicado por el Instituto Nacional de Estadística u organismo que le sustituya en su función.

1.2. De producirse la eventualidad de la desaparición de la Residencia asistida [DENOMINACIÓN DE LA RESIDENCIA], de [LOCALIDAD], la prestación de alimentos se convertirá, a elección de la entidad alimentante, en una pensión mensual de [IMPORTE EN LETRA] euros ([IMPORTE] €), actualizable cada primero de año conforme la evolución del índice de precios al consumo del territorio de [TERRITORIO], publicado por el Instituto Nacional de Estadística u organismo que le sustituya en su función, pagadera dentro de los cinco días de cada mes, o en el alojamiento, manutención y asistencia integral en otra Residencia asistida del territorio de [TERRITORIO], hasta el valor equivalente de dicha pensión.

Segunda.- Duración

Las prestaciones en favor del alimentista se pactan durante todo el tiempo de su vida, salvo extinción previa del presente contrato.

Tercera.- Aportaciones al alimentante

3.1. El capital que transmiten Don [NOMBRE Y APELLIDOS] y Doña [NOMBRE Y APELLIDOS], consiste en:

Inmuebles: [DESCRIPCIÓN PRECISA, CON VALORACIÓN Y DATOS REGISTRALES].

Valores mobiliarios: [DESCRIPCIÓN Y VALORACIÓN].

Fondos dinerarios: [IMPORTE].

[Nota: describir con precisión las aportaciones, con valoración de las no dinerarias y expresión de la identificación registral de los bienes registrables.]

3.2. Los anteriores bienes y derechos son de exclusiva propiedad de la comunidad conyugal de Don [NOMBRE Y APELLIDOS] y Doña [NOMBRE Y APELLIDOS], y se transmiten libres de cargas y gravámenes, arrendatarios, y limitaciones administrativas, y la presente escritura conforma la tradición simbólica de la posesión de los bienes materiales aportados por el título contractual, cuyo dominio así se transfiere a la ASOCIACIÓN [DENOMINACIÓN DE LA ASOCIACIÓN].

3.3. Las vicisitudes de los bienes y derechos, una vez que se transmiten, no afectarán a la extensión y calidad de las prestaciones de alimentos que son obligación en favor de Don/Doña [NOMBRE Y APELLIDOS DEL ALIMENTISTA] de la nueva titular.

3.4. En garantía de la restitución del capital transmitido para caso de resolución por incumplimiento de la obligación de alimentos, y demás supuestos de resolución por causa legal o convencional, se pacta la inscripción de la condición resolutoria expresa en el Registro de la Propiedad de [LOCALIDAD], en la finca [DATOS REGISTRALES].

Cuarta.- Resolución del contrato

4.1. Corresponde a la representación legal del alimentista la facultad de resolución del presente contrato, conforme al régimen legal de la resolutoria de obligaciones recíprocas, además de por el incumplimiento de cualquiera de las obligaciones de prestación de alimentos, por:

1) La disolución de la ASOCIACIÓN [DENOMINACIÓN DE LA ASOCIACIÓN], por cualquier causa legal o estatutaria.

2) Por los indicios de que la ASOCIACIÓN [DENOMINACIÓN DE LA ASOCIACIÓN] ha recaído en situación de insolvencia, revelada por haber sido solicitada la declaración de su concurso.

4.2. Para el caso de resolución ejercitada por la representación legal del alimentista, la restitución de los bienes y derechos transmitidos al alimentante deberá producirse en el plazo de quince días siguientes al requerimiento fehaciente.

La restitución en tal caso de las prestaciones devengadas y percibidas por el alimentista, se sujetará a las siguientes reglas:

a) Mediante la venta de los bienes y derechos restituidos realizables, realizada a tercero o terceros, o la cesión a la alimentante ASOCIACIÓN [DENOMINACIÓN DE LA ASOCIACIÓN] de alguno de ellos mediante su valoración objetiva a la fecha, emitida por la empresa especializada [EMPRESA VALORADORA], incrementada en un veinte por ciento.

b) El importe de dinero o valor en bienes se corresponderá con el importe actualizado de las prestaciones alimenticias realmente recibidas, siempre que reste un superávit para Don/Doña [NOMBRE Y APELLIDOS DEL ALIMENTISTA], equivalente a la capitalización de la pensión mensual que se fija en el punto 1.2 de la estipulación primera por toda su esperanza de vida.

c) Si se optara por la venta a tercero y devolución pecuniaria podrá aplazarse a voluntad de la representación legal de Don/Doña [NOMBRE Y APELLIDOS DEL ALIMENTISTA] durante el espacio de un año desde la efectiva restitución de los bienes y derechos.

Todo lo cual ratifican y suscriben de toda conformidad los intervinientes en el lugar y fecha indicados.

Firma D. [NOMBRE Y APELLIDOS]

Firma Dña. [NOMBRE Y APELLIDOS]

Firma del Secretario/a del Consejo rector de la Asociación [DENOMINACIÓN DE LA ASOCIACIÓN]
