---
name: recurso-casacion-razon-cuantia-regimen-anterior-rdl-5-civ-1330
description: "Recurso de casación por razón de la cuantía (régimen anterior al RDL 5 2023). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Recurso de casación por razón de la cuantía (régimen anterior al RDL 5 2023)

> Formulario **CIV-1330** del plugin **Recursos civiles: reposición, apelación, casación y queja** (`formularios-recursos-civiles`) · Civil › Recursos · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **recursos**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Recurso de casación por razón de la cuantía (régimen anterior al RDL 5 2023)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Recurso de casación por razón de la cuantía (régimen anterior al RDL 5 2023)” para mi caso». También puedes invocarla directamente con `/formularios-recursos-civiles:recurso-casacion-razon-cuantia-regimen-anterior-rdl-5-civ-1330`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-recursos-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Recursos civiles: reposición, apelación, casación y queja) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (6 veces)
- [ ] EXPONER EL MOTIVO
- [ ] FOLIO
- [ ] IMPORTE
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] NOMBRE O DENOMINACIÓN
- [ ] NOMBRE Y APELLIDOS
- [ ] Nº DE PROCEDIMIENTO

## Normas que cita el formulario

- art. 477.2 LEC
- art. 479 LEC
- art. 448.2 LEC
- art. 481 LEC
- art. 1104 Código Civil
- art. 1903 Código Civil

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

Rollo nº [Nº DE PROCEDIMIENTO]

A LA SECCIÓN DE LA AUDIENCIA PROVINCIAL

D. [NOMBRE Y APELLIDOS], Procurador de los Tribunales y de [NOMBRE DEL REPRESENTADO/A], según tengo acreditado en autos, ante la Sala comparezco y como mejor proceda en derecho DIGO:

1) Que en fecha [FECHA] esta parte ha sido notificada de la sentencia de fecha [FECHA] dictada en el Rollo arriba expresado, cuya parte dispositiva es del siguiente tenor literal: “[NOMBRE O DENOMINACIÓN]”

2) Que entendiendo que dicha sentencia no es ajustada a derecho, dicho sea con los debidos respetos y en términos de defensa, por medio del presente escrito, al amparo de lo dispuesto en el apartado 2º del artículo 477.2 de la LEC, interpongo contra la misma RECURSO DE CASACIÓN, en base a los siguientes presupuestos de admisibilidad y motivos:

I. ADMISIBILIDAD DEL RECURSO

PRIMERO.- Se recurre la sentencia de la Audiencia Provincial de fecha [FECHA] dictada en el Rollo arriba expresado, en proceso seguido por razón de la materia, siendo que dicha sentencia produce un evidente gravamen a esta parte, impugnándose todos sus pronunciamientos.

SEGUNDO.- El supuesto que habilita la interposición del recurso es el del ordinal 2º del art. 477.2 de la LEC, al tratarse de sentencia dictada en proceso de cuantía superior a 600.000 euros, constando en la resolución de fecha [FECHA] obrante en folio [FOLIO] de las actuaciones que la cuantía quedo fijada en [IMPORTE] euros.

TERCERO.- El presente recurso se interpone dentro del plazo de veinte días establecido en el artículo 479 de la LEC, computados conforme al artículo 448.2 de la LEC.

CUARTO.- Mediante el presente escrito, al amparo de lo dispuesto en el art. 481 de la LEC, interpongo recurso de casación por infracción de los artículos 1104 y 1903 del Código Civil, según se desarrolla a continuación extensamente, acompañando como documento número 1 certificación de la sentencia impugnada.

II. MOTIVOS DEL RECURSO

PRIMERO.- El primer motivo se interpone al amparo de lo dispuesto en el art. 477.2, ordinal segundo, de la LEC por infracción del artículo 1104 y 1903 del Código Civil, los cuales resultan vulnerados por cuanto que en la sentencia recurrida no se aprecia culpa o negligencia en la propietaria del buque y no se la considera responsable la defectuosa o inexistente vigilancia llevada a cabo por los vigilantes contratados por aquélla al realizar una valoración centrada exclusivamente en la falta de diligencia, lo cual infringe el canon interpretativo del “agotamiento de la diligencia”, que viene siendo exigido jurisprudencialmente, entre otras, en SSTS 413/1998, de 5 de Mayo, rec. 916/1994 y 1156/2002, de 5 de diciembre,

Desarrollo del motivo: El motivo de casación invocado lo es por infracción legal de los arts. 1104 y 1903 del Código Civil, en cuanto que la sentencia de segunda instancia no apreció negligencia en el propietario del buque quien, conforme al citado art. 1903, era responsable de la defectuosa o inexistente vigilancia llevada a cabo por los vigilantes contratados por aquél.

Para exponer el motivo de casación debemos partir del relato de hechos probados que se recoge en la sentencia de apelación, donde se afirma que había una situación de vulnerabilidad del buque, con aumento de su permeabilidad exterior y la disminución de la estabilidad transversal del mismo, que fueron consecuencia del desguace llevado a cabo en él por encargo del propietario.

Por tanto, y de acuerdo a la propia sentencia, la situación en que se hallaba el buque no era por tanto consecuencia de un hecho o circunstancia ajeno a la voluntad de la propietaria y debió de ser tenido en cuenta a la hora de adoptar las medidas de seguridad pertinentes, adecuadas al estado del objeto asegurado en el momento de la vigencia del contrato de seguro.

Las medidas adoptadas por la propiedad del buque, contratando vigilancia para el buque y en la compra de una bomba de achique, no pueden estimarse suficientes, mayormente, si como recoge la sentencia de instancia, consta que desde que comenzaron las lluvias el día [FECHA] hasta su hundimiento no se practicó actividad alguna tendente a paliar los efectos del temporal e, incluso, consta que en el momento del hundimiento no había personal alguno de vigilancia, por lo que existió una clara responsabilidad in eligendo o in vigilando por parte de la propiedad.

Centrada así la cuestión, expuesta con pleno respeto de los hechos probados de la sentencia, de acuerdo a los preceptos que resultan infringidos, debe partirse de la definición del art. 1104 del Código Civil de la culpa o negligencia del deudor como «la omisión de aquella diligencia que exija la naturaleza de la obligación y corresponda a las circunstancias de las personas, del tiempo y del lugar», en este artículo se está haciendo referencia a la culpa en el aspecto de falta de diligencia y previsión y su exoneración se produce cuando los sucesos no hubiesen podido preverse, lo que, en dimensión de responsabilidad, requería la ausencia de todo resquicio a esta imprevisibilidad como ha señalado el Alto Tribunal al que nos dirigimos en sentencias de 7 de octubre de 1991 ) y de 5 de mayo de 1998, rec. 916/1994. Con mayor claridad se expresa en la sentencia del Tribunal Supremo de 10 de julio de 1985, que indica que la jurisprudencia de esta Sala ha creado diversos paliativos cuales son el acentuar el rigor con que debe ser aplicado el art. 1104, definidor de la culpa o negligencia, que no se elimina siquiera con el puntual cumplimiento de las precauciones y prevenciones legales y reglamentarias y de las aconsejadas por la técnica si todas ellas se revelan insuficientes para la evitación del riesgo, erigiéndose como canon la exigencia de «agotar la diligencia».

En este caso, es claro que no resulta imprevisible que durante el tiempo en que el buque permaneció en el muelle después de su desguace, durante casi dos años, se habría de producir algún fenómeno atmosférico capaz de producir, por su intensidad o persistencia, la inundación del buque dadas las amplias cesáreas abiertas en su cubierta y que permitían el paso de agua sin impedimento alguno, lo que aumentaría los efectos de la permeabilidad exterior causada por el desguace, lo que obligaba a adoptar, todas las medidas necesarias y suficientes para evitar el hundimiento.

En consecuencia, tal como hizo el Tribunal de instancia, se aprecia una conducta culposa o negligente imputable a la sociedad tomadora del seguro, al no haber agotado las medidas que pudieran haber evitado el siniestro, o al ser inadecuadas por la constatada falta de cumplimiento de la vigilancia contratada, de donde también derivaría la responsabilidad del empleador por el inadecuado cumplimiento de sus obligaciones, conforme al art. 1903 del Código Civil, ya sea por culpa in eligendo o por culpa in vigilando.

Por tanto, interesamos que se case la sentencia recurrida y se resuelva sobre la cuestión debatida en forma concorde a las normas legales aplicables y, en consecuencia, entendemos que ha de confirmarse la sentencia dictada en primera instancia, imponiendo a la contraparte las costas del recurso de apelación.

SEGUNDO.- [EXPONER EL MOTIVO]
Por lo expuesto,

SUPLICO A LA SALA Que tenga por presentado este escrito con certificación de traslado, se sirva admitirlo y, en su virtud, tenga por interpuesto recurso de casación contra la sentencia [FECHA] dictada en el Recurso arriba indicado y que se remitan los autos a la Sala Primera del Tribunal Supremo, suplicando a la Excma. Sala acuerde estimar los motivos de casación alegados, casando y anulando la sentencia dictada, y confirmando la sentencia de primera instancia, con imposición a la parte recurrida de las costas del recurso de apelación.

OTROSÍ PRIMERO DIGO que, de conformidad con lo dispuesto en los apartados 3.d) y 6 de la disposición adicional decimoquinta de la LOPJ acompaño a este escrito resguardo de consignación en la cuenta de Depósitos y Consignaciones abierta a nombre del Tribunal del depósito exigido para interponer el recurso por importe de 50 euros.

Por lo que, SUPLICO A LA SALA que tenga por constituido el depósito, dejando interesada desde este momento su devolución para el caso de estimación total o parcial del recurso.

En L. y F.

(Firma Procurador y Abogado)

========================================================================
