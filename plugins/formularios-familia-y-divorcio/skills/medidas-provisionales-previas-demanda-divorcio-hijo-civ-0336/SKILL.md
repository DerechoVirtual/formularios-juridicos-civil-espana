---
name: medidas-provisionales-previas-demanda-divorcio-hijo-civ-0336
description: "Medidas provisionales previas a la demanda de divorcio con hijo menor y riesgo para el solicitante. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Medidas provisionales previas a la demanda de divorcio con hijo menor y riesgo para el solicitante

> Formulario **CIV-0336** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Escrito formulando solicitud de medidas provisionales previas a la demanda de divorcio del matrimonio, con hijo menor de edad. Escrito inicial con representación de procurador, que solicita medidas de adopción inmediata por riesgo de indemnidad del solicitante. Aunque la cuestión es discutida por la doctrina, el modelo contempla la NO sujeción al previo intento de resolución de controversias en vía no jurisdiccional por tratarse de materias excluidas del requisito de procedibilidad de acuerdo con el art. 4.1 II LO 1/2025, entre las cuales se encuentran los conflictos que afecten a derechos y obligaciones que no estén a disposición de las partes, además de concurrir razones de urgencia.

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Medidas provisionales previas a la demanda de divorcio con hijo menor y riesgo para el solicitante» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Medidas provisionales previas a la demanda de divorcio con hijo menor y riesgo para el solicitante” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:medidas-provisionales-previas-demanda-divorcio-hijo-civ-0336`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (10 veces)
- [ ] LOCALIDAD (8 veces)
- [ ] NÚMERO (8 veces)
- [ ] NOMBRE DEL HIJO/A (5 veces)
- [ ] FECHA (3 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] AÑO (2 veces)
- [ ] CALLE (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] COLEGIO
- [ ] DENOMINACIÓN SOCIAL
- [ ] DÍA
- [ ] ENTIDAD BANCARIA
- [ ] FECHA DE NACIMIENTO
- [ ] LUGAR
- [ ] NOMBRE DEL MENOR
- [ ] Nº DE COLEGIADO/A
- [ ] PISO

## Normas que cita el formulario

- art. 771 LEC
- art. 81 CC
- art. 4.1 LO 1/2025
- art. 102 CC
- art. 103 CC
- art. 81.2.º CC
- art. 104 CC
- art. 92.3 CC
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

- Junto a «…ECCIÓN CIVIL [LOCALIDAD] SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD DE [LOCALIDAD]»: Denominación legal: Sección de Familia, Infancia y Capacidad. Si no existe en el partido, conoce la Sección Civil o la Única (art. 86.3-4 LOPJ). Fuente: LOPJ arts. 84.2.a) y 86 (redacc. LO 1/2025, BOE-A-2025-76).

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

AL TRIBUNAL DE INSTANCIA

SECCIÓN CIVIL [LOCALIDAD]

SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD DE [LOCALIDAD]

D./Dña. [NOMBRE Y APELLIDOS], Procurador de los Tribunales con número de colegiado [Nº DE COLEGIADO/A], en nombre y representación de Doña [NOMBRE Y APELLIDOS], con domicilio en esta ciudad, n.º [NÚMERO], lo que acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], con la asistencia del Letrado suscrito D./Dña. [NOMBRE Y APELLIDOS], colegiado n.º [NÚMERO] del Iltre. Colegio de Abogados de [COLEGIO], con despacho abierto en [LOCALIDAD], calle [CALLE], ante el Tribunal comparezco y como mejor en Derecho proceda, DIGO

Que por medio del presente escrito vengo a formular solicitud de MEDIDAS PROVISIONALES PREVIAS frente a D. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], en base a los siguientes datos y argumentos:

HECHOS

PRIMERO.- De la relación de mi mandante con D. [NOMBRE Y APELLIDOS], nació el [FECHA DE NACIMIENTO] un hijo, de nombre [NOMBRE DEL HIJO/A], conforme se acredita mediante la aportación como Documento n.º [NÚMERO], de la certificación de la inscripción de nacimiento.

SEGUNDO.- Mi mandante ha contraído matrimonio (canónico, civil) con D. [NOMBRE Y APELLIDOS], en [LOCALIDAD], el día [FECHA], a cuya acreditación se acompaña certificación expedida por el Registro Civil de [LOCALIDAD] como Documento n.º [NÚMERO], y por lo tanto, hace nada más que mes y medio.

TERCERO.- Desde el nacimiento del hijo común, en otoño del año pasado, el esposo de mi mandante hizo dejación de sus obligaciones familiares para con la solicitante y aquél, habiendo sido la relación entre los ahora casados tormentosa, resultando que desde prácticamente después de la vuelta del viaje de novios, el [DÍA] del mes pasado, no ha pernoctado el marido en el domicilio conyugal, sin aportar nada de sus ingresos al sostenimiento de la familia, provocando en las ocasiones que ha entrado en dicho domicilio escenas de maltrato psíquico a la demandante, que empezaron por lo irrespetuoso y han acabado con violencia.

Se acompaña informe médico de la Dr./a [NOMBRE Y APELLIDOS], del centro de salud mental de [LOCALIDAD], que atiende desde entonces a mi mandante (Documento n.º [NÚMERO]), y certificado de denuncia por delito de violencia doméstica de fecha [FECHA] ante la Comisaría de Policía de [LOCALIDAD] (Documento n.º [NÚMERO]).

CUARTO.- El régimen económico del matrimonio es el legal supletorio, por no haberse otorgado nunca capitulaciones, siendo que la solicitante tiene empleo como limpiadora para la empresa [DENOMINACIÓN SOCIAL], mientras que el demandado es titular de un negocio de carpintería como trabajador autónomo, denominado Puertas del Barrio, gozando de unos rendimientos con los que es dable mantener el nivel de gastos fijos de la atención de la casa y que genera la manutención y educación de los hijos en común.

Se adjuntan copias de las autoliquidaciones del I.R.P.F. de ejercicios [AÑO] y [AÑO], de la actora y demandado, como Documentos nos. y [Nº DE DOCUMENTO], documento TC1, en que aparecen los asalariados del esposo empresario (Documento n.º [NÚMERO]), así como extractos de movimientos y saldos de cuenta bancaria por la entidad financiera [ENTIDAD BANCARIA], que ha conseguido mi representada, como Documentos nos. y [Nº DE DOCUMENTO]).

QUINTO.- Es intención de mi mandante solicitar el divorcio inmediatamente.

FUNDAMENTOS DE DERECHO

I.- Es competente el Tribunal de Instancia del lugar del domicilio del solicitante, conforme al art. 771.1 párrafo 1.º LEC.

II.- El proceso adecuado es el del art. 771 LEC para conocer de la solicitud de medidas provisionales previas.

III.- Tiene la demandante legitimación activa ordinaria por hallarse en la situación jurídica de relación conyugal, como detenta la pasiva su marido (arts. 81 CCiv y 10 párrafo 1.º LEC), siendo el objeto del proceso la tutela judicial cautelar de la pretensión de disolución vincular por divorcio anunciada.

IV.- La presente demanda no está sujeta al previo intento de resolución de controversias en vía no jurisdiccional por tratarse de materias excluidas del requisito de procedibilidad de acuerdo con el art. 4.1 II LO 1/2025, entre las cuales se encuentran los conflictos que afecten a derechos y obligaciones que no estén a disposición de las partes.

V.- El fondo de la pretensión consiste en la adopción de los efectos del art. 102 CCiv y medidas del art. 103 CCiv, de cognición judicial, derivados de la futura admisión de la demanda de divorcio a su instancia.

La demanda se fundará en la pura petición de esta parte, de conformidad con el art. 86 por relación al art. 81.2.º, ambos del CCiv.

Comoquiera que no han transcurrido aún los tres meses desde la celebración del matrimonio, y ni siquiera lo hará para cuando deba interponerse la anunciada demanda, con arreglo a la previsión del último citado precepto, se alega y acredita la existencia de un riesgo cierto para la libertad e integridad moral, e incluso la integridad física, del cónyuge solicitante.

El art. 104 CCiv presume la urgencia para la tutela sumaria cautelar y el peligro de infructuosidad de no adoptarse los anteriores efectos y medidas.

El hijo menor [NOMBRE DEL MENOR] ha estado siempre en compañía de la madre, mi mandante, desde su nacimiento, y es lo conveniente que continúe con ella, habida cuenta de la conducta desarreglada del padre y su salida del hogar, y puesto que se solicitará con la demanda la privación de la patria potestad del padre conforme al art. 92.3 CCiv, dada la desatención para con el mismo, y siendo un bebé, la violencia ejercida sobre la madre, interesa que no haya comunicación del padre con el hijo, por lo menos hasta la resolución definitiva.

En cuanto a la vivienda familiar, procede que se atribuya a mi mandante su uso, así como la utilización del ajuar familiar, sin perjuicio de los inventarios que se estimen necesarios, toda vez que, por lo expuesto en la demanda, queda claro que resulta ser el interés familiar más necesitado de protección.

Dada la situación económica de D. [NOMBRE Y APELLIDOS] y de mi mandante aquél deberá abonar como contribución a las cargas del matrimonio y alimentos la cantidad de [IMPORTE] euros.

Esta cantidad se justifica por la comparación de rendimientos de marido y mujer, y sobre la base de que la estimación objetiva singular del IRPF para el negocio de carpintería del primero en modo alguno desvela su situación financiera y patrimonial real, mucho más boyante.

VI.- Las costas procesales deben ser impuestas a la parte demandada, por criterio del íntegro vencimiento, en atención al art. 394 LEC.

Y demás normas y jurisprudencia de general y pertinente aplicación.

En virtud de lo expuesto,

SUPLICO AL TRIBUNAL:

que, teniendo por presentado este escrito con sus copias y documentos adjuntados, se digne admitir uno y otros, tener a la firmante por comparecida y parte, entendiéndose conmigo las sucesivas diligencias y por deducida solicitud de adopción de medidas provisionales previas, seguido que sea su pertinente trámite, se dicte Auto por el que se aprueben las siguientes:

a) Separación provisional de los cónyuges, con cese de la presunción de convivencia.
b) Revocación de los consentimientos y poderes que cualquiera de los cónyuges hubiera otorgado a favor del otro, cesando la posibilidad de vincular los bienes privativos del otro cónyuge en el ejercicio de la potestad doméstica.
c) Asignación a la madre actora de la exclusiva guarda y custodia del hijo menor en potestad [NOMBRE DEL HIJO/A], sin fijación de ningún derecho provisional de comunicación y estancia del demandado con su hijo.
d) Atribución del uso exclusivo de la vivienda familiar sita en la calle [CALLE], n.º [NÚMERO], piso [PISO], a la solicitante y su hijo [NOMBRE DEL HIJO/A], así como del ajuar doméstico en ella existente.
e) Fijación de la cantidad de [IMPORTE] euros mensuales en concepto de contribución al levantamiento de las cargas familiares, que será ingresada, en cumplimiento de oficio del Tribunal, por meses anticipados, dentro de los cinco primeros días de cada mes en la cuenta bancaria que la solicitante designe.

Dicha cantidad se actualizará anualmente, con efectos de primero de enero de cada año, en proporción a las variaciones que experimenten los índices de precio al consumo, según el INE u organismo que le sustituya.

Es de Justicia que pido en [LUGAR], a [FECHA].

OTROSÍ DIGO: Que de conformidad con el art. 771.2 párrafo 2.º LEC, mediante auto, y de forma inmediata a la presentación de esta solicitud, pueden acordarse con carácter inmediato los efectos del art. 102 CCiv y las medidas del art. 103 CCiv atenidas a la custodia de los hijos y al uso del domicilio y ajuar familiares, por lo que se considera urgente que, habida cuenta el trato vejatorio y hasta violento de D. [NOMBRE Y APELLIDOS], se decreten los dichos efectos y se mande a éste salir de la convivencia con la solicitante y su hijo [NOMBRE DEL HIJO/A], quedando éste bajo la custodia exclusiva de su madre.

En su virtud,

SUPLICO AL TRIBUNAL que, teniendo por causadas las precedentes manifestaciones a los efectos oportunos, se digne proveer en su consecuencia, acordando de inmediato los efectos del art. 102 CCiv y la salida del hogar familiar de D. [NOMBRE Y APELLIDOS] con el provisional uso exclusivo del mismo y el ajuar doméstico por la solicitante y su hijo [NOMBRE DEL HIJO/A], y quedando éste bajo la exclusiva custodia de su madre.

Reitero Justicia en lugar y fecha "ut supra ".

Firma del Abogado/a	Firma del Procurador/a

========================================================================
