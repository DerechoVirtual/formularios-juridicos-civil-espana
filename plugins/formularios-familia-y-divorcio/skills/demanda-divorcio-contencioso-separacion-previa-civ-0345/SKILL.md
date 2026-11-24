---
name: demanda-divorcio-contencioso-separacion-previa-civ-0345
description: "Demanda de divorcio contencioso con separación previa y modificación provisional de las medidas. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de divorcio contencioso con separación previa y modificación provisional de las medidas

> Formulario **CIV-0345** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Demanda de divorcio contencioso, con separación judicial previa, y solicitando la modificación provisional de las medidas definitivas aprobadas en la separación.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de divorcio contencioso con separación previa y modificación provisional de las medidas» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de divorcio contencioso con separación previa y modificación provisional de las medidas” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-divorcio-contencioso-separacion-previa-civ-0345`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (9 veces)
- [ ] IMPORTE (7 veces)
- [ ] LOCALIDAD (6 veces)
- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] NÚMERO (5 veces)
- [ ] Nº (4 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] CALLE (2 veces)
- [ ] FECHA DE NACIMIENTO (2 veces)
- [ ] NOMBRE DEL HIJO/A (2 veces)
- [ ] COLEGIO
- [ ] DATOS DEL PROCEDIMIENTO ANTERIOR
- [ ] DIRECCIÓN
- [ ] DOMICILIO
- [ ] FECHAS
- [ ] LUGAR
- [ ] SEDE
- [ ] TIPO Y Nº DE PROCEDIMIENTO

## Normas que cita el formulario

- art. 86 CC
- art. 769.1 LEC
- art. 770 LEC
- art. 251 LEC
- art. 437.1 LEC
- art. 5 Ley Orgánica 1/2025
- art. 81.2.º CC
- art. 91 CC
- art. 394 LEC
- art. 775.3 LEC

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

- Junto a «…ELEGIR: SECCIÓN CIVIL / SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD] DE [LOCALIDAD]»: Denominación legal: Sección de Familia, Infancia y Capacidad. Si no existe en el partido, conoce la Sección Civil o la Única (art. 86.3-4 LOPJ). Fuente: LOPJ arts. 84.2.a) y 86 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…IPO Y Nº DE PROCEDIMIENTO] en el Tribunal de Instancia de [SEDE], plaza n.º [Nº]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

AL TRIBUNAL DE INSTANCIA [ELEGIR: SECCIÓN CIVIL / SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD] DE [LOCALIDAD]

D./Dña. [NOMBRE Y APELLIDOS], Procurador de los Tribunales, que actúa en nombre y representación de D. [NOMBRE Y APELLIDOS], provisto de D.N.I. n.º [NÚMERO], con domicilio en [LOCALIDAD], calle [CALLE], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], bajo dirección del/la Letrado/a D./Dña. [NOMBRE Y APELLIDOS], colegiada n.º [NÚMERO] del Iltre. Colegio de Abogados de [COLEGIO], cuyo despacho se abre en [DIRECCIÓN], calle [CALLE], ante el Tribunal comparezco y como mejor en Derecho proceda, DIGO:

Que por medio del presente escrito, siguiendo la instrucción de mi mandante, vengo a formular demanda de DIVORCIO frente a su esposa Dña. [NOMBRE Y APELLIDOS], con domicilio actual en [DOMICILIO], ejercitando la acción de divorcio prevista en el art. 86 CCiv, y con base a los siguientes datos y argumentos:

HECHOS

PRIMERO.- Mi mandante contrajo matrimonio canónico con Dña. [NOMBRE Y APELLIDOS], en [LOCALIDAD], el día [FECHA]. Se acompaña la correspondiente certificación de matrimonio expedida por el Registro Civil de [LOCALIDAD] (DOCUMENTO N.º [NÚMERO]).

De dicha unión nacieron dos hijos que son menores de edad, de nombre [NOMBRE DEL HIJO/A] y [NOMBRE DEL HIJO/A], nacidos el [FECHA DE NACIMIENTO], y el [FECHA DE NACIMIENTO] Se adjuntan las correspondientes certificaciones de nacimiento que ha emitido el Registro Civil de [LOCALIDAD] (DOCUMENTOS NÚMEROS [Nº] y [Nº]).

SEGUNDO.- Con fecha [FECHA] se interpuso demanda de separación que se siguió con el n.º [Nº] de autos [TIPO Y Nº DE PROCEDIMIENTO] en el Tribunal de Instancia de [SEDE], plaza n.º [Nº] [DATOS DEL PROCEDIMIENTO ANTERIOR], recayendo con fecha [FECHA] Sentencia firme en la que se declara la separación legal de los cónyuges y las medidas definitivas a adoptar. Se acompaña como DOCUMENTO N.º [NÚMERO] testimonio literal de la citada resolución.

TERCERO.- Al margen del cese de la convivencia entre los cónyuges, y de que se ha reanudado en algún momento, es voluntad de mi representado, por razones que ha sopesado debidamente, que se extinga su matrimonio por divorcio.

CUARTO.- Previamente a la presentación de la presente demanda, se han llevado a cabo negociaciones con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad, y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria; incluyéndose entre las acciones realizadas el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución.

Finalmente, mi representado envió un requerimiento fehaciente al demandado con fecha [FECHA], fijando un plazo de 30 días naturales para llegar a un acuerdo amistoso, a través del abogado que firma este escrito, el cual fue contestado por el demandado por el mismo medio, rechazando el acuerdo/ habiendo sido solo posible un acuerdo parcial, viéndonos en la necesidad de acudir a la presente vía judicial, respecto a los extremos de la controversia en los que se mantiene la discrepancia.

Acompaño como documento nº [Nº DE DOCUMENTO], el requerimiento efectuado y como documento nº [Nº DE DOCUMENTO], la contestación del demandado.

A los anteriores hechos sirven de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

I.- Es competente el Tribunal de Instancia del lugar del domicilio del demandado, que es el criterio alternativo, a elección del demandante, conforme al art. 769.1 LEC, párrafo 1.º LEC.

II.- El procedimiento adecuado es el del art. 770 LEC para conocer de las demandas de divorcio contenciosas.

III.- Tienen legitimación ordinaria por hallarse en la situación jurídica de relación matrimonial ambos cónyuges (arts. 86 y 10.1 LEC), siendo el objeto de la pretensión la disolución vincular por divorcio.

IV.- Se fija la cuantía de la demanda, en lo que tiene de estimable, por razón de la pretensión de medidas que incluye reclamaciones de pensiones periódicas, acumulada a la disolución vincular, en [IMPORTE] euros, en armonía con la regla 7.ª del art. 251 LEC.

V.- La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 en relación con el art. 437.1 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

VI.- El fondo de la pretensión consiste en la declaración de divorcio, con la disolución del matrimonio, a instancia de uno de los cónyuges, por su sola voluntad, con arreglo al régimen para la separación matrimonial del art. 81.2.º CCiv, una vez transcurridos los tres primeros meses desde la celebración del enlace, que se transfiere, no ya para el cese de la vida en común, sino para la extinción vincular, desde el art. 86 CCiv.

VII.- Son de aplicación los artículos 91, 97 CC y concordantes del Código Civil

VIII.- No hay ninguna razón para excluir la aplicación del principio del vencimiento en punto a las costas procesales (art. 394 LEC), debiéndose condenar al demandado que se oponga, dado que el obtener la razón precisando de un proceso no ha de suponer una merma patrimonial del que tiene razón.

En virtud de lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito con los documentos que se acompañan y sus copias, se digne admitirlos, tenerme por comparecida y parte en la representación que ostento, entendiéndose conmigo las sucesivas diligencias y por formulada demanda de disolución del matrimonio por divorcio, de modo que seguido que sea el pertinente procedimiento, con intervención del Ministerio Fiscal, se dicte en su día sentencia por la que se declare el divorcio de los esposos D. y Dña. [NOMBRE Y APELLIDOS], con expresa condena en costas a la demandada, oficiándose al Registro Civil de [LOCALIDAD] para la anotación de su parte dispositiva en la inscripción del matrimonio, acordando la adopción como definitivas de las medidas adoptadas en la sentencia de separación, con las modificaciones que con carácter provisional se solicitan en el presente escrito, respecto de las pensiones alimenticias y compensatorias.

Es Justicia de hacerse en [LUGAR], a [FECHA].

OTROSÍ DIGO: Que al amparo de lo dispuesto en el artículo 775.3 LEC, se solicita la MODIFICACIÓN PROVISIONAL DE LAS MEDIDAS DEFINITIVAS adoptadas en su día en la Sentencia de separación, en virtud de los siguientes

HECHOS

ÚNICO.-

Que como consecuencia de la crisis sufrida por el sector de la industria cárnica D. fue despedido en fecha [FECHA] encontrándose actualmente en situación de desempleo.

Desde el [FECHA] hasta el del mismo año, el demandante pasa a percibir una cantidad de [IMPORTE] euros, en concepto de subsidio de desempleo, y desde el [FECHA] hasta el [FECHA] la cantidad subsidiada se reduce a [IMPORTE] euros, como acredita la cartilla de desempleo que se aporta como DOCUMENTO N.º [NÚMERO].

Las circunstancias económicas del esposo, desde la sentencia de separación, en que se tuvo en cuenta el trabajo de ambos cónyuges, han sufrido una modificación peyorativa, y de un sueldo superior a [IMPORTE] euros mensuales ha pasado a ganar [IMPORTE] euros, reducción que debe considerarse sustancial.

FUNDAMENTOS DE DERECHO

I.- Los arts 91 y 100 CCiv en cuanto a la alteración sustancial de las circunstancias fácticas sobre las que se proyectó la fijación de las concretas medidas acordadas anteriormente con motivo de la separación

II.- El art. 773 en cuanto al procedimiento para su modificación, por remisión del art. 775.3, ambos de la LEC.

Por lo expuesto,

SUPLICO AL TRIBUNAL

que tenga por promovido este incidente de modificación provisional de medidas definitivas, y previa la comparecencia de las partes, y tras los demás trámites que sean pertinentes, se dicte Auto en el que se adopten, con carácter provisional y en tanto no recaiga Sentencia definitiva, las siguientes medidas relativas a la pensión alimenticia y compensatoria, manteniendo las restantes:

1.- La fijación en [IMPORTE] € mensuales de la cantidad que en concepto de contribución a las cargas familiares debe abonar el otro cónyuge.
2.- La fijación en [IMPORTE] € mensuales de la cantidad en concepto de pensión compensatoria a cargo del demandante.

Reitero Justicia en lugar y fecha "ut supra ".

Firma del Abogado/a	Firma del Procurador/a

========================================================================
