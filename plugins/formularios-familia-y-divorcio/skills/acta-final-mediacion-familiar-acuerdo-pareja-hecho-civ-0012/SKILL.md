---
name: acta-final-mediacion-familiar-acuerdo-pareja-hecho-civ-0012
description: "Acta final de mediación familiar con acuerdo de una pareja de hecho con hijos menores. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Acta final de mediación familiar con acuerdo de una pareja de hecho con hijos menores

> Formulario **CIV-0012** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Acta final de mediación familiar con acuerdo de una pareja de hecho con hijos menores» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Acta final de mediación familiar con acuerdo de una pareja de hecho con hijos menores” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:acta-final-mediacion-familiar-acuerdo-pareja-hecho-civ-0012`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] Nº (3 veces)
- [ ] CALLE (2 veces)
- [ ] CORREO ELECTRÓNICO (2 veces)
- [ ] DNI/NIE (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] LETRA (2 veces)
- [ ] MES (2 veces)
- [ ] PISO (2 veces)
- [ ] AÑO
- [ ] DATOS DEL MEDIADOR
- [ ] DÍA
- [ ] FECHA
- [ ] LEY AUTONÓMICA DE MEDIACIÓN

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

Número de expediente

Institución de mediación

Partes:

Personas mediadas

D. [NOMBRE Y APELLIDOS], mayor de edad, con DNI [DNI/NIE], y domiciliado en [DOMICILIO], C.P., calle [CALLE], núm. [Nº], piso [PISO], letra [LETRA], dirección electrónica [CORREO ELECTRÓNICO], y teléfono

Y Dª [NOMBRE Y APELLIDOS], mayor de edad, con DNI [DNI/NIE], y domiciliada en [DOMICILIO], C.P., calle [CALLE], núm. [Nº], piso [PISO], letra [LETRA], dirección electrónica [CORREO ELECTRÓNICO] y teléfono

Mediador: D. [NOMBRE Y APELLIDOS], [DATOS DEL MEDIADOR]

EXPONEN

Que las partes manifestaron su voluntad de someter a mediación el conflicto entre ellas existente por razón de su intención de cesar en la convivencia como unión estable de pareja, según consta en acta de sesión constitutiva de fecha [FECHA] de [MES] de

Que la mediación tenía como objeto dirimir las controversias derivadas del cese de la unión de hecho de los mediados, en especial en relación a los efectos en orden a la guarda, custodia, visitas y pensión alimenticia en relación a la hija común [NOMBRE Y APELLIDOS], de [Nº] años de edad.

Que se ha seguido el procedimiento de mediación ajustado a las previsiones de la Ley [LEY AUTONÓMICA DE MEDIACIÓN], habiendo intervenido el mediador que suscribe este acta.

Las partes declaran haber participado en la mediación de forma totalmente libre y voluntaria y un ACUERDO sobre su objeto, el cual se refleja a todos los efectos en este acta final, firmándose por las partes en prueba de conformidad, y el cual se conviene en los siguientes

TÉRMINOS

Ambos progenitores ejercerán conjuntamente la patria potestad sobre la hija común. En cambio, la guarda y custodia será individual de la madre.

La hija común convivirá con el padre y estará en su compañía, durante los días y períodos que a continuación se indican:

a.- Fines de semana alternos, desde el viernes a la salida del colegio hasta el domingo a las veintiuna horas, más dos tardes entre semana -martes y jueves, salvo que acuerden otros días- desde la salida del colegio hasta las 21 horas.

b.- Días festivos intersemanales alternos, desde las 10 a las 20 horas, salvo que se trate de un viernes o lunes, pues en este último supuesto se atribuirá el día de fiesta al progenitor que haya tenido consigo a la niña ese fin de semana. Lo dispuesto en este punto no operará en los períodos vacacionales de Semana Santa, Navidad y verano.

En todos los supuestos, el padre -o la persona que designe- recogerá a la niña en el domicilio materno -o en el colegio, según proceda- al inicio de los períodos y lo devolverá a dicho domicilio al final.

c.- Las vacaciones escolares de Navidad y Semana Santa se distribuirán de la siguiente manera: i) Las de Navidad se dividirán en dos períodos: el primero comprenderá desde el momento de la finalización del colegio hasta el día 30 de diciembre a las 20 horas; y el segundo desde este día y hora hasta el último día de vacaciones a las 20 horas; y ii) Las de Semana Santa se dividirán también en dos períodos: el primero comprenderá desde el momento de la finalización del colegio hasta el Miércoles Santo a las 20 horas; y el segundo desde este día y hora hasta el último día de vacaciones a las 20 horas.

En ambos períodos vacacionales la hija estará con el padre durante el primer período y con la madre el segundo en los años pares; en los años impares se procederá a la inversa.

d.- Las vacaciones de verano se dividirán en dos períodos que comprenderán los siguientes días: el primero, desde el día siguiente a la finalización del curso escolar a las 12 horas, hasta el 31 de julio a las 20 horas; el segundo, desde este día y hora hasta el penúltimo día de vacaciones a las 20 horas. En los años pares la niña estará con el padre durante el primer período, y con la madre durante el segundo; en los años impares se procederá a la inversa.

Durante los días y períodos que un progenitor no tenga a la hija en su compañía, podrá comunicarse con ella por cualquier medio que considere oportuno, pero respetando, en todo caso, los horarios de descanso de la hija y del otro progenitor y los horarios y obligaciones educacionales. El mismo derecho tendrá la hija.

Se fija en SEISCIENTOS EUROS (600 €) durante los doce meses del año, la pensión con la que el padre contribuirá a la manutención, educación y demás necesidades de la hija. Esta cantidad será entregada a la madre por meses anticipados dentro de los cinco primeros días de cada mes, ingresándola en la cuenta corriente que ella indique, y se revisará anual y automáticamente en función de las variaciones que experimente el I.P.C.

Los gastos extraordinarios serán sufragados por mitad entre los progenitores, entendiéndose por tales gastos los derivados de la salud no cubiertos por la Seguridad Social, así como matrículas, colonias, excursiones y actividades extraescolares.

La pensión subsistirá mientras la hija no sea autosuficiente económicamente.

Se atribuye a la madre e hija el uso del domicilio donde se llevó a cabo la convivencia, sito en [LOCALIDAD], así como el ajuar familiar.

El padre fija su domicilio en [LOCALIDAD]

Ambas partes se comprometen a notificar inmediatamente cualquier cambio de domicilio.

Los progenitores se comprometen también a cumplir los anteriores pactos, a no molestarse ni provocar cuestiones entre ellos, a solucionar de mutuo acuerdo cuantas contingencias pudieran plantearse en el futuro y a no interferirse en sus respectivas vidas privadas.

Ambas partes se comprometen a suscribir los documentos necesarios para homologar el presente acuerdo, a fin de que sea aprobado por la autoridad judicial, facultándose recíprocamente para ello.

Y a los efectos de la finalización del procedimiento de mediación, se firma el presente acuerdo en tres ejemplares, por el mediador, y por las partes que en él han intervenido, con entrega de un ejemplar a cada uno de los intervinientes, en la ciudad de [LOCALIDAD], a [DÍA] de [MES] de [AÑO]

Firma de las partes y del mediador

========================================================================
