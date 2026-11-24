---
name: otrosi-medidas-provisionales-coetaneas-convenidas-civ-0229
description: "Otrosí de medidas provisionales coetáneas convenidas en demanda de nulidad, separación o divorcio. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Otrosí de medidas provisionales coetáneas convenidas en demanda de nulidad, separación o divorcio

> Formulario **CIV-0229** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Otrosí de medidas provisionales coetáneas convenidas en demanda de nulidad, separación o divorcio» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Otrosí de medidas provisionales coetáneas convenidas en demanda de nulidad, separación o divorcio” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:otrosi-medidas-provisionales-coetaneas-convenidas-civ-0229`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (9 veces)
- [ ] FECHA (6 veces)
- [ ] CALLE (5 veces)
- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] Nº (4 veces)
- [ ] MES (3 veces)
- [ ] AÑO (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] NOMBRE DEL HIJO/A (2 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] PISO (2 veces)
- [ ] PROFESIÓN (2 veces)
- [ ] PUERTA (2 veces)
- [ ] DNI/NIE
- [ ] ENTIDAD BANCARIA
- [ ] NÚMERO DE LA CALLE
- [ ] PROVINCIA
- [ ] TOMO

## Normas que cita el formulario

- art. 773 LEC
- art. 104 Código Civil

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

OTROSÍ DIGO que, al amparo del artículo 773 de la LEC, y no habiéndose adoptado con anterioridad medidas provisionales en relación a la separación (o divorcio o nulidad) del matrimonio, por medio del presente escrito solicito la adopción de las MEDIDAS PROVISIONALES que se dirán, acordadas por ambas partes en el convenio de medidas acompañado como documento número [Nº DE DOCUMENTO] de la demanda, en base a los siguientes HECHOS Y FUNDAMENTOS:

I. HECHOS

PRIMERO.- En la fase previa al proceso, mi representada y el demandado han llegado a un acuerdo sobre medidas provisionales que se recoge en el documento número de la demanda y cuya transcripción íntegra es la siguiente:

CONVENIO DE MEDIDAS PROVISIONALES

En la ciudad de [LOCALIDAD], a [FECHA]

REUNIDOS

De una parte,

Doña [NOMBRE Y APELLIDOS], mayor de edad, casada, de profesión [PROFESIÓN], vecina de la localidad de [LOCALIDAD], con domicilio en calle [CALLE], número [NÚMERO], piso [PISO], puerta [PUERTA], provista de DNI núm. [DNI/NIE]

Y. de otra parte,

Don [NOMBRE Y APELLIDOS], mayor de edad, casado, de profesión [PROFESIÓN], vecino de la localidad de [LOCALIDAD], con domicilio en calle [CALLE], número [NÚMERO], piso [PISO], puerta [PUERTA], provisto de DNI núm. [Nº];

Actúan ambos en nombre e interés propio, y se reconocen mutua y recíprocamente capacidad legal bastante para otorgar el presente convenio regulador, a cuyo efecto libre y espontáneamente,

MANIFIESTAN

I.-Que están casados en virtud de matrimonio celebrado en [LOCALIDAD] en forma [ELEGIR: civil / religiosa] el día [FECHA], del mes de [MES], del año [AÑO], que se encuentra inscrito en el Registro civil de [LOCALIDAD], tomo [TOMO], folio

II.-Que de este matrimonio han nacido y viven dos hijos, ambos menores de edad: [NOMBRE DEL HIJO/A], nacido/a el día [FECHA], del mes de [MES], del año [AÑO]; y [NOMBRE DEL HIJO/A], nacida/o el día [FECHA], del mes de [MES], del año

III.-El régimen económico del matrimonio es la sociedad de gananciales.

IV.-El domicilio conyugal está sito en la localidad de [LOCALIDAD], calle [CALLE], núm. [NÚMERO DE LA CALLE]

V.-Siendo voluntad de ambas partes proceder a la separación (o nulidad o divorcio), suscriben el presente convenio de medidas provisionales que han de regir durante la tramitación del proceso judicial, a fin de que sea aprobado judicialmente.

Y a tal efecto, convienen las siguientes

MEDIDAS

De la separación provisional

Se conviene la separación provisional de los cónyuges, la cual se ha producido de hecho desde el día [FECHA], con revocación de consentimientos y poderes entre cónyuges que pudieran existir.

De la patria potestad, guarda y custodia y régimen de visitas de los hijos menores del matrimonio

Que la patria potestad de los hijos menores del matrimonio quedará compartida entre ambos cónyuges, atribuyéndose a la madre la guarda y custodia del menor; estableciéndose el régimen de visitas de los hijos menores a favor del padre que, sin perjuicio del acuerdo de los padres en interés de los hijos, se establece en los siguientes términos:

A) En cuanto a los fines de semana, el padre tendrá en su compañía a sus hijos, los fines de semana alternos, desde el viernes a las 20:00 horas hasta el domingo a las 20:00 horas, correspondiendo a la madre los fines de semana de las semanas pares en cómputo anual y en consecuencia al padre los fines de semana impares de las semanas impares en cómputo anual.
B) En cuanto a las vacaciones de Navidad, los hijos pasarán la mitad de las vacaciones escolares de Navidad con su padre y la otra mitad con su madre, iniciándose el primer período el día siguiente a aquél en que finalicen las clases y finalizando el mismo, el día 31 de diciembre al mediodía. El segundo período comenzará el día 31 de diciembre al mediodía y finalizará el día inmediatamente anterior a aquel en que comiencen las clases. Los padres se alternarán cada año los distintos períodos, correspondiendo el primer período a la madre los años pares y el segundo los años impares, de forma que al padre le corresponderá los años pares el segundo período y en los años impares el primer período.
C) En cuanto a las vacaciones de Semana Santa, los hijos pasarán la mitad de las vacaciones escolares de Semana Santa con su padre y la otra mitad con su madre, iniciándose el primer período el día siguiente a aquel en que finalicen las clases y finalizando el mismo, el miércoles al mediodía. El segundo período comenzará el primer miércoles al mediodía y finalizará el día inmediatamente anterior a aquél en que comiencen las clases. Los padres se alternarán cada año los distintos períodos, correspondiéndole el primer período a la madre los años pares y el segundo los años impares, y así sucesivamente.
D) En cuanto a las vacaciones estivales, julio y agosto, los hijos pasarán la mitad de sus vacaciones con la madre y la otra mitad de sus vacaciones con el padre. Los cónyuges decidirán en cada año quién tiene en su compañía a los menores, ya en julio, ya en agosto, en función de sus ocupaciones laborales, y para el improbable supuesto de no llegar a un acuerdo, el padre será quien decida en los años impares y la madre en los años pares.

Del domicilio conyugal y ajuar familiar

El uso y disfrute del domicilio conyugal sito en la localidad de [LOCALIDAD], provincia de [PROVINCIA], calle [CALLE], núm. [Nº], queda atribuido a la madre que reside en el mismo junto con los hijos del matrimonio, fijando el esposo su domicilio en la ciudad de [LOCALIDAD], calle [CALLE], núm. [Nº], donde está residiendo actualmente.

De la contribución a las cargas familiares y a los alimentos de los hijos

El esposo abonará, en concepto de contribución a las cargas familiares y alimentos para los menores, la cantidad de [IMPORTE] euros mensuales, a pagar dentro de los cinco primeros días de cada mes, a ingresar en la cuenta núm. [Nº] que Doña [NOMBRE Y APELLIDOS] tiene abierta en la entidad financiera [ENTIDAD BANCARIA], actualizándose anualmente conforme al Índice Oficial de Precios al Consumo para el conjunto nacional.

Asimismo, y con relación a dichas cargas, el esposo asume la obligación de satisfacer en su integridad las cuotas correspondientes a la hipoteca que grava el domicilio doméstico.

Dicha cantidad se actualizará automáticamente cada doce meses, incrementándose o disminuyéndose según el IPC que publique el Instituto Nacional de Estadística u otro organismo oficial que pudiera sustituirlo.

Los gastos extraordinarios que se puedan originar mientras subsista la contribución de alimentos para los hijos deben ser sufragados por mitad entre ambos progenitores. Se entenderán como gastos extraordinarios aquellos que, derivados del estado de salud de los hijos, no sean cubiertos por la Seguridad Social; también aquellos derivados de los estudios que en un futuro lleve a término la hija común, los refuerzos y actividades escolares.

Los cónyuges manifiestan su voluntad de acudir al Tribunal competente acompañando el convenio de medidas provisionales aquí suscrito, sin perjuicio de que puedan formular las pretensiones que estimen convenientes en relación a las medidas definitivas conforme autoriza el artículo 773 de la LEC.

Y en prueba de conformidad, los comparecientes se ratifican en el contenido de todos y cada uno de los pactos que integran el presente documento, los cuales han sido redactados según sus propias instrucciones, firmándolo por triplicado y a un solo efecto en el lugar y fecha arriba indicados, quedando uno de ellos en poder de cada uno de los esposos, y el tercero en poder de esta representación a efectos de presentarlo conjuntamente con la demanda de separación (o de divorcio o de nulidad).

Dicho convenio se acompaña como documento número [Nº DE DOCUMENTO] de la demanda y aparece suscrito y firmado por ambos cónyuges en prueba de conformidad.

Pese al acuerdo alcanzado, esta parte mantiene su pretensión de que la medida definitiva relativa a la pensión por alimentos para los hijos comunes se establezca por importe de [IMPORTE] euros mensuales, tal como autoriza el artículo 773 de la LEC, al entender que se ajusta en mayor medida a los parámetros exigidos jurisprudencialmente, sin perjuicio desde luego de solicitar la aprobación de las medidas convenidas para que rijan con carácter provisional.

FUNDAMENTOS DE DERECHO

Legitimación activa y pasiva

La ostentan las respectivas partes en su condición de cónyuges, en relación con los hechos y pretensiones formuladas. En especial, invoco el artículo 104 del Código Civil y el artículo 773 de la Ley de Enjuiciamiento Civil.

Competencia

Artículo 769 y 773 de la Ley de Enjuiciamiento Civil.

Medidas a adoptar y procedimiento

Artículos 773 de la Ley de Enjuiciamiento Civil y 104 del Código civil y su remisión al artículo 103 del mismo.

Procedimiento

Artículo 773 en relación con el artículo 771 de la Ley de Enjuiciamiento Civil, al no haberse solicitado anteriormente la adopción de medidas provisionales.

Intervención del Ministerio Fiscal

Artículo 749 de la LEC

Demás normas concordantes y de aplicación: iura novit curia.

En su virtud,

SUPLICO AL TRIBUNAL: Que tenga por presentado este escrito con los documentos acompañados y sus copias; por interpuesta por el Procurador que suscribe, con quien se entiendan las sucesivas diligencias, en nombre y representación de Doña [NOMBRE Y APELLIDOS], con devolución de la escritura de poderes una vez quede testimonio en autos, demanda de MEDIDAS PROVISIONALES COETÁNEAS de separación conyugal (en su caso, nulidad o divorcio) contra Don [NOMBRE Y APELLIDOS]; y previos los trámites pertinentes y con intervención del Ministerio Fiscal, dicte Auto por el que se acuerden las medidas provisionales convenidas por ambos cónyuges en fecha [FECHA], transcritas en el hecho primero de este otrosí.

Es justicia que insto en [LOCALIDAD]

========================================================================
