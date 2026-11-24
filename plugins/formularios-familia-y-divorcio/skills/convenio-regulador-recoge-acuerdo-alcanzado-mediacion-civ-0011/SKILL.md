---
name: convenio-regulador-recoge-acuerdo-alcanzado-mediacion-civ-0011
description: "Convenio regulador que recoge un acuerdo alcanzado en mediación. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Convenio regulador que recoge un acuerdo alcanzado en mediación

> Formulario **CIV-0011** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Convenio regulador que recoge un acuerdo alcanzado en mediación» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Convenio regulador que recoge un acuerdo alcanzado en mediación” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:convenio-regulador-recoge-acuerdo-alcanzado-mediacion-civ-0011`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] MES (7 veces)
- [ ] AÑO (6 veces)
- [ ] LOCALIDAD (6 veces)
- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] Nº (5 veces)
- [ ] FECHA (4 veces)
- [ ] CALLE (3 veces)
- [ ] DÍA (3 veces)
- [ ] ENTIDAD BANCARIA (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] NOMBRE DE LA INSTITUCIÓN DE MEDIACIÓN (2 veces)
- [ ] NÚMERO DE LA CALLE
- [ ] PROVINCIA
- [ ] TOMO

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

CONVENIO REGULADOR

En la ciudad de [LOCALIDAD], a [DÍA] de [MES] de [AÑO]

MANIFIESTAN

Que están casados en virtud de matrimonio celebrado en [LOCALIDAD] en forma [ELEGIR: civil / religiosa] el día [FECHA], del mes de [MES], del año [AÑO], que se encuentra inscrito en el Registro civil de [LOCALIDAD], tomo [TOMO], folio

Que de este matrimonio han nacido y viven dos hijos, ambos menores de edad: [NOMBRE Y APELLIDOS], nacido/a el día [FECHA], del mes de [MES], del año [AÑO]; y [NOMBRE Y APELLIDOS], nacida/o el día [FECHA], del mes de [MES], del año

El régimen económico del matrimonio es el sociedad de gananciales.

El domicilio conyugal está sito en la localidad de [LOCALIDAD], calle [CALLE], núm. [NÚMERO DE LA CALLE]

Siendo voluntad de ambas partes proceder a la disolución de su matrimonio, en fecha [DÍA] de [MES] de [AÑO] iniciaron un procedimiento de mediación ante la institución de mediación [NOMBRE DE LA INSTITUCIÓN DE MEDIACIÓN], habiendo alcanzado un acuerdo de mediación en fecha [FECHA] de [MES] de

Y de conformidad con los pactos alcanzados en el acuerdo de mediación de fecha [DÍA] de [MES] de [AÑO], el cual se integra en el presente convenio como ANEXO I, suscriben el presente convenio, a fin de que sea aprobado judicialmente. Y a tal efecto, convienen los siguientes

PACTOS

De la disolución por divorcio

Ambos cónyuges, acuerdan con carácter definitivo la disolución por divorcio de su matrimonio, y declaran que nada tienen que decirse ni reclamarse por razón de la propio divorcio y de sus causas, salvo lo que en el presente documento se determina.

De la patria potestad, guarda y custodia y régimen de visitas de los hijos menores del matrimonio

Que la patria potestad de los hijos menores del matrimonio quedará compartida entre ambos cónyuges, y conviniendo la guarda y custodia compartida, teniendo en su compañía el padre a los hijos desde el mes de abril de cada año y hasta el mes de septiembre, y la madre desde el mes de octubre y hasta el mes de marzo, por lo que el régimen de visitas será alternativo en función del progenitor que tenga a los hijos menores en guarda y custodia.

El régimen de visitas del progenitor no custodio será el siguiente:

A) En cuanto a los fines de semana, tendrá en su compañía a sus hijos, los fines de semana alternos, desde el viernes a las 20:00 horas hasta el domingo a las 20:00 horas;

B) En cuanto a las vacaciones de Navidad, los hijos pasarán la mitad de las vacaciones escolares de Navidad con su padre y la otra mitad con su madre, iniciándose el primer período el día siguiente a aquél en que finalicen las clases y finalizando el mismo, el día 31 de diciembre al mediodía. El segundo período comenzará el día 31 de diciembre al mediodía y finalizará el día inmediatamente anterior a aquél en que comiencen las clases. Los padres se alternarán cada año los distintos períodos, correspondiendo el primer período a la madre los años pares y el segundo los años impares, de forma que al padre le corresponderá los años pares el segundo período y en los años impares el primer período;

C) En cuanto a las vacaciones de Semana Santa, los hijos pasarán la mitad de las vacaciones escolares de Semana Santa con su padre y la otra mitad con su madre, iniciándose el primer período el día siguiente a aquél en que finalicen las clases y finalizando el mismo, el miércoles al mediodía. El segundo período comenzará el primer miércoles al mediodía y finalizará el día inmediatamente anterior a aquél en que comiencen las clases. Los padres se alternarán cada año los distintos períodos, correspondiéndole el primer período a la madre los años pares y el segundo los años impares, y así sucesivamente; y

D) En cuanto a las vacaciones estivales, Julio y Agosto, los hijos pasarán la mitad de sus vacaciones con la madre y la otra mitad de sus vacaciones con el padre. Los cónyuges decidirán en cada año quien tiene en su compañía a los menores, ya en Julio, ya en Agosto, en función de sus ocupaciones laborales.

En el caso de que surja cualquier discrepancia en el cumplimiento de la guarda y custodia o visitas, las partes se comprometen a someter el asunto a la mediación del mediador D. o aquel otro que designe el instituto de mediación [NOMBRE DE LA INSTITUCIÓN DE MEDIACIÓN], antes de iniciar cualquier acción jurisdiccional.

Del domicilio conyugal y ajuar familiar

El uso y disfrute del domicilio conyugal sito en la localidad de [LOCALIDAD], provincia de [PROVINCIA], calle [CALLE], núm. [Nº], queda atribuido a la madre que reside en el mismo junto con los hijos del matrimonio en el periodo de custodia compartida, fijando el esposo su domicilio en la ciudad de [LOCALIDAD], calle [CALLE], núm. [Nº], donde residirán los hijos del matrimonio en el periodo de custodia compartida.

La hipoteca que grava la vivienda del hasta ahora domicilio conyugal será asumida íntegramente por la esposa, así como el Impuesto sobre Bienes Inmuebles (IBI) y cualquier otro importe que tenga su origen en la propiedad del inmueble, y los servicios de suministros y mantenimiento de la finca.

En cuanto al ajuar doméstico y objetos de uso ordinario que se encuentran en el domicilio conyugal, nada cabe acordar, dado que ya han sido previamente repartidos de común acuerdo entre ambos consortes con anterioridad a la firma del presente documento.

De la contribución a los alimentos de los hijos

El padre contribuirá a la alimentación, cuidado y educación de sus hijos mediante el pago de una pensión alimenticia que se fija en la cantidad de [IMPORTE] EUROS MENSUALES (.- €/mes), la cual satisfacerá únicamente durante el periodo que la madre ejerza la custodia.

Esta pensión se calcula en función de la capacidad económica de los padres y compensando los periodos de custodia que a cada uno de ellos corresponde.

Dicha pensión se abonará, dentro de los cinco primeros días de cada mes, en la cuenta bancaria núm. [Nº], que la Sra. tiene abierta en la entidad financiera [ENTIDAD BANCARIA], oficina núm. [Nº]

Dicha pensión se actualizará automáticamente cada doce meses, incrementándose o disminuyéndose según el IPC que publique el Instituto Nacional de Estadística u otro organismo oficial que pudiera sustituirle.

Los gastos extraordinarios que se puedan originar mientras subsista la contribución de alimentos para los hijos serán sufragados por el padre. Se entenderán como gastos extraordinarios aquellos que derivados del estado de salud de los hijos no sean cubiertos por la Seguridad Social, también aquellos derivados de los estudios que en un futuro lleve a término la hija común, los refuerzos y actividades escolares.

De la pensión compensatoria

Se establece como pensión compensatoria en favor de la esposa la cantidad de [IMPORTE] EUROS MENSUALES (.- euros/mes), que deberá ingresar Don [NOMBRE Y APELLIDOS] en la cuenta de Doña [NOMBRE Y APELLIDOS], núm. [Nº], de la entidad financiera [ENTIDAD BANCARIA], y que deberá actualizar anualmente, cada mes de enero, a partir del mes de enero del año [AÑO], conforme al Índice Oficial de precios al Consumo para el conjunto del Estado.

De la disolución del régimen económico matrimonial

Dado que el régimen económico es el de sociedad de gananciales, y que los únicos bienes que lo conforman son el domicilio que ha venido siendo conyugal y muebles constitutivos del ajuar doméstico, ambas partes consideran oportuno diferir su liquidación al momento en que dichos bienes dejen de quedar afectados del derecho de uso anteriormente establecido. Entre tanto, Doña [NOMBRE Y APELLIDOS] correrá a cargo de todos los gastos que la propiedad comporte.

El presente convenio plasma el acuerdo de mediación incorporado como ANEXO I y resuelve todas las diferencias existentes entre los cónyuges e implica transacción de todas las cuestiones planteadas entre los mismos, por lo que ambos se comprometen a solicitar su divorcio de mutuo acuerdo, constituyendo el presente documento como PROPUESTA DEL CONVENIO REGULADOR de todos sus efectos, conforme a lo previsto en el Artículo 90 CC.

Los cónyuges manifiestan su voluntad de acudir al Tribunal competente para obtener su divorcio, acompañando a la demanda de divorcio de mutuo acuerdo el convenio aquí estipulado.

Y en prueba de conformidad, los comparecientes se ratifican en el contenido de todos y cada uno de los pactos que integran el presente documento, los cuales han sido redactados según sus propias instrucciones, firmándolo por triplicado y a un solo efecto en el lugar y fecha arriba indicados, quedando uno de ellos en poder de cada uno de los esposos, y el tercero en poder de esta representación a efectos de a presentarlo con la demanda de separación de mutuo acuerdo.

Fdo.: Fdo.:

========================================================================
