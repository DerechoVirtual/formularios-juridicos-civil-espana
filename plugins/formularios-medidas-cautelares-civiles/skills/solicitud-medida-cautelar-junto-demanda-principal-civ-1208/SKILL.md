---
name: solicitud-medida-cautelar-junto-demanda-principal-civ-1208
description: "Solicitud de medida cautelar junto con la demanda principal, modelo general. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud de medida cautelar junto con la demanda principal, modelo general

> Formulario **CIV-1208** del plugin **Medidas cautelares y diligencias preliminares** (`formularios-medidas-cautelares-civiles`) · Civil › Medidas cautelares y diligencias preliminares · normativa revisada el 24-11-2026.

## Qué es

Modelo general de otrosí, incluido en la demanda principal, para solicitar una medida cautelar (embargo preventivo, intervención o administración judicial, depósito, inventario, anotación preventiva de demanda, suspensión de acuerdos sociales, órdenes de cese, etc.), justificando la apariencia de buen derecho, el peligro por la mora procesal y ofreciendo caución.

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud de medida cautelar junto con la demanda principal, modelo general» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud de medida cautelar junto con la demanda principal, modelo general” para mi caso». También puedes invocarla directamente con `/formularios-medidas-cautelares-civiles:solicitud-medida-cautelar-junto-demanda-principal-civ-1208`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-medidas-cautelares-civiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Medidas cautelares y diligencias preliminares) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LUGAR (4 veces)
- [ ] BIENES (3 veces)
- [ ] IMPORTE (3 veces)
- [ ] FECHA (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] ACTIVIDAD
- [ ] DENOMINACIÓN SOCIAL
- [ ] ESPECIFICAR EL OBJETO PRINCIPAL DE LA DEMANDA
- [ ] ESPECIFICAR LA CAUCIÓN, FORMA, CANTIDAD Y SUFICIENCIA
- [ ] HECHO QUE RESULTA DEL DOCUMENTO
- [ ] LOCALIDAD
- [ ] MEDIOS DE PRUEBA
- [ ] NOMBRE Y APELLIDOS O DENOMINACIÓN SOCIAL
- [ ] Nº
- [ ] TÍTULO

## Normas que cita el formulario

- art. 728 LEC
- art. 733.2 LEC
- art. 727 LEC
- art. 590 LEC
- art. 730 LEC

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

OTROSÍ DIGO que en el presente procedimiento se demanda [ESPECIFICAR EL OBJETO PRINCIPAL DE LA DEMANDA]; que, presentándose con el presente escrito justificación documental suficiente del derecho que se ejercita, en base a los arts. 721 y siguientes, y sus concordantes, de la LEC, formulo la petición de medida cautelar consistente en [ESPECIFICAR LA MEDIDA INSTADA, EXPONIENDO LA IDONEIDAD PARA LOS FINES BUSCADOS], por cuanto se considera necesaria para asegurar la efectividad de la tutela judicial que se quiere se otorgue en la sentencia estimatoria que se dicte en este proceso, entendiendo esta representación que, de no acordarse como medida cautelar, puede verse impedida (o dificultada) por situaciones producidas durante la pendencia del proceso.

Concurren los presupuestos que exige el art. 728 LEC para la adopción de la medida cautelar referida: en cuanto a la necesaria apariencia de buen derecho, se deriva de forma más que indiciaria, según exige el apartado 2 del artículo mencionado, de los documentos presentados con este escrito, especialmente del documento n.º [Nº], del que resulta inequívocamente [HECHO QUE RESULTA DEL DOCUMENTO]; por lo que respecta al peligro por la mora procesal, [JUSTIFICAR LA CONCURRENCIA DEL FUMUS BONI IURIS Y DEL PERICULUM IN MORA EN EL CASO CONCRETO].

De conformidad con el art. 732.2, párrafo 3.º, LEC, se propone la práctica de prueba consistente en [MEDIOS DE PRUEBA] para la acreditación de los presupuestos de la medida cautelar, señalándose como documentos los que acompañan la demanda principal. [OPCIONAL — si ha lugar] Si la urgencia u otras razones aconsejan acordar la medida sin audiencia previa del demandado, hágase constar así conforme al art. 733.2 LEC, justificando dichas razones.

A los efectos legales procedentes, se ofrece caución por la suma de [IMPORTE] euros, cantidad que se considera suficiente para responder, en su caso, de los daños y perjuicios que la adopción de la medida cautelar que se interesa pudiera causar en el patrimonio del demandado, que, dada su cuantía, se constituirá [ELEGIR: en metálico, mediante su consignación en la Cuenta de Depósitos y Consignaciones del Tribunal / mediante aval bancario / otra forma admitida] [ESPECIFICAR LA CAUCIÓN, FORMA, CANTIDAD Y SUFICIENCIA]; en cualquier caso, esta parte ofrece prestar la caución que se fije por el Tribunal, de ser ésta superior a la ofrecida anteriormente, y en la forma que se determine.

Por lo expuesto, y al amparo de lo previsto en los arts. 721 y siguientes, y concordantes, de la LEC,

SUPLICO AL TRIBUNAL, que se tengan por hechas las anteriores manifestaciones, y habiendo quedado acreditada cumplidamente la concurrencia de los presupuestos que exige la ley para la adopción de la medida cautelar de [ESPECIFICAR LA MEDIDA DE QUE SE TRATE: EMBARGO PREVENTIVO DE BIENES / INTERVENCIÓN EN LA ADMINISTRACIÓN DE BIENES PRODUCTIVOS / DEPÓSITO DE COSAS MUEBLES / FORMACIÓN DE INVENTARIO DE BIENES / ANOTACIÓN PREVENTIVA DE DEMANDA / CESE PROVISIONAL DE LA ACTIVIDAD O ABSTENCIÓN TEMPORAL DE UNA CONDUCTA O LA PROHIBICIÓN DE INTERRUMPIR O CESAR EN UNA PRESTACIÓN / INTERVENCIÓN O DEPÓSITO DE INGRESOS DE UNA ACTIVIDAD ILÍCITA / DEPÓSITO TEMPORAL DE EJEMPLARES DE LAS OBRAS CON INFRACCIÓN DE LA PROPIEDAD INTELECTUAL O INDUSTRIAL / SUSPENSIÓN DE ACUERDOS SOCIALES], que desde ahora se interesa, previos los trámites legales, incluida la audiencia de las partes, se sirva dictar resolución en la que, declarando justificada la pretensión, se acuerde la adopción de la medida cautelar interesada, disponiendo al efecto:

[ELEGIR LA QUE PROCEDA Y SUPRIMIR LAS DEMÁS:]

— El embargo preventivo sobre los bienes del demandado D./Dña. [NOMBRE Y APELLIDOS], por la cantidad de [IMPORTE] euros de principal, más la de [IMPORTE] euros que, por ahora y sin perjuicio, se calculan para intereses y las costas que se causen.

— La intervención o, en su caso, administración judicial de [BIENES] que se hayan en [LUGAR].

— El depósito de [BIENES] que se haya en [LUGAR].

— La formación de inventario de bienes, con relación a [BIENES], que se hayan en [LUGAR], en las condiciones que el Tribunal disponga.

— Librar mandamiento por duplicado de anotación preventiva de los bienes objeto de medida cautelar.

— El cese provisional de la actividad que viene desarrollando en [LUGAR] D./Dña. [NOMBRE Y APELLIDOS], consistente en [ACTIVIDAD].

— La intervención y depósito judicial de los ingresos procedentes de la actividad ilícita desarrollada por [NOMBRE Y APELLIDOS O DENOMINACIÓN SOCIAL].

— El depósito temporal de los ejemplares de la obra [TÍTULO], a cuyo fin requiérase al demandado para que ponga a disposición judicial, en el lugar que designe, los citados ejemplares.

— La suspensión cautelar del acuerdo adoptado en Junta General de Accionistas de la sociedad [DENOMINACIÓN SOCIAL] el [FECHA].

Es de justicia que pido en [LOCALIDAD], a [FECHA].

NOTAS DE USO

1. Es necesaria la solicitud de parte para la adopción de medidas cautelares. Puede ser planteada tanto por el actor principal como por el reconviniente.

2. El art. 727 de la LEC desarrolla los supuestos de medidas cautelares que en la práctica resultan más usuales: 1.ª embargo preventivo (debe recordarse la conveniencia de señalar bienes del ejecutado sobre los que pueda recaer embargo, y no parece que existan obstáculos para que puedan solicitarse medidas de investigación judicial del patrimonio del deudor previstas en el art. 590 de la LEC); 2.ª intervención o administración judiciales; 3.ª depósito de cosa mueble; 4.ª formación de inventarios; 5.ª anotación preventiva de demanda; 6.ª otras anotaciones registrales; 7.ª órdenes judiciales conminatorias; 8.ª intervención y depósito de ingresos por actividad ilícita; 9.ª depósito temporal de publicaciones; 10.ª suspensión de acuerdos sociales. Además, el apartado 11.ª abre una especie de «cajón de sastre» en el que tienen cabida todas cuantas medidas adecuadas se invoquen para la protección de los derechos, ya aparezcan previstas en las leyes, ya resulten simplemente adecuadas para garantizar la finalidad de la tutela judicial que se persiga.

3. Aun cuando el art. 730 de la LEC establece en su párrafo primero que «las medidas cautelares se solicitarán, de ordinario, junto con la demanda principal», puntualiza a renglón seguido que podrán solicitarse también con anterioridad a la demanda si quien las solicita acredita razones de urgencia o necesidad. En este caso las medidas quedarán sin efecto si no se formula la demanda con las que aparecen relacionadas dentro de los veinte días siguientes a su adopción (límite temporal que no rige en relación con los casos de formalización judicial del arbitraje o de arbitraje institucional).

4. Con posterioridad a la presentación de la demanda solo podrán solicitarse medidas cautelares cuando se acredite el acaecimiento de hechos posteriores a dicha presentación que justifiquen la urgencia o necesidad de su adopción.

5. Puede solicitarse también que la adopción de medidas se realice sin audiencia del demandado.
