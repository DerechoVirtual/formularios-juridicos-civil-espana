---
name: demanda-divorcio-contencioso-sin-separacion-previa-civ-0344
description: "Demanda de divorcio contencioso sin separación previa, con solicitud de medidas provisionales. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de divorcio contencioso sin separación previa, con solicitud de medidas provisionales

> Formulario **CIV-0344** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Demanda de divorcio contencioso, sin separación judicial previa, y solicitando medidas provisionales.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de divorcio contencioso sin separación previa, con solicitud de medidas provisionales» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de divorcio contencioso sin separación previa, con solicitud de medidas provisionales” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-divorcio-contencioso-sin-separacion-previa-civ-0344`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (7 veces)
- [ ] NOMBRE DEL HIJO/A (7 veces)
- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] Nº (7 veces)
- [ ] IMPORTE (6 veces)
- [ ] CALLE (3 veces)
- [ ] FECHA (3 veces)
- [ ] Nº DE CUENTA (IBAN) (3 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] FECHA DE NACIMIENTO (2 veces)
- [ ] BENEFICIARIO
- [ ] COLEGIO
- [ ] DENOMINACIÓN SOCIAL
- [ ] DIRECCIÓN
- [ ] DNI/NIE
- [ ] DOMICILIO
- [ ] FECHAS
- [ ] LUGAR
- [ ] NÚMERO
- [ ] PORCENTAJE

## Normas que cita el formulario

- art. 86 CC
- art. 770 LEC
- art. 251 LEC
- art. 437.1 LEC
- art. 5 Ley Orgánica 1/2025
- art. 81.2.º CC
- art. 91 CC
- art. 97 CC
- art. 97.4 CC
- art. 97.6 CC
- art. 97.8 CC
- art. 394 LEC
- art. 773.1 LEC
- art. 103 CC
- art. 771 LEC
- art. 773.3 LEC
- art. 102 CC
- art. 809 LEC

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

- Junto a «…ELEGIR: SECCIÓN CIVIL / SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD] DE [LOCALIDAD]»: Denominación legal: Sección de Familia, Infancia y Capacidad. Si no existe en el partido, conoce la Sección Civil o la Única (art. 86.3-4 LOPJ). Fuente: LOPJ arts. 84.2.a) y 86 (redacc. LO 1/2025, BOE-A-2025-76).

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

AL TRIBUNAL DE INSTANCIA, [ELEGIR: SECCIÓN CIVIL / SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD] DE [LOCALIDAD]

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, que actúa en nombre y representación de Dña. [NOMBRE Y APELLIDOS], provista de DNI n.º [DNI/NIE], con domicilio en [LOCALIDAD], calle [CALLE], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], bajo dirección del Letrado D./Dña. [NOMBRE Y APELLIDOS], ejerciente en el Iltre. Colegio de Abogados de [COLEGIO], cuyo despacho se abre en [DIRECCIÓN], ante el Tribunal comparezco y como mejor en Derecho proceda, DIGO:

Que por medio del presente escrito, siguiendo la instrucción de mi mandante, vengo a formular demanda de DIVORCIO frente a su esposo D. [NOMBRE Y APELLIDOS], con domicilio actual en [DOMICILIO], ejercitando la acción prevista en el art. 86 CC y con base a los siguientes datos y argumentos:

HECHOS

PRIMERO.- Mi mandante contrajo matrimonio canónico con D. [NOMBRE Y APELLIDOS], en [LOCALIDAD], el día [FECHA]. Se acompaña la correspondiente certificación de matrimonio expedida por el Registro Civil de [LOCALIDAD] (DOCUMENTO N.º [NÚMERO]).

De dicha unión nacieron dos hijos que son menores de edad, de nombre [NOMBRE DEL HIJO/A] y [NOMBRE DEL HIJO/A], nacidos el [FECHA DE NACIMIENTO], y el [FECHA DE NACIMIENTO]. Se adjuntan las correspondientes certificaciones de nacimiento que ha emitido el Registro Civil de [LOCALIDAD] (DOCUMENTOS NÚMEROS [Nº] y [Nº]).

SEGUNDO.- El régimen conyugal de bienes es el de sociedad de gananciales, por la vecindad de los consortes y no haberse otorgado nunca capitulaciones matrimoniales.

TERCERO.- En la actualidad, mi mandante ocupa el domicilio conyugal junto a los dos hijos habidos del matrimonio, adquirido para la sociedad de gananciales por ambos cónyuges mediante documento público (inscripción registral y certificado de empadronamiento, DOCUMENTOS NÚMEROS [Nº] y [Nº]).

CUARTO.- El demandado percibe unos ingresos de [IMPORTE] euros mensuales como trabajador de la empresa [DENOMINACIÓN SOCIAL], mientras que mi representada carece de ingresos propios, y aún de cualificación profesional de cualquier tipo, por haber dedicado su vida, desde su matrimonio, al cuidado de la casa y de la familia, habiendo tenido que recurrir, desde que el marido se prodigaba en el bingo, a sus propios padres para subvenir a los gastos de la casa y la formación de los hijos. Se adjunta, al objeto de demostrar las rentas de la unidad familiar, copias de la declaración -conjunta- del I.R.P.F. del año pasado y el anterior, como DOCUMENTOS NÚMEROS [Nº] y [Nº].

QUINTO.- Por consecuencia de las desavenencias entre los cónyuges, mi representada está persuadida de lo adecuado de su decisión de disolver el vínculo matrimonial mediante divorcio, sin que haya sido posible tramitarlo de mutuo acuerdo, por lo que se interpone la presente demanda contenciosa.

SEXTO.- A tal fin, previamente a la presentación de la presente demanda, se han llevado a cabo negociaciones con la parte demandada, con el objetivo de cumplir el requisito de procedibilidad, y resolver la controversia de manera amistosa y extrajudicial. Dichas negociaciones se desarrollaron en cumplimiento de los principios de buena fe, con la intención de alcanzar una solución satisfactoria; incluyéndose entre las acciones realizadas el intercambio de comunicaciones formales mediante correspondencia escrita, en fechas [FECHAS], en las cuales esta parte expresó su disposición para dialogar y propuso alternativas de solución.

Finalmente, mi representado envió un requerimiento fehaciente al demandado con fecha [FECHA], fijando un plazo de 30 días naturales para llegar a un acuerdo amistoso, a través del abogado que firma este escrito, el cual fue contestado por el demandado por el mismo medio, rechazando el acuerdo/ habiendo sido solo posible un acuerdo parcial, viéndonos en la necesidad de acudir a la presente vía judicial, respecto a los extremos de la controversia en los que se mantiene la discrepancia.

Acompaño como documento nº [Nº DE DOCUMENTO], el requerimiento efectuado y como documento nº [Nº DE DOCUMENTO], la contestación del demandado.

FUNDAMENTOS DE DERECHO

I.- Es competente el Tribunal de Instancia del lugar del domicilio del demandado, que es el criterio alternativo, a elección del demandante, conforme al art. 769.1, párrafo 1.º LEC.

II.- El procedimiento adecuado es el del art. 770 LEC para conocer de las demandas de divorcio contenciosas.

III.- Tienen legitimación ordinaria por hallarse en la situación jurídica de relación matrimonial ambos cónyuges (arts. 86 CC y 10.1 LEC), siendo el objeto del proceso principal la pretensión de disolución vincular por divorcio y la adopción de medidas definitivas derivadas de la misma.

IV.- Se fija la cuantía de la demanda, en lo que tiene de estimable, por razón de la pretensión de medidas que incluye reclamaciones de pensiones periódicas, acumulada a la disolución vincular, en [IMPORTE] euros, en armonía con la regla 7.ª del art. 251 LEC.

V.- La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 en relación con el art. 437.1 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

VI.- El fondo de la pretensión consiste en la declaración de divorcio, a fin de la disolución del matrimonio, a instancia de uno de los cónyuges, de conformidad con el art. 81.2.º CC, por remisión del art. 86 CC, sin que puedan oponerse por el otro cónyuge, no expresamente conforme ninguna causa de oposición material, al fundarse en la voluntad de no permanecer casado, como corolario legal del derecho del art. 32 CE a contraer matrimonio.

VII.- Conforme a los arts. 91 CC y 774 LEC, el Tribunal deberá pronunciarse en definitiva sobre las medidas que se solicitarán que se adopten con carácter de provisionales, acerca de los hijos, vivienda y cargas familiares, y régimen matrimonial de bienes, las cuales se pretenden igualmente como definitivas, debiéndose particularizar el establecimiento de la pensión compensatoria en aplicación del art. 97 CC, que se solicita por tiempo indefinido.

De los nueve ordinales de criterios legales del precitado precepto para fijarla, sin acuerdo entre los cónyuges, en tanto que no existen especiales circunstancias sobre el estado de salud, ni se pierde un derecho de pensión, ni tampoco ha existido negocio del esposo demandado en que se colaborara, resulta esencial la edad, y la duración del matrimonio y de la convivencia conyugal, por una regla equitativa práctica, pues resulta manifiesto que las posibilidades de reconstrucción de una convivencia con un tercero son más difíciles cuanto mayor sea la edad, y mayor haya sido la adaptación interconyugal. Por otro lado, el caudal y medios económicos y las necesidades de uno y otro cónyuge, siempre teniendo en cuenta, como cánones hermenéuticos, la realidad social del tiempo en que adopte la decisión y el espíritu y finalidad de la norma, que en este caso es el mantenimiento del nivel patrimonial desequilibrado por la disolución del matrimonio.

En el caso presente, la cónyuge demandante sufre a causa de la disolución un desequilibrio económico, tomando como punto de referencia la posición del otro cónyuge, en la faceta económica con evidencia, ya que la esposa carece de ingresos, y las rentas familiares íntegras proceden del esposo, pero también desde el punto de vista de los beneficios, influencias, amistades y otras circunstancias peyorativas socio-económico-culturales.

El desequilibrio económico debe referirse al último período de la convivencia conyugal, sin que exista aquí comparación posible entre cónyuges de sus ingresos respectivos, dado que sólo los tiene el demandado.

Con los datos acreditados, la dedicación pasada a la familia (art. 97.4 CC), puesto que la actora se ha dedicado a ser ama de casa, los [Nº] años de duración del matrimonio y de la convivencia conyugal (art. 97.6 CC), pero esencialmente los medios económicos y las necesidades de uno y otro cónyuge (art. 97.8 CC), es clara la necesidad de establecimiento de la pensión compensatoria, y en lo relativo a la cuantía, la mejor doctrina indica la conveniencia de tomar en cuenta otros criterios como la culpabilidad, por el daño moral causado al cónyuge que queda en debilidad social y económica.

Por ello se valora la cuota mensual de la pensión compensatoria en [IMPORTE] euros ( €), además de la pensión alimenticia para los hijos comunes.

VIII.- No hay ninguna razón para excluir la aplicación del principio del vencimiento en punto a la costas procesales (art. 394 LEC), debiéndose condenar al demandado que se oponga, dado que el obtener la razón precisando de un proceso no ha de suponer una merma patrimonial del que tiene razón.

En virtud de lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito con los documentos que se acompañan y sus copias, se digne admitirlos, tenerme por comparecida y parte en la representación que ostento, entendiéndose conmigo las sucesivas diligencias y por formulada demanda de disolución del matrimonio por divorcio, de modo que seguido que sea el pertinente procedimiento, con citación del Ministerio Fiscal, se dicte en su día sentencia por la que se declare el divorcio de los esposos D. y Dña. [NOMBRE Y APELLIDOS], con expresa condena en costas al demandado, oficiándose al Registro Civil de [LOCALIDAD] para la anotación de su parte dispositiva en la inscripción del matrimonio, y se acuerden las siguientes medidas definitivas, que se podrán modificar si se alteraren sustancialmente las circunstancias:

1.- Atribución de la guarda y custodia de los hijos menores [NOMBRE DEL HIJO/A] y [NOMBRE DEL HIJO/A] a la demandante, quedando la patria potestad compartida por ambos progenitores.
2.- Fijación de un derecho de visitas del demandado conforme al que el progenitor demandado podrá tener en su compañía a los hijos menores los fines de semana alternos desde las 12 horas del sábado a las 20 horas del domingo, así como la primera mitad de las vacaciones escolares de Navidad, Semana Santa y Verano los años pares, y la segunda mitad los años impares.
3.- Atribución del uso exclusivo de la vivienda familiar sita en la calle [CALLE], a la demandante y los dos hijos, así como del ajuar doméstico en ella existente.
4.- Establecimiento de una pensión compensatoria a favor de la demandante de [IMPORTE] euros mensuales ( €), y sendas pensiones alimenticias, a favor de [BENEFICIARIO] y de [NOMBRE DEL HIJO/A] de [IMPORTE] euros mensuales ( €), todas ellas a cargo del demandado D. [NOMBRE Y APELLIDOS], pagaderas por meses anticipados, mediante ingreso en la cuenta corriente [Nº DE CUENTA (IBAN)], y actualizables anualmente conforme a las variaciones que experimente el Índice de Precios al Consumo que publique el Instituto Nacional de Estadística, u organismo oficial que lo sustituya.

Es Justicia de hacerse en [LUGAR], a [FECHA].

OTROSÍ DIGO: Que al amparo del art. 773.1 LEC, no habiéndose adoptado con anterioridad, se solicitan mediante el presente escrito MEDIDAS PROVISIONALES coetáneas a la admisión de la demanda, en base a los siguientes:

HECHOS

PRIMERO.- Los dos hijos menores comunes del matrimonio han estado siempre en compañía de la madre, mi mandante, y es lo conveniente que continúen con ella, habida cuenta de la conducta desordenada del padre, absolutamente encajada en la prodigalidad, pareciendo suficiente la comunicación y estancia sin pernocta del padre, en casa de los abuelos donde éste reside, los sábados de todas las semanas, por lo menos hasta la resolución definitiva, o que la prodigalidad y costumbres de D. no se demuestren corregidas.

SEGUNDO.- Puesto que el interés familiar más necesitado de protección es el de los hijos en potestad, tanto ellos como mi representada deben continuar en el uso de la vivienda familiar.

TERCERO.- Como quiera que mi representada carece de ingresos propios o de bienes rentables, constituyendo las fuentes del activo familiar el sueldo como trabajador por cuenta ajena del demandado, es necesaria su aportación con el [PORCENTAJE] % para hacer frente a las cargas familiares, toda vez que el dicho sueldo es al presente perfectamente derrochado, y el demandado vive con sus padres, que gozan de asentada posición.

La dicha cantidad debiera ser directamente ingresada en la cuenta bancaria [Nº DE CUENTA (IBAN)], habida cuenta que todos los datos apuntan que el cumplimiento voluntario no es verosímil que se produzca, y en evitación de dilaciones y diligencias ejecutivas inútiles.

FUNDAMENTOS DE DERECHO

I.- El cónyuge que solicita el divorcio está legitimado para pedir con la demanda medidas provisionales del art. 103 CC (art. 773.1 LEC).

II.- El procedimiento adecuado es el del art. 771 LEC para medidas previas, conforme remisión del art. 773.3 LEC.

III.- Esta pretensión consiste en la adopción de los efectos ope legis del art. 102 CC y medidas del art. 103 CC, de cognición judicial, derivados de la tutela cautelar por la lesión que, de no adoptarse, pueden padecer las partes y los hijos menores, por la duración del proceso.

En su virtud,

SUPLICO AL TRIBUNAL

que, teniendo por causadas las precedentes manifestaciones a los efectos oportunos, y por deducida solicitud de adopción de medidas provisionales, seguido que sea su pertinente trámite, se dicte Auto por el que se aprueben las siguientes:

a) Asignación a la madre actora de la guarda y custodia de los dos hijos menores en potestad [NOMBRE DEL HIJO/A] y [NOMBRE DEL HIJO/A]
b) Fijación de un derecho provisional de comunicación y visita del demandado a sus hijos todos los sábados de cada semana de diez a veinte horas.
c) Atribución del uso exclusivo de la vivienda familiar sita en la calle [CALLE], a la solicitante y los dos hijos, así como del ajuar doméstico en ella existente. Para la constancia de dicho derecho de uso, expedirá mandamiento por duplicado el Tribunal junto con testimonio del Auto que la acuerde, a fin de que el Registro de la Propiedad de [LOCALIDAD] publique la afectación de la finca.
d) Fijación de la cantidad de [IMPORTE] euros mensuales en concepto de contribución al levantamiento de las cargas familiares, que será ingresada, en cumplimiento de oficio del Tribunal, por meses anticipados, dentro de los cinco primeros días de cada mes en la cuenta bancaria [Nº DE CUENTA (IBAN)] Dicha cantidad se actualizará anualmente, con efectos de primero de enero de cada año, en proporción a las variaciones que experimenten los índices de precio al consumo, según el Instituto Nacional de Estadística u organismo que le sustituya.
e) Formación de inventario del patrimonio de la sociedad conyugal de bienes al objeto de cautelar la liquidación de régimen económico del matrimonio conforme al art. 809 LEC.

Reitero Justicia en lugar y fecha "ut supra ".

Firma del Abogado/a	Firma del Procurador/a

========================================================================
