---
name: expediente-jurisdiccion-voluntaria-medidas-civ-0254
description: "Expediente de jurisdicción voluntaria de medidas provisionales sobre menores (art. 158 CC). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Expediente de jurisdicción voluntaria de medidas provisionales sobre menores (art. 158 CC)

> Formulario **CIV-0254** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Expediente de jurisdicción voluntaria de medidas provisionales sobre menores (art. 158 CC)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Expediente de jurisdicción voluntaria de medidas provisionales sobre menores (art. 158 CC)” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:expediente-jurisdiccion-voluntaria-medidas-civ-0254`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE DEL MENOR (8 veces)
- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] SEDE (2 veces)
- [ ] CORREO ELECTRÓNICO
- [ ] FECHA
- [ ] IMPORTE
- [ ] NACIONALIDAD
- [ ] Nº
- [ ] PARENTESCO
- [ ] PAÍS

## Normas que cita el formulario

- art. 158 Código Civil
- art. 85.3 LJV
- art. 158.3 CC

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
- Junto a «…risdicción Voluntaria, ante la Sección Civil del Tribunal de Instancia de [SEDE]»: Un solo TI por partido judicial (art. 84.1 LOPJ): sobra «de los de». Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

D. [NOMBRE Y APELLIDOS] y D, [NOMBRE Y APELLIDOS] actuando en su nombre y representación y en interés del menor [NOMBRE DEL MENOR], con el cual nos une una relación de parentesco de [PARENTESCO], y bajo la dirección Letrada de Don [NOMBRE Y APELLIDOS], al amparo de lo dispuesto en el artículo 158 del Código Civil y en el art. 87 de la Ley de Jurisdicción Voluntaria, ante la Sección Civil del Tribunal de Instancia de [SEDE] que por turno de reparto corresponda comparezco y, como mejor proceda en Derecho, DIGO:

Que mediante el presente escrito promueve expediente de jurisdicción voluntaria para LA ADOPCIÓN DE LAS MEDIDAS CONVENIENTES PARA EVITAR LA SUSTRACCIÓN del menor [NOMBRE DEL MENOR] por parte de su progenitor [NOMBRE Y APELLIDOS] en base a los siguientes

HECHOS

PRIMERO.- Que los promotores de este expediente son abuelos maternos del menor [NOMBRE DEL MENOR], actualmente de [Nº] años de edad, quien es conocedor de esta solicitud y está conforme con la misma.

Los padres del menor son D. [NOMBRE Y APELLIDOS], de nacionalidad [NACIONALIDAD] y la hija de los solicitantes Dª..

Ambos padres tuvieron una relación de convivencia ya finalizada de la que nació el menor [NOMBRE DEL MENOR], siguiéndose proceso civil para determinar su guarda y custodia y alimentos en el que se dictó sentencia de fecha [FECHA] en el que se atribuía la misma a la madre [NOMBRE Y APELLIDOS], fijándose un régimen de visitas a favor del padre, quien debía satisfacer una pensión mensual de [IMPORTE] euros Como quiera que la madre inició otra relación con otra persona y no quiso hacerse cargo del menor, éste paso a residir con los abuelos, quienes se ocupan de él desde hace años. En todo este tiempo, el padre apenas ha visitado al hijo en un par de ocasiones, no habiendo abonado en ningún momento la pensión a que viene obligado.

SEGUNDO.- Pese a que el padre del menor se ha desentendido totalmente de sus obligaciones personales y económicas con su hijo, recientemente ha visitado al menor en dos ocasiones, en dos fines de semana, en el cual le ha insistido en que debe irse a vivir con él a su país de origen [PAÍS], propósito de total seriedad por cuanto obligó a ir al menor a las dependencias de la Policía Nacional en [LOCALIDAD] a efectos de que le fuera expedido el pasaporte.

Según hemos podido saber, al parecer el padre tiene otra familia en su país de origen y pretende llevarse al menor [NOMBRE DEL MENOR] a vivir con él, habiendo manifestado a algunos conocidos que "es su hijo y se lo puede llevar cuando quiera".

Por tanto, existe un patente riesgo de sustracción del menor por parte del padre que, de materializarse, produciría gravísimos perjuicios al menor, que se opone radicalmente a irse a vivir con su padre, con quien no ha tenido ninguna relación y que se ha despreocupado totalmente de él, a la vez que se rompería totalmente cualquier lazo del menor con sus abuelos, pues se desconoce cualquier dato sobre el domicilio o residencia del padre en su país de origen.

A fin de acreditar estos extremos, interesamos que sea oído el menor [NOMBRE DEL MENOR] y ofrecemos información testifical de las personas que indicamos en el otrosí, quienes conocen perfectamente la situación personal, familiar y social del menor.

TERCERO.- Que a fin y efecto de evitar la sustracción del menor por parte de su padre, solicitamos que se adopten las medidas que se estimen convenientes, proponiéndose que se prohíba la expedición de pasaporte al menor y que se prohíba la salida del territorio nacional, salvo autorización judicial previa.

FUNDAMENTOS DE DERECHO

PRIMERO.- 1) COMPETENCIA. Son competentes las secciones civiles de los tribunales de instancia de esta ciudad, por ser el del domicilio del menor, conforme a lo dispuesto en el art. 87.2 de la Ley de Jurisdicción Voluntaria.

SEGUNDO.- PROCEDIMIENTO. Debe seguirse el procedimiento de jurisdicción voluntaria regulado en los artículos 87 y siguientes de la Ley de Jurisdicción Voluntaria.

TERCERO.- LEGITIMACIÓN. Esta parte está legitimada conforme a lo dispuesto en el art. 158 del Código Civil y art. 87.1 de la Ley de Jurisdicción Voluntaria, no siendo preceptiva la intervención de Abogado ni Procurador conforme al art. 85.3 LJV.

CUARTO.- FUNDAMENTOS DE FONDO. El art. 158 del Código Civil establece, entre otras prescripciones, que el juez adoptará las medidas necesarias para evitar la sustracción de los hijos menores por algunos de los progenitores o por terceras personas y en general todas aquellas medidas para evitar peligro al menor o evitarle perjuicio, debiendo aplicarse este precepto teniendo en cuenta el prevalente interés del menor. En particular, conforme al art. 158.3º CC, puede adoptar las siguientes medidas: a) Prohibición de salida del territorio nacional, salvo autorización judicial previa; b) Prohibición de expedición del pasaporte al menor o retirada del mismo si ya se hubiere expedido; y c) Sometimiento a autorización judicial previa de cualquier cambio de domicilio del menor.

Por lo expuesto,

AL TRIBUNAL SUPLICO: Que tenga por presentado este escrito, lo admita, y por promovido expediente de jurisdicción voluntaria de medidas de protección en relación al menor, y practicadas las diligencias oportunas, con audiencia del menor, práctica de la información testifical interesada y con intervención del Ministerio Fiscal, y previos los demás trámites con arreglo a Derecho dicte resolución en forma de auto en la que se acuerde la adopción de las medidas necesarias para evitar la sustracción del menor [NOMBRE DEL MENOR] por su padre biológico [NOMBRE Y APELLIDOS], tal como se solicitan en el hecho tercero de este escrito.

OTROSÍ PRIMERO DIGO que a efectos de comunicaciones designo el domicilio del letrado firmante de este escrito sito en [LOCALIDAD], así como la dirección de correo electrónico del mismo [CORREO ELECTRÓNICO] y el número de fax

SUPLICO AL TRIBUNAL: tenga por hecha la citada designación de domicilio.

OTROSÍ SEGUNDO DIGO: Que acreditar la certeza de los hechos relatados, solicito que sea oído el menor [NOMBRE DEL MENOR] y ofrezco los siguientes testigos que, por razón de su conocimiento de los hechos, pueden declarar sobre la situación del menor y el riesgo de sustracción por parte de su padre biológico:

- D. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD]

-.

SUPLICO AL TRIBUNAL: Tenga por propuestos a los testigos indicados, admitiendo la testifical ofrecida, comprometiéndose esta parte a que comparezcan en el día y hora que se señale.

Es Justicia que insto en [LOCALIDAD].

========================================================================
