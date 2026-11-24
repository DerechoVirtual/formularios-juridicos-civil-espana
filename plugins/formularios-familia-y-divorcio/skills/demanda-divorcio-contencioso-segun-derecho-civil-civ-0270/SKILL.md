---
name: demanda-divorcio-contencioso-segun-derecho-civil-civ-0270
description: "Demanda de divorcio contencioso según el Derecho civil catalán tras separación judicial previa. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de divorcio contencioso según el Derecho civil catalán tras separación judicial previa

> Formulario **CIV-0270** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Demanda de divorcio contencioso conforme a Derecho civil especial de Cataluña, tras separación judicial previa.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de divorcio contencioso según el Derecho civil catalán tras separación judicial previa» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de divorcio contencioso según el Derecho civil catalán tras separación judicial previa” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-divorcio-contencioso-segun-derecho-civil-civ-0270`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NÚMERO (11 veces)
- [ ] NOMBRE Y APELLIDOS (10 veces)
- [ ] LOCALIDAD (7 veces)
- [ ] FECHA (6 veces)
- [ ] CALLE (4 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] Nº (2 veces)
- [ ] SEDE (2 veces)
- [ ] AÑO
- [ ] COLEGIO
- [ ] DENOMINACIÓN SOCIAL
- [ ] DOMICILIO
- [ ] IMPORTE
- [ ] LUGAR
- [ ] MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] NOMBRE DEL HIJO/A 1
- [ ] NOMBRE DEL HIJO/A 2
- [ ] TIPO Y Nº DE PROCEDIMIENTO

## Normas que cita el formulario

- art. 231 Código Civil
- art. 770 LEC
- art. 232 CC
- art. 6.1.1.º LEC
- art. 750.1 LEC
- art. 86 CC
- art. 437.1 LEC
- art. 5 Ley Orgánica 1/2025
- art. 81.2.º CC
- art. 233 CC
- art. 552.10.1 Código Civil
- art. 404 CC
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

### Avisos de actualización (2) — se aplican en el texto, nunca se copian en el documento

- Junto a «…CIA [ELEGIR: SECCIÓN CIVIL / SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD] DE [SEDE]»: Denominación legal: Sección de Familia, Infancia y Capacidad. Si no existe en el partido, conoce la Sección Civil o la Única (art. 86.3-4 LOPJ). Fuente: LOPJ arts. 84.2.a) y 86 (redacc. LO 1/2025, BOE-A-2025-76).
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

AL TRIBUNAL DE INSTANCIA [ELEGIR: SECCIÓN CIVIL / SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD] DE [SEDE]

Dña. [NOMBRE Y APELLIDOS], Procurador de los Tribunales, que actúa en nombre y representación de D. [NOMBRE Y APELLIDOS], provisto de D.N.I. n.º [NÚMERO], con domicilio en [LOCALIDAD], calle [CALLE], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], bajo dirección del Letrado D./Dña. [NOMBRE Y APELLIDOS], colegiada n.º [NÚMERO] del Iltre. Colegio de Abogados de [COLEGIO], cuyo despacho se abre en [LOCALIDAD], calle [CALLE], ante el Tribunal comparezco y como mejor en Derecho proceda, DIGO:

Que por medio del presente escrito, siguiendo la instrucción de mi mandante, vengo a formular DEMANDA CONTENCIOSA DE DIVORCIO frente a su esposa Dña. [NOMBRE Y APELLIDOS], con domicilio actual en [DOMICILIO], con base a los siguientes datos y argumentos:

HECHOS

PRIMERO.- Mi mandante contrajo matrimonio canónico con Dña. [NOMBRE Y APELLIDOS], en [LOCALIDAD], el día [FECHA]. Se acompaña la correspondiente certificación de matrimonio expedida por el Registro Civil de [LOCALIDAD] (documento n.º [NÚMERO]).

De dicha unión nacieron y viven dos hijos, de nombre [NOMBRE DEL HIJO/A 1] y [NOMBRE DEL HIJO/A 2], nacidos el [FECHA], y el [FECHA], hoy todos mayores de edad y que viven fuera del domicilio conyugal. Se adjuntan las correspondientes certificaciones de nacimiento que ha emitido el Registro Civil de [LOCALIDAD] (documentos n.º [NÚMERO]).

SEGUNDO.- El régimen económico del matrimonio es el de separación de bienes, ya que por residencia y lugar de celebración del matrimonio la vecindad de los cónyuges es la catalana, no habiéndose otorgado nunca capitulaciones matrimoniales (art. 231-10 del Libro II del Código Civil de Cataluña aprobado por Ley 25/2010 de 29 de julio, en adelante, CCC).

No obstante, durante los años de convivencia matrimonial los litigantes han trabajado como empleados en la empresa [DENOMINACIÓN SOCIAL] aportando sus sueldos íntegramente a la economía familiar.

Debido al prolongado período de convivencia, la buena situación laboral de ambos y su capacidad de ahorro, los litigantes han tenido un incremento patrimonial que les ha permitido la adquisición de la vivienda familiar y otros bienes. Se acompaña como documento n.º [NÚMERO] la escritura de compraventa de la vivienda donde se ha desarrollado la convivencia durante los últimos quince años, perteneciente en plena propiedad y por mitades indivisas a ambos cónyuges, y la inscripción registral correspondiente.

TERCERO.- Con fecha [FECHA] se interpuso demanda de separación que se siguió con el n.º [Nº] de autos [TIPO Y Nº DE PROCEDIMIENTO] en el Tribunal de Instancia de [SEDE], plaza n.º [Nº] , recayendo con fecha [FECHA] sentencia firme en la que se declara la separación legal de los cónyuges y las medidas definitivas a adoptar. Se acompaña como documento n.º [NÚMERO] testimonio literal de la citada resolución.

Como consecuencia de las graves desavenencias entre los cónyuges, mi representado está persuadido de lo adecuado de su decisión de disolver el vínculo matrimonial mediante divorcio, sin que haya sido posible tramitarlo de mutuo acuerdo, por lo que se interpone la presente demanda contenciosa.

CUARTO.- Como efectos de la demanda que ahora se ejercita, se solicita el mantenimiento de estas medidas aprobadas por sentencia de separación, exceptuando la referente a la atribución del derecho de uso de la vivienda familiar a la esposa y a los hijos entonces menores de edad, interesando la extinción de este derecho de uso y disfrute, al considerar que han cambiado las circunstancias personales y familiares tenidas en cuenta a la hora de adoptar dichas medidas, que denotan que aquellos han dejado de presentar un interés más necesitado de protección, por cuanto tal y como se acredita mediante los documentos n.º [NÚMERO] el esposo ha mermado sus ingresos cobrando en la actualidad una pensión de invalidez permanente y los hijos comunes han cumplido la mayoría de edad siendo independientes económicamente de sus padres. Mientras, la esposa no reside en esta vivienda, no haciendo uso de tal derecho, ya que reside en la vivienda sita en [LOCALIDAD], como se demuestra con los documentos n.º [Nº DE DOCUMENTO]

QUINTO.- Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento nº [Nº DE DOCUMENTO]

FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN.

Es competente la jurisdicción civil, según lo establecido en los arts. 9.2 y 21.1 LOPJ.

II.- COMPETENCIA.

Es competente el Tribunal de Instancia del lugar del domicilio del demandado, que es el criterio alternativo, a elección del demandante, conforme al art. 769.1, párrafo 1.º LEC.

III.- PROCEDIMIENTO.

El procedimiento adecuado es el del art. 770 LEC para conocer de las demandas de divorcio contenciosas.

IV.- ACUMULACIÓN DE ACCIONES.

El art. 232-12 CCC introduce la especialidad procesal -amparada en el art. 149.1-6.° CE- relativa a la acumulabilidad a los juicios de nulidad, separación y divorcio, de la acción de división de bienes comunes en proindiviso ordinario por parte de los cónyuges bajo régimen de separación de bienes, entre los que gozan de vecindad civil catalana, procediéndose a la indicada división de los bienes en el trámite de ejecución de la sentencia.

V.- CAPACIDAD.

Mi mandante ostenta capacidad procesal suficiente, conforme al artículo 6.1.1.º LEC.

VI.- POSTULACIÓN.

Comparece representado por Procurador debidamente habilitado para actuar en el territorio de este Tribunal, y asistido por Abogado, conforme a lo establecido en el artículo 750.1 LEC.

VII.- LEGITIMACIÓN.

Tienen legitimación ordinaria por hallarse en la situación jurídica de relación matrimonial ambos cónyuges (art. 86 CCiv y art. 10 párrafo 1.º LEC), siendo el objeto del proceso principal la pretensión de disolución vincular por divorcio.

VIII.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC en relación con el art. 437.1 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

IX.- FONDO DE LA PRETENSIÓN

I.-Petición de divorcio.

El fondo de la pretensión consiste en la declaración de divorcio, a fin de la disolución del matrimonio, a instancia de uno de los cónyuges, de conformidad con el art. 81.2.º CCiv, por remisión del art. 86 CCiv, sin que puedan oponerse por el otro cónyuge, no expresamente conforme ninguna causa de oposición material, al fundarse en la voluntad de no permanecer casado, como corolario legal del derecho del art. 32 CE a contraer matrimonio.

II.-Medidas que han de regular los efectos del divorcio.

En lo referente a sus efectos, prevé el art. 233-7.1 CCC que "las medidas ordenadas en un proceso matrimonial pueden modificarse, mediante una resolución posterior, si varían sustancialmente las circunstancias concurrentes en el momento de dictarlas", que, dado que el procedimiento de divorcio ha de concluir mediante la resolución en forma de sentencia que le ponga fin, dicha resolución judicial posterior será la sentencia que ponga fin al procedimiento de divorcio, en el que, por tratarse de un proceso diferente y autónomo del de separación, aunque deba tenerse en cuenta lo en él resuelto atendidas las circunstancias entonces concurrentes, habrá de valorarse la concurrencia o no de dichas circunstancias sobrevenidas que determinen o no la modificación de la medida de que se trate, alteración sustancial que según se ha expuesto en el relato fáctico, concurre indudablemente en el presente caso.

El Sr./a [NOMBRE Y APELLIDOS] percibe pensión por invalidez permanente en grado de absoluta, habiéndose acreditado documentalmente que el importe de la misma asciende en el año [AÑO] a [IMPORTE] euros. Los hijos de los litigantes, menores de edad al tiempo de la separación de los progenitores, son en la actualidad mayores de edad e independientes económicamente. De estos hechos deriva sin duda que se ha producido una modificación de la situación existente al tiempo del dictado de sentencia de separación conyugal, y ello determina que no percibiéndose en la Sra. [NOMBRE Y APELLIDOS] y en los hijos mayores de edad, a los efectos del art. 233-20 CCC, una mayor necesidad en la atribución del uso del domicilio conyugal, dada la propia situación del Sr./a [NOMBRE Y APELLIDOS], no procede conceder dicho uso a los mismos.

La concurrencia de hijos mayores de edad, nacidos en el curso de la relación matrimonial, determina la aplicación del art. 233-20.3.b) CCC, el cual se extiende no solo a los supuestos de inexistencia de hijos, tal como reseña el precepto, sino también a los casos de la concurrencia de hijos mayores de edad, ya que aunque el matrimonio tiene dos hijos, hace tiempo que alcanzaron autosuficiencia económica, y el criterio de atribución del uso en que sustenta dicho precepto es el de necesidad.

Sentada tal consideración, no se aprecia en ninguno de los cónyuges un interés más necesitado de protección, que fundamente la atribución en su favor del uso del domicilio familiar en forma temporal, mientras dure tal situación de necesidad.

Lo anterior determina que deba dejarse sin efecto la atribución del uso de la vivienda a la esposa y a los hijos comunes, toda vez que no puede ser mantenida en sede del pleito de familia ninguna limitación al derecho de propiedad que ostentan ambos copropietarios sobre la vivienda, por lo que cualquiera de ellos puede ejercitar las acciones que se derivan de los arts. 552.10.1 del Libro V del Código Civil de Catalunya, relativo a los derechos reales, aprobado por Ley 5/2006 de 10 de mayo; y 232-12 CCC, en lo que se refiere a la liquidación y partición de la propiedad en común.

III.-Acciones acumuladas.

Se formula acumuladamente en esta demanda acción de división de cosa común, consistente exclusivamente en la finca que constituyera el domicilio familiar sita en la calle [CALLE], número [NÚMERO] de [LOCALIDAD], referida en el ordinal segundo de los hechos de la demanda, que es propiedad indivisa de ambos cónyuges por partes iguales, con invocación del art. 232-12 CCC.

Como indica la jurisprudencia (SAP Barcelona -18.ª- de 10 de marzo de 2005, rec. 436/2004 y SAP Barcelona -18.ª- de 3 de mayo de 2005, rec. 292/2004, entre otras) la finalidad de este precepto no es otra que la de facilitar que a través del mismo y único proceso puedan los cónyuges resolver otras cuestiones colaterales y subsiguientes a la ruptura del vínculo matrimonial, posibilitando asimismo la "separación" efectiva de patrimonios, en el sentido de acordar la división de aquellos bienes que pudieran tener en régimen de proindiviso. Así lo aclaraba de forma expresa la Exposición de Motivos de la propia Llei 9/1998: "Constituye otra innovación interesante la posibilidad de solicitar, por razones de economía procesal, en aquellos procedimientos o en los trámites indicados, la división de los bienes de los cónyuges en indivisión".

En concordancia con la previsión del art. 232-12 CCC, el art. 233-4.2 dispone que la autoridad judicial deberá acordar la liquidación del régimen matrimonial (lo que es de aplicación a los regímenes de gananciales y participación) y la división de los bienes comunes o en comunidad ordinaria indivisa (lo que es de aplicación al régimen matrimonial de separación de bienes), si alguno de los cónyuges lo solicita.

Por lo tanto es la propia ley la que dispone que se procederá a la división de los bienes comunes, por lo que no cabrá exigir para la indivisión mayores requisitos que los propios de la división de la cosa común que contempla el art. 552.10.1 del Libro V del Código Civil de Catalunya, relativo a los derechos reales, aprobado por Ley 5/2006 de 10 de mayo, sin que a estos efectos deba acreditarse necesidad económica ni personal. Tratándose de una vivienda, la efectividad de la división se llevará a cabo en la forma prevista en el art. 552.11.5, esto es, la legislación catalana no prevé la venta en pública subasta, tal y como hace el art. 404 CCiv, como medio de poner fin a la indivisión, sino que deja en manos del azar la adquisición de la propiedad total. Todo ello pasa, por la necesidad de peritar previamente el inmueble para que, sabido el precio, pueda alguna de las partes no tener interés en su adquisición, pero si ello no es así, será la suerte la que deberá decidir, en el bien entendido de que el perito lo será necesariamente por designación judicial, y el adjudicatario o adjudicataria deberá pagar al otro el valor pericial de su participación, que en ningún caso tiene la consideración de precio ni de exceso de adjudicación. Si ningún cotitular tiene interés, se venderá y se repartirá el precio.

X.- COSTAS.

No hay ninguna razón para excluir la aplicación del principio del vencimiento en punto a las costas procesales (art. 394 LEC), debiéndose condenar al demandado que se oponga, dado que el obtener la razón precisando de un proceso no ha de suponer una merma patrimonial del que tiene razón.

En virtud de lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito con los documentos que se acompañan y sus copias, se digne admitirlos, tenerme por comparecida y parte en la representación que ostento, entendiéndose conmigo las sucesivas diligencias y por formulada DEMANDA DE DISOLUCIÓN DEL MATRIMONIO POR DIVORCIO y ACCIÓN DE DIVISIÓN DE COSA COMÚN CON RESPECTO A BIEN EN PROINDIVISO, de modo que seguido que sea el pertinente procedimiento, se dicte en su día sentencia por la estimando la presente demanda:

1.- DECLARE disuelto por divorcio el matrimonio de los esposos D. y Dña. [NOMBRE Y APELLIDOS], manteniendo como efectos los acordados en la sentencia de separación a excepción del derecho de uso de la vivienda familiar en favor de la Sra. [NOMBRE Y APELLIDOS] y de los hijos comunes de los litigantes, que debe declararse extinguido.
2.- ACUERDE la división de su patrimonio común adquirido constante el matrimonio en proindiviso, constituido por la vivienda sita en esta ciudad, calle [CALLE] núm. [NÚMERO], piso núm. [NÚMERO], puerta núm. [NÚMERO], que habrá de llevarse a efecto en fase de ejecución de sentencia.

En todo caso, se pronuncie el reintegro de las costas con cargo al demandado opuesto.

Es Justicia de hacerse en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a

========================================================================
