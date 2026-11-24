---
name: escrito-proponiendo-declinatoria-falta-jurisdiccion-civ-0879
description: "Escrito proponiendo la declinatoria por falta de jurisdicción debida a inmunidad de jurisdicción. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito proponiendo la declinatoria por falta de jurisdicción debida a inmunidad de jurisdicción

> Formulario **CIV-0879** del plugin **Proceso civil: demandas, contestaciones, prueba y vista** (`formularios-proceso-civil`) · Civil › Escritos procesales (demanda, contestación, prueba, vista) · normativa revisada el 24-11-2026.

## Qué es

ESCRITO DE SOLICITUD DE EXCEPCIÓN DE DECLINATORIA DE INCOMPETENCIA JURISDICCIONAL POR CAUSA DE INMUNIDAD DE JURISDICCIÓN

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito proponiendo la declinatoria por falta de jurisdicción debida a inmunidad de jurisdicción» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito proponiendo la declinatoria por falta de jurisdicción debida a inmunidad de jurisdicción” para mi caso». También puedes invocarla directamente con `/formularios-proceso-civil:escrito-proponiendo-declinatoria-falta-jurisdiccion-civ-0879`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-proceso-civil:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Proceso civil: demandas, contestaciones, prueba y vista) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] PAÍS (2 veces)
- [ ] TIPO DE PROCEDIMIENTO (2 veces)
- [ ] ÓRGANO JUDICIAL (2 veces)
- [ ] AÑO
- [ ] COLEGIO
- [ ] DÍA
- [ ] FECHA
- [ ] LUGAR
- [ ] MES
- [ ] Nº DE COLEGIADO
- [ ] Nº DE COLEGIADO/A
- [ ] Nº DE PROCEDIMIENTO
- [ ] TIPO Y Nº DE PROCEDIMIENTO

## Normas que cita el formulario

- art. 64.1 LEC
- art. 63 LEC
- art. 39 LEC
- art. 63.2 LEC
- art. 64 LEC
- art. 36 LEC

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

D. [NOMBRE Y APELLIDOS] Procurador de los Tribunales, en nombre y representación de D. [NOMBRE Y APELLIDOS], en virtud de apoderamiento apud acta/poder notarial según tengo acreditado en autos de juicio [Nº DE PROCEDIMIENTO] seguidos ante el Tribunal [ÓRGANO JUDICIAL] y asistido de la intervención del Letrado D. [NOMBRE Y APELLIDOS], Abogado del Ilustre Colegio de [COLEGIO], con número de colegiado [Nº DE COLEGIADO/A];

Comparezco ante el Tribunal [ÓRGANO JUDICIAL] en sede de Autos [TIPO Y Nº DE PROCEDIMIENTO] y como mejor proceda en Derecho, DIGO:

Que por el presente escrito, interpongo excepción de declinatoria de jurisdicción en plazo legal, según indica el art. 64.1 de la LEC: «la declinatoria se habrá de proponer dentro de los diez primeros días del plazo para contestar a la demanda, o en los cinco primeros días posteriores a la citación para vista, y surtirá el efecto de suspender, hasta que sea resuelta, el plazo para contestar, o el cómputo para el día de la vista y el curso del procedimiento principal» y todo ello con base a los siguientes

HECHOS

Primero.— Se ha interpuesto demanda de proceso civil contra mi representado el Sr.D., Cónsul del país [PAÍS] en España en procedimiento de [TIPO DE PROCEDIMIENTO], resultando que dicha persona se beneficia de inmunidad de jurisdicción establecida por normas del Derecho Internacional Público. Dicha demanda ha sido trasladada a mi representado con fecha [FECHA] según consta en Autos.

Segundo.— Los hechos a los que se refiere la demanda afectan al ejercicio de la función consular, por lo que están cubiertos por la excepción de inmunidad de jurisdicción ya que no son actos realizados a título particular sino en garantía del normal ejercicio de la función de representación diplomática/consular. Como prueba de los hechos citados se aportan a los autos los siguientes documentos

FUNDAMENTOS DE DERECHO

Primero.—De orden procesal.

Legitimación, capacidad para ser parte y postulación procesal.—Dispone el artículo 63 de la LEC que: «1. Mediante la declinatoria, el demandado y los que puedan ser parte legítima en el juicio promovido podrán denunciar la falta de jurisdicción del tribunal ()». La inmunidad de jurisdicción es apreciable de oficio; sin embargo, también cabe su interposición ex parte, como es el caso, mediante declinatoria, como indica el artículo 39 de la LEC: «El demandado podrá denunciar mediante declinatoria la falta de competencia internacional o la falta de jurisdicción por pertenecer el asunto a otro orden jurisdiccional o por haberse sometido a arbitraje la controversia». Por lo que en su virtud y siendo parte de este procedimiento debidamente postulada (artículos 23.1, 24.131 de la LEC), esta parte ostenta la legitimación activa para promover el presente incidente toda vez que se cumplen los demás requisitos de capacidad y consta la cualidad de demandado de esta representación.

Competencia.—De conformidad con el artículo 63.2 LEC la competencia para resolver sobre la solicitud de declinatoria por carencia de Jurisdicción corresponde «() ante el mismo tribunal que esté conociendo del pleito y al que se considere carente de jurisdicción o de competencia. No obstante, la declinatoria podrá presentarse también ante el tribunal del domicilio del demandado, que la hará llegar por el medio de comunicación más rápido posible al tribunal ante el que se hubiera presentado la demanda, sin perjuicio de remitirsela por oficio al día siguiente de su presentación». Por lo expuesto, y siendo que en este Tribunal se siguen los autos de procedimiento () contra mi representado, es por lo que resulta competente para resolver el presente incidente.

Plazo de interposición.—De conformidad con el artículo 64.1 de la LEC: «la declinatoria se habrá de proponer dentro de los diez primeros días del plazo para contestar a la demanda, o en los cinco primeros días posteriores a la citación para vista, y surtirá el efecto de suspender, hasta que sea resuelta, el plazo para contestar, o el cómputo para el día de la vista y el curso del procedimiento principal»; se interpone el presente escrito dentro del legal plazo y en el momento procesal procedente para resolver de esta cuestión.

Efectos inmediatos.—De conformidad con lo que dispone el artículo 64 de la LEC en su apartado 1 (...) «surtirá el efecto de suspender, hasta que sea resuelta, el plazo para contestar, o el cómputo para el día de la vista, y el curso del procedimiento principal».

Segundo. Sobre la incompetencia jurisdiccional.—Por medio del presente escrito, se solicita como cuestión previa a la resolución del fondo del asunto principal, que este Tribunal resuelva sobre su eventual incompetencia derivada de la concurrencia de inmunidad de Jurisdicción en la parte demandada en el procedimiento principal que acredita esta representación por los documentos acompañados al presente escrito, y a la vista de su resultado, dicte Auto por el cual se inhiba de conocer la acción principal contra mi representado.

En virtud del artículo 36 de la LEC «2. Los tribunales civiles españoles se abstendrán de conocer de los asuntos que se les sometan cuando concurra en ellos alguna de las circunstancias siguientes: 1.ª Cuando se haya formulado demanda o solicitado ejecución respecto de sujetos o bienes que gocen de inmunidad de jurisdicción o de ejecución conforme a las normas del Derecho Internacional Público ()».

Se sigue proceso civil contra mi representado el Sr.D., Cónsul del país [PAÍS] en España en procedimiento de [TIPO DE PROCEDIMIENTO], resultando que dicha persona se beneficia de inmunidad de jurisdicción establecida por normas del Derecho Internacional Público. En concreto, sería de aplicación el artículo 43 párrafo 1 del Convenio sobre relaciones consulares, hecho en Viena el 24 de abril de 1963 (BOE de 6 de marzo de 1970), según el cual «Los funcionarios consulares y los empleados consulares no estarán sometidos a la jurisdicción de las autoridades judiciales y administrativas del Estado receptor por los actos ejecutados en el ejercicio de las funciones consulares». Se han acompañado al presente escrito documental acreditativa y medios de prueba que demuestran que la acción principal afecta al normal ejercicio de la función de representación diplomática/consular, protegida privilegiadamente por el ordenamiento jurídico internacional a través de la subsodicha inmunidad de jurisdicción y/o ejecución.

En su virtud, por todo lo expuesto, SUPLICO AL TRIBUNAL:

Que tenga por presentado este escrito de solicitud de excepción de declinatoria de jurisdicción, junto con sus documentos y copias de todo ello y que tenga a bien admitirlo a trámite, teniendo por interpuesta la excepción de declinatoria de jurisdicción y tras los trámites que procedan, resuelva finalmente el presente incidente de cuestión previa dictando en su día Auto por el cual este Tribunal se inhiba de conocer y seguir los autos del procedimiento principal contra mi representado al acoger la excepción jurisdiccional por inmunidad de mi representado que se acredita y fundamenta por medio del presente escrito.

Otrosí digo: que de conformidad con el artículo 64.1 LEC, previa admisión a trámite del presente incidente, se acuerde de forma automática la suspensión de los Autos de procedimiento principal.

SUPLICO al Tribunal acuerde la supensión de los Autos de procedimiento principal conforme se interesa.

Es Justicia que pido en [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma y número del Letrado [Nº DE COLEGIADO]

Firma del Procurador

========================================================================
