---
name: documento-voluntades-anticipadas-testamento-vital-civ-0386
description: "Documento de voluntades anticipadas o testamento vital. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Documento de voluntades anticipadas o testamento vital

> Formulario **CIV-0386** del plugin **Discapacidad y medidas de apoyo (Ley 8/2021)** (`formularios-discapacidad-y-medidas-de-apoyo`) · Civil › Capacidad y medidas de apoyo · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Documento de voluntades anticipadas o testamento vital» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Documento de voluntades anticipadas o testamento vital” para mi caso». También puedes invocarla directamente con `/formularios-discapacidad-y-medidas-de-apoyo:documento-voluntades-anticipadas-testamento-vital-civ-0386`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-discapacidad-y-medidas-de-apoyo:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Discapacidad y medidas de apoyo (Ley 8/2021)) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (4 veces)
- [ ] Nº (4 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] AÑO
- [ ] CALLE
- [ ] CLASE
- [ ] DÍA
- [ ] MES
- [ ] NIF/DNI
- [ ] NOMBRE DEL NOTARIO
- [ ] NÚMERO
- [ ] PISO
- [ ] SERIE

## Normas que cita el formulario

- No cita artículos concretos; Claude localizará las normas aplicables con Jurisprudenciator si el documento las necesita.

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

TESTAMENTO VITAL

En [LOCALIDAD], mi residencia, a [DÍA] de [MES] de [AÑO]

Ante mí [NOMBRE DEL NOTARIO], Notario/a del Ilustre Colegio de Notarios de [LOCALIDAD]

COMPARECE

D. [NOMBRE Y APELLIDOS], mayor de edad, soltero, vecino de [LOCALIDAD], con domicilio en [LOCALIDAD], en la calle [CALLE], número [NÚMERO], piso [PISO], letra, con D.N.I. número [NIF/DNI]

A mi juicio, la capacidad legal necesaria para para otorgar TESTAMENTO VITAL, y al efecto, y a tal efecto,

DICE

Que es hijo/a de los consortes D. [NOMBRE Y APELLIDOS], fallecidos ambos. Que está soltero/a y carece de toda clase de legitimarios.

Que ordena su última voluntad a tenor de las siguientes

ESTIPULACIONES

Designación de representante

Designo como representante a fin de que tome la determinación o determinaciones precisas y actúe como interlocutor válido frente a médicos, personal sanitario en general, y antes las instituciones sanitarias que en su caso deban prestarme asistencia, a D. Dicha persona debe en consecuencia recibir la información precisa y detallada para cualquier asistencia, intervención, o aplicación de tratamiento, para en su caso prestar el correspondiente consentimiento informado.

Autorizo en consecuencia a quien designo representante para que en mi nombre tome decisiones respecto a mi salud, asistencia sanitaria, intervenciones quirúrgicas, aplicación de tratamientos, internamientos y cualquier otra circunstancia relacionada con dicha salud, para el caso de que no pueda por mí mismo tomar dichas decisiones.

Las decisiones que tome mi representante no pueden ir en contradicción con las voluntades que de manera expresa y anticipada hago constar en este documento.

Manifestación de voluntades

Manifiesto mi expresa voluntad de:

a) Se me tenga informado en todo momento de toda las circunstancias relativas a la salud y a la asistencia sanitaria que precise, y en todo caso si no fuere posible por mi estado recibir dicha información la misma sea facilitada a mi representante;

b) No prolongar mi vida de manera artificial, mediante técnicas de soporte vital tales como ventilación mecánica, diálisis, reanimación cardiopulmonar, fluidos intravenosos, fármacos o alimentación artificial, siempre que dichas técnicas aplicadas sean inútiles para evitar mi muerte;

c) Que se me suministren los fármacos necesarios para paliar en lo posible el sufrimiento físico o psíquico, dolor, o malestar que pueda producir la enfermedad;

d) Se me garantice la asistencia necesaria para procurarme una muerte digna;

e) Que no se me apliquen tratamientos complementarios o terapias que no garanticen efectividad o que sean inútiles en el propósito de prolongar mi vida en las circunstancias que he expuesto anteriormente;

f) Que se prescinda del internamiento en centro sanitario, si fuere posible aplicar el tratamiento indispensable en mi propio domicilio;

g) En caso de embarazo todas las anteriores disposiciones quedarán en suspenso hasta que se produzca el parto, en caso de que éste sea factible, y ello no afecte negativamente al feto, ya que en tal caso siempre se tendrá en cuenta en primer lugar lo más favorable para que el parto llegue a buen fin;

h) Manifiesto además mi voluntad de donar mis órganos para transplantes, tratamientos, investigación o enseñanza.

Copias

El señor compareciente autoriza que cualquier persona pueda pedir y obtener copias de esta acta, mientras no conste en ella nota de prohibición o revocación

RESERVAS Y ADVERTENCIAS LEGALES

Así lo dice y otorga, siendo las [Nº] horas y [Nº] minutos.

Leo en alta voz el contenido de este testamento, por elección de su otorgante, advertida por mí de su derecho a leerlo por sí, y de explicarle yo, el Notario, su contenido del que me manifiesta su conformidad, por ser fiel y exacta expresión de su voluntad, y se ratifica y firma conmigo.

De conocer a la compareciente y, en general, de haberse observado las formalidades legales en un solo acto y de todo lo demás consignado en este instrumento público, que queda extendido en [Nº] folios de la clase [CLASE], serie [SERIE], números [Nº], el presente y el siguiente en orden, doy fe.

Firmas

========================================================================
