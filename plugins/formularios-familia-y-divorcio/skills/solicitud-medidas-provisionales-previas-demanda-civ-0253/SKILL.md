---
name: solicitud-medidas-provisionales-previas-demanda-civ-0253
description: "Solicitud de medidas provisionales previas a la demanda en un proceso de menores. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud de medidas provisionales previas a la demanda en un proceso de menores

> Formulario **CIV-0253** del plugin **Familia: divorcio, custodia, pensiones y parejas** (`formularios-familia-y-divorcio`) · Civil › Familia · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud de medidas provisionales previas a la demanda en un proceso de menores» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud de medidas provisionales previas a la demanda en un proceso de menores” para mi caso». También puedes invocarla directamente con `/formularios-familia-y-divorcio:solicitud-medidas-provisionales-previas-demanda-civ-0253`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-familia-y-divorcio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Familia: divorcio, custodia, pensiones y parejas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (10 veces)
- [ ] Nº (6 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] AÑO (2 veces)
- [ ] CALLE (2 veces)
- [ ] ENTIDAD BANCARIA (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] PISO (2 veces)
- [ ] PUERTA (2 veces)
- [ ] SEDE (2 veces)
- [ ] FECHA
- [ ] MES
- [ ] NOMBRE DEL MENOR

## Normas que cita el formulario

- art. 771.2 LEC

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

### Avisos de actualización (2) — se aplican en el texto, nunca se copian en el documento

- Junto a «…MILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE]»: Denominación legal: Sección de Familia, Infancia y Capacidad. Si no existe en el partido, conoce la Sección Civil o la Única (art. 86.3-4 LOPJ). Fuente: LOPJ arts. 84.2.a) y 86 (redacc. LO 1/2025, BOE-A-2025-76).
- Junto a «…n [NOMBRE Y APELLIDOS] ante la Sección Civil del Tribunal de Instancia de [SEDE]»: Un solo TI por partido judicial (art. 84.1 LOPJ): sobra «de los de». Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

Proceso de menores

A LA [ELEGIR: SECCIÓN DE FAMILIA, INFANCIA Y CAPACIDAD / SECCIÓN CIVIL] DEL TRIBUNAL DE INSTANCIA DE [SEDE]

Don [NOMBRE Y APELLIDOS], Procurador de los Tribunales, en la representación que ostento de Doña [NOMBRE Y APELLIDOS], según acredito mediante escritura de poderes que acompaño para su unión a los autos por medio de testimonio, previo cotejo y devolución del original, y bajo la dirección Letrada de Don [NOMBRE Y APELLIDOS] ante la Sección Civil del Tribunal de Instancia de [SEDE] que por turno de reparto corresponda (o Sección de Familia, Infancia y Capacidad) comparezco y como mejor proceda en Derecho, DIGO:

Que solicito adopción de MEDIDAS PROVISIONALES PREVIAS a la demanda de guarda y custodia del hijo menor D. [NOMBRE Y APELLIDOS] y reclamación de alimentos que esta parte se propone entablar contra el otro progenitor Don [NOMBRE Y APELLIDOS], vecino de la localidad [LOCALIDAD], con domicilio en calle [CALLE], núm. [Nº], piso [PISO], puerta [PUERTA], solicitud que fundo en los siguientes

HECHOS

PRIMERO.- Mi representada y D. [NOMBRE Y APELLIDOS], han venido conviviendo en pareja desde el año [AÑO], teniendo un hijo común [NOMBRE DEL MENOR], nacido el día [FECHA], del mes de [MES], del año [AÑO], por consiguiente, menor de edad, según acredito mediante certificación del Registro civil de la localidad de [LOCALIDAD], que acompaño como documento número uno.

SEGUNDO.- El domicilio está sito en la localidad de [LOCALIDAD], calle [CALLE], núm. [Nº], piso [PISO], puerta [PUERTA], el cual pertenece a ambos progenitores por mitad.

En dicho domicilio conviven aún ambos progenitores y el hijo común, aunque en situación extrema, que se pasa a exponer.

TERCERO.- En efecto, sin perjuicio de cuanto se exponga en la demanda principal que en estos momentos está en fase de elaboración y que esta parte se compromete a presentar en el plazo establecido en los artículos 104.2 del Código civil y 771.5 de la Ley de Enjuiciamiento civil, baste decir que en los últimos meses la convivencia se ha deteriorado gravemente, con numerosas discusiones en el propio domicilio conyugal y en presencia del propio hijo común, principalmente como consecuencia de que el demandado está observando una conducta desordenada, llegando al domicilio a altas horas de la madrugada, la mayor parte de las veces en estado ebrio, y sin aportar cantidad alguna para la alimentación y gastos diarios desde hace varios meses. El hijo común está enormemente afectado por lo sucedido, y corre peligro su equilibrio emocional. Acompaño, como documento núm. [Nº], certificación de psiquiatra infantil que atiende al menor.

En consecuencia, es necesario que se decreten urgentemente las medidas prevenidas en el art. 771.2 de la LEC, atribuyendo a mi representada la guarda y custodia del menor, y a madre e hijo el uso de la vivienda común y de su correspondiente ajuar.

CUARTO.- El padre cuenta con importantes medios económicos, los cuales consisten, básicamente, en los siguientes:

Por otra parte, los medios económicos de los que dispone mi representada son eventuales dada la precariedad del trabajo, estando retribuido de manera insuficiente, dada su falta de cualificación profesional, su edad, y su estado de salud; a pesar de lo cual, procura, dentro de lo que su estado de salud le permite, realizar algunos trabajos de limpieza de carácter doméstico, en casas particulares, que le proporcionan algunos ingresos con los cuales apenas pueden subsistir madre e hijo. Acompaño como documento núm. [Nº], certificación médica sobre estado de salud de mi representada.

QUINTO.- Los gastos ordinarios del menor son los siguientes:

Por todo ello se solicita que el padre satisfaga en concepto de contribución a las cargas familiares y alimentos para el menor la cantidad de [IMPORTE] euros mensuales (- euros/mes), dentro de los cinco primeros días de cada mes, a ingresar en la cuenta núm. [Nº] que Doña [NOMBRE Y APELLIDOS] tiene abierta en la entidad financiera [ENTIDAD BANCARIA], actualizándose anualmente, cada mes de enero, conforme al Índice Oficial de Precios al Consumo para el conjunto Nacional.

A los anteriores Hechos le son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

I.-Legitimación activa y pasiva. La ostentan las respectivas partes en su condición de cónyuges, en relación a los hechos y pretensiones formuladas. En especial, invoco el artículo 104 del Código civil y artículos 770.6 y 771.1 de la Ley de Enjuiciamiento Civil.

II.-Competencia. Artículo 771.1 de la Ley de Enjuiciamiento Civil.

III.- Procedimiento. Artículo 770.6 y 771.1 de la Ley de Enjuiciamiento Civil.

IV.-Intervención del Ministerio Fiscal: Artículo 749 de la LEC

V.-Demás normas concordantes y de aplicación: iura novit curia.

En su virtud,

SUPLICO AL TRIBUNAL: Que tenga por presentado este escrito con los documentos acompañados y sus copias; por interpuesta por el Procurador que suscribe, con quien se entiendan las sucesivas diligencias, en nombre y representación de Doña [NOMBRE Y APELLIDOS], con devolución de la escritura de poderes una vez quede testimonio en autos, demanda de MEDIDAS PROVISIONALES PREVIAS de contra Don [NOMBRE Y APELLIDOS]; y previos los trámites pertinentes y con intervención del Ministerio Fiscal, dicte Auto por el que se acuerden las siguientes medidas:

a.- Atribución a la madre de la guarda y custodia del menor, sin perjuicio de un régimen de comunicación y estancia entre padre e hijo, adecuado a las circunstancias del caso.

b.- Atribución a la madre y al hijo del matrimonio del uso de la vivienda común y ajuar.

c.- La obligación del padre de satisfacer en concepto de alimentos para el menor la cantidad de [IMPORTE] euros mensuales a pagar dentro de los cinco primeros días de cada mes, a ingresar en la cuenta núm. [Nº] que Doña [NOMBRE Y APELLIDOS] tiene abierta en la entidad financiera [ENTIDAD BANCARIA], actualizándose anualmente, conforme al Índice Oficial de Precios al Consumo para el conjunto Nacional.

OTROSÍ DIGO: Que dada la urgencia del caso, y la situación de extrema tensión en que vive la familia, solicito, de conformidad con lo previsto en el artículo 771.2 párrafo segundo de la Ley de Enjuiciamiento Civil, que en la misma resolución en que se cite a las partes para la celebración de la comparecencia, se acuerde la atribución a mi representada de la guarda y custodia del menor, y la atribución a madre e hijo del uso de la vivienda y ajuar común, así como del animal de compañía, sin perjuicio de las demás medidas que proceda dictar, una vez celebrada la comparecencia.

Por lo expuesto

SUPLICO AL TRIBUNAL: Que acuerde de inmediato, en la misma resolución en que se cite a las partes para la comparecencia, las medidas de atribución a la madre de la guarda y custodia del menor y de atribución de uso a madre e hijo de la vivienda y ajuar común.

Es justicia que insto en [LOCALIDAD]

========================================================================
