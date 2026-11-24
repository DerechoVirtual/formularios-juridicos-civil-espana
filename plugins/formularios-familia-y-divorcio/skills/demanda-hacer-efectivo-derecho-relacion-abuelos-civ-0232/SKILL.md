---
name: demanda-hacer-efectivo-derecho-relacion-abuelos-civ-0232
description: "Demanda para hacer efectivo el derecho de relación con abuelos, hermanos y allegados (Cataluña). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda para hacer efectivo el derecho de relación con abuelos, hermanos y allegados (Cataluña)

> Formulario **CIV-0232** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda para hacer efectivo el derecho de relación con abuelos, hermanos y allegados (Cataluña)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda para hacer efectivo el derecho de relación con abuelos, hermanos y allegados (Cataluña)” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-hacer-efectivo-derecho-relacion-abuelos-civ-0232`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (14 veces)
- [ ] NOMBRE DEL MENOR (6 veces)
- [ ] Nº (5 veces)
- [ ] Nº DE DOCUMENTO (5 veces)
- [ ] SEDE (3 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] CALLE
- [ ] EDAD (Nº DE AÑOS)
- [ ] MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] NOMBRE DEL CENTRO ESCOLAR

## Normas que cita el formulario

- art. 236 Código Civil
- art. 85.1 LOPJ
- art. 770.3 LEC
- art. 155.2 Ley 1/2000
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

### Avisos de actualización (1) — se aplican en el texto, nunca se copian en el documento

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] Q.P.T.R.C.»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] Q.P.T.R.C.

Don [NOMBRE Y APELLIDOS] Procurador de los Tribunales, actuando en nombre y representación de Don [NOMBRE Y APELLIDOS], y Doña [NOMBRE Y APELLIDOS], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], y bajo la dirección Letrada de Don [NOMBRE Y APELLIDOS], ante el Tribunal comparezco y,como mejor proceda en Derecho, DIGO:

Que en la indicada representación y siguiendo instrucciones de mi principal formulo DEMANDA DE PROCESO DE MENORES contra Doña [NOMBRE Y APELLIDOS], provista de Documento Nacional de Identidad núm. [Nº], con domicilio a efectos de notificaciones y emplazamientos en la localidad de [LOCALIDAD], calle [CALLE], a fin y efecto de que se declare el derechos de los menores [NOMBRE DEL MENOR] y [NOMBRE DEL MENOR] a relacionarse con los abuelos paternos y se fije un régimen de visitas, adoptándose las medidas que el Juzgador estime necesarias para la efectividad de lo solicitado, la cual baso en los siguientes

HECHOS

PRIMERO.- Que mis mandantes están legitimados para ejercitar el derecho reclamado en el presente litigio, al amparo de lo que dispone el artículo 236-4 del Código Civil de Cataluña, ante la imposiblidad de relacionarse con sus nietos y en su calidad de abuelos paternos de los menores [NOMBRE DEL MENOR], de [Nº] años de edad y [NOMBRE DEL MENOR] de [Nº] años de edad, hijos de Don [NOMBRE Y APELLIDOS] y de Doña [NOMBRE Y APELLIDOS], acompañando en prueba de lo manifestado certificado literal de nacimiento del menor del Registro Civil de los de [SEDE] como Documento núm. [Nº], siendo a su vez Don [NOMBRE Y APELLIDOS] hijo de mis representados, acompañando en prueba de lo manifestado certificado literal del nacimiento del Registro Civil de los de [SEDE] como Documento núm. [Nº DE DOCUMENTO]

SEGUNDO.- La imposibilidad de mis mandantes de relacionarse con sus nietos trae causa del procedimiento de separación matrimonial instado por Doña [NOMBRE Y APELLIDOS] contra Don [NOMBRE Y APELLIDOS], hijo de mis representados, en el cual se adjudicó la guarda y custodia de los hijos comunes del matrimonio a la madre, privándose el derecho de visitas y estancia al padre como consecuencia de la interposición de una querella por agresión sexual contra el mismo lo que motivó que en sentencia de separación matrimonial, sin que se estableciera ningún derecho a relacionarse con los abuelos paternos ( acompaño en prueba y mediante testimonio de la sentencia como Documento núm. [Nº DE DOCUMENTO]). En todo este tiempo, la madre se ha negado reiteradamente a que los menores fueran visitados por sus abuelos, cortando todo tipo de relación con su familia paterna, cuando los abuelos paternos siempre han velado por el bienestar de los menores y han tenido una extraordinaria relación personal con ellos.

Por tanto, en la fecha de interposición de la presente demanda los abuelos paternos llevan más de seis meses sin comunicar con su nietos ante la incomprensible y arbitraria negativa de la madre a que el menor atienda sus llamadas telefónicas, razón por la cual se han visto en la obligación de interponer la presente acción ante la imposibilidad de llegar a un buen entendimiento con la madre del menor y en protección del interés del mismo, teniendo en consideración que con anterioridad a la separación matrimonial los abuelos mantenían una relación afectiva muy estrecha con su nieto al ser los encargados de recogerlo diariamente a la salida del colegio [NOMBRE DEL CENTRO ESCOLAR] quedándose con frecuencia a pernoctar en su domicilio familiar.

Esta situación si bien en todo caso es perjudicial los menores, por los lazos afectivos que siempre han tenido con sus abuelos, no hay que pasar por alto el daño personal y emocional que están sufriendo mis mandantes.

Esta representación desconoce las razones por las cuales la madre priva a los abuelos paternos el derecho a disfrutar de su nieto, al carecer de justa causa para ello, si bien con anterioridad a la interposición de la presente demanda han realizado todos los esfuerzos para solventar familiarmente la situación planteada resultando del todo inútiles, es por lo que lo solicitado en la presente demanda, entiende esta representación, dicho sea con el debido respeto, es de cabal importancia para los menores no pudiendo este derecho ser impedido unilateral y caprichosamente por quien dispone de la guarda y custodia.

TERCERO.- Como consecuencia de lo anterior, amparado en el artículo 236-4 del Código Civil de Cataluña, solicitamos que se fije un régimen de visitas y estancia de los menores con los abuelos paternos, proponiendo que puedan pasar con ellos los fines de semana alternos desde las 11 horas a las 20 horas del sábado y del domingo pernoctando en el domicilio familiar, que en los periodos vacacionales los abuelos paternos podrán tener consigo al menor durante quince días de las vacaciones de verano y una semana de las de Navidad, siendo los abuelos quienes elijan los días los años pares y la madre los años impares. Y que puedan comunicar telefónicamente con los menores cuantas veces lo consideren oportuno.

CUARTO.- Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento nº [Nº DE DOCUMENTO]

A estos hechos son de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

Jurisdicción

El orden jurisdiccional civil es el único competente para conocer de los negocios o demandas civiles que se susciten en territorio español, entre españoles, extranjeros y entre españoles y extranjeros, con arreglo a lo estipulado en la Ley Orgánica del Poder Judicial y en los tratados y convenios internacionales.

Competencia objetiva y funcional

Con arreglo a lo dispuesto en el artículo 45 de la Ley de Enjuiciamiento Civil, en relación con lo dispuesto en el art. 85.1º LOPJ, la Sección Civil del Tribunal de Instancia es competente para conocer el presente litigio.

Competencia territorial

Los Tribunales a los que me dirijo son competentes al ser los del domicilio de los menores, conforme al artículo 770.3 de la LEC.

Clase de juicio

En virtud de lo dispuesto en el apartado 3 del artículo 236-4 del Código Civil de Cataluña debe sustanciarse el presente litigio por los trámites del procedimiento especial sobre guarda de menores.

Capacidad de la parte actora y de la demandada

De conformidad con lo dispuesto en el artículo 6.1 de la Ley de Enjuiciamiento civil, relativo a la capacidad para ser parte, podrán se parte en los procesos ante los tribunales civiles: 1º. Las personas físicas, de lo que se infiere que tanto los actores como la demandada tienen capacidad para ser parte.

Legitimación activa

De conformidad con el artículo 236-4 del Código Civil de Cataluña la legitimación activa la ostentan mis mandantes por ser los abuelos paternos del menor, según se acredita mediante los certificados literales de nacimiento acompañados al presente escrito de demanda como documentos números [Nº DE DOCUMENTO] y

Legitimación pasiva

En relación con la legitimación pasiva significar que la ostenta la demandada por ser la madre del menor y la titular de la patria potestad y la guarda y custodia que está privando sin justa causa del disfrute del régimen de visitas, estancia y comunicaciones a los abuelos paternos y al nieto.

Postulación y defensa

Conforme a lo dispuesto en los artículos 23 y 31 de la Ley de Enjuiciamiento Civil se cumplen con las normas de postulación, al comparecer mis mandantes en el presente procedimiento representados por el Procurador de los Tribunales, tal y como ya se ha indicado en el encabezamiento del presente escrito y en virtud de los poderes que se acompañan, y bajo la dirección del Letrado firmante.

Requisitos formales

El presente procedimiento se inicia por medio de demanda que reúne todos los requisitos exigidos en el artículo 399 de la Ley de Enjuiciamiento Civil y demás relativos a esta materia. A los efectos prevenidos en el artículo 399 en relación con el artículo 155.2 de la Ley 1/2000, de 7 de enero de Enjuiciamiento Civil han de consignarse los datos y circunstancias de identificación y domicilio de la parte actora y de la parte demandada.

Intervención del Ministerio Fiscal y Audiencia del menor

De conformidad con el artículo 749.2 de la Ley de Enjuiciamiento Civil, teniendo los nietos la edad de [EDAD (Nº DE AÑOS)] y [Nº] años, resulta preceptiva la intervención del Ministerio Fiscal, al disponer que "En los demás procesos a que se refiere este título será preceptiva la intervención del Ministerio Fiscal, siempre que alguno de los interesados en el procedimiento sea menor, incapacitado o esté en situación de ausencia legal.", los cuales deberán ser oídos si tienen suficiente juicio.

Cumplimiento de los requisitos de procedibilidad

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 en relación con el art. 437.1 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

Normas de derecho sustantivo

El artículo 236-4 del Código Civil de Cataluña dispone que los hijos tiene derecho a relacionarse con los abuelos y éstos tienen el derecho a relacionarse con los hijos, y que los progenitores deberán facilitar estas relaciones y sólo pueden impedirlas si existe justa causa. A través de la presente demanda mis mandantes han solicitado el reconocimiento del derecho regulado en el citado artículo 236-4 no mediando justa causa que impida las relaciones personales de los abuelos con sus nietos, siendo unánime el criterio jurisprudencial que protege el derecho de los abuelos a relacionarse con el nieto, pudiendo citarse la Sentencia del Tribunal Supremo de 23 de noviembre de 1999, rec. 1048/1995 y las en ella citadas de 11 de junio de 1996, rec. 3446/1991 y 17 de septiembre de 1996, rec. 2631/1992 y de 11 de junio de 1998, rec. 1474/1994, y Sentencia de la Audiencia Provincial de Barcelona de 14 de septiembre 2.000, rec. 16/2000.

Costas

Conforme establece el artículo 349 de la Ley de Enjuiciamiento Civil, las costas se impondrán a la parte cuyas pretensiones se hayan visto totalmente rechazadas.

Iura novit curia

Demás normas concordantes y de aplicación: iura novit curia.

Por lo expuesto,

AL TRIBUNAL SUPLICO: Que teniendo por presentado este escrito con los documentos acompañados y sus copias, lo admita; tenga por interpuesta y formulada por el Procurador que suscribe, con quien se entiendan las sucesivas diligencias, en nombre y representación de Don [NOMBRE Y APELLIDOS] y Doña [NOMBRE Y APELLIDOS], con devolución de la copia electrónica del poder notarial de representación informática (o digitalizada) una vez quede testimonio en autos, DEMANDA DE PROCESO DE GUARDA DE MENORES contra la demandada Doña [NOMBRE Y APELLIDOS], emplazándola debidamente y, sustanciada por todos sus trámites y en méritos de los hechos y fundamentos de derecho alegados se dicte Sentencia por la que se condene a Doña [NOMBRE Y APELLIDOS] a permitir la relación entre los demandantes y sus nietos [NOMBRE DEL MENOR] y [NOMBRE DEL MENOR], cumpliendo con el régimen de visitas, estancia y comunicaciones que se deja interesado en el hecho tercero de esta demanda, tomándose para ello las medidas que el Juzgador estime más oportunas, con expresa imposición de costas a la demandada, dando a los autos el impulso procesal con arreglo a Derecho.

I OTROSI DIGO: Que siendo la voluntad de esta representación la de cumplir los requisitos exigidos por la Ley intereso que de conformidad con el artículo 231 de la Ley de Enjuiciamiento Civil puedan ser subsanados los defectos en que incurran los actos procesales de esta parte.

Por lo expuesto,

AL TRIBUNAL SUPLICO: Que se tenga por efectuada la anterior manifestación a los efectos legales oportunos.

II OTROSÍ DIGO: Que esta parte interesa el recibimiento a prueba en el momento procesal oportuno.

En su virtud,

AL TRIBUNAL SUPLICO: Que se tenga por efectuada la anterior manifestación a los efectos legales oportunos.

Es justicia que insto en [LOCALIDAD]

Firmas del Letrado y del Procurador:

========================================================================
