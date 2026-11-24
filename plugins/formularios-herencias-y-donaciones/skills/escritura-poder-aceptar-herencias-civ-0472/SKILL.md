---
name: escritura-poder-aceptar-herencias-civ-0472
description: "Escritura de poder para aceptar herencias. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escritura de poder para aceptar herencias

> Formulario **CIV-0472** del plugin **Herencias, testamentos y donaciones** (`formularios-herencias-y-donaciones`) · Civil › Sucesiones y donaciones · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escritura de poder para aceptar herencias» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escritura de poder para aceptar herencias” para mi caso». También puedes invocarla directamente con `/formularios-herencias-y-donaciones:escritura-poder-aceptar-herencias-civ-0472`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-herencias-y-donaciones:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Herencias, testamentos y donaciones) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (8 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] CALLE (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] AÑO (2 veces)
- [ ] DÍA (2 veces)
- [ ] MES (2 veces)
- [ ] NIF/DNI (2 veces)
- [ ] PISO (2 veces)
- [ ] DOMICILIO
- [ ] NOMBRE DEL NOTARIO
- [ ] PROFESIÓN

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

En [LOCALIDAD], mi residencia, a [DÍA] de [MES] De [AÑO]

Ante mí [NOMBRE DEL NOTARIO], Notario/a del Ilustre Colegio de Notarios de [LOCALIDAD] y al efecto de otorgar escritura de poder

COMPARECE/N:

D. [NOMBRE Y APELLIDOS], mayor de edad, casado/soltero, vecino de [LOCALIDAD], con domicilio en [LOCALIDAD], en la calle [CALLE], número [NÚMERO], piso [PISO], letra, con D.N.I. número [NIF/DNI]

D. [NOMBRE Y APELLIDOS], mayor de edad, casado/soltero, vecino de [LOCALIDAD], con domicilio en [LOCALIDAD], en la calle [CALLE], número [NÚMERO], piso [PISO], letra, con D.N.I. número [NIF/DNI]

[ELEGIR UNA OPCIÓN: Intervienen / En nombre propio / En representación]

Tienen

A mi juicio, la capacidad legal necesaria para formalizar esta escritura de PODER PARA ACEPTACIÓN DE HERENCIA y a tal efecto,

EXPONEN

TITULO

Que por medio del presente instrumento público confiere/n poder, tan amplio como fuere necesario en Derecho, a favor de D. [NOMBRE Y APELLIDOS], mayor de edad, de profesión [PROFESIÓN], vecino de [LOCALIDAD], domiciliado en [DOMICILIO], Calle [CALLE], con D.N.I. número [NÚMERO], para que en nombre y representación del compareciente, pueda realizar los actos siguientes con plenitud de competencias, atribuciones y facultades, y con libertad para fijar pactos, cláusulas, disposiciones, determinaciones y declaraciones, de suerte que la apoderada ostente la plena representación de la poderdante sin traba, limitación ni excepción alguna.

FACULTADES

FACULTADES PARA ACEPTAR HERENCIA

Intervenir, judicial o extrajudicialmente, en las herencias intestadas de Don [NOMBRE Y APELLIDOS], fallecido en [LOCALIDAD] el día [DÍA] de [MES] de [AÑO], aceptando legados, donaciones y herencias, éstas simplemente o a beneficio de inventario o con derecho de deliberar o renunciarlos. Solicitar la apertura y protocolización de testamentos ológrafos y otorgados en peligro de muerte. Instar judicial o notarialmente declaraciones de herederos.

Solicitar copias de testamentos, certificaciones del Registro de Estado Civil, del Registro General de Actos de Última Voluntad o cualesquiera otras. Nombrar peritos y contadores.

Aprobar e impugnar inventarios, cuentas, avalúos, balances, liquidaciones, incluso la de la sociedad conyugal, efectuar y formalizar con y en sus bienes de toda clase, divisiones, segregaciones, agrupaciones y cualesquiera modificaciones hipotecarias, pudiendo incluso efectuar operaciones de declaración y rectificación de obra nueva, establecimiento y división en propiedad horizontal, y asimismo colaciones y adjudicaciones, incluso con excesos o defectos de adjudicación, con compensaciones en especie o en metálico, o bien sin ellas, otorgando carta de pago.

Abonar o percibir cantidades por exceso o defecto de adjudicación, estipulando plazos y condiciones. Admitir bienes en pago y para pago. Transigir diferencias. Solicitar prórrogas y cancelación de multas.

Practicar cuanto proceda hasta la terminación de las operaciones particionales. Satisfacer los impuestos correspondientes. Tomar posesión de los bienes muebles e inmuebles adjudicados, inscribiéndolos en los correspondientes Registros de la Propiedad y otorgar las escrituras públicas o privadas que a los expresados fines fueren necesarias

FACULTADES DE REPRESENTACIÓN PROCESAL

A todos los expresados fines, comparecer ante Jueces, Tribunales y Autoridades competentes, de cualquier clase, grado y jurisdicción, incluso el Tribunal Supremo, en actos, asuntos y juicios civiles, criminales, administrativos, contencioso-administrativos, laborales o de cualquier otra clase, siguiéndolos en todas sus incidencias y recursos, incluso de casación, hasta obtener sentencia o resolución firme y su ejecución. Presentar escritos y ratificarlos. Transigir diferencias. Desistir de los procedimientos iniciados. Ejecutar cuanto fuere necesario o conveniente para la defensa judicial de sus intereses, pudiendo nombrar abogados y procuradores y dar a su favor poderes generales para pleitos.

FACULTADES DE DISPOSICIÓN SOBRE LOS BIENES ACEPTADOS

Sólo en relación con los bienes procedentes de dichas herencias, se conceden también facultades para VENDER, a la persona o personas, naturales o jurídicas, en su totalidad o por participaciones indivisas, pudiendo efectuar operaciones de declaración y rectificación de obra nueva, establecimiento y división en propiedad horizontal, segregación, división y cualquier otra modificación hipotecaria, fijando los precios, plazos y condiciones que estime pertinentes, estableciendo las garantías que se estimen oportunas, en caso de aplazar parte del precio, pudiendo posteriormente cobrar y dar recibo de dichos precios aplazados y otorgar carta de pago del mismo, así como cancelar las garantías que se hubiesen establecido, ya sean éstas personales o reales; y asimismo firmar cuantos documentos públicos o privados sean precisos, incluso escrituras de subsanación y rectificación, hasta su total inscripción en el Registro de la Propiedad.

FACULTADES DE APODERAMIENTO

Sustituir, en todo o en parte, este poder, revocar las sustituciones y otorgar otras, cuantas veces fuera oportuno

FACULTAD PARA FIRMAR DOCUMENTOS PÚBLICOS O PRIVADOS

Otorgar y firmar cuantos documentos, públicos y privados, sean precisos para los fines expresados en las cláusulas que anteceden.

Así lo dice y otorga el señor compareciente, quien enterado de su derecho a leer por sí este documento, procedo por su elección a la lectura del mismo, en cuyo contenido se ratifica y firma.

Y yo, el Notario, DOY FE de identificar a los señores comparecientes por medio de sus documentos nacionales de identidad y de todo lo demás contenido en este instrumento público, extendido en cincuenta y un folios de papel sellado, de serie PC, números:

========================================================================
