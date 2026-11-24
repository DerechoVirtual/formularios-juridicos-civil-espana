---
name: demanda-divorcio-contencioso-entre-conyuge-espanol-civ-0042
description: "Demanda de divorcio contencioso entre cónyuge español en España y cónyuge extracomunitario fuera. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de divorcio contencioso entre cónyuge español en España y cónyuge extracomunitario fuera

> Formulario **CIV-0042** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Demanda de divorcio contencioso entre cónyuge español residente en España y cónyuge extranjero de país no miembro de la UE residente en el extranjero; con hijos menores, petición de medidas definitivas sobre guarda, custodia y visitas, sin solicitud de medidas provisionales.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de divorcio contencioso entre cónyuge español en España y cónyuge extracomunitario fuera» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de divorcio contencioso entre cónyuge español en España y cónyuge extracomunitario fuera” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-divorcio-contencioso-entre-conyuge-espanol-civ-0042`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (14 veces)
- [ ] LOCALIDAD (9 veces)
- [ ] Nº DE DOCUMENTO (5 veces)
- [ ] FECHA (3 veces)
- [ ] CALLE (2 veces)
- [ ] COLEGIO
- [ ] CÓDIGO DEL REGISTRO CIVIL
- [ ] DATOS DE LA ESCRITURA
- [ ] LUGAR
- [ ] NACIONALIDAD
- [ ] NOMBRE DEL MENOR
- [ ] Nº
- [ ] NÚMERO
- [ ] PAÍS
- [ ] PROVINCIA
- [ ] RÉGIMEN ECONÓMICO
- [ ] SEDE

## Normas que cita el formulario

- art. 36.1 LEC
- art. 9.2 LOPJ
- art. 45 LEC
- art. 85.1 LOPJ
- art. 86 LOPJ
- art. 769.1 LEC
- art. 23.1 LEC
- art. 31.1 LEC
- art. 749.2 LEC
- art. 770 LEC
- art. 399.3 LEC
- art. 5 Ley Orgánica 1/2025
- art. 9.2 CC
- art. 9.2 Código Civil
- art. 1435 Código Civil
- art. 9.4 CC
- art. 81.2.º CC
- art. 86 CC
- art. 91 CC
- art. 394 LEC

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

- Junto a «…: SECCIÓN CIVIL / SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD] DE [SEDE] Q.P.T.R.C.»: Denominación legal: Sección de Familia, Infancia y Capacidad. Si no existe en el partido, conoce la Sección Civil o la Única (art. 86.3-4 LOPJ). Fuente: LOPJ arts. 84.2.a) y 86 (redacc. LO 1/2025, BOE-A-2025-76).

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

AL TRIBUNAL DE INSTANCIA [ELEGIR: SECCIÓN CIVIL / SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD] DE [SEDE] Q.P.T.R.C.

D./Dña. [NOMBRE Y APELLIDOS], Procurador de los Tribunales, que actúa en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS], de nacionalidad española, vecino de [LOCALIDAD], con domicilio en [LOCALIDAD], como acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], bajo dirección del Letrado D./Dña. [NOMBRE Y APELLIDOS], colegiada n.º [NÚMERO] del Iltre. Colegio de Abogados de [COLEGIO], cuyo despacho se abre en [LOCALIDAD], calle [CALLE], ante el Tribunal comparezco y como mejor en Derecho proceda, DIGO:

Que por medio del presente escrito interpongo DEMANDA CONTENCIOSA DE DIVORCIO contra Doña [NOMBRE Y APELLIDOS], de nacionalidad [NACIONALIDAD], residente en dicho país, con domicilio en [LOCALIDAD], en base a los siguientes:

HECHOS

PRIMERO.- Mi representado y Doña [NOMBRE Y APELLIDOS], contrajeron matrimonio civil en la República de [PAÍS], Provincia de [PROVINCIA], Municipio de [LOCALIDAD], inscrito en el Registro Civil de dicha localidad, con código [CÓDIGO DEL REGISTRO CIVIL], según se acredita mediante la certificación de dicho Registro Civil que se aporta como documento número [Nº DE DOCUMENTO] de la presente demanda.

SEGUNDO.- De dicha unión nació una hija que es menor de edad, de nombre [NOMBRE Y APELLIDOS], nacida el [FECHA], así pues, de [Nº] años de edad.

Se adjunta la correspondiente certificación de nacimiento que ha emitido el Registro Civil de [LOCALIDAD] como documento número [Nº DE DOCUMENTO]

TERCERO.- Celebrado el matrimonio, poco después el matrimonio se trasladó a vivir a España, fijando el domicilio conyugal en la calle [CALLE] de [LOCALIDAD], donde continua residiendo el demandante junto con su hija menor, conforme acredito con certificados de empadronamiento expedidos por el Ayuntamiento de [LOCALIDAD] que se acompañan como documentos números

CUARTO.- El pasado día [FECHA] Doña [NOMBRE Y APELLIDOS] se marchó del domicilio familiar y volvió a su país de origen, sin que haya existido ulterior reanudación de la convivencia conyugal, fijando su residencia en la localidad de [LOCALIDAD], donde también residen sus padres.

Desde entonces, el ejercicio efectivo de la guarda y custodia de la menor ha correspondido en la práctica exclusivamente a mi mandante, así como todos los gastos de manutención, dado que la demandada no ha colaborado en la misma desde su marcha, reduciéndose todo contacto con su hija a algunas llamadas esporádicas.

QUINTO.- Al margen del cese de la convivencia entre los cónyuges, es voluntad de mi representado, por razones que ha sopesado debidamente, que se extinga su matrimonio por divorcio.

Asimismo se solicita la adopción de medidas reguladoras de las relaciones paterno filiales, en concreto, sobre guarda, custodia y régimen de visitas respecto a la hija menor que los litigantes tienen en común.

SEXTO.- Adjuntamos como documento nº [Nº DE DOCUMENTO] declaración responsable de esta parte, de la imposibilidad de llevar a cabo la actividad negociadora previa a la vía judicial por no disponerse de un número de teléfono, correo electrónico u otro medio de comunicación que permita establecer contacto directo con la parte demandada para entablar la negociación exigida antes de la interposición de la demanda.

A los anteriores hechos son de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN Y COMPETENCIA

Competencia internacional

La resolución de la pretensión de divorcio pertenece a la jurisdicción, y a tenor del art. 36.1 LEC, la extensión y límites de la jurisdicción de los tribunales civiles españoles se determinará por lo dispuesto en la Ley Orgánica del Poder Judicial y en los tratados y convenios internacionales en los que España sea parte.

Dicha normativa viene constituida por el Reglamento (UE) 2019/1111 del Consejo, de 25 de junio de 2019, relativo a la competencia, el reconocimiento y la ejecución de resoluciones en materia matrimonial y de responsabilidad parental, y sobre la sustracción internacional de menores, relativo a la competencia, el reconocimiento y la ejecución de resoluciones judiciales en materia matrimonial y de responsabilidad parental.

En lo que respecta a la petición de divorcio, el art. 3.1.a) circunstancia 6.ª del Reglamento atribuye competencia a los tribunales españoles, al ser los órganos jurisdiccionales del Estado miembro en cuyo territorio tiene su residencia habitual el demandante desde hace más de seis meses, siendo de nacionalidad española.

Por su parte, el art. 7.1 del Reglamento, específicamente referido a la responsabilidad parental, establece como fuero de competencia general el Estado miembro el de residencia habitual del menor en el momento en que se presenta el asunto ante el órgano jurisdiccional.

Competencia genérica

Está atribuida al orden civil de jurisdicción, conforme al art. 9.2 LOPJ.

Competencia objetiva

Por lo tocante a la competencia objetiva corresponde a los Tribunales de Instancia -art. 45 LEC en relación con el art. 85.1º LOPJ-, y con arreglo a la especialización ex art. 86 LOPJ, a las Secciones de Familia, Infancia y Capacidad que hay en esta ciudad.

Competencia territorial interna

Se asigna desde el art. 769.1 in fine LEC, a los Tribunales del domicilio actual de la parte actora.

II.- PARTES

Capacidad

Las partes poseen capacidad para ser parte y procesal, en cuanto que personas físicas mayores de edad en pleno ejercicio de sus derechos civiles (arts. 6.1.1.º y 7.1 LEC).

Legitimación

Ostentan las partes legitimación ordinaria por ocupar la posición de cónyuges en la situación jurídica de relación matrimonial (art. 10 párrafo 1.º LEC), siendo el objeto del proceso principal la pretensión de disolución vincular por divorcio y la adopción de medidas definitivas derivadas de la misma.

Postulación

Esta parte, como será debido para la personación que convenga a la contraria, comparece por medio de Procurador de los Tribunales habilitado ante el tribunal (art. 23.1 LEC), y bajo la dirección del Letrado en ejercicio (art. 31.1 LEC).

Intervención del Ministerio Fiscal

Es preceptiva la intervención del Ministerio Fiscal en este proceso dada la existencia de una menor, conforme a lo establecido por el art. 749.2 LEC.

Emplazamiento de la parte demandada

Teniendo la demandada su residencia en el extranjero es necesario su emplazamiento a través de la correspondiente Comisión Rogatoria cursada por el Tribunal.

III.- PROCEDIMIENTO

El procedimiento a través del que ha de sustanciarse la pretensión es el recogido en el art. 770 LEC.

IV.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD

La presente demanda cumple con los requisitos de procedibilidad exigidos por el art. 264.4º y art. 399.3 de la LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

V.- FONDO DEL ASUNTO

1) Derecho aplicable

AL DIVORCIO

En virtud de lo dispuesto en el art. 8.d) del Reglamento (UE) 1259/2010 del Consejo, de 20 de diciembre de 2010, por el que se establece una cooperación reforzada en el ámbito de la ley aplicable al divorcio y a la separación judicial, resulta de aplicación la ley española, dado que ha transcurrido más de un año desde la ruptura convivencial y es España el lugar ante cuyos órganos jurisdiccionales se interpone la presente demanda.

AL RÉGIMEN ECONÓMICO MATRIMONIAL

El art. 9.2 CCiv establece que los efectos del matrimonio se regirán por la ley personal común de los cónyuges al tiempo de contraerlo, en defecto de esta ley, por la ley personal o de la residencia habitual de cualquiera de ellos, elegida por ambos en documento auténtico otorgado antes de la celebración del matrimonio; a falta de esta elección, por la ley de la residencia habitual común inmediatamente posterior a la celebración, y, a falta de dicha residencia, por el lugar de la celebración del matrimonio.

No teniendo los cónyuges en este caso una ley personal común al momento de celebrarlo, los efectos se regirán por la ley española al haber sido elegida ésta por los cónyuges al otorgar capitulaciones matrimoniales en escritura pública [DATOS DE LA ESCRITURA] (documento número [Nº DE DOCUMENTO]), en la que de forma expresa se estableció que los comparecientes hacían constar que su residencia habitual común inmediatamente posterior al matrimonio sería [RÉGIMEN ECONÓMICO] y, "de acuerdo con el artículo 9.2 del Código Civil, la ley que rija según los efectos del matrimonio sea la de derecho común, aplicando el régimen de separación de bienes regulado en los artículos 1435 a 1444 del Código Civil".

A LAS RELACIONES PATERNO-FILIALES

Deberá aplicarse el derecho del foro según el art. 15 del Convenio de La Haya de 19 de octubre de 1996 relativo a la competencia, la ley aplicable, el reconocimiento, la ejecución y la cooperación en materia de responsabilidad parental y de medidas de protección de los niños.

El citado precepto incorpora la máxima lex fori in foro propio, estableciendo que las autoridades de los Estados contratantes aplicarán su propia ley cuando resulten internacionalmente competentes de conformidad con las disposiciones del Capítulo II del Convenio.

Ahora bien, dado que la menor respecto de la cual se interesan las medidas de protección reside habitualmente en España, la competencia judicial internacional viene determinada, no por los foros de competencia judicial internacional del dicho Capítulo II del Convenio de la Haya de 1996, sino por las disposiciones del Reglamento (UE) 2019/1111 del Consejo, de 25 de junio de 2019, relativo a la competencia, el reconocimiento y la ejecución de resoluciones en materia matrimonial y de responsabilidad parental, y sobre la sustracción internacional de menores, de conformidad con lo previsto en el art. 97.1.a) del propio Reglamento, que en materia de responsabilidad parental (cfr.: art. 7), otorga competencia a los órganos jurisdiccionales del Estado miembro de la residencia habitual del menor en el momento en el que se presenta el asunto ante dicho órgano jurisdiccional.

De este modo, una interpretación estricta del art. 15.1 del Convenio de La Haya de 1996 podría inducir a pensar que en supuestos como el que nos ocupa no resultaría de aplicación la norma de conflicto convencional, debiendo, entonces, tener que acudir a la norma de conflicto de producción interna, es decir, al art. 9.4 CCiv. No obstante lo dicho, de conformidad con acreditada doctrina científica (CALVO, CARRASCOSA), debe entenderse que si, como es el caso, el foro del Reglamento 2201/2003 en el cual el órgano jurisdiccional fundamenta su competencia judicial internacional, en tanto que incorpora idéntico criterio de atribución de competencia, es equivalente a uno de los que contempla el Convenio de la Haya de 1996, nada impide al Tribunal aplicar las normas de conflicto previstas en el citado Convenio. Dicha solución resulta conforme con el "espíritu conflictual" del Convenio, puesto que lleva a aplicar el Derecho material del Estado contratante cuyas autoridades resultan competentes en virtud de uno de los foros previstos en la propia norma convencional, cual es el de la residencia habitual del menor, incorporado en el art. 5.1 del Convenio de La Haya de 1996 (en este sentido, SAP Zaragoza de 20 de abril de 2012, rec. 146/2012).

2) Petición de divorcio

El fondo de la pretensión consiste en la declaración de divorcio, a fin de la disolución del matrimonio, a instancia de uno de los cónyuges, de conformidad con el art. 81.2.º CCiv, por remisión del art. 86 CCiv, después de transcurridos tres meses desde la celebración del matrimonio sin que puedan oponerse por el otro cónyuge, no expresamente conforme ninguna causa de oposición material, al fundarse en la voluntad de no permanecer casado, como corolario legal del derecho del art. 32 CE a contraer matrimonio.

3) Medidas

En relación a las medidas a adoptar deberán aplicarse los arts. 91 a 96 CC y concordantes del Código Civil.

3.1) GUARDA Y CUSTODIA DE LOS HIJOS. Habida cuenta la edad de la hija menor, y considerando su interés como el criterio rector de cualquier medida en relación con la misma, carece de sentido que se posibilite la vivencia con la madre demandada, sin que haya ámbito por el momento a respetar inviables decisiones personales de la menor.

Es lo oportuno, por naturaleza, que el padre actor, hasta el momento quien ha vivido con la hija común, desde el abandono de Doña [NOMBRE Y APELLIDOS], retenga la guarda y custodia de ésta, sin perjuicio de que la patria potestad siga compartida por ambos progenitores.

3.2) DERECHO DE VISITA. Se postula a favor de Doña [NOMBRE Y APELLIDOS] un derecho de visitas a su hija [NOMBRE Y APELLIDOS], que en todo caso deberá llevarse a cabo en España, con la simple comunicación a mi mandante con razonable antelación, sin posibilidad de trasladar a la menor fuera de España sin el consentimiento expreso de mi representado.

3.3) RÉGIMEN ECONÓMICO MATRIMONIAL. El régimen económico que rige los aspectos económicos del matrimonio desde su comienzo es de plena separación de bienes, por lo que no es menester medida alguna en lo que se refiere al régimen.

VI.- COSTAS

Deberá ser impuesto a la contraparte el reembolso de las costas del proceso, en virtud de lo establecido en el art. 394 LEC.

En su virtud,

SUPLICO AL TRIBUNAL:

Que, teniendo por presentado este escrito de demanda junto con los documentos que se acompañan y sus copias, por el Letrado de la Administración de Justicia se sirva admitirlo, tenerme por comparecido y parte en la representación que ostento de Don [NOMBRE Y APELLIDOS], y por interpuesta DEMANDA CONTENCIOSA DE DIVORCIO contra Doña [NOMBRE Y APELLIDOS], y, previa la tramitación legal de rigor, con traslado al Ministerio Fiscal, y el emplazamiento de la demandada a través de la correspondiente Comisión Rogatoria por el Tribunal, en atención a su lugar de residencia, por el tribunal se dicte en su día Sentencia por la que estimando la presente demanda:

a) SE DECLARE EL DIVORCIO de los esposos Don [NOMBRE Y APELLIDOS] y Doña [NOMBRE Y APELLIDOS]
b) SE ACUERDEN LAS SIGUIENTES MEDIDAS DEFINITIVAS, que se podrán modificar si se alteraren sustancialmente las circunstancias:
1.- Atribución de la guarda y custodia de la hija menor [NOMBRE DEL MENOR] al demandante, en cuya compañía convive, conservándose la patria potestad compartida por ambos progenitores.
2.- Derecho de comunicación y visita con dicha hija menor de su madre conforme a lo expuesto en el fundamento de derecho IV.3.2.

En todo caso, se pronuncie el reintegro de las costas con cargo al demandado opuesto.

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a

========================================================================
