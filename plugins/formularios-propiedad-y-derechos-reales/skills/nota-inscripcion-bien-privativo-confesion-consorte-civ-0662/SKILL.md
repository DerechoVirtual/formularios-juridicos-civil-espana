---
name: nota-inscripcion-bien-privativo-confesion-consorte-civ-0662
description: "Nota de inscripción de bien privativo por confesión del consorte. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Nota de inscripción de bien privativo por confesión del consorte

> Formulario **CIV-0662** del plugin **Propiedad, posesión, servidumbres e hipotecas** (`formularios-propiedad-y-derechos-reales`) · Civil › Propiedad y derechos reales · normativa revisada el 24-11-2026.

## Qué es

Modelo de asiento de inscripción registral (con la nota marginal de afección fiscal) de una compraventa de vivienda realizada por una pareja casada en gananciales, en la que, por confesión del otro cónyuge, el precio se paga con dinero privativo de uno de ellos y el bien se inscribe con carácter privativo y no ganancial (art. 95.4 del Reglamento Hipotecario).

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Nota de inscripción de bien privativo por confesión del consorte» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Nota de inscripción de bien privativo por confesión del consorte” para mi caso». También puedes invocarla directamente con `/formularios-propiedad-y-derechos-reales:nota-inscripcion-bien-privativo-confesion-consorte-civ-0662`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-propiedad-y-derechos-reales:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Propiedad, posesión, servidumbres e hipotecas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (5 veces)
- [ ] AÑO (4 veces)
- [ ] DÍA (4 veces)
- [ ] IMPORTE (4 veces)
- [ ] IMPORTE EN LETRA (4 veces)
- [ ] LINDERO (4 veces)
- [ ] MES (4 veces)
- [ ] DNI/NIE (3 veces)
- [ ] SUPERFICIE (3 veces)
- [ ] DOMICILIO (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL COMPRADOR/A (2 veces)
- [ ] Nº (2 veces)
- [ ] DATOS DE LA CUENTA
- [ ] ENTIDAD BANCARIA
- [ ] ESTADO CIVIL
- [ ] HORA
- [ ] MINUTOS
- [ ] NOMBRE DEL NOTARIO
- [ ] NOMBRE Y APELLIDOS DEL CÓNYUGE
- [ ] NOMBRE Y APELLIDOS DEL CÓNYUGE QUE CONFIESA
- [ ] NOMBRE Y APELLIDOS DEL VENDEDOR/A
- [ ] Nº DE ASIENTO
- [ ] Nº DE DIARIO
- [ ] Nº DE INSCRIPCIÓN
- [ ] Nº DE ORDEN EN LA DIVISIÓN HORIZONTAL
- [ ] Nº DE PROTOCOLO
- [ ] PLANTA
- [ ] PORCENTAJE
- [ ] REFERENCIA CATASTRAL

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

- Junto a «… satisfechos en autoliquidación. En [LOCALIDAD], a [DÍA] de [MES] del año [AÑO].»: el original solo contenía este asiento registral de ejemplo; es un modelo ilustrativo del contenido que se presenta al Registro de la Propiedad. Comprobar el régimen fiscal aplicable (ITPAJD o IVA/AJD, según la transmisión) y que la confesión de privatividad se haya formulado en la escritura conforme al art. 95.4 del Reglamento Hipotecario y a la normativa vigente de Derecho civil aplicable al régimen económico matrimonial.

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

URBANA: Del edificio en [LOCALIDAD], sito en la calle [DOMICILIO], número [Nº].

NÚMERO [Nº DE ORDEN EN LA DIVISIÓN HORIZONTAL].- VIVIENDA en planta [PLANTA], señalada su puerta con el número [Nº], con una superficie útil de [SUPERFICIE] metros cuadrados, construida de [SUPERFICIE] metros cuadrados y construida con participación en los elementos comunes de [SUPERFICIE] metros cuadrados, que linda: por el frente con [LINDERO], por la derecha con [LINDERO], por la izquierda con [LINDERO] y por el fondo con [LINDERO].- Cuota de participación en elementos comunes: [PORCENTAJE] por ciento.

[OPCIONAL — si ha lugar]

Calificada de vivienda de protección oficial.

Referencia catastral: [REFERENCIA CATASTRAL].

CARGAS: Afecta al impuesto.

TITULAR ACTUAL Y TÍTULO DE ADQUISICIÓN.- D./Dña. [NOMBRE Y APELLIDOS DEL VENDEDOR/A], mayor de edad, [ESTADO CIVIL], con DNI/NIE [DNI/NIE], adquirió esta finca, en pleno dominio, por el título de [ELEGIR: compraventa / otro título que proceda], con carácter privativo, según la precedente inscripción [Nº DE INSCRIPCIÓN], donde constan el resto de sus circunstancias.

TRANSMISIÓN QUE SE INSCRIBE.- Y ahora la VENDE, libre de arrendatarios, al corriente en el pago de impuestos, gastos y contribuciones, a D./Dña. [NOMBRE Y APELLIDOS DEL COMPRADOR/A], en el régimen legal de gananciales con D./Dña. [NOMBRE Y APELLIDOS DEL CÓNYUGE], mayores de edad, vecinos de [LOCALIDAD], calle [DOMICILIO], con DNI/NIF [DNI/NIE] y [DNI/NIE], respectivamente, por el precio de [IMPORTE EN LETRA] euros ([IMPORTE] €), que, según el/la compareciente D./Dña. [NOMBRE Y APELLIDOS DEL CÓNYUGE QUE CONFIESA], se satisface con dinero privativo de su citado cónyuge, y que se confiesa recibido por el vendedor de la siguiente manera: [IMPORTE EN LETRA] euros ([IMPORTE] €) en efectivo metálico, con anterioridad al acto de otorgamiento de la escritura que se inscribe; y [IMPORTE EN LETRA] euros ([IMPORTE] €) en dicho acto mediante la entrega de cheque bancario por dicho importe contra la cuenta [DATOS DE LA CUENTA], que manifiestan los compradores tienen abierta a su nombre en la entidad [ENTIDAD BANCARIA] y del que se acompaña, unido a la matriz de la que motiva este asiento, testimonio por fotocopia.

En su virtud, previo el expresado traslado, inscribo el pleno dominio sobre esta finca a favor de D./Dña. [NOMBRE Y APELLIDOS DEL COMPRADOR/A], por el título de compraventa y con carácter privativo por confesión de su [ELEGIR: esposo / esposa], conforme al art. 95.4 del Reglamento Hipotecario.

Así resulta del Registro y de la escritura autorizada el [DÍA] de [MES] del año [AÑO] por el Notario de [LOCALIDAD], D./Dña. [NOMBRE DEL NOTARIO], protocolo número [Nº DE PROTOCOLO], primera copia de la cual fue presentada a las [HORA] horas y [MINUTOS] minutos del día [DÍA] de [MES] del año [AÑO], según el asiento [Nº DE ASIENTO] del Diario [Nº DE DIARIO]. Pagado el impuesto y archivados el justificante de presentación de la oficina liquidadora correspondiente y la autoliquidación.

En [LOCALIDAD], a [DÍA] de [MES] del año [AÑO].

NOTA MARGINAL DE AFECCIÓN FISCAL:

AFECCIÓN FISCAL.- Esta finca está afecta, por plazo de cinco años a partir de esta fecha, al pago del Impuesto sobre Transmisiones Patrimoniales y Actos Jurídicos Documentados, con motivo de la operación a que se refiere el asiento adjunto, habiendo quedado liberada en la cantidad de [IMPORTE EN LETRA] euros ([IMPORTE] €) (cantidad satisfecha por autoliquidación del Impuesto sobre Transmisiones Patrimoniales y Actos Jurídicos Documentados al que está sujeta la operación), satisfechos en autoliquidación.

En [LOCALIDAD], a [DÍA] de [MES] del año [AÑO].
