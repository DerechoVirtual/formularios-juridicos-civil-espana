---
name: demanda-separacion-contenciosa-prestacion-civ-0241
description: "Demanda de separación contenciosa con prestación compensatoria (Derecho civil catalán). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de separación contenciosa con prestación compensatoria (Derecho civil catalán)

> Formulario **CIV-0241** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Demanda de separación contenciosa de un matrimonio sin hijos, entre cónyuges de vecindad civil catalana y régimen de separación de bienes, en la que se solicita la atribución del uso de la vivienda conyugal y la fijación de una prestación compensatoria (arts. 233-14 a 233-17 del Código Civil de Cataluña), junto con la separación del art. 81 del Código Civil.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de separación contenciosa con prestación compensatoria (Derecho civil catalán)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de separación contenciosa con prestación compensatoria (Derecho civil catalán)” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-separacion-contenciosa-prestacion-civ-0241`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (11 veces)
- [ ] AÑO (5 veces)
- [ ] IMPORTE (4 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] MES (3 veces)
- [ ] DÍA (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL DEMANDADO (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL DEMANDANTE (2 veces)
- [ ] SEDE (2 veces)
- [ ] AÑOS
- [ ] CALLE
- [ ] DENOMINACIÓN SOCIAL
- [ ] DOLENCIA
- [ ] DOMICILIO
- [ ] EDAD
- [ ] ENTIDAD
- [ ] EXPONER LOS MOTIVOS EN CADA CASO
- [ ] IBAN
- [ ] LUGAR DE LA CELEBRACIÓN
- [ ] NOMBRE Y APELLIDOS DEL ABOGADO/A
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] NOMBRE Y APELLIDOS, Nº DE COLEGIADO
- [ ] PISO
- [ ] PUERTA

## Normas que cita el formulario

- art. 81 Código Civil
- art. 233 Código Civil
- art. 769 LEC
- art. 85.1 LOPJ
- art. 437.1 LEC
- art. 5 Ley Orgánica 1/2025

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
- Junto a «… económica regulada en el art. 232-5; e) cualquier otra circunstancia relevante.»: la enumeración anterior corresponde a la redacción antigua del art. 233-15 del Código Civil de Cataluña; en los fundamentos de derecho se transcribe la redacción posterior. Comprobar la redacción vigente del precepto y unificar la cita.

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

Q.P.T.R.C.

[NOTA: en su caso, la competencia corresponderá a la Sección de Familia, Infancia y Capacidad, donde se hubiera constituido.]

Don/Doña [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, en la representación que ostento de Doña/Don [NOMBRE Y APELLIDOS DEL DEMANDANTE], según acredito mediante copia electrónica del poder notarial de representación, y bajo la dirección letrada de Don/Doña [NOMBRE Y APELLIDOS DEL ABOGADO/A], ante la Sección Civil del Tribunal de Instancia de [SEDE] que por turno de reparto corresponda, comparezco y, como mejor proceda en Derecho, DIGO:

Que, siguiendo instrucciones de mi poderdante, por medio del presente escrito interpongo, en nombre del mismo/de la misma, DEMANDA DE SEPARACIÓN CONYUGAL contra Don/Doña [NOMBRE Y APELLIDOS DEL DEMANDADO], vecino/a de la localidad de [LOCALIDAD], con domicilio en calle [CALLE], núm. [Nº], piso [PISO], puerta [PUERTA], la cual baso en los siguientes

HECHOS

PRIMERO.– Mi representado/a y el/la cónyuge demandado/a contrajeron matrimonio en forma [ELEGIR: civil / religiosa] el día [DÍA] del mes de [MES] del año [AÑO] en [LUGAR DE LA CELEBRACIÓN], según acredito mediante certificación literal del Registro Civil de la localidad de [LOCALIDAD] que acompaño como documento número [Nº], constando inscrito el mismo en el Tomo [Nº], Folio [Nº], Sección [Nº] [OPCIONAL — si ha lugar: en virtud de certificación eclesiástica, de ser matrimonio canónico].

SEGUNDO.– Del referido matrimonio no han nacido hijos.

TERCERO.– El domicilio conyugal, propiedad de mi representado/a, ha venido siendo el sito en [DOMICILIO], según acredito mediante la correspondiente escritura, que acompaño como documento núm. [Nº].

CUARTO.– El régimen económico del matrimonio es el de separación de bienes, teniendo en cuenta que la vecindad civil de ambos cónyuges es la catalana.

QUINTO.– Habiendo transcurrido el periodo establecido en el artículo 81 del Código Civil y por razones que no son del caso exponer, lo cierto es que la convivencia entre los cónyuges se ha deteriorado, con la consiguiente pérdida de la «affectio maritalis», lo cual determina la concurrencia de la causa de separación matrimonial que se invoca en este proceso conforme al citado artículo 81 del Código Civil.

SEXTO.– Por lo que se refiere a las medidas que deben fijarse como consecuencia de la separación, paso a manifestar lo siguiente:

A) En cuanto al uso de la vivienda conyugal y ajuar, se solicita que se atribuya a mi representado/a por los siguientes motivos [EXPONER LOS MOTIVOS EN CADA CASO], al tratarse del interés más necesitado de protección y ser titular exclusivo/a de la vivienda que constituyó el domicilio familiar.

B) Siendo ambos cónyuges de vecindad catalana y rigiendo el régimen económico-matrimonial de separación de bienes, procede fijar la prestación compensatoria establecida en el art. 233-14 del Código Civil de Cataluña, teniendo en cuenta que la misma ha sido interpretada por las SSTSJ Cataluña de 30 de mayo de 2007, rec. 53/2006, con cita de las de 4 de marzo de 2002, rec. 61/2001, 28 de octubre de 2003, rec. 75/2003 y 19 de enero de 2004, rec. 110/2003, con una finalidad reequilibradora, de forma que pretende compensar al cónyuge perjudicado en aplicación del principio de solidaridad económica existente durante la situación convivencial y, habida cuenta de que los términos comparativos que generan el derecho a la pensión son dos, la situación existente durante el matrimonio y la situación previsible después de la crisis, atendidas las circunstancias personales y profesionales del beneficiario, debiendo tenerse en cuenta, conforme al art. 233-15 del Código Civil de Cataluña, las siguientes circunstancias: a) la situación económica resultante para los cónyuges como consecuencia de la nulidad, el divorcio o la separación judicial y las perspectivas económicas previsibles para uno y otro; b) la duración de la convivencia conyugal; c) la edad y la salud de ambos cónyuges; d) en su caso, la compensación económica regulada en el art. 232-5; e) cualquier otra circunstancia relevante.

En este caso, y conforme a los anteriores parámetros, deben significarse las siguientes circunstancias:

1) El/la demandado/a es titular de un negocio de [ACTIVIDAD, p. ej. antigüedades] que ofrece una alta rentabilidad, que ha sido la principal fuente de ingresos del matrimonio, participando mi mandante en ocasiones directamente, sin percibir sueldo alguno, y durante todo el periodo de convivencia de forma indirecta por su dedicación a las tareas domésticas. Hay que resaltar que dicho negocio genera unos rendimientos anuales de gran importancia; se aportan como documentos número [Nº] copias del impuesto sobre la renta de las personas físicas de los ejercicios [AÑOS] a efectos acreditativos.

2) Situación económica resultante de los cónyuges con posterioridad a la separación: aunque mi representado/a desempeñó hasta el mes de [MES] del año [AÑO] jornada laboral reducida en la empresa [DENOMINACIÓN SOCIAL] y percibía un exiguo sueldo de [IMPORTE] euros, tal y como se justifica mediante la aportación de copia del contrato de trabajo y recibo de nómina como documentos número [Nº], actualmente carece de otros ingresos o bienes con los que mantenerse, siendo su único bien la vivienda que fue familiar, en tanto que el/la demandado/a sigue explotando el negocio de su titularidad y es propietario/a de varios inmuebles arrendados a terceras personas, por los que percibe unas rentas anuales de [IMPORTE] euros, tal como se constata del examen de las declaraciones fiscales aportadas.

3) La duración de la convivencia conyugal: debiendo tenerse en cuenta que, tal y como puede apreciarse, mi representado/a contrajo matrimonio con D./Dña. [NOMBRE Y APELLIDOS] en [AÑO], por lo que la convivencia conyugal ha tenido una duración de [Nº] años.

4) La edad y la salud de los cónyuges: debe tenerse en cuenta que mi representado/a cuenta en la actualidad con [EDAD] años de edad, lo que imposibilita de forma absoluta la posibilidad de acceso al mercado laboral. Por otro lado, la situación física de mi representado/a no puede calificarse de correcta, ya que viene padeciendo desde el año [AÑO] [DOLENCIA], dolencia que es crónica y degenerativa, tal y como consta en el informe médico expedido por el Dr./la Dra. [NOMBRE Y APELLIDOS], que se aporta como documento número [Nº].

En orden a todas las consideraciones efectuadas, se cifra la cuantía de la compensación solicitada por mi mandante en [IMPORTE] euros mensuales, la cual deberá fijarse con carácter indefinido y con las actualizaciones correspondientes, de acuerdo con lo que dispone el art. 233-17 del Código Civil de Cataluña.

SÉPTIMO.– Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [INDICAR EL MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS AL QUE LAS PARTES SE HAN SOMETIDO EN CUMPLIMIENTO DEL REQUISITO DE PROCEDIBILIDAD QUE EXIGE LA LO 1/2025], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento n.º [Nº] [ESPECIFICAR EL DOCUMENTO QUE ACREDITA QUE SE HA ACUDIDO A UN MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS].

A los anteriores hechos les son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

Legitimación activa y pasiva

La ostentan ambas partes por su condición de cónyuges del matrimonio cuya separación se solicita, en relación con la causa de separación invocada.

Competencia

Es competente este Tribunal, de conformidad con lo previsto en el artículo 769 de la LEC, en relación con lo dispuesto en el art. 85.1 LOPJ.

Procedimiento

Son de aplicación las normas contenidas en el Libro IV, Título Primero, Capítulo Primero de la LEC y las normas del juicio verbal, con sujeción, además, a las reglas establecidas en el artículo 770 de la misma ley, conforme se previene en el párrafo preliminar de dicho artículo.

Cumplimiento de los requisitos de procedibilidad

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4.º y 399.3 LEC, en relación con el art. 437.1 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

Separación

Artículo 81 del Código Civil.

Causa de separación

Existe petición de mi representado/a, habiendo transcurrido más de tres meses desde la celebración del matrimonio.

Efectos derivados o medidas

Es de aplicación el Código Civil de Cataluña, en especial el artículo 233-14, cuando establece el derecho a la prestación compensatoria del cónyuge cuya situación económica, como consecuencia de la ruptura de la convivencia, resulte más perjudicada, en cuantía que no exceda el nivel de vida de que gozaba durante el matrimonio, ni del que pueda mantener el cónyuge obligado al pago, teniendo en cuenta el derecho de alimentos de los hijos, que es prioritario; para establecer dicha cuantía, el art. 233-15 establece que debe valorar especialmente: «a) La posición económica de los cónyuges, teniendo en cuenta, si procede, la compensación por razón de trabajo o las previsibles atribuciones derivadas de la liquidación del régimen económico matrimonial. b) La realización de tareas familiares u otras decisiones tomadas en interés de la familia durante la convivencia, si eso ha reducido la capacidad de uno de los cónyuges de obtener ingresos. c) Las perspectivas económicas previsibles de los cónyuges, teniendo en cuenta su edad y estado de salud y la forma en que se atribuye la guarda de los hijos comunes. d) La duración de la convivencia. e) Los nuevos gastos familiares del deudor, si procede».

Asimismo, se cumple el requisito establecido en el apartado 2 del art. 233-14 tras la reforma operada por la Ley del Parlamento de Cataluña 5/2017, con entrada en vigor el 1 de enero de 2018, al solicitarse en este proceso, que es el primer proceso matrimonial entre las partes.

En cuanto al pago de la prestación compensatoria, es de aplicación el art. 233-17 del Código Civil de Cataluña, solicitando que se abone en forma de pensión en dinero y por mensualidades anticipadas, fijando los correspondientes criterios objetivos y automáticos de actualización de la cuantía, tal como autoriza el apartado 3 del precepto.

Procedimiento

Son de aplicación las normas contenidas en el Libro IV, Título Primero, Capítulo Primero de la LEC y las normas del juicio verbal, con sujeción, además, a las reglas establecidas en el artículo 770 de la misma ley, conforme se previene en el párrafo preliminar de dicho artículo.

Costas

Artículo 394 de la LEC.

Demás normas concordantes y de aplicación

Iura novit curia.

En su virtud,

SUPLICO AL TRIBUNAL: Que tenga por presentado este escrito con los documentos acompañados y sus copias; admita todo ello; por interpuesta por el Procurador/a que suscribe, con quien se entiendan las sucesivas diligencias, en nombre y representación de Don/Doña [NOMBRE Y APELLIDOS DEL DEMANDANTE], DEMANDA DE SEPARACIÓN CONYUGAL contra Don/Doña [NOMBRE Y APELLIDOS DEL DEMANDADO]; y previa notificación y emplazamiento, y por los trámites procesales pertinentes, dicte sentencia por la que, dando lugar a la separación conyugal, determine como medidas o efectos derivados de la misma los siguientes:

a) En cuanto al uso de la vivienda conyugal y ajuar, que se atribuya a mi mandante.

b) En cuanto a la prestación compensatoria, que se fije la cantidad de [IMPORTE] euros mensuales, a pagar por mensualidades anticipadas dentro de los cinco primeros días de cada mes, mediante ingreso en la cuenta n.º [IBAN] que Doña/Don [NOMBRE Y APELLIDOS] tiene abierta en la entidad financiera [ENTIDAD], actualizándose anualmente conforme al Índice Oficial de Precios al Consumo para el conjunto nacional.

c) En cuanto al régimen económico del matrimonio: se solicita su disolución como efecto inherente a la firmeza de la sentencia de separación.

Y con condena en costas a la parte demandada, si concurrieren las circunstancias previstas en el artículo 394 de la Ley de Enjuiciamiento Civil.

Es justicia que insto en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma de Abogado: [NOMBRE Y APELLIDOS, Nº DE COLEGIADO]

Firma de Procurador: [NOMBRE Y APELLIDOS]
