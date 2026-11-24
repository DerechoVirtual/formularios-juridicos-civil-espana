---
name: demanda-contenciosa-sobre-relaciones-paternofiliales-civ-0309
description: "Demanda contenciosa sobre relaciones paternofiliales tras ruptura de pareja de hecho. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda contenciosa sobre relaciones paternofiliales tras ruptura de pareja de hecho

> Formulario **CIV-0309** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Demanda contenciosa para regular los efectos respecto de un hijo menor tras la ruptura de una pareja de hecho (guarda y custodia, visitas, uso de la vivienda familiar y alimentos), por el cauce del art. 748.4.º LEC, con solicitud de medidas provisionales por otrosí (arts. 770.6.ª y 773 LEC) y adaptada al requisito de procedibilidad de la LO 1/2025.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda contenciosa sobre relaciones paternofiliales tras ruptura de pareja de hecho» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda contenciosa sobre relaciones paternofiliales tras ruptura de pareja de hecho” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-contenciosa-sobre-relaciones-paternofiliales-civ-0309`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (8 veces)
- [ ] LOCALIDAD (7 veces)
- [ ] Nº DE DOCUMENTO (7 veces)
- [ ] AÑO (6 veces)
- [ ] DOMICILIO (6 veces)
- [ ] DÍA (4 veces)
- [ ] MES (4 veces)
- [ ] NOMBRE DEL MENOR (4 veces)
- [ ] NOMBRE Y APELLIDOS DEL DEMANDADO (4 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] FIRMA (2 veces)
- [ ] HORA (2 veces)
- [ ] CENTRO EDUCATIVO
- [ ] DNI/NIE
- [ ] DOCUMENTO QUE ACREDITA LA ACTIVIDAD NEGOCIADORA
- [ ] DOMICILIO PROFESIONAL
- [ ] EDAD
- [ ] INDICAR EL MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS
- [ ] LUGAR DONDE RESIDE
- [ ] LUGAR O PERSONAS CON QUIENES RESIDE
- [ ] NOMBRE Y APELLIDOS
- [ ] NOMBRE Y APELLIDOS DEL ABOGADO/A
- [ ] NOMBRE Y APELLIDOS DEL DEMANDANTE
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] Nº
- [ ] Nº DE COLEGIADO
- [ ] NÚMERO
- [ ] SEDE

## Normas que cita el formulario

- art. 769.3 LEC
- art. 1.2 Real Decreto 1322/1981
- art. 154 CC
- art. 749.2 LEC
- art. 748.4.º LEC
- art. 753 LEC
- art. 769 LEC
- art. 142 CC
- art. 437.1 LEC
- art. 5 Ley Orgánica 1/2025
- art. 159 CC
- art. 110 CC
- art. 143 CC
- art. 146 CC
- art. 96 CC
- art. 394 LEC
- art. 770.6.ª LEC
- art. 771 LEC
- art. 773.3 LEC
- art. 103 CC
- art. 748.4 LEC
- art. 96 Código Civil

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

- Junto a «…el derecho de goce de la vivienda junto con el progenitor con ellos conviviente.»: el art. 96 CC ha sido modificado por la Ley 8/2021; comprobar la redacción vigente antes de entrecomillarlo.

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
SECCIÓN CIVIL – SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, que actúa en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDANTE], provisto/a de DNI n.º [DNI/NIE], con domicilio en [LOCALIDAD], calle [DOMICILIO], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento n.º [Nº DE DOCUMENTO], bajo la dirección del/de la Letrado/a D./Dña. [NOMBRE Y APELLIDOS DEL ABOGADO/A], colegiado/a n.º [Nº DE COLEGIADO] del Ilustre Colegio de la Abogacía de [LOCALIDAD], cuyo despacho se abre en [DOMICILIO PROFESIONAL], ante el Tribunal comparezco y, como mejor en Derecho proceda (véase nota 1), DIGO:

Que por medio del presente escrito, siguiendo las instrucciones de mi mandante, vengo a formular DEMANDA CONTENCIOSA SOLICITANDO LA REGULACIÓN DE LOS EFECTOS RESPECTO A SU HIJO/A MENOR DERIVADOS DE LA RUPTURA DE UNA PAREJA DE HECHO, frente a D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDADO], con domicilio en [DOMICILIO], y el Ministerio Fiscal.

La demanda se basa en los siguientes:

HECHOS

PRIMERO.– Mi patrocinado/a y D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDADO] mantuvieron una relación de pareja semejante a la de los casados entre los años [AÑO] y [AÑO], cuando, por desavenencias que no vienen al caso, se puso fin a la misma, habiendo convivido en relación afectiva semejante a la de las parejas casadas en la vivienda adquirida por ambos sita en calle [DOMICILIO], n.º [Nº], de [LOCALIDAD], como se acredita mediante certificados municipales de empadronamiento y escritura de compraventa de la citada vivienda, que se aportan como DOCUMENTOS N.º [Nº DE DOCUMENTO], siendo este el último domicilio en el que el demandante y el demandado convivieron.

SEGUNDO.– Fruto de dicha unión nació el [DÍA] de [MES] de [AÑO] un/a hijo/a, de nombre [NOMBRE DEL MENOR], por consiguiente menor de edad, como se demuestra con la certificación registral que se aporta como DOCUMENTO N.º [Nº DE DOCUMENTO], en el que consta el reconocimiento del padre dentro del plazo de inscripción.

TERCERO.– Desde el día [DÍA] de [MES] de [AÑO] cesó la convivencia entre mi patrocinado/a y el hoy demandado D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDADO], habiendo abandonado este último el domicilio que la pareja venía compartiendo, trasladándose a vivir con [LUGAR O PERSONAS CON QUIENES RESIDE] en [LOCALIDAD], que es el domicilio arriba reseñado.

CUARTO.– D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDADO] tiene un trabajo fijo y estable en la empresa [DENOMINACIÓN SOCIAL], sita en [LOCALIDAD], calle [DOMICILIO], percibiendo un sueldo mensual de [IMPORTE] euros, además de [NÚMERO] pagas extraordinarias por importe cada una de ellas de [IMPORTE] euros. Se acompaña como DOCUMENTO N.º [Nº DE DOCUMENTO] copia de la última nómina a la que ha tenido acceso mi representado/a (o cualquier otro medio de prueba de que se disponga y, en otro caso, solicitar en este momento su práctica por medio de oficios a los órganos correspondientes: a la Tesorería General de la Seguridad Social, a la Agencia Tributaria, etc.).

Mi patrocinado/a [DESCRIBIR SU SITUACIÓN LABORAL Y ECONÓMICA: cualificación profesional, ocupación y recursos. Ejemplo del modelo original: carece de cualificación profesional y únicamente obtiene ingresos esporádicos en trabajos ocasionales en la hostelería, percibiendo actualmente [IMPORTE] euros mensuales correspondientes a su salario como trabajador/a eventual en la empresa [DENOMINACIÓN SOCIAL]]. Se adjunta certificación de haberes como DOCUMENTO N.º [Nº DE DOCUMENTO].

Por lo que respecta a las necesidades del/de la hijo/a menor, se desglosan en los siguientes conceptos:

a) Educación: el/la menor, que cuenta en la actualidad con [EDAD] años de edad, acude a [CENTRO EDUCATIVO], debiendo abonar en concepto de pago por asistencia una cantidad de [IMPORTE] euros mensuales.

b) Vestido: [IMPORTE] euros.

c) Otros gastos (actividades extraescolares o complementarias, ocio, transporte): [IMPORTE] euros.

Se aportan para justificar los gastos referidos los DOCUMENTOS N.º [Nº DE DOCUMENTO].

QUINTO.– Por todo el relato fáctico expuesto, y puesto que han resultado infructuosos todos los intentos pacíficos de solucionar la situación ante las continuas promesas incumplidas por el demandado, interesa al derecho de mi mandante garantizar el ejercicio de la guarda y custodia de su hijo/a menor, dada la irregular situación familiar planteada y el perjuicio que se le pueda irrogar en su desarrollo afectivo y emocional, y garantizar los derechos económicos que le asisten, viéndose obligado/a a la interposición de esta demanda ante la negativa del demandado a abonar cantidad alguna en este concepto.

SEXTO.– Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [INDICAR EL MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento n.º [Nº DE DOCUMENTO] [DOCUMENTO QUE ACREDITA LA ACTIVIDAD NEGOCIADORA].

FUNDAMENTOS DE DERECHO

I.– COMPETENCIA

Conforme a lo establecido en el art. 769.3 LEC (en su caso, en relación con el art. 1.2 del Real Decreto 1322/1981, de 3 de julio), como fuero de competencia territorial se fija la circunscripción del Tribunal competente para conocer del proceso en el partido del último domicilio común de los progenitores.

II.– PARTES

La legitimación activa y pasiva para intervenir en el procedimiento corresponde a ambos progenitores, habida cuenta de que son los que se hallan en la situación jurídica respectiva del derecho-deber de velar por los hijos menores no emancipados y alimentarlos (art. 154 CC). Con arreglo al art. 749.2 LEC, deberá ser parte el Ministerio Fiscal, por existir hijos menores.

III.– PROCEDIMIENTO

Conforme a lo establecido en el art. 748.4.º LEC, las pretensiones que versan exclusivamente sobre guarda y custodia de hijos menores y sobre alimentos reclamados por un progenitor contra el otro en nombre de tales hijos se incluyen en el ámbito de aplicación del Título I del Libro IV y se sustancian conforme al modelo de proceso especial del art. 753 LEC, que es juicio verbal con contestación escrita.

Una interpretación amplia lleva, sin embargo, para integrar todos los efectos que con relación a los hijos menores de edad deben regularse necesariamente al producirse el cese de la convivencia, a entender que los conceptos de custodia, visitas y alimentos integran el concepto general de patria potestad. Asimismo, con relación a la atribución del uso de la vivienda, viene aceptándose mayoritariamente por los tribunales, con relación a los hijos menores extramatrimoniales, como integrante del concepto más amplio de alimentos.

Como indica la SAP Baleares, Secc. 4.ª, de 9 de julio de 2002, rec. 233/2002: «si bien la letra del artículo 748.4 de la Ley de Enjuiciamiento Civil dice que el procedimiento debe versar exclusivamente sobre la guarda y custodia de los hijos o sobre alimentos, ello no es así en la praxis judicial, sino que también en estos procesos se dirimen otros temas, como el uso de la vivienda, el régimen de visitas y cualquier otra cuestión pendiente que surja, como si se tratara de procedimiento de separación conyugal».

Así se mantiene también en la SAP Barcelona, Secc. 18.ª, de 17 de enero de 2003, rec. 32/2002:

«Por lo que se refiere a la excepción de inadecuación de procedimiento, la fundamenta en que el art. 748.4.º solo se refiere a los pleitos que versen exclusivamente sobre la guarda y custodia o sobre los alimentos a los hijos menores, y habiéndose reclamado la atribución del uso de la vivienda y régimen de visitas, el procedimiento adecuado sería el ordinario de acuerdo con dicha nueva regulación. Pues bien, entendemos que de conformidad con dicho precepto, este es el procedimiento adecuado por establecerlo expresamente el mismo en relación con los arts. 769, 770 y 771 LEC, no siendo óbice que no toquen el tema de la vivienda, a la vista de lo que abajo se dirá por la existencia de un menor […]. A este respecto, la sentencia del TS de 16-12-1996, rec. 2016/1993, y la más reciente de 10-3-1998, rec. 133/1994, señalan que las normas que sobre la vivienda familiar contiene el CC en relación al matrimonio y sus crisis, entre ellas la ruptura del vínculo, se proyectan más allá de su estricto ámbito, a situaciones como la convivencia prolongada entre un hombre y una mujer como pareja, ya que las razones que abonan y justifican aquellas valen también para este último caso si existen hijos comunes, supuesto en el cual la eventual asignación se haría en favor de tal hijo común y dentro del específico concepto de alimentos. Visto pues, que puede hacerse tal atribución, puesto que la guarda y custodia se atribuye a la madre, la vivienda debería atribuirse a la misma e hijo […]».

Y en la más reciente SAP Orense, Secc. 1.ª, de 4 de febrero de 2004, rec. 187/2003:

«El apartado 4 del art. 748, antes transcrito, no alude a procesos u uniones matrimoniales, por lo que nada obsta para estimar incluidas en su ámbito las pretensiones sobre guarda, custodia y alimentos (incluyendo vivienda por la alusión que el art. 142 CC efectúa a "habitación" dentro del concepto de alimentos) cuando se trata de progenitores no ligados por vínculo conyugal […]».

IV.– CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4.º y 399.3 LEC, en relación con el art. 437.1 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

V.– FONDO DEL ASUNTO

Resulta obvia la existencia de la denominada sociológicamente «unión de hecho», que, como familia natural, debe ser merecedora, como dice la STS, Sala 1.ª, de 29 de octubre de 1997, rec. 2892/1993, de la misma protección por parte de los poderes públicos que para la familia jurídica establece el art. 39.1 de la Constitución Española, sobre todo cuando de dicho texto no se desprende que haya una sola forma de familia reconocida.

Además, la realidad social indica que tales uniones dan las características básicas de la familia jurídica, con la única particularidad de no existir una formalización religiosa o civil de tal unión de hecho.

Y así la STS de 18 de mayo de 1992, que cita la de 13 de junio de 1986 y la de 14 de julio de 1988, así como la del Tribunal Constitucional de 4 de abril de 1991, afirma que «las uniones libres, aunque están carentes de precisa normativa, no por eso son totalmente desconocidas por nuestro ordenamiento jurídico. La Constitución no lo prevé, pero tampoco expresamente las interdicta y rechaza, y así se desprende de su art. 32 en relación al 39 que se proyecta a la protección de la familia en forma genérica, es decir, como núcleo creado tanto por el matrimonio como por la unión de hecho».

Se reconoce jurisprudencialmente no solo la existencia social de estas uniones, sino que las mismas constituyen una integración familiar defendible y que crea derechos y obligaciones entre sus miembros, derechos que son trascendentes, por ejemplo, en materia de arrendamientos urbanos.

Incluso en el derecho comparado afín, el Tribunal de Casación de Italia vino a reconocer, en su sentencia de 2 de febrero de 1977, la denominada «famiglia di fatto», como entidad social que ejercita unas funciones en la educación y mantenimiento de sus miembros y que debe ser protegida a tenor de lo dispuesto en el art. 2 de la Constitución italiana.

Más recientemente, en el ámbito autonómico, se han dictado leyes de parejas estables en diversas Comunidades que reconocen los mismos derechos para este tipo de relaciones paramatrimoniales que para los matrimonios.

Mis representados formaron familia natural constituida por ellos mismos y su hijo/a y, por lo ya expuesto, se separaron, debiendo ahora regularse, a través de la adopción de las medidas necesarias, sus obligaciones y derechos con respecto a su hijo/a menor.

Guarda y custodia del menor.

El art. 159 CC previene que, si los padres viven separados y no decidieren de común acuerdo, el Juez decidirá, siempre en beneficio de los hijos, al cuidado de qué progenitor quedarán los hijos menores de edad.

Es claro que la guarda del hijo no es un derecho subjetivo del padre o de la madre, y que las medidas relativas al cuidado de los hijos menores de edad deben ser adoptadas siempre en su beneficio, como ha manifestado reiteradamente la jurisprudencia, prevaleciendo siempre el bienestar de los mismos.

En el caso presente el/la progenitor/a demandante está en una disposición correcta para ocuparse de su hijo/a; es natural su convivencia con el/la menor; y el otro progenitor no ha asumido realmente sus deberes paterno-filiales.

Alimentos del menor

Uno de los deberes fundamentales del titular de la patria potestad es la alimentación de los hijos (art. 154, párrafo segundo, 1.º CC), deber que se deriva de la relación paterno-filial hasta el punto de que la mantiene aun en los casos de privación de la patria potestad (art. 110 CC). Este deber-función se traduce en la obligación de prestar alimentos establecida en los arts. 143, 144 CC y concordantes del Código Civil.

El/La hijo/a [NOMBRE DEL MENOR] tiene una edad en la que progresivamente se van ampliando sus necesidades, tanto escolares como de mantenimiento y educación, que son esenciales para su formación.

La cantidad que se solicita resulta ajustada a las necesidades del/de la menor, puesto que los alimentos comprenden todo lo que es indispensable para el sustento, habitación, vestido y asistencia médica, así como también la educación, con arreglo a lo establecido en el art. 142 CC, y su cuantía debe ser proporcional al caudal o medios de quien los da y a las necesidades de quien los recibe, a tenor del art. 146 CC, siendo deber de los progenitores el procurar una formación integral de los hijos.

Mientras que el demandado es un profesional que disfruta de una buena situación económica, mi representado/a tiene unos ingresos económicos limitados, más allá de la pequeña contribución de sus padres, y no puede hacer frente por sí solo/a a todos los gastos de mantenimiento y escolaridad, que son cada día más cuantiosos.

Todo ello conforme con el criterio de protección y salvaguardia de los intereses de los hijos que inspira toda nuestra normativa positiva, no siendo lícito a uno de los progenitores abandonar sus deberes de asistencia y alimentos que le incumben respecto a los mismos, haciéndolos recaer exclusivamente sobre el otro progenitor.

Por todo ello, interesa al derecho de mi mandante garantizar los derechos económicos que le asisten al/a la hijo/a menor de ambos progenitores, viéndose obligado/a a solicitar amparo jurídico ante la negativa del demandado a asumir las obligaciones que legalmente le corresponden.

Atribución del uso de la vivienda familiar.

Existiendo hijos comunes, resulta aplicable analógicamente el art. 96 CC a los supuestos de ruptura de la convivencia more uxorio, por cuanto los menores representan el interés preferente más necesitado de protección, razonando que esta atribución del uso de la vivienda común al progenitor custodio tiene su fundamento en la protección y beneficio del menor, en aras a garantizar el mejor ejercicio de la patria potestad por parte de quien asuma las funciones de guarda y compañía, que es independiente del hecho de que su nacimiento sea matrimonial o no matrimonial.

De conformidad con lo dispuesto en el art. 96 CC, párrafo primero, «en defecto de acuerdo de los cónyuges aprobado por el Juez, el uso de la vivienda familiar […] corresponde a los hijos y al cónyuge en cuya compañía queden», precepto que, inspirado en el principio favor filii, supedita al interés más necesitado de protección la concesión del uso de la vivienda familiar; por lo que es de justicia su extensión analógica a los supuestos de los hijos habidos en una relación de convivencia análoga a la matrimonial, de donde resulta que son los hijos menores los titulares del derecho de goce de la vivienda junto con el progenitor con ellos conviviente.

En sentido favorable se muestra la práctica totalidad de la doctrina y de la jurisprudencia menor.

Entre los pronunciamientos más recientes, el de la SAP Badajoz, Secc. 1.ª, de 28 de mayo de 2003, rec. 201/2002, que declara que: «considerando que los verdaderos titulares del disfrute de la vivienda familiar son los hijos y, por extensión, y en contemplación a ellos, el progenitor en cuya compañía queden (art. 96 CC). Si a ello le unimos el dato de que la madre carece de otra vivienda y que con ella permanecerá el menor así como los mayores, aunque se dice que estos permanecen en parte en otro domicilio de Badajoz, la Sala considera que la atribución del uso de la vivienda familiar debe de hacerse a la Sra. […] al menos hasta que el hijo menor de edad adquiera la mayoría de edad»; o el de la SAP Madrid, Secc. 22.ª, de 11 de julio de 2003, rec. 182/2003, para la que: «dada la plena equiparación de los hijos ante la Ley (artículo 39 de la Constitución), al artículo 96 del citado Código, en orden a la atribución de uso de la vivienda familiar, en cuanto uno de los componentes de la obligación alimenticia». Añadiendo la SAP Castellón de 9 de abril de 2003, rec. 329/2002 que: «si examinamos el caso litigioso desde la perspectiva del artículo 39 de la Constitución, que dispone que los poderes públicos han de asegurar la protección integral de la familia (apartado 1), así como la protección integral de los hijos, que son iguales ante la ley con independencia de su filiación (ap. 2), así como que los padres han de prestar asistencia a los hijos habidos dentro o fuera del matrimonio, durante su minoría de edad y en los demás casos en que legalmente proceda (ap. 3), es clara la razón de la aplicación analógica del artículo 96 CC a las uniones de hecho. Obsérvese que este precepto no dice a cuál de los cónyuges ha de asignarse la vivienda que fue familiar, ya que su principal designio es su atribución a los hijos, dependiendo que pase a usarla uno u otro de los cónyuges del hecho de que los hijos habidos de la unión queden en su compañía ("a los hijos y al cónyuge en cuya compañía queden", dice el artículo 96 CC)».

VI.– COSTAS

Las costas procesales deben ser impuestas a la parte demandada, por criterio del íntegro vencimiento, en atención al art. 394 LEC.

En virtud de lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito con los documentos que se acompañan y sus copias, se digne admitirlos, tenerme por comparecido/a y parte en la representación que ostento y, seguido que sea el procedimiento por sus pertinentes trámites, con citación del Ministerio Fiscal, se sirva dictar Sentencia por la que, estimando la presente demanda:

a) Se atribuya al/a la progenitor/a actor/a la guarda y custodia del/de la hijo/a menor [NOMBRE DEL MENOR], manteniéndose el ejercicio de la patria potestad compartida por ambos progenitores.

b) Se fije un derecho de visitas conforme al que el progenitor demandado podrá tener en su compañía al/a la menor los fines de semana alternos desde las [HORA] horas del sábado a las [HORA] horas del domingo, así como la primera mitad de las vacaciones escolares de Navidad, Semana Santa y Verano los años pares, y la segunda mitad los años impares.

c) Se atribuya el uso exclusivo de la vivienda familiar sita en la calle [DOMICILIO] al/a la demandante y al/a la menor, así como del ajuar doméstico en ella existente, pudiendo el demandado, previo inventario, retirar del mismo sus ropas y enseres de uso personal y necesario, para el supuesto de que no lo haya verificado.

d) Se condene al demandado a abonar al/a la actor/a, en concepto de alimentos para el/la hijo/a menor [NOMBRE DEL MENOR], la suma mensual de [IMPORTE] euros, que habrá de hacer efectivos al progenitor custodio en la cuenta corriente que este designe, por meses anticipados, dentro de los cinco primeros días de cada mes, y que habrá de ser actualizada anualmente según las variaciones que experimente el Índice de Precios al Consumo emitido por el Instituto Nacional de Estadística, u organismo que lo supla.

Todo ello con expresa imposición de las costas procesales al demandado si resiste la pretensión.

Es de Justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

OTROSÍ DIGO: Que, al amparo del art. 770.6.ª LEC, se solicitan mediante el presente escrito MEDIDAS PROVISIONALES, en base a los siguientes:

HECHOS

ÚNICO.– Se tienen por reproducidos los hechos de la pretensión principal, debiendo destacarse que el/la hijo/a menor ha estado siempre en compañía del progenitor actor, mi mandante, y es lo conveniente que continúe con él/ella, pareciendo suficiente la comunicación y estancia, sin pernocta, del otro progenitor, en [LUGAR DONDE RESIDE], los sábados de todas las semanas, por lo menos hasta la resolución definitiva. Por otro lado, puesto que el interés familiar más necesitado de protección es el de los hijos en potestad, tanto el/la menor como mi representado/a deben continuar en el uso de la vivienda familiar.

FUNDAMENTOS DE DERECHO

I.– El procedimiento adecuado es el de la comparecencia del art. 771 LEC para medidas previas, conforme a la remisión del art. 773.3 LEC, que a su vez es uno de los cauces a que se refiere el art. 770.6.ª LEC.

II.– Esta pretensión consiste en la adopción, de acuerdo con las reglas de la analogía, de las medidas del art. 103 CC y concordantes, derivadas de la tutela cautelar por la lesión que, de no adoptarse, pueden padecer las partes y los hijos menores por la duración del proceso, una vez llegado el caso de la ruptura de la vida en común en análoga relación a la marital.

En su virtud,

SUPLICO AL TRIBUNAL

que, teniendo por causadas las precedentes manifestaciones a los efectos oportunos, y por deducida solicitud de adopción de medidas provisionales, seguido que sea su pertinente trámite, se dicte Auto por el que se aprueben las siguientes:

a) Atribución provisional de la guarda y custodia del/de la hijo/a menor al/a la actor/a D./Dña. [NOMBRE Y APELLIDOS].

b) Fijación de un derecho provisional de comunicación y visita del demandado a su hijo/a todos los sábados de cada semana de diez a veinte horas.

c) Atribución del uso exclusivo de la vivienda familiar sita en la calle [DOMICILIO] al/a la solicitante y al/a la menor, así como del ajuar doméstico en ella existente, pudiendo el demandado, previo inventario, retirar del mismo sus ropas y enseres de uso personal y necesario.

d) Fijación a cargo del demandado de la cantidad de [IMPORTE] euros mensuales en concepto de contribución al sostenimiento del/de la hijo/a menor de edad, que será ingresada, por meses anticipados, dentro de los cinco primeros días de cada mes, en la cuenta bancaria que el/la solicitante designe. Esta cantidad se actualizará anualmente conforme a las variaciones que experimente el Índice de Precios al Consumo emitido por el Instituto Nacional de Estadística, u organismo que lo supla.

Todo ello con condena en costas del incidente si la parte adversa se opusiera.

Es justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Abogado/a: [FIRMA] Firma del Procurador/a: [FIRMA]

NOTA 1 (cauce procedimental del art. 748.4 LEC)

En cuanto al cauce procedimental del art. 748.4 LEC, no hay unanimidad en que en un procedimiento de atribución de la guarda y custodia y fijación de alimentos proceda pronunciarse sobre la atribución de la vivienda familiar. Así, en SAP Asturias, Secc. 7.ª, de 25 de marzo de 2003, rec. 142/2003:

«En lo que debe la Sala revocar la sentencia de instancia es en lo atinente a la atribución de la vivienda familiar común a la madre y su hija, y ello no porque no se repute aplicable, siquiera analógicamente, el art. 96 del Código Civil a las crisis de parejas de hecho como la de autos, sino porque se estima que no es esta cuestión que pueda discutirse en el procedimiento a que se refiere el art. 748.4 de la Ley de Enjuiciamiento Civil.

Como señalábamos en nuestra reciente sentencia de 20 de marzo último, aunque con alguna vacilación hace años (STS de 30-12-1994, rec. 2322/1991), el Tribunal Supremo ha venido admitiendo entre los posibles efectos de la ruptura de una unión de hecho la atribución de la vivienda familiar a quien resultare perjudicado por la crisis de la pareja, existiere o no descendencia (por todas, SSTS de 16-12-1996, rec. 2016/1993; 10-3-1998, rec. 133/1994, o 27-3-2001, rec. 919/1996), ya por considerar aplicable analógicamente el artículo 96 del Código Civil, ya los principios generales que se deducen tanto del citado precepto como de la propia Constitución (artículos 10, 14 y 39), y la jurisprudencia que los interpreta.

Ahora bien, dicho ello debe señalarse también que en todos los casos se trataba de procedimientos de menor cuantía en el que uno de los integrantes de la pareja de hecho litigaba contra el otro para obtener de los Tribunales una declaración sobre los efectos de la ruptura de la convivencia; que ni la L.E.C. 1881 ni la vigente L.E.C. 2000 establecen un procedimiento especial para conocer de ese tipo de pretensiones; que si con la L.E.C. de 1881 y la Ley 11/1981, de 13 de mayo, la cuestión podía resultar discutible, hoy puede sostenerse que el legislador no ha querido dar igual tratamiento procesal a las crisis matrimoniales y a las de las uniones de hecho (opción de política legislativa esta, por cierto, que ha criticado la doctrina, por considerar que se ha desaprovechado la oportunidad de adecuar la normativa procesal a la realidad social de la familia); y que el único procedimiento especial que la L.E.C. 2000 contempla aplicable a supuestos como el que nos ocupa versa "exclusivamente sobre guarda y custodia de hijos menores o sobre alimentos reclamados por un progenitor contra el otro en nombre de los hijos menores", artículo 748.4 de la Ley de Enjuiciamiento Civil.

Pues bien, hallándonos ante un procedimiento del artículo 748.4 de la Ley de Enjuiciamiento Civil, cuyo exclusivo objeto queda definido en los términos expresados, no estima la Sala que proceda pronunciamiento alguno sobre la atribución de la vivienda familiar, ya que, por más amplitud que se quiera conferir a la pretensión alimenticia, y aun cuando las necesidades de vivienda hayan de ser tenidas en consideración para la fijación de la cuantía de la pensión, la referida atribución no forma parte de los alimentos de los hijos, como por otra parte se sigue del hecho de que tanto la legislación sustantiva como la procesal las regulen como efectos distintos y diferenciados de las crisis matrimoniales. Consecuentemente habrán de dilucidar los litigantes de común acuerdo el régimen de uso de la vivienda común, y caso de no alcanzar ninguno deberá decidirse esta cuestión, como otros posibles efectos del cese de la convivencia, en procedimiento ordinario.»
