---
name: escrito-solicitud-nombramiento-tercer-perito-civ-0858
description: "Escrito de solicitud de nombramiento de un tercer perito. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito de solicitud de nombramiento de un tercer perito

> Formulario **CIV-0858** del plugin **Proceso civil: demandas, contestaciones, prueba y vista** (`formularios-proceso-civil`) · Civil › Escritos procesales (demanda, contestación, prueba, vista) · normativa revisada el 24-11-2026.

## Qué es

Expediente judicial para nombrar un tercer perito a fin de que emita dictamen pericial que determine la valoración vinculante de los objetos sustraídos en un establecimiento

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito de solicitud de nombramiento de un tercer perito» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito de solicitud de nombramiento de un tercer perito” para mi caso». También puedes invocarla directamente con `/formularios-proceso-civil:escrito-solicitud-nombramiento-tercer-perito-civ-0858`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-proceso-civil:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Proceso civil: demandas, contestaciones, prueba y vista) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] TÍTULO DEL APARTADO (7 veces)
- [ ] CALLE (4 veces)
- [ ] NÚMERO (4 veces)
- [ ] FECHA (3 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] IMPORTE (2 veces)
- [ ] ASEGURADORA
- [ ] DENOMINACIÓN SOCIAL
- [ ] DNI/NIE
- [ ] LO
- [ ] LUGAR
- [ ] MODALIDAD DEL SEGURO
- [ ] PROFESIÓN
- [ ] SEDE

## Normas que cita el formulario

- art. 136 Ley 15/2015
- art. 38 Ley 50/1980
- art. 18 LCS
- art. 38 LCS
- art. 137.2 LJV
- art. 138.2 LJV
- art. 137.1 LJV
- art. 85.1 LOPJ

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

Notas al pie del formulario original:
(1) La exigencia de abogado y procurador para plantear expediente de jurisdicción voluntaria variará, según el art. 3.2 LJV, en función del expediente de que se trate, y la exigencia legal al respecto. En todo caso, aun cuando no sea necesario, las partes que lo deseen podrán actuar asistidas o representadas por Abogado y Procurador, respectivamente. En el supuesto específico del presente escrito, el art. 137.3 LJV no exige esos requisitos para la tramitación del expediente.


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

A LA SECCIÓN DE LO MERCANTIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS], con DNI [DNI/NIE], de profesión [PROFESIÓN], y domicilio en [LOCALIDAD], calle [CALLE], nº [NÚMERO], ante el Tribunal comparezco y como mejor en Derecho proceda, DIGO:

Que por medio del presente escrito, y de conformidad con el art. 136 de la Ley 15/2015, de 2 de julio, de la Jurisdicción Voluntaria (en lo sucesivo, LJV), promuevo expediente en solicitud de nombramiento de tercer perito. Todo ello, en base a los siguientes

Hechos y consideraciones jurídicas:

1.ª [TÍTULO DEL APARTADO])

En fecha [FECHA] concerté un seguro de robo, en su modalidad de [MODALIDAD DEL SEGURO], con la entidad aseguradora [ASEGURADORA] SA, en relación a mi establecimiento comercial abierto al público social en [LO], calle [CALLE], nº [NÚMERO]. Las primas anuales pactadas han sido correctamente abonadas, sin retraso alguno, desde el inicio del contrato hasta la actualidad.

2.ª [TÍTULO DEL APARTADO])

Que la noche del pasado [FECHA] mi establecimiento fue objeto de un robo con fuerza en las cosas, tras forzar personas desconocidas las distintas cerraduras de seguridad instaladas al efecto, por recomendación de la propia entidad aseguradora. El robo fue denunciado ante el Cuerpo Nacional de Seguridad al día siguiente, incoándose el correspondiente atestado policial, que todavía no ha sido objeto de instrucción judicial al no conocerse el autor o presuntos autores del mismo.

3.ª [TÍTULO DEL APARTADO])

Dentro del plazo de cinco días que marca el art. 38 de la Ley 50/1980, de 8 de octubre, de Contrato de Seguro (en lo sucesivo, LCS), se comunicó a la entidad aseguradora la relación de los objetos robados y sus valoraciones, acompañando los correspondientes albaranes y justificantes entregados por los proveedores. Si bien, dentro del plazo legal de 40 días que marca el art. 18 LCS, no se alcanzó un acuerdo sobre el importe de la suma a abonar, procediéndose a nombrar un perito por cada parte. Como asegurado nombré al perito tasador D./Dña. [NOMBRE Y APELLIDOS] con despacho profesional en [LOCALIDAD], calle [CALLE], nº [NÚMERO]; mientras que la entidad aseguradora hizo lo propio con el también perito tasador D./Dña. [NOMBRE Y APELLIDOS] con despacho profesional en [LOCALIDAD], calle [CALLE], nº [NÚMERO].

4.ª [TÍTULO DEL APARTADO])

Tras realizar cada uno de ellos su correspondiente peritación y emitir los preceptivos dictámenes, no se pudo alcanzar un acuerdo a reflejar en acta conjunta conforme a lo dispuesto en el párrafo quinto del mencionado art. 38 LCS. En este sentido, las correspondientes valoraciones se encuentran muy alejadas entre sí, oscilando entre los [IMPORTE] euros calculados por el perito de la aseguradora, y los [IMPORTE] euros calculados por el perito elegido por mí. El desacuerdo es de tal magnitud que se ha extendido también a la posibilidad de designación conjunta de un tercer perito.

5.ª [TÍTULO DEL APARTADO])

En consecuencia, y por remisión del párrafo sexto de dicho precepto legal, se acude al expediente previsto en los arts. 136 y ss. LJV, para lo cual me encuentro legitimado con arreglo a lo dispuesto en el art. 137.2 LJV como asegurado que soy. Tal y como preceptúa el art. 138.2 LJV, procederá la convocatoria de comparecencia ante el Letrado de la Administración de Justicia, a los efectos de buscar un acuerdo o consenso, y, en caso contrario, proceder a su nombramiento conforme a lo que determina el art. 341 la Ley de Enjuiciamiento Civil.

6.ª [TÍTULO DEL APARTADO])

Que es competente la Sección de lo Mercantil del Tribunal de Instancia al que me dirijo conforme al art. 137.1 LJV, en relación con lo dispuesto en el art. 85.1º LOPJ, al encontrarse en su partido judicial mi domicilio, como asegurado y parte del contrato de seguro que soy.

7.ª [TÍTULO DEL APARTADO])

Se acompañan a esta solicitud copia de la póliza de seguro, extracto bancario donde se aprecian los pagos de las correspondientes primas, copia del atestado policial, relación y valoración de los objetos sustraídos enviados a la aseguradora, y dictámenes de los peritos nombrados por cada parte.

Por todo lo expuesto, al amparo de los arts. 136 y ss. LJV y del art. 38 LCS,

SUPLICO AL TRIBUNAL

Que teniendo por presentado este escrito y documentos que lo acompañan y por promovido expediente de jurisdicción voluntaria; y previa convocatoria de comparecencia ante el Letrado de la Administración de Justicia prevista en el art. 138.2 LJV, con citación de la entidad [DENOMINACIÓN SOCIAL] SA, y de quien se estime oportuno, se dicte decreto acordando nombrar un tercer perito a fin de que emita dictamen pericial que determine la valoración vinculante de los objetos sustraídos en el establecimiento de mi propiedad.

Por ser de Justicia que pido en [LUGAR], a [FECHA].

Firma del solicitante
