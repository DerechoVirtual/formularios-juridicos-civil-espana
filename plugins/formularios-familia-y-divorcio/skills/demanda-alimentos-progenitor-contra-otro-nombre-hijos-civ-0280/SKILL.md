---
name: demanda-alimentos-progenitor-contra-otro-nombre-hijos-civ-0280
description: "Demanda de alimentos de un progenitor contra el otro en nombre de hijos menores. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de alimentos de un progenitor contra el otro en nombre de hijos menores

> Formulario **CIV-0280** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Demanda en reclamación de alimentos para un hijo menor de edad, por parte de un progenitor contra el otro.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de alimentos de un progenitor contra el otro en nombre de hijos menores» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de alimentos de un progenitor contra el otro en nombre de hijos menores” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-alimentos-progenitor-contra-otro-nombre-hijos-civ-0280`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] CALLE (4 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] NOMBRE DEL MENOR (4 veces)
- [ ] FECHA (3 veces)
- [ ] IMPORTE (2 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] AÑO
- [ ] COLEGIO
- [ ] DENOMINACIÓN SOCIAL
- [ ] LUGAR
- [ ] MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] Nº DE COLEGIADO/A
- [ ] NÚMERO
- [ ] SEDE

## Normas que cita el formulario

- art. 769.3 LEC
- art. 753 LEC
- art. 437.1 LEC
- art. 5 Ley Orgánica 1/2025
- art. 110 CC
- art. 143 Código Civil
- art. 142 CC
- art. 394 LEC
- art. 770.6 LEC

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

- Junto a «…AL DE INSTANCIA SECCIÓN CIVIL SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD DE [SEDE]»: Denominación legal: Sección de Familia, Infancia y Capacidad. Si no existe en el partido, conoce la Sección Civil o la Única (art. 86.3-4 LOPJ). Fuente: LOPJ arts. 84.2.a) y 86 (redacc. LO 1/2025, BOE-A-2025-76).

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

SECCIÓN CIVIL

SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS], Procurador de los Tribunales, que actúa en nombre y representación de Dña. [NOMBRE Y APELLIDOS] provista de D.N.I. nº [NÚMERO], con domicilio en esta ciudad, calle [CALLE], a virtud de poder para pleitos cuya copia acompaño para su unión a los autos mediante testimonio bastante, con ruego de devolución de la copia autorizada por necesitarla a otros usos, bajo dirección de la Letrada Dña. [NOMBRE Y APELLIDOS], colegiada nº [Nº DE COLEGIADO/A] del Iltre. Colegio de Abogados de [COLEGIO], cuyo despacho se abre en [LOCALIDAD], calle [CALLE], ante el Tribunal comparezco y como mejor en Derecho proceda, DIGO:

Que por medio del presente escrito, siguiendo las instrucciones de mi mandante, vengo a formular demanda en reclamación de ALIMENTOS para su hija menor [NOMBRE DEL MENOR], frente a D. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], y el MINISTERIO FISCAL, con base a los siguientes datos y argumentos:

HECHOS

PRIMERO.- Mi patrocinada y D. mantuvieron una relación de pareja semejante a la de los casados entre los años [AÑO], y fruto de la misma nació el [FECHA] una hija, de nombre [NOMBRE DEL MENOR], por consiguiente menor de edad, como se demuestra con la certificación registral que hace documento nº [Nº DE DOCUMENTO], en el que consta el reconocimiento del padre dentro del plazo de inscripción.

SEGUNDO.- Desde el día [FECHA] cesó la convivencia entre mi patrocinada y el hoy demandado D. [NOMBRE Y APELLIDOS], habiendo abandonado este último el domicilio que la pareja venía compartiendo sito en esta Ciudad, calle [CALLE], desatendiendo desde esta fecha las obligaciones alimenticias que legalmente le incumben respecto a su hija menor.

TERCERO.- D. tiene un trabajo fijo y estable en la empresa [DENOMINACIÓN SOCIAL] sita en esta Ciudad, calle [CALLE], percibiendo un sueldo mensual de [IMPORTE] euros, además de dos pagas extraordinarias por el importe cada una de ellas de [IMPORTE] euros, y es titular de un piso sito en [LOCALIDAD] y de una finca sita en [LOCALIDAD], mientras que mi patrocinada carece de ingresos propios, y aún de cualificación profesional de cualquier tipo, habiendo tenido que recurrir a sus propios padres para subvenir a los gastos de formación y alimentación de la hija común de ambos.

CUARTO.- Mi mandante ha apurado todos los procedimientos a su alcance para lograr que el hoy demandado asuma las obligaciones económicas respecto a su hija [NOMBRE DEL MENOR], viéndose obligada a interponer la presente demanda ante la negativa de éste a abonar cantidad alguna en este concepto.

Así, previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento nº [Nº DE DOCUMENTO]

FUNDAMENTOS DE DERECHO

I.- COMPETENCIA

Conforme a lo establecido en el art. 769.3 LEC como fuero de competencia territorial se fija la circunscripción del Juez competente para conocer del proceso en el partido del último domicilio común de los progenitores.

II.- PROCEDIMIENTO

Las pretensiones que versan exclusivamente sobre alimentos reclamados por un progenitor contra el otro en nombre de los hijos menores se incluyen en el ámbito de aplicación del Título I del Libro IV, y se sustancian conforme al modelo de proceso especial del art. 753 LEC, que es juicio verbal con contestación escrita.

III.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 en relación con el art. 437.1 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

IV.- FONDO DEL ASUNTO

Uno de los deberes fundamentales del titular de la patria potestad es la alimentación de los hijos (art. 154, párrafo II.1º CC) deber que se deriva de la relación paterno-filial hasta el punto de que la mantiene aún en los casos de privación de la patria potestad (art. 110 CC). Este deber-función se traduce en la obligación de prestar alimentos establecida en los artículos 143, 144 y concordantes del Código Civil.

La hija [NOMBRE DEL MENOR] tiene una edad en la que progresivamente se van ampliando sus necesidades, tanto escolares como de mantenimiento y educación, que son esenciales para la formación de la menor.

La cantidad que se solicita resulta ajustada a las necesidades de la menor puesto que los alimentos comprenden todo lo que es indispensable para el sustento, habitación, vestido y asistencia médica, así como también la educación, con arreglo a lo establecido en el artículo 142 CC, y su cuantía debe ser proporcional al caudal o medios de quien los da, y a las necesidades de quien los recibe, a tenor del artículo 146 del citado cuerpo legal, siendo el deber de los progenitores el procurar una formación integral de los hijos.

Mientras que el demandado es un profesional que disfruta de una buena situación económica, mi representada carece de ingresos económicos más allá de la pequeña contribución de sus padres, y no puede hacer frente por sí sola a todos los gastos de mantenimiento y escolaridad, que son cada día más cuantiosos.

Todo ello conformado con el criterio de protección y salvaguardia de los intereses de los hijos que inspira toda nuestra normativa positiva, no siendo lícito a uno de los progenitores abandonar sus deberes de asistencia y alimentos que le incumben respecto a los mismos, haciéndolos recaer exclusivamente sobre el otro progenitor.

Por todo ello, interesa al derecho de mi mandante garantizar los derechos económicos que le asisten a la hija menor de ambos progenitores, viéndose obligada a solicitar amparo jurídico ante la negativa del demandado a asumir las obligaciones que legalmente le corresponden.

V.- COSTAS

Las costas procesales deben ser impuestas a la parte demandada, por criterio del íntegro vencimiento, en atención al art. 394 LEC.

Y demás normas y jurisprudencia de general y pertinente aplicación.

En virtud de lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito con los documentos que se acompañan y sus copias, se digne admitirlos y tener por formulada demanda en reclamación de alimentos contra D. [NOMBRE Y APELLIDOS], y seguido que sea el procedimiento por sus pertinentes trámites, con citación del Ministerio Fiscal, se sirva dictar Sentencia por la que, estimando la presente demanda, se condene al demandado a abonar a la actora, en concepto de alimentos para su hija menor, la suma mensual deeuros, revalorizables anualmente conforme a, con expresa imposición de las costas procesales al demandado si resiste la pretensión.

OTROSÍ DIGO que por necesitar para otros usos la copia de escritura de poder acreditativa de la representación del suscrito Procurador, intereso y

SUPLICO AL TRIBUNAL se sirva acordar su desglose y devolución a esta parte, dejando en autos testimonio de la misma.

Es de Justicia que pido en [LUGAR], a [FECHA].

SEGUNDO OTROSÍ DIGO: Que al amparo del art. 770.6ª LEC interesa al derecho de mi parte, como MEDIDA CAUTELAR, para garantizar la efectividad de la sentencia que en su día recaiga, se acuerde el embargo de bienes del demandado en cantidad suficiente para cubrir la deuda alimenticia reclamada.

Reitero Justicia en lugar y fecha ‘ut supra’.

Firma del Abogado/a	Firma del Procurador/a

========================================================================
