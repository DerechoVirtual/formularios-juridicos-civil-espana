---
name: escrito-declinatoria-haberse-sometido-cuestion-civ-1761
description: "Escrito de declinatoria por haberse sometido la cuestión a mediación. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito de declinatoria por haberse sometido la cuestión a mediación

> Formulario **CIV-1761** del plugin **Mediación, MASC, arbitraje y jurisdicción voluntaria** (`formularios-mediacion-arbitraje-y-voluntaria`) · Civil › Jurisdicción voluntaria, MASC, mediación y arbitraje · normativa revisada el 24-11-2026.

## Qué es

Declinatoria por sometimiento de la cuestión a mediación.

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito de declinatoria por haberse sometido la cuestión a mediación» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito de declinatoria por haberse sometido la cuestión a mediación” para mi caso». También puedes invocarla directamente con `/formularios-mediacion-arbitraje-y-voluntaria:escrito-declinatoria-haberse-sometido-cuestion-civ-1761`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-mediacion-arbitraje-y-voluntaria:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Mediación, MASC, arbitraje y jurisdicción voluntaria) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (3 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] Nº (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] AÑO
- [ ] COLEGIO
- [ ] DENOMINACIÓN SOCIAL
- [ ] IMPORTE
- [ ] LUGAR
- [ ] NOMBRE DE LA INSTITUCIÓN DE MEDIACIÓN
- [ ] NOMBRE DEL SOLICITANTE
- [ ] Nº DE DOCUMENTO

## Normas que cita el formulario

- art. 63.2 LEC
- art. 63.1 LEC
- art. 10.2 Ley 5/2012
- art. 39 LEC

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

- Junto a «…A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA N.º [NÚMERO] de [LOCALIDAD]»: Regla general: el TI tiene Sección Única, de Civil y de Instrucción; solo en los partidos que fija la Ley 38/1988 hay Sección Civil separada. Donde no la haya: «A LA SECCIÓN ÚNICA, DE CIVIL Y DE INSTRUCCIÓN, DEL TRIBUNAL DE INSTANCIA DE…». Fuente: LOPJ art. 84.2 (redacc. LO 1/2025, BOE-A-2025-76).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Notas al pie del formulario original:
(1) El art. 10.2 LM exige compromiso de mediación y su inicio; por lo que el supuesto se adapta a un procedimiento de mediación iniciado. Ciertamente el escrito tendrá menos operatividad en la práctica que el que tendría sobre la base de un contrato de sometimiento a mediación sin que ésta se hubiera iniciado, algo que es habitual en arbitraje, puesto que no será normal que iniciado ese proceso de mediación, una de las partes, sin romperlo, demande a la otra, y genere la necesidad de la declinatoria.

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

A LA SECCIÓN CIVIL DEL TRIBUNAL DE INSTANCIA N.º [NÚMERO] de [LOCALIDAD]

D./Dña. [NOMBRE Y APELLIDOS] Procurador/a de los Tribunales y de la entidad [DENOMINACIÓN SOCIAL], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], con la dirección técnica del Letrado ejerciente D./ Dña. [NOMBRE Y APELLIDOS], del Colegio de Abogados de [COLEGIO], con despacho profesional abierto en [LOCALIDAD], en los autos de juicio ordinario n.º [Nº], seguidos a instancia de [NOMBRE DEL SOLICITANTE]; comparezco y como mejor en Derecho proceda, DIGO:

Que por medio del presente escrito, formulo declinatoria de jurisdicción por sometimiento de la cuestión a mediación en plazo legal de los diez primeros días posteriores al emplazamiento para contestar a la demanda, y ello conforme a los siguientes

HECHOS

PRIMERO.- Que mi principal ha sido emplazada por decreto del Letrado/a de la Administración de Justicia de fecha [FECHA], a fin de que comparezca y conteste como demandado, si es su interés, en el presente juicio, en que se ejercita acción de resolución de contrato de permuta y correlativa reclamación de [IMPORTE]) euros de daños y perjuicios.

SEGUNDO.- Como se acredita mediante copia del acta de la sesión informativa celebrada, como documento n.° [NÚMERO] del presente escrito, las partes contratantes y aquí litigiosas se encuentran inmersas en un procedimiento de mediación, con n.º [Nº]/[AÑO] desarrollado ante la Institución [NOMBRE DE LA INSTITUCIÓN DE MEDIACIÓN], y dirigida por el mediador D./Dña. [NOMBRE Y APELLIDOS]; habiéndose emplazado a las partes a la sesión constitutiva que tendrá lugar el próximo día [FECHA].

TERCERO.- Resulta evidente que el litigio se encuentra sometido a procedimiento de mediación, aceptado voluntariamente por las partes, lo que excluye a la Jurisdicción contenciosa que nos ocupa.

A dichos hechos son de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

PRIMERO.- El presente escrito se presenta ante el Tribunal a quien tengo el honor de dirigirme, el cual está conociendo del asunto, conforme a lo dispuesto en el art. 63.2 LEC, puesto que se ha admitido la demanda y se le considera competente.

SEGUNDO.- Conforme a lo dispuesto en el art. 63.1 LEC, mi mandante tiene personalidad jurídica propia y actúa por medio de sus representantes legales, con plena capacidad para ser parte y comparecer en juicio, estando legitimada para proponer esta cuestión de competencia, al haber sido demandada en el proceso.

TERCERO.- Al no excepcionarse las normas generales de postulación, y siendo incidente previo en un juicio ordinario, se comparece con Procurador de los Tribunales habilitado ante el tribunal, y con dirección de Letrado en ejercicio que redacta y suscribe (arts. 23.1 y 31.1 LEC).

CUARTO.- La declinatoria constituye el cauce común para plantear cualquier defecto de jurisdicción y competencia (art. 63.1 LEC), siendo su trámite el del art. 65, que en este supuesto abocará a abstenerse de conocer el Tribunal y sobreseer el juicio (art. 65.2, párrafo 2.º LEC), y surtirá el efecto de suspender, hasta que sea resuelta y mediante resolución del Letrado de la Administración de Justicia, el cómputo para contestar a la demanda y el curso del procedimiento principal.

QUINTO.- De conformidad con la posibilidad prevista en el art. 10.2 de la Ley 5/2012, de 6 de julio, de mediación en asuntos civiles y mercantiles, mi mandante, como parte del proceso de mediación en curso, interesa la presente declinatoria a fin de que no se desarrolle ninguna actuación judicial como la que nos ocupa, cuanto menos, durante el tiempo que dure la mediación recién iniciada que versa sobre el conflicto entre las partes, que es objeto de la demanda que da pie al presente procedimiento.

En este sentido, y tal y como dispone el mencionado precepto legal, concurren los presupuestos exigidos, dado que las partes se han comprometido a someterse a mediación y la misma se ha iniciado, como se puede observar en el acta de la sesión informativa aportada y firmada por ambas partes. Asimismo, la demanda no viene acompañada de ninguna suerte de medidas cautelares u otras medidas urgentes, constituyendo una acción judicial que no puede ser ejercitada por la contraparte.

En consecuencia, de acuerdo con el art. 39 LEC, mi mandante puede denunciar mediante declinatoria la falta de jurisdicción por haberse sometido a mediación la controversia, procediendo que, tras la tramitación del presente incidente, se dicte auto por el cual el Tribunal sobresea el juicio ordinario, absteniéndose de conocer del mismo.

Por lo expuesto,

SUPLICO AL TRIBUNAL

que teniendo por presentado este escrito con su copia, se digne admitir uno y otra, y me tenga por comparecido y parte en nombre y derecho propios, tenga por formulada cuestión declinatoria de jurisdicción, por haberse sometido a mediación la controversia, se suspenda por el Letrado de la Administración de Justicia el curso del proceso, se de traslado de la misma a parte actora, a fin de que alegue lo que tenga por conveniente; y se dicte finalmente auto por el cual el Tribunal se abstenga de conocer y sobresea el proceso, con condena en costas procesales a la demandante, y con lo demás que proceda

Es justicia de hacerse en [LUGAR], a [FECHA].

Firma del Abogado/a	Firma del Procurador/a
