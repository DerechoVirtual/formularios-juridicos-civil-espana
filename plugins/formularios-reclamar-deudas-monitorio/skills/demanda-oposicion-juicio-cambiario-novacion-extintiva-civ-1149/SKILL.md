---
name: demanda-oposicion-juicio-cambiario-novacion-extintiva-civ-1149
description: "Demanda de oposición en juicio cambiario por novación extintiva e incumplimiento del contrato. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de oposición en juicio cambiario por novación extintiva e incumplimiento del contrato

> Formulario **CIV-1149** del plugin **Cobrar deudas: monitorio y cambiario** (`formularios-reclamar-deudas-monitorio`) · Civil › Monitorio y cambiario · normativa revisada el 24-11-2026.

## Qué es

Demanda de oposición del deudor en un juicio cambiario fundada en novación extintiva como supuesto de extinción del crédito cambiario (art. 67.2º.4º LCCH) y en incumplimiento contractual radical, porque no se trata de obra ejecutada defectuosamente sino de ‘aliud pro alio’, con citación de un perito arquitecto para acreditar este último extremo.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de oposición en juicio cambiario por novación extintiva e incumplimiento del contrato» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de oposición en juicio cambiario por novación extintiva e incumplimiento del contrato” para mi caso». También puedes invocarla directamente con `/formularios-reclamar-deudas-monitorio:demanda-oposicion-juicio-cambiario-novacion-extintiva-civ-1149`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-reclamar-deudas-monitorio:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Cobrar deudas: monitorio y cambiario) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (11 veces)
- [ ] NÚMERO (5 veces)
- [ ] FECHA (3 veces)
- [ ] IMPORTE
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] Nº DE DOCUMENTO

## Normas que cita el formulario

- art. 824 LEC
- art. 820 LEC
- art. 85.1 LOPJ
- art. 826 LEC
- art. 31 LEC
- art. 824.2 LEC
- art. 1.591 CC
- art. 394 LEC
- art. 347 LEC

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

AL TRIBUNAL

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, que actúa en nombre y representación de [NOMBRE DEL REPRESENTADO/A], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO]; ante el Tribunal comparezco bajo la dirección del Abogado D./Dña. [NOMBRE Y APELLIDOS], colegiado n.º [NÚMERO] y, como mejor proceda en derecho, DIGO:

Que mi mandante ha sido notificado de la demanda y requerido de pago en el Juicio Cambiario seguido en este Tribunal con el n.º [NÚMERO] y promovido por D./Dña. [NOMBRE Y APELLIDOS]

Y dentro del término conferido de diez días, en forma de demanda, según el art. 824 LEC, vengo a formular escrito de oposición a dicha pretensión, en base a los siguientes:

HECHOS

PRIMERO.- Que es cierto lo expuesto en el correlativo del escrito de demanda deducida por D./Dña. [NOMBRE Y APELLIDOS], en cuanto a la existencia de la letra de cambio librada a cargo y aceptada por mi patrocinado, de importe de [IMPORTE] euros, y cuya copia se me ha trasladado.

SEGUNDO.- Que la cantidad cuyo pago se instrumentaba por medio de tal cambial obedecía al precio alzado de una ejecución de obra, pero el crédito cartáceo no es vencido y exigible, porque después de que el tenedor de la letra consideró que la obra había sido terminada, le desengañó mi representada, indicándole las importantes deficiencias que habían de subsanarse y capítulos que habían de rehacerse, y llegaron a un nuevo acuerdo verbal sobre la forma de pago, librando D./Dña. [NOMBRE Y APELLIDOS] una nueva letra de cambio de vencimiento en fecha [FECHA], que sustituía a la de autos. Prueba de ello es el documento que testimonia en nuevo trato y que lleva fotocopia de la otra letra de cambio de la misma cantidad y condiciones, salvo la fecha de pago, que como DOCUMENTO N.º [NÚMERO] acompañamos.

TERCERO.- Con independencia de lo anterior, sin que D./Dña. [NOMBRE Y APELLIDOS], poseedor de las letras, se haya dignado a volver a la obra para acabarla según se proyectó y contrató, no es sólo que tal obra no ha sido recibida a satisfacción por mi representada, sino que constituye una genuina ruina funcional.

A la demostración de este extremo se cuenta con el dictamen del arquitecto director de la obra D./Dña. [NOMBRE Y APELLIDOS], en que se informa de las partidas no ejecutadas, las ejecutadas inserviblemente, y las defectuosas, con el correspondiente juicio técnico y valoración, de fecha [FECHA], acompañado de juego de fotografías diligenciadas notarialmente, que se aporta como DICTAMEN PERICIAL (DOCUMENTO N.º [NÚMERO]).

FUNDAMENTOS DE DERECHO

I.- COMPETENCIA.

La competencia de este Tribunal viene determinada por la interposición de la demanda de juicio cambiario en el domicilio de mi mandante, conforme al art. 820 LEC en relación con lo dispuesto en el art. 85.1º LOPJ.

II.- PROCEDIMIENTO.

Seguido hasta ahora el trámite del proceso especial y documental cambiario, y al haberse presentado escrito de oposición, deberá tenerse en cuenta lo dispuesto en el art. 826 LEC.

III.- POSTULACIÓN Y DEFENSA.

La presente oposición se formula por medio de Abogado y Procurador, al ser preceptiva su intervención, según los arts. 31 y 23 de la LEC.

IV.- FONDO DEL ASUNTO.

El art. 824.2 LEC remite el ámbito de oposición del pretendido deudor cambiario a las causas o motivos de oposición previstos en el art. 67 LCCH, norma que, después de enumerar unas que llama excepciones, acaba disponiendo que frente al ejercicio de la acción cambiaria sólo caben dichas excepciones.

Tradicionalmente se clasifican tales excepciones, que operan como hechos constitutivos de nuestra pretensión opositora, en cambiarias y extracambiarias, las primeras que tocan al negocio de creación o circulación de la letra de cambio, y las segundas a la relación jurídica causal o subyacente.

En cuanto al primer plano, se aduce la novación extintiva como supuesto de extinción del crédito cambiario (art. 67.3.ª LCCH), ya que el crédito articulado en el título inicial fue sustituido por otro, como se refrenda con el documento que acompaño (DOCUMENTO N.º [NÚMERO]), firmado por el demandante, que también es crédito cambiario, si bien todavía no resulta vencido ni exigible.

En cuanto al segundo plano, de los hechos fundados en las relaciones personales entre librador, supuesto acreedor, y mi representada, librada aceptante, se aduce el incumplimiento contractual radical, puesto que no se trata de una obra ejecutada defectuosamente, sino lo que la jurisprudencia denomina un ‘aliud pro alio’, es decir, una prestación de cosa que sirve en absoluto al fin para el que sirvió para causalizar el negocio conmutativo, invocando el precepto del art. 1.591 CCiv. y la batería de preceptos del derecho de obligaciones (arts. 1.091, 1.100, 1.101 y 1.258 CCiv.), y las conclusiones del dictamen pericial del arquitecto superior D./Dña. [NOMBRE Y APELLIDOS], que se adjunta con la demanda.

V.- COSTAS.

El éxito de la pretensión opositora en este juicio cambiario, como declarativo especial, determinará la imposición de las costas a la parte vencida, conforme al art. 394 LEC.

Por lo expuesto,

SUPLICO AL TRIBUNAL

que, teniendo por presentado este escrito, con su documento y dictamen adjuntos, y copia de todo ello, se sirva admitirlo, teniéndome por comparecido y parte en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS], mandando se entiendan conmigo las sucesivas actuaciones; teniéndome por opuesto a la demanda de juicio cambiario deducido contra mi mandante por D./Dña. [NOMBRE Y APELLIDOS], y tras la pertinente tramitación, se solicita se dicte sentencia por la que se estime íntegramente esta oposición, con inmediato alzamiento del embargo preventivo trabado e imposición de costas al demandante.

Es de Justicia que se pide en [LUGAR], a [FECHA].

OTROSÍ PRIMERO DIGO que, conforme a lo prevenido en el art. 826 LEC, solicito la celebración de vista, al ser necesaria para dirimir la controversia fáctica planteada en esta oposición

SUPLICO AL TRIBUNAL que tenga por efectuada la anterior manifestación a los efectos oportunos.

OTROSÍ SEGUNDO DIGO: Que interesa al derecho de esta parte valerse para el acto de la vista de la intervención del perito arquitecto D./Dña. [NOMBRE Y APELLIDOS], autor del dictamen que se adjunta, a fin de que exponga su informe, y responda a las aclaraciones o preguntas que se le formulen, para lo cual se solicita, previa declaración de pertinencia y utilidad por el Tribunal, se le cite en su despacho sito en [LOCALIDAD], con arreglo a las prevenciones del art. 347 LEC.

SUPLICO AL TRIBUNAL que, teniendo por causada la anterior manifestación a los efectos oportunos, se sirva ordenar lo conducente a la práctica del medio probatorio como se pide, según es Justo en lugar y fecha que reitero.

Firma del Abogado/a	Firma del Procurador/a
