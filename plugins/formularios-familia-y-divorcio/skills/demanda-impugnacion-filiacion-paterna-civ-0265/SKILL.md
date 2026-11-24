---
name: demanda-impugnacion-filiacion-paterna-civ-0265
description: "Demanda de impugnación de la filiación paterna. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de impugnación de la filiación paterna

> Formulario **CIV-0265** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de impugnación de la filiación paterna» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de impugnación de la filiación paterna” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-impugnacion-filiacion-paterna-civ-0265`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (13 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] CALLE (2 veces)
- [ ] Nº (2 veces)
- [ ] PISO (2 veces)
- [ ] PUERTA (2 veces)
- [ ] EDAD
- [ ] LUGAR Y FECHA
- [ ] Nº DE DOCUMENTO
- [ ] SEDE

## Normas que cita el formulario

- art. 50 LEC
- art. 753 LEC
- art. 405 LEC
- art. 752.1 LEC
- art. 767.1 LEC
- art. 5.2 Ley Orgánica 1/2025
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

- Junto a «…NCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE] Q.P.T.R.C.»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
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

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE] Q.P.T.R.C.

Don [NOMBRE Y APELLIDOS], Procurador de los Tribunales, actuando en nombre y representación que ostento de Don [NOMBRE Y APELLIDOS], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], y bajo la dirección letrada de Don [NOMBRE Y APELLIDOS], ante la Sección Civil del Tribunal de Instancia que por turno de reparto corresponda comparezco y, como mejor proceda en Derecho, DIGO:

Que a través del presente escrito, y en virtud de la representación conferida, interpongo demanda en juicio declarativo especial por la que ejercito acción de IMPUGNACIÓN DE FILIACIÓN PATERNA/MATERNA, en contra de Don [NOMBRE Y APELLIDOS], de [EDAD] de edad, vecino de la localidad de [LOCALIDAD], con domicilio en calle [CALLE], núm. [Nº], piso [PISO], puerta [PUERTA]; y de Doña [NOMBRE Y APELLIDOS], vecina de la localidad de [LOCALIDAD], con domicilio en calle [CALLE], núm. [Nº], piso [PISO], puerta [PUERTA]; la cual baso en los siguientes

HECHOS

PRIMERO.- Que si bien es cierto que en el Registro Civil de [LOCALIDAD] figura mi mandante como hijo natural de Don [NOMBRE Y APELLIDOS], tal como acredito con certificación literal del citado registro que se acompaña como documento núm. uno, no es menos cierto que la mencionada inscripción no se corresponde con la verdad material de los hechos. Fue como consecuencia de la declaración de la abuela materna del demandante, que realizó a través de su testamento, que acompaño como documento núm. dos, cuando se tuvo conocimiento sobre la falsedad de la paternidad inscrita en el Registro Civil.

A raíz de este evento fue cuando el actor recordó un antiguo suceso, relacionado con una donación de sangre en la que no existía compatibilidad con su supuesto padre, pero que su carencia de conocimiento impidió asociar a la falsedad de la paternidad.

Pero para más abundamiento indicar que mi representado ha descubierto que quien creía era su padre natural, no convivió con su madre en fechas anteriores al parto, pues ambos demandados ni tan siquiera se conocían. Es más, durante quince meses después al nacimiento el demandado se encontraba fuera de España, en concreto en Alemania, trabajando en una empresa del sector automovilístico.

SEGUNDO.- Que cuando mi principal tuvo noticia, a través del citado testamento, fue a hablar con quien creía que era su progenitor, quien acabó reconociendo los hechos, pese a sus iniciales reticencias.

Declaraciones de varios testigos, realizadas ante notario, ofrecen prueba de haber oído a la madre de mi mandante comentar en más de una ocasión que el ahora demandado no era el padre biológico de aquél. Asimismo, se aportan originales de cartas amorosas, que acompaño como documento núm. tres, enviadas por un tercero ajeno a la causa, que revelan una más que razonable probabilidad de unión carnal de la madre de mi principal con el mismo.

TERCERO.- Que como prueba de las anteriores manifestaciones, acompañamos los documentos precitados, solicitando la prueba testifical de las personas que a continuación pasamos a enumerar que constatarán la señalada falta de convivencia, así como la confesión del mismo demandado y, en su caso, la prueba biológica pertinente. A los efectos de audiencia, se relacionan a continuación las personas aludidas y sus domicilios: Don [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], Doña [NOMBRE Y APELLIDOS], con domicilio en

Que en relación con las fechas de estancia en Alemania, y para el caso que el demandado no reconozca los hechos a través de su confesión, podrían reclamársele los documentos acreditativos de su trabajo en el extranjero.

Fundamentos de derecho

[ELEGIR UNA OPCIÓN: Legitimación matrimonial / Si se carece de la posesión de estado / Si hubiera posesión de estado / — y además elegir: Legitimación extramatrimonial / Si se carece de la posesión de estado / Si hubiera posesión de estado]

Las acciones ejercidas sobre filiación hacen competente objetivo al Tribunal de instancia, según el artículo 85.1º de la Ley Orgánica del Poder Judicial y el artículo 45 de la Ley de Enjuiciamiento Civil. La competencia territorial, por su parte, se atribuye aplicando el fuero general de las personas físicas, señalado en los apartados primero y segundo del artículo 50 de la LEC, que como regla general establece el domicilio del demandado.

En lo que hace referencia al procedimiento es de aplicación el artículo 753 de la LEC, que establece el cauce procesal del juicio verbal, si bien bajo la exigencia de una contestación a la demanda regulada en el artículo 405 de la LEC, y permitiendo que los hechos que llevarán a la decisión judicial sean introducidos en el proceso en cualquier momento y de manera distinta a la habitual, según el artículo 752.1 de la LEC, siempre que se lleguen a debatir en contradicción. Se añaden las especialidades del artículo 767.1 de la LEC, precepto que exige presentación de un principio de prueba por escrito de los hechos en que se funde la demanda, cosa que ha hecho mi representada.

La presente demanda no está sujeta al previo intento de resolución de controversias en vía no jurisdiccional por tratarse de proceso excluido del requisito de procedibilidad de acuerdo con el art. 5.2 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

Sin perjuicio de acumular la pretensión de rectificación del Registro Civil como consecuencia de la pretensión principal, se alega que no existe sentencia judicial firme que haya declarado una filiación contraria.

En cuanto a las costas es de aplicación artículo 394 de la LEC.

Demás normas concordantes y de aplicación: Iura novit Curia.

Por lo expuesto,

SOLICITO AL TRIBUNAL: Que tenga por presentado este escrito con los documentos acompañados y sus copias, admita todo ello; y por promovido por el Procurador que suscribe, con quien se entiendan las sucesivas diligencias, en nombre y representación de Don [NOMBRE Y APELLIDOS], con devolución de la escritura de poderes una vez quede testimonio en autos, JUICIO ESPECIAL DE IMPUGNACIÓN DE FILIACIÓN PATERNA/MATERNA contra Don [NOMBRE Y APELLIDOS] y Doña [NOMBRE Y APELLIDOS]; y que previa práctica de la prueba presentada, se dicte sentencia que declare que Don/Doña [NOMBRE Y APELLIDOS] no es el padre/madre natural de Don [NOMBRE Y APELLIDOS], a fin de que se suprima el apellido paterno/materno de este último, que se halla inscrito en el Registro Civil de [LOCALIDAD], cancelando los asientos que sean precisos, tanto del anterior como de cualquier otro Registro público, y con la imposición de costas al demandado que se hubiere opuesto, con expresa declaración de temeridad y mala fe.

Es Justicia que insto en [LUGAR Y FECHA].

Firmas de Letrado y Procurador.

========================================================================
