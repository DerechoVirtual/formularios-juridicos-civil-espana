---
name: escrito-sucinto-inicial-oposicion-declaracion-no-civ-0139
description: "Escrito sucinto inicial de oposición a la declaración de no idoneidad para adoptar. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito sucinto inicial de oposición a la declaración de no idoneidad para adoptar

> Formulario **CIV-0139** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Al Tribunal Comparecencia Presentación de escrito sucinto inicial de oposición a la declaración de no idoneidad HECHOS FUNDAMENTOS DE DERECHO Suplico Firmas

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito sucinto inicial de oposición a la declaración de no idoneidad para adoptar» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito sucinto inicial de oposición a la declaración de no idoneidad para adoptar” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:escrito-sucinto-inicial-oposicion-declaracion-no-civ-0139`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] AÑO (5 veces)
- [ ] DÍA (5 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] MES (5 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] NÚMERO (2 veces)
- [ ] COLEGIO
- [ ] LUGAR
- [ ] Nº DE DOCUMENTO
- [ ] ÓRGANO ADMINISTRATIVO
- [ ] ÓRGANO O PERSONA

## Normas que cita el formulario

- art. 780.2 LEC
- art. 779 LEC
- art. 780 LEC
- art. 753 LEC
- art. 780.4 LEC

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

- Junto a «…CIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA NÚMERO DE [LOCALIDAD]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…L DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).]»: desde la LO 1/2025 la familia, la infancia y los apoyos corresponden a la Sección de Familia, Infancia y Capacidad del Tribunal de Instancia (arts. 84.2.a y 86 LOPJ); donde no exista, a la Sección Civil o Única.

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

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA NÚMERO DE [LOCALIDAD]

D./Dª [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, en nombre y representación de D./Dª [NOMBRE Y APELLIDOS] y de y de D./Dª [NOMBRE Y APELLIDOS], cuya representación acreditaré mediante comparecencia apud acta cuando sea requerido para ello o bien: “según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño", comparezco en este TRIBUNAL con la asistencia del Letrado D. /Dª [NOMBRE Y APELLIDOS], del Ilustre Colegio de Abogados de [COLEGIO], y DIGO

Que por medio del presente escrito y en la representación que ostento, presento, conforme a lo dispuesto en el art. 780.2 LEC, ESCRITO INICIAL DE OPOSICIÓN A LA RESOLUCIÓN ADMINISTRATIVA DE NO IDONEIDAD dictada en fecha [DÍA] de [MES] de [AÑO] por la Delegación Territorial de [LOCALIDAD] del Departamento de Acción social (o Consellería de Bienestar Social, o lo que corresponda según la Comunidad Autónoma de que se trate) de la Comunidad Autónoma de [LOCALIDAD], en expediente de adopción nacional/internacional número [NÚMERO], conforme a los siguientes.

HECHOS

PRIMERO.- En fecha [DÍA] de [MES] de [AÑO], se dictó por [ÓRGANO ADMINISTRATIVO] de la Comunidad Autónoma de [LOCALIDAD] resolución administrativa por la que declaró la no idoneidad del solicitante en el expediente de adopción nacional/internacional número [NÚMERO].

La citada resolución fue notificada a mis mandantes en fecha [DÍA] de [MES] de [AÑO] (el párrafo segundo del art. 780.2 LEC, introducido por Ley 26/2015, de 28 de julio, establece la obligación de consignar expresamente en el escrito inicial de oposición a las resoluciones administrativas en materia de protección de menores, la fecha de notificación de la resolución administrativa).

Se acompaña como DOCUMENTO Nº [Nº DE DOCUMENTO] testimonio de la citada resolución.

SEGUNDO.- En la resolución de referencia se considera que las razones que mueven al solicitante a la adopción no son las adecuadas, con lo cual manifiesta éste su absoluta disconformidad, de ahí su intención de oponerse a aquélla.

TERCERO.- No consta a mi mandante la existencia de otros procedimientos relativos al menor declarado en desamparo. (El párrafo segundo del art. 780.2 LEC, introducido por Ley 26/2015, de 28 de julio, establece el deber de manifestar, en el escrito inicial de oposición a las resoluciones administrativas en materia de protección de menores, si existen procedimientos relativos a ese menor.)

Resultan aplicables a los anteriores hechos, los siguientes.

FUNDAMENTOS DE DERECHO

I. COMPETENCIA.- La competencia corresponde a este Tribunal, conforme al art. 779 LEC, que la atribuye al Tribunal de Instancia del domicilio de la entidad pública.

II. LEGITIMACIÓN.- La ostenta el abajo firmante como solicitante de adopción, cuya idoneidad niega la resolución que se impugna.

III. PROCEDIMIENTO. Dispone el art. 780 LEC: “1. No será necesaria reclamación previa en vía administrativa para formular oposición, ante los Tribunales civiles, a las resoluciones administrativas en materia de protección de menores. La oposición a las mismas podrá formularse en el plazo de dos meses desde su notificación.

Estarán legitimados para formular oposición a las resoluciones administrativas en materia de protección de menores, siempre que tengan interés legítimo y directo en tal resolución, los menores afectados por la resolución, los progenitores, tutores, acogedores, guardadores, el Ministerio Fiscal y aquellas personas que expresamente la ley les reconozca tal legitimación. Aunque no fueran actores podrán personarse en cualquier momento en el procedimiento, sin que se retrotraigan las actuaciones.

Los menores tendrán derecho a ser parte y a ser oídos en el proceso conforme a lo establecido en la Ley Orgánica de Protección Jurídica del Menor. Ejercitarán sus pretensiones en relación a las resoluciones administrativas que les afecten a través de sus representantes legales siempre que no tengan intereses contrapuestos a los suyos, o a través de la persona que se designe como su defensor para que les represente.

2. El proceso de oposición a una resolución administrativa en materia de protección de menores se iniciará mediante la presentación de un escrito inicial en el que el actor sucintamente expresará la pretensión y la resolución a que se opone.

En el escrito consignará expresamente la fecha de notificación de la resolución administrativa y manifestará si existen procedimientos relativos a ese menor.

3. El Letrado de la Administración del Estado reclamará a la entidad administrativa un testimonio completo del expediente, que deberá ser aportado en el plazo de veinte días.

4. Recibido el testimonio del expediente administrativo, el Letrado de la Administración del Estado emplazará al actor por veinte días para que presente la demanda, que se tramitará con arreglo a lo previsto en el artículo 753.

5. Si el Ministerio Fiscal, las partes o el Juez competente tuvieren conocimiento de la existencia de más de un procedimiento de oposición a resoluciones administrativas relativas a la protección de un mismo menor, pedirán los primeros y dispondrá el segundo, incluso de oficio, la acumulación ante el Tribunal que estuviera conociendo del procedimiento más antiguo.

Acordada la acumulación, se procederá según dispone el artículo 84, con la especialidad de que no se suspenderá la vista que ya estuviera señalada si fuera posible tramitar el resto de procesos acumulados dentro del plazo determinado por el señalamiento. En caso contrario, el Letrado de la Administración del Estado acordará la suspensión del que tuviera la vista ya fijada, hasta que los otros se hallen en el mismo estado, procediendo a realizar el nuevo señalamiento para todos con carácter preferente y, en todo caso, dentro de los diez días siguientes.

Contra el auto que deniegue la acumulación podrán interponerse los recursos de reposición y apelación sin efectos suspensivos. Contra el auto que acuerde la acumulación no se dará recurso alguno.”

El art. 753 LEC, por su parte, se remite a los trámites del juicio verbal, con las especialidades que el mismo precepto establece.

En su virtud:

SUPLICO AL TRIBUNAL: Que teniendo por presentado este escrito, en tiempo y forma, con los documentos que se acompañan, se sirva admitirlo y tenga por interpuesto ESCRITO INICIAL DE OPOSICIÓN A LA DECLARACIÓN DE NO IDONEIDAD efectuada por resolución de fecha [DÍA] de [MES] de [AÑO] dictada por [ÓRGANO O PERSONA] organismo autonómico que corresponda de la Comunidad Autónoma de [LOCALIDAD]; y, a la vista de lo expuesto y previa reclamación de testimonio completo del expediente administrativo, que deberá ser aportado en el plazo de veinte días, el Letrado de la Administración del Estado emplace a esta parte para la presentación, en tiempo el plazo es de veinte días, según dispone el art. 780.4 LEC y forma, de la correspondiente demanda, que se tramitará con arreglo a lo previsto en el artículo 753 LEC, según dispone el art. 780.4 LEC.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma del solicitante

========================================================================
