---
name: solicitud-liquidacion-sociedad-gananciales-propuesta-civ-0312
description: "Solicitud de liquidación de la sociedad de gananciales con propuesta de liquidación. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud de liquidación de la sociedad de gananciales con propuesta de liquidación

> Formulario **CIV-0312** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Escrito solicitando la liquidación del régimen de gananciales al haberse dictado sentencia de separación en la que se acordaba el efecto legal de la disolución del régimen de gananciales, con propuesta de liquidación.

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud de liquidación de la sociedad de gananciales con propuesta de liquidación» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud de liquidación de la sociedad de gananciales con propuesta de liquidación” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:solicitud-liquidacion-sociedad-gananciales-propuesta-civ-0312`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (23 veces)
- [ ] NOMBRE Y APELLIDOS (9 veces)
- [ ] FECHA (6 veces)
- [ ] Nº DE DOCUMENTO (5 veces)
- [ ] NÚMERO (5 veces)
- [ ] Nº (3 veces)
- [ ] CUOTA DE PARTICIPACIÓN (2 veces)
- [ ] MARCA/MODELO (2 veces)
- [ ] MATRÍCULA (2 veces)
- [ ] NOMBRE DEL VENDEDOR (2 veces)
- [ ] AÑO
- [ ] CALLE
- [ ] DESCRIPCIÓN DE DERECHOS Y ACCIONES
- [ ] IMPORTE EN CIFRA
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] PISO
- [ ] SEDE

## Normas que cita el formulario

- art. 807 LEC
- art. 809 LEC
- art. 5 Ley Orgánica 1/2025
- art. 810.2 LEC
- art. 810.4 LEC

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

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, que actúa en nombre y representación de Dña. [NOMBRE Y APELLIDOS], según consta debidamente acreditado en los autos de separación contenciosa número [NÚMERO]/[AÑO], ante el Tribunal comparezco y, como mejor proceda en Derecho, DIGO:

Que en la representación que ostento, vengo a solicitar la LIQUIDACIÓN DEL RÉGIMEN ECONÓMICO MATRIMONIAL existente entre los cónyuges, frente a D. [NOMBRE Y APELLIDOS], demandado en los autos principales, con arreglo a los siguientes hechos y fundamentos jurídicos:

HECHOS

PRIMERO.- Mi mandante y D. [NOMBRE Y APELLIDOS], formaban matrimonio cuyo régimen económico era el supletorio legal de la sociedad de gananciales.

SEGUNDO.- Que con fecha [FECHA] se dictó sentencia de separación de los cónyuges D. y Dña. [NOMBRE Y APELLIDOS], en la que entre otros pronunciamientos, acordaba el efecto legal de la disolución del régimen de gananciales, sentencia que es firme.

TERCERO.- La liquidación que se propone es la siguiente:

A) INVENTARIO Y AVALÚO (Acta de [FECHA])
1.- Librería
Descripción: Local número [NÚMERO] sito en [LOCALIDAD], finca registral número [NÚMERO], de [Nº] metros cuadrados construidos, con una cuota de participación en la comunidad de propietarios de [CUOTA DE PARTICIPACIÓN]. El local que se describe tiene señalado como anejo inseparable, almacén en semisótano señalado con n.º [Nº]
Título: Contrato de compraventa a [NOMBRE DEL VENDEDOR] de fecha [FECHA]. Se acompaña como documento número [Nº DE DOCUMENTO] copia del contrato de compraventa.
Valoración: El valor de compra del local asciende, según el contrato de compraventa, a [IMPORTE] euros. Debe añadirse a esto el stock de mercaderías que suman [IMPORTE] euros y el mobiliario y otros enseres, que tienen un valor de [IMPORTE] euros. Todo lo cual hace que el valor actual de la Librería asciende a un total de [IMPORTE] euros.

Cargas: las deudas que pesan sobre la Librería en el momento de presentar este escrito son los siguientes:

- Hipoteca que grava el local y almacén de semisótano, mencionada en el contrato de compraventa del mismo, y cuyo importe que resta por pagar es actualmente de [IMPORTE] euros. Se acompaña como documento número [Nº DE DOCUMENTO] justificante de dicha deuda.
- Deuda de mercadería por un importe total de [IMPORTE] euros, acreditándose con el documento número [Nº DE DOCUMENTO].
El total del pasivo de la Librería es de [IMPORTE] euros.
2.- Automóvil marca [MARCA/MODELO], matrícula [MATRÍCULA], valorado en [IMPORTE] euros.
3.- Automóvil marca [MARCA/MODELO], matrícula [MATRÍCULA], valorado en [IMPORTE] euros.
4.- Vivienda sita en el piso [PISO] de la finca número [NÚMERO] de la calle [CALLE], con una superficie de [Nº] metros cuadrados, finca registral número [NÚMERO], teniendo como cuota de participación en la comunidad de propietarios [CUOTA DE PARTICIPACIÓN].
Título: el contrato de compraventa a [NOMBRE DEL VENDEDOR] de fecha [FECHA] Se acompaña como documento número [Nº DE DOCUMENTO] copia del contrato de compraventa.
Valoración: el valor de compra de la vivienda asciende, según el contrato de compraventa, a [IMPORTE] euros.

Cargas: no existen.

5.- Derechos y acciones [DESCRIPCIÓN DE DERECHOS Y ACCIONES]
6.- Ajuar, enseres, mobiliario y equipamiento de la vivienda ()

Lo anterior supone que la liquidación total es la siguiente:

Suma el activo: [IMPORTE] euros ( €)
Suma el pasivo: [IMPORTE] euros ( €)
B) LIQUIDACIÓN Y ADJUDICACIÓN
A cada cónyuge le corresponde la mitad del activo, esto es, () euros ( €), y la mitad del pasivo, que son [IMPORTE] euros ( € [IMPORTE EN CIFRA]).

Se propone la siguiente adjudicación:

1.- A D. se le adjudican los siguientes bienes:
- El automóvil 2 [IMPORTE] euros
- Las acciones [IMPORTE] euros
Total [IMPORTE] euros
2.- A Dña. se le adjudican los siguientes bienes:
- La vivienda [IMPORTE] euros
- La librería [IMPORTE] euros
- El automóvil 3. euros
- Los enseres de la vivienda [IMPORTE] euros
Total [IMPORTE] euros
- Deudas del negocio [IMPORTE] euros
Total adjudicación [IMPORTE] euros
Dña. compensará a D. [NOMBRE Y APELLIDOS] con la cantidad de [IMPORTE] euros, estableciendo así la igualdad en la adjudicación.
Se hace esta propuesta de liquidación ya que la librería es un negocio que lleva directamente Dña. [NOMBRE Y APELLIDOS], y que aporta unos ingresos mínimos a mi representada, que asumirá todas las deudas que tiene contraído el local y negocio. Por otro lado, la vivienda familiar es la que ocupa Dña. [NOMBRE Y APELLIDOS] con los hijos habidos del matrimonio, todos ellos menores de edad, y cuyo uso y disfrute exclusivo le ha atribuido la sentencia firme

Se ponen a disposición del Tribunal todos los balances, libros y documentos de la Librería.

CUARTO.- Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento nº [Nº DE DOCUMENTO]

FUNDAMENTOS DE DERECHO

I.- COMPETENCIA.

Se atribuye legalmente a la Sección Civil del Tribunal de Instancia que hubiera conocido del proceso de separación que determina la disolución de régimen económico matrimonial (art. 807 LEC).

II.- INVENTARIO.

Se solicitó como medida provisional con la demanda de separación y se acordó por auto de fecha [FECHA], realizándose de común acuerdo en comparecencia ante la Letrado de la Administración de Justicia, convocada con arreglo al art. 809 LEC.

III.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

IV.- TRÁMITE.

Se solicita una vez firme la resolución definitiva del proceso de separación, acompañando propuesta de liquidación, y de división del remanente, en que se expresan los reintegros entre partes y se forman los lotes con atención de las preferencias del Derecho civil (art. 810.2 LEC), siendo el régimen sustantivo el de arts. 1.392 a 1.410 CC.

Deberá convocarse a ambas partes para ante la Sra. Letrado de la Administración de Justicia, con admonición al adverso de que su injustificada incomparecencia se considerará conformidad con lo que se propone (art. 810.4 LEC).

Por lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito, se sirva admitirlo, y tener por solicitada la liquidación de la sociedad de gananciales del matrimonio formado por D. y Dña. [NOMBRE Y APELLIDOS], acompañándose propuesta de liquidación y división, y se inicie el procedimiento, citando a las partes, con traslado a la parte contraria de la propuesta de liquidación y adjudicación que se contiene en el cuerpo de este escrito, a fin de que se alcance un acuerdo, o en otro caso, se designe contador, y si fuera menester, peritos, con advertencia al demandado de que si no comparece se le tendrá por conforme con la indicada propuesta.

Es justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a

========================================================================
