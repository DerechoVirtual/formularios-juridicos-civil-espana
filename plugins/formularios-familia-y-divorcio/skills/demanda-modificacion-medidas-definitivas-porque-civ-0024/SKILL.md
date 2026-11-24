---
name: demanda-modificacion-medidas-definitivas-porque-civ-0024
description: "Demanda de modificación de medidas definitivas porque el progenitor custodio cambia de domicilio. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de modificación de medidas definitivas porque el progenitor custodio cambia de domicilio

> Formulario **CIV-0024** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de modificación de medidas definitivas porque el progenitor custodio cambia de domicilio» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de modificación de medidas definitivas porque el progenitor custodio cambia de domicilio” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:demanda-modificacion-medidas-definitivas-porque-civ-0024`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] AÑO (8 veces)
- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] MES (5 veces)
- [ ] DÍA (4 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] Nº (3 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] DIRECCIÓN (2 veces)
- [ ] Nº DE PROCEDIMIENTO (2 veces)
- [ ] CALLE
- [ ] COLEGIO
- [ ] FECHA
- [ ] FUNDAMENTOS
- [ ] MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] NOMBRE DEL COLEGIO
- [ ] Nº DE ARTÍCULO
- [ ] NÚMERO
- [ ] SEDE
- [ ] TEXTO DE LA CLÁUSULA

## Normas que cita el formulario

- art. 775 LEC
- art. 90 CC
- art. 749.2 LEC
- art. 750 LEC
- art. 437.1 LEC
- art. 5 Ley Orgánica 1/2025
- art. 90.3 CC
- art. 775.1 LEC
- art. 91 CC
- art. 103.1 CC
- art. 394 LEC
- art. 770 LEC
- art. 775.2 LEC

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

- Junto a «…Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).
- Junto a «…2666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.

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

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

D./Dª [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, en nombre y representación de D./Dª [NOMBRE Y APELLIDOS], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], comparezco en este TRIBUNAL con la asistencia del Letrado D. /Dª [NOMBRE Y APELLIDOS], del Ilustre Colegio de Abogados de [COLEGIO], y DIGO:

Que por medio del presente escrito y en la representación que ostento, interpongo DEMANDA DE MODIFICACIÓN DE MEDIDAS DEFINITIVAS, adoptadas en sentencia de divorcio/separación dictada en el procedimiento de mutuo acuerdo/contencioso, seguido ante este Tribunal al cual me dirijo, número de procedimiento [Nº DE PROCEDIMIENTO]/[AÑO], contra D./Dª [NOMBRE Y APELLIDOS], mayor de edad, con domicilio en [LOCALIDAD], calle [CALLE], nº [NÚMERO], pta. La presente demanda se basa en los siguientes

HECHOS:

PRIMERO En fecha [DÍA] de [MES] de [AÑO], se dictó sentencia de divorcio [ELEGIR: contencioso / de mutuo acuerdo], de mutuo acuerdo núm. [Nº]/[AÑO] puede tratarse también de un procedimiento contencioso, en cuyo caso, las referencias que se hacen a continuación al convenio regulador judicialmente homologado, lo serían a las medidas adoptadas por el Juez, en la que se procedió a homologar el Convenio regulador de fecha [DÍA] de [MES] de [AÑO], presentado por las partes.

En la estipulación [Nº] del citado Convenio, en la que se regula el régimen de guarda y custodia de los hijos menores del matrimonio, se atribuye ésta a la madre, con régimen de visitas en favor del padre, mi representado. El tenor literal de la citada estipulación es el siguiente: [TEXTO DE LA CLÁUSULA].

SEGUNDO En fecha [DÍA] de [MES] de [AÑO], mi representado recibió un burofax de la damandada en que le comunicaba su decisión unilateral de cambiar su domicilio, en el que convive con los hijos comunes sobre los que tiene atribuida la guarda y custodia y que hasta entonces estaba fijado en: [DIRECCIÓN]. El nuevo domicilio, al que ya se ha trasladado la demandada con los citados hijos se encuentra en: [DIRECCIÓN], a 300 km de distancia del domicilio anterior.

Se acompañan como DOCUMENTO Nº [Nº DE DOCUMENTO] el citado burofax, para acreditar los hechos referidos.

TERCERO El referido cambio de domicilio dificulta que los menores puedan mantener el arraigo con su entorno afectivo, lo cual perjudica gravemente sus intereses y, además, entorpece gravemente las posibilidades de mi mandante de relacionarse con sus hijos conforme al régimen de visitas inicialmente pactado. Por ello, mi representado desea solicitar que se prohíba a la demandada el cambio de domicilio y, subsidiariamente, de no estimarse esto, que se modifique el régimen de guarda y custodia, suspendiéndose la de la madre y atribuyéndose en favor de mi mandante.

CUARTO Mi representado, padre de los menores, está perfectamente capacitado y tiene disponibilidad para su cuidado. Puede hacerse cargo de sus hijos todos los días de la semana, menos uno, cada quince días, en que no puede recogerlos del colegio, pero cuenta con dos hermanas, tías de los menores, cuyos hijos asisten al mismo colegio y se encargarían de recoger y atender al menor ese día hasta las 21 h. Por otra parte, mi mandante está acostumbrado a cuidar a sus hijos cuando están con él: alimentarlos, bañarlos, vestirlos, etc. Además, los acompaña y recoge de las actividades extraescolares y de las fiestas infantiles a las que asisten..

QUINTO Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento nº [Nº DE DOCUMENTO]

Resultan aplicables a los citados hechos los siguientes

FUNDAMENTOS DE DERECHO

Competencia

Es competente el Tribunal al que me dirijo, de acuerdo con el artículo 775 LEC.

Legitimación

La de ambas partes deriva del artículo 775 LEC y de los artículos 90 y 91 CC. Conforme al art. 749.2 LEC, debe intervenir el Ministerio Fiscal, por encontrarse interesados menores.

Procedimiento

Arts. 775.2 y 770 LEC.

Representación y defensa

El/La demandante comparece representado y defendido, respectivamente, por el Procurador y el Letrado que constan en el encabezamiento de este escrito, de acuerdo con lo dispuesto en el artículo 750 LEC, en relación con los artículos 770 y 775.2 LEC.

Cumplimiento de los requisitos de procedibilidad

La presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 LEC en relación con el art. 437.1 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

Derecho sustantivo

El art. 90.3, primer inciso CC dispone: “Las medidas que el Juez adopte en defecto de acuerdo o las convenidas por los cónyuges judicialmente, podrán ser modificadas judicialmente o por nuevo convenio aprobado por el Juez, cuando así lo aconsejen las nuevas necesidades de los hijos o el cambio de las circunstancias de los cónyuges” "Asimismo, podrá modificarse el convenio o solicitarse modificación de las medidas sobre los animales de compañía si se hubieran alterado gravemente sus circunstancias." (párrafo introducido por Ley 17/2021, de 15 diciembre), en relación con el art. 775.1 LEC, que regula la modificación de las medidas definitivas y que señala: “El Ministerio Fiscal, habiendo hijos menores o hijos con discapacidad con medidas de apoyo atribuidas a sus progenitores y, en todo caso, los cónyuges, podrán solicitar del Tribunal que acordó las medidas definitivas, la modificación de las medidas convenidas por los cónyuges o de las adoptadas en defecto de acuerdo, siempre que hayan variado sustancialmente las circunstancias tenidas en cuenta al aprobarlas o acordarlas”. [Nº DE ARTÍCULO]. En el mismo sentido, el art. 91 CC, señala que las medidas judiciales “podrán ser modificadas cuando se alteren sustancialmente las circunstancias”.

La libertad de elección del domicilio como derecho fundamental de las personas (art. 19 CE) tiene limitaciones cuando se proyecta sobre los hijos menores sujetos a patria potestad, que pueden verse drásticamente afectados por un ejercicio irresponsable de este derecho fundamental (en este sentido, el auto del TC nº 127/86, de 12 de febrero).

La elección de domicilio, entorno y educación de los hijos corresponde a los padres que ostentan la patria potestad; a los dos, titulares de dicha patria potestad, aunque la guarda y custodia se encuentre atribuida a uno solo de ellos, como se desprende de los arts. 154 y ss. CC. Un cambio de domicilio relevante para la vida del menor, es una cuestión que debería ser decidida conjuntamente por los dos cotitulares de la patria potestad, y, en defecto de acuerdo, por la autoridad judicial (arts. 103.1º y 156 CC). De ahí que mi mandante, que sigue ostentando la patria potestad sobre sus hijos menores de edad, tenga derecho a ser oído y tenida en cuenta su opinión en relación con un eventual cambio de residencia que afecte a los hijos, lo cual no se ha respetado en el caso presente.

El interés superior del menor requiere que éste pueda mantener el arraigo con su entorno afectivo: familiares y amigos. Por ello es conveniente que mantenga el domicilio que hasta ahora tenía, sito en [LOCALIDAD] y los menores sigan asistiendo al colegio en el que estaban hasta ahora matriculados: [NOMBRE DEL COLEGIO]. Subsidiariamente, para el caso de que la demandada no cumpla con lo indicado o alegue no poderlo cumplir por razones laborales o personales o de cualquier otra índole, se solicita la suspensión de la guarda y custodia de la misma sobre sus hijos, concediéndose a su padre, mi mandante, para que residan en su compañía en [LOCALIDAD], lo que les permitirá seguir asistiendo a su colegio habitual y mantener el arraigo con su entorno.

[FUNDAMENTOS]

Costas

Se impondrán de acuerdo con lo dispuesto en el art. 394 LEC.

Iura novit curia y las demás normas que resulten procedentes

Por lo expuesto

SUPLICO AL TRIBUNAL:

Que tras admitir este escrito con los documentos que lo acompañan y sus copias, me tenga por comparecido y parte en la representación que ostento, entendiéndose conmigo las sucesivas diligencias, y tenga por interpuesta DEMANDA DE MODIFICACIÓN DE MEDIDAS DEFINITIVAS DE DIVORCIO o de separación, que habrá de sustanciarse por los trámites del juicio verbal con las especialidades del art. 770 LEC, conforme a lo establecido en el art. 775.2 LEC, contra D./Dª [NOMBRE Y APELLIDOS]; y, previos los trámites legales que procedan, entre ellos, el traslado de la presente demanda al/a la demandado/a y al Ministerio Fiscal, dicte resolución por la que, estimando íntegramente la demanda, se modifiquen las medidas adoptadas en la sentencia de divorcio/separación dictada por este Tribunal en fecha [FECHA], de [MES], de [AÑO], procedimiento núm. [Nº DE PROCEDIMIENTO]/[AÑO] en relación con la guarda y custodia del hijo menor de los cónyuges [NOMBRE Y APELLIDOS], en el sentido de que en el caso de que la demandada persista en el cambio de domicilio efectuado, se suspenda la guarda y custodia que tiene atribuida sobre los hijos comunes, [NOMBRE Y APELLIDOS] y [NOMBRE Y APELLIDOS], y se atribuya dicha guarda y custodia a mi mandante, reconociendo a la demanda el derecho a visitar a sus hijos, todo ello en los siguientes términos: Así mismo, se solicita la imposición de las costas a la demandada si se opone a esta demanda, conforme al art. 394 LEC.

En [LOCALIDAD], a [DÍA], de [MES], de [AÑO]

Firma y número del Letrado	Firma del Procurador

========================================================================
