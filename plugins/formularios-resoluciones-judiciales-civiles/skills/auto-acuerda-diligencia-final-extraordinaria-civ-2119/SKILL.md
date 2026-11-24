---
name: auto-acuerda-diligencia-final-extraordinaria-civ-2119
description: "Auto que acuerda una diligencia final extraordinaria de ampliación del dictamen pericial económico. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Auto que acuerda una diligencia final extraordinaria de ampliación del dictamen pericial económico

> Formulario **CIV-2119** del plugin **Resoluciones judiciales civiles: autos, decretos y diligencias** (`formularios-resoluciones-judiciales-civiles`) · Civil › Resoluciones judiciales (autos, decretos, providencias, diligencias) · normativa revisada el 24-11-2026.

## Qué es

Auto dictado por un Juez de Primera Instancia, por la que se acuerda la práctica de diligencia final extraordinaria, de ampliación del dictamen pericial económico de la parte actora.

Es un modelo de tipo **resoluciones judiciales (autos, decretos, providencias, diligencias)**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Auto que acuerda una diligencia final extraordinaria de ampliación del dictamen pericial económico» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Auto que acuerda una diligencia final extraordinaria de ampliación del dictamen pericial económico” para mi caso». También puedes invocarla directamente con `/formularios-resoluciones-judiciales-civiles:auto-acuerda-diligencia-final-extraordinaria-civ-2119`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-resoluciones-judiciales-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Resoluciones judiciales civiles: autos, decretos y diligencias) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] FECHA (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] SEDE (2 veces)
- [ ] AÑO
- [ ] ENTIDAD BANCARIA
- [ ] LUGAR
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] Nº
- [ ] Nº DE PROCEDIMIENTO

## Normas que cita el formulario

- art. 435.2 LEC
- art. 337.2 LEC

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

- Junto a «…ado-Juez de la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. «De los de» es residuo de los varios juzgados de una plaza. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Notas al pie del formulario original:
(1) Las diligencias finales del art. 435.2 LEC son excepcionales, según indica su denominación legal, y se comprueba por los ejemplos, puesto que el asunto se podría reducir a la documental incompleta o prueba de fuente personal (testifical o pericial) frustrada, sin negligencia de parte, transcendental en su contenido para sentenciar, y que no se ha efectuado como debiera, pero que se ha efectuado, por razón de una circunstancia que se ha desvanecido luego del acto del juicio.

Los casos más frecuentes son aquellos que se ha intentado practicar la prueba, pero con resultado negativo (v.gr.: un exhorto para testifical que no se cumplimenta con declaración del testigo porque estaba hospitalizado al ser citado, en que el auxilio jurisdiccional se ha practicado, pero no la prueba), y encaja en las diligencias finales ordinarias del art. 435.1.2.ª LEC.

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

SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA N.º [NÚMERO]

PROCEDIMIENTO: Juicio Ordinario n.º [Nº DE PROCEDIMIENTO]/[AÑO]

PARTES:

Número de Identificación Informática

AUTO

En [LUGAR], a [FECHA].

ANTECEDENTES DE HECHO

ÚNICO.-

Por el Procurador/a. D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de [NOMBRE DEL REPRESENTADO/A] se ha presentado escrito en este Tribunal el día [FECHA] por el que interesa la práctica de la diligencia final de ampliación del dictamen pericial económico de dicha parte actora, ya practicado, en base a que concurrían los presupuestos legales.

FUNDAMENTOS DE DERECHO

PRIMERO.- Preceptúa el art. 435.2 LEC que excepcionalmente, el tribunal podrá acordar, de oficio o a instancia de parte, que se practiquen de nuevo pruebas sobre hechos relevantes, oportunamente alegados, si los actos de prueba anteriores no hubieran resultado conducentes a consecuencia de circunstancias ya desaparecidas e independientes de la voluntad y diligencia de las partes, siempre que existan motivos fundados para creer que las nuevas actuaciones permitirán adquirir certeza sobre aquellos hechos. Es decir, una prueba propuesta, admitida y practicada, que no ha servido para demostrar un hecho alegado, puede reproducirse si la razón de su inutilidad depende de un dato que ha cambiado, al margen de intervención de las partes.

SEGUNDO.- Se interesa que se practique como diligencia final ampliatoria del dictamen pericial del auditor censor jurado de cuentas D./Dña. [NOMBRE Y APELLIDOS], evacuado a instancias de esa parte actora, en tanto que ha aportado la parte demandada en el acto del juicio -extraviado el documento original- copia del contrato de apertura de cuenta de crédito cuya ausencia determinó que no pudiera responder su informe al punto relativo al monto de comisiones por máximo mensual de descubierto, de mantenimiento, y de reclamación de morosos, con relación a la deuda de la mercantil demandada.

Concurren los requisitos de la práctica de una prueba no conducente por causa ajena a las partes, causa que ha desaparecido, y cuya reproducción ampliatoria conducirá a la más adecuada solución del proceso, por lo que se admite la práctica de la prueba interesada, suspendiéndose el plazo para dictar sentencia, y concediendo a la actora plazo de diez días para aportar nuevo dictamen pericial, con indicación de si desea la asistencia del perito a comparecencia para dar las explicaciones del art. 337.2 LEC, lo que se trasladará a la contraparte, y luego proveerá.

PARTE DISPOSITIVA

Se acuerda la admisión de la práctica de la prueba interesada por el Procurador/a. de los Tribunales D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación del BANCO [ENTIDAD BANCARIA], de nuevo dictamen pericial económico de parte sobre el extremo omitido, en las condiciones apuntadas, suspendiéndose el plazo para dictar sentencia.

Así lo acuerda, manda y firma el Ilmo. Sr. Magistrado-Juez de la Sección Civil del Tribunal de Instancia de [SEDE], plaza n.º [Nº] [SEDE] y su partido.

Firma del Magistrado-Juez:

Contra esta resolución cabe interponer recurso de reposición, mediante escrito ante este Tribunal que se presenta dentro de los cinco días hábiles siguientes al de notificación, y en el que deberá indicarse la infracción cometida a juicio del recurrente, y sin perjuicio del cual se llevará a efecto lo acordado.

Para interponer el recurso será necesario la constitución de un depósito de 25 euros, sin cuyo requisito no será admitido a trámite. El depósito se constituirá consignando dicho importe en la Cuenta de Depósitos y Consignaciones que este Tribunal tiene abierta en el grupo Banesto (Banco Español de Crédito) con el número [NÚMERO], indicando en el campo concepto del resguardo de ingreso que se trata de un "Recurso" código 00-Reposición. La consignación deberá ser acreditada al interponer el recurso (disp. adic. 15ª de la LOPJ).

Están exentos de constituir el depósito para recurrir los incluidos en el apartado 5 de la disposición citada y quienes tengan reconocido el derecho a la asistencia jurídica gratuita.
