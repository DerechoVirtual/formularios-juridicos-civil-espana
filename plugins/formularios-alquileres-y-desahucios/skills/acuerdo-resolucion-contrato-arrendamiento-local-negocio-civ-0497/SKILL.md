---
name: acuerdo-resolucion-contrato-arrendamiento-local-negocio-civ-0497
description: "Acuerdo de resolución del contrato de arrendamiento de local de negocio. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Acuerdo de resolución del contrato de arrendamiento de local de negocio

> Formulario **CIV-0497** del plugin **Alquileres y desahucios** (`formularios-alquileres-y-desahucios`) · Civil › Arrendamientos y desahucio · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Acuerdo de resolución del contrato de arrendamiento de local de negocio» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Acuerdo de resolución del contrato de arrendamiento de local de negocio” para mi caso». También puedes invocarla directamente con `/formularios-alquileres-y-desahucios:acuerdo-resolucion-contrato-arrendamiento-local-negocio-civ-0497`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-alquileres-y-desahucios:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Alquileres y desahucios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (5 veces)
- [ ] FECHA (4 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] CALLE (3 veces)
- [ ] AÑO
- [ ] DNI/NIE
- [ ] DOMICILIO
- [ ] DÍA
- [ ] FOLIO
- [ ] IMPORTE
- [ ] LIBRO
- [ ] MES
- [ ] NÚMERO DE LA CALLE
- [ ] PORCENTAJE
- [ ] TOMO
- [ ] ÓRGANO O PERSONA

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

En [LOCALIDAD], a [DÍA] de [MES] 20 [AÑO]

Comparecen:

De una parte [NOMBRE Y APELLIDOS], como ARRENDADOR (persona física o jurídica)

(Persona física: D/D.ª [NOMBRE Y APELLIDOS] mayor de edad, casado, con domicilio en [LOCALIDAD] c/ [CALLE] núm. con DNI/NIF núm. [DNI/NIE])

(Persona jurídica: constituida en escritura pública otorgada el día [FECHA] ante Notario de [LOCALIDAD] D/D.ª [NOMBRE Y APELLIDOS] e inscrita en el Registro Mercantil de [LOCALIDAD] Libro [LIBRO] Tomo [TOMO] Folio [FOLIO] domiciliada en [DOMICILIO] calle [CALLE] núm. [NÚMERO DE LA CALLE] y con CIF núm. representada por [ÓRGANO O PERSONA], mayor de edad, con domicilio en [LOCALIDAD] c/ [CALLE] núm. con DNI/NIF núm. cuyas facultades derivan del poder otorgando por el notario D/D.ª [NOMBRE Y APELLIDOS], debidamente inscrito, que es declarado vigente y sin modificación alguna)

De otra parte, como ARRENDATARIO (persona física o jurídica)

Ambas partes se reconocieron en su día con carácter mutuo y capacidad legal suficiente para otorgar el presente contrato de arrendamiento de local de negocio, que en este acto pasa a resolverse, para lo cual las partes se reconocen nuevamente con carácter mutuo y capacidad legal suficiente y manifiestan:

1. Que el ARRENDADOR y EL ARRENDATARIO suscribieron contrato de arrendamiento de local de negocio con fecha [FECHA] (detallar), sometiéndose desde entonces a los pactos contemplados.

2. Que con fecha de [FECHA] (detallar) el ARRENDATARIO puso en conocimiento del ARRENDADOR su decisión de desistir unilateralmente y con efectos a partir de la fecha [FECHA] (detallar), como consecuencia de las dificultades económicas por las que atraviesa el ARRENDATARIO que le impiden continuar utilizando el local de negocios.

3. Tras las negociaciones habidas entre el ARRENDADOR y el ARRENDATARIO ambas partes han acordado proceder a la resolución del correspondiente contrato de arrendamiento y para ello

Convienen

1. El contrato de arrendamiento celebrado entre el ARRENDADOR y el ARRENDATARIO queda resuelto desde la fecha… (detallar).

2. Como consecuencia de la resolución anticipada del contrato por voluntad unilateral del ARRENDATARIO, éste debe abonar al ARRENDADOR en concepto de pena por incumplimiento y de indemnización por daños y perjuicios la cantidad equivalente al [PORCENTAJE] % (detallar porcentaje) del importe de las rentas no vencidas hasta el cumplimiento íntegro del contrato. El importe de la cantidad adeudada se eleva hasta € (detallar en número y en letra). El pago del citado importe se realizará mediante abono en la cuenta corriente del ARRENDADOR donde habitualmente se realizaba el abono del precio del arrendamiento, o mediante cheque nominativo emitido por el correspondiente valor, a favor del ARRENDADOR. Servirá como carta de pago el presente documento.

Además, el ARRENDATARIO pierde a favor del ARRENDADOR el importe de la fianza constituida con ocasión de la celebración del presente contrato, por la cantidad de [IMPORTE] € (detallar en letra y en número).

En ese acto, el ARRENDATARIO hace entregar al ARRENDADOR de las llaves del local objeto del contrato, así como su plena posesión. Por su parte, el ARRENDADOR entrega al ARRENDATARIO el original del aval bancario a primer requerimiento que se había constituido como garantía en el momento de la firma de contrato ahora resuelto

3. El ARRENDADOR ha tenido la oportunidad de inspeccionar el local de negocios objeto del contrato de arrendamiento y comprobar que no existe ningún desperfecto imputable a la conducta del ARRENDATARIO, antes de la firma del presente documento.

4. El ARRENDATARIO se compromete por el presente documento, a no dejar pendiente de pago ningún gasto, coste o servicio relacionado con los suministros contratados para el funcionamiento del local de negocio. Si tras la resolución del contrato se devengara algún gasto que fuera imputable al ARRENDATARIO y cuya reclamación llegara al ARRENDADOR, éste podrá reclamar contra el ARRENDATARIO el importe de tales gastos, costes o servicios.

5. El incumplimiento por el ARRENDATARIO de cualquiera de las obligaciones asumidas en virtud de la firma del presente documento, facultará al ARRENDADOR a ejercitar las acciones legales que sean oportunas, sin necesidad de requerimiento previo en tal sentido.

6. Sin perjuicio de las circunstancias que pudieran concurrir, reseñadas en las cláusulas anteriores, ambas partes reconocen que ya no tienen ninguna reclamación que hacerse al una a la otra derivada de la celebración del contrato de arrendamiento de local de negocio que en este acto queda resuelto, para lo cual firman el presente documento.

EL ARRENDADOR EL ARRENDATARIO
