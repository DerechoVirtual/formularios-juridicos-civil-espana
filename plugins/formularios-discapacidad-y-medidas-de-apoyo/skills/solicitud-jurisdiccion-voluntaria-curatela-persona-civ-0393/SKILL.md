---
name: solicitud-jurisdiccion-voluntaria-curatela-persona-civ-0393
description: "Solicitud en jurisdicción voluntaria de curatela para persona con ludopatía grave. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud en jurisdicción voluntaria de curatela para persona con ludopatía grave

> Formulario **CIV-0393** del plugin **Discapacidad y medidas de apoyo (Ley 8/2021)** (`formularios-discapacidad-y-medidas-de-apoyo`) · Civil › Capacidad y medidas de apoyo · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud en jurisdicción voluntaria de curatela para persona con ludopatía grave» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud en jurisdicción voluntaria de curatela para persona con ludopatía grave” para mi caso». También puedes invocarla directamente con `/formularios-discapacidad-y-medidas-de-apoyo:solicitud-jurisdiccion-voluntaria-curatela-persona-civ-0393`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-discapacidad-y-medidas-de-apoyo:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Discapacidad y medidas de apoyo (Ley 8/2021)) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (12 veces)
- [ ] LOCALIDAD (6 veces)
- [ ] FECHA (5 veces)
- [ ] AÑO (2 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] LUGAR (2 veces)
- [ ] DNI/NIE
- [ ] DÍA
- [ ] ESTUDIOS
- [ ] IMPORTE
- [ ] MES
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] Nº
- [ ] PROFESIÓN
- [ ] REFERENCIAS CATASTRALES
- [ ] SEDE

## Normas que cita el formulario

- art. 85.1 LOPJ
- art. 199 CC

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

- Junto a «…MILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
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

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D/Dª [NOMBRE Y APELLIDOS] Procurador de los Tribunales actuando en nombre y representación de D/Dª [NOMBRE Y APELLIDOS], mayor de edad, casado, de profesión [PROFESIÓN], vecino de esta ciudad C/, según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño a este escrito, actuando bajo la dirección Letrada de D/Dª [NOMBRE Y APELLIDOS], Colegiado/a núm. con domicilio profesional en [LOCALIDAD], ante el Tribunal comparezco y como mejor proceda en Derecho DIGO:

Que en la indicada representación formulo EXPEDIENTE DE JURISDICCIÓN VOLUNTARIA DE MEDIDA DE APOYO —CURATELA— DE D. [NOMBRE Y APELLIDOS], provisto de DNI [DNI/NIE], nacido en [LOCALIDAD] en fecha [FECHA], de estado civil casado, con domicilio en [LOCALIDAD], se aporta como DOCUMENTO NÚM. 1 certificación literal de nacimiento expedida por el Registro Civil de [LOCALIDAD], todo ello en base a los siguientes

HECHOS

PRIMERO.- Mi representada es la única hija habida en el matrimonio que contrajo el demandado con Dª [NOMBRE Y APELLIDOS] en fecha [FECHA], tal y como consta en DOCUMENTO NÚM. 1 certificación literal de expedida por el Registro Civil de [LOCALIDAD] La que fue esposa de D [NOMBRE Y APELLIDOS] falleció en el año [AÑO], tal y como se acredita mediante la aportación como DOCUMENTO NÚM. 2 de la declaración de fallecimiento.

SEGUNDO.- El demandado, empresario del sector automovilístico, poseía en el año 2003, es decir hace tan sólo dos años, un patrimonio que rondaba el millón de euros. El mismo se encontraba compuesto por inmuebles, activos financieros, cuentas corrientes que fueron recogidos en el informe de auditoría que se presenta como DOCUMENTO NÚM. 2.

TERCERO.- Desde hace aproximadamente dos años D. padece una ludopatía severa que le fue diagnosticada por el Doctor en psiquiatría D. [NOMBRE Y APELLIDOS], se aporta informe detallado como DOCUMENTO NÚM. 3.

CUARTO.- La adicción al juego ha llevado a que D. haya abandonado su actividad empresarial dilapidando más de la mitad de su patrimonio en tan sólo dos años. Se aporta como DOCUMENTO NÚM. 4 informe expedido por el Auditor de cuentas colegiado D. [NOMBRE Y APELLIDOS] en fecha [FECHA] en el que se observan las ventas de dos fincas urbanas y tres rústicas con referencias catastrales [REFERENCIAS CATASTRALES], así como la disposición de activos financieros por importe de [IMPORTE] Euros.

Asimismo se aporta como DOCUMENTO NÚM. 5 informe con soporte audiovisual realizado por el Investigador Privado D [NOMBRE Y APELLIDOS] con licencia gubernativa núm. [Nº] en el que se detallan las frecuentes visitas del demandado a los diferentes casinos y centros de juego que en él se recogen tanto de la geografía nacional como internacional.

QUINTO.- Mi representada se encuentra cursando los estudios universitarios de [ESTUDIOS] en la ciudad de [LOCALIDAD]. Hasta la fecha ha venido compaginando su actividad académica con la laboral realizando prácticas remuneradas en la empresa [DENOMINACIÓN SOCIAL] SL si bien su contrato finalizó en fecha [FECHA] no desempañando en la actualidad actividad laboral alguna, negándose su progenitor a prestarle ayuda alguna. Se aporta como DOCUMENTO NÚM. 6 resguardo de matrícula universitaria, como DOCUMENTO NÚM. 7 recibos de la residencia universitaria en la que se encuentra hospedada y DOCUMENTO NÚM. 8 la comunicación de la expiración del contrato de prácticas suscrito con la empresa [DENOMINACIÓN SOCIAL] SL.

A los anteriores hechos le son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

I. COMPETENCIA

De acuerdo con lo establecido en los artículos 2 y 43 de la Ley de la Jurisdicción Voluntaria, en la nueva redacción dada por la Ley 8/2021, de 2 de junio, en relación con lo dispuesto en el art. 85.1º LOPJ, corresponderá la competencia a la Sección Civil del Tribunal de Instancia al que me dirijo, por resultar que el demandado tiene su domicilio en la misma.

II. PROCEDIMIENTO

Se tramitará conforme a lo dispuesto en los artículos 44 y 45 de la Ley de la Jurisdicción Voluntaria, en la nueva redacción dada por la Ley 8/2021, de 2 de junio.

El expediente se iniciará mediante solicitud presentada en nuestro caso por la persona legalmente indicada para promover la curatela, expresando el hecho que dé lugar a ésta y acompañando los documentos acreditativos de la situación y legitimación.

En la comparecencia se oirá al promotor, a la persona cuya designación se proponga si fuera distinta al promotor, a aquel cuya curatela se pretenda constituir si fuera mayor de 12 años, a los parientes más próximos, al Ministerio Fiscal, y a cuantas personas se considere oportuno.

El Juez designará curador a la persona o determinadas, de conformidad con lo prevenido en el Código Civil.

En la resolución acordando el nombramiento de tutor o curador, se adoptarán las medidas de fiscalización de la tutela o curatela establecidas por los progenitores en testamento o documento público notarial, o por el propio afectado en el documento público notarial otorgado al respecto salvo que sea otro el interés de la persona afectada.

Cuando corresponda de acuerdo con la legislación civil aplicable, en la resolución por la que se constituya la curatela, el Juez podrá acordar las medidas de vigilancia y control oportunas, así como exigir al curador informe sobre la situación personal del menor o persona con discapacidad y el estado de la administración de sus bienes.

El Juez, en la resolución por la que constituya la curatela o en otra posterior, podrá exigir al tutor o curador de modo excepcional la constitución de fianza que asegure el cumplimiento de sus obligaciones, debiendo determinar, en tal caso, la modalidad y cuantía de la misma.

III. LEGITIMACIÓN ACTIVA

Corresponde a mi representada, de acuerdo con lo establecido en el artículo 42 bis a) 3 de la Ley de la Jurisdicción Voluntaria.

“Podrá promover este expediente el Ministerio Fiscal, la propia persona con discapacidad, su cónyuge no separado de hecho o legalmente o quien se encuentre en una situación de hecho asimilable y sus descendientes, ascendientes o hermanos”.

En nuestro caso, la demandante es descendiente del curatelable.

IV. LEGITIMACIÓN PASIVA

Corresponderá al demandado de acuerdo con lo establecido en la referencia fáctica realizada, así como en el artículo 199 CC.

V. MEDIDAS DE APOYO A PERSONAS CON DISCAPACIDAD.

Artículos 268 a 298 del Código Civil, en la nueva redacción dada por la Ley 8/2021 de 2 de junio.

La autoridad judicial constituirá la curatela mediante resolución motivada cuando no exista otra medida de apoyo suficiente para la persona con discapacidad.

La autoridad judicial determinará los actos para los que la persona requiere asistencia del curador en el ejercicio de su capacidad jurídica atendiendo a sus concretas necesidades de apoyo.

Sólo en los casos excepcionales en los que resulte imprescindible por las circunstancias de la persona con discapacidad, la autoridad judicial determinará en resolución motivada los actos concretos en los que el curador habrá de asumir la representación de la persona con discapacidad.

Los actos en los que el curador deba prestar el apoyo deberán fijarse de manera precisa, indicando, en su caso, cuáles son aquellos donde debe ejercer la representación. El curador actuará bajo los criterios fijados en el artículo 249.

En ningún caso podrá incluir la resolución judicial la mera privación de derechos.

VI. FUNDAMENTACIÓN JURÍDICA DE LA ACCIÓN DEDUCIDA.

En nuestro caso concreto, solicitamos que se instaure la curatela sobre D. [NOMBRE Y APELLIDOS] y que dicho nombramiento recaiga en la promotora de este expediente, su hija D.ª [NOMBRE Y APELLIDOS], solicitando que la resolución contenga expresamente los siguientes actos para los que D. precisará la intervención y apoyo de la persona que se propone como curadora:

(Se determinarán claramente los actos para los que se solicita la medida de apoyo: especialmente los actos de disposición y gravamen, así como la obligación de formalizar inventario de los bienes).

Por todo lo expuesto,

SUPLICO AL TRIBUNAL: Tenga por presentado el presente escrito junto con el poder que se adjunta, documentos y copias, solicitándose la devolución del poder original aportado, por ser necesario para otros usos, dándose a las copias el curso legalmente establecido, teniéndome por comparecido y parte en la representación de [NOMBRE DEL REPRESENTADO/A] Así se tenga por promovido expediente de jurisdicción voluntaria DE MEDIDA DE APOYO —CURATELA— de D. [NOMBRE Y APELLIDOS], cuyas circunstancias ya han sido reflejadas en autos y siguiendo la tramitación legalmente establecida por la vía del juicio verbal, con intervención del Ministerio Fiscal, se dicte sentencia constituyendo la curatela de D. procediéndose al nombramiento de curador con necesaria intervención al objeto de (por ejemplo: administrar sus bienes, vender, enajenar, gravarlos, transigir, renunciar, someter a arbitraje, repudiar o aceptar herencias a beneficio de inventario, ceder en arrendamiento, disponer de bienes a título gratuito, dar o tomar dinero a préstamo, ceder créditos, constituir sociedades, prestar avales o fianzas o cualesquiera otros que sean determinados en sentencia). Procédase asimismo al libramiento de las correspondientes comunicaciones al Registro Civil y de la Propiedad y demás registros públicos establecidos legalmente. Es Justicia que pido en [LUGAR], a [FECHA].

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma Abogado y Procurador

========================================================================
