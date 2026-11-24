---
name: demanda-guarda-custodia-hijos-menores-no-matrimoniales-civ-0311
description: "Demanda de guarda y custodia de hijos menores no matrimoniales con medidas provisionales. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de guarda y custodia de hijos menores no matrimoniales con medidas provisionales

> Formulario **CIV-0311** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Demanda sobre guarda y custodia de hijos menores de edad no matrimoniales, con solicitud de medidas provisionales.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de guarda y custodia de hijos menores no matrimoniales con medidas provisionales» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de guarda y custodia de hijos menores no matrimoniales con medidas provisionales” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-guarda-custodia-hijos-menores-no-matrimoniales-civ-0311`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (6 veces)
- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] Nº DE DOCUMENTO (4 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] CALLE (2 veces)
- [ ] DNI/NIE (2 veces)
- [ ] LUGAR (2 veces)
- [ ] AÑOS DE LA RELACIÓN
- [ ] COLEGIO
- [ ] DIRECCIÓN
- [ ] DOMICILIO
- [ ] ENFERMEDAD
- [ ] FECHA DE NACIMIENTO
- [ ] MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] NOMBRE DE LA ASOCIACIÓN
- [ ] NOMBRE DE LA LIBRERÍA
- [ ] NOMBRE DEL HIJO/A
- [ ] Nº DE COLEGIADO/A

## Normas que cita el formulario

- art. 769.3 LEC
- art. 154 CC
- art. 749.2 LEC
- art. 753 LEC
- art. 437.1 LEC
- art. 5 Ley Orgánica 1/2025
- art. 159 CC
- art. 394 LEC
- art. 770.6.ª LEC
- art. 771 LEC
- art. 773.3 LEC

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

- Junto a «… INSTANCIA SECCIÓN CIVIL SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD DE [LOCALIDAD]»: Denominación legal: Sección de Familia, Infancia y Capacidad. Si no existe en el partido, conoce la Sección Civil o la Única (art. 86.3-4 LOPJ). Fuente: LOPJ arts. 84.2.a) y 86 (redacc. LO 1/2025, BOE-A-2025-76).

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

SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD DE [LOCALIDAD]

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, que actúa en nombre y representación de Dña. [NOMBRE Y APELLIDOS] provista de DNI n.º [DNI/NIE], con domicilio en esta ciudad, calle [CALLE], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño a este escrito, bajo dirección del/ la Letrado/a D./Dña. [NOMBRE Y APELLIDOS], colegiado/a nº [Nº DE COLEGIADO/A] del Iltre. Colegio de Abogados de [COLEGIO], cuyo despacho se abre en [DIRECCIÓN], calle [CALLE], ante el Tribunal comparezco y como mejor en Derecho proceda, DIGO:

Que por medio del presente escrito, siguiendo las instrucciones de mi mandante, vengo a formular demanda sobre GUARDA Y CUSTODIA DE HIJOS MENORES, frente a D. [NOMBRE Y APELLIDOS], con DNI n.º [DNI/NIE], del que se desconoce el paradero actual, siendo el último domicilio conocido el de sus padres, en [DOMICILIO], y el MINISTERIO FISCAL, con base a los siguientes datos y argumentos:

HECHOS

PRIMERO.- Mi patrocinada y D. mantuvieron una relación de pareja semejante a la de los casados entre los años [AÑOS DE LA RELACIÓN], y fruto de la misma nació el [FECHA DE NACIMIENTO], un/a hijo/a, de nombre [NOMBRE DEL HIJO/A], por consiguiente menor de edad, como se demuestra con la certificación registral que hace documento n.º [NÚMERO], en el que consta el reconocimiento del padre dentro del plazo de inscripción.

SEGUNDO.- Mi patrocinada y su compañero han mantenido una vida desarraigada familiar y socialmente, inmersos en el mundo de la toxicomanía, y con una historia de delincuencia habitual asociada, motivo por lo que, desde muy poco después del nacimiento, la hija quedó al cuidado de los padres del demandado D. Se aporta certificado censal del Ayuntamiento de [LOCALIDAD], como documento n.º [NÚMERO].

TERCERO.- Mi patrocinada estuvo ingresada en prisión desde [FECHA] hasta [FECHA], en que ha pasado a tercer grado penitenciario, y habiéndose sometido a un programa de desintoxicación, se encuentra en la actualidad plenamente resocializada, y deseosa de asumir sus responsabilidades materno-filiales. Acompaño certificados del Dr./a. [NOMBRE Y APELLIDOS], y de la Asociación [NOMBRE DE LA ASOCIACIÓN], como documentos n.os y [Nº DE DOCUMENTO].

CUARTO.- El demandado nunca ha tenido realmente en su compañía a su hija, de la que está desentendido por completo, si bien, cuando mi mandante ha solicitado comunicar con su hija, a partir de [FECHA], los suegros ni siquiera han consentido que la actora ejercite su derecho de visitas.

Conoce mi mandante que su hija está teniendo serios y persistentes problemas de salud, que los abuelos no están sabiendo remediar adecuadamente. Se aporta informe de alta del Centro de Salud de [LOCALIDAD], haciendo documento n.º [NÚMERO].

QUINTO.- La demandante está empleada actualmente como dependiente de la librería [NOMBRE DE LA LIBRERÍA], en relación laboral indefinida. Se adjuntan el contrato de trabajo y último recibo de salarios, como documentos [Nº DE DOCUMENTO] y [Nº DE DOCUMENTO].

SEXTO.- Mi mandante ha apurado todos los procedimientos a su alcance para lograr que se asuma su derecho a la guarda de la hija común, estando los suegros utilizando a su hijo, que apenas aparecía por la casa donde se hallaba la hija -ahora, no se conoce que viva en ella-, para negar el acceso a la madre, lo que no es difícil, dada la dependencia a la heroína y su desequilibrio de la personalidad concurrente en el demandado. Acompaño carta recibida del demandado de fecha [FECHA], como documento n.º 8.

En este sentido, previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

Así, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento nº [Nº DE DOCUMENTO]

FUNDAMENTOS DE DERECHO

I.- COMPETENCIA.

Conforme a lo establecido en el art. 769.3 LEC como fuero de competencia territorial, para caso de domicilios de los progenitores en dos partidos judiciales, se fija la circunscripción del Juez competente para conocer del proceso en el partido del último domicilio del demandado, que coincide con la residencia del menor.

II.- PARTES.

La legitimación activa y pasiva para intervenir en el procedimiento corresponde a ambos progenitores, habida cuenta que son los que se hallan en la situación jurídica respectiva del derecho-deber de velar por los hijos menores no emancipados (art. 154 CC). Con arreglo al art. 749.2 LEC, deberá ser parte el Ministerio Fiscal, por existir hijos menores.

III.- PROCEDIMIENTO.

Las pretensiones que versan exclusivamente sobre guarda y custodia de hijos menores o sobre alimentos reclamados por un progenitor contra el otro en nombre de tales hijos, se incluyen en el ámbito de aplicación del Título I del Libro IV, y se sustancian conforme al modelo de proceso especial del art. 753 LEC, que es juicio verbal con contestación escrita.

IV.- CUMPLIMIENTO DE LOS REQUISITOS DE PROCEDIBILIDAD.

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 en relación con el art. 437.1 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

V.- FONDO DEL ASUNTO.

El art. 159 CC previene que si los padres viven separados y no decidieren de común acuerdo, el Juez decidirá, siempre en beneficio de los hijos, al cuidado de qué progenitor quedarán los hijos menores de edad.

Es claro que la guarda del hijo no es un derecho subjetivo del padre, como que no hay razón para que unos abuelos no queden custodios de la nieta, si es lo conveniente para su educación, por circunstancias concurrentes en las personas de los titulares de la patria potestad, ya que las medidas relativas al cuidado de los hijos menores de edad deben ser adoptadas siempre en su beneficio, como ha manifestado reiteradamente la jurisprudencia, prevaleciendo siempre el bienestar de los mismos.

Mas, en el caso presente la madre está en una disposición física, psíquica y económica correcta para ocuparse de su hija, después de tiempos amargos de distanciamiento; es natural su convivencia con la hija menor; y el padre no ha asumido realmente sus deberes paterno-filiales desde el mismo nacimiento de la hija; en fin, los abuelos no tienen edad ni cultura para ocuparse de la niña, que padece enfermedad crónica [ENFERMEDAD], etc

VI.- COSTAS.

Las costas procesales deben ser impuestas a la parte demandada, por criterio del íntegro vencimiento, en atención al art. 394 LEC.

Y demás normas y jurisprudencia de general y pertinente aplicación.

En virtud de lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito con los documentos que se acompañan y sus copias, se digne admitirlos, tenerme por comparecido y parte en la representación que ostento, y seguido que sea el procedimiento por sus pertinentes trámites, con citación del Ministerio Fiscal, se sirva dictar Sentencia por la que, estimando la presente demanda, declare el derecho de la demandante Dña.a la exclusiva guarda y custodia del/ la hijo/a menor, con expresa imposición de las costas procesales al demandado si resiste la pretensión.

Es de Justicia que pido en [LUGAR], a [FECHA].

OTROSÍ DIGO: Que al amparo del art. 770.6.ª LEC, se solicitan mediante el presente escrito MEDIDAS PROVISIONALES, en base a los siguientes:

HECHOS

ÚNICO.-

Se tienen por reproducidos los hechos de la pretensión principal, destacando la urgencia de la salud y educación de la hija menor de edad.

FUNDAMENTOS DE DERECHO

I.- La madre que solicita la guarda y custodia está legitimada según el art. 159 CC, siendo el procedimiento adecuado, en tanto que demandante de las mismas, el de la comparecencia del art. 771 LEC para medidas previas, conforme remisión del art. 773.3 LEC, que a su vez es uno de los cauces a que se refiere el art. 770.6.ª LEC.

II.- Son presupuestos de las medidas cautelares la apariencia de buen derecho y el peligro de demora.

El derecho aparece positivizado en los principios que inspiran iniciativas legislativas como las de la Ley 1/1996, de 15 de enero, de Protección Jurídica del Menor, y de la titularidad de la patria potestad, que encierra el derecho-deber de ocuparse de que puedan llevarlos a ejecución los menores (art. 154 CC), sin que se demuestre siquiera indicio de circunstancia excepcional que indique contraproducente la convivencia.

El peligro de demora deriva de que el tiempo -siquiera el puramente legal- del proceso dificulta la efectividad de la pretensión que debe prosperar, porque cada momento que la hija permanece separada de la madre se pierde un tiempo, ya irrecuperable, de la formación del menor, fuera del modelo de personalidad adecuado, educado y alimentado con el amor maternal.

En su virtud,

SUPLICO AL TRIBUNAL

que, teniendo por causadas las precedentes manifestaciones a los efectos oportunos, y por deducida solicitud de adopción de medidas provisionales, seguido que sea su pertinente trámite, se dicte Auto por el que se apruebe la atribución provisional de la guarda y custodia de la hija menor a la actora Dña. [NOMBRE Y APELLIDOS],con condena en costas del incidente si la parte adversa se opusiera.

Reitero Justicia en lugar y fecha ut supra.

Es justicia que pido en [LUGAR], a [FECHA].

Firma de Abogado/a	Firma de Procurador/a

========================================================================
