---
name: solicitud-diligencia-preliminar-exhibicion-cosa-mueble-civ-1200
description: "Solicitud de diligencia preliminar de exhibición de cosa mueble. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud de diligencia preliminar de exhibición de cosa mueble

> Formulario **CIV-1200** del plugin **Medidas cautelares y diligencias preliminares** (`formularios-medidas-cautelares-civiles`) · Civil › Medidas cautelares y diligencias preliminares · normativa revisada el 24-11-2026.

## Qué es

Escrito dirigido al Tribunal de Instancia solicitando la práctica, como diligencia preliminar, de la exhibición de una cosa para que la pueda identificar como propia. El solicitante ofrece caución.

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud de diligencia preliminar de exhibición de cosa mueble» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud de diligencia preliminar de exhibición de cosa mueble” para mi caso». También puedes invocarla directamente con `/formularios-medidas-cautelares-civiles:solicitud-diligencia-preliminar-exhibicion-cosa-mueble-civ-1200`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-medidas-cautelares-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Medidas cautelares y diligencias preliminares) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] DNI/NIE (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] MOTIVO (2 veces)
- [ ] ACTIVIDAD
- [ ] AÑO
- [ ] COLEGIO
- [ ] CONDICIÓN DEL SOLICITANTE
- [ ] DATOS QUE SE NECESITA CONOCER
- [ ] DESCRIPCIÓN DEL BIEN
- [ ] DESCRIPCIÓN DEL DOCUMENTO
- [ ] DIRECCIÓN
- [ ] DÍA
- [ ] IMPORTE
- [ ] LUGAR
- [ ] MES
- [ ] Nº DE FAX
- [ ] OBJETO DE LA DEMANDA
- [ ] SEDE
- [ ] TELÉFONO
- [ ] TIPO DE PROCEDIMIENTO

## Normas que cita el formulario

- art. 256.1.2.º LEC
- art. 256.12.º LEC
- art. 85.1 LOPJ
- art. 258 LEC
- art. 263 LEC
- art. 261.3.ª LEC

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS], Procurador de los Tribunales, actuando en nombre de D./Dña. [NOMBRE Y APELLIDOS], en virtud de la representación que acredito con la escritura de poder que acompaño y cuya devolución solicito, previo su testimonio en Autos, ante el Tribunal comparezco bajo la dirección letrada de D./Dña. [NOMBRE Y APELLIDOS], colegiado núm.del Iltre. Colegio de Abogados de [COLEGIO], y como mejor proceda en derecho DIGO:

Que mediante el presente escrito, en nombre de mi representado y al amparo de lo dispuesto en el artículo 256.1.2.º de la LEC, promuevo DILIGENCIA PRELIMINAR de exhibición de cosa prevista en el artículo 256.12.º de la LEC, frente a D./Dña. [NOMBRE Y APELLIDOS], domiciliado en [DOMICILIO], con DNI [DNI/NIE] y provisto de número de teléfono [TELÉFONO] y número de fax [Nº DE FAX], basándome en los siguientes

ANTECEDENTES

Mi representado tiene intención de promover demanda de [TIPO DE PROCEDIMIENTO] en el ejercicio de la acción reivindicatoria frente a D./Dña. [NOMBRE Y APELLIDOS]

El objeto concreto de la demanda que tiene previsto formular mi mandante consiste en [OBJETO DE LA DEMANDA] (detallar). La cosa objeto de esta solicitud es [DESCRIPCIÓN DEL BIEN] (describir de manera que permita una identifi indubitada).

Como documento núm. acompaño [DESCRIPCIÓN DEL DOCUMENTO] (por ejemplo, documento acreditativo de la titularidad que ostenta mi representado sobre la cosa cuya exhibición se pide).

Para plantear adecuadamente la demanda precisa mi poderdante conocer [DATOS QUE SE NECESITA CONOCER] (por ejemplo, el estado u otras circunstancias que afecten a esta de la cosa objeto de esta solicitud).

Resulta necesario a mi mandante conocer tales circunstancias relativas a la cosa a la que refiere esta Diligencia debido a [MOTIVO] (justificar la necesidad de la Diligencia Preliminar solicitada).

Resultan de aplicación los siguientes

FUNDAMENTOS DE DERECHO

Competencia

Es competente el Tribunal al que me dirijo en virtud de lo dispuesto por el artículo 257 de la Ley de Enjuiciamiento Civil (LEC), en relación con el art. 85.1º LOPJ

Procedimiento

La solicitud se tramitará por el cauce establecido en las artículos 258 y siguientes de la LEC.

Caución

El artículo 263 de la LEC exige el ofrecimiento de prestación de caución para responder de eventuales gastos y daños y perjuicios que se pudieran irrogar a la parte frente a la que se promueven estas diligencias. Se verifica dicho ofrecimiento mediante otrosí.

Fondo

El artículo 256.1.2.° de la LEC habilita la preparación del juicio mediante la petición a la persona a que se pretende demandar para que «exhiba la cosa que tenga en su poder y a la que se haya de referir el juicio».

En el presente caso se justifican la pertinencia y proporcionalidad de la diligencia preliminar interesada por las circunstancias de [MOTIVO] (justificar mediante la alegación de las razones concurrentes).

La justa causa y el interés legítimo de mi mandante que exige el artículo 258 de la LEC radican en su condición de [CONDICIÓN DEL SOLICITANTE] (por ejemplo: titular de la cosa que tiene intención de reivindicar judicialmente).

(desarrollar cuantas razones contribuyan a plantear la diligencia como adecuada a la finalidad perseguida y acreditar que la medida guarda proporcionalidad con dicho fin).

Por todo lo expuesto,

SUPLICO AL TRIBUNAL que tenga por presentado este escrito, con el poder y el documento que se acompañan con sus copias preceptivas, se sirva admitirlo, teniendo por promovida la diligencia preliminar solicitada, y en su virtud requiera a D./Dña. [NOMBRE Y APELLIDOS] para que exhiba la cosa objeto de esta solicitud que se deja descrita en el antecedente PRIMERO, acordando, si no atendiese el requerimiento ni formulase oposición, la entrada y registro en el local sito en [LOCALIDAD] donde se encuentra la cosa objeto de esta diligencia, todo ello con los demás pronunciamientos procedentes en derecho, y, una vez practicada la diligencia interesada, se me expida testimonio de su resultado.

Es Justicia que pido en [LUGAR], a [DÍA] de [MES] de [AÑO].

OTROSÍ DIGO: que a los efectos previstos en los artículos 256.3 y 258.3, y aun cuando esta parte interpreta que la diligencia solicitada no la precisaría, ofrecemos prestar, en la forma y plazos legalmente establecidos, la caución de [IMPORTE] euros, o subsidiariamente la que fije el Tribunal, comprometiéndonos a constituir la caución que se señale.

OTROSÍ SEGUNDO DIGO: que al amparo de lo dispuesto en el artículo 261.3.ª de la LEC, y para el supuesto de que la persona requerida no atienda al requerimiento ni formule oposición, solicito que por el Tribunal se ordene la entrada y registro del inmueble donde se encuentra la cosa objeto de solicitud de exhibición, sito en [LOCALIDAD] de [DIRECCIÓN], y que se acuerde el depósito de esta (u otra garantía pertinente), a cuyo efecto vengo a designar como depositario a D./Dña. [NOMBRE Y APELLIDOS], provisto de DNI [DNI/NIE] y domiciliado en [DOMICILIO], industrial del ramo de [ACTIVIDAD] de reconocida solvencia, que desempeñará leal y eficazmente el cargo de depositario.

NUEVAMENTE SUPLICO AL TRIBUNAL: tenga por hechas las anteriores manifestaciones, ordene la entrada y registro solicitados y acuerde el depósito de la cosa a que se contraen estas diligencias preliminares, adoptando las medidas oportunas para la efectividad del depósito y para el nombramiento del depositario que se deja propuesto o, subsidiariamente, del que determine el Tribunal, teniendo por formuladas las demás manifestaciones a los efectos legales pertinentes.

Es justicia que reitero en igual lugar y fecha.

NUEVAMENTE SUPLICO AL TRIBUNAL: tenga por hecha la anterior manifestación y por ofrecida la prestación de caución a los efectos legales oportunos.

Es Justicia que reitero en igual lugar y fecha.
