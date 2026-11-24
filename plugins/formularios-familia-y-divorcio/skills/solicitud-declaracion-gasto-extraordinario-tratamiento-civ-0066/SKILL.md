---
name: solicitud-declaracion-gasto-extraordinario-tratamiento-civ-0066
description: "Solicitud de declaración de gasto extraordinario por tratamiento del hijo común antes de ejecutar. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud de declaración de gasto extraordinario por tratamiento del hijo común antes de ejecutar

> Formulario **CIV-0066** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Escrito por el que se solicita al tribunal que declare que unos gastos derivados de la atención del hijo común (por ejemplo, un tratamiento médico o terapéutico necesario) tienen la consideración de gastos extraordinarios, con carácter previo a la demanda ejecutiva, cuando la sentencia o el convenio solo fija el reparto porcentual de los gastos extraordinarios pero no concreta cuáles son (art. 776.4.ª LEC).

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud de declaración de gasto extraordinario por tratamiento del hijo común antes de ejecutar» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud de declaración de gasto extraordinario por tratamiento del hijo común antes de ejecutar” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:solicitud-declaracion-gasto-extraordinario-tratamiento-civ-0066`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº DE DOCUMENTO (4 veces)
- [ ] FECHA (2 veces)
- [ ] Nº DE BLOQUE (2 veces)
- [ ] AÑO
- [ ] CLASE DE PROCEDIMIENTO
- [ ] DESCRIPCIÓN DE LOS GASTOS
- [ ] DESCRIPCIÓN DEL TRATAMIENTO O GASTO NECESARIO
- [ ] DÍA
- [ ] FRECUENCIA Y DURACIÓN DE LAS SESIONES O PRESTACIONES
- [ ] IMPORTE
- [ ] LOCALIDAD
- [ ] MES
- [ ] NOMBRE DEL HIJO/A
- [ ] NOMBRE Y APELLIDOS DEL DEMANDADO/A
- [ ] NOMBRE Y APELLIDOS DEL DEMANDANTE
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] NOMBRE Y APELLIDOS DEL REPRESENTADO/A
- [ ] Nº
- [ ] Nº DE PROCEDIMIENTO
- [ ] Nº DE SECCIÓN
- [ ] PERIODO
- [ ] PORCENTAJE
- [ ] PROVINCIA
- [ ] SEDE

## Normas que cita el formulario

- art. 776.4.ª LEC
- art. 776 LEC
- art. 387 LEC
- art. 552.1 LEC
- art. 390 LEC

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

### Avisos de actualización (0) — se aplican en el texto, nunca se copian en el documento

- Ninguno.

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

A LA SECCIÓN [ELEGIR: DE FAMILIA, INFANCIA Y CAPACIDAD / CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales, que actúa en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS DEL REPRESENTADO/A], según tengo acreditado, junto con la dirección letrada y las circunstancias personales, en los autos de [CLASE DE PROCEDIMIENTO] n.º [Nº DE PROCEDIMIENTO], seguidos a instancias de D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDANTE] frente a D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDADO/A], ante el Tribunal comparezco y, como mejor proceda en Derecho (véase la nota explicativa del final), DIGO:

Que por medio del presente escrito, y conforme a lo establecido en el art. 776.4.ª LEC, interesa esta parte, con carácter previo a presentar demanda ejecutiva, la DECLARACIÓN DE GASTO EXTRAORDINARIO de los gastos relativos a [DESCRIPCIÓN DE LOS GASTOS], en base a las siguientes

ALEGACIONES

PRIMERA.- El día [FECHA] el tribunal al que me dirijo dictó [ELEGIR: sentencia / auto] de [CLASE DE RESOLUCIÓN: DIVORCIO, SEPARACIÓN, MODIFICACIÓN DE MEDIDAS, ETC.], que en su parte dispositiva fijaba, entre otras medidas, la obligación de cada progenitor de abonar el [PORCENTAJE] % de los gastos extraordinarios del hijo menor de edad.

Sin embargo, la resolución judicial no concretaba qué gastos tenían dicha consideración.

[OPCIONAL — incluir si procede]

SEGUNDA.- Dicha resolución fue recurrida en apelación, dictando la Sección [Nº DE SECCIÓN] de la Audiencia Provincial de [PROVINCIA] sentencia de fecha [FECHA], que ratificó el referido pronunciamiento.

TERCERA.- Desde hace [PERIODO], [ELEGIR: ante las dificultades del menor en el habla / ante otra circunstancia sobrevenida] y por indicación de su [ELEGIR: pediatra / médico / especialista], el menor [NOMBRE DEL HIJO/A] ha recibido [DESCRIPCIÓN DEL TRATAMIENTO O GASTO NECESARIO], que se han venido repitiendo a razón de [FRECUENCIA Y DURACIÓN DE LAS SESIONES O PRESTACIONES].

CUARTA.- Se ha requerido al otro progenitor para que abone la mitad de los gastos derivados del necesario tratamiento, que ascienden a [IMPORTE] euros, pues los mismos no están cubiertos por ninguna de las coberturas sanitarias de los progenitores, sin que se haya obtenido respuesta alguna.

Se acompañan testimonios de la sentencia de instancia y, en su caso, de la de apelación como documentos n.º [Nº DE DOCUMENTO] y [Nº DE DOCUMENTO], el informe médico como documento n.º [Nº DE DOCUMENTO], las facturas del profesional como bloque documental n.º [Nº DE BLOQUE], así como los recibos de pago efectuados por [ELEGIR: la madre / el padre] del menor, que también se acompañan como bloque documental n.º [Nº DE BLOQUE]. Por último, se acompaña, como documento n.º [Nº DE DOCUMENTO], el requerimiento de pago extrajudicial, desatendido por el futuro ejecutado.

QUINTA.- Considera esta parte que dichos gastos pueden ser considerados extraordinarios, atendiendo al carácter no habitual de los mismos, al hecho de que se generan en atención a una circunstancia del menor que no se pudo prever en su momento, y a su elevado importe, por lo que se interesa que por el Tribunal se declare que la cantidad pagada por aquéllos tiene la consideración de gastos extraordinarios, a fin de proceder a su exacción por la vía ejecutiva.

De conformidad con lo anteriormente expuesto,

SUPLICO AL TRIBUNAL:

Que, por presentado este escrito, con los documentos acompañados y copia de todo ello, se sirva admitir uno y otros y, en méritos del mismo, previo traslado a la parte contraria y demás trámites legales oportunos, se dicte Auto declarando que los gastos justificados por esta parte tienen la consideración de gastos extraordinarios.

Es justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del Abogado/a Firma del Procurador/a

NOTA EXPLICATIVA (suprimir antes de presentar el escrito):

La Ley 13/2009, de 3 de noviembre, añadió al art. 776 LEC una regla 4.ª que regula un incidente declarativo previo al despacho de ejecución forzosa por gastos extraordinarios no previstos expresamente en el título ejecutivo judicial.

La regla 4.ª del art. 776 LEC configura legalmente el incidente declarativo como una cuestión incidental de previo pronunciamiento respecto del proceso principal de ejecución forzosa en reclamación de gastos extraordinarios, al establecer que la iniciación y terminación de este incidente ha de ser previa al despacho de ejecución ("... deberá solicitarse previamente al despacho de ejecución la declaración de que la cantidad reclamada tiene la consideración de gasto extraordinario...").

De ahí que sean de aplicación a este incidente declarativo las disposiciones contenidas en los arts. 387 a 393 LEC, referidos a las cuestiones incidentales, en todos los aspectos no regulados en la propia regla 4.ª del art. 776.

En principio, el incidente podrá iniciarse en alguna de las formas siguientes:

a) Por escrito formulado, antes de presentar la demanda ejecutiva, por la parte que se proponga demandar la ejecución forzosa por impago de gastos extraordinarios, que es el caso que contempla este modelo.

El incidente se promoverá por propia iniciativa de la parte que tenga intención de presentar demanda ejecutiva en reclamación de gastos extraordinarios, cuando considere que los gastos reclamados no están expresamente previstos como extraordinarios en el título ejecutivo judicial en que funde su pretensión.

b) Por escrito presentado por la parte ejecutante, después de interponer la demanda ejecutiva, cuando el tribunal deniegue el despacho de ejecución.

Es perfectamente posible también que la parte, no estimando necesario seguir el incidente de previo pronunciamiento, presente demanda ejecutiva en reclamación de gastos extraordinarios y solicite directamente el despacho de ejecución, pero el tribunal, tras examinar el título ejecutivo en que se funde el ejecutante, considere necesaria la apertura del incidente de previo pronunciamiento.

En este caso el tribunal denegará el despacho de ejecución, conforme al art. 552.1 LEC, por entender que del título ejecutivo no se desprende con claridad que la cantidad reclamada participa de los caracteres de gasto extraordinario, previniendo a la parte instante de la ejecución para que, si a su derecho interesa, presente escrito solicitando la declaración de que el gasto reclamado es extraordinario.

c) Por petición realizada (normalmente por medio de otrosí) por la parte ejecutante en su demanda ejecutiva, formulada con carácter subsidiario de la pretensión de despacho de ejecución, para el supuesto de que el tribunal estime necesario seguir el incidente de previo pronunciamiento y suspenda el curso del proceso de ejecución (posponiendo la decisión sobre el despacho de ejecución) hasta que el incidente de previo pronunciamiento sea resuelto.

Ciertamente, esta posibilidad no aparece expresamente contemplada en el art. 776.4.ª, pero tampoco su tenor literal la impide.

d) Por último, no faltan autores que estiman posible -aunque cabalmente se trate de una posibilidad contraria al tenor literal de la norma- que sea necesario proceder a la apertura judicial del incidente, en virtud de solicitud que formule la parte ejecutada dentro del plazo de diez días de que dispone para oponerse a la ejecución despachada. Ello acaecerá cuando la parte ejecutante no estime necesario seguir el incidente de previo pronunciamiento y el tribunal tampoco lo considere necesario y despache ejecución, si el ejecutado aduce el carácter ordinario del gasto que se le reclama como extraordinario.

Se fundamenta esta opinión en que no ha de privarse al ejecutado, que es el principal interesado en sostener la naturaleza ordinaria del gasto, de la única vía procesal legalmente habilitada para defender su posición, y que además no tiene noticia alguna de la reclamación del ejecutante hasta que se le notifica el auto despachando ejecución y se le da traslado de la demanda ejecutiva, de modo que, en caso de interesar a su derecho de defensa aducir el carácter ordinario del gasto reclamado como extraordinario, no debe impedírsele encauzar su defensa a través del incidente de previo pronunciamiento previsto a tal fin (i); el principio de igualdad de armas procesales exige conceder al ejecutado las mismas posibilidades de defensa que al ejecutante y, por ello, no puede dejarse únicamente en manos del ejecutante la posibilidad de promover el incidente (ii); y tampoco el tribunal puede denegar la apertura del incidente a instancia del ejecutado, en caso de solicitarse por éste, con el argumento de que, antes de acordar el despacho de ejecución, comprobó que el gasto extraordinario estaba expresamente previsto en el título, pues ello equivaldría a prejuzgar la declaración que constituye el objeto procesal del incidente mismo. Ahora bien, debe admitirse la posibilidad de que el ejecutado formule solicitud de declaración de que el gasto no tiene la consideración de extraordinario, siempre que la formule con carácter previo a la oposición y dentro del plazo legal de 10 días, y que ello debe dar lugar a la apertura del incidente con suspensión de la ejecución en el estado en que se encuentre (art. 393.2 en relación con el art. 390 LEC).
