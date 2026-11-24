---
name: demanda-mutuo-acuerdo-sobre-guarda-custodia-alimentos-civ-0325
description: "Demanda de mutuo acuerdo sobre guarda, custodia y alimentos de hijos tras ruptura de unión de hecho. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de mutuo acuerdo sobre guarda, custodia y alimentos de hijos tras ruptura de unión de hecho

> Formulario **CIV-0325** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Demanda de mutuo acuerdo sobre guarda, custodia y alimentos de hijos menores de edad tras la ruptura de una unión de hecho.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de mutuo acuerdo sobre guarda, custodia y alimentos de hijos tras ruptura de unión de hecho» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de mutuo acuerdo sobre guarda, custodia y alimentos de hijos tras ruptura de unión de hecho” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-mutuo-acuerdo-sobre-guarda-custodia-alimentos-civ-0325`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] LOCALIDAD (6 veces)
- [ ] FECHA (4 veces)
- [ ] COLEGIO (2 veces)
- [ ] FOLIO (2 veces)
- [ ] LIBRO (2 veces)
- [ ] TOMO (2 veces)
- [ ] CALLE
- [ ] DIRECCIÓN
- [ ] DOMICILIO
- [ ] LUGAR
- [ ] Nº
- [ ] Nº DE DOCUMENTO
- [ ] NÚMERO

## Normas que cita el formulario

- art. 6 LEC
- art. 154 CC
- art. 769.3 LEC
- art. 777 LEC
- art. 748.4.º LEC
- art. 777.1 LEC
- art. 770.5.ª LEC
- art. 750.2 LEC
- art. 4.1 CC
- art. 110 CC
- art. 142 CC
- art. 749.2 LEC

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

- Junto a «…IÓN CIVIL DE [LOCALIDAD] SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD DE [LOCALIDAD]»: Denominación legal: Sección de Familia, Infancia y Capacidad. Si no existe en el partido, conoce la Sección Civil o la Única (art. 86.3-4 LOPJ). Fuente: LOPJ arts. 84.2.a) y 86 (redacc. LO 1/2025, BOE-A-2025-76).

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

SECCIÓN CIVIL DE [LOCALIDAD]

SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD DE [LOCALIDAD]

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, que actúa en nombre y representación de Dña.y D. [NOMBRE Y APELLIDOS], mayores de edad, solteros, vecinos de [LOCALIDAD] y con domicilio en [LOCALIDAD] y [DOMICILIO], respectivamente, como acredito mediante la designación por turno de oficio efectuada por el Iltre. Colegio de Procuradores de [COLEGIO], previamente comunicada, bajo dirección del Letrado/a D./Dña. [NOMBRE Y APELLIDOS],colegiado/a n.º [NÚMERO] del Iltre. Colegio de Abogados de [COLEGIO], cuyo despacho se abre en [DIRECCIÓN], calle [CALLE], ante el Tribunal comparezco y como mejor en Derecho proceda, DIGO:

Que por medio del presente escrito, siguiendo las instrucciones de mis mandantes, vengo a formular demanda de mutuo acuerdo sobre GUARDA, CUSTODIA Y FIJACIÓN DE PENSIÓN DE ALIMENTOS para hijos menores de edad, nacidos de la unión estable formada por mis mandantes, con base en los siguientes:

HECHOS

PRIMERO.- Dña. y D. [NOMBRE Y APELLIDOS], formaron familia natural desde la fecha [FECHA], en la que iniciaron su relación paramatrimonial con intención de permanencia y consolidación, y fruto de esta unión nacieron dos hijos, A [NOMBRE Y APELLIDOS], nacido el [FECHA], inscrito en el Registro Civil de [LOCALIDAD], Libro [LIBRO], Tomo [TOMO], Folio [FOLIO]; y B [NOMBRE Y APELLIDOS], nacido el [FECHA], inscrito en el Registro Civil de [LOCALIDAD], Libro [LIBRO], Tomo [TOMO], Folio [FOLIO], por consiguiente menores de edad; ambos aparecen inscritos como hijos de los dos litigantes según se demuestra con las certificaciones literales de nacimiento que se acompañan como documentos números

Esta convivencia lo ha sido con carácter paramatrimonial, en el sentido de relación afectiva semejante a la de las parejas casadas, heterosexual, monógama, estable y duradera, puesto que alcanzó [Nº] años, apareciendo ante los vecinos, amigos, compañeros de trabajo y familiares como marido y mujer, compartiendo techo, ingresos y vida sentimental, siendo el último domicilio común

SEGUNDO.- Hace unos meses Dña. y D. decidieron poner fin a la convivencia en pareja por desavenencias que no vienen al caso, suscribiendo un convenio en el que regulaban los efectos de su ruptura respecto a las relaciones paterno-filiales.

Se adjunta al presente escrito, como documento número [Nº DE DOCUMENTO], el convenio firmado por ambos progenitores para su homologación judicial.

A los anteriores hechos son de aplicación los siguientes,

FUNDAMENTOS DE DERECHO

I.- CAPACIDAD

Mis representados ostentan la capacidad procesal necesaria conforme a lo establecido en los arts. 6 y siguientes LEC.

II.- LEGITIMACIÓN

Mis representados se hallan legitimados por haber formado parte de la unión de hecho y en su condición de padres de los menores sobre los que han de recaer los efectos del convenio suscrito entre las partes, habida cuenta que son los que se hallan en la situación jurídica respectiva del derecho-deber de velar por los hijos menores no emancipados (art. 154 CC).

III.- JURISDICCIÓN

Es competente la jurisdicción civil, conforme a lo dispuesto en los artículos 9.2 y 21.1 de la LOPJ.

IV.- COMPETENCIA

Es competente el Tribunal al que nos dirigimos de conformidad con lo dispuesto en el art. 769.3 LEC (en su caso, en relación con el artículo 1.2 del RD 1322/81 de 3 de julio), que fija como fuero de competencia territorial el correspondiente al Tribunal del lugar del último domicilio común de los progenitores.

V.- PROCEDIMIENTO

En cuanto al procedimiento a seguir, resulta de aplicación el trámite previsto en el art. 777 LEC, que regula el procedimiento de mutuo acuerdo, y ello en virtud de lo establecido en el art. 748.4.º de la LEC, al disponer que las disposiciones del Título Primero del Libro IV serán aplicables, entre otros, a los procesos que versen exclusivamente sobre guarda y custodia de hijos menores o sobre alimentos reclamados por un progenitor contra el otro en nombre de los hijos menores, como es el objeto de la presente litis.

La extensión del cauce procedimental de mutuo acuerdo para pretender la guarda, custodia y alimentos para hijos menores de las parejas de hecho, a pesar de los términos del art. 777.1 LEC, dimana de que la posibilidad de transformación del contencioso (art. 770.5.ª LEC) implica la posibilidad del recurso inicial al procedimiento consensual.

VI.- POSTULACIÓN

Al amparo de lo dispuesto en el art. 750.2 LEC, para el caso de solicitudes de común acuerdo, se concurre con una sola defensa y representación.

VII.- FONDO DE LA PRETENSIÓN

Resulta obvio la existencia de la denominada sociológicamente "unión de hecho" y que como familia natural, debe ser merecedora (como dice la STS de 29 de octubre de 1997, Rec. 2892/1993) de la misma protección por parte de los poderes públicos que para la familia jurídica establece el art. 39.1 de la Constitución Española, sobre todo cuando de dicho Texto no se desprende que haya una sola forma de familia reconocida.

Además la realidad social indica que tales uniones dan las características básicas de la familia jurídica, con la única característica especial de no existir una formalización religiosa o civil de tal unión de hecho.

Y así la STS de 18 de mayo de 1992, que cita la de 13 de junio de 1986 y la de 14 de julio de 1988, así como la del Tribunal Constitucional de 4 de abril de 1991, afirma que "las uniones libres aunque están carentes de precisa normativa, no por eso son totalmente desconocidas por nuestro ordenamiento jurídico. La Constitución no lo prevé, pero tampoco expresamente las interdicta y rechaza, y así se desprende de su art. 32 en relación al 39 que se proyecta a la protección de la familia en forma genérica, es decir como núcleo creado tanto por el matrimonio, como por la unión de hecho".

Se reconoce jurisprudencialmente no sólo la existencia social de estas uniones sino que las mismas constituyen una integración familiar defendible, y que crea derechos y obligaciones entre sus miembros, derechos que son trascendentes, por ejemplo, en materia de arrendamientos urbanos.

Incluso en el derecho comparado afín, el Tribunal de Casación de Italia vino a reconocer en su sentencia de 2 de febrero de 1977, la denominada "familia di fatto", como entidad social que ejercita unas funciones en la educación y mantenimiento de sus miembros, y que debe ser protegida a tenor de lo dispuesto en el art. 2 de la Constitución Italiana.

Más recientemente, en el ámbito autonómico, se han dictado Leyes de Parejas Estables en diversas Comunidades que reconocen los mismos derechos para este tipo de relaciones paramatrimoniales que para los matrimonios.

Mis representados formaron familia natural constituida por ellos mismos y sus hijos, y por lo ya expuesto se separaron, debiendo ahora regularse a través de la adopción de las medidas necesarias sus obligaciones y derechos con respecto a sus hijos menores. Al ser una separación de mutuo acuerdo se presenta para establecer dichas medidas acuerdo suscrito entre las partes.

Así, en relación a las medidas a adoptar en el caso de ruptura de la pareja de hecho son de aplicación de acuerdo a las reglas de la analogía (art. 4.1 CC) los arts. 91 y ss. CC en relación con el artículo 159 del mismo texto legal que dispone que "si los padres viven separados y no decidieren de común acuerdo, el Juez decidirá, siempre en beneficio de los hijos, al cuidado de qué progenitor quedarán los hijos menores de edad" y el art. 154 CC, que consagra como uno de los deberes fundamentales del titular de la patria potestad el de la alimentación de los hijos (art. 154, párrafo II.1.º CC), deber que se deriva de la relación paterno-filial hasta el punto de que la mantiene aún en los casos de privación de la patria potestad (art. 110 CC). Este deber-función se traduce en la obligación de prestar alimentos establecida en los arts. 142, 143, 144 y concordantes CC.

VIII.- PROPUESTA DE CONVENIO REGULADOR

Conforme a lo dispuesto en el apartado 2.º del art. 777 de la LEC, se aporta con el presente escrito, la documentación exigida en el mismo, y así por lo tanto, la propuesta de convenio regulador redactada con arreglo a lo establecido por la legislación civil y firmada por ambos progenitores.

IX.- INTERVENCIÓN DEL MINISTERIO FISCAL

Con arreglo al art. 749.2 LEC será preceptiva la intervención del Ministerio Fiscal, siempre que alguno de los interesados en el procedimiento sea menor.

Por lo expuesto,

X.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD

La presente demanda no está sujeta al previo intento de resolución de controversias en vía no jurisdiccional, de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia, por tratarse en sí de un acuerdo consensual y voluntario entre las partes, necesitando únicamente la homologación del mismo por parte del Tribunal, siendo que el convenio regulador (arts. 775.2 y 777.9 LEC y 90.3 CCiv) se entiende acreditativo de haber realizado esa actividad negociadora.

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito, con los documentos y copias que se acompañan, se sirva admitirlo y en méritos del mismo y en la representación que ostento de Dña. y D. [NOMBRE Y APELLIDOS], tenga por instada DEMANDA DE MUTUO ACUERDO EN SOLICITUD DE ADOPCIÓN DE MEDIDAS PATERNO-FILIALES DERIVADAS DE LA RUPTURA DE LA UNIÓN DE HECHO habida entre mis mandantes, para la aprobación judicial de la propuesta de convenio regulador suscrito entre ambos, dando traslado de la misma al Ministerio Fiscal y, previos los trámites legales pertinentes, incluida la ratificación del convenio ante el Letrado de la Administración de Justicia, dicte en su día sentencia por la que se apruebe judicialmente dicho convenio regulador en todos sus extremos.

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a

========================================================================
