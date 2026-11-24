---
name: expediente-jurisdiccion-voluntaria-constituir-tutela-civ-0389
description: "Expediente de jurisdicción voluntaria para constituir tutela y nombrar tutor (Aragón). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Expediente de jurisdicción voluntaria para constituir tutela y nombrar tutor (Aragón)

> Formulario **CIV-0389** del plugin **Discapacidad y medidas de apoyo (Ley 8/2021)** (`formularios-discapacidad-y-medidas-de-apoyo`) · Civil › Capacidad y medidas de apoyo · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Expediente de jurisdicción voluntaria para constituir tutela y nombrar tutor (Aragón)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Expediente de jurisdicción voluntaria para constituir tutela y nombrar tutor (Aragón)” para mi caso». También puedes invocarla directamente con `/formularios-discapacidad-y-medidas-de-apoyo:expediente-jurisdiccion-voluntaria-constituir-tutela-civ-0389`.
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
- [ ] NOMBRE DEL MENOR (3 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] SEDE (2 veces)
- [ ] AÑO
- [ ] CALLE
- [ ] CORREO ELECTRÓNICO
- [ ] DÍA
- [ ] LUGAR
- [ ] MES
- [ ] Nº

## Normas que cita el formulario

- art. 44 LJV

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

### Avisos de actualización (3) — se aplican en el texto, nunca se copian en el documento

- Junto a «…MILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.
- Junto a «…recho Foral de Aragón, ante la Sección Civil del Tribunal de Instancia de [SEDE]»: Un solo TI por partido judicial (art. 84.1 LOPJ): sobra «de los de». Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

D. [NOMBRE Y APELLIDOS], actuando en su nombre y representación, menor de edad emancipado por resolución de fecha [FECHA], y bajo la dirección Letrada de Don [NOMBRE Y APELLIDOS], al amparo de lo dispuesto en el artículo 130 y siguientes del Código de Derecho Foral de Aragón, ante la Sección Civil del Tribunal de Instancia de [SEDE] que por turno de reparto corresponda comparezco y, como mejor proceda en Derecho, DIGO:

Que mediante el presente escrito promueve expediente de jurisdicción voluntaria para NOMBRAMIENTO DE TUTOR respecto del menor [NOMBRE DEL MENOR], de [Nº] años de edad, de vecindad civil aragonesa, con domicilio en [LOCALIDAD], en base a los siguientes

HECHOS

Que el solicitante es hermano de la difunta madre y tío carnal del menor [NOMBRE DEL MENOR], de .. años de edad, el cual se halla en situación de sujeción a tutela al haber fallecido ambos padres en fecha [FECHA] y no encontrarse sujeto a autoridad familiar (se acompañan como documentos [Nº DE DOCUMENTO] certificados de defunción de ambos padres), por lo que en cumplimiento de lo dispuesto en el artículo 131 del Código de Derecho Foral de Aragón, por medio del presente escrito promueve la constitución de la tutela del menor

En efecto en fecha [FECHA] falleció la madre del menor y hermana del solicitante Dª [NOMBRE Y APELLIDOS], y poco después falleció el padre [NOMBRE Y APELLIDOS], teniendo como único hijo al menor [NOMBRE DEL MENOR], debiendo constituirse la tutela respecto de éste por cuanto que no existen otros parientes que puedan ejercitar la autoridad familiar, al haber fallecido todos los abuelos, además de haber sido designado como tutor el solicitante en testamento de fecha [FECHA] como se expondrá seguidamente.

Al margen del solicitante, la madre tiene otros dos hermanos D. y D. [NOMBRE Y APELLIDOS], en tanto que el padre del menor tiene un hermano D. [NOMBRE Y APELLIDOS], tal como se acredita con los certificados de nacimiento que se acompañan.

Habiendo fallecido ambos padres, y en previsión de ello, dados los lazos afectivos y de confianza con mi representado, éstos designaron como tutor de su hijo al solicitante para el caso de fallecimiento de ambos progenitores, tal como se acredita por el testamento de fecha [FECHA] que se acompaña a la presente solicitud como documento número [Nº DE DOCUMENTO]., debiendo estarse a dicha delación conforme a lo que dispone el 114 del Código de Derecho Foral de Aragón.

En relación al nombramiento, debe hacerse constar que, tal como se acreditará en este procedimiento, el demandante no incurre en ninguna de las causas de inhabilidad del artículo 124 del Código, acompañando a efectos acreditativos como documento [Nº DE DOCUMENTO] certificado negativo de antecedentes penales, y que es la persona más idónea para el ejercicio de la tutela, por cuanto que el menor se puede integrar en el núcleo familiar, al tener dos hijos de edad similar a la de su sobrino, teniendo una especial relación afectiva con la familia del solicitante, con quien actualmente está conviviendo, por lo que es indudable que defenderá los intereses del menor como si fueran propios.

FUNDAMENTOS DE DERECHO

Competencia

Son competentes las secciones civiles de los tribunales de instancia de esta ciudad, por ser el del domicilio del menor.

Procedimiento

Debe seguirse el procedimiento de jurisdicción voluntaria regulado en los artículos 44 y siguientes de la LJV, y artículos 130 y siguientes del Código de Derecho Foral de Aragón.

Legitimación

Esta parte está legitimada conforme a lo dispuesto en el art. 131 del Código de Derecho Foral de Aragón, el cual establece que "estarán obligados a promover la constitución de la tutela desde el momento en que conocieren el hecho que la motiva los llamados a ella por disposición voluntaria y los mencionados en las letras a) y b) del apartado 1 del artículo 121. También, desde el momento en que conocieren el hecho que motiva la tutela, los llamados a ella por delación voluntaria, así como la persona bajo cuya guarda se encuentre el menor.

Fundamentos de fondo

El art. 130 del Código de Derecho Foral de Aragón establece que estarán sujetos a tutela ordinaria los menores no emancipados que no estén bajo la autoridad familiar, en tanto que e artículo 110 del mismo Código regula la delación hecha por titulares de la autoridad familiar, estableciendo que las mismas disposiciones "podrán adoptar en instrumento público notarial, sea o no testamento, los titulares del ejercicio de la autoridad familiar respecto de la persona o bienes de los menores que sigan bajo su autoridad para cuando llegue el día en el que ya no puedan ocuparse de ellos y deban quedar sujetos a tutela"; las delación testamentaria será eficaz al fallecimiento del testador salvo que entonces se hallara privado por su culpa del ejercicio de la autoridad familiar; las hechas en escritura pública lo serán además en caso de que el disponente no pueda ejercer la autoridad familiar por causa no culpable, solicitando que por todo ello que sea nombrado como tutor el solicitante D. [NOMBRE Y APELLIDOS], el cual fue designado por los padres del menor para el ejercicio del cargo.

Por lo expuesto,

AL TRIBUNAL SUPLICO: Que tenga por presentado este escrito con los documentos que se acompañan, lo admita, y tenga por promovido expediente de jurisdicción voluntaria de constitución de tutela y nombramiento de tutor del solicitante, y practicadas las diligencias oportunas, incluida la información testifical que se interesa en el otrosí y con intervención del Ministerio Fiscal, y previos los demás trámites con arreglo a Derecho dicte resolución en la que se nombre curador a D. [NOMBRE Y APELLIDOS] para que complemente la capacidad del solicitante en la venta de la vivienda sita en [LOCALIDAD], calle [CALLE] de su propiedad.

OTROSÍ PRIMERO DIGO que a efectos de comunicaciones designo el domicilio del letrado firmante de este escrito sito en [LOCALIDAD], así como la dirección de correo electrónico del mismo [CORREO ELECTRÓNICO] y el número de fax

SUPLICO AL TRIBUNAL: tenga por hecha la citada designación de domicilio.

OTROSÍ SEGUNDO DIGO: Que acreditar la certeza de los hechos relatados, solicito que sean oídos los tíos del menor D. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], y D. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], y asimismo ofrezco los siguientes testigos:

- D. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD]

- [NOMBRE Y APELLIDOS]

SUPLICO AL TRIBUNAL: Tenga por propuestos a los testigos indicados, admitiendo la testifical ofrecida, comprometiéndose esta parte a que comparezcan en el día y hora que se señale (o, en su caso, solicitando que sean citados judicialmente para la práctica de la diligencia).

Es Justicia que insto en [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma del solicitante y letrado

========================================================================
