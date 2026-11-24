---
name: demanda-cese-convivencia-pareja-estable-hecho-medidas-civ-0234
description: "Demanda por cese de convivencia de pareja estable de hecho con medidas cautelares (Derecho común). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda por cese de convivencia de pareja estable de hecho con medidas cautelares (Derecho común)

> Formulario **CIV-0234** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Parte HECHOS FUNDAMENTOS DE DERECHO Suplico de presentación de la demanda Otrosí de cuantía Otrosí de solicitud de adopción de medida cautelar de atribución del uso de la vivienda familiar PRIMERO.- SEGUNDO.- TERCERO.- FUNDAMENTOS DE DERECHO Firmas

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda por cese de convivencia de pareja estable de hecho con medidas cautelares (Derecho común)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda por cese de convivencia de pareja estable de hecho con medidas cautelares (Derecho común)” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-cese-convivencia-pareja-estable-hecho-medidas-civ-0234`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (11 veces)
- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] LOCALIDAD (7 veces)
- [ ] NOMBRE DEL HIJO/A (3 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] AÑO (2 veces)
- [ ] FECHA (2 veces)
- [ ] DÍA
- [ ] ESTUDIOS QUE CURSA
- [ ] LUGAR
- [ ] MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] MES
- [ ] NÚMERO
- [ ] SEDE
- [ ] VECINDAD CIVIL

## Normas que cita el formulario

- art. 49 LEC
- art. 85.1 LOPJ
- art. 249.2 LEC
- art. 5 Ley Orgánica 1/2025
- art. 394 LEC
- art. 730 LEC
- art. 727.11 LEC
- art. 732.2 LEC
- art. 723.1 LEC
- art. 721 LEC
- art. 733 LEC
- art. 728.2 LEC
- art. 728.1 LEC
- art. 732.3 LEC

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

- Junto a «…A, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE Q.P.T.R.C.»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
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

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE Q.P.T.R.C.

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, en nombre y representación de D/Dª [NOMBRE Y APELLIDOS] con domicilio en [LOCALIDAD], según acredito por certificación del registro electrónico de apoderamientos judiciales que acompaño (o mediante designación apud acta ante el/la Letrado/a de la Administración de Justicia de [SEDE], bajo la dirección letrada de D/Dª [NOMBRE Y APELLIDOS], Abogado/a del Iltre. Colegio de [LOCALIDAD], ante el Tribunal comparezco y como mejor en derecho proceda DIGO:

Que por medio del presente escrito formulo demanda de juicio ordinario en ejercicio de los derechos derivados de la extinción de la relación de pareja estable frente al demandado D. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], fundado mi pretensión en los siguientes:

HECHOS

Mi representado y el demandado D. [NOMBRE Y APELLIDOS], ambos de vecindad civil [VECINDAD CIVIL] han mantenido una relación de pareja de hecho desde el año [AÑO], habiendo tenido un hijo en común, en la actualidad mayor de edad, nacido el día [FECHA] según acredito mediante libro de familia y certificado literal de nacimiento del hijo común que acompaño como documentos número

Ambas partes y el hijo común vienen residiendo desde entonces en la vivienda familiar sita en [LOCALIDAD],propiedad pro indiviso de ambas partes, respecto de la cual se peticionarán las correspondientes medidas cautelares en el otrosí de este escrito.

En fecha [FECHA] y por motivos personales, se produjo la extinción de la convivencia entre la pareja constituida por mi representada y por el demandado, quien ha iniciado una relación sentimental con una tercera persona.

La situación de convivencia es totalmente insostenible, puesto que el demandado, si bien sigue pernoctando en la vivienda familiar, se ha despreocupado absolutamente de los alimentos y necesidades del hijo común, a la vez que observa una conducta totalmente despectiva en relación a mi representada.

En la presente demanda se pretende que se atribuya el uso de la vivienda familiar a mi representada y al hijo común, en tanto que éste no pueda independizarse, y que se fije una compensación económica a favor de mi representada por importe de [IMPORTE] euros en aplicación del principio de enriquecimiento injusto.

En primer lugar, y en cuanto a la atribución del uso de la vivienda familiar, se insta esta medida de atribución del uso de la vivienda de cotitularidad de ambos convivientes a favor de mi mandante y del hijo común, por ser consecuencia necesaria de la aplicación del principio de prohibición de enriquecimiento injusto, según se expondrá seguidamente, y por ser el interés de mi mandante, y del hijo común, el más necesitado de protección, por cuanto que en el domicilio vive dicho hijo común mayor de edad, que en la actualidad está cursando estudios de [ESTUDIOS QUE CURSA], cuya relación con el padre está totalmente deteriorada según se acreditará oportunamente mediante la proposición de la prueba testifical, y el cual ha demandado al padre por alimentos ante su absoluta falta de colaboración económica y personal en la educación del hijo común.

En segundo lugar, se solicita una compensación económica a favor de mi representada, puesto que se dan los requisitos expresados en la STS de 27 de marzo de 2001, rec. 919/1996, en relación a las uniones de hecho, máxime las de larga duración, como la presente, con apoyo en el enriquecimiento injusto, a favor de aquel conviviente que, sin retribución o con retribución insuficiente, haya trabajado para el hogar común, o para el otro conviviente, en caso de que se haya generado por este motivo una situación de desigualdad entre el patrimonio de los dos que implique un enriquecimiento injusto.

En este caso, y según se acreditará en este proceso, mi representada, ama de casa, ha dedicado todos estos años de convivencia al trabajo en el hogar familiar y al cuidado y educación del hijo común, en tanto que el demandado se dedicaba a su trabajo profesional, con una alta remuneración económica que sólo en parte revertía en la pareja e hijo, puesto que el demandado ingresaba en la cuenta común una cantidad de [IMPORTE] euros mensuales, al efecto de cubrir los gastos de vivienda y de manutención del familia, lejos de los [IMPORTE] euros mensuales en que pueden cifrarse sus ingresos durante todo este periodo de tiempo (se acompañan como documentos [Nº DE DOCUMENTO] extractos de cuenta bancaria número [NÚMERO] de titularidad común, declaraciones del IRPF del demandado, nóminas del demandado, certificado de la inscripción de la actora como demandante de empleo [Nº DE DOCUMENTO]).

Por tanto, se ha generado una situación de desequilibrio que perjudica a la demandante y que beneficia al demandado, lo cual nos lleva a reclamar la cantidad de [IMPORTE] euros por el desajuste económico que se ha producido en todo este tiempo de convivencia común.

Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento nº [Nº DE DOCUMENTO]

A estos hechos son de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

Competencia

Es competente este Tribunal, de conformidad con lo previsto en el artículo 49 y 52 de la LEC, en relación con lo dispuesto en el art. 85.1º LOPJ.

Procedimiento

Deben seguirse los trámites del proceso ordinario conforme al art. 249.2 de la LEC al ser la cuantía reclamada superior a 15.000 euros.

Legitimación activa y pasiva

La ostentan ambas partes por su relación de pareja de hecho.

Cumplimiento de los requisitos de procedibilidad

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

Medidas

La STS Sala 1ª de 27 de marzo de 2001, rec. 919/1996, expresa la doctrina de la Sala indicando que ha tenido buen cuidado en admitir que las uniones de hecho, máxime las de larga duración, pueden en ocasiones ser causa legítima de alguna reclamación, bien por aportación a la creación de un patrimonio, o con apoyo en el enriquecimiento injusto o en algún otro precepto incluso aplicable por analogía.

En este caso, nos hallamos ante un supuesto de extinción de la pareja estable no casada en la cual, con fundamento en el enriquecimiento injusto, se interesa la atribución de la vivienda familiar a la madre y al hijo común, mayor de edad, y que se fije una compensación económica por importe de [IMPORTE] euros.

Con arreglo a lo establecido en el art. 394 de la LEC procede imponer las costas de este proceso a la parte demandada.

Por cuanto antecede,

SUPLICO AL TRIBUNAL: Que tenga por presentada esta demanda, con su copia y documentos que la acompañan, que la admita y que me tenga por personado y parte en la representación que ostento de [NOMBRE Y APELLIDOS] en virtud de la escritura de poder general para pleitos cuya devolución intereso previa unión a los autos de copia testimoniada (o designa apud acta), que se entiendan conmigo las sucesivas diligencias de proceso ordinario y que, en su día y tras los trámites legales, se dicte sentencia por la que se estime la demanda y en su virtud:

1) se atribuya el uso de la vivienda familiar sita en [LOCALIDAD] a la madre y al hijo común en tanto que éste siga viviendo en el domicilio.

2) se condene al demandado [NOMBRE Y APELLIDOS] a indemnizar a mi representada en la cantidad de [IMPORTE] euros, en ambos casos más los intereses correspondientes, en concepto de extinción de la relación de pareja de hecho.

3) se impongan expresamente las costas a la parte demandada.

OTROSÍ I DIGO: Que fijo la cuantía del proceso en la cantidad de [IMPORTE] euros.

Por lo que SUPLICO AL TRIBUNAL tenga por hecha la citada manifestación a los efectos oportunos.

OTROSÍ II DIGO por medio del presente y al amparo de lo dispuesto en el artículo 730 de la LEC en relación con el artículo 727.11ª de la LEC, solicito la adopción de la MEDIDA CAUTELAR DE ATRIBUCIÓN DEL USO DE LA VIVIENDA FAMILIAR A MI REPRESENTADA EN TANTO QUE EL HIJO COMÚN D [NOMBRE DEL HIJO/A] RESIDA EN EL DOMICILIO, en base a los siguientes:

HECHOS

PRIMERO.- Que, tal como se ha relatado en la demanda, la relación de convivencia de hecho de las partes se ha deteriorado extraordinariamente, especialmente respecto de la relación del padre con el hijo común, quienes no tienen ningún tipo de contacto personal, habiéndose despreocupado el padre de las obligaciones con su hijo. Asimismo, la dedicación exclusiva de mi mandante al hogar y al hijo común son elementos que patentizan una clara situación de enriquecimiento injusto a favor del demandado.

SEGUNDO.- El deterioro de la convivencia entre la pareja está generando una situación de grave conflicto personal, que repercute especialmente de forma negativa en el hijo común de la pareja, quien no se habla con su padre, al cual ha demandado en solicitud de prestación alimenticia, habiendo observado una clara disminución del rendimiento escolar como consecuencia de estos hechos, a la vez que han existido enfrentamientos verbales graves entre los miembros de la pareja y entre el hijo y el padre, como consecuencia de la actitud negativa de éste.

TERCERO.- Para acreditar los anteriores hechos, y al amparo de lo que dispone el artículo 732.2 de la LEC, se acompañan a esta demanda los documentos en que esta parte funda su derecho, relacionados en los hechos de este otrosí, interesándose, además, la práctica de los siguientes medios probatorios en orden a justificar la concurrencia de los presupuestos para la adopción de la medida cautelar:

- TESTIFICAL, a fin de que se cite al hijo común D. [NOMBRE Y APELLIDOS], quien comparecerá voluntariamente, a efectos que declare sobre la situación de convivencia con el padre, actitud de éste, ingresos y dedicación familiar y profesional de sus progenitores.

A los anteriores hechos son de aplicación los siguientes

PRIMERO.- FUNDAMENTOS DE DERECHO

PRIMERO.- Competencia.- Le corresponde al Tribunal al que me dirijo ya que es aquel ante el que se ha presentado la demanda principal (art. 723.1 LEC).

SEGUNDO.- Legitimación.- Le corresponde a esta parte ante su condición de demandante en las presentes actuaciones (art 721 LEC).

TERCERO.-Procedimiento.-Es el previsto en los arts. 733 y 734 LEC solicitando que la vista se celebre y la medida se adopte con la mayor urgencia dados los gravísimos perjuicios que está sufriendo mi representada y su hijo.

CUARTO.-Apariencia de buen derecho.-Se deriva de la documentación adjunta a esta solicitud (art. 728.2 LEC).

QUINTO.-Peligro de mora.-Se deriva de la grave alteración de la convivencia personal y familiar como consecuencia de la actitud del demandado, tal como resulta expuesto en los hechos de este otrosí (art. 728.1 LEC).

SEXTO.-Medida interesada.-Es la de la atribución provisional del uso de la vivienda familiar a mi representada en tanto que el hijo común resida en dicho domicilio con fundamento en lo dispuesto en el art. 727.11 de la LEC.

SÉPTIMO.-Caución.-Con fundamento en el art. 732.3 LEC se solicita sea fijada ésta en [IMPORTE] euros dado que la vivienda es de titularidad proindiviso de ambas partes, la situación personal y familiar y los posibles perjuicios que se les pudieren generar por ello.

En base a lo anterior,

SUPLICO AL TRIBUNAL: Que tenga por presentada solicitud con los documentos acompañados y que, tras los trámites legales, incluida la práctica de la prueba que dejo interesada en el hecho tercero de este otrosí, acuerde la atribución provisional del uso de la vivienda familiar sita en [LOCALIDAD] a mi representada en tanto que el hijo común D [NOMBRE DEL HIJO/A] resida en dicho domicilio. De cara a la adopción de tal medida cautelar se solicita asimismo que se tenga por ofrecida una caución de [IMPORTE] euros.

FUNDAMENTOS DE DERECHO

PRIMERO.- Competencia.- Le corresponde al Tribunal al que me dirijo ya que es aquel ante el que se ha presentado la demanda principal (art. 723.1 LEC).

SEGUNDO.- Legitimación.- Le corresponde a esta parte ante su condición de demandante en las presentes actuaciones (art 721 LEC).

TERCERO.- Procedimiento.-Es el previsto en los arts. 733 y 734 LEC solicitando que la vista se celebre y la medida se adopte con la mayor urgencia dados los gravísimos perjuicios que está sufriendo mi representada y su hijo.

CUARTO.- Apariencia de buen derecho.-Se deriva de la documentación adjunta a esta solicitud (art. 728.2 LEC).

QUINTO.- Peligro de mora.-Se deriva de la grave alteración de la convivencia personal y familiar como consecuencia de la actitud del demandado, tal como resulta expuesto en los hechos de este otrosí (art. 728.1 LEC).

SEXTO.- Medida interesada.-Es la de la atribución provisional del uso de la vivienda familiar a mi representada en tanto que el hijo común resida en dicho domicilio con fundamento en lo dispuesto en el art. 727.11 de la LEC.

SÉPTIMO.- Caución.-Con fundamento en el art. 732.3 LEC se solicita sea fijada ésta en [IMPORTE] euros dado que la vivienda es de titularidad proindiviso de ambas partes, la situación personal y familiar y los posibles perjuicios que se les pudieren generar por ello.

En base a lo anterior,

SUPLICO AL TRIBUNAL: Que tenga por presentada solicitud con los documentos acompañados y que, tras los trámites legales, incluida la práctica de la prueba que dejo interesada en el hecho tercero de este otrosí, acuerde la atribución provisional del uso de la vivienda familiar sita en [LOCALIDAD] a mi representada en tanto que el hijo común D [NOMBRE DEL HIJO/A] resida en dicho domicilio. De cara a la adopción de tal medida cautelar se solicita asimismo que se tenga por ofrecida una caución de [IMPORTE] euros.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma de Abogado y Procurador

========================================================================
