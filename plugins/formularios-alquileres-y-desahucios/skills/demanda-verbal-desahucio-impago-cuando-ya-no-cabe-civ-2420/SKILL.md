---
name: demanda-verbal-desahucio-impago-cuando-ya-no-cabe-civ-2420
description: "Demanda verbal de desahucio por impago cuando ya no cabe enervar la acción. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda verbal de desahucio por impago cuando ya no cabe enervar la acción

> Formulario **CIV-2420** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 25-11-2026.

## Qué es

Demanda de Juicio Verbal de desahucio por falta de pago de la renta de la vivienda arrendada, no procediendo la enervación por haber tenido ya anteriormente una, de conformidad con lo establecido en los artículos 439 y 22 LEC 2000.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda verbal de desahucio por impago cuando ya no cabe enervar la acción» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda verbal de desahucio por impago cuando ya no cabe enervar la acción” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:demanda-verbal-desahucio-impago-cuando-ya-no-cabe-civ-2420`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- `SKILL.md` (este fichero): qué es el formulario, para qué sirve, cómo se usa, los datos que pide, las normas que cita, los avisos de actualización y las instrucciones para Claude.
- `assets/formulario.md`: el formulario seco, tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…]. Es el texto que se rellena; no lleva explicaciones.
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] COMPLETAR (24 veces)
- [ ] NOMBRE Y APELLIDOS (11 veces)
- [ ] CALLE (6 veces)
- [ ] NÚMERO (6 veces)
- [ ] IMPORTE (5 veces)
- [ ] FECHA (4 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] Nº (2 veces)
- [ ] PISO (2 veces)
- [ ] SEDE (2 veces)
- [ ] TELÉFONO (2 veces)
- [ ] AÑO
- [ ] FECHAS
- [ ] LUGAR
- [ ] TIPO Y Nº DE PROCEDIMIENTO

## Normas que cita el formulario

- art. 439.6 LEC
- art. 439.3 LEC
- art. 22.4 LEC
- art. 36 LEC
- art. 45 LEC
- art. 52.1.7.º LEC
- art. 23 LEC
- art. 250.1.1.º LEC
- art. 253 LEC
- art. 3 k) Ley 12/2023
- art. 5 Ley Orgánica 1/2025
- art. 27.2.a Ley 29/1994
- art. 438.5 LEC
- art. 22.6 LEC
- art. 549.3 LEC
- art. 399.1 LEC

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

- Al principio del formulario: Los hechos sobre vivienda habitual y patrimonio del actor son un ejemplo: adaptarlos y aportar la certificación registral si se niega la condición de gran tenedor (art. 439.6 LEC).
- Junto a «…tificación registral si se niega la condición de gran tenedor (art. 439.6 LEC).]»: La enervación anterior no impide una nueva si el cobro se frustró por causa imputable al arrendador (art. 22.4 LEC).
- Junto a «…dor (art. 439.6 LEC).]»: Arrendatario vulnerable: posible suspensión hasta el 31-12-2030 (art. 2 RDL 29/2026) y trámite del art. 441.5-7 LEC.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Notas al pie del formulario original:
(1) Son aplicables aquí las mismas consideraciones que en Formulario anterior ("Demanda de Juicio Verbal de desahucio por falta de pago"), si bien en este caso con la particularidad de que no cabrá la enervación de la acción de desahucio por falta de pago al haberse enervado ya en una ocasión anterior. Recuérdese que constituye requisito de admisibilidad de la demanda (art. 439.3 LEC) determinar en la misma las circunstancias que puedan permitir o no la enervación del desahucio.

Conforme a lo previsto en la regla 9 del art. 251 LEC, en la nueva redacción conferida al mismo por Ley 19/2009, de 23 de noviembre, en los juicios sobre arrendamiento de bienes, salvo cuando tengan por objeto reclamaciones de las rentas o cantidades debidas, la cuantía de la demanda será el importe de una anualidad de renta, cualquiera que sea la periodicidad con que ésta aparezca fijada en el contrato.

El art. 438.5 LEC, introducido por RDL 6/2023, establece que en los casos de demandas en las que se ejercite la pretensión de desahucio por falta de pago de rentas o cantidades debidas, acumulando o no la pretensión de condena al pago de las mismas, el Letrado de la Administración de Justicia, tras la admisión, y previamente a la vista que se señale, requerirá al demandado para que, en el plazo de diez días, desaloje el inmueble, pague al actor o, en caso de pretender la enervación, pague la totalidad de lo que deba o ponga a disposición de aquel en el tribunal o notarialmente el importe de las cantidades reclamadas en la demanda y el de las que adeude en el momento de dicho pago enervador del desahucio; o en otro caso comparezca ante éste y alegue sucintamente, formulando oposición, las razones por las que, a su entender, no debe, en todo o en parte, la cantidad reclamada o las circunstancias relativas a la procedencia de la enervación.

Si el demandante ha expresado en su demanda que asume el compromiso a que se refiere el apartado 3 del artículo 437, se le pondrá de manifiesto en el requerimiento, y la aceptación de este compromiso equivaldrá a un allanamiento con los efectos del artículo 21.

Además, el requerimiento expresará el día y la hora que se hubieran señalado para que tengan lugar la eventual vista en caso de oposición del demandando, para la que servirá de citación, y el día y la hora exactos para la práctica del lanzamiento en caso de que no hubiera oposición. Asimismo se expresará que en caso de solicitar asistencia jurídica gratuita el demandado, deberá hacerlo en los tres días siguientes a la práctica del requerimiento, así como que la falta de oposición al requerimiento supondrá la prestación de su consentimiento a la resolución del contrato de arrendamiento que le vincula con el arrendador.

El requerimiento se practicará en la forma prevista en el artículo 161 de esta Ley, teniendo en cuenta las previsiones contenidas en apartado 3 del artículo 155 y en el último párrafo del artículo 164, apercibiendo al demandado de que, de no realizar ninguna de las actuaciones citadas, se procederá a su inmediato lanzamiento, sin necesidad de notificación posterior, así como de los demás extremos comprendidos en el apartado siguiente de este mismo artículo.

Si el demandado no atendiere el requerimiento de pago o no compareciere para oponerse o allanarse, el Letrado de la Administración de Justicia dictará decreto dando por terminado el juicio de desahucio y se procederá el lanzamiento en la fecha fijada.

Si el demandado atendiere el requerimiento en cuanto al desalojo del inmueble sin formular oposición ni pagar la cantidad que se reclamase, el Letrado de la Administración de Justicia lo hará constar, y dictará decreto dando por terminado el procedimiento, y dejando sin efecto la diligencia de lanzamiento, a no ser que el demandante interese su mantenimiento para que se levante acta sobre el estado en que se encuentre la finca, dando traslado al demandante para que inste el despacho de ejecución en cuanto a la cantidad reclamada, bastando para ello con la mera solicitud.

El art. 437.3 LEC último inciso, señala que puede interesarse en la demanda que se tenga por solicitada la ejecución del lanzamiento en el día y hora que se fije por el Tribunal a los efectos señalados en el art. 549.3 LEC. Esta norma dispone que en la sentencia condenatoria de desahucio por falta de pago de las rentas o cantidades debidas, o por expiración legal o contractual del plazo, o en los decretos que pongan fin al referido desahucio si no hubiera oposición al requerimiento, la solicitud de su ejecución en la demanda de desahucio será suficiente para la ejecución directa de dichas resoluciones, sin necesidad de ningún otro trámite para proceder al lanzamiento en el día y hora señalados en la propia sentencia o en la fecha que se hubiera fijado al ordenar la realización del requerimiento al demandado.

En el caso de situaciones concursales, debe tenerse en cuenta lo previsto en los arts. 44, 156 y siguientes y 168 del texto refundido de la Ley Concursal, aprobado por Real Decreto Legislativo 1/2020, de 5 de mayo, que entró en vigor el 1 de septiembre de 2020.

(2) Normativa aplicable

Real Decreto de 24 de julio de 1889, texto de la edición del Código Civil mandada publicar en cumplimento de la Ley de 26 de mayo último: Art. 1543, 1555, 1569.2º

Ley 29/1994, de 24 de noviembre, de Arrendamientos Urbanos: Art. 27.2.a

Ley 1/2000, de 7 de enero, de Enjuiciamiento Civil: Art. 22.4, 438.5 y 438.6.

(3) Jurisprudencia de interés

Tribunal Supremo, Sala Primera, de lo Civil, Sentencia 335/2014 de 23 de junio, Rec. 1437/2013

Audiencia Provincial de Barcelona, Sección 4ª, Sentencia 58/2014 de 11 de febrero, Rec. 820/2012

Audiencia Provincial de Madrid, Sección 21ª, Sentencia 20/2008 de 29 de enero, rec. 305/2006


### Flujo

1. **Paso 0**: comprueba Jurisprudenciator (arriba).
2. Lee entero `assets/formulario.md` (el formulario que vas a rellenar, en la carpeta de esta skill) y la parte de `../indice/marco.md` que afecte al caso. Limítate a la materia de este formulario: no añadas contenido ajeno a él.
3. Pide los datos de la lista en una sola tanda. Si un dato aparece varias veces, aclara a qué persona o acto corresponde cada vez. Lo que el usuario no sepa se queda como hueco visible con su etiqueta (p. ej. [FECHA]).
4. Resuelve cada [ELEGIR …] y cada [OPCIONAL …] según los hechos, y sustituye cualquier indicación entre paréntesis del formulario («(se describirá…)», «(indicar…)») por el contenido que corresponda. Redacta las partes que dependen del caso (hechos, motivos, descripción de bienes).
5. Aplica los avisos de actualización en el lugar que indican. Comprueba con `buscar_articulo` cada norma citada; si alguna ha cambiado, usa la redacción vigente. Si citas jurisprudencia, localízala con `buscar_sentencias` o `buscar_por_cita` y léela con `leer_sentencias`.
6. Antes de entregarlo, pasa `verificar_escrito` con las frases que citan normas o sentencias y corrige lo que señale.
7. **Documento final = el formulario tal cual, rellenado y limpio.**
   - Empieza exactamente por la primera línea de `assets/formulario.md` y sigue su estructura y su orden hasta la firma.
   - No pongas en el documento título, nombre del formulario o de la skill, código, encabezados, «Para qué sirve», leyendas, avisos, notas de uso, comentarios ni explicaciones. Tampoco marcas [ELEGIR…] u [OPCIONAL…]: ya están resueltas.
   - Formato Word (.docx, con la skill de Word disponible): **Times New Roman 11 pt** en todo el documento, **interlineado 1,15**, **texto justificado**, márgenes de 2,5 cm. Los rótulos del formulario (REUNIDOS, CLÁUSULAS, HECHOS, SUPLICO…) en su propia línea y en negrita, sin cambiar su texto.
8. En el chat (nunca dentro del documento): datos pendientes, partes redactadas por ti, normas y sentencias comprobadas con Jurisprudenciator (y, si algún dato sale de internet, cuál y su enlace) y, si es un escrito judicial o administrativo, el plazo y el órgano ante el que se presenta.

El resultado es un borrador para que lo revise un profesional antes de usarlo.
