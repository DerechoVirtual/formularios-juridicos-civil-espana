---
name: demanda-extincion-convivencia-alimentos-pension-civ-0089
description: "Demanda de extinción de convivencia con alimentos y pensión compensatoria (convivientes en Cataluña). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de extinción de convivencia con alimentos y pensión compensatoria (convivientes en Cataluña)

> Formulario **CIV-0089** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de extinción de convivencia con alimentos y pensión compensatoria (convivientes en Cataluña)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de extinción de convivencia con alimentos y pensión compensatoria (convivientes en Cataluña)” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-extincion-convivencia-alimentos-pension-civ-0089`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (11 veces)
- [ ] IMPORTE (5 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] CALLE (3 veces)
- [ ] FECHA (3 veces)
- [ ] Nº DE COLEGIADO (3 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] NOMBRE DE LA PARTE (2 veces)
- [ ] Nº (2 veces)
- [ ] A) PROCESALES
- [ ] AÑO
- [ ] B) DE FONDO
- [ ] COLEGIO
- [ ] DÍA
- [ ] MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] MES
- [ ] Nº DE CUENTA (IBAN)
- [ ] Nº DE PISO
- [ ] SEDE

## Normas que cita el formulario

- art. 5 LEC
- art. 6 LEC
- art. 399 LEC
- art. 23 LEC
- art. 31 LEC
- art. 45 LEC
- art. 50 LEC
- art. 253 LEC
- art. 251 LEC
- art. 5 Ley Orgánica 1/2025
- art. 328 LEC

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

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, con número de Colegiado/a [Nº DE COLEGIADO] y de D./Dña. [NOMBRE Y APELLIDOS]; según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], con la dirección letrada del Abogado/a perteneciente al Ilustre Colegio de Abogados de [COLEGIO], D./Dña. [NOMBRE Y APELLIDOS], con núm. [Nº] de colegiado/a, ante el Tribunal comparezco y, como mejor proceda en derecho, DIGO:

Que por medio del presente escrito promuevo DEMANDA DE DECLARACIÓN DE RUPTURA DE PAREJA DE HECHO entre mi mandante D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con domicilio en la calle [CALLE] de [LOCALIDAD], y D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con domicilio en la calle [CALLE] de [LOCALIDAD]; y ADOPCIÓN JUDICIAL DE ALIMENTOS Y PRESTACIÓN ALIMENTARIA ENTRE CONVIVIENTES derivadas del cese de la convivencia de la unión estable, debiendo seguirse los trámites del Juicio Ordinario de la Ley de Enjuiciamiento Civil, por no existir acuerdo entre los ex convivientes.

Se basa la presente demanda en los siguientes,

HECHOS

Unión more uxorio

D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS] iniciaron una relación de pareja marital en fecha [FECHA] Ambos han convivido durante [Nº] años y han formado una familia, habiendo formalizado la relación en escritura pública.

Hijos

De la citada unión han nacido los siguientes hijos: y [NOMBRE Y APELLIDOS] nacidos en las fechas [FECHA] y [FECHA], respectivamente.

Se aportan como Documentos núms. los certificados literales del registro civil [Nº DE DOCUMENTO]

Vecindad civil y domicilio familiar

El último domicilio familiar se encontraba sito en [LOCALIDAD] calle [CALLE] núm. Piso [Nº DE PISO], que fue abandonado por ambos convivientes.

Se acompaña como Documentos núms.: certificados de empadronamiento.

Los convivientes no otorgaron convenio alguno para la regulación de los derechos y deberes de la unión. En consecuencia, ha sido de aplicación el régimen supletorio legal que establece la legislación foral catalana.

Ruptura

Habiendo surgido dificultades en la convivencia, de carácter íntimo y que no se considera preciso relatar, la convivencia se ha vuelto imposible por lo que, mi representado/a, ha decidido solicitar la declaración de ruptura de la unión estable.

Situación económica del actor/a

Mi mandante durante el tiempo que ha durado la convivencia se ha dedicado a las tareas domésticas, así como, a cuidar y educar a los hijos comunes.

Por otro lado, dada su edad y escasa cualificación, mi mandante se encuentra en una situación desfavorable para acceder a un empleo.

Por lo que es necesario fijar una prestación alimentaria por importe de [IMPORTE] euros mensuales por tiempo indefinido.

Situación económica del demandado/a

La situación económica del demandado/a es, por el contrario, muy desahogada. Es abogado, tiene su propio estudio, obteniendo unos rendimientos medios anuales que ascienden a [IMPORTE] euros.

Se solicita se requiera al demandado para que aporte las declaraciones de IRPF correspondientes a los ejercicios tres últimos ejercicios. Dejándose designados los archivos de la Agencia Estatal Tributaria a efectos de prueba, toda vez que a la obtención de dichos documentos no tiene acceso esta parte.

Proceso de negociación previo y medios de solución de controversias de manera amistosa y extrajudicial

Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento nº [Nº DE DOCUMENTO]

A los anteriores hechos son de aplicación los siguientes

FUNDAMENTOS DE DERECHO [A) PROCESALES]

Jurisdicción

Son competentes los Tribunales civiles de conformidad con lo dispuesto en los artículos 5 y 36 de la LECiv.

Capacidad

Mi representado/a ostenta la capacidad necesaria para ser parte en el presente proceso, de conformidad con lo dispuesto en los artículos 6 y siguientes de la LECiv.

Representación procesal y dirección letrada

La representación del actor y la postulación a la presente demanda es la procedente conforme al artículo 399 y siguientes de la LECiv.

- PROCURADOR. El art. 23 de la LECiv establece que la comparecencia en juicio será por medio de Procurador legalmente habilitado para actuar en el tribunal que conozca del juicio.

- ABOGADO. El artículo 31 de la LECiv dispone asimismo que los litigantes serán dirigidos por Abogados habilitados para ejercer su profesión en el tribunal que conozca del juicio.

Legitimación

La legitimación activa le corresponde a [NOMBRE DE LA PARTE] como titular del derecho que se reclama.

La legitimación pasiva le corresponde a [NOMBRE DE LA PARTE] por ser frente a quien se ejercita la pretensión procesal.

Competencia objetiva

Corresponde a los Tribunales de Instancia en función de lo establecido por los artículos art. 85.1º de la Ley Orgánica del Poder Judicial y art. 45 de la LECiv.

COMPETENCIA TERRITORIAL: El art. 50, 1 de la LECiv establece el fuero general de las personas físicas que establece: Salvo que la ley disponga otra cosa, la competencia territorial corresponderá al tribunal del domicilio del demandado y, si no lo tuviere en el territorio nacional, será juez competente el de su residencia en dicho territorio.

Procedimiento

El establecido en los artículos 399 y siguientes de la Ley de Enjuiciamiento Civil, en virtud de lo dispuesto en el art. 251 del citado texto procesal.

La cuantía de la demanda a los efectos de lo dispuesto en los artículos 253 a 255 de la LECiv es la de [IMPORTE] euros, según los establecido en el art. 251,7º de la LECiv.

Cumplimiento de los requisitos de procedibilidad

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

FUNDAMENTOS DE DERECHO [B) DE FONDO]

a) Derecho sustantivo:

FORAL:

-Código Civil Catalán, capítulo IV"convivencia estable en pareja"

Artículo 234-1. Pareja estable.

Dos personas que conviven en una comunidad de vida análoga a la matrimonial se consideran pareja estable en cualquiera de los siguientes casos:

a) Si la convivencia dura más de dos años ininterrumpidos.

b) Si durante la convivencia, tienen un hijo común.

c) Si formalizan la relación en escritura pública.

Artículo 234-2. Requisitos personales.

No pueden constituir una pareja estable las siguientes personas:

a) Los menores de edad no emancipados.

b) Las personas relacionadas por parentesco en línea recta, o en línea colateral dentro del segundo grado.

c) Las personas casadas y no separadas de hecho.

d) Las personas que convivan en pareja con una tercera persona.

Artículo 234-4. Causas de extinción.

1. La pareja estable se extingue por las siguientes causas:

a) Cese de la convivencia con ruptura de la comunidad de vida.

b) Muerte o declaración de fallecimiento de uno de los convivientes.

c) Matrimonio de cualquiera de los convivientes.

d) Común acuerdo de los convivientes formalizado en escritura pública.

e) Voluntad de uno de los convivientes notificada fehacientemente al otro.

2. La extinción de la pareja estable implica la revocación de los consentimientos y poderes que cualquiera de los convivientes haya otorgado a favor del otro.

Artículo 234-5. Pactos en previsión del cese de la convivencia.

En previsión del cese de la convivencia, los convivientes pueden pactar en escritura pública los efectos de la extinción de la pareja estable. A estos pactos se les aplica el artículo 231-20.

Artículo 234-6. Acuerdos conseguidos después del cese de la convivencia.

1. Después del cese de la convivencia, los convivientes pueden acordar los efectos de la extinción de la pareja estable.

2. En el caso de acuerdos alcanzados después del cese de la convivencia, los convivientes de común acuerdo o uno de los convivientes con el consentimiento del otro pueden someter a la aprobación de la autoridad judicial una propuesta de convenio que incluya todos los efectos que la extinción deba producir respecto a los hijos comunes y entre los convivientes.

3. Se aplican a los acuerdos incluidos en una propuesta de convenio y a los alcanzados fuera de convenio los artículos 233-3 y 233-5, respectivamente.

4. Si no hay acuerdo entre los convivientes, se aplica lo establecido por el artículo 233-4.

Sección 3.ª Efectos de la extinción de la pareja estable

Artículo 234-7. Ejercicio de la guarda de los hijos y relaciones personales.

En materia de ejercicio de la guarda de los hijos y relaciones personales, se aplican a la pareja estable los artículos 233-8 a 233-13.

Artículo 234-8. Atribución o distribución del uso de la vivienda familiar.

1. Los convivientes en pareja estable pueden acordar la atribución a uno de ellos del uso de la vivienda familiar, con su ajuar, para satisfacer en la parte que sea pertinente los alimentos de los hijos comunes que convivan con el beneficiario del uso o la eventual prestación alimentaria de este.

2. Si no existe acuerdo o si este no es aprobado, en el caso de que los convivientes tengan hijos comunes, la autoridad judicial puede atribuir el uso de la vivienda familiar, teniendo en cuenta las circunstancias del caso y aplicando las siguientes reglas:

a) Preferentemente, al miembro de la pareja a quien corresponda la guarda de los hijos mientras dure esta.

b) Si la guarda de los hijos es compartida o distribuida entre ambos miembros de la pareja, al que tenga más necesidad.

3. La atribución o distribución del uso de la vivienda, si esta pertenece en todo o en parte al miembro de la pareja que no es beneficiario, debe ser tenida en cuenta para la fijación de los alimentos a los hijos y la prestación alimentaria que eventualmente devengue el otro miembro de la pareja.

4. Se aplica a la atribución o distribución del uso de la vivienda lo establecido por el artículo 233-20.6 y 7 y los artículos 233-21 a 233-25.

Artículo 234-9. Compensación económica por razón de trabajo.

1. Si un conviviente ha trabajado para la casa sustancialmente más que el otro o ha trabajado para el otro sin retribución o con una retribución insuficiente, tiene derecho a una compensación económica por esta dedicación siempre y cuando en el momento del cese de la convivencia el otro haya obtenido un incremento patrimonial superior, de acuerdo con las reglas del artículo 232-6.

2. Se aplica a la compensación económica por razón de trabajo lo establecido por los artículos 232-5 a 232-10.

Artículo 234-10. Prestación alimentaria.

1. Si la pareja estable se extingue en vida de los convivientes, cualquiera de los convivientes puede reclamar al otro una prestación alimentaria, si la necesita para atender adecuadamente a su sustentación, en uno de los siguientes casos:

a) Si la convivencia ha reducido la capacidad del solicitante de obtener ingresos.

b) Si tiene la guarda de hijos comunes, en circunstancias en que su capacidad de obtener ingresos quede disminuida.

2. Los pactos de renuncia a la prestación alimentaria no son eficaces en aquello en que comprometan la posibilidad de atender a las necesidades básicas del conviviente que tiene derecho a pedir, salvo que hayan sido incorporados a una propuesta de convenio presentada de acuerdo con el artículo 234-6.

3. Si uno de los convivientes muere antes de que pase un año desde la extinción de la pareja estable, el otro, en los tres meses siguientes al fallecimiento, puede reclamar a los herederos su derecho a la prestación alimentaria. La misma regla debe aplicarse si el procedimiento dirigido a reclamar la prestación alimentaria se extingue por el fallecimiento del conviviente que debería pagarla.

Artículo 234-11. Pago de la prestación alimentaria.

1. La prestación alimentaria puede atribuirse en forma de capital o en forma de pensión.

2. Si no existe acuerdo, la autoridad judicial resuelve sobre la modalidad de pago de conformidad con las reglas del artículo 233-17.

3. La prestación alimentaria en forma de pensión tiene carácter temporal, con un máximo de tres anualidades, salvo que la prestación se fundamente en la disminución de la capacidad del acreedor de obtener ingresos derivada de la guarda de hijos comunes. En este caso, puede atribuirse mientras dure la guarda.

4. La prestación alimentaria en forma de pensión puede modificarse en los términos del artículo 233-18.

Artículo 234-12. Extinción de la prestación alimentaria fijada en forma de pensión.

La prestación alimentaria en forma de pensión se extingue de acuerdo con las reglas del artículo 233-19.

Artículo 234-13. Ejercicio de los derechos.

Los derechos a la compensación económica por razón de trabajo y a la prestación alimentaria prescriben en el plazo de un año a contar de la extinción de la pareja estable y deben reclamarse, si procede, en el mismo procedimiento en que se determinan los demás efectos de la extinción de la pareja estable.

Artículo 234-14. Efectos de la extinción por muerte.

En caso de extinción de la pareja estable por muerte de uno de los convivientes, el superviviente tiene, además de la compensación por razón de trabajo que eventualmente le corresponda de acuerdo con el artículo 232-5.5, los derechos viduales familiares reconocidos por los artículos 231-30 y 231-31.

Por lo expuesto,

SUPLICO AL TRIBUNAL: Que teniendo por presentado este escrito con los documentos que se acompañan y sus copias, se sirva admitirlos y, en su virtud, tenga por comparecido y parte a D./Dña. [NOMBRE Y APELLIDOS] y en su nombre tener por instada DEMANDA DE DECLARACIÓN DE RUPTURA DE UNIÓN DE HECHO Y ADOPCIÓN DE MEDIDAS ENTRE CONVIVIENTES, y previos los trámites legales pertinentes, dicte sentencia por la que:

1. Se declare judicialmente la ruptura de la unión estable de pareja formada por D./Dña [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS]

2. Se acuerde la adopción de las siguientes medidas:

a) Fijación de prestación alimentaria a favor de mi mandante por la desigualdad económica que produce la ruptura por importe de [IMPORTE] euros/mes por tiempo indefinido.

b) Fijación en concepto de pensión alimenticia para los hijos en la cantidad de [IMPORTE] euros

mes que deberán ser ingresadas en la cuenta [Nº DE CUENTA (IBAN)], por mensualidades anticipadas, del uno al cinco de cada mes.

c) El régimen de visitas que considere más adecuado el Juzgador para el conviviente no custodio.

OTROSÍ DIGO: Que de conformidad con lo dispuesto en el art. 328 de la LECiv, solicitamos del Tribunal requiera al demandado/a a fin de que el día señalado para la vista aporte la documentación que se relaciona:

- Declaración del Impuesto Sobre la Renta de las Personas Físicas correspondiente a los ejercicios fiscales de los tres últimos ejercicios

SUPLICO AL TRIBUNAL: Tenga por hechas las anteriores manifestaciones a los efectos procedentes.

Es Justicia que pido en [LOCALIDAD] a, [DÍA] de [MES] de 20 [AÑO]

Fdo: letrado/a

Colegiado/a núm. [Nº DE COLEGIADO]

Fdo: Procurador/a

Colegiado/a núm. [Nº DE COLEGIADO]

========================================================================
