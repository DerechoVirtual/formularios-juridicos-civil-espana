---
name: escritura-poder-miseria-civ-0911
description: "Escritura de poder de miseria. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escritura de poder de miseria

> Formulario **CIV-0911** del plugin **Proceso civil: demandas, contestaciones, prueba y vista** (`formularios-proceso-civil`) · Civil › Escritos procesales (demanda, contestación, prueba, vista) · normativa revisada el 24-11-2026.

## Qué es

Escritura notarial de poder general por la que el poderdante apodera a una persona de su confianza para realizar actos de administración y de disposición sobre sus bienes y derechos, y para representarle ante tribunales, oficinas y organismos.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escritura de poder de miseria» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escritura de poder de miseria” para mi caso». También puedes invocarla directamente con `/formularios-proceso-civil:escritura-poder-miseria-civ-0911`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-proceso-civil:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Proceso civil: demandas, contestaciones, prueba y vista) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (6 veces)
- [ ] AÑO (3 veces)
- [ ] CALLE (3 veces)
- [ ] DNI/NIE (3 veces)
- [ ] DÍA (3 veces)
- [ ] MES (3 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] LETRA (2 veces)
- [ ] Nº (2 veces)
- [ ] PISO (2 veces)
- [ ] CARGO
- [ ] COLEGIO NOTARIAL
- [ ] DENOMINACIÓN SOCIAL
- [ ] DOMICILIO
- [ ] NOMBRE DEL NOTARIO
- [ ] NOMBRE Y APELLIDOS DEL APODERADO
- [ ] Nº DE FOLIOS
- [ ] NÚMEROS
- [ ] PROFESIÓN
- [ ] SERIE

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

### Avisos de actualización (1) — se aplican en el texto, nunca se copian en el documento

- Al principio del formulario: el título original de este formulario («poder de miseria») no se corresponde con el texto, que es un poder general para actos de administración, de disposición y de representación procesal; se ha reconstruido el texto original. Si se pretende un poder con alcance limitado, deben suprimirse las facultades que no se deseen conferir.

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

En [LOCALIDAD], mi residencia, a [DÍA] de [MES] de [AÑO].

Ante mí, [NOMBRE DEL NOTARIO], Notario del Ilustre Colegio Notarial de [COLEGIO NOTARIAL], y al efecto de otorgar escritura de poder.

COMPARECE/N:

Don/Doña [NOMBRE Y APELLIDOS], mayor de edad, [ELEGIR: casado/a / soltero/a], vecino/a de [LOCALIDAD], con domicilio en [LOCALIDAD], en la calle [CALLE], número [Nº], piso [PISO], letra [LETRA], con DNI/NIE número [DNI/NIE].

[OPCIONAL — incluir si hay más de un compareciente]
Don/Doña [NOMBRE Y APELLIDOS], mayor de edad, [ELEGIR: casado/a / soltero/a], vecino/a de [LOCALIDAD], con domicilio en [LOCALIDAD], en la calle [CALLE], número [Nº], piso [PISO], letra [LETRA], con DNI/NIE número [DNI/NIE].

INTERVIENE/N

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— En nombre propio: [ELEGIR: Interviene en su propio nombre y derecho. / Intervienen ambos en su propio nombre y derecho.]

— En representación: Don/Doña [NOMBRE Y APELLIDOS], en nombre y representación de [DENOMINACIÓN SOCIAL], constituida el [DÍA] de [MES] de [AÑO], ejerce esta representación como [CARGO], estando facultado/a para este otorgamiento por acuerdo de fecha [DÍA] de [MES] de [AÑO], según resulta de la certificación o escritura de poder que se incorpora a esta matriz. Me asegura el/la compareciente la vigencia de esta representación.

TIENE/N, a mi juicio, la capacidad legal necesaria para formalizar esta escritura de PODER PARA REALIZAR ACTOS DE ADMINISTRACIÓN Y DISPOSICIÓN, y a tal efecto,

EXPONEN

TÍTULO

Que por medio del presente instrumento público confiere/n poder, tan amplio como fuere necesario en Derecho, a favor de Don/Doña [NOMBRE Y APELLIDOS DEL APODERADO], mayor de edad, de profesión [PROFESIÓN], vecino/a de [LOCALIDAD], domiciliado/a en [DOMICILIO], calle [CALLE], con DNI/NIE número [DNI/NIE], para que, en nombre y representación del/de la compareciente, pueda realizar los actos siguientes con plenitud de competencias, atribuciones y facultades, y con libertad para fijar pactos, cláusulas, disposiciones, determinaciones y declaraciones, de suerte que el/la apoderado/a ostente la plena representación del/de la poderdante sin traba, limitación ni excepción alguna.

FACULTADES

FACULTADES DE ADMINISTRACIÓN

Administrar bienes muebles e inmuebles; ejercitar y cumplir toda clase de derechos y obligaciones; rendir, exigir y aprobar cuentas; firmar y seguir correspondencia; hacer y retirar giros y envíos; constituir, modificar, extinguir y liquidar contratos de todo tipo, particularmente de arrendamiento, aparcería, seguro, trabajo y transporte de cualquier clase; desahuciar inquilinos, arrendatarios, aparceros, colonos, porteros, precaristas y todo género de ocupantes; admitir y despedir obreros y empleados; reconocer, aceptar, pagar y cobrar cualesquiera deudas y créditos, por capital, intereses, dividendos y amortizaciones, y con relación a cualquier persona o entidad pública o privada, incluso el Estado, Comunidad Autónoma, provincia, municipio o cualquier otra entidad, firmando recibos, saldos, conformidades y resguardos; asistir con voz y voto a juntas de regantes, propietarios, consocios, condueños y demás cotitulares o de cualquier otra clase.

FACULTADES DE DISPOSICIÓN

— Disponer, enajenar, gravar, adquirir y contratar activa o pasivamente, respecto de toda clase de bienes muebles o inmuebles, derechos reales y personales, acciones y obligaciones, cupones, valores y cualesquiera efectos públicos o privados, pudiendo en tal sentido, con las condiciones y por el precio de contado, confesado o aplazado que estime pertinentes, ejercitar, otorgar, conceder y aceptar compraventas, aportes, permutas, cesiones en pago y para pago, amortizaciones, rescates, subrogaciones, retractos, opciones y tanteos, agrupaciones, segregaciones, parcelaciones, divisiones, declaraciones de obra nueva y de obra derruida, alteraciones de fincas, cartas de pago, fianzas, transacciones, arbitrajes; constituir, reconocer, aceptar, ejecutar, transmitir, dividir, modificar, extinguir y cancelar, total o parcialmente, usufructos, servidumbres, prendas, hipotecas, anticresis, comunidades de toda clase, propiedades horizontales, censos, derechos de superficie y, en general, cualesquiera derechos reales y personales; y aceptar donaciones puras, condicionales u onerosas de cualquier clase de bienes.

— Aceptar, repudiar, manifestar, partir, entregar, recibir, aprobar e impugnar herencias, legados, liquidaciones de sociedades y, en general, bienes y derechos de todas clases y en todo caso.

— Comerciar, dirigir y administrar negocios mercantiles e industriales, realizando cualesquiera actos relativos al tráfico mercantil; tomar parte en concursos y subastas, formulando propuestas, reservas y protestas y aceptando adjudicaciones; constituir, modificar, prorrogar, disolver y liquidar toda clase de sociedades, ejercitar los derechos y obligaciones inherentes a la cualidad de socio y aceptar y desempeñar cargos en ellas.

— Librar, aceptar, avalar, endosar, cobrar, pagar, intervenir y protestar letras de cambio, talones, cheques y otros efectos; abrir, seguir, cancelar y liquidar libretas de ahorro, cuentas corrientes y de crédito, con garantía personal o de valores; concertar activa o pasivamente créditos comerciales; afianzar y dar garantías por otros; dar y tomar dinero en préstamo, con o sin interés y con garantía personal, de valores o cualquier otra; constituir, transferir, modificar, cancelar y retirar depósitos provisionales o definitivos, de metálico, valores y otros bienes; comprar, vender, canjear, pignorar y negociar efectos y valores, y cobrar sus intereses, dividendos y amortizaciones; arrendar cajas de seguridad; y, en general, operar con cajas de ahorro, bancos, incluso el de España y otros oficiales, y entidades similares, disponiendo de los bienes existentes en ellos por cualquier concepto, y haciendo, en general, cuanto permita la legislación y la práctica bancarias.

FACULTADES DE REPRESENTACIÓN PROCESAL

Comparecer en Tribunales, Fiscalías, sindicatos, delegaciones, jurados, comisiones, notarías, registros y toda clase de oficinas públicas o privadas, autoridades y organismos del Estado, Comunidad Autónoma, provincia y municipio, en asuntos civiles, mercantiles, penales, administrativos, económico-administrativos, contencioso-administrativos, sociales o laborales, gubernativos, fiscales y constitucionales, de todos los grados, jurisdicciones e instancias; promover, iniciar, instar, seguir, contestar y terminar, como actor, solicitante, demandante, coadyuvante, requerido, demandado, oponente, interviniente o en cualquier otro concepto, toda clase de expedientes, actas, juicios, pretensiones, tramitaciones, declaraciones, quejas y recursos, incluso de casación o acciones autónomas de impugnación y recursos de amparo, con facultades de formalizar ratificaciones personales, desistimiento, renuncia y allanamiento; otorgar, para los fines antedichos, poderes en favor de Procuradores de los Tribunales, Letrados y Graduados Sociales, con las facultades usuales.

Sustituir este poder en todo o en parte, revocar las sustituciones conferidas; pedir y retirar copias de esta escritura.

Así lo dice y otorga el/la compareciente (o los comparecientes), quien/es, enterado/s de su derecho a leer por sí este documento, procedo por su elección a la lectura del mismo, en cuyo contenido se ratifica/n y firma/n.

Y yo, el Notario, DOY FE de identificar a los comparecientes por medio de sus documentos nacionales de identidad y de todo lo demás contenido en este instrumento público, extendido en [Nº DE FOLIOS] folios de papel timbrado de uso exclusivamente notarial, de la serie [SERIE], números [NÚMEROS].

Firmas de los comparecientes y firma y signo del Notario.
