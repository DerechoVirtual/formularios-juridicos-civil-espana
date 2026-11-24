---
name: solicitud-autorizacion-judicial-vender-bienes-hijos-civ-0189
description: "Solicitud de autorización judicial para vender bienes de hijos menores (Derecho civil catalán). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud de autorización judicial para vender bienes de hijos menores (Derecho civil catalán)

> Formulario **CIV-0189** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Solicitud de expediente de jurisdicción voluntaria para obtener la autorización judicial necesaria para vender bienes inmuebles de hijos menores sujetos a la potestad del progenitor, conforme al Derecho civil de Cataluña (arts. 236-27 y 236-28 del Código Civil de Cataluña) y a los arts. 61 y siguientes de la Ley de Jurisdicción Voluntaria. Hay que acreditar la necesidad o utilidad de la venta para los menores y el destino del precio.

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud de autorización judicial para vender bienes de hijos menores (Derecho civil catalán)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud de autorización judicial para vender bienes de hijos menores (Derecho civil catalán)” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:solicitud-autorizacion-judicial-vender-bienes-hijos-civ-0189`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (10 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] DOMICILIO (3 veces)
- [ ] NOMBRE Y APELLIDOS DE LOS MENORES (3 veces)
- [ ] SEDE (3 veces)
- [ ] AÑO (2 veces)
- [ ] EDAD (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL PERITO (2 veces)
- [ ] DOMICILIO DE LOS INMUEBLES
- [ ] DÍA
- [ ] EDADES
- [ ] ENTIDAD BANCARIA
- [ ] FECHA
- [ ] IMPORTE
- [ ] MES
- [ ] NOMBRE DEL NOTARIO
- [ ] NOMBRE Y APELLIDOS
- [ ] NOMBRE Y APELLIDOS DEL COMPRADOR
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] NOMBRE Y APELLIDOS DEL PROGENITOR
- [ ] NOMBRE Y APELLIDOS DEL PROGENITOR FALLECIDO
- [ ] NOMBRE Y APELLIDOS DEL TESTIGO
- [ ] Nº DE FINCA
- [ ] PROMOTORA
- [ ] SUPERFICIE
- [ ] TOMO
- [ ] ZONA

## Normas que cita el formulario

- art. 236 Código Civil

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

- Junto a «…MILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.

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

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, actuando en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS DEL PROGENITOR], según acredito mediante apoderamiento «apud acta» otorgado ante el Letrado/a de la Administración de Justicia de la Oficina judicial de [SEDE], ante el Tribunal comparezco y, como mejor proceda en Derecho, DIGO:

Que, al amparo de lo dispuesto en los artículos 236-27 y 236-28 del Código Civil de Cataluña, en relación con los arts. 61 y siguientes de la Ley de Jurisdicción Voluntaria, mediante el presente escrito deduzco expediente de jurisdicción voluntaria en SOLICITUD DE AUTORIZACIÓN DE VENTA DE BIENES DE MENORES, concretamente de los inmuebles sitos en [DOMICILIO DE LOS INMUEBLES], propiedad de los hijos de mi representado, [NOMBRE Y APELLIDOS DE LOS MENORES], menores de edad, de [EDADES] años de edad, respectivamente, en atención a los siguientes

HECHOS

PRIMERO.– Mi representado solicita la autorización judicial de la venta de [Nº] viviendas desocupadas que pertenecen a sus hijos menores, actuando en la representación legal que tiene conferida y en interés de sus hijos [NOMBRE Y APELLIDOS DE LOS MENORES], que en la actualidad tienen [EDAD] y [EDAD] años de edad, respectivamente.

Mi representado es el padre/la madre de los menores, ostentando la potestad parental y la condición de único representante legal de los mismos, al haber fallecido [su madre / su padre] D./Dña. [NOMBRE Y APELLIDOS DEL PROGENITOR FALLECIDO] en el año [AÑO] (a efectos acreditativos acompaño libro de familia, certificados de nacimiento de los hijos, de matrimonio de los padres y certificado literal de defunción como documentos números [Nº]).

SEGUNDO.– Los hijos de mi representado son titulares, en proindiviso, de las siguientes fincas:

«Urbana sita en [DOMICILIO], de superficie [SUPERFICIE]».

Está inscrita en el Registro de la Propiedad número [Nº] de [LOCALIDAD], con el número [Nº DE FINCA], Tomo [TOMO] (se acompaña certificación del Registro de la Propiedad como documento número [Nº]).

Dichas viviendas fueron adquiridas «mortis causa» por los menores por testamento otorgado por [su madre / su padre] y causante D./Dña. [NOMBRE Y APELLIDOS], según consta en la escritura de partición de herencia de fecha [FECHA], otorgada ante el Notario de [LOCALIDAD] D. [NOMBRE DEL NOTARIO], que se acompaña por copia auténtica como documento número [Nº].

TERCERO.– Las viviendas pretenden enajenarse por el precio de [IMPORTE] euros cada una al comprador D./Dña. [NOMBRE Y APELLIDOS DEL COMPRADOR], según se acredita en el compromiso de compraventa condicionado a la obtención de la autorización judicial ahora solicitada, que se acompaña como documento número [Nº].

La enajenación que se pretende resulta ventajosa para los menores, puesto que el precio acordado es [ELEGIR: muy superior al valor de mercado / ajustado al valor de mercado], tal como se acredita por el dictamen pericial emitido por D./Dña. [NOMBRE Y APELLIDOS DEL PERITO] sobre valoración del precio de mercado de las citadas viviendas, que se acompaña como documento número [Nº].

CUARTO.– La venta cuya autorización se pretende es necesaria y útil para los menores por cuanto se trata de la venta de dos viviendas desocupadas, que difícilmente pueden ser arrendadas a terceras personas, de una considerable antigüedad y de una superficie muy reducida, siendo que los menores están en condiciones actualmente de acceder a la adquisición de dos viviendas en la zona de [ZONA], de nueva construcción y de una superficie considerablemente superior, con lo cual pueden quedar cubiertas incluso sus futuras necesidades de vivienda (acompaño como documento [Nº] oferta de venta recibida de la promotora [PROMOTORA] en relación con dichas viviendas).

Como se puede comprobar, el precio ofertado por los inmuebles que se pretenden adquirir es muy superior al de la enajenación de las viviendas de las cuales son titulares, si bien mi representado está dispuesto a sufragar la diferencia entre el precio de ambos inmuebles en interés de sus hijos, habiendo gestionado la concesión de un préstamo personal por la diferencia de precio, según se acredita por certificación de la entidad bancaria [ENTIDAD BANCARIA], que se acompaña como documento [Nº].

Como queda expuesto, la necesidad y utilidad de la enajenación de los inmuebles deriva de que su importe íntegro será destinado a la compra de una vivienda para cada uno de los hijos, de condiciones mucho más óptimas, comprometiéndose mi representado a sufragar la diferencia, por lo que se cumplen los requisitos establecidos en el artículo 236-28 del Código Civil de Cataluña, por realizarse en interés de los menores y en su beneficio.

A los anteriores hechos son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

COMPETENCIA

Son competentes las secciones civiles de los tribunales de instancia de [SEDE], por ser el lugar del domicilio de los menores, conforme a lo dispuesto en el art. 62.1 de la Ley de Jurisdicción Voluntaria.

PROCEDIMIENTO

Teniendo en cuenta que se solicita la autorización para la enajenación de bienes de menores, debe seguirse el procedimiento de jurisdicción voluntaria regulado en los artículos 61 y siguientes de la Ley de Jurisdicción Voluntaria.

LEGITIMACIÓN, CUANTÍA Y POSTULACIÓN

Mi representado está legitimado al ostentar la potestad parental sobre los menores, conforme a lo establecido en los artículos 236-27 y 236-28 del Código Civil de Cataluña, compareciendo representado por Procurador y asistido por Abogado según lo dispuesto en el art. 62.3 de la Ley de Jurisdicción Voluntaria, al exceder el valor de la venta del importe de 6.000 euros, tal como se acredita por el dictamen pericial acompañado como documento [Nº].

FUNDAMENTOS DE FONDO

Los arts. 236-27 y 236-28 del Código Civil de Cataluña regulan la necesidad y los requisitos de la autorización judicial, justificándose las circunstancias y características fundamentales de la enajenación que se pretende realizar, así como la utilidad de la misma para los menores.

Por lo anterior,

SUPLICO AL TRIBUNAL que tenga por presentada esta solicitud de autorización para la enajenación de las viviendas sitas en la calle [DOMICILIO] de la localidad de [LOCALIDAD], descritas en el hecho segundo, propiedad de los hijos menores de edad de mi representado, [NOMBRE Y APELLIDOS DE LOS MENORES], y, tras los trámites legales, practicando la información testifical que dejo ofrecida en el otrosí y previa audiencia del Ministerio Fiscal, dicte auto por el que conceda la autorización para enajenar los inmuebles antes expresados.

OTROSÍ PRIMERO DIGO: Que, a los efectos establecidos en el art. 64 de la Ley de Jurisdicción Voluntaria, solicito la comparecencia del perito D./Dña. [NOMBRE Y APELLIDOS DEL PERITO], autor del dictamen pericial acompañado, así como de los menores y de los siguientes testigos que, por razón de su conocimiento de los hechos, pueden aseverar la necesidad y utilidad de la venta:

— D./Dña. [NOMBRE Y APELLIDOS DEL TESTIGO], con domicilio en [DOMICILIO].

SUPLICO AL TRIBUNAL: Tenga por propuestas a las personas indicadas, admitiendo la práctica de la prueba ofrecida, comprometiéndose esta parte a que comparezcan en el día y hora que se señale.

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Procurador/a o del interesado y del Abogado/a

[OPCIONAL — si ha lugar]

Firma del menor (en caso de que el menor sea mayor de doce años)
