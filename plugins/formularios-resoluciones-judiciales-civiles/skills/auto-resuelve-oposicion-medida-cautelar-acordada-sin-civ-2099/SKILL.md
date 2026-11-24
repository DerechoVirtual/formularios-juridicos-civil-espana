---
name: auto-resuelve-oposicion-medida-cautelar-acordada-sin-civ-2099
description: "Auto que resuelve la oposición a una medida cautelar acordada sin audiencia previa. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Auto que resuelve la oposición a una medida cautelar acordada sin audiencia previa

> Formulario **CIV-2099** del plugin **Resoluciones judiciales civiles: autos, decretos y diligencias** (`formularios-resoluciones-judiciales-civiles`) · Civil › Resoluciones judiciales (autos, decretos, providencias, diligencias) · normativa revisada el 24-11-2026.

## Qué es

Auto que resuelve la oposición a la medida cautelar de embargo preventivo de bienes, manteniendo éste si bien reduce la cantidad que garantizará y accediendo a la sustitución de dicho embargo preventivo reducido por caución para asegurar el efectivo cumplimiento de la sentencia estimatoria que se dictare, en forma de aval bancario indefinido, y en plazo de diez días.

Es un modelo de tipo **resoluciones judiciales (autos, decretos, providencias, diligencias)**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Auto que resuelve la oposición a una medida cautelar acordada sin audiencia previa» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Auto que resuelve la oposición a una medida cautelar acordada sin audiencia previa” para mi caso». También puedes invocarla directamente con `/formularios-resoluciones-judiciales-civiles:auto-resuelve-oposicion-medida-cautelar-acordada-sin-civ-2099`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-resoluciones-judiciales-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Resoluciones judiciales civiles: autos, decretos y diligencias) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] DENOMINACIÓN SOCIAL (6 veces)
- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] FECHA (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] IMPORTE EN CIFRA (2 veces)
- [ ] GRUPO
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] NÚMERO

## Normas que cita el formulario

- art. 727 LEC
- art. 726 LEC
- art. 746 LEC
- art. 1.258 CC
- art. 741.2 LEC
- art. 394.2 LEC
- art. 735.2 LEC

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

Notas al pie del formulario original:
(1) Si se alzaren, se condenará al actor a las costas y al pago de los daños y perjuicios que éstas hayan producido (art. 741.2 párrafos 2.º y 3.º LEC y art. 742 LEC).

(2) Estimando la oposición formulada por el Procurador D. [NOMBRE Y APELLIDOS]..., en nombre y presentación de WW, S.A., a la medida cautelar acordada sin su previa audiencia a instancias de la Procuradora D./Dña. [NOMBRE Y APELLIDOS]..., en nombre y representación de D. [NOMBRE Y APELLIDOS]..., se alza el embargo preventivo de bienes de responsabilidad de WW, S.A. por la cantidad que se reclama y otros... euros (... €) calculados para intereses y costas.

Se impone a la parte demandante el pago de las costas de este incidente y se le condena a indemnizar los daños y perjuicios que se hayan ocasionado, los cuales se harán efectivos, una vez firme el presente, por los trámites previstos en los arts. 712 y ss. LEC.

========================================================================


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

AUTO

En [LUGAR], a [FECHA].

Juez Sr/a.

ANTECEDENTES DE HECHO

PRIMERO

Por auto de este Tribunal de fecha [FECHA], accediendo a lo solicitado por el Procurador/a Sr./a [NOMBRE Y APELLIDOS], en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS], se acordó la medida cautelar consistente en embargo preventivo de la demandada [DENOMINACIÓN SOCIAL], S.A., bajo presupuesto de la ejecución de la medida de la prestación de caución de [IMPORTE] euros ( €), en forma de aval bancario, dentro del plazo de cinco días.

SEGUNDO

Dentro de los veinte días siguientes a la notificación a la parte demandada del meritado auto, por el Procurador/a Sr./a [NOMBRE Y APELLIDOS], en nombre y representación de [NOMBRE DEL REPRESENTADO/A], S.A., se ha deducido oposición a la medida cautelar, en escrito que alegaba falta de presupuestos de la medida cautelar, oferta de contracautela en cantidad de [IMPORTE], y al final, exceso del embargo e insuficiencia de la caución del demandante.

TERCERO

Las partes fueron convocadas a vista por el LAJ, en la que alegaron lo que a su derecho convino, practicándose por su orden la prueba que propusieron y fue admitida como pertinente, con el resultado que obra en soporte audiovisual, además de resumido en acta.

RAZONAMIENTOS JURÍDICOS

PRIMERO

El embargo preventivo es la primera de las medidas cautelares previstas en el art. 727 LEC, y el principio es la oportunidad de decretarlo en pretensiones pecuniarias, a instancia de parte, como aseguramientos temporales, provisionales e instrumentales de la efectividad de una futurible estimación con condena al sujeto pasivo de la medida, y lo mismo que es posible sustituirlas siempre por otras menos onerosas para el demandado (art. 726 LEC), su misma finalidad se cumple con la caución sustitutoria por el sujeto pasivo (art. 746 LEC).

En el caso presente, el peligro de mora procesal es evidente cuando el eventual deudor -que admite los parámetros del crédito, el contrato y el devengo de comisiones, y un impago- nos dice que sus bienes son escasamente los que han sido embargados y atraviesa dificultades financieras serias, es decir, el objetivo peligro de retardo. A ello se suma el indicio "oscuro" de la comunidad de componentes de [DENOMINACIÓN SOCIAL], S.A. y [DENOMINACIÓN SOCIAL], S.A., es decir, una sospecha de infructuosidad.

La apariencia de buen derecho nace de la antedicha admisión de las diferencias de comisiones, y del hecho de que no tiene fundamento que se sostenga que las comisiones del contrato del Sr. Zubero estuvieran sometidas " a los avatares del mercado y de las ventas", sino que el contrato formalizado por escrito, según consta en autos, contemple la rebaja respecto a los pactos retributivos por la comitente, y a que, en principio -se trata de un juicio indiciario- se contemplen datos por lo que puedan alterarse las comisiones unilateralmente por la empresa, conforme a reglas generales -arts. 1.091, 1.257 párrafo 1.º CCiv y art. 1.258 CCiv- y a las particulares de la ley especial de ‘ius cogens’ -art. 3.1 ‘in fine’ LAG-.

SEGUNDO

Muy otra cosa es que la cantidad del embargo que se garantiza arropa una reclamación, que consecuentemente con lo anterior, también tiene buena apariencia jurídica, pero que se liquida por la parte actora a su voluntad, como es arriesgado pronunciarse sobre si la mora es automática desde el devengo o no.

Es por ello que, limitado al importe de las comisiones aparentemente adeudadas y el cincuenta por ciento de la indemnización, sin intereses, se ha de reducir la cantidad que sea objeto de caución sustitutoria. Ésta, sin que se haya enfrentado el actor a que se acuerde, se justifica indiciariamente en la situación económica que aduce WW, S.A., una vez que demuestra la liberación de embargo precedente con documento apropiado.

TERCERO

Previene el art. 741.2 LEC que, si se mantuvieren las medidas se condenará al opositor a las costas de la oposición, y la solicitud de fijación de caución sustitutoria, estimada, se solicitó como pedimento subsidiario y no único, si bien, aunque en el mantenimiento se produce, se limita la cantidad que debe garantizarse, de modo que se aplicarán criterios del art. 394.2 LEC.

PARTE DISPOSITIVA

Desestimando en parte la oposición formulada por el Procurador D./Dña. [NOMBRE Y APELLIDOS], en nombre y presentación de [DENOMINACIÓN SOCIAL], S.A., a la medida cautelar acordada sin su previa audiencia a instancias de la Procuradora D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS], se mantiene la medida de embargo preventivo de bienes de responsabilidad de [DENOMINACIÓN SOCIAL], S.A., si bien se reduce la cantidad que garantizará a la deeuros (€ [IMPORTE EN CIFRA]).

Se accede a que, en sustitución de dicho embargo preventivo reducido, se preste caución por [DENOMINACIÓN SOCIAL], S.A., en cantidad de las predichaseuros (€ [IMPORTE EN CIFRA]), para asegurar el efectivo cumplimiento de la sentencia estimatoria que se dictare, en forma de aval bancario indefinido, y en plazo de diez días.

Las costas del incidente serán a cargo de cada parte.

La presente resolución no es firme, por cuanto pueden interponer Recurso de Apelación para ante la Iltma. Audiencia Provincial en el plazo de cinco días hábiles contados desde el siguiente de la notificación, mediante escrito ante este Tribunal exponiendo el apelante las alegaciones en que se base la impugnación, además de citar la resolución apelada y los pronunciamientos que impugna (arts. 455 y 458.2 LEC), careciendo tal Recurso de efectos suspensivos de lo acordado, conforme al art. 735.2 'in fine' LEC.

Para interponer el recurso será necesaria la constitución de un depósito de 50 euros, sin cuyo requisito no será admitido a trámite. El depósito se constituirá consignando dicho importe en la Cuenta de Depósitos y Consignaciones que este Tribunal tiene abierta en el grupo [GRUPO] con el número [NÚMERO], indicando en el campo concepto del resguardo de ingreso que se trata de un "Recurso" código 02-Apelación. La consignación deberá ser acreditada al interponer el recurso (disp. adic. 15.ª de la LOPJ).

No están obligados a constituir el depósito para recurrir los declarados exentos en la disposición citada y quienes tengan reconocido el derecho a la asistencia jurídica gratuita.

Así lo acuerdo, mando y firmo:

Lo acuerda, manda y firma el Ilmo. Sr./a:

Juez de Instrucción de [LOCALIDAD]

Firma del Juez:
