---
name: demanda-consensual-medidas-parentales-economicas-tras-civ-0188
description: "Demanda consensual de medidas parentales y económicas tras ruptura de pareja de hecho (Cataluña). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda consensual de medidas parentales y económicas tras ruptura de pareja de hecho (Cataluña)

> Formulario **CIV-0188** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Demanda de mutuo acuerdo en solicitud de adopción de medidas sobre responsabilidades parentales y relaciones patrimoniales derivadas de la ruptura de la pareja estable conforme a Derecho civil especial de Cataluña

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda consensual de medidas parentales y económicas tras ruptura de pareja de hecho (Cataluña)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda consensual de medidas parentales y económicas tras ruptura de pareja de hecho (Cataluña)” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-consensual-medidas-parentales-economicas-tras-civ-0188`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (12 veces)
- [ ] LOCALIDAD (7 veces)
- [ ] NÚMERO (7 veces)
- [ ] FECHA (4 veces)
- [ ] CALLE
- [ ] COLEGIO
- [ ] DNI/NIE
- [ ] DOMICILIO
- [ ] FOLIO
- [ ] LIBRO
- [ ] LUGAR
- [ ] MES
- [ ] NOMBRE DEL HIJO
- [ ] Nº
- [ ] TOMO

## Normas que cita el formulario

- art. 234 CC
- art. 233 CC
- art. 6 LEC
- art. 769.3 LEC
- art. 777 LEC
- art. 750.2 LEC
- art. 90.3 CC

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

### Avisos de actualización (0) — se aplican en el texto, nunca se copian en el documento

- Ninguno.

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

SECCIÓN DE DE FAMILIA DE [LOCALIDAD]

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, que actúa en nombre y representación de Doña [NOMBRE Y APELLIDOS] y Don [NOMBRE Y APELLIDOS], mayores de edad, solteros, vecinos de [LOCALIDAD] y con domicilio en [LOCALIDAD] y [DNI/NIE], respectivamente, según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como doc. n.º [NÚMERO], bajo dirección del Letrado/a D./Dña. [NOMBRE Y APELLIDOS],colegiado n.º [NÚMERO] del Iltre. Colegio de Abogados de [COLEGIO], cuyo despacho se abre en [LOCALIDAD], calle [CALLE], ante el Tribunal comparezco y como mejor en Derecho proceda, DIGO:

Que por medio del presente escrito, siguiendo las instrucciones de mis mandantes, vengo a formular demanda de mutuo acuerdo sobre ADOPCIÓN DE MEDIDAS SOBRE RESPONSABILIDADES PARENTALES Y RELACIONES PATRIMONIALES TRAS LA RUPTURA DE LA UNIÓN ESTABLE formada por mis mandantes, con base en los siguientes:

HECHOS

PRIMERO.- Doña [NOMBRE Y APELLIDOS] y Don [NOMBRE Y APELLIDOS], formaron familia natural desde la fecha [FECHA], en la que iniciaron su relación paramatrimonial con intención de permanencia y consolidación, como se acredita mediante certificación expedida por el Registro Municipal de Uniones Civiles del Ayuntamiento de [LOCALIDAD] que se acompaña como doc. n.º [NÚMERO].

SEGUNDO.- Fruto de esta unión nació un hijo, de nombre [NOMBRE DEL HIJO], nacido el [FECHA], inscrito en el Registro Civil de [LOCALIDAD], Libro [LIBRO], Tomo [TOMO], Folio [FOLIO], por consiguiente menor de edad; aparece inscrito como hijo de mis mandantes, según se demuestra con la certificación literal de nacimiento que se acompaña como doc. n.º [NÚMERO].

TERCERO.- Esta convivencia lo ha sido con carácter paramatrimonial, en el sentido de relación afectiva semejante a la de las parejas casadas, heterosexual, monógama, estable y duradera, puesto que alcanzó [Nº] años, apareciendo ante los vecinos, amigos, compañeros de trabajo y familiares como marido y mujer, compartiendo techo, ingresos y vida sentimental, siendo el último domicilio común [DOMICILIO], como acredita el contrato de arrendamiento que se adjunta como doc. n.º [NÚMERO].

CUARTO.- Hace unos meses mis mandantes decidieron poner fin a la convivencia en pareja por desavenencias que no vienen al caso, comunicando fehacientemente Doña [NOMBRE Y APELLIDOS] a Don [NOMBRE Y APELLIDOS] su decisión de dar por extinguida la relación de unión estable de pareja existente entre ambos, según lo establecido por el art. 234-4.1e) del Código Civil de Cataluña, en adelante CCC (doc. n.º [NÚMERO]), y desde el pasado día [FECHA] de [MES] viven de forma separada en los domicilios anteriormente referenciados.

QUINTO.- Después de diversas negociaciones Doña [NOMBRE Y APELLIDOS] y Don [NOMBRE Y APELLIDOS] han suscrito una propuesta de convenio en el que regulan los efectos de su ruptura respecto a las relaciones paterno-filiales y de las relaciones patrimoniales entre los exconvivientes, en cumplimiento de lo establecido por el apartado 2 del art. 234-6 CCC, en relación con el art. 233-2 del mismo texto.

Se adjunta al presente escrito, como documento n.º [NÚMERO], la propuesta de convenio firmada por ambos progenitores para su homologación judicial, que incluye Plan de Parentalidad ajustado a las exigencias del art. 233-9 CCC.

A los anteriores hechos son de aplicación los siguientes,

FUNDAMENTOS DE DERECHO

I.- CAPACIDAD.

Mis representados ostentan la capacidad procesal necesaria conforme a lo establecido en los arts. 6 y siguientes LEC.

II.- LEGITIMACIÓN.

Mis representados se hallan legitimados por haber formado parte de la unión de hecho y en su condición de padres del menor sobre el que han de recaer los efectos del convenio suscrito entre las partes, habida cuenta que son los que se hallan en la situación jurídica respectiva del derecho-deber de cuidar de los hijos menores no emancipados (arts. 236-1 y 236-17.1 CCC).

III.- JURISDICCIÓN.

Es competente la jurisdicción civil, conforme a lo dispuesto en los arts. 9.2 y 21.1 LOPJ.

IV.- COMPETENCIA.

Es competente el Tribunal al que nos dirigimos de conformidad con lo dispuesto en el art. 769.3 LEC artículo 1.2 del RD 1322/81 de 3 de julio), que fija como fuero de competencia territorial el correspondiente al Tribunal del lugar del último domicilio común de los solicitantes.

V.- PROCEDIMIENTO.

En cuanto al procedimiento a seguir, resulta de aplicación el trámite previsto en el art. 777 LEC, que regula el procedimiento de mutuo acuerdo, y ello en virtud de la remisión que establece la Disposición adicional 5.ª CCC.

VI.- POSTULACIÓN.

Al amparo de lo dispuesto en el art. 750.2 LEC, para el caso de solicitudes de común acuerdo, se concurre con una sola defensa y representación.

VII.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD

La presente demanda no está sujeta al previo intento de resolución de controversias en vía no jurisdiccional, de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia, por tratarse en sí de un acuerdo consensual y voluntario entre las partes, necesitando únicamente la homologación del mismo por parte del Tribunal, siendo que el convenio regulador (arts. 775.2 y 777.9 LEC y art. 90.3 CCiv) se entiende acreditativo de haber realizado esa actividad negociadora.

VIII.- FONDO DE LA PRETENSIÓN.

El art. 234-7 CCC regula el ejercicio de la guarda de los hijos y relaciones personales tras la extinción de la pareja estable, con remisión a los genéricos arts. 233-8 a 233-13 CCC sobre las relaciones parentales tras las rupturas matrimoniales.

Respecto a la atribución del uso de la vivienda familiar, rige lo dispuesto en el art. 234-8 que se remite a su vez a lo establecido en los apartados 6.º y 7.º del art. 233-20 y los arts. 233-21 a 233-25.

En cuanto a la compensación económica por razón de trabajo y la prestación alimentaria, rige lo dispuesto en los arts. 234-9, 234-10, 234-11, 234-12 y 234-13.

Por lo expuesto,

SUPLICO AL TRIBUNAL

que teniendo por presentado este escrito, con los documentos y copias que se acompañan, se sirva admitirlo y en méritos del mismo y en la representación que ostento de Doña [NOMBRE Y APELLIDOS] y Don [NOMBRE Y APELLIDOS], tenga por instada DEMANDA DE MUTUO ACUERDO EN SOLICITUD DE ADOPCIÓN DE MEDIDAS SOBRE RESPONSABILIDADES PARENTALES Y RELACIONES PATRIMONIALES DERIVADAS DE LA RUPTURA DE LA PAREJA ESTABLE habida entre mis mandantes, para la aprobación judicial de la propuesta de convenio regulador suscrito entre ambos y el Plan de Parentalidad que contiene, dando traslado de la misma al Ministerio Fiscal y, previos los trámites legales pertinentes, incluida la ratificación del convenio ante el Letrado de la Administración de Justicia, dicte en su día sentencia por la que se apruebe judicialmente dicho Convenio Regulador en todos sus extremos.

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a

========================================================================
