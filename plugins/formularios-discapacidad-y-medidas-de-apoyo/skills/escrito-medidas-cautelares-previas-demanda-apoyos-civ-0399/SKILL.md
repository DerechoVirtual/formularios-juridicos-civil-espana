---
name: escrito-medidas-cautelares-previas-demanda-apoyos-civ-0399
description: "Escrito de medidas cautelares previas a la demanda de apoyos judiciales a persona con discapacidad. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito de medidas cautelares previas a la demanda de apoyos judiciales a persona con discapacidad

> Formulario **CIV-0399** del plugin **Discapacidad y medidas de apoyo (Ley 8/2021)** (`formularios-discapacidad-y-medidas-de-apoyo`) · Civil › Capacidad y medidas de apoyo · normativa revisada el 24-11-2026.

## Qué es

Escrito solicitando la adopción de medidas cautelares del artículo 762 de la LEC, previas a la demanda de adopción de medidas judiciales de apoyo a personas con discapacidad, con inventario de bienes y abstención de actos de disposición.

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito de medidas cautelares previas a la demanda de apoyos judiciales a persona con discapacidad» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito de medidas cautelares previas a la demanda de apoyos judiciales a persona con discapacidad” para mi caso». También puedes invocarla directamente con `/formularios-discapacidad-y-medidas-de-apoyo:escrito-medidas-cautelares-previas-demanda-apoyos-civ-0399`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-discapacidad-y-medidas-de-apoyo:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Discapacidad y medidas de apoyo (Ley 8/2021)) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (16 veces)
- [ ] Nº DE DOCUMENTO (8 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] Nº (3 veces)
- [ ] FECHA (2 veces)
- [ ] CALLE
- [ ] COLEGIO
- [ ] DENOMINACIÓN SOCIAL
- [ ] IMPORTE
- [ ] IMPORTE EN CIFRA
- [ ] LUGAR
- [ ] SEDE

## Normas que cita el formulario

- art. 762 LEC
- art. 756 LEC
- art. 762.3 LEC
- art. 734 LEC
- art. 721.1 LEC
- art. 726.1.1.ª LEC
- art. 728.1 LEC
- art. 728.2 LEC
- art. 768.3 LEC

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

D./Dña. [NOMBRE Y APELLIDOS], Procurador de los Tribunales, en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS], vecino de [LOCALIDAD] calle [CALLE], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], ante el Tribunal comparezco, bajo la dirección técnica de D./Dña. [NOMBRE Y APELLIDOS], Letrado del Ilustre Colegio de Abogados de [COLEGIO], con despacho profesional en [LOCALIDAD], y como mejor proceda en Derecho DIGO:

Que por medio del presente escrito vengo a instar la tutela cautelar específica del art. 762 LEC, en base a los siguientes

HECHOS

PRIMERO.- D./Dña. [NOMBRE Y APELLIDOS], hermano del demandante, tal y como se acredita con el Libro de Familia que se aporta como documento número [Nº DE DOCUMENTO], tiene en la actualidad [Nº] años de edad, y durante toda su vida ha permanecido en el domicilio de sus padres, hasta que estos fallecieron en fecha [FECHA] en desgraciado accidente de tráfico, asumiendo desde entonces mi representado el cuidado y las atenciones que requiere su hermano debido a la enfermedad que padece.

A partir de dicho momento, D./Dña. [NOMBRE Y APELLIDOS] ha convivido en el domicilio de mi representado junto a éste y su familia.

Se acompañan los certificados de defunción de los progenitores como documentos número [Nº DE DOCUMENTO] y [Nº DE DOCUMENTO].

SEGUNDO.- D./Dña. [NOMBRE Y APELLIDOS] está diagnosticado de esquizofrenia residual crónica, tal y como se recoge en el dictamen emitido por el Doctor en Psiquiatría D./Dña. [NOMBRE Y APELLIDOS], con una evolución de la misma desde hace [Nº] años, que, dada su gravedad y cronicidad, mínimamente modificada por el tratamiento neuroléptico, le origina un alto grado de discapacidad para que pueda gobernar su persona y bienes.

En la actualidad, y como consecuencia de su situación psicopatológica, D./Dña. [NOMBRE Y APELLIDOS] necesita tratamiento neuroléptico y vigilancia permanente por parte de médico especialista, tal y como se acredita con los informes médicos que se acompañan como documentos números [Nº DE DOCUMENTO] y [Nº DE DOCUMENTO].

El cumplimiento del tratamiento farmacológico y el control médico psiquiátrico ambulatorio es esencial para D./Dña. [NOMBRE Y APELLIDOS], de manera que cuando padece síntomas de descompensación psicótica, ha tenido que ser internado (Se aporta informe médico de la Dr./a [NOMBRE Y APELLIDOS], Psiquiatra del Centro de Salud Mental de [LOCALIDAD], en que se consigna el historial de internamientos, como documento número [Nº DE DOCUMENTO]).

TERCERO.- Como consecuencia de la enfermedad que sufre, desde que quedó al cuidado de mi representado D./Dña. [NOMBRE Y APELLIDOS] sufre trastornos conductuales importantes que dificultan su convivencia social y cuya principal manifestación es la de disipar compulsivamente su virtualmente única fuente de ingresos consistente en un fondo de inversión en la entidad [DENOMINACIÓN SOCIAL], ya que únicamente percibe una exigua pensión de la Seguridad Social, insuficiente por sí sola para subvenir a las necesidades que motiva el tratamiento de su enfermedad.

La habitualidad y permanencia de esa conducta de D./Dña. [NOMBRE Y APELLIDOS], en cuanto a la dilapidación de su patrimonio, resulta de los siguientes acontecimientos:

A la acreditación de estos detalles, de adjuntan [Nº DE DOCUMENTO]

El riesgo que supone esperar a la demanda que se formulará y posterior sentencia de provisión de medidas de apoyo motiva esta solicitud de adopción de medidas cautelares.

FUNDAMENTOS DE DERECHO

I.- COMPETENCIA.

La competencia para conocer de las solicitudes de medidas cautelares si el proceso no se hubiere iniciado, corresponde a la Sección Civil del Tribunal de Instancia del lugar de residencia del sujeto de la cautela, que es el Tribunal competente para conocer de la demanda principal (art. 723.1 en relación con el art. 756 LEC).

II.- PROCEDIMIENTO.

El art. 762.3 LEC establece que las medidas cautelares se acordarán previa audiencia de la personas afectadas, siendo de aplicación lo dispuesto en los arts. 734, 735 y 736 LEC.

III.- MEDIDA SOLICITADA

1.- Justificación. Con objeto de asegurar la efectividad de la tutela judicial que pudiera otorgarse en la sentencia estimatoria que se dictare (art. 721.1 LEC), de modo que no pueda verse impedida o dificultada por situaciones producidas durante la pendencia del proceso correspondiente (art. 726.1.1.ª LEC), hay posibilidad de acordar, respecto de los bienes y derechos del demandado, medidas cautelares para protección del presunto incapaz y de su patrimonio (art. 762.2 párrafo 2.º LEC).

Las medidas cautelares que se solicitan en concreto son las del art. 727.4.ª y 7.ª LEC de formación de inventario de bienes del demandado, y de abstención temporal de llevar a cabo determinadas conductas inminentes, concretamente las consistentes en ‘non facere’ con relación a la enajenación del fondo de inversión que obra en la entidad bancaria

2.- Presupuestos. Son presupuestos de la adopción de medidas cautelares, el peligro de retardo o ‘periculum in mora’ (art. 728.1 LEC), y la apariencia de buen derecho o ‘fumus boni iuris’ (art. 728.2 LEC), que se derivan de la simple exposición fáctica de este escrito.

No puede dudarse, y está documentado que, sin ningún sentido, más en práctica autodestructiva, se está dilapidando un patrimonio que constituye virtualmente la única fuente de ingresos de D./Dña. [NOMBRE Y APELLIDOS]

Con independencia de la determinación de la extensión y límites de la declaración de discapacidad que se pretenda, así como del régimen de curatela o guarda al que haya de quedar sometido el discapacitado, esta parte entiende que tampoco puede dudarse del peligro de infructuosidad, una vez deducida la demanda, por cuanto durante su preparación puede precisamente acelerarse el proceso de dilapidación.

3.- Caución. Aunque es requisito de la ejecución de las medidas cautelares la prestación de caución, para responder de los daños y perjuicios que la adopción de la medida cautelar pudiera causar al demandado, debe tenerse presente que la restricción temporal de la libertad de disponibilidad económica del demandado difícilmente puede razonarse que le perjudique en el presente caso, y que son medidas de protección de la persona y su patrimonio por las que deben velar la Fiscalía y la misma Jurisdicción, por lo que, en analogía con lo prevenido en el art. 768.3 ‘in fine’ LEC, se solicita la dispensa de caución.

Subsidiariamente, se ofrece prestar caución por importe de [IMPORTE] euros, sin perjuicio de lo que fije S. Sª. Iltma. oídas las partes.

Por todo lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por recibida está presente solicitud de medidas cautelares junto con sus copias y documentos que la acompañan, se digne admitirla y convocando por el Letrado de la Administración de Justicia a la vista a las partes, seguido que sea el oportuno trámite, dicte auto por el que se disponga, sin caución ninguna, o previa la prestación de la caución por la actora en la cuantía ofrecida deeuros (€ [IMPORTE EN CIFRA]):

a) La formación de inventario de bienes del demandado.
b) La abstención temporal del demandado de realizar actos de disposición sobre el fondo de inversión existente en la entidad bancaria, identificado como

A cuyo efecto se librará oficio prohibitorio a la citada entidad depositaria

Todo ello con imposición de la costas del proceso cautelar a la parte contraria, si se resistiere a la adopción de la medida.

Es Justicia en [LUGAR], a [FECHA].

OTROSÍ DIGO que interesa al derecho de esta parte valerse para la vista de los siguientes medios de prueba:

DOCUMENTAL, consistente en la unión definitiva a los autos de los [Nº] documentos aportados con este escrito.

TESTIFICAL de los siguiente tres individuos, que se manifiesta acudirán voluntariamente a la citación judicial de esta parte:

D./Dña. [NOMBRE Y APELLIDOS], D./Dña. [NOMBRE Y APELLIDOS], y D./Dña. [NOMBRE Y APELLIDOS]

SUPLICO AL TRIBUNAL que, teniendo por causada la anterior manifestación al efecto oportuno, se digne proveer conforme a lo solicitado, como es Justicia que reitero en lugar y fecha que ya consta.

Firma de Abogado/a	Firma de Procurador/a

========================================================================
