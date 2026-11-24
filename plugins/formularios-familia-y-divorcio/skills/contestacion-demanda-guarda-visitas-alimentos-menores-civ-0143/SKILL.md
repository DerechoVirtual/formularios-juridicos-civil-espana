---
name: contestacion-demanda-guarda-visitas-alimentos-menores-civ-0143
description: "Contestación a la demanda de guarda, visitas y alimentos de menores presentada por un progenitor. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contestación a la demanda de guarda, visitas y alimentos de menores presentada por un progenitor

> Formulario **CIV-0143** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Contestación a la demanda sobre guarda y custodia, régimen de visitas y pensión de alimentos reclamados por un progenitor contra el otro en nombre de hijos menores

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contestación a la demanda de guarda, visitas y alimentos de menores presentada por un progenitor» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contestación a la demanda de guarda, visitas y alimentos de menores presentada por un progenitor” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:contestacion-demanda-guarda-visitas-alimentos-menores-civ-0143`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (9 veces)
- [ ] IMPORTE (6 veces)
- [ ] NOMBRE DEL MENOR (2 veces)
- [ ] Nº (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] CALLE
- [ ] COLEGIO
- [ ] FECHA
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] Nº DE DOCUMENTO

## Normas que cita el formulario

- art. 92 CC
- art. 94 CC
- art. 93 CC
- art. 142 CC
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

AL TRIBUNAL

D./Dña. [NOMBRE Y APELLIDOS], Procurador de los Tribunales, que actúa en nombre y representación de D. [NOMBRE Y APELLIDOS], como acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], bajo la dirección del Letrado/a D./Dña. [NOMBRE Y APELLIDOS], colegiada n.º [NÚMERO] del Iltre. Colegio de Abogados de [COLEGIO], con despacho abierto en [LOCALIDAD], calle [CALLE], n.º [NÚMERO], ante el Tribunal comparezco y como mejor proceda en Derecho, DIGO:

Que, en la representación que ostento y dentro del plazo legal, vengo a formular, en virtud de lo dispuesto en los artículos 748.4.º y 753 de la Ley de Enjuiciamiento Civil, CONTESTACIÓN A LA DEMANDA SOBRE GUARDA Y CUSTODIA, RÉGIMEN DE VISITAS Y PENSIÓN DE ALIMENTOS para el menor [NOMBRE DEL MENOR], interpuesta por Dña. [NOMBRE Y APELLIDOS] frente a mi mandante, en base a los siguientes,

HECHOS

PRIMERO.- Nada que oponer a lo relatado en el antecedente fáctico primero de la demanda en cuanto son ciertos y notorios los datos consignados respecto al tiempo de convivencia, domicilio de la pareja durante la relación sentimental y nacimiento del hijo común.

SEGUNDO.- Incierta la versión del correlativo, en cuanto a la exposición de la situación económica de ambos progenitores. Lo cierto es que la Sra [NOMBRE Y APELLIDOS] trabaja como funcionaria para la Administración de Justicia con un salario mensual de [IMPORTE] euros, mientras que a fecha de hoy mi principal se encuentra en situación de desempleo, teniendo reconocida una prestación de [IMPORTE] euros mensuales, sin percibir ningún otro ingreso.

Para la acreditación de ambos extremos se adjuntan, respectivamente, copia de la última declaración de IRPF de Dña. [NOMBRE Y APELLIDOS] que ha tenido en su poder mi mandante como documento n.º 1; y cartilla de desempleo con certificación de haberes de mi representado como documento n.º 2.

En virtud de todo ello interesa a mi principal que se fije como contribución de alimentos a su cargo la cantidad de [IMPORTE] euros mensuales, por ser esta cantidad proporcional a los ingreso de mi mandante así como a las necesidades del hijo y al caudal y medios económicos de la madre.

TERCERO.- No se acepta el correlativo de la demanda, en cuanto que mi principal solicita le sea atribuido un régimen de visitas lo más amplio posible, puesto que siendo fundamental la protección del interés del menor en virtud del principio del favor filii entendemos que es un derecho del hijo, no sólo del padre, el mantener un contacto intenso y continuado con su progenitor. Por ello, teniendo en cuenta que el menor cuenta tan sólo con [Nº] años de edad, es primordial fomentar al máximo la relación entre padres e hijos en aras al correcto desarrollo de los aspectos afectivos y emocionales del niño en una etapa tan decisiva para su formación.

En virtud de todo ello se propone un régimen de visitas a favor del padre consistente en fines de semana alternos desde los sábados a las 10 horas hasta el domingo a las 21:00 horas, así como la mitad de las vacaciones de Navidad, Semana Santa y verano, correspondiendo elegir, en caso de discrepancia entre los padres, a la madre los años pares y el padre los impares.

FUNDAMENTOS DE DERECHO

I a VI.-

Conforme con los correlativos fundamentos jurídicos del escrito de demanda sobre capacidad, representación, legitimación, jurisdicción, competencia, procedimiento e intervención del Ministerio Fiscal.

VII.- FONDO DEL ASUNTO.

El favor filii ha de inspirar la adopción de medidas derivadas de la extinción de las uniones de hecho. Así lo exige el art. 39.2 CE que se refiere a la protección integral de los hijos, sin distinguir si éstos son matrimoniales o extramatrimoniales, y la propia regulación legal de toda esta materia para el caso de que los progenitores estén unidos por vínculo matrimonial (arts. 90, 91, 92, 93, 94, 96 y 103 CCiv), preceptos que resultan aplicables, por razón de identidad, a la extinción de las uniones more uxorio; y ello ocurre con especial intensidad cuando las medidas a acordar son de las que, como la custodia o el régimen de visitas, afectan de modo directo a las relaciones de los menores con sus progenitores, ya que son éstas las que van a permitir la creación de lazos de afectividad que contribuirán, de modo decisivo, a la configuración del carácter y personalidad del menor.

En cuanto a la atribución de la guarda y custodia, no hay cuestión sobre que la guarda y custodia de los hijos menores se reserve para la madre, de conformidad con el art. 92 CCiv, ya que, por un lado, el padre no lo solicita y, por otro lado, el menor siempre ha estado y actualmente está también con la madre, no existiendo motivos que impliquen realizar un pronunciamiento distinto.

En cuanto a la fijación del régimen de visitas para el progenitor no custodio, según establece el art. 94 CCiv, se entiende ajustada al favor filii el pronunciamiento relativo a este extremo antes referido y que luego se dirá en el suplico, que incluye pernocta del menor en casa del padre y que no ha supuesto ningún problema, ya que el menor ha ido pernoctando con el padre los fines de semana que ha acudido a su domicilio y no se ha producido ninguna situación de riesgo o malestar para el menor.

En consecuencia, es el interés de los hijos el que debe ser tomado en cuenta para establecer el régimen de guarda y custodia con prevalencia sobre el deseo de los progenitores de tenerlos consigo.

En cuanto a la pensión alimenticia, se regula en el art. 93 CCiv y, en este caso, a la vista de las circunstancias económicas de D. [NOMBRE Y APELLIDOS], que está cobrando la prestación por desempleo, y las necesidades del hijo, que cuenta con [Nº] años de edad, se estima adecuado establecer una pensión alimenticia a cargo del padre de [IMPORTE] euros mensuales.

Los alimentos comprenden todo lo que es indispensable para el sustento, habitación, vestido y asistencia médica del menor, así como también la educación, con arreglo a lo establecido en el art. 142 CCiv, y la determinación de la cuantía de la pensión debe tener en cuenta dos factores, a saber, la capacidad económica de los alimentantes y las necesidades del alimentista, a tenor del art. 146 del citado cuerpo legal, de modo que con los datos existentes dicha cantidad resulta ajustada para cubrir las necesidades del menor por cuanto el mismo tiene garantizada la asistencia sanitaria y la formación educativa, y la dispensación de la habitación, sustento y vestido queda debidamente asegurada con la prestación alimenticia por importe de [IMPORTE] euros, debiendo ponerse en necesaria relación con las posibilidades económicas de la persona obligada a prestar los alimentos.

VIII.- COSTAS.

Deberán ser impuestas a la contraparte las costas en virtud de lo establecido en el art. 394 LEC.

Por todo lo expuesto,

SUPLICO AL TRIBUNAL,

que teniendo por presentado este escrito, con sus documentos y copias de todo ello, se sirva admitirlo, y tener por formulada en tiempo y forma CONTESTACIÓN A LA DEMANDA SOBRE GUARDA Y CUSTODIA, RÉGIMEN DE VISITAS Y PENSIÓN DE ALIMENTOS para el menor [NOMBRE DEL MENOR], interpuesta por Dña. [NOMBRE Y APELLIDOS] frente a D. [NOMBRE Y APELLIDOS]; y tras los trámites de rigor, previa la intervención del Ministerio Fiscal, se dicte Sentencia, en la que, estimándose los argumentos de esta parte, se acuerde la desestimación de la demanda en lo relativo a la pensión alimenticia y régimen de visitas, y se declaren los siguientes pronunciamientos:

1) Establecimiento de un régimen de visitas a favor del padre consistente en fines de semana alternos desde los sábados a las 10 horas hasta el domingo a las 21:00 horas, así como la mitad de las vacaciones de Navidad, Semana Santa y verano, correspondiendo elegir, en caso de discrepancia entre los padres, a la madre los años pares y el padre los impares.
2) Fijación de una pensión de alimentos a favor del hijo menor en la cantidad de [IMPORTE] mensuales que deberá ingresar el padre todos los meses por adelantado dentro de los primeros cinco días de cada mes en la cuenta que designe la actora, que serán actualizables cada año conforme a la variación porcentual experimentada por el IPC, al vencimiento de cada anualidad de la sentencia.
3) Con expresa imposición de costas a la parte contraria.

Es de Justicia que pido en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a

========================================================================
