---
name: demanda-disolucion-sociedad-gananciales-discapacidad-civ-0187
description: "Demanda de disolución de la sociedad de gananciales por discapacidad de un cónyuge con liquidación. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de disolución de la sociedad de gananciales por discapacidad de un cónyuge con liquidación

> Formulario **CIV-0187** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Demanda que presenta el curador con facultades de representación de una persona con discapacidad casada en gananciales para que se declare disuelta la sociedad de gananciales (art. 1393.1.º CC) y se liquide, divida y adjudique el patrimonio común, aportando una propuesta de inventario, avalúo y adjudicación.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de disolución de la sociedad de gananciales por discapacidad de un cónyuge con liquidación» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de disolución de la sociedad de gananciales por discapacidad de un cónyuge con liquidación” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-disolucion-sociedad-gananciales-discapacidad-civ-0187`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (25 veces)
- [ ] Nº (21 veces)
- [ ] NOMBRE Y APELLIDOS DE LA PERSONA CON DISCAPACIDAD (8 veces)
- [ ] NOMBRE Y APELLIDOS DEL CÓNYUGE (6 veces)
- [ ] DOMICILIO (5 veces)
- [ ] IMPORTE EN LETRA (4 veces)
- [ ] NOMBRE Y APELLIDOS DEL CURADOR/A (4 veces)
- [ ] FECHA (3 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] MARCA (2 veces)
- [ ] MATRÍCULA (2 veces)
- [ ] PORCENTAJE (2 veces)
- [ ] SEDE (2 veces)
- [ ] SUPERFICIE (2 veces)
- [ ] AÑO
- [ ] COLEGIO
- [ ] DESCRIBIR Y VALORAR
- [ ] DÍA
- [ ] MES
- [ ] NO EXISTEN / DESCRIBIR
- [ ] NOMBRE Y APELLIDOS DEL ABOGADO/A
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] Nº DE COLEGIADO
- [ ] PISO

## Normas que cita el formulario

- art. 50.1 LEC
- art. 807 LEC
- art. 85.1.º LOPJ
- art. 6.1.1.º LEC
- art. 7.2 LEC
- art. 287.7.º Código Civil
- art. 23 LEC
- art. 5 Ley Orgánica 1/2025
- art. 1393.1.º CC
- art. 806 LEC
- art. 1396 CC
- art. 1397 CC
- art. 1410 CC

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

### Avisos de actualización (3) — se aplican en el texto, nunca se copian en el documento

- Junto a «…MILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.
- Junto a «…ión de la persona con discapacidad, con arreglo al art. 287.7.º del Código Civil»: comprobar el ordinal exacto del art. 287 CC en su redacción vigente

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

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS DEL CURADOR/A], que es representante legal de [ELEGIR: su hermano / su hermana / PARENTESCO] D./Dña. [NOMBRE Y APELLIDOS DE LA PERSONA CON DISCAPACIDAD], como curador/a con facultades de representación, con domicilio en [DOMICILIO], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento n.º [Nº], ante el Tribunal comparezco y, como mejor proceda en Derecho, DIGO:

Que, en la representación que ostento, asistido/a del Letrado/a D./Dña. [NOMBRE Y APELLIDOS DEL ABOGADO/A], colegiado/a n.º [Nº DE COLEGIADO] del Ilustre Colegio de Abogados de [COLEGIO], con despacho abierto en [DOMICILIO], vengo a solicitar la DISOLUCIÓN Y LIQUIDACIÓN DEL RÉGIMEN ECONÓMICO MATRIMONIAL existente entre la persona con discapacidad a quien represento y su cónyuge D./Dña. [NOMBRE Y APELLIDOS DEL CÓNYUGE], con domicilio en [DOMICILIO], con arreglo a los siguientes hechos y fundamentos jurídicos:

HECHOS

PRIMERO.– D./Dña. [NOMBRE Y APELLIDOS DE LA PERSONA CON DISCAPACIDAD] y D./Dña. [NOMBRE Y APELLIDOS DEL CÓNYUGE] contrajeron matrimonio, cuyo régimen económico es el supletorio legal de la sociedad de gananciales. Se acredita este extremo mediante el documento n.º [Nº], consistente en el certificado de matrimonio expedido por el Registro Civil.

SEGUNDO.– D./Dña. [NOMBRE Y APELLIDOS DEL CURADOR/A] es curador/a, con facultades de representación, de [su hermano/a] D./Dña. [NOMBRE Y APELLIDOS DE LA PERSONA CON DISCAPACIDAD], con arreglo al Auto del Tribunal de Instancia n.º [Nº] de [SEDE], de [FECHA], tras expediente de jurisdicción voluntaria n.º [Nº] seguido al efecto sobre provisión de medidas judiciales de apoyo a persona con discapacidad a favor de D./Dña. [NOMBRE Y APELLIDOS DE LA PERSONA CON DISCAPACIDAD]. Se acompaña testimonio de dicho auto como documento n.º [Nº] y acta de aceptación del cargo como documento n.º [Nº].

TERCERO.– La propuesta de inventario de los bienes conyugales y su liquidación es la siguiente:

A) INVENTARIO Y AVALÚO

1.– [DESCRIPCIÓN DEL NEGOCIO O ACTIVO PRINCIPAL, p. ej., librería].

Descripción: local número [Nº], sito en el número [Nº] de la calle [DOMICILIO] de [LOCALIDAD], finca registral número [Nº], de [SUPERFICIE] metros cuadrados construidos, con una cuota de participación en la comunidad de propietarios de [PORCENTAJE] %. El local que se describe tiene señalado como anejo inseparable almacén en semisótano señalado con n.º [Nº].

Título: contrato de compraventa de fecha [FECHA]. Se acompaña como documento n.º [Nº] copia del contrato de compraventa.

Valoración: el valor de compra del local asciende, según el contrato de compraventa, a [IMPORTE] euros. Debe añadirse a esto el stock de mercaderías, que suma [IMPORTE] euros, y el mobiliario y otros enseres, que tienen un valor de [IMPORTE] euros, todo lo cual hace que el valor actual del negocio ascienda a un total de [IMPORTE] euros.

Cargas: las deudas que pesan sobre el negocio en el momento de presentar este escrito son las siguientes:

— Hipoteca que grava el local y almacén de semisótano, mencionada en el contrato de compraventa del mismo, y cuyo importe pendiente de pago es actualmente de [IMPORTE] euros. Se acompaña como documento n.º [Nº] justificante de dicha deuda.

— Deuda de mercadería por un importe total de [IMPORTE] euros, acreditándose con el documento n.º [Nº].

El total del pasivo del negocio es de [IMPORTE] euros.

2.– Automóvil marca [MARCA], matrícula [MATRÍCULA], valorado en [IMPORTE] euros.

3.– Automóvil marca [MARCA], matrícula [MATRÍCULA], valorado en [IMPORTE] euros.

4.– Vivienda sita en el piso [PISO] de la finca número [Nº] de la calle [DOMICILIO] de [LOCALIDAD], con una superficie de [SUPERFICIE] metros cuadrados, finca registral número [Nº], teniendo como cuota de participación en la comunidad de propietarios [PORCENTAJE] %.

Título: contrato de compraventa de fecha [FECHA]. Se acompaña como documento n.º [Nº] copia del contrato de compraventa.

Valoración: el valor de compra de la vivienda asciende, según el contrato de compraventa, a [IMPORTE] euros.

Cargas: [NO EXISTEN / DESCRIBIR].

5.– Derechos y acciones: [DESCRIBIR, p. ej., acciones o participaciones sociales, con su valor].

6.– Ajuar, enseres, mobiliario y equipamiento de la vivienda: [DESCRIBIR Y VALORAR].

Lo anterior supone que la liquidación total es la siguiente:

Suma el activo: [IMPORTE EN LETRA] euros ([IMPORTE] €).

Suma el pasivo: [IMPORTE EN LETRA] euros ([IMPORTE] €).

B) LIQUIDACIÓN Y ADJUDICACIÓN

A cada cónyuge le corresponde la mitad del activo, esto es, [IMPORTE EN LETRA] euros ([IMPORTE] €), y la mitad del pasivo, que son [IMPORTE EN LETRA] euros ([IMPORTE] €).

Se propone la siguiente adjudicación:

1.– A D./Dña. [NOMBRE Y APELLIDOS DE LA PERSONA CON DISCAPACIDAD] se le adjudican los siguientes bienes:

— La vivienda: [IMPORTE] euros.

— Los enseres de la vivienda: [IMPORTE] euros.

Total: [IMPORTE] euros.

2.– A D./Dña. [NOMBRE Y APELLIDOS DEL CÓNYUGE] se le adjudican los siguientes bienes:

— El negocio: [IMPORTE] euros.

— Las acciones o participaciones: [IMPORTE] euros.

— El automóvil 2: [IMPORTE] euros.

— El automóvil 3: [IMPORTE] euros.

Total: [IMPORTE] euros.

— Deudas del negocio: [IMPORTE] euros.

Total adjudicación: [IMPORTE] euros.

D./Dña. [NOMBRE Y APELLIDOS DEL CÓNYUGE] compensará a D./Dña. [NOMBRE Y APELLIDOS DE LA PERSONA CON DISCAPACIDAD] con la cantidad de [IMPORTE] euros, estableciendo así la igualdad en la adjudicación.

Se hace esta propuesta de liquidación ya que el negocio es una actividad que lleva directamente D./Dña. [NOMBRE Y APELLIDOS DEL CÓNYUGE], que asumirá todas las deudas contraídas por el local y negocio. Por otro lado, la vivienda familiar es la que ocupa D./Dña. [NOMBRE Y APELLIDOS DE LA PERSONA CON DISCAPACIDAD].

Se ponen a disposición del Tribunal todos los balances, libros y documentos del negocio.

CUARTO.– Previamente a la interposición de la presente demanda se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial. En este sentido, se acudió a [INDICAR EL MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS AL QUE LAS PARTES SE HAN SOMETIDO, en cumplimiento del requisito de procedibilidad que exige la LO 1/2025], no habiendo sido posible alcanzar un acuerdo definitivo. Se acompaña como documento n.º [Nº] [ESPECIFICAR EL DOCUMENTO QUE ACREDITA QUE SE HA ACUDIDO A UN MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS].

FUNDAMENTOS DE DERECHO

I.– COMPETENCIA.

Es competente el Tribunal al que me dirijo, por aplicación del art. 50.1 LEC, dado que pertenece a su circunscripción el lugar de domicilio del demandado. A su vez, el art. 807 LEC, en relación con lo dispuesto en el art. 85.1.º LOPJ, atribuye la competencia por conexión para conocer del procedimiento de liquidación al Tribunal de Instancia ante el que se sigan las actuaciones sobre disolución del régimen económico matrimonial por alguna de las causas previstas en la legislación civil.

II.– CAPACIDAD Y LEGITIMACIÓN.

D./Dña. [NOMBRE Y APELLIDOS DE LA PERSONA CON DISCAPACIDAD], mayor de edad, está sujeto/a a la curatela de [su hermano/a] D./Dña. [NOMBRE Y APELLIDOS DEL CURADOR/A], de modo que su capacidad para ser parte (art. 6.1.1.º LEC) se cohonesta con una capacidad para comparecer en juicio mediante la representación legal del curador (art. 7.2 LEC), habiéndose obtenido la previa autorización judicial para interponer la demanda por parte del curador en representación de la persona con discapacidad, con arreglo al art. 287.7.º del Código Civil (se adjunta como documento n.º [Nº] la resolución del expediente n.º [Nº] del procedimiento sobre provisión de medidas judiciales de apoyo a persona con discapacidad a favor de D./Dña. [NOMBRE Y APELLIDOS], n.º [Nº] del Tribunal de Instancia n.º [Nº]).

La demandada, persona física mayor de edad, se presume capaz material y procesalmente, por naturaleza (arts. 6.1.1.º y 7.1 LEC).

En cualquier caso, se requiere la capacidad de postulación, mediante la representación técnica de procurador de los tribunales y la dirección de abogado en ejercicio (arts. 23 y 31 LEC).

Por lo que respecta a la legitimación activa y pasiva, las mismas se desprenden como acreditadas: la primera, en virtud de ser D./Dña. [NOMBRE Y APELLIDOS DEL CURADOR/A] curador/a legal con facultades de representación en el momento de ser presentada la demanda; y la segunda, por cuanto D./Dña. [NOMBRE Y APELLIDOS DEL CÓNYUGE] es copartícipe de la sociedad de gananciales junto con la persona con discapacidad.

III.– CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda cumple con el requisito de procedibilidad exigido por el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

IV.– TRÁMITE.

Disolución de la sociedad de gananciales. Prevé el art. 1393.1.º CC, en sede de regulación del régimen económico-matrimonial, la posibilidad de conclusión de la sociedad de gananciales por decisión judicial, fuera del proceso matrimonial, al disponer que «también concluirá por decisión judicial la sociedad de gananciales, a petición de uno de los cónyuges, en alguno de los casos siguientes: 1.º Si respecto del otro cónyuge se hubieren dispuesto judicialmente medidas de apoyo que impliquen facultades de representación plena en la esfera patrimonial, si hubiere sido declarado ausente o en concurso, o condenado por abandono de familia. Para que la autoridad judicial acuerde la disolución bastará que el cónyuge que la pidiere presente la correspondiente resolución judicial».

Liquidación, división y adjudicación del patrimonio ganancial. Dispone el art. 806 LEC que «la liquidación de cualquier régimen económico matrimonial que, por capitulaciones matrimoniales o por disposición legal, determine la existencia de una masa común de bienes y derechos sujeta a determinadas cargas y obligaciones se llevará a cabo, en defecto de acuerdo entre los cónyuges, con arreglo a lo dispuesto en el presente capítulo y a las normas civiles que resulten aplicables»; señalando el art. 1396 CC que «disuelta la sociedad se procederá a su liquidación, que comenzará por un inventario del activo y pasivo de la sociedad», que se conformarán de modo imperativo en el modo dispuesto en los arts. 1397 y 1398 CC, rigiendo en todo lo no dispuesto las normas de las particiones de las herencias a que se refiere el art. 1410 CC.

Por lo expuesto,

SUPLICO AL TRIBUNAL

Que, teniendo por presentado este escrito, se sirva admitirlo, junto con sus documentos y justificantes de entrega de copias simples a la contraria, declare judicialmente, por causa de haberse dispuesto judicialmente respecto del otro cónyuge medidas de apoyo que implican facultades de representación plena en la esfera patrimonial, la disolución del régimen económico-matrimonial de sociedad de gananciales que regía el matrimonio formado por D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS]; teniendo por presentada propuesta de inventario de los bienes gananciales y su liquidación y división, citando a las partes, con traslado a la parte contraria de la propuesta que se contiene en el cuerpo de este escrito, a fin de que se alcance un acuerdo o, en otro caso, se ventile la oposición por los trámites legales, con advertencia al demandado de que, si no comparece, se le tendrá por conforme con la indicada propuesta.

Es justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Abogado/a Firma del Procurador/a
