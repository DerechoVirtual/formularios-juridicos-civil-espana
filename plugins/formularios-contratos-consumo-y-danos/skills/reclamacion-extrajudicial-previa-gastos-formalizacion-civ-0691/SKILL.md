---
name: reclamacion-extrajudicial-previa-gastos-formalizacion-civ-0691
description: "Reclamación extrajudicial previa de los gastos de formalización de una hipoteca. Lo redacta con los datos del caso y comprueba las normas con Jurisprudenciator."
---

# Reclamación extrajudicial previa de los gastos de formalización de una hipoteca

> Formulario **CIV-0691** del plugin **Contratos civiles, consumo y reclamación de daños** (`formularios-contratos-consumo-y-danos`) · Civil › Contratos, consumo y responsabilidad civil · normativa revisada el 24-11-2026.

## Qué es

Carta de reclamación extrajudicial previa que un consumidor dirige a la entidad prestamista para solicitar la nulidad de la cláusula de gastos de su préstamo hipotecario y la devolución de los gastos de formalización abonados (notaría, registro, gestoría, impuestos), como requisito de procedibilidad previo a la demanda judicial.

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Reclamación extrajudicial previa de los gastos de formalización de una hipoteca» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Reclamación extrajudicial previa de los gastos de formalización de una hipoteca” para mi caso». También puedes invocarla directamente con `/formularios-contratos-consumo-y-danos:reclamacion-extrajudicial-previa-gastos-formalizacion-civ-0691`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-consumo-y-danos:indice`.

## Qué contiene esta skill

- `formulario.md`: el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `marco.md`: la guía del tema (Contratos civiles, consumo y reclamación de daños) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] Nº DE CLÁUSULA (2 veces)
- [ ] Nº DE PRÉSTAMO (2 veces)
- [ ] AÑO
- [ ] CONCEPTO DE LOS GASTOS
- [ ] DENOMINACIÓN SOCIAL DE LA ENTIDAD PRESTAMISTA
- [ ] DNI/NIE
- [ ] DOMICILIO
- [ ] DOMICILIO DE LA ENTIDAD
- [ ] DÍA
- [ ] IMPORTE
- [ ] MES
- [ ] NOMBRE DEL NOTARIO
- [ ] NOMBRE Y APELLIDOS
- [ ] Nº DE PROTOCOLO
- [ ] RELACIÓN DE DOCUMENTOS
- [ ] TRANSCRIPCIÓN LITERAL DE LA CLÁUSULA DE GASTOS

## Normas que cita el formulario

- art. 439.5 LEC
- art. 439 bis LEC

---

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

- Junto a «…dieran haber sido establecidos en normativa sectorial en desarrollo de la misma.»: comprobar en el texto vigente de la LEC y de la LO 1/2025 la numeración de los arts. 439.5 y 439 bis y de la disposición adicional séptima.
- Junto a «…estamista; los de cancelación, al prestatario. d) Gastos de gestoría: por mitad.»: esta nota resume la doctrina del Tribunal Supremo en la materia según el original; comprobar su vigencia y actualización conforme a la Ley 5/2019, de contratos de crédito inmobiliario, y a la jurisprudencia del TJUE y del Tribunal Supremo posterior, citando la sentencia concreta con su número y fecha antes de usarla.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

NOTAS EXPLICATIVAS

La LO 1/2025 introduce la actividad negociadora como requisito de procedibilidad en el art. 439.5 LEC, para el caso de demandas interpuestas por consumidores y usuarios con objeto de obtener la devolución de las cantidades indebidamente satisfechas en aplicación de cláusulas suelo o cláusulas abusivas insertas en contratos de préstamo o crédito con garantía hipotecaria. En estos supuestos, la admisión de la demanda requerirá que el consumidor justifique una reclamación previa extrajudicial a la persona física o jurídica que realice la actividad de concesión de préstamos o créditos de manera profesional, con el fin de que reconozca expresamente el carácter abusivo de dichas cláusulas, con la consiguiente devolución de las cantidades.

Los requisitos que debe reunir la reclamación extrajudicial y los términos de su realización están previstos en el art. 439 bis LEC, que establece que el consumidor deberá realizar la reclamación previa a la persona física o jurídica que realice la actividad de concesión de préstamos o créditos de manera profesional. El requerido deberá denegarla o admitirla, realizando en este último caso un cálculo de la cantidad a devolver de manera desglosada, incluyendo los intereses, y reconociendo o denegando la nulidad de las cláusulas. El consumidor deberá comunicar si acepta o no la liquidación, procediendo el requerido, en caso de aceptación, a reconocer la nulidad de las cláusulas y a la devolución del dinero. Si considera improcedente la devolución, comunicará los motivos, respecto de los que queda vinculado para el posterior proceso judicial, no pudiendo oponer otros distintos. El plazo máximo para la negociación será de un mes desde la reclamación extrajudicial. El procedimiento extrajudicial se considerará concluido sin acuerdo si el requerido rechaza expresamente la solicitud del consumidor, si transcurre el mes sin contestación y si no existe conformidad entre requerido y requirente. En caso de acuerdo, el requerido tiene un plazo de un mes para abonar las cantidades acordadas; a partir de ese plazo, la cantidad devengará el interés legal incrementado en ocho puntos, quedando además expedita la vía judicial para el consumidor, que estará vedada para las partes durante el tiempo de negociación, teniendo carácter gratuito. La postura de las partes durante este procedimiento extrajudicial previo será valorada por el tribunal para resolver sobre la condena.

Por otro lado, la disposición adicional séptima de la Ley Orgánica 1/2025 establece alternativas sobre el cumplimiento de este requisito procesal en los litigios en materia de consumo, de modo que se entenderá también cumplido el requisito de procedibilidad con la resolución de las reclamaciones presentadas por los usuarios de los servicios financieros ante el Banco de España, la Comisión Nacional del Mercado de Valores y la Dirección General de Seguros y Fondos de Pensiones en los términos establecidos por el artículo 30 de la Ley 44/2002, de 22 de noviembre, de Medidas de Reforma del Sistema Financiero, o por haber acudido a alguno de los procedimientos a que se refiere la Ley 7/2017, de 2 de noviembre, por la que se incorpora al ordenamiento jurídico español la Directiva 2013/11/UE, del Parlamento Europeo y del Consejo, de 21 de mayo de 2013, relativa a la resolución alternativa de litigios en materia de consumo, o los que pudieran haber sido establecidos en normativa sectorial en desarrollo de la misma.


### Flujo

1. **Paso 0**: comprueba Jurisprudenciator (arriba).
2. Lee `formulario.md` entero y la parte de `marco.md` que afecte al caso. Limítate a la materia de este formulario: no añadas contenido ajeno a él.
3. Pide los datos de la lista en una sola tanda. Si un dato aparece varias veces, aclara a qué persona o acto corresponde cada vez. Lo que el usuario no sepa se queda como hueco visible con su etiqueta (p. ej. [FECHA]).
4. Resuelve cada [ELEGIR …] y cada [OPCIONAL …] según los hechos, y sustituye cualquier indicación entre paréntesis del formulario («(se describirá…)», «(indicar…)») por el contenido que corresponda. Redacta las partes que dependen del caso (hechos, motivos, descripción de bienes).
5. Aplica los avisos de actualización en el lugar que indican. Comprueba con `buscar_articulo` cada norma citada; si alguna ha cambiado, usa la redacción vigente. Si citas jurisprudencia, localízala con `buscar_sentencias` o `buscar_por_cita` y léela con `leer_sentencias`.
6. Antes de entregarlo, pasa `verificar_escrito` con las frases que citan normas o sentencias y corrige lo que señale.
7. **Documento final = el formulario tal cual, rellenado y limpio.**
   - Empieza exactamente por la primera línea de `formulario.md` y sigue su estructura y su orden hasta la firma.
   - No pongas en el documento título, nombre del formulario o de la skill, código, encabezados, «Para qué sirve», leyendas, avisos, notas de uso, comentarios ni explicaciones. Tampoco marcas [ELEGIR…] u [OPCIONAL…]: ya están resueltas.
   - Formato Word (.docx, con la skill de Word disponible): **Times New Roman 12 pt** en todo el documento, **interlineado 1,15**, **texto justificado**, márgenes de 2,5 cm. Los rótulos del formulario (REUNIDOS, CLÁUSULAS, HECHOS, SUPLICO…) en su propia línea y en negrita, sin cambiar su texto.
8. En el chat (nunca dentro del documento): datos pendientes, partes redactadas por ti, normas y sentencias comprobadas con Jurisprudenciator (y, si algún dato sale de internet, cuál y su enlace) y, si es un escrito judicial o administrativo, el plazo y el órgano ante el que se presenta.

El resultado es un borrador para que lo revise un profesional antes de usarlo.
