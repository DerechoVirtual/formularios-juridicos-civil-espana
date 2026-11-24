---
name: decreto-admite-demanda-reconvencion-emplaza-contestar-civ-1856
description: "Decreto que admite la demanda y la reconvención y emplaza para contestar. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Decreto que admite la demanda y la reconvención y emplaza para contestar

> Formulario **CIV-1856** del plugin **Resoluciones judiciales civiles: autos, decretos y diligencias** (`formularios-resoluciones-judiciales-civiles`) · Civil › Resoluciones judiciales (autos, decretos, providencias, diligencias) · normativa revisada el 24-11-2026.

## Qué es

Decreto del Letrado de la Administración de Justicia que, en un proceso de separación matrimonial, tiene por contestada la demanda por el demandado y el Ministerio Fiscal, admite a trámite la reconvención formulada por el demandado (art. 770, regla 2.ª, LEC) y emplaza al actor para contestarla.

Es un modelo de tipo **resoluciones judiciales (autos, decretos, providencias, diligencias)**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Decreto que admite la demanda y la reconvención y emplaza para contestar» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Decreto que admite la demanda y la reconvención y emplaza para contestar” para mi caso». También puedes invocarla directamente con `/formularios-resoluciones-judiciales-civiles:decreto-admite-demanda-reconvencion-emplaza-contestar-civ-1856`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-resoluciones-judiciales-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Resoluciones judiciales civiles: autos, decretos y diligencias) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS DEL DEMANDADO (3 veces)
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A (3 veces)
- [ ] AÑO
- [ ] DÍA
- [ ] FECHA
- [ ] FIRMA
- [ ] GRUPO
- [ ] LOCALIDAD
- [ ] MES
- [ ] NOMBRE Y APELLIDOS
- [ ] NOMBRE Y APELLIDOS DEL DEMANDANTE
- [ ] Nº DE CUENTA

## Normas que cita el formulario

- art. 6 LEC
- art. 770 LEC

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

DECRETO DEL LETRADO/A DE LA ADMINISTRACIÓN DE JUSTICIA

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Sr./Sra. Letrado/a de la Administración de Justicia [NOMBRE Y APELLIDOS]

ANTECEDENTES DE HECHO

PRIMERO.– En el presente proceso, promovido por el/la Procurador/a de los Tribunales Sr./Sra. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDANTE], se formuló demanda de separación del matrimonio, habiéndose emplazado a la parte demandada D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDADO], el día [FECHA], para que compareciera en el proceso y contestara a la demanda en el plazo de veinte días.

SEGUNDO.– Dentro de dicho plazo, el/la Procurador/a de los Tribunales Sr./Sra. [NOMBRE Y APELLIDOS DEL PROCURADOR/A], como mandatario procesal de D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDADO], ha comparecido en el juicio, presentando escrito de contestación a la demanda y planteando reconvención frente a la parte actora, en solicitud de que se declare [ELEGIR: la disolución del matrimonio por causa de divorcio / la nulidad del matrimonio] y solicitando determinadas medidas definitivas.

Igualmente, el Ministerio Fiscal ha presentado, dentro de plazo, escrito de contestación a la demanda, con sus copias.

FUNDAMENTOS DE DERECHO

PRIMERO.– En cuanto a la contestación de la demanda, debe tenerse en cuenta que se han presentado dentro de plazo la del Fiscal y la de la parte demandada, y esta cumple con los requisitos de capacidad, representación y postulación procesales necesarios para comparecer en juicio conforme a lo determinado en los arts. 6, 7 y 750 LEC, de modo que procede tener a dicha parte por comparecida y contestada la demanda.

SEGUNDO.– Dispone la regla 2.ª del art. 770 LEC que solo se admitirá la reconvención:

a) Cuando se funde en alguna de las causas que pueden dar lugar a la nulidad del matrimonio.

b) Cuando el cónyuge demandado de separación o de nulidad pretenda el divorcio.

c) Cuando el cónyuge demandado de nulidad pretenda la separación.

d) Cuando el cónyuge demandado pretenda la adopción de medidas definitivas que no hubieran sido solicitadas en la demanda y sobre las que el tribunal no deba pronunciarse de oficio.

En el presente caso, la reconvención formulada cumple con dicha exigencia, por cuanto la pretensión reconvencional es que [ELEGIR: se declare la disolución del matrimonio por divorcio / se declare la nulidad del matrimonio], así como, en su caso, la adopción de medidas distintas de las que se solicitan con la demanda y sobre las que el juez no debe pronunciarse de oficio, por lo que procede su admisión, dando traslado de la misma a la parte actora para que la conteste en el plazo señalado en el precepto indicado.

PARTE DISPOSITIVA

1.– Se tiene al/a la Procurador/a de los Tribunales Sr./Sra. [NOMBRE Y APELLIDOS DEL PROCURADOR/A] por comparecido/a en este proceso en nombre y representación de la parte demandada D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDADO] y por contestada la demanda.

Asimismo se tiene por contestada la demanda por el Ministerio Fiscal, uniéndose el escrito a los autos y entregándose las copias a las demás partes.

2.– Se admite a trámite la reconvención formulada por la parte demandada, cuya pretensión se sustanciará y decidirá al propio tiempo y en la misma forma que las pretensiones objeto de la demanda principal.

3.– Dése traslado de la reconvención a la parte actora para que la conteste en el plazo de diez días hábiles siguientes a la notificación de la misma.

Dése traslado por el mismo plazo y finalidad al Ministerio Fiscal.

Devuélvase el poder presentado, previo su testimonio en autos.

Contra esta resolución cabe interponer recurso de reposición, mediante escrito ante el LAJ que se presentará dentro de los cinco días hábiles siguientes al de notificación, y en el que deberá indicarse la infracción cometida a juicio del recurrente, y sin perjuicio del cual se llevará a efecto lo acordado.

Para interponer el recurso será necesaria la constitución de un depósito de 25 euros, sin cuyo requisito no será admitido a trámite. El depósito se constituirá consignando dicho importe en la Cuenta de Depósitos y Consignaciones que este Tribunal tiene abierta en el grupo [GRUPO] con el número [Nº DE CUENTA], indicando en el campo concepto del resguardo de ingreso que se trata de un «Recurso» código 00-Reposición. La consignación deberá ser acreditada al interponer el recurso (disp. adic. 15.ª LOPJ).

Están exentos de constituir el depósito para recurrir los incluidos en el apartado 5 de la disposición citada y quienes tengan reconocido el derecho a la asistencia jurídica gratuita.

Así lo acuerdo y firmo.

Firma del Letrado/a de la Administración de Justicia: [FIRMA]
