---
name: escrito-ejecutante-impugna-defectos-procesales-civ-2884
description: "Escrito del ejecutante que impugna por defectos procesales la oposición a la ejecución. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito del ejecutante que impugna por defectos procesales la oposición a la ejecución

> Formulario **CIV-2884** del plugin **Oposición a la ejecución, tercerías y recursos en la ejecución** (`formularios-oposicion-a-la-ejecucion`) · Civil › Ejecución · normativa revisada el 25-11-2026.

## Qué es

Escrito presentado por el ejecutante impugnando, por defectos procesales, la oposición realizada por la entidad aseguradora a la ejecución del auto ejecutivo recaído en juicio penal por accidente con vehículos a motor.

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito del ejecutante que impugna por defectos procesales la oposición a la ejecución» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito del ejecutante que impugna por defectos procesales la oposición a la ejecución” para mi caso». También puedes invocarla directamente con `/formularios-oposicion-a-la-ejecucion:escrito-ejecutante-impugna-defectos-procesales-civ-2884`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-oposicion-a-la-ejecucion:indice`.

## Qué contiene esta skill

- `SKILL.md` (este fichero): qué es el formulario, para qué sirve, cómo se usa, los datos que pide, las normas que cita, los avisos de actualización y las instrucciones para Claude.
- `assets/formulario.md`: el formulario seco, tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…]. Es el texto que se rellena; no lleva explicaciones.
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Oposición a la ejecución, tercerías y recursos en la ejecución) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] COMPLETAR (4 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] DENOMINACIÓN SOCIAL
- [ ] FECHA
- [ ] LUGAR
- [ ] Nº DE CUENTA (IBAN)
- [ ] SEDE

## Normas que cita el formulario

- No cita artículos concretos; Claude localizará las normas aplicables con Jurisprudenciator si el documento las necesita.

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

- Al principio del formulario: Las sentencias del TS (1979-1993) y de Audiencias Provinciales citadas en las notas no se han podido localizar en la base oficial: sin comprobar.
- Junto a «…adas en las notas no se han podido localizar en la base oficial: sin comprobar.]»: En el hecho segundo el campo (Nº DE CUENTA (IBAN)) está mal puesto: debe exponerse el motivo (p. ej. la convivencia acreditada).
- Junto a «…convivencia acreditada).] A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Notas al pie del formulario original:
(1) De conformidad con el artículo 13del texto refundido de la Ley de Responsabilidad Civil y Seguro en la Circulación de Vehículos a Motor, cuando en un proceso penal, incoado por hecho cubierto por el seguro de responsabilidad civil de suscripción obligatoria en la circulación de vehículos de motor, recayera sentencia absolutoria, si el perjudicado no hubiera renunciado a la acción civil ni la hubiera reservado para ejercitarla separadamente, el juez o tribunal que hubiera conocido de la causa dictará auto, a instancia de parte, en el que se determinará la cantidad líquida máxima que puede reclamarse como indemnización de los daños y perjuicios sufridos por cada perjudicado, amparados por dicho seguro de suscripción obligatoria y según la valoración que corresponda con arreglo al sistema de valoración del anexo de esta Ley. En los casos de fallecimiento en accidente de circulación se dictará también el auto, a solicitud del perjudicado, cuando recaiga resolución que ponga fin, provisional o definitivamente, al proceso penal sin declaración de responsabilidad. Es importante resaltar lo de obligatorio, por cuanto el límite de ese seguro obligatorio vigente en la fecha de ocurrencia del siniestro actuará como cuantía máxima por la cual pueda dictarse el auto ejecutivo.

Continúa el artículo diciendo que el auto referido se dictará a la vista de la oferta motivada o de la respuesta motivada del asegurador o del Consorcio de Compensación de Seguros (si no constan, el juez convocará antes a una comparecencia, y el acuerdo que en ella se alcance se homologará con efectos de transacción judicial), que contra él no cabe recurso y que contendrá la descripción del hecho, la indicación de las personas y de los vehículos que intervinieron y de los aseguradores de cada uno de ellos. A título meramente ejemplificativo, el auto procederá tras una sentencia absolutoria al no resultar acreditados los hechos denunciados o al considerarse que no existió imprudencia en la conducción del vehículo por parte del denunciado...

Actualmente, los límites del aseguramiento obligatorio de la responsabilidad civil ocasionada por la circulación de vehículos de motor están fijados en el artículo 4.2 del propio texto refundido: 70 millones de euros por siniestro en los daños a las personas y 15 millones de euros por siniestro en los daños en los bienes.

Dicho auto viene a ser como un cheque o pagaré extendido contra una entidad aseguradora por un importe determinado, viniendo obligada dicha aseguradora a atender ese pago, salvo que pudiera oponer y probar (la carga de la prueba recaerá sobre ella) una serie de excepciones tasadas (fundamentalmente culpa exclusiva o fuerza mayor). En consecuencia, antes de iniciar el procedimiento ejecutivo para reclamar el auto, lo habitual es efectuar gestión extrajudicial de cobro ante la aseguradora en cuestión.

Dicho auto es título ejecutivo suficiente para iniciar el juicio ejecutivo previsto en los artículos 538 y siguientes de la LEC contra la Entidad Aseguradora.

Si la controversia sobre la oposición que se planteara en el juicio ejecutivo no pudiera resolverse con los documentos aportados con los escritos de las partes, las partes podrán solicitar la celebración de vista, que se sustanciará por los trámites del juicio verbal (nos remitimos a efectos de prueba a la propuesta en el declarativo, teniendo en cuenta que en este procedimiento es de aplicación la inversión de la carga de la prueba).

Como el auto ejecutivo sólo puede dictarse por el máximo del seguro obligatorio vigente en la fecha del siniestro, el exceso del perjuicio causado en el accidente de circulación podrá reclamarse por el procedimiento de juicio declarativo que corresponda contra el responsable directo y/o contra la entidad aseguradora con la que aquél tenga concertado el seguro voluntario (que suele coincidir con la aseguradora del obligatorio).

El plazo de prescripción de la acción es de un año desde la notificación del auto de cuantía máxima a los interesados.

(2) El plazo para impugnar la oposición por defectos procesales es de cinco días.

En sentido contrario véase la siguiente jurisprudencia:

Jurisprudencia sobre la culpa exclusiva: No se estima en las siguientes sentencias de la AP: SAP Burgos de 5-9-97, rec. 408/1997, de la que destacamos lo siguiente: «aunque es indudable la culpa del fallecido conductor de la furgoneta, no es menos cierto que no ha quedado acreditado que fuese su conducta la única causa eficiente del accidente, pues la prueba practicada pone de manifiesto que...»; SAP La Coruña de 5-12-97, rec. 776/1997; de SAP Murcia de 25-9-97, rec. 243/1996; SAP Barcelona de 14-2-97, rec. 893/1995; SAP Cádiz de 7-2-97, rec. 268/1996; SAP Badajoz de 13-12-96, rec. 639/1996; SAP Badajoz de 3-10-96, Rec. 250/1996.

Se estima la excepción por la sentencia de la AP de La Coruña de 24-10-97, Rec. 1041/1997 y de Cádiz de 24-4-97, rec. 335/1996.

Jurisprudencia sobre la fuerza mayor: La sentencia de la AP de Ciudad Real de 10 de marzo de 1995, rec. 315/1994, estimó la excepción de fuerza mayor por irrupción de un animal en la calzada que obligó al demandado a frenar bruscamente. Dice esta sentencia que la fuerza mayor «se proyecta más sobre la imprevisibilidad que sobre la inevitabilidad y es evidente que la fuerza mayor se ha producido cuando el accidente sobreviene como en este caso a causa de un animal que irrumpe sorpresivamente en la calzada, sobreviniendo el accidente a causa de la colisión del vehículo anterior, sin que nada pudiera hacer el conductor ante lo imprevisible de lo acaecido». La sentencia de la AP de Guadalajara de 28 de abril de 1994, rec. 381/1993, estimó asimismo la excepción de fuerza mayor, al haberse producido la colisión por una placa de hielo existente en la calzada..

Jurisprudencia sobre el tema de la exclusión de los daños materiales: La sentencia de la AP de Madrid de 3-10-94, rec. 608/1993, que, entendiendo que en el supuesto enjuiciado existe concurrencia de culpas, aprecia la excepción de pluspetición por lo que respecta a los daños materiales, al entender que, respecto a éstos «sólo se responde según lo establecido en los artículos 1902 y siguientes del Código Civil». En el mismo sentido se pronuncia la sentencia de la AP de Lleida de 4-7-94, rec. 15142/1996, que dice que respecto a los daños materiales «no rige el régimen cuasi-objetivo de responsabilidad someramente descrito, sino el general de responsabilidad consagrado en el art. 1902 del Código Civil».

Jurisprudencia sobre la reducción de la indemnización si coexiste culpa de la víctima. Es favorable la sentencia de la AP de Murcia de 25-9-97, rec. 243/1996; la sentencia de la AP de Lleida de 17-3-97, rec. 624/1996; de la AP de Córdoba de 20-1-97, rec. 263/1996. Esta última sentencia da, al respecto, los siguientes argumentos que por su interés reproducimos:

«a) La Ley de Circulación y Reglamentación correspondiente del Seguro Obligatorio no regula la compensación, pero tampoco la prohíbe o excluye.

b) Tal regulación no consagra, como se dice a menudo, un sistema de responsabilidad civil totalmente objetiva -pues si no, no operaría la culpa exclusiva de la víctima- por lo que no debe haber inconveniente alguno, ni es contrario a los principios inspiradores del sistema que la culpa concurrente se configure como un motivo de disminución de la indemnización correspondiente dentro de los límites de dicho Seguro.

c) Admitido que en el ámbito del seguro obligatorio hay responsabilidad civil siempre que no existe culpa exclusiva de la víctima o fuerza mayor, nada impide que en la fijación de la indemnización se tenga en cuenta la contribución de la víctima en parte a la producción del accidente.

d) El seguro obligatorio es un seguro de responsabilidad civil, es decir de personas, no de accidentes o de daños, por lo cual sería contrario a la propia naturaleza incluir los causados por la víctima a sí misma, no por tercero, de ahí que quede excluida la cobertura cuando exista culpa exclusiva del perjudicado y deba reducirse la indemnización en la parte atribuida a la propia conducta.

e) Que si bien la tesis contraria a la admisión de la compensación en el Seguro Obligatorio pudiera tener justificación en los tiempos en que sus límites cuantitativos eran escasos y aun ridículos, tal justificación hoy no existe, pues se han alcanzado cifras realmente cuantiosas, sin olvidar que la regulación legal prevé expresamente que si concurren la negligencia del conductor y la del perjudicado se procederá a la equitativa moderación de la responsabilidad y al repartimiento en la cuantía de la indemnización.» Hoy, el art. 1.2 del texto refundido aprobado por Real Decreto Legislativo 8/2004 (redacción de la Ley 35/2015) dispone que, cuando la víctima capaz de culpa civil solo contribuya a la producción del daño, se reducirán todas las indemnizaciones en atención a la culpa concurrente hasta un máximo del setenta y cinco por ciento.

Jurisprudencia sobre la prescripción de la acción: Se considera que el dies a quo lo constituye la fecha de notificación del auto de fijación de la cuantía máxima a los interesados. A este respecto, véanse las sentencias del TS de 2 de julio de 1979, de 8 de marzo de 1982, de 3 de marzo de 1983, de 15 de abril de 1987, de 14 de mayo de 1990, 3 de febrero, 5 de octubre y 13 de diciembre de 1993. Asimismo se pronuncian las Audiencias Provinciales, como la SAP Granada de 16 de septiembre de 1997, rec. 719/1996; SAP Toledo de 18 de mayo de 1995, SAP La Coruña de 20 de abril de 1993, rec. 158/1992; SAP Pontevedra de 12 de mayo de 1992, Rec. 96/1992; de Lleida de 18 de diciembre de 1995.

De ésta es destacable su supuesto de hecho: Auto de archivo de las actuaciones penales sin que por parte de S.Sª se haya dictado auto con cargo al seguro obligatorio. Transcurrido el tiempo, el interesado comparece en las actuaciones penales e interesa la notificación del auto de archivo y que se dictara el auto ejecutivo. Insiste dicha sentencia diciendo que «las diligencias penales sólo pueden darse por finiquitadas cuando se haya dictado el auto fijando la cantidad líquida reclamable por el perjudicado, que le da oportunidad de ejercitar bien la acción ejecutiva o bien la ordinaria».

Junto a este escrito deberá acompañarse la documentación que justifique las alegaciones que se efectúan.


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
