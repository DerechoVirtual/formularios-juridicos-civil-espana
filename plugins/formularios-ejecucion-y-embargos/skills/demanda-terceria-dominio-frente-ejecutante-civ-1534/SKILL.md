---
name: demanda-terceria-dominio-frente-ejecutante-civ-1534
description: "Demanda de tercería de dominio frente al ejecutante. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de tercería de dominio frente al ejecutante

> Formulario **CIV-1534** del plugin **Ejecución de sentencias y embargos** (`formularios-ejecucion-y-embargos`) · Civil › Ejecución · normativa revisada el 24-11-2026.

## Qué es

Demanda de tercería de dominio frente a la parte ejecutante de un procedimiento de ejecución, al ser ese bien propiedad de un tercero.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de tercería de dominio frente al ejecutante» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de tercería de dominio frente al ejecutante” para mi caso». También puedes invocarla directamente con `/formularios-ejecucion-y-embargos:demanda-terceria-dominio-frente-ejecutante-civ-1534`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ejecucion-y-embargos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Ejecución de sentencias y embargos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (16 veces)
- [ ] FECHA (9 veces)
- [ ] Nº DE DOCUMENTO (9 veces)
- [ ] LOCALIDAD (6 veces)
- [ ] Nº (6 veces)
- [ ] SEDE (4 veces)
- [ ] AÑO (2 veces)
- [ ] COLEGIO
- [ ] CURSO
- [ ] DENOMINACIÓN SOCIAL
- [ ] FINCA
- [ ] LUGAR
- [ ] MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO
- [ ] NOMBRE DEL CENTRO
- [ ] NOMBRE DEL MENOR
- [ ] Nº DE PROCEDIMIENTO
- [ ] NÚMERO
- [ ] PISO
- [ ] PUERTA
- [ ] PÁGINA
- [ ] TOMO

## Normas que cita el formulario

- art. 595.3 LEC
- art. 85.1 LOPJ
- art. 595 LEC
- art. 600 LEC
- art. 23 LEC
- art. 437 LEC
- art. 596 LEC
- art. 1445 Código Civil
- art. 437.1 LEC
- art. 5 Ley Orgánica 1/2025
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

### Avisos de actualización (2) — se aplican en el texto, nunca se copian en el documento

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º LOS DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…e Abogados de [COLEGIO], ante el Tribunal de Instancia de [SEDE], plaza n.º [Nº]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. «De los de» es residuo de los varios juzgados de una plaza. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º LOS DE [SEDE]

Don [NOMBRE Y APELLIDOS], Procurador de los Tribunales, actuando en nombre y representación de Don [NOMBRE Y APELLIDOS], según acredito mediante apoderamiento apud acta otorgado ante el Letrado de la Administración de Justicia de [LOCALIDAD], y bajo la dirección Letrada de Don [NOMBRE Y APELLIDOS], del Ilustre Colegio de Abogados de [COLEGIO], ante el Tribunal de Instancia de [SEDE], plaza n.º [Nº] comparezco y, como menor proceda en Derecho, DIGO:

Que en la indicada representación por medio del presente escrito interpongo DEMANDA DE TERCERÍA DE DOMINIO a sustanciar por los trámites del juicio verbal contra Don [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], y como parte ejecutante en el presente procedimiento de ejecución núm. [Nº DE PROCEDIMIENTO] del año [AÑO] que se sigue en ese tribunal, y contra Don [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], como parte ejecutada, al haber resultado embargado en el presente procedimiento bien inmueble que luego se dirá como perteneciente al ejecutado y ser designado por éste, cuando pertenece a mi mandante, la cual baso en los siguientes:

Hechos

Primero.– Bien embargado

Que en el procedimiento ejecutivo sustanciado ante este mismo Tribunal como núm. [Nº] del año [AÑO] y promovido por Don [NOMBRE Y APELLIDOS] contra Don [NOMBRE Y APELLIDOS], ambos codemandados en la presente tercería, ha resultado embargado con fecha [FECHA] como bien presuntamente perteneciente al ejecutado, la finca urbana sita en [LOCALIDAD], inscrita en el Registro de la Propiedad núm. [Nº] de los de [SEDE] al Libro, tomo [TOMO], página [PÁGINA], finca [FINCA], la cual en fecha [FECHA] mi mandante adquirió del ejecutado por medio de escritura pública otorgada ante el Notario Don [NOMBRE Y APELLIDOS], del Ilustre Colegio de Notarios de [LOCALIDAD] en prueba de lo manifestado se acompaña escritura pública de compraventa como Documento núm. [Nº DE DOCUMENTO].

Segundo.– Dominio del bien

Que dicha finca pertenece realmente a mi mandante Don [NOMBRE Y APELLIDOS] desde fecha [FECHA] en la que el ejecutado Don [NOMBRE Y APELLIDOS], aún hoy aparente titular registral, vendió mediante escritura pública la finca a mi principal, entregando la posesión de la finca en aquel mismo acto, según resulta de la propia escritura y de sus pactos, ya acompañada, que a su vez constituye el principio de prueba escrito que exige el artículo 595.3 LEC como fundamento de la pretensión de mi principal.

Que una vez satisfecho el importe del impuesto de transmisiones patrimoniales, tal como se acredita con la copia para el contribuyente del modelo correspondiente de declaración-liquidación, que acompaño como Documento núm. [Nº], mi representado se personó en el registro de la propiedad número [NÚMERO] de la localidad de [LOCALIDAD] al objeto de entregar la escritura pública de compraventa para proceder a su inscripción, solicitando a la vez que una vez practicada la inscripción se le entregara nota simple de la misma al objeto de solicitar un préstamo con garantía hipotecaria, por habérselo así indicado y requerido su entidad financiera para así poder constituir la hipoteca.

Que al expedir por el Registro de la Propiedad antes mencionado la citada nota simple es cuando mi mandante tiene conocimiento de que sobre la finca descrita en el Hecho I constaba anotado un embargo decretado por este Tribunal en fecha [FECHA], posterior al de la escritura de compraventa anteriormente referenciada y acompañada, y anotado en el Registro con fecha [FECHA].

Que en prueba de lo manifestado se acompaña copia de la diligencia de embargo practicada a resultas de la ejecución referida y de la que resulta que el embargo sobre dicho bien se produce a designa del ejecutado, como Documento núm. [Nº], así como la nota simple librada por el Registro de la Propiedad antes referido, como Documento núm. [Nº], de la que resulta la anotación de embargo derivada del procedimiento indicado.

Tercero.– Realidad de la transmisión

Que la realidad de la transmisión plasmada en la escritura pública de compraventa aportada resulta, además, y sin perjuicio de la plena acreditación que de ello se efectuará en el momento procesal oportuno, mediante las testificales y demás documentales públicas de las que intentará valerse esta parte, de los siguientes documentos, todos ellos de fecha muy anterior a la traba del embargo propiciada por la falta de reflejo de la transmisión realizada en documento privado, en el registro de la propiedad, donde viene reflejándose una realidad registral en desacuerdo con la realidad jurídica extrajudicial.

a) Actas de Junta de copropietarios del inmueble en el que se ubica la finca, celebradas al amparo de la Ley de Propiedad Horizontal y en las que resulta presente mi principal como propietario del piso [PISO] puerta [PUERTA] que constituye la finca cuyo embargo se pretende, que acompaño como Documentos núms. a [Nº DE DOCUMENTO].

b) Certificado del padrón municipal acreditativo de la primera fecha de ocupación por parte de mi mandante y su familia de la finca de referencia, que acompaño como Documento núm. [Nº DE DOCUMENTO].

c) Póliza de contratación de suministro de energía eléctrica suscrito con la compañía suministradora a título de dueño de fecha [FECHA], así como recibos de consumos del último año, que acompaño como Documentos núms. a [Nº DE DOCUMENTO].

d) Solicitud de alta de línea telefónica de fecha [FECHA], así como contrato realizado con la compañía telefónica [DENOMINACIÓN SOCIAL] en el momento de dar de alta la línea telefónica, que acompaño como Documentos núms. y [Nº DE DOCUMENTO].

e) Póliza de contratación de suministro de gas natural suscrito con las compañía suministradora a título de dueño de fecha [FECHA], así como recibos de consumos del último año, que acompaño como Documentos núms. a [Nº DE DOCUMENTO].

f) Acta notarial de manifestaciones recogida por el Ilustre Notario de esta ciudad Don [NOMBRE Y APELLIDOS], y recogidas de los vecinos del mismo inmueble y en las que se constata el carácter de ser la vivienda en cuestión el domicilio familiar de representado, que acompaño como Documento núm. [Nº DE DOCUMENTO].

g) Certificado del colegio público [NOMBRE DEL CENTRO] acreditativo de que el hijo menor [NOMBRE DEL MENOR] cursa estudios desde el curso académico [CURSO] en el indicado centro por ser el que le corresponde en función de la ubicación de la vivienda familiar de los padres, que acompaño como Documento núm. [Nº DE DOCUMENTO].

A los anteriores hechos les son de aplicación los siguientes:

Cuarto.– Proceso de negociación previo y medios de solución de controversias de manera amistosa y extrajudicial

Previamente a la interposición de la presente demanda, se efectuaron diversas gestiones negociadoras con la parte demandada, con el propósito de cumplir con el requisito de procedibilidad y resolver el litigio de manera amistosa y extrajudicial.

En este sentido, se acudió a [MEDIO ADECUADO DE SOLUCIÓN DE CONTROVERSIAS UTILIZADO], no habiendo sido posible alcanzar un acuerdo definitivo.

Se acompaña como documento nº [Nº DE DOCUMENTO]

A los anteriores hechos son de aplicación los siguientes

Fundamentos de derecho

Primero.– Competencia

Con arreglo al artículo 599 de la Ley de Enjuiciamiento Civil en relación con lo dispuesto en el art. 85.1º LOPJ, corresponde al Tribunal de Instancia al que me dirijo, por resultar este Tribunal el que viene conociendo de la ejecución en la que se ha producido el embargo del que trae causa la presente tercería.

Segundo.– Capacidad para ser parte

Conforme lo dispuesto en el artículo 6 y ss. LEC la tienen demandante y demandado.

Tercero.– Legitimación Activa

Con arreglo a lo dispuesto en el artículo 595 LEC la legitimación activa resulta a favor de la parte actora por resultar el verdadero propietario del bien embargado como perteneciente al ejecutado en el procedimiento de ejecución de constante referencia.

Cuarto.– Legitimación Pasiva

Conforme a lo dispuesto en el artículo 600 de la LEC la demanda de tercería se interpondrá en todo caso frente al acreedor ejecutante y frente al deudor ejecutado cuando el bien a que se refiere la tercería hubiere sido embargado por designa de éste.

Quinto.– Representación procesal y Defensa técnica

A tenor de lo dispuesto en los artículos 23, 31 y 32 LEC, se cumplen los requisitos de postulación y defensa por actuar representado de procurador y dirigido por abogado.

Sexto.– Acción ejercitada y Procedimiento

Se ejercita la tercería de dominio prevista en el artículo 595 y ss. de la Ley de Enjuiciamiento Civil, la cual deberá sustanciarse por los trámites del juicio verbal previsto en los artículos 437 y siguientes de la LEC.

Séptimo.– Momento de interposición

Con arreglo a lo dispuesto en el artículo 596 LEC la demanda se presenta en el momento procesal oportuno, pues se ha decretado el embargo y no se ha procedido todavía a su venta o adjudicación.

Octavo.– Fondo del asunto

Con arreglo a lo dispuesto en el artículo 1445 y concordantes del Código Civil.

Noveno.– Requisito de procedibilidad

A la demanda se acompaña el documento que acredita la adquisición del bien en fecha anterior al embargo, por lo que se cumple con el requisito exigido por el artículo 595 LEC.

Por otro lado, la presente demanda cumple con los requisitos de procedibilidad exigidos por los arts. 264.4º y 399.3 en relación con el art. 437.1 LEC, así como con lo dispuesto en el art. 5 de la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia.

Décimo.– Costas

En cuanto a las costas generadas por el proceso, conforme a lo dispuesto en el artículo 603 en relación con el artículo 394, ambos de la LEC, habrán de imponerse a los demandados que se opusieren.

Undécimo.– Iura novit Curia

Iura novit Curia y cuantos otros resulten de aplicación.

En su virtud,

AL TRIBUNAL SUPLICO: Que teniendo por presentado este escrito, documentos acompañados (en su caso, y copia de todo), los admita y en sus méritos, me tenga, en la representación que ostento y dejo acreditada de Don [NOMBRE Y APELLIDOS], por comparecido y por formulada DEMANDA DE TERCERÍA DE DOMINIO que deberá sustanciarse por los trámites del juicio ordinario y frente a Don [NOMBRE Y APELLIDOS] y Don [NOMBRE Y APELLIDOS], de las circunstancias personales ya señaladas, y en fuerza de cuya demanda acuerde la suspensión de la ejecución en cuanto al bien que ha quedado descrito en el hecho primero de la presente demanda, y emplazados que resulten los demandados y seguido el procedimiento por todos sus trámites, dicte en su día resolución en forma de auto por la que, estimando la presente tercería y teniendo por acreditado el derecho de mi principal sobre el bien embargado, deje sin efecto el embargo trabado sobre el mismo, ordenando su alzamiento y el libramiento de cuantos mandamientos fueren necesarios para llevar dicha declaración donde fuere menester, todo ello con expresa imposición de las costas de la tercería a cargo de los demandados.

Es Justicia que insto en [LUGAR], a [FECHA].

Abogado/a	Procurador/a

Fdo. D./Dña. [NOMBRE Y APELLIDOS]: Fdo. D./Dña. [NOMBRE Y APELLIDOS]:

========================================================================
