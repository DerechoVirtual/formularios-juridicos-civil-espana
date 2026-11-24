---
name: escrito-inicial-oposicion-resolucion-administrativa-civ-0347
description: "Escrito inicial de oposición a resolución administrativa de protección de menores. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito inicial de oposición a resolución administrativa de protección de menores

> Formulario **CIV-0347** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Escrito inicial con el que los progenitores manifiestan su intención de oponerse a una resolución administrativa de la entidad pública de protección de menores (por ejemplo, la declaración de desamparo con asunción de la tutela por ministerio de la ley), conforme al art. 780 LEC. Tras este escrito se reclama el expediente administrativo y se emplaza a la parte para presentar la demanda.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito inicial de oposición a resolución administrativa de protección de menores» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito inicial de oposición a resolución administrativa de protección de menores” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:escrito-inicial-oposicion-resolucion-administrativa-civ-0347`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE DEL MENOR (6 veces)
- [ ] AÑO (4 veces)
- [ ] DÍA (4 veces)
- [ ] MES (4 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] DOMICILIO (2 veces)
- [ ] EDAD (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] ÓRGANO ADMINISTRATIVO (2 veces)
- [ ] COLEGIO
- [ ] COMUNIDAD AUTÓNOMA
- [ ] NOMBRE Y APELLIDOS DE LA LETRADA
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] Nº DE COLEGIADA
- [ ] Nº DE DOCUMENTO
- [ ] NÚMERO
- [ ] PROVINCIA
- [ ] SEDE

## Normas que cita el formulario

- art. 780.2 LEC
- art. 779 LEC
- art. 780 LEC
- art. 753 LEC

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

NOTAS PRÁCTICAS: la tramitación de estos procedimientos tiene carácter preferente. El plazo para presentar la oposición es de dos meses desde la notificación de la resolución. La competencia territorial corresponde, conforme al art. 779 LEC, al Tribunal de Instancia del domicilio de la entidad pública y, en su defecto, o en los supuestos de adopción, al del domicilio del adoptante.


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

A LA SECCIÓN CIVIL (SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD) DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales y de D. [NOMBRE Y APELLIDOS] y Dña. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], calle [DOMICILIO], n.º [NÚMERO], representación que acredito con copia de poder notarial, que tengo aceptado y cuya reproducción acompaño para que me sea devuelto el original, previo su testimonio en autos, porque se necesita para más usos, asistidos de la Letrada Dña. [NOMBRE Y APELLIDOS DE LA LETRADA], colegiada n.º [Nº DE COLEGIADA] del Ilustre Colegio de Abogados de [COLEGIO], cuyo despacho se abre en [LOCALIDAD], calle [DOMICILIO], ante el Tribunal comparezco y, como mejor proceda en Derecho, DIGO:

Que mediante el presente escrito, y en cumplimiento de lo dispuesto en el art. 780.2 LEC, mis representados manifiestan la intención de oponerse a la resolución administrativa de fecha [DÍA] de [MES] de [AÑO], dictada por [ÓRGANO ADMINISTRATIVO: Delegación Territorial de [PROVINCIA] del Departamento/Consejería competente en materia de servicios sociales de la Comunidad Autónoma de [COMUNIDAD AUTÓNOMA]], sobre protección de los menores [NOMBRE DEL MENOR] y [NOMBRE DEL MENOR], en base a los siguientes datos y consideraciones jurídicas:

HECHOS

PRIMERO.– Mis mandantes son los padres de los menores [NOMBRE DEL MENOR] y [NOMBRE DEL MENOR], que tienen en la actualidad [EDAD] y [EDAD] años de edad, respectivamente.

SEGUNDO.– Con fecha [DÍA] de [MES] de [AÑO] [ÓRGANO ADMINISTRATIVO] dictó resolución por la que se declaraba la situación legal de desamparo de los citados menores, asumiendo la tutela de los mismos por ministerio de la ley, quedando en acogimiento [ELEGIR: residencial / familiar].

TERCERO.– Aunque la anterior declaración fue notificada a mis representados con fecha [DÍA] de [MES] de [AÑO] (documento n.º [Nº DE DOCUMENTO]), no han tenido acceso al expediente administrativo en el cual se fundamenta la misma, por lo que se desconocen los hechos en los que se ha podido basar la entidad pública para dictar dicha resolución y, en todo caso, niegan cualquier alegación que se pueda realizar en cuanto al desamparo de los menores, pues están perfectamente atendidos, no solo por sus padres, sino también por sus tíos, primos y abuelos, por lo que esta parte se opone a dicha resolución.

FUNDAMENTOS DE DERECHO

I.– COMPETENCIA

La competencia corresponde al Tribunal de Instancia del domicilio de la entidad pública que dictó la resolución, conforme a lo establecido en el art. 779 LEC.

II.– PROCEDIMIENTO

Conforme a lo establecido en el art. 780 LEC, quien pretenda oponerse a una resolución administrativa en materia de protección de menores presentará un escrito inicial en el que sucintamente expresará su pretensión y la resolución a que se opone.

El Letrado de la Administración de Justicia reclamará a la entidad administrativa un testimonio completo del expediente, que deberá ser aportado en el plazo de diez días.

Recibido el testimonio del expediente administrativo, se emplazará al actor por diez días para que presente la demanda, que se tramitará con arreglo a lo previsto en el art. 753 LEC.

III.– ACUMULACIÓN

A efectos de lo dispuesto en el art. 780.2, párrafo 2.º, LEC, se manifiesta que no existen otros procedimientos relativos a los citados menores, no procediendo en consecuencia la acumulación de procedimientos.

Por lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito, se sirva admitirlo, teniendo por instado el procedimiento de oposición a la resolución administrativa de desamparo de los menores [NOMBRE DEL MENOR] y [NOMBRE DEL MENOR], dictada por [ÓRGANO ADMINISTRATIVO], y reclame testimonio completo del expediente administrativo a la entidad pública, y una vez recibido y puesto de manifiesto a mis mandantes, se emplace por el Letrado de la Administración de Justicia a esta parte para interponer la correspondiente demanda, junto a lo demás que en Derecho proceda.

Es justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Abogado/a Firma del Procurador/a
